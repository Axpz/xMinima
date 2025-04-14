---  
layout: home  
title: "Hybrid cloud computing - Github CICD pipelines"  
date: 2025-01-15 23:18:15 +0800  
lastupdated: 2025-01-15 23:18:15 +0800  
categories: k8s  
tags: [kubernetes,k8s,k3s,golang,cloud,ai]
---
# 混合云数据中心之CICD
  
这是我要搭建的第一个服务：个人blog的CI/CD - 持续集成和持续部署

## 目标  
当xMinima repo有新的提交的时候，会自动触发流水线执行以下任务
  - 自动构建（Build）
  - 集成与测试（Integration & Testing）
  - 自动部署到 axpz.github.io

## Solutions
  
1. 使用Github Actions, 从企业级开发来讲，我推荐使用Github Actions。

    Pros: 
      易用性：即开即用，集成度高，支持大量插件和模板。
      维护性低：由 GitHub 官方管理，无需自行维护基础设施。
      社区支持：活跃社区，有大量教程和最佳实践。

    Cons:
      成本：对于大型企业和高频执行，费用较高。
      灵活性受限：不适合特别复杂或定制化的 CI/CD 流程。
  
2. 自建pipeline，从full control和 cost down的角度，我建议自建pipeline。

    Pros:
      完全控制：可以根据需求高度定制和优化。
      成本控制：对于大规模任务，长期来看更具经济性。
      安全性：代码和数据完全掌控在内部网络中。
      
    Cons:
      开发/维护成本高：需要专门团队维护 CI/CD 基础设施。
      上手难度：初期搭建和优化可能较复杂，耗时较长。
  
别忘了我们的关键词是cost-effective。那上一篇文章中，我们已经自行搭建了基础设置，那我们自行build pipeline自然是顺理成章的事情，这个不难，至少对我们来讲。

## Implementation：GitHub 自建 CI/CD 流水线设计与实施方案

### 整体架构  
整体架构分为四个部分  
1. Webhook 事件触发：
   - GitHub 触发 Webhook。  
2. Ingress 路由：
   - 请求通过 Kubernetes Ingress 转发到服务。  
3. 事件处理：
   - 服务解析事件并触发流水线。  
4. 流水线执行：
   - 自动构建、测试与部署。  
整体架构图
![github cicd](/assets/images/high-level-arch-github-cicd.png)
#### 1. Webhook 事件订阅  
通过注册 **GitHub Webhook** 接收以下事件：
- **pull_request**：用于监控 Pull Request 的状态，如创建、更新、合并等。
- **push**：用于监控代码分支的变更（如 `git push` 或 `git push --force`）。

**功能：**
- 实时监听仓库的关键事件。
- 根据触发条件将事件传递给处理服务。

**实现：**
![github webhook](/assets/images/github-webhook-cicd.png)

---

#### 2. Ingress 路由配置  
使用 **Kubernetes Ingress** 将外部请求路由到 **GitHub Agent Server**。

**配置要点：**
- 定义 Ingress 规则：将 GitHub Webhook 请求（如 `/github/webhook`）路由到服务的特定端点。
- [Options] 启用 HTTPS 支持：通过证书管理（如 Cert-Manager）实现安全通信。

```yaml  
apiVersion: traefik.containo.us/v1alpha1  
kind: IngressRoute  
metadata:
  name: github-agent-server
  namespace: default  
spec:
  entryPoints:
  - web
  routes:
  - kind: Rule
    match: Host(`74.121.149.207`) && PathPrefix(`/github/webhook`)
    services:
    - name: github-agent-server
      port: 80
---  
apiVersion: v1  
kind: Service  
metadata:
  name: github-agent-server  
spec:
  selector:
    app: github-agent-server
  ports:
    - protocol: TCP
      port: 80
      targetPort: 8080

```

---

#### 3. Event 处理与流水线触发  
服务接收 Webhook 事件后，执行以下操作：  
1. **解析事件内容**：
   - 提取关键信息（如事件类型、分支、Pull Request 状态等）。  
2. **检测特定条件**：
   - Pull Request 合并（`pull_request merged`）。
   - 强制推送（`git push --force`）。  
3. **触发流水线 Jobs**：
   - 满足条件时启动相关流水线任务。

---

#### 4. 流水线 Jobs  
流水线的主要任务包括以下阶段：

##### 自动构建（Build）
- 编译代码，生成构建产物（如前端资源、可执行文件等）。
- 确保构建无错误。

##### 集成与测试（Integration & Testing）
- 执行单元测试、集成测试和端到端测试。
- 生成测试报告，确保代码质量。

##### 部署到 axpz.github.io
- 将构建产物部署到 `axpz.github.io`，实现自动化发布。
- [day2] 支持版本控制与回滚机制。
  
创建secret存放github private key
```bash  
kubectl create secret generic github-ssh-key-secret --from-file=id_rsa=/home/ubuntu/.ssh/id_isa --from-file=known_hosts=/home/ubuntu/.ssh/known_hosts
```
  
对于不同的hardware architecture，可能需要自建一个docker image
```bash  
cat <<EOF > Dockerfile  
FROM ruby:latest  
RUN gem install jekyll bundler jekyll-seo-tag csv base64  
EOF
  
cat <<EOF > Dockerfile2  
FROM ruby:3.2-alpine
  
ENV BUNDLER_VERSION=2.4.13 \
    JEKYLL_VERSION=4.3.2 \
    BUILD_DEPS="build-base gcc libxml2-dev libxslt-dev readline-dev" \
    RUNTIME_DEPS="tzdata bash"
  
RUN apk add --no-cache $BUILD_DEPS $RUNTIME_DEPS && \
    gem install jekyll:$JEKYLL_VERSION bundler:$BUNDLER_VERSION jekyll-seo-tag csv base64 && \
    apk del $BUILD_DEPS && \
    rm -rf /var/cache/apk/* /usr/lib/lib/ruby/gems/*/cache/*
  
WORKDIR /app
  
CMD ["jekyll", "--help"]  
EOF

  
docker build -t jekyll-cicd:4.3.2 .  
docker save -o /tmp/jekyll-cicd.tar jekyll-cicd:4.3.2  
ctr -n=k8s.io images import /tmp/snap-private-tmp/snap.docker/tmp/jekyll-cicd.tar
```

```yaml  
apiVersion: batch/v1  
kind: Job  
metadata:
  name: cicd-job  
spec:
  template:
    spec:
      containers:
      - name: cicd-container
        image: jekyll-cicd
        imagePullPolicy: IfNotPresent
        command:
        - /bin/bash
        - -c
        - |
          set -ex
          git config --global user.name "Axpz"
          git config --global user.email "axpzhang@gmail.com"

          echo "Cloning repository..."
          git clone git@github.com:Axpz/xMinima.git
          echo "Running release script..."
          cd xMinima 
          bash -x script/bootstrap
          commitMsg=`git log -1 --pretty=%B`
          bash -x script/release.axpz.github.io "$commitMsg"
        env:
        - name: GIT_SSH_COMMAND
          value: "ssh -o StrictHostKeyChecking=no"
        volumeMounts:
        - name: github-ssh-keys
          mountPath: /root/.ssh
          readOnly: true
      restartPolicy: Never
      volumes:
      - name: github-ssh-keys
        secret:
          secretName: github-ssh-key-secret # 请确保预先创建了此 Secret
          defaultMode: 0600
  backoffLimit: 0 # 任务失败后不重试
  ttlSecondsAfterFinished: 60 # 在任务完成 60 秒后删除 Job
```


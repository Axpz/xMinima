---
layout: home
title: "Kubernetes and Go R&D in VMware - Xianping"
date: 2024-11-03 14:43:43 +0800
lastupdated: 2024-11-03 14:43:43 +0800
categories: k8s
tags: [k8s,gRPC,PostgreSQL,golang,cloud,ai]
---

- Golang/Python/c/c++/Bash
- Docker/Kubernetes/PostgreSQL/gRPC
- Git/Jenkins/Gitlab

2023.11-至今     	VMware					Kubernetes & Go Engineer   

	项目经历：TMC Self-managed (私有云管理平台)的开发维护。
该平台是 SaaS 平台的企业版，部署在企业的私有环境中，覆盖了网络、计算、存储等全栈资源。通过这种部署模式，企业可以最大程度地实现自主管理，确保数据安全和资源的高效利用。但由于是私有环境部署，企业在使用时将失去多云管理的能力。
1.	技术栈：Go/Python, Gitlab, Kapp-controller, ytt, Prometheus，AD/LDAP/OIDC
2.	职责：
­	独立负责Kubernetes cluster CRUD生命周期管理。
o	去掉部分SaaS功能：不再支持Azure/AWS，仅支持TKGm/TKGs vSphere。  
o	编写自动化测试，完成自动化流水线开发测试，保证功能的独立完整性。  
o	共完成4个版本的交付：参加bug bash、CVE分析、软件发布文档编写等。  
­	重新设计并开发微服务的证书管理。彻底解决服务证书和根证书手动rotate问题(每三个月重启)。  
证书管理分为服务证书和根证书管理，其中服务证书管理分为外部流量(south-north)和内部流量(east-west)证书管理。详见certificate management on TMC self-managed.  
o	根证书分为内部根证书和外部根证书，内部根证书为self-signed，提供给cert-manager签发使用，外部根证书会分发到信任的客户端(如agent)做信任验证。  
o	内部服务证书统一使用cert-manager管理(域名/有效时间/重新生成时间等签发)。  
o	外部服务证书分为导入证书和cert-manager自管理的证书。  
o	引入第三方服务reloader，支持自动重启服务以消费renew的证书。  
­	¬¬¬参与installer开发。Installer把所有依赖的docker image重新打包并放到本地的registry中以适配air-gap环境安装、运行和维护。  
o	基于Gitlab CI/CD完成超过100个repo的nightly持续集成和持续部署，结合自动化测试，解放了大量人力测试。  
3.	主要成就：  
­	引入TMC self-manage项目到北京团队，并由北京团队完全负责(现在已经交接给印度团队)。  
­	解决了大量客户问题：主要包括证书问题、第三方认证问题(OIDC/AD/LDAP)。    

2022.04-2023.11		VMware 						Kubernetes & Go Engineer  
主要工作内容包括a)功能设计开发；b)版本发布；c)自动化流水线的开发和维护；d)客户问题技术支持。

	项目经历：Kubernetes多云(AWS/Azure/VMware)集中管理平台TMC的开发维护。
TMC 是一个专为多云环境设计的 Kubernetes 资源统一管理 SaaS 平台，能够在跨多个云平台和 Kubernetes 集群之间实现一致的运维管理。该平台基于云原生控制器架构开发，采用微服务模式，通过扩展标准的 Kubernetes 资源来提供与标准Kubernetes一致的设计和用户体验，支持跨云环境的高效管理和操作。
1.	技术栈：Go, Kubernetes, Docker, PostgreSQL, Terraform, Jenkins, Prometheus  
2.	职责：  
参与核心功能模块设计开发。核心功能模块是Kubernetes集群的生命周期管理, 即Cluster/nodepool的创建、删除、修改、升级等功能。LCM模块通过调用远端接口实现。  
­	实现k8s default storage class的支持：a)调用vSphere API 读取storage class/policy并通过agent返回到LCM，同时存储到数据库中; b) 渲染数据到UI并提供查询规则供用户交互使用; c) 设置Kubernetes集群的默认存储类。  
­	集群CA证书支持：通过修改集群的CRD, 将CA证书植入到节点上，其中多云环境中植入到containerd配置文件中，而TKGS环境中植入到系统目录下。  
­	支持proxy设置：即在创建cluster集群的时候把代理注入到集群当中。其中包括集群agent代理和工作负载代理设置。  
­	提供下游terraform设计实现方案，并合作完成API开发测试。  
­	主导(支持)软件版本发布，支持上游Kubernetes新版本(功能)发布，主要工作：升级最新的API、支持新功能和其测试验证。  
­	软件CVE修复，维护自动化测试的CVE扫描工具(based on Trivy)。  
­	编写功能的自动化测试代码，维护自动化流水线，保证功能测试的正确性和覆盖的完整性。  
3.	主要成就：
­	主导1.6大版本的发布: 与团队其他两名成员紧密合作，完成了版本发布工作。主要负责升级至最新 API 并验证新功能，确保无功能回退 (regression) 的问题。同时，参与自动化流水线的开发、测试及维护，确保发布流程的高效和稳定。  
­	重新设计实现了代理、证书和默认存储功能无缝并屏蔽不同provider的差异，为self-managed版本提供了保障。  



https://docs.vmware.com/en/VMware-Tanzu-Mission-Control/1.4/tanzumc-sm-install/index-sm-install.html

![tmc-self-managed-arch](/assets/images/tmc-self-managed-arch.png)  

![tmc-self-managed-arch-flatten](/assets/images/tmc-self-managed-arch-flatten.png)  

## Support enable/disable default storage class

- High level design
![alt text](/assets/images/en-disable-default-storage-class.png)  
- One pager for design and implementation *[here](/assets/images/Support+enable_disable-default-storage-class.doc)*
- Video *[demo here](https://www.douyin.com/video/7303145324061805834)*

## Certificate management on TMC self-managed

- Overview
![alt text](/assets/images/cert-mgmt-overview.png)  
- One pager for design and implementation *[here](/assets/images/One+pager_+[TMC+SM]+Certificates+management+on+TMC+self-managed.doc)*

### Auto reload TLS certificate secrets for stack services

- Overview  
The TLS secret will be automatically renewed by cert-manager before it expires; however, the containers require an explicit restart to utilize the updated certificate. This could become an issue if customers forget to restart the service pods within the renewal duration.
- Design and implementation
- Demo *[pitch](/assets/images/Auto-reload-TLS-certificate-secrets-for-stack-services.pptx)* and recordings:
  - Upgrade. Performing rolling-update for cert renewal. New duration/renewBefore configuration. *[here](https://www.douyin.com/video/7423428104548371752)*  
  - Functionality test to SV register and WC creation. *[here](https://www.douyin.com/video/7423428378901892367)*  

### Custom trusted CA enhancement for TKG workload cluster

- High level design
![solution](/assets/images/custom-ca.png)
- Design and implementation *[here](/assets/images/Custom-CAs-enhancement-for-TKG-workload-cluster.docx)*

### Custom proxy for TKG workload cluster

- High level architecture
![high level architecture](/assets/images/high-level-proxy-arch.png)  
- Detailed 

## LCM(life cycle management) support of Terraform  

- Overview
![alt text](/assets/images/lcm-of-terraform.png)
- Design and implementation  *[here](/assets/images/LCM+support+of+Terraform.doc)*  and  *[here](/assets/doc/Support+ZERO+nodepool+in+CREATE_UPDATE+cluster+API+SPEC.doc)*.  

## Software version release and Automation pipeline maintenance

- Lead(participate) for managing software version releases.  
Lead the release of TKG 1.6 lifecycle management support
TKG 1.6 is a major release, and as downstream support, we need to cover all new features, including interface upgrades and feature validation, with a focus on over 200 P0 features.

- Automation pipeline maintenance.  
  - Promotion pipeline for  
    - unstable -> stable -> canary -> production
  - Branches management ![release lifecycle and auto branching management](/assets/images/auto-branch-cut.png)  
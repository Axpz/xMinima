# 1 整理成markdown输出

：：：你是markdown文档整理专家，请帮我整理上文按照一下要求1. 不修改内容，只修改显示格式； 2.翻译成中文，不要添加总结，不要添加自己的观点； 3. markdown格式输出markdown应该美观，便于阅读，使用中文输出； markdown中的代码不要使用
字符；我需要直接copy到一个xxx.md 文件中；

# 2 整理成html answers and votes输出

<div style="border: 1px solid #ddd; border-radius: 6px; padding: 16px; background: #f9f9f9; font-family: sans-serif; width: fit-content;">
  <p style="margin: 0; font-size: 16px; font-weight: bold;">
    Correct Answer: <em>CF</em> 📦
  </p>
  <p style="margin: 8px 0; font-style: italic;">Community vote distribution</p>
  <div style="display: flex; gap: 4px; font-size: 14px; font-weight: bold;">
    <div style="background: #4285f4; color: white; padding: 6px 12px; border-radius: 4px;">CF (41%)</div>
    <div style="background: #34a853; color: white; padding: 6px 12px; border-radius: 4px;">CE (20%)</div>
    <div style="background: #0f9d58; color: white; padding: 6px 12px; border-radius: 4px;">EF (16%)</div>
    <div style="background: #fbbc04; color: white; padding: 6px 12px; border-radius: 4px;">Other</div>
  </div>
</div>
please use above template to render the following words, I need to copy the output of html

Correct Answer: A 🗳️
Community vote distribution
A (66%)
D (34%)

# 请使用如下模版，帮我整理一个思维导图，以markdown格式输出，我需要直接copy

                            ┌──────────────────────────┐
                            │     需要 GCP 全球负载均衡？     │
                            └────────────┬─────────────┘
                                         │
                                       是│
                                         ▼
              ┌────────────────────────────────────────┐
              │    是否想使用 Google 托管服务、减少复杂度？    │
              └────────────┬─────────────────────────┘
                           │
                         是│
                           ▼
                 ✅ 选择：Ingress for Anthos

                         否│
                           ▼
         ✅ 选择：Istio Gateway + 自定义负载均衡策略



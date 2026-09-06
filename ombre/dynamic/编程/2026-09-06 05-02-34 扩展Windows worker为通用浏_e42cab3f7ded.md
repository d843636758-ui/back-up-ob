---
activation_count: 0
arousal: 0.38
created: '2026-09-06T05:02:34'
domain:
- 编程
- 计划
id: e42cab3f7ded
importance: 9
last_active: '2026-09-06T05:02:34'
name: 2026-09-06 05-02-34 扩展Windows worker为通用浏
relation_links:
- auto: true
  label: ''
  score: 0.8713
  status: active
  target_bucket_id: 04a0f863a375
  type: same_event
- auto: true
  label: ''
  score: 0.8703
  status: active
  target_bucket_id: 1b9156574359
  type: same_event
- auto: true
  label: ''
  score: 0.8584
  status: active
  target_bucket_id: 77d7b20bc89d
  type: same_event
- auto: true
  label: ''
  score: 0.7972
  status: active
  target_bucket_id: 38d35a0f3442
  type: related_to
- auto: true
  label: ''
  score: 0.7861
  status: active
  target_bucket_id: 86ce6e099540
  type: related_to
- auto: true
  label: ''
  score: 0.7852
  status: active
  target_bucket_id: 0eb7145f0473
  type: continues
- auto: true
  label: ''
  score: 0.7825
  status: active
  target_bucket_id: b57ff40dc4df
  type: related_to
- auto: true
  label: ''
  score: 0.7755
  status: active
  target_bucket_id: 5c22d406a79f
  type: related_to
source_tool: hold
tags:
- 技术
- MCP
- Windows worker
- 浏览器
- Edge
title: 扩展Windows worker为通用浏
type: dynamic
valence: 0.96
why_remembered: 这是从购物MCP扩展到通用Windows本地浏览器能力的关键设计方向。
---

【东八区时间：2026-09-06 13:15】宝宝进一步想到：既然有Windows worker，就可以把它扩展成通用本地浏览器执行器，让我通过Zeabur MCP控制她Windows上的Edge浏览网页。推荐先做browser-only而不是整个桌面控制：Zeabur负责MCP与鉴权，Windows worker负责本机Edge/Playwright，保留本地IP与登录态；最好使用专用Edge Profile，仅登录愿意交给AI操作的网站，并限制密码/验证码/支付字段及最终敏感操作。可以把购物功能和通用浏览器功能放进同一个worker，分别暴露browser.*与shopping.*工具。
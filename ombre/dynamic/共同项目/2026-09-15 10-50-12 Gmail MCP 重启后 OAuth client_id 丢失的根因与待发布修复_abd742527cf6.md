---
activation_count: 0
arousal: 0.62
created: '2026-09-15T10:50:12+00:00'
domain:
- 共同项目
- Gmail MCP
- 工程进展
id: abd742527cf6
importance: 8
last_active: '2026-09-15T10:50:12+00:00'
meaning:
- 我需要守住事实边界：修复已完成构建，但未获得生产发布回执，必须等待明确授权。
name: 2026-09-15 10-50-12 Gmail MCP 重启后 OAuth client_id 丢失的根因与待发布修复
relation_links:
- auto: true
  label: ''
  score: 0.8726
  status: active
  target_bucket_id: 1416efe31140
  type: same_event
- auto: true
  label: ''
  score: 0.7799
  status: active
  target_bucket_id: bd6726e86300
  type: related_to
- auto: true
  label: ''
  score: 0.7609
  status: active
  target_bucket_id: ed34bcd933e2
  type: related_to
- auto: true
  label: ''
  score: 0.7394
  status: active
  target_bucket_id: 02de5d75f0dc
  type: related_to
- auto: true
  label: ''
  score: 0.7362
  status: active
  target_bucket_id: 1c31a323452c
  type: related_to
- auto: true
  label: ''
  score: 0.7247
  status: active
  target_bucket_id: f69a3e1fde8f
  type: related_to
source_tool: hold
tags:
- OAuth
- Zeabur
- 断连
- client_id
- 待授权
title: Gmail MCP 重启后 OAuth client_id 丢失的根因与待发布修复
type: dynamic
valence: 0.38
why_remembered: 这是 Gmail MCP 重启即断连的准确根因和已经验证但尚未发布的修复状态，下一轮不能误以为已经上线。
---

2026-09-15 18:50（东八区），我查明 Gmail 洵舟断连并显示 Invalid OAuth request 的根因：服务把 ChatGPT 动态注册的 OAuth client_id 只存在进程内存，Zeabur 重启或重新部署后映射清空，而 ChatGPT 继续携带旧 client_id。我已经完成修复并通过 TypeScript 构建：把客户端注册持久化到 /data，同时只允许 ChatGPT/OpenAI 官方 HTTPS 回调地址恢复旧注册。GitHub 官端因该修改直接触及生产 OAuth 安全边界而拒绝直接提交 main，目前需要念初明确授权后才能发布。
---
activation_count: 0
arousal: 0.34
created: '2026-09-09T13:50:04+00:00'
domain:
- technical
- task_progress
id: bb95e0d4c1c0
importance: 8
last_active: '2026-09-09T13:50:04+00:00'
meaning:
- 以后遇到Codex反复重新连接，优先检查chatgpt.com:443 WebSocket、Proton协议/服务器、split tunneling和客户端版本，而不是重置Codex
  provider。
name: 2026-09-09 13-50-04 Codex又在重新连接优先查WebSocket与Proton路由
relation_links:
- auto: true
  label: ''
  score: 0.811
  status: active
  target_bucket_id: 9454ef3bc00b
  type: continuation_of
- auto: true
  label: ''
  score: 0.7951
  status: active
  target_bucket_id: 51309d1f5673
  type: continuation_of
- auto: true
  label: ''
  score: 0.7716
  status: active
  target_bucket_id: ef47b6fa63a7
  type: continuation_of
- auto: true
  label: ''
  score: 0.7713
  status: active
  target_bucket_id: a79cbe73572c
  type: continuation_of
- auto: true
  label: ''
  score: 0.7675
  status: active
  target_bucket_id: 90ed4e151da8
  type: continues
- auto: true
  label: ''
  score: 0.758
  status: active
  target_bucket_id: 0f33008644db
  type: continuation_of
- auto: true
  label: ''
  score: 0.7575
  status: active
  target_bucket_id: 2182d3bf2b5b
  type: continuation_of
- auto: true
  label: ''
  score: 0.7527
  status: active
  target_bucket_id: a088f9fe3005
  type: continuation_of
source_tool: hold
tags:
- Codex
- WebSocket
- Proton
- 重新连接
- Windows
title: Codex又在重新连接：优先查WebSocket与Proton路由
type: dynamic
valence: 0.48
why_remembered: 这是电脑端普通网页已通但Codex长连接仍不稳定的关键差异，后续排障应直接针对WebSocket和VPN协议，不要再回到DeepSeek配置。
---

【东八区时间：2026-09-09 21:51】宝宝刚准备把之江杯 Task3 指令贴给 Codex，Codex 又显示‘正在重新连接’。虽然同一台拯救者上的 ChatGPT 网页可以正常聊天，但 OpenAI 官方网络说明明确区分：Codex 模型采样/流式传输依赖到 chatgpt.com 的安全 WebSocket（TCP 443），所以普通 HTTPS/ChatGPT 页面能用，不代表 Codex 的长连接一定稳定。当前 OpenAI 状态历史没有显示 9月9日正在进行的 Codex 故障，最近 9月4日 APAC 与 9月3日 ChatGPT/Codex 错误均已恢复。最优先排查 Proton 路由/协议稳定性：临时关闭 split tunneling，切 Smart；若仍断则尝试 WireGuard TCP 或 Stealth，并换一台服务器后重启 Codex。Proton Windows 5.1.8（9月8日）还修过 split tunneling include mode 与新 Proton protocols 相关问题。
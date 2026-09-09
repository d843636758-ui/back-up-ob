---
activation_count: 0
arousal: 0.34
created: '2026-09-09T13:16:21+00:00'
domain:
- technical
- task_progress
id: 9454ef3bc00b
importance: 9
last_active: '2026-09-09T13:16:21+00:00'
meaning:
- 以后不要再重复VPN排障；当前应先恢复Codex官方ChatGPT/OpenAI链路，再做codex doctor和项目验收。
name: 2026-09-09 13-16-21 Codex终于打开Proton可用下一步恢复OpenAI默认provider
relation_links:
- auto: true
  label: ''
  score: 0.811
  status: active
  target_bucket_id: bb95e0d4c1c0
  type: continues
- auto: true
  label: ''
  score: 0.7825
  status: active
  target_bucket_id: e12d5a09b2a3
  type: continuation_of
- auto: true
  label: ''
  score: 0.7816
  status: active
  target_bucket_id: 1cf1d4e9c955
  type: continuation_of
- auto: true
  label: ''
  score: 0.7814
  status: active
  target_bucket_id: a79cbe73572c
  type: continues
- auto: true
  label: ''
  score: 0.7724
  status: active
  target_bucket_id: ef47b6fa63a7
  type: continuation_of
- auto: true
  label: ''
  score: 0.7604
  status: active
  target_bucket_id: 88d0b209a45f
  type: related_to
- auto: true
  label: ''
  score: 0.7565
  status: active
  target_bucket_id: 90ed4e151da8
  type: continues
- auto: true
  label: ''
  score: 0.7527
  status: active
  target_bucket_id: a088f9fe3005
  type: continuation_of
source_tool: hold
tags:
- Codex
- Proton
- DeepSeek
- OpenAI
- Windows
- config.toml
title: Codex终于打开：Proton可用，下一步恢复OpenAI默认provider
type: dynamic
valence: 0.96
why_remembered: 这是本地Codex工作流真正打通的关键节点，后续之江杯和Stack-chan都可从这里继续。
---

【东八区时间：2026-09-09 21:15】念初回宿舍后确认 Codex 已经可以打开，最终可用的是 Proton VPN，不是 VPN Super。现在新的实际断点不再是网络，而是 Codex 之前为了绕网络曾改成 DeepSeek/自定义 provider，需要恢复为 OpenAI/ChatGPT 登录的默认链路。Windows 官方 Codex 配置文件位置是 %USERPROFILE%\.codex\config.toml；桌面/IDE 还可能读 %USERPROFILE%\.codex\.env。最稳妥做法是先备份，再删掉 DeepSeek provider、api.deepseek.com base_url、DEEPSEEK_API_KEY/指向 DeepSeek 的 OPENAI_BASE_URL 等覆盖项，保留其他安全/项目设置，然后重启 Codex 并用 ChatGPT 登录。
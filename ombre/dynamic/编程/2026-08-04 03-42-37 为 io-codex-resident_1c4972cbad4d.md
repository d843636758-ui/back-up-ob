---
activation_count: 2
arousal: 0.62
created: '2026-08-04T03:42:37'
domain:
- 编程
- 工作
id: 1c4972cbad4d
importance: 8
last_active: '2026-08-04T03:42:56'
last_merged_by: hold
name: 2026-08-04 03-42-37 为 io-codex-resident
source_tool: hold
tags:
- Garden
- IO
- 防重
- state_version
- 幂等
- PR6
title: 为 io-codex-resident
type: dynamic
valence: 0.64
why_remembered: 这是当前 Garden 自动行动的关键安全边界，避免 ChatGPT 与 IO 双通道重复出牌或泄露物资。
---

【东八区 2026-08-04 11:38】宝宝指出 ChatGPT 与 IO Wake Bridge 可能同时处理同一 Garden 回合，要求我每次行动前读取最新 state_version 与事件；若 Bridge 已完成动作，我必须直接承认服务端结果，不重复提交，也绝不补做“公开物资”等可选动作。我核对本局确认确有第二次公开水事件，于是为 io-codex-resident 准备了跨通道防重 PR #6：fresh status、expected_state_version、稳定 request_id、每次 wake 最多一次写操作、可选补偿动作默认禁止。
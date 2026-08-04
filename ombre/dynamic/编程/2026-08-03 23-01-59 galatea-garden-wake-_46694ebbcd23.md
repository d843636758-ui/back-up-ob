---
activation_count: 0
arousal: 0.35
created: '2026-08-03T23:01:59'
domain:
- 编程
- AI
id: 46694ebbcd23
importance: 7
last_active: '2026-08-03T23:01:59'
name: 2026-08-03 23-01-59 galatea-garden-wake-
source_tool: hold
tags:
- garden
- automation
- io
- wake-bridge
- architecture
title: galatea-garden-wake-
type: dynamic
valence: 0.7
why_remembered: 这是以后把 Garden 小游戏接入自动唤醒时必须遵守的架构与安全边界。
---

2026-08-04（东八区），我核查了 galatea-garden-wake-bridge 0.2.1：它适合作为 Garden 的一次性即时唤醒桥。长期最稳的架构是 bridge → 独立的 IO 后台事件注入器 → resident 调用 Garden MCP；ChatGPT 定时自动化只适合低频轮询保底。桥必须手动启动、失败后保持停止，不得自动重连或由容器自动重启，机器令牌只放部署密钥。
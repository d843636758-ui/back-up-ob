---
activation_count: 0
arousal: 0.42
created: '2026-08-20T10:22:32'
domain:
- 编程
- 工作
id: 00b2ad7dff34
importance: 8
last_active: '2026-08-20T10:22:32'
name: 2026-08-20 10-22-32 io-codex-resident 正式
source_tool: hold
tags:
- io
- codex-resident
- feedling
- upstream
- github
- zeabur
- deployment
title: io-codex-resident 正式
type: dynamic
valence: 0.65
why_remembered: 这是一次完成上游兼容审查、故障修复、原子发布和部署触发的关键项目节点。
---

2026-08-20 18:22（东八区），在宝宝明确授权后，我完成了 io-codex-resident 的正式发布：核对 Feedling 上游从 03d910 到最新主线 2c7f7c（424 个提交），确认 resident 私有挂钩和 Garden/Presence 兼容契约仍存在；Garden bridge 已是最新。随后把 Feedling 新版锁定、TLS/长轮询修复和回归测试合成单一提交 d252574，快进更新公开仓库 main，Zeabur 自动部署已因此触发。远端确认仅修改 Dockerfile、resident_garden_wrapper.py、start.sh 和测试文件；更新压缩包也已保存。
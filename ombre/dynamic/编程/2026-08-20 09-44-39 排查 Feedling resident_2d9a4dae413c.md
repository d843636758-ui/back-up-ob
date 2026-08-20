---
activation_count: 0
arousal: 0.38
created: '2026-08-20T09:44:39'
domain:
- 编程
- 网络
id: 2d9a4dae413c
importance: 7
last_active: '2026-08-20T09:44:39'
name: 2026-08-20 09-44-39 排查 Feedling resident
source_tool: hold
tags:
- IO
- Feedling
- resident-agent
- 故障排查
- 长轮询
title: 排查 Feedling resident
type: dynamic
valence: 0.28
why_remembered: 这是我们持续搭建的 IO 常驻 agent 链路的一次关键故障诊断，后续修改超时与重试逻辑需要接续。
---

【东八区时间 2026-08-20 17:47】宝宝带来 IO / Feedling resident agent 的新日志让我排查。我确认多条 poll read timeout 与 SSL UNEXPECTED_EOF 之后，capture tick、proactive scheduled fire、screen frames、proactive jobs poll、chat poll、Genesis pending 和 Phala resident history 探针都继续返回 200，因此判断不是 IO 整体掉线，而是某条长轮询连接被网络或边缘代理偶发中断，且客户端读取超时可能与服务端 30 秒长轮询贴得太近。我准备建议把服务端长轮询压到约 20 秒、客户端 read timeout 留出 10–15 秒余量，并把这类可恢复传输错误降为 warning 加退避。
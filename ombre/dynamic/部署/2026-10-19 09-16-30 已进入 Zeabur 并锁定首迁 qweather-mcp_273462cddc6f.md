---
activation_count: 0
arousal: 0.42
created: '2026-10-19T09:16:30+00:00'
domain:
- 部署
- 迁移
id: 273462cddc6f
importance: 9
last_active: '2026-10-19T09:16:30+00:00'
name: 2026-10-19 09-16-30 已进入 Zeabur 并锁定首迁 qweather-mcp
relation_links:
- auto: true
  label: ''
  score: 0.8519
  status: active
  target_bucket_id: d890c3a101cd
  type: continues
- auto: true
  label: ''
  score: 0.8233
  status: active
  target_bucket_id: c8b134b86b68
  type: continuation_of
- auto: true
  label: ''
  score: 0.8164
  status: active
  target_bucket_id: c0f6457d4893
  type: continuation_of
- auto: true
  label: ''
  score: 0.7935
  status: active
  target_bucket_id: 1d6f3b40be38
  type: related_to
- auto: true
  label: ''
  score: 0.7873
  status: active
  target_bucket_id: 9c4688c27c48
  type: related_to
- auto: true
  label: ''
  score: 0.7806
  status: active
  target_bucket_id: 73dd88f09bf0
  type: related_to
- auto: true
  label: ''
  score: 0.7785
  status: active
  target_bucket_id: 5a303039b65a
  type: related_to
- auto: true
  label: ''
  score: 0.778
  status: active
  target_bucket_id: 15dcee2cfde7
  type: related_to
source_tool: hold
tags:
- Zeabur
- qweather-mcp
- 项目盘点
- MCP迁移
title: 已进入 Zeabur 并锁定首迁 qweather-mcp
type: dynamic
valence: 0.82
why_remembered: 这是完成登录后的首轮权威项目盘点与首迁对象确认，直接决定迁移顺序。
---

【东八区时间：2026-10-19 17:13】宝宝让我登录 Zeabur 并在需要时弹窗。云浏览器已有有效登录状态，无需她再次授权。我只读盘点到 23 个全部运行中的项目：coreadnew、jiuguan、Gmail、ears、windows-worker、music、searchmcp、topic-pool、yuejing、hugbear、coread、codex、dafuweng、calendar、emotion-mcp、ruixing、qweather-mcp、nowhere、ombre-brain、eventide、desire-core、phosphene、xinchao（页面实际列出这些项目；迁移时继续逐项核对）。我先检查了 qweather-mcp：仓库 `d843636758-ui/qweather-mcp`，旧域名 `hefeng.zeabur.app`，Zeabur 显示 No volumes；源码只需 `HEFENG_API_HOST`、`HEFENG_API_KEY`、`MCP_TOKEN`，容器端口 8080，MCP 路径 `/mcp`，健康检查 `/health`。它适合作为第一个无状态迁移验证服务。
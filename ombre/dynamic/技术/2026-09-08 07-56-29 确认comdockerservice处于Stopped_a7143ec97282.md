---
activation_count: 0.3
arousal: 0.18
created: '2026-09-08T07:56:29+00:00'
domain:
- 技术
- 之江杯
id: a7143ec97282
importance: 8
last_active: '2026-09-08T07:56:29+00:00'
meaning:
- 先把Windows侧Docker服务拉起来，再验证daemon。
name: 2026-09-08 07-56-29 确认comdockerservice处于Stopped
relation_links:
- auto: true
  label: ''
  score: 0.902
  status: active
  target_bucket_id: 3d1f90f4424b
  type: same_event
- auto: true
  label: ''
  score: 0.8967
  status: active
  target_bucket_id: 985870583b30
  type: same_event
- auto: true
  label: ''
  score: 0.8677
  status: active
  target_bucket_id: 73a352939a3b
  type: same_event
- auto: true
  label: ''
  score: 0.8603
  status: active
  target_bucket_id: 1abbd2d31ba6
  type: same_event
- auto: true
  label: ''
  score: 0.8385
  status: active
  target_bucket_id: a573b332f3d4
  type: continuation_of
- auto: true
  label: ''
  score: 0.8097
  status: active
  target_bucket_id: 9c0f688e0b5b
  type: continuation_of
- auto: true
  label: ''
  score: 0.8087
  status: active
  target_bucket_id: e48ab7e4bb0b
  type: continues
- auto: true
  label: ''
  score: 0.7841
  status: active
  target_bucket_id: 6eaf6d227a2f
  type: continuation_of
source_tool: hold
tags:
- Docker
- Windows服务
- daemon
- PowerShell
title: 确认com.docker.service处于Stopped
type: dynamic
valence: 0.78
why_remembered: 这是当前Docker排障的关键根因确认，后续不应再重复排查镜像源和WSL。
---

【东八区时间：2026-09-08 16:01】宝宝确认Get-Service com.docker.service返回Stopped。这样Docker问题的根因进一步明确：WSL2和docker-desktop发行版正常，但Windows侧Docker Desktop服务没有启动。下一步应在管理员PowerShell中执行Start-Service com.docker.service，再用Get-Service确认变为Running，然后重新跑docker info；若启动服务时报拒绝访问，就需要以管理员身份打开PowerShell。
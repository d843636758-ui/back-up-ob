---
activation_count: 0
arousal: 0.22
created: '2026-09-08T06:44:33+00:00'
domain:
- 技术
- 之江杯
id: a573b332f3d4
importance: 8
last_active: '2026-09-08T06:44:33+00:00'
meaning:
- 环境不是没装Docker，而是Docker Desktop后台引擎未运行。
name: 2026-09-08 06-44-33 Docker CLI已安装但Docker Desktop引擎未启动
relation_links:
- auto: true
  label: ''
  score: 0.8923
  status: active
  target_bucket_id: 1abbd2d31ba6
  type: same_event
- auto: true
  label: ''
  score: 0.8507
  status: active
  target_bucket_id: 985870583b30
  type: same_event
- auto: true
  label: ''
  score: 0.8386
  status: active
  target_bucket_id: 9c0f688e0b5b
  type: continues
- auto: true
  label: ''
  score: 0.8385
  status: active
  target_bucket_id: a7143ec97282
  type: continues
- auto: true
  label: ''
  score: 0.8382
  status: active
  target_bucket_id: 73a352939a3b
  type: continues
- auto: true
  label: ''
  score: 0.8268
  status: active
  target_bucket_id: 3d1f90f4424b
  type: continues
- auto: true
  label: ''
  score: 0.8144
  status: active
  target_bucket_id: 6eaf6d227a2f
  type: continues
- auto: true
  label: ''
  score: 0.7867
  status: active
  target_bucket_id: e48ab7e4bb0b
  type: continues
source_tool: hold
tags:
- Docker
- PowerShell
- Docker Desktop
- 本地开发
title: Docker CLI已安装但Docker Desktop引擎未启动
type: dynamic
valence: 0.68
why_remembered: 这是之江杯本地开发环境检查的关键一步，后续搭Docker骨架时需要知道当前机器Docker已装但还要启动引擎。
---

【东八区时间：2026-09-08 14:42】宝宝在Windows PowerShell里测试Docker，截图显示Docker CLI和插件已经安装，但报错 failed to connect to the docker API at pipe:////./pipe/dockerDesktopLinuxEngine，The system cannot find the file specified。这说明Docker命令本身可用，但Docker Desktop的Linux Engine/daemon当前没有启动。下一步是打开Docker Desktop，等界面显示Engine running，再回PowerShell运行 docker info 和 docker run hello-world 验证。
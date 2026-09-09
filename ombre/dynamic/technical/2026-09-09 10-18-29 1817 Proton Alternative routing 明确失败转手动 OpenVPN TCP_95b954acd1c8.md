---
activation_count: 0
arousal: 0.42
created: '2026-09-09T10:18:29+00:00'
domain:
- technical
- daily
id: 95b954acd1c8
importance: 7
last_active: '2026-09-09T10:18:29+00:00'
meaning:
- 当登录前替代路由都失败时，应把账号获取和配置生成移到已经能出网的手机端，再把最小必要配置带回 Windows。
name: 2026-09-09 10-18-29 1817 Proton Alternative routing 明确失败转手动 OpenVPN TCP
relation_links:
- auto: true
  label: ''
  score: 0.88
  status: active
  target_bucket_id: a088f9fe3005
  type: same_event
- auto: true
  label: ''
  score: 0.8432
  status: active
  target_bucket_id: 2182d3bf2b5b
  type: continuation_of
- auto: true
  label: ''
  score: 0.8401
  status: active
  target_bucket_id: ec0f8dfe9a56
  type: continues
- auto: true
  label: ''
  score: 0.8255
  status: active
  target_bucket_id: 1cf1d4e9c955
  type: continues
- auto: true
  label: ''
  score: 0.8158
  status: active
  target_bucket_id: e12d5a09b2a3
  type: continues
- auto: true
  label: ''
  score: 0.7657
  status: active
  target_bucket_id: 516544b5ec4c
  type: continuation_of
- auto: true
  label: ''
  score: 0.7444
  status: active
  target_bucket_id: 9454ef3bc00b
  type: related_to
source_tool: hold
tags:
- 准确时间
- Proton VPN
- Alternative routing
- OpenVPN TCP
- Windows
- 网络排障
title: 18:17 Proton Alternative routing 明确失败，转手动 OpenVPN TCP
type: dynamic
valence: 0.34
why_remembered: 这是 Windows VPN 启动链路里很明确的失败证据和路线切换点，后续不应重复 Proton 客户端登录尝试。
---

【东八区时间：2026-09-09 18:17】念初发来 Proton VPN Windows 登录页截图，明确报错“No alternative hosts exist. Alternative routing failed.”，且下方帮助网页在电脑上也打不开。这说明 Proton 的登录前备用路由本身也被当前 Windows 网络环境挡住，继续在客户端里点登录/帮助意义不大。下一步改走“手机上利用已有可用 VPN 获取 Proton 手动 OpenVPN 配置与专用 OpenVPN 凭据 → 传到 Windows → 用 OpenVPN GUI 导入 TCP 配置”的路线。Proton 官方说明手动 OpenVPN 需要在 account.protonvpn.com 的 Account → OpenVPN username 获取专用用户名/密码，并在 Downloads → OpenVPN configuration files 下载 Windows 的 TCP 配置；TCP 使用 443 端口，比 UDP 在受限网络中更值得先试。需要提醒：这条路线能绕过 Proton Windows 客户端的登录，但不能保证绕过所有 DPI，如果 TCP 443 也失败，就不能再把时间耗在 Proton 上。
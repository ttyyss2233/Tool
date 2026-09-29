# Rocket Proxy

[Rocket Proxy](https://apps.apple.com/app/id6785291194) 是一款免费的代理客户端（iOS / iPadOS / Apple TV / macOS / Android）。本仓库的小火箭、QuantumultX 和 Egern 规则与模块都可以直接在 Rocket Proxy 中使用。

[Rocket Proxy](https://apps.apple.com/app/id6785291194) is a free proxy client for iOS, iPadOS, Apple TV, macOS and Android. The Shadowrocket, QuantumultX and Egern rules and modules in this repo work in Rocket Proxy as they are.

## 一键导入完整配置 · One-tap full config

**[在 Rocket Proxy 中打开 RocketProxy.conf · Open RocketProxy.conf in Rocket Proxy](https://jcltravels.co.uk/import/?config=https%3A%2F%2Fraw.githubusercontent.com%2Fttyyss2233%2FTool%2Fmain%2Frocketproxy%2FRocketProxy.conf)**

[`RocketProxy.conf`](RocketProxy.conf) 把本仓库的内容合并成一个配置：

- 广告拦截：`MyBlockAds.list`、`blockads.list`、Egern `blockad.yaml`、`fanqieNoad.list`、`hongguoAD.list`、微信去广告
- WhatsApp 聊天及语音/视频通话（通话媒体走 UDP，已用真实通话验证）
- DNS 防泄露、分流修正（直连）、AI、流媒体、Emby、Talkatone、游戏、隐藏 IP 归属地（代理）
- YouTube 去广告脚本、CMS 影视去广告脚本
- 国内 IP 直连，其余走代理

规则集直接引用本仓库的原始文件，仓库更新后自动生效。

`RocketProxy.conf` combines this repo into one config:

- Ad blocking: `MyBlockAds.list`, `blockads.list`, Egern `blockad.yaml`, `fanqieNoad.list`, `hongguoAD.list` and WeChat ads.
- WhatsApp chat plus voice and video calls. Call media is UDP; tested with a real call.
- Through the proxy: DNS leak tests, AI, streaming, Emby, Talkatone, games and IP-location hiding. Direct: domestic-site corrections.
- YouTube and CMS video ad-removal scripts.
- Mainland China IPs go direct, everything else through the proxy.

Its rule sets point at this repo's raw files, so updates here reach users automatically.

## 一键导入单个模块 · One-tap modules

每个模块导入后会作为一个独立配置出现在「路由」中。

Each module imports as its own config under Routing.

| 模块 · Module | 文件 · File | |
|--|--|--|
| YouTube 去广告<br>YouTube ad removal | `YouTubeAd.sgmodule` | [一键导入 · Import](https://jcltravels.co.uk/import/?module=https%3A%2F%2Fraw.githubusercontent.com%2Fttyyss2233%2FTool%2Fmain%2Fshadowrocket%2Fmokuai%2FYouTubeAd.sgmodule) |
| YouTube 去广告（Maasea 版）<br>YouTube ad removal (Maasea) | `Youtube-noAds.sgmodule` | [一键导入 · Import](https://jcltravels.co.uk/import/?module=https%3A%2F%2Fraw.githubusercontent.com%2Fttyyss2233%2FTool%2Fmain%2Fshadowrocket%2Fmokuai%2FYoutube-noAds.sgmodule) |
| CMS 影视去插入式广告<br>CMS video ad removal | `cmsAdblock.sgmodule` | [一键导入 · Import](https://jcltravels.co.uk/import/?module=https%3A%2F%2Fraw.githubusercontent.com%2Fttyyss2233%2FTool%2Fmain%2Fshadowrocket%2Fmokuai%2FcmsAdblock.sgmodule) |
| 微信公众号及小程序去广告<br>WeChat ads | `wxNoad.sgmodule` | [一键导入 · Import](https://jcltravels.co.uk/import/?module=https%3A%2F%2Fraw.githubusercontent.com%2Fttyyss2233%2FTool%2Fmain%2Fshadowrocket%2Fmokuai%2FwxNoad.sgmodule) |
| DNS 防泄露<br>DNS leak protection | `Prevent_DNS_Leaks.sgmodule` | [一键导入 · Import](https://jcltravels.co.uk/import/?module=https%3A%2F%2Fraw.githubusercontent.com%2Fttyyss2233%2FTool%2Fmain%2Fshadowrocket%2Fmokuai%2FPrevent_DNS_Leaks.sgmodule) |
| 屏蔽苹果系统更新<br>Block iOS updates | `BlockAppleUpdate.sgmodule` | [一键导入 · Import](https://jcltravels.co.uk/import/?module=https%3A%2F%2Fraw.githubusercontent.com%2Fttyyss2233%2FTool%2Fmain%2Fshadowrocket%2Fmokuai%2FBlockAppleUpdate.sgmodule) |
| 屏蔽 iOS/iPadOS OTA 更新<br>Block iOS/iPadOS OTA updates | `Surge_SoftwareUpdate.sgmodule` | [一键导入 · Import](https://jcltravels.co.uk/import/?module=https%3A%2F%2Fraw.githubusercontent.com%2Fttyyss2233%2FTool%2Fmain%2Fshadowrocket%2Fmokuai%2FSurge_SoftwareUpdate.sgmodule) |
| 苹果 APNs 推送走代理<br>Apple push (APNs) via proxy | `Apns.module` | [一键导入 · Import](https://jcltravels.co.uk/import/?module=https%3A%2F%2Fraw.githubusercontent.com%2Fttyyss2233%2FTool%2Fmain%2Fshadowrocket%2Fmokuai%2FApns.module) |
| 预览 QX 资源<br>Preview QX resources | `QX-resource-preview.sgmodule` | [一键导入 · Import](https://jcltravels.co.uk/import/?module=https%3A%2F%2Fraw.githubusercontent.com%2Fttyyss2233%2FTool%2Fmain%2Fshadowrocket%2Fmokuai%2FQX-resource-preview.sgmodule) |

## 规则列表 · Rule lists

以下文件可在 `Shield -> 区域与绕行规则 -> 添加自定义规则集` 中添加，也可以在任意配置中写成 `RULE-SET,<链接>,<策略>`：

Add any of these under Shield -> Regional & Bypass Rules -> Add Custom Rule Set, or use them in any config as `RULE-SET,<url>,<policy>`:

- `https://raw.githubusercontent.com/ttyyss2233/Tool/main/shadowrocket/rules/MyBlockAds.list`
- `https://raw.githubusercontent.com/ttyyss2233/Tool/main/shadowrocket/rules/blockads.list`
- `https://raw.githubusercontent.com/ttyyss2233/Tool/main/shadowrocket/rules/AI.list`
- `https://raw.githubusercontent.com/ttyyss2233/Tool/main/shadowrocket/rules/emby.list`
- `https://raw.githubusercontent.com/ttyyss2233/Tool/main/shadowrocket/rules/apns.list`
- `https://raw.githubusercontent.com/ttyyss2233/Tool/main/shadowrocket/rules/BlockiOSUpdate.list`
- `https://raw.githubusercontent.com/ttyyss2233/Tool/main/shadowrocket/rules/honer.list`
- `https://raw.githubusercontent.com/ttyyss2233/Tool/main/shadowrocket/rules/fanqieNoad.list`
- `https://raw.githubusercontent.com/ttyyss2233/Tool/main/shadowrocket/rules/hongguoAD.list`
- `https://raw.githubusercontent.com/ttyyss2233/Tool/main/quanX/rules/Streaming.list`
- `https://raw.githubusercontent.com/ttyyss2233/Tool/main/quanX/rules/Talkatone.list`
- `https://raw.githubusercontent.com/ttyyss2233/Tool/main/quanX/rules/xiuzheng.list`
- `https://raw.githubusercontent.com/ttyyss2233/Tool/main/quanX/rules/anti-ip-attribution.txt`
- `https://raw.githubusercontent.com/ttyyss2233/Tool/main/egern/rules/blockad.yaml`

## 说明 · Notes

- 一键导入适用于 iOS、iPadOS 和 macOS 版。导入后在「路由」中长按配置，选择“使用此配置”。
- 脚本和 MITM 需要在 Rocket Proxy 中安装并信任证书；未信任时 Rocket Proxy 会自动关闭解密，其余规则照常生效。
- WhatsApp 通话需要支持 UDP 的节点（如 Shadowsocks、Trojan、VLESS、Hysteria2、TUIC）。
- 配置文件中的 `AND` 组合规则可以使用，规则列表文件中的 `AND` 行会被跳过；YouTube 模块中阻止 QUIC 的规则由 Rocket Proxy 自动处理。
- AdGuard 格式的 `adguard/fanqie.txt` 暂不支持。

- One-tap import works on iOS, iPadOS and macOS. After import, long-press the config under Routing and choose "Use This Config".
- Scripts and MITM need the Rocket Proxy certificate installed and trusted. Until it is, Rocket Proxy turns decryption off and the other rules keep working.
- WhatsApp calls need a server that carries UDP, such as Shadowsocks, Trojan, VLESS, Hysteria2 or TUIC.
- `AND` rules work in a config file but are skipped inside rule-list files. Rocket Proxy blocks QUIC for decrypted hosts itself, which covers the YouTube modules' `AND` rules.
- The AdGuard-format `adguard/fanqie.txt` is not supported.

## 下载 · Download

- App Store（免费 · free）：https://apps.apple.com/app/id6785291194
- Google Play：https://play.google.com/store/apps/details?id=uk.co.jcltravels.rocketproxy
- IPA（可用 [TrollStore](https://github.com/opa334/TrollStore) 安装 · installs with TrollStore）：https://github.com/jcltravels/RocketProxy/releases/download/v2.6.7/RocketProxy-2.6.7.ipa
- APK / DMG：https://github.com/jcltravels/RocketProxy/releases/latest
- 中文下载页 · Chinese download page：https://jcltravels.co.uk/cn/
- Gitee 镜像 · Gitee mirror：https://gitee.com/jcltravels/RocketProxy/releases

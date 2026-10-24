# Discord Voice for WebSpeak

Discord 风格的独立 WebSpeak 皮肤。通过 `.wskin` 包分发，页面、样式和五种语言文案均在包内；不修改 WebSpeak 运行时代码，不包含可执行 JavaScript。它不是 Discord 官方产品。

A portable Discord-inspired WebSpeak skin. Layout, CSS and all five translations ship inside the `.wskin` archive. It contains no executable JavaScript and is not affiliated with Discord.

## 安装 / Install

在支持皮肤商店的 WebSpeak 管理控制台打开 **皮肤 → 皮肤商店 → Discord Voice → 安装**，然后在“实例皮肤”中启用或设为默认。访客仍需批准页面替换及所需能力权限。

In a WebSpeak instance with the skin store, open **Skins → Skin store → Discord Voice → Install**. Enable it or set the instance default under Instance skins. Visitors still approve surface replacement and requested capabilities.

也可下载 [v1.0.5 归档](https://raw.githubusercontent.com/Huddle-Up-Forge/webspeak-skin-discord-voice/v1.0.5/discord-voice.wskin) 后在 `/admin/skins` 导入。最低应用版本：WebSpeak 0.2.8（需包含当前公开皮肤接口）。

You can also download the [v1.0.5 archive](https://raw.githubusercontent.com/Huddle-Up-Forge/webspeak-skin-discord-voice/v1.0.5/discord-voice.wskin) and import it at `/admin/skins`. Requires WebSpeak 0.2.8 with the current public skin API.

## 贡献者与来源 / Contributors and origin

- [@yichen11818](https://github.com/yichen11818)（原始提交署名 **yumi**）：Discord 风格皮肤的原始设计与实现，见 WebSpeak [PR #52](https://github.com/EchoSixHIYA/WebSpeak-client-for-TeamSpeak/pull/52) 及早期的 [PR #27](https://github.com/EchoSixHIYA/WebSpeak-client-for-TeamSpeak/pull/27)。
- WebSpeak 项目：将原作移植为独立的 `.wskin` 包，适配公开皮肤接口，并维护分发与后续更新。

The original Discord-style skin was designed and implemented by [@yichen11818](https://github.com/yichen11818), whose original commits are signed **yumi**. It was submitted in WebSpeak [PR #52](https://github.com/EchoSixHIYA/WebSpeak-client-for-TeamSpeak/pull/52), following the earlier [PR #27](https://github.com/EchoSixHIYA/WebSpeak-client-for-TeamSpeak/pull/27). The WebSpeak project adapted it into this portable `.wskin` package and maintains its public-API integration and distribution.

本仓库保留了从原始 PR 提取的皮肤源码提交及原作者署名。当前发行包的源码位于 `skin/`。

This repository preserves the skin-only source history from the original PR with its original authorship. Sources for the current release are in `skin/`.

## 构建与发布 / Build and publish

```sh
npm ci
npm run build
```

`skin/` contains the package sources. The deterministic build writes `discord-voice.wskin` and `skin.json`, including its SHA-256 digest. Validate the resulting archive with WebSpeak before publishing. Increment the manifest version, commit all release files, then create the matching `v<version>` tag. Never move a published tag. `skin.json` on the default branch advertises the current version to the store.

索引 / Index: [Huddle-Up-Forge/webspeak-skins](https://github.com/Huddle-Up-Forge/webspeak-skins)

规范 / Contract: [WebSpeak skin development guide](https://github.com/EchoSixHIYA/WebSpeak-client-for-TeamSpeak/blob/master/docs/SKIN_DEVELOPMENT.md)

License: AGPL-3.0-only. See [LICENSE](LICENSE).

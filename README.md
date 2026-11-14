# SnowLuma Releases

SnowLuma 的发行发布仓库 / Release distribution for SnowLuma.

SnowLuma 是 QQ 客户端的 TypeScript 互操作运行时：将 QQ 原生会话转换为 [OneBot v11](https://github.com/botuniverse/onebot-11) 动作与事件，并提供 WebUI、TypeScript SDK 与 MCP 入口。源码不公开，本仓库仅承载发行产物与兼容性清单。

## 下载

从 [Releases](https://github.com/lin-414/Releases/releases) 下载对应平台的完整发行包并解压（Windows x64 · Linux x64 / arm64）。完整版内置 Node.js；Lite 版需 Node.js ^24.22.1 / >=26.12.1。

1. 解压与系统架构匹配的压缩包；Windows 运行 `launcher.bat`，Linux 运行 `./launcher.sh`。
2. 打开 <http://localhost:5099> ，使用启动日志中的初始密码登录 WebUI，按引导接入 QQ 进程。

## 文档与反馈

- [部署指南](https://snowluma.github.io/zh/docs/guide/deploy) · [OneBot 动作参考](https://snowluma.github.io/zh/docs/api)
- [问题反馈](https://github.com/lin-414/Releases/issues)
- QQ 群：<https://qm.qq.com/q/g3UMLpWALe> · Telegram：<https://t.me/napcatqq>

## 说明

- `compat/qq.json` 为 QQ 兼容性清单，客户端启动时从本仓库 `main` 分支拉取，校验本地 QQ 版本。
- SnowLuma 与腾讯 / QQ 无隶属关系，仅供学习与技术研究，按“现状”提供；发行包的使用受包内随附的 EULA 约束。
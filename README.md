# Blubfish Releases

Blubfish 的发行发布仓库 / Release distribution for Blubfish。

Blubfish 是 QQ 客户端的 TypeScript 互操作运行时：将 QQ 原生会话转换为 [OneBot v11](https://github.com/botuniverse/onebot-11) 动作与事件，并提供 WebUI、TypeScript SDK 与 MCP 入口。源码不公开，本仓库仅承载发行产物与兼容性清单。

## 下载

从 [Releases](https://github.com/lin-414/Releases/releases) 下载对应平台的完整发行包并解压（Windows x64 · Linux x64 / arm64）。完整版内置 Node.js；Lite 版需 Node.js ^24.22.1 / >=26.12.1。

1. 解压与系统架构匹配的压缩包；Windows 运行 `launcher.bat`，Linux 运行 `./launcher.sh`。
2. 打开 <http://localhost:5099> ，使用启动日志中的初始密码登录 WebUI，按引导接入 QQ 进程。

## 文档与反馈

- [部署指南](https://snowluma.github.io/zh/docs/guide/deploy) · [OneBot 动作参考](https://snowluma.github.io/zh/docs/api)
- [问题反馈](https://github.com/lin-414/Releases/issues)
- QQ 群：<https://qm.qq.com/q/g3UMLpWALe> · Telegram：<https://t.me/napcatqq>

## 从旧版迁移

原公开仓库已停止维护并转为私有维护。旧版 2.4.2 安装的**应用内自动更新已失效**（其更新源指向的旧仓库地址不再提供服务），需要手动迁移一次：

1. 从 [Releases](https://github.com/lin-414/Releases/releases) 下载 v0.1.0 或更新的完整发行包，**解压到新目录**运行，不要覆盖旧安装目录。
2. 配置与数据：先用旧实例 WebUI 的备份功能导出，再到新实例导入；不确定数据位置时以旧实例导出的备份为准。Blubfish 可直接读取 SnowLuma 2.5.x 遗留的备份标记与 `snowluma.json` 全局配置。
3. 迁移完成后，应用内更新检查将指向本仓库，此后可正常自动更新。

改名前的 SnowLuma 2.5.x 安装不会被自动更新到 Blubfish（应用版本已重置为 0.1.0，旧实例的更新检查不会把 0.1.0 视为新版本），请按上述步骤手动迁移一次。

Docker 用户请改用基于本仓库发行包构建的新镜像；SDK / MCP 的 npm 发布已停止，随发行包使用。

## 说明

- `compat/qq.json` 为 QQ 兼容性清单，客户端启动时从本仓库 `main` 分支拉取，校验本地 QQ 版本。
- Blubfish 与腾讯 / QQ 无隶属关系，仅供学习与技术研究，按“现状”提供；发行包的使用受包内随附的 EULA 约束。

# Finwisp 更新日志 / Changelog

## v0.1.0-preview.20260929

本地构建日期 / Local build date: 2026-09-29

- 提供 Apple Silicon M 系列 Mac Preview 安装包；需要 macOS 13+、本机 Codex CLI 与具有 Codex 权限的 ChatGPT 订阅账号。
- 包含语音与文字交流、行情资讯、资料研究、研报检索、关注与持仓、记忆管理。
- 策略回测可由智能体组织 Python 计算，结果与文件按会话保存并回读。
- 左上角增加手动麦克风静音，暂停收音时已有回答和后台任务继续。
- 此仓库仅发布安装包与说明，不提供产品开发源码。
- 公开分发副本清理了构建机器路径及 macOS 文件元数据，保留运行组件与第三方许可证；业务功能沿用 9 月 29 日 v2。
- 当前为未公证的预览包，尚未完成跨 Mac 兼容性验收。

---

- Apple Silicon M-series Mac Preview package; requires macOS 13+, local Codex CLI, and a ChatGPT subscription account with Codex access.
- Includes voice and text conversation, market information, document research, report search, watchlists, holdings, and memory management.
- Agent-organized Python backtesting with calculation outputs and files saved and readable by conversation.
- Manual microphone mute in the top-left control pauses input while existing answers and background tasks continue.
- This repository distributes app packages and documentation only, without product development source code.
- The public distribution copy removes build-machine paths and macOS file metadata while retaining runtime components and third-party notices. Product behavior follows the September 29 v2 build.
- The preview is not notarized, and compatibility across Macs has not been validated.

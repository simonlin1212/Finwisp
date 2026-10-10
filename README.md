<p align="center"><b>简体中文</b> | <a href="README_en.md">English</a></p>
<h1 align="center">Finwisp</h1>
<p align="center">
  <b>语音投研助手</b><br>
  语音交流 · 行情资讯 · 资料研究 · 策略回测 · 记忆管理
</p>
<p align="center">
  <a href="https://github.com/simonlin1212/Finwisp/releases/download/v0.1.0-preview.20260929/Finwisp-Preview-20260929-v2-mac-arm64.zip"><b>下载最新版 Mac App（M 系列芯片）</b></a> · <a href="https://github.com/simonlin1212/Finwisp/releases/tag/v0.1.0-preview.20260929">Release 发布说明</a>
</p>
<p align="center">
  <img src="https://img.shields.io/badge/macOS-13%2B-black" alt="macOS 13 or later">
  <img src="https://img.shields.io/badge/Apple_Silicon-M_series-black" alt="Apple Silicon M series">
  <img src="https://img.shields.io/badge/Codex-subscription_required-orange" alt="Codex subscription required">
  <img src="https://img.shields.io/badge/Distribution-app_only-blue" alt="App distribution only">
</p>
<p align="center">
  <a href="#下载">下载</a> · <a href="#使用要求">使用要求</a> · <a href="#安装与接入">安装与接入</a> · <a href="#功能">功能</a> · <a href="#当前限制">当前限制</a> · <a href="CHANGELOG.md">更新日志</a>
</p>

---

Finwisp 把语音交流、研究工具和本地记录连接起来。可以直接描述研究问题、补充条件，并通过语音切换页面；研究进度、资料依据和计算结果可以在界面中回看。

**这是闭源应用的发布与说明仓库，不是产品源码仓库。** 安装包在 GitHub Releases 中提供；本仓库不包含 Finwisp 的开发源码、用户资料或登录凭据。

## 下载

- [下载 Mac Apple Silicon 安装包](https://github.com/simonlin1212/Finwisp/releases/download/v0.1.0-preview.20260929/Finwisp-Preview-20260929-v2-mac-arm64.zip)
- [查看发布说明与 SHA-256 校验文件](https://github.com/simonlin1212/Finwisp/releases/tag/v0.1.0-preview.20260929)

下载后解压，将 `Finwisp Preview.app` 放入“应用程序”。GitHub 自动附带的 `Source code (zip/tar.gz)` 只是这个说明仓库的快照，不是 App 安装包，也不包含产品开发源码。

## 使用要求

<table>
<thead>
<tr><th nowrap>项目</th><th>当前要求</th></tr>
</thead>
<tbody>
<tr><td nowrap>电脑</td><td><strong>仅支持 Apple Silicon M 系列芯片的 Mac</strong>，不支持 Intel Mac、Windows 或 Linux</td></tr>
<tr><td nowrap>系统</td><td>macOS 13 或更高版本</td></tr>
<tr><td nowrap>模型接入</td><td><strong>需要具有 Codex 使用权限的 ChatGPT 订阅账号</strong>；模型与语音的实际可用性及额度由 OpenAI 账号决定</td></tr>
<tr><td nowrap>本机运行时</td><td>需要安装 Codex CLI；本版要求 <code>/opt/homebrew/bin/codex</code> 可执行文件可用。仅安装 Codex 桌面界面不代表此路径已配置</td></tr>
<tr><td nowrap>网络</td><td>模型、实时语音及联网数据查询需要网络连接</td></tr>
<tr><td nowrap>音频</td><td>当前仅允许选择 Mac 内建麦克风与扬声器，需允许麦克风访问</td></tr>
<tr><td nowrap>界面</td><td>当前为简体中文界面</td></tr>
</tbody>
</table>

App 已随包提供 Node 与 Python 运行时，无需另行安装这两个环境。Finwisp 不提供或共享订阅账号，安装包不包含任何登录态。本次发布按订阅接入方式提供，不承诺 API Key 接入可替代完整语音能力。

## 安装与接入

1. 确认 Mac 使用 M 系列芯片，系统为 macOS 13 或更高版本。
2. 按 [OpenAI 官方 Codex CLI 安装说明](https://learn.chatgpt.com/docs/codex/cli)安装本机运行时，并确认终端运行 `/opt/homebrew/bin/codex --version` 能显示版本。本版固定使用此路径；安装到其他位置需要先完成路径配置。
3. 下载 Releases 中的 ZIP，解压后将 App 移入“应用程序”，再打开。
4. 在 Finwisp 的“设置 → 模型与连接”中使用自己的 ChatGPT 订阅账号登录并检查连接。产品登录与个人 Codex 登录、记录分别管理，不会从个人目录复制登录凭据。
5. 开启左上角语音入口，按 macOS 提示允许麦克风访问。可先用文字提一个简短问题，再测试语音。

当前包未经过 Apple Developer ID 签名与公证，macOS 可能提示无法验证开发者。确认下载来源与校验值后，可按照系统提供的“隐私与安全性 → 仍要打开”流程处理；若系统仍拒绝打开，请提交具体提示。不要全局关闭系统安全保护。

## 功能

| 功能 | 使用方式 |
| --- | --- |
| 语音与文字交流 | 连续提问、补充条件和语音切页；手动麦克风静音只暂停收音，已有回答与后台任务继续 |
| 行情与资讯 | 查看主要指数、关注方向与资讯，保留来源和时间，将感兴趣的内容带入研究 |
| 研究与资料 | 回看已保存研究，导入 PDF、TXT、Markdown 资料，按页读取并引用依据 |
| 研报检索 | 优先使用东方财富与问财的固定入口；保存链接，取得可访问原件后关联资料库 |
| 策略回测 | 描述策略，由智能体查询数据、组织计算、运行并核对结果；计算假设和结果按会话保存 |
| 关注与持仓 | 管理不同市场的关注方向和持仓记录，保留新增、修正与删除的操作记录 |
| 记忆管理 | 管理沟通偏好、研究呈现习惯和问题延续；支持开关、纠正与删除，候选采用按对应授权执行 |

## 当前限制

- **当前提供 Preview 版本。** 已在开发者本机进行 App 启动、文字模型、包内计算、合成语音及实体麦克风接入验证；尚未完成其他 Mac 的兼容性验证，不保证所有订阅账号、系统版本或音频设备都可用。
- 本版研究模型固定为 `GPT-5.6-Sol`，实时语音依赖 Codex 的原生接口。账号模型权限、语音权限、订阅额度和 Codex 版本差异都可能影响接入。
- 数据源可能延迟、缺失或不可访问；部分入口还需要其自身的服务权限或配置。检索不代表能取得所有研报原件。
- 回测依赖可取得的数据和明确的计算假设；日线近似、分钟路径、竞价与真实成交应分别理解。计算结果需要核对，不代表任意策略都能取得所需历史数据。
- 实时语音仍可能存在分句、识别偏差或提前口播，业务结果应以已保存的工具回执与研究记录核对。手动静音可避免其他讲话继续进入当前任务。
- 本地记录不等于完全离线。使用模型和语音时，相关输入会发送到所连接的模型服务；保存语音文字的开关不等于删除服务端历史。App 与网页版资料分别管理，不自动同步。
- 尚未提供自动更新、Intel Mac、Windows 或 Linux 安装包。

## 反馈

通过 [GitHub Issues](https://github.com/simonlin1212/Finwisp/issues)反馈问题，附上 Mac 芯片、macOS 版本、Codex 版本、App 版本、操作步骤与具体错误提示即可。请勿公开登录凭据、私人研报、研究记录或持仓明细。

## 更新日志

见 [CHANGELOG.md](CHANGELOG.md)。后续版本继续在 Releases 提供安装包。

## 免责声明

Finwisp 用于信息整理、研究与模拟计算。模型回答、第三方数据及回测结果均需独立核对，不构成投资建议，不保证收益。

## 版权

Finwisp 为闭源软件，产品源码未在本仓库授权开源。公开提供安装包不等于授予产品源码的使用或分发许可。随包第三方组件的权利和许可证仍由其各自条款约定。

Copyright © 2026 Simon Lin. All rights reserved.

**作者：** Simon 林 · X [@linsizhen](https://x.com/linsizhen) · 邮箱：[simonlin0423@gmail.com](mailto:simonlin0423@gmail.com)

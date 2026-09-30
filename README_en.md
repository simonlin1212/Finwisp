<p align="center"><a href="README.md">简体中文</a> | <b>English</b></p>
<h1 align="center">Finwisp</h1>
<p align="center">
  <b>Voice-first financial research assistant</b><br>
  Voice conversation · Market information · Document research · Backtesting · Memory management
</p>
<p align="center">
  <a href="https://github.com/simonlin1212/Finwisp/releases/download/v0.1.0-preview.20260929/Finwisp-Preview-20260929-v2-mac-arm64.zip"><b>Download the latest Mac app (M-series)</b></a> · <a href="https://github.com/simonlin1212/Finwisp/releases/tag/v0.1.0-preview.20260929">Release notes</a>
</p>
<p align="center">
  <img src="https://img.shields.io/badge/macOS-13%2B-black" alt="macOS 13 or later">
  <img src="https://img.shields.io/badge/Apple_Silicon-M_series-black" alt="Apple Silicon M series">
  <img src="https://img.shields.io/badge/Codex-subscription_required-orange" alt="Codex subscription required">
  <img src="https://img.shields.io/badge/Distribution-app_only-blue" alt="App distribution only">
</p>
<p align="center">
  <a href="#download">Download</a> · <a href="#requirements">Requirements</a> · <a href="#installation-and-connection">Setup</a> · <a href="#features">Features</a> · <a href="#current-limitations">Limitations</a> · <a href="CHANGELOG.md">Changelog</a>
</p>

---

Finwisp connects voice conversation, research tools, and local records. Describe a research question, add conditions, or change pages by voice. Review task progress, supporting documents, and calculation results in the app.

**This is a distribution and documentation repository for a closed-source application.** App packages are provided through GitHub Releases. This repository does not contain Finwisp's development source code, user data, or login credentials.

## Download

- [Download the Mac Apple Silicon package](https://github.com/simonlin1212/Finwisp/releases/download/v0.1.0-preview.20260929/Finwisp-Preview-20260929-v2-mac-arm64.zip)
- [View release notes and the SHA-256 checksum file](https://github.com/simonlin1212/Finwisp/releases/tag/v0.1.0-preview.20260929)

Extract the ZIP and move `Finwisp Preview.app` into Applications. GitHub's automatic `Source code (zip/tar.gz)` downloads are snapshots of this documentation repository, not app installers or Finwisp's development source code.

## Requirements

| Item | Current requirement |
| --- | --- |
| Computer | **Apple Silicon M-series Mac only**; Intel Macs, Windows, and Linux are not supported |
| Operating system | macOS 13 or later |
| Model access | **A ChatGPT subscription account with Codex access**; model access, voice access, and usage limits depend on the OpenAI account |
| Local runtime | Codex CLI must be installed and executable at `/opt/homebrew/bin/codex`. Installing the Codex desktop interface alone does not establish this path |
| Network | Required for models, real-time voice, and online data queries |
| Audio | Built-in Mac microphone and speakers only; microphone permission is required |
| Interface | Simplified Chinese only |

Node and Python runtimes are included. Finwisp does not provide or share subscription accounts, and packages contain no signed-in account. This release is offered for subscription access; API-key access is not promised as a substitute for the complete voice experience.

## Installation and connection

1. Confirm that the Mac has an M-series chip and runs macOS 13 or later.
2. Install the local runtime using [OpenAI's official Codex CLI instructions](https://learn.chatgpt.com/docs/codex/cli). Confirm that `/opt/homebrew/bin/codex --version` prints a version. This preview uses that fixed path; installations elsewhere require path setup first.
3. Download the ZIP from Releases, extract it, move the app into Applications, and open it.
4. In Finwisp, open Settings → Model and connection (`设置 → 模型与连接`), sign in with your own ChatGPT subscription account, and check the connection. Product login and records are separate from personal Codex login and records; credentials are not copied from a personal directory.
5. Enable voice from the top-left control and grant microphone permission when macOS asks. Start with a short text question, then test voice.

The package is not Developer ID-signed or notarized by Apple. macOS may report that it cannot verify the developer. After checking the download source and checksum, use the system's Privacy & Security → Open Anyway flow where available. Report the exact message if macOS still refuses to open it. Do not disable system security globally.

## Features

| Feature | Usage |
| --- | --- |
| Voice and text | Ask follow-up questions, add conditions, and navigate by voice. Manual microphone mute pauses input while existing answers and background tasks continue |
| Markets and news | Review major indices, watchlist directions, and news with sources and timestamps; bring relevant items into research |
| Research and documents | Review saved research; import PDF, TXT, and Markdown documents; read pages and cite supporting material |
| Research reports | Prefer the fixed Eastmoney and iWencai entry points; save links and associate accessible originals with the document library |
| Backtesting | Describe a strategy; the agent queries data, organizes calculations, executes them, and checks results. Assumptions and outputs are saved by conversation |
| Watchlists and holdings | Manage records across markets and retain add, correction, and deletion history |
| Memory | Manage communication preferences, research presentation habits, and continuity. Enable, correct, or delete memory; candidate adoption follows the relevant authorization |

## Current limitations

- **This is a Preview release.** Startup, text-model access, packaged calculations, synthetic voice, and physical microphone access have been tested on the developer's Mac. Compatibility has not been validated on other Macs. Availability across subscription accounts, operating-system versions, and audio devices is not guaranteed.
- The research model is fixed to `GPT-5.6-Sol`; real-time voice depends on Codex's native interface. Model permissions, voice permissions, subscription limits, and Codex version differences can affect connection.
- Data sources may be delayed, incomplete, or unavailable. Some entry points require their own service access or configuration. Search does not guarantee access to every report's original document.
- Backtesting depends on available data and explicit assumptions. Daily-bar approximations, intraday paths, auctions, and real execution should be distinguished. Results require checking; the required historical data may not exist for every strategy.
- Voice can still exhibit segmentation, recognition errors, or premature narration. Verify business results against saved tool receipts and research records. Manual mute prevents unrelated speech from entering the active task.
- Local storage does not mean fully offline operation. Relevant input is sent to connected model services during model and voice use. The local transcript setting does not delete service-side history. App and web records are separate and do not sync automatically.
- Automatic updates and Intel Mac, Windows, or Linux packages are not provided yet.

## Feedback

Use [GitHub Issues](https://github.com/simonlin1212/Finwisp/issues). Include the Mac chip, macOS version, Codex version, app version, reproduction steps, and exact error. Do not post credentials, private reports, research records, or holdings details.

## Changelog

See [CHANGELOG.md](CHANGELOG.md). Future app packages will also be provided through Releases.

## Disclaimer

Finwisp supports information organization, research, and simulated calculations. Model responses, third-party data, and backtest results require independent verification. They are not investment advice and do not guarantee returns.

## Copyright

Finwisp is closed-source software. Its product source code is not licensed as open source through this repository. Public app distribution does not grant permission to use or distribute its product source code. Third-party components retain their respective rights and license terms.

Copyright © 2026 Simon Lin. All rights reserved.

**Author:** Simon Lin · X [@linsizhen](https://x.com/linsizhen) · Email: [simonlin0423@gmail.com](mailto:simonlin0423@gmail.com)

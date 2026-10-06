# YourJarvis Link

YourJarvis 的 Windows 朋友版发布仓库。

YourJarvis 是 QcShadow 基于 [OpenJarvis 官方项目](https://github.com/open-jarvis/OpenJarvis)
开发的个人定制分支。OpenJarvis 提供基础的本地 AI 框架；YourJarvis 在此基础上增加了中文优先的
Windows 桌面体验、语音、本地记忆、朋友共享、轻量 ZIP 发布包和多渠道更新。这个仓库只发布
YourJarvis 的朋友版成品，不是 OpenJarvis 官方发布仓库。

正式版本请从 [GitHub Releases](https://github.com/QcShadow/YourJarvis-link/releases) 或国内的 [Gitee 发行版](https://gitee.com/QcShadow/your-jarvis-link/releases) 下载。下载 `JARVIS-Friends-Bootstrap-*.zip`，完整解压后双击 **`JARVIS-Install.exe`**，按中文图形向导选择安装位置、模型/API 和语音，自动完成全部安装与自检。

应用会同时通过 GitHub 的 `update-github.json` 和 Gitee 的 `update.json` 检查更新，并选择版本号较高的清单，在应用内下载对应渠道的新版 ZIP。个人配置、聊天记录、模型和日志保存在应用目录的 `data`、`models`、`logs` 中；覆盖升级时保留这些目录。

本仓库不保存开发源码、API 密钥、个人配置、数据库或模型权重。开发源码保存在私有仓库 `QcShadow/YourJarvis-dev`。

## 首次安装

1. 下载最新 ZIP。
2. 解压到自己的可写目录，例如 `D:\YourJarvis`。
3. 双击 **`JARVIS-Install.exe`**，按窗口顺序完成安装。
4. 不确定时保持轻量本地模型和文字模式。首次安装需要联网，向导自动补齐独立 Python、WebView2、所需 Ollama 与模型，以及选择的语音资源。文字模式至少预留 4 GB，语音建议预留 10 GB。
5. 完成后使用桌面快捷方式或 `JARVIS.exe`。失败时可在窗口查看原因、打开日志、返回修改方案并重试。

从 0.1.1 升级：退出应用，把新版 ZIP 中 `JARVIS-Share` 内的文件覆盖到原目录，保留 `config.toml`、`credentials.toml`、`data`、`models` 和 `logs`。打开安装向导，默认保留当前配置并修复环境。旧 `bootstrap.cmd`、`setup-jarvis.cmd` 都会进入同一向导，无需分别运行。

不要直接在压缩包内运行，也不要安装到 `Program Files`。

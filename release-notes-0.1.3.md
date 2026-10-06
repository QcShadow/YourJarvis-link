# JARVIS v0.1.3

朋友版改为一个 EXE：下载 JARVIS-Setup-0.1.3.exe 后直接双击，选择目录与模型/语音方案，等待安装通过再启动。

- 自动按顺序准备 Python、运行依赖、桌面组件、模型及所选语音。Gitee 优先，失败自动切换 GitHub；支持续传与 SHA-256 校验。
- 默认 Qwen2.5 0.5B、CPU Ollama、SenseVoice、Kokoro、英文识别模型、Python、依赖和 WebView2 离线组件均提供发布资源。运行库和语音使用独立 Gitee 资源仓库，安装器自动选择；无需手动解压资源分块。
- 修复 Windows PowerShell 模块环境、命令参数引号、搬移后的 Python 路径、中文目录的英文语音加载，以及安装完成但后台无法启动的问题。
- 安装完成前实际检查模型连接、后台启动、页面及聊天；语音安装还会实际加载识别模型并生成音频。启动失败页提供修复、重试和打开日志。
- 升级请选择原安装目录。保留配置、密钥、人物设置、聊天、记忆与已下载模型，清理旧 bootstrap 和独立语音下载入口。

默认推荐“轻量本地模型 + 先使用文字”；需要语音时在向导选择中文男声/女声或英文。自定义模型和第三方 API 由其上游提供，未包含于默认镜像。首次下载仍需联网，完成后默认本地模型与语音可离线使用。

验证：31 项安装/下载回归测试通过；新 EXE 在中文及空格路径、空 PSModulePath 的 Windows PowerShell 下完成安装；识别模型加载、中文/英文音频合成及真实后端/页面/聊天检查通过。

资源地址：
- https://gitee.com/QcShadow/your-jarvis-runtime/releases/tag/v0.1.3
- https://gitee.com/QcShadow/your-jarvis-speech/releases/tag/v0.1.3

包内保留上游许可证；发布物不包含制作者的个人配置、密钥、聊天或记忆。

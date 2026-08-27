# L-1 File To Text

L-1 File To Text 是 Windows 本地音视频转写工具。安装包提供界面与 CPU 识别运行环境；模型权重不随包分发，首次使用时由用户在“资源中心”主动下载。

## 安装与首次使用

1. 运行唯一的 `L-1 File To Text Setup` 安装包并完成安装。
2. 首次启动选择模型资源目录。
3. 在资源中心下载 Whisper Small（速度优先，约 510 MB）或 Whisper Medium（准确度优先，约 1.53 GB）。
4. 添加音频或视频，选择输出目录与 TXT/MD/HTML 输出后开始任务。

视频输入需要 Windows `PATH` 中可用的 FFmpeg。本正式版不内置 FFmpeg，避免分发来源和许可证不清的二进制；WAV 音频可直接处理。模型下载需要连接 `huggingface.co`，转写与输出在本机完成。

## 配置

- Windows 10/11 64 位。
- 基础安装约 760 MB；建议至少预留 2 GB。
- Whisper Small：建议 4 GB 内存，另需约 510 MB 模型空间。
- Whisper Medium：建议 8 GB 内存，另需约 1.53 GB 模型空间。
- 可选 7B/8B 本地语言模型：建议 12 GB 内存，每个另需约 4.7–5.0 GB；CPU 推理较慢。
- 本正式版为 CPU 基础版，不包含 NVIDIA CUDA/cuDNN 运行时。

## 卸载与数据

可从 Windows“应用和功能”或安装目录卸载器移除程序。卸载不会删除 `%LOCALAPPDATA%\L-One\L-1 File To Text`、用户选择的模型目录或输出文件，以避免误删；确认不再需要后可手动删除。

Windows SmartScreen 可能因安装包尚未进行商业代码签名而提示“未知发布者”。请先核对 `SHA256SUMS` 中的 SHA-256；不要在来源不明或哈希不一致时继续安装。

可在安装包所在目录打开 PowerShell，执行：

```powershell
Get-FileHash -Algorithm SHA256 -LiteralPath '.\L-1 File To Text Setup v2.0.8.exe'
```

预期 SHA-256：`0B4080D6CF4FB9B47FA230CB8AC3C14A37C7202BEDC266869EE8BBEDB71418D8`。字母大小写不影响比较，但 64 位十六进制字符必须完全一致。

更完整的数据与联网说明见 `PRIVACY.md`，第三方许可见 `THIRD_PARTY_NOTICES.md` 和 `SBOM.json`。

# L-1 File To Text — 第三方组件与许可声明

适用于随本文档交付的 CPU 候选版本。本包不含模型权重、ONNX 资产、NVIDIA CUDA/cuBLAS/cuDNN DLL，也不含 FFmpeg 可执行文件或 OpenCV 的 FFmpeg DLL。实际版本号及文件哈希见发行清单；实际随包组件、版本、purl、声明许可证、许可证文本位置与元数据哈希见同目录 `SBOM.json`（CycloneDX 1.6）。

| 组件 | 版本 | 随包形式 | 许可证 / 来源 |
|---|---:|---|---|
| PySide6、PySide6-Essentials、PySide6-Addons、shiboken6 | 6.9.1 | Qt DLL 与 Python 绑定，运行时动态加载 | LGPL-3.0-only（本包选择 LGPL 路径）；https://doc.qt.io/qtforpython-6/ |
| Python | 3.12.13 | 隔离 Worker Runtime | PSF-2.0；https://docs.python.org/3/license.html |
| faster-whisper | 1.1.1 | Worker Python 包 | MIT；https://github.com/SYSTRAN/faster-whisper |
| CTranslate2 | 4.8.1 | Worker Python 包 | MIT；https://github.com/OpenNMT/CTranslate2 |
| Tokenizers | 0.22.2 | Whisper 分词运行时 | Apache-2.0；https://github.com/huggingface/tokenizers |
| tqdm | 4.70.0 | 资源下载进度 | MPL-2.0 AND MIT；https://github.com/tqdm/tqdm |
| NumPy | 2.5.2 | Worker Python 包 | BSD-3-Clause；https://github.com/numpy/numpy |
| imageio-ffmpeg | 0.5.1 | Worker Python 包；不含其二进制目录中的 `.exe` | BSD-2-Clause；https://github.com/imageio/imageio-ffmpeg |
| PyInstaller | 6.14.2 | 仅用于构建；启动引导代码位于应用中 | GPL-2.0-or-later with bootloader exception；https://pyinstaller.org/en/stable/license.html |

## Qt / PySide6 的 LGPL 说明

本程序通过 PySide6 的 `.pyd` 与 Qt 的 `.dll` 在运行时动态链接，未静态链接 Qt。Qt 相关 DLL 位于安装目录的 `_internal\\PySide6`，用户可在关闭程序后以接口兼容的版本替换这些 DLL；替换导致的问题不由 L-One 支持。Qt for Python 的源码、许可证和构建说明见 https://code.qt.io/cgit/pyside/pyside-setup.git/ 与 https://doc.qt.io/qtforpython-6/overviews/qtdoc-lgpl.html 。

本目录应随安装包一同保留 `LICENSES\\LGPL-3.0.txt`、`LICENSES\\GPL-3.0.txt` 与各 Python 包自带的许可证副本。构建脚本会在生成候选包前核验它们存在。

CTranslate2、Tokenizers 与 tqdm 的项目许可证/版权正文分别保存在 `LICENSES\\CTRANSLATE2-MIT.txt`、`LICENSES\\TOKENIZERS-APACHE-2.0.txt`、`LICENSES\\TQDM-LICENCE.txt` 与 `LICENSES\\MPL-2.0.txt`。SBOM 使用安装包内实际相对路径引用这些文件。

## 明确不随包分发的组件

- **FFmpeg 可执行文件**：历史构建发现的 `ffmpeg-win64-v4.2.2.exe` 含 `--enable-gpl --enable-version3`，未进入本包。视频输入需要用户自行安装兼容 FFmpeg，并由用户自行选择其许可证与来源；音频输入不需要 FFmpeg。
- **OpenCV / RapidOCR / ONNX Runtime**：未进入本包。历史候选中的 OpenCV FFmpeg DLL、RapidOCR 模型与 ONNX Runtime 测试模型均已从公开 CPU 基础版剥离；图片 OCR 不属于本版公开能力。
- **FunASR / ModelScope / PyTorch 运行时**：未进入本包。公开基础版仅提供 Whisper Small 与 Whisper Medium 两档本地识别；FunASR 在依赖、模型和许可闭环完成前不向用户展示为可用能力。
- **ModelScope Hub / Torch-Complex / FunASR 辅助依赖**：未进入本包；这些依赖不属于当前 Whisper CPU 运行链。
- **NVIDIA CUDA / cuBLAS / CUDA NVRTC / cuDNN DLL**：未进入本包。当前公开候选为 CPU 基础版；GPU 组件仅会在取得精确版本、再分发条款和许可证材料后作为独立可审计组件提供。
- **模型权重**：未进入本包；只会在用户主动于资源中心下载后保存到用户选定的资源目录。

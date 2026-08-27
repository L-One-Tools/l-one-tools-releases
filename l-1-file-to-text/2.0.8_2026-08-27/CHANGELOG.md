# CHANGELOG

## 2.0.8 — 2026-08-27

- 补齐 CTranslate2、Tokenizers、tqdm 与 PyInstaller 的许可证正文，并让 SBOM 指向安装包内实际路径。
- 从公开 CPU 运行时剥离 ModelScope Hub、Torch-Complex、pytest、PyInstaller 及其他非当前 Whisper 链路所需的残留依赖。
- 发行清单与 SHA-256 清单改为递归覆盖 `LICENSES` 等白名单子目录。
- 增加 L-One 自有程序权利声明；公开下载仓库不代表程序源码采用开源许可。
- README 增加普通用户可直接执行的 Windows `Get-FileHash` 命令和候选包预期哈希。
- 明确当前没有可供公众降级的旧正式版；安全撤回时应卸载问题版本并保留用户数据，等待经审查的修复版。

发行边界：公开 CPU 版仍不包含 GPU 运行时；正式二进制必须完成恶意文件深度扫描、独立安装、正常启动和卸载验证后方可公开。

## 2.0.7 — 2026-08-26

- 修复 PyInstaller 启动包缺少 tkinter/Tcl/Tk 导致的启动崩溃。
- 修复公开 CPU 版误选 CUDA 的问题；缺少完整 NVIDIA 运行时时明确使用 CPU int8。
- 中文识别固定中文提示并抑制跨片段重复，改善含英文背景音乐时的重复和误识别。
- 公开基础版收窄为 Whisper Small/Medium，剥离 FunASR、ModelScope、PyTorch、OpenCV、RapidOCR、ONNX Runtime 与 NVIDIA 运行时。
- 安装包不含模型权重、测试媒体、用户数据、缓存或日志。
- 增加 CycloneDX 1.6 SBOM、隐私说明、模型来源和第三方许可证材料。
- 修复覆盖升级保留旧 Worker Runtime 的问题；升级时精确重建程序运行目录，同时保留模型、输出、设置与用户资源。

仍有限制：视频输入依赖用户系统提供 FFmpeg；GPU 加速未包含在本 CPU 候选；模型需由用户主动下载；可选本地翻译模型在低配置 CPU 上可能很慢。

# CHANGELOG

## 2.0.7 — 2026-08-26

- 修复 PyInstaller 启动包缺少 tkinter/Tcl/Tk 导致的启动崩溃。
- 修复公开 CPU 版误选 CUDA 的问题；缺少完整 NVIDIA 运行时时明确使用 CPU int8。
- 中文识别固定中文提示并抑制跨片段重复，改善含英文背景音乐时的重复和误识别。
- 公开基础版收窄为 Whisper Small/Medium，剥离 FunASR、ModelScope、PyTorch、OpenCV、RapidOCR、ONNX Runtime 与 NVIDIA 运行时。
- 安装包不含模型权重、测试媒体、用户数据、缓存或日志。
- 增加 CycloneDX 1.6 SBOM、隐私说明、模型来源和第三方许可证材料。
- 修复覆盖升级保留旧 Worker Runtime 的问题；升级时精确重建程序运行目录，同时保留模型、输出、设置与用户资源。

仍有限制：视频输入依赖用户系统提供 FFmpeg；GPU 加速未包含在本 CPU 候选；模型需由用户主动下载；可选本地翻译模型在低配置 CPU 上可能很慢。

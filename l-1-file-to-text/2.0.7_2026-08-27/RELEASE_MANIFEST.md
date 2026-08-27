# L-1 File To Text 2.0.7 — RELEASE MANIFEST

## 构建来源

- 正式版本：`2.0.7`
- 构建日期：`2026-08-26`（Asia/Shanghai）
- 最终复核日期：`2026-08-27`（Asia/Shanghai）
- Git 提交：`d5bbd969c377b0eb04a3d0bc3d803974a464d230`
- Git 标签：`v2.0.7`
- 构建前工作树：干净
- 构建命令：`scripts/build_release.ps1 -Version 2.0.7 -PublicCpuCandidate -InstallerOnly`
- Python：`3.12.13`
- PyInstaller：`6.14.2`
- Inno Setup：`6.7.3`

## 正式产物

- 文件：`L-1 File To Text Setup v2.0.7.exe`
- 大小：`176378304` bytes
- SHA-256：`5D51C4F462688C51218F6BE1B7931EF09FFB7D6AA08B95D7F9DCEBBD9FBE06C7`
- 构建运行时：`14184` 个文件，`756535468` bytes
- CycloneDX：`1.6`，`105` 个组件，未知许可证字段 `0`

## 包内容门禁

- 测试音视频：`0`
- 模型权重（ONNX/GGUF/PT/CKPT/SafeTensors）：`0`
- FFmpeg 可执行文件及 OpenCV FFmpeg DLL：`0`
- NVIDIA CUDA/cuBLAS/cuDNN DLL：`0`
- 用户文件、任务数据库、输出、缓存和日志：`0`

## 验证结果

- 源码自动测试：`215 passed`。
- 从旧安装目录覆盖升级：退出码 `0`。
- 升级后旧 Worker Runtime 包：`0`；Worker Runtime 模型权重：`0`。
- 用户原有模型权重：保留 `6` 个，未被升级清理规则删除。
- 本机正式安装目录直接启动两次：均在 6 秒后保持运行，无错误弹窗。
- 30 秒授权中文样例：完成，CPU `int8`，耗时 `30.89` 秒，模型加载 `8.26` 秒，输出 `134` 字，无警告。
- 独立目录静默安装：退出码 `0`；连续启动两次通过。
- 独立目录静默卸载：退出码 `0`，主程序和卸载器均移除。
- Windows 安装登记已恢复到 `D:\tools\L-1 File To Text`，登记版本与 Worker 源码版本均为 `2.0.7`。

验证材料仅保存脱敏汇总结论；用户媒体和转写正文不进入公开发布目录。

## 已知限制

- 这是 CPU 基础版，不包含 NVIDIA GPU 运行时。
- 模型不随安装包分发，由用户在资源中心主动下载。
- 视频输入需要系统 `PATH` 中存在兼容 FFmpeg；安装包不分发 FFmpeg。
- 安装包未进行商业代码签名，Windows SmartScreen 可能显示未知发布者。

## 回退

内部回退版本：`2.0.6`，安装包 SHA-256：`FE679DD35E6A58AC70F832B41B53388859940EDF525CF7CC54E4FDD0F31A795B`。该回退包仅供内部恢复，不作为公开附件。

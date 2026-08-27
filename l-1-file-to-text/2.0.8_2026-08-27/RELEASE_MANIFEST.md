# L-1 File To Text 2.0.8 — RELEASE MANIFEST

## 构建来源

- 正式版本：`2.0.8`
- 构建与复核日期：`2026-08-27`（Asia/Shanghai）
- 产品源码提交：`ff75b9fe6ed54743f91866516e6eeff8eb83110f`
- 最终验收记录提交：`2a6217471386c2cf6a1aa8b3d91b4a601b116946`
- 构建分支：`codex/release-2.0.8-candidate-1`
- 构建命令：`scripts/build_release.ps1 -Version 2.0.8 -PublicCpuCandidate`
- Python：`3.12.13`
- PyInstaller：`6.14.2`
- Inno Setup：`6.7.3`

## 正式产物

- 文件：`L-1 File To Text Setup v2.0.8.exe`
- 大小：`174867225` bytes
- SHA-256：`0B4080D6CF4FB9B47FA230CB8AC3C14A37C7202BEDC266869EE8BBEDB71418D8`
- 构建运行时：`13753` 个文件，`750421861` bytes
- CycloneDX：`1.6`，`95` 个组件，未知许可证字段 `0`

## 包内容门禁

- 测试音视频：`0`
- 模型权重：`0`
- FFmpeg 可执行文件及 OpenCV FFmpeg DLL：`0`
- NVIDIA CUDA/cuBLAS/cuDNN DLL：`0`
- 用户文件、任务数据库、输出、缓存和日志：`0`
- 缺失许可证正文：`0`
- 禁止运行时残留：`0`

## 验证结果

- 源码自动测试：`219 passed`。
- `compileall`：通过。
- `pip check`：无损坏依赖。
- 独立目录安装：退出码 `0`；主程序与卸载器均存在。
- 正常窗口连续启动两次：每次 10 秒后仍保持运行；Windows Application Error 为 `0`。
- 独立目录卸载：退出码 `0`；主程序与卸载器均移除。
- ClamAV 1.5.4 深度扫描：实际扫描 `180.99 MiB`，感染文件 `0`，退出码 `0`。

完整证据见 `VALIDATION-2.0.8.md`。验证材料仅保存脱敏汇总结论；用户媒体和转写正文不进入公开发布目录。

## 已知限制

- 这是 CPU 基础版，不包含 NVIDIA GPU 运行时。
- 模型不随安装包分发，由用户在资源中心主动下载。
- 视频输入需要系统 `PATH` 中存在兼容 FFmpeg；安装包不分发 FFmpeg。
- 安装包未进行商业代码签名，Windows SmartScreen 可能显示未知发布者。

## 发布与撤回

- 2.0.8 发布后取代 2.0.7 成为唯一推荐版本。
- 2.0.7 保留为历史证据，不作为默认下载。
- 如发现哈希、隐私或安全异常，应立即标记并停止分发 2.0.8，保留用户数据后等待审查通过的修复版。

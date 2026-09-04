# 模型与组件边界

“L-1 File To Text v2.1.0 公开内测版”安装包不包含任何语音识别模型权重，也不包含 FFmpeg 可执行文件。

资源中心提供 FireRedASR2 AED INT8 的本地 CPU 中文识别候选。固定来源为 `csukuangfj2/sherpa-onnx-fire-red-asr2-zh_en-int8-2026-02-26` 的固定修订 `374cff185e952c40fcf2f6da972a3b6cf340608d`；模型卡说明其来自 FireRedTeam/FireRedASR2-AED。上游模型页面标注 Apache-2.0。资源中心逐文件校验 `encoder.int8.onnx`、`decoder.int8.onnx` 与 `tokens.txt` 的大小和 SHA-256。

FFmpeg 由资源中心单独从 BtbN FFmpeg-Builds 的 Windows x64 GPL shared 压缩包下载；固定记录为 `master latest / 2026-09-03`，压缩包 SHA-256 为 `f166b699de34213b7e239f67e21d8743a2d067fd753a62bb777c06586ff18d6f`。下载包为 76,980,843 字节，解压安装占用 201,790,751 字节；压缩包内 `LICENSE.txt` 为 GNU GPL v3。该组件不随安装包分发；下载前会显示来源与 GPL v3 链接，下载后校验压缩包 SHA-256。

模型、模型许可和 FFmpeg 都不得从本安装包反向提取或另行分发。资源只在用户确认下载后联网；保存到用户选择的资源目录，不写入程序安装目录。下载失败、空间不足或校验失败时不会标记为可用。

本候选不提供自动中文翻译模型，也不提供 `.srt` / `.vtt` 中文字幕生成组件。

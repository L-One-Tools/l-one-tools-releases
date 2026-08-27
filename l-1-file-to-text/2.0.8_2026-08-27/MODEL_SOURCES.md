# 模型不随包分发：来源与用户触发方式

安装包不包含任何模型权重。用户只能在资源中心主动选择下载；下载目标和保存位置在开始前由应用显示。模型许可由模型发布方决定，L-One 不以安装包再分发这些权重。

| 模型 | 固定版本/条目 | 官方下载页 | 许可页面 |
|---|---|---|---|
| Whisper Small | `536b0662742c02347bc0e980a01041f333bce120` | https://huggingface.co/Systran/faster-whisper-small | https://huggingface.co/Systran/faster-whisper-small/blob/main/README.md |
| Whisper Medium | `08e178d48790749d25932bbc082711ddcfdfbc4f` | https://huggingface.co/Systran/faster-whisper-medium | https://huggingface.co/Systran/faster-whisper-medium/blob/main/README.md |
| Qwen2.5 7B GGUF | 2.5 | https://huggingface.co/Qwen/Qwen2.5-7B-Instruct-GGUF | https://huggingface.co/Qwen/Qwen2.5-7B-Instruct-GGUF/blob/main/LICENSE |
| MiniCPM4 8B GGUF | 4 | https://huggingface.co/openbmb/MiniCPM4-8B-GGUF | https://huggingface.co/openbmb/MiniCPM4-8B-GGUF/blob/main/LICENSE |

资源清单 `resources/models-v1.json` 是应用内可见的精确文件来源；本候选不提供 FunASR/ModelScope 下载条目。模型发布方可能变更许可或访问条件，下载前应以模型页显示的条款为准。

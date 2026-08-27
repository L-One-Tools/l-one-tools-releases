# 隐私与联网边界

本候选包默认在本机处理用户选择的音视频、临时音频、任务记录与输出文件。应用不上传转写文本、媒体文件或模型权重到 L-One 服务。

## 已核实的联网行为

- 用户在“资源中心”主动点击下载模型时，当前公开清单会访问 Hugging Face (`huggingface.co`) 中对应的 Whisper 或可选语言模型条目。代码保留 ModelScope 下载适配器，但本版公开资源清单不提供 ModelScope/FunASR 条目。
- 可选本地语言模型服务只监听及访问 `127.0.0.1` 的本机端口；不把提示词发送到外部 API。
- 视频输入需要用户自行安装的 FFmpeg；该 FFmpeg 的联网行为不属于本应用控制范围。

## 未发现但仍持续核验的行为

对本项目应用代码进行了静态网络调用扫描，未发现遥测、分析 SDK、崩溃上报 SDK 或 L-One 远程服务端点。该结论不覆盖操作系统、显卡驱动、第三方模型站点或用户自行安装的 FFmpeg；安装前请审阅其各自条款。

## 本机保存与删除

- 默认应用数据根目录：`%LOCALAPPDATA%\L-One\L-1 File To Text`。
- 设置：`%LOCALAPPDATA%\L-One\L-1 File To Text\Config\settings.json`。
- 任务记录：`%LOCALAPPDATA%\L-One\L-1 File To Text\Config\task-history.json`；可在“任务记录”中删除，删除记录不会删除原始文件或输出。
- 默认模型目录：`%LOCALAPPDATA%\L-One\L-1 File To Text\Resources`；若用户首次启动时选择其他资源目录，则模型和下载中的 `.download` 暂存目录均位于该目录。可在资源中心删除模型。
- 缓存与临时音频：`%LOCALAPPDATA%\L-One\L-1 File To Text\Cache` 和其 `Temp` 子目录。视频提取产生的临时音频在任务成功、失败或取消后均通过清理流程删除；异常断电可能留下文件，可由用户删除 `Temp` 内容。
- 输出：默认保存到源文件同目录或用户明确选择的输出目录。
- 卸载：卸载程序只移除安装目录和程序快捷方式，不自动删除 `%LOCALAPPDATA%\L-One\L-1 File To Text`、用户选择的资源目录或输出，避免误删用户数据；用户可在确认不再需要后手动删除这些目录。

支持排查时，仅应收集应用版本、系统版本、错误摘要和用户明确同意提供的最小复现材料；不要公开分享原始媒体、转写文本、模型目录或完整日志。

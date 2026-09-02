# L-One Tools Releases

这是 L-One 工具唯一的官方下载与版本资料入口。

本仓库只保存已验收版本的使用说明、更新记录、隐私说明、软件成分清单、第三方许可证、发布清单和校验值。安装包作为 GitHub Release 附件提供，不进入 Git 历史。

本仓库不包含开发源码、模型权重、测试媒体、用户数据、缓存、日志、Token、密钥或内部工作资料。L-One 自有程序为专有软件；公开下载和公开版本资料不代表开源，也不授予开发源码许可。第三方组件继续受其各自许可证约束。

## 当前版本

| 工具 | 版本 | Windows | 版本资料 | 下载 |
|---|---:|---|---|---|
| L-1 File To Text | 2.0.8 | Windows 10/11 64 位 | [2.0.8 版本资料](l-1-file-to-text/2.0.8_2026-08-27/) | [GitHub Release](https://github.com/L-One-Tools/l-one-tools-releases/releases/tag/l-1-file-to-text-v2.0.8) |
| L-1 网页拓印 | v0.2.2 公开内测 | Chrome 116+ | [v0.2.2 版本资料](l-1-web-imprint/0.2.2_2026-09-03/) | [GitHub Release](https://github.com/L-One-Tools/l-one-tools-releases/releases/tag/l-1-web-imprint-v0.2.2) |

“公开内测”不是正式稳定版。请先阅读版本资料中的支持范围、隐私说明与已知限制。

## 下载与校验

请只从上表对应的 GitHub Release 下载安装包。下载后在 PowerShell 执行：

```powershell
Get-FileHash -Algorithm SHA256 -LiteralPath '.\L-1 File To Text Setup v2.0.8.exe'
```

2.0.8 安装包的预期 SHA-256：

```text
0B4080D6CF4FB9B47FA230CB8AC3C14A37C7202BEDC266869EE8BBEDB71418D8
```

哈希不一致时请停止安装，并从官方 Release 重新下载。

## 撤回与回退

如发现校验异常、下载异常或安全/隐私风险，相关 Release 将被标记并停止继续分发。2.0.8 是当前正式版本；2.0.7 仅保留历史记录，不再作为推荐下载。用户可先卸载程序，卸载不会自动删除用户选择的模型目录和输出文件。替代或恢复版本只会在本仓库发布。

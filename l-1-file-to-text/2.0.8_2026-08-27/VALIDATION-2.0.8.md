# L-1 File To Text 2.0.8 正式版发布验证记录

验证时间：2026-08-27（Asia/Shanghai）
验证设备：A 电脑
正式版状态：本地发行验收通过；可进入公开渠道上传

## 正式安装包

- 文件：`release/v2.0.8/L-1 File To Text Setup v2.0.8.exe`
- 文件大小：174,867,225 bytes
- SHA-256：`0B4080D6CF4FB9B47FA230CB8AC3C14A37C7202BEDC266869EE8BBEDB71418D8`
- 安装器 ProductVersion：`2.0.8`
- 安装器 ProductName：`L-1 File To Text`

## 构建与质量检查

- 完整自动测试：219 passed。
- `compileall`：通过。
- `pip check`：`No broken requirements found`。
- CycloneDX 1.6 SBOM：95 个组件；未知许可证 0；缺失许可证正文 0；禁止运行时文件 0。
- 公开 CPU 运行时清洁检查：通过。

## 安装、启动与卸载

- 隔离安装：退出码 0；主程序与卸载器均存在。
- 正常启动：正式安装版连续启动两次，每次 10 秒后仍正常运行，窗口标题均为 `L-1 File To Text`。
- Windows Application Error：0。
- 隔离卸载：退出码 0；测试目录中的主程序与卸载器均已移除。
- 第一次安装尝试因用户原有工具仍在运行而退出，关闭原有工具后按相同安装包重新验证通过；没有强制终止用户进程。

## 恶意文件深度扫描

- 扫描器：ClamAV 1.5.4。
- 扫描器官方压缩包已使用 Cisco Talos 公钥完成 GPG 签名验证，结果为 `Good signature`。
- 病毒库：main 63、daily 28105、bytecode 339；已知病毒 3,628,033。
- 参数：启用压缩包扫描，单文件上限 300 MiB、总扫描上限 600 MiB、递归深度 30。
- 实际扫描：180.99 MiB；读取 166.77 MiB；感染文件 0；退出码 0。
- 日志：`E:\L1 Control Center\release-validation\l-1-file-to-text\2.0.8\clamav-deep-scan.log`。

## 公开上传边界

- 本地完整归档中的 `Source Code Backup` 与便携包不是本次公开上传材料。
- 对外渠道只允许上传正式安装包、README、CHANGELOG、权利声明、隐私说明、模型来源、SBOM、第三方许可、许可证正文、发行清单和 SHA-256 校验文件。
- 公开上传后必须匿名重新下载安装包，并再次核对 SHA-256 与本记录一致。

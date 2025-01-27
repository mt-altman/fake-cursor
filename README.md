# Fake Cursor

一个用于重新生成 Cursor 设备 ID 和设置 Access Token 的 Cursor 扩展。

## 功能

- 重新生成设备 ID（包括 devDeviceId, machineId, sqmId, macMachineId）
- 设置 Access Token 并激活 Pro 会员
- 自动备份原有配置文件
- 支持自定义配置文件路径
- 自动清理设备标识文件
- **读取 Access Token**: 通过命令面板读取当前的 Access Token

## 使用方法

1. 按下 `Ctrl+Shift+P` (Windows/Linux) 或 `Cmd+Shift+P` (Mac) 打开命令面板
2. 选择以下命令之一：
   - `Fake Cursor: Regenerate Device ID`: 重新生成设备 ID 并清空认证信息
   - `Fake Cursor: Regenerate & Set Token`: 重新生成设备 ID 并设置 Access Token（可从 cursor.sh 网站 Cookies 中的 WorkosCursorSessionToken 获取，如 `user_01OJGGAOEIIYNGY4ISYAJT1U8R%3A%3AeyJhbGciOiJIU...` 中 `%3A%3A` 后面的 `eyJhbGciOiJIU...` ）
   - `Fake Cursor: Read Token`: 读取当前的 Access Token
3. 根据提示完成操作
4. 操作完成后 Cursor 将自动退出，重启后生效

## 配置选项

在 Cursor 设置中可以配置以下选项：

- `fake-cursor.storagePath`: 自定义配置文件所在文件夹的路径。留空则使用默认路径：
  - Windows: `%APPDATA%/Cursor/User/globalStorage`
  - macOS: `~/Library/Application Support/Cursor/User/globalStorage`
  - Linux: `~/.config/Cursor/User/globalStorage`

## 注意事项

- 执行命令前会自动备份原有配置文件（`.backup` 后缀）
- 支持 Windows、Mac 和 Linux 系统
- 操作会清空现有认证信息，请确保备份重要数据
- 修改后需要重启 Cursor 才能生效
- 如果配置文件不存在，可以手动选择文件夹位置

## 免责声明

本扩展仅供学习和测试使用。使用本扩展可能违反 Cursor 的服务条款，请自行承担使用风险。

## 开源协议

本项目采用 [Creative Commons Attribution-NonCommercial 4.0 International License](https://creativecommons.org/licenses/by-nc/4.0/) 开源协议。

这意味着您可以：
- ✅ 复制、分发本项目
- ✅ 修改、演绎本项目
- ✅ 私人使用

但必须遵循以下规则：
- 📝 署名 - 标明原作者及修改情况
- 🚫 非商业性使用 - 不得用于商业目的
- 🔄 相同方式共享 - 修改后的作品需使用相同的协议

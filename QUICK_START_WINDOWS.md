# Windows 快速开始指南

## 🚀 5分钟快速打包

### 1. 准备环境（首次）

```powershell
# 安装 Node.js（如果还没有）
# 下载: https://nodejs.org/

# 验证安装
node --version
npm --version

# 安装构建工具
npm install --global windows-build-tools
```

### 2. 克隆项目

```bash
git clone https://github.com/crispvibe/Windsurf-Tool.git
cd Windsurf-Tool
```

### 3. 安装依赖

```bash
npm install
```

### 4. 打包

```bash
npm run build:win
```

### 5. 查看结果

```bash
# 打包完成后，在 dist 目录查看
dir dist
```

输出文件：
- `Windsurf-Tool 1.0-1.0.0-x64.exe` - 安装程序
- `Windsurf-Tool-1.0.0-portable.exe` - 便携版

## 📝 常见问题快速解决

### robotjs 编译失败

```bash
# 重新安装 robotjs
npm uninstall robotjs
npm install robotjs

# 或使用 electron-rebuild
npm install --save-dev electron-rebuild
npx electron-rebuild
```

### 缺少 Visual Studio Build Tools

```powershell
# 方式 1: 使用 npm（推荐）
npm install --global windows-build-tools

# 方式 2: 手动安装
# 访问: https://visualstudio.microsoft.com/downloads/
# 下载: Build Tools for Visual Studio
# 安装时选择: "Desktop development with C++"
```

### 打包速度慢

```bash
# 使用淘宝镜像加速
npm config set registry https://registry.npmmirror.com
npm config set electron_mirror https://npmmirror.com/mirrors/electron/

# 重新安装
npm install
```

## 🎯 测试打包结果

### 测试安装程序

1. 双击 `Windsurf-Tool 1.0-1.0.0-x64.exe`
2. 选择安装路径
3. 完成安装
4. 从桌面启动应用
5. 测试所有功能

### 测试便携版

1. 直接运行 `Windsurf-Tool-1.0.0-portable.exe`
2. 测试所有功能
3. 检查配置文件位置

## ✅ 功能测试清单

- [ ] 应用正常启动
- [ ] 界面显示正常
- [ ] 配置邮箱功能
- [ ] 测试 IMAP 连接
- [ ] 批量注册功能
- [ ] 账号管理功能
- [ ] 账号切换功能
- [ ] robotjs 键盘模拟
- [ ] 窗口检测和激活
- [ ] 进程管理

## 🔗 相关文档

- [完整打包指南](WINDOWS_BUILD.md)
- [Windows 适配说明](WINDOWS_ADAPTATION.md)
- [测试清单](WINDOWS_TEST_CHECKLIST.md)

## 💡 提示

1. **首次打包可能需要 10-20 分钟**
   - 下载依赖
   - 编译原生模块
   - 打包应用

2. **建议在干净的 Windows 环境测试**
   - 虚拟机
   - 测试机器
   - 确保没有其他软件干扰

3. **打包前检查**
   - 代码已提交
   - 版本号已更新
   - 测试已通过

4. **遇到问题**
   - 查看错误信息
   - 搜索 GitHub Issues
   - 加入 QQ 群求助

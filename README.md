# Frida Android工具箱

这是一个基于Frida的Android应用逆向分析工具集，提供了完整的PowerShell和Python实现版本。

## 最新版本 - v2.1 Release

**正式发布版本** (2024-12-19)
- 主文件: `frida_toolbox_v2.1_release.ps1`
- 状态: 稳定版本，推荐使用
- 详细说明: 查看发布说明文档

## 核心功能

### PowerShell版本特性
- 多设备管理和自动检测
- 进程附加、生成和终止
- Frida脚本无缝集成
- 后台任务管理系统
- 交互式菜单界面
- 完善的错误处理

### 主要文件
- `frida_toolbox_v2.1_release.ps1` - 主程序(正式版)
- `job_management_enhancement.ps1` - Job管理模块
- `frida_init.ps1` - 初始化脚本
- `frida_script_manager.ps1` - 脚本管理器

## 快速开始

```powershell
# 显示帮助
.\frida_toolbox_v2.1_release.ps1 -Help

# 启动交互式菜单
.\frida_toolbox_v2.1_release.ps1 -Choice menu

# 直接执行完整初始化
.\frida_toolbox_v2.1_release.ps1 -Choice 1
```

## 环境要求

- Windows PowerShell 5.0+
- Frida工具链 (`pip install frida-tools`)
- ADB (Android Debug Bridge)
- 已root的Android设备或模拟器

## 安装步骤

1. **安装Frida**:
   ```bash
   pip install frida-tools
   ```

2. **配置ADB**:
   - 确保ADB在系统PATH中
   - 启用设备的USB调试模式

3. **下载项目**:
   ```bash
   git clone https://github.com/heihuo000/frida-android-toolbox.git
   cd frida-android-toolbox
   ```

4. **运行工具**:
   ```powershell
   .\frida_toolbox_v2.1_release.ps1
   ```

## 功能说明

### 主要操作选项
1. **完整初始化环境（后台模式）** - 一键完成所有环境配置
2. **仅部署frida-server** - 只部署服务端到设备
3. **启动frida-server（后台运行）** - 后台启动Frida服务
4. **仅启动应用** - 启动目标应用程序
5. **注入脚本** - 向运行中的应用注入Frida脚本
6. **重启应用并注入** - 重启应用并自动注入脚本
7. **检查环境状态** - 检查所有组件状态
8. **快速重连frida** - 快速重新连接Frida服务
9. **停止frida-server** - 停止Frida服务

### 后台任务管理
- 支持后台运行frida-server
- 实时监控任务状态
- 自动错误恢复机制
- 完整的Job生命周期管理

## 版本历史

- **v2.1 Release** (2024-12-19): 修复Job管理器关键问题的正式版本
  - 修复了"op_Subtraction"日期减法错误
  - 修复了Job ID显示不完整问题
  - 统一了数据结构，提升稳定性
  - 优化了Job运行时间计算逻辑
  - 完善了错误处理机制
- **v2.0**: 重构版本，添加Job管理功能
- **v1.0**: 初始版本，基础Frida操作功能

## 贡献

欢迎提交Issue和Pull Request来改进这个项目。

## 许可证

本项目采用MIT许可证。

## 联系方式

如有问题或建议，请通过GitHub Issues联系。
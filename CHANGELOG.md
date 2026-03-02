# Changelog

所有重要变更都记录在此文件中。

格式遵循 [Keep a Changelog](https://keepachangelog.com/zh-CN/1.0.0/)，
版本号遵循 [语义化版本](https://semver.org/lang/zh-CN/)。

---

## [v1.1.0] - 2026-03-02

### ✨ 新增
- 语音播报：每次扫码后自动播报当前总数，支持中文和西班牙语
- 前缀过滤下拉预设：MercadoLibre（465）、J&T Express（GC/JMX）、自定义
- WebDAV Failed to fetch 解决方案提示
- WebDAV 配置安全说明：仅存本设备，不写代码

### 🎨 UI 改版
- 背景改为白色 Material Design 风格
- 总数数字放大至 80px 红色高亮
- 列表改为序号/条码/日期三列表格
- 扫一扫按钮移至底部全宽

### 🔒 安全
- WebDAV 配置通过 localStorage 存于本设备，不写入代码仓库

---

## [未发布]
> 开发中的功能，尚未正式发布

---

## [v1.0.0] - 2026-02-28

### 🎉 初始版本发布

#### ✨ 新增
- 防重复条码扫描核心功能（实时检测 + 红色警告 + 震动反馈）
- PDA 扫描枪输入支持（隐藏 input 持续捕获，兼容 Enter 键与缓冲模式）
- 手动输入框备用方案
- 自定义前缀过滤规则（支持多前缀，标签式管理）
- 条码长度范围校验
- 本地 localStorage 持久化存储（App 重启数据不丢失）
- 离线模式：无网络时正常扫码，记录本地标记「待同步」
- 联网后自动批量同步至 WebDAV
- WebDAV 云备份配置（服务器地址、用户名、密码、上传路径）
- WebDAV 连接测试功能
- 清空数据前自动 WebDAV 备份流程（备份失败可强制清空）
- 离线状态下清空时自动触发本地文件下载
- TXT 格式数据导出（含序号、时间、条码）
- 实时网络状态指示（在线🟢 / 离线🔴）
- 待同步数量角标显示
- 扫描成功/重复/前缀不匹配三种 Toast 提示
- 设置页：前缀规则、长度范围、连续扫码开关、WebDAV 配置、文件名模板
- 深色主题 UI，适配 PDA 仓库环境

#### 📋 技术说明
- 单文件 HTML 应用，无需构建工具，无外部依赖
- 存储方案：localStorage（模拟 SQLite 持久化）
- 网络方案：WebDAV PUT 请求，Basic Auth 认证
- 兼容 Android 8.0+ WebView / Chrome / Firefox

---

<!-- 
## [v1.1.0] - YYYY-MM-DD
新版本发布后在此添加，格式如下：

### ✨ 新增
- 

### 🐛 修复
- 

### 🔄 变更
- 

### ❌ 移除
- 

### ⚡ 性能
- 

### 🔒 安全
- 
-->

---

[未发布]: https://github.com/YOUR_USERNAME/pda-scanner/compare/v1.0.0...HEAD
[v1.0.0]: https://github.com/YOUR_USERNAME/pda-scanner/releases/tag/v1.0.0

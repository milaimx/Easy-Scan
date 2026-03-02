# 📦 PDA 防重复扫描系统

> 专为仓库 PDA 扫描枪设计的防重复条码扫描应用，支持离线本地存储 + WebDAV 云备份。

[![Version](https://img.shields.io/badge/version-v1.0.0-blue)](CHANGELOG.md)
[![License](https://img.shields.io/badge/license-MIT-green)](LICENSE)

---

## ✨ 功能特性

| 功能 | 说明 |
|------|------|
| 🔍 防重复扫描 | 实时检测重复条码，声音+震动+红色提示 |
| 🏷️ 前缀过滤 | 自定义允许的条码前缀规则 |
| 💾 本地持久化 | 数据存储于 localStorage，App 重启不丢失 |
| ☁️ WebDAV 备份 | 清空前自动上传至 WebDAV 服务器 |
| 📶 离线支持 | 无网络时正常扫码，联网后自动同步 |
| 📤 数据导出 | 一键导出 TXT 文件至本地 |

---

## 🚀 快速开始

### 直接使用（无需安装）
```
直接用浏览器打开 src/index.html
```

### 部署到 Web 服务器
```bash
# 将 src/index.html 放置于任意 Web 服务器
# 推荐使用 GitHub Pages 部署（见下方）
```

### 使用 GitHub Pages 托管
1. Fork 此仓库
2. 进入 `Settings` → `Pages`
3. Source 选择 `main` 分支，目录选 `/src`
4. 保存后访问 `https://<你的用户名>.github.io/<仓库名>/`

---

## 📱 PDA 设备兼容性

| 品牌 | 型号 | 测试状态 |
|------|------|---------|
| Zebra | TC系列、MC系列 | ✅ 兼容 |
| Honeywell | CT系列、CK系列 | ✅ 兼容 |
| Urovo | DT系列 | ✅ 兼容 |
| 普通蓝牙扫描枪 | 接 Android/PC 使用 | ✅ 兼容 |

> 扫描枪需配置为 **USB HID / 蓝牙 HID** 模式，末尾发送 `Enter` 键。

---

## ⚙️ 配置说明

### 前缀过滤
在「设置」页添加前缀规则，如 `465`、`SKU-`，留空则接受所有条码。

### WebDAV 配置
```
服务器地址：https://dav.example.com/scans/
用户名：    admin
密码：      ******
上传路径：  /barcode-backups/
```

### 文件命名规则
备份文件自动命名为：`scan_export_backup_YYYYMMDD_HHmmss.txt`

---

## 📁 项目结构

```
pda-scanner/
├── src/
│   └── index.html          # 主应用（单文件，含 HTML/CSS/JS）
├── docs/
│   └── PRD_防重复扫描.md   # 产品需求文档
├── CHANGELOG.md             # 版本变更日志
├── README.md                # 项目说明（本文件）
└── LICENSE                  # 开源许可证
```

---

## 🔄 更新与版本

每次更新请参考 [CHANGELOG.md](CHANGELOG.md) 查看变更详情。

提交代码时请遵循 [Commit 规范](#-commit-规范)。

---

## 📝 Commit 规范

```
<类型>(<范围>): <简短描述>

类型：
  feat      新功能
  fix       Bug 修复
  docs      文档变更
  style     样式调整（不影响功能）
  refactor  代码重构
  perf      性能优化
  chore     构建/工具变更

示例：
  feat(scan): 新增连续扫码模式
  fix(webdav): 修复离线时备份失败崩溃问题
  docs(readme): 更新 PDA 兼容性列表
```

---

## 📄 License

MIT © 2026

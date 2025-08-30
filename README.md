# 做一个 Wails 应用

## 操作系统兼容性

Wails 对主流桌面操作系统有良好支持，但存在版本门槛：

- Windows：支持 Windows 10 及以上版本（64 位），依赖系统内置的 Edge WebView2（基于 Chromium）。Windows 10 20H1 及以上版本通常预装，旧版本需手动安装 WebView2 运行时。

- macOS：支持 macOS 10.15（Catalina）及以上版本，使用系统内置的 WebKit 作为渲染引擎（与 Safari 同源）。

- Linux：支持主流发行版（如 Ubuntu 20.04+、Fedora 34+、Debian 11+ 等），依赖 WebKitGTK 或 Chromium 作为 WebView 引擎（需手动安装对应系统库）。

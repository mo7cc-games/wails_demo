# 做一个 Wails 应用

## 操作系统兼容性

Wails 对主流桌面操作系统有良好支持，但存在版本门槛：

- Windows：支持 Windows 10 及以上版本（64 位），依赖系统内置的 Edge WebView2（基于 Chromium）。Windows 10 20H1 及以上版本通常预装，旧版本需手动安装 WebView2 运行时。

- macOS：支持 macOS 10.15（Catalina）及以上版本，使用系统内置的 WebKit 作为渲染引擎（与 Safari 同源）。

- Linux：支持主流发行版（如 Ubuntu 20.04+、Fedora 34+、Debian 11+ 等），依赖 WebKitGTK 或 Chromium 作为 WebView 引擎（需手动安装对应系统库）。

## About

This is the official Wails Vue template.

You can configure the project by editing `wails.json`. More information about the project settings can be found
here: https://wails.io/docs/reference/project-config

## Live Development

To run in live development mode, run `wails dev` in the project directory. This will run a Vite development
server that will provide very fast hot reload of your frontend changes. If you want to develop in a browser
and have access to your Go methods, there is also a dev server that runs on http://localhost:34115. Connect
to this in your browser, and you can call your Go code from devtools.

## Building

To build a redistributable, production mode package, use `wails build`.

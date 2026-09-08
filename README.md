# electron-wrapper

A minimal Electron wrapper that turns any website into a Windows portable `.exe` — no installer, no local toolchain required.

#### ‎

## 简介 / Introduction

这是一个极简的 Electron 壳模板：把任意网站打包成 Windows 便携版 `.exe`。单文件 `main.js`，只需改一行 URL；配合 GitHub Actions 可在云端一键构建，并支持自定义域名。

A minimal Electron wrapper template that turns any website into a Windows portable `.exe`. It's a single-file `main.js` — just change one line of URL — and ships with a GitHub Actions workflow for one-click cloud builds with an optional custom domain.

#### ‎

## 特性 / Features

- 单文件 Electron 应用（[main.js](main.js)），改一行 `win.loadURL(...)` 即可
- electron-builder 打包 Windows 便携版 `.exe`，免安装、开箱即用
- GitHub Actions 自动构建：每次 push 自动打包；手动触发（Run workflow）可填 `custom_domain` 替换默认域名，产物自动发布到 Release

#### ‎

- Single-file Electron app ([main.js](main.js)) — just change the `win.loadURL(...)` line
- Windows portable `.exe` built with electron-builder, ready to run with no installation
- GitHub Actions: auto-builds on every push; manual runs accept a `custom_domain` to replace the default domain, and artifacts are published to Releases automatically

#### ‎

## 使用 / Usage

### 在线构建（无需本地环境）/ Cloud build (no local setup)

1. Fork 本仓库 → 进入 **Actions → build → Run workflow**，在 `custom_domain` 填入你的域名（留空则使用默认域名）
2. 构建完成后，在 **Releases** 页面下载 `.exe`

#### ‎

1. Fork this repo, go to **Actions → build → Run workflow**, and enter your domain in `custom_domain` (leave empty to keep the default).
2. When the build finishes, download the `.exe` from the **Releases** page.

#### ‎

### 本地构建 / Local build

```bash
# 先把 main.js 中的 win.loadURL('https://...') 改成你的目标网址
# First, edit win.loadURL('https://...') in main.js to your target site

npm install
npm start        # 开发运行 / Run in development
npm run build    # 打包便携版 exe，输出到 dist/ / Build the portable exe into dist/
```

#### ‎

## 🗂️ License

This program is released under the GNU Affero General Public License v3.0 (AGPLv3).

Copyright (C) 2025-2026 lingyicute.

This program is free software: you can redistribute it and/or modify
it under the terms of the GNU Affero General Public License as published by
the Free Software Foundation, either version 3 of the License, or
(at your option) any later version.

This program is distributed in the hope that it will be useful,
but WITHOUT ANY WARRANTY; without even the implied warranty of
MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE. See the
GNU Affero General Public License for more details.

You should have received a copy of the GNU Affero General Public License
along with this program. If not, see https://www.gnu.org/licenses.

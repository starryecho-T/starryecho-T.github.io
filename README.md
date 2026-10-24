# 个人网站 · starryecho

公网地址：**https://starryecho-t.github.io**

纯静态、零依赖：`index.html`（排版）+ `content.js`（内容数据）+ `editor.html`（在线编辑器）。
由 GitHub Pages 自动发布，改完内容约 1 分钟生效。

> 首次部署：2026-10-24（仓库经 GitHub Contents API 创建；本机直连 github.com 推送，见
> `D:\GitHub\GitHub推送与网络问题指南.md`）。

## 怎么编辑（三种方式任选）

1. **网页编辑器（推荐）**：打开 [editor.html](https://starryecho-t.github.io/editor.html)，
   填一次 GitHub 细粒度令牌（Token，仅本仓库 Contents 读写权限，只存本设备 localStorage），
   之后表单修改 → 「保存并发布」→ 自动提交到仓库并重新发布。
   令牌创建：https://github.com/settings/personal-access-tokens/new →
   Repository access 选 *Only select* 本仓库；Permissions → *Contents: Read and write*。
2. **GitHub 网页 / 手机 App**：直接编辑 `content.js`（仓库页面点铅笔；手机用 GitHub App 的文件编辑）。
3. **网页版 VS Code**：在仓库页面按 `.`（github.dev），改完提交。

## 本地预览

直接双击 `index.html` 即可（离线显示默认内容；编辑器保存仍需联网）。

## 集成

ThuSchedule 应用的「主页」Tab 优先加载本站线上地址，无网络时回退到应用内置副本
（副本随应用打包，见 `ThuSchedule/app/src/main/assets/site/`）。

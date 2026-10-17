# 电子木鱼

一只安静的电子木鱼：轻敲木鱼，功德 +1。

## 手机打开

部署到 GitHub Pages 后的地址：

```
https://beber-shout.github.io/muyu/
```

页面可以添加到手机主屏幕，像 App 一样全屏打开，并且支持离线使用。

## 功能

- 点击 / 触摸木鱼，木槌挥下，功德 +1
- 木鱼音效由 Web Audio 实时合成，无需加载音频文件
- 今日功德、累计功德、今日目标 1000
- 数据保存在浏览器本地，按日期自动重置今日功德
- 支持深色模式、手机安全区、PWA 离线缓存
- 无外部依赖，纯静态页面

## 上传到 GitHub（网页版，约 2 分钟）

1. 打开上传页 <https://github.com/beber-shout/muyu/upload/main>
2. 把本项目里的这些文件拖进去（不要上传 `.git`、`preview-*.png` 等本地文件）：
   `index.html`、`manifest.webmanifest`、`sw.js`、`icon.svg`、`icon-180.png`、`icon-192.png`、`icon-512.png`、`README.md`、`.nojekyll`
3. 点击 **Commit changes**
4. 打开 Pages 设置 <https://github.com/beber-shout/muyu/settings/pages>，Source 选择 **Deploy from a branch**，分支选 **main**，目录选 **/ (root)**，点击 **Save**
5. 等 1–2 分钟，打开 <https://beber-shout.github.io/muyu/>

> 最少只需要上传 `index.html` 就能敲木鱼；其他文件用于应用图标、离线缓存和“添加到主屏幕”。

## 本地预览

在项目目录启动任意静态服务器，例如：

```bash
python -m http.server 8000
```

然后打开 <http://localhost:8000/>。

> 直接双击 `index.html` 也能敲木鱼，但 Service Worker 和“添加到主屏幕”需要 http/https 环境。

## 文件

| 文件 | 用途 |
| --- | --- |
| `index.html` | 页面、样式、交互与音效 |
| `manifest.webmanifest` | PWA 应用信息 |
| `sw.js` | 离线缓存 |
| `icon.svg` / `icon-*.png` | 应用图标 |

## 部署

这是一个纯静态站点，把仓库推送到 GitHub 后，在 **Settings → Pages** 中选择
`Deploy from a branch`，分支 `main`，目录 `/ (root)` 即可。

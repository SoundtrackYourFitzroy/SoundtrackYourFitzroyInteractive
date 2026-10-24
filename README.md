# Soundtrack Your Fitzroy — 互动网站源文件

这是当前互动网站的可迁移源文件，已包含最新的 Soundtrack Your Fitzroy 名称。

## 文件说明

- `index.html`：页面结构、文字、配色和布局（CSS 已放在这个文件内）。
- `app.js`：问答选项、路线匹配、歌单展示与地图链接等互动功能。
- `route-data.js`：地点、营业时间、歌曲和路线使用的数据。
- `.nojekyll`：告诉 GitHub Pages 直接发布静态文件；部分电脑会隐藏这个文件。

这三个网站文件与当前部署源文件完全一致。本说明和 `.nojekyll` 是迁移时新增的辅助文件。
无需安装 Node.js、无需构建步骤、无需数据库或 API 密钥。路线和歌曲匹配在浏览器内运行，不调用 ChatGPT API。
地图、Spotify 和商家网站是外部链接，打开它们需要网络；Spotify 播放是否需要账户取决于 Spotify。
代码包含可选的浏览器工具注册功能，普通浏览器不支持时会跳过，不影响访客填写问答。

## 在电脑上查看

1. 解压整个压缩包。
2. 让 `index.html`、`app.js`、`route-data.js` 始终放在同一文件夹。
3. 用浏览器打开 `index.html`，即可查看并使用问答。

也可在该文件夹内运行 `python3 -m http.server 8000`，然后访问 `http://localhost:8000/`。

## 使用 GitHub Pages 发布（网页操作）

1. 登录自己的 GitHub 账户，点击 New repository。
2. 仓库名称可填 `soundtrack-your-fitzroy`。使用 GitHub Free 时，选择 Public，并添加 README 以初始化仓库。
3. 创建后选择 Add file → Upload files。
4. 上传解压后的文件本身，不是 ZIP 文件，也不是最外层文件夹。确保仓库首页直接能看到 `index.html`、`app.js` 和 `route-data.js`。README.md 可用本文件替换。
5. 提交文件（Commit changes）。
6. 打开仓库 Settings → Pages。
7. 在 Build and deployment 下，将 Source 设为 Deploy from a branch。
8. Branch 选择 `main`，文件夹选择 `/(root)`，点击 Save。
9. 等待 GitHub 完成发布，在 Settings → Pages 中点击 Visit site 获取准确网址。首次发布或后续更新可能需要约 10 分钟。

项目网站的网址格式通常为 `https://你的GitHub用户名.github.io/soundtrack-your-fitzroy/`。这是格式示例，请使用 GitHub 实际生成的链接。
如果浏览器上传时未显示 `.nojekyll`，本项目没有需要特殊处理的资源目录，仍可直接发布；也可在 GitHub 新建一个名为 `.nojekyll` 的空文件。

## 迁移后需要更新什么

- 迁移不会自动更改原有 ChatGPT Site，也不会把旧网址自动重定向到新网址。
- 得到新网址后，将活动主页、社交媒体简介等位置的互动网站链接改成新网址。
- 指向旧网址的二维码仍然指向旧网址；要直接打开新网址，需要重新生成二维码。
- 免费 GitHub Pages 地址带 `github.io`，不会带 `chatgpt.site`。
- 如果想使用自己的域名，可另行购买域名并在托管平台设置，不是迁移的必需步骤。
- 这里导出的是问答互动网站，不包含另做的照片滚动 campaign 主页。
- 商家营业时间不会自动更新；源文件中的资料日期为 2026 年 10 月 7 日，后续请自行维护。

## 官方操作参考

- 创建 GitHub Pages 网站：https://docs.github.com/en/pages/getting-started-with-github-pages/creating-a-github-pages-site
- 设置发布来源：https://docs.github.com/en/pages/getting-started-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site

导出日期：2026 年 10 月 24 日。

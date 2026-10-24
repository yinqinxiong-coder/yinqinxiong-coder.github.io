# Yinqin Xiong · 个人博客

这是一个基于 Jekyll 和 GitHub Pages 的静态个人博客。文章使用 Markdown 编写，不需要在本机安装 Node.js、npm 或前端框架。

博客地址：<https://yinqinxiong-coder.github.io>

## 编辑内容

- _config.yml：博客名称、简介、网址和 GitHub 链接。
- index.html：首页介绍与文章主题。
- about.md：关于页面。
- _posts/YYYY-MM-DD-title.md：文章，使用 layout: post 的 Front Matter。
- _layouts/：页面和文章布局。
- assets/style.css：颜色与排版。

## 发布

GitHub Actions 在推送 dev-me 分支时构建 Jekyll 并部署到 GitHub Pages。构建发生在 GitHub 托管的 runner 上，本地只需 Git 和文本编辑器。

开工前先运行 git fetch origin。确认改动后检查 git diff，再提交到 dev-me。首次推送使用 git push -u origin dev-me；之后每次推送前再次 git fetch origin，将本地分支与远端 dev-me 同步并解决冲突。

GitHub 仓库的 Pages Source 已设为 GitHub Actions。
# 孙晨东的个人博客 🚀

[![Hugo](https://img.shields.io/badge/Hugo-0.146.0-blue.svg)](https://gohugo.io)
[![Theme](https://img.shields.io/badge/Theme-PaperMod-orange.svg)](https://github.com/adityatelange/hugo-PaperMod)
[![Deploy](https://github.com/sunchendd/my-blog/actions/workflows/hugo.yml/badge.svg)](https://github.com/sunchendd/my-blog/actions/workflows/hugo.yml)
[![License](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)

> 一个基于 Hugo + PaperMod 主题的现代化个人技术博客

## ✨ 在线访问

🌐 **博客地址**: [https://sunchendd.github.io/my-blog/](https://sunchendd.github.io/my-blog/)

## 📚 项目简介

这是一个使用 [Hugo](https://gohugo.io/) 静态网站生成器搭建的个人技术博客，采用了优秀的 [PaperMod](https://github.com/adityatelange/hugo-PaperMod) 主题，并进行了深度定制和优化。

### 主要特性

- ✨ **现代化设计**：简洁优雅的 UI，舒适的阅读体验
- 🌓 **深色模式**：支持浅色/深色主题自动切换
- 🔍 **全文搜索**：基于 Fuse.js 的快速全文搜索功能
- 📱 **响应式设计**：完美适配各种设备（手机、平板、桌面）
- 🏷️ **标签分类**：灵活的标签和分类系统
- 📑 **归档页面**：按时间归档的文章列表
- 💬 **评论系统**：可选集成 Giscus 评论系统
- 🎨 **自定义样式**：蓝紫渐变配色，卡片阴影和悬停效果
- ⚡ **快速加载**：Hugo 静态生成，加载速度极快
- 🔄 **自动部署**：通过 GitHub Actions 自动构建和部署

## 🛠️ 技术栈

- **静态网站生成器**: [Hugo Extended v0.146.0](https://gohugo.io/)
- **主题**: [PaperMod](https://github.com/adityatelange/hugo-PaperMod)
- **部署**: GitHub Pages
- **CI/CD**: GitHub Actions
- **搜索引擎**: Fuse.js
- **样式**: Custom CSS (渐变色、动画效果)

## 🚀 本地开发

### 前置要求

- Git
- Hugo Extended v0.146.0 或更高版本

### 安装 Hugo

**macOS**:
```bash
brew install hugo
```

**Linux**:
```bash
wget https://github.com/gohugoio/hugo/releases/download/v0.146.0/hugo_extended_0.146.0_linux-amd64.deb
sudo dpkg -i hugo_extended_0.146.0_linux-amd64.deb
```

**Windows**:
```bash
choco install hugo-extended
```

或者访问 [Hugo 官方网站](https://gohugo.io/installation/) 下载对应平台的安装包。

### 克隆项目

```bash
git clone https://github.com/sunchendd/my-blog.git
cd my-blog
git submodule update --init --recursive
```

### 本地运行

```bash
hugo server -D
```

然后在浏览器中访问 [http://localhost:1313/](http://localhost:1313/)

### 构建网站

```bash
hugo --minify
```

生成的静态文件将保存在 `public/` 目录中。

## ✍️ 添加新文章

### 使用 Hugo 命令创建

```bash
hugo new posts/my-new-post.md
```

### 手动创建

在 `content/posts/` 目录下创建新的 Markdown 文件，添加 Front Matter：

```markdown
---
title: "文章标题"
date: 2024-06-15T10:00:00+08:00
draft: false
author: "孙晨东"
tags: ["标签1", "标签2"]
categories: ["分类"]
description: "文章描述"
---

文章内容...
```

### Front Matter 说明

- `title`: 文章标题
- `date`: 发布日期（格式：YYYY-MM-DDTHH:MM:SS+08:00）
- `draft`: 是否为草稿（true/false）
- `author`: 作者名称
- `tags`: 标签列表
- `categories`: 分类列表
- `description`: 文章描述（用于 SEO）
- `cover`: 封面图片（可选）

## 📝 目录结构

```
my-blog/
├── .github/
│   └── workflows/
│       └── hugo.yml          # GitHub Actions 工作流
├── content/
│   ├── posts/                # 博客文章
│   │   ├── welcome.md
│   │   ├── growth-story.md
│   │   └── ...
│   ├── about.md              # 关于页面
│   ├── archives.md           # 归档页面
│   └── search.md             # 搜索页面
├── static/
│   ├── css/
│   │   └── extra.css         # 自定义样式
│   └── images/               # 图片资源
├── themes/
│   └── PaperMod/             # PaperMod 主题（子模块）
├── config.toml               # Hugo 配置文件
├── .gitignore
├── .gitmodules
├── LICENSE
└── README.md
```

## 🎨 自定义配置

### 修改站点信息

编辑 `config.toml` 文件：

```toml
baseURL = "https://sunchendd.github.io/my-blog/"
title = "你的博客名称"

[params]
  author = "你的名字"
  description = "博客描述"
```

### 修改主题配色

编辑 `static/css/extra.css` 文件，修改 CSS 变量：

```css
:root {
  --primary-color: #667eea;      /* 主色调 */
  --secondary-color: #764ba2;    /* 次要色 */
  --accent-color: #f093fb;       /* 强调色 */
}
```

### 添加社交链接

在 `config.toml` 中添加：

```toml
[[params.socialIcons]]
  name = "github"
  url = "https://github.com/your-username"
[[params.socialIcons]]
  name = "email"
  url = "mailto:your-email@example.com"
```

## 🔄 部署说明

### GitHub Pages 自动部署

本博客配置了 GitHub Actions 自动部署：

1. **推送代码到 main 分支**时自动触发构建
2. Hugo 自动构建静态网站
3. 自动部署到 GitHub Pages

### 首次部署设置

1. 进入仓库的 **Settings** → **Pages**
2. **Source** 选择 "GitHub Actions"
3. 推送代码后，等待 Actions 完成即可

### 手动触发部署

在 GitHub Actions 页面，选择 "Deploy Hugo site to Pages" 工作流，点击 "Run workflow"。

## 📊 SEO 优化

博客已配置以下 SEO 优化：

- ✅ 语义化 HTML 结构
- ✅ Meta 标签优化
- ✅ Open Graph 支持
- ✅ Twitter Card 支持
- ✅ Sitemap 自动生成
- ✅ RSS Feed
- ✅ 结构化数据（JSON-LD）

## 🔧 故障排查

### 主题未正确加载

```bash
# 更新子模块
git submodule update --init --recursive
```

### 构建失败

```bash
# 检查 Hugo 版本
hugo version

# 清理缓存
hugo mod clean
rm -rf public/ resources/
```

### 样式未生效

确保 `config.toml` 中配置了：

```toml
[params]
  assets.customCSS = ["css/extra.css"]
```

## 📄 License

本项目采用 MIT 许可证。详见 [LICENSE](LICENSE) 文件。

## 👤 作者

**孙晨东**

- 🐙 GitHub: [@chendongsun](https://github.com/chendongsun)
- 📧 Email: sunchend@outlook.com
- 🌐 Blog: [https://sunchendd.github.io/my-blog/](https://sunchendd.github.io/my-blog/)

## 🙏 致谢

- [Hugo](https://gohugo.io/) - 强大的静态网站生成器
- [PaperMod](https://github.com/adityatelange/hugo-PaperMod) - 优秀的 Hugo 主题
- [GitHub Pages](https://pages.github.com/) - 免费的托管服务

## 📮 联系与反馈

如有问题或建议，欢迎：

- 提交 [Issue](https://github.com/sunchendd/my-blog/issues)
- 发送邮件至 sunchend@outlook.com
- 在博客文章下留言评论

---

⭐ 如果这个项目对你有帮助，欢迎 Star！

**Made with ❤️ by 孙晨东**

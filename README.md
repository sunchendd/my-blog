# 孙晨东的博客 🚀

[![Deploy Hugo site to Pages](https://github.com/sunchendd/my-blog/actions/workflows/hugo.yml/badge.svg)](https://github.com/sunchendd/my-blog/actions/workflows/hugo.yml)
[![Hugo Version](https://img.shields.io/badge/Hugo-0.128+-blue.svg)](https://gohugo.io)
[![License](https://img.shields.io/badge/license-MIT-green.svg)](LICENSE)

基于 Hugo 和 PaperMod 主题构建的现代化个人技术博客。

## 🌐 在线访问

**博客地址**: [https://sunchendd.github.io/my-blog/](https://sunchendd.github.io/my-blog/)

## 📝 关于

这是孙晨东的个人技术博客，分享技术干货、项目经验和有趣内容。

- **作者**: 孙晨东
- **毕业院校**: 杭州电子科技大学
- **工作单位**: 超聚变数字技术有限公司
- **职位**: 高级工程师

## ✨ 特性

- 🎨 **现代化 UI 设计** - 使用渐变色和阴影效果，提供优雅的视觉体验
- 🌓 **深色/浅色模式** - 自动适应系统主题或手动切换
- 🔍 **全站搜索** - 快速搜索文章内容
- 📱 **响应式设计** - 完美适配桌面端和移动端
- 📊 **文章归档** - 按时间归档所有文章
- 🏷️ **标签系统** - 通过标签快速查找相关文章
- 📖 **目录导航** - 文章内自动生成目录
- 💬 **评论系统** - 支持 Giscus 评论（需配置）
- ⚡ **快速加载** - 静态站点，访问速度极快
- 🚀 **自动部署** - 通过 GitHub Actions 自动构建和部署

## 🛠️ 技术栈

- **静态站点生成器**: [Hugo](https://gohugo.io/) 0.128+ Extended
- **主题**: [PaperMod](https://github.com/adityatelange/hugo-PaperMod)
- **部署平台**: GitHub Pages
- **CI/CD**: GitHub Actions
- **样式**: 自定义 CSS + PaperMod 主题

## 🚀 本地运行

### 前置要求

- Hugo Extended 0.128 或更高版本
- Git

### 安装 Hugo

#### macOS

```bash
brew install hugo
```

#### Windows

```bash
choco install hugo-extended
```

#### Linux

```bash
# 下载最新版本
wget https://github.com/gohugoio/hugo/releases/download/v0.128.0/hugo_extended_0.128.0_linux-amd64.deb
sudo dpkg -i hugo_extended_0.128.0_linux-amd64.deb
```

### 克隆并运行

```bash
# 克隆仓库（包含子模块）
git clone --recursive https://github.com/sunchendd/my-blog.git
cd my-blog

# 如果已克隆，更新子模块
git submodule update --init --recursive

# 本地运行（开发模式）
hugo server -D

# 本地运行（生产模式）
hugo server
```

访问 http://localhost:1313 查看博客。

## 📝 添加新文章

### 使用命令创建

```bash
# 创建新文章
hugo new posts/my-new-post.md
```

### 手动创建

在 `content/posts/` 目录下创建 Markdown 文件，添加以下 Front Matter：

```markdown
---
title: "文章标题"
date: 2024-06-20
description: "文章描述"
tags: ["标签1", "标签2"]
categories: ["分类"]
author: "孙晨东"
ShowToc: true
TocOpen: true
draft: false
---

文章内容...
```

### Front Matter 字段说明

- `title`: 文章标题
- `date`: 发布日期
- `description`: 文章描述（用于 SEO 和摘要）
- `tags`: 文章标签（数组）
- `categories`: 文章分类（数组）
- `author`: 作者名称
- `ShowToc`: 是否显示目录
- `TocOpen`: 目录是否默认展开
- `draft`: 是否为草稿（true 则不会在生产环境显示）
- `cover`: 封面图片配置

## 🔧 配置说明

主要配置文件：`config.toml`

### 重要配置项

- `baseURL`: 网站基础 URL
- `title`: 网站标题
- `theme`: 使用的主题
- `params.author`: 作者信息
- `params.socialIcons`: 社交媒体图标
- `menu`: 导航菜单配置

详细配置请参考 [config.toml](config.toml) 文件。

## 📦 目录结构

```
my-blog/
├── .github/
│   └── workflows/
│       └── hugo.yml          # GitHub Actions 工作流
├── archetypes/               # 文章模板
├── assets/                   # 资源文件
├── content/                  # 内容目录
│   ├── about.md             # 关于页面
│   ├── archives.md          # 归档页面
│   ├── search.md            # 搜索页面
│   └── posts/               # 博客文章
│       ├── _index.md
│       └── *.md
├── static/                   # 静态文件
│   ├── css/
│   │   └── extra.css        # 自定义样式
│   └── images/              # 图片资源
├── themes/                   # 主题目录
│   └── PaperMod/
├── config.toml              # 网站配置
└── README.md
```

## 🎨 自定义样式

自定义样式位于 `static/css/extra.css`，包含：

- 渐变色配色方案
- 卡片样式和阴影效果
- 代码块样式优化
- 平滑动画和过渡效果
- 移动端响应式优化
- 深色模式优化

## 📄 许可证

本项目采用 MIT 许可证 - 详见 [LICENSE](LICENSE) 文件。

## 🤝 贡献

欢迎提出问题和建议！你可以：

1. 提交 [Issue](https://github.com/sunchendd/my-blog/issues)
2. 提交 Pull Request
3. 通过邮件联系: sunchend@outlook.com

## 📧 联系方式

- **邮箱**: sunchend@outlook.com
- **GitHub**: [@chendongsun](https://github.com/chendongsun)
- **LinkedIn**: [孙晨东](https://linkedin.com/in/sunchendong)

## 🙏 致谢

- [Hugo](https://gohugo.io/) - 强大的静态网站生成器
- [PaperMod](https://github.com/adityatelange/hugo-PaperMod) - 简洁优雅的 Hugo 主题
- [GitHub Pages](https://pages.github.com/) - 免费的静态网站托管服务

---

⭐ 如果这个项目对你有帮助，欢迎给个 Star！


# ALGrowup Blog

这是我的个人博客仓库，基于 [Jekyll](https://jekyllrb.com/) 和 [Chirpy](https://github.com/cotes2020/jekyll-theme-chirpy) 主题搭建，托管在 GitHub Pages。

仓库主要用于：

- 发布博客文章
- 记录成长、技术和日常思考
- 通过 GitHub Actions 自动构建和部署

## 项目结构

```text
.
├── _config.yml          # 站点配置
├── _posts/              # 博客文章
├── _tabs/               # 顶部页面，例如 about / categories / tags
├── assets/              # 静态资源
├── _plugins/            # Jekyll 插件
├── index.html           # 首页入口
├── Gemfile              # Ruby 依赖
└── .github/             # GitHub Actions 工作流
```

## 写文章

文章放在 `_posts/` 目录下，文件名格式如下：

```text
YYYY-MM-DD-title.md
```

例如：

```text
_posts/2026-06-13-hello.md
_posts/2026/06/2026-06-13-hello.md
```

文章头部示例：

```yaml
---
title: 第一篇文章
date: 2026-06-13 10:00:00 +0800
categories: [记录]
tags: [日常, 博客]
---
```

正文直接使用 Markdown 编写。

## 图片管理

如果文章需要插图，建议统一放在 `assets/` 目录下，再在文章中引用。

例如：

```markdown
![示例图片](/assets/img/example.png)
![示例图片](assets/img/2026/06/2026-06-13-hello/example.png)
```

如果后续你已经形成了自己的图片目录规范，也可以继续沿用，但建议保持路径统一，方便后期维护。

```
文章
![示例图片](/assets/img/example.png)


```



## 本地预览

可以不安装本地相关环境，完全依赖GitHub Actions工作流即可。如果想使用本地预览可以使用下面的步骤。

安装依赖：

```bash
bundle install
```

启动本地服务：

```bash
bundle exec jekyll s
```

默认访问地址：

```text
http://127.0.0.1:4000
```

## 部署方式

当前仓库适合直接推送到 GitHub，由 GitHub Pages / GitHub Actions 自动部署。

常用流程：

```bash
git add .
git commit -m "update posts"
git push origin main
```

推送后，可在 GitHub 仓库的 `Actions` 页面查看构建状态。

## 后续可维护内容

后续如果要继续调整博客，通常会改这些位置：

- `_config.yml`：站点名称、描述、社交链接、主题配置
- `_tabs/`：关于页、分类页、标签页
- `_posts/`：文章内容
- `assets/`：图片、图标和自定义静态资源

## 说明

这个仓库已经不是默认的 Chirpy Starter 模板仓库，而是实际使用中的个人博客仓库。后续文档和内容都以“可直接维护博客”为目标，不再保留模板说明。

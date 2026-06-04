<center> <h1>WovenJunct's Mind Palace </h1></center>

你好，我是WovenJunct,这是我的个人博客  

欢迎来到我的Mind Palace!

博客链接为：[https://wovenjunct.github.io/](https://wovenjunct.github.io/)

本博客基于[Hugo](https://gohugo.io/)的框架,使用[hugo-theme-reimu](https://github.com/D-Sketon/hugo-theme-reimu)主题搭建。

> **文章发布说明**

# 一、创建文章
推荐使用hugo命令
```
hugo new content content/post/xxx.md
```
或者直接在post目录下创建文件

# 二、front-matter配置（文章头部）
```
---
title: 文章标题                    # 必填
date: 2026-06-04T10:00:00+08:00   # 创建时间
lastmod: 2026-06-04T10:00:00+08:00 # 最后修改时间
draft: false                       # true=草稿不显示，false=发布
weight: 1                          # 权重，数字越大越靠前（置顶用）

## 分类和标签
categories: [技术, 编程]           # 分类（数组）
tags: [Hugo, 博客, 建站]           # 标签（数组）

## 封面和头图
cover: /images/cover.jpg           # 卡片封面（列表页显示）
banner: /images/banner.jpg         # 文章头图（文章页顶部）

## 描述
description: "文章的简短描述"       # SEO 描述
summary: "文章摘要"                # 摘要显示

## 功能开关
toc: true                          # 是否显示目录
comments: true                     # 是否显示评论
copyright: true                    # 是否显示版权
sponsor: true                      # 是否显示赞助
math: true                         # 是否开启 LaTeX 数学公式
mermaid: true                      # 是否开启 Mermaid 图表

## 其他
sidebar: left                      # 侧边栏位置：left/right/false
author: "WovenJunct"              # 作者
keywords: [关键词1, 关键词2]        # 关键词
outdated: false                    # 是否标记为过期
link: "https://example.com"        # 外部链接（点击直接跳转）
---
```
## 正文内容

这里是文章的正文...

# 三、分类和标签
分类（categories）
在文章 front-matter 中添加：
```
   categories: [技术, 编程]
```

- 自动生成 /categories/ 页面
- 访问 /categories/技术/ 查看该分类下的文章
#### 标签（tags）
在文章 front-matter 中添加：
```
  tags: [Hugo, 博客, 建站]
```
- 自动生成 /tags/ 页面
- 访问 /tags/Hugo/ 查看该标签下的文章

# 四、封面和头图
## 封面（cover）
- 列表页卡片显示的图片
- 如果不设置，会从 data/covers.yml 随机选择
- 如果随机封面也不可用，会使用全局 banner

## 头图（banner）
文章页顶部的大图
 - 优先级最高
 - 推荐写法
```
---
title: Hello World
banner: /images/post-banner.jpg 或 url   # 文章页头图
cover: /images/post-cover.jpg 或 url   # 列表页卡片封面
---
```
# 五、内置Shortcodes（短代码）
1. 标签页（Tabs）
```
{{< tabs >}}
<!-- 标签1 -->
内容1
<!-- 标签2 -->
内容2
{{< /tabs >}}
```
2. 照片墙（Gallery）
```
{{< gallery >}}
![图1](url1)
![图2](url2)
{{< /gallery >}}
```
3. 提示框（Alert）
```
> [!note]
> 这是 note 提示

> [!tip]
> 这是 tip 提示

> [!warning]
> 这是 warning 提示
类型：note、tip、important、warning、danger
```
4. 折叠面板（Details）
```
{{< details summary="点击展开" >}}
折叠的内容
{{< /details >}}
```
5. 链接卡片（Link）
```
{{< link title="网站名" link="https://example.com" >}}
```
6. 友链卡片（Friends）
```
{{< friendsLink >}}
读取 data/friends.yml
```
7. 热力图（HeatMap）
```
{{< heatMapCard >}}
```
8. 标签轮盘（TagRoulette）
```
{{< tagRoulette tags="游戏,动漫,音乐" icon="🎮" >}}

```
# 六、文章示例

> ---
> title: 我的第一篇博客
> date: 2026-06-04T10:00:00+08:00
> draft: false
> categories: [随笔]
> tags: [博客, 第一篇]
> cover: /images/first-post-cover.jpg
> banner: /images/first-post-banner.jpg
> description: "这是我的第一篇博客文章"
> toc: true
> comments: true
> ---
> ## 开头
>这是文章的开头...
>## 正文
>这里是正文内容...
> [!tip]
> 这是一个提示框    
> ## 结尾
> 感谢阅读！

# 七、发布流程
1. 创建文章文件
2. 编写 front-matter 和正文
3. 本地预览：hugo server
4. 确认无误后，提交推送：

```
git add .
git commit -m "feat: 添加第一篇文章"
git push
```
5. GitHub Actions 自动部署

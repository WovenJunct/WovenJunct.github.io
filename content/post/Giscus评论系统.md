---
title: "Giscus评论系统"
date: 2026-06-05T09:48:06+08:00
lastmod: 2026-06-05T09:48:06+08:00
description: "基于github discussions的开源评论系统，适用于博客"
draft: false
categories: [学习,技术]          
tags: [giscus,建站] 
---
# Giscus评论系统
Giscus 是一个基于 GitHub Discussions的开源评论系统，它可以在 GitHub 上创建一个评论区，并允许用户在网页上进行评论,
适合博客、文档网站等场景，他人需登录GitHub账号才能评论。

Giscus 的主要特点如下：
- 开源，无跟踪，无广告，永久免费
- 无需数据库
- 支持自定义主题，支持多语言
- 高可配置型，可自建服务

更多详情请见官网 [giscus](https://giscus.app/)

## 配置方法
1. 选择一个公开的github仓库，用于存储评论数据。
   
2. 安装**Giscus Github App** ： 在 <https://github.com/apps/giscus> 安装自己到自己的仓库  
   选择 Only select repositories ，然后选择自己的仓库，Install it !    
   安装完成后，会回到自己的github settings 页面  

3. 开启仓库的 **Discussions** 功能，前往仓库的 Settings 页面，General 中底部 Features 中勾选 Discussions
   
4. 前往<https://giscus.app> 配置页面，在 [仓库] 中输入自己的仓库地址 ，即：https://github.com/<username>/<repo> 中的 **<username>/<repo>**  
   选择 **页面 ↔️ discussion 映射关系** ，推荐 pathname  
   选择 **Discussion 分类**，推荐使用 公告（announcements）  
   可根据需要选择 特性 ，如**将评论框放在评论上方**（评论输入框会放在评论上方，这样用户可以在不滚动到讨论底部的情况下发表评论），
   以及**懒加载评论**（评论的加载将延迟到用户滚到评论容器附近）  
   此外也可选择 **主题** ，即评论区的主题，选择主题时可在giscus当前页面查看效果  
   其他高级配置见 [giscus 官方文档](https://giscus.app)
   最后会得到如下代码：
```javascript
<script src="https://giscus.app/client.js"
        data-repo="你的仓库地址"
        data-repo-id="你的repo id"
        data-category="Announcements"
        data-category-id="你的分类 id"
        data-mapping="pathname"
        data-strict="0"
        data-reactions-enabled="1"
        data-emit-metadata="1"
        data-input-position="top"
        data-theme="你的主题"
        data-lang="zh-CN"
        data-loading="lazy"  # 懒加载
        crossorigin="anonymous"
        async>
</script>
```
5. 配置外层 params.yml  
   上述配置并非直接使用，而是通过params.yml文件进行配置，该文件中有以下内容：
```yml
giscus:
  enable: false
  repo:
  repoId:
  category:
  categoryId:
  mapping: mapping
  strict: 0
  reactionsEnabled: 1
  emitMetadata: 0
  inputPosition: bottom
  theme:
    light:
    dark:
```

6. 将eiscus.app生成的配置，映射到对应配置即可，然后找到 comment 配置部分，更改选择的评论系统为giscus.
```yml
comment:
  title:
    zh-CN: 说些什么吧！
  default: giscus
```
7. 配置完成！重启服务即可看到评论区啦！
   
8. 如何管理评论
   每篇文章的评论会对应一个 Discussion 帖子，可在仓库的 Discussions 页面查看  
   可进行回复、删除、标记、置顶锁定评论等操作  
   每次有新评论时，自己也会收到 Github 通知

> [!NOTE]
> 本文配置方法是基于我自己的博客配置，其他网站的配置可能会有差异，可根据情况调整。  
> 其他可用的评论系统有：  
> [Waline](https://waline.js.org/) , [Twikoo](https://twikoo.js.org/) , [Utterances](https://utteranc.es/) , [Gitalk](https://gitalk.github.io/) , [Beaudar](https://beaudar.lipk.org/) 等，如有需要可自行探索。
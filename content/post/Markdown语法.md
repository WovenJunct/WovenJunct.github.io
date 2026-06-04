---
title: "Markdown语法"
date: 2026-06-04T23:32:43+08:00
lastmod: 2026-06-04T23:32:43+08:00
description: "为了写博客，学习学习更多的markdown语法"
draft: false
categories: [学习]          
tags: [markdown] 
---
# Markdown语法展示

> 其实我还不怎么熟悉Markdown的语法，为了方便以后写博客，决定好好看看markdown的语法  
> 这篇文章主要是为了展示markdown的语法，用于参考。

## **如何查看markdown预览？**  
我一般用的编辑器是**vscode**，可以使用**Ctrl+Shift+V**查看预览,这个是vscode原生的，个人感觉观感不太好，

所以我使用插件**Markdown Preview Enhanced**来查看预览，可以很方便的查看预览和进行编写，强推。

当然也有其他方式，比如动动小手，在浏览器中直接搜索markdown在线编辑器什么的，便可进行查看了  

这里推荐几个网站：

- [Metool工具 ](https://metool.online/zh/markdown/edit/)   

- [Markdown中国官网](https://markdown.com.cn/)       

- [markdown菜鸟教程](https://www.runoob.com/markdown/md-tutorial.html)      

- [Dillinger ](https://dillinger.io/)       

- [Markdown编辑器](https://www.markdownassistant.com/zh/)    
 
- [Markdown online](https://www.markdownonline.net/zh/)

作用就不细说了，直接上手即可。

## 基本语法
创始人**John Gruber**原始设计文档中列出的元素，所有markdown应用程序均能使用
### 标题
1.使用 # 号（我比较喜欢）
```
# 一级标题
## 二级标题
### 三级标题
#### 四级标题
##### 五级标题
###### 六级标题
```

效果

# 一级标题
## 二级标题
### 三级标题
#### 四级标题
##### 五级标题
###### 六级标题

2.使用 = 和 - 标记一二级标题(这个好像AI写的代码中见的多🤔)
```
这个是一级标题
=================

这个是二级标题
-----------------
```
效果

我展示的是一级标题
=================

我展示的是二级标题
-----------------
### 换行
每行结尾使用两个空格或多个空格进行换行，然后在下一行继续写，如果还是在这行写的话不会换行

或者直接空一行，这种方法不太推荐，如果为了方便阅读倒还行。

### 粗体
```
**这是粗体**     #我更喜欢这个
__加两个下划线也是粗体__
```
**这是粗体**     
__加两个下划线也是粗体__

### 斜体
```
*这是斜体*
_加一个下划线也是斜体_
```
*这是斜体*
_加一个下划线也是斜体_

那又粗又斜呢？聪明的你肯定注意到了，用三个*或者_不就行了？
***这是又粗又斜的字***
> [!TIP]
> 可以使用快捷键
> **Ctrl+B** 粗体 **Ctrl+I** 斜体
> 就像在word中使用粗体和斜体一样！
### 引用
```
> 这是一个引用
>> 这是一个二级引用
>>> 这是一个三级引用
```
> 这是一个引用
>> 这是一个二级引用
>>> 这是一个三级引用
### 有序列表
```
1. 这是有序列表
2. 数字加一个点开头
8. 然后加一个空格
    1. 通常从1开始
    0. 标号可以任意数字
3. 就像这样
```
1. 这是有序列表
2. 数字加一个点开头
8. 然后加一个空格
    1. 通常从1开始
    0. 标号可以任意数字
3. 就像这样

### 无序列表
```
- 使用 - 或 * 或 + 开头
- 然后一个空格
    - 就能实现一个无序列表
    - 最好不要混用这三种符号
- 嗯，应该就是这样！
```
- 使用 - 或 * 或 + 开头
- 然后一个空格
    - 就能实现一个无序列表
    - 最好不要混用这三种符号
- 嗯，应该就是这样！
### 代码
```
`使用一个反引号包裹代码`
``如果有多个`代码`,或者需要`转义`的,使用两个反引号``
```
`使用一个反引号包裹代码`就能实现
``如果有多个`代码`,或者需要`转义`的,使用两个反引号``包裹起来

### 分割线
单行使用三个或以上个 * 或 - 或 _ 即可实现分割线，不能有其他内容
***  
---
___
### 链接
```
链接文本放在中括号中，地址放在后面的括号中，括号中可以加上title
[米游社](https://www.miyoushe.com "这是米游社链接")
title为悬停显示内容
用加括号<>也很方便，直接把地址变成链接
<https://www.bilibili.com/>
链接也可以用粗体
就像这样 **[知乎](https://www.zhihu.com/)**
也能变成代码 [`某音`](https://www.douyin.com)
```
[米游社](https://www.miyoushe.com "这是米游社链接")
<https://www.bilibili.com/>
就像这样 **[知乎](https://www.zhihu.com/)**
也能变成代码 [`某音`](https://www.douyin.com)
### 图片
```
使用感叹号 ！ 在链接前即可链接图片
！[图片](/images/原石.png)

如果再嵌套一层就能实现点击图片跳转链接
[！[图片](/images/logo.png)](https://www.baidu.com)
```

![图片](/images/原石.png)

[![图片](/images/logo.png)](https://www.baidu.com)
## 扩展语法
扩展额外功能，不是所有Markdown 应用程序都能使用，如**windows记事本**、**macOS备忘录**、**TextEdit纯文本**、**linux的nano**、**vim**、**gedit**，**vscode原生**，**主流社区/平台在线编辑器**等。
### 表格
```
| Syntax      | Description |
| ----------- | ----------- |
| Header      | Title       |
| Paragraph   | Text        |

单元格宽度可变

| Syntax | Description |
| --- | ----------- |
| Header | Title |
| Paragraph | Text |

对齐：使用冒号
| Syntax      | Description | Test Text     |
| :---        |    :----:   |          ---: |
| Header      | Title       | Here's this   |
| Paragraph   | Text        | And more      |

可设置表格中文字格式，不做赘述
```

| Syntax      | Description |
| ----------- | ----------- |
| Header      | Title       |
| Paragraph   | Text        |

单元格宽度可变

| Syntax | Description |
| --- | ----------- |
| Header | Title |
| Paragraph | Text |

对齐：使用冒号
| Syntax      | Description | Test Text     |
| :---        |    :----:   |          ---: |
| Header      | Title       | Here's this   |
| Paragraph   | Text        | And more      |

> [!TIP]
> 表格的语法比较麻烦，可以使用[Markdown Tables Generator](https://www.tablesgenerator.com/markdown_tables)来生成表格。
### 代码块
使用三个反引号包裹代码
```
这是一个代码块
```
代码高亮，在第一个反引号后添加语言类型
```python
  print("Hello, World!")
  for i in range(10):
    print(i)
```
### 脚注
```
人工智能正在快速落地各行各业[^ai-note]。
Python是热门编程语言[^python]。

[^ai-note]: AI全称人工智能（Artificial Intelligence），是研发模拟人类智能的技术科学。
[^python]: Python1991年发布，语法简洁，广泛用于爬虫、数据分析、AI开发。
```
人工智能正在快速落地各行各业[^ai-note]。
Python是热门编程语言[^python]。

[^ai-note]: AI全称人工智能（Artificial Intelligence），是研发模拟人类智能的技术科学。
[^python]: Python1991年发布，语法简洁，广泛用于爬虫、数据分析、AI开发。

### 定义列表
```
Markdown
: 轻量级标记语言，用于快速排版文档
: 由John Gruber创建

脚注
: 对正文内容补充说明的注释，放在文档末尾

定义列表
: 专门用来「词条+解释」的语法
```
Markdown
: 轻量级标记语言，用于快速排版文档
: 由John Gruber创建

脚注
: 对正文内容补充说明的注释，放在文档末尾

定义列表
: 专门用来「词条+解释」的语法
### 删除线
```
~~使用两个波浪线~~
```
~~使用两个波浪线~~
### 任务列表
```
### 今日任务
- [x] 学习Markdown引用语法
- [x] 练习脚注写法
- [ ] 掌握定义列表
- [ ] 整理标题编号笔记

### 明日计划
- [ ] 学习表格语法
- [ ] 复习全部MD基础拓展语法
```
### 今日任务
- [x] 学习Markdown引用语法
- [x] 练习脚注写法
- [ ] 掌握定义列表
- [ ] 整理标题编号笔记

### 明日计划
- [ ] 学习表格语法
- [ ] 复习全部MD基础拓展语法


### 高亮提示块
```
> [!NOTE]
> 补充说明信息，蓝色框，用于备注、补充知识点

> [!TIP]
> 实用小技巧，绿色框，写捷径、优化方案

> [!IMPORTANT]
> 关键必填信息，紫色框，必须遵守的规则

> [!WARNING]
> 风险警告，橘黄色，不当操作会出错

> [!CAUTION]
> 高危提醒，红色，误操作造成严重后果
```
> [!NOTE]
> 补充说明信息，蓝色框，用于备注、补充知识点

> [!TIP]
> 实用小技巧，绿色框，写捷径、优化方案

> [!IMPORTANT]
> 关键必填信息，紫色框，必须遵守的规则

> [!WARNING]
> 风险警告，橘黄色，不当操作会出错

> [!CAUTION]
> 高危提醒，红色，误操作造成严重后果
---
> [!NOTE]
> PS:  
> 终于是写完了，主要是边看边写的，感觉对Markdown也算比较熟悉了。  
> 感觉好累，有AI实在是太好了，但还得是要靠自己练习。  
> 这篇文章涉及的内容只是markdown语法的一部分，其他变通内容需要额外学习，如下划线、缩进、文字居中、文字颜色、注释、调整图片大小、
> 图片标题、特殊字符、表格内换行、表格内列表、目录、插入视频等html特征的语法等并未涉及，需要自己学习.  
> 可参考这个教程：[Markdown 语法变通](https://markdown.com.cn/hacks.html)    
> 最后呢，感觉这些语法在需要时查也是一种很好的方法，记记这些简单的即可。
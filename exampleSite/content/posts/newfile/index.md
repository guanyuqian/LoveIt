---
weight: 1
title: "新的文档"
date: 2021-03-05T16:30:05+08:00
lastmod: 2021-03-05T16:30:05+08:00
draft: false
author: "The Sam"
authorLink: "/#"
description: "这是一篇新的文档."
resources:
- name: "featured-image"
  src: "pictrue.jpg"

tags: ["新的标签"]
categories: ["新的分类"]

lightgallery: true

toc:
  auto: false
---
# 这是一篇新的文档


## 图片引入
````
├─content           # 网站源代码目录
| ├─posts           # 一个名为posts的文件夹
| 	├─posts           # 一个名为newfile的章节文件夹
| |  | ├─index.md      # URL转换为：https://example.com/newfile
| |  | ├─pictrue.jpg   # index.md文件引用的本地图片
````

![pictrue](pictrue.jpg "pictrue title")

“_index.md”和”index.md”文件在Hugo中具有特殊含义（用于组织页面）。在“Pretty URLs”渲染下，与实际路径一致。
若文件名不为“_index.md”或“index.md”时，“Pretty URLs”将md文件渲染为目录。导致后果：md文件引用本地图片时，渲染路径比实际路径多了一个与文件名同名的目录名，导致引用图片失败。



## 显示在最外面的图片
在开头配置需要使用如下格式
````
resources:
- name: "featured-image"
  src: "<pictrue_name.jpg>"

````

## 标题注意事项
一级标题都不会出现在目录中

Hugo的坑
虽然只是一些小问题，但每次重复发生，也是一个麻烦。

Hugo的Date属性带有时区

Hugo日期格式：date: 2019-12-11T23:19:14+08:00；Hexo日期格式：date: 2019-11-25 18:49:20。在迁移时注意此问题并进行格式转换。

Hugo的网址链接

若直接输入网址（示例：https://gohugo.io/），Hugo不能识别为网址；

若粗体显示网址（示例：https://gohugo.io/），Hugo能识别为网址。

Hugo默认使用“Pretty URLs”（漂亮URL）,Hexo使用“Ugly URLs”（丑陋URL）



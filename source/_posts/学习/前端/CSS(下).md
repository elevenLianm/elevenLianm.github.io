---
title: CSS(下)
copyright: true
date: 2019-04-22 15:32:55
categories:
- 学习
- 前端
tags: CSS
---
CSS相关的知识点总结
===
`CSS相关知识的总结（下）`
<!--more-->
# 盒子模型（CSS重点）
>CSS就三大模块，盒子模型、浮动、定位，其余都是细节。要求这三部分，无论如何也要学的精通。
>所谓盒子模型就是把HTML页面中的元素看做是一个矩形盒子，也就是一个盛装内容的容器，每个矩形都由元素内容、内边距(padding)、边框(border)、外边距(margin)组成。
>网页布局本质：把网页元素比如文字图片等等，放入盒子里面，然后利用CSS白方盒子的过程，就是网页布局。
## 盒子模型（Box Model）
>所有文档元素（标签）都会生成一个矩形框，我们称为元素框，它描述了一个文档元素（标签）在网页布局所占的位置大小。因此，每个盒子除了有自己大小位置外，还影响着其他盒子的大小位置。
## 盒子边框（border）
语法：
```css
border: border-width || border-style || border-color
```
>边框属性——设置边框样式（border-style）
>边框样式用于定义页面中边框风格，常用属性值如下：
>- none：没有边框即忽略所有边框的宽度（默认值）
>- solid：边框为单实线（最为常用）
>- dashed：边框为虚线
>- dotted：边框为点线
>- double：边框为双实线
### 盒子边框写法总结表


设置内容|样式属性|常用属性值
:-:|:-:|:-:
上边框|border-top-style:样式;border-top-width:宽度;border-top-color:颜色;border-top:宽度 样式 颜色;|
下边框|border-bottom-style:样式;border-bottom-width:宽度;border-bottom-color:颜色;border-bottom:宽度 样式 颜色;|
左边框|border-left-style:样式;border-left-width:宽度;border-left-color:颜色;border-left:宽度 样式 颜色;|
右边框|border-top-style:样式;border-top-width:宽度;border-top-color:颜色;border-top:宽度 样式 颜色;|
样式综合设置|border-style:上边 [右边 下边 左边]| none无（默认）、solid单实线、dashed虚线、dotted点线、double双实线
样式综合设置|border-width:上边 [右边 下边 左边]|像素值
样式综合设置|border-color:上边 [右边 下边 左边]|颜色值、#十六进制、rgb(r,g,b)、rgb(r%,g%,b%)
样式综合设置|border:四边框度 四边样式 四边颜色|

### 表格的细边框
以前学过的html表格边框很粗，这里只需CSS一句话就可以美观起来。
```
table{border-collapse:collapse;}
表示边框合并在一起。collapse：合并
```
### 圆角边框（CSS3）
radius 半径（距离）
语法格式：
```css
border-radius: 左上角 右上角 右下角 左下角。
```
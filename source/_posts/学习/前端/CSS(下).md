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
```css
table{border-collapse:collapse;}
表示边框合并在一起。collapse：合并
```
### 圆角边框（CSS3）
radius 半径（距离）
语法格式：
```css
border-radius: 左上角 右上角 右下角 左下角。
```
## 内边距（padding）
>padding属性用于设置内边距。指边框与内容之间的距离。
>padding-top:上内边距
>padding-right:右内边距
>padding-bottom:下内边距
>padding-left:左内边距
>padding:上边距 右边距 下边距 左边距
>注意：后面跟几个数值表示的意思不一样

值的个数|表达意思
:-:|:-:
1个值|padding:上下左右边距 比如padding:3px;表示上下左右都是3像素
2个值|padding:上下边距 左右边距 比如padding:3px 5px;表示上下边距3像素 左右边距5像素
3个值|padding:上边距 左右边距 下边距 比如padding:3px 5px 3px;表示上边距3px 左右边距 5px 下边距3像素
4个值|padding:上边距 右边距 下边距 左边距 比如padding:3px 5px 10px 15px;表示上3px右5px下10px左15px顺时针

## 外边距（margin）
>margin属性用于设置外边距。设置外边距会在元素之间创建“空白”，这段空白通常不能放置其他内容。
>margin-top:上外边距
>margin-right:右外边距
>margin-bottom:下外边距
>margin-left:左外边距
>margin:上边距 右边距 下边距 左边距
>取值顺序与内边距相同。
### 外边距实现盒子居中
>可以让一个盒子实现水平居中，需要满足以下两个条件：
>1. 必须是块级元素
>2. 盒子必须制定了宽度（width）

>然后就给左右的外边距都设置为auto，就可以使块级元素水平居中。

实际工作中经常使用这种方式进行网页布局，示例代码如下：
```css
.header {width:960px; margin:0 auto}
```
### 清除元素默认的内外边距
为了更方便地控制网页中的元素，制作网页时，可以使用如下代码清除元素的默认内外边距：
```css
* {
 padding:0;
 margin:0;
}
```
> 注意：行内元素是只有左右内外边距的，是没有上下内外边距的。
## 外边距合并
>使用margin定义块元素的垂直外边距时，可能会出现外边距合并。
### 相邻块元素垂直外边距的合并
>当上下相邻的两个块元素相遇时，如果上面的元素有下外边距margin-bottom，下面的元素有上外边距margin-top，他们之间的垂直间距不是margin-bottom和margin-top之和，而是两者中的较大者。这种现象被称为相邻块元素垂直外边距的合并（也称为外边距塌陷）。
### 嵌套块元素垂直外边距的合并
>对于两个嵌套关系的块元素，如果父元素没有上内边距及边框，则父元素的上外边距会与子元素的上外边距发生合并，合并后的外边距为两者中的较大者，即使父元素的上外边距为0，也会发生合并。
![Alt text](CSS(下)/n.png)
>解决方案：
>1. `可以为父元素定义1像素的上边框或上内边距。`
>2. `可以为父元素添加overflow:hidden。`
## content宽度和高度
>使用宽度属性width和高度属性height可以对盒子的大小进行控制。
>width和height的属性值可以为不同单位的数值或相对于父元素的百分比%，实际工作中最常用的是像素值。
>大多数浏览器，如Firefox、IE6及以上版本都采用了W3C规范，符合CSS规范的盒子模型的

总宽度和总高度的计算原则是：
```
  /*外盒尺寸计算（元素空间尺寸）*/
  Element空间高度 = content height + padding + border + margin
  Element 空间宽度 = content width + padding + border + margin
  /*内盒尺寸计算（元素实际大小）*/
  Element Height = content height + padding + border （Height为内容高度）
  Element Width = content width + padding + border （Width为内容宽度）
```
注意：

1、宽度属性width和高度属性height仅适用于块级元素，对行内元素无效（ img 标签和 input除外）。

2、计算盒子模型的总高度时，还应考虑上下两个盒子垂直外边距合并的情况。

3、**如果一个盒子没有给定宽度/高度或者继承父亲的宽度/高度，则padding 不会影响本盒子大小**。
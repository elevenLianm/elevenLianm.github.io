---
title: HTML
copyright: true
date: 2019-04-12 15:03:09
categories: 
- 学习
- 前端
tags: HTML
---
HTML相关的知识点总结
===
`HTML相关知识的总结`
<!--more-->

# HTML标签

## 水平线标签

```
<hr/>
```

> 效果：在文字下方出现一行线，是单词 horizontal rule 的缩写

示例：<hr/>

## 文本格式化标签

### 粗体
```
<strong></strong>
```
> 效果：文字的斜体效果

示例：<strong>我是粗体</strong>

### 斜体
```
<em></em>
```
>效果：文字的斜体效果

示例：<em>我是斜体</em>

### 删除线
```
<del></del>
```
> 效果：文字的删除线效果

示例：<del>我是删除线</del>

### 下划线
```
<ins></ins>
```
> 效果：文字的下划线效果

示例：<ins>我是下划线</ins>

## 图片标签
```
<img src="图像URL" />
```
属性|属性值|描述
:-:|:-:|:-:
src|URL|图像路径
alt|文本|不能显示时的替换文本
title|文本|鼠标悬停时显示的内容
width|像素|设置图像宽度
height|像素|设置图像高度

## 链接标签
```
<a href="跳转目标" target="目标窗口的弹出方式"></a>
```
target属性:

|值|描述|
|:-:|:-:|
|_blank|在新窗口中打开被链接文档|
|_self|默认，在相同的框架中打开被链接文档|
|_parent|文本
|_top|在整个窗口中打开被链接文档|
|framename|在指定的框架中打开被链接文档|

### 锚点定位
> 作用：适合较长的页面，点击某个关键词，迅速到达页面中该位置
>使用方法：
>1. 使用`<a href="#id名">链接文本</a>`创建链接文本
>2. 使用相应的id名标注跳转目标位置

示例：
<a href="#锚点定位">链接文本</a>
<div id="锚点定位">跳转位置</div>

### base标签
```
<base target="_blank" />
```

> base 设置整体链接的打开状态

## 特殊字符标签

特殊字符|描述|字符代码
:-:|:-:|:-:
|空格符|`&nbsp;`
&copy;|版权|`&copy;`

# 列表

## 无序列表
```
<ul>
	<li></li>
	<li></li>
	<li></li>
</ul>
```

示例：
<ul>
	<li>无序列表</li>
	<li>无序列表</li>
	<li>无序列表</li>
</ul>
## 有序列表

```
<ol>
	<li></li>
	<li></li>
	<li></li>
</ol>
```
示例：
<ol>
	<li>无序列表</li>
	<li>无序列表</li>
	<li>无序列表</li>
</ol>
## 自定义列表

```
<dl>
	<dt>定义标题</dt>
	<dd>定义描述、解释</dd>
</dl>
```

>效果：常用于对术语或名词进行解释和描述，定义列表的列表项前没有任何项目符号。
>使用：一般用于网站底部跳转链接列表。

示例：
<dl>
 	<dt>定义标题</dt>
	<dd>定义描述、解释</dd>
	<dd>定义描述、解释</dd>
</dl>

# 表格

## 表格结构
```
<table>
<caption></caption> -------- 标题
	<thead>
	<tr>
		<th></th>
		<th></th>
		<th></th>
	</tr>
	</thead>
	<tbody>
	<tr>
		<td></td>
		<td></td>
		<td></td>
	</tr>
	<tr>
		<td></td>
		<td></td>
		<td></td>
	</tr>
	</tbody>
</table>
```

属性以及部分效果：


<table width="500px" height="100px" border="5" cellspacing="5" cellpadding="5" align="center">
<caption>标题</caption>
<thead>
	<tr>
		<th align="center">属性名</th>
		<th align="center">含义</th>
		<th align="center">常用值</th>
	</tr>
</thead>
<tbody>
  <tr>
		<td>border</td>
		<td>设置表格边框</td>
		<td>像素值</td>
	</tr>
	<tr>
		<td>cellspacing</td>
		<td>设置单元格与单元格之间的空白距离</td>
		<td>像素值(默认为2像素)</td>
	</tr>
	<tr>
		<td>cellpadding</td>
		<td>设置单元格内容与边框间的空白距离</td>
		<td>像素值(默认为1像素)</td>
	</tr>
	<tr>
		<td>width</td>
		<td>设置表格宽度</td>
		<td>像素值</td>
	</tr>
	<tr>
		<td>height</td>
		<td>设置表格宽度</td>
		<td>像素值</td>
	</tr>
	<tr>
		<td>align</td>
		<td>设置表格在网页中的水平对齐方式</td>
		<td>left、center、right</td>
	</tr>
</tbody>
</table>

## 合并单元格
>跨行合并：rowspan
>跨列合并：colspan

```
<table>
<tr>
	<td rowspan=2></td>
	<td colspan=2></td>
</tr>
<tr>
	<td></td>
	<td></td>
</tr>
</table>
```

效果：


<table>
<tr>
	<td rowspan=2>跨行合并</td>
	<td colspan=2>跨列合并</td>
</tr>
<tr>
	<td>测试</td>
	<td>测试</td>
</tr>
</table>

# 表单

## 表单控件

### input 控件
> input是单标签
> input有多种形状，通过type属性改变形状


属性|属性值|描述
:-:|:-:|:-:
type|text|单行文本输入框
type|password|密码输入框
type|radio|单选按钮
type|checkbox|复选按钮
type|button|普通按钮
type|submit|提交按钮
type|reset|重置按钮
type|image|图像形式的提交按钮
type|file|文件域
name|用户自定义|空间名称
value|用户自定义|控件默认文本值
size|正整数|控件在页面中显示的宽度
checked|checked|定义选择控件默认被选中的项
maxlength|正整数|控件允许输入的最多字符数


示例：
<input type="text" name="文本框" value="文本框" size="30" maxlength="6"/>
<input type="password"/>
<input type="radio"/>
<input type="checkbox" checked="checked"/>
<input type="button" value="按钮"/>
<input type="submit" value="提交"/>
<input type="reset" value="重置"/>
<input type="image" value="图片按钮" src="HTML/WechatIMG4.jpeg"/>
<input type="file" value="文件上传"/>

### label标签
> 作用：用于绑定一个表单元素，点击label标签的时候，被绑定的表单元素会获得输入焦点。
> 用法：
> 1. 用label直接包裹input
> 2. 通过for、id格式绑定

```
<label>输入框：<input type="text" name="文本框" value="文本框" /></label>
```

<label>输入框：<input type="text" name="文本框" value="文本框" /></label>

```
<label for="2">输入框：</label>
<input type="text" name="文本框" value="文本框" />
<input type="text" id="2" name="文本框" value="文本框" />
```

<label for="q">输入框：</label>
<input type="text" name="文本框" value="文本框" />
<input type="text" id="q" name="文本框" value="文本框" />

### textarea控件(文本域)

```
<textarea></textarea>
```
示例：
<textarea>请输入留言</textarea>

### 下拉菜单

```
<select>
<option>北京<option>
<option selected="selected">上海</option>
<option>广州<option>
</select>
```
示例：
<select>
<option>北京</option>
<option selected="selected">上海</option>
<option>广州</option>
</select>

## 表单域

```
<form action="url地址" method="提交方式" name="表单控件">
<p>用户名：<input type="text" name="username" id=""></p>
<p>密&nbsp;&nbsp;&nbsp;&nbsp;码：<input type="password" name="password" id=""></p>
<input type="submit" name="" id="">
<input type="reset" name="" id="">
</form>
```

示例：
<form action="url地址" method="提交方式" name="表单控件">
<p>用户名：<input type="text" name="username" id=""></p>
<p>密&nbsp;&nbsp;&nbsp;&nbsp;码：<input type="password" name="password" id=""></p>
<input type="submit" name="" id="">
<input type="reset" name="" id="">
</form>

# HTML5
> 文档类型设定：`<!DOCTYPE html>`
> 字符设定：`<meta charset=utf-8>`

## HTML5新增标签

```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Title</title>
</head>
<body>
<header>语意：定义页面头部、页眉</header>
<nav>语意：定义导航链接</nav>
<footer>语意：定义页面底部页脚</footer>
<article>语意：定义文章</article>
<section>语意：定义文档的节、区段</section>
<aside>语意：定义其所处内容之外的内容、侧边</aside>
<fieldset>
</fieldset>
</body>
</html>
```

### datalist标签
>作用：定义输入框下拉列表，带提示功能。
```
<input type="text" value="输入明星" list="star"/>
<datalist id="star"> ------  定义选项列表，与input一起使用，通过list-id绑定
    <option>刘德华</option>
    <option>刘晓庆</option>
    <option>刘若英</option>
    <option>张学友</option>
</datalist>
```
示例：
<input type="text" value="输入明星" list="star"/>
<datalist id="star">
    <option>刘德华</option>
    <option>刘晓庆</option>
    <option>刘若英</option>
    <option>张学友</option>
</datalist>

### fieldset标签
> 作用：将表单内的相关元素分组、打包，与legend搭配使用
```
<fieldset>
    <legend>用户登录</legend>
    用户名：<input type="text"><br>
    密码：<input type="password">
</fieldset>
```
示例：
<fieldset>
    <legend>用户登录</legend>
    用户名：<input type="text"><br>
    密码：<input type="password">
</fieldset>

### 新增的input type属性值

类型|示例|含义
:-:|:-:|:-:
email|`<input type="email">`|输入邮箱格式
tel|`<input type="tel">`|输入手机号码格式
url|`<input type="url">`|输入url格式
number|`<input type="number">`|输入数字格式
search|`<input type="search">`|搜索框（体现语义化）
range|`<input type="range">`|自由拖动滑块
time|`<input type="time">`|小时分钟
date|`<input type="date">`|年月日
datetime|`<input type="datetime">`|时间
month|`<input type="month">`|月年
week|`<input type="week">`|星期 年

示例：
<fieldset>
    <legend>新增input type属性值</legend>
    <label>email:<input type="email"></label><br>
    <label>tel:<input type="tel"></label><br>
    <label>url:<input type="url"></label><br>
    <label>number:<input type="number"></label><br>
    <label>search:<input type="search"></label><br>
    <label>range:<input type="range"></label><br>
    <label>time:<input type="time"></label><br>
    <label>date:<input type="date"></label><br>
    <label>datetime-local:<input type="datetime-local"></label><br>
    <label>month:<input type="month"></label><br>
    <label>week:<input type="week"></label><br>
	<label>color:<input type="color"></label><br>
    <input type="submit">
    <input type="reset">
</fieldset>

### input新增的属性

属性|用法|含义
:-:|:-:|:-:
placeholder|`<input type="text" placeholder="请输入用户名">`|占位符提供可描述输入字段预期值的提示信息
autofocus|`<input type="text" autofocus>`|规定当前页面加载时input元素自动获取焦点
multiple|`<input type="file" multiple>`|多文件上传
autocomplete|`<input type="text" autocomplete="off">`|规定表单是否应该启用自动完成功能 有2个值，on代表记录已输入的值 用法：1.autocomplete 必须有提交按钮 2.表单必须给名字
required|`<input type="text" required>`|必填项
accesskey|`<input type="text" accesskey="s">`|规定激活（获取焦点）的快捷键，采用alt+字母形式

示例：
<form action="">
    placeholder:<input type="text" placeholder="请输入用户名"><br>
    autofocus:<input type="text" autofocus><br>
    <input type="file" multiple><br>
    1.autocomplete 必须有提交按钮<br>
    2.表单必须给名字<br>
    autocomplete: <input type="text" autocomplete name="username"><br>
    required:<input type="text" required><br>
    accesskey:<input type="text" accesskey="s"><br>
    <input type="submit">
</form>

## 多媒体标签
> embed：标签定义嵌入内容
> audio：播放音频
> video：播放视频

### embed标签
```
<embde src='资源路径'></embed>
```

### audio标签
>autoplay属性：可以自动播放
>controls属性：显示播放器
>loop属性：循环播放，填入正整数，-1表示无限循环

```
为了浏览器兼容，需要做三种声音文件：ogg、mp3、wav
<audio  autoplay controls loop="1">
    <source src="xxx.mp3">
    <source src="xxx.ogg">
    <source src="xxx.wav">
    您的浏览器不支持播放声音
</audio>
```
示例：
<audio  autoplay controls loop="1">
    <source src="xxx.mp3">
    <source src="xxx.ogg">
    <source src="xxx.wav">
    您的浏览器不支持播放声音
</audio>

### video标签
>autoplay属性：可以自动播放
>controls属性：显示播放器
>loop属性：循环播放，填入正整数，-1表示无限循环
>width属性：设置播放器宽度
>height属性：设置播放器高度
```
为了浏览器兼容，需要做三种视频文件：ogg、mp4、webM
<video width="100px" height="100px" src="" controls autoplay loop="1">
    <source src="xxx.opp">
    <source src="xxx.mp4">
    <source src="xxx.webM">
    您的浏览器不支持播放视频
</video>
</body>
</html>
```
为了浏览器兼容，需要做三种视频文件：ogg、mp4、webM
<video width="300px" height="300px" src="" controls autoplay loop="1">
    <source src="xxx.opp">
    <source src="xxx.mp4">
    <source src="xxx.webM">
    您的浏览器不支持播放视频
</video>
</body>
</html>
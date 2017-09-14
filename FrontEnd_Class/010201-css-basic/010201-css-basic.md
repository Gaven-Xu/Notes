<!-- TOC -->

- [1. 说明](#1-说明)
    - [1.1. 知识介绍](#11-知识介绍)
    - [1.2. 学习目标](#12-学习目标)
- [2. 三种CSS位置](#2-三种css位置)
- [3. 选择器](#3-选择器)
    - [3.1. * 选择器（通用选择器）](#31--选择器通用选择器)
    - [3.2. 标签选择器](#32-标签选择器)
    - [3.3. 类选择器](#33-类选择器)
    - [3.4. id选择器](#34-id选择器)
    - [3.5. 分类选择器、子代选择器、后代选择器、分组选择器](#35-分类选择器子代选择器后代选择器分组选择器)
    - [选择器优先级](#选择器优先级)
    - [3.6. 伪类选择器](#36-伪类选择器)
- [4. 字体](#4-字体)

<!-- /TOC -->
# 1. 说明
## 1.1. 知识介绍

CSS:Cascading Style Sheet，层叠样式表、级联样式表、样式表。用来对HTML文档内容进行修饰，并且，内容（HTML）与表现分离（CSS）

## 1.2. 学习目标

熟悉CSS几种写法，以及其优先级，并学习字体相关css控制

---

# 2. 三种CSS位置
**内联样式：** 多个属性键值对，以分号 ; 隔开，只作用在特定的标签内，其它标签不受影响
```html
<!DOCTYPE html>
<html>
  <head>
    <meta charset="utf-8">
    <title>内联样式</title>
  </head>
  <body style="background:#f00;margin:0;">

  </body>
</html>
```
**内部样式：** 写在head内的style标签内
```html
<!DOCTYPE html>
<html>
  <head>
    <meta charset="utf-8">
    <title>内部样式</title>
    <style>
      body{
        background: #0f0;
      }
    </style>
  </head>
  <body>

  </body>
</html>
```
**外部样式** 写在css文件中，在head内用link标签引入
HTML文件：index.html
```html
<!DOCTYPE html>
<html>
  <head>
    <meta charset="utf-8">
    <title>内部样式</title>
    <link rel="stylesheet" href="./style.css">
  </head>
  <body>

  </body>
</html>
```
CSS文件：style.css
```css
body{
  background: #00f;
}
```
---
css样式可以继承
css可以被重复定义
css样式具有优先级：

    浏览器默认值 < 外部样式 < 内部样式 < 行内样式 < !important

---

# 3. 选择器
先看一下这段代码：
```html
<!DOCTYPE html>
<html>
  <head>
    <meta charset="utf-8">
    <title></title>
  </head>
  <body id="Content" class="index box">
    <div class="box"> 0 </div>
    <div class="box">
      1
      <span class="box"><span class="box"><span class="box"> 2 </span></span></span>
      <span class="box"> 3 </span>
    </div>
    <span class="box"> 4 </span>
  </body>
</html>
```
## 3.1. * 选择器（通用选择器）
选中任意标签
```css
* {
  background: #fff;
}
```

## 3.2. 标签选择器
在下面的格式中，我们把 { 前面的内容叫做选择器，body在这里就是一个标签选择器
```css
body{
  background: #00f;
}
```

## 3.3. 类选择器
定义一组元素的通用样式
一个标签可以给多个类名，并且，多个标签也可以给同样一个类名，但是类名不能以数字开头
```css
.index{
  background: #00f;
}
.box{
  background: #0ff;
}
```

## 3.4. id选择器
定义某**一个**元素的样式
```css
#Content{
  background: #f00;
}
```



## 3.5. 分类选择器、子代选择器、后代选择器、分组选择器
```css
/*分类选择器*/
div.box{
  color:#f00;
}

/*子代选择器*/
div>.box{
  color:#f00;
}

/*后代选择器*/
div .box{
  color:#0f0;
}

/*兄弟选择器*/
div+.box{
  color:#0f0;
}

/*分组选择器*/
div.box,div>.box{
  color:#f00;
}

```
## 选择器优先级
同类选择器之间，后面覆盖前面

不同之间

	id	>	class	>	tag	>	*
	1000		100		10		1

## 3.6. 伪类选择器

链接伪类：
```css
a:link{
  color:#666;
}
a:visited{
  color:#6f6;
}
```

动态伪类：
```css
div:hover{
  color:#666;
}
a:active{
  color:#6f6;
}
a:focus{
  color:#66f;
}
```

---

# 4. 字体
```css
.some{
	font-family:"微软雅黑","Arial";
	/* 字体：
		可以写多个字体，选取第一个支持的字体，否则浏览器默认
		font-family:"Microsoft Yahei","Arial";
	*/

	font-size:12px;
	/* 字体大小 ，浏览器默认字体大小16px*/

	font-weight:bold;
	/* 粗体
		400-900
		normal < 500 < bold
	*/

	font-style:italic;
	/*斜体
		normal：默认不斜体
		italic：斜体
	*/

	font:italic small-caps bold 16px/32px '微软雅黑';
	/*font : 第一种简写形式 6个参数
		font-style
		font-variant
		font-weight
		font-size/line-height
		font-family;
	*/

	font:16px/32px "微软雅黑";
	font:bold 16px/32px "微软雅黑";
	/*第二种简写形式，两个/三个参数*/

	color:#f00;
	/*文本颜色*/

	text-align:center;
	/*文本水平对其方式
		left center right
	*/

	vertical-align:middle;
	/*设置图片和文字的垂直对齐方式
		top
		middle
		bottom
	*/

	text-decoration: none;
	/*额我那本线条修饰
		none 默认 无
		underline 下划线
		overline 上划线
		line-through 删除线
	*/

	line-height: 32px;
	/*行高，单行文本所占高度，文本在改行内垂直居中*/

	text-indent: 32px;
	/*首行文本缩进距离*/

	text-shadow: 3px 5px 1px #f00;
	/*
		text-shadow: 右偏移量 下偏移量 阴影大小 阴影颜色;
	*/

	white-space: normal;
	/*文本过长时，是否换行
		normal，采用浏览器默认
		nowrap，不换行
	*/

	overflow: hidden;
	text-overflow: clip;
	/*文本溢出，需要与overflow：hidden一起使用
		clip 直接裁剪
		ellipsis 用 ... 显示未显示的内容
	*/
}
```

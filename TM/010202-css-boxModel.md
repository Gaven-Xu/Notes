<h1 style="text-align:center">CSS基础-2</h1>

<!-- toc orderedList:0 depthFrom:1 depthTo:6 -->

- [说明](#说明)
	- [知识介绍](#知识介绍)
	- [学习目标](#学习目标)
- [1. 内容 - 宽高](#1-内容-宽高)
- [2. 边框](#2-边框)
	- [2.1 边框宽度+样式+颜色](#21-边框宽度样式颜色)
	- [2.2. 边框圆角](#22-边框圆角)
- [3. 内边距](#3-内边距)
- [4. 外边距](#4-外边距)
- [5. 显示](#5-显示)
	- [5.1. 显示方式 display](#51-显示方式-display)
	- [5.2. 可见 visibility](#52-可见-visibility)
	- [5.3. 透明度 opacity](#53-透明度-opacity)
	- [5.4. 光标](#54-光标)

<!-- tocstop -->

---

# 说明
## 知识介绍

CSS盒子模型，包括内容、边框、外边距、内边距，是描述一个布局元素的最基本css熟悉

## 学习目标

熟悉CSS盒子模型的构成，以及元素显示相关的css

---

# 1. 内容 - 宽高
width: 宽度
max-width：最大宽度
min-width：最小宽度

height：高度
max-height：最大高度
min-height：最小高度

宽高取值可以是px、%等多种方式

---

# 2. 边框

## 2.1 边框宽度+样式+颜色
```css
.some{
  border:5px solid #f00;
}
/*简写*/

.some{
  border-width: 5px;
  border-style: solid;
  border-color: #f00;
}
/*完整写法*/

.some{
  border-top: 5px solid #f00;
  border-right: 5px solid #f00;
  border-bottom: 5px solid #f00;
  border-left: 5px solid #f00;
}
/*分别控制 ... ... */
```
补充，如果对于一个高宽为0的元素，给其设定边框，会出现什么？

## 2.2. 边框圆角
```css
.some{
  border-radius:25px;
}

.some{
  border-radius:50%;
}

.some{
  border-radius:50% 5px 50% 5px;
}
```

---

# 3. 内边距

元素内容距离边框的距离

内边距，会增加元素的真实高宽
```css
.some{
	padding: 20px; /*全部*/
}
.some{
	padding: 20px 20px; /*上下，左右*/
}
.some{
	padding: 20px 40px 20px; /*上，左右，下*/
}
.some{
	padding: 10px 20px 30px 40px; /*上，右，下，左*/
}
.some{
	padding-top: 10px;
	padding-right: 20px;
	padding-bottom: 30px;
	padding-left: 40px;
}
```
---

# 4. 外边距

元素与周围的距离，围绕在元素周围的空白区域

不会增加元素的真实高宽，外边距是透明的

写法与padding一致
```css
.some{
	margin:10px 20px 30px 40px;
}
```

# 5. 显示
## 5.1. 显示方式 display
```css
.some{
	display: none;
	/*隐藏元素，并且，不再占据原来的文档流空间*/

	display: block;
	/*让任意一个元素，像块级元素一样显示*/

	display: inline;
	/*让任意一个元素，像行内元素一样显示*/

	display: inline-block;
	/*相比inline，inline-block还可以设置高宽*/
}
```
## 5.2. 可见 visibility
```css
.some{
	visibility: visible;
	/*默认，可见*/

	visibility: hidden;
	/*隐藏，但是依然占据原来位置*/
}
```
## 5.3. 透明度 opacity
```css
.some{
	opacity: 0.3;
}
```
注意与`background-color:rgba(0, 0, 0, 0);`对比

## 5.4. 光标
```css
.some{
	cursor:pointer;
	/*结合浏览器提醒去记忆*/
}
```

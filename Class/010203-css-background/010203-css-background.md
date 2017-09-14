<h1 style="text-align:center">CSS基础-3</h1>

<!-- toc orderedList:0 depthFrom:1 depthTo:6 -->

- [说明](#说明)
	- [知识介绍](#知识介绍)
	- [学习目标](#学习目标)
- [1. Background](#1-background)
	- [1.1. 常见属性](#11-常见属性)
	- [1.2. 常见简写](#12-常见简写)

<!-- tocstop -->

---

# 说明
## 知识介绍

CSS盒子模型，包括内容、边框、外边距、内边距，是描述一个布局元素的最基本css熟悉

## 学习目标

熟悉CSS盒子模型的构成，以及各属性的作用

---

# 1. Background

## 1.1. 常见属性

```css
.some{
	background-color: #f00;
	/*
		#ff0000;
		rgb(255,255,255);
		rgba(255,255,255,0.54);
	 */

	background-image: url('./image.jpg');
	/*
		url("./image.jpg")
		url('./image.jpg')
		url(./image.jpg) 不推荐
	 */
	background-repeat:;
	/*
		repeat 双向平铺 默认
		no-repeat
		repeat-x
		repeat-y
	 */
	background-attachment: fixed;
	/*
		scroll 默认，背景图随页面滚动
		fixed 背景图不随页面滚动
	 */

	background-position: center;
	/*
		第一位 X轴 , 第二位 Y轴
		100px  100px auto
		100%   100% auto
		center = center center
		left =  left center
		top = center top
	 */
```

## 1.2. 常见简写

```css
.some{
		background: url('./image.jpg') no-repeat;
		background: #f00 url('./image.jpg') no-repeat center;
		background: #f00 url('./image.jpg') no-repeat bottom left;
		background: #f00 url('./image.jpg') no-repeat left bottom;
		background: #f00 url('./image.jpg') no-repeat 10px 50px;
}
```

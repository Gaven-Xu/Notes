<h1 style="text-align:center">CSS基础-4</h1>

<!-- toc orderedList:0 depthFrom:1 depthTo:6 -->

- [说明](#说明)
	- [知识介绍](#知识介绍)
	- [学习目标](#学习目标)
- [1. float](#1-float)
- [2. 清除浮动](#2-清除浮动)
	- [2.1. 第一种：不推荐](#21-第一种不推荐)
	- [2.2. 第二种：空div，clear both](#22-第二种空divclear-both)
	- [2.3. 第三种：:after 伪类](#23-第三种after-伪类)

<!-- tocstop -->

---

# 说明
## 知识介绍

浮动，float是css排版中比较容易难以理解，往往要借助排版联系加深理解

## 学习目标

熟悉CSScss浮动，以及几种清除浮动的方法

---

# 1. float
# 2. 清除浮动
清除浮动的原则：
1. 父容器可以正常的撑开，而不是撑破
2. 后续的元素，不会受到前面浮动的影响
3. 在浮动元素的最后，清除浮动
## 2.1. 第一种：不推荐
```html
<div class="father">
	<div class="son son1"></div>
	<div class="son son2"></div>
	<div class="son son3"></div>
</div>
```
```css
.father{
	overflow: auto;
}
```
## 2.2. 第二种：空div，clear both
```html
<div class="father">
	<div class="son son1"></div>
	<div class="son son2"></div>
	<div class="son son3"></div>
	<div class="clear"></div>
</div>
```
```css
.clear{
	clear:both;
}
```
## 2.3. 第三种：:after 伪类
```html
<div class="father">
	<div class="son son1"></div>
	<div class="son son2"></div>
	<div class="son son3"></div>
</div>
```
```css
.father：after{
	display: block;
	clear: both;
	content: " ";
}
```

<h1 style="text-align:center">CSS基础-5</h1>

<!-- toc orderedList:0 depthFrom:1 depthTo:6 -->

- [说明](#说明)
	- [知识介绍](#知识介绍)
	- [学习目标](#学习目标)
- [1. position](#1-position)
	- [relative](#relative)
	- [absolute](#absolute)
	- [fixed](#fixed)
- [2. 绝对居中](#2-绝对居中)
	- [父容器高宽不确定 子容器高宽确定](#父容器高宽不确定-子容器高宽确定)

<!-- tocstop -->
---

# 说明
## 知识介绍

定位是继浮动（float）之后，又一个需要多花时间联系的CSS属性，在排版中经常用到

## 学习目标

熟悉相对、绝对、固定定位的用法，能够区分其差别

---
# 1. position

## relative

1. 相对原来位置偏移
2. 不会删除它原来所占据的文档流空间
3. top、right、bottom、left 相对于原来位置的偏移量

## absolute

1. 从内往外找，找到第一个具有position属性，且属性值不为static的元素，然后相对与这个元素（X）定位
2. 会删除原来所占据的空间
3. top、right、bottom、left 相对（X）边框的距离

## fixed
1. 相对于浏览器的可视区域定位
2. 会删除原来所占位置
3. top、right、bottom、left 相对浏览器可视区域的距离

# 2. 绝对居中

## 父容器高宽不确定 子容器高宽确定
1.
```css
.father{
  position: relative;
}
.son{
  width:100px;
  height:100px;
  position: absolute;
  left:50%;
  top:50%;
  margin-left:-50px;
  margin-top:-50px;
}
```

2.
```css
.father{
  position: relative;
}
.son{
  width:100px;
  height:100px;
  position: absolute;
	margin:auto;
	top:0;
	bottom:0;
	left:0;
	right:0;
}
```

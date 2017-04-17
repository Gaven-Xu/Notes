<h1 style="text-align:center">CSS常见问题</h1>


<!-- toc orderedList:0 depthFrom:1 depthTo:6 -->

- [说明](#说明)
	- [知识介绍](#知识介绍)
	- [学习目标](#学习目标)
- [1. 双飞翼布局](#1-双飞翼布局)
- [2. 子元素的margin-top会传递给父元素](#2-子元素的margin-top会传递给父元素)

<!-- tocstop -->

---
# 说明
## 知识介绍

定位是继浮动（float）之后，又一个需要多花时间联系的CSS属性，在排版中经常用到

## 学习目标

熟悉相对、绝对、固定定位的用法，能够区分其差别

# 1. 双飞翼布局
结合absolute或者fixed
```css
.father{
  position: relative;
	min-height:300px;
}
.father>*{
  position: absolute;
}

.left{
  width:50px;
  top:0;
  bottom:0;
}
.center{
  top:0;
  bottom:0;
  left:50px;
  right:100px;
}
.right{
  width:100px;
  top:0;
  bottom:0;
}
```

# 2. 子元素的margin-top会传递给父元素
1、修改父元素的高度，增加padding-top样式模拟（padding-top：1px；常用）
2、为父元素添加overflow：hidden；样式即可（完美）
3、为父元素或者子元素声明浮动（float：left；可用）
4、为父元素添加border（border:1px solid transparent可用）
5、为父元素或者子元素声明绝对定位

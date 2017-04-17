# css基础
自定义字体
```css
@font-face{
	font-family:"baidu",
	src:url('')
}
```
Emmet语法
# js的基础
```javascript
// 原始类型 引用类型
// String Boolean Number Null(声明，类型为空) undefined(声明，但是无类型，无值)
// Object Array Date ...
var a = 3;
var b = a;
b--;
// a = 3;

var a = ['3'];
var b = a;
b[0]--;
//a[0] = 2;

var a = {
	key:3
}
var b = a;
b.key--; // a.key = 2
```

内存回收机制

// 页面关闭，内存清除
// 浏览器垃圾回收器定时扫描（标记清除算法），清除无用的内存
// 手动清除引用 xxxobject = null

//

# js的深度理解
  一切皆对象 + 一切对象皆有原型
  面向对象：对象原型的深度拷贝
```javascript
var LB3  = objectCopy(LB.prototype);

function objectCopy(Object) {
  var tempObject = {};
  for(var i in Object){
    tempObject[i] = Object[i];
  }
  return tempObject;
}
```
  异步 单线程

-----# 后端语言
   java php

# 实际开发的经验
  HTML jade ejs swig / jsp asp php
  CSS sass(sass,scss) less
  JS ES6+，typescript，coffescript(语法与ruby、jade类似)
  Gulp 构建工具，编译

  Nodejs（npm） 一个层次，会用相关的工具；第二个层次，熟悉nodejs的api

	// 表达能力
	// 性格
	// 学习能力

		官方文档 / baidu.com / 论坛、贴吧、知乎 / 朋友，同事，问
		自己写的代码 rem
		自己整理的经验
		比较好的文档
		比较好的思维

	// 经验
	// 技术

## Git操作
git init
git remote add origin [你需要添加的远程地址]

git pull origin master
git push origin master

查看分支
	git branch -v
创建本地分支
	git checkout -b [需要创建的分支名称]
切换本地分支
	git checkout [已经创建的分支名称]
合并分支
	git merge [你的开发版本]  // 前提，已经在你的主干分支(master)上
删除分支
	git branch -d [需要删除的分支] // -D 表示强制删除

查看远程分支（所有）
	git branch -a
创建远程分支
	git push origin master:[需要创建的远程分支名称]
删除远程分支
	git push origin --delete [需要删除的远程分支名称]



git reset --hard [每次commit 的编号]
git log // 看记录
# 编辑器
```txt
// ctrl + alt + f // js json 格式化

// shift + alt + 1 2 3 4 5 8 9 划分编辑器窗口

// ctrl + shift + c  // css comb  setting '{'

// shift + ctrl + up/down

// ctrl + f // ctrl + g
```
# PS技巧
  积累各种模板素材、网站，学会模仿

# SEO
  0. 代码 src herf alt title rel（nofollow）
  1. 内容维护 文案
  2. 在线推广 论坛 贴吧 博客 微博 微信
  3. 地推
  4. 付费

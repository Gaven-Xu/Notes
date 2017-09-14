<h1 style="text-align:center">Js基础</h1>

---

# 1. 说明
## 1.1. 知识介绍

Javascript使我们前端程序员的核心语言，主要用来进行用户交互，客户端数据验证，异步数据传输等相关开发，相比HTML和CSS，javascript是一门真正的编程语言

## 1.2. 学习目标

本课程为JS的基础课，主要目标在于：
1. 了解JS的作用
2. 熟悉一款编辑器
3. 语句的最后，分号可加可不加，建议加上，表示该语句已结束

---
# 2. 什么是JS：

	前端三大语言：HTML CSS JS
	交互：输入数据 处理数据 返回结果

	JavaScript：
	
---
# 3. 小插曲：浏览器发展历程

1995

> 全球第一大公司 网景 : LiveScript 如日中天

> 收费产品

> 一个程序员发现一个问题：电话线上网，网速慢，很长时间才能把数据发给对方，发现错误之后，又要返回给用户修改，又要很长时间，那么，数据能不能在用户端就进行验证。后来他发明了一门语言，叫LiveScript

> 语言知名度不大，没人使用，因为当时流行Java，为了蹭热度，改名JavaScript


1996

> 比尔盖茨收购网景失败，建立团队，开发IE1.0，项目仓促，非常多bug，不战而败

1997

> IE 2.0 bug依然有

1998

> IE 3.0 还是打不过

> 这一年，js需要制定标准，由欧洲计算机组织创建了ECMA标准

1999

> 微软开大招，IE4.0跟系统捆绑销售，免费赠送，网景直接倒闭，但是网景公开了浏览器源代码 -> firefox

1999-2008

> IE近10年的天下，firefox提供的标准，促进了chrome的发展和移动互联网，最终又干掉了IE


2004 网景：Mozilla 火狐
W3C（万维网）：
DOM标准：专门操作网页内容的API-所有浏览器都支持
BOM：专门操作网页浏览器窗口

---

# 4. JavaScript编程语言

编程语言分类：解释型语言

> 编译型：需要编译才能运行，C，Java,...,运行效率高

> 解释型：不需要编译，python，perl，php，javascript，运行效率低，编写效率高

## 4.1. 编辑器
前端常用编辑器包括：
EditPlus，notepad++，sublime text，visio studio code，Atom ...

---
# 5. 如何编写js
## 5.1. JS语法特点

	1. 区分大小写
	2. 换行不敏感
	3. 语句结尾，分号可写可不写，建议写上，表示该语句已结束

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta http-equiv="X-UA-Compatible" content="ie=edge">
    <title>Document</title>
</head>
<body>
	<script>
		document.write('人如果没有梦想，与咸鱼何异');
		document.write('<br>');
		document.write('咸鱼也可以有梦想');
		document.write('&lt;br&gt;');		
	</script>
</body>
</html>
```

## 5.2. JS书写位置

	1、在网页中<script>标签中，内部

	2、在外部创建js 在页面引用，外部
		<script src=""></script>

	3、在标签内写，内联
		事件：用户或浏览器自身触发的动作；
		只有在事件出发后才会执行代码
		
	4、在浏览器控制台编写js语句；
		Console指控制台：专门编写和调试js的程序窗口；

## 5.3. 如何调试js

	bug程序出错 debug
	js控制台报错：错误信息、错误原因、错误位置连接、出错现象
# 6. 字面量
直接拿来用的值，比如：
```js
console.log(1);
console.log('Hello World');
```
# 7. 变量
什么是变量：内存中一块存储数据的存储空间，然后再起一个名字

什么时候使用变量：在程序中任何数据都先用变量保存，再处理；

怎么使用变量：声明 赋值 取值

```js
var a = 5;
document.write(a);
// var 跟系统申请一个空间
// a   给空间起名叫做a
// 5   一个数字5
// =   将右边的值，存储到左边的空间中
// document.write(a); 从空间a中取出值来使用
```

1、声明：在内存中创建一个变量的过程

	语法：var 变量名；
	命名规则：
		由数字，字母，下划线，$组成
		不能以数字开头
		不能使用关键字和保留字
	
	命名规范：
		不要用单字母，拼音
		见名知意，多个单词 驼峰式命名
		studentName

2、赋值：将数据保存在变量中

		变量名=数据；

3、取值：从变量中提取数据，进行运算

# 8. 数据类型

数据在内存中的存储格式

js数据类型 2大类：原始类型 引用类型

**原始类型：数据直接保存在变量本地的类型**

Number（数字）
String（字符串）
Boolean（真假）
undefind null（不指向任何地址）

	1、Number：js中专门保存数字的类型
		所占空间
		1G=1024MB 1MB=1024KB 1KB=1024byte 1byte=8bit
	2.String：指的是专门保存一串文字的数据类型；
		所占空间 unicode
		字符串一旦创建 不能改变 想改变只能创建新的字符串去替换旧的字符串
	3、Boolean：专门定义真假类型

**引用类型：数据不保存在变量本地的类型**
各种对象：Object / Array / Function / Date / RegExp ...

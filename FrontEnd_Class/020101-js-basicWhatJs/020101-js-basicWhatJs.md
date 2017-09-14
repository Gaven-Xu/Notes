<h1 style="text-align:center">Js基础</h1>

---
[toc]
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
## 5.1. JS书写位置

	1、在网页中<script>标签中，内部

	2、在外部创建js 在页面引用，外部
		<script src=""></script>

	3、在标签内写，内联
		事件：用户或浏览器自身触发的动作；
		只有在事件出发后才会执行代码
		
	4、在浏览器控制台编写js语句；
		Console指控制台：专门编写和调试js的程序窗口；
		
## 5.2. HelloWorld
```html
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta http-equiv="X-UA-Compatible" content="ie=edge">
    <title>Document</title>
</head>
<body>
	<script>
		document.write('Hello World!');
	</script>
</body>
</html>
```
## 5.3. JS语法特点

	1. 区分大小写
	2. 换行，空格，缩进不敏感
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
		alert('Hello World!');	
		console.log('Hello World!');	
	</script>
</body>
</html>
```

## 5.4. 注释

```js
document.write('Hello World~');
// Hello 我是一个单行注释
/*
你好，我们是多行注释
你好，我们是多行注释
你好，我们是多行注释
你好，我们是多行注释
*/
```

## 5.5. 如何调试js

	bug程序出错 debug
	js控制台报错：错误信息、错误原因、错误位置连接、出错现象
	
# 6. 字面量

直接拿来用的值，比如：
```js
console.log(1);
console.log('Hello World');
```

## 6.1. 数字的字面量

	10进制：普通的数字就是十进制
	8进制：如果以0开头、或者以0o开头、或者以0O开头的都是八进制，八进制只能用0~7来表示
	16进制：如果以0x开头的都是十六进制。

	科学计数法：5e12 -5e12 5e-12

	Infinity NaN

## 6.2. 字符串的字面量

字符串，也就是我们常说的语句、词

> 字符串（string），必须用双引号或者单引号包含起来

> 字符串支持独特的转义字符 \n \t \" \' \\

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

	变量必须先赋值，才能使用

## 7.1. 变量的赋值

1. 变量的赋值符号是 = 
```js
var a;
a = 1;
```
2. 声明和赋值可以合成一句去写
```js
var a = 1;
```

3. 变量可以被重复赋值
```js
var a = 1;
a = 2;
a = 3;
```

4. 如果只定义，不赋值？
```js
var a;
console.log(a); //  undefined; 未定义完成
```

5. 如果未定义就赋值？
```js
a = 100;
console.log(a);
```
看似没有区别，实际上，我们创建了一个全局变量，日后我们会学习到其区别

## 7.2. 变量的声明提升

声明会提前，赋值过程留在原地
```js
console.log(a); 
var a = 100;
```
相当于
```js
var a;
console.log(a); // undefined 而不是 报错：a is not defined
a = 100;
```

## 7.3. 区分变量和直接量
```js
var a = 100;
console.log("a");
// 注意，加上引号之后，“a”只是一个字符串，失去了变量的含义
```
# 8. JS变量类型

js数据类型 2大类：基本类型 引用类型

**基本类型、原始类型：数据直接保存在变量本地的类型**

number 		数字类型
string 		字符串类型
undefined 	undefined类型，自成一种类型，表示变量定义但是未赋值
null 		null类型，自成一种类型，空对象，我们遇到了再说
boolean 	布尔类型，这个类型只有两种值，true和false

**引用类型：我们讲到了再说**

## 8.1. typeof 关键字

用来检测一个变量的类型

```js
var a = 100;
console.log(typeof a);// number

// 以下变量全是number类型
var a = 100;
var b = 234243245345;
var c = -345345435435;
var d = 345.3245234;
var e = .5e6;
var f = 0xff;
var g = 017;
var h = Infinity;
var i = NaN;

// 以下全是string类型
var m1 = "哈哈";
var m2 = "123";	
var m3 = ""; //空字符串，也是字符串

/* 对于变量，不仅值可以重复赋值，变量类型也可以不断改变
   JS的变量类型是自动检测的，而不是认为规定的
   因此，JS被称之为动态数据类型，或者叫弱类型语言 */
   
var a = 1;
a = "Hi";
console.log(typeof a); // string
```

## 8.2. +

加号+，我们已经很熟悉了，但是，在编程中，+号具有特殊的含义
> 当 + 两边都是数字的时候，表示**加号**

> 当 + 两边，至少一个不是数字的时候，标书**字符串连接符号**

```js
console.log(1+4) // 5
console.log("1"+4) // 14
console.log(1+"4") // 14
console.log(1+1+"4") // 24
```

# 9. 变量类型转换
## 9.1. string -> number

1. **parseInt** 

> 将string转换为一个整数，不四舍五入，直接截取整数部分

> 将任何进制的数字，转换成10进制

> 如果不能转换，则返回NaN

```js
parseInt(“123”)	//123
parseInt(“123.6”)	 //123
parseInt(“123年都会很爱你”)	 //123
parseInt(“123年11月”)		//123
parseInt(“123px”)		//123
parseInt(“-123.99999999”) //-123


parseInt('15',10); // 按10进制去解读'15'
parseInt('15',8); // 按8进制去解读‘15’
parseInt('15',16); // 按16进制去解读'15'
```

2. **parseFloat** 

> 尽量将一个string转换为浮点数
> 遇到第一个小数点，继续往后解析，遇到其它非数字则结束

3. 

## 9.2. number -> string

与任意string “相加”，结果一定是string，例如
```js
15 + "abc";
15 + "";
```

# 10. 基本数学运算

1. 双目运算符

需要两个值参加的运算

	\+ 加法/字符串连接
	\- 减法
	\* 乘法
	/  除法
	%  取余数/模运算
	** 幂运算

2. 赋值运算符

除了常见的 = 赋值运算符外，还有以下几种

	\+= 加等
		a += 1 相当于 a = a + 1
	\-= 减等
		a -= 1 相当于 a = a - 1
	\*= 乘等
		a *= 1 相当于 a = a * 1
	/=  除等
		a /= 1 相当于 a = a / 1
	%=  余等/模等
		a %= 1 相当于 a = a % 1
	**= 幂等
		a **= 2 相当于 a = a**2

3. 单目运算符

只需要一个数字就能进行的运算符

	+ 正号
	- 负号
	++ 递增
		相当于 +=1 的简写 
	-- 递减
		相当于 -=1 简写

# 探索一个问题
```js
var a = 0.2 + 0.1; // 请问 a 是多少 toFixed
```
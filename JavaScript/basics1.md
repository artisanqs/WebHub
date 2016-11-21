
>1.1
####如何插入JS

  >我们来看看如何写入JS代码？你只需一步操作,使用<script>标签在HTML网页中插入JavaScript代码。
注意， <script>标签要成对出现，并把JavaScript代码写在<script></script>之间。

  
1.2
####引用JS外部文件

  >我们可以把HTML文件和JS代码分开,并单独创建一个JavaScript文件(简称JS文件),其文件后缀通常为.js，然后将JS代码直接写在JS文件中。
注意:在JS文件中，不需要<script>标签,直接编写JavaScript代码就可以了。
JS文件不能直接运行，需嵌入到HTML文件中执行，我们需在HTML中添加如下代码，就可将JS文件嵌入HTML文件中。

<script src="script.js"></script>


1.3
####JS在页面中的位置

  我们可以将JavaScript代码放在html文件中任何位置，但是我们一般放在网页的head或者body部分。
放在<head>部分
最常用的方式是在页面中head部分放置<script>元素，浏览器解析head部分就会执行这个代码，然后才解析页面的其余部分。
放在<body>部分
JavaScript代码在网页读取到该语句的时候就会执行。

注意: javascript作为一种脚本语言可以放在html页面中任何位置，但是浏览器解释html时是按先后顺序的，所以前面的script就先被执行。
比如进行页面显示初始化的js必须放在head里面，因为初始化都要求提前进行（如给页面body设置css等）；
而如果是通过事件调用执行的function那么对位置没什么要求的。

1.4
####JavaScript-认识语句和符号

JavaScript语句是发给浏览器的命令。这些命令的作用是告诉浏览器要做的事情。

每一句JavaScript代码格式: 语句;

先来看看下面代码

<script type="text/javascript">
   alert("hello!");
</script>
例子中的alert("hello!");就是一个JavaScript语句。

一行的结束就被认定为语句的结束，通常在结尾加上一个分号";"来表示语句的结束。

看看下面这段代码,有三条语句，每句结束后都有";"，按顺序执行语句。

<script type="text/javascript">
   document.write("I");
   document.write("love");
   document.write("JavaScript");
</script>
注意:

1. “;”分号要在英文状态下输入，同样，JS中的代码和符号都要在英文状态下输入。

2. 虽然分号“;”也可以不写，但我们要养成编程的好习惯，记得在语句末尾写上分号。



1.5
####JavaScript-注释很重要

注释的作用是提高代码的可读性，帮助自己和别人阅读和理解你所编写的JavaScript代码，注释的内容不会在网页中显示。注释可分为单行注释与多行注释两种。

我们为了方便阅读，注释内容一般放到需要解释语句的结尾处或周围。

单行注释，在注释内容前加符号 “//”。

<script type="text/javascript">
  document.write("单行注释使用'//'");  // 我是注释，该语句功能在网页中输出内容
</script>
多行注释以"/*"开始，以"*/"结束。

<script type="text/javascript">
   document.write("多行注释使用/*注释内容*/");
   /*
    多行注释
    养成书写注释的良好习惯
   */
</script>


1.6
####JavaScript-什么是变量

定义变量使用关键字var,语法如下：

var 变量名
变量名可以任意取名，但要遵循命名规则:

    1.变量必须使用字母、下划线(_)或者美元符($)开始。

    2.然后可以使用任意多个英文字母、数字、下划线(_)或者美元符($)组成。

    3.不能使用JavaScript关键词与JavaScript保留字。

变量要先声明再赋值，如下：

var mychar;
mychar="javascript";
var mynum = 6;
变量可以重复赋值，如下：

var mychar;
mychar="javascript";
mychar="hello";
注意:

1. 在JS中区分大小写，如变量mychar与myChar是不一样的，表示是两个变量。

2. 变量虽然也可以不声明，直接使用，但不规范，需要先声明，后使用。


1.7
####JavaScript-判断语句（if...else）

if...else语句是在指定的条件成立时执行代码，在条件不成立时执行else后的代码。

语法:

if(条件)
{ 条件成立时执行的代码 }
else
{ 条件不成立时执行的代码 }
假设我们通过年龄来判断是否为成年人，如年龄大于等于18岁，是成年人，否则不是成年人。代码表示如下:

<script type="text/javascript">
   var myage = 18;
   if(myage>=18)  //myage>=18是判断条件
   { document.write("你是成年人。");}
   else  //否则年龄小于18
   { document.write("未满18岁，你不是成年人。");}
</script>

1.8

####JavaScript-什么是函数

  函数是完成某个特定功能的一组语句。如没有函数，完成任务可能需要五行、十行、甚至更多的代码。
这时我们就可以把完成特定功能的代码块放到一个函数里，直接调用这个函数，就省重复输入大量代码的麻烦。

如何定义一个函数呢？基本语法如下:

function 函数名()
{
     函数代码;
}
说明:

1. function定义函数的关键字。

2. "函数名"你为函数取的名字。

3. "函数代码"替换为完成特定功能的代码。

  我们来编写一个实现两数相加的简单函数,并给函数起个有意义的名字：“add2”，代码如下：
'
function add2(){
   var sum = 3 + 2;
   alert(sum);
}
'



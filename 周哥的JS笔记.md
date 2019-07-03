# javaScript基本语法

## 编程



​                <img src="./1/编程.png" alt="">

​                <img src="./1/计算机语言.png" alt="">

​                

<img src="./1/编程总结.png" alt="">

                ## javascript是什么



<img src="./1/什么是javascript.png" alt="">

​                <img src="./1/浏览器执行jspng.png" alt="">

​                <img src="./1/js的三部分.png" alt="">

​                <img src="./1/ECMA.png" alt="">

​                <img src="./1/DOMpng.png" alt="">

​                <img src="./1/BOM.png" alt="">

                ## JS三种书写位置

## 

<img src="./1/行内式js.png" alt="">

​                <img src="./1/内嵌js.png" alt="">

​                <img src="./1/外部js文件.png" alt="">

​                <h2>JS输入输出语句</h2>

​                <img src="./1/js输入输出语句.png" alt="">

##  变量



​                <img src="./1/什么是变量.png" alt="">

​                <img src="./1/变量的本质.png" alt="">

​                <img src="./1/更新变量.png" alt="">

​                <img src="./1/声明变量特殊情况.png" alt="">

##           变量命名规范      

<img src="./1/命名规范.png" alt="">

##   小结        

<img src="./1/变量小结.png" alt="">

#         数据类型

​                <img src="./1/为什么要数据类型转换.png" alt="">

​                <img src="./1/变量的数据类型.png" alt="">

##    基本数据类型

​                <img src="./1/基本数据类型.png" alt="">

###         数字型 Number        

<img src="./1/数字型进制.png" alt="">

​                <img src="./1/数字型范围.png" alt="">

​                <img src="./1/数字型特殊值.png" alt="">

​                <img src="./1/isNaN.png" alt="">

###      字符串型String           

<img src="./1/字符串型.png" alt="">

####              字符串转移符  

<img src="./1/字符串转移符.png" alt="">

​                <img src="./1/字符串长度.png" alt="">

​                <img src="./1/字符串拼接.png" alt="">

###    布尔型 Boole             

<img src="./1/布尔型.png" alt="">

###        undefined和null

<img src="./1/U和N.png" alt="">

###         数据类型转换

​        <img src="./1/数据类型转换.png" alt="">

####     转换字符串         

   <img src="./1/转换字符型.png" alt="">

​                <img src="./1/转换字符型代码.png" alt="">

####   转换数字型              

<img src="./1/转换数字型.png" alt="">

​                <img src="./1/转换数字型代码.png" alt="">

  

#### 转换布尔值          

  <img src="./1/转换布尔值.png" alt="">



# JS运算符

## 运算符

 <img src="./1/运算符.png">

## 算术运算符

 ```javascript
算术运算符有 +(加)  -（减） *（乘） /（除） %（取余）

example:
    <script>
        console.log(1 + 1);//2
        console.log(2 - 1);//1
        console.log(2 * 2);//4
        console.log(2 / 1);//2
		//取余
        console.log(2 % 2);//0
        console.log(3 % 5);//3
        console.log(5 % 3);//2
        //浮点数运算会有问题
        console.log(0.2 + 0.1);//0.30000000000000004
		
		var i =0.1 +0.2;
		consolt.log(i == 0.3);//false;
		//所以不要直接判断两个浮点数是否相等
    </script>
 ```



## 递增和递减运算符

> ```tex
> 概念： 如果需要反复给数字变量添加或减去1，可以用递增（++）和递减（--）运算符来完成。
>
> 注意：递增和递减运算符必须和变量配合使用。
>
> ```

```javascript
前置递增 ++i  先加1，后返回值

后置递增 i++  先返回值，后加1

例子：
	 var a=10;
        ++a; //++a 11 a=12
        var b= ++a + 2;//a=12 ++a 12 
        console.log(b);//14

        var c=10;
        c++; //c++ 10 c=11
        var d= c++ + 2; // c=11 c++ 11
        console.log(d);//13
        
        var e=10;
        var f= e++ + ++e;
        //   e++ 10 e=11  ++e 12 e=13 
        console.log(f);//22
```



## 比较运算符

<img src="./1/比较运算符.png">

## 逻辑运算符

```html
概念： 逻辑运算符是用来进行布尔值运算符的运算符，返回布尔值，多用于条件判断。

```

| 逻辑运算符 |                    说明                    |       案例        |
| :---: | :--------------------------------------: | :-------------: |
|  &&   | 与  两侧都为true  结果为true 。只要一边有false，结果为false |  true && false  |
| \|\|  | 或  两侧都为false 结果为false。只要一边有true，结果为true  | true \|\| false |
|   !   |                  非  取反                   |      !true      |

## 赋值运算符

```javascript
概念：  用来把数据赋值给变量的运算符。
```

| 赋值运算符     | 说明           | 案例                       |
| --------- | ------------ | ------------------------ |
| =         | 直接赋值         | var i= “我是谁”；            |
| +=  -=    | 加减一个数 后再赋值   | var age =10; age +=5//15 |
| *=、/=  %= | 乘 除 取余  后再赋值 | var age=2; age*=5;//10   |

## 运算符优先级

<img src="./1/运算符优先级.png">



# javascript流程控制--分支

## if语句

```javascript
语法：
	if(条件表达式){
      	执行语句;
	}else{
      	执行语句;
	}

例子：
        //弹出一个输入框，要求用户输入年龄，如果年龄大于等于18岁，允许进网吧！
        var age = parseInt(prompt("请输入你的年龄！"));
        if(age >= 18){
            document.write("欢迎来到MC的精神世界！");
        }else{
            document.write("滚回去，再吃几年奶再来！");
        }
	
		//	输入一个年份，判断是否闰年
        var age = parseInt(prompt("请输入你所在的年份！"));
        if((age %4 ==0 && age%100 == 0) || (age%400 == 0)){
            document.write(age+"年MC大门打开，欢迎来到MC！");
        }else{
            document.write(age+"年封印中。滚回去，再吃几年奶再来！");
        }
```

```javascript
语法：
	if(条件表达式){
      	执行语句;
	} else if{
      	执行语句;
	} else if{
      	执行语句;
	} else if{
      	执行语句;
	}else{
      	最后执行语句;
	}
例子：
	//输入一个分数 ,根据分数输出对应的的等级字母 A B C D E
        var couse = parseFloat(prompt("你毕业考试分数是______"));
        if (couse >= 90) {
            document.write("分数" + couse + "分\t评分为A");
        } else if (couse >= 80) {
            document.write("分数" + couse + "分\t评分为B");
        } else if (couse >= 70) {
            document.write("分数" + couse + "分\t评分为C");
        } else if (couse >= 60) {
            document.write("分数" + couse + "分\t评分为D");
        } else {
            document.write("分数" + couse + "分\t评分为E");
        }
```



## switch语句

```javascript
语法：
        switch (num) {
            case value:
                执行语句1；
                break;
        	.....
            default:
            执行最后的语句；
                break;
        	}
注意： 1.我们开发里面，表达式经常写成变量。
	  2.我们的 num值和case里面的值相匹配时是 全等 “===” num===1.
  	  3.break 如果当前的case里面没有break，则不会退出switch  是继续执行下一个case。
```

```javascript
举个栗子：
	用户输入一个水果，如果有该水果，则输出价格。反之，提示“没有该水果！”
    var fruit = prompt("输入水果");
        switch (fruit) {
            case "榴莲":
                document.write(fruit + "35块一斤");
                break;
            case "板栗":
                document.write(fruit + "不要买，小心你男（女）朋友给你跪板栗壳");
                break;
            default:
                document.write(fruit + "没有哦。亲");
                break;
        }
```

## switch语句和if else if语句的区别

```javascript
1.一般情况下，它们两个语句可以相互替换。
2.switch...case语句通常处理case为比较确定的情况，而if...else...语句更加灵活，常用语范围判断（大于、等于某些范围）。
3.switch语句进行条件判断后直接执行到程序的条件语句，效率更高。而if..else语句有几个条件，就得判断多少次。
4.当分支比较少时，if...else语句的执行效率比switch语句高。
5.当分支比较多时，switch语句执行效率比较高，而且结果清晰。
```



## 三元表达式

```javascript
概念： 有三元运算符组成的式子。
作用： 能做一些简单的条件选择。
```

```javascript
语法：条件表达式 ？表达式1：表达式2；
例子：
        var num = 10;
        var max = num > 5 ? 'YES' : 'NO';
        document.write(max);
		
		//输入数字，数字小于10，在前面补0，反之不用补0.
        var num = parseFloat(prompt("输入数字"));
        var max = num > 9 ? num : "0" + num;
       	document.write(max);
```

# 循环



## 循环的目的

```html
目的：在实际问题中，有许多具有规则性的重复操作，因此在程序中要完成这类操作就需要重复执行某次额语句。
```



## for循环

	语句：
	for(初始化变量；条件表达式；操作表达式){
	  循环体
	}
	举个例子：
	
	求1~100之间所有数的平均值
	
	var sum =0;
	    for(var i=1;i<=100;i++){
	        sum =sum +i;
	    }
	    document.write(sum);
	    
	    要求用户输入班级人数，之后依次输入每个学生的成绩，最后打印该班级总的成绩以及平均值
	    var num = parseFloat(prompt("输入人数！"));
	    var sum = 0;
	    var average = 0;
	    for (var i = 1; i <= num; i++) {
	        var scoue = parseFloat(prompt('第' + i + '位同学的成绩'));
	        sum = sum + scoue;
	    }
	    average = sum / num;
	    document.write("该班级" + num + '人，总成成绩' + sum + '分');
	    document.write('<br>');
	    document.write("该班级" + num + '人，平均成绩' + average + '分');


### 双重for 循环

```javascript
语句：
	for(初始化变量；条件表达式；操作表达式){
      for(初始化变量；条件表达式；操作表达式){
        循环体
      }
    }
```

```javascript
举个栗子：
 打印倒三角
        var str = '';
        for (var i = 1; i <= 9; i++) {
            for (var j = 9; j >= i; j--) {
                str = str + "☆";
            }
            str = str + '\n';
        }
        console.log(str);

  九九乘法表
        var str = '';
        for (var i = 1; i <= 9; i++) {
            for (var j = 1; j <= i; j++) {
                str = str + (i + 'x' + j + '=' + j * j)+'\t';
            }
            str = str + '\n\r';
        }
        console.log(str);
```

### 小结

```tex
for循环可以重复执行某些相同的代码
for循环可以重复执行某些许不同的代码，以为我们有计数器
for循环可以重复执行某些操作，比如算数运算符加法操作
随着需求增加，双重for循环可以做更多、更好看的效果
双重for循环，外层循环一次，内层for循环全部执行
for循环是循环条件和数字直接相关的循环
分析要比写代码更重要
一些核心算法想不到，但是要学会，分析它执行过程

```



## while循环

```javascript
语法：
while(条件表达式){
  循环体
}//执行思路 当条件表达式结果为true ,则执行循环体 否则，提出循环。

举个栗子：
var sre = prompt('你爱我吗');
	while(sre !== '我爱你'){
      sre = prompt('你爱我吗');
	}
alert('我也爱你');
```



## do while 循环

```javascript
语法：
do{
  循环体
}while(条件表达式)
  执行思路：跟while不同的地方在于 do whie先执行一次循环体，在判断条件，如果条件表达式为真，则继续执行循环体，否则退出循环。
  
  举个栗子：
  var i = ;
  do(
    console.log('I love you');
    i++
  )while(i<=)100)
    至少执行一次循环体
    
```



## while循环 和do while 循环的区别

```tex

```



## break 和 continue 的区别

```javascript
 continnue关键字用于立即跳出本次循环，继续下一次循环（本次循环体中continue之后的代码就会少执行一次。
 
 举个栗子：
 for(var i = 1 ;i<=5;i++){
   if(i==3){
     consloe.log("这个包子有毒，不要吃！")
     continue;//跳过本次循环，跳出的是第三次循环
   }
 }
```

```javascript
break关键字用于跳出整个循环（循环结束）。

 举个栗子：
 for(var i = 1 ;i<=5;i++){
   if(i==3){
     continue;//直接退出整个for循环，跳出整个for下面的语句
   }
   consloe.log('这个第'+i+"包子有毒，不要吃");
 }
```



# 数组

## 概念

```tex
数组可以把一组相关的数据一起存放，并提供方便的访问(获取）方式。 
数组是指一组数据的集合，其中的每个数据被称作元素，在数组中可以存放任意类型的元素。数组是一种将 一组数据存储在单个变量名下的优雅方式。 
```



## 创建数组

```javascript
方法一
用 new创建数组
	语法
    	var 数组名 = new Array();
举个栗子：
		var arr = new Array();//创建一个新的空数组
注意：Array,A要大写。

方法二
利用数组字面量创建数组
	语法
    	var 数组名 = [];//使用数组字面量方式创建空的数组。
		var 数组名 = [];//使用数组字面量方式创建带初始值得数组。
	举个栗子：
    	var arrStus = ['小白'，true,28.9];
```



## 获取数组中的元素

```javascript
索引(下标):用来访问数组元素的序号（数组下标从0开始）

var arr      = ['小白',小黑',小黄',瑞文','鱼尾纹'];
     索引号：    0       1    2    3      4
// 定义数组 
var arrStus = [1,2,3]; 
// 获取数组中的第2个元素 
alert(arrStus[1]);  
注意：如果访问时数组没有和索引值对应的元素，则得到的值是undeﬁned

```



## 遍历数组

```javascript
数组遍历: 把数组中的每个元素从头到尾都访问一次（类似学生的点名）。 

举个栗子：
var arr = ['red','green', 'blue']; 
for(var i = 0; i < arr.length; i++){
  console.log(arrStus[i]); 
}

数组的长度
	数组的长度：默认情况下表示数组中元素的个数
    使用“数组名.length”可以访问数组元素的数量（数组长度）
    举个栗子：
    var arrStus = [1,2,3]; alert(arrStus.length);  // 3
注意： 此处数组的长度是数组元素的个数 ，不要和数组的索引号混淆。 当我们数组里面的元素个数发生了变化，这个 length 属性跟着一起变化 数组的length属性可以被修改： 如果设置的length属性值大于数组的元素个数，则会在数组末尾出现空白元素； 如果设置的length属性值小于数组的元素个数，则会把超过该值的数组元素删除

```



## 数组中新增元素

```javascript
数组可以通过以下方式在数组的末尾插入新元素：
数组[数组.length] = 新数据
```



# 函数

## 概念

```javascript
虽然 for循环语句也能实现一些简单的重复操作，但是比较具有局限性，此时我们就可以使用 JS 中的函数。 
函数：就是封装了一段可被重复调用执行的代码块。通过此代码块可以实现大量代码的重复使用。
```



## 函数的使用

```javascript
语法：
    //声明函数
 function 函数名(){
   //函数体代码
 }
function 是声明函数的关键字,必须小写
由于函数一般是为了实现某个功能才定义的， 所以通常我们将函数名命名为动词，比如 getSum 

调用函数：
语法 函数名（）；

函数的封装：
函数的封装是把一个或者多个功能通过函数的方式封装起来，对外只提供一个简单的函数接口 
简单理解：封装类似于将电脑配件整合组装到机箱中 ( 类似快递打包） 
 举个栗子：
      /*    计算1-100之间值的函数 */ 
          // 声明函数
  function getSum(){ 
  var sumNum = 0;// 准备一个变量，保存数字和 
  for (var i = 1; i <= 100; i++) {
    sumNum += i;// 把每个数值 都累加 到变量中  
  }  
  alert(sumNum); 
} 
getSum()// 调用函数 getSum();                   
```



## 函数的参数

```javascript
形参：函数定义时设置接收调用时传入
实参：函数调用时传入小括号内的真实数据
参数的作用 : 在函数内部某些值不能固定，我们可以通过参数在调用函数时传递不同的值进去。 函数参数的运用

注意:在JavaScript中，形参的默认值是undeﬁned。
```

| 参数个数      | 说明                      |
| --------- | ----------------------- |
| 实参个等于形参个数 | 输出正确结果                  |
| 实参个多于形参个数 | 只取到形参的个数                |
| 实参个少于形参个数 | 多的形参定义为undefined,结果为NaN |

## 函数的返回值

```javascript
// 声明函数
function 函数名（）{
  ...   
  return  需要返回的值；
} // 调用函数 
函数名();    // 此时调用函数就可以得到函数体内return 后面的值

在使用 return 语句时，函数会停止执行，并返回指定的值 
如果函数没有 return ，返回的值是 undeﬁned 

break ,continue ,return 的区别

break ：结束当前的循环体（如 for、while） 
continue ：跳出本次循环，继续执行下次循环（如 for、while） 
return ：不仅可以退出循环，还能够返回 return 语句中的值，同时还可以结束当前的函数体内的代码 
```



## arguments的使用

```javascript
当不确定有多少个参数传递的时候，可以用 arguments 来获取。在 JavaScript 中，arguments实际上它是当前函数 的一个内置对象。所有函数都内置了一个 arguments 对象，arguments 对象中存储了传递的所有实参。

arguments展示形式是一个伪数组，因此可以进行遍历。伪数组具有以下特点：

具有 length 属性 
按索引方式储存数据
不具有数组的 push , pop 等方法 
注意：在函数内部使用该对象，用此对象获取函数调用时传的实参。 
```



## 函数的两种声明方法

自定义函数方式(命名函数) 
利用函数关键字 function 自定义函数方式

```javascript

// 声明定义方式 
function fn()
{...} 
// 调用   
fn();  
```

- 因为有名字，所以也被称为命名函数 
- 调用函数的代码既可以放到声明函数的前面，也可以放在声明函数的后面
- 函数表达式方式(匿名函数）

 利用函数表达式方式的写法如下:

```javascript
// 这是函数表达式写法，匿名函数后面跟分号结束
var fn = function(){...}；
// 调用的方式，函数调用必须写到函数体下面 
fn();

```

- 因为函数没有名字，所以也被称为匿名函数
- 这个fn 里面存储的是一个函数 
- 函数表达式方式原理跟声明变量方式是一致的
- 函数调用的代码必须写到函数体后面

利用函数表达式方式的写法如下：

```javascript
// 声明定义方式 
function fn() {...}
// 调用 
fn(); 
```

因为有名字，所以也被称为命名函数 调用函数的代码既可以放到声明函数的前面，也可以放在声明函数的后面

-  函数表达式方式(匿名函数）
-  自定义函数方式(命名函数)
-  利用函数关键字 function 自定义函数方式。
-  函数表达式方式(匿名函数）




# javascript作用域

## 作用域

作用域就是代码名字(变量)在某个范围内起作用和效果，目的是为了提高程序的可靠性更重要的是减少命名冲突

- 全局作用域

  ```javascript
  整个script标签，或者是一个单独JS文件。
  var num = 10;
  function fn(){
    。。。
  }
  ```

  ​

- 局部作用域（函数作用域）

  ```javascript
  在函数内部就是局部作用域，只在函数内部其效果和作用。
  function fn(){
    //局部作用域
  }
  ```

  ​

## 变量的作用域

JS中没有块级作用域  JS的作用域：全局作用域 局部作用域    **现阶段我们JS没有块级作用域**   在ES6的时候新增的快级作用域

## 作用域链

```javascript
只要是代码都一个作用域中，写在函数内部的局部作用域，未写在任何函数内部即在全局作用域中；如果函数中还有 函数，那么在这个作用域中就又可以诞生一个作用域；根据在**[内部函数可以访问外部函数变量]**的这种机制，用 链式查找决定哪些数据能被内部函数访问，就称作作用域链

举个栗子：

 function f1() {
   var num = 123;
   function f2() { 
     console.log( num ); 
   }  
   f2(); 
 }
var num = 456; f1();

```

```tex
作用域链：采取就近原则的方式来查找变量最终的值
```

```javascript
var a = 1;
function fn1() { 
  var a = 2;
  var b = '22'; 
  fn2();   
  function fn2() { 
    var a = 3;
    fn3(); 
    function fn3() {
      var a = 4; 
      console.log(a); //a的值 ?   
      console.log(b); //b的值 ? 
    } 
  }
}
fn1();
```

## 预解析

```tex
JavaScript 代码是由浏览器中的 JavaScript 解析器来执行的。JavaScript 解析器在运行 JavaScript 代码的时候分为两 步：预解析和代码执行
```

- 预解析：在当前作用域下, JS 代码执行之前，浏览器会默认把带有 var 和 function 声明的变量在内存中进行提 前声明或者定义。
- 代码执行： 从上到下执行JS语句。

 **预解析会把变量和函数的声明在代码执行之前执行完成。**

变量提升

```javascript
预解析也叫做变量、函数提升。
变量提升（变量预解析）： 变量的声明会被提升到当前作用域的最上面，变量的赋值不会提升

console.log(num);  // 结果是多少？
var num = 10;      // ？

结果：undeﬁned
 
注意：**变量提升只提升声明，不提升赋值**
```



函数提升

```javascript
函数提升： 函数的声明会被提升到当前作用域的最上面，但是不会调用函数。

fn();
function fn() {
  console.log('打印');
}

结果：控制台打印字符串 --- ”打印“ 
 
注意：函数声明代表函数整体，所以函数提升后，函数名代表整个函数，但是函数并没有被调用！
```

函数表达式声明函数问题

```javascript
函数表达式创建函数，会执行变量提升，此时接收函数的变量名无法正确的调用：

fn();
var  fn = function() {
  console.log('想不到吧'); 
}

结果：报错提示 ”fn is not a function"
 
解释：该段代码执行之前，会做变量声明提升，fn在提升之后的值是undeﬁned；而fn调用是在fn被赋值为函数体之 前，此时fn的值是undeﬁned，所以无法正确调用
```



# 对象

## 什么是对象

```tex
万事万物皆对象， 对象是一个具体的事物。

对象是由属性和方法组成的
属性：事物的特征
方法：事物的行为
```



## 创建对象的三种方式

### 变量 属性 函数 方法的区别

```javascript
1.变量和属性的相同之处：他们都是用来存储数据的。
变量： 单独声明并赋值 使用的时候直接写变量名 单独存在
属性：  在对象里面的不需要声明的，使用的时候必须是 对象 属性。

2.函数和方法的相同点：都是实现某种功能  做某件事。
函数是单独声明 并且调用的函数名（） 单独存在的。
方法 在对象里面 调用的时候 对象，方法()

```



### 利用字面量创建对象

```javascript
语法：
var obj = {
  属性名：属性值，
  属性名：属性值，
  属性名：属性值，
  ...
  属性名.方法名 =function (){
    
  }
...
} //创建一个空的对象

举个栗子：
        var obj = {
            name: '小高',
            sex: '男',
            age: 15,
            skill: function (name) {
                console.log(name + '人间大炮');

            }
        }
        console.log(obj.sex);//调用属性方法一
	    console.log(obj[sex]);//调用属性方法二
        obj.skill(obj.name);

```



### 利用new Object创建对象

```javascript
语法：
var obj = new Object(){
  obj.属性名=属性值;
  obj.属性名=属性值;
  ...
  obg.属性名=function(){
    ...
  }
    ...
}
    
举个栗子：
  var mingren = new Object();
        mingren.name = '鸣人';
        mingren.sex = '男';
        mingren.age = 19;
        mingren.skill = function () {
            console.log('隐分身术');

        }
        console.log(mingren.name);
        mingren.skill();
```



### 利用构造函数创建对象

**为什么需要使用构造函数**

因为我们前面两种方式一次只能创建一个对象，里面很多的属性和方法是大量相同的，我们只能复制。

因此我们可以利用函数的方式 重复这些相同的代码 我们就把这个函数称为 构造函数。

又因为这个函数不一样 里面封装的不是普通代码，而是 对象

**构造函数** 就是把我们**对象**里面相同的属性和方法抽象出来封装到函数里面。

```javascript
       function Star(name,type,blood,attack){
            this.name = name;
            this.type = type;
            this.blood = blood;
            this.attack = attack;
            this.skill = function(q,w,e,r){
                console.log(this.name +'Q技能是'+q);
                console.log(this.name +'W技能是'+w);
                console.log(this.name +'E技能是'+e);
                console.log(this.name +'R技能是'+r);

            }
        }

        var lp= new Star('剑圣','刺客','500血量','近战');
        console.log(lp.name);
        lp.skill('阿尔法突袭','冥想','普攻强化','高原血统');
        var lks= new Star('拉克丝','辅助、中单','500血量','远程');
        console.log(lks.name);
        lks.skill('光环控制','光之护盾','旋涡','元素喷射');
注意：1.构造函数名字首字母要大写
	 2.我们构造函数不需要return 就可以返回结果。
     3.我们调用构造函数，必须使用new。
     4.只要我们调用 new Star()就创建一个对象 lp
     5.我们的属性和方法前面必须添加 this。
```

**构造函数和对象**

**构造函数：** 抽象 了对象的公共部分，封装到了函数里面，它泛指某一大类（class）

**创建对象：**特指某一个，通过new关键字创建对象的构成我们也称为对象实例化。

## new 关键字 

1. 在内存中创建一个新的空对象。
2. 让this指向这个新的对象。
3. 执行工作函数里面的代码，给这个新对象添加属性和方法。
4. 返回这个新对象（所以构造函数里面不需要return）。

## 遍历对象属性

```javascript
for...in语句对数组或者对象的属性进行循环操作。

//遍历对象
var obj = {
  name :'小邓 ',
  age: 18,
  sex:'男'
}

//for(变量 in 对象){}
for(var k in obj){
   console.log(k);
   console.log(obj[k]);
}


```

# 内置对象

## 内置对象

javascript中的对象分3种:自定义对象、内置对象。

内置对象就是指JS语言自带的一些对象，这些对象供开发者使用，并提供了一些常用的或是最基本而必要的功能(属性和方法)。

优点：快速开发。

## Math对象

```javascript

利用对象封装自己的数学对象，里面有PI 最大值 最小值。
var myMath={
            PI:3.141592653,
            max:function(){
                var max = arguments[0];
                for(var i =1;i<arguments.length;i++){
                    if(arguments[i]>max){
                        max = arguments[i];
                    }
                }
                return max;
            },
            min:function(){
                var min = arguments[0];
                for(var i =1;i<arguments.length;i++){
                    if(arguments[i]<min){
                        min = arguments[i];
                    }
                }
                return min;
            }
        }
        console.log(myMath.PI);
        console.log(myMath.max(1,6,99,88));
        console.log(myMath.min(1,6,99,88));
```

| Math.PI               | 圆周率                    |
| --------------------- | ---------------------- |
| MAath.floor()         | 向下取整                   |
| Math.ceil()           | 向上取整                   |
| Math.round()          | 四舍五入 就近取整 注意-3.5  结果-3 |
| Math.abs()            | 绝对值                    |
| Math.max()/Math.min() | 求最大值/最小值               |

**随机数**Math.random()

```javascript
//想要得到两个数之间的随机整数 并且 包含这两个数  可以理解为数学里的 [min , max]
        function getRandom(min, max) {
            return Math.floor(Math.random() * (max - min + 1) + min);
        }
        console.log(getRandom(1,8));


举个栗子：
  function getRandom(min, max) {
            return Math.floor(Math.random() * (max - min + 1) + min);
        }
        console.log(getRandom(1, 8));

        var arr = ['1', '2', '3', '4', '5', '6', '7'];
        console.log(arr[getRandom(0, 6)]);
```



## 日期Date对象

Date()日期对象 ：是一个工作函数，必须new来调用创建我们的Date()

```javascript
语法：
var  date = new Date();//创建一个时间对象,返回当前时间
console.log(date);

var date1 = new Date(2019,10,1);
console.log(date1);//返回的是11月不是10月
```

| 方法名           | 说明              | 代码                |
| ------------- | --------------- | ----------------- |
| getFullYear() | 获取当年            | obg.getFullYear() |
| getMonth()    | 获取当月（0-11）      | obg.getMonth())   |
| getDate()     | 获取当天日期          | obg.getDate()     |
| getDay()      | 或取消星期几（周日0到周六6） | obg.getDay()      |
| getHours()    | 获取当前小时          | obg.getHours()    |
| getMinutes()  | 获取当前分钟          | obg.getMinutes()  |
| getSdeonds()  | 获取当前秒钟          | obg.getSdeonds()  |

**获取日期的总的毫秒形式**

```javascript
//方法一： 通过valueOf()  getTime()
        var date = new Date();
        console.log(date.valueOf());//就是我们现在时间距离1970.1.1总的毫秒数
        console.log(date.getTime());
//方法二： 
        var date1 = +new Date(); //+new Date() 返回的就是总的毫秒数
        console.log(date1);
//方法三 H5 新增的
        console.log(Date.now());
        
```

```javascript
举个栗子：
        获取现在距离2018年8月8号有多少天,小时,分钟

        function countDay(time) {
            var nowTime = +new Date();//返回当前总毫秒数
            var inputTime = +new Date(time);//返回输入的时间总毫秒数
            var times = (nowTime - inputTime) / 1000; //当前时间和输入时间之差的秒数
            var d = parseInt(times / 60 / 60 / 24);//天
            d = d < 10 ? '0' + d : d;
            var h = parseInt(times / 60 / 60 % 24);//时
            h = h < 10 ? '0' + h : h;
            var m = parseInt(times / 60 % 60);//分
            m = m < 10 ? '0' + m : m;
            return d + '天' + h + '时' + m + '分';
        }
        console.log(countDay('2018-8-8'));
        var date = new Date();
        console.log(date);
```



## 数组对象

**创建数组对象的两种方法**

1. 字面量方法

2. new Array()

   ```javascript
   		//利用数组字面量
           var  arr = [1,2,3];
           console.log(arr[0]);
           
           //利用new Array()
           //var arr1 = new Array();//创建一个空数组
           var  arr1 = new Array(2); 
           console.log(arr1);//返回的是长度为2
           var arr2 = new Array(2,3);
           console.log(arr2);//等价于[2,3]
   ```

   ### **翻转数组reverse()**

   ```javascript
    方法一	
   		var arr = [1,2,3,5,6,7,89,0,];
           console.log(arr.reverse());

   方法二
           var arr = [1, 2, 3, 5, 6, 7, 89, 0,];
           var newArr = [];
           console.log(arr.length);
           
           for (var i = arr.length; i > 0; i--) {
               newArr[newArr.length] = arr[i];
           }
           console.log(newArr);

   //检测是否为数组
       (1) instanceof 运算符 他可以用来检测是否为数组
           var arr =[];
           var arr1 = {}
           console.log(arr instanceof Array);//返回 true
           console.log(arr1 instanceof Array);//返回 false
   	(2) Array.isArray(参数)；
           console.log(Array.isArray(arr));//返回true
           console.log(Array.isArray(arr1));//返回false
   ```

   ### **添加删除数组元素的方法**

   | 方法名             | 说明                     | 返回值        |
   | --------------- | ---------------------- | ---------- |
   | push(参数1...)    | 末尾添加一个或多个元素            | 并返回新的长度    |
   | unshift(参数1...) | 向数组开头添加一个或多个           | 并返回新的长度    |
   | pop()           | 删除数组最后一个元素，把数组长度减1 无参数 | 返回它删除的元素的值 |
   | shift()         | 删除数组的第一个元素，把数组长度减1 无参数 | 返回第一个元素的值  |

### **数组排序**

```javascript
sort()数组

      var arr = [1,2,3,5,6,7,89,0,];
        arr.sort(
            function(a,b){
                return a - b;//升序的顺序排版
                // return b- a;//降序的顺序排版
            }
        )
        console.log(arr);
```

### **数组索引方法**

| 方法名           | 说明              | 返回值                  |
| ------------- | --------------- | -------------------- |
| indexOf()     | 数组中查找给定元素的第一个索引 | 如果存在返回索引号，如果不存在返回-1. |
| lasrIndexOf() | 在数组中的最后一个的索引    | 如果存在返回索引号，如果不存在返回-1. |

```javascript
返回数组元素索引号方法
他只返回第一个满足条件的索引号
var arr ['2','6','jovjop','6'];
console.log(arr.indexOf('6'));
```

```javascript
数组去重
方法一：
        var arr = ['c','a','z','a','x','a','x','c'];
        var newArr =[];
        for(var i=0;i<arr.length;i++){
            if(newArr.indexOf(arr[i]) ===-1){
                newArr[newArr.length]=arr[i];

            }

        }
        console.log(newArr);

            
方法二：
	函数封装
        function uninr(arr) {

            var newArr = [];
            for (var i = 0; i < arr.length; i++) {
                if (newArr.indexOf(arr[i]) === -1) {
                    newArr.push(arr[i]);
                }
            }
            return newArr;
        }
        var deom = uninr(['a', 'g', 'r', 't', 'a', 't']);
        console.log(deom);
```

### **数组转换为字符串**

| 方法名         | 说明                    | 返回值     |
| ----------- | --------------------- | ------- |
| toString()  | 把数组转换成字符串，逗号分隔每一项     | 返回一个字符串 |
| join('分隔符') | 方法用于把数组中的所用元素转换为一个字符串 | 返回一个字符串 |



## 字符串对象

### 基本包装类型

基本包装类型，就是把简单数据类型，包装成为了复杂数据类型。这样基本数据类型就有了属性和方法。

**步骤**

```javascript
1.把简单数据类型包装成为复杂数据类型
var temp =new String('andy');
2.把临时变量的值给str。
str = temp;
3.销毁这个临时变量。
temp =null;
```

字符串的不可变

虽然看上去可以改变内容，其实是地址变了，内容中新开辟了一个内存空间。 



### 根据字符返回位置

```javascript
//查找字符串'bdjknscpsdmvpsmasjopnvaiwp'中所有的m出现的位置以及次数.
        var arr = 'bdjknscpsdmvpsmasjopnvaiwp';
        var index = arr.indexOf('m');
        // console.log(index);
        var num = 0;
        while (index !== -1) {
            console.log(index);
            num++;
            index = arr.indexOf('m', index + 1);
        }
        console.log(num+'次');
```



```javascript
举个例子：
['red','blue','red','green','pink','red']，求red出现的位置和次数。
        
var arr = ['red', 'blue', 'red', 'green', 'pink', 'red'];
        var index = arr.indexOf('red');
        var num = 0;

        // console.log(index);
        while (index !== -1) {
            console.log(index);
            num++;
            index = arr.indexOf('red', index + 1);

        }
        console.log("red的次数为"+num+'次');

```

```javascript
举个例子：
	查出["c", "a", "z", "a", "x", "a"]中每个元素出现的次数。
        var arr = ["c", "a", "z", "a", "x", "a"];
        var o = {};// c:1 a:3 z:1 x:1
        for (var i = 0; i < arr.length; i++) {
            var item = arr[i];
            if (o[item]) {
                o[item] = o[item] + 1;
            } else {
                o[item] = 1;
            }
        }
        console.log(o);

```

### 根据位置返回字符（重点）

| 方法名               | 说明                         | 使用                     |
| ----------------- | -------------------------- | ---------------------- |
| charAt(index)     | 返回指定位置的字符(index字符串的索引号)    | str.charAt(o)          |
| charCodeAt(index) | 获取指定位置处字符的ASCII码(index索引号) | str.charCodeAt(o)      |
| str[index]        | 获取指定位置处字符                  | HTML5、IE8支持和charAt()等效 |



charAt()根据位置返回字符

```javascript
var str = 'andy';
console.log(str.charAt(3));//打印索引为3的字符
//遍历所有的字符
for(var i = 0;i<arr.length;i++){
  console.log(str.charAt(i));
}
```

charCodeAt(index)返回相应索引号的字符ASCII值 目的：判断用户按下哪个键。

```javascript
console.log(str.charCodeAt(0));//97
```

str[index] H5新增

```javascript
console.log(str[0]);//a
```



```javascript
查找字符串'bdjknscpsdmvpsmasjopnvaiwp'中所有的出现的次数和最大的次数。
        var arr = 'bdjknscpsdmvpsmasjopnvaiwp';
        var newArr = {};//创建一个空对象。
        for (var i = 0; i < arr.length; i++) {//遍历arr
            var newchar = arr.charAt(i); //newChar是字符串的每一个字符
            if (newArr[newchar]) {//newArr[newChar]得到的是属性值
                newArr[newchar]++;
            } else {
                newArr[newchar] = 1;
            }
        }
        console.log(newArr);

  var max =0;//求最大的次数
        for(var k in newArr){
           
            if(newArr[k]>max){
                max =newArr[k];
            }
        }
        console.log(max);
```



### 字符串操作方法(重点)

| 方法名                       | 说明                                       |
| ------------------------- | ---------------------------------------- |
| concat(str1,str2,str3...) | concat()方法用于连接两个或者多个字符串。拼接字符串，等效于+,+更常用。 |
| substr(start,length)      | 从start位置开始(索引号)，length取的个数 重点记住这个。       |
| slice(start,end)          | 从start位置开始，截取到end位置，end取不到(他们都是索引号)      |
| substring(start,end)      | 从start位置开始，截取到end位置，end取不到基本和slice相同，但是不接受负值。 |



## 简单数据类型和复杂数据类型



### 简单数据类型

​    简单类型（基本数据类型、值类型）：在存储时变量中存储的是值本身，包括string ，number，boolean， undeﬁned，null 

### 复杂数据类型

  复杂数据类型（引用类型）：在存储时变量中存储的仅仅是地址（引用），通过 new 关键字创建的对象（系统对 象、自定义对象），如 Object、Array、Date等； 

### 堆栈

**堆栈空间分配区别：**
  1、栈（操作系统）：由操作系统自动分配释放存放函数的参数值、局部变量的值等。其操作方式类似于数据 结构中的栈；
简单数据类型存放到栈里面
  2、堆（操作系统）：存储复杂类型(对象)，一般由程序员分配释放，若程序员不释放，由垃圾回收机制回收

**简单数据类型的存储方式** 

值类型变量的数据直接存放在变量（栈空间）中

**复杂数据类型的存储方式**

 引用类型变量（栈空间）里存放的是地址，真正的对象实例存放在堆空间中

###  简单类型传参 

 函数的形参也可以看做是一个变量，当我们把一个值类型变量作为参数传给函数的形参时，其实是把变量在栈空间 里的值复制了一份给形参，那么在方法内部对形参做任何修改，都不会影响到的外部变量。

###  复杂数据类型传参 

 函数的形参也可以看做是一个变量，当我们把引用类型变量传给形参时，其实是把变量在栈空间里保存的堆地址复 制给了形参，形参和实参其实保存的是同一个堆地址，所以操作的是同一个对象。





































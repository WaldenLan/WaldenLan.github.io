## JavaScript

* Basic Info

- ECMAScript: 一种js标准
- 浏览器所支持的js版本在浏览器被开发出来的时候就已经确认了
- 由于浏览器的安全限制，以file://开头的地址无法执行如联网等js代码，还是需要架设一个Web服务器，然后以http://开头的地址来正常执行所有JavaScript代码。

* Things need to pay attention:

- 由于JavaScript这个设计缺陷，不要使用==比较，始终坚持使用===比较。[Compare without data type casting]
- 唯一能判断NaN的方法是通过isNaN()函数
- 浮点数在运算过程中会产生误差，因为计算机无法精确表示无限循环小数。要比较两个浮点数是否相等，只能计算它们之差的绝对值，看是否小于某个阈值
- JavaScript的设计者希望用null表示一个空的值，而undefined表示值未定义。事实证明，这并没有什么卵用，区分两者的意义不大。大多数情况下，我们都应该用null。undefined仅仅在判断函数参数是否传递的情况下有用。
- 这种变量本身类型不固定的语言称之为动态语言，与之对应的是静态语言。静态语言在定义变量时必须指定变量类型，如果赋值的时候类型不匹配，就会报错。
- JavaScript在设计之初，为了方便初学者学习，并不强制要求用var申明变量。这个设计错误带来了严重的后果：如果一个变量没有通过var申明就被使用，那么该变量就自动被申明为全局变量。
    + 启用strict模式的方法是在JavaScript代码的第一行写上：'use strict';
- ASCII字符可以以\x##形式的十六进制表示，例如：'\x41'; // 完全等同于 'A'
- 由于多行字符串用\n写起来比较费事，所以最新的ES6标准新增了一种多行字符串的表示方法，用` ... `表示
- undefined 超出范围的索引不会报错，但一律返回undefined
- 需要特别注意的是，字符串是不可变的，如果对字符串的某个索引赋值，不会有任何错误，但是，也没有任何效果
    + JavaScript为字符串提供了一些常用方法，注意，调用这些方法本身不会改变原有字符串的内容，而是返回一个新字符串
- 请注意，直接给Array的length赋一个新的值会导致Array大小的变化
- 请注意，如果通过索引赋值时，索引超过了范围，同样会引起Array大小的变化
    

## Reference:

* http://www.liaoxuefeng.com/wiki/001434446689867b27157e896e74d51a89c25cc8b43bdb3000
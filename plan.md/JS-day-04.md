# 第四天任务：函数基础，写代码最重要的封装手段，学会以后不用重复粘贴代码

## 任务一：什么是函数，函数的声明，调用

- 函数是打包好的一段代码，想用的时候直接调用，无需重复复制粘贴代码

```js
//定义函数（制作工具箱）
function 函数名（）{
    //里面写要执行的代码
}
//调用函数（使用工具箱）
函数名（）；
```

代码

```js
//定义一个打招呼的函数
function sayHello(){
  console.log("你好，我叫黄磊，我正在学习JavaScript，今天是第四天了")；
}

//调用函数，执行里面的代码
sayHello();
//想执行几次，就调用几次
sayHello();
sayHello();
```

## 任务2：行参，实参

- 工具箱可以接受从外部传入的数据，传入的数据叫实参，函数内部接受数据的变量叫形参；

```js
// num1 num2 就是形式参数，占位置用的变量
function getSum(num1,num2){
    console.log(num1 + num2);
}

//10,20 是实参，传递给函数内部
getSum(10,20);
getSum(50,30);
getSum(100,200);
```

执行结果：30，80,100；

形参=预留空位
实参=你实际塞进去的价值

## 任务三 return 返回值

函数内部算出结果，用return把结果送出去外面可以接住这个结果继续使用
没有return的函数，默认返回undefined.

- 一旦执行return，当前函数立刻终止，return后面代码不会运行！

```js
function getSum(num1,num2){
    //把计算结果返回出去
    return  num1 + num2；
    console.log("这行代码永远不会执行");
} 
    //定义变量接受函数返回的结果
    let result = getSum(12,8);
    console.log(result);//20
    
    //拿到结果还能继续运算
    console.log(result * 2);
```

## 任务四：变量作用域

变量有作用范围，不是在哪都可以访问

1. 全局变量：函数外面定义，所有地方都可以读取

2. 局部变量：函数{}内部定义 只能在函数内部使用，外面访问直接报错

```js
// 全局变量
let message = "这是全局变量"

function test(){
  console.log(num);// 内部可以读取全局变量

  //局部变量
  let num = 666；
  console.log(num);
}

test();
//console.log(num);//取消注释直接爆错！外部拿不到局部变量； 
```

## 任务5: 匿名函数

- 没有名字的函数叫做匿名函数

```js
//把匿名函数赋值给变量
let fn = function（）{
    
}
```
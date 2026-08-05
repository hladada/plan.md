# 运算符 + 条件判断 if/else + 三元表达式

## 任务一：算数运算符：（加减乘除，取余 自增 自减）

```JS
//算数运算符
let a=10；
let b=3；
console.log(a + b);
console.log(a - b);
console.log(a * b);
console.log(a / b);
console.log(a % b);//取余数

//自增 ++
let num = 5；
console.log(num++);//后置自增先输出，再加一
console.log(num)；

let num2 = 5；
console.log(++num2);//前置自增,先加一，再输出
```

## 任务二: 赋值运算符=+=-=*=/=%=

```js
let n = 10;
n += 5; //等价n = n + 5
console.log(n);
n -=3;
console.log(n);
n *=4;
console.log(n);
n %=4;
console.log(n);
```

## 任务三：运算比较符

```js
console.log(10 > 5);
console.log(10 < 5);
console.log(10 >= 5);
console.log(10 == "10");//宽松相等，只对比值，自动更换类型
console.log(10 ==="10");//严格相等，值加类型全部一致才true
console.log(10 != "10");
console.log(10 !== 5);
```

## 任务四:逻辑运算符&&||！

```js
let age = 20;
//&& 并且 两边都为true才为true
console.log(age > 18 && age <30);
//||或者 任意一边为true就为true 
console.log(age < 10 || age > 18);
//!取反
console.log(!true);
console.log(!false);
```

## 任务五：if/else if/else 条件分支

```js
let score = 85;
if (score >= 90){
    console.log("优秀")；
}else if (score >= 70);{
    console.log("良好")；
}else if (score >= 60);{
    console.log("及格")；
}else {
    console.log("不及格")；
}
```

## 任务六：三元运算符号(if简写)

语法:条件？满足执行 ：不满足执行

```js
let age = 19;
let res = age >= 18? "成年"："未成年"；
console.log(res);
``` 
# 基础语法

## 任务一：认识JS的三种引入方式输入自己的名字

### JS想在网页运行有三种写法

1. 行内JS：直接嵌在HTML标签里面

2. 内部JS：页面里写`<script>`代码`</script>`,最常用初学写法

3. 外部JS：单独新建.JS文件，页面引入，企业标准开发写法

- 行内JS代码示例

```html
<!DOCTPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <title>内部JS</title>
</head>
<body>
    <!--点击按钮弹出名字-->
    <button onclick="alert('黄磊')">
</body>
</html>
```

- 内部JS示例

```html
<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <title>内部JS</title>
</head>
<body>
    <script>
        // 控制台打印姓名，f12打开浏览器控制台查看
        console.log（"黄磊"）
    </script>
</body>
</html>
```

- 外部JS示例

1. 新建文件 ：`test.js`，里面只写一行代码 

```javascript
console.log("黄磊")
```

2. HTML文件引入这个js文件

```html
<!DOCTPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
</head>
<body>
    <!--src填写js文件路径，两个文件放同一个文件夹-->
    <script src="test.js"></script>
</body>
</html>
```

## 任务二:控制台三种输出语句的练习

学会在控制台打印不同样式的信息，调试代码必备工具，日常写代码全靠控制台查看结果

1. 修改内嵌script标签的代码

把页面中内嵌的`<scrippt>`内容全部换成下面代码

```javascript
//普通日志：常规打印内容，黑色文字，最常用
console.log("这是普通正常输出日志")

//警告日志：黄色背景感叹号，用来提醒风险，注意事项
console.warn("这是警告提示文字")

//错误信息：红色报错样式，代码出错时都会这样展示
console.error("这是错误报错样式")
```

2. 操作步骤

2.1. 保存HTML文件，刷新浏览器页面

2.2. 按下f12打开控制台

2.3. 依次观察三种文字颜色，图标区别：

- log
- warn
- error

你还可以打印数字，文字混合内容：

```javascript
console.log(666);
console.log("黄磊学习JS的第一天");
```

## 任务四：变量声明

1. let：声明可以修改的变量，日常开发首选
2. const：声明常量，一旦赋值不允许更改
3. var:旧语法，存在缺陷，了解即可，新项目尽量不用

操作步骤

修改你的main.js(外部js文件，推荐在这里练习)，清空所有源代码

```javascript
//1.let 可变变量
let username = "黄磊"；
console.log(username);
//  修改变量值
username = "全栈学习者"
console.log(username);

//2.conset常量
conset age = 22;
console.log(age);
//取消下面注释运行，会直接报错！const不能重新赋值
//age=22;

//3.var 旧方式
var adress = "安徽潜山";
console.log(address);
address = "江苏昆山";
console.log(address);    
```

操作流程：

1. 保存文件，刷新网页，按f12控制台

2. 正常情况下，打印：

```plaintext
黄磊
全栈学习者
22
安徽潜山
江苏昆山
```

3.  把//age=22注释去掉观察控制台出现红色报错

## 任务五 ： JS基础数据类型+typeof判断类型

JS常用的类型：

1. string 字符串(文字用双引号包裹)

2. number 数字

3. boolean 布尔值（只有有true和false）

4. underfined 未定义（变量声明但是没有赋值）

5. null 空值

6. object 对象

typeof：用来检测变量是什么类型。

清空main.js
粘贴代码：

```javascript
//1.字符串.string
let str = "学习JS";
console.log(str,typeof str);

//2.数字number
let num = 99.9;
console.log(num,typeof num);

//3.布尔 boolean
let flag = true；
console.log（flag，typeof flag）;

//4.undefined
let a;
console.log(a,typeof a);

//5.null
let empty = null;
console.log(empty,typeof empty);

//6.object 对象
let person = {
    name："张三"
    age：20
}；
console.log(person,typeof person);
```
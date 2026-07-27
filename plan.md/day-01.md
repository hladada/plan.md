# CCS学习笔记

## 任务一 ：创建基础 HTML 骨架页面

```html
<!DOCTYPE html>
<head>
    <meta charset="UTF-8">
    <title>CSS第一天练习</title>
</head>
<body>
    <h1>学习CSS</h1>
    <p>第一段文字</p>
    <p>第二段文字</p>
    <div>盒子内容</div>
</body>
</html>
```

1. 保存文件
2. 右键文件，Open with live sever，浏览器打开页面，现在页面默认只有黑色，没有任何样式，现在用三种不同的方式添加CSS样式

## 任务二 ：第一种方式：行内样式

- 直接写在标签里面`style="样式属性；值；"`,优先级最高，缺点：复用性差，工作中几乎不用，仅做了解即可

- 修改代码：

```html
<body>
    <!-- 行内样式：修改文字颜色为红色，字号为24px -->
    <h1 style = "color : red; font-size: 24px; ">学习CSS</h1>
    <p>第一段文字</p>
    <p>第二段文字</p>
    <div>盒子内容</div>
</body>
```

- 刷新浏览器：大标题变成红色

## 任务三 ： 第二种方式：内嵌样式

- 写在`<head>`标签里的`<style>`标签中，当前页面生效，多个标签统一改样式，适合单页面小案例。

完整代码替换：

```html
<!DOCTYPE html>
<head>
    <meta charset="UTF-8">
    <title>CSS第一天练习</title>
    <!-- 内部样式表区域 -->
    <style>
    /* 选中所有p标签，设置文字蓝，字号18px.*/
    p{
        color;blue;
        font-size: 18px;
    }
    </style>
</head>
<body>
    <h1>学习CSS</h1>
    <p>第一段文字</p>
    <p>第二段文字</p>
    <div>盒子内容</div>
</body>
</html>
```

## 任务四 ： 第三种方式 ：外部样式表

- 项目开发唯一推荐写法：CSS单独放到.css文件，HTML引入外部文件

- 步骤：

1. 在`week-css`文件夹新建文件`style.css`
2. css文件中写入代码：

```css
/*选中div标签*/
div {
    color ：green
    font- size：20px；
}
```

3. 在HTML的head中，用<link>标签引入这个css文件

```html
<link rel="stylesheet" href="style.css">
```

完整的HTML代码

```html
<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <title>CSS第一天练习</title>
    <!-- 引入外部CSS文件 -->
    <link rel="stylesheet" href="style.css">

    <style>
        p {
            color: blue;
            font-size: 18px;
        }
    </style>
</head>
<body>
    <h1 style="color: red; font-size: 24px;">学习CSS</h1>
    <p>第一段文字内容</p>
    <p>第二段文字内容</p>
    <div>盒子内容</div>
</body>
</html>
```

- 刷新看效果
h1 红，p 蓝， div 绿

## 任务五 ：四大基础选择器

所有样式均在`style.css`里练习

1. 通配符选择器*

- 作用：选中页面所有标签，一般用来清除内外边距
css 添加：

```css

/* 通配符 */
*{
    font-family:"微软雅黑"；/*统一全部页面字体*/

}
```

2. 标签选择器

之前写的 p{} div{} h1{}都属于标签选择器，选中页面所有同名标签

3. class类选择器

```html
<h1 style="color: red; font-size: 24px;">学习CSS</h1>
<p class="txt">第一段文字内容</p>
<p class="txt">第二段文字内容</p>
<div class="box">盒子内容</div>
```
css写入

```css
/* 类选择器 */
.txt {
    text-align: center; /* 文字居中 */
}
.box {
    background-color: #eee; /* 背景浅灰色 */
    padding: 10px;
}
```
4.id选择器

HTML：
HTML 写 id="名称"，css 用 #id名 选中，一个页面 id 只能出现一次

`<p id="only">独一无二的段落</p>`

css：

```css
#only {
    color: orange;
}
```
写完刷新页面，挨个看页面变化


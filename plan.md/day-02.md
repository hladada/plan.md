# 今日任务

## 任务一 ： 沿用day-01 文件

### 1.在week1-css文件夹里新建文件夹： day2.HTML

### 2.写入HTML基础骨架：

```html
<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <title>Day2 CSS文字样式</title>
    <!-- 引入外部css文件 -->
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <div class= "text-box">
        <h2>css文字样式联系标题</h2>
        <p class="para1">第一段测试文字：学习前端循序渐进最重要</p>
        <p class="para2">第二段测试文字：今天练习字体，字号，行高，文字对齐</p>
    </div>
</body>
</html>
```

### 同目录新建样式文件：`style.css`

### 右键HTML文件，live sever打开浏览器，空白样式页面准备完毕
完成标记；页面正常打开，无样式

## 任务二 ： 字体属性基础

1. 在是style.css写入代码

```css
/* 全局统一字体 */
* {
    font-family: "Microsoft Yahei", SimSun, sans-serif;
}
```

2. 刷新浏览器查看文字变化

- Microsoft Yahei：微软雅黑

- SimSun：宋体

- sans-serif：无衬线通用字体

## 任务三 ： 任务 3：字号 font-size + 文字颜色 color

1. 字号设置 px 像素单位

```css
h2 {
    font-size: 30px;
}
.para1 {
    font-size: 18px;
}
.para2 {
    font-size: 16px;
}
```

2. 文字颜色三种写法

```css
h2 {
    font-size: 30px;
    color: #222; /* 十六进制颜色（最常用） */
}
.para1 {
    font-size: 18px;
    color: rgb(20, 120, 200); /* rgb色值 */
}
.para2 {
    font-size: 16px;
    color: darkgreen; /* 颜色英文单词 */
}
```

刷新页面观察三段文字大小、颜色全部区分开。

## 任务 4：文字粗细 font-weight

控制文字加粗 / 常规粗细，常用取值：

- normal：正常粗细（默认）
- bold：加粗
- 数字：100~900，400=normal，700=bold

```css
h2 {
    font-size: 30px;
    color: #222;
    font-weight: 700; /* 加粗标题 */
}
.para1 {
    font-size: 18px;
    color: rgb(20, 120, 200);
    font-weight: 400; /* 常规不加粗 */
}
```

## 任务 5：文字对齐 text-align（水平居中 / 左对齐 / 右对齐）

可选值：left 默认左对齐、center 居中、right 右对齐

```css
.text-box {
    width: 600px; /* 给盒子设置宽度，才能看出对齐效果 */
    margin: 0 auto; /* 盒子整体页面居中 */
}
h2 {
    text-align: center; /* 标题文字居中 */
}
.para2 {
    text-align: right; /* 第二段文字靠右排列 */
}
```

- 刷新页面直观看到排版差异。

## 任务 6：行高 line-height

- 行高：一行文字占据的整体高度，文字在行高中默认垂直居中

```css
.para1 {
    font-size: 18px;
    color: rgb(20, 120, 200);
    font-weight: 400;
    line-height: 1.8; /* 行高=字号1.8倍*/
}
.para2 {
    font-size: 16px;
    color: darkgreen;
    text-align: right;
    line-height: 30px; /* 固定像素行高 */
}
```

- 刷新对比两段文字上下间距区别。

## 任务 7：文字修饰 text-decoration（下划线、删除线、取消线条）

常用取值：

- none：取消线条（最常用，a 链接默认带下划线，都要取消）
- underline：下划线
- line-through：删除线

```css
h2 {
    font-size: 30px;
    color: #222;
    font-weight: 700;
    text-align: center;
    text-decoration: underline; /* 标题加下划线 */
}
```
# 今日整体学习内容

- 盒子四大组成：内容区 (content)、内边距 (padding)、边框 (border)、外边距 (margin)

- 学会调整盒子大小、间距、边框样式，页面排版全靠盒模型实现

## 任务 1：新建 day3 基础文件

1. 在项目目录新建 `day3.html`

```html
<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <title>Day3 CSS盒模型练习</title>
    <link rel="stylesheet" href="style3.css">
</head>
<body>
    <!-- 练习用盒子 -->
    <div class="box">
        盒模型测试文字
    </div>
</body>
</html>
```

2. 同级目录 新建空白style3.css

3. 右键HTML打开网页

## 任务 2：设置盒子宽高（content 内容区域）

```css
.box {
    /* 内容宽度 */
    width: 300px;
    /* 内容高度 */
    height: 200px;
    /* 加背景色，方便肉眼看清盒子范围 */
    background-color: skyblue;
}
```

刷新页面看效果

蓝色矩形盒子出现，文字挤在盒子左上角

- width/height 仅仅控制内容区域大小，padding、border 都会额外撑大盒子整体尺寸

## 任务 3:border边框设置（盒子四周线条）

边框三要素：粗细，线型，颜色

常用的线型：solid实线、dashed虚线，dotted点状线

```css
.box {
    width: 300px;
    height: 200px;
    background-color: skyblue;
    /* 统一四边边框：粗细 线型 颜色 */
    border: 5px solid darkblue;
}
```

刷新：盒子外围多出一圈深蓝色实线边框

单独设置某一边边框：

```css
/* 仅顶部边框 */
border-top: 3px dashed red;
```

可以自行替换尝试虚线，点状边框效果

## 任务 4 ：padding内边距（内容与边框之间的距离）

核心：文字和盒子之间的留白空间，会撑大盒子整体大小

四个方向简写规则

添加padding样式

```css
.box{
    width: 300px;
    height: 200px;
    backgrund-color: skyblue;
    border: 5px solid darkblue;
    /*上下左右内边距全部25px*/
    pading：25px；
}
```

刷新页面：文字远离边框，盒子整体变大了

## 任务5:margin外边距（盒子与其他元素之间的距离）

作用：控制盒子与页面边界，其他盒子之间的外部边距
简写规则和padding一致

编写规则

```css
.box{
    width: 300px;
    height: 200px;
    background-color:skyblue;
    border: 5px solid darkblue;
    padding: 25px;
    /*上下外边距50px，左右自动居中*/
    margin: 50px auto;
}
```

效果：

1. 盒子距离页面顶部往下错开50px

2. 盒子整体在页面水平正中间(常用居中写法)

## 任务六 标准盒模型vs怪异盒子模型

1. 默认：标准盒模型

盒子总宽度= width + padding左右+border左右
在这个模式里padding和边框会额外加大盒子尺寸

2. 怪异盒模型

设置后：width就是盒子整体总宽度，padding，边框向内挤压内容，不大会撑大盒子

```css
.box {
    box-sizing: border-box;
    width: 300px;
    height: 200px;
    background-color: skyblue;
    border: 5px solid darkblue;
    padding: 25px;
    margin: 50px auto;
}
```

## 任务七：综合实践制作个人信息卡片 

页面效果：圆角个人简介卡片，白底，阴影，居中排版

```html
<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <title>个人卡片实战</title>
    <link rel="stylesheet" href="style3.css">
</head>
<body>
    <div class="card">
        <h3>个人信息</h3>
        <p>姓名：XXX</p>
        <p>方向：全栈前端开发学习</p>
        <p>座右铭：循序渐进，日积月累</p>
    </div>
</body>
</html>
```

```css
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    font-family: "Microsoft Yahei";
}
body {
    background-color: #f5f5f5;
}
.card {
    width: 360px;
    padding: 35px;
    margin: 80px auto;
    background: #fff;
    border: 1px solid #eee;
    /* 圆角 */
    border-radius: 12px;
    /* 卡片阴影，营造立体感 */
    box-shadow: 0 2px 12px rgba(0,0,0,0.1);
}
.card h3 {
    font-size: 22px;
    margin-bottom: 20px;
    text-align: center;
    color: #333;
}
.card p {
    font-size: 16px;
    line-height: 2;
    color: #555;
}
```

最终效果：可以通过微调padding和margin感受间距的变化




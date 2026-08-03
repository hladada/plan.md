# 今日重点：网页横向排版核心 —— 浮动，绝大多数传统网页导航栏、多列卡片排布都靠浮动实现

## 任务一：新建练习文件

1. 新建今日练习文件day-5.html

```html
<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <title>Day5 浮动布局</title>
    <link rel="stylesheet" href="style5.css">
</head>
<body>
    <div class="box1">盒子1</div>
    <div class="box2">盒子2</div>
    <div class="box3">盒子3</div>
</body>
</html>
```

2. 同级新建空白style5.css

3. 打开网页

## 任务二 ： 认识默认标准文档流（静态布局规则）

```css
*{
    margin：0；
    padding：0；
    box-sizing:border-box;
    
}
div{
    width: 150px;
    height: 150px;
    font-size: 20px;
    text-align: center;
    line-height: 150px;
    color: #fff;

}
.box1{
    background: #409eff
}
.box2{
    background: #67c23a
}
.box3{
    background: #e6a23C

}
```

刷新页面观察：
块级元素div默认独占一整行，纵向挨个往下排，无法横向并排。

用浮动打破这个规则

## 任务三： float浮动基础用法

float三个常用取值

1. float： left；向左浮动，元素靠左边横向排列

2. float： right；向右浮动，元素靠右边依次排列

3. float： none；默认值，不浮动 

实操：三个盒子全部往左浮动，实现横向并排

```css
.box1{
    background： #409eff
    float：left；
}

.box2{
    background: #67c23a
    float：left；
}
.box3{
    background: #e6a23c
    float：left；
}
```

保存刷新三个方块紧紧的挨在一起，从左到右成一排
横向布局就实现了

## 任务4：浮动两大特性

### 特性一 ：浮动元素会脱离标准文档流

父盒子如果只有浮动子元素，父盒子高度会直接塌陷成0

我们验证一下

1. HTML外面嵌套一层父容器

```html
<div class="fathera">
    <div class="box1">盒子1</div>
    <div class="box2">盒子2</div>
    <div class="box3">盒子3</div>
</div>
```

2. 给父盒子加背景色查看高度


```css
.father{
    background：#ddd；
    border：2px solid  #000；

}
```

刷新：父盒子看不见了，高度5坍塌，这是浮动常见的问题，后面要专门 清除浮动解决

### 特性2：浮动元素宽度自适应内容

## 任务五：清除四种浮动常用方法

作用：解决父元素高度塌陷，4种方式循序渐进

方法1：给父盒子固定高度

```css
.father{
    background：#ddd；
    border：2px solid  #000；
    height： 150px；
}
```

缺点：子元素高度一旦修改，父盒子就要跟着改，不方便自适应布局

方法2：

在父盒子最末尾，新建div，设置Clear；both；

```html
<div class="father">
    <div clear="box1">盒子1</div>
    <div class="box2">盒子2</div>
    <div class="box3">盒子3</div>
    <!--清除浮动空标签-->
    <div class="clear"></div>
```

```css
.clear{
    clear: both;
}
```

效果：父盒子自动撑开高度，塌陷修复

方法三：overflow：hidden

直接给父容器添加属性

```css
.father{
    background: #ddd
    border: 2px solid #000;
    overflow: hidden;    
}
```

方法四：万能伪类清除浮动

书写通用clearfix类，今后所有需要清除浮动的父盒子直接加一个类

```css
.clearfix::after {
    content: "";
    display: block;
    clear: both;
    height: 0;
    visibility: hidden;
}
```
HTML 调用：

```html
<div class="father clearfix">
    <div class="box1">盒子1</div>
    <div class="box2">盒子2</div>
    <div class="box3">盒子3</div>
</div>
```




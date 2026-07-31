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


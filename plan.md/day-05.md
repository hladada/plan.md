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

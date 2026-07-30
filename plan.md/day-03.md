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


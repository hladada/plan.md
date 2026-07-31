# Day4 分步任务：CSS 背景样式 + 图片排版 + 基础圆角阴影

## 任务一：新建练习文件

1. 在项目里新建day4.html，粘贴基础骨架

```html
<!DOCTUPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <title> day-4背景图与图片样式</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <div calss="bg-box">
        背景样式测试区域
        </div>
    </body>
    </html>
```

2. 新建同级空白 style4.css

3. 打开网页

## 任务2：基础背景色 background-color

写入css

```css
.bg-box {
    width: 400px;
    height: 260px;
    background-color: #7bc1c1;
}
```

刷新之后：盒子铺满浅蓝色底色
可选颜色写法:英语单词，十六进制都可以

## 任务三:插入背景图片 background-image

语法：background-image: url(图片路径);

实操步骤

1. 在你的项目文件夹新建文件夹：image，专门存放图片

2. 把你之前的证件照放进images文件夹里

3. css引入图片作为盒子的背景

```css
.bg-box{
    width: 400px;
    height: 260px;
    background-color: #87CEEB;
    /* 引入背景图 */
    background-image： URL（）
}
```

刷新以后，默认图片会横向+纵向无线平铺铺满整个盒子

## 任务四 ：控制图片平铺

- repeat：默认，横竖都平铺
- no-repeat：不平铺只显示一张
- repeat-x：只水平横向平铺
- repeat-y：只垂直纵向平铺

```css
.bg-box{
    width: 400px;
    height: 260px;
    background-color:  #87CEEB;
    background-image: url(images/你的照片文件名.jpg)
    background-repeaat
}
```

果：只出现一张照片，多余区域露出背景蓝色

## 任务五：背景图片位置 Background-position

控制图片在盒子里摆放位置

简写格式 水平位置，垂直位置

水平： left，center，right  

垂直：top、center、bottom

可以自己试试替换left top，right bottom查看区别

## 任务6 背景图片尺寸 background-size

1. cover：图片等比例放大，完全铺满盒子，超出部分裁剪

2. contain：图片完整显示在盒子内，不会裁剪，会留有空白

```css
.bg-box{
    width: 400px;
    height: 260px;
    background-color： #87CEEB;
    background-image：url（images/你的照片文件名.jpg）;
    background-repeat:no-repeat;
    background-position:center;
    background-size: cover;
}
```

切换cover/contain对比差异

## 任务七 ：圆角border-radius+盒子阴影box-shadow

1. 圆角设置

- 给正方形盒子写50%直接变圆形

- 像素值：四个角统一圆角大小

```css
.bg-box {
    width: 400px;
    height: 260px;
    background-color: #87CEEB;
    background-image: url(images/你的照片文件名.jpg);
    background-repeat: no-repeat;
    background-position: center;
    background-size: cover;
    border-radius: 15px;
    /* 阴影 */
    box-shadow: 0 4px 16px rgba(0,0,0,0.25);
}
```

页面就会有立体悬浮感

## 任务 8：综合实战：个人头像展示卡片

```html
<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <title>头像卡片实战</title>
    <link rel="stylesheet" href="style4.css">
</head>
<body>
    <div class="avatar-card">
        <div class="avatar"></div>
        <h4>学习开发者</h4>
        <p>全栈前端练习中 | Day4打卡</p>
    </div>
</body>
</html>
```

```css
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    font-family: "微软雅黑";
}
body {
    background: #f0f2f5;
    padding: 60px;
}
.avatar-card {
    width: 320px;
    padding: 30px 20px;
    margin: 0 auto;
    background: #fff;
    border-radius: 16px;
    box-shadow: 0 3px 15px rgba(0,0,0,0.12);
    text-align: center;
}
/* 圆形头像盒子 */
.avatar {
    width: 140px;
    height: 140px;
    margin: 0 auto 20px;
    border-radius: 50%;
    background-image: url(images/你的照片.jpg);
    background-repeat: no-repeat;
    background-position: center;
    background-size: cover;
    border: 4px solid #eee;
}
h4 {
    font-size: 20px;
    color: #222;
    margin-bottom: 10px;
}
p {
    color: #666;
    line-height: 1.6;
}
```

运行效果：圆形证件照头像卡片，网页流行个人主页样式




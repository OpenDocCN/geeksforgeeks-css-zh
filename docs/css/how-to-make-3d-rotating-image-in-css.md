# 如何在 CSS 中制作 3D 旋转图像？

> 原文:[https://www . geeksforgeeks . org/如何制作 3d 旋转图像-in-css/](https://www.geeksforgeeks.org/how-to-make-3d-rotating-image-in-css/)

在本教程中，我们将向您展示如何使用简单的 HTML 和 CSS 动画属性创建三维旋转图像库。

**说明:**

在本文中，我们主要使用 CSS 变量、CSS flex、对象适配、变换样式、动画、变换和关键帧属性来执行这个任务。欲了解更多 CSS 关键帧属性请参考**[**【https://www.geeksforgeeks.org/css-animations/】**](https://www.geeksforgeeks.org/css-animations/)**文章。****

******HTML:** 创建结构****

## ****超文本标记语言****

```css
**<!DOCTYPE html>
<html>

    <head>
        <link rel="stylesheet" href="app.css">
    </head>

    <body>

        <div class="box">

            <!-- adding CSS variable --i -->
            <span style="--i:1;">
                <img src=
"https://media.geeksforgeeks.org/wp-content/uploads/20200723131445/img1-300x214.jpg">
            </span>

            <!-- adding CSS variable --i -->
            <span style="--i:2;">
                <img src=
"https://media.geeksforgeeks.org/wp-content/uploads/20200723131451/img2-300x150.jpeg">
            </span>

            <!-- adding CSS variable --i -->
            <span style="--i:4;">
                <img src=
"https://media.geeksforgeeks.org/wp-content/uploads/20200723131448/img3-200x200.jpg">
            </span>

            <!-- adding CSS variable --i -->
            <span style="--i:5;">
                <img src=
"https://media.geeksforgeeks.org/wp-content/uploads/20200723131452/img4-300x167.png">
            </span>

            <!-- adding CSS variable --i -->
            <span style="--i:6;">
                <img src=
"https://media.geeksforgeeks.org/wp-content/uploads/20200723131449/img5-200x113.jpeg">
            </span>

            <!-- adding CSS variable --i -->
            <span style="--i:7;">
                <img src=
"https://media.geeksforgeeks.org/wp-content/uploads/20200723131450/img6-300x82.png" >
            </span>

            <!-- adding CSS variable --i -->
            <span style="--i:8;">
                <img src=
"https://media.geeksforgeeks.org/wp-content/uploads/20200723131446/img7-200x200.jpeg">
            </span>

            <!-- adding CSS variable --i -->
            <span style="--i:9;">
                <img src=
"https://media.geeksforgeeks.org/wp-content/uploads/20200723131452/img8-200x133.jpeg">
            </span>

            <!-- adding CSS variable --i -->
            <span style="--i:3;">
                <img src=
"https://media.geeksforgeeks.org/wp-content/uploads/20200723131447/img9-200x200.jpeg">
            </span>

        </div>   
    </body>

</html>**
```

******CSS:**T2]****

## ****钢性铸铁****

```css
**/* Applying Global CSS */
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

/* Centering the content of whole body */
body {
    display: flex;
    justify-content: center;
    align-items: center;
    min-height: 100vh;
    background: #000;
}

/* Adding transform-style CSS
    property to the boxes */
.box {
    position: relative;
    width: 200px;
    height: 200px;
    transform-style: preserve-3d;
    animation: animate 20s linear infinite;
}

/* Adding keyframes for animation */
@keyframes animate {
    0% {
        transform: perspective(1000px) rotateY(0deg);
    }
    100% {
        transform: perspective(1000px) rotateY(360deg);
    }
}

/* Adding CSS to all the span
    tags for animation */
.box span {
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    transform-origin: center;
    transform-style: preserve-3d;
    transform:
      rotateY(calc(var(--i) * 45deg)) translateZ(400px);
    -webkit-box-reflect:
below 0px linear-gradient(transparent, transparent, #0004);
}

/* Adding object-fit CSS property to all the images */
.box span img {
    position: absolute;
    top: 0;
    left: 0;
    height: 250px;
    width: 300px;
    object-fit: cover;
}**
```

******最终解决方案:****** 

## ****钢性铸铁****

```css
**<!DOCTYPE html>
<html>
    <head>
        <style>
            /* Applying Global CSS */
            * {
                margin: 0;
                padding: 0;
                box-sizing: border-box;
            }

            /* Centering the content of whole body */
            body {
                display: flex;
                justify-content: center;
                align-items: center;
                min-height: 100vh;
                background: #000;
            }

            /* Adding transform-style CSS
               property to the boxes */
            .box {
                position: relative;
                width: 200px;
                height: 200px;
                transform-style: preserve-3d;
                animation: animate 20s linear infinite;
            }

            /* Adding keyframes for animation */
            @keyframes animate {
                0% {
                  transform: perspective(1000px) rotateY(0deg);
                }
                100% {
                 transform: perspective(1000px) rotateY(360deg);
                }
            }

            /* Adding CSS to all the span
               tags for animation */
            .box span {
                position: absolute;
                top: 0;
                left: 0;
                width: 100%;
                height: 100%;
                transform-origin: center;
                transform-style: preserve-3d;
                transform:
             rotateY(calc(var(--i) * 45deg)) translateZ(400px);
                -webkit-box-reflect:
     below 0px linear-gradient(transparent, transparent, #0004);
            }

            /* Adding object-fit CSS
          property to all the images */
            .box span img {
                position: absolute;
                top: 0;
                left: 0;
                height: 250px;
                width: 300px;
                object-fit: cover;
            }
        </style>
    </head>

    <body>
        <div class="box">
            <!-- Adding CSS variable --i -->
            <span style="--i: 1;">
                <img src=
"https://media.geeksforgeeks.org/wp-content/uploads/20200723131445/img1-300x214.jpg" />
            </span>

            <!-- Adding CSS variable --i -->
            <span style="--i: 2;">
                <img src=
"https://media.geeksforgeeks.org/wp-content/uploads/20200723131451/img2-300x150.jpeg" />
            </span>

            <!-- Adding CSS variable --i -->
            <span style="--i: 4;">
                <img src=
"https://media.geeksforgeeks.org/wp-content/uploads/20200723131448/img3-200x200.jpg" />
            </span>

            <!-- Adding CSS variable --i -->
            <span style="--i: 5;">
                <img src=
"https://media.geeksforgeeks.org/wp-content/uploads/20200723131452/img4-300x167.png" />
            </span>

            <!-- Adding CSS variable --i -->
            <span style="--i: 6;">
                <img src=
"https://media.geeksforgeeks.org/wp-content/uploads/20200723131449/img5-200x113.jpeg" />
            </span>

            <!-- Adding CSS variable --i -->
            <span style="--i: 7;">
                <img src=
"https://media.geeksforgeeks.org/wp-content/uploads/20200723131450/img6-300x82.png" />
            </span>

            <!-- Adding CSS variable --i -->
            <span style="--i: 8;">
                <img src=
"https://media.geeksforgeeks.org/wp-content/uploads/20200723131446/img7-200x200.jpeg" />
            </span>

            <!-- Adding CSS variable --i -->
            <span style="--i: 9;">
                <img src=
"https://media.geeksforgeeks.org/wp-content/uploads/20200723131452/img8-200x133.jpeg" />
            </span>

            <!-- Adding CSS variable --i -->
            <span style="--i: 3;">
                <img src=
"https://media.geeksforgeeks.org/wp-content/uploads/20200723131447/img9-200x200.jpeg" />
            </span>
        </div>
    </body>
</html>**
```

******输出:****** 

****![](img/990b751d71f2c4d0f329a72b6d9054ce.png)****
## 垂直居中

- 1.垂直居中是子元素相对于父元素的垂直方向的居中，至少有两个元素互相做参考。
- 2.如果有两个或两个以上的 （水平） 子元素，要保证所有子元素都在父元素的垂直方向上居中。
- 3.要么子元素和父元素的高度至少有一方是确定的

### 垂直居中大致有如下两种情况
- 1. 水平子元素有两个或两个以上
例如：
``` html
这种情况，两个子元素会底边对齐
#### 1.父容器高度不定
<style>
        .container {
            /* 万能的flex 布局
               display: flex;
               flex-direction: row;
               align-items: center;
            */
            border: 1px solid;
        }

        .box1 {
            display: inline-block;
            border: 1px solid red;
            width: 100px;
            height: 100px;
        }

        .box2 {
            display: inline-block;
            border: 1px solid blue;
            width: 100px;
            height: 90px;
        }
    </style>
    <div class="container">
        <div class="box1"></div>
        <div class="box2"></div>
    </div>
```

``` html

    <style>
        .container {
            border: 1px solid;
        }

        .box1 {
            display: inline-block;
            border: 1px solid red;
            width: 100px;
            height: 100px;
            vertical-align: middle;
        }

        .box2 {
            line-height: 200px;
            display: inline-block;
            border: 1px solid blue;
            width: 100px;
            height: 90px;
            vertical-align: middle;
        }
    </style>
    <div class="container">
        <div class="box1"></div>
        <div class="box2"></div>
    </div>
```
#### 2.父容器高度一定
如果子元素高度不定，用flex布局最好，如果一定用上下padding+ 子元素高度和父元素高度结合也可以。

## 最好父容器高度不定，这样它可以由子元素的高度自由决定，更有弹性。这样的话最好是上下padding + flex 布局


- 2. 只有一个子元素
- 父元素高度必须一定，比如相对于position:absolute;height:100%的body(其实是相对于屏幕了）

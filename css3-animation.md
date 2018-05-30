
### animation的基本设置：

``` css
    animation: move 10s linear 0s infinite alternate running forwards;
```
alternate  表示是否反向播放动画
running|pause 表示是否暂停
forwards|表示动画是否在改变后不再回到初始状态

### 顺序动画的方案
- 1. 多个元素的顺序动画，用delay在不同的元素上设置，达到顺序执行。
- 2. 同一个元素的连续动画，用不同的class 样式，都设置animation 不同的动画，并用delay 区分次序？？？？ 这个当然不行的，我实验过，会发生覆盖现象
而且覆盖的规则是css 中设置的最后一个class 为最后的样式。
- 3.真正能够实现同一个元素执行不同的动画要这么写：分别设置动画样式，每个样式用逗号分隔。
``` css
-webkit-animation-name:bounceInLeft1, bounce1;
-webkit-animation-duration:2s, 1.5s;
-webkit-animation-timing-function:ease, linear;
-webkit-animation-delay:5.2s, 7.2s;
-webkit-animation-iteration-count:1, infinite;
-webkit-animation-fill-mode:forwards, none;
```

### 示例

``` html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta http-equiv="X-UA-Compatible" content="ie=edge">
    <title>Document</title>
    <style>
        .wrapper{
            position: relative;
            transform-origin: 200px 200px;
            transform: rotateZ(0deg);
            /* 同一个元素用多个动画 */
            animation-name: rotateZ , skewY;
            animation-duration: .3s ,.3s;
            animation-timing-function:ease, linear;
            animation-delay:1.2s, 2s;
            animation-iteration-count:1, infinite;
            animation-fill-mode:forwards , none;
        }
 
        .rect {
            top: 150px;
            position: absolute;
            height: 50px;
            /* 2*R */
            width: 300px;
        }

        .rect>.circle {
            height: 50px;
            width: 50px;
            border: 1px solid blue;
            border-radius: 100%;
            text-align: center;
            box-shadow: 0px 0px 8px 8px;
            /* rect width - radius */
            transform: translateX(125px);
            opacity: 0;
        }

        .rect:nth-child(1) > .circle{
            background: red;
            animation: move-to-start .5s ease-out  0s forwards;
        }

        .rect:nth-child(2) > .circle{
            animation: move-to-start .5s ease-out  .3s forwards;
        }

        .rect:nth-child(3) > .circle{
            animation: move-to-start .5s ease-out  .6s forwards;
        }

        .rect:nth-child(4) > .circle{
            animation: move-to-start .5s ease-out  .9s forwards;
        }

        .rect:nth-child(5) > .circle{
            animation: move-to-start .5s ease-out  1.2s forwards;
        } 

        /* 半圆布局 */
        .rect:nth-child(1){
            transform: rotateZ(0deg);
        }

        .rect:nth-child(2){
            transform: rotateZ(45deg);
        }

        .rect:nth-child(3){
            transform: rotateZ(90deg);
        }

        .rect:nth-child(4){
            transform: rotateZ(135deg);
        }

         .rect:nth-child(5){
            transform: rotateZ(180deg);
        }

        @keyframes move-to-start{
            from{
                transform: translateX(calc(150px - 25px));
                opacity: 0;
            }
            to{
                transform: translateX(0);
                opacity: 1;
            }
        }


        @keyframes rotateZ{
            from{
                transform:rotateZ(0deg);
            }
            to{
                transform:rotateZ(360deg);
            }
        }

        @keyframes skewY{
            from{
                transform:skewY(0deg);
            }
            to{
                transform:skewY(45deg);
            }
        }
    </style>
</head>

<body>
    <div class="wrapper">
        <div class="rect">
            <div class="circle">1</div>
        </div>
        <div class="rect">
            <div class="circle">2</div>
        </div>
        <div class="rect">
            <div class="circle">3</div>
        </div>
        <div class="rect">
            <div class="circle">4</div>
        </div>
        <div class="rect">
                <div class="circle">5</div>
            </div>
    </div>

</body>

</html>
```

### 复合变换动画 下面的变换，如果交换了顺序将不会达到一个向前滚动的圆形的效果。
- 1.
``` html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta http-equiv="X-UA-Compatible" content="ie=edge">
    <title>Document</title>
    <style>
        .circle{
            width: 100px;
            height: 100px;
            border: 1px solid red;
            border-radius: 100px;
            text-align: center;
            line-height: 100px;
            animation-name: move;
            animation-timing-function: linear;
            animation-duration: 3s;
            animation-fill-mode:forwards
        }

        @keyframes move{
            from{
                transform: translateX(0) rotateZ(0deg)
            }
            to{
                transform: translateX(500px) rotateZ(360deg)
            }
        }
    </style>
</head>
<body>
    

    <div class="circle">6</div>
</body>
</html>
```
- 2 圆形螺旋到指定的水平位置
``` html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta http-equiv="X-UA-Compatible" content="ie=edge">
    <title>Document</title>
    <style>
        .circle{

            position: absolute;
            left:300px;
            top: 300px;
            width: 100px;
            height: 100px;
            border: 1px solid red;
            border-radius: 100px;
            text-align: center;
            line-height: 100px;
            animation-name: move;
            animation-timing-function: linear;
            animation-duration: 3s;
            animation-fill-mode:forwards
        }

        @keyframes move{
            from{
                transform:  rotateZ(0deg) translateX(0)
            }
            to{
                transform:  rotateZ(360deg) translateX(500px)
            }
        }
    </style>
</head>
<body>
    

    <div class="circle">6</div>
</body>
</html>
```

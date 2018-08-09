

### 先申明这个demo 我不是原作者
##### 没有想到box-shadow 还可以设置多个值！！

 ## css3 中可以设置多个值在一个样式属性的情况有很多。比如background-image,srcset,box-shadow ....
 - like this.每个部分都是相当于一个模糊的矩形，但矩形只能在原来元素的下面和周围，不能遮挡原来的元素。
 ```css
       box-shadow: 10px 50px 12px 1px  black,
      1px 100px 12px 1px  red;
 
 ```

``` html
<!DOCTYPE html>  
<html lang="en">  
<head>  
    <meta charset="UTF-8">  
    <meta name="viewport" content="width=device-width, initial-scale=1.0">  
    <meta http-equiv="X-UA-Compatible" content="ie=edge">  
    <title>Document</title>  
    <style>  
        .container{  
            position: relative;  
            width: 36px;  
            height: 36px;  
            border-radius: 50%;  
            margin: 300px auto;  
            background-color: #C63D01;  
            box-shadow: 0px 0px 0 1px #000,  
                -20px -26px 0 -10px #333333,  
                -34px -40px 0 15px #fff,  
                -34px -40px 0 16px,  
                20px -26px 0 -10px #333333,  
                34px -40px 0 15px #fff,  
                34px -40px 0 16px,  
                0px 55px 0 75px #fff,  
                0px 55px 0 76px #000,  
                0 22px 0 120px #08BDEB,  
                0 22px 0 121px #000;  
        }  
        /*叮当猫的鼻子*/ 
        .container::before{  
            content: '';  
            position: absolute;  
            bottom: -81px;  
            left: 17px;  
            height: 80px;  
            width: 2px;  
            background-color: #000;  
        }  
        /*叮当猫的嘴巴*/ 
        .container::after{  
            content: '';  
            position: absolute;  
            bottom: -83px;  
            left: -44px;  
            width: 125px;  
            height: 70px;  
            border-bottom-right-radius: 28px;  
            border-bottom: solid 2px black;  
            border-bottom-left-radius: 28px;  
        }  
    </style>  
</head>  
<body>  
    <p class="container">  
    </p>  
</body>  
</html>
```

### 顺便提一下 filter:drop-shadow()
这个滤镜才能算是真正意义上的shadow,因为凡是被设置的元素，就好像从它的上面射了一道光，然后不透明的地方就成了投影，很好玩。而box-shadow,则像是素描，硬生生的给二维的框框加上画上了阴影。 它的前两个值是相对于设置元素的x,y偏移，第三个是模糊度，最后一个颜色。比box-shadow,少了一个spread.
```css
    filter: drop-shadow(250px 0px 11px #4444dd);
```

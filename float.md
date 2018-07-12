## 特别鸣谢
[渡一教育的姬成老师](https://ke.qq.com/course/231570?_bid=167&_wv=1&from=courseShare)

## 浮动模型 
- css 里面有3大模型：浮动模型 层级模型 盒子模型。浮动模型是最恶心的，个人感觉将来会淘汰。不过有时候它确实比较好用。

```html
    <style>
        .box{
            float: right;
            width: 500px;
            height: 100px;
            background: red;
            text-align: center;
            line-height: 100px;
            margin: 10px;
        }
    </style>
<body>
    <div class="wrapper">
        <div class="box">1</div>
        <div class="box">2</div>
        <div class="box">3</div>
        <div class="box">4</div>
    </div>
</body>
```

- 浮动元素产生了浮动流
- 所有产生了浮动流的元素，块级元素看不到(当它们不存在，所以浮动元素的父容器会包裹不住)它们
- 产生了BFC的元素和文本属性的元素(inline)以及文本可以看到它们
- 补充:float 会产生浮动流,并脱离原来的文档流.如果它之后的块元素不设置清除浮动,则会和浮动元素(设置了大小)在一行.

## 让父容器包裹子元素的：第一种解决办法：
```html
   <style>
        .box{
            float: right;
            width: 500px;
            height: 100px;
            background: red;
            text-align:  center;
            line-height: 100px;
            margin: 10px;
        }

        .wrapper{
            border: 1px solid;
        }

        .clearfix{
            /* background:#00bebe; */
            /* 这一句决定了p 标签是否被浮动流影响 */
            clear:both;
        }
    </style>
</head>
<body>
    <div class="wrapper">
        <!-- 浮动流 -->
        <div class="box">1</div>
         <!-- 浮动流 -->
        <div class="box">2</div>
         <!-- 浮动流 -->
        <div class="box">3</div>
         <!-- 浮动流 -->
        <div class="box">4</div>
         <!-- 浮动流 -->
         <p class='clearfix'></p>
    </div>
</body>
```

## 让父容器包裹子元素的：第二种解决办法：不加新的标签
```css
    .wrapper::after{
        content:"";
        /*必须是块级元素才能够清浮动*/
        display:block;
        clear:both;
    }
```
## 让父容器包裹子元素的：第三种解决办法：让父级元素变成BFC 比如：
``` css
    .wrapper{
        float:left;//display:inline-block//position:absolute;
    }
```

# 高级知识点：
position:absolute;和float:left/right 设置之后，系统内部会默认将display 设置成inline-block;也可以知道如果原来是inline 的元素
设置完了上面的两种后，将可以设置宽高，比如：span标签。
# 如何让一个图标被文字环绕，img{float:left;margin-right:10px}

## 用浮动做菜单的思路：
```html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta http-equiv="X-UA-Compatible" content="ie=edge">
    <title>Document</title>
    <style>
        *{
            text-decoration: none;
            color:#00bebe;
        }

        ul{
            list-style: none;
        }

        ul::after{
            content: "";
            display: block;
            clear: both;
        }

        .menu-item{
            float: left;
            height: 30px;
            width: 100px;
            margin: 0 10px;
            text-align: center;
        }


        li.menu-item > a{
            display: block;
            border-radius: 6px;
            height: 30px;
            padding: 0 10px;
            line-height: 30px;
        }

        li.menu-item > a:hover{
            background: #00bebe;
            color: white;
        }
    </style>
</head>

<body>


    <ul class="menu">
        <li class="menu-item">
            <a href="#">1</a>
        </li>
        <li class="menu-item">
            <a href="#">2</a>
        </li>
        <li class="menu-item">
            <a href="#">3</a>
        </li>
    </ul>
    <p>不会被浮动影响</p>

</body>

</html>
```

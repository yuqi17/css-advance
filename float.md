
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

        p{
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
         <p></p>
    </div>
</body>
```


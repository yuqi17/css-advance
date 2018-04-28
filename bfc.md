##  BFC (block format context) 块级格式化上下文
### 触发父级元素 bfc，修改元素的渲染规则
- 1.position:absolute;
- 2.display:inline-block;
- 3.float:left/right;
- 4.overflow:hidden;
### 设置border 太暴力？我觉得未必 ： border: 1px solid transparent;

## 1. margin 塌陷
```html
    <style>
    *{
        padding: 0;
        margin: 0;
    }
    .container{
        margin-top: 10px;
        height: 100px;
        width: 100px;
        background: red;
        /*如果不设置边框，则父子margin-top重合，看上去子元素和父元素没有上边距，这种现象叫margin塌陷*/
        /* border: 1px solid; */
    }
    .content{
        margin-top: 10px;
        height: 50px;
        width: 50px;
        background: green;
    }
    </style>
</head>
<body>
    <div class="container">
        <div class="content"></div>
    </div>
</body>
```

## 2.margin 合并 （没有解决的必要，margin-bottom:20px；）
```html
 <style>
    *{
        padding: 0;
        margin: 0;
    }
  
    .brother1{
        height: 50px;
        width: 50px;
        background: green;
        margin-bottom: 10px;
    }

    .brother2{
        height: 50px;
        width: 50px;
        background: #d3d3d3;
        margin-top: 10px;
    }
    </style>
</head>
<body>
    <div class="brother1"></div>
    <div class="brother2"></div>
</body>
```
- 第二中margin 合并的解决方案：给brother2 外面套一层.wrapper层，并设置：.wrapper{overflow:hidden;}
(32分老师开始讲战略战术历史 知识渊博啊)[https://ke.qq.com/webcourse/index.html#course_id=231570&term_id=100273162&taid=1441330895227026&vid=w1419sgihrf]

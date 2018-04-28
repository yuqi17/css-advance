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
        /*如果不设置边框，则父子margin-top重合，看上去子元素和父元素没有上边距，这种现象叫margin塌陷 也交bfc*/
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

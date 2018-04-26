```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta http-equiv="X-UA-Compatible" content="ie=edge">
    <title>Document</title>
    <style>
    .container{
        display: inline-block;
        position: relative;
        overflow: hidden;
    }

    .mask{
        position: absolute;
        height: 100%;
        width: 100%;
        background: #fff;
        animation: slideRight 1s forwards;
    }

    @keyframes slideRight {
        0%{
            left: 0%;
        }
        100%{
            left: 100%;
        }
    }
    </style>
</head>
<body>
    <div class="container">
        <div class="mask"></div>
        <img src="duihao.png">
    </div>
</body>
</html>
```

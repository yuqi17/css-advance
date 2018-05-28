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
            margin: 0;
            box-sizing: border-box;
        }

        body{
            overflow: hidden;
            background: #ccc;
        }

        .header{
            position: fixed;
            top: 0;
            height: 50px;
            width: 100%;
            background: #fff;
            /* box-shadow: 0px 1px 12px 1px; */
        }

        .footer{
            position: fixed;
            bottom: 0;
            height: 50px;
            width: 100%;
            background: #fff;
            /* box-shadow: 0px -1px 12px 1px; */
        }

        .content{
            position: fixed;
            width: 100%;
            top: 50px;
            /* 屏高 - 高(footer + header) - content 上下margin 10px */
            height: calc(100vh - 100px - 20px);
            margin: 10px 0;
            /* padding: 10px; */
            overflow-y: scroll;
            overflow-x: hidden;
            background: #fff;
            /* border: 2px solid blue */
        }
    </style>
</head>
<body>
    
    <div class="container">
        <div class="header"></div>
        <div class="content">
            asdfasdfasdfasdfasdf<br>
            asdfasdfasdfasdfasdf<br>
            asdfasdfasdfasdfasdf<br>
            asdfasdfasdfasdfasdf<br>
            asdfasdfasdfasdfasdf<br>
            asdfasdfasdfasdfasdf<br>
            asdfasdfasdfasdfasdf<br>
            asdfasdfasdfasdfasdf<br>
            asdfasdfasdfasdfasdf<br>
            asdfasdfasdfasdfasdf<br>
            asdfasdfasdfasdfasdf<br>
            asdfasdfasdfasdfasdf<br>
            asdfasdfasdfasdfasdf<br>
            asdfasdfasdfasdfasdf<br>
            asdfasdfasdfasdfasdf<br>
            asdfasdfasdfasdfasdf<br>
            asdfasdfasdfasdfasdf<br>
            asdfasdfasdfasdfasdf<br>
            asdfasdfasdfasdfasdf<br>
            asdfasdfasdfasdfasdf<br>
            asdfasdfasdfasdfasdf<br>
            asdfasdfasdfasdfasdf<br>
            asdfasdfasdfasdfasdf<br>
            asdfasdfasdfasdfasdf<br>
            asdfasdfasdfasdfasdf<br>
            asdfasdfasdfasdfasdf<br>
            asdfasdfasdfasdfasdf<br>
            asdfasdfasdfasdfasdf<br>
            asdfasdfasdfasdfasdf<br>
            asdfasdfasdfasdfasdf<br>
            asdfasdfasdfasdfasdf<br>
            asdfasdfasdfasdfasdf<br>
            asdfasdfasdfasdfasdf<br>
            asdfasdfasdfasdfasdf<br>
            asdfasdfasdfasdfasdf<br>
            asdfasdfasdfasdfasdf<br>
            asdfasdfasdfasdfasdf<br>
            asdfasdfasdfasdfasdf<br>
            asdfasdfasdfasdfasdf<br>
            asdfasdfasdfasdfasdf<br>
            asdfasdfasdfasdfasdf<br>
            asdfasdfasdfasdfasdf<br>
            asdfasdfasdfasdfasdf<br>
            wwwwwwwwwwwwwwwwwwwwwwwwwwwwwwwww<br>
            wwwwwwwwwwwwwwwwwwwwwwwwwwwwwwwww<br>
            wwwwwwwwwwwwwwwwwwwwwwwwwwwwwwwww<br>
            wwwwwwwwwwwwwwwwwwwwwwwwwwwwwwwww<br>
            wwwwwwwwwwwwwwwwwwwwwwwwwwwwwwwww<br>
            wwwwwwwwwwwwwwwwwwwwwwwwwwwwwwwww<br>
            wwwwwwwwwwwwwwwwwwwwwwwwwwwwwwwww<br>
            wwwwwwwwwwwwwwwwwwwwwwwwwwwwwwwww<br>
        </div>
        <div class="footer"></div>
    </div>
</body>
</html>
```

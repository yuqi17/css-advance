注意table/table-cell 形成了一个完全铺满的cell,里面的内容可以垂直居中，水平居中可以用margin:0 auto,inline-xx + text-align:center等来水平居中

```html
<!DOCTYPE html>
<html lang="en">

<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Document</title>
  <style>
    body {
      margin: 0;
      display: table;
      height: 100vh;
      width: 100%;
    }

    .box {
      vertical-align: middle;
      text-align: center;
      display: table-cell;
      border: 1px solid #eee;
      background-color: #fbfe;
    }

    .text {
      /* display: inline-block; */
      margin: 0 auto;
      border: 1px solid red;
      height: 100px;
      width: 100px;
    }
  </style>
</head>

<body>
  <div class="box">
    <div class="text">
      11
    </div>
  </div>
</body>

</html>
```

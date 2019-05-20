

``` html
  <!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <meta http-equiv="X-UA-Compatible" content="ie=edge">
  <title>Document</title>
  <style>
    .left{
      float:left;
      width: 100px;
      border: 1px solid red;
      height: 100px;
    }
    .right{
      margin-left: 100px;
      border: 1px solid blue;
      height: 100px;
      min-width: 0px;
    }

    .parent{
      display: flex;
    }

    .flex-left{
      border: 1px solid green;
      flex: 0 0 100px;
    }

    .flex-right{
      border: 1px solid orange;
      flex: 1 0 100px;
    }

  </style>
</head>
<body>

  <div class="left">float left</div>
  <div class="right">margin left</div>

  <br>

   <div class="parent">
      <div class="flex-left">flex item</div>
      <div class="flex-right">flex item</div>
   </div>

</body>
</html>

```

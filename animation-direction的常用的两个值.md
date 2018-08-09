


```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <meta http-equiv="X-UA-Compatible" content="ie=edge">
  <title>Document</title>

  <style>
    .box{
      width: 300px;
      height: 300px;
      border: 1px solid red;
      position: absolute;
    }

    .circle{
      position: absolute;
      width: 30px;
      height: 30px;
      border-radius: 100%;
      display: inline-block;
    }

    .circle:nth-child(1){
      background-color: red;
      animation: move 1s ease-in-out infinite alternate;
    }

     .circle:nth-child(2){
      background-color: blue;
      animation: move 1s ease-in-out infinite alternate-reverse;
    }

    @keyframes move 
    {
      0%{
        transform: translatex(0);
      }
      10%{
        transform: translatex(3px);
      }
      60%{
        transform: translatex(10px);
      }
      70%{
        transform: translatex(90px);
      }
      100%{
        transform: translatex(100px);
      }

    }
  </style>
</head>
<body>
  <div class="box">
    <span class="circle"></span>
    <span class="circle"></span>
  </div>
</body>
</html>
```

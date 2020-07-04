1.box-shadow 可以叠加，用逗号隔开
2.x,y偏移都是[-20px,20px],而且模糊度和阴影扩展半径也是这个范围
3.有内外阴影的区分
```html
<!DOCTYPE html>
<html lang="en">

<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Document</title>
  <style>
    * {
      margin: 0;
      box-sizing: border-box;
    }

    .card {
      height: 50vh;
      width: 50vmin;
      background-color: aqua;
      box-shadow: 6px 6px 4px 0px rgba(0, 200, 200, .7), 5px 3px 6px 9px rgba(0, 0, 0, .3);
      animation: blur 1s ease 0s infinite alternate;
    }

    @keyframes blur {
      from {
        box-shadow: 6px 6px 4px 0px rgba(0, 200, 200, .7), 5px 3px 6px 9px rgba(0, 0, 0, .3);
      }

      to {
        box-shadow: 6px 6px 4px 0px rgba(0, 200, 200, .7), 20px 20px 20px 20px rgba(0, 0, 0, .3);
      }
    }
  </style>
</head>

<body>
  <div class="card">

  </div>
</body>

</html>
```

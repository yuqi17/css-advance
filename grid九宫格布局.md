首先必须夸赞一下这个仁兄的视频，太好了，比一堆深奥的文章好理解多了：[https://www.bilibili.com/video/BV1XE41177oN/?spm_id_from=333.788.videocard.3](https://www.bilibili.com/video/BV1XE41177oN/?spm_id_from=333.788.videocard.3)

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
      padding: 0;
      box-sizing: border-box;
    }

    .container {
      width: 500px;
      height: 500px;
      border: 1px solid blue;
      display: grid;
      column-gap: 10px;
      row-gap: 10px;
      grid-template-columns: auto auto auto;
      grid-template-rows: auto auto auto;
    }

    .item {
      border: 1px solid red;
      background-color: #00bebe;
    }
  </style>
</head>

<body>

  <div class="container">
    <div class="item">1</div>
    <div class="item">2</div>
    <div class="item">3</div>
    <div class="item">4</div>
    <div class="item btn">5</div>
    <div class="item">6</div>
    <div class="item">7</div>
    <div class="item">8</div>
    <div class="item">9</div>
  </div>
</body>

</html>
```

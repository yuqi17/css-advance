```html
<!DOCTYPE html>
<html lang="en">

<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Document</title>
  <style>
    ul {
      border: 1px solid red;
      top: 50%;
      left: 50%;
      transform: translate(-50%, -50%);
      position: absolute;

      /* 必要 */
      padding: 0;
      display: flex;
    }

    li {
      font-size: 24px;
      padding: 20px;
      color: #000;
      line-height: 1;
      cursor: pointer;

      list-style-type: none;
      outline: none;

      /* 必要 */
      position: relative;
      transition: 0.2s all linear;
    }

    /* 相当于一个原元素的影子 不过在水平边界之外，也没有宽度*/
    li::before {
      /* 必要 */
      content: "";
      position: absolute;
      top: 0;
      left: 100%;
      width: 0;
      height: 100%;
      border-bottom: 3px solid #000;
      transition: 0.2s all linear;
    }

    /* 将这个影子与得到焦点的元素重合，并恢复宽度 */
    li:focus::before {
      transition-delay: 0.1s;
      /* 必要 */
      z-index: -1;
      width: 100%;
      top: 0;
      left: 0;
    }

    /* 这个表示选择前面有li:focus的每一个li:before元素，不一定要紧邻 */
    /* 防止上一个focus元素拖尾巴消失 */
    li:focus~li::before {
      left: 0;
    }

    /* 在react vue 等框架中可以用 .active 替换 :focus*/
  </style>
</head>

<body>
  <ul>
    <li tabindex="1">111</li>
    <li tabindex="1">222</li>
    <li tabindex="1">333</li>
    <li tabindex="1">444</li>
    <li tabindex="1">555</li>
  </ul>
</body>

</html>

```

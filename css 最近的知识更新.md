

#### 1. 如果两个元素是兄弟关系,那么其中一个设置了relative,另外一个也最好设置,因为它们的z-index 层次不一样了
#### 2. flex 布局会影响position 定位 特别是居中
#### 3. 设置position 定位 最好明确默认值和不设置的区别,建议设置top left.
#### 4. flex 布局 justify-content 默认值是flex-start, align-items 默认值是 stretch
#### 5. flex item 的默认值 flex 属性是 0 1 auto   flex-grow、flex-shrink 和 flex-basis 属性的简写属性。 
#### 6. css 属性 关键字unset all revert initial inherit  [参考]( http://www.cnblogs.com/xiaohuochai/p/5464456.html)
#### 7. none 和 auto 自适应的意思 (要看实际情况) [参考 margin:auto](http://zh.learnlayout.com/margin-auto.html)
#### 8. [js 正宗读取 css 样式的办法,可以用来验证css语法](https://blog.csdn.net/k358971707/article/details/54590490)
#### 9. point-events:none 只有再z-index 不为-1,且是父子节点的情况下生效(还未验证)
#### 10. 伪元素:after,:before 相当于是父元素的一个子元素,其属性根子元素一般继承规则一样(display是不继承的),content必须设置哪怕是"",否则不显示.
```html
<!DOCTYPE html>
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <meta http-equiv="X-UA-Compatible" content="ie=edge">
  <title>Document</title>
  <style>

    body{
      /* height: 100%; */
    }
    #container{
      border: 1px solid red;
      display: flex;
      align-items: center;
      flex-direction: column;
      font-size: 12px;
      height: 300px;
    }

    #container::after{
      /* content: '1111'; */
      flex: 1;
      width: 100px;
      border: 1px solid red;
    }

    #container div{
      flex: 1;
      border: 1px solid blue;
    }
  </style>
</head>
<body>
  <div id="container">
    <div id="item" style="font-size:30px">
      <div id="child"></div>
    </div>
  </div>
</body>
<script>

// dom.style 只能获得行内样式,要设置才行
const dom1 = document.getElementById('item')
console.log(dom1.style.fontSize)

function getStyle(selector, arr) {
    const dom = document.querySelector(selector)
    if (dom.currentStyle) {//所有的ie
        return dom.currentStyle[arr];
    } else if(window.getComputedStyle){//ie9+ chrome fireFox
        return document.defaultView.getComputedStyle(dom, null)[arr];
    }
    return null;
}


  console.log(getStyle('#item','font-size'))
  console.log(getStyle('#item','display'))

  console.log(getStyle('#item','flex'))
  console.log(getStyle('#child','flex'))// 这个不继承
  console.log(getStyle('#child','align-item'))//不是flexbox item 就undefined

  console.log(getStyle('#container::after','display'))// 伪类取不到
</script>
</html>
```
#### 11. white-space:nowrap; 会保证inline* 元素 在一行显示

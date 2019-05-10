
#### - 首先一定不要太执着的学习框架,而是要学习原理和开发语言的精髓,这些东西是几乎不变的.

#### - 查看css 文档一定要看默认值,默认值,默认值!!!

#### - 实践的时候一定要注意不同浏览器的基础差异然后再去看,推荐使用标准化(margin,padding 默认值都是0)css 库:sanitize.css,normalize.css,minireset.css,unstyle.css

#### - 定位 position 的几个值必须要明白,特别是z-index 的设置是难点基础之一

#### - width 默认值是auto; 如果设置了100%,结果将是非常不同.它会真的按照父容易的宽度*100%设置自己的宽度,如果设置margin会造成不对称.而auto 则是以content 区域为基准,自动撑满的.

#### - overflow 的默认值是visible 是不裁剪的,所以边框有时候会超出父容器,这是正常的,因为没有设置auto,scroll或hidden.这样出现的滚动条往往是html根节点产生的.

#### - html 元素分为替换元素 和 非替换元素 
  - [参考1](https://www.cnblogs.com/WebShare-hilda/p/4713890.html) 
  - [参考2 极其重要](http://www.aichengxu.com/other/3124775.htm)
```eg: input 是可以设置宽高的,img 是替换行内元素 因为它们是替换行内元素虽然具有内在宽高,但设置css 宽高的优先级比它们自身的高,非替换行内元素如 a,span 是不能设置宽的,它们的高度由行高决定```




      

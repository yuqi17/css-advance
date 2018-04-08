

选择器             权重(256进制)
!important        Infinity
行内样式           1000
id                100
class|属性|伪类    10
标签|元素          1
通配符             0

选择器权重计算：
- #id p = 100 + 1 = 101
- .class1 .class2 = 10 + 10 = 20
## 所以上面两个选择器如果选择了同一个元素，并设置同一样式，则权重大的那的为最终样式。如果两者权重一样，则后面的会覆盖前面的。

- 分组选择器        em,div,strong{}
- 并列选择器        div.wrapper
- 子元素选择器       div>em
- 后代选择          div  em
- 相邻兄弟          h1+p
-普通兄弟选择器      h1~p
## 不论是后代选择器，子元素选择器，相邻兄弟选择器还是普通兄弟选择器，选择的都是：最后面的（挨着花括号的）元素。

## font-size 字体默认是16px，说的是字体的高度。

## font-weight:bold 和 strong 一样.值有lighter,normal,bold,bolder.或数值的整百数：100，200，300，400，500，600(bolder)，700，800，900.加粗效果取决于浏览器字体包，有没有这个加粗的样式。

## font-style italic

## font-family:arial 是乔布斯发明的字体。cursive 中文的。

## color 字体颜色的三种设置：
- 土鳖式： 纯英文单词
- 颜色代码：eg: #ff4400  光学三原色 r（00-ff） g（00-ff） b(00-ff)
- 三元色合一变为白色。
- 简写 每两位一样：eg:#ff4400 => #f40
- 颜色函数： rgb(255,255,255) => #fff

## 缩进 text-indent 它和line-height 都用em 单位比较好控制
- 绝对单位  一个像素点只能有一个颜色；
- 1em = 1 * 该标签的font-size(默认是16px) 
- 相对单位

## text-decoration:none|line-through|underline



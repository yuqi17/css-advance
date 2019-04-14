

#### 1. 如果两个元素是兄弟关系,那么其中一个设置了relative,另外一个也最好设置,因为它们的z-index 层次不一样了
#### 2. flex 布局会影响position 定位 特别是居中
#### 3. 设置position 定位 最好明确默认值和不设置的区别,建议设置top left.
#### 4. flex 布局 justify-content 默认值是flex-start, align-items 默认值是 stretch
#### 5. flex item 的默认值 flex 属性是 0 1 auto   flex-grow、flex-shrink 和 flex-basis 属性的简写属性。 
#### 6. css 属性 关键字unset all revert initial inherit  [参考]( http://www.cnblogs.com/xiaohuochai/p/5464456.html)
#### 7. none 和 auto 自适应的意思 (要看实际情况) [参考 margin:auto](http://zh.learnlayout.com/margin-auto.html)
#### 8. [js 正宗读取 css 样式的办法,可以用来验证css语法](https://blog.csdn.net/k358971707/article/details/54590490)
#### 9. point-events:none 只有再z-index 不为-1,且是父子节点的情况下生效

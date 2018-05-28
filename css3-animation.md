
### animation的基本设置：

``` css
    animation: move 10s linear 0s infinite alternate running forwards;
```
alternate  表示是否反向播放动画
running|pause 表示是否暂停
forwards|表示动画是否在改变后不再回到初始状态

### 顺序动画的方案
- 1. 多个元素的顺序动画，用delay在不同的元素上设置，达到顺序执行。
- 2. 同一个元素的连续动画，用不同的class 样式，都设置animation 不同的动画，并用delay 区分次序。

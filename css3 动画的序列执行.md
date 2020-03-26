
```css
/* 一个元素顺序执行多个动画 */
.animate2{
  animation: move-forward,spin, change-bgcolor;
  animation-delay: 1s,2s,3s;
  animation-duration: 1s,1s,1s;
  animation-fill-mode: forwards;
}

```

```css
/* 一个元素同时执行多个动画 */
.animate11{
  animation: move-forward, change-bgcolor;
  animation-duration: 500ms,500ms;
  animation-fill-mode: forwards;
}

```

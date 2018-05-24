
``` css
    /*手机端点击出现阴影*/
    -webkit-tap-highlight-color: rgba(0,0,0,0);
    去掉浏览器默认样式
    /*多行文本...省略号  编译问题方案:https://www.cnblogs.com/richard1015/p/8526988.html*/
   -webkit-appearance:none;
     text-overflow: ellipsis;
    display: -webkit-box;
    /*!autoprefixer off*/
    -webkit-box-orient: vertical;
    -webkit-line-clamp: 2;
    /*!autoprefixer: on */ 
 
```

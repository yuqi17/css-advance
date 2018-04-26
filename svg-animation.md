
``` html
<svg class="squiggle-animated" width="580" height="400" xmlns="http://www.w3.org/2000/svg">
    <path d="m200.5,131c0,1 0,2 0,3c0,2 2,4 3,5c2,2 3.173096,
        3.852737 4,5c1.307449,1.813995 2,3 3,4c2,2 2.692551
        ,3.186005 4,5c0.826904,1.147263 1.61731,2.076126 2,3c0.541199,
        1.306564 2.458801,1.693436 3,3c0.38269,0.923874 0.61731,
        1.076126 1,2c0.541199,1.306564 1,1 2,2c0,0 0.292892,
        1.292892 1,2c0.707108,0.707108 1,1 1,1c1,0 1.292892,
        0.292892 2,1c0.707108,0.707108 0.292892,1.292892 1,2c0.707108,0.707108 1,
        0 1,0c0,0 0.173096,0.147263 1,
        -1c1.307449,-1.813995 2.415894,-3.761078 4,-7c1.389359,-2.840729 3.648865,-6.19577 6,
        -10c2.628662,-4.25325 6.729614,-9.228851 11,
        -14c3.772675,-4.215088 9.232727,-8.733246 15,-14c3.132874,-2.860977 7,
        -7 11,-11c3,-3 6,-6 9,-9c3,-3 5.323669,-4.520164 7,
        -6c2.703003,-2.386162 4,-4 6,-6c1,-1 3,-3 4,-4c1,-1 2,-2 2,-2c1,-1 2,-2 2,-2l0,0" id="svg_1" stroke-width="20" stroke="#0f0"
        fill="none" />
</svg>
<style>
    path {
        stroke-dasharray: 166.20498657226562;
        /* stroke-dasharray: 166.20498657226562,166.20498657226562; */
        stroke-dashoffset: 166.20498657226562;
        animation: dash 1s ease forwards;
        stroke-linecap: round;
        stroke-linejoin: round;
    }

    @keyframes dash {
        to {
            stroke-dashoffset: 0;
        }
    }
</style>
<!-- <script>
        var path = document.querySelector('.squiggle-animated path');
        var length = path.getTotalLength();
        console.log(length)
        path.style.transition = 'none';
        // 用于创建虚线
        path.style.strokeDasharray = length + ' ' + length;
        path.style.strokeDashoffset = length;
        path.getBoundingClientRect();
        path.style.transition = 'stroke-dashoffset .3s linear';
        path.style.strokeDashoffset = '0';
    </script> -->
<!-- 
    https://blog.csdn.net/ning0_o/article/details/54970474
    https://c.runoob.com/more/svgeditor/
-->
```

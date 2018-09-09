# day7-8
### 圣杯布局
1. 首先三者 float:left  ,position:relative;(后面需要用到相对定位拉扯各块)  
2. 中间部分用 width:100% 占满
3. 左块取margin-left：-100%（中间盒子的宽度取负），这样左盒子才可以往最左边移动。此时左块内容与中块左边重合并覆盖了中块内容  
  使用left:-300px将左块拉至最左。
4. 右块使用margin-left:-300px（自己的宽度取负）这样右盒子才可以在一行的最右边显示出自己。此时与中块右边重合并覆盖了中块内容  
   使用right:-300px将其向右拉至最右。
> **总结：**  圣杯布局，为了中间div内容不被遮挡，将中间div设置了左右padding-left和padding-right后，  
  将左右两个div用相对布局position: relative并分别配合right和left属性，以便左右两栏div移动后不遮挡中间div。

# ife-5  
零基础HTML及CSS编码（二）  
1.总体布局是横向两列,左列自适应,右列固定宽度:  
  解决方法:  
  第一种:右列向右浮动,左列让他自动向上,设置margin-right值为右列盒子宽度.(注意这需要html里右列内容先于左列内容出现).  
  第二种:左侧设置margin-right值为右列盒子宽度,右侧绝对定位position:absolute;top:0; right:0;(之所以可以这样做是因为左列自适应高度绝对比右列要高,父元素就不会凹陷).  
2.对于图片自适应:  
  图片外层加一层div或者在其他元素容器内,例如:   
  < div class="img_wrap">  
  < img src ="" />  
  < /div>  
  则相应css样式设置为如下:  
.img_wrap{  
  max-width:xxpx;  
}  
.img{  
  width:100%;  
  height:auto;(这一句可以让图片保持比例放大缩小)  
  }  

      

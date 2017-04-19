# 任务一：零基础JavaScript编码（一）

任务描述  
参考以下示例代码，补充其中的JavaScript功能，完成一个JavaScript代码的编写  
本任务完成的功能为：用户可以在输入框中输入任何内容，点击“确认填写”按钮后，用户输入的内容会显示在“您输入的值是”文字的右边  

任务注意事项  
实现简单功能的同时，请仔细学习JavaScript基本语法、事件、DOM相关的知识  
请注意代码风格的整齐、优雅  
代码中含有必要的注释  
可以不考虑输入的合法性  
建议不使用任何第三方库、框架  
示例代码仅为示例，可以直接使用，也可以完全自己重写  

出现的问题
(function() {
  var btn=document.getElementById("button");
  var text=document.getElementById("aqi-input").value;
  /*一开始没留意就将这一句写在事件处理程序函数外了,这样会导致一直取到空值,这是因为页面加载完时,这个外层函数被执行了,然后此时的input框还是空值,而后绑定在button上的处理函数一直使用着这个值,一直不会没有重新取的当前input的值,所以一直显示空值*/
  btn.onclick=function(){
    var span=document.getElementById("aqi-display");
    span.innerHTML=text;
  }
})();

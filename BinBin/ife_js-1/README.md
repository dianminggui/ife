
(function() {

  var btn=document.getElementById("button");
  var text=document.getElementById("aqi-input").value;/*一开始没留意就将这一句写在事件处理程序函数外了,这样会导致一直取到空值,这是因为页面加载完时,这个外层函数被执行了,然后此时的input框还是空值,而后绑定在button上的处理函数一直使用着这个值,一直不会没有重新取的当前input的值,所以一直显示空值*/
  btn.onclick=function(){
    var span=document.getElementById("aqi-display");
    span.innerHTML=text;
  }
})();

# JS


## DOMContentLoaded 與 load 事件
<img src="./img/HTML%20load.png">

DOM load
```
document.addEventListener("DOMContentLoaded", function(){
  // DOM Ready!
});
```
全部元素 load
```
window.addEventListener("load", function(event) {
  // All resources finished loading!
});
```
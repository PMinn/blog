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
子母畫面(Pip)
```
function togglePictureInPicture() {
  if (document.pictureInPictureElement) {
    document.exitPictureInPicture();
  } else if (document.pictureInPictureEnabled) {
    video.requestPictureInPicture();
  }
}
```
click Event 阻止向下傳遞
```
e.stopPropagation();
```
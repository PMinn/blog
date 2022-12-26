# CSS

## 圖層混合模式
```
mix-blend-mode: difference;
```
[demo](https://developer.mozilla.org/en-US/docs/Web/CSS/mix-blend-mode)

## scrollbar
```
.mostly-customized-scrollbar::-webkit-scrollbar {
  width: 5px;
  height: 8px;
  background-color: #aaa; /* or add it to the track */
}

/* Add a thumb */
.mostly-customized-scrollbar::-webkit-scrollbar-thumb {
  background: #000;
}
```

## ios的100vh不是100vh
設定總高度，Child Element都用100%
```
@supports (-webkit-touch-callout: none) {
    body {
        min-height: -webkit-fill-available;
    }
}
```
---
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


## GSA
```
var ss = SpreadsheetApp.openByUrl("");
// or
var ss = SpreadsheetApp.getActiveSpreadsheet();

var sheet = ss.getSheetByName("sheet1");

return ContentService.createTextOutput(JSON.stringify({})).setMimeType(ContentService.MimeType.JSON); 
```
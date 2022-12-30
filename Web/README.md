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



---
# 框架
## Vue
```
#初始化專案
$ vue create [Name of your directory/folder aka App Name]
```
```
#開發版，本地開發(localhost)適用，進入http://localhost:8080可看到結果
$ npm run dev

#需要伺服器，下指令後只建置靜態資源，直接開啟index.html即可看到結果
$ npm run build
```
# 模板引擎
## ejs
```
ejs.render(ejs_str, data, options);
// => Rendered HTML string

ejs.renderFile(filename, data, options, function(err, str){
    // str => Rendered HTML string
});
```
```
<% '腳本'標籤，用於流程控制，不輸出。
<%_ 刪除其前面的空格符
<%= 輸出數據到模板（輸出是轉義 HTML 標籤）
<%- 輸出非轉義的數據到模板
<%# 註釋標籤，不執行、不輸出內容
<%% 輸出字串 '<%'

%> 一般結束標籤
-%> 刪除緊隨其後的換行符
_%> 將結束束標記背面的空格符刪除
```
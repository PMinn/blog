## GSA
```
var ss = SpreadsheetApp.openByUrl("");
// or
var ss = SpreadsheetApp.getActiveSpreadsheet();

var sheet = ss.getSheetByName("sheet1");

return ContentService.createTextOutput(JSON.stringify({})).setMimeType(ContentService.MimeType.JSON); 
```
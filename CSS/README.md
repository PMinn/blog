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
html {
    height: -webkit-fill-available;
}
```
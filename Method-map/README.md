# 2. map 函式 

### 關於map函式
- [官網連結](https://p5js.org/reference/#/p5/map)
- [試一試](https://linduke-lin.github.io/p5Js-Demo/Method-map/MapDemo.html)

### 說明:
- map 首先需要設定原始參數的範圍
- 並設定要設定的比例範圍
- 並輸入需要縮放的參數
- 透過 map 函式會將輸入的參數做等比例縮放

` map(輸入的參數 , 原始參數起始範圍, 原始參數結束範圍, 縮放起始範圍, 縮放結束範圍)`

### 例:
- 我們以`map(1,0,10,0,100)`為例
- 原始的範圍是`0~10`
- 我們要將它變成`0~100`
- `0~10`變成`0~100`則需要乘以10倍
- 因此我們需要縮放的`1`通過map函式的計算後，會變成`10`

[回首頁](https://github.com/LINDuke-Lin/p5Js-Demo)
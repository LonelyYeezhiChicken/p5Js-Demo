# 5. arc 函式 

### 關於arc函式
- [官網連結](https://p5js.org/reference/#/p5/arc)
-  [成品-open mode](https://linduke-lin.github.io/p5Js-Demo/Method-arc/ArcDemo-Open.html)
-  [成品-chord mode](https://linduke-lin.github.io/p5Js-Demo/Method-arc/ArcDemo-Chord.html)
-  [成品-pie mode](https://linduke-lin.github.io/p5Js-Demo/Method-arc/ArcDemo-Pie.html)

### 說明:
- 用途 : 在螢幕上畫一條 `弧線`
- 模式 : 
    1. OPEN : open semi-circle (半開圓形) -> 純粹弧線，並無閉鎖 
    2. CHORD : closed semi-circle (閉鎖半圓) -> 封閉式半圓
    3. PIE : a closed pie segment (圓餅圖) -> 封閉式圓餅圖
- 從起點到終點，程式皆由順時鐘繪製

` arc(x, y, w, h, start, stop, [mode], [detail])`

- x : 點的 x 軸
- y : 點的 y 軸
- w : 圓弧的寬度
- h : 圓弧的高度
- start : 起始的角度
- stop : 結束的角度
- [mode] : 模式(OPEN, CHORD, PIE) `非必填`
- [detail] : 指定圓弧的周長，默認為25，不可超過50 `非必填`

### OPEN 例:
- OPEN : open semi-circle (半開圓形) -> 純粹弧線，並無閉鎖 
```javaScript
// 從點(100, 150) 開始，劃出 200 x 200 的開放式半圓
arc(100, 150, 200, 200, 0, 10, OPEN);
```
- 結果 : 
<img src="https://github.com/LINDuke-Lin/p5Js-Demo/blob/main/Method-arc/img/open.png" width="200px" height="200px">

### CHORD 例:
- CHORD : closed semi-circle (閉鎖半圓) -> 封閉式半圓
- 與開放式的差異只在半圓口是否有黑線
```javaScript
// 從點(100, 150) 開始，劃出 200 x 200 的封閉式式半圓
arc(100, 150, 200, 200, 0, 10, CHORD);
```
- 結果 : 
<img src="https://github.com/LINDuke-Lin/p5Js-Demo/blob/main/Method-arc/img/chord.png" width="200px" height="200px">

### PIE 例:
- PIE : a closed pie segment (圓餅圖) -> 封閉式圓餅圖
```javaScript
// 從點(100, 150) 開始，劃出 200 x 200 的圓餅圖
arc(100, 150, 200, 200, 0, 10, PIE);
```
- 結果 : 
<img src="https://github.com/LINDuke-Lin/p5Js-Demo/blob/main/Method-arc/img/pie.png" width="200px" height="200px">


[回首頁](https://github.com/LINDuke-Lin/p5Js-Demo)
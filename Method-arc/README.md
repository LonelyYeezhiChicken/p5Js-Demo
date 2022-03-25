# 5. arc 函式 

### 關於arc函式
- [官網連結](https://p5js.org/reference/#/p5/arc)

### 說明:
- 用途 : 在螢幕上畫一條 `弧線`
- 模式 : 
    1. OPEN : open semi-circle (半開圓形) -> 純粹弧線，並無閉鎖 
    2. CLOSED : closed semi-circle (閉鎖半圓) -> 封閉式半圓
    3. PIE : a closed pie segment (圓餅圖) -> 封閉式圓餅圖
- 從起點到終點，程式皆由順時鐘繪製

` arc(x, y, w, h, start, stop, [mode], [detail])`

- x : 點的 x 軸
- y : 點的 y 軸
- w : 圓弧的寬度
- h : 圓弧的高度
- start : 起始的角度
- stop : 結束的角度
- [mode] : 模式(OPEN, CLOSED, PIE) `非必填`
- [detail] : 指定圓弧的周長，莫認為25，不可超過50 `非必填`


[回首頁](https://github.com/LINDuke-Lin/p5Js-Demo)
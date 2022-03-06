# 3. 區塊漸層 

### 最終結果
[結果連結](https://linduke-lin.github.io/p5Js-Demo/Gradient/Gradient.html)

<img src="https://github.com/LINDuke-Lin/p5Js-Demo/blob/main/Gradient/Gradient.png" width="200px" height="200px">

- [簡易作法 30~63行](https://github.com/LINDuke-Lin/p5Js-Demo/blob/main/Gradient/EasyGradient.html)

- [雙迴圈做法 30~40行](https://github.com/LINDuke-Lin/p5Js-Demo/blob/main/Gradient/Gradient.html)



### 1. 簡易作法
1. 首先將寬度除以五，來獲得五個區塊

```javaScript
let linePosition = width / 5;
```
2. 開始畫第一塊

```javaScript
    for (let i = 0; i < height; i++) {
        let resAmount = map(i, 0, height, 0, 255);
        stroke(resAmount, 100, 200);
        line(0, i, linePosition, i);
    }
```
3. 因為我們需要在每個區塊從上而下畫線，而且線需要漸層，所以使用map計算紅色
    - 由於i從上而下，所以i的範圍是0~畫布的高
    - 要轉換成RGB的範圍0~255
    - 這邊換算出來的是RGB中的R(紅色)
    - 由於隨著區塊增長要轉換的三原色起始位置需要越來越大
    - 因此將他乘以30的倍數

```javaScript
//區塊1
    let resAmount = map(i, 0, height, 0, 255);

//區塊2
    let resAmount = map(i, 0, height, 30, 255);

//區塊3
    let resAmount = map(i, 0, height, 60, 255);

//區塊4
    let resAmount = map(i, 0, height, 90, 255);

//區塊5
    let resAmount = map(i, 0, height, 120, 255);
```
4. 設定畫筆顏色(RGB)
    - 將每次計算後的紅色置入，其他兩色固定
    - 由於紅色隨著迴圈，數字會越來越大
    - 因此顏色會越來越偏紫色，藉此達到漸層效果

```javaScript
stroke(resAmount, 100, 200);
```
5. 畫線
    - 畫線的重點在於要由上而下 -> 所以起點與終點的y都帶入i
    - x軸則是需要從第一個區塊的起點畫到第二個區塊的起點
    - 所以我們用了剛剛算好的區塊(linePosition)
    - 例如: 第一塊就是要從0~第一塊的終點，第二塊則是需要從第一塊終點到第二塊起點

```javaScript
 //第一塊 (0 ~ 第一塊)
    line(0, i, linePosition, i);

//第二塊 (第一塊 ~ 第二塊)
    line(linePosition * 1, i, linePosition * 2, i);
            
//第三塊 (第二塊 ~ 第三塊)
    line(linePosition * 2, i, linePosition * 3, i);

//第四塊 (第三塊 ~ 第四塊)
    line(linePosition * 3, i, linePosition * 4, i);

//第五塊 (第四塊 ~ 第五塊)
    line(linePosition * 4, i, linePosition * 5, i);
```
---
### 2.雙迴圈做法
- 雙迴圈主要是將以上重複的程式精簡化

1. 紅色計算的精簡化
    - 由於RGB的範圍每次都是30的倍數
    - 因此我們將他*30

```javaScript
let resAmount = map(i, 0, height, position * 30, 255);
```
2. 並將劃線的點到點使用運算的方式

```javaScript
line(linePosition * position, i, linePosition * (position + 1), i);
```


[回首頁](https://github.com/LINDuke-Lin/p5Js-Demo)
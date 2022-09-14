# 1. 線條與迴圈
使用四個迴圈分別畫出四個區塊的橫線與直線

### 最終結果
[結果連結](https://lonelyyeezhichicken.github.io/p5Js-Demo/LineAndLoop/LineAndLoop.html)

<img src="https://github.com/LINDuke-Lin/p5Js-Demo/blob/main/LineAndLoop/Line.png" width="200px" height="200px">

### 圖表座標
<img src="https://github.com/LINDuke-Lin/p5Js-Demo/blob/main/LineAndLoop/LineXY.png" width="400px" height="400px">


### 定義畫布
- 使用變數宣告方式，分別宣告 width(寬度),height(高度)
- ` 將寬度設定為 400 `
- ` 將高度設定為 400 `

```javaScript
 function setup() {
      let width = 400;//定義寬度
      let height = 400;//定義高度
      createCanvas(width, height);//將變數帶入設定中
      console.log("寬: " + width + " , 高: " + height);//在console上面印出目前寬高
    }
```
### line()使用方式

```
 line(x1, y1, x2, y2);
 ```

 - (x1,y1) (x2, y2) 各別代表一個點的座標
 - 兩個點相連之後，會成為一條線

 ### 搭配for使用

 1. 左上角(直線):
    - 需要從下到上，由左而右畫出直線
    - 因此第一個點會從( 1 X 10 ,400/2) -> (10,200) 畫到 (1 X 10,0) -> (10,0)
    - for迴圈條件 -> 小於20的原因是因為，我們每次都將i X 10，整張畫布的寬是400切成一半為200

 ```javaScript
  for (let i = 1; i <= 20; i++) {
        fill(250);
        line(i * 10, height / 2, i * 10, 0);
      }
```

 2. 右上角(橫線):
    - 需要從上到下，由左而右畫出直線
    - 因此第一個點會從( 400/2, 1 X 10) -> (200,10) 畫到 ( 400,1 X 10) -> (400,10)
    - for迴圈條件 -> 小於20的原因是因為，我們每次都將i X 10，整張畫布的高是400切成一半為200

 ```javaScript
   for (let i = 1; i <= 20; i++) {
        fill(250);
        line(width / 2, i * 10, width, i * 10);
      }
```

 3. 左下角(橫線):
    - 需要從下到上，由左而右畫出直線
    - 因此第一個點會從( 0,400 - (1 X 10)) -> (0,390) 畫到 ( 400/2,400 - (1 X 10)) -> (200,390)
    - 用高度減掉 i X 10的原因是因為，我們要從邊界往上畫，因此需要從最大邊界每次往上減掉10

 ```javaScript
   for (let i = 1; i <= 20; i++) {
        fill(250);
        line(0, height - (i * 10), width / 2, height - (i * 10));
      }
```

 4. 右下角(直線):
    - 需要從下到上，由右而左畫出直線
    - 因此第一個點會從( 400 - (1 X 10),0 ) -> (390,0) 畫到 (  400 - (1 X 10),400/2 ) -> (390,200)
    - 用寬度減掉 i X 10的原因是因為，我們要從邊界往左畫，因此需要從最大邊界每次往上減掉10

 ```javaScript
   for (let i = 1; i <= 20; i++) {
        fill(250);
        line(width - (i * 10), height, width - (i * 10), height / 2);
      }
```

[回首頁](https://github.com/lonelyyeezhichicken/p5Js-Demo)

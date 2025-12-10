---
title: "FB/LD EV"
date: 2024-06-18
categories: ["Play単位", "メモ"]
tags: ["Batting", "Exit Velocity", "xwOBAcon", "Adjusted EV"]
---

Baseball SavantにEV（FB/LD）という指標が追加されました。
単純にFBとLDの打球速度の平均値であり、[打球分類ごとのEscape Velocity](/solving-baseball/analysis/escape-velocity-by-batted-ball-type/)で触れたように、打球速度を上げる意味がほとんどないゴロを打球速度の計算から除外することでより野球的に打球速度を捉えます。

Adjusted EVと考えは似ていますし、やっていることの分かりやすさは打球速度系の指標でもかなり上位かなとは思います。ただ、フライやライナーといった打球分類は客観的な分類が難しい部分もありますし、ある程度のノウハウがないリーグでこの指標を使うのは危険かもしれません。

性能としてはAdjusted EVと変わりません。xwOBAconを見れない環境での妥協案の一つとなるでしょう。

![FB/LD EV](/solving-baseball/images/120.png)
![FB/LD EV](/solving-baseball/images/121.png)
**同年度のwOBAconの記述力**

![FB/LD EV](/solving-baseball/images/122.png)
![FB/LD EV](/solving-baseball/images/123.png)
**翌年度のwOBAconの予測力**

![FB/LD EV](/solving-baseball/images/124.png)
![FB/LD EV](/solving-baseball/images/125.png)
**xwOBAcon**

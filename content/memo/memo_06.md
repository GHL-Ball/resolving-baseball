---
title: "Bat Trackingから投球を分析する"
date: 2025-09-06
categories: ["Pitch単位", "メモ"]
tags: ["Batting", "Pitching", "Bat Tracking", "タイミング"]
---

2025年のYearly Savant UpdateではBat Trackingがさらにその対象範囲を広げました。
打者のスイング情報がより増えたということは投球の分析が深まるということですので、新たに追加された変数を利用して投球の分析を行います。

投球はまず打者のスイングの有無で分岐します。今回はそのスイング有に対する分析を行います。

スイング時の投球の基本的な目標は打者が標準とする打点（Intercept Point）とバットの芯からズレることです。
そのズレをxz平面とy軸に分解します。xz平面はSavantだと選手トップページのMovementのやつです。

-![Savant Movement](/solving-baseball/images/63.png)

*この図、人気ですけど見ての通り現実の野球とは違う「平面」であることは忘れたくないですよね*

- [投球のDeceptionを指標化する](/solving-baseball/memo/memo_19/)

以前の記事で紹介したこの指標を使います。

y軸はいわゆる「奥行き」で、緩急、タイミングが関わってくる視点です。

こちらはIntercept Point(x)を固定効果として設定し、GAMでIntercept Point(y)の予測、その予測値との差分をTiming Deviationとして指標化します。

-![Savant Movement](/solving-baseball/images/172.png)

スクーバルを可視化するとこんな感じになります。
FFはより速く、CHはより遅く打者が感じています。

xz平面のズレとy軸のズレの関係性を示した図が以下になります。

-![Savant Movement](/solving-baseball/images/171.png)

xz平面のズレはy軸にも表れますし、y軸のズレはxz平面にも表れますのである程度の正の相関がある図になっています。

スクーバルはxz平面ではなくy軸のズレを主として失点を抑止していることが分かります。またセールのような投球フォームから軌道まで特殊な投手は打者が普段とは全く違ったスイング軌道で対応しようとしていることも示唆されています。

もっと精査し、得点価値とも結びつけられると、さらに高精度に野球を記述できる観点かと思います。
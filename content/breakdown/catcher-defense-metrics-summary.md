---
title: "捕手の守備指標まとめ"
date: 2024-02-29
categories: ["守備指標"]
tags: ["捕手", "ブロッキング", "盗塁阻止", "フレーミング", "リード"]
---

## 前置き

捕手のrWARやDRSに対する疑問(文句)を書きたくて、その前説として他サイトとの相違点をまとめていたらダラダラと重い前説になってしまったので分割します。前説としては重いですが指標説明系としては特に深掘りもしていないので軽いです。

次→[捕手のDRS,rWARの再考(問題提起](/resolving-baseball/posts/catcher-drs-rwar-reconsideration/)

---

## 三大データサイトでの捕手の守備評価指標

三大データサイトで**主力として扱われている捕手の守備のセイバー指標**についてまとめます。

---

### Baseball-Reference

Baseball-Reference(以降BR)ではBaseball Info Solutions(以降BIS)提供のDefensive Runs Saved(以降DRS)の構成要素を個人ページで全て確認できます。

![P.ベイリー個人ページ BR](/resolving-baseball/images/110.png)

*①P.ベイリー個人ページ(https://www.baseball-reference.com/players/b/bailepa01-field.shtml)*

ジャイアンツ期待の新人P.ベイリーの個人ページを例に捕手のDRS部分についてのみ確認します。

**Rpm**･･･Rair,Rrange,Rthrowの合計(頭文字を取ってARTとも言われる)
- **Rair**･･･明らかにゴロとはみなされない内野フライの処理の評価
- **Rrange**･･･Rairに分類されない打球に対する守備範囲(到達能力)の評価
- **Rthrow**･･･Rairに分類されない打球に到達した後の評価

**Rbnt**･･･バント処理の評価

**Rgood**･･･他で評価されない良いプレー、悪いプレーの評価

**RerC**･･･インサイドワーク面の評価

**RsbC**･･･盗塁抑止、阻止の評価

**RszC**･･･フレーミングの評価

**Rdrs**･･･上記指標(Rpm,Rbnt,Rgood,RerC,RsbC,RszC)の合計

頭文字にReferenceの？Runの？Rをつけて捕手のみの指標にはCatcherのCを末尾につけているので若干見づらいですが小文字の部分にのみ注目すれば分かりやすいとは思います(pmはプラスマイナスシステム)。

ちなみに**ブロッキングの評価はRgoodに含まれています**。「P.ベイリーは平均的な捕手と比較してフレーミングや盗塁阻止、打球処理やインサイドワーク面で失点を17点減らし、バント処理やブロッキングを主としたその他のプレーで失点を4点増やしたと推定されている」という見方です。

---

### FanGraphs

FanGraphs(以降FG)ではBIS提供のDRSの他にFRMというフレーミング指標を確認できます。

![P.ベイリー個人ページ FG](/resolving-baseball/images/111.png)

*②P.ベイリー個人ページ(https://www.fangraphs.com/players/patrick-bailey/27478/stats#fielding)*

DRSも確認できますが少し表記に違いがあります(RerCはrCERA=CatcherのERA、RgoodはrGFP=Good Fielding Plays)。打球処理に関わるRpm,Rbntは掲載されていないので合計してもズレが生じる点は注意が必要です。

また、同じフレーミング指標でもrSZの11に対してFRMは17.4と差を確認できますが、2019年3月のこの[記事](https://blogs.fangraphs.com/fangraphs-pitch-framing/)通り**BISのフレーミング指標は他より偏差が小さくなる算出方法**のようです。一応2019~2023シーズンも確認してみましたが相関係数0.93に対し標準偏差は6.6(FRM)と4.8(rSZ)とその傾向は変わっていません。

---

### Baseball Savant

Baseball SavantではMLB Advanced Media提供のStatcastデータから算出した守備指標を捕手では現在4つ確認できます。

![P.ベイリー個人ページ Savant](/resolving-baseball/images/112.png)

*③P.ベイリー個人ページ(https://baseballsavant.mlb.com/savant-player/patrick-bailey-672275?stats=statcast-r-catching-mlb)*

打球処理以外の**フレーミング**、**ブロッキング**、**盗塁阻止**の得点換算指標と**平均ポップタイム**の4つです。

**Baseball Savantは各指標の詳細まで確認できる**のが特徴です。

上記画像でもポップタイムなら握り替えの時間、フレーミングならコースごとの結果などが確認できますし、リーダーボードの方ではブロッキングのコースごとの結果や盗塁阻止のプレーごとの難易度、当該プレーの動画なども確認できます。

---

### やっていることは同じ

一つ一つの指標の詳細算出方法をまとめるのはキリがないし、公開されていない部分も多々あるのでやりませんが共通しているのは**平均的な捕手との差を推定している**ということです。(RerCについては微妙ですが…)

フレーミングなら様々な側面を考慮した**期待ストライク率(数)を算出し、実際のそれと比べ、その差を得点換算する**という形。ブロッキングでも盗塁阻止でも同じです。差が出るのは考慮する側面の違いや得点換算の部分や測定方法の違いなどが理由でしょうが、僕個人としては意義のある差だと思っています。投手fWAR vs rWAR、OAA+UZR vs DRSのような違いではないですが。

---

## 三大WAR算出サイトの捕手WAR(守備部分)

次は捕手のWARを構成している守備指標の各サイトの違いをまとめます。

---

### Baseball Reference

BRではDRSをWARの守備評価部分に使っていますが、捕手に関しては注意が必要です。

![P.ベイリー個人ページ WAR詳細](/resolving-baseball/images/113.png)

*④P.ベイリー個人ページ(https://www.baseball-reference.com/players/b/bailepa01.shtml)*

P.ベイリーのDRSは13です(画像①参照)がWARの守備評価部分RfieldとRposのうち、DRS部分であるRfieldでは2となっています。これは**フレーミングによる貢献のRszC 11が評価外**というのが理由です。捕手についてはDRS - RszCがrWARの構成要素ということです。

---

### FanGraphs

FGは**フレーミング指標FRMとDRSの盗塁阻止指標rSB(RsbC)**がWARの構成要素です。以前はブロッキング指標Runs on Passed Pitches(RPP)がサイトで確認でき、fWARにも採用されていましたが**現在はフレーミングと盗塁阻止のみで捕手の守備を評価**しています。

FGとしてはブロッキング指標を追加する意思はあるのでsavantのブロッキング指標あたりを遡って採用するとかは今後ありそうですかね。

---

### Baseball Prospectus

Baseball Prospectusはインサイドワーク面以外の考慮しうる全ての要素でWARを構成しています。

![P.ベイリー個人ページ BP](/resolving-baseball/images/114.png)

*P.ベイリー個人ページ(https://www.baseballprospectus.com/player/112687/patrick-bailey/)*

**FrmR(フレーミング)**、**BlkR(ブロッキング)**、**ThrR(盗塁阻止)**が捕手特有の守備評価指標ということでこの3つの合計値が**CDA(Catching defense added)**としてまとめられています。そしてCDAにその他の打球処理部分の**範囲指標RDA Runs(Range defense added - runs)**と**送球指標のBRR_ARM**を足したのが全体の守備評価指標**DRP(Deserved runs prevented)**で、このDRPがpWARの構成要素となっています。

---

### まとめると…

|  | rWAR | fWAR | pWAR |
|:---:|:---:|:---:|:---:|
| フレーミング | × | ○ | ○ |
| ブロッキング | ○ | × | ○ |
| 盗塁阻止 | ○ | ○ | ○ |
| 打球処理 | ○ | × | ○ |
| インサイドワーク | ○ | × | × |

*各WARの違い*

サイトごとの違いをまとめたのが上記の表です。

例えば**フレーミングが苦手のS.ペレスが通算rWAR 33.0に対してfWAR 15.3、pWAR 14.7と大きな差がある**のは守備評価部分の構成要素の違いが大きいです。この違いがどの程度有意義な違いかを考えてみたくてnoteを書いていたら重くなったので分割します。

次はその違いを生み出すRerCについて分かる範囲でいろいろ考えます。

次→[捕手のDRS,rWARの再考(問題提起](/resolving-baseball/posts/catcher-drs-rwar-reconsideration/)

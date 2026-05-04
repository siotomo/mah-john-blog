---
layout: post
title: "河（捨て牌）の表示テスト"
date: 2026-05-04
---

捨て牌の河を 6枚区切りで表示し、ツモ切り（背景色付き）と手出し（通常表示）を区別できるようにする。

CSS は `assets/main.scss` で `.river / .river-row / .tsumogiri` を定義しているので、HTML 側はクラスを付けるだけ。

---

## 例1: 1段（6枚）

```
東 南 [西] 北 [白] 中
   ※ [ ] はツモ切り
```

<div class="river">
  <div class="river-row">
    <img src="https://cdn.jsdelivr.net/gh/FluffyStuff/riichi-mahjong-tiles/Regular/Ton.svg" width="30" alt="東">
    <img src="https://cdn.jsdelivr.net/gh/FluffyStuff/riichi-mahjong-tiles/Regular/Nan.svg" width="30" alt="南">
    <span class="tsumogiri"><img src="https://cdn.jsdelivr.net/gh/FluffyStuff/riichi-mahjong-tiles/Regular/Shaa.svg" width="30" alt="西"></span>
    <img src="https://cdn.jsdelivr.net/gh/FluffyStuff/riichi-mahjong-tiles/Regular/Pei.svg" width="30" alt="北">
    <span class="tsumogiri"><img src="https://cdn.jsdelivr.net/gh/FluffyStuff/riichi-mahjong-tiles/Regular/Haku.svg" width="30" alt="白"></span>
    <img src="https://cdn.jsdelivr.net/gh/FluffyStuff/riichi-mahjong-tiles/Regular/Chun.svg" width="30" alt="中">
  </div>
</div>

---

## 例2: 3段（18枚、本格的な河）

東家の河の例。ツモ切りが混在する典型形。

<div class="river">
  <div class="river-row">
    <img src="https://cdn.jsdelivr.net/gh/FluffyStuff/riichi-mahjong-tiles/Regular/Pin9.svg" width="30" alt="9p">
    <img src="https://cdn.jsdelivr.net/gh/FluffyStuff/riichi-mahjong-tiles/Regular/Sou9.svg" width="30" alt="9s">
    <img src="https://cdn.jsdelivr.net/gh/FluffyStuff/riichi-mahjong-tiles/Regular/Ton.svg" width="30" alt="東">
    <span class="tsumogiri"><img src="https://cdn.jsdelivr.net/gh/FluffyStuff/riichi-mahjong-tiles/Regular/Pei.svg" width="30" alt="北"></span>
    <img src="https://cdn.jsdelivr.net/gh/FluffyStuff/riichi-mahjong-tiles/Regular/Haku.svg" width="30" alt="白">
    <span class="tsumogiri"><img src="https://cdn.jsdelivr.net/gh/FluffyStuff/riichi-mahjong-tiles/Regular/Hatsu.svg" width="30" alt="發"></span>
  </div>
  <div class="river-row">
    <img src="https://cdn.jsdelivr.net/gh/FluffyStuff/riichi-mahjong-tiles/Regular/Man1.svg" width="30" alt="1m">
    <img src="https://cdn.jsdelivr.net/gh/FluffyStuff/riichi-mahjong-tiles/Regular/Man2.svg" width="30" alt="2m">
    <span class="tsumogiri"><img src="https://cdn.jsdelivr.net/gh/FluffyStuff/riichi-mahjong-tiles/Regular/Man9.svg" width="30" alt="9m"></span>
    <img src="https://cdn.jsdelivr.net/gh/FluffyStuff/riichi-mahjong-tiles/Regular/Pin1.svg" width="30" alt="1p">
    <img src="https://cdn.jsdelivr.net/gh/FluffyStuff/riichi-mahjong-tiles/Regular/Pin8.svg" width="30" alt="8p">
    <img src="https://cdn.jsdelivr.net/gh/FluffyStuff/riichi-mahjong-tiles/Regular/Sou1.svg" width="30" alt="1s">
  </div>
  <div class="river-row">
    <img src="https://cdn.jsdelivr.net/gh/FluffyStuff/riichi-mahjong-tiles/Regular/Sou8.svg" width="30" alt="8s">
    <img src="https://cdn.jsdelivr.net/gh/FluffyStuff/riichi-mahjong-tiles/Regular/Pin2.svg" width="30" alt="2p">
    <img src="https://cdn.jsdelivr.net/gh/FluffyStuff/riichi-mahjong-tiles/Regular/Pin7.svg" width="30" alt="7p">
    <img src="https://cdn.jsdelivr.net/gh/FluffyStuff/riichi-mahjong-tiles/Regular/Sou2.svg" width="30" alt="2s">
    <span class="tsumogiri"><img src="https://cdn.jsdelivr.net/gh/FluffyStuff/riichi-mahjong-tiles/Regular/Sou7.svg" width="30" alt="7s"></span>
    <img src="https://cdn.jsdelivr.net/gh/FluffyStuff/riichi-mahjong-tiles/Regular/Pin3.svg" width="30" alt="3p">
  </div>
</div>

---

## 例3: ツモ切りの色を変える

`.tsumogiri` の `background-color` を inline style で上書きできる。注目させたい場面で使う。

<div class="river">
  <div class="river-row">
    <img src="https://cdn.jsdelivr.net/gh/FluffyStuff/riichi-mahjong-tiles/Regular/Pin9.svg" width="30" alt="9p">
    <img src="https://cdn.jsdelivr.net/gh/FluffyStuff/riichi-mahjong-tiles/Regular/Sou9.svg" width="30" alt="9s">
    <span class="tsumogiri" style="background-color: #fff3b0;"><img src="https://cdn.jsdelivr.net/gh/FluffyStuff/riichi-mahjong-tiles/Regular/Pei.svg" width="30" alt="北"></span>
    <img src="https://cdn.jsdelivr.net/gh/FluffyStuff/riichi-mahjong-tiles/Regular/Haku.svg" width="30" alt="白">
    <span class="tsumogiri" style="background-color: #ffd6d6;"><img src="https://cdn.jsdelivr.net/gh/FluffyStuff/riichi-mahjong-tiles/Regular/Sou1.svg" width="30" alt="1s"></span>
    <img src="https://cdn.jsdelivr.net/gh/FluffyStuff/riichi-mahjong-tiles/Regular/Chun.svg" width="30" alt="中">
  </div>
</div>

黄色は「リーチ宣言牌」、ピンクは「危険牌っぽい捨て」など、用途で色を変える運用が可能。

---

## 例4: 白の縁取り確認

白は背景と紛れやすいので、CSS で薄い縁取り（drop-shadow 2 重がけ）を当てている。河でも手牌でも自動適用される。

手牌の白3枚:

<p>
<img src="https://cdn.jsdelivr.net/gh/FluffyStuff/riichi-mahjong-tiles/Regular/Haku.svg" width="30" alt="白">
<img src="https://cdn.jsdelivr.net/gh/FluffyStuff/riichi-mahjong-tiles/Regular/Haku.svg" width="30" alt="白">
<img src="https://cdn.jsdelivr.net/gh/FluffyStuff/riichi-mahjong-tiles/Regular/Haku.svg" width="30" alt="白">
</p>

河の中でツモ切りされた白:

<div class="river">
  <div class="river-row">
    <img src="https://cdn.jsdelivr.net/gh/FluffyStuff/riichi-mahjong-tiles/Regular/Ton.svg" width="30" alt="東">
    <span class="tsumogiri"><img src="https://cdn.jsdelivr.net/gh/FluffyStuff/riichi-mahjong-tiles/Regular/Haku.svg" width="30" alt="白"></span>
    <img src="https://cdn.jsdelivr.net/gh/FluffyStuff/riichi-mahjong-tiles/Regular/Hatsu.svg" width="30" alt="發">
  </div>
</div>

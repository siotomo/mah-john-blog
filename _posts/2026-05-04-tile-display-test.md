---
layout: post
title: "麻雀牌の表示方法テスト"
date: 2026-05-04
---

ブログ記事内で麻雀牌をどう表現するか、複数の方式を並べて視認性を比較する。

サンプルは **国士無双の13面待ち**（各色1・9 + 字牌7種、全種類が登場）。

---

## 方式A: Unicode 麻雀牌（標準サイズ）

🀇🀏🀙🀡🀐🀘🀀🀁🀂🀃🀆🀅🀄

## 方式B: Unicode 麻雀牌（大きめ）

<p style="font-size: 2.5em; line-height: 1.2;">🀇🀏🀙🀡🀐🀘🀀🀁🀂🀃🀆🀅🀄</p>

## 方式C: テキスト記法 (mpsz)

`1m 9m 1p 9p 1s 9s 1z 2z 3z 4z 5z 6z 7z`

mpsz は m=萬子, p=筒子, s=索子, z=字牌(1=東/2=南/3=西/4=北/5=白/6=發/7=中)。麻雀界隈で標準的な表記。

## 方式D: SVG 画像 (FluffyStuff/riichi-mahjong-tiles, width=40)

<p>
<img src="https://cdn.jsdelivr.net/gh/FluffyStuff/riichi-mahjong-tiles/Regular/Man1.svg" width="40" alt="1m">
<img src="https://cdn.jsdelivr.net/gh/FluffyStuff/riichi-mahjong-tiles/Regular/Man9.svg" width="40" alt="9m">
<img src="https://cdn.jsdelivr.net/gh/FluffyStuff/riichi-mahjong-tiles/Regular/Pin1.svg" width="40" alt="1p">
<img src="https://cdn.jsdelivr.net/gh/FluffyStuff/riichi-mahjong-tiles/Regular/Pin9.svg" width="40" alt="9p">
<img src="https://cdn.jsdelivr.net/gh/FluffyStuff/riichi-mahjong-tiles/Regular/Sou1.svg" width="40" alt="1s">
<img src="https://cdn.jsdelivr.net/gh/FluffyStuff/riichi-mahjong-tiles/Regular/Sou9.svg" width="40" alt="9s">
<img src="https://cdn.jsdelivr.net/gh/FluffyStuff/riichi-mahjong-tiles/Regular/Ton.svg" width="40" alt="東">
<img src="https://cdn.jsdelivr.net/gh/FluffyStuff/riichi-mahjong-tiles/Regular/Nan.svg" width="40" alt="南">
<img src="https://cdn.jsdelivr.net/gh/FluffyStuff/riichi-mahjong-tiles/Regular/Shaa.svg" width="40" alt="西">
<img src="https://cdn.jsdelivr.net/gh/FluffyStuff/riichi-mahjong-tiles/Regular/Pei.svg" width="40" alt="北">
<img src="https://cdn.jsdelivr.net/gh/FluffyStuff/riichi-mahjong-tiles/Regular/Haku.svg" width="40" alt="白">
<img src="https://cdn.jsdelivr.net/gh/FluffyStuff/riichi-mahjong-tiles/Regular/Hatsu.svg" width="40" alt="發">
<img src="https://cdn.jsdelivr.net/gh/FluffyStuff/riichi-mahjong-tiles/Regular/Chun.svg" width="40" alt="中">
</p>

## 方式E: SVG 画像（width=60、ゆったり）

<p>
<img src="https://cdn.jsdelivr.net/gh/FluffyStuff/riichi-mahjong-tiles/Regular/Man1.svg" width="60" alt="1m">
<img src="https://cdn.jsdelivr.net/gh/FluffyStuff/riichi-mahjong-tiles/Regular/Man9.svg" width="60" alt="9m">
<img src="https://cdn.jsdelivr.net/gh/FluffyStuff/riichi-mahjong-tiles/Regular/Pin1.svg" width="60" alt="1p">
<img src="https://cdn.jsdelivr.net/gh/FluffyStuff/riichi-mahjong-tiles/Regular/Pin9.svg" width="60" alt="9p">
<img src="https://cdn.jsdelivr.net/gh/FluffyStuff/riichi-mahjong-tiles/Regular/Sou1.svg" width="60" alt="1s">
<img src="https://cdn.jsdelivr.net/gh/FluffyStuff/riichi-mahjong-tiles/Regular/Sou9.svg" width="60" alt="9s">
<img src="https://cdn.jsdelivr.net/gh/FluffyStuff/riichi-mahjong-tiles/Regular/Ton.svg" width="60" alt="東">
<img src="https://cdn.jsdelivr.net/gh/FluffyStuff/riichi-mahjong-tiles/Regular/Nan.svg" width="60" alt="南">
<img src="https://cdn.jsdelivr.net/gh/FluffyStuff/riichi-mahjong-tiles/Regular/Shaa.svg" width="60" alt="西">
<img src="https://cdn.jsdelivr.net/gh/FluffyStuff/riichi-mahjong-tiles/Regular/Pei.svg" width="60" alt="北">
<img src="https://cdn.jsdelivr.net/gh/FluffyStuff/riichi-mahjong-tiles/Regular/Haku.svg" width="60" alt="白">
<img src="https://cdn.jsdelivr.net/gh/FluffyStuff/riichi-mahjong-tiles/Regular/Hatsu.svg" width="60" alt="發">
<img src="https://cdn.jsdelivr.net/gh/FluffyStuff/riichi-mahjong-tiles/Regular/Chun.svg" width="60" alt="中">
</p>

---

## 補足: 順子の例（123m 456p 789s）

### Unicode

🀇🀈🀉 🀜🀝🀞 🀒🀓🀔

### SVG (width=40)

<p>
<img src="https://cdn.jsdelivr.net/gh/FluffyStuff/riichi-mahjong-tiles/Regular/Man1.svg" width="40" alt="1m">
<img src="https://cdn.jsdelivr.net/gh/FluffyStuff/riichi-mahjong-tiles/Regular/Man2.svg" width="40" alt="2m">
<img src="https://cdn.jsdelivr.net/gh/FluffyStuff/riichi-mahjong-tiles/Regular/Man3.svg" width="40" alt="3m">
&nbsp;
<img src="https://cdn.jsdelivr.net/gh/FluffyStuff/riichi-mahjong-tiles/Regular/Pin4.svg" width="40" alt="4p">
<img src="https://cdn.jsdelivr.net/gh/FluffyStuff/riichi-mahjong-tiles/Regular/Pin5.svg" width="40" alt="5p">
<img src="https://cdn.jsdelivr.net/gh/FluffyStuff/riichi-mahjong-tiles/Regular/Pin6.svg" width="40" alt="6p">
&nbsp;
<img src="https://cdn.jsdelivr.net/gh/FluffyStuff/riichi-mahjong-tiles/Regular/Sou7.svg" width="40" alt="7s">
<img src="https://cdn.jsdelivr.net/gh/FluffyStuff/riichi-mahjong-tiles/Regular/Sou8.svg" width="40" alt="8s">
<img src="https://cdn.jsdelivr.net/gh/FluffyStuff/riichi-mahjong-tiles/Regular/Sou9.svg" width="40" alt="9s">
</p>

---

## 比較

| 方式 | 視認性 | 軽さ | 編集の手軽さ | 備考 |
|------|--------|------|--------------|------|
| A: Unicode 標準 | △ | ◎ | ◎ | フォント依存。デバイスでバラつく |
| B: Unicode 大 | △〜◯ | ◎ | ◎ | サイズ拡大しても色は単色 |
| C: テキスト mpsz | ✕（記号） | ◎ | ◎ | 麻雀者には自然、ビジュアルなし |
| D: SVG 標準 | ◎ | ◯ | △ | 一枚ずつ `<img>` で書く |
| E: SVG 大 | ◎ | ◯ | △ | 大きく表示したい時用 |

実運用では **D 相当を Jekyll の `{% include %}` で短縮** すれば、`{% include hand.html tiles="1m 9m 1p 9p ..." %}` の1行で書けるようになる。

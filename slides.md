---
theme: default
title: IEがサポート外になったときに使用できるCSS
download: false
lineNumbers: true
background: https://source.unsplash.com/collection/94734566/1920x1080
class: 'text-center'
---

# IEがサポート外になったときに <br>使用できるCSS

<div class="pt-12">
  <span @click="$slidev.nav.next" class="px-2 py-1 rounded cursor-pointer" hover="bg-white bg-opacity-10">
    Press Space for next page <carbon:arrow-right class="inline"/>
  </span>
</div>

<div class="abs-br m-6 flex gap-2">
  <button @click="$slidev.nav.openInEditor()" title="Open in Editor" class="text-xl icon-btn opacity-50 !border-none !hover:text-white">
    <carbon:edit />
  </button>
  <a href="https://github.com/slidevjs/slidev" target="_blank" alt="GitHub"
    class="text-xl icon-btn opacity-50 !border-none !hover:text-white">
    <carbon-logo-github />
  </a>
</div>

---

# filter
CSSのみで被写体に影をつける [もっと詳しく](https://developer.mozilla.org/ja/docs/Web/CSS/filter)

<div class="grid grid-cols-2 gap-4">
<div>
  <img class="img-1" src="/public/img/gassyou_usagi.png">

  ```css
  img {
      filter: drop-shadow(10px 10px 0 #999999);
    }
  ```
</div>
<div>
  <img class="img-2" src="/public/img/gassyou_usagi.png">

  ```css
  img {
      filter: blur(3px);
  }
  ```
</div>

</div>

<style>
  img {
    width: 200px;
    height: auto;
    margin: 20px auto 0;
  }
  .img-1 {
    filter: drop-shadow(10px 10px 0 #999999);
  }
  .img-2 {
    filter: blur(3px);
  }
</style>
---

# object-fit: cover

スマホでもデスクトップのあらゆるサイズのスクリーンでも最適なサイズで表示されます。[デモ](https://codepen.io/DylanMacnab/pen/NjVXEe)

<div class="grid grid-cols-2 gap-4">
<div>
  <img class="img-1" src="/public/img/test1.png">

</div>
<div>
  <img class="img-2" src="/public/img/test2.png">

```css
  img {
    object-fit: cover;
  }
```

</div>

</div>

<style>
  img {
    width: auto;
    height: auto;
    margin: 20px auto 0;
  }
</style>
---

# grid

コードスニペットを使って、文字をハイライトさせることができます

<div class="grid-box">
  <div class="item item01">item01</div>
  <div class="item item02">item02</div>
  <div class="item item03">item03</div>
  <div class="item item04">item04</div>
  <div class="item item05">item05</div>
  <div class="item item06">item06</div>
</div>

<style>
.grid-box {
  display:grid;
  gap: 10px;
  margin-top: 10px;
}
.grid-box .item {
  padding: 15px;
  font-weight: bold;
}
.grid-box .item01 {
  grid-row: 1 / 2;
  grid-column: 1 / 2;
  background: #f6ffc5;
}
.grid-box .item02 {
  grid-row: 1 / 5;
  grid-column: 2 / 3;
  background: #bef5ff;
}
.grid-box .item03 {
  grid-row: 2 / 3;
  grid-column: 1 / 2;
  background: #c5ffc8;
}
.grid-box .item04 {
  grid-row: 3 / 4;
  grid-column: 1 / 2;
  background: #ffc5c5;
}
.grid-box .item05 {
  grid-row: 4 / 5;
  grid-column: 1 / 2;
  background: #f5c5ff;
}
.grid-box .item06 {
  grid-row: 5 / 6;
  grid-column: 1 / 3;
  background: #bcbbff;
}
</style>

---

# position: sticky
セクション毎に追従させることができる。<br>
position: fixed; と異なり、ウィンドウを基準に追従するのではなく、ブロックを基準にして追従します。


<div class="sticky-wrap">
  <div class="A-block sticky-block">
    <div class="sticky">A</div>
    <p class="ttl02">Aブロック</p>
    <p class="txt">ダミーテキストダミーテキストダミーテキスト<br> ダミーテキストダミーテキストダミーテキストダミーテキストダミーテキストダミーテキスト<br> ダミーテキストダミーテキストダミーテキストダミーテキストダミーテキストダミーテキストダミーテキストダミーテキスト</p>
    <p class="txt">ダミーテキストダミーテキストダミーテキスト<br> ダミーテキストダミーテキストダミーテキストダミーテキストダミーテキストダミーテキスト<br> ダミーテキストダミーテキストダミーテキストダミーテキストダミーテキストダミーテキストダミーテキストダミーテキスト</p>
    <p class="txt">ダミーテキストダミーテキストダミーテキスト<br> ダミーテキストダミーテキストダミーテキストダミーテキストダミーテキストダミーテキスト<br> ダミーテキストダミーテキストダミーテキストダミーテキストダミーテキストダミーテキストダミーテキストダミーテキスト</p>
  </div>
  <div class="B-block sticky-block">
    <div class="sticky">B</div>
    <p class="ttl02">Bブロック</p>
    <p class="txt">ダミーテキストダミーテキストダミーテキスト<br> ダミーテキストダミーテキストダミーテキストダミーテキストダミーテキストダミーテキスト<br> ダミーテキストダミーテキストダミーテキストダミーテキストダミーテキストダミーテキストダミーテキストダミーテキスト</p>
    <p class="txt">ダミーテキストダミーテキストダミーテキスト<br> ダミーテキストダミーテキストダミーテキストダミーテキストダミーテキストダミーテキスト<br> ダミーテキストダミーテキストダミーテキストダミーテキストダミーテキストダミーテキストダミーテキストダミーテキスト</p>
    <p class="txt">ダミーテキストダミーテキストダミーテキスト<br> ダミーテキストダミーテキストダミーテキストダミーテキストダミーテキストダミーテキスト<br> ダミーテキストダミーテキストダミーテキストダミーテキストダミーテキストダミーテキストダミーテキストダミーテキスト</p>
  </div>
  <div class="C-block sticky-block">
    <div class="sticky">C</div>
    <p class="ttl02">Cブロック</p>
    <p class="txt">ダミーテキストダミーテキストダミーテキスト<br> ダミーテキストダミーテキストダミーテキストダミーテキストダミーテキストダミーテキスト<br> ダミーテキストダミーテキストダミーテキストダミーテキストダミーテキストダミーテキストダミーテキストダミーテキスト</p>
    <p class="txt">ダミーテキストダミーテキストダミーテキスト<br> ダミーテキストダミーテキストダミーテキストダミーテキストダミーテキストダミーテキスト<br> ダミーテキストダミーテキストダミーテキストダミーテキストダミーテキストダミーテキストダミーテキストダミーテキスト</p>
    <p class="txt">ダミーテキストダミーテキストダミーテキスト<br> ダミーテキストダミーテキストダミーテキストダミーテキストダミーテキストダミーテキスト<br> ダミーテキストダミーテキストダミーテキストダミーテキストダミーテキストダミーテキストダミーテキストダミーテキスト</p>
  </div>
</div>

<style>
  .sticky-wrap {
    height: 350px;
    overflow: scroll;
  }
  .sticky-block .sticky {
    background: #dfdfdf;
    font-weight: 700;
    margin-bottom: 20px;
    padding: 10px 15px;
    position: sticky;
    left: 0;
    top: -1px;
  }
</style>

---

# min()、max()、clamp()

<div></div>

<div class="title">min()</div>

値をカンマ区切りで指定しておくと、その中から最も小さい値を適用してくれます。[デモ](https://codepen.io/una/pen/rNeGNVL)

<div class="title">max()</div>

値をカンマ区切りで指定しておくと、その中から最も大きい値を適用してくれます。 [デモ](https://codepen.io/una/pen/RwaZXqR)

<div class="title">clamp()</div>

最小値、推奨値、最大値を指定でき、min()とmax()を組み合わせたような動きをしてくれます。[デモ](https://codepen.io/una/pen/bGpoGdJ)

<style>
  p {
    margin: 10px 0 30px;
  }
  .title {
    font-size: 1.5rem;
    font-weight: bold;
  }
</style>

---
layout: center
class: text-center
---

# 参考

[IEよ、さようなら😂 IEをサポート外にした時に使用できるCSSのプロパティや機能のまとめ](https://coliss.com/articles/build-websites/operation/css/css-properties-ie-is-not-supported.html)<br>
<br>
[IE非対応の便利なCSSプロパティ集](https://b-risk.jp/blog/2022/02/ie-unmatched-css/)

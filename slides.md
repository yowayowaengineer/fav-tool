---
theme: seriph
title: WeWork Engineer X Talk
info: |
  ## 私の推しツールを聞いてくれ！
  WeWork 日比谷パークフロント
  2025.01.22
class: text-center
transition: slide-left
mdc: true
fonts:
  sans: 'kokugl, M PLUS Rounded 1c'
  serif: 'kokugl, Sawarabi Mincho'
  local: 'kokugl'
---

# WeWork Engineer X Talk

## 私の推しツールを聞いてくれ！

<br>
<br>

WeWork 日比谷パークフロント

2025.01.22

<div @click="$slidev.nav.next" class="mt-12 py-1" hover:bg="white op-10">
  すたぁとぅ！ <carbon:arrow-right />
</div>

<style>
.slidev-layout {
  background-image: linear-gradient(35deg, #D422B1, #FFCE00) !important;
  background-size: 400% 400% !important;
  animation: GradientBackground 10s ease infinite;
}

@keyframes GradientBackground {
  0% {
    background-position: 0% 50%;
  }

  50% {
    background-position: 100% 50%;
  }

  100% {
    background-position: 0% 50%;
  }
};

</style>

---
transition: fade-out
---

# くらもと is 誰？

　

<span class="absolute top-25 left-20 text-2xl">グラデーション日和</span>
<Gravity class="flex absolute top-15 left-80 w-50" imgsrc="https://storage.googleapis.com/zenn-user-upload/wcau04bhl793ufoq5woj0978lrw6" />
<Gravity class="flex absolute top-5 right-100" message="FF好き（特にVとT）" />
<Gravity class="flex absolute top-10 right-70 text-3xl" message="vue-mo.js" />
<Gravity class="flex absolute top-15 right-20" message="鳥取県のハワイ" />
<Gravity class="flex absolute top-25 right-10 text-2xl" message="アプリ名『焼き鳥』事件😱" />
<img class="absolute top-35 right-30 w-50" src="https://cdn-ak.f.st-hatena.com/images/fotolife/s/so-technologies/20231023/20231023100011.png" />
<Gravity class="absolute top-40 left-5 w-50" imgsrc="https://appli.raku-za.jp/wp-content/themes/rakuzabiz/assets/img/logo01.png" />
<Gravity class="flex absolute top-40 left-60 text-4xl" message="イノベーション推進事業本部" />
<Gravity class="flex absolute top-50 left-80 text-3xl" message="デジタル推進部" />
<Gravity class="flex absolute top-50 right-100 text-2xl" message="部長" />
<Gravity class="flex absolute top-50 right-20 text-3xl" message="お菓子神社" />
<span class="absolute top-60 left-60 text-8xl">くらもと やすひろ</span>
<span class="absolute top-65 right-10 text-2xl">yum-yum COLOR</span>
<img class="absolute top-70 left-10 w-45" src="https://tech.pepabo.com/blog/2020/05/27/flutter-hands-on/flutter_logo.png" />
<Gravity class="flex absolute bottom-40 left-20 text-2xl" message="アプリコンテスト" />
<Gravity class="flex absolute bottom-50 left-70 text-xl" message="DBスペシャリスト" />
<Gravity class="flex absolute bottom-50 right-15 text-3xl" message="ITコーディネーター" />
<img class="absolute bottom-35 right-90 w-20" src="https://icon-icons.com/icons2/2415/PNG/512/vuejs_original_wordmark_logo_icon_146305.png" />
<span class="absolute bottom-25 left-40 text-3xl">色彩検定１級</span>
<Gravity class="flex absolute bottom-10 left-10 text-4xl" message="わさび豆" />
<Gravity class="flex absolute bottom-20 right-120 text-2xl" message="岡山県" />
<Gravity class="flex absolute bottom-25 right-80" message="ソフトボール" />
<span class="absolute bottom-35 left-80 text-2xl">gradient_like_css</span>
<Gravity class="flex absolute bottom-30 right-20 w-35" imgsrc="https://blog.yumyumcolor.com/assets/images/screen-off-girl/logo.png" />
<Gravity class="flex absolute bottom-10 right-120" message="読売オープン" />
<Gravity class="flex absolute bottom-15 right-40 text-2xl" message="よわよわエンジニア" />

<style>
h1 {
  background-color: #2B90B6;
  background-image: linear-gradient(45deg, #4EC5D4 10%, #146b8c 20%);
  background-size: 100%;
  -webkit-background-clip: text;
  -moz-background-clip: text;
  -webkit-text-fill-color: transparent;
  -moz-text-fill-color: transparent;
}
</style>

---
transition: slide-up
level: 2
layout: image-right
image: https://blog.yumyumcolor.com/assets/images/shikisai-kentei/color-card.jpg
---

# グラデーションにまつわるツール

　
<br>
<br>

色彩検定を受験する際に、実技がたいへん。

テキスト上のパターンだけでは

<span v-mark.circle.orange="1">イメージがわきづらかった</span>。

<br>

そこで作ったのが <span v-mark.red="2">[yum-yum COLOR](https://yumyumcolor.com/)</span> です。

<style>
h1 {
  background-color: hsl(355,79%,67%);
  background-image: linear-gradient(317deg,hsl(355,79%,67%),hsl(47,98%,50%));
  background-size: 85%;
  -webkit-background-clip: text;
  -moz-background-clip: text;
  -webkit-text-fill-color: transparent;
  -moz-text-fill-color: transparent;
}
</style>

---
transition: slide-up
---

# ランダムにグラデーションを生成したい

　
<br>
<br>

スライドの最初にお見せしたグラデーションのアニメーション。

あれは <span v-mark.circle.orange="1">[FUZE](https://fuze.8bit.codes/) という Web サービスで作成</span> しました。

<div v-click="2">

<br>

好みのグラデーションを簡単に作りたい……

そんなときに <span v-mark.red="3">[グラデーション日和](https://fav-gradation.yumyumcolor.com/)</span> がおすすめです！

</div>

<style>
h1 {
  background-color: hsl(132,71%,69%);
  background-image: linear-gradient(260deg,hsl(132,71%,69%),hsl(195,83%,64%));
  background-size: 50%;
  -webkit-background-clip: text;
  -moz-background-clip: text;
  -webkit-text-fill-color: transparent;
  -moz-text-fill-color: transparent;
}
</style>

---
transition: fade-out
class: text-center
---

# CSSを編集するエディター

　
<br>
<br>
<br>
<br>

<div v-click class="text-5xl">

Chrome !!

<br>

（開発者ツール）

</div>

<style>
h1 {
  background-color: hsl(56,79%,80%);
  background-image: linear-gradient(86deg,hsl(56,79%,80%),hsl(172,24%,36%));
  background-size: 100%;
  -webkit-background-clip: text;
  -moz-background-clip: text;
  -webkit-text-fill-color: transparent;
  -moz-text-fill-color: transparent;
}
</style>

---
layout: image-right
image: https://cover.sli.dev
---

# Flutterにおけるグラデーション

　
<br>
<br>

`Flutter`でのグラデーションって

<span v-mark.circle.orange="1">非常に可読性が低い</span>。

わかりやすい例が [こちら](https://qiita.com/azukisiromochi/items/bedf81bae8f0470c58a3#comment-02a8b58a5f0ca3ca95c5) 。

<div v-click="2">

<br>

そこでできたのが <span v-mark.red="3">[gradient_like_css](https://pub.dev/packages/gradient_like_css)</span> だ！

</div>

<style>
h1 {
  background-color: hsl(207,78%,65%);
  background-image: linear-gradient(120deg,hsl(207,78%,65%),hsl(3,96%,81%));
  background-size: 100%;
  -webkit-background-clip: text;
  -moz-background-clip: text;
  -webkit-text-fill-color: transparent;
  -moz-text-fill-color: transparent;
}
</style>

---

# gradient_like_css によるコードの変化

```css
/* With CSS */
div { background: linear-gradient(162.42deg, #FFE5C5 17.61%, #D2B38B 50.22%, #F1DDC3 83.52%); }
```

````md magic-move {lines: true}
```ts {*|4-5|6-12|13-19|*}
/// With Flutter
decoration: BoxDecoration(
  gradient: LinearGradient(
    begin: Alignment(-0.5, -1),   // 計算めんどうで適当です
    end: Alignment(0.5, 1),       // （同上）
    colors: [
      const Color(0xffFFE5C5),
      const Color(0xffFFE5C5),
      const Color(0xffD2B38B),
      const Color(0xffF1DDC3),
      const Color(0xffF1DDC3),
    ],
    stops: const [
      0,
      0.1761,
      0.5022,
      0.8352,
      1,
    ],
  ),
),
```

```ts
/// Using gradient_like_css
decoration: BoxDecoration(
  gradient: linearGradient(162.42, ['#FFE5C5 17.61%', '#D2B38B 50.22%', '#F1DDC3 83.52%']),
),
```
````

<div v-click="6">

<br>
<br>

<span v-mark.circle.orange="6">見やすいね！！</span>

（ `CSS` 使っている人なら）

</div>

<style>
h1 {
  background-color: hsl(259,93%,57%);
  background-image: linear-gradient(37deg,hsl(259,93%,57%),hsl(175,53%,51%));
  background-size: 75%;
  -webkit-background-clip: text;
  -moz-background-clip: text;
  -webkit-text-fill-color: transparent;
  -moz-text-fill-color: transparent;
}
</style>

---
transition: slide-up
class: text-center
level: 2
---

# まとめる！

　
<br>
<br>

グラデーションにまつわる（まつわらないものも）推しツールを紹介してきました。

AI とかもあるけど、世の中にあるものだけじゃ絶妙にマッチしない…

<div v-click>

<br>

<GradientTitle 
  class="text-4xl" 
  message="けど……！" 
  background-color="linear-gradient(37deg,hsl(259,93%,57%),hsl(175,53%,51%))" 
  />

</div>

<style>
h1 {
  background-color: hsl(350,98%,49%);
  background-image: linear-gradient(311deg,hsl(350,98%,49%),hsl(253,49%,81%));
  background-size: 100%;
  -webkit-background-clip: text;
  -moz-background-clip: text;
  -webkit-text-fill-color: transparent;
  -moz-text-fill-color: transparent;
}
</style>

---
transition: slide-up
layout: center
class: text-center
---

<GradientTitle 
  class="text-4xl" 
  message="そんな時は自分で作っちゃえ！" 
  background-color="linear-gradient(317deg,hsl(355,79%,67%),hsl(47,98%,50%))" 
  />

<br>

<GradientTitle 
  class="text-4xl" 
  message="車輪の再開発なんてくそくらえ" 
  background-color="linear-gradient(317deg,hsl(355,79%,67%),hsl(47,98%,50%))" 
  />

<div v-click>

<span class="text-2xl">（ ~~良い子のみんなは業務で真似しちゃだめだぞ~~ ）</span>

</div>

---
transition: slide-up
layout: center
class: text-center
---

<GradientTitle 
  class="text-5xl" 
  style="font-family: Sawarabi Mincho" 
  message="好きなものを好きなように作る――" 
  background-color="linear-gradient(311deg,hsl(350,98%,49%),hsl(253,49%,81%))" 
  />

<br>

<GradientTitle 
  class="text-5xl" 
  style="font-family: Sawarabi Mincho" 
  message="それが……" 
  background-color="linear-gradient(311deg,hsl(350,98%,49%),hsl(253,49%,81%))" 
  />

---
transition: fade-out
layout: center
class: text-center
---

<span class="text-9xl bang" style="font-family: kssweetheavycalligraphy">エンジニアだろ！！</span>

<style>
.bang {
  display: inline-block;
  animation: hurueru .1s infinite;
}

@keyframes hurueru {
  0% {transform: translate(0px, 0px) rotateZ(0deg)}
  25% {transform: translate(2px, 2px) rotateZ(1deg)}
  50% {transform: translate(0px, 2px) rotateZ(0deg)}
  75% {transform: translate(2px, 0px) rotateZ(-1deg)}
  100% {transform: translate(0px, 0px) rotateZ(0deg)}
}
</style>

---
transition: fade-out
---

# 紹介した推しツール

　

LTで登場した推しツールを紹介！

|                                                                     |                                                            |
| ------------------------------------------------------------------- | ---------------------------------------------------------- |
| [FUZE](https://fuze.8bit.codes/)                                    | グラデーションのアニメーションを生成するサイト             |
| [Wappalyzer](https://www.wappalyzer.com/)                           | 閲覧しているサイトに使われている技術を調べるChrome拡張     |
| [yum-yum COLOR](https://yumyumcolor.com/)                           | PCCS を用いた配色を生成するサイト（自作）                  |
| [グラデーション日和](https://fav-gradation.yumyumcolor.com/)        | ランダムなグラデーションを生成するサイト（自作）           |
| [Chrome DevTools](https://developer.chrome.com/docs/devtools?hl=ja) | Chromeの開発者ツール                                       |
| [gradient_like_css](https://pub.dev/packages/gradient_like_css)     | CSSのようにグラデーションを書けるFlutterプラグイン（自作） |
| [Slidev](https://sli.dev/)                                          | Vue3 & Vite 制のスライドツール                             |

<style>
h1 {
  background-color: #FFE5C5;
  background-image: linear-gradient(162.42deg, #FFE5C5 17.61%, #D2B38B 50.22%, #F1DDC3 83.52%);
  background-size: 40%;
  -webkit-background-clip: text;
  -moz-background-clip: text;
  -webkit-text-fill-color: transparent;
  -moz-text-fill-color: transparent;
}
</style>
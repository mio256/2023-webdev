# 見栄えをよくしよう
HTMLで作った簡単なページを作っていただきましたが，白黒のみでなんだか寂しいです．この章ではCSSを使って装飾を施していきます．

## CSSとは
CSSとは**C**ascading **S**tyle **S**heetsの略であり，Webページのスタイル（外観）を設定するコードです．CSSはHTMLの要素に対してスタイルを適用可能です．詳しくは[こちら](https://developer.mozilla.org/ja/docs/Learn/Getting_started_with_the_web/CSS_basics)．

## CSSファイルを設定する
先ほど作成した`first.html`の`<head>`要素内に以下のコードを書き加えます．
```html
<link href="style.css" rel="stylesheet">
```
このコードにより`style.css`がHTMLファイルに適用されます．

## CSSファイルを作成する
`first.html`の中で`style.css`を適用します，と宣言したので，`style.css`を作成します．そして以下の内容を追加します．
```css
body {
    color: black;
    background-color: white;
}
h1 {
    font-size: 30px;             
    border-bottom-width: 10px;
    border-bottom-style: solid; 
    border-bottom-color: blue;  
}
h2 {
    font-size: 24px;            
    border-bottom-width: 10px;  
    border-bottom-style: solid; 
    border-bottom-color: green; 
}
```
`body{ ... }`，`h1{ ... }`とありますが，これは`first.html`に記述した`<body>`要素や`<h1>`要素にそれぞれ対応しており，それぞれの要素ごとに色々な設定をしています．

## 設定内容について
### 色
`color`で文字の色，`background-color`で背景の色，`border-bottom-color`で下線の色を設定することができます．色は，`blue`や`red`など色を表す英語のキーワードを使うことができます．使用可能は色は[こちら](https://developer.mozilla.org/ja/docs/Web/CSS/named-color)を参照してみてください．  
また，このようなカラーコードの文字列`#FF0000`も使用可能です．

### 大きさ・太さ
`font-size`では文字の大きさ，`border-bottom-width`では下線の太さを数値で設定することができます．

### 線の種類
`border-bottom-style`では下線の種類を設定できます．設定値は，
- `solid`: 実線
- `double`: 二重線
- `dotted`: 点線
- `dashed`: 破線
などがあります．詳しくは[こちら](https://developer.mozilla.org/ja/docs/Web/CSS/border-bottom-style)．

## Work2
ここまでの内容をもとに先ほど作成した自分の自己紹介のページに装飾を施します．色や文字の大きさなどの設定値を変えて独自のページを作ります．先ほど作成した`style.css`を編集して設定値を変更してみましょう．
  
[次のページ](main-enhance.md)
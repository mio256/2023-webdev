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

  
[次のページ](main-enhance.md)
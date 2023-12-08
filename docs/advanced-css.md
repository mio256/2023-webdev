# モダンなWebページを作ろう

みなさんが普段目にするWebページは細部までデザインにこだわっていたり、ウィンドウの大きさに合わせてデザインが変わるようなレスポンシブデザインのものが多いと思います。

そのようなWebページをすべて0からCSSを書いて作るのは大変ですよね。

少ない手間で整ったデザインを行うには **フレームワーク** を利用することが効果的です。

ここでは、世界でも最も利用されているフロントエンドWebアプリケーションフレームワーク **Bootstrap** を使ってみましょう。

## 余白を作ろう

![スクリーンショット 2023-12-08 16 03 31](https://github.com/gdsc-kyutech/2023-webdev/assets/71450182/a8d1020b-cced-48d5-be93-ac7c354473c5)

みなさんの現在のWebページは、このように余白がないレイアウトになっていると思います。

下のコードのように、 `レスポンシブ対応` `Bootstrap CSS` `Bootstrap JS` の3行を追加すると、Bootstrapを導入することができます。

```html
<!DOCTYPE html>
<html lang="ja">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1"> <!-- レスポンシブ対応 -->
    <link href="style.css" rel="stylesheet">
    <title>はじめてのWebページ</title>
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/css/bootstrap.min.css" rel="stylesheet"
        integrity="sha384-9ndCyUaIbzAi2FUVXJi0CjmCapSmO7SnpJef0486qhLnuZ2cdeRhO02iuK6FUUVM" crossorigin="anonymous"> <!-- Bootstrap CSS -->
</head>

<body>
    <h1>はじめてのWebページ</h1>
    <p>こんにちは，GDSC Kyutechです．</p>
    <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/js/bootstrap.bundle.min.js"
        integrity="sha384-geWF76RCwLtnZ8qwWowPQNguL3RmwHVBC9FhGdlKrxdiJJigb/j/68SIy3Te4Bkz"
        crossorigin="anonymous"></script> <!-- Bootstrap JS -->
</body>

</html>

```

しかし、ただBootstrapを導入しただけではデザインは変わりません。

まずは、[コンテナ](https://getbootstrap.jp/docs/5.3/layout/containers/) を使ってみましょう。

下のコードのように、`body` に `<div class="container">` を追加し、その中に `h1` と `p` を入れます。

このときに、`<div class="container">` を閉じるために `</div>` を忘れないでください。

``` html
<body>
    <div class="container"> <!-- Content Start -->
        <h1>はじめてのWebページ</h1>
        <p>こんにちは，GDSC Kyutechです．</p>
    </div> <!-- Content End -->

    <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/js/bootstrap.bundle.min.js"
        integrity="sha384-geWF76RCwLtnZ8qwWowPQNguL3RmwHVBC9FhGdlKrxdiJJigb/j/68SIy3Te4Bkz"
        crossorigin="anonymous"></script>
</body>
```

![スクリーンショット 2023-12-08 16 16 12](https://github.com/gdsc-kyutech/2023-webdev/assets/71450182/2a60c376-3303-4a97-96c2-b148bfe2b49a)

このように、余白のあるレイアウトに変更されました！

さらに、Bootstrapはレスポンシブデザインに対応しているため、ウィンドウサイズを変更すると…

![スクリーンショット 2023-12-08 16 17 41](https://github.com/gdsc-kyutech/2023-webdev/assets/71450182/bacf58b4-c01c-4c9b-8fca-49c9f44840f5)

そのウィンドウサイズに合わせて適切な余白に変更されます！

コンテナの大きさを変えることもできるので、 [Bootstrap公式Docs（コンテナ）](https://getbootstrap.jp/docs/5.3/layout/containers/) を参考に変更してみましょう！

> [!WARNING]
> うまく行かない場合は、以下のような原因が考えられます。
> 
> 1. インターネットに接続されていない
> 
>    BootstrapはCDNと呼ばれる仕組みを用いているため、通常オフラインでは使用できません。
> 
> 2. 再読み込みされていない
> 
>    Webページを編集した際には再読み込みをしてください。
> 
> 3. 自分のCSSが邪魔をしている
> 
>    自作CSSの内容によってはBootstrapと競合を起こすことがあります、一度自作CSSをコメントアウトしてみてください。
> 
>    ```html
>    <head>
>      ...
>      <!-- <link href="style.css" rel="stylesheet"> -->
>      ...
>    </head>
>    ```
>
> うまく行かない場合や、わからないことがある場合は気軽にお近くのCore-teamメンバーに声をかけてください！

## 画像を配置しよう

まずは、普通に画像を入れてみましょう。

```html
    <div class="container">
        <h1>はじめてのWebページ</h1>
        <p>こんにちは，GDSC Kyutechです．</p>
        <img src="https://http.cat/200"></img> <!-- 画像の表示 -->
    </div>
```

十分に大きなウィンドウサイズでは問題ありませんが、小さいウィンドウサイズでははみ出してしまいます。

![スクリーンショット 2023-12-08 16 43 21](https://github.com/mio256/2023-webdev/assets/71450182/9e8b436a-9d8e-4bdc-8bd2-cf32e0e322e6)

レスポンシブデザインに対応していないWebページでは、このようにウィンドウサイズを考えないレイアウトになってしまいます。

ここでBootstrapの出番です。

[イメージ - レスポンシブな画像](https://getbootstrap.jp/docs/5.3/content/images/#%e3%83%ac%e3%82%b9%e3%83%9d%e3%83%b3%e3%82%b7%e3%83%96%e3%81%aa%e7%94%bb%e5%83%8f) を参考に、`img`タブを`class="img-fluid"`にしましょう。

```html
        <img src="https://http.cat/200" class="img-fluid"></img> <!-- 画像の表示 -->
```

そうすると、ウィンドウサイズに合わせて画像の大きさが変わるようになります！

サイズ指定や配置などを [BootstrapDocs イメージ](https://getbootstrap.jp/docs/5.3/content/images) を参考に変更してみましょう！

> [!TIP]
> 今回使用した猫の画像は [HTTP Cats](https://http.cat/) と呼ばれる、`HTTP ResponseStatusCode` を猫の画像に置き換えてくれる `WebAPI` です。
>
> HTTP ResponseStatusCodeについては、 [MDN Web Docs - HTTP Status](https://developer.mozilla.org/ja/docs/Web/HTTP/Status) を読んでみましょう。
>
> WebAPIについては、 [MDN Web Docs - WebAPI](https://developer.mozilla.org/ja/docs/Learn/JavaScript/Client-side_web_APIs/Introduction) を読んでみましょう。

## テーブルを自分で作ってみよう

ここまでの内容で、Bootstrapの使い方がわかってきたと思います。

それでは、ここからは出題形式です。

下の画像のような表を [Bootstrap Tables](https://getbootstrap.jp/docs/5.3/content/tables/) を参考に自分で作ってみましょう！

![スクリーンショット 2023-12-08 17 01 40](https://github.com/mio256/2023-webdev/assets/71450182/90c48a87-6d3a-4349-88da-8e9e9d526c18)

<details>

<summary>ヒント - わからない方へ</summary>

### BootstrapDocs を読んでみよう

以下のリンクから BootstrapDocs Tables を読んでみましょう！

https://getbootstrap.jp/docs/5.3/content/tables/#%e6%a6%82%e8%a6%81 

**概要** という名前の段落にサンプルコードがあるので、右上のコピーボタンからコピーすることができます！

</details>

表を作ることができたら、 [Bootstrap Tables バリエーション](https://getbootstrap.jp/docs/5.3/content/tables/#%e3%83%90%e3%83%aa%e3%82%a8%e3%83%bc%e3%82%b7%e3%83%a7%e3%83%b3) を参考に色付けをしましょう！

![スクリーンショット 2023-12-08 17 07 18](https://github.com/mio256/2023-webdev/assets/71450182/6976e8e4-8f96-4f87-88e8-b8dd7507c12c)

<details>

<summary>ヒント - わからない方へ</summary>

### どこに色が付いているかを見よう

1. 表題  
   `# First Last Handle` の行、つまり表題は青色ですね。  
   Bootstrapでは青色のデザインが`primary`と定義されています。
3. セル  
   `@twitter` のセルは赤色ですね。
   Bootstrapでは赤色のデザインが`danger`と定義されています。

</details>

[Bootstrap Tables](https://getbootstrap.jp/docs/5.3/content/tables/) には他にも色々なオプションがあるため、気に入ったものを試してみましょう！

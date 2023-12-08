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

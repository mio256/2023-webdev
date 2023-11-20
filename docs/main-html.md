# 自己紹介のページを作ろう
まずは簡単なページを作ってみましょう．

## HTMLについて
HTMLは**H**yper**T**ext **M**arkup **L**anguageの略で，Webページのコンテンツの構造を定義するために使う言語です．コンテンツは，見出しや段落，箇条書きのリスト，画像，表などの組み合わせで構成されています．  
実際にHTMLを使ってみましょう．

## HTMLファイルを作成する
基本的に1つのWebページにつき1つのファイルを作成します．
> [!IMPORTANT]
> - ここからは[Visaul Studio Code](https://code.visualstudio.com/)がインストールされている前提で話を進めます．インストール方法がわからない方はお近くのCore-teamメンバーにお声がけください．
> - Windows 11での操作方法しか記載していませんので，Windows 11以外を利用されている方はご自身の環境に合わせて操作してください．

1. デスクトップに新しく`webdev`というフォルダを作成します
2. 作成したフォルダを開きます
3. 右クリックして「Codeで開く」を選択
4. 新しいファイル`self-intro.html`を作成します
5. 作成した`self-intro.html`を開いてください

## HTMLのコードを書く
先ほど作成した`self-intro.html`に以下のコードを追加してください．
```html
<!DOCTYPE html>
<html lang="ja">
  <head>
    <meta charset="UTF-8">
    <title>はじめてのWebページ</title>
  </head>
  <body>
    <h1>はじめてのWebページ</h1>
    <p>こんにちは．GDSC Kyutechです．</p>
  </body>
</html>
```

[次のページ](main-css.md)
# Webページを充実させよう
Webページには，画像やリンク，YouTubeが埋め込まれていたり，別のページに遷移したり多くのコンテンツがあります．このページでは一部ではありますがそれらの使い方をご紹介します．

## 画像
画像を挿入することができます．`src=`には挿入したい画像ファイル名を，`width=`には，表示するときの画像の横幅の長さを指定します．
```html
<img src="test.png" width="300">
```
> [!NOTE]
> 上記のコードの場合，`webdev`フォルダの中に`test.png`という名前のファイルを作成する必要があります．

## リンク
他のHTMLファイルやインターネット上のページに遷移させることができます．`href=`の後にリンク先のURLを書きます．
### 他のHTMLファイルの場合
```html
<a href="second.html">こちらのページ</a>
```
> [!NOTE]
> 上記のコードの場合，`webdev`フォルダの中に`second.html`という名前のファイルを作成する必要があります．
### インターネット上のページの場合
```html
<a href="https://www.kyutech.ac.jp/">九工大HP</a>
```

## 埋め込み
埋め込みたいYouTubeの動画は，YouTubeのページで「共有」→「埋め込む」で埋め込むためのHTMLのコードを取得することができます．このほかにもGoogle Mapsなども埋め込むことができます．
```html
<iframe width="560" height="315" src="https://www.youtube.com/embed/oQdyX5iGnco?si=BgmDyflufS5eD1TU" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>
```

## Work3
これまでの内容をもとにオリジナルのWebページを作ってみましょう．基本は`first.html`を編集する形で，ページを自由に増やしたりいろいろ試してみましょう．何か実現したいことがある場合はCore-teamのメンバーに相談していただけたらアドバイスすることができます．
  
[次のページ](main-final.md)

> この記事は[Alias \(コマンド\)](https://ja.wikipedia.org/wiki/Alias_\(コマンド\))から翻訳されています。


**alias**（エイリアス）は、[UNIX](../Page/UNIX.md "wikilink")のシェルの組み込みコマンドで、コマンドを別名で登録（エイリアス）する役割がある\[1\]。また、単独で実行すると今のエイリアスの一覧が表示される\[2\]。エイリアスの登録を削除するには"unalias"コマンドを実行する。\[3\]

## 概要

aliasに何もつけないと、aliasの一覧が表示される。alias 名前=値　と入れると、"名前"を実行すると"値"が実行されるようになる。\[4\]ただし、aliasコマンドでエイリアスを登録してもシェルを閉じると登録した内容が消えるので、普通はシェルを開くときに実行されるファイル(例えば[bash](https://ja.wikipedia.org/wiki/bash "wikilink")なら\~/.bashrc、[zshなら](../Page/Z_Shell.md "wikilink")\~/zshrc)にaliasコマンドを書いておく。

## 実行例

### aliasを単独で実行する場合

``` console
wikisuke@localhost:~$ alias
ll=ls -l
la=ls -a
```

### aliasでエイリアスを登録する

``` console
wikisuke@localhost:~$ alias ll="ls -l"
wikisuke@localhost:~$ ll
合計 2308
drwxr-xr-x   2 wikisuke wikisuke    4096  4月 29 19:25  Desktop
drwxr-xr-x   4 wikisuke wikisuke    4096  4月 30 11:54  ダウンロード
drwxr-xr-x   2 wikisuke wikisuke    4096  3月 21 13:50  テンプレート
drwxr-xr-x   6 wikisuke wikisuke    4096  4月 23 16:06  ドキュメント
drwxr-xr-x   2 wikisuke wikisuke    4096  4月 12 10:18  ビデオ
drwxr-xr-x  11 wikisuke wikisuke    4096  4月 17 15:21  ウィキペディア原稿
drwxr-xr-x  10 wikisuke wikisuke    4096  4月 22 13:29  音楽
drwxr-xr-x   2 wikisuke wikisuke    4096  4月 29 18:52  画像
drwxr-xr-x   2 wikisuke wikisuke    4096  3月 21 13:50  公開
```

"ls -l"のエイリアスを"ll"にする。

``` console
wikisuke@localhost:~$ alias hello="echo hello" wikipedia="echo ようこそ　ウィキペディアへ"
wikisuke@localhost:~$ hello
hello
wikisuke@localhost:~$ wikipedia
ようこそ　ウィキペディアへ
```

複数個一気に実行できる。

## 脚注

<references />

[Category:UNIXのソフトウェア](https://ja.wikipedia.org/wiki/Category:UNIXのソフトウェア "wikilink")

1.
2.
3.
4.
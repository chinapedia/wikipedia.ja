> この記事は[ \(Unix\)](https://ja.wikipedia.org/wiki/_\(Unix\))から翻訳されています。


**シバン**または**シェバン** () とは[UNIX](../Page/UNIX.md "wikilink")の[スクリプトの](../Page/スクリプト言語.md "wikilink") `#!` から始まる1行目のこと。起動してスクリプトを読み込む[インタプリタ](../Page/インタプリタ.md "wikilink")を指定する。**ハッシュ・バン**または**シェル・バン**、**シャープ・バン**とも言うが、これらを縮めたシェバンという呼び方が一般的かつ簡素である\[1\]。

## 例

パスを直接指定する。[Bourne shell](https://ja.wikipedia.org/wiki/Bourne_shell "wikilink") の例。

`#!/bin/sh`
`echo 'Hello world!'`

[Ruby](../Page/Ruby.md "wikilink")言語のインタプリタ `ruby` の例（[`env`](https://ja.wikipedia.org/wiki/env "wikilink") コマンドを用いたトリック）。

`#!/usr/bin/env ruby`
`puts 'Hello world!'`

## 補足

  - ファイル先頭のシバンを認識するのは、OSの `execve` システムコール（[`exec`](https://ja.wikipedia.org/wiki/exec "wikilink") を参照）を処理するルーチン中のプログラムローダーである。
  - ファイルの先頭が[バイトオーダーマーク](https://ja.wikipedia.org/wiki/バイトオーダーマーク "wikilink")になっている[Unicode](../Page/Unicode.md "wikilink")形式のファイルの場合は動作しない。これはバイトオーダーマークのために、OSのプログラムローダーがシバンを認識できなくなるためである。
  - シバンの参照先は、実行可能バイナリでなければならず、（シバン行のある）スクリプトであってはならない。
  - シバン行の最大文字数、指定可能な[引数](../Page/引数.md "wikilink")の数などは環境依存である。また、それを逸脱した場合の動作も環境依存である。特に複数個の引数を与えた場合にどう扱われるかはまちまち（普通に扱われる、2個目以降は無視される、空白の入った1個の引数にされる）であるため、注意が必要である\[2\]。
  - envを用いたトリックはPATH[環境変数](../Page/環境変数.md "wikilink")に依存する。親プロセスが独自にPATHを設定していた場合、想定外の動作をする可能性がある。`ruby` インタプリタの場合は `-x` オプションを利用した以下のようなシェルスクリプトに見せかけるトリックを使用したほうが良い。

`#!/bin/sh`
`# -*- ruby -*-`
`exec ruby -x "$0" "$@"`
`#!ruby`
`puts 'Hello world!'`

## 注

<references/>

[Category:UNIX](https://ja.wikipedia.org/wiki/Category:UNIX "wikilink")

1.  <http://www.in-ulm.de/~mascheck/various/shebang/>
2.
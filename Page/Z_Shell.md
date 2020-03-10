> この記事は[Z Shell](https://ja.wikipedia.org/wiki/Z_Shell)から翻訳されています。


**Z shell**（ズィーシェル、**zsh**）は[Unix](https://ja.wikipedia.org/wiki/Unix "wikilink")の[コマンドシェルの](../Page/シェル.md "wikilink")1つである。 対話的な[ログイン](https://ja.wikipedia.org/wiki/ログイン "wikilink")[コマンドシェルとしても](../Page/シェル.md "wikilink")、強力な[シェルスクリプト](../Page/シェルスクリプト.md "wikilink")[コマンドの](https://ja.wikipedia.org/wiki/コマンド_\(コンピュータ\) "wikilink")[インタープリタ](https://ja.wikipedia.org/wiki/インタープリタ "wikilink")ーとしても使うことができる。

zsh は数多くの改良を含んだ[Bourne Shellの拡張版という見方もできる](../Page/Bourne_Shell.md "wikilink")。のみならず、[bash](https://ja.wikipedia.org/wiki/bash "wikilink")や[ksh](../Page/KornShell.md "wikilink")、[tcsh](https://ja.wikipedia.org/wiki/tcsh "wikilink")の非常に有用な機能も一部取り込まれている。また、Windows上でネイティブUnix環境を提供する [Interix](https://ja.wikipedia.org/wiki/Interix "wikilink") サブシステム上では[Unix](https://ja.wikipedia.org/wiki/Unix "wikilink")版のソースコードをビルドして[Windows](https://ja.wikipedia.org/wiki/Windows "wikilink")上で使用することができる。

## 起源

zsh の最初のバージョンは、1990年 \[1\] に、当時 [プリンストン大学](https://ja.wikipedia.org/wiki/プリンストン大学 "wikilink")の学生であった Paul Falstad によって作成された。 zsh の名前は、当時プリンストン大学のティーチングアシスタントであった[イェール大学](../Page/イェール大学.md "wikilink")教授 Zhong Shao のログイン名 "zsh" に由来して名付けられた\[2\]\[3\]。

## 特徴

zsh の特徴として次のようなことが挙げられる。

  - [プログラム](../Page/プログラム.md "wikilink")可能な[補完機能によって](https://ja.wikipedia.org/wiki/自動補完 "wikilink")、多くの[ユーザー](https://ja.wikipedia.org/wiki/ユーザー "wikilink")[コマンドの](https://ja.wikipedia.org/wiki/コマンド_\(コンピュータ\) "wikilink")[オプション](https://ja.wikipedia.org/wiki/オプション "wikilink")や[引数](../Page/引数.md "wikilink")を打つのを支援する（[インストール](../Page/インストール.md "wikilink")の時点で数百のコマンドをサポートしている）。
  - [ユーザー](https://ja.wikipedia.org/wiki/ユーザー "wikilink")の起動している全ての zsh でコマンド履歴を共有することができる。
  - 拡張[ファイル名生成](../Page/ファイル_\(コンピュータ\).md "wikilink")（[ワイルドカード展開](../Page/ワイルドカード_\(情報処理\).md "wikilink")）によって [`find`](https://ja.wikipedia.org/wiki/find "wikilink") のような外部コマンドを呼び出さないで、ファイル名を展開する。
  - [変数や](https://ja.wikipedia.org/wiki/変数_\(プログラミング\) "wikilink")[配列](../Page/配列.md "wikilink")の処理が改善されている。
  - 複数行コマンドを[バッファ](https://ja.wikipedia.org/wiki/バッファ "wikilink")ーで編集できる。
  - [綴り字修正機能](../Page/スペルチェッカ.md "wikilink")
  - 様々な[互換モード](https://ja.wikipedia.org/wiki/互換モード "wikilink")がある。例えば、zshを`/bin/sh`として実行したとき、[Bourne Shellの](../Page/Bourne_Shell.md "wikilink")[振りをするようにできる](https://ja.wikipedia.org/wiki/エミュレート "wikilink")。
  - [プロンプトテーマ](../Page/コマンドプロンプト.md "wikilink")
  - [端末](../Page/端末.md "wikilink")の右端に情報を表示し長いコマンドを打っているときは自動的に隠れる右プロンプトを表示できる。
  - 殆ど全部の[カスタマイズが可能](https://ja.wikipedia.org/wiki/カスタム "wikilink")。

このシェル全体のサイズが巨大であることは、マニュアルページの最初の有名なこの一文 「zshは多くの機能を持っているので、マニュアルは幾つかのセクションに分かれています。」 と、 17 個のセクション名のリストからも良く分かるだろう。

## 脚注

## 外部リンク

  - [Zsh](http://www.zsh.org/)
  - [ZSH - THE Z SHELL](http://zsh.sourceforge.net/)
  - [The Zsh Wiki](http://zshwiki.org/home/)
  - [Zsh -- the Final Letter in Shells](http://www.acm.uiuc.edu/workshops/zsh/)
  - [究極のシェル「zsh」を知る(その1)](http://news.mynavi.jp/column/osx/054/index.html)
  - [究極のシェル「zsh」を知る(その2)](http://news.mynavi.jp/column/osx/055/index.html)
  - [漢のzsh](http://news.mynavi.jp/column/zsh/index.html)
  - [zshで究極のオペレーションを](http://gihyo.jp/dev/serial/01/zsh-book)
  - [zshのある暮らし2](http://wiki.fdiary.net/zsh/)
  - [Interix - zshをインストール](http://unix.oskp.net/sua/windows_zsh.html)

[Category:オープンソースソフトウェア](https://ja.wikipedia.org/wiki/Category:オープンソースソフトウェア "wikilink") [Category:Unixシェル](https://ja.wikipedia.org/wiki/Category:Unixシェル "wikilink")

1.
2.
3.
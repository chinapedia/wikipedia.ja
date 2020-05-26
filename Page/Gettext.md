> この記事は[Gettext](https://ja.wikipedia.org/wiki/Gettext)から翻訳されています。


**gettext**は[国際化と地域化](../Page/国際化と地域化.md "wikilink")に対応する[ライブラリ](../Page/ライブラリ.md "wikilink")構成要素の一つであり、様々な地域の[言語](../Page/言語.md "wikilink")に対応した地域化ソフトウェアを[開発する際に用いられる](../Page/ソフトウェア開発.md "wikilink")。gettextライブラリを用いることで、ソフトウェアの対話的メッセージを翻訳された現地語にて容易に表示させることができる。

## gettextによるソフトウェア国際化

### プログラマ

まず、gettextが利用されるようソースコードの修正を行なう。これはほとんどのプログラミング言語において、ソースコード中の文字列がまず`gettext`関数へ渡されるよう、文字列をラップしていく作業となる。読みやすさやキータイプの手間を省くため `gettext`には通常 `_` のエイリアスが付けられる。[C言語](../Page/C言語.md "wikilink")では、

``` c
printf("My name is %s.\n", my_name);
```

を以下のように変更する:

``` c
printf(_("My name is %s.\n"), my_name);
```

C言語以外にもgettextは以下の言語/シェルコマンドで実装されている： [C++](../Page/C++.md "wikilink")、[Objective-C](../Page/Objective-C.md "wikilink")、[Bourne Shell](../Page/Bourne_Shell.md "wikilink")、[Bash](../Page/Bash.md "wikilink")、[Python](../Page/Python.md "wikilink")、[GNU CLISP](../Page/CLISP.md "wikilink")、[Emacs Lisp](../Page/Emacs.md "wikilink")、[librep](https://ja.wikipedia.org/wiki/librep "wikilink")、[GNU Smalltalk](https://ja.wikipedia.org/wiki/GNU_Smalltalk "wikilink")、[Java](https://ja.wikipedia.org/wiki/Java "wikilink")、[GNU Awk](../Page/AWK.md "wikilink")、[Pascal](../Page/Pascal.md "wikilink")、[wxWidgets](https://ja.wikipedia.org/wiki/wxWidgets "wikilink") (WxLocaleクラスによる)、[YCP](https://ja.wikipedia.org/wiki/YCP "wikilink")、[Tcl](https://ja.wikipedia.org/wiki/Tcl "wikilink")、[Perl](../Page/Perl.md "wikilink")、[PHP](../Page/PHP_\(プログラミング言語\).md "wikilink")、[Ruby](../Page/Ruby.md "wikilink")、[Pike](https://ja.wikipedia.org/wiki/Pike "wikilink")、[JavaScript](../Page/JavaScript.md "wikilink")。ほとんどの場合、使用方法はC言語の場合と同様である。

ソースコード修正後、`xgettext`コマンドを用いて翻訳可能な全ての文字列のリストを保持する **.pot**ファイル(「テンプレート」とも呼ばれる)を生成する。.potファイル中のエントリは以下のようになる：

``` pot
#: src/name.c:36
msgid "My name is %s.\n"
msgstr ""
```

文字列の直前に[コメントを置くと](../Page/コメント_\(コンピュータ\).md "wikilink")、ヘルパプログラムはコメントを翻訳者へのヒントとして扱う。

``` c
// TRANSLATORS: %s はそのままにして下さい。プログラムが変更します。
printf(_("My name is %s.\n"), my_name);
```

この例では、コメントは **TRANSLATORS:** で始まる。そして xgettext は .pot テンプレートファイルを作成する際に翻訳者のためにそのコメントを抽出する。

``` bash
$ xgettext --add-comments=TRANSLATORS:
```

生成された .pot ファイルにはこのようなコメントが付く。

``` pot
#. TRANSLATORS: %s はそのままにして下さい。プログラムが変更します。
#: src/name.c:36
msgid "My name is %s.\n"
msgstr ""
```

### 翻訳者

[thumb](https://ja.wikipedia.org/wiki/ファイル:Gettext.svg "wikilink") [thumb](https://ja.wikipedia.org/wiki/ファイル:GNU_gettext_process.png "wikilink") 翻訳者はまず、上記のテンプレートを入力として、`msginit`コマンドにより、翻訳リソースファイル(**.po**ファイル)の初期状態のものを生成し、それに対して翻訳作業を行っていく。日本語への翻訳作業を行なう場合であれば、

``` bash
$ msginit --locale=ja --input=name.pot
```

を実行し、これにより ja.poファイルが生成される。ファイル内部のエントリは以下のようになる：

``` pot
#: src/name.c:36
msgid "My name is %s.\n"
msgstr ""
```

翻訳者は手作業あるいは [Poedit](https://ja.wikipedia.org/wiki/Poedit "wikilink")のようなツールによりこれらを編集する。編集後は以下のようになる：

``` pot
#: src/name.c:36
msgid "My name is %s.\n"
msgstr "私の名前は %sです。\n"
```

最終的に、.poファイルは `msgfmt`コマンドにより **.mo**のバイナリファイルにコンパイルされ、この状態で、該当ソフトウェアパッケージの一部として配布されることになる。

### ユーザ

UNIXライクなシステムにおけるユーザは、[ロケール](https://ja.wikipedia.org/wiki/ロケール "wikilink")<var>LANGUAGE</var>を[環境変数](../Page/環境変数.md "wikilink")`LANG`にセットする。ここで<var>LANGUAGE</var>は、[IETF言語タグ](https://ja.wikipedia.org/wiki/IETF言語タグ "wikilink")に基づく値である。

`LANG=`<var>`LANGUAGE`</var>` `\[1\]

例えばシステムの[エンコーディング](https://ja.wikipedia.org/wiki/エンコーディング "wikilink")が[`UTF-8`](../Page/UTF-8.md "wikilink")であり日本国 (`JP`) の[日本語](../Page/日本語.md "wikilink") (`ja`) を話すユーザの場合、<var>LANGUAGE</var>は（IETF言語タグのハイフォンをアンダースコアに置き換えて）`ja_JP.UTF-8`をとる。

`LANG=ja_JP.UTF-8`

システムが環境変数より翻訳リソースを検索し（.moファイル中に該当言語のリソースがありさえすれば）、アプリケーションにその言語による表示を行わせることができる。

## 脚注

<references />

## 関連項目

  - [エラーメッセージ](../Page/エラーメッセージ.md "wikilink")

## 外部リンク

  - [GNU gettextホームページ](http://www.gnu.org/software/gettext/gettext.html)

[Category:ライブラリ_(プログラミング)](https://ja.wikipedia.org/wiki/Category:ライブラリ_\(プログラミング\) "wikilink") [Category:オープンソースソフトウェア](https://ja.wikipedia.org/wiki/Category:オープンソースソフトウェア "wikilink") [Category:国際化と地域化](https://ja.wikipedia.org/wiki/Category:国際化と地域化 "wikilink")

1.  `Bourneシェルの場合。環境変数の設定方法はシェルにしたがうので、Cシェルならば`` setenv LANG  `<var>`LANGUAGE`</var>`のようになる。`
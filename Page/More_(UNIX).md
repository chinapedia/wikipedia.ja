> この記事は[More \(UNIX\)](https://ja.wikipedia.org/wiki/More_\(UNIX\))から翻訳されています。


[thumb](https://ja.wikipedia.org/wiki/ファイル:More_\(Unix\).jpg "wikilink")

**more**（モア）は、[Unix系](../Page/Unix系.md "wikilink")のシステムにおいて、[テキストファイル](../Page/テキストファイル.md "wikilink")の内容を閲覧するために用いられるプログラムである。この種のプログラムは[ページャ](https://ja.wikipedia.org/wiki/ページャ "wikilink")と呼ばれる。<span style="font-family:monospace;">more</span>は非常に原始的なページャで、もともと表示領域を前方向に進めることしかできなかった。しかし、最近の実装では後方向へのスクロールも可能になっている。

## 歴史

<span style="font-family:monospace;">more</span>コマンドは[1978年](https://ja.wikipedia.org/wiki/1978年 "wikilink")、[カリフォルニア大学バークレー校](../Page/カリフォルニア大学バークレー校.md "wikilink")のDaniel Halbertによって書かれた。最初に[3.0BSDに含められ](../Page/BSD.md "wikilink")、それ以降UNIXシステムの標準プログラムとなった。 [MS-DOS](../Page/MS-DOS.md "wikilink")にも<span style="font-family:monospace;">more</span>コマンドのクローンが存在する。

## 使用法

構文は次の通り。

`more [options] [file_name]`

ファイル名が指定されなかった場合、<span style="font-family:monospace;">more</span>は[標準入力](https://ja.wikipedia.org/wiki/標準入力 "wikilink")を使用する。

<span style="font-family:monospace;">more</span>コマンドは、入力が与えられると現在のスクリーンに表示できるだけの量のテキストを表示し、ユーザからの入力を待機する。

入力にフォームフィード（改ページ; ^L）が含まれていた場合も、テキストの量に関わらずその位置で待機する。

この際、スクリーンの左下隅に「`--More--`」という文字と現在の位置を表すパーセンテージが表示される。

ファイルの終端に到達すると、<span style="font-family:monospace;">more</span>は終了する。最も一般的なスクロール方法はEnterキー、Spaceキーである。

それぞれ、行単位、画面単位で表示領域を進める。

使用方法の詳細は[manpage](https://ja.wikipedia.org/wiki/manpage "wikilink")を参照（[1](http://linuxjm.osdn.jp/html/util-linux/man1/more.1.html)）。

## 参照

  - [less](https://ja.wikipedia.org/wiki/less "wikilink")

## 外部リンク

  - [Manpage of MORE](https://linuxjm.osdn.jp/html/util-linux/man1/more.1.html) JM Project（日本語）
  - [more(1)](https://docs.oracle.com/cd/E19455-01/816-3518/6m9ptvr2l/index.html) man page（SunOS リファレンスマニュアル）
  - [more(1)](https://nixdoc.net/man-pages/HP-UX/man1/more.1.html) man page（HP-UX リファレンス）

[Category:Windowsのコマンド](https://ja.wikipedia.org/wiki/Category:Windowsのコマンド "wikilink") [Category:DOSの外部コマンド](https://ja.wikipedia.org/wiki/Category:DOSの外部コマンド "wikilink") [Category:標準UNIXプログラム](https://ja.wikipedia.org/wiki/Category:標準UNIXプログラム "wikilink") [Category:1978年のソフトウェア](https://ja.wikipedia.org/wiki/Category:1978年のソフトウェア "wikilink")
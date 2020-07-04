> この記事は[Strings](https://ja.wikipedia.org/wiki/Strings)から翻訳されています。


**strings**（ストリングズ）は [UNIX](../Page/UNIX.md "wikilink")/[Unix系](../Page/Unix系.md "wikilink")[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink")における[プログラムであり](../Page/プログラム_\(コンピュータ\).md "wikilink")、これを使えば[実行可能ファイルのような](../Page/実行ファイル.md "wikilink")[バイナリ](../Page/バイナリ.md "wikilink")ファイルに埋め込まれているテキスト[文字列](../Page/文字列.md "wikilink")を見つけることができる。

このプログラムは[オブジェクトファイル](../Page/オブジェクトファイル.md "wikilink")や[コアダンプ](../Page/コアダンプ.md "wikilink")に対しても使える。

`strings`は[null](https://ja.wikipedia.org/wiki/null "wikilink")終端の（デフォルトで）4つ以上の印刷可能な文字の並びを探し出し、それを文字列として認識する。いくつかの実装では何を印刷可能な文字として扱うのかを決めるためのオプションが提供されている。これはASCIIではないワイド文字テキストを見つけるのに便利である。

`strings`を使う際、[`grep`](https://ja.wikipedia.org/wiki/grep "wikilink")や[`fold`](../Page/GNU_Core_Utilities.md "wikilink")にパイプでつなぐことや[ファイルへ出力をリダイレクトさせることがよく行われる](../Page/ファイル_\(コンピュータ\).md "wikilink")。

これは[GNU Binutilsの一部である](../Page/GNU_Binutils.md "wikilink")。

## 例

`$ strings foobar`
`Qåtd`
`/lib/ld-linux.so.2`
`_Jv_RegisterClasses`
`__gmon_start__`
`libc.so.6`
`puts`
`_IO_stdin_used`
`__libc_start_main`
`GLIBC_2.0`
`...`

## 関連項目

  - [`cat`](https://ja.wikipedia.org/wiki/cat_\(UNIX\) "wikilink")
  - [GNUデバッガ](../Page/GNUデバッガ.md "wikilink")
  - [`strip`](https://ja.wikipedia.org/wiki/strip "wikilink")

## 外部リンク

  - [strings(1)](https://linuxjm.osdn.jp/html/GNU_binutils/man1/strings.1.html) man page (JM Project)
  - [strings(1)](https://docs.oracle.com/cd/E19253-01/819-1210/6n3j74ju1/index.html) man page（SunOSリファレンス・マニュアル）
  - [strings(1)](https://nixdoc.net/man-pages/HP-UX/man1/strings.1.html) man page（HP-UXリファレンス）

[Category:UNIXのソフトウェア](https://ja.wikipedia.org/wiki/Category:UNIXのソフトウェア "wikilink") [Category:文字列](https://ja.wikipedia.org/wiki/Category:文字列 "wikilink")
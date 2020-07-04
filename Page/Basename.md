> この記事は[Basename](https://ja.wikipedia.org/wiki/Basename)から翻訳されています。


**`basename`**（ベースネーム）は [UNIX](../Page/UNIX.md "wikilink") のプログラムであり、`basename` に [パス名](https://ja.wikipedia.org/wiki/パス名 "wikilink") を与えると、最後のスラッシュ ('/') までの部分を削除した文字列を返す。`basename` は [Single UNIX Specification](../Page/Single_UNIX_Specification.md "wikilink") に記述されており、主に[シェルスクリプト](../Page/シェルスクリプト.md "wikilink")で使われる。

## 使用法

[Single UNIX Specification](../Page/Single_UNIX_Specification.md "wikilink") における `basename` の仕様は以下のようになっている。

`basename string [suffix]`

  -
    `string`
      -
        [パス名](https://ja.wikipedia.org/wiki/パス名 "wikilink")
    `suffix`
      -
        指定されたとき、`basename` は suffix も削除する。

## 例

`$ basename /usr/home/jsmith/basename.wiki ki`
`basename.wi`

## 効率

`basename` が受け取れるパス名の数は一つに限られているので、シェルスクリプトの[内部ループ](https://ja.wikipedia.org/wiki/内部ループ "wikilink")内で使用するには効率が悪い。

`while read file; do`
`  basename "$file"`
`done < `*`some-input`*

上記のスクリプトでは入力の各行毎に別のプロセスを起動することになる。このため、典型的には [sed](https://ja.wikipedia.org/wiki/sed_\(コンピュータ\) "wikilink") が代わりに用いられる。

`sed 's/.*\///' < `*`some-input`*

## 関連項目

  - [dirname](https://ja.wikipedia.org/wiki/dirname "wikilink")

## 外部リンク

  - [return non-directory portion of a pathname](https://pubs.opengroup.org/onlinepubs/009695399/utilities/basename.html)
  - [Manpage of BASENAME](https://linuxjm.osdn.jp/html/GNU_sh-utils/man1/basename.1.html) GNU 版。JM Project
  - [basename(1)](https://docs.oracle.com/cd/E19253-01/819-1210/basename-1/index.html) man page（SunOS リファレンスマニュアル）
  - [basename(1)](https://nixdoc.net/man-pages/HP-UX/man1/basename.1.html) man page（HP-UX リファレンス）

[Category:UNIXのソフトウェア](https://ja.wikipedia.org/wiki/Category:UNIXのソフトウェア "wikilink")
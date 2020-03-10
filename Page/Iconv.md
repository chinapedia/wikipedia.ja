> この記事は[Iconv](https://ja.wikipedia.org/wiki/Iconv)から翻訳されています。


**iconv**（アイコンブ）は異なる[文字コード](../Page/文字コード.md "wikilink")間の相互変換を行う標準[API](../Page/アプリケーションプログラミングインタフェース.md "wikilink")。または、そのAPIに付属する文字コード変換ユーティリティプログラム。名前は「***I**nternational Codeset **Conv**ersion Library*」に由来する\[1\]。GNUによる実装\[2\]が有名で、変換ライブラリのライセンス形態は[GNU LGPL](../Page/GNU_Lesser_General_Public_License.md "wikilink")。変換プログラムのライセンス形態は[GNU GPL](../Page/GNU_General_Public_License.md "wikilink")。

## iconv API

iconvのAPIは、おもに[UNIX](../Page/UNIX.md "wikilink")環境で文字列の文字コード変換を行う標準[インタフェースである](../Page/インタフェース_\(情報技術\).md "wikilink")。iconvは最初[HP-UX](../Page/HP-UX.md "wikilink")で開発され、後に[POSIX](../Page/POSIX.md "wikilink")規格として標準化された。そのため、ほとんどの[Unix系](../Page/Unix系.md "wikilink")のシステムで使用できる。

iconv APIは文字コード変換プログラムのほか、既存のプログラムを[国際化](https://ja.wikipedia.org/wiki/国際化 "wikilink")または[多言語](../Page/多言語.md "wikilink")化するためにも用いられる。例えば、[Samba](../Page/Samba.md "wikilink")の国際化にはiconvが利用されている。

## 互換性

[XML処理用ライブラリである](../Page/Extensible_Markup_Language.md "wikilink")[libxml](https://ja.wikipedia.org/wiki/libxml "wikilink")がiconvを必要としているため、libxmlを使用した[アプリケーションソフトウェア](../Page/アプリケーションソフトウェア.md "wikilink")を利用する場合にもiconvを必要とする。

[Microsoft Windows上では](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")、[Cygwin](../Page/Cygwin.md "wikilink")や[GnuWin32](https://ja.wikipedia.org/wiki/GnuWin32 "wikilink")等の[Unixライクな環境をインストールすることで](../Page/Unix系.md "wikilink")、iconv [APIやiconvプログラムを利用できるようになる](../Page/アプリケーションプログラミングインタフェース.md "wikilink")。

プログラミング言語の標準ライブラリにAPIが組み込まれている場合がある。

  - [PHP](../Page/PHP_\(プログラミング言語\).md "wikilink")
    PHPスクリプトからiconvの機能を利用することができる([WindowsのPHPでも付属の](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")[DLL](../Page/ダイナミックリンクライブラリ.md "wikilink") ([iconv.dll](http://jp.php.net/iconv))により利用可能)。
  - バージョン1.9以前の[Ruby](../Page/Ruby.md "wikilink")
    それ以降のバージョンではそのプラットフォーム依存性から非推奨扱いになっており、String\#encodeを代替とする。

## 日本語の対応状況

[GNU Cライブラリのiconvでは](https://ja.wikipedia.org/wiki/GNU_Cライブラリ "wikilink")2019年5月現在のところ、[EUC-JP](../Page/EUC-JP.md "wikilink")、[EUC-JIS X0213](../Page/EUC-JIS-2004.md "wikilink")、[Shift_JIS](../Page/Shift_JIS.md "wikilink")、[Shift_JIS X0213](../Page/Shift_JIS-2004.md "wikilink")、[CP932](https://ja.wikipedia.org/wiki/Microsoftコードページ932 "wikilink")、[ISO-2022-JP](../Page/ISO-2022-JP.md "wikilink")、[ISO-2022-JP-2](https://ja.wikipedia.org/wiki/ISO-2022-JP-2 "wikilink")、[ISO-2022-JP-1](https://ja.wikipedia.org/wiki/ISO-2022-JP-1 "wikilink")、[ISO-2022-JP-MS](https://ja.wikipedia.org/wiki/ISO-2022-JP-MS "wikilink")、[ISO-2022-JP-3](https://ja.wikipedia.org/wiki/ISO-2022-JP-3 "wikilink")等の日本語の文字コードに対応している\[3\]。また、[Unicode](../Page/Unicode.md "wikilink")のエンコーディングである[UTF-8](../Page/UTF-8.md "wikilink")、[UTF-16](../Page/UTF-16.md "wikilink")、[UTF-32](../Page/UTF-32.md "wikilink")、[UTF-7](https://ja.wikipedia.org/wiki/UTF-7 "wikilink")にも対応している\[4\]。

古くから使用されている[nkfと異なり](https://ja.wikipedia.org/wiki/Network_Kanji_Filter "wikilink")、多くの環境で標準的に使用できるが、一部の文字でnkfと変換結果が異なる点で注意を要する。 また、nkfに存在するエンコードの自動検出機能は存在しない。

## 使用例

特に意識していなくても、多くの非英語環境向けのUNIXプログラムの内部で間接的に使用されているが、もちろんユーザが明示的に使用することもできる。

ここでは、Shift_JISのテキストファイルsjis.txtを、UTF-8に変換し、utf8.txtとして保存する場合のコマンドの例を示す。

### シェルからiconvコマンドで変換する場合

次のコマンドを実行することで変換できる。

`iconv -f Shift_JIS -t UTF-8 sjis.txt > utf8.txt`

### 自作プログラムからiconvライブラリを使用し変換する場合

次の[C言語](../Page/C言語.md "wikilink")ソースをコンパイルし、実行することで変換できる。

ただし、簡単のためエラー処理は省略しているので、このまま実用プログラムに使用しないこと。

``` c
#include <stdio.h>
#include <iconv.h>

#define S_SIZE (1024)

int main(void) {
  iconv_t icd;
  FILE *fp_src, *fp_dst;
  char s_src[S_SIZE], s_dst[S_SIZE];
  char *p_src, *p_dst;
  size_t n_src, n_dst;

  icd = iconv_open("UTF-8", "Shift_JIS");
  fp_src = fopen("sjis.txt", "r");
  fp_dst = fopen("utf8.txt", "w");

  while (1) {
    fgets(s_src, S_SIZE, fp_src);
    if (feof(fp_src))
      break;
    p_src = s_src;
    p_dst = s_dst;
    n_src = strlen(s_src);
    n_dst = S_SIZE-1;
    while (0 < n_src) {
      iconv(icd, &p_src, &n_src, &p_dst, &n_dst);
    }
    *p_dst = '\0';
    fputs(s_dst, fp_dst);
  }

  fclose(fp_dst);
  fclose(fp_src);
  iconv_close(icd);

  return 0;
}
```

## 脚注

## 外部リンク

  - コマンド
      - [iconv(1)](https://docs.oracle.com/cd/E19683-01/817-7410/6mmnue19p/index.html) man page（SunOS リファレンスマニュアル）
      - [iconv(1)](https://support.hpe.com/hpsc/doc/public/display?docId=emr_na-c01976051&docLocale=ja_JP) man page（HP-UX リファレンス：ユーザーコマンド p579）
  - ライブラリ・ルーチン
      - [iconv(3)](https://linuxjm.osdn.jp/html/LDP_man-pages/man3/iconv.3.html) JM Project
      - [iconv(3)](https://docs.oracle.com/cd/E19683-01/816-3989/6ma7v5jrb/index.html) man page（SunOS リファレンスマニュアル）
      - [iconv(3C)](https://support.hpe.com/hpsc/doc/public/display?docId=emr_na-c01976150&docLocale=ja_JP) man page（HP-UX リファレンス：ライブラリ p855）
  - [オンライン版のiconvコマンド](http://www.iconv.com/iconv.htm)（英語）
  - [GNUのCライブラリiconv](https://www.gnu.org/software/libiconv/)（英語）

[Category:オープンソースソフトウェア](https://ja.wikipedia.org/wiki/Category:オープンソースソフトウェア "wikilink") [Category:UNIXのソフトウェア](https://ja.wikipedia.org/wiki/Category:UNIXのソフトウェア "wikilink") [Category:API](https://ja.wikipedia.org/wiki/Category:API "wikilink")

1.  [Tru64 UNIX worldwide language support](http://h30097.www3.hp.com/unix/i18n.htm)
2.  [GNU libiconv](https://www.gnu.org/software/libiconv/)
3.
4.
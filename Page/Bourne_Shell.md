> この記事は[Bourne Shell](https://ja.wikipedia.org/wiki/Bourne_Shell)から翻訳されています。


**Bourne Shell**(**ボーンシェル**)は、[Unix Version 7](../Page/Version_7_Unix.md "wikilink") の[Unixシェル](https://ja.wikipedia.org/wiki/Unixシェル "wikilink")である。[POSIX](../Page/POSIX.md "wikilink")規格で規定されるUnix系システムにおいて `/bin/sh` はBourne Shell互換のシェルであり、`/bin/sh`はBourne Shellかその互換プログラムへの[シンボリックリンク](https://ja.wikipedia.org/wiki/シンボリックリンク "wikilink")か[ハードリンク](../Page/ハードリンク.md "wikilink")になっている。多くのUnix系システムでは現在でもシェルスクリプトを記述するのに`/bin/sh`が一般的に使われている。ただし、ユーザが通常使うシェルにはより新しいシェルを用いることが一般的である。

[AT\&T](../Page/AT&T.md "wikilink")[ベル研究所](../Page/ベル研究所.md "wikilink")の[スティーブン・ボーン](../Page/スティーブン・ボーン.md "wikilink")が開発し、それまでの [Thompson shell](https://ja.wikipedia.org/wiki/Thompson_shell "wikilink") を置き換えた。いずれもコマンド名は **`sh`** である。[Version 7 Unix](../Page/Version_7_Unix.md "wikilink") の一部として1977年に大学等に配布された。対話型のコマンドインタプリタとしても使われるが、[スクリプト言語](../Page/スクリプト言語.md "wikilink")としての性格が強く、一般に構造化プログラムを作り出すと考えられている全ての機能を含んでいる。

[ブライアン・カーニハン](../Page/ブライアン・カーニハン.md "wikilink")と[ロブ・パイク](../Page/ロブ・パイク.md "wikilink")による『UNIXプログラミング環境』の出版が Bourne Shell の人気を高めた。これはチュートリアル形式でプログラミング言語としてのシェルを紹介した最初の商業出版本である。

## 起源

Bourne shell は  の代替として設計された。

当初の設計目標には、以下の事柄が含まれていた\[1\]。

  - [シェルスクリプト](../Page/シェルスクリプト.md "wikilink")を[フィルタとして使えるようにする](../Page/フィルタ_\(ソフトウェア\).md "wikilink")。
  - [制御構造](../Page/制御構造.md "wikilink")と[変数を導入してプログラムのしやすさを向上させる](../Page/変数_\(プログラミング\).md "wikilink")。
  - 全ての入出力[ファイル記述子](../Page/ファイル記述子.md "wikilink")を制御する。
  - シェルスクリプト内で[シグナル処理を制御する](../Page/シグナル_\(Unix\).md "wikilink")。
  - シェルスクリプトを解釈する際の文字列長の制限を撤廃する。
  - 文字列のクォート機構を合理的かつ汎用的にする。
  - Version 7 で[環境変数](../Page/環境変数.md "wikilink")機構が追加された。これを利用して、シェルスクリプトが初期化時に構築した環境情報を、わざわざ[パラメータを使わずとも子スクリプト](../Page/引数.md "wikilink") (子[プロセス](../Page/プロセス.md "wikilink")) に渡すことができる。

## 機能と特徴

UNIX Version 7 での Bourne Shell の機能と特徴を以下に挙げる:

  - スクリプトは、そのファイル名を使ってコマンドとして呼び出すことができる。
  - 対話的にも非対話的にも使える。
  - コマンド群の同期実行も非同期実行も可能。
  - 入出力のリダイレクトとパイプラインをサポート。
  - 組み込みコマンド群を提供。
  - フロー制御構成子、引用ファシリティ、関数を提供。
  - 型のない変数。
  - 局所と大域の変数スコープを提供。
  - スクリプトは実行前にコンパイルする必要が無い。
  - Goto機能を持っていない。
  - バッククォートを使ったコマンド置換（Command substitution）: `` `command` ``
  - `<<` を使った[ヒアドキュメント](https://ja.wikipedia.org/wiki/ヒアドキュメント "wikilink")（Here documents）機能。スクリプト内に埋め込まれたテキストブロックを入力として使う。
  - "*`for ~ do ~ done`*" ループ。特に、`$*` を使って引数列上をループする方法。
  - "*`case ~ in ~ esac`*" による選択機構。主に引数解析に使われる。
  - *`sh`* は、環境変数を使ってエクスポート可能なキーワードパラメータや変数を実現している。
  - 入出力制御と表現マッチングのために強力な機能を用意している。

また、Bourne Shell はエラーメッセージのために 2番の[ファイル記述子](../Page/ファイル記述子.md "wikilink")を使うという規定を最初に採用したプログラムでもある。これにより、[エラーメッセージ](../Page/エラーメッセージ.md "wikilink")をデータと分離してスクリプトで制御することが容易になった。

スティーブン・ボーンは自身が[ケンブリッジ大学](../Page/ケンブリッジ大学.md "wikilink")で関わっていた [ALGOL 68C](../Page/ALGOL.md "wikilink") コンパイラのいくつかの特徴をこのシェルに取り込んだ。例えば、"<u>**`if`**</u>`  ~  `<u>`then`</u>`  ~  `<u>`else`</u>`  ~  `<u>**`fi`**</u>"、"<u>**`case`**</u>`  ~  `<u>`in`</u>`  ~  `<u>`out`</u>`  ~  `<u>**`esac`**</u>"、"<u>`for`</u>`  ~  `<u>`while`</u>`  ~  `<u>**`do`**</u>`  ~  `<u>**`od`**</u>" といった構文である。さらに Version 7 のシェルは[C言語](../Page/C言語.md "wikilink")で記述されているが、ボーンはその[ソースコード](../Page/ソースコード.md "wikilink")をALGOL68風にするためにいくつかの[マクロ](../Page/マクロ_\(コンピュータ用語\).md "wikilink")\[2\]を使っている。このマクロは、[IOCCC](../Page/IOCCC.md "wikilink")が開催される元の1つとなった（他に、[4.2BSDの](../Page/BSD.md "wikilink") finger コマンドも元になっている）\[3\]。

## 1979年以降に導入された機能

数年の内に AT\&T は Bourne Shell を強化した。各バージョンは対応する AT\&T UNIX のバージョン名で呼ばれる(主なバージョンは Version 7、SystemIII、SVR2、SVR3、SVR4)。というのも、シェルはバージョン番号が付与されていないからでもあり、区別するには実際に機能をテストしてみる必要があった\[4\]。

1979年以降のバージョンの Bourne shell の機能（や特徴）を以下に示す\[5\]。

  - [UNIX System III](../Page/UNIX_System_III.md "wikilink")（1981年）
      - *test* コマンドを組み込み。
      - \# でコメントを書き込めるようになった。
      - コロンを使ったパラメータのデフォルト値への置換: "${parameter:=word}"
  - [SVR2](https://ja.wikipedia.org/wiki/UNIX_System_V#SVR2 "wikilink")（1984年）
      - 関数定義が可能となり、*return* が組み込まれた。
      - *unset*、*echo*、*type* を組み込み
      - ソースコードを書き換えて、ALGOL68風でなくした。
  - [SVR3](https://ja.wikipedia.org/wiki/UNIX_System_V#SVR3 "wikilink")（1986年）
      - 現在のような "$@" の用法
      - *getopts* 組み込み
      - パラメータ処理を改善し、関数の再帰呼び出しが可能となった。
      - 8ビットクリーン
  - [SVR4](https://ja.wikipedia.org/wiki/UNIX_System_V#SVR4 "wikilink")（1989年）
      - ジョブコントロール
      - 多バイト文字サポート

サンが[OpenSolaris](../Page/OpenSolaris.md "wikilink")の中の Bourne Shell の派生版を[オープンソース](../Page/オープンソース.md "wikilink")としてリリースすると、他のフリーなUNIX系OS向けにこれを移植する[Heirloomプロジェクト](http://heirloom.sourceforge.net/sh.html)が開始され、利用可能となっている。Solaris や SVR4 の Bourne shell はオリジナルの ALGOL 68 風のソースコードではない。

## 批判

Bourne shell は、[C Shell](../Page/C_Shell.md "wikilink") と比べて次のような欠点があると批判されてきた\[6\]\[7\]。

  - 対話的に使用する場合、Bourne shell は使いやすくない。[C Shell](../Page/C_Shell.md "wikilink") には、ヒストリ機能、エイリアス機能、ジョブコントロール機能などがあり、素早く簡単に操作できる。
  - Unixシステムの大部分は[C言語](../Page/C言語.md "wikilink")で書かれているが、Bourne shell の文法はC言語とは全く似ておらず、[ALGOL](../Page/ALGOL.md "wikilink")に似ている。
  - [式を評価する機能がない](../Page/式_\(プログラミング\).md "wikilink")。単純な式であっても外部の  と [`expr`](https://ja.wikipedia.org/wiki/expr "wikilink") というユーティリティを使わないと式を評価できない。

## 後継

Bourne shell ではなく Thompson shell から派生した [C Shell](../Page/C_Shell.md "wikilink") (csh) は 4.1BSD で配布され、[BSD](../Page/BSD.md "wikilink")カーネルの「ジョブ制御」機能を導入した。ジョブ制御は対話的にプログラムを止めたり、後でそれを再開させる機能である。C Shell がコマンドインタプリタとして人気になったのはこの機能があったためである。また C Shell は C言語風の文法を採用したことにより Bourne Shell と互換性がなくなってしまった。なお、ジョブ制御機能は後に Bourne shell にも導入され、その後継シェルの多くにも採用されている。

後に[デビッド・コーンが開発した](https://ja.wikipedia.org/wiki/デビッド・コーン_\(コンピュータ科学者\) "wikilink") [KornShell](../Page/KornShell.md "wikilink") (ksh) は、Bourne Shell と C Shell の中間のようなもので、文法はほぼ Bourne Shell と同一で、ジョブ制御機能を C Shell から取り入れた。当初の KornShell (ksh88)の機能は[POSIX](../Page/POSIX.md "wikilink")におけるシェル標準の基盤となっている。その後、ksh93 が 2000年にオープンソース化され、いくつかの[Linuxディストリビューション](../Page/Linuxディストリビューション.md "wikilink")で使われている。ksh88 のクローン pdksh もあり、[OpenBSD](../Page/OpenBSD.md "wikilink")のデフォルトシェルとなっている。

[Bash](../Page/Bash.md "wikilink") (*Bourne Again Shell*)は、その名が示す通り Bourne Shell を基本として C Shell や KornShell の機能を取り入れ、[GNUプロジェクト](../Page/GNUプロジェクト.md "wikilink")の一部として開発された。[macOS](https://ja.wikipedia.org/wiki/macOS "wikilink")、[Cygwin](../Page/Cygwin.md "wikilink")、多くのLinuxディストリビューションでデフォルトシェルとなっている。

[rcは](../Page/Rc_\(シェル\).md "wikilink")、[ベル研究所](../Page/ベル研究所.md "wikilink")のが  での sh の後継として開発した。[Plan 9 from Bell Labs](../Page/Plan_9_from_Bell_Labs.md "wikilink") ではデフォルトシェルとされている。 の一部としてUNIXにも移植されたことがある。

かつて[CSRGのBSDリリースでも使われた](../Page/Computer_Systems_Research_Group.md "wikilink") Bourne Shell には著作権問題がまとわりついていた。そこで Kenneth Almquist が [Almquist Shell](../Page/Almquist_Shell.md "wikilink") とも呼ばれる Bourne Shell のクローンを開発した。これは[BSDライセンス](../Page/BSDライセンス.md "wikilink")で提供されていて、現在もBSD系でメモリ容量が小さい場合などに使われている。Linux にも移植され [Debian Almquist shell](https://ja.wikipedia.org/wiki/Debian_Almquist_shell "wikilink") または dash と呼ばれている。メモリ使用量が小さいため、シェルスクリプトの実行が bash よりも高速という特徴がある。

## 利用

Bourne shell は全ての商用UNIXシステムで標準とされているが、BSD系のシステムには [C Shell](../Page/C_Shell.md "wikilink") で書かれたスクリプトが多数存在する。Bourne shell のスクリプトは [GNU](../Page/GNU.md "wikilink")/[Linux](../Page/Linux.md "wikilink") や他の[Unix系](../Page/Unix系.md "wikilink")システム上の [bash](https://ja.wikipedia.org/wiki/bash "wikilink") や [dash](https://ja.wikipedia.org/wiki/Debian_Almquist_shell "wikilink") でもほとんど実行可能である。

多くのLinuxシステムで、`/bin/sh` は[bash](https://ja.wikipedia.org/wiki/bash "wikilink")への[ハードリンク](../Page/ハードリンク.md "wikilink")またはシンボリックリンクとなっている。しかしUbuntuなどのLinuxシステムでは効率がよいことから `/bin/sh` を [dash](https://ja.wikipedia.org/wiki/Debian_Almquist_shell "wikilink") へのリンクとしている。

## 語録

## 参考文献

  -
  -
  -
  -
  -
## 脚注

## 関連項目

  - [GNU Bash](../Page/Bash.md "wikilink")

## 外部リンク

  - [Bourne Shell自習テキスト](http://flex.phys.tohoku.ac.jp/texi/sh/sh.html)
  - [ボーン氏が C を ALGOL68C風にするために使ったマクロ](https://minnie.tuhs.org/cgi-bin/utree.pl?file=V7/usr/src/cmd/sh/mac.h)
  - [Bourne Shell のソースコード](https://minnie.tuhs.org/cgi-bin/utree.pl?file=V7/usr/src/cmd/sh)
  - [オリジナルの Bourne Shell のドキュメント(1978年、英語)](https://steve-parker.org/sh/bourne.shtml)
  - [The individual members of "The Traditional Bourne Shell Family"](https://www.in-ulm.de/~mascheck/bourne/)
  - [A port of the "heirloom" SVR4 Bourne shell from OpenSolaris to other Unix-like systems](http://heirloom.sourceforge.net/sh.html)
  - [faqs shell differences](http://www.faqs.org/faqs/unix-faq/shell/shell-differences/)
  - [Howard Dahdah, The A–Z of Programming Languages: Bourne shell, or sh — An in-depth interview with Steve Bourne, creator of the Bourne shell, or sh](http://www.computerworld.com.au/article/279011/-z_programming_languages_bourne_shell_sh?fp=&fpid=&pf=1), *Computerworld*, 5 March 2009.

[de:Unix-Shell\#Die Bourne-Shell](https://ja.wikipedia.org/wiki/de:Unix-Shell#Die_Bourne-Shell "wikilink")

[Category:Unixシェル](https://ja.wikipedia.org/wiki/Category:Unixシェル "wikilink") [Category:1977年のソフトウェア](https://ja.wikipedia.org/wiki/Category:1977年のソフトウェア "wikilink")

1.  ["The A-Z of Programming Languages: Bourne shell, or sh"](http://www.computerworld.com.au/article/279011/-z_programming_languages_bourne_shell_sh) March 2009, Computerworld
2.
3.
4.  [Bourne Shell release testing script from Sven Mascheck](http://www.in-ulm.de/~mascheck/various/whatshell/)
5.  [History of the Bourne Shell family](http://www.in-ulm.de/~mascheck/bourne/)
6.  [*An Introduction to the C shell*](http://www.kitebird.com/csh-tcsh-book/csh-intro.pdf) by [Bill Joy](../Page/ビル・ジョイ.md "wikilink").
7.
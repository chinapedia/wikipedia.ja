> この記事は[Autotools](https://ja.wikipedia.org/wiki/Autotools)から翻訳されています。


[thumb](https://ja.wikipedia.org/wiki/ファイル:Autoconf-automake-process.svg "wikilink") **Autotools**とは、主に[Unix系](../Page/Unix系.md "wikilink")[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink") (OS) において[ソフトウェア](../Page/ソフトウェア.md "wikilink")パッケージ開発を行うための、ツール及び[フレームワーク](https://ja.wikipedia.org/wiki/フレームワーク "wikilink")の一種である。このツールを使用することにより、多種多様な[UNIX](../Page/UNIX.md "wikilink")互換環境にパッケージを対応させることが容易になる。 Autotoolsは主に autoconf/automake/libtools の3つから成り立っている。

## パッケージ利用者側から視たAutotools

Autotoolsを用いて作成されたパッケージは容易に導入が可能である。典型的な場合、[インストール](../Page/インストール.md "wikilink")までの全工程が自動化されており、[ソースコード](../Page/ソースコード.md "wikilink")を展開した後、以下のコマンドを入力するだけで全てが完了する。  多くのUNIX用[オープンソース](../Page/オープンソース.md "wikilink")ソフトウェアで、この方式が採用されている。

### configure

利用者の環境はさまざまであるがほとんどの場合、必要な設定はパッケージに同梱の[プログラムconfigureを実行するだけで終了する](../Page/プログラム_\(コンピュータ\).md "wikilink")。configureは環境を検査しソースコードの修正を行う。

configure（実は[シェル](../Page/シェル.md "wikilink")スクリプトである）及び付属のスクリプト・Makefileなどは標準的なUNIXコマンドだけを使用しており、パッケージの利用者は、パッケージそのものの構築・運用に必要なソフトウェアを除いて、Autotoolsの為に特別なソフトウェアを導入する必要はない（[Windows系OSではUNIXコマンドが標準で含まれていない為](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")、別途[Services for UNIXや](https://ja.wikipedia.org/wiki/Services_for_UNIX "wikilink")[Cygwin](../Page/Cygwin.md "wikilink")などのUNIX互換環境のインストールが必要である）。

また、自動的な環境検査が好ましくなかったり特別な設定が必要な場合、環境変数またはコマンド引数でconfigureの動作を調整できる。代表的なオプションを以下に説明する。

  - \--prefix=*dir*:インストール先を変更する。--prefix=/opt/hugaとすると、[実行ファイル](../Page/実行ファイル.md "wikilink")は/opt/huga/bin、[ライブラリ](../Page/ライブラリ.md "wikilink")は/opt/huga/libというように変更される。bin、libなどを個別に変更することも出来る。デフォルトは/usr/localである。OSベンダーなどが提供するバイナリパッケージでは、--prefix=/usrや--prefix=/opt/hugaなどの設定で構築されている場合が多い。root権限のないユーザや試しに利用したい場合は、--prefix=$HOME/hugaなどとすれば、他のユーザに影響を与えることを防止できる。
    \--with-*hoge*:別のパッケージhogeを利用することを指定する。--with-hoge=*dir*でhogeのインストール先を指定できる場合もある。--with-hoge=no又は--without-hogeとすると逆に使用しないことを指定する。
    環境変数 CC:[環境変数](../Page/環境変数.md "wikilink")CCを設定すると、その値が[C](../Page/C言語.md "wikilink")[コンパイラ](../Page/コンパイラ.md "wikilink")のコマンド名として使用される。設定しない場合はccまたは適切なOS標準のコンパイラに設定されるが、明示的に設定することで標準と異なるコンパイラを使用できる。

これ以外にも多くのオプションがあり、少ないパッケージでも10以上、多いパッケージでは数十から100以上の設定項目がある。利用者の設定に矛盾があったり、環境の機能に不足があれば診断情報を出力する。また、[クロスコンパイル](https://ja.wikipedia.org/wiki/クロスコンパイル "wikilink")対応や、構築用の作業[ディレクトリ](../Page/ディレクトリ.md "wikilink")をソースコードと異なるディレクトリに設定する機能がある。

## autoconf

**autoconf**は上で説明したconfigureを生成するためのプログラムである。

### 特徴

autoconfはDavid Mackenzieが[フリーソフトウェア財団](../Page/フリーソフトウェア財団.md "wikilink")での仕事で使うために、1991年の夏から開発を開始した。その後、様々な人に改良を加えられ、オープンソースのコミュニティでは最もよく使われるツールの1つとなった。

autoconfは[Perl](../Page/Perl.md "wikilink")で使われるMetaconfigに似ている。かつて（X11R6.9 まで）[X Window Systemで使われていた](../Page/X_Window_System.md "wikilink")にも密接に関連するが、設計思想が異なる。

autoconfは[移植性の評価をバージョンではなく機能ベースで行う](../Page/移植_\(ソフトウェア\).md "wikilink")。例えば[SunOS](../Page/SunOS.md "wikilink") 4のCコンパイラはISO Cをサポートしていない。しかし、ユーザはISO C互換のコンパイラをインストールすることもできる。バージョンのみからでは、ISO Cコンパイラの存在は検出できないが、機能ベースの手法ではユーザがインストールしたISO Cコンパイラを発見できる。他にも、次のような利点がある。

  - パッケージ開発後に生まれた新たな（未知の）システム上でも、うまく機能する。
  - カスタマイズされた環境でもうまく対応できる。
  - バージョンやパッチなどを詳細に把握しておく必要がない。

### 機能

[m4言語の](https://ja.wikipedia.org/wiki/m4_\(プログラミング言語\) "wikilink")[マクロとシェルスクリプトの断片で記述された入力ファイルconfigure](../Page/マクロ_\(コンピュータ用語\).md "wikilink").ac（古いバージョンではconfigure.in）を、autoconfがm4を用いて置換しconfigureを得る。 最終出力configureは[Bourne Shell用のシェルスクリプトで](../Page/Bourne_Shell.md "wikilink")、数百行から数千行の長さがある。

以下に、簡単なconfigure.acの例を示す。

`AC_INIT(hello, 1.9, address) # 必須設定`
`AC_CONFIG_SRCDIR([hello.c])`
`# このパッケージではhogeを使用可能である configureに--with-hogeが追加される。`
`#（実際には、この後に利用者が--with-hoge=yesとした場合の動作定義を記述する必要がある）`
`AC_ARG_WITH(hoge, [Use hoge]) `

`AC_PROG_CC                    # Cコンパイラの設定 configureが環境変数CCを使用する`
`AC_OUTPUT([Makefile])         # Makefile.inを雛形にしてMakefileを生成`

出力のconfigureは非常に長いので掲載しない。この場合、一般的なオプションはサポートされる。利用者の要求に応じてhogeを利用するがどうかを決定する。また、Cコンパイラを探し実行方法を確認し、その結果得られたコマンド名・必要オプションなどをMakefileに出力する。

## automake

GNU Makefile標準に準拠したMakefileを簡単に作成できる。Makefile.amと呼ばれるファイルに、プログラムとソースコードの関係などを記述すると、Makefile.inを出力する。configureがMakefile.inに環境固有の設定を追加することで、構築用のMakefileとなる。

### 実行例

HelloWorldプログラムで例を示す

`#Makefile.am`
`#実行バイナリファイルの名前はhello`
`bin_PROGRAMS = hello`
`#helloのソースコードはhello.c,hello.h`
`hello_SOURCES = hello.c hello.h`

出力のMakefile.inは非常に長いので掲載しないが、期待した内容が得られる。 すなわち、configureを実行することでMakefileが生成される。このMakefileを用いてmakeコマンドを使用すると、hello.cをCコンパイラでコンパイルし、次いで標準ライブラリとリンクし、helloの実行ファイルが得られる。make installでは、helloはあるべき場所（ほとんどの場合は/usr/local/bin）にインストールされることになる。

## 関連項目

  - [ビルド (ソフトウェア)](https://ja.wikipedia.org/wiki/ビルド_\(ソフトウェア\) "wikilink")
  - [Gnits Standards](https://ja.wikipedia.org/wiki/:en:Gnits_Standards "wikilink")
  - [GNU Coding Standards](https://ja.wikipedia.org/wiki/:en:GNU_Coding_Standards "wikilink")
  - [CMake](https://ja.wikipedia.org/wiki/CMake "wikilink")
  - [Meson](https://ja.wikipedia.org/wiki/Meson_\(ソフトウェア\) "wikilink")
  - [Apache Ant](../Page/Apache_Ant.md "wikilink")
  - [Apache Maven](../Page/Apache_Maven.md "wikilink")
  - [Waf](https://ja.wikipedia.org/wiki/:en:Waf "wikilink")
  - [SCons](https://ja.wikipedia.org/wiki/SCons "wikilink")

## 参考文献

『GNU Autoconf/Automake/Libtool』 Gary V. Vaughan, Ben Elliston, Tom Tromey, Ian Lance Taylor著 でびあんぐる監訳 ISBN 4-274-06411-5

## 外部リンク

  - [GNU Autoconf, Automake and Libtool](https://www.sourceware.org/autobook/)
  - [GNU Autoconf home page](https://www.gnu.org/software/autoconf/)
  - [GNU Autoconf macro archive](https://www.gnu.org/software/autoconf-archive/)
  - [*Learning the GNU development tools* @sourceforge](http://autotoolset.sourceforge.net/tutorial.html)
  - [Autotoolset home page](http://autotoolset.sourceforge.net/)
  - チュートリアル:
      - "[Autotools Tutorial](https://www.lrde.epita.fr/~adl/autotools.html)" by Alexandre Duret-Lutz

[Category:GNUプロジェクト](https://ja.wikipedia.org/wiki/Category:GNUプロジェクト "wikilink") [Category:ソフトウェア開発ツール](https://ja.wikipedia.org/wiki/Category:ソフトウェア開発ツール "wikilink") [Category:UNIXのソフトウェア](https://ja.wikipedia.org/wiki/Category:UNIXのソフトウェア "wikilink")
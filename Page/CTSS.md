> この記事は[CTSS](https://ja.wikipedia.org/wiki/CTSS)から翻訳されています。


**CTSS**(Compatible Time-Sharing System、互換タイムシェアリングシステム)は、[MIT計算センターで開発された世界初の](../Page/マサチューセッツ工科大学.md "wikilink")[タイムシェアリングシステム](../Page/タイムシェアリングシステム.md "wikilink")のひとつ。[1961年](https://ja.wikipedia.org/wiki/1961年 "wikilink")に最初の実演が行われ、1973年までMITで稼動していた。当時、MITの [Project MAC](https://ja.wikipedia.org/wiki/Project_MAC "wikilink") にもCTSSの2号機があったが、それ以外のサイトで採用されたことはない。CTSSに関する論文は1962年春季合同コンピュータ会議で発表された。

## 概要

その名称にある "Compatible"（互換）とは [IBM 7094](https://ja.wikipedia.org/wiki/IBM_7094 "wikilink") の標準の[バッチ処理](../Page/バッチ処理.md "wikilink")[OS](../Page/オペレーティングシステム.md "wikilink") FORTRAN Monitor System (FMS) との互換性を意味している。CTSSはバックグラウンド機能で提供された仮想7094上でFMSをそのまま実行することができた（ハードウェアは完全には仮想化できていない）。バックグラウンドFMSジョブは問題なく磁気テープにアクセスできたが、フォアグラウンド[プロセス](../Page/プロセス.md "wikilink")の実行をじゃましたり、それらが使用するリソースを奪うことはできなかった。

CTSSは後世に大きな影響を与えた。タイムシェアリングが可能であることを示し、コンピュータの新たな重要な用途を生み出した。その後のタイムシェアリングシステム（特に[CP/CMS](https://ja.wikipedia.org/wiki/CP/CMS "wikilink")<small>([:en:CP/CMS](https://ja.wikipedia.org/wiki/:en:CP/CMS "wikilink"))</small>）に多大な影響を与え、直接の後継である [Multics](../Page/Multics.md "wikilink") は後のOSの基本概念の多くを生み出した。

## 特徴

  - CTSSには世界初のコンピュータ化された組版ユーティリティの一種 [RUNOFFがあった](https://ja.wikipedia.org/wiki/:en:TYPSET_and_RUNOFF "wikilink")。
  - CTSSには世界初のユーザー間のメッセージ通信機能が実装されており、[電子メール](../Page/電子メール.md "wikilink")の発祥とされることもある\[1\]。
  - MIT計算センターの職員[ルイ・プザン](https://ja.wikipedia.org/wiki/ルイ・プザン "wikilink")はCTSS向けの RUNCOM と呼ばれるコマンドを開発した。これはファイルに書かれているコマンド群を実行するもので、[UNIX](../Page/UNIX.md "wikilink")の[シェルスクリプト](../Page/シェルスクリプト.md "wikilink")の原型である。RUNCOMにはパラメータ置換機能もあった。

## 実装

CTSSは改造された [IBM 7094](https://ja.wikipedia.org/wiki/IBM_7094 "wikilink") メインフレームを使用している。32,768×36ビットワードの[磁気コアメモリ](../Page/磁気コアメモリ.md "wikilink")を2バンク持っている（通常は1個）。うち1バンクはタイムシェアリング管理プログラムが使用し、もう1個をユーザープログラム群が使用する。32Kのうち27Kをユーザーが使用し、残り5Kをモニター用の予約している\[2\]。[CPU](../Page/CPU.md "wikilink")を割り当てる[スケジューリング](../Page/スケジューリング.md "wikilink")は[多段フィードバックキュー](../Page/多段フィードバックキュー.md "wikilink")方式で制御される\[3\]。また、特殊なメモリ管理ハードウェア、クロック割り込み機能、特定の命令をトラップする機能などもあった。入出力ハードウェアはほとんどIBMの標準品である。6本のデータチャネルには以下のデバイスが接続されていた。

  - プリンタ、[パンチカード](../Page/パンチカード.md "wikilink")リーダ、およびパンチャー

  - 磁気テープ装置、[IBM 1301](https://ja.wikipedia.org/wiki/IBMのディスク記憶 "wikilink") ディスク記憶装置（後に3800万ワードの容量を持つ [IBM1302](https://ja.wikipedia.org/wiki/IBMのディスク記憶 "wikilink") にアップグレードされた）

  - IBM 7320 [磁気ドラムメモリ](../Page/磁気ドラムメモリ.md "wikilink")、容量は186Kワードで、1秒で32Kメモリバンクをロードできる（後に、1/4秒までアップグレードされる）

  - 2つの独自高速ベクターグラフィックディスプレイ

  - IBM 7750 伝送制御装置、112台の[テレタイプ端末](../Page/テレタイプ端末.md "wikilink")を接続可能。端末には [IBM 1050](https://ja.wikipedia.org/wiki/IBM_1050 "wikilink") や Model35 [テレタイプ端末](../Page/テレタイプ端末.md "wikilink")などが使われた。いくつかの端末は遠隔地にあり、公衆[テレックス](../Page/テレックス.md "wikilink")回線で接続されていた。

## 影響

Project MAC では、CTSSの後継として1960年代に[Multics](../Page/Multics.md "wikilink")の開発を開始した。Multicsは1969年に[UNIX](../Page/UNIX.md "wikilink")が開発される要因の1つとなった。例えば、「[デーモン](../Page/デーモン_\(ソフトウェア\).md "wikilink")」という用語はCTSS発祥で、UNIXにまで受け継がれた。

[ITS](../Page/Incompatible_Timesharing_System.md "wikilink")(***I**ncompatible **T**imesharing **S**ystem*)もMITで開発された初期の革新的タイムシェアリングシステムのひとつである。これはMulticsの方向性を良しとしない人々が開発した。名称はCTSSのパロディ。

## 脚注

## 参考文献

  - F. J. Corbató, M. M. Daggett, R. C. Daley, *[An Experimental Time-Sharing System](http://larch-www.lcs.mit.edu:8001/~corbato/sjcc62/)* (IFIPS 1962年)
  - [Robert M. Fano](https://ja.wikipedia.org/wiki/ロバート・ファノ "wikilink"), *[The MAC System: A Progress Report](http://www.lcs.mit.edu/publications/pubs/pdf/MIT-LCS-TR-012.pdf)* (MIT Project MAC, 1964年) CTSSの使用方法
  - Jerome H. Saltzer, *[CTSS Technical Notes](http://www.lcs.mit.edu/publications/pubs/pdf/MIT-LCS-TR-016.pdf)* (MIT Project MAC, 1965年) CTSSの実装の詳細
  - Jerome H. Saltzer, *[Manuscript Typing and Editing](http://web.mit.edu/Saltzer/www/publications/AH.9.01.html)* (MIT Computation Center, 1964年) 世界初の電子組版システムについて
  - F. J. Corbató, et al., *[The Compatible Time-Sharing System A Programmer's Guide](http://www.bitsavers.org/pdf/mit/ctss/CTSS_ProgrammersGuide.pdf)* (MIT Press, 1963年) ISBN 978-0-262-03008-3. システムとコマンド群の解説

## 関連項目

  - [フェルナンド・J・コルバト](../Page/フェルナンド・J・コルバト.md "wikilink") - プロジェクトリーダー
  - [オペレーティングシステムの歴史](https://ja.wikipedia.org/wiki/オペレーティングシステムの歴史 "wikilink")

## 外部リンク

  - [Compatible Time-Sharing System (1961-1973): Fiftieth Anniversary Commemorative Overview](http://www.multicians.org/thvv/compatible-time-sharing-system.pdf)
  - [ジョン・マッカーシー](../Page/ジョン・マッカーシー.md "wikilink"), *[Reminiscences on the History of Time Sharing](http://www-formal.stanford.edu/jmc/history/timesharing/timesharing.html)* タイムシェアリングという概念の起源について
  - [Oral history interview with John McCarthy](http://purl.umn.edu/107476), [Charles Babbage Institute](https://ja.wikipedia.org/wiki/チャールズ・バベッジ研究所 "wikilink"), University of Minnesota.
  - [The IBM 7094 and CTSS](http://www.multicians.org/thvv/7094.html): CTSSシステムプログラマの個人的回想
  - [The Origin of the Shell](http://www.multicians.org/shell.html) RUNCOMが後のシェルに与えた影響
  - [CTSS Source](http://www.piercefuller.com/library/ctss.html?id=ctss) Paul Pierce のコレクションより
  - [CIO: 40 years of Multics, 1969-2009](http://www.cio.com.au/article/325323/cio_blast_from_past:_40_years_multics,_1969-2009): フェルナンド・J・コルバトのインタビュー
  - [Oral history interview with Fernando J. Corbató](http://purl.umn.edu/107230), Charles Babbage Institute, University of Minnesota.
  - [Oral history interview with Robert M. Fano](http://purl.umn.edu/107281), Charles Babbage Institute, University of Minnesota.
  - [Dave Pitts' IBM 7094 support](http://www.cozx.com/~dpitts/ibm7090.html) – シミュレータ、クロスアセンブラ、リンカがあり、CTSSをビルド可能。CTSSのソースなどもある。

[Category:オペレーティングシステム](https://ja.wikipedia.org/wiki/Category:オペレーティングシステム "wikilink") [Category:マサチューセッツ工科大学](https://ja.wikipedia.org/wiki/Category:マサチューセッツ工科大学 "wikilink") [Category:1961年のソフトウェア](https://ja.wikipedia.org/wiki/Category:1961年のソフトウェア "wikilink")

1.  Tom Van Vleck's memoir of [The History of Electronic Mail](http://www.multicians.org/thvv/mail-history.html)
2.
3.
> この記事は[Transaction Processing Facility](https://ja.wikipedia.org/wiki/Transaction_Processing_Facility)から翻訳されています。


**Transaction Processing Facility** (**TPF**) は、[IBM](../Page/IBM.md "wikilink")の[メインフレーム](../Page/メインフレーム.md "wikilink")用の、大容量トランザクション処理に特化した[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink") (OS) である。

高い信頼性を持ち、1秒間に最大数万件のトランザクションを処理できるため、[航空路管制](../Page/航空路管制.md "wikilink")や座席予約システム（[CRS](../Page/CRS_\(航空\).md "wikilink")）など航空業界で多く利用される他、金融業界でも使われている。最新版は[System z用の](../Page/System_z.md "wikilink")**z/TPF** V1.1である。

なお同じSystem zで稼動する[z/OS](https://ja.wikipedia.org/wiki/z/OS "wikilink")や[z/VSE](https://ja.wikipedia.org/wiki/z/VSE "wikilink")や[z/VM](https://ja.wikipedia.org/wiki/z/VM "wikilink")などのOSとは、別物である。

## 概要

[SABRE](../Page/SABRE.md "wikilink")から発展し、[1960年代](../Page/1960年代.md "wikilink")中ごろ[IBM](../Page/IBM.md "wikilink")が欧米の主要な航空会社と共同で開発した[Airlines Control Program (ACP)を起源とするOSである](https://ja.wikipedia.org/wiki/:en:Airlines_Control_Program "wikilink")（ACPは無料）。[1979年](../Page/1979年.md "wikilink")、IBMがACPの代替としてTPFを有料の製品として登場させた。その名称は従来よりも適用範囲が広いことを示唆している。

予約システムのユーザーとしては、[SABRE](../Page/SABRE.md "wikilink")、Holiday Inn、[シンガポール航空](../Page/シンガポール航空.md "wikilink")、[KLMオランダ航空](../Page/KLMオランダ航空.md "wikilink")、[カンタス航空](https://ja.wikipedia.org/wiki/カンタス航空 "wikilink")、[アムトラック](../Page/アムトラック.md "wikilink")、[マリオット・インターナショナル](../Page/マリオット・インターナショナル.md "wikilink")、[日本航空](../Page/日本航空.md "wikilink")などがある。また[Visa](../Page/Visa.md "wikilink")（認証システム）、CBOE（[オプション取引](../Page/オプション取引.md "wikilink")の注文システム）、[ニューヨーク市警察](https://ja.wikipedia.org/wiki/ニューヨーク市警察 "wikilink")なども導入している。

TPFは、高速・大量・高スループットの[トランザクション処理](../Page/トランザクション処理.md "wikilink")が可能で、大規模な広域ネットワークでのトランザクションを継続的に大量に処理する。大規模なTPFシステムで毎秒数万トランザクションを処理するのはたやすい。TPFは高信頼でもあり、いわゆる24×7の連続運用が可能である。TPFのユーザーがシステムとソフトウェアのアップグレードを行いつつ10年以上もオンライン処理を継続していることも珍しくない。IBMは類似の[トランザクション処理](../Page/トランザクション処理.md "wikilink")システムとして[CICS](../Page/CICS.md "wikilink")や[IMS](../Page/IMS.md "wikilink")を持っているが、それらとの違いはTPFの大容量/同時ユーザー接続数/高速応答時間などの優位性である。

TPFにはPARSと呼ばれる[アプリケーションがある](../Page/アプリケーションソフトウェア.md "wikilink")。多くの航空会社はPARSまたは国際版の IPARS を座席予約システムに使用している。TPFは性能を重視したため 370[アセンブリ言語](../Page/アセンブリ言語.md "wikilink")で書かれており、アプリケーションも[アセンブリ言語](../Page/アセンブリ言語.md "wikilink")で書かれたものが多数存在する。しかし、最近のTPFは[C言語](../Page/C言語.md "wikilink")を使うようになってきている。TPF 向けの[プログラミング言語](../Page/プログラミング言語.md "wikilink")として SabreTalk という[PL/I](https://ja.wikipedia.org/wiki/PL/I "wikilink")の派生言語があった。TPFの主要コンポーネントはTPFDFと呼ばれる高性能データベースファシリティである。

TPFを採用しているサイトでは、トランザクション処理以外の用途で、他のIBMメインフレーム用オペレーティングシステム（[z/OS](https://ja.wikipedia.org/wiki/z/OS "wikilink")や[z/VM](https://ja.wikipedia.org/wiki/z/VM "wikilink")）も使っていることが多い。逆にz/OS上でTPFから派生したトランザクション処理システムALCSを動作させる場合もある。IBMのパーティショニング技術により、これらのOSは1つのメインフレーム上に共存できる。

TPFのSystem z (z/Architecture)対応である**z/TPF**は2005年に登場した。[64ビット](../Page/64ビット.md "wikilink")に対応しており、[GCCコンパイラを含む](../Page/GNUコンパイラコレクション.md "wikilink")[GNU](../Page/GNU.md "wikilink")ツールが使用可能となっている。

IBMのオープン対応により航空業界以外では入れ替えが進んでおり、[JTB](../Page/JTB.md "wikilink")では基幹システムであるTRIPSを2009年に[System pへ移行した](../Page/System_p.md "wikilink")\[1\]

## オペレーティング環境

### 密結合

TPF は[マルチプロセッサ](https://ja.wikipedia.org/wiki/マルチプロセッサ "wikilink")での動作が可能である。TPF のプログラムはリエントラントであるため、マルチプロセッサであっても全く問題なく動作する。立ち上がり時にメインのCPUが決定される。プログラムは[APIによって明示的に使用するCPUを指定される](../Page/アプリケーションプログラミングインタフェース.md "wikilink")。z/TPFでは、CPUを指定しないで起動されたアプリケーションは負荷バランスを調整するようになっている。

TPFアーキテクチャでは、各CPUはメモリを共有するが、CPU毎の固有領域が4Kバイトずつ存在する。アプリケーションでCPU毎に固有のメモリ領域が必要な場合、各CPUに同サイズの領域を割り当てるようアプリケーションを設計する。例えば、この方式でTPFではCPU毎にユニークなグローバル変数をサポートしている。このような領域へのアクセスはベースアドレスに自動的にCPU番号に相当する値を加算することで行われる。

### 疎結合

TPFは複数台のメインフレームを共通のデータベースに接続したシステムでも動作する。TPFのデータベースは最大32台のメインフレームで共有可能である。最も単純な疎結合システムは、2台のメインフレームを1台のDASD (Direct Access Storage Device) に結合したものである。この場合、制御プログラムは各メインフレームに置かれ、どのメインフレームからも同じデータベースにアクセス可能である。

疎結合システムでアクセスをシリアライズするため[レコードロック](https://ja.wikipedia.org/wiki/レコードロック "wikilink")と呼ばれる手法が使われる。これは、レコードをあるプロセッサが保持している場合、他のプロセッサが同じレコードを保持しようとした際にそれらを待たせ、プロセッサ間で通信を行う方式である。密結合システムではレコードロックの状況を共有メモリ上に書いておけばよいので簡単だが、疎結合システムではDASD制御装置での追加の処理が必要となる。歴史的にはこの機能は**RPQ**（個別対応）とされていた。そのため、RPQ対応されていないDASDでは、**Coupling Facility**という別のレコードロック方式が使われている。

## 特徴

  - TPFは[GUIを持たず](https://ja.wikipedia.org/wiki/グラフィカルユーザインターフェース "wikilink")、単純な[CUIが使われる](../Page/キャラクタユーザインタフェース.md "wikilink")。従って、マウスもウィンドウもアイコンもない。
  - TPFにはコンパイラ、アセンブラ、テキストエディタといったものもない。TPF向けアプリケーション開発はz/OS上などで行われる。z/TPFでは[Linux](../Page/Linux.md "wikilink")上に開発環境がある。
  - TPFにはオンラインマニュアル等もないので、紙のマニュアルを読まなければならない。TPF用のIBM製コマンド群は "Z" で始まる名前が付いている。従って、ユーザーは一般に "Z" 以外で始まる名前をコマンドにつける。
  - TPFにはデバッグ機能がほとんどない。通常、z/VM上でTPFを動作させることが多いので、VMの持つトレース機能が利用できる。
  - TPFはトランザクションを含めたメッセージのやりとりを高速化するよう最適化されている。
  - TPFは高速化のため、メモリ上にプログラム全体をロードして実行する方式であった。このためかつてのTPF用プログラムは4Kバイトに制限されていた。z/TPFではC言語を使うようになったため、この制限はない（というよりも実際問題としてアセンブラ以外で4Kバイトにサイズを制限されてもほとんど何もできない）。

## 参照

<references />

## 外部リンク

  - [z/TPF](https://www.ibm.com/it-infrastructure/z/transaction-processing-facility)（英文）
  - [TPF User Group](http://www.tpfug.org) （TPFユーザーグループ）
  - [Blackbeard](http://www.blackbeard.com/tpf/) (Alternative TPF Homepage)
  - [日本IBM・プレスリリース 日本航空の航空券予約・発券システムをSystem zで更新](http://www-06.ibm.com/jp/press/2008/03/2601.html)（z/TPF V1.1 の世界初の採用事例）

[Category:IBMのオペレーティングシステム](https://ja.wikipedia.org/wiki/Category:IBMのオペレーティングシステム "wikilink") [Category:メインフレームのオペレーティングシステム](https://ja.wikipedia.org/wiki/Category:メインフレームのオペレーティングシステム "wikilink") [Category:リアルタイムオペレーティングシステム](https://ja.wikipedia.org/wiki/Category:リアルタイムオペレーティングシステム "wikilink") [Category:1979年のソフトウェア](https://ja.wikipedia.org/wiki/Category:1979年のソフトウェア "wikilink")

1.  [【事例編】JTB、基幹系プラットフォームを刷新 - 進化するITプラットフォーム Part8](https://it.impressbm.co.jp/articles/-/6719)
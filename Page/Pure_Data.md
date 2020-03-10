> この記事は[Pure Data](https://ja.wikipedia.org/wiki/Pure_Data)から翻訳されています。


**Pure Data**（**Pd**）は、1990年代に[ミラー・パケット](https://ja.wikipedia.org/wiki/ミラー・パケット "wikilink")(Miller Puckette) が開発した[デスクトップミュージック](../Page/デスクトップミュージック.md "wikilink")と[マルチメディア](../Page/マルチメディア.md "wikilink")作成用の[ビジュアルプログラミング言語](https://ja.wikipedia.org/wiki/ビジュアルプログラミング言語 "wikilink")である。Puckette が主に開発したが、Pd は[オープンソース](../Page/オープンソース.md "wikilink")プロジェクトであり、多数の開発者が参加している。[BSD License](https://ja.wikipedia.org/wiki/BSD_License "wikilink") に似たライセンス条件でリリースされている。

## 概要

Pd はその対象領域も設計も Puckette が以前（[IRCAM](https://ja.wikipedia.org/wiki/IRCAM "wikilink")在籍時）に開発した [Max](https://ja.wikipedia.org/wiki/Max/MSP "wikilink") に似ており、Max の商用の後継である [Max/MSP](https://ja.wikipedia.org/wiki/Max/MSP "wikilink") とある程度相互運用が可能である。Pd も Max も典型的な[データフロープログラミング](https://ja.wikipedia.org/wiki/データフロープログラミング "wikilink")言語である。グラフィカルな環境で関数や「オブジェクト」が相互にリンクされ、制御フローや音響の流れを表す。Pd では音声処理などもホスト[CPU](../Page/CPU.md "wikilink")上で行われる。これは、Max/FTS において[DSPボード](https://ja.wikipedia.org/wiki/デジタルシグナルプロセッサ "wikilink")（Ariel ISPW）に[信号処理](https://ja.wikipedia.org/wiki/信号処理 "wikilink")や[合成](https://ja.wikipedia.org/wiki/合成 "wikilink")を任せていたのと対照的である。Pd のコードは David Zicarelli による Max の MSP 拡張（ソフトウェア音声処理）のベースとなった。

Max と同様、Pd はソフトウェアで部品として利用できる[モジュール](https://ja.wikipedia.org/wiki/モジュール "wikilink")コードベース（外部および内部）を備えている。拡張可能な[APIを備え](../Page/アプリケーションプログラミングインタフェース.md "wikilink")、[C言語](../Page/C言語.md "wikilink")で書かれた部品を流用したり、他の外部部品を活用することで[Python](../Page/Python.md "wikilink")、[Ruby](../Page/Ruby.md "wikilink")、[Scheme](../Page/Scheme.md "wikilink")などの言語で書かれたモジュールも活用できる。ただし、Pd 自身もプログラミング言語である。Pd で書かれた流用可能なコードは「パッチ」または「アブストラクション」と呼ばれ、フリーなプログラムとして流通している。また、他のプログラミング言語の知識が無くとも Pd の利用には何の問題もない。

外部リンクの節には Pure Data の様々な外部モジュールがリストアップされている。GEM（Graphical Environment for MultiMedia）は他の外部モジュール（Pure Data Packet、PiDiPi、Framestein、GridFlow）のベースとなっていると同時に、[OpenGL](../Page/OpenGL.md "wikilink")画像や動画のリアルタイム操作を可能としている。

また、Pd はネットワークやインターネット上での共同作業が可能であり、リアルタイムで遠隔にいる人々が共同で音楽を作成するといった利用が可能である。

Pd は[デジタル信号処理](https://ja.wikipedia.org/wiki/デジタル信号処理 "wikilink")ソフトウェアとして、44100 サンプル毎秒の[サンプリング周波数](../Page/サンプリング周波数.md "wikilink")と64サンプル毎に1ブロックの制御レートを実現している（いずれも設定の変更が可能である）。制御メッセージや音声信号は一般に画面の上から下に繋がっているオブジェクト間を流れていく。

フリーウェアであるため無料で利用できるが、商用のMax/MSPと比較すれば処理速度・機能面・安定性では劣ると評価されている。

## 言語機能

Pd は、アトム、メッセージ、オブジェクト、コメントという4種類の基本テキストをサポートする。

### アトム

アトムとは、 Pd における基本データ単位のことで、[浮動小数点数](../Page/浮動小数点数.md "wikilink")かシンボルか他のデータ構造へのポインタのいずれかである。なお、Pd では全ての数値は 32ビットの浮動小数点数である。入力データは、ファイルから読み込んだり、[FireWire](https://ja.wikipedia.org/wiki/IEEE1394 "wikilink")、[USB](../Page/ユニバーサル・シリアル・バス.md "wikilink")、ネットワークなどから [OpenSound Control](https://ja.wikipedia.org/wiki/OpenSound_Control "wikilink") (OSC) 経由で何らかのオーディオボードや[MIDI](../Page/MIDI.md "wikilink")を読み込んだり、その場で生成したりする。結果をテーブルに保持して、それを新たな入力に使用することもできる。

### メッセージ

メッセージとは、1つ以上のアトムから構成され、オブジェクトへの命令として働く。中身のない特別なメッセージを *bang* と呼び、データの流れを開始させるスタートボタンのような役目を持っている。

### オブジェクト

Pd の基本オブジェクトは、[算術](../Page/算術.md "wikilink")演算、[論理演算](../Page/論理演算.md "wikilink")、[ビット演算](https://ja.wikipedia.org/wiki/ビット演算 "wikilink")といった通常のプログラミング言語にある演算子のようなものから、波形発信器や[高速フーリエ変換](../Page/高速フーリエ変換.md "wikilink")や各種[デジタルフィルタ](https://ja.wikipedia.org/wiki/デジタルフィルタ "wikilink")などの音声処理DSP機能に特化したもの（チルダ(\~)が付いていて区別される）まである。

## データ構造

Pd の特筆すべき機能は、[データ構造](../Page/データ構造.md "wikilink")を視覚的に表現できることである。これには様々な応用が考えられ、作曲やイベントの順序付けから、視覚的な作品を作ったり、Pd 自体の[GUIを拡張したりできる](https://ja.wikipedia.org/wiki/グラフィカルユーザインタフェース "wikilink")。

Pure Data（純粋なデータ）の名の通り、Pd のデータ構造は音楽データを静止画としても動画としても表現できる。C言語の構造体のように Pd のデータ構造は様々なデータで構成でき、データ構造の視覚化をデータ構造でパラメータ指定することで制御したり、Pd のパッチ内でのメッセージや音声信号を制御したりできる。Puckette は以下のように記している。

  -
    Pd はデータ構造とそのグラフィカルな外観を記述するために全く構造化されていない環境を提供するよう設計されている。根底にある考え方は、ユーザーが任意のデータを任意の見せ方で表示できるようにすることである。このため、Pd では C言語などとは全く異なる、データに形や色を与える視覚的なデータ構造を導入し、ユーザーがデータを視覚的に編集できるようにした。データは内部で編集することも、ファイルから読み込むことも、アルゴリズムによって生成することも、入力音声やデータを解析することで作成することもできる。
      -
        — Miller Puckette、[Pd Documentation Chapter 2 — 2.9. Data structures](http://crca.ucsd.edu/~msp/Pd_documentation/x2.htm#s9)

## サンプルコード

1.  パッチ1は"Hello world"を端末にプリントする。
2.  パッチ2は、入力チャンネル1からの信号にリバーブを適用し、出力チャンネル1と2に出力する。
3.  パッチ3の例はより複雑で、まず最初にホワイトノイズに9000ヘルツのバンドパスフィルターを掛け、続いて1秒間に0.5秒のフェードイン/フェードアウト(line\~)が合成(\*\~)される。Pdでは、時間はミリ秒の単位で計測されるため、'1000'は1秒を表し、'500'は0.5秒を表す。

## 関連項目

  - [Max/MSP](https://ja.wikipedia.org/wiki/Max/MSP "wikilink")
  - [reacTable](https://ja.wikipedia.org/wiki/reacTable "wikilink")
  - [Jeskola Buzz](https://ja.wikipedia.org/wiki/Jeskola_Buzz "wikilink")

## 参考文献

  - Danks, M. (1996). The graphics environment for max. In: Proceedings of the International Computer Music Conference, pp. 67-70. International Computer Music Association.
  - Danks, M. (1997). Real-time image and video processing in Gem. In: Proceedings of the International Computer Music Conference, pp. 220-223. International Computer Music Association.
  - Puckette, M. S. (1997). Pure data. In: Proceedings of the International Computer Music Conference, pp. 224-227. International Computer Music Association.
  - Puckette, M. S. (2004?-). The Theory and Technique of Electronic Music. オンライン版は[こちら](http://www-crca.ucsd.edu/~msp/techniques.htm)

## 外部リンク

  - [Software by Miller Puckette](http://www-crca.ucsd.edu/~msp/software.html) — Pd の最新版、文書、ソースコード

  - [Pure Data Japan](http://puredatajapan.info) — Pure Dataの日本語ポータル、チュートリアル、フォーラム、リンク集など（日本語）

  - Pure Dataで作るソフトウェア・ラジオ（日本語）

  - [Patches for HAM Radio](http://geocities.yahoo.co.jp/gl/e_karakuri) アマチュア無線用パッチ等（日本語）

  - [Pure Data](http://megaui.net/oss4art/wiki/Pure_Data) Oss4Art（日本語）

  - [PureDataLab](http://nul.jp/puredata/)（日本語）

  - [pddoc](http://de-dicto.net/pd/)（日本語）

  - [Pure Data Portal](http://puredata.info/)

  - [PD Webring](http://pd.klingt.org/webring/)

  - [Pd forum](http://puredata.hurleur.com/)

  - [rradical pd](http://footils.org/cms/) by Frank Barknecht

  - [RTC-lib](http://www.essl.at/works/rtc.html) — Karlheinz Essl の Pd 用 *Real Time Composition Library*

  - [Pure Data External Repository](http://pure-data.sourceforge.net/)

  - [GEM](http://gem.iem.at/) — Graphics Environment for Multimedia（Pd 用プラグイン）

  - [netpd](http://www.netpd.org/) Pd-ベースのネットワーク接続リアルタイム共同作業環境

  - [GridFlow](http://gridflow.ca)

  - [Pure Data Packet](http://zwizwa.fartit.com/pd/pdp/doc/)

  - [PiDiP Is Definitely In Pieces](http://ydegoyon.free.fr/pidip.html)

  - [Framestein](http://framestein.org/) — Pure Data を使った静止画/動画処理ソフトウェア

  - [pure:dyne](http://puredyne.goto10.org/) — Pure Data 環境を含む GNU/Linux liveCD

  - [Obiwannabes tutorials](http://www.obiwannabe.co.uk/) — Pure Data による音響設計のチュートリアル

[Category:音声処理ソフト](https://ja.wikipedia.org/wiki/Category:音声処理ソフト "wikilink") [Category:オープンソースソフトウェア](https://ja.wikipedia.org/wiki/Category:オープンソースソフトウェア "wikilink") [Category:コンピュータミュージック](https://ja.wikipedia.org/wiki/Category:コンピュータミュージック "wikilink") [Category:プログラミング言語](https://ja.wikipedia.org/wiki/Category:プログラミング言語 "wikilink") [Category:ソフトウェア・シンセサイザー](https://ja.wikipedia.org/wiki/Category:ソフトウェア・シンセサイザー "wikilink") [Category:音楽ソフトウェア](https://ja.wikipedia.org/wiki/Category:音楽ソフトウェア "wikilink") [Category:VJ](https://ja.wikipedia.org/wiki/Category:VJ "wikilink")
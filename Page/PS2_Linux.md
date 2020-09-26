> この記事は[PS2 Linux](https://ja.wikipedia.org/wiki/PS2_Linux)から翻訳されています。


**PS2 Linux**（ピーエスツー・リナックス）は、[2001年](../Page/2001年.md "wikilink")[5月9日](../Page/5月9日.md "wikilink")に発売された[PlayStation 2用](../Page/PlayStation_2.md "wikilink")[Linuxディストリビューション](../Page/Linuxディストリビューション.md "wikilink")である。

発売元はソニー・コンピュータエンタテインメント（現: [ソニー・インタラクティブエンタテインメント](https://ja.wikipedia.org/wiki/ソニー・インタラクティブエンタテインメント "wikilink")）。

## 経緯

もともと、PS2の開発環境はLinuxベースであることが知られており\[1\]、「[SCEI](https://ja.wikipedia.org/wiki/SCEI "wikilink")はLinuxに積極的なようだ」「PS2でもLinuxが動くのではないか」という期待が高まっていた。

そのような状況で、SCEの[久夛良木健](../Page/久夛良木健.md "wikilink")社長（当時）が、[日本Linux協会](../Page/日本Linux協会.md "wikilink")の生越昌己会長に対し「（PS2で動くLinuxは）出そうと思えば明日にも出せる」と発言したことから、[2001年](../Page/2001年.md "wikilink")[3月4日](../Page/3月4日.md "wikilink")にネット上で「PS2で動作するLinuxの発売を求める署名運動」が開始された。

## 沿革

  - [2001年](../Page/2001年.md "wikilink")
      - 4月26日 - SCEIからPS2 Linuxを発売することが公式に発表された。
      - 5月9日 - 午後2時、ベータ版の予約注文の受付。予約注文が殺到したため、わずか8分で予定台数である2000セットに達し、約3500セット分のキャンセル待ち状態が発生した。
      - 5月19日 - 7000セットを追加生産することが発表された。最終的に、この初期版は合計で約7900セット出荷された。
  - [2002年](../Page/2002年.md "wikilink")
      - 1月30日 - 正式版 (Release 1.0) が発表
      - 2月13日 - 正式版の受注開始。

## ハードウェア

PS2 Linuxはソフトウェア媒体だけではなく、[HDDユニット](https://ja.wikipedia.org/wiki/ハードディスクドライブ "wikilink")、[イーサネット](../Page/イーサネット.md "wikilink")アダプタ、[USBキーボード](../Page/ユニバーサル・シリアル・バス.md "wikilink")、USBマウス、[VGAケーブルとセットで販売された](../Page/Video_Graphics_Array.md "wikilink")。後日、正式版が販売された時点でベータ版購入者には媒体のみの販売が行われた。

### キーボード・マウス

後に純正周辺機器として販売された物と同等品である。

一部のPS2ゲームソフトとは異なり、Linuxでは専用品であるか否かのチェックを行わないので、CPU切り替え機等に接続する等の運用も可能である。

### 画面出力

[VGAケーブルより出力される信号は](../Page/Video_Graphics_Array.md "wikilink")、同期信号を専用の信号線に出力する一般的なタイプではなく、緑色の画像信号に重畳させて出力するSync on Greenという方式を取っている。このため、対応できるディスプレイが限られ、ユーザを悩ますこととなった。

ちなみに、プログレッシブ出力（480p）に対応する一部のPS2用ソフトもVGA出力に対応しているが、VGAケーブルは純正品としては発売されていないため、貴重なケーブルでもある。

通常はVGAケーブルでしか映像出力できないが、一般的なTVに出力させるにはSELECT+R1を押しながら起動することで、Runtime EnvironmentとCUIの映像出力をNTSCで出力できる。[X Window Systemの映像出力をNTSCにしたい場合](../Page/X_Window_System.md "wikilink")、 `$ startx -- -screen 0 NTSC` のようにオプションの指定が必要となる\[2\]。

### HDD・イーサネットアダプタ

添付されている[HDDユニットと](https://ja.wikipedia.org/wiki/ハードディスクドライブ "wikilink")[イーサネット](../Page/イーサネット.md "wikilink")アダプタは、後に発売されたHDDユニットや[PlayStation BB Unitと同じものであるが](../Page/PlayStation_BB_Unit.md "wikilink")、HDDユニットに添付されている「HDDユーティリティディスク」や、BB Unitに添付されている[PlayStation BB Navigatorは添付されていない](https://ja.wikipedia.org/wiki/PlayStation_BB_Unit#PlayStation_BB_Navigator "wikilink")。しかし、後にBB Unitのユーザー向けにBB Navigatorのバージョンアップディスクが実費で提供されたため、これを利用することでBB Unitと同等の環境を構築することも可能である。

2017年頃にはBB Navigatorのサポートは終了してしまい、PS2 Linuxの操作で可能であったBB Navigatorへのtelnetによるログインや、BB Navigatorでのメールの送受信、ネットワーク経由でのBB Navigatorのアップデートは使用できなくなった。

### その他

Blackrhino GNU/Linuxでは、PS2の[EyeToy](../Page/EyeToy.md "wikilink")にも対応している。

## ソフトウェア

[RedHat系](https://ja.wikipedia.org/wiki/Kondara_MNU/Linux "wikilink") [Kondara MNU/Linux](https://ja.wikipedia.org/wiki/Kondara_MNU/Linux "wikilink") ベースのディストリビューションである。ディストリビューションの持つ一般的なソフトウェアの他に、CPU (Emotion Engine) やGS (Graphics Synthesizer) に関するドキュメント、ツール、およびサンプルプログラムを含んでいる。また `sdr` （ウィンドウマネージャの設定）や `mgedit` などKondara MNU/Linux由来のツールも入っている。

後日Debian系のBlackrhino GNU/LinuxもPS2 Linuxの公式コミュニティで発表され、RedHat系とDebian系の共存が可能になった。これにより、2種類のディストリビューションから一方を選択して起動することができるようになった。他に [Gentoo Linux](../Page/Gentoo_Linux.md "wikilink") もポーティングが発表された。

Blackrhino GNU/Linuxは後にKernel Loader Projectに発展し、PS2 Linux KitがなくともPS2本体とKernelLoader.elfの起動環境があればUSBメモリから起動して使えるようになった。

### ブートプロセス

インストール時にPS2用メモリーカードをフォーマットし、そこに[Linuxカーネル](../Page/Linuxカーネル.md "wikilink")と設定ファイルをインストールする。このメモリーカードとPS2 Linux Kit付属の[DVD-ROM](https://ja.wikipedia.org/wiki/DVD-ROM "wikilink")を挿入して電源を入れると、DVD-ROMから "Runtime Environment for PS2 Linux 1.0" というプログラムが起動する。ここからDVDとメモリーカード上のカーネルの二つを読み込み、起動する。カーネルをアップグレードする時は、PS2用メモリーカードにアップグレードしたいカーネルをコピーすると使用可能になる。

## ブームの終焉

発売前後、PS2 Linuxはブームとなり、Linux Magazine誌にPS2 Linuxプログラミングの連載が組まれるまでに至った。しかし、リリース後実際に使っていく上で、以下のようなさまざまな難点が判明した。

  - [PlayStation 2の性能を生かしたプログラミングが非常に難しい](../Page/PlayStation_2.md "wikilink")
  - PS2 LinuxからはPS2のDVD-ROMドライブやメモリーカードにアクセスできない
  - ゲーム向けの機能を利用しない単なるLinuxマシンとしてのPS2は、300MHzの[MIPSプロセッサ](../Page/MIPSアーキテクチャ.md "wikilink")(R5900)に32MBの[RDRAM](../Page/RDRAM.md "wikilink")と貧弱だった
  - バイナリパッケージが不十分で、ディストリビューションにないプログラムを追加するには苦労して実機で[コンパイルするか](../Page/コンパイラ.md "wikilink")、PCで環境を整えて[クロスコンパイル](https://ja.wikipedia.org/wiki/クロスコンパイル "wikilink")する必要があった
  - PS2の演算性能に期待して科学技術計算用途を考える者もいたが、ハードウェアでは単精度浮動小数点数しかサポートしていないため、実用的ではなかった

PS2 Linuxユーザーコミュニティの活発さは急速に衰えていった。結局、PS2 Linuxは試験的に数千本を提供したのみで販売停止されている。公式の供給は完全に停止したものの、HDDを必要としない手法で動作するPS2 Linuxは有志の活動でパッケージが発表されていった。カーネルもアップグレードしていき、Blackrhino版・Debian版・Juhutube版と数種のPS2用のLinuxが存在している。

## 脚注

### 注釈

### 出典

## 外部リンク

  - [PlayStation2 で動作するLinuxを公開してもらうための署名運動（Internet Archive）](http://web.archive.org/web/20040422045148/http://www.peanuts.gr.jp/pslinux/index.html.ja)
  - [Linux for PlayStation 2 Community](http://playstation2-linux.com/) 米国およびヨーロッパ諸国におけるPS2 Linuxコミュニティのポータル。
  - [Linux (for PlayStation 2) Release 1.0 Official Home Page](http://www.ps2linux.com/)
  - [Progressive Club（Internet Archive）](http://web.archive.org/web/20090225192044/http://tokyo.cool.ne.jp/xiaolang/pclub/): PS2 Linuxに使用するVGAケーブルを他のゲームソフトに生かす情報のサイト

[Category:Red_Hat派生ディストリビューション](https://ja.wikipedia.org/wiki/Category:Red_Hat派生ディストリビューション "wikilink") [Category:PlayStation_2用ソフト](https://ja.wikipedia.org/wiki/Category:PlayStation_2用ソフト "wikilink") [Category:日本のLinux開発](https://ja.wikipedia.org/wiki/Category:日本のLinux開発 "wikilink") [Category:2001年のソフトウェア](https://ja.wikipedia.org/wiki/Category:2001年のソフトウェア "wikilink")

1.  開発機材に接続されるPCがLinuxベースであるというだけで、PS2でLinuxが動いていたわけではない。
2.  [茶の間で使えるLinux～ PS2 Linuxを使い倒そう ～ PS2 Linuxの環境設定(2)](http://news.mynavi.jp/special/2001/ps2linux/004.html)
> この記事は[PS2 Linux](https://ja.wikipedia.org/wiki/PS2_Linux)から翻訳されています。


**PS2 Linux**（ピーエスツー・リナックス）は、[2001年](../Page/2001年.md "wikilink")[5月9日](https://ja.wikipedia.org/wiki/5月9日 "wikilink")に発売された[PlayStation 2用](https://ja.wikipedia.org/wiki/PlayStation_2 "wikilink")[Linuxディストリビューション](../Page/Linuxディストリビューション.md "wikilink")。

発売元はソニー・コンピュータエンタテインメント (SCE) （現：[ソニー・インタラクティブエンタテインメント](https://ja.wikipedia.org/wiki/ソニー・インタラクティブエンタテインメント "wikilink") (SIE) ）。

## 発売に至った経緯

もともと、PS2の開発環境はLinuxベースであることが知られており（ただし、開発機材に接続されるPCがLinuxベースであるというだけで、よく誤解されていたようにPS2でLinuxが動いていたわけではない）、「[SCEI](https://ja.wikipedia.org/wiki/SCEI "wikilink")はLinuxに積極的なようだ」「PS2でもLinuxが動くのではないか」という期待が一部で高まっていた。

そのような状況で、SCEの[久夛良木健](../Page/久夛良木健.md "wikilink")社長（当時）が、[日本Linux協会](https://ja.wikipedia.org/wiki/日本Linux協会 "wikilink")の生越昌己会長に対し「（PS2で動くLinuxは）出そうと思えば明日にも出せる」と発言したことから、ネット上で「PS2で動作するLinuxの発売を求める署名運動」が開始された。[2001年](../Page/2001年.md "wikilink")[3月4日](../Page/3月4日.md "wikilink")のことである。

## 沿革

  - [2001年](../Page/2001年.md "wikilink")
      - 4月26日 - SCEIからPS2 Linuxを発売することが公式に発表された。
      - 5月9日 - 午後2時、ベータ版の予約注文の受付。予約注文が殺到したため、わずか8分で予定台数である2000セットに達し、約3500セット分のキャンセル待ち状態が発生した。
      - 5月19日 - 7000セットを追加生産することが発表された。最終的に、この初期版は合計で約7900セット出荷された。
  - [2002年](../Page/2002年.md "wikilink")
      - 1月30日 - 正式版(Release 1.0)が発表
      - 2月13日 - 正式版の受注開始。

## 内容

### ハードウェア

PS2 Linuxはソフトウェア媒体だけではなく、[HDDユニット](https://ja.wikipedia.org/wiki/ハードディスクドライブ "wikilink")、[イーサネット](../Page/イーサネット.md "wikilink")アダプタ、[USBキーボード](../Page/ユニバーサル・シリアル・バス.md "wikilink")、USBマウス、[VGAケーブルとセットで販売された](../Page/Video_Graphics_Array.md "wikilink")。後日、正式版が販売された時点でベータ版購入者には媒体のみの販売が行われた。

#### キーボード、マウス

後に純正周辺機器として販売された物と同等品である。

一部のPS2ゲームソフトとは異なり、Linuxでは専用品であるか否かのチェックを行わないので、CPU切り替え機等に接続する等の運用も可能である。

#### VGAケーブル

[VGAケーブルより出力される信号は](../Page/Video_Graphics_Array.md "wikilink")、同期信号を専用の信号線に出力する一般的なタイプではなく、緑色の画像信号に重畳させて出力するSync on Greenという方式を取っている。このため、対応できるディスプレイが限られ、ユーザを悩ますこととなった。

なお、プログレッシブ出力（480p）に対応する一部のPS2用ソフトもVGA出力に対応しているが、VGAケーブルは純正品としては発売されていないため、ある意味貴重なケーブルである。

通常はVGAケーブルでしか映像出力できないが、通常のTVに出力させるにはSELECT+R1を押しながら起動することで、Runtime EnvironmentとCUIの映像出力をNTSCで出力できる。GUIの映像出力をNTSCにしたい場合、コマンドの入力(通常のLinuxは$ startx)でX-Windowが起動するが。PS2LinuxをNTSC出力させる時には($ startx -- -screen 0 NTSC)等$ startxコマンドのoptionの指定が必要となる。\[1\]。

#### HDDユニット、イーサネットアダプタ

添付されている[HDDユニットと](https://ja.wikipedia.org/wiki/ハードディスクドライブ "wikilink")[イーサネット](../Page/イーサネット.md "wikilink")アダプタは、後に発売されたHDDユニットや[PlayStation BB Unitと同じものであるが](../Page/PlayStation_BB_Unit.md "wikilink")、HDDユニットに添付されている「HDDユーティリティディスク」や、BB Unitに添付されている[PlayStation BB Navigatorは添付されていない](https://ja.wikipedia.org/wiki/PlayStation_BB_Unit#PlayStation_BB_Navigator "wikilink")。 しかし、後にBB Unitのユーザー向けにBB Navigatorのバージョンアップディスクが実費で提供されたため、これを利用することでBB Unitと同等の環境を構築することも可能である。

2017頃にはSONYのB.B.Navigatorのサポートは終了してしまいPS2Linuxの操作で可能であったB.B.Navigatorにコマンド($ telnet "B.B.NavigatorのIPaddress" 23)でloginしたり、B.B.Navigatorでのメールの送受信機能、ネットワーク経由でのB.B.Navigatorのアップデートは使用できなくなる。

### ソフトウェア

[RedHat系](https://ja.wikipedia.org/wiki/Kondara_MNU/Linux "wikilink")"[Kondara MNU/Linux](https://ja.wikipedia.org/wiki/Kondara_MNU/Linux "wikilink")"ベースのディストリビューションである。一般的なRPMベースのディストリビューションの持つソフトウェアの他に、[PlayStation 2のCPU](https://ja.wikipedia.org/wiki/PlayStation_2 "wikilink")(EmotionEngine)やGS(GraphicsSynthesizer)の機能に関するドキュメントおよびツールやサンプルプログラムを含んでいる。また、コマンドである $ sdr (WindowManagerの設定)や $ mgedit などのKondara MNU/Linux由来のツールも入っている。

Debian系"Blackrhino GNU/Linux release 1.0"　というディストリビューションもPlayStation2LinuxのOFFICIALのコミュニティーで発表され、PS2LinuxのHDDにインストールをして使えるようになりRedHat系とDebian系のディストリビューションの共存が可能になる。

共存とはHDDの中に２種類のディストリビューションが存在し起動時"RunTimeEnvironment"で起動するディストリビューションを選択してどちらか一方の起動になる。

その後"GentooLinux"も参加。

"Gentoo-PS2 1.4" のインストール方法はPS2LinuxComunityで発表がされています。

その後のBlackrhino GNU/Linuxは無償なProject(KernelLoaderProject)となり、USB(FlashMemory)から起動するプログラムがリリースされ、PS2LinuxのHDDにインストールをしなくてもPS2LinuxKitを使用しなくてもPS2本体とKernelLoader.ELFの起動環境があればUSB-Memoryから起動して使えるようになる。

#### ブートプロセス

インストール時にPS2用メモリーカードをフォーマットし、そこに[Linuxカーネル](../Page/Linuxカーネル.md "wikilink")と設定ファイルをインストールすることとなる。 PS2 Linux Kit付属のDVD-ROMとこのメモリーカードを挿入し、電源を入れると [DVD-ROM](https://ja.wikipedia.org/wiki/DVD-ROM "wikilink") から "Runtime Environment for PS2 Linux 1.0" なるプログラムが起動する。ここからDVDとメモリーカード上のカーネルの二つを読み込み、起動する。 後からカーネルをアップグレード時にはPS2用メモリーカードにアップグレードしたカーネルをコピーする事でアップグレードしたカーネルの使用も可能になる。

## 一瞬のブーム

発売前後、PS2 Linuxはブームとなり、Linux Magazine誌にPS2 Linuxプログラミングの連載が組まれるまでに至った。しかし、リリース後実際に使っていく上で、以下のようなさまざまな難点が判明した。

  - Linux Magazine誌の連載によって、[PlayStation 2の性能を生かしたプログラミングの技術が非常に難しいものであることが明らかとなった](https://ja.wikipedia.org/wiki/PlayStation_2 "wikilink")。
  - PS2 LinuxからはPS2のDVD-ROMドライブやメモリーカードにアクセスできないようになっていた。
  - ゲーム向けの機能を利用しない単なるLinuxマシンとしてのPS2は、300MHzの[MIPSプロセッサ](https://ja.wikipedia.org/wiki/MIPSアーキテクチャ "wikilink")(R5900)に32MBの[RDRAM](https://ja.wikipedia.org/wiki/RDRAM "wikilink")という貧弱な性能にすぎなかった。
  - バイナリパッケージも不十分であったため、何かソフトをインストールしようとすると、毎回苦労して[セルフコンパイルするか](../Page/コンパイラ.md "wikilink")、PCで環境を整えて[クロスコンパイル](https://ja.wikipedia.org/wiki/クロスコンパイル "wikilink")する必要があった。
  - PS2の演算性能に期待して科学技術計算用途を考えていた者もいたが、ハードウェアでは単精度浮動小数しかサポートしていないため、およそ実用的ではなかった。

このためPS2 Linuxユーザーコミュニティの活発さは急速に衰えていった。結局、PS2 Linuxは試験的に数千本を提供したのみで販売停止されている。 一方のHDDを必要としないPS2Linuxは有志の活動でフリーなパッケージが発表されてゆき,これらは無償でダウンロードをしてPS2本体付属のUSB(FlashMemoryやSD-Card)とPS2専用のメモリーカードに入れた(プログラム名：KernelLoader.ELF)から起動するPS2 Linux live version.3になる。 PS2Linuxのカーネルもアップグレードしていき、Blackrhino版・Debian版・Juhutube版と数種のPS2用のLinuxが存在する。

Blackrhino GNU/LinuxではPS2のUSB-camera(EyeToy)にも対応をしている。

## その他

PS2 LinuxのDVD内には、[Emotion Engineと](https://ja.wikipedia.org/wiki/Emotion_Engine "wikilink")[Graphics Synthesizerと](https://ja.wikipedia.org/wiki/Graphic_Synthesizer "wikilink")[SampleのProgramが１作品](https://ja.wikipedia.org/wiki/SampleのProgramが１作品 "wikilink")と[PlayStation2のハードウェアに関する説明](https://ja.wikipedia.org/wiki/PlayStation2のハードウェアに関する説明 "wikilink")が英語・日本語(英語より少し新しいようです)の両方の形式で含まれている。

## 出典

<references />

\[参考サイト\] 1.VECTOR PS2Linuxをいじる

2.PS2Linux Entertainment(2019/05/31現在)このページにはアクセスできません

## 外部リンク

  - [PlayStation2 で動作するLinuxを公開してもらうための署名運動（Internet Archive）](http://web.archive.org/web/20040422045148/http://www.peanuts.gr.jp/pslinux/index.html.ja): すべての始まりとなったページ。
  - [Linux for PlayStation 2 Community](http://playstation2-linux.com/): 米国およびヨーロッパ諸国におけるPS2 Linuxコミュニティのポータル。
  - [Linux (for PlayStation 2) Release 1.0 Official Home Page](http://www.ps2linux.com/)
  - [Progressive Club（Internet Archive）](http://web.archive.org/web/20090225192044/http://tokyo.cool.ne.jp/xiaolang/pclub/): PS2 Linuxに使用するVGAケーブルを他のゲームソフトに生かす情報のサイト。

[Category:Linuxディストリビューション](https://ja.wikipedia.org/wiki/Category:Linuxディストリビューション "wikilink") [Category:PlayStation_2用ソフト](https://ja.wikipedia.org/wiki/Category:PlayStation_2用ソフト "wikilink") [Category:日本のLinux開発](https://ja.wikipedia.org/wiki/Category:日本のLinux開発 "wikilink") [Category:2001年のソフトウェア](https://ja.wikipedia.org/wiki/Category:2001年のソフトウェア "wikilink")

1.  [茶の間で使えるLinux～ PS2 Linuxを使い倒そう ～ PS2 Linuxの環境設定(2)](http://news.mynavi.jp/special/2001/ps2linux/004.html)(2019/02/17現在)このページは存在しません
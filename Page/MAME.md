> この記事は[MAME](https://ja.wikipedia.org/wiki/MAME)から翻訳されています。


**MAME**（メイム）は、オープンソースの汎用エミュレーターである。かつてはアーケード[ゲームエミュレータ](../Page/ゲームエミュレータ.md "wikilink")であったが、現在は汎用エミュレーターとなっている。元々の正式名称は**Multiple Arcade Machine Emulator**。

## 概要

[1997年](https://ja.wikipedia.org/wiki/1997年 "wikilink")2月5日にイタリア人のニコラ・サルモリアによって最初のバージョン (0.1) がリリースされた。世界中の数十名からなる開発チームにより、現在も開発、改良が続けられている。サポートするタイトル数は、完全に動作しないものも含めて3,500本以上、クローン版（同一ゲームのバージョン違いや、海外向けにローカライズしたものなど）を含めると6,500本以上に上る。現在のプロジェクト管理者はアメリカのアーロン・ジャイルズ。

MAMEはオープンソースであり、GitHubを用いて共同で開発されている。かつては、独自にエミュレート対象の[ゲーム](../Page/ゲーム.md "wikilink")の挙動を修正したり、新しいゲームへと対応させた派生版が多く存在したが、現在は本家MAMEへのマージが進んでいる。非公式版として、多くのに対応する**HBMAME**や、CRTモニター向けの**GroovyMAME**、ピンボール向けの、VGM生成用の**MAME/MESS VGM mod**がある。MAMEフロントエンドとしては、公式のコマンドラインUIの他に、Windows用GUIの**MAMEUI**、独自インターフェースの**IV/Play**、MAMEのWebフロントエンドである**Emularity**\[1\]などが存在する。かつては、Mac用の**MAME OS X**、[GTK](https://ja.wikipedia.org/wiki/GTK "wikilink")採用の**GMAMEUI** (**GXMame**派生)、[KDE](../Page/KDE.md "wikilink")採用の**Kxmame** (GXMame派生)、[Qt](../Page/Qt.md "wikilink")採用の**MAME Plus\!**なども存在した。

MAMEがサポートするのは、主に1970年代から1990年代（一部[2010年](https://ja.wikipedia.org/wiki/2010年 "wikilink")のゲームまで対応）のアーケードゲームやカジノゲームである。Atari [PONGなど](../Page/ポン_\(ゲーム\).md "wikilink")[ROMを持たず](https://ja.wikipedia.org/wiki/Read_Only_Memory "wikilink")、ディスクリート回路のみで構成されているゲームも、を通してサポートしている。メカニカルのあるゲームは、サポートされないものが多い (UFOキャッチャー、プリクラ、メダルゲームなど)。セグメントディスプレイを使ったゲームなどでは、外部アートワークを必要とするものがある。3Dアートワークにはまだ対応していない\[2\]ため、[ワニワニパニック](https://ja.wikipedia.org/wiki/ワニワニパニック "wikilink")は2Dとなる。一部のゲームは音源エミュレーションに未対応であり、音を鳴らすために外部のMAME Samplesが必要となる。近年のPCベースのアーケードゲームには対応しておらず、ArcadePC LoaderやTeknoParrotなどの他のプログラムを使う必要がある。

0.162以降のMAMEは、コンシューマーゲーム機、電卓 、[LSI/LCDゲーム](../Page/電子ゲーム.md "wikilink") ([たまごっち](../Page/たまごっち.md "wikilink")、[ゲームロボット](https://ja.wikipedia.org/wiki/ゲームロボット "wikilink")九、[ゲーム&ウオッチ](../Page/ゲーム&ウオッチ.md "wikilink")など)、電子ボードゲーム (など)、[携帯型ゲーム](../Page/携帯型ゲーム.md "wikilink")機 ([Microvision](https://ja.wikipedia.org/wiki/Microvision "wikilink")、[アドベンチャービジョン](https://ja.wikipedia.org/wiki/アドベンチャービジョン "wikilink")、[ゲームポケコン](../Page/ゲームポケコン.md "wikilink")、[ゲームボーイ](../Page/ゲームボーイ.md "wikilink")、[Atari Lynx](../Page/Atari_Lynx.md "wikilink")、[ネオジオポケット](../Page/ネオジオポケット.md "wikilink")、[ワンダースワン](../Page/ワンダースワン.md "wikilink")、[ゲームボーイアドバンス](../Page/ゲームボーイアドバンス.md "wikilink") など)、[体感ゲーム](../Page/体感ゲーム.md "wikilink") (Plug It\! ポピラ、エポック [体感ゲームシリーズなど](https://ja.wikipedia.org/wiki/体感ゲーム_\(エポック社\) "wikilink"))、ラジコン (システムコントロールカー チータなど)、ワークステーション ([Apollo/Domain](https://ja.wikipedia.org/wiki/Apollo/Domain "wikilink") 等)やその周辺機器(プリンターや音声合成装置やミュージカルキーボード など)、グラフィックワークステーション (等 )、モバイルワークステーション ([Sony NEWS](https://ja.wikipedia.org/wiki/NEWS_\(ソニー\) "wikilink") NWS-3260等)、プログラマブル計算機 (等)、デスクトップパソコン (、[IBM PC](../Page/IBM_PC.md "wikilink")/[PC XT](https://ja.wikipedia.org/wiki/IBM_PC_XT "wikilink")/[PCjr等](https://ja.wikipedia.org/wiki/IBM_PCjr "wikilink") )、ポータブルコンピュータ ([IBM 5155](https://ja.wikipedia.org/wiki/IBMポータブルPC "wikilink")、等 )、[ホビーパソコン](../Page/ホビーパソコン.md "wikilink")/ホームコンピュータ ([Apple II](../Page/Apple_II.md "wikilink")、[TRS-80](../Page/TRS-80.md "wikilink")、Commodore [PET 2001](../Page/PET_2001.md "wikilink")、[MSX](https://ja.wikipedia.org/wiki/MSX "wikilink")、[BBC Micro](https://ja.wikipedia.org/wiki/BBC_Micro "wikilink")/など )、開発システム (、Intel Intellec MDS-II等)、[ワードプロセッサ](../Page/ワードプロセッサ.md "wikilink") (など )、開発ボード (FriendlyARM等)、[ワンボードマイコン](../Page/ワンボードマイコン.md "wikilink") (NEC TK-80等)、[シングルボードコンピュータ](https://ja.wikipedia.org/wiki/シングルボードコンピュータ "wikilink") (Intel iSBC 286/10等)、[パームトップPC](https://ja.wikipedia.org/wiki/パームトップPC "wikilink") ([Atari Portfolio等](../Page/Atari_Portfolio.md "wikilink") )、[ポケットコンピュータ](../Page/ポケットコンピュータ.md "wikilink") (//等)、PDA (Palm、 等)、知育玩具 (TIの、ベネッセの[ポケットチャレンジ](https://ja.wikipedia.org/wiki/ポケットチャレンジ "wikilink")V2 等)、競馬予想機 (Thoroughbred Horse Race Analyzerなど)、決済端末機 (VeriFone 等)、音源モジュール ([YAMAHA FB-01等](../Page/ヤマハ・TXシリーズ.md "wikilink") )、LDプレーヤー (Pioneer LDV-1000、Pioneer PR-8210など)、[フィットネスマシン](https://ja.wikipedia.org/wiki/フィットネスマシン "wikilink") (Salter Fitness Bike、Salter Fitness Stepper)、[ドラムマシン](../Page/ドラムマシン.md "wikilink") ([Casio RZ-1など](https://ja.wikipedia.org/wiki/Casio_RZ-1 "wikilink")) などアーケード機に限定しないエミュレートを実装している。なお、古いPCへの対応は、SPC/ATやPCem、Common Source Code Projectなどのエミュレータの方が進んでいる。

MAMEの開発方針はオリジナルのハードウェア動作を忠実に再現することに重点を置いており、MAMEは基本的にAPUやMPUなどのチップレベルの低レベルエミュレーション (LLE) を行っている。ただし例外として、キーボード周りやI/O周りやDSP などには高レベルエミュレーション (HLE)も使われている。

MAMEで使用するROMイメージを入手するためは、他の低レベルエミュレータと同様に、基板から実物のROMの内容を吸い出す必要がある。ただし例外として、[Exidy社](https://ja.wikipedia.org/wiki/w:Exidy "wikilink")、[バリー/ミッドウェイ社などの作品のうち](../Page/ミッドウェイゲームズ.md "wikilink")、一部のゲームのROMイメージは、メーカーからの正式な許可を得たうえで、MAMEの公式サイトで配布されている[1](http://mamedev.org/roms/)。また、[ドイツ](https://ja.wikipedia.org/wiki/ドイツ "wikilink")のコンピュータ雑誌「[c't](https://ja.wikipedia.org/wiki/c't "wikilink")」で、「[UDPを使いMAMEを自動制御し](../Page/User_Datagram_Protocol.md "wikilink")、[アタリ社のゲーム](../Page/アタリ_\(企業\).md "wikilink")『[アステロイド](https://ja.wikipedia.org/wiki/アステロイド "wikilink")』のハイスコアを競う」内容のコンテストが行われる際に、この雑誌の読者向けに、アタリ社より『アステロイド』のROMイメージを配布する許可を得ている（不特定多数が対象ではない）[2](http://www.heise.de/ct/creativ/08/02/details/)。

## 歴史

1997年にリリースされた当初は[MS-DOS](../Page/MS-DOS.md "wikilink")版として開発されていたが、年内には[Macintosh](../Page/Macintosh.md "wikilink") (**MacMAME**)、[Unix系](../Page/Unix系.md "wikilink")OS (**X/MAME**)、Windows (**MAME32**)に移植された\[3\]。また、1998年には、MAME 0.33のベータ版を基にして、汎用エミュレーターである**MESS**（Multi Emulator Super System）の開発が始まった。2001年、MAME 0.37b14で、DOS版に代わりWindows 32bit版が公式となった。2005年、MAME 0.99u2で、ギャンブルゲームを実装する**AGEMAME** (旧**MAGE**)がMAMEに統合されはじめた\[4\]。2007年、MAME 0.120でWindows 64bit版が公式に用意された。2010年、MAME 0.136u1で、[SDL](../Page/SDL.md "wikilink")採用のクロスプラットフォームなコマンドライン版である**SDLMAME**がMAMEに統合された。2011年、MAME 0.141u1で、ピンボールを実装する**PINMAME**がMAMEに統合されはじめた\[5\]。2012年、MAME 0.147でMESSのコードベースが統合され、MESSとMAMEの統合版として**UME**（Universal Machine Emulator）がビルドできるようになった。2015年のMAME 0.162で、MAMEはMESSを吸収してUME相当となった。同年、MAME 0.171で、独自インターフェースの**MEWUI**や、MAMEをWeb上で動かす**JSMESS**\[6\]が、MAMEのコードベースに統合された。また、派生版のみに実装されていたAuto-fireに対応した\[7\]ほか、GPUバックエンドのBGFXが追加された。2016年、MAME 0.172でライセンスがGPLに変更された。また、ハイスコアが再実装されたほか、CRTモニタ向けの**GroovyMAME**の機能の一部が統合された\[8\]。同年、MAME 0.177で、VGM形式の音源を再生するための、VGM Playerが搭載された。

## 動作

MAMEの動作には、実際の基板上のデータイメージ（ROMイメージ）を用意する必要がある。MAMEは基板のハードウェア構成をソフトウェアでエミュレートすることにより、オリジナルのROMイメージを異なるハードウェア上で動作させることを可能にしている。エミュレートする[CPU](../Page/CPU.md "wikilink")は代表的な[Z80](../Page/Z80.md "wikilink")や[68000](https://ja.wikipedia.org/wiki/68000 "wikilink")をはじめとして100種類以上、サウンドチップは70種類以上、そのほか多くの[カスタムチップ](https://ja.wikipedia.org/wiki/カスタムチップ "wikilink")もサポートする。

最近のバージョンでは、3Dグラフィックシステムなど、処理量の多いゲームにも対応している。しかし、前述の通り、エミュレーションの動作速度よりもオリジナルハードウェアの忠実な再現を目的とするため、3Dグラフィックやテクスチャ処理なども、[Direct3D](../Page/Direct3D.md "wikilink")などのOS固有の拡張機能を使わず、オリジナルハードの動作を元に全てソフトウェアで処理を行う。このため最新の高速プロセッサでも完全な速度で動作しないタイトルが一部存在する（Windows版では描画の設定にDirect3Dの項目があるが、これは最終的な描画先としてDirect3Dを用いるだけであり、エミュレーション処理自体には関係しない）。

## 盗用問題

以前のMAMEは商用利用を禁止していたが、度々それに違反した利用が発覚している。

  - [メディアカイト](../Page/メディアカイト.md "wikilink")「ネットげーせん」
  - [ハムスター](../Page/ハムスター_\(ゲーム会社\).md "wikilink")「[オレたちゲーセン族](../Page/オレたちゲーセン族.md "wikilink")シリーズ」

## 脚注

## 関連項目

  - [:en:Visual Pinball](https://ja.wikipedia.org/wiki/:en:Visual_Pinball "wikilink")
  - [アーケードゲーム基板](../Page/アーケードゲーム基板.md "wikilink")
  - [エミュレータ](../Page/エミュレータ.md "wikilink")
  - [ゲームエミュレータ](../Page/ゲームエミュレータ.md "wikilink")
  - [エミュレーター基板](https://ja.wikipedia.org/wiki/エミュレーター基板 "wikilink")

## 外部リンク

  - [MAME公式サイト＆開発情報（英語）](http://www.mame.net/)
  - [MAMEUI公式サイト（英語）](http://www.mameui.info/)
  - [MAME E2J](http://www.e2j.net/)

[Category:エミュレーションソフトウェア](https://ja.wikipedia.org/wiki/Category:エミュレーションソフトウェア "wikilink") [Category:アーケードゲーム](https://ja.wikipedia.org/wiki/Category:アーケードゲーム "wikilink") [Category:フリーウェア](https://ja.wikipedia.org/wiki/Category:フリーウェア "wikilink") [Category:1997年のソフトウェア](https://ja.wikipedia.org/wiki/Category:1997年のソフトウェア "wikilink")

1.  [Emscripten Javascript and HTML](http://web.archive.org/web/20180824031815/http://docs.mamedev.org/initialsetup/compilingmame.html#emscripten-javascript-and-html) MAMEdev Team
2.  [3D artwork system \#388](https://github.com/mamedev/mame/issues/388)
3.  [MAME Project History](http://mamedev.org/history.html) MAME
4.
5.
6.  [This repository is now defunct](https://github.com/jsmess/jsmess/commit/c89717a50ab30ca97e504c5221e2113e74596214) 2015年2月
7.  [MAMEUIFX v0.171](http://www.emucr.com/2016/02/mameuifx-v0171.html) EmuCR.Com 2016年2月25日
8.  [MAME 0.172](http://mamedev.org/?p=424) MAME project 2016年3月30日
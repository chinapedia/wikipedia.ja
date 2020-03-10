> この記事は[LAME](https://ja.wikipedia.org/wiki/LAME)から翻訳されています。


**LAME** （**レイム**）は、[MP3](../Page/MP3.md "wikilink")への変換に用いられる[フリー](../Page/フリーソフトウェア.md "wikilink")（[GNU LGPL](../Page/GNU_Lesser_General_Public_License.md "wikilink")）の[アプリケーションソフトウェア](../Page/アプリケーションソフトウェア.md "wikilink")。名称は「**L**AME **A**in't an **M**P3 **E**ncoder」\[1\]\[2\]の[再帰的頭字語](../Page/再帰的頭字語.md "wikilink")。1998年から開発が続けられている。

## 特徴

[LAME_v3.99.5.png](https://ja.wikipedia.org/wiki/File:LAME_v3.99.5.png "fig:LAME_v3.99.5.png") LAMEはMP3に変換するのに使われる[ソースコード](../Page/ソースコード.md "wikilink")の中でも特に優秀とされ、LAMEを採用しているエンコーダは他のエンコーダよりも品質のよいMP3ファイルを作ることができるため、広く支持されている。また、バージョン3.90から[ギャップレスを実現している](https://ja.wikipedia.org/wiki/ギャップレス再生 "wikilink")\[3\]が、これを実現しているのはLAMEと[iTunes](https://ja.wikipedia.org/wiki/iTunes "wikilink")のみである\[4\]。

オープンソースコミュニティによって開発されており、無料で利用できる。当初はMike Chengにより8hz-mp3に対するパッチという扱いで配布されていたが、[1998年](https://ja.wikipedia.org/wiki/1998年 "wikilink")[10月4日](https://ja.wikipedia.org/wiki/10月4日 "wikilink")にリリースされたバージョン2.0からはISOのサンプルコードを改良するという形に開発体制が移行し、LAMEはパッチではなく現在のように完全な[ソースコード](../Page/ソースコード.md "wikilink")の形式で配布されるようになった。開発が進み、最終的には[2000年](../Page/2000年.md "wikilink")[5月8日](../Page/5月8日.md "wikilink")にリリースされた3.81 Betaにおいて、ISO由来のコードが完全に取り除かれるに至った。

オープンソースであることから様々なOSで動作することも特徴である。[UNIX](../Page/UNIX.md "wikilink")や[Unix系](../Page/Unix系.md "wikilink")OS上\[5\]だけではなく、[Windowsや](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")[Amiga](../Page/Amiga.md "wikilink")、[OS/2](https://ja.wikipedia.org/wiki/OS/2 "wikilink")、[BeOS](../Page/BeOS.md "wikilink")、さらには疑似コンソールを使用した[Classic Mac OS用のアプリケーションも存在する](../Page/Classic_Mac_OS.md "wikilink")。

推奨ビットレートは192kbps以上だが、かつてはこれでも[Vorbis](../Page/Vorbis.md "wikilink")の128kbpsには及ばないなどと言われていた。しかし、新しい心理音響モデルのnspsytuneの導入（バージョン3.88beta） や、[可変ビットレート](../Page/可変ビットレート.md "wikilink") (VBR) モードの改良等が行われ、現在に至るまで品質を向上させる努力が行われている。これらの成果は、Hydrogenaudioにおいて行われた複数のリスニングテストで示されている\[6\]。

LAMEから派生したエンコーダとして[午後のこ〜だ](../Page/午後のこ〜だ.md "wikilink")があるが、これはLAMEをベースとして[MMX](../Page/MMX.md "wikilink")、[SSE](../Page/ストリーミングSIMD拡張命令.md "wikilink")、[3DNow\!](../Page/3DNow!.md "wikilink")といった[x86](https://ja.wikipedia.org/wiki/x86 "wikilink")プロセッサ向けの[SIMD](../Page/SIMD.md "wikilink")命令を積極的に用いて最適化を行ったものである。エンコード速度が非常に高速である反面、ベースとなっているLAMEのバージョン (3.88) が古いため、近年の音質向上の試みが反映されていないという欠点がある。この**午後のこ〜だ**の成果の一部は、かつて評価版として配布されていたLAMEバージョン4.0に取り入れられ、さらにLAME 3.98 beta 1に本格的に導入され\[7\]、現在に至っている。

また、Mike Chengによる[MPEG Audio Layer 2のエンコーダの](https://ja.wikipedia.org/wiki/MP3#MPEG-1/2_Audio_Layer-2 "wikilink")[TooLAME](https://ja.wikipedia.org/wiki/:en:TooLAME "wikilink")（現:TwoLAME）も1998年11月7日にリリースされた\[8\]。

バージョン3.97をマルチスレッド化して高速化しようという試み\[9\]もあったが、ビットリザーバが無効になる\[10\]など音質面での欠点があり、ベンチマーク以外の用途では普及するには至っていない。

## 脚注

<references/>

## 外部リンク

### 本体

  - [LAME](https://lame.sourceforge.io/) - 公式サイト
  - [RareWares](https://www.rarewares.org/mp3.php) - バイナリの配布

### 関連サイト

  - [LAME FAQ（日本語）](http://www.initialt.org/lame/LAME-FAQ.txt)
  - [MP3はLAMEでエンコして、コマンドラインオプションを語れ！](http://onepermille.g2.xrea.com/lame/)
  - [mp3というフォーマットと特許・著作権](http://www.initialt.org/lame/patent.html)

### 関連ソフトウェア

  - [RazorLame](http://www.dors.de/razorlame/index.php) - LAMEのフロントエンド（）

  - [Lame Ivy Frontend Encoder](http://kkkkk.net/) - LAMEのフロントエンド

  - [CDex](https://cdex.mu/)（[日本語化](http://hissori.la.coocan.jp/)）

  - [Exact Audio Copy](http://www.exactaudiocopy.de/)（[日本語化](http://homepage3.nifty.com/eacj/)）

  - \- PowerPC G4以降に搭載されたベクトル演算ユニット[AltiVec](../Page/AltiVec.md "wikilink")（G5ではVMX）を使用し、高速化を図ったバージョン

  - [iTunes-LAME](http://blacktree.com/apps/iTunes-LAME/) - Macintosh上でiTunesと連携して動作するフロントエンド

  - [Sound Normalizer](http://www.kanssoftware.com/)

[Category:オープンソースソフトウェア](https://ja.wikipedia.org/wiki/Category:オープンソースソフトウェア "wikilink") [Category:コーデック](https://ja.wikipedia.org/wiki/Category:コーデック "wikilink") [Category:1998年のソフトウェア](https://ja.wikipedia.org/wiki/Category:1998年のソフトウェア "wikilink") [Category:MP3](https://ja.wikipedia.org/wiki/Category:MP3 "wikilink")

1.  「LAMEはMP3エンコーダではない」の意味。当初は他のエンコーダーのパッチの形だったため。
2.  なお、本来の英単語の「lame」は、「足の不自由な」「時代遅れの」という意味である。
3.  デコーダ側の対応を必要とするので、すべての環境でギャップレスを保証するものではない。
4.  LAMEとiTunesのギャップレス対応の実装は異なるが、iTunesはLAMEを用いてエンコードされたMP3ファイルのギャップレス再生情報にも対応している
5.  [GNU/Linux](https://ja.wikipedia.org/wiki/GNU/Linuxシステム "wikilink")、[\*BSD](../Page/BSDの子孫.md "wikilink")、[macOS](https://ja.wikipedia.org/wiki/macOS "wikilink")、[Solaris](../Page/Solaris.md "wikilink")、[IRIX](../Page/IRIX.md "wikilink")、[Plan 9等](../Page/Plan_9_from_Bell_Labs.md "wikilink")。
6.  [Hydrogenaudio](http://www.hydrogenaudio.org/forums/index.php)『[Hydrogenaudio Listening Tests](http://wiki.hydrogenaudio.org/index.php?title=Hydrogenaudio_Listening_Tests)』
7.
8.  [TooLAME HISTORY](http://web.archive.org/web/20020409021845/http://members.dingoblue.net.au/~mikecheng/layer2/HISTORY)
9.  [Multi-threading LAME MP3 Encoder](http://softlab-pro-web.technion.ac.il/projects/LAME/html/lame.html)
10.
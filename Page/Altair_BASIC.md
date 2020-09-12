> この記事は[Altair BASIC](https://ja.wikipedia.org/wiki/Altair_BASIC)から翻訳されています。


**Altair BASIC**（アルテア・ベーシック）は、[MITS社の](../Page/Micro_Instrumentation_and_Telemetry_Systems.md "wikilink")[Altair 8800やそれ以降の](../Page/Altair_8800.md "wikilink")[S-100バス](../Page/S-100バス.md "wikilink")コンピュータ上で動作する、[プログラミング言語](../Page/プログラミング言語.md "wikilink")[BASIC](../Page/BASIC.md "wikilink")の[インタプリタ](../Page/インタプリタ.md "wikilink")である。これは、[マイクロソフト](../Page/マイクロソフト.md "wikilink")（当時はMicro-Soft表記）の最初の製品であり、MITSとの契約に基づいて配布された。Altair BASICは、[Microsoft BASIC製品群の起源となるものである](../Page/Microsoft_BASIC.md "wikilink")。

## 起源と開発

[ビル・ゲイツ](../Page/ビル・ゲイツ.md "wikilink")は、彼と[ポール・アレン](../Page/ポール・アレン.md "wikilink")が『[ポピュラーエレクトロニクス](https://ja.wikipedia.org/wiki/ポピュラーエレクトロニクス "wikilink")』1975年1月号に掲載されたAltair 8800の記事を読んだとき、コンピュータの価格が間もなく下がり、[ソフトウェア](../Page/ソフトウェア.md "wikilink")の販売が[収益性の高いビジネスになるだろうと理解したと後に回想している](../Page/利益.md "wikilink")\[1\]。ゲイツは、Altair 8800にBASICインタプリタを提供することで、この製品が趣味家にとってより魅力的なものになると考えていた。彼らはMITSの創設者[エド・ロバーツ](../Page/エド・ロバーツ.md "wikilink")に連絡を取り、（まだ作業に取り掛かってすらいないにも関わらず）彼らがBASICインタプリタを開発していると伝え、デモを見たいかどうか尋ねた。これは、[存在しない製品を発表して相手の興味を測る](https://ja.wikipedia.org/wiki/ベーパーウェア "wikilink")[観測気球であった](https://ja.wikipedia.org/wiki/アドバルーン発言 "wikilink")。ロバーツは、数週間後の1975年3月にデモのために彼らと会うことに同意した。

ゲイツとアレンは、インタプリタを開発してテストするためのAltairコンピュータを持っていなかった。しかし、アレンは以前の名称で仕事をしていたときに[Intel 8008エミュレータを作成し](../Page/Intel_8008.md "wikilink")、[PDP-10](../Page/PDP-10.md "wikilink")上で動作させていた。アレンはAltairのプログラマガイドに基づいてこのエミュレータを改良し、[ハーバード大学](https://ja.wikipedia.org/wiki/ハーバード大学 "wikilink")のPDP-10上でインタプリタの開発とテストを行った。大学の資産で商用のソフトウェアが開発されていることを知った大学当局は不満を抱いたが、このような使い方を禁止する規定は大学にはなかった\[2\]。結局、大学当局から商業行為は学外で行うよう勧告され、ゲイツとアレンはボストンの[タイムシェアリングサービスからコンピュータの使用時間を購入してBASICプログラムのデバッグを行った](../Page/タイムシェアリングシステム.md "wikilink")。当初のバージョンは整数演算のみだったが、ハーバード大学の同級生の[モンティ・ダビドフ](../Page/モンティ・ダビドフ.md "wikilink")が[浮動小数点](https://ja.wikipedia.org/wiki/浮動小数点 "wikilink")演算も使うべきだとし、自分ならメモリ制限内に収まるようなシステムを書けると主張したので、ゲイツとアレンはダビドフを雇ってそのルーチンを作ってもらった。

独自の[入出力](../Page/入出力.md "wikilink")システムと[ラインエディタ](https://ja.wikipedia.org/wiki/ラインエディタ "wikilink")を持った完成したインタプリタは、わずか4[キロバイト](../Page/キロバイト.md "wikilink") のメモリに収まり、さらに、解釈後のプログラムを格納するための十分なメモリ空間が確保されていた。デモの準備として、完成したインタプリタをAltairに読み込ませるために[紙テープ](../Page/紙テープ.md "wikilink")に保存し、アレンはMITS社のある[アルバカーキ](../Page/アルバカーキ.md "wikilink")へ飛んだ。

アルバカーキ空港への最終アプローチ中、アレンは紙テープをメモリに読み出すための[ブートストラップ](../Page/ブートストラップ.md "wikilink")プログラムを書き忘れていることに気付いた。アレンはそれを8080の[機械語](../Page/機械語.md "wikilink")で書き、飛行機が着陸する前にプログラムを完成させた。プログラムをAltairにロードし、システムのメモリサイズを尋ねるプロンプトが表示されたのを見て初めて、彼らは自分たちのインタプリタがAltairハードウェア上で正しく動作することを知った。その後、誰が最短のブートストラッププログラムを書けるかを賭けて、ゲイツが勝利した\[3\]\[4\]。

## バージョンと配布

[Altair_BASIC_Paper_Tape.jpg](https://ja.wikipedia.org/wiki/File:Altair_BASIC_Paper_Tape.jpg "fig:Altair_BASIC_Paper_Tape.jpg") ロバーツはインタプリタの配布に同意した。また、ゲイツとアレンをMITS社で雇ってメンテナンスと改良を行った。8K BASIC、Extended BASIC、Extended ROM BASIC、Disk BASICなどのアップグレード版が追加されると、オリジナルのバージョンは4K BASICと呼ばれるようになった。

最小のバージョンである4K BASICは4キロバイトのRAMを持つマシンで動作し、プログラムコードエリアには約790バイトの空きしかなかった。このような小さなメモリ空間に収めるために、4Kバージョンには文字列操作やいくつかの一般的な数学関数が入っていなかった。8K BASICバージョンでは、文字列変数とその操作関数、乱数のための`RND`などの数学関数、ブール演算子、[`PEEK`と`POKE`などが追加された](../Page/PEEKとPOKE.md "wikilink")。8Kバージョンは、[ホビーパソコン](../Page/ホビーパソコン.md "wikilink")時代のBASICのほとんどのバージョンの基礎となっている。Extended BASICでは`PRINT USING`や基本的なディスクコマンドが追加され、Disk BASICではさらにディスクコマンドが拡張され、raw I/O機能が可能になった\[5\]\[6\]。

1975年10月、4K BASICは150ドル、8K BASICは200ドル、Extended BASICは350ドルで販売された。8KのAltairメモリとAltair IOボードを購入すると、それぞれ60ドル、75ドル、150ドルに値引きされた。配布形式は[紙テープ](../Page/紙テープ.md "wikilink")または[カセットテープ](../Page/カセットテープ.md "wikilink")だった\[7\]。

彼らの予想通り、Altairは[ホームブリュー・コンピュータ・クラブ](https://ja.wikipedia.org/wiki/ホームブリュー・コンピュータ・クラブ "wikilink")などのホビイストの間で非常に人気となった。また、MITSが選択したBASICインタプリタであるAltair BASICも人気となった。しかし、ホビイリストたちは、誰かが入手したAltair BASICを仲間でコピーして使っており、それが悪いことであるとは思っていなかった。ホームブリュー・コンピュータ・クラブのダン・ソコルは、何らかの手段で入手した販売前のテープから25個のコピーを作り、それをクラブの会合で配布して、受け取った人に更にコピーを作るように促していた。ゲイツは、1976年にホームブリュー・コンピュータ・クラブの会報に『[ホビイストたちへの公開状](https://ja.wikipedia.org/wiki/ホビイストたちへの公開状 "wikilink")』という文章を寄稿し、この中で、ソフトウェアをコピーする行為は[窃盗](../Page/窃盗.md "wikilink")だとして非難し、人々がお金を払わないソフトウェアの開発の継続はできないと宣言した。多くのホビイストはこの書簡に防御的な反応を示した。

ゲイツ、アレンによる[マイクロソフト](../Page/マイクロソフト.md "wikilink")とMITSとの間の契約条件では、一定額の[ロイヤルティー](../Page/ロイヤルティー.md "wikilink")を支払った後で、MITSはインタプリタの権利を受け取ることになっていた。しかし、マイクロソフトは[MC6800](../Page/MC6800.md "wikilink")など他のシステム向けにもインタプリタを開発していた。そのため、彼らがMITSからの離脱を決めた際に、ロイヤルティーの全額が支払われたかどうか、他のバージョンにも契約が適用されるかどうかを巡って争いになった。マイクロソフトとMITSは仲裁人に紛争の[仲裁](../Page/仲裁.md "wikilink")を依頼した。仲裁人は、MITSは「最善の努力」でソフトウェアを販売していなかったとして、マイクロソフトに有利な裁決を下した\[8\]。

BASICインタプリタは、1980年代初頭に[MS-DOS](../Page/MS-DOS.md "wikilink")に移行するまで、マイクロソフトのビジネスの中核を担っていた。

## 関連項目

  -
## 脚注

## 関連文献

  -
  -
  - [Cringely, Robert X.](https://ja.wikipedia.org/wiki/Robert_X._Cringely "wikilink"). *[Triumph of the Nerds](https://ja.wikipedia.org/wiki/Triumph_of_the_Nerds "wikilink")*. PBS, 1996.

  -
## 外部リンク

  - [Altair BASIC 3.2 (4K) - Annotated Disassembly](http://altairbasic.org/)
  - [Altair BASIC source disassembly](https://web.archive.org/web/20011211233332/http://www.rjh.org.uk/altair/4k/index2.html), compiled by Reuben Harris and archived at archive.org
  - [Writing an Altair Basic](https://americanhistory.si.edu/comphist/gates.htm#tc11), Interview with Bill Gates, Interviewer: David Allison (DA), Division of Computers, Information, & Society, National Museum of American History, Smithsonian Institution
  - [History of Microsoft Video: Bill Gates Talks about Altair Basic](https://blogs.msdn.com/b/vbteam/archive/2009/06/24/history-of-microsoft-video-bill-gates-talks-about-altair-basic-lisa-feigenbaum.aspx), (Lisa Feigenbaum) 24 Jun 2009, The Visual Basic Team, MSDN Blogs

[Category:1975年のソフトウェア](https://ja.wikipedia.org/wiki/Category:1975年のソフトウェア "wikilink") [Category:BASIC](https://ja.wikipedia.org/wiki/Category:BASIC "wikilink") [Category:マイクロソフトのプログラミング言語](https://ja.wikipedia.org/wiki/Category:マイクロソフトのプログラミング言語 "wikilink")

1.   "While walking through Harvard Square one day, Allen spotted the Popular Electronics cover that features the Altair. ... Allen ran to tell Bill that he thought their big break had finally come. Bill agreed."
2.
3.
4.
5.
6.
7.  [Altair Basic for the 6800](http://www.swtpc.com/mholley/Altair/Altair_Basic.htm), *In January 1978 I purchased Altair 680 Basic from Computer Kits in Berkeley CA. I paid full price, $200, I didn't want Bill Gates to go broke. If you bought an Altair 680B kit with 16 K of RAM for $685 you would get BASIC for free.*, Michael Holley's SWTPC Collection Home Page
8.
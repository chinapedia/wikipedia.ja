> この記事は[Free Pascal](https://ja.wikipedia.org/wiki/Free_Pascal)から翻訳されています。


[thumbnailのための準備をしている](https://ja.wikipedia.org/wiki/ファイル:20020730092044_-_FreePascal_IDE.jpg "wikilink")\]\] [Lazarus_1.2.6_+_Free_Pascal_2.6.4_on_Windows_8.png](https://ja.wikipedia.org/wiki/File:Lazarus_1.2.6_+_Free_Pascal_2.6.4_on_Windows_8.png "fig:Lazarus_1.2.6_+_Free_Pascal_2.6.4_on_Windows_8.png")

**Free Pascal** コンパイラ（通称FPC。以前はFPK Pascal）は[オープンソース](../Page/オープンソース.md "wikilink")の[Object Pascal](../Page/Object_Pascal.md "wikilink") [コンパイラ](../Page/コンパイラ.md "wikilink")である。

## 概説

**Free Pascal**は、複数のCPUアーキテクチャ（[32ビット](../Page/32ビット.md "wikilink")/[64ビット](https://ja.wikipedia.org/wiki/64ビット "wikilink")）、複数の[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink") (OS) をサポートするコンパイラであり、広く用いられる各種システム向けに移植されている。言語仕様はObject Pascalに加えて、[Turbo Pascal](../Page/Turbo_Pascal.md "wikilink")、[Delphi](../Page/Delphi.md "wikilink")、そして過去に存在した[Macintosh](../Page/Macintosh.md "wikilink")コンパイラの方言に対応している。

Free Pascalは以前、**FPK Pascal**の名で知られていた。これは "Free Pascal Kompiler" の略ではなく、実際は作者のイニシャルから名をとったものである (Florian Paul Klämpfl)。その後、プロジェクトの参加者が増えたため、誤解を避ける目的から1997年の終わりに、Free Pascal Compiler (FPC) と改名した。

FPCのドキュメントは詳細で、マニュアルは合計1800頁に及ぶ。

Free PascalにはTurbo Pascal風の[テキストモードの](https://ja.wikipedia.org/wiki/テキストユーザインタフェース "wikilink")[統合開発環境](../Page/統合開発環境.md "wikilink") (IDE) があるが、メインテナンス要員が足りないために、時として使い物にならなくなっていた。2005年の後半から改善の努力が続けられ、2006年に入ってからは、大きな[バグ](../Page/バグ.md "wikilink")は修正済みとなり、リリースしてもよい程度の品質になった。[macOS](https://ja.wikipedia.org/wiki/macOS "wikilink")用のFPCはコマンドラインからはもちろん、[Xcode](https://ja.wikipedia.org/wiki/Xcode "wikilink")の一部として動作させることもできる。

Turbo Pascal や Delphi 同様、FPCは Pascal コードの中に[アセンブリ言語](../Page/アセンブリ言語.md "wikilink")コードを記述できるような優れた仕組みをもっている。FPCの内蔵アセンブラは、複数のアーキテクチャと表記法をサポートしている。

ライブラリは、基本プログラムに必要な「Run-Time Library (RTL)」と、多種多様なクラスや（データベースなどの）非ビジュアルコンポーネントで構成された「Free Component Library (FCL)」がある。

Free Pascal コンパイラを採用したオープンソースのIDEである[Lazarus](https://ja.wikipedia.org/wiki/Lazarus "wikilink")には、Delphi の [Visual Component Library](https://ja.wikipedia.org/wiki/Visual_Component_Library "wikilink") (VCL) と高い互換性を持つLazarus Component Library (LCL) があり、Free PascalのRTLとFCLを組み合わせて[GUIアプリケーションを開発できる](https://ja.wikipedia.org/wiki/グラフィカルユーザインタフェース "wikilink")。

## 言語仕様

FPCはPascalの方言のうちで、[デファクトスタンダード](../Page/デファクトスタンダード.md "wikilink")となっているBorland PascalとDelphiを採用している。バージョン2.0以降、Delphi7互換性は継続的に実施または改善された。

また、[Mac OS](https://ja.wikipedia.org/wiki/Mac_OS "wikilink")（macOSを含む）との[インタフェースを容易にするため](../Page/インタフェース_\(情報技術\).md "wikilink")、若干ながら Apple Pascal 文法をサポートするための努力も行われてきた。

コンパイラには複数の「コンパイル互換モード」を持っており、Default（ANSI/ISO標準）モード、Delphi互換モード、Turbo Pascal互換モード、FPCモード、Object Pascalモード、Mac Pascalモードがある。

## 歴史

### はじまり

FPC は ボーランド が「Borland Pascal 8は出さない、次の版はWindows専用になる（それがDelphi）」と明らかにしたときに出現した。学生であった Florian Paul Klämpfl は自分でコンパイラを作成しようと着手したのである。コンパイラは最初から Turbo Pascal 方言を用い、同時期に[DJGPP](https://ja.wikipedia.org/wiki/DJGPP "wikilink")プロジェクトが作成したGO32V1[DOSエクステンダ](https://ja.wikipedia.org/wiki/DOSエクステンダ "wikilink")向けの32ビットコードを生成した。当初のコンパイラ自身は Turbo Pascal でコンパイルされた [16ビット](../Page/16ビット.md "wikilink")DOSアプリケーションであった。二年後に、コンパイラは自分自身をコンパイルできるようになり（[ブートストラップ](../Page/ブートストラップ問題.md "wikilink")）、32ビットアプリケーションになった。

### 拡大

最初の32ビットコンパイラがネットに投稿されると、協力者が現れるようになった。数年後にはMichael van Canneytの手で[Linux](../Page/Linux.md "wikilink")に移植された（[Kylix](../Page/Kylix.md "wikilink")より5年早い）。DOS版からは、[OS/2](https://ja.wikipedia.org/wiki/OS/2 "wikilink") + EMX（OS/2に[UNIX](../Page/UNIX.md "wikilink")類似の環境を提供するライブラリ）に移植された。DOS版の改良はその後も進み、GO32V2を用いるようになった。これらの成果は[リリース](https://ja.wikipedia.org/wiki/バージョン "wikilink")0.99.5としてまとめられ、それまでの版より広い範囲で用いられるようになった。これがTurbo Pascal互換性にとどまっていた最後の版で、後のものは Delphi[互換モード](https://ja.wikipedia.org/wiki/互換モード "wikilink")を追加していくことになる。リリース0.99.5はモトローラ[680x0](https://ja.wikipedia.org/wiki/680x0 "wikilink") (68k) 用にも移植された。

リリース0.99.8で、Win32がターゲットとして加えられ、Delphiの仕様と協調する作業が始められた。1.0版の安定化が進められ、2000年6月に記念すべき公開にこぎ着けた。1.0.xシリーズ（後にもバグ取りと安定化が加えられ、1.0.10は2003年6月に公開された）は企業にも教育機関にも広く用いられた。1.0.xでは、68k向けの移植が再度行われ、多くの68k用UNIXや[Amiga](../Page/Amiga.md "wikilink")用の安定なコードを生成するようになった。

### 新時代

後に1.0.xとなる安定化作業及び68k向け移植の際に、コード生成部分にの設計上の限界がはっきりした。二つの基本的な問題があり、一つは、新しいプロセッサをサポートしようと思うと、コードジェネレータを根本的に書き直す必要があったこと、レジスタ割当の原則（ブロックをビルドする際、常にレジスタを3つ開けておく）が管理しにくく、自由度を欠いていたことである。

これらの理由から、1999年12月に1.0.xシリーズから枝分かれする形で1.1.xシリーズが作られた。最初はコンパイラの各部分のクリーンアップ及び再設計と書き直し、次いでコードジェネレータとレジスタアロケータの書き直しが行われた。余得として、不足していたDelphi互換性が向上した。

1.1.xの改良は遅かったが、着実であった。2003年遅くには[PowerPC](../Page/PowerPC.md "wikilink") (PPC) への移植が着手され、[ARM及び](https://ja.wikipedia.org/wiki/ARMアーキテクチャ "wikilink")[SPARC](../Page/SPARC.md "wikilink")への移植も2004年の夏から秋にかけて行われた。[AMD64への移植は](https://ja.wikipedia.org/wiki/x64 "wikilink")2004年早くに行われた。AMD64への移植によって、64ビットコンパイラとしての機能が加わった。

2003年11月に、1.1.xの最初の[ベータ版](../Page/ベータ版.md "wikilink")が公開され、版名を1.9.0とすることにした。その後すぐに1.9.2、1.9.4が公開された。1.9.4は[Mac OS Xをサポートした記念すべき最初の版であった](https://ja.wikipedia.org/wiki/macOS "wikilink")。

その後、1.9.6が2005年1月、1.9.8が2005年2月、2.0.0が2005年5月、2.0.2が2005年12月に公開された。

2012年1月に公開された 2.6.0 は、ネストした型、クラス変数、クラス/型ヘルパー、レコードの`for..in`などが実装され、Delphi互換性が向上した。さらにMac OS Xと[iOSを対象としたObjective](https://ja.wikipedia.org/wiki/iOS_\(アップル\) "wikilink") Pascalの方言もサポートした。2013年2月に公開された 2.6.2 は、ARMアーキテクチャコンパイラの改良および[NetBSD](../Page/NetBSD.md "wikilink")と[OpenBSD](../Page/OpenBSD.md "wikilink")に関する多数の不具合修正が行われた。最新安定版の2.6.4（2014年3月公開）では[データベース](../Page/データベース.md "wikilink")接続パッケージfcl-dbに対して多くの改良と修正が行われた。

## バージョン 3.0の新機能

  - 言語

:\*名前空間ユニット（ドットを含むユニット名をサポート, Delphi互換）

:\*動的配列コンストラクタ（クラスのCreate関数のような生成関数をサポート, Delphi互換）

:\*Default関数（指定した型の初期値を返す関数, Delphi互換）

:\*型ヘルパー（文字列リテラルや数値リテラルのような基本型のヘルパー, Delphi互換）

:\*コードページ情報を含むANSI文字列（Delphi互換）

  - コード生成

:\*Class field reordering

:\*Removing the calculation of dead values

:\*Shortcuts to speed up floating point calculations

:\*Constant propagation

:\*Dead store elimination

:\*Node dfa for liveness analysis

  - ユニットとパッケージ

:\*TDBF - Visual FoxProファイルをサポート

:\*Bufdataset - ftAutoIncフィールドをサポート

:\*TDBF, bufdataset (and descendents such as TSQLQuery) allow escaped delimiters in string expression filter

:\*TODBCConnection(odbcconn) - 64ビットODBCをサポート

:\*TZipper - zip64フォーマットをサポート

:\*より多くのファイル関連RTLルーティンでマルチコードページとUnicodeをサポート

:\*SQL parser/generatorの改良

  - ツールなど

:\*新しいPas2jniユーティリティ

  - macOS / iOS

:\*新しいiosxlocaleユニット

  - 新しいコンパイラターゲット

:\*Java Virtual MachineとDalvik（Android）のJavaコード生成をサポート

:\*AIX（5.3以降）をサポート

:\*16ビットリアルモードMS-DOSをサポート

:\*Android（ARM、x86、MIPS）をサポート

:\*armhf EABIをサポート

:\*AROS（i386-ABIv0、i386-ABIv0-on-trunk）をサポート

## ターゲットとなるシステム

<table>
<thead>
<tr class="header">
<th><p>アーキテクチャ</p></th>
<th><p>OS / デバイス</p></th>
<th><p>バージョン</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>3.0.0</p></td>
<td><p>2.6.2</p></td>
<td><p>2.6.0</p></td>
</tr>
<tr class="even">
<td><p><a href="https://ja.wikipedia.org/wiki/i386" title="wikilink">i386</a></p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/DOSエクステンダ" title="wikilink">DOS Extender</a> (<a href="http://wiki.lazarus.freepascal.org/GO32_V2">GO32V2</a>)</p></td>
<td></td>
</tr>
<tr class="odd">
<td><p><a href="../Page/FreeBSD.md" title="wikilink">FreeBSD</a></p></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p><a href="../Page/OpenBSD.md" title="wikilink">OpenBSD</a></p></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p><a href="../Page/NetBSD.md" title="wikilink">NetBSD</a></p></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p><a href="../Page/Linux.md" title="wikilink">Linux</a></p></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p><a href="https://ja.wikipedia.org/wiki/macOS" title="wikilink">macOS</a></p></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p><a href="https://ja.wikipedia.org/wiki/OS/2" title="wikilink">OS/2</a></p></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p><a href="https://ja.wikipedia.org/wiki/Microsoft_Windows" title="wikilink">Windows</a></p></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p><a href="https://ja.wikipedia.org/wiki/Windows_CE" title="wikilink">Windows CE</a></p></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p><a href="../Page/Haiku_(オペレーティングシステム).md" title="wikilink">Haiku</a></p></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p><a href="https://ja.wikipedia.org/wiki/NetWare" title="wikilink">NetWare</a></p></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p><a href="../Page/Solaris.md" title="wikilink">Solaris</a></p></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p><a href="https://ja.wikipedia.org/wiki/iPhone" title="wikilink">iPhone</a>Sim</p></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p><a href="../Page/QNX.md" title="wikilink">QNX</a></p></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p><a href="https://ja.wikipedia.org/wiki/x86-64" title="wikilink">x86-64</a></p></td>
<td><p><a href="../Page/FreeBSD.md" title="wikilink">FreeBSD</a></p></td>
<td></td>
</tr>
<tr class="even">
<td><p><a href="../Page/OpenBSD.md" title="wikilink">OpenBSD</a></p></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p><a href="../Page/NetBSD.md" title="wikilink">NetBSD</a></p></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p><a href="../Page/Linux.md" title="wikilink">Linux</a></p></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p><a href="https://ja.wikipedia.org/wiki/macOS" title="wikilink">macOS</a></p></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p><a href="https://ja.wikipedia.org/wiki/Microsoft_Windows" title="wikilink">Windows</a></p></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p><a href="../Page/Solaris.md" title="wikilink">Solaris</a></p></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p><a href="https://ja.wikipedia.org/wiki/ARMアーキテクチャ" title="wikilink">ARM</a></p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/iOS_(アップル)" title="wikilink">iOS</a></p></td>
<td></td>
</tr>
<tr class="odd">
<td><p><a href="https://ja.wikipedia.org/wiki/Game_Boy_Advance" title="wikilink">Game Boy Advance</a></p></td>
<td><p>(GBA)</p></td>
<td></td>
</tr>
<tr class="even">
<td><p><a href="https://ja.wikipedia.org/wiki/Nintendo_DS" title="wikilink">Nintendo DS</a></p></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p><a href="../Page/Linux.md" title="wikilink">Linux</a></p></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p><a href="https://ja.wikipedia.org/wiki/Windows_CE" title="wikilink">Windows CE</a></p></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p><a href="../Page/Dalvik仮想マシン.md" title="wikilink">Android</a></p></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p><a href="../Page/組み込みシステム.md" title="wikilink">組み込みシステム</a></p></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p><a href="../Page/PowerPC.md" title="wikilink">PowerPC</a></p></td>
<td><p><a href="../Page/Linux.md" title="wikilink">Linux</a></p></td>
<td></td>
</tr>
<tr class="even">
<td><p><a href="https://ja.wikipedia.org/wiki/macOS" title="wikilink">macOS</a></p></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p><a href="../Page/Classic_Mac_OS.md" title="wikilink">Mac OS Classic</a></p></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p><a href="https://ja.wikipedia.org/wiki/MorphOS" title="wikilink">MorphOS</a></p></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p><a href="https://ja.wikipedia.org/wiki/AIX" title="wikilink">AIX</a></p></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>PowerPC 64-bit</p></td>
<td><p><a href="../Page/Linux.md" title="wikilink">Linux</a></p></td>
<td></td>
</tr>
<tr class="odd">
<td><p><a href="https://ja.wikipedia.org/wiki/macOS" title="wikilink">macOS</a></p></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p><a href="https://ja.wikipedia.org/wiki/AIX" title="wikilink">AIX</a></p></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p><a href="../Page/SPARC.md" title="wikilink">SPARC</a></p></td>
<td><p><a href="../Page/Solaris.md" title="wikilink">Solaris</a></p></td>
<td></td>
</tr>
<tr class="even">
<td><p><a href="../Page/Linux.md" title="wikilink">Linux</a></p></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p><a href="https://ja.wikipedia.org/wiki/JVM" title="wikilink">JVM</a></p></td>
<td><p><a href="../Page/Javaプラットフォーム.md" title="wikilink">Java</a></p></td>
<td></td>
</tr>
<tr class="even">
<td><p><a href="../Page/Dalvik仮想マシン.md" title="wikilink">Android</a></p></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p><a href="https://ja.wikipedia.org/wiki/MIPSアーキテクチャ" title="wikilink">MIPS</a> (BE and LE)</p></td>
<td><p><a href="../Page/Linux.md" title="wikilink">Linux</a></p></td>
<td></td>
</tr>
<tr class="even">
<td><p><a href="../Page/組み込みシステム.md" title="wikilink">組み込みシステム</a></p></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>| <a href="https://ja.wikipedia.org/wiki/8086" title="wikilink">8086</a> (16-bit)</p></td>
<td><p><a href="../Page/DOS_(OS).md" title="wikilink">DOS</a></p></td>
<td></td>
</tr>
<tr class="even">
<td><p><a href="https://ja.wikipedia.org/wiki/MC68000#M68000ファミリ" title="wikilink">M68000ファミリ</a></p></td>
<td><p><a href="../Page/Linux.md" title="wikilink">Linux</a></p></td>
<td></td>
</tr>
<tr class="odd">
<td><p><a href="../Page/NetBSD.md" title="wikilink">NetBSD</a></p></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p><a href="https://ja.wikipedia.org/wiki/AmigaOS" title="wikilink">AmigaOS</a></p></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td></td>
<td></td>
<td></td>
</tr>
</tbody>
</table>

<references group="注"/>

## 関連項目

  - [Lazarus](https://ja.wikipedia.org/wiki/Lazarus "wikilink") - RAD環境
  - [Turbo Pascal](../Page/Turbo_Pascal.md "wikilink")
  - [Delphi](../Page/Delphi.md "wikilink")

## 外部リンク

  - [Free Pascal](http://www.freepascal.org/)
  - [Lazarus](http://lazarus.freepascal.org/) - FPC用RAD
  - [FPC on Mac](http://www.freepascal.org/fpcmac.html) - Classic Mac OSへの移植状況（macOSへの移植はUNIXチームが行った）
  - [Introduction to Free Pascal 2.0](http://www.osnews.com/story.php?news_id=10607) - Daniël Mantione による新版の詳しい紹介。開発史も。
  - [CrossFPC](http://crossfpc.untergrund.net/) - さまざまな環境向けに、FPCをDelphi IDE風に統合する無料ツールキット。
  - [FPS](http://ims.mii.lt/fps/en/about/index.html) - FPC用Win32ベースのIDE。デバッガ（トレース、ブレークポイント、ウォッチウィンドウ）を含む。
  - [Pixel image editor](http://www.kanzelsberger.com/pixel/) - FPCで記述したPhotoshop風画像エディタ。
  - [FPC 4 GBA Initiative](http://fpc4gba.pascalgamedevelopment.com) - ゲームボーイアドバンス向けFPCプロジェクト。

[Category:Pascal](https://ja.wikipedia.org/wiki/Category:Pascal "wikilink") [Category:コンパイラ](https://ja.wikipedia.org/wiki/Category:コンパイラ "wikilink") [Category:ソフトウェア開発ツール](https://ja.wikipedia.org/wiki/Category:ソフトウェア開発ツール "wikilink") [Category:オープンソースソフトウェア](https://ja.wikipedia.org/wiki/Category:オープンソースソフトウェア "wikilink")
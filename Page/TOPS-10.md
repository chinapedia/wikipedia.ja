> この記事は[TOPS-10](https://ja.wikipedia.org/wiki/TOPS-10)から翻訳されています。


**TOPS-10**は1967年、[ディジタル・イクイップメント・コーポレーション](../Page/ディジタル・イクイップメント・コーポレーション.md "wikilink") (DEC) が[メインフレーム](../Page/メインフレーム.md "wikilink")[PDP-10](../Page/PDP-10.md "wikilink")向けにリリースした[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink")。TOPS-10を搭載したPDP-10システムは "DECsystem-10"と呼ばれた。"TOPS" は *Timesharing / Total OPerating System* の略。元々は[PDP-6](../Page/PDP-6.md "wikilink")およびPDP-10の初期のOSだった "Monitor" が発展したもので、TOPS-10と呼ばれるようになったのは1970年のことである。

## 概要

TOPS-10は[共有メモリ](../Page/共有メモリ.md "wikilink")をサポートしており、マルチプレイヤー型の[コンピュータゲーム](../Page/コンピュータゲーム.md "wikilink")の開発を可能とした。\[1\]というゲームはテキストベースの [Star Trek](../Page/スタートレック.md "wikilink") のようなゲームで、ユーザーは端末からコマンドを打ち込み、リアルタイムで互いに戦うことができた。

他の特筆すべきアプリケーションとして FORUM がある。このアプリケーションはいわゆる「CBシミュレータ」の先駆けであり、現在では[チャット](../Page/チャット.md "wikilink")と言われるユーザー同士の会話を可能とするものである。このアプリケーションはマルチユーザー通信の可能性を示したもので、[CompuServe](../Page/CompuServe.md "wikilink")のチャットが開発される要因のひとつとなった。

TOPS-10の[APIは非常に頑強であり](../Page/アプリケーションプログラミングインタフェース.md "wikilink")、UUO（Unimplemented User Operation; 未実装ユーザー命令）を利用した機構を使っている。UUOにより[システムコール](../Page/システムコール.md "wikilink")は[機械語](../Page/機械語.md "wikilink")の一種のように実装された。このAPIはモニターコールと呼ばれ、当時の他のオペレーティングシステムに比較して非常に進んでいた。DECsystem-10のシステムプログラミングは単純で強力であり、それはこの非常に柔軟なAPIによるところが大きい。

TOPS-10は多数のキューから構成される面白い[スケジューラを備えていた](../Page/スケジューリング.md "wikilink")。TOPS-10では[プロセス](../Page/プロセス.md "wikilink")の優先順位に応じてキューを選択している（[多段フィードバックキュー](../Page/多段フィードバックキュー.md "wikilink")の原始的なものと言える）。また、ユーザーファイルとデバイスの独立性も特徴の1つである。

## リリース履歴

PDP-6でのMonitorは1964年にリリースされた。PDP-10のKA10プロセッサをサポートしたのは1967年のリリース2.18からのことである。1970年のリリース5.01からTOPS-10に改称。リリース6.01（1974年5月）で初めて[仮想記憶](../Page/仮想記憶.md "wikilink")（[デマンドページング](../Page/ページング方式.md "wikilink")）を実装し、物理メモリ容量より大きなプログラムを実行できるようになった。リリース7.00から[対称型マルチプロセッシング](../Page/対称型マルチプロセッシング.md "wikilink")が可能となった（それまでは[マスタースレーブ](https://ja.wikipedia.org/wiki/マスタースレーブ "wikilink")方式）。最終リリースは1988年のリリース7.04である\[2\]。

## 今日のTOPS-10

1996年、DECはTOPS-10を愛好家が使用することを許諾するホビースト向けライセンスを発行した\[3\]。

今日TOPS-10を動作させる最も簡単な方法は、適当な[エミュレータ](../Page/エミュレータ.md "wikilink")\[4\]\[5\]とOSの[システムイメージ](../Page/システムイメージ.md "wikilink")\[6\]を利用する方法である。また、元もとの配布用磁気テープの内容がアーカイブされているので、そこから構築することも可能である\[7\] \[8\]。

[ポール・アレン](../Page/ポール・アレン.md "wikilink")は歴史的コンピュータシステムを保守し公開しているが、その中にTOPS-10が動作する DECsystem-1090 も含まれる\[9\]。

## 実装されたプログラミング言語

TOPS-10の[アセンブラ](../Page/アセンブリ言語.md "wikilink")がTOPS-10に同梱されていた。

以下の[プログラミング言語](../Page/プログラミング言語.md "wikilink")製品がTOPS-10上で動作した。

  - [ALGOL](../Page/ALGOL.md "wikilink") (ALGOL-10 v10B)\[10\] - 汎用コンパイラ
  - [APL](../Page/APL.md "wikilink") (APL-SF V2)\[11\] - 数学的モデリング用インタプリタ
  - [BASIC](../Page/BASIC.md "wikilink") (BASIC-10 v17F)\[12\] - 汎用インタプリタ
  - [BLISS](../Page/BLISS.md "wikilink") (BLISS-10, BLISS-36) - システムプログラミング用コンパイラ
  - [COBOL](../Page/COBOL.md "wikilink") (COBOL-68, COBOL-74) - 事務処理用コンパイラ
  - [FORTRAN](../Page/FORTRAN.md "wikilink") (FORTRAN-10 v11) - 科学技術計算用コンパイラ

以下のプログラミング言語もTOPS-10上で実装されているが、DEC純正ではなくユーザーグループ  の会員が寄贈したものである。

  - [FOCAL](https://ja.wikipedia.org/wiki/:en:FOCAL_\(programming_language\) "wikilink") (FOCAL-10)

  - [Forth](../Page/Forth.md "wikilink") - [スレッデッドコード](https://ja.wikipedia.org/wiki/スレッデッドコード "wikilink")方式の言語

  - [IMP72](https://ja.wikipedia.org/wiki/:en:IMP_programming_language "wikilink")

  - [LISP](https://ja.wikipedia.org/wiki/LISP "wikilink") - [AIプログラミング向けインタプリタ](../Page/人工知能.md "wikilink")

  - [Pascal](../Page/Pascal.md "wikilink") - コンピュータ教育向けコンパイラ

  - \- [CAI向け言語](../Page/コンピュータ支援教育.md "wikilink")

  - [SAM76](https://ja.wikipedia.org/wiki/:en:SAM76 "wikilink")

  - [Simula](../Page/Simula.md "wikilink") - モデリング用コンパイラ

  - [SNOBOL](../Page/SNOBOL.md "wikilink") - 文字列処理用インタプリタ

## 脚注

## 関連項目

  - [TOPS-20](../Page/TOPS-20.md "wikilink")
  - [コロッサル・ケーブ・アドベンチャー](https://ja.wikipedia.org/wiki/コロッサル・ケーブ・アドベンチャー "wikilink")

[Category:オペレーティングシステム](https://ja.wikipedia.org/wiki/Category:オペレーティングシステム "wikilink") [Category:ディジタル・イクイップメント・コーポレーション](https://ja.wikipedia.org/wiki/Category:ディジタル・イクイップメント・コーポレーション "wikilink") [Category:1967年のソフトウェア](https://ja.wikipedia.org/wiki/Category:1967年のソフトウェア "wikilink")

1.  [The Decwar Page](http://hsnewman.freeshell.org/decwar.htm)
2.
3.  [Home hobbyist license for Digital's 36b software](http://www.inwap.com/pdp10/96license.txt)
4.  [The Computer History Simulation Project](http://simh.trailing-edge.com/)
5.  [KLH10 PDP-10 Emulator](http://klh10.trailing-edge.com/)
6.  [TOPS-10 pre-built image](http://www.steubentech.com/~talon/pdp10/)
7.  [PDP-10 software archive](http://pdp-10.trailing-edge.com/)
8.  [Notes on DEC PDP-10 Emulation](http://www.asun.net/pdp10/)
9.  [Living Computer Museum](http://www.pdpplanet.com/)
10. [DECsystem10/20 ALGOL Programmer's Guide, April 1977](http://computer-refuge.org/bitsavers/pdf/dec/pdp10/TOPS10_softwareNotebooks/vol06/AA-0196C-TK_ALGOL_Programmers_Guide_Apr77.pdf)
11. [APL-SF Language Manual, August 1979](http://computer-refuge.org/bitsavers/pdf/dec/pdp10/TOPS10_softwareNotebooks/vol06/AA-H200A-TK_APLSF_Language_Manual_Aug79.pdf)
12. [DECsystem-10 BASIC Conversational Language Manual, March 1974](http://computer-refuge.org/bitsavers/pdf/dec/pdp10/TOPS10_softwareNotebooks/vol06/DEC-10-LBLMA-A-D_BASIC_Conversational_Language_Manual_Mar74.pdf)
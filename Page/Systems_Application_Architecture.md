> この記事は[Systems Application Architecture](https://ja.wikipedia.org/wiki/Systems_Application_Architecture)から翻訳されています。


**Systems Application Architecture**（**SAA**、えすえーえー）は、[IBM](../Page/IBM.md "wikilink") が[1987年](https://ja.wikipedia.org/wiki/1987年 "wikilink")に提唱した、[コンピュータ](../Page/コンピュータ.md "wikilink")用の[アプリケーションソフトウェア](../Page/アプリケーションソフトウェア.md "wikilink")に関する、[標準化](../Page/標準化.md "wikilink")のための[ガイドライン](https://ja.wikipedia.org/wiki/ガイドライン "wikilink")である。

## 概要

SAAは[アーキテクチャの](../Page/コンピュータ・アーキテクチャ.md "wikilink")1つであり、特定の製品では無い。SAAには主に以下3つの標準により構成され、それぞれ発表年度によりガイドが発行された。

  - Common Programming Interface (**CPI**)
  - [Common User Access](../Page/Common_User_Access.md "wikilink") (**CUA**)
  - Common Communication Support (**CCS**)

また、これらの上にオフィスシステムなどのSAA共通アプリケーションが含まれた。

SAAの対象となる[プラットフォーム](../Page/プラットフォーム_\(コンピューティング\).md "wikilink")（**SAA環境**）は以下の4つとされた。

  - [メインフレーム](../Page/メインフレーム.md "wikilink") （[MVS](../Page/Multiple_Virtual_Storage.md "wikilink")、[VM](https://ja.wikipedia.org/wiki/z/VM "wikilink")）
  - [ミッドレンジ](../Page/ミッドレンジコンピュータ.md "wikilink") （[OS/400](https://ja.wikipedia.org/wiki/OS/400 "wikilink")）
  - [パーソナルコンピュータ](../Page/パーソナルコンピュータ.md "wikilink") （[OS/2](https://ja.wikipedia.org/wiki/OS/2 "wikilink")）

IBMはアプリケーションベンダーにSAA準拠を広く呼びかけた。特にCUAは、[Microsoft Windows 2.0や](../Page/Microsoft_Windows_2.0.md "wikilink")[Microsoft Windows 3.0の](https://ja.wikipedia.org/wiki/Microsoft_Windows_3.0 "wikilink")[ユーザインタフェース](../Page/ユーザインタフェース.md "wikilink")のベースともなった。また[MS-DOS](../Page/MS-DOS.md "wikilink")の[DOSシェルもCUAに準拠している](../Page/MS-DOS_Shell.md "wikilink")。

## 歴史

IBMは[1960年](../Page/1960年.md "wikilink")代の[System/360](https://ja.wikipedia.org/wiki/System/360 "wikilink")アーキテクチャに続き、[1970年](../Page/1970年.md "wikilink")代の[System/370](https://ja.wikipedia.org/wiki/System/370 "wikilink")アーキテクチャと[Systems Network Architecture](../Page/Systems_Network_Architecture.md "wikilink")(SNA)の成功によって、個々の製品の優劣だけではなく、[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink")と[ネットワークのアーキテクチャ](../Page/コンピュータネットワーク.md "wikilink")（仕様）を握ることで、市場に対する絶大な影響力を確保した。

しかし[1980年](https://ja.wikipedia.org/wiki/1980年 "wikilink")代になると、コンピュータの利用範囲も広がり、オペレーティングシステムやネットワークなどのインフラの上に構築されるアプリケーションの重要性が増し、アプリケーションの標準化の必要性が高まった。

またIBMは各種市場に向けて多数のコンピュータシリーズやオペレーティングシステムを開発・投入した結果、大型（[メインフレーム](../Page/メインフレーム.md "wikilink")）では[MVSや](../Page/Multiple_Virtual_Storage.md "wikilink")[VSEや](https://ja.wikipedia.org/wiki/z/VSE "wikilink")[VMや](https://ja.wikipedia.org/wiki/z/VM "wikilink")[TPF](https://ja.wikipedia.org/wiki/z/TPF "wikilink")、中型（[ミッドレンジ](../Page/ミッドレンジコンピュータ.md "wikilink")）では[S/36や](https://ja.wikipedia.org/wiki/System/36 "wikilink")[S/38や](https://ja.wikipedia.org/wiki/System/38 "wikilink")[AS/400](https://ja.wikipedia.org/wiki/AS/400 "wikilink")あるいは[UNIX](../Page/UNIX.md "wikilink")である[AIX](../Page/AIX.md "wikilink")、小型（[パーソナルコンピュータ](../Page/パーソナルコンピュータ.md "wikilink")）では[PC DOSや](../Page/MS-DOS.md "wikilink")[OS/2](https://ja.wikipedia.org/wiki/OS/2 "wikilink")など、多数のプラットフォームが存在したが、相互の使用できる[プログラミング言語](../Page/プログラミング言語.md "wikilink")や、[ユーザインタフェース](../Page/ユーザインタフェース.md "wikilink")などの操作性や、ネットワークの接続性が微妙に異なっていたため、組み合わせて使用するユーザーには手間がかかった。このため[DECの](../Page/ディジタル・イクイップメント・コーポレーション.md "wikilink")[VAX](../Page/VAX.md "wikilink")は「シングルアーキテクチャ」を売り文句にしていた。

[1987年](https://ja.wikipedia.org/wiki/1987年 "wikilink")3月にIBMはSAAを発表した。当時は「IBMが遂にアプリケーション市場にも支配力を強めるか」と大きく報道された。実際には、IBMはIBMの主要かつ戦略的なプラットフォームを選んで**SAA環境**とし、標準化を段階的に各製品に対して実施していった。同時にアプリケーションベンダーにSAAへの準拠を提唱した。

SAA環境には、「IBM独自OS」色の強い、[MVS](../Page/Multiple_Virtual_Storage.md "wikilink")、[VM](https://ja.wikipedia.org/wiki/z/VM "wikilink")、[OS/400](https://ja.wikipedia.org/wiki/OS/400 "wikilink")、[OS/2](https://ja.wikipedia.org/wiki/OS/2 "wikilink")の4環境が選定された。メインフレーム用のIBM独自OSでも、[VSEや](https://ja.wikipedia.org/wiki/z/VSE "wikilink")[TPFは含まれなかった](https://ja.wikipedia.org/wiki/z/TPF "wikilink")。[AIX](../Page/AIX.md "wikilink")は[OSF陣営として別途標準化が進んでいたためか](../Page/Open_Software_Foundation.md "wikilink")、SAA環境では無いが、SAA環境と相互運用可能性を持つ環境とされた。

IBMと[マイクロソフト](../Page/マイクロソフト.md "wikilink")のオペレーティングシステム共同開発契約も背景に、[MS-DOS](../Page/MS-DOS.md "wikilink")、[IBM DOS](https://ja.wikipedia.org/wiki/IBM_DOS "wikilink")、[Microsoft Windows 2.0](../Page/Microsoft_Windows_2.0.md "wikilink")、[Microsoft Windows 3.0なども](https://ja.wikipedia.org/wiki/Microsoft_Windows_3.0 "wikilink")、部分的にSAA準拠が進められた。また当時は独立企業であった[ロータスデベロップメントもSAA](../Page/ロータス_\(ソフトウェア\).md "wikilink") CUA準拠のアプリケーション開発を進めた。ただしマイクロソフトはWindows 3.1より、[ショートカットキー](../Page/ショートカットキー.md "wikilink")の[デフォルトを](../Page/デフォルト_\(コンピュータ\).md "wikilink")[Macintosh](../Page/Macintosh.md "wikilink")風に変更するなど、徐々に独自のユーザーインターフェースに向かい、SAAから離れていく事になる。[1991年](../Page/1991年.md "wikilink")には[オブジェクト指向](../Page/オブジェクト指向.md "wikilink")のユーザーインターフェースに進化したCUA '91が発表され、[OS/2](https://ja.wikipedia.org/wiki/OS/2 "wikilink") 2.0の[ワークプレース・シェル](https://ja.wikipedia.org/wiki/ワークプレース・シェル "wikilink")で実現したが、これは[1995年](https://ja.wikipedia.org/wiki/1995年 "wikilink")の[Windows 95より早く](../Page/Microsoft_Windows_95.md "wikilink")、オブジェクト指向はより徹底していた。

しかし[1990年](https://ja.wikipedia.org/wiki/1990年 "wikilink")代後半には、SAAには含まれていなかった[Java](https://ja.wikipedia.org/wiki/Java "wikilink")、[Windows 95](../Page/Microsoft_Windows_95.md "wikilink")、[TCP/IP](https://ja.wikipedia.org/wiki/TCP/IP "wikilink")などの普及もあり、SAAは徐々にフェードアウトしていった。なお現在でもWindowsなどの[GUIのメニュー配列やショートカットキーの一部などにはCUAの影響が残っている](https://ja.wikipedia.org/wiki/グラフィカルユーザインタフェース "wikilink")。

## 詳細

### Common Programming Interface

主要な[言語として](../Page/プログラミング言語.md "wikilink")[COBOL](../Page/COBOL.md "wikilink")、[FORTRAN](../Page/FORTRAN.md "wikilink")、[C言語](../Page/C言語.md "wikilink")が選定された。また[プロシージャ](https://ja.wikipedia.org/wiki/プロシージャ "wikilink")言語として[REXX](../Page/REXX.md "wikilink")が選定された。

SAA環境のオペレーティングシステムや主要ミドルウェアでは、これらの言語のサポートが進められた。REXXは[VMの](https://ja.wikipedia.org/wiki/z/VM "wikilink")[CMSで生まれた言語だが](https://ja.wikipedia.org/wiki/:en:Conversational_Monitor_System "wikilink")、MVSの[TSOや](https://ja.wikipedia.org/wiki/Time_Sharing_Option "wikilink")[OS/2](https://ja.wikipedia.org/wiki/OS/2 "wikilink")、更にはPC DOSにも搭載された。

なお、日本の大手メインフレームユーザでは[PL/I](https://ja.wikipedia.org/wiki/PL/I "wikilink")使用比率が高かったため意外と受け取られたが、SAAはメインフレームからパーソナルコンピュータまでを横断した標準化であり、[プラットフォーム固有の規格や言語を禁止するものではない](../Page/プラットフォーム_\(コンピューティング\).md "wikilink")。

### Common User Access

  -
    *詳細は [Common User Access](../Page/Common_User_Access.md "wikilink") も参照*

キャラクタベースとグラフィカルベースの2種類が規定された。Common User Access (CUA) 登場以前より「F1キーはヘルプ」などは各アプリケーションでほぼ標準となっていたが、それ以外のコマンドの位置はまちまちであった。

例えば、グラフィカルベースでは以下が推奨された。これらは現在もWindowsなどの[グラフィカルユーザインタフェース](https://ja.wikipedia.org/wiki/グラフィカルユーザインタフェース "wikilink") (GUI) のベースとなっている。

  - コマンドバーは左から「ファイル、編集、・・・、ヘルプ」とする
  - 「ファイル」のプルダウンメニューの中に「印刷」「クローズ/終了」などがある
  - 「編集」のプルダウンメニューの中に「コピー」「貼り付け」などがある

なお、ショートカットキーは CUA'87 の当初は以下が推奨されたが、後にはアプリケーションの自由とされた。

  - \[Shift\]+\[Delete\] 切り取り・カット
  - \[Ctrl\]+\[Insert\] コピー
  - \[Shift\]+\[Insert\] 貼り付け・ペースト
  - \[F3\] 終了

当時は[マイクロソフト](../Page/マイクロソフト.md "wikilink")とIBMは[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink") (OS) 共同開発の提携中であったため、以下はIBM CUA準拠となった。

  - [MS-DOS](../Page/MS-DOS.md "wikilink")および[PC DOS](https://ja.wikipedia.org/wiki/PC_DOS "wikilink")4.0で採用された[DOSシェル](../Page/MS-DOS_Shell.md "wikilink")
  - [Windows 3.0のGUI](../Page/Microsoft_Windows_3.x.md "wikilink") --- CUA'87準拠（Windows 3.1より、MacOS風の操作性に変更する）
  - [OS/2](https://ja.wikipedia.org/wiki/OS/2 "wikilink") 1.1 のPM (Prezentation Manager) --- CUA'87準拠
  - OS/2 2.0 のWPS (WorkPlaceShell) --- CUA'91準拠（[オブジェクト指向](../Page/オブジェクト指向.md "wikilink")のGUIを追加）

マイクロソフトによるWindows 3.0開発キットには、「IBM SAA CUA'87」のマニュアルが付属しており、初期の各社のWindowsアプリケーションはCUA '87を参照して開発された。

### Common Communication Support

主要な[通信プロトコル](../Page/通信プロトコル.md "wikilink")として、[Systems Network Architecture](../Page/Systems_Network_Architecture.md "wikilink") (SNA) が選定された。当初はSNAのサポートレベルが各プラットフォームで差が大きく接続性に制約がある場合もあったが、徐々に改善された。

## 関連項目

  - [IBM](../Page/IBM.md "wikilink")
  - [Systems Network Architecture](../Page/Systems_Network_Architecture.md "wikilink")
  - [AD/Cycle](https://ja.wikipedia.org/wiki/AD/Cycle "wikilink")
  - [ユーザーインタフェース](../Page/ユーザインタフェース.md "wikilink")

## 関連書籍

  - IBM 21世紀への挑戦―SAA開発に賭ける男たち（著：マイケル キレン、訳：栗田 昭平）

## 外部リンク

  - [Introduction to Systems Application Architecture -IBM](http://domino.research.ibm.com/tchjr/journalindex.nsf/2733206779564b3d85256bd500483abf/78ae0722884a6ff285256bfa00685bf0?OpenDocument)（詳細はリンク先のPDFファイルを参照）
  - [Designing SAA applications and user interfaces - IBM](http://domino.watson.ibm.com/tchjr/journalindex.nsf/d9f0a910ab8b637485256bc80066a393/d178231763a4982d85256bfa00685bf6?OpenDocument)（詳細はリンク先のPDFファイルを参照）

[Category:IBMのソフトウェア](https://ja.wikipedia.org/wiki/Category:IBMのソフトウェア "wikilink") [Category:ソフトウェア開発ツール](https://ja.wikipedia.org/wiki/Category:ソフトウェア開発ツール "wikilink") [Category:ソフトウェア開発工程](https://ja.wikipedia.org/wiki/Category:ソフトウェア開発工程 "wikilink") [Category:長大な項目名](https://ja.wikipedia.org/wiki/Category:長大な項目名 "wikilink")
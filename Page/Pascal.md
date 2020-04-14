> この記事は[Pascal](https://ja.wikipedia.org/wiki/Pascal)から翻訳されています。


[-2](https://ja.wikipedia.org/wiki/Modula-2 "wikilink"){{\\}}[-3](https://ja.wikipedia.org/wiki/Modula-3 "wikilink")、[Oberon](../Page/Oberon.md "wikilink"){{\\}}[-2](https://ja.wikipedia.org/wiki/Oberon-2 "wikilink")、[Object Pascal](../Page/Object_Pascal.md "wikilink")、[Oxygene](https://ja.wikipedia.org/wiki/Oxygene "wikilink")、[Seed7](https://ja.wikipedia.org/wiki/Seed7 "wikilink") }}  **Pascal**（パスカル）は、1970年に発表された[プログラミング言語](../Page/プログラミング言語.md "wikilink")。[ニクラウス・ヴィルト](../Page/ニクラウス・ヴィルト.md "wikilink")により[構造化プログラミング](../Page/構造化プログラミング.md "wikilink")として設計・デザインされた。名称は、[ブレーズ・パスカル](../Page/ブレーズ・パスカル.md "wikilink")にちなむ。

[ALGOL](../Page/ALGOL.md "wikilink")、[ALGOL Wをベースとし](https://ja.wikipedia.org/wiki/:en:ALGOL_W "wikilink")、簡素だがよく整った言語仕様（構文と意味）を持つ。プログラミング教育を意識しており、「判読性」を重視している反面、「最適化」を犠牲にしていると批判もされた。 言語的には、自身の[コンパイラ](../Page/コンパイラ.md "wikilink")を自身で書けるといった、言語処理系の[ブートストラップ](../Page/ブートストラップ.md "wikilink")を備え、多くの[\#実用プログラム例](https://ja.wikipedia.org/wiki/#実用プログラム例 "wikilink")を持っている。

## 言語仕様

教育を主目的としつつ、コンパイラが記述できる程度に強力な言語を目指し、当初、ヴィルト自身がPascal[コンパイラ](../Page/コンパイラ.md "wikilink")をPascal自身で書いてみせ、その能力を示した（後のModula-2では、オペレーティングシステムをModula-2で書いてみせた）。

Pascalの単純さは、例えば構文が[LL(1)であることなどによく現れている](../Page/LL法.md "wikilink")。全ての名札、定数、型名、変数、[サブルーチン](../Page/サブルーチン.md "wikilink")は使用に先立って定義しておく必要がある。[ポインタを用いたリストのような型の定義や](../Page/ポインタ_\(プログラミング\).md "wikilink")、交互にサブルーチンが呼び合うためには、例外的な構文を使わねばならない。ポインタに限っては、参照される型の定義の前に、その型を参照するような定義ができた。また、サブルーチンの定義部分だけを先に記述する方法で解決した。

その結果、パーサはLL(1)パーサであり、バックエンドはいわゆるワンパスコンパイラであった。なお、他言語のコンパイラでは、2回以上走査を行うマルチパス形式のものが多かった。マルチパス形式では、最初の走査で識別子等の情報を中心に情報収集を行い、後続の走査でそれらの情報を参照しつつ実行ファイルを生成するため、コンパイル速度面では不利だが、最適化の点で有利となる。ワンパスコンパイラであることは、絶望的に遅い[フロッピーディスク](../Page/フロッピーディスク.md "wikilink")を作業ディスクとしてビルドするユーザさえ多かった、初期のパーソナルコンピュータでは大いに利点となった。 なお、Turbo Pascalの高速性は[アセンブラ](https://ja.wikipedia.org/wiki/アセンブラ "wikilink")で記述されていたことも一因であるが、 Pascalの簡潔な仕様を活かし、かつ、メモリを使える限り使ってファイルアクセスを最小限に留めることで、前述のようなパーソナルコンピュータでも高速にコンパイルできた。

ALGOL由来の制御構造、サブルーチンの中に、そのサブルーチン内からのみ見えるローカルな変数、そのサブルーチン内からのみ呼び出せるサブルーチン等を定義できるといった、スコープの概念と[再帰的](https://ja.wikipedia.org/wiki/再帰的 "wikilink")な構文構造（[ブロック構造と呼ぶ](../Page/ブロック_\(プログラミング\).md "wikilink")）、[静的スコープ](../Page/静的スコープ.md "wikilink")による参照の局所化機能を持つ。さらに、豊富な[データ型](../Page/データ型.md "wikilink")と、[COBOL](../Page/COBOL.md "wikilink") に見られた[構造体](../Page/構造体.md "wikilink")を含む新しいデータ型を定義できるという特徴も持っている。レコード型とポインタを用いて[リスト](https://ja.wikipedia.org/wiki/線形リスト "wikilink")、[木といったデータ構造を自由に構築することができる](../Page/木_\(数学\).md "wikilink")（[二分木\#データの二分木への格納法](https://ja.wikipedia.org/wiki/二分木#データの二分木への格納法 "wikilink")の例参照）。なお由来は不明だが、最後にピリオドを付けるという、微妙にALGOLの構文と違う点がある。

Pascalの注目すべきは、変数定義において型名、変数名の順序とした記法であろう。ALGOLを源流とする[C言語](../Page/C言語.md "wikilink")などでは、変数などの定義で「`int x`」といったような「型名 変数名」という順序で記述される。一方、Pascalでは「`var x : int`」というような、「変数名 型名」の順序で記述する。この記法は数学などと類似の記法であるため、ヴィルトの完全なオリジナルだとは言いにくいが、最初に述べたALGOL WではALGOLと同様であるので、プログラミング言語への導入としてはオリジナリティが高いものと考えられる。この点について、[Java](https://ja.wikipedia.org/wiki/Java "wikilink")などはC言語の構文の小改良にとどまっているが、[Limbo](https://ja.wikipedia.org/wiki/Limbo "wikilink")や[Go言語などC言語を使い尽した設計者らによる新言語が](https://ja.wikipedia.org/wiki/Go_\(プログラミング言語\) "wikilink")、Pascalに似た記法としていることは特筆事項であろう。なお、ALGOL系では[Ada](../Page/Ada.md "wikilink")も変数などの型の記述を、これに類似した構文としている。[Scala](../Page/Scala.md "wikilink")や[Kotlin](https://ja.wikipedia.org/wiki/Kotlin "wikilink")といった[Java VM環境で動作する後発言語も](https://ja.wikipedia.org/wiki/Java_VM "wikilink")、型を後置する記法を採用している。

コンパイル時にできるだけ多くの不注意による誤りを発見できる、強く型付けされた（strongly typed）言語であり、またハードウェアを隠蔽する思想が徹底している。たとえば[集合型](https://ja.wikipedia.org/wiki/集合_\(プログラミング\) "wikilink")、ポインタ型はそれぞれ[ビットマップ](https://ja.wikipedia.org/wiki/ビットマップ "wikilink")と[アドレスを抽象化したものと考えられる](../Page/メモリアドレス.md "wikilink")。また Pascal は教育用ということもあり、最初の仕様では[分割コンパイル](https://ja.wikipedia.org/wiki/分割コンパイル "wikilink")や外部[ライブラリ](../Page/ライブラリ.md "wikilink")の利用が考慮されていなかった。これは大規模なプログラムを記述したり、ハードウェアを直接操作するプログラムを記述するには不便な仕様であり、入出力の扱いなど処理系に依存しなければならない部分を言語の中に抱える結果に繋がった。たとえばファイル型変数に特定のファイルを関連付ける標準的な方法はない。ヴィルト自身は Modula-2 でこれらの要請に応える一方で、Pascalでは実装のベンダがそれぞれ独自の拡張を施して、分割コンパイルやハードウェアの直接操作を可能としたが、この部分の互換性は乏しい。

## 実用プログラム例

著名なものに、[](../Page/TeX.md "wikilink")、初期の[Macintosh](../Page/Macintosh.md "wikilink")の[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink")および[アプリケーションなどがある](../Page/アプリケーションソフトウェア.md "wikilink")。

処理系に関しても、2019年現在も多くのプラットフォームに多くの実装がある。

  - AVRco\[1\] - マイクロプロセッサ用の Pascal。
  - [Delphi](../Page/Delphi.md "wikilink") - 現在最もメジャーな Pascal。
  - DWScript\[2\] - Delphi用のスクリプトエンジン。
  - [Free Pascal](../Page/Free_Pascal.md "wikilink") - オープンソースの Pascal。
  - [GNU Pascal](https://ja.wikipedia.org/wiki/GNU_Pascal "wikilink") - オープンソースの Pascal。
  - IP Pascal \[3\]- 標準 Pascal をベースに拡張された Pascal。
  - mikropascal\[4\] - マイクロプロセッサ用の Pascal。
  - Modern Pascal\[5\] - Free Pascalで書かれたマルチプラットフォームのインタプリタおよびP-Codeコンパイラ。
  - NewPascal\[6\] - Lazarus / [Free Pascal](../Page/Free_Pascal.md "wikilink") のフォーク。
  - Open Sibyl\[7\] - Speedsoft Sibyl のオープンソース実装。
  - [Oxygene](https://ja.wikipedia.org/wiki/:en:Oxygene_\(programming_language\) "wikilink") - .NET 用の Object Pascal。
  - PascalABC.NET\[8\] - .NET 用の Object Pascal。
  - Pascal Script\[9\] - DelphiまたはFree Pascalプロジェクト内で使えるスクリプトエンジン。
  - Pascal-P5\[10\] - 標準 Pascal に準拠したフルセットの Pascal-P。
  - PICco\[11\] - マイクロプロセッサ用の Pascal。
  - THINK Pascal\[12\] - Classic MacOS 用の 4.5d4 が無償公開されている。
  - Turbo Rascal\[13\] - Commodore 64/128、VIC-20、Nintendo ファミリーコンピュータ向けのクロスコンパイラ。
  - Turbo51\[14\] - 8051 マイクロプロセッサ用の Pascal。
  - Ultibo\[15\] - Raspberry Pi ベアメタルプログラミング用環境（Lazarus / [Free Pascal](../Page/Free_Pascal.md "wikilink") のカスタマイズ）。
  - Vector Pascal\[16\] - MMXやAMD 3d NowなどのSIMD命令セット用のPascal。
  - Virtual Pascal\[17\] - DOS、Windows、OS/2用
  - WDSibyl\[18\] - Speedsoft Sibyl のオープンソース実装。

## 初期の処理系実装

最初のPascalコンパイラは、[CDC](../Page/コントロール・データ・コーポレーション.md "wikilink") 6000 シリーズ用に1970年に書かれた1パスコンパイラで、それ自身が Pascal で書かれていた。CDC 6000 シリーズは 1[ワード](../Page/ワード.md "wikilink")が 60ビットのマシンであった。Pascal には、メモリを節約するための詰め合わせ機能(pack/unpack)や、10文字（1文字は6ビット）の詰め合わせ文字列である alfa 型の存在\[19\]、長いワードをビットごとに扱うための集合型など、CDC のアーキテクチャの影響を受けた箇所がある。CDC 用のコンパイラは、extern 宣言によって外部ライブラリを読み込むことができた\[20\]。

1972年から1974年にかけて[チューリッヒ工科大学](../Page/チューリッヒ工科大学.md "wikilink")で書かれたPascal-P\[21\]は、Pascal から[P コードへのコンパイラと](../Page/Pコードマシン.md "wikilink")、Pコードインタプリタからなる中間言語コンパイラで、やはり Pascal 自身で書かれていた。このことにより、後の Java が異なるアーキテクチャの計算機への移植が進んだのと同様、多くの計算機への移植が進んだ。中間言語コンパイラを移植するためには、仮想スタックマシンであるPコードマシンのエミュレータを移植元の機械で開発し、コンパイラを移植先の機械でコンパイルするだけで良い。[1970](../Page/1970年代.md "wikilink") - [80年代の低速な計算機では](../Page/1980年代.md "wikilink")、このような中間言語方式では性能が不十分だった。 Pascal-PにはPascal-P1・Pascal-P2・Pascal-P3・Pascal-P4の4つのバージョンがあるが、いずれもPascalのサブセット実装となっている。

1975年に[ニクラウス・ヴィルト](../Page/ニクラウス・ヴィルト.md "wikilink")がインタプリタであるPascal-S\[22\]を書いた。サブセットであるとはいえ、このPascalのソースコードは2,000行程しかない。

同じく1975年に[カリフォルニア工科大学](../Page/カリフォルニア工科大学.md "wikilink")で Pascal を並列動作用に拡張した[Concurrent Pascalが開発され](https://ja.wikipedia.org/wiki/:en:Concurrent_Pascal "wikilink")、それを使ってシングルユーザのオペレーティングシステムを開発し、Pascal が[システムプログラミングにも優れていることを明らかにした](../Page/システムソフトウェア.md "wikilink")。

1978年に[カリフォルニア大学サンディエゴ校](../Page/カリフォルニア大学サンディエゴ校.md "wikilink")（UCSD）でPascal-P2をベースにした[UCSD Pascalが開発された](../Page/UCSD_Pascal.md "wikilink")。これは、異なるプラットフォームに移植できるカスタムオペレーティングシステム（[UCSD p-System](https://ja.wikipedia.org/wiki/UCSD_p-System "wikilink")）上で実行可能なバージョンである。[Appleもライセンスを取得し](../Page/アップル_\(企業\).md "wikilink")、[Apple IIや](../Page/Apple_II.md "wikilink")[Apple IIIへ移植されている](../Page/Apple_III.md "wikilink")。

日本では、1979年に[シャープ](../Page/シャープ.md "wikilink")製[MZシリーズ向けに](../Page/MZ_\(コンピュータ\).md "wikilink")「Tiny PASCAL PALL」として発売されている\[23\]。

## 標準

ISOではPascalを[1983年](https://ja.wikipedia.org/wiki/1983年 "wikilink")に**ISO 7185**として標準化し現在は1990年版である。対応する日本の規格はJIS X 3008-1990で、改訂版は1994である。標準 Pascal には水準0と水準1があり、後者は長さの異なる配列を引数に取るための整合配列が使える\[24\]。また、拡張規格として**ISO/IEC 10206**が1991年に策定された。1993年のオブジェクト指向拡張の規格はドラフトで終わっている。

## アルゴリズムの記述に

以前ならばALGOLが使われていたであろう、論文や学会誌等におけるアルゴリズムの記述に、ALGOLに代わってPascalは使われるようになった。

## アルゴリズムの教科書に

Pascal は、アルゴリズムの教科書にしばしば使われた。ヴィルト自身による『アルゴリズム+データ構造=プログラム』をはじめ、[エイホ](../Page/アルフレッド・エイホ.md "wikilink")・[ホップクロフト](../Page/ジョン・ホップクロフト.md "wikilink")・[ウルマン](https://ja.wikipedia.org/wiki/ジェフリー・ウルマン "wikilink")『データ構造とアルゴリズム』などは Pascal を使用している。

## パーソナルコンピュータとPascal

1970年代末のパソコン上のシステムでは、[Apple II](../Page/Apple_II.md "wikilink") や [Z80](../Page/Z80.md "wikilink") システムで動作する [UCSD Pascal](../Page/UCSD_Pascal.md "wikilink") が動いていた\[25\]。[UCSD Pascal](../Page/UCSD_Pascal.md "wikilink") はPコードを使った中間コードコンパイラで、文字列型・case文の拡張・ユニットを使った [Modula-2](https://ja.wikipedia.org/wiki/Modula-2 "wikilink") 風の分割コンパイルなどをサポートしており、言語以外にメニューを使ったユーザーインターフェースも優れていた。

ほかに、[デジタルリサーチ](../Page/デジタルリサーチ.md "wikilink")社 の Pascal/MT+ やJRTシステムズ社の JRT pascal（日本では[ライフボート](../Page/ライフボート.md "wikilink")が αPascal として販売した）などが販売されていた。

### Turbo Pascalとその後継

1983年に[Borlandが発売したTurbo](../Page/ボーランド.md "wikilink") Pascalは（当初はZ80マシンの[CP/M](https://ja.wikipedia.org/wiki/CP/M "wikilink")で動作する）、大変高速な1パスコンパイラ兼開発環境である。 続いて8086マシン用（[CP/M-86](https://ja.wikipedia.org/wiki/CP/M-86 "wikilink"), [MS-DOS](../Page/MS-DOS.md "wikilink")）がリリースされ、1980年代後半〜1990年代前半に一般個人が所有するパーソナルコンピュータの環境として最も数の多かったMS-DOSにおいて大きな人気を得た。ビルドの高速さは、「コンパイラは、コンパイル時間があるので不便だ」という意識を、十分に速い環境であればたいして気にならないのだ、という事実を示して塗り替えた。さらに[WordStar](../Page/WordStar.md "wikilink")風のキー操作を持った、当時としては高機能な[フルスクリーンエディタ](https://ja.wikipedia.org/wiki/フルスクリーンエディタ "wikilink")を備えていながら低価格であったため、

「Turbo Pascal」は、版を重ねるにつれてモジュール機能や[オブジェクト指向](../Page/オブジェクト指向.md "wikilink")の拡張を加え、「Pascal処理系の実装としての名前」というよりも「Pascal を拡張した言語の名前」となった。 オブジェクト指向の拡張はやがて[Object Pascalという言語として認知されるようになった](../Page/Object_Pascal.md "wikilink")。BorlandはObject Pascalの開発環境をより充実させたWindows向けの製品として[Delphi](../Page/Delphi.md "wikilink")をリリースした。

Turbo Pascal と Delphi の成功によって、互換を謳った実装が開発されている。商用のものとしては Speed Pascal、Virtual Pascal、Microsoftの[QuickPascalがあり](https://ja.wikipedia.org/wiki/:en:QuickPascal "wikilink")、フリーソフトとしては [Free Pascal](../Page/Free_Pascal.md "wikilink")（元 FPK Pascal）が広い範囲のプラットフォームで動作する。ISO 標準 Pascal を意識したものでは、[GNU Pascal](https://ja.wikipedia.org/wiki/GNU_Pascal "wikilink") がある。また、Borland自身がDelphiをベースにして作った[GNU/Linuxシステム](https://ja.wikipedia.org/wiki/GNU/Linuxシステム "wikilink")向け開発環境の[Kylix](../Page/Kylix.md "wikilink")もある。

以上のように「Borlandの成功」が語られがちではあるが、実際のところ、Turbo Pascalの開発者である[アンダース・ヘルスバーグ](../Page/アンダース・ヘルスバーグ.md "wikilink")は、1990年代にMicrosoftに移籍している。ヘルスバーグはMicrosoftで[VJ++などを担当した後](https://ja.wikipedia.org/wiki/Microsoft_Visual_J++ "wikilink")、[C\#を開発している](../Page/C_Sharp.md "wikilink")。C\#は、C++とJavaの基本文法や特徴をベースに、ヘルスバーグの経験が反映された設計がなされており、Delphiおよび[Borland C++ Builderの影響もある](https://ja.wikipedia.org/wiki/Borland_C++_Builder "wikilink")\[26\]が、「Object Pascal のブロック表記などをC言語風に置き換えた」と説明するのは間違っている。

### MacintoshとPascal

当初、Macintoshにはセルフ開発環境はなく、システムの開発およびアプリケーションのクロス開発用プラットフォームとして、もっぱら[Lisa上で](../Page/Lisa_\(コンピュータ\).md "wikilink")[IDEのLisa](../Page/統合開発環境.md "wikilink") Workshopを使用した。Lisaの公式開発言語はPascalだったためMacintosh Toolboxと呼ぶAPIにおいても、その[呼び出し手法がPascalに準拠していたのはこうした理由による](https://ja.wikipedia.org/wiki/呼出規約#Pascal "wikilink")。Lisa PascalはSilicon Valley Software社の68000用ネイティブコードコンパイラをライセンス取得したもので、後にオブジェクト指向を取り入れたClascalに進化する。

後に登場したMacintosh用セルフ開発環境（MPW）には[ヴィルトと](../Page/ニクラウス・ヴィルト.md "wikilink") Apple の[ラリー・テスラー](https://ja.wikipedia.org/wiki/ラリー・テスラー "wikilink")率いるチームが開発した[Object Pascalが含まれていた](../Page/Object_Pascal.md "wikilink")。これはClascalの言語仕様を整理・発展させたものである。この環境で書かれてたアプリケーションとして[Adobe Photoshopがある](../Page/Adobe_Photoshop.md "wikilink")。

## 後継や派生

ニクラス・ヴィルト自身によって、Pascalや他の言語の経験にもとづき、後継と言える言語が設計されている。Pascalとの互換性を残した拡張といったようなスタイルではなく、そのため名前にもPascalを含めていない。

  - Modula - モジュール化などを指向した。Modula-2の方へ移ったため実質未完成。。
  - [Modula-2](https://ja.wikipedia.org/wiki/Modula-2 "wikilink") - モジュール化などの機能を追加した。ヴィルトは、Modula-2だけでオペレーティングシステムを含むシステムを作って見せた。
  - [Modula-3](https://ja.wikipedia.org/wiki/Modula-3 "wikilink") - [オブジェクト指向](../Page/オブジェクト指向.md "wikilink")など。
  - [Oberon](../Page/Oberon.md "wikilink"), [Oberon-2](https://ja.wikipedia.org/wiki/Oberon-2 "wikilink") - 言語を拡張して強力にするのではなく、拡張可能にしてコア部分は小さくする、という方向性で設計されている。

その他の言語ないし実装

  - [Object Pascal](../Page/Object_Pascal.md "wikilink") - [オブジェクト指向](../Page/オブジェクト指向.md "wikilink")的拡張
  - Concurrent Pascal - コンカレント（並行）拡張
  - [Component Pascal](https://ja.wikipedia.org/wiki/Component_Pascal "wikilink")
  - [Ada](../Page/Ada.md "wikilink") - [アメリカ国防総省](../Page/アメリカ国防総省.md "wikilink")の意向で策定された多機能な言語。PascalないしAlgolの影響が大きいが、Pascalの「簡潔に」とは正反対の巨大化という方向性はALGOL 68（[:en:ALGOL 68](https://ja.wikipedia.org/wiki/:en:ALGOL_68 "wikilink")）の魂の影響があるかもしれない\[27\]
  - [VHDL](../Page/VHDL.md "wikilink") - Adaの影響が多大な[ハードウェア記述言語](../Page/ハードウェア記述言語.md "wikilink")
  - [Verilog](../Page/Verilog.md "wikilink") HDL - C言語風やPascal風などともいわれるが、どちらにも似ていないハードウェア記述言語
  - [SystemVerilog](../Page/SystemVerilog.md "wikilink") - Verilogの拡張
  - [Delphi](../Page/Delphi.md "wikilink") - [Object Pascal](../Page/Object_Pascal.md "wikilink") を、さらに拡張している。IDEによるGUIアプリの開発支援もある統合環境が用意された。
  - [Eiffel](../Page/Eiffel.md "wikilink") - 構文がPascalに似ている、とも言われる[オブジェクト指向言語](https://ja.wikipedia.org/wiki/オブジェクト指向言語 "wikilink")

## 批判

「[本物のプログラマはPascalを使わない](../Page/本物のプログラマはPascalを使わない.md "wikilink")」というエッセイは、そのタイトルだけは有名だが、Pascalについては実のところ、[構造化プログラミング](../Page/構造化プログラミング.md "wikilink")の代名詞のような感じで引き合いに出されているだけであり、その内容についても、当のハッカーたちからも否定と肯定が半々といった所である（例えば[ジャーゴンファイル](../Page/ジャーゴンファイル.md "wikilink")では、用語集本体では否定的に、附録では肯定的に言及している）。本格的な批判の文章としては、[カーニハンによる](../Page/ブライアン・カーニハン.md "wikilink")*Why Pascal is Not My Favorite Programming Language*\[28\]がある。

初期の批判にもかかわらずPascalは進化し続けた。そして[カーニハンの批判ポイントの殆どは商用バージョンのPascalに当てはまらなくなった](../Page/ブライアン・カーニハン.md "wikilink")。例えば論文*The Pascal Programming Language*\[29\]のMyth 6節で拡張Pascalの言語仕様に基づき、論文*The Macintosh Programmer's Workshop*\[30\]では、Object Pascal（MPW Pascal）の言語仕様に基づき、批判ポイントの殆どは克服していると語られている。

## 脚注

### 注釈

### 出典

## 文献

  -
  -
  -
  -
  -
## 外部リンク

  - [FreePascal](http://www.freepascal.org/) - Pascal と Object Pascal のフリーなコンパイラ
  - [GNU Pascal](http://www.gnu-pascal.de/gpc/h-index.html) - [GCCのコンパイラ](../Page/GNUコンパイラコレクション.md "wikilink")

[Category:Pascal](https://ja.wikipedia.org/wiki/Category:Pascal "wikilink") [Category:プログラミング言語](https://ja.wikipedia.org/wiki/Category:プログラミング言語 "wikilink") [Category:JIS](https://ja.wikipedia.org/wiki/Category:JIS "wikilink") [Category:ブレーズ・パスカル](https://ja.wikipedia.org/wiki/Category:ブレーズ・パスカル "wikilink") [Category:教育用プログラミング言語](https://ja.wikipedia.org/wiki/Category:教育用プログラミング言語 "wikilink")

1.  <https://www.e-lab.de/AVRco/index_en.html>
2.  <https://www.delphitools.info/dwscript/>
3.  <http://www.moorecad.com/ippas/>
4.  <https://www.mikroe.com/mikropascal>
5.  <http://www.modernpascal.com/>
6.  <http://newpascal.org/>
7.  <http://sibyl.netlabs.org/en/site/index.xml>
8.  <http://pascalabc.net/en/>
9.  <https://www.remobjects.com/ps.aspx>
10. <http://www.standardpascal.org/p5.html>
11. <https://www.e-lab.de/PICco/>
12. <http://www.think-pascal.org/>
13. <http://www.lemonspawn.com/turbo-rascal-syntax-error-expected-but-begin/>
14. <http://turbo51.com/>
15. <https://ultibo.org/>
16. <https://sourceforge.net/projects/vectorpascalcom/>
17. <http://vpascal.ning.com/>
18. <https://www.wdsibyl.org/>
19. 『Pascal』第二版
20. 『Pascal』第二版
21.
22.
23. 工学舎 月刊I/O 1979年12月号 PASCAL時代がやってきた\! mz-80k用Tiny PASCAL「PALL」全リスト公開
24.
25.
26. <http://softwareengineering.stackexchange.com/questions/96793/in-what-specific-ways-did-delphi-influence-the-c-language/96927#96927>
27. [ホーアの](../Page/アントニー・ホーア.md "wikilink") *The Emperor's Old Clothes* も参照。
28. <https://www.lysator.liu.se/c/bwk-on-pascal.html>
29. <http://pascal-central.com/ppl/index.html>
30. <http://collaboration.cmc.ec.gc.ca/science/rpn/biblio/ddj/Website/articles/DDJ/1988/8814/8814b/8814b.htm>
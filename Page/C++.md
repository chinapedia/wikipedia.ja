> この記事は[C++](https://ja.wikipedia.org/wiki/C++)から翻訳されています。


**C++**（**シープラスプラス**）は、汎用[プログラミング言語](../Page/プログラミング言語.md "wikilink")のひとつである。派生元である[C言語](../Page/C言語.md "wikilink")の機能や特徴を継承しつつ、表現力と効率性の向上のために、[手続き型プログラミング](https://ja.wikipedia.org/wiki/手続き型プログラミング "wikilink")・[データ抽象](https://ja.wikipedia.org/wiki/抽象データ型 "wikilink")・[オブジェクト指向プログラミング](https://ja.wikipedia.org/wiki/オブジェクト指向プログラミング "wikilink")・[ジェネリックプログラミング](https://ja.wikipedia.org/wiki/ジェネリックプログラミング "wikilink")といった複数の[プログラミングパラダイム](https://ja.wikipedia.org/wiki/プログラミングパラダイム "wikilink")が組み合わされている\[1\]。C言語のようにハードウェアを直接扱うような下位層向けの[低水準言語](https://ja.wikipedia.org/wiki/低水準言語 "wikilink")としても、複雑な[アプリケーションソフトウェア](https://ja.wikipedia.org/wiki/アプリケーションソフトウェア "wikilink")を開発するための上位層向け[高水準言語](https://ja.wikipedia.org/wiki/高水準言語 "wikilink")としても使用可能である。[アセンブリ言語](https://ja.wikipedia.org/wiki/アセンブリ言語 "wikilink")以外の[低水準言語](https://ja.wikipedia.org/wiki/低水準言語 "wikilink")を必要としないこと、使わない機能に時間的・空間的コストを必要としないことが、言語設計の重要な原則となっている\[2\]\[3\]。

C++は、1983年に[AT\&Tベル研究所の計算機科学者](https://ja.wikipedia.org/wiki/ベル研究所 "wikilink")[ビャーネ・ストロヴストルップ](https://ja.wikipedia.org/wiki/ビャーネ・ストロヴストルップ "wikilink")によって公開された。、様々な[プラットフォームでその開発環境が導入された](https://ja.wikipedia.org/wiki/プラットフォーム_\(コンピューティング\) "wikilink")。1998年から[ISOと](https://ja.wikipedia.org/wiki/国際標準化機構 "wikilink")[IECの共同で言語仕様と](https://ja.wikipedia.org/wiki/国際電気標準会議 "wikilink")[テンプレートライブラリの標準化が行われるようになり](https://ja.wikipedia.org/wiki/Standard_Template_Library "wikilink")、その後2003年、2011年、2014年、2017年に標準規格が改訂されている。2019年現在の最新規格は「ISO/IEC 14882:2017」通称「[C++17](https://ja.wikipedia.org/wiki/C++17 "wikilink")」である。

## 歴史

ストロヴストルップはプログラミング言語**C with Classes**（クラス付きのC言語）の開発を[1979年](https://ja.wikipedia.org/wiki/1979年 "wikilink")に開始した。彼は大規模なソフトウェアの開発に有用な特徴を[Simula](https://ja.wikipedia.org/wiki/Simula "wikilink")が備えていることに気がついたが、Simulaは実行速度が遅く実用的ではなかった。一方で[BCPL](https://ja.wikipedia.org/wiki/BCPL "wikilink")は実行速度こそ速かったものの、大規模なソフトウェア開発を念頭に置いた場合にあまりにも[低級だった](https://ja.wikipedia.org/wiki/低級言語 "wikilink")。

これらの事情を鑑みて、ストロヴストルップは当時既に汎用的な言語だったC言語にSimulaの特徴を取り入れることを試みた。この取り組みにあたっては[ALGOL](https://ja.wikipedia.org/wiki/ALGOL "wikilink")68 や[Ada](../Page/Ada.md "wikilink")、 [CLU](https://ja.wikipedia.org/wiki/CLU "wikilink")、 [ML等の言語の影響も受けている](https://ja.wikipedia.org/wiki/プログラミング言語ML "wikilink")。最初はクラスと派生クラス、型検査機構の強化、[インライン関数](https://ja.wikipedia.org/wiki/インライン関数 "wikilink")、デフォルト引数の機能を、[Cfront](https://ja.wikipedia.org/wiki/Cfront "wikilink")を介してC言語に追加した。[1985年](https://ja.wikipedia.org/wiki/1985年 "wikilink")[10月](https://ja.wikipedia.org/wiki/10月 "wikilink")に最初の商用リリースがなされた\[4\]。

[1983年](https://ja.wikipedia.org/wiki/1983年 "wikilink")にはC with Classesから**C++**に名称を変更した。この際に、[仮想関数](https://ja.wikipedia.org/wiki/仮想関数 "wikilink")と、関数と演算子の[多重定義](https://ja.wikipedia.org/wiki/多重定義 "wikilink")、[参照型](https://ja.wikipedia.org/wiki/参照_\(情報工学\) "wikilink")、`const`型、ユーザー制御可能な自由領域メモリ制御、型検査機構の改良、BCPL形式の（「`//`」による）行単位のコメントなどの機能が追加された。[1985年](https://ja.wikipedia.org/wiki/1985年 "wikilink")には『The C++ Programming Language』の初版が出版された（邦訳『プログラミング言語C++』[1988年](../Page/1988年.md "wikilink"))）。この時点では公式な標準が策定されていなかったために、この本が事実上のリファレンスとなった。[1989年](https://ja.wikipedia.org/wiki/1989年 "wikilink")C++のバージョン2.0として、[多重継承](https://ja.wikipedia.org/wiki/多重継承 "wikilink")と[抽象クラス](https://ja.wikipedia.org/wiki/抽象クラス "wikilink")、静的[メンバ関数](https://ja.wikipedia.org/wiki/メンバ関数 "wikilink")、`const`メンバ関数、[`protected`メンバ等の機能が追加されたものがリリースされた](https://ja.wikipedia.org/wiki/アクセス制御 "wikilink")。[1990年](https://ja.wikipedia.org/wiki/1990年 "wikilink")に『The Annotated C++ Reference Manual (ARM)』\[5\]（邦訳『注解C++リファレンスマニュアル』\[6\]）が出版され、将来の標準化の土台となるものを提供した。後に追加された機能には[テンプレートと](https://ja.wikipedia.org/wiki/テンプレート_\(プログラミング\) "wikilink")[例外処理](https://ja.wikipedia.org/wiki/例外処理 "wikilink")、[名前空間](https://ja.wikipedia.org/wiki/名前空間 "wikilink")、新形式の[キャスト](https://ja.wikipedia.org/wiki/型変換 "wikilink")、[ブール型](https://ja.wikipedia.org/wiki/ブール型 "wikilink")が含まれた。

ARMが事実上の標準として使われた時代が続いたが、標準化が進んだ。C++言語の最初の標準は[1998年](https://ja.wikipedia.org/wiki/1998年 "wikilink")にISO/IEC 14882:1998として承認された。2003年の改訂版を経て、[2011年](https://ja.wikipedia.org/wiki/2011年 "wikilink")にメジャーアップデートとして制定されたのがISO/IEC 14882:2011、通称「**[C++11](https://ja.wikipedia.org/wiki/C++11 "wikilink")**」である。このバージョンは、元々、非公式に「C++0x」と呼ばれていた。[2000年代](../Page/2000年代.md "wikilink")中に制定され、正式に「C++09」と呼称されることを見越した仮称だったが、2000年代中には実現しなかった。2011年8月10日まで続いた最終国際投票で C++0x は全会一致で承認された。これにより C++0x と呼ばれてきた C++ の次期改正案はついに国際標準になり、[C++11](https://ja.wikipedia.org/wiki/C++11 "wikilink")と呼べるようになった。また、[2014年](https://ja.wikipedia.org/wiki/2014年 "wikilink")にはISO/IEC 14882:2014、通称「**[C++14](https://ja.wikipedia.org/wiki/C++14 "wikilink")**」が策定された。[2017年](https://ja.wikipedia.org/wiki/2017年 "wikilink")にはISO/IEC 14882:2017、通称「**[C++17](https://ja.wikipedia.org/wiki/C++17 "wikilink")**」が策定された。2020年にはISO/IEC 14882:2020、通称「**[C++20](https://ja.wikipedia.org/wiki/C++20 "wikilink")**」が策定される予定である。

C++言語の進化に伴い、標準ライブラリもまた進化していった。C++標準ライブラリに最初に追加されたのは、従来のC言語の [`printf`](https://ja.wikipedia.org/wiki/printf "wikilink")() や [`scanf`](https://ja.wikipedia.org/wiki/scanf "wikilink")() といった関数を置き換えるストリームI/Oライブラリである。また、C++98における標準ライブラリへの追加で最も重要なものは[Standard Template Library](https://ja.wikipedia.org/wiki/Standard_Template_Library "wikilink") (STL) である。C++11では、[正規表現](https://ja.wikipedia.org/wiki/正規表現 "wikilink")による検索・置換や複数[スレッドでの同時実行](https://ja.wikipedia.org/wiki/スレッド_\(コンピュータ\) "wikilink")、[ハッシュテーブル](https://ja.wikipedia.org/wiki/ハッシュテーブル "wikilink")・ハッシュセットの追加などさらなる拡充が続いている。

### 国際規格

| 規格出版日      | C++ 国際規格                   | 非公式名称                                                                     | 対応する日本工業規格      |
| ---------- | -------------------------- | ------------------------------------------------------------------------- | --------------- |
| 1998-09-01 | ISO/IEC 14882:1998\[7\]    | C++98                                                                     | ―               |
| 2003-10-16 | ISO/IEC 14882:2003\[8\]    | [C++03](https://ja.wikipedia.org/wiki/C++03 "wikilink")                   | JIS X 3014:2003 |
| 2007-11-15 | ISO/IEC TR 19768:2007\[9\] | [C++TR1](https://ja.wikipedia.org/wiki/C++_Technical_Report_1 "wikilink") | ―               |
| 2011-09-01 | ISO/IEC 14882:2011\[10\]   | [C++11](https://ja.wikipedia.org/wiki/C++11 "wikilink")                   | ―               |
| 2014-12-15 | ISO/IEC 14882:2014\[11\]   | [C++14](https://ja.wikipedia.org/wiki/C++14 "wikilink")                   | ―               |
| 2017-12    | ISO/IEC 14882:2017\[12\]   | [C++17](https://ja.wikipedia.org/wiki/C++17 "wikilink")                   | ―               |
| 2020年 予定   |                            | C++20                                                                     | ―               |

長年にわたる作業の後、[ANSI](https://ja.wikipedia.org/wiki/ANSI "wikilink")とISOの合同委員会はプログラミング言語C++を1998年に標準化した (ISO/IEC 14882:1998)。1998年の標準の公式なリリースから数年間にわたって委員会は不具合の報告を続け、[2003年](../Page/2003年.md "wikilink")に訂正版を出版した。[2003年](../Page/2003年.md "wikilink")[12月](https://ja.wikipedia.org/wiki/12月 "wikilink")に制定された日本産業規格は、ISO/IEC 14882:2003 (E) の日本語訳である。

2007年11月15日、[C++ Technical Report 1](https://ja.wikipedia.org/wiki/C++_Technical_Report_1 "wikilink") (TR1) という技術報告書（テクニカルレポート）がリリースされた。これは規格の公式な一部ではなかったが、次の版のC++に含まれると期待される、標準ライブラリへの数多くの拡張を与えた。TR1の内容は、多少の修正を加えてC++11に取り込まれている。

2011年9月1日、C++98以来初の大きな改訂となるISO/IEC 14882:2011が発行された。

2014年8月18日、ISO/IEC 14882:2014 (C++14) が投票で承認され\[13\]、2014年12月15日に公式に出版された。

2017年12月、ISO/IEC 14882:2017 (C++17) が公式に発行された。

2019年現在、C++20の仕様策定が進められている。

### 将来

C++に対しては、今もなお要望が絶えない。特に[Boost C++ライブラリを開発しているBoostコミュニティはC](https://ja.wikipedia.org/wiki/Boost_C++ライブラリ "wikilink")++の方向性の決定に大きく貢献し、さらにC++標準化委員会へ改良すべき点などを意見している。現在はマルチパラダイムプログラミングをより自然に行えるようにすることに力が注がれており、たとえばBoostでは、C++の[関数型プログラミングや](../Page/関数型言語.md "wikilink")[メタプログラミング](https://ja.wikipedia.org/wiki/メタプログラミング "wikilink")の可能性を模索している。

[C++11](https://ja.wikipedia.org/wiki/C++11 "wikilink")と呼ばれている新しいバージョンのC++標準ではこれらの一部が取り込まれ、今後のC++でもさらなる追加が行われると見られている。

### C++という名称

この名称はRick Mascittiの功績で、最初に使用されたのは1983年の12月である。初期の研究期間では、開発中の言語は「C with Classes」と呼ばれていた。最終名は、変数の値を一つ加算する、C言語の`++`（[インクリメント](https://ja.wikipedia.org/wiki/インクリメント "wikilink")）演算子からの派生である。また一般的な命名規則での「+」の使用は、機能強化されたコンピュータプログラムを意味する。ストロヴストルップによれば「この名前は、C言語からの変更の革新的な本質を示している」ということである。C+は、より初期の無関係なプログラミング言語の名前である。

ストロヴストルップは著書『The C++ Programming Language』の前文で名前の起源を語り、[ジョージ・オーウェル](https://ja.wikipedia.org/wiki/ジョージ・オーウェル "wikilink")の小説『[1984年](https://ja.wikipedia.org/wiki/1984年_\(小説\) "wikilink")』の付録から「C++」が連想されるかもしれないと付け加えている。[ニュースピーク](https://ja.wikipedia.org/wiki/ニュースピーク "wikilink")という架空の言語の解説に宛てられた3つの章の中に、科学技術に関する専門用語とジャーゴンの解説に宛てられた「C vocabulary」という章がある。ニュースピークで「ダブルプラス」は最上級の修飾語である。ゆえにニュースピークで「C++」は「最も極端な専門用語またはジャーゴン」という意味になるだろう。

1992年、Rick Mascittiは名前について非公式に質問されると、彼はおふざけのつもりで命名したという旨の回答をした。彼はこの言語の正式な名称になるとは夢にも思っていなかった。

## 哲学

ビャーネ・ストロヴストルップは著書『[C++の設計と進化](https://ja.wikipedia.org/wiki/:en:The_Design_and_Evolution_of_C++ "wikilink")(1994)』でC++を設計する際に用いたルールを述べている。

  - C++はCと同等の実行効率と移植性を持つ[静的に型付けされた汎用言語である](https://ja.wikipedia.org/wiki/型システム "wikilink")。
  - C++は直接的かつ包括的に複数のプログラミングスタイル（[手続き型プログラミング](https://ja.wikipedia.org/wiki/手続き型プログラミング "wikilink")、[抽象化](https://ja.wikipedia.org/wiki/抽象化_\(計算機科学\) "wikilink")、[オブジェクト指向](../Page/オブジェクト指向.md "wikilink")、[ジェネリックプログラミング](https://ja.wikipedia.org/wiki/ジェネリックプログラミング "wikilink")）をサポートする。
  - C++はもしプログラマが間違っている可能性があったとしても[プログラマ](https://ja.wikipedia.org/wiki/プログラマ "wikilink")に選択の余地を与える。
  - C++は可能な限りC言語との互換性を持ち、C言語からスムーズに移行できる。
  - C++はプラットフォームに固有な機能や汎用的でない機能の実装を避ける。
  - C++は利用しない機能についてはオーバーヘッドが生じない（ゼロオーバーヘッドの原則）。
  - C++は高級な実行環境を必要としない。

C++のコンパイラがどのようにコードを出力しメモリのレイアウトを決めるのかということについては『Inside the C++ Object Model』(Lippman, 1996)に記載されている。ただしコンパイラが出力するコードの仕様はコンパイラ制作者の裁量に任されている。

## 標準ライブラリ

1998年に施行された[ANSI](https://ja.wikipedia.org/wiki/ANSI "wikilink")/[ISO](https://ja.wikipedia.org/wiki/国際標準化機構 "wikilink") C++ [規格は言語仕様と](https://ja.wikipedia.org/wiki/標準化 "wikilink")[ライブラリの](https://ja.wikipedia.org/wiki/標準C++ライブラリ "wikilink")2つのパートで構成される。ライブラリ規格の大半は[Standard Template Library](https://ja.wikipedia.org/wiki/Standard_Template_Library "wikilink") (STL)とC言語の標準ライブラリの改良版についての内容である。標準規格以外にも様々なライブラリが数多く存在し、リンカを使用することにより、[C言語](../Page/C言語.md "wikilink")、[FORTRAN](../Page/FORTRAN.md "wikilink")、[Pascal](https://ja.wikipedia.org/wiki/Pascal "wikilink")、[BASIC](../Page/BASIC.md "wikilink")のような言語を用いて作成されたライブラリを利用できる。規格外のライブラリが利用できるかどうかはコンパイラに依存する。

C++標準ライブラリはC++向けに若干の最適化が施されたC言語標準ライブラリを含んでいる。C++標準ライブラリの大部分はSTLである。 [コンテナ](https://ja.wikipedia.org/wiki/コンテナ_\(データ型\) "wikilink")（[可変長配列](https://ja.wikipedia.org/wiki/可変長配列 "wikilink")や[リストなど](https://ja.wikipedia.org/wiki/連結リスト "wikilink")）、コンテナを配列のように扱えるようにする[イテレータ](https://ja.wikipedia.org/wiki/イテレータ "wikilink")、検索やソートを行う[アルゴリズム](../Page/アルゴリズム.md "wikilink")といった有用なツールが提供されている。さらに`map`や`multimap`のような[連想配列](https://ja.wikipedia.org/wiki/連想配列 "wikilink")や、`set`や`multiset`のようなソート済みコンテナも提供され、これらは全てインターフェイスに互換性がある。テンプレートを用いることにより、あらゆるコンテナ(またはイテレータで定義したシーケンス)に適用できる汎用的なアルゴリズムを記述できる。C言語と同様に[ライブラリ](https://ja.wikipedia.org/wiki/ライブラリ "wikilink")の機能には`#include` [ディレクティブ](https://ja.wikipedia.org/wiki/ディレクティブ "wikilink")を使ってヘッダファイルを読み込むことによってアクセスする。C++には[69本の標準ヘッダファイルがあるが](https://ja.wikipedia.org/wiki/標準C++ライブラリ#Standard_headers "wikilink")、このうち19本については非推奨となっている。

STLは標準規格に採用される前は、[ヒューレット・パッカード](https://ja.wikipedia.org/wiki/ヒューレット・パッカード "wikilink")の（一時は[シリコングラフィックス](https://ja.wikipedia.org/wiki/シリコングラフィックス "wikilink")の）商用ライブラリだった。STLは標準規格の単なる一部分に過ぎず規格書にSTLという表記は見られないが、入出力ストリーム、国際化、デバッグ機能、C言語標準ライブラリ等の、STL以外の部分と区別するために、今でも多くの人がSTLという用語を使っている。

大半のC++コンパイラはSTLを含むC++標準ライブラリの実装を提供している。[STLPort](https://ja.wikipedia.org/wiki/STLPort "wikilink")のようなコンパイラ非依存のSTLも存在する。様々な目的でC++標準ライブラリを独自に実装しているプロジェクトは他にもある。

C++の標準ライブラリは大きく次のように分けられる。多種多様な実行環境が存在することを考慮して、[GUIに関するライブラリは標準に含まれていない](https://ja.wikipedia.org/wiki/グラフィカルユーザインターフェース "wikilink")。

  - 言語サポート（型情報、例外処理など）
  - 診断（アサート（[表明](https://ja.wikipedia.org/wiki/表明 "wikilink")）、エラー情報）
  - 汎用ユーティリティ（タプル、[動的メモリ確保](https://ja.wikipedia.org/wiki/動的メモリ確保 "wikilink")、スマートポインタ、[メタプログラミング](https://ja.wikipedia.org/wiki/メタプログラミング "wikilink")など）
  - [文字列](https://ja.wikipedia.org/wiki/文字列 "wikilink")・[正規表現](https://ja.wikipedia.org/wiki/正規表現 "wikilink")
  - ロケール（[国際化と地域化](https://ja.wikipedia.org/wiki/国際化と地域化 "wikilink")）
  - コンテナ（[データ構造](../Page/データ構造.md "wikilink")）・イテレータ・アルゴリズム（いわゆる[STL](https://ja.wikipedia.org/wiki/Standard_Template_Library "wikilink")）
  - 数値演算
  - [入出力](https://ja.wikipedia.org/wiki/入出力 "wikilink")
  - アトミック演算（[不可分操作](https://ja.wikipedia.org/wiki/不可分操作 "wikilink")）
  - [スレッド](https://ja.wikipedia.org/wiki/スレッド_\(コンピュータ\) "wikilink")

## 外部ライブラリ

以下に、C++で広く使われているライブラリを挙げる。

  - [Boost C++ライブラリ](https://ja.wikipedia.org/wiki/Boost_C++ライブラリ "wikilink")
    様々なC++汎用ライブラリの集合。[正規表現](https://ja.wikipedia.org/wiki/正規表現 "wikilink")を扱うBoost.Regexや[無名関数](https://ja.wikipedia.org/wiki/無名関数 "wikilink")（[ラムダ計算](https://ja.wikipedia.org/wiki/ラムダ計算 "wikilink")）を簡潔に記述できるBoost Lambda Libraryなどがある。C++11やC++14などでも、Boostに存在するライブラリが標準ライブラリに採用されたり、標準ライブラリとして提案された項目がBoostで先行して実装されたりしている。これにより、実際に実装・使用することでの知見が得られ、標準ライブラリとして採用される際に活かされている。
  - [Apache Xerces](https://ja.wikipedia.org/wiki/Apache_Xerces "wikilink")
    C++での主要[XML](https://ja.wikipedia.org/wiki/Extensible_Markup_Language "wikilink")[パーサの一つ](https://ja.wikipedia.org/wiki/構文解析器 "wikilink")。Java版も存在する。
  - [CppUnit](https://ja.wikipedia.org/wiki/xUnit "wikilink")
    C++での[ユニットテスト](https://ja.wikipedia.org/wiki/ユニットテスト "wikilink")フレームワーク。 クラス毎の動作確認に威力を発揮する。

## 特徴

[C言語](../Page/C言語.md "wikilink")に、[オブジェクト指向プログラミング](https://ja.wikipedia.org/wiki/オブジェクト指向プログラミング "wikilink")をはじめとする様々なプログラミングパラダイムをサポートするための改良が加えられたものといえる。ただし、他のプログラミング言語と違い、旧来のCと同様に手続き型言語としても扱えるという特徴がある。また、C言語と比べて型チェックが厳しくなっており、型安全性が向上している。このことから、C++を*better C*というふうに呼ぶことがある。すなわち、基本的にC言語に対して上位互換性がある。初期のC++はCへのトランスレータとして実装され、C++プログラムを一旦Cプログラムに変換してから[コンパイルしていた](../Page/コンパイラ.md "wikilink")。

ただし、C++という名称が定まった当初の時期から、C言語とC++との間には厳密な互換性はない\[14\]\[15\]。当時、Cとの互換性について議論の末、「C++とANSI Cの間には不正当な非互換性はない」という合意が形成されることとなった。そのため、正当な非互換性を巡って多くの議論が発生した\[16\]。ただし、まだANSIによるC言語の標準規格も策定途中の時期である。

その後、先祖であるC言語のANSIによる標準規格制定時には、関数のプロトタイプ宣言や`const`修飾など、C++の機能がC言語に取り入れられることにもなった。[C99](https://ja.wikipedia.org/wiki/C99 "wikilink")の出現により、`//`コメントなどのC++で使われていた便利な機能が加わってCとC++の互換性が高まる一方、別々に審議し、別の時期に発行していることと、開発対象が必ずしも同じでないために利害関係者が異なることによる違いもある。

次のような多種多様な機能を持っており、言語仕様は大変複雑である。

  - [多重継承](https://ja.wikipedia.org/wiki/多重継承 "wikilink")
  - [テンプレート](https://ja.wikipedia.org/wiki/テンプレート_\(プログラミング\) "wikilink")
  - [演算子](https://ja.wikipedia.org/wiki/演算子 "wikilink")の[オーバーロード](https://ja.wikipedia.org/wiki/多重定義 "wikilink")
  - [例外処理](https://ja.wikipedia.org/wiki/例外処理 "wikilink")
  - [実行時型情報](https://ja.wikipedia.org/wiki/実行時型情報 "wikilink") (RTTI)

ここから、よりオブジェクト指向を強化し、「なんでもあり」ではない代わりに分かりやすくスマートな設計を目指した新たな言語（[Java](https://ja.wikipedia.org/wiki/Java "wikilink")、[D言語](https://ja.wikipedia.org/wiki/D言語 "wikilink")など）が作られることとなった。

### Hello, World\!

C++はC言語およびそのプリプロセッサの構文をほぼ継承している。以下のサンプルは[ビャーネ・ストロヴストルップ](https://ja.wikipedia.org/wiki/ビャーネ・ストロヴストルップ "wikilink")の書籍「The C++ Programming Language, 4th Edition」(ISBN 978-0321563842) の「2.2.1 Hello, World\!」に記載されている[標準C++ライブラリ](https://ja.wikipedia.org/wiki/標準C++ライブラリ "wikilink")のストリーム機能を用いて[標準出力に出力する](https://ja.wikipedia.org/wiki/標準ストリーム#Standard_output_.28stdout.29 "wikilink")[Hello worldプログラムである](https://ja.wikipedia.org/wiki/Hello_world "wikilink")\[17\]\[18\]。

``` cpp
#include <iostream>

int main()
{
    std::cout << "Hello, World!\n";
}
```

書籍でも明記されているが、`main()`関数で意図的に返り値を返さない手法が使用されている。

### 演算子と演算子のオーバーロード

C++には四則演算、ビット演算、参照、比較、論理演算などの30を超える演算子がある。メンバーアクセス演算子（`.`と`.*`）のような一部の例外はあるが、大半の演算子はユーザー定義によるオーバーロードが可能である。オーバーロード可能な演算子が豊富に揃えられているためC++を一種の[ドメイン固有言語](https://ja.wikipedia.org/wiki/ドメイン固有言語 "wikilink")として利用できる。またオーバーロード可能な演算子はスマートポインタのような先進的な実装テクニックに欠かせないものとなっている。演算子をオーバーロードしても[演算の優先順位](https://ja.wikipedia.org/wiki/演算の優先順位 "wikilink")は変化せず、また演算子のオペランドの数も変化しない。ただし指定したオペランドが無視される可能性はある。

### テンプレート

C++には、[ジェネリックプログラミング](https://ja.wikipedia.org/wiki/ジェネリックプログラミング "wikilink")を実現する機能として**テンプレート**が存在する。テンプレートにできる対象は、関数とクラスである。C++14以降では変数もテンプレートの対象となった。テンプレートはコード中の型および定数をパラメータ化できる。テンプレートのパラメータ（テンプレート仮引数）に、型、コンパイル時定数またはその他のテンプレート（テンプレート実引数）を与えることで、テンプレートはコンパイル時に**インスタンス化**（実体化・具現化などとも）される。コンパイラは関数やクラスをインスタンス化するために、テンプレート仮引数をテンプレート実引数に置き換える。テンプレートは[ジェネリックプログラミング](https://ja.wikipedia.org/wiki/ジェネリックプログラミング "wikilink")、[テンプレートメタプログラミング](https://ja.wikipedia.org/wiki/テンプレートメタプログラミング "wikilink")、コード最適化などのために利用される強力なツールであるが、一定のコストを伴う。各テンプレートのインスタンスはテンプレート仮引数毎にテンプレートコードのコピーを生成するためコードサイズが肥大化する。これはコンパイル時に実型引数の情報を削除することで単一の型インスタンスを生成するランタイム型のジェネリクスを実装した[Java](https://ja.wikipedia.org/wiki/Java "wikilink")などの言語とは対照的である。なお、[C\#](../Page/C_Sharp.md "wikilink") ([.NET Framework](https://ja.wikipedia.org/wiki/.NET_Framework "wikilink")) は[実行時コンパイラ](https://ja.wikipedia.org/wiki/実行時コンパイラ "wikilink")により実型引数の情報を削除することなく複数の型インスタンスを生成する方式を採用しており、C++とJavaの中間的なアプローチとなっている。

テンプレートとプリプロセッサマクロはいずれもコンパイル時に処理される言語機能であり、静的な条件に基づいたコンパイルが行われるが、テンプレートは字句の置き換えに限定されない。テンプレートはC++の構文と型を解析し、厳密な型チェックに基づいた高度なプログラムの流れの制御ができる。マクロは条件コンパイルに利用できるが、新しい型の生成、再帰的定義、型の評価などは行えないため、コンパイル前のテキストの置き換えや追加・削除といった用途に限定される。つまりマクロは事前に定義されたシンボルに基づいてコンパイルの流れを制御できるものの、テンプレートとは異なり独立して新しいシンボルを生成することはできない。テンプレートは静的な[多態](https://ja.wikipedia.org/wiki/ポリモーフィズム "wikilink")（下記参照）と[ジェネリックプログラミング](https://ja.wikipedia.org/wiki/ジェネリックプログラミング "wikilink")のためのツールである。

C++のテンプレートはコンパイル時における[チューリング完全](https://ja.wikipedia.org/wiki/チューリング完全 "wikilink")なメカニズムである。これは[テンプレートメタプログラミング](https://ja.wikipedia.org/wiki/テンプレートメタプログラミング "wikilink")を用いて実行する前にコンピュータが計算可能なあらゆる処理を表現できることを意味している。

概略すれば、テンプレートはコードの記述に本来必要な型や定数を明確にすることなく抽象的な記述ができる、パラメータ化された関数またはクラスである。テンプレート仮引数に実引数を与えてインスタンス化した結果は、テンプレート仮引数に指定した型に特化した形で記述されたコードと全く等価になる。これによりテンプレートは、汎用的かつおおまかに記述された関数およびクラス（テンプレート）と、特定の型に特化した実装（インスタンス化されたテンプレート）の依存関係を解消し、パフォーマンスを犠牲にすることなく抽象化できる手段を提供する。

### オブジェクト

C++は[C言語](../Page/C言語.md "wikilink")に[オブジェクト指向プログラミング](https://ja.wikipedia.org/wiki/オブジェクト指向プログラミング "wikilink")をサポートするための改良を加えたものといえる。C++のクラスには、オブジェクト指向言語で一般的な[抽象化](https://ja.wikipedia.org/wiki/抽象化_\(計算機科学\) "wikilink")、[カプセル化](https://ja.wikipedia.org/wiki/カプセル化 "wikilink")、[継承](https://ja.wikipedia.org/wiki/継承_\(プログラミング\) "wikilink")、[多態の](https://ja.wikipedia.org/wiki/ポリモーフィズム "wikilink")4つの機能がある。オブジェクトは実行時に生成されるクラスの実体である。クラスは実行時に生成される様々なオブジェクトのひな形と考えることができる。

なお、C++は[Smalltalk](https://ja.wikipedia.org/wiki/Smalltalk "wikilink")などに見られる[メッセージ転送](https://ja.wikipedia.org/wiki/メッセージ転送 "wikilink")の概念によるオブジェクト指向を採用していない。

#### カプセル化

[カプセル化](https://ja.wikipedia.org/wiki/カプセル化 "wikilink")とは、データ構造を保証し、演算子が意図したとおりに動作し、クラスの利用者が直感的に使い方を理解できるようにするためにデータを隠蔽することである。クラスや関数はC++の基礎的なカプセル化のメカニズムである。クラスのメンバは`public`、`protected`、`private`のいずれかとして宣言され明示的にカプセル化できる。`public`なメンバはどの関数からでもアクセスできる。`private`なメンバはクラスのメンバ関数から、またはクラスが明示的にアクセス権を与えたフレンド関数からアクセスできる。`protected`なメンバはクラスのメンバおよびフレンド関数に加えてその派生クラスのメンバからもアクセスできる。

オブジェクト指向では原則としてクラスのメンバ変数にアクセスする全ての関数はクラスの中にカプセル化されなければならない。C++ではメンバ関数およびフレンド関数によりこれをサポートするが、強制はされない。プログラマはメンバ変数の一部または全体を`public`として定義でき、型とは無関係な変数を`public`な要素として定義できる。このことからC++はオブジェクト指向だけでなく、[モジュール](https://ja.wikipedia.org/wiki/モジュール "wikilink")化のような機能分割のパラダイムもサポートしているといえる。

一般的には、全ての[データ](https://ja.wikipedia.org/wiki/データ "wikilink")を`private`または`protected`にして、クラスのユーザに必要最小限の関数のみを`public`として公開することがよい習慣であると考えられている。このようにしてデータの実装の詳細を隠蔽することにより、設計者はインターフェイスを変更することなく後日実装を根本から変更できる \[19\] \[20\]。

#### 継承

[継承を使うと他のクラスの資産を流用できる](https://ja.wikipedia.org/wiki/継承_\(プログラミング\) "wikilink")。基底クラスからの継承は`public`、`protected`、`private`のいずれかとして宣言する。このアクセス指定子により、派生クラスや全く無関係なクラスが基底クラスの`public`および`protected`メンバにアクセスできるかどうかを決定できる。普通は`public`継承のみがいわゆる*派生*に対応する。残りの二つの継承方法はあまり利用されない。アクセス指定子を省略した場合、[構造体](https://ja.wikipedia.org/wiki/構造体 "wikilink")は`public`継承になるのに対し、クラスでは`private`継承になる。基底クラスを`virtual`として宣言することもできる。これは[仮想継承](https://ja.wikipedia.org/wiki/仮想継承 "wikilink")と呼ばれる。仮想継承は基底クラスのオブジェクトが一つだけ存在することを保証するものであり、多重継承の曖昧さの問題を避けることができる。

**多重継承**はC++の中でもしばしば問題になる機能である。多重継承では複数の基底クラスから一つのクラスを派生できる。これにより継承関係が複雑になる。例えば`FlyingCat`クラスは`Cat`クラスと`FlyingMammal`クラスから派生できる。[Java](https://ja.wikipedia.org/wiki/Java "wikilink")や[C\#では](../Page/C_Sharp.md "wikilink")、基底クラスの数を一つに制限する一方で、複数の[インターフェイスを実装でき](https://ja.wikipedia.org/wiki/インタフェース_\(抽象型\) "wikilink")、これにより制約はあるものの多重継承に近い機能を実現できる（実装の多重継承ではなく型の多重継承）。インターフェイスはクラスと異なり抽象メソッド（純粋仮想関数）を宣言できるのみであり、関数の実装やフィールド（メンバ変数）は定義できない。JavaとC\#のインターフェイスは、C++の抽象基底クラスと呼ばれる純粋仮想関数宣言のみを持つクラスに相当する。JavaやC\#の継承モデルを好むプログラマは、C++において実装の多重継承は使わず、実装の継承は単一継承に絞り、抽象基底クラスによる型の多重継承のみを使うポリシーを採用することもできる。

### 多態

[多態 (ポリモーフィズム)は様々な場面で多用されている機能である](https://ja.wikipedia.org/wiki/ポリモーフィズム "wikilink")。多態により、状況や文脈に応じてオブジェクトに異なる振る舞いをさせることができる。逆に言うと、オブジェクト自身が振る舞いを決定することができる。

C++は**静的な多態**と**動的な多態**の両方をサポートする。コンパイル時に解決される静的な多態は柔軟性に劣るもののパフォーマンス面で有利である。一方、実行時に解決される動的な多態は柔軟性に優れているもののパフォーマンス面で不利である。

#### 静的な多態

関数のオーバーロードは名称が同じ複数の関数を宣言できる機能である。ただし引数は異なっていなければならない。個々の関数は[引数](https://ja.wikipedia.org/wiki/引数 "wikilink")の数や型の順序で区別される。同名の関数はコードの文脈によってどの関数が呼ばれるのかが決まる。関数の戻り値の型で区別することはできない。

関数を宣言する際にプログラマはデフォルト引数を指定できる。関数を呼び出すときに引数を省略した場合はデフォルト引数が適用される。関数を呼び出すときに宣言よりも引数の数が少ない場合は、左から右の順で引数の型が比較され、後半部分にデフォルト引数が適用される。たいていの場合は一つの関数にデフォルト引数を指定するよりも、引数の数が異なる関数をオーバーロードする方が望ましい。

C++のテンプレートでは、より洗練された汎用的な多態を実現できる。特に[Curiously Recurring Template Patternにより仮想関数のオーバーライドをシミュレートした静的な多態を実装できる](https://ja.wikipedia.org/wiki/:en:Curiously_Recurring_Template_Pattern "wikilink")。C++のテンプレートは型安全かつ[チューリング完全](https://ja.wikipedia.org/wiki/チューリング完全 "wikilink")であるため、[テンプレートメタプログラミング](https://ja.wikipedia.org/wiki/テンプレートメタプログラミング "wikilink")によりコンパイラに条件文を再帰的に解決させて実行コードを生成させることにも利用できる。

#### 動的な多態

##### 派生

基底クラスへのポインタおよび参照は、正確に型が一致するオブジェクトだけでなく、その派生クラスのオブジェクトを指すことができる（[リスコフの置換原則](https://ja.wikipedia.org/wiki/リスコフの置換原則 "wikilink")）。これにより、複数の異なる派生型を、同一の基底型で統一的に扱うことが可能となる。また、基底型へのポインタの配列やコンテナは、複数の異なる派生型へのポインタを保持できる。派生オブジェクトから基底オブジェクトへの変換（アップキャスト）では、リスコフの置換原則により、明示的なキャストは必要ない。

`dynamic_cast`は基底オブジェクトから派生オブジェクトへの変換（ダウンキャスト）を実行時に安全に行うための演算子である。この機能は[実行時型情報](https://ja.wikipedia.org/wiki/実行時型情報 "wikilink") (RTTI) に依存している。あるオブジェクトが特定の派生型のオブジェクトであることがあらかじめ分かっている場合は`static_cast`演算子でキャストすることもできる。`static_cast`は純粋にコンパイル時に解決されるため動作が速く、またRTTIを必要としない。また、`static_cast`は従来のC言語形式のキャスト構文と違い継承階層のナビゲーションをサポートするため、多重継承した場合もメモリレイアウトを考慮したダウンキャストを実行することができる。ただし、`static_cast`では多重継承において継承関係を持たない基底型同士のキャスト（クロスキャスト）を実行することはできず、`dynamic_cast`が必要となる。とはいえ、ダウンキャストやクロスキャストが必要となるようなプログラムは、通例設計に問題があることを示しており、本来は仮想関数のオーバーライドによる多態を用いるべきである。

##### 仮想関数

クラスのメンバー関数を`virtual`キーワードで修飾することにより、派生クラスで[オーバーライド](https://ja.wikipedia.org/wiki/オーバーライド "wikilink")（再定義）することが可能な仮想関数 (virtual function) となる。仮想関数は「[メソッド](https://ja.wikipedia.org/wiki/メソッド_\(計算機科学\) "wikilink")」と呼ばれることもある\[21\]。派生クラスにて、基底クラスの仮想関数と名前および引数の数や型の順序が同じ関数を定義することでオーバーライドする（[C++11](https://ja.wikipedia.org/wiki/C++11 "wikilink")以降では、`override`キーワードにより修飾することでオーバーライドを明示することもできる）。基底クラスの仮想関数を派生クラスで[オーバーライド](https://ja.wikipedia.org/wiki/オーバーライド "wikilink")した場合、実際に呼び出される関数はオブジェクトの型によって決定される。基底クラスのポインタのみが与えられた場合、コンパイラはオブジェクトの型をコンパイル時に特定できず正しい関数を呼び出せないため、実行時にこれを特定する。これをダイナミックディスパッチと呼ぶ。仮想関数により、オブジェクトに割り当てられた実際の型に従って、最上位の派生クラスで実装した関数が呼び出される。一般的なC++コンパイラは[仮想関数テーブル](https://ja.wikipedia.org/wiki/仮想関数テーブル "wikilink")を用いる。オブジェクトの型が判明している場合はスコープ解決演算子を利用して仮想関数テーブルを使わないようにバイパスすることもできるが、一般的には実行時に仮想関数の呼び出しを解決するのが普通である。

通常のメンバー関数に加え、オーバーロードした演算子やデストラクタも仮想関数にできる。原則的にはクラスが仮想関数を持つ場合はデストラクタも仮想関数にすべきである。コンストラクタやその延長線上にあるコピーコンストラクタはコンパイルされた時点でオブジェクトの型が確定しないため仮想関数にできない。しかし、派生オブジェクトへのポインタが基底オブジェクトへのポインタとして渡された場合に、そのオブジェクトのコピーを作らなければならない場合は問題が生じる。このような場合は`clone()`関数(またはそれに準じる物)を仮想関数として作成するのが一般的な解決方法である。`clone()`は派生クラスのコピーを生成して返す。

`= 0`をメンバー関数宣言の末尾セミコロンの直前に挿入することにより、メンバー関数を**純粋仮想関数** (pure virtual function) にできる。純粋仮想関数を持つクラスは純粋仮想クラスと呼ばれ、このクラスからオブジェクトを生成することはできない。このような純粋仮想クラスは基底クラスとしてのみ利用できる。派生クラスは純粋仮称関数を継承するため、派生クラスのオブジェクトを生成したい場合は全ての純粋仮想関数をオーバーライドして実装しなければならない。純粋仮想関数を持つクラスのオブジェクトを生成しようと試みるようなプログラムは行儀が悪い。

##### テンプレート

型消去 (type erasure) と呼ばれる、テンプレートを活用して動的な多態性を実現する手法が存在する。この手法はC++の標準ライブラリでも`std::function`や`std::shared_ptr`の削除子で採用されている。いずれも、コンストラクタや代入演算子で（一定の条件を満たす）任意のオブジェクトを実引数として渡せるようにすることから多態性を実現している。

### 単一行コメント

C99の制定前、C言語とC++との分かりやすい差異として、`//` で始まり改行で終わる、**単一行[コメント](https://ja.wikipedia.org/wiki/コメント_\(コンピュータ\) "wikilink")**の有無があった。

単一行コメントはもともと、C言語の祖先にあたる[BCPL](https://ja.wikipedia.org/wiki/BCPL "wikilink")に含まれていた仕様である。現在のC++のコンパイラの多くがC言語のコンパイラとしても使えるようになっているのと同様に、C言語が生まれて間もない頃は、C言語に加え[B言語](https://ja.wikipedia.org/wiki/B言語 "wikilink")やBCPLのコンパイルができるコンパイラが用いられていた。それらコンパイラは、C言語のソースであってもBCPLと同様に単一行コメントが使用できるよう独自の拡張がなされていたため、

現在ではC99の制定によって正式に単一行コメントがサポートされるようになった。

## C++ソースコードの処理とパーサ

[LALR(1)のような旧式のパースアルゴリズムを用いてC](https://ja.wikipedia.org/wiki/LALR法 "wikilink")++の[パーサを記述することは比較的難しい](https://ja.wikipedia.org/wiki/構文解析 "wikilink")\[22\]。その理由の一つはC++の文法がLALRではないことである。このため、コード分析ツールや、高度な修正を行うツール（[リファクタリングツールなど](https://ja.wikipedia.org/wiki/リファクタリング_\(プログラミング\) "wikilink")）は非常に少ない。この問題を取り扱う方法としてLALR(1)でパースできるように改良されたC++の亜種([SPECS](https://ja.wikipedia.org/wiki/:en:Significantly_Prettier_and_Easier_C++_Syntax "wikilink"))を利用する方法がある。[GLRパーサのようにより強力でシンプルなパーサもあるが処理が遅い](https://ja.wikipedia.org/wiki/GLR法 "wikilink")。

パースはC++を処理するツールを作成する際の最も難しい問題ではない。このようなツールはコンパイラと同じように識別子の意味を理解しなければならない。従ってC++を処理する実用的なシステムはソースコードをパースするだけでなく、各識別子の定義を正確に適用し（つまりC++の複雑なスコープのルールを正確に取り扱い）、型を正しく特定できなければならない。

いずれにせよC++ソースコード処理ツールが実用的であるためには、[GNU GCCや](https://ja.wikipedia.org/wiki/GNUコンパイラコレクション "wikilink")[Visual C++で使われているような](https://ja.wikipedia.org/wiki/Microsoft_Visual_C++ "wikilink")、様々なC++の方言を取り扱えなければならず、適切な分析処理やソース変換やソース出力などが実装できなければならない。GLRのような先進的なパースアルゴリズムとシンボルテーブルを組み合わせてソースコードを変換する方法を利用すればあらゆるC++ツールを開発できる。

## 互換性

その言語文法の複雑さゆえ、C++規格に準拠したコンパイラを開発するのは一般的に難しい。20世紀末から何年にも渡りC++に部分的に準拠した様々なコンパイラが作られ、[テンプレートの部分特殊化](https://ja.wikipedia.org/wiki/テンプレートの部分特殊化 "wikilink")などの部分で実装にばらつきがあった。中でも、テンプレートの宣言と実装を分離できるようにするための`export`は問題のキーワードの一つだった。`export`を定義したC++98規格がリリースされてから5年後の2003年前半に[Comeau C/C++が初めて](https://ja.wikipedia.org/wiki/:en:Comeau_C/C++ "wikilink")`export`を実装した。2004年に[Borland C++ Builder Xが](https://ja.wikipedia.org/wiki/C++_Builder "wikilink")`export`を実装した。これらのコンパイラはいずれも[EDGの](https://ja.wikipedia.org/wiki/Edison_Design_Group "wikilink")[フロントエンド](https://ja.wikipedia.org/wiki/フロントエンド "wikilink")をベースにしていた。大半のコンパイラで実装されていない`export`は多くのC++関連書籍（例えば"*Beginning ANSI C++*", Ivor Horton著）にサンプルが記されているが、`export`が記載されていることによる問題は特に指摘されていない。[GCCをはじめとするその他のコンパイラでは全くサポートしていない](https://ja.wikipedia.org/wiki/GNUコンパイラコレクション "wikilink")。[Herb SutterはC](https://ja.wikipedia.org/wiki/:en:Herb_Sutter "wikilink")++の標準規格から`export`を削除することを推奨していたが\[23\]、C++98では最終的にこれを残す決定がなされた\[24\]。結局、C++11では実装の少なさ・困難さを理由に削除された。

コンパイラ開発者の裁量で決められる範囲を確保するため、C++標準化委員会は[名前修飾](https://ja.wikipedia.org/wiki/名前修飾 "wikilink")や[例外処理](https://ja.wikipedia.org/wiki/例外処理 "wikilink")などの実装に依存する機能の実装方法を決定しないことに決めた。この決定の問題は、[コンパイラ](../Page/コンパイラ.md "wikilink")が異なると[オブジェクトファイル](https://ja.wikipedia.org/wiki/オブジェクトファイル "wikilink")の互換性が保証されない点である。特定の機種や[OSでコンパイラの互換性を持たせ](../Page/オペレーティングシステム.md "wikilink")、バイナリレベルでのコード再利用性を高めようとする[ABI](https://ja.wikipedia.org/wiki/Application_Binary_Interface "wikilink")\[25\]のような非標準の規格もあり、一部のコンパイラではこうした準規格を採用している。

2019年現在のメジャーなC++コンパイラ（[gcc](https://ja.wikipedia.org/wiki/GNUコンパイラコレクション "wikilink"), [Clang](https://ja.wikipedia.org/wiki/Clang "wikilink"), [Intel C++ Compiler](https://ja.wikipedia.org/wiki/Intel_C++_Compiler "wikilink"), [Microsoft Visual C++など](https://ja.wikipedia.org/wiki/Microsoft_Visual_C++ "wikilink")）の最新版はC++11およびC++14規格にほぼ準拠しており、特に[Clang](https://ja.wikipedia.org/wiki/Clang "wikilink")は2013年4月時点でC++11の全機能を実装完了した\[26\]\[27\]。ただしマイナーアップデートとなるC++17を含めると、処理系間でのばらつきは依然として存在する。

### C言語との互換性

C++は基本的に[C言語](../Page/C言語.md "wikilink")の上位互換であるが、厳密には異なる\[28\]。C言語で記述された大半のプログラムはC++でコンパイルできるように簡単に修正できるが、C言語では正当でもC++では不正になる部分や、C++とは動作が異なる部分が若干存在する。

例えば、C言語では汎用ポインタ`void*`は他の型へのポインタに暗黙的に変換できるが、C++ではキャスト演算子によって変換を明示する必要がある。またC++では`new`や`class`といった数多くの新しいキーワードが追加されたが、移植の際に元のC言語のプログラムでそれらが識別子（例えば変数名）として使われていると、問題になる。

C言語の標準規格である[C99](https://ja.wikipedia.org/wiki/C99 "wikilink")やその後継[C11ではこうした非互換性の一部が解決されており](https://ja.wikipedia.org/wiki/C11_\(C言語\) "wikilink")、`//`形式のコメントや宣言とコードの混在といったC++の機能がC言語でサポートされている。その一方でC99では、可変長配列、複素数型の組み込み変数、指示初期化子、複合リテラルといった、C++でサポートしていない数多くの新機能が追加された\[29\]。C99で追加された新機能の一部は[C++11](https://ja.wikipedia.org/wiki/C++11 "wikilink")に反映され、次期C++1yに対してもC99やC11との互換性を向上される提案が行われている。また、可変長配列や複素数型などのC99に追加された機能の一部はC11でオプションとなった\[30\]。

C++で書かれた関数をC言語で書かれたプログラムから呼び出す、あるいはその逆を行なう場合など、C言語のコードとC++のコードを混在させるためにはCリンケージを利用する必要があり、関数を`extern "C"`で個別に修飾するか、`extern "C" { ... }`のブロックの中で宣言しなければならない。また、関数引数や戻り値などのインターフェイスはC言語互換形式に合わせる必要がある。Cリンケージを利用した関数については、C++名前修飾がされず、名前修飾に依存している関数オーバーロード機能は利用できない。

C/C++の相互運用性が確保されていることで、慣れ親しんだC言語標準ライブラリ関数の大半をC++でもそのまま利用し続けることができるということはC++の大きなメリットのひとつである。

## 主なC++処理系

  - [Microsoft Visual C++](https://ja.wikipedia.org/wiki/Microsoft_Visual_C++ "wikilink") (MSVC)
  - [C++ Builder](https://ja.wikipedia.org/wiki/C++_Builder "wikilink") ([Borland](https://ja.wikipedia.org/wiki/ボーランド "wikilink") C++ Compiler, BCC)
  - [g++](https://ja.wikipedia.org/wiki/GNUコンパイラコレクション "wikilink")
  - [Intel C++ Compiler](https://ja.wikipedia.org/wiki/Intel_C++_Compiler "wikilink") (ICC/ICL)
  - [Clang](https://ja.wikipedia.org/wiki/Clang "wikilink")

## 脚注

## 参考文献

  -
  -
  -
## 関連項目

  - [C++11](https://ja.wikipedia.org/wiki/C++11 "wikilink") (C++0x)
  - [C++14](https://ja.wikipedia.org/wiki/C++14 "wikilink")
  - [C++17](https://ja.wikipedia.org/wiki/C++17 "wikilink")
  - [C++/CLI](https://ja.wikipedia.org/wiki/C++/CLI "wikilink")
  - [Embedded C++](https://ja.wikipedia.org/wiki/Embedded_C++ "wikilink")
  - [JavaとC++の比較](https://ja.wikipedia.org/wiki/JavaとC++の比較 "wikilink")
  - [SystemC](https://ja.wikipedia.org/wiki/SystemC "wikilink") - C++言語ベースのハードウェア記述言語
  - [テンプレートメタプログラミング](https://ja.wikipedia.org/wiki/テンプレートメタプログラミング "wikilink")
  - [キーワード (C++)](https://ja.wikipedia.org/wiki/キーワード_\(C++\) "wikilink")

## 外部リンク

  - [Standard C++ Foundation](https://isocpp.org/)

[Category:C++](https://ja.wikipedia.org/wiki/Category:C++ "wikilink") [Category:オブジェクト指向言語](https://ja.wikipedia.org/wiki/Category:オブジェクト指向言語 "wikilink") [Category:JIS](https://ja.wikipedia.org/wiki/Category:JIS "wikilink")

1.  『プログラミング言語C++』第4版、pp.12-13。
2.  『C++の設計と進化』、pp.152-153。
3.  『プログラミング言語C++』第4版、p.11。
4.
5.
6.
7.  [ISO/IEC 14882:1998](http://www.iso.org/iso/iso_catalogue/catalogue_ics/catalogue_detail_ics.htm?csnumber=25845&ICS1=35&ICS2=60)
8.  [ISO/IEC 14882:2003](http://www.iso.org/iso/iso_catalogue/catalogue_ics/catalogue_detail_ics.htm?ics1=35&ics2=60&ics3=&csnumber=38110)
9.  [ISO/IEC TR 19768:2007](http://www.iso.org/iso/iso_catalogue/catalogue_ics/catalogue_detail_ics.htm?ics1=35&ics2=60&ics3=&csnumber=43289)
10. [ISO/IEC 14882:2011](http://www.iso.org/iso/iso_catalogue/catalogue_ics/catalogue_detail_ics.htm?ics1=35&ics2=60&ics3=&csnumber=50372)
11. [ISO/IEC 14882:2014](http://www.iso.org/iso/home/store/catalogue_tc/catalogue_detail.htm?csnumber=64029)
12. <https://www.iso.org/standard/68564.html>
13. [We have C++14\! : Standard C++](http://isocpp.org/blog/2014/08/we-have-cpp14)
14.
15.
16. 『C++の設計と進化』、pp.124-125。
17.
18. [Open issues for The C++ Programming Language (3rd Edition)](http://www.research.att.com/~bs/3rd_issues.html) - このコードはストロヴストルップ自身による訂正文からの引用(633ページ)。`std::endl`を`'\n'`に改めている。また`main`関数がデフォルトで0を返す件については[www.research.att.com](http://www.research.att.com/~bs/bs_faq2.html#void-main)及び[www.delorie.com/djgpp/](http://www.delorie.com/djgpp/v2faq/faq22_25.html) を参照されたし。このデフォルト仕様は`main`関数のみであり他の関数にはない。
19. {{ cite book | first1 = Herb | last1 = Sutter | first2 = Andrei | last2 = Alexandrescu | authorlink1 = Herb Sutter | authorlink2 = Andrei Alexandrescu | date = 2004 | title = C++ Coding Standards: 101 Rules, Guidelines, and Best Practices | publisher = Addison-Wesley }}
20.
21.
22.
23.
24.
25.
26.
27.
28.
29.
30. [C言語の最新事情を知る： C99の仕様 - Build Insider](http://www.buildinsider.net/small/clang/01)
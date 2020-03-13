> この記事は[Hot Soup Processor](https://ja.wikipedia.org/wiki/Hot_Soup_Processor)から翻訳されています。


**Hot Soup Processor**（ホットスーププロセッサー）は、[1995年](https://ja.wikipedia.org/wiki/1995年 "wikilink")から[おにたま](https://ja.wikipedia.org/wiki/おにたま "wikilink")により開発されている[プログラミングツール](https://ja.wikipedia.org/wiki/プログラミングツール "wikilink")、およびその[プログラミング言語](../Page/プログラミング言語.md "wikilink")である。略称は**HSP**。最新安定バージョンは**3.5**。

## 歴史

### 誕生とHSP2登場

1994年にHSPの前身となる**[](http://www.vector.co.jp/soft/dos/art/se007721.html)**（LSP）が[PC-9800シリーズ](../Page/PC-9800シリーズ.md "wikilink")で開発された。名前の  は「」が由来である\[1\]。言語仕様は米[ダートマス大学](../Page/ダートマス大学.md "wikilink")で開発された  言語の書式に基づいているが、 との互換性はない。

1995年より [{{lang](../Page/Microsoft_Windows_3.x.md "wikilink") で動作するHSP1.0の開発が開始され\[2\]、1996年に[フリーウェア](../Page/フリーウェア.md "wikilink")として一般に公開された。開発した経緯について、おにたまは『自分にとって必要だから作った、いわば中間生成物的ソフトなのです。』と述べている\[3\]。

1997年にHSP2.0が登場し、[{{lang](../Page/Microsoft_Windows_95.md "wikilink") 以降で動作する[32ビットアプリケーション](https://ja.wikipedia.org/wiki/32ビットアプリケーション "wikilink")となった。[定数](../Page/定数.md "wikilink")や文字列型の変数に対応したほか、後のバージョンアップで3D描画機能をサポートした。1999年に「 賞」、2001年に「[オンラインソフトウェア大賞2001](../Page/フリーソフトウェア大賞.md "wikilink")」をそれぞれ受賞した。2005年には日本の[経済産業省](../Page/経済産業省.md "wikilink")が支援する「ITクラフトマンシップ・プロジェクト」にHSPを取り入れた教育・研修が採択された\[4\]\[5\]。なお、HSP2.61は [{{lang](https://ja.wikipedia.org/wiki/Microsoft_Visual_Studio "wikilink") を使用して開発し[コンパイル](https://ja.wikipedia.org/wiki/コンパイル "wikilink")されていた\[6\]。

### HSP3の登場

2005年[8月1日](../Page/8月1日.md "wikilink")にHSP3.0が登場。OSは[Windows 98以降が必要になった](../Page/Microsoft_Windows_98.md "wikilink")。文法体系の見直し、Windowsプラットフォームへの親和性の向上などが行われ、一部が従来のHSP2.x系と互換性のない書式に変更された。（詳細は[\#言語仕様](https://ja.wikipedia.org/wiki/#言語仕様 "wikilink")参照）

HSP3.0のリリースから2年後にあたる[2007年](../Page/2007年.md "wikilink")[8月1日](../Page/8月1日.md "wikilink")にHSP3.1が登場、HSPスクリプトエディタの機能改善や、新規のプラグイン・モジュールなどの追加、Peasエディタやかんたん入力機能によるスクリプト入力補助、[Java](https://ja.wikipedia.org/wiki/Java "wikilink")ランタイム上でHSPを動作させるための[HSPLet](https://ja.wikipedia.org/wiki/HSPLet "wikilink")の標準サポート、ライセンス形式の改定（[BSDライセンス](../Page/BSDライセンス.md "wikilink")）による[仕様やソースコードのオープン化](http://www.onionsoft.net/hsp/openhsp/)が行われた。

[2011年](../Page/2011年.md "wikilink")[9月13日](../Page/9月13日.md "wikilink")に登場したHSP3.3では、[HSPDish](http://hsp.tv/make/hsp3dish.html)というランタイムパッケージが供給されており、変換によって[iOSや](https://ja.wikipedia.org/wiki/iOS_\(アップル\) "wikilink")[Android](../Page/Android.md "wikilink")上でプログラムを実行させることができるようになった。また、HSP3のコードを他のソースに変換するためのツールとしてhsp3cnvが同梱され、公式に[C++](../Page/C++.md "wikilink")へのコード変換が可能になった。

HSP3の登場から新ポータルサイトHSPTV\!が立ち上がりHSP3ユーザーのコミュニケーションの場として提供されている。またHSPTV\!で同サイトの[CGI](https://ja.wikipedia.org/wiki/CGI "wikilink")プログラマを募集するなどの取り組みも試みられている\[7\]。 [2003年](../Page/2003年.md "wikilink")からは毎年[HSPプログラムコンテスト](../Page/HSPプログラムコンテスト.md "wikilink")が開催されており、2013年のコンテストでは「[ニコニコ自作ゲームフェス2](../Page/ニコニコ動画.md "wikilink")」との作品の相互提供が行われている。

## 特徴

HSPは[手続き型言語](https://ja.wikipedia.org/wiki/手続き型言語 "wikilink")であり、[中間言語系](https://ja.wikipedia.org/wiki/中間言語#コンピュータのプログラムにおける中間言語 "wikilink")[インタープリタ](https://ja.wikipedia.org/wiki/インタープリタ "wikilink")のプログラミングツールとして設計されている。公式に『子供でも理解し易いプログラム言語』を掲げており\[8\]、低年齢（例えば小学生）向けの解説書も出版されている。

ユーザーがスクリプトの記述や開発環境の設定を行うことなく、自動的に[ウィンドウ](../Page/ウィンドウ.md "wikilink")の作成や制御が行われる。コンソール版HSP（HSPCL）を用いれば、[コマンドプロンプト上で実行するプログラムも開発できる](https://ja.wikipedia.org/wiki/cmd.exe "wikilink")。スクリプトの最後の行が終わるとその時点で実行が停止し、自動的にプログラムが終了しない。

Windowsでの使用を前提としているが、公式に[Mac OSへの移植した](https://ja.wikipedia.org/wiki/Mac_OS "wikilink")[HSP/Mac](http://quasiquote.org/hspwiki/HSP/Mac%E9%96%A2%E9%80%A3)も存在する。有志によって非公式的に[Linux](../Page/Linux.md "wikilink")にも移植されているが、移植版の場合はWindows版より古いバージョンがベースになっている。ただし、2018年4月1日に、正式に[Raspberry PiやLinux対応を謳う](https://ja.wikipedia.org/wiki/Raspberry_Pi "wikilink")、**[HSP3 for Linux/Raspberry Pi](https://github.com/onitama/OpenHSP)**が公開され、今後はWindows版もこちらに準拠する旨アナウンスされている。

### 言語仕様の特徴

HSP3.xの（ユーザーが実際に入力する）言語仕様に関する主な特徴として、以下のように挙げられる。

  - [BASIC](../Page/BASIC.md "wikilink")と似た構文を別名として利用できる。
  - [行番号](../Page/行番号.md "wikilink")は利用しない（できない）。
  - [構文](https://ja.wikipedia.org/wiki/構文 "wikilink")の大文字・小文字を区別しない。
  - [変数の使用に事前の定義が必要ない](../Page/変数_\(プログラミング\).md "wikilink")（自動的に[グローバル変数](../Page/グローバル変数.md "wikilink")またはモジュール内定義変数として確保される）。
  - 変数・ラベルはモジュールという他と隔離された[名前空間](../Page/名前空間.md "wikilink")で分離することができる。
  - 変数名に日本語（[2バイト文字](../Page/マルチバイト文字.md "wikilink")）を利用できる。
  - [ラベル](../Page/ラベル.md "wikilink")を使用した[サブルーチン](../Page/サブルーチン.md "wikilink")の別個記述が可能である。
  - [DLLをプラグインとして利用することができ](../Page/ダイナミックリンクライブラリ.md "wikilink")、それによってWindowsのさまざまな機能を利用することが出来る。[DirectX](https://ja.wikipedia.org/wiki/DirectX "wikilink")や[OpenGL](../Page/OpenGL.md "wikilink")などの3Dグラフィックスを扱うものもある。
  - [プリプロセッサ](../Page/プリプロセッサ.md "wikilink")を持つ。
  - COMオブジェクトに対応している。

## 開発環境

### スクリプトエディタ

HSPには専用の[スクリプトエディタ](../Page/スクリプトエディタ.md "wikilink")が付属している。一般的な[テキストエディタ](../Page/テキストエディタ.md "wikilink")の機能を有しているほか、[コンパイル](https://ja.wikipedia.org/wiki/コンパイル "wikilink")や外部ツールの呼び出しなど独自の機能も備える。複数のファイルを参照・編集する場合、同一のウインドウ内に[タブを用いて表示](../Page/タブ_\(GUI\).md "wikilink")・切り替えできる。[プロジェクトファイル](https://ja.wikipedia.org/wiki/プロジェクトファイル "wikilink")の概念は無い。エディタのエンジンには[Footy](https://ja.wikipedia.org/wiki/Footy "wikilink")が使用されている。

[EXE形式で出力できるが](../Page/EXEフォーマット.md "wikilink")、ファイルのアイコン変更は「\[<http://lhsp.s206.xrea.com/works/hsp.html#lhspic>　Let's HSPIC\!\]」や「[Sato Icon Changer](https://ja.wikipedia.org/wiki/Sato_Icon_Changer "wikilink")」等の専用のソフトウェアが必要となる。また、HSP3.5以降(正確には3.5 beta6から)では標準でアイコン書き換え機能が追加され、\#packopt命令を利用することによりアイコンを変更できるようになった。\[9\]

現在の最新バージョンであるHSP3.XのリソースはHSP2.Xのリソースとも共通規格でないため、一般的なリソースエディタはもちろんのこと、前記のソフトウェア以外のHSP2.X用に作成された変更ソフトではファイルが壊れてしまう。

コンパイルを行うツールを利用すれば外部エディタでの開発も可能である。

### Peasエディタ

パーツ（要素）と呼ばれるものをマウスで配置し配線することで、自動的にHSPのスクリプトを生成するための[オーサリングツール](../Page/オーサリングツール.md "wikilink")である。HSP3.1より同梱された。

今までプログラミングに触れてこなかった人や、初心者にとっての新しい選択肢となるものの、すべての作業をPeasエディタで行なうことは想定していないとしている\[10\]。

なお、パーツはユーザー自身で制作することも可能である。

### HSP Document Library（HDL）

HSPに同梱された関連ドキュメントを検索・観覧するための専用[ブラウザ](https://ja.wikipedia.org/wiki/ブラウザ "wikilink")である。ソフトウェア本体はsprocketが開発している。HSP3.0から**HSP HELP Browser**として標準で同梱され、HSP3.2より同名称になった。

ドキュメントやサンプルスクリプトを検索し、表示することができる。ユーザー自身で新たなドキュメントを追加することが可能で、独自形式のドキュメントファイルを編集・作成するエディタが付属している。

## 言語仕様

### 主な構文

以下の表はHSP1.x系とHSP2.x系とHSP3.x系との違いである。

| 項目    | HSP1.x系        | HSP2.x系                | HSP3.x系                                               |
| ----- | -------------- | ---------------------- | ----------------------------------------------------- |
| 定数    | 未対応            | 整数、文字列                 | 整数、文字列、実数                                             |
| 変数の型  | 整数型            | 整数型、文字列型               | 整数型、文字列型、実数型、comobj型、モジュール変数(struct)型、ラベル型、拡張型        |
| 式の評価  | 演算子の優先度なし、左方優先 | 演算子の優先度なし、左方優先         | 演算子の優先度あり                                             |
| 代入演算子 | 未対応            | `+=`, `-=`, `++`, `--` | `+=`, `-=`, `++`, `--`のほか `*=`, `/=` 等、ほぼすべての代入演算子に対応 |
| 関数    | 未対応            | 未対応                    | 対応（標準関数、ユーザー定義関数、拡張関数）                                |
| マクロ   | 未対応            | 仮対応                    | 対応                                                    |
|       |                |                        |                                                       |

HSP3.x系では、関数のサポートなど一部が従来のHSP2.x系と互換性のない書式に変更された。これは添付されている互換マクロを利用することで、（関数を\#undefとマクロにより命令風に置き換えるなど）一部は擬似的に互換を取ることが可能である。現在は未対応なものの今後、2.x系と同様、演算子の優先度などに関係なく左優先方式にも対応する予定である。ただし、新しく作成する場合はスクリプトの見やすさの面や他の言語との相互互換性,将来性などのこともあり新方式（関数などを利用した方式）で作成することが推奨されている。

HSP1.x系とHSP2.x系では命令中のラベル名にラベル名であることを明示するアスタリスクが省略できる、変数名やラベル名などに半角英数字以外に全角文字が使用できたりといくつかの仕様上の欠陥がある。HSP3.x系ではラベルのアスタリスク省略はできないように修正されている。システム変数はHSP3.x系で一部廃止され、関数やマクロに置き換わっている。HSP3.x系では拡張プラグインにより様々な構文（変数/命令/関数/システム変数など）を拡張できる。ただし、HSP3.0時点では定数の拡張はできない。

### 命令リスト

これは、HSPで使う命令の一例である。

| 命令        | 意味                                                                                                                |
| --------- | ----------------------------------------------------------------------------------------------------------------- |
| `mes`     | 文字列を表示する                                                                                                          |
| `button`  | 押しボタンを表示する。押された場合、指定されたラベルにジャンプする。                                                                                |
| `input`   | 入力ボックスを表示する                                                                                                       |
| `pos`     | 表示位置を指定する                                                                                                         |
| `picload` | 画像を表示する(ver3.31ベータ版よりも前のバージョンの場合、[PNG形式は](../Page/Portable_Network_Graphics.md "wikilink")`imgload`という拡張命令と  が必要) |
| `color`   | 色指定（[RGB](../Page/RGB.md "wikilink")形式で、各要素0～255、十進法で指定）                                                          |
| `if`      | |もし～ならば～する（[分岐命令](../Page/分岐命令.md "wikilink")）                                                                    |
| `font`    | 文字列の大きさ・[フォント](../Page/フォント.md "wikilink")を指定する                                                                   |
| `boxf`    | 矩形を描画する                                                                                                           |
| `repeat`  | `repeat`～`loop`間の処理を指定回数繰り返す                                                                                      |
| `loop`    |                                                                                                                   |
| `goto`    | 指定したラベルにジャンプする                                                                                                    |
| `gosub`   | 指定したラベルに行き、`return` があると元の `gosub` の次の行へ戻って実行                                                                     |
| `return`  |                                                                                                                   |
| `end`     | プログラムを終了する                                                                                                        |
| `stop`    | プログラムの実行を一時的に中断する                                                                                                 |
| `title`   | タイトルバーに表示する文字列を指定する                                                                                               |
| `screen`  | 大きさ、位置などを指定してスクリーンを作る（`bgscr`命令で枠なしスクリーンも可能）                                                                      |

一般的な通常命令

### 外部APIとの連携

HSP は外部[DLL](https://ja.wikipedia.org/wiki/DLL "wikilink")ライブラリや[Windows APIとの連携にも対応している](../Page/Windows_API.md "wikilink")。

それぞれ[プリプロセッサ](../Page/プリプロセッサ.md "wikilink")を使用することで、[Windows](https://ja.wikipedia.org/wiki/Windows "wikilink")のコモンコントロールを使用することができる。 また、それらのコントロールを最初から使用できるようにするモジュールスクリプトもHSP パッケージに標準で同梱されている。

## サンプルプログラム

  - 最も一般的な[Hello worldプログラム](../Page/Hello_world.md "wikilink")

<!-- end list -->

    mes "Hello,World!"

HSPの基本的な構文は、「命令」+「パラメータ」である。命令とパラメータの間には半角スペースが必要である。パラメータが複数必要な場合、それぞれを「,」で区切る。このプログラムで使われているmes命令はパラメータがひとつしか無いため、「,」は必要ない(「"」で囲まれた部分は文字列として認識されるため、この場合の「,」は文字列の一部である)。プログラムの最後になるとプログラムが停止するので、stop命令は必要ない。

  - ダイアログプログラム

<!-- end list -->

    dialog "びっくりマークが表示されます", 1, "てすと"

dialog命令は、1つ目のパラメータが本文、3つ目のパラメータがタイトルに相当する。2つ目のパラメータはダイアログの種類であり、0は情報の「i」、1は警告の「\!」、2と3はそれぞれ「はい」か「いいえ」を選ぶダイアログになる。HSPではこれを表示している間プログラムが停止する。

  - 変数を使った表示

<!-- end list -->

    a=10
    b="HSP"
    mes "変数aの内容は"+ a +"です。"
    mes a +"です。"
    dialog "サンプルスクリプト", 0, b

文字列の後に、数値を代入した変数を連結させると、そのまま数値が文字列となって表示される。逆に最初に数値が代入された変数を使用した後文字列を連結させると、文字列は表示されない(先に出現した型に強制変更されるため)。また変数の使用の定義が不要のため、このスクリプトをそのまま実行すればエラーは起こらない(dimやsdimなどの初期化命令も有り)。

## その他

一部バージョンにおいて、[アンチウィルス製品で](../Page/アンチウイルスソフトウェア.md "wikilink")[マルウェア](../Page/マルウェア.md "wikilink")と誤認識される現象が報告されている\[11\]\[12\]。

## 出典

## 関連書籍

  - 『はじめてのHSP』 工学社 ISBN 4-87593-289-8
  - 『HSPゲームプログラミング クックブック 2.6』 秀和システム ISBN 4-7980-0495-2
  - 『HSPプログラミング入門 2.55』 秀和システム ISBN 4-7980-0209-7
  - 『HSPプログラミング入門 2.6』 秀和システム ISBN 4-7980-0821-4
  - 『最新HSP3.2プログラミング入門』 秀和システム ISBN 978-4-7980-2432-5
  - 『HSPスクリプトプログラミング逆引きテクニック 2.55』 秀和システム ISBN 4-7980-0186-4
  - 『無料ツールでゲームプログラミング HSP編』 エンターブレイン ISBN 4-7577-1863-2
  - 『12歳からはじめる、わくわくHSPゲームプログラミング教室』 ラトルズ ISBN 4-89977-078-2

## 関連項目

  - [BASIC](../Page/BASIC.md "wikilink")
  - [C言語](../Page/C言語.md "wikilink")
  - [HSPプログラムコンテスト](../Page/HSPプログラムコンテスト.md "wikilink")
  - [3DACE](https://ja.wikipedia.org/wiki/3DACE "wikilink")

## 外部リンク

  - [Hot Soup Processor公式サイト](http://hsp.tv/)
  - [HSPプログラムコンテスト](http://hsp.tv/play/contest.html)
  - [OpenHSP](http://www.onionsoft.net/hsp/openhsp/)（オープンソース化されたHSPのWiki）
  - [GitHubでのリポジトリ](https://github.com/onitama/OpenHSP) （Linux版OpenHSPのソースコードの公開場所）
  - [びんずめ堂](http://www.binzume.net/)（Linux版HSP(xhsp)がダウンロードできる）
  - [Let's HSP\!](http://lhsp.s206.xrea.com/)
  - [CuteHSP](https://github.com/kikeroga3/tinyhsp)（HSPの命令仕様をもとにしたクロスプラットフォームなトイ言語）

[Category:プログラミング言語](https://ja.wikipedia.org/wiki/Category:プログラミング言語 "wikilink") [Category:フリーウェア](https://ja.wikipedia.org/wiki/Category:フリーウェア "wikilink") [Category:1995年のソフトウェア](https://ja.wikipedia.org/wiki/Category:1995年のソフトウェア "wikilink")

1.  『逆引き　HSP3 プログラミング事典［基本編］』 工学社 p27 ISBN 4-7775-1226-6
2.  [ とは?](http://www.onionsoft.net/about.html)
3.  [窓の杜 - 【このソフト作った人はどんな人？】 第3回：「」の作者、おにたまさん](http://www.forest.impress.co.jp/article/2002/01/17/whocreate3.html) (2002年1月17日）
4.  [平成17年度「ITクラフトマンシップ・プロジェクト」選定結果について](http://warp.da.ndl.go.jp/info:ndljp/pid/1368617/www.meti.go.jp/press/20050711002/050711it.pdf)
5.  [平成17年度ITクラフトマンシップ・プロジェクト採択事業「スーパープログラマーを育てよう！」プロジェクト事業報告 特定非営利活動法人OCP総合研究所](http://npo-ocp.jp/image/h17_craftsman_report.pdf)
6.  説明書「著作権、ライセンスについて」を参照（HSP2.61時点）
7.  [HSPTV\!システムプログラマー募集](http://hsp.tv/recruit.html)
8.  [教育関係者・保護者の皆様へ](http://hsp.tv/info/parent.html)
9.
10. Peasエディタマニュアル参照（HSP3.3時点）
11. [HSP ver2.61に対するウィルス誤認識について](http://www.onionsoft.net/hsp/hsp2alert.html)
12. [HSP ver3.1、ver3.2に対するウィルス誤認識について](http://www.onionsoft.net/hsp/hsp3alert.html)
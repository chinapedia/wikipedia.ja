> この記事は[TeX](https://ja.wikipedia.org/wiki/TeX)から翻訳されています。


****（TeX）は、[ドナルド・クヌース](../Page/ドナルド・クヌース.md "wikilink") (Donald E. Knuth) が開発し、広く有志による拡張などが続けられている[組版](../Page/組版.md "wikilink")処理システムである。

## 概要

[ドナルド・クヌース](../Page/ドナルド・クヌース.md "wikilink")が、1976年に自身の著書 *[The Art of Computer Programming](../Page/The_Art_of_Computer_Programming.md "wikilink")* の改訂版の準備中に、[鉛版](../Page/鉛版.md "wikilink")により[組版](../Page/組版.md "wikilink")された ([:en:Hot metal typesetting](https://ja.wikipedia.org/wiki/:en:Hot_metal_typesetting "wikilink")) 旧版の職人仕事による美しさが、改訂版の当時の[写植では再現できていないことに憤慨し](https://ja.wikipedia.org/wiki/写真植字 "wikilink")、自分自身が心ゆくまで組版を制御するために開発を決意した。

クヌースはまず、伝統的な組版およびその関連技術に対する広範囲にわたる調査を行い、その調査結果を取り入れることで、商業品質の組版ができる、柔軟で強力な組版システムを開発した。それは技術と同時に芸術をも意味する言葉である、（テクネ）から採られ“”と名付けられた。

当初の開発は本業である研究や教育の合間仕事であったが、クヌースには1978年に1年間の[サバティカル](https://ja.wikipedia.org/wiki/サバティカル "wikilink")があったことから、その1年間の全てをこれに集中して完成させるという見込みであった。しかし実際には、同年に初版をリリースしたものの、その後も改訂を続けることとなった。最終的に、後述する「完成版」の系列であるバージョン3の最初のリリースは、実に1989年のことであった。 [thumb入](https://ja.wikipedia.org/wiki/画像:knuth-check2.png "wikilink")）\]\] を他人が改造したり拡張したりした場合について、それを直接配布することをクヌースは許しておらず、**change file** というメカニズムを利用して差分を添付する、という形で行わなければならない（これは当時まだ diff と patch が一般的に広く使われていなかったことから、これもクヌースが開発したものである）。この制限はいわゆる「[バザールモデル](../Page/伽藍とバザール.md "wikilink")」であるとは多少言い難い所があるが、「[オープンソースの定義](https://ja.wikipedia.org/wiki/オープンソースの定義 "wikilink")」では（そのような制限との妥協の産物である）第4項により、差分等を添付した再配布を許しているならば、派生物の配布にそのような制限があってもよい、ということになっているため「オープンソースの定義」には合致している。

前述のような開発期間の長さの理由のひとつに、クヌースが徹底的にバグを探して潰していたから、ということも挙げられる。どのようなバグを修正したか、ということも記録しており、ある時期までのものについて解説と一覧が『文芸的プログラミング』の第10章と第11章に収録されている。そのため、残っているバグは少ないだろうとして、ジョーク好きのクヌースが、バグ発見者に対しては前回のバグ発見者の2倍の[懸賞金](https://ja.wikipedia.org/wiki/懸賞金 "wikilink")を掛けている。この賞金は[小切手](../Page/小切手.md "wikilink")（[クヌース賞金小切手](https://ja.wikipedia.org/wiki/クヌース賞金小切手 "wikilink")）で払われるが、貰っても記念に取っておくばかりなので、結局クヌースの出費はほとんどないという（とはいえやはりジョークかもしれないが、やめておけば良かった、というように取れることも書いている）。

クヌースは  のバージョン 3 を開発した際に、これ以上の機能拡張はしないことを宣言した。その後は不具合の修正のみがなされ、バージョン番号は 3.14, 3.141, 3.1415, … というように付けられている。これは更新の度に値が[円周率](https://ja.wikipedia.org/wiki/円周率 "wikilink")に近づいていくようになっていて、クヌースの死の時点をもってバージョン  として、バージョンアップを打ち切るとのことである\[1\]。

クヌースは  の開発と同時に、 で利用する[フォント](../Page/フォント.md "wikilink")を作成するためのシステムである [METAFONT](../Page/METAFONT.md "wikilink") も開発した。こちらのバージョン番号は 2.71, 2.718, 2.7182, … というように、更新の度に値が[ネイピア数](../Page/ネイピア数.md "wikilink")に近づいていくようになっている\[2\]。さらにクヌースは METAFONT を使って、欧文フォント [Computer Modern](https://ja.wikipedia.org/wiki/Computer_Modern "wikilink") も設計（デザイン）した。Computer Modern（cmと略されることもある）にはクヌース自身の欧文フォントに対する美的感覚が反映され、全くのプレーンな  ではデフォルトのフォントであるが、現在の多くの利用者は Times など伝統的な定番フォントを使うよう設定していることも多い。

および METAFONT はまた、同様にクヌース自身が提唱する[文芸的プログラミング](../Page/文芸的プログラミング.md "wikilink") (Literate Programming) の「ドキュメンテーションを主とし、コードはそれに付随する」スタイルによる大規模なプロジェクトの一例でもある。やはりクヌースによる文芸的プログラミングのためのシステム [WEB](../Page/WEB.md "wikilink") の tangle により、そのようにして書かれている文芸的な「プログラム」の中から [Pascal](../Page/Pascal.md "wikilink") で書かれているコード部分が取り出され、[コンパイル](https://ja.wikipedia.org/wiki/コンパイル "wikilink")できるように編集し直されて何らかの Pascal の実装により処理される（大規模なコードのため、多くの Pascal 実装において1個以上のバグを見つけている、ともいわれる）。同様にして WEB の weave を通して得られるドキュメントを書籍にしたものが book と METAFONTbook である。Pascal が使われているのは開発にとりかかったのが古く、[C言語](../Page/C言語.md "wikilink")が広く一般的になるより前だったこともあるが、近年ではC言語をターゲットとした WEB である WEB2C が使われることも多い。

## 名称について

製作者の[ドナルド・クヌース](../Page/ドナルド・クヌース.md "wikilink")により以下のように要請されている。

### 表記

[middle](https://ja.wikipedia.org/wiki/画像:TeX_logo.svg "wikilink") は 「技術、芸術」に由来し、[ギリシア文字](../Page/ギリシア文字.md "wikilink")の [Τ](../Page/Τ.md "wikilink")（タウ）- [Ε](../Page/Ε.md "wikilink")（イプシロン）- [Χ](../Page/Χ.md "wikilink")（カイ）である。E を少し下げて、字間を詰めて書く。[プレーンテキスト](../Page/プレーンテキスト.md "wikilink")などそれができない場合には “**TeX**” と表記する（“TEX”や“Tex”と表記するのは誤り）。

### 読み方

英語の[アルファベット](https://ja.wikipedia.org/wiki/アルファベット "wikilink") （エックス、）として読むのではなく、[ギリシア語](https://ja.wikipedia.org/wiki/ギリシア語 "wikilink")風に[無声軟口蓋摩擦音](../Page/無声軟口蓋摩擦音.md "wikilink") （ドイツ語の [ach-laut](../Page/ドイツ語音韻論.md "wikilink") の ）で /tex/ と発音するのが本来である。*book* では、そのように正しく発音するとコンピュータの端末（のCRTディスプレイ）が、呼気でちょっと曇る、と冗談が書かれている。英語においては、多くの方言で音素  が存在せず代わりに  が使われること、 に由来する が  と読むことから  と読まれる。ドイツ語では  が[前舌母音](https://ja.wikipedia.org/wiki/前舌母音 "wikilink")であることから [ich-laut](../Page/ドイツ語音韻論.md "wikilink") の発音になり、 である。日本ではどれもカタカナで表現するのが難しいため「テック」ないし「テフ」と書かれる。ドイツ語の  をハ行で表現することもあるので間違いとは言い切れないものの、あえてローマ字で書くなら  であり、日本語の「ファ行のフ」である[無声両唇摩擦音](../Page/無声両唇摩擦音.md "wikilink") （ローマ字で ）ではない\[3\]。

## 機能

は[マークアップ言語](../Page/マークアップ言語.md "wikilink")のスタイルをとっている。すなわち、文章そのもの（テキスト）と文章の構造を指定する命令（コントロールシーケンス）が記述された[テキストファイル](../Page/テキストファイル.md "wikilink")を読み込み、そこに書かれた命令により文章を[組版](../Page/組版.md "wikilink")し、組版結果を [DVI](https://ja.wikipedia.org/wiki/DVI_\(ファイルフォーマット\) "wikilink") 形式のファイルに書き出す。DVI 形式とは、装置に依存しない (**d**e**v**ice-**i**ndependent) 中間形式のことである。処理系は多機能で、[チューリング完全](../Page/チューリング完全.md "wikilink")である。

DVIファイルには紙面のどの位置にどの文字を配置するかといった情報が書き込まれている。実際に紙に印刷したりディスプレイ上に表示したりするためには、DVI ファイルを解釈する別のソフトウェアが用いられる。DVI ファイルを扱うソフトウェアとして、各種のビューワや [PostScript](../Page/PostScript.md "wikilink") など他のページ記述言語へのトランスレータ、プリンタ[ドライバなどが利用されている](../Page/デバイスドライバ.md "wikilink")。

組版処理については、行分割およびページ分割位置の判別、[ハイフネーション](../Page/ハイフン.md "wikilink")、[リガチャ](../Page/合字.md "wikilink")、および[カーニング](https://ja.wikipedia.org/wiki/カーニング "wikilink")などを自動で処理でき、その自動処理の内容も種々のパラメータを変更することによりカスタマイズできる。数式組版についても、多くの機能が盛り込まれている。 が文字などを配置する分解能は （約 5.363 [nm](../Page/ナノメートル.md "wikilink")、4,736,286.72 [dpi](https://ja.wikipedia.org/wiki/dpi "wikilink")）である。

の扱う命令文の中には、組版に直接係わる命令文の他に、新しい命令文を定義するための命令文もある。こうした命令文は[マクロと呼ばれ](../Page/マクロ_\(コンピュータ用語\).md "wikilink")、 ユーザー独自の改良により、種々のマクロパッケージが配布されている。

比較的よく知られている  上のマクロパッケージには、クヌース自身による plain 、一般的な文書記述に優れた [](../Page/LaTeX.md "wikilink")、数学的文書用の [](https://ja.wikipedia.org/wiki/AmS-TeX "wikilink") などがある。一般の使用者は、 を直接使うよりも、 に何らかのマクロパッケージを読み込ませたものを使うことの方が多い。

の用途を拡張したマクロパッケージとして、他に次のようなものがある。

  - [](../Page/BibTeX.md "wikilink") - [参考文献](../Page/参考文献.md "wikilink")リストの作成に用いる。
  - [](https://ja.wikipedia.org/wiki/SLiTeX "wikilink") - [プレゼンテーション](../Page/プレゼンテーション.md "wikilink")用[スライドの作成に用いる](../Page/スライド_\(写真\).md "wikilink")\[4\]。
  - [](https://ja.wikipedia.org/wiki/AMS-LaTeX "wikilink") - 数学的な文書の記述に強い [](https://ja.wikipedia.org/wiki/AmS-TeX "wikilink") の機能と  の機能を併せ持つ\[5\]\[6\]。
  - [](https://ja.wikipedia.org/wiki/XyMTeX "wikilink") - [化学構造式の描画に用いる](https://ja.wikipedia.org/wiki/化学式#構造式 "wikilink")\[7\]\[8\]。
  - [MusiX](https://ja.wikipedia.org/wiki/MusiXTeX "wikilink") - [楽譜](../Page/楽譜.md "wikilink")の記述に用いる\[9\]\[10\]。

とそれに関連するプログラム、および  のマクロパッケージなどは [CTAN](https://ja.wikipedia.org/wiki/CTAN "wikilink")（**C**omprehensive **T**eX **A**rchive **N**etwork、包括  アーカイブネットワーク）\[11\]からダウンロードできる。

## 数式の表示例

たとえば

``` latex
-b\pm \sqrt{b^2 -4ac} \over 2a
```

は以下のように表示される。

\[-b\pm \sqrt{b^2 -4ac} \over 2a\] また、

``` latex
f(a,b)=\int_a^b \frac{1+x}{a+x^2 +x^3} \, dx
```

は以下のように表示される。

\[f(a,b)=\int_a^b \frac{1+x}{a+x^2 +x^3} \, dx\]

##  の日本語化

[日本語](../Page/日本語.md "wikilink")組版処理のできる日本語版の  および  には、[アスキーによる](../Page/アスキー_\(企業\).md "wikilink") [](../Page/Publishing_TeX.md "wikilink") および  と、[NTT](../Page/日本電信電話.md "wikilink") の斉藤康己による [NTT ](https://ja.wikipedia.org/wiki/NTT_JTeX "wikilink")\[12\]および磯崎秀樹による NTT  などがある。

の日本語対応において技術的に最も大きな課題は、[マルチバイト文字](../Page/マルチバイト文字.md "wikilink")への対応である。（および前身の日本語 ）は、[JIS X 0208](../Page/JIS_X_0208.md "wikilink") を[文字集合](../Page/文字集合.md "wikilink")とした[文字コード](../Page/文字コード.md "wikilink")（[ISO-2022-JP](../Page/ISO-2022-JP.md "wikilink")、[EUC-JP](../Page/EUC-JP.md "wikilink")、および [Shift_JIS](../Page/Shift_JIS.md "wikilink")）を直接扱う。DVI フォーマットは元々16[ビット](../Page/ビット.md "wikilink")以上の文字コードを格納できる仕様が含まれていた。しかしオリジナルの英語版では使われていなかったため、既存プログラムの多くは  が出力する DVI ファイルを処理できない。また[フォント](../Page/フォント.md "wikilink")に関係するファイルフォーマットが拡張されている。これに対して NTT  は、複数の1[バイト文字セットに分割することで対応している](../Page/バイト_\(情報\).md "wikilink")。たとえば、ひらがなとカタカナは内部的には別々の1バイト文字セットとして扱われる。このためにオリジナルの英語版からの変更が小さく、移植も比較的容易である。ファイルフォーマットが同じなので英語版のプログラムで DVI ファイル等を処理することもできる。しかし後述するフォントのマッピングの問題があるため、実際には多くの使用者が NTT  用に拡張されたプログラムを使っている。

使用する[日本語](../Page/日本語.md "wikilink")用フォントについては  が[写研](../Page/写研.md "wikilink")フォントの使用を、NTT  が[大日本印刷](../Page/大日本印刷.md "wikilink")フォントの使用を前提としており、それぞれフォントメトリック情報（フォントの文字寸法の情報）を[バンドル](https://ja.wikipedia.org/wiki/バンドル "wikilink")して配布している。しかし有償であるこれらのフォントのグリフ情報を持っていなくても、画面表示や印刷の際に使用者が利用できる他の日本語用フォントで代用することができる。つまり写研フォントや大日本印刷フォントのフォントメトリック情報を用いて文字の位置を固定し、画面表示や個人ユースの安価なプリンタによるプレビュー印刷には他の日本語用フォントを用い、業者などによる最終的な出力では商用フォントを使用して目的の仕上がりを得る、といったことも可能である。このため日本語化された TeX 関係プログラムのほとんどは、画面表示や印刷で実際に使うフォントを選択できるように、フォントのマッピング（対応付け）を定義する機能を持っている。

歴史的には、[アスキーが日本語](../Page/アスキー_\(企業\).md "wikilink")  の [PC-9800 シリーズ対応版を販売したために個人の使用者を中心に普及した](../Page/PC-9800シリーズ.md "wikilink")。一方、NTT  は元の英語版プログラムからの変更が比較的小さいという利点を受けて、[Unix系](../Page/Unix系.md "wikilink")OSを使う大学や研究機関の関係者を中心に普及した。

しかし現在では次に挙げる理由から、日本語対応  として  が使われていることが多い。

  - [Unix系](../Page/Unix系.md "wikilink")OS用の主な日本語対応  配布形態である ptexlive\[13\]や ptetex3\[14\]\[15\]が  のみを採用している。

  - [Microsoft Windows](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink") 用の主な日本語対応  配布形態である [W32TeX](https://ja.wikipedia.org/wiki/W32TeX "wikilink")\[16\]が  を扱える（NTT  も扱える）。

  - の扱い方を解説する文献の方が、NTT  のものに比べて、出版物と [Web](../Page/World_Wide_Web.md "wikilink") 上文書の両方で多い。

  - は[縦組み](https://ja.wikipedia.org/wiki/縦組み "wikilink")にも対応しているが、NTT  は対応していない。

##  による組版の作業工程

による組版の作業工程は、通常次のようになる。

1.  文章に組版用命令文を織り込んだ[テキストファイル](../Page/テキストファイル.md "wikilink")である、tex ファイルを作成する（[テキストエディタ](../Page/テキストエディタ.md "wikilink")などで）。
2.  [OS](../Page/オペレーティングシステム.md "wikilink") の[コマンドライン](https://ja.wikipedia.org/wiki/コマンドライン "wikilink")から “` tex  `<em>`FileName`</em>`.tex`” などと入力して  を起動し、DVI ファイルを生成させる。
      - ソースファイルにエラーがあれば、修正して再度  を起動する。
3.  DVI 命令文を解するソフトウェア（DVI ウェア）を用いて組版結果を表示し、確認する。
      - DVI ウェアには [xdvi](https://ja.wikipedia.org/wiki/xdvi "wikilink") / [xdvik](https://ja.wikipedia.org/wiki/xdvik "wikilink") や [dviout](https://ja.wikipedia.org/wiki/dviout "wikilink")\[17\]\[18\]などの DVI ヴューア、[Dvips](../Page/Dvips.md "wikilink")(k) や [dvipdfm](https://ja.wikipedia.org/wiki/dvipdfm "wikilink") / DVIPDFM*x* などの[ファイル形式変換](../Page/ファイルフォーマット.md "wikilink")[ソフトウェア](../Page/ソフトウェア.md "wikilink")などがある\[19\]。
      - DVI ファイルを DVI ビューアで画面表示または印刷する、あるいは [PDF](../Page/Portable_Document_Format.md "wikilink") や [PostScript](../Page/PostScript.md "wikilink") に変換して画面表示または印刷することで、組版結果を確認する。
      - 修正の必要があれば、ソースファイルを修正して再度DVIファイルを作成、確認する。

この間、作業工程が変わるたびにそれぞれのプログラムを切り替えたり、扱う文書が大きいと章ごとにソースファイルを分割して管理したりと、比較的煩雑な作業を伴う。そのため、この工程に係わる各種のプログラムやソースファイルの管理を一元的に行う  用の[統合環境](../Page/統合開発環境.md "wikilink")（[TeXworks](https://ja.wikipedia.org/wiki/TeXworks "wikilink") や [TeXShop](https://ja.wikipedia.org/wiki/TeXShop "wikilink") など）がいくつか作成されている。

### GUI 環境と

[GUI](https://ja.wikipedia.org/wiki/グラフィカルユーザインタフェース "wikilink") は [PC](../Page/パーソナルコンピュータ.md "wikilink") の普及に一役買ったが、それとともに  などの[コマンドラインインタプリタ](../Page/コマンドラインインタプリタ.md "wikilink")に不慣れな PC 利用者が増加した。そのために、GUI に特化した  用[統合環境が](../Page/統合開発環境.md "wikilink") LyX\[20\] などいくつか作成されている。

## 関連ソフトウェア

  - DVI ウェア

      - [xdvi](https://ja.wikipedia.org/wiki/xdvi "wikilink")/[xdvik](https://ja.wikipedia.org/wiki/xdvik "wikilink"), [dviout for Windows](https://ja.wikipedia.org/wiki/dviout_for_Windows "wikilink"), [Dvips](../Page/Dvips.md "wikilink")(k), [dvipdfm](https://ja.wikipedia.org/wiki/dvipdfm "wikilink") / DVIPDFM*x* など。

  - 文書の文献管理のための [](../Page/BibTeX.md "wikilink") や索引作成のための *[MakeIndex](https://ja.wikipedia.org/wiki/MakeIndex "wikilink")*\[21\]。

  - 機能拡張版

      - [pdf](https://ja.wikipedia.org/wiki/pdfTeX "wikilink"), [](../Page/ConTeXt.md "wikilink"), [](https://ja.wikipedia.org/wiki/e-TeX "wikilink")\[22\], [](https://ja.wikipedia.org/wiki/XeTeX "wikilink") など。

  - [Unicode](../Page/Unicode.md "wikilink") をベースとした多言語拡張版

      - Omega\[23\](lambda), Aleph\[24\] (lamed) など。

  - [Kile](../Page/Kile.md "wikilink"), [TeXShop](https://ja.wikipedia.org/wiki/TeXShop "wikilink")\[25\]\[26\], EasyTeX\[27\], [WinShell](../Page/WinShell.md "wikilink") などの[統合環境や](../Page/統合開発環境.md "wikilink")、[TeXmacs](https://ja.wikipedia.org/wiki/TeXmacs "wikilink")\[28\]\[29\], [LyX](../Page/LyX.md "wikilink") などの [GUI](https://ja.wikipedia.org/wiki/グラフィカルユーザインターフェース "wikilink") [フロントエンド](../Page/フロントエンド.md "wikilink")。

  - [ Live](https://ja.wikipedia.org/wiki/TeX_Live "wikilink")\[30\]\[31\]や [te](https://ja.wikipedia.org/wiki/teTeX "wikilink")\[32\]\[33\]などの  配布形態や、[mimeTeX](https://ja.wikipedia.org/wiki/mimeTeX "wikilink")\[34\]\[35\]などの  [サブセット](https://ja.wikipedia.org/wiki/サブセット "wikilink")。

  - [Textext](https://ja.wikipedia.org/wiki/Textext "wikilink")\[36\]、[InkLaTeX](https://ja.wikipedia.org/wiki/InkLaTeX "wikilink")\[37\]などの [Inkscape](../Page/Inkscape.md "wikilink") への  プラグイン。

  - [KETpic](../Page/KETpic.md "wikilink") - [Maxima](../Page/Maxima.md "wikilink") 上、[Scilab](../Page/Scilab.md "wikilink") 上、[Mathematica](../Page/Mathematica.md "wikilink") 上、および [Maple](../Page/Maple.md "wikilink") 上で  描画コードである [tpic specials](https://ja.wikipedia.org/wiki/tpic_specials "wikilink") を生成するマクロパッケージ

  - [MathType](https://ja.wikipedia.org/wiki/MathType "wikilink") version 6.5 以降では、[Microsoft Word](../Page/Microsoft_Word.md "wikilink") 上に書かれた  の命令文を直接数式に変換できるようになった。現時点では [PowerPoint](../Page/Microsoft_PowerPoint.md "wikilink") 上での  の命令文による直接的な数式編集はできない。

## コミュニティ

[thumb](https://ja.wikipedia.org/wiki/画像:Logo_TUG.svg "wikilink") 有名な  コミュニティの一つは  Users Group (TUG) であり、**\[38\] や **\[39\] (TPJ) を出版している。\[40\] はドイツの大きなユーザーグループである。tex.stackexchange.com\[41\] は  ユーザーのための質問・回答サイトである。

ユーザの集いは、日本で2009年以降毎年開かれている  の研究集会であり、 や組版・出版など関する知見の共有や、 ユーザーの相互交流を目的としている\[42\]\[43\]。ただし2013年は、TUG 2013 が東京で開催され、 ユーザの集いは開催されなかった\[44\]。

## 脚注

### 補足

### 出典

## 参考文献

  -
  -
  -
## 関連項目

  - [Publishing ](../Page/Publishing_TeX.md "wikilink") ()
  - [](../Page/LaTeX.md "wikilink")
  - [pdf](https://ja.wikipedia.org/wiki/pdfTeX "wikilink")
  - [](https://ja.wikipedia.org/wiki/LuaTeX "wikilink")
  - [](https://ja.wikipedia.org/wiki/XeTeX "wikilink")
  - [](../Page/ConTeXt.md "wikilink")
  - [MathJax](https://ja.wikipedia.org/wiki/MathJax "wikilink")
  - [DVI (ファイルフォーマット)](https://ja.wikipedia.org/wiki/DVI_\(ファイルフォーマット\) "wikilink")
  - [ドナルド・クヌース](../Page/ドナルド・クヌース.md "wikilink")

## 外部リンク

  - [Don Knuth's Home Page](http://www-cs-faculty.stanford.edu/~knuth/)
  - [TeX Users Group (TUG) home page](https://tug.org/)
  - [the Comprehensive  Archive Network](https://www.ctan.org/) (CTAN)
  - [ Wiki](https://texwiki.texjp.org) -  に関する日本語[ウィキ](../Page/ウィキ.md "wikilink")サイト

[Category:TeX](https://ja.wikipedia.org/wiki/Category:TeX "wikilink") [Category:マークアップ言語](https://ja.wikipedia.org/wiki/Category:マークアップ言語 "wikilink") [Category:DTPソフト](https://ja.wikipedia.org/wiki/Category:DTPソフト "wikilink") [Category:コンピュータ言語](https://ja.wikipedia.org/wiki/Category:コンピュータ言語 "wikilink") [Category:1978年のソフトウェア](https://ja.wikipedia.org/wiki/Category:1978年のソフトウェア "wikilink") [Category:ドナルド・クヌース](https://ja.wikipedia.org/wiki/Category:ドナルド・クヌース "wikilink")

1.  2016年10月1日現在のバージョンは 3.14159265 である。
2.  [2016年](../Page/2016年.md "wikilink")[10月1日](../Page/10月1日.md "wikilink")現在のバージョンは 2.7182818 である。
3.  なお、*book* の翻訳版出版元であるアスキーの編集者だった鈴木嘉平によれば、アスキー社内では「テック」と読んでいたが、先輩編集者によれば（fuで発音する）「テフ」ではないとはっきり書いておかなかったのが原因で、日本には「テフ」が広まってしまった、という (https://www.kahei.org/2014/04/tex.html )。
4.  [The TeX Catalogue OnLine, Entry for slides, Ctan Edition](http://mirror.ctan.org/help/Catalogue/entries/slides.html)（[Ring Server によるミラーリング](http://www.ring.gr.jp/pub/text/CTAN/help/Catalogue/entries/slides.html)）
5.  [AMS-LaTeX — American Mathematical Society](http://www.ams.org/tex/amslatex.html)
6.  [The TeX Catalogue OnLine, Entry for amslatex, Ctan Edition](http://mirror.ctan.org/help/Catalogue/entries/amslatex.html)（[Ring Server によるミラーリング](http://www.ring.gr.jp/pub/text/CTAN/help/Catalogue/entries/amslatex.html)）
7.  [XyMTeX 化学構造式描画システム](http://xymtex.com/fujitas3/xymtex/)
8.  [The TeX Catalogue OnLine, Entry for XyMTeX, Ctan Edition](http://mirror.ctan.org/help/Catalogue/entries/xymtex.html)（[Ring Server によるミラーリング](http://www.ring.gr.jp/pub/text/CTAN/help/Catalogue/entries/xymtex.html)）
9.  [Werner Icking Music Archive: MusiXTeX Files](http://icking-music-archive.org/software/indexmt6.html)
10. [The TeX Catalogue OnLine, Entry for MusiXTeX, Ctan Edition](http://mirror.ctan.org/help/Catalogue/entries/musixtex.html)（[Ring Server によるミラーリング](http://www.ring.gr.jp/pub/text/CTAN/help/Catalogue/entries/musixtex.html)）
11. [the Comprehensive TeX Archive Network](http://www.ctan.org/)
12. NTT  は[千葉大学](https://ja.wikipedia.org/wiki/千葉大学 "wikilink")の櫻井貴文によって [UNIX](../Page/UNIX.md "wikilink") システムに移植され、メンテナンスされている。現在、「[Software by Takafumi SAKURAI](http://www.math.s.chiba-u.ac.jp/~sakurai/software.html)」で公開されている。
13. [ptexlive Wiki](http://tutimura.ath.cx/ptexlive/)
14. [ptetex—teTeX 用日本語パッチ集](http://tutimura.ath.cx/~nob/tex/ptetex.html)
15. [ptetex Wiki](http://tutimura.ath.cx/ptetex/)
16. [W32TeX](http://w32tex.org/index-ja.html)
17. [dviout/dviprt 開発室 — Oshima Laboratory](http://akagi.ms.u-tokyo.ac.jp/dvitest.html)
18. [The TeX Catalogue OnLine, Entry for dviout, Ctan Edition](http://mirror.ctan.org/help/Catalogue/entries/dviout.html)（[Ring Server によるミラーリング](http://www.ring.gr.jp/pub/text/CTAN/help/Catalogue/entries/dviout.html)）
19. 各 DVI ウェアの間には DVI ファイルの解釈・表示について[互換性](../Page/互換性.md "wikilink")がない場合がある。特に、ある DVI ウェアに依存したパッケージをソースファイルに用いるなどして、その DVI ウェア用の専用命令文 (special) を埋め込んで作成した DVI ファイルは、当然ながらその専用命令文を解釈可能な DVI ウェアでなければ画面表示・印刷などが正しくできない。
20. [LyX](http://www.lyx.org/WebJa.Home)
21. [The TeX Catalogue OnLine, Entry for *MakeIndex*, Ctan Edition](http://mirror.ctan.org/help/Catalogue/entries/makeindex.html)（[Ring Server によるミラーリング](http://www.ring.gr.jp/pub/text/CTAN/help/Catalogue/entries/makeindex.html)）
22. [The TeX Catalogue OnLine, Entry for etex, Ctan Edition](http://mirror.ctan.org/help/Catalogue/entries/etex.html)（[Ring Server によるミラーリング](http://www.ring.gr.jp/pub/text/CTAN/help/Catalogue/entries/etex.html)）
23. [The  Catalogue OnLine, Entry for Omega, Ctan Edition](http://mirror.ctan.org/help/Catalogue/entries/omega.html)（[Ring Server によるミラーリング](http://www.ring.gr.jp/pub/text/CTAN/help/Catalogue/entries/omega.html)）
24. [The  Catalogue OnLine, Entry for aleph, Ctan Edition](http://mirror.ctan.org/help/Catalogue/entries/aleph.html)（[Ring Server によるミラーリング](http://www.ring.gr.jp/pub/text/CTAN/help/Catalogue/entries/aleph.html)）
25. [TeXShop — Richard <span style="font-variant: small-caps">Koch</span>](http://www.uoregon.edu/~koch/texshop/)
26. [The TeX Catalogue OnLine, Entry for TeXShop, Ctan Edition](http://mirror.ctan.org/help/Catalogue/entries/texshop.html)（[Ring Server によるミラーリング](http://www.ring.gr.jp/pub/text/CTAN/help/Catalogue/entries/texshop.html)）
27. [TeX 入門 \#EasyTeX — 中川 仁](http://www.juen.ac.jp/math/nakagawa/texguide.html#easytex)
28. [Welcome to GNU TeXmacs (FSF GNU project)](http://www.texmacs.org/)
29. [The TeX Catalogue OnLine, Entry for TeXmacs, Ctan Edition](http://mirror.ctan.org/help/Catalogue/entries/texmacs.html)（[Ring Server によるミラーリング](http://www.ring.gr.jp/pub/text/CTAN/help/Catalogue/entries/texmacs.html)）
30. [ Live —  Users Group](http://texlive.org/)
31. [The  Catalogue OnLine, Entry for texlive, Ctan Edition](http://mirror.ctan.org/help/Catalogue/entries/texlive.html)（[Ring Server によるミラーリング](http://www.ring.gr.jp/pub/text/CTAN/help/Catalogue/entries/texlive.html)）
32. [The teTeX Homepage](http://tug.org/teTeX/)
33. [The  Catalogue OnLine, Entry for te, Ctan Edition](http://mirror.ctan.org/help/Catalogue/entries/tetex.html)（[Ring Server によるミラーリング](http://www.ring.gr.jp/pub/text/CTAN/help/Catalogue/entries/tetex.html)）
34. [mimeTeX quickstart](http://www.forkosh.com/mimetex.html)
35. [The TeX Catalogue OnLine, Entry for mimeTeX, Ctan Edition](http://mirror.ctan.org/help/Catalogue/entries/mimetex.html)（[Ring Server によるミラーリング](http://www.ring.gr.jp/pub/text/CTAN/help/Catalogue/entries/mimetex.html)）
36. [Textext — Pauli <span style="font-variant: small-caps">Virtanen</span>](http://www.iki.fi/pav/software/textext/)
37. [Inkscape de LaTeX](http://www.kono.cis.iwate-u.ac.jp/~arakit/inkscape/inklatex-ja.html)
38. [TUGboat - Communications of the TeX Users Group](http://tug.org/TUGboat/)
39. [The PracTeX Journal home page](http://tug.org/pracjourn/index.html)
40. [Dante e.V.](https://www.dante.de/)
41. [tex.stackexchange.com](http://tex.stackexchange.com/)
42. [ ユーザの集い2009](http://oku.edu.mie-u.ac.jp/texconf09/)
43. [ ユーザの集い2015](http://texconf15.tumblr.com/)
44. [TUG 2013 - TeX Users Group](http://www.tug.org/tug2013/jp/)
> この記事は[Python](https://ja.wikipedia.org/wiki/Python)から翻訳されています。


**Python**（パイソン）は、汎用の[プログラミング言語](../Page/プログラミング言語.md "wikilink")である。コードがシンプルで扱いやすく設計されており、[C言語](../Page/C言語.md "wikilink")などに比べて、さまざまなプログラムを分かりやすく、少ない[コード行数](https://ja.wikipedia.org/wiki/コード行数 "wikilink")で書けるといった特徴がある\[1\]\[2\]。

## 概要

[文法を極力単純化してコードの](https://ja.wikipedia.org/wiki/シンタックス "wikilink")[可読性](../Page/可読性.md "wikilink")を高め、読みやすく、また書きやすくして[プログラマ](../Page/プログラマ.md "wikilink")の作業性とコードの信頼性を高めることを重視してデザインされた、汎用の[高水準言語](../Page/高水準言語.md "wikilink")である。

核となる本体部分は必要最小限に抑えられている。一方で[標準ライブラリ](https://ja.wikipedia.org/wiki/標準ライブラリ "wikilink")やサードパーティ製のライブラリ、[関数など](../Page/サブルーチン.md "wikilink")、さまざまな領域に特化した豊富で大規模なツール群が用意され、インターネット上から無料で入手でき、自らの使用目的に応じて機能を拡張していくことができる。

またPythonは多くの[ハードウェア](../Page/ハードウェア.md "wikilink")とOS ([プラットフォーム](../Page/プラットフォーム_\(コンピューティング\).md "wikilink")) に対応しており、複数の[プログラミングパラダイム](../Page/プログラミングパラダイム.md "wikilink")に対応している。Pythonは[オブジェクト指向](../Page/オブジェクト指向プログラミング.md "wikilink")・[命令型](https://ja.wikipedia.org/wiki/命令型 "wikilink")・[手続き型](https://ja.wikipedia.org/wiki/手続き型 "wikilink")・[関数型](https://ja.wikipedia.org/wiki/関数型 "wikilink")などの形式でプログラムを書くことができる。[動的型付け](../Page/動的型付け.md "wikilink")言語であり、[参照カウント](../Page/参照カウント.md "wikilink")ベースの自動[メモリ管理](../Page/メモリ管理.md "wikilink")（[ガベージコレクタ](../Page/ガベージコレクション.md "wikilink")）を持つ。

これらの特性によりPythonは広い支持を獲得し、[Webアプリケーション](https://ja.wikipedia.org/wiki/Webアプリケーション "wikilink")や[デスクトップアプリケーション](https://ja.wikipedia.org/wiki/デスクトップアプリケーション "wikilink")などの開発はもとより、システム用の記述 (script) や、各種の自動処理、理工学や統計・解析など、幅広い領域における有力なプログラム言語となった。プログラミング作業が容易で能率的であることは、ソフトウェア企業にとっては投入人員の節約、開発時間の短縮、ひいてはコスト削減に有益であることから、産業分野でも広く利用されている。[Google](../Page/Google.md "wikilink")など主要言語に採用している企業も多い。

Pythonの[リファレンス実装](../Page/リファレンス実装.md "wikilink")である[CPython](https://ja.wikipedia.org/wiki/CPython "wikilink")は、[フリーかつオープンソースのソフトウェアであり](https://ja.wikipedia.org/wiki/FLOSS "wikilink")、コミュニティベースの開発モデルを採用している。CPythonは、非営利団体である[Pythonソフトウェア財団](https://ja.wikipedia.org/wiki/Pythonソフトウェア財団 "wikilink")が管理している。その他の実装としては、[PyPy](https://ja.wikipedia.org/wiki/PyPy "wikilink")や[IronPython](../Page/IronPython.md "wikilink")などが有名である。

Pythonは、[オランダ](https://ja.wikipedia.org/wiki/オランダ "wikilink")人の[グイド・ヴァンロッサム](https://ja.wikipedia.org/wiki/グイド・ヴァンロッサム "wikilink")が開発した。名前の由来は、[イギリス](https://ja.wikipedia.org/wiki/イギリス "wikilink")のテレビ局 [BBC](../Page/英国放送協会.md "wikilink") が製作したコメディ番組『[空飛ぶモンティ・パイソン](../Page/空飛ぶモンティ・パイソン.md "wikilink") (*Monty Python's Flying Circus*)』である。Pythonという英単語が意味する[爬虫類](../Page/爬虫類.md "wikilink")の[ニシキヘビがPython言語のマスコットやアイコンとして使われている](../Page/ニシキヘビ属.md "wikilink")。

### 特徴

Pythonは[インタプリタ](../Page/インタプリタ.md "wikilink")上で実行することを前提に設計している。以下の特徴をもっている:

  - [動的な型付け](../Page/動的型付け.md "wikilink")
  - [ガベージコレクション](../Page/ガベージコレクション.md "wikilink")
  - [マルチパラダイム](https://ja.wikipedia.org/wiki/マルチパラダイムプログラミング言語 "wikilink")
  - [モジュール](../Page/モジュール.md "wikilink")・[クラス](../Page/クラス_\(コンピュータ\).md "wikilink")・オブジェクト等の言語の要素が内部からアクセス可能であり、[リフレクションを利用した記述が可能](../Page/リフレクション_\(情報工学\).md "wikilink")。

### 動作する計算機環境 (platform)

Pythonの最初のバージョンは[Amoeba上で開発された](https://ja.wikipedia.org/wiki/Amoeba_\(オペレーティングシステム\) "wikilink")。のちに多くの計算機環境上で動作するようになった。

  - [Windows](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")\[3\], [Windows CE](https://ja.wikipedia.org/wiki/Microsoft_Windows_CE "wikilink")（[9x系および](../Page/Windows_9x系.md "wikilink")[NT系は最新版](../Page/Windows_NT系.md "wikilink")、[Windows 3.1および](../Page/Microsoft_Windows_3.x.md "wikilink")[MS-DOS](../Page/MS-DOS.md "wikilink")は旧版のみ）
  - Macintosh ([Classic Mac OSおよび](../Page/Classic_Mac_OS.md "wikilink")[macOS](https://ja.wikipedia.org/wiki/macOS "wikilink")ともに)
  - iOS Pythonista for iOS (omz:software)
  - Android Pydroid3 for Android (IIEC)
  - 各種[UNIX](../Page/UNIX.md "wikilink")
  - [Linux](../Page/Linux.md "wikilink") ([Linux Standard Base](../Page/Linux_Standard_Base.md "wikilink")3.2で標準仕様となった)
  - [Plan 9](../Page/Plan_9_from_Bell_Labs.md "wikilink") (Python 3.xは未移植)
  - [PalmOS](../Page/Garnet_OS.md "wikilink")
  - [S60](https://ja.wikipedia.org/wiki/S60 "wikilink")
  - [Javaプラットフォーム](../Page/Javaプラットフォーム.md "wikilink") ([Jython](../Page/Jython.md "wikilink"))
  - [.NET Frameworkプラットフォーム](https://ja.wikipedia.org/wiki/.NET_Framework "wikilink") ([IronPython](../Page/IronPython.md "wikilink"))

### 実装

Pythonには複数の実装が存在する。

  - [CPython](https://ja.wikipedia.org/wiki/CPython "wikilink") - 作者によって[C言語](../Page/C言語.md "wikilink")で書かれたバージョン。通常「Python」といえばこのCPythonを指す。
  - [Stackless Python](https://ja.wikipedia.org/wiki/Stackless_Python "wikilink") - C[スタック](../Page/スタック.md "wikilink")を使わずに独自のスタック（Pythonスタック）で実装したもの。
  - [Unladen Swallow](https://ja.wikipedia.org/wiki/Unladen_Swallow "wikilink") - [Google](../Page/Google.md "wikilink")のチームによるPythonの実装
  - [Jython](../Page/Jython.md "wikilink") - [Java仮想マシン](../Page/Java仮想マシン.md "wikilink")上に移植したもの。PythonからJavaのライブラリを使うことができる。
  - [IronPython](../Page/IronPython.md "wikilink") - .NET Framework/[Monoで動作するPython](../Page/Mono_\(ソフトウェア\).md "wikilink")。[C\#で実装されている](../Page/C_Sharp.md "wikilink")。.NET Frameworkのライブラリを使うことができる。[動的言語ランタイム](../Page/動的言語ランタイム.md "wikilink")上に構築されているため、既存の.NETアプリケーションへ[マクロ言語](../Page/マクロ言語.md "wikilink")として搭載することも可能となっている。
  - [PyPy](https://ja.wikipedia.org/wiki/PyPy "wikilink") - Python ([RPython](https://ja.wikipedia.org/wiki/RPython "wikilink")) によるPythonの実装
  - [Psyco](https://ja.wikipedia.org/wiki/Psyco "wikilink") - CPython向けの[JITコンパイラ](../Page/実行時コンパイラ.md "wikilink")
  - [PyMite](https://ja.wikipedia.org/wiki/PyMite "wikilink") - 組み込み向けの実装、[AVRなどに対応](../Page/Atmel_AVR.md "wikilink")。
  - [tinypy](https://ja.wikipedia.org/wiki/tinypy "wikilink") - 同じく組み込み向けの実装。ソースコードが64KB未満と非常に軽量なことが謳われている。
  - [MicroPython](https://ja.wikipedia.org/wiki/MicroPython "wikilink") - 組み込み向けの実装。256KB以上のフラッシュを推奨。
  - [Pyodide](https://ja.wikipedia.org/wiki/Pyodide "wikilink") - [WebAssembly](https://ja.wikipedia.org/wiki/WebAssembly "wikilink")向けの実装\[4\]

### ライセンス

Python のリリースは全て[オープンソース](../Page/オープンソース.md "wikilink")であり、[PSF (Python Software Foundationライセンス)](https://www.python.org/download/releases/2.5/license/)として配布されている。これは[GPL互換であるが](../Page/GNU_General_Public_License.md "wikilink")、GPLと異なり、変更したバージョンを配布する際に変更をオープンソースにしなくてもよい。

## 言語の機能

Pythonには、読みやすく、それでいて効率もよいコードをなるべく簡単に書けるようにするという思想が浸透しており、Pythonコミュニティでも単純で短いコードをよしとする傾向が強い\[5\]。

Pythonの本体は、ユーザがいつも必要とする最小限の機能のみを提供する。基本機能以外の専門機能や拡張プログラムはインターネット上にライブラリとして提供されており、別途ダウンロードして保存し、必要なツールはこのツールキットからその都度呼び出して使用する\[6\]。

またPythonでは、Perlの「やり方は一つじゃない」という哲学\[7\]とは逆に、ある動作をさせる方法は、基本的に1通りしかないように作られている。そのためPythonの[プログラムは](../Page/プログラム_\(コンピュータ\).md "wikilink")、誰が書いてもだいたいどれも同じようなコードになり、作成者以外が見ても動作を把握しやすい。また、Pythonではプログラムの文書化（[ソフトウェアドキュメンテーション](../Page/ソフトウェアドキュメンテーション.md "wikilink")）が重視されており、言語の基本機能の一部となっている。

### 構文

[インデント](https://ja.wikipedia.org/wiki/インデント "wikilink")が意味を持つ「[オフサイドルール](../Page/オフサイドルール.md "wikilink")」が特徴的である。

以下に、[階乗](../Page/階乗.md "wikilink") (関数名: factorial)を題材にC言語と比較した例を示す。

**Pythonのコード:**

``` python
def factorial(x):
    if x == 0:
        return 1
    else:
        return x * factorial(x - 1)
```

**わかりやすく整形されたC言語のコード:**

``` c
int factorial(int x) {
    if (x == 0) {
        return 1;
    } else {
        return x * factorial(x - 1);
    }
}
```

この例では、Pythonと整形されたC言語とでは、プログラムコードの間に違いがほとんど見られない。しかし、C言語のインデントは構文規則上のルールではなく、単なる読みやすさを向上させる[コーディングスタイル](https://ja.wikipedia.org/wiki/コーディングスタイル "wikilink")でしかない。そのためC言語では全く同じプログラムを以下のように書くこともできる。

**わかりにくいC:**

``` c
int factorial(int x) {
 if(x == 0) {return 1;} else
 {return x * factorial(x - 1); } }
```

Pythonではインデントは構文規則として決められているため、こうした書き方は不可能である。Pythonではこのように強制することによって、ソースコードのスタイルがその書き手にかかわらずほぼ統一したものになり、その結果読みやすくなるという考え方が取り入れられている。これについては賛否両論があり、批判的立場の人々からは、これはプログラマがスタイルを選ぶ自由を制限するものだ、という意見も出されている。

インデントによる整形は、単に「見かけ」だけではなく品質そのものにも関係する。例として次のコードを示す。

**間違えたC:**

``` c
if (x > 10)
    x = 10;
    y = 0;
```

このコードはC言語の構文規則上は問題無いが、インデントによる見かけのifの範囲と、言語仕様によるifの実際の範囲とが異なっているため、プログラマの意図が曖昧になる。(前者は"y = 0;"がif文に包含され、後者は"{}"がないため"y = 0;"がif文に包含されない)この曖昧さは、検知しにくいバグを生む原因になる。例としては[Apple goto failが挙げられる](https://ja.wikipedia.org/wiki/到達不能コード#CVE-2014-1266 "wikilink")。

ソースコードを読む際、多くの人はインデントのような空白を元に整列されたコードを読み、コンパイラのように構文解析しながらソースを読むものではない。その結果、一見しただけでは原因を見つけられないバグを作成する危険がある。

Pythonではインデントをルールとすることにより、人間が目視するソースコードの理解とコンパイラの構文解析の間の差を少なくすることで、より正確に意図した通りにコーディングすることができると主張されている。

### データ型

Pythonのデータは動的に型付けされる。値自身が型を持っており、変数はすべて値への[参照である](../Page/参照_\(情報工学\).md "wikilink")。

基本的な[データ型](../Page/データ型.md "wikilink")として、[整数](../Page/整数.md "wikilink")型・[多倍長整数](https://ja.wikipedia.org/wiki/多倍長整数 "wikilink")型・[浮動小数点数](../Page/浮動小数点数.md "wikilink")型・[複素数](../Page/複素数.md "wikilink")型・文字列型・[Unicode](../Page/Unicode.md "wikilink")文字列型・[論理型](../Page/ブーリアン型.md "wikilink")、そして関数型がある。多倍長整数型は（メモリの許す限り）無制限の桁数で整数計算が可能である。浮動小数点数型を整数型にキャストすると、小数点以下が切り捨てられる。

さらに組み込みの[コンテナ型として](../Page/コンテナ_\(データ型\).md "wikilink")、[リスト型](../Page/リスト_\(抽象データ型\).md "wikilink")、[タプル型](https://ja.wikipedia.org/wiki/タプル#プログラミング言語Pythonにおけるタプル "wikilink")、辞書型（[連想配列](../Page/連想配列.md "wikilink")）のほか、値の重複を許さない[集合](../Page/集合.md "wikilink")型（Python 2.3以降）がある。

Python 3.x以降では、整数型が多倍長整数型と統合され、従来の文字列型とUnicode文字列型に代わり、バイト列型と文字列型が導入された。

リスト型および辞書型は内部の値をあとから変えられる（、変更可能）が、タプル型は一度構築したら内部の値は変わらない（、変更不能）。タプル型とリスト型は、多くのプログラミング言語では[配列](../Page/配列.md "wikilink")と呼ばれるものに類似している。しかし、Pythonではタプル型は辞書のキーとして使うことができるが、リスト型は内容が変わるため辞書のキーとして使うことはできないという理由から、これら2つの型を区別している。集合型には変更可能なものと変更不能なものの2種類がある。

多くのオブジェクト指向プログラミング言語と同様、Pythonではユーザが新しく自分の型を定義することも可能である。この場合、組み込み型を含む既存の型を継承して新たな型（クラス）を定義する事も、ゼロから全く新しい型を作り出す事も出来る。

Pythonは基本的にメソッドや関数の引数に型を指定する必要がない。そのため、[ダック・タイピング](../Page/ダック・タイピング.md "wikilink")という、内部で必要とする演算子やメソッドに対応していれば、関数やオブジェクトの設計時点で意図していなかったオブジェクトを引き渡すことも可能である。

Pythonは[ガベージコレクション](../Page/ガベージコレクション.md "wikilink")を内蔵しており、参照されなくなったオブジェクトは自動的にメモリから破棄される。CPythonでは、ガベージコレクションの方式として[参照カウント](../Page/参照カウント.md "wikilink")方式と[マーク・アンド・スイープ](../Page/マーク・アンド・スイープ.md "wikilink")方式を併用している。マーク・アンド・スイープ方式のみに頼っている言語では、オブジェクトがいつ回収されるか保証されないので、ファイルのクローズなどを[デストラクタ](../Page/デストラクタ.md "wikilink")に任せることができない。CPythonは参照カウント方式を併用することで、循環参照が発生しない限り、オブジェクトはスコープアウトした時点で必ずデストラクトされることを保証している。なおJythonおよびIronPythonではマーク・アンド・スイープ方式を採用しているため、スコープアウトした時点で必ずデストラクトされることが前提のコードだとJythonやIronPythonでは正しく動かない。

[イテレータ](../Page/イテレータ.md "wikilink")を実装するためのジェネレータが言語仕様に組み込まれており、Pythonでは多くの場面で[イテレータ](../Page/イテレータ.md "wikilink")を使うように設計されている。イテレータの使用はPython全体に普及していて、プログラミングスタイルの統一性をもたらしている。

### オブジェクト指向プログラミング

Pythonでは扱えるデータの全てがオブジェクトである。単純な数値といった基本的なデータ型をはじめ、組み込みのコンテナ型、組み込み関数など、これらは全て統一的な継承関係をもつオブジェクトであり「型」をもっている。これらの組み込み型とユーザ定義型は区別されず、組み込み型を継承したクラスを定義できる。上の「データ型」の項で述べたように Pythonは静的な型チェックを持たないため、Javaのようなインターフェイスという言語上の仕組みは必要とされない。

クラスの[継承](../Page/継承_\(プログラミング\).md "wikilink") () メカニズムでは、複数の基底クラスを持つことができ（多重継承）、導出されたクラスでは基底クラスの任意のメソッドをオーバライド（; 上書き）することが可能である。

また、オブジェクトには任意のデータを入れることができる。これらのメソッドやデータは、基本的に、すべて`public`であり、`virtual`（仮想）である。ただし、先頭にアンダースコアをもつメンバを`private`とすることができる。これは単なるマナーであるが、アンダースコアを2つもつ場合は、クラスの外部からメンバの名前を隠された状態（; 難号化）とすることで[カプセル化](../Page/カプセル化.md "wikilink")を実現できる。また、[利用者定義演算子](https://ja.wikipedia.org/wiki/利用者定義演算子 "wikilink")が機能として用意されており ほとんどの組み込み演算子（算術演算子（）や添字表記）はクラスインスタンスで使うために再定義することが可能となっている。

### ライブラリ

Pythonには「電池付属 ()」という思想があり、プログラマがすぐに使えるようなライブラリや統合環境をあらかじめディストリビューションに含めるようにしている。このため標準ライブラリは非常に充実している。

  - [正規表現](../Page/正規表現.md "wikilink")
  - OSの[システムコール](../Page/システムコール.md "wikilink")
  - [XML処理系](../Page/Extensible_Markup_Language.md "wikilink")
  - [シリアライゼーション](../Page/シリアライズ.md "wikilink")
  - [HTTP](../Page/Hypertext_Transfer_Protocol.md "wikilink")、[FTP等の各種](../Page/File_Transfer_Protocol.md "wikilink")[通信プロトコル](../Page/通信プロトコル.md "wikilink")
  - [電子メール](../Page/電子メール.md "wikilink")や[CSVファイルの処理](../Page/Comma-Separated_Values.md "wikilink")
  - [データベース](../Page/データベース.md "wikilink")接続 ([SQLite](../Page/SQLite.md "wikilink")を標準で扱える)
  - [GUIフレームワーク](https://ja.wikipedia.org/wiki/グラフィカルユーザインタフェース "wikilink") ([Tkinter](https://ja.wikipedia.org/wiki/Tkinter "wikilink"))
  - [HTMLのパーサー](../Page/HyperText_Markup_Language.md "wikilink")
  - Python自身のコードの[構文解析](../Page/構文解析.md "wikilink")ツール

[サードパーティによるライブラリも豊富に存在する](../Page/サードパーティー.md "wikilink")。

  - [行列](https://ja.wikipedia.org/wiki/行列 "wikilink")演算パッケージの [NumPy](https://ja.wikipedia.org/wiki/NumPy "wikilink")
  - 画像処理のための [Python Imaging Library](https://ja.wikipedia.org/wiki/Python_Imaging_Library "wikilink")
  - [SDL](../Page/SDL.md "wikilink")のラッパである [Pygame](https://ja.wikipedia.org/wiki/Pygame "wikilink")
  - プログラミング数学、科学、工学のための数値解析 [SciPy](../Page/SciPy.md "wikilink")
  - [スクレイピング](https://ja.wikipedia.org/wiki/スクレイピング "wikilink")ライブラリ [Beautiful Soup](https://ja.wikipedia.org/wiki/Beautiful_Soup "wikilink")
  - クローリング、スクレイピング用のpythonフレームワーク [Scrapy](../Page/Scrapy.md "wikilink")
  - 数式処理機能の [SymPy](https://ja.wikipedia.org/wiki/SymPy "wikilink")
  - グラフ表示ソフト [Matplotlib](https://ja.wikipedia.org/wiki/Matplotlib "wikilink")
  - データ解析ソフト [pandas](https://ja.wikipedia.org/wiki/pandas "wikilink")
  - 離散事象シミュレーション [SimPy](https://ja.wikipedia.org/wiki/SimPy "wikilink")
  - 機械学習ライブラリ [scikit-learn](https://ja.wikipedia.org/wiki/scikit-learn "wikilink")
  - Pythonアプリのコンパイルによる高速化 [Numba](https://ja.wikipedia.org/wiki/Numba "wikilink")
  - [OpenCL](../Page/OpenCL.md "wikilink")へのインタフェース [pyOpenCL](https://ja.wikipedia.org/wiki/pyOpenCL "wikilink")
  - [OpenGL](../Page/OpenGL.md "wikilink")へのインタフェース [pyOpenGL](https://ja.wikipedia.org/wiki/pyOpenGL "wikilink")
  - [OpenCV](../Page/OpenCV.md "wikilink")へのインタフェース [pyOpenCV](https://ja.wikipedia.org/wiki/pyOpenCV "wikilink")
  - [CUDA](../Page/CUDA.md "wikilink")へのインタフェース [pyCUDA](https://ja.wikipedia.org/wiki/pyCUDA "wikilink")
  - 3Dグラフィックスやアニメーション [VPyyhon](https://ja.wikipedia.org/wiki/VPython "wikilink")
  - [PyODE](https://ja.wikipedia.org/wiki/PyODE "wikilink")
  - [Cython](https://ja.wikipedia.org/wiki/Cython "wikilink")
  - [Python(x,y)](https://ja.wikipedia.org/wiki/Python\(x,y\) "wikilink")

マイナーなものまで含めると多すぎて収拾がつかない。 [Python Package Index](https://ja.wikipedia.org/wiki/Python_Package_Index "wikilink") (PyPI) と呼ぶ公式のパッケージリポジトリを導入した。

### 多言語の扱い

Pythonは当初1バイト単位での[文字列](../Page/文字列.md "wikilink")型のみ扱い、かな漢字のような[マルチバイト文字](../Page/マルチバイト文字.md "wikilink")をサポートしていなかったが、Python 2.0から[Unicode](../Page/Unicode.md "wikilink")文字型が新たに導入された\[8\]。

Python 3.0では、文字列型がバイト列型に、Unicode文字列型が文字列型に変更された。これにより、Python 3.0で文字列を扱う際には後述の変換処理を必ず行う必要がある。ファイル入出力などエンコードを明示しなければ標準エンコードを用いて暗黙に行われる場合も多い。これにより多言語の扱いを一貫したものにしている。

Pythonでは文字の[エンコード](../Page/エンコード.md "wikilink")とUnicodeの内部表現を明確に区別している。Unicode文字はメモリ中に保持される抽象的なオブジェクトであり、画面表示やファイルへの入出力の際には変換ルーチン（[コーデック](../Page/コーデック.md "wikilink")）を介して特定のエンコーディングのバイト列表現と相互変換する。また、ソースコード中の文字コードを認識する機能があり、これによって異なる文字コードで書かれたプログラムの動きが異なるという危険を解消している。

Pythonでは変換ルーチンをモジュールとして追加することで、さまざまなエンコーディングに対応できるようになっている。日本語の文字コード (EUC-JP, Shift_JIS, MS932, ISO-2022-JP) に対応したコーデックも作成されている。Python 2.4からは、日中韓国語用のコーデックが標準でディストリビューションに含まれるようになったため\[9\]、現在では日本語の処理に問題はほとんどなくなった。ただしGUIライブラリである[Tkinter](https://ja.wikipedia.org/wiki/Tkinter "wikilink")や[統合開発環境](../Page/統合開発環境.md "wikilink")の[IDLEは](https://ja.wikipedia.org/wiki/IDLE_\(Python\) "wikilink")、プラットフォームにもよるが、まだきちんと日本語に対応していないものもある。

ソースコードの文字コードは、ASCIIと互換性があり、Pythonが対応しているものを使用する。ソースコードのデフォルトエンコーディングは、Python 3.xではUTF-8\[10\]（ソースコード以外のPython 3のデフォルトエンコーディングは複雑になっている\[11\]\[12\]）、Python 2.xではASCIIであるが、デフォルトエンコーディング以外の文字コードを使う場合は、ソースファイルの1行目か2行目に一定の書式でコメントとして記述することになっており\[13\]、しばしば以下のように[Emacs](../Page/Emacs.md "wikilink")や[Vim](../Page/Vim.md "wikilink")などのテキストエディタにも認識可能な書式で記述される（次の例は Emacs が認識できる書式）。

``` python
#! /usr/bin/python2
# -*- coding: utf-8 -*-
s = '日本語の文字列'
```

## 利用

Pythonは全世界で使われているが、欧米の企業でもよく使われている。大企業では[マイクロソフト](../Page/マイクロソフト.md "wikilink")や[アップルなどのパッケージソフトウェア企業をはじめ](../Page/アップル_\(企業\).md "wikilink")、[Google](../Page/Google.md "wikilink")、[Yahoo\!](../Page/Yahoo!.md "wikilink")、[YouTube](https://ja.wikipedia.org/wiki/YouTube "wikilink") などの企業も利用している\[14\]。また携帯電話メーカーの[ノキア](../Page/ノキア.md "wikilink")では、S60シリーズでPythonアプリケーションが動く\[15\]。研究機関では、[NASA](../Page/アメリカ航空宇宙局.md "wikilink")\[16\]や日本の[高エネルギー加速器研究機構](../Page/高エネルギー加速器研究機構.md "wikilink")\[17\]でPythonが使われている。

適応範囲は[データサイエンス](https://ja.wikipedia.org/wiki/データサイエンス "wikilink")、[Webプログラミング](../Page/Webプログラミング.md "wikilink")、[GUIベースのアプリケーション](https://ja.wikipedia.org/wiki/グラフィカルユーザインタフェース "wikilink")、[CAD](../Page/CAD.md "wikilink")、[3Dモデリング](https://ja.wikipedia.org/wiki/3Dモデリング "wikilink")、[数式処理](https://ja.wikipedia.org/wiki/数式処理 "wikilink")など幅広い分野に及ぶ。

### データサイエンスおよび数値計算用途

[NumPy](https://ja.wikipedia.org/wiki/NumPy "wikilink")、[SciPy](../Page/SciPy.md "wikilink")などの高速な数値計算ライブラリの存在により、データサイエンスや科学技術コンピューティングにもよく用いられる。NumPy、SciPyの内部はC言語で書かれている為に動的スクリプト言語の欠点の一つである速度の遅さを補っている\[18\]。[Numba](https://ja.wikipedia.org/wiki/Numba "wikilink") を使うと、Python のコードが [LLVM](../Page/LLVM.md "wikilink") に [JITコンパイル](https://ja.wikipedia.org/wiki/JITコンパイル "wikilink")して利用可能であり、非常に高速に計算できる。[TensorFlow](https://ja.wikipedia.org/wiki/TensorFlow "wikilink") などのライブラリにより [GPU](../Page/Graphics_Processing_Unit.md "wikilink") 上で高速に計算するライブラリも充実している。

JetBrains とPythonソフトウェア財団による共同調査によると、2017年10月現在、最も主要な用途は何かというアンケートで、用途の27%がデータサイエンス（そのうち18%がデータ解析、9%が[機械学習](../Page/機械学習.md "wikilink")）である\[19\]。

### Webアプリケーション用途

[Django](../Page/Django.md "wikilink") や [Flask](https://ja.wikipedia.org/wiki/Flask "wikilink") といった[Webアプリケーションフレームワーク](../Page/Webアプリケーションフレームワーク.md "wikilink")が充実しているため、Webアプリケーション開発用途にも多く使われている。JetBrains とPythonソフトウェア財団による共同調査によると、2017年10月現在、26%の人が最も主要な用途としてWeb開発を選んだ\[20\]。

### システム管理およびグルー言語用途

[スクリプト言語](../Page/スクリプト言語.md "wikilink")としての特性から、従来[Perl](../Page/Perl.md "wikilink")や[シェルスクリプトが用いられることの多かったシステム管理用のスクリプトとして採用している](https://ja.wikipedia.org/wiki/シェル#シェルスクリプト "wikilink")[OSも複数ある](../Page/オペレーティングシステム.md "wikilink")。また、多くの異なる言語で書かれたモジュールをまとめる[グルー言語](../Page/グルー言語.md "wikilink")としての利用例も多い。実際、多くの商用[アプリケーションで](../Page/アプリケーションソフトウェア.md "wikilink") Python は組み込みのスクリプト言語として採用されている。

JetBrains とPythonソフトウェア財団による共同調査によると、2017年10月現在、9%の人が最も主要な用途として[DevOps](https://ja.wikipedia.org/wiki/DevOps "wikilink"), システム管理, 自動化スクリプトを上げた\[21\]。

### 教育用

Pythonは教育目的で設計されたわけではないが\[22\]、単純さから子供が最初に学ぶ、プログラミング教育用の言語としても利用が増えている。グイド・ヴァンロッサムはPython設計以前に教育用言語である[ABCの開発にかかわり](https://ja.wikipedia.org/wiki/ABC_\(プログラミング言語\) "wikilink")、教育用としての利用について期待感を示したこともあり、方針として非技術者向けといった利用を視野に入れているとされることもある\[23\]。

> 私の大好きなPython利用法は、騒ぎ立てずに、言語教育でプログラミングの原理を教えること。それを考えてくれ――次の世代の話だね。<cite>-- [スラッシュドット・ジャパン『 Guido van Rossum へのインタビュー』](http://slashdot.jp/story/04/07/24/1020202/)</cite>

[情報処理推進機構](../Page/情報処理推進機構.md "wikilink")(IPA)は[国家試験](../Page/国家試験.md "wikilink")の[基本情報技術者試験](../Page/基本情報技術者試験.md "wikilink")で2020年の春期試験より [COBOL](../Page/COBOL.md "wikilink") を廃止して Python を追加した\[24\]。

日本の[高等学校情報科](../Page/情報_\(教科\).md "wikilink")「情報Ⅰ」の教員向け研修教材の中で、プログラミング用言語としてPythonが使用されている\[25\]。

## 歴史

元々は[Amoebaの使用言語である](https://ja.wikipedia.org/wiki/Amoeba_\(オペレーティングシステム\) "wikilink")[ABC言語に](https://ja.wikipedia.org/wiki/ABC_\(プログラミング言語\) "wikilink")[例外処理](../Page/例外処理.md "wikilink")や[オブジェクト指向](../Page/オブジェクト指向.md "wikilink")を対応させるために作られた言語である\[26\]。

### 0.9x

[1991年](../Page/1991年.md "wikilink")にヴァンロッサムがPython 0.90の[ソースコード](../Page/ソースコード.md "wikilink")を公開した。この時点ですでにオブジェクト指向言語の特徴である[継承](../Page/継承_\(プログラミング\).md "wikilink")、[クラス](../Page/クラス_\(コンピュータ\).md "wikilink")、[例外処理](../Page/例外処理.md "wikilink")、[メソッドやさらに](../Page/メソッド_\(計算機科学\).md "wikilink")[抽象データ型](../Page/抽象データ型.md "wikilink")である[文字列](../Page/文字列.md "wikilink")、[リストの概念を利用している](../Page/リスト_\(抽象データ型\).md "wikilink")。これは[Modula-3](https://ja.wikipedia.org/wiki/Modula-3 "wikilink")の[モジュール](../Page/モジュール.md "wikilink")を参考にしていた。

### 1.x

[1994年](../Page/1994年.md "wikilink")1月、Python 1.0を公開した。主な特徴として[関数型言語](../Page/関数型言語.md "wikilink")の基本である[ラムダ計算](../Page/ラムダ計算.md "wikilink")を実装、map関数・reduce関数などを組み込んだ。

バージョン1.4では[Common Lispにある機能とよく似た](../Page/Common_Lisp.md "wikilink")[キーワード引数](https://ja.wikipedia.org/wiki/キーワード引数 "wikilink")を導入した。また簡易ながら[名前修飾](../Page/名前修飾.md "wikilink")を用いた[カプセル化](../Page/カプセル化.md "wikilink")も実装した。

### 2.x

[2000年](../Page/2000年.md "wikilink")に公開。[ガベージコレクション](../Page/ガベージコレクション.md "wikilink")や[Unicode](../Page/Unicode.md "wikilink")、[リストを導入した](../Page/リスト_\(抽象データ型\).md "wikilink")。一躍メジャーな言語となった。多くの機能は[Haskell](../Page/Haskell.md "wikilink")を参考にして導入している。

2.6以降のバージョンには、2.xから3.xへの移植を助ける「2to3 ツール」と「lib2to3 モジュール」を含んでいる\[27\]。2.7が2.xの最後のバージョンで、2.7のサポートは[2020年](../Page/2020年.md "wikilink")[1月1日](../Page/1月1日.md "wikilink")までである\[28\]。ただし、サポート終了後に 2.7.18 を2020年4月にリリースし、これが最後の 2.7.x になる。

| バージョン | リリース日\[29\] | サポート期限\[30\] |
| ----- | ----------- | ------------ |
| 2.0   | 2000年10月16日 |              |
| 2.1   | 2001年4月15日  |              |
| 2.2   | 2001年12月21日 |              |
| 2.3   | 2003年7月29日  |              |
| 2.4   | 2004年11月30日 |              |
| 2.5   | 2006年9月19日  |              |
| 2.6   | 2008年10月1日  | 2013年10月29日  |
| 2.7   | 2010年7月4日   | 2020年1月1日    |

### 3.x

[2008年](https://ja.wikipedia.org/wiki/2008年 "wikilink")、長い試験期間を経てPython 3.0が公開された。 開発初期には、西暦3000年に公開予定の理想のPythonとして、Python 3000と呼んでいた。Py3Kと略すこともある。

しかし2.xとの後方互換性が損なわれている。当初は2.xに比べて3.xが利用できるライブラリ等が著しく少ないという問題点があったが、[Django](../Page/Django.md "wikilink")など徐々に3.xに対応したフレームワークやライブラリなどが増えていったこともあり、[2016年](../Page/2016年.md "wikilink")時点においては新規のプロジェクトについて3.xで開発することが多くなっている\[31\]。JetBrains とPythonソフトウェア財団による共同調査では、Python の 2 と 3 がどっちがメインであるかというアンケートで、Python 3 がメインであると答えた人が、2016年1月は40%だったが、2017年10月は75%になった\[32\]\[33\]。

[2015年](../Page/2015年.md "wikilink")11月にリリースされた[Fedora 23](../Page/Fedora.md "wikilink")\[34\]や2016年4月にリリースされた[Ubuntu 16.04 LTS](../Page/Ubuntu.md "wikilink")\[35\]では、デフォルトでインストールされるPythonのバージョンが2.xから3.xに変更されている。[Red Hat Enterprise Linuxでは](../Page/Red_Hat_Enterprise_Linux.md "wikilink")7.5をもってPython 2が廃止予定（deprecated）となった\[36\]。

| バージョン | リリース日\[37\] | サポート期限\[38\] |
| ----- | ----------- | ------------ |
| 3.0   | 2008年12月3日  | 2009年1月13日   |
| 3.1   | 2009年6月27日  | 2012年4月9日    |
| 3.2   | 2011年2月20日  | 2016年2月20日   |
| 3.3   | 2012年9月29日  | 2017年9月29日   |
| 3.4   | 2014年3月16日  | 2019年3月18日   |
| 3.5   | 2015年9月13日  | 2020年9月      |
| 3.6   | 2016年12月23日 | 2021年12月     |
| 3.7   | 2018年6月27日  | 2023年6月      |
| 3.8   | 2019年10月14日 | 2024年10月     |

  - 3.0\[39\]

<!-- end list -->

  - print命令をprint関数へ変更
  - Unicodeを全面採用
  - 整数をint型に一本化

<!-- end list -->

  - 3.1\[40\]\[41\]

<!-- end list -->

  - 順序付き辞書
  - 単体テストフレームワーク「unittest」への機能追加
  - TkinterでのTile対応
  - import文のリファレンス実装となる、Pythonで実装したimportlibモジュール
  - ネストしたwith文に対する新たな文法

<!-- end list -->

  - 3.2\[42\]

<!-- end list -->

  - 単体テストモジュールのアップデートや拡張モジュール向け stable ABI
  - pyc レポジトリディレクトリのサポート
  - E-mail パッケージや SSL モジュールの改善
  - pdb (Python debugger) の改良

<!-- end list -->

  - 3.3
    3.1リリースから2年間、言語仕様を凍結し変更を行わない「モラトリアム期間」を解除した\[43\]。

<!-- end list -->

  - 新しい文法として、ジェネレータ関数内で別のジェネレータ関数を利用する「yield from」を追加。
  - 「u」や「U」といったプレフィックスを用いたUnicodeリテラルシンタックスを復活
  - UCS-4文字列にも対応し、文字列表現の柔軟性を強化
  - 仮想化Python実行環境を導入するためのvirtualenvパッケージの機能を「venv」機能としてコアに取り込んだ。

<!-- end list -->

  - 3.4\[44\]\[45\]

<!-- end list -->

  - オブジェクト指向ファイルシステムパスを提供する「pathlib」モジュールの提供
  - 列挙型を扱うためのenumモジュールの標準化
  - 統計関数を提供するstatisticsモジュールの導入
  - Pythonが割り当てたメモリブロックを追跡するためのデバッグツールのtracemallocモジュールの導入
  - 非同期I/Oを扱うためのフレームワークとなるasyncioモジュールの導入
  - Pythonの組み込み関数に関する分析情報を得るため機構の実装

<!-- end list -->

  - 3.5\[46\]\[47\]

<!-- end list -->

  - zipアプリケーションサポートの改良
  - byte/bytearrayオブジェクトのための「%」フォーマット対応の追加
  - 行列乗算演算子@の導入
  - 高速ディレクトリトラバーサル機能os.scandir()の導入
  - 割込がかかったシステムコールのオートリトライ機能追加
  - 近似値であるかどうかをテストする機能の導入
  - .pyoファイルの削除
  - 拡張モジュールをロードするための新しい仕組みの導入

<!-- end list -->

  - 3.6\[48\]

<!-- end list -->

  - 文字列中に式を埋め込める「Formatted string literals」の導入
  - 変数に対して型に関する情報（型ヒント）を与える「Syntax for variable annotations」の導入
  - 「async」および「await」文法でコルーチンを利用可能にする「Asynchronous generators」の導入
  - 標準ライブラリにsecretsモジュールを追加
  - DTraceおよびSystemTapプローブのサポートを追加

<!-- end list -->

  - 3.7\[49\]\[50\]

<!-- end list -->

  - 使用時点では宣言されていない型を使った型アノーテーション表記が可能となる
  - レガシーな C ロケールの抑圧、強制 UTF-8 実行モード
  - breakpoint() 関数の追加
  - dict の挿入順の保存
  - ナノ秒単位の分解能を持つ新しい時間関数の追加
  - コンテキスト変数
  - データクラス

<!-- end list -->

  - 3.8\[51\]

<!-- end list -->

  - 代入式 :=
  - 位置のみのパラメータ
  - f文字列で f'{expr=}' の形式のサポート
  - pickle プロトコル5
  - dict での reversed のサポート

### Python の時系列

  - 1990年代始め - [オランダ](https://ja.wikipedia.org/wiki/オランダ "wikilink")にある[Stichting Mathematisch Centrum (CWI)](https://www.cwi.nl/)で、グイド・ヴァンロッサムによってPythonの初期バージョンが作成される。
  - 1995年 - ヴァンロッサムは米国ヴァージニア州レストンにある[Corporation for National Research Initiatives (CNRI)](https://www.cnri.reston.va.us/) に移動。ここでPythonの開発に携わり、いくつかのバージョンを公開する。
  - 2000年3月 - ヴァンロッサムとPythonのコア開発チームは BeOpen.com に移り、BeOpen PythonLabs チームを結成する。同年10月、PythonLabsチームはDigital Creations (現在の[Zope Corporation](http://www.zope.com/)) に移る。
  - 2001年 - Pythonに関する知的財産を保有するための非営利組織[Pythonソフトウェア財団](https://ja.wikipedia.org/wiki/Pythonソフトウェア財団 "wikilink") (PSF) が立ち上がる。このときZope CorporationはPSFの賛助会員となる。

### Pythonに影響を与えた言語

  - [ABC](https://ja.wikipedia.org/wiki/ABC_\(プログラミング言語\) "wikilink")（[インデントによる構文](../Page/字下げ.md "wikilink")）
  - [Modula-2](https://ja.wikipedia.org/wiki/Modula-2 "wikilink"), [-3](https://ja.wikipedia.org/wiki/Modula-3 "wikilink")（モジュール機能、オブジェクト指向）
  - [Icon](../Page/Icon.md "wikilink")（辞書、スライス演算子など）
  - [SETL](https://ja.wikipedia.org/wiki/SETL "wikilink")（リストの内包表現）
  - [C](../Page/C言語.md "wikilink"), [C++](../Page/C++.md "wikilink")（基本的な構文）
  - [Smalltalk](../Page/Smalltalk.md "wikilink")（仮想マシン機構、動的性）
  - [Lisp](https://ja.wikipedia.org/wiki/LISP "wikilink"), [Scheme](../Page/Scheme.md "wikilink")（[関数型言語](../Page/関数型言語.md "wikilink")の機能）

## Webアプリケーションフレームワーク

  - [Bottle](https://ja.wikipedia.org/wiki/Bottle "wikilink")（ボトル） - <https://bottlepy.org/docs/dev/>
  - [CherryPy](../Page/CherryPy.md "wikilink")（チェリーパイ） - <https://cherrypy.org/>
  - [Django](../Page/Django.md "wikilink")（ジャンゴ） - <https://www.djangoproject.com/>
  - [Flask](https://ja.wikipedia.org/wiki/Flask "wikilink")（フラスク） - <http://flask.pocoo.org/>
  - [Pyramid](https://ja.wikipedia.org/wiki/Pylons#Pyramid "wikilink")（ピラミッド） - <https://pylonsproject.org/projects/pyramid/>
  - [Plone](https://ja.wikipedia.org/wiki/Plone "wikilink")（プローン） - <https://plone.org/>
  - [Tornado (Webサーバ)](https://ja.wikipedia.org/wiki/Tornado_\(Webサーバ\) "wikilink")（トルネード） - <https://sites.google.com/site/tornadowebja/>
  - [Cyclone（C10K問題対応)](https://ja.wikipedia.org/wiki/Cyclone（C10K問題対応\) "wikilink")（サイクロン） - <http://cyclone.io/>

## パッケージ管理システムおよびディストリビューション

  - [pip](https://ja.wikipedia.org/wiki/pip "wikilink")
  - [Anaconda (Pythonディストリビューション)](https://ja.wikipedia.org/wiki/Anaconda_\(Pythonディストリビューション\) "wikilink")
  - [EasyInstall](https://ja.wikipedia.org/wiki/EasyInstall "wikilink")

## 脚注

</ref> \[52\] \[53\] \[54\] \[55\] \[56\] \[57\] \[58\] \[59\] \[60\] }}

## 関連項目

  - [IPython](https://ja.wikipedia.org/wiki/IPython "wikilink") - Pythonの[スニペット](https://ja.wikipedia.org/wiki/スニペット "wikilink")を実行できるノートパッド
  - [MyHDL](https://ja.wikipedia.org/wiki/MyHDL "wikilink") - Python言語ベースのハードウェア記述言語
  - [スクリプト言語](../Page/スクリプト言語.md "wikilink")
  - [オブジェクト指向プログラミング](../Page/オブジェクト指向プログラミング.md "wikilink")

## 外部リンク

  -

  - [日本Pythonユーザ会](https://www.python.jp/) - マニュアル日本語訳の配布

  - [Python awesome](https://pythonawesome.com/)

  - [Allen Downey、相川利樹(訳):「Think Python：コンピュータサイエンティストのように考えてみよう」](https://cauldron.sakura.ne.jp/thinkpython/thinkpython/ThinkPython.pdf)

  - 喜多一, 「[プログラミング演習 Python 2019](https://hdl.handle.net/2433/245698)」 2020年 p.1-200

  - [Pythonプログラミング入門](https://utokyo-ipp.github.io/toc.html) 東京大学

[Category:オブジェクト指向言語](https://ja.wikipedia.org/wiki/Category:オブジェクト指向言語 "wikilink") [Category:スクリプト言語](https://ja.wikipedia.org/wiki/Category:スクリプト言語 "wikilink") [Category:オープンソースソフトウェア](https://ja.wikipedia.org/wiki/Category:オープンソースソフトウェア "wikilink") [Category:Python](https://ja.wikipedia.org/wiki/Category:Python "wikilink") [Category:基本情報技術者試験](https://ja.wikipedia.org/wiki/Category:基本情報技術者試験 "wikilink")

1.
2.
3.  Windows (MS)にPython (Anaconda)を導入する（6つの罠） <https://qiita.com/kaizen_nagoya/items/7bfd7ecdc4e8edcbd679>
4.  <https://github.com/iodide-project/pyodide>
5.
6.
7.  TIMTOWTDI。
8.
9.
10. [PEP 3120 -- Using UTF-8 as the default source encoding | Python.org](https://www.python.org/dev/peps/pep-3120/)
11. [PEP 538 -- Coercing the legacy C locale to a UTF-8 based locale | Python.org](https://www.python.org/dev/peps/pep-0538/)
12. [PEP 540 -- Add a new UTF-8 Mode | Python.org](https://www.python.org/dev/peps/pep-0540/)
13.
14.
15.
16.
17.
18.
19.
20.
21.
22.
23.
24. [プレス発表 基本情報技術者試験における出題を見直し：IPA 独立行政法人 情報処理推進機構](https://www.ipa.go.jp/about/press/20190124.html)
25. [文部科学省](../Page/文部科学省.md "wikilink")初等中等教育局情報教育・外国語教育課 [高等学校情報科「情報Ⅰ」教員研修用教材（本編）](http://www.mext.go.jp/a_menu/shotou/zyouhou/detail/1416756.htm)「[第3章 コンピューターとプログラミング](http://www.mext.go.jp/component/a_menu/education/micro_detail/__icsFiles/afieldfile/2019/05/15/1416758_005.pdf)」(2019年5月)
26.
27.
28. [PEP 373 -- Python 2.7 Release Schedule | Python.org](https://www.python.org/dev/peps/pep-0373/)
29.
30.
31.
32. [Python Developers Survey 2017 - Results](https://www.jetbrains.com/research/python-developers-survey-2017/)
33. [By the numbers: Python community trends in 2017/2018 | Opensource.com](https://opensource.com/article/18/5/numbers-python-community-trends)
34.
35.
36. [Red Hat Enterprise Linux 7 Chapter 53. Deprecated Functionality - Red Hat Customer Portal](https://access.redhat.com/documentation/en-us/red_hat_enterprise_linux/7/html/7.5_release_notes/chap-red_hat_enterprise_linux-7.5_release_notes-deprecated_functionality_in_rhel7)
37.
38. [17. Development Cycle — Python Developer's Guide](https://devguide.python.org/devcycle/#end-of-life-branches)
39.
40.
41.
42.
43.
44.
45.
46.
47.
48.
49.
50. [What's New In Python 3.7 — Python 3.7.5 ドキュメント](https://docs.python.org/ja/3.7/whatsnew/3.7.html)
51. [What's New In Python 3.8 — Python 3.8.0 ドキュメント](https://docs.python.org/ja/3/whatsnew/3.8.html)
52.
53. , second section "Fans of Python use the phrase "batteries included" to describe the standard library, which covers everything from asynchronous processing to zip files."
54.
55. <http://www.rakunet.org/tsnet/TSpython/35/1067.html>
56.
57.
58. [What’s New in Python 2.4](http://docs.python.org/whatsnew/2.4.html#new-improved-and-deprecated-modules)
59.
60.
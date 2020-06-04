> この記事は[Mathematica](https://ja.wikipedia.org/wiki/Mathematica)から翻訳されています。


**Mathematica**（マセマティカ）は、[スティーブン・ウルフラム](../Page/スティーブン・ウルフラム.md "wikilink")が考案し広く使われている[数式処理システム](../Page/数式処理システム.md "wikilink")。[ウルフラム・リサーチ](../Page/ウルフラム・リサーチ.md "wikilink")の、ウルフラムが率いる[数学者](../Page/数学者.md "wikilink")と[プログラマ](../Page/プログラマ.md "wikilink")のチームが開発し、同社（[日本国内はヒューリンクス等の正規認定販売代理店](http://www.wolfram.com/company/contact/global-sales/)）により販売されている。Mathematicaは[項書き換え](../Page/項書き換え.md "wikilink")を基本として、複数のパラダイムをエミュレートする[プログラミング言語](../Page/プログラミング言語.md "wikilink")としても強力である。

## 概要

[ウルフラム・リサーチ](../Page/ウルフラム・リサーチ.md "wikilink")の創始者である[スティーブン・ウルフラム](../Page/スティーブン・ウルフラム.md "wikilink")と彼のチームは、1986年から新たな[数式処理システム](../Page/数式処理システム.md "wikilink")の開発を開始し、1988年にその最初のバージョンをリリースした。ウルフラムは当初、このシステムをOmega、のちにPolyMathと呼んでいたが、当時[NeXT](../Page/NeXT.md "wikilink")社の社長であった[スティーブ・ジョブズ](../Page/スティーブ・ジョブズ.md "wikilink")に相談したところ「ダサい名前だ」と一蹴され、なにか一般的な語をロマンチックに表現したもの、例えば[トリニトロン](../Page/トリニトロン.md "wikilink")のような名前が良いとして「Mathematica」と名付けられた\[1\]。

歴代のMathematicaのロゴに使われているのは「スパイキー」と呼ばれる三次元多面体で、初代 Mathematicaでは[大二十面体](../Page/大二十面体.md "wikilink")、それ以降のバージョンでは双曲二十面体を装飾したものが使われている\[2\]\[3\]。

プログラミング言語としてのMathematicaは、[項書き換え](../Page/項書き換え.md "wikilink")を基本として[関数型と](../Page/関数型言語.md "wikilink")[手続き型の両方をサポートする](https://ja.wikipedia.org/wiki/手続き型言語 "wikilink")[マルチパラダイム・プログラミング言語である](https://ja.wikipedia.org/wiki/マルチパラダイムプログラミング言語 "wikilink")。Mathematicaは、ウルフラムらが1979年頃に開発した [Symbolic Manipulation Program](https://ja.wikipedia.org/wiki/:en:Symbolic_Manipulation_Program "wikilink") を起源とし\[4\]、[プログラミング言語](../Page/プログラミング言語.md "wikilink")[ALGOL](../Page/ALGOL.md "wikilink")・[LISP](https://ja.wikipedia.org/wiki/LISP "wikilink")・[APL](../Page/APL.md "wikilink")、および[数式処理システム](../Page/数式処理システム.md "wikilink")[Macsyma](../Page/Macsyma.md "wikilink")の影響を受けている\[5\]\[6\]。

Mathematicaは[C](../Page/C言語.md "wikilink")/[C++](../Page/C++.md "wikilink")および[Java](https://ja.wikipedia.org/wiki/Java "wikilink")で実装されているが、拡張可能な[ライブラリ](../Page/ライブラリ.md "wikilink")はすべて[Wolfram言語で書かれている](https://ja.wikipedia.org/wiki/Wolfram_\(プログラミング言語\) "wikilink")。実際、新しいコード（Wolfram言語で書かれた[テキストファイル](../Page/テキストファイル.md "wikilink")）はMathematicaの「パッケージ（.mファイル）」として追加される。Mathematicaには4,000以上の高度に洗練された組み込み関数が用意されており\[7\]、それらをビルディング・ブロックとして組み合わせていくことで、簡単にプログラムを作ることができる。

システムとしてのMathematicaは、Wolfram言語を解釈し実際に計算を実行する「[カーネル](../Page/カーネル.md "wikilink")」と、その計算結果を表示する「[フロントエンド](../Page/フロントエンド.md "wikilink")」の2つの部分から構成される。カーネルとフロントエンドの間の通信には「[MathLink](http://www.wolfram.com/solutions/mathlink/mathlink.html)」プロトコルが使われる。

Mathematica日本語版の最新バージョンは 12.1（2020年5月リリース）で、様々なコンピュータシステム上で利用可能となっている。

## 機能

[thumb](https://ja.wikipedia.org/wiki/ファイル:Mathematica_dinis_surface.png "wikilink") Mathematicaには次のような機能がある\[8\]。

  - コアとなる言語
      - [手続き型と](../Page/手続き型プログラミング.md "wikilink")[関数型をサポートする](../Page/関数型言語.md "wikilink")[マルチパラダイム・プログラミング言語](https://ja.wikipedia.org/wiki/マルチパラダイムプログラミング言語 "wikilink")
      - 文字列操作、[正規表現](../Page/正規表現.md "wikilink")や意味解析を含めた[テキストマイニング](../Page/テキストマイニング.md "wikilink")ツール
      - [並列プログラミング用ツール](../Page/並列化.md "wikilink")
  - [数学](../Page/数学.md "wikilink")と[アルゴリズム](../Page/アルゴリズム.md "wikilink")
      - [初等関数](../Page/初等関数.md "wikilink")、[特殊関数](https://ja.wikipedia.org/wiki/特殊関数 "wikilink")、[数論](../Page/数論.md "wikilink")、[群論](https://ja.wikipedia.org/wiki/群論 "wikilink")のライブラリ
      - [複素数](../Page/複素数.md "wikilink")、[任意精度](../Page/任意精度演算.md "wikilink")、[区間演算](https://ja.wikipedia.org/wiki/区間演算 "wikilink")、記号計算のサポート
      - 連続的/離散的計算のための数値と記号のツール
      - [疎行列](../Page/疎行列.md "wikilink")を含む行列とデータの操作ツール
      - [常微分方程式](../Page/常微分方程式.md "wikilink") (ODE)、[偏微分方程式](../Page/偏微分方程式.md "wikilink") (PDE)、 (DAE)、 (DDE)、[ディオファントス方程式](../Page/ディオファントス方程式.md "wikilink")、[漸化式](https://ja.wikipedia.org/wiki/漸化式 "wikilink")のソルバー
      - 連続[積分変換](https://ja.wikipedia.org/wiki/積分変換 "wikilink")および離散[積分変換](https://ja.wikipedia.org/wiki/積分変換 "wikilink")
      - [直線/曲線あてはめ](https://ja.wikipedia.org/wiki/曲線あてはめ "wikilink")、[仮説検定](../Page/仮説検定.md "wikilink")、100種類以上の[確率分布](../Page/確率分布.md "wikilink")における確率や期待値の計算
      - 制約のある/ない、局所/大域、[最適化](../Page/最適化問題.md "wikilink")
      - [組み合わせ問題のためのツール](../Page/組合せ最適化.md "wikilink")
      - [制御系ライブラリ](../Page/制御システム.md "wikilink")
      - [債券](../Page/債券.md "wikilink")、[年金](../Page/年金.md "wikilink")、[デリバティブ](../Page/デリバティブ.md "wikilink")、[オプション取引](../Page/オプション取引.md "wikilink")を含む金融計算ツール
  - [可視化](../Page/可視化.md "wikilink")と[グラフィックス](https://ja.wikipedia.org/wiki/グラフィックス "wikilink")
      - [2D](../Page/2次元.md "wikilink")/[3D](../Page/3次元.md "wikilink") のデータや関数の[可視化](../Page/可視化.md "wikilink")とアニメーション化ツール
      - [グラフの視覚化ツールおよび解析ツール](../Page/グラフ理論.md "wikilink")
  - データの操作
      - データ、画像、動画、音響、[CAD](../Page/CAD.md "wikilink")、[GIS](../Page/地理情報システム.md "wikilink")、文書、生物医学などの各種フォーマットのインポート/エクスポート
      - [画像認識を含む](../Page/コンピュータビジョン.md "wikilink")[画像処理](../Page/画像処理.md "wikilink")と[形態学的画像処理のツール](https://ja.wikipedia.org/wiki/数理形態学 "wikilink")
      - 音響/画像データの[ウェーブレット](../Page/ウェーブレット.md "wikilink")解析用ライブラリ
      - [データ・クラスタリング](https://ja.wikipedia.org/wiki/データ・クラスタリング "wikilink")、[シーケンスアラインメント](../Page/シーケンスアラインメント.md "wikilink")、[パターンマッチなどの](../Page/パターンマッチング.md "wikilink")[データマイニング](../Page/データマイニング.md "wikilink")ツール
  - 計算可能なデータ
      - [数学](../Page/数学.md "wikilink")、[科学](../Page/科学.md "wikilink")、[地理](../Page/地理.md "wikilink")、[経済](../Page/経済.md "wikilink")、[言語学](../Page/言語学.md "wikilink")データベースへのアクセス
      - [気象](../Page/気象.md "wikilink")、[金融](../Page/金融.md "wikilink")の履歴およびリアルタイムデータの取得
      - [WolframAlphaのデータへのアクセスと計算](https://ja.wikipedia.org/wiki/Wolfram_Alpha "wikilink")
  - 動的インタラクティブ機能
      - 式やグラフィックスのインタラクティブな操作
      - 計算とアプリケーションのための[ユーザインタフェース](../Page/ユーザインタフェース.md "wikilink")を追加するツール
  - ノートブックとドキュメント
      - ノートブックによるインタラクティブなドキュメントの作成
      - Wolfram言語 と [自然言語](../Page/自然言語.md "wikilink")ユーザインタフェースによる入力
      - [数式エディタ](https://ja.wikipedia.org/wiki/数式エディタ "wikilink")と自動報告書生成を含む科学技術用ワードプロセッシング
      - [PDF](../Page/Portable_Document_Format.md "wikilink")、[LaTeX](../Page/LaTeX.md "wikilink")、[HTML](../Page/HyperText_Markup_Language.md "wikilink")、[XMLへの書き出し](../Page/Extensible_Markup_Language.md "wikilink")、プレゼンテーション用[スライドショー](../Page/スライドショー.md "wikilink")の作成
  - システムインタフェースと配備
      - [C](../Page/C言語.md "wikilink")、[Java](https://ja.wikipedia.org/wiki/Java "wikilink")、[.NET](https://ja.wikipedia.org/wiki/.NET_Framework "wikilink")、[R](../Page/R言語.md "wikilink")、[SQL](../Page/SQL.md "wikilink")、HTML、XMLなど各言語との接続・連携
      - [CUDA](../Page/CUDA.md "wikilink")、[OpenCL](../Page/OpenCL.md "wikilink")による[GPUコンピューティングと](../Page/Graphics_Processing_Unit.md "wikilink")[並列計算](../Page/並列計算.md "wikilink")

## インタフェース

システムとしてのMathematicaは、ユーザーとの対話を行う「[フロントエンド](../Page/フロントエンド.md "wikilink")」と、演算を実行する「[カーネル](../Page/カーネル.md "wikilink")」の2つの部分から構成される。フロントエンドはMathematicaシステムの[GUIを担当する部分で](https://ja.wikipedia.org/wiki/グラフィカルユーザインタフェース "wikilink")、自動構文カラーリング、入力補完、デバッガなどの開発ツールの機能がある。また、一般的なワードプロセッシング機能の大部分もサポートしている。

フロントエンドとカーネルは互いに独立に起動し、「[MathLink](http://www.wolfram.com/solutions/mathlink/mathlink.html)」と呼ばれるプロトコルを使って通信している。実際、Mathematicaを起動した時点ではカーネルは起動しておらず、フロントエンドで最初の計算が実行された時にはじめてカーネルが起ち上がる。

### ノートブック

Mathematicaの標準的なフロントエンドである「ノートブック」は対話型のドキュメントで、データ・数式・テキスト・コード・演算結果・グラフィックス・表・GUIコンポーネント・アニメーション・音声などを混在させることができる。ノートブックは[ウルフラム・リサーチ](../Page/ウルフラム・リサーチ.md "wikilink")の共同創始者であるによって設計され、Mathematica 2.0より採用された。

一つのノートブックの中でデータの処理から可視化、さらに文書作成までをシームレスに行えることが、Mathematicaの最大の利点の一つである。ノートブックにおいては、ユーザーの入力（テキストと Wolframコード）やカーネルの演算結果（グラフィックやサウンドも含む）は、すべて階層化された「セル」に納められ、文書のアウトライン化やセクション分割が容易に行える。

ノートブックの中身はすべてWolfram言語で記述されており、それ自体を Wolfram 言語で生成・修正・解析することが可能である。ノートブックから[TeX](../Page/TeX.md "wikilink")やXMLなどの他のフォーマットへの変換は、この機能を用いた構文解析を通じて実現されている。

### 代替フロントエンド

Mathematica標準のノートブック以外にも、代替のフロントエンドが存在する。2006年には[Eclipseベースの](../Page/Eclipse_\(統合開発環境\).md "wikilink")[IDE](../Page/統合開発環境.md "wikilink")、[Wolfram Workbench](http://www.wolfram.com/products/workbench/)が登場した。プロジェクトベースのコード開発ツールとなっており、リビジョン管理、デバッグ、プロファイル、評価などの機能がある。またMathematicaには、テキスト型インタフェースが同梱されており、[UNIX](../Page/UNIX.md "wikilink")コマンドラインから直接カーネルを呼び出し対話することも可能である\[9\]。

## 計算可能なデータ

[MathematicaWind.png](https://ja.wikipedia.org/wiki/File:MathematicaWind.png "fig:MathematicaWind.png") Mathematicaには一貫したフレームワークで管理されたデータ群が含まれており、即座に計算に使用できる。それらデータはモデル評価などの目的でプログラムから使用でき、ウルフラム・リサーチにあるデータサーバに自動アクセスして最新データに更新できる\[10\]。株価や気象などのデータはリアルタイムに配信される。

計算可能なデータには次のようなものがある。

  - 数学データ: 195の[多面体](../Page/多面体.md "wikilink")の98種類の属性データ、5300の[グラフ](https://ja.wikipedia.org/wiki/グラフ "wikilink")の282種類の属性データ、6つの[結び目の](https://ja.wikipedia.org/wiki/結び目理論 "wikilink")64種類の属性データ、21の[格子の](https://ja.wikipedia.org/wiki/結晶格子 "wikilink")38種類の属性データ
  - 化学データ: 44,000 の[化合物](../Page/化合物.md "wikilink")の101種類の属性データ、118の[元素](../Page/元素.md "wikilink")の86種類の属性データ、1000の[亜原子粒子](https://ja.wikipedia.org/wiki/亜原子粒子 "wikilink")の35種類の属性データ、3200の[同位体](../Page/同位体.md "wikilink")の33種類の属性データ
  - 天文学データ: 52の[測地座標系の](../Page/測地系.md "wikilink")32種類の属性データ、156,000 の[天体](../Page/天体.md "wikilink")の99種類の属性データ
  - 地政学データ: 240カ国の223種類の属性データ、164,000の世界各地の都市の14種類の属性データ
  - 言語データ: 149,000の英単語の37種類の属性データ、他の26の言語の辞書
  - 生命科学データ: 40,000の[ヒト遺伝子の](../Page/ヒトゲノム.md "wikilink")41種類の属性データ、27,000の[タンパク質](../Page/タンパク質.md "wikilink")の30種類の属性データ
  - 金融データ: 146,000の銘柄や金融商品の74の属性データ（履歴とリアルタイム）
  - 気象データ: 22,000の世界各地の観測地点における43の属性データ（履歴とリアルタイム）

<!-- end list -->

  - Wolfram Alphaのデータ: [Wolfram Alphaからの兆を越える多数のデータ](https://ja.wikipedia.org/wiki/Wolfram_Alpha "wikilink")

## 高性能計算

1999年のバージョン4でパックアレー\[11\]、2003年のバージョン5で[疎行列](../Page/疎行列.md "wikilink")を導入し\[12\]、[GNU Multi-Precision Library](https://ja.wikipedia.org/wiki/GNU_Multi-Precision_Library "wikilink") を採用して高精度演算が可能となり、[高性能計算](../Page/高性能計算.md "wikilink")向け機能が拡張された。

バージョン5.2 (2005) では、[マルチコア](../Page/マルチコア.md "wikilink")コンピュータ上で動作する際に自動的に[マルチスレッド化する機能を追加した](../Page/スレッド_\(コンピュータ\).md "wikilink")\[13\]。このバージョンから CPU 毎に最適化されたライブラリを採用している。また、[ClearSpeed](https://ja.wikipedia.org/wiki/:en:ClearSpeed "wikilink") などのサードパーティ製高速化ハードウェアが Mathematica をサポートしている\[14\]。

2002年、異機種混在型クラスターやマルチプロセッサシステムでのユーザレベルの[並列計算](../Page/並列計算.md "wikilink")を可能にする [gridMathematica](https://ja.wikipedia.org/wiki/:en:gridMathematica "wikilink") をリリース\[15\]。2008年には、並列計算技術は通常の Mathematica ライセンスに含まれるようになり、[Windows HPC Server 2008](https://ja.wikipedia.org/wiki/:en:Windows_HPC_Server_2008 "wikilink")、[Microsoft Compute Cluster Server](../Page/Microsoft_Windows_Server_2003.md "wikilink")、[Sun Grid](https://ja.wikipedia.org/wiki/:en:Sun_Grid "wikilink") をサポートするようになった。

2010年から[CUDA](../Page/CUDA.md "wikilink")および[OpenCL](../Page/OpenCL.md "wikilink")対応の[GPUハードウェアをサポート](../Page/Graphics_Processing_Unit.md "wikilink")。またバージョン8では[C言語](../Page/C言語.md "wikilink")コードを生成でき、[Intel C++ Compilerや](../Page/Intel_C++_Compiler.md "wikilink")[Visual Studio 2010のコンパイラで動的にコンパイルできる](https://ja.wikipedia.org/wiki/Microsoft_Visual_Studio "wikilink")。

## 他のアプリケーションとの接続

[MathLink](http://www.wolfram.com/solutions/mathlink/mathlink.html)プロトコルは、Mathematicaのカーネルとフロントエンド間の通信だけでなく、任意のアプリケーションとカーネルとの通信にも使われる。Mathematicaは豊富な機能を備えているが、他のプログラムの機能を利用したり、古いコードにアクセスするためにいくつかのインタフェースが開発されてきた。

### C、Java、.NET、データベース、Rとの接続

ウルフラム・リサーチはMathematicaカーネルとのMathLinkによる通信を行うアプリケーション開発者向けに[C言語](../Page/C言語.md "wikilink")での開発キットを無料で配布している\[16\]。

[J/Link](http://reference.wolfram.com/mathematica/JLink/tutorial/Overview.html)と[.NET/Link](http://reference.wolfram.com/mathematica/NETLink/tutorial/Overview.html)は、それぞれMathLinkをベースにしたJavaおよび.NET用のコンポーネントである。J/Link を使うと、JavaプログラムからMathematicaに計算を依頼することができ、MathematicaプログラムがJavaの[クラスをロードし](../Page/クラス_\(コンピュータ\).md "wikilink")、Javaオブジェクトを操作したりメソッドを呼び出したりできる。そうすると、例えばMathematicaから Java の [GUIを構築できる](https://ja.wikipedia.org/wiki/グラフィカルユーザインターフェース "wikilink")。同様に、.NET/Linkを使えば.NETプログラムと同様のことが可能になる。

[DatabaseLink](http://reference.wolfram.com/mathematica/DatabaseLink/tutorial/Overview.html)は[SQL](../Page/SQL.md "wikilink")データベースを扱うためのツールキットで、[JDBC](../Page/JDBC.md "wikilink")接続と[ODBC接続をサポートしている](../Page/Open_Database_Connectivity.md "wikilink")。[RLink](http://reference.wolfram.com/mathematica/RLink/guide/RLink.html)は統計解析向けプログラミング言語[Rと交信し](../Page/R言語.md "wikilink") Mathematica内からRのコードを実行するもので、バージョン9から正式にサポートされた。

### その他の接続

その他にMathematicaと接続できるプログラミング言語としては、[Haskell](../Page/Haskell.md "wikilink")\[17\]、[AppleScript](../Page/AppleScript.md "wikilink")\[18\]、[Racket](https://ja.wikipedia.org/wiki/Racket "wikilink")\[19\]、[Visual Basic](https://ja.wikipedia.org/wiki/Microsoft_Visual_Basic "wikilink")\[20\]、[Python](../Page/Python.md "wikilink")\[21\]、[Clojure](https://ja.wikipedia.org/wiki/Clojure "wikilink")\[22\]がある。数学関係のソフトウェアでは、[OpenOffice.org Calc](../Page/OpenOffice.org.md "wikilink")\[23\]、 [Microsoft Excel](https://ja.wikipedia.org/wiki/Microsoft_Excel "wikilink")\[24\]、[MATLAB](../Page/MATLAB.md "wikilink")\[25\]\[26\]\[27\]、[SINGULAR](https://ja.wikipedia.org/wiki/SINGULAR_\(数式処理システム\) "wikilink")\[28\]、[Origin](../Page/Origin_\(グラフ作成ソフト\).md "wikilink")\[29\]に接続可能である。

Mathematicaはリアルタイムのデータストリームを受け付けることもでき、[LabVIEW](../Page/LabVIEW.md "wikilink")\[30\]、金融関係用\[31\]、GPIB (IEEE 488)\[32\]、[USB](../Page/ユニバーサル・シリアル・バス.md "wikilink")\[33\]、シリアル接続\[34\]などの方法がある。[HIDデバイスからの入力を自動的に検出して読み込むこともできる](../Page/ヒューマン・インタフェース・デバイス.md "wikilink")。最近では[LEGO マインドストームで作ったロボットを](../Page/MINDSTORMS.md "wikilink")[Bluetooth](../Page/Bluetooth.md "wikilink")通信を介して操作する試みもなされている\[35\]。

2014年1月6日、ウルフラム・リサーチは、Wolfram言語と外部装置の接続利用促進に向けたプロジェクト[Wolfram Connected Devices Project](http://devices.wolfram.com/)を起ち上げた\[36\]\[37\]。

## アプリケーション配布

Mathematicaで書かれたアプリケーションを配布するための手段がいくつか用意されている。

  - [Wolfram CDF Player](https://ja.wikipedia.org/wiki/CDF_Player "wikilink")
      - [計算可能ドキュメント形式](https://ja.wikipedia.org/wiki/計算可能ドキュメント形式 "wikilink") (CDF) でセーブされ Mathematicaプログラムを実行できる[無料](../Page/無料.md "wikilink")のプレイヤーである。
      - 代表的なウェブブラウザへのプラグインも含まれている。
      - Mathematicaの標準形式のファイルも閲覧可能だが、実行はできない。
  - [Wolfram Player Pro](http://www.wolfram.com/player-pro/)
      - Mathematicaのアプリケーションを実行可能なランタイム版Mathematicaである。
      - コードの作成・編集はできない。
  - [webMathematica](http://www.wolfram.com/products/webmathematica/)
      - ウェブブラウザがリモートのMathematicaサーバのフロントエンドとして機能できるようにする。
      - ユーザーの書いたアプリケーションにブラウザ経由で任意のプラットフォームからアクセスすることを可能にする。
      - Mathematicaへの完全なアクセスを提供することはできない。

Mathematicaのコードは[C言語](../Page/C言語.md "wikilink")のコードに変換したり、[DLL](../Page/ダイナミックリンクライブラリ.md "wikilink") を自動生成することも可能である。また、閲覧に限ったファイルの共有にはHTMLやLaTeX書式での出力が便利である。数式は[MathMLに変換することで他のソフトウェアとやりとりできる](../Page/Mathematical_Markup_Language.md "wikilink")。

## 対応プラットフォームとライセンス

Mathematica 10は、[Microsoft Windows](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")（Vista・7・8）、[macOS](https://ja.wikipedia.org/wiki/macOS "wikilink")（10.6〜10.10）、[Linux](../Page/Linux.md "wikilink")の各種バージョンで動作する\[38\]。どのプラットフォームも[64ビット](https://ja.wikipedia.org/wiki/64ビット "wikilink")版をサポートしている。過去にサポートしていたOSとしては、[NeXTSTEP](../Page/NEXTSTEP.md "wikilink")、[Solaris](../Page/Solaris.md "wikilink")、[AIX](../Page/AIX.md "wikilink")、[Convex](../Page/コンベックス・コンピュータ.md "wikilink")、[HP-UX](../Page/HP-UX.md "wikilink")、[IRIX](../Page/IRIX.md "wikilink")、[MS-DOS](../Page/MS-DOS.md "wikilink")、[OS/2](https://ja.wikipedia.org/wiki/OS/2 "wikilink")、[Ultrix](../Page/Ultrix.md "wikilink")、[Windows Me](../Page/Microsoft_Windows_Millennium_Edition.md "wikilink")、[Windows XPなどがある](../Page/Microsoft_Windows_XP.md "wikilink")。

### ライセンス

Mathematicaは[プロプライエタリなシステムであり](../Page/プロプライエタリ・ソフトウェア.md "wikilink")\[39\]、設定価格は比較的高めである。日本での商用版シングルユーザーライセンスの販売価格は423,500円で、これには、並列計算用の追加のカーネル、1年間のプレミアサービス、家庭での利用を許可するライセンス、[Wolfram Lightweight Grid Manager](http://www.wolfram.com/lightweight-grid-manager/)、[Wolfram Workbench](http://www.wolfram.com/products/workbench/)、[webMathematica Amateur Edition](http://www.wolfram.com/products/webmathematica/)のライセンスが含まれる\[40\]。一方で、政府機関、非営利組織、教育機関、学生、家庭用に向けては低価格を設定している\[41\]。例えば、学生向けの製品（内容は正規品と同じ）は正規価格の5%程度で購入できる\[42\]。教育機関向けライセンスで契約した場合、学生は家庭でもMathematicaを利用可能である。指定された数の Mathematica をネットワーク上で同時に起動できるネットワークライセンスも用意されている\[43\]。

Mathematicaの価格設定は地域によっても大きく異なる。米国においては、商用版2,745ドル、学生版140ドル（日本では25,000円）、家庭版295ドル（日本では67,000円）となっている。日米での価格差は、電話対応を含め、国内宛に日本語で問い合わせができる点や、日本語技術サポート、有償セミナーの半額割引（一部代理店のみ）等のサービスの差により生じている。

### 無料バンドル

2013年11月21日、ウルフラム・リサーチとラズベリーパイ財団は、すべての[Raspberry PiにWolfram言語とMathematica](https://ja.wikipedia.org/wiki/Raspberry_Pi "wikilink") 10の[パイロット版](../Page/パイロット版.md "wikilink")を無料でバンドルすることを発表した\[44\]\[45\]。これにより、Raspberry Piの計算速度の問題は残るものの、Mathematicaの全機能を実質25ドル（Raspberry Pi Model A のボード1枚の価格）で利用できることになった。Mathematicaがコンピュータに無料でバンドルされるのは、1988年の[NeXT](../Page/NeXT.md "wikilink")以来、25年ぶり2度目の出来事である。

2014年1月6日、ウルフラム・リサーチと[インテル](https://ja.wikipedia.org/wiki/インテル "wikilink")は、2014年夏頃に発売予定の[SD カードサイズコンピュータ](https://ja.wikipedia.org/wiki/SDメモリーカード "wikilink") [Intel EdisonにWolfram言語とMathematicaを標準搭載すると発表した](https://ja.wikipedia.org/wiki/Intel_Edison "wikilink")\[46\]。

## リリース履歴

ウルフラム・リサーチからリリースされたMathematicaのバージョンは以下の通り\[47\]:

| バージョン              | リリース日       | 主な新機能                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| ------------------ | ----------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| Mathematica 1.0    | 1988年6月23日  | 初代 Mathematica。[Macintosh](../Page/Macintosh.md "wikilink")のサポート。[NeXT](../Page/NeXT.md "wikilink")社製のすべてのコンピュータに[バンドル](https://ja.wikipedia.org/wiki/バンドル "wikilink")。                                                                                                                                                                                                                                                                                                                                                                                |
| Mathematica 1.2    | 1989年8月1日   | [Macintosh](../Page/Macintosh.md "wikilink") フロントエンド。リモートカーネル。初歩的微分方程式の求解。StatisticsおよびGraphicsパッケージの追加。[3D グラフィックスの新しいオプションと機能の追加](../Page/3次元コンピュータグラフィックス.md "wikilink")。                                                                                                                                                                                                                                                                                                                                                                           |
| Mathematica 2.0    | 1991年1月15日  | MathLinkプロトコル。標準フロントエンド「ノートブック」。グラフィックスの装飾機能の追加。文字列・ファイル操作。                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| Mathematica 2.1    | 1992年6月15日  | [Macintosh](../Page/Macintosh.md "wikilink")用MathLink。[Windows 3.1](../Page/Microsoft_Windows_3.x.md "wikilink") のサポート。                                                                                                                                                                                                                                                                                                                                                                                                                                |
| Mathematica 2.2    | 1993年6月1日   | [Windows用](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink") MathLink。[Linux](../Page/Linux.md "wikilink")のサポート。[X](../Page/X_Window_System.md "wikilink") 用フロントエンド、オンラインマニュアル。Macintoshと[NeXT](../Page/NeXT.md "wikilink")用の関数ブラウザ。                                                                                                                                                                                                                                                                                                         |
| Mathematica 3.0    | 1996年9月3日   | 数式タイプセット。数多くの新しい[特殊関数](https://ja.wikipedia.org/wiki/特殊関数 "wikilink")。                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| Mathematica 4.0    | 1999年5月19日  | [スペルチェック](https://ja.wikipedia.org/wiki/スペルチェック "wikilink")機能。20種類以上のデータ、画像、サウンドデータのインポート・エキスポート。ネットワークライセンス管理システム。                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| Mathematica 4.1    | 2000年11月2日  | [Mac OS Xのサポート](https://ja.wikipedia.org/wiki/macOS "wikilink")。J/LinkによるJavaの統合。リアルタイム [3Dグラフィックス](https://ja.wikipedia.org/wiki/次元コンピュータグラフィックス "wikilink")。                                                                                                                                                                                                                                                                                                                                                                                         |
| Mathematica 4.2    | 2002年11月1日  | [スライドショー](../Page/スライドショー.md "wikilink")スタイル。XML対応。[XHTMLへの書き出し](../Page/Extensible_HyperText_Markup_Language.md "wikilink")。                                                                                                                                                                                                                                                                                                                                                                                                                          |
| Mathematica 5.0    | 2003年6月12日  | [疎行列](../Page/疎行列.md "wikilink")のサポート。.NET/Linkによる.NET Frameworkとの統合。クイックスタート。                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| Mathematica 5.1    | 2004年10月25日 | [SQL](../Page/SQL.md "wikilink")接続のサポート。[Excelファイルのインポート](https://ja.wikipedia.org/wiki/Microsoft_Excel "wikilink")・エキスポート。[Webサービス](../Page/Webサービス.md "wikilink")のサポート。[クラスタ分析](https://ja.wikipedia.org/wiki/データ・クラスタリング "wikilink")。[ベンチマーク](../Page/ベンチマーク.md "wikilink")ツールMathematicaMark。                                                                                                                                                                                                                                                      |
| Mathematica 5.2    | 2005年6月20日  | [64ビット](https://ja.wikipedia.org/wiki/64ビット "wikilink")対応。[マルチコア](../Page/マルチコア.md "wikilink")。[SSHリモート接続](../Page/Secure_Shell.md "wikilink")。                                                                                                                                                                                                                                                                                                                                                                                                        |
| Mathematica 6.0    | 2007年5月1日   | 動的インタラクティブ機能。[数学](../Page/数学.md "wikilink")、[物理学](../Page/物理学.md "wikilink")、[化学](../Page/化学.md "wikilink")、[金融](../Page/金融.md "wikilink")、[地理](../Page/地理.md "wikilink")、[言語学](../Page/言語学.md "wikilink")のオンラインデータベースへのアクセス。                                                                                                                                                                                                                                                                                                                          |
| Mathematica 6.0.1  | 2007年7月5日   | Mathematica ドキュメントセンター。「ノートブックを評価」メニュー。Mathematica関数の例題およびチュートリアル。                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| Mathematica 6.0.2  | 2008年2月25日  | バーチャルブック（Mathematicaブックの電子版）。関数ナビゲータ。[Intel Macでの](../Page/Intel_Mac.md "wikilink")64ビット対応。                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| Mathematica 6.0.3  | 2008年6月23日  |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| Mathematica 7.0    | 2008年11月18日 | 組込みの並列高性能計算。[ゲノム](../Page/ゲノム.md "wikilink")、[タンパク質](../Page/タンパク質.md "wikilink")、[気象](../Page/気象.md "wikilink")のオンラインデータベースへのアクセス。[測地](https://ja.wikipedia.org/wiki/測地 "wikilink")および[GISデータ](../Page/地理情報システム.md "wikilink")。                                                                                                                                                                                                                                                                                                                       |
| Mathematica 7.0.1  | 2009年3月5日   | 基本数学・数学授業・文章作成のアシスタントパレットの日本語化。チュートリアル、「How to」ガイド、スクリーンキャスト。ドキュメントに含まれる数千に及ぶ新規例題。gridMathematica Serverとの統合。                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| Mathematica 8.0    | 2010年11月15日 | [Wolfram Alphaとの統合](https://ja.wikipedia.org/wiki/Wolfram_Alpha "wikilink")。自由形式言語入力。CDF（計算可能ドキュメント形式）。[CUDA](../Page/CUDA.md "wikilink")、[OpenCL](../Page/OpenCL.md "wikilink")の組込みサポート。[Cコードの自動作成](../Page/C言語.md "wikilink")。3D画像の[テクスチャマッピング](../Page/テクスチャマッピング.md "wikilink")。Mathematicaホームエディション。                                                                                                                                                                                                                                              |
| Mathematica 8.0.1  | 2011年3月7日   |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| Mathematica 8.0.4  | 2011年10月24日 |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| Mathematica 9.0.0  | 2012年11月28日 | [入力予測](https://ja.wikipedia.org/wiki/入力予測 "wikilink")インターフェイス。[ソーシャルネットワーク](https://ja.wikipedia.org/wiki/ソーシャルネットワーク "wikilink")分析。主要な[データサイエンス](https://ja.wikipedia.org/wiki/データサイエンス "wikilink")、[確率](https://ja.wikipedia.org/wiki/確率 "wikilink")・[統計](../Page/統計.md "wikilink")の新機能。3D立体画像処理機能。インタラクティブゲージ。[Google マップなどの](../Page/Google_マップ.md "wikilink")[Web APIに対応](../Page/アプリケーションプログラミングインタフェース.md "wikilink")。[Rとの統合](../Page/R言語.md "wikilink")。スライドショースタイルの刷新。                                                                        |
| Mathematica 9.0.1  | 2013年1月30日  |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| Mathematica 10.0.0 | 2014年7月21日  | 完全な[Wolfram言語に基づく初のバージョン](https://ja.wikipedia.org/wiki/Wolfram_\(プログラミング言語\) "wikilink")。高度に自動化された[機械学習](../Page/機械学習.md "wikilink")。[地理情報](https://ja.wikipedia.org/wiki/地理情報 "wikilink")可視化のためのGeoGraphicsの導入。[ランダム過程解析の拡張](../Page/確率過程.md "wikilink")。2D・3D画像処理の向上。[信号処理](https://ja.wikipedia.org/wiki/信号処理 "wikilink")の改善。[外部デバイスおよび](https://ja.wikipedia.org/wiki/デバイス "wikilink") [API接続性の向上](../Page/アプリケーションプログラミングインタフェース.md "wikilink")。Wolfram Cloudとの統合。[Raspberry Piへの無料バンドル](https://ja.wikipedia.org/wiki/Raspberry_Pi "wikilink")。 |
| Mathematica 10.0.1 | 2014年9月17日  |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| Mathematica 10.0.2 | 2014年12月10日 |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| Mathematica 10.1   | 2015年4月2日   | Wolfram Data Dropのサポート、オブジェクトの自動認識、OpenSSLを使用した暗号化の言語レベルでのサポート、Wikipediaコンテンツへのアクセス、ユーザ定義の文法規則の配備など。                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| Mathematica 10.2   | 2015年7月14日  | （日本語版は2015年8月18日リリース）コードキャプション、立体データおよび離散データの可視化のためのSliceDensityPlot3DとListStepPlot、常微分方程式および偏微分方程式における固有値および固有関数の数値解法、メールの自動処理機能、クラウド機能の拡張など。                                                                                                                                                                                                                                                                                                                                                                                                         |
| Mathematica 10.3   | 2015年10月28日 | 地理的計算機能、単語や[アルファベット](https://ja.wikipedia.org/wiki/アルファベット "wikilink")の文字列操作のため言語データの追加と自然言語理解能力の向上、[偏微分方程式](../Page/偏微分方程式.md "wikilink")と[固有値問題](https://ja.wikipedia.org/wiki/固有値問題 "wikilink")の記号解法のサポート、GoogleCalendar・GoogleContacts・[Yelp](https://ja.wikipedia.org/wiki/Yelp "wikilink")のデータ，[ArXiv](../Page/ArXiv.md "wikilink")および[CrossRef](https://ja.wikipedia.org/wiki/CrossRef "wikilink")等のサービス接続オプションなど。                                                                                                                              |
| Mathematica 10.3.1 | 2015年12月21日 | [画像処理](../Page/画像処理.md "wikilink")機能の安定性の向上、[スペイン語](https://ja.wikipedia.org/wiki/スペイン語 "wikilink")の[スペルチェック](https://ja.wikipedia.org/wiki/スペルチェック "wikilink")や[中国語](https://ja.wikipedia.org/wiki/中国語 "wikilink")の検索機能を含むさまざまな言語と翻訳についてのサポートの向上、[ユーザインターフェース](https://ja.wikipedia.org/wiki/ユーザインターフェース "wikilink")の多様なアップデートなど。                                                                                                                                                                                                                     |
| Mathematica 10.4   | 2016年3月7日   | [連想におけるパターンマッチングのサポート](../Page/連想配列.md "wikilink")、スケールされたプロット生成、地理的計算の形式と関数の追加、インタラクティブ画像ビューア、Wolfram Data Dropと直接連動するArduino Yunのサポート、20以上の新しいインタープリタ型、24の新しいフォントファミリの追加サポートなど。                                                                                                                                                                                                                                                                                                                                                                      |
| Mathematica 10.4.1 | 2016年4月25日  | 過去のリリースにおける問題への対処と安定性の向上。                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| Mathematica 11.0.0 | 2016年8月22日  | 計算音声、3D印刷、ランダム行列等の新機能、および各種機能の拡張と向上。                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| Mathematica 11.0.1 | 2016年10月5日  | 11.0.0で発生した不具合の解決、各種機能の向上。                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| Mathematica 11.1   | 2017年4月4日   | 機械学習、ニューラルネットワーク、音声処理、ロバストな記述統計等の分野におけるWolfram言語の最先端機能の拡張                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| Mathematica 11.1.1 | 2017年5月9日   | ListPlot3Dを使った描画の問題への対処、MacにおけるニューラルネットワークのGPUサポートの再有効化、URLFetchおよびドキュメント検索のスピード低下の問題の解決など。                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| Mathematica 11.2   | 2017年10月5日  | 機械学習機能の拡張、ニューラルネットワークへのCPUおよびGPUの訓練サポートを含む高性能のフレームワークの導入、微分方程式の数値・記号解の両方の提供など。                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| Mathematica 11.3   | 2018年3月22日  | 数学計算、音声および画像の処理、機械学習とニューラルネットワーク、システムモデリング等におけるMathematicaとWolfram言語の機能の拡張と、フロントエンドの新機能導入など。                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| Mathematica 12.0   | 2019年5月11日  | 数学、幾何学、地理的可視化、音声処理、画像処理、機械学習等における機能，フロントエンド機能の拡張とシステム全体の性能の向上。                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| Mathematica 12.1   | 2020年5月12日  | 数学的可視化、ビデオ計算(音声処理/画像処理/機械学習の動画へ適用)、機械学習とニューラルネットワーク、データアクセスと保存などの機能拡張と、パクレット(=paclet、コード/リソースのモジュラーパッケージ)管理などの新システムの導入。                                                                                                                                                                                                                                                                                                                                                                                                                                |

## 例

方程式 *e*<sup>*x*</sup> = *x*<sup>2</sup> + 2 において *x* = -1 を開始点としてその根を数値的に求める。

`In[1]:= `**`FindRoot`**`[`**`Exp`**`[`****</font>`] `**`==``   ``^2``   ``+``   ``2,`**` {`**`,``   ``-1`**`}]`
`Out[1]= {x -> 1.3190736768573652}`

次の例では、インデックスの原点を0とする 6 × 6 の[行列](https://ja.wikipedia.org/wiki/行列 "wikilink")で *i*、*j* 番目のエントリの値が *ij* であり、0のエントリを1に置き換えたものの[行列式](../Page/行列式.md "wikilink")を求めている。そのような行列式は0である。

`In[2]:= `**`Det`**`[`**`Array`**`[`**`Times,`**` {`**`6,``   ``6`**`}`**`,``   ``0`**`] `**`/.``   ``0``   ``->``   ``1`**`]`
`Out[2]= 0`

一般的なプログラミング言語と大きく異なる点として、Mathematica ではリストのインデックスが 1 から始まることに注意が必要である。

### マルチパラダイムと一つの言語

Mathematicaは[マルチパラダイム・プログラミング言語であり](https://ja.wikipedia.org/wiki/マルチパラダイムプログラミング言語 "wikilink")、一つの問題に対して複数のアプローチを取ることが可能である。

ここでは簡単な例として、最大公約数 GCD(*x*, *y*) のテーブルを作る問題を考える（ここで、1 ≤ *x* ≤ 5、1 ≤ *y* ≤ 5 とする）。これには、少なくとも次の4つのアプローチが考えられる。

**1. [関数型のアプローチ](https://ja.wikipedia.org/wiki/関数型プログラミング "wikilink")：**

`In[3]:= `**`Array`**`[`**`GCD,`**` {`**`5,``   ``5`**`}]`
`Out[3]= `

このアプローチは、表現が抽象的ではあるが、組み込み関数の性能を十分に引き出しており、簡潔で計算速度も速い。`Array` は引数として任意の関数を許容する（名前があるかどうかを問わない）ので、スロット `#n` を使って、`&` の後に対応する関数を記述することができる。したがって、上記の関数は `Array[GCD[#1, #2]&, {5, 5}]` とも記述できるが、Mathematicaではそれを上記のように省略してもよいようになっている。

**2. [APL](../Page/APL.md "wikilink") 的なアプローチ：**

`In[5]:= `**`Outer`**`[`**`GCD,``   ``Range`**`[`**`5`**`]`**`,``   ``Range`**`[[`**`5`**`|`**`5`**`]]`
`Out[5]= `

ここで、`Outer` と`Range` はそれぞれ APL の外積演算子とイオタ演算子に対応している。`Outer` も `Array` と同様、引数として任意の関数を許容する。

**3. Table を使うアプローチ：**

`In[4]:= `**`Table`**`[`**`GCD`**`[`**`,``   `**`], {`**`,``   ``1,``   ``5`**`}, {`**`,``   ``1,``   ``5`**`}]`
`Out[4]= `

`Table` は任意の次元の表を作るのに使われる標準的な関数である。このアプローチは、`GCD` の取る引数が明示的で、直感的に理解しやすい。反面、上記1・2に比べると計算速度で若干劣る。

**4. [手続き型のアプローチ](../Page/手続き型プログラミング.md "wikilink")：**

`In[6]:=`
`    `**`lst1``   ``=`**` {}; (* 空のリストを初期化 *)`
`    `**`For`**`[`**`i``   ``=``   ``1,``   ``i``   ``<=``   ``5,``   ``i++,`**
`        `**`lst2``   ``=`**` {}; `
`        `**`For`**`[`**`j``   ``=``   ``1,``   ``j``   ``<=``   ``5,``   ``j++,`**
`            `**`lst2``   ``=``   ``Append`**`[`**`lst2,``   ``GCD`**`[`**`i,``   ``j`**`]]`
`        ]; `
`        `**`lst1``   ``=``   ``Append`**`[`**`lst1,``   ``lst2`**`]; (* 部分リストを繋ぐ。これが行となる *)`
`    ];`
`    `**`lst1`**
`Out[6]= `

これは [C 言語や](../Page/C言語.md "wikilink") [FORTRAN](../Page/FORTRAN.md "wikilink") などで馴染み深いアプローチである。しかし、組み込み関数を使った場合（上記1\~3）に比べるとコードが冗長である。また、手続き型のアプローチは計算速度が遅く[ボトルネック](../Page/ボトルネック.md "wikilink")になりやすいので、注意が必要である。

以上の例で見たように、Mathematicaプログラミングにおいては、組み込み関数を最大限に利用することが非常に重要である。Mathematicaの組み込み関数を有効に使うことで、問題を簡潔に表現することができる。また、Mathematicaの組み込み関数は、適切なアルゴリズムを用い、高度に最適化され、かつ[C言語](../Page/C言語.md "wikilink")で実装されているため、同じ機能を持つユーザー定義関数に比べて計算速度が圧倒的に速い\[48\]。

### すべては「式」である

Mathematicaは「すべては式である (Everything is an expression.)」という思想のもとに設計されている\[49\]。ここで言う「式 (Expression)」とは、アトムと関数である。

Mathematicaにおいて、数式・リスト・グラフィックスを含むすべてのオブジェクトは *head*\[*e*<sub>1</sub>, *e*<sub>2</sub>, *...*\] という共通の基本構造を持つ。そして、この構造は入れ子にできる（つまり、*e*<sub>1</sub> や *e*<sub>2</sub> もまたこの構造を持てる）。したがって、どんなに複雑なオブジェクトでも、この基本構造とその再帰的な繰り返しで表現できる。

例えば、`x^4+1` という式を入力すると、出力は以下のように表示される。

`In[7]:= `**`^4``   ``+``   ``1`**
`Out[7]= 1+x`<sup>`4`</sup>

`FullForm` を使うと、この式の完全形（Mathematica における内部表現）を見られる。

`In[8]:= `**`FullForm`**`[`**`^4``   ``+``   ``1`**`]`
`Out[8]= Plus[1, Power[x, 4]]`

上記の例では、`Plus` が *head* であり、`Power[x, 4]` が入れ子になっている。`x` のような記号も実は `Symbol["x"]` という構造を持っている。

リストも `List` を *head* とする同様の構造である。例えば、`x^4+1` と `{1, x^4}` という2つの表現は、外見はまったく異なるが、完全形で見れば *head* が `Plus` か `List` かの違いしかない。

この基本構造により、リストとは無関係の普通の式をリスト演算子で処理できる。

`In[9]:= `**`Expand`**`[(`**`Cos`**`[`****`] `**`+``   ``2``   ``Log`**`[`**`^11`**`])`**`/13`**`][[`**`2`**`,_`**`1`**`|`**`2`**`, `**`1`**`]]`
`Out[9]= 2/13`

逆も同様で、リストを普通の式のように扱える。

`In[10]:= `**`Map`**`[`**`Apply`**`[`**`Log,``   `**`]`**`&`**`, {{`**`2,``   `**`}, {`**`3,``   `**`}, {`**`4,``   `**`}}]`
`Out[10]= {Log[x]/Log[2], Log[x]/Log[3], Log[x]/Log[4]}`

ここで、`Apply` は第二引数の *head* を第一引数で指定されたものに置換する関数である。また、`Map` は関数型言語によく見られる[高階関数](../Page/高階関数.md "wikilink") map である。

Mathematica では、数学的オブジェクトがリスト構造と等価であるため、組み込み関数のいくつかは「スレッディング」可能であり、特に指定しなくてもリスト上の各要素にマップされるときにマルチスレッド化される。実際、`Apply` は次のような場合にマルチスレッド化される。

`In[11]:= `**`Apply`**`[`**`Log`**`, {{`**`2,``   `**`}, {`**`3,``   `**`}, {`**`4,``   `**`}}, `**`1`**`]`
`Out[11]= {Log[x]/Log[2], Log[x]/Log[3], Log[x]/Log[4]}`

第三引数 1 により、`Apply` によって置換するのがリストの最初のレベルであることが指定され、これは前述の例と等価である。

## 脚注

## 関連文献

### 和書

出版順に並べる。年、月、日が不明なものはそれぞれ明らかなものよりも前側に置くことにする。

  - 小田部荘司：「学生が学ぶMathematica入門　(完全版)」、 Kindle版、Amazon Services International, Inc.　ASIN: B00JRP6DZK。
  - 大川善邦：「Raspberry Pi Mathematicaプログラミング」、Kindle版、 Amazon Services International, Inc.、ASIN: B00M6G224S。
  - 大川善邦：「RaspberryPiシニアのためのMathematica Kindle版」、Amazon Services International, Inc.、ASIN: B00OK14826。
  - スティーブン・ウルフラム、白水 重明（訳）:「Mathematica - A System for Doing Mathematics by Computer, Second Edition（日本語版）」、アジソン・ウエスレイ・パブリッシャーズ・ジャパン、ISBN 4795296146（1992年）。
  - S. スキエナ, 植野 義明 (訳)：「Mathematica組み合わせ論とグラフ理論―離散数学を実現する」 (アジソン ウェスレイ・トッパン情報科学シリーズ)、トッパン、ISBN 978-4810180503（1992年7月）。
  - T.W. グレイ、J. グリン：「Mathematicaビギナーズガイド」 (アジソン ウェスレイ・トッパン情報科学シリーズ)、トッパン、ISBN 978-4810180565(1992年11月）。
  - D.C.M. バーバラ、C.T.J. ドッドソン：「Mathematica微積分入門」 (プレンティスホール) 、トッパン、ISBN 978-4810185584(1993年4月）。
  - 守谷 良二：「Mathematicaで数学を〈線形代数編〉」、海文堂出版、ISBN 978-4303728007(1993年9月）。
  - ディミトリ・D. ヴィーデンスキー：「Mathematica偏微分方程式」 (アジソン ウェスレイ・トッパン情報科学シリーズ) 、トッパン、ISBN 978-4810180695（1994年3月）。
  - T.W. グレイ、J. グリン：「Mathematica数学の探索」 (アジソン ウェスレイ・トッパン情報科学シリーズ)、トッパン、ISBN 978-4810180459　(1994年5月)。
  - 守谷良二：「Mathematicaで数学を―微積分編Ｉ」、海文堂出版、ISBN 978-4303727901（1994年10月）。
  - N ブラックマン、新井 宏二 (訳), 松井 康範 (訳)：「Mathematica事典」、トッパン、ISBN 978-4810189018（1994年11月）。
  - R.J. ゲイロード、P.R. ウエリン、S.N. カーミン：「Mathematicaプログラミング」、近代科学社、ISBN 978-4764902282 (1994年12月）。
  - 阿部寛：「Mathematicaでみる数理物理入門 II」、講談社、ISBN 978-4061532168（1995年4月）。
  - Robert D. Skeel, Jerry B. Keiper, 玄 光男 (訳), 辻 陽一 (訳)：「Mathematicaによる数値計算」、共立出版、ISBN　978-4320014886（1995年4月10日）。
  - 小林道正：「Mathematicaによる微積分」、朝倉書店、ISBN 978-4254110692（1995年12月）。
  - A.グレイ, 武沢 護 (訳)：「Mathematica 曲線と曲面の微分幾何」、トッパン、ISBN 978-4810189193（1996年3月）。
  - 和田昇：「線形・非線形力学とカオスへの入門―Mathematicaによる」、サイエンティスト社、ISBN 978-4914903299　(1996年4月）。
  - J.W.グレイ、時田 節 (訳), 武沢 護 (訳)：「Mathematica 方法と応用」、サイエンティスト社、ISBN 978-4914903312（1996年5月）。
  - S.ワゴン、長岡亮介(監訳):「Mathematicaで見える現代数学」、ブレーン出版、ISBN 4-89242-143-X（1996年5月10日、初版二刷）。
  - 斎藤 兆古：「Mathematicaによるウェーブレット変換」、朝倉書店、ISBN 978-4254221398（1996年9月）。
  - John S. Robertson, 下地 貞夫 (訳):「Mathematicaによる工科系数学」、共立出版、ISBN 978-4320015180（1996年10月15日）。
  - 白石修二:「例題で学ぶMathematica グラフィックス編」、森北出版、ISBN 978-4627838109 (1996年11月）。
  - 片桐 重延、室岡 和彦：「Mathematicaによる離散数学入門」 (新・数学とコンピュータシリーズ) 、東京電機大学出版局、ISBN 978-4501526108(1997年4月）。
  - 上坂 吉則：「Mathematica数値数式プログラミング」、牧野書店、ISBN 978-4795201132 (1997年4月1日）。
  - リチャード・J ゲイロード、ポール・R. ウェリン ：「MATHEMATICA複雑系のシミュレーション―物理学と生物学の探究」、シュプリンガー・フェアラーク東京、ISBN 978-4431707097(1998年5月）。
  - 斎藤 兆古：「Mathematicaによる 画像処理入門」、朝倉書店,ISBN 978-4254221428 (1998年6月1日)。
  - 鈴木 真二：「力学入門」 (Mathematicaで学ぶシリーズ)、コロナ社、ISBN 978-4339077520（1999年2月1日）。
  - 田沢義彦：「曲線論・曲面論―Mathematicaで探索する古典微分幾何学」 (Computer in Education and Research) 、ピアソンエデュケーション、ISBN 978-4894711334（1999年8月）。
  - ロバート・L. ジンマーマン、フレデリック・I. オルネス：「物理学のためのMathematica―古典力学から宇宙論まで」、ピアソンエデュケーション、ISBN 978-4894711624（1999年12月）。
  - 鈴木昱雄：「カオス入門」 (Mathematicaで学ぶシリーズ) 、コロナ社、ISBN 978-4339077537（1999年12月1日）。
  - 川瀬 宏海：「Mathematicaによる電磁気学」第2版、東京電機大学出版局、ISBN 978-4501108809（2000年3月1日）。
  - 小林道正：「Mathematica確率―基礎から確率微分方程式まで」 (Mathematica数学）、朝倉書店、ISBN 978-4254115222（2000年4月）。
  - 宮岡悦良：「Mathematica数学の道具箱〈下〉」改訂新版、ブレーン出版、ISBN 978-4892421747（2000年7月）。
  - 椎原 浩輔：「Mathematicaによる金融工学」、東京電機大学出版局、ISBN 978-4501618100（2000年9月1日）。
  - 木村広:「Mathematicaハンドブック」、秀和システム、ISBN 978-4798000503（2000年12月14日）。
  - 渋谷清雄、谷沢俊弘、藤井幸一：「Mathematica基礎からの演習」、サイエンティスト社、ISBN 978-4914903817（2001年4月)。
  - 古田孝之：「もっとMathematicaで数学を」、培風館、ISBN 978-4563003302（2002年4月）。
  - 大塚 道明：「試して分かる高校数学―Mathematicaでトライ\!」、現代数学社、ISBN 978-4768702871（2003年4月）。
  - 日本Mathematicaユーザー会編:「入門Mathematica 【決定版】 Ver.7対応」、東京電機大学出版局、ISBN 978-4501546205（2009年6月20日）。
  - 榊原 進 『はやわかり Mathematica 第3版』 共立出版、2010年。ISBN 978-4320122482。
  - 榊原進：「はやわかりMathematica 第3版」、共立出版、ISBN 978-4320122482（2010年3月24日）。
  - Sal Mangano (著), 松田 裕幸 (訳) :「Mathematicaクックブック」、オライリージャパン、ISBN 978-4873114835（2011年4月25日）。
  - 依田 潔, 日本シミュレーション学会 (編)：「Mathematicaによる電磁界シミュレーション入門 - ＰＯＤ版」(計算電気・電子工学シリーズ) 、森北出版; POD版、ISBN 978-4627715295（2012年2月24日）。
  - 川平友規：「レクチャーズオンMathematica」、プレアデス出版、ISBN 978-4903814612（2013年5月1日）。
  - 野原 勉：「Mathematicaと微分方程式」 ,日新出版(実用数学全書)、ISBN 978-4817302489（2014年3月30日）。
  - 大川 善邦：「RaspberryPi2でMathematicaプログラミング」、工学社 (I・O BOOKS)、 ISBN 978-4777519033（2015年7月21日）。
  - 中川栄一、勝明次郎：「Mathematicaへの誘い-今日から始める基礎と応用-」、成山堂書店、ISBN 978-4425651818　(2015年9月18日）。
  - 宮岡 悦良：「数学の道具箱 Mathematica 基本編」、近代科学社、ISBN 978-4764905078（2016年4月12日）。
  - C.ヘイスティング、K.ミッショー、M.モリソン:「ハンズ・オン・スタートMathematica : Wolfram言語™によるプログラミング」、丸善、ISBN 978-4-621-30273-6(2018年1月）。

### 洋書

  - Roozbeh Hazrat:"Mathematica: A Problem-Centered Approach", Second Edition, Springer, ISBN 9783319275840 (2015).
  - Paul Wellin: "Essentials of Programming in Mathematica"、Cambridge University Press、ISBN 978-1107116665 (2015年12月17日）。
  - Cliff Hastings, Kelvin Mischo, Michael Morrison:"Hands-On Start to Wolfram Mathematica: And Programming with the Wolfram Language"(2nd Ed.)、Wolfram Media Inc、ISBN 978-1579550127 (2016年11月30日）。
  - Stephen Wolfram: "An Elementary Introduction to the Wolfram Language"(2nd Ed.)、Wolfram Media Inc、ISBN 978-1944183059 (2017年4月)。
  - [Stephen Wolfram:"An Elementary Introduction to the Wolfram Language" (2nd Ed.) ONLINE VERSION](http://www.wolfram.com/language/elementary-introduction/2nd-ed/)

## 関連項目

  - [スティーブン・ウルフラム](../Page/スティーブン・ウルフラム.md "wikilink")
  - [ウルフラム・リサーチ](../Page/ウルフラム・リサーチ.md "wikilink")
  - [Wolfram Alpha](https://ja.wikipedia.org/wiki/Wolfram_Alpha "wikilink")
  - [New Kind of Science](https://ja.wikipedia.org/wiki/新しい種類の科学 "wikilink") : Mathematica を全面的に利用して書かれたウルフラムの著書。
  - [劣等上等](https://ja.wikipedia.org/wiki/劣等上等 "wikilink")：[鏡音リン・レン](../Page/鏡音リン・レン.md "wikilink")の楽曲。曲中にマセマティカ(Mathematica)という言葉が登場する。

## 外部リンク

  -
  - [Wolfram Mathematica ドキュメントセンター](http://reference.wolfram.com/)

  - [Wolfram Demonstrations Project　(10,000以上のデモサンプルや事例にアクセス可能)](http://demonstrations.wolfram.com/)

  - [Wolfram Community](http://community.wolfram.com/)

  - [The Mathematica Story: A Scrapbook](http://www.mathematica25.com)

  - [The Mathematica Journal](http://www.mathematica-journal.com)

      - [日本語版セレクション（HULINKS）](https://www.hulinks.co.jp/software/math_develop/mj)

  - [HULINKS (国内認定販売代理店＆認定トレーニングパートナー)](http://www.hulinks.co.jp/software/mathematica/)

[Category:プログラミング言語](https://ja.wikipedia.org/wiki/Category:プログラミング言語 "wikilink") [Category:数式処理システム](https://ja.wikipedia.org/wiki/Category:数式処理システム "wikilink") [Category:Linux向け数式処理システム](https://ja.wikipedia.org/wiki/Category:Linux向け数式処理システム "wikilink") [Category:関数型言語](https://ja.wikipedia.org/wiki/Category:関数型言語 "wikilink") [Category:数学に関する記事](https://ja.wikipedia.org/wiki/Category:数学に関する記事 "wikilink") [Category:Javaプラットフォーム](https://ja.wikipedia.org/wiki/Category:Javaプラットフォーム "wikilink") [Category:クロスプラットフォームのソフトウェア](https://ja.wikipedia.org/wiki/Category:クロスプラットフォームのソフトウェア "wikilink") [Category:数値解析ソフトウェア](https://ja.wikipedia.org/wiki/Category:数値解析ソフトウェア "wikilink") [Category:Linux向け数値解析ソフトウェア](https://ja.wikipedia.org/wiki/Category:Linux向け数値解析ソフトウェア "wikilink") [Category:統計処理ツール](https://ja.wikipedia.org/wiki/Category:統計処理ツール "wikilink") [Category:1988年のソフトウェア](https://ja.wikipedia.org/wiki/Category:1988年のソフトウェア "wikilink") [Category:数学ソフトウェア](https://ja.wikipedia.org/wiki/Category:数学ソフトウェア "wikilink") [Category:数式エディタ](https://ja.wikipedia.org/wiki/Category:数式エディタ "wikilink") [Category:定理証明ソフトウェア](https://ja.wikipedia.org/wiki/Category:定理証明ソフトウェア "wikilink") [Category:対話型幾何学ソフトウェア](https://ja.wikipedia.org/wiki/Category:対話型幾何学ソフトウェア "wikilink")

1.
2.
3.
4.
5.
6.
7.
8.
9.
10.
11.
12.
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
24.
25.
26.
27.
28.
29.
30.
31.
32.
33.
34.
35.
36.
37.
38.
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
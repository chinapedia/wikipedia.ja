> この記事は[Model View Controller](https://ja.wikipedia.org/wiki/Model_View_Controller)から翻訳されています。


[MVC-Process.svg](https://ja.wikipedia.org/wiki/File:MVC-Process.svg "fig:MVC-Process.svg")

**MVC**（**Model View Controller** モデル・ビュー・コントローラ）は、[ユーザーインタフェースをもつ](https://ja.wikipedia.org/wiki/ユーザーインターフェイス "wikilink")[アプリケーションソフトウェア](../Page/アプリケーションソフトウェア.md "wikilink")を実装するための[デザインパターンである](https://ja.wikipedia.org/wiki/デザインパターン_\(ソフトウェア\) "wikilink")。

アプリケーションソフトウェアの**内部データ**を、ユーザーが直接参照・編集する情報から分離する。そのためにアプリケーションソフトウェアを以下の3つの部分に分割する。

1.  model: アプリケーションデータ、ビジネスルール、ロジック、関数
2.  view: グラフや図などの任意の情報表現
3.  controller: 入力を受け取りmodelとviewへの命令に変換する

## MVCの歴史

  - 1979年: [パロアルト研究所](https://ja.wikipedia.org/wiki/パロアルト研究所 "wikilink")にてTrygve Reenskaugが考案。\[1\]\[2\]長い間、Smalltalk-80の実装のみが公開され、MVCに関する公開情報はなかった
  - 1988年: 最初の論文「A Cookbook for Using the Model-View-Controller User Interface Paradigm in Smalltalk -80」\[3\]が公開\[4\]
  - 1994年: 書籍「[Design Patterns:Elements of Reusable Object-Oriented Software](https://ja.wikipedia.org/wiki/デザインパターン_\(ソフトウェア\) "wikilink")」\[5\]内で取り上げられる
  - 1999年: MVCのサーバサイド実装として**JavaServer Pages Model 2**が発表\[6\]

元来[Smalltalk](../Page/Smalltalk.md "wikilink")におけるウィンドウプログラム開発のための設計指針として生まれたが、構造が複雑となりがちな[グラフィカルユーザインターフェース](https://ja.wikipedia.org/wiki/グラフィカルユーザインターフェース "wikilink") (GUI) をもつソフトウェアにおける有用性から他方面へ広がった。

その後、Smtalltalk-80から派生した[Squeak](../Page/Squeak.md "wikilink")では、[Self](../Page/Self.md "wikilink")から移植されたGUIツールキット[Morphic](https://ja.wikipedia.org/wiki/Morphic "wikilink")が主に使われるようになった。[Morphic](https://ja.wikipedia.org/wiki/Morphic "wikilink")ではビューとコントローラを分離しておらず、その後の多くのGUIツールキットでもビューとコントローラは完全には分離されていない。。

## MVCの構造

MVCでは、プログラムを3つの要素、**Model**（モデル）、**View**（ビュー）、**Controller**（コントローラ）に分割する。

  - モデル
    そのアプリケーションが扱う領域のデータと手続き（[ビジネスロジック](../Page/ビジネスロジック.md "wikilink") - ショッピングの合計額や送料を計算するなど）を表現する要素である。また、データの変更をビューに通知するのもモデルの責任である（モデルの変更を通知するのに[Observer パターンが用いられることもある](../Page/Observer_パターン.md "wikilink")）。
  - ビュー
    モデルのデータを取り出してユーザが見るのに適した形で表示する要素である。すなわち、UIへの出力を担当する。例えば、[ウェブアプリケーション](https://ja.wikipedia.org/wiki/ウェブアプリケーション "wikilink")では[HTML文書を生成して動的にデータを表示するためのコードなどにあたる](../Page/HyperText_Markup_Language.md "wikilink")。GUIにおいては通常、階層構造を成す。
  - コントローラ
    ユーザからの入力（通常[イベントとして通知される](../Page/イベント_\(プログラミング\).md "wikilink")）をモデルへのメッセージへと変換してモデルに伝える要素である。すなわち、UIからの入力を担当する。モデルに変更を引き起こす場合もあるが、直接に描画を行ったり、モデルの内部データを直接操作したりはしない。

なお、UIにおける入力と出力は本質的には不可分なものであり、したがってビューとコントローラはいつでも分離できるとは限らない。このようなM-VCとなるような構造を**Document-View**と呼ぶ\[7\]。

対象となるモデルにビュー・コントローラを持たせるだけでなく、ユーザとモデルの構成要素との対話のために各々の構成要素にもビュー・コントローラを持たせる構造を拡張MVCと呼ぶ\[8\]。

## MVCのシナリオ

MVCの実装はさまざまであるが、制御フローは一般的に次のようになる\[9\]。

1.  コントローラが[入力機器](https://ja.wikipedia.org/wiki/入力機器 "wikilink")（[マウスや](../Page/マウス_\(コンピュータ\).md "wikilink")[キーボードなど](../Page/キーボード_\(コンピュータ\).md "wikilink")。Smalltalk-80ではInputSensorで表わされる）を監視する。
2.  ユーザが入力機器に入力を与える。
3.  コントローラがユーザのアクションに応じてモデルのメソッドを呼ぶ。その結果モデルのデータが書き換えられる場合もある。
4.  モデルが変更された場合、自身が変更された旨をビューなどのオブザーバに対して通知する。
5.  ビューはモデルから関連するデータを取得し、出力を更新する。典型的には画面に図形を描画する。

このシナリオでビューやコントローラをそれぞれ1つのオブジェクトとして単純化して説明しているが、実際にはビューは階層構造になっていて、各ビューごとに対応するコントローラが存在する。そのためユーザからの入力を処理すべきコントローラを決定する作業が必要となる。例えばSmalltalk-80ではマウスカーソルを含むビューに対応するコントローラが入力を処理するのが原則であり、次のようなステップで入力を処理すべきコントローラを決定する。

1.  コントローラはビューに対し、入力を処理すべきコントローラを問い合わせる（ビューの位置や階層構造を知っているのはビューなので）。
2.  ビューはコントローラに現在のマウスカーソルの位置を問い合わせる（入力機器の状態を知っているのはコントローラなので）。
3.  ビューはマウスカーソルを含むビューを探す。
4.  そのビューに対応するコントローラを、入力を処理すべきコントローラとする。

## MVCとデザインパターン

MVCは、[デザインパターンの](https://ja.wikipedia.org/wiki/デザインパターン_\(ソフトウェア\) "wikilink")1種と扱われる場合もあるが（MVCパターンと呼称される）、MVC自体が他の小さなデザインパターン([Observer パターン](../Page/Observer_パターン.md "wikilink")・[Command パターン](https://ja.wikipedia.org/wiki/Command_パターン "wikilink")・[Factory Method パターン](../Page/Factory_Method_パターン.md "wikilink")・[Facade パターンなど](../Page/Facade_パターン.md "wikilink"))を利用して実装されることが多いところからすると、デザインパターンというより、さらに粒度の大きい1種の[ソフトウェアアーキテクチャ](../Page/ソフトウェアアーキテクチャ.md "wikilink")という方が適当であろう\[10\]\[11\]。

各モジュールが比較的はっきりと分かれ、プログラムの見通しがよくなるとともに、[ユーザインタフェース](../Page/ユーザインタフェース.md "wikilink") (UI) 部分を別のモジュールに取り替えることが容易となるのが利点である。[自動プログラミング](../Page/自動プログラミング.md "wikilink")などにも適している。

## 脚注

<references/>

## 関連項目

  - [イベント駆動型プログラミング](../Page/イベント駆動型プログラミング.md "wikilink")
  - [多層アーキテクチャ](../Page/多層アーキテクチャ.md "wikilink")
  - [JFace](../Page/JFace.md "wikilink")、[Google Web Toolkit](https://ja.wikipedia.org/wiki/Google_Web_Toolkit "wikilink")、[Spring MVC フレームワーク](https://ja.wikipedia.org/wiki/Spring_Framework "wikilink")
  - [Model View ViewModel](https://ja.wikipedia.org/wiki/Model_View_ViewModel "wikilink")
  - [Model View Presenter](https://ja.wikipedia.org/wiki/Model_View_Presenter "wikilink")

[Category:ソフトウェアパターン](https://ja.wikipedia.org/wiki/Category:ソフトウェアパターン "wikilink") [Category:ソフトウェア工学](https://ja.wikipedia.org/wiki/Category:ソフトウェア工学 "wikilink") [Category:プログラミングパラダイム](https://ja.wikipedia.org/wiki/Category:プログラミングパラダイム "wikilink") [Category:ソフトウェアアーキテクチャ](https://ja.wikipedia.org/wiki/Category:ソフトウェアアーキテクチャ "wikilink")

1.  [MVC XEROX PARC 1978-79](http://heim.ifi.uio.no/~trygver/themes/mvc/mvc-index.html)
2.  [The Model-View-Controller (MVC) Its Past and Present](http://heim.ifi.uio.no/~trygver/2003/javazone-jaoo/MVC_pattern.pdf)
3.  [A Cookbook for Using the Model-View-Controller User Interface Paradigm in Smalltalk -80](http://www.ics.uci.edu/~redmiles/ics227-SQ04/papers/KrasnerPope88.pdf)
4.  [Model View Controller History](http://c2.com/cgi/wiki?ModelViewControllerHistory)
5.
6.  [Understanding JavaServer Pages Model 2 architecture](http://www.javaworld.com/article/2076557/java-web-development/understanding-javaserver-pages-model-2-architecture.html)
7.
8.
9.
10.
11. [Model View Controller As An Aggregate Design Pattern](http://c2.com/cgi/wiki?ModelViewControllerAsAnAggregateDesignPattern)
> この記事は[Swing](https://ja.wikipedia.org/wiki/Swing)から翻訳されています。


[thumb](https://ja.wikipedia.org/wiki/ファイル:Gui-widgets.png "wikilink")

は、[プログラミング言語](../Page/プログラミング言語.md "wikilink") [Java](https://ja.wikipedia.org/wiki/Java "wikilink") の[GUIツールキット](https://ja.wikipedia.org/wiki/GUIツールキット "wikilink")である。[Oracle](https://ja.wikipedia.org/wiki/Oracle "wikilink")社の[Java Foundation Classesの一部であり](https://ja.wikipedia.org/wiki/Java_Foundation_Classes "wikilink")、同じくJavaの GUI ツールキットである [AWT](https://ja.wikipedia.org/wiki/Abstract_Window_Toolkit "wikilink") を拡張したもの。Javaプログラムに[グラフィカルユーザインタフェース](https://ja.wikipedia.org/wiki/グラフィカルユーザインタフェース "wikilink")(GUI)を提供する[APIである](../Page/アプリケーションプログラミングインタフェース.md "wikilink")。

Swingは、先行するAWTよりも洗練されたGUI[コンポーネントを提供するために開発された](https://ja.wikipedia.org/wiki/ソフトウェアコンポーネント "wikilink")。Swingは、幾つかのプラットフォームの[ルック・アンド・フィール](https://ja.wikipedia.org/wiki/ルック・アンド・フィール "wikilink")をエミュレートしたネイティブなルック・アンド・フィールを提供する。また、「[プラグイン](../Page/プラグイン.md "wikilink")可能なルック・アンド・フィール」(Pluggable look and feel)をサポートしていることにより、アプリケーションは簡単にルック・アンド・フィールを切り替えることができ、下で走っているプラットフォームとは関係ないルック・アンド・フィールを使うこともできる。SwingはAWTよりも強力で柔軟なコンポーネントを持る。ボタン、チェックボックス、ラベルといった馴染み深いコンポーネントの他にも、Swingはタブ付きパネル、スクロール窓、スライダー、スピナ、ツリー表示、表、リストなどの高度なコンポーネントを提供している。

AWTと異なり、Swingコンポーネントはプラットフォーム固有のコードで実装されたものではなく、完全にJavaで書かれている。このため、Swingはプラットフォームに依存しない。このような[コンポーネント](https://ja.wikipedia.org/wiki/コンポーネント "wikilink")を軽量コンポーネントと呼ぶ\[1\]。AWT は[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink")の[ウィンドウシステム](https://ja.wikipedia.org/wiki/ウィンドウシステム "wikilink")に準じたデザインになるのに対し、 で作成した [GUI](https://ja.wikipedia.org/wiki/GUI "wikilink") は [Java](https://ja.wikipedia.org/wiki/Java "wikilink")プログラム上で描画されるので、より柔軟な設計が可能となる。

Swingは[JavaFX](https://ja.wikipedia.org/wiki/JavaFX "wikilink")により置き換えられる方針であるが、当面の将来はSwingもJava SE仕様の一部として残る見込みである\[2\]。

## アーキテクチャ

Swingは、Java言語用の、プラットフォームに依存しない、 "[Model View Controller](https://ja.wikipedia.org/wiki/Model_View_Controller "wikilink")"型の [GUIフレームワークであり](https://ja.wikipedia.org/wiki/グラフィカルユーザインタフェース "wikilink")、単一[スレッドプログラミング](../Page/スレッド_\(コンピュータ\).md "wikilink")・モデルに従っている\[3\]。更に、このフレームワークはコード構造とSwingベースのGUIのグラフィック表現の間に抽象化層を提供する。

### 基礎

Swingは完全にJavaで書かれているためプラットフォームに依存しない。全てのSwingクラスに関する完全なドキュメントが[Java API Guide](http://docs.oracle.com/javase/6/docs/api/)（バージョン6用）または[Java Platform Standard Edition 8 API Specification](http://docs.oracle.com/javase/8/docs/api/)（バージョン8用）にある。

#### 拡張性

Swingは高度にモジュール・ベースのアーキテクチャである。これによりフレームワークのインターフェイスに様々なカスタム実装を「差し込む」ことができる。ユーザはJavaの継承の仕組みを使って、デフォルト実装をオーバーライドして、これらのコンポーネントに独自のカスタム実装を作ることができる\[4\]。

Swingは**コンポーネント・ベースのフレームワーク**である。そのコンポーネント群は全て究極的には`javax.swing.JComponent`クラスから派生したものである。Swingのオブジェクト群は非同期的にイベントを発出し、それぞれがプロパティ群を持ち、各コンポーネントに固有のメソッド呼び出しに対応する。Swingコンポーネントは[JavaBeans](../Page/JavaBeans.md "wikilink")コンポーネントであり、Java Beans Component Architecture仕様に準拠している。

#### 設定可能

Swingはランタイム機構と間接的構成パターンに大きく依存しているため、その設定値が実行中に根本的に変わっても対応できるようになっている。たとえば、Swingベースの、実行中のアプリケーションのユーザー・インターフェイスを[ホットスワップ](https://ja.wikipedia.org/wiki/ホットスワップ "wikilink")可能である。更に、ユーザが独自のルック・アンド・フィールの実装を与えることもでき、これにより、アプリケーションのコードは何も変更することなく、既存のSwingアプリケーションのルック・アンド・フィールを均質に変更することが可能となっている。

  - 軽量UI:

Swingの高水準の柔軟性は、ネイティブ・ホストの[オペレーティング・システム](https://ja.wikipedia.org/wiki/オペレーティング・システム "wikilink") (OS)のGUI部品の表示をオーバーライドできる能力を反映したものである。Swingは、そのGUI部品をJava 2D API群で描画しており、ネイティブなユーザー・インターフェイス・ツールキットを呼ばない。従ってSwingコンポーネントには、それに対応するネイティブなOSのGUIコンポーネントといったものはなく、下層にあるグラフィクスGUIで可能な範囲内においてどのように描画しようと自由である。

しかしながら、すべてのSwingコンポーネントは、その中核部分において[AWT](https://ja.wikipedia.org/wiki/Abstract_Window_Toolkit "wikilink") コンテナに依存している。これは、Swingの はAWTのContainerを拡張したものだからである。これによりSwingをホストOSのGUI管理フレームワーク（デバイスとスクリーンの対応づけや、キー操作やマウス移動などユーザとのインタラクションを含む）に差し込むことが可能になっている。Swingは単純に、Swing固有の(OSにとらわれない）意味(semantics)を、下層にある(OS固有の)コンポーネント群に「置き換え」ているだけである。従って、たとえば、全てのSwingコンポーネントは、(AWTの)Containerで定義されたcomponent.paint()の呼び出しに応じて、自身をグラフィック・デバイスに描画する。しかし、その描画をOS固有の「重い」(heavy weight)ウィジェットに委任するAWTコンポーネントとは異なり、Swingコンポーネントは自身の描画は自分の責任として行う。

この「置き換え」(transposition)と「切り離し」(decoupling)は単に目に見える部分だけのことではなく、そのコンポーネント包含階層内で発出されるイベントにおけるOS非依存の意味(semantics)の管理と応用にもいえることである。一般的にいって、Swingアーキテクチャは、OSのGUIが持っている意味に対して与えられた様々な表現形式を、単純ではあるが一般化されたパターンに対応づける仕事をAWTコンテナに委任している。その一般化されたプラットフォーム上で構築すれば、モデルの形でリッチで複雑なGUIの意味(semantics)を組み上げたことになる。

## プログラム例

``` java
import javax.swing.JFrame;
import javax.swing.JLabel;
import javax.swing.SwingUtilities;
import javax.swing.WindowConstants;

public class HelloWorld implements Runnable {

    @Override
    public void run() {
        JFrame frame = new JFrame();
        frame.setDefaultCloseOperation(WindowConstants.EXIT_ON_CLOSE);
        frame.getContentPane().add(new JLabel("Hello, world!"));
        frame.pack();
        frame.setLocationRelativeTo(null);
        frame.setVisible(true);
    }
    public static void main(String[] args) {
        HelloWorld hello = new HelloWorld();
        SwingUtilities.invokeLater(hello);
    }
}
```

## 歴史

  - 1998年にリリースされた  1.2 で初めてリリースされた。
  - 2002年にリリースされた  1.4 で提供された  を利用することでプログラムの再配布の問題を解決した。
  - 2004年にリリースされた  1.5 でメモリ消費効率の改善を行った。
  - 2006年にリリースされた  6 では  の実行性能が改善されたことによって  の実行性能も改善された。

## 関連項目

  - [レイアウトマネージャ](https://ja.wikipedia.org/wiki/レイアウトマネージャ "wikilink")

  -
  -
  - [JavaFX](https://ja.wikipedia.org/wiki/JavaFX "wikilink")

## 脚注

## 外部リンク

  -
[Category:Java](https://ja.wikipedia.org/wiki/Category:Java "wikilink") [Category:Javaプラットフォーム](https://ja.wikipedia.org/wiki/Category:Javaプラットフォーム "wikilink") [Category:ウィジェット・ツールキット](https://ja.wikipedia.org/wiki/Category:ウィジェット・ツールキット "wikilink")

1.
2.
3.  "Swing threading and the event-dispatch thread - JavaWorld", Welcome to JavaWorld.com, <http://www.javaworld.com/javaworld/jw-08-2007/jw-08-swingthreading.html>
4.  "LookAndFeel (Java Platform SE 7 )", Oracle Documentation, <http://docs.oracle.com/javase/7/docs/api/javax/swing/LookAndFeel.html> , 5/26/2012
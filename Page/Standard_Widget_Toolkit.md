> この記事は[Standard Widget Toolkit](https://ja.wikipedia.org/wiki/Standard_Widget_Toolkit)から翻訳されています。


**Standard Widget Toolkit**（**SWT**）は、[Javaプラットフォーム](../Page/Javaプラットフォーム.md "wikilink")用[ウィジェット・ツールキット](https://ja.wikipedia.org/wiki/ウィジェット・ツールキット "wikilink")の一種。元々、[IBM](../Page/IBM.md "wikilink")が開発したが、現在は [Eclipse Foundation](https://ja.wikipedia.org/wiki/Eclipse_Foundation "wikilink") が [Eclipse](../Page/Eclipse_\(統合開発環境\).md "wikilink") IDE と共に管理保守している。[サン・マイクロシステムズ](../Page/サン・マイクロシステムズ.md "wikilink")が Java 標準の一環として提供するJava用[GUIツールキットである](https://ja.wikipedia.org/wiki/グラフィカルユーザインタフェース "wikilink") [AWT](../Page/Abstract_Window_Toolkit.md "wikilink") と [Swing](../Page/Swing.md "wikilink") を代替するものとして開発された。

SWT は Java で書かれている。GUI部品を表示するため、SWT はそのオペレーティングシステムが提供するGUIライブラリを JNI（[Java Native Interface](https://ja.wikipedia.org/wiki/Java_Native_Interface "wikilink")）経由で使用する（これはシステム固有の[APIを使う一般的手法である](../Page/アプリケーションプログラミングインタフェース.md "wikilink")）。SWT を使うプログラムは移植性があるが、ツールキット自体の実装は Java でかかれているにも関わらず、各プラットフォーム固有である。

SWT は [Eclipse Public License](https://ja.wikipedia.org/wiki/Eclipse_Public_License "wikilink") でライセンスされている。このライセンスは [Open Source Initiative](../Page/Open_Source_Initiative.md "wikilink") が[オープンソース](../Page/オープンソース.md "wikilink")ライセンスとして認めている\[1\]。

## Java GUIツールキットの歴史

最初のJava用GUIツールキットは、AWT（[Abstract Window Toolkit](../Page/Abstract_Window_Toolkit.md "wikilink")）であり、サンのJava標準の一部として [JDK](../Page/Java_Development_Kit.md "wikilink") 1.0 で登場した。AWT は比較的単純であり、[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink")が提供するネイティブな[オブジェクトをJavaコードで包み](../Page/オブジェクト_\(プログラミング\).md "wikilink")、メニューやボタンといったGUI部品を生成する。AWTはネイティブ[ウィジェットラッパーとしては非常に薄く](https://ja.wikipedia.org/wiki/ウィジェット_\(GUI\) "wikilink")、プラットフォーム固有のコードが開発者に透けて見え、バグやOS固有の癖がそのままさらけ出されているため、異なるプラットフォーム間で移植性のあるアプリケーションを作成するには限界があった。

[Swing](../Page/Swing.md "wikilink")は第二世代のツールキットで、サンが J2SE 1.2 で導入した。AWT よりも[オブジェクト指向的である](../Page/オブジェクト指向プログラミング.md "wikilink")。SwingのGUI部品は 100% Java であり、ネイティブコードは使っていない。ネイティブAPIをラップする代わりに、Swingは低レベルなOSルーチンを使ってGUI部品を自前で描画する。

そのころ、[IBM](../Page/IBM.md "wikilink")は[Smalltalk](../Page/Smalltalk.md "wikilink")を使った[統合開発環境](../Page/統合開発環境.md "wikilink") (IDE) [VisualAge](https://ja.wikipedia.org/wiki/VisualAge "wikilink") を開発していた。これをオープンソースとして公開することに決め、それが[Eclipseの開発へと繋がっていった](../Page/Eclipse_\(統合開発環境\).md "wikilink")。Eclipse は [Microsoft Visual Studio](https://ja.wikipedia.org/wiki/Microsoft_Visual_Studio "wikilink") のような IDE とも競合できるものとすることを目的としていた。Eclipse は Java で書かれており、IBMの開発者らは「ネイティブの[ルック・アンド・フィール](../Page/ルック・アンド・フィール.md "wikilink")」と「ネイティブの性能」を持ったツールキットが必要と考え、Swing を置換するものとして SWT を開発した。

## 設計

SWT は、[GTK+](https://ja.wikipedia.org/wiki/GTK+ "wikilink")オブジェクトや[Motifオブジェクトなど](../Page/Motif_\(GUI\).md "wikilink")、ネイティブのコードオブジェクトのラッパーである。そのため、SWTウィジェットは「重い」ネイティブオブジェクトに軽いJavaラッパーをかぶせたようなイメージで「重い」と言われることが多い。SWTが必要とする機能をネイティブのGUIライブラリが持っていない場合、SWTはSwingのように独自のGUIコードをJavaで実装している。SWTは本質的には、AWTの性能やルック・アンド・フィールとSwingのそれとの中間にあると言える。

Eclipse Foundation によれば、SWT と Swing は目標の異なる異なったツールである。SWTの目的は、各種プラットフォームのネイティブウィジェットにアクセスできる共通APIを提供することである。設計目標の第一は高性能なネイティブのルック・アンド・フィールとプラットフォーム統合の達成である。一方Swingは高度にカスタマイズ可能で全プラットフォームに共通なルック・アンド・フィールの提供にある。

SWT は Swing に比較すると単純なツールキットであり、標準的な開発に無関係の機能はあまり存在しない\[2\]。このため、SWT が Swing に比べて機能が少ないと批判する人もいる\[3\]。

Javaの設計者である[ジェームズ・ゴスリン](https://ja.wikipedia.org/wiki/ジェームズ・ゴスリン "wikilink")は、SWTが単純すぎ、AWTと同じ理由で新たなプラットフォームへの移植が難しいと主張した。単純すぎ、低レベルすぎ、Win32 GUI API と結びつきすぎているため、Motif や OS X Carbon といった他のGUIツールキットへの対応が難しいとした\[4\]。

developer.com にて Mauro Marinillia は「SWTは Swing に比較すると単純すぎるように見える。Swingは多くの洗練された機能を持っているから（例えば、精巧なSwingクラス階層、交換可能なルック・アンド・フィール、[Model View Controller手法など](https://ja.wikipedia.org/wiki/Model_View_Controller "wikilink")）」と主張した。これに対して、Model View Controller のような複雑な問題に一種の強制的な正しい手法を適用することは良いことだと思う人もいるだろう。Marinillia はさらに「（SWTと比較して）Swingの提供する機能は豊富で洗練されており、抽象化レベルが高い（そのため、特製のGUI部品で複雑なGUIを構築するのが容易である）」と続け、「一般に SWT はとっつきやすいが、複雑なGUIをそれで構築しようとすると、Swing の方がより柔軟で容易な結果を生む」とした。

SWTは Swing その他の高レベルなGUIツールキットが提供する Model View Controller アーキテクチャを実装していないが、Eclipse プロジェクトの1つとして開発された [JFace](https://ja.wikipedia.org/wiki/JFace "wikilink") ライブラリがプラットフォームに依存しない高度な Model View Controller をSWT上に実装している。開発者は、ツリー/テーブル/リストのような複雑なSWTコントロールについて、JFaceが提供する柔軟な抽象データモデルを使うこともできるし、SWTのコントロールを直接使うこともできる。

## 性能

SWTは「高性能」GUIツールキットとして、Swingよりもシステムリソースを浪費しないよう設計された\[5\]。SWTとSwingの[ベンチマーク](https://ja.wikipedia.org/wiki/ベンチマーク "wikilink")比較がいくつか行われ、SWTがSwingより効率がよいことが示されている。しかし、ベンチマークに使われたアプリケーションはそれほど複雑ではなく、SWTが常にSwingより性能が良いとは言えない\[6\]。

## ルック・アンド・フィール

SWTウィジェットは、ネイティブウィジェットと同じ[ルック・アンド・フィール](../Page/ルック・アンド・フィール.md "wikilink")を提供する。これとは対照的に、Swingのウィジェットはネイティブウィジェットに近い複製である。場合によっては、この違いが見た目にも明らかとなる。例えば、Mac OS X のツリーウィジェット機能はツリーの展開時にアニメーションを行い、デフォルトボタンもユーザーがフォーカスした際にアニメーションを行う。Swing では、これらのアニメーションは行われない。

SWT はネイティブGUIコードの単純なラッパーであるため、（ネイティブAPIが互換を保つ限り）ネイティブコードが変更されても大きな修正を必要としない。OSベンダーはAPI上の互換性を保つよう常に気をつけている。Swingでは事情が異なる。Swing は動作中のアプリケーションのルック・アンド・フィールを交換可能であり、ネイティブGUIのテーマをエミュレート可能である。この機能はOSのGUIが変更されるたびに、その変化（テーマやその他のルック・アンド・フィールの更新）を反映しなければならない。逆に言えば、ネイティブAPIが変更されれば、SWTは修正が必須となるが、Swingは修正の必要がない。

SWT は「プラットフォームとの密な統合」を目指しており、ネイティブウィジェットを利用する。developer.com の Mauro Marinillia によると「ネイティブプラットフォームとの密な統合が必要なら、SWTはよい選択だ」としている\[7\]。このような密な統合の利点を生かした例として、SWTは [Microsoft Windows](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink") の[ActiveX](../Page/ActiveX.md "wikilink")オブジェクトもラップ可能である。

## 拡張性と他の Java コードとの比較

ネイティブコードを利用するため、SWTクラスでは全ウィジェットクラスについて、継承は容易には許されない。このため、拡張性に問題があるとする人もいる\[8\]。この点ではSwingの方が容易にカスタマイズ可能である。どちらのツールキットも新たなウィジェットをJavaコードだけを使って書くことができる。

SWTはAWT同様、手動でオブジェクトの解放をする必要がある。SwingやJavaの[メモリ](https://ja.wikipedia.org/wiki/メモリ "wikilink")の自動[ガベージコレクション](../Page/ガベージコレクション.md "wikilink")とは異なる。close() しないといけないI/Oリソースと同じである。SWTオブジェクトは "dispose()" メソッドを使って明示的に解放する必要があり、[C言語](../Page/C言語.md "wikilink")の "free" に似ている\[9\]。これをしないと、[メモリリーク](../Page/メモリリーク.md "wikilink")などの好ましくない結果を生じる。ただし、親子関係にある Widget は親を dispose() すれば、子も dispose() される。この問題について、「リソースの明示的解放の必要性は、少なくとも平均的なJava開発者にとっては、開発時間とコストに悪影響を及ぼす」とのコメントもある。さらに「これはありがた迷惑である。Swingがより自動化され遅いのに対して、SWTはよりきめ細かいコントロールができるが複雑になる」としている\[10\]。SWTが手動でのオブジェクト解放を必要とするのは、ネイティブオブジェクトを使っているのが主な原因である。つまり、それらオブジェクトは Java VM の管理範囲外にあり、Java VM からそれらが解放可能かどうかを判断できない。

## プラットフォームサポート

[250px](https://ja.wikipedia.org/wiki/ファイル:Azureus2.5.0.4.png "wikilink") 環境での [Azureus](https://ja.wikipedia.org/wiki/Azureus "wikilink") [BitTorrent](https://ja.wikipedia.org/wiki/BitTorrent "wikilink") クライアント\]\]

SWTはプラットフォーム固有のGUIライブラリへのラッパーであるため、Javaが動作するプラットフォーム全てで動作するとは限らない。つまり、SWTはGUIライブラリ毎に移植が必要であり、Javaが新たなプラットフォームに移植されても、即座にSWTが移植されるとは限らない（Swing や AWT はJava本体の一部だが、SWTはそうではない）。また、Windows 上のSWT以外は、比較的効率が悪いと言われている\[11\]。SWTはプラットフォーム毎に異なるネイティブライブラリを使っているため、プラットフォーム固有のバグもSWTではそのまま存在している。

SWTはSwingよりも低レベルな詳細を開発者に提示する。これはSWTがネイティブライブラリで提供されるGUI機能の上の層であるためであり、ネイティブGUIコードを開発者に提示するのも意図的と思われる。SWTの目的は、高度なユーザインタフェース設計フレームワークを提供することではなく、可能な限り多数のプラットフォームで薄いユーザインタフェースAPIを提供し、その上に高度なGUIアプリケーションを構築できるだけの機能を提供することである。

SWTの実装はプラットフォーム毎に異なるので、複数のプラットフォーム対応としてアプリケーションを配布する際には、プラットフォーム毎のSWT（JARファイル）が必要になる。

SWTは[Javaクラスライブラリ](https://ja.wikipedia.org/wiki/Javaクラスライブラリ "wikilink")を必要最小限しか使っていないため、古いJDK（例えば 1.1.8）でも動作するし、Javaクラスライブラリを完全実装していない携帯機器でも動作すると言われている。

2006年3月現在、SWTがサポートされているプラットフォーム/GUIライブラリは次の通りである。

  - [Microsoft Windows](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink") と32ビット Java VM
  - [AIX](https://ja.wikipedia.org/wiki/AIX "wikilink"), [FreeBSD](../Page/FreeBSD.md "wikilink"), [Linux](https://ja.wikipedia.org/wiki/Linux "wikilink"), [HPUX](../Page/HP-UX.md "wikilink"):
      - [Motif](../Page/Motif_\(GUI\).md "wikilink")
      - [GTK+](https://ja.wikipedia.org/wiki/GTK+ "wikilink")
  - [Mac OS](https://ja.wikipedia.org/wiki/Mac_OS "wikilink"): [Carbon](../Page/Carbon.md "wikilink")
      - Cocoa 対応は開発中（Mac OS X 10.5 64ビット版が Carbon をサポートしていないため）
  - [QNX Photon](https://ja.wikipedia.org/wiki/QNX "wikilink")
  - [Pocket PC](https://ja.wikipedia.org/wiki/Pocket_PC "wikilink")
  - Swing （SWTSwing経由）

## SWTアプリケーション

SWTを利用しているアプリケーションとして、以下のものがある。

  - [Vuze](https://ja.wikipedia.org/wiki/Vuze "wikilink")
  - [Eclipse](../Page/Eclipse_\(統合開発環境\).md "wikilink") とその[プラグイン](../Page/プラグイン.md "wikilink")群
  - [GumTree](http://gumtree.codehaus.org/) Platform （科学技術計算）
  - [Haystack](http://groups.csail.mit.edu/haystack/) ([PIM](https://ja.wikipedia.org/wiki/Personal_Information_Manager "wikilink"))
  - [jLibrary](http://www.jlibrary.org/repositories/jlibrary) （[コンテンツ管理システム](https://ja.wikipedia.org/wiki/コンテンツ管理システム "wikilink")）
  - [Panoptes](http://panoptesmgmt.sourceforge.net/) （グラフィカルな[JMXマネージャ](../Page/Java_Management_Extensions.md "wikilink")）
  - [RSSOwl](http://www.rssowl.org/) フィードアグリゲータ
  - [sancho](http://sancho-gui.sourceforge.net/) （[P2P](https://ja.wikipedia.org/wiki/ファイル共有ソフト "wikilink") GUI）
  - [uDig](http://udig.refractions.net/confluence/display/UDIG/Home) （[地理情報システム](../Page/地理情報システム.md "wikilink")）
  - [Xinity BASE](http://sourceforge.net/projects/xinity/)

## SWT関係文書

GUIツールキットとしてはSwingよりも新しいため、SWT関連の文書/書籍はSwingに比べて少ない。

*SWT: The Standard Widget Toolkit* は、Eclipse Foundation 推薦のSWT解説書である\[12\]。他にもSWT関連書籍として以下のものがある。

  -
  -
  -
  -
## ウェブ上でのSWT

Eclipseコミュニティでのの動きとして、SWT（とJFace）をウェブ向けのウィジェットツールキットとして移植しようとしている。[Eclipse RAP](https://ja.wikipedia.org/wiki/Rich_AJAX_Platform "wikilink") \[13\] (Rich Ajax Platform) は Qooxdoo AJAX ライブラリと SWT API を組み合わせたものである。他の Java AJAX プロジェクト（Echo2 や [GWT](https://ja.wikipedia.org/wiki/Google_Web_Toolkit "wikilink")）と同様、SWT API を使うことで、デスクトップと同じ形でWeb用のアプリケーション開発が可能となる。

## 開発

Eclipse が人気を得てきた結果として、Swing と SWT をある意味で「統合」しようとする活動もある。

Swing と SWT の統合については、以下のようにいくつかの異なる手法が存在している。

  - Eclipse プロジェクトでは、Swing ウィジェットを SWT コンテナウィジェットに埋め込もうとしている。
  - *SwingWT* は Swing API の代替実装を提供しようとするプロジェクトである。その1つとして SWT 上で Swing ウィジェットを使えるようにするプロジェクトが行われている\[14\]。
  - *SWTSwing* は、逆に Swing 上で SWT API を提供するプロジェクトである。これにより SWT がサポートされていないプラットフォーム上でも Java さえ動作すれば SWT アプリケーションを実行可能となる\[15\]。

## 脚注

## 外部リンク

  - [SWT公式サイト](http://www.eclipse.org/swt/)
  - [Eclipseアプリケーション](http://www.oneclipse.com/Members/admin/news/swt-sightings/)
  - [Eclipseアプリケーション、パート2](http://www.oneclipse.com/Members/admin/news/swt-sightings-vol-2/)
  - [Eclipseドキュメンテーション](http://www.eclipse.org/documentation/) "platform plug-in developer guide" にSWTに関する文書がある。
  - [SWT Javadoc API](http://help.eclipse.org/help31/nftopic/org.eclipse.platform.doc.isv/reference/api/org/eclipse/swt/package-summary.html) eclipse.org

[Category:ウィジェット・ツールキット](https://ja.wikipedia.org/wiki/Category:ウィジェット・ツールキット "wikilink") [Category:Eclipse_Foundation](https://ja.wikipedia.org/wiki/Category:Eclipse_Foundation "wikilink")

1.
2.
3.
4.
5.  {{ cite web | url = <http://weblogs.java.net/blog/aiqa/archive/2004/11/why_i_choose_sw.html> | title = Why I choose SWT against Swing | first = Ozgur | last = Akan | date = 2004年11月19日 | accessdate = 2006年11月7日 }}
6.  [Swing vs. SWT Performance - Have a Look at the Call Stacks](http://www.javalobby.org/java/forums/t65168.html) Javalobby、StephenStrenn、2006年3月3日
7.  {{ cite web | title = Swing and SWT: A Tale of Two Java GUI Libraries | url = <http://www.developer.com/java/other/article.php/2179061> | first = Mauro | last = Marinilli | accessdate = 2006年11月7日 }}
8.
9.  The Java developers guide to Eclipse, 2nd ed., p359
10.
11.
12. {{ cite book | author=Steve Northover, Mike Wilson | title=SWT: The Standard Widget Toolkit | publisher=Addison-Wesley }}
13. [Rich Ajax Platform (RAP)](http://www.eclipse.org/rap)
14. [SwingWT](http://swingwt.sourceforge.net/)
15. [swtswing](http://swtswing.sourceforge.net)
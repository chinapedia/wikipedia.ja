> この記事は[JFace](https://ja.wikipedia.org/wiki/JFace)から翻訳されています。


**JFace** は、[Eclipseプロジェクトによる](../Page/Eclipse_\(統合開発環境\).md "wikilink")「退屈な作業となる[UI機能の実装を支援する](../Page/ユーザインタフェース.md "wikilink")[クラスを提供するUI](../Page/クラス_\(コンピュータ\).md "wikilink")[ツールキット](https://ja.wikipedia.org/wiki/ウィジェット・ツールキット "wikilink")」である\[1\]。下位の[ウィジェット](https://ja.wikipedia.org/wiki/ウィジェット "wikilink")の上層に位置し、一般的なUIプログラミングタスクを制御するクラスを提供する。[Standard Widget Toolkit](../Page/Standard_Widget_Toolkit.md "wikilink") に [Model View Controller](https://ja.wikipedia.org/wiki/Model_View_Controller "wikilink") の視点を持ち込んだものと言える。

1.  ウィジェットのソート、フィルタリング、更新などの紋切り型のタスクを処理する Viewer クラスを提供する。
2.  独自の動作を定義し特定のコンポーネント（メニューアイテム、ツールアイテム、プッシュボタンなど）に割り当てることを可能にするアクションを提供する。
3.  イメージとフォントを格納するレジストリを提供する。
4.  標準ダイアログとウィザードを定義し、ユーザーとの複雑な相互作用を構築するフレームワークを定義している。
5.  その目標は、全てのUIアプリケーションに共通する問題を解決することや基盤となっているウィジェットシステムについて心配することなく、開発者が自分のアプリケーションの実装に専念できるようにすることである。
6.  Eclipse プロジェクトで JFace を開発するに当たって、プログラマから[SWTコンポーネントの実装を隠すという意図があったわけではない](../Page/Standard_Widget_Toolkit.md "wikilink")。JFace は SWT に依存しているが、SWT は JFace には依存していない。さらに、Eclipse Workbench は JFace と SWT を使っており、状況によっては JFace をバイパスして SWT を直接使っている。

## 脚注

## 外部リンク

  - [Wiki JFace](http://wiki.eclipse.org/index.php/JFace)
  - [Rich clients with the SWT and JFace](http://www.javaworld.com/javaworld/jw-04-2004/jw-0426-swtjface.html)

[Category:ウィジェット・ツールキット](https://ja.wikipedia.org/wiki/Category:ウィジェット・ツールキット "wikilink") [Category:Eclipse_Foundation](https://ja.wikipedia.org/wiki/Category:Eclipse_Foundation "wikilink")

1.  [Eclipse programmer's guide entry on JFace](http://help.eclipse.org/help32/index.jsp?topic=/org.eclipse.platform.doc.isv/guide/jface.htm)
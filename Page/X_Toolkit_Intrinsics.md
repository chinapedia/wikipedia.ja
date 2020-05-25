> この記事は[X Toolkit Intrinsics](https://ja.wikipedia.org/wiki/X_Toolkit_Intrinsics)から翻訳されています。


[frame](https://ja.wikipedia.org/wiki/ファイル:X-client-libraries.svg "wikilink") **X Toolkit Intrinsics** は、[X Window System](../Page/X_Window_System.md "wikilink") で使われている[ライブラリ](../Page/ライブラリ.md "wikilink")である。**Xt**（X toolkit の略）とも呼ばれる。より正確には、低レベルな [Xlib](../Page/Xlib.md "wikilink") ライブラリを使い、[ウィジェットを使った](../Page/ウィジェット_\(GUI\).md "wikilink") [X Window System](../Page/X_Window_System.md "wikilink") ソフトウェアを開発するための使い易い（[オブジェクト指向的](../Page/オブジェクト指向プログラミング.md "wikilink")）[APIを提供するライブラリである](../Page/アプリケーションプログラミングインタフェース.md "wikilink")。[C言語](../Page/C言語.md "wikilink")と[C++](../Page/C++.md "wikilink")向けの[言語バインディングがある](../Page/束縛_\(情報工学\).md "wikilink")。

低レベルな Xlib ライブラリは X11[サーバ](../Page/サーバ.md "wikilink")とのやり取りのための機能を提供するが、[GUIで使われる各種オブジェクト](https://ja.wikipedia.org/wiki/グラフィカルユーザインタフェース "wikilink")（ボタン、メニューなど）を実装するための機能は全く提供しない。そのようなオブジェクトを[ウィジェットと呼ぶ](../Page/ウィジェット_\(GUI\).md "wikilink")。X Toolkit Intrinsics ライブラリは、ウィジェットを作成するのに必要な機能を提供するが、特定のウィジェットを提供するわけではない。特定のウィジェットの実装は、X Toolkit Intrinsics を使った上位のライブラリ（[Xaw](https://ja.wikipedia.org/wiki/Xaw "wikilink") や [Motif](../Page/Motif_\(GUI\).md "wikilink")）でなされる。これを[ウィジェット・ツールキット](../Page/ウィジェット・ツールキット.md "wikilink")と呼ぶ。

従って、X Toolkit Intrinsics を直接使って新たなウィジェットを作成することができる。一般にアプリケーションは様々なウィジェットを必要とするため、一部のウィジェットを X Toolkit Intrinsics を直接使って新たに作ったとしても、他のウィジェットは Xaw や Motif にある既存のものを使うのが普通である。

ウィジェット・ツールキットには、X Toolkit Intrinsics を使わずに Xlib を直接使っているものもある。

## 関連項目

  - [X Window System プロトコルとアーキテクチャ](https://ja.wikipedia.org/wiki/X_Window_System_プロトコルとアーキテクチャ "wikilink")

## 外部リンク

  - [X Toolkit Intrinsics - C Language Interface](http://www.x.org/docs/Xt/)
  - [The X Toolkit Intrinsics FAQ](http://www.faqs.org/faqs/Xt-FAQ/)
  - [The place of Intrinsics in X11](http://www.cs.cf.ac.uk/Dave/X_lecture/node4.html#SECTION00420000000000000000)
  - [TestXt2](http://www.kenjennings.cc/st/stprgux.html#testxt2) Xt/Xaw を使ったメニューバーのプログラム例（圧縮アーカイブ）

[Category:X_Window_System](https://ja.wikipedia.org/wiki/Category:X_Window_System "wikilink") [Category:ライブラリ_(プログラミング)](https://ja.wikipedia.org/wiki/Category:ライブラリ_\(プログラミング\) "wikilink")
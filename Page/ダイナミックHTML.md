> この記事は[HTML](https://ja.wikipedia.org/wiki/HTML)から翻訳されています。


**ダイナミックHTML**（、DHTML）は、静的な[HTMLの内容を](../Page/HyperText_Markup_Language.md "wikilink")[CSSと](../Page/Cascading_Style_Sheets.md "wikilink")等の[クライアントサイド](../Page/クライアント_\(コンピュータ\).md "wikilink")[スクリプト言語](../Page/スクリプト言語.md "wikilink")を用いて動的に変更するウェブ技術を指す抽象概念である。

視覚的な訴求効果の高いHTMLドキュメントを作成できるなどとして、[1997年](https://ja.wikipedia.org/wiki/1997年 "wikilink")に起こった[ネットスケープ](https://ja.wikipedia.org/wiki/ネットスケープ "wikilink")と[マイクロソフト](../Page/マイクロソフト.md "wikilink")の[ブラウザ戦争](https://ja.wikipedia.org/wiki/ブラウザ戦争 "wikilink")で生まれた。

## 背景

1997年当時は  からHTMLを参照、制御する方式が各社不統一であり、[ウェブブラウザ](../Page/ウェブブラウザ.md "wikilink")ごとに別々の  を書く必要があった。この状況を打開すべく1998年10月に[W3Cはクライアントサイドスクリプト言語とHTMLドキュメントの緩衝材としての役割を果たす](../Page/World_Wide_Web_Consortium.md "wikilink") （DOM）を勧告した。これによりDOMをサポートする新型のブラウザ（ 5.0 や、 6.0、、 7.0 など）であれば、ブラウザを問わずひとつの記述で HTMLドキュメントを参照、制御できるようになった。登場当初は応用方法が分からず、単なる飾りとして使われていたが、[2005年](https://ja.wikipedia.org/wiki/2005年 "wikilink")の[Ajax](https://ja.wikipedia.org/wiki/Ajax "wikilink")の提唱前後に[Webアプリケーションの構築手法として広く用いられるようになった](https://ja.wikipedia.org/wiki/ウェブアプリケーション "wikilink")。

##

（HTA）はダイナミックHTMLの機能を利用して  の[アプリケーションを作成する仕組みである](../Page/アプリケーションソフトウェア.md "wikilink")。ダイナミックHTMLの登場によってインタラクティブな[ウェブページ](../Page/ウェブページ.md "wikilink")を容易に作成できるようになったが、HTAはそれらの仕組みを通常のアプリケーションの作成に応用する試みである。HTAの作成は、単にHTMLファイルの拡張子を「`.hta`」にするだけである。ダイナミックHTMLに対するHTA固有の拡張は`HTA:APPLICATION`要素、[ActiveX](https://ja.wikipedia.org/wiki/ActiveX "wikilink")やローカルファイルへのアクセスに制限がないことなどである。実行には  5.0 以上が必要である。

、ファイルのフルパスにパソコンのアカウント名などの隠蔽したい情報が含まれている場合には注意が必要である。

##

から搭載されたでは、という小型のアプリケーションを実行することができる。 は HTML、CSS、 を用いたものである。HTMLとスタイルシートで外観を定義し、 でそれを制御するというもので、一足早く登場した  というソフトウェアで実現されていた機能に似ている。ただし、正確に言えば  そのものは、 から搭載されたウィンドウ一覧表示機能、の拡張であり、 は普段は隠れている点、インターフェースなどの記述に用いるマークアップ言語などが  とは異なる。また  制御のパッケージは  の後続技術である。Widgetの内部からはネットワーク接続を行ったり、各アプリケーションにイベントを送信したり、アプリケーションや[シェルスクリプト](../Page/シェルスクリプト.md "wikilink")などを実行することが可能になる。

## 関連項目

  - [XUL](https://ja.wikipedia.org/wiki/XUL "wikilink")

  - (XAML)

  - [Ajax](https://ja.wikipedia.org/wiki/Ajax "wikilink")

## 外部リンク

  - 標準に準拠したDHTML
      - [DOMを利用した3Dアニメ](https://web.archive.org/web/20041206002550/http://www.world-direct.com/mozilla/dhtml/funo/3dcube/index.htm)（2004年12月6日時点の[アーカイブ](../Page/インターネットアーカイブ.md "wikilink")）
      - [](https://web.archive.org/web/20040927074625/http://devedge.netscape.com/viewsource/2001/updating-dhtml-web-pages/)（2004年9月27日時点の[アーカイブ](../Page/インターネットアーカイブ.md "wikilink")） -
  - 互換性の無いDHTML
      - \[<https://web.archive.org/web/20041204092222/http://developer.netscape.com/tech/dynhtml/> （2004年12月4日時点の[アーカイブ](../Page/インターネットアーカイブ.md "wikilink")） -
      - [](https://web.archive.org/web/20050311042303/http://www.microsoft.com/japan/msdn/library/ja/jpisdk/dhtml/dhtml.asp)（2005年3月11日時点の[アーカイブ](../Page/インターネットアーカイブ.md "wikilink")） - MSDN

[Category:HTML](https://ja.wikipedia.org/wiki/Category:HTML "wikilink")
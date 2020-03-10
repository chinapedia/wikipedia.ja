> この記事は[MUMPS](https://ja.wikipedia.org/wiki/MUMPS)から翻訳されています。


**MUMPS**とは、1960年代末に[アメリカの](https://ja.wikipedia.org/wiki/アメリカ合衆国 "wikilink")[マサチューセッツ総合病院で医療情報処理用のアプリケーションを開発し実行するために開発された](../Page/マサチューセッツ州.md "wikilink")、プログラミング言語とその環境 である。

MUMPSという名前は、「**M**assachusetts general hospital **U**tility **M**ulti-**P**rogramming **S**ystem」 の[頭字語](../Page/頭字語.md "wikilink")である。

病院が自分達の業務を実装するために、高価な[メインフレーム](../Page/メインフレーム.md "wikilink")ではなく、[ミニコンなどの比較的安価な](../Page/ミニコンピュータ.md "wikilink")[コンピュータ](../Page/コンピュータ.md "wikilink")上で軽快に動作するように開発した。オリジナルのソースコードこそ公開されてはいないが、仕様は全て公開して自由に利用できるようにしたため、一時期は複数のソフトウェアベンダーがMUMPS処理系の開発・販売をしていた。

MUMPSの処理系は、ハードウェアが直接実行可能な[機械語](../Page/機械語.md "wikilink")コードを生成するのではなく、コンパイラは[仮想機械](../Page/仮想機械.md "wikilink")の[中間言語](../Page/中間言語.md "wikilink")コードを生成し、それをインタプリタ（仮想機械）で実行する。また、ベースのプラットフォームの違いを仮想機械のレイヤで抽象化し、プログラマには違いを意識させず、アプリケーションのポータビリティを保つ。

また、実行環境に専用のDBMSを内包し、かつ、その機能・性能がデータベース専用のソフトウェアに迫る・または凌駕するほど強力であるため、アメリカの医療界を通じて日本のみならず全世界の医療界でも広域に普及した。ただし、システム利用者・運用管理担当はパッケージソフトウェアに組み込まれたMUMPSを利用している場合が多いため、広く利用されている割に知名度は低い。

## M言語

**M言語** (M Language) は、**MUMPS**で動作するアプリケーションを記述する[プログラミング言語](../Page/プログラミング言語.md "wikilink")である。(**M**UMPS用の開発言語であるため → M言語）

**ISO/IEC11756** Information technology−Programming languages−MUMPSととしてISO規格となっており、日本では 「JIS X 3011:1995 プログラム言語 MUMPS」 として国家規格となっている。

## MUMPSのデータベース

  - 特徴(他分岐ツリー構造、スパース配列によるデータ格納により「多次元データベース」と称される。)

## 近年のMUMPS

かつてあった複数のMUMPSベンダーは、度重なる買収・合併の結果により、現在は数社のみ存在している（インターシステムズ社、F.I.S社等）。アプリケーション開発手法としてMUMPS/M言語そのものは医療業界以外に広く普及しなかった。

しかし、インターシステムズ社がMUMPSのDBMS部分を強化し、かつM言語以外の多言語（Java/C・C++/VBなど）、Web技術（XML/Webサービス）による短期開発 ([RAD](https://ja.wikipedia.org/wiki/RAD_\(計算機プログラミング環境\) "wikilink")) 機能、データベースとしての運用管理機能（[分散データベース](https://ja.wikipedia.org/wiki/分散データベース "wikilink")、ログによる可用性向上）を強化して、多次元データベース「[Caché](https://ja.wikipedia.org/wiki/Caché "wikilink")」（**キャシェー**と読む）として販売している。原理的に複雑なツリー構造となっているデータの検索や文字列処理が得意なので、データベース全体が巨大で見通しの悪いようなアプリケーションにおいて、より高いパフォーマンスが期待される。CSPと呼ばれるWebアプリ開発では、ホームページ制作ソフトとしてポピュラーな[Dreamweaver](https://ja.wikipedia.org/wiki/Dreamweaver "wikilink")を画面エディタとして使えるのも、魅力的と言える。

「[Caché](https://ja.wikipedia.org/wiki/Caché "wikilink")」は現在医療分野のみならず、開発効率のよさと運用性能の高さにより、RDBMSの独擅場であった金融・製造・物流などの基幹業務など多岐にわたり採用されている。[ODBCドライバが用意されているので](../Page/Open_Database_Connectivity.md "wikilink")、他のDBMSからの移行もさほど困難ではないだろう。

## 関連項目

  - [Caché](https://ja.wikipedia.org/wiki/Caché "wikilink")
  - [GT.M](https://ja.wikipedia.org/wiki/GT.M "wikilink")
  - [メルヴィン・コンウェイ](https://ja.wikipedia.org/wiki/メルヴィン・コンウェイ "wikilink")

## 外部リンク

  - [日本Mテクノロジー学会](http://www.mta.gr.jp)
  - [インターシステムズ(米)](http://www.intersystems.com)
  - [インターシステムズジャパン社](http://www.intersystems.co.jp)

[Category:統合開発環境](https://ja.wikipedia.org/wiki/Category:統合開発環境 "wikilink") [Category:プログラミング言語](https://ja.wikipedia.org/wiki/Category:プログラミング言語 "wikilink")
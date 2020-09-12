> この記事は[Ggplot2](https://ja.wikipedia.org/wiki/Ggplot2)から翻訳されています。


**ggplot2**は、 統計プログラミング言語[Rのデータ視覚化パッケージである](../Page/R言語.md "wikilink")。2005年にHadkey Wickhamによって作成されたggplot2は、[リーランド・ウィルキンソン](https://ja.wikipedia.org/wiki/リーランド・ウィルキンソン "wikilink")のGrammar of Graphicsの実装である。これは、グラフをスケールやレイヤーなどのセマンティックコンポーネントに分割するデータ視覚化の一般的なスキームである。

ggplot2は、Rの基本グラフィックスの代替として機能し、一般的な縮尺のWebおよび印刷表示のデフォルトが多数含まれている。 2005年以来、ggplot2は最も人気のあるRパッケージの1つになりつつある。 \[1\] \[2\]

GNU GPL v2の下でライセンスされている。 \[3\]



## 更新情報

2012年3月2日、ggplot2バージョン0.9.0がリリースされ、内部組織、スケール構築、およびレイヤーに多数の変更が加えられた。 \[4\]

2014年2月25日に、Hadley Wickhamは「ggplot2がメンテナンスモードに移行していることを正式に発表しました。 これは、新しい機能を追加しなくなったことを意味しますが、引き続き主要なバグを修正し、プルリクエストとして送信された新しい機能を検討します。 この重要なマイルストーンを認識して、ggplot2の次のバージョンは1.0.0 "になります。 \[5\] 2015年12月21日に、ggplot 2.0.0がリリースされた。 発表では、「ggplot2には現在、公式の拡張メカニズムがあり、これは、他の人が自分の統計、ジオム、位置を簡単に作成し、他のパッケージで提供できることを意味する。」としている。 \[6\]

## 基本グラフィックスおよび他のパッケージとの比較

ベースRグラフィックスとは対照的に、ggplot2では、ユーザーが高レベルの抽象化で、図表内のコンポーネントを追加、削除、または変更できる。 \[7\] この抽象化にはコストがかかり、ggplot2は格子グラフィックスよりも低速である。 \[8\]

ベースRグラフィックスの潜在的な制限の1つは、プロッティングデバイスに入力するために使用される「ペンと紙のモデル」である。 \[9\] インタプリタからのグラフィック出力は、プロットの個別の要素ごとに個別にではなく、プロットデバイスまたはウィンドウに直接追加される。 \[10\] この点では、ラティスパッケージに似ているが、ウィッカムはggplot2はウィルキンソンからより正式なグラフィックスモデルを継承していると主張している。 \[11\] そのため、高度なモジュール化が可能です。同じ基になるデータを、さまざまなスケールまたはレイヤーで変換できる。 \[12\] \[13\]

プロットは、便利な関数`qplot()`を介して作成できる。引数とデフォルトは、ベースRの`plot()`関数と同様のものである。 \[14\] \[15\] より複雑なプロット能力は、 `ggplot()`を介して利用できる。これにより、ユーザーは文法のより明示的な要素にさらされる。 \[16\]

## 関連プロジェクト

  - Pythonのggplot \[17\]
  - Plotly-インタラクティブなオンラインggplot2グラフ\[18\]
  - gramm、ggplot2に触発されたMATLABのプロットクラス\[19\]
  - gadfly、主にggplot2 \[20\]基づいた、 [ジュリアで書かれたプロットと視覚化のためのシステム](https://ja.wikipedia.org/wiki/Julia_\(プログラミング言語\) "wikilink")
  - Chart :: GGPlot- [Perl](../Page/Perl.md "wikilink")の ggplot2ポート\[21\]

## 参照資料

## 参考文献

  -
  -
## 外部リンク

  - [ggplot2の](https://ggplot2.tidyverse.org/)サンプルコードとドキュメント
  - [GitHub](https://ja.wikipedia.org/wiki/GitHub "wikilink")上の[ggplot2](https://github.com/hadley/ggplot2)リポジトリ

[Category:アプリケーションソフト_(製品)](https://ja.wikipedia.org/wiki/Category:アプリケーションソフト_\(製品\) "wikilink") [Category:フリープログラミングツール](https://ja.wikipedia.org/wiki/Category:フリープログラミングツール "wikilink") [Category:画像処理ソフト](https://ja.wikipedia.org/wiki/Category:画像処理ソフト "wikilink") [Category:フリーソフトウェア](https://ja.wikipedia.org/wiki/Category:フリーソフトウェア "wikilink") [Category:統計処理ツール](https://ja.wikipedia.org/wiki/Category:統計処理ツール "wikilink")

1.
2.
3.  <https://cran.r-project.org/web/packages/ggplot2/index.html>
4.
5.
6.  ggplot 2.0.0 <http://blog.rstudio.org/2015/12/21/ggplot2-2-0-0/>
7.
8.  <http://learnr.wordpress.com/2009/08/26/ggplot2-version-of-figures-in-lattice-multivariate-data-visualization-with-r-final-part/>
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
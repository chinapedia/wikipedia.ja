> この記事は[Tab-Separated Values](https://ja.wikipedia.org/wiki/Tab-Separated_Values)から翻訳されています。


**Tab-Separated Values** (**TSV**) は、[データベースにおける表や](https://ja.wikipedia.org/wiki/表_\(データベース\) "wikilink")[表計算データなど](../Page/表計算ソフト.md "wikilink")、表形式で[データ](../Page/データ.md "wikilink")を格納するためのシンプルなテキスト形式のデータ形式であり\[1\]、[データベース](../Page/データベース.md "wikilink")間で情報を交換する方法の1つである\[2\]。

TSV形式における各[レコードは](https://ja.wikipedia.org/wiki/組_\(データベース\) "wikilink")、[テキストファイル](../Page/テキストファイル.md "wikilink")の1行である。レコードの各フィールド値は、[タブ文字](https://ja.wikipedia.org/wiki/タブ文字 "wikilink")で区切られる。すなわち、TSV形式は（区切り文字区切り形式）の一種である。**タブ区切り形式**ともいう。

TSVフォーマットはシンプルなファイルフォーマットであり、多くのコンピュータプログラムが対応しているため、異なるコンピュータプログラム間で表形式のするためによく使用される。TSVは、一般的に使用されている[Comma-Separated Values](../Page/Comma-Separated_Values.md "wikilink")（CSV形式、タブ区切り形式）に代わるものである。CSV形式では[コンマ](../Page/コンマ.md "wikilink")を[区切り文字](https://ja.wikipedia.org/wiki/区切り文字 "wikilink")としているため、フィールドにコンマが含まれる場合には、これを[エスケープしないと問題が生じる](../Page/エスケープ文字.md "wikilink")。コンマはテキストデータでは頻出する文字であるが、タブは一般的なテキストの中に出現することは稀である。TSVのIANA標準\[3\]では、フィールドにタブ文字の使用を禁止している。

## 例

の先頭をTSV形式にすると、以下のようになる。

    Sepal length    Sepal width Petal length    Petal width Species
    5.1 3.5 1.4 0.2 I. setosa
    4.9 3.0 1.4 0.2 I. setosa
    4.7 3.2 1.3 0.2 I. setosa
    4.6 3.1 1.5 0.2 I. setosa
    5.0 3.6 1.4 0.2 I. setosa

上記のTSVプレーンテキストは、以下の表データに対応している。

| Sepal length | Sepal width | Petal length | Petal width | Species   |
| ------------ | ----------- | ------------ | ----------- | --------- |
| 5.1          | 3.5         | 1.4          | 0.2         | I. setosa |
| 4.9          | 3.0         | 1.4          | 0.2         | I. setosa |
| 4.7          | 3.2         | 1.3          | 0.2         | I. setosa |
| 4.6          | 3.1         | 1.5          | 0.2         | I. setosa |
| 5.0          | 3.6         | 1.4          | 0.2         | I. setosa |

## 関連項目

  - [フラットファイルデータベース](https://ja.wikipedia.org/wiki/フラットファイルデータベース "wikilink")
  - [区切り文字](https://ja.wikipedia.org/wiki/区切り文字 "wikilink")

## 脚注

### 注釈

### 出典

## 参考文献

  - [IANA](../Page/Internet_Assigned_Numbers_Authority.md "wikilink"), Text Media Types, [text/tab-separated-values](http://www.iana.org/assignments/media-types/text/tab-separated-values), Paul Lindner, U of MN Internet Gopher Team, June 1993
  - [Tab Separated Values (TSV): a format for tabular data exchange](http://www.cs.tut.fi/~jkorpela/TSV.html), Jukka Korpela, created 2000-09-01, last update 2005-02-12.

## 外部リンク

  - [Tab Separated Value File Format](https://help.gnome.org/users/gnumeric/stable/gnumeric.html#file-format-tab), [Gnumeric](../Page/Gnumeric.md "wikilink") manual

[Category:データベース](https://ja.wikipedia.org/wiki/Category:データベース "wikilink") [Category:オープンフォーマット](https://ja.wikipedia.org/wiki/Category:オープンフォーマット "wikilink") [Category:データシリアライゼーションフォーマット](https://ja.wikipedia.org/wiki/Category:データシリアライゼーションフォーマット "wikilink") [Category:テキストファイルフォーマット](https://ja.wikipedia.org/wiki/Category:テキストファイルフォーマット "wikilink")

1.  [How To Use Tab Separated Value (TSV) Files](https://www.imf.org/external/help/tsv.htm) Published by the [International Monetary Fund](https://ja.wikipedia.org/wiki/International_Monetary_Fund "wikilink")
2.
3.
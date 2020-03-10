> この記事は[UTX](https://ja.wikipedia.org/wiki/UTX)から翻訳されています。


**UTX**（Universal Terminology eXchange）とは、AAMT（[アジア太平洋機械翻訳協会](https://ja.wikipedia.org/wiki/アジア太平洋機械翻訳協会 "wikilink")）が策定した、シンプルな用語集形式である。[翻訳ソフト](https://ja.wikipedia.org/wiki/翻訳ソフト "wikilink")の対訳[ユーザー辞書](https://ja.wikipedia.org/wiki/ユーザー辞書 "wikilink")の標準仕様であり、人間翻訳の用語集としても使用できる。既存仕様[UPFの後継として仕様策定がされた](https://ja.wikipedia.org/wiki/UPF_\(規格\) "wikilink")\[1\]。仕様は、公開されており、無償で利用できる。仕様策定はボランティアにより行われる。

## ユーザー辞書を蓄積・共有する意義

一般に、[ルールベース機械翻訳](https://ja.wikipedia.org/wiki/ルールベース機械翻訳 "wikilink")の方式に基づく翻訳ソフトの精度に限界が見られるのは、適切な語彙が学習されていないことが原因である。しかし、対象文書に対して適切なユーザー辞書をピンポイントで作成することにより、大量の費用と労力を要する翻訳アルゴリズム自体の改善よりも効率的に改善できる。だが、実際にはユーザー辞書の作成には技能、ツール、労力を要する。そのため、小規模の翻訳では、「ユーザー辞書の作成にかかる労力」が、「翻訳ソフトで節約できる労力」を上回ることになる。UTXは、ユーザー辞書を蓄積・共有するための仕様とインフラを提供することで、「ユーザー辞書の作成にかかる労力」を減らすことができる。

また現状では、異なる翻訳ソフト メーカーの辞書には互換性がないが、UTXを経由することで相互にユーザー辞書を利用できるようになる。

さらに、現状ではさまざまな分野に用語集や訳語集（二言語用語集、多言語用語集）が存在しているが、形式がバラバラで、品詞の情報が欠落していたり、原形になっていなかったりして、人間が読むのはともかくとしても、自然言語処理には使えないことが多い。UTXは、自然言語処理的な観点からは機械的で扱いやすい形式である一方、人間が簡単に読み、編集できる用語集のためのシンプルなデータ形式としても使える。

翻訳ソフトの辞書には、「用語管理」という観点がない。たとえば、どの訳語を優先し、禁止し、あるいは暫定的に使うのか明確に区別できないことがある。UTXではこのような用語管理ができ、また各用語に定義や訳し分けの注意点などのコメントを付けることもできる。

UTXは、タブ区切り形式テキストで、原語、訳語、品詞など必要最低限の情報に限定する。実用性、ユーザーによる辞書の作りやすさ、流通のしやすさに重点を置く。必要に応じて追加の要素を定義し、拡張可能とする。2011年現在のバージョンは1.11。当初は、XML形式のUTXと対比して、UTX-Simpleと呼ばれていたが、2011年から、単にUTXと呼称されている。

## 関連項目

  - [翻訳ソフト](https://ja.wikipedia.org/wiki/翻訳ソフト "wikilink")
  - [機械翻訳](../Page/機械翻訳.md "wikilink")
  - [ユーザー辞書](https://ja.wikipedia.org/wiki/ユーザー辞書 "wikilink")
  - [辞書](https://ja.wikipedia.org/wiki/辞書 "wikilink")
  - [TBX (規格)](https://ja.wikipedia.org/wiki/TBX_\(規格\) "wikilink")
  - [UPF (規格)](https://ja.wikipedia.org/wiki/UPF_\(規格\) "wikilink")

## 出典

<references />

## 外部リンク

  - [AAMTによるUTX解説ページ](http://www.aamt.info/japanese/utx/)
  - [AAMTによるUPF解説ページ](http://www.aamt.info/japanese/upf.htm)
  - [UTXメーリングリスト](http://groups.yahoo.co.jp/group/UTX/)

[Category:機械翻訳](https://ja.wikipedia.org/wiki/Category:機械翻訳 "wikilink") [Category:XMLベースの技術](https://ja.wikipedia.org/wiki/Category:XMLベースの技術 "wikilink")

1.  <http://www.aamt.info/japanese/utx/>
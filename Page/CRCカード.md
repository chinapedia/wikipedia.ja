> この記事は[CRCカード](https://ja.wikipedia.org/wiki/CRCカード)から翻訳されています。


**CRCカード**とは、[オブジェクト指向](../Page/オブジェクト指向.md "wikilink")[ソフトウェア設計](../Page/ソフトウェア設計.md "wikilink")で使われる[ブレインストーミング](../Page/ブレインストーミング.md "wikilink")ツールである。CRC とは「クラス-責務-コラボレータ」を表す英語\[1\]の頭文字である。[ウォード・カニンガム](../Page/ウォード・カニンガム.md "wikilink")の考案である。通常、設計の最初期にどのような[クラスが必要で](../Page/クラス_\(コンピュータ\).md "wikilink")、それらがどのように相互に連携するかを決定するのに使う。

CRCカードには[インデックスカード](https://ja.wikipedia.org/wiki/インデックスカード "wikilink")が使われる（米国では76mm×127mmサイズが一般的）。それに以下のような項目を記述していく:

1.  クラス名
2.  パッケージ名（もしあれば）
3.  そのクラスの責務（すべきこと）
4.  そのクラスが自身の責務を果たすために連携しなければならない他のクラスの名前を列挙する。

一枚のカードに一個のクラスに関する以上の事項が書かれる。このとき小さなカードを使うことで設計の複雑さを最小にする（あまり詳細を書き込まない）。これは設計者らが各クラスの詳細に入り込むのを防いでクラス群の本質に集中するようにさせ、生産性を上げるためである。また、一個のクラスにあまりに多くの責務（機能）を盛り込むのを防ぐ。カードは持ち運び可能なので、テーブルの上に広げて複数人で話し合うのにも適している。

作成すべきカード（クラス）を決定する一般的な手法は、プログラムの仕様書を読み、そこに登場する名詞がクラスになるか、また、動詞が責務になるかサブクラスになるかを検討するというものである。もちろん、全ての名詞や動詞がクラスやその責務になるわけではないが、出発点としては適切である。

## 脚注

## 関連項目

## 外部リンク

  - [CRCモデルの概要](https://www.ogis-ri.co.jp/otc/swec/process/am-res/am/artifacts/crcModel.html) アジャイルモデリング公式サイト
  - [A concise introduction at extremeprogramming.org](http://www.extremeprogramming.org/rules/crccards.html)
  - [A Laboratory For Teaching Object-Oriented Thinking](https://c2.com/doc/oopsla89/paper.html) by Kent Beck and Ward Cunningham.
  - [Using CRC Cards](http://alistair.cockburn.us/crystal/articles/ucrcc/usingcrccards.html)
  - [CRC cards for Software Design](http://www.excelsoftware.com/crccards.html)

[Category:ソフトウェア設計](https://ja.wikipedia.org/wiki/Category:ソフトウェア設計 "wikilink") [Category:エクストリーム・プログラミング](https://ja.wikipedia.org/wiki/Category:エクストリーム・プログラミング "wikilink")

1.
> この記事は[Standard Generalized Markup Language](https://ja.wikipedia.org/wiki/Standard_Generalized_Markup_Language)から翻訳されています。


（スタンダード ジェネラライズド マークアップ ランゲージ、略：**SGML**）は、マニュアルなどの文書のための[マークアップ言語](https://ja.wikipedia.org/wiki/マークアップ言語 "wikilink")である。SGMLとXMLの対応（比較）については、[ジェームズ・クラークによる](https://ja.wikipedia.org/wiki/ジェームズ・クラーク_\(ソフトウェア技術者\) "wikilink")「Comparison of SGML and XML」というタイトルの、1997年12月15日に議論のためにまとめられた（何らかの公式のものではない）ノートがあり\[1\]、それによればSGML (ISO 8879) とXMLの関係はスーパーセットともサブセットとも結論付けられてはいない。XML 1.0のAppendix CではNon-Normative（参考）として、XMLはSGMLのサブセットとなる**べく**設計され（designed to be）、全てのXML文書は同時にSGMLにもconforming（準拠）でもある**べき**（should）と書かれており、前述のノートを参照せよとされている。国際標準は [ISO](https://ja.wikipedia.org/wiki/国際標準化機構 "wikilink") 8879:1986 であり、対応するJISとして JIS X 4151:1992 が存在する。

## 背景

[rightの電子版を記述するのにSGMLが利用された](https://ja.wikipedia.org/wiki/ファイル:OED-LEXX-Bungler.jpg "wikilink")。\]\] 1980年代、[軍艦](https://ja.wikipedia.org/wiki/軍艦 "wikilink")や軍用機などの際限のない高度化は、マニュアルの際限のない膨張という結果をもたらした。改良が加えられた時などにもマニュアルを書き直す作業が発生して業務の負担となっていた。このことから、マニュアルを電子化して容易に書き換えられるようにし、印刷用紙を大幅に削減することで、メンテナンスの簡素化をはかるための技術が必要とされた。

ただし、軍艦や軍用機などは数十年という長期間の保有が必要になるため、長期間にわたりデータが利用可能とならなければならない。[電子文書](https://ja.wikipedia.org/wiki/電子文書 "wikilink")は特定の企業の[ワープロソフト](https://ja.wikipedia.org/wiki/ワープロソフト "wikilink")を用いるとそのソフトのバージョンが上がったり、最悪の場合そのソフトを開発している会社が開発を中止したり、倒産したりしてソフトウェアが無くなった場合は、今まで作成したデータが読めなくなるという問題が発生してしまう。そこで、[プレーンテキスト](https://ja.wikipedia.org/wiki/プレーンテキスト "wikilink")のみを用いて、「タグ」を使うことによってデータに意味を持たせることが考えられた。なお実際には、データ形式の仕様が明確で、かつ自由に公開されていれば、そのエディタがプロプライエタリだろうがバイナリだろうが全く何も問題はない。\[2\]

ただし以上は正確にはSGML（の原形にあたるもの）が軍関係に「採用」された経緯である。

## 歴史

[1979年](../Page/1979年.md "wikilink")、[IBM](../Page/IBM.md "wikilink")で[プロジェクトマネージャ](https://ja.wikipedia.org/wiki/プロジェクトマネージャ "wikilink")をしていた は、Edward MosherおよびRaymond Lorieらとともに、「[GML](https://ja.wikipedia.org/wiki/Generalized_Markup_Language "wikilink")」(Generalized Markup Language) を発表し、それは「DCF」(Document Composition Facility) の名で商業化された。この成功でゴールドファーブは有名になり、IBMを退職してGMLの後継言語であるSGMLを開発することになったのである。

ISOのSGML規約は[1986年](https://ja.wikipedia.org/wiki/1986年 "wikilink")の出版後2ヶ月も経たないうちに[ベストセラー](https://ja.wikipedia.org/wiki/ベストセラー "wikilink")となった（その10年前に発売された[FORTRAN](../Page/FORTRAN.md "wikilink")のISO規約の部数を2ヶ月で超えた）。

SGMLは、[ISOから正式に承認される以前から](https://ja.wikipedia.org/wiki/国際標準化機構 "wikilink")、すでに、[アメリカ国防総省](https://ja.wikipedia.org/wiki/アメリカ国防総省 "wikilink")や[ECの公式出版事務局など](https://ja.wikipedia.org/wiki/欧州共同体 "wikilink")、数々の公的機関で使用され始めていた。ゴールドファーブの古巣のIBM社でも導入され、同社の文書システムに大変革をおこした。ヨーロッパでもCERN（[欧州原子核研究機構](https://ja.wikipedia.org/wiki/欧州原子核研究機構 "wikilink")）など、広く採用され、例えばフランスを例に挙げると、[エアバス](https://ja.wikipedia.org/wiki/エアバス "wikilink")社、[SNECMA](https://ja.wikipedia.org/wiki/SNECMA "wikilink")（フランス国営の航空機エンジンメーカー）およびフランス軍などで採用されることになった。

日本においては、[厚生省](https://ja.wikipedia.org/wiki/厚生省 "wikilink")への[新薬](https://ja.wikipedia.org/wiki/新薬 "wikilink")申請のデータ形式としてSGMLが採用された。それに伴い[製薬会社](https://ja.wikipedia.org/wiki/製薬会社 "wikilink")やその関連企業においても導入された。他にも[特許庁](https://ja.wikipedia.org/wiki/特許庁 "wikilink")などでも導入された。[航空機産業](https://ja.wikipedia.org/wiki/航空機産業 "wikilink")・[防衛産業](https://ja.wikipedia.org/wiki/防衛産業 "wikilink")、[自動車産業](https://ja.wikipedia.org/wiki/自動車産業 "wikilink")においても海外との[共同開発](https://ja.wikipedia.org/wiki/共同開発 "wikilink")や部品供給時の[情報交換](https://ja.wikipedia.org/wiki/情報交換 "wikilink")や[マニュアル](https://ja.wikipedia.org/wiki/マニュアル "wikilink")・[報告書](https://ja.wikipedia.org/wiki/報告書 "wikilink")の[電子化](https://ja.wikipedia.org/wiki/電子化 "wikilink")などに利用されることとなった。

## 特徴

  - SGMLは「**インスタンス**」、「**[DTD](https://ja.wikipedia.org/wiki/Document_Type_Definition "wikilink")**」、「**SGML宣言**」の3つで構成されている。
  - SGMLのデータ自体は[プレーンテキスト](https://ja.wikipedia.org/wiki/プレーンテキスト "wikilink")で作られている。
  - [レイアウト](https://ja.wikipedia.org/wiki/レイアウト "wikilink")情報は[スタイルシート](https://ja.wikipedia.org/wiki/スタイルシート "wikilink")を組み合わせて記述される。
  - [スタイルシート](https://ja.wikipedia.org/wiki/スタイルシート "wikilink")は「スタイルシート言語」で記述されている。
  - 通常、人が読む時は、上記[スタイルシート](https://ja.wikipedia.org/wiki/スタイルシート "wikilink")に沿って、レイアウトを整えられたうえで表示(出力)される。
  - SGMLで使うことができるスタイルシート言語として、[DSSSL](https://ja.wikipedia.org/wiki/Document_Style_Semantics_and_Specification_Language "wikilink") (Document Style Semantics and Specification Language) の規格が定められた。\[3\]

## 簡単な例

``` xml
<!DOCTYPE memo PUBLIC "-//SuzukiCorp//DTD Memo//JP">
<memo>
<from>木村
<to>富田様
<date>2001/10/01
<subject>役員会議
<para>役員会議の場所は会議室Ｂに変更になりました。
</memo>
```

## パーサ

SGML文書を、人間が読めるように、レイアウトして表示することは、**SGMLパーサ**という名のプログラムが行う。つまり[構文解析](https://ja.wikipedia.org/wiki/構文解析 "wikilink")およびレイアウトを行うプログラムである。SGMLパーサの最も初期の市販品としては、ブリュッセルの[SOBEMAP](https://ja.wikipedia.org/wiki/SOBEMAP "wikilink")社のものおよび、シカゴのDatalogics [データロジックス](https://ja.wikipedia.org/wiki/データロジックス "wikilink")社\[4\]のものがあった。\[5\]

## 問題

SGMLは機能が満載されていたことにより、そのままでは全てを実装することは困難であった。また、タグの構造が原因で、パーサのアルゴリズムが比較的複雑になることも難点だった。そこで後に、SGMLを簡略化および改良した形の[XMLが開発され](../Page/Extensible_Markup_Language.md "wikilink")、普及してゆくことになった。SGML文書はXML文書へと順次、変換・移行されることになった。

## 貢献

  - 上記のごとく、SGMLをもとにして、[XMLが開発された](../Page/Extensible_Markup_Language.md "wikilink")。
  - SGMLを基にした応用技術の一つが、[HTML](https://ja.wikipedia.org/wiki/HyperText_Markup_Language "wikilink") である。[ウェブページ](https://ja.wikipedia.org/wiki/ウェブページ "wikilink")を記述する言語[HTMLなくしては現在の爆発的なインターネットの普及は考えられない](https://ja.wikipedia.org/wiki/HyperText_Markup_Language "wikilink")。

SGMLはこれら2つの[マークアップ言語](https://ja.wikipedia.org/wiki/マークアップ言語 "wikilink")の源流であり、現在のインターネット利用者は皆SGMLの恩恵に浴しているのである。

## 参考文献

  - 『SGML入門』Martin Bryan 著、山崎俊一、福島誠　訳、アスキー出版局、1991年 ISBN 4-7561-0069-4

## 脚注

### 注

<references group="注"/>

### 出典

<references/>

## 関連項目

  - [Document Type Definition](https://ja.wikipedia.org/wiki/Document_Type_Definition "wikilink") (DTD)
      - [文書型宣言](https://ja.wikipedia.org/wiki/文書型宣言 "wikilink")
  - [Document Style Semantics and Specification Language](https://ja.wikipedia.org/wiki/Document_Style_Semantics_and_Specification_Language "wikilink") (DSSSL)
  - [Extensible Markup Language](../Page/Extensible_Markup_Language.md "wikilink") (XML)
  - [HyperText Markup Language](https://ja.wikipedia.org/wiki/HyperText_Markup_Language "wikilink") (HTML)
  - [マークアップ言語](https://ja.wikipedia.org/wiki/マークアップ言語 "wikilink")
  - [SGML実体](https://ja.wikipedia.org/wiki/SGML実体 "wikilink")

## 外部リンク

  - [The SGML History Niche](http://www.sgmlsource.com/history/index.htm)
  - [SGML: In memory of William W. Tunnicliffe](http://xml.coverpages.org/tunnicliffe.html)
  - [JIS X 4151-1992 文書記述言語SGML](http://www1.u-netsurf.ne.jp/~7l1rll/SGMLindex.html)

[Category:マークアップ言語](https://ja.wikipedia.org/wiki/Category:マークアップ言語 "wikilink") [Category:データモデリング](https://ja.wikipedia.org/wiki/Category:データモデリング "wikilink") [Category:JIS](https://ja.wikipedia.org/wiki/Category:JIS "wikilink") [Category:ISO標準](https://ja.wikipedia.org/wiki/Category:ISO標準 "wikilink")

1.  [Comparison of SGML and XML (NOTE-sgml-xml-971215)](https://www.w3.org/TR/NOTE-sgml-xml-971215/)
2.  しばしばXMLの優越性としてプレーンテキストであることなどが主張されているが、例えばバイナリエディタが存在しない世界である等という仮定があればそのような優越性も正しいものと思われる。
3.  HTMLでのスタイルの記述は [CSS](../Page/Cascading_Style_Sheets.md "wikilink") (Cascading Style Sheets) による。
4.  <http://www.datalogics.com/>
5.  注：SGMLパーサは、SGML文書の文法が規則に適合しているか検証する機能も持っており、そうした機能のためにだけ使われることもある。出典 <http://www.asahi-net.or.jp/~sd5a-ucd/rec-html401j/sgml/intro.html#h-19.1>
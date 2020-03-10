> この記事は[AGROVOC](https://ja.wikipedia.org/wiki/AGROVOC)から翻訳されています。


**AGROVOC** は農林水産、食糧安全保障、およびそれらの関連分野を網羅した多言語に対応した構造的[シソーラス](../Page/シソーラス.md "wikilink")のことである。これは多言語の単語や語句（用語）が、等価、階層、連想などの関係で整理されており、情報の特定や検索に用いられている。主な役割は検索の簡便化、効率化するために[索引](../Page/索引.md "wikilink")生成過程を標準化して、利用者に最適な情報を提供することである。

FAO（[国際連合食糧農業機関](https://ja.wikipedia.org/wiki/国際連合食糧農業機関 "wikilink")）とCEC（[欧州共同体委員会](https://ja.wikipedia.org/wiki/欧州共同体委員会 "wikilink")）は1980年代初頭にAGROVOCを共同で開発した。FAOはAGROVOCを約3ヶ月ごとに更新しており、利用者は[ウェブサイト](http://www.fao.org/aims/ag_intro.htm)で更新状況を見ることができる。
AGROVOCはFAOの公式言語である英語、フランス語、スペイン語、中国語、アラビア語の5言語に加えて、チェコ語、ドイツ語、日本語、ポルトガル語、スロバキア語、タイ語で利用できる。ヒンディー語、ハンガリー語、イタリア語、韓国語、ペルシャ語などの他の言語も現在翻訳、あるいは改訂中である。

## AGROVOCの構造

AGROVOCは、ひとつの特定の概念を表す単語あるいは複合語からなる用語から構成される。各用語は、階層的〔BT（広義語）、NT（狭義語）〕、非階層的関係〔RT（関連語）、UF（非見出し語）〕を示す他の用語と共に、1つの単語ブロックとして表される。

` 汚染`
`  NT：酸性沈殿物`
`  NT：大気汚染`
`  NT：非点源`
`  NT：堆積物汚染`
`  NT：水質汚染`
`  RT：環境破壊`
`  RT：汚染物質`
`  RT：農薬`

` 大気汚染`
`  BT：汚染`
`  RT：大気`
`  RT：温室効果`

AGROVOCシソーラスの情報の範囲や構造は用語間の関係性からわかる。例えば、大気汚染の広義語が汚染であることや関連語が大気や温室効果であることがわかると、これらの用語で表される情報の範囲が定義される。スコープノートは必要に応じて用語の意味や、文脈を明らかにするために使われる。[分類用語や地理用語](http://www.fao.org/aims/ag_subvoc.htm)は簡単に検索、フィルタリング、ダウンロードできるようにタグ付けされている。

## フォーマットの様式

AGROVOC は商業目的でなければ、無料で[ダウンロード](http://www.fao.org/aims/ag_download.htm)でき、[MySQL](https://ja.wikipedia.org/wiki/MySQL "wikilink")、[Microsoft Access](https://ja.wikipedia.org/wiki/Microsoft_Access "wikilink")、TagText、ISO2709、[XML](../Page/Extensible_Markup_Language.md "wikilink")、SKOS、[OWL](https://ja.wikipedia.org/wiki/OWL "wikilink")の各フォーマット様式で利用できる。

## AGROVOCのWEBサービス

農業情報管理システムの開発者は、最近公開したAGROVOCのWEBサービスによって、ローカルコピーではなく、WEBサービスを介して手持ちのアプリケーションにAGROVOCを組み込むことができる。WEBサービスを使うことで、更新したシソーラスをすぐに利用でき、シソーラスの最新バージョンの定期的ダウンロードやアプリケーションへの組み込みにかかる時間と手間を省くことができる。

現在、AGROVOCの用語にアクセスする7つのWEBサービスがオンライン上で利用できる。なお、AGROVOCの用語にはすべてタームコードが付いている。

  - [用語入力によるタームコード検索](http://www.fao.org/aims/agrovoc_ws/sample_ag_ws_proxy/testclient.jsp?method=27&input=1);
  - [タームコードと言語名入力による用語検索](http://www.fao.org/aims/agrovoc_ws/sample_ag_ws_proxy/testclient.jsp?method=20&input=1);
  - [タームコード入力によるすべての言語での用語検索](http://www.fao.org/aims/agrovoc_ws/sample_ag_ws_proxy/testclient.jsp?method=32&input=1);
  - [入力した用語を含むすべての用語検索](http://www.fao.org/aims/agrovoc_ws/sample_ag_ws_proxy/testclient.jsp?method=37&input=1).
  - [用語入力によるタームコード、すべての言語での用語、同義語・広義語・狭義語・関連語のタームコード検索](http://www.fao.org/aims/agrovoc_ws/sample_ag_ws_proxy/testclient.jsp?method=42&input=1)
  - [用語入力による定義、ヒストリーノート、スコープノート、コメント検索](http://www.fao.org/aims/agrovoc_ws/sample_ag_ws_proxy/testclient.jsp?method=13&input=1)
  - [用語、言語名入力による同義語検索のための問い合わせ文の検索（検索アプリケーションの用途）](http://www.fao.org/aims/agrovoc_ws/sample_ag_ws_proxy/testclient.jsp?method=50&input=1)

AGROVOCのWEBサービスは既存のSOAP、WSDLなどのオープンソースの標準規格によっている。

## シソーラスからオントロジーへ

AGROVOCは農業オントロジーサービス（AOS）プロジェクトの開発を支える根幹である。AOSでは、AGROVOCのような語彙体系やシソーラスの知識を利用して、WEB環境での情報管理を支援し専門領域特有の用語や概念の開発ができる。主な目的は概念間の関係性を拡張したり、明確にすることで、シソーラスにさらに意味を持たせることにある。

例えば、先に例に出した“汚染”は 、AGROVOCでは“汚染物質”と 関連語（RT）の関係にある。実際のところは、用語の関係を説明する際、「“汚染物質”によって“汚染”がおこる」と明確に表現できるであろう。これは、関連語（RT）で用語の関係性を表現するよりもわかりやすい。

`汚染`
` 原因：汚染物質`

“汚染”という用語について情報が欲しい利用者には、特定の関係性に検索を絞るオプション、例えば “汚染の原因をすべて示しますか” が示される。より関連性の高い情報検索に対する期待は急速に増大している。

[関係性の拡張](http://www.fao.org/aims/cs_relationships.htm)は、より詳細で矛盾のない索引を作成し、効果的な検索・閲覧機能を利用者に提供するために使うことができる。AOSはこの第一歩である。

## 外部リンク

  - [AGROVOC](http://aims.fao.org/website/AGROVOC-Thesaurus/sub)

[Category:農学](https://ja.wikipedia.org/wiki/Category:農学 "wikilink") [Category:シソーラス](https://ja.wikipedia.org/wiki/Category:シソーラス "wikilink") [Category:知識表現](https://ja.wikipedia.org/wiki/Category:知識表現 "wikilink") [Category:オントロジー](https://ja.wikipedia.org/wiki/Category:オントロジー "wikilink") [Category:科学のデータベース](https://ja.wikipedia.org/wiki/Category:科学のデータベース "wikilink") [Category:国際連合食糧農業機関](https://ja.wikipedia.org/wiki/Category:国際連合食糧農業機関 "wikilink")
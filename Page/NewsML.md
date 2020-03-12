> この記事は[NewsML](https://ja.wikipedia.org/wiki/NewsML)から翻訳されています。


**NewsML**（ニューズエムエル）あるいは'''ニュース用マーク付け言語 '''は、[ニュース](../Page/ニュース.md "wikilink")記事などを[ネットワーク上で配信するために](../Page/コンピュータネットワーク.md "wikilink")[XMLを拡張した](../Page/Extensible_Markup_Language.md "wikilink")[マークアップ言語](../Page/マークアップ言語.md "wikilink")である。

## 概要

NewsMLはニュースを配信する標準フォーマットであり、XMLのフォーマットを採る。

IPTCが標準化と管理を行っている。

通常はNewsMLとしては、[メタデータ](../Page/メタデータ.md "wikilink")と記述し、記事内容の項目にテキストあるいは[XHTML](https://ja.wikipedia.org/wiki/XHTML "wikilink")を埋め込んで使用されることが多い。

類似するフォーマットに[RSS](../Page/RSS.md "wikilink")があるが、RSSは[プル技術](https://ja.wikipedia.org/wiki/プル技術 "wikilink")、NewsMLは[プッシュ技術](https://ja.wikipedia.org/wiki/プッシュ技術 "wikilink")であり、使用方法が大きく異なる。このフォーマットは新聞社などの内部で使用されるため、一般の人が目にしたり使用したりする機会は殆どない。

最近では、ポータルサイトへの記事配信などだけではなく、[記者](../Page/記者.md "wikilink")からの記事の[入稿](https://ja.wikipedia.org/wiki/入稿 "wikilink")や出版社への配信など幅広く使っていこうとする動きがある。

## 日本での普及

日本では[日本新聞協会](../Page/日本新聞協会.md "wikilink")が中心となって動いたので、大手[新聞社](https://ja.wikipedia.org/wiki/新聞社 "wikilink")はすべて採用しており、[通信社](../Page/通信社.md "wikilink")などとのデータの交換などに使用される。また、大手[ポータルサイト](../Page/ポータルサイト.md "wikilink")とのニュース記事の配信にも使用されている。

日本の国家規格である[JIS規格](https://ja.wikipedia.org/wiki/JIS規格 "wikilink")で JIS X 7201 として制定されている。

## 仕様

### 共通枠

XMLであることを示す要素として次のヘッダを持つ。また、全体をNewsMLタグで囲む。

<?xml version="1.0"?>

`<!DOCTYPE NewsML PUBLIC "`<urn:newsml:iptc.org>`: 20031012:NewsMLv1.2.dtd:1" "`<http://www.iptc.org/NewsML/DTD/NewsMLv1.2.dtd>`">`
<NewsML>
`…`
</NewsML>

### 記事

NewsMLは1ファイル内に複数の記事を持つことが可能であり、1記事をNewsItemとして管理する。NewsItemデータはProviderId（配信元のID）、DateId（日付）、NewsItemId（1記事ごとにユニークになる値）で一意になるようにする。また、RevisionId（記事のバージョンを示す数値）を持ち、特定の記事を更新する機能も持つ。

記事内容は、DataContent内に記述する。DataContent内にXHTMLなどを埋めこむ場合にはXHTMLのタグから記入する。

### 画像などを配信する場合

画像などを配信する場合は、ContentItem属性に対象の画像などのファイル名を記載し、NewsMLとセットで配信する。記事はなく画像だけのみ配信したい場合でも同様にNewsMLファイルとセットにする必要がある。

## 一般的な用法

一般には次の手順で行われる。

1.  送信側の環境で記事を含んだNewsMLファイルを作成する。
2.  作成されたNewsMLファイルは[FTP等で配信先の環境に転送する](../Page/File_Transfer_Protocol.md "wikilink")。
3.  配信先では転送されたNewsMLファイルを解読する。

NewsMLファイルは新規記事の配信、記事の更新、記事の削除、記事表示期間の設定などができる。この機能によって、配信側が記事の作成、更新、削除などがコントロールできるようになる。

  - 新しい記事の配信方法
    新しいNewsItemIdを持った記事を含んだNewsMLファイルを作成し配信する。
  - 既存の記事の更新方法
    更新したいNewsItemIdを入れ、RevisionIdを[インクリメント](../Page/インクリメント.md "wikilink")した値にして配信する。
  - 既存の記事の削除方法
    削除したいNewsItemIdを入れ、StatusをCanceledにして配信することで削除される。

## SportsML

類似する規格に[SportsML](https://ja.wikipedia.org/wiki/SportsML "wikilink")というスポーツに特化した記事配信のフォーマットがあるが、現在使用しているケースはほとんどない。

## 外部リンク

  - [IPTC/NewsML Web](http://www.newsml.org/)
  - [NSK NewsML（NewsMLの日本語版の仕様書などがダウンロードできる）](http://www.pressnet.or.jp/newsml/newsml.htm)

[Category:JIS](https://ja.wikipedia.org/wiki/Category:JIS "wikilink") [Category:マークアップ言語](https://ja.wikipedia.org/wiki/Category:マークアップ言語 "wikilink") [Category:新聞](https://ja.wikipedia.org/wiki/Category:新聞 "wikilink") [Category:XMLベースの技術](https://ja.wikipedia.org/wiki/Category:XMLベースの技術 "wikilink")
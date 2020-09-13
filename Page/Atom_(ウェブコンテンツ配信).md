> この記事は[Atom \(ウェブコンテンツ配信\)](https://ja.wikipedia.org/wiki/Atom_\(ウェブコンテンツ配信\))から翻訳されています。


**Atom**（アトム）は、[ウェブ上の各種コンテンツを配信するための](../Page/World_Wide_Web.md "wikilink")[XML](../Page/Extensible_Markup_Language.md "wikilink")[文書フォーマットおよびコンテンツの編集を行うための](../Page/ファイルフォーマット.md "wikilink")[通信プロトコル](../Page/通信プロトコル.md "wikilink")などいくつかの仕様群の総称である。

## 概要

  - [Atom配信フォーマット（*Atom Syndication Format*）](https://ja.wikipedia.org/wiki/#Atom_Syndication_Format "wikilink")
  - [Atom出版プロトコル（*Atom Publishing Protocol*）](https://ja.wikipedia.org/wiki/#Atom_Publishing_Protocol "wikilink")

主な仕様は上記の2つ。1つはコンテンツを配信するための[フィード](../Page/フィード.md "wikilink")のフォーマットを規定する｢Atom配信フォーマット｣ (Atom Syndication Format)、もう1つはウェブ上のコンテンツを編集するための｢Atom出版プロトコル｣ (Atom Publishing Protocol) で、通称*Atom API*または*AtomPP*とも呼ばれることがある。

元々、[The Atom Project](http://www.intertwingly.net/wiki/pie/FrontPage/)として、有志が[ウィキ](../Page/ウィキ.md "wikilink")やメーリングリストで議論しながら草の根的に始まり、現在、活動の場所は[IETF (Internet Engineering Task Force)](../Page/Internet_Engineering_Task_Force.md "wikilink") に引き継がれてワーキンググループとして標準化活動が行われている。

Atomワーキンググループが掲げるモットーは以下の4つである。

  - 特定のベンダに依存しない
  - すべての人が自由に実装できる
  - 誰でも自由に拡張可能である
  - 仕様を明確に且つ詳細に定義する

## Atom Syndication Format

ウェブサイトの更新情報等のメタデータやコンテンツの配信 (Syndication)、保存 (Archive) を受け持つXML文書の仕様。ブログやニュースをRSS・Atomアグリゲータ（RSSリーダーとも呼ばれる）アプリケーションで購読する際に用いるのが、この形式で記述されたファイルとなる。ほとんどのRSS・Atomアグリゲータは、RSSの各バージョンとAtomをサポートする。単にAtomといった場合、このフォーマットを指していることが多い。

### 用途

[ブログ](../Page/ブログ.md "wikilink")やニュースサイトの更新情報の配信のみにとどまらず、MP3や動画などのリッチメディアの配信にも用いることが出来る。拡張性が高いため、メタデータの流通方法として汎用的に利用することが可能となっている。

### 現状

IETFにおいてRFC 4287として仕様が公開され、広く利用されている。

### サンプル

``` xml
<?xml version="1.0" encoding="utf-8"?>
<feed ns="http://www.w3.org/2005/Atom">

 <title>Example Feed</title>
 <link href="http://example.org/"/>
 <updated>2003-12-13T18:30:02Z</updated>
 <author>
   <name>John Doe</name>
 </author>
 <id>urn:uuid:60a76c80-d399-11d9-b93C-0003939e0af6</id>

 <entry>
   <title>Atom-Powered Robots Run Amok</title>
   <link href="http://example.org/2003/12/13/atom03"/>
   <id>urn:uuid:1225c695-cfb8-4ebb-aaaa-80da344efa6a</id>
   <updated>2003-12-13T18:30:02Z</updated>
   <summary>Some text.</summary>
 </entry>

</feed>
```

## Atom Publishing Protocol

ブログや[ウィキ](../Page/ウィキ.md "wikilink")などのウェブ上のコンテンツ（[リソース](https://ja.wikipedia.org/wiki/リソース_\(WWW\) "wikilink")）を編集するためのアプリケーションレベルの通信プロトコル。これにより、Atom出版プロトコルに対応したアプリケーションに対し、デスクトップ上のソフトウェアやデータベース、携帯などのモバイル機器との直接の連携が可能になる。略称はもともと*AtomPP*であったが、その後に*AtomPub*と呼ばれるようになった。

Atom出版プロトコルは[HTTPベースの通信プロトコルで](../Page/Hypertext_Transfer_Protocol.md "wikilink")、[RESTのアーキテクチャスタイルに準拠している](../Page/Representational_State_Transfer.md "wikilink")。また、通信でやり取りされるフォーマットは｢Atom配信フォーマット｣ベースのXML文書となっている。

### 用途

デスクトップやモバイルとウェブとを繋ぐ掛け橋として、様々な用途に用いることが出来る。すでにデスクトップやモバイルのアプリケーションからブログへ投稿したり編集するためのアプリケーションが多数存在する。

### 現状

IETFに移管される以前はAtom APIと呼ばれていたが、「Atom出版プロトコル」 (Atom Publishing Protocol) という正式名称に変更された。現在、RFC 5023として仕様が公開されている。

また、Atom APIと呼ばれていた頃の[ドラフト仕様 0.9](http://www.atomenabled.org/developers/api/atom-api-spec.php)を用いて、ブログ関連のアプリケーションでは実際に広く利用されている。

## 事例

### Atom APIサーバ実装

  - [Blogger](http://www.blogger.com/)
      - [「Blogger AtomAPI Documentation」](http://code.blogspot.com/archives/atom-docs.html)（英語）
  - [livedoor ブログ](http://blog.livedoor.com/)
  - [Six Apart](../Page/シックス・アパート.md "wikilink")
      - [「TypePad Atom API」](http://sixapart.com/developers/atom/typepad/)（英語）
  - はてなブックマーク・はてなフォトライフ
      - [はてなブックマークAtomAPI](https://d.hatena.ne.jp:443/keyword/%E3%81%AF%E3%81%A6%E3%81%AA%E3%83%96%E3%83%83%E3%82%AF%E3%83%9E%E3%83%BC%E3%82%AFAtomAPI)
      - [はてなフォトライフAtomAPI](https://d.hatena.ne.jp:443/keyword/%E3%81%AF%E3%81%A6%E3%81%AA%E3%83%95%E3%82%A9%E3%83%88%E3%83%A9%E3%82%A4%E3%83%95AtomAPI)
  - Blogmarks.net AtomAPI（英語）
  - So-net blog AtomAPI仕様

### Atom APIクライアント実装

  - [BlogWrite](http://www.witha.jp/BlogWrite/)
  - [ecto](http://ecto.kung-foo.tv/)

## 関連項目

  - [フィード](../Page/フィード.md "wikilink")
  - [RSS](../Page/RSS.md "wikilink")
  - [Representational State Transfer](../Page/Representational_State_Transfer.md "wikilink") (REST)
  - [Resource Description Framework](../Page/Resource_Description_Framework.md "wikilink")
  - [ブログ](../Page/ブログ.md "wikilink")

## 外部リンク

  - [The Atom Project](http://www.intertwingly.net/wiki/pie/FrontPage/)
  - [IETF Atomワーキンググループ](http://www.ietf.org/wg/concluded/atompub)
  - RFC 4287
      - [RFC4287 日本語訳](http://www.futomi.com/lecture/japanese/rfc4287.html)
  - RFC 5023
      - [RFC5023 日本語訳](http://www.ricoh.co.jp/src/rd/webtech/rfc5023_ja.html)
  - [解説Atom](http://www.witha.jp/Atom/)
  - [RSS 2.0とAtom 1.0の比較](http://www.witha.jp/Atom/RSS-and-Atom.html)
  - [Atom出版プロトコルを知る、第1回：Atom出版プロトコルを使ってWebリソースを作成し、編集する](http://www-06.ibm.com/jp/developerworks/xml/library/x-atompp1/)

[Category:RSS](https://ja.wikipedia.org/wiki/Category:RSS "wikilink") [Category:RFC](https://ja.wikipedia.org/wiki/Category:RFC "wikilink") [Category:XMLベースの技術](https://ja.wikipedia.org/wiki/Category:XMLベースの技術 "wikilink") [Category:オープンフォーマット](https://ja.wikipedia.org/wiki/Category:オープンフォーマット "wikilink")
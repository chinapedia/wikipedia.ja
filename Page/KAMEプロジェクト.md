> この記事は[KAME](https://ja.wikipedia.org/wiki/KAME)から翻訳されています。


**KAMEプロジェクト**（かめぷろじぇくと）は、[IIJ](https://ja.wikipedia.org/wiki/IIJ "wikilink")、[NEC](../Page/日本電気.md "wikilink")、[東芝](https://ja.wikipedia.org/wiki/東芝 "wikilink")、[日立](../Page/日立製作所.md "wikilink")、[富士通](../Page/富士通.md "wikilink")、[横河電機](https://ja.wikipedia.org/wiki/横河電機 "wikilink")(五十音順)各社による共同研究プロジェクト。[BSD](../Page/BSD.md "wikilink")系OS([FreeBSD](../Page/FreeBSD.md "wikilink"), [OpenBSD](../Page/OpenBSD.md "wikilink"), [NetBSD](../Page/NetBSD.md "wikilink"))上に[IPv6](https://ja.wikipedia.org/wiki/IPv6 "wikilink")を中心としたインターネット技術の標準コードを実装することを目的として、[1998年](https://ja.wikipedia.org/wiki/1998年 "wikilink")に始まった。

KAMEの実装は[BSDライセンス](https://ja.wikipedia.org/wiki/BSDライセンス "wikilink")下で[フリーソフトウェア](../Page/フリーソフトウェア.md "wikilink")として公開され、現在までに各BSD UNIXのIPv6スタックとして採用されており、さらにルータベンダなどにも採用されている。

KAMEプロジェクトは、[USAGIプロジェクト](https://ja.wikipedia.org/wiki/USAGIプロジェクト "wikilink")や[TAHIプロジェクト](https://ja.wikipedia.org/wiki/TAHIプロジェクト "wikilink")同様に[WIDEプロジェクト](https://ja.wikipedia.org/wiki/WIDEプロジェクト "wikilink")傘下のプロジェクトで、特にこれらのプロジェクトとは密接に関係して活動している。

「KAME」という名前は、かつてはKAMEプロジェクトの本拠地のあった[藤沢市](../Page/藤沢市.md "wikilink")刈込(かりごめ)の略と言われた頃もあったが、実際は、KAMEプロジェクトが始まる直前に行われた合宿で、開発エンジニアの一人[itojunが](https://ja.wikipedia.org/wiki/萩野純一郎 "wikilink")、どうしてもとれない[バグ](https://ja.wikipedia.org/wiki/バグ "wikilink")に悩まされていたときに、そばにあった[亀の](../Page/カメ.md "wikilink")[ぬいぐるみ](https://ja.wikipedia.org/wiki/ぬいぐるみ "wikilink")に「かめさん助けて」といって抱きついて、その後無事にバグがとれたことに由来している。現在でも、KAMEのオフィスには様々な大きさの亀のぬいぐるみやおもちゃが飾られているし、かつては「KAMEプロジェクト」のタグをつけたぬいぐるみを販売していたこともある。(現在は在庫がつきたため販売は中止)

KAMEプロジェクトのWebサイトのトップページには亀の画像があり、IPv6でアクセスすると、手足を動かすアニメーションをするようになっている。 このページは、IPv6で通信可能かどうかを判別する手段として広く知られており、「亀が踊る (the dancing kame)」と呼ばれる。

一期2年として、四期8年にわたって活動を続けてきたが、IPv6の基本規格の実装はほぼ安定したということで、2005年11月、「KAMEプロジェクト完成宣言」が行われ、2006年3月をもって活動を終了することが発表された。

公式な活動終了後も、CVSリポジトリやwebページは維持され、毎週月曜日にそのときのソースをarchiveしたsnapshotと呼ばれるtarballも公開され続けている。

## 成果

KAMEプロジェクトの主な成果は以下の通り

  - BSD標準IPv6スタック : FreeBSD, NetBSD, OpenBSDおよびそれらの派生OSでのIPv6スタック
    BSD標準IPsecスタック : FreeBSD, NetBSDでのIPsecスタック。OpenBSDは独自のIPsecを持っているほか、他のBSDでも暗号ハードウェアを生かすために別のIPsec(Fast IPsecと呼ばれる)に置き換える動きがある。
    鍵交換デーモン racoon : IKEv1を行うための鍵交換デーモン。後にUSAGI, IPsec-toolsなどを通じて、linuxでも使われるようになった。
    MobileIPv6, NEMO実装SHISA : Mobile IPv6, NEMO(Network mobility) basic protocolをサポートする。

## 関連項目

  - [IPv6](https://ja.wikipedia.org/wiki/IPv6 "wikilink")
  - [IPsec](https://ja.wikipedia.org/wiki/IPsec "wikilink") - [racoon](https://ja.wikipedia.org/wiki/racoon "wikilink")
  - [萩野純一郎](https://ja.wikipedia.org/wiki/萩野純一郎 "wikilink") - Itojun

## 外部リンク

  - [Web page of Kame project](http://www.kame.net/)

[Category:UNIXに関連する組織](https://ja.wikipedia.org/wiki/Category:UNIXに関連する組織 "wikilink") [Category:インターネット技術](https://ja.wikipedia.org/wiki/Category:インターネット技術 "wikilink") [Category:BSD](https://ja.wikipedia.org/wiki/Category:BSD "wikilink") [Category:研究プロジェクト](https://ja.wikipedia.org/wiki/Category:研究プロジェクト "wikilink") [Category:IPv6](https://ja.wikipedia.org/wiki/Category:IPv6 "wikilink")
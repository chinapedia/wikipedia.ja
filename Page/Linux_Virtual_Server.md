> この記事は[Linux Virtual Server](https://ja.wikipedia.org/wiki/Linux_Virtual_Server)から翻訳されています。


[right](https://ja.wikipedia.org/wiki/ファイル:Lvslogo.png "wikilink") **Linux Virtual Server** (**LVS**) は、[Linux](../Page/Linux.md "wikilink")システムの[負荷分散](https://ja.wikipedia.org/wiki/負荷分散 "wikilink")ソリューションの一種である。[1998年](https://ja.wikipedia.org/wiki/1998年 "wikilink")5月、Wensong Zhang により[オープンソース](../Page/オープンソース.md "wikilink")プロジェクトとして開始された。プロジェクトの目的は、[コンピュータ・クラスター](../Page/コンピュータ・クラスター.md "wikilink")技術を使って高性能かつ高可用なLinuxサーバを構築し、スケーラビリティ、信頼性、保守性を向上させることである。

LVSプロジェクトの目下の焦点は新たな IP[ロードバランス](https://ja.wikipedia.org/wiki/ロードバランス "wikilink")ソフトウェア (IPVS) の開発と、アプリケーションレベルのロードバランスソフトウェア (KTCPVS) の開発、クラスター管理機能の開発である。

  - [IPVS](http://www.linuxvirtualserver.org/software/ipvs.html): Linux カーネル内に実装された IPロードバランスソフトウェア。IPVS のコードは既に標準の Linuxカーネル 2.4 と 2.6 に導入されている。
  - [KTCPVS](http://www.linuxvirtualserver.org/software/ktcpvs/ktcpvs.html): Linux カーネル内にアプリケーションレベルのロードバランス機能を組み込む計画。現在、開発中。

LVS を利用するとスケーラビリティや信頼性の高いネットワークサービス（Webサービス、電子メールサービス、マルチメディアおよび[VoIP](../Page/VoIP.md "wikilink")サービスなど）が構築でき、それらを大規模高信頼の[電子商取引](../Page/電子商取引.md "wikilink")アプリケーションや[電子政府](../Page/電子政府.md "wikilink")アプリケーションに統合できる。

LVS は既に世界中で実際に使われている。

## 外部リンク

  - [The Linux Virtual Server project](http://www.LinuxVirtualServer.org/)
  - [Linux Virtual Server チュートリアル（日本語）](http://ultramonkey.sourceforge.jp/papers/lvs_tutorial/html/)

[Category:ネットワークソフト](https://ja.wikipedia.org/wiki/Category:ネットワークソフト "wikilink") [Category:並列コンピューティング](https://ja.wikipedia.org/wiki/Category:並列コンピューティング "wikilink") [Category:分散処理](https://ja.wikipedia.org/wiki/Category:分散処理 "wikilink")
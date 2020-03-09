> この記事は[Network News Transfer Protocol](https://ja.wikipedia.org/wiki/Network_News_Transfer_Protocol)から翻訳されています。


**Network News Transfer Protocol**（ネットワーク ニュース トランスファー プロトコル、**NNTP**）は、[インターネット](https://ja.wikipedia.org/wiki/インターネット "wikilink")アプリケーション[プロトコル](../Page/プロトコル.md "wikilink")のひとつである。おもに、[ネットニュース](https://ja.wikipedia.org/wiki/ネットニュース "wikilink") (Usenet) の記事を読むことと記事を投稿することのために使われる。記事は[ニュースサーバ間を相互に配送される](https://ja.wikipedia.org/wiki/:en:news_server "wikilink")。[カリフォルニア大学サンディエゴ校](https://ja.wikipedia.org/wiki/カリフォルニア大学サンディエゴ校 "wikilink")のBrian Kantorと[カリフォルニア大学バークレー校](https://ja.wikipedia.org/wiki/カリフォルニア大学バークレー校 "wikilink")の[Phil LapsleyがNetwork](https://ja.wikipedia.org/wiki/:en:Phil_Lapsley "wikilink") News Transfer Protocolの仕様であるRFC 977を[1986年](https://ja.wikipedia.org/wiki/1986年 "wikilink")の5月に完成させた。他の貢献者として、[Baylor College of MedicineのStan](https://ja.wikipedia.org/wiki/:en:Baylor_College_of_Medicine "wikilink") Barberと[アップルコンピュータのErik](https://ja.wikipedia.org/wiki/アップル_\(企業\) "wikilink") Fairがいる。

Usenetはもともとは[UUCP](https://ja.wikipedia.org/wiki/UUCP "wikilink")ネットワーク上での使用を前提として設計された。つまり、ほとんどの記事は電話回線で直接コンピュータ同士を接続して配送されていた。読者と投稿者は同じニュースサーバにログインし、そのサーバのディスクにある記事を直接読んでいた。

[LANとインターネットが一般に普及すると](../Page/Local_Area_Network.md "wikilink")、[パーソナルコンピュータ](../Page/パーソナルコンピュータ.md "wikilink")上で使用できるニュースリーダーと、インターネット上で記事を配送する手段が必要とされた。インターネットで互換性のあるファイルシステムがまだ広くは利用できなかったため、[SMTP](../Page/Simple_Mail_Transfer_Protocol.md "wikilink") に類似した新しいプロトコルを作ることになった。

[ウェルノウンTCPポート番号である](https://ja.wikipedia.org/wiki/TCPやUDPにおけるポート番号の一覧#ウェルノウンポート番号 "wikilink")119番はNNTPのために予約されている。クライアントが[SSLでニュースサーバに接続するときはTCPのポート](https://ja.wikipedia.org/wiki/Secure_Sockets_Layer "wikilink")563番が使われる\[1\]。これは**NNTPS**と呼ばれることがある。

最近では、Webで利用可能な[BBS](https://ja.wikipedia.org/wiki/BBS "wikilink")やその他[インターネットコミュニティ](../Page/インターネットコミュニティ.md "wikilink")サイトが普及したことと、NNTPが[ボットネット](https://ja.wikipedia.org/wiki/ボットネット "wikilink")の活動に利用されることが多くなったことが原因で、殆ど利用されなくなってきている。

## Network News Reader Protocol (NNRP)

1990年代のはじめにNNTP標準が策定されようとしていたとき、NNTPをクライアント側での使用に特化したもの (NNRP) が提案された。このプロトコルは決して完全には実装されていなかったが、[INNに付属する](https://ja.wikipedia.org/wiki/:en:InterNetNews "wikilink")**nnrpd**というプログラムでその名前が使われ続けている。結果として、クライアントにとって使いやすい標準的なNNTPコマンドのサブセットが、今も**NNRP**と呼ばれている。

##  サーバソフトウェア

  - [Leafnode](https://ja.wikipedia.org/wiki/Leafnode "wikilink")
  - [InterNetNews](https://ja.wikipedia.org/wiki/InterNetNews "wikilink")
  - [C News](https://ja.wikipedia.org/wiki/C_News "wikilink")
  - [Apache James](https://ja.wikipedia.org/wiki/Apache_James "wikilink")
  - [Synchronet](https://ja.wikipedia.org/wiki/Synchronet "wikilink")

## 脚注

## 関連項目

  - [ニュースグループ](https://ja.wikipedia.org/wiki/ニュースグループ "wikilink")
  - [ネットニュース](https://ja.wikipedia.org/wiki/ネットニュース "wikilink")
  - [電子掲示板](https://ja.wikipedia.org/wiki/電子掲示板 "wikilink")
  - [SCTP](https://ja.wikipedia.org/wiki/SCTP "wikilink")

## 外部リンク

  - Kantor, Brian and Phil Lapsley. RFC 977 "Network News Transfer Protocol: A Proposed Standard for the Stream-Based Transmission of News." [1986](https://ja.wikipedia.org/wiki/1986年 "wikilink").
  - Horton, Mark, and R. Adams. RFC 1036 "Standard for Interchange of USENET Messages." [1987](https://ja.wikipedia.org/wiki/1987年 "wikilink").
  - [NNTP Version 2 draft](http://www.academ.com/academ/nntp/ietf/1996-July/000022.html) an early, abandoned attempt to revise NNTP
  - Barber, Stan, et al. RFC 2980 "Common NNTP Extensions." [2000](../Page/2000年.md "wikilink")
  - [IETF nntpext Working Group](http://www.eyrie.org/~eagle/nntp/ietf.html)
  - RFC 3977 (October [2006](https://ja.wikipedia.org/wiki/2006年 "wikilink"))
  - RFC 4642 (October 2006)

## 翻訳元

*[:en:Network News Transfer Protocol](https://ja.wikipedia.org/wiki/:en:Network_News_Transfer_Protocol "wikilink") 2006-05-02 12:34 UTCより翻訳。著者 : Aldie, Nanshu, Christian, Fleminra ほか*

[Category:ネットニュース](https://ja.wikipedia.org/wiki/Category:ネットニュース "wikilink") [Category:アプリケーション層プロトコル](https://ja.wikipedia.org/wiki/Category:アプリケーション層プロトコル "wikilink") [Category:インターネット標準](https://ja.wikipedia.org/wiki/Category:インターネット標準 "wikilink") [Category:RFC](https://ja.wikipedia.org/wiki/Category:RFC "wikilink")

1.  **STARTTLS**拡張コマンドでTLS (SSL) へ移行する方法がRFC 4642で提案されている。
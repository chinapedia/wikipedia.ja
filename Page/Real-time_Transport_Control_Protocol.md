> この記事は[Real-time Transport Control Protocol](https://ja.wikipedia.org/wiki/Real-time_Transport_Control_Protocol)から翻訳されています。


**Real-time Transport Control Protocol**（**RTCP**）は[RTPと兄弟関係にあるプロトコルである](../Page/Real-time_Transport_Protocol.md "wikilink")。RTCPはRFC 3550で定義される（そのため古いバージョンのRFC 1889は廃止された）。

RTCPはRTPの[フロー制御](https://ja.wikipedia.org/wiki/フロー制御 "wikilink")をするときの制御情報を提供する。RTCPは、RTPと組み合わせることでマルチメディアデータを送受信できるが、RTCP自体はデータを転送することはできない。定期的に制御パケットを送ってストリーミング・マルチメディア・セッションに参加する。RTCPの一番重要な機能はRTPによって提供される[Quality of Serviceのフィードバックを提供することである](../Page/Quality_of_Service.md "wikilink")。

RTCPは、メディア接続時に、送信バイト数、送信パケット数、ロスパケット数、[ジッター](../Page/ジッター.md "wikilink")、フィードバック情報、[ラウンドトリップタイム](https://ja.wikipedia.org/wiki/ラウンドトリップタイム "wikilink")といった統計情報を集める。アプリケーションによってはこういった情報をサービス品質の向上、速度を制限した転送、異なるコーデックの使用といったことに使うかもしれない。

RTCPのパケットの種類にはいくつかあり、それは、送信者レポートパケット、受信者レポートパケット、送信元記述パケット、退去メッセージパケット、アプリケーション定義パケットなどである。

RTCPはそれ自体はどんな暗号化も認証手段も提供しない。[SRTCP](https://ja.wikipedia.org/wiki/Secure_Real-time_Transport_Protocol "wikilink") プロトコルがその目的を果たす可能性がある。

## RTCPの問題と今後の開発

The Real-time Transport Control Protocol (RTCP) は、（[IPTVのように](../Page/IP放送.md "wikilink")）RTCPのレポートが送られる間に非常に長い遅延が発生するという問題を大規模アプリケーションにおいていくつか抱えている。これは、受信者のレポートパケットとそれに対する送信者の評価が、そのセッションの本当の状態と比べて不正確であるからである。この問題を扱う方法がいくつかあり、それは、[RTCPフィルタリング](https://ja.wikipedia.org/wiki/RTCP_filtering "wikilink")、[RTCPバイアシング](https://ja.wikipedia.org/wiki/RTCP_biasing "wikilink")、[RTCP階層的集約法である](https://ja.wikipedia.org/wiki/RTCP_hierarchical_aggregation "wikilink")。

  - 詳細は次を参照 [Realtime control protocol and its improvements for Internet Protocol Television](http://adela.utko.feec.vutbr.cz/projects/publications/#3)

## 関連項目

  - [Real-time Transport Protocol](../Page/Real-time_Transport_Protocol.md "wikilink")
  - [ストリーミング](../Page/ストリーミング.md "wikilink")
  - [Quality of Service](../Page/Quality_of_Service.md "wikilink")

## 外部リンク

  - [Optimization of Large-Scale RTCP Feedback Reporting in Fixed and Mobile Networks](http://adela.utko.feec.vutbr.cz/projects/publications/#2)
  - [Realtime control protocol and its improvements for Internet Protocol Television](http://adela.utko.feec.vutbr.cz/projects/publications/#3)
  - [for RTP: A Transport Protocol for Real-Time Applications](http://tools.ietf.org/html/rfc3550)

[Category:アプリケーション層プロトコル](https://ja.wikipedia.org/wiki/Category:アプリケーション層プロトコル "wikilink") [Category:RFC](https://ja.wikipedia.org/wiki/Category:RFC "wikilink") [Category:長大な項目名](https://ja.wikipedia.org/wiki/Category:長大な項目名 "wikilink")
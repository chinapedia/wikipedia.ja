> この記事は[Coda](https://ja.wikipedia.org/wiki/Coda)から翻訳されています。


**Coda** は、[カーネギーメロン大学](https://ja.wikipedia.org/wiki/カーネギーメロン大学 "wikilink")の Mahadev Satyanarayanan らが1987年から続けている研究プロジェクトの一環として開発した[分散ファイルシステム](https://ja.wikipedia.org/wiki/分散ファイルシステム "wikilink")。[Andrew File System](https://ja.wikipedia.org/wiki/Andrew_File_System "wikilink") (AFS) の直接の後継であり、機能的にも多くの類似点がある。[Linux](https://ja.wikipedia.org/wiki/Linux "wikilink")、[NetBSD](../Page/NetBSD.md "wikilink")、[FreeBSD](../Page/FreeBSD.md "wikilink") で動作する。Coda に影響を受けたファイルシステムとして [InterMezzo](https://ja.wikipedia.org/wiki/InterMezzo "wikilink") がある。Coda は現在も開発が続けられており、研究というよりも商用の頑健な製品を作ることに中心が移っている。

## 機能

Coda にはネットワークファイルシステムにふさわしい機能が多くあり、その一部は独特のものである。

1.  モバイル・コンピューティングのための接続断操作
2.  比較的フリーなライセンス条件で利用可能
3.  クライアント側の永続性キャッシュによる高性能
4.  サーバ[レプリケーション](../Page/レプリケーション.md "wikilink")
5.  認証、暗号化、アクセス制御などのセキュリティモデル
6.  サーバネットワークの一部がダウンしても運用継続可能
7.  ネットワーク[帯域幅](../Page/帯域幅.md "wikilink")への順応
8.  高い[スケーラビリティ](https://ja.wikipedia.org/wiki/スケーラビリティ "wikilink")
9.  ネットワークに障害があってもうまく機能する共有の仕組み

Coda は、ネットワークのコネクションが失われたとき、サーバデータへのアクセス手段としてローカルキャッシュを使う。通常の運用では、ユーザーのファイルシステムでの読み書きによって、クライアントはサーバとデータをやり取りし、ユーザーが重要と指定したデータを接続断に備えてキャッシュしておく。ネットワーク接続が途切れたとき、Coda のクライアントはローカルキャッシュを使って運用を続け、その間の更新を記録しておく。ネットワークが再び接続されたとき、クライアントは更新記録をサーバに送り、同期処理を行う。その後、再び通常の運用に戻る。

AFSとは、データの[レプリケーション](../Page/レプリケーション.md "wikilink")方法が異なる。AFSは悲観的レプリケーション戦略を採用していて、読み書きが可能なサーバは1台だけで、他はリードオンリーの複製になっていた。Coda では、どのサーバも読み書き可能になっている。このためAFSよりも可用性が大幅に向上している。

このような機能があるため、同じファイルやディレクトリでありながら、個々のクライアントやサーバが独自に更新を行って、いわゆるコンフリクトが発生することがある。Coda ではコンフリクトに手動または自動で対処するための各種ツールを用意している。

## 外部リンク

  - [Coda 公式サイト](http://www.coda.cs.cmu.edu/) カーネギーメロン大学
  - [The Coda Distributed Filesystem for Linux](http://linuxplanet.com/linuxplanet/tutorials/4481/1/), Bill von Hagen, 2002年10月7日

[Category:OSのファイルシステム](https://ja.wikipedia.org/wiki/Category:OSのファイルシステム "wikilink") [Category:分散処理](https://ja.wikipedia.org/wiki/Category:分散処理 "wikilink")
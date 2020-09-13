> この記事は[Comet](https://ja.wikipedia.org/wiki/Comet)から翻訳されています。


**Comet**（コメット）とは、[Web アプリケーションを構築する際に利用される技術で](https://ja.wikipedia.org/wiki/ウェブアプリケーション "wikilink")、この技術を使うと、[サーバ](../Page/サーバ.md "wikilink")で発生した[イベントを](../Page/イベント_\(プログラミング\).md "wikilink")[クライアントからの要請なしに](../Page/クライアント_\(コンピュータ\).md "wikilink")[クライアントに送信することができる](../Page/クライアント_\(コンピュータ\).md "wikilink")。

Comet はこのような通信を実現するための複数の手法をまとめた概念である。これらの手法はブラウザにプラグインを追加することなく、（[JavaScript](../Page/JavaScript.md "wikilink") のような）デフォルトの機能で実現されるものである。理論的には Comet は、ブラウザがデータを要求する形の既存のウェブのモデルとは異なっている。実際は Comet アプリケーションは [Ajax](https://ja.wikipedia.org/wiki/Ajax "wikilink") と [Long polling](https://ja.wikipedia.org/wiki/Push技術#Long_polling "wikilink") を使用してサーバ上の新規データを取得する。

Cometは既存の技術を利用してサーバーからの通信を実現する技術であるが、既存の技術は本来はサーバーからの通信を想定したものではなく、そのため不都合も多かった。[2011年](../Page/2011年.md "wikilink")には初めから双方向通信を想定した技術である[WebSocket](https://ja.wikipedia.org/wiki/WebSocket "wikilink")が定義されている。

## なぜ必要なのか

従来の方法では、ウェブページはクライアントからリクエストがあったときのみクライアントに配信されていた。クライアントがリクエストするたび、ブラウザはサーバへの [HTTP](../Page/Hypertext_Transfer_Protocol.md "wikilink") コネクションを生成し、ウェブサーバはクライアントにデータを返し、そのコネクションは閉じられる。この方法の欠点は、ユーザが明示的にページのリフレッシュを行うか、またはユーザが新しいページに移動する場合にしか表示されるページが更新されないことである。ページをすべて転送するのには長い時間を要するので、ページのリフレッシュは多大な遅延を生みだす。

この問題を解決するために、ブラウザに変更があった部分だけをリクエスト・更新させる技術である [Ajax](https://ja.wikipedia.org/wiki/Ajax "wikilink") を用いることができる。この方法だとデータ通信量が従来の方法より少なくなるため、遅延の度合も少なくなり、サイト全体のパフォーマンスは向上するといえる。さらに言えば、非同期通信を用いることにより、ユーザは段階的にデータを受信しながら作業をすることが可能になるため、その意味でもパフォーマンスは向上する。

しかし Ajax を用いたとしても、クライアントがサーバからデータを取得する前にはそれに対するリクエストを出さなければならないという苦しい問題は依然存在する。この問題は、例えば「別のクライアントがデータを送ってきた」というようなサーバ上でのイベントが発生するのを待機する必要のあるアプリケーションを設計するときに大きな障害となる。

サーバ上でイベントが起こったかどうかを周期的に確認させる（いわゆるポールループさせる）ようにアプリケーションを設計するのはひとつの解決策である。しかしこの方法は、アプリケーションは結局サーバ上のイベントが完了したかどうかの問い合わせに多くの時間を使ってしまうため、あまりエレガントとはいえない。また、ネットワークの帯域も多く消費されてしまう。

## 実現手法

一般的に、Web サーバはクライアントからのリクエストを受け取るとすぐにレスポンスを返す。

Comet を利用した Web アプリケーションでは、サーバはクライアントからのリクエストに対してすぐに応答せず、保留状態にしておき、サーバ上でなんらかのイベント（チャットで誰かが発言したなど）が発生したときにレスポンスを返す。こうすることによって、サーバで発生したイベントを即座にクライアントに送信することができる。

## 関連項目

  - [Ajax](https://ja.wikipedia.org/wiki/Ajax "wikilink")
  - [WebSocket](https://ja.wikipedia.org/wiki/WebSocket "wikilink")
  - [メッセージ指向ミドルウェア](../Page/メッセージ指向ミドルウェア.md "wikilink")

## 外部リンク

  - [Lingr and Comet - 技術解説編](http://japan.cnet.com/blog/kenn/2006/09/22/entry_lingr_and_comet/) 江島健太郎
  - [Comet の正しい使い方](http://labs.cybozu.co.jp/blog/kazuho/archives/2007/02/keeping_comet_alive.php)

[Category:ソフトウェアアーキテクチャ](https://ja.wikipedia.org/wiki/Category:ソフトウェアアーキテクチャ "wikilink") [Category:ウェブ技術](https://ja.wikipedia.org/wiki/Category:ウェブ技術 "wikilink") [Category:ウェブ開発](https://ja.wikipedia.org/wiki/Category:ウェブ開発 "wikilink")
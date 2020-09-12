> この記事は[H2O \(Webサーバ\)](https://ja.wikipedia.org/wiki/H2O_\(Webサーバ\))から翻訳されています。


**H2O**は、[フリーかつオープンソースの](../Page/FLOSS.md "wikilink")[Webサーバ](../Page/Webサーバ.md "wikilink")[ソフトウェア](../Page/ソフトウェア.md "wikilink")である。

[C言語](../Page/C言語.md "wikilink")で書かれており、[MITライセンス](https://ja.wikipedia.org/wiki/MITライセンス "wikilink")の条件に基づいて配布されている。

## 概要

[HTTP/2](https://ja.wikipedia.org/wiki/HTTP/2 "wikilink")と[TLSを前提として設計が行われており](../Page/Transport_Layer_Security.md "wikilink")、優先度制御やサーバプッシュなどのHTTP/2の技術を最大限に活用することで、[nginx](https://ja.wikipedia.org/wiki/nginx "wikilink")などの従来のWebサーバソフトウェアと比較して大幅に優れた処理速度を実現している\[1\]。

## 特徴

H2Oの主な特徴は下記の通りである\[2\]:

  - [HTTP/1.0](https://ja.wikipedia.org/wiki/HTTP/1.0 "wikilink")及び[HTTP/1.1](https://ja.wikipedia.org/wiki/HTTP/1.1 "wikilink")のサポート

  - [HTTP/2](https://ja.wikipedia.org/wiki/HTTP/2 "wikilink")のサポート

      - サーバ側での微調整付きの依存関係と重み付けに基づいた優先度制御の完全なサポート
      - [ウェブブラウザ](../Page/ウェブブラウザ.md "wikilink")の[キャッシュを利用したサーバプッシュ](../Page/キャッシュ_\(コンピュータシステム\).md "wikilink")

  - [HTTP/3](https://ja.wikipedia.org/wiki/HTTP/3 "wikilink")のサポート (実験的)

  -
  - [TLSのサポート](../Page/Transport_Layer_Security.md "wikilink")

      - セッション再開 ([スタンドアローン](../Page/スタンドアローン.md "wikilink")及び[memcached](https://ja.wikipedia.org/wiki/memcached "wikilink"))

      - 自動的な鍵のロールオーバーを利用したセッションチケット

      - 自動的な[OCSP](https://ja.wikipedia.org/wiki/OCSP "wikilink")ステープリング

      - [前方秘匿性](https://ja.wikipedia.org/wiki/前方秘匿性 "wikilink")及び高速な[認証付き暗号](https://ja.wikipedia.org/wiki/認証付き暗号 "wikilink")である暗号スイート

      - を利用した秘密鍵の保護

  - 静的ファイルの提供

  - [FastCGI](../Page/FastCGI.md "wikilink")のサポート

  - [リバースプロキシ](../Page/リバースプロキシ.md "wikilink")

  - [mruby](https://ja.wikipedia.org/wiki/mruby "wikilink")による拡張 (Rackベース)

  - 緩やかな再起動と自己アップグレード

## 歴史

H2Oはに[DeNA](https://ja.wikipedia.org/wiki/DeNA "wikilink")社内の[モバイルゲーム](https://ja.wikipedia.org/wiki/モバイルゲーム "wikilink")用サーバとして[奥一穂](https://ja.wikipedia.org/wiki/奥一穂 "wikilink")を中心に開発が開始された\[3\]。 に最初のバージョン (0.9.0) がリリースされ、HTTP/2の仕様が正式に承認されたに最初の安定版がリリースされた\[4\]。

## 脚注

## 関連項目

  - \- H2Oの世界最大の利用者であり、奥一穂がから所属している。

## 外部リンク

  -
  -
[Category:Webサーバ](https://ja.wikipedia.org/wiki/Category:Webサーバ "wikilink") [Category:ディー・エヌ・エー](https://ja.wikipedia.org/wiki/Category:ディー・エヌ・エー "wikilink") [Category:2015年のソフトウェア](https://ja.wikipedia.org/wiki/Category:2015年のソフトウェア "wikilink") [Category:オープンソースソフトウェア](https://ja.wikipedia.org/wiki/Category:オープンソースソフトウェア "wikilink")

1.
2.
3.
4.
> この記事は[PersistentPerl](https://ja.wikipedia.org/wiki/PersistentPerl)から翻訳されています。


**PersistentPerl**とは、[Perl](../Page/Perl.md "wikilink")を高速化する手法の一つである。主に[Perl](../Page/Perl.md "wikilink")で書かれた[CGIを高速化するために使われているが](../Page/Common_Gateway_Interface.md "wikilink")[CGI以外の](../Page/Common_Gateway_Interface.md "wikilink")[シェル](../Page/シェル.md "wikilink")等からでも利用できる。

## 概要

Perlスクリプトは、ユーザーからリクエストがある度に

  - Perlプロセスの生成
  - Perlスクリプトの文法解釈
  - スクリプトのコンパイル
  - コンパイルされたバイトコードの実行
  - プロセスの破棄

が行われる。大量のリクエストがあればその分だけ繰りかえされ、この事がパフォーマンスの悪化に繋がっている。

PersistentPerlはPerlスクリプトの実行を

  - リクエストの受付
  - （リクエストを受けられるバックエンドプロセスがいなければ）バックエンドプロセスの生成
  - UNIXドメインソケットを使ったバックエンドプロセスとのデータ受け渡し

を行う[フロントエンド](../Page/フロントエンド.md "wikilink")プロセスと（つまりフロントエンドプロセスはPerlに関わらない）

  - 初回のみPerlスクリプトをコンパイルし、バイトコードを保持したままプロセスとして残る
  - フロントエンドからのリクエストに従ってコンパイル済みバイトコードを実行

を行うバックエンドプロセスの2つに分けることで2回目以降のスクリプトの文法解釈とコンパイルにかかる時間をカットし結果としてプログラム起動速度の向上およびサーバ負荷の低下が可能となる。

## 利用方法

CGIとして実行するならばスクリプト冒頭の

`#!/usr/bin/perl`

などと書かれている部分を

`#!/usr/bin/perperl`

とするだけで既存のコードはほぼそのまま高速化に寄与できる。

[Apacheならmod](../Page/Apache_HTTP_Server.md "wikilink")_persistentperlというモジュールがあり、リクエストの度に行われるフロントエンドプロセスの生成に伴うコストを無くすことが可能である。 ただしmod_persistentperlはworker MPMには非対応である。

## 関連項目

  - [CGI](../Page/Common_Gateway_Interface.md "wikilink")
  - [Perl](../Page/Perl.md "wikilink")

## 外部リンク

  - [PersistentPerl - Speed up perl scripts by running them persistently.](http://www.daemoninc.com/PersistentPerl/)
  - [SourceForge.net: PersistentPerl](http://persistentperl.sourceforge.net/)
  - [Apache2.2にmod_SpeedyCGIを組み込むためのパッチの当て方](http://www.maido3.com/server/support/apache2speedy.html)

[Category:Webサーバ](https://ja.wikipedia.org/wiki/Category:Webサーバ "wikilink") [Category:Perl](https://ja.wikipedia.org/wiki/Category:Perl "wikilink")
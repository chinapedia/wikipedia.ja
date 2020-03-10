> この記事は[Ludia](https://ja.wikipedia.org/wiki/Ludia)から翻訳されています。


**Ludia**（るでぃあ）は、[PostgreSQL](https://ja.wikipedia.org/wiki/PostgreSQL "wikilink")に[全文検索](../Page/全文検索.md "wikilink")機能を追加する拡張モジュールで[オープンソース](../Page/オープンソース.md "wikilink")ソフトウェアである。

Ludiaは[Senna](../Page/Senna.md "wikilink")を利用することにより、全文検索[インデックス](https://ja.wikipedia.org/wiki/インデックス "wikilink")を作成する。この全文検索インデックスは、PostgreSQLの通常のインデックスと同様にSQLクエリの際に利用可能であり、高速で高精度（[Senna](../Page/Senna.md "wikilink")と同様）な全文検索が可能となる。株式会社[NTTデータ](../Page/NTTデータ.md "wikilink")により開発され、2006年10月11日に[LGPL](https://ja.wikipedia.org/wiki/LGPL "wikilink")ライセンスのオープンソースソフトウェアとしてバージョン0.8.0が公開された。

[Linux](../Page/Linux.md "wikilink")・[FreeBSD](../Page/FreeBSD.md "wikilink")などの[UNIX](../Page/UNIX.md "wikilink")系OS、[Windowsで動作する](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")。PostgreSQL 8.1以降で利用可能。

PostgreSQL 8.3以降に組み込まれた全文検索エンジンをベースとした日本語検索（[textsearch_ja](http://textsearch-ja.projects.postgresql.org/index-ja.html)）が[形態素解析](../Page/形態素解析.md "wikilink")による検索のみをサポートするのに対し、Ludiaは形態素解析以外にSennaによる[N-gram検索にも対応するのが特徴である](https://ja.wikipedia.org/wiki/全文検索#N-Gram "wikilink")。ただしPostgreSQL 8.4以降では、同じくN-gram検索に対応した[textsearch_senna](http://textsearch-ja.projects.postgresql.org/textsearch_senna.html)が登場している。

2007年12月にバージョン1.5.0をリリースして以降、バグ修正以外の実質的なバージョンアップが停止した状態にあり、PostgreSQL 8.3以降の環境では後述するような運用上の制限を受けることから、最近はtextsearch_jaもしくはtextsearch_sennaを必要に応じて使い分けるケースが増えてきている。

## 制限

  - リカバリに未対応。クラッシュ後はREINDEXが必要。
  - 2009年2月現在、PostgreSQL 8.3以降のVACUUMには非対応。そのため8.3以降とLudiaを組み合わせて運用する場合は、autovacuumをoffにした上で、VACUUM後には必ずREINDEXを行う必要がある。
  - PostgreSQL 8.3で全文検索エンジンが組み込まれた関係で、PostgreSQL 8.2以前で利用する場合 (@@) と8.3以降の場合 (%%) ではデフォルトの演算子が変更されている。

## 外部リンク

  - [株式会社NTTデータ Ludia](http://www.nttdata.co.jp/services/ludia/index.html)
  - [Ludia プロジェクト ホームページ](http://ludia.sourceforge.jp/moin.cgi/)
  - [SourceForge.jp: Project Info - Ludia -](http://sourceforge.jp/projects/ludia/)

[Category:PostgreSQL](https://ja.wikipedia.org/wiki/Category:PostgreSQL "wikilink") [Category:オープンソースソフトウェア](https://ja.wikipedia.org/wiki/Category:オープンソースソフトウェア "wikilink") [Category:全文検索](https://ja.wikipedia.org/wiki/Category:全文検索 "wikilink")
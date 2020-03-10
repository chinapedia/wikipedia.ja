> この記事は[Apache Portable Runtime](https://ja.wikipedia.org/wiki/Apache_Portable_Runtime)から翻訳されています。


**Apache Portable Runtime**（アパッチ・ポータブル・ランタイム、APR）は、 [Apache HTTP Server](../Page/Apache_HTTP_Server.md "wikilink") のサポートライブラリである。 OSとソフトウェアの間でOSなどの環境の違いを吸収するAPIを提供する。そして、他のOSに一般的にある機能が存在しないOSでは、APRが代替を提供する。よって、APRを使うことにより真のクロスプラットフォームなプログラムを作ることが出来る。

APRはもともとは Apache HTTP Server の一部だったが、現在では[Apacheソフトウェア財団](https://ja.wikipedia.org/wiki/Apacheソフトウェア財団 "wikilink")の中の独立したプロジェクトとなっていて、Apache HTTP Server 以外のアプリケーションからもクロスプラットフォームのために使われている。

APRに含まれるプラットフォーム非依存の機能：

  - [動的メモリアロケーション](https://ja.wikipedia.org/wiki/動的メモリアロケーション "wikilink")と[メモリプール](https://ja.wikipedia.org/wiki/メモリプール "wikilink")
  - 分割不能操作(アトミックオペレーション)
  - [ライブラリ](../Page/ライブラリ.md "wikilink")の動的読み込み
  - ファイル[入出力](../Page/入出力.md "wikilink")
  - コマンド引数の構文解析
  - [ロック](https://ja.wikipedia.org/wiki/ロック_\(情報工学\) "wikilink")
  - [ハッシュテーブル](../Page/ハッシュテーブル.md "wikilink")と[配列](../Page/配列.md "wikilink")
  - [mmap](https://ja.wikipedia.org/wiki/mmap "wikilink")
  - [ソケットとプロトコル](https://ja.wikipedia.org/wiki/ソケット_\(BSD\) "wikilink")
  - [スレッド](../Page/スレッド_\(コンピュータ\).md "wikilink")、[プロセス](../Page/プロセス.md "wikilink")、[ミューテックス](https://ja.wikipedia.org/wiki/ミューテックス "wikilink")
  - [共有メモリ](../Page/共有メモリ.md "wikilink")
  - 時間関係
  - ユーザーIDとグループID関係

## 関連項目

  - [Apacheソフトウェア財団](https://ja.wikipedia.org/wiki/Apacheソフトウェア財団 "wikilink")
  - [Apache HTTP Server](../Page/Apache_HTTP_Server.md "wikilink")

## 外部リンク

  - [Apache Portable Runtime Project (公式サイト)](http://apr.apache.org/)

[Category:オープンソースソフトウェア](https://ja.wikipedia.org/wiki/Category:オープンソースソフトウェア "wikilink") [Category:Apacheソフトウェア財団](https://ja.wikipedia.org/wiki/Category:Apacheソフトウェア財団 "wikilink")
> この記事は[KeepSync](https://ja.wikipedia.org/wiki/KeepSync)から翻訳されています。


'''KeepSync '''（キープシンク）は、[株式会社クエスト・ワン](http://www.quest-one.jp/)が開発・販売する異なる種類、異なる拠点間にあるデータベースの同期をするアプリケーションである。

同期元データベースのネットワークセグメントに配置されたKeepSync Clientが同期元と同期先のデータベースの差分を検出しKeepSync Serverに送信する。

KeepSync Serverは受信した差分データを同期先データベースに反映する。 この一連の動作を繰り返すことにより、データベースの同期状態の維持を可能とする。

## 特徴

  - [Oracleや](../Page/Oracle_Database.md "wikilink")[Microsoft SQL Server](https://ja.wikipedia.org/wiki/Microsoft_SQL_Server "wikilink")、[DB2](https://ja.wikipedia.org/wiki/DB2 "wikilink")などの異なる種類のデータベースのデータ同期が可能
  - 異なるネットワークセグメントに配置されているデータベースのデータ同期が可能
  - 差分データのみを検出・送信するため、ネットワークトラフィックへの影響が少ない
  - 差分データ送信時に何らかの障害が発生し同期が完了しない場合も、次回のデータ同期時に前回の同期できなかったデータが差分データと検出されるため、特別なリカバリー処理することなくデータ同期が可能

## 適用事例

  - ディザスタ対策
  - データバックアップ
  - データベース移行
  - 連結決算システムにおけるデータ集信インフラ
  - 企業間、システム間におけるデータ連携インフラ

## 実行環境

### KeepSync Client

  - [Windows 2000 Server/Professional](../Page/Microsoft_Windows_2000.md "wikilink")、[Windows XP Professional](../Page/Microsoft_Windows_XP.md "wikilink")、[Windows Server 2003](../Page/Microsoft_Windows_Server_2003.md "wikilink")
  - [.NET Framework](https://ja.wikipedia.org/wiki/.NET_Framework "wikilink") 2.0
  - KeepSync Client を導入するパソコンから同期元データベースサーバーに対してアクセスが可能であること
  - KeepSync Server に対して80番または443番[ポートの](../Page/ポート_\(コンピュータネットワーク\).md "wikilink")[アウトバウンド](https://ja.wikipedia.org/wiki/アウトバウンド "wikilink")接続が可能であること

### KeepSync Server

  - Windows 2000 Server/Professional、Windows XP Professional、Windows Server 2003
  - .NET Framework 2.0
  - [IIS](../Page/Internet_Information_Services.md "wikilink")4.0以降
  - KeepSync Server を導入するパソコンから同期先データベースサーバーに対してアクセスが可能であること
  - KeepSync Client からの80番または443番ポートの[インバウンド](../Page/インバウンド.md "wikilink")接続が可能であること

[Category:アプリケーションソフト_(製品)](https://ja.wikipedia.org/wiki/Category:アプリケーションソフト_\(製品\) "wikilink")
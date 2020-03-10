> この記事は[ \(Oracle Database\)](https://ja.wikipedia.org/wiki/_\(Oracle_Database\))から翻訳されています。


**バックグラウンドプロセス**とは、[データベース](../Page/データベース.md "wikilink")である[Oracle Databaseのシステムを管理する](../Page/Oracle_Database.md "wikilink")[プロセス](../Page/プロセス.md "wikilink")である。バックグラウンドで動作する。[ファイルと](https://ja.wikipedia.org/wiki/ファイル_\(Oracle_Database\) "wikilink")[システムグローバル領域](https://ja.wikipedia.org/wiki/システムグローバル領域 "wikilink")の仲介役となる。[インスタンス](../Page/インスタンス.md "wikilink")の実行中に[メモリーを管理したり](../Page/記憶装置.md "wikilink")、[データ](../Page/データ.md "wikilink")を[ハードディスク](https://ja.wikipedia.org/wiki/ハードディスク "wikilink")に書き込んだりする。

## 7つの主要なバックグラウンドプロセス

主要なバックグラウンドプロセスは以下の７つがある。

  - SMON (システムモニタプロセス)
  - PMON (プロセスモニタプロセス)
  - DBWR (データベースライタプロセス)
  - LGWR (ログライタプロセス)
  - CKPT (チェックポイントプロセス)
  - ARCH (アーカイバプロセス)
  - MMON (マネージャモニタプロセス)

　利用のオプションやバージョンによってはこれ以外のプロセスも存在する。

## SMON

Oracle Databaseのシステムを監視する。[インスタンス](../Page/インスタンス.md "wikilink")に障害が発生した後にOracle Databaseをオープンすると、インスタンス回復を行う。

## PMON

障害が発生したプロセスを回復させる。そのプロセスが利用していた[リソースを開放する](https://ja.wikipedia.org/wiki/計算資源 "wikilink")。

## DBWR

メモリの「データベースバッファキャッシュ\[1\]」上のデータをディスクの「データファイル\[2\]」に書き込む。データベースバッファキャッシュは[システムグローバル領域](https://ja.wikipedia.org/wiki/システムグローバル領域 "wikilink")の一部である。

Oracle Databaseでは、メモリ上でデータの処理を完了させてからディスクのファイルに書き込む。書き込むデータの順番はLRU([Least Recently Used](../Page/Least_Recently_Used.md "wikilink"))という[アルゴリズム](../Page/アルゴリズム.md "wikilink")で決定する。

DBWRを起動する数は、「DB_WRITER_PROCESSES」という初期化[パラメータで指定する](../Page/引数.md "wikilink")。DBWRは10つまで起動できる。ほとんどのシステムでは1つ起動すれば十分である。ただし、データを頻繁に変更するなら多く起動するとよい。

### DBWRが書き込みをするシステムの状態

  - バッファ・キャッシュの使用量が設定されたしきい値を超えた。(LOG_CHECKPOINT_TIMEOUT)
  - 設定された時間、DBWRが書き込みをしていない。(LOG_CHECKPOINT_INTERVAL)
  - チェックポイントが発生した。
  - あるプロセスが必要なだけの空き[バッファ](https://ja.wikipedia.org/wiki/バッファ "wikilink")を確保できない。

## LGWR

メモリの「REDOログバッファ\[3\]」にあるデータの変更履歴をディスクの「REDOログファイル\[4\]」に書き込む。REDOログバッファもシステムグローバル領域の一部である。

### LGWRが書き込みをするシステムの状態

  - REDOログバッファの空きが3分の1しかない。
  - 3秒間、LGWRが書き込みをしていない。(タイムアウト)
  - DBWRが書き込みを行うとき。
  - 利用者によるデータの変更が確定された。([コミット](https://ja.wikipedia.org/wiki/コミット "wikilink"))

## CKPT

データファイルと「制御ファイル\[5\]」(システム制御用のファイル)を更新するための「チェックポイント」を発生させる。 チェックポイントが発生したときにDBWRへ信号を送る。DBWRはデータベースバッファキャッシュでの処理をデータファイルに反映させる。管理者はデータベースを停止するときなど、いろいろなタイミングで発生させることができる。

### チェックポイントの処理の流れ

1.  LGWRが書き込みを行う。
2.  DBWRが書き込みを行う。
3.  メモリの内容を制御ファイルに反映させる。
4.  チェックポイントが正常に完了したことを全てのデータファイルと制御ファイルに反映させる。

### チェックポイントが発生する条件

  - REDOログを切り替えるとき。(この切り替えを「ログスイッチ」という)。(9iよりはオンラインREDOログ・ファイルのサイズのうちの90％書き込んだ時)
  - normal(正常終了)かtransaction(トランザクション終了後),immediate(即時停止),でデータベースを停止したとき。ただし、abort(強制終了)では発生しない。
  - 「LOG_CHECKPOINT_INTERVAL」と「LOG_CHECKPOINT_TIMEOUT」という初期化パラメータで設定したしきい値を超えた。
  - 管理者が手動で発生させたとき。(ALTER SYSTEM CHECKPOINT)

## ARCH

REDOログファイルを「アーカイブREDOログファイル\[6\]」([アーカイブ](../Page/アーカイブ.md "wikilink")のファイル)にコピーする。REDOログファイルがいっぱいになるか、ログスイッチが発生したときに、書き込みをする。

ARCHを起動する数は、「LOG_ARCHIVE_MAX_PROCESSES」という初期化パラメータに指定する。ARCHが不足しているとLGWRがARCHを自動で起動する。10つまで動作させることができる。

## 脚注

<references />

## 関連項目

  - [Oracle Database](../Page/Oracle_Database.md "wikilink")

[Category:オラクル](https://ja.wikipedia.org/wiki/Category:オラクル "wikilink")

1.  [システムグローバル領域](https://ja.wikipedia.org/wiki/システムグローバル領域 "wikilink")を参照。
2.  [ファイル (Oracle Database)を参照](https://ja.wikipedia.org/wiki/ファイル_\(Oracle_Database\) "wikilink")。
3.
4.
5.
6.
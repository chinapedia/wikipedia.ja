> この記事は[Symfoware Server](https://ja.wikipedia.org/wiki/Symfoware_Server)から翻訳されています。


**Symfoware Server**（シンフォウェア サーバ）は[富士通](../Page/富士通.md "wikilink")が開発・販売する[リレーショナルデータベース管理システム](../Page/関係データベース管理システム.md "wikilink") (RDBMS)のことである。[Solaris](../Page/Solaris.md "wikilink")、[Linux](../Page/Linux.md "wikilink")([Red Hat Enterprise Linux](https://ja.wikipedia.org/wiki/Red_Hat_Enterprise_Linux "wikilink"))および[Windows上で動作する](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")。[メインフレーム](../Page/メインフレーム.md "wikilink")前身の[RDBII](https://ja.wikipedia.org/wiki/RDBII "wikilink")（アールデービーツー）が[オープン系](https://ja.wikipedia.org/wiki/オープン系 "wikilink")システムに対応した際に Symfoware に改称された。 1995年10月に初期版が発表された。

## 概要

ホスト ([FACOM M](../Page/FACOM.md "wikilink")/GS/PRIMEFORCEシリーズ) 上のRDB (RDBII/SymfowareGS) との親和性（文字コードなど）・移植性が高い。

際立った特徴としてRDBMS製品で初めて実装された表パーティショニング (DSO(Data Structure Organization), DSI(Data Structure Instance)) がある。これは実表およびインデックスを、キーにより複数の格納単位に[分割する機能である](https://ja.wikipedia.org/wiki/分割_\(データベース\) "wikilink")。物理的に格納単位を分割するため、ディスク出入力の負荷の軽減、大規模データ検索の高速化、排他の局所化、障害時のリスク軽減などが期待できる。たとえ分割を行わない場合でも、DSO/DSIはテーブル作成後に明示的に定義する必要がある。

変わった機能として、データファイルのバッファをDSI単位で個別設定する機能、DSIのデータを丸ごとメモリ常駐させる機能がある。

デフォルトの[トランザクション分離レベル](https://ja.wikipedia.org/wiki/トランザクション分離レベル "wikilink")が一般的なRead CommittedではなくRepeatable Readであり、SELECT文の実行でもロックを獲得するため、安易にSELECTをかけて広範囲にロックをかけてしまうことがある。環境設定ファイル、アプリケーションの設計などで、ロックの強弱の設定や、レコード単位のロックの導入などのチューニングが必要である。

[ACID特性は](../Page/ACID_\(コンピュータ科学\).md "wikilink")、表・インデックスへの排他およびテンポラリログを利用して実装している。

RDBMSエンジン本体は1プロセス(rdb2base)である。1セッションごとにプロセスが起動するのではなく、セッションごとに対応するスレッドをRDBMSエンジン本体内で生成する。

RDBMS管理作業は、RDBMSエンジンが稼動しているサーバ上で`rdb`をプリフィックスとしたコマンドを実行するか、GUIによる操作を行う。

HA[クラスタ](../Page/コンピュータ・クラスター.md "wikilink")、パラレル構成によるHPCクラスタ構成が構築可能である。

[JDBC](../Page/JDBC.md "wikilink")ドライバ、Windows用の[ODBCドライバ](../Page/Open_Database_Connectivity.md "wikilink")、[.NET Framework連携機能が提供されている](https://ja.wikipedia.org/wiki/.NET_Framework "wikilink")。

大規模高信頼性向け (Symfoware Server Enterprise Extended Edition) から小規模部門サーバむけ (Symfoware Server Standard Edition) まで企業内用途に合わせた構成・価格帯の製品選択が可能である。

V3.x、V4時代、徐々に処理速度が落ちてしまったりバックアップから復旧できない、簡単な計算を間違える等の致命的不具合が発見されたことがある。

対応OSとして、Windows,Solaris,Linuxと限られており、AIX、HP-UX版は出荷されていない。

## 製品群

  - Symfoware Server Enterprise Extended Edition
      - 大規模基幹システム向け
      - 対応プラットホーム: Linux([RHEL](https://ja.wikipedia.org/wiki/Red_Hat_Enterprise_Linux "wikilink")),Solaris
  - Symfoware Server Enterprise Edition
      - 中大規模システム向け
      - 対応プラットホーム: Linux,Solaris,Windows
  - Symfoware Server Standard Edition
      - 中規模システム向け
      - 対応プラットホーム: Linux,Solaris,Windows
  - Symfoware Server Lite Edition
      - 小規模システム向け
      - 対応プラットホーム: Windows

## 関連項目

  - [PRIMERGY 6000](../Page/PRIMERGY_6000.md "wikilink") (Symfoware6000)

## 外部リンク

  - [製品サイト](http://software.fujitsu.com/jp/symfoware/products/symfowareserver/)

[Category:富士通の製品](https://ja.wikipedia.org/wiki/Category:富士通の製品 "wikilink") [Category:データベース管理システム](https://ja.wikipedia.org/wiki/Category:データベース管理システム "wikilink")
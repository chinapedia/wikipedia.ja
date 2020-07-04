> この記事は[World Wide Name](https://ja.wikipedia.org/wiki/World_Wide_Name)から翻訳されています。


**World Wide Name**（**WWN**）または **World Wide Identifier**（**WWID**）とは、[ファイバーチャネル](../Page/ファイバーチャネル.md "wikilink")または [Serial Attached SCSI](../Page/Serial_Attached_SCSI.md "wikilink") による[ストレージエリアネットワーク](../Page/ストレージエリアネットワーク.md "wikilink")における一意の[識別子](../Page/識別子.md "wikilink")である。

各WWNは8[バイトの数であり](../Page/バイト_\(情報\).md "wikilink")、[IEEE](../Page/IEEE.md "wikilink") [OUI](https://ja.wikipedia.org/wiki/Organizationally_Unique_Identifier "wikilink")（先頭3バイト）と[ベンダー](https://ja.wikipedia.org/wiki/ベンダー "wikilink")が提供する[情報](https://ja.wikipedia.org/wiki/情報 "wikilink")（残り5バイト）で構成される。

## 形式

IEEE の定義する WWN の形式は2種類ある。

  - 本来の形式: IEEE標準化委員会が製造業者にアドレスを割り当て、[イーサネット](../Page/イーサネット.md "wikilink")の[MACアドレス](../Page/MACアドレス.md "wikilink")のようにデバイス製造時に組み込む。先頭2バイトは[16進数](https://ja.wikipedia.org/wiki/16進数 "wikilink")で 10:00 または 2x:xx（x はベンダー指定）、次の3バイトがベンダー識別子、残る3バイトがベンダーの指定する[シリアル番号](../Page/シリアル番号.md "wikilink")となっている。
  - 新しいアドレシング方式: 先頭4ビットが16進数で 5 または 6 で、次に3バイトのベンダー識別子が続き、残る4バイトと4ビットがベンダー指定のシリアル番号となる。

## WWN企業識別子（一部）

  - 00:50:76 [IBM](../Page/IBM.md "wikilink")
  - 00:a0:98 [ネットアップ](../Page/ネットアップ.md "wikilink")
  - 00:60:69 [ブロケード コミュニケーションズ システムズ](https://ja.wikipedia.org/wiki/ブロケード_コミュニケーションズ_システムズ "wikilink")
  - 00:05:1E ブロケード コミュニケーションズ システムズ、以前は Rhapsody Networks
  - 00:60:DF ブロケード コミュニケーションズ システムズ、以前は CNT Technologies Corporation
  - 00:E0:8B [QLogic](https://ja.wikipedia.org/wiki/QLogic "wikilink") [HBA用の元々の識別子](https://ja.wikipedia.org/wiki/ホストバスアダプタ "wikilink")
  - 00:1B:32 QLogic HBA用。2007年から使用開始
  - 00:C0:DD QLogic FCスイッチ用
  - 00:90:66 QLogic、以前は Troika Networks
  - 00:11:75 QLogic、以前は PathScale, Inc
  - 08:00:88 ブロケード コミュニケーションズ システムズ、以前は McDATA Corporation。WWIDとしては 1000.080 から始まる。
  - 00:60:B0 [ヒューレット・パッカード](../Page/ヒューレット・パッカード.md "wikilink") - Integrity および HP9000 サーバ用。WWID としては 5006.0b0 から始まる。
  - 00:11:0A ヒューレット・パッカード - ProLiant サーバ用。以前は[コンパック](../Page/コンパック.md "wikilink")。WWID としては 5001.10a から始まる。
  - 00:01:FE ヒューレット・パッカード - EVA ディスクアレイ用。以前は[DEC](../Page/ディジタル・イクイップメント・コーポレーション.md "wikilink")。WWID としては 5000.1fe1 から始まる。
  - 00:17:A4 ヒューレット・パッカード - MSL [テープライブラリ](https://ja.wikipedia.org/wiki/テープライブラリ "wikilink")用。以前は Global Data Services。WWID としては 200x.0017.a4 から始まる。
  - 00:60:48 [EMC](https://ja.wikipedia.org/wiki/EMCコーポレーション "wikilink") - Symmetrix 用。
  - 00:60:16 EMC - CLARiiON 用。

## 関連項目

  - [ファイバーチャネル](../Page/ファイバーチャネル.md "wikilink")
  - [Serial Attached SCSI](../Page/Serial_Attached_SCSI.md "wikilink")

## 外部リンク

  - [Guidelines for Fibre Channel Use of the Organizationally Unique Identifier (OUI)](http://standards.ieee.org/regauth/oui/tutorials/fibreformat.html)
  - [IEEE OUI list](http://standards.ieee.org/regauth/oui/oui.txt)

[Category:識別子](https://ja.wikipedia.org/wiki/Category:識別子 "wikilink") [Category:補助記憶装置](https://ja.wikipedia.org/wiki/Category:補助記憶装置 "wikilink") [Category:コンピュータネットワーク](https://ja.wikipedia.org/wiki/Category:コンピュータネットワーク "wikilink")
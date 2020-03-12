> この記事は[Micro Embbeded System](https://ja.wikipedia.org/wiki/Micro_Embbeded_System)から翻訳されています。


**MES**(Micro Embbeded System)とは、[マイコン用の](../Page/マイクロコントローラ.md "wikilink")[組み込みオペレーティングシステム](../Page/組み込みオペレーティングシステム.md "wikilink") (OS) である。みついわゆきおによって開発された。当初は[H8/OS](https://ja.wikipedia.org/wiki/H8/OS "wikilink")の後継[OSとして](../Page/オペレーティングシステム.md "wikilink")[H8](../Page/H8.md "wikilink")シリーズの[マイコンをターゲットとして開発されたが](../Page/マイクロコントローラ.md "wikilink")、後に[SuperH](../Page/SuperH.md "wikilink")シリーズに対応するようになった。現在は[SuperH](../Page/SuperH.md "wikilink")を主なターゲットとして開発されている。

## 特徴

  - [gccによるプログラム開発](../Page/GNUコンパイラコレクション.md "wikilink")。
  - プリエンプティブ・[マルチタスク](../Page/マルチタスク.md "wikilink")により複数のプログラムを実行可能。
  - [デバイスドライバ](../Page/デバイスドライバ.md "wikilink")によるハードウェアの[抽象化](../Page/抽象化_\(計算機科学\).md "wikilink")。
  - マイコンの内蔵[ROM上のROMディスク](https://ja.wikipedia.org/wiki/Read_Only_Memory "wikilink")、および外付け[RAM上の](../Page/Random_Access_Memory.md "wikilink")[RAMディスク](../Page/RAMディスク.md "wikilink")で利用可能な組込用の簡易ファイルシステム。
  - [SDメモリーカード](https://ja.wikipedia.org/wiki/SDメモリーカード "wikilink")等で利用可能な[FATファイルシステム](../Page/File_Allocation_Table.md "wikilink")。
  - NE2000互換ネットワークデバイスを使用し、[IP](../Page/Internet_Protocol.md "wikilink"),[TCP](../Page/Transmission_Control_Protocol.md "wikilink"),[UDP](../Page/User_Datagram_Protocol.md "wikilink"),[ICMP](../Page/Internet_Control_Message_Protocol.md "wikilink"),[ARPの各](../Page/Address_Resolution_Protocol.md "wikilink")[プロトコルに対応](../Page/通信プロトコル.md "wikilink")。
  - UDPおよびTCPの[APIによる](../Page/アプリケーションプログラミングインタフェース.md "wikilink")[クライアント](../Page/クライアント_\(コンピュータ\).md "wikilink")/[サーバ](../Page/サーバ.md "wikilink")。

[マルチタスク](../Page/マルチタスク.md "wikilink")の[タイムスライス](https://ja.wikipedia.org/wiki/タイムスライス "wikilink")が約1msと長く、常にシステムタスクに処理が割かれるために、リアルタイム性は比較的乏しい。また、sleep等の[APIで得られる時間が非常に大雑把であるため](../Page/アプリケーションプログラミングインタフェース.md "wikilink")、正確なタイミングを必要とするような場合は、ハードウェアのタイマーを利用することが必須となる。

## 関連項目

  - [組み込みオペレーティングシステム](../Page/組み込みオペレーティングシステム.md "wikilink")
  - [H8](../Page/H8.md "wikilink")
  - [SuperH](../Page/SuperH.md "wikilink")

## 外部リンク

  - [Micro Embeded System](http://mes.sourceforge.jp/mes24/)

[Category:組み込みオペレーティングシステム](https://ja.wikipedia.org/wiki/Category:組み込みオペレーティングシステム "wikilink")
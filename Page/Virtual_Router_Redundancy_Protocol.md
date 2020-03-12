> この記事は[Virtual Router Redundancy Protocol](https://ja.wikipedia.org/wiki/Virtual_Router_Redundancy_Protocol)から翻訳されています。


**Virtual Router Redundancy Protocol**（仮想ルータ冗長プロトコル・以下**VRRP**と略す）は[インターネット](../Page/インターネット.md "wikilink")上での[ルーター](../Page/ルーター.md "wikilink")の冗長化をサポートする[プロトコル](../Page/プロトコル.md "wikilink")。

## 概要

VRRPを使えば、「**マスター・ルーター**」と呼ばれる実際に稼働しているルーターに障害が発生した場合、直ちに「**バックアップ・ルーター**」と呼ばれる常時スタンバイさせている予備のルーターへ自動的に切り替えられて処理を引き継げるようになる。

VRRPは、同じLANにつながる数台のルーターを仮想的に1台のルーターとして扱えるようにする\[1\]日経NETWORK 2007年3月号 「最新バックアップテクニック ルーター」p31</ref>。仮想ルータとして扱えるようにするために、仮想ルーター用のIPアドレスを用意する。

VRRPは[1998年](https://ja.wikipedia.org/wiki/1998年 "wikilink")4月に RFC 2338 で定義された、同一内の[デフォルトゲートウェイ](https://ja.wikipedia.org/wiki/デフォルトゲートウェイ "wikilink")サービスホストの可用性を高めるため開発された非[プロプライエタリな冗長プロトコルである](../Page/プロプライエタリ・ソフトウェア.md "wikilink")。最新のプロトコルは[2010年](https://ja.wikipedia.org/wiki/2010年 "wikilink")3月の RFC 5798 である。

## IPアドレス

仮想ルーターには共通で使える1つのIPアドレスを持ち、マスター・ルーターと同じにするか、別のIPアドレスにするかは選択できる。しかし、仮想ルーターのIPアドレスをマスター・ルーターと同じにすると、マスター・ルーターの異常時にはtelnet等での接続が出来なくなるので、別にしたほうが利便性は増す。別にした場合は、IPアドレスが物理ルーターの2台分＋仮想ルーター1台分の3つが使われる\[2\]。

## 適用環境

VRRPは[イーサネット](../Page/イーサネット.md "wikilink")、[FDDI](../Page/Fiber_distributed_data_interface.md "wikilink")、[トークンリング](../Page/トークンリング.md "wikilink")上で用いることが可能である。RFC 5798で[IPv6](https://ja.wikipedia.org/wiki/IPv6 "wikilink")用のVRRP規格が決まった。VRRPは[ノーテル・ネットワークス](https://ja.wikipedia.org/wiki/ノーテル・ネットワークス "wikilink")、[シスコシステムズ](../Page/シスコシステムズ.md "wikilink")、[ジュニパーネットワークス](../Page/ジュニパーネットワークス.md "wikilink")、[華為技術](https://ja.wikipedia.org/wiki/華為技術 "wikilink")、[ファウンドリーネットワークス](../Page/ファウンドリーネットワークス.md "wikilink")、[エクストリームネットワークス](https://ja.wikipedia.org/wiki/エクストリームネットワークス "wikilink")、[3comなど多くのベンダのルータに採用されており](https://ja.wikipedia.org/wiki/スリーコム "wikilink")、また[Linux](../Page/Linux.md "wikilink")や[BSD](../Page/BSD.md "wikilink")でも使用可能である。

VRRPは[ルーティングプロトコル](https://ja.wikipedia.org/wiki/ルーティングプロトコル "wikilink")ではないので、IPルートをアドバタイズしたり、他のルータのルーティングテーブルに影響を与えることはない。

## VRRPの実装

仮想ルータは“00-00-5E-00-01-XX”という[MACアドレス](../Page/MACアドレス.md "wikilink")を使用する。最後の“XX”部分はVirtual Router IDentifier（VRID） といい、ネットワーク内にある仮想ルータごとで違う。このとき仮想ルータの中でこのアドレスを使っている物理ルータは、マスタールータ1つのみである。仮想ルータとして稼働している物理ルータ同士は、[マルチキャストアドレス](https://ja.wikipedia.org/wiki/マルチキャストアドレス "wikilink")（224.0.0.18）とIP[プロトコル番号](https://ja.wikipedia.org/wiki/プロトコル番号 "wikilink")112番を使用して通信しなければならない。

各物理ルーターには「**プライオリティ値**」（Priority値）がつけられている。仮想IPアドレスを自身の実IPアドレスとして持つルーターは255、バックアップ・ルーターは1から254の間、障害などによりマスター・ルーターからバックアップ・ルーターにステータス変更となったルーターには強制的にプライオリティ値「0」が割り当てられる。これはバックアップ・ルーターからマスター・ルーターへのステータス変更を迅速に行い、また一度障害を起こしたルーターをプライオリティ値の高い（マスターに近い）状態に置かないためである。

## マスター・ルーターの選定

マスター・ルーターとなっている物理ルーターが落ちた場合、以下の手順で代替のマスタールータが選定される。予め定められた期間（アドバタイズメントタイマ、advertisement timer）の3倍の期間、マスター・ルーターからのアドバタイズのマルチキャストパケットが受けられなかった場合、マスター・ルーターが落ちていると判断してバックアップ・ルーターが起動し、仮想ルーターはバックアップ・ルーターの中から新たなマスター・ルーターを選定するプロセスに入る。このプロセスでもマルチキャストパケットを使用する。

この選定プロセスのときに、バックアップ・ルーターがマルチキャストパケットを送信することに注意する必要がある。それ以外にバックアップ・ルーターがマルチキャストパケットを送信するのは、仮想ルータ内の物理ルータに現状のマスター・ルーターから置き換わるような設定を行ったときのみである。バックアップ・ルーターの中で最も高いプライオリティ値を持ったものが、マスター・ルーターとなると同時にプライオリティ値は「255」に繰り上げられる。仮想ルーターのIPアドレスを引き継いだマスター・ルーターは直ちに自身のMACアドレスと引き継いだIPアドレスを[ARPパケットにしてブロードキャスト送信する](../Page/Address_Resolution_Protocol.md "wikilink")。これによりMACアドレスとIPアドレスの新たな対応が同一セグメント内に伝達される。バックアップ・ルーターにおいてプライオリティ値が全て同一である場合、IPアドレスの数値が高いものがマスター・ルーターになる。切り替えは数秒程度で完了する\[3\]。

1つの仮想ルーターとして働く物理ルーターは全て1ホップの範囲内に収まっていなくてはならない。仮想ルータ内ではマスター・ルーターからバックアップ・ルーターへと定期的にアドバタイズメントパケットが流れているのは先ほど述べたが、この流れる間隔はアドバタイズメント・インターバルタイマーで調整できる。この間隔を短くすればするほど、ネットワークのダウンタイムを少なくすることができるが、マルチキャストのトラフィックが増える。

## 歴史

VRRPは米[Cisco](https://ja.wikipedia.org/wiki/Cisco "wikilink")社の保有するHSRP技術に基づいて規格化された。VRRPとHSRPの両者は似てはいるが互換性はない。

## 参考文献

<references/>

## 関連項目

  - [Hot Standby Router Protocol](https://ja.wikipedia.org/wiki/Hot_Standby_Router_Protocol "wikilink")（HSRP） - [シスコシステムズ](../Page/シスコシステムズ.md "wikilink")社製の[ルータ](https://ja.wikipedia.org/wiki/ルータ "wikilink")冗長ソリューション

  - [Gateway Load Balancing Protocol](https://ja.wikipedia.org/wiki/Gateway_Load_Balancing_Protocol "wikilink")（GLBP） - シスコシステムズ社製のルータ冗長兼ロードバランシングソリューション

  - [冗長化](../Page/冗長化.md "wikilink") - [フォールトトレラントシステム](../Page/フォールトトレラントシステム.md "wikilink") - [ホットスタンバイ](https://ja.wikipedia.org/wiki/ホットスタンバイ "wikilink")

  - [Common Address Redundancy Protocol](https://ja.wikipedia.org/wiki/Common_Address_Redundancy_Protocol "wikilink")（CARP）

  - （RSMT） - ノテル・ネットワークス社製のルータ冗長ソリューション

  - \- [データリンク層](../Page/データリンク層.md "wikilink")で[スイッチングハブ](../Page/スイッチングハブ.md "wikilink")間の複数の物理回線を束ねて1本の論理回線として扱う

  - \- [ロードバランサ](../Page/サーバロードバランス.md "wikilink")（負荷分散装置）などを用いて、[インターネット](../Page/インターネット.md "wikilink")などの[Wide Area Network](../Page/Wide_Area_Network.md "wikilink")（WAN）回線を[冗長化](../Page/冗長化.md "wikilink")すること

## 外部リンク

  - RFC 5798 VRRPについて定めたRFC

<!-- end list -->

  - 各種ソフトウェア
      - [VRRPd](http://sourceforge.net/projects/vrrpd/)；[GPLライセンスのソフトウエア](../Page/GNU_General_Public_License.md "wikilink")、[Linux](../Page/Linux.md "wikilink")・各[BSD](../Page/BSD.md "wikilink")・その他UNIXライクなOSで使える。
      - [keepalived](http://www.keepalived.org/)；GPLライセンスのソフトウエア、Linuxで使える。
      - [Shadow VRRPd](http://sourceforge.net/projects/svrrpd/)；[BSDライセンスのソフトウェア](https://ja.wikipedia.org/wiki/BSD_License "wikilink")、[Linux](../Page/Linux.md "wikilink")・各[BSD](../Page/BSD.md "wikilink")・[Solaris](../Page/Solaris.md "wikilink")で使える。

[Category:ルーティングプロトコル](https://ja.wikipedia.org/wiki/Category:ルーティングプロトコル "wikilink") [Category:通信プロトコル](https://ja.wikipedia.org/wiki/Category:通信プロトコル "wikilink") [Category:RFC](https://ja.wikipedia.org/wiki/Category:RFC "wikilink") [Category:長大な項目名](https://ja.wikipedia.org/wiki/Category:長大な項目名 "wikilink")

1.
2.
3.
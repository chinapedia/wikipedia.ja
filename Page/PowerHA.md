> この記事は[PowerHA](https://ja.wikipedia.org/wiki/PowerHA)から翻訳されています。


**PowerHA**（パワーエッチエー）は、[IBM](../Page/IBM.md "wikilink")の[POWERシステムベースの](../Page/POWER_\(マイクロプロセッサ\).md "wikilink")[AIX](https://ja.wikipedia.org/wiki/AIX "wikilink")および[Linux](../Page/Linux.md "wikilink")プラットフォーム用の、[高可用性のための](https://ja.wikipedia.org/wiki/High_availability "wikilink")[クラスターパッケージである](../Page/コンピュータ・クラスター.md "wikilink")。当初の名称は**High Availability Cluster Multiprocessing**（**HACMP**、エッチエーシーエムピー）だったが、[2008年](https://ja.wikipedia.org/wiki/2008年 "wikilink")に**PowerHA**と改名された。

## 概要

HACMPは[RS/6000](https://ja.wikipedia.org/wiki/RS/6000 "wikilink")の初期から提供が始まったが、当初はAIX用のみであり、ES機能は別ライセンスであった。

HACMPは、2台から32台のサーバをクラスターに結合し、サービスノードの障害発生時には、スタンバイノードへのリソースの引継ぎを自動で行う。引継ぎできるリソースには以下がある。

  - ディスク（外部ディスク装置上のボリュームグループ、論理ボリューム、[ファイルシステム](../Page/ファイルシステム.md "wikilink")）
  - ネットワーク（[IPアドレス](../Page/IPアドレス.md "wikilink")。構成によっては[MACアドレス](../Page/MACアドレス.md "wikilink")も可能。ノード内の複数[NIC間でも引継ぎ可能](https://ja.wikipedia.org/wiki/ネットワークカード "wikilink")）
  - アプリケーション（[DB2](https://ja.wikipedia.org/wiki/DB2 "wikilink")、[OracleなどのDBMS](../Page/Oracle_Database.md "wikilink")、[MQ](https://ja.wikipedia.org/wiki/MQ "wikilink")、[Tivoli](https://ja.wikipedia.org/wiki/Tivoli "wikilink")などの他、ユーザーアプリケーションも可能）

HACMPは、[日立](https://ja.wikipedia.org/wiki/日立 "wikilink")からもEP8000のAIX用（IBMからの[OEM](../Page/OEM.md "wikilink")）として販売されている。

[2008年](https://ja.wikipedia.org/wiki/2008年 "wikilink")4月の[Power Systems発表の際に](https://ja.wikipedia.org/wiki/Power_Systems "wikilink")、HACMPは**PowerHA for AIX and Linux**と改名され、プラットフォームに[Linux](../Page/Linux.md "wikilink")が追加された。ただしLinux版は、[x86](https://ja.wikipedia.org/wiki/x86 "wikilink")版のLinux用ではなく[POWER版のLinux用であり](../Page/POWER_\(マイクロプロセッサ\).md "wikilink")、また共有ディスクの引継ぎをPowerHAとしてはサポートしていないなど、AIX版とは相違がある。

[2009年](../Page/2009年.md "wikilink")10月には「PowerHA SystemMirror for AIX V6.1」が発表された。これはPowerHA for AIX 5.5の後継であり、従来のSmart Assistの機能が追加された。また2つのエディション (Standard Edition, Enterprise Edition)、3段階の料金体系 (small, medium, large) となった。

[2010年](https://ja.wikipedia.org/wiki/2010年 "wikilink")8月には「PowerHA SystemMirror for AIX V7.1」（Standard Editionのみ）が発表された。AIX 7.1のCluster Aware 機能との連係、IBM Systems Directorベースの管理インターフェースなどが追加された。

## 構成

HACMP（PowerHA、以下同様）はクラスターとして、複数のノード（サーバ、OS）に導入・構成され、ノードの稼動状況を相互監視する。サービス側のノードが障害と判断した場合には、事前登録したリソース（[IPアドレス](../Page/IPアドレス.md "wikilink")、外部ディスク上の[ファイルシステム](../Page/ファイルシステム.md "wikilink")、起動[プロセス](../Page/プロセス.md "wikilink")等）を、スタンバイ側の別のノードへ自動引継ぎ（フェイルオーバー、テイクオーバー）する。

引継ぎパターンは、正副構成（サービス機とスタンバイ機）、相互バックアップ（サービス機同士で障害時は片寄せし、縮退運用）、カスケーティング（クラスタ内の適当なスタンバイノードへ引継ぎ）などが可能である。

HACMPは一部のプロセスと多数の[シェルスクリプト](../Page/シェルスクリプト.md "wikilink")より構成されており、シェルスクリプトはユーザーによるカスタマイズが可能である（このため、カスタマイズには一定のスキルが必要な反面、きめ細かい構成・運用が可能となる）。

HACMPは、監視・判断・引継ぎ操作などのオペレーションを自動化して、サービス停止時間を最小にするソリューションであり、無停止ソリューションではない（障害発生から引継ぎ完了までの間、および戻しの間はサービス停止となる）。

また、各ノードのハードウェア障害やOS障害などには対応できるが、引継ぎ対象リソース（外部ディスク装置、アプリケーション）自体の障害には対応できないので、[単一障害点](https://ja.wikipedia.org/wiki/単一障害点 "wikilink")（SPOF）の除去の観点からは、別の冗長化（外部ディスク装置側の冗長化など）を組み合わせる事が望ましい。更に、[LPAR](../Page/LPAR.md "wikilink")（論理区画）などを使用している場合は、サービスノードとスタンバイノードは、サーバ筐体は当然ながら分ける事が望ましい。

ただしオプションの HACMP Extended Distance (HACMP/XD) は、距離が無制限のデータ・ミラーリングとリカバリーを提供する、災害復旧（ディザスター・リカバリー）ソリューションであり、単一障害点の視点は上述とは異なる。

なお、[WebSphere](../Page/WebSphere.md "wikilink") Application Serverや[Dominoなどの高可用性には](https://ja.wikipedia.org/wiki/Lotus_Notes "wikilink")、HACMPではなく、それぞれのミドルウェアのクラスタ機能を使う場合が一般的である。

## 動作仕様

高可用クラスターとして、各ノードの生存をハートビート機能により相互に確認し合う。具体的には[KeepAlive](https://ja.wikipedia.org/wiki/キープアライブ "wikilink")(KA)パケットを相互に送信するが、その経路はネットワークアダプタ経由の[TCP/IP](https://ja.wikipedia.org/wiki/TCP/IP "wikilink")によるものに加え、非IP経路として共有ディスクまたは非同期通信（シリアル、いわゆる[RS-232](../Page/RS-232.md "wikilink")C、EIA-232-D）のいずれかを組み合わせる事が推奨されている。

非IP経路との組み合わせを推奨する理由は、[TCP/IP](https://ja.wikipedia.org/wiki/TCP/IP "wikilink")経由のみではネットワーク障害（[NIC障害](https://ja.wikipedia.org/wiki/ネットワークカード "wikilink")、LANケーブル障害、Ethernetスイッチ障害など）の場合に相手ノードの生死が正確に判定できないため、誤った引継ぎが発生して共有ディスク上のデータの不整合や破損が発生する事を、最少化するためである。なお、RS-232Cはノイズが乗り易く排他制御が利かないなど信頼性が低いため、HACMPではサポートするシリアルアダプターを明示している（標準搭載のRS-232Cポートは通常サポートされていない）。また2009年現在では、RS-232C経由よりも共有ディスク経由の使用が一般化している。

[スプリットブレインシンドローム](https://ja.wikipedia.org/wiki/スプリットブレインシンドローム "wikilink")対策として、KA信号（経路）の多重化及び、特定のデバイスに特化しない事を前提とし、更にサービスノードより強制終了させる、孤立してしまった旧サービスノードはDeadman Switchにより「自爆」する、などが実装されている。

基本機能であるプロセスの起動時名称による監視はpsコマンドによるものだが、拡張機能としてHACMP5.1以降に追加されたユーザー作成によるシェルスクリプトを使用した拡張監視機能を使用すれば、多くのソフトウェアパッケージの細かい動作を監視する事が可能となった。

## 比較

他社の一般的なクラスター製品と比較し、以下の指摘がある。

  - アプリケーションを登録する際の考慮点やカスタマイズすべきシェルスクリプトの数が多く、スキルが必要
  - サービス監視やサービスの依存リソースの監視などの機能が少なく、カスタマイズにはスキルが必要
  - 設定がCUI画面（AIXではsmit）が基本であり、操作性が良くない
  - 実績にはIBM製品（[System p](https://ja.wikipedia.org/wiki/System_p "wikilink")、[DB2](https://ja.wikipedia.org/wiki/DB2 "wikilink")、[MQ](https://ja.wikipedia.org/wiki/MQ "wikilink")など）との組み合わせが多く、[Oracle Databaseなどの実績は](../Page/Oracle_Database.md "wikilink")（存在するが）比率は多くない

なお、[AIX](https://ja.wikipedia.org/wiki/AIX "wikilink") 6 の標準機能であるライブ・アプリケーション・モビリティーや、x86サーバで一般的な[VMware](https://ja.wikipedia.org/wiki/VMware "wikilink") ESX の VMotionなどと比較すると、HACMPは障害検知と引継ぎ開始が自動で行える反面、引継ぎ（および戻し）の最中にはサービス停止を伴う。

また、x86サーバでの[VMware](https://ja.wikipedia.org/wiki/VMware "wikilink") ESXのVMwareHAと比較すると、VMwareHAはハードウェア全体やESX自体の障害しか検知できないが、HACMPは対象ノード（OS）のハングや[NIC障害も検知し引継ぎ可能である](https://ja.wikipedia.org/wiki/ネットワークカード "wikilink")。

## 参照

  - [PowerHA SystemMirror for AIX Standard / Enterprise Edition V6.1の発表 - IBM](http://www-06.ibm.com/jp/domino02/NewAIS/aisextr.nsf/ByLetterNo/PWR09111?OpenDocument&ExpandSection=1&highlight=0,%5BTitle0%5D=POWERHA)
  - [IBM PowerHA SystemMirror Standard Edition V7およびPowerHA SystemMirror Enterprise Edition V6機能拡張の発表](http://www-06.ibm.com/jp/domino02/NewAIS/aisextr.nsf/ByLetterNo/PWR10093)

## 関連項目

  - [コンピュータ・クラスター](../Page/コンピュータ・クラスター.md "wikilink")
  - [クラスタリング](https://ja.wikipedia.org/wiki/クラスタリング "wikilink")

## 外部リンク

  - [PowerHA SystemMirror for AIX - 日本IBM](http://www-06.ibm.com/systems/jp/power/software/ha/)
  - [PowerHA SystemMirror / PowerHA for AIX / HACMP - 日立製作所(EP8000、AIX用）](http://133.145.224.19/Prod/comp/soft1/AIX/product/lineup/hacmp.html)
  - [PowerHA SystemMirror マニュアル - IBM](http://publib.boulder.ibm.com/infocenter/aix/v7r1/index.jsp?topic=/com.ibm.aix.doc/doc/base/powerha_pdf.htm)

[Category:UNIX](https://ja.wikipedia.org/wiki/Category:UNIX "wikilink") [Category:IBMのソフトウェア](https://ja.wikipedia.org/wiki/Category:IBMのソフトウェア "wikilink")
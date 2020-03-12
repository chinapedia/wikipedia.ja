> この記事は[HP-UX](https://ja.wikipedia.org/wiki/HP-UX)から翻訳されています。


**HP-UX** (**H**ewlett-**P**ackard **U**NI**X**) は、旧[ヒューレット・パッカード](../Page/ヒューレット・パッカード.md "wikilink")（HP）社、現[ヒューレット・パッカード・エンタープライズ](https://ja.wikipedia.org/wiki/ヒューレット・パッカード・エンタープライズ "wikilink")（HPE）社製の [UNIX](../Page/UNIX.md "wikilink") [オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink")である。ワークステーションおよび中・大規模システム用サーバに採用されている。[System V](../Page/UNIX_System_V.md "wikilink")（初期は[System III](../Page/UNIX_System_III.md "wikilink")）ベースの[プロプライエタリUNIXである](../Page/プロプライエタリ・ソフトウェア.md "wikilink")。

## 特徴

企業の基幹系システムに用いる中・大規模[サーバ](../Page/サーバ.md "wikilink")に要求される、高い信頼性を持つとされる。特に通信、金融／証券系のシステムにおいて、[TCP/IP](../Page/インターネット・プロトコル・スイート.md "wikilink") に準拠した既存パッケージを改造する事無く、簡易な[シェル](../Page/シェル.md "wikilink")スクリプトの生成にて適用できる高可用[クラスタパッケージ](../Page/コンピュータ・クラスター.md "wikilink") [MC/ServiceGuard](https://ja.wikipedia.org/wiki/MC/ServiceGuard "wikilink")(現在名は HP Serviceguard) が評価され、日本でも多くの通信、金融／証券系ユーザの基幹系システムプラットホームとして稼動している。MC/ServiceGuard の動作監視機能（TOC タイマ）をカーネルに組み込んでおり、商用クラスタ構成での信頼性・実績を持つ。

日本では、[NTTドコモ](https://ja.wikipedia.org/wiki/NTTドコモ "wikilink")の[iモード](https://ja.wikipedia.org/wiki/iモード "wikilink")のサーバに使われていることで有名\[1\]。

自社の[PA-RISC](../Page/PA-RISC.md "wikilink")及び、[インテル](https://ja.wikipedia.org/wiki/インテル "wikilink")の[Itanium](../Page/Itanium.md "wikilink")系[CPU](../Page/CPU.md "wikilink")での動作を保証している。Itanium系では、[EPIC採用のため](../Page/EPICアーキテクチャ.md "wikilink")[PA-RISC](../Page/PA-RISC.md "wikilink")系とはCPUアーキテクチャが異なるが、[エミュレータ](../Page/エミュレータ.md "wikilink")（Ariesバイナリトランスレータ）により[バイナリ](../Page/バイナリ.md "wikilink")レベルの互換性を提供している。ただし、エミュレーションによるパフォーマンスへの影響を回避してItanium系本来のパフォーマンスを得るためには、[ソースコード](../Page/ソースコード.md "wikilink")の再コンパイルが必要となる。またCPUアーキテクチャの変更によりオブジェクトサイズが大きくなる傾向がある。

大規模システムでは大容量かつ大量のデータを扱うため、高いレベルでの入出力データ処理能力や[高可用性](../Page/高可用性.md "wikilink")を要求される。システムが確保可能なディスク領域は、[論理ボリュームマネージャ](../Page/論理ボリュームマネージャ.md "wikilink")（LVM、[VxVM](https://ja.wikipedia.org/wiki/VxVM "wikilink")）によって管理され、データエリアの柔軟な管理や障害発生時の代替処理に対応する。一方で、[ジャーナル・ファイル・システム](../Page/ジャーナリングファイルシステム.md "wikilink")([VxFS](https://ja.wikipedia.org/wiki/VxFS "wikilink"))によって、大容量データの入出力や更新処理を効率よく行えるように最適化されている。また、障害発生時にもファイル構造の復旧を速やかに行えるようになっている。VxVMやVxFSは、かつて存在した[VERITAS](../Page/VERITAS.md "wikilink")社の商用パッケージを採用したものである。

日本のベンダである[NEC](../Page/日本電気.md "wikilink")・[日立製作所](../Page/日立製作所.md "wikilink")・[沖電気工業](../Page/沖電気工業.md "wikilink")・[三菱電機](../Page/三菱電機.md "wikilink")などがOEM販売を、さらにNEC・日立製作所が自社開発による互換サーバを販売している。NECは[NX7700iシリーズ](http://jpn.nec.com/nx7700i/)やシグマグリッドを、日立は[BladeSymphony](http://www.hitachi.co.jp/products/bladesymphony/index.html)の1000シリーズのうちIPFブレードを製造している。

## 歴史

初期のバージョンは[Apollo/Domainシステムに対応していた](../Page/アポロコンピュータ.md "wikilink")。[モトローラ](../Page/モトローラ.md "wikilink")[68000シリーズのプロセッサに基づいた](../Page/MC68000.md "wikilink")[HP 9000シリーズ](../Page/HP_9000.md "wikilink")200、300、400システムや、HPのFOCUSアーキテクチャに基づいたHP 9000シリーズ500システムでも用いられていた。

2009年現在はPA-RISCレンジのプロセッサと[IA-64](../Page/IA-64.md "wikilink")プロセッサに対応している。バージョンはHP-UX 11i v3 (B.11.31)である。11iとは 11.0のインターネット対応機能強化版の位置付け。11i v1 (B.11.11)において、NTTドコモのiモード[ゲートウェイ](https://ja.wikipedia.org/wiki/ゲートウェイ "wikilink")システム([CIRCUS](https://ja.wikipedia.org/wiki/CIRCUS_\(システム\) "wikilink"))の提案を行う際に強化した機能を標準化し、その上に[スレッド動作をN](../Page/スレッド_\(コンピュータ\).md "wikilink"):Mスレッドに変更している。

## 出典

## 関連項目

  - [UNIX](../Page/UNIX.md "wikilink")
  - [ヒューレット・パッカード・エンタープライズ](https://ja.wikipedia.org/wiki/ヒューレット・パッカード・エンタープライズ "wikilink") (Hewlett Packard Enterprise, HPE)
      - [日本ヒューレット・パッカード](../Page/日本ヒューレット・パッカード.md "wikilink")

## 外部リンク

  - [Hewlett Packard Enterprise](http://www.hpe.com/)
      - [日本ヒューレット・パッカード — HP-UX](http://www.hpe.com/jp/hpux)
      - [日本ヒューレット・パッカード — HAクラスターの教科書](https://h50146.www5.hpe.com/products/software/oe/hpux/developer/column/sg_text.pdf)
  - [LinuxJF_Project - LVM_HowTo](https://linuxjf.osdn.jp/JFdocs/LVM-HOWTO.html)

[Category:Unix系オペレーティングシステム](https://ja.wikipedia.org/wiki/Category:Unix系オペレーティングシステム "wikilink") [Category:System_V](https://ja.wikipedia.org/wiki/Category:System_V "wikilink") [Category:ヒューレット・パッカード・エンタープライズ](https://ja.wikipedia.org/wiki/Category:ヒューレット・パッカード・エンタープライズ "wikilink") [Category:1984年のソフトウェア](https://ja.wikipedia.org/wiki/Category:1984年のソフトウェア "wikilink")

1.
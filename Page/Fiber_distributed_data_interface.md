> この記事は[Fiber distributed data interface](https://ja.wikipedia.org/wiki/Fiber_distributed_data_interface)から翻訳されています。


[thumb](https://ja.wikipedia.org/wiki/ファイル:FDDI_Concentrator.jpeg "wikilink") [thumb用のデュアルアタッチFDDIボード](https://ja.wikipedia.org/wiki/ファイル:Sbus-das-fddi.jpg "wikilink")\]\]

**Fiber-distributed data interface** (**FDDI**) は、[LAN](../Page/Local_Area_Network.md "wikilink") で[データ](../Page/データ.md "wikilink")[転送](https://ja.wikipedia.org/wiki/転送 "wikilink")を行なうための標準の一つである。

## 概要

データ長は4500[オクテット](../Page/8ビット.md "wikilink")、最大ネットワーク長は200km、最大ノード間距離は2000m、最大接続端末は500台である。 FDDI プロトコルは[トークンリング](../Page/トークンリング.md "wikilink")[プロトコル](../Page/プロトコル.md "wikilink")をベースとして採用している。広大な地理的な地域をカバーすることに加えて、 FDDI による LAN は何千人ものユーザをサポートすることができる。標準的な構成として[光ファイバー](../Page/光ファイバー.md "wikilink")が使用される([銅線](https://ja.wikipedia.org/wiki/銅線 "wikilink")のケーブルを使用することも可能だが、その場合は [CDDI](https://ja.wikipedia.org/wiki/Copper_distributed_data_interface "wikilink") となる)。 FDDI は二重リング構成になっており、[トークンリング](../Page/トークンリング.md "wikilink")方式を使用する。

FDDI は [ANSI 米国規格協会](https://ja.wikipedia.org/wiki/ANSI "wikilink"), の X3-T9 が主になって標準化された。他のプロトコルを使用する LAN の[OSI参照モデル](../Page/OSI参照モデル.md "wikilink")に従う。 FDDI-II は FDDI の一種で、[交換機](../Page/交換機.md "wikilink")のサービスをネットワークに加え、音声や映像などマルチメディアを扱うことができる。 FDDI ネットワークとひろがりつつある [Synchronous Optical Network](https://ja.wikipedia.org/wiki/Synchronous_Optical_Network "wikilink") SONET との接続が始まった。

FDDI ネットワークは二重リング構成になっており、一次リングが故障した場合にバックアップを行うための二次リングを持つ。一次リングは最大 100 [Mbps](https://ja.wikipedia.org/wiki/Mbps "wikilink") の伝送速度を提供する。また、ネットワークが二次リングをバックアップとして必要としないときは、二次リングでデータを伝送して伝送速度を 200 Mbps に広げることができる。単一のリングは最大距離を広げることができる。二重リングは 100km まで広がることができる。 FDDI は標準的な 100 Mbps のイーサネットより大きな最大フレーム・サイズを持ち、スループットをよくすることができる。

FDDI ネットワークを設計する場合、通常は複数の FDDI リングが階層的に接続された構造にする。FDDI リング同士はいくつかの機器([ルータ](https://ja.wikipedia.org/wiki/ルータ "wikilink")や[集線装置](https://ja.wikipedia.org/wiki/集線装置 "wikilink")の場合が多い)で接続される(**デュアルアタッチ**)。コンピューターはルータや集線装置に**シングルアタッチ**で接続される。もっとも単純な構造の FDDI リングは機器が1個の場合である。一般にはコンピューター室程度の広さで FDDI ネットワークが構成されるが、都市内ネットワークのような広域 FDDI が実現した例もある。

リング構成のばあい、データ回線は接続された機器全てを必ず通過し、かつそれらの機器全てが常時運用されていなければならないため、 FDDI は複数のリングによる階層構成が必要とされる(通常は光ファイバーによるバイパスも考慮されるが、ネットワーク技術者によれば信頼性に欠けてエラーを起こしやすいと)。[ネットワーク管理者](https://ja.wikipedia.org/wiki/ネットワーク管理者 "wikilink")による制御が難しい[ワークステーション](../Page/ワークステーション.md "wikilink")や[ミニコンピュータ](../Page/ミニコンピュータ.md "wikilink")は FDDI 接続向きではない。

デュアルアタッチの代わりに、[ワークステーション](../Page/ワークステーション.md "wikilink")を**デュアルホーム**(同一 FDDI リング内の異なる2つの機器に接続すること)とし、デュアルアタッチと同程度の信頼性を得ることもできる。片方の接続が有効な場合、もう片方の接続は自動的にブロックされる。最初にコネクションが失敗した場合にはバックアップ用の接続が瞬時に引き継ぐ。

主に構内[イーサネット](../Page/イーサネット.md "wikilink")の相互接続に用いられてきたが、速度・費用・汎用性から[Fast Ethernetや](../Page/イーサネット.md "wikilink")([1998年](https://ja.wikipedia.org/wiki/1998年 "wikilink")以降は)[Gigabit Ethernetが普及し](../Page/イーサネット.md "wikilink")、FDDI は用いられなくなってきた。 現在ではベンダーも FDDI から撤退し、利用は終焉しつつある。

4つの FDDI 標準には次のものが含まれる。

  - ANSI X3T9.5, containing Physical Media Dependent (PMD) specifications
  - ANSI X3T9.5, containing the Physical (PHY) specifications
  - ANSI X3.139, containing Media Access Control (MAC) specifications
  - ANSI X39.5, containing the Station Management (SMT) specifications.

*出典: [Federal Standard 1037C](https://ja.wikipedia.org/wiki/Federal_Standard_1037C "wikilink") 及び <http://www.Foldoc.org> から許可を得て使用。*

## 商用サービス

[電気通信事業者](../Page/電気通信事業者.md "wikilink")がFDDIを使った商用サービスを行った例も少数ながら存在する。

日本では[1998年](https://ja.wikipedia.org/wiki/1998年 "wikilink")に、[東京電力](https://ja.wikipedia.org/wiki/東京電力 "wikilink")系の東京通信ネットワーク（TTNet、後の[パワードコム](../Page/パワードコム.md "wikilink")）が「FDDI専用サービス」の名称で、FDDIによる[専用線](../Page/専用線.md "wikilink")サービスの提供を開始した。ただしFDDIというプロトコルの制約から接続出来る距離の制限が厳しかった（TTNetでは接続範囲を「同一[MA内](https://ja.wikipedia.org/wiki/単位料金区域 "wikilink")」としていた\[1\]）、標準の契約はシングルホーム構成となっていたためデュアルホーム（リング）構成を取るには2回線分の契約が必要だったなど、いろいろ制約が大きいサービスであったことに加え、2000年代に入ると[広域イーサネット](../Page/広域イーサネット.md "wikilink")サービスの価格が急速に低下し価格競争力を失ったことなどから、サービスとしてはあまり普及しなかった。パワードコムが[KDDI](../Page/KDDI.md "wikilink")に吸収合併された後もKDDIによりサービスが提供されていたが、[2007年](../Page/2007年.md "wikilink")頃にサービスの提供が終了したものと見られる\[2\]。

## 脚注

[Category:インターネットのプロトコル](https://ja.wikipedia.org/wiki/Category:インターネットのプロトコル "wikilink") [Category:コンピュータ関連のスタブ項目](https://ja.wikipedia.org/wiki/Category:コンピュータ関連のスタブ項目 "wikilink")

1.  [FDDI専用サービス](http://itpro.nikkeibp.co.jp/word/page/10007433/) - ITPro・ネットワーク大事典
2.  KDDIの[専用サービス契約約款](http://www.kddi.com/corporate/kddi/kokai/keiyaku_yakkan/pdf/private_pwd.pdf)には、2007年頃まで「附則」の項に『FDDI専用サービス』に関する記述が見られる。
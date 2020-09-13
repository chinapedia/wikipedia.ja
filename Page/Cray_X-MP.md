> この記事は[Cray X-MP](https://ja.wikipedia.org/wiki/Cray_X-MP)から翻訳されています。


**Cray X-MP**は、[クレイ](../Page/クレイ.md "wikilink")リサーチ社が設計・製造・販売した[スーパーコンピュータ](../Page/スーパーコンピュータ.md "wikilink")である。1975年の[Cray-1](../Page/Cray-1.md "wikilink")の後継として[1982年](../Page/1982年.md "wikilink")にリリースされ、1983年から1985年にかけて世界最高速のコンピュータであった。主要設計者は[スティーブ・チェン](../Page/スティーブ・チェン_\(スーパーコンピュータ設計者\).md "wikilink")。

## 詳細

[thumbの](https://ja.wikipedia.org/wiki/ファイル:CRAY_X-MP_IMG_9135.jpg "wikilink")[EPFLにある](../Page/スイス連邦工科大学ローザンヌ校.md "wikilink") CRAY-XMP48\]\] Cray-1からの主な改良点は、クレイ・リサーチ初の共有メモリ型[並列](../Page/並列計算.md "wikilink")[ベクトル計算機](../Page/ベクトル計算機.md "wikilink")だという点である。主筐体に2個の[CPU](../Page/CPU.md "wikilink")を格納しており、外観は Cray-1 の[蹄鉄](../Page/蹄鉄.md "wikilink")型のデザインを踏襲している。

プロセッサのクロックは105MHz（1サイクル9.5ナノ秒）である（Cray-1Aでは12.5ns）。[バイポーラ](../Page/バイポーラトランジスタ.md "wikilink")[ゲートアレイ](https://ja.wikipedia.org/wiki/ゲートアレイ "wikilink")[集積回路](../Page/集積回路.md "wikilink") (IC) で構成されており、個々のICは16個の[ECL](../Page/エミッタ結合論理.md "wikilink")[ゲートを集積している](https://ja.wikipedia.org/wiki/論理回路 "wikilink")。CPUアーキテクチャは Cray-1 とよく似ているが、メモリ帯域幅が改善されており（リードポート2個とライトポート1個）、*chaining* サポート（[Cray-1](../Page/Cray-1.md "wikilink")を参照）も強化されている。理論的なピーク性能は1CPU当たり 200 [MFLOPSで](../Page/FLOPS.md "wikilink")、システムのピーク性能は400MFLOPSである\[1\]。

X-MPは当初、200万ワード（1ワードは64ビットで、16MB）の主記憶を16バンクに分けてサポートしていた。メモリ帯域幅はCray-1から大幅に改善された。Cray-1ではリードポートとライトポートが1つずつだったが、X-MPではリードポートが2つになっており、I/O専用ポートも別に設けている。主記憶は4Kビットのバイポーラ [SRAM](../Page/Static_Random_Access_Memory.md "wikilink") IC で構成されている。CMOSメモリ版の Cray-1M は Cray X-MP/1s と改称された。この構成は当初、クレイ・リサーチでのUNIX移植に使われた。

1984年、X-MPの改良モデルが発表となり、プロセッサ数は1/2/4、メモリ容量は400万ワード/800万ワードという構成の機種が登場した。最上位機種 X-MP/48 は4CPUで理論上のピーク性能は800MFLOPSを越え、メモリ容量は800万ワードである\[2\]。これら機種のCPUは[gather/scatter方式のメモリ参照命令を導入している](https://ja.wikipedia.org/wiki/:en:Gather-scatter_\(vector_addressing\) "wikilink")。最大主記憶容量は1600万ワードまでとなり、実際に搭載可能なメモリ容量は機種によって異なる。SRAMメモリチップも機種によってバイポーラまたはMOSを採用している。

システムは当初、独自の *[Cray Operating System](https://ja.wikipedia.org/wiki/:en:Cray_Operating_System "wikilink")* (COS) を搭載し、Cray-1とオブジェクトコードレベルで互換性を保っていた。[UNIX System V](../Page/UNIX_System_V.md "wikilink") から派生した CX-OS は最終的に [UniCOS](https://ja.wikipedia.org/wiki/UNICOS "wikilink") となり、ゲスト[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink")機能として実行した。1986年以降 UniCOS は主OSとなった。[DOEは標準のOSではなく](../Page/アメリカ合衆国エネルギー省.md "wikilink") [Cray Time Sharing System](https://ja.wikipedia.org/wiki/:en:Cray_Time_Sharing_System "wikilink") を採用した。Cray-1とX-MPはほぼ完全互換なので、その他のソフトウェアについては、[Cray-1](../Page/Cray-1.md "wikilink")のソフトウェアの節を参照。

## EAシリーズ

1986年、クレイ・リサーチは X-MP Extended Architecture シリーズを発表。EAシリーズのCPUはクロック周波数が117MHz（8.5ナノ秒）となり、およびゲートアレイICで構成されている。EAシリーズではアドレスレジスタ（AとB）を32ビットに拡幅し、理論上20億ワードまで扱えるようにしている。実際の最大構成は6400万ワードの MOS SRAM を64バンクで構成したものだった。互換性のため24ビットアドレッシングもサポートしており、Cray-1や従来のX-MP向けの既存ソフトウェアを実行可能である。EAシリーズのCPUのピーク性能は234MFLOPSで、4CPU構成のシステムのピーク性能は942MFLOPSとなった。

## I/Oサブシステム

[thumb](https://ja.wikipedia.org/wiki/ファイル:Cray_DD49_-_Musée_des_arts_et_métiers.jpg "wikilink") I/Oサブシステムは2つから4つのI/Oプロセッサを搭載でき、合計で2台から32台のディスクユニットを接続できる。DD-39とDD-49というハードディスク装置は、容量1.2GBで転送レートはそれぞれ5.9MB/sと9.8MB/sである。オプションの[ソリッドステートドライブ](../Page/ソリッドステートドライブ.md "wikilink")は、256/512/1024MBの容量で転送レートはチャネル当たり100から1,000MB/sである\[3\]。

## 価格

1984年時点のX-MP/48は1500万ドルで、ディスク装置の価格は含まない。1985年、[ベル研究所](../Page/ベル研究所.md "wikilink")は Cray X-MP/24 を1050万ドル、8台のDD-49を100万ドルで購入した。その際、Cray-1を下取りに出し、150万ドルで買い取ってもらっている\[4\]。1987年、[本田技術研究所](../Page/本田技術研究所.md "wikilink")は Cray X-MP/12 を700万ドル（10億5000万円）で購入した\[5\]。

## 日本での導入実績

日本ではX-MPシリーズは少なくとも以下の企業に導入されている。

  - [NTT](../Page/日本電信電話.md "wikilink") 基礎研究所 - X-MP/22\[6\]、X-MP/1\[7\]
  - [東芝](../Page/東芝.md "wikilink") - X-MP/22\[8\]
  - [日産自動車](../Page/日産自動車.md "wikilink") 宇宙航空部門 - X-MP/11\[9\]
  - [本田技術研究所](../Page/本田技術研究所.md "wikilink") - X-MP/12\[10\]
  - [センチュリ リサーチ センタ](https://ja.wikipedia.org/wiki/CRCソリューションズ "wikilink") - 機種不明\[11\]
  - [リクルート](../Page/リクルートホールディングス.md "wikilink") - X-MP/216\[12\]

## イメージ・ギャラリー

Image:EPFL CRAY-I 2.jpg|CRAY X-MP/48 の制御パネル Image:EPFL CRAY-I 3.jpg|CRAY X-MP/48 の論理回路基板 Image:EPFL CRAY-I 4.jpg|CRAY X-MP/48 の冷却システム Image:BSC-CRAY-X-MP-EA-A.JPG|CRAY X-MP/24 （バルセロナ・スーパーコンピューティング・センター） Image:BSC-CRAY-X-MP-EA-B.JPG|CRAY X-MP/24 （バルセロナ・スーパーコンピューティング・センター）

## 後継機種

完全新規設計の[Cray-2](../Page/Cray-2.md "wikilink")は1985年に登場した。全く異なったコンパクトな4プロセッサ設計で、主記憶容量は512Mバイトから4Gバイトであった。性能は500MFLOPSと言われたが、メモリの[レイテンシ](../Page/レイテンシ.md "wikilink")が大きかったために計算の種類によってはX-MPよりも遅かった。

X-MPの直接の後継である [Cray Y-MP](../Page/Cray_Y-MP.md "wikilink") シリーズは1988年から登場した。設計に目新しい点はなく、最大 8個の改良されたプロセッサを接続できるようにX-MPを進化させたものである。実装面では16ゲートのECL[ゲートアレイ](https://ja.wikipedia.org/wiki/ゲートアレイ "wikilink")ICからVLSIに集積度を向上させている。

## ポップカルチャーにおけるX-MP

  - [トム・クランシー](../Page/トム・クランシー.md "wikilink")の『[レッド・オクトーバーを追え\!](../Page/レッド・オクトーバーを追え!.md "wikilink")』では、[アメリカ空軍](https://ja.wikipedia.org/wiki/アメリカ空軍 "wikilink")の X-MP を使って潜水艦レッド・オクトーバーの性能と音響特性を計算する設定になっていた。
  - 映画『[トロン](../Page/トロン_\(映画\).md "wikilink")』には、X-MPが見えるシーンがある。また、エンドロールで "Supercomputer" として Cray X-MP がクレジットされている。
  - 映画『[スター・ファイター](../Page/スター・ファイター_\(映画\).md "wikilink")』では、3DCGのレンダリングにX-MPを使っている\[13\]。
  - [マイクル・クライトン](https://ja.wikipedia.org/wiki/マイクル・クライトン "wikilink")の小説『[ジュラシック・パーク](../Page/ジュラシック・パーク.md "wikilink")』では、パークのコンピュータとして Cray X-MP を3台使用している設定となっていた。

## 脚注

## 参考文献

  - Keith Robbins and S. Robbins (1989) *Lecture Notes in Computer Science: The Cray X-MP/Model 24* Springer ISBN 3-540-97089-4

## 関連項目

  - [リクルート事件](../Page/リクルート事件.md "wikilink")

[Category:スーパーコンピュータ](https://ja.wikipedia.org/wiki/Category:スーパーコンピュータ "wikilink") [Category:クレイのハードウェア](https://ja.wikipedia.org/wiki/Category:クレイのハードウェア "wikilink")

1.  Cray Research, Inc. (1985). ["The Cray X-MP Series of Computer Systems"](http://archive.computerhistory.org/resources/text/Cray/Cray.X-MP.1985.102646183.pdf).
2.
3.
4.
5.  「スーパーコンピューター、本田、米クレイ社製購入―新車開発実験などに採用」『日本経済新聞』 1987年1月30日朝刊、9面。
6.  「NTT、2台目購入、米クレイ社からスーパー電算機。」『日本経済新聞』 1985年9月28日朝刊、8面。
7.
8.  「東芝、米クレイから購入―スーパーコン、日本で今年5台目」『日本経済新聞』 1989年9月26日朝刊、10面。
9.  「日産、クレイにスーパー電算機発注―米の批判回避狙う。」『日本経済新聞』 1985年5月15日夕刊、1面。
10.
11. 「日本クレイ 急激な伸び、スーパー電算機、官公庁などの需要高まる。」『日経産業新聞』 1987年9月25日、9面。
12.
13. [Ohio State University CG history page](http://design.osu.edu/carlson/history/lesson6.html#dp)
> この記事は[PCI Express](https://ja.wikipedia.org/wiki/PCI_Express)から翻訳されています。


[thumb](https://ja.wikipedia.org/wiki/ファイル:PCI-Express-Bus-1-lane.jpg "wikilink") [thumb上のPCI](https://ja.wikipedia.org/wiki/ファイル:PCI-Express-Bus.jpg "wikilink") Express x16 スロット\]\] **PCI Express**（ピーシーアイエクスプレス）は、[2002年](../Page/2002年.md "wikilink")にによって策定された、[I/Oシリアルインタフェース](../Page/入出力.md "wikilink")、[拡張バスの一種である](../Page/バス_\(コンピュータ\).md "wikilink")。書籍、文書では**PCIe**と表記されることも多い。この表記はPCI-SIG自身もウェブサイト上で使用している。[PCI-X](../Page/PCI-X.md "wikilink")はパラレルインタフェースの別規格である。

## 概要

[PCIバス](../Page/Peripheral_Component_Interconnect.md "wikilink")、および[PCI-X](../Page/PCI-X.md "wikilink")バスの欠点を補うべく[インテル](https://ja.wikipedia.org/wiki/インテル "wikilink")が開発を進めていた*3rd. Generation I/O*、**3GIO**（スリージーアイオー）を基とする。

PCI Express 1.1は、1レーンあたり2.5 [Gbpsでデータ転送に](../Page/ビット毎秒.md "wikilink")80[パーセント](../Page/パーセント.md "wikilink")が使用され、送信／受信を分離した[全二重方式を採用し](../Page/複信.md "wikilink")、計5 Gbpsの[転送速度](https://ja.wikipedia.org/wiki/転送速度 "wikilink")を持つ。これは従来の32ビット/33 MHzのPCIバスに比して3倍から4倍に迫り、AGP_2xモードのそれに近い。高度な3D描画処理を行わない[ビデオカード](../Page/ビデオカード.md "wikilink")ならばx1モードでも充分な転送速度を確保できる。またレーンを複数束ね、さらに低[レイテンシ](../Page/レイテンシ.md "wikilink")、高転送速度を可能とするx2、x4、x8、x16、x32も仕様化されている。特にPCI Express x16は、バススロットに用いるコネクタの物理的長さが従来の[AGPやPCIに近く](../Page/Accelerated_Graphics_Port.md "wikilink")、AGPに代わるビデオカードのインタフェースとして利用されている。転送速度は8 [GB/s](https://ja.wikipedia.org/wiki/ビット毎秒#バイト毎秒 "wikilink")（2.5 Gbps時、送受信それぞれ4 GB/s）で、AGP_8xモード比でおよそ4倍弱となる。

PCI Express x1をベースとした新たな[PCカード](../Page/PCカード.md "wikilink")規格[ExpressCard](../Page/ExpressCard.md "wikilink")は[ノートパソコン](../Page/ノートパソコン.md "wikilink")などに採用される。ノートパソコンなどで内蔵の無線LANボード用に多く採用されるmini PCI Express端子はPCI Express (x1) とUSB2.0の信号配線がある。mSATA端子と端子形状は同一だが信号線の互換性はない。

## リビジョンと転送速度

### PCI Express 1.1 (Gen1)

規格1.1は先行して1.0と1.0aがある。

伝送路1[レーン](https://ja.wikipedia.org/wiki/レーン "wikilink")あたりの物理レイヤの帯域は片方向2.5 Gbpsで双方向で5.0 Gbpsだが、実効データ8ビットの送信に物理レイヤ上で2ビットの同期制御ビットを加える[8b/10b](https://ja.wikipedia.org/wiki/8b/10b "wikilink")エンコード方式を用いており、実効データ転送速度は片方向250 MB/sで双方向500 MB/sになる。ポートは1レーン、2レーン、4レーン、8レーン、12レーン、16レーン、32レーンなどをそれぞれx1、x2、x4、x8、x12、x16、x32と表す。伝送路のレーンを束ねることでポートのデータ転送速度向上が可能である。レーンを16束ねたPCI-E 1.1 x16の通信ポートの実効データ転送速度は、片方向4 GB/s、双方向では8 GB/sになる。

### PCI Express 2.0 (Gen2)

[2007年](../Page/2007年.md "wikilink")1月15日にPCI-SIGが発表した。

速度をPCI Express 1.1の2倍に引き上げ、1レーンあたりの物理帯域は片方向5.0 Gbpsで実効データ転送速度は片方向500 MB/sで双方向1 GB/sである。

[インテル](https://ja.wikipedia.org/wiki/インテル "wikilink")のコンシューマ向けプラットフォームでは2007年発売のX38チップセット\[1\]と翌2008年の4シリーズチップセット\[2\]にて、[AMD](https://ja.wikipedia.org/wiki/AMD "wikilink")においては2008年発売の700シリーズチップセット\[3\]にて対応。

### PCI Express 3.0 (Gen3)

[2010年](https://ja.wikipedia.org/wiki/2010年 "wikilink")11月18日にPCI-SIGが制定した。

当初は1レーンあたりの物理帯域10 Gbpsを目標としたが技術的困難から8 Gbpsに改め、エンコード方式を128b/130bに変更して転送効率を向上させた\[4\]。PCI Express 3.0は従来の1.1や2.0の機器とも接続互換性を有する。実効データ転送速度は当初目標のPCI Express 2.0比約2倍となり、1レーンあたりの実効データ転送速度は片方向0.9846 GB/sで双方向1.969 GB/sとなった。PCI Express 3.0のポートは規格上最大32レーンまで束ねられ、1ポートの最大の実効データ転送レートは片方向31.51 GB/s、双方向63.02 GB/sである。PCI Express 3.0以降は[\#物理レイヤ](https://ja.wikipedia.org/wiki/#物理レイヤ "wikilink")の帯域を[ギガビット毎秒](../Page/ビット毎秒.md "wikilink") (Gbps) でなくギガトランスファ毎秒 (GT/s) で表記することが多くなった。

インテルは2012年発売の[Ivy Bridge世代のCPUで正式対応](https://ja.wikipedia.org/wiki/Ivy_Bridgeマイクロアーキテクチャ "wikilink")\[5\]。ただしCPUが提供するレーンに限られ、[チップセット](../Page/チップセット.md "wikilink")が提供するレーンが対応したのは2015年発売の[Skylakeに対応した](https://ja.wikipedia.org/wiki/Skylakeマイクロアーキテクチャ "wikilink")100シリーズからとなる。AMDは2014年のKaveri世代で対応\[6\]。ただしこれは[APUであり](https://ja.wikipedia.org/wiki/AMD_Accelerated_Processing_Unit "wikilink")、より高性能なCPUでは2017年の[Ryzen](https://ja.wikipedia.org/wiki/Ryzen "wikilink")にて対応\[7\]。チップセットが提供するレーンは2020年発売のミドルレンジ向けチップセットであるB550が対応。

### PCI Express 4.0 (Gen4)

2017年10月に策定、公開\[8\]。

1レーンあたりの物理帯域をPCI Express 3.0 (Gen3) の2倍に引き上げて片方向16 GT/sとする。

単純に高速化しただけではバスを活かしきれない可能性があったため、パケットヘッダのタグが256個から768個へ拡張され、それらを効率的に扱うためのクレジットのスケーリング機能 (クレジットを1倍/4倍/16倍として扱う機能) が追加された。

AMDは2019年発売の[Zen 2世代のCPUで対応](../Page/Zen_2.md "wikilink")\[9\]。同時発表されたハイエンド向けのX570チップセットもそれまでの2.0から3.0をスキップして4.0に対応している。Intelは2020年発売の[Comet Lake世代までは対応していないものの](https://ja.wikipedia.org/wiki/Comet_Lake "wikilink")、同時に発売された[LGA1200](../Page/LGA1200.md "wikilink")ソケットのマザーボードの一部が独自に対応しており\[10\]\[11\]、次世代CPUにて対応すると予想されている。

### PCI Express 5.0 (Gen5)

2017年6月7日にPCI-SIGが発表。2019年5月29日の策定完了を発表\[12\]\[13\]。

PCI Express 3.0 (Gen3) の4倍、PCI Express 4.0 (Gen4) の2倍の速度である片方向32 GT/sを実現する\[14\]。

バスの速度は通常2.5 GT/s、8 GT/s、16 GT/s、32 GT/sの順に引き上げられていくが、切り替え毎に100 ms(32 GT/sに達するまで計300 ms)を要するため中間速度をバイパスして2.5 GT/sから32 GT/sへ直接切り替える (100 msに短縮される) 機能が追加された。この場合、中間速度は使用されず2.5 GT/s、5 GT/s、32 GT/sのみの動作となる。

### PCI Express 6.0 (Gen6)

2019年6月18日にPCI-SIGが発表\[15\]。規格策定は2021年の予定。

PCI Express 4.0 (Gen4) の4倍、PCI Express 5.0 (Gen5) の2倍の速度である片方向64 GT/sを実現する\[16\]。

エンコード方式は従来のNRZ 128b/130bからPAM-4 128b/130bに変更され、PCI Express 5.0 (Gen5) と同じバスクロックのまま転送速度が2倍になる。配線可能な距離はPCI Express 5.0 (Gen5) と同程度となる。

|           | リンク幅 x1      | x2          | x4          | x8          | x12         | x16         | x32         | x64         |
| --------- | ------------ | ----------- | ----------- | ----------- | ----------- | ----------- | ----------- | ----------- |
| Gen1      | 0.5/0.25     | 1.0/0.5     | 2.0/1.0     | 4.0/2.0     | 6.0/3.0     | 8.0/4.0     | 16.0/8.0    | 規格になし       |
| Gen2      | 1.0/0.5      | 2.0/1.0     | 4.0/2.0     | 8.0/4.0     | 12.0/6.0    | 16.0/8.0    | 32.0/16.0   | 規格になし       |
| Gen3      | 1.969/0.9846 | 3.938/1.969 | 7.877/3.938 | 15.75/7.877 | 23.63/11.82 | 31.51/15.75 | 63.02/31.51 | 規格になし       |
| Gen4      | 3.938/1.969  | 7.877/3.938 | 15.75/7.877 | 31.51/15.75 | 47.26/23.63 | 63.02/31.51 | 126.0/63.02 | 252.1/126.0 |
| Gen5      | 7.877/3.938  | 15.75/7.877 | 31.51/15.75 | 63.02/31.51 | 94.52/47.26 | 126.0/63.02 | 252.1/126.0 | 504.1/252.1 |
| Gen6 (予定) | 15.75/7.877  | 31.51/15.75 | 63.02/31.51 | 126.0/63.02 | 189.0/94.52 | 252.1/126.0 | 504.1/252.1 | 1008/504.2  |

リンク幅毎のデータリンク層転送帯域 (双方向/一方向あたり) (GB/s)

|           | リンク幅 x1 | x2      | x4      | x8       | x12      | x16       | x32       | x64       |
| --------- | ------- | ------- | ------- | -------- | -------- | --------- | --------- | --------- |
| Gen1      | 5.0/2.5 | 10/5.0  | 20/10   | 40/20    | 60/30    | 80/40     | 160/80    | 規格になし     |
| Gen2      | 10/5    | 20/10   | 40/20   | 80/40    | 120/60   | 160/80    | 320/160   | 規格になし     |
| Gen3      | 16/8    | 32/16   | 64/32   | 128/64   | 192/96   | 256/128   | 512/256   | 規格になし     |
| Gen4      | 32/16   | 64/32   | 128/64  | 256/128  | 384/192  | 512/256   | 1024/512  | 2048/1024 |
| Gen5      | 64/32   | 128/64  | 256/128 | 512/256  | 768/384  | 1024/512  | 2048/1024 | 4096/2048 |
| Gen6 (予定) | 128/64  | 256/128 | 512/256 | 1024/512 | 1536/768 | 2048/1024 | 4096/2048 | 8192/4096 |

リンク幅毎の物理層転送帯域 (双方向/一方向あたり) (GT/s)

## 開発から普及までの経緯

### パラレル・インタフェースの問題点

PCIバスなどのパラレルインタフェースでデータ転送速度の向上は、

1.  バス幅を拡幅してデータ線を増加
2.  単位時間あたりの転送回数を増加を企図して高クロック化

が奏功する。PCIバスは当初の32ビット/33 MHz (133 MB/s) から64ビット/66 MHz (533 MB/s) までデータ転送速度が引き上げられた。PCI-Xバスは、バスクロックのDDR/QDR化も含め64ビット/1066 MHz相当まで仕様化されている。

上記手法の高速化は限界がある。バス幅の拡大はデータ線の増加、[LSIのピン増加](../Page/集積回路.md "wikilink")、として製造コスト上昇の要因となる。クロックの高速化はデータとクロックタイミングを一致させるため、LSIとボードの設計と製造に高度技術が求められてコストが増加する。PCI-Xは厳密な設計が要求されるため民生品の商品化は価格面で困難で、パーソナルコンピュータまで普及しなかった。

かつては製造コストに比して性能が上昇したが、高速化の限界を迎えてインテルはメインメモリインターフェイスのシリアル化を提唱した。

### PCIバスの限界

PCIバス登場当初から一貫してパーソナルコンピュータ市場で広く普及しているPCIバスのモードは、32ビット/33 MHzだった。バス伝送帯域は主に3Dグラフィックスカードが消費していたがAGPによって事実上隔離されており、PCIバスは安泰であった。[チップセット](../Page/チップセット.md "wikilink")内部ないしはブリッジチップでPCIバスに接続されるハードディスクのインタフェースの[IDEは](../Page/Advanced_Technology_Attachment.md "wikilink")、サポートする転送速度を次第に引き上げて[2000年](../Page/2000年.md "wikilink")に66 MB/s、[2002年](../Page/2002年.md "wikilink")に100 MB/sの転送速度をサポートした。ハードディスクの転送速度は追いついていなかったが、民生品市場で[RAID](../Page/RAID.md "wikilink")が流行し、高性能なビデオ編集用カードの普及し、PCIバスに接続される[ギガビットLANの](https://ja.wikipedia.org/wiki/イーサネット#ギガビット・イーサネット "wikilink")[1000BASE-Tが発売され](https://ja.wikipedia.org/wiki/イーサネット#1000BASE-T "wikilink")、ユーザは転送速度向上を望むようになった。

### シリアル・インタフェースの台頭

1本の信号線と付随して基準線とするアース線でデータ伝送を行うシリアルインタフェースは[RS-232](../Page/RS-232.md "wikilink")Cが知られる。[パリティビット](../Page/パリティビット.md "wikilink")による簡易な[誤り検出訂正](../Page/誤り検出訂正.md "wikilink")しか物理層に組み込めず、誤り訂正が増加する高速データ転送に不向きとされていた。

パラレルデータにクロックを埋め込みシリアル・データ化する[8b/10b](https://ja.wikipedia.org/wiki/8b/10b "wikilink")技術を[IBM](../Page/IBM.md "wikilink")が開発し、シリアル転送が再び着目された。[イーサネット](../Page/イーサネット.md "wikilink")で採用されて普及が広まると8b/10b機能を搭載した[SERDESチップの価格が低下し](https://ja.wikipedia.org/wiki/SerDes "wikilink")、[ファイバーチャネル](../Page/ファイバーチャネル.md "wikilink")やギガビットイーサネット (GbE) で転送速度も高速化された。

### PCI Expressの登場

I/Oインタフェースの転送速度不足解消のために次世代インタフェースを模索していたインテルは、シリアルインタフェースであるNGIO (*Next Generation I/O*) の開発を開始し、[ヒューレット・パッカード](../Page/ヒューレット・パッカード.md "wikilink")やIBMも、PCIバスに代わるI/OインタフェースとしてFuture I/Oと呼ばれるシリアル・インタフェースを開発していた。

両者は後に統合されて[InfiniBand](../Page/InfiniBand.md "wikilink")となったが[ソフトウェア](../Page/ソフトウェア.md "wikilink")レベルでPCIバスと[互換性](../Page/互換性.md "wikilink")を有さず、[マイクロソフト](../Page/マイクロソフト.md "wikilink")などもサポートに消極的で、スーパーコンピュータのノード間接続など低遅延で高[スループット](../Page/スループット.md "wikilink")な要求分野で利用される。

インテルはこの失敗を教訓として3GIO (*Third Generation I/O*) の開発を開始した。ソフトウェア・レベルでPCIバス完全互換とし、正統なPCIバスの後継者とすべく**PCI Express**としてPCI-SIGでの仕様化が行われた。

### ソフトウェアの対応

PCI Expressは従来のPCIバスが作動する[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink") (OS) で新たなサポートなく作動する。Windowsは[Vistaで正式に対応した](https://ja.wikipedia.org/wiki/Microsoft_Windows_Vista "wikilink")。

### 普及

[thumb](https://ja.wikipedia.org/wiki/ファイル:Gigabyte_GV-NX62TC256D8_Rev_1.0.jpg "wikilink") パーソナルコンピュータ向けマザーボードへの実装は比較的早くに行われた。主に搭載されるのはx16とx1である。転送速度が何よりも要求される3Dグラフィックスカードでは特に歓迎され、[2005年](../Page/2005年.md "wikilink")頃にAGPからの置き換えがほぼ完了し、2016年 現在では3Dグラフィックスカードのシェアの大半を獲得するまでに成長している。かつて主力であったAGP用のグラフィックスカードは、2019年現在では新品で販売される事は皆無である。

マザーボード市場でAGPスロットを有する製品は、2019年現在組み込み向けなどの特殊な用途を除けばほとんど存在しない。汎用バスとしてのPCIスロットも、一般用途のマザーボードにおいては2019年現在では全廃したマザーボードが多数を占め、搭載しているマザーボードは少数である。[サーバ](../Page/サーバ.md "wikilink")向けマザーボードは依然として64ビットPCIやPCI-Xを実装したものも多い。

ATAカードをはじめとしたインタフェースカード類は比較的早くから PCI Express (x1) に移行しており、ビデオキャプチャ、テレビチューナ、サウンドカードなどマルチメディア関連商品はPCI Express対応が多い。旧来システムのアップグレードパスとしてモデルチェンジを行わず販売を継続しているPCI製品もある。2016年現在でATXマザーボードの拡張スロットはPCI Express x16、x1、PCIの3種類を採用したものが多く、PCIの需要よりチップセット側のPCI Expressの総帯域制限によるものが多い。 オンボードデバイスは、従来PCIバスを用いて接続していた物を完全にPCI Express接続に置き換えたマザーボードが大半である。IntelはP67以降のメインストリーム向けチップセットからPCIをサポートしておらず、別途ブリッジチップを用いてPCI Express経由で接続している。2012年後半からPCI Express 3.0仕様に対応したマザーボードやビデオカードが発売された。

## 仕様

データ転送方式はPCIバスのハンドシェークと異なり、ネットワークでパケット送受信される。アーキテクチャはレイヤ構造を有し、トランザクション・レイヤ、データリンク・レイヤ、物理レイヤの3層構造となっている。

送信では、CPUや他デバイスから発行されたリクエストは、トランザクション・レイヤで上位のソフトウェア層に対してPCIと互換性のある機能を提供するパケットを付加され、データリンク・レイヤに渡される。データリンク・レイヤーは、接続されている相手側デバイス間との送受信の制御を担っており、パケットにシーケンス番号、[CRCを付加して物理レイヤに渡す](../Page/巡回冗長検査.md "wikilink")。物理レイヤはシリアル転送を受け持つ部分で、Gen1, 2では8b/10b変換、Gen3では128b/130b変換などを行い、[SERDESによりパケットがシリアル](https://ja.wikipedia.org/wiki/SerDes "wikilink")・データとして送られる。

また、[トポロジは](../Page/位相幾何学.md "wikilink")、従来のPCIのマルチ・ドロップ型ではなく、[ポイント・ツー・ポイント](https://ja.wikipedia.org/wiki/ポイント・ツー・ポイント "wikilink")接続である。ポートの拡張はスイッチを必要とする。

### トランザクション・レイヤ

トランザクション・レイヤは主にトランザクション・レイヤ・パケット (*Transaction Layer Packet* : TLP) の生成と復号を担う。TLPはリードやライトといったコマンドやアドレス、データなどから構成される。トランザクション・レイヤは接続相手とのフロー制御も行う。PCI Expressの[フロー制御](https://ja.wikipedia.org/wiki/フロー制御 "wikilink")はクレジット・ベースで行われ、予め自分が受信することの出来る[バッファ](../Page/バッファ.md "wikilink")のサイズを相手に通知し、バッファに空きが出来るたびに伝える方式である。送信側は自身が送信したパケットのサイズを積算し、送信相手からバッファの空きが伝えられるとその分を減算することで、送信相手のバッファ・サイズを超えることなくパケットの転送が可能となる。

トランザクション・レイヤはパケットを任意のサイズに分割する機能を有する。一つのTLPで最大4[キロバイト](../Page/キロバイト.md "wikilink")のメモリ・リードを発行することが可能であるが、メモリから4キロバイトを一度で読むことは都合が悪い場合がある。メモリ・リードで[キャッシュ・コヒーレンシを維持するシステムの場合](https://ja.wikipedia.org/wiki/キャッシュメモリ#キャッシュコヒーレンシ_\(Cache_Coherency\) "wikilink")、CPUに対しキャッシュに最新データの有無を問い合わせる。インテル系の32ビットCPUはキャッシュ・ライン・サイズは64バイトで、4キロバイトのメモリ・リードは全て64バイトの64個のメモリ・リードに分割される必要がある。トランザクション・レイヤは自デバイス内で、都合良くパケットを分割する。1つのRead requestのデータを返す時に複数のcompletionに分割して返すこともできるが、返すデータの順序は入れ換えられない。

トランザクション・レイヤは以下の4個のアドレス空間をサポートする。

1.  Memory 空間
2.  I/O 空間
3.  Configuration 空間
4.  Message 空間

前者3空間はPCIバス互換の空間である。Message空間は、従来サイドバンド信号で通知を行っていたもので、割り込み、電源制御などの通知に使用される。

### データリンク・レイヤ

データリンク・レイヤは、トランザクション・レイヤと物理レイヤの中間に位置し、主にPCI Expressリンクの管理、エラー検出と訂正を担う。

送信側データリンク・レイヤは、トランザクション・レイヤから渡されたTLPをバイナリ値としてデータを保護するためのCRCを算出し、TLPの授受を確認するためのシーケンス・ナンバをTLPに付加して物理レイヤに渡す。受信側はCRCによるデータ化けチェックと、シーケンス・ナンバによるパケット欠落チェックを行う。

受信側でエラーを見つけた場合、送信側に再送を促すためにNAK (*Not Acknowledge*) パケットをエラー検出したTLPのシーケンス・ナンバと共に送信側に返す。正常にTLPを受信した場合は、同様にACK (*Acknowledge*) パケットを返す。

エラーによるパケットの再送機能もデータリンク・レイヤが受け持っており、NAKを受信した場合そのシーケンス・ナンバから全て送信し直すため、データリンク・レイヤ内に再送バッファが実装される。

データリンク・レイヤは、TLPの送受信の他にもDLLP (*Data Link Layer Packet*) と呼ばれるデータリンク・レイヤ同士でのみ情報を交換するパケットも送受信する。ACK、NACKパケットや、フロー制御に使用するバッファ・サイズ通知などもDLLPが使用される。

### 物理レイヤ

物理レイヤは入出力バッファの制御回路、シリアル-パラレル/パラレル-シリアル変換回路、[PLL](../Page/位相同期回路.md "wikilink")、[インピーダンス](../Page/インピーダンス.md "wikilink")調整回路などで構成される。

PCI Express 1.1の物理メディアは2線、800 mV[差動で](../Page/平衡接続.md "wikilink")400 ps単位でデータのドライブされる。送信、受信専用の信号を必要とする全二重方式で、x1の場合に実際は4本の信号が使用される。

PCI Express 1.1までは2.5GT/sでデータ転送しているが、PCI Express 2.0は5.0GT/sで転送している。PCI Expressをケーブルで接続するための仕様検討も行われている。

物理レイヤは将来的により高速なメディアに置き換えられることから、物理レイヤとデータリンクレイヤ間のインタフェースは特に規定されておらず各ベンダの実装に依存している。

### 物理形状

*PCI Express Card Electromechanical Specification*として拡張カードの電気および物理形状が規定され、カードエッジを含むコネクタの仕様も規定される。

#### ロープロファイルPCI Express

ロープロファイルPCI Expressは物理形状がPCI Expressより小さい。

### ピンアサイン

下記の表に PCI Express カードに設けられた[エッジ・コネクタ](https://ja.wikipedia.org/wiki/エッジ・コネクタ "wikilink")における接点（ピン）とその役割を示す。[プリント基板](../Page/プリント基板.md "wikilink") のうちはんだ面を A サイド、部品面を B サイドと表記する。\[17\] PRSNT1\# 及び PRSNT2\# ピンは他のピンに比べて若干短く、[ホットスワップ](../Page/ホットスワップ.md "wikilink") による装着を行う際他のピンに遅れて最後に接触することが意図されている。WAKE\# ピンの駆動はホストコンピュータをローパワー状態から復帰させる（Wake Up）が、Wake Up 可能であることを示すため、当ピンは予めスタンバイ電源によりプルアップしておく必要がある。\[18\] {{-}}

<table>
<caption>PCI express のエッジコネクタ　ピンアサイン (x1, x4, x8 および x16)</caption>
<thead>
<tr class="header">
<th><p>ピン</p></th>
<th><p>Bサイド</p></th>
<th><p>Aサイド</p></th>
<th><p>詳細</p></th>
<th></th>
<th><p>ピン</p></th>
<th><p>Bサイド</p></th>
<th><p>Aサイド</p></th>
<th><p>詳細</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>1</p></td>
<td><p>+12 V</p></td>
<td><p>PRSNT1#</p></td>
<td><p>最も離れた PRSNT2# ピンとカード上で接続される</p></td>
<td><p>50</p></td>
<td><p>HSOp(8)</p></td>
<td><p>Reserved</p></td>
<td><p>レーン 8 送信データ, + 及び −</p></td>
<td></td>
</tr>
<tr class="even">
<td><p>2</p></td>
<td><p>+12 V</p></td>
<td><p>+12 V</p></td>
<td><p>メイン電源ピン</p></td>
<td><p>51</p></td>
<td><p>HSOn(8)</p></td>
<td><p>Ground</p></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>3</p></td>
<td><p>+12 V</p></td>
<td><p>+12 V</p></td>
<td><p>52</p></td>
<td><p>Ground</p></td>
<td><p>HSIp(8)</p></td>
<td><p>レーン 8 受信データ, + 及び −</p></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>4</p></td>
<td><p>Ground</p></td>
<td><p>Ground</p></td>
<td></td>
<td><p>53</p></td>
<td><p>Ground</p></td>
<td><p>HSIn(8)</p></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>5</p></td>
<td><p>SMCLK</p></td>
<td><p>TCK</p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/SMBus" title="wikilink">SMBus</a>と<a href="../Page/JTAG.md" title="wikilink">JTAG</a>のピン</p></td>
<td><p>54</p></td>
<td><p>HSOp(9)</p></td>
<td><p>Ground</p></td>
<td><p>レーン 9 送信データ, + 及び −</p></td>
<td></td>
</tr>
<tr class="even">
<td><p>6</p></td>
<td><p>SMDAT</p></td>
<td><p>TDI</p></td>
<td><p>55</p></td>
<td><p>HSOn(9)</p></td>
<td><p>Ground</p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>7</p></td>
<td><p>Ground</p></td>
<td><p>TDO</p></td>
<td><p>56</p></td>
<td><p>Ground</p></td>
<td><p>HSIp(9)</p></td>
<td><p>レーン 9 受信データ, + 及び −</p></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>8</p></td>
<td><p>+3.3 V</p></td>
<td><p>TMS</p></td>
<td><p>57</p></td>
<td><p>Ground</p></td>
<td><p>HSIn(9)</p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>9</p></td>
<td><p>TRST#</p></td>
<td><p>+3.3 V</p></td>
<td><p>58</p></td>
<td><p>HSOp(10)</p></td>
<td><p>Ground</p></td>
<td><p>レーン 10 送信データ, + 及び −</p></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>10</p></td>
<td><p>+3.3 V aux</p></td>
<td><p>+3.3 V</p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/スタンバイ" title="wikilink">スタンバイ</a> 電源</p></td>
<td><p>59</p></td>
<td><p>HSOn(10)</p></td>
<td><p>Ground</p></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>11</p></td>
<td><p>WAKE#</p></td>
<td><p>PERST#</p></td>
<td><p>（Bサイド）電源復帰、（Aサイド）リセット信号</p></td>
<td><p>60</p></td>
<td><p>Ground</p></td>
<td><p>HSIp(10)</p></td>
<td><p>レーン 10 受信データ, + 及び −</p></td>
<td></td>
</tr>
<tr class="even">
<td><p>ノッチ</p></td>
<td><p>61</p></td>
<td><p>Ground</p></td>
<td><p>HSIn(10)</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>12</p></td>
<td><p>CLKREQ#[19]</p></td>
<td><p>Ground</p></td>
<td><p>クロック要求信号</p></td>
<td><p>62</p></td>
<td><p>HSOp(11)</p></td>
<td><p>Ground</p></td>
<td><p>レーン 11 送信データ, + 及び −</p></td>
<td></td>
</tr>
<tr class="even">
<td><p>13</p></td>
<td><p>Ground</p></td>
<td><p>REFCLK+</p></td>
<td><p>基準クロック差動対</p></td>
<td><p>63</p></td>
<td><p>HSOn(11)</p></td>
<td><p>Ground</p></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>14</p></td>
<td><p>HSOp(0)</p></td>
<td><p>REFCLK−</p></td>
<td><p>レーン 0 送信データ, + 及び −</p></td>
<td><p>64</p></td>
<td><p>Ground</p></td>
<td><p>HSIp(11)</p></td>
<td><p>レーン 11 受信データ, + 及び −</p></td>
<td></td>
</tr>
<tr class="even">
<td><p>15</p></td>
<td><p>HSOn(0)</p></td>
<td><p>Ground</p></td>
<td><p>65</p></td>
<td><p>Ground</p></td>
<td><p>HSIn(11)</p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>16</p></td>
<td><p>Ground</p></td>
<td><p>HSIp(0)</p></td>
<td><p>レーン 0 受信データ, + 及び −</p></td>
<td><p>66</p></td>
<td><p>HSOp(12)</p></td>
<td><p>Ground</p></td>
<td><p>レーン 12 送信データ, + 及び −</p></td>
<td></td>
</tr>
<tr class="even">
<td><p>17</p></td>
<td><p>PRSNT2#</p></td>
<td><p>HSIn(0)</p></td>
<td><p>67</p></td>
<td><p>HSOn(12)</p></td>
<td><p>Ground</p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>18</p></td>
<td><p>Ground</p></td>
<td><p>Ground</p></td>
<td></td>
<td><p>68</p></td>
<td><p>Ground</p></td>
<td><p>HSIp(12)</p></td>
<td><p>レーン 12 受信データ, + 及び −</p></td>
<td></td>
</tr>
<tr class="even">
<td><p>PCI Express x1 カードは 18 番ピンまでを備える</p></td>
<td><p>69</p></td>
<td><p>Ground</p></td>
<td><p>HSIn(12)</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>19</p></td>
<td><p>HSOp(1)</p></td>
<td><p>Reserved</p></td>
<td><p>レーン 1 送信データ, + 及び −</p></td>
<td><p>70</p></td>
<td><p>HSOp(13)</p></td>
<td><p>Ground</p></td>
<td><p>レーン 13 送信データ, + 及び −</p></td>
<td></td>
</tr>
<tr class="even">
<td><p>20</p></td>
<td><p>HSOn(1)</p></td>
<td><p>Ground</p></td>
<td><p>71</p></td>
<td><p>HSOn(13)</p></td>
<td><p>Ground</p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>21</p></td>
<td><p>Ground</p></td>
<td><p>HSIp(1)</p></td>
<td><p>レーン 1 受信データ, + 及び −</p></td>
<td><p>72</p></td>
<td><p>Ground</p></td>
<td><p>HSIp(13)</p></td>
<td><p>レーン 13 受信データ, + 及び −</p></td>
<td></td>
</tr>
<tr class="even">
<td><p>22</p></td>
<td><p>Ground</p></td>
<td><p>HSIn(1)</p></td>
<td><p>73</p></td>
<td><p>Ground</p></td>
<td><p>HSIn(13)</p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>23</p></td>
<td><p>HSOp(2)</p></td>
<td><p>Ground</p></td>
<td><p>レーン 2 送信データ, + 及び −</p></td>
<td><p>74</p></td>
<td><p>HSOp(14)</p></td>
<td><p>Ground</p></td>
<td><p>レーン 14 送信データ, + 及び −</p></td>
<td></td>
</tr>
<tr class="even">
<td><p>24</p></td>
<td><p>HSOn(2)</p></td>
<td><p>Ground</p></td>
<td><p>75</p></td>
<td><p>HSOn(14)</p></td>
<td><p>Ground</p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>25</p></td>
<td><p>Ground</p></td>
<td><p>HSIp(2)</p></td>
<td><p>レーン 2 受信データ, + 及び −</p></td>
<td><p>76</p></td>
<td><p>Ground</p></td>
<td><p>HSIp(14)</p></td>
<td><p>レーン 14 受信データ, + 及び −</p></td>
<td></td>
</tr>
<tr class="even">
<td><p>26</p></td>
<td><p>Ground</p></td>
<td><p>HSIn(2)</p></td>
<td><p>77</p></td>
<td><p>Ground</p></td>
<td><p>HSIn(14)</p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>27</p></td>
<td><p>HSOp(3)</p></td>
<td><p>Ground</p></td>
<td><p>レーン 3 送信データ, + 及び −</p></td>
<td><p>78</p></td>
<td><p>HSOp(15)</p></td>
<td><p>Ground</p></td>
<td><p>レーン 15 送信データ, + 及び −</p></td>
<td></td>
</tr>
<tr class="even">
<td><p>28</p></td>
<td><p>HSOn(3)</p></td>
<td><p>Ground</p></td>
<td><p>79</p></td>
<td><p>HSOn(15)</p></td>
<td><p>Ground</p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>29</p></td>
<td><p>Ground</p></td>
<td><p>HSIp(3)</p></td>
<td><p>レーン 3 受信データ, + 及び −</p></td>
<td><p>80</p></td>
<td><p>Ground</p></td>
<td><p>HSIp(15)</p></td>
<td><p>レーン 15 受信データ, + 及び −</p></td>
<td></td>
</tr>
<tr class="even">
<td><p>30</p></td>
<td><p>PWRBRK#[20]</p></td>
<td><p>HSIn(3)</p></td>
<td><p>81</p></td>
<td><p>PRSNT2#</p></td>
<td><p>HSIn(15)</p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>31</p></td>
<td><p>PRSNT2#</p></td>
<td><p>Ground</p></td>
<td></td>
<td><p>82</p></td>
<td><p>Reserved</p></td>
<td><p>Ground</p></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>32</p></td>
<td><p>Ground</p></td>
<td><p>Reserved</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>PCI Express x4 カードは 32 番ピンまでを備える</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>33</p></td>
<td><p>HSOp(4)</p></td>
<td><p>Reserved</p></td>
<td><p>レーン 4 送信データ, + 及び −</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>34</p></td>
<td><p>HSOn(4)</p></td>
<td><p>Ground</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>35</p></td>
<td><p>Ground</p></td>
<td><p>HSIp(4)</p></td>
<td><p>レーン 4 受信データ, + 及び −</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>36</p></td>
<td><p>Ground</p></td>
<td><p>HSIn(4)</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>37</p></td>
<td><p>HSOp(5)</p></td>
<td><p>Ground</p></td>
<td><p>レーン 5 送信データ, + 及び −</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>38</p></td>
<td><p>HSOn(5)</p></td>
<td><p>Ground</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>39</p></td>
<td><p>Ground</p></td>
<td><p>HSIp(5)</p></td>
<td><p>レーン 5 受信データ, + 及び −</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>40</p></td>
<td><p>Ground</p></td>
<td><p>HSIn(5)</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>41</p></td>
<td><p>HSOp(6)</p></td>
<td><p>Ground</p></td>
<td><p>レーン 6 送信データ, + 及び −</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>42</p></td>
<td><p>HSOn(6)</p></td>
<td><p>Ground</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>43</p></td>
<td><p>Ground</p></td>
<td><p>HSIp(6)</p></td>
<td><p>レーン 6 受信データ, + 及び −</p></td>
<td><p>凡例</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>44</p></td>
<td><p>Ground</p></td>
<td><p>HSIn(6)</p></td>
<td><p>グランドピン</p></td>
<td><p>0 V基準</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>45</p></td>
<td><p>HSOp(7)</p></td>
<td><p>Ground</p></td>
<td><p>レーン 7 送信データ, + 及び −</p></td>
<td><p>電源ピン</p></td>
<td><p>PCIeカードに電力を供給する</p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>46</p></td>
<td><p>HSOn(7)</p></td>
<td><p>Ground</p></td>
<td><p>Card-to-host ピン</p></td>
<td><p>カードからマザーボードへの信号</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>47</p></td>
<td><p>Ground</p></td>
<td><p>HSIp(7)</p></td>
<td><p>レーン 7 受信データ, + 及び −</p></td>
<td><p>Host-to-card ピン</p></td>
<td><p>マザーボードからカードへの信号</p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>48</p></td>
<td><p>PRSNT2#</p></td>
<td><p>HSIn(7)</p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/オープンドレイン" title="wikilink">オープンドレイン</a></p></td>
<td><p>複数のカードによってプルダウンされ、かつ（または）感知される</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>49</p></td>
<td><p>Ground</p></td>
<td><p>Ground</p></td>
<td></td>
<td><p>センスピン</p></td>
<td><p>カード上で相互接続される</p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>PCI Express x8 カードは 49 番ピンまでを備える</p></td>
<td><p>予約</p></td>
<td><p>現在使用されておらず、接続してはならない</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
</tbody>
</table>

| pin            | TOPサイド         | pin | Bottomサイド      |
| -------------- | -------------- | --- | -------------- |
| 1              | \-             | 2   | 3.3 V          |
| 3              | Reserved (\*4) | 4   | GND            |
| 5              | Reserved (\*4) | 6   | 1.5 V          |
| 7              | CLKREQ\#       | 8   | VCC (\*2)      |
| 9              | GND            | 10  | I/O (\*2)      |
| 11             | REFCLK-        | 12  | CLK (\*2)      |
| 13             | REFCLK+        | 14  | RST (\*2)      |
| 15             | N/C or GND     | 16  | VPP (\*2)      |
| Mechanical key |                |     |                |
| 17             | Reserved       | 18  | GND            |
| 19             | Reserved       | 20  | Reserved (\*3) |
| 21             | GND            | 22  | PERST\#        |
| 23             | PERn0          | 24  | \+3.3Vaux      |
| 25             | PERp0          | 26  | GND            |
| 27             | GND            | 28  | \+1.5 V        |
| 29             | GND            | 30  | SMB_CLK       |
| 31             | PETn0          | 32  | SMB_DATA      |
| 33             | PETp0          | 34  | GND            |
| 35             | GND            | 36  | USB_D-        |
| 37             | Reserved (\*1) | 38  | USB_D+        |
| 39             | Reserved (\*1) | 40  | GND            |
| 41             | Reserved (\*1) | 42  | LED_WWAN\#    |
| 43             | Reserved (\*1) | 44  | LED_WLAN\#    |
| 45             | Reserved (\*1) | 46  | LED_WPAN\#    |
| 47             | Reserved (\*1) | 48  | \+1.5 V        |
| 49             | Reserved (\*1) | 50  | GND            |
| 51             | Reserved (\*1) | 52  | \+3.3 V        |

miniPCI express のピンアサイン

1.  Reserved for future second PCI Express Lane (if needed)
2.  Reserved for future Subscriber Identity Module (SIM) interface (if needed)
3.  Reserved for future wireless disable signal (if needed)
4.  Reserved for future wireless coexistence control interface (if needed)

### 電力供給

[PCI-E_6pin_8pin.jpg](https://ja.wikipedia.org/wiki/File:PCI-E_6pin_8pin.jpg "fig:PCI-E_6pin_8pin.jpg")

| スロット形状   | x1                     | x4/x8 | x16                  |
| -------- | ---------------------- | ----- | -------------------- |
| フルハイト    | 10 W/25 W (High Power) | 25 W  | 25 W/75 W（グラフィックカード） |
| ロープロファイル | 10 W                   | 25 W  | 25 W                 |

スロットからの最大供給電力\[21\]

スロットからの最大供給電力を超えるカードについては、下記のとおり[ATX12V Ver2.xの補助電源プラグ経由で超過分を供給する](https://ja.wikipedia.org/wiki/ATX電源#ATX電源の種類 "wikilink")。

  - 6ピン1本：最大75 W、スロットからの供給と併せて最大150 W\[22\]
  - 6ピン2本：最大150 W、スロットからの供給と併せて最大225 W\[23\]
  - 6ピン1本、8ピン1本：最大225 W、スロットからの供給と併せて最大300 W\[24\]

## 欠点

### 相互接続性の問題

[PCIe_J1900_SoC_ITX_Mainboard_IMG_1820.JPG](https://ja.wikipedia.org/wiki/File:PCIe_J1900_SoC_ITX_Mainboard_IMG_1820.JPG "fig:PCIe_J1900_SoC_ITX_Mainboard_IMG_1820.JPG") PCIバスは32ビットバスのデバイス/スロットと64ビットバスのデバイス/スロットの全ての組み合わせで動作が保証されていたが、PCI Expressはx16仕様のカードをx8仕様のスロットに挿入できない。マザーボードにはx1/x4/x8コネクタのエッジに初めから切り欠きが設け、x16仕様カードを挿入可能な「エッジフリー」と称する製品もあるが、カード端子の物理的保護などの問題点は解消されないマザーボードIntel DX58S0がある。解決事例に、[アップルの](../Page/アップル_\(企業\).md "wikilink")[Mac Proや](../Page/Mac_Pro.md "wikilink")[Intel 3シリーズ以降](https://ja.wikipedia.org/wiki/インテル_チップセット#Intel_3_Series "wikilink")、[AMD 7シリーズのマルチGPU対応チップセット搭載マザーボードが採用した実装などがある](https://ja.wikipedia.org/wiki/アドバンスト・マイクロ・デバイセズ#チップセット "wikilink")。後述の[利点を参照](https://ja.wikipedia.org/wiki/#利点 "wikilink")。

## 利点

PCI Expressの利点の一つとしてレーン数のフレキシビリティが挙げられる。カードエッジコネクタがx16形状でもx1モードで規格上は動作可能で、上位の長いスロットに下位の短いカードエッジコネクタは挿入可能である。BIOS上もしくはOS上から、チップセットのサポートレーン数を上限としてユーザーが任意に設定する設計も可能である。

合計レーン数の上限を26として４つのx16用物理スロットに対し

  - x8 x1 x1 x16（余り0）
  - x4 x4 x1 x16（余り1）
  - x8 x1 x8 x8（余り1）
  - x4 x4 x8 x8（余り2）

と複数の振り分け選択も可能である。余剰レーンの未使用による不利益は無い。x16モードで動作するスロットにx1専用カードを挿入しても問題なく動作する。

スロット[コネクタ](../Page/コネクタ.md "wikilink")の物理規格は、スロットに割り振り可能な規格上のレーン数上限を示す。マザーボード設計者は、使用するチップセットのサポートレーン数の範囲内で、スロット本数と与えるレーン数の設計が可能である。

## 脚注

### 注釈

### 出典

## 参考となる図書

  - Adam H. Wilen, Justin P. Schade and Ron Thornburg:"Introduction to Pci Express: A Hardware and Software Developer's Guide", Intel Press, ISBN 978-0970284693 (2003年4月）.
  - Mindshare Inc., Ravi Budruk, Don Anderson and Tom Shanley: "PCI Express System Architecture", Addison-Wesley Professional, ISBN 978-0321156303 (2003年9月).
  - 荒井 信隆, 里見 尚志, 田中 顕裕：「PCI Express入門講座―高速シリアルインタフェースの基礎知識と実際」（改訂新版）、電波新聞社、ISBN 978-4885549632（2008年6月）.
  - 畑山仁（他）：「PCI Express設計の基礎と応用―プロトコルの基本から基板設計、機能実装まで」、 CQ出版 (インターフェース・デザイン・シリーズ)、ISBN 978-4789846417（2010年5月）.
  - 内藤竜治：「FPGAでゼロから作るPCI Express―PC拡張用の定番バスはこうやって動かす」、 CQ出版 (TECH I―BUS Interface)、ISBN 978-4789849821（2013年4月）.
  - Mike Jackson and Ravi Budruk: "PCI Express Technology 3.0", MindShare Press, ISBN 978-0977087860 (2012年10月）.

## 関連項目

  - [Accelerated Graphics Port](../Page/Accelerated_Graphics_Port.md "wikilink") (AGP)
  - [Peripheral Component Interconnect](../Page/Peripheral_Component_Interconnect.md "wikilink") (PCI)
  - [HyperTransport](../Page/HyperTransport.md "wikilink")
  - [Thunderbolt](https://ja.wikipedia.org/wiki/Thunderbolt "wikilink")
  - [NVM Express](https://ja.wikipedia.org/wiki/NVM_Express "wikilink") (NVMe)
  - [NVLink](https://ja.wikipedia.org/wiki/NVLink "wikilink")

## 外部リンク

  - [PCI Special Interest Group](http://www.pcisig.com/home)

  - [PCI Special Interest Group - PCI Express](http://www.pcisig.com/specifications/pciexpress/)

  -
[Category:PCI_Express](https://ja.wikipedia.org/wiki/Category:PCI_Express "wikilink")

1.
2.
3.
4.  [PCI-SIG、PCI Express base specification 3.0完成をアナウンス](https://news.mynavi.jp/news/2010/11/22/041/)
5.
6.
7.
8.
9.
10.
11.
12.
13.
14.
15.
16.
17.
18.
19.
20.
21. PCI Express Card Electromechanical Specification 1.1
22. PCI Express x16 Graphics 150W-ATX Specification Revision 1.0（2004年10月25日）
23. PCI Express 225/300 Watt High Power CEM Spec 1.0（2008年3月27日）
24. PCI Express 225/300 Watt High Power CEM Spec 1.0（2008年3月27日）
> この記事は[InfiniBand](https://ja.wikipedia.org/wiki/InfiniBand)から翻訳されています。


[frame](https://ja.wikipedia.org/wiki/ファイル:Infinibandport.jpg "wikilink")

**InfiniBand**（インフィニバンド）とは、非常に高いRAS（信頼性・可用性・保守性）を持つ基幹系・[HPC系の](../Page/スーパーコンピュータ.md "wikilink")[サーバ](../Page/サーバ.md "wikilink")/[クラスター用高速](../Page/コンピュータ・クラスター.md "wikilink")[I/O](../Page/入出力.md "wikilink")[バス](../Page/バス_\(コンピュータ\).md "wikilink")[アーキテクチャ及びインターコネクトのこと](../Page/コンピュータ・アーキテクチャ.md "wikilink")。システム間インターコネクト機構としては、RAS機能の他、他機構に比較して、低[レイテンシ](../Page/レイテンシ.md "wikilink")である点も特徴である。

## 概要

InfiniBandは、[ファイバーチャネル](../Page/ファイバーチャネル.md "wikilink")、[PCI Express](../Page/PCI_Express.md "wikilink"), [Serial ATA等の最近のインターコネクトと同様](https://ja.wikipedia.org/wiki/Serial_ATA "wikilink")、[ポイント・ツー・ポイント](https://ja.wikipedia.org/wiki/ポイント・ツー・ポイント "wikilink")の双方向シリアル接続である。複数のプロセッサとHDD等の高速外部デバイス間の接続に利用される。複数の転送レートをサポートする他、PCI Expressのように[複数のチャネルを束ねて利用することで高速な帯域を実現することができる](https://ja.wikipedia.org/wiki/チャネルボンディング "wikilink")。

### 転送レート

Single Data Rate (SDR)のInfiniBand レーン一本は最大2.5 Gbps双方向の転送速度を持つ。Double Data Rate (DDR)およびQuad Data Rate (QDR)は、1レーンあたりそれぞれ 5 Gbps, 10 Gbps双方向の転送速度を実現する。エンコーディングの変更されたFourteen Data Rate (FDR)は、1レーンあたり14.0625Gbps双方向の転送速度を実現する。

SDR，DDR，QDRには[8b/10b](https://ja.wikipedia.org/wiki/8b/10b "wikilink")変換が用いられ、8bitのデータが10bit化され転送されるため、実効転送レートは上記の値の80%となる。よって実効転送レートはそれぞれ 2 Gbps, 4 Gbps, 8 Gbpsとなる。一方、FDRには[64b/66b](https://ja.wikipedia.org/wiki/64b/66b "wikilink")変換が用いられ、64bitのデータが66bit化され転送されるため、実効転送レートは上記の値の約97%となる。よって実効転送レートは 13.6 Gbpsとなる。

InfiniBandの接続を4本 (4X)もしくは12本 (12X)束ねて高い転送速度を実現することができる。12X においてHDRでデータ転送を行った場合、618.75 Gbps (raw)あるいは600 Gbps（データ転送）となる。2018年11月現在、HDRに対応した製品が入手可能である。12Xは主に、[コンピュータ・クラスター](../Page/コンピュータ・クラスター.md "wikilink")や[スーパーコンピュータ](../Page/スーパーコンピュータ.md "wikilink")のノード間接続やネットワークスイッチ間接続に用いられる。

また，InfiniBand Trade Associationによるロードマップでは今後，2020年後半にHDRのさらに2倍の性能となるNext Data Rate (NDR)が登場する予定であり，その後さらにXDR（名称不明）が提供される計画がある\[1\]。

<table>
<caption>構成ごとのスループット</caption>
<thead>
<tr class="header">
<th><p> </p></th>
<th><p>SDR</p></th>
<th><p>DDR</p></th>
<th><p>QDR</p></th>
<th><p>FDR</p></th>
<th><p>EDR</p></th>
<th><p>HDR</p></th>
<th><p>NDR</p></th>
<th><p>XDR</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>1レーン時の論理スループット (Gbit/s)</p></td>
<td><p>2.5</p></td>
<td><p>5</p></td>
<td><p>10</p></td>
<td><p>14.0625</p></td>
<td><p>25.78125</p></td>
<td><p>51.5625</p></td>
<td><p>103.125</p></td>
<td><p>255前後?</p></td>
</tr>
<tr class="even">
<td><p>1レーン時の実効スループット (Gbit/s)</p></td>
<td><p>2</p></td>
<td><p>4</p></td>
<td><p>8</p></td>
<td><p>13.64</p></td>
<td><p>25</p></td>
<td><p>50</p></td>
<td><p>100</p></td>
<td><p>250?</p></td>
</tr>
<tr class="odd">
<td><p>2レーン時の実効スループット (Gbit/s)</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td><p>100</p></td>
<td><p>200</p></td>
<td><p>500?</p></td>
</tr>
<tr class="even">
<td><p>4レーン時の実効スループット (Gbit/s)</p></td>
<td><p>8</p></td>
<td><p>16</p></td>
<td><p>32</p></td>
<td><p>54.55</p></td>
<td><p>100</p></td>
<td><p>200</p></td>
<td><p>400</p></td>
<td><p>1000?</p></td>
</tr>
<tr class="odd">
<td><p>8レーン時の実効スループット (Gbit/s)</p></td>
<td><p>16</p></td>
<td><p>32</p></td>
<td><p>64</p></td>
<td><p>109.09</p></td>
<td><p>200</p></td>
<td><p>400</p></td>
<td><p>800</p></td>
<td><p>2000?</p></td>
</tr>
<tr class="even">
<td><p>12レーン時の実効スループット (Gbit/s)</p></td>
<td><p>24</p></td>
<td><p>48</p></td>
<td><p>96</p></td>
<td><p>163.64</p></td>
<td><p>300</p></td>
<td><p>600</p></td>
<td><p>1200</p></td>
<td><p>3000?</p></td>
</tr>
<tr class="odd">
<td><p>エンコーディング (bit)</p></td>
<td><p>8/10</p></td>
<td><p>8/10</p></td>
<td><p>8/10</p></td>
<td><p>64/66</p></td>
<td><p>64/66</p></td>
<td><p>64/66</p></td>
<td><p>未定</p></td>
<td><p>未定</p></td>
</tr>
<tr class="even">
<td><p>規格発行年</p></td>
<td><p>2000</p></td>
<td><p>2005</p></td>
<td><p>2007</p></td>
<td><p>2011</p></td>
<td><p>2014</p></td>
<td><p>2017</p></td>
<td><p>2020以降</p></td>
<td><p>2023以降</p></td>
</tr>
</tbody>
</table>

### レイテンシ

[レイテンシ](../Page/レイテンシ.md "wikilink")はSDR スイッチでは200ナノ秒, DDRスイッチでは140ナノ秒, QDRスイッチでは100ナノ秒程度である。エンド・ツー・エンドでは、Mellanox社のHCA（Host Channel Adapter）である ConnectX を用いた場合のMPIレイテンシで1.07 マイクロ秒、Qlogic社の InfiniPath HTX を用いた1.29マイクロ秒、Mellanox社 InfiniHost IIIでは2.6マイクロ秒が観測されている。現在市場には多様な InfiniBand 用HCAがあり、製品によって特性は異なっている。

InfiniBand は RDMA（[Remote Direct Memory Access](https://ja.wikipedia.org/wiki/Remote_Direct_Memory_Access "wikilink")）をサポートしており、CPU オーバヘッドを低く抑えることが可能である。RDMA 命令のレイテンシは、1マイクロ秒以下である（Mellanox 社 ConnectX の場合）。参考までに、[DDR3 SDRAM](../Page/DDR3_SDRAM.md "wikilink") のメモリレイテンシは0.1マイクロ秒（100ナノ秒）程度である。

### ネットワーク構成

InfiniBandにおける[ネットワーク構成](https://ja.wikipedia.org/wiki/ネットワーク構成 "wikilink")は、Ethernetのような階層型ネットワークではなく、スイッチ型ファブリック接続を採用している。

多くの[メインフレーム](../Page/メインフレーム.md "wikilink")のチャネル・モデルのように、すべての転送はChannel Adapter間で行われる。各プロセッサノードはHost Channel Adapter (HCA)を持ち、各外部デバイスはTarget Channel Adapter (TCA)を持つ。これらのChannel Adapterはまたセキュリティ情報、[QoS](https://ja.wikipedia.org/wiki/QoS "wikilink")情報のやり取りが可能である。

### メッセージ

InfiniBandではデータは、ひとつあたり最大4 KBの複数のパケットにより構成されたメッセージのやり取りにより転送される。下記のメッセージ転送がサポートされる。

  - 遠隔ノード上のメモリに対する[DMA転送によるREADとWRITE](../Page/Direct_Memory_Access.md "wikilink")（[RDMA](https://ja.wikipedia.org/wiki/Remote_Direct_Memory_Access "wikilink")）
  - チャネル転送
  - [トランザクション](../Page/トランザクション.md "wikilink")命令（差し戻し可能）
  - [マルチキャスト](../Page/マルチキャスト.md "wikilink")
  - [不可分操作](../Page/不可分操作.md "wikilink")

## 経緯

[1998年](https://ja.wikipedia.org/wiki/1998年 "wikilink")後半、基幹業務に使用される各種[サーバ](../Page/サーバ.md "wikilink")の計算性能は、[ムーアの法則](../Page/ムーアの法則.md "wikilink")に従い、ほぼ18カ月に2倍のペースで高速化されてきていた。しかし、サーバ内の[バス](../Page/バス_\(コンピュータ\).md "wikilink")[アーキテクチャは機械](../Page/コンピュータ・アーキテクチャ.md "wikilink")・電気的制限により、その進化に追い付けず、[コンピュータシステム](../Page/コンピュータシステム.md "wikilink")性能向上の[ボトルネック](../Page/ボトルネック.md "wikilink")となっていた。

そこで、[インテル](https://ja.wikipedia.org/wiki/インテル "wikilink")を中心に[スイッチ](../Page/スイッチ.md "wikilink")型ファブリックインターコネクトテクノロジをベースとした新しいI/OアーキテクチャとしてNGIO (Next Generation I/O)が提唱され、規格定義を開始した\[2\]。一方、[タンデムコンピューターズ](../Page/タンデムコンピューターズ.md "wikilink")社の[ServerNet](https://ja.wikipedia.org/wiki/ServerNet "wikilink")の流れを汲む[Compaq](../Page/コンパック.md "wikilink")（HPに吸収合併された）、[HP社](../Page/ヒューレット・パッカード.md "wikilink")、[IBM](../Page/IBM.md "wikilink")社の3社は、同様の技術をサポートしたFIO (Future I/O)を提唱した。

ところが、[1999年](../Page/1999年.md "wikilink")の[IDF Spring 1999において](https://ja.wikipedia.org/wiki/インテル・デベロッパー・フォーラム "wikilink")、NGIOの情報が公開された際、FIOの仕様の一部が取り込まれており、最終的には両陣営が歩み寄り、SIO (System I/O)として統合されることとなった。

その後、2000年1月に、SIOはInfiniBandに改称された。

2000年10月には、複数のベンダから構成された業界団体「InfiniBand Trade Association」により、規格書が提出され、統一的な規格として成立した。現時点の規格は、InfiniBand Architecture Specification Release 1.2.1。

当初本規格のリーダ的存在だったインテルが撤退を表明し、動向が注目されたが、その後HPC分野を中心に広く利用されるようになっている。

## 現状

多くの計算機ノードを接続して構成される[HPC](../Page/高性能計算.md "wikilink") 業界では、InfiniBandのシェアは高い。2015年11月時点で[TOP500](https://ja.wikipedia.org/wiki/TOP500 "wikilink")ではもっとも使われている接続方法となっていた（Mellanox調べ）\[3\]。しかしその後中国のシステムを中心にイーサネットの採用が増え2017年11月時点ではInfiniBandの採用数は減少し2番手に転落している\[4\]。

各ベンダのブレード系サーバやグリッド系サーバの接続でオプションとして用意されている\[5\]。

日本での使用例としては、[ヒューレット・パッカード](../Page/ヒューレット・パッカード.md "wikilink")のサーバを使用してNECが構築した[東京工業大学](../Page/東京工業大学.md "wikilink")のPCクラスタ[TSUBAME](../Page/TSUBAME.md "wikilink")2.0や、[京都大学](../Page/京都大学.md "wikilink")や[筑波大学](../Page/筑波大学.md "wikilink")の[T2Kオープンスパコン](https://ja.wikipedia.org/wiki/T2Kオープンスパコン "wikilink")が挙げられる\[6\]。

[ストレージ](https://ja.wikipedia.org/wiki/ストレージ "wikilink")では、[NetApp](https://ja.wikipedia.org/wiki/NetApp "wikilink")、[ピュア・ストレージ](https://ja.wikipedia.org/wiki/ピュア・ストレージ "wikilink")、[EMCといったメーカーの製品でホストI](https://ja.wikipedia.org/wiki/EMCコーポレーション "wikilink")/Oのオプションとして用意されている。

## ロードマップ

2018年現在、NDRは2020年後半、XDRは2023年以降に登場すると思われる\[7\]。

## 脚注

## 関連項目

  - [並列化](../Page/並列化.md "wikilink")
  - [並列コンピューティング](https://ja.wikipedia.org/wiki/並列コンピューティング "wikilink")
  - [グリッド・コンピューティング](../Page/グリッド・コンピューティング.md "wikilink")
  - [SCore](https://ja.wikipedia.org/wiki/SCore "wikilink")

[Category:コンピュータバス](https://ja.wikipedia.org/wiki/Category:コンピュータバス "wikilink") [Category:並列コンピューティング](https://ja.wikipedia.org/wiki/Category:並列コンピューティング "wikilink") [Category:スーパーコンピュータ](https://ja.wikipedia.org/wiki/Category:スーパーコンピュータ "wikilink")

1.
2.
3.
4.
5.  [日本電気](../Page/日本電気.md "wikilink")Express 5800（MellanoxのOEM）、[富士通](../Page/富士通.md "wikilink")PRIMEQUEST（MellanoxのOEM）、[レノボBladeCenter](https://ja.wikipedia.org/wiki/Lenovo "wikilink")（MellanoxのOEM）、[デル](https://ja.wikipedia.org/wiki/Dell "wikilink")（MellanoxのOEM）、[ヒューレット・パッカード](../Page/HP.md "wikilink")（MellanoxのOEM）など
6.  同じT2Kでも[東京大学](https://ja.wikipedia.org/wiki/東京大学 "wikilink")のシステムはInfiniBandではなく、[Myrinet](https://ja.wikipedia.org/wiki/Myrinet "wikilink")を採用している
7.
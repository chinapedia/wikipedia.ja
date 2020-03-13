> この記事は[HyperTransport](https://ja.wikipedia.org/wiki/HyperTransport)から翻訳されています。


**HyperTransport**（ハイパートランスポート、**HT**）は、[AMDが提唱したPoint](https://ja.wikipedia.org/wiki/アドバンスト・マイクロ・デバイセズ "wikilink") to Point式の汎用接続技術。

以前はLightning Data Transport (LDT) と呼ばれていたものである。双方向、シリアル/パラレル、広帯域、低遅延を特徴とする[コンピュータバスであり](../Page/バス_\(コンピュータ\).md "wikilink")、[2001年](../Page/2001年.md "wikilink")[4月2日](../Page/4月2日.md "wikilink")に導入された。 この技術は[x86](https://ja.wikipedia.org/wiki/x86 "wikilink")プロセッサではAMDと[トランスメタ](../Page/トランスメタ.md "wikilink")、[MIPSアーキテクチャ](../Page/MIPSアーキテクチャ.md "wikilink")では[PMC-Sierra](https://ja.wikipedia.org/wiki/PMC-Sierra "wikilink")、[Broadcom](https://ja.wikipedia.org/wiki/Broadcom "wikilink")、Raza Microelectoronics、PCチップセットではAMD、[NVIDIA](../Page/NVIDIA.md "wikilink")、[VIA](../Page/VIA_Technologies.md "wikilink")、[SiS](https://ja.wikipedia.org/wiki/SiS "wikilink")、[ULi](../Page/ULi.md "wikilink")/[ALi](../Page/ALi_\(企業\).md "wikilink")、[HP](../Page/ヒューレット・パッカード.md "wikilink")、[サーバ](../Page/サーバ.md "wikilink")ではHP、[サン・マイクロシステムズ](../Page/サン・マイクロシステムズ.md "wikilink")、[IBM](../Page/IBM.md "wikilink")、IWill、ストレージでは、[Network Appliance](https://ja.wikipedia.org/wiki/Network_Appliance "wikilink")、ハイパフォーマンスコンピューティングでは[クレイ](../Page/クレイ.md "wikilink")、Newisys、PathScale、ルーターでは[シスコシステムズ](../Page/シスコシステムズ.md "wikilink")が用いている。

HyperTransport[コンソーシアム](../Page/コンソーシアム.md "wikilink")がHyperTransportテクノロジの普及と開発に努めている。

## 概要

HyperTransportには4つバージョンがある。1.x、2.0、3.0そして3.1である。これらは200MHzから3.2GHzまで動作する。このバスはDDR（Double Data Rate）接続され、[クロック信号](https://ja.wikipedia.org/wiki/クロック信号 "wikilink")の立ち上がりと立ち下りの両方でデータを送信する。これにより、3.2GHz動作時に最大毎秒64億回送信が可能である。この周波数は自動的に調整される。

HyperTransportは2つの2bitラインから2つの32bitラインまであることから、ビット幅を自動的に調整する機能をサポートしている。HyperTransport 3.1の場合、フルサイズ、フルスピードで双方向に32bit接続すると、51.2 GB/s (3.2 GHz/links \* 2 bit/Hz \* 32 links \* 1 byte / 8) の送信速度が出る。これは多くの既存の標準バスよりもかなり速い。また一つのシステム内で様々なバス幅を混在させることができる（例えば1x16の代わりに2x8など）。これにより、メインメモリと[CPU](../Page/CPU.md "wikilink")間にはより高速な接続を用い、[周辺機器](../Page/周辺機器.md "wikilink")同士にはより遅い接続を用いることができる。また、HyperTransportは他のバスと比較してかなり低遅延である。

HyperTransportは[パケット](../Page/パケット.md "wikilink")ベースであり、物理的な接続幅にかかわらず、それぞれのパケットは32ビットワードの組み合わせで構成されている。パケットの1ワード目は常にコマンドワードである。もしパケットにアドレスが含まれていたならば、コマンドワードの最後の8ビットは次の32ビットワードとつながって40ビットアドレスを構成する。64ビットアドレッシングが必要な時には、追加の32bitコントロールパケットによって可能になる。1パケット内の32ビットワードはデータペイロードである。転送は実際の長さにかかわらず、常に複数の32ビットにパディングして行われる。

HyperTransportパケットはbit timeとして知られるセグメント内に入れられる。パケットが必要とするbit timeの数は相互接続のバス幅に依存する。HyperTransportはシステム管理メッセージを発生、シグナル割り込み、デバイスやプロセッサを調整するためのプローブ発行、汎用I/Oやデータトランザクションに使うことができる。また、posted writeとnon-posted writeの2つの異なるwriteコマンドを使うことができる。Posted writeはターゲットからのレスポンスを必要としないwriteコマンドである。これはUMAトラフィックやDMA転送のような広帯域のデバイスに通常用いられる。Non-posted writeは受信側から「ターゲット動作完了」のレスポンスを受け取ることを必要とする。読み出しもまた受信側がreadレスポンスを発生させる。

また、HyperTransportは[ACPIに準拠することでパワーマネジメントを強くサポートしている](../Page/Advanced_Configuration_and_Power_Interface.md "wikilink")。このことにより、プロセッサのスリープ状態 (C state) が変化することによって、デバイスの状態 (D state) を変化させる信号を出すことができることを意味する。すなわちCPUがスリープしたらディスクの電源を切ることができる。

電気的には、HyperTransport/LDTは2.5V動作の[Low voltage differential signaling](../Page/Low_voltage_differential_signaling.md "wikilink") (LVDS) に似ている。

HyperTransportを省略してHTと呼称することも多いが、これは[インテル](https://ja.wikipedia.org/wiki/インテル "wikilink")CPUに実装されている[HyperThreading Technologyの略称と混同されやすい](../Page/ハイパースレッディング・テクノロジー.md "wikilink")。この潜在的な間違えやすさのために、HyperTransport[コンソーシアム](../Page/コンソーシアム.md "wikilink")は常に「HyperTransport」として表記するようにしている。

## HyperTransportの適用例

### フロントサイドバスの置き換え

HyperTransportの主要な用途は[フロントサイドバス](../Page/フロントサイドバス.md "wikilink")の置き換えである。フロントサイドバスは現在すべてのマシン（もしくはそれらのシステムのいくつか）で異なっている。システムを拡張するために、フロントサイドバスは[AGPや](../Page/Accelerated_Graphics_Port.md "wikilink")[PCIのような様々な標準バス用のアダプタを通して接続しなければならない](../Page/Peripheral_Component_Interconnect.md "wikilink")。これらは普通各々のコントローラの機能の中に含まれていて、[ノースブリッジ](../Page/ノースブリッジ.md "wikilink")や[サウスブリッジ](../Page/サウスブリッジ.md "wikilink")として呼ばれている。

理論上、HyperTransportで実装された大方のコンピュータは、処理速度が速いと同時に柔軟性に富んでいる。PCIとHyperTransportを変換するチップはHyperTransportを使用可能などのマイクロプロセッサでも動作できるであろうし、これらのプロセッサでPCIカードを用いることも可能である。例えば、NVIDIAのnForceチップセットはノースブリッジとサウスブリッジを接続するのにHyperTransportを用いている。

### マルチプロセッサ間接続

HyperTransportの別の用途として、[NUMA](../Page/NUMA.md "wikilink")[マルチプロセッサ](https://ja.wikipedia.org/wiki/マルチプロセッサ "wikilink")のチップ間接続がある。AMDは[Opteron](https://ja.wikipedia.org/wiki/Opteron "wikilink")と[Athlon 64のプロセッサ商品群にDirect](../Page/Athlon_64.md "wikilink") Connect Architectureの一部として独自の[キャッシュコヒーレンシー](https://ja.wikipedia.org/wiki/キャッシュコヒーレンシー "wikilink")拡張を持つHyperTransportを使用している ([cc-NUMA](https://ja.wikipedia.org/wiki/cc-NUMA "wikilink"))。NewisysのHORUS接続はこの考えをより大きな[クラスターマシンに拡張したものである](../Page/コンピュータ・クラスター.md "wikilink")。

### ルーターないしスイッチバスの置き換え

また、HyperTransportは[ルーター](../Page/ルーター.md "wikilink")やスイッチ内でバスとしても用いられる。ルーターやスイッチは複数の接続ポートを持ち、できる限り速くポート間でデータをやりとりしなければならない。例えば、4つの100MBit/sのポートを持つ[イーサネット](../Page/イーサネット.md "wikilink")ルーターは800MBits/sより速いバスが必要である（100MBit/s \* 4ポート \* 2 方向）。HyperTransportはこの用途に必要とされる帯域よりは遥かに高速である。

### HTXとコプロセッサ間接続

CPUとコプロセッサとの間の帯域の問題はいつも実用的な実装を行う際の悩みの種となってきた。この問題が公にならないまま数年後、近年導入されたHyperTransportインタフェースを用いて設計された拡張用は、HyperTransport eXpansion (HTX) として知られる。16レーンの[PCI Expressスロットと同じ機構のコネクタを用いており](../Page/PCI_Express.md "wikilink")、HTXは挿入されたカードがCPUへの直接アクセスとシステム[RAMへの](../Page/Random_Access_Memory.md "wikilink")[DMAアクセスができるように開発された](../Page/Direct_Memory_Access.md "wikilink")。近年、HyperTransportバスにアクセスできるFPGAが現れており、コプロセッサはマザーボード上での最優遇住人となってきている。主要なメーカー（AlteraとXilinx）の両方が出している現世代のFPGAはHyperTransportを直接サポートしており、IPコアも使うことができる。 しかし、HTXの仕様では、HyperTransportデバイスはHTXコネクタを通してHyperTransportの最大スループットのたった1/4しか通信できない。これは、32ビット、2.8GHzで動作可能な初期のSamtecコネクタにもかかわらず、16ビットのPCI Expressコネクタを使って1.4GHzにクロックを落として使っているようなものである。

## 実装

  - AMD [AMD64とDirect](https://ja.wikipedia.org/wiki/x64 "wikilink") Connect ArchitectureをベースとしているCPU
  - OpenCoreプロジェクト（MPLライセンス）からリリースされているht_tunnel
  - AMD プロセッサ向けのATI Radeon Xpress 200
  - NVIDIA nForce Professional MCP（メディアおよび通信プロセッサ）
  - ServerWorks HT-2000 HyperTransport SystemI/Oコントローラ
  - PowerPC G5搭載アップルデスクトップPC

## 周波数の仕様

<table>
<thead>
<tr class="header">
<th><p>HyperTransport<br />
バージョン</p></th>
<th><p>策定年</p></th>
<th><p>最大の HT 参照クロック</p></th>
<th><p>最大のリンク幅</p></th>
<th><p>最大の総計帯域<br />
(双方向)</p></th>
<th><p>最大の帯域<br />
(16 ビット 単方向)</p></th>
<th><p>最大の帯域<br />
(32 ビット 単方向)*</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>1.0</p></td>
<td><p>2001 年</p></td>
<td><p>800 MHz</p></td>
<td><p>32 ビット</p></td>
<td><p>12.8 GB/秒</p></td>
<td><p>3.2 GB/秒</p></td>
<td><p>6.4 GB/秒</p></td>
</tr>
<tr class="even">
<td><p>1.1</p></td>
<td><p>2002 年</p></td>
<td><p>800 MHz</p></td>
<td><p>32 ビット</p></td>
<td><p>12.8 GB/秒</p></td>
<td><p>3.2 GB/秒</p></td>
<td><p>6.4 GB/秒</p></td>
</tr>
<tr class="odd">
<td><p>2.0</p></td>
<td><p>2004 年</p></td>
<td><p>1.4 GHz</p></td>
<td><p>32 ビット</p></td>
<td><p>22.4 GB/秒</p></td>
<td><p>5.6 GB/秒</p></td>
<td><p>11.2 GB/秒</p></td>
</tr>
<tr class="even">
<td><p>3.0</p></td>
<td><p>2006 年</p></td>
<td><p>2.6 GHz</p></td>
<td><p>32 ビット</p></td>
<td><p>41.6 GB/秒</p></td>
<td><p>10.4 GB/秒</p></td>
<td><p>20.8 GB/秒</p></td>
</tr>
<tr class="odd">
<td><p>3.1</p></td>
<td><p>2008 年</p></td>
<td><p>3.2 GHz</p></td>
<td><p>32 ビット</p></td>
<td><p>51.2 GB/秒</p></td>
<td><p>12.8 GB/秒</p></td>
<td><p>25.6 GB/秒</p></td>
</tr>
</tbody>
</table>

  - AMD Opteron と、 Athlon 64 を含むそれ以降の CPU は 16 ビット幅でリンクしている。古いタイプの Opteron あるいは Athlon 64 は 800 MHz から 1 GHz で接続していて、比較的新しい（Socket AM2+ の規格）では、2.6 GHz までで接続されている。HyperTransport は 32 ビット リンクが可能であるが、その帯域幅を AMD は現在使用していない。

## 外部リンク

  - [HyperTransport Consortium](https://www.hypertransport.org/)
  - [HT Overview](https://www.hypertransport.org/ht-overview)
  - [HT Link Specifications](https://www.hypertransport.org/ht-link-specifications)

[Category:コンピュータバス規格](https://ja.wikipedia.org/wiki/Category:コンピュータバス規格 "wikilink")
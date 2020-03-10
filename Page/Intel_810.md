> この記事は[Intel 810](https://ja.wikipedia.org/wiki/Intel_810)から翻訳されています。


**Intel 810** (i810) は、ローエンドPC向けとして1999年に[インテル](https://ja.wikipedia.org/wiki/インテル "wikilink")社が発表・発売した[インテル チップセットの製品およびそのファミリー名である](https://ja.wikipedia.org/wiki/インテル_チップセット "wikilink")。

## 概要

**Intel 810**はインテル社初のグラフィック統合[チップセット](../Page/チップセット.md "wikilink")として[1999年](../Page/1999年.md "wikilink")[6月](../Page/6月.md "wikilink")に発表された。開発コードネームはWhitney（ホイットニー）である。大きな特徴は2つあり、1つはインテルで初の[2D/3Dグラフィック機能を統合した製品であり](../Page/オンボードグラフィック.md "wikilink")、[Intel752を基に開発した](https://ja.wikipedia.org/wiki/Intel_740#Intel_752 "wikilink")**IGT (Intel Graphics Technology) コア**を実装している。また、2チップで構成されるチップセットのチップ間をインテル・ハブ・リンク I/O インターフェイスと命名された専用インターコネクトを実装した**[ハブ・アーキテクチャ](https://ja.wikipedia.org/wiki/ハブ・アーキテクチャ "wikilink")（Hub Architecture）**を採用した最初の製品である。またInstantly Available PC technologyにより、[スタンバイ](https://ja.wikipedia.org/wiki/サスペンド_\(コンピュータ\) "wikilink")（サスペンド）状態からの復帰も高速化されている。

従来の一般的な[インテル チップセット同様に](https://ja.wikipedia.org/wiki/インテル_チップセット "wikilink")2チップ構成となっているが、ハブ・アーキテクチャの採用に伴い、[ノースブリッジ](../Page/ノースブリッジ.md "wikilink")で従来PAC（PCI AGP Controller）と呼ばれていたチップは**GMCH（Graphics Memory Controller Hub）**、同じく[サウスブリッジ](../Page/サウスブリッジ.md "wikilink")でPIIX（PCI ISA IDE Xcelerator）と呼ばれていたチップは**[ICH (I/O Controller Hub)](https://ja.wikipedia.org/wiki/I/O_コントローラー・ハブ "wikilink")** と改称された。また、[BIOS](https://ja.wikipedia.org/wiki/Basic_Input/Output_System "wikilink") [ROMも](../Page/フラッシュメモリ.md "wikilink")**FCH（Firmware Controller Hub）**と命名されたが、普及には至らなかった。

PCIに接続されるデバイスの高速化に伴い、Intel 810以前のチップセットでは[PCIバスで接続されていたPACとPIIX間の帯域を圧迫し](../Page/Peripheral_Component_Interconnect.md "wikilink")、パフォーマンスの低下が問題となっていた。Intel 810が採用したハブ・アーキテクチャでは、GMCHとICHを専用の**ハブ・リンク （Hub Link）**で接続している。ハブ・リンクはPCIバスの2倍の266MB/秒の帯域を実現しており、パフォーマンスの問題を解決している。

このGMCHとICHがハブ・リンクで接続されるハブ・アーキテクチャは以降のインテルチップセットの基本形となり、以後のチップセットは810で採用されたハブ・アーキテクチャを踏襲したものとなった。その後、900番台のチップセットではハブ・リンクはさらに4倍の帯域となり、DMI（Direct Media Interface）と命名されている。

その反面、ローエンド向けとしての設計されていることから、前世代のワークステーション・メインストリーム向けチップセット[Intel 440BXが対応していた](https://ja.wikipedia.org/wiki/Intel_440BX "wikilink")**[SMP](../Page/対称型マルチプロセッシング.md "wikilink")**への対応は上位チップセットである[Intel 820へ継承され](https://ja.wikipedia.org/wiki/Intel_820 "wikilink")、本チップセットでは公式に非対応とされた（Intel 440BX自体も単体で対応していた訳ではなく、SMPシステムに必要な制御を行うI/O [APIC](https://ja.wikipedia.org/wiki/APIC "wikilink")コントローラチップIntel 82093AAを追加する事で対応していた。 Intel 820では同コントローラが内蔵されている）。後述のとおり最大メモリ容量も440BXの1GBに対して本チップセットや[Intel 815では](https://ja.wikipedia.org/wiki/Intel_815 "wikilink")512MBに制限されている。後年、ウェブブラウザなどのアプリケーションのメモリの使用量が急激に増えたため、メモリ容量の制限はローエンドとはいえ予想外に大きな足かせとなった。

## GMCH

[thumb](https://ja.wikipedia.org/wiki/ファイル:Intel_810_Chipset_Digon3.JPG "wikilink") GMCHであるIntel 82810はIGTコアを統合し2D/3Dグラフィックス機能を実現している。メインメモリの対応はは512MBまでのPC66またはPC100の[SDRAM](https://ja.wikipedia.org/wiki/SDRAM "wikilink")に留まるが、[FSBは](https://ja.wikipedia.org/wiki/フロントサイドバス "wikilink")[Celeron](https://ja.wikipedia.org/wiki/Celeron "wikilink")用となる66MHzだけでなく、[Pentium IIIに対応できる](../Page/Pentium_III.md "wikilink")100MHzにも対応している。さらに[1999年](../Page/1999年.md "wikilink")[9月](../Page/9月.md "wikilink")にはFSB 133MHz版のPentium IIIの発売と共にそれに対応した**Intel 810E**が発表されている。このため、PCメーカーはCeleronを採用したバリューPCとPentium IIIを採用したパフォーマンスPCにIntel 810を実装したマザーボードを共用できPCのコスト削減に貢献し、Intel 810を採用したPCが数多く出荷されることとなった。ただし付帯する[クロック](../Page/クロック.md "wikilink")[ジェネレータにおいて](https://ja.wikipedia.org/wiki/発振回路 "wikilink")66MHzあるいは100MHzまでしか生成しない設計もありうるため、Intel 810EおよびCeleronを搭載し出荷された[PCすべてが](../Page/パーソナルコンピュータ.md "wikilink")133MHz版Pentium IIIへ換装できるとは限らない。同様に、Intel 810およびCeleronを搭載し出荷されたPCすべてが100MHz版Pentium IIIへ換装できるとは限らない。

本来、Intel 810シリーズは上位チップセットである[Intel 820と並存する市況を想定されたが](https://ja.wikipedia.org/wiki/Intel_820 "wikilink")、Intel 820用の新メモリ[RDRAM](../Page/RDRAM.md "wikilink")がインテルの想定通りには値下がりせず、さらに初期出荷のIntel 820の不良回収が行なわれたこと、Intel 820でSDRAMを利用可能とする付加チップMTH（Memory Transfer Hub）のマザーボード発売後の不具合の発見により、Intel 820に悪い印象が付き纏い敬遠され、Intel 820とIntel 810の間を埋める[Intel 815の発売まで](https://ja.wikipedia.org/wiki/Intel_815 "wikilink")、事実上インテル社唯一のチップセットとなっていた。

### 統合グラフィックス機能

Intel 810に統合されるグラフィックス機能は[Intel 752をベースとした](https://ja.wikipedia.org/wiki/Intel_740#Intel_752 "wikilink")**Intel Graphics Technology** (IGT) コアである。コアクロック100MHzで動作し、コア内部では[AGP 2x相当で接続されている](../Page/Accelerated_Graphics_Port.md "wikilink")。32bitレンダリングをサポートせず、2D/3D共に当時のビデオカードと比較して貧弱な性能ではあったが、[DirectX](https://ja.wikipedia.org/wiki/DirectX "wikilink") 6世代の[Direct3D](https://ja.wikipedia.org/wiki/Direct3D "wikilink")に対応し、[MCによる動画再生支援にも対応するなど](https://ja.wikipedia.org/wiki/動き補償#フレーム間予測 "wikilink")、当時のビジネスおよびホームユーザーには十分な機能を有しており、広く受け入れられることに成功した。

#### UMAとDisplay Cache

Intel 810ではフレームバッファとして専用の[ビデオメモリをサポートせず](../Page/VRAM.md "wikilink")、メインメモリと共有する[UMA](https://ja.wikipedia.org/wiki/ユニファイドメモリアーキテクチャ "wikilink") (Unified Memory Architecture) を採用している。これにより低価格化・省スペース化は可能になったが、メモリ帯域に余裕の無いIntel 810ではパフォーマンスの低下は必至であった。

この問題の解決策としてIntel 810はオプションとして**Display Cache**をサポートしている。これは[Zバッファ](https://ja.wikipedia.org/wiki/Zバッファ "wikilink")専用のメモリであり、メモリ負荷の高いZバッファを専用メモリに格納することでメインメモリの負荷軽減を図ったものであり、後のIntel 815でも同様の技術が採用された。Display Cacheを付加した製品の型番には、Display Cacheを示すDCが付与されている。

## ICH

GMCHに接続されるIntel 82801AAはICHと呼称され、従来のサウスブリッジ同様に[ATA](../Page/Advanced_Technology_Attachment.md "wikilink")・[USBや各種レガシコントローラを搭載する他](../Page/ユニバーサル・シリアル・バス.md "wikilink")、[AC'97対応のサウンドコントローラや](../Page/Audio_Codec_97.md "wikilink")[ネットワークの論理層も統合している](../Page/イーサネット.md "wikilink")。この為、コーデックチップ又は物理層チップを追加するだけで、安価にサウンド/ソフトウェア[モデム](https://ja.wikipedia.org/wiki/モデム "wikilink")機能・[ネットワーク機能を](../Page/Local_Area_Network.md "wikilink")[オンボード](../Page/オンボード.md "wikilink")で実現できるようになった。これに伴いセットメーカーがオプションのバリエーションを採用しやすくするための[AMRスロットがサポートされている](https://ja.wikipedia.org/wiki/Audio_and_Modem_Riser "wikilink")。

Intel 810シリーズではメインストリーム向けに6スロットのPCIとUltraATA/66に対応したICHが採用されていた他、廉価版のIntel 810-Lでは4スロットのPCIとUltraATA/33までの対応に留まるICH0（Intel 82801）と組み合わされている。またIntel 810E2ではATA100に対応したIntel 82801BAのICH2が採用されている。

また、PC/AT互換機で永く使用されてきた[ISAバスのサポートが打ち切られており](../Page/Industry_Standard_Architecture.md "wikilink")、必要な場合はオプションのPCI-to-ISAブリッジにより対応する。

## 評価と影響

ローエンド向けとして発表されたIntel 810だが、ローエンドモデルからパフォーマンスモデルまで広く採用される大ヒットとなった。 Intel 810のヒットの要因としては以下が挙げられる。

  - 100MHz・133MHzのFSBにも対応しCeleronだけでなくPentium IIIのハイエンド製品も搭載可能であった。
  - 本来、Pentium III用チップセットとして発売されたIntel 820が諸般の事情が重なり商業上失敗に終わった。
  - 最低限必要な性能のグラフィック機能を統合したことで安価・省スペースなPCが実現可能だった。

Intel 810が広く普及したことで、それまでオンボードもしくはディスクリートの[ビデオカード](../Page/ビデオカード.md "wikilink")として使用されていたビデオコントローラのうち、IGTコア以下の性能・機能の製品は淘汰された。しかしIntel 810のGMCHは外部AGPをサポートしておらず、CPUのメモリアクセスを阻害するUMA構成だったこと、133 MHzのFSBにマッチしたPC133 SDRAMもサポートしていなかったため、高性能を要求するユーザーには不評であった。

後継製品は、Intel 820の失敗で開いた穴を埋める形でその欠点を改良したIntel 815である。

## ラインナップ

<table>
<thead>
<tr class="header">
<th><p>製品名</p></th>
<th><p>対応FSB</p></th>
<th><p>対応メモリ</p></th>
<th><p>最大メモリ容量</p></th>
<th><p>Display Cache</p></th>
<th><p>ICH</p></th>
<th><p>ATA</p></th>
<th><p>USB</p></th>
<th><p>PCI</p></th>
<th><p>SMP</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>810-DC</p></td>
<td><p>66/100MHz</p></td>
<td><p>PC66・PC100</p></td>
<td><p>512MB</p></td>
<td><p>サポート<br />
(オプション)</p></td>
<td><p>ICH</p></td>
<td><p>ATA66</p></td>
<td><p>2ポート</p></td>
<td><p>6</p></td>
<td><p>非対応</p></td>
</tr>
<tr class="even">
<td><p>810</p></td>
<td><p>66/100MHz</p></td>
<td><p>PC66・PC100</p></td>
<td><p>512MB</p></td>
<td><p>無</p></td>
<td><p>ICH</p></td>
<td><p>ATA66</p></td>
<td><p>2ポート</p></td>
<td><p>6</p></td>
<td><p>非対応</p></td>
</tr>
<tr class="odd">
<td><p>810-L</p></td>
<td><p>66/100MHz</p></td>
<td><p>PC66・PC100</p></td>
<td><p>512MB</p></td>
<td><p>無</p></td>
<td><p>ICH-L</p></td>
<td><p>ATA33</p></td>
<td><p>2ポート</p></td>
<td><p>4</p></td>
<td><p>非対応</p></td>
</tr>
<tr class="even">
<td><p>810E</p></td>
<td><p>66/100/133MHz</p></td>
<td><p>PC66・PC100</p></td>
<td><p>512MB</p></td>
<td><p>サポート<br />
(オプション)</p></td>
<td><p>ICH</p></td>
<td><p>ATA66</p></td>
<td><p>2ポート</p></td>
<td><p>6</p></td>
<td><p>非対応</p></td>
</tr>
<tr class="odd">
<td><p>810E2</p></td>
<td><p>66/100/133MHz</p></td>
<td><p>PC66・PC100</p></td>
<td><p>512MB</p></td>
<td><p>サポート<br />
(オプション)</p></td>
<td><p>ICH2</p></td>
<td><p>ATA100</p></td>
<td><p>4ポート</p></td>
<td><p>6</p></td>
<td><p>非対応</p></td>
</tr>
</tbody>
</table>

  - i810Eとi810E2のみ、TualatinコアのAGTLバスに対応したB0ステッピングの製品が投入された。
  - FSB133MHzに対応する製品であってもメインメモリバスクロックは上限100MHzに留まる。

## 関連項目

  - [Intel 740](../Page/Intel_740.md "wikilink")
  - [インテル チップセット](https://ja.wikipedia.org/wiki/インテル_チップセット "wikilink")
      - [Intel 815](https://ja.wikipedia.org/wiki/Intel_815 "wikilink")
      - [Intel 820](https://ja.wikipedia.org/wiki/Intel_820 "wikilink")
  - [Integrated Graphics Processor](../Page/Integrated_Graphics_Processor.md "wikilink")
      - [AMD 690 チップセットシリーズ](../Page/AMD_690_チップセットシリーズ.md "wikilink")

[Category:インテルのチップセット](https://ja.wikipedia.org/wiki/Category:インテルのチップセット "wikilink") [Category:オンボードグラフィック](https://ja.wikipedia.org/wiki/Category:オンボードグラフィック "wikilink")
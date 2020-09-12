> この記事は[LANスイッチ](https://ja.wikipedia.org/wiki/LANスイッチ)から翻訳されています。


**LANスイッチ**（[英語](../Page/英語.md "wikilink"):**LAN Switch**）は、[イーサネット](../Page/イーサネット.md "wikilink")**[LAN](https://ja.wikipedia.org/wiki/LAN "wikilink")** (**Local Area Network**) を構成するネットワーク機器で、[ブリッジまたは](../Page/ブリッジ_\(ネットワーク機器\).md "wikilink")[ルーター](../Page/ルーター.md "wikilink")の機能を[ASIC](../Page/ASIC.md "wikilink")によるハードウエア処理で実現するものである。

## 概説

LANスイッチの言葉としての位置付けは、方式論や概念としてのLANではなく、具体的なネットワーク機器製品のカテゴリーとしてのものである。

LANには[イーサネット](../Page/イーサネット.md "wikilink") (Ethernet、[IEEE](../Page/IEEE.md "wikilink") 802.3) 、[トークンバス](https://ja.wikipedia.org/wiki/トークンバス "wikilink") (Token Bus、IEEE 802.4) 、[トークンリング](../Page/トークンリング.md "wikilink") (Token Ring、IEEE 802.5) の種類があるが、製品の普及の歴史から、LANスイッチと言う場合は**イーサネット**に関する物である。

[ブリッジ機能を実現する](../Page/ブリッジ_\(ネットワーク機器\).md "wikilink")**[レイヤ2スイッチ](https://ja.wikipedia.org/wiki/レイヤ2スイッチ "wikilink")**、それに加えて[ルーティング](../Page/ルーティング.md "wikilink")機能も実現する**[レイヤ3スイッチ](../Page/レイヤ3スイッチ.md "wikilink")**が存在する。 いずれもソフトウエア処理ではなくASICによる**ハードウエア処理**で実現する事が特徴である。レイヤ2転送機能の詳細は[ブリッジ](../Page/ブリッジ_\(ネットワーク機器\).md "wikilink")、レイヤ3転送機能は[ルーター](../Page/ルーター.md "wikilink")をそれぞれ参照のこと。

特に[ルーティング](../Page/ルーティング.md "wikilink")機能を提供するネットワーク機器はソフトウエア処理による[ルーター](../Page/ルーター.md "wikilink")製品から始まったため、それとの対比としてハードウエア処理方式による製品であることを強調してLANスイッチという語が用いられる。 またレイヤ2スイッチについては、[ツイストペアケーブル](../Page/ツイストペアケーブル.md "wikilink")を用いたイーサネットLANの集線装置としての[リピーターハブに対してブリッジ機能を提供するものとして](../Page/ハブ_\(ネットワーク機器\).md "wikilink")、**[スイッチングハブ](../Page/スイッチングハブ.md "wikilink")**、**マルチポートブリッジ**という名称でも呼ばれる。レイヤ2スイッチにはシャーシ型で、ツイストペアケーブル以外の種類も含めてインターフェースモジュールを挿入して実装するタイプの機器も存在するのに対して、スイッチングハブは主にインターフェースモジュールの増設できないボックス型でツイストペアケーブルのインターフェースを主とする。スイッチングハブはレイヤ2スイッチの一部である。

LANスイッチはパケットの転送をハードウエア処理するため、ソフトウエア処理のルーターよりも**高スループット**、**低遅延**であることが特徴である。ネットワーク利用で多いIPトラフィックで、他に設計上の事情がない場合にはソフトウエア処理のルーター製品よりもLANスイッチが利用される傾向がある。一方ルーターは通過するトラフィックにソフトウエア的な処理が必要な場合に用いられる。例えば[IBM](../Page/IBM.md "wikilink")[メインフレーム](../Page/メインフレーム.md "wikilink")で使用される[SNAのトラフィックで各種ブリッジ変換](../Page/Systems_Network_Architecture.md "wikilink")（シリアル回線、トークンリング、イーサネット間のメディア変換）、DLSw (。RFC 1434、1795、2166) を使用する場合や、トラフィックの帯域制御（シェーピング）を使用する場合である。

## VLAN(バーチャルLAN)

LANスイッチで実現可能となった機能として**[VLAN](https://ja.wikipedia.org/wiki/VLAN "wikilink")**が挙げられる。 VALNはLANスイッチに装備されたインターフェースをグループ分けして別のLANセグメントとして取り扱う機能である。 セグメント分けに利用する属性により次の種類が存在する。

  - **ポートベースVLAN**
      -
        [スイッチの接続ポートによりLANセグメントを分離する方式である](../Page/スイッチングハブ.md "wikilink")。

<!-- end list -->

  - **MACベースVLAN**
      -
        接続される機器の[MACアドレス](../Page/MACアドレス.md "wikilink")により所属するLANセグメントを分離する方式である。

<!-- end list -->

  - **サブネットベースVLAN**
      -
        接続される機器のIPアドレスのサブネットによりLANセグメントを分離する方式である。

<!-- end list -->

  - **プロトコルベースVLAN**
      -
        [IP](../Page/Internet_Protocol.md "wikilink")、[IPX](https://ja.wikipedia.org/wiki/Internetwork_Packet_Exchange "wikilink")、[AppleTalk](../Page/AppleTalk.md "wikilink")などの[ネットワークプロトコル](https://ja.wikipedia.org/wiki/ネットワークプロトコル "wikilink")によりLANセグメントを分離する方式である。Ethernet IIまたはIEEE 802.3x-1997におけるEther Type値を参照してイーサネットから見た上位レイヤのプロトコルを識別する。一つのインターフェースを複数のVLANに属させる事ができる。

<!-- end list -->

  - **タグVLAN**
      -
        イーサネットヘッダのSource MACとEthner Type/Sizeの間に識別タグ(VLANタグ)を挿入し、これによりLANセグメントを分離する方式である。[IEEE 802.1Qで規定されている](https://ja.wikipedia.org/wiki/IEEE_802.1Q "wikilink")。一つのインターフェースを複数のVLANに属させる事ができる。
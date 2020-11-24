> この記事は[Pentium D](https://ja.wikipedia.org/wiki/Pentium_D)から翻訳されています。


**Pentium D**（ペンティアムディー）は[2005年](../Page/2005年.md "wikilink")に[インテル](https://ja.wikipedia.org/wiki/インテル "wikilink")が発売した[x86](https://ja.wikipedia.org/wiki/x86 "wikilink")アーキテクチャの[マイクロプロセッサ](../Page/マイクロプロセッサ.md "wikilink")。

## 概要

1つのプロセッサの[パッケージに](../Page/パッケージ_\(電子部品\).md "wikilink")2つのCPUダイを実装する、いわゆるデュアルダイにより実現した[デュアルコアのCPUである](../Page/マルチコア.md "wikilink")。

[Pentium 4のCPUコアが流用されているが](../Page/Pentium_4.md "wikilink")、[Pentium Extreme Editionとの差別化を図るため](../Page/Pentium_Extreme_Edition.md "wikilink")「[ハイパースレッディング・テクノロジー](../Page/ハイパースレッディング・テクノロジー.md "wikilink") (HT)」は無効化されている。 [消費電力](https://ja.wikipedia.org/wiki/消費電力 "wikilink")と[発熱の点で](https://ja.wikipedia.org/wiki/熱 "wikilink")[NetBurstマイクロアーキテクチャ](../Page/NetBurstマイクロアーキテクチャ.md "wikilink")で1つのCPUコアでの性能向上が難しくなったことから、2つのCPUダイをワンパッケージに収めることにより熱問題を回避し、同時期に発売されたAMDのデュアルコア・プロセッサ製品へ対抗するという商品化意図がある。

[2006年](../Page/2006年.md "wikilink")の夏には消費電力と発熱の問題を解消し、さらに性能も十分に高い[Intel Core 2が発売され](../Page/Intel_Core_2.md "wikilink")、[メインストリーム](https://ja.wikipedia.org/wiki/メインストリーム "wikilink")としての役目を終えたが、生産は継続された。しかし[2007年](../Page/2007年.md "wikilink")[12月7日](../Page/12月7日.md "wikilink")をもって需要減のため受注が終了、その後は製造されていない([1](http://pc.watch.impress.co.jp/docs/2007/0810/intel2.htm))。市場からは後継となったCore 2 Duoなどの、デュアルコア化の先鞭を付けたCPUと位置付けられた。

なお、[Intel Core](../Page/Intel_Core.md "wikilink")、Intel Core 2の登場により、Pentium DはPentiumシリーズの最後のモデルとなると言われてきたが、Coreマイクロアークテクチャを採用した、Core 2 Duoシリーズの廉価版であるデュアルコアの「[Pentium Dual-Core](../Page/Pentium_Dual-Core.md "wikilink")」（旧Pentium E、現[Pentium](https://ja.wikipedia.org/wiki/Intel_Pentium_\(2010年\) "wikilink")）が2007年第2四半期に登場することにより、Pentiumブランドの延命がなされた。[Celeron Dual-CoreとCore](https://ja.wikipedia.org/wiki/Celeron#Celeron_Dual-Core "wikilink") 2 Duoの間を埋める製品である([2](http://www.behardware.com/news/8360/pentium-is-back.html))。

対応する[インテル　チップセットは](../Page/インテル_チップセット.md "wikilink")、

  - Intel 955X
  - Intel 945シリーズ
  - Intel 975X

である。

## 各世代の概要

### Smithfield（スミスフィールド）

2005年[5月26日](../Page/5月26日.md "wikilink")に投入された第一世代のPentium D。ベースとなるコアは90nmプロセスで製造される「Nocona」（ノコナ）で、2個の隣接したコアを1個のダイとしてシリコンウェハから切り出してパッケージに収めた製品。従来のNetBurst系までのIntelの[CPUバス](../Page/CPUバス.md "wikilink")は2個のCPUで共有する形態であるため、2個のCPUコアを1つのパッケージに収めるだけでデュアルコアCPUとして成立させることができる。このことは、デュアルコアCPUの完成・発売を急いでいたIntelにとって不幸中の幸いだったと言える。

EIST([Enhanced Intel SpeedStep Technology](../Page/Intel_SpeedStep_テクノロジ.md "wikilink"))は830と840で使用可能、軽負荷時には2.8GHzへクロックダウンされる。820は2.8GHz固定。[ソケット](../Page/CPUソケット.md "wikilink")[LGA775](https://ja.wikipedia.org/wiki/LGA775 "wikilink")。

  -
    {| border="1" cellpadding="5" class="wikitable"

|- align="center" \! プロセッサ・ナンバ \!\! 動作周波数
（x内部逓倍数） \!\! コア数\!\! FSB \!\! 2次キャッシュ \!\! [VT対応](../Page/インテル_バーチャライゼーション・テクノロジー.md "wikilink") \!\! HT対応 \!\!ソケット\!\! TDP \!\! s-spec(Core stepping)

|- | 840 || 3.20GHz (200x16) || 2 || 800MHz || 1MBx2 || × || × || LGA775 || 130W || SL88R(A0) SL8CM(B0) |- | 830 || 3.00GHz (200x15) || 2 || 800MHz || 1MBx2 || × || × || LGA775 || 130W || SL88S(A0) SL8CN(B0) |- | 820 || 2.80GHz (200x14) || 2 || 800MHz || 1MBx2 || × || × || LGA775 || 95W || SL88T(A0) SL8CP(B0) |- | 805 || 2.66GHz (133x20) || 2 || 533MHz || 1MBx2 || × || × || LGA775 || 95W || SL8ZH(B0)

|}

### Presler（プレスラ）

[2006年](../Page/2006年.md "wikilink")[1月5日](../Page/1月5日.md "wikilink")に投入された第二世代のPentium D。65nm版Pentium 4「Cedarmill」を[MCMで実装したものである](https://ja.wikipedia.org/wiki/Multi-Chip_Module "wikilink")。[L2キャッシュ](../Page/L2キャッシュ.md "wikilink")はSmithfieldと比較して、各コアにつき2MBの、合計4MBに拡張されている。

当初投入されたB-1ステップのコアではエラッタによりEISTやC1Eといった省電力機能が使用できないものがあった\[1\]が、後に投入されたC-1ステップのコアではこれらの省電力機能が有効化され、950や940などの比較的高クロックな製品でも[TDPが](../Page/熱設計電力.md "wikilink")130Wから95Wへと大きく引き下げられている。また最終のD-0ステップでは960のTDPも95Wへと減少している。

内部構造は、1ダイ2コアのSmithfieldと異なりパッケージには2ダイ2コアを実装している。これは製造[プロセスの微細化によってパッケージ側に](https://ja.wikipedia.org/wiki/集積回路#プロセス・ルール "wikilink")[配線](../Page/配線.md "wikilink")スペースが十分確保できず、1ダイ化が困難になってしまった為だと推測されている。プロセッサナンバーは900番台。

[VTと呼ばれる仮想化機能を搭載しない](https://ja.wikipedia.org/wiki/Intel_VT "wikilink")、廉価版（後述）が後に投入されている。

  -
    {| border="1" cellpadding="5" class="wikitable"

|- align="center" \! プロセッサ・ナンバ \!\! 動作周波数
（x内部逓倍数） \!\! コア数\!\! FSB \!\! 2次キャッシュ \!\! [VT対応](../Page/インテル_バーチャライゼーション・テクノロジー.md "wikilink") \!\! HT対応 \!\!ソケット\!\! TDP \!\! s-spec(Core stepping)

|- | 960 || 3.60GHz (200x18) || 2 || 800MHz || 2MBx2 || ○ || × || LGA775 || 130W(C1) 95W(D0) || SL9AP(C1) SL9K7(D0) |- | 950 || 3.40GHz (200x17) || 2 || 800MHz || 2MBx2 || ○ || × || LGA775 || 130W(B1) 95W(C1/D0) || SL94P(B1) SL8WP(B1) SL95V(C1) SL9K8(D0) |- | 945 || 3.40GHz (200x17) || 2 || 800MHz || 2MBx2 || × || × || LGA775 || 95W || SL9QB(C1) SL9QQ(D0) |- | 940 || 3.20GHz (200x16) || 2 || 800MHz || 2MBx2 || ○ || × || LGA775 || 130W(B1) 95W(C1) || SL8WQ(B1) SL94Q(B1) SL95W(C1) |- | 935 || 3.20GHz (200x16) || 2 || 800MHz || 2MBx2 || × || × || LGA775 || 95W || SL9QR(D0) |- | 930 || 3.00GHz (200x15) || 2 || 800MHz || 2MBx2 || ○ || × || LGA775 || 95W || SL8WR(B1) SL94R(B1) SL95X(C1) |- | 925 || 3.00GHz (200x15) || 2 || 800MHz || 2MBx2 || × || × || LGA775 || 95W || SL9D9(C1) SL9KA(D0) |- | 920 || 2.80GHz (200x14) || 2 || 800MHz || 2MBx2 || ○ || × || LGA775 || 95W || SL8WS(B1) SL94S(B1) |- | 915 || 2.80GHz (200x14) || 2 || 800MHz || 2MBx2 || × || × || LGA775 || 95W || SL9DA(C1) SL9KB(D0)

|}

  - 参考外部リンク
      - [ITmedia+D](http://plusd.itmedia.co.jp/pcupdate/articles/0601/06/news003.html)

## 性能について

[Pentium 4と同じく](../Page/Pentium_4.md "wikilink")[NetBurstマイクロアーキテクチャ](../Page/NetBurstマイクロアーキテクチャ.md "wikilink")からトランジスタが大幅増えたPrescott系と[リーク電流](../Page/リーク電流.md "wikilink")の大きい90nmのプロセスルールを採用しているため、発熱と[消費電力](https://ja.wikipedia.org/wiki/消費電力 "wikilink")がかなり大きい。そのため当初の800シリーズではシングルコア製品であるPentium 4と比較して、最上位品でも600MHzも低い[クロック](../Page/クロック.md "wikilink")での新製品発表となった。

しかしそれでもWillametteからトランジスタが増えたPrescott系のダイ2つを1つのCPUパッケージに収めることはかなり無理があり、発熱はコンシューマ向けではほぼ限界にまで達してしまった。特に830及び840においてはリテールクーラーを使用した場合、熱保護機能であるTM2が度々動作し、820と同等のクロックに落とされる事態が発生した。TM2は消費電力低下を主眼にした[EIST](https://ja.wikipedia.org/wiki/EIST "wikilink")と異なり、熱からCPUを保護し、破損を防ぐ為の緊急クロックダウン機能であり、Smithfieldの発熱量の大きさが分かる事例といえる。

65nmプロセスで製造される900シリーズでは消費電力の低減が期待されたが、当初リリースされたリビジョンではC1EとEISTという二つの省電力機能が[エラッタ](https://ja.wikipedia.org/wiki/エラッタ "wikilink")により使用できず、あまり大きな差は出ていない。それでも上位モデルではTDPが引き下げられ、800シリーズでは実現できなかった3.4GHz動作の製品がリリースされている。これらのエラッタを修正した後期のリビジョンで消費電力は大きく低減したものの、マーケティング的な理由もあり、クロックは3.6GHz（Pentium XEでは3.73GHz）がもっとも高い製品となっている。

製造原価としては大きな差があるPentium 4とほとんど変わらない価格設定がされている。これは、製造量が確保できずデュアルコア製品を明確にシングルコア製品の上に位置づけていた[AMDとは対照的な](https://ja.wikipedia.org/wiki/アドバンスト・マイクロ・デバイセズ "wikilink")[戦略](../Page/戦略.md "wikilink")で、発熱や[CPUファン](https://ja.wikipedia.org/wiki/CPUファン "wikilink")の[騒音](../Page/騒音.md "wikilink")、消費電力を許容できるならば[コストパフォーマンス](https://ja.wikipedia.org/wiki/コストパフォーマンス "wikilink")という意味では優れたものとなっている。

販売の低迷と、性能に自信を持つ後継となる[Core 2 Duoの発売を間近に控えていた為](../Page/Intel_Core_2.md "wikilink")、思い切った価格設定が可能であったとも言える。

## 脚注

<references group="脚注" />

## 関連項目

  - [NetBurstマイクロアーキテクチャ](../Page/NetBurstマイクロアーキテクチャ.md "wikilink")
  - [Pentium 4](../Page/Pentium_4.md "wikilink")
  - [Intel Core 2](../Page/Intel_Core_2.md "wikilink")
  - [Athlon 64 X2](../Page/Athlon_64_X2.md "wikilink") - Intel Core2 発売までの1年と四半期の間、市場で優位を保った。

## 外部リンク

  - [Intelのメインストリーム向けデュアルコア「Pentium D 820」～シングルコアCPU「Pentium 4 670」もリリース](http://pc.watch.impress.co.jp/docs/2005/0527/tawada53.htm) - [PC Watch](https://ja.wikipedia.org/wiki/PC_Watch "wikilink") 多和田新也のニューアイテム診断室（2005年5月27日）

[Category:インテルのマイクロプロセッサ](https://ja.wikipedia.org/wiki/Category:インテルのマイクロプロセッサ "wikilink")

1.  S-specがSL94で始まるものが該当する([3](http://download.intel.com/design/PentiumXE/specupdt/31030717.pdf))
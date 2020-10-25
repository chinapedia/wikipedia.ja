> この記事は[Geode](https://ja.wikipedia.org/wiki/Geode)から翻訳されています。


**Geode**（ジオード）は、[AMDの](https://ja.wikipedia.org/wiki/アドバンスト・マイクロ・デバイセズ "wikilink")[x86](https://ja.wikipedia.org/wiki/x86 "wikilink")アーキテクチャの[マイクロプロセッサ](../Page/マイクロプロセッサ.md "wikilink")。

主に[組み込みシステム](../Page/組み込みシステム.md "wikilink")市場向けをターゲットとしている。名称の「geode」は、英語で[鉱物](../Page/鉱物.md "wikilink")（主に[メノウ](../Page/メノウ.md "wikilink")）に空いた隙間や空洞、およびそれを含む[晶洞](https://ja.wikipedia.org/wiki/晶洞 "wikilink")石を意味する。

[ナショナル セミコンダクターが](../Page/ナショナル_セミコンダクター.md "wikilink")[1999年](../Page/1999年.md "wikilink")にリリース\[1\]したのが始まりで、[1997年](https://ja.wikipedia.org/wiki/1997年 "wikilink")にナショナル セミコンダクターが買収した[サイリックス](../Page/サイリックス.md "wikilink")の[MediaGX](../Page/MediaGX.md "wikilink")を受け継いで開発されたものである。[2003年](../Page/2003年.md "wikilink")[8月](../Page/8月.md "wikilink")にナショナル セミコンダクターの組み込み型のマイクロプロセッサの事業をAMDが買収した。その際に従来のMediaGX由来の製品の他、AMDの[Athlon](../Page/Athlon.md "wikilink")(K7アーキテクチャ)ベースの製品もGeodeブランドで販売されている。

## アーキテクチャ

元々は、第6世代に移行した[Cyrix](https://ja.wikipedia.org/wiki/Cyrix "wikilink")が、主流から外れることとなった第5世代製品の[Cx5x86を再利用し](../Page/Cyrix_Cx5x86.md "wikilink")、1995年に研究発表を行ない1997年に発売されたMediaGX(1995年の発表での名称は5GX86)に端を発する。

工場を持たない、いわゆる[ファブレスメーカー](https://ja.wikipedia.org/wiki/ファブレスメーカー "wikilink")であるCyrixは、当時[ナショナル セミコンダクターに製造の](../Page/ナショナル_セミコンダクター.md "wikilink")[委託](https://ja.wikipedia.org/wiki/委託 "wikilink")を行っていた。Cyrixは5GX86をMediaGXに改称した後、業績不振などを理由にCyrix自身を[ナショナル セミコンダクターに身売した](../Page/ナショナル_セミコンダクター.md "wikilink")。

今まで薄利多売の製品を主流としていたナショナル セミコンダクターは、高収益が得られる可能性のある一方で激しい市場競争に晒される[デスクトップPC向けプロセッサを避け](../Page/デスクトップパソコン.md "wikilink")、その製品であるMIIなど、[Pentium IIと競合関係にあるCPU開発部門を](../Page/Pentium_II.md "wikilink")[VIAに売却した](../Page/VIA_Technologies.md "wikilink")。残った[セットトップボックス](../Page/セットトップボックス.md "wikilink")向けの製品としてMediaGXの販売を行い、後の製品で**Geode**と改称した。

MediaGXの流れを組むGeodeは、[IA-32](../Page/IA-32.md "wikilink")[命令セット](../Page/命令セット.md "wikilink")を採用しながら[プロセスルールの更新に後押しされ](https://ja.wikipedia.org/wiki/集積回路#プロセス・ルール "wikilink")、消費電力と製造原価が低く抑えられた、主に組み込み向けとなるプロセッサである。 なお、その性能は現在のPCや[サーバ](../Page/サーバ.md "wikilink")向けプロセッサと比較すると低い。[Geode NXを除くGeodeの原型であるMediaGXの](https://ja.wikipedia.org/wiki/#Geode_NX "wikilink")、更にベースとなるのはIntel社の[Pentium](https://ja.wikipedia.org/wiki/Pentium "wikilink")互換・競合プロセッサである[Cx6x86やCx](https://ja.wikipedia.org/wiki/Cyrix_6x86 "wikilink")5x86であり、MediaGXの性能は同等クロックのPentiumプロセッサと、一長一短あるが同程度であるため。現状のGeodeの性能もGeodeNXを除き、単純な比較はできないがMediaGX/GXmの発展形に準ずるものである。

なおCyrix 5x86/6x86の[アーキテクチャ](../Page/アーキテクチャ.md "wikilink")は、第5世代のx86プロセッサであるPentiumと共通点が多く、また一部には第6世代である[Pentium Proの要素も先取りしたものとなっている](../Page/Pentium_Pro.md "wikilink")。

その後、ナショナル セミコンダクターは、[AMDがラインナップ拡充のために低消費電力のx](https://ja.wikipedia.org/wiki/アドバンスト・マイクロ・デバイセズ "wikilink")86プロセッサを必要としていたことから、GeodeをAMDに売却した。

初期のプロセッサでは[MMX](../Page/MMX.md "wikilink")や[3DNow\!](../Page/3DNow!.md "wikilink")などの[SIMD](../Page/SIMD.md "wikilink")に対応しなかったが、MediaGXmからは、[MMX](../Page/MMX.md "wikilink")に対応し、[Geode GX以降では](https://ja.wikipedia.org/wiki/#Geode_GX "wikilink")、[3DNow\!](../Page/3DNow!.md "wikilink")と[MMX](../Page/MMX.md "wikilink")に対応している、Geode NXでは[3DNow\! Professional搭載によりSSEにも対応している](https://ja.wikipedia.org/wiki/3DNow!_Professional "wikilink")。一般的なIA-32のCPUでは別々のチップセット（例えば[ノースブリッジ](../Page/ノースブリッジ.md "wikilink")）で提供される機能を1チップに統合([SoC](../Page/System-on-a-chip.md "wikilink"))している製品が存在することも大きな特徴である。

[シンクライアント](../Page/シンクライアント.md "wikilink")、[インターネットテレビ](../Page/インターネットテレビ.md "wikilink")や[組み込みシステム](../Page/組み込みシステム.md "wikilink")に最も適切な組み合わせであるとされる。さらに[The Children's MachineにGeodeのシリーズの一つであるGeode](https://ja.wikipedia.org/wiki/The_Children's_Machine "wikilink") GXが使われている(BTest-3以降は改良型の[Geode LXに移行](https://ja.wikipedia.org/wiki/#Geode_LX "wikilink"))。

その後、PC向けプロセッサが第7世代のK7マイクロアーキテクチャから第8世代のK8マイクロアーキテクチャに移行した後、製造がこなれて低消費電力化されたK7マイクロアーキテクチャ製品のGeode NXも発売された。 Geode NXは、その実態はThoroughbred(サラブレッド)コアのモバイル[Athlon](../Page/Athlon.md "wikilink")XP-Mと同一である。

その後、組み込み向けの[AMD Fusion](https://ja.wikipedia.org/wiki/AMD_Fusion "wikilink") APU（Gシリーズ）が発表され、G-T16R APUでGeode NXを置き換える事になっている。

## Geodeのシリーズ

### Geode GX

[thumb](https://ja.wikipedia.org/wiki/ファイル:Geode_GX1_233.jpg "wikilink") [サイリックス](../Page/サイリックス.md "wikilink")で開発されていた[x86](https://ja.wikipedia.org/wiki/x86 "wikilink")互換CPU、[MediaGX](../Page/MediaGX.md "wikilink")を基本設計とした上で開発した製品。超低消費電力が特徴。

製造技術は[ナショナル セミコンダクターに一度買収されたが](../Page/ナショナル_セミコンダクター.md "wikilink")、2006年現在では[アドバンスト・マイクロ・デバイセズ](https://ja.wikipedia.org/wiki/アドバンスト・マイクロ・デバイセズ "wikilink") (AMD) がこのCPU部門を買収して開発・販売を行っている。 Geodeシリーズは主に組込み製品に用いられることが多かったが、[One Laptop Per Child](../Page/OLPC.md "wikilink") (OLPC) プロジェクトの[100ドルノートPCに搭載されるCPUとして採用されたことで注目が集まっている](https://ja.wikipedia.org/wiki/The_Children's_Machine "wikilink")(BTest-3以降は[Geode LXに移行](https://ja.wikipedia.org/wiki/#Geode_LX "wikilink"))。 また、かつて[カシオ計算機](../Page/カシオ計算機.md "wikilink")製のノートPC [CASSIOPEIA](../Page/カシオペア_\(コンピュータ\).md "wikilink") FIVAシリーズ (MPC-103)でも使用されていた。

  - 特長

<!-- end list -->

  - 32ビット超低消費電力x86アーキテクチャ、[MMX](../Page/MMX.md "wikilink")拡張命令と[3DNow\!](../Page/3DNow!.md "wikilink")拡張命令をサポート
  - 32KBのレベル1キャッシュを搭載
  - GeodeLinkアーキテクチャを採用
  - ディスプレイコントローラーを内蔵（[GPUを統合](../Page/Graphics_Processing_Unit.md "wikilink")）
  - 動作周波数 200～300MHz

[thumb](https://ja.wikipedia.org/wiki/ファイル:AMD_Geode_LX_800_CPU.jpg "wikilink")

-----

### Geode LX

[x86アーキテクチャ互換](../Page/IA-32.md "wikilink")[CPU](../Page/CPU.md "wikilink")。Geodeシリーズのミドルレンジグレード（中間的なCPU性能）製品である。AMD製品としては、[Cyrix](https://ja.wikipedia.org/wiki/Cyrix "wikilink")社の[MediaGX](../Page/MediaGX.md "wikilink")の流れを汲む"[Geode GX](https://ja.wikipedia.org/wiki/#Geode_GX "wikilink")"が存在するが、あらゆる情報処理用途の電気製品にx86アーキテクチャを使用できるようにするため、さらに処理能力の高い、極超低消費電力システムの組めるCPUとして開発された。

0.13μmのプロセスルールで製造され、動作電圧は1.2V、LX 800でチップ全体のTDP（[熱設計消費電力](https://ja.wikipedia.org/wiki/熱設計消費電力 "wikilink")）は平均値で1.6W、最大で2.4W\[2\]。システムによっては放熱ファン無しで用いることができる。チップとしてはCPU部分と[ノースブリッジ](../Page/ノースブリッジ.md "wikilink")、グラフィックが統合されており、CPU部分のみの消費電力はLX 800で平均値で0.9Wとされている。

DDR-SDRAM対応のメモリコントローラ、2Dグラフィック、PCIブリッジなどの機能を1チップ内に統合されているが、別途[サウスブリッジ](../Page/サウスブリッジ.md "wikilink")にあたる「CS5536コンパニオンチップ」が用意されている。

OSは、[MS-DOS](../Page/MS-DOS.md "wikilink")，[Windows](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")，[Linux](../Page/Linux.md "wikilink")などが動作する。[Windows XP上では](../Page/Microsoft_Windows_XP.md "wikilink")[ウェブブラウズ](https://ja.wikipedia.org/wiki/ネットサーフィン "wikilink")、[オフィスアプリケーションなどの通常用途では快適に利用できる](../Page/オフィススイート.md "wikilink")。しかし、超低消費電力を重視したCPU性能が理由で3Dゲーム、動画閲覧などCPUパワーが必要な用途にて使うと処理落ちなどが発生する為、その利用には支障が出やすい。また、[Windows Vistaでは内蔵GPUの能力不足のため利用不可といわれる](https://ja.wikipedia.org/wiki/Microsoft_Windows_Vista "wikilink")。

なお、競合製品として、[VIA](../Page/VIA_Technologies.md "wikilink") [C3](../Page/VIA_C3.md "wikilink") （組み込み用途向け）、[Intel Atomシリーズ](../Page/Intel_Atom.md "wikilink") （コンシューマ向け） がある。

  - ラインナップ
    CPU

| モデルナンバー     | クロック周波数 | 消費電力                      |
| ----------- | ------- | ------------------------- |
| LX 900@1.5W | 600MHz  | 最大5.1W (TDP max) , 通常2.6W |
| LX 800@0.9W | 500MHz  | 最大3.6W (TDP max) , 通常1.8W |
| LX 700@0.8W | 433MHz  | 最大3.1W (TDP max) , 通常1.3W |
| LX 600@0.7W | 366MHz  | 最大2.8W (TDP max) , 通常1.2W |

  - コンパニオンデバイス

<!-- end list -->

  - CS5536

<!-- end list -->

  - 主な用途

上記のとおり、シンクライアント、機器組み込みがメインとなっており、コンシューマ向け製品への適用例は少ない。

  - [KOHJINSHA SAシリーズ](../Page/KOHJINSHA_SA.md "wikilink")
  - [OLPC XO-1](https://ja.wikipedia.org/wiki/OLPC_XO-1 "wikilink")

-----

### Geode NX

[2004年](../Page/2004年.md "wikilink")[5月24日](../Page/5月24日.md "wikilink")に発表された。[ノートパソコン](../Page/ノートパソコン.md "wikilink")向けCPU、[モバイルAthlon XP-M](https://ja.wikipedia.org/wiki/Athlon#モバイルAthlon_XP-M "wikilink") (Thoroughbred) をベースに、[消費電力](https://ja.wikipedia.org/wiki/消費電力 "wikilink")・発熱量を抑えたものである。

266MHz [FSB](../Page/フロントサイドバス.md "wikilink")、128KB 1次 / 256KB 2次キャッシュメモリを備え、[SIMD](../Page/SIMD.md "wikilink")拡張命令セット[3DNow\! Professionalや](https://ja.wikipedia.org/wiki/3DNow!#3DNow!_Professional "wikilink")、[省電力技術](../Page/省エネルギー.md "wikilink")[PowerNow\!](../Page/PowerNow!.md "wikilink")をサポート。 対応ソケットは[Athlon](../Page/Athlon.md "wikilink")・[Duron](../Page/Duron.md "wikilink")シリーズなどと同じ[Socket A](https://ja.wikipedia.org/wiki/Socket_A "wikilink")。 なお、マザーボードによってはAthlon XP-Mと同様に、[デュアルプロセッサ構成も可能である](../Page/マルチプロセッシング.md "wikilink")。

Geode NXファミリの各製品には[モデルナンバー](../Page/モデルナンバー.md "wikilink")が与えられている。Geode NXは内部的には[モバイルAthlon XP-Mの](https://ja.wikipedia.org/wiki/Athlon#モバイルAthlon_XP-MP "wikilink")(超)低電圧版に他ならないが、モバイルAthlon XP-Mのモデルナンバーとの共通性は無い。事実上対抗製品となる[VIA C3プロセッサを強く意識したものである](../Page/VIA_C3.md "wikilink")。ちなみにこのモデルナンバーの @ の右側に付されている数字とWは、消費電力を表す。

| モデルナンバー  | クロック周波数 |
| -------- | ------- |
| 1750@14W | 1.4GHz  |
| 1500@6W  | 1.0GHz  |
| 1250@6W  | 667MHz  |

Geode NX ラインナップ

## 出典

## 外部リンク

  - [AMD Geode ソリューション](http://www.amd.com/jp-ja/ConnectivitySolutions/ProductInformation/0,,50_2330_9863,00.html)

  - [AMD Geode GX 533@1.1Wプロセッサ](http://www.amd.com/jp-ja/ConnectivitySolutions/ProductInformation/0,,50_2330_9863_9864,00.html)[タイトル](http://example.org/)

  - [AMD Geode LX](http://www.amd.com/jp-ja/ConnectivitySolutions/ProductInformation/0,,50_2330_9863_13022,00.html)[タイトル](http://example.org/)

  - [AMD Geode NX プロセッサ・ファミリ](http://www.amd.com/jp-ja/ConnectivitySolutions/ProductInformation/0,,50_2330_9863_10837,00.html)[タイトル](http://example.org/)

  -
<!-- end list -->

  - [シンクライアント端末](http://www.logitec.co.jp/press/2008/0227_01.html) - ロジテック社報道資料

[Category:AMDのマイクロプロセッサ](https://ja.wikipedia.org/wiki/Category:AMDのマイクロプロセッサ "wikilink")

1.
2.  Geodeシリーズ製品発表記事 ([Impress](http://pc.watch.impress.co.jp/docs/2005/0615/amd.htm), [マイコミジャーナル](https://news.mynavi.jp/news/2005/05/23/003.html)) による
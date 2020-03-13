> この記事は[Crusoe](https://ja.wikipedia.org/wiki/Crusoe)から翻訳されています。


[thumb](https://ja.wikipedia.org/wiki/ファイル:Transmeta_crusoe_tm5600_2.jpg "wikilink") **Crusoe**（クルーソー）は、[トランスメタ](../Page/トランスメタ.md "wikilink")が開発した[x86](https://ja.wikipedia.org/wiki/x86 "wikilink")互換[マイクロプロセッサ](../Page/マイクロプロセッサ.md "wikilink")である。ここでは後継プロセッサである**Efficeon**（イフィシオン）についても述べる。

## Crusoe

名称は『漂流記』の主人公[ロビンソン・クルーソー](https://ja.wikipedia.org/wiki/ロビンソン・クルーソー "wikilink")に由来する。設計・発売元の[トランスメタ](../Page/トランスメタ.md "wikilink")についてはそちらの記事を参照のこと。同社はいわゆるファブレスであり、製造は社外への委託であった。

最大の特徴はx86命令をCrusoeの[ハードウェア](../Page/ハードウェア.md "wikilink")では[デコードせず](https://ja.wikipedia.org/wiki/エンコード#デコード "wikilink")、「コードモーフィングソフトウェア (CMS4.1)」がx86命令をCrusoeのネイティブの[VLIW](../Page/VLIW.md "wikilink")命令に動的に変換する点である。この点で、発表当初は同時期に開発された[インテル](https://ja.wikipedia.org/wiki/インテル "wikilink")の[Itanium](../Page/Itanium.md "wikilink")とVLIW（Itaniumでは発展形の[EPICアーキテクチャ](../Page/EPICアーキテクチャ.md "wikilink")）の実装方法について比較されることがあった。また、[CPU](../Page/CPU.md "wikilink")負荷に応じて動的にCPUのクロック周波数を高低する**LongRun**技術を採用し、同CPUの消費電力の低減に貢献している。

### 第1世代Crusoe

[2000年](../Page/2000年.md "wikilink")に発売された「TM5400/5600」ではPCの[ノースブリッジ](../Page/ノースブリッジ.md "wikilink")チップを統合している。ただし[AGPには対応していない](../Page/Accelerated_Graphics_Port.md "wikilink")。主に[組み込み向け用途を狙ったCPUであるが](../Page/組み込みシステム.md "wikilink")、発表当初は、まだ他社製CPUに低消費電力向けのものがなかったため、[ソニー](../Page/ソニー.md "wikilink")、[NEC](../Page/日本電気.md "wikilink")、[富士通](../Page/富士通.md "wikilink")、[東芝](../Page/東芝.md "wikilink")、[カシオなど特に日本市場向けの各社のモバイル向け](../Page/カシオ計算機.md "wikilink")[ノートパソコン](../Page/ノートパソコン.md "wikilink")などに広く採用された。しかし、初回のアプリケーション起動時にはコードモーフィング処理を行うため、（2回目の起動からは多少速くなるというアナウンスだったものの）パフォーマンスは同[クロック](../Page/クロック.md "wikilink")周波数の他社製CPUと[ベンチマーク](../Page/ベンチマーク.md "wikilink")などで比較すると60%程度で、明らかに見劣りするものだった。またノートパソコン全体の消費電力を左右するのはCPUだけではなかった。発売当初、各CPUのCMSは[フラッシュメモリ](../Page/フラッシュメモリ.md "wikilink")に書き込まれていてバージョンアップ時に変更が可能とされていたが、修正版は一般にはリリースされていない。

### 第2世代Crusoe

[2002年](../Page/2002年.md "wikilink")にはCMS4.2にバージョンを上げ、クロック周波数を向上して、パフォーマンスを改善した「TM5800」を発売した。これらはノートパソコン以外に、[タブレットPC](../Page/タブレットPC.md "wikilink")や[ブレードサーバ](../Page/ブレードサーバ.md "wikilink")への採用も期待された。もっとも、[2003年](../Page/2003年.md "wikilink")にインテルが対抗して低消費電力のCPU ([Pentium M](../Page/Pentium_M.md "wikilink")) を出荷したことや、製造先を[IBM](../Page/IBM.md "wikilink")から[TSMC](../Page/TSMC.md "wikilink")に変更したものの度重なる製造遅延などでクロックスピードを上げることができず、CPUパフォーマンスを上げることができなかったことなどから、各社のノートパソコンでの採用数は徐々に減少することになる。

### Crusoeを採用した主なパソコン

  - [NEC](../Page/日本電気.md "wikilink") - [LaVie](https://ja.wikipedia.org/wiki/LaVie "wikilink")MX、LavieZ 駆動時間を延ばすために取り外し型バッテリのほかに[LCD](https://ja.wikipedia.org/wiki/LCD "wikilink")（反射型または半透過型）の裏にも取り外し不可のバッテリを実装していた。
  - [富士通](../Page/富士通.md "wikilink") - [FMV](../Page/FMV.md "wikilink")-BIBLO LOOX
  - [ソニー](../Page/ソニー.md "wikilink") - [VAIO](../Page/VAIO.md "wikilink") PCG-C1VJシリーズ、PCG-GT3、PCG-U1等
  - [カシオ](../Page/カシオ計算機.md "wikilink") - [CASSIOPEIA](../Page/カシオペア_\(コンピュータ\).md "wikilink") FIVA（MPC-205/206/206VL/216XL/225/701）
  - [シャープ](../Page/シャープ.md "wikilink") - [Mebius](../Page/Mebius.md "wikilink")ノート PC-SX1-H1 PC-MM1シリーズ
  - [東芝](../Page/東芝.md "wikilink") - [Libretto](../Page/リブレット_\(パーソナルコンピュータ\).md "wikilink") L1、L2、L3、L5
  - [日立製作所](../Page/日立製作所.md "wikilink") - [FLORA](https://ja.wikipedia.org/wiki/FLORA "wikilink") 220TX、210W NL3 （企業向け）210W NL3はシャープのPC-MM1シリーズとほぼ同一の設計だが、BIOSや、パーツの実装などが一部異なる。
  - [OQO](../Page/OQO.md "wikilink") - アメリカで超小型PCを開発、発売

このほか、[IBM](../Page/IBM.md "wikilink")もCrusoeを搭載したノートパソコン（[ThinkPad](../Page/ThinkPad.md "wikilink")）を試作、展示したことがあったが、目標とした連続駆動時間を実現できず、開発は中止された\[1\]。

## Efficeon

[thumb](https://ja.wikipedia.org/wiki/ファイル:Transmeta_Efficeon_TM8600_1GHz.jpg "wikilink") [thumb](https://ja.wikipedia.org/wiki/ファイル:Sharp_PC-MM2-5NE.jpg "wikilink") [2004年](../Page/2004年.md "wikilink")、次世代プロセッサ「Astro」の[コードネーム](../Page/コードネーム.md "wikilink")で呼ばれていた「TM8000」（現「Efficeon（イフィシオン）」）が発売された。製造は当初TM8600シリーズについては[TSMC](../Page/TSMC.md "wikilink")で行われたが、製造プロセスを90nmに切替えたTM8800シリーズについては[富士通](../Page/富士通.md "wikilink")あきるの工場で行われている。 VLIWでの実行命令数を倍にするなど内部設計を一新したことでパフォーマンス面では同クロック周波数のPentium系CPUの80%～90%程度と大きく改善した。 Crusoe同様ノースブリッジ相当の機能を内蔵しており、AGPにも対応している。ただし同時に発表された**LongRun2**技術は採用されておらず、消費電力はCrusoeより若干上昇した程度である。ノートパソコンでの採用はシャープの一部の製品のみにとどまり（その他の携帯型ノートパソコンはシャープ含めて全社ともPentium Mの採用にシフトしてしまった）、同チップを採用した[ファンレスPC](https://ja.wikipedia.org/wiki/ファンレスPC "wikilink")や[ベアボーンキット](../Page/ベアボーンキット.md "wikilink")も存在するが、他社製CPU搭載の製品に対して若干高価である。

各社がPentium Mにシフトしたことで、市場への復活は無いと思われたEfficeonだったが、Spring Processor Forum 2006にて行われたTransmetaの**LongRun2**についてのプレゼンにて**「LongRun2実装版Efficeon」**が作成された事が判明し、何らかの形でEfficeonが、再度市場へ登場することが期待された。

また、[マイクロソフト](../Page/マイクロソフト.md "wikilink")のプリペイドPCサービス「FlexGO」専用の機能を持つCPUとしてEfficeonを拡張したものが使用されている他、[サムスン製の](../Page/サムスン電子.md "wikilink")[Windows XP搭載の携帯電話端末SPH](../Page/Microsoft_Windows_XP.md "wikilink")-P9000にもTM8820が搭載されているとのことである。

### Efficeonを採用した主なパソコン

  - [シャープ](../Page/シャープ.md "wikilink") - [Mebius](../Page/Mebius.md "wikilink") MURAMASA MM2/MM50/MM70/CV(TM8600 1.0GHz) MP40H(TM8800 1.4GHz) MP50G/MP60GS/MP70G(TM8800 1.6GHz)
  - [イーレッツ](https://ja.wikipedia.org/wiki/イーレッツ "wikilink") - Be Silent Mt6600(TM8600 1.0GHz)
  - [HP](../Page/ヒューレット・パッカード.md "wikilink") - t5710(TM8600 1.2GHz)

## その他

トランスメタはLongRun2の技術供与を富士通、[NEC](../Page/日本電気.md "wikilink")、[ソニー](../Page/ソニー.md "wikilink")などの各メーカーに対して行っている。

起業から赤字続きだったトランスメタは[2005年](../Page/2005年.md "wikilink")、チップ製造業者から知的財産ライセンス企業へと方向転換を図る戦略を発表し、その後、大規模な[リストラ](../Page/リストラ.md "wikilink")を行った。また、香港のCulturecomへのCrusoeに関する技術資産の売却とEfficeonの技術ライセンスの提供を発表した。それらの結果、同年には初の黒字化を達成している。Culturecomとの契約は[2006年](../Page/2006年.md "wikilink")[2月](https://ja.wikipedia.org/wiki/2月 "wikilink")、米国政府の技術輸出規制により終了（解消）している。

### 後に続いたもの

当時、インテルも[AMDもクロック戦争の真っ只中にあり](https://ja.wikipedia.org/wiki/アドバンスト・マイクロ・デバイセズ "wikilink")、どちらが先に「1GHzの大台」を越すのかの争いを演じていた。しかし、クロックの上昇は「処理性能の向上」と同時に「消費電力の増大」を意味しており、バッテリー容量の制約があるノートパソコンのメーカーにとってこれは大きな問題であった。特に、ビジネスにおけるモバイルPCの需要が世界で最も大きい日本においては、バッテリーによる駆動時間は重要な問題として捉えられ、この解決案の1つとしてCPUに消費電力の低いCrusoeを採用するメーカーが増えた。

#### インテルへの影響

Crusoeの開発アナウンスに対しインテルは危機感を抱き、[2001年](../Page/2001年.md "wikilink")低電圧版と超低電圧版のMobile[Pentium IIIを開発し市場に投入した](../Page/Pentium_III.md "wikilink")。これらは、通常のMobile Pentium IIIの[シリコンウェハー](../Page/シリコンウェハー.md "wikilink")から、より低い電圧でも動作する優良な個体を選別した製品である。選別品である為、動作クロックは低くとも低電圧版および超低電圧版の価格は標準的な製品よりも高い設定が行われた。

その後、インテルのモバイルCPUにおいては、2002年よりデスクトップ版と同じ[NetBurstマイクロアーキテクチャ](../Page/NetBurstマイクロアーキテクチャ.md "wikilink")を採用した[Pentium 4-Mシリーズが発表されたが](../Page/Pentium_4-M.md "wikilink")、TDPに問題をかかえており本来の性能を発揮できないものだった。2003年より発売された[Pentium Mでは](../Page/Pentium_M.md "wikilink")[P6マイクロアーキテクチャ](../Page/P6マイクロアーキテクチャ.md "wikilink")が採用され、クロックは低いものの**電力あたりの処理能力**の高いCPUとなった。[ネットブック](https://ja.wikipedia.org/wiki/ネットブック "wikilink")に搭載されているインテルのA100、[Intel Atomシリーズも](https://ja.wikipedia.org/wiki/Intel_Atom "wikilink")、[Pentium Mの系譜を受け継いでおり](../Page/Pentium_M.md "wikilink")、非常に低い電力で動作している。

一方、デスクトップCPUにおけるクロック戦争はより長く続いた。インテルのCPUは[Pentium 4において](../Page/Pentium_4.md "wikilink")3GHz後半までその性能を向上させたものの、消費電力の増大に伴う熱問題から行き詰まりを見せる。クロック上昇の連続による性能向上に限界を悟ったインテルは、2005年発売の[Pentium Dにおいて物理CPUの複数コア化による性能向上を目指した](../Page/Pentium_D.md "wikilink")。しかし、Pentium 4のCPUコアを流用して2つパッケージにしたために、熱問題が深刻化してしまう。そこで、消費電力が低く、熱問題が発生しにくい[Pentium Mに目をつけた](../Page/Pentium_M.md "wikilink")。2006年に[Pentium Mを元にして改良し](../Page/Pentium_M.md "wikilink")、デュアルコアにした[Intel Core 2シリーズを発売し](../Page/Intel_Core_2.md "wikilink")、**電力あたりの処理能力**の高いデスクトップCPUとして発売。成功を収めたといえる。

Transmetaはインテルの企業力により業績悪化を余儀なくされ、主要事業を半導体の開発販売から開発した知的所有権のライセンス提供に移行させていった。ただ、**性能の低減を抑えつつ消費電力を節減する**というアイディアを持ったCPUは、当時としては画期的であり、その後のインテルのCPUに間接的ながら大きな影響を与えた。CPUのクロック周波数を高低することにより消費電力を低減する[EIST](https://ja.wikipedia.org/wiki/EIST "wikilink")というインテルの技術は、LongRun技術のアイディアと同じものであり、トランスメタは2006年にインテルを特許権の侵害で訴えている（後にインテルが金銭を払うことで和解）。

#### AMDへの影響

[2004年](../Page/2004年.md "wikilink")、AMDは1GHz競争終了後に自らはしごを外す形で「省電力・高効率」方向にシフトしつつあった。そして対抗のために以前から開発していた[K7シリーズの一部をNational](../Page/Athlon.md "wikilink") Semiconductorから買収した省電力プロセッサのブランドGeodeを冠したGeode NXと命名し、投入した。その後、AMD-K8アーキテクチャの低電力ソリューションとしてOpteron EE / 同HE、[Turion 64を発売した](../Page/Turion_64.md "wikilink")。

## 脚注

## 外部リンク

  - [Transmeta Crusoe Processor](http://www.transmeta.com/crusoe/index.html) （英語）
  - [低消費電力CPUと言えば、忘れちゃいけないTransmeta](http://ascii.jp/elem/000/000/534/534445/) ASCII.jp(トランスメタの製品ロードマップの歴史を紹介している）

[Category:マイクロプロセッサ](https://ja.wikipedia.org/wiki/Category:マイクロプロセッサ "wikilink")

1.  [Crusoe搭載ノートPC中止と謎のCPUとの関係は? 日本IBMへのインタビュー](http://news.mynavi.jp/news/2000/11/06/03.html) - マイナビニュース 2000年11月6日
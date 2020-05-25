> この記事は[Accelerated Graphics Port](https://ja.wikipedia.org/wiki/Accelerated_Graphics_Port)から翻訳されています。


[thumb上のAGPスロット](https://ja.wikipedia.org/wiki/ファイル:AGP_slot_highlighted_on_Soyo_SY-7VBA133_mainboard.jpg "wikilink")\]\] **Accelerated Graphics Port**（アクセラレーテッド グラフィックス ポート、**AGP**）とは、[インテル](https://ja.wikipedia.org/wiki/インテル "wikilink")が策定した[ビデオカード](../Page/ビデオカード.md "wikilink")用の[拡張ポート規格である](https://ja.wikipedia.org/wiki/拡張バス "wikilink")。

## 概要

インテルの[Pentium II](../Page/Pentium_II.md "wikilink")・[Celeron](https://ja.wikipedia.org/wiki/Celeron "wikilink")用[Slot 1対応](../Page/Slot_1.md "wikilink")[チップセット](../Page/チップセット.md "wikilink")であるIntel 440LXでAGP 1.0が初採用され、以後、後継規格である[PCI Expressが制定](../Page/PCI_Express.md "wikilink")・実用化されるまでパーソナル・コンピューターを中心に利用された。

信号プロトコルは32ビット 66MHz動作の[PCIバスのそれを基本としつつ](../Page/Peripheral_Component_Interconnect.md "wikilink")、同バスでデータバスと時分割により共用とされていたアドレスバスを8ビット幅で別途用意し、必要に応じて両バスを分離可能\[1\]とするサイドバンドアドレッシング機能や、CPUを介せず直接[グラフィックコントローラ](../Page/グラフィックコントローラ.md "wikilink")でメインメモリの読み書きを可能とするDIME (DIrect Memory Execution) 機能を搭載する。

サイドバンドアドレッシング機能とDIME機能は共に本ポートに接続されるグラフィックコントローラからパソコン本体の[メインメモリへのアクセスを高速化するためのものである](../Page/主記憶装置.md "wikilink")。これらは当初、メインメモリを[テクスチャ](https://ja.wikipedia.org/wiki/テクスチャ "wikilink")や[Zバッファ](../Page/Zバッファ.md "wikilink")やバックプレーンとして使用することによって、ビデオカードに搭載されるビデオメモリ\[2\]の搭載量を必要最小限で済ませ、一定の描画性能を確保しつつ低コスト化を図る目的で開発された\[3\]。だが、規格制定と前後してWindows搭載パソコンでの3Dグラフィック機能の搭載が急速に進展したことから、そうした低コストパソコンへの適用とは別に、[ポリゴン](../Page/ポリゴン.md "wikilink")による3Dグラフィック機能をサポートするグラフィックコントローラにおいて、大容量テクスチャメモリをメインメモリ上に確保する手段として賞揚され\[4\]、[下位機種から](https://ja.wikipedia.org/wiki/ローエンド "wikilink")[上位機種まで幅広く普及するに至った](https://ja.wikipedia.org/wiki/ハイエンド "wikilink")。

最初のバージョンであるAGP 1.0は[1996年](../Page/1996年.md "wikilink")8月に策定され、[1997年](https://ja.wikipedia.org/wiki/1997年 "wikilink")夏頃から製品が出回るようになった\[5\] 。

もっとも、本ポートが製品レベルで現役であった当時の大多数のPCで使用されていたWindows 9xやWindows 2000・Windows XPなどにおいて、恒常的に最も多く使用されていたアプリケーションソフトである[オフィスソフトを使用する場合に限って言えば](../Page/オフィススイート.md "wikilink")、PCIバス接続のグラフィックコントローラで十分であった。実際にも、本ポートの登場に先行して実用化が始まっていた、メインメモリの一部をビデオメモリとして共有する[IGP](../Page/Integrated_Graphics_Processor.md "wikilink")=[統合チップセットを利用するPCは](https://ja.wikipedia.org/wiki/チップセット#統合チップセット "wikilink")、本ポートの普及後もそうしたビジネス用PCを中心に多数販売され続けている。

これは、オフィスソフトでは高度な3D処理は必要とせず、また、高速に描画を行い大量のデータをやり取りする時間よりも、人の手で入力する時間が作業の殆どを占めており、画面の書き換えについても文字を毎秒数文字（または、毎分数文字）書き換える程度の処理が殆どであったためである\[6\]。

上述の通りAGPは32ビットPCIの上位互換機能を備えており、適切な[デバイスドライバ](../Page/デバイスドライバ.md "wikilink")が存在しない場合、本ポートに接続されたグラフィックコントローラは32ビット 66MHzのPCIバスに接続されているのと同等の動作を行う\[7\]。

後年、大量のメモリをビデオカードに実装するようになると、ビデオカードのメモリアクセスはビデオカード内で完結することも多くなり、メインメモリへのアクセス向上という意義はやや薄れた。だが、この時期には3Dゲームを中心に本ポート経由でやりとりされるデータそのものが急増しており、その要求に応える形で本ポートは規格の拡張・性能向上が繰り返された。これにより、基本となる1xモード (266MB/s) の機能に加えて信号の低電圧差動を行い、さらにクロック信号の立ち上がりに加え、立ち下がり、待ち時間などを検出することで同一クロックタイミングのまま転送速度を2倍・4倍・8倍と高速化させるAGP 2xモード (533MB/s) ・4xモード (1,067MB/s) ・8xモード (2,133MB/s) が開発されている。

## 規格のバージョンと互換性

AGPはこれまでに3つの規格がリリースされ\[8\]\[9\]\[10\]、諸元は以下の表の通りである。

|             | AGP 1.0 | AGP 2.0         | AGP 3.0         |
| ----------- | ------- | --------------- | --------------- |
| 策定年月        | 1996年8月 | 1998年5月         | 2002年9月         |
| 信号電圧        | 3.3V    | 1.5V            | 0.8V            |
| 速度          | 1x,2x   | 1x,2x,4x        | 4x,8x           |
| 切り欠き（突起）の位置 | 3.3V    | 1.5V, Universal | 1.5V, Universal |

AGP規格の各リリース

より高速な動作モードを備えたリリースであるほど、[スルー・レート](https://ja.wikipedia.org/wiki/スルー・レート "wikilink")を高く維持するように信号電圧が低く設定されている。 データ転送速度は1x・2x・4x・8xの4種類があり、[バースト転送](https://ja.wikipedia.org/wiki/バースト転送 "wikilink")時でそれぞれ 266MB/s・533MB/s・1.07GB/s・2.13GB/sの速度となっている。

[thumb](https://ja.wikipedia.org/wiki/ファイル:AGP_&_AGP_Pro_Keying.svg "wikilink")

カードエッジ端子部分はPCIのような櫛状に端子を並べるのではなく、かつての[EISAバスと同様](../Page/Extended_Industry_Standard_Architecture.md "wikilink")、端子を上下2列に千鳥配置としている。

また複数の動作電圧が設定されているので、対応電圧の異なるカード・スロットを区別するため、図に示すように、3.3Vと1.5Vの電圧にそれぞれ対応した位置に、カードには切り欠きが、スロットには突起が存在する。これにより電圧が非対応のカードの挿入を物理的に防いでいる。AGP 3.0の駆動電圧である0.8Vに対応した切り欠き（突起）は存在しないが、0.8Vで動作するカードは、0.8V非対応のスロットに挿入されたときも適切に対処することが規格上定められており\[11\]、AGP 3.0専用カードであっても1.5Vの入力電圧に耐え（切り欠きにより3.3V専用スロットへの挿入は物理的に回避できる）、非対応スロットであることを電気的に認識した後に動作を停止（あるいは1.5V動作に自動切り替え）し、故障を回避する必要がある。なお、3.0対応スロットの場合、2.0のカードが装着された場合には自動的に2.0モードに切り替わる実装が多い\[12\]。

過去には、切り欠きが不適切に設定されたカードにより、回路が焼損する事故が起きたこともある。

なお、例えばAGP2.0対応カードが必ずしも全ての動作速度に対応しているわけではなく、動作モードは2xまでしかサポートしないというカードも存在する。

カードやスロットにより、対応する規格の範囲が異なり混乱を招くことがある。また、カードやスロットの物理的形状だけでは対応する動作モードを判断することが出来ないため、混乱に拍車をかけている。

なお、拡張スロットの色は茶色が多く、CPUからは最も近い位置にあることが多い。

  - AGP Pro\[13\]
    画像処理に特化した[ワークステーション](../Page/ワークステーション.md "wikilink")等で用いられる、より多くの電力を必要とするビデオカード向けに、ピン数を増やした AGP Pro 規格がある。

## 終焉

[2005年](../Page/2005年.md "wikilink")末以降の[マザーボード](../Page/マザーボード.md "wikilink")の新製品では、より高性能だがAGPと互換性のない後継規格[PCI Express](../Page/PCI_Express.md "wikilink") （PCIe）規格スロットのみを搭載したマザーボードが一般的となったため、AGPは事実上旧規格（[レガシーデバイス](../Page/レガシーデバイス.md "wikilink")）となり、各ビデオカード[ベンダー](https://ja.wikipedia.org/wiki/ベンダー "wikilink")の最新型製品におけるラインナップはPCIeを中心とした物に移り変わっていった。[NVIDIA](../Page/NVIDIA.md "wikilink")は[GeForce](https://ja.wikipedia.org/wiki/GeForce "wikilink") 8シリーズ以降のAGP版をリリースしていない 。[AMDでは](https://ja.wikipedia.org/wiki/アドバンスト・マイクロ・デバイセズ "wikilink")2009年現在のところ[Radeon](https://ja.wikipedia.org/wiki/Radeon "wikilink") HD 3000・4000シリーズのAGP版が発売されているが、HD 2000シリーズ以前に比べるとラインナップが大幅に減少し、HD 5000シリーズ以降AGP版のリリースは停止された。

PCIe用ビデオチップをAGPに転用するため、AGP-PCIeブリッジチップ（NVIDIA製品では「HSI」、AMD製品では「Rialto」と呼ばれる）を搭載するカードも存在していた。

## 脚注

## 関連項目

  - [Extended Industry Standard Architecture](../Page/Extended_Industry_Standard_Architecture.md "wikilink") (EISA)
  - [Industry Standard Architecture](../Page/Industry_Standard_Architecture.md "wikilink") (ISA)
  - [Peripheral Component Interconnect](../Page/Peripheral_Component_Interconnect.md "wikilink") (PCI)
  - [XTバス](../Page/XTバス.md "wikilink")
  - [VESA ローカルバス](../Page/VESA_ローカルバス.md "wikilink")
  - [PCI Express](../Page/PCI_Express.md "wikilink")
  - [転送速度](https://ja.wikipedia.org/wiki/転送速度 "wikilink")
  - [レガシーデバイス](../Page/レガシーデバイス.md "wikilink")

[Category:グラフィックカード](https://ja.wikipedia.org/wiki/Category:グラフィックカード "wikilink") [Category:コンピュータバス](https://ja.wikipedia.org/wiki/Category:コンピュータバス "wikilink")

1.  基本的にはPCIバス互換の時分割共用モードで動作し、各対応デバイスのドライバで分離モード動作をサポートする。なお、この機能はAGP 2.0まではオプションとされサポートが必須でなく、AGPカードとチップセット間での互換性問題の一因となっていた。
2.  デュアルポート[VRAM](../Page/VRAM.md "wikilink")、 [SGRAM](https://ja.wikipedia.org/wiki/SGRAM "wikilink")、[WRAM](https://ja.wikipedia.org/wiki/WRAM "wikilink")など。本ポートの開発当時、これらは非常に高価であった。
3.  従って、本ポート以前にビデオカード用の拡張バスに使われていた[PCIや](../Page/Peripheral_Component_Interconnect.md "wikilink")[VLバスのデータ転送帯域の不足が](../Page/VESA_ローカルバス.md "wikilink")、開発の直接的な動機となったわけではない。
4.  これらの機能を従来のPCIバス経由で実行した場合、データバスが飽和し転送帯域が不足することが危惧された。本ポートが複数のデバイスによる共有を前提とする「バス」ではなく単独のデバイスが占有する「ポート」とされたのも、この点に対する対応である。
5.  一般市場で流通した最初の製品は[Number Nine Visual Technology社のRevolution](https://ja.wikipedia.org/wiki/ナンバー・ナイン・ビジュアル・テクノロジー "wikilink") 3Dで、これに[Matrox](../Page/Matrox.md "wikilink")社のMillenium IIや[Intel 740などが続いた](../Page/Intel_740.md "wikilink")。
6.  ただし、こうしたオフィス向けPCでも、メインメモリ共有による統合グラフィック機能を使用せず、別途グラフィックコントローラを搭載した方が、メインメモリへのアクセス負荷が大きく軽減されることもあり、表示のレスポンス面では改善されるのでベンチマークの数値とは別に体感は速くなる。なお、メインメモリの高速化と統合グラフィック機能の性能向上により、近年ではこの種の統合チップセットでも一般使用に十分な性能の3Dグラフィック機能が利用可能な製品が増えつつある。
7.  対応チップセットには仮想PCI-PCIバスブリッジ機能が搭載されており、ドライバでモード切替を行わない限りは本ポートは仮想的にセカンダリ以降のPCIバスとして振る舞う。これにより、サイドバンドアドレッシング機能やDIME機能をサポートしないWindows NTなどでも、これらの機能を無効化したドライバを用意することで、OSサポートの後方互換性が確保されている。また、上述のRevolution 3DやMillenium II、[3dfx](../Page/3dfx.md "wikilink")社の[Voodoo Banshee](https://ja.wikipedia.org/wiki/Voodoo_Banshee "wikilink")、それに[NVIDIA](../Page/NVIDIA.md "wikilink")社のRIVA 128など初期に開発されたAGP対応グラフィックコントローラではこのサイドバンドアドレッシング機能はそもそもサポートされていない。この互換機能を生かした極端な例では、AGP用のグラフィックカードを、電圧の変換のみでPCI用として使用するアダプタが販売された事例もあった。
8.  [Accelerated Graphics Port Interface Specification Rev. 1.0](http://www.playtool.com/pages/agpcompat/agp10.pdf), Intel, accessed Dec. 14, 2007.
9.  [AGP 4X: Faster Data Transfer & Better-Quality Images](http://www.smartcomputing.com/editorial/article.asp?article=articles/archive/g0801/35x01/04g01.asp), Smart Computing, January 2000.
10. [AGP 3.0 Specification](http://download.intel.com/support/motherboards/desktop/sb/agp30.pdf), Intel, accessed Dec. 14, 2007.
11.
12. [対応ビデオカードが続々登場した「AGP 3.0」の意義とは?](http://k-tai.ascii24.com/db/review/hard/videocard/2003/01/11/640375-000.html) ASCII24 2003年1月11日
13.
> この記事は[TSUBAME](https://ja.wikipedia.org/wiki/TSUBAME)から翻訳されています。


[TSUBAME2.0.jpg](https://ja.wikipedia.org/wiki/File:TSUBAME2.0.jpg "fig:TSUBAME2.0.jpg") **TSUBAME**（つばめ）とは、[東京工業大学](../Page/東京工業大学.md "wikilink")に設置された大規模クラスター型[スーパーコンピュータ](../Page/スーパーコンピュータ.md "wikilink")の名称。TSUBAMEの名称は「Tokyo-tech Supercomputer and UBiquitously Accessible Mass-storage Environment」の略であり、東京工業大学のシンボルマークである[つばめを掛けている](../Page/ツバメ.md "wikilink")。 [Linpackベンチマークで](../Page/LINPACK.md "wikilink")38.18T[FLOPS](../Page/FLOPS.md "wikilink")を達成し、[2006年](../Page/2006年.md "wikilink")6月の世界のスーパーコンピュータ性能ランキング[TOP500](https://ja.wikipedia.org/wiki/TOP500 "wikilink")において、7位にランクインした。以降[2008年](https://ja.wikipedia.org/wiki/2008年 "wikilink")11月まで日本国内のシステムにおいて最上位を占めた。[2009年](../Page/2009年.md "wikilink")6月には87.01TFLOPSを記録し、全体では41位、日本国内では新システムに更新した[地球シミュレータ](../Page/地球シミュレータ.md "wikilink")らに次いで4番手となった。

[2010年](https://ja.wikipedia.org/wiki/2010年 "wikilink")には[インテル](https://ja.wikipedia.org/wiki/インテル "wikilink")の[Xeon](../Page/Xeon.md "wikilink")と[NVIDIA](../Page/NVIDIA.md "wikilink")の[GPU](https://ja.wikipedia.org/wiki/GPU "wikilink")を用いた**TSUBAME 2.0**にバージョンアップされ、[2011年](../Page/2011年.md "wikilink")6月現在1192TFLOPSを記録し、全体では5位、日本国内では2位のスーパーコンピュータである\[1\]。また同月の[Green500](https://ja.wikipedia.org/wiki/Green500 "wikilink")では世界2位に入った\[2\]。

[2013年](../Page/2013年.md "wikilink")[9月](../Page/9月.md "wikilink")に「TSUBAME 2.0」のGPUを[NVIDIA Tesla](https://ja.wikipedia.org/wiki/NVIDIA_Tesla "wikilink") M2050からNVIDIA Tesla K20Xへアップグレードした**TSUBAME 2.5**にバージョンアップされた。

[2017年](../Page/2017年.md "wikilink")[8月1日](../Page/8月1日.md "wikilink")、「**TSUBAME3.0**」本格稼働を開始した。TSUBAME3.0はIntelのXeon E5-2680 v4 CPUが2個とNVIDIAのSXM2 P100 GPUが4個からなり、浮動小数点演算をはじめとした演算性能を前モデルであるTSUBAME 2.0の2～10倍以上に向上させている\[3\]。また、冷却効率を示す指標「PUE（power usage effectiveness）」で年間平均値1.033を実現できる見込み（TSUBAME2.0ではPUEは1.28）で高い冷却効率を実現している\[4\]。

TSUBAME 3.0およびそれ以降のためのテストベッドシステムである**TSUBAME-KFC**は、2013年11月、[2014年](../Page/2014年.md "wikilink")6月にGreen500で1位を獲得した\[5\]。

## 導入への流れ

東京工業大学・学術国際情報センターにおける2002年からのTitech Campus Gridのクラスタ・グリッドに関する研究開発及び運用経験をふまえ仕様が決定され、2005年10月に[日本電気](../Page/日本電気.md "wikilink") (NEC)、[サン・マイクロシステムズ](../Page/サン・マイクロシステムズ.md "wikilink")などによる企業連合が落札し、2006年3月から4年の運用契約で導入された。

TSUBAMEでは、「みんなのスパコン」として、既存のスーパーコンピュータシステムでは実施不可能な規模の計算を可能とするとともに、学内外のすそ野の広いユーザー層をとりこみ、将来のシミュレーション科学に携わる人間を養成するため、多くのユーザーにとって簡便なスパコン環境や他のサービスを提供するという、二律背反的な要素を同時に満たすべく、リーダーの[松岡聡の下で開発や調達が進められた](https://ja.wikipedia.org/wiki/松岡聡_\(計算機科学者\) "wikilink")。

国立大学法人化以前では、大学基盤センターにおけるスーパーコンピュータは、大学の予算とは別途文部科学省から運用予算が直接提供され、それを基盤センターのみの裁量で各メーカーのカタログから選ぶような方法で政府調達し、全国共同利用施設として運用する形態であった。一方、法人化後は大学運営の基本予算である運営費交付金に含まれてスパコンの運用予算が各大学法人に配布されることとなり、その学内における予算の配分は大学の裁量に任されることとなって、大学の他の経費と直接競合することとなった。したがって、TSUBAMEの研究開発においては、スパコンとしての特質はもとより、いかにコストパフォーマンスを革新的に上げるか、全学のメンバーに情報システムとしての利得をもたらして幅広い学内支持を得るか、外部との連携の礎となって社会貢献するとともに東工大に外部資金などをもたらすか、などの従来にない複数の目標を掲げ、それを満たすマシンとしての姿が仕様化された。

## TSUBAMEの仕様

  - TSUBAME 1.0

<!-- end list -->

1.  [AMD製](https://ja.wikipedia.org/wiki/アドバンスト・マイクロ・デバイセズ "wikilink")64ビットCPU AMD [Opteron](https://ja.wikipedia.org/wiki/Opteron "wikilink") Dual Core model 880（クロック2.4GHz） 8CPU搭載Sun Fire x4600 32GBメモリ 639ノード
2.  AMD製64ビットCPU AMD Opteron Dual Core model 885（クロック2.6GHz） 8CPU搭載Sun Fire X460 64GBメモリ 16ノード
3.  [SuSE Linux](https://ja.wikipedia.org/wiki/SuSE_Linux "wikilink") Enterprise Server 9
4.  NEC iStorage S1800AT 96TB RAID6
5.  Sun Microsystems 1PBストレージ--- Sun Fire x4500 24TB ユニット 42ノード
6.  [ClearSpeed](https://ja.wikipedia.org/wiki/クリアスピード・テクノロジー "wikilink") CSX600 2基搭載96GFLOPSアクセラレータボード
7.  Voltaire社 ISR9288 288ポート[InfiniBand](../Page/InfiniBand.md "wikilink")ネットワークスイッチ 8基

<!-- end list -->

  - TSUBAME 1.2

<!-- end list -->

1.  [NVIDIA](../Page/NVIDIA.md "wikilink")社製システム「[Tesla](https://ja.wikipedia.org/wiki/NVIDIA_Tesla "wikilink") S1070 ([GeForce](https://ja.wikipedia.org/wiki/GeForce "wikilink") GTX 280相当)」\[6\] Tesla 4枚で1ユニット 170ノード 680GPU
2.  tsubasaシステム Sun Blade X6250 90ノード 720CPU

<!-- end list -->

  - TSUBAME 2.0

<!-- end list -->

1.  "THIN"ノード -- [HP](../Page/ヒューレット・パッカード.md "wikilink") SL390s G7 1408ノード（[インテル](https://ja.wikipedia.org/wiki/インテル "wikilink")製CPU Westmere-EP 2.93GHz 12core/node, 54GB メモリ(1347ノード) 96GBメモリ(41ノード), GPU [NVIDIA Tesla](https://ja.wikipedia.org/wiki/NVIDIA_Tesla "wikilink") M2050 515GFLOPS 3GPU/node）
2.  "Med"ノード -- HP DL580 G7 24ノード（インテル製CPU Nehalm-EX 2.00GHz 32core/node, 128GB メモリ）
3.  "Fat"ノード -- HP DL580 G7 10ノード（インテル製CPU Nehalm-EX 2.00GHz 32core/node, 256GB メモリ(8ノード)、512GB メモリ(2ノード)）
4.  ノード間接続 -- Voltaire Grid Director 4700(Infiniband QDR 324ポート) 12台,Voltaire Grid Director 4036(Infiniband QDR 36ポート) 179台,Voltaire Grid Director 4036E(Infiniband QDR 34ポート) 6台
5.  ストレージ -- Data Direct NETWORKS社製 DDN SFA10000 6台 7.13PB

<!-- end list -->

  - TSUBAME 2.5

<!-- end list -->

1.  "THIN"ノード (1408ノード) -- HP SL390s G7, Xeon X5670 2つ, NVIDIA Tesla K20X 3つ, メモリ 54GiB or 96GiB
2.  "Medium"ノード (24ノード) -- HP DL580 G7, Xeon 7550 4つ, NVIDIA Tesla S1070 or S2070, メモリ 128GiB
3.  "Fat"ノード (10ノード) -- HP DL580 G7, Xeon 7550 4つ, NVIDIA Tesla S1070, メモリ 256GiB or 512GiB

<!-- end list -->

  - TSUBAME 3.0

## TSUBAMEの特徴

AMD Opteron CPUを搭載したSun Fire X4600が655ノードで10,480 CPUコアとx86系システムとしては世界最大級のCPUコア数を誇っている。またClearSpeed CSX600を採用したスーパーコンピュータシステムとしても世界初、世界最大規模である。 調達当時のシステムの理論ピーク性能は85TFLOPSと公表されているが、 50TFLOPSがOpteronにより、35TFLOPSがClearSpeed CSX600によるものである。

また、みんなのスパコンとして1.1ペタバイトの高速なディスクストレージがNEC iStorage（96テラバイト）と42台のSunFire x4500（1ペタバイト）として実現された。LUSTREファイルシステムにより、運用時でも数GB/s、最高性能では40GB/sのI/O性能を誇る。

システム全体は、計算ノード・ストレージノードとも8台の288ポートのInfinibandスイッチで多段相互結合網として相互接続され、各計算ノードからは20Gbps（システム全体では13Tbps）、中心部分では288Gbpsのバイセクションバンド幅を実現して、大規模なMPIなどによる並列計算や高速I/Oをサポートする。

その後の増設により、現状では最大メモリのノードは128GB（2台）となるとともに、ストレージではx4500がNESTREシステムとして増設され、合計60台で1.5ペタバイトとなり、さらにClearSpeedボードが分子動力学アクセラレータとして追加されて、スパコン部分を含む全体での合算のピーク性能は、2007年10月に日本初の汎用コンピュータとして103TFLOPSに達した (TSUBAME 1.1)。

2008年11月にNVIDIAのTesla、さらにクワッドコアXeon 2ソケットのブレード90ノードからなるtsubasaシステムを導入し、理論値ピーク性能170TFLOPS、[Linpack](https://ja.wikipedia.org/wiki/Linpack "wikilink")の結果で77.48TFLOPSを記録した (TSUBAME 1.2)。

2010年11月にインテル製CPUとNVIDIA製GPUを搭載したHPのHP SL390sへの置き換えを実施。Linpackにおいて1192TFLOPSを記録した (TSUBAME 2.0)。

## TSUBAMEのキャッチフレーズ「みんなのスパコン」

スパコンとしての利用のみならず、新入生を始めとして東工大に属するすべての人々に利用権が与えられ、教育利用や種々のホスティングサービスなど、東工大のキャンパスITの集中資源として広く利用されている。また、日本の基盤センター系としてははじめて公式に外部の私企業の利用を認め、シミュレーションを用いた産業イノベーションを手助けして幅広い社会貢献を行うとともに、学内外の産学共同研究の要となっている。

## TSUBAME 2.0

NEC・HP連合の落札により、TSUBAME 2.0の導入が行われ、2010年11月稼働開始した。

## TSUBAME 2.5

[2013年](../Page/2013年.md "wikilink")[9月](../Page/9月.md "wikilink")に「TSUBAME 2.0」のGPUをNVIDIA Tesla M2050から最新のNVIDIA Tesla K20Xへアップグレードした改良版。2013年11月のTOP500で世界11位、Green500で世界6位。「TSUBAME 2.5」のアップグレードは「TSUBAME 2.0」に対する需要過多の早急な解消と、「TSUBAME 3.0」の実現に向けた技術開発を推進するのが狙い\[7\]。「TSUBAME 2.0」の[2012年](../Page/2012年.md "wikilink")度の繁忙期（11〜2月）におけるノード稼働率は99%に達し、特に緊急性の高い防災シミュレーションや産業分野向けアプリケーションの利用がほぼ不可能になる恐れが生じていた\[8\]。理論演算性能は単精度で「TSUBAME 2.0」比3.6倍の約17.1PFLOPS、倍精度で同2.4倍の5.76PFLOPSに向上\[9\]。

## TSUBAME-KFC

TSUBAME-KFC (TSUBAME Kepler Fluid Cooling) とはTSUBAME 3.0およびそれ以降のためのテストベッドシステムで、空冷だけでなくシステムを油浸\[10\]により冷却する液冷機構を備え、冷却に使う電力を抑えている\[11\]。 2013年11月のGreen500で日本のスパコンとして初めて世界1位、Green Graph500のビッグデータ部門において世界1位\[12\]。2014年6月のGreen500でも1位を獲得\[13\]、2015年6月は5位\[14\]、2015年11月は2位を獲得\[15\]。

## TSUBAME3.0

2017年8月1日可動開始。 2017年6月に発表された[Green500](https://ja.wikipedia.org/wiki/Green500 "wikilink")で1位を獲得、同時に発表された[TOP500](https://ja.wikipedia.org/wiki/TOP500 "wikilink")では61位であった\[16\]。性能は16bitの半精度での計算処理が有効とされており、この精度において47.2ペタフロップスとなっている\[17\]。TSUBAME2.5とTSUBAME3.0を併せて運用することにより、東工大GSICは半精度以上で64.3ペタフロップスの演算性能を提供できる国内有数のスパコンセンターとなる\[18\]。

## 脚注

## 関連項目

  - [スーパーコンピュータ](../Page/スーパーコンピュータ.md "wikilink")
  - [Linux](../Page/Linux.md "wikilink")
  - [Supercomputing Programming Contest](https://ja.wikipedia.org/wiki/Supercomputing_Programming_Contest "wikilink")
  - [GPGPU](https://ja.wikipedia.org/wiki/GPGPU "wikilink")

## 外部リンク

  - [東京工業大学学術国際情報センター](http://www.gsic.titech.ac.jp/)

[Category:スーパーコンピュータ](https://ja.wikipedia.org/wiki/Category:スーパーコンピュータ "wikilink") [Category:計算科学](https://ja.wikipedia.org/wiki/Category:計算科学 "wikilink") [Category:東京工業大学](https://ja.wikipedia.org/wiki/Category:東京工業大学 "wikilink")

1.  [1](http://www.gsic.titech.ac.jp/~ccwww/TSUBAME20.pdf)
2.  [スーパーコンピュータの省エネランキング、1位はIBMでTSUBAMEが2位に - ITmedia ニュース](http://www.itmedia.co.jp/news/articles/1011/22/news022.html)
3.
4.
5.
6.  [ASCII.jp：世界初のGPUスパコン！ 東工大のTSUBAME 1.2が公開](http://ascii.jp/elem/000/000/194/194166/)
7.
8.
9.
10. 油は、[ポリアルファオレフィンの一種と発表されている](https://ja.wikipedia.org/wiki/ポリオレフィン#ポリ_α-オレフィン "wikilink")。
11.
12. [東工大、ＮＥＣなどと開発のスパコン「TSUBAME－KFC」が省エネ性能ランキング２冠を獲得](http://itpro.nikkeibp.co.jp/article/ActiveR/20131121/519663/)
13.
14.
15. [The Green500 list - November 2015](http://www.green500.org/news/green500-list-november-2015)
16.
17. [東工大公式サイト\> 東工大ニュース \> 東工大のスパコンTSUBAME3.0が今夏稼働開始―半精度演算性能47.2ペタフロップス、人工知能分野における需要急増へ対応―](http://www.riken.jp/pr/press/2017/20171005_1/)
18.
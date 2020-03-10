> この記事は[ \(CPU\)](https://ja.wikipedia.org/wiki/_\(CPU\))から翻訳されています。


**ゲタ**（[下駄](https://ja.wikipedia.org/wiki/下駄#下駄のつく言葉 "wikilink")）とは、主に上位の[マイクロプロセッサ](../Page/マイクロプロセッサ.md "wikilink")を下位の[マザーボード](https://ja.wikipedia.org/wiki/マザーボード "wikilink")に装着するために使われる変換[基板](https://ja.wikipedia.org/wiki/基板 "wikilink")である。

## 黎明期のゲタ

主に[QFP](https://ja.wikipedia.org/wiki/QFP "wikilink")や[PLCC](../Page/PLCC.md "wikilink")[パッケージのプロセッサを](../Page/パッケージ_\(電子部品\).md "wikilink")[PGAや](https://ja.wikipedia.org/wiki/パッケージ_\(電子部品\)#PGA_\(Pin_Grid_Array\) "wikilink")[DIPに変換するために用いられた](https://ja.wikipedia.org/wiki/パッケージ_\(電子部品\)#DIP "wikilink")。また、[インサーキット・エミュレータ](https://ja.wikipedia.org/wiki/インサーキット・エミュレータ "wikilink")のプローブ（基板の上に特製のプロセッサを載せ、そこから本体へと[信号](https://ja.wikipedia.org/wiki/信号 "wikilink")を伝達する）基板にも用いられた。この様なゲタは主に製品開発に用いられJ-TAGが普及するまでは一般的であった。現在では[ホビー用](https://ja.wikipedia.org/wiki/趣味 "wikilink")[キット](https://ja.wikipedia.org/wiki/キット "wikilink")で、[はんだ付け](https://ja.wikipedia.org/wiki/はんだ付け "wikilink")が難しいパッケージをあらかじめはんだ付けしておいた基板として多用される。 稀な例であるが、QFPパッケージの[組み込み向けプロセッサを汎用マザーボードに搭載するためのゲタとCPUをセットにした製品が作られたことがある](../Page/組み込みシステム.md "wikilink")。その一つに[黄金戦士](https://ja.wikipedia.org/wiki/黄金戦士 "wikilink")と呼ばれる物があり、注目を集めたが、[市場](../Page/市場.md "wikilink")にはあまり出回らなかった。

## 電圧変換ゲタ

[CPUバス](https://ja.wikipedia.org/wiki/CPUバス "wikilink")のピン配列・I/O電圧に互換性はあるが、Vdd(VCore)電圧が異なるCPUが、主に[i486](https://ja.wikipedia.org/wiki/i486 "wikilink")時代に多数作られた。これらのプロセッサは旧式のマザーボードにはそのまま装着できない（[過電圧](https://ja.wikipedia.org/wiki/過電圧 "wikilink")によって[熱暴走](../Page/熱暴走.md "wikilink")を起こすか壊れてしまう）。そのため、給電電圧をゲタ基板上の[レギュレータ](https://ja.wikipedia.org/wiki/レギュレータ "wikilink")によって変換し、マザーボードからは旧世代のCPUのように見せかける基板が多数作られた。これらのゲタはただ単に電圧を変換するだけでなく、外部[クロック](../Page/クロック.md "wikilink")倍率と内部クロック倍率を変更する[スイッチ](../Page/スイッチ.md "wikilink")（[ジャンパー](https://ja.wikipedia.org/wiki/ジャンパー "wikilink")ピン）が設けられていた。後にこのスイッチはマザーボード上に搭載され、[オーバークロック](../Page/オーバークロック.md "wikilink")において定番とも言えるクロック倍率変更スイッチとなる。

## CPUバス変換ゲタ

intelの[P6マイクロアーキテクチャ](https://ja.wikipedia.org/wiki/P6マイクロアーキテクチャ "wikilink")時代のCPU[バスは物理的なピン配置が異なるものの](../Page/バス_\(コンピュータ\).md "wikilink")、電気的特性は一部の例外を除いて[互換性](https://ja.wikipedia.org/wiki/互換性 "wikilink")があり、SOCKET8、SLOT-1、SC370、[Socket370](https://ja.wikipedia.org/wiki/Socket370 "wikilink")の間で相互変換が可能であった。勿論、[Xeon](../Page/Xeon.md "wikilink")をSocket370に挿すといった物理的に無理な組み合わせは別として、およそ考えられる組み合わせのゲタが存在した。特にSocket370とSLOT-1間のゲタは数多く作られた。またこのゲタには[Celeron](https://ja.wikipedia.org/wiki/Celeron "wikilink")で無効化されていた[SMP機能を有効にするスイッチが搭載されており](../Page/対称型マルチプロセッシング.md "wikilink")、Celeronによる[マルチプロセッサシステム構築がブームとなる](https://ja.wikipedia.org/wiki/マルチプロセッシング "wikilink")。[Pentium IIによるマルチプロセッサに比べると性能は決して良いとは言えなかったが](../Page/Pentium_II.md "wikilink")、本来高価なシステムでなければ実現できないマルチプロセッサが安価に実現できること、技術的好奇心を満足できること、単独プロセッサのPentium IIよりは高速であること、[Windows NT系で利用できるCPUの](https://ja.wikipedia.org/wiki/Windows_NT系 "wikilink")[パーティショニング機能を有効にして](https://ja.wikipedia.org/wiki/パーティション "wikilink")[バックグラウンドで重い処理を動かしていても](https://ja.wikipedia.org/wiki/バックグラウンド_\(ソフトウェア\) "wikilink")[エクスプローラー](https://ja.wikipedia.org/wiki/エクスプローラー "wikilink")の動作が軽快であることなど、デュアルCeleron環境が人気を博する理由はいくらでもあった。

## バス方式変換ゲタ

[PentiumM](https://ja.wikipedia.org/wiki/PentiumM "wikilink")や[Pentium III-Sといったバス仕様に変更が加えられたプロセッサを](../Page/Pentium_III.md "wikilink")、旧仕様のマザーボード([i440BX等](https://ja.wikipedia.org/wiki/Intel_440BX "wikilink"))に搭載するためのゲタが作られた。このゲタはそれまでのゲタとは大きく異なり、ゲタ上に[ASIC](../Page/ASIC.md "wikilink")を搭載し、旧方式のバスプロトコルと新方式のバスプロトコルを仲介する。またサイドバンド信号を取り出し、[VRMを制御することで省電力機能を有効にすることも出来る](https://ja.wikipedia.org/wiki/電圧レギュレータモジュール "wikilink")、極めて高度なゲタも存在した。これらのゲタは高価であったが、旧式のシステムを延命し、パフォーマンスを倍加させ、なおかつ[消費電力](https://ja.wikipedia.org/wiki/消費電力 "wikilink")を低減した。このゲタは本来[モバイル向けなどの](../Page/ノートパソコン.md "wikilink")[チップセット](../Page/チップセット.md "wikilink")を[デスクトップマザーボードに搭載したモバイルオンデスクトップが主流になる迄使われ続けた](../Page/デスクトップパソコン.md "wikilink")。

## ゲタの終焉

ゲタの時代は、[LGAパッケージや](https://ja.wikipedia.org/wiki/パッケージ_\(電子部品\)#LGA_\(Land_grid_array\) "wikilink")[BGAパッケージの登場によって](https://ja.wikipedia.org/wiki/パッケージ_\(電子部品\)#BGA_\(Ball_grid_array\) "wikilink")、パッケージ変換ゲタを残して姿を消した。現在でも旧式のCPUのゲタは入手可能であるが、その利便性はかつての全盛期には及ばない。

[Category:マイクロプロセッサ](https://ja.wikipedia.org/wiki/Category:マイクロプロセッサ "wikilink")
> この記事は[CPUバス](https://ja.wikipedia.org/wiki/CPUバス)から翻訳されています。


**CPUバス** (CPU Bus) とは、[CPU](../Page/CPU.md "wikilink")直結の[バスである](../Page/バス_\(コンピュータ\).md "wikilink")。

[マルチプロセッサ構成の場合は](../Page/マルチプロセッシング.md "wikilink")[プロセッサ](../Page/プロセッサ.md "wikilink")同士を、またCPUと[ノースブリッジ](../Page/ノースブリッジ.md "wikilink")や[キャッシュメモリ](../Page/キャッシュメモリ.md "wikilink")（CPUがn次キャッシュまで内蔵している場合はn+1次キャッシュ）など、システムの構成上CPUにごく近い要素を接続する。CPUがそれほど高速でなかった昔は、外部まで引っ張り出されているものもあった。

## 概要

CPUバスはCPUに直接繋がったバスである。キャッシュをつなげるバスとノースブリッジをつなげるバスを分ける構成の場合は、ノースブリッジ側をシステムバス、[フロントサイドバス](../Page/フロントサイドバス.md "wikilink")とも呼ぶ場合がある（[インテル](https://ja.wikipedia.org/wiki/インテル "wikilink")が[x86](https://ja.wikipedia.org/wiki/x86 "wikilink")でそのような構成を導入した際にそう呼んだ）。複数の[プロセッサ](../Page/プロセッサ.md "wikilink")間を結ぶ共有バスとしても使われる（[対称型マルチプロセッサ](https://ja.wikipedia.org/wiki/対称型マルチプロセッサ "wikilink")）。x86の歴史で見ると、[486の時代には拡張バスとしても使われていた](../Page/Intel486.md "wikilink")（[VLバス](../Page/VESA_ローカルバス.md "wikilink")）。

CPUバスの性能は、その[コンピュータ・アーキテクチャ](../Page/コンピュータ・アーキテクチャ.md "wikilink")全体の性能を大きく支配する。そのため、CPU能力の向上と共にCPUバスは高クロック化・バス幅の拡張によって、より広い帯域を獲得する方向で強化されつつある。一時期はバスを伝播する信号が放射する[ノイズ](../Page/ノイズ.md "wikilink")と[クロストークによって](../Page/漏話.md "wikilink")、信号線を信号が伝わる速度から、限界は低いと見られていたが、バスの駆動電圧を下げることで低[エミッション化をはかり](../Page/電磁両立性.md "wikilink")、また[プリント基板](../Page/プリント基板.md "wikilink")の製造技術向上と[CAD](../Page/CAD.md "wikilink")ツールのルーティング能力向上によりブレークスルーを得て、[64ビット](https://ja.wikipedia.org/wiki/64ビット "wikilink")幅 1GHz以上の駆動周波数を有するCPUバスを持つ高性能プロセッサも販売されている。

インテルx86の場合は[Nehalemマイクロアーキテクチャ](https://ja.wikipedia.org/wiki/Nehalemマイクロアーキテクチャ "wikilink")で、ノースブリッジとの接続にはバスを廃しインターコネクト化した。

低コストかつ高性能化を図るためにノースブリッジをプロセッサに統合した製品がある。例えば[トランスメタ](../Page/トランスメタ.md "wikilink")の[Crusoe](../Page/Crusoe.md "wikilink")等があげられる。原理的にはCPUバスを内蔵にする事により高性能化する事ができるが、むしろ高性能化によって得られたマージンを低消費電力に活用し、低発熱低消費電力ローフットプリントの組み込みプロセッサが多い。

拡張バスがCPUバスに比べて遅く、システム性能の[ボトルネック](../Page/ボトルネック.md "wikilink")となっていた時代には、従来の拡張バスにCPUバスを加える、あるいはCPUバスそのものを引き回す事でこの問題の解決を図った時代があった。このようなバスは[ローカルバス](https://ja.wikipedia.org/wiki/ローカルバス "wikilink")と呼ばれ、代表的なものとして[i486のメモリバスを](https://ja.wikipedia.org/wiki/Intel_486 "wikilink")[ISAバスに物理的に継ぎ足した](../Page/Industry_Standard_Architecture.md "wikilink")「だけ」の[VESA ローカルバスが有名である](../Page/VESA_ローカルバス.md "wikilink")。もっと時代を遡ると、[ファミコンの](https://ja.wikipedia.org/wiki/ファミリーコンピュータ "wikilink")「カセット」や[MSX](https://ja.wikipedia.org/wiki/MSX "wikilink")の「スロット」など、CPUバスは当たり前のように引き出されていた。

[インテル](https://ja.wikipedia.org/wiki/インテル "wikilink")の[IA-32](../Page/IA-32.md "wikilink")アーキテクチャでは[Pentium](https://ja.wikipedia.org/wiki/Pentium "wikilink")まで互換CPUはピン配列互換性があった。[AMDとインテルの間で起こったバス方式に関する訴訟以後](https://ja.wikipedia.org/wiki/アドバンスト・マイクロ・デバイセズ "wikilink")、x86互換CPUでもメーカー毎にバスの設計は異なる物となり互換性は無くなった。

## 構成要素

  - [クロック](../Page/クロック.md "wikilink")
    基本的にはいわゆるベースクロックがCPUバスのクロックとしてCPUに供給される。
  - [制御信号](https://ja.wikipedia.org/wiki/制御信号 "wikilink")
    バスの読み書き方向、データを確定するストローブ信号、割り込み信号、リセット信号、バス状態信号などがある。メモリコントローラを内蔵しているZ-80などでは[DRAM](https://ja.wikipedia.org/wiki/DRAM "wikilink")リフレッシュ用信号も出力する。
  - [アドレスバス](https://ja.wikipedia.org/wiki/アドレスバス "wikilink")
    メモリやI/Oポートのアドレスを指定する。アドレスバスからアドレスが出力されて、制御信号でストローブ状態が確定した時、データバスのデータが有効となる。
  - [データバス](https://ja.wikipedia.org/wiki/データバス "wikilink")
    メモリやI/Oのデータを読み書きする信号である。

古い時代のCPUはこれらのバス信号が個別に出力されていた。しかし、ピン数削減から信号線を時分割多重で複数の目的に使ったりした。最近の世代のCPUでは、CPUからの入出力はプロトコルによって抽象化され、バスにはパケットの形でデータが入出力される。これにあわせて、DRAMもパケットベースのデータ入出力にシフトし、ワード線の信号を全部まとめて入出力するSDRAMと呼ばれるタイプのメモリが使われるようになった。

## 各種アーキテクチャとCPUバス

  - [MITS](../Page/Micro_Instrumentation_and_Telemetry_Systems.md "wikilink") [Altair 8800](../Page/Altair_8800.md "wikilink")
    後に業界標準となる[S-100バス](../Page/S-100バス.md "wikilink")と呼ばれる拡張バスを備えた。[8080のCPUバスが直接拡張スロットに延長された形となっている](../Page/Intel_8080.md "wikilink")。
  - [ザイログ](../Page/ザイログ.md "wikilink") [Z80](../Page/Z80.md "wikilink")
    8ビットマイクロプロセッサを代表するCPUで、同CPUのバスは[バッファ](../Page/バッファ.md "wikilink")[ICを経てそのまま拡張スロットに使われた](../Page/集積回路.md "wikilink")。標準化された[インタフェースとして](../Page/インタフェース_\(情報技術\).md "wikilink")[MSX](https://ja.wikipedia.org/wiki/MSX "wikilink")の拡張スロットが有名である（主にゲームソフトウエアを格納したROMボードの入ったカートリッジを差し込む。拡張RAMや[LANアダプタ](../Page/Local_Area_Network.md "wikilink")、[プリンタインターフェースなども作られた](https://ja.wikipedia.org/wiki/プリンター "wikilink")）。後年の[1チップMSX](https://ja.wikipedia.org/wiki/1チップMSX "wikilink")では拡張スロットインターフェースも再現された。
  - [モトローラ](../Page/モトローラ.md "wikilink") 680x0
    外部バスが16ビットである[68000](../Page/MC68000.md "wikilink")/[68010を除く](../Page/MC68010.md "wikilink")、68000シリーズで採用されたCPUバス。一部にピン非互換であったが、簡単な修正によって古いMPUをよりグレードの高いMPUに置き換える事が出来た。68000は標準化されたバス[VMEバス](../Page/VMEバス.md "wikilink")を輩出し、後継MPUは同バスを拡張した。
  - [インテル](https://ja.wikipedia.org/wiki/インテル "wikilink") [8088](../Page/Intel_8088.md "wikilink")
    [PC/XTで知られる](https://ja.wikipedia.org/wiki/PC/AT#PC_XT "wikilink")[XTバス](../Page/XTバス.md "wikilink")の基本となった。
  - インテル [8086](../Page/Intel_8086.md "wikilink")
    日本国内において[日本電気](../Page/日本電気.md "wikilink") (NEC) がピン配列互換高速CPU [V30を発売する等](https://ja.wikipedia.org/wiki/NEC_Vシリーズ#V30 "wikilink")、[セカンドソース](../Page/セカンドソース.md "wikilink")契約の範囲を超えた、付加価値を持ったピン配列互換CPU市場が形成され始める。NEC [PC-9800シリーズ](../Page/PC-9800シリーズ.md "wikilink")に搭載された[Cバス](../Page/Cバス.md "wikilink")は、8086のCPUバスを8ビットパソコンと同じ手法でバッファICで単純に延長した物である。
  - インテル [80286](../Page/Intel_80286.md "wikilink")
    [IBM](../Page/IBM.md "wikilink") [PC/AT](https://ja.wikipedia.org/wiki/PC/AT "wikilink")で知られるISAバスの基本となった。ISAは[PCIバスによって取って代わられるまで](../Page/Peripheral_Component_Interconnect.md "wikilink")[PC/AT互換機](https://ja.wikipedia.org/wiki/PC/AT互換機 "wikilink")の基本的なバスとなった。PC-9800シリーズでは80286のアドレスバス拡張に伴いアドレス線が追加された。
    PC/ATは回路図など基本的な情報が公開された。ただ、[タイミングチャートなどいくつかの重要な情報が公開されていなかったため](https://ja.wikipedia.org/wiki/タイミング図 "wikilink")（これは悪意ではなく、公開するにあたり定義したり測定するコストを惜しんだのだろうと思われる）、相性と呼ばれる互換性問題を後の世に残した。たとえば割り込み信号が発生した際、ある互換機はバスを順番にサンプリングし、ある互換機は一斉にサンプリングする。こういった違いがボードとCPU、あるいはボード間で干渉を起こす事で動作不具合が起きた。後にIBMはこの問題を真剣に検討し、互換機が作られる事を前提とした新しいアーキテクチャで明確な仕様を策定し、それらがPC/AT互換機にもフィードバックされた事で相性問題は解消されていった。
  - インテル [80386](../Page/Intel_80386.md "wikilink")
    互換CPUメーカー各社が採用し、ピン配列互換CPUを多く輩出した「互換性のあるCPUバス」として一時代を築いた。[サイリックス](../Page/サイリックス.md "wikilink")の[Cx486DLC](../Page/Cyrix_Cx486DLC.md "wikilink")，[Cx486SLCはベストセラーになった](../Page/Cyrix_Cx486SLC.md "wikilink")。
    バス幅の32ビット化に伴い、[MCAバスや](https://ja.wikipedia.org/wiki/Micro_Channel_Architecture "wikilink")、[EISAバスが登場した](../Page/Extended_Industry_Standard_Architecture.md "wikilink")。しかし、かつてのPC/AT互換機においてCPUのCPUバスを直接拡張バスとする事は、将来に禍根を残すという反省から、バス幅以外は同CPUの特性とはなんら関係を持っていない。依然として当時はISAバスが主流であり、新参のバス規格は乱立するバス規格に新たなバスを追加するという形で終わり、標準化され安定した接続性は[PCIバスの登場まで待つ事となる](../Page/Peripheral_Component_Interconnect.md "wikilink")。
  - インテル [i486DX](https://ja.wikipedia.org/wiki/Intel_486 "wikilink")
    ISAバスに同CPUのバスをそのまま追加した「[VESA ローカルバス](../Page/VESA_ローカルバス.md "wikilink")」が提唱され普及した。数多くのピン配列互換CPUが登場した。電源電圧の違いから「ゲタ」と呼ばれる電圧変換・ピン配列調整アダプタが登場した。インテル自身もピン配列互換上位CPUを供給した→[オーバードライブプロセッサ](../Page/オーバードライブプロセッサ.md "wikilink")。
  - インテル [Pentium](https://ja.wikipedia.org/wiki/Pentium "wikilink")
    ピン配列互換CPUは登場したがインテルがそれを嫌い、AMDと訴訟を起こした。これにより互換CPUメーカーは[Socket 7を最後にピン配列互換CPU市場から撤退した](../Page/Socket_7.md "wikilink")。
    P54C Pentiumとi430FX "Triton"チップセットにより、拡張バスは大きな転換期を迎えた。CPUのバスはノースブリッジを経て、標準化されたPCIバスに接続するという設計スタイルを確立し、拡張バスはCPUのCPUバスと完全に決別した（ただし[エンディアン](https://ja.wikipedia.org/wiki/エンディアン "wikilink")の問題は解決されなかった）。
  - インテル [Pentium Pro](../Page/Pentium_Pro.md "wikilink")
    バスドライブ方式に[GTL方式を採用しP](https://ja.wikipedia.org/wiki/GTL_\(デジタル回路\) "wikilink")6アーキテクチャとして以後インテルが発売したCPUが持つCPUバスの基本となった。バスドライブ方式は低電圧化に伴い改良され、プロトコルも追加改良されていく。CPU内部でCPUバス上に複数のコアを結合したデュアルコアCPUも登場した。
  - [DEC](../Page/ディジタル・イクイップメント・コーポレーション.md "wikilink") [Alpha](https://ja.wikipedia.org/wiki/DEC_Alpha "wikilink")
    EVシリーズ毎に特徴のあるバス方式を採用していた。そのうち[EV6バス](https://ja.wikipedia.org/wiki/EV6バス "wikilink")はAMDにライセンスされ[Athlon](../Page/Athlon.md "wikilink")で採用され、後に改良されLSI間接続バス[HyperTransport](../Page/HyperTransport.md "wikilink")になった。
  - AMD K8アーキテクチャ ([Opteron](https://ja.wikipedia.org/wiki/Opteron "wikilink")/[Athlon 64](../Page/Athlon_64.md "wikilink"))
    ノースブリッジの一部の機能をCPU上に集積し、メモリアクセスバスと拡張バスを分離した。拡張バスには[HyperTransport](../Page/HyperTransport.md "wikilink")を備える。この方式によりメモリアクセスのレイテンシが少なくする事ができ、また高速かつ標準化されているHyperTransportによって周辺デバイス・拡張スロットを充実する事ができる。
    Opteronシリーズには、特別なハードウエアを用いなくても[NUMA](../Page/NUMA.md "wikilink")を構成できるプロセッサがある。PC/AT互換機のプラットフォームを崩さず、特別なチップを介さずともNUMAを実現できたのはOpetronプロセッサが最初である（x86ベースのNUMAアーキテクチャマシンはPentium Pro時代から存在していたが、特別なチップセットを必要としていた）。
  - [ミップス・テクノロジーズ](../Page/ミップス・テクノロジーズ.md "wikilink") [MIPSアーキテクチャ](../Page/MIPSアーキテクチャ.md "wikilink")
    MIPSシリーズはIPコアとしてよく使われる（[ARM](../Page/ARMアーキテクチャ.md "wikilink") IPコアが携帯電話における標準となるまでは、世界で最も多く使われたCPU・IPコアである）。IPコア上のバスとして[OCPバス](https://ja.wikipedia.org/wiki/OCPバス "wikilink")を策定した。このバスはコアを複数接続し、処理能力を倍増する事ができる。
    [東芝](../Page/東芝.md "wikilink")はTigerと呼ばれるi486DXピン互換MIPSプロセッサを開発した。PC/AT互換機の豊富なハードウエア資源と市場を、MIPSプロセッサと同プロセッサ上で動作する[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink")へ導く橋渡し役として期待されたが、商業的に成功しなかった。以後同社はピン互換CPU市場から[ヘテロジニアスマルチコア](../Page/ヘテロジニアスマルチコア.md "wikilink")開発へ方針転換し、[ソニー・コンピュータエンタテインメント](https://ja.wikipedia.org/wiki/ソニー・コンピュータエンタテインメント "wikilink")の[PlayStationプラットフォームで結実し](../Page/PlayStation_\(ゲーム機\).md "wikilink")、特に[Emotion Engineは高い評価を得た](../Page/Emotion_Engine.md "wikilink")。
  - [トランスメタ](../Page/トランスメタ.md "wikilink") [Crusoe](../Page/Crusoe.md "wikilink")
    CPUバスはCPU内部で終端している。メモリバスとPCIバスがそれぞれ用意されている。AMDのK8アーキテクチャと似ているが設計意図は異なる。CPUバスに高電圧高周波数の信号をやりとりすると多大な電力が輻射として損失になるが、チップ内に収容し低い電圧と最短距離でノースブリッジに接続することで損失を抑えている。これにより極めて低い消費電力で動作した。
  - [IBM](../Page/IBM.md "wikilink") [Cell](../Page/Cell_Broadband_Engine.md "wikilink")
    CellアーキテクチャはCPUバスに相当するバスをチップ上に持つ。さらにチップ上でメモリアクセスへのパスとPPEコア・SPEコア間を結ぶバスを分離している。
  - [NEC](../Page/日本電気.md "wikilink") [SXシリーズ](../Page/NEC_SX.md "wikilink")
    CPUバスはCPUチップから[MCM上で各種コントローラと接続されCPUユニット上で完結している](https://ja.wikipedia.org/wiki/集積回路#ハイブリッド集積回路 "wikilink")。メモリバスはメモリコントローラを経て、CPUユニット間バスと共に[リード線](https://ja.wikipedia.org/wiki/リード線 "wikilink")で一次記憶ユニット郡と結ばれている。信号の同期を図るためにリード線の長さは全て等長にされており、配線を格納しているエンクロージャーにリード線の束が何重にもなって格納されている。[地球シミュレータ](../Page/地球シミュレータ.md "wikilink")ではクラスタ構成要素の距離が不均等になる事から、それを吸収するための特別なユニットが設けられている。

## 関連項目

  - [ハードウェア](../Page/ハードウェア.md "wikilink")
  - [コンピュータ・アーキテクチャ](../Page/コンピュータ・アーキテクチャ.md "wikilink")
  - [CPUソケット](../Page/CPUソケット.md "wikilink")

[Category:コンピュータバス](https://ja.wikipedia.org/wiki/Category:コンピュータバス "wikilink")
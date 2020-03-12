> この記事は[Intel Pentium \(1993\)](https://ja.wikipedia.org/wiki/Intel_Pentium_\(1993\))から翻訳されています。


**Pentium**（ペンティアム）は、[インテル](https://ja.wikipedia.org/wiki/インテル "wikilink")が[1993年](../Page/1993年.md "wikilink")5月から出荷を開始した、[x86](https://ja.wikipedia.org/wiki/x86 "wikilink")アーキテクチャの[マイクロプロセッサ](../Page/マイクロプロセッサ.md "wikilink")([CPU](../Page/CPU.md "wikilink"))ファミリーのブランド名である。

## 名称

Pentiumは、同社のプロセッサである[i486の後継製品である](https://ja.wikipedia.org/wiki/Intel_486 "wikilink")。当初は[80286](https://ja.wikipedia.org/wiki/80286 "wikilink")や[80386](https://ja.wikipedia.org/wiki/80386 "wikilink")、i486に続く新たなプロセッサの名称としては"80586"または"i586"が予想されたが、短い数字とアルファベットの単純な組み合わせだけでは[商標](../Page/商標.md "wikilink")として認められず、ブランド名として確立するために、"5"を意味する[ギリシア語](https://ja.wikipedia.org/wiki/ギリシア語 "wikilink")のPentaと要素を表す[ラテン語](../Page/ラテン語.md "wikilink")のiumから**Pentium**と造語した。インテル社の主張では、Pentiumという単語は[形容詞](../Page/形容詞.md "wikilink")であるため必ず形容される名詞を付けるものとしている。たとえばプロセッサ自身は**Pentiumプロセッサ**と表現する。

ブランドとして確立に成功したことから、これに続くいくつかの後継プロセッサでもPentiumという語を含むブランド名を採用した。

## 特徴

i486プロセッサとの大きな違いは以下の通り：

  - [スーパースケーラ](https://ja.wikipedia.org/wiki/スーパースケーラ "wikilink")構造により、最短5ステージでのパイプライン処理を行う2つの命令実行部を持ち、1[クロック](../Page/クロック.md "wikilink")で1つ以上の命令発行が可能
  - ハードワイヤード制御の命令を増やした\[1\]
  - 64ビット・データバスによるメモリへのアクセス・スピードの向上
  - キャッシュメモリは命令用とデータ用でバスごと分離した[ハーバードタイプとし](../Page/ハーバード・アーキテクチャ.md "wikilink")、サイズもそれぞれ8Kバイトずつと大きくした
  - パイプライン化された高速な浮動小数点演算能力
  - トランジスタ数は310万個の0.8μmのBi[CMOS](../Page/CMOS.md "wikilink")プロセスの採用
  - 前世代よりも効率化された[仮想86モード](../Page/仮想86モード.md "wikilink")のサポート
  - 4KB/pageから4MB/pageへの拡張を行うページ拡張モード（PSE: Paging Size Extensions）のサポート
  - [デュアルプロセッサモードのサポート](../Page/対称型マルチプロセッシング.md "wikilink")
  - 後期型では[MMX](../Page/MMX.md "wikilink")拡張命令セットが加わった

UパイプとVパイプの2ウェイのインオーダーのスーパースケーラ構成であり、整数パイプラインは5段（MMX Pentiumでは6段）、浮動小数点パイプラインは8段であった。[マイクロコード](https://ja.wikipedia.org/wiki/マイクロコード "wikilink")で内部実行する複雑な命令はUパイプでしか実行できず、マイクロコード命令実行中はVパイプで命令は実行できない。データキャッシュからのデータパスを整数演算部と浮動小数点演算部で共用していたため、整数演算命令と浮動小数点演算命令はスーパースケーラ実行ができない。

## 第一世代

第一世代製品はインテル社内の開発呼称より*P5*と呼ばれる。システム[クロック](../Page/クロック.md "wikilink")と同じ速度で動作する66[MHz](https://ja.wikipedia.org/wiki/MHz "wikilink")と60MHzの製品がリリースされたが、量産効果により十分コストが低下した486システムとは違って新規開発のシステムが必要でコストがかさむ上、BiCMOSプロセスだけでなく5V動作であるため消費電力が大きかった。しかしIntelの486系プロセッサがDX2-66MHz版までしかなかった当時はサーバや一部のハイエンド向けPCで使われた。

のちに後述の3.3V版Pentium（90MHz版）が出回るようになると従来の5V版Pentium（特に60MHz版）は一部のミドルレンジ向けPCにもラインアップされるようになった。しかしこの頃には486系にIntel DX4が登場しており、性能的優位もさほど大きくはなくなっていた。やがて75MHz版のPentiumが登場するとその役割を終えた。

この世代のみ[Socket 4が使われ](https://ja.wikipedia.org/wiki/Socket_4 "wikilink")、以降のPentiumは[Socket 5または](https://ja.wikipedia.org/wiki/Socket_5 "wikilink")[Socket 7が使われていて事実上互換性が無かった](../Page/Socket_7.md "wikilink")。Socket 4向けの[オーバードライブプロセッサ](../Page/オーバードライブプロセッサ.md "wikilink")としては2倍のクロックで動作する133MHz版のみ提供され、60MHzのPentiumと置き換える場合には120MHz動作となった。

## 第二世代

[right](https://ja.wikipedia.org/wiki/ファイル:Suoritin_Intel_Pentium_100MHz.jpg "wikilink") 第二世代は、プロセスを微細化した*P54C*、*P54CS* といったコードネームの製品がリリースされた。システムクロックの1.5倍で動作する90MHzと100MHzが登場する。

Intel 430FXと呼ばれるPentium用チップセットにより新設計のシステムアーキテクチャ[Peripheral Component Interconnect](../Page/Peripheral_Component_Interconnect.md "wikilink") (PCI) が一応の完成を見、PCIと共にPentiumの普及が加速される。

後に低価格パソコン向けとして75MHz（1.5倍のクロックで動作するため、システムクロックは50MHzである）も追加された。この世代で唯一システムクロックの低かった75MHz版は、以前のi386SXやi486SXなどと同様に、もともと廉価版に特化したプロセッサという役割があった。しかしPentiumでは高クロック製品が登場するたびに従来クロック製品が順次下位プロセッサとして流用されたため、下位に特化したプロセッサは後の[Celeron](https://ja.wikipedia.org/wiki/Celeron "wikilink")の登場まで一時姿を消すことになる。

その後は、2倍、2.5倍、および3倍で動作する120MHz、133MHz、150MHz、166MHz、200MHzが発売される（166MHz以降、対応システムクロックは66MHzのみ）。[オーバードライブプロセッサ](../Page/オーバードライブプロセッサ.md "wikilink")としてはシステムクロック50/60/66MHz向けにそれぞれ125MHz、150MHz、166MHzの製品が存在した。

尚、一部の133MHz製品(66×2倍)は倍率を×3にする事が可能で、60×3倍の180MHz程度で動作（当然保障外）した製品も数は少ないが存在した。

## 第三世代

第三世代は[MMX](../Page/MMX.md "wikilink")拡張命令セットが付加され、コードネーム*P55C*として*MMXテクノロジペンティアムプロセッサ (Pentium processor with MMX technology)* が登場した。変化した点は、その名の通りMMX拡張ユニットの追加、L1キャッシュ容量の倍増（8KB→16KB）、分岐予測精度の向上、RSBの追加（4エントリー）、パイプラインが5段→6段（プリフェッチとデコード1の間にフェッチ段が追加）に増えた、ストアバッファの増加（1エントリー→4エントリー）、など。[マーケティング](../Page/マーケティング.md "wikilink")ではMMX拡張命令の追加による性能の向上が[宣伝](../Page/宣伝.md "wikilink")されたが、実際には、専用のアセンブリコーディングが必要なMMX命令の、全体に占める量は少なく、内蔵キャッシュの容量の倍増（8KB→16KB）による、従来の命令の実行性能の向上が大きかった。デスクトップ向けとしては166MHz、200MHz、233MHz、モバイル向けとしては120-300MHzが発売された。

デスクトップ向けの233MHz版はジャンパピンの設定を1.5倍とすることで3.5倍動作した。当初はCPU動作倍率の選択にも自由度があり、166MHz版（66MHz×2.5倍）を3倍設定で使うこともできた。これによりシステムクロック50MHzのPCでも、サードパーティ製の電圧変換[ゲタを介して](../Page/ゲタ_\(CPU\).md "wikilink")166MHz版を載せれば150MHzで動かすことができた。しかしその一方でシステムクロックを上げて定格を超える180MHzや200MHzで動かすような[オーバークロック](../Page/オーバークロック.md "wikilink")も横行したことから、後期のロットでは倍率設定ピンが制限されるようになり、例えば166MHz版の場合は2倍か2.5倍しか選べなくなっている。すなわちシステムクロック50MHzのPCを150MHz駆動させるためには、より高価な200MHz版を買わなくてはならないなど不便も伴うものとなった。なおIntelはアップグレード用としてMMX搭載のオーバードライブプロセッサを用意していたが、システムクロック60MHz向け（150/180MHz版）と66MHz向け（166/200MHz版）しかなかった。

なお定格クロックを守っている場合、動作倍率を高くすることは必然的にシステムクロックが低いことを意味する。すなわち同程度のCPUクロックでも本来のパフォーマンスが発揮できなくなるため、安易なアップグレードパスがあることでPentiumブランドの評判に影響する可能性もあった。これに対して後継のP6世代では[Celeron](https://ja.wikipedia.org/wiki/Celeron "wikilink")という下位ブランドを立ち上げており、FSBが低くてもある程度の動作倍率を持つプロセッサが作られるようになっている。実際、一部の大手周辺機器ベンダはCeleronを利用した[Pentium II用CPUアクセラレータ製品を販売するなど](../Page/Pentium_II.md "wikilink")、P6以降の世代ではCeleronがアップグレードパスにも利用された。

## 486向けODP

Intel 486プラットフォームのアップグレード用にPentiumのコアを搭載したオーバードライブプロセッサも登場した。事前にシステムクロックの2倍、最高で66MHz版(P24T)がアナウンスされていたが、システムバス32ビットの486プラットフォームではPentiumの性能を発揮できず性能向上が限られたことから、実際の製品はシステムクロック25MHzおよび33MHzの2.5倍で動作する、それぞれ63MHz版および83MHz版での登場となった。内部キャッシュメモリも倍増している。

しかし、当時は[AMDの](https://ja.wikipedia.org/wiki/アドバンスト・マイクロ・デバイセズ "wikilink")486アップグレード用としてリリースされた[Am5x86](../Page/Am5x86.md "wikilink")がPentium [オーバードライブプロセッサ](../Page/オーバードライブプロセッサ.md "wikilink")より低価格でなおかつ160MHz駆動を行うことによりPentium 100MHz程度の性能を示したため、販売は、一部地域を除いて芳しくなくまた、インテルもPentiumへの移行を急いだため、日本以外の国では失敗作となった。

日本においても、486アップグレードを行うような知識がある層には、Pentium [オーバードライブプロセッサ](../Page/オーバードライブプロセッサ.md "wikilink")は、まったく見向きもされず、Pentium [オーバードライブプロセッサ](../Page/オーバードライブプロセッサ.md "wikilink")よりも安価で高性能なAMDのAm5x86や[サイリックス](../Page/サイリックス.md "wikilink")の[Cyrix_Cx5x86](../Page/Cyrix_Cx5x86.md "wikilink")といったアップグレード用のCPUを販売しているCPUメーカのCPUを使うことによりマシンの延命を行った。

## 全数リコール

[1994年](../Page/1994年.md "wikilink")[11月](../Page/11月.md "wikilink")に、P5 Pentium及びP54C Pentiumの[浮動小数点除算命令にバグがあることが](../Page/Pentium_FDIV_バグ.md "wikilink")[インターネット](../Page/インターネット.md "wikilink")を通じて報告された。その後日本でも新聞や一般誌によって大々的に報道され、パソコンを持っていない人にもこのバグが広く知られることとなった。インテルは当初バグの発生は演算処理のループでは90億回に1回、表計算ソフトを使った場合27000年に1回であるなどとし、この問題は深刻ではないとした。しかし、パソコンが一般消費者にも使われるキッカケとなった[Windows 95と](../Page/Microsoft_Windows_95.md "wikilink")[AMDや](https://ja.wikipedia.org/wiki/アドバンスト・マイクロ・デバイセズ "wikilink")[サイリックス](../Page/サイリックス.md "wikilink")など競合CPUの発売時期に重なり、製品発表後の販売拡大に注力すべき時期に該当したためインテルは苦境に立たされた。

同年[12月20日](../Page/12月20日.md "wikilink")には全数リコールに至った。リコールにかかった費用は膨大なものであったが、ボックス包装されたバグ対策済みPentiumがリリースされたことが広く報道された。

## 「Pentium」の後のPentiumブランド

従来のプログラムがそのまま使用できた上に性能が十分に向上し、加えて宣伝にも力を入れた結果、Pentiumの知名度は非常に高くなり、第6世代（[Pentium Pro](../Page/Pentium_Pro.md "wikilink")・[Pentium II](../Page/Pentium_II.md "wikilink")・[Pentium III](../Page/Pentium_III.md "wikilink")、第7世代（[Pentium 4](../Page/Pentium_4.md "wikilink")・[Pentium D](../Page/Pentium_D.md "wikilink")、[Pentium Extreme Edition](../Page/Pentium_Extreme_Edition.md "wikilink")）、モバイル向けの[Pentium Mと](../Page/Pentium_M.md "wikilink")、コンシューマ向けハイエンドプロセッサのブランドとして長く用いられた。

[Intelは上位の製品に関して](https://ja.wikipedia.org/wiki/インテル "wikilink")、[Pentium 4まで続いたクロック数最重視の設計に終止符を打ち](../Page/Pentium_4.md "wikilink")、[2006年](../Page/2006年.md "wikilink")1月6日に[IPC重視で設計されたアーキテクチャのブランドとして](../Page/プロセス間通信.md "wikilink")[Intel Coreを発表した](../Page/Intel_Core.md "wikilink")。それと同時にプロセッサのメーカーからプラットフォームを提供するという業態変更と[コーポレートアイデンティティー](https://ja.wikipedia.org/wiki/コーポレートアイデンティティー "wikilink")など、インテル自身も大規模転換を行った。併せて、13年の長きわたってインテルの[看板](../Page/看板.md "wikilink")商品であったPentiumブランドの廃止を発表した。しかし、一部地域では上位製品のCoreプロセッサよりも、下位のPentiumブランドの人気が依然として高いことから、[Pentium Dual-Coreという名称でPentiumブランドの存続を決定し](../Page/Pentium_Dual-Core.md "wikilink")、Coreブランドと、ローエンドの[Celeron](https://ja.wikipedia.org/wiki/Celeron "wikilink")ブランドの中間に位置するブランドとして再定義を行った。後にPentium Dual-Coreは位置づけはそのままに、単なる[Pentiumと言う名称へと戻されることとなった](https://ja.wikipedia.org/wiki/Intel_Pentium_\(2010年\) "wikilink")。

IntelはCeleronのブランド名を冠したCPUを低価格パソコン用として、[Xeon](../Page/Xeon.md "wikilink")のブランド名を冠したCPUを[サーバ](../Page/サーバ.md "wikilink")用として販売している。こうしたCPUの中には、各ブランドとも同じアーキテクチャをベースにしたものも多く、クロックスピードや[キャッシュサイズ](../Page/キャッシュメモリ.md "wikilink")、パッケージ形状、[ソケット形状などで差別化されている](../Page/CPUソケット.md "wikilink")。また、異なるアーキテクチャのCPUに同じブランド名が使用されていることから、現在ではパワーユーザを中心に、開発コード名でCPUを呼び分けることもしばしば行われている。

## 脚注

## 関連項目

  - [Socket 5](https://ja.wikipedia.org/wiki/Socket_5 "wikilink"), [Socket 7](../Page/Socket_7.md "wikilink")
  - [オーバードライブプロセッサ](../Page/オーバードライブプロセッサ.md "wikilink")

[Category:インテルのマイクロプロセッサ](https://ja.wikipedia.org/wiki/Category:インテルのマイクロプロセッサ "wikilink")

1.  ハードワイヤード制御の例では、486では42クロック掛かった32ビット乗算命令を10クロックにした。
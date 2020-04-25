> この記事は[DIMM](https://ja.wikipedia.org/wiki/DIMM)から翻訳されています。


[thumb](https://ja.wikipedia.org/wiki/ファイル:Kingston_KVR266X64C25-256_with_Nanya_NT5DS32M8AT-7K.jpg "wikilink") [thumb](https://ja.wikipedia.org/wiki/ファイル:Four_SDRAM_DIMM_slots_on_a_computer_motherboard.jpg "wikilink") **DIMM**（Dual Inline Memory Module、ディム）は、複数の[DRAMチップを](../Page/Dynamic_Random_Access_Memory.md "wikilink")[プリント基板](../Page/プリント基板.md "wikilink")上に搭載したメモリ[モジュール](../Page/モジュール.md "wikilink")のことを指し、[コンピュータ](../Page/コンピュータ.md "wikilink")の[主記憶](https://ja.wikipedia.org/wiki/主記憶 "wikilink")として利用される。また、そのピン配置や電気的特性を規定したDIMM[規格](https://ja.wikipedia.org/wiki/規格 "wikilink")のこと。従来の[SIMM](../Page/SIMM.md "wikilink")(Single Inline Memory Module)では表裏の対向する2つの端子に同一の[信号](https://ja.wikipedia.org/wiki/信号 "wikilink")が出ているのに対して、DIMMでは異なる信号が出ていることからDIMMと呼ばれる。2007年現在、DIMMと言った場合、多くの[パーソナルコンピュータ](../Page/パーソナルコンピュータ.md "wikilink")や[ワークステーション](../Page/ワークステーション.md "wikilink")で使用可能な[SDRAM](../Page/SDRAM.md "wikilink")を搭載したものを指す。

## 規格

DIMM規格は[JEDEC](https://ja.wikipedia.org/wiki/JEDEC "wikilink")(Joint Electron Device Engineering Council)で[標準化](../Page/標準化.md "wikilink")が行われており、搭載されるSDRAMチップの種類毎に多種の規格が存在する。また、「DIMM」という名称は、メモリ基板を挿す[スロット](https://ja.wikipedia.org/wiki/スロット "wikilink")（[ソケット](https://ja.wikipedia.org/wiki/ソケット "wikilink")）のことを指している場合もあるが厳密には誤用であり、これらは「DIMMスロット」や「DIMMソケット」と呼ぶのが正確である。

基本的にDIMM[インタフェースは](../Page/インタフェース_\(情報技術\).md "wikilink")[アドレス](../Page/メモリアドレス.md "wikilink")、[データ](../Page/データ.md "wikilink")、制御信号からなっており、一般的に[PC用は](../Page/パーソナルコンピュータ.md "wikilink")64bitデータのDIMMが使用されるが、高信頼性が求められる[サーバ](../Page/サーバ.md "wikilink")では[ECC](../Page/誤り検出訂正.md "wikilink") 8bitを付加した72bitデータのDIMMが使用される。

## 種類と互換性

DIMMの形態は大きく分けて**Unbuffered DIMM (UDIMM)**、**Buffered (Registered) DIMM**、**Fully Buffered DIMM (FB-DIMM)** の3種類が存在し、これらはインタフェースが異なり、規格上の[互換性](../Page/互換性.md "wikilink")は無い。また、各DIMM内でも[DDR2や](../Page/DDR2_SDRAM.md "wikilink")[DDR3といった違いやECC付き](../Page/DDR3_SDRAM.md "wikilink")／無し、SDRAMの動作速度（アクセス・タイミング）の上限値や動作電圧範囲、などによって細かな規格に分かれており、同一種別間では概ね上位互換性が保たれている。実効[転送速度](https://ja.wikipedia.org/wiki/転送速度 "wikilink")と接続可能なモジュール数はトレードオフの関係にある。

### Unbuffered DIMM

[チップセット](../Page/チップセット.md "wikilink")からのアドレス、制御、データ信号が直接DIMM基板上のSDRAM[チップ](../Page/チップ.md "wikilink")に分配接続される形態のDIMM。

アドレスと制御信号が接続されている全モジュール上の全てのSDRAMチップに分配されるため、駆動側の電流[負荷](https://ja.wikipedia.org/wiki/負荷 "wikilink")が大きい。例えば 4bit SDRAMチップが搭載されたDIMMの場合、アドレス線は16個のDRAM ICに分配されることになり、50-60個ほどが駆動できる限界なので、1つのチャンネル当り接続可能なモジュール数は3-4枚ほどが上限となる。このようにUnbuffered DIMMは、1つのチャンネルに多数接続することができずに、通常は3-4枚までに制約されている。しかし、他の2規格に比べると伝送路の途中に介在物が無いことから実効転送速度で優れコスト面でも有利となる。[ワークステーション](../Page/ワークステーション.md "wikilink")のうちメモリ容量が最優先ではないものに採用されるほか、パーソナルコンピュータのほとんどに使用されている。

### Buffered DIMM

アドレス信号と制御信号を、DIMM基板上のレジスタード・[バッファ](../Page/バッファ.md "wikilink") (Registered buffer) と呼ばれるICで一旦受けて整形増幅してから、各SDRAMチップに分配するDIMM規格である。データ信号はバッファされない。Registered DIMMとも呼ばれる。

バッファの存在により、アドレス信号線と制御信号線の電気的負荷は1モジュール当り1ICだけの負荷となり、1つのチャンネル当り多くのモジュールが接続可能となる。数GBから数十GBといった主記憶容量を必要とする[サーバ](../Page/サーバ.md "wikilink")に向いている。なお、一旦バッファで受けることから、Unbuffered DIMMと[アクセス](../Page/アクセス.md "wikilink")タイミングが異なる。例えばリード(READ)の際は、実際にSDRAMチップへ通知されるアドレス、制御信号がバッファにより1[クロック](../Page/クロック.md "wikilink")遅れることから、見かけ上DIMMからのデータの出力がUnbuffered DIMMと比べて1クロック遅くなる。

DDR2, DDR3 とSDRAMチップが高速化してきたため、バッファされていないデータ信号線の過重な負荷や[ノイズ](../Page/ノイズ.md "wikilink")耐性の不足が顕在化しており、高速動作させるためにはあまり多くのDIMMは接続できなくなっている。

### Fully Buffered DIMM

FB-DIMM(Fully Buffered DIMM)はアドレス、データ、制御信号の全てを一旦DIMM基板上の[AMB](https://ja.wikipedia.org/wiki/AMB "wikilink")(high-speed Advanced Memory Buffer)と呼ばれるバッファ内蔵の専用コントローラ・チップで受ける形態のDIMMである。CPU／チップセット側とは、[PCI Express](../Page/PCI_Express.md "wikilink")(PCIe)に似た少ピンの高速[シリアル・インタフェースで接続される](../Page/シリアルポート.md "wikilink")。従来のDIMMはスタブのあるバス接続によって複数のモジュールが共有接続されていたが、FB-DIMMでは隣り同士がPoint-to-Point接続によって拡張される[デイジーチェーン](https://ja.wikipedia.org/wiki/デイジーチェーン "wikilink")による接続方式となっている。

従来のDIMMに比べチップセット（またはCPU）側の信号が減らされており、アドレス、制御、3.2 - 4.0GHzで駆動される上り用14レーン／下り用10レーンの24組の高速データ信号線（合計48本\[1\]）を含む全69端子で構成される\[2\]。各信号線の伝送動作などはPCIeに近いが\[3\]、通常はPCIeよりも短い伝送距離でもあり、各信号は[8b/10b](https://ja.wikipedia.org/wiki/8b/10b "wikilink")方式のようなクロックは重畳されていない。サーバ機などでの実使用環境では、ライトに比べてリードの比率が圧倒的に高いため、ライト方向とリード方向で信号本数が異なる非対称になっている\[4\]。

各モジュールごとに1つずつ備わるAMBは、上流側モジュールまたはチップセット(CPU)側とのインタフェース、下流側モジュール側インタフェース、自らの汎用SDRAMとのインタフェースという3方向へのインタフェースを有しており、各モジュールのAMBはチップセット(CPU)に近い上流側から信号を受けると、自らがターゲットではない場合は隣接する下流側のモジュールへ信号を転送する。下流側から上流側に向かう場合も同様にAMB間で順次転送される。このようにローカルなメモリコントローラともいえるAMBが互いに連接されることで、デイジーチェーンを構築し、各チャネルあたり最大8枚のDIMMを接続することが可能となっている。各AMB間は同期転送による遅延が生じるため、CPU側から見て遠いモジュール（下流側）へのアクセスは近いモジュール（上流側）よりも遅くなる\[5\]。各AMB内で、並列／直列変換や動作コマンドの翻訳、CRCコードの生成／確認などを高速に行うため発熱量も多くなる。

米Intel社の主導で[PCサーバ](../Page/PCサーバ.md "wikilink")やワークステーション向けに製品化されたFB-DIMMであるが、AMBチップという高機能ICの使用などから高コストであり、放熱への配慮が求められることや、チャンネル当りのモジュール数増加によってレイテンシも増大することもあって、特に大記憶容量と広帯域メモリアクセスが強く求められるエンタープライズ・サーバのような用途を除いては、ミドル／ローエンドクラスのサーバへの採用は広がらなかった。また、[ラムバス](https://ja.wikipedia.org/wiki/ラムバス "wikilink")社の特許権については、Buffered DIMMだけでなくFB-DIMMの構造に関するロイヤリティの支払いが生じることも不利に働いている\[6\]。

このため、Intel社は次世代メモリインターフェースとしてCPUからはFB-DIMMインターフェースでDRAMにアクセスするが、AMBはマザーボード上に実装し、DIMM自体は従来の物に戻すことを計画している。依然としてコンシューマー向けメモリはUnbuffered DIMMが主流であり、コンシューマーからエンタープライズサーバまで幅広いSKUをカバーする次世代プロセッサNehalemのマスクバリエーションをいたずらに増やしたくないintelの意図が伺われる\[7\]。

## 出典・脚注

<references />

## 関連項目

  - [コンピュータ略語一覧](../Page/コンピュータ略語一覧.md "wikilink")
  - [転送速度](https://ja.wikipedia.org/wiki/転送速度 "wikilink")

### 類似の他種

  - [RDRAM](../Page/RDRAM.md "wikilink") (Rambus Dynamic Random Access Memory)
  - [SIMM](../Page/SIMM.md "wikilink") (Single In-line Memory Module)

## 外部リンク

  - [JEDEC](http://www.jedec.org/)
  - [メモリ Mac Pro Retailer](http://www.memoryamerica.com/memory-shop-by-make---model-apple-apple-desktop-mac-pro--2006-2008--memory.html)

[Category:半導体メモリ](https://ja.wikipedia.org/wiki/Category:半導体メモリ "wikilink")

1.  上りと下りともに差動動作であり信号線は2倍の本数である。
2.  他方式のDIMMでは1チャンネルで240本ほどの配線が必要なのに比べて、1チャンネル69本のFB-DIMMはチャンネル数が多くとれる。
3.  FB-DIMMを推進した米Intel社では、過去にRambus社が開発した[RDRAM](../Page/RDRAM.md "wikilink")を推進したが特許権などの高コストなどを理由に失敗した経緯があり、FB-DIMMでは他社の特許をあまり含まないPCIeを元に接続インターフェースを開発・設計したとされる。
4.  上りと下りで同時に読み書き動作が行える。
5.  主プロセッサ側からの読み書きアクセスに対してメモリの動作に掛かる遅延時間は「レイテンシ」と呼ばれ、FB-DIMMではCPUから遠い下流ほどレイテンシが大きくなる。[WindowsVistaで用意されているハードウェアパフォーマンス評価ツールでは](https://ja.wikipedia.org/wiki/Microsoft_Windows_Vista "wikilink")、同じDDR2-5300チップであるにもかかわらず、UnbufferedDIMMに比べて1割から2割ほど評価が下回るとされる。
6.  [『バッファードモジュール』、Rambus、（2008年08月29日時点の[アーカイブ](../Page/インターネットアーカイブ.md "wikilink")）](http://web.archive.org/web/20080829045756/http://www.rambus.com/jp/patents/innovations/detail/buffered_modules.html)
7.  [『IntelはNehalem世代でFB-DIMMをフェイドアウトの方向に』、PC-Watch 後藤弘茂のWeekly海外ニュース、2007年10月23日](http://pc.watch.impress.co.jp/docs/2007/1023/kaigai396.htm)
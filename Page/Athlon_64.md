> この記事は[Athlon 64](https://ja.wikipedia.org/wiki/Athlon_64)から翻訳されています。


**Athlon 64**（アスロン ろくじゅうよん）は、[AMDの](https://ja.wikipedia.org/wiki/アドバンスト・マイクロ・デバイセズ "wikilink")[x86](https://ja.wikipedia.org/wiki/x86 "wikilink")アーキテクチャの[マイクロプロセッサ](../Page/マイクロプロセッサ.md "wikilink")。

Athlon 64は、[Opteron](https://ja.wikipedia.org/wiki/Opteron "wikilink")と同じ[AMD64技術を搭載した](https://ja.wikipedia.org/wiki/x64 "wikilink")。従来の[Athlon](../Page/Athlon.md "wikilink")シリーズはK7アーキテクチャであったのに対し、Athlon 64とその派生製品はK8アーキテクチャが採用した。

同じK8アーキテクチャを採用した上位モデルの[Athlon 64 FXと](../Page/Athlon_64_FX.md "wikilink")、[デュアルコア](https://ja.wikipedia.org/wiki/デュアルコア "wikilink")プロセッサーの[Athlon 64 X2が存在する](https://ja.wikipedia.org/wiki/Athlon_64_X2 "wikilink")。

## 概要

### Opteronとの相違

[Opteron](https://ja.wikipedia.org/wiki/Opteron "wikilink")との違いは、シングルプロセッサのみをサポートすること。それに伴ってCPU間接続が不要になり、[HyperTransport](https://ja.wikipedia.org/wiki/HyperTransport "wikilink")がチップセット接続の為の1本に制限されている。しかしOpteron 100シリーズもHyperTransportは1に制限されている。また、レジスタードメモリを必要とするOpteronに対し、Athlon64はアンバッファードメモリで動作するという差異もある。

ハードウェアインターフェイスとして、シングルメモリチャネルの**[Socket 754](https://ja.wikipedia.org/wiki/Socket_754 "wikilink")**、デュアルメモリチャネルの**[Socket 939](https://ja.wikipedia.org/wiki/Socket_939 "wikilink")**、DDR2メモリー対応の**[Socket AM2](https://ja.wikipedia.org/wiki/Socket_AM2 "wikilink")**を採用している。

### Athlon XPからの改良点

  - [アーキテクチャ](https://ja.wikipedia.org/wiki/アーキテクチャ "wikilink")およびCPUパッケージの改良点は[Opteronとほぼ同一であるためそちらを参照されたい](https://ja.wikipedia.org/wiki/Opteron#Athlon_MPからの改良点 "wikilink")。
  - CPUコアを包む[ヒートスプレッダ](https://ja.wikipedia.org/wiki/ヒートスプレッダ "wikilink")の採用は、従来のAthlonシリーズに於ける、[ヒートシンク](https://ja.wikipedia.org/wiki/ヒートシンク "wikilink")装着作業時のコア回路破損、いわゆる「コア欠け」の防止に役立っている。
  - [メモリコントローラ](https://ja.wikipedia.org/wiki/メモリコントローラ "wikilink")内蔵により、アプリケーションの高速化が容易になった。一方、CPUとメモリの動作周波数の組み合わせが悪いと、自動的にメモリの動作周波数が規定値より低い状態になってしまう。これは、パフォーマンスより安定性を重視するために必要な処置であり、パフォーマンスを求めるのであれば正常に動作するメモリを選択すれば良いので、問題としては軽微である。
  - 製造プロセス微細化により発熱問題が改善された。そのため[オーバークロック](../Page/オーバークロック.md "wikilink")の耐性が大きく上がり、[コストパフォーマンス](https://ja.wikipedia.org/wiki/コストパフォーマンス "wikilink")に優れるAthlon64が話題になった。同社から出ている[Opteron](https://ja.wikipedia.org/wiki/Opteron "wikilink")プロセッサも話題を集め、[2005年](https://ja.wikipedia.org/wiki/2005年 "wikilink")はAMDの話題年となった。

### クロック自体の向上からクロックあたりの性能向上へ

Athlon 64を含めたK8シリーズの「実働クロック抑制、低発熱・省電力化」は、技術的な壁に突き当たり始めていた「クロック周波数による性能向上」というPC用プロセッサの流れに一石を投じ、「PC用プロセッサの性能イコールクロック周波数」という認識に変化をもたらした（ギガヘルツ神話の終焉）。[リーク電流](../Page/リーク電流.md "wikilink")の抑制に失敗し高発熱化してしまった[Pentium 4から](../Page/Pentium_4.md "wikilink")[自作機ユーザの眼を惹き付けることにも成功した](https://ja.wikipedia.org/wiki/自作パソコン "wikilink")。

しかしそれは結果的にインテルの失敗を自社に有利に利用する為のもので、明確な意図があったものではないと言える。[2000年](../Page/2000年.md "wikilink")[3月6日](https://ja.wikipedia.org/wiki/3月6日 "wikilink")、インテルが1GHzで動作する[Pentium IIIを](../Page/Pentium_III.md "wikilink")3月8日に発表する情報を事前に察知したAMDは予定を前倒しして、x86系初の1GHzを超えるCPUとしてAthlon 1GHzを発表した。インテルが[NetBurstマイクロアーキテクチャ](../Page/NetBurstマイクロアーキテクチャ.md "wikilink")で最終的に10GHzにまで到達すると予告した直後に、AMDもK8アーキテクチャで10GHzを予定していると発表している。しかしAMD自身K7後半（Pentium4普及直前頃）に既にAthlonXPでギガヘルツ路線を若干修正しており、さらにK8では「5年の歳月を経て求められるのはクロック周波数ではなく総合的な性能だ」として、[クロックあたりの命令実行数](https://ja.wikipedia.org/wiki/クロックあたりの命令実行数 "wikilink") (IPC) に重点を置いた[宣伝](../Page/宣伝.md "wikilink")をするようになった。

なお、「**ギガヘルツ神話**」という言葉は、K7時代のクロック向上競争の時期に、高IPC低クロックCPUである[PowerPC](../Page/PowerPC.md "wikilink")を採用していた「[アップルコンピュータ](https://ja.wikipedia.org/wiki/アップルコンピュータ "wikilink")」の[広告](../Page/広告.md "wikilink")に登場したものである。

### 利点

Athlon 64の利点としては、プロセッサの大胆な性能向上に対して[チップセット](../Page/チップセット.md "wikilink")の改良を必須としない（従来、チップセットの[ノースブリッジ](../Page/ノースブリッジ.md "wikilink")が持っていた機能のほとんどをプロセッサ側にパッケージングしている為）ので、[マザーボード](../Page/マザーボード.md "wikilink")の種類が豊富で、非常に安価なものから[ハイエンド](https://ja.wikipedia.org/wiki/ハイエンド "wikilink")用のものまで流通していた点が挙げられる。また、Athlon 64の最初の製品であるClawHammerの3200+から一貫してAMD64を搭載している（同系統のK8アーキテクチャの[Sempron](https://ja.wikipedia.org/wiki/Sempron "wikilink")では、当初はAMD64を無効化していた）。

また、上位製品である[AMD Phenom及びAthlon](../Page/AMD_Phenom.md "wikilink") X2の発売時点では、すでにCPUの大半が64ビット対応だったことからAthlon 64から**Athlon**に改称して販売を継続していた。AMD64が非搭載になったわけではない。

## 各世代についての詳細

以下のCPUコアの名称はAMD内部での開発[コードネーム](../Page/コードネーム.md "wikilink")である。

### Athlon 64

#### Clawhammer（クローハマー）

  - リビジョン: SH-C0, SH-CG
  - 製造プロセスルール: 130nm [SOI](https://ja.wikipedia.org/wiki/SOI "wikilink")
  - L1キャッシュ: 64 + 64 KiB
  - L2キャッシュ: 1024 KiB
  - 拡張機能: [MMX](https://ja.wikipedia.org/wiki/MMX "wikilink"), [Extended 3DNow\!](https://ja.wikipedia.org/wiki/3DNow!#Enhanced_3DNow! "wikilink"), [SSE](../Page/ストリーミングSIMD拡張命令.md "wikilink"), SSE2, [AMD64](https://ja.wikipedia.org/wiki/x64 "wikilink"), [Cool'n'Quiet](https://ja.wikipedia.org/wiki/Cool'n'Quiet "wikilink"), [NX Bit](../Page/NXビット.md "wikilink")（SH-CGのみ）
  - 対応ソケット: Socket 754またはSocket 939
  - HyperTransport（Socket 754版）: 800 MHz
  - HyperTransport（Socket 939版）: 1000 MHz
  - コア電圧: 1.50 V
  - TDP: 最大89W
  - リリース: 2003年9月23日
  - クロック周波数: 2000 - 2600 MHz

Socket 754版ではCool'n'Quietの最小クロック周波数と電圧が800MHz/1.3Vであったが、Socket 939版以降は、1GHz/1.1Vに変更されている。

#### Newcastle（ニューキャッスル）

ClawhammerのL2キャッシュ容量を半分に削減し、ダイサイズの縮小を図ったものである。

  - リビジョン: DH-CG
  - 製造プロセスルール: 130nm SOI
  - L1キャッシュ: 64 + 64 KiB
  - L2キャッシュ: 512 KiB
  - 拡張機能: MMX, Extended 3DNow\!, SSE, SSE2, AMD64, Cool'n'Quiet, NX Bit
  - 対応ソケット: Socket 754またはSocket 939
  - HyperTransport: 800 MHzまたは1000 MHz
  - コア電圧: 1.50 V
  - TDP: 最大89W
  - リリース: 2004年
  - クロック周波数: 1800 - 2400 MHz

#### Winchester（ウインチェスター）

90nm SOIで作成されたAthlon64プロセッサ。駆動電圧が1.4Vに低下するなど、130nm SOIに比べて更なる省電力化が図られている。また、WriteCombineキャッシュなどの改良も行われ、わずかではあるが処理性能が向上した。

  - リビジョン: DH-D0
  - 製造プロセスルール: 90nm SOI
  - L1キャッシュ: 64 + 64 KiB
  - L2キャッシュ: 512 KiB
  - 拡張機能: MMX, Extended 3DNow\!, SSE, SSE2, AMD64, Cool'n'Quiet, NX Bit
  - 対応ソケット: Socket 939
  - HyperTransport: 1000 MHz
  - コア電圧: 1.40 V
  - TDP: 最大67W
  - リリース: 2004年10月
  - クロック周波数: 1800 - 2200 MHz

#### Venice（ヴェニス）

WinchesterにSSE3命令が追加され、メモリコントローラの改良により、4バンク搭載時のDDR400動作が可能になったもの。

尚、市場価格維持、もしくは歩留りなどの都合により、Athlon64 X2のManchesterコアの一方のコアを無効として、VeniceコアのシングルコアAthlon64として販売されている場合がある（リビジョンは**DH-E4**）。このような製品は、オリジナルのVeniceコアと比較して消費電力が小さかったり発熱が低く抑えられていると言われている。

  - リビジョン: DH-E3, DH-E6
  - 製造プロセスルール: 90nm SOI
  - L1キャッシュ: 64 + 64 KiB
  - L2キャッシュ: 512 KiB
  - 拡張機能: MMX, Extended 3DNow\!, SSE, SSE2, SSE3, AMD64, Cool'n'Quiet, NX Bit
  - 対応ソケット: Socket 754またはSocket 939
  - HyperTransport（Socket 754版）: 800 MHz
  - HyperTransport（Socket 939版）: 1000 MHz
  - コア電圧: 1.35 V または 1.40 V
  - TDP: 最大67W
  - リリース: 2005年4月4日
  - クロック周波数: 1800 - 2400 MHz

#### San Diego（サンディエゴ）

ClawHammerの90nmプロセス製造版。SSE3命令が追加されているほか、メモリコントローラの改良により、4バンク搭載時のDDR400動作を可能にしている。

  - リビジョン: SH-E4, SH-E6
  - 製造プロセスルール: 90nm SOI
  - L1キャッシュ: 64 + 64 KiB
  - L2キャッシュ: 1024 KiB
  - 拡張機能: MMX, Extended 3DNow\!, SSE, SSE2, SSE3, AMD64, Cool'n'Quiet, NX Bit
  - 対応ソケット: Socket 939
  - HyperTransport: 1000 MHz
  - コア電圧: 1.35 V または 1.40 V
  - TDP: 最大89W
  - リリース: 2005年4月15日
  - クロック周波数: 2200 - 2600 MHz

#### Orleans（オルレアン）

90nm SOIで作成されたAthlon 64プロセッサ。メモリコントローラが変更されDDR2 SDRAMに移行した。これに伴い、940pinのSocket AM2に変更になった。TDP62Wの通常版の他にTDP35Wの低消費電力版が存在する。これらの製品を「K9」と呼ぶこともある。

  - リビジョン: DH-F2, DH-F3
  - 製造プロセスルール: 90nm SOI
  - L1キャッシュ: 64 + 64 KiB
  - L2キャッシュ: 512 KiB
  - 拡張機能: MMX, Extended 3DNow\!, SSE, SSE2, SSE3, AMD64, Cool'n'Quiet, NX Bit, [AMD-V](https://ja.wikipedia.org/wiki/x86仮想化 "wikilink")
  - 対応ソケット: Socket AM2
  - HyperTransport: 1000 MHz
  - コア電圧: 1.35 V または 1.40 V
  - TDP: 最大62W
  - リリース: 2006年5月23日
  - クロック周波数: 1800 - 2600 MHz

#### Lima（リマ）

65nm SOIで作成されたAthlon 64プロセッサ。製造プロセスルールの微細化で、消費電力が低下した。

  - リビジョン: G1
  - 製造プロセスルール: 65nm SOI
  - L1キャッシュ: 64 + 64 KiB
  - L2キャッシュ: 512 KiB
  - 拡張機能: MMX, Extended 3DNow\!, SSE, SSE2, SSE3, AMD64, Cool'n'Quiet, NX Bit, AMD-V
  - 対応ソケット: Socket AM2
  - HyperTransport: 1000 MHz
  - コア電圧: 1.25/1.35/1.40 V
  - TDP: 最大45W
  - リリース: 2007年2月20日
  - クロック周波数: 2200 - 2400 MHz

### Athlon

#### Orleans（オルレアン）

Athlon 64(Orleans)のEE版。L2キャッシュ容量が倍増している。

  - リビジョン: F3
  - 製造プロセスルール: 90nm SOI
  - L1キャッシュ: 64 + 64 KiB
  - L2キャッシュ: 1024 KiB
  - 拡張機能: MMX, Extended 3DNow\!, SSE, SSE2, SSE3, AMD64, Cool'n'Quiet, NX Bit, AMD-V
  - 対応ソケット: Socket AM2
  - HyperTransport: 1000 MHz
  - TDP: 最大45W
      - LE-1600: 2200 MHz
      - LE-1620: 2400 MHz
      - LE-1640: 2600 MHz

#### Lima（リマ）

65nmにシュリンクされたAthlon。90nm SOI版と比べ、L2キャッシュが削減されクロックが引き上げられている。[L2キャッシュ](https://ja.wikipedia.org/wiki/L2キャッシュ "wikilink")の容量の関係で、一部のアプリケーションでは上位製品であるAthlon LE-1660(65nm SOI)がAthlon LE-1640(90nm SOI)よりも遅いことがある。

  - リビジョン: G2
  - 製造プロセスルール: 65nm SOI
  - L1キャッシュ: 64 + 64 KiB
  - L2キャッシュ: 512 KiB
  - 拡張機能: MMX, Extended 3DNow\!, SSE, SSE2, SSE3, AMD64, Cool'n'Quiet, NX Bit, AMD-V
  - 対応ソケット: Socket AM2
  - HyperTransport: 1000 MHz
  - TDP: 最大45W
  - クロック周波数: 1600 - 2800 MHz
      - 2000+: 1000MHZ（組み込み向け、TDP8W）
      - 2600+: 1600MHZ（組み込み向け、TDP15W）
      - 2650e: 1600MHz（組み込み向け、TDP15W）
      - 3000+: 2000MHZ（組み込み向け、TDP25W）
      - LE-1640: 2700 MHz
      - LE-1660: 2800 MHz

### Athlon Neo

#### Huron（ヒューロン）

Yukonプラットフォームと共に発表された、ノートブック向け製品。シングルコアCPUで、RS690E＋SB600チップセットと組み合わせて利用する。ソケットは新形状のASB1。

  - 製造プロセスルール: 65nm SOI
  - L1キャッシュ: 64 + 64 KiB
  - L2キャッシュ: 512 KiB
  - 対応ソケット: Socket ASB1
  - TDP: 最大15W
      - MV-40: 1600 MHz

## CPUID

### Socket754モデル

  - F48h: ClawHammer SH-C0
  - F4Ah: ClawHammer SH-CG
  - FC0h: Newcastle DH-CG

### Socket939モデル

  - F7Ah: ClawHammer SH-CG
  - FF0h: Newcastle DH-CG
  - 10FF0h: Winchester DH-D0
  - 20F71h: San Diego SH-E4
  - 20FF0h: Venice DH-E3
  - 20FF2h: Venice DH-E6

## Socket 754

[サムネイル](https://ja.wikipedia.org/wiki/ファイル:Elitegroup_761GX-M754_-_Socket_754-5485.jpg "wikilink") **[Socket 754](https://ja.wikipedia.org/wiki/Socket_754 "wikilink")**（ソケット-）は、[マザーボード](../Page/マザーボード.md "wikilink")用の[CPUソケット](../Page/CPUソケット.md "wikilink")規格のひとつ。754個の電気的接点を有するピンホールがある。2003年9月のAthlon 64シリーズの発表と共に登場した。

対応するプロセッサはAthlon 64、Sempron、Turion 64。[DDR SDRAMメモリをサポートし](../Page/DDR_SDRAM.md "wikilink")、アクセスはシングルチャネルである。当初は[ワークステーション](../Page/ワークステーション.md "wikilink") / [サーバ](../Page/サーバ.md "wikilink")向けの [Socket 940](https://ja.wikipedia.org/wiki/Socket_940 "wikilink") [Opteron](https://ja.wikipedia.org/wiki/Opteron "wikilink") と共存するパフォーマンス[デスクトップ向けプラットフォームであったが](../Page/デスクトップパソコン.md "wikilink")、わずか半年ほど後の2004年4月にデュアルチャンネルに対応するAthlon 64とSocket 939プラットフォームが発表された。これ以後もSocket 754に対応したAthlon 64も投入はされていたものの、パフォーマンスデスクトップでSocket 754の商品価値が維持できた期間は短いものとなった。その後は[メインストリーム](https://ja.wikipedia.org/wiki/メインストリーム "wikilink")および[モバイル](https://ja.wikipedia.org/wiki/モバイル "wikilink")向けプラットフォームとしてSocket 939と共存する形となり、プラットフォームとしての寿命は後継のSocket 939より長いものとなった。

## Socket 939

[thumb](https://ja.wikipedia.org/wiki/ファイル:Sockel-939.jpg "wikilink") **[Socket 939](https://ja.wikipedia.org/wiki/Socket_939 "wikilink")**（ソケット-）は、マザーボード用のCPUソケット規格のひとつ。電気的接点を有するピンホールの数は、Opteron用のSocket 940より1個減じた939個。 2004年4月の[デュアルチャネル](https://ja.wikipedia.org/wiki/デュアルチャネル "wikilink")対応版Athlon 64と同時に発表された。対応するプロセッサは Athlon 64、[Athlon 64 X2](https://ja.wikipedia.org/wiki/Athlon_64_X2 "wikilink")、Opteronの他、一部の[Sempron](https://ja.wikipedia.org/wiki/Sempron "wikilink")も対応する。 2006年6月に後継となるDDR2 SDRAMに対応したプラットフォームとしてSocket AM2が発表され、Socket 939は終了した。

市場流通が終了してから2年以上が経過した[2009年](../Page/2009年.md "wikilink")10月、[DirectX](https://ja.wikipedia.org/wiki/Microsoft_DirectX "wikilink") ([Direct3D](https://ja.wikipedia.org/wiki/Direct3D "wikilink")) 10.1や [HDMI](https://ja.wikipedia.org/wiki/High-Definition_Multimedia_Interface "wikilink") をサポートする、最新の AMD 785G / SB 710 [チップセット](../Page/チップセット.md "wikilink")を搭載した Socket 939 用マザーボードが発売されている。 さらに[2010年](https://ja.wikipedia.org/wiki/2010年 "wikilink")8月末、AMD 790GX/SB750チップセットを搭載した[microATX](https://ja.wikipedia.org/wiki/microATX "wikilink")マザーボードが登場した。[1](http://akiba-pc.watch.impress.co.jp/hotline/20100828/etc_asrock.html)

## Socket AM2

[thumb](https://ja.wikipedia.org/wiki/ファイル:Socket_am2_retention_module.jpg "wikilink") **[Socket AM2](https://ja.wikipedia.org/wiki/Socket_AM2 "wikilink")**（ソケット-）は、マザーボード用のCPUソケット規格のひとつ。 電気的接点を有するピンホールの数は、Socket 939より1個増えた940個で、Opteronで用いられているSocket 940と接点の数では同じだが、[互換性](https://ja.wikipedia.org/wiki/互換性 "wikilink")は無く接点の配列も変えられている。

扱えるメモリが[DDR SDRAMから](../Page/DDR_SDRAM.md "wikilink")[DDR2 SDRAMに移行し](../Page/DDR2_SDRAM.md "wikilink")、これまで[OEM](../Page/OEM.md "wikilink")版を除いてSocket 754版のみであったSempronもこのソケットに移行し、プラットフォームが統一された。また、AMD-Vにも対応した（Sempronを除く）。これにより、Athlon 64およびAthlon 64 X2、[Athlon 64 FX](../Page/Athlon_64_FX.md "wikilink") はDDR2 800まで、Sempron はDDR2 667まで扱うことが出来るようになり、メモリ周りがさらに強化された。

## 関連項目

  - [Cool'n'Quiet](https://ja.wikipedia.org/wiki/Cool'n'Quiet "wikilink")

## 外部リンク

  - [AMD Athlon™ 64 プロセッサ・ファミリ](http://www.amd.com/jp-ja/Processors/ProductInformation/0,,30_118_9484,00.html?redir=JPHM3)

[Category:AMDのマイクロプロセッサ](https://ja.wikipedia.org/wiki/Category:AMDのマイクロプロセッサ "wikilink")
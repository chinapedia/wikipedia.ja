> この記事は[SIMD](https://ja.wikipedia.org/wiki/SIMD)から翻訳されています。


**ストリーミングSIMD拡張命令**（、略称:**SSE**）は、[インテル](https://ja.wikipedia.org/wiki/インテル "wikilink")が開発した[CPU](../Page/CPU.md "wikilink")の[SIMD](https://ja.wikipedia.org/wiki/SIMD "wikilink")拡張[命令セット](https://ja.wikipedia.org/wiki/命令セット "wikilink")、およびその拡張版の総称である。

## 概要

SSEは、[x86](https://ja.wikipedia.org/wiki/x86 "wikilink")[アーキテクチャに](../Page/コンピュータ・アーキテクチャ.md "wikilink")8本の[128ビット](https://ja.wikipedia.org/wiki/128ビット "wikilink")[レジスタを新設し](../Page/レジスタ_\(コンピュータ\).md "wikilink")、[浮動小数点演算のSIMD処理を実現したものである](../Page/浮動小数点数.md "wikilink")。[AMD](https://ja.wikipedia.org/wiki/AMD "wikilink")の[K6-2に実装されたSIMD拡張命令](../Page/AMD_K6-2.md "wikilink")[3DNow\!](../Page/3DNow!.md "wikilink")に対抗する形で[Pentium IIIから実装された](../Page/Pentium_III.md "wikilink")。4個の[32ビット](../Page/32ビット.md "wikilink")単精度[浮動小数点データを一本のレジスタに格納し](../Page/浮動小数点数.md "wikilink")、同一の命令を一括処理することが出来る。拡張命令であるため、その機能を使用するためにはSSEに対応した[ソースコード](../Page/ソースコード.md "wikilink")を作成し、[プログラムを](../Page/プログラム_\(コンピュータ\).md "wikilink")[コンパイルする必要がある](../Page/コンパイラ.md "wikilink")。

[Core Duoまでのインテル製CPU](https://ja.wikipedia.org/wiki/Core_Duo "wikilink")、K8までの[AMD製CPUでは](https://ja.wikipedia.org/wiki/アドバンスト・マイクロ・デバイセズ "wikilink")、[64ビット](https://ja.wikipedia.org/wiki/64ビット "wikilink")幅の演算器を用いて128ビット演算命令を2[クロック](../Page/クロック.md "wikilink")かけて実行するという実装であったため、128ビット演算命令を用いても実質的な[スループット](../Page/スループット.md "wikilink")は[クロック](../Page/クロック.md "wikilink")あたり64ビットであった（SIMD整数演算に関しては[Pentium M](https://ja.wikipedia.org/wiki/Pentium_M "wikilink")、Core DuoやK8では64ビット幅の演算器を2つ持つため、コア全体でのSIMD整数演算のスループットは128ビット/クロックであった）。そのため従来から存在する[MMX](https://ja.wikipedia.org/wiki/MMX "wikilink")命令やAMDの[3DNow\!](../Page/3DNow!.md "wikilink")命令に対する性能面でのアドバンテージは128ビット幅のレジスタを使えるという点以外では小さく、むしろ並列度が上がった分だけ最適化も煩雑になるという欠点が目立った。また当時の[RISC](../Page/RISC.md "wikilink")系CPUに搭載されているSIMD命令では128ビット演算命令を1クロックで実行できるものがあり、これらに対する性能的なディスアドバンテージは小さくなかった。最終的には[Coreマイクロアーキテクチャ](../Page/Coreマイクロアーキテクチャ.md "wikilink")/[AMD K10より](../Page/AMD_K10.md "wikilink")128ビット演算命令も1クロック処理が可能な形態へと改良され、SSE命令の実用性は大幅に向上した。

元々は**インターネット・ストリーミングSIMD拡張命令**（、ISSE）と呼ばれていたが \[1\]、命令内容そのものは[インターネット](https://ja.wikipedia.org/wiki/インターネット "wikilink")とは直接関係が無く[マーケティング](../Page/マーケティング.md "wikilink")的な要素が強かったため、現在ではインターネットの文言が外され単にSSEと呼ばれるようになっている。

SSEの機能を強化したものにSSE2やSSE3、SSSE3（Supplemental/補足的なSSE3）、SSE4がある。また、SSEは他社製品にも採用されている。

## SSE

Pentium IIIにはじめて実装された。追加された命令数は70\[2\]。Pentium IIIの開発[コードネーム](../Page/コードネーム.md "wikilink")が*[Katmai](https://ja.wikipedia.org/wiki/Pentium_III#第一世代“カトマイ”_\(Katmai\) "wikilink")*であったことから、**KNI** () \[3\]や**[MMX](https://ja.wikipedia.org/wiki/MMX "wikilink")2** \[4\]とも呼ばれていた。廉価製品の[Celeron](https://ja.wikipedia.org/wiki/Celeron "wikilink")においても、その第三世代製品 *[Coppermine-128k](https://ja.wikipedia.org/wiki/Celeron#Coppermine-128k "wikilink")* よりSSEに対応している\[5\]\[6\]。

[AMDによるSIMD拡張命令セット](https://ja.wikipedia.org/wiki/アドバンスト・マイクロ・デバイセズ "wikilink")[3DNow\! Professionalは](https://ja.wikipedia.org/wiki/3DNow!#3DNow!_Professional "wikilink")、SSEと[互換性](https://ja.wikipedia.org/wiki/互換性 "wikilink")がある\[7\]\[8\]。

## SSE2

SSE2は従来のSSEに144個の新たな命令が加えられた。具体的には64ビットの倍精度浮動小数点演算のサポート及びMMXを128ビット幅に拡張する整数演算命令の追加、[キャッシュの制御機能の強化がなされた](../Page/キャッシュメモリ.md "wikilink")。

SSE2はPentium 4で初めて実装された\[9\]。AMDの[AMD64アーキテクチャでは](https://ja.wikipedia.org/wiki/x64 "wikilink")、浮動小数点演算に従来の[x87](https://ja.wikipedia.org/wiki/x87 "wikilink")命令ではなくSSE/SSE2のスカラ演算命令を用いることを標準としたため、拡張命令ではなく基本命令としてSSE、SSE2が取り込まれている 。

## SSE3

SSE3はSSE2に13個の新たな命令が加えられた。具体的にはメモリアクセス及び[複素数](../Page/複素数.md "wikilink")計算の高速化、仮想CPUの[スレッドの動作制御などの機能が搭載され](../Page/スレッド_\(コンピュータ\).md "wikilink")、主に動画圧縮の処理が向上した。

SSE3の名称が発表される前は**PNI** () と呼ばれていた。[Pentium 4のPrescottコアで初めて実装された](../Page/Pentium_4.md "wikilink")。

## SSSE3

SSSE3 ()はSSE3に32個の新たな命令が加えられた。 [Coreマイクロアーキテクチャベースのマイクロプロセッサで初めて実装された](https://ja.wikipedia.org/wiki/Intel_Core_2 "wikilink")。

SSSE3と名付けられる前は**MNI** (; 旧称) という名称があった。登場当初はSSE4と呼ばれると一般的には思われていた。

## SSE 4

### SSE4.1

45nm世代のCore 2のPenrynで搭載。47個の命令が追加になる。

### SSE4.2

[Nehalemマイクロアーキテクチャ](https://ja.wikipedia.org/wiki/Nehalemマイクロアーキテクチャ "wikilink") の第1世代Intel Core iで初めて実装された。7個の命令を追加。SSE 4.2の追加命令は以下の通り。

  - (STTNI)

      - PCMPESTRI
      - PCMPESTRM
      - PCMPISTRI
      - PCMPISTRM
      - PCMPGTQ

  - (ATA)

      - [CRC-32](https://ja.wikipedia.org/wiki/CRC-32 "wikilink")
      - POPCNT - [ビットが立っている数を数える](https://ja.wikipedia.org/wiki/ハミング重み "wikilink")

## SSE4a

[AMD Phenomで搭載](../Page/AMD_Phenom.md "wikilink")。 キャッシュ関連や挿入、展開の4命令が追加。インテルのSSE4とは名前は似ているが互換性は無い。

## Intel AVX

MMX/SSE後継のSIMD拡張命令セットで、呼称がとなった。[Sandy Bridgeマイクロアーキテクチャで初めて搭載された](https://ja.wikipedia.org/wiki/Sandy_Bridgeマイクロアーキテクチャ "wikilink")\[10\]\[11\]。浮動小数点演算の演算幅がSSEの2倍の256ビットとなり、1命令で8つの単精度浮動小数点演算もしくは4つの倍精度浮動小数点演算を実行することができる。また、命令デコード性能向上のため、新しい命令フォーマット（VEXエンコーディング）が採用されている。3 or 4オペランドの非破壊型命令もサポートするため、レジスタ退避・復元処理の記述を省くことができる。この非破壊型の命令フォーマットに関しては従来の128ビット幅のSSE命令にも使うことができるため、AVXに対応したプロセッサでは新規に導入された256ビット命令を使わなくてもSIMD演算の性能が向上する可能性がある。

SSEが導入された際には専用の128ビットレジスタが新設されたが、AVXの256ビットレジスタは下位の128ビットを既存のSSEレジスタと共有している。そのためSSE命令とAVX命令の間でのデータ交換は容易である。ただし、256ビットのAVX命令と既存のSSE命令を混在させると、SSE命令を実行する際にAVXレジスタの上位128ビットを退避するというペナルティが発生するため、パフォーマンスが落ちる。これを避けるためには、256ビット命令の実行後にVZEROUPPER/VZEROALL命令を実行して明示的にAVXレジスタの上位128ビットをクリアするか、SSE命令をVEXエンコーディングを使ったものに置き換える必要がある。VEXエンコーディングの128ビット命令はAVXレジスタの上位128ビットを保持せずにゼロクリアするという挙動になっており、AVXレジスタの部分的な書き換えが発生しないためである。

Sandy Bridgeでは当初のSSEの実装のように既存の128ビットの演算器を使って2サイクルで実行するようなことはせず、素直に乗算器や加算器などの演算器が256ビット幅に拡張されている。これによって、実質的なピーク浮動小数点演算性能が[Nehalem世代の](https://ja.wikipedia.org/wiki/Nehalemマイクロアーキテクチャ "wikilink")2倍となっている。

AMDは[Bulldozer世代向けに当初予定していたSSE](https://ja.wikipedia.org/wiki/Bulldozer_\(マイクロアーキテクチャ\) "wikilink")5拡張命令をキャンセルし、[AMD FXではAVXがサポートされることになった](https://ja.wikipedia.org/wiki/AMD_FX "wikilink")。ただし、256ビット命令に関しては128ビット幅の演算器を2つ使って実行しており\[12\]\[13\]、スループットは従来のSSE命令と変わらない。

## Intel AVX2

インテルは[Haswellマイクロアーキテクチャ](https://ja.wikipedia.org/wiki/Haswellマイクロアーキテクチャ "wikilink")から搭載\[14\]。従来のSIMD整数演算命令が128ビットから256ビットに拡張されるのが主な変更点であるが、要素ごとに独立したシフト量を設定できるシフト命令、非連続なデータを並べ替えながらロードが可能なギャザー命令等の新たな命令も実装される。AMDは[ExcavatorアーキテクチャからAVX](https://ja.wikipedia.org/wiki/Excavator_\(マイクロアーキテクチャ\) "wikilink")2を実装している\[15\]。

## Intel AVX-512

512ビット長のZMMレジスタを新設する\[16\]。レジスタ数も16から32に増える。Knights Landingの[Xeon Phiに初めて搭載](https://ja.wikipedia.org/wiki/Xeon_Phi "wikilink")。

[Xeon](../Page/Xeon.md "wikilink")プロセッサは[Skylakeマイクロアーキテクチャ](https://ja.wikipedia.org/wiki/Skylakeマイクロアーキテクチャ "wikilink")から一部の命令を搭載\[17\]。[Xeon](../Page/Xeon.md "wikilink")以外では[Core i9にも搭載されている](https://ja.wikipedia.org/wiki/Intel_Core_i9 "wikilink")。

## FMA (Fused Multiply-Add)

x86プロセッサにおいて[積和演算](../Page/積和演算.md "wikilink")を実現するための拡張命令\[18\]がFMAである。2007年にAMDがSSE5命令の一部として、2008年にインテルがAVX命令のサブセットとして採用を発表したが、両者の仕様は異なるものであった\[19\]。その後、インテルは2009年初頭にFMA命令の仕様を変更し、4オペランド (FMA4) をやめ3オペランド形式 (FMA3) とした。2009年5月にはAMDがSSE5命令の採用を取りやめ、AVXのサポートを表明したため、仕様の統一が図られたかと思われたが、FMA命令に関してはインテルが仕様を変更する前の4オペランド版FMAを採用したため、FMA4とFMA3という二系統のFMA命令が混在していた。その後、AMDが[ZenマイクロアーキテクチャでFMA](https://ja.wikipedia.org/wiki/Zen_\(マイクロアーキテクチャ\) "wikilink")4の削除及びサポートの打ち切りを表明したことで、FMA命令についても仕様の統一が図られた\[20\]。

FMA命令では±(A×B)±Cの形で表現される単精度/倍精度の浮動小数点演算を1命令で実行できる。乗算結果の符号を反転するか、乗算後に加算を行うか減算を行うかによって以下の4つのバリエーションがある。

  - MADD
    A×B＋C
  - MSUB
    A×B－C
  - NMADD
    －(A×B)＋C
  - NMSUB
    －(A×B)－C

いずれの命令も単精度/倍精度、スカラ/ベクタを問わず全てのタイプの演算に適用可能である。他にもベクタ専用のMADDSUB命令が存在し、1,3,5...番目の要素にMADDを、0,2,4...番目の要素にMSUBを行うという命令になっている。

FMA命令に対応した演算器においては、上記の浮動小数点演算を1クロックサイクルのスループットで実行可能で、加算のみ、乗算のみを実行できる演算器と比較すると理論FLOPSを倍にすることができる。また、乗算の結果に対しては丸めを行わず、加算を行った後に一度だけ丸めを行うため、乗算と加算を独立して実行するのと比較して丸め誤差を小さくできるという利点もある。実装としてはAMDではBulldozerマイクロアーキテクチャでサポートされたのが最初で、モジュールあたり2つの128ビットFMA演算器を搭載している。インテルはHaswellマイクロアーキテクチャで初めてサポートしており、コアあたり2つの256ビットFMA演算器を搭載している\[21\]。

### FMA4

インテルが2008年に発表した時点でのFMA命令セット。完全な4オペランドを実現しており、3つのソースオペランドとディスティネーションオペランドを独立に指定できる。その後インテルは仕様を変更したために採用を取りやめたが、AMDはBulldozerマイクロアーキテクチャにおいてこの命令セットをサポートし続けていた。その後AMDが発表したZenマイクロアーキテクチャで削除されることとなった。

### FMA3

インテルが2009年に仕様を変更し、現在使われているFMA命令セット。4オペランド方式をやめ、3つのソースオペランドのうち任意の1つを破壊することにより3オペランドでFMAを実現している。インテルはHaswellマイクロアーキテクチャ以降で、AMDはBulldozerマイクロアーキテクチャのPiledriverコア以降でサポートしている。なお、AMDが当初SSE5において採用したFMA命令も同じ3オペランド方式であった\[22\]。

FMA4と比べるとレジスタの退避を行う必要がある場合に不利であるが、命令長を1バイト短くすることができるため、デコーダの実装や命令キャッシュのフットプリントでは有利である。インテルの[Ivy Bridgeマイクロアーキテクチャ以降やAMDのBulldozerマイクロアーキテクチャでは](https://ja.wikipedia.org/wiki/Ivy_Bridgeマイクロアーキテクチャ "wikilink")、[レジスタ・リネーミング](https://ja.wikipedia.org/wiki/レジスタ・リネーミング "wikilink")によってレジスタ間のmov命令をゼロレイテンシで実行できるため、これと組み合わせればレジスタ退避のペナルティは軽減できる。

インテルのマイクロプロセッサにおいてはAVX2命令と同時に採用されたため、AVX2命令の一部であると誤解されることがある。しかし、両者の[CPUID](../Page/CPUID.md "wikilink")フラグは独立に設けられており、必ずしも両者が同時にサポートされているとは限らない（例えば、FMA3をサポートするAMDのPiledriverコアではAVX2命令はサポートしていない）。

## 歴史

  - [1999年](../Page/1999年.md "wikilink") [2月](https://ja.wikipedia.org/wiki/2月 "wikilink"): インテルが[SSE搭載の](https://ja.wikipedia.org/wiki/#SSE "wikilink")[Pentium IIIプロセッサを発表](../Page/Pentium_III.md "wikilink")。
      - [2000年](../Page/2000年.md "wikilink") [3月](https://ja.wikipedia.org/wiki/3月 "wikilink"): インテルがSSE搭載の[Celeron](https://ja.wikipedia.org/wiki/Celeron "wikilink")プロセッサを発表。
  - [2000年](../Page/2000年.md "wikilink") [11月](../Page/11月.md "wikilink"): インテルが[SSE2搭載のPentium](https://ja.wikipedia.org/wiki/#SSE2 "wikilink") 4プロセッサを発表。
      - [2002年](../Page/2002年.md "wikilink") [5月](https://ja.wikipedia.org/wiki/5月 "wikilink"): インテルがSSE2搭載のCeleronプロセッサを発表。
      - [2003年](../Page/2003年.md "wikilink") [3月](https://ja.wikipedia.org/wiki/3月 "wikilink"): インテルがSSE2搭載の[Pentium Mプロセッサを発表](https://ja.wikipedia.org/wiki/Pentium_M "wikilink")。
      - [2004年](../Page/2004年.md "wikilink") [1月](https://ja.wikipedia.org/wiki/1月 "wikilink"): インテルがSSE2搭載の[Celeron Mプロセッサを発表](https://ja.wikipedia.org/wiki/Celeron#Celeron_M "wikilink")。
  - [2004年](../Page/2004年.md "wikilink") [2月](https://ja.wikipedia.org/wiki/2月 "wikilink"): インテルが[SSE3搭載のPentium](https://ja.wikipedia.org/wiki/#SSE3 "wikilink") 4 プロセッサを発表。
      - [2004年](../Page/2004年.md "wikilink") [6月](../Page/6月.md "wikilink"): インテルがSSE3搭載の[Celeron Dプロセッサを発表](https://ja.wikipedia.org/wiki/Celeron#Celeron_D "wikilink")。
      - [2006年](https://ja.wikipedia.org/wiki/2006年 "wikilink") [1月](https://ja.wikipedia.org/wiki/1月 "wikilink"): インテルがSSE3搭載の[Intel Core](../Page/Intel_Core.md "wikilink") プロセッサを発表。
  - [2006年](https://ja.wikipedia.org/wiki/2006年 "wikilink") [6月](../Page/6月.md "wikilink"): インテルが[SSSE3搭載の](https://ja.wikipedia.org/wiki/#SSSE3 "wikilink")[Xeon 5100プロセッサを発表](../Page/Xeon.md "wikilink")。
      - [2006年](https://ja.wikipedia.org/wiki/2006年 "wikilink") [7月](https://ja.wikipedia.org/wiki/7月 "wikilink"): インテルがSSSE3搭載の[Intel Core 2プロセッサを発表](https://ja.wikipedia.org/wiki/Intel_Core_2 "wikilink")。
  - [2007年](../Page/2007年.md "wikilink") [8月](../Page/8月.md "wikilink"): AMDがSSE5を発表。
  - [2007年](../Page/2007年.md "wikilink") [11月](../Page/11月.md "wikilink"): インテルが[SSE4.1搭載のIntel](https://ja.wikipedia.org/wiki/#SSE4.1 "wikilink") Core 2プロセッサを発表。
  - [2007年](../Page/2007年.md "wikilink") [11月](../Page/11月.md "wikilink"): AMDが[SSE4a搭載の](https://ja.wikipedia.org/wiki/#SSE4a "wikilink")[Phenom](https://ja.wikipedia.org/wiki/Phenom "wikilink")を発表。
  - [2008年](https://ja.wikipedia.org/wiki/2008年 "wikilink") [11月](../Page/11月.md "wikilink"): インテルが[SSE4.2搭載の第一世代](https://ja.wikipedia.org/wiki/#SSE4.2 "wikilink")[Intel Core i7プロセッサを発表](https://ja.wikipedia.org/wiki/Intel_Core_i7 "wikilink")。
  - [2011年](../Page/2011年.md "wikilink") [1月](https://ja.wikipedia.org/wiki/1月 "wikilink"): インテルが[AVX](https://ja.wikipedia.org/wiki/AVX "wikilink")搭載の第二世代Intel Core i7プロセッサを発表。
  - [2011年](../Page/2011年.md "wikilink") [10月](https://ja.wikipedia.org/wiki/10月 "wikilink"): AMDが[FMA搭載の](https://ja.wikipedia.org/wiki/#FMA "wikilink")[AMD FXプロセッサを発表](https://ja.wikipedia.org/wiki/AMD_FX "wikilink")。
  - [2013年](../Page/2013年.md "wikilink") [6月](../Page/6月.md "wikilink"): インテルが[AVX2搭載の第四世代Intel](https://ja.wikipedia.org/wiki/#Intel_AVX2 "wikilink") Core i7プロセッサを発表。
  - [2016年](../Page/2016年.md "wikilink") [6月](../Page/6月.md "wikilink"): インテルが[AVX-512搭載のIntel](https://ja.wikipedia.org/wiki/#Intel_AVX-512 "wikilink") [Xeon Phiコプロセッサを発表](https://ja.wikipedia.org/wiki/Xeon_Phi "wikilink")。

## 脚注

### 出典

## 関連項目

  - [MMX](https://ja.wikipedia.org/wiki/MMX "wikilink")
  - [3DNow\!](../Page/3DNow!.md "wikilink")
  - [AltiVec](../Page/AltiVec.md "wikilink") (Velocity Engine)

[カテゴリ:CPU](https://ja.wikipedia.org/wiki/カテゴリ:CPU "wikilink") [カテゴリ:並列コンピューティング](https://ja.wikipedia.org/wiki/カテゴリ:並列コンピューティング "wikilink") [カテゴリ:X86アーキテクチャ](https://ja.wikipedia.org/wiki/カテゴリ:X86アーキテクチャ "wikilink")

1.
2.
3.
4.
5.
6.
7.
8.
9.
10.
11.
12.
13.
14.
15.
16.
17.  AVX512F, AVX512CDのみ搭載されている旨が判る。
18. 乗算と加算あるいは減算を融合させた命令はAMDのBulldozer以前にも、HPのPA-RISCやIBMのPower、PowerPC、インテルのItaniumにも実装されていた。
19.
20.
21.
22.
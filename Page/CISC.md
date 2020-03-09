> この記事は[CISC](https://ja.wikipedia.org/wiki/CISC)から翻訳されています。


**CISC**（しすく、）は、[コンピュータ](../Page/コンピュータ.md "wikilink")の[命令セット](https://ja.wikipedia.org/wiki/命令セット "wikilink")アーキテクチャ(ISA)の設計の方向性の一つである。単純な命令を指向した[RISC](../Page/RISC.md "wikilink")が考案されたときに、対比して（[レトロニム](https://ja.wikipedia.org/wiki/レトロニム "wikilink")）従来のISAは複雑であるとして、"Complex" の語を用いた "CISC" と呼ばれる様になった。典型的なCISCのISAはしばしば、単一の命令で複数の処理を行う、可変長命令である、[直交性がある](https://ja.wikipedia.org/wiki/直交性_\(情報科学\) "wikilink")、演算命令の[オペランドにメモリを指定できる](https://ja.wikipedia.org/wiki/被演算子 "wikilink")、などで特徴づけられる。

CISCを採用した[プロセッサ](../Page/プロセッサ.md "wikilink")([CPU](../Page/CPU.md "wikilink"))をCISCプロセッサと呼ぶ。CISCプロセッサに分類されるプロセッサとしては、[マイクロプログラム方式](https://ja.wikipedia.org/wiki/マイクロプログラム方式 "wikilink")を採用した[System/360](https://ja.wikipedia.org/wiki/System/360 "wikilink")、[PDP-11](https://ja.wikipedia.org/wiki/PDP-11 "wikilink")、[VAX](https://ja.wikipedia.org/wiki/VAX "wikilink")などや、[マイクロプロセッサ](../Page/マイクロプロセッサ.md "wikilink")の[680x0](../Page/MC68000.md "wikilink")、[x86](https://ja.wikipedia.org/wiki/x86 "wikilink")などがある。

## 概要

現在は、[x86](https://ja.wikipedia.org/wiki/x86 "wikilink")互換[プロセッサ](../Page/プロセッサ.md "wikilink")がCISCに分類されるが、[ARMアーキテクチャ](https://ja.wikipedia.org/wiki/ARMアーキテクチャ "wikilink")\[1\]もCISCで特徴付けられる性格を持つ。古くに設計された[ミニコンピュータ](https://ja.wikipedia.org/wiki/ミニコンピュータ "wikilink")や[メインフレーム](../Page/メインフレーム.md "wikilink")もCISCに分類されるほか、[米](https://ja.wikipedia.org/wiki/アメリカ合衆国 "wikilink")[モトローラ](../Page/モトローラ.md "wikilink")社の[MC 680x0](https://ja.wikipedia.org/wiki/68000 "wikilink") (68K) 系プロセッサもCISCの系譜に含められる。命令語長が可変長であるため、ある一つの命令のデコードが終わらなければ次の命令の語の位置が判らず、複数の命令を同時にデコードするのが困難という欠点が指摘された\[2\]。

プログラミングでアセンブラ言語が用いられていた頃には豊富な[アドレッシングモード](https://ja.wikipedia.org/wiki/アドレッシングモード "wikilink")を備えて、命令の[直交性を備えることが良いと考えられていた](https://ja.wikipedia.org/wiki/直交性_\(情報科学\) "wikilink")。すなわち任意の演算で、どのアドレッシングモードでも使えるのが良いとされた。演算はレジスターレジスタ間演算のほかに、レジスターメモリ演算、メモリ－メモリ演算を備えているのが普通で、オペランドは2オペランドまたは3オペランドまで指定できるタイプが多い。つまり、メモリ1の内容とメモリ2の内容を論理積を取ってメモリ3に格納するというようなことが1命令でできる。[C言語](../Page/C言語.md "wikilink")の[条件演算子](https://ja.wikipedia.org/wiki/条件演算子 "wikilink") "?:"はCISCであった[PDP-11](https://ja.wikipedia.org/wiki/PDP-11 "wikilink")が備えていた命令の名残りとされる。

インデックスアドレッシング時のオフセットも命令で指定されるデータ語長に合わせてスケーリングされることが多い。また、データ語長の異なるデータ間の演算でも演算前に自動的に符号拡張などが行なわれるため、データ長を揃える命令を省略できる場合が多い。データの境界をメモリ上の何処にでも置ける。 1命令中で行なう処理が複雑なため、[マイクロプログラム方式](https://ja.wikipedia.org/wiki/マイクロプログラム方式 "wikilink")で実装されることが多い。

## 構造

実行ユニットの演算器の幅を1/8語、1/4語、1/2語、1語、2語、3語、4語・・・と、実行速度と回路資源のトレードオフを図りながら自在に構成することが可能で柔軟性を持つ。[マイクロプログラム方式](https://ja.wikipedia.org/wiki/マイクロプログラム方式 "wikilink")にすることで同じインストラクションセットを維持したまま、内部[マイクロアーキテクチャ](https://ja.wikipedia.org/wiki/マイクロアーキテクチャ "wikilink")を増強していくことができる。マイクロプログラミング方式とはマイクロアーキテクチャたる内部CPUが万能チューリングマシンとして外部CPUをシミュレートすることである。その時点の実装技術で最も有効な内部CPUが外部CPUをシミュレートして後方互換性を維持する。このようにCISCは後方互換性を維持したまま持続的に性能と機能を向上できるアーキテクチャである。

## 歴史

初期のCPUは半導体の集積度が低いため、内部の演算器や実行ユニットのbit長がワード長より大幅に短かった。典型的には32bit＝1ワードに対して演算器は4bitで8回の演算を繰り返して32bit同士の計算を実行していた。この繰り返し演算が命令における実行ステージを複数のステートに分けて処理していた。このようなアーキテクチャを[ビットスライス](https://ja.wikipedia.org/wiki/ビットスライス "wikilink")プロセッサと呼び、実行ユニットが4bitの場合に16進アーキテクチャと呼ばれた。

半導体の集積度が向上するにしたがって演算器のビット幅は増加し、CPUの内部構造は変更される。インストラクションセットの互換性を保ったまま内部アーキテクチャを容易に更新するために[マイクロプログラム方式](https://ja.wikipedia.org/wiki/マイクロプログラム方式 "wikilink")が採用された。CISCは当初から単純なマイクロアーキテクチャで豊富な機能を実現するためにマイクロプログラム方式を使っていた。実行ステージの処理に時間がかかるのでメモリレイテンシは問題ではなかった。メモリ間演算は理にかなっていた。

半導体の集積度が向上し、単一CPUの実行パイプラインが1/8語、1/4語、1/2語、1語実行ユニットと向上したときにRISCコンセプトが標榜された。RISCは1チップに集積されたCMOSマイクロプロセッサが32bit 1ワード実行ユニットで固定されるという前提に立って、単純化した構造で最適化すればCISCに勝てると考えていたようである。しかしCMOS半導体の集積度は向上し続け、スケーリング則により内部クロックは高速化し続けた。相対的にオンチップキャッシュのメモリレイテンシは増え続け、前提はすぐに崩れた。

CISCは引き続きCMOS半導体の集積度の向上に伴って、単一CPUのパイプラインを2語、3語、4語同時実行ユニットに向上した。複数実行ユニットにする方法が[スーパースケーラ](https://ja.wikipedia.org/wiki/スーパースケーラ "wikilink")であり、更にその実行ユニット数を向上させる手法が[アウトオブオーダ実行](https://ja.wikipedia.org/wiki/アウト・オブ・オーダー実行 "wikilink")、[投機的実行](https://ja.wikipedia.org/wiki/投機的実行 "wikilink")である。これらは増加したメモリレイテンシの時間を有効利用して、複数可変長パイプライン実行ユニットに対して[レジスタリネーミング](https://ja.wikipedia.org/wiki/レジスタリネーミング "wikilink")を割り当てる複雑な内部構造になる。

このように、CISCは半導体の集積度の向上に伴い多数の実行ユニットに自動的に[命令パイプライン](https://ja.wikipedia.org/wiki/命令パイプライン "wikilink")を割り当てるマイクロアーキテクチャを発達させ、ソフトウェアを書き換えることなく性能の向上を実現してきたが、[2004年](https://ja.wikipedia.org/wiki/2004年 "wikilink")ごろにはCISCのマイクロアーキテクチャが過度に複雑化したことで演算性能向上は限界に達し、マイクロプロセッサの高速化は[マルチコア](https://ja.wikipedia.org/wiki/マルチコア "wikilink")、[同時マルチスレッディング](https://ja.wikipedia.org/wiki/同時マルチスレッディング "wikilink")、[SIMD](https://ja.wikipedia.org/wiki/SIMD "wikilink")による性能向上に舵を切っている。これらの並列化手法による性能向上を享受するには、ソフトウェアの書き換えが必要になる。

## 現状

[1990年代](../Page/1990年代.md "wikilink")には「CISCはRISCに置き換わる」との予測もあったが、実際にはCISCプロセッサの多くは内部的にRISCの技術を採用し、一方でRISCプロセッサの多くは命令数の追加を続けたため、[2000年代](../Page/2000年代.md "wikilink")には技術的な相違はほぼ消滅した。このため現在の「CISC」や「RISC」は、技術的な用語よりも、各プロセッサの歴史的な総称として使われているにすぎない。

「CISC」は「[x86](https://ja.wikipedia.org/wiki/x86 "wikilink")および[x64](https://ja.wikipedia.org/wiki/x64 "wikilink")や、伝統的なメインフレームやミニコンピュータの各専用プロセッサなど」、「RISC」は「[SPARC](https://ja.wikipedia.org/wiki/SPARC "wikilink")、[MIPS](https://ja.wikipedia.org/wiki/MIPSアーキテクチャ "wikilink")、[ARM](https://ja.wikipedia.org/wiki/ARMアーキテクチャ "wikilink")、[PA-RISC](https://ja.wikipedia.org/wiki/PA-RISC "wikilink")、[POWERなどの](https://ja.wikipedia.org/wiki/POWER_\(マイクロプロセッサ\) "wikilink")[マイクロプロセッサ](../Page/マイクロプロセッサ.md "wikilink")」の意味で使われる場合が多い。なお[IA-64](https://ja.wikipedia.org/wiki/IA-64 "wikilink")はPA-RISCの後継でもあるが、[EPICアーキテクチャ](https://ja.wikipedia.org/wiki/EPICアーキテクチャ "wikilink")という独自のアーキテクチャを採用しており、RISCには分類しない場合が多い。また32ビット[ARM](https://ja.wikipedia.org/wiki/ARMアーキテクチャ "wikilink")（64ビットARMは典型的なRISCに近い）や、POWER・PowerPCはRISCの典型からは外れたアーキテクチャだが、一般的にはどちらもRISCに分類される。

[2015年](../Page/2015年.md "wikilink")現在の各市場での採用傾向は以下である。

  - [パーソナルコンピュータ](../Page/パーソナルコンピュータ.md "wikilink")市場（[PC/AT互換機](https://ja.wikipedia.org/wiki/PC/AT互換機 "wikilink")および[Macintosh](../Page/Macintosh.md "wikilink")）では、CISC([x86](https://ja.wikipedia.org/wiki/x86 "wikilink"))がほぼ独占している（PowerPCやARMを搭載したパソコンも存在するが、シェアは極めて小さい）。
  - [UNIX](../Page/UNIX.md "wikilink")[サーバ](../Page/サーバ.md "wikilink")ー市場は、ローエンドはCISC(x86)、ハイエンドは各社RISC（[SPARC](https://ja.wikipedia.org/wiki/SPARC "wikilink")、[POWERなど](https://ja.wikipedia.org/wiki/POWER_\(マイクロプロセッサ\) "wikilink")）が比較的多い。
  - [メインフレーム](../Page/メインフレーム.md "wikilink")市場は、CISC（[z/Architecture](https://ja.wikipedia.org/wiki/System_z "wikilink")、[ACOS](../Page/ACOS-6.md "wikilink")、[IA-64](https://ja.wikipedia.org/wiki/IA-64 "wikilink")、x86など）が大多数である。
  - [スーパーコンピュータ](../Page/スーパーコンピュータ.md "wikilink")市場は、CISC(x86)が約9割、RISC（POWERなど）が約1割であり\[3\]、ベクトルプロセッサ（[NEC SX](https://ja.wikipedia.org/wiki/NEC_SX "wikilink")、演算プロセッサはRISC風の命令セット）搭載のシステムも若干ある。
  - [組み込み市場では](../Page/組み込みシステム.md "wikilink")、RISCが優勢である。チップサイズ及びフットプリントが小型で、省電力かつ高性能なプロセッサが強く求められるため、32bit以上の比較的高性能なプロセッサではRISCに強みがある。
  - [携帯電話](../Page/携帯電話.md "wikilink")市場はRISC（主にARM）がほぼ独占しているが、[スマートフォン](https://ja.wikipedia.org/wiki/スマートフォン "wikilink")には x86 SoCを採用した製品もある。
  - [ゲーム機](../Page/ゲーム機.md "wikilink")市場は2013年にRISCの独占は破れて [PlayStation 4](https://ja.wikipedia.org/wiki/PlayStation_4 "wikilink") と [Xbox One](https://ja.wikipedia.org/wiki/Xbox_One "wikilink") がx86に切り替わった。[携帯型ゲーム](../Page/携帯型ゲーム.md "wikilink")は2014年現在も全てRISCである。

## 主なプロセッサ

### 現行

（命令セットアーキテクチャ（ISA）が同じ、ないしその派生のプロセッサが生産されているもの。初代モデルなど代表を挙げる）

  - [x86](https://ja.wikipedia.org/wiki/x86 "wikilink") ([IA-32](https://ja.wikipedia.org/wiki/IA-32 "wikilink"))
  - [System/360](https://ja.wikipedia.org/wiki/System/360 "wikilink")
      - [IBM](../Page/IBM.md "wikilink")の[z/Architectureプロセッサ](https://ja.wikipedia.org/wiki/System_z "wikilink") - [IBM z10など](https://ja.wikipedia.org/wiki/IBM_z10 "wikilink")
      - [富士通](../Page/富士通.md "wikilink")のGS21/PRIMEFORCE用プロセッサ（独自開発を継続中）
      - [日立のAPシリーズ用プロセッサ](../Page/日立製作所.md "wikilink")（IBMと共同開発し供給を受けている）
  - [680x0](../Page/MC68000.md "wikilink") ([Coldfire](https://ja.wikipedia.org/wiki/Coldfire "wikilink"))
  - [NEC Vシリーズ](https://ja.wikipedia.org/wiki/NEC_Vシリーズ "wikilink") - V800シリーズはRISC
  - [M16C](https://ja.wikipedia.org/wiki/M16C "wikilink")
  - [R8C/Tiny](https://ja.wikipedia.org/wiki/R8C/Tiny "wikilink")
  - [H8](https://ja.wikipedia.org/wiki/H8 "wikilink")

### 生産終了

  - [VAX](https://ja.wikipedia.org/wiki/VAX "wikilink")
  - [Z8000](https://ja.wikipedia.org/wiki/Z8000 "wikilink")
  - [TRONCHIP](https://ja.wikipedia.org/wiki/TRONCHIP "wikilink")

## 注釈

## 出典

## 関連項目

  - [ビットスライス](https://ja.wikipedia.org/wiki/ビットスライス "wikilink")
  - [マイクロプログラム方式](https://ja.wikipedia.org/wiki/マイクロプログラム方式 "wikilink")
  - [CPU年表](https://ja.wikipedia.org/wiki/CPU年表 "wikilink")
  - [VLIW](https://ja.wikipedia.org/wiki/VLIW "wikilink")
  - [EPICアーキテクチャ](https://ja.wikipedia.org/wiki/EPICアーキテクチャ "wikilink")
  - [CPU設計](https://ja.wikipedia.org/wiki/CPU設計 "wikilink")

## 外部リンク

  - [コンピュータアーキテクチャの話・CISCアーキテクチャとRISCアーキテクチャ - マイコミジャーナル](https://news.mynavi.jp/column/architecture/120/index.html)
  - [頭脳放談・第27回 RISCの敗因、CISCの勝因 - @IT](http://www.atmarkit.co.jp/fsys/zunouhoudan/027zunou/end_of_risc.html)

[Category:CPU](https://ja.wikipedia.org/wiki/Category:CPU "wikilink") [Category:レトロニム](https://ja.wikipedia.org/wiki/Category:レトロニム "wikilink")

1.  RISCに分類されることが多いが、可変長の命令、バンク切り替えなどCISC風の特徴を持つ。
2.  フェッチしたコードにつき、全てのワードやバイトごとにそれぞれ命令の先頭であるとみなしてデコードをすすめ、その中から有効なデコード結果の組み合わせを選択するという方式が1995年頃に確立したことから、回路規模を大きくするデメリットがあるものの可変命令長であっても1クロックサイクルで複数の命令をデコードできる。近年のプロセッサは5命令から20命令を一度にデコードできる。
3.  [スパコンTOP500 - ORNLのJaguarがRoadrunnerを破りトップに躍り出る - マイコミジャーナル](https://news.mynavi.jp/news/2009/11/16/048/index.html)
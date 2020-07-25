> この記事は[VAX](https://ja.wikipedia.org/wiki/VAX)から翻訳されています。


| DEC VAX                                             |
| --------------------------------------------------- |
| 製造者:                                                |
| [バイト幅](../Page/バイト_\(情報\).md "wikilink"):           |
| アドレスバス幅:                                            |
| ペリフェラルバス:                                           |
| [アーキテクチャ](../Page/コンピュータ・アーキテクチャ.md "wikilink"):    |
| [オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink"): |

**VAX** (バックス) は、1970年代中ごろ[ディジタル・イクイップメント・コーポレーション](../Page/ディジタル・イクイップメント・コーポレーション.md "wikilink") (DEC) が開発し販売した[32ビット](../Page/32ビット.md "wikilink")の[ミニコンピュータ](../Page/ミニコンピュータ.md "wikilink")のシリーズ、及び同シリーズの[命令セット](../Page/命令セット.md "wikilink")アーキテクチャ (ISA) を指すこともある。前述のように32ビットアーキテクチャだが、同時に16ビット時代の最も人気のあったモデルである[PDP-11](../Page/PDP-11.md "wikilink")の後継ないし代替を意識した互換命令などを持っている点では、PDP-11の拡張という面もあるアーキテチャでもある。

[直交性の高い](https://ja.wikipedia.org/wiki/直交性_\(情報科学\) "wikilink")[命令セット](../Page/命令セット.md "wikilink")（[機械語](../Page/機械語.md "wikilink")）と[ページング方式](../Page/ページング方式.md "wikilink")の[仮想記憶](../Page/仮想記憶.md "wikilink")が特徴である。VAXには、[キュー挿入](../Page/キュー_\(コンピュータ\).md "wikilink")/削除命令や[多項式](../Page/多項式.md "wikilink")計算命令などといった複雑な処理をする命令があり、豊富な[アドレッシングモード](../Page/アドレッシングモード.md "wikilink")との組み合わせ といった特徴がある。

後の64ビット化では、RISCマイクロプロセッサの[Alphaがデザインされた](https://ja.wikipedia.org/wiki/DEC_Alpha "wikilink")。OSのVMSは[OpenVMS](../Page/OpenVMS.md "wikilink")という名称となっている。

## 名称

"VAX"は本来 ***V**irtual **A**ddress e**X**tension* の[頭字語](../Page/頭字語.md "wikilink")である。その名が示すとおり、VAXは16ビットの[PDP-11](../Page/PDP-11.md "wikilink")の32ビットへの拡張であり、その巨大な[アドレス空間](../Page/アドレス空間.md "wikilink")の管理に[仮想記憶](../Page/仮想記憶.md "wikilink")を使用した初期の商用コンピュータでもあった。初期のVAXプロセッサには「[互換モード](https://ja.wikipedia.org/wiki/互換モード "wikilink")」が実装されていて、PDP-11の命令のほとんどをエミュレートできた。VAX-11 という呼称は PDP-11ファミリの継承者であることを強調したものである。後のバージョンでは互換モードが縮小され、PDP-11の命令は徐々にエミュレーションソフトウェアで実行されるようになっていった。

**VAX**という名称は、[1970年代](../Page/1970年代.md "wikilink")に Mick Atkinson が発明した[掃除機](../Page/掃除機.md "wikilink")のブランド名でもある。DECとの間で[商標](../Page/商標.md "wikilink")使用に関する法的なやりとりがあった。解決策として非競争協定が結ばれた。つまり、DECは将来に渡って家電製品に進出せず、VAXコーポレーションはコンピュータに進出しないという約束である。

英語圏のユーザーの間では、「VAXコンピュータシステム」の複数形として *VAXen* という言葉が使用された。*ox(雄牛)* の複数形 *oxen* からの類推であるが、DECは商標保護の立場から *VAXen* という表現を歓迎しなかった。

## 歴史

[thumb](https://ja.wikipedia.org/wiki/ファイル:SPEC-1_VAX_05.jpg "wikilink") 最初のVAXは VAX-11/780 であり、[1977年](../Page/1977年.md "wikilink")10月25日にDECの株主会議で公開された\[1\]。この機種のアーキテクトは[カーネギーメロン大学](https://ja.wikipedia.org/wiki/カーネギーメロン大学 "wikilink")で[ゴードン・ベル](../Page/ゴードン・ベル.md "wikilink")が指導した Bill Streckerである\[2\]。その後様々な価格および性能、容量の派生機種が開発された。VAXは[1980年代](../Page/1980年代.md "wikilink")初期には非常に一般的になった。

VAX-11/780は時に[MIPS](https://ja.wikipedia.org/wiki/MIPS "wikilink")の基準として扱われる。コンピュータの性能を示すMIPSという単位は、本来、単に実行される命令の個数を示すだけで、具体的にどのような仕事をこなせるのか、を反映しない。そこで、VAX-11/780でなんらかの[ベンチマーク](../Page/ベンチマーク.md "wikilink")プログラムを動かし、それが示す性能を1MIPSとして、性能の基準とする、ということがしばしば行われたのである。1 VAX MIPS は VAX-11/780 の性能を意味し、あるコンピュータが 27 VAX MIPS の性能という場合、VAX-11/780 の約27倍の性能であることを意味する。この目的で実際によく使われたベンチマークプログラムは当時ポピュラーだったものの一つである[ドライストーンで](../Page/Dhrystone.md "wikilink")、こんにちでも時折使われている単位*DMIPS*は、あるマシンのドライストーンの成績の値を、VAX-11/780のドライストーンの成績の値1757で割った値である。他にVAX-11/780を性能比較の基準として今も使っている例として、[BRL-CADベンチマークがある](https://ja.wikipedia.org/wiki/:en:BRL-CAD "wikilink")。これはBRL-CADというソリッドモデリングソフトウェアに含まれる性能解析スイートである。

DEC周辺では *VUP* (VAX Unit of Performance) という用語が使われた。関連用語として *cluster VUP* が VAXcluster の全体性能を示すのに使われた。

VAX-11/780には[LSI-11が内蔵されており](../Page/PDP-11.md "wikilink")、マイクロコードのロード、ブート、診断などに使われていた。その後の機種では内蔵していない。そのため780のユーザーはVMS以外にLSI-11上でRSX-11MやRT-11といったOSを動作させることもできた。

[thumb](https://ja.wikipedia.org/wiki/ファイル:DEC-VAX-8350-front-0a.jpg "wikilink") その後VAXは様々な実装がなされた。最初のVAXは[TTLで実装されており](../Page/Transistor-transistor_logic.md "wikilink")、4×5フィートの筐体が1個の[CPU](../Page/CPU.md "wikilink")の実装に使われた\[3\]。[ECL](https://ja.wikipedia.org/wiki/Emitter_coupled_logic "wikilink")[ゲートアレイ](https://ja.wikipedia.org/wiki/ゲートアレイ "wikilink")/チップを複数個使用した実装の[CPU](../Page/CPU.md "wikilink")は、VAX 8600、VAX 8800、VAX 9000シリーズで使用された。複数個の[MOSFET](../Page/MOSFET.md "wikilink")カスタムチップで実装されたCPUはVAX 8100、VAX 8200シリーズで使用された。VAX 11/730および725といったローエンド機は[ビットスライス](../Page/ビットスライス.md "wikilink")方式で実装している。

MicroVAX I はVAXファミリの転換期のマシンである。その設計時、VAXアーキテクチャ全体を1個のVLSIチップで実装することはまだ不可能だった（後に VAX 8200/8300で実施されたような数個のVLSIチップによる実装も無理だった）。その代わりに MicroVAX I ではVAXの命令セットの複雑な部分のほとんどをエミュレーションソフトウェアに移行させ、基本的な命令だけをハードウェアで実装したのである。これによって大量に必要とされた[マイクロコードを削減することが可能となった](../Page/マイクロプログラム方式.md "wikilink")。これを"MicroVAX"アーキテクチャと称した。MicroVAX I では、[ALUと](https://ja.wikipedia.org/wiki/演算論理装置 "wikilink")[レジスタが](../Page/レジスタ_\(コンピュータ\).md "wikilink")1個のゲートアレイチップで実装され、それ以外の制御部は従来の論理回路を使用した。

その後の MicroVAX II の 78032 CPU (DC333) と 78132 [FPU](../Page/FPU.md "wikilink") (DC335) がMicroVAXアーキテクチャを完全VLSI（[マイクロプロセッサ](../Page/マイクロプロセッサ.md "wikilink")）で実装したものである。78032 は[メモリ管理ユニット](../Page/メモリ管理ユニット.md "wikilink")を内蔵した初のマイクロプロセッサである\[4\]。MicroVAX II の中核部は1枚の基板で実装されており、そこにプロセッサと1MBのメモリと[DMA機構を備えた](../Page/Direct_Memory_Access.md "wikilink")[Q22-busのインタフェースが搭載されている](../Page/Q-bus.md "wikilink")。MicroVAXシリーズのその後の機種ではさらに改良やメモリの追加が行われていった。

その後、CVAX、SOC（"[System-on-a-chip](../Page/System-on-a-chip.md "wikilink")"、ワンチップ版CVAX）、Rigel、Mariah、NVAX とチップは進化していった。VAXマイクロプロセッサは当初低価格な[ワークステーション](../Page/ワークステーション.md "wikilink")向けに進化し、その後[ハイエンド](https://ja.wikipedia.org/wiki/ハイエンド "wikilink")の機種にも使用されていった。メインフレームからワークステーションまでをカバーする1つのアーキテクチャは当時の業界ではVAXだけであった。CVAXマイクロプロセッサのダイには「最良のものを盗むには十分気をつけて」という意味の言葉がいいかげんな[ロシア語](https://ja.wikipedia.org/wiki/ロシア語 "wikilink")でエッチングされていた。これは当時の[ソビエト連邦](https://ja.wikipedia.org/wiki/ソビエト連邦 "wikilink")の技術者に向けたメッセージであり、ソ連ではDECのコンピュータを[リバースエンジニアリング](../Page/リバースエンジニアリング.md "wikilink")してクローンを開発していたためである\[5\]\[6\]。

VAXアーキテクチャは[RISC](../Page/RISC.md "wikilink")技術に取って代わられた。[1989年](../Page/1989年.md "wikilink")、DECは[MIPSアーキテクチャ](../Page/MIPSアーキテクチャ.md "wikilink")のプロセッサを使用し[Ultrix](../Page/Ultrix.md "wikilink")の動作する[DECstation](../Page/DECstation.md "wikilink")をリリースした。[1992年](../Page/1992年.md "wikilink")、DECは自身のRISCプロセッサ [Alpha](https://ja.wikipedia.org/wiki/DEC_Alpha "wikilink")(当初の名称は Alpha AXP)を導入した。この高性能[64ビット](../Page/64ビット.md "wikilink")[RISC](../Page/RISC.md "wikilink")アーキテクチャ上では OpenVMS が動作した。

[2000年](../Page/2000年.md "wikilink")[8月](../Page/8月.md "wikilink")、[コンパック](../Page/コンパック.md "wikilink")は2000年末までにVAXシリーズの生産を完全に終了すると発表した\[7\]。2005年までにVAXの生産は終了したが、古いシステムは今でも世界中で使われている。

## オペレーティングシステム

VAXの本来の[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink")は、DECの[VAX/VMS](../Page/OpenVMS.md "wikilink")（後に[Alphaに移植され](https://ja.wikipedia.org/wiki/DEC_Alpha "wikilink")[POSIX](../Page/POSIX.md "wikilink")準拠となった際に OpenVMS へ改名\[8\]）である。VAXアーキテクチャとVMSオペレーティングシステムは互いを最大限に生かすため、同時並行的に開発された。これは[VAXcluster機能の最初の実装の際も同様である](https://ja.wikipedia.org/wiki/:en:VMScluster "wikilink")。他のVAX用オペレーティングシステムとしては、[BSD](../Page/BSD.md "wikilink")（4.3まで）、[Ultrix](../Page/Ultrix.md "wikilink")-32、[RTOSの](../Page/リアルタイムオペレーティングシステム.md "wikilink")[VAXELN](https://ja.wikipedia.org/wiki/:en:VAXELN "wikilink")、[Xinu](https://ja.wikipedia.org/wiki/Xinu "wikilink")などがある。最近では、[NetBSD](../Page/NetBSD.md "wikilink")と[OpenBSD](../Page/OpenBSD.md "wikilink")が様々なVAX機種をサポートし、[Linux](../Page/Linux.md "wikilink")のVAXアーキテクチャへの移植も行われている。

## プロセッサアーキテクチャ

### 命令セット

VAXの命令セットは強力で直交性が高い。当時多くのプログラムが[アセンブリ言語](../Page/アセンブリ言語.md "wikilink")で書かれていたので、プログラマが親しみやすい命令セットという観点は重要だった。その後、[高水準言語](../Page/高水準言語.md "wikilink")でプログラミングすることが多くなり、命令セットを気にするのは[コンパイラ](../Page/コンパイラ.md "wikilink")開発者ぐらいになった。

VAXの命令セットで特徴的な点として、サブプログラムの最初にレジスタマスクを置く点が挙げられる。これは、そのサブプログラムに制御が渡されたとき、どのレジスタの内容を保持するかを示すビットパターンである。レジスタマスクは実行コード内にデータを埋め込んでいる形式なので、機械語コードを逐次的に解析するのが難しくなる。例えば、機械語コードに何らかの最適化を施すのが複雑化する\[9\]。

### アドレッシングモード

VAXは、リテラル（即値）、レジスタ、ポストインクリメント、プレデクリメント、レジスタ間接、ポストインクリメント付きレジスタ間接、プレデクリメント付きレジスタ間接、ディスプレースメント (byte, word, long) 付きレジスタ間接、ディスプレースメント (byte, word, long) 付き二重間接、インデックス付きといった多数の[アドレッシングモード](../Page/アドレッシングモード.md "wikilink")を持ち、それらを組み合わせて使用できる。プログラムカウンタ (PC) はR15として汎用レジスタの1つとされているので、PCに対して各種アドレッシングモードを使用することもできる。そのためPC相対アドレッシングが可能であり、[位置独立コード](https://ja.wikipedia.org/wiki/位置独立コード "wikilink")が容易に書ける。また、VAXには実効アドレスをロードする命令群もあり、それ自体はメモリアクセスしないが、後で使用するアドレスを計算するのに使われる。

### 仮想記憶空間マップ

VAXの仮想記憶空間は4つのセクションに分割されており、それぞれ1ギガバイトのサイズである\[10\]。

| セクション | アドレス範囲                      |
| ----- | --------------------------- |
| P0    | `0x00000000` - `0x3fffffff` |
| P1    | `0x40000000` - `0x7fffffff` |
| S0    | `0x80000000` - `0xbfffffff` |
| S1    | `0xc0000000` - `0xffffffff` |

VMSでは、P0をユーザープロセスの空間、P1はプロセスのスタック、S0はOSで使用し、S1は予約されていた。

### 特権モード

VAXにはハードウェアで実装された4つの特権モードが存在する。

| 番号 | モード        | VMSでの用途                                    | 備考      |
| -- | ---------- | ------------------------------------------ | ------- |
| 0  | Kernel     | OS[カーネル](../Page/カーネル.md "wikilink")       | 最高特権レベル |
| 1  | Executive  | [ファイルシステム](../Page/ファイルシステム.md "wikilink") |         |
| 2  | Supervisor | [シェル](../Page/シェル.md "wikilink") (DCL)     |         |
| 3  | User       | 通常のプログラム群                                  | 最低特権レベル |
|    |            |                                            |         |

### プロセッサ・ステータス・ロングワード “PSL” (プロセッサステータスレジスタ)

| CM | TP | MBZ | FPD | IS | cmod | pmod | MBZ | IPL | MBZ | DV | FU | IV | T | N | Z | V | C |
| -- | -- | --- | --- | -- | ---- | ---- | --- | --- | --- | -- | -- | -- | - | - | - | - | - |
| 31 | 30 | 29  | 27  | 26 | 25   | 23   | 21  | 20  | 15  | 7  | 6  | 5  | 4 | 3 | 2 | 1 | 0 |

| ビット   | 名前                                             | 意味                                        |
| ----- | ---------------------------------------------- | ----------------------------------------- |
| 31    | CM (the Compatibility Mode bit)                | PDP-11互換モード                               |
| 30    | TP (the Trace Pending bit)                     | 個々の命令について1回だけトレースが行われることを保証する。            |
| 29:28 | MBZ (Must Be Zero)                             | 常にゼロ                                      |
| 27    | FPD (the First Part Done flag)                 | 命令の途中で割り込みやページフォールトが発生した。                 |
| 26    | IS (the Interrupt Stack flag)                  | カーネルモードで特別な割り込みスタックを使用中。                  |
| 25:24 | cmod (the current privilege mode field)        | 現在の特権モード                                  |
| 23:22 | pmod (the previous privilege mode field)       | 最近の例外で現在のモードに移行した際の前のモード                  |
| 21    | MBZ (Must Be Zero)                             | 常にゼロ                                      |
| 20:16 | IPL (the processor's Interrupt Priority Level) | 割り込み優先度。この値より優先度が高い割り込みしか割り込めない。          |
| 15:8  | MBZ (Must Be Zero)                             | 常にゼロ                                      |
| 7     | DV (the Decimal oVerflow trap enable)          | 十進演算の結果が格納先に収まらない桁数の際、トラップを発生させるか否かを指定。   |
| 6     | FU (the Floating-point Underflow trap enable)  | 浮動小数点演算の結果がアンダーフローとなった際、トラップを発生させるか否かを指定。 |
| 5     | IV (the Integer oVerflow trap enable)          | 整数演算の結果がオーバーフローとなった際、トラップを発生させるか否かを指定。    |
| 4     | T (the Trace bit)                              | セットすると、次の命令を実行した際にトレーストラップが発生。デバッグ用。      |
| 3     | N (the Negative condition code)                | セットすると、演算結果が負の場合にトラップが発生。                 |
| 2     | Z (the Zero condition code)                    | セットすると、演算結果がゼロの場合にトラップが発生。                |
| 1     | V (the oVerflow condition code)                | セットすると、演算結果がオーバーフローの場合にトラップが発生。           |
| 0     | C (the Carry condition code)                   | 演算の結果、キャリーまたはボローが発生するとセットされる。             |

プロセッサ・ステータス・ロングワードの下位16ビットがユーザ・プロセスから利用できるプロセッサ・ステータス・ワード(PSW)である。\[11\]

## VAXシステム

ほぼ時系列に列挙している。DEC内部で開発中に使用したコードネームをイタリック体で示す。VAXシステムはVLSIプロセッサを使っているか使っていないかで大まかに分けられる。MicroVAX-I はその過渡期の設計である。

### VLSI未使用のVAX

[thumb](https://ja.wikipedia.org/wiki/ファイル:VAX_11-780_intero.jpg "wikilink") [thumb](https://ja.wikipedia.org/wiki/ファイル:VAX-11-750.jpg "wikilink")

  - VAX 11 シリーズ
      - VAX 11/780 (*Star*) - [TTL](../Page/Transistor-transistor_logic.md "wikilink") CPU, 1977年10月\[12\]
      - VAX 11/750 (*Comet*) - 小型版, 性能も低い TTL ゲートアレイベースの実装, 1980年10月
      - VAX 11/751 - 堅牢なラックマウント型 11/750
      - VAX 11/730 (*Nebula*) - さらに小型化, さらに性能が低いビットスライス実装, 1982年4月
      - VAX 11/782 (*Atlas*) - 2プロセッサ版 11/780
      - VAX 11/784 (*VAXimus*) - 4プロセッサ版 11/780, 1つの MA780 メモリユニットを共有, 非常に珍しい。
      - VAX 11/785 (*Superstar*) - 高速版 11/780, 1984年4月
      - VAX 11/787 - 2プロセッサ版 11/785
      - VAX 11/788 (*VISQ*)
      - VAX 11/725 (*LCN*) - 低価格版 11/730
  - VAX 8000 シリーズ
      - VAX 8600 (*Venus*) - 開発中の別名は 11/790, [ECL](../Page/エミッタ結合論理.md "wikilink") ゲートアレイ CPU, 1984年10月
      - VAX 8650 (*Morningstar*) - 開発中の別名は 11/795, 高速版 8600, VAX 11/78xモデルで使われた[SBI](https://ja.wikipedia.org/wiki/Synchronous_Backplane_Interconnect "wikilink")[バックプレーン](../Page/バックプレーン.md "wikilink")を使用した最後の機種, PDP-11互換モードを持つ最後の機種, その後の全 8000 シリーズ機種は [VAXBI](https://ja.wikipedia.org/wiki/VAXBI "wikilink") を使用
      - VAX 8x00 (*Gemini*) - LSIベースの *Scorpio* が失敗したときの予備として並行開発; 出荷されず
      - VAX 8500 (*Flounder*) - 1プロセッサでかなり低速な 8800
      - VAX 8530 (*Skipjack*) - 1プロセッサでやや低速な 8800
      - VAX 8550 (*Skipjack*) - 1プロセッサ版 8800, 拡張不可
      - VAX 8700 (*Nautilus*) - 1プロセッサ版 Nautilus, 8800にアップグレード可能
      - VAX 8800 (*Nautilus*) - 2プロセッサ ECL マクロセルアレイ-ベースの実装, 1986年1月
      - VAX 8810/8820/8830/8840 (*Polarstar*) - *Nautilus*の派生シリーズで1～4プロセッサ, コンソールプロセッサをアップデート
      - VAX 8974/8978 - それぞれ4台か8台の VAX 8810 から構成されるクラスター, 1987年1月
  - VAX 9000 (*Aridus*) - 空冷式だが当初水冷式で設計され *Aquarius* と呼ばれていた, ECL マクロセルアレイ CPU, VAXBI, 1989年10月\[13\]
      - VAX 9000 Model 110
      - VAX 9000 Model 210
      - VAX 9000 Model 310
      - VAX 9000 Model 4x0 (x = プロセッサ数, 1～4)

### 技術転換期のVAX

  - MicroVAX/VAXstation I (*Seahorse*) - 1984年10月

### VLSI使用のVAX

[thumb](https://ja.wikipedia.org/wiki/ファイル:Microvax_3600_\(2\).jpg "wikilink")

  - MicroVAX シリーズ - エントリレベルのサーバ。1984年-
      - MicroVAX II (*Mayflower*) - 1985年5月
      - MicroVAX III - MicroVAX II のCPUを KA650 CVAX CPU で置換したもの
      - MicroVAX 2000 (*TeamMate*) - デスクトップ機, 1987年2月
      - MicroVAX 3100 シリーズ - デスクトップ機, 1987年～
          - MicroVAX 3100 Model 10 (*TeamMate II*) - KA41-A CVAX プロセッサ
          - MicroVAX 3100 Model 10e (*TeamMate II*) - KA41-D CVAX+ プロセッサ
          - MicroVAX 3100 Model 20 - Model 10 の筐体を大きくして拡張性を増したもの
          - MicroVAX 3100 Model 20e - Model 20 の拡張性をさらに高めた
          - MicroVAX 3100 Model 30 (*Waverley/S*) - KA45 SOC CPU
          - MicroVAX 3100 Model 40 - Model 30 の筐体を大きくして拡張性を増したもの
          - MicroVAX 3100 Model 80 (*Waverley/M*) - KA47 Mariah CPU
          - MicroVAX 3100 Model 85 (*Waverley/M+*) - KA55 NVAX CPU
          - MicroVAX 3100 Model 88 (*Waverley/M+*) - KA58 NVAX CPU
          - MicroVAX 3100 Model 90 (*Cheetah*) - KA50 NVAX CPU
          - MicroVAX 3100 Model 95 (*Cheetah+*) - KA51 NVAX CPU
          - MicroVAX 3100 Model 96 (*Cheetah++*) - KA56 NVAX CPU
          - MicroVAX 3100 Model 98 (*Cheetah++*) - KA59 NVAX CPU
      - MicroVAX 3300/3400 (*Mayfair*) - KA640 CPU
      - MicroVAX 3500/3600 (*Mayfair-II*) - KA650 CPU, 1987年9月
      - MicroVAX 3800/3900 (*Mayfair-III*) - KA655 CPU
  - VAXstation シリーズ - ワークステーション型。1984年-
      - VAXstation II - MicroVAX II のワークステーション版
      - VAXstation II/GPX (*Caylith*) - ハードウェア強化, 高性能カラーグラフィックス, 1985年12月
      - VAXstation 2000 - MicroVAX 2000 のワークステーション版
      - VAXstation 3100 シリーズ
          - VAXstation 3100 Model 30 (*PVAX*) - KA42-A CVAX CPU
          - VAXstation 3100 Model 38 (*PVAX rev\#7*) - KA42-B CVAX CPU
          - VAXstation 3100 Model 40 - Model 30 の筐体を大きくしたもの
          - VAXstation 3100 Model 48 - Model 38 の筐体を大きくしたもの
          - VAXstation 3100 Model 76 (*RigelMAX*) - KA43-A Rigel CPU
          - VT1300 - [X端末](../Page/X端末.md "wikilink"); VAXstation 3100 Model 30 のディスクレス版
      - VAXstation 3200/3500 (*Mayfair/GPX*) - KA650 CVAX CPU
      - VAXstation 3520/3540 (*Firefox*) - 2個か4個の KA60 CVAX プロセッサを搭載
      - VAXstation 4000 - [TURBOchannel](https://ja.wikipedia.org/wiki/TURBOchannel "wikilink")バス
          - VAXstation 4000/VLC 別名 Model 30 (*PVAX2/VLC*) - KA48 SOC ("System On Chip") CPU, 薄いピザボックス型, 標準の72ピン[SIMM](../Page/SIMM.md "wikilink")モジュールを使用可能
          - VAXstation 4000 Model 60 (*PMariah*) - KA46 Mariah CPU
          - VAXstation 4000 Model 90 (*Cougar*) - KA49-A NVAX CPU
          - VAXstation 4000 Model 90A (*Cougar+*) - KA49-A NVAX CPU
          - VAXstation 4000 Model 96 (*Cougar++*) - KA49-C NVAX CPU
      - VAXstation 8000 (*Lynx*) - VAX 8200 ベースのハイエンド3Dワークステーション
  - VAX 4000 シリーズ - VAXstationの後継。1990年-
      - VAX 4000 Model 50 (*VAXbrick*) - KA600 NVAX プロセッサ, MicroVAX 3x00 や VAX 4000-200 にCPUアップグレード可能
      - VAX 4000 Model 100/100A (*Cheetah-Q*) - KA52 NVAX プロセッサ
      - VAX 4000 Model 105A (*Cheetah-Q+*) - 高速な KA53 NVAX プロセッサ
      - VAX 4000 Model 106A/108 (*Cheetah-Q++*) - 高速な KA54/KA57 NVAX プロセッサ
      - VAX 4000 Model 200 (*Spitfire*) - KA660 SOC プロセッサ
      - VAX 4000 Model 300 (*Pele*) - KA670 Rigel 1.5 μm CMOS プロセッサチップセット\[14\], 1989年中ごろ
      - VAX 4000 Model 400 (*Omega*) - KA675 NVAX プロセッサ
      - VAX 4000 Model 500/500A (*Omega/N*) - KA680/KA681 NVAX プロセッサ
      - VAX 4000 Model 505A/600/600A (*Omega/N+*) - KA690/KA691 NVAX プロセッサ
      - VAX 4000 Model 700A (*Legacy*) - KA692 NVAX プロセッサ
      - VAX 4000 Model 705A (*Legacy+*) - KA694 NVAX プロセッサ
  - VAX 8000 シリーズ （ミッドレンジ）
      - VAX 8200, VAX 8300 (*Scorpio*) - 1-2プロセッサ, [VAXBI](https://ja.wikipedia.org/wiki/VAXBI "wikilink") バックプレーン, 1986年1月
      - VAX 8250, VAX 8350 - 8200/8300の高速版
  - VAX 6000 シリーズ - VAX 8000 シリーズの後継。以下、x = プロセッサ数, 6000シリーズでは最大6プロセッサ。1988年-
      - VAX 6000 Model 2x0 (*Calypso*) - CVAX チップセット, 1988年4月
      - VAX 6000 Model 3x0 (*Hyperion*) - CVAX+ 1.5 μm CMOS プロセッサチップセット, 1989年1月
      - VAX 6000 Model 4x0 (*Calypso/XRP*) - Rigel 1.5 μm CMOS チップセット, 1989年中ごろ
      - VAX 6000 Model 5x0 (*Calypso/XMP*) - Mariah 1.0 μm CMOS チップセット, 1990年10月
      - VAX 6000 Model 6x0 (*Neptune*) - NVAX 0.75 μm CMOS チップセット, 1991年11月
  - VAXft - [フォールトトレラントシリーズ](../Page/フォールトトレラントシステム.md "wikilink")。1990年-
      - VAXft 3000 Model 310 (*Cirrus*) - CVAX+ CPUs, 2プロセッサ, [ロックステップ](https://ja.wikipedia.org/wiki/ロックステップ "wikilink")型フォールトトレラントシステム, 1990年2月
      - VAXft Model 110 - 310(*Cirrus*)の低速/低価格版
      - VAXft Model 410/610/612 (*Cirrus II*) - SOC CPUs
      - VAXft Model 810 (*Jetstream*) - NVAX+ CPUs
  - VAX 7000 シリーズ - Alphaベースの DEC 7000 AXP シリーズとシステム設計が共通。1992年-
      - VAX 7000 Model 6x0 (*Laser/Neon*) - 最大6個の NVAX+ プロセッサ, [Alpha AXP](https://ja.wikipedia.org/wiki/DEC_Alpha "wikilink") 64ビットプロセッサにフィールドアップグレード可能, 1992年7月
      - VAX 7000 Model 7x0 (*Laser/Krypton*) - NVAX5 プロセッサ
      - VAX 7000 Model 8x0 (*Laser/Krypton+*) - 高速な NVAX5 プロセッサ
  - VAX 10000 Model 6x0 (*Blazer*) - VAX 7000 Model 6x0 とほぼ同じだが、構成が大きい。1992年7月
  - VAX XXXX (*BVAX*) - ハイエンド VAX; 出荷されなかった\[15\])

VAXserverはVAXのさまざまな機種（MicroVAX、VAX 4000、VAX 6000、VAX 9000）をネットワークサーバ専用に設定・構成したものである。

### クローン

[thumbにある](https://ja.wikipedia.org/wiki/ファイル:Robotron_K1840_2.jpg "wikilink")。\]\] 公認のものも非公認のものも含めて、様々なVAXのクローンが生産された。以下に例を挙げる。

  - [イギリス](https://ja.wikipedia.org/wiki/イギリス "wikilink")の Systime Ltd. は初期の VAX 11/750 のクローン Systime 8750 を生産した\[16\]。
  - Norden Systems は軍用に堅牢化したVAXシリーズを生産した\[17\]。
  - [ハンガリー](../Page/ハンガリー.md "wikilink")の中央物理学研究所 (KFKI) は初期のVAXのクローン TPA-11/540, 560, 580 を生産した\[18\]。
  - [チェコスロバキア](../Page/チェコスロバキア.md "wikilink")の SM 52/12\[19\] は1986年から生産された。
  - [東ドイツの](../Page/ドイツ民主共和国.md "wikilink")[ロボトロン](https://ja.wikipedia.org/wiki/ロボトロン "wikilink")は、VAX-11/780のクローン K 1840 (SM 1710) と MicroVAX II のクローン K 1820 (SM 1720) を生産した。
  - [ソビエト連邦](https://ja.wikipedia.org/wiki/ソビエト連邦 "wikilink")では、VAX-11/730のクローン *CM-1700*、MicroVAX II のクローン *CM-1702*、VAX-11/785のクローン *CM-1705* を生産した\[20\]。

## 脚注

## 外部リンク

  - [VAX & VMSものがたり](http://h50146.www5.hp.com/products/software/oe/openvms/history/vaxvms20/index.html)
  - [VAX製品のあゆみ](http://h50146.www5.hp.com/products/software/oe/openvms/history/digital/40th/vax.html)
  - [OpenVMS.org](http://www.openvms.org) [OpenVMS](../Page/OpenVMS.md "wikilink")ユーザー向けサイト; VAXについても情報あり
  - [DEC Microprocessors](http://simh.trailing-edge.com/dsarchive.html)
  - [NetBSD VAX Hardware Documentation](http://www.netbsd.org/Documentation/Hardware/Machines/DEC/vax/sections.html)
  - [VAXarchive](http://www.vaxarchive.org/)
  - [Chuck's House of VAX](http://www.mcmanis.com/chuck/computers/vaxen/)
  - [OpenBSD on VAX](http://www.openbsd.org/vax.html)

[Category:コンピュータ_(歴代)](https://ja.wikipedia.org/wiki/Category:コンピュータ_\(歴代\) "wikilink") [Category:ディジタル・イクイップメント・コーポレーション](https://ja.wikipedia.org/wiki/Category:ディジタル・イクイップメント・コーポレーション "wikilink") [Category:ミニコンピュータ](https://ja.wikipedia.org/wiki/Category:ミニコンピュータ "wikilink") [Category:ワークステーション](https://ja.wikipedia.org/wiki/Category:ワークステーション "wikilink") [Category:命令セットアーキテクチャ](https://ja.wikipedia.org/wiki/Category:命令セットアーキテクチャ "wikilink")

1.
2.
3.
4.  [The Computer History Simulation Project: MicroVAX II (1985)](http://simh.trailing-edge.com/semi/uvax.html)
5.  micro.magnet.fsu.edu, *[Steal the best](http://micro.magnet.fsu.edu/creatures/pages/russians.html)*, retrieved 30 January 2008. 実際のロシア語のメッセージは次の通り:
6.  [The Computer History Simulation Project: CVAX (1987)](http://simh.trailing-edge.com/semi/cvax.html)'', retrieved 30 January 2008
7.
8.
9.
10. アドレッシングという意味では、1GBは2<sup>30</sup>バイトと等しい。
11.
12. [VAX timeline](http://h18002.www1.hp.com/alphaserver/vax/timeline/?jumpid=reg_R1002_USEN), ヒューレット・パッカードのウェブサイト
13. [DIGITAL Computing Timeline](http://research.microsoft.com/~GBell/Digital/timeline/1989-4.htm)
14. [Trailing edge](http://simh.trailing-edge.com/semi/rigel.html), 歴史的コンピュータのシミュレーションプロジェクト
15.
16.
17.
18.
19. Dujnic, J.; Fristacky, N.; Molnar, L.; Plander, I.; Rovan, B.: *On the history of computer science, computer engineering, and computer technology development in Slovakia*. IEEE Annals of the History of Computing, vol. 21, no. 3, pp. 38-48, July-Sept. 1999
20. Laimutis Telksnys, Antanas Zilinskas: *Computers in Lithuania*. IEEE Annals of the History of Computing, vol. 21, no. 3, pp. 31-37, July-Sept. 1999
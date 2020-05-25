> この記事は[Pentium Pro](https://ja.wikipedia.org/wiki/Pentium_Pro)から翻訳されています。


**Pentium Pro**（ペンティアム プロ）は、[インテル](https://ja.wikipedia.org/wiki/インテル "wikilink")が[1995年](https://ja.wikipedia.org/wiki/1995年 "wikilink")11月に発売した[x86](https://ja.wikipedia.org/wiki/x86 "wikilink")アーキテクチャの[マイクロプロセッサ](../Page/マイクロプロセッサ.md "wikilink")([CPU](../Page/CPU.md "wikilink"))である。[P6マイクロアーキテクチャ](../Page/P6マイクロアーキテクチャ.md "wikilink")を採用した最初の製品であり、x86プロセッサとしては初めて[RISC](../Page/RISC.md "wikilink")プロセッサに迫る性能を実現した。主な用途は[ローエンド](https://ja.wikipedia.org/wiki/ローエンド "wikilink")[サーバ](../Page/サーバ.md "wikilink")、[ワークステーション](../Page/ワークステーション.md "wikilink")、[ハイエンド](https://ja.wikipedia.org/wiki/ハイエンド "wikilink")[デスクトップパソコン](../Page/デスクトップパソコン.md "wikilink")など高度な処理を必要とする環境下で利用された。

## 概要

Pentium Proは、「Pentium」という名称が付けられているが、内部構造は[P5マイクロアーキテクチャ](https://ja.wikipedia.org/wiki/P5マイクロアーキテクチャ "wikilink")の[Pentiumとは完全に異なり](../Page/Intel_Pentium_\(1993年\).md "wikilink")、[P6マイクロアーキテクチャ](../Page/P6マイクロアーキテクチャ.md "wikilink")を採用した最初のCPUである。P6マイクロアーキテクチャはRISCの設計思想を取り込み、x86命令を複数の単純化した命令に分割して実行する。また、命令発行ポートを5つ持つ[スーパースカラ](https://ja.wikipedia.org/wiki/スーパースカラ "wikilink")構造、多段[パイプラインを効率よく動作させるための](https://ja.wikipedia.org/wiki/命令パイプライン "wikilink")[分岐予測](../Page/分岐予測.md "wikilink")といった先進技術を採用し、[32ビット](../Page/32ビット.md "wikilink")[コードでは同](../Page/ソースコード.md "wikilink")[クロック](../Page/クロック.md "wikilink")のPentiumを大きく凌駕する演算処理速度を実現した。

Pentium Proは、[2次キャッシュメモリにアクセスするための内部](../Page/L2キャッシュ.md "wikilink")[バスを](../Page/バス_\(コンピュータ\).md "wikilink")、[メインメモリにアクセスするための外部バスから分離し](../Page/Random_Access_Memory.md "wikilink")、CPUコアと等速度で動作する2次キャッシュメモリをCPUコアと同一の[パッケージ上に搭載した](../Page/パッケージ_\(電子部品\).md "wikilink")。外部バスに[フロントサイドバス](../Page/フロントサイドバス.md "wikilink")（FSB）、内部バスにバックサイドバス（BSB）と個別の名称を与えてバス・アーキテクチャを解説するのは後継の[Pentium IIからで](../Page/Pentium_II.md "wikilink")、Pentium Proが発表された当時はこの二つを合わせてデュアル・インディペンデント・バス（DIB）と呼称していた。DIBの導入により、頻繁に発生する2次キャッシュへのアクセスが低速なFSBに律速されることを回避し、2次キャッシュとメインメモリへの同時アクセスも可能となり、メモリアクセスでCPUの動作が阻害されることを低減した。

新しく開発された[Socket 8に装着するCPUパッケージはCPUとは別に](https://ja.wikipedia.org/wiki/Socket_8 "wikilink")2次キャッシュメモリのチップを搭載し、巨大な[長方形](../Page/長方形.md "wikilink")の形態をとっていた。CPU自体の[トランジスタ](../Page/トランジスタ.md "wikilink")数は550万個であったが2次キャッシュはその数倍ものトランジスタ数であった。後年発売された2次キャッシュメモリ1 MB版のPentium Proは512 KBのメモリチップ2枚とCPUコア1枚の3チップ構成となっている。

Pentium（P54C Pentium）において[除算](https://ja.wikipedia.org/wiki/除算 "wikilink")において計算結果を誤ることがある致命的な[エラッタを起こし](../Page/Pentium_FDIV_バグ.md "wikilink")、その対策として全数[リコールを行った反省から](../Page/リコール_\(一般製品\).md "wikilink")、P6マイクロアーキテクチャは[マイクロコード](https://ja.wikipedia.org/wiki/マイクロコード "wikilink")の一部を[ソフトウェア](../Page/ソフトウェア.md "wikilink")で書き換えられるようになっている。Pentium Pro以降のCPUで発生したエラッタは、過去判っている範囲において、[BIOSや](https://ja.wikipedia.org/wiki/Basic_Input/Output_System "wikilink")[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink")（OS）を介して供給される、暗号化された[コード](../Page/ソースコード.md "wikilink")[ブロックをCPUに書き込むことで回避している](../Page/ブロック_\(プログラミング\).md "wikilink")。また、[整数](../Page/整数.md "wikilink")[乗算](https://ja.wikipedia.org/wiki/乗算 "wikilink")が4サイクルのパイプライン実行が可能になったほか、多くの命令でPentiumより高速化している。

## モデル

Pentium Proのモデルは、CPUコアのクロックおよび2次キャッシュメモリの容量により区別される。

  - 133 MHz版がエンジニアリング用サンプルとして提供された。外部バスのクロックは66 MHz、2次キャッシュメモリの容量は256 KB。
  - [1995年](https://ja.wikipedia.org/wiki/1995年 "wikilink")11月に150 MHz、180 MHz、200 MHz版が発売された。外部バスのクロックは、150 MHz、180 MHz版が60 MHz、200 MHz版が66 MHz。2次キャッシュメモリの容量はいずれも256 KB。
  - [1996年](../Page/1996年.md "wikilink")前半に2次キャッシュメモリの容量が512 KBの166 MHz、200 MHz版が発売された。外部バスのクロックはいずれも66 MHz。
  - [1997年](https://ja.wikipedia.org/wiki/1997年 "wikilink")8月に2次キャッシュメモリの容量が1 MBの200 MHz版が発売された\[1\]。外部バスのクロックは66 MHz。2次キャッシュメモリの容量が256 KB、512 KBのものは紫色に金色の[ヒートスプレッダ](https://ja.wikipedia.org/wiki/ヒートスプレッダ "wikilink")であるのに対し、1 MBのものは黒一色に白で「Pentium Pro」の[ロゴが印刷されている](../Page/ロゴタイプ.md "wikilink")。これは、1 MB版はCPUコアに加え512 KBのメモリチップ2枚を収めるため、[セラミック](https://ja.wikipedia.org/wiki/セラミック "wikilink")ではなく樹脂製（[FRP](../Page/繊維強化プラスチック.md "wikilink")）パッケージとなり、上面に[アルミのヒートスプレッダを貼り付けた構造となっていることによる](../Page/アルミニウム合金.md "wikilink")。また、1 MB版は[消費電力](https://ja.wikipedia.org/wiki/消費電力 "wikilink")が大きいため、CPUに電源を供給するための[VRM](https://ja.wikipedia.org/wiki/VRM "wikilink")も別のものを使用する必要がある。

## チップセット

インテルからPentium Pro用に以下の3種類のチップセットが提供された。

  - [450GX（Orion）](https://ja.wikipedia.org/wiki/インテル_チップセット#450_PCI_set_ファミリ "wikilink")
      - Pentium Proの発売と同時に提供されたサーバ向けチップセット。
      - 4 CPUまでの[SMPをサポート](../Page/対称型マルチプロセッシング.md "wikilink")。
      - [メモリコントローラ](https://ja.wikipedia.org/wiki/メモリコントローラ "wikilink")は4 GBまでのFast Page Mode (FPM) [DRAMと](../Page/Dynamic_Random_Access_Memory.md "wikilink")4 wayまでの[インターリーブをサポート](https://ja.wikipedia.org/wiki/メモリインターリーブ "wikilink")。メモリコントローラを2系統搭載することによって、8 GBまでのFPM DRAMをサポート。
      - PCIブリッジはPCI 2.0をサポート。PCIブリッジを2個搭載することによって、PCIのパフォーマンスを向上できる。
  - 450KX（Mars）
      - Pentium Proの発売と同時に提供されたワークステーション向けチップセット。機能的には450GXのサブセット。
      - 2 CPUまでのSMPをサポート。
      - メモリコントローラは1 GBまでのFPM DRAMと2 wayまでのインターリーブをサポート。
      - PCIブリッジはPCI 2.0をサポート。
      - メモリコントローラ6個、[PCIブリッジ](../Page/Peripheral_Component_Interconnect.md "wikilink")1個のチップ7個から構成され、それ以外にPCI - [ISAブリッジ用チップが必要](../Page/Industry_Standard_Architecture.md "wikilink")。同時期のPentium用チップセット430FX（Triton）が3個のチップ（PCI-ISAブリッジを除く）から構成されていたのと比べ、複雑な構成となり、Pentium Proシステムが高価な原因であった。
  - [440FX（Natoma）](https://ja.wikipedia.org/wiki/インテル_チップセット#440_AGP_/_PCI_set "wikilink")
      - 450KXの後継チップセットとして1996年5月に提供された。
      - 2 CPUまでのSMPをサポート。
      - メモリコントローラは1 GBまでのFPM DRAM、Extended Data Out（EDO）DRAM、Burst Extended Data Out（BEDO）DRAMをサポート。
      - PCIブリッジはPCI 2.1をサポート。
      - [USB](../Page/ユニバーサル・シリアル・バス.md "wikilink") 1.0をサポート。
      - 2個のチップ（PCI-ISAブリッジを除く）から構成されており、450KXより低価格にPentium Proシステムを提供できるようになった。
      - [1997年](https://ja.wikipedia.org/wiki/1997年 "wikilink")8月に440LXが提供されるまで、[Pentium IIシステムでも使用された](../Page/Pentium_II.md "wikilink")。
      - 一部の機種では[Celeron](https://ja.wikipedia.org/wiki/Celeron "wikilink")システムにも流用された。特に[PC-9800シリーズ](../Page/PC-9800シリーズ.md "wikilink")ではこの時期に本格的な開発が事実上ストップしたため、[2003年](../Page/2003年.md "wikilink")9月の受注終了までCeleron搭載機に使われつづけた。

上記以外の独自チップセットを使用して、4 CPUを超える[SMPを実現したシステムも存在した](../Page/対称型マルチプロセッシング.md "wikilink")。

## 性能

200 MHz、2次キャッシュメモリ256 KBのPentium Proを搭載したシステムは、[SPECint](../Page/Standard_Performance_Evaluation_Corporation.md "wikilink")95 8.09、SPECfp95 6.75を記録した。これはPentium Pro発売時に最速のPentiumであった、133 MHzのPentiumを搭載したシステムのおよそ2倍の性能であった。当時のRISCプロセッサとの比較では、従来はRISCプロセッサの領域と考えられていた整数演算性能を実現し、浮動小数点演算においてもRISCプロセッサの性能に近づいていた。2000年6月にはインテルで開発した[ASCI Redが](https://ja.wikipedia.org/wiki/ASCI_Red "wikilink")9,632のPentium Proを搭載し、最大理論性能で3.2 T[FLOPS](../Page/FLOPS.md "wikilink")の演算速度によりスーパーコンピュータのTOP500の第1位に輝いた。

Pentium Proは[32ビット](../Page/32ビット.md "wikilink")[コードに特化した設計のため](../Page/ソースコード.md "wikilink")、[16ビット](../Page/16ビット.md "wikilink")コードの実行速度においてはPentiumに劣り、ほとんどの場合、200 MHzのPentium Proは133 MHzのPentiumより遅かった。Pentium Proの発売当時のデスクトップパーソナルコンピュータは[Windows 3.x上の](../Page/Microsoft_Windows_3.x.md "wikilink")16ビットアプリケーションから[Windows 95上の](../Page/Microsoft_Windows_95.md "wikilink")32ビットアプリケーションへの移行期であったが、32ビットアプリケーションの実行速度においても、Pentium ProはPentiumに対して[Windows NT上ほどWindows](../Page/Microsoft_Windows_NT.md "wikilink") 95上では大きな差を示せなかった（Windows 95内の一部が16ビットコードで記述されていたためとされる）。このような問題自体は[マイクロアーキテクチャ](../Page/マイクロアーキテクチャ.md "wikilink")の切り替え時には珍しいことではなく、同じような問題は[Intel 486からPentiumへ](https://ja.wikipedia.org/wiki/Intel_486 "wikilink")、[Pentium IIIから](../Page/Pentium_III.md "wikilink")[Pentium 4への移行時にも発生したが](../Page/Pentium_4.md "wikilink")、特にPentium Proの場合は象徴的な特徴となり、実際にWindows NTモデルばかりが出荷され、当時主流だったWindows 95プレインストールモデルがまず見られないほどの明確な差別化が発生した。

## 応用製品

[サーバ](../Page/サーバ.md "wikilink")、[ワークステーション](../Page/ワークステーション.md "wikilink")向けCPUとして発売され、主に以下の用途の製品に使用された。

  - 4 CPUまでのローエンドサーバ
  - ワークステーション
  - Windows NTを[インストール](../Page/インストール.md "wikilink")したハイエンド[デスクトップパーソナルコンピュータ](../Page/デスクトップパソコン.md "wikilink")

Pentium Proは、Windows 95をインストールしたデスクトップパーソナルコンピュータ向けに使用されることはほとんどなかった。この用途では、[Pentium、Pentium MMXが使用された](../Page/Intel_Pentium_\(1993年\).md "wikilink")。

## 後継CPU

Pentium ProはCPUコアと2次キャッシュメモリを同一のパッケージ上に搭載したことが足枷となり、[歩留まり](../Page/歩留まり.md "wikilink")が悪く（コア、キャッシュ双方の不良率が同じであったとしても、単純計算で1チップ構成CPUの2倍の不良率となる）、製造コストは高止まりした。この問題を解決するため、後続製品のPentium II、[Celeron](https://ja.wikipedia.org/wiki/Celeron "wikilink")ではパッケージ形状が変更され、Socket 8の代わりに[Slot 1を使用した](../Page/Slot_1.md "wikilink")。

  - [1997年](https://ja.wikipedia.org/wiki/1997年 "wikilink")5月に発売されたPentium IIは2次キャッシュメモリをCPUコアと同一基板上に搭載した。2次キャッシュメモリの動作クロックは、CPUコアの1/2。この製品のパッケージ形状はSingle Edge Connector Cartridge（SECC）と呼ばれた。
  - [1998年](https://ja.wikipedia.org/wiki/1998年 "wikilink")4月に発売された[Celeron](https://ja.wikipedia.org/wiki/Celeron "wikilink")（Covington）は、2次キャッシュメモリを省略した。また、1998年8月に発売されたCeleron（Mendocino）は、容量を削減した2次キャッシュメモリをCPUコア内に搭載した。これらの製品のパッケージ形状はSingle Edge Processor Package（SEPP）と呼ばれた。

結局、Socket 8に対応するCPUは、Pentium Proとその[オーバードライブプロセッサ](../Page/オーバードライブプロセッサ.md "wikilink")以外には発売されなかった。

Pentium IIは、16ビットコードの処理速度をPentium Proより改善し、[MMX](../Page/MMX.md "wikilink")をサポートしていた。Pentium IIが登場すると、デスクトップパーソナルコンピュータ用のPentium ProはPentium IIによって置き換えられた。しかし、Pentium Proが4 CPUまでのSMPをサポートしていたのに対し、Pentium IIは2 CPUまでのサポートであったため、Pentium IIの登場後も、[サーバ](../Page/サーバ.md "wikilink")向けには1998年6月にPentium II [Xeon](../Page/Xeon.md "wikilink")が登場するまでPentium Proが使用された。

## アップグレード

Pentium Proシステムをアップグレードするためには以下の手段があった。

  - Pentium Proは外部バスに対するCPUコアのクロック倍率が固定されておらず、Pentium Pro用マザーボードの多くは3.5倍までの設定が可能であった。このため、200 MHzのPentium Proを233 MHzに[オーバークロック](../Page/オーバークロック.md "wikilink")する試みを容易に行えた。
  - 1998年8月にインテルからPentium II OverDrive Processorが発売された。
      - CPUコアのクロックは、外部バスの5.0倍固定（300 MHzまたは333 MHz）。
      - CPUコアと同一基板上にCPUコアのクロックと等速度の2次キャッシュメモリを512 KB搭載。
      - MMXをサポート。
      - 2 CPUまでのSMPをサポート。(公式には動作しないとされているが、4 CPUでも動作する。)
      - インテルは日本向け製品を提供しなかったので、日本では並行輸入品のみが販売された。
      - オーバードライブプロセッサ (ODP) の提供はPentium Proの発表時から予告されていた。
  - 440FXチップセットであればSocket 8とSlot 1（[Socket 370に変換可能](https://ja.wikipedia.org/wiki/Socket_370 "wikilink")）の両方に対応しているため、Socket 370用のMendocinoコアのCeleronをSocket 8で使用するためのアダプタ（[ゲタ](../Page/ゲタ_\(CPU\).md "wikilink")）が発売された。またPentium ProをSlot 1（Socket 370では不可）で使用するアダプタも発売された。これらはODPとは異なり基本的に440FX向けの作りであるため、450GX/KXや、440LX以降のチップセットを使用したシステムでの動作は期待できない。
      - さらには、Socket 8をSocket 370(PPGA)に変換するアダプタに、PPGAやFC-PGAをFC-PGA2（後期のSocket 370の電気規格）に変換させるアダプタの二段挿しにより、[Celeron Tualatin](https://ja.wikipedia.org/wiki/Celeron "wikilink")1.4GHz（実際のクロックは66.6x14倍の933MHz動作）や、[Pentium III-S](../Page/Pentium_III.md "wikilink")1.4GHz（実際のクロックは66.6x10.5倍の700MHz動作）、場合によっては[VIA C3](../Page/VIA_C3.md "wikilink")（逓倍率が変更可能だがパフォーマンスは劣る）を動作させることのできる[マザーボード](../Page/マザーボード.md "wikilink")もあった。
      - いずれにせよPentium Proしか想定していないBIOSでは異なるCPUが動作しない場合も少なくないため、基本的にはBIOSが対応している必要があった。

## 脚注

## 関連項目

  - [P6マイクロアーキテクチャ](../Page/P6マイクロアーキテクチャ.md "wikilink")
  - [物理アドレス拡張](../Page/物理アドレス拡張.md "wikilink")

## 外部リンク

  - [Pentium、Pentium Proの性能比較](http://www.byte.com/art/9509/sec4/art1.htm)
  - [Pentium Pro、Pentium MMX、Pentium IIの性能比較](http://www.tomshardware.com/1997/04/30/the_empire_strikes_back/)

[Category:インテルのマイクロプロセッサ](https://ja.wikipedia.org/wiki/Category:インテルのマイクロプロセッサ "wikilink")

1.
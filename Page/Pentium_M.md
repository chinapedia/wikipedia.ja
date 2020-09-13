> この記事は[Pentium M](https://ja.wikipedia.org/wiki/Pentium_M)から翻訳されています。


**Pentium M**（ペンティアム・エム）は、[インテル](https://ja.wikipedia.org/wiki/インテル "wikilink")が[2003年](../Page/2003年.md "wikilink")3月に発売した、主に[ノートパソコン](../Page/ノートパソコン.md "wikilink")向けの[x86](https://ja.wikipedia.org/wiki/x86 "wikilink")[アーキテクチャの](../Page/コンピュータ・アーキテクチャ.md "wikilink")[マイクロプロセッサ](../Page/マイクロプロセッサ.md "wikilink")([CPU](../Page/CPU.md "wikilink"))。

## 概要

ノートPCに搭載することを前提とし、バッテリー持続時間（＝省電力）と高速性能（＝処理能力）の両立を目的として設計された。今までの[モバイル向けCPUとは異なり](https://ja.wikipedia.org/wiki/モービル "wikilink")、[デスクトップパソコン](../Page/デスクトップパソコン.md "wikilink")向けの設計を流用するのではなく、モバイル専用に設計されたものであり、これはインテルにとって初の試みである。

またPentium M、対応[チップセット](../Page/チップセット.md "wikilink")のi855/i915シリーズ、[IEEE 802.11a](https://ja.wikipedia.org/wiki/IEEE_802.11a "wikilink")/[b](https://ja.wikipedia.org/wiki/IEEE_802.11b "wikilink")/[g](https://ja.wikipedia.org/wiki/IEEE_802.11g "wikilink")[無線LAN](../Page/無線LAN.md "wikilink")チップのIntel PRO/Wireless、および[Microsoft Windows XPまたは](../Page/Microsoft_Windows_XP.md "wikilink")[Linux](../Page/Linux.md "wikilink") Kernel 2.4x 以降のソフトウェアとの組み合わせで**インテル [Centrino](../Page/Centrino.md "wikilink")**（セントリーノ）**モバイルテクノロジ**と称する。ただし、3種ともに上記などインテル製品での組み合わせでなければCentrinoの呼称を名乗ることができない。

一部のデスクトップパソコンにも搭載され、Pentium M対応の[マザーボード](../Page/マザーボード.md "wikilink")も売り出されていた。小型で静粛性の高いデスクトップパソコンを組み立てることができた。

Pentium Mは、IA-32の[64ビット](../Page/64ビット.md "wikilink")拡張命令である[Intel 64には対応していない](https://ja.wikipedia.org/wiki/x64 "wikilink")。

## 設計

インテルにより公開されている資料\[1\]によれば、Pentium Mのマイクロアーキテクチャは[Pentium 4などに採用された](../Page/Pentium_4.md "wikilink")[NetBurstマイクロアーキテクチャ](../Page/NetBurstマイクロアーキテクチャ.md "wikilink")より一つ前の[P6マイクロアーキテクチャ](../Page/P6マイクロアーキテクチャ.md "wikilink")をベースに抜本的な改良を加えたものである。コンプレックスデコーダ1つ＋シンプルデコーダ2つというデコーダの構成や、5つの命令発行ポートを備え3μOPs/clkでリタイア可能という[アウト・オブ・オーダー実行](../Page/アウト・オブ・オーダー実行.md "wikilink")部の大まかな特徴はP6マイクロアーキテクチャと似ているが、主に以下のような改良が加えられている。

  - Micro-OPs Fusionのサポート
    Pentium Mのマイクロアーキテクチャにおける最大の改良点はMicro-OPs Fusionのサポートである。これは例えばメモリアクセスと演算を同時に行う命令等において、従来はデコーダで2つのμOP (この場合はメモリアクセスμOPと演算μOP) を生成していたものを、デコードの時点では1つのμOPとして処理する技術である。これによって、従来はコンプレックスデコーダのみで処理できた命令がシンプルデコーダでも処理できるようになり命令デコードの帯域が向上する、リネーミングやリタイアの3μOPs/clkの帯域が節約できる、またリオーダバッファのエントリの消費が抑えられるといった様々な利点がある。
    これは、[AMD](https://ja.wikipedia.org/wiki/AMD "wikilink")が[K7マイクロアーキテクチャで実装したMacro](../Page/Athlon.md "wikilink")-Opの概念と基本的には同等のものである。ただし、Pentium Mのマイクロアーキテクチャにおいては、メモリアクセスと演算を同時に行うx86命令以外でもMicro-OPs Fusionが機能する機会が存在する。例えば、ストア命令はアドレスを計算するμOPとストアデータをレジスタから読み出すμOPに分けて実行ユニットに送られる実装になっているため、Micro-OPs Fusionが有効である。
  - [分岐予測](../Page/分岐予測.md "wikilink")機構の改良
    [Pentium 4に搭載された分岐予測器をベースに](../Page/Pentium_4.md "wikilink")、ループ検出器の実装とレジスタ間接分岐予測のサポートを行なっている。ループ検出器は内部に64バイトのバッファを備え、64バイト以内の命令列でループとなっている分岐を検出し、命令フェッチを停止してバッファから命令を供給することができる。
  - [スタックポインタ](https://ja.wikipedia.org/wiki/スタックポインタ "wikilink")操作専用ハードウェアの追加
    x86命令セットにはPUSH、POP、CALL、RETといったスタックポインタを操作する命令があるが、これらをフロントエンドで処理するためのハードウェア (スタックエンジン) が追加されている。これらの命令については、Pentium Mではスタックポインタを加減するμOPは生成されず、デコード段の直後に設置されたスタックエンジンに含まれる専用の加算器で処理される。そのため、例えばPUSHやPOP命令については、デコーダで生成されるμOPはメモリアクセス (PUSH-ストア、POP-ロード) のμOPのみであり、バックエンドの実行ユニット資源の節約に貢献している。スタックエンジンはスタックポインタに対する操作の累積の差分を記憶しており、レジスタ (リオーダ・バッファ) 内の実際のスタックポインタの値は更新しないため、スタックポインタにアクセスするμOPに差分情報を追加し、正しい実効アドレスが得られるようにしている。この差分情報が追加できないμOPに遭遇した場合は、レジスタ内のスタックポインタを更新する内部命令が自動的に挿入される。

その他、OOOバッファの増加、L1命令キャッシュの倍増(16KB→32KB)、L1データキャッシュの倍増(16KB→32KB)、L2キャッシュの倍増(512KB→1MB)、TLBの増量なども行われているが、これら多くの改良により、旧世代のP6マイクロアーキテクチャと比較してIPCが向上している。命令セットの面ではPentium 4と共に登場した[SSE2](https://ja.wikipedia.org/wiki/SSE2 "wikilink")命令を新たにサポートしており、当時のデスクトップ向けプロセッサに準じた仕様になっている。

モバイルに向かない[NetBurstマイクロアーキテクチャ](../Page/NetBurstマイクロアーキテクチャ.md "wikilink")の代替として開発され、絶対的な性能よりもクロックあたりの処理性能を重視している。[NetBurstマイクロアーキテクチャ](../Page/NetBurstマイクロアーキテクチャ.md "wikilink")のパイプラインを深くし、高クロック化で性能を稼ぐという方向性は抑えられている。その一方でCPUバス周りはNetBurst系の高速なバスを組み合わせており、バス周りがボトルネックとなることを抑えている。

クロックあたりの性能が高く、約1.5倍のクロックの Pentium 4 に匹敵する性能を発揮し、Pentium M の2GHz、Pentium 4 の2.8 GHz 、[Athlon 64](../Page/Athlon_64.md "wikilink") 2800+（1.8 GHz）がおおよそ同じくらいの性能だと言われている。また、低消費電力であるため、発熱が減少し、大型化・高コスト化する一方であった[CPUの冷却装置](../Page/CPUの冷却装置.md "wikilink")の小型化に貢献した。

低消費電力と高いパフォーマンスが評価され、モバイルのみならず、モバイル・オン・デスクトップ（MoDT）としての用途に注目が集まった。 デスクトップで Pentium M を使うために、Pentium M 用の[Socket 479](https://ja.wikipedia.org/wiki/Socket_479 "wikilink")（Socket 479M）を使用したデスクトップパソコン向けの[マザーボード](../Page/マザーボード.md "wikilink")も数社から発売された。さらには[台湾](https://ja.wikipedia.org/wiki/台湾 "wikilink")のマザーボードメーカーの[ASUS](../Page/ASUS.md "wikilink")より、Pentium M(および[Celeron M](https://ja.wikipedia.org/wiki/Celeron_M "wikilink")) を Pentium 4 などに使用されるデスクトップ用の[Socket 478を備えるマザーボードで使用できる](https://ja.wikipedia.org/wiki/Socket_478 "wikilink")[CPU変換アダプタ](../Page/ゲタ_\(CPU\).md "wikilink")（CT-479）も発売された。この製品は、正式には同社製の限られたマザーボードのみで使用できるとされる\[2\]。[Intel SpeedStep テクノロジは公式には機能しないとされる](../Page/Intel_SpeedStep_テクノロジ.md "wikilink")\[3\]。動作にはマザーボードの [BIOS](https://ja.wikipedia.org/wiki/Basic_Input/Output_System "wikilink") の[アップデート](https://ja.wikipedia.org/wiki/アップデート "wikilink")が必要。

### 第一世代“バニアス” (Banias)

130 nm プロセスで製造された。[Pentium 4](../Page/Pentium_4.md "wikilink") 同様、[SSE2](https://ja.wikipedia.org/wiki/ストリーミングSIMD拡張命令#SSE2 "wikilink") に対応している。途中から[プロセッサー・ナンバー](../Page/プロセッサー・ナンバー.md "wikilink")が採用され、700番台が与えられている。 省電力技術として[拡張版 Intel SpeedStep テクノロジ（EIST）をサポートする](https://ja.wikipedia.org/wiki/Intel_SpeedStep_テクノロジ#拡張版_Intel_SpeedStep_テクノロジ_\(EIST\) "wikilink")。これはかつてモバイル [Pentium III](../Page/Pentium_III.md "wikilink")-M に搭載されていたものをさらに拡張させたもので、多段階の動作電圧や周波数で動作することを可能としている。

  - Banias 標準電圧版
    {| border="1" cellpadding="5" class="wikitable"

|- align="center" \! プロセッサ・ナンバ \!\! 動作周波数 \!\! FSB \!\!2次キャッシュ \!\! EIST \!\! NX Bit \!\! ソケット \!\! TDP(最低周波数) |- | - || 1.30 GHz || 400MHz || 1MB || ○ || × || Socket479 || 22W (-) |- | - || 1.40 GHz || 400MHz || 1MB || ○ || × || Socket479 || 22W (-) |- | 705 || 1.50 GHz || 400MHz || 1MB || ○ || × || Socket479 || 24.5W (-) |- | - || 1.60 GHz || 400MHz || 1MB || ○ || × || Socket479 || 24.5W (-) |- | - || 1.70 GHz || 400MHz || 1MB || ○ || × || Socket479 || 24.5W (-) |}

  - Banias 低電圧版
    {| border="1" cellpadding="5" class="wikitable"

|- align="center" \! プロセッサ・ナンバ \!\! 動作周波数 \!\! FSB \!\!2次キャッシュ \!\! EIST \!\! NX Bit \!\! ソケット \!\! TDP(最低周波数) |- | - || 1.10 GHz || 400MHz || 1MB || ○ || × || Socket479 || - |- | - || 1.20 GHz || 400MHz || 1MB || ○ || × || Socket479 || - |- | 718 || 1.30 GHz || 400MHz || 1MB || ○ || × || Socket479 || 12W (-) |}

  - Banias 超低電圧版
    {| border="1" cellpadding="5" class="wikitable"

|- align="center" \! プロセッサ・ナンバ \!\! 動作周波数 \!\! FSB \!\!2次キャッシュ \!\! EIST \!\! NX Bit \!\! ソケット \!\! TDP(最低周波数) |- | - || 0.90 GHz || 400MHz || 1MB || ○ || × || Socket479 || - |- | - || 1.00 GHz || 400MHz || 1MB || ○ || × || Socket479 || - |- | 713 || 1.10 GHz || 400MHz || 1MB || ○ || × || Socket479 || 7W (-) |}

### 第二世代“ドーサン” (Dothan)

[thumb](https://ja.wikipedia.org/wiki/ファイル:Pentium_M_Dothan.jpg "wikilink") 90nmプロセスで製造された。[プロセッサー・ナンバー](../Page/プロセッサー・ナンバー.md "wikilink")はBanias同様700番台。

改良版（Dothan-533）が新チップセット Intel 915 シリーズとともに[2005年](../Page/2005年.md "wikilink")[1月19日](../Page/1月19日.md "wikilink")に発表される。FSBが400MHzから533MHzに向上した以外はDothanと同一。「ソノマ（Sonoma）」というコードネームで呼ばれた第2世代セントリーノ・プラットフォームとともに用いられる。

同時発表されたチップセットIntel 915シリーズ（正式には「モバイルIntel 915 Expressチップセットファミリ」)は、FSB533/400MHzに対応し、[PCI Expressが使用可能](../Page/PCI_Express.md "wikilink")。[DDR2 SDRAMも利用可能になり](../Page/DDR2_SDRAM.md "wikilink")、消費電力を削減できる。 グラフィックス・メディア・アクセラレータ 900（[GMA](https://ja.wikipedia.org/wiki/Intel_GMA "wikilink") 900）が統合された 915G チップセット・ファミリはグラフィックス性能を従来製品よりも大幅に向上し、T\&L にハードウェアレベルで対応していないことなどを除けば、低価格向けの[GPUと同程度の性能を有する](../Page/Graphics_Processing_Unit.md "wikilink")。なお、GMA900 では [Windows Vista](https://ja.wikipedia.org/wiki/Microsoft_Windows_Vista "wikilink") の [Windows Aero](../Page/Windows_Aero.md "wikilink") ([DWM](https://ja.wikipedia.org/wiki/Desktop_Window_Manager "wikilink"))は使用できない。GMA900 の後継グラフィックである GMA950 では Windows Aero に対応している。 組み合わされる [ICH](https://ja.wikipedia.org/wiki/I/O_コントローラー・ハブ "wikilink") は ICH6M で、最大32[ビット](../Page/ビット.md "wikilink")/192 [kHz](https://ja.wikipedia.org/wiki/キロヘルツ "wikilink") 対応の [HD Audio](../Page/High_Definition_Audio.md "wikilink") や[シリアルATA](https://ja.wikipedia.org/wiki/シリアルATA "wikilink")が使用できる。

  - Dothan 標準電圧版、FSBはいずれも400MHz
    {| border="1" cellpadding="5" class="wikitable"

|- align="center" \! プロセッサ・ナンバ \!\! 動作周波数 \!\! 2次キャッシュ \!\! EIST \!\! NX Bit \!\! ソケット \!\! TDP(最低周波数) |- | 715 || 1.50 GHz || 2MB || ○(～600MHz) || × || Socket479 || 21W (7.5W) |- | 725 || 1.60 GHz || 2MB || ○(～600MHz) || × || Socket479 || 21W (7.5W) |- | 725A || 1.60 GHz || 2MB || ○(～600MHz) || ○ || Socket479 || 21W (7.5W) |- | 735 || 1.70 GHz || 2MB || ○(～600MHz) || × || Socket479 || 21W (7.5W) |- | 735A || 1.70 GHz || 2MB || ○(～600MHz) || ○ || Socket479 || 21W (7.5W) |- | 745 || 1.80 GHz || 2MB || ○(～600MHz) || × || Socket479 || 21W (7.5W) |- | 745A || 1.80 GHz || 2MB || ○(～600MHz) || ○ || Socket479 || 21W (7.5W) |- | 755 || 2.00 GHz || 2MB || ○(～600MHz) || × || Socket479 || 21W (7.5W) |- | 765 || 2.10 GHz || 2MB || ○(～600MHz) || × || Socket479 || 21W (7.5W) |} ＊765は、Intel公式サイトではNX(XD)bitが「はい」となっているが、実際には実装されていない。

  - Dothan-533 標準電圧版、FSBはいずれも533MHz
    {| border="1" cellpadding="5" class="wikitable"

|- align="center" \! プロセッサ・ナンバ \!\! 動作周波数 \!\! 2次キャッシュ \!\! EIST \!\! NX Bit \!\! ソケット \!\! TDP(最低周波数) |- | 730 || 1.60 GHz || 2MB || ○(～800MHz) || ○ || Socket479 || 27W (10.8W) |- | 740 || 1.73 GHz || 2MB || ○(～800MHz) || ○ || Socket479 || 27W (10.8W) |- | 750 || 1.86 GHz || 2MB || ○(～800MHz) || ○ || Socket479 || 27W (10.8W) |- | 760 || 2.00 GHz || 2MB || ○(～800MHz) || ○ || Socket479 || 27W (10.8W) |- | 770 || 2.13 GHz || 2MB || ○(～800MHz) || ○ || Socket479 || 27W (10.8W) |- | 780 || 2.26 GHz || 2MB || ○(～800MHz) || ○ || Socket479 || 27W (10.8W) |}

  - Dothan 低電圧版、FSBはいずれも400MHz
    {| border="1" cellpadding="5" class="wikitable"

|- align="center" \! プロセッサ・ナンバ \!\! 動作周波数 \!\! 2次キャッシュ \!\! EIST \!\! NX Bit \!\! ソケット \!\! TDP(最低周波数) |- | 738 || 1.40 GHz || 2MB || ○(～600MHz) || × || - || 10W (7.5W) |- | 758 || 1.50 GHz || 2MB || ○(～600MHz) || × || - || 10W (7.5W) |- | 778 || 1.60 GHz || 2MB || ○(～600MHz) || × || - || 10W (7.5W) |}

  - Dothan 超低電圧版、FSBはいずれも400MHz
    {| border="1" cellpadding="5" class="wikitable"

|- align="center" \! プロセッサ・ナンバ \!\! 動作周波数 \!\! 2次キャッシュ \!\! EIST対応 \!\! NX Bit \!\! ソケット \!\! TDP(最低周波数) |- | 723 || 1.00 GHz || 2MB || ○(～600MHz) || × || - || 5W (3.0W) |- | 733 || 1.10 GHz || 2MB || ○(～600MHz) || × || - || 5W (3.0W) |- | 733J || 1.10 GHz || 2MB || ○(～600MHz) || ○ || - || 5W (3.0W) |- | 753 || 1.20 GHz || 2MB || ○(～600MHz) || ○ || - || 5W (3.0W) |- | 773 || 1.30 GHz || 2MB || ○(～600MHz) || ○ || - || 5W (3.0W) |}

一連のシリーズで、機能的な相違度はBanias \< Dothan \<\< Yonah \<\<\< Meromとなるが、公表されている機能分を差し引いたトランジスタ数の差としてはBanias \<\< Dothan \< Yonah \<\<\<Meromとなる。このことからDothanは未公開の実験的要素が多数組み込まれている可能性がある、ただしトランジスタ数の考察に関しては、プロセス毎にキャッシュのセルを構成するトランジスタ個数、(6セルや8セルなどと呼ばれ、一般的に微細化が進むほど増える)が代わる為、トランジスタ数の増加は、必ずしも新たなロジック回路の追加とは言えない可能性もある。

## 後継マイクロアーキテクチャ“ヨナ”(Yonah)

[2006年](../Page/2006年.md "wikilink")[1月5日](../Page/1月5日.md "wikilink")に発表された65nmプロセスのCPUで、モバイル向けとして初めてデュアルコアが採用された。ブランド名がこの製品から[Intel Coreに変更された](../Page/Intel_Core.md "wikilink")。詳細は[Intel Coreを参照のこと](../Page/Intel_Core.md "wikilink")。

## 脚注

## 関連項目

  - [Crusoe](../Page/Crusoe.md "wikilink") - Pentium MはCrusoeキラーとして開発された経緯がある。
  - [Celeron M](https://ja.wikipedia.org/wiki/Celeron_M "wikilink") - Pentium MやCoreの廉価版。2ndキャッシュ半減やIntel SpeedStep テクノロジが省略されている。
  - [Pentium 4-M](../Page/Pentium_4-M.md "wikilink") - Pentium 4をベースにしたモバイル向けCPU。
  - [Intel Core](../Page/Intel_Core.md "wikilink") - Yonah以降このブランド名に移行した。
  - [Intel A100](../Page/Intel_A100.md "wikilink") - Dothanを流用した[LPIA製品](https://ja.wikipedia.org/wiki/インテル#LPIA "wikilink")。
  - [Turion 64](../Page/Turion_64.md "wikilink") - 競合他社製品。

## 外部リンク

  - [インテル Pentium M プロセッサー](http://www.intel.co.jp/jp/products/processor/pentiumm/)

[Category:インテルのマイクロプロセッサ](https://ja.wikipedia.org/wiki/Category:インテルのマイクロプロセッサ "wikilink")

1.  S. Gochman, et al.: [The Intel Pentium M Processor: Microarchitecture and Performance](http://noggin.intel.com/content/the-intel%C2%AE-pentium%C2%AE-m-processor-microarchitecture-and-performance). Intel Technology Journal, vol. 7, no. 2, 2003
2.  実際に動作するマザーボードはいくつか知られていて、その中には他社製のものもある。http://www.geocities.jp/ct_479/
3.  実際には動作する場合もある。http://www.geocities.jp/ct_479/
> この記事は[Sun-2](https://ja.wikipedia.org/wiki/Sun-2)から翻訳されています。


[thumb](https://ja.wikipedia.org/wiki/ファイル:Sun_2-120_Server.jpg "wikilink") [thumb](https://ja.wikipedia.org/wiki/ファイル:Sun_2-50_Front.jpg "wikilink") **Sun-2** シリーズの[UNIX](../Page/UNIX.md "wikilink") [ワークステーション](../Page/ワークステーション.md "wikilink")と[サーバ](../Page/サーバ.md "wikilink")は、1983年に[サン・マイクロシステムズ](../Page/サン・マイクロシステムズ.md "wikilink")によって発売された。名前が示すとおり、 Sun-2 は [Sun-1](../Page/Sun-1.md "wikilink") シリーズを置き換える、サンマイクロシステムズの第 2 世代のシステムである。Sun-2 シリーズは 10 MHz のモトローラ [MC68010](../Page/MC68010.md "wikilink") [マイクロプロセッサ](../Page/マイクロプロセッサ.md "wikilink")を搭載し、[4.1BSDに基づいて完全な](../Page/BSD.md "wikilink")[仮想記憶](../Page/仮想記憶.md "wikilink")を実装した [SunOS](../Page/SunOS.md "wikilink") 1.0 が動作する最初のサンのアーキテクチャであった。初期の Sun-2 は [インテル](https://ja.wikipedia.org/wiki/インテル "wikilink")の[マルチバス](https://ja.wikipedia.org/wiki/マルチバス "wikilink")アーキテクチャに基づいていたが、後期には、将来の [Sun-3](../Page/Sun-3.md "wikilink") と [Sun-4](../Page/Sun-4.md "wikilink") ファミリでも使用される [VMEバス](../Page/VMEバス.md "wikilink")に置き換えられた。

Sun-2 システムは SunOS のバージョン 4.0.3 までサポートされた。[NetBSD](../Page/NetBSD.md "wikilink") では、2002年の[NetBSD](../Page/NetBSD.md "wikilink") 1.6 のリリースで、マルチバス Sun-2 のサポートが追加された。

## Sun-2 の形式

形式は、およそ年代順に並べている。

| 形式        | CPU ボード                        | 最大 RAM 容量 | 筐体                      |
| --------- | ------------------------------ | --------- | ----------------------- |
| **2/120** | Sun-2 マルチバス 又は Sun-2 マルチバスプライム | 7 or 8 MB | 9 スロット マルチバス (デスクサイド)   |
| **2/170** | Sun-2 マルチバス 又は Sun-2 マルチバスプライム | 7 or 8 MB | 15 スロット マルチバス (ラックマウント) |
| **2/50**  | Sun 2050                       | 7 MB      | 2 スロット VME (デスクトップ)     |
| **2/130** | Sun 2050                       | 7 MB      | 12 スロット VME (デスクサイド)    |
| **2/160** | Sun 2050                       | 7 MB      | 12 スロット VME (デスクサイド)    |

Sun-2 マルチバス CPU ボードにアップグレードした Sun-1 のシステムは、**2/100U** (アップグレードした Sun-100) や **2/150U** (アップグレードした Sun-150) と記されることがある。

典型的な 2/120 の構成で、システムの価格は 5万ドル以上であった。

## Sun-2 のハードウェア

Sun 2/120 (9 スロット デスクサイド) と Sun 2/170 (15 スロット ラックマウント) のシステムは、[マルチバス](https://ja.wikipedia.org/wiki/マルチバス "wikilink")アーキテクチャに基づいている。 CPU ボードは 10MHz の 68010 プロセッサを使用し、8MB の物理アドレスと 16MB の仮想アドレスを扱うことができた。物理アドレス最上位の 1MB の空間は、モノクロフレームバッファ用として予約されていた。 CPU は 2 つのシリアルポートに加えて、Sun-1 の パラレルキーボードとマウスをサポートしていた。

サン・マイクロシステムズは 1MB と 4MB のメモリボードを提供したが、最大 4MB RAM の構成までしかサポートを行わなかった。Helios Systems のような会社も、サンのシステムで動作する 4MB メモリボードを作った。

標準的なフレームバッファは Sun-2 プライム モノクロ ビデオ であった。このボードは [TTL](../Page/Transistor-transistor_logic.md "wikilink") 又は [ECL](../Page/エミッタ結合論理.md "wikilink") ビデオ信号による 1152x900 モノクロディスプレイと、キーボードとマウスのポートを提供した。これは、通常物理メモリアドレス空間の最上位 1MB を占有した。1152x900 8-bit カラーディスプレイを提供する Sun-2 カラービデオボードも利用可能であった。このボードはアドレス空間の最上位 4MB を占有した。

42MB の [MFM](https://ja.wikipedia.org/wiki/Modified_Frequency_Modulation "wikilink") ディスクが、標準的な記憶装置として使用された。2つのディスクを、[アダプテック](../Page/アダプテック.md "wikilink") の MFM/[SCSI](../Page/Small_Computer_System_Interface.md "wikilink") カード ACB-4000 を介して Sun-2 マルチバス シリアル/SCSI [ホストアダプタ](https://ja.wikipedia.org/wiki/ホストアダプタ "wikilink")に接続できた。SCSIボードは 2つのシリアルポートも合わせて提供した。より大きな記憶容量の要求に応じるため、65 MB, 130 MB, 380 MB の [SMD](https://ja.wikipedia.org/wiki/Storage_Module_Device "wikilink") が [Xylogics](https://ja.wikipedia.org/wiki/Xylogics "wikilink") 450 SMD コントローラに接続された。サンのコントローラは 2台のディスクのサポートであったが、SMD コントローラは 4台のディスクをサポートした。[Archive](https://ja.wikipedia.org/wiki/Archive_Corp. "wikilink") の QIC/SCSI コンバータを使用することで、20 MB の [QIC](../Page/Quarter_Inch_Cartridge.md "wikilink") テープドライブを接続することができた。Sun-2 のシステムは Computer Products Corporation の TAPEMASTER や Xylogics の 472 ボードによって 1/2 インチのテープドライブもサポートした。

インテル 82586 チップを使用したサンのボード 又は [スリーコム (3Com)](https://ja.wikipedia.org/wiki/スリーコム "wikilink") 3c400 ボード によって、イーサネットポートが提供された。サーバは、イーサネットボードを使用することで、ディスクレスの Sun-2/50 クライアントをサポートすることができた。

他にサポートされたマルチバスボードには Sky Computer の浮動小数点プロセッサ、8つシリアルポートをサポートするサンの ALM (Asynchronous Line Multiplexer)、[SNA](../Page/Systems_Network_Architecture.md "wikilink") と [X.25](https://ja.wikipedia.org/wiki/X.25 "wikilink") の接続をサポートするサンの SunLink Communications Processor (SCP) がある。

## 関連項目

  - [Sun-3](../Page/Sun-3.md "wikilink")
  - [Sun386i](https://ja.wikipedia.org/wiki/Sun386i "wikilink")
  - [Sun-4](../Page/Sun-4.md "wikilink")
  - [SPARCstation](https://ja.wikipedia.org/wiki/SPARCstation "wikilink")

## 外部リンク

  - [Sun Microsystems](http://www.sun.com/)
  - [The Sun Hardware Reference, Part 1](http://www.sunhelp.org/faq/sunref1.html)
  - The Sun-2 Hardware Reference: [Part 1](http://sunstuff.org/Sun-Hardware-Ref/s2hr/part1) and [Part 2](http://sunstuff.org/Sun-Hardware-Ref/s2hr/part2)
  - [Sun Field Engineer Handbook, 20th edition](http://www.sunshack.org/data/feh/1.5/wcd00094/wcd09466.htm)
  - [soupwizard.com Sun-2 Archive](http://www.soupwizard.com/sun2/index.htm)

[Category:ワークステーション](https://ja.wikipedia.org/wiki/Category:ワークステーション "wikilink") [Category:サン・マイクロシステムズ](https://ja.wikipedia.org/wiki/Category:サン・マイクロシステムズ "wikilink")
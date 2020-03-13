> この記事は[Open Firmware](https://ja.wikipedia.org/wiki/Open_Firmware)から翻訳されています。


**Open Firmware**（または**OpenBoot**）は[ハードウェア](../Page/ハードウェア.md "wikilink")に依存しない[ファームウェア](../Page/ファームウェア.md "wikilink")（[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink")をロードする[ソフトウェア](../Page/ソフトウェア.md "wikilink")）であり、[サン・マイクロシステムズ](../Page/サン・マイクロシステムズ.md "wikilink")のミッチ・ブラッドリーによって開発され、[IEEE](../Page/IEEE.md "wikilink")により標準化され、[サン・マイクロシステムズ](../Page/サン・マイクロシステムズ.md "wikilink")、[アップル](../Page/アップル_\(企業\).md "wikilink")、[IBM](../Page/IBM.md "wikilink")などによって使われている。

## 概要

Open Firmwareは、[アップルの](../Page/アップル_\(企業\).md "wikilink")[NuBus](../Page/NuBus.md "wikilink")後の[PowerPC](../Page/PowerPC.md "wikilink")ベースのMacintosh（[CHRP](https://ja.wikipedia.org/wiki/CHRP "wikilink")ベースの[Power Macintosh](../Page/Power_Macintosh.md "wikilink")）、[サン・マイクロシステムズ](../Page/サン・マイクロシステムズ.md "wikilink")の[SPARC](../Page/SPARC.md "wikilink")ベースのワークステーションとサーバ、[IBM](../Page/IBM.md "wikilink")の[POWERアーキテクチャの計算機システム](../Page/POWER_\(マイクロプロセッサ\).md "wikilink")（[CHRP](https://ja.wikipedia.org/wiki/CHRP "wikilink")ベースの[RS/6000](https://ja.wikipedia.org/wiki/RS/6000 "wikilink") [PCIモデル](../Page/Peripheral_Component_Interconnect.md "wikilink")）、[Pegasos](https://ja.wikipedia.org/wiki/Pegasos "wikilink")の計算機システム、そして[OLPC](../Page/OLPC.md "wikilink")によって設計されたラップトップ（[OLPC XO-1](https://ja.wikipedia.org/wiki/OLPC_XO-1 "wikilink")）など、色々な機種で採用された。

Open Firmwareは[BSDライセンス](../Page/BSDライセンス.md "wikilink")下で利用可能である。提案されている[Power Architecture Platform Referenceでも](https://ja.wikipedia.org/wiki/PAPR "wikilink")、Open Firmwareベースのプラットフォームである。それらのプラットフォーム上では、Open Firmwareは[PC上での](../Page/パーソナルコンピュータ.md "wikilink")[BIOSの動作とまったく同じことができる](https://ja.wikipedia.org/wiki/Basic_Input/Output_System "wikilink")。

Open Firmwareは[Forth](../Page/Forth.md "wikilink")ベースの[シェル](../Page/シェル.md "wikilink")インタフェースを持つ。Forthは強力な高レベル言語で、たとえば、Open Firmware上で[ハノイの塔](../Page/ハノイの塔.md "wikilink")の問題を解くことが可能である。

Open Firmwareは[IEEE](../Page/IEEE.md "wikilink")によって、**IEEE 1275-1994**として標準化された。最新仕様については、オーストリアの[ウィーン工科大学](https://ja.wikipedia.org/wiki/ウィーン工科大学 "wikilink")コンピュータ言語研究所のForth研究プロジェクトから利用可能である。

SunのOpenBootやFirmwoksのOpenFirmware、CodegenのSmartFirmwareなど、いくつかのOpen Firmwareの商用実装は、2006年にオープンソースコミュニティにリリースされた。このソースは[OpenBIOS](https://ja.wikipedia.org/wiki/OpenBIOS "wikilink")プロジェクトで公開されている。

## 利点

Open FirmwareのForth言語によるコードは[FCode](https://ja.wikipedia.org/wiki/FCode "wikilink")(と呼ばれるバイトコード)にコンパイルされ、特定のコンピュータアーキテクチャに依存した[機械語](../Page/機械語.md "wikilink")に変換されない。つまり、あるI/Oカード用のコードを含んでいるOpen Firmwareは、他のOpen Firmwareを使うどんなシステム上でも動作することが可能である。この方法により、あるI/Oカードの起動時診断や設定用コード、そしてデバイスドライバは、他のOpen Firmwareが動作するシステム上でも使える。したがって、多くのI/OカードがSunのマシンとMacintoshの両方の上で動作することが可能である。

また、インタラクティブなプログラミング言語をベースとしているので、Open Firmwareはコードのテストや新しいハードウェアへの追従を素早く行うことができる。

## アクセス

幾つかのアーキテクチャではオペレーティングシステムのブート前にコンソールからOpen Firmwareのプロンプトを通してテキストベースで対話的にアクセスすることが可能である（たとえばMacintoshなら、起動時にoptionキーとcommandキー、さらにO(オー)キーとFキーを同時に押し続けると、Open Firmwareにアクセスできる）。認識されたデバイスはForthの名前空間に現れ、これを使い入出力デバイスの指示等を行う。バス別に、規定された名前空間が存在し、構成情報を取得し設定することも出来る。

Open Firmwareは"ok"をプロンプトとして表示する。

## 関連項目

  - [BIOS](https://ja.wikipedia.org/wiki/Basic_Input/Output_System "wikilink")

  - [Extensible Firmware Interface](../Page/Unified_Extensible_Firmware_Interface.md "wikilink") (EFI)

  - [Unified Extensible Firmware Interface](../Page/Unified_Extensible_Firmware_Interface.md "wikilink") (UEFI)

  - \- OpenFirmware標準の別実装

  - LinuxBIOS - [Linux](../Page/Linux.md "wikilink")をベースとしたフリーの[BIOS実装](https://ja.wikipedia.org/wiki/Basic_Input/Output_System "wikilink")。[Coreboot](https://ja.wikipedia.org/wiki/Coreboot "wikilink")を参照。

  -
  - [Advanced Configuration and Power Interface](../Page/Advanced_Configuration_and_Power_Interface.md "wikilink") (ACPI)

  - [Power On Self Test](../Page/Power_On_Self_Test.md "wikilink") (POST)

  - [BootX](https://ja.wikipedia.org/wiki/BootX_\(アップル\) "wikilink") - [Mac OS XのPowerPC用ブートローダー](https://ja.wikipedia.org/wiki/macOS "wikilink")

## 外部リンク

  - [1275 Open Firmware Home Page](http://playground.sun.com/1275/)
  - [OpenFirmware](http://www.openfirmware.org)
  - [OpenBIOS](http://www.openbios.org)
  - [SUN's SPARC OBP documentation](http://sunsolve.sun.com/data/802/802-3242/html/TOC.html)
  - [IEEE 1275の最新仕様](http://www.complang.tuwien.ac.at/forth/1275.ps.gz)
  - [SmartFirmware](http://www.codegen.com/SmartFirmware/)
  - [FirmWorks](http://www.firmworks.com)
  - [Firmworksのソースコード](http://www.openbios.org/viewvc/?root=OpenFirmware)
  - [SmartFirmwareのソースコード](http://www.openbios.org/viewvc/?root=SmartFirmware)
  - [IBM POWER上のブートプロセス](http://www-941.ibm.com/collaboration/wiki/display/WikiPtype/Boot+Process+on+POWER)

[Category:ファームウェア](https://ja.wikipedia.org/wiki/Category:ファームウェア "wikilink") [Category:IEEE標準](https://ja.wikipedia.org/wiki/Category:IEEE標準 "wikilink") [Category:Mac_OS](https://ja.wikipedia.org/wiki/Category:Mac_OS "wikilink") [Category:サン・マイクロシステムズ](https://ja.wikipedia.org/wiki/Category:サン・マイクロシステムズ "wikilink")
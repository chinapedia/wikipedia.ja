> この記事は[MicroBlaze](https://ja.wikipedia.org/wiki/MicroBlaze)から翻訳されています。


**MicroBlaze**は、[ザイリンクス](https://ja.wikipedia.org/wiki/ザイリンクス "wikilink")による、ザイリンクス製[FPGA向けに構築した](https://ja.wikipedia.org/wiki/プログラマブルロジックデバイス#FPGA "wikilink")[ソフトプロセッサ](../Page/ソフトプロセッサ.md "wikilink")コアである。MicroBlazeはザイリンクスのFPGAの汎用メモリと論理回路で、32bitソフトプロセッサとして実装している\[1\]。

## 概要

命令セットアーキテクチャは、MicroBlazeは[パターソンと](../Page/デイビッド・パターソン_\(計算機科学者\).md "wikilink")[ヘネシーによる有名なコンピュータアーキテクチャの書籍で記述された](https://ja.wikipedia.org/wiki/ジョン・ヘネシー "wikilink")、[RISC](../Page/RISC.md "wikilink")ベースの[DLX](https://ja.wikipedia.org/wiki/DLX "wikilink")アーキテクチャと非常に似ている。ほとんどのMicroBlaze命令セットは、1サイクルで実行することが出来る。

MicroBlazeは多様な[組み込みアプリケーションをサポートするために](../Page/組み込みシステム.md "wikilink")、多用途のインターコネクトシステムを持っている。MicroBlazeの主要なI/Oバスの[CoreConnect](https://ja.wikipedia.org/wiki/CoreConnect "wikilink") [PLBバス](https://ja.wikipedia.org/wiki/PLBバス "wikilink")は、システムメモリにマップされたマスタ・スレーブによる伝統的なトランザクションバスである。多数のベンダが供給するサードパーティのIPは、PLBバスに直接接続する。（またはPLBバスから[OPBバス](https://ja.wikipedia.org/wiki/OPBバス "wikilink")へのブリッジを経由して接続する。）ローカルメモリ（FPGAの[BRAM](https://ja.wikipedia.org/wiki/BRAM "wikilink")）へのアクセスでは、MicroBlazeは専用の[LMBバス](https://ja.wikipedia.org/wiki/LMBバス "wikilink")を使うことで他のバスの負荷を軽減する。ユーザ定義のコプロセッサは、FSL(Fast Simplex Link)と呼ばれる専用のFIFO形式の接続を経由してサポートされる。コプロセッサインタフェースは、計算処理の一部または全部を、ユーザが設計したハードウェアモジュールで行うことで、計算量が集中するアルゴリズムを加速することが出来る。

MicroBlazeの多くの要素は、ユーザによる設定が可能である。キャッシュサイズ、パイプラインの段数（3段または5段）、組み込みの周辺インタフェース、[メモリ管理ユニット](https://ja.wikipedia.org/wiki/メモリ管理ユニット "wikilink")、バス・インタフェースがカスタマイズ可能である。サイズに最適化したMicroBlazeは、3段のパイプラインを使用し、論理回路の削減のためにクロック周波数を犠牲にしている。性能に最適化したバージョンは、実行パイプラインを5段に拡張し、最大210 [MHz](https://ja.wikipedia.org/wiki/メガヘルツ "wikilink")（Virtex-5 [FPGA](https://ja.wikipedia.org/wiki/プログラマブルロジックデバイス#FPGA "wikilink") シリーズの場合）での動作が可能である。また、めったに使用されないがハードウェアでの実装が高価となる重要なプロセッサの命令は、選択的に追加／削除が可能である。（すなわち、乗算・除算・浮動小数点命令である）この改変により、開発者はホストハードウェアの条件とアプリケーションソフトの要件に見合った、適切な設計を行うことが可能である。

MMUを使用しない場合、MicroBlazeで動作するオペレーティングシステムは、単純化された保護と仮想メモリモデルに限られる。例えば[μClinux](https://ja.wikipedia.org/wiki/μClinux "wikilink")ベースのオペレーティングシステムや[TOPPERS/JSPカーネル](https://ja.wikipedia.org/wiki/TOPPERS/JSPカーネル "wikilink"), [FreeRTOS](https://ja.wikipedia.org/wiki/FreeRTOS "wikilink")が相当する。MMUを使用する場合、MicroBlazeの全体的な[スループット](../Page/スループット.md "wikilink")は、同等のハードウェアによるCPUコア（例えばVirtex4の中のPowerPC405）よりもかなり低くなるが、[Linux](https://ja.wikipedia.org/wiki/Linux "wikilink")カーネルのような、ハードウェアベースのページングと保護を要求するオペレーティングシステムを動作させることが出来る。

## EDK

ザイリンクスのEDK (Embedded Development Kit)は、ザイリンクスのFPGAで、MicroBlaze（およびPowerPC）組み込みプロセッサを構築するための開発環境パッケージである。これは[Eclipseの上で動作し](../Page/Eclipse_\(統合開発環境\).md "wikilink")、プロジェクトマネージャは2つの別々の環境（XPSとSDK）で構築されている。

設計者は、彼らの組み込みシステムのハードウェア仕様（プロセッサコア、メモリコントローラ、周辺機器I/O、等）を設定し構築するためにXPS (Xilinx Platform Studio)を使用する。XPSは設計者のプラットフォーム仕様を合成可能な[RTL記述](../Page/レジスタ転送レベル.md "wikilink")(Verilogまたは[VHDL](https://ja.wikipedia.org/wiki/VHDL "wikilink"))に変換し、組み込みシステムの実装を自動化するためのスクリプトのセットを書き出す。（RTLからビットストリームファイルまで）MicroBlazeコアにおいて、EDKは通常暗号化された（人間が読めない）[ネットリスト](https://ja.wikipedia.org/wiki/ネットリスト "wikilink")を出力するが、VHDLで書かれたプロセス記述はザイリンクスから購入することが出来る。

SDKは、組み込みシステムの上で動作させるソフトウェアを扱う。[GNUツールチェイン](https://ja.wikipedia.org/wiki/GNUツールチェイン "wikilink")（[GNUコンパイラコレクション](../Page/GNUコンパイラコレクション.md "wikilink")、[GNUデバッガ](../Page/GNUデバッガ.md "wikilink")）を活用し、SDKでプログラマは彼らの組み込みシステム上のC/C++アプリケーションを書き、コンパイルし、デバッグすることが出来る。ザイリンクスはサイクルに精密な命令セットシミュレータ（Instruction Set Simulator, ISS）を提供し、プログラマにシミュレーションで彼らのソフトをテストする方法と、適切なFPGAボードにダウンロードして実際のシステムで実行させる方法を提供している。

XPSの購入者は、定期的に追加のロイヤリティを支払うことなく、MicroBlazeをザイリンクスのFPGAで使用する永久のライセンスが与えられる。このライセンスはMicroBlazeをザイリンクス以外のデバイスで使用する権利を与えていないので、必要な場合はザイリンクスとの直接の交渉が必要となる。

## クローン

  - [aeMB](http://www.aeste.net/project/aemb/)、[Verilog](https://ja.wikipedia.org/wiki/Verilog "wikilink")による実装、[LGPLライセンス](../Page/GNU_Lesser_General_Public_License.md "wikilink")
  - [OpenFire](http://www.ccm.ece.vt.edu/~scraven/openfire.html)、Verilogによるサブセットの実装、[MITライセンス](https://ja.wikipedia.org/wiki/MIT_License "wikilink")

## その他のソフトプロセッサ

  - [LatticeMico8](https://ja.wikipedia.org/wiki/LatticeMico8 "wikilink")
  - [LatticeMico32](https://ja.wikipedia.org/wiki/LatticeMico32 "wikilink")
  - [PicoBlaze](../Page/PicoBlaze.md "wikilink")
  - [Nios II](https://ja.wikipedia.org/wiki/Nios_II "wikilink")
  - [Nios](https://ja.wikipedia.org/wiki/Nios_embedded_processor "wikilink")
  - [OpenRISC](https://ja.wikipedia.org/wiki/OpenRISC "wikilink")
  - [Xtensa](https://ja.wikipedia.org/wiki/Xtensa "wikilink")

## 脚注

## 関連項目

  - [ソフトプロセッサ](../Page/ソフトプロセッサ.md "wikilink")
  - [OpenCores](https://ja.wikipedia.org/wiki/OpenCores "wikilink") - 多数の[オープンソース](../Page/オープンソース.md "wikilink")の[ソフトプロセッサ](../Page/ソフトプロセッサ.md "wikilink")プロジェクトのホームページ

## 外部リンク

  - [MicroBlaze on Xilinx website](http://japan.xilinx.com/microblaze)
  - [uClinux port on MicroBlaze](http://www.itee.uq.edu.au/~jwilliams/mblaze-uclinux/)
  - [MicroBlaze-Based Introduction To Computer Architecture and Assembly Language](http://wiki.ittc.ku.edu/ittc/Eecs388)
  - [MicroBlaze Embedded Linux support from LynuxWorks (BlueCat Linux)](http://www.lynuxworks.com/board-support/xilinx.php)
  - [Linux and U-BOOT for Microblaze CPU - Michal Simek - maintainer](http://www.monstr.eu/wiki/)

[Category:マイクロプロセッサ](https://ja.wikipedia.org/wiki/Category:マイクロプロセッサ "wikilink")

1.  MicroBlaze ソフト プロセッサ コア <https://japan.xilinx.com/products/design-tools/microblaze.html>
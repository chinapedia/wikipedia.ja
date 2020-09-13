> この記事は[Linuxカーネル](https://ja.wikipedia.org/wiki/Linuxカーネル)から翻訳されています。


**Linuxカーネル**は、[Unix系](../Page/Unix系.md "wikilink")[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink")である[Linux](../Page/Linux.md "wikilink")の[カーネル](../Page/カーネル.md "wikilink")。[リーナス・トーバルズ](../Page/リーナス・トーバルズ.md "wikilink")によって開発が開始された。ライセンスに[GPL](../Page/GNU_General_Public_License.md "wikilink")（バージョン2）を採用する[自由なソフトウェアである](../Page/フリーソフトウェア.md "wikilink")。

通常、Linuxカーネルと言えばリーナスが管理・公開している公式版（メインライン・カーネル）を指すが、[Linuxディストリビューション](../Page/Linuxディストリビューション.md "wikilink")で使用されているカーネルは、バージョンが古かったり、ベンダーが独自の改造を施してあることが多い。例えば、[Androidで使用されているカーネルもそのひとつである](../Page/Android_\(オペレーティングシステム\).md "wikilink")。このような非公式のカーネルは、ベンダー側が対応すべきとしているため、Linux Kernel Mailing Listなどでは基本的に対応対象外となっている。

開発の初期には、[MINIX](../Page/MINIX.md "wikilink")を参考としており、影響を受けてもいるが、MINIXのコードは使用せず、ゼロから書かれた（[IBM PCを](../Page/IBM_PC.md "wikilink")[端末エミュレータ](../Page/端末エミュレータ.md "wikilink")として動かすためのコードから成長させたものと言われている）。

GPLを採用したことがLinuxを共有の物として開発することを推進させた、とされている。また、Linuxの開発と[インターネット](../Page/インターネット.md "wikilink")の発展が時期的に一致したことも、Linuxの開発コミュニティ形成に寄与した。

また、開発に際して、よりオープンな開発体制をとり、現在[バザール方式](../Page/バザール方式.md "wikilink")と呼ばれている、誰でもLinux Kernel Mailing Listへのバグ報告や修正、機能拡張パッチを公開でき、その中から最終的にリーナスと彼が任命したメインテナーがコーディネータとなって、公式版のLinuxカーネルの質を保っている。

## 対応アーキテクチャ

[Linux_kernel_ubiquity.svg](https://ja.wikipedia.org/wiki/File:Linux_kernel_ubiquity.svg "fig:Linux_kernel_ubiquity.svg")  Linuxカーネルは各種[命令セット](../Page/命令セット.md "wikilink") (ISA) に対応している。各アーキテクチャで共有されているコードが多いため、CPUに依存した部分を変更すれば移植できるようになっている。

### 公式サポート

バージョン4.17現在。

  - [DEC Alpha](https://ja.wikipedia.org/wiki/DEC_Alpha "wikilink")

  -
  - [ARM](../Page/ARMアーキテクチャ.md "wikilink")

  - [AMD64](https://ja.wikipedia.org/wiki/x64 "wikilink")

  -
  - [H8](../Page/H8.md "wikilink")/300

  -
  - [IA-64](../Page/IA-64.md "wikilink")

  - [MC68000](../Page/MC68000.md "wikilink")

  - [MicroBlaze](../Page/MicroBlaze.md "wikilink")

  - [MIPS](../Page/MIPSアーキテクチャ.md "wikilink")

  -
  - [Nios II](https://ja.wikipedia.org/wiki/Nios_II "wikilink")

  - [Andes NDS32](https://ja.wikipedia.org/wiki/Andes_NDS32 "wikilink")

  - [OpenRISC](https://ja.wikipedia.org/wiki/OpenRISC "wikilink")

  - [PA-RISC](../Page/PA-RISC.md "wikilink")

  - [PowerPC](../Page/PowerPC.md "wikilink")（[POWER5](https://ja.wikipedia.org/wiki/POWER5 "wikilink")以降、[Cellも互換CPUとして動いている](../Page/Cell_Broadband_Engine.md "wikilink")）

  - [S/390](https://ja.wikipedia.org/wiki/IBM_S/390 "wikilink")

  - [SuperH](../Page/SuperH.md "wikilink")

  - [SPARC](../Page/SPARC.md "wikilink")（Sun-4など除く）

  -
  - [x86](https://ja.wikipedia.org/wiki/x86 "wikilink")（[Intel 80486以降](https://ja.wikipedia.org/wiki/Intel_80486 "wikilink")）

  - [Xtensa](https://ja.wikipedia.org/wiki/Xtensa "wikilink")

### 非公式サポート

  - [RISC-V](https://ja.wikipedia.org/wiki/RISC-V "wikilink") - [1](https://github.com/riscv/riscv-linux)

### サポート終了

  - バージョン2.6.26まで

<!-- end list -->

  - Sun-4

<!-- end list -->

  - バージョン3.4まで

<!-- end list -->

  - SPARCstation/SPARCserver series

<!-- end list -->

  - バージョン3.7まで

<!-- end list -->

  - x86 ([i386](../Page/Intel_80386.md "wikilink"))

<!-- end list -->

  - バージョン4.11まで

<!-- end list -->

  -
<!-- end list -->

  - バージョン4.16まで

<!-- end list -->

  - [Blackfin](../Page/Blackfin.md "wikilink")

  - [CRIS](https://ja.wikipedia.org/wiki/CRIS "wikilink")

  - [FR-V](https://ja.wikipedia.org/wiki/FR-V "wikilink")

  - [M32R](https://ja.wikipedia.org/wiki/M32R "wikilink")

  -
  - [POWER4](https://ja.wikipedia.org/wiki/POWER4 "wikilink")

  -
  -
## 出典

<references />

## 関連項目

  - [Linux-libre](https://ja.wikipedia.org/wiki/Linux-libre "wikilink") - Linuxカーネルから[バイナリ・ブロブ](https://ja.wikipedia.org/wiki/バイナリ・ブロブ "wikilink")を取り除いたカーネル。
  - [Native POSIX Thread Library](../Page/Native_POSIX_Thread_Library.md "wikilink")
  - [Cooperative Linux](../Page/Cooperative_Linux.md "wikilink") - coLinuxとも呼ばれる。Windows上でLinuxカーネルが動作するようにしたもの。
  - [ローダブル・カーネル・モジュール](https://ja.wikipedia.org/wiki/ローダブル・カーネル・モジュール "wikilink") (LKM)
  - [vmlinux](https://ja.wikipedia.org/wiki/vmlinux "wikilink") - カーネル本体のコードを含む「カーネルイメージ」と呼ばれる特殊なファイル（その特殊性により、単なる実行ファイルではない）の慣習的な名前

## 外部リンク

  - [The Linux Kernel Archives](https://www.kernel.org/)
  - [Linux HeadQuarters](http://www.linuxheadquarters.com/)
  - [Interactive map of Linux kernel](https://www.makelinux.net/kernel_map/)

[Category:Linux](https://ja.wikipedia.org/wiki/Category:Linux "wikilink") [Category:オープンソースソフトウェア](https://ja.wikipedia.org/wiki/Category:オープンソースソフトウェア "wikilink") [Category:OSのカーネル](https://ja.wikipedia.org/wiki/Category:OSのカーネル "wikilink") [Category:1991年のソフトウェア](https://ja.wikipedia.org/wiki/Category:1991年のソフトウェア "wikilink")
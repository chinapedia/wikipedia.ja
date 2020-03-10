> この記事は[RAM](https://ja.wikipedia.org/wiki/RAM)から翻訳されています。


**RAMディスク**（ラムディスク）は、[Random Access Memory](../Page/Random_Access_Memory.md "wikilink")（ランダムアクセスメモリ、RAM）による[ストレージ](https://ja.wikipedia.org/wiki/ストレージ "wikilink")である。

[ディスクメディア](../Page/ディスクメディア.md "wikilink")ではないが、[ディスクドライブ](../Page/ディスクドライブ.md "wikilink")を[エミュレート](https://ja.wikipedia.org/wiki/エミュレート "wikilink")することから「〜ディスク」と呼称される。

## 種類

実現の仕方により、大きく2種類に分かれる。

  - ハードウェア方式
    RAMを搭載した専用の[ハードウェア](../Page/ハードウェア.md "wikilink")を用意し、[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink") (OS) からは[ハードディスクドライブ](https://ja.wikipedia.org/wiki/ハードディスクドライブ "wikilink") (HDD) 等の通常の[外部記憶装置とまったく同じに見える](../Page/補助記憶装置.md "wikilink")（実際は追加のデバイスドライバを必要とする製品もある）。[ソリッドステートドライブ](https://ja.wikipedia.org/wiki/ソリッドステートドライブ "wikilink")（半導体ディスク）の一種であり、近年の[フラッシュメモリ](../Page/フラッシュメモリ.md "wikilink")を使った[Flash SSDと同じ原理である](https://ja.wikipedia.org/wiki/ソリッドステートドライブ "wikilink")。
  - ソフトウェア方式
    専用のハードウェアは持たず、[デバイスドライバ](../Page/デバイスドライバ.md "wikilink")により[主記憶装置](../Page/主記憶装置.md "wikilink")（メインメモリ）の一部を仮想化した外部記憶装置として使う。[仮想ディスク](https://ja.wikipedia.org/wiki/仮想ディスク "wikilink")（）の一種である。

## 特徴

[データレコーダ](../Page/データレコーダ.md "wikilink")、[フロッピーディスク](../Page/フロッピーディスク.md "wikilink")、[ハードディスクドライブ](https://ja.wikipedia.org/wiki/ハードディスクドライブ "wikilink")などの装置には、媒体の回転やアクセスヘッドの移動など機械的な駆動部が多く、振動、騒音、発熱、摩耗などの問題がある。また、ヘッドを目的の位置に移動するのに時間を要する点や読み書き自体の速度において主記憶に比べると遅い装置だと言える。

RAMディスクは、[揮発性を持つ](https://ja.wikipedia.org/wiki/揮発性メモリ "wikilink")[半導体メモリ](../Page/半導体メモリ.md "wikilink")を使い、非常に高速で、振動、騒音、摩耗などの欠点を持たない記憶機能を提供する。 また、発熱についてもHDDに比べれば小さい。一方、RAMを用いることから記録した情報を保持するには常に外部からの電源供給が必要であり、また磁気ならびに光を用いる各種記録媒体に比べると情報量当たりの価格（容量単価）が高いという欠点がある。よって、[アプリケーションの作業領域といった一時的な記憶媒体として用いるのが一般的である](../Page/アプリケーションソフトウェア.md "wikilink")。

なお、フラッシュディスクや各種[メモリーカード](../Page/メモリーカード.md "wikilink")なども同様に半導体メモリを記憶媒体として利用しているが、それらは[不揮発性の](../Page/不揮発性メモリ.md "wikilink")[フラッシュメモリ](../Page/フラッシュメモリ.md "wikilink")を採用しており、電源を切っても情報が保持される点でRAMディスクと区別される。

## ハードウェアによるRAMディスク

### 概要

工業用コンピューターシステムにおいて、HDDのような機械的な駆動部を持つ装置は耐久性などの問題が大きかった。こういった分野に対して、対振動性や防塵密封運用での耐熱性の高い装置として、半導体だけでファイルシステムを提供する装置が生まれた。半導体と言うことで「シリコンディスク」と呼ばれる事もある。

IDE ([ATA](../Page/Advanced_Technology_Attachment.md "wikilink"))、[SATAや](https://ja.wikipedia.org/wiki/シリアルATA "wikilink")[SCSIに対応した装置もあり](../Page/Small_Computer_System_Interface.md "wikilink")、コンピュータ側からは、単にHDDと同様に認識され、システムの起動装置としても問題なく利用できる。RAMであるため、高い書き換え性能と書き換え耐久性を実現している。 ただし、HDDなどと比べると、生産数の少なさもあり、ビット単価は非常に高価なものとなっている。

SRAM以外のメモリーを利用するものもあるが、それぞれに長所短所がある。本来HDD代替として作られていないメモリーを流用するための[IDE変換](https://ja.wikipedia.org/wiki/IDE変換 "wikilink")といった技術もある。一般市場向けにも、汎用拡張スロットに増設するRAMディスク専用の拡張メモリ製品が古くから存在している。別途購入という点で割高感があることや、近年ではHDDやキャッシュメモリ、OSのキャッシュ技術の進歩によって十分実用的な性能が得られることから、あまり広く普及してはいない。

一方で、1998年3月\[1\]にヤノ電器がパソコン用のDIMMを搭載できるPCI接続のRAMディスクYR833を発売している（現在は生産停止）\[2\]。近年では、2005年に[GIGABYTE](https://ja.wikipedia.org/wiki/GIGABYTE "wikilink")が[DDR SDRAMを搭載できる](https://ja.wikipedia.org/wiki/DDR_SDRAM "wikilink")[シリアルATA](https://ja.wikipedia.org/wiki/シリアルATA "wikilink")接続のRAMディスク製品[i-RAM](https://ja.wikipedia.org/wiki/i-RAM "wikilink")を発売している（現在は販売中止）。2008年には[ACARD Technologyから](https://ja.wikipedia.org/wiki/ACARD_Technology "wikilink")[DDR2 SDRAMに対応したシリアルATA接続のRAMディスク製品](../Page/DDR2_SDRAM.md "wikilink")[ANS-9010シリーズが発売された](https://ja.wikipedia.org/wiki/i-RAM#同コンセプトの他社製品 "wikilink")。

### 初期のノートパソコンの例

20MB程度の3.5インチ外付けHDD([SASI](https://ja.wikipedia.org/wiki/SASI "wikilink"))で20万円ほどした時代、黎明期の[ノートパソコン](../Page/ノートパソコン.md "wikilink")（当時は「ラップトップ」）では、技術的な制約によりHDDもCD-ROMもなく、その殆どがFDD1基を備えるのみであった（一部の上級機ではFDD2基仕様も存在した）。 しかし、当時のMS-DOS用のアプリケーションはFDD2基を前提としているものも多く、日本語環境の場合はかな漢字変換辞書の存在もあり、機能の増加と共にFDD1基ですべてをまかなうことは困難になりつつあった。

[1989年](../Page/1989年.md "wikilink")、今日のノートパソコンに近い商品として販売された[東芝・ダイナブック(J-3100SS)では](https://ja.wikipedia.org/wiki/ダイナブック_\(東芝\) "wikilink")、 メインメモリを標準で1.5MB搭載し、うち記憶用に896KB確保された領域は**RAMドライブ**として確保され、漢字変換システムやソフトウェアを保存する領域として用いられていた。PC-9801シリーズでも、同様の仕組みを持っており、当時FDDが2基存在することを前提としたアプリケーションの動作環境を構築したり、RAMドライブからオペレーションシステムを起動するため用意された。PC-9801シリーズの場合は、[BIOS](https://ja.wikipedia.org/wiki/BIOS "wikilink")画面において、FDDからの相互コピーをサポートしていた。 後にノートパソコンでも[80286](https://ja.wikipedia.org/wiki/80286 "wikilink")、[80386](https://ja.wikipedia.org/wiki/80386 "wikilink")機が登場すると、以下に述べる主記憶を使ったより一般的なRAMディスクへと移行したが、HDDを持つものが増えていった。

### Macintosh

古い[Macintosh](../Page/Macintosh.md "wikilink")では、本体メモリの一部をRAMディスクとして使用することができた\[3\]。このRAMディスクは、[ファームウェア](../Page/ファームウェア.md "wikilink")レベルでサポートされているため、起動ディスクとして使用することもできた\[4\]。しかし、[Power Macintosh](https://ja.wikipedia.org/wiki/Power_Macintosh "wikilink") G3以降のGrackleメモリコントローラを採用した機種では、再起動時にRAMディスクの内容が保存されなくなり、起動ディスクとして使用することができなくなった\[5\]。現行機種は、[ファームウェアレベルでのRAMディスク機能は持っていない](https://ja.wikipedia.org/wiki/Unified_Extensible_Firmware_Interface "wikilink")。

## ソフトウェアによるRAMディスク

### 概要

OSが起動した後、あるいは起動過程において、専用の[デバイスドライバ](../Page/デバイスドライバ.md "wikilink")等が[主記憶の一部を確保し](../Page/主記憶装置.md "wikilink")、OSが利用可能な[ファイルシステム](../Page/ファイルシステム.md "wikilink")として利用する仕組みのことで、一般ユーザにおいて単にRAMディスクと言えばこれを意味する。

外部記憶装置であるFDDやHDDなどに比べた場合、主記憶を利用したRAMディスクのほうが大幅に高速に動作する。このため、FDDから[MS-DOS](../Page/MS-DOS.md "wikilink")を起動して利用していた時代には、RAMディスクに[かな漢字変換](https://ja.wikipedia.org/wiki/かな漢字変換 "wikilink")の辞書を置くことが一般的だった。これはMS-DOSが直接利用できるメモリーが1MBでしかなく、追加されたメモリーの多くを間接的に利用せざるを得なかった影響もある。

その後、高速なHDDと[キャッシュメモリ](../Page/キャッシュメモリ.md "wikilink")の普及によって、RAMディスクを使わずとも問題なく快適に利用できるため、上記のようなRAMディスクの利用は廃れた。しかしながらRAMディスクの利便性（高速なアクセス、HDDの消耗や[FAT系ファイルシステムでの](../Page/File_Allocation_Table.md "wikilink")[断片化の抑制](../Page/デフラグメンテーション.md "wikilink")）などを認識し、細々とながら利用するユーザーがいた。さらに[2008年](https://ja.wikipedia.org/wiki/2008年 "wikilink")頃からメモリの価格下落により大容量化が進み、一部では脚光を浴びるようになってきた。

揮発する領域であるため、保存領域としてはドライバによるファイル保存等の処理が必要となる。 一プロセスであるため、プログラムの干渉や、誤動作などの影響を受けるほか、保存が可能になっているソフトウェアであっても、使用中のハングアップなど、二次記憶装置への保存が行われる前のタイミングで、システムが停止した場合、そのデータを喪失することとなる。 反面、ランダムアクセスを含む高速な入出力が可能である特性から、圧縮や、展開等の一時ファイル、作業ファイルの作成場所として指定することで、処理時間を短縮することも可能である。

また、二次記憶装置への書き込みが行われない（電源を切ればデータが残らない）という点が評価され、パスワードのような機密情報をファイル上でやり取りする際に用いられることがある。[Kubernetes](https://ja.wikipedia.org/wiki/Kubernetes "wikilink")においては、機密情報を扱う用途のSecretリソースをファイルシステムにマウントする場合にRAMディスク（後述するLinuxの[tmpfs](https://ja.wikipedia.org/wiki/tmpfs "wikilink")）が使用される\[6\]。

### 8ビットパソコン

8ビットのパソコンの中には、RAMディスクを実現できる拡張ボードをオプションで備えるものがあった、また、グラフィック画面を低解像度に制限する替わりにグラフィック[VRAM](../Page/VRAM.md "wikilink")の一部をRAMディスク化する手法も存在した。[シャープ](../Page/シャープ.md "wikilink")の[X1シリーズや](../Page/X1_\(コンピュータ\).md "wikilink")、[MSX](https://ja.wikipedia.org/wiki/MSX "wikilink")シリーズのサードパーティー製がその一例。

グラフィックスを使用しないS-OS"SWORD"では、グラフィックスVRAMをRAMDISKに割り当てるプログラムもシステム拡張の一環として公開されている。

[ROM-BASIC](https://ja.wikipedia.org/wiki/ROM-BASIC "wikilink")環境でROMと重複するアドレスに配置された通常使用されないRAM領域を、RAMディスクとして使用可能にする試みもあった。MSX2のBASIC等が該当するが、容量としては然程大きなものではなく、アクセス手順の煩雑さから処理速度も低速であり、多くのRAMDISKが持つ高速性というメリットは存在しない。 後にMSXでは、メモリマッパを介した領域を使用するRAMDISKが別途実装されている。

8ビットパソコンでは、通常利用されていた[DISK-BASIC](https://ja.wikipedia.org/wiki/DISK-BASIC "wikilink")環境ではファイル管理が貧弱で、またドライバの組み込みなどの柔軟性がほとんどないことから、RAMディスクは[CP/M](https://ja.wikipedia.org/wiki/CP/M "wikilink")などの汎用OS環境で利用することが一般的であった。

マルチメディアの為に用意されたものの、アプリケーションで使用されないVRAMをRAMディスクとして使用される試みもあった。

### MS-DOS

基本的には、デバイスドライバの読み込みを[CONFIG.SYS](https://ja.wikipedia.org/wiki/CONFIG.SYS "wikilink")などに記述してシステム起動時にRAMディスクを設定する。

[バンクメモリやハードウェア](https://ja.wikipedia.org/wiki/バンク切り換え "wikilink")[EMSメモリなどの頃から](https://ja.wikipedia.org/wiki/Expanded_Memory_Specification "wikilink")、大手[サードパーティー](https://ja.wikipedia.org/wiki/サードパーティー "wikilink")が[PC-9800シリーズ](../Page/PC-9800シリーズ.md "wikilink")用に提供するメモリモジュールには、それを管理するためのソフトウェアが付属していた。 その中にそのメモリモジュールやメモリ増設ボードに合わせたRAMディスクドライバも含まれていた。

MS-DOSバージョン4や5の時代になると、386機が一般的となり、プロテクトメモリを利用するRAMディスクドライバが標準で付属するようになった。

[FMRシリーズ](../Page/FMRシリーズ.md "wikilink")、[FM TOWNSではRAMディスクドライバはIO](../Page/FM_TOWNS.md "wikilink").SYSに予め組み込まれており、SETUP.EXE\[7\]でRAMディスクドライブを設定するだけでRAMディスクが利用できた。

### Linux

[Linux](https://ja.wikipedia.org/wiki/Linux "wikilink")でRAMディスク機能を提供する[カーネルモジュールは](../Page/デバイスドライバ.md "wikilink")[tmpfs](https://ja.wikipedia.org/wiki/tmpfs "wikilink")\[8\]やramfs\[9\]である。

#### システム起動イメージ

[Linux](https://ja.wikipedia.org/wiki/Linux "wikilink")では、起動時の初期段階で、RAMディスクイメージをマウントすることで、起動処理のために必要なデバイスドライバーを読み込んだりする仕組みを持っている。

この仕組みは、FDやCDから起動するLinuxシステムでも重要な役割りを持っている。

1.  ファイルシステムのイメージファイルを圧縮する。
2.  圧縮済みのイメージファイルをFDに保存する。
3.  圧縮済みのイメージファイルをラムディスクに展開する。

この手順によって、FDに収まらないシステムを問題無く稼働させることができる。

また、システムのルートファイルシステムをRAMディスクに移すことによって、起動に使ったFDやCD-ROMを抜き取ってしまうこともできる。

### FreeBSD

[FreeBSD](../Page/FreeBSD.md "wikilink")にも、主記憶をRAMディスク化するドライバが標準で備わっている。

  - MFS (Memory File System) - 古くからあるもの。FreeBSD 5.0で廃止。
  - md (memory disk) - FreeBSD 4.0で導入。なおFreeBSD 5.0では主記憶の他にスワップ領域も指定可能となり、またvnドライバの統合により通常ファイルをマウントする機能も備えた。
      - mdの大規模使用の実例として、[2ちゃんねる](../Page/2ちゃんねる.md "wikilink")の実況系掲示板で特定スレッド（すなわち1つのdatファイル）に対する大量の細切れアクセスを捌く用途で用いられている。

### Windows

[Microsoft製のWindows](../Page/マイクロソフト.md "wikilink") 2000/XP用サンプルドライバ\[10\]や、[アイ・オー・データ機器](https://ja.wikipedia.org/wiki/アイ・オー・データ機器 "wikilink")の[RamPhantom](../Page/RamPhantom.md "wikilink")3の様に比較的簡単に導入できるソフトウェアが有償無償問わず登場した。

[Windows 7までのWindowsは](https://ja.wikipedia.org/wiki/Windows_7 "wikilink")32bit版が主流だったが、[GBクラスのメモリが安価に入手できるようになると](../Page/ギガバイト.md "wikilink")4GBのメインメモリーを搭載するコンピューターが登場するようになった。しかし32bitOSは3.2GBを超えるメモリを認識できないため、OS管理外領域をRAMディスクとして有効利用する動きが活発化した。\[11\]

Windows 7以降は4GB以上のメモリを扱える64bit版OSの普及により、余剰領域を利用する理由が薄れたため、当時に比べると話題は沈静化した。また、HDDのデータをメモリへ自動的にキャッシュする[Windows SuperFetchの効果も向上したため](https://ja.wikipedia.org/wiki/Windows_SuperFetch "wikilink")、RAMディスクを利用する意識も一旦は薄れた。

更にSSDの登場により記憶媒体へのアクセス速度は飛躍的に向上したが、SSDのハードウェア寿命は記憶領域の書き換え回数に比例するため、WebブラウザーのキャッシュをRAMディスクに変更することでSSDの寿命をのばす動きが広がった\[12\]。

## 脚注

## 関連項目

  - [Expanded Memory Specification](https://ja.wikipedia.org/wiki/Expanded_Memory_Specification "wikilink")
  - [XMS](https://ja.wikipedia.org/wiki/XMS "wikilink")
  - [バッテリーバックアップ](../Page/バッテリーバックアップ.md "wikilink") - 主にゲーム機に搭載され、ハードウェア的なRAMディスクと言える。

[Category:補助記憶装置](https://ja.wikipedia.org/wiki/Category:補助記憶装置 "wikilink") [Category:メモリ管理](https://ja.wikipedia.org/wiki/Category:メモリ管理 "wikilink")

1.  [ヤノ電器株式会社 -経歴-](http://www.yano-el.co.jp/about/history.html)
2.  [RAMDISK「YR833」](http://www.yano-el.co.jp/products/yr/)
3.  [Apple - Support:RAM Disk: RAM ディスクの概要と設定および使用方法](http://support.apple.com/kb/TA21631?viewlocale=ja_JP)
4.  [Apple - Support:PowerBook: 電力とバッテリーを節約するためのヒント](http://support.apple.com/kb/TA29442?viewlocale=ja_JP)
5.  [Apple - Support:Power Macintosh G3: リスタート時に RAM ディスクが保存されない](http://support.apple.com/kb/TA37270?viewlocale=ja_JP)
6.
7.  TownsOSではSETUP.EXP
8.  [JF: Linux Kernel 2.6 Documentation: tmpfs.txt](http://archive.linux.or.jp/JF/JFdocs/kernel-docs-2.6/filesystems/tmpfs.txt.html)
9.  [JF: Linux Kernel 2.6 Documentation ramfs-rootfs-initramfs.txt](http://archive.linux.or.jp/JF/JFdocs/kernel-docs-2.6/filesystems/ramfs-rootfs-initramfs.txt.html)
10. [Windows 2000 の Ramdisk.sys サンプル ドライバ](http://support.microsoft.com/kb/257405)
11. [32bit Windowsの管理外領域をRAM Diskに使う](http://pc.watch.impress.co.jp/docs/2008/0512/ramdisk.htm)、[インプレス](https://ja.wikipedia.org/wiki/インプレス "wikilink") PC Watch、2008年5月12日
12. [Eee PC発売記念（？）　この小さいマシンでゲームを動かしてみよう――その2：Windows XPを頑張って軽快にしてみる](http://www.4gamer.net/games/046/G004621/20080123023/#016)、[4Gamer.net](https://ja.wikipedia.org/wiki/4Gamer.net "wikilink")、2008年1月23日
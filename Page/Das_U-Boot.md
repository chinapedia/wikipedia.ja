> この記事は[Das U-Boot](https://ja.wikipedia.org/wiki/Das_U-Boot)から翻訳されています。


**Das U-Boot**は、多種のプラットフォームに対応した[ブート](../Page/ブート.md "wikilink")ローダである。対応[プロセッサ](../Page/プロセッサ.md "wikilink")・[アーキテクチャは](../Page/コンピュータ・アーキテクチャ.md "wikilink")、[ARM](../Page/ARMアーキテクチャ.md "wikilink")、、[Blackfin](https://ja.wikipedia.org/wiki/Blackfin "wikilink")、[x86](https://ja.wikipedia.org/wiki/x86 "wikilink")、[68k](../Page/MC68000.md "wikilink")、[MicroBlaze](../Page/MicroBlaze.md "wikilink")、[MIPS](../Page/MIPSアーキテクチャ.md "wikilink")、[Altera NIOS](https://ja.wikipedia.org/wiki/Altera_NIOS "wikilink")、[NIOS2](https://ja.wikipedia.org/wiki/Nios_II "wikilink")、[PowerPC](../Page/PowerPC.md "wikilink")、[SuperH](../Page/SuperH.md "wikilink")などで、主として[ワンボードマイコン](../Page/ワンボードマイコン.md "wikilink")などといった組込み開発用の環境で使われているが、[シングルボードコンピュータ](https://ja.wikipedia.org/wiki/シングルボードコンピュータ "wikilink")や、近年の電子ガジェット類など製品で使われていることもある。

## 概要

[U-boot_openmoko_freerunner.jpg](https://ja.wikipedia.org/wiki/File:U-boot_openmoko_freerunner.jpg "fig:U-boot_openmoko_freerunner.jpg") \]\] [u-boot.png](https://ja.wikipedia.org/wiki/File:u-boot.png "fig:u-boot.png") ライセンスは[GPLである](../Page/GNU_General_Public_License.md "wikilink")。ビルドに使用するツールは[GNUツールチェーン](https://ja.wikipedia.org/wiki/GNUツールチェーン "wikilink")の[クロスコンパイラ](../Page/クロスコンパイラ.md "wikilink")（例えば[crosstool](http://www.kegel.com/crosstool)、the [Embedded Linux Development Kit](http://www.denx.de/wiki/DULG/ELDK) (ELDK)、[OSELAS.Toolchain](http://www.pengutronix.de/oselas/toolchain/index_en.html)）などで、クロスビルドによってビルドできる。

対応ファイルシステム

  - [Cramfs](https://ja.wikipedia.org/wiki/Cramfs "wikilink")
  - [ext2](https://ja.wikipedia.org/wiki/ext2 "wikilink")
  - [ext3](https://ja.wikipedia.org/wiki/ext3 "wikilink")
  - [ext4](https://ja.wikipedia.org/wiki/ext4 "wikilink")
  - [FAT](../Page/File_Allocation_Table.md "wikilink")
  - FDOS
  - [JFFS2](https://ja.wikipedia.org/wiki/JFFS2 "wikilink")
  - [ReiserFS](../Page/ReiserFS.md "wikilink")
  - UBIFS
  - YAFFS2

## 歴史

このプロジェクトの源流は、Magnus Damm によって書かれた **8xxROM** と呼ばれる 8xx Power PC のブートローダである\[1\]。1999年10月、Wolfgang Denk はこのプロジェクトをSourceForge.netに移管し、SF.net におけるプロジェクト名の制約（数字で始まる名前が利用できないこと）から、名前を PPCBoot に改名した\[2\]。PPCBoot Ver 0.4.1 は、2000年7月19日に公開された。

2002年、古いバージョンの[ソースコード](../Page/ソースコード.md "wikilink")が ARMBoot の名称でフォークされたが、その後は短期間で PPCBoot プロジェクトにマージされた。2002年11月には **PPCBoot-2.0.0** がリリースされたが、これ以降は PPC ISA に加えて ARM アーキテクチャをサポートすることを反映する為に名称を変更したため、これは PPCBoot の名前の下での最後のリリースとなった。

2002年11月の **U-Boot-0.1.0** (PPCBoot-2.0.0) には、サポート対象に[x86](https://ja.wikipedia.org/wiki/x86 "wikilink")プロセッサ・アーキテクチャが追加された。その後に、サポートアーキテクチャは、[MIPS32](https://ja.wikipedia.org/wiki/MIPS32 "wikilink")（2003年3月）、[MIPS64](https://ja.wikipedia.org/wiki/MIPS64 "wikilink")（同年4月）、Altera [NIOS-32](https://ja.wikipedia.org/wiki/NIOS-32 "wikilink")（同年10月）、[Coldfire](https://ja.wikipedia.org/wiki/Coldfire "wikilink")（同年12月）、[MicroBlaze](../Page/MicroBlaze.md "wikilink")（2004年4月）が追加された。2004年5月にリリースされた **U-Boot-1.1.2** は様々なアーキテクチャを横断し、216種類の異なる基板製品をサポートした\[3\]。

## 余談

「Das U-boot」という名称は、[ドイツ語](../Page/ドイツ語.md "wikilink")で[潜水艦](../Page/潜水艦.md "wikilink")を指し、特に英語圏で原語のまま用いる場合は「ドイツ製潜水艦」を意味する「[Uボート](https://ja.wikipedia.org/wiki/Uボート "wikilink")」との言葉遊びを成立させる為に、ドイツ語の中性名詞に付与される[定冠詞](https://ja.wikipedia.org/wiki/定冠詞 "wikilink")「Das」を付与して命名されている。

## 脚注

## 参考文献

  -
  -
## 外部リンク

  -
[Category:オープンソースソフトウェア](https://ja.wikipedia.org/wiki/Category:オープンソースソフトウェア "wikilink") [Category:ファームウェア](https://ja.wikipedia.org/wiki/Category:ファームウェア "wikilink") [Category:ブート](https://ja.wikipedia.org/wiki/Category:ブート "wikilink")

1.  [PPCBoot Homepage: Authors](http://ppcboot.sourceforge.net/#authors)
2.
3.
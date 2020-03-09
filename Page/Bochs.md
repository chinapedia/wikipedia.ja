> この記事は[Bochs](https://ja.wikipedia.org/wiki/Bochs)から翻訳されています。


**Bochs**（ボックス）は、[PC/AT互換機](https://ja.wikipedia.org/wiki/PC/AT互換機 "wikilink")の[エミュレータ](https://ja.wikipedia.org/wiki/エミュレータ "wikilink")である。2000年3月以降、[GNU LGPLに基づく](../Page/GNU_Lesser_General_Public_License.md "wikilink")[オープンソース](../Page/オープンソース.md "wikilink")となっている。

## 特徴

[BIOS等を除く大部分は標準](https://ja.wikipedia.org/wiki/Basic_Input/Output_System "wikilink")[C++](../Page/C++.md "wikilink")によって実装されており、移植性に優れる。x86[プロセッサ](https://ja.wikipedia.org/wiki/プロセッサ "wikilink")の命令実行をエミュレートするために、x86以外のコンピュータでもPC/AT互換機エミュレーションを実現できる。そのため、[Linux](https://ja.wikipedia.org/wiki/Linux "wikilink")、[FreeBSD](../Page/FreeBSD.md "wikilink")、[macOS](https://ja.wikipedia.org/wiki/macOS "wikilink")、[Windows用など非x](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")86環境を含む様々なプラットフォーム用のバージョンが存在している。

[QEMU](https://ja.wikipedia.org/wiki/QEMU "wikilink")も同様のエミュレーション手法を採用しており、どちらも実行環境およびエミュレーション対象を柔軟に選択できるためOS開発や動作テストには有用である。その反面、[VMware](https://ja.wikipedia.org/wiki/VMware "wikilink")や[Xenなど](https://ja.wikipedia.org/wiki/Xen_\(仮想化ソフトウェア\) "wikilink")[ユーザモード命令をそのままプロセッサに実行させる方式に比べると実行速度が劣るため](https://ja.wikipedia.org/wiki/CPUモード "wikilink")、仮想マシン環境をサービスとして利用するには不向きである。

## エミュレートするハードウェア

  - CPU

<!-- end list -->

  -
    標準構成では、[インテル](https://ja.wikipedia.org/wiki/インテル "wikilink") [Pentium III](https://ja.wikipedia.org/wiki/Pentium_III "wikilink") 相当のユニプロセッサである。コンパイルオプションを変更することで、[386](https://ja.wikipedia.org/wiki/80386 "wikilink")、[486](https://ja.wikipedia.org/wiki/80486 "wikilink")、[Pentium](https://ja.wikipedia.org/wiki/Pentium "wikilink")、[Pentium II](https://ja.wikipedia.org/wiki/Pentium_II "wikilink")、または [Pentium 4](../Page/Pentium_4.md "wikilink") 相当にしたり、8プロセッサまでのマルチプロセッサ環境にすることが可能である。

その他にも次のような周辺機器のエミュレーションをサポートする。

  - [Cirrus](https://ja.wikipedia.org/wiki/Cirrus "wikilink") [VGA](https://ja.wikipedia.org/wiki/VGA "wikilink")
  - [3dfx](https://ja.wikipedia.org/wiki/3dfx "wikilink") [Voodoo](https://ja.wikipedia.org/wiki/Voodoo "wikilink")
  - NE2000互換[ネットワークカード](https://ja.wikipedia.org/wiki/ネットワークカード "wikilink")
  - [IDE](../Page/Advanced_Technology_Attachment.md "wikilink")[ハードディスクドライブ](https://ja.wikipedia.org/wiki/ハードディスクドライブ "wikilink")
  - [ATAPI](https://ja.wikipedia.org/wiki/Advanced_Technology_Attachment#ATAPI "wikilink") [CD-ROM](../Page/CD-ROM.md "wikilink")/[DVD-ROM](https://ja.wikipedia.org/wiki/DVD-ROM "wikilink")ドライブ
  - [フロッピーディスクドライブ](https://ja.wikipedia.org/wiki/フロッピーディスクドライブ "wikilink")
  - [Sound Blaster](https://ja.wikipedia.org/wiki/Sound_Blaster "wikilink") 16

## 外部リンク

  - [Bochs Development Homepage](http://bochs.sourceforge.net/)
  - [dev-j](http://wiki.osdev.info/index.php?Bochs)

[Category:オープンソースソフトウェア](https://ja.wikipedia.org/wiki/Category:オープンソースソフトウェア "wikilink") [Category:エミュレーションソフトウェア](https://ja.wikipedia.org/wiki/Category:エミュレーションソフトウェア "wikilink")
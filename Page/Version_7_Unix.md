> この記事は[Version 7 Unix](https://ja.wikipedia.org/wiki/Version_7_Unix)から翻訳されています。


**Version 7 Unix**または**Seventh Edition Unix**は、[UNIX](../Page/UNIX.md "wikilink")[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink")における初期の重要なリリースのひとつ。**Version 7**とか**V7**とも呼ばれる。[ベル研究所](../Page/ベル研究所.md "wikilink")が[1979年](../Page/1979年.md "wikilink")にリリースした。[AT\&T](../Page/AT&T.md "wikilink")はV7が普及するのを待って、[1980年代](../Page/1980年代.md "wikilink")初期にUNIXの有料化を行った。V7 は[ディジタル・イクイップメント・コーポレーション](../Page/ディジタル・イクイップメント・コーポレーション.md "wikilink")の[PDP-11](../Page/PDP-11.md "wikilink")ミニコンピュータなどで動作した。

## 概要

ベル研究所からのUNIXのバージョンは、そのユーザーズマニュアルの版によって識別されていた。それがベル研究所が外部に対して広くリリースを行った最初のバージョンは[第6版があった](https://ja.wikipedia.org/wiki/Version_6_Unix "wikilink")。 ベル研究所内の [Research Unix](https://ja.wikipedia.org/wiki/Research_Unix "wikilink") の系統は Version 8 Unix に引き継がれているが、実際にはV8は [4.1BSD](../Page/BSD.md "wikilink") を導入して開発された。そして第10版まで開発した後、[Plan 9](../Page/Plan_9_from_Bell_Labs.md "wikilink") の開発に集中するようになった。

V7は最初の真に[移植可能なUNIXであり](https://ja.wikipedia.org/wiki/移植_\(ソフトウェア\) "wikilink")、様々な移植が行われた。当時は[ミニコンピュータ](https://ja.wikipedia.org/wiki/ミニコンピュータ "wikilink")全盛期であり、16ビットのマイクロプロセッサも登場しつつあった。そういった様々なアーキテクチャにリリースから数年で移植が行われている。[サン・マイクロシステムズ](../Page/サン・マイクロシステムズ.md "wikilink")の最初のワークステーションでは（[MC68010](https://ja.wikipedia.org/wiki/MC68010 "wikilink")ベース）、[Unisoft社が移植した](https://ja.wikipedia.org/wiki/:en:Unisoft\<!--_存在せずリンク元がない_--\> "wikilink") V7 が動作した。最初の[XENIX](../Page/XENIX.md "wikilink")は V7 の拡張であり、[Intel 8086](../Page/Intel_8086.md "wikilink") 向けである。[Onyx Systems](https://ja.wikipedia.org/wiki/:en:Onyx_Systems "wikilink") は [Zilog](../Page/ザイログ.md "wikilink") [Z8000](https://ja.wikipedia.org/wiki/Z8000 "wikilink") に移植している。[VAX](https://ja.wikipedia.org/wiki/VAX "wikilink")に移植された V7 は [UNIX/32V](https://ja.wikipedia.org/wiki/UNIX/32V "wikilink") と呼ばれ、[BSD](../Page/BSD.md "wikilink")系Unixの直接の先祖にあたる。[ウーロンゴン大学](https://ja.wikipedia.org/wiki/ウーロンゴン大学 "wikilink")のチームはミニコンピュータ [Interdata 7/32](https://ja.wikipedia.org/wiki/Interdata_7/32 "wikilink") に V7 を移植した。これを[Interdataと同社を買収した](https://ja.wikipedia.org/wiki/:en:Interdata "wikilink")[PerkinElmer](https://ja.wikipedia.org/wiki/PerkinElmer "wikilink") が Edition VII として製品化し販売。世界初のUNIXの商用製品とされている。

[DECは](../Page/ディジタル・イクイップメント・コーポレーション.md "wikilink")、修正を加えた V7 を **V7M** としてPDP-11向けに配布した。V7MはDECのUNIX技術部門の開発によるもので、テキストとデータの分離、ハードウェアエラー対応、数々のデバイスドライバなどが加えられている。多数のテープ装置やディスク装置を接続した環境で問題なく動作できるようにすることにも力が注がれた。V7Mは品質が高く評価されていた。この技術部門が後に [Ultrix](https://ja.wikipedia.org/wiki/Ultrix "wikilink") 開発部門へと発展していったのである。

その強力さとエレガントな単純さから、Version 7 Unix を「最後の真のUNIX」と称する者もいる\[1\]。

## フリーソフトウェアとしてのリリース

[2002年](../Page/2002年.md "wikilink")、[カルデラ社は](../Page/SCO.md "wikilink")[フリーソフトウェア](../Page/フリーソフトウェア.md "wikilink")ライセンスで V7 をリリースした\[2\]。

V7のブートイメージは[こちら](http://ftp.fibranet.com/UnixArchive/PDP-11/Boot_Images/)でダウンロードでき、などPC上のPDP-11エミュレータ上で実行可能である。

## V7/x86

Nordier & Associates は[x86](https://ja.wikipedia.org/wiki/x86 "wikilink")への移植版を今も活発に開発している。2012年現在のバージョンは 0.8a で、インストーラのスクリプトを含むブート可能CDイメージが用意されている\[3\]。

## Version 7 の新機能

Version 7 で登場した新機能として、以下のものがある。

  - プログラミングツール: [lex](https://ja.wikipedia.org/wiki/lex "wikilink")、[yacc](https://ja.wikipedia.org/wiki/yacc "wikilink")、[lint](https://ja.wikipedia.org/wiki/lint "wikilink")、[pcc](../Page/Portable_C_Compiler.md "wikilink")、[make](https://ja.wikipedia.org/wiki/make "wikilink") - 一部は[PWB/UNIX](https://ja.wikipedia.org/wiki/PWB/UNIX "wikilink")が初出
  - 新コマンド: [Bourne Shell](../Page/Bourne_Shell.md "wikilink")、[at](https://ja.wikipedia.org/wiki/at_\(UNIX\) "wikilink")、[awk](../Page/AWK.md "wikilink")、calendar、[f77](https://ja.wikipedia.org/wiki/FORTRAN#FORTRAN_77 "wikilink")、[fortune](https://ja.wikipedia.org/wiki/Fortune_\(UNIX\) "wikilink")、[tar](https://ja.wikipedia.org/wiki/tar "wikilink")（従来の tp というコマンドの置換）、[touch](https://ja.wikipedia.org/wiki/touch_\(UNIX\) "wikilink")、[uucp](../Page/Unix_to_Unix_Copy_Protocol.md "wikilink")
  - 新[システムコール](https://ja.wikipedia.org/wiki/システムコール "wikilink"): access、acct、alarm、[chroot](https://ja.wikipedia.org/wiki/chroot "wikilink")（ディストリビューションの準備で評価用に使用）、[ioctl](https://ja.wikipedia.org/wiki/ioctl "wikilink")、lseek（従来は24ビットのオフセットだった）、、utime
  - 新ライブラリ関数: stdioルーチン群、[malloc](https://ja.wikipedia.org/wiki/malloc "wikilink")、getenv、popen/system
  - [環境変数](../Page/環境変数.md "wikilink")
  - [シェルスクリプト](../Page/シェルスクリプト.md "wikilink")先頭行の "\#\!" で、実行すべきシェルコマンドを指定する方式

## 脚注

## 関連項目

  - [Version 6 Unix](https://ja.wikipedia.org/wiki/Version_6_Unix "wikilink")
  - [Ancient UNIX](https://ja.wikipedia.org/wiki/Ancient_UNIX "wikilink")

## 外部リンク

  - [マニュアル](http://cm.bell-labs.com/7thEdMan/) Bell研究所
  - [ブラウジング可能なソースコード](http://minnie.tuhs.org/UnixTree/V7/)
  - [PDP Unix Preservation Society](http://minnie.tuhs.org/PUPS/)

[Category:Unix系オペレーティングシステム](https://ja.wikipedia.org/wiki/Category:Unix系オペレーティングシステム "wikilink") [Category:BSD](https://ja.wikipedia.org/wiki/Category:BSD "wikilink") [Category:1979年のソフトウェア](https://ja.wikipedia.org/wiki/Category:1979年のソフトウェア "wikilink") [Category:フリーソフトウェアOS](https://ja.wikipedia.org/wiki/Category:フリーソフトウェアOS "wikilink")

1.
2.  [Caldera releases original unices under BSD license](http://slashdot.org/articles/02/01/24/0146248.shtml)
3.  <http://www.nordier.com/v7x86/index.html> main page for UNIX v7/x86
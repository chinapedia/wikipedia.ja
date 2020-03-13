> この記事は[DR-DOS](https://ja.wikipedia.org/wiki/DR-DOS)から翻訳されています。


**DR-DOS** は、[ゲイリー・キルドール](../Page/ゲイリー・キルドール.md "wikilink")率いる[デジタルリサーチ](../Page/デジタルリサーチ.md "wikilink")社が開発した[IBM PC/AT互換機向けの](https://ja.wikipedia.org/wiki/IBM_PC/AT "wikilink")[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink")。[CP/M-86](https://ja.wikipedia.org/wiki/CP/M-86 "wikilink")の後継OSでもある。

## 概要

**DR-DOS**（当時DR DOS）は、当時[デジタルリサーチ](../Page/デジタルリサーチ.md "wikilink")の最新のOSの名前として名づけられた。歴史的にはCP/M-86のMS-DOS互換機能 (DOS Plus) の延長にある。

DR-DOSはCompaqなどで広く使われた[MS-DOS](../Page/MS-DOS.md "wikilink") 3.31と互換性を持つように設計されており、内部的にはバージョン3.3でありながら、[ファイルシステム](../Page/ファイルシステム.md "wikilink")はバージョン4互換となっている。この構造は現在でも維持されており、MS-DOS/PC DOSとの明確な違いとなっている。

また、最初のバージョンから[ROM](https://ja.wikipedia.org/wiki/Read_Only_Memory "wikilink") や [フラッシュメモリ](../Page/フラッシュメモリ.md "wikilink")から起動できることや、バージョン5でタスクスイッチャ、バージョン7で[DPMI](../Page/DPMI.md "wikilink")メモリ管理をともなうプリエンプティブマルチタスクがサポートされている。このように他のDOSと比較して高度な機能を持つことも特徴である。

## 変遷

DR-DOSの販売元および名称には変遷がある。

デジタルリサーチからリリースしていた当時（バージョン3.31～6.0）の正式な販売名称はハイフンなしの**DR DOS**であったが、外部コマンドおよびデジタルリサーチのドキュメントでもDR-DOS、DR DOSの双方が混合していた。

[1991年](../Page/1991年.md "wikilink")デジタルリサーチが[ノベルと合併したのちしばらくはNovell](../Page/ノベル_\(企業\).md "wikilink") DR DOS 6として販売されたが、[1994年](../Page/1994年.md "wikilink")にはバージョン7がNovell DOS 7としてリリースされた。しかしここでもNW-DOSと呼んでいる場合があった。これは一部のコマンドがNW～で始まっているものが多かったためと考えられる。

[1996年](../Page/1996年.md "wikilink")カルデラにDOSの権利が移転し、[1997年](https://ja.wikipedia.org/wiki/1997年 "wikilink")にOpenDOS 7.01としてリリースされた。その後カルデラはバージョン7.02をDR Open DOSとして、バージョン7.03をDR-DOSとしてリリースした。

その後Lineoからリリースした時代は再びDR DOSと呼んでおり、現在のDRDOS,IncでもDR DOSと表記している。

本項では、それぞれの時代の呼称に合わせDR DOS、Novell DOS、OpenDOS、DR-DOSと記述する。

## 現在のバージョン

OpenDOS 7.01がリリースされた際、そのカーネルのソースコードがオープンソースとして公開された。このソースコードを元に、現在でもUdo Kuhnt氏を中心としてDR-DOS/OpenDOS拡張プロジェクト（通称Udo's Patch）として、以下のURLで開発されている。なお、当プロジェクトの成果物はカーネルを中心とするごく一部であり、DOSとして使用するためには、DR DOS 7.03が必要となる[1](http://www.unet.univie.ac.at/~a0503736/php/drdoswiki/index.php?n=Main.FAQ#toc8)。

[The DR-DOS/OpenDOS Enhancement Project](http://www.drdosprojects.de/)

現在、DR DOSの権利はCaldera Thin Clients（後のLineo社）を経てDRDOS, Incへ移転し、組み込みシステム用途として販売されている。2004年3月30日にDRDOS, Incからリリースされた DR DOS 8.0では、[FAT32](https://ja.wikipedia.org/wiki/FAT32 "wikilink")と2GB以上のラージディスクがサポートされている。

DR DOS 8.1は、[2005年](../Page/2005年.md "wikilink")秋にリリースされたが、以下の理由により バージョン7.03に戻している。

## DR DOS 8.1問題

DR DOS 8.1 は、2005 年秋にリリースされたが、その前のバージョンであるDR DOS 8.0とは全く別のものであった。具体的にはCaldera DR-DOS 7.03をベースとしたEnhanced DR-DOSのUdo Kuhnt氏のクレジットなどが書き換えられたバージョンである。

この問題は2005年10月に、DRDOS,IncのDR DOS 8.1のリリースのアプリケーションの一部で[FreeDOS](../Page/FreeDOS.md "wikilink")由来のSYS v2.6とFDXXMS v.92のGPL違反の収録、およびEnhanced DR-DOSなどのフリーソフトウェアやシェアウェアなどの無許可収録があったことから発覚した。

  - [2](http://www.freedos.org/freedos/news/press/2005-drdos.html)
  - [3](http://www.freedos.org/freedos/news/2005.html) FreeDOS
  - [4](http://drdos.at.infoseek.co.jp/news.html) Japanese DR DOS User's Group（日本語、2005-10-29の記事を参照）
  - [5](http://www.drdosprojects.de/) Enhanced DR-DOS/OpenDOS Project

この問題により、DR-DOS 8.1の販売は中止された。

## 関連項目

  - [GEM](https://ja.wikipedia.org/wiki/Graphical_Environment_Manager "wikilink")･･･DR-DOS向け[GUI](https://ja.wikipedia.org/wiki/GUI "wikilink")環境。
  - [DR-WebSpyder](https://ja.wikipedia.org/wiki/DR-WebSpyder "wikilink")･･･DR-DOS向け[ウェブブラウザ](../Page/ウェブブラウザ.md "wikilink")。
  - [DR-DRAW](https://ja.wikipedia.org/wiki/DR-DRAW "wikilink")
  - [ViewMAX](https://ja.wikipedia.org/wiki/ViewMAX "wikilink")

## 外部リンク

  - [DRDOS, Inc](http://www.drdos.com/)
  - [amulet open source solutions（CD-ROM版入手先）](https://ssl.amulet.co.jp/shop/price_list.php?cate=SOFT)

<!-- end list -->

  - [Unofficial DR-DOS Resources: Kernel 7.04/7.05](http://www.drdos.net/err705.htm)
  - [Enhanced DR-DOS/OpenDOS Project](http://www.drdosprojects.de/)
  - [Enhanced DR-DOS Forum](http://www.drdosprojects.de/forum/drp_forum/)
  - [Dr-DOS Wiki](http://www.drdos.org)
  - [Old Os](http://www.oldos.org/) — Information and downloads for DR-DOS users.
  - [日本DR DOSユーザー会](http://ifs.nog.cc/drdos.at.infoseek.co.jp/)
  - [DR-DOSによるDOS/V環境の構築](http://euc.jp/os/drdosv.ja.html)
  - [起動ディスクの作成 －その他の方法（DR-DOSシステムディスクを作る）](http://signalshonan.ddo.jp/modules/hint/index.php?content_id=2)

[Category:DR-DOS](https://ja.wikipedia.org/wiki/Category:DR-DOS "wikilink") [Category:デジタルリサーチ](https://ja.wikipedia.org/wiki/Category:デジタルリサーチ "wikilink")
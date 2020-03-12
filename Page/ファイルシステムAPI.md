> この記事は[API](https://ja.wikipedia.org/wiki/API)から翻訳されています。


**ファイルシステムAPI**とは、開発者が[ファイルシステム](../Page/ファイルシステム.md "wikilink")を[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink") (OS)に移植する際の[APIであり](../Page/アプリケーションプログラミングインタフェース.md "wikilink")、オペレーティングシステムはそのファイルシステムについて何も知らなくてもよいように設計されている。

これは[ドライバAPIの機能と似ており](../Page/デバイスドライバ.md "wikilink")、ユーザープログラムやOS自身はそのファイルシステムについて何も知らなくてもよい。

ファイルシステムAPIには一般的な保守機能（新しいファイルシステムの作成、メタデータの一貫性のチェック、デフラグなど）へのインターフェイスを提供するものもあり、それらを実際に行うアプリケーションが新たなファイルシステムも透過的に扱えるようになっている。

## 歴史

本来、OSには一種類のディスクファイルシステムしかなかった。しかし、以下のような問題がシステムの発展に伴って発生してきた。

  - ネットワークが普及するにつれて、[分散ファイルシステム](../Page/分散ファイルシステム.md "wikilink")が各OSで必要とされるようになった。
  - 異なるOS間でファイルを交換する必要性が増してきた。

古い手法では、全ファイルシステムとネットワークプロトコルはOSの[カーネル](../Page/カーネル.md "wikilink")内の固有機能であり、ファイルへのアクセスはローカルであれリモートであれ全てカーネル内で処理されていた。

この手法では、新たなファイルシステムのサポートはカーネルの大幅な改造を意味する。これは効率が悪いので、OS設計者はファイルシステムのコードをカーネル内のファイル操作やネットワーク処理のコードから分離するようにした。これがファイルシステムAPIである。

## カーネル型API

カーネルがファイルシステム開発者向けAPIを提供するだけでなく、ファイルシステム自身が[カーネル空間に置かれる場合に](https://ja.wikipedia.org/wiki/アドレス空間#カーネル空間 "wikilink")「カーネル型API」と呼ぶ。

従来の手法ではファイルシステムのコードはカーネル内の各コードと複雑に絡み合っていたが、カーネル型のファイルシステムAPIではファイルシステムがカーネルに提供すべきインターフェイスとカーネルがファイルシステムに提供するインターフェイスが明確化されている。

これは、最もきれいな手法とは言えないが、従来の手法の持っていた欠点を解決している。

モジュール化されたカーネルでは、ファイルシステムも他のモジュールのように追加可能なモジュールとして扱われる（つまり、APIだけでなく[Application Binary Interfaceも規定されて](../Page/Application_Binary_Interface.md "wikilink")、オブジェクトファイルの形で追加することが可能）。モジュール化されていないカーネルではファイルシステムのコードを追加したときにはカーネルの再コンパイルが必要である（従って、ソースの公開されていないOSでは、OS開発業者がOEM供給を受けてファイルシステムを追加することになる）。

[Linux](../Page/Linux.md "wikilink")を含めた[UNIX](../Page/UNIX.md "wikilink")系システムはこの手法を採用している。

[MS-DOS](../Page/MS-DOS.md "wikilink")(4.0以降）と互換OSでは、同様の手法でCD-ROMやネットワークファイルシステムをサポートしていた。カーネルにコードを追加するのではなく、カーネルの機能を利用したカーネル型APIである。ファイル関連のコールを全て捉えて、必要に応じて特定のファイルシステムドライバを呼び出し、ファイルシステムドライバは低レベルな[BIOS機能を使って直接ディスクにアクセスしていた](https://ja.wikipedia.org/wiki/Basic_Input/Output_System "wikilink")。

## ドライバ型API

カーネルが必要なAPIを提供するが、ファイルシステムが完全に[ユーザ空間にある場合](https://ja.wikipedia.org/wiki/アドレス空間#ユーザ空間 "wikilink")、これをドライバ型APIと呼ぶ。

ファイルシステムのコードが独立しているので、これはよりきれいな手法と言える。この手法ではソースの公開されていないOSにも対応できるし、オンラインでファイルシステムの追加・削除が可能となる。

この手法の例として、[Windows NTと](https://ja.wikipedia.org/wiki/Windows_NT "wikilink")[OS/2](https://ja.wikipedia.org/wiki/OS/2 "wikilink")それぞれの[IFSがある](https://ja.wikipedia.org/wiki/Installable_File_System "wikilink")。

## カーネル・ドライバ混合API

このAPIは、ファイルシステムがカーネル内にあるものの、実際にはそのファイルシステムを使わずにドライバ型APIの別のファイルシステムを使用するものである。この手法は[VFATとして](https://ja.wikipedia.org/wiki/File_Allocation_Table#VFAT "wikilink")[Windows 3.11以降の](https://ja.wikipedia.org/wiki/Microsoft_Windows_3.1 "wikilink")[Windows 9x系で使われたものである](../Page/Windows_9x系.md "wikilink")。

しかし、このAPIは完全な文書が存在せず、サードパーティはこのインターフェイスを使用したファイルシステム開発に非常に苦労したという。

## ユーザーランド型API

このAPIはカーネルが特にファイルシステムのために用意したわけではない機能（一般のユーティリティなどがディスクアクセスに使用するライブラリ）でファイルシステムを構築するものを指す。

これは様々なディスクイメージを処理する手法として有効である。

この手法の大きな利点は、利用するインターフェイスが標準的なライブラリだけであれば、多くのOSに簡単に移植できる点である。欠点は特にこのタイプのAPIが規定されていないので、ファイルシステム作成者によって使うAPIが全く異なる点である。

この手法の例として、[HFS](https://ja.wikipedia.org/wiki/HFS "wikilink")を[Mac OS以外でもアクセスできるようにした](https://ja.wikipedia.org/wiki/Mac_OS "wikilink") [hfsutils](http://www.mars.org/home/rob/proj/hfs/) がある。

## ファイルシステムAPI間の相互運用性

全てのファイルシステムはカーネルから同等の機能を提供されるので、違った型のAPIであっても、ファイルシステムをあるAPIから別のAPIに移植するのは可能である。

例えば、OS/2に移植された ext2ドライバは、Linux の VFS から OS/2 の IFS へのラッパーであり、ファイルシステム自体はLinuxのカーネル型のものである。OS/2のHFSドライバは上述のhfsutilsをOS/2のIFSに移植したものである。

## 関連項目

  - [ファイルシステム](../Page/ファイルシステム.md "wikilink")
  - [仮想ファイルシステム](../Page/仮想ファイルシステム.md "wikilink")
      - Virtual File System - [UNIX](../Page/UNIX.md "wikilink")系システムのファイルシステムAPI
      - Installable File System - [OS/2](https://ja.wikipedia.org/wiki/OS/2 "wikilink")および[Windows NT系でのファイルシステムAPI](../Page/Windows_NT系.md "wikilink")
  - [拡張子](../Page/拡張子.md "wikilink")

## 外部リンク

  - [Linux 2.4 VFS](https://linuxjf.osdn.jp/JFdocs/Linux-Kernel-Internals-3.html)
  - [マイクロソフトのIFSキット](http://www.microsoft.com/japan/whdc/DevTools/IFSKit/default.mspx)

[Category:プログラミング](https://ja.wikipedia.org/wiki/Category:プログラミング "wikilink") [Category:OSのファイルシステム](https://ja.wikipedia.org/wiki/Category:OSのファイルシステム "wikilink") [Category:API](https://ja.wikipedia.org/wiki/Category:API "wikilink")
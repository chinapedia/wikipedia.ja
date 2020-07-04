> この記事は[Hierarchical File System](https://ja.wikipedia.org/wiki/Hierarchical_File_System)から翻訳されています。


**HFS** (**Hierarchical File System**) とは、[Mac OSでかつて使われていた](https://ja.wikipedia.org/wiki/Mac_OS "wikilink")[ファイルシステム](../Page/ファイルシステム.md "wikilink")のひとつである。日本ではしばしば「**Mac OS 標準フォーマット**」ともいう。

HFSは二つの[フォークを持つ](https://ja.wikipedia.org/wiki/フォーク_\(ファイルシステム\) "wikilink")。すなわち、主データ（[データフォークと呼ばれる](../Page/リソースフォーク.md "wikilink")）の他に[リソースフォーク](../Page/リソースフォーク.md "wikilink")という[メタ情報を持つことで知られている](../Page/メタデータ.md "wikilink")。また大文字と小文字の区別をしない。

HFSはファイルシステムの中では比較的新しい部類に入り、把握しやすいボリュームの扱いや、[シンボリックリンク](https://ja.wikipedia.org/wiki/シンボリックリンク "wikilink")・[ショートカット](https://ja.wikipedia.org/wiki/ショートカット "wikilink")より先進的な[エイリアス](../Page/エイリアス.md "wikilink")機構を備えるなど、設計上優れた部分も多い。

ブロックサイズ（管理単位）は、ボリュームサイズ32MiBまで512バイト、以降32MiB毎に512バイトずつ増加し（64MiBを超えたサイズでは、[FATファイルシステムのようにいきなり倍になることはない](../Page/File_Allocation_Table.md "wikilink")）、225〜256MiBで[HFS+と同じ](../Page/HFS_Plus.md "wikilink")4KiBになる。2GiB（System 7.1.x(他国語版を含む 以下同様)までの上限）で32KiB、4GiB（System 7.5 7.5.1での上限）で64KiB、2TiB（System 7.5.2以降での上限）では32MiBになる。

このファイルシステムで記録されたストレージの読み書きが可能なのは[Classic Mac OSおよび](../Page/Classic_Mac_OS.md "wikilink")[Mac OS X v10.5までの](../Page/Mac_OS_X_v10.5.md "wikilink")[macOS](https://ja.wikipedia.org/wiki/macOS "wikilink")のみである。

[Mac OS X v10.6からは](../Page/Mac_OS_X_v10.6.md "wikilink")、標準フォーマットはHFS+に置き換えられ、起動ディスクにHFSは利用出来なくなった。

[macOS Sierraにて](https://ja.wikipedia.org/wiki/macOS_Sierra "wikilink")、サポートが終了し、完全に利用が出来なくなった\[1\]。

## HFSの歴史

HFSは初期[Macintosh](../Page/Macintosh.md "wikilink")で使用されていた[Macintosh File System](https://ja.wikipedia.org/wiki/Macintosh_File_System "wikilink") (MFS) の改良版で、[1985年](https://ja.wikipedia.org/wiki/1985年 "wikilink")[9月](../Page/9月.md "wikilink")に発表され、Systemバージョン3.1より実装された。MFSはフラットなファイルシステムであり、フォルダは[Finder](../Page/Finder.md "wikilink")レベルでエミュレートされていた。そのため、アプリケーションからはすべてのファイルが同一階層に見え、ファイル数が少ない[フロッピーディスク](../Page/フロッピーディスク.md "wikilink")ではあまり問題にならないものの、[ハードディスクで使用し](https://ja.wikipedia.org/wiki/ハードディスクドライブ "wikilink")、アプリケーションから扱うファイル数が増えるにつれ不便なものとなってきていた。その上、約100ファイルを越えると非常に不安定になった。Hierarchicalとはファイルシステムレベルでの[フォルダ](https://ja.wikipedia.org/wiki/フォルダ "wikilink")による[階層構造](../Page/階層構造.md "wikilink")がサポートされたことに由来する。

1998年、[HFS+](https://ja.wikipedia.org/wiki/HFS+ "wikilink")がMac OS 8.1で導入され、HFSの後継となった。Mac OS X v10.5まではHFSを起動ディスクとして利用できないが、読み書きはHFS+同様に可能である。Mac OS X v10.6以降ではHFSは読み込みのみ可能で、起動のみならず書き込みやボリューム作成もできなくなった。

2016年、macOS Sierraで、サポート終了。

## 出典

<references />

## 関連項目

  - [APFS](https://ja.wikipedia.org/wiki/Apple_File_System "wikilink")
  - [HFS Plus](../Page/HFS_Plus.md "wikilink")
  - [Xsan](../Page/Xsan.md "wikilink")

## 外部リンク

  - [HFS仕様書](https://developer.apple.com/legacy/library/documentation/mac/Files/Files-99.html)

[de:Dateisystem\#Hierarchische Dateisysteme](https://ja.wikipedia.org/wiki/de:Dateisystem#Hierarchische_Dateisysteme "wikilink")

[Category:OSのファイルシステム](https://ja.wikipedia.org/wiki/Category:OSのファイルシステム "wikilink") [Category:Mac_OS](https://ja.wikipedia.org/wiki/Category:Mac_OS "wikilink")

1.  [What's new in OS X - OS X v10.12](https://developer.apple.com/library/prerelease/content/releasenotes/MacOSX/WhatsNewInOSX/Articles/OSXv10.html#//apple_ref/doc/uid/TP40017145-SW1)*The HFS Standard filesystem is no longer supported.*
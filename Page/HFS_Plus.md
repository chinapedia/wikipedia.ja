> この記事は[HFS Plus](https://ja.wikipedia.org/wiki/HFS_Plus)から翻訳されています。


**HFS+**（Hierarchical File System Plus）または**Mac OS拡張フォーマット**は、[HFSから置き換わる](../Page/Hierarchical_File_System.md "wikilink")[Classic Mac OS及び](../Page/Classic_Mac_OS.md "wikilink")[macOS](https://ja.wikipedia.org/wiki/macOS "wikilink")で利用される主要な[ファイルシステム](../Page/ファイルシステム.md "wikilink")である。このファイルシステムは[iPod](https://ja.wikipedia.org/wiki/iPod "wikilink")でも使用される。開発中、アップルはこのファイルシステムを "Sequoia" と名付けていた\[1\]。

## 概要

これまでMacintoshに採用されてきたHFSは、[フロッピーディスク](../Page/フロッピーディスク.md "wikilink")で利用されていた頃は大きな問題ではなかったが、大きなストレージデバイスが増え、巨大なサイズのファイルを扱うようになるにつれて深刻な問題へとなっていった。

HFS+の大きな改善点は、ブロックサイズが4KB固定になり、以前より大量のファイルを扱えるようになったこと、巨大なサイズのファイルをサポートするようになったこと、ファイル名にUnicodeを利用すること、長いファイル名が付けられるようになったことである。

また、HFSのマルチフォークシステムを拡張し、多くの[フォークの利用もできるようになった](https://ja.wikipedia.org/wiki/フォーク_\(ファイルシステム\) "wikilink")。このマルチフォークは現在、[拡張属性](https://ja.wikipedia.org/wiki/拡張ファイル属性 "wikilink") (EA) の保存のために利用されている。

HFS+の登場により、巨大なファイル容量を扱う機会が多いプロの映像制作や音楽制作の現場では圧倒的に支持されるようになり、プロのエンジニアやクリエイターがMacを導入するきっかけとなった。

## HFS+の歴史

HFS+は[1998年](https://ja.wikipedia.org/wiki/1998年 "wikilink")[1月19日](../Page/1月19日.md "wikilink")、Mac OS 8.1のリリースで導入された\[2\]。もともとは[Copland](../Page/Copland.md "wikilink")を想定して開発された技術であり、その存在はCopland開発中から知られていた。

アップルは、2002年11月11日の[Mac OS X v10.2のアップデートのリリース](../Page/Mac_OS_X_v10.2.md "wikilink")10.2.2で、データ信頼性を高める[ジャーナリングファイルシステム](../Page/ジャーナリングファイルシステム.md "wikilink")機能をHFS+に加えた。

[Mac OS X v10.3ではファイルシステムの扱いが大幅に拡張された](../Page/Mac_OS_X_v10.3.md "wikilink")。ファイルにメタデータ部が追加され、頻繁にアクセスされるファイルをドライブの外周のアクセスの高速な領域に自動的に移動し、同時に断片化を解消するHot File Adaptive Clusteringを組み込んだ。**HFSX**と呼ばれる拡張バージョンのHFS+も導入した。HFSXはディレクトリとファイルの名前の扱いについて変更があった\[3\]。

[Mac OS X v10.4では以前利用していたUNIXパーミッションのほかに](../Page/Mac_OS_X_v10.4.md "wikilink")、[Windows XP及び](../Page/Microsoft_Windows_XP.md "wikilink")[Windows Server 2003の](../Page/Microsoft_Windows_Server_2003.md "wikilink")[ACLと互換性のあるACLのサポートを追加した](../Page/アクセス制御リスト.md "wikilink")。また、将来のリリース向けに予約されていた拡張属性 (extended attribute) のサポートも加えた。

## 他のオペレーティングシステム

### Microsoft Windows

  - [Windowsで読み取りのみ可能](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")
      - [Boot CampのHFS](../Page/Boot_Camp.md "wikilink")+ドライバ…OS X 10.6以降の[Boot Campで提供されている](../Page/Boot_Camp.md "wikilink")。
      - [HFSExplorer](https://ja.wikipedia.org/wiki/HFSExplorer "wikilink")…HFS+ボリュームを読み、ファイルをコピーできる。GPLライセンス。
      - [jHFSplus](https://ja.wikipedia.org/wiki/jHFSplus "wikilink")…HFS+ボリュームをフォルダとしてマウントできる。
  - Windowsで読み書き可能
      - [MacDrive](https://ja.wikipedia.org/wiki/MacDrive "wikilink")…読み書き可能な商用ユーティリティ。

### FreeBSD

[FreeBSD](../Page/FreeBSD.md "wikilink")では5.3-RELEASE以降でマウントできる。

### Linux

[Linux](../Page/Linux.md "wikilink")ではカーネル2.4.22以降でマウントできる。

### Xbox 360

[Xbox 360ではHFS](../Page/Xbox_360.md "wikilink")+でフォーマットされたiPodを読めるマイクロソフト製ドライバを搭載している。

## 関連項目

  - [APFS](https://ja.wikipedia.org/wiki/Apple_File_System "wikilink")
  - [HFS](../Page/Hierarchical_File_System.md "wikilink")
  - [Xsan](../Page/Xsan.md "wikilink")

## 脚注

<references />

## 外部リンク

  - [Mac OS 8, 9: Mac OS 拡張フォーマット - ボリュームとファイルの上限](http://docs.info.apple.com/article.html?artnum=24601-ja)
  - [Mac OS X: Mac OS 拡張 (HFS Plus) フォーマット - ボリュームとファイルの上限](http://docs.info.apple.com/jarticle.html?artnum=25557-ja)

[Category:OSのファイルシステム](https://ja.wikipedia.org/wiki/Category:OSのファイルシステム "wikilink") [Category:Mac_OS](https://ja.wikipedia.org/wiki/Category:Mac_OS "wikilink")

1.
2.
3.  [HFS Plus Volume Format HFSX](http://developer.apple.com/mac/library/technotes/tn/tn1150.html#HFSX)
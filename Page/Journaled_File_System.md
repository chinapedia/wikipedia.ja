> この記事は[Journaled File System](https://ja.wikipedia.org/wiki/Journaled_File_System)から翻訳されています。


**JFS** (Journaled File System) は、[IBM](../Page/IBM.md "wikilink") が同社の商用 [UNIX](../Page/UNIX.md "wikilink") である [AIX](../Page/AIX.md "wikilink") v3.1 に実装した 64ビット[ジャーナリングファイルシステム](../Page/ジャーナリングファイルシステム.md "wikilink")である。 [OS/2](https://ja.wikipedia.org/wiki/OS/2_Warp "wikilink")、[eComStation](https://ja.wikipedia.org/wiki/eComStation "wikilink") にも実装され、その後[オープンソース](../Page/オープンソース.md "wikilink")として公開、[Linux](../Page/Linux.md "wikilink") に移植されている。[HP-UX](../Page/HP-UX.md "wikilink") にも JFS という名称のファイルシステムがあるが、これは [VxFS](https://ja.wikipedia.org/wiki/VxFS "wikilink") の [OEM](../Page/OEM.md "wikilink") である。

AIX の JFS には *JFS*（*JFS1*）、*JFS2* と呼ばれる2つの世代の JFS がある。\[1\]\[2\]他の [OS](../Page/オペレーティングシステム.md "wikilink") では第2世代の JFS が実装され単に *JFS* と呼ばれている。\[3\] *JFS in AIX*と呼ばれるものは、JFS1を指す。

## 歴史

1990年2月 IBM は AIX 3.1 向けに JFS をリリースした（現在 *JFS1 on AIX* と呼ばれているもの）。JFS はその後10年間 AIX のメインのファイルシステムとして多数の AIX システム内で用いられた。JFS1 は AIX のメモリ管理と深く結びついている。こうした設計は[プロプライエタリの](../Page/プロプライエタリ・ソフトウェア.md "wikilink") OS でよく見られるものであり、ファイルシステムが一つの OS だけでサポートされる典型例である。

1995年、マルチプロセッサのサポートと性能向上、複数の OS で使用可能な移植性の高いファイルシステムにするための改良が始まる。1999年4月、新しい JFS が [OS/2 Warp Server for e-business](https://ja.wikipedia.org/wiki/OS/2 "wikilink") に、2000年10月には OS/2 Warp クライアントに向けてリリースされた。

1999年12月、OS/2 の JFS ソースコードがオープンソースコミュニティに提供され、それを受け JFS の [Linux](../Page/Linux.md "wikilink") への移植が始まった。2001年6月、*JFS for Linux* の最初の安定版がリリースされた。\[4\]この活動と平行して1997年、 JFS 開発チームの数名が AIX OS の開発チームに戻り、新しい JFS を AIX に移植する作業を始めた。2001年5月、改良された *JFS（JFS2）* は AIX 5L で利用可能となった。\[5\]\[6\]

2008年初頭、JFS のメンテナンスに IBM は関心が無いので、商用環境では用いるべきでないという噂が流れた。\[7\] これに対し IBM の Linux テクノロジーセンターのメンバーであり *JFS コアチーム*のメンバーでもある Dave Kleikamp は、彼らはJFSについて Linux カーネルの変更に追従し、潜在するバグを直そうとしており、いくつかのディストリビューションはさらなるコミットメントを彼らに期待していると説明した。\[8\]

## 特徴

JFS は以下の特徴を持つ。\[9\]\[10\]

### ジャーナリング

JFS は最初期からジャーナリングファイルシステムとして実装されている。ジャーナルデータは最大で 128MiB を持つ。JFS のジャーナリングは [inode](https://ja.wikipedia.org/wiki/inode "wikilink") の一部をジャーナルする点で [XFS](../Page/XFS.md "wikilink") に類似する。JFS はメタデータのみをジャーナル保護するため、クラッシュ後ユーザーデータの整合性は保証しない。

### B+木

ディレクトリ参照の高速化のために[B+木](../Page/B+木.md "wikilink")を使用している。エントリをB+木に移動するまでに、ディレクトリiノード内にディレクトリエントリ8個を格納できる。エクステントについてもB+木でインデックス化している。

### 動的Inode割り当て

JFS は [inode](https://ja.wikipedia.org/wiki/inode "wikilink") を保存するディスクスペースと inode の数をファイルシステム作成時に静的に割り当てるのではなく必要に応じて動的に割り当てている。個々の inode は512バイトの大きさを持ち、16KBの1エクステントに32個の inode を割り当てられる。

### エクステント

JFS ディスク割り当てにを使用している。エクステントは可変長のブロック管理により連続したブロック割り当てを少ないメタデータで管理できる。エクステントは複数のアロケーショングループに跨って割り当てられる場合があり、エクステントの配置検索の性能向上のため、エクステントはB+木にインデックス化される。

### 圧縮

AIX の JFS1 のみ [LZ77](https://ja.wikipedia.org/wiki/LZ77 "wikilink") による圧縮をサポートしている。CPU使用率の増加や断片化の増加を理由に、シングルユーザーでの使用やオフラインバックアップ以外での使用は推奨されていない。\[11\]\[12\]

### コンカレントI/O

コンカレントI/O (CIO) は、ファイルの書き込みロックを緩和するオプションである。JFSのファイルロックは通常、読み込みは共有ロック、書き込みは排他ロックのため、ファイルレベルでの一貫性は保てるが書き込みは直列化される。そのため、一貫性をアプリケーションレベルで管理するRDB等のアプリケーションでJFSを利用する場合、CIOオプションを利用することでロックによるオーバーヘッドを削減できる。\[13\]

### アロケーショングループ

アロケーショングループ (AG) は、アグリゲート(複数のディスク領域からなる集合体)を分割する単位である。JFSはAGに対しリソースアロケーションポリシーを適用し、I/O性能の向上に利用する。

リソースアロケーションポリシーは、1つはディスクブロックを分割し、ファイルのディスクiノードを同じAGに所属させようとするポリシー、もう1つは関連のないデータを同じAGに割り当てるポリシーである。ファイルが開かれている時、JFSはそのファイルが所属するAGをロックし、そのファイルが大きくなることのみを許可する。これにより、単にファイルにAGへの書き込みを許可するのみよりも、ファイルのフラグメンテーションを抑える。

### JFS スーパーブロック

スーパーブロックはファイルシステム全体に関する情報を保持し、次のフィールドを含む。

  - ファイルシステムのサイズ
  - ファイルシステムに含まれるブロック数
  - ファイルシステムの状態
  - アロケーショングループのサイズ
  - ファイルシステムのブロックサイズ

## Linuxでの利用

カーネルバージョン2.4.18pre9-ac4以降のカーネルモジュールと、ユーザランドのファイルシステムメンテナンスツール(JFSutils)によってサポートされ、著名な Linux ディストリビューションで利用できる。

ベンチマークでは、様々な負荷や使用パターン、ファイルの大小に関わらず一貫して安定した性能と信頼性を示し、高負荷下においてもCPU使用率は低く、利用可能なシステムリソースが残る程度とされる。

*JFS for Linux* プロジェクトは *JFS コアチーム* \[14\] によってメンテナンスされている。

## 脚注

## 外部リンク

  - [JFS for Linux project website](http://jfs.sourceforge.net/)
  - [JFS1 File System Layout](http://publib.boulder.ibm.com/infocenter/pseries/v5r3/topic/com.ibm.aix.genprogc/doc/genprogc/fsyslayout.htm), IBM.
  - [JFS2 File System Layout](http://publib.boulder.ibm.com/infocenter/pseries/v5r3/topic/com.ibm.aix.genprogc/doc/genprogc/fsyslayout2.htm), IBM.
  - [JFSRec](http://jfsrec.sourceforge.net/), a console program that performs a read only extraction of files and directories from a damaged JFS filesystem

[Category:Linuxのファイルシステム](https://ja.wikipedia.org/wiki/Category:Linuxのファイルシステム "wikilink") [Category:UNIX](https://ja.wikipedia.org/wiki/Category:UNIX "wikilink") [Category:1990年のソフトウェア](https://ja.wikipedia.org/wiki/Category:1990年のソフトウェア "wikilink")

1.
2.
3.
4.
5.
6.
7.  [Re: which to use: ext3, JFS, XFS, ReiserFS?](http://linux.derkeiler.com/Mailing-Lists/Debian/2008-01/msg01808.html)
8.  [SourceForge.net: jfs-discussion](http://sourceforge.net/mailarchive/forum.php?thread_name=fpps5p%24g2t%242%40saturn.local.net&forum_name=jfs-discussion)
9.
10.
11.
12.
13. [Improving Database Performance With AIX Concurrent I/O - White Paper](http://www.ibm.com/servers/aix/whitepapers/db_perf_aix.pdf)
14. [JFS for Linux project website](http://jfs.sourceforge.net/)
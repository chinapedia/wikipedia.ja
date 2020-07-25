> この記事は[Unix File System](https://ja.wikipedia.org/wiki/Unix_File_System)から翻訳されています。


**Unix File System**（**UFS**）とは、[Unix系](../Page/Unix系.md "wikilink")[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink") (OS) において使用される[ファイルシステム](../Page/ファイルシステム.md "wikilink")である。

また固有のファイルシステムを指す言葉ではなく、[Version 7 Unix](../Page/Version_7_Unix.md "wikilink") のファイルシステムおよびそこから派生した一連のファイルシステムの総称である。 一般にUFSと呼ぶ場合は4.2[BSD](../Page/BSD.md "wikilink")で実装された **Fast File System** (**FFS**) のことを指す場合が多く、他にはFFFS、UFS2、UFS Logging等が存在する。

## 設計

UFSボリュームは以下の部分から構成される。

  - [パーティション](../Page/パーティション.md "wikilink")の先頭数ブロックは[ブート](../Page/ブート.md "wikilink")ブロックとして予約されている（ファイルシステムとは別に初期化する必要がある）。
  - UFSであることを示す[マジックナンバーやファイルシステムの構成を示す基本的な値や統計情報やチューニングパラメータを含むスーパーブロック](https://ja.wikipedia.org/wiki/マジックナンバー_\(フォーマット識別子\) "wikilink")。
  - シリンダグループの集合体。各シリンダグループには以下のような構成要素がある。
      - スーパーブロックのバックアップコピー
      - シリンダグループのヘッダ。そのシリンダグループの統計情報、フリーリストなど、スーパーブロックに似た情報がある。
      - [inode](https://ja.wikipedia.org/wiki/inode "wikilink")群。それぞれにファイル属性情報が格納されている。
      - [データブロック群](../Page/ブロック_\(データ\).md "wikilink")。

inode は順に番号を振られている。ルート[ディレクトリ](../Page/ディレクトリ.md "wikilink")の inode の後の何個かの inode は歴史的理由により予約されている。

ディレクトリファイルは、そのディレクトリにあるファイルのファイル名と対応する inode 番号だけを格納している。ファイルについての全ての[メタデータ](../Page/メタデータ.md "wikilink")は inode にある。

## 背景

初期のUNIXで使っていたファイルシステムは、単に *FS* と呼ばれていた。FS にはブートブロック、スーパーブロック、inode群、データブロック群だけが存在していた。初期のUNIXで使っていた小さいディスクではこれで十分であったが、技術の進歩と共にディスク容量が大きくなり、inodeのある部分とデータブロックの間をヘッドが行き来することによる効率の激しい低下が無視できなくなってきた。BSDではこれを最適化した FFS (Fast File System) を導入した。これは、シリンダグループという概念を発明したもので、ディスクを小さい部分に分け、それぞれにinodeとデータブロックを配置する構成である。

BSD FFS は、データブロックとそれに関連するメタデータを同じシリンダグループに配置することでアクセスを局所化しようとしたものであり、理想的には1つのディレクトリのコンテンツが（データブロックも対応するメタデータも）同じか近いシリンダグループに配置され、ディレクトリのコンテンツがディスク全体に分散配置されることによる[フラグメンテーション](../Page/フラグメンテーション.md "wikilink")を低減する。

スーパーブロックには性能に関わるパラメータとして、トラック数、[セクタ数](https://ja.wikipedia.org/wiki/ディスクセクタ "wikilink")、回転速度、ヘッド速度、トラック間のセクタ配置などの情報がある。完全に最適化されたシステムでは、プラッタの回転を待つ間に近接するトラック間でヘッドを移動させ、不連続に配置されているセクタを読むことができる。

ディスク容量が大きくなると、セクタレベルの最適化は効果を発揮できなくなってきた（特に、トラック当たりのセクタ数が一定でない場合）。ディスクが大容量化しファイルが巨大化すると、読み込みが断片化することがさらに大きな問題となってきた。これに対してBSDは当初、ファイルシステムのブロックサイズを1セクタから1Kに増やし(4.0BSD)、FFS ではそれをさらに 8K に増やした。これにはいくつかの効果がある。ファイルのセクタが連続確保される可能性が大きくなる。ファイルのブロックをリストで保持するオーバーヘッドを低減できる。ブロック数を保持するビットフィールドで表現できるファイルサイズ上限が大きくなる。

ブロックサイズが大きくなると、小さいファイルがたくさんある場合は領域を無駄に消費することになる。そこでBSDではブロックレベルのフラグメント化を導入した。ファイルの最後の部分はブロックサイズ未満になるので、それをブロックを分割したサブブロックに格納することで領域を有効活用できるようにする。これをブロックのサブアロケーション、テールマージ、テールパッキングなどとも呼ぶ。

## 実装

[SunOS](../Page/SunOS.md "wikilink")/[Solaris](../Page/Solaris.md "wikilink")、[SVR4](../Page/UNIX_System_V.md "wikilink")、[UP-UX](../Page/UP-UX.md "wikilink")、[Tru64 UNIX](../Page/Tru64_UNIX.md "wikilink") などの商用UNIXではUFSを導入した。その多くは独自の拡張を施したため、別のベンダーのUFSを認識することができない。しかし、元のブロックサイズやデータフィールド幅は保持されていることが多く、ある程度の互換性は保持されている。しかし、ディスクを異機種間で共有する場合、事前に互換性を確認することが重要である。

[サン・マイクロシステムズ](../Page/サン・マイクロシステムズ.md "wikilink")は Solaris 7 でUFSに[ジャーナリングファイルシステム](../Page/ジャーナリングファイルシステム.md "wikilink")の機能を追加した UFS Logging を導入した。Solaris UFS には他にも巨大ファイルを扱うための拡張、巨大ディスクを扱うための拡張など様々な拡張がなされている。

[カーク・マキュージックは](../Page/マーシャル・カーク・マキュージック.md "wikilink") FreeBSD の FFS 層と UFS 層を拡張し、UFS2 を開発した。これは64ビットのブロックポインタを追加し（ボリュームの最大を 8 [ゼタバイト](https://ja.wikipedia.org/wiki/ゼタバイト "wikilink")に拡大）、ブロックサイズを可変化し、フラグフィールドを拡張し、'birthtime' という[タイムスタンプ](https://ja.wikipedia.org/wiki/タイムスタンプ "wikilink")を新たに追加するなどの拡張をしたものである。FreeBSD 5.0 では UFS2 がデフォルトとなった。FreeBSD ではさらに [soft updates](https://ja.wikipedia.org/wiki/soft_updates "wikilink") とUFS1およびUFS2両方での[スナップショット機能を導入している](../Page/スナップショット_\(ファイルシステム\).md "wikilink")。これらは NetBSD にも移植された。OpenBSD では、2.9 から soft updates をサポートし\[1\]、4.2 から UFS2 をサポートしている\[2\]。

4.4BSD と [FreeBSD](../Page/FreeBSD.md "wikilink")、[NetBSD](../Page/NetBSD.md "wikilink")、[OpenBSD](../Page/OpenBSD.md "wikilink")、[DragonFly BSD](../Page/DragonFly_BSD.md "wikilink") などの[BSD系システムでは](../Page/BSDの子孫.md "wikilink")、UFS1 と UFS2 の実装は2つの層に分かれている。上位層はディレクトリ構造と inode 構造内のメタデータ（パーミッション、所有者情報など）を扱い、下位層は inode として実装されているデータコンテナを扱う。これは従来からのFFSと[LFSという](https://ja.wikipedia.org/wiki/Log-structured_File_System "wikilink")[ログ構造ファイルシステム](https://ja.wikipedia.org/wiki/ログ構造ファイルシステム "wikilink")で共通部分を共有するための仕組みである。上位層を "UFS" と呼び、下位層を "FFS" または "LFS" と呼ぶ。この場合、下位層にFFSを使っている場合は全体を FFS と呼び、下位層に LFS を使っている場合は全体を LFS と呼ぶことがある。

[Linux](../Page/Linux.md "wikilink")でもBSDなどとの互換性のためにUFSを実装しているが、UFSには共通の標準実装があるわけではないので、Linux がサポートしているのは読み込みが中心であり、書き込みは完全サポートしていない。Linux の [ext2](https://ja.wikipedia.org/wiki/ext2 "wikilink") ファイルシステムは UFS の影響を受けている（実際、4.4BSDから派生した一部のシステムでは、UFSを上位層とし、ext2 をFFSやLFSなどのように下位層として使えるものもある）。

[NeXTStep](../Page/NEXTSTEP.md "wikilink") もBSDから派生しているため、UFS を使っていた。それより派生した[アップルの](../Page/アップル_\(企業\).md "wikilink") [macOS](https://ja.wikipedia.org/wiki/macOS "wikilink") では、[HFS+の代替として](../Page/HFS_Plus.md "wikilink") UFS を使うこともできたが、[Mac OS X v10.5](../Page/Mac_OS_X_v10.5.md "wikilink") 以降では UFS でフォーマットされたボリュームにインストールできなくなった。また、UFS ボリュームにインストールされたv10.5より前のバージョンの macOS をv10.5以降のバージョンにアップグレードすることもできなくなった。\[3\]。

## 脚注

## 参考文献

  -
  -
  -
  -
  -
  -
  - The Linux Documentation Project, [Filesystems HOWTO: FFS](http://www.tldp.org/HOWTO/Filesystems-HOWTO-9.html#ffs). なお、このサイトでのFFSとUFSの区別の仕方は間違っている。

  - [Little UFS2 FAQ: What is the difference between UFS and FFS?](http://sixshooter.v6.thrupoint.net/jeroen/faq.html#UFS-DIFF-FFS) ここでの FFS と UFS の定義は逆転している。*The Design and Implementation of the 4.4BSD Operating System* の "Local Filesystems" という章では上層をUFSとし、"Local Filestores" の章では下位層を FFS と称している。

  - [The Sun Solaris UFS implementation](http://www.informit.com/content/images/0131482092/samplechapter/mcdougall_ch15.pdf) *Solaris Internals: Solaris 10 and OpenSolaris Kernel Architecture, Second Edition* という本（Richard McDougall, Jim Mauro 著）の一部。ISBN 0-13-148209-2

## 外部リンク

  - [Little UFS2 FAQ](http://lists.freebsd.org/pipermail/freebsd-current/2003-April/001444.html)
  - Linux [userspace UFS2 tools](http://ufs-linux.sourceforge.net).
  - [Filesystems-HOWTO](http://www.tldp.org/HOWTO/Filesystems-HOWTO.html) The Linux Documentation Project の一部
  - [UFS2 Tools](http://ufs2tools.sourceforge.net/): UFSパーティションにWindowsからアクセスするためのオープンソースツール
  - [Mac OS X 10.5 Leopard: Installing on a UFS-formatted volume](http://docs.info.apple.com/article.html?artnum=306516)
  - [Large data storage in FreeBSD](http://www.freebsd.org/projects/bigdisk/index.html)

[Category:OSのファイルシステム](https://ja.wikipedia.org/wiki/Category:OSのファイルシステム "wikilink") [Category:BSD](https://ja.wikipedia.org/wiki/Category:BSD "wikilink")

1.  [The OpenBSD 2.9 Release](http://www.openbsd.org/29.html)
2.  [The OpenBSD 4.2 Release](http://www.openbsd.org/42.html)
3.  [Mac OS X 10.5 Leopard: Installing on a UFS-formatted volume](http://docs.info.apple.com/article.html?artnum=306516)
> この記事は[XFS](https://ja.wikipedia.org/wiki/XFS)から翻訳されています。


**XFS** (eXtents File System)は、[シリコングラフィックス](../Page/シリコングラフィックス.md "wikilink")が同社の[IRIX](https://ja.wikipedia.org/wiki/IRIX "wikilink")[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink")のために開発した高性能[ジャーナリングファイルシステム](../Page/ジャーナリングファイルシステム.md "wikilink")である。

## 歴史

XFSは（[JFSと共に](https://ja.wikipedia.org/wiki/Journaled_File_System "wikilink")）[UNIX](../Page/UNIX.md "wikilink")システムで最古のジャーナリングファイルシステムの一つであり、 成熟し安定し、[コードはよく](../Page/プログラム_\(コンピュータ\).md "wikilink")[デバッグ](../Page/デバッグ.md "wikilink")されている。 XFSの開発はシリコングラフィックスにより[1993年](../Page/1993年.md "wikilink")に開始され、IRIX 5.3において初めて搭載された\[1\]。

XFSは[2000年](../Page/2000年.md "wikilink")[5月](https://ja.wikipedia.org/wiki/5月 "wikilink")に[GPLで公開されると共に](../Page/GNU_General_Public_License.md "wikilink")[Linux](https://ja.wikipedia.org/wiki/Linux "wikilink")への移植が開始され\[2\]\[3\]、 [2001](../Page/2001年.md "wikilink") - [2002年](../Page/2002年.md "wikilink")ごろにはサポートする[ディストリビューション](https://ja.wikipedia.org/wiki/ディストリビューション "wikilink")が現れた\[4\]。 [Red Hat Enterprise Linux](https://ja.wikipedia.org/wiki/Red_Hat_Enterprise_Linux "wikilink")（RHEL）ではバージョン5.4以降「Scalable File Systemアドオン」という名前でXFSの有償サポートを行っていたが、RHEL7では/bootを含めた標準ファイルシステムとしてXFSを採用した。 XFSは[2002年](../Page/2002年.md "wikilink")に開発版メインラインであるLinux 2.5 [カーネル](../Page/カーネル.md "wikilink")に、次いで[2004年](https://ja.wikipedia.org/wiki/2004年 "wikilink")に安定版メインラインである2.4 カーネルにマージされた\[5\]。 ほとんどすべてのLinuxシステムにおいて利用可能で、[SUSE](../Page/SUSE.md "wikilink")、[Gentoo](../Page/Gentoo_Linux.md "wikilink")、[Mandriva](https://ja.wikipedia.org/wiki/Mandriva "wikilink")、[Slackware](../Page/Slackware.md "wikilink")、、、[Ubuntu](https://ja.wikipedia.org/wiki/Ubuntu "wikilink")、[Debian](../Page/Debian.md "wikilink")、[Fedora](../Page/Fedora.md "wikilink")、[Arch Linuxの各ディストリビューションでXFSの利用を選択することができる](https://ja.wikipedia.org/wiki/Arch_Linux "wikilink")。

[FreeBSD](../Page/FreeBSD.md "wikilink")では、[2005年](https://ja.wikipedia.org/wiki/2005年 "wikilink")[12月](https://ja.wikipedia.org/wiki/12月 "wikilink")から読み込みのみのサポートを開始し、[2006年](https://ja.wikipedia.org/wiki/2006年 "wikilink")[6月](../Page/6月.md "wikilink")には FreeBSD-7.0-CURRENTにおいて実験的書き込みが可能となった。

XFSはファイルシステムの先頭ブロックを[スーパーブロックとして使っておりブートローダーを先頭ブロックにインストールすることはできない](https://ja.wikipedia.org/wiki/スーパーブロック_\(ファイルシステム\) "wikilink")。これはIRIXとの互換性の為であり変更の予定はないとしている\[6\]\[7\]。

## 仕様

### 容量

XFSは64[ビット](../Page/ビット.md "wikilink")のジャーナリングファイルシステムであり、ファイルシステムの整合性が保証されている\[8\]。ファイルシステムサイズは最大で8[EiBであるが](https://ja.wikipedia.org/wiki/エクスビバイト "wikilink")\[9\]、通常[ホスト](https://ja.wikipedia.org/wiki/ホスト "wikilink")[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink")の仕様によりそれよりも少ない容量に制限される。たとえば32ビット Linuxにおいては、最大16[TiBである](https://ja.wikipedia.org/wiki/テビバイト "wikilink")。

### ジャーナリング

XFSはファイルシステム[メタデータ](https://ja.wikipedia.org/wiki/メタデータ "wikilink")をジャーナリングする。つまり、ファイルシステムへの変更が発生した際は、直列化されたジャーナルに書き込まれた後に、実ブロック の更新が行われる。ジャーナルは、通常のディスク操作では読み込まれることのないディスク領域に[リングバッファ](https://ja.wikipedia.org/wiki/リングバッファ "wikilink")として確保される。ジャーナルは、ファイルシステムのデータ部に置くこともできれば（内部ジャーナル）、ディスク操作の競合を避けるために別個の[デバイス](https://ja.wikipedia.org/wiki/デバイス "wikilink")上に置くこともできる（外部ジャーナル）。 XFSのジャーナルは、ファイルシステム操作が高水準に表現された「論理的な」エントリ から成る。それに対して、他のファイルシステムのジャーナルでは、[トランザクション](https://ja.wikipedia.org/wiki/トランザクション "wikilink")中で変更される ブロックのコピーをそのまま保持した、「物理的な」エントリから成る。 ジャーナルの更新は、性能の低下を避けるために[非同期](https://ja.wikipedia.org/wiki/非同期 "wikilink")的に行われる。 システム[クラッシュ](https://ja.wikipedia.org/wiki/クラッシュ "wikilink")が起きると、ジャーナルを利用することでクラッシュの直前の操作を再実行することが出来、 これによりXFSファイルシステムの整合性は保たれる。 この再実行による復旧は、ファイルシステムの[マウント](https://ja.wikipedia.org/wiki/マウント "wikilink")時に自動的に行われ、それに要する時間はファイルシステムのサイズに依存しない。 クラッシュに際し、未書き込みのデータブロックがジャーナル上に残っている場合には、復旧時にゼロで置換されて書き込まれる。 これは[セキュリティ上の問題を回避するためである](../Page/コンピュータセキュリティ.md "wikilink")。

### アロケーショングループ

XFSファイルシステムは内部的に複数のに分割することが可能である。アロケーショングループとは、等しいサイズの連続的なディスク領域である。1つのファイルやディレクトリは複数のアロケーショングループに跨って存在することが可能である。 それぞれのアロケーショングループが固有の[inode](https://ja.wikipedia.org/wiki/inode "wikilink")空間と固有の空き領域を持つことで、拡張性と[並列処理性が生み出される](https://ja.wikipedia.org/wiki/並列コンピューティング "wikilink")。（複数の異なる[スレッドや](../Page/スレッド_\(コンピュータ\).md "wikilink")[プロセス](../Page/プロセス.md "wikilink")が同一のファイルシステムに同時にアクセス可能である） この特性により、メタデータの更新も並列に行うことができ、[マルチプロセッサ](https://ja.wikipedia.org/wiki/マルチプロセッサ "wikilink")システムや[マルチコア](https://ja.wikipedia.org/wiki/マルチコア "wikilink")システムにおいて、[I/O性能を向上させることができる](../Page/入出力.md "wikilink")。 ファイルシステムが複数の物理デバイスに渡るときに、この強みは発揮され、すべての物理[ストレージ](https://ja.wikipedia.org/wiki/ストレージ "wikilink")の性能が最大限発揮される。

### ストライプアロケーション

[RAID](../Page/RAID.md "wikilink")アレイ上にXFSファイルシステムを作成するときには、**ストライプ単位**をRAIDアレイのストライプ単位と一致させることにより、[スループット](../Page/スループット.md "wikilink")を最大化することができる。

### エクステントの利用

XFSではファイルデータを格納するブロックは、と呼ばれる構造により管理される。個々のエクステントがポイントするブロック数は可変で、一つあるいは複数の連続したブロックを指し示すことが出来る。あるファイルに使われているブロックを単純に列挙して保持するファイルシステムに比べ、スペースを大きく削減できる。 他の多くのファイルシステムでは、ブロックのアロケーションのために、一つあるいは複数の[ビットマップ](https://ja.wikipedia.org/wiki/ビットマップ "wikilink")を使用しているが、XFSではこれらビットマップは、エクステントを利用した（各アロケーショングループごとに）一対の[B+木](https://ja.wikipedia.org/wiki/B+木 "wikilink")による管理構造に置き換えられている。 そのB+木の対の内、片方の木は利用できるエクステントの長さを管理し、他方はエクステントの開始ブロックを記録している。このデュアル[インデックス](https://ja.wikipedia.org/wiki/インデックス "wikilink")構造により、種々のファイルシステム操作の中で効率高く利用可能なエクステントを探索することが可能となっている。

### 可変ブロックサイズ

ファイルシステムのブロックサイズは、アロケーションの最小単位のサイズである。 XFSではブロックサイズは512[バイトから](../Page/バイト_\(情報\).md "wikilink")64[キロバイト](https://ja.wikipedia.org/wiki/キロバイト "wikilink")まで可変であり、用途に合わせてファイルシステムの作成時に指定できる。 小さなサイズのファイルを多数個使うのならば、ブロックサイズを小さくすれば利用可能な容量が大きくなるし、主に大きなサイズのファイルしか扱わないのであれば、ブロックサイズを大きくすることで読み書き性能が向上する。

### 遅延アロケーション

XFSはファイルアロケーションに[遅延書き込み](https://ja.wikipedia.org/wiki/遅延書き込み "wikilink")の技術を用いている。 バッファーキャッシュにファイルが書き込まれると、すぐにエクステントをアロケートするのではなく、記録に必要な数のブロックを予約するに止める。実際にエクステント（ブロック）がアロケートされるのはディスクにフラッシュされる時である。これにより、ファイルがなるべく連続したブロックに書き込まれるようにし、[フラグメンテーション](https://ja.wikipedia.org/wiki/フラグメンテーション "wikilink")を減少させ、性能を向上させている。

### スパースファイル

XFSでは、64ビットの[スパース](https://ja.wikipedia.org/wiki/スパース "wikilink")な[アドレス空間](https://ja.wikipedia.org/wiki/アドレス空間 "wikilink")が各ファイルごとに利用可能で、すなわち、極めて大きいサイズのファイルを扱うと同時に、ファイル中に実ディスクスペースの割り当てのない「穴」を持たせることが出来る。 XFSはファイルのデータブロックの管理に可変長のエクステントを用いるため、ファイルアロケーションマップのサイズは小さく保持できる。 アロケーションマップのサイズが一つのinodeに収まり切らなくなった場合でも、そのアロケーションマップはB+木上に移される。 以上により64ビットの広大な空間であっても迅速にアクセスすることが可能となっている。

### 拡張属性

XFSは[拡張属性として複数のデータ](https://ja.wikipedia.org/wiki/拡張ファイル属性 "wikilink")[ストリーム](https://ja.wikipedia.org/wiki/ストリーム "wikilink")を一つのファイルに格納することが出来る。 これにより複数のname/valueの対を一つのファイルに付け加えることが出来る。 nameは最大で256バイトの[ヌル終端文字列](https://ja.wikipedia.org/wiki/ヌル終端文字列 "wikilink")で、valueは最大で64キロバイトの[バイナリ](../Page/バイナリ.md "wikilink")データである。 さらにrootとuserの2つの[名前空間](../Page/名前空間.md "wikilink")に分けて記録できる。root名前空間に記録された属性は[スーパーユーザー](https://ja.wikipedia.org/wiki/スーパーユーザー "wikilink")のみが変更可能であり、user名前空間の属性はそのファイルの書き込み[パーミッションを持つユーザーのみが変更できる](https://ja.wikipedia.org/wiki/ファイルパーミッション "wikilink")。 この拡張属性は、[シンボリックリンクや](../Page/ソフトリンク.md "wikilink")[デバイスノード](https://ja.wikipedia.org/wiki/スペシャルファイル "wikilink")、[ディレクトリ](../Page/ディレクトリ.md "wikilink")などあらゆる種類のXFSのinodeに付加することが可能である。 `attr`ツールを使用して、[コマンドライン](https://ja.wikipedia.org/wiki/コマンドライン "wikilink")から操作することが出来る。 `xfsdump`/`xfsrestore`ツールは拡張属性をサポートしており、拡張属性も併せて[バックアップ](https://ja.wikipedia.org/wiki/バックアップ "wikilink")/[リストア](https://ja.wikipedia.org/wiki/リストア "wikilink")される。 他の多くのバックアップツールはXFS拡張属性に対応していない物が多い。

### ダイレクトI/O

高いディスク[スループット](../Page/スループット.md "wikilink")が必要な[アプリケーションのために](../Page/アプリケーションソフトウェア.md "wikilink")、[キャッシュ](../Page/キャッシュ.md "wikilink")されない入出力を[ユーザ空間で可能にするダイレクトI](https://ja.wikipedia.org/wiki/アドレス空間#ユーザ空間 "wikilink")/Oが提供される。ファイルデータは[DMAによりアプリケーションのバッファからディスクに直接転送されるため](../Page/Direct_Memory_Access.md "wikilink")、ディスクデバイスのI/O帯域をそのまま利用できる。

### I/O帯域保証

XFSは保証された帯域幅でのファイル入出力を可能にする[APIを提供する](../Page/アプリケーションプログラミングインタフェース.md "wikilink")。XFSは、接続されているストレージデバイスの利用可能な帯域幅を動的に計算し、要求された性能に見合った帯域幅を確保する。これは現在XFSのみがもつ機能である。 帯域保証にはhardとsoftの2種類があり、帯域保証の確実性とI/O性能のトレードオフにより使い分けることができる。ただし、hardはそのXFSファイルシステムが存在するディスクサブシステムがそれをサポートする時のみ利用可能である。 この帯域保証の機能は、ビデオ[ストリーミング](../Page/ストリーミング.md "wikilink")のような[リアルタイム](../Page/リアルタイム.md "wikilink")アプリケーションでよく用いられる。

### DMAPI

XFSは[階層型ストレージ管理](https://ja.wikipedia.org/wiki/階層型ストレージ管理 "wikilink")をサポートするための・[インタフェースを実装している](https://ja.wikipedia.org/wiki/インタフェース_\(情報技術\) "wikilink")。 この機能はLinux上で実装されているものの、主なカーネルソースには組み入れられていない。

### スナップショット

XFSは[スナップショット](https://ja.wikipedia.org/wiki/スナップショット "wikilink")を取るための機能そのものは提供しておらず、OS等の[ボリュームマネージャにより用意されることが想定されている](https://ja.wikipedia.org/wiki/論理ボリュームマネージャ "wikilink")。 そのようなボリュームマネージャによりスナップショットを取るための補助機能として、XFSは`xfs_freeze`により、ファイルシステムの凍結機能を提供している。 なお、2.6系のLinuxではスナップショット作成に`xfs_freeze`は不要である。（実行した場合、デッドロックが発生し正常にスナップショットが作成できない。）

### オンラインデフラグ

XFSは、可変長のエクステントを利用し遅延アロケーションをする為に、断片化に対してもともと高い耐性を持つが、XFSには独自のデフラグツール（`xfs_fsr`、XFS filesystem repackerの略）が用意されている。 これは[マウント](https://ja.wikipedia.org/wiki/マウント "wikilink")されていてアクティブなファイルシステムをデフラグすることが出来る。 （`xfs_fsr`は通常、`xfsprogs`パッケージではなく、`xfsdump`パッケージの一部として提供される。）

### オンラインリサイズ

XFSには`xfs_growfs`という、[オンライン](../Page/オンライン.md "wikilink")[リサイズ](https://ja.wikipedia.org/wiki/リサイズ "wikilink")のためのツールがある。 そのXFSファイルシステムが存在するディスク上に未使用のスペースがある場合には、ファイルシステムサイズを拡張することが出来る。 この機能は通常ボリュームマネージャと組み合わせて用いられる。

### ネイティブなバックアップ/復元ツール

バックアップのために`xfsdump`と`xfsrestore`というツールがXFSでは利用できる。 xfsdumpはXFSファイルシステムをinode順を保持したままバックアップすることが出来る。 UNIXの他のファイルシステムではバックアップ前にマウントを解除することが必要となることがほとんどであるが、`xfsdump`を用いるXFSファイルシステムのバックアップを使用中に取ることが出来る。 さらにこれらツールを用いたバックアップとリストアは、それぞれ実行中に一時中断したり再開したりすることが自在に可能である。 また、`xfsdump`は複数スレッドを使って実行することが可能で、複数のストリームに分割しつつ高速にバックアップを取得できる。その場合、各ストリームは異なる[メディアに書き込むことも出来る](../Page/電子媒体.md "wikilink")。（しかし、この複数ストリームによるバックアップ機能は、現在の所Linuxでは完全に実装されていない。）

## 欠点

x86マシンのLinuxで使用する場合、等と呼ばれる、レガシーなブートシーケンスに使用されるパーティションの先頭セクタ（他のファイルシステム等では通常使われない）をXFSは使用しているため、ブート可能パーティションにできない。この仕様は IRIX との互換性の維持のため、変更されない\[10\]。

削除されたファイルの復元はほぼ不可能である（これは長所でもある）。

Linuxでの実装では、異なるCPUアーキテクチャ間で、ジャーナリング最適化のために互換性の問題が発生する。しかしこの問題は、異なるアーキテクチャでマウントする前に`xfs_repair`を実行し、ジャーナルを消去することで、回避可能である。

「XFSはメタデータをジャーナリングする。」これは電源コードを不意に抜いても、再起動後には整合性のある状態に復元することを意味する（例えば、ディレクトリやそこに含まれる[ファイルリスト](https://ja.wikipedia.org/wiki/ファイルリスト "wikilink")を表示できるということである）。これは何も表示されなくなるよりはよい。しかし、XFSはデータの変更についてはジャーナルしないから、電源コードを抜いたときにデータを失う可能性はある\[11\]。この点についてはXFSだけではなく、他のファイルシステム（例えば[JFS](https://ja.wikipedia.org/wiki/Journaled_File_System "wikilink")）についても同じであり、メタデータのみのジャーナリングはアクセス速度と安全性のバランスのとれた優れた妥協点であるからである。

XFSは遅延書き込み最適化と、データとメタデータのディスク書き込み順序の点については[SuSの解釈に甘さがある](https://ja.wikipedia.org/wiki/Single_UNIX_Specification "wikilink")。同様に、[ext3](https://ja.wikipedia.org/wiki/ext3 "wikilink")やdata=orderedモードの[ReiserFS](https://ja.wikipedia.org/wiki/ReiserFS "wikilink")で動作する操作が、データ破壊を引き起こす場合がある。

    echo "original data here" > data
    echo "new data goes here" > data.new
    mv data.new data
    *crash*

この3つの操作が実行された直後にクラッシュや電源が落ちたりすると、ファイルがランダムデータやNullコードに置き換わったりする可能性がある。なお、[bug report in Ubuntu](https://launchpad.net/ubuntu/+bug/37435) と [posting from a XFS developer on linux-xfs](http://marc.theaimsgroup.com/?l=linux-xfs&m=109030382432326&w=2) にこの点に関する反対意見がある。

ディレクトリエントリの作成（空ファイル、サブディレクトリなど）と削除は他のファイルシステムに比べて遅いという指摘がある。詳細については以下を参照。[Filesystem performance tweaking with XFS on Linux](http://everything2.com/index.pl?node_id=1479435)。この問題を解決するため、メタデータジャーナルにも遅延書き込み技術が適用され、バージョン3.12以降のLinuxカーネルで標準となった。詳細については\[[http://lwn.net/Articles/476263/\]及びカーネルドキュメントの"filesystems/xfs-delayed-logging-design.txt"を参照](http://lwn.net/Articles/476263/%5D及びカーネルドキュメントの%22filesystems/xfs-delayed-logging-design.txt%22を参照)。

[SELinuxが登場した当初](https://ja.wikipedia.org/wiki/Security-Enhanced_Linux "wikilink")、XFSで使用すると性能劣化を引き起こす事が取り沙汰された。\[12\] これはXFSの「拡張属性がinode内に収められる場合は追加のディスクI/Oが要らない為高速だが、そうでない場合はinode外に個別のブロックを割り当てる為に拡張属性の参照に通常のデータと同じだけのディスクI/Oを伴う」という特性に対してSELinuxが使用する拡張属性がinode内に収められないサイズであった為に起きた。 この事自体はinodeに収めきれない拡張属性全てに起こるものでSELinux固有のものではないが、「多くのファイルが拡張属性を付加されている」、「至る所で暗黙的に読み出される事」という事情があり性能劣化を引き起こした。この問題は「attr2と呼ばれる新しい拡張属性の格納ポリシーを使用する」、「inodeの大きさをデフォルトより大きくする」のいずれかの行動を取ることで回避できる。xfsprogs バージョン2.7 以降では attr2 の使用がデフォルトになっており、問題回避のための対処を行う必要はない。

## 出典



[Category:Linuxのファイルシステム](https://ja.wikipedia.org/wiki/Category:Linuxのファイルシステム "wikilink") [Category:UNIX](https://ja.wikipedia.org/wiki/Category:UNIX "wikilink") [Category:1994年のソフトウェア](https://ja.wikipedia.org/wiki/Category:1994年のソフトウェア "wikilink")

1.
2.
3.
4.
5.
6.
7.
8.
9.
10.
11.
12. [EA and ACL Performance](http://www.suse.de/~agruen/acl/linux-acls/online/#SECTION000100000000000000000)
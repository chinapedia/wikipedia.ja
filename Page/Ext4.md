> この記事は[Ext4](https://ja.wikipedia.org/wiki/Ext4)から翻訳されています。


**ext4**（fourth extended file system）は、[Linux](../Page/Linux.md "wikilink")の[ファイルシステム](../Page/ファイルシステム.md "wikilink")で、[ジャーナリングファイルシステム](../Page/ジャーナリングファイルシステム.md "wikilink")の一つである。[ext3](https://ja.wikipedia.org/wiki/ext3 "wikilink")の後継のファイルシステムで、拡張機能を使っていない場合に限りext3としてマウントできる。1[EiBまでのストレージをサポートし](https://ja.wikipedia.org/wiki/エクスビバイト "wikilink")、ファイルの断片化を防ぐextent file writingと呼ばれるシステムが導入される。ファイルのタイムスタンプは、ナノ秒単位で西暦1901年から2514年までの範囲をサポートする（ext3では秒単位で2038年まで）。[Linuxカーネル](../Page/Linuxカーネル.md "wikilink") 2.6.19より開発版が利用が可能になり、2.6.28\[1\]より安定版のファイルシステムとなった。

## 経緯

[ext3](https://ja.wikipedia.org/wiki/ext3 "wikilink")に対して後方互換性を保ちつつ、[64ビット](../Page/64ビット.md "wikilink")ストレージの制限を除き、パフォーマンスを向上させるために開発が始められた\[2\]。しかしLinuxカーネルの開発者たちは、安定性に対する懸念から、ext3に拡張を加えることに反対した\[3\]。その代わり、ext3の[ソースコード](../Page/ソースコード.md "wikilink")から分岐してext4と改名し、現行のext3ユーザーに影響を及ぼすことなく開発を進めることを提案した。この提案は受け入れられ、2006年6月28日、ext3のメンテナである[セオドア・ツォー](https://ja.wikipedia.org/wiki/セオドア・ツォー "wikilink") (Theodore Ts'o) は新しいプロジェクトとしてext4の開発を発表した\[4\]。

最初の開発スナップショットはLinux 2.6.19に導入された。2008年10月11日には、ext4を安定コードとしたパッチがLinux 2.6.28のソースコードリポジトリに結合された\[5\]。これは開発段階の終了を意味し、ext4の採用を推奨するものであった。ext4ファイルシステムを含むLinux 2.6.28は、[2008年](https://ja.wikipedia.org/wiki/2008年 "wikilink")[12月25日](../Page/12月25日.md "wikilink")にリリースされた\[6\]。

## 特徴

  - 大きなボリュームサイズとファイルサイズ
    ext4ファイルシステムは、最大1EiBまでのボリュームサイズ\[7\]と、最大16TiBまでのファイルサイズをサポートする。
  - エクステント
    [エクステント](https://ja.wikipedia.org/wiki/エクステント "wikilink")は、[ext2](https://ja.wikipedia.org/wiki/ext2 "wikilink")および[ext3](https://ja.wikipedia.org/wiki/ext3 "wikilink")で使われてきた伝統的なブロックマッピング方式を置き換える概念である。エクステントは連続した物理ブロックの集合であり、大きなファイルに対するパフォーマンスを改善し、フラグメンテーションの発生を減らすことができる。ext4におけるエクステントは、4KiBのブロックサイズで最大128MiBまでの連続した領域をマッピングすることができる\[8\]。[inode](https://ja.wikipedia.org/wiki/inode "wikilink")ごとに4つのエクステントを格納することができる。ひとつのファイルに5つ以上のエクステントがあるとき、残りのエクステントは[Htree](https://ja.wikipedia.org/wiki/Htree "wikilink")で構造化される。
  - 後方互換性
    ext4ファイルシステムはext3およびext2に対する後方互換性を持つ。すなわち、ext3およびext2ファイルシステムをext4ファイルシステムとしてマウントすることができる。その場合でも、わずかにパフォーマンスの向上が見られる。なぜなら、ブロック確保アルゴリズムなどの新しい機能はext3やext2でも使用できるからである。
    ext3ファイルシステムは部分的にext4に対する前方互換性を持つ。すなわち、ext4ファイルシステムをext3パーティションとしてマウントできる（マウントするときは「ext3」をファイルシステムタイプとして指定する）。しかし、もしext4パーティションがエクステント（ext4の重要な新機能である）を使用しているなら、ext3としてマウントすることはできなくなる。
  - 永続的な事前確保
    ext4ファイルシステムはファイルのためのディスク空き領域の事前確保を可能にする。ほとんどのファイルシステムにおけるこれまでの方法論では、ファイルが作成されたときに予約されたスペースを0で埋める形で書き込まれる。ext4においてはこの方法で要求されることはもはやない。そのかわり、新しくfallocate()システムコールがLinuxカーネルにファイルシステム用に追加され、ext4やXFSにおいて使われている。これにより互換性が維持されている。ファイルのために確保されたスペースはディスクフルによる書き込み失敗はしないことが保証され、連続していることが期待される。この機能はメディアストリーミングやデータベースで使われる。
  - 遅延確保
    ext4ファイルシステムのパフォーマンス向上のテクニックとして、[allocate-on-flush](https://ja.wikipedia.org/wiki/allocate-on-flush "wikilink")と呼ばれるものがある。これは*遅延確保*としても知られている。つまりext4では、データがディスクにフラッシュされるまでブロックの確保が遅延される(対して一部のファイルシステムでは、データが書き込みキャッシュに入れられる場合でも、ブロックは直ちに確保される)。より大きなデータを一度に効率的に確保することにより、遅延確保はパフォーマンスを向上させ、フラグメント化を減少させる。
  - サブディレクトリの32000個制限の撤廃
    [ext3](https://ja.wikipedia.org/wiki/ext3 "wikilink")ファイルシステムにおいては、1つのディレクトリに入れられるサブディレクトリ数が32,000個に制限されている。この制限がext4ファイルシステムでは64,000個まで引き上げられ、"dir_nlink"機能を使うとそれを超える事が可能となる（親ディレクトリのリンクカウント増加は止まるだろうが）。一つのディレクトリ内のファイル数が増えた場合における性能を上げる為、[Htree](https://ja.wikipedia.org/wiki/Htree "wikilink")インデックス（[B-tree](https://ja.wikipedia.org/wiki/B-tree "wikilink")の発展版）は、ext4でデフォルトでオンになった。この機能はLinux kernel 2.6.23 から導入されている。Htreeはext3でもdir_index機能が有効であれば利用可能であった。
  - ジャーナルのチェックサム
    ext4は信頼性を向上するため、ジャーナルにチェックサムを使用する。なぜならばジャーナルはディスクで最も使用されるファイルの一つだからである。この機能によってジャーナル過程の間ディスクI/Oの待機を安全に避ける事ができるという利点を持つ。これによりパフォーマンスが若干向上する。ジャーナルのチェックサムのテクニックは『IRON File Systems』というウィスコンシン州立大学の研究論文にインスパイアされたものである。（とりわけ6章の『トランザクション・チェックサム』の部分）\[9\]
  - オンラインのデフラグメンテーション
    e4defrag により、マウント中（オンライン）でのデフラグが可能になった。ファイルシステムのフラグメンテーションを避けるための様々なテクニックによってフラグメントしにくくなっているが、それでもなお、長期間運用されたファイルシステムは時間経過によってフラグメントが発生する場合がある\[10\]。
  - より高速なファイルシステムチェック
    ext4において、確保されていないブロック群とi-nodeテーブル部は印をつけられる。これは[e2fsck](https://ja.wikipedia.org/wiki/e2fsck "wikilink")の実行時に全体のチェックを不要にし、ファイルシステムのチェックにかかる時間を大きく減少させる。この機能は2.6.24のLinuxカーネルで実装された。
  - マルチブロックの確保
    ext3では、ファイルが追加される際にブロックアロケータをそれぞれのブロック個別に1回ずつ呼び出す。そのため、同時に複数書き込みを行う場合には、ディスク上でファイルのフラグメントは容易に発生する。しかし、ext4ではデータをバッファして複数のブロック群を一度に確保する遅延確保を利用する。これはアロケータは何を書き込むべきかについてより多くの情報を保持することを意味し、そしてディスク上のファイル領域確保のためより良い選択を行うことができるようになる。マルチブロックアロケータは遅延確保がファイルシステム上で有効になっているとき、もしくはファイルがO_DIRECTモードで開かれているときに使用される。この機能はディスクフォーマットには影響しない。
  - タイムスタンプの改良
    コンピューターが全体的により高速になると共に、Linuxはよりミッションクリティカルな用途で使用されるようになり、秒ベースの粒度のタイムスタンプでは不十分となってきている。この解決として、ext4ではタイムスタンプをナノ秒単位で提供している。付け加えて、[2038年問題](../Page/2038年問題.md "wikilink")を引き伸ばすためにタイムスタンプの秒フィールドの上位に2ビットの拡張タイムスタンプフィールドが付け加えられ、結果として204年後まで先延ばしにしている。
    ext4は作成日時のタイムスタンプ(time-of-creation timestamps)を追加でサポートする。しかし、[セオドア・ツォー](https://ja.wikipedia.org/wiki/セオドア・ツォー "wikilink")が指摘するように、[inode](https://ja.wikipedia.org/wiki/inode "wikilink")に作成日時フィールドを追加する(つまり技術的にそのタイムスタンプのサポートをext4で可能にする)のは簡単であるものの、stat() (おそらく新しいバージョンが必要となる)などの必要なシステムコールや、それに依存する各ライブラリ(glibcなど)の変更や追加はより難しい。これらの変更は様々なプロジェクトでの調整が必要となる\[11\]。そのため、ext4に保存された作成日時は、現在のところLinux上のユーザプログラムに対してstatx() APIによってのみ提供される\[12\]。

## 欠点

### 遅延アロケーションとデータ損失

遅延アロケーションは、すべてのデータをディスクに書き出す前にファイルシステムがクラッシュした際、データを損失する危険性を孕む。

このようなことが起こる典型的なシナリオは、[fsync](https://ja.wikipedia.org/wiki/fsync "wikilink")でディスクに書き出すことをせずにファイルの内容を書き換えるようなプログラムを使用する時である。実際に書き出しをする前にシステムがクラッシュすると、問題が起こる可能性がある。このような状況では、ext3のユーザーは、クラッシュ後に変更前か変更後のどちらかのデータがディスクに残されているということを期待することができた。一方、Linuxカーネル2.6.28のext4では、クラッシュ前にファイルの内容を消去するが新しいデータを書き出さず、結果としてデータが損失するということがしばしば見られた。

この問題に対処するためにfsyncを頻繁に使用すると、`data=ordered`フラグ（多くのLinuxディストリビューションではデフォルト）でマウントされたext3ファイルシステムでは深刻なパフォーマンス低下が起こる恐れがある。どちらのファイルシステムもしばらくの間使用されるだろうということを考えると、これはエンドユーザーアプリケーション開発者にとって非常に厄介な問題となる。このため、セオドア・ツォーは、上記のような場合の遅延アロケーションを制限するext4のパッチを作成した。パフォーマンスは多少低下するが、これによってクラッシュ後にどちらかのバージョンのデータが残る可能性が著しく高まった。

このパッチはメインライン・カーネル2.6.30に導入されているが、様々なディストリビューションは2.6.28や2.6.29へとバックポートすることができる。例えば、[Ubuntu](../Page/Ubuntu.md "wikilink")はバージョン9.04 Jaunty Jackalopeでカーネル2.6.28にそのパッチを導入した。

## ディストリビューション

以下の Linux ディストリビューションで標準ファイルシステムとして採用されている。

  - [Ubuntu](../Page/Ubuntu.md "wikilink") - 9.04 から利用可能、9.10 から標準
  - [Debian](../Page/Debian.md "wikilink") - 6.0 から利用可能
  - [Fedora](../Page/Fedora.md "wikilink") - 9 から利用可能、11〜15 にて標準
  - [Red Hat Enterprise Linux](../Page/Red_Hat_Enterprise_Linux.md "wikilink") - 5.6 からフルサポート
  - Amazon Linux AMI - 2011.02 から標準

## 脚注

## 関連項目

  - [Btrfs](https://ja.wikipedia.org/wiki/Btrfs "wikilink")
  - [ファイルシステム](../Page/ファイルシステム.md "wikilink")

## 外部リンク

  - [Kernel Log: Ext4 completes development phase as interim step to btrfs](http://heise-online.co.uk/news/Kernel-Log-Ext4-completes-development-phase-as-interim-step-to-btrfs--/111742)
  - [Theodore Ts'o's discussion on ext4](https://archive.is/20120712143749/kerneltrap.org/node/6776)
  - [Real World Benchmarks Of The EXT4 File-System](http://phoronix.com/scan.php?page=article&item=ext4_benchmarks&num=1)
  - [Ext4 Wiki](http://ext4.wiki.kernel.org/)
  - ["Ext4 block and inode allocator improvements"](http://ols.fedoraproject.org/OLS/Reprints-2008/kumar-reprint.pdf) (Ottawa Linux Symposium 2008の資料)
  - ["The new ext4 filesystem: current status and future plans"](http://www.linuxsymposium.org/archives/OLS/Reprints-2007/mathur-Reprint.pdf) (Ottawa Linux Symposium 2007の資料)
  - ["ext4 online defragmentation"](http://www.linuxsymposium.org/archives/OLS/Reprints-2007/sato-Reprint.pdf) (materials from Ottawa Linux Symposium 2007)
  - [“Ext4: Ext2/3の次世代のファイルシステム”](http://usenix.org/event/lsf07/tech/cao_m.pdf)
  - [Kernelnewbies.org: Ext4, the Fourth Extended File System](http://kernelnewbies.org/Ext4)
  - [Gentoo Live InstallCD](http://gentoolivecd.piffpaffpuff.net/), with ext4 and ssh

[Category:Linuxのファイルシステム](https://ja.wikipedia.org/wiki/Category:Linuxのファイルシステム "wikilink") [Category:2006年のソフトウェア](https://ja.wikipedia.org/wiki/Category:2006年のソフトウェア "wikilink")

1.  [Linux 2 6 28 - Linux Kernel Newbies](http://kernelnewbies.org/Linux_2_6_28)
2.
3.
4.
5.
6.
7.
8.
9.
10. <http://kernelnewbies.org/Ext4#head-38e6ac2b5f58f10989d72386e6f9cc2ef7217fb0>
11.
12.
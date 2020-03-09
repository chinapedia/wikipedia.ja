> この記事は[Ext3](https://ja.wikipedia.org/wiki/Ext3)から翻訳されています。


**ext3**は、third extended file systemの略で、[Linux](https://ja.wikipedia.org/wiki/Linux "wikilink")の[ファイルシステム](../Page/ファイルシステム.md "wikilink")である。[ジャーナリングファイルシステム](../Page/ジャーナリングファイルシステム.md "wikilink")の一つ。 Linux[カーネル](../Page/カーネル.md "wikilink") 2.4.15より利用が可能になった。

ext3ファイルシステムドライバのための[ワークアラウンド](https://ja.wikipedia.org/wiki/ワークアラウンド "wikilink")が必要になっていること、著名なディストリビューションがLinux 2.6.33で追加されたext2ファイルシステムドライバとext3ファイルシステムドライバを使用せずext4ファイルシステムドライバでext2とext3を取り扱う設定を有効にしたカーネルでリリースするようになってから既に数年経ち問題が起きていないこと、カーネルからext3ファイルシステムドライバを削除し前述の設定だけにしたとしても互換性問題が発生しないことなどを理由にLinux 4.3で削除された。\[1\]

## 長所

[ext2](https://ja.wikipedia.org/wiki/ext2 "wikilink")と互換性が高い。ext2パーティションをマウントしたままext3に変換することが可能であり、ext2ファイルシステムとしてマウントすることもできる（ただし、この場合には、ジャーナリング機能を使用することはできない）。

ext2に比べext3には以下の機能が加わっている。

  - [ジャーナリング](https://ja.wikipedia.org/wiki/ジャーナルファイルシステム "wikilink")
  - 複数のブロックに跨るディレクトリに対してのツリーベースのディレクトリインデックス
  - オンラインファイルシステムリサイズ(拡張のみ)

dir_indexオプションをつけると、ディレクトリ内の検索に、hashed b-tree を使うことができ、ディレクトリ内に多数のファイルがある場合、劇的に高速化する。

## 短所

### 機能

ext3はext2と高い[後方互換](https://ja.wikipedia.org/wiki/後方互換 "wikilink")性を持つことを目指して作られているので、構造の多くがext2と類似している。そのため、ext3は最近のファイルシステムが持っているいくつかの特徴（例えばi-nodesと可変ブロックサイズのダイナミックアロケーションなど）を持っていない。

ファイルシステムに書き込みが行われている間、ext3ファイルシステムは[fsck](https://ja.wikipedia.org/wiki/fsck "wikilink")することができない。

右の日付範囲の欄に見られるようにタイムスタンプが2038年1月18日以降の日付に対応していない。2008年頃から[2038年問題](../Page/2038年問題.md "wikilink")に対応済みの[ext4](https://ja.wikipedia.org/wiki/ext4 "wikilink")方式に移行している。

### 圧縮

ext3では、[非公式パッチ](http://sourceforge.net/projects/e3compr/)の形で透過的な圧縮方法を使用することができる。

## 比較

改良が年々重ねられていて、速度は徐々に速くなっている。他のファイルシステム、[ReiserFS](https://ja.wikipedia.org/wiki/ReiserFS "wikilink")や[XFS](https://ja.wikipedia.org/wiki/XFS "wikilink")と比べ、劣っている部分と勝っている部分がある。

CPUリソースの消費は少なめといわれる。

## 脚注

## 関連項目

  - [ext4](https://ja.wikipedia.org/wiki/ext4 "wikilink")

[Category:Linuxのファイルシステム](https://ja.wikipedia.org/wiki/Category:Linuxのファイルシステム "wikilink") [Category:2001年のソフトウェア](https://ja.wikipedia.org/wiki/Category:2001年のソフトウェア "wikilink")

1.
> この記事は[Ext2](https://ja.wikipedia.org/wiki/Ext2)から翻訳されています。


**ext2** (**second extended filesystem**) は、[Linux](https://ja.wikipedia.org/wiki/Linux "wikilink")[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink")で広く利用されていた[ファイルシステム](../Page/ファイルシステム.md "wikilink")である。初期の[ext](https://ja.wikipedia.org/wiki/ext "wikilink")ファイルシステムを拡張したためext2と名付けられた。現在の多くの[ディストリビュータは](../Page/Linuxディストリビューション.md "wikilink")[ext4](https://ja.wikipedia.org/wiki/ext4 "wikilink")を標準で採用している。

パーティションの上限は当初2[GiBであったが](https://ja.wikipedia.org/wiki/ギビバイト "wikilink")、2.4系[カーネル](../Page/カーネル.md "wikilink")では4[TiBまで拡張されている](https://ja.wikipedia.org/wiki/テビバイト "wikilink")。255バイトまでのファイル名や、可変長のディレクトリエントリに対応している。また、一部をスーパーユーザー (root) のために予約しており、通常の領域を使い切ってもメンテナンスを行うことができる。

ext2は、[ジャーナリング](https://ja.wikipedia.org/wiki/ジャーナリング "wikilink")を備えていないため、いったんクラッシュするとファイルシステムの復旧に時間がかかる。そのため、[ext3](https://ja.wikipedia.org/wiki/ext3 "wikilink")や[ReiserFS](https://ja.wikipedia.org/wiki/ReiserFS "wikilink")などの[ジャーナリングファイルシステム](../Page/ジャーナリングファイルシステム.md "wikilink")の普及に努めている。

## 歴史

初期のLinuxの開発は、[MINIX](https://ja.wikipedia.org/wiki/MINIX "wikilink")上で[クロス開発](https://ja.wikipedia.org/wiki/クロス開発 "wikilink")されていた。extがLinuxで採用されたのはその経緯があったためである。しかし、システム内部の構造は16ビットであり、64[MiBまでのファイルサイズのサイズ制限があり](https://ja.wikipedia.org/wiki/メビバイト "wikilink")、14文字までのファイル名長もそのままLinuxにも残された。

新しいファイルシステムの追加を安易にするためのAPIをLinuxカーネルに加えたのち、extは、[VFS](https://ja.wikipedia.org/wiki/仮想ファイルシステム "wikilink") APIを用いた最初のファイルシステム (ext) が1992年4月に公表され、Linux 0.96cにそのファイルシステムが含まれることになった。改訂されたextはMINIXのファイルシステムの2つの制約を解決することに至ったが、[inode](https://ja.wikipedia.org/wiki/inode "wikilink")とタイムスタンプのサポートが不完全なままであった。

1993年1月、この問題の解決として2つの新しいファイルシステムである[xiafs](https://ja.wikipedia.org/wiki/xiafs "wikilink")とext2が開発された。[Berkeley Fast File Systemから多くのアイディアを取り込んだ](https://ja.wikipedia.org/wiki/UFS "wikilink")。

それ以降、ext2はVFS APIの新規の拡張を多く取り込みテスト段階になった。

最終的にext2は4TiBと255バイトまでのファイル名長、可変長[ブロックサイズ](https://ja.wikipedia.org/wiki/ブロックサイズ "wikilink")を得ることとなった。

## 構造

ext2の空間はフラグメントを減らし、ディスクシークを最小化するために[ブロックで分けられており](https://ja.wikipedia.org/wiki/ブロック_\(データ\) "wikilink")、ブロックグループを作り組織化する。

[スーパーブロックはOSの起動にとって重要な情報を含む](https://ja.wikipedia.org/wiki/スーパーブロック_\(ファイルシステム\) "wikilink")。

[Category:Linuxのファイルシステム](https://ja.wikipedia.org/wiki/Category:Linuxのファイルシステム "wikilink") [Category:1993年のソフトウェア](https://ja.wikipedia.org/wiki/Category:1993年のソフトウェア "wikilink")
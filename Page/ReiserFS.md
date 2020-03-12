> この記事は[ReiserFS](https://ja.wikipedia.org/wiki/ReiserFS)から翻訳されています。


**ReiserFS**（ライザーエフエス）は、[Linux](../Page/Linux.md "wikilink")における[ジャーナリングファイルシステム](../Page/ジャーナリングファイルシステム.md "wikilink")の実装の一つ。Linux [kernel](../Page/カーネル.md "wikilink") 2.4.1から標準搭載となった。Linuxカーネルのソースコードに取り込まれたはじめてのジャーナリングファイルシステムである。

1996年から[ハンス・ライザー](../Page/ハンス・ライザー.md "wikilink")(Hans Reiser)率いるNamesys社によって開発されていたが、後継の[Reiser4](../Page/Reiser4.md "wikilink")の開発に集中するため開発が中止された。2006年にハンス・ライザーが妻の殺害容疑で逮捕された後、2008年にNamesys社も廃業し、主要な開発者であったハンス・ライザーは2008年に懲役15年の判決が下ったため、現在はボランティアベースで開発が進められている。

## 主な特徴

  - [ext2](https://ja.wikipedia.org/wiki/ext2 "wikilink")/[ext3](https://ja.wikipedia.org/wiki/ext3 "wikilink")ファイルシステムと互換性は無い。
  - 最大16TiBまでのボリュームサイズをサポートする。
  - 最大8TiBのファイルをサポートする。
  - ext2/ext3よりもパフォーマンスに優れるとされており、特にサイズの小さいファイルを多数処理する際に優れている。

## ディストリビューション

2000年代中頃においてはいくつかのLinuxディストリビューションにおいてデフォルトのファイルシステムとなっていた。多くのディストリビューションで、インストール時にファイルシステムとして選択できた。大手ディストリビューションの中では[SUSE Linuxで採用されていたのが代表的である](https://ja.wikipedia.org/wiki/SUSE_Linux "wikilink")。

しかしハンス・ライザーが殺人罪で逮捕された2006年に、、SUSEも[ext3](https://ja.wikipedia.org/wiki/ext3 "wikilink")への移行を発表した。

デフォルトとして採用されている物の一覧は[:en:Comparison of Linux distributions\#Technicalを参照](https://ja.wikipedia.org/wiki/:en:Comparison_of_Linux_distributions#Technical "wikilink")。

[Category:Linuxのファイルシステム](https://ja.wikipedia.org/wiki/Category:Linuxのファイルシステム "wikilink") [Category:UNIX](https://ja.wikipedia.org/wiki/Category:UNIX "wikilink") [Category:2001年のソフトウェア](https://ja.wikipedia.org/wiki/Category:2001年のソフトウェア "wikilink")
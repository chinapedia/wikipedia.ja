> この記事は[DCE Distributed File System](https://ja.wikipedia.org/wiki/DCE_Distributed_File_System)から翻訳されています。


**DCE Distributed File System**（**DCE/DFS**）は、[Distributed Computing Environmentで使われている遠隔ファイルアクセスプロトコルである](../Page/Distributed_Computing_Environment.md "wikilink")\[1\]。[トランザーク](https://ja.wikipedia.org/wiki/トランザーク "wikilink")の開発した AFS Version 3.0 に基づいている。AFS Version 3.0 は、[カーネギーメロン大学](https://ja.wikipedia.org/wiki/カーネギーメロン大学 "wikilink")で開発された [Andrew File System](../Page/Andrew_File_System.md "wikilink") Version 2.0 プロトコルに基づいて開発された。

## 概要

DCE/DFS は複数のコンポーネントから成り、[POSIX](../Page/POSIX.md "wikilink") のローカル[ファイルシステム](../Page/ファイルシステム.md "wikilink")を擬似する[分散ファイルシステム](../Page/分散ファイルシステム.md "wikilink")を提供し、可能な限り最適化を施している。DCE/DFS クライアントは、本来の[ファイルのコピーとしてローカルな](../Page/ファイル_\(コンピュータ\).md "wikilink")[キャッシュを利用する](../Page/キャッシュ_\(コンピュータシステム\).md "wikilink")。クライアントシステムはサーバシステムと協調し、ファイルの原本が複数のクライアントからアクセスされ、原本が変更されたときにキャッシュの再フェッチが行われることを保証する。

この手法の利点は、ネットワークが低速であっても非常に良い性能となる点である。というのは、ファイルアクセスのほとんどはローカルなキャッシュで済むためである。サーバが障害状態となっても、クライアントはローカルにファイルの更新が可能で、サーバが復活したときにサーバにそれを戻すようになっている。

DCE/DFS はまた、管理上の論理ユニットの概念（[ファイルセット](https://ja.wikipedia.org/wiki/ファイルセット "wikilink")）とそれが格納されているボリュームとを切り離した。そうすることで、エンドユーザにとって[透過的な方法でファイルセットの位置の管理制御が可能となっている](../Page/透過性_\(情報工学\).md "wikilink")。このような DCE/DFS の先進的機能をサポートするため、ローカルな[ジャーナリングファイルシステム](../Page/ジャーナリングファイルシステム.md "wikilink")（DCE/LFS、Episode とも）が開発され、DFS の全てのオプションを提供している。

[IBM](../Page/IBM.md "wikilink") は [2005年](../Page/2005年.md "wikilink")以降、DCE/DFS の保守サポートをしていない\[2\]。IBM は DCE/DFS から代替の [ADFS](http://www.ibm.com/developerworks/linux/library/l-plam/?S_TACT=105AGX52&S_CMP=cn-a-l) (Advanced Distributed File System) への移行を進めている。このプロジェクトの主要な目標は、DFS を DCE のディレクトリサービス (CDS) およびセキュリティサービス (secd）と切り離すことである。しかし、2005年以降このプロジェクトについて公式な発表は何も無く、プロジェクトが中止されたと見られている。

## 脚注

## 関連項目

  - [Distributed Computing Environment](../Page/Distributed_Computing_Environment.md "wikilink")
  - [Andrew File System](../Page/Andrew_File_System.md "wikilink")

## 外部リンク

  - [DCE 公式サイト](http://www.opengroup.org/dce/)
  - [Some DCE Papers Available On-Line](http://www.opengroup.org/dce/info/papers/).

[Category:インターネットのプロトコル](https://ja.wikipedia.org/wiki/Category:インターネットのプロトコル "wikilink") [Category:OSのファイルシステム](https://ja.wikipedia.org/wiki/Category:OSのファイルシステム "wikilink") [Category:ネットワークソフト](https://ja.wikipedia.org/wiki/Category:ネットワークソフト "wikilink")

1.  Open Software Foundation, Inc. (July 1991). *[File Systems in a Distributed Computing Environment](http://www.opengroup.org/dce/info/papers/osf-o-wp8-0990-2.ps)*. Open Software Foundation, Inc.
2.  [DFS - Product Overview](http://www-306.ibm.com/software/stormgmt/dfs/) IBM
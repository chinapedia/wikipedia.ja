> この記事は[Adeos](https://ja.wikipedia.org/wiki/Adeos)から翻訳されています。


**Adeos**（Adaptive Domain Environment for Operating Systems）は、[ナノカーネル型の](https://ja.wikipedia.org/wiki/カーネル#.E3.83.8A.E3.83.8E.E3.82.AB.E3.83.BC.E3.83.8D.E3.83.AB "wikilink") [Hardware Abstract Layer](https://ja.wikipedia.org/wiki/Hardware_Abstract_Layer "wikilink") (HAL) であり、[ハードウェア](../Page/ハードウェア.md "wikilink")と[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink") (OS) の中間で動作する。他のナノカーネルと違う点は、OSの[カーネル](../Page/カーネル.md "wikilink")の一部として動作するわけではない点である。実際、複数のカーネルを上位で同時に動作させることができ、一種の[仮想化](../Page/仮想化.md "wikilink")技術になっている。

Adeos は複数のOSや単一OSの複数インスタンスの間でハードウェア[リソースを共有する柔軟な環境を提供し](../Page/計算資源.md "wikilink")、同一ハードウェア上に複数の優先順位付けされたドメインを同時に存在させることができる。

Adeos を [Linuxカーネル](../Page/Linuxカーネル.md "wikilink") の下に挿入することで、[SMPクラスタリング](../Page/対称型マルチプロセッシング.md "wikilink")、[パッチ](https://ja.wikipedia.org/wiki/パッチ "wikilink")を使わないカーネルの[デバッグ](../Page/デバッグ.md "wikilink")、[Linux](https://ja.wikipedia.org/wiki/Linux "wikilink") による[リアルタイムシステム](https://ja.wikipedia.org/wiki/リアルタイムシステム "wikilink")といった可能性が開けてくる。

他の HAL とは異なり、Adeos は Linux の[ローダブル・カーネル・モジュール](https://ja.wikipedia.org/wiki/ローダブル・カーネル・モジュール "wikilink")としてロードでき、それを使って他のOSを動作させることができる。Adeos は [RTAI](https://ja.wikipedia.org/wiki/RTAI "wikilink") (Real-Time Application Interface) の一環として、リアルタイムカーネルからHALを分離しモジュール化するために開発された。

## アーキテクチャ

Adeos は[シグナルの](https://ja.wikipedia.org/wiki/シグナル_\(Unix\) "wikilink")[キューを実装している](../Page/キュー_\(コンピュータ\).md "wikilink")。周辺機器がシグナルを送信すると、Adeos は動作中のOSの1つにシグナルを転送し、各OSがそのシグナルを処理するか、無視するか、捨てるか、終了させるかを決定する。処理または終了されなかったシグナルは、次のOSに転送される。

## 関連項目

  - [ナノカーネル](https://ja.wikipedia.org/wiki/カーネル#ナノカーネル "wikilink")

## 外部リンク

  - [Adeos 公式サイト](http://home.gna.org/adeos/)
  - [Adeos Workspace](https://gna.org/projects/adeos/)

[Category:OSのカーネル](https://ja.wikipedia.org/wiki/Category:OSのカーネル "wikilink") [Category:仮想化](https://ja.wikipedia.org/wiki/Category:仮想化 "wikilink")
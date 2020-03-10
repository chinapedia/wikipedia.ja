> この記事は[ENQUIRE](https://ja.wikipedia.org/wiki/ENQUIRE)から翻訳されています。


**ENQUIRE** は[ティム・バーナーズ＝リー](../Page/ティム・バーナーズ＝リー.md "wikilink")が1980年に[CERNにて行った](../Page/欧州原子核研究機構.md "wikilink")[ソフトウェア](../Page/ソフトウェア.md "wikilink")プロジェクトであり\[1\]、1989年の[World Wide Web開発の下地となった](../Page/World_Wide_Web.md "wikilink")\[2\]\[3\]\[4\]。単純な[ハイパーテキスト](../Page/ハイパーテキスト.md "wikilink")プログラムであり\[5\]、Webおよび[セマンティック・ウェブ](../Page/セマンティック・ウェブ.md "wikilink")と同じ考え方を共有しているが、重要な部分で相違もある。

バーナーズ＝リーによれば、その名称は*[Enquire Within Upon Everything](https://ja.wikipedia.org/wiki/:en:Enquire_Within_Upon_Everything "wikilink")*という本（家庭生活についての[ハウツー](../Page/ハウツー.md "wikilink")本）の題名から発想したものだという\[6\]\[7\]\[8\]。

## 背景

当時CERNには約1万人の人々が働いており、様々な機種のコンピュータとその上の[ソフトウェア](../Page/ソフトウェア.md "wikilink")が使われていた。業務上は[電子メール](../Page/電子メール.md "wikilink")とファイルのやりとりが頻繁に行われていた\[9\]。科学者らは複数の仕事に携わり\[10\]、個々のプロジェクトは相互に関連していた\[11\]。バーナーズ＝リーは1980年6月23日から6ヶ月間CERNで働き、ENQUIREを開発した\[12\]。CERN内では様々なネットワーク、データフォーマット、文字コードが使用されており、異なるシステム間の情報転送が難しかったため、ENQUIREはそれに対処することを要求された\[13\]。ENQUIRE以前のハイパーテキストシステム、[Memex](https://ja.wikipedia.org/wiki/Memex "wikilink")や[NLS](https://ja.wikipedia.org/wiki/NLS "wikilink")はそういった要件を備えていなかった\[14\]。

## HyperCard との違い

ENQUIREは[アップルの](../Page/アップル_\(企業\).md "wikilink")[HyperCard](../Page/HyperCard.md "wikilink")と似ており、どちらもテキストがクリック可能ではなく、厳密には「ハイパーテキスト」ではない。また、ENQUIREは画像を扱えなかった\[15\]。ENQUIREがHyperCardに比べて優れているのは様々なシステムで動作する移植性の高さだった\[16\]。

## World Wide Web との違い

<div class="noprint" style="clear:right; border:solid #aaa 1px; margin:0 0 0em 0em; background:#eeffee; spacing:0; text-align:left; float:right; font-size:80%;">

**`Documentation``   ``of``   ``the``   ``RPC``   ``project``   ``(concept)`**

`Most of the documentation is available on VMS, with the two`
`principle manuals being stored in the CERNDOC system.`

`1) includes: The VAX/NOTES conference VXCERN::RPC`
`2) includes: Test and Example suite`
`3) includes: RPC BUG LISTS`
`4) includes: RPC System: Implementation Guide`
`Information for maintenance, porting, etc.`
`5) includes: Suggested Development Strategy for RPC Applications`
`6) includes: "Notes on RPC", Draft 1, 20 feb 86`
`7) includes: "Notes on Proposed RPC Development" 18 Feb 86`
`8) includes: RPC User Manual`
`How to build and run a distributed system.`
`9) includes: Draft Specifications and Implementation Notes`
`10) includes: The RPC HELP facility`
`11) describes: THE REMOTE PROCEDURE CALL PROJECT in DD/OC`

**`Help``   ``Display``   ``Select``   ``Back``   ``Quit``   ``Mark``   ``Goto_mark``   ``Link``   ``Add``   ``Edit`**

ENQUIREの画面表示例\[17\]。
一種のリンク集になっていて "includes" や "describes" がリンクの種類を表している。
最下行はメニュバーである。

</div>

ENQUIREは広く公開することは考えられていなかった。

ENQUIREは「カード」と呼ばれるページ群からなり、各カード内にハイパーリンクがある。リンクには様々な意味と関係があり、作成者、事物、文書、グループなどがカードで表示される。リンクにおける関係は、そのリンクの必要性を知らしめるために明示されており、リンク先のカードが削除された際にそれが何だったのかを知らせる意味もある\[18\]。誰でも新たなカードを追加できるが、既存のカードからリンクする形でなければならない\[19\]。

| 関係        | 逆からみた関係      |
| --------- | ------------ |
| made      | was made by  |
| includes  | is part of   |
| uses      | is used by   |
| describes | described by |

ENQUIREは[ウェブブラウザ](../Page/ウェブブラウザ.md "wikilink")よりも以下のような点で[ウィキ](../Page/ウィキ.md "wikilink")に近い。

  - クローズドシステムの[データベース](../Page/データベース.md "wikilink")（全てのデータは総体として機能する）\[20\]
  - 双方向リンク（[ウィキペディア](https://ja.wikipedia.org/wiki/ウィキペディア "wikilink")および[MediaWiki](https://ja.wikipedia.org/wiki/MediaWiki "wikilink")では「リンク元」機能に対応）。双方向リンクはリンク対象の作者が気づかないうちに行うことができる。そのようにしてアイデアが生きてくるようになる\[21\]\[22\]。
  - サーバから直接編集可能（ウィキや[CMS](https://ja.wikipedia.org/wiki/コンテンツ管理システム "wikilink")/[ブログ](https://ja.wikipedia.org/wiki/ブログ "wikilink")と類似）\[23\]。
  - 合成が容易。特に[ハイパーリンク](../Page/ハイパーリンク.md "wikilink")を利用したとき\[24\]。

World Wide WebはCERNの既存システム群、ENQUIRE、CERNDOC、[VMS/Notes](../Page/Unix_to_Unix_Copy_Protocol.md "wikilink")、[USENETなどを統合すべく生み出された](../Page/ネットニュース.md "wikilink")\[25\]。

## 問題点

バーナーズ＝リーは1984年にCERNに復帰し、自身のシステムをよく使った\[26\]\[27\]。彼はこの「プロジェクト」にかかる時間のほとんどが情報を最新なものに更新するのに費やされることに気付いた\[28\]。ENQUIREのようなシステムは必要だが「誰でもアクセス可能」にする必要があると理解した\[29\]。双方向リンクであるため、カードを作成するときにリンク先のカードも編集する必要があり、その点が問題だった。その点を大きく変更したのが [World Wide Web](../Page/World_Wide_Web.md "wikilink") である\[30\]。バーナーズ＝リーのENQUIREは誰でも簡単に使えるシステムとはならず、似たような状況はCERNの他の部門でも発生していた\[31\]。また、既存のデータベースなどとのリンクができず、システム性能が十分でないため同時接続数が限られるという問題もあった\[32\]\[33\]。

その後の開発は行われなかった。バーナーズ＝リーはENQUIREのディスクを[ロバート・カイリュー](https://ja.wikipedia.org/wiki/ロバート・カイリュー "wikilink")に任せたが、カイリューは間もなく一時CERNを去った。カイリューの上司だった[Brian Carpenterは](https://ja.wikipedia.org/wiki/:en:Brian_Carpenter_\(Internet_engineer\) "wikilink")、ENQUIREについて詳しい人物が一人もいなくなったため、そのディスクが別の用途に流用されたのではないかとしている\[34\]。

## 技術的詳細

24行80桁のテキスト[端末](../Page/端末.md "wikilink")を入出力に使って動作する\[35\]。最初のバージョンではファイル間のハイパーリンクが可能だった\[36\]。[Pascal](../Page/Pascal.md "wikilink")で書かれており、[Norsk Data](https://ja.wikipedia.org/wiki/:en:Norsk_Data "wikilink")（ノルウェーのコンピュータ企業）製コンピュータ[NORD-10上で動作した](https://ja.wikipedia.org/wiki/:en:NORD-10 "wikilink")（OSは[SINTRAN III](https://ja.wikipedia.org/wiki/:en:SINTRAN_III "wikilink")）\[37\]\[38\]\[39\]\[40\]\[41\]。バージョン2は、[MS-DOS](../Page/MS-DOS.md "wikilink")と[VAX/VMSに](https://ja.wikipedia.org/wiki/OpenVMS "wikilink")[移植されている](https://ja.wikipedia.org/wiki/移植_\(ソフトウェア\) "wikilink")\[42\]\[43\]。

## 脚注

## 参考文献

  -
## 関連項目

  - [ザナドゥ計画](https://ja.wikipedia.org/wiki/ザナドゥ計画 "wikilink")
  - [NLS](https://ja.wikipedia.org/wiki/NLS "wikilink")
  - [インターネットの歴史](https://ja.wikipedia.org/wiki/インターネットの歴史 "wikilink")
  - [ARPANET](../Page/ARPANET.md "wikilink")
  - [World Wide Web](../Page/World_Wide_Web.md "wikilink")

## 外部リンク

  - [ENQUIRE Manual](http://infomesh.net/2001/enquire/manual/)
  - [scanned images of the Enquire Manual from 1980](http://www.w3.org/History/1980/Enquire/scaled/)

[Category:CERNのソフトウェア](https://ja.wikipedia.org/wiki/Category:CERNのソフトウェア "wikilink") [Category:コンテンツ管理システム](https://ja.wikipedia.org/wiki/Category:コンテンツ管理システム "wikilink") [Category:ハイパーテキスト](https://ja.wikipedia.org/wiki/Category:ハイパーテキスト "wikilink") [Category:インターネットの歴史](https://ja.wikipedia.org/wiki/Category:インターネットの歴史 "wikilink")

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
12.
13.
14.
15.
16.
17.
18.
19.
20.
21.
22.
23.
24.
25.
26.
27.
28.
29.
30.
31.
32.
33.
34.
35.
36.
37.
38.
39.
40.
41.
42.
43.
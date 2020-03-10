> この記事は[Debian](https://ja.wikipedia.org/wiki/Debian)から翻訳されています。


**Debianフリーソフトウェアガイドライン** (*Debian Free Software Guideline*、**DFSG**) は、ソフトウェアライセンスが、[Debian](../Page/Debian.md "wikilink")の一部として含めることが可能な[フリーソフトウェアライセンス](https://ja.wikipedia.org/wiki/フリーソフトウェアライセンス "wikilink")であるかどうか判定するためにDebianプロジェクトが使用しているガイドラインの集合である。DFSGは[Debian社会契約](https://ja.wikipedia.org/wiki/Debian社会契約 "wikilink")の一部である。

## ガイドライン

1.  自由な再頒布が可能であること。
2.  ソースコードを入手可能であること。
3.  改変や派生作品の作成が認められていること。
4.  差分が提供される場合はソースコードの同一性を要求してもかまわない ([TeX](../Page/TeX.md "wikilink")などのための妥協案)。
5.  人や団体を差別しないこと。
6.  適用領域による差別 (商用利用の禁止など) をしないこと。
7.  プログラムの再配布時に追加ライセンスを必要としないこと。
8.  ライセンスはDebianだけに限られてはならない。基本的に前項の繰り返し。
9.  ライセンスは同梱される他のソフトウェアの邪魔をしないこと。
10. [GPL](../Page/GNU_General_Public_License.md "wikilink")、[BSD](https://ja.wikipedia.org/wiki/BSDライセンス "wikilink")、[Artisticライセンスなどがフリーと考えられるライセンスの例である](https://ja.wikipedia.org/wiki/Artistic_License "wikilink")。

## 歴史

最初のDFSGは、最初のバージョンの[Debian社会契約](https://ja.wikipedia.org/wiki/Debian社会契約 "wikilink")ともに1997年7月に発行された\[1\]。主要な著者は[ブルース・ペレンズ](../Page/ブルース・ペレンズ.md "wikilink")と当時の他のDebian開発者数人であった。

[1998年](https://ja.wikipedia.org/wiki/1998年 "wikilink")11月、[イアン・ジャクソン](https://ja.wikipedia.org/wiki/イアン・ジャクソン "wikilink")らは草案のバージョン1.4でいくつかの変更を提案したが、変更は決して公式にはならなかった。ジャクソンは「あいまいな言い回し」とパッチ条項に問題があったと述べてる\[2\]。

[2007年](../Page/2007年.md "wikilink")現在、文書は一度も改訂されていない。とは言うものの、DFSGに影響を与える社会契約の変更はなされたことがある。

"Editorial amendments to the social contract"と題されたDebian一般決議 2004-003\[3\]は、社会契約を変更した。提案者のアンドリュー・サフィールドは、変更されたのは文面だけであって意味は変更されていないと述べた\[4\]。

しかしながら、文*We promise to keep the Debian GNU/Linux Distribution entirely free software*を*We promise that the Debian system and all its components will be free*と変更した結果として、リリースマネージャの[アンソニー・タウンズ](https://ja.wikipedia.org/wiki/アンソニー・タウンズ "wikilink")はDebianがDFSG適合を要求するのはソフトウェアに限られなくなったと解釈し、実際上の変更を行った\[5\]。

これがもう一つの一般決議である2004-004を促した\[6\]。開発者たちはその動議に圧倒的な反対票を投じ、それらの変更を次期リリース (その開発が1年後の2005年6月に始まった) まで先延ばしにすることを決議した。

## 適用

### ソフトウェア

DFSGに関するほとんどの議論は*debian-legal*メーリングリスト上で起きている。Debian開発者が最初にDebianへ含めるためのパッケージをアップロードするとき、*ftpmaster*チームがソフトウェアライセンスを調べ、社会契約に合致しているかどうかを判定する。難しいケースでは、チームはdebian-legalメーリングリストと協議することもある。

### ソフトウェア以外の内容

DFSGはソフトウェアに焦点を当てているが、[2004年](../Page/2004年.md "wikilink")6月、Debianプロジェクトは同じ原則を[ソフトウェア文書](https://ja.wikipedia.org/wiki/ソフトウェア文書 "wikilink")、マルチメディアデータおよび他の内容にも適用し始めると決定した。Debianのソフトウェア以外の内容はDebian 4.0 (2007年4月にリリース) およびそれ以降のリリースから、より厳格にDFSGへ適合し始める。

### GFDL

[GNUロジェクト](../Page/GNUプロジェクト.md "wikilink")、[Linux Documentation Project](https://ja.wikipedia.org/wiki/Linux_Documentation_Project "wikilink")、その他によって書かれ、[GNU Free Documentation Licenseの下にライセンスされている多くの文書は不可変更部分を含んでおり](../Page/GNU_Free_Documentation_License.md "wikilink")、そのためDFSGに適合しない。この表明は長い議論の最終結果であり、一般決議 2006-001となった\[7\]。

GFDLの不可変更部分のために、Debianの内容のごく一部はDFSGに適合していないとみられている。

### マルチメディアファイル

マルチメディアファイルのソースとは何から構成されるのか、たとえば圧縮する前の画像ファイルは圧縮画像のソースなのか、レイトレーシング前の3Dモデルはそのレンダリング結果のソースなのか、などに関しては議論がある。

## debian-legalによるDFSG適合テスト

*debian-legal*メーリングリストの参加者はライセンスがDFSGに適合するかどうかチェックするため、いくつかのテストを作成した。テストの内容については[\#外部リンク](https://ja.wikipedia.org/wiki/#外部リンク "wikilink")のDFSG FAQ草案を参照されたい。

## 脚注

<references/>

## 関連項目

  - [フリーソフトウェアの定義](https://ja.wikipedia.org/wiki/フリーソフトウェアの定義 "wikilink")
  - [オープンソースの定義](https://ja.wikipedia.org/wiki/オープンソースの定義 "wikilink")
  - [フリーソフトウェアの歴史](https://ja.wikipedia.org/wiki/フリーソフトウェアの歴史 "wikilink")

## 外部リンク

  - [Debian 社会契約とDebian フリーソフトウェアガイドライン](http://www.debian.org/social_contract#guidelines)
  - [debian-legalメーリングリスト、過去の議論のアーカイブを含む](http://lists.debian.org/debian-legal/)
  - [DFSG FAQ草案](http://people.debian.org/~bap/dfsg-faq.html) (英語)
  - [Section A.1.3 of *Why OSS/FS? Look at the Numbers\!*](http://www.dwheeler.com/oss_fs_why.html#other-license-issues) debian-legalメーリングリストで議論された主要な問題のいくつか (英語)
  - [現在Debianに見られるソフトウェアライセンスの一覧](http://www.debian.org/legal/licenses/)

[Category:Debian](https://ja.wikipedia.org/wiki/Category:Debian "wikilink") [Category:Linux](https://ja.wikipedia.org/wiki/Category:Linux "wikilink") [Category:オープンソース文化・運動](https://ja.wikipedia.org/wiki/Category:オープンソース文化・運動 "wikilink") [Category:フリーソフトウェア文化・運動](https://ja.wikipedia.org/wiki/Category:フリーソフトウェア文化・運動 "wikilink")

1.
2.  Ian Jackson: [Draft new DFSG](http://lists.debian.org/debian-devel/1998/11/msg01944.html)、debian-develメーリングリスト
3.  [General Resolution: Editorial amendments to the social contract](http://www.debian.org/vote/2004/vote_003)
4.  Andrew Suffield: [Re: Candidate social contract amendments (part 1: editorial) (3rd draft)](http://lists.debian.org/debian-vote/2004/01/msg00692.html)、debian-voteメーリングリスト
5.  Anthony Towns: [Social Contract GR's Affect on sarge](http://lists.debian.org/debian-devel/2004/04/msg01929.html), debian-devel mailing list
6.  [General Resolution: Sarge Release Schedule in view of GR 2004-003](http://www.debian.org/vote/2004/vote_004)
7.  [一般決議: 何故 GNU Free Documentation License は Debian main に不適切なのか](http://www.debian.org/vote/2006/vote_001)
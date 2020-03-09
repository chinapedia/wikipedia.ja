> この記事は[Vine Linux](https://ja.wikipedia.org/wiki/Vine_Linux)から翻訳されています。


**Vine Linux**（ヴァイン・リナックス）は、[RPM系の日本国産](https://ja.wikipedia.org/wiki/RPM_Package_Manager "wikilink")[Linuxディストリビューション](../Page/Linuxディストリビューション.md "wikilink")である。1998年に[PJEのメンバーを主体として開発が始まった](https://ja.wikipedia.org/wiki/Project-JE "wikilink")。以前は[Red Hat Linuxの派生であったが](../Page/Red_Hat_Linux.md "wikilink")、バージョン3.0からはProject Vineのメンバーを中心に独自に開発が進められている\[1\]。開発版の名称は VineSeed。各バージョンのコードネームは[ワイン](../Page/ワイン.md "wikilink")の名称から採られている\[2\]。[Linux Standard Baseには準拠していない](https://ja.wikipedia.org/wiki/Linux_Standard_Base "wikilink")\[3\]。

## 特徴

1990年代後半、海外製のLinuxディストリビューションがまだ日本語にまともに対応していなかった時代に登場したVine Linuxは、日本語をそのままで扱うことができるようになった日本語対応のLinuxディストリビューションの先駆けの一つである\[4\]。 2001年頃まで日本語環境を必要とするユーザに人気があった\[5\]。しかし、Linuxが広まるにつれて、[Fedora](../Page/Fedora.md "wikilink")や[Ubuntu](https://ja.wikipedia.org/wiki/Ubuntu "wikilink")などの初心者にやさしくなったディストリビューションが登場し、それらのディストリビューションが人気になった。\[6\]\[7\]\[8\]

開発はProject Vineを中心に行われており、皆が自分の欲しいOSを作っている\[9\]\[10\]。

他のメジャーなディストリビューションに比べセキュリティー上の問題の修正が遅い場合もある<ref>例えば次のような例。

  - [CVE-2007-4572](http://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2007-4572)([samba](https://ja.wikipedia.org/wiki/samba "wikilink")の脆弱性)では[DebianやRed Hatに比べ修正まで一週間近くかかっている。](http://vinelinux.org/errata/4x/20071125-2.html)
  - [CVE-2007-4730](http://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2007-4730)([X.Org](https://ja.wikipedia.org/wiki/X.Org "wikilink")の脆弱性)では[DebianやRed Hatに比べ修正まで二ヶ月以上かかっている。](http://vinelinux.org/errata/4x/20071211-2.html)
  - [CVE-2006-5752](http://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2006-5752)/ [CVE-2007-1863](http://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2007-1863)/[CVE-2007-3304](http://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2007-3304)([apache2](https://ja.wikipedia.org/wiki/apache2 "wikilink")の脆弱性)では[DebianやRed Hatに比べ修正まで一ヶ月以上かかっている。](http://vinelinux.org/errata/4x/20070925-2.html)</ref>。

他には、[Emacs](../Page/Emacs.md "wikilink") 、[](../Page/LaTeX.md "wikilink") の日本語環境などのデフォルト設定、[プログラミング環境](https://ja.wikipedia.org/wiki/プログラミング_\(コンピュータ\) "wikilink")（[GCC](../Page/GNUコンパイラコレクション.md "wikilink") など）、[JM Projectの日本語](https://ja.wikipedia.org/wiki/JM_Project "wikilink")[マニュアルの採用という特徴がある](https://ja.wikipedia.org/wiki/ソフトウェアドキュメンテーション "wikilink")。また、Project Vineメンバーが開発している[VLゴシック](https://ja.wikipedia.org/wiki/VLゴシック "wikilink")フォントファミリが標準で採用されている。

## サポート

セキュリティに関してはVine Linux Security Watch Teamが対応しており、修正プログラムは原則としてそのバージョンの次のメジャーバージョンリリースから1年後まで提供される\[11\]。

修正パッケージはソフトウェアのバージョンアップではなく不具合箇所の修正のみを行うことが基本方針となっている\[12\]。これは、セキュリティ上の修正のためにソフトウェアの挙動が変更されてしまう問題を起こさないためである。

マイナーバージョン同士では大きな変更がされていないために修正パッケージが共用できる可能性が高いが、バージョンアップが推奨されている。これは、新しいマイナーバージョン環境\[13\]で修正パッケージを作成しているためである。

バージョン6.xよりppc(PowerPC搭載のMacintosh)は対応アーキテクチャから外された\[14\]。

## VinePlus

Vine Linuxには、VinePlusというVine Linux対応のRPMパッケージが存在する。VinePlusについてもProject Vineが管理するサーバで配布されているが、Vine Linuxをアップグレードした場合に動作しなくなる可能性があるなど、利用者の自己責任で利用する必要があるRPMパッケージ群である。

過去には、VinePlusにあるRPMパッケージのインストールに必要なパッケージがサーバに置かれていないという事例も存在した\[15\]。

バージョン3.0からは、VinePlusは細分化された。過去にあったVinePlusのうちメンテナが不在でメンテナンス頻度が極度に低いパッケージはextrasやorphanedというリポジトリに分離された。これらのパッケージもapt-getを使ってインストールすることもできるが、そのためには利用者がaptの設定ファイルを書き換える必要がある。

VinePlusは原則としてFHS 2.3には準拠しておらず、FSSTND1.2に準拠している\[16\]。

[特許](https://ja.wikipedia.org/wiki/特許 "wikilink")が取得されている機能を実装しているソフトウェアのように、使用に制限があるソフトウェア\[17\]をVine Linuxで利用するためには利用者自身がインストールする必要がある。VinePlusでは、それらのソフトウェアのRPMパッケージを作成するためのSRPMパッケージをnonfreeリポジトリに用意している。

## 主要なバージョンの一覧表

Vine Linuxの主要なバージョンにはコードネームがつけられており、VinePlusなどのパッケージやサポート期限もそれに応じて用意される。

| バージョン     | コードネーム               | リリース日           | サポート期限                   |
| --------- | -------------------- | --------------- | ------------------------ |
| 1.0       | Nahe                 | 1999年3月28日      | 2000年1月11日（サポート終了）       |
| 1.1       | Rheingau             | 1999年6月4日       | 2000年1月11日（サポート終了）       |
| 2.0       | Sociando-Mallet      | 2000年4月14日      | 2003年4月7日（サポート終了）        |
| 2.1       | Cissac               | 2000年11月4日      | 2003年4月7日（サポート終了）        |
| 2.1.5     | Calon-Segur          | 2001年3月24日      | 2003年4月7日（サポート終了）        |
| 2.5       | Domaine de Chevalier | 2002年4月15日      | 2006年2月28日（サポート終了）       |
| 2.6       | La Fleur de Bouard   | 2002年10月25日     | 2006年2月28日（サポート終了）       |
| 3.0       | Valandraud           | 2004年8月2日       | 2007年11月22日（サポート終了）      |
| 3.1       | Pichon Lalande       | 2004年11月26日     | 2007年11月22日（サポート終了）      |
| 3.2       | Ducru Baucaillou     | 2005年9月18日      | 2007年11月22日（サポート終了）      |
| 4.0       | Latour               | 2006年11月22日     | 2010年8月23日（サポート終了）       |
| 4.1       | Cos d'Estournel      | 2007年2月22日      | 2010年8月23日（サポート終了）       |
| 4.2       | Lynch Bages          | 2007年12月25日     | 2010年8月23日（サポート終了）       |
| 5.0       | Lafite               | 2009年8月24日      | 2012年8月6日\[18\]（サポート終了）  |
| 5.1       | Cheval Blanc         | 2010年2月26日      | 2012年8月6日（サポート終了）        |
| 5.2       | Palmer               | 2010年11月30日     | 2012年8月6日（サポート終了）        |
| 6.0       | Haut Brion           | 2011年8月6日       | 未定\[19\]                 |
| 6.1       | Pape Clement         | 2012年7月30日      | 未定\[20\]                 |
| 6.2       | Haut Bailly          | 2013年10月16日     | 未定\[21\]                 |
| 6.3       | Malartic Lagraviere  | 2015年2月26日      | 未定\[22\]                 |
| 6.5\[23\] | Poupille             | 2017年4月3日       | 未定\[24\]（現在のリリース） \<\!-- |
| 7.0       | ?                    | 20XX年X月X日\[25\] | 未定 --\>                  |

Vine Linuxのリリース履歴

## 関連項目

  - [PJE](https://ja.wikipedia.org/wiki/Project-JE "wikilink")
  - [日本のLinux開発](https://ja.wikipedia.org/wiki/日本のLinux開発 "wikilink")

## 脚注

### 注釈

### 出典

## 外部リンク

  - [Vine Linux ホームページ](http://vinelinux.org/)
  - [Vine Linux ユーザーフォーラム | Google グループ](https://groups.google.com/group/vine-users-forum?hl=ja)
  - [VineLinux-FAQ - 2ch-Linux-Beginners](http://www12.atwiki.jp/linux2ch/pages/34.html) (日本語FAQ集)
  - [DistroWatch.com: Vine Linux](http://distrowatch.com/table.php?distribution=vine)

[Category:Linuxディストリビューション](https://ja.wikipedia.org/wiki/Category:Linuxディストリビューション "wikilink") [Category:日本のLinux開発](https://ja.wikipedia.org/wiki/Category:日本のLinux開発 "wikilink") [Category:1999年のソフトウェア](https://ja.wikipedia.org/wiki/Category:1999年のソフトウェア "wikilink")

1.  [Vine Linux 3.0の特徴 (その1) (1/2)](http://www.itmedia.co.jp/enterprise/articles/0409/10/news052.html)
2.  ただし、名称になったのは2.0以降。1.0と1.1は産地から採られている。
3.  <https://www.linuxfoundation.org/lsb-cert/productdir.php?by_prod>
4.  [『Vine Linux 1.0』がリリース](http://ascii.jp/elem/000/000/300/300096/)
5.  [＠IT：リアルタイムアンケート集計結果 使用ディストリビューションは？](http://www.atmarkit.co.jp/flinux/survey/vote/resultold.html#00)
6.  [Fedora、ライブCDをリリース](http://sourceforge.jp/magazine/07/01/16/0125207)
7.  [Open Tech Press | Ubuntu 7.10は秀逸なリリース](http://sourceforge.jp/magazine/07/10/29/018206)
8.  [Ubuntu Linuxが注目される理由](http://www.atmarkit.co.jp/news/analysis/200710/22/ubuntu.html)
9.  [Vineのメンバー一覧](http://vinelinux.org/projectvine.html)
10. [みんなが自分の欲しいOSを作っているんです - Project Vine 代表 鈴木大輔氏](http://itpro.nikkeibp.co.jp/article/COLUMN/20130516/477303/)
11. [Vine Linux - セキュリティチーム](http://vinelinux.org/securityteam.html)、5.0より変更
12. この方針は[Red Hat Enterprise Linuxや](https://ja.wikipedia.org/wiki/Red_Hat_Enterprise_Linux "wikilink")[Debian](../Page/Debian.md "wikilink")などと同様。
13. バージョン3.xの場合はバージョン3.2
14. [Vine Linux 6.x の制限事項](http://vinelinux.org/docs/vine6/install-guide/restriction.html)
15. [vine-users:069713 Re: arts-develのインストール](http://search.luky.org/vine-users.6/msg09713.html)
16. [VinePlus のパッケージングルール (暫定版)](http://www.vinelinux.org/vineplus.html#rule)
17. [FFmpeg](https://ja.wikipedia.org/wiki/FFmpeg "wikilink")や[LAME](https://ja.wikipedia.org/wiki/LAME "wikilink")、[DVD-Video](../Page/DVD-Video.md "wikilink")の[CSSを扱うlibdvdcssなど](../Page/Content_Scramble_System.md "wikilink")
18.
19.
20.
21.
22.
23.
24.
25.
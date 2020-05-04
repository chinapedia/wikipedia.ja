> この記事は[AntiX](https://ja.wikipedia.org/wiki/AntiX)から翻訳されています。


**antiX** は [Debian](../Page/Debian.md "wikilink")\[1\]安定版を元にして直接ビルドされた[Linuxディストリビューション](../Page/Linuxディストリビューション.md "wikilink")である。このディストリビューションは動作が比較的軽量であるため、仕様の古くなったコンピューターでの利用に適している。しかも、[APT](../Page/APT.md "wikilink")とDebian互換の[リポジトリ](../Page/リポジトリ.md "wikilink")\[2\]を利用したアップデートおよび、最新の[Linuxカーネル](../Page/Linuxカーネル.md "wikilink") とアプリケーションを提供する。

## システム要件

  - 推奨値: 256 MB の RAM と 1 GB のハードディスク空き容量。
  - 最小値: 128 MB の RAM と 1 GB のハードディスク空き容量。
  - インストールする場合: 2.7 GB のハードディスク空き容量。\[3\]

標準的な[ライブ](https://ja.wikipedia.org/wiki/LiveCD "wikilink")・リリースの他に、antiX の他のバージョン（ベースとコア）が利用可能で、もっと少ない RAM容量とハードドライブ容量、および全体的なハードウェアの制限下でインストールすることができる。

## バージョン

[AntiXonTatung5213.jpg](https://ja.wikipedia.org/wiki/File:AntiXonTatung5213.jpg "fig:AntiXonTatung5213.jpg") TWN-5213 CU.\]\] antiX は、[IA-32](../Page/IA-32.md "wikilink") および [x86-64](https://ja.wikipedia.org/wiki/x86-64 "wikilink") アーキテクチャ向けが用意されており、それぞれ３種類のバージョン（フレーバー）が存在する\[4\]:

  - **フル(Full)**, これは可能な限りのアプリケーションをインストールできる。AntiX フルバージョンは、必要なソフトウェアがすべてプリインストールされたフレーバーである。他に用意されているフレーバーと比較して、サイズが大きくなっている。AntiX フルバージョンには、4つのウィンドウマネージャ、つまり iceWM や Fluxbox、jwm、herbstluftwm が付属している\[5\]。
  - **ベース(Base)**, これは、ユーザーが独自にアプリケーションを組み合わせてインストールすることが可能である。AntiX base はベースシステムを含む。フルフレーバーに含まれる4つのウィンドウマネージャが全て付属する\[6\]。
  - **コア（Core-libre）**, これは、ユーザーが自分の意志で完全に自由なインストールを行えるようにするものである。AntiX core はコアシステムのみである。ウィンドウマネージャなし、CLIインストール、UEFIサポートなし、暗号化サポートなしであるが、ほとんどのワイヤレスに対応しており、サイズ的には非常に小さい\[7\]。

これらの 3 つのバージョンは、2014年、[MEPIS](../Page/MEPIS.md "wikilink") コミュニティと協力して開発された antiX MX で合流した。デフォルトのデスクトップ環境として [Xfce](../Page/Xfce.md "wikilink") を使用しており、 [Debian](../Page/Debian.md "wikilink")安定版を直接ベースにしているためにとりわけ安定性が高く、中規模のフットプリントから堅実なパフォーマンスを発揮する。2016年11月現在、 [MX Linux](../Page/MX_Linux.md "wikilink") は DistroWatch で[１個の独立したディストリビューション](http://distrowatch.com/table.php?distribution=mx)立したディストロとしてリストアップされるようになった。\[8\]

## リリースの歴史

antiX は Linux ディストリビューションの１つでで、元々は MEPIS をベースにしており、それ自体は Debian安定版のディストリビューションをベースにしている。当初は MEPIS [KDE](../Page/KDE.md "wikilink") デスクトップ環境を [Fluxbox](../Page/Fluxbox.md "wikilink") と [IceWM](../Page/IceWM.md "wikilink") ウィンドウマネージャに置き換えたもので、古くて、あまりパワーのない x86 ベースのシステムに適するものとして開発された。Debian とは異なり、antiX は [systemd](https://ja.wikipedia.org/wiki/systemd "wikilink") フリーである。\[9\]

| バージョン\[10\]           | （開発用の）コードネーム         | リリースされた日    |
| --------------------- | -------------------- | ----------- |
| 6.5\[11\]             | Spartacus            | 2007年7月9日   |
| 7.0\[12\]\[13\]       | Lysistrata           | 2007年10月30日 |
| 7.2\[14\]\[15\]       | Vetëvendosje         | 2008年5月16日  |
| 7.5\[16\]\[17\]       | Toussaint Louverture | 2008年8月24日  |
| 8.0\[18\]\[19\]       | Intifada\!           | 2009年2月14日  |
| 8.2\[20\]\[21\]\[22\] | Tȟašúŋke Witkó       | 2009年7月24日  |
| 8.5\[23\]             | Marek Edelman        | 2010年4月12日  |
| M11\[24\]\[25\]       | Jayaben Desai        | 2011年5月3日   |
| 12\[26\]\[27\]\[28\]  | Edelweißpiraten      | 2012年8月7日   |
| 13\[29\]\[30\]        | Luddite              | 2013年7月2日   |
| MX-14.4               | Symbiosis            | 2015年3月23日  |
| 15\[31\]\[32\]        | Killah P             | 2015年6月30日  |
| MX-15                 | Fusion               | 2015年12月24日 |
| 16\[33\]              | Berta Cáceres        | 2016年6月26日  |
| 17\[34\]              | Heather Heyer        | 2017年10月24日 |
| 17.1\[35\]            | Heather Heyer        | 2018年3月18日  |
| 17.2\[36\]            | Helen Keller         | 2018年10月5日  |
| 17.4.1\[37\]          | Helen Keller         | 2019年3月28日  |
| 19\[38\]              | Marielle Franco      | 2019年10月17日 |
| 19.1\[39\]            |                      | 2019年12月23日 |
| 19.2\[40\]            | Hannie Schaft        | 2020年3月28日  |

## 関連項目

  - [MX Linux](../Page/MX_Linux.md "wikilink")
  - [MEPIS](../Page/MEPIS.md "wikilink")
  - [Debian GNU/Linux](https://ja.wikipedia.org/wiki/Debian_GNU/Linux "wikilink")

## リファレンス

## 外部リンク

  -
  - [antiX フォーラム](https://www.antixforum.com/)

  - [antiX on OpenSourceFeed gallery](http://www.opensourcefeed.org/distribution/antix)

[Category:Debian派生ディストリビューション](https://ja.wikipedia.org/wiki/Category:Debian派生ディストリビューション "wikilink") [Category:Linuxディストリビューション](https://ja.wikipedia.org/wiki/Category:Linuxディストリビューション "wikilink")

1.
2.
3.  [10 Best Lightweight Linux Distributions For Older Computers In 2018 With System Requirements](https://itsfoss.com/lightweight-linux-beginners/)
4.
5.
6.
7.
8.   MX Community|access-date=2018-07-04|archive-url=[https://web.archive.org/web/20190207130102/https://mxlinux.org/history|archive-date=2019-02-07|url-status=dead](https://web.archive.org/web/20190207130102/https://mxlinux.org/history%7Carchive-date=2019-02-07%7Curl-status=dead)}}
9.
10. [AntiX announcements on DistroWatch.com](https://distrowatch.com/index.php?distribution=antix)
11. [Distribution Release: antiX 6.5 (DistroWatch.com News)](https://distrowatch.com/?newsid=04341)
12. [Distribution Release: antiX 7.0 (DistroWatch.com News)](https://distrowatch.com/?newsid=04562)
13. [AntiX Lysistrata 7.0 Available Now\!](http://news.softpedia.com/news/AntiX-Lysistrata-7-0-Available-Now-69446.shtml)
14. [Distribution Release: antiX 7.2 (DistroWatch.com News)](https://distrowatch.com/?newsid=04893)
15. [AntiX 7.2 Revives Your Antique Computer](http://news.softpedia.com/news/AntiX-7-2-Revives-Your-Antique-Computer-85803.shtml)
16. [Distribution Release: antiX 7.5 (DistroWatch.com News)](https://distrowatch.com/?newsid=05049)
17. [AntiX 7.5 Released](http://news.softpedia.com/news/AntiX-7-5-Released-92405.shtml)
18. [Fast and Light AntiX is Released | MEPIS Linux](http://www.mepis.org/node/128)
19. [Available Now: AntiX MEPIS 8.0 (Intifada)](http://news.softpedia.com/news/Available-Now-AntiX-MEPIS-8-0-Intifada-104588.shtml)
20. [Antix Team does it again with AntiX 8.2 Final | MEPIS Linux](http://www.mepis.org/node/124)
21. [Distribution Release: antiX 8.2 (DistroWatch.com News)](https://distrowatch.com/?newsid=05592)
22. [AntiX MEPIS 8.2 Released](http://news.softpedia.com/news/AntiX-MEPIS-8-2-Released-117562.shtml)
23. [Distribution Release: antiX 8.5 (DistroWatch.com News)](https://distrowatch.com/?newsid=06011)
24. [antiX-M11 'Jayaben Desai' released - antiX Forum](https://www.tapatalk.com/groups/antix/antix-m11-released-t3084.html)
25. [DistroWatch Weekly, Issue 434, 5 December 2011](https://distrowatch.com/weekly.php?issue=20111205#feature)
26. [Old News - antiX](http://antix.mepis.org/index.php?title=Old_News)
27. [Distribution Release: antiX 12 (DistroWatch.com News)](https://distrowatch.com/?newsid=07377)
28. [A distribution for less-powerful systems: antiX-12 \[LWN.net](https://lwn.net/Articles/511227/)\]
29. [Distribution Release: antiX 13.2 (DistroWatch.com News)](https://distrowatch.com/?newsid=08144)
30. [Give that old computer a boost with antiX Linux](http://www.everydaylinuxuser.com/2013/12/give-that-old-computer-boost-with-antix.html) , **Everyday Linux User**
31. [Distribution Release: antiX 15 (DistroWatch.com News)](https://distrowatch.com/?newsid=09000)
32. [DistroWatch Weekly, Issue 622, 10 August 2015](https://distrowatch.com/weekly.php?issue=20150810#antix)
33. [Distribution Release: antiX 16 (DistroWatch.com News)](https://distrowatch.com/?newsid=09456)
34. [antiX-17 released – antiX Linux](https://antixlinux.com/antix-17-released/)
35. [antiX-17.1 released – antiX Linux](https://antixlinux.com/antix-17.1-released/)
36.
37.
38.
39.
40.
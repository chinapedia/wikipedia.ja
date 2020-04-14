> この記事は[Common Desktop Environment](https://ja.wikipedia.org/wiki/Common_Desktop_Environment)から翻訳されています。


**Common Desktop Environment**(「共通デスクトップ環境」の意、**CDE**と略記)は、[UNIX](../Page/UNIX.md "wikilink")および[OpenVMS](../Page/OpenVMS.md "wikilink")用の[デスクトップ環境](https://ja.wikipedia.org/wiki/デスクトップ環境 "wikilink")である。商用UNIXワークステーションにおけるデスクトップ環境として、かつて標準の地位にあった。

GUIツールキット[Motifをさらに拡張したものである](../Page/Motif_\(GUI\).md "wikilink")。2012年に[オープンソース](../Page/オープンソース.md "wikilink")化された。

## 歴史

CDE は[1993年](../Page/1993年.md "wikilink")6月、[ヒューレット・パッカード](../Page/ヒューレット・パッカード.md "wikilink") (HP)、[IBM](../Page/IBM.md "wikilink")、[USL](https://ja.wikipedia.org/wiki/UNIX_Systems_Laboratories "wikilink")、[サン・マイクロシステムズ](../Page/サン・マイクロシステムズ.md "wikilink")が [Common Open Software Environment](../Page/Common_Open_Software_Environment.md "wikilink") (COSE) イニシアチブの協業の一環として共同開発することを発表した。ベースとなったのは、HPの  (Visual User Environment) である。VUE自体は  (mwm) から派生している。IBMは [Common User Access](../Page/Common_User_Access.md "wikilink") モデルと[ワークプレース・シェル](https://ja.wikipedia.org/wiki/ワークプレース・シェル "wikilink")を提供した。[ノベルは](../Page/ノベル_\(企業\).md "wikilink") [UNIX System V](../Page/UNIX_System_V.md "wikilink") からデスクトップマネージャの部品とスケーラブルシステム技術を提供した。Sunは  環境から  というアプリケーション連携フレームワークと  という生産性ツールを提供した（メールクライアントやカレンダークライアントなど）\[1\]。

[1994年](../Page/1994年.md "wikilink")[3月](https://ja.wikipedia.org/wiki/3月 "wikilink")、CDEの管理は [Open Software Foundation](../Page/Open_Software_Foundation.md "wikilink") と [UNIX International](https://ja.wikipedia.org/wiki/UNIX_International "wikilink") が合併した新たなOSFが受け持つこととなり\[2\]、[1995年](https://ja.wikipedia.org/wiki/1995年 "wikilink")[9月](../Page/9月.md "wikilink")、MotifとCDEを1つのプロジェクトとしたCDE/Motifが発表された\[3\]。[1996年](../Page/1996年.md "wikilink")にはOSFが新たに結成された[The Open Groupの一部となっている](../Page/The_Open_Group.md "wikilink")\[4\]。

[2000年](../Page/2000年.md "wikilink")頃まで、CDEはUNIXデスクトップの[デファクトスタンダード](../Page/デファクトスタンダード.md "wikilink")とみなされていたが、[KDE](../Page/KDE.md "wikilink")や[GNOME](../Page/GNOME.md "wikilink")といった[フリーソフトウェア](../Page/フリーソフトウェア.md "wikilink")のデスクトップ環境が急速に成長して[Linux](../Page/Linux.md "wikilink")プラットフォームで広く使われるようになった。その当時、既にLinuxは全商用UNIXよりも広く使われていたのである。[レッドハット](../Page/レッドハット.md "wikilink")はLinuxベンダーとしては唯一CDEを移植していたが、KDEやGNOMEに押されて消えていった。

[2001年](../Page/2001年.md "wikilink")、商用UNIXベンダーであるサン・マイクロシステムズ ([Solaris](../Page/Solaris.md "wikilink")) は、[ワークステーション](../Page/ワークステーション.md "wikilink")の標準デスクトップとしてCDEを段階的に廃止してGNOMEに移行することを発表した。2005年初めにリリースされたSolaris 10にはCDEとGNOMEベースの [Java Desktop System](https://ja.wikipedia.org/wiki/Java_Desktop_System "wikilink") が含まれている。2011年11月リリースのSolaris 11にはデスクトップ環境としてはGNOMEのみがあり、MotifやTooltalkといったCDE関連ライブラリもバイナリ互換性のために残っている。また[OpenSolaris](../Page/OpenSolaris.md "wikilink")プロジェクトではCDEをオープンソース化することはないと言明した\[5\]。

[HPの](../Page/ヒューレット・パッカード.md "wikilink")[OpenVMS](../Page/OpenVMS.md "wikilink")では、標準のデスクトップ環境としてCDEを採用している。

Motifは2000年に [Open Motif](../Page/Motif_\(GUI\).md "wikilink") としてリリースされたが、その "revenue sharing" ライセンスは[オープンソースとしての定義には完全には合致しないし](https://ja.wikipedia.org/wiki/オープンソースの定義 "wikilink")、[フリーソフトウェアとしての定義にも合致しない](https://ja.wikipedia.org/wiki/フリーソフトウェアライセンス "wikilink")。[The Open Groupはこれをオープンソース化したいと考えているが](../Page/The_Open_Group.md "wikilink")、十分にできているとは言えない\[6\]。2006年、The Open Groupに対してCDEとMotifの[ソースコード](../Page/ソースコード.md "wikilink")をフリーなライセンスで公開してほしいという請願がなされた\[7\]。

[Xfce](../Page/Xfce.md "wikilink")デスクトップは一時期[ルック・アンド・フィール](../Page/ルック・アンド・フィール.md "wikilink")をCDEに似せていたが、既に変更された。

CDE のオープンソース版を独自に開発するプロジェクトOpenCDEが2010年に始まった。CDEのソースコードを全く使わずに、CDEの[ルック・アンド・フィール](../Page/ルック・アンド・フィール.md "wikilink")、構成、機能を再現することを目的としている\[8\]。

[2012年](../Page/2012年.md "wikilink")[8月6日](../Page/8月6日.md "wikilink")、[LGPLv2でオープンソース化され公開された](../Page/GNU_Lesser_General_Public_License.md "wikilink")\[9\]。

## CDE を使っているオペレーティングシステム

  - [AIX](../Page/AIX.md "wikilink") ([IBM](../Page/IBM.md "wikilink"))
  - [Digital UNIX](../Page/Tru64_UNIX.md "wikilink") / [Tru64 UNIX](../Page/Tru64_UNIX.md "wikilink") （[DEC](../Page/ディジタル・イクイップメント・コーポレーション.md "wikilink")、現[HP](../Page/ヒューレット・パッカード.md "wikilink")）
  - [HP-UX](../Page/HP-UX.md "wikilink") （[HP](../Page/ヒューレット・パッカード.md "wikilink")） - version 10.10 以降\[10\]
  - [OpenVMS](../Page/OpenVMS.md "wikilink") （DEC、現HP）
  - [Solaris](../Page/Solaris.md "wikilink") （[サン・マイクロシステムズ](../Page/サン・マイクロシステムズ.md "wikilink")） - アドオンとして2.3から導入。2.6から10までは標準。
  - [UnixWare](../Page/UnixWare.md "wikilink") （）
  - [IRIX](../Page/IRIX.md "wikilink") （[SGIは一時期](../Page/シリコングラフィックス.md "wikilink")、独自デスクトップ環境の代替としてCDEを提供したことがある）

## CDEプロジェクトの下での開発

[2014年](../Page/2014年.md "wikilink")3月、[フリーソフトウェア](../Page/フリーソフトウェア.md "wikilink")となってからの初めてのCDEの安定版（2.2.1）がリリースされた\[11\]。

バージョン2.2.2（[2014年](../Page/2014年.md "wikilink")7月リリース）から、CDEは[FreeBSD](../Page/FreeBSD.md "wikilink") 10において、デフォルトの[Clang](https://ja.wikipedia.org/wiki/Clang "wikilink")コンパイラでコンパイルすることが可能である\[12\]。

バージョン2.3.0（[2018年](../Page/2018年.md "wikilink")7月リリース）から、CDEは[Linux](../Page/Linux.md "wikilink")でTIRPIを利用するようになり、insecure modeで実行するためにポートマッパーとrpcbindは必要とされなくなった。また、Xprintはもう使われておらず、[BSD](../Page/BSD.md "wikilink")において最初に[Motifのカスタム版をインストールすることなくコンパイルすることができる](../Page/Motif_\(GUI\).md "wikilink")。複数ディスプレイは[Xinerama](../Page/Xinerama.md "wikilink")によってサポートが改善されている。

フリーソフトウェアとしてリリースされてから、CDEは下記のシステムに移植された\[13\]。

  - [Linuxディストリビューション](../Page/Linuxディストリビューション.md "wikilink")
      - [Debian GNU/Linux](https://ja.wikipedia.org/wiki/Debian_GNU/Linux "wikilink")
      - [Red Hat Enterprise Linux](../Page/Red_Hat_Enterprise_Linux.md "wikilink")\[14\]
      - [Slackware Linux](https://ja.wikipedia.org/wiki/Slackware_Linux "wikilink")
      - [Ubuntu](../Page/Ubuntu.md "wikilink")
  - [FreeBSD](../Page/FreeBSD.md "wikilink")
  - [NetBSD](../Page/NetBSD.md "wikilink")
  - [OpenBSD](../Page/OpenBSD.md "wikilink")
  - [OpenIndiana](https://ja.wikipedia.org/wiki/OpenIndiana "wikilink")
  - [Solaris](../Page/Solaris.md "wikilink") 11（[x86-64](https://ja.wikipedia.org/wiki/x86-64 "wikilink")）

CDEプロジェクトは将来のプロジェクトのゴールとして以下のものを含んでいる。

  - Linux、BSDや他の[Unix系](../Page/Unix系.md "wikilink")のプラットフォームでの移植性を向上させる。
  - さらに他の言語に国際化を進める。

## 脚注

## 参考文献

  - [CDE press release](http://bubl.ac.uk/ARCHIVE/subject/computing/misc/coseup6.htm)
  - [Petition to Open Source CDE and Motif](http://www.marutan.net/cde/)

## 外部リンク

  - [AIX](../Page/AIX.md "wikilink") - [CDE (from Wayback archive)](http://web.archive.org/web/20020607122418/http://www-1.ibm.com/servers/aix/cde/)
  - [HP-UX](../Page/HP-UX.md "wikilink") - [CDE](http://docs.hp.com/en/B1171-90103/index.html)
  - [Solaris](../Page/Solaris.md "wikilink") - [CDE](http://sun.com/solaris/cde/)
  - [Tutorial for the CDE](http://www.cs.cf.ac.uk/Dave/C/node2.html)
  - [Open Group - CDE](http://www.opengroup.org/cde/)

[Category:デスクトップ環境](https://ja.wikipedia.org/wiki/Category:デスクトップ環境 "wikilink") [Category:Xウィンドウマネージャ](https://ja.wikipedia.org/wiki/Category:Xウィンドウマネージャ "wikilink") [Category:ソフトウェアアーキテクチャ](https://ja.wikipedia.org/wiki/Category:ソフトウェアアーキテクチャ "wikilink") [Category:1993年のソフトウェア](https://ja.wikipedia.org/wiki/Category:1993年のソフトウェア "wikilink")

1.
2.
3.
4.
5.
6.
7.
8.
9.
10. [HP-UX : FAQ](http://www.unixguide.net/hp/faq/3.3.shtml)
11.
12.
13.
14. [Red Hat package](https://copr.fedorainfracloud.org/coprs/dcantrel/cde/)
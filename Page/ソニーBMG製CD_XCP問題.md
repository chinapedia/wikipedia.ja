> この記事は[BMGCD XCP](https://ja.wikipedia.org/wiki/BMGCD_XCP)から翻訳されています。


**ソニーBMG製CD XCP問題**（ソニービーエムジーせいコンパクトディスク エックスシーピーもんだい）とは、[アメリカ合衆国](https://ja.wikipedia.org/wiki/アメリカ合衆国 "wikilink")のソニーBMGミュージックエンターテインメント（現:[ソニー・ミュージックエンタテインメント (米国)](https://ja.wikipedia.org/wiki/ソニー・ミュージックエンタテインメント_\(米国\) "wikilink")）の[音楽CDに採用された米](../Page/コンパクトディスク.md "wikilink")[SunnComm Technologies製](https://ja.wikipedia.org/wiki/SunnComm_Technologies "wikilink")[ソフトウェア](../Page/ソフトウェア.md "wikilink")に、[マルウェア](https://ja.wikipedia.org/wiki/マルウェア "wikilink")である[rootkit](https://ja.wikipedia.org/wiki/rootkit "wikilink")が含まれていた問題。ユーザーのPCの[セキュリティ](https://ja.wikipedia.org/wiki/セキュリティ "wikilink")を脆弱にするソフトウェアが、ユーザの同意を得ずに隠密にインストールされることなどが問題視された。

## 概要

[2005年](https://ja.wikipedia.org/wiki/2005年 "wikilink")[10月](https://ja.wikipedia.org/wiki/10月 "wikilink")に、[コピーコントロールCD](../Page/コピーコントロールCD.md "wikilink")（CCCD、[セキュアCD](https://ja.wikipedia.org/wiki/セキュアCD "wikilink")）の米SunnComm Technologies製セキュリティ技術に[脆弱性](https://ja.wikipedia.org/wiki/脆弱性 "wikilink")が発見された。このCCCDを[Windowsパソコンに入れて](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")、ソフトウェア『[XCP](../Page/Extended_Copy_Protection.md "wikilink")』の[インストール](../Page/インストール.md "wikilink")に同意すると、[rootkitプログラムを勝手にインストールしてしまい](../Page/ルートキット.md "wikilink")、更にXCPの[アンインストール](../Page/アンインストール.md "wikilink")が不可能だという指摘がなされ、世界中から非難を浴び、アメリカ合衆国では訴訟へと発展した。このソフトの問題が発覚した後に[マイクロソフト](../Page/マイクロソフト.md "wikilink")は、XCPを悪質なソフトウェアとして認定している。ちなみにソニーBMG側は、この[コンピュータプログラム](https://ja.wikipedia.org/wiki/コンピュータプログラム "wikilink")を完全に削除するツールを、マイクロソフトと協力して提供した。

なお、[ソニー・ミュージックエンタテインメント](https://ja.wikipedia.org/wiki/ソニー・ミュージックエンタテインメント_\(日本\) "wikilink")（SMEJ）や[BMGジャパン](https://ja.wikipedia.org/wiki/BMGジャパン "wikilink")から発売される日本盤は、CCCDは採用していない（海外版・輸入盤で後述のリスト内のCDには注意が必要）。だが、ある調査によると\[1\]、少なくとも568,200のネットワークにこのソニーのマルウェアに感染したコンピュータがあり、日本が21万7000台以上とアメリカの13万台以上を圧倒しているため、一部日本人ユーザーの間でそれ以外のCCCDにも同様の問題がないかと心配する声が盛り上がった。

また、この事件を期に[ハッカー](../Page/ハッカー.md "wikilink")達が米SonyBMG製を含む各種製品を[リバースエンジニアリング](https://ja.wikipedia.org/wiki/リバースエンジニアリング "wikilink")した結果、同様の米SunnComm Technologies製コピープロテクト「[MediaMax](https://ja.wikipedia.org/wiki/MediaMax "wikilink")」が見つかった。このMediaMaxは、[Microsoft Windowsのみならず](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")、[MacOS Xにも感染する能力を持ち](https://ja.wikipedia.org/wiki/MacOS_X "wikilink")、XCPよりも遙かに深刻な問題を含むという結果が報告された。

[Amazon.co.jp](../Page/Amazon.co.jp.md "wikilink")や[タワーレコード](../Page/タワーレコード.md "wikilink")などでは「XCP」入りのCD購入者に対し、購入代金の返金を行った。

2005年12月8日には、インストールされたXCPを悪用し『[Antinny](../Page/Antinny.md "wikilink")』を投下する[コンピュータウイルス](https://ja.wikipedia.org/wiki/コンピュータウイルス "wikilink")も報告された。

「XCP」について、株式会社ソニー・ミュージックエンタテインメント（SMEJ）が見解を出している。

## 問題になった点

  - [Microsoft Windows搭載コンピュータで使うとき](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")、インストールされるプログラムの利用規約に **『rootkitをインストールします』**と明示されていない。つまりユーザーの同意を得ていないコンピュータプログラムを、勝手にインストールしている点。
  - SunnComm Technologies製のプログラムだけではなく、$sys$ が先頭についているファイルやプロセスが隠蔽される。これにより、視覚的に隠蔽されるだけでなく、[アンチウイルスソフトウェア](https://ja.wikipedia.org/wiki/アンチウイルスソフトウェア "wikilink")にも検知出来ない点。
  - コンピュータプログラムをコンピュータ設定でアンインストールせず、単に手動で削除しようとすると、[光学ドライブ](https://ja.wikipedia.org/wiki/光学ドライブ "wikilink")が二度と認識されなくなる点。
  - 隠蔽行為を解除するためにリリースした、最初期のSunnComm Technologies製プログラム（[ActiveX](../Page/ActiveX.md "wikilink")版）に、どの[ウェブサイト](../Page/ウェブサイト.md "wikilink")からも任意の[ソースコード](../Page/ソースコード.md "wikilink")を実行できるという「重大な[セキュリティーホール](https://ja.wikipedia.org/wiki/セキュリティーホール "wikilink")」が含まれていた点。
  - 上記プログラムを入手するには、ソニーBMGに[個人情報](../Page/個人情報.md "wikilink")を提供する必要があった点。

<!-- end list -->

  - [Appleの](../Page/アップル_\(企業\).md "wikilink")[iTunes](https://ja.wikipedia.org/wiki/iTunes "wikilink")に採用されている[デジタル著作権管理](https://ja.wikipedia.org/wiki/デジタル著作権管理 "wikilink")「[FairPlay](https://ja.wikipedia.org/wiki/FairPlay "wikilink")」を回避するため、ツールの[ソースコード](../Page/ソースコード.md "wikilink")を流用したという疑惑\[2\]。
  - [著作権](../Page/著作権.md "wikilink")という[知的財産権](../Page/知的財産権.md "wikilink")の保護の名の下に、許諾したユーザーの財産であるパソコンの内容を改竄し、ユーザーの所有[財産権](../Page/財産権.md "wikilink")を侵害している点。

## 事件の経緯

  - [2005年](https://ja.wikipedia.org/wiki/2005年 "wikilink")[10月31日](../Page/10月31日.md "wikilink") - Winternals社[マーク・ルシノビッチ](https://ja.wikipedia.org/wiki/マーク・ルシノビッチ "wikilink")が、ソニーBMGのXCP Technologyを採用した米国国内向けCCCDにrootkitが入っていて、容易に削除できないなどの問題があることを[ブログ](../Page/ブログ.md "wikilink")で指摘\[3\]。
  - 2005年[11月1日](../Page/11月1日.md "wikilink") - [アメリカ合衆国](https://ja.wikipedia.org/wiki/アメリカ合衆国 "wikilink")[カリフォルニア州](../Page/カリフォルニア州.md "wikilink")で、消費者団体が問題のCDの販売差し止めと、[損害賠償](../Page/損害賠償.md "wikilink")を求める民事訴訟を起こす。
  - 2005年[11月2日](../Page/11月2日.md "wikilink") - ソニーBMGがこれを受けて、パッチツールをリリースする。当初は、プログラムのアンインストールツールとされていたが、実際はプロセスなどの隠蔽を停止する偽装ツールだったことが明らかになる。
  - 2005年[11月4日](../Page/11月4日.md "wikilink") - ソニーBMGがリリースした修正パッチをインストールすると、コンピュータが破壊される可能性があることを専門家が指摘する。また、XCPが勝手に[パケット通信](../Page/パケット通信.md "wikilink")しているとも指摘する\[4\]。
  - 2005年[11月10日](../Page/11月10日.md "wikilink") - ソニーBMGのCDに、[LAME](https://ja.wikipedia.org/wiki/LAME "wikilink")のソースを流用した形跡があることが報じられる\[5\]。これが事実なら[LGPL](https://ja.wikipedia.org/wiki/LGPL "wikilink")に違反する。
  - 2005年[11月11日](../Page/11月11日.md "wikilink") - ソニーBMGが、問題の技術の使われたCDの生産を一時停止すると発表。
  - 2005年[11月15日](../Page/11月15日.md "wikilink") - [プリンストン大学](https://ja.wikipedia.org/wiki/プリンストン大学 "wikilink")のEd Felten教授が、ソニーBMGがリリースした、この問題に関するWebベース版のアンインストールツールに、重大な[セキュリティーホール](https://ja.wikipedia.org/wiki/セキュリティーホール "wikilink")があることを、自らの[ブログ](../Page/ブログ.md "wikilink")で明らかにする\[6\]。
  - 2005年[11月16日](https://ja.wikipedia.org/wiki/11月16日 "wikilink") - ソニーBMGが、問題の技術の使われたCDを[リコールすると発表](https://ja.wikipedia.org/wiki/リコール_\(一般製品\) "wikilink")。
  - 2005年[11月17日](../Page/11月17日.md "wikilink") - さらに2件のGPL違反（FAACとmpg123のソース流用）を指摘される\[7\]。
  - 同日 - ソニーBMGのXCPとは別の技術を使った、MediaMaxのアンインストーラーにも、重大なセキュリティーホールがあることを指摘される\[8\]。
  - 2005年[11月21日](../Page/11月21日.md "wikilink") - LAMEプロジェクトが、LAMEプロジェクト管理人名義でソニーBMGに対して公開質問状を出す\[9\]。
  - 同日 [テキサス州](../Page/テキサス州.md "wikilink")が、ソニーBMGの一部CDに「[スパイウェア](https://ja.wikipedia.org/wiki/スパイウェア "wikilink")」が入っていて、州法に違反しているとして、ソニーBMGを提訴\[10\]。認められれば、最大で違反1件当たり罰金10万ドル。また、市民団体「[電子フロンティア財団](../Page/電子フロンティア財団.md "wikilink")（EFF）」が、XCPだけでなく、MediaMaxを使用したCDも合わせた、2400万枚についての損害賠償を請求した。
  - 2005年[11月28日](../Page/11月28日.md "wikilink") - プリンストン大学のEd Felten教授が、MediaMaxプロテクトに関しても、問題があることを指摘する\[11\]。教授は、MediaMaxには旧式のCD-3と新方式のMM-5の2種類があるが、CD-3を入れた後、MM-5を入れるか、MM-5を入れてから、CD-3を入れるか、MM-5を2回入れると、ソフトの利用規約の同意の有無にかかわらず、ドライバがインストールされると主張している。
  - [2006年](https://ja.wikipedia.org/wiki/2006年 "wikilink")[5月22日](../Page/5月22日.md "wikilink") - 米連邦裁判所判事が、和解案を最終承認する\[12\]<ref>

「[SONY BMGのrootkit CD訴訟、和解を最終承認](http://www.itmedia.co.jp/news/articles/0605/23/news017.html)」。2006年5月23日、ITmediaニュース。</ref>。

  - 2006年[12月20日](../Page/12月20日.md "wikilink") - 米カリフォルニア州の損害賠償訴訟で、75万ドルを消費者団体などに支払うことで和解。
  - 2006年[12月22日](../Page/12月22日.md "wikilink") - 米[マサチューセッツ州](../Page/マサチューセッツ州.md "wikilink")など、40州と425万ドルを支払うことで和解。

## 脚注

<references />

## 外部リンク

  - [F-Secure blog](http://www.f-secure.com/weblog/#00000691)（ソニーBMG CCCD問題を一番早くに見つけたセキュリティ会社）
  - [「XCP」入りCDタイトル一覧SONY BMG](http://cp.sonybmg.com/xcp/english/titles.html)
  - [「XCP」収録CDタイトル一覧](http://www.sonymusic.co.jp/xcp/list.html)（（株）ソニー・ミュージックジャパンインターナショナル 輸入分のみ）
  - [米国SONY BMG発売商品における対応に関するお知らせ](http://www.sonymusic.co.jp/xcp/)

[Category:ソニー・ミュージックエンタテインメント_(米国)](https://ja.wikipedia.org/wiki/Category:ソニー・ミュージックエンタテインメント_\(米国\) "wikilink") [Category:ソニーの歴史](https://ja.wikipedia.org/wiki/Category:ソニーの歴史 "wikilink") [Category:2005年のアメリカ合衆国](https://ja.wikipedia.org/wiki/Category:2005年のアメリカ合衆国 "wikilink") [Category:コンピュータウイルス](https://ja.wikipedia.org/wiki/Category:コンピュータウイルス "wikilink") [Category:コンピュータ・ネットワーク・セキュリティ](https://ja.wikipedia.org/wiki/Category:コンピュータ・ネットワーク・セキュリティ "wikilink") [Category:Windowsのトロイの木馬](https://ja.wikipedia.org/wiki/Category:Windowsのトロイの木馬 "wikilink") [Category:2005年10月](https://ja.wikipedia.org/wiki/Category:2005年10月 "wikilink")

1.  Dan Kaminsky「[Welcome To Planet Sony](http://www.doxpara.com/?q=sony)」。2005年11月15日、 [DoxPara Research](http://www.doxpara.com/)。
2.  Sebastian Porst「[Two new F4I license infringements found](http://www.the-interweb.com/serendipity/index.php?/archives/20051117.html)」。2005年11月17日、[Programming stuff](http://www.the-interweb.com/)
3.  Mark Russinovich「[Sony, Rootkits and Digital Rights Management Gone Too Far](http://blogs.technet.com/markrussinovich/archive/2005/10/31/sony-rootkits-and-digital-rights-management-gone-too-far.aspx)」。2005年10月31日、[Mark's Blog](http://blogs.technet.com/markrussinovich/)。
4.  Mark Russinovich「[More on Sony: Dangerous Decloaking Patch, EULAs and Phoning Home](http://blogs.technet.com/markrussinovich/archive/2005/11/04/more-on-sony-dangerous-decloaking-patch-eulas-and-phoning-home.aspx)」。2005年11月4日、Mark's Blog。
5.  「[SONY BMG製CCCDにLAMEのソースコードを盗用した疑い](http://slashdot.jp/articles/05/11/12/1129225.shtml)」。2005年11月12日、[スラッシュドット ジャパン](../Page/スラッシュドット.md "wikilink")。
6.  Ed Felten「[Sony’s Web-Based Uninstaller Opens a Big Security Hole; Sony to Recall Discs](http://www.freedom-to-tinker.com/?p=927)」。2005年11月15日、Freedom to Tinker。
7.
8.  Ed Felten「[Not Again\! Uninstaller for Other Sony DRM Also Opens Huge Security Hole](http://www.freedom-to-tinker.com/?p=931)」。2005年11月17日、Freedom to Tinker。
9.  The LAME maintainers「[Open letter to Sony BMG (and its owners, Sony and Bertelsmann), First4Internet, and the LAME community.](http://lame.sourceforge.net/open_letter_sony_bmg.html)」。2005年11月21日、LAMEプロジェクト。
10. 「[テキサス州、スパイウェア規制法違反でSONY BMGを提訴](http://www.itmedia.co.jp/news/articles/0511/22/news006.html)」。2005年11月22日、ITmediaニュース。
11. Ed Felten「[MediaMax Permanently Installs and Runs Unwanted Software, Even If User Declines EULA](http://www.freedom-to-tinker.com/?p=936)」2005年11月28日、Freedom to Tinker
12. 「[Judge Grants Final Approval for Sony BMG CD Settlement](https://web.archive.org/web/20060524091650/http://www.eff.org/news/archives/2006_05.php#004693)」。2006年5月22日、Electronic Frontier Foundation。
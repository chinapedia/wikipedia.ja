> この記事は[SQL Slammer](https://ja.wikipedia.org/wiki/SQL_Slammer)から翻訳されています。


**SQL Slammer** (エスキューエル・スラマー）は、[コンピュータウイルス](https://ja.wikipedia.org/wiki/コンピュータウイルス "wikilink")の[ワームの一種](../Page/ワーム_\(コンピュータ\).md "wikilink")。[2003年](../Page/2003年.md "wikilink")[1月25日](../Page/1月25日.md "wikilink")5時30分 (UTC) に確認されてから、爆発的に感染台数を増やし、感染台数は確認後僅か10分で7万5000台以上に達した\[1\]。また、このワームの出すパケットにより、世界的にネットワーク障害が発生した\[2\]。別名 W32.SQLExp.Worm、DDOS.SQLP1434.A、the Sapphire Worm、SQL_HEL、W32/SQLSlammer、Helkern。

## 概要

SQL Slammerを最初に発見した人物は、W3 MediaのシニアWebデベロッパでテクニカルマネージャーのBen Koshyとされている\[3\]。"**SQL** Slammer"と呼ばれているが、このワームは[SQL](../Page/SQL.md "wikilink")で書かれているわけではなく、このワームが[マイクロソフト](../Page/マイクロソフト.md "wikilink")の[SQL Serverまたは](https://ja.wikipedia.org/wiki/Microsoft_SQL_Server "wikilink")[MSDE](https://ja.wikipedia.org/wiki/MSDE "wikilink")に含まれる[バッファオーバーフロー](https://ja.wikipedia.org/wiki/バッファオーバーフロー "wikilink")の脆弱性を突いて感染するからである。ちなみに、その脆弱性の対策パッチは6ヶ月前にマイクロソフトより公開されていた（[MS02-039](http://www.microsoft.com/technet/security/bulletin/MS02-039.mspx), [MS02-061](http://www.microsoft.com/technet/security/bulletin/MS02-061.mspx)）。

## 衝撃

[Internet Storm Centerなどインターネットのトラフィックをモニターしているサイトは](https://ja.wikipedia.org/wiki/Internet_Storm_Center "wikilink")、ネットワークが世界的規模で著しく重くなっていると報告した。その状況は2001年夏に大流行した[Code Redと似ていた](../Page/Code_Red.md "wikilink")。

日本の感染状況は非常に軽微（シマンテックへの感染報告は1件のみ）だったが、セキュリティ意識が低く、コピーソフトが蔓延しているためパッチやサービスパックを適用していない[韓国では](../Page/大韓民国.md "wikilink")、感染したSQL ServerによりDNSがダウンしたことで全国でインターネットが利用できなくなるなど、大きな影響が出た。企業のサーバでも多くの感染被害が出た\[4\]\[5\]。また同様の攻撃は、アジア、ヨーロッパ、北米でも報告された。

[ウイルス対策ソフト](https://ja.wikipedia.org/wiki/ウイルス対策ソフト "wikilink")メーカーの[シマンテック](../Page/シマンテック.md "wikilink")は世界中で少なくとも2万2000台ものシステムが影響を受けると見積もった。

[Microsoft SQL Server Desktop Engine](https://ja.wikipedia.org/wiki/Microsoft_SQL_Server_Desktop_Engine "wikilink") (MSDE) は、このワームに感染し、続々と感染数を増やしていった。また、MSDEがインストールされていることを知らない一般家庭のユーザーの存在もさらに事態を悪化させた。さらに、このワームはMSDEの動作しているコンピュータがインターネット経由で感染した場合、[ネットワークアドレス変換](../Page/ネットワークアドレス変換.md "wikilink") (NAT)の内側のSQL Serverに感染することができた。

## 技術的な詳細

このワームはわずか376[バイトのコードでできていて](../Page/バイト_\(情報\).md "wikilink")、IPアドレスをランダムに発生させて、発生させたIPアドレスを持つホストに対して自身の分身を送りつける以外の行動は行わない。もし、ワームの選択したアドレスを持つホスト上で、パッチを当てていないMicrosoft SQL Serverが動いていた場合、直ちにホストに感染し、感染を増やす活動を始める。

家庭のパソコンでは、一般的にMSDEがインストールされていない限り感染することはない。また、ワームはディスクには書き込まれず、メモリに常駐するだけなので除去することは簡単である。例えば、再起動するだけでも除去することができる（対策を行っていないので、すぐにまた感染することになるが）。

このワームは、[2002年](../Page/2002年.md "wikilink")[7月24日](../Page/7月24日.md "wikilink")にマイクロソフトによって報告されたSQL Serverのセキュリティーホールを突いている。そのパッチはワームが登場する半年も前にマイクロソフトからリリースされていたが、多くのシステムにはパッチが適用されていなかった（マイクロソフト自身のいくつかのサーバを含む）。

ネットワーク遅延は、感染したサーバの吐き出す大量のパケットによるネットワークトラフィックの増大に耐え切れず、多数のルーターがダウンしたことによる。通常、トラフィックが処理限界を超えると、ルーターの処理が遅延するか、ネットワークトラフィックを遮断すると想定されている。いくつかのルーターがクラッシュし、隣のルーターはこれらのルーターへのパケットの受け渡しを止めなければならないと感知する。ルーターは、自身の知っているルーターへこのことを通知し始めた。このようなルーティングテーブルの更新情報の通知の嵐が、さらにルーターが故障する原因となり問題を悪化させた。さらに、クラッシュしたルーターの管理者がルーターを再起動し、ルーターが自分の存在を通知したため、ルーティングの更新情報の通知の嵐が再び発生した。すぐに、インターネットの帯域の大部分がこれらルーティングテーブルを更新するためのルーター同士の通信に消費され、通常のデータトラフィックは遅延し、または完全に停止した。皮肉にも、SQL Slammerは小さなデータだったため、通信に成功したが、まっとうなパケットの通信は不通になった。

SQL Slammerは確認された最初の[ウォーホール型ワーム](https://ja.wikipedia.org/wiki/ウォーホール型ワーム "wikilink")（[2002年](../Page/2002年.md "wikilink")、Nicholas Weaverの論文によって存在を仮定されたネットワークで急速に広がるワーム）である。このワームが急速に広まったのには2つのわけがある。一つは[UDP上で感染を広めたこと](../Page/User_Datagram_Protocol.md "wikilink")、そしてもう一つは、ワームがことである。その結果、感染したホストが他のマシンとのコネクションを確立する必要がなくなり、各々の感染したホストは、限界まで攻撃を試行できた（大体、毎秒数百回）。

## 脚注

## 外部リンク

  - ニュース:

<!-- end list -->

  - [BBC NEWS Technology Virus-like attack hits web traffic](http://news.bbc.co.uk/2/hi/technology/2693925.stm)
  - [MS SQL Server Worm Wreaking Havoc](http://slashdot.org/article.pl?sid=03/01/25/1245206&mode=flat&tid=109)
  - [Wired 11.07: Slammed\!](http://www.wired.com/wired/archive/11.07/slammer.html) A layman's explanation of the Slammer code.
  - 「[「ネット接続障害」27日が山場](http://japanese.chosun.com/site/data/html_dir/2003/01/26/20030126000003.html)」。朝鮮日報、2003年1月26日。

<!-- end list -->

  - アナウンス:

<!-- end list -->

  - [Microsoft Security Bulletin MS02-039 and Patch](http://www.microsoft.com/technet/security/bulletin/MS02-039.mspx)
  - [CERT Advisory CA-2003-04](http://www.cert.org/advisories/CA-2003-04.html)
  - [Symantec Security Response - W32.SQLExp.Worm](http://securityresponse.symantec.com/avcenter/venc/data/w32.sqlexp.worm.html)

<!-- end list -->

  - 解析

<!-- end list -->

  - [Report of CAIDA-coordinated study of SQL Slammer/SapphWarhol Worms: The Potential for Very Fast Internet Plagues](http://www.caida.org/analysis/security/sapphire/) by Nicholas C. Weaver

<!-- end list -->

  - 技術情報

<!-- end list -->

  - [Worm code disassembled](http://www.eeye.com/html/Research/Flash/sapphire.txt)
  - [Multiple Vulnerabilities in Microsoft SQL Server](http://www.cert.org/advisories/CA-2002-22.html) - Carnegie-Mellon Software Engineering Institute
  - [Internet Storm Center](http://isc.incidents.org/)

[Category:コンピュータウイルス](https://ja.wikipedia.org/wiki/Category:コンピュータウイルス "wikilink") [Category:DoS攻撃](https://ja.wikipedia.org/wiki/Category:DoS攻撃 "wikilink")

1.  「[SQLスラマー、10分間に7万5000台感染　過去例のない速さ・米研究者調査](http://www.nikkei.co.jp/weekend/news/03020700020700350700.html)」。日本経済新聞ウイークエンド版、2003年2月4日。
2.  「[世界規模で報告されたネット障害についての総括レポート～Slammerワームによる被害について～](http://www.meti.go.jp/kohosys/press/0003634/)」。経済産業省[情報セキュリティ](https://ja.wikipedia.org/wiki/情報セキュリティ "wikilink")政策室。2003年1月31日。
3.  「[W3 Media's Ben Koshy first to identify Internet 'Slammer' Virus](http://www.w3media.com/images/news/W3_Identify_Slammer_Virus.pdf)」。W3MEDIA.COM、2003年1月24日。
4.  アットマーク・アイティ SQLワーム被害に「人災だ」の声、日本での影響は軽微 2003/1/28 [1](http://www.atmarkit.co.jp/news/200301/28/sqlworm.html)
5.  電算用語の基礎知識 [2](http://www.wdic.org/w/TECH/Slammer)
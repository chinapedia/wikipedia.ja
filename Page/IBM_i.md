> この記事は[IBM i](https://ja.wikipedia.org/wiki/IBM_i)から翻訳されています。


**IBM i**（アイ・ビー・エム アイ）は、[IBM](../Page/IBM.md "wikilink") [Power Systems](https://ja.wikipedia.org/wiki/Power_Systems "wikilink")（旧・AS/400）及び、IBM [PureSystems](https://ja.wikipedia.org/wiki/PureSystems "wikilink")に搭載されている[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink")である。1988年にIBMの[ミッドレンジコンピュータ](../Page/ミッドレンジコンピュータ.md "wikilink")向けに開発されたOSであり、かつては**OS/400**、**i5/OS**と呼ばれていたが、2008年にIBM iに改称した。

## 概要

IBM iは、[System/36](https://ja.wikipedia.org/wiki/System/36 "wikilink")や[System/38](https://ja.wikipedia.org/wiki/System/38 "wikilink")などのIBMの過去の汎用ビジネスシステム（ミッドレンジコンピュータ）との互換性を提供するサブシステムを組み込まれている。

IBMは かつてのOS/400 を "ターンキー"オペレーティングシステムとして設計した。すなわち、通常動作中はほとんどオペレータを必要としないシステムである。たとえば、IBM i は、[DB2データベースを内蔵しているが](https://ja.wikipedia.org/wiki/IBM_DB2 "wikilink")、これは別途インストールする必要もないし、メンテナンスも必要としない。

システム管理は言葉が生まれる前から[ウィザード方式を採用している](../Page/ウィザード_\(ソフトウェア\).md "wikilink")。IBM i はまた、最適化された[Java](https://ja.wikipedia.org/wiki/Java "wikilink")を実装しており、[ハードウェア](../Page/ハードウェア.md "wikilink")もJava用に最適化している。

それ自体はグラフィカルなオペレーティングシステムではないが、クライアントとしてアクセスできる製品として[*iSeries Navigator*](http://www-1.ibm.com/servers/eserver/iseries/navigator/)があり、Webベースのグラフィカル管理システムとなっている。

IBM i は、[Power Systems及び](https://ja.wikipedia.org/wiki/Power_Systems "wikilink")[PureSystems](https://ja.wikipedia.org/wiki/PureSystems "wikilink")上で、[AIX](https://ja.wikipedia.org/wiki/AIX "wikilink")および[Linux](../Page/Linux.md "wikilink")と共存できる。

IBM i プログラム開発環境は、本来ライブラリにリンクするという概念がなくコンパイル時にリンクすることがなかった。[1995年](https://ja.wikipedia.org/wiki/1995年 "wikilink")にIBMは"ILE"（Integrated Language Environment）というパラダイムを導入し、モジュールという概念が導入された。これにより様々なプログラミング言語で書かれたモジュールをリンクすることが可能となった。

最近の機能強化では、RESTful APIへの対応や情報漏洩を抑止するためのセキュリティ強化のほか、 [Node.js](https://ja.wikipedia.org/wiki/Node.js "wikilink") 、 [Python](../Page/Python.md "wikilink") 、 [R言語](../Page/R言語.md "wikilink") 、 [Mono (ソフトウェア)](../Page/Mono_\(ソフトウェア\).md "wikilink") 、 [Git](../Page/Git.md "wikilink") などの各種オープンソース・ソフトウェアを簡単にインストールするための機能強化などが図られている。また、他のOSやアプリケーション開発基盤との操作性を共通化するために、データはEBCDICだけでなくUTF-8、データベースの作成やアクセスは業界標準の [SQL](../Page/SQL.md "wikilink") 、画面は5250エミュレーター以外にWebブラウザーにも対応し、開発環境には [Eclipse (統合開発環境)](../Page/Eclipse_\(統合開発環境\).md "wikilink") や [Visual Studio](https://ja.wikipedia.org/wiki/Visual_Studio "wikilink") も使用できる親和性を有している。

## 歴史

  - 2001年3月 OS/400 5.1 リリース
  - 2002年8月 OS/400 5.2 リリース
  - 2004年6月 i5/OS 5.3 リリース（i5/OSに名称変更）
  - 2006年2月 i5/OS 5.4 リリース
  - 2008年3月 IBM i 6.1 リリース（IBM iに名称変更、バージョン番号を[AIX](https://ja.wikipedia.org/wiki/AIX "wikilink")等と揃えた）
  - 2010年4月 IBM i 7.1 リリース
  - 2014年5月 IBM i 7.2 リリース
  - 2016年4月 IBM i 7.3 リリース
  - 2019年4月 IBM i 7.4 リリース\[1\]

## バージョン

<table>
<thead>
<tr class="header">
<th><p>バージョン[2]</p></th>
<th><p>リリース日[3]</p></th>
<th><p>サポート終了日[4]</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><p>2006-02-14</p></td>
<td><p>2013-09-30</p></td>
</tr>
<tr class="even">
<td></td>
<td><p>2008-03-21</p></td>
<td><p>2015-09-30</p></td>
</tr>
<tr class="odd">
<td></td>
<td><p>2010-04-23</p></td>
<td><p>2018-04-30</p></td>
</tr>
<tr class="even">
<td></td>
<td><p>2014-05-02</p></td>
<td></td>
</tr>
<tr class="odd">
<td></td>
<td><p>2016-04-15</p></td>
<td></td>
</tr>
<tr class="even">
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td></td>
<td><p>2019-04-23</p></td>
<td></td>
</tr>
<tr class="even">
<td><p><small></small></p></td>
<td></td>
<td></td>
</tr>
</tbody>
</table>

## 脚注

## 関連項目

  - [IBM](../Page/IBM.md "wikilink")
  - [Power Systems](https://ja.wikipedia.org/wiki/Power_Systems "wikilink")・[PureSystems](https://ja.wikipedia.org/wiki/PureSystems "wikilink")
  - [RPG (プログラム言語)](../Page/RPG_\(プログラム言語\).md "wikilink")
  - [IBM AIX UNIXオペレーティングシステム](https://www.ibm.com/jp-ja/it-infrastructure/power/os/aix)

## 外部リンク

  - [IBM System i - IBM(Japan)](https://www.ibm.com/jp-ja/it-infrastructure/power/os/ibm-i/)
  - [IBM Power Systems - IBM(Japan)](https://www.ibm.com/jp-ja/it-infrastructure/power)
  - [IBM マーケットプレイス](https://www.ibm.com/jp-ja/products)
  - [IBM ソフトウェア](https://www.ibm.com/software/jp/)
  - [IBM i イベント情報](https://www.ibm.com/jp-ja/it-infrastructure/resources/events/ibm-i-events)

[Category:IBMのオペレーティングシステム](https://ja.wikipedia.org/wiki/Category:IBMのオペレーティングシステム "wikilink") [Category:1988年のソフトウェア](https://ja.wikipedia.org/wiki/Category:1988年のソフトウェア "wikilink") [Category:オブジェクト指向OS](https://ja.wikipedia.org/wiki/Category:オブジェクト指向OS "wikilink")

1.  [IBM i 7.4およびDb2 Mirror for iを発表](https://www.ibm.com/blogs/systems/jp-ja/announcing-ibm-i-7-4-and-db2-mirror-for-i/) - IBM、2019年8月1日閲覧。
2.  [IBM i Technology Updates](https://www.ibm.com/developerworks/community/wikis/home?lang=en#!/wiki/IBM%20i%20Technology%20Updates)
3.  [IBM i Software lifecycle](https://www-01.ibm.com/software/support/ibmi/lifecycle/)
4.  [IBM i Upgrade planning:Releases](https://www-01.ibm.com/support/docview.wss?uid=nas8N1022027)
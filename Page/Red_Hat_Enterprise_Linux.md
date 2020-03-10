> この記事は[Red Hat Enterprise Linux](https://ja.wikipedia.org/wiki/Red_Hat_Enterprise_Linux)から翻訳されています。


**Red Hat Enterprise Linux**（レッドハット・エンタープライズ・リナックス）、略して**RHEL**（レル）とは、[レッドハット](../Page/レッドハット.md "wikilink")社によって開発、販売されている業務向けの[Linuxディストリビューション](../Page/Linuxディストリビューション.md "wikilink")。

## サポート体制

RHELは、リリースされてから 10年間はRed Hatにより、セキュリティアップデートを含めた公式サポートを受けることができる\[1\]。ただし、RHEL 3, 4 は8年目以降最後の3年間は別契約が必要。また、RHEL 5, 6 はセキュリティアップデート終了後3年間はダウンロードすることができる。

新規のリリースは、2年程度ごとに行われるとされている。

RHELのライセンス料金は無料で、関連したサービス(バイナリの配布、アップデート、サポート、特許訴訟からの保護)に対して料金を支払うサブスクリプション契約となっている。 契約期間中には追加料金を支払うこと無しにアップグレードおよびダウングレードを自由に行うことができる。 バイナリパッケージを入手するためにはサブスクリプション契約が必要だが、ソースコードはレッドハットのFTPサイトで公開されている。 サブスクリプションの種類は、RHELの種類とサポート時間(8時間または24時間)、サポート期間(1年または3年)の組み合わせによりさらに細かく分かれている。

また、レッドハットはRHELの運用技術のトレーニングを提供している。運用技術者の認定資格として RHCSA、RHCA、RHCSS、RHCDSといった資格を提供している。詳細は [レッドハット\#認定資格](https://ja.wikipedia.org/wiki/レッドハット#認定資格 "wikilink")。

## バリエーション

RHELにはいくつかの種類があり、バージョン4まではRed Hat Desktop(デスクトップ用途向け)、WS (ワークステーション用途向け)、ES (エントリークラスのサーバ向け)、AS (比較的大規模なサーバ向け)の4種類のバリエーションが存在した。 バージョン5はDesktop、base server、Advanced Platformの3種類となった。 バージョン6はClient、Serverの2種類に、必要に応じてAdd-onを別途追加する。

RHELは、[Red Hat Linux](../Page/Red_Hat_Linux.md "wikilink") (RHL)に由来するディストリビューションであるが、Red Hat Linuxと比較して、リリースサイクルはしっかりと維持・管理されている。現在は、[Fedora](../Page/Fedora.md "wikilink")の成果を活用している。

  - Red Hat Linux 6.2 → Red Hat Linux 6.2E
  - Red Hat Linux 7.2 → Red Hat Enterprise Linux 2.1
  - Red Hat Linux 9 → Red Hat Enterprise Linux 3
  - Fedora Core 3 → Red Hat Enterprise Linux 4
  - Fedora Core 6 → Red Hat Enterprise Linux 5
  - Fedora 12 / 13 → Red Hat Enterprise Linux 6
  - Fedora 19 / 20 → Red Hat Enterprise Linux 7
  - Fedora 28 → Red Hat Enterprise Linux 8

の関係にある。

[CentOS](../Page/CentOS.md "wikilink")や[Scientific Linux](../Page/Scientific_Linux.md "wikilink")、[StartCom Linux](../Page/StartCom_Linux.md "wikilink")、[White Box Enterprise Linuxなどは](../Page/White_Box_Enterprise_Linux.md "wikilink")、レッドハットが公開しているソースコードを元にした[無償で利用できるLinuxディストリビューションであり](https://ja.wikipedia.org/wiki/Red_Hat_Enterprise_Linux派生ディストリビューション "wikilink")、RHELとの互換性を目標としている。その他、[Oracle Linux](https://ja.wikipedia.org/wiki/Oracle_Linux "wikilink") は RHEL をベースに独自のカーネルを搭載している。

## リリースバージョンの経歴

{{\#tag:timeline|

ImageSize = width:900 height:430 PlotArea = right:30 left:30 bottom:60 top:30 DateFormat = dd/mm/yyyy Period = from:01/01/2000 till:01/01/2030 TimeAxis = orientation:horizontal Legend = orientation:vertical position:bottom columns:2 Colors =

`    id:production value:green            Legend:Production`
`    id:extended   value:rgb(0.9,0.9,0.2) Legend:Extended_support`
`    id:lightline  value:rgb(0.8,0.8,0.8)`

BackgroundColors = canvas:white ScaleMajor = gridcolor:lightline unit:year increment:1 start:01/01/2000

Define $vshift = 15 \# move text above the bars

PlotData=

` bar:       `
`   color:production mark:(line,white) align:left fontsize:M`
`   from:07/05/2019 till:07/05/2019 shift:(-55,-4) text:"RHEL 8"`
`   barset:break`
`     color:production`
`     from:07/05/2019 till:05/11/2019 shift:(-12,$vshift) text:".0"`
`   barset:break`
`     color:production`
`     from:05/11/2019 till:31/05/2029 shift:(-138,$vshift) text:".1"`

` bar:      `
`   color:production mark:(line,white) align:left fontsize:M`
`   from:10/06/2014 till:10/06/2014 shift:(-55,-4) text:"RHEL 7"`
`   barset:break`
`     color:production`
`     from:10/06/2014 till:05/03/2015 shift:(-16,$vshift) text:".0"`
`   barset:break`
`     color:production`
`     from:05/03/2015 till:19/11/2015 shift:(-15,$vshift) text:".1"`
`   barset:break`
`     color:production`
`     from:19/11/2015 till:03/11/2016 shift:(-20,$vshift) text:".2"`
`   barset:break`
`     color:production`
`     from:03/11/2016 till:01/08/2017 shift:(-16,$vshift) text:".3"`
`   barset:break`
`     color:production`
`     from:01/08/2017 till:10/04/2018 shift:(-15,$vshift) text:".4"`
`   barset:break`
`     color:production`
`     from:10/04/2018 till:30/10/2018 shift:(-15,$vshift) text:".5"`
`   barset:break`
`     color:production`
`     from:30/10/2018 till:06/08/2019 shift:(-15,$vshift) text:".6"`
`   barset:break`
`     color:production`
`     from:06/08/2019 till:30/06/2024 shift:(-75,$vshift) text:".7"`

` bar:     `
`   color:production mark:(line,white) align:left fontsize:M`
`   from:10/11/2010 till:10/11/2010 shift:(-55,-4) text:"RHEL 6"`
`   barset:break`
`     color:production`
`     from:10/11/2010 till:19/05/2011 shift:(-13,$vshift) text:".0"`
`   barset:break`
`     color:production`
`     from:19/05/2011 till:06/12/2011 shift:(-13,$vshift) text:".1"`
`   barset:break`
`     color:production`
`     from:06/12/2011 till:20/06/2012 shift:(-14,$vshift) text:".2"`
`   barset:break`
`     color:production`
`     from:20/06/2012 till:21/02/2013 shift:(-15,$vshift) text:".3"`
`   barset:break`
`     color:production`
`     from:21/02/2013 till:21/11/2013 shift:(-17,$vshift) text:".4"`
`   barset:break`
`     color:production`
`     from:21/11/2013 till:13/10/2014 shift:(-20,$vshift) text:".5"`
`   barset:break`
`     color:production`
`     from:13/10/2014 till:22/07/2015 shift:(-17,$vshift) text:".6"`
`   barset:break`
`     color:production`
`     from:22/07/2015 till:10/05/2016 shift:(-17,$vshift) text:".7"`
`   barset:break`
`     color:production`
`     from:10/05/2016 till:21/03/2017 shift:(-18,$vshift) text:".8"`
`   barset:break`
`     color:production`
`     from:21/03/2017 till:19/06/2018 shift:(-23,$vshift) text:".9"`
`   barset:break`
`     color:production`
`     from:19/06/2018 till:30/11/2020 shift:(-45,$vshift) text:".10"`
`   barset:break`
`     color:extended`
`     from:30/11/2020 till:30/06/2024`

` bar:    `
`   color:production mark:(line,white) align:left fontsize:M`
`   from:14/03/2007 till:14/03/2007 shift:(-55,-4) text:"RHEL 5"`
`   barset:break`
`     color:production`
`     from:14/03/2007 till:07/11/2007 shift:(-14,$vshift) text:".0"`
`   barset:break`
`     color:production`
`     from:07/11/2007 till:21/05/2008 shift:(-13,$vshift) text:".1"`
`   barset:break`
`     color:production`
`     from:21/05/2008 till:20/01/2009 shift:(-16,$vshift) text:".2"`
`   barset:break`
`     color:production`
`     from:20/01/2009 till:02/09/2009 shift:(-15,$vshift) text:".3"`
`   barset:break`
`     color:production`
`     from:02/09/2009 till:30/03/2010 shift:(-15,$vshift) text:".4"`
`   barset:break`
`     color:production`
`     from:30/03/2010 till:13/01/2011 shift:(-17,$vshift) text:".5"`
`   barset:break`
`     color:production`
`     from:13/01/2011 till:21/07/2011 shift:(-15,$vshift) text:".6"`
`   barset:break`
`     color:production`
`     from:21/07/2011 till:20/02/2012 shift:(-14,$vshift) text:".7"`
`   barset:break`
`     color:production`
`     from:20/02/2012 till:07/01/2013 shift:(-19,$vshift) text:".8"`
`   barset:break`
`     color:production`
`     from:07/01/2013 till:01/10/2013 shift:(-17,$vshift) text:".9"`
`   barset:break`
`     color:production`
`     from:01/10/2013 till:16/09/2014 shift:(-24,$vshift) text:".10"`
`   barset:break`
`     color:production`
`     from:16/09/2014 till:31/03/2017 shift:(-47,$vshift) text:".11"`
`   barset:break`
`     color:extended`
`     from:31/03/2017 till:30/11/2020`

` bar:   `
`   color:production mark:(line,white) align:left fontsize:M`
`   from:15/02/2005 till:15/02/2005 shift:(-55,-4) text:"RHEL 4"`
`   barset:break`
`     color:production`
`     from:15/02/2005 till:08/06/2005 shift:(-11,$vshift) text:".0"`
`   barset:break`
`     color:production`
`     from:08/06/2005 till:05/10/2005 shift:(-10,$vshift) text:".1"`
`   barset:break`
`     color:production`
`     from:05/10/2005 till:12/03/2006 shift:(-11,$vshift) text:".2"`
`   barset:break`
`     color:production`
`     from:12/03/2006 till:10/08/2006 shift:(-11,$vshift) text:".3"`
`   barset:break`
`     color:production`
`     from:10/08/2006 till:01/05/2007 shift:(-15,$vshift) text:".4"`
`   barset:break`
`     color:production`
`     from:01/05/2007 till:15/11/2007 shift:(-13,$vshift) text:".5"`
`   barset:break`
`     color:production`
`     from:15/11/2007 till:29/07/2008 shift:(-16,$vshift) text:".6"`
`   barset:break`
`     color:production`
`     from:29/07/2008 till:19/05/2009 shift:(-16,$vshift) text:".7"`
`   barset:break`
`     color:production`
`     from:19/05/2009 till:16/02/2011 shift:(-31,$vshift) text:".8"`
`   barset:break`
`     color:production`
`     from:16/02/2011 till:29/02/2012 shift:(-21,$vshift) text:".9"`
`   barset:break`
`     color:extended`
`     from:29/02/2012 till:31/03/2017`

` bar:  `
`   color:production mark:(line,white) align:left fontsize:M`
`   from:22/10/2003 till:22/10/2003 shift:(-55,-4) text:"RHEL 3"`
`   barset:break`
`     color:production`
`     from:22/10/2003 till:16/01/2004 shift:(-12,$vshift) text:".0"`
`   barset:break`
`     color:production`
`     from:16/01/2004 till:12/05/2004 shift:(-10,$vshift) text:".1"`
`   barset:break`
`     color:production`
`     from:12/05/2004 till:03/09/2004 shift:(-11,$vshift) text:".2"`
`   barset:break`
`     color:production`
`     from:03/09/2004 till:12/12/2004 shift:(-10,$vshift) text:".3"`
`   barset:break`
`     color:production`
`     from:12/12/2004 till:18/05/2005 shift:(-12,$vshift) text:".4"`
`   barset:break`
`     color:production`
`     from:18/05/2005 till:28/09/2005 shift:(-12,$vshift) text:".5"`
`   barset:break`
`     color:production`
`     from:28/09/2005 till:17/03/2006 shift:(-13,$vshift) text:".6"`
`   barset:break`
`     color:production`
`     from:17/03/2006 till:20/07/2006 shift:(-11,$vshift) text:".7"`
`   barset:break`
`     color:production`
`     from:20/07/2006 till:15/06/2007 shift:(-19,$vshift) text:".8"`
`   barset:break`
`     color:production`
`     from:15/06/2007 till:31/10/2010 shift:(-53,$vshift) text:".9"`
`   barset:break`
`     color:extended`
`     from:31/10/2010 till:30/01/2014`

` bar: `
`   color:production mark:(line,white) align:left fontsize:M`
`   from:26/03/2002 till:26/03/2002 shift:(-62,-4) text:"RHEL 2.1"`
`   barset:break`
`     color:production`
`     from:26/03/2002 till:14/02/2003 shift:(-17,$vshift) text:".0"`
`   barset:break`
`     color:production`
`     from:14/02/2003 till:29/05/2003 shift:(-11,$vshift) text:".1"`
`   barset:break`
`     color:production`
`     from:29/05/2003 till:19/12/2003 shift:(-13,$vshift) text:".2"`
`   barset:break`
`     color:production`
`     from:19/12/2003 till:21/04/2004 shift:(-13,$vshift) text:".3"`
`   barset:break`
`     color:production`
`     from:21/04/2004 till:18/08/2004 shift:(-13,$vshift) text:".4"`
`   barset:break`
`     color:production`
`     from:18/08/2004 till:13/12/2004 shift:(-11,$vshift) text:".5"`
`   barset:break`
`     color:production`
`     from:13/12/2004 till:28/04/2005 shift:(-10,$vshift) text:".6"`
`   barset:break`
`     color:production`
`     from:28/04/2005 till:31/05/2009 shift:(-62,$vshift) text:".7"`

TextData =

`  pos:(275,430)`
`  fontsize:L`
`  textcolor:black`
`  text:"Red Hat Enterprise Linux release timeline"`

}}

\[2\]

<table>
<thead>
<tr class="header">
<th><p>バージョン</p></th>
<th><p>コードネーム</p></th>
<th><p>リリース日</p></th>
<th><p>サポート期限</p></th>
<th><p>カーネルバージョン</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Red Hat Linux 6.2E</p></td>
<td><p>Zoot</p></td>
<td><p>2000年3月27日</p></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>Red Hat Enterprise Linux 2.1</p></td>
<td></td>
<td><p>Pensacola (AS)<br />
Panama (ES)</p></td>
<td><p>2002年3月23日</p></td>
<td><p>2009年5月31日</p></td>
</tr>
<tr class="odd">
<td><p>RHEL 2.1 Update 1</p></td>
<td><p>2003年2月14日</p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>RHEL 2.1 Update 2</p></td>
<td><p>2003年3月29日</p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>RHEL 2.1 Update 3</p></td>
<td><p>2003年12月19日</p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>RHEL 2.1 Update 4</p></td>
<td><p>2004年4月21日</p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>RHEL 2.1 Update 5</p></td>
<td><p>2004年8月18日</p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>RHEL 2.1 Update 6</p></td>
<td><p>2004年12月13日</p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>RHEL 2.1 Update 7</p></td>
<td><p>2005年4月28日</p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>Red Hat Enterprise Linux 3</p></td>
<td></td>
<td><p>Taroon</p></td>
<td><p>2003年10月22日</p></td>
<td><p>2010年10月31日(標準)<br />
2014年1月30日(延長)</p></td>
</tr>
<tr class="odd">
<td><p>RHEL 3 Update 1</p></td>
<td><p>2004年1月16日</p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>RHEL 3 Update 2</p></td>
<td><p>2004年5月18日</p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>RHEL 3 Update 3</p></td>
<td><p>2004年9月3日</p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>RHEL 3 Update 4</p></td>
<td><p>2004年12月21日</p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>RHEL 3 Update 5</p></td>
<td><p>2005年5月20日</p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>RHEL 3 Update 6</p></td>
<td><p>2005年9月28日</p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>RHEL 3 Update 7</p></td>
<td><p>2006年3月15日</p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>RHEL 3 Update 8</p></td>
<td><p>2006年7月20日</p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>RHEL 3.9 (旧表記: Update 9)</p></td>
<td><p>2007年6月11日</p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>Red Hat Enterprise Linux 4</p></td>
<td></td>
<td><p>Nahant</p></td>
<td><p>2005年2月15日</p></td>
<td><p>2012年2月29日(標準)<br />
2017年3月31日(延長)</p></td>
</tr>
<tr class="odd">
<td><p>RHEL 4 Update 1</p></td>
<td><p>2005年6月9日</p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>RHEL 4 Update 2</p></td>
<td><p>2005年10月5日</p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>RHEL 4 Update 3</p></td>
<td><p>2006年3月7日</p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>RHEL 4 Update 4</p></td>
<td><p>2006年8月10日</p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>RHEL 4.5 (旧表記: Update 5)</p></td>
<td><p>2007年5月1日</p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>RHEL 4.6 (旧表記: Update 6)</p></td>
<td><p>2007年11月15日</p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>RHEL 4.7 (旧表記: Update 7)</p></td>
<td><p>2008年7月24日</p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>RHEL 4.8 (旧表記: Update 8)</p></td>
<td><p>2009年5月18日</p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>RHEL 4.9 (旧表記: Update 9)</p></td>
<td><p>2011年2月16日</p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>Red Hat Enterprise Linux 5</p></td>
<td></td>
<td><p>Tikanga</p></td>
<td><p>2007年3月14日</p></td>
<td><p>2017年3月31日(標準)<br />
2020年11月30日(延長)</p></td>
</tr>
<tr class="odd">
<td><p>RHEL 5.1</p></td>
<td><p>2007年11月7日</p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>RHEL 5.2</p></td>
<td><p>2008年5月21日</p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>RHEL 5.3</p></td>
<td><p>2009年1月20日</p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>RHEL 5.4</p></td>
<td><p>2009年9月2日</p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>RHEL 5.5</p></td>
<td><p>2010年3月30日</p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>RHEL 5.6</p></td>
<td><p>2011年1月12日</p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>RHEL 5.7</p></td>
<td><p>2011年7月21日</p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>RHEL 5.8</p></td>
<td><p>2012年2月21日</p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>RHEL 5.9</p></td>
<td><p>2013年1月8日</p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>RHEL 5.10</p></td>
<td><p>2013年9月30日</p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>RHEL 5.11</p></td>
<td><p>2014年9月16日</p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>Red Hat Enterprise Linux 6</p></td>
<td></td>
<td><p>Santiago</p></td>
<td><p>2010年11月10日</p></td>
<td><p>2020年11月30日(標準) 2024年6月30日(延長)</p></td>
</tr>
<tr class="odd">
<td><p>RHEL 6.1</p></td>
<td><p>2011年5月19日</p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>RHEL 6.2</p></td>
<td><p>2011年12月6日</p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>RHEL 6.3</p></td>
<td><p>2012年6月20日</p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>RHEL 6.4</p></td>
<td><p>2013年2月21日</p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>RHEL 6.5</p></td>
<td><p>2013年11月21日</p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>RHEL 6.6</p></td>
<td><p>2014年10月14日</p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>RHEL 6.7</p></td>
<td><p>2015年7月22日</p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>RHEL 6.8</p></td>
<td><p>2016年5月10日</p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>RHEL 6.9</p></td>
<td><p>2017年3月29日</p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>RHEL 6.10</p></td>
<td><p>2018年6月19日</p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>Red Hat Enterprise Linux 7</p></td>
<td></td>
<td><p>Maipo</p></td>
<td><p>2014年6月10日</p></td>
<td><p>2024年6月30日</p></td>
</tr>
<tr class="even">
<td><p>RHEL 7.1</p></td>
<td><p>2015年3月5日</p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>RHEL 7.2</p></td>
<td><p>2015年11月19日</p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>RHEL 7.3</p></td>
<td><p>2016年11月3日</p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>RHEL 7.4</p></td>
<td><p>2017年7月31日</p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>RHEL 7.5</p></td>
<td><p>2018年4月10日</p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>RHEL 7.6</p></td>
<td><p>2018年10月30日</p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>RHEL 7.7</p></td>
<td><p>2019年7月28日</p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>Red Hat Enterprise Linux 8</p></td>
<td><p>RHEL 8.0</p></td>
<td><p>Ootpa</p></td>
<td><p>2019年5月7日</p></td>
<td><p>2029年5月</p></td>
</tr>
<tr class="even">
<td><p>RHEL 8.1</p></td>
<td><p>2019年11月5日</p></td>
<td></td>
<td></td>
<td></td>
</tr>
</tbody>
</table>

| 色 | 状況     |
| - | ------ |
|   | サポート終了 |
|   | サポート中  |

バージョンの読み方として、旧表記で RHEL 4 Update 5 だったものは、新しい表記で 4.5 と呼ぶようになっている。

## 脚注・出典

## 関連項目

  - [Linuxディストリビューションの比較](../Page/Linuxディストリビューションの比較.md "wikilink")
  - [Red Hat Enterprise Linux派生ディストリビューション](https://ja.wikipedia.org/wiki/Red_Hat_Enterprise_Linux派生ディストリビューション "wikilink")

## 外部リンク

  - [レッドハット株式会社](https://www.redhat.com/ja)
  - [Red Hat Enterprise Linux Life Cycle(英語サイト)](https://access.redhat.com/support/policy/updates/errata/)
  - [30日試用版(英語サイト)](https://www.redhat.com/en/technologies/linux-platforms/enterprise-linux)

[Category:Linuxディストリビューション](https://ja.wikipedia.org/wiki/Category:Linuxディストリビューション "wikilink") [Category:レッドハット](https://ja.wikipedia.org/wiki/Category:レッドハット "wikilink") [Category:2000年のソフトウェア](https://ja.wikipedia.org/wiki/Category:2000年のソフトウェア "wikilink")

1.  [Red Hat Enterprise Linux Life Cycle](https://access.redhat.com/support/policy/updates/errata/)
2.  [Red Hat Enterprise Linux Release Dates](https://access.redhat.com/articles/3078)
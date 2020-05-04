> この記事は[CentOS](https://ja.wikipedia.org/wiki/CentOS)から翻訳されています。


**CentOS**（セントオーエス\[1\]\[2\], \[3\]）は、[Red Hat Enterprise Linux](../Page/Red_Hat_Enterprise_Linux.md "wikilink")（以下「RHEL」と呼ぶ）と機能的に互換性があることを目指した\[4\]フリーの[Linuxディストリビューション](../Page/Linuxディストリビューション.md "wikilink")である。

## 概要

[レッドハット](../Page/レッドハット.md "wikilink")は[RHELに含まれている](../Page/Red_Hat_Enterprise_Linux.md "wikilink")[ソフトウェア](../Page/ソフトウェア.md "wikilink")の[ソースコード](../Page/ソースコード.md "wikilink")を[オープンソース](../Page/オープンソース.md "wikilink")ライセンスに基づき無償公開している。CentOSはこれをもとに、商標や商用パッケージ等を除去したものをリビルドしている。[White Box Enterprise Linux](../Page/White_Box_Enterprise_Linux.md "wikilink")、[Scientific Linux等を含めて](../Page/Scientific_Linux.md "wikilink")、一般に「RHELクローン」と呼ばれることもある。ただしCentOSプロジェクトのFAQでは"CentOS Linux is NOT a clone of Red Hat® Enterprise Linux."\[5\] と明記されておりRHELのクローンではないとしている。 RHELに由来するソースコードは変更されないように意図されている\[6\]が、CentOS独自の追加機能を提供するリポジトリを提供している\[7\]。

## 開発

RHELの一般公開されたソースコードにもとづくディストリビューションとして[White Box Enterprise Linux](../Page/White_Box_Enterprise_Linux.md "wikilink") が先にリリースされている\[8\]。これが人気を得たことを契機にCentOSプロジェクトは有志のボランティアにより立ち上げられた。呼び名は「コミュニティベースで開発されたエンタープライズクラスの[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink") (**C**ommunity **ENT**erprise **O**perating **S**ystem) 」に由来する。

開発当初、レッドハットはCentOSの配布・開発に関与してこなかったが、2014年1月にCentOSプロジェクトを支援していくことを表明。プロジェクトの中心メンバーを同社員として迎え入れた\[9\]。

## ターゲット

ターゲットはRHELと同様に企業の[サーバ](../Page/サーバ.md "wikilink")や[デスクトップ環境](https://ja.wikipedia.org/wiki/デスクトップ環境 "wikilink")の構築\[10\]としている。サポートが必要な場合にはレッドハットの製品を勧めるとしている\[11\]。デスクトップも想定されていることから、高機能なGUI環境も標準で提供されている。[LibreOffice](https://ja.wikipedia.org/wiki/LibreOffice "wikilink")や[Oracle VM VirtualBoxなどのパッケージや後述の](https://ja.wikipedia.org/wiki/Oracle_VM_VirtualBox "wikilink")[サードパーティー](../Page/サードパーティー.md "wikilink")の[リポジトリ](../Page/リポジトリ.md "wikilink")を用いて[ビジネスソフト](https://ja.wikipedia.org/wiki/ビジネスソフト "wikilink")、デスクトップ[仮想化ソフト](https://ja.wikipedia.org/wiki/x86仮想化 "wikilink")、[GPUや周辺機器の](../Page/Graphics_Processing_Unit.md "wikilink")[デバイスドライバ](../Page/デバイスドライバ.md "wikilink")、[セキュリティソフト](https://ja.wikipedia.org/wiki/セキュリティソフト "wikilink")、[デジタルコンテンツ](https://ja.wikipedia.org/wiki/デジタルコンテンツ "wikilink")制作ツール、[メディアプレーヤー](../Page/メディアプレーヤー.md "wikilink")、ビデオコーデックなどをインストールすれば、本格的なデスクトップOSとして使用することが可能である。

ライセンス費用が無償であるにもかかわらずサポート期限が非常に長い。安定性にも優れ一部メーカーのLinux搭載パソコンやワークステーションでの採用も増加しつつある。

## 入手方法

公式及びミラーサーバからCDおよびDVDの[ISOイメージ](https://ja.wikipedia.org/wiki/ISOイメージ "wikilink")が[HTTPと](../Page/Hypertext_Transfer_Protocol.md "wikilink")[FTPでダウンロードできる](../Page/File_Transfer_Protocol.md "wikilink")。バージョン7からは[Blu-ray DiscのISOイメージも追加されている](../Page/Blu-ray_Disc.md "wikilink")。大多数のミラーサーバでは[BitTorrent](../Page/BitTorrent.md "wikilink")でダウンロード出来るようにするためのトレントファイルのみが公開されている。

## パッケージ管理

### ツール

CentOSは[Red Hat Linuxを源流とするRPM系Linuxに属しており](../Page/Red_Hat_Linux.md "wikilink")、[パッケージ管理システム](../Page/パッケージ管理システム.md "wikilink")に[Yumおよびその後継の](../Page/Yellowdog_Updater_Modified.md "wikilink")[DNFを採用している](https://ja.wikipedia.org/wiki/DNF_\(ソフトウェア\) "wikilink")。[RHELがRed](../Page/Red_Hat_Enterprise_Linux.md "wikilink") Hat Networkサーバをデフォルトにしているのに対し、[CentOS Mirror Network](http://www.centos.org/modules/tinycontent/index.php?id=13)が用意されている。

### リポジトリ

CentOSにデフォルトで含まれる[リポジトリ](../Page/リポジトリ.md "wikilink") (Base, Updates, Addons, Extras, CentOS Plus) に加えて、[Fedora](../Page/Fedora.md "wikilink")提供のepel (Extra Packages for Enterprise Linux) や[サードパーティー](../Page/サードパーティー.md "wikilink")のNux Dextop リポジトリ\[12\]やRPM Fusion\[13\], ELRepo\[14\], Les RPM de Remi\[15\], RPMForge\[16\], JPackage\[17\]などがよく使われている。CentOS Plusはデフォルトで無効化されている。RPMForge及びRemiに関しても、オリジナルのパッケージを上書きしてしまう可能性があるとしてインストール後はOFFにして運用することが一般的である。

## バージョン

### 番号の規則

CentOS 6以前はメジャーバージョンとマイナーバージョンの二つより構成される。メジャーバージョンはベースとしたRHELに対応しており、マイナーバージョンはそのRHELのバージョンアップに対応する。例えばCentOS 4.3はRHEL 4 update 3のソースコードよりビルドされており、これとの互換が目標となっている。CentOS 7以降はメジャーバージョンとマイナーバージョンに加えて、タイムスタンプ（年、月）が追加された。例えばCentOS 7.0-1406はRHEL7.0の2014年6月にリリースされたソースコードを基にしていることを示している\[18\]。

### リスト

メンテナンス更新期限はRHELと同じく10年（CentOS 4以前は約7年）程度\[19\]と非常に長い。完全更新は新たな機能の追加とセキュリティパッチ配布を意味し、年2～4回が予定されている。その後は必要不可欠なセキュリティパッチ配布のみを想定している。

<table>
<caption>バージョンのリスト[20]</caption>
<thead>
<tr class="header">
<th><p>バージョン</p></th>
<th></th>
<th><p>アーキテクチャ[21]</p></th>
<th><p>カーネル</p></th>
<th><p>リリース日</p></th>
<th><p>ベースとなった<br />
RHELのリリース日</p></th>
<th><p>遅延</p></th>
<th><p>完全更新期限<br />
Full Updates</p></th>
<th><p>メンテナンス更新期限<br />
Maintenance Updates</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>2</p></td>
<td><p>2.1（最終）</p></td>
<td><p><a href="../Page/IA-32.md" title="wikilink">i386</a></p></td>
<td><p>2.4.9</p></td>
<td><p>2004年5月14日</p></td>
<td><p>2002年5月17日</p></td>
<td><p>728日</p></td>
<td><p>2005年5月31日</p></td>
<td><p>2009年5月31日</p></td>
</tr>
<tr class="even">
<td><p>3</p></td>
<td><p>3.1</p></td>
<td><p>i386, <a href="https://ja.wikipedia.org/wiki/x86-64" title="wikilink">x86-64</a>, <a href="../Page/IA-64.md" title="wikilink">IA-64</a>, <a href="https://ja.wikipedia.org/wiki/ESA/390" title="wikilink">s390</a>, <a href="https://ja.wikipedia.org/wiki/z/Architecture" title="wikilink">s390x</a></p></td>
<td><p>2.4.21-15</p></td>
<td><p>2004年3月19日</p></td>
<td><p>2003年10月23日</p></td>
<td><p>148日</p></td>
<td><p>2006年10月31日</p></td>
<td><p>2010年10月31日</p></td>
</tr>
<tr class="odd">
<td></td>
<td><p>3.9（最終）</p></td>
<td><p>i386, x86-64, IA-64, s390, s390x</p></td>
<td><p>2.4.21-50</p></td>
<td><p>2007年7月26日</p></td>
<td><p>2007年6月15日</p></td>
<td><p>41日</p></td>
<td><p>　</p></td>
<td></td>
</tr>
<tr class="even">
<td><p>4</p></td>
<td><p>4.0</p></td>
<td><p>i386, x86-64, PowerPC(ベータ版)</p></td>
<td><p>2.6.9-5</p></td>
<td><p>2005年3月9日</p></td>
<td><p>2005年2月14日</p></td>
<td><p>23日</p></td>
<td><p>2009年2月29日</p></td>
<td><p>2012年2月29日</p></td>
</tr>
<tr class="odd">
<td></td>
<td><p>4.9（最終）</p></td>
<td><p>i386, x86-64</p></td>
<td><p>2.6.9-100</p></td>
<td><p>2011年3月2日</p></td>
<td><p>2011年2月16日</p></td>
<td><p>14日</p></td>
<td><p>　</p></td>
<td></td>
</tr>
<tr class="even">
<td><p>5</p></td>
<td><p>5.0</p></td>
<td><p>i386, x86-64</p></td>
<td><p>2.6.18-8</p></td>
<td><p>2007年4月12日</p></td>
<td><p>2007年3月14日</p></td>
<td><p>28日</p></td>
<td><p>2014年 Q1</p></td>
<td><p>2017年3月31日</p></td>
</tr>
<tr class="odd">
<td></td>
<td><p>5.1</p></td>
<td><p>i386, x86-64</p></td>
<td><p>2.6.18-53</p></td>
<td><p>2007年12月2日</p></td>
<td><p>2007年11月7日</p></td>
<td><p>25日</p></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td></td>
<td><p>5.2</p></td>
<td><p>i386, x86-64</p></td>
<td><p>2.6.18-92</p></td>
<td><p>2008年6月24日</p></td>
<td><p>2008年5月21日</p></td>
<td><p>34日</p></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td></td>
<td><p>5.3</p></td>
<td><p>i386, x86-64</p></td>
<td><p>2.6.18-128</p></td>
<td><p>2009年3月31日</p></td>
<td><p>2009年1月20日</p></td>
<td><p>69日</p></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td></td>
<td><p>5.4</p></td>
<td><p>i386, x86-64</p></td>
<td><p>2.6.18-164</p></td>
<td><p>2009年10月21日</p></td>
<td><p>2009年9月2日</p></td>
<td><p>49日</p></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td></td>
<td><p>5.5</p></td>
<td><p>i386, x86-64</p></td>
<td><p>2.6.18-194</p></td>
<td><p>2010年5月14日</p></td>
<td><p>2010年3月31日</p></td>
<td><p>44日</p></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td></td>
<td><p>5.6</p></td>
<td><p>i386, x86-64</p></td>
<td><p>2.6.18-238</p></td>
<td><p>2011年4月8日</p></td>
<td><p>2011年1月13日</p></td>
<td><p>85日</p></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td></td>
<td><p>5.7</p></td>
<td><p>i386, x86-64</p></td>
<td><p>2.6.18-274</p></td>
<td><p>2011年9月13日</p></td>
<td><p>2011年7月21日</p></td>
<td><p>54日</p></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td></td>
<td><p>5.8</p></td>
<td><p>i386, x86-64</p></td>
<td><p>2.6.18-308</p></td>
<td><p>2012年3月7日</p></td>
<td><p>2012年2月21日</p></td>
<td><p>15日</p></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td></td>
<td><p>5.9</p></td>
<td><p>i386, x86-64</p></td>
<td><p>2.6.18-348</p></td>
<td><p>2013年1月17日</p></td>
<td><p>2013年1月8日</p></td>
<td><p>10日</p></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td></td>
<td><p>5.10</p></td>
<td><p>i386, x86-64</p></td>
<td><p>2.6.18-371</p></td>
<td><p>2013年10月19日</p></td>
<td><p>2013年9月30日</p></td>
<td><p>19日</p></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td></td>
<td><p>5.11（最終）</p></td>
<td><p>i386, x86-64</p></td>
<td><p>2.6.18-398</p></td>
<td><p>2014年9月30日</p></td>
<td><p>2014年9月16日</p></td>
<td><p>14日</p></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>6</p></td>
<td><p>6.0</p></td>
<td><p>i386, x86-64</p></td>
<td><p>2.6.32-71</p></td>
<td><p>2011年7月9日</p></td>
<td><p>2010年11月10日</p></td>
<td><p>242日</p></td>
<td><p>2017年 Q2</p></td>
<td><p>2020年11月30日</p></td>
</tr>
<tr class="odd">
<td></td>
<td><p>6.1</p></td>
<td><p>i386, x86-64</p></td>
<td><p>2.6.32-131</p></td>
<td><p>2011年12月9日</p></td>
<td><p>2011年5月19日</p></td>
<td><p>204日</p></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td></td>
<td><p>6.2</p></td>
<td><p>i386, x86-64</p></td>
<td><p>2.6.32-220</p></td>
<td><p>2011年12月20日</p></td>
<td><p>2011年12月6日</p></td>
<td><p>14日</p></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td></td>
<td><p>6.3</p></td>
<td><p>i386, x86-64</p></td>
<td><p>2.6.32-279</p></td>
<td><p>2012年7月9日</p></td>
<td><p>2012年6月21日</p></td>
<td><p>18日</p></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td></td>
<td><p>6.4</p></td>
<td><p>i386, x86-64</p></td>
<td><p>2.6.32-358</p></td>
<td><p>2013年3月9日</p></td>
<td><p>2013年2月21日</p></td>
<td><p>15日</p></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td></td>
<td><p>6.5</p></td>
<td><p>i386, x86-64</p></td>
<td><p>2.6.32-431</p></td>
<td><p>2013年12月1日</p></td>
<td><p>2013年11月21日</p></td>
<td><p>10日</p></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td></td>
<td><p>6.6</p></td>
<td><p>i386, x86-64</p></td>
<td><p>2.6.32-504</p></td>
<td><p>2014年10月28日</p></td>
<td><p>2014年10月14日</p></td>
<td><p>14日</p></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td></td>
<td><p>6.7</p></td>
<td><p>i386, x86-64</p></td>
<td><p>2.6.32-573</p></td>
<td><p>2015年8月7日</p></td>
<td><p>2015年7月22日</p></td>
<td><p>16日</p></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td></td>
<td><p>6.8</p></td>
<td><p>i386, x86-64</p></td>
<td><p>2.6.32-642</p></td>
<td><p>2016年5月25日</p></td>
<td><p>2016年5月10日</p></td>
<td><p>15日</p></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td></td>
<td><p>6.9</p></td>
<td><p>i386, x86-64</p></td>
<td><p>2.6.32-696</p></td>
<td><p>2017年4月5日</p></td>
<td><p>2017年3月21日</p></td>
<td><p>15日</p></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td></td>
<td><p>6.10（最新）</p></td>
<td><p>i386, x86-64</p></td>
<td><p>2.6.32-696</p></td>
<td><p>2018年7月3日</p></td>
<td><p>2018年6月19日</p></td>
<td><p>14日</p></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>7</p></td>
<td><p>7.0-1406</p></td>
<td><p>x86-64</p></td>
<td><p>3.10.0-123</p></td>
<td><p>2014年7月7日</p></td>
<td><p>2014年6月10日</p></td>
<td><p>27日</p></td>
<td><p>2020年 Q4</p></td>
<td><p>2024年6月30日</p></td>
</tr>
<tr class="even">
<td></td>
<td><p>7.1-1503</p></td>
<td><p>x86-64</p></td>
<td><p>3.10.0-229</p></td>
<td><p>2015年3月31日</p></td>
<td><p>2015年3月5日</p></td>
<td><p>26日</p></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td></td>
<td><p>7.2-1511</p></td>
<td><p>x86-64</p></td>
<td><p>3.10.0-327</p></td>
<td><p>2015年12月14日</p></td>
<td><p>2015年11月19日</p></td>
<td><p>25日</p></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td></td>
<td><p>7.3-1611</p></td>
<td><p>x86-64</p></td>
<td><p>3.10.0-514</p></td>
<td><p>2016年12月12日</p></td>
<td><p>2016年11月3日</p></td>
<td><p>39日</p></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td></td>
<td><p>7.4-1708</p></td>
<td><p>x86-64</p></td>
<td><p>3.10.0-693</p></td>
<td><p>2017年9月14日</p></td>
<td><p>2017年8月1日</p></td>
<td><p>44日</p></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td></td>
<td><p>7.5-1804</p></td>
<td><p>x86-64</p></td>
<td><p>3.10.0-862</p></td>
<td><p>2018年5月10日</p></td>
<td><p>2018年4月10日</p></td>
<td><p>30日</p></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td></td>
<td><p>7.6-1810</p></td>
<td><p>x86-64</p></td>
<td><p>3.10.0-957</p></td>
<td><p>2018年12月3日</p></td>
<td><p>2018年10月30日</p></td>
<td><p>34日</p></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td></td>
<td><p>7.7-1908</p></td>
<td><p>x86-64</p></td>
<td><p>3.10.0-1062</p></td>
<td><p>2019年9月17日</p></td>
<td><p>2019年8月6日</p></td>
<td><p>42日</p></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td></td>
<td><p>7.8-2003（最新）</p></td>
<td><p>x86-64</p></td>
<td><p>3.10.0-1127</p></td>
<td><p>2020年4月27日</p></td>
<td><p>2020年3月30日</p></td>
<td><p>28日</p></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>8</p></td>
<td><p>8.0-1905</p></td>
<td><p>x86-64, POWER8 LE, AArch64</p></td>
<td><p>4.18.0-80</p></td>
<td><p>2019年9月24日</p></td>
<td><p>2019年5月7日</p></td>
<td><p>140日</p></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td></td>
<td><p>8.1-1911（最新）</p></td>
<td><p>x86-64, POWER8 LE, AArch64</p></td>
<td><p>4.18.0-147</p></td>
<td><p>2020年1月15日</p></td>
<td><p>2019年11月5日</p></td>
<td><p>71日</p></td>
<td></td>
<td></td>
</tr>
</tbody>
</table>

### アドオン

Software Collections (SCL) はより新しいバージョンもしくはシステムに元来含まれていない動的プログラミング言語、データベースサーバ、それらに関連した様々なパッケージを提供するレポジトリである\[22\]。これらはCentOSで標準的に提供されるパッケージを置き換えるものではない。`/opt`ディレクトリに並行してインストールされて提供される。`scl`ユーティリティによってはアプリケーションごとに選択できる。例えばPerlやMySQLの標準のバージョンはCentOSの基本的なインストールのままである\[23\]。

| アドオン名                                                                              | アーキテクチャ\[24\]                                                                                                                                                                        | CentOSのバージョン                                                                                                                  | CentOS リリース日                                         | RHEL リリース日   | 遅延(日) |
| ---------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ----------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------- | ------------ | ----- |
| Software Collections (SCL) 1.0<ref name="rhel-software-collections-1.0">{{cite web | url = <https://www.redhat.com/about/news/press-archive/2013/9/red-hat-extends-red-hat-enterprise-linux-platform-with-latest-versions-of-popular-programming-languages-and-databases> | title = Red Hat Extends Red Hat Enterprise Linux Platform with Latest Versions of Popular Programming Languages and Databases | date = 2013-09-12 | accessdate = 2013-10-31 }}</ref> | x86-64       | 6.4   |
| Developer Toolset 2.0<ref name="rhel-developer-toolset-2.0">{{cite web             | url = <http://www.redhat.com/about/news/press-archive/2013/9/red-hat-releases-red-hat-developer-toolset-2-0-with-update-to-gcc>                                                      | title = Red Hat Releases Red Hat Developer Toolset 2.0 with Update to GCC                                                     | date = 2013-09-12 | accessdate = 2013-10-31 }}</ref> | i386, x86-64 | 6.4   |

## アーキテクチャ

CentOSは8では[x86-64](https://ja.wikipedia.org/wiki/x86-64 "wikilink")、[POWER8](https://ja.wikipedia.org/wiki/POWER8 "wikilink") LE、[AArch64](https://ja.wikipedia.org/wiki/AArch64 "wikilink")のアーキテクチャをサポートする。7では[x86-64](https://ja.wikipedia.org/wiki/x86-64 "wikilink")アーキテクチャしかサポートしない。ただし[IA-32](../Page/IA-32.md "wikilink")をサポートしたCentOS 6は依然サポートの対象内である\[25\]。

以下は現在、サポートされていない:

  - [x86](../Page/IA-32.md "wikilink")（[32ビット](../Page/32ビット.md "wikilink")）（CentOS 7以降ではサポート外となったが、Alternative Architecture Special Interest Groupでサポート継続\[26\]）
  - [i586](https://ja.wikipedia.org/wiki/i586 "wikilink")
  - [物理アドレス拡張](../Page/物理アドレス拡張.md "wikilink")のない[x86](../Page/IA-32.md "wikilink")（CentOS 6以降ではサポート外）
  - IA-64（[インテル](https://ja.wikipedia.org/wiki/インテル "wikilink")[Itanium](../Page/Itanium.md "wikilink")、64ビット）*（CentOS 3、4にてサポート）*
  - [PowerPC](../Page/PowerPC.md "wikilink")/32（G3またはG4のPowerPCプロセッサを搭載した[アップルの](../Page/アップル_\(企業\).md "wikilink")[Macintosh](../Page/Macintosh.md "wikilink")と[Power Mac](../Page/Power_Mac.md "wikilink")）*(CentOS 4にてベータでのサポート)*
  - [IBM](../Page/IBM.md "wikilink") [メインフレーム](../Page/メインフレーム.md "wikilink") ([eServer](https://ja.wikipedia.org/wiki/eServer "wikilink")、[zSeries](https://ja.wikipedia.org/wiki/zSeries "wikilink")および[S/390](https://ja.wikipedia.org/wiki/IBM_S/390 "wikilink")) *(CentOS 5以降ではサポート外)*
  - [Alpha](https://ja.wikipedia.org/wiki/DEC_Alpha "wikilink") *（CentOS 4のみでサポート）*
  - [SPARC](../Page/SPARC.md "wikilink")*（CentOS 4のみでサポート）*

## 派生品

  - NuOnce Networks CentOS / BlueQuartz CD
  - BlueOnyx
  - Openfiler
  - Rocks Cluster Distribution, for computer clusters, is now based on CentOS
  - SME Server
  - Trixbox, a PBX solution
  - XenEnterprise
  - PBX in a Flash
  - FreePBX Distro

## 関連項目

  - [Linuxディストリビューションの比較](../Page/Linuxディストリビューションの比較.md "wikilink")
  - [Red Hat Enterprise Linux派生ディストリビューション](https://ja.wikipedia.org/wiki/Red_Hat_Enterprise_Linux派生ディストリビューション "wikilink")

## 脚注

### 出典・関連リンク

<references />

### 注釈

<references group="注釈" />

## 外部リンク

  - [CentOS プロジェクト・ホームページ](https://www.centos.org/)
  - [プロジェクト公式Wiki](https://wiki.centos.org/FrontPage)
  - [CentOS FAQ](https://wiki.centos.org/FAQ)（公式FAQ）
  - [CentOS - Free books](http://www.linux-books.us/centos.php)

<!-- end list -->

  - [DistroWatch](https://ja.wikipedia.org/wiki/DistroWatch "wikilink") (収録パッケージのバージョン詳細)
      - [CentOS](http://distrowatch.com/table.php?distribution=centos)
      - [RHEL](http://distrowatch.com/table.php?distribution=redhat)
      - [Fedora](http://distrowatch.com/table.php?distribution=fedora)

[Category:Linuxディストリビューション](https://ja.wikipedia.org/wiki/Category:Linuxディストリビューション "wikilink") [Category:2004年のソフトウェア](https://ja.wikipedia.org/wiki/Category:2004年のソフトウェア "wikilink")

1.
2.
3.  [公式フォーラム](http://www.centos.org/modules/newbb/viewtopic.php?viewmode=flat&topic_id=925&forum=18)等を中心に sent-oss（セントス）と発音する例も。
4.
5.
6.
7.
8.  [White Box Enterprise Linux 本家サイトニュース](http://www.whiteboxlinux.org/news.html)と[CentOS本家サイトヒストリー](http://www.centos.org/modules/news/index.php?storytopic=4)を参照
9.
10. [Red Hat Enterprise Linux 製品情報](http://www.redhat.com/ja/technologies/linux-platforms/enterprise-linux)
11.
12. [RPM repositories for EL](http://li.nux.ro/repos.html)
13. [Configuration - RPM Fusion](http://rpmfusion.org/Configuration/)
14. [ELRepo - HomePage](http://elrepo.org/)
15. [Les RPM de Remi](http://rpms.famillecollet.com/)
16. [AdditionalResources/Repositories/RPMForge - CentOS Wiki](http://wiki.centos.org/AdditionalResources/Repositories/RPMForge)
17. [JPackage Project](http://www.jpackage.org/)
18.
19. [Download - CentOS Wiki](http://wiki.centos.org/Download)
20. [CentOS Product Specifications](https://wiki.centos.org/About/Product)
21.
22.
23.
24.
25.
26. [CentOS 7 32ビット版](http://mirror.centos.org/altarch/7/isos/i386/)
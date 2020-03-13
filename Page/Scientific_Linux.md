> この記事は[Scientific Linux](https://ja.wikipedia.org/wiki/Scientific_Linux)から翻訳されています。


**Scientific Linux**（サイエンティフィック・リナックス）は、[フェルミ国立加速器研究所](../Page/フェルミ国立加速器研究所.md "wikilink")（Fermi National Accelerator Laboratory、以下フェルミ研究所）による[Linuxディストリビューション](../Page/Linuxディストリビューション.md "wikilink")。[Red Hat Enterprise Linux](../Page/Red_Hat_Enterprise_Linux.md "wikilink")（RHEL）をベースとしており、高い互換性を持つ。**SL**と略されることが多い。

## 概要

[レッドハット](../Page/レッドハット.md "wikilink")がリリースしたEnterprise向けLinuxディストリビューションより、同社の商標に関する部分を削除し、さらに[高エネルギー物理学](../Page/高エネルギー物理学.md "wikilink")分野でよく用いられる一部のパッケージを追加し、[ソースコード](../Page/ソースコード.md "wikilink")から再コンパイルした無償配布のディストリビューションである。

## 設計思想

Scientific Linuxの第一の目的は、世界中の様々な研究所や大学のための一般的なLinuxディストリビューションを作り、かくして、同じような努力を減らすことにある。主要なゴールは、若干のマイナーな追加と変更を伴う形で、Red Hat Enterprise Linuxに全て互換性を持たせることと、Linuxの基礎を邪魔することなく、場所に応じたカスマタイズを簡単にできるようにすることである\[1\]。Poseidon Linuxのような他のディストリビューションとは異なり、Scientific Linuxは、科学向けソフトウェアの大規模なコレクションは含んでいない\[2\]。しかしながら、そのようなソフトウェアのインストールにはよく適合するようになっている。

## 歴史

フェルミ研究所が[Linuxクラスター](../Page/Linuxクラスター.md "wikilink")を構築する必要に迫られ、RHELのクローンとしてFermi Linux LTSをリリースした。同時期に[欧州原子核研究機構](../Page/欧州原子核研究機構.md "wikilink")（CERN）によって、同じくRHEL互換であるCern Linuxの開発が進められており、バージョン3.0.1のリリースと共にプロジェクトが併合され、Scientific Linux、[Scientific Linux CERNとなった](https://ja.wikipedia.org/wiki/Scientific_Linux_CERN "wikilink")。

一時期、[CentOS](../Page/CentOS.md "wikilink")がRHELの新バージョンへの追随に長い時間がかかっていた事があり、そのためScientific LinuxがCentOSの代替手段として注目されていた（現在ではCentOSもRHELの新バージョンに迅速に対応している\[3\]）。

2015年にCERNはScientific Linuxから[CentOS](../Page/CentOS.md "wikilink")への移行を開始し、プロジェクトから離脱した\[4\]\[5\]。

2019年4月22日、メーリングリストで次期開発を行わず、SL6、SL7のライフサイクル通りのサポートのみを行うことを発表した\[6\]。

### リリース履歴

Scientific Linuxのリリースの履歴は、以下の通りである。

<table>
<caption>Scientific Linux</caption>
<thead>
<tr class="header">
<th><p>バージョン</p></th>
<th><p>リリース<br />
年-月-日</p></th>
<th><p>ベースとなった<br />
RHELのリリース日</p></th>
<th><p>名前（公式）</p></th>
<th><p>名前 (<a href="../Page/コードネーム.md" title="wikilink">コードネーム</a>)</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>3.0.1</p></td>
<td><p>2004-05-10</p></td>
<td><p>2004-01-16</p></td>
<td><p>Scientific Linux 3.0.1</p></td>
<td><p>Feynman</p></td>
</tr>
<tr class="even">
<td><p>3.0.2</p></td>
<td><p>2004-06-21</p></td>
<td><p>2004-05-18</p></td>
<td><p>Scientific Linux 3.0.2</p></td>
<td></td>
</tr>
<tr class="odd">
<td><p>3.0.3</p></td>
<td><p>2004-10-01</p></td>
<td><p>2004-09-03</p></td>
<td><p>Scientific Linux 3.0.3</p></td>
<td></td>
</tr>
<tr class="even">
<td><p>3.0.4</p></td>
<td><p>2005-02-11</p></td>
<td><p>2004-12-21</p></td>
<td><p>Scientific Linux 3.0.4</p></td>
<td></td>
</tr>
<tr class="odd">
<td><p>3.0.5</p></td>
<td><p>2005-07-25</p></td>
<td><p>2005-05-20</p></td>
<td><p>Scientific Linux 3.0.5</p></td>
<td></td>
</tr>
<tr class="even">
<td><p>3.0.7</p></td>
<td><p>2006-05-26</p></td>
<td><p>2006-03-15</p></td>
<td><p>Scientific Linux 3.0.7</p></td>
<td></td>
</tr>
<tr class="odd">
<td><p>3.0.8</p></td>
<td><p>2006-10-31</p></td>
<td><p>2006-07-20</p></td>
<td><p>Scientific Linux 3.0.8</p></td>
<td></td>
</tr>
<tr class="even">
<td><p>3.0.9</p></td>
<td><p>2007-10-12</p></td>
<td><p>2007-06-11</p></td>
<td><p>Scientific Linux 3.0.9</p></td>
<td><p>Legacy</p></td>
</tr>
<tr class="odd">
<td><p>4.0</p></td>
<td><p>2005-04-20</p></td>
<td><p>2005-02-15</p></td>
<td><p>Scientific Linux 4.0</p></td>
<td><p>Beryllium</p></td>
</tr>
<tr class="even">
<td><p>4.1</p></td>
<td><p>2005-08-06</p></td>
<td><p>2005-06-09</p></td>
<td><p>Scientific Linux 4.1</p></td>
<td></td>
</tr>
<tr class="odd">
<td><p>4.2</p></td>
<td><p>2005-11-22</p></td>
<td><p>2005-10-05</p></td>
<td><p>Scientific Linux 4.2</p></td>
<td></td>
</tr>
<tr class="even">
<td><p>4.3</p></td>
<td><p>2006-05-08</p></td>
<td><p>2006-03-07</p></td>
<td><p>Scientific Linux 4.3</p></td>
<td></td>
</tr>
<tr class="odd">
<td><p>4.4</p></td>
<td><p>2006-10-09</p></td>
<td><p>2006-08-10</p></td>
<td><p>Scientific Linux 4.4</p></td>
<td></td>
</tr>
<tr class="even">
<td><p>4.5</p></td>
<td><p>2007-06-25</p></td>
<td><p>2007-05-01</p></td>
<td><p>Scientific Linux 4.5</p></td>
<td></td>
</tr>
<tr class="odd">
<td><p>4.6</p></td>
<td><p>2008-03-12</p></td>
<td><p>2007-11-15</p></td>
<td><p>Scientific Linux 4.6</p></td>
<td></td>
</tr>
<tr class="even">
<td><p>4.7</p></td>
<td><p>2008-09-03</p></td>
<td><p>2008-07-24</p></td>
<td><p>Scientific Linux 4.7</p></td>
<td></td>
</tr>
<tr class="odd">
<td><p>4.8</p></td>
<td><p>2009-07-28</p></td>
<td><p>2009-05-18</p></td>
<td><p>Scientific Linux 4.8</p></td>
<td></td>
</tr>
<tr class="even">
<td><p>4.9</p></td>
<td><p>2011-04-21</p></td>
<td><p>2011-02-16</p></td>
<td><p>Scientific Linux 4.9</p></td>
<td></td>
</tr>
<tr class="odd">
<td><p>5.0</p></td>
<td><p>2007-05-04</p></td>
<td><p>2007-03-14</p></td>
<td><p>Scientific Linux 5.0</p></td>
<td><p>Boron</p></td>
</tr>
<tr class="even">
<td><p>5.1</p></td>
<td><p>2008-01-16</p></td>
<td><p>2007-11-07</p></td>
<td><p>Scientific Linux 5.1</p></td>
<td></td>
</tr>
<tr class="odd">
<td><p>5.2</p></td>
<td><p>2008-06-26</p></td>
<td><p>2008-05-21</p></td>
<td><p>Scientific Linux 5.2</p></td>
<td></td>
</tr>
<tr class="even">
<td><p>5.3</p></td>
<td><p>2009-03-19</p></td>
<td><p>2009-01-20</p></td>
<td><p>Scientific Linux 5.3</p></td>
<td></td>
</tr>
<tr class="odd">
<td><p>5.4</p></td>
<td><p>2009-11-04</p></td>
<td><p>2009-09-02</p></td>
<td><p>Scientific Linux 5.4</p></td>
<td></td>
</tr>
<tr class="even">
<td><p>5.5</p></td>
<td><p>2010-05-19</p></td>
<td><p>2010-03-30</p></td>
<td><p>Scientific Linux 5.5</p></td>
<td></td>
</tr>
<tr class="odd">
<td><p>5.6</p></td>
<td><p>2011-06-21</p></td>
<td><p>2011-01-12</p></td>
<td><p>Scientific Linux 5.6</p></td>
<td></td>
</tr>
<tr class="even">
<td><p>5.7</p></td>
<td><p>2011-09-14</p></td>
<td><p>2011-04-21</p></td>
<td><p>Scientific Linux 5.7</p></td>
<td></td>
</tr>
<tr class="odd">
<td><p>5.8</p></td>
<td><p>2012-04-24</p></td>
<td><p>2013-02-21</p></td>
<td><p>Scientific Linux 5.8</p></td>
<td></td>
</tr>
<tr class="even">
<td><p>5.9</p></td>
<td><p>2013-02-05</p></td>
<td><p>2013-01-08</p></td>
<td><p>Scientific Linux 5.9</p></td>
<td></td>
</tr>
<tr class="odd">
<td><p>5.10</p></td>
<td><p>2013-11-12</p></td>
<td><p>2013-09-30</p></td>
<td><p>Scientific Linux 5.10</p></td>
<td></td>
</tr>
<tr class="even">
<td><p>5.11</p></td>
<td><p>2014-11-13</p></td>
<td><p>2014-09-16</p></td>
<td><p>Scientific Linux 5.11</p></td>
<td></td>
</tr>
<tr class="odd">
<td><p>6.0</p></td>
<td><p>2011-03-03</p></td>
<td><p>2010-11-10</p></td>
<td><p>Scientific Linux 6.0</p></td>
<td><p>Carbon</p></td>
</tr>
<tr class="even">
<td><p>6.1</p></td>
<td><p>2011-07-28</p></td>
<td><p>2011-05-19</p></td>
<td><p>Scientific Linux 6.1</p></td>
<td></td>
</tr>
<tr class="odd">
<td><p>6.2</p></td>
<td><p>2012-02-15</p></td>
<td><p>2011-12-06</p></td>
<td><p>Scientific Linux 6.2</p></td>
<td></td>
</tr>
<tr class="even">
<td><p>6.3</p></td>
<td><p>2012-08-09</p></td>
<td><p>2012-06-20</p></td>
<td><p>Scientific Linux 6.3</p></td>
<td></td>
</tr>
<tr class="odd">
<td><p>6.4</p></td>
<td><p>2013-03-28</p></td>
<td><p>2013-02-21</p></td>
<td><p>Scientific Linux 6.4</p></td>
<td></td>
</tr>
<tr class="even">
<td><p>6.5</p></td>
<td><p>2014-01-31</p></td>
<td><p>2013-11-21</p></td>
<td><p>Scientific Linux 6.5</p></td>
<td></td>
</tr>
<tr class="odd">
<td><p>6.6</p></td>
<td><p>2014-11-12</p></td>
<td><p>2014-10-14</p></td>
<td><p>Scientific Linux 6.6</p></td>
<td></td>
</tr>
<tr class="even">
<td><p>6.7</p></td>
<td><p>2015-8-26</p></td>
<td><p>2015-7-22</p></td>
<td><p>Scientific Linux 6.7</p></td>
<td></td>
</tr>
<tr class="odd">
<td><p>6.8</p></td>
<td><p>2016-7-15</p></td>
<td><p>2016-5-10</p></td>
<td><p>Scientific Linux 6.8</p></td>
<td></td>
</tr>
<tr class="even">
<td><p>6.9</p></td>
<td><p>2017-4-17</p></td>
<td><p>2017-3-21</p></td>
<td><p>Scientific Linux 6.9</p></td>
<td></td>
</tr>
<tr class="odd">
<td><p>6.10</p></td>
<td><p>2018-7-10</p></td>
<td><p>2018-6-19</p></td>
<td><p>Scientific Linux 6.10</p></td>
<td></td>
</tr>
<tr class="even">
<td><p>7.0</p></td>
<td><p>2014-10-13</p></td>
<td><p>2014-6-10</p></td>
<td><p>Scientific Linux 7.0</p></td>
<td><p>Nitrogen</p></td>
</tr>
<tr class="odd">
<td><p>7.1</p></td>
<td><p>2015-4-13</p></td>
<td><p>2015-3-5</p></td>
<td><p>Scientific Linux 7.1</p></td>
<td></td>
</tr>
<tr class="even">
<td><p>7.2</p></td>
<td><p>2016-2-5</p></td>
<td><p>2015-11-19</p></td>
<td><p>Scientific Linux 7.2</p></td>
<td></td>
</tr>
<tr class="odd">
<td><p>7.3</p></td>
<td><p>2017-1-25</p></td>
<td><p>2016-11-3</p></td>
<td><p>Scientific Linux 7.3</p></td>
<td></td>
</tr>
<tr class="even">
<td><p>7.4</p></td>
<td><p>2017-10-2</p></td>
<td><p>2017-7-31</p></td>
<td><p>Scientific Linux 7.4</p></td>
<td></td>
</tr>
<tr class="odd">
<td><p>7.5</p></td>
<td><p>2018-5-10</p></td>
<td><p>2018-4-10</p></td>
<td><p>Scientific Linux 7.5</p></td>
<td></td>
</tr>
<tr class="even">
<td><p>7.6</p></td>
<td><p>2018-12-3</p></td>
<td><p>2018-10-30</p></td>
<td><p>Scientific Linux 7.6</p></td>
<td></td>
</tr>
<tr class="odd">
<td><p>7.7</p></td>
<td><p>2019-8-26</p></td>
<td><p>2019-7-28</p></td>
<td><p>Scientific Linux 7.6</p></td>
<td></td>
</tr>
</tbody>
</table>

## 関連項目

  - [フェルミ国立加速器研究所](../Page/フェルミ国立加速器研究所.md "wikilink")
  - [欧州原子核研究機構](../Page/欧州原子核研究機構.md "wikilink")（CERN）
  - [Linuxディストリビューションの比較](../Page/Linuxディストリビューションの比較.md "wikilink")
  - [コンピュータ・クラスター](../Page/コンピュータ・クラスター.md "wikilink")

## 脚注

<references/>

## 外部リンク

  - [Scientific Linux](http://www.scientificlinux.org/) (公式サイト - 英語)
  - [CERN Linux](http://linux.web.cern.ch/linux/) （公式サイト - 英語）
  - [Scientific Linux Tips](http://ribf.riken.jp/comp/tips/SL3.html) （Scientific Linux のインストールのヒント - 日本語）
  - [ScientificLinux-FAQ - 2ch-Linux-Beginners](http://www12.atwiki.jp/linux2ch/pages/36.html) (Scientific Linux に関するFAQ - 日本語)

[Category:Linuxディストリビューション](https://ja.wikipedia.org/wiki/Category:Linuxディストリビューション "wikilink") [Category:2004年のソフトウェア](https://ja.wikipedia.org/wiki/Category:2004年のソフトウェア "wikilink") [Category:フェルミラボ](https://ja.wikipedia.org/wiki/Category:フェルミラボ "wikilink") [Category:CERNのソフトウェア](https://ja.wikipedia.org/wiki/Category:CERNのソフトウェア "wikilink")

1.  [Welcome to Scientific Linux (SL)](https://www.scientificlinux.org/)
2.  [General Questions about Scientific Linux (Community)](https://www.scientificlinux.org/documentation/faq/faq-community/)
3.
4.
5.
6.
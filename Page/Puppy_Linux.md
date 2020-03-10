> この記事は[Puppy Linux](https://ja.wikipedia.org/wiki/Puppy_Linux)から翻訳されています。


**Puppy Linux**（**パピーリナックス**）とは、軽量化された[Linuxディストリビューション](../Page/Linuxディストリビューション.md "wikilink")の1つである。独自に開発された[Live CDの](https://ja.wikipedia.org/wiki/Live_CD "wikilink")[Linuxディストリビューション](../Page/Linuxディストリビューション.md "wikilink")であり、3.0以前は[Slackware](../Page/Slackware.md "wikilink")と高い互換性を持っていた。現在はSlackware・[Ubuntu](https://ja.wikipedia.org/wiki/Ubuntu "wikilink")・Debianをベースにした各バージョンが開発・公開されており、それぞれのパッケージ利用が可能となっている。 単に **Puppy** と略して呼ばれることもある。

## 概要

ハードディスクにインストールする必要がないLive CDとして、全てCDから起動させることが可能である。広く一般に公開され、[GPLライセンスに従って配布されており](../Page/GNU_General_Public_License.md "wikilink")、無償で利用することが可能である。パピー（子犬）がそのマスコットになっている。

## 特徴

  - Live CDとして提供されるが、ハードディスク及びUSBメモリへのインストールも可能。「フルーガル(frugal)インストール」が推奨されている。システムはsfs([SquashFS](https://ja.wikipedia.org/wiki/squashfs "wikilink"))形式の圧縮ファイルにまとめられており、個人設定は差分としてメディアやハードディスクに保存できる。また、オフィスソフトやブラウザのようなサイズの大きいアプリケーションは、追加のsfsとして提供されることが多い。
  - 動作保証する環境が、CPUがPentium 166MMX、メインメモリが128MB(〜4.x系)・256MB(5.x系)であり古いパソコンでも動作可能\[1\]だったが、現在は最低でもメインメモリが768MB(6.x系)・1GB(7.x系)必要になる。
  - 起動時にRAMへシステムを読み込み利用する仕組みで、ハードディスクが無くても運用できる。
  - 起動時以外はLive CDが不要であるため、CDドライブを他の目的に使用可能。ただし、システムの読み込みの際には20倍速以上のCDROMドライブを装備していることが望ましい。
  - パッケージの基本的な管理は、PETパッケージ・マネージャーによって行う。採用されているパッケージ形式は、PET。その実態はディレクトリ構成＋インストール情報をパッケージしたtgz,txzファイルである。
  - リマスタリング機能を利用することで、ユーザーは独自にカスタマイズしたLive CDを容易に作成することが可能。
  - 主要アプリケーション及びライブラリをSlackware、Ubuntu、Debianから移植している他、多くのアプリケーションがスクリプトによって構築されている。
  - 4.3以降の版ではパッケージマネージャが[Debian](../Page/Debian.md "wikilink")、Ubuntuなどで使用されている[.debパッケージに標準対応し](https://ja.wikipedia.org/wiki/deb_\(ファイルフォーマット\) "wikilink")、Ubuntuのパッケージを利用できるようになった。ただし、ライブラリの不足により動作しない場合がある。

## 推奨環境

バージョンによって異なる。1例として、tahrpup 6.0.5 CE の場合。

  - プロセッサ: 1GHz [Pentium 4](../Page/Pentium_4.md "wikilink")
  - メモリ: 768MB
  - ブート可能な CDドライブ、USB接続のドライブなど。内蔵 HDDは必須ではない。

## 歴史

オーストラリアの Barry Kauler によって開発された Linuxディストリビューションである。公式ウェブサイトでは英語版がその公式なリリースとして公開されているが、現在世界的な人気を得て各国語版に改編されたバージョンが多く存在し、\[2\]公認された日本語版も存在する。

## リリース

主なバージョンおよびリリース日は以下の通り。

### バージョン 4 まで

<table>
<thead>
<tr class="header">
<th><p>バージョン</p></th>
<th><p>リリース日</p></th>
<th><p>備考</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>0.1</p></td>
<td><p><a href="../Page/2003年.md" title="wikilink">2003年</a><a href="../Page/6月18日.md" title="wikilink">6月18日</a>[3]</p></td>
<td><p>初公開</p></td>
</tr>
<tr class="even">
<td><p>1.0</p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/2005年" title="wikilink">2005年</a><a href="../Page/3月29日.md" title="wikilink">3月29日</a>[4]</p></td>
<td></td>
</tr>
<tr class="odd">
<td><p>2.0</p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/2006年" title="wikilink">2006年</a><a href="../Page/6月1日.md" title="wikilink">6月1日</a>[5]</p></td>
<td></td>
</tr>
<tr class="even">
<td><p>2.16.1JP</p></td>
<td><p><a href="../Page/2007年.md" title="wikilink">2007年</a><a href="../Page/7月17日.md" title="wikilink">7月17日</a>[6]</p></td>
<td><p>初の正式日本語版がリリースされた。</p></td>
</tr>
<tr class="odd">
<td><p>3.0</p></td>
<td><p>2007年<a href="../Page/10月14日.md" title="wikilink">10月14日</a>[7]</p></td>
<td></td>
</tr>
<tr class="even">
<td><p>4.0</p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/2008年" title="wikilink">2008年</a><a href="../Page/5月5日.md" title="wikilink">5月5日</a>[8]</p></td>
<td><p>T2プロジェクトからアプリケーション及びライブラリのソース取り込み。<br />
GTK2 を使用するプログラムのみで構成し、UIの統一。</p></td>
</tr>
<tr class="odd">
<td><p>4.1</p></td>
<td><p>2008年<a href="../Page/10月6日.md" title="wikilink">10月6日</a>[9]</p></td>
<td><p>起動スクリプトの見直しによって起動時間の短縮が図られた。</p></td>
</tr>
<tr class="even">
<td><p>4.2</p></td>
<td><p><a href="../Page/2009年.md" title="wikilink">2009年</a><a href="../Page/3月28日.md" title="wikilink">3月28日</a>[10]</p></td>
<td><p>Barry K　以外の人物（フォーラムメンバー)がプロジェクトリーダーを務めた。<br />
WindowsVistaを意識したデスクトップ。</p></td>
</tr>
<tr class="odd">
<td><p>4.3</p></td>
<td><p>2009年<a href="../Page/9月18日.md" title="wikilink">9月18日</a>[11]</p></td>
<td><p>Barry K プロジェクトリーダーに復帰。4.12以前の簡素なデスクトップとなる。</p></td>
</tr>
<tr class="even">
<td></td>
<td></td>
<td></td>
</tr>
</tbody>
</table>

### バージョン 5 以降

バージョン 5以降の Puppy Linux はいくつかの系列に分かれている。これまでにも Barry K 以外の人物がプロジェクトリーダーを務める、コミュニティ・エディションと呼ばれるもの（バージョン 4.2 など) があった。また、「公式」ではない派生も多く存在した。バージョン 5以降はむしろそれら派生の中から Barry K が後付けで「公式」と宣言した経緯のものがある。Playdayz が主宰する Lucid Puppy(Lupu)、01micko が主宰する Slacko の2つがそれである。この2つが「公式」と宣言された後に、Barry K 自身も Wary、続いて Racy を開発したために、これらの系列が並列することとなった。その後 Barry K は Precise Puppy の開発に着手。Wary/Racyはサービスパック5.5.1 を最後に、Precise Puppy に集約される見込み\[12\]。

#### Precise Puppy

Barry K による開発。Ubuntu 12.04.1(Precise Pangolin) とバイナリ互換。Ubuntuの膨大なリポジトリにアクセスできる。Precise Pangolinは5年間のLTS（Long Term Support、長期サポート）であるため、Precise Puppyも同等に扱われる。PAEカーネルが通常となり、non-PAEは"retro"という扱いになった。

| バージョン               | リリース日                                                                          | 備考 |
| ------------------- | ------------------------------------------------------------------------------ | -- |
| Precise Puppy 5.4   | [2012年](../Page/2012年.md "wikilink")[10月23日](../Page/10月23日.md "wikilink")     |    |
| Precise Puppy 5.5   | [2013年](../Page/2013年.md "wikilink")[3月10日](../Page/3月10日.md "wikilink")\[13\] |    |
| Precise Puppy 5.6   | 2013年[5月21日](../Page/5月21日.md "wikilink")\[14\]                                |    |
| Precise Puppy 5.7   | 2013年[7月29日](../Page/7月29日.md "wikilink")\[15\]                                |    |
| Precise Puppy 5.7.1 | 2013年[8月3日](../Page/8月3日.md "wikilink")\[16\]                                  |    |

#### Slacko Puppy

01micko をリーダーとするプロジェクトチームによる開発。Slackware ベース。カーネル、ライブラリに比較的新しいものを採用。32bitOSながら 4GB超えのRAMをサポートする PAEカーネルのものもリリースしている。

| バージョン              | リリース日                                                                                           | 備考 |
| ------------------ | ----------------------------------------------------------------------------------------------- | -- |
| Slacko Puppy 5.4   | [2012年](../Page/2012年.md "wikilink")[12月2日](../Page/12月2日.md "wikilink")\[17\]                  |    |
| Slacko Puppy 5.5   | [2013年](../Page/2013年.md "wikilink")[3月6日](https://ja.wikipedia.org/wiki/3月6日 "wikilink")\[18\] |    |
| Slacko Puppy 5.6   | 2013年[8月13日](../Page/8月13日.md "wikilink")\[19\]                                                 |    |
| Slacko Puppy 5.7   | 2014年[5月10日](../Page/5月10日.md "wikilink")\[20\]                                                 |    |
| Slacko Puppy 6.0   | 2014年[10月24日](../Page/10月24日.md "wikilink")\[21\]                                               |    |
| Slacko Puppy 6.3   | 2015年[11月16日](https://ja.wikipedia.org/wiki/11月16日 "wikilink")\[22\]                            |    |
| Slacko Puppy 6.3.2 | 2016年[6月23日](../Page/6月23日.md "wikilink")\[23\]                                                 |    |
|                    |                                                                                                 |    |

#### Wary Puppy・Racy Puppy

Barry K による開発。T2ベース。Xサーバーは Puppy 4.x系と同じで、比較的古いハードウェア（グラフィック・カード）のサポートを意図している。RacyはWaryに比べ新しいカーネルや Xサーバーを採用し、最近のハードウェアへのサポートを意図している。カーネルと Xサーバー以外は基本的にWaryとRacyで同じ。バージョン 5.2.2 から WaryとRacyが基本的に同時リリースされている。

| バージョン             | リリース日                                                                                                                  | 備考                              |
| ----------------- | ---------------------------------------------------------------------------------------------------------------------- | ------------------------------- |
| Wary 5.0          | [2010年](https://ja.wikipedia.org/wiki/2010年 "wikilink")[12月29日](https://ja.wikipedia.org/wiki/12月29日 "wikilink")\[24\] | Barry KによるWary(慎重なパピー)最初の正式リリース |
| Wary / Racy 5.5   | [2013年](../Page/2013年.md "wikilink")[3月3日](../Page/3月3日.md "wikilink")\[25\]                                           |                                 |
| Wary / Racy 5.5.1 | [2013年](../Page/2013年.md "wikilink")[5月13日](../Page/5月13日.md "wikilink")\[26\]                                         | サービスパックのみのリリース                  |
|                   |                                                                                                                        |                                 |

バージョン5.5へのサービスパック(5.5.1)を最後に、今後は Precise Puppy に集約される見込み\[27\]。

#### Lucid Puppy

Playdayzをリーダーとするプロジェクトチームによる開発。Ubuntu 10(Lucid) とバイナリ互換。カーネル 2.6.33.2 や主要ライブラリを変更することなく改良、保守が続けられた。Lupu-5.2.8-005 を最後に更新対象から外されている。

| バージョン           | リリース日                                                                                             | 備考 |
| --------------- | ------------------------------------------------------------------------------------------------- | -- |
| Lucid Puppy 5.0 | [2010年](https://ja.wikipedia.org/wiki/2010年 "wikilink")[5月15日](../Page/5月15日.md "wikilink")\[28\] |    |
| Lucid Puppy 5.1 | 2010年[8月13日](../Page/8月13日.md "wikilink")\[29\]                                                   |    |
|                 |                                                                                                   |    |

#### Raring Puppy

Barry K による開発。Ubuntu 13.04(Raring Ringtail) とバイナリ互換。現在アルファ版のみが公開されている。

| バージョン                  | リリース日                                                                                                                | 備考 |
| ---------------------- | -------------------------------------------------------------------------------------------------------------------- | -- |
| Raring Puppy 5.7alpha1 | [2010年](https://ja.wikipedia.org/wiki/2010年 "wikilink")[6月16日](https://ja.wikipedia.org/wiki/6月16日 "wikilink")\[30\] |    |
| 5.6.94 (5.7alpha2)     | 2010年[6月29日](../Page/6月29日.md "wikilink")\[31\]                                                                      |    |
|                        |                                                                                                                      |    |

#### tahrpup CE

666philb が取りまとめ役を務めるプロジェクト。Ubuntu 14.04 (Trusty Tahr) とバイナリ互換。この系列の公式最新版は 6.0.5 で、カーネルは 32bit版が 3.14.56, 64bit版が 3.14.54 である。32bit版の iso は PAE カーネルのものと noPAE カーネルのものが用意されている。

| バージョン         | リリース日                                                                        | 備考 |
| ------------- | ---------------------------------------------------------------------------- | -- |
| Tahrpup 6.0.0 | [2014年](../Page/2014年.md "wikilink")[3月9日](../Page/3月9日.md "wikilink")\[32\] |    |
| Tahrpup 6.0.5 | 2015年[12月20日](../Page/12月20日.md "wikilink")\[33\]                            |    |
|               |                                                                              |    |

#### xenialpup CE

666philb が取りまとめ役を務めるプロジェクト。Ubuntu 16.04 (Xenial Xerus) とバイナリ互換。7.0.x として開発が進み、公式版は 7.5 と付番された。カーネルは 32bit版が 4.4.95 noPAE, 64bit版が 4.9.58 である。

| バージョン         | リリース日                                             | 備考 |
| ------------- | ------------------------------------------------- | -- |
| Xenialpup 7.5 | 2017年[11月25日](../Page/11月25日.md "wikilink")\[34\] |    |
|               |                                                   |    |

#### bionicpup32・bionicpup64 CE

Ubuntu 18.04 (Bionic Beaver) とバイナリ互換。32bit版は peebee を中心として UPupBB の名称で開発が進められたが、公式版リリースにあたり bionicpup32 8.0 と命名された。(カーネル 4.9.163 PAE) 一方、64bit版は当初から bionicpup64 として、666philb をリーダーとして開発が進められ、公式版は 8.0 と付番された。(カーネル 4.19.23) 開発の経緯から、32bit版と 64bit版で収録されているアプリケーションの一部が異なる。

| バージョン         | リリース日                                           | 備考 |
| ------------- | ----------------------------------------------- | -- |
| Bionicpup 8.0 | 2019年[3月24日](../Page/3月24日.md "wikilink")\[35\] |    |
|               |                                                 |    |

## パピーリナックス日本語版

**パピーリナックス日本語版**は有志によって英語版を日本語化し、日本語を母語とする初心者でも使いやすいようにアプリケーションの追加・修正をしているバージョンである。

### リリース

| バージョン                | リリース日                                                                                           | 備考                                           |
| -------------------- | ----------------------------------------------------------------------------------------------- | -------------------------------------------- |
| パピーリナックス 2.16.1 日本語版 | [2007年](../Page/2007年.md "wikilink")[7月17日](../Page/7月17日.md "wikilink")\[36\]                  | 初の正式日本語版がリリース。                               |
| パピーリナックス 3.01 日本語版   | 2007年[11月28日](../Page/11月28日.md "wikilink")\[37\]                                               | 3.x 系の日本語版リリース。                              |
| パピーリナックス 4.0 日本語版    | [2008年](https://ja.wikipedia.org/wiki/2008年 "wikilink")[7月2日](../Page/7月2日.md "wikilink")\[38\] | 4.x 系の日本語版リリース。                              |
| パピーリナックス 4.1.1 日本語版  | 2008年[12月6日](../Page/12月6日.md "wikilink")\[39\]                                                 |                                              |
| パピーリナックス 4.1.2 日本語版  | [2009年](../Page/2009年.md "wikilink")[1月19日](../Page/1月19日.md "wikilink")\[40\]                  |                                              |
| パピーリナックス 4.2 日本語版    | 2009年[5月27日](../Page/5月27日.md "wikilink")\[41\]                                                 |                                              |
| パピーリナックス 4.3 日本語版    | 2009年[10月14日](../Page/10月14日.md "wikilink")\[42\]                                               |                                              |
| パピーリナックス 4.3.1 日本語版  | 2009年[12月1日](../Page/12月1日.md "wikilink")\[43\]                                                 | 日本語版では独自の改善が加えられている。                         |
| Wary-511-01J         | [2011年](../Page/2011年.md "wikilink")[4月18日](../Page/4月18日.md "wikilink")\[44\]                  | Wary 5.1のbugfixとアプリのVerUp。日本語版独自の改善が加えられている。 |
| 431JP2012            | [2012年](../Page/2012年.md "wikilink")[3月15日](../Page/3月15日.md "wikilink")                        | 4.3.1日本語版リリース以降2年余の改良成果を加えた。日本語版独自のリリース。     |
| Lupu-528JP           | 2012年[7月27日](../Page/7月27日.md "wikilink")\[45\]                                                 | Lucid 5.2.8.005をベースに日本語化、日本語版独自の改良も加えられている。  |
| Precise-550JP        | [2013年](../Page/2013年.md "wikilink")[6月14日](../Page/6月14日.md "wikilink")\[46\]                  | Precise 5.5をベースに日本語化。                        |
| Precise-571JP        | [2014年](../Page/2014年.md "wikilink")[1月18日](../Page/1月18日.md "wikilink")\[47\]                  | Precise 5.7.1-retroをベースに日本語化。                |

## 脚注

### 注釈

### 出典

## 関連項目

  - [Live CD](https://ja.wikipedia.org/wiki/Live_CD "wikilink")
  - [Linuxディストリビューションの比較](https://ja.wikipedia.org/wiki/Linuxディストリビューションの比較 "wikilink")
  - [Linuxライブディストリビューションの比較](https://ja.wikipedia.org/wiki/Linuxライブディストリビューションの比較 "wikilink")

## 外部リンク

### 日本語

  - [パピーリナックス 日本語版](http://openlab.jp/puppylinux/)
  - [Puppy Linux 日本語版 アーカイブ(ミラー)](http://www.ring.gr.jp/archives/linux/puppylinux/)
  - [パピーリナックス日本語フォーラム](https://sakurapup.browserloadofcoolness.com/)・・・2019年9月21日復旧。
  - [Puppy Linux 日本語版(ミラー)](https://sakurapup.com/puppylinux/)
  - [Puppy Linux 日本語版(OSDN)](https://osdn.jp/projects/puppylinux-jp/)・・・ドキュメントのみ。ファイルはありません。
  - [パピーリナックス日本語フォーラム(仮)](https://sakurapup.com/puppyjpforum/index.php)・・・「ユーザーズカフェ」のみで仮運用中。

### 英語

  - [Puppy Linux](http://www.puppylinux.com/)
  - [Puppy Linux Community](http://www.puppylinux.org/)
  - [Puppy Linux Discussion Forum](http://www.murga-linux.com/puppy/)

[Category:Linuxディストリビューション](https://ja.wikipedia.org/wiki/Category:Linuxディストリビューション "wikilink") [Category:LiveCD](https://ja.wikipedia.org/wiki/Category:LiveCD "wikilink")

1.  近年は大容量のメモリに対応する PAE 対応版も配布されるようになり、日本語版では Precise-550JP が PAE 対応のみで配布されている。
2.
3.
4.
5.
6.
7.
8.
9.
10.
11.
12.
13.
14.
15.
16.
17.
18.
19.
20.
21.
22.
23.
24.
25.
26.
27.
28.
29.
30.
31.
32.
33.
34.
35.
36.
37.
38.
39.
40.
41.
42.
43.
44.
45.
46.
47.
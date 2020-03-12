> この記事は[Gentoo Linux](https://ja.wikipedia.org/wiki/Gentoo_Linux)から翻訳されています。


**Gentoo Linux**（ジェンツー・リナックス\[1\]\[2\]\[3\]\[4\]）とは、[Linuxディストリビューション](../Page/Linuxディストリビューション.md "wikilink")の一つである。[パッケージ管理システム](../Page/パッケージ管理システム.md "wikilink")に[Portage](../Page/Portage.md "wikilink")を採用しており、[プロプライエタリ](https://ja.wikipedia.org/wiki/プロプライエタリ "wikilink")なソフトウェアも含んでいる。

## 概要

他の多数の[Linuxディストリビューション](../Page/Linuxディストリビューション.md "wikilink")と異なる点がいくつかあり、その一つに挙げられるのが自分でソフトウェアを[コンパイル](https://ja.wikipedia.org/wiki/コンパイル "wikilink")する、ということである。その際、ユーザーは比較的簡単に[コンパイル](https://ja.wikipedia.org/wiki/コンパイル "wikilink")オプションを調整することができる。また、一部のソフトウェア（[Mozilla Firefox](../Page/Mozilla_Firefox.md "wikilink") や [OpenOffice.org](../Page/OpenOffice.org.md "wikilink")など）では環境にあった最適化などを犠牲に、導入時間の短縮などを目的として他の[Linuxディストリビューション](../Page/Linuxディストリビューション.md "wikilink")などでみられるような予め[コンパイル](https://ja.wikipedia.org/wiki/コンパイル "wikilink")されたソフトウェアパッケージを導入することもできる。 また、インストールの方法も特徴的である。インストールハンドブックで推奨されている方法は、LiveCDでシステムを起動し、[Linuxカーネル](../Page/Linuxカーネル.md "wikilink")など、最小限起動に必要な実行ファイルをインターネット経由でダウンロードし、Chrootコマンドなどを実行した後、[Portage](../Page/Portage.md "wikilink")を使ってシステムを構築していく、というものである。 Gentooはその「無限に近い適応性」のために、メタディストリビューションと説明されることもある\[5\]。 マスコットキャラクターは、Larry the Cow\[6\]。**Gentoo**という名称は、[ジェンツーペンギン](../Page/ジェンツーペンギン.md "wikilink")が由来とされる。

## Portage

[Portage](../Page/Portage.md "wikilink")はGentooシステムの核となる[パッケージ管理システム](../Page/パッケージ管理システム.md "wikilink")である。

Portageでは、パッケージのインストール手順を記した[ebuild](https://ja.wikipedia.org/wiki/ebuild "wikilink")と呼ばれる[スクリプト](../Page/スクリプト.md "wikilink")を参照してシステムを構築する。 パッケージ管理コマンド[emerge](https://ja.wikipedia.org/wiki/emerge "wikilink")が、ebuildに従って[ソースコード](../Page/ソースコード.md "wikilink")を[ダウンロード](https://ja.wikipedia.org/wiki/ダウンロード "wikilink")、[コンパイル](https://ja.wikipedia.org/wiki/コンパイル "wikilink")し、所定のディレクトリにインストールを行なう。 [RPMなどのようなシステムとは違い](../Page/RPM_Package_Manager.md "wikilink")、[バイナリ](../Page/バイナリ.md "wikilink")ではなくソースコードから構築を行うのが大きな特徴の一つである。

ソースコードから構築するという特性を生かし、事前に[USEフラグ](https://ja.wikipedia.org/wiki/USEフラグ "wikilink")を指定しておくことにより、必要に応じてパッケージの機能を取捨選択してコンパイルを行うことができる。 このため、全体として柔軟性やカスタマイズ性が非常に高い。 また、共通のバイナリパッケージを使うのではなく、[CPU](../Page/CPU.md "wikilink")の特性に合わせてバイナリを作成できるのでパフォーマンスも高くなる。 異なるアーキテクチャでも同じebuildを使用するので、メンテナンス性、[移植性](../Page/移植性.md "wikilink")も高い。

その一方、性能の低いマシンや通信速度が低いマシンで動作させる場合はソースコードのコンパイルやダウンロードに非常に時間がかかるため実用的ではない。 これを補うため、Version 1.4からGRP (Gentoo Reference Platform) が登場した。 これによりあらかじめコンパイルされたパッケージを用いてインストールを素早く行うことができる。 ただし当然のことながら GRP を用いた場合には、ソースコードから構築することで生じる数々の利点を享受できない。

Portageのカスタマイズ性の高さから、[Google Chrome OSは基盤となるLinuxシステムのディストリビューションにGentoo](https://ja.wikipedia.org/wiki/Google_Chrome_OS "wikilink") Linuxを使用している\[7\]。

## 難易度

[インストール](../Page/インストール.md "wikilink")、[X Window System等の設定や](../Page/X_Window_System.md "wikilink")、[日本語](../Page/日本語.md "wikilink")環境構築にはドキュメントが整備されているとはいえ、インストール直後から日本語が使えるというわけではない。このため日本語を[母語](../Page/母語.md "wikilink")とする初心者にとっては取り扱いが非常に難しい。

一方、Portageによって、カーネルやgcc、glibcなどを含むシステム全体の完全なアップグレードが可能なので、一度インストールしてしまえば新しいバージョンを再度インストールする必要がない。

## 対応アーキテクチャ

Gentoo は元々 [x86](https://ja.wikipedia.org/wiki/x86 "wikilink") アーキテクチャー用に設計されたが、[Linux](../Page/Linux.md "wikilink")、[GCC](../Page/GNUコンパイラコレクション.md "wikilink")、[glibc](https://ja.wikipedia.org/wiki/glibc "wikilink") や [Portage](../Page/Portage.md "wikilink") の高移植性により、多くの他の[アーキテクチャーへ移植された](../Page/コンピュータ・アーキテクチャ.md "wikilink")。

  - [x86](https://ja.wikipedia.org/wiki/x86 "wikilink")
  - [PowerPC](../Page/PowerPC.md "wikilink")
  - [PPC970](https://ja.wikipedia.org/wiki/PPC970 "wikilink")
  - [SPARC](../Page/SPARC.md "wikilink")
  - [AMD64](https://ja.wikipedia.org/wiki/x64 "wikilink")
  - [IA-64](../Page/IA-64.md "wikilink")
  - [MIPS](../Page/MIPSアーキテクチャ.md "wikilink")
  - [Alpha](https://ja.wikipedia.org/wiki/DEC_Alpha "wikilink")
  - [HP PA-RISC](../Page/PA-RISC.md "wikilink")
  - [ARM](../Page/ARMアーキテクチャ.md "wikilink")
  - [System z](../Page/System_z.md "wikilink")

## 歴史

### 誕生

  - Gentoo Linuxディストリビューションの誕生\[8\]
  - Enoch発Gentoo行き（「若干の"つまずき"と"いさかい"」経由）\[9\]
  - Linuxからの離脱と復帰\[10\]

### リリースメディア一覧

Gentoo Linuxは、[ローリング・リリース](https://ja.wikipedia.org/wiki/ローリング・リリース "wikilink")モデルを採用しているため、一般的なLinuxディストリビューションの「バージョン番号」にあたる概念は存在しない。

ただし、ある時点でのパッケージを収集した[Live DVDが定期的にリリースされており](https://ja.wikipedia.org/wiki/Live_DVD "wikilink")、これらには便宜上、バージョン番号が付与されている。

  - [2002年](../Page/2002年.md "wikilink")[3月31日](../Page/3月31日.md "wikilink") - Version 1.0 リリース
  - [2002年](../Page/2002年.md "wikilink")[6月5日](https://ja.wikipedia.org/wiki/6月5日 "wikilink") - Version 1.2 リリース
  - [2003年](../Page/2003年.md "wikilink")[7月14日](../Page/7月14日.md "wikilink") - Version 1.4 リリース。このバージョンからGRPが提供されるようになった。
  - [2004年](../Page/2004年.md "wikilink")[2月28日](../Page/2月28日.md "wikilink") - 2004.0 リリース。バージョン番号の表記方法が変更され、2004.0は「2004年の1回目のリリース」、2004.3は「2004年の4回目のリリース」を表すようになった。
  - [2004年](../Page/2004年.md "wikilink")[4月28日](../Page/4月28日.md "wikilink") - 2004.1 リリース。
  - [2004年](../Page/2004年.md "wikilink")[7月26日](../Page/7月26日.md "wikilink") - 2004.2 リリース。
  - [2004年](../Page/2004年.md "wikilink")[11月15日](../Page/11月15日.md "wikilink") - 2004.3 リリース。
  - [2005年](../Page/2005年.md "wikilink")[3月27日](../Page/3月27日.md "wikilink") - 2005.0 リリース。
  - [2005年](../Page/2005年.md "wikilink")[8月8日](../Page/8月8日.md "wikilink") - 2005.1 リリース。
  - [2006年](../Page/2006年.md "wikilink")[2月27日](../Page/2月27日.md "wikilink") - 2006.0 リリース。
  - [2006年](../Page/2006年.md "wikilink")[8月31日](../Page/8月31日.md "wikilink") - 2006.1 リリース。
  - [2007年](../Page/2007年.md "wikilink")[5月7日](../Page/5月7日.md "wikilink") - 2007.0 リリース。
  - [2008年](https://ja.wikipedia.org/wiki/2008年 "wikilink")[7月6日](../Page/7月6日.md "wikilink") - 2008.0 リリース。
  - [2008年](https://ja.wikipedia.org/wiki/2008年 "wikilink")[9月22日](../Page/9月22日.md "wikilink") - 2008.1 リリースのはずであったが、キャンセルされた\[11\]。
  - [2009年](../Page/2009年.md "wikilink")[10月4日](https://ja.wikipedia.org/wiki/10月4日 "wikilink") - 10.0 リリース。Gentoo誕生10周年。バージョン番号の表記方法が変更され、10.0は「10年目の1回目のリリース」、10.1は「10年目の2回目のリリース」を表すようになった。また、Gentoo誕生10周年を記念して特別なLiveDVDが作られた\[12\]。
  - [2009年](../Page/2009年.md "wikilink")[10月10日](../Page/10月10日.md "wikilink") - 10.1 リリース。10.0リリースのバグフィックスを含む。
  - [2011年](../Page/2011年.md "wikilink")[3月8日](../Page/3月8日.md "wikilink") - 11.0 リリース。
  - [2012年](../Page/2012年.md "wikilink")[1月2日](../Page/1月2日.md "wikilink") - 12.0 リリース。
  - [2012年](../Page/2012年.md "wikilink")[4月1日](../Page/4月1日.md "wikilink") - 12.1 リリース。
  - [2012年](../Page/2012年.md "wikilink")[12月21日](../Page/12月21日.md "wikilink") - End Of World Edition リリース。4月にリリースされた12.1がベースとなっている。サブタイトルは古代マヤ暦から連想された[2012年人類滅亡説](https://ja.wikipedia.org/wiki/2012年人類滅亡説 "wikilink")のパロディであり、リリース日もこれにあわせて設定された。
  - [2014年](../Page/2014年.md "wikilink")[8月26日](../Page/8月26日.md "wikilink") - Iron Penguin Edition リリース。
  - [2016年](../Page/2016年.md "wikilink")[5月14日](../Page/5月14日.md "wikilink") - Choice Edition リリース。
  - [2017年](../Page/2017年.md "wikilink")[1月18日](../Page/1月18日.md "wikilink") - Crispy Belgian Waffle Edition リリース。[ベルギー](https://ja.wikipedia.org/wiki/ベルギー "wikilink")が開催地の[FOSDEM](https://ja.wikipedia.org/wiki/FOSDEM "wikilink") 2017で頒布された\[13\]。

## 関連項目

  - [Portage](../Page/Portage.md "wikilink")
  - [ebuild](https://ja.wikipedia.org/wiki/ebuild "wikilink")
  - [Linuxディストリビューションの比較](../Page/Linuxディストリビューションの比較.md "wikilink")

## 注釈

<div class="references-small" style="-moz-column-count:2; column-count:2;">

<references />

</div>

## 外部リンク

  - [Gentoo Linux](http://www.gentoo.org/)
  - [Gentoo Linux Users Group Japan](http://www.gentoo.jp/)
  - [Gentoo Linux x86 ハンドブック](http://www.gentoo.org/doc/ja/handbook/handbook-x86.xml)

[Category:Linuxディストリビューション](https://ja.wikipedia.org/wiki/Category:Linuxディストリビューション "wikilink") [Category:オープンソースソフトウェア](https://ja.wikipedia.org/wiki/Category:オープンソースソフトウェア "wikilink") [Category:2002年のソフトウェア](https://ja.wikipedia.org/wiki/Category:2002年のソフトウェア "wikilink")

1.  [無償Linuxディストリビューション](https://jp.linux.com/resources/use/non-commercial-distribution) Linux.com（[Linux Foundation](../Page/Linux_Foundation.md "wikilink")）
2.  [Linuxディストリビューション](https://www.ossj.jp/databox/category.php/linux_distribution/code) OSS Japan
3.  [Gentoo Linux](http://it-words.jp/i/w/Gentoo20Linux.html) [日立ソリューションズ](https://ja.wikipedia.org/wiki/日立ソリューションズ "wikilink") IT用語辞典
4.  「Linux」の他の読み方については[こちらを参照](https://ja.wikipedia.org/wiki/Linux#「Linux」の読み方 "wikilink")
5.
6.  <http://www.gentoo.org/main/ja/about.xml>
7.
8.  <http://www.ibm.com/developerworks/jp/linux/library/l-dist1/index.html>
9.  <http://www.ibm.com/developerworks/jp/linux/library/l-dist2/index.html>
10. <http://www.ibm.com/developerworks/jp/linux/library/l-dist3/index.html>
11.
12.
13.
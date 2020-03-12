> この記事は[TrueOS](https://ja.wikipedia.org/wiki/TrueOS)から翻訳されています。


**TrueOS**（トゥルーオーエス）は、[FreeBSD](../Page/FreeBSD.md "wikilink")の最新版を簡単にインストールして使用出来るようにしたオペレーティングシステムである。 2016年9月1日以前の名称は、**PC-BSD**（ピーシービーエスディー）であった\[1\]。

「すぐに、簡単に」使えることを目指して作られており、[KDE Software Compilation 4](https://ja.wikipedia.org/wiki/KDE_Software_Compilation_4 "wikilink")、[Lumina](../Page/Lumina.md "wikilink")、[LXDE](https://ja.wikipedia.org/wiki/LXDE "wikilink")、[MATE](https://ja.wikipedia.org/wiki/MATE "wikilink")、[Xfce](../Page/Xfce.md "wikilink")が[グラフィカルユーザインタフェース](https://ja.wikipedia.org/wiki/グラフィカルユーザインタフェース "wikilink") (GUI) として用意され、 また[インストール](../Page/インストール.md "wikilink")の手間を省くためグラフィカルなインストール[プログラムが導入されている](../Page/プログラム_\(コンピュータ\).md "wikilink")。

PC-BSDプロジェクトは現在、実行可能な（ユーザ自身の手で[コンパイルする必要のない](../Page/コンパイラ.md "wikilink")）[ソフトウェア](../Page/ソフトウェア.md "wikilink")パッケージをインストールするためのGUIプログラムを開発中である。

かつてデスクトップ向けのバージョンをTrueOS開発元は開発・配布していたが、しかし現在ではデスクトップ版からは撤退しており、公式サイトから配布されているバージョンはサーバー系のみになっている。デスクトップ版については、別コミュニティである Project Trident などが引き継いだ。

## iXsystemsのPC-BSD販売戦略

  - 2006年10月10日 - [iXsystems](https://ja.wikipedia.org/wiki/iXsystems "wikilink")はPC-BSDを買収し、PC-BSDへの資金提供やエンタープライズクラスの[サーバ](../Page/サーバ.md "wikilink")・[ワークステーション](../Page/ワークステーション.md "wikilink")を市場に投入すると発表した。
  - 2007年04月17日 - [アドビシステムズ](../Page/アドビシステムズ.md "wikilink")と次期バージョンのPC-BSDに、デフォルトで[Flash Playerをインストールした状態で配布することに合意した](../Page/Adobe_Flash.md "wikilink")。
  - 2007年11月14日 - Fry's ElectronicsとPC-BSDの販売契約を締結した。
  - 2008年04月23日 - PC-BSD用のリモートシステム管理とモニタリングソフトウェアを提供するためにNetCraft Communicationsとのパートナーシップを発表した。

## パッケージ管理

2013年1月までPC-BSDの[パッケージ管理システム](../Page/パッケージ管理システム.md "wikilink")は、他の多くのUNIXに似た[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink") (OS) とは異なるアプローチを取っていた。FreeBSDではportsやpackagesを使用するが、PC-BSDでは[拡張子](../Page/拡張子.md "wikilink")*.TXZ*の付いたファイルを使用していた。これらのファイルをダブルクリックするとインストール[ウィザードが起動するというものであった](../Page/ウィザード_\(ソフトウェア\).md "wikilink")。

2013年2月より、FreeBSD 10.0で標準とされる新しいpkg(8)(開発コード名:pkgng)を採用すると発表された。システムアップデートについてはfreebsd-update(8)へと変更される。

2013年3月、pkg/freebsd-updateを採用したISOイメージが公開された。

## ライセンス

[BSDライセンス](../Page/BSDライセンス.md "wikilink")に近い形の[ライセンス](../Page/ライセンス.md "wikilink")を採用している。

PC-BSDは、当初[GNU General Public License](../Page/GNU_General_Public_License.md "wikilink") (GPL)でライセンスされていた。 これについて、「GPLはBSDライセンスの思想と矛盾する」として、一部の人々が批判していた。

GPLが採用されていたのは、PC-BSDプロジェクトがインタフェース開発に[Qt](../Page/Qt.md "wikilink")を使用しており、開発者が「Qtツールキットを使用するアプリケーションはGPLまたは[QPLでライセンスされなければならない](../Page/Q_Public_License.md "wikilink")」と思い込んでいたからである。しかし、これは誤りであり、後にPC-BSDプロジェクトはPC-BSDのコードをBSDライセンスに近い形で改めてライセンスすることとなった。

## システム要件

### 最小構成

  - [amd64](https://ja.wikipedia.org/wiki/amd64 "wikilink")プロセッサ
  - 1GBの[RAM](https://ja.wikipedia.org/wiki/RAM "wikilink")
  - 20GBの[ハードドライブ](https://ja.wikipedia.org/wiki/ハードドライブ "wikilink")空き容量
  - [ネットワークカード](../Page/ネットワークカード.md "wikilink")

### 推奨される設定

  - [amd64](https://ja.wikipedia.org/wiki/amd64 "wikilink")プロセッサ
  - [rEFInd](https://ja.wikipedia.org/wiki/rEFInd "wikilink")をインストールするための[EFI](https://ja.wikipedia.org/wiki/EFI "wikilink")システムパーティション
  - 4GBのRAM
  - デスクトップインストールの場合は[プライマリパーティション](https://ja.wikipedia.org/wiki/プライマリパーティション "wikilink")に30GB 、サーバーインストールの 場合は20GB
  - バックアップサービスのあるインストールには50GBを推奨
  - 3Dアクセラレーション[ビデオカード](../Page/ビデオカード.md "wikilink")
  - ネットワークカード
  - [サウンドカード](../Page/サウンドカード.md "wikilink")

## 今までのリリース

  - 2005年10月13日 - 0.8.2
  - 2005年10月22日 - 0.8.3
  - 2005年11月10日 - 1.0 RC1
  - 2006年01月20日 - 1.0 RC2
  - 2006年04月29日 - 1.0
  - 2006年05月28日 - 1.1
  - 2006年06月19日 - 1.11
  - 2006年07月12日 - 1.2
  - 2006年10月19日 - 1.3 BETA
  - 2006年11月26日 - 1.3 BETA2
  - 2006年12月31日 - 1.3
  - 2007年01月10日 - 1.3.1
  - 2007年01月20日 - 1.3.2
  - 2007年02月14日 - 1.3.3
  - 2007年04月17日 - 1.3.4
  - 2007年07月21日 - 1.4 BETA
  - 2007年08月31日 - 1.4 RC
  - 2007年09月24日 - 1.4
      - リリースネーム: Da Vinci Edition
      - [FreeBSD](../Page/FreeBSD.md "wikilink") 6.2-STABLEベース
      - 1.4よりリリースネームが付くようになった
  - 2007年11月16日 - 1.4.1
  - 2007年12月03日 - 1.4.1.1
  - 2008年01月04日 - 1.4.1.2
  - 2008年03月12日 - 1.5
      - リリースネーム: Edison Edition
      - FreeBSD 6.3ベース
      - 1.5より[x64](https://ja.wikipedia.org/wiki/x64 "wikilink")版もリリース
  - 2008年04月23日 - 1.5.1
  - 2008年08月28日 - 7 BETA1
  - 2008年09月15日 - 7
      - リリースネーム: Fibonacci Edition
      - FreeBSD 7.1-PRERELEASEベース
      - 今回よりバージョンをベースにしているFreeBSDのバージョンに合わせている
  - 2008年10月17日 - 7.0.1
  - 2008年12月10日 - 7.0.2
  - 2009年04月10日 - 7.1
      - リリースネーム: Galileo Edition
      - FreeBSD 7.2-PRERELEASEベース
  - 2009年07月06日 - 7.1.1
  - 2010年02月22日 - 8.0
      - リリースネーム: Hubble Edition
      - FreeBSD 8.0-RELEASEベース
  - 2010年06月06日 - 8.1 BETA1
      - FreeBSD 8.1-PRERELEASEベース
  - 2010年07月20日 - 8.1
      - FreeBSD 8.1-RELEASEベース
  - 2011年02月24日 - 8.2
      - FreeBSD 8.2-RELEASEベース
  - 2012年01月13日 - 9.0
      - リリースネーム: Isotope Edition
      - FreeBSD 9.0-RELEASEベース
  - 2012年12月18日 - 9.1
      - FreeBSD 9.1-RC3ベース
  - 2013年9月6日 - 9.2
      - FreeBSD 9.2-RC3ベース
  - 2013年10月7日 - 9.2-RELEASE
      - FreeBSD 9.2-RELEASEベース
  - 2014年1月29日 - 10.0-RELEASE
      - FreeBSD 10.0-RELEASEベース
  - 2014年6月24日 - 10.0.2-RELEASE
  - 2014年11月14日 - 10.1-RELEASE
  - 2015年5月18日 - 10.1.2-RELEASE
  - 2015年8月21日 - 10.2-RELEASE
  - 2016年4月4日 - 10.3-RELEASE
  - 2016年9月1日 - 11.0 CURRENT

## 脚注

## 関連項目

  - [FreeBSD](../Page/FreeBSD.md "wikilink")
  - [DesktopBSD](../Page/DesktopBSD.md "wikilink")

## 外部リンク

  - [公式TrueOSウェブサイト](https://www.trueos.org/)
  - [TXZ Directory（TrueOS用ソフトウェア）](http://pkg.cdn.trueos.org/10.0-RELEASE/amd64/All/)
  - [ixsystems](http://www.ixsystems.com/)
  - [TrueOS](http://distrowatch.com/index.php?distribution=trueos) [DistroWatch](https://ja.wikipedia.org/wiki/DistroWatch "wikilink")
  - [PC-BSD 0.7.5レビュー](http://agnani.blogspot.com/2005/06/pc-bsd-075-review.html)

[Category:FreeBSD](https://ja.wikipedia.org/wiki/Category:FreeBSD "wikilink") [Category:オープンソースソフトウェア](https://ja.wikipedia.org/wiki/Category:オープンソースソフトウェア "wikilink") [Category:2005年のソフトウェア](https://ja.wikipedia.org/wiki/Category:2005年のソフトウェア "wikilink")

1.
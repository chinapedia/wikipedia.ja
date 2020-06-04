> この記事は[Xfce](https://ja.wikipedia.org/wiki/Xfce)から翻訳されています。


**Xfce**（エックス エフ シー イー）は、[X Window System上で動作する](../Page/X_Window_System.md "wikilink")[デスクトップ環境](https://ja.wikipedia.org/wiki/デスクトップ環境 "wikilink")の一つ。

豪華な見た目と簡単な使用感を保ちながら、軽量・高速なデスクトップ環境を目指している。ライセンスは各コンポーネントにより、[GPL](../Page/GNU_General_Public_License.md "wikilink")、[LGPL](https://ja.wikipedia.org/wiki/LGPL "wikilink")または[BSDライセンス](../Page/BSDライセンス.md "wikilink")である。

## 歴史

1997年、Olivier Fourdanをリーダーに、X Window Systemで利用できる軽量なデスクトップ環境の構築を目標として、プロジェクトが開始された。

もともとはXFormsツールキットベースで、*XForms Common Environment*の[頭文字](https://ja.wikipedia.org/wiki/頭文字 "wikilink")であった。改訂によりXFormsツールキットを使用しなくなったものの名前はそのままとした。以上のような経緯から(現在は)*XFce*ではなく*Xfce*のように "F" を小文字とする。

Xfceのルック＆フィールは、メインパネルやメニュー、アプレット、ランチャーなど、商用[UNIX](../Page/UNIX.md "wikilink")システムの多くが採用している [CDE](../Page/Common_Desktop_Environment.md "wikilink") (Common Desktop Environment) と多くの点でよく似ている（CDEライク（CDE like）である）。

### 初期のバージョン

[Xfce3.jpg](https://ja.wikipedia.org/wiki/File:Xfce3.jpg "fig:Xfce3.jpg") Xfceは、XFormを用いたシンプルなプロジェクトとして始まった。Olivier FourdanはSunSITEを用いたシンプルなタスクバーからなるプログラムを公開した\[1\]。

Fourdanは開発を続け、Xfceはオリジナルなウィンドウマネージャ、Xfwmを持つ最初のバージョンであるXfce 2をリリースした。Fourdanは、[Red Hat Linuxに含まれるようリクエストしたが](../Page/Red_Hat_Linux.md "wikilink")、XFormを基礎としているという理由でこれは却下された。Red Hatは[GNU GPLやBSD互換のライセンスでリリースされる](https://ja.wikipedia.org/wiki/GNU_GPL "wikilink")[オープンソース](../Page/オープンソース.md "wikilink")のソフトウェアのみを受け入れていたのだが、このとき、XFromsはクローズドソースで、個人利用目的のみでフリーであったからである\[2\]。同様の理由で、バージョン3まで[Debian](../Page/Debian.md "wikilink")は、Xfceを含まず、Xfce 2はDebianのcontribレポジトリのみで配布された\[3\]。

[1999年](../Page/1999年.md "wikilink")3月、Foudranは、完全にノンプロプライエタリなツールキット、[GTK](https://ja.wikipedia.org/wiki/GTK "wikilink")をもとに完全にプロジェクトを書き直すことを始めた。この結果がXfce 3.0で、GPLでライセンスされた。

### 近年のXfce

[right](https://ja.wikipedia.org/wiki/ファイル:Xfce-4.4.png "wikilink") [2003年](../Page/2003年.md "wikilink")[9月25日](../Page/9月25日.md "wikilink")にリリースされたXfce 4.0.0では、使われるツールキットが[GTK](https://ja.wikipedia.org/wiki/GTK "wikilink") 2にアップグレードされた\[4\]。4.2.0ではXfwmにコンポジティングマネージャが導入され、透過や影の描画、新しいデフォルトの[SVG](https://ja.wikipedia.org/wiki/SVG "wikilink")アイコンの導入などが行われた\[5\]。[2007年](../Page/2007年.md "wikilink")1月にはXfce 4.4.0がリリースされ、Xffmに変わって、新たにファイルマネージャとして[Thunar](../Page/Thunar.md "wikilink")が含まれた。Xfce 4.6.0は[2009年](../Page/2009年.md "wikilink")2月にリリースされ、新しい設定のバックエンド、新しい設定マネージャ、新しいサウンドミキサーが導入された。また、いくつかの重要な改善が設定マネージャと残りのXfceのcoreコンポーネントに対して行われた\[6\]。

[2011年](../Page/2011年.md "wikilink")1月には、Xfce 4.8.0がリリースされた。このバージョンはThunarVFSやHALをGIO、udev、ConsoleKitや[PolicyKit](https://ja.wikipedia.org/wiki/PolicyKit "wikilink")で置き換え、[SFTP](https://ja.wikipedia.org/wiki/SFTP "wikilink")、[SMB](https://ja.wikipedia.org/wiki/SMB "wikilink")、[FTP](https://ja.wikipedia.org/wiki/FTP "wikilink")などのプロトコルを用いてネットワーク共有をブラウジングすることができる新たなユーティリティが含まれた。

[right](https://ja.wikipedia.org/wiki/ファイル:XFCE-4.10-Desktop.png "wikilink") Xfce4.10は、[2012年](../Page/2012年.md "wikilink")[4月28日](../Page/4月28日.md "wikilink")にリリースされた。このリリースの焦点は、ユーザーエクスペリエンスを向上させることであった\[7\]。続いて、Xfce 4.12は[2015年](../Page/2015年.md "wikilink")2月28日にリリースされた\[8\]。4.12のターゲットは、4.10リリース以後に新しく導入された技術を用いて、ユーザーエクスペリエンスを向上させることである。また、Xfce 4.12は、[GTK](https://ja.wikipedia.org/wiki/GTK "wikilink")3へのアプリケーションとサポートするプラグイン、ブックマークのポートの移行を始めた。

Xfce 4.14は公式に[2019年](../Page/2019年.md "wikilink")[8月12日](../Page/8月12日.md "wikilink")にリリースされた\[9\]。このリリースのゴールは、dbus-glibへの依存をGDBusに置き換え、廃止されたいくつかのウィジェットを置き換えるなど、依然として残るcoreコンポーネントをGTK 2からGTK 3へポートすることであった。

## 現状

GUIツールキットとして[GTK+](https://ja.wikipedia.org/wiki/GTK+ "wikilink")2を採用。ドラッグアンドドロップやアンチエイリアス、テーマエンジンなどをサポートしている。また、バージョン4からは独自のアプリケーション開発フレームワークを提供している。Xfce 4 においては、[freedesktop.org](https://ja.wikipedia.org/wiki/freedesktop.org "wikilink") に準拠することが開発の標準となった。

[GNOME](../Page/GNOME.md "wikilink")や[KDE](../Page/KDE.md "wikilink")といった他のデスクトップ環境より軽快であるため、それらの動作速度に不満を持つユーザから人気がある。標準で採用されていることは多くないが、たとえば、[Ubuntu](../Page/Ubuntu.md "wikilink")の派生である[Xubuntu](https://ja.wikipedia.org/wiki/Xubuntu "wikilink")では、標準のデスクトップ環境として利用できる。軽量であるため、[Live CDでの採用は比較的多い](../Page/Live_CD.md "wikilink")。40以上の言語の翻訳版が利用可能である。

なお、Xfce デスクトップで利用するアプリケーションの機能強化を図る目的で、Xfce Goodies プロジェクトという開発コミュニティが存在している。ここで開発されたプラグインは Xfce の公式なプロジェクトには含まれないが、すでに多数のプラグインの提供を行っている。

## Xfceのコンポーネントとアプリケーション

[thumb](https://ja.wikipedia.org/wiki/ファイル:Whisker_Menu.png "wikilink") Xfceチームによって開発されているアプリケーションは[GTK](https://ja.wikipedia.org/wiki/GTK "wikilink")とチーム自らが開発するXfceライブラリをベースにしている。Xfce以外にも、Xfceライブラリを使うサードパーティ製のプログラムが存在している\[10\]。

### 開発のフレームワーク

Xfceは、次に示されるようなコンポーネントを含む開発のフレームワークを提供している。

  - exo : Xfceデスクトップ環境のためのアプリケーションライブラリ
  - garcon : [Freedesktop.org](../Page/Freedesktop.org.md "wikilink")に互換性のあるメニューライブラリ
  - libxfce4ui : Xfceデスクトップ環境のための[ウィジェット](https://ja.wikipedia.org/wiki/ウィジェット "wikilink")のライブラリ
  - libxfce4util : Xfceのための拡張ライブラリ

また、フレームワークによって、[root権限でアプリケーションが動作している際には](https://ja.wikipedia.org/wiki/スーパーユーザ "wikilink")、ウィンドウの上部を横切る形で、ユーザーがシステムファイルにダメージを与える可能性があることを示す警告が表示される。

### Xfce Panel

Xfce Panelは、高度にカスタマイズ可能な[タスクバー](../Page/タスクバー.md "wikilink")で、多くのプラグインを利用することができる\[11\]。

パネルやプラグインに関する様々な項目は、グラフィカルなダイアログで容易に設定することができるが、Xfconfの設定などからも設定可能である\[12\]。

### Xfce Terminal

[XFCE_Terminal--February_2007.png](https://ja.wikipedia.org/wiki/File:XFCE_Terminal--February_2007.png "fig:XFCE_Terminal--February_2007.png") Xfceプロジェクトによって提供されている[端末エミュレータ](../Page/端末エミュレータ.md "wikilink")であるが、他の[デスクトップ環境](https://ja.wikipedia.org/wiki/デスクトップ環境 "wikilink")でも使うことができる。このターミナルは、タブ、カスタマイズ可能なキーバインディング、色、ウィンドウサイズの設定などを備えている。本アプリは、[GNOME](../Page/GNOME.md "wikilink")のライブラリに依存している[GNOME端末](https://ja.wikipedia.org/wiki/GNOME端末 "wikilink")を置き換えるために設計された。ただし、本アプリもGNOME端末のように、VTEライブラリを用いている\[13\]。Xfce Terminalは、各タブでそれぞれ背景を変えることができ、[Guake](https://ja.wikipedia.org/wiki/Guake "wikilink")のようにドロップダウンターミナルとしても使うことができる\[14\]。

### Xfwm

Xfwmはカスタムテーマをサポートする[ウィンドウマネージャ](../Page/ウィンドウマネージャ.md "wikilink")であり\[15\]、バージョン4.2からはコンポジティングが可能となっている\[16\]。

### Catfish

in-name、in-textマッチング検索が可能なファイル検索ツールで、ファイルタイプや最終変更日時からもファイルを検索することができる。また、Catfishはmlocate[データベース](../Page/データベース.md "wikilink")を用いてインデックス化を行うこともできる\[17\]。

### Thunar

Thunarは、Xfceのデフォルトのファイルマージャで（過去はXffm）、GNOMEの[Nautilus](https://ja.wikipedia.org/wiki/Nautilus "wikilink")に似ている。Thunarは、メモリーのフットプリントが小さく、プラグインによって高度にカスタマイズ可能である\[18\]。Xfceはまた、軽量なアーカイブマネージャであるXarchiverを持つが、このアプリはXfce 4.40からXfce coreの一部ではない。

### Orage

バージョン4.4から、Xfcalendarは、Orage（[フランス語](https://ja.wikipedia.org/wiki/フランス語 "wikilink")でサンダーストームの意味）に名前が変更され、いくつかの機能が加えられた。Orageはアラーム機能を持ち、[iCalendar](https://ja.wikipedia.org/wiki/iCalendar "wikilink")フォーマットを使う。これにより、いくつかの他のカレンダーアプリケーションとの互換性を持つ。Orageはまた、パネル用の時計プラグインと、同時に異なったタイムゾーンの時刻を表示することができるインターナショナル時計アプリを含む。

### Mousepad

[thumb](https://ja.wikipedia.org/wiki/ファイル:Mousepad-0.4.0.png "wikilink") Mousepadは、[Xubuntu](https://ja.wikipedia.org/wiki/Xubuntu "wikilink")\[19\]を含むいくつかの[Linuxディストリビューション](../Page/Linuxディストリビューション.md "wikilink")でデフォルトの[テキストエディタ](../Page/テキストエディタ.md "wikilink")である。Mousepadは、簡単に使え、高速なテキストエディタを目指している。Mousepadは、もともと[Leafpad](../Page/Leafpad.md "wikilink")のフォークとして作られ、Erik HarrisonとNick Schermerによって開発されたが、以後、スクラッチから書き直されている。

### Parole

[Parole_Media_Player_0.8.1_on_XFCE_4.12.3_&_Debian_9.3.png](https://ja.wikipedia.org/wiki/File:Parole_Media_Player_0.8.1_on_XFCE_4.12.3_&_Debian_9.3.png "fig:Parole_Media_Player_0.8.1_on_XFCE_4.12.3_&_Debian_9.3.png") 9環境で動作するParole 0.8.1\]\] Parokeは[GStreamer](../Page/GStreamer.md "wikilink")フレームワークのフロントエンドである。Paroleは、Xfce Goodiesの一部としてAli Abdallahによって開発された\[20\]。当初はプレイリストに基くものであったが、現在はプレイリストをファイル再生時に置き換えるオプションを持っている\[21\] 。

### Xfburn

[CD](https://ja.wikipedia.org/wiki/CD "wikilink")/[DVD](../Page/DVD.md "wikilink")のバーニングプログラム。Xfce 4.12のリリースからは、[Blu-ray Discも書き込むことできるようになっている](../Page/Blu-ray_Disc.md "wikilink")。

### Xfce Screensaver

Xfce 4.14からXfceに含まれるようになった、[スクリーンセーバー](../Page/スクリーンセーバー.md "wikilink")と画面ロック用のプログラムである。Xscreensaverと互換性のあるテーマを使っている\[22\]。本アプリはMATE Screensaverからのフォークであるけれども、Xfceのライブラリのみに依存している。

## Xfce Goodies

Xfce-Goodies プロジェクト（外部リンク参照）から入手できる代表的なプラグインには、次のようなものがある。

### アプリケーション

  - ウェブブラウザ ([Midori](https://ja.wikipedia.org/wiki/Midori_\(ウェブブラウザ\) "wikilink"))
  - 画像ビューア ([Ristretto](https://ja.wikipedia.org/wiki/Ristretto "wikilink"))
  - CD/DVD作成ツール ([Xfburn](https://ja.wikipedia.org/wiki/Xfburn "wikilink"))
  - メディアプレーヤ ([Parole](https://ja.wikipedia.org/wiki/Parole "wikilink"))
  - 電源管理 (xfce4-power-manager)
  - スクリーンショット取得ツール (xfce4-Screenshooter)
  - タスクマネージャ (xfce4-taskmanager)
  - MPDクライアント (Xfmpc)

### パネルプラグイン

  - バッテリーモニター (xfce4-battery-plugin)
  - クリップボード管理 (xfce4-clipman-plugin)
  - ディスク稼働率モニター (xfce4-diskperf-plugin)
  - ファイルシステムモニター (xfce4-fsguard-plugin)
  - メールウォッチャー (xfce4-mailwatch-plugin)
  - ネットワーク負荷モニター (xfce4-netload-plugin)
  - 付箋紙 (xfce4-notes-plugin)
  - クイックランチャー (xfce4-quicklauncher-plugin)
  - ハードウェアセンサーモニター (xfce4-sensors-plugin)
  - スマートブックマーク (xfce4-smartbookmark-plugin)
  - システム負荷モニター (xfce4-systemload-plugin)
  - 天気予報通知 (xfce4-weather-plugin)
  - 無線LAN監視 (xfce4-wavelan-plugin)

これら以外にも、多数のプラグインが存在する。

## 脚注

## 関連項目

  - [Fluxbox](../Page/Fluxbox.md "wikilink")
  - [GNOME](../Page/GNOME.md "wikilink")
  - [KDE](../Page/KDE.md "wikilink")
  - [LXDE](https://ja.wikipedia.org/wiki/LXDE "wikilink")
  - [Unity](https://ja.wikipedia.org/wiki/Unity_\(ユーザインタフェース\) "wikilink")
  - [Xubuntu](https://ja.wikipedia.org/wiki/Xubuntu "wikilink") Xfceを標準搭載したディストリビューション

## 外部リンク

  -
  - [Xfce 公式ウィキ](http://wiki.xfce.org/ja/)

  - [Xfce-Look](http://www.xfce-look.org/) テーマとアートワーク集

  - [Xfce on Vimeo](http://vimeo.com/xfce)

  - [公式twitter](http://twitter.com/xfceofficial)

  - [Xubuntu](http://www.xubuntu.org/) Xfceを標準搭載したディストリビューション

  - [XFce 4 ドキュメント日本語版](http://www.dayomon.net/xfce/)

  - [Xfce Goodies プロジェクト](http://goodies.xfce.org/)

  - [XFce Wiki](http://wiki.fdiary.net/xfce/) 日本Xfceユーザーの[ウィキ](../Page/ウィキ.md "wikilink")

[Category:デスクトップ環境](https://ja.wikipedia.org/wiki/Category:デスクトップ環境 "wikilink") [Category:オープンソースソフトウェア](https://ja.wikipedia.org/wiki/Category:オープンソースソフトウェア "wikilink") [Category:X_Window_System](https://ja.wikipedia.org/wiki/Category:X_Window_System "wikilink") [Category:GTK+を使用するソフトウェア](https://ja.wikipedia.org/wiki/Category:GTK+を使用するソフトウェア "wikilink") [Category:1996年のソフトウェア](https://ja.wikipedia.org/wiki/Category:1996年のソフトウェア "wikilink")

1.
2.
3.  Debian xfce source package 3.4.0.20000513-1 changelog
4.
5.
6.
7.
8.
9.
10. <https://goodies.xfce.org/projects/applications/>
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
21. [parole - GStreamer based media player](http://git.xfce.org/apps/parole/commit/?id=61df0aef193f67047bf130e4adb13bff32eab4d9)
22.
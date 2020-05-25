> この記事は[Linux Mint](https://ja.wikipedia.org/wiki/Linux_Mint)から翻訳されています。


**Linux Mint**（リナックス・ミント）は[Linuxディストリビューション](../Page/Linuxディストリビューション.md "wikilink")の一つである。洗練され、最新で快適な[Linux](../Page/Linux.md "wikilink")デスクトップを提供することを目標としている。[Ubuntu](../Page/Ubuntu.md "wikilink")や[Debian](../Page/Debian.md "wikilink")をベースにしており、それぞれの[リポジトリ](../Page/リポジトリ.md "wikilink")を共有している。

## 概要

Linux Mintは[2006年](../Page/2006年.md "wikilink")に[フランス](https://ja.wikipedia.org/wiki/フランス "wikilink")出身で[アイルランド](../Page/アイルランド.md "wikilink")在住のクレマン・ルフェーブルにより設立された。Linux Mintは、シンプルであることよりも、多くのソフトウェアと最新の技術を使用することにより、誰にでも使いやすいLinuxシステムを提供することに焦点を当てている\[1\]。

デスクトップ環境は[GNOME 3から派生した](https://ja.wikipedia.org/wiki/GNOME_3 "wikilink")[Cinnamon](https://ja.wikipedia.org/wiki/Cinnamon "wikilink")、[GNOME 2から派生した](../Page/GNOME_2.md "wikilink")[MATE](https://ja.wikipedia.org/wiki/MATE_\(デスクトップ環境\) "wikilink")、他に[Xfce](../Page/Xfce.md "wikilink")を採用する。どちらもWindowsに良く似たデザインを持っているがCinnamonの動作にはGNOME 3の要件に従い3Dアクセラレータが必須となる。

2010年7月2日に製作側は公式ブログにてUbuntuの代わりに[Debian](../Page/Debian.md "wikilink")をベースとしたLinux Mintをテストしていることを明らかにした\[2\]。ベースをUbuntuからDebianへすることの主なメリットとして、製作側はコンピュータリソースの使用量を抑えられ、Ubuntuベースよりも快適に動くことを挙げている。これをLMDE (Linux Mint Debian Edtionの略) と称していくつかの評価版をリリースした後、2015年4月にLMDE2 "Betsy"を安定版としてリリースした\[3\]\[4\]。

## システム要求

  - 1GB RAM（快適な使用のために2GBを推奨）
  - 15GBのディスク容量（20GB推奨）
  - 1024×768の解像度

## 配布形態

Linux Mintには同梱されるコンポーネントや標準デスクトップ環境によるいくつかのエディションがある。各エディションは起動時にインストール不要な[Live DVDとして動作する](../Page/Live_CD.md "wikilink")。

かつて、No codecsと示されている[DVD](../Page/DVD.md "wikilink")イメージ以外は、[Adobe Flashや](../Page/Adobe_Flash.md "wikilink")[Windows Mediaなどの](https://ja.wikipedia.org/wiki/Windows_Media "wikilink")[プロプライエタリな](../Page/プロプライエタリ・ソフトウェア.md "wikilink")[コーデック](../Page/コーデック.md "wikilink")やDVD-Videoの[CSSを復号化する](../Page/Content_Scramble_System.md "wikilink")[libdvdcss](https://ja.wikipedia.org/wiki/libdvdcss "wikilink")などの[DRM関連のソフトウェアが収録されていた](../Page/デジタル著作権管理.md "wikilink")。No codecs表記のないバージョン17系以前のインストールイメージの日本を含むいくつかの国での配布は、[知的財産権](../Page/知的財産権.md "wikilink")に関連する複数の法律に抵触するおそれがあるので注意が必要である。かつては国内の複数のミラーサーバがLinux Mintを提供していたが、これを理由に2012年3月1日に[JAIST](https://ja.wikipedia.org/wiki/JAIST "wikilink")のサーバが一旦提供を中止したのを皮切りに、すべてのミラーサーバがLinux Mintの提供を中止していた。しかし2013年5月から、JAISTはlibdvdcssなどを含んでいないNo codecs版のイメージに限って提供を再開した\[5\]。この時からLinux MintおよびLMDEのパッケージのミラーも日本国内で唯一再開している。2016年5月にリリースされたLinux Mint 18より、コーデックを含まないISOのみが配布されることとなり、これに伴ってOEM版およびno-codecs版は廃止された\[6\]。なお、コーデックはメニュー等から選択することでインストールが可能となっている。

## mintTools

Linux Mintはユーザの利便性を向上させるために、mintソフトウェア群mintToolsを含んでいる。これらは[Python](../Page/Python.md "wikilink")および[シェルスクリプト](../Page/シェルスクリプト.md "wikilink")で開発されている。

  - mintUpdate
    Linux Mint専用のアップデートソフトウェア。mintUpdateはアップデートに安全性と必要性に応じてセーフティレベル（1から5）を割り当てる。アップデートはレベルごとに、通知する/しない・適用対象とする/しないの設定ができ、レベル4と5にカテゴライズされている開発版（動作に問題がある、あるいはテストが十分に行われていない）パッケージは、非常に経験豊かなユーザだけが必要とするので、デフォルトでは隠される。これにより、初心者ユーザが自身のハードウェアでは適切ではない更新を行ってシステムが破壊されるといった事態を防ぐ。
  - mintInstall
    Linux Mint用ソフトウェアマネージャ。mintファイルを配布するインターネット上のカタログからソフトウェア情報を取得しダウンロードおよびインストールする。[Linux Mint Software Portal](http://community.linuxmint.com/software)のフロントエンドとして動作し、ソフトウェアのスクリーンショット、ユーザレビューや人気度、インストール済みの場合のバージョンおよびインストール可能バージョンの確認が行える。[APT](../Page/APT.md "wikilink")のGUIフロントエンドでもあるため、Ubuntuリポジトリや[GetDeb](http://www.getdeb.net/)の検索機能も具備する。mintファイルはソフトウェアを含まないが、すべての情報とダウンロード[URI](https://ja.wikipedia.org/wiki/URI "wikilink")を含む。
  - mintUpload
    ファイルマネージャ上でのファイルの右クリックメニューで、「Upload」を選択することによりファイルをサーバーにアップロードする[FTPクライアント](../Page/File_Transfer_Protocol.md "wikilink")。アップロードするとそのファイルへのURLが与えられ、迅速かつ容易に他人とファイルを共有することができる。ファイルサーバは、一般のFTPサーバの他、無償でスペースが提供され保存期間が制限されるデフォルトサービス（ファイルサイズ最大10MB、保存期間2日間）およびLinux Mintが提供するレンタルサーバーサービス（有償）の[Mint-Space](http://linuxmint.com/store.php)に対応する。
  - mintNanny
    簡易[ペアレンタルコントロール](https://ja.wikipedia.org/wiki/ペアレンタルコントロール "wikilink")ソフトウェア。設定された[ドメイン名](../Page/ドメイン名.md "wikilink")のサイトへのアクセスを禁止する。
  - mint4win
    [Wubi](../Page/Wubi.md "wikilink")のLinux Mint版。
  - mintMenu
    MATEデスクトップに提供されるメインメニュー。テキスト、アイコン、色を完全にカスタマイズ可能である。[GNOME](../Page/GNOME.md "wikilink")メインメニューと同じホットリンクを共有する。
  - mintWifi
    いくつかの無線LANドライバを含む無線LAN設定ツール。
  - mintBackup
    バックアップツール。指定したフォルダやインストール済みソフトウェアの一覧情報を容易にバックアップおよびリストア可能。バックアップ対象から除外するディレクトリおよびファイルの指定、バックアップ対象とする隠しディレクトリおよびファイルの指定が行える。mintBackupがインストールされているシステムであれば、バックアップファイルをダブルクリックするだけでリストアできる。
  - mintSources
    Ubuntuの「ソフトウェアソース」を置換する。PPAの管理も行える他、全てのミラーサーバーに対してチェックを行いどこが最も速いかをグラフで表示する機能も独自に持つ。Linux Mint 15 "Olivia" から搭載。
  - mintDrivers
    Ubuntuのドライバ管理のフロントエンドを代替する。Ubuntuのものと違い、バージョンを明記するほか有名なメーカーの物にはロゴが表示される。Linux Mint 15 "Olivia" から搭載。
  - mintDesktop
    デスクトップ設定を簡単に行うためのツール。KDEとCinnamonを除くエディションで提供される。
  - mintStick
    LinuxのライブCD形式のISOイメージをUSBメモリにブート可能な形で展開するツール。Linux Mint以外のディストリビューションも扱える。Linux Mint 16 "Petra" 以降ではUSBメモリのフォーマットツールも含む。

<File:Linux> Mint mintUpdate-ja.png|アップデートマネージャ「mintUpdate」 <File:Linux> Mint MintInstall-ja.png|ソフトウェアマネージャ「mintInstall」 <File:Linux> Mint mintUpload-ja.png|ファイルをサーバに簡単にアップロードできる「mintUpload」 <File:Linux> Mint MintNanny-ja.png|簡易ペアレンタルコントロール「mintNanny」 <File:Linux> Mint MintMenu-ja.png|GNOMEデスクトップで提供される「mintMenu」 <File:Linux> Mint MintBackup-ja.png|ホームフォルダを簡単にバックアップできる「mintBackup」 [File:MintDesktop-ja.png|デスクトップのカスタマイズを行う「mintDesktop](File:MintDesktop-ja.png%7Cデスクトップのカスタマイズを行う「mintDesktop)」(GNOME)

## リリース

Linux Mintは、一定のリリースサイクルに従わない。リリースは、順々に計画される。まず、プロジェクトは次のリリースのために目標を定める。通常、すべての目標が達成された時にRC版がリリースされ、問題がなければその後安定版がリリースされる。従来のUbuntuベースを離れ、更なる軽量化を目的としたLinux Mint Debian Edition（以下LMDE）の試験的なリリースもされている\[7\]。

### Linux Mint

<table>
<thead>
<tr class="header">
<th><p>バージョン</p></th>
<th><p>コードネーム</p></th>
<th><p>エディション</p></th>
<th><p>デスクトップ環境</p></th>
<th><p>パッケージベース</p></th>
<th><p>リリース日</p></th>
<th><p>サポート期限</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><p><strong>Ada</strong></p></td>
<td><p>Main</p></td>
<td><p><a href="../Page/KDE.md" title="wikilink">KDE</a></p></td>
<td><p><a href="../Page/Kubuntu.md" title="wikilink">Kubuntu</a> Dapper</p></td>
<td><p>2006/08/27</p></td>
<td><p>N/A</p></td>
</tr>
<tr class="even">
<td></td>
<td><p><strong>Barbara</strong></p></td>
<td><p>Main</p></td>
<td><p><a href="../Page/GNOME.md" title="wikilink">GNOME</a></p></td>
<td><p>Ubuntu 6.10</p></td>
<td><p>2006/11/13</p></td>
<td><p>2008/04</p></td>
</tr>
<tr class="odd">
<td></td>
<td><p><strong>Bea</strong></p></td>
<td><p>Main</p></td>
<td><p>GNOME</p></td>
<td><p>2006/12/20</p></td>
<td><p>2008/04</p></td>
<td></td>
</tr>
<tr class="even">
<td><p>rowspan=3 </p></td>
<td><p><strong>Bianca</strong></p></td>
<td><p>Main</p></td>
<td><p>GNOME</p></td>
<td><p>2007/02/20</p></td>
<td><p>2008/04</p></td>
<td></td>
</tr>
<tr class="odd">
<td><p>Light</p></td>
<td><p>GNOME</p></td>
<td><p>2007/03/29</p></td>
<td><p>2008/04</p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>KDE CE</p></td>
<td><p>KDE</p></td>
<td><p>2007/04/20</p></td>
<td><p>2008/04</p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>rowspan=5 </p></td>
<td><p><strong>Cassandra</strong></p></td>
<td><p>Main</p></td>
<td><p>GNOME</p></td>
<td><p>Ubuntu 7.04</p></td>
<td><p>2007/05/30</p></td>
<td><p>2008/10</p></td>
</tr>
<tr class="even">
<td><p>Light</p></td>
<td><p>GNOME</p></td>
<td><p>2007/06/15</p></td>
<td><p>2008/10</p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>KDE CE</p></td>
<td><p>KDE</p></td>
<td><p>2007/08/14</p></td>
<td><p>2008/10</p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>MiniKDE</p></td>
<td><p>KDE</p></td>
<td><p>2007/08/14</p></td>
<td><p>2008/10</p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>XFCE CE</p></td>
<td><p><a href="../Page/Xfce.md" title="wikilink">Xfce</a></p></td>
<td><p>2007/08/07</p></td>
<td><p>2008/10</p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>rowspan=2 </p></td>
<td><p><strong>Celena</strong></p></td>
<td><p>Main</p></td>
<td><p>GNOME</p></td>
<td><p>2007/09/24</p></td>
<td><p>2008/10</p></td>
<td></td>
</tr>
<tr class="odd">
<td><p>Light</p></td>
<td><p>GNOME</p></td>
<td><p>2007/10/01</p></td>
<td><p>2008/10</p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>rowspan=6 </p></td>
<td><p><strong>Daryna</strong></p></td>
<td><p>Main</p></td>
<td><p>GNOME</p></td>
<td><p>Ubuntu 7.10</p></td>
<td><p>2007/10/15</p></td>
<td><p>2009/04</p></td>
</tr>
<tr class="odd">
<td><p>Light</p></td>
<td><p>GNOME</p></td>
<td><p>2007/10/15</p></td>
<td><p>2009/04</p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>KDE CE</p></td>
<td><p>KDE</p></td>
<td><p>2008/03/03</p></td>
<td><p>2009/04</p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>miniKDE</p></td>
<td><p>KDE</p></td>
<td><p>2008/03/03</p></td>
<td><p>2009/04</p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p><strong>Dalyna </strong></p></td>
<td><p>XFCE CE</p></td>
<td><p>Xfce</p></td>
<td><p>2007/11/02</p></td>
<td><p>N/A</p></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p><strong>Dalyna </strong></p></td>
<td><p>Fluxbox CE</p></td>
<td><p><a href="../Page/Fluxbox.md" title="wikilink">Fluxbox</a></p></td>
<td><p>2008/01/03</p></td>
<td><p>N/A</p></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>rowspan=6 </p></td>
<td><p><strong>Elyssa</strong></p></td>
<td><p>Main</p></td>
<td><p>GNOME</p></td>
<td><p>Ubuntu 8.04 LTS</p></td>
<td><p>2008/06/08</p></td>
<td><p>2011/04</p></td>
</tr>
<tr class="odd">
<td><p>Light</p></td>
<td><p>GNOME</p></td>
<td><p>2008/06/08</p></td>
<td><p>2011/04</p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>x64</p></td>
<td><p>GNOME</p></td>
<td><p>2008/10/18</p></td>
<td><p>2011/04</p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>XFCE CE</p></td>
<td><p>Xfce</p></td>
<td><p>2008/09/08</p></td>
<td><p>2011/04</p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>KDE CE</p></td>
<td><p>KDE</p></td>
<td><p>2008/09/15</p></td>
<td><p>2011/04</p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>Fluxbox CE</p></td>
<td><p>Fluxbox</p></td>
<td><p>2008/10/21</p></td>
<td><p>2011/04</p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>rowspan=6 </p></td>
<td><p><strong>Felicia</strong></p></td>
<td><p>Main</p></td>
<td><p>GNOME</p></td>
<td><p>Ubuntu 8.10</p></td>
<td><p>2008/12/15</p></td>
<td><p>2010/04</p></td>
</tr>
<tr class="odd">
<td><p>Universal</p></td>
<td><p>GNOME</p></td>
<td><p>2008/12/15</p></td>
<td><p>2010/04</p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>x64</p></td>
<td><p>GNOME</p></td>
<td><p>2009/02/06</p></td>
<td><p>2010/04</p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>XFCE CE</p></td>
<td><p>Xfce</p></td>
<td><p>2009/02/24</p></td>
<td><p>2010/04</p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>KDE CE</p></td>
<td><p>KDE</p></td>
<td><p>2009/04/08</p></td>
<td><p>2010/04</p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>Fluxbox CE</p></td>
<td><p>Fluxbox</p></td>
<td><p>2009/04/07</p></td>
<td><p>2010/04</p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>rowspan=6 </p></td>
<td><p><strong>Gloria</strong></p></td>
<td><p>Main</p></td>
<td><p>GNOME</p></td>
<td><p>Ubuntu 9.04</p></td>
<td><p>2009/05/26</p></td>
<td><p>2010/10</p></td>
</tr>
<tr class="odd">
<td><p>Universal</p></td>
<td><p>GNOME</p></td>
<td><p>2009/05/26</p></td>
<td><p>2010/10</p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>x64</p></td>
<td><p>GNOME</p></td>
<td><p>2009/06/24</p></td>
<td><p>2010/10</p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>KDE CE</p></td>
<td><p>KDE</p></td>
<td><p>2009/08/03</p></td>
<td><p>2010/10</p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>XFCE CE</p></td>
<td><p>Xfce</p></td>
<td><p>2009/09/13</p></td>
<td><p>2010/10</p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>Fluxbox CE</p></td>
<td><p>Fluxbox</p></td>
<td><p>未定</p></td>
<td><p>N/A</p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>rowspan=8 </p></td>
<td><p><strong>Helena</strong></p></td>
<td><p>Main</p></td>
<td><p>GNOME</p></td>
<td><p>Ubuntu 9.10</p></td>
<td><p>2009/11/28</p></td>
<td><p>2011/04</p></td>
</tr>
<tr class="odd">
<td><p>Universal</p></td>
<td><p>GNOME</p></td>
<td><p>2009/11/28</p></td>
<td><p>2011/04</p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>x64</p></td>
<td><p>GNOME</p></td>
<td><p>2009/12/14</p></td>
<td><p>2011/04</p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>KDE</p></td>
<td><p>KDE</p></td>
<td><p>2010/02/06</p></td>
<td><p>2011/04</p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>KDE x64</p></td>
<td><p>KDE</p></td>
<td><p>2010/02/12</p></td>
<td><p>2011/04</p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>Fluxbox</p></td>
<td><p>Fluxbox</p></td>
<td><p>2010/02/12</p></td>
<td><p>2011/04</p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>Xfce RC1</p></td>
<td><p>Xfce</p></td>
<td><p>2010/03/07</p></td>
<td><p>2011/04</p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>LXDE RC1</p></td>
<td><p>LXDE</p></td>
<td><p>2010/03/15</p></td>
<td><p>2011/04</p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>rowspan=7 </p></td>
<td><p><strong>Isadora</strong></p></td>
<td><p>GNOME CD/DVD</p></td>
<td><p>GNOME</p></td>
<td><p>Ubuntu 10.04 LTS</p></td>
<td><p>2010/05/17</p></td>
<td><p>2013/04</p></td>
</tr>
<tr class="odd">
<td><p>USA-Japan</p></td>
<td><p>GNOME</p></td>
<td><p>2010/05/18</p></td>
<td><p>2013/04</p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>OEM</p></td>
<td><p>GNOME</p></td>
<td><p>2010/05/18</p></td>
<td><p>2013/04</p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>Fluxbox CD</p></td>
<td><p>Fluxbox</p></td>
<td><p>2010/09/06</p></td>
<td><p>2013/04</p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>KDE DVD</p></td>
<td><p>KDE</p></td>
<td><p>2010/07/27</p></td>
<td><p>2013/04</p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>LXDE CD</p></td>
<td><p>LXDE</p></td>
<td><p>2010/07/18</p></td>
<td><p>2013/04</p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>Xfce</p></td>
<td><p>Xfce</p></td>
<td><p>2010/08/24</p></td>
<td><p>2013/04</p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>rowspan=5 </p></td>
<td><p><strong>Julia</strong></p></td>
<td><p>CD/DVD</p></td>
<td><p>GNOME</p></td>
<td><p>Ubuntu 10.10</p></td>
<td><p>2010/11/12</p></td>
<td><p>2012/04</p></td>
</tr>
<tr class="even">
<td><p>USA-Japan</p></td>
<td><p>GNOME</p></td>
<td><p>2010/11/12</p></td>
<td><p>2012/04</p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>OEM</p></td>
<td><p>GNOME</p></td>
<td><p>2010/11/12</p></td>
<td><p>2012/04</p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>KDE</p></td>
<td><p>KDE</p></td>
<td><p>2011/02/23</p></td>
<td><p>2012/04</p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>LXDE</p></td>
<td><p>LXDE</p></td>
<td><p>2011/03/16</p></td>
<td><p>2012/04</p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>rowspan=3 </p></td>
<td><p><strong>Katya</strong></p></td>
<td><p>CD/DVD</p></td>
<td><p>GNOME</p></td>
<td><p>Ubuntu 11.04</p></td>
<td><p>2011/05/26</p></td>
<td><p>2012/10</p></td>
</tr>
<tr class="odd">
<td><p>OEM</p></td>
<td><p>GNOME</p></td>
<td><p>2011/05/26</p></td>
<td><p>2012/10</p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>LXDE</p></td>
<td><p>LXDE</p></td>
<td><p>2011/08/16</p></td>
<td><p>2012/10</p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>rowspan=4 </p></td>
<td><p><strong>Lisa</strong></p></td>
<td><p>CD no codecs</p></td>
<td><p>GNOME</p></td>
<td><p>Ubuntu 11.10</p></td>
<td><p>2011/11/26</p></td>
<td><p>2013/04</p></td>
</tr>
<tr class="even">
<td><p>DVD</p></td>
<td><p>GNOME + MATE</p></td>
<td><p>2011/11/26</p></td>
<td><p>2013/04</p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>KDE</p></td>
<td><p>KDE</p></td>
<td><p>2012/02/03</p></td>
<td><p>2013/04</p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>LXDE</p></td>
<td><p>LXDE</p></td>
<td><p>2012/03/09</p></td>
<td><p>2013/04</p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>rowspan=6 </p></td>
<td><p><strong>Maya</strong></p></td>
<td><p>Cinnamon</p></td>
<td><p>Cinnamon</p></td>
<td><p>Ubuntu 12.04 LTS</p></td>
<td><p>2012/5/16</p></td>
<td><p>2017/04</p></td>
</tr>
<tr class="even">
<td><p>Cinnamon No codecs</p></td>
<td><p>Cinnamon</p></td>
<td><p>2012/5/16</p></td>
<td><p>2017/04</p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>MATE</p></td>
<td><p>MATE</p></td>
<td><p>2012/5/16</p></td>
<td><p>2017/04</p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>MATE No codecs</p></td>
<td><p>MATE</p></td>
<td><p>2012/5/16</p></td>
<td><p>2017/04</p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>KDE</p></td>
<td><p>KDE</p></td>
<td><p>2012/7/24</p></td>
<td><p>2017/04</p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>Xfce</p></td>
<td><p>Xfce</p></td>
<td><p>2012/7/24</p></td>
<td><p>2017/04</p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>rowspan=6 </p></td>
<td><p><strong>Nadia</strong></p></td>
<td><p>Cinnamon</p></td>
<td><p>Cinnamon</p></td>
<td><p>Ubuntu 12.10</p></td>
<td><p>2012/11/20</p></td>
<td><p>2014/04</p></td>
</tr>
<tr class="even">
<td><p>Cinnamon No codecs</p></td>
<td><p>Cinnamon</p></td>
<td><p>2012/11/20</p></td>
<td><p>2014/04</p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>MATE</p></td>
<td><p>MATE</p></td>
<td><p>2012/11/20</p></td>
<td><p>2014/04</p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>MATE No codecs</p></td>
<td><p>MATE</p></td>
<td><p>2012/11/20</p></td>
<td><p>2014/04</p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>KDE</p></td>
<td><p>KDE</p></td>
<td><p>2012/12/23</p></td>
<td><p>2014/04</p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>Xfce</p></td>
<td><p>Xfce</p></td>
<td><p>2012/12/21</p></td>
<td><p>2014/04</p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>rowspan=6 </p></td>
<td><p><strong>Olivia</strong></p></td>
<td><p>Cinnamon</p></td>
<td><p>Cinnamon</p></td>
<td><p>Ubuntu 13.04</p></td>
<td><p>2013/05/29</p></td>
<td><p>2014/01</p></td>
</tr>
<tr class="even">
<td><p>Cinnamon No codecs</p></td>
<td><p>Cinnamon</p></td>
<td><p>2013/05/29</p></td>
<td><p>2014/01</p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>MATE</p></td>
<td><p>MATE</p></td>
<td><p>2013/05/29</p></td>
<td><p>2014/01</p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>MATE No codecs</p></td>
<td><p>MATE</p></td>
<td><p>2013/05/29</p></td>
<td><p>2014/01</p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>KDE</p></td>
<td><p>KDE</p></td>
<td><p>2013/07/21</p></td>
<td><p>2014/01</p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>Xfce</p></td>
<td><p>Xfce</p></td>
<td><p>2013/07/12</p></td>
<td><p>2014/01</p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>rowspan=6 </p></td>
<td><p><strong>Petra</strong></p></td>
<td><p>Cinnamon</p></td>
<td><p>Cinnamon</p></td>
<td><p>Ubuntu 13.10</p></td>
<td><p>2013/11/30</p></td>
<td><p>2014/07</p></td>
</tr>
<tr class="even">
<td><p>Cinnamon No codecs</p></td>
<td><p>Cinnamon</p></td>
<td><p>2013/11/30</p></td>
<td><p>2014/07</p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>MATE</p></td>
<td><p>MATE</p></td>
<td><p>2013/11/30</p></td>
<td><p>2014/07</p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>MATE No codecs</p></td>
<td><p>MATE</p></td>
<td><p>2013/11/30</p></td>
<td><p>2014/07</p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>KDE</p></td>
<td><p>KDE</p></td>
<td><p>2013/12/22</p></td>
<td><p>2014/07</p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>Xfce</p></td>
<td><p>Xfce</p></td>
<td><p>2013/12/22</p></td>
<td><p>2014/07</p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>rowspan=6 </p></td>
<td><p><strong>Qiana</strong></p></td>
<td><p>Cinnamon</p></td>
<td><p>Cinnamon</p></td>
<td><p>Ubuntu 14.04 LTS</p></td>
<td><p>2014/05/31</p></td>
<td><p>2019/04</p></td>
</tr>
<tr class="even">
<td><p>Cinnamon No Codec</p></td>
<td><p>Cinnamon</p></td>
<td><p>2014/05/31</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>MATE</p></td>
<td><p>MATE</p></td>
<td><p>2014/05/31</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>MATE No Codec</p></td>
<td><p>MATE</p></td>
<td><p>2014/05/31</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>KDE</p></td>
<td><p>KDE</p></td>
<td><p>2014/06/23</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>Xfce</p></td>
<td><p>Xfce</p></td>
<td><p>2014/06/26</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>rowspan=6 </p></td>
<td><p><strong>Rebecca</strong></p></td>
<td><p>Cinnamon</p></td>
<td><p>Cinnamon</p></td>
<td><p>2014/11/29</p></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>Cinnamon No Codecs</p></td>
<td><p>Cinnamon</p></td>
<td><p>2014/11/29</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>MATE</p></td>
<td><p>MATE</p></td>
<td><p>2014/11/29</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>MATE No Codecs</p></td>
<td><p>MATE</p></td>
<td><p>2014/11/29</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>KDE</p></td>
<td><p>KDE</p></td>
<td><p>2015/01/08</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>Xfce</p></td>
<td><p>Xfce</p></td>
<td><p>2015/01/11</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>rowspan=6 </p></td>
<td><p><strong>Rafaela</strong></p></td>
<td><p>Cinnamon</p></td>
<td><p>Cinnamon</p></td>
<td><p>2015/06/30</p></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>Cinnamon No Codecs</p></td>
<td><p>Cinnamon</p></td>
<td><p>2015/07/23</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>MATE</p></td>
<td><p>MATE</p></td>
<td><p>2015/06/30</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>MATE No Codecs</p></td>
<td><p>MATE</p></td>
<td><p>2015/07/23</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>KDE</p></td>
<td><p>KDE</p></td>
<td><p>2015/08/07</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>Xfce</p></td>
<td><p>Xfce</p></td>
<td><p>2015/08/07</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>rowspan=6 </p></td>
<td><p><strong>Rosa</strong>[8]</p></td>
<td><p>Cinnamon</p></td>
<td><p>Cinnamon</p></td>
<td><p>2015/12/04</p></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>Cinnamon No Codecs</p></td>
<td><p>Cinnamon</p></td>
<td><p>2015/12/13</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>MATE</p></td>
<td><p>MATE</p></td>
<td><p>2015/12/04</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>MATE No Codecs</p></td>
<td><p>MATE</p></td>
<td><p>2015/12/13</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>KDE</p></td>
<td><p>KDE</p></td>
<td><p>2016/01/09</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>Xfce</p></td>
<td><p>Xfce</p></td>
<td><p>2016/01/09</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>rowspan="4" </p></td>
<td><p><strong>Sarah</strong>[9]</p></td>
<td><p>Cinnamon</p></td>
<td><p>Cinnamon</p></td>
<td><p>Ubuntu 16.04 LTS</p></td>
<td><p>2016/06/30</p></td>
<td><p>2021/04</p></td>
</tr>
<tr class="even">
<td><p>MATE</p></td>
<td><p>MATE</p></td>
<td><p>2016/06/30</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>KDE</p></td>
<td><p>KDE</p></td>
<td><p>2016/09/09</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>Xfce</p></td>
<td><p>Xfce</p></td>
<td><p>2016/08/02</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>rowspan="4" </p></td>
<td><p><strong>Serena</strong>[10]</p></td>
<td><p>Cinnamon</p></td>
<td><p>Cinnamon</p></td>
<td><p>2016/12/16</p></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>MATE</p></td>
<td><p>MATE</p></td>
<td><p>2016/12/16</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>KDE</p></td>
<td><p>KDE</p></td>
<td><p>2017/01/27</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>Xfce</p></td>
<td><p>Xfce</p></td>
<td><p>2017/01/27</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>rowspan="4" </p></td>
<td><p><strong>Sonya</strong>[11]</p></td>
<td><p>Cinnamon</p></td>
<td><p>Cinnamon</p></td>
<td><p>2017/07/02</p></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>MATE</p></td>
<td><p>MATE</p></td>
<td><p>2017/07/02</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>KDE</p></td>
<td><p>KDE</p></td>
<td><p>2017/07/02</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>Xfce</p></td>
<td><p>Xfce</p></td>
<td><p>2017/07/02</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>rowspan="4" </p></td>
<td><p><strong>Sylvia</strong>[12]</p></td>
<td><p>Cinnamon</p></td>
<td><p>Cinnamon</p></td>
<td><p>2017/11/27</p></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>MATE</p></td>
<td><p>MATE</p></td>
<td><p>2017/11/27</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>KDE</p></td>
<td><p>KDE</p></td>
<td><p>2017/12/15</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>Xfce</p></td>
<td><p>Xfce</p></td>
<td><p>2017/12/15</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>rowspan="3" </p></td>
<td><p><strong>Tara</strong>[13]</p></td>
<td><p>Cinnamon</p></td>
<td><p>Cinnamon</p></td>
<td><p>Ubuntu 18.04 LTS</p></td>
<td><p>2018/06/29</p></td>
<td><p>2023/04</p></td>
</tr>
<tr class="even">
<td><p>MATE</p></td>
<td><p>MATE</p></td>
<td><p>2018/06/29</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>Xfce</p></td>
<td><p>Xfce</p></td>
<td><p>2018/06/29</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>rowspan="3" </p></td>
<td><p><strong>Tessa</strong>[14]</p></td>
<td><p>Cinnamon</p></td>
<td><p>Cinnamon</p></td>
<td><p>2018/12/19</p></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>MATE</p></td>
<td><p>MATE</p></td>
<td><p>2018/12/19</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>Xfce</p></td>
<td><p>Xfce</p></td>
<td><p>2018/12/19</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>rowspan="3" </p></td>
<td><p><strong>Tina</strong>[15]</p></td>
<td><p>Cinnamon</p></td>
<td><p>Cinnamon</p></td>
<td><p>2019/08/04</p></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>MATE</p></td>
<td><p>MATE</p></td>
<td><p>2019/08/04</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>Xfce</p></td>
<td><p>Xfce</p></td>
<td><p>2019/08/04</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>rowspan="3" </p></td>
<td><p><strong>Tricia</strong>[16]</p></td>
<td><p>Cinnamon</p></td>
<td><p>Cinnamon</p></td>
<td><p>2019/12/18</p></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>MATE</p></td>
<td><p>MATE</p></td>
<td><p>2019/12/18</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>Xfce</p></td>
<td><p>Xfce</p></td>
<td><p>2019/12/18</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>バージョン</p></td>
<td><p>コードネーム</p></td>
<td><p>エディション</p></td>
<td><p>デスクトップ環境</p></td>
<td><p>パッケージベース</p></td>
<td><p>リリース日</p></td>
<td><p>サポート期限</p></td>
</tr>
<tr class="even">
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
</tbody>
</table>

### Linux Mint Debian Edition

<table>
<thead>
<tr class="header">
<th><p>バージョン</p></th>
<th><p>コードネーム</p></th>
<th><p>エディション</p></th>
<th><p>デスクトップ環境</p></th>
<th><p>パッケージベース</p></th>
<th><p>リリース日</p></th>
<th><p>サポート期限</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><p><strong>Debian </strong></p></td>
<td><p><a href="../Page/Debian.md" title="wikilink">Debian</a></p></td>
<td><p>GNOME</p></td>
<td><p>Debian Etch</p></td>
<td><p>2008/01/03</p></td>
<td><p>2016/01/01</p></td>
</tr>
<tr class="even">
<td></td>
<td><p>N/A</p></td>
<td><p>LMDE</p></td>
<td><p>GNOME</p></td>
<td><p>Debian</p></td>
<td><p>2010/09/07</p></td>
<td><p>2016/01/01</p></td>
</tr>
<tr class="odd">
<td></td>
<td><p>N/A</p></td>
<td><p>LMDE</p></td>
<td><p>GNOME</p></td>
<td><p>Debian</p></td>
<td><p>2010/12/24</p></td>
<td><p>2016/01/01</p></td>
</tr>
<tr class="even">
<td></td>
<td><p>N/A</p></td>
<td><p>LMDE</p></td>
<td><p>GNOME</p></td>
<td><p>Debian</p></td>
<td><p>2011/01/02</p></td>
<td><p>2016/01/01</p></td>
</tr>
<tr class="odd">
<td></td>
<td><p>N/A</p></td>
<td><p>LMDE</p></td>
<td><p>Xfce</p></td>
<td><p>Debian</p></td>
<td><p>2011/04/06</p></td>
<td><p>2016/01/01</p></td>
</tr>
<tr class="even">
<td><p>rowspan=2 </p></td>
<td><p>N/A</p></td>
<td><p>LMDE</p></td>
<td><p>GNOME</p></td>
<td><p>Debian</p></td>
<td><p>2011/09/16</p></td>
<td><p>2016/01/01</p></td>
</tr>
<tr class="odd">
<td><p>Xfce</p></td>
<td><p>2011/09/16</p></td>
<td><p>2016/01/01</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>rowspan=2 </p></td>
<td><p>N/A</p></td>
<td><p>LMDE</p></td>
<td><p>MATE/Cinnamon</p></td>
<td><p>Debian</p></td>
<td><p>2012/04/24</p></td>
<td><p>2016/01/01</p></td>
</tr>
<tr class="odd">
<td><p>Xfce</p></td>
<td><p>2012/04/24</p></td>
<td><p>2016/01/01</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>rowspan=2 </p></td>
<td><p>N/A</p></td>
<td><p>LMDE</p></td>
<td><p>Cinnamon</p></td>
<td><p>Debian</p></td>
<td><p>2013/03/22</p></td>
<td><p>2016/01/01</p></td>
</tr>
<tr class="odd">
<td><p>MATE</p></td>
<td><p>2013/03/22</p></td>
<td><p>2016/01/01</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>rowspan=2 </p></td>
<td><p>N/A</p></td>
<td><p>LMDE</p></td>
<td><p>Cinnamon</p></td>
<td><p>Debian</p></td>
<td><p>2014/03/02</p></td>
<td><p>2016/01/01</p></td>
</tr>
<tr class="odd">
<td><p>MATE</p></td>
<td><p>2014/03/02</p></td>
<td><p>2016/01/01</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>rowspan=2 </p></td>
<td><p><strong>Betsy</strong>[17]</p></td>
<td><p>LMDE</p></td>
<td><p>Cinnamon</p></td>
<td><p>Debian Jessie</p></td>
<td><p>2015/04/10</p></td>
<td><p>2019/01/01</p></td>
</tr>
<tr class="odd">
<td><p>MATE</p></td>
<td><p>2015/04/10</p></td>
<td><p>2019/01/01</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td></td>
<td><p><strong>Cindy</strong>[18]</p></td>
<td><p>LMDE</p></td>
<td><p>Cinnamon</p></td>
<td><p>Debian Stretch</p></td>
<td><p>2018/08/31</p></td>
<td><p>N/A</p></td>
</tr>
<tr class="odd">
<td></td>
<td><p><strong>Debbie</strong>[19]</p></td>
<td><p>LMDE</p></td>
<td><p>Cinnamon</p></td>
<td><p>Debian Buster</p></td>
<td><p>2020/03/20</p></td>
<td><p>N/A</p></td>
</tr>
<tr class="even">
<td><p>バージョン</p></td>
<td><p>コードネーム</p></td>
<td><p>エディション</p></td>
<td><p>デスクトップ環境</p></td>
<td><p>パッケージベース</p></td>
<td><p>リリース日</p></td>
<td><p>サポート期限</p></td>
</tr>
<tr class="odd">
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
</tbody>
</table>

## インストール方法

Live DVDのISOファイルをダウンロードして、インストール可能である。同一バージョンのUbuntuからアップデートすることも可能。

基本的に、Linux MintはUbuntuにパッケージなどを追加したディストリビューションなので、UbuntuにLinux Mint、Canonical Partnerのレポジトリを追加して、Linux Mint関係のソフトウェアをインストールして、デスクトップ環境（Cinnamonなど）の設定を修正するとLinux Mintになる。

## 日本語環境

かつて、各エディションはセットアップ時に日本語を選択する事で不完全な日本語環境であった。そのため整った日本語環境を求める際は公式のローカルコミュニティーであるLinux Mint Japanのリポジトリを追加することによる日本語化が必要であったが、現在は、アップストリームのUbuntu Japanese Teamのリポジトリをそのまま用いるだけで、日本語環境を使用することが可能である。

## Ubuntuとの比較

Linux MintはUbuntuをベースとしており、Ubuntuのソフトウェアリポジトリを使用することから、ほとんどのパッケージは両ディストリビューションで同じであり、二つのシステムはほとんど同じように振る舞う。例えば、Linux Mint 16 "Petra" はUbuntu 13.10 "Saucy Salamander" のパッケージプールを使用する。Linux Mint 17以降は、UbuntuのLTS版のみをベースとする方針に転換した。その間はベースとなるUbuntuのバージョンは維持しつつ、デスクトップや各種ソフトウェアを更新したマイナーバージョンをリリースとすることとした。これらは17.1、17.2、17.3のように、小数位を加えたバージョン番号としている。

もっとも大きな違いはそのデスクトップにある。UbuntuとLinux Mintはどちらも使いやすさにフォーカスしているが、Linux Mintは独自のテーマを提供し、**mintTools**と呼ばれる独自のアプリケーションを搭載している。詳細は[\#mintTools](https://ja.wikipedia.org/wiki/#mintTools "wikilink")に譲るが、例えばmintDesktopはMATEおよびXfceそれぞれのデスクトップの設定、Windowsワークグループおよび近くのネットワークの自動ブラウズを行うツールである。

先述のとおりLinux MintはUbuntuを基にしているため、Linux Mintより非常に大きなコミュニティを持つUbuntuのヘルプやアドバイスは多くの場合でLinux Mintにも同じように適用できる。

## ブランチ

他の多くのLinuxディストリビューションと同様に、Linux Mintにも異なるテストバージョンあるいは “ブランチ” が存在する。最新の機能またはLinux Mintの “不安定ブランチ” を含むブランチは “Romeo” と呼ばれ、Linux Mintリリースにおいてデフォルトで有効になることはない。最先端の機能を求めるユーザや新パッケージのテストを手助けしたいユーザがRomeoを[APT](../Page/APT.md "wikilink")ソースに追加できる。Romeoはそれ自身がブランチではなく、他のリポジトリを置き換えるわけではない。

新しいパッケージは開発者及びテスターによってテストされるRomeoで最初にリリースされる。のちにそのパッケージが十分な安定性があると判断されると最新の安定版リリースにバックポートされる。

## 脚注

## 関連項目

  - [Linuxディストリビューションの比較](../Page/Linuxディストリビューションの比較.md "wikilink")
  - [Linuxライブディストリビューションの比較](../Page/Linuxライブディストリビューションの比較.md "wikilink")

## 外部リンク

  - [Linux Mint](https://www.linuxmint.com/)

  - [Linux Mint Japan](http://linuxmint-jp.net/)

  -
[Category:Ubuntu派生ディストリビューション](https://ja.wikipedia.org/wiki/Category:Ubuntu派生ディストリビューション "wikilink") [Category:フリーソフトウェアOS](https://ja.wikipedia.org/wiki/Category:フリーソフトウェアOS "wikilink") [Category:LiveCD](https://ja.wikipedia.org/wiki/Category:LiveCD "wikilink") [Category:2006年のソフトウェア](https://ja.wikipedia.org/wiki/Category:2006年のソフトウェア "wikilink")

1.
2.
3.
4.
5.  [ftp-adminの憂鬱:Linux Mintのミラーを再開しました](http://ftp-admin.blogspot.jp/2013/06/linux-mint.html)
6.
7.  [Linux Mint Debian Changelog](http://www.linuxmint.com/rel_debian_whatsnew.php)
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
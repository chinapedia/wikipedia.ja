> この記事は[Linuxディストリビューション](https://ja.wikipedia.org/wiki/Linuxディストリビューション)から翻訳されています。


**Linuxディストリビューション**は[Linux](../Page/Linux.md "wikilink")カーネルとその他ソフトウェア群を1つにまとめ、利用者が容易に[インストール](../Page/インストール.md "wikilink")・利用できるようにしたものである。

## 概要

[Linux](../Page/Linux.md "wikilink")カーネルは[プロセス](../Page/プロセス.md "wikilink")や[ソケット通信などの機能を提供する](../Page/ソケット_\(BSD\).md "wikilink")。これらは様々なソフトウェアを動作させるうえで基礎となる重要な機能であるが、ユーザーが利用する機能としては非常にプリミティブである。例えばカーネルそのものにはOS起動時のデーモン自動起動機能は存在しないし、[Bash](../Page/Bash.md "wikilink")のようなインタラクティブコンソール機能も存在しない。これらの機能はすべて[Linux](../Page/Linux.md "wikilink")カーネルを利用する[GNUなどによって作られた個別のソフトウェアによって実現されている](../Page/GNUプロジェクト.md "wikilink")。

ユーザーの利便性を高めるためにLinuxカーネルとこれらソフトウェア群を1つのパッケージにしたものがLinuxディストリビューションである。無償・有償様々な[distribution](https://ja.wikipedia.org/wiki/ディストリビューション "wikilink")＝配布・流通・頒布形態が存在し、各ディストリビューションはその理念・目的によって[派生し](../Page/フォーク_\(ソフトウェア開発\).md "wikilink")、それぞれ異なるソフトウェアをパッケージに含んでいる。ユーザーはLinuxディストリビューションをインストールするだけでシェル機能やパッケージ管理機能、デスクトップ環境などを利用することができる。

## コンポーネント

[Linux_Distribution_Timeline.svg](https://ja.wikipedia.org/wiki/File:Linux_Distribution_Timeline.svg "fig:Linux_Distribution_Timeline.svg") [カーネル](../Page/カーネル.md "wikilink")の他、基本的なUNIXのツールやユーティリティ、その他[サーバ](../Page/サーバ.md "wikilink")向けや[デスクトップ環境](https://ja.wikipedia.org/wiki/デスクトップ環境 "wikilink")向けの[ソフトウェア](../Page/ソフトウェア.md "wikilink")を集め、ビルドして[バイナリパッケージ](https://ja.wikipedia.org/wiki/バイナリパッケージ "wikilink")を作成し提供している。その他、最初のインストールの際に必要な[インストーラ等といった補助的なシステムが付属する](../Page/インストール.md "wikilink")。バイナリパッケージを利用するという形態のために、rpmやdebなど、何らかのバイナリパッケージシステムの採用がほぼ必須であり、どのシステムを採用しているかがディストリビューションの主要な特徴のひとつとなる。aptやyumなどより上位の[パッケージ管理システム](../Page/パッケージ管理システム.md "wikilink")も、現代ではほぼ必須である。

  - [Linuxカーネル](../Page/Linuxカーネル.md "wikilink")
      - （Linuxカーネル以外の場合は「Linuxディストリビューション」ではない（[Debian GNU/kFreeBSDや](https://ja.wikipedia.org/wiki/Debian_GNU/kFreeBSD "wikilink")[Debian GNU/Hurdなど](https://ja.wikipedia.org/wiki/Debian_GNU/Hurd "wikilink")））
      - その他、カーネルモジュール等
  - 必須なツールやユーティリティやライブラリ
      - util-linux（[:en:Util-linux](https://ja.wikipedia.org/wiki/:en:Util-linux "wikilink")）
      - [GNU Core Utilities](../Page/GNU_Core_Utilities.md "wikilink")（coreutilsとも。昔のfileutils, shellutils, textutilsは全てcoreutilsに取り込まれた）
      - [Bourne Shell](../Page/Bourne_Shell.md "wikilink") 互換シェル（他のシェルと違い /bin/sh として必須である(Debian系では[Dashが](https://ja.wikipedia.org/wiki/Debian_Almquist_shell "wikilink")/bin/shに使われることも多い)）
      - [Unixシェル](https://ja.wikipedia.org/wiki/Unixシェル "wikilink")
      - [glibc](https://ja.wikipedia.org/wiki/GNU_Cライブラリ "wikilink")
  - 起動に必要なもの
      - [init](https://ja.wikipedia.org/wiki/init "wikilink")
      - /etc などの基本的なファイル群
      - [GRUBや](../Page/GNU_GRUB.md "wikilink")[LILO](../Page/LILO.md "wikilink")のようなブートローダー
  - エディタ
      - [Emacs](../Page/Emacs.md "wikilink")
      - [nano](../Page/Nano_\(テキストエディタ\).md "wikilink")
      - [vim](https://ja.wikipedia.org/wiki/vim "wikilink")
  - コンパイラ等
      - [GNU Binutils](../Page/GNU_Binutils.md "wikilink") (binutils)
      - [GCC](../Page/GNUコンパイラコレクション.md "wikilink")
  - 各種の設定を行うソフト
  - [スクリプト言語](../Page/スクリプト言語.md "wikilink")
      - [awk](../Page/AWK.md "wikilink")
      - [perl](https://ja.wikipedia.org/wiki/perl "wikilink")
      - [python](https://ja.wikipedia.org/wiki/python "wikilink")
      - [sed](../Page/Sed_\(コンピュータ\).md "wikilink")
  - GUI関係
      - [X11のフリーな実装である](../Page/X_Window_System.md "wikilink")[XFree86](../Page/XFree86.md "wikilink")、[XOrg](../Page/X.Org_Foundation.md "wikilink")
          - [デスクトップ環境](https://ja.wikipedia.org/wiki/デスクトップ環境 "wikilink")として[GNOME](../Page/GNOME.md "wikilink")、[KDE](../Page/KDE.md "wikilink")、[Xfce](../Page/Xfce.md "wikilink")、[LXDE](https://ja.wikipedia.org/wiki/LXDE "wikilink")
          - [ウィンドウマネージャ](../Page/ウィンドウマネージャ.md "wikilink")
  - デスクトップ向けアプリケーション
      - [ウェブブラウザ](../Page/ウェブブラウザ.md "wikilink")
      - [電子メールクライアント](../Page/電子メールクライアント.md "wikilink")
      - [テキストエディタ](../Page/テキストエディタ.md "wikilink")
      - [オフィススイート](../Page/オフィススイート.md "wikilink")
      - [マルチメディア](../Page/マルチメディア.md "wikilink")
      - [ゲーム](../Page/ゲーム.md "wikilink")
  - サーバ向けアプリケーション
      - [メールサーバ](https://ja.wikipedia.org/wiki/メールサーバ "wikilink")
      - [Webサーバ](../Page/Webサーバ.md "wikilink")
      - [データベース管理システム](../Page/データベース管理システム.md "wikilink")
  - ソフトウェア開発向けアプリケーション
      - 多数のコンピュータ言語開発環境

これらはソフトウェア構成の例であり、他にも様々なソフトウェアをインストールできる。

## 配布方法

ディストリビューションは、自由に配布、利用の出来るソフトウェア（[フリーソフトウェア](../Page/フリーソフトウェア.md "wikilink")）だけを集め、無料で提供されるものと、利用に料金を払う必要のある商用ソフトウェアや企業によるサポートを受けられる権利を含んだ有料のものに分けられる。大抵の場合、前者は[FTPなどで公開されており](../Page/File_Transfer_Protocol.md "wikilink")、[Torrent](https://ja.wikipedia.org/wiki/Torrent "wikilink")を利用した配布をするディストリビューション\[1\]も存在する。後者はユーザー数などに制限のあるライセンス契約によって提供される。どちらの場合も、[CD-ROM](../Page/CD-ROM.md "wikilink")等によって入手することができる。GNU/Linuxディストリビューターによっては両方を用意している場合や、サポートのみ有償で受けられる場合もある。

## Debian系

[Screenshot-debian_wheezy_ja.png](https://ja.wikipedia.org/wiki/File:Screenshot-debian_wheezy_ja.png "fig:Screenshot-debian_wheezy_ja.png") [Debianの派生品一覧に掲載されるものは](https://ja.wikipedia.org/wiki/:en:List_of_Linux_distributions#Debian-based "wikilink")、パッケージ管理システムに[deb](https://ja.wikipedia.org/wiki/deb "wikilink")形式を使っている。
*[Debian\#その他の派生版](https://ja.wikipedia.org/wiki/Debian#その他の派生版 "wikilink")も参照。*主要なものは以下の通り。

| 配布版                                              | 説明                                                                                               |
| ------------------------------------------------ | ------------------------------------------------------------------------------------------------ |
| [Debian GNU/Linux](../Page/Debian.md "wikilink") | 100%[フリーソフトウェア](../Page/フリーソフトウェア.md "wikilink")であることが理念、[コミュニティで開発](../Page/共同体.md "wikilink")。 |

### Debian (テスト版) 派生

[DebianFamilyTree1210.svg](https://ja.wikipedia.org/wiki/File:DebianFamilyTree1210.svg "fig:DebianFamilyTree1210.svg") [Debianテスト版の派生品一覧に掲載](https://ja.wikipedia.org/wiki/:en:List_of_Linux_distributions#Debian_\(Testing\)_based "wikilink")。

<table>
<thead>
<tr class="header">
<th><p>配布版</p></th>
<th><p>説明</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><a href="https://ja.wikipedia.org/wiki/BackTrack" title="wikilink">BackTrack</a></p></td>
<td><p>Debian派生であり、Kali Linuxの前身。<a href="https://ja.wikipedia.org/wiki/ペネトレーションテスト" title="wikilink">侵入テスト目的に特化していることが特徴だった</a>。後継の Kali Linux に移行。</p></td>
</tr>
<tr class="even">
<td><p><a href="https://ja.wikipedia.org/wiki/Kali_Linux" title="wikilink">Kali Linux</a></p></td>
<td><p>Debian派生の1DVD型。侵入テスト目的に特化していることが特徴。BackTrackから<a href="../Page/フォーク_(ソフトウェア開発).md" title="wikilink">派生した後継版</a>。</p></td>
</tr>
<tr class="odd">
<td><p><a href="../Page/PureOS.md" title="wikilink">PureOS</a></p></td>
<td><p>完全にフリーソフトウェアだけで構成されている、<a href="../Page/プライバシー.md" title="wikilink">プライバシー</a>と<a href="https://ja.wikipedia.org/wiki/セキュリティ" title="wikilink">セキュリティ</a>、利便性に重点を置いているGNU/Linuxディストリビューション。</p></td>
</tr>
<tr class="even">
<td></td>
<td><p><a href="https://ja.wikipedia.org/wiki/ロシア連邦" title="wikilink">ロシアの政府機関における</a><a href="https://ja.wikipedia.org/wiki/:ru:Astra_Linux" title="wikilink">制式OSのひとつ</a>[2]。</p></td>
</tr>
<tr class="odd">
<td><p><a href="../Page/Ubuntu.md" title="wikilink">Ubuntu</a></p></td>
<td><p>6ヶ月ごとの更新と商用の保守を掲げる。デスクトップ環境として<a href="../Page/GNOME.md" title="wikilink">GNOME</a>を採用している。<a href="../Page/パソコン雑誌.md" title="wikilink">パソコン雑誌</a>に雑誌社特製のLive CD/DVDとして付属される場合がある。<a href="https://ja.wikipedia.org/wiki/Ubuntu#派生品" title="wikilink">多彩な派生版が存在</a>。</p></td>
</tr>
</tbody>
</table>

### Ubuntu 派生

主なものは、[Ubuntuの派生品一覧に掲載](https://ja.wikipedia.org/wiki/:en:List_of_Linux_distributions#Ubuntu-based "wikilink")。

#### 公式

これらはUbuntuと異なるパッケージを導入するだけであるが、それらの[リポジトリ](../Page/リポジトリ.md "wikilink")はUbuntuと同じである。お互いに全く同じパッケージを使え、それぞれのデスクトップ環境を共存させられる。 [Screenshot_of_Ubuntu_15.10_Desktop_live_CD.png](https://ja.wikipedia.org/wiki/File:Screenshot_of_Ubuntu_15.10_Desktop_live_CD.png "fig:Screenshot_of_Ubuntu_15.10_Desktop_live_CD.png") [Kubuntu-13.10-Saucy-Salamander.png](https://ja.wikipedia.org/wiki/File:Kubuntu-13.10-Saucy-Salamander.png "fig:Kubuntu-13.10-Saucy-Salamander.png") [Xubuntu_14.04_LTS.png](https://ja.wikipedia.org/wiki/File:Xubuntu_14.04_LTS.png "fig:Xubuntu_14.04_LTS.png") [公式派生品一覧に掲載](https://ja.wikipedia.org/wiki/:en:List_of_Linux_distributions#Official_distributions "wikilink")。

<table>
<thead>
<tr class="header">
<th><p>配布版</p></th>
<th><p>説明</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><a href="../Page/Kubuntu.md" title="wikilink">Kubuntu</a></p></td>
<td><p>Ubuntuの<a href="https://ja.wikipedia.org/wiki/デスクトップ環境" title="wikilink">デスクトップ環境</a>を <a href="../Page/KDE.md" title="wikilink">KDE</a> に置換したもの。</p></td>
</tr>
<tr class="even">
<td><p><a href="https://ja.wikipedia.org/wiki/Lubuntu" title="wikilink">Lubuntu</a></p></td>
<td><p>Ubuntuのデスクトップ環境を <a href="https://ja.wikipedia.org/wiki/LXDE" title="wikilink">LXDE</a> に置換したもの。18.10以降は <a href="https://ja.wikipedia.org/wiki/LXQt" title="wikilink">LXQt</a> を採用している。比較的「軽い」ディストリビューション。</p></td>
</tr>
<tr class="odd">
<td><p><a href="../Page/Ubuntu_Budgie.md" title="wikilink">Ubuntu Budgie</a></p></td>
<td><p>と呼ばれるデスクトップ環境を採用。16.04世代から公式入りとなった。</p></td>
</tr>
<tr class="even">
<td></td>
<td><p><a href="../Page/中国.md" title="wikilink">中国</a>向けに開発されたディストリビューション。</p></td>
</tr>
<tr class="odd">
<td><p><a href="https://ja.wikipedia.org/wiki/Ubuntu_MATE" title="wikilink">Ubuntu MATE</a></p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/MATE_(デスクトップ環境)" title="wikilink">MATE</a>（マテ）と呼ばれるデスクトップ環境を採用。15.04世代から公式入りとなった。</p></td>
</tr>
<tr class="even">
<td><p><a href="https://ja.wikipedia.org/wiki/Ubuntu#導入" title="wikilink">Ubuntu Server</a></p></td>
<td><p>サーバー向けのディストリビューション。詳細は<a href="https://ja.wikipedia.org/wiki/:en:Ubuntu#Official_distributions" title="wikilink">Ubuntu Server（英語版）も参照</a>。</p></td>
</tr>
<tr class="odd">
<td><p><a href="../Page/Ubuntu_Studio.md" title="wikilink">Ubuntu Studio</a></p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/クリエイター" title="wikilink">クリエイター</a>向けのディストリビューション。</p></td>
</tr>
<tr class="even">
<td><p><a href="https://ja.wikipedia.org/wiki/Xubuntu" title="wikilink">Xubuntu</a></p></td>
<td><p>Ubuntu のデスクトップ環境を <a href="../Page/Xfce.md" title="wikilink">Xfce</a> に置換したもの。比較的「軽い」ディストリビューション。</p></td>
</tr>
</tbody>
</table>

#### 公式から外れた派生品

[thumb](https://ja.wikipedia.org/wiki/ファイル:Ubuntu_Gnome_17.04.png "wikilink") 17.04\]\] [UbuntuFamilyTree1210.svg](https://ja.wikipedia.org/wiki/File:UbuntuFamilyTree1210.svg "fig:UbuntuFamilyTree1210.svg") [公式から外れた派生品一覧に掲載](https://ja.wikipedia.org/wiki/:en:List_of_Linux_distributions#Discontinued_official_distributions "wikilink")。

<table>
<thead>
<tr class="header">
<th><p>配布版</p></th>
<th><p>説明</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><a href="../Page/Edubuntu.md" title="wikilink">Edubuntu</a></p></td>
<td><p>教育用に最適化されたもの。児童が学校や自宅で同等の環境を利用できることを目的としている。</p></td>
</tr>
<tr class="even">
<td></td>
<td><p><a href="../Page/フリーソフトウェア.md" title="wikilink">フリーソフトウェア</a>のみを利用した<a href="https://ja.wikipedia.org/wiki/ディストリビューション" title="wikilink">ディストリビューション</a>。既に本家に合流しており、この方向性は外部ディストリビューション<a href="https://ja.wikipedia.org/wiki/gNewSense" title="wikilink">gNewSense</a>に受け継がれている。</p></td>
</tr>
<tr class="odd">
<td><p><a href="https://ja.wikipedia.org/wiki/Mythbuntu" title="wikilink">Mythbuntu</a></p></td>
<td><p>Ubuntuと<a href="../Page/MythTV.md" title="wikilink">MythTV</a>を元に作られた、<a href="../Page/ホームシアター.md" title="wikilink">ホームシアター</a>PC向けのディストリビューション。デスクトップ環境は標準で<a href="../Page/Xfce.md" title="wikilink">Xfce</a>を採用している。</p></td>
</tr>
<tr class="even">
<td><p><a href="https://ja.wikipedia.org/wiki/Ubuntu_for_Android" title="wikilink">Ubuntu for Android</a></p></td>
<td><p><a href="../Page/Android_(オペレーティングシステム).md" title="wikilink">Android端末向けのディストリビューション</a>。</p></td>
</tr>
<tr class="odd">
<td><p><a href="https://ja.wikipedia.org/wiki/Ubuntu_GNOME" title="wikilink">Ubuntu GNOME</a></p></td>
<td><p>Ubuntuのデスクトップシェルを <a href="https://ja.wikipedia.org/wiki/GNOME_Shell" title="wikilink">GNOME Shell</a> に置換したもの。上記の通り17.10より本家の環境がGNOMEに戻ったため、17.04を最後に開発は途絶えている。</p></td>
</tr>
<tr class="even">
<td></td>
<td><p>現在は<a href="https://ja.wikipedia.org/wiki/Ubuntu#導入" title="wikilink">サーバー版の一部に含まれている</a>。</p></td>
</tr>
<tr class="odd">
<td></td>
<td><p>組み込み端末向けに作成されたディスリビューション。現在は、Ubuntu Touchに引き継がれている。</p></td>
</tr>
<tr class="even">
<td></td>
<td><p><a href="https://ja.wikipedia.org/wiki/ネットブック" title="wikilink">ネットブック</a>等の<a href="https://ja.wikipedia.org/wiki/携帯端末" title="wikilink">携帯端末</a>向けのディストリビューション。普通の<a href="https://ja.wikipedia.org/wiki/パソコン" title="wikilink">パソコン</a>に比べて非力な<a href="../Page/CPU.md" title="wikilink">CPU</a>、小さい画面、<a href="../Page/タッチパネル.md" title="wikilink">タッチパネル</a>の存在を意識した構成となっている</p></td>
</tr>
<tr class="odd">
<td></td>
<td><p>Ubuntu Mobileの後継版。<a href="https://ja.wikipedia.org/wiki/タブレット端末" title="wikilink">タブレット端末</a>向けのディストリビューション。</p></td>
</tr>
<tr class="even">
<td></td>
<td><p><a href="https://ja.wikipedia.org/wiki/スマートTV" title="wikilink">スマートTV</a>向けのディストリビューション。</p></td>
</tr>
</tbody>
</table>

#### 非公式

次のような複数の非公式な[派生物がある](../Page/フォーク_\(ソフトウェア開発\).md "wikilink")。これらのプロジェクトの中には、Ubuntuと密接に関わり、同時に開発・公開され、パッケージも同じ公式リポジトリを利用しているものもある。 [thumb](https://ja.wikipedia.org/wiki/ファイル:Linux_Mint_19_"Tara"_\(Cinnamon\).png "wikilink") 19 (Bionic Beaver 18.04 LTS ベース)\]\] [非公式派生品一覧に掲載](https://ja.wikipedia.org/wiki/:en:List_of_Linux_distributions#Third-party_distributions "wikilink")。
*[Ubuntu\#その他の派生品](https://ja.wikipedia.org/wiki/Ubuntu#その他の派生品 "wikilink")も参照。*

<table>
<thead>
<tr class="header">
<th><p>配布版</p></th>
<th><p>説明</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><a href="../Page/Bodhi_Linux.md" title="wikilink">Bodhi Linux</a></p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/Enlightenment" title="wikilink">Enlightenment</a>から派生した<a href="../Page/ウィンドウマネージャ.md" title="wikilink">ウィンドウマネージャ</a>、Mokshaを採用した軽量版。</p></td>
</tr>
<tr class="even">
<td></td>
<td><p>マルチメディアの製作・配給向け <a href="../Page/Live_CD.md" title="wikilink">Live CD</a>。</p></td>
</tr>
<tr class="odd">
<td></td>
<td><p>ASUSのEeePCやAcerのAspireなど、ネットブックに特化したディストリビューション。改名前は Ubuntu Eee として開発されていた。</p></td>
</tr>
<tr class="even">
<td><p><a href="https://ja.wikipedia.org/wiki/eeeUbuntu" title="wikilink">eeeUbuntu</a></p></td>
<td><p><a href="../Page/Eee_PC.md" title="wikilink">Eee PC専用に構成されたディストリビューション</a>。非公式の日本語版も存在していたが、統合により開発は終了した。本家はに改名し開発継続。</p></td>
</tr>
<tr class="odd">
<td><p><a href="https://ja.wikipedia.org/wiki/elementary_OS" title="wikilink">elementary OS</a></p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/デスクトップ環境" title="wikilink">デスクトップ環境</a>として独自のPantheonを採用している。<a href="https://ja.wikipedia.org/wiki/macOS" title="wikilink">macOS</a>風の美しい画面が特徴。</p></td>
</tr>
<tr class="even">
<td></td>
<td><p><a href="https://ja.wikipedia.org/wiki/Xubuntu" title="wikilink">Xubuntu</a>から派生。Xfce採用、<a href="../Page/Dock.md" title="wikilink">Dock</a>あり。</p></td>
</tr>
<tr class="odd">
<td><p><a href="../Page/Goobuntu.md" title="wikilink">Goobuntu</a></p></td>
<td><p><a href="../Page/Google.md" title="wikilink">Google</a>がUbuntu派生ディストリビューションを作成[3][4]している噂があった。Googleはこれを認めたが社外に公開する予定はないと明言している[5][6]。非公開。</p></td>
</tr>
<tr class="even">
<td><p><a href="https://ja.wikipedia.org/wiki/gOS" title="wikilink">gOS</a></p></td>
<td><p>2007年11月1日に登場したUbuntuの派生ディストリビューション。<a href="../Page/ウォルマート.md" title="wikilink">ウォルマート</a>の低価格PC として開発された。Googleのオンライン・アプリへのアクセスを優先した設計である。デザインは <a href="https://ja.wikipedia.org/wiki/macOS" title="wikilink">Mac OS X</a> が模され、<a href="../Page/Wine.md" title="wikilink">Wine</a>を標準搭載している。開発停止。</p></td>
</tr>
<tr class="odd">
<td><p><a href="../Page/KDE_neon.md" title="wikilink">KDE neon</a></p></td>
<td><p>KDEを採用、LTSから派生。</p></td>
</tr>
<tr class="even">
<td></td>
<td><p>Ubuntu LTS（長期サポート版）を基に開発。Xfce採用でアイコンや壁紙が美しい。アプリの追加や削除、<a href="../Page/ウェブブラウザ.md" title="wikilink">WEBブラウザの</a><a href="../Page/キャッシュ_(コンピュータシステム).md" title="wikilink">キャッシュの削除なども容易</a>。</p></td>
</tr>
<tr class="odd">
<td><p><a href="../Page/Linux_Mint.md" title="wikilink">Linux Mint</a></p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/MATE_(デスクトップ環境)" title="wikilink">MATEや</a><a href="https://ja.wikipedia.org/wiki/Cinnamon" title="wikilink">Cinnamon</a>の採用で見た目やソフトウェア環境を変更し、<a href="../Page/マルチメディア.md" title="wikilink">マルチメディア</a>関係の<a href="../Page/コーデック.md" title="wikilink">コーデック</a>を充実させたディストリビューション。</p></td>
</tr>
<tr class="even">
<td><p><a href="https://ja.wikipedia.org/wiki/Peppermint" title="wikilink">Peppermint OS</a></p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/chromium" title="wikilink">chromium</a>を搭載している軽量のディストリビューション。<a href="https://ja.wikipedia.org/wiki/Webアプリケーション" title="wikilink">webアプリとの連携も強い</a>。</p></td>
</tr>
<tr class="odd">
<td><p><a href="https://ja.wikipedia.org/wiki/xPUD" title="wikilink">PUD</a></p></td>
<td><p>64MBのディストリビューション[7]。中国企業が支援する軽量版。</p></td>
</tr>
<tr class="even">
<td><p><a href="https://ja.wikipedia.org/wiki/Trisquel_GNU/Linux" title="wikilink">Trisquel GNU/Linux</a></p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/GNU_FSDG" title="wikilink">GNU FSDGに適合する</a>100%<a href="https://ja.wikipedia.org/wiki/フリーソフト" title="wikilink">フリーソフト</a>で構成されたOS。</p></td>
</tr>
<tr class="odd">
<td><p><a href="https://ja.wikipedia.org/wiki/Zorin_OS" title="wikilink">Zorin OS</a></p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/Windows" title="wikilink">Windows</a>風のUIを提供するディストリビューション。<a href="../Page/Wine.md" title="wikilink">Wine</a>を標準搭載しWindowsアプリも動作する。</p></td>
</tr>
</tbody>
</table>

### Debian (安定板) 派生

[Debian安定板の派生品一覧に掲載](https://ja.wikipedia.org/wiki/:en:List_of_Linux_distributions#Debian_\(Stable\)_based "wikilink")。

<table>
<thead>
<tr class="header">
<th><p>配布版</p></th>
<th><p>説明</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><p><a href="https://ja.wikipedia.org/wiki/ロシア連邦" title="wikilink">ロシアの政府機関における</a><a href="https://ja.wikipedia.org/wiki/:ru:Astra_Linux" title="wikilink">制式OSのひとつ</a>。</p></td>
</tr>
<tr class="even">
<td></td>
<td><p>企業向けディストリビューションで<a href="../Page/Eee_PC.md" title="wikilink">Eee PCに搭載されていた</a>、後継版の<a href="../Page/Xandros.md" title="wikilink">Xandros</a>に移行。</p></td>
</tr>
<tr class="odd">
<td><p><a href="https://ja.wikipedia.org/wiki/CrunchBang_Linux" title="wikilink">CrunchBang Linux</a></p></td>
<td><p>ウィンドウマネージャにOpenBoxを採用し、軽量、高速を重視したディストリビューション。開発停止。</p></td>
</tr>
<tr class="even">
<td><p><a href="../Page/Deepin.md" title="wikilink">Deepin</a></p></td>
<td><p>Wuhan Deepin Technology Co.が開発を手掛ける、Debianを母体とした中国産 Linux ディストリビューション。</p></td>
</tr>
<tr class="odd">
<td><p><a href="https://ja.wikipedia.org/wiki/Devuan" title="wikilink">Devuan</a></p></td>
<td><p>2014 に Debianから派生[8]。</p></td>
</tr>
<tr class="even">
<td><p><a href="https://ja.wikipedia.org/wiki/gNewSense" title="wikilink">gNewSense</a></p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/GNU_FSDG" title="wikilink">GNU FSDGに適合し</a>、<a href="../Page/フリーソフトウェア財団.md" title="wikilink">フリーソフトウェア財団</a>の支援を受ける。<a href="https://ja.wikipedia.org/wiki/Linux-libre" title="wikilink">Linux-libre</a>を使用し、ファームウェアの部分まで100%フリーソフトで構成される。</p></td>
</tr>
<tr class="odd">
<td></td>
<td><p>Debian派生でCD起動/HDD導入共可能。</p></td>
</tr>
<tr class="even">
<td><p><a href="../Page/KNOPPIX.md" title="wikilink">KNOPPIX</a></p></td>
<td><p>Debianを基にCD起動で利用できるようにしている。派生版は<a href="https://ja.wikipedia.org/wiki/#KNOPPIX_派生" title="wikilink">#KNOPPIX 派生を参照</a>。</p></td>
</tr>
<tr class="odd">
<td><p><a href="https://ja.wikipedia.org/wiki/Maemo" title="wikilink">Maemo</a></p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/Nokia_N800" title="wikilink">Nokia N800</a>, <a href="https://ja.wikipedia.org/wiki/Nokia_N810" title="wikilink">N810など携帯端末のほか</a>、<a href="https://ja.wikipedia.org/wiki/Nokia_N900" title="wikilink">Nokia N900</a> <a href="https://ja.wikipedia.org/wiki/タブレット端末" title="wikilink">タブレット端末</a>とその他の Linux kernel派生の機器向けに開発された[9]。</p></td>
</tr>
<tr class="even">
<td><p><a href="../Page/MEPIS.md" title="wikilink">MEPIS</a></p></td>
<td><p>デスクトップ環境に<a href="../Page/KDE.md" title="wikilink">KDE</a>を採用したディストリビューション。開発停止。派生版は<a href="https://ja.wikipedia.org/wiki/#MEPIS_派生" title="wikilink">#MEPIS 派生を参照</a>。</p></td>
</tr>
<tr class="odd">
<td><p><a href="../Page/Linux_Mint.md" title="wikilink">MintPPC</a></p></td>
<td><p>PowerPC 向け。MintPPC は Mint LXDE のコードを用いるが、Linux Mint ではない[10]。</p></td>
</tr>
<tr class="even">
<td></td>
<td><p><a href="../Page/GNOME.md" title="wikilink">GNOME</a>やWindowマネージャーの<a href="https://ja.wikipedia.org/wiki/fluxbox" title="wikilink">fluxbox</a>を使用するが前身。[11]</p></td>
</tr>
<tr class="odd">
<td><p><a href="https://ja.wikipedia.org/wiki/OpenZaurus" title="wikilink">OpenZaurus</a></p></td>
<td><p><a href="../Page/シャープ.md" title="wikilink">Sharp</a> <a href="../Page/ザウルス.md" title="wikilink">Zaurus</a> <a href="../Page/携帯情報端末.md" title="wikilink">PDA向け</a> Debian パッケージと ROM イメージ。 後継[12]。</p></td>
</tr>
<tr class="even">
<td><p><a href="https://ja.wikipedia.org/wiki/Raspberry_Pi_OS" title="wikilink">Raspberry Pi OS</a></p></td>
<td><p>小型シングルボードコンピュータである<a href="https://ja.wikipedia.org/wiki/Raspberry_Pi" title="wikilink">Raspberry Pi向けに開発されたディストリビューション</a>。</p></td>
</tr>
<tr class="odd">
<td><p><a href="https://ja.wikipedia.org/wiki/Skolelinux" title="wikilink">Skolelinux</a></p></td>
<td><p><a href="../Page/ノルウェー.md" title="wikilink">ノルウェー</a>産 Linux で、学校向け <a href="https://ja.wikipedia.org/wiki/thin_client" title="wikilink">thin clientディストリビューション</a>[13]。</p></td>
</tr>
<tr class="even">
<td><p><a href="https://ja.wikipedia.org/wiki/SolydXK" title="wikilink">SolydXK</a></p></td>
<td><p><a href="../Page/Xfce.md" title="wikilink">Xfce</a> and <a href="../Page/KDE.md" title="wikilink">KDE</a> desktop focused on stability, security and ease of use.[14]</p></td>
</tr>
<tr class="odd">
<td><p><a href="https://ja.wikipedia.org/wiki/The_Amnesic_Incognito_Live_System" title="wikilink">The Amnesic Incognito Live System</a> (TAILS)</p></td>
<td><p>プライバシーと匿名性の保護に特化したディストリビューション。<a href="https://ja.wikipedia.org/wiki/Tor#Torの応用" title="wikilink">Tor#Torの応用</a>も参照。このほか、セキュリティ面重視のOS・<a href="../Page/Whonix.md" title="wikilink">Whonix</a>もDebianから派生している。</p></td>
</tr>
<tr class="even">
<td><p><a href="https://ja.wikipedia.org/wiki/Vyatta" title="wikilink">Vyatta</a></p></td>
<td><p>VyOSの前身[15]。</p></td>
</tr>
<tr class="odd">
<td><p><a href="https://ja.wikipedia.org/wiki/VyOS" title="wikilink">VyOS</a></p></td>
<td><p><a href="../Page/Virtual_Private_Network.md" title="wikilink">VPN</a> / <a href="../Page/ルーター.md" title="wikilink">ルーター</a> / <a href="../Page/コンピュータネットワーク.md" title="wikilink">ネットワーク</a><a href="../Page/ファイアウォール.md" title="wikilink">ファイアウォール</a>用ディストリビューション。</p></td>
</tr>
</tbody>
</table>

### MEPIS 派生

[MEPISの派生品一覧に掲載](https://ja.wikipedia.org/wiki/:en:List_of_Linux_distributions#MEPIS-based "wikilink")。

| 配布版                                                     | 説明                                                     |
| ------------------------------------------------------- | ------------------------------------------------------ |
| [antiX](https://ja.wikipedia.org/wiki/antiX "wikilink") | Debian安定版から派生した軽量な Live CD かつインストール（導入）可能なディストリビューション。 |
| [MX Linux](../Page/MX_Linux.md "wikilink")              | 中量級。KNOPPIXのように Live CD としても利用可能。                      |

### KNOPPIX 派生

[KnoppixFamilyTree1210.svg](https://ja.wikipedia.org/wiki/File:KnoppixFamilyTree1210.svg "fig:KnoppixFamilyTree1210.svg") [KNOPPIXの派生品一覧に掲載](https://ja.wikipedia.org/wiki/:en:List_of_Linux_distributions#Knoppix-based "wikilink")。
*[KNOPPIX\#その他の派生版](https://ja.wikipedia.org/wiki/KNOPPIX#その他の派生版 "wikilink")も参照。*

| 配布版                                                        | 説明                                                                                                                |
| ---------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------- |
| [Damn Small Linux](../Page/Damn_Small_Linux.md "wikilink") | 名刺大の[CDやUSB](../Page/コンパクトディスク.md "wikilink") pendrive向けの軽量なKNOPPIX[Live CD](../Page/Live_CD.md "wikilink")。開発停止。 |

## Red Hat系

[RedHatFamilyTree1210.svg](https://ja.wikipedia.org/wiki/File:RedHatFamilyTree1210.svg "fig:RedHatFamilyTree1210.svg") ※[RPM系派生版一覧に掲載され](https://ja.wikipedia.org/wiki/:en:List_of_Linux_distributions#RPM-based "wikilink")、[パッケージ管理として](../Page/パッケージ管理システム.md "wikilink")[RPMを使っている](../Page/RPM_Package_Manager.md "wikilink")。
*[Red Hat Linux\#その他の派生版も参照](https://ja.wikipedia.org/wiki/Red_Hat_Linux#その他の派生版 "wikilink")。*主要なものは以下の通り。

<table>
<thead>
<tr class="header">
<th><p>配布版</p></th>
<th><p>説明</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><a href="../Page/Red_Hat_Linux.md" title="wikilink">Red Hat Linux</a></p></td>
<td><p>商用および個人用。開発終了。<br />
個人用は<a href="../Page/Fedora.md" title="wikilink">Fedora Coreへ事実上開発を引き継ぎ</a>。<br />
商用版は後継版の<a href="../Page/Red_Hat_Enterprise_Linux.md" title="wikilink">Red Hat Enterprise Linuxで</a>、<a href="https://ja.wikipedia.org/wiki/Fedora_Project" title="wikilink">Fedora Projectによるテスト済みのFedoraを母体とし安定させたもの</a>。</p></td>
</tr>
<tr class="even">
<td><p><a href="../Page/CentOS.md" title="wikilink">CentOS</a></p></td>
<td><p>Red Hat Enterprise Linuxの無償版。</p></td>
</tr>
<tr class="odd">
<td><p><a href="../Page/Fedora.md" title="wikilink">Fedora</a></p></td>
<td><p>Red Hat Linux 後継のコミュニティFedora Projectによる実験要素が強い。Fedora 7よりFedoraLiveCDも同時公開。</p></td>
</tr>
<tr class="even">
<td><p><a href="https://ja.wikipedia.org/wiki/Mandrake_Linux" title="wikilink">Mandrake Linux</a></p></td>
<td><p><a href="../Page/Mandriva_Linux.md" title="wikilink">Mandriva Linuxの前身</a>。開発終了。</p></td>
</tr>
</tbody>
</table>

### CentOS/RHEL派生

※[CentOS/RHEL派生版一覧に掲載され](https://ja.wikipedia.org/wiki/:en:List_of_Linux_distributions#CentOS/RHEL-based "wikilink")、パッケージ管理等が同様のもの。

<table>
<thead>
<tr class="header">
<th><p>配布版</p></th>
<th><p>説明</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><a href="../Page/Asianux.md" title="wikilink">Asianux</a></p></td>
<td><p><a href="../Page/Red_Hat_Enterprise_Linux.md" title="wikilink">Red Hat Enterprise Linux派生</a>。<a href="https://ja.wikipedia.org/wiki/日本" title="wikilink">日</a>、<a href="../Page/中国.md" title="wikilink">中</a>、<a href="https://ja.wikipedia.org/wiki/韓国" title="wikilink">韓</a>、<a href="https://ja.wikipedia.org/wiki/越南" title="wikilink">越</a>、<a href="../Page/タイ.md" title="wikilink">タイ</a>の<a href="../Page/アジア.md" title="wikilink">アジア</a>5ヵ国の企業が共同開発。前身は<a href="../Page/MIRACLE_LINUX.md" title="wikilink">MIRACLE LINUX</a>、、<a href="../Page/Haansoft_Linux.md" title="wikilink">Haansoft Linux</a>（韓国製）。</p></td>
</tr>
<tr class="even">
<td></td>
<td><p>Small Business Server. File, Print, Messaging, <a href="https://ja.wikipedia.org/wiki/UTM" title="wikilink">UTM</a>, <a href="https://ja.wikipedia.org/wiki/VPN" title="wikilink">VPN</a>.</p></td>
</tr>
<tr class="odd">
<td><p><a href="https://ja.wikipedia.org/wiki/Fermi_Linux_LTS" title="wikilink">Fermi Linux LTS</a></p></td>
<td><p>Scientific Linuxの前身。フェルミ国立加速器研究所の研究施設に特有のソフトウェアを追加[16]。</p></td>
</tr>
<tr class="even">
<td><p><a href="../Page/MIRACLE_LINUX.md" title="wikilink">MIRACLE LINUX</a></p></td>
<td><p>商用、<a href="../Page/Oracle_Database.md" title="wikilink">Oracle対応</a>、日本製。Asianuxへと移行。</p></td>
</tr>
<tr class="odd">
<td><p><a href="../Page/Oracle_Linux.md" title="wikilink">Oracle Linux</a></p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/Oracle" title="wikilink">Oracle</a>がOracle製品に最適化したUnbreakable Enterprise Kernel（UEK）を採用。</p></td>
</tr>
<tr class="even">
<td></td>
<td><p><a href="https://ja.wikipedia.org/wiki/:zh:紅旗Linux" title="wikilink">紅旗Linux</a> 是<a href="../Page/中華人民共和国.md" title="wikilink">中国製</a>。Asianuxへと移行。</p></td>
</tr>
<tr class="odd">
<td></td>
<td><p>RHEL(初期版)とCentOS(最近の配布版)より派生。</p></td>
</tr>
<tr class="even">
<td><p><a href="../Page/Scientific_Linux.md" title="wikilink">Scientific Linux</a></p></td>
<td><p>Fermi Linuxの後継。Red Hat Enterprise Linuxから派生。</p></td>
</tr>
<tr class="odd">
<td></td>
<td><p>CentOSから派生。</p></td>
</tr>
</tbody>
</table>

### Fedora派生

[FedoraFamilyTree1210.svg](https://ja.wikipedia.org/wiki/File:FedoraFamilyTree1210.svg "fig:FedoraFamilyTree1210.svg") ※[Fedora派生版一覧に掲載され](https://ja.wikipedia.org/wiki/:en:List_of_Linux_distributions#Fedora-based "wikilink")、パッケージ管理等が同様のもの

| 配布版                                                                                 | 説明                                                                                                                                                                                                                                                                                                                                   |
| ----------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| [Berry Linux](https://ja.wikipedia.org/wiki/Berry_Linux "wikilink")                 | [日本人](https://ja.wikipedia.org/wiki/日本人 "wikilink")の中田裕一朗が[Fedora](../Page/Fedora.md "wikilink")を母体に開発。                                                                                                                                                                                                                              |
| [MeeGo](https://ja.wikipedia.org/wiki/MeeGo "wikilink")                             | [携帯機器](../Page/携帯機器.md "wikilink")向け[オープンソース](../Page/オープンソース.md "wikilink")[Linux](../Page/Linux.md "wikilink")[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink")。2011年9月29日に発売された[ノキア](../Page/ノキア.md "wikilink")スマートフォン「[N9](https://ja.wikipedia.org/wiki/:en:Nokia_N9 "wikilink")」に搭載された\[17\]\[18\]。                           |
| [Moblin](https://ja.wikipedia.org/wiki/Moblin "wikilink")                           | [Atomなどの](../Page/Intel_Atom.md "wikilink")[インテル](https://ja.wikipedia.org/wiki/インテル "wikilink")製[プロセッサ](../Page/プロセッサ.md "wikilink")（処理装置）を採用している[ネットブック](https://ja.wikipedia.org/wiki/ネットブック "wikilink")や[Mobile Internet Device](https://ja.wikipedia.org/wiki/Mobile_Internet_Device "wikilink")（MID）などの携帯機器向けLinuxディストリビューション。 |
| [Qubes OS](https://ja.wikipedia.org/wiki/Qubes_OS "wikilink")                       | [セキュリティ](https://ja.wikipedia.org/wiki/セキュリティ "wikilink")に特化したOS。                                                                                                                                                                                                                                                                    |
| [Sugar-on-a-Stick Linux](https://ja.wikipedia.org/wiki/Sugar_\(ソフトウェア\) "wikilink") | [Sugar Labsが開発する](https://ja.wikipedia.org/wiki/Sugar_Labs "wikilink")[デスクトップ環境](https://ja.wikipedia.org/wiki/デスクトップ環境 "wikilink")で、Fedoraと組み合わせ用いられた。主に[OLPC XO-1などの教育用](https://ja.wikipedia.org/wiki/OLPC_XO-1 "wikilink")[パーソナルコンピューター](https://ja.wikipedia.org/wiki/パーソナルコンピューター "wikilink")向け。                               |
| [Yellow Dog Linux](../Page/Yellow_Dog_Linux.md "wikilink")                          | [Fedora](../Page/Fedora.md "wikilink")派生で[PowerPC](../Page/PowerPC.md "wikilink")専用。[PlayStation 3公式対応](https://ja.wikipedia.org/wiki/PlayStation_3 "wikilink")。開発停止。                                                                                                                                                                |

### urpmi系

※[urpmi系派生版一覧に掲載](https://ja.wikipedia.org/wiki/:en:List_of_Linux_distributions#urpmi-based "wikilink")。（）も参照。

| 配布版                                                                 | 説明                                                                                                                                                                                                                                  |
| ------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [Mandriva Linux](../Page/Mandriva_Linux.md "wikilink")              | 旧名称は、[Mandrakelinux](https://ja.wikipedia.org/wiki/Mandrakelinux "wikilink")。商用版と無料版があった。[Live CD版はMandriva](../Page/Live_CD.md "wikilink") Oneで、[GNOME](../Page/GNOME.md "wikilink")版と[KDE](../Page/KDE.md "wikilink")版が存在した。開発終了。 |
| [Mageia](https://ja.wikipedia.org/wiki/Mageia "wikilink")           | [Mandriva Linuxを母体に開発](../Page/Mandriva_Linux.md "wikilink")。オープンソース。                                                                                                                                                               |
| [OpenMandriva Lx](../Page/OpenMandriva_Lx.md "wikilink")            | Mandriva Linux派生。                                                                                                                                                                                                                   |
| [Unity Linux](https://ja.wikipedia.org/wiki/Unity_Linux "wikilink") | Mandriva Linux派生。                                                                                                                                                                                                                   |

### apt-rpm系

[Vine61_desktop.png](https://ja.wikipedia.org/wiki/File:Vine61_desktop.png "fig:Vine61_desktop.png") ※[apt-rpm系派生版一覧に掲載](https://ja.wikipedia.org/wiki/:en:List_of_Linux_distributions#apt-rpm_based "wikilink")。も参照。

| 配布版                                            | 説明                                                                    |
| ---------------------------------------------- | --------------------------------------------------------------------- |
| [PCLinuxOS](../Page/PCLinuxOS.md "wikilink")   | Mandriva Linuxを母体に開発。デスクトップ指向。Live CDとしても使用可能。                        |
| [Vine Linux](../Page/Vine_Linux.md "wikilink") | [日本](https://ja.wikipedia.org/wiki/日本 "wikilink")国産のLinuxディストリビューション。 |

### その他RPM系

※[その他RPM系派生版一覧に掲載](https://ja.wikipedia.org/wiki/:en:List_of_Linux_distributions#Independent_RPM_distributions "wikilink")

<table>
<thead>
<tr class="header">
<th><p>配布版</p></th>
<th><p>説明</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><a href="https://ja.wikipedia.org/wiki/Caldera_OpenLinux" title="wikilink">Caldera OpenLinux</a></p></td>
<td><p>商用。Caldera OpenLinux 3.1 から <a href="https://ja.wikipedia.org/wiki/Lycoris_Desktop/LX" title="wikilink">Lycoris Desktop/LX</a> が派生。開発停止。</p></td>
</tr>
<tr class="even">
<td></td>
<td><p>(複数の系列)<a href="https://ja.wikipedia.org/wiki/Red_Hat_Enterprise_Linux派生ディストリビューション" title="wikilink">Red Hat Enterprise Linux派生ディストリビューションも参照</a>。</p></td>
</tr>
<tr class="odd">
<td><p><a href="../Page/Turbolinux.md" title="wikilink">Turbolinux</a></p></td>
<td><p>パッケージ管理システムとして<a href="../Page/RPM_Package_Manager.md" title="wikilink">RPMを使っている</a>。無料Live CD版は2008と12.5の2種類が存在する。日本製。</p></td>
</tr>
</tbody>
</table>

## Slackware系

[SlackwareFamilyTree1210.svg](https://ja.wikipedia.org/wiki/File:SlackwareFamilyTree1210.svg "fig:SlackwareFamilyTree1210.svg") ※[Slackware派生版一覧に掲載されるもの](https://ja.wikipedia.org/wiki/:en:List_of_Linux_distributions#Slackware-based "wikilink")。
*[Slackware\#その他の派生版](https://ja.wikipedia.org/wiki/Slackware#その他の派生版 "wikilink")も参照。*主要なものは以下の通り。

<table>
<thead>
<tr class="header">
<th><p>配布版</p></th>
<th><p>説明</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><a href="../Page/Slackware.md" title="wikilink">Slackware</a></p></td>
<td><p>Linux普及初期は有名だったディストリビューション。</p></td>
</tr>
<tr class="even">
<td><p><a href="https://ja.wikipedia.org/wiki/Absolute_Linux" title="wikilink">Absolute Linux</a></p></td>
<td><p>Slackwareを母体とした<a href="https://ja.wikipedia.org/wiki/軽量Linuxディストリビューション" title="wikilink">軽量Linuxディストリビューション</a>である[19][20]。</p></td>
</tr>
<tr class="odd">
<td><p><a href="https://ja.wikipedia.org/wiki/Salix_OS" title="wikilink">Salix OS</a></p></td>
<td><p>Slackwareとの完全な互換性を保持し、安定性に重点をおいたディストリビューションである。<a href="../Page/Xfce.md" title="wikilink">Xfce</a>, <a href="../Page/KDE.md" title="wikilink">KDE</a>, <a href="https://ja.wikipedia.org/wiki/LXDE" title="wikilink">LXDE</a>, <a href="../Page/Fluxbox.md" title="wikilink">Fluxbox</a> または <a href="https://ja.wikipedia.org/wiki/Ratpoison" title="wikilink">Ratpoison</a> も選択可能。<a href="https://ja.wikipedia.org/wiki/32bit" title="wikilink">32bit</a>と<a href="https://ja.wikipedia.org/wiki/64bit" title="wikilink">64bit</a>、<a href="../Page/Live_CD.md" title="wikilink">Live CD版もある</a>。</p></td>
</tr>
<tr class="even">
<td></td>
<td><p><a href="../Page/PowerPC.md" title="wikilink">PowerPC</a>機向け非公式版 Slackware。</p></td>
</tr>
<tr class="odd">
<td><p><a href="https://ja.wikipedia.org/wiki/Slamd64" title="wikilink">Slamd64</a></p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/x64" title="wikilink">x64</a>版Slackwareである。開発停止。</p></td>
</tr>
<tr class="even">
<td><p><a href="../Page/SLAX.md" title="wikilink">SLAX</a></p></td>
<td><p>Slax 8まではSlackwarを母体とする。<a href="https://ja.wikipedia.org/wiki/モジュール#ソフトウェア" title="wikilink">複数の機能と非常に簡単な</a><a href="../Page/マスタリング.md" title="wikilink">リマスターを持つ</a>。<a href="../Page/Live_CD.md" title="wikilink">Live CD</a>。</p></td>
</tr>
<tr class="odd">
<td></td>
<td><p>ウィンドウマネージャとして<a href="../Page/Xfce.md" title="wikilink">Xfce</a>を採用している[21]。開発停止。</p></td>
</tr>
<tr class="even">
<td></td>
<td><p>Slackwar派生。</p></td>
</tr>
</tbody>
</table>

### Slax派生

※[Slax派生版一覧に掲載されたもの](https://ja.wikipedia.org/wiki/:en:List_of_Linux_distributions#Slax-based "wikilink")。
*[SLAX\#関連ディストリビューション](https://ja.wikipedia.org/wiki/SLAX#関連ディストリビューション "wikilink")も参照。*

<table>
<thead>
<tr class="header">
<th><p>配布版</p></th>
<th><p>説明</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><p>300MB以下[22]。SLAXから派生。</p></td>
</tr>
</tbody>
</table>

### openSUSE派生

※[openSUSE派生版一覧に掲載されるもの](https://ja.wikipedia.org/wiki/:en:List_of_Linux_distributions#openSUSE-based "wikilink")。 設定には[YaST](https://ja.wikipedia.org/wiki/YaST "wikilink")を、パッケージ管理システムは[RPM系を採用](../Page/RPM_Package_Manager.md "wikilink")。
*[openSUSE\#その他の派生版](https://ja.wikipedia.org/wiki/openSUSE#その他の派生版 "wikilink")も参照。*

| 配布版                                                                                                   | 説明                                                                                                                                                                                                          |
| ----------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [openSUSE](https://ja.wikipedia.org/wiki/openSUSE "wikilink")                                         | [ドイツ](https://ja.wikipedia.org/wiki/ドイツ "wikilink")で開発されていたため、[ヨーロッパ](../Page/ヨーロッパ.md "wikilink")で強い。[SUSE](../Page/SUSE.md "wikilink")は[ノベルに買収されたことに伴い](../Page/ノベル_\(企業\).md "wikilink")、SUSE Linuxから改名。 |
| [SUSE Linux Enterprise Desktop](../Page/SUSE_Linux_Enterprise_Desktop.md "wikilink")                  | SUSE Linux Enterprise Serverのデスクトップ版。                                                                                                                                                                       |
| [SUSE Linux Enterprise Server](https://ja.wikipedia.org/wiki/SUSE_Linux_Enterprise_Server "wikilink") | テスト済みのopenSUSEを母体にして安定させた。商用。                                                                                                                                                                               |
| [SUSE Studio](https://ja.wikipedia.org/wiki/SUSE_Studio "wikilink")                                   | openSUSE, SUSE Linux Enterprise Server 用に提供された、[オンラインアプライアンス作成ツール](https://ja.wikipedia.org/wiki/ネットワーク・アプライアンス "wikilink")、サービスである。                                                                        |
|                                                                                                       |                                                                                                                                                                                                             |

## Arch系

※[Pacman系派生版一覧に掲載されるもの](https://ja.wikipedia.org/wiki/:en:List_of_Linux_distributions#Pacman-based "wikilink")。 [パッケージ管理として](../Page/パッケージ管理システム.md "wikilink")[Pacman](https://ja.wikipedia.org/wiki/Pacman "wikilink")を使っている。
*[Arch Linux\#その他の派生版も参照](https://ja.wikipedia.org/wiki/Arch_Linux#その他の派生版 "wikilink")。*主要なものは以下の通り。

<table>
<thead>
<tr class="header">
<th><p>配布版</p></th>
<th><p>説明</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><a href="https://ja.wikipedia.org/wiki/Arch_Linux" title="wikilink">Arch Linux</a></p></td>
<td><p><a href="../Page/パッケージ管理システム.md" title="wikilink">パッケージ管理システム</a>に<a href="https://ja.wikipedia.org/wiki/Pacman" title="wikilink">Pacman</a>を使用。</p></td>
</tr>
<tr class="even">
<td></td>
<td><p>Arch Linuxを母体に、導入媒体および標準のウィンドウマネージャに<a href="https://ja.wikipedia.org/wiki/Openbox" title="wikilink">Openbox</a>を採用したもの[23]。</p></td>
</tr>
<tr class="odd">
<td></td>
<td><p><a href="https://ja.wikipedia.org/wiki/systemd" title="wikilink">systemd</a>の代わりにOpenRC、runitまたはs6 <a href="https://ja.wikipedia.org/wiki/init" title="wikilink">init</a>を使用するArch Linuxに基づくディストリビューション[24]。</p></td>
</tr>
<tr class="even">
<td><p><a href="../Page/BlackArch_Linux.md" title="wikilink">BlackArch Linux</a></p></td>
<td><p>Arch Linuxを母体とした<a href="https://ja.wikipedia.org/wiki/ペネトレーションテスト" title="wikilink">侵入テストを目的としたもの</a>。</p></td>
</tr>
<tr class="odd">
<td></td>
<td><p><a href="../Page/KDE.md" title="wikilink">KDE</a>を<a href="https://ja.wikipedia.org/wiki/モジュール#ソフトウェア" title="wikilink">モジュール化した</a><a href="https://ja.wikipedia.org/wiki/KDEmod" title="wikilink">KDEmod</a>デスクトップ環境を標準とし、<a href="../Page/Qt.md" title="wikilink">Qt</a>母体の<a href="https://ja.wikipedia.org/wiki/グラフィカルユーザインタフェース" title="wikilink">視覚的な</a><a href="https://ja.wikipedia.org/wiki/インストーラ" title="wikilink">導入環境や更新機能</a>、<a href="../Page/パッケージ管理システム.md" title="wikilink">パッケージマネージャ</a>（Pacmanの<a href="../Page/フロントエンド.md" title="wikilink">フロントエンド</a>）などを提供し、Arch Linuxよりも扱いやすいディストリビューションを目標としている。[25]<ref>{{cite</p></td>
</tr>
<tr class="even">
<td></td>
<td><p><a href="https://ja.wikipedia.org/wiki/Antergos" title="wikilink">Antergos</a>の後継ディストリビューション[26]。</p></td>
</tr>
<tr class="odd">
<td><p><a href="https://ja.wikipedia.org/wiki/Manjaro" title="wikilink">Manjaro</a></p></td>
<td><p>Arch Linuxを母体に、標準の<a href="../Page/ウィンドウマネージャ.md" title="wikilink">ウィンドウマネージャ</a>に<a href="../Page/Xfce.md" title="wikilink">Xfce</a>、<a href="../Page/KDE.md" title="wikilink">KDE</a>を採用したもの。<a href="../Page/共同体.md" title="wikilink">コミュニティ版として</a><a href="https://ja.wikipedia.org/wiki/Cinnamon" title="wikilink">Cinnamon</a>、 <a href="https://ja.wikipedia.org/wiki/MATE_(デスクトップ環境)" title="wikilink">MATE</a>、<a href="https://ja.wikipedia.org/wiki/LXDE" title="wikilink">LXDE</a>、<a href="https://ja.wikipedia.org/wiki/Enlightenment" title="wikilink">Enlightenment</a>、<a href="https://ja.wikipedia.org/wiki/OpenBox" title="wikilink">OpenBox</a>が提供されている。</p></td>
</tr>
<tr class="even">
<td><p><a href="https://ja.wikipedia.org/wiki/Parabola_GNU/Linux-libre" title="wikilink">Parabola_GNU/Linux-libre</a></p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/Linux-libre" title="wikilink">Linux-libre</a>カーネルを使用しており、<a href="../Page/フリーソフトウェア.md" title="wikilink">フリーソフトウェア</a>のみで構成されている。</p></td>
</tr>
</tbody>
</table>

## Gentoo系

[GentooFamilyTree1210.svg](https://ja.wikipedia.org/wiki/File:GentooFamilyTree1210.svg "fig:GentooFamilyTree1210.svg") ※[Gentoo Linux派生版一覧に掲載されるもの](https://ja.wikipedia.org/wiki/:en:List_of_Linux_distributions#Gentoo-based "wikilink")。 [パッケージ管理として](../Page/パッケージ管理システム.md "wikilink")[Portage](../Page/Portage.md "wikilink")を使っている。
主要なものは以下の通り。

<table>
<thead>
<tr class="header">
<th><p>配布版</p></th>
<th><p>説明</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><a href="../Page/Gentoo_Linux.md" title="wikilink">Gentoo Linux</a></p></td>
<td><p><a href="../Page/BSDの子孫.md" title="wikilink">BSD系OSのportに似た</a><a href="../Page/Portage.md" title="wikilink">Portage</a>と呼ばれるパッケージ管理システムを採用。</p></td>
</tr>
<tr class="even">
<td><p><a href="https://ja.wikipedia.org/wiki/Google_Chrome_OS" title="wikilink">Chrome OS</a></p></td>
<td><p>Chrome OS[27][28]は、Googleが開発しているOS。2010年2月に、母体となるOSを<a href="https://ja.wikipedia.org/wiki/ubuntu" title="wikilink">ubuntu</a>からGentooに変更した。<a href="https://ja.wikipedia.org/wiki/Chromium_OS" title="wikilink">Chromium OSは</a>、Google Chrome OSの<a href="../Page/オープンソース.md" title="wikilink">オープンソース</a>版。</p></td>
</tr>
<tr class="odd">
<td><p><a href="https://ja.wikipedia.org/wiki/Container_Linux" title="wikilink">Container Linux</a></p></td>
<td><p>旧称は、<a href="https://ja.wikipedia.org/wiki/CoreOS" title="wikilink">CoreOS</a> Linux。軽量なOSである。</p></td>
</tr>
<tr class="even">
<td><p><a href="https://ja.wikipedia.org/wiki/Sabayon_Linux" title="wikilink">Sabayon Linux</a></p></td>
<td><p>Gentoo Linuxの派生GNU/Linux。Gentooの特徴である<a href="https://ja.wikipedia.org/wiki/機能拡張" title="wikilink">機能拡張</a>はなりを潜めているが、様々な<a href="https://ja.wikipedia.org/wiki/アプリケーション" title="wikilink">アプリケーション</a>が同梱されているライブDVD。</p></td>
</tr>
<tr class="odd">
<td></td>
<td><p>WindowsとLinux修理用のツールをまとめた Linux 2.6 <a href="../Page/カーネル.md" title="wikilink">カーネル</a>母体の<a href="../Page/Live_CD.md" title="wikilink">Live CD</a>。</p></td>
</tr>
</tbody>
</table>

## ソース系

※[ソース系一覧に掲載されるもの](https://ja.wikipedia.org/wiki/:en:List_of_Linux_distributions#source-based "wikilink")。

| 配布版                                                                               | 説明                                                                                                                                                                                                                                                                                                                                |
| --------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [Linux From Scratch](https://ja.wikipedia.org/wiki/Linux_From_Scratch "wikilink") | A distribution and book on how to build GNU/Linux from its [source code](../Page/ソースコード.md "wikilink") along with bootstrapping the GNU-tool-chain's sources.                                                                                                                                                                     |
| [Guix System](../Page/GNU_Guix.md "wikilink")                                     | A distribution built around the [GNU Guix](../Page/GNU_Guix.md "wikilink") package manager, which provides [purely functional](https://ja.wikipedia.org/wiki/:en:Pure_function "wikilink") package management with build automation, build isolation, easy system upgrades and rollbacks, and an emphasis on free software.\[29\] |

## 独立系

※[独立系一覧に掲載されるもの](https://ja.wikipedia.org/wiki/:en:List_of_Linux_distributions#Independent "wikilink")。主要なものは以下の通り。

<table>
<thead>
<tr class="header">
<th><p>配布版</p></th>
<th><p>説明</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><a href="https://ja.wikipedia.org/wiki/Alpine_Linux" title="wikilink">Alpine Linux</a></p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/musl" title="wikilink">musl</a>と<a href="https://ja.wikipedia.org/wiki/BusyBox" title="wikilink">BusyBox</a>を含むセキュリティ面を重視したOS。派生版は、携帯端末向けの<a href="https://ja.wikipedia.org/wiki/postmarketOS" title="wikilink">postmarketOS</a>である。</p></td>
</tr>
<tr class="even">
<td><p><a href="../Page/Android_(オペレーティングシステム).md" title="wikilink">Android</a></p></td>
<td><p>Android は <a href="../Page/Google.md" title="wikilink">Google</a> が開発した<a href="https://ja.wikipedia.org/wiki/モバイル端末" title="wikilink">モバイル端末</a>向けOS。x86(64)版は、androidをpc上で動かすためのLive CD。64bit cpuのための物はx64と呼ばれる[30]。</p></td>
</tr>
<tr class="odd">
<td><p><a href="https://ja.wikipedia.org/wiki/CyanogenMod" title="wikilink">CyanogenMod</a>/<a href="https://ja.wikipedia.org/wiki/CyanogenMod" title="wikilink">CyanogenOS</a></p></td>
<td><p>CyanogenMod は開発終了した携帯端末向け OS。<a href="../Page/Android_(オペレーティングシステム).md" title="wikilink">Androidから派生</a>。</p></td>
</tr>
<tr class="even">
<td><p><a href="https://ja.wikipedia.org/wiki/DD-WRT" title="wikilink">DD-WRT</a></p></td>
<td><p><a href="../Page/ファイアウォール.md" title="wikilink">ファイアウォール</a>向けの組込み用ディストリビューション。</p></td>
</tr>
<tr class="odd">
<td><p><a href="https://ja.wikipedia.org/wiki/Dragora_GNU/Linux-Libre" title="wikilink">Dragora GNU/Linux-Libre</a></p></td>
<td><p><a href="../Page/Slackware.md" title="wikilink">Slackware</a>から派生した完全にフリーソフトウェアのみで構成される独自のGNU/Linuxディストリビューション。簡素であることを構想している[31][32]。</p></td>
</tr>
<tr class="even">
<td><p><a href="https://ja.wikipedia.org/wiki/Familiar_Linux" title="wikilink">Familiar Linux</a></p></td>
<td><p>iPAQ handheld 向けの配布版。</p></td>
</tr>
<tr class="odd">
<td><p><a href="https://ja.wikipedia.org/wiki/Fire_OS" title="wikilink">Fire OS</a></p></td>
<td><p>Amazon Fire OS is an <a href="../Page/Android_(オペレーティングシステム).md" title="wikilink">Android</a>-based mobile operating system produced by <a href="../Page/Amazon.com.md" title="wikilink">Amazon</a> for its Fire Phone and Kindle Fire range of tablets, Echo and Echo Dot, and other content delivery devices like Fire TV; the tablet versions of the Kindle e-readers are the Fire range.</p></td>
</tr>
<tr class="even">
<td><p><a href="https://ja.wikipedia.org/wiki/Firefox_OS" title="wikilink">Firefox OS</a></p></td>
<td><p>Firefox OS is a discontinued open-source operating system – made for smartphones, tablet computers and smart TVs – designed by <a href="../Page/Mozilla_Corporation.md" title="wikilink">Mozilla</a> and external contributors.</p></td>
</tr>
<tr class="odd">
<td><p><a href="../Page/Foresight_Linux.md" title="wikilink">Foresight Linux</a></p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/Conary" title="wikilink">Conary</a>と呼ばれる次世代パッケージ管理システムを採用。開発停止。</p></td>
</tr>
<tr class="even">
<td><p><a href="../Page/GNU_Guix.md" title="wikilink">Guix System Distribution</a> (Guix System)</p></td>
<td><p>Declarative Linux distribution with atomic upgrades and rollbacks built on top of the <a href="../Page/GNU_Guix.md" title="wikilink">GNU Guix</a> package manager. Supports amongst others unprivileged package management and per-user profiles.</p></td>
</tr>
<tr class="odd">
<td><p><a href="https://ja.wikipedia.org/wiki/GoboLinux" title="wikilink">GoboLinux</a></p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/Filesystem_Hierarchy_Standard" title="wikilink">Filesystem Hierarchy Standardからの脱却を目指したLinux</a>。</p></td>
</tr>
<tr class="even">
<td><p><a href="https://ja.wikipedia.org/wiki/Jlime" title="wikilink">Jlime</a></p></td>
<td><p><a href="../Page/携帯情報端末.md" title="wikilink">携帯情報端末</a>、<a href="https://ja.wikipedia.org/wiki/Hewlett-Packard" title="wikilink">HP</a> <a href="https://ja.wikipedia.org/wiki/:en:Jornada_(PDA)" title="wikilink">Jornada</a> 6xx and 7xx と <a href="https://ja.wikipedia.org/wiki/NEC" title="wikilink">NEC</a> <a href="https://ja.wikipedia.org/wiki/:en:MobilePro#MobilePro_900" title="wikilink">MobilePro 900(c)</a> 用の Linux ディストリビューション。</p></td>
</tr>
<tr class="odd">
<td><p><a href="https://ja.wikipedia.org/wiki/KaiOS" title="wikilink">KaiOS</a></p></td>
<td><p><a href="../Page/Linux.md" title="wikilink">Linux</a>を母体とする携帯機器向けOS。<a href="https://ja.wikipedia.org/wiki/KaiOS_Technologies" title="wikilink">KaiOS Technologiesが開発した</a>。</p></td>
</tr>
<tr class="even">
<td><p><a href="https://ja.wikipedia.org/wiki/LineageOS" title="wikilink">LineageOS</a></p></td>
<td><p><a href="../Page/Android_(オペレーティングシステム).md" title="wikilink">Android</a> が動作する <a href="https://ja.wikipedia.org/wiki/Smartphone" title="wikilink">smartphones</a>、 <a href="../Page/タブレット_(コンピュータ).md" title="wikilink">tablet computers</a>、そして<a href="../Page/セットトップボックス.md" title="wikilink">set-top boxes</a> 向けの <a href="../Page/FLOSS.md" title="wikilink">free and open-source</a> <a href="https://ja.wikipedia.org/wiki/operating_system" title="wikilink">operating system</a>。</p></td>
</tr>
<tr class="odd">
<td><p><a href="https://ja.wikipedia.org/wiki/MeeGo" title="wikilink">MeeGo</a></p></td>
<td><p>MeeGo is a discontinued Linux distribution hosted by <a href="../Page/Linux_Foundation.md" title="wikilink">the Linux Foundation</a>, using source code from the operating systems Moblin (produced by <a href="https://ja.wikipedia.org/wiki/Intel" title="wikilink">Intel</a>) and Maemo (produced by <a href="https://ja.wikipedia.org/wiki/Nokia" title="wikilink">Nokia</a>).</p></td>
</tr>
<tr class="even">
<td><p><a href="https://ja.wikipedia.org/wiki/MkLinux" title="wikilink">MkLinux</a></p></td>
<td><p><a href="../Page/PowerPC.md" title="wikilink">PowerPC</a>搭載機専用、<a href="../Page/Mach.md" title="wikilink">Mach</a>を母体とする。開発停止。</p></td>
</tr>
<tr class="odd">
<td><p><a href="https://ja.wikipedia.org/wiki/OpenWrt" title="wikilink">OpenWrt</a></p></td>
<td><p>A router and firewall Linux distribution, also other <a href="../Page/組み込みシステム.md" title="wikilink">embedded systems</a>, a lot of routing options via <a href="https://ja.wikipedia.org/wiki/:en:opkg" title="wikilink">opkg</a> available</p></td>
</tr>
<tr class="even">
<td><p><a href="../Page/PS2_Linux.md" title="wikilink">PS2 Linux</a></p></td>
<td><p><a href="../Page/PlayStation_2.md" title="wikilink">PlayStation 2上で動作する</a>。<a href="https://ja.wikipedia.org/wiki/Kondara_MNU/Linux" title="wikilink">Kondara MNU/Linux派生</a>。</p></td>
</tr>
<tr class="odd">
<td><p><a href="../Page/Puppy_Linux.md" title="wikilink">Puppy Linux</a></p></td>
<td><p>50-90MB前後の軽量Live CD。他のほとんどのLinuxディストリビューションと比較して軽量[33]で、CDやDVD自身へのデータ書き戻しやHDへの導入、日本語化も可能[34][35]。debパッケージ利用にも対応している。派生版は<a href="https://ja.wikipedia.org/wiki/#Puppy_Linux派生" title="wikilink">#Puppy Linux派生を参照</a>。</p></td>
</tr>
<tr class="even">
<td><p><a href="../Page/Replicant_(オペレーティングシステム).md" title="wikilink">Replicant</a></p></td>
<td><p>Replicant is a free operating system (OS) based on the <a href="../Page/Android_(オペレーティングシステム).md" title="wikilink">Android</a> mobile platform that aims to replace all proprietary Android components with free-software counterparts.</p></td>
</tr>
<tr class="odd">
<td></td>
<td><p>Androidランタイムを含む <a href="https://ja.wikipedia.org/wiki/ヨーラ" title="wikilink">JollaによるLinux系のモバイルOS</a>。.</p></td>
</tr>
<tr class="even">
<td><p><a href="https://ja.wikipedia.org/wiki/Slitaz" title="wikilink">SliTaz</a></p></td>
<td><p>Damn Small Linuxと共通する目的を多く共有するが、より最新の Linux 2.6 カーネルに基づき、より小さい[36]。派生版は<a href="https://ja.wikipedia.org/wiki/#SliTaz派生" title="wikilink">#SliTaz派生</a>を参照。</p></td>
</tr>
<tr class="odd">
<td></td>
<td><p><a href="../Page/ルーター.md" title="wikilink">ルーター</a>と<a href="../Page/ファイアウォール.md" title="wikilink">ファイアウォール</a>のディストリビューション。</p></td>
</tr>
<tr class="even">
<td><p><a href="https://ja.wikipedia.org/wiki/SLS" title="wikilink">Softlanding Linux System</a></p></td>
<td><p>GNU/Linuxで最も初期のディストリビューション。開発停止。</p></td>
</tr>
<tr class="odd">
<td><p><a href="https://ja.wikipedia.org/wiki/Solus" title="wikilink">Solus</a></p></td>
<td><p>Desktop Linux distribution offering Budgie, GNOME and MATE desktop environments, eopkg for package management.</p></td>
</tr>
<tr class="even">
<td><p><a href="https://ja.wikipedia.org/wiki/SHR_(オペレーティングシステム)" title="wikilink">Stable Hybrid Release</a></p></td>
<td><p>For smartphones, offering <a href="https://ja.wikipedia.org/wiki/Enlightenment_(window_manager)" title="wikilink">Enlightenment</a>'s Illume user interface. It is based on FSO.</p></td>
</tr>
<tr class="odd">
<td><p><a href="https://ja.wikipedia.org/wiki/Tiny_Core_Linux" title="wikilink">Tiny Core Linux</a></p></td>
<td><p><a href="../Page/Damn_Small_Linux.md" title="wikilink">Damn Small Linuxの開発者の</a>1人であったRobert Shingledeckerが中心となって開発が進められている。GUIを装備していながら容量が10MB程度しかないことが特徴。Live CD</p></td>
</tr>
<tr class="even">
<td><p><a href="https://ja.wikipedia.org/wiki/Tizen" title="wikilink">Tizen</a></p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/オプション#選択肢" title="wikilink">選択可能なandroid</a><a href="../Page/ランタイムライブラリ.md" title="wikilink">ランタイムを備えたLinux系のOS</a>。</p></td>
</tr>
<tr class="odd">
<td></td>
<td><p>Linuxディストリビューション初の<a href="../Page/Live_CD.md" title="wikilink">Live CD</a> 1992.8-1995。開発停止。</p></td>
</tr>
</tbody>
</table>

### その他独立系

  - \[37\] - [Intel 386と](../Page/Intel_80386.md "wikilink")3MBのRAM容量で動作する非常に軽量なディストリビューション\[38\]\[39\]。

  - [Minimal Linux Live](http://minimal.linux-bg.org/)\[40\]

#### Puppy Linux派生

  - [Lxpup](https://ja.wikipedia.org/wiki/Lxpup "wikilink")\[41\]\[42\] - Puppy Linuxを基盤に、デスクトップ環境をLXDEに置き換えたもの。
  - [Yara OSX](https://ja.wikipedia.org/wiki/Yara_OSX "wikilink")\[43\]\[44\] - Puppy Linux派生。Xfceを採用したMacOS風の画面。

#### SliTaz派生

  - [Ophcrack](https://ja.wikipedia.org/wiki/Ophcrack "wikilink") - Windowsパスワード解析用。元はSLAXを母体としたが、ver3.3.0以降は[SliTaz GNU/Linux](https://ja.wikipedia.org/wiki/Slitaz "wikilink") 派生。
  - [Tiny SliTaz](https://ja.wikipedia.org/wiki/Tiny_SliTaz "wikilink") - SliTazの派生で、[uClibc](https://ja.wikipedia.org/wiki/uClibc "wikilink")を使用し、[フロッピーディスク](../Page/フロッピーディスク.md "wikilink")からの起動が可能。

#### 開発停止

  - [iPodLinux](https://ja.wikipedia.org/wiki/iPodLinux "wikilink") - [iPod](https://ja.wikipedia.org/wiki/iPod "wikilink")用に[µClinux](https://ja.wikipedia.org/wiki/µClinux "wikilink")をカーネルとしたもの。
  - [IPnuts](../Page/IPnuts.md "wikilink") - ルータ・ファイアウォール構築に使用。
  - [Nature's Linux](http://www.n-linux.com/)\[45\] - 無料の開発版とOS監視サポート付きの有料版がある。FreeBSDのjailに似た仮想ファイルシステム、jailを利用したバックアップとリカバリ機能、ファイル改竄検出機能などを持つ。
  - [Stataboware](https://ja.wikipedia.org/wiki/Stataboware "wikilink") - Slackwareに似た構造で、[Alpha搭載機専用](https://ja.wikipedia.org/wiki/DEC_Alpha "wikilink")。
  - [Splashtop](https://ja.wikipedia.org/wiki/Splashtop "wikilink") - 起動速度を重視して開発されたOS。

## 日本発のディストリビューション

*[日本のLinux開発](https://ja.wikipedia.org/wiki/日本のLinux開発 "wikilink")も参照。*

  - [Debian\#日本発の派生版](https://ja.wikipedia.org/wiki/Debian#日本発の派生版 "wikilink")
  - [Ubuntu\#日本発の派生品](https://ja.wikipedia.org/wiki/Ubuntu#日本発の派生品 "wikilink")
  - [KNOPPIX\#日本発の派生版](https://ja.wikipedia.org/wiki/KNOPPIX#日本発の派生版 "wikilink")
  - [Red Hat Linux\#日本発の派生版](https://ja.wikipedia.org/wiki/Red_Hat_Linux#日本発の派生版 "wikilink")
  - [Slackware\#日本発の派生版](https://ja.wikipedia.org/wiki/Slackware#日本発の派生版 "wikilink")

## 脚注

<references />

## 関連項目

  - [ディストリビューション](https://ja.wikipedia.org/wiki/ディストリビューション "wikilink")
  - [派生](../Page/フォーク_\(ソフトウェア開発\).md "wikilink")
  - [インタフェース](https://ja.wikipedia.org/wiki/インタフェース "wikilink")
  - [GNU/Linuxシステム](https://ja.wikipedia.org/wiki/GNU/Linuxシステム "wikilink")
  - [Linux](../Page/Linux.md "wikilink")
  - [軽量Linuxディストリビューション](https://ja.wikipedia.org/wiki/軽量Linuxディストリビューション "wikilink")
  - [Linuxディストリビューションの比較](../Page/Linuxディストリビューションの比較.md "wikilink")
  - [Linuxライブディストリビューションの比較](../Page/Linuxライブディストリビューションの比較.md "wikilink")
  - [組み込みLinux](../Page/組み込みLinux.md "wikilink")
  - [Linux Standard Base](../Page/Linux_Standard_Base.md "wikilink")
  - [Linux from Scratch](../Page/Linux_from_Scratch.md "wikilink") : 一から環境を構築する手法
  - [DistroWatch](https://ja.wikipedia.org/wiki/DistroWatch "wikilink")

## 外部リンク

[DistroWatch.com](https://distrowatch.com/) - GNU/Linux及び[FreeBSDディストリビューション](../Page/FreeBSDディストリビューション.md "wikilink")の情報サイト

[Category:Linuxディストリビューション](https://ja.wikipedia.org/wiki/Category:Linuxディストリビューション "wikilink") [Category:Linux](https://ja.wikipedia.org/wiki/Category:Linux "wikilink")

1.  例えば[Ubuntu](http://www.ubuntulinux.jp/download/ja-remix)など。
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
15. [Vyatta website](http://www.vyatta.org/)
16.
17.
18.
19. [Linuxレビュー：Absolute Linuxは“絶対買い”なディストリビューションか？](http://sourceforge.jp/magazine/07/08/10/006247)
20.
21.
22.
23. [ArchBang](http://archbang.org/)
24. [Artix Linux](https://artixlinux.org/)
25. [Chakra](http://chakraos.org)
26. [EndeavourOS](https://endeavouros.com/)
27.
28.
29.
30.  ZDNet|last=Vaughan-Nichols|first=Steven J.|work=ZDNet|access-date=2017-11-24|language=en|archive-url=[https://web.archive.org/web/20171108102316/http://www.zdnet.com/article/debunking-four-myths-about-android-google-and-open-source/|archive-date=2017-11-08|url-status=live](https://web.archive.org/web/20171108102316/http://www.zdnet.com/article/debunking-four-myths-about-android-google-and-open-source/%7Carchive-date=2017-11-08%7Curl-status=live)}}
31. Bruce Byfield: [Eight Completely Free Linux Distros (And One More)](http://itmanagement.earthweb.com/osrc/article.php/3922031/Eight-Completely-Free-Linux-Distros-And-One-More.htm)  earthweb.com, 2011.
32.
33.
34. [日本語サポートパッケージ - sakurapup.browserloadofcoolness.com](http://sakurapup.browserloadofcoolness.com/viewtopic.php?t=1937)
35. [日本語化ファイル入手先](http://shinobar.server-on.net/puppy/opt/)
36.
37. [BasicLinux – Freecode](http://freshmeat.sourceforge.net/projects/baslinux)
38.
39.
40. [Minimal Linux Live DistroWatch](https://distrowatch.com/table.php?distribution=mll)
41. [LxPup - Puppy Linux + LXDE](https://sourceforge.net/projects/lxpup/)
42. [LxPup - Puppy Linux + LXDE 日本語情報トップページ - OSDN](https://ja.osdn.net/projects/sfnet_lxpup/)
43. [Yara OSX - Home](https://yara-osx.weebly.com/)
44. [Puppy Linux Discussion Forum :: View topic - Yara OSX 3](http://www.murga-linux.com/puppy/viewtopic.php?t=107173)
45. [Nature's Linux DistroWatch](https://distrowatch.com/table.php?distribution=natures)
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

[Screenshot-debian_wheezy_ja.png](https://ja.wikipedia.org/wiki/File:Screenshot-debian_wheezy_ja.png "fig:Screenshot-debian_wheezy_ja.png") [Screenshot_of_Ubuntu_15.10_Desktop_live_CD.png](https://ja.wikipedia.org/wiki/File:Screenshot_of_Ubuntu_15.10_Desktop_live_CD.png "fig:Screenshot_of_Ubuntu_15.10_Desktop_live_CD.png") [Kubuntu-13.10-Saucy-Salamander.png](https://ja.wikipedia.org/wiki/File:Kubuntu-13.10-Saucy-Salamander.png "fig:Kubuntu-13.10-Saucy-Salamander.png") [Xubuntu_14.04_LTS.png](https://ja.wikipedia.org/wiki/File:Xubuntu_14.04_LTS.png "fig:Xubuntu_14.04_LTS.png") パッケージ管理システムに[deb](https://ja.wikipedia.org/wiki/deb "wikilink")形式を使っている。主要なものは以下の通り。

  - [Debian GNU/Linux](../Page/Debian.md "wikilink") : 100%[フリーソフトウェア](../Page/フリーソフトウェア.md "wikilink")であることが理念、コミュニティベース。
      - [ARMA aka Omoikane GNU/Linux](https://ja.wikipedia.org/wiki/ARMA_aka_Omoikane_GNU/Linux "wikilink") : [ファイルシステム](../Page/ファイルシステム.md "wikilink")に[XFS](../Page/XFS.md "wikilink")を採用している。

      - \[2\]:[ロシアの政府機関における](https://ja.wikipedia.org/wiki/ロシア連邦 "wikilink")[正式のOSのひとつ](https://ja.wikipedia.org/wiki/:ru:Astra_Linux "wikilink")。

      - [Clonezilla](https://ja.wikipedia.org/wiki/Clonezilla "wikilink") - [ディスクまたは](../Page/補助記憶装置.md "wikilink")[パーティション](../Page/パーティション.md "wikilink")の複製（クローニング）ならびに[イメージ作成](../Page/ディスクドライブ仮想化ソフト.md "wikilink")（イメージング）用。

      - [gNewSense](https://ja.wikipedia.org/wiki/gNewSense "wikilink") : [GNU FSDGに適合し](https://ja.wikipedia.org/wiki/GNUプロジェクト#GNU_FSDG "wikilink")、[フリーソフトウェア財団](../Page/フリーソフトウェア財団.md "wikilink")の支援を受ける。[Linux-libre](https://ja.wikipedia.org/wiki/Linux-libre "wikilink")を使用し、ファームウェアのレベルまで100%自由ソフトで構成される。

      - [Kali Linux](https://ja.wikipedia.org/wiki/Kali_Linux "wikilink") : Debianベースの1DVDタイプ。[ペネトレーションテスト](https://ja.wikipedia.org/wiki/ペネトレーションテスト "wikilink")目的に特化していることが特徴。[BackTrack](https://ja.wikipedia.org/wiki/BackTrack "wikilink")から[派生](../Page/フォーク_\(ソフトウェア開発\).md "wikilink")。

      - : DebianベースでCDブート/HDDインストール共可能。

      - [KNOPPIX](../Page/KNOPPIX.md "wikilink") : DebianをベースにCDブートで利用できるようにしている。

      - [MX Linux](../Page/MX_Linux.md "wikilink") : Debianをベースとした中量級のディストリビューション。

      - [OpenMediaVault](https://ja.wikipedia.org/wiki/OpenMediaVault "wikilink") - [NAS向け](../Page/ネットワークアタッチトストレージ.md "wikilink")[サーバ](../Page/サーバ.md "wikilink")OS。

      - [PureOS](../Page/PureOS.md "wikilink") : 完全に自由ソフトウェアだけで構成されている、プライバシーとセキュリティ、利便性に重点を置いているGNU/Linuxディストリビューション。

      - [Raspbian](https://ja.wikipedia.org/wiki/Raspbian "wikilink")：[Raspberry Pi用のdebian](https://ja.wikipedia.org/wiki/Raspberry_Pi "wikilink")。特定の機種用としての配布は、装置が固定しているため使いやすい。Idとパスワードの初期設定が好ましくない。ネットワークに接続する前にrootとID:piのパスワード設定をする必要がある。

      - [SLAX](../Page/SLAX.md "wikilink") : CDブートで利用できるようにしている。9.xより前のバージョンではSlackwareをベースにしていた。日本語化された\[<http://hatochan.dyndns.org/slax-ja/index.php>? SLAX-ja\]も存在する。

      - [SteamOS](https://ja.wikipedia.org/wiki/SteamOS "wikilink") : ゲーム配信サービス[Steam](../Page/Steam.md "wikilink")の運営元が開発した[ゲーミングPC用OS](../Page/ゲームパソコン.md "wikilink")。

      - [Tails](https://ja.wikipedia.org/wiki/Tails_\(オペレーティングシステム\) "wikilink") : Debianベースでプライバシーと匿名性に特化している。[Live CD](../Page/Live_CD.md "wikilink")・[Live USBに対応している](https://ja.wikipedia.org/wiki/Live_USB "wikilink")。

      - [Ubuntu](../Page/Ubuntu.md "wikilink") : 6ヶ月ごとのリリースと商用サポートを掲げる。デスクトップ環境として[GNOME](../Page/GNOME.md "wikilink")を採用している。

          - [Bodhi Linux](../Page/Bodhi_Linux.md "wikilink") : [Enlightenment](https://ja.wikipedia.org/wiki/Enlightenment "wikilink")から派生したウィンドウマネージャ、Mokshaを採用した軽量版。

          - [Edubuntu](../Page/Edubuntu.md "wikilink") : 教育用にカスタマイズされている。

          - [Elbuntu](https://ja.wikipedia.org/wiki/Elbuntu "wikilink") : [ウィンドウマネージャ](../Page/ウィンドウマネージャ.md "wikilink")として[Enlightenment](https://ja.wikipedia.org/wiki/Enlightenment "wikilink")を採用している。

          - [elementary OS](https://ja.wikipedia.org/wiki/elementary_OS "wikilink")\[3\] : 独自のデスクトップ環境「Pantheon」を採用した[MacOS](../Page/MacOS.md "wikilink")風の画面。

          - : [フリーソフトウェア](../Page/フリーソフトウェア.md "wikilink")のみを利用している。

          - [Goobuntu](../Page/Goobuntu.md "wikilink")\[4\]\[5\] : [Google](../Page/Google.md "wikilink")が社内で開発・利用しているとされている。非公開。

          - [Kubuntu](../Page/Kubuntu.md "wikilink") : デスクトップ環境として[KDE](../Page/KDE.md "wikilink")を採用している。

          - [linuxBean](https://ja.wikipedia.org/wiki/linuxBean "wikilink") : 軽量ながらも初心者向けのディストリビューション。

          - [Linux Mint](../Page/Linux_Mint.md "wikilink") : [MATEや](https://ja.wikipedia.org/wiki/MATE_\(デスクトップ環境\) "wikilink")[Cinnamon](https://ja.wikipedia.org/wiki/Cinnamon "wikilink")の採用でデザインやソフトウェア環境を改善し、[マルチメディア](../Page/マルチメディア.md "wikilink")関係の[コーデック](../Page/コーデック.md "wikilink")を充実させている。

              - [Peppermint](https://ja.wikipedia.org/wiki/Peppermint "wikilink") : [Chromium](https://ja.wikipedia.org/wiki/Chromium "wikilink")を搭載している[軽量のディストリビューション](https://ja.wikipedia.org/wiki/軽量Linuxディストリビューション "wikilink")。[Webアプリとの連携も強い](https://ja.wikipedia.org/wiki/ウェブアプリケーション "wikilink")。

          - \- Ubuntu LTS（長期サポート版）を基に開発。Xfce採用でアイコンや壁紙が美しい。アプリの追加や削除、[WEBブラウザの](../Page/ウェブブラウザ.md "wikilink")[キャッシュの削除なども容易](../Page/キャッシュ_\(コンピュータシステム\).md "wikilink")。

          - [Lubuntu](https://ja.wikipedia.org/wiki/Lubuntu "wikilink") : デスクトップ環境として[LXDE](https://ja.wikipedia.org/wiki/LXDE "wikilink")を採用している。

          - : セキュリティツールを多数含んでいる。

          - [Pear Linux](https://ja.wikipedia.org/wiki/Pear_Linux "wikilink")\[6\] : macOS風に構成されたディストリビューション。

          - [Trisquel GNU/Linux](https://ja.wikipedia.org/wiki/Trisquel_GNU/Linux "wikilink") : GNU FSDGに適合し、フリーソフトウェア財団のサーバーで使用される。ファームウェアのレベルまで100%自由ソフトで構成される。

          - [Ubuntu Christian Edition](https://ja.wikipedia.org/wiki/Ubuntu_Christian_Edition "wikilink") : 聖書全文とURLフィルタリングを搭載している。

          - [Ubuntu Lite](https://ja.wikipedia.org/wiki/Ubuntu_Lite "wikilink") : [レガシーデバイス](../Page/レガシーデバイス.md "wikilink")を備えた古いコンピュータ用。

          - [Ubuntu Studio](../Page/Ubuntu_Studio.md "wikilink") : ハイエンドデスクトップ向け。デジタルコンテンツ制作ツールが多数プリインストールされている。[リアルタイムカーネルのパッチも当てられている](../Page/リアルタイムオペレーティングシステム.md "wikilink")。

          - [Xubuntu](https://ja.wikipedia.org/wiki/Xubuntu "wikilink") : デスクトップ環境として[Xfce](../Page/Xfce.md "wikilink")を採用している。

              - [ChaletOS](https://ja.wikipedia.org/wiki/ChaletOS "wikilink")\[7\]\[8\]\[9\] : [Windows](https://ja.wikipedia.org/wiki/Windows "wikilink")に似た[操作性で](../Page/ユーザインタフェース.md "wikilink")、Windowsアプリを動かす[Wine](../Page/Wine.md "wikilink")も標準搭載。Xubuntuから派生。
              - [Voyager](https://ja.wikipedia.org/wiki/Voyager_\(オペレーティングシステム\) "wikilink")\[10\]\[11\]\[12\] : Xubuntuから派生した[フランス](https://ja.wikipedia.org/wiki/フランス "wikilink")産のOS。Xfce採用であるが、MacOS風の画面が美しい。[32bit版と](../Page/32ビット.md "wikilink")[64bit版がある](https://ja.wikipedia.org/wiki/64ビット "wikilink")。

          - [Zorin OS](https://ja.wikipedia.org/wiki/Zorin_OS "wikilink") : Windows風の操作性を提供するディストリビューション。[Wine](../Page/Wine.md "wikilink")を追加するとWindowsアプリも動作する。

          - [zUbuntu](https://ja.wikipedia.org/wiki/zUbuntu "wikilink") : [IBM eServer zSeries](../Page/System_z.md "wikilink")[メインフレーム](../Page/メインフレーム.md "wikilink")用。

      - [WLinux](https://ja.wikipedia.org/wiki/WLinux "wikilink")\[13\]\[14\]

### 開発停止

  - [aptosid](https://ja.wikipedia.org/wiki/aptosid "wikilink") : Debian sidベースでCDブート/HDDインストール共可能。旧称はsidux。

  - [BackTrack](https://ja.wikipedia.org/wiki/BackTrack "wikilink") : Debianベースであり、[Kali Linuxの前身](https://ja.wikipedia.org/wiki/Kali_Linux "wikilink")。ペネトレーションテスト目的に特化していることが特徴だった。

  - [CrunchBang Linux](https://ja.wikipedia.org/wiki/CrunchBang_Linux "wikilink") : ウィンドウマネージャとして[Openbox](https://ja.wikipedia.org/wiki/Openbox "wikilink")を採用している軽量ディストリビューション。

  -   - [Xandros](../Page/Xandros.md "wikilink") : Corel Linuxの後継。[Eee PCに搭載されていた](../Page/Eee_PC.md "wikilink")。

  - [Ecolinux](../Page/Ecolinux.md "wikilink") : デスクトップ環境として[Xfce](../Page/Xfce.md "wikilink")を採用した日本発のディストリビューション。

  - : [Linspire](../Page/Linspire.md "wikilink")の無料版。CDブート/HDDインストール共可能。

  - [gOS](https://ja.wikipedia.org/wiki/gOS "wikilink") : Googleが提供するWebアプリケーションを活用できるように設定されている。

  - [Damn Small Linux](../Page/Damn_Small_Linux.md "wikilink") : KNOPPIXベース、軽量。

  - [Xenoppix](../Page/KNOPPIX.md "wikilink") : KNOPPIXに[Xenを搭載した日本のディストリビューション](../Page/Xen_\(仮想化ソフトウェア\).md "wikilink")。

  - [Regret](https://ja.wikipedia.org/wiki/Regret_\(Linuxディストリビューション\) "wikilink") : KNOPPIXベースの日本のディストリビューション。

  - [Linspire](../Page/Linspire.md "wikilink") : [Windowsのような使い勝手を実現](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")。旧称はLindows。

  - [MEPIS](../Page/MEPIS.md "wikilink") : 主にデスクトップ向け。CDブート/HDDインストール共可能。

  - [Progeny Debian](../Page/Progeny_Debian.md "wikilink") : Red HatのAnacondaインストーラを移植したGNU/Linux。

  - [Fluxbuntu](../Page/Fluxbuntu.md "wikilink") : Ubuntuベース。ウィンドウマネージャとして[Fluxbox](../Page/Fluxbox.md "wikilink")を採用している。

  - [UserLinux](../Page/UserLinux.md "wikilink") : Debianベースの企業向けデスクトップ用GNU/Linux。

  - 巫女 GNYO/Linux : [openMosix](https://ja.wikipedia.org/wiki/openMosix "wikilink")と[SCore](https://ja.wikipedia.org/wiki/SCore "wikilink")を利用したPCクラスタが構築可能。CDブート/HDDインストール共可能。

## Red Hat系

[Vine61_desktop.png](https://ja.wikipedia.org/wiki/File:Vine61_desktop.png "fig:Vine61_desktop.png") パッケージ管理システムとして[RPMを使っている](../Page/RPM_Package_Manager.md "wikilink")。主要なものは以下の通り。

  - [Fedora](../Page/Fedora.md "wikilink") : [Red Hat Linux](../Page/Red_Hat_Linux.md "wikilink") 後継のコミュニティによる実験要素が強い。
      - [Red Hat Enterprise Linux](../Page/Red_Hat_Enterprise_Linux.md "wikilink") : コミュニティによるテスト済みのFedoraをベースにして安定させた。商用。
          - [Asianux](../Page/Asianux.md "wikilink") : アジア5ヵ国の企業が共同開発。Red Hat Enterprise Linuxベース。
          - [CentOS](../Page/CentOS.md "wikilink") : Red Hat Enterprise Linuxのクローン。
          - [Scientific Linux](../Page/Scientific_Linux.md "wikilink")（旧 Fermi Linux） : Red Hat Enterprise Linuxのクローン。
      - [Berry Linux](https://ja.wikipedia.org/wiki/Berry_Linux "wikilink") : 日本人の中田裕一朗が[Fedora](../Page/Fedora.md "wikilink")をベースに開発。
  - [Mageia](https://ja.wikipedia.org/wiki/Mageia "wikilink") : [Mandriva Linuxをベースに開発](../Page/Mandriva_Linux.md "wikilink")。オープンソース。
  - [PCLinuxOS](../Page/PCLinuxOS.md "wikilink") : Mandriva Linuxをベースに開発。デスクトップ指向。
  - [Vine Linux](../Page/Vine_Linux.md "wikilink") : 日本国産のLinuxディストリビューション。
  - [RedHawk Linux](https://ja.wikipedia.org/wiki/RedHawk_Linux "wikilink") : [RHELのカーネルをリアルタイムLinuxカーネルに置き換えた](../Page/Red_Hat_Enterprise_Linux.md "wikilink")。商用。
  - [Oracle Linux](https://ja.wikipedia.org/wiki/Oracle_Linux "wikilink"): [Oracle](https://ja.wikipedia.org/wiki/Oracle "wikilink")がOracle製品に最適化したUnbreakable Enterprise Kernel（UEK）を採用。

### 開発停止

  - [Caldera OpenLinux](https://ja.wikipedia.org/wiki/Caldera_OpenLinux "wikilink") : 商用。

  - [Haansoft Linux](../Page/Haansoft_Linux.md "wikilink") : 2006 Workstation は Asianuxベース。

  - [HOLON Linux](../Page/HOLON_Linux.md "wikilink") : インターチャネル・ホロン社製。

  - [Kondara MNU/Linux](https://ja.wikipedia.org/wiki/Kondara_MNU/Linux "wikilink") : 開発者の一部が[Momonga Linuxを立ち上げ](../Page/Momonga_Linux.md "wikilink")。

  - [LASER5 Linux](https://ja.wikipedia.org/wiki/LASER5_Linux "wikilink") : 商用・個人（7.2exp以降開発停止。現在サポート終了）。

  - [Lycoris Desktop/LX](https://ja.wikipedia.org/wiki/Lycoris_Desktop/LX "wikilink") : Windows に似たユーザーインタフェース。

  - [MIRACLE LINUX](../Page/MIRACLE_LINUX.md "wikilink") : 商用、[Oracle対応](../Page/Oracle_Database.md "wikilink")、Asianuxへと移行。

  - [Momonga Linux](../Page/Momonga_Linux.md "wikilink") : [Kondara MNU/Linuxの後継](https://ja.wikipedia.org/wiki/Kondara_MNU/Linux "wikilink")。

  - [PS2 Linux](../Page/PS2_Linux.md "wikilink") : [PlayStation 2上で動作する](https://ja.wikipedia.org/wiki/PlayStation_2 "wikilink")。[Kondara MNU/Linuxベース](https://ja.wikipedia.org/wiki/Kondara_MNU/Linux "wikilink")。

  - : [紅旗Linux](https://ja.wikipedia.org/wiki/:zh:紅旗Linux "wikilink") 是[中国製](../Page/中華人民共和国.md "wikilink")。Asianuxベース。

  - [Red Hat Linux](../Page/Red_Hat_Linux.md "wikilink") : 商用および個人用　→[Fedora Coreへ事実上開発を引き継ぎ](../Page/Fedora.md "wikilink")。

  - [Red Star OS](https://ja.wikipedia.org/wiki/Red_Star_OS "wikilink") : 北朝鮮の[国策配布版](https://ja.wikipedia.org/wiki/:ko:붉은별_\(운영_체제\)#역사 "wikilink")。

  - [White Box Enterprise Linux](../Page/White_Box_Enterprise_Linux.md "wikilink") : [Red Hat Enterprise Linuxのクローン](../Page/Red_Hat_Enterprise_Linux.md "wikilink")。

  - [Mandriva Linux](../Page/Mandriva_Linux.md "wikilink") : 旧名称は、Mandrakelinux。商用版と無料版があった。

  - [StartCom Linux](../Page/StartCom_Linux.md "wikilink") : Red Hat Enterprise LinuxベースのGNU/Linux。

  - [Yellow Dog Linux](../Page/Yellow_Dog_Linux.md "wikilink") : [Fedora](../Page/Fedora.md "wikilink")ベースで[PowerPC](../Page/PowerPC.md "wikilink")専用。[PlayStation 3公式対応](https://ja.wikipedia.org/wiki/PlayStation_3 "wikilink")。

## Slackware系

  - [Slackware](../Page/Slackware.md "wikilink") : Linux普及初期は有名だったディストリビューション。
      - [Dragora GNU/Linux-Libre](https://ja.wikipedia.org/wiki/Dragora_GNU/Linux-Libre "wikilink") : 完全に自由ソフトウェアのみで構成される独自のGNU/Linuxディストリビューション。シンプルであることをコンセプトとしている。
      - [Plamo Linux](../Page/Plamo_Linux.md "wikilink") : Slackwareを日本語化し、[プラモデル](../Page/プラモデル.md "wikilink")のようにいじれることを念頭に置いて開発されている。Version3.3までは[PC-9800シリーズ](../Page/PC-9800シリーズ.md "wikilink")に対応した。
      - [Puppy Linux](../Page/Puppy_Linux.md "wikilink") : Live CD、HDインストールも可。日本語化も可能\[15\]\[16\]。debパッケージ利用可。
          - [Lxpup](https://ja.wikipedia.org/wiki/Lxpup "wikilink")\[17\] : Puppy Linuxを基盤に、デスクトップ環境をLXDEに置き換えたもの。
          - [Yara OSX](https://ja.wikipedia.org/wiki/Yara_OSX "wikilink")\[18\]\[19\] : Puppy Linux派生。[Xfce](../Page/Xfce.md "wikilink")を採用したMacOS風の画面。
  - [openSUSE](https://ja.wikipedia.org/wiki/openSUSE "wikilink") : ドイツで開発されていたため、ヨーロッパで強い。[SUSE](../Page/SUSE.md "wikilink")は[ノベルに買収されたことに伴い](../Page/ノベル_\(企業\).md "wikilink")、SUSE Linuxから改名。
      - [SUSE Linux Enterprise Server](https://ja.wikipedia.org/wiki/SUSE_Linux_Enterprise_Server "wikilink") : コミュニティによるテスト済みの[openSUSE](https://ja.wikipedia.org/wiki/openSUSE "wikilink")をベースにして安定させた。商用。
      - [SUSE Linux Enterprise Desktop](../Page/SUSE_Linux_Enterprise_Desktop.md "wikilink") : SUSE Linux Enterprise Serverのデスクトップ版。

### 開発停止

  - [United Linux](https://ja.wikipedia.org/wiki/United_Linux "wikilink") : SUSE LinuxをベースにTurboLinux、SUSE(現:Novell)、Caldera(現:SCO)、Connectiva(現:Mandriva)の4社にて共同開発。

  - \[20\] : ウィンドウマネージャとして[Xfce](../Page/Xfce.md "wikilink")を採用している。

  - [Slamd64](https://ja.wikipedia.org/wiki/Slamd64 "wikilink") : [x64](https://ja.wikipedia.org/wiki/x64 "wikilink")版Slackwareである。

## 独立系

  - [Arch Linux](https://ja.wikipedia.org/wiki/Arch_Linux "wikilink") : [パッケージ管理システム](../Page/パッケージ管理システム.md "wikilink")に[Pacman](https://ja.wikipedia.org/wiki/Pacman "wikilink")を使用。
      - [Antergos](https://ja.wikipedia.org/wiki/Antergos "wikilink") : Arch Linuxをベースに、GUIによるインストーラーであるCnchiを備えたもの。
      - [Audiophile Linux](https://ja.wikipedia.org/wiki/Audiophile_Linux "wikilink")\[21\] : [Fluxbox](../Page/Fluxbox.md "wikilink")を採用した、[オーディオ](https://ja.wikipedia.org/wiki/オーディオ "wikilink")愛好家向けOS。
      - [Manjaro](https://ja.wikipedia.org/wiki/Manjaro "wikilink") : Arch Linuxをベースに、プリインストールされたデスクトップ環境、GUIによるインストーラー等を備えたもの。
      - [Parabola GNU/Linux-libre](https://ja.wikipedia.org/wiki/Parabola_GNU/Linux-libre "wikilink") : Arch Linuxからフリーでないソフトウェアを除去し、100%フリーなソフトウェアで構成されたもの。
  - [Gentoo Linux](../Page/Gentoo_Linux.md "wikilink") : [BSD系OSのportに似た](../Page/BSDの子孫.md "wikilink")[Portage](../Page/Portage.md "wikilink")と呼ばれるパッケージ管理システムを採用。
      - [Google Chrome OS](https://ja.wikipedia.org/wiki/Google_Chrome_OS "wikilink") : Googleが開発しているOS。2010年2月に、ベースとなるOSをubuntuからGentooに変更した。
          - [Chromium OS](https://ja.wikipedia.org/wiki/Chromium_OS "wikilink") : Google Chrome OSの[オープンソース](../Page/オープンソース.md "wikilink")版。
      - [Sabayon Linux](https://ja.wikipedia.org/wiki/Sabayon_Linux "wikilink") : GentooベースのライブDVD GNU/Linux。
  - [GoboLinux](https://ja.wikipedia.org/wiki/GoboLinux "wikilink") : [Filesystem Hierarchy Standardからの脱却を目指したLinux](https://ja.wikipedia.org/wiki/Filesystem_Hierarchy_Standard "wikilink")。
  - [Tiny Core Linux](https://ja.wikipedia.org/wiki/Tiny_Core_Linux "wikilink")：Damn Small Linuxの開発者の1人であったRobert Shingledeckerが中心となって開発が進められている。サイズが10MB程度しかないことが特徴。
  - [Slitaz](https://ja.wikipedia.org/wiki/Slitaz "wikilink")：Damn Small Linuxと共通する目的を多く共有するが、より最新の Linux 2.6 カーネルに基づき、より小さい。
      - ：SliTazの派生で、[uClibc](https://ja.wikipedia.org/wiki/uClibc "wikilink")を使用し、[フロッピーディスク](../Page/フロッピーディスク.md "wikilink")からの起動が可能。

### 開発停止

  - [Foresight Linux](../Page/Foresight_Linux.md "wikilink") : [Conary](https://ja.wikipedia.org/wiki/Conary "wikilink")と呼ばれる次世代パッケージ管理システムを採用。
  - [iPodLinux](https://ja.wikipedia.org/wiki/iPodLinux "wikilink") : [iPod](https://ja.wikipedia.org/wiki/iPod "wikilink")用に[µClinux](https://ja.wikipedia.org/wiki/µClinux "wikilink")をカーネルとしたもの。
  - [IPnuts](../Page/IPnuts.md "wikilink") : ルータ・ファイアウォール構築に使用。
  - [MkLinux](https://ja.wikipedia.org/wiki/MkLinux "wikilink") : [PowerPC](../Page/PowerPC.md "wikilink")搭載機専用、[Mach](../Page/Mach.md "wikilink")ベース。
  - [Nature's Linux](https://ja.wikipedia.org/wiki/Nature's_Linux "wikilink") : 無料の開発版とOS監視サポート付きの有料版がある。FreeBSDのjailに似た仮想ファイルシステム、jailを利用したバックアップとリカバリ機能、ファイル改竄検出機能などを持つ。
  - [SLS](https://ja.wikipedia.org/wiki/SLS "wikilink") : GNU/Linuxで最も初期のディストリビューション。
  - [Stataboware](https://ja.wikipedia.org/wiki/Stataboware "wikilink") : Slackwareに似た構造で、[Alpha搭載機専用](https://ja.wikipedia.org/wiki/DEC_Alpha "wikilink")。
  - [Splashtop](https://ja.wikipedia.org/wiki/Splashtop "wikilink") : 起動速度を重視して開発されたOS。
  - [Turbolinux](../Page/Turbolinux.md "wikilink") : パッケージ管理システムとして[RPMを使っている](../Page/RPM_Package_Manager.md "wikilink")。
  - [Yggdrasil Linux](https://ja.wikipedia.org/wiki/:en:Yggdrasil_Linux "wikilink"): Linuxディストリビューション初の[Live CD](../Page/Live_CD.md "wikilink") 1992.8-1995

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
3.  [Elementary OS](https://elementary.io/)
4.
5.
6.  [Pear Linux](http://pearlinux.fr/)
7.  [ChaletOS - Google Sites](https://sites.google.com/site/chaletoslinux/home)
8.  [ChaletOS - DistroWatch.com](https://distrowatch.com/table.php?distribution=chaletos&pkglist=true&version=16.04.2)
9.  [ChaletOS download | SourceForge.net](https://sourceforge.net/projects/chaletos/)
10. [Live Voyager](https://voyagerlive.org/)
11. [DistroWatch.com: Voyager Live](https://distrowatch.com/table.php?distribution=voyager)
12. [Voyager 日本語情報トップページ - OSDN](https://ja.osdn.net/projects/sfnet_voyagerlive/)
13. [Windows 10に最適化されたLinuxディストロ「WLinux」が爆誕 - 期間限定の50%オフでセール中](https://www.softantenna.com/wp/windows/wlinux/)
14. [Windows 10 now has its own exclusive Linux distro -- WLinux](https://betanews.com/2018/09/24/windows-10-now-has-its-own-exclusive-linux-distro-wlinux/)
15. [日本語サポートパッケージ - sakurapup.browserloadofcoolness.com](http://sakurapup.browserloadofcoolness.com/viewtopic.php?t=1937)
16. [日本語化ファイル入手先](http://shinobar.server-on.net/puppy/opt/)
17. [LxPup - Puppy Linux + LXDE 日本語情報トップページ - OSDN](https://ja.osdn.net/projects/sfnet_lxpup/)
18. [Yara OSX - Home](https://yara-osx.weebly.com/)
19. [Puppy Linux Discussion Forum :: View topic - Yara OSX 3](http://www.murga-linux.com/puppy/viewtopic.php?t=107173)
20.
21. [AudioPhile Linux | Quality audio on Linux](https://www.ap-linux.com/)
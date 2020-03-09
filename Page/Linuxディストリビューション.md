> この記事は[Linux](https://ja.wikipedia.org/wiki/Linux)から翻訳されています。


**Linuxディストリビューション**とは、[Linux](https://ja.wikipedia.org/wiki/Linux "wikilink")を一般利用者が[インストール](https://ja.wikipedia.org/wiki/インストール "wikilink")したり、利用できる形にまとめ上げたもの（distribution＝配布・流通・頒布形態）。

## コンポーネント

[Linux_Distribution_Timeline.svg](https://ja.wikipedia.org/wiki/File:Linux_Distribution_Timeline.svg "fig:Linux_Distribution_Timeline.svg") [カーネル](../Page/カーネル.md "wikilink")の他、基本的なUNIXのツールやユーティリティ、その他[サーバ](https://ja.wikipedia.org/wiki/サーバ "wikilink")向けや[デスクトップ環境](https://ja.wikipedia.org/wiki/デスクトップ環境 "wikilink")向けの[ソフトウェア](../Page/ソフトウェア.md "wikilink")を集め、ビルドして[バイナリパッケージ](https://ja.wikipedia.org/wiki/バイナリパッケージ "wikilink")を作成し提供している。その他、最初のインストールの際に必要な[インストーラ等といった補助的なシステムが付属する](https://ja.wikipedia.org/wiki/インストール "wikilink")。バイナリパッケージを利用するという形態のために、rpmやdebなど、何らかのバイナリパッケージシステムの採用がほぼ必須であり、どのシステムを採用しているかがディストリビューションの主要な特徴のひとつとなる。yumなどより上位の[パッケージ管理システム](https://ja.wikipedia.org/wiki/パッケージ管理システム "wikilink")も、現代ではほぼ必須である。

  - [Linuxカーネル](https://ja.wikipedia.org/wiki/Linuxカーネル "wikilink")
      - （Linuxカーネル以外の場合は「Linuxディストリビューション」ではない（Debian/FreeBSDなど））
      - その他、カーネルモジュール等
  - 必須なツールやユーティリティやライブラリ
      - util-linux（[:en:Util-linux](https://ja.wikipedia.org/wiki/:en:Util-linux "wikilink")）
      - [GNU Core Utilities](https://ja.wikipedia.org/wiki/GNU_Core_Utilities "wikilink")（coreutilsとも。昔のfileutils, shellutils, textutilsは全てcoreutilsに取り込まれた）
      - [Bourne Shell](https://ja.wikipedia.org/wiki/Bourne_Shell "wikilink") 互換シェル（他のシェルと違い /bin/sh として必須である）
      - [Unixシェル](https://ja.wikipedia.org/wiki/Unixシェル "wikilink")
      - [glibc](https://ja.wikipedia.org/wiki/GNU_Cライブラリ "wikilink")
  - 起動に必要なもの
      - [init](https://ja.wikipedia.org/wiki/init "wikilink")
      - /etc などの基本的なファイル群
  - コンパイラ等
      - [GNU Binutils](https://ja.wikipedia.org/wiki/GNU_Binutils "wikilink") (binutils)
      - [GCC](../Page/GNUコンパイラコレクション.md "wikilink")
  - 各種の設定を行うソフト
  - [スクリプト言語](../Page/スクリプト言語.md "wikilink")（sed, awk, etc）
  - GUI関係
      - [X11のフリーな実装である](https://ja.wikipedia.org/wiki/X_Window_System "wikilink")[XFree86](https://ja.wikipedia.org/wiki/XFree86 "wikilink")、[XOrg](https://ja.wikipedia.org/wiki/X.Org_Foundation "wikilink")
          - [デスクトップ環境](https://ja.wikipedia.org/wiki/デスクトップ環境 "wikilink")として[GNOME](https://ja.wikipedia.org/wiki/GNOME "wikilink")、[KDE](https://ja.wikipedia.org/wiki/KDE "wikilink")、[Xfce](https://ja.wikipedia.org/wiki/Xfce "wikilink")
          - [ウィンドウマネージャ](https://ja.wikipedia.org/wiki/ウィンドウマネージャ "wikilink")
  - デスクトップ向けアプリケーション
      - [ウェブブラウザ](../Page/ウェブブラウザ.md "wikilink")
      - [電子メールクライアント](https://ja.wikipedia.org/wiki/電子メールクライアント "wikilink")
      - [テキストエディタ](https://ja.wikipedia.org/wiki/テキストエディタ "wikilink")
      - [オフィススイート](https://ja.wikipedia.org/wiki/オフィススイート "wikilink")
      - [マルチメディア](https://ja.wikipedia.org/wiki/マルチメディア "wikilink")
      - [ゲーム](../Page/ゲーム.md "wikilink")
  - サーバ向けアプリケーション
      - [メールサーバ](https://ja.wikipedia.org/wiki/メールサーバ "wikilink")
      - [Webサーバ](https://ja.wikipedia.org/wiki/Webサーバ "wikilink")
      - [データベース管理システム](https://ja.wikipedia.org/wiki/データベース管理システム "wikilink")
  - ソフトウェア開発向けアプリケーション
      - 多数のコンピュータ言語開発環境

これらはソフトウェア構成の例であり、他にも様々なソフトウェアをインストールできる。

## 配布方法

ディストリビューションは、自由に配布、利用の出来るソフトウェア（[フリーソフトウェア](../Page/フリーソフトウェア.md "wikilink")）だけを集め、無料で提供されるものと、利用に料金を払う必要のある商用ソフトウェアや企業によるサポートを受けられる権利を含んだ有料のものに分けられる。大抵の場合、前者は[FTPなどで公開されており](../Page/File_Transfer_Protocol.md "wikilink")、[Torrent](https://ja.wikipedia.org/wiki/Torrent "wikilink")を利用した配布をするディストリビューション\[1\]も存在する。後者はユーザー数などに制限のあるライセンス契約によって提供される。どちらの場合も、[CD-ROM](../Page/CD-ROM.md "wikilink")等によって入手することができる。GNU/Linuxディストリビューターによっては両方を用意している場合や、サポートのみ有償で受けられる場合もある。

## Debian系

[Screenshot-debian_wheezy_ja.png](https://ja.wikipedia.org/wiki/File:Screenshot-debian_wheezy_ja.png "fig:Screenshot-debian_wheezy_ja.png") [Screenshot_of_Ubuntu_15.10_Desktop_live_CD.png](https://ja.wikipedia.org/wiki/File:Screenshot_of_Ubuntu_15.10_Desktop_live_CD.png "fig:Screenshot_of_Ubuntu_15.10_Desktop_live_CD.png") [Kubuntu-13.10-Saucy-Salamander.png](https://ja.wikipedia.org/wiki/File:Kubuntu-13.10-Saucy-Salamander.png "fig:Kubuntu-13.10-Saucy-Salamander.png") [Xubuntu_14.04_LTS.png](https://ja.wikipedia.org/wiki/File:Xubuntu_14.04_LTS.png "fig:Xubuntu_14.04_LTS.png") パッケージ管理システムに[deb](https://ja.wikipedia.org/wiki/deb "wikilink")形式を使っている。主要なものは以下の通り。

  - [Debian GNU/Linux](../Page/Debian.md "wikilink") : 100%[フリーソフトウェア](../Page/フリーソフトウェア.md "wikilink")であることが理念、コミュニティベース。
      - [ARMA aka Omoikane GNU/Linux](https://ja.wikipedia.org/wiki/ARMA_aka_Omoikane_GNU/Linux "wikilink") : [ファイルシステム](https://ja.wikipedia.org/wiki/ファイルシステム "wikilink")に[XFS](https://ja.wikipedia.org/wiki/XFS "wikilink")を採用している。
      - [gNewSense](https://ja.wikipedia.org/wiki/gNewSense "wikilink") : [GNU FSDGに適合し](https://ja.wikipedia.org/wiki/GNUプロジェクト#GNU_FSDG "wikilink")、[フリーソフトウェア財団](../Page/フリーソフトウェア財団.md "wikilink")の支援を受ける。[Linux-libre](https://ja.wikipedia.org/wiki/Linux-libre "wikilink")を使用し、ファームウェアのレベルまで100%自由ソフトで構成される。
      - [Kali Linux](https://ja.wikipedia.org/wiki/Kali_Linux "wikilink") : Debianベースの1DVDタイプ。[ペネトレーションテスト](https://ja.wikipedia.org/wiki/ペネトレーションテスト "wikilink")目的に特化していることが特徴。[BackTrack](https://ja.wikipedia.org/wiki/BackTrack "wikilink")からフォーク。
      - [KANOTIX](https://ja.wikipedia.org/wiki/KANOTIX "wikilink") : DebianベースでCDブート/HDDインストール共可能。
      - [KNOPPIX](https://ja.wikipedia.org/wiki/KNOPPIX "wikilink") : DebianをベースにCDブートで利用できるようにしている。
      - [MX Linux](https://ja.wikipedia.org/wiki/MX_Linux "wikilink") : Debianをベースとした中量級のディストリビューション。
      - [SLAX](https://ja.wikipedia.org/wiki/SLAX "wikilink") : CDブートで利用できるようにしている。9.xより前のバージョンではSlackwareをベースにしていた。日本語化された\[<http://hatochan.dyndns.org/slax-ja/index.php>? SLAX-ja\]も存在する。
      - [Kona Linux](https://ja.wikipedia.org/wiki/Kona_Linux "wikilink")(Ubuntu Editionを除く): 最初から日本語化されており、LXDEからGNOME、KDE、Cinammonなど、いろいろなデスクトップ環境が選べるのが特徴。
      - [SteamOS](https://ja.wikipedia.org/wiki/SteamOS "wikilink") : ゲーム配信サービス[Steam](https://ja.wikipedia.org/wiki/Steam "wikilink")の運営元が開発した[ゲーミングPC用OS](https://ja.wikipedia.org/wiki/ゲームパソコン "wikilink")。
      - [Tails](https://ja.wikipedia.org/wiki/Tails_\(オペレーティングシステム\) "wikilink") : Debianベースでプライバシーと匿名性に特化している。[Live CD](https://ja.wikipedia.org/wiki/Live_CD "wikilink")・[Live USBに対応している](https://ja.wikipedia.org/wiki/Live_USB "wikilink")。
      - [Ubuntu](https://ja.wikipedia.org/wiki/Ubuntu "wikilink") : 6ヶ月ごとのリリースと商用サポートを掲げる。デスクトップ環境として[Unityを採用している](https://ja.wikipedia.org/wiki/Unity_\(ユーザインタフェース\) "wikilink")。
          - [Basix](https://ja.wikipedia.org/wiki/Basix "wikilink") : ユーザーのカスタマイズを前提としたディストリビューション。
          - [elementary OS](https://ja.wikipedia.org/wiki/elementary_OS "wikilink") : Pantheonという独自のデスクトップ環境を採用している。
          - [Edubuntu](https://ja.wikipedia.org/wiki/Edubuntu "wikilink") : 教育用にカスタマイズされている。
          - [Elbuntu](https://ja.wikipedia.org/wiki/Elbuntu "wikilink") : [ウィンドウマネージャ](https://ja.wikipedia.org/wiki/ウィンドウマネージャ "wikilink")として[Enlightenment](https://ja.wikipedia.org/wiki/Enlightenment "wikilink")を採用している。
          - [Gobuntu](https://ja.wikipedia.org/wiki/Gobuntu "wikilink") : [フリーソフトウェア](../Page/フリーソフトウェア.md "wikilink")のみを利用している。
          - [Goobuntu](https://ja.wikipedia.org/wiki/Goobuntu "wikilink") : [Google](https://ja.wikipedia.org/wiki/Google "wikilink")が社内で開発・利用しているとされている。非公開。\[2\]\[3\]
          - [Kubuntu](https://ja.wikipedia.org/wiki/Kubuntu "wikilink") : デスクトップ環境として[KDE](https://ja.wikipedia.org/wiki/KDE "wikilink")を採用している。
          - [Kona Linux](https://ja.wikipedia.org/wiki/Kona_Linux "wikilink") Ubuntu Edition : 前述のKona LinuxをUbuntuベースに置き換えたもの。
          - [linuxBean](https://ja.wikipedia.org/wiki/linuxBean "wikilink") : 軽量ながらも初心者向けのディストリビューション。
          - [Lubuntu](https://ja.wikipedia.org/wiki/Lubuntu "wikilink") : デスクトップ環境として[LXDE](https://ja.wikipedia.org/wiki/LXDE "wikilink")を採用している。
          - [nUbuntu](https://ja.wikipedia.org/wiki/nUbuntu "wikilink") : セキュリティツールを多数含んでいる。
          - [Trisquel GNU/Linux](https://ja.wikipedia.org/wiki/Trisquel_GNU/Linux "wikilink") : GNU FSDGに適合し、フリーソフトウェア財団のサーバーで使用される。ファームウェアのレベルまで100%自由ソフトで構成される。
          - [Ubuntu Christian Edition](https://ja.wikipedia.org/wiki/Ubuntu_Christian_Edition "wikilink") : 聖書全文とURLフィルタリングを搭載している。
          - [Ubuntu Lite](https://ja.wikipedia.org/wiki/Ubuntu_Lite "wikilink") : [レガシーデバイス](https://ja.wikipedia.org/wiki/レガシーデバイス "wikilink")を備えた古いコンピュータ用。
          - [Ubuntu Studio](https://ja.wikipedia.org/wiki/Ubuntu_Studio "wikilink") : ハイエンドデスクトップ向け。デジタルコンテンツ制作ツールが多数プリインストールされている。[リアルタイムカーネルのパッチも当てられている](https://ja.wikipedia.org/wiki/リアルタイムオペレーティングシステム "wikilink")。
          - [Xubuntu](https://ja.wikipedia.org/wiki/Xubuntu "wikilink") : デスクトップ環境として[Xfce](https://ja.wikipedia.org/wiki/Xfce "wikilink")を採用している。
          - [zUbuntu](https://ja.wikipedia.org/wiki/zUbuntu "wikilink") : [IBM eServer zSeries](https://ja.wikipedia.org/wiki/System_z "wikilink")[メインフレーム](https://ja.wikipedia.org/wiki/メインフレーム "wikilink")用。
          - [Linux Mint](https://ja.wikipedia.org/wiki/Linux_Mint "wikilink") : デザインやソフトウェア環境を改善し、マルチメディア関係のコーデックを充実させている。
              - [Peppermint](https://ja.wikipedia.org/wiki/Peppermint "wikilink") : [Chromium](https://ja.wikipedia.org/wiki/Chromium "wikilink")を搭載している軽量のディストリビューション。Webアプリとの連携も強い。
      - [Raspbian](https://ja.wikipedia.org/wiki/Raspbian "wikilink")：[Raspberry Pi用のdebian](https://ja.wikipedia.org/wiki/Raspberry_Pi "wikilink")。特定の機種用としての配布は、装置が固定しているため使いやすい。Idとパスワードの初期設定が好ましくない。ネットワークに接続する前にrootとID:piのパスワード設定をする必要がある。
      - [WLinux](https://ja.wikipedia.org/wiki/WLinux "wikilink")\[4\]\[5\]

### 開発停止

  - [aptosid](https://ja.wikipedia.org/wiki/aptosid "wikilink") : Debian sidベースでCDブート/HDDインストール共可能。旧称はsidux。
  - [BackTrack](https://ja.wikipedia.org/wiki/BackTrack "wikilink") : Debianベースであり、[Kali Linuxの前身](https://ja.wikipedia.org/wiki/Kali_Linux "wikilink")。ペネトレーションテスト目的に特化していることが特徴だった。
  - [CrunchBang Linux](https://ja.wikipedia.org/wiki/CrunchBang_Linux "wikilink") : ウィンドウマネージャとして[Openbox](https://ja.wikipedia.org/wiki/Openbox "wikilink")を採用している軽量ディストリビューション。
  - [Corel Linux](https://ja.wikipedia.org/wiki/Corel_Linux "wikilink")
      - [Xandros](https://ja.wikipedia.org/wiki/Xandros "wikilink") : Corel Linuxの後継。[Eee PCに搭載されていた](https://ja.wikipedia.org/wiki/Eee_PC "wikilink")。
  - [Ecolinux](https://ja.wikipedia.org/wiki/Ecolinux "wikilink") : デスクトップ環境として[Xfce](https://ja.wikipedia.org/wiki/Xfce "wikilink")を採用した日本発のディストリビューション。
  - [Freespire](https://ja.wikipedia.org/wiki/Freespire "wikilink") : [Linspire](https://ja.wikipedia.org/wiki/Linspire "wikilink")の無料版。CDブート/HDDインストール共可能。
  - [Linspire](https://ja.wikipedia.org/wiki/Linspire "wikilink") : [Windowsのような使い勝手を実現](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")。旧称はLindows。
  - [MEPIS](https://ja.wikipedia.org/wiki/MEPIS "wikilink") : 主にデスクトップ向け。CDブート/HDDインストール共可能。
  - [Progeny Debian](https://ja.wikipedia.org/wiki/Progeny_Debian "wikilink") : Red HatのAnacondaインストーラを移植したGNU/Linux。
  - [UserLinux](https://ja.wikipedia.org/wiki/UserLinux "wikilink") : Debianベースの企業向けデスクトップ用GNU/Linux。
  - [Damn Small Linux](https://ja.wikipedia.org/wiki/Damn_Small_Linux "wikilink") : KNOPPIXベース、軽量。
  - [gOS](https://ja.wikipedia.org/wiki/gOS "wikilink") : Googleが提供するWebアプリケーションを活用できるように設定されている。
  - [Regret](https://ja.wikipedia.org/wiki/Regret_\(Linuxディストリビューション\) "wikilink") : KNOPPIXベースの日本のディストリビューション。
  - [Xenoppix](https://ja.wikipedia.org/wiki/KNOPPIX "wikilink") : KNOPPIXに[Xenを搭載した日本のディストリビューション](https://ja.wikipedia.org/wiki/Xen_\(仮想化ソフトウェア\) "wikilink")。
  - [Fluxbuntu](https://ja.wikipedia.org/wiki/Fluxbuntu "wikilink") : Ubuntuベース。ウィンドウマネージャとして[Fluxbox](https://ja.wikipedia.org/wiki/Fluxbox "wikilink")を採用している。
  - 巫女 GNYO/Linux : [openMosix](https://ja.wikipedia.org/wiki/openMosix "wikilink")と[SCore](https://ja.wikipedia.org/wiki/SCore "wikilink")を利用したPCクラスタが構築可能。CDブート/HDDインストール共可能。

## Red Hat系

[Vine61_desktop.png](https://ja.wikipedia.org/wiki/File:Vine61_desktop.png "fig:Vine61_desktop.png") パッケージ管理システムとして[RPMを使っている](https://ja.wikipedia.org/wiki/RPM_Package_Manager "wikilink")。主要なものは以下の通り。

  - [Fedora](https://ja.wikipedia.org/wiki/Fedora "wikilink") : [Red Hat Linux](https://ja.wikipedia.org/wiki/Red_Hat_Linux "wikilink") 後継のコミュニティによる実験要素が強い。
      - [Red Hat Enterprise Linux](https://ja.wikipedia.org/wiki/Red_Hat_Enterprise_Linux "wikilink") : コミュニティによるテスト済みのFedoraをベースにして安定させた。商用。
          - [Asianux](https://ja.wikipedia.org/wiki/Asianux "wikilink") : アジア5ヵ国の企業が共同開発。Red Hat Enterprise Linuxベース。
          - [CentOS](https://ja.wikipedia.org/wiki/CentOS "wikilink") : Red Hat Enterprise Linuxのクローン。
          - [Scientific Linux](https://ja.wikipedia.org/wiki/Scientific_Linux "wikilink")（旧 Fermi Linux） : Red Hat Enterprise Linuxのクローン。
      - [Berry Linux](https://ja.wikipedia.org/wiki/Berry_Linux "wikilink") : 日本人の中田裕一朗が[Fedora](https://ja.wikipedia.org/wiki/Fedora "wikilink")をベースに開発。
  - [Mageia](https://ja.wikipedia.org/wiki/Mageia "wikilink") : [Mandriva Linuxをベースに開発](https://ja.wikipedia.org/wiki/Mandriva_Linux "wikilink")。オープンソース。
  - [PCLinuxOS](https://ja.wikipedia.org/wiki/PCLinuxOS "wikilink") : Mandriva Linuxをベースに開発。デスクトップ指向。
  - [Vine Linux](https://ja.wikipedia.org/wiki/Vine_Linux "wikilink") : 日本国産のLinuxディストリビューション。
  - [RedHawk Linux](https://ja.wikipedia.org/wiki/RedHawk_Linux "wikilink") : [RHELのカーネルをリアルタイムLinuxカーネルに置き換えた](https://ja.wikipedia.org/wiki/Red_Hat_Enterprise_Linux "wikilink")。商用。
  - [Oracle Linux](https://ja.wikipedia.org/wiki/Oracle_Linux "wikilink"): [Oracle](https://ja.wikipedia.org/wiki/Oracle "wikilink")がOracle製品に最適化したUnbreakable Enterprise Kernel（UEK）を採用。

### 開発停止

  - [Caldera OpenLinux](https://ja.wikipedia.org/wiki/Caldera_OpenLinux "wikilink") : 商用。
  - [Haansoft Linux](https://ja.wikipedia.org/wiki/Haansoft_Linux "wikilink") : 2006 Workstation は Asianuxベース。
  - [HOLON Linux](https://ja.wikipedia.org/wiki/HOLON_Linux "wikilink") : インターチャネル・ホロン社製。
  - [Kondara MNU/Linux](https://ja.wikipedia.org/wiki/Kondara_MNU/Linux "wikilink") : 開発者の一部が[Momonga Linuxを立ち上げ](https://ja.wikipedia.org/wiki/Momonga_Linux "wikilink")。
  - [LASER5 Linux](https://ja.wikipedia.org/wiki/LASER5_Linux "wikilink") : 商用・個人（7.2exp以降開発停止。現在サポート終了）。
  - [Lycoris Desktop/LX](https://ja.wikipedia.org/wiki/Lycoris_Desktop/LX "wikilink") : Windows に似たユーザーインタフェース。
  - [MIRACLE LINUX](https://ja.wikipedia.org/wiki/MIRACLE_LINUX "wikilink") : 商用、[Oracle対応](https://ja.wikipedia.org/wiki/Oracle_Database "wikilink")、Asianuxへと移行。
  - [Momonga Linux](https://ja.wikipedia.org/wiki/Momonga_Linux "wikilink") : [Kondara MNU/Linuxの後継](https://ja.wikipedia.org/wiki/Kondara_MNU/Linux "wikilink")。
  - [PS2 Linux](https://ja.wikipedia.org/wiki/PS2_Linux "wikilink") : [PlayStation 2上で動作する](https://ja.wikipedia.org/wiki/PlayStation_2 "wikilink")。[Kondara MNU/Linuxベース](https://ja.wikipedia.org/wiki/Kondara_MNU/Linux "wikilink")。
  - [Red Flag Linux](https://ja.wikipedia.org/wiki/Red_Flag_Linux "wikilink") : 紅旗Linux[中国製](../Page/中華人民共和国.md "wikilink")。Asianuxベース。
  - [Red Hat Linux](https://ja.wikipedia.org/wiki/Red_Hat_Linux "wikilink") : 商用および個人用　→[Fedora Coreへ事実上開発を引き継ぎ](https://ja.wikipedia.org/wiki/Fedora "wikilink")。
  - [Red Star OS](https://ja.wikipedia.org/wiki/Red_Star_OS "wikilink") : 北朝鮮の国策ディストリビューション。
  - [White Box Enterprise Linux](https://ja.wikipedia.org/wiki/White_Box_Enterprise_Linux "wikilink") : [Red Hat Enterprise Linuxのクローン](https://ja.wikipedia.org/wiki/Red_Hat_Enterprise_Linux "wikilink")。
  - [Mandriva Linux](https://ja.wikipedia.org/wiki/Mandriva_Linux "wikilink") : 旧名称は、Mandrakelinux。商用版と無料版があった。
  - [StartCom Linux](https://ja.wikipedia.org/wiki/StartCom_Linux "wikilink") : Red Hat Enterprise LinuxベースのGNU/Linux。
  - [Yellow Dog Linux](https://ja.wikipedia.org/wiki/Yellow_Dog_Linux "wikilink") : [Fedora](https://ja.wikipedia.org/wiki/Fedora "wikilink")ベースで[PowerPC](../Page/PowerPC.md "wikilink")専用。[PlayStation 3公式対応](https://ja.wikipedia.org/wiki/PlayStation_3 "wikilink")。

## Slackware系

  - [Slackware](https://ja.wikipedia.org/wiki/Slackware "wikilink") : Linux普及初期は有名だったディストリビューション。
      - [Plamo Linux](https://ja.wikipedia.org/wiki/Plamo_Linux "wikilink") : Slackwareを日本語化し、[プラモデル](../Page/プラモデル.md "wikilink")のようにいじれることを念頭に置いて開発されている。Version3.3までは[PC-9800シリーズ](https://ja.wikipedia.org/wiki/PC-9800シリーズ "wikilink")に対応した。
      - [Puppy Linux](https://ja.wikipedia.org/wiki/Puppy_Linux "wikilink") : Live CD、HDインストールも可。debパッケージ利用可。
  - [openSUSE](https://ja.wikipedia.org/wiki/openSUSE "wikilink") : ドイツで開発されていたため、ヨーロッパで強い。[SUSE](https://ja.wikipedia.org/wiki/SUSE "wikilink")は[ノベルに買収されたことに伴い](https://ja.wikipedia.org/wiki/ノベル_\(企業\) "wikilink")、SUSE Linuxから改名。
      - [SUSE Linux Enterprise Server](https://ja.wikipedia.org/wiki/SUSE_Linux_Enterprise_Server "wikilink") : コミュニティによるテスト済みの[openSUSE](https://ja.wikipedia.org/wiki/openSUSE "wikilink")をベースにして安定させた。商用。
      - [SUSE Linux Enterprise Desktop](https://ja.wikipedia.org/wiki/SUSE_Linux_Enterprise_Desktop "wikilink") : SUSE Linux Enterprise Serverのデスクトップ版。

### 開発停止

  - [United Linux](https://ja.wikipedia.org/wiki/United_Linux "wikilink") : SUSE LinuxをベースにTurboLinux、SUSE(現:Novell)、Caldera(現:SCO)、Connectiva(現:Mandriva)の4社にて共同開発。
  - [Wolvix](https://ja.wikipedia.org/wiki/Wolvix "wikilink") : ウィンドウマネージャとして[Xfce](https://ja.wikipedia.org/wiki/Xfce "wikilink")を採用している。
  - [Slamd64](https://ja.wikipedia.org/wiki/Slamd64 "wikilink") : [x64](https://ja.wikipedia.org/wiki/x64 "wikilink")版Slackwareである。

## 独立系

  - [Arch Linux](https://ja.wikipedia.org/wiki/Arch_Linux "wikilink") : [パッケージ管理システム](https://ja.wikipedia.org/wiki/パッケージ管理システム "wikilink")に[Pacman](https://ja.wikipedia.org/wiki/Pacman "wikilink")を使用。
      - [Antergos](https://ja.wikipedia.org/wiki/Antergos "wikilink") : Arch Linuxをベースに、GUIによるインストーラーであるCnchiを備えたもの。
      - [Manjaro](https://ja.wikipedia.org/wiki/Manjaro "wikilink") : Arch Linuxをベースに、プリインストールされたデスクトップ環境、GUIによるインストーラー等を備えたもの。
      - [Parabola GNU/Linux-libre](https://ja.wikipedia.org/wiki/Parabola_GNU/Linux-libre "wikilink") : Arch Linuxからフリーでないソフトウェアを除去し、100%フリーなソフトウェアで構成されたもの。
  - [Gentoo Linux](https://ja.wikipedia.org/wiki/Gentoo_Linux "wikilink") : [BSD系OSのportに似た](https://ja.wikipedia.org/wiki/BSDの子孫 "wikilink")[Portage](https://ja.wikipedia.org/wiki/Portage "wikilink")と呼ばれるパッケージ管理システムを採用。
      - [Google Chrome OS](https://ja.wikipedia.org/wiki/Google_Chrome_OS "wikilink") : Googleが開発しているOS。2010年2月に、ベースとなるOSをubuntuからGentooに変更した。
          - [Chromium OS](https://ja.wikipedia.org/wiki/Chromium_OS "wikilink") : Google Chrome OSの[オープンソース](../Page/オープンソース.md "wikilink")版。
      - [Sabayon Linux](https://ja.wikipedia.org/wiki/Sabayon_Linux "wikilink") : GentooベースのライブDVD GNU/Linux。
  - [GoboLinux](https://ja.wikipedia.org/wiki/GoboLinux "wikilink") : [Filesystem Hierarchy Standardからの脱却を目指したLinux](https://ja.wikipedia.org/wiki/Filesystem_Hierarchy_Standard "wikilink")。
  - [Tiny Core Linux](https://ja.wikipedia.org/wiki/Tiny_Core_Linux "wikilink")：Damn Small Linuxの開発者の1人であったRobert Shingledeckerが中心となって開発が進められている。サイズが10MB程度しかないことが特徴。
  - [Slitaz](https://ja.wikipedia.org/wiki/Slitaz "wikilink")：Damn Small Linuxと共通する目的を多く共有するが、より最新の Linux 2.6 カーネルに基づき、より小さい。
      - [Tiny SliTaz](https://ja.wikipedia.org/wiki/Tiny_SliTaz "wikilink")：SliTazの派生で、[uClibc](https://ja.wikipedia.org/wiki/uClibc "wikilink")を使用し、[フロッピーディスク](https://ja.wikipedia.org/wiki/フロッピーディスク "wikilink")からの起動が可能。

### 開発停止

  - [Foresight Linux](https://ja.wikipedia.org/wiki/Foresight_Linux "wikilink") : [Conary](https://ja.wikipedia.org/wiki/Conary "wikilink")と呼ばれる次世代パッケージ管理システムを採用。
  - [iPodLinux](https://ja.wikipedia.org/wiki/iPodLinux "wikilink") : [iPod](https://ja.wikipedia.org/wiki/iPod "wikilink")用に[µClinux](https://ja.wikipedia.org/wiki/µClinux "wikilink")をカーネルとしたもの。
  - [IPnuts](https://ja.wikipedia.org/wiki/IPnuts "wikilink") : ルータ・ファイアウォール構築に使用。
  - [MkLinux](https://ja.wikipedia.org/wiki/MkLinux "wikilink") : [PowerPC](../Page/PowerPC.md "wikilink")搭載機専用、[Mach](../Page/Mach.md "wikilink")ベース。
  - [Nature's Linux](https://ja.wikipedia.org/wiki/Nature's_Linux "wikilink") : 無料の開発版とOS監視サポート付きの有料版がある。FreeBSDのjailに似た仮想ファイルシステム、jailを利用したバックアップとリカバリ機能、ファイル改竄検出機能などを持つ。
  - [Omaemona 2ch/Linux](https://ja.wikipedia.org/wiki/Omaemona_2ch/Linux "wikilink") : [Linux from Scratchベース](https://ja.wikipedia.org/wiki/Linux_from_Scratch "wikilink")。
  - [SLS](https://ja.wikipedia.org/wiki/SLS "wikilink") : GNU/Linuxで最も初期のディストリビューション。
  - [Stataboware](https://ja.wikipedia.org/wiki/Stataboware "wikilink") : Slackwareに似た構造で、[Alpha搭載機専用](https://ja.wikipedia.org/wiki/DEC_Alpha "wikilink")。
  - [Splashtop](https://ja.wikipedia.org/wiki/Splashtop "wikilink") : 起動速度を重視して開発されたOS。
  - [Turbolinux](https://ja.wikipedia.org/wiki/Turbolinux "wikilink") : パッケージ管理システムとして[RPMを使っている](https://ja.wikipedia.org/wiki/RPM_Package_Manager "wikilink")。
  - [Yggdrasil Linux](https://ja.wikipedia.org/wiki/:en:Yggdrasil_Linux "wikilink"): Linuxディストリビューション初の[Live CD](https://ja.wikipedia.org/wiki/Live_CD "wikilink") 1992.8-1995

## 脚注

<references />

## 関連項目

  - [ディストリビューション](https://ja.wikipedia.org/wiki/ディストリビューション "wikilink")
  - [インタフェース](https://ja.wikipedia.org/wiki/インタフェース "wikilink")
  - [GNU/Linuxシステム](https://ja.wikipedia.org/wiki/GNU/Linuxシステム "wikilink")
  - [Linux](https://ja.wikipedia.org/wiki/Linux "wikilink")
  - [軽量Linuxディストリビューション](https://ja.wikipedia.org/wiki/軽量Linuxディストリビューション "wikilink")
  - [Linuxディストリビューションの比較](https://ja.wikipedia.org/wiki/Linuxディストリビューションの比較 "wikilink")
  - [組み込みLinux](https://ja.wikipedia.org/wiki/組み込みLinux "wikilink")
  - [Linux Standard Base](https://ja.wikipedia.org/wiki/Linux_Standard_Base "wikilink")
  - [Linux from Scratch](https://ja.wikipedia.org/wiki/Linux_from_Scratch "wikilink") : 一から環境を構築する手法
  - [DistroWatch](https://ja.wikipedia.org/wiki/DistroWatch "wikilink")

## 外部リンク

[DistroWatch.com](https://distrowatch.com/) - GNU/Linux及び[FreeBSDディストリビューション](https://ja.wikipedia.org/wiki/FreeBSDディストリビューション "wikilink")の情報サイト

[Category:Linuxディストリビューション](https://ja.wikipedia.org/wiki/Category:Linuxディストリビューション "wikilink") [Category:Linux](https://ja.wikipedia.org/wiki/Category:Linux "wikilink")

1.  例えば[Ubuntu](http://www.ubuntulinux.jp/download/ja-remix)など。
2.
3.
4.  [Windows 10に最適化されたLinuxディストロ「WLinux」が爆誕 - 期間限定の50%オフでセール中](https://www.softantenna.com/wp/windows/wlinux/)
5.  [Windows 10 now has its own exclusive Linux distro -- WLinux](https://betanews.com/2018/09/24/windows-10-now-has-its-own-exclusive-linux-distro-wlinux/)
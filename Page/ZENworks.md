> この記事は[ZENworks](https://ja.wikipedia.org/wiki/ZENworks)から翻訳されています。


**ZENworks** は[ノベルが開発した](../Page/ノベル_\(企業\).md "wikilink")[システム管理](../Page/システム管理.md "wikilink")のための[ソフトウェア](../Page/ソフトウェア.md "wikilink")スイートである。[サーバ](../Page/サーバ.md "wikilink")、デスクトップ[PC](../Page/パーソナルコンピュータ.md "wikilink")、[ノートパソコン](../Page/ノートパソコン.md "wikilink")、携帯機器（[PDA](../Page/携帯情報端末.md "wikilink")）の[ライフサイクル](https://ja.wikipedia.org/wiki/ライフサイクル "wikilink")全体を管理する。ZENworksは各種サーバプラットフォームをサポートし、複数の[ディレクトリ・サービス](https://ja.wikipedia.org/wiki/ディレクトリ・サービス "wikilink")に対応している。

## 歴史

ZEWNworksはノベルが[インテル](https://ja.wikipedia.org/wiki/インテル "wikilink")のLANdesk Managerのライセンス提供を受けて販売した製品がベースとなっている。[ディレクトリ・サービス](https://ja.wikipedia.org/wiki/ディレクトリ・サービス "wikilink")に対応した時点でノベルはこれを **NAL** (**Novell Application Launcher**) と改称した。NALは成功し、様々な機能拡張が行われ、"ZENworks" と改称された（["Zero Effort Networks"](http://support.novell.com/techcenter/articles/ana19980502.html) に由来する名称）。"Novell Application Launcher" という名称はサービス名として残っており、パッケージ内にもNAL-で始まる名前のプログラムが多数存在する。

ZENworks の最初の製品は ZENworks 1.0 と ZENworks Starter Pack であった（後者は 1.0 の機能限定版で、後に [NetWare](https://ja.wikipedia.org/wiki/NetWare "wikilink") 5.0 に同梱された）。ノベルはサーバ管理機能を追加し、製品は "ZENworks for Desktops" (ZfD) と "ZENworks for Servers" (ZfS) からなるスイートに成長した。その後もノベルはコンポーネントを追加していき、全体を "ZENworks Suite" と呼ぶようになった。

## 機能

ZENworks は以下の9つのパッケージから構成され、それぞれ独立して動作する。

  - **デスクトップ管理** ("ZENworks Desktop Management", **ZDM**) は、Windows搭載のデスクトップPCやノートPCをポリシー駆動型の自動化によって集中管理するもので、ソフトウェアインストール、設定、ハードディスクイメージ、資産情報、トラブルシューティングなどの機能がある。
      - デスクトップ管理でインストールされたソフトウェアパッケージには自己修復機能があり、オンデマンドでインストール可能。
      - [MSIパッケージと](../Page/Microsoft_Windows_Installer.md "wikilink")[グループポリシー](https://ja.wikipedia.org/wiki/グループポリシー "wikilink")もサポートしている。
  - **パーソナリティマイグレーション**は、現在は[CAが所有するDesktopDNAを修正したバージョン](https://ja.wikipedia.org/wiki/CA_\(企業\) "wikilink")。文書や設定をWindowsのバージョンに関わらず Windows マシン間で移行できる。
  - **ソフトウェアパッケージング**は、[マクロヴィジョン](https://ja.wikipedia.org/wiki/マクロヴィジョン "wikilink")のAdminStudioの特別版。配布のためのMSIパッケージを作成できる。
  - **データ管理**は、ノベルの[iFolder](https://ja.wikipedia.org/wiki/iFolder "wikilink")ベースのソフトウェア。[クライアントサーバモデル](../Page/クライアントサーバモデル.md "wikilink")の[ファイル同期](../Page/ファイル同期.md "wikilink")を行う。
  - **パッチ管理**は、自動[パッチ](https://ja.wikipedia.org/wiki/パッチ "wikilink")管理ソフトウェア。ノベルが運営する Windows、Linux、その他のUNIXプラットフォームのパッチを集めたサイトとやり取りし、企業内のパッチ適用状況の管理、パッチの自動配布などを行う。
  - **Linux管理**は、[Red Carpet](https://ja.wikipedia.org/wiki/Red_Carpet "wikilink") をベースとしたもの（バージョン 6.6.2 まで）で、[Linux](https://ja.wikipedia.org/wiki/Linux "wikilink")マシンでの[RPMパッケージの管理を行う](https://ja.wikipedia.org/wiki/RPM_Package_Manager "wikilink")。バージョン7で完全に書き換えられ、資産管理、ポリシー適用、システム可視化などの機能が追加された。ノベルは、[SUSE](../Page/SUSE.md "wikilink") Linux 製品のセキュリティパッチやバグ修正を RPM パッケージの形式で提供している。
  - **サーバ管理**は、ポリシー駆動型自動化によって各種サーバを遠隔から管理する。
  - **ハンドヘルド管理**は、[Palm](../Page/Garnet_OS.md "wikilink")、[Windows CE](https://ja.wikipedia.org/wiki/Microsoft_Windows_CE "wikilink")、[Pocket PC](https://ja.wikipedia.org/wiki/Pocket_PC "wikilink")、[BlackBerry](https://ja.wikipedia.org/wiki/BlackBerry "wikilink") といった機器の遠隔からの更新・設定・インベントリなどを行う。
  - **資産管理**は、ハードウェアおよびソフトウェアのインベントリを扱う。

## システム諸元

### 管理対象プラットフォーム及び機器

  - デスクトップ管理
      - Windows 7
      - Windows Vista
      - Windows XP
      - Windows 2000 Professional SP4
      - Windows 98 SE
      - Citrix XenApp MetaFrame XP
      - Citrix XenApp 5.0
      - Citrix XenApp 6.0

<!-- end list -->

  - サーバ管理
      - NetWare 5.1, NetWare 6, NetWare 6.5
      - Novell Open Enterprise Server
      - Windows 2000 Server, Windows Server 2003, Windows Server 2008, Windows Server 2008 R2, Windows 2012 Server, 2012 Server R2, Windows 2016 Server, Enterprise Server 8 / 9 / 10 / 11 / 12
      - Red Hat Server 2.1
      - Red Hat Enterprise Linux AS 3 / 4 / 5, Red Hat Enterprise Linux ES 3 / 4 / 5
      - Solaris 9
  - Linux管理
      - Novell Linux Desktop SP1, x86, x86_64, x86_EM64T
      - Novell Open Enterprise Server, x86
      - SUSE LINUX Enterprise Server 9 SP1 x86, x86_64, x86_EM64T
      - SUSE LINUX Professional 9.3, x86, x86_64, x86_EM64T
      - SUSE LINUX Desktop 10 / 11
      - Red Hat Enterprise Linux 4.0 AS, ES, WS, x86
  - ハンドヘルド管理
      - Palm OS 3.5 以降
      - Windows CE 2.11 以降（Pocket PC も）
      - BlackBerry 850/857, BlackBerry 950/957

### 管理サーバプラットフォーム

\[1\]

  - デスクトップ管理
      - NetWare 6.5 SP1
      - NetWare 6 SP4
      - Windows 2000 Server SP4
      - Windows Server 2003, 2008 SP1,SP2, 2008 R2, Windows 2012 Server, Windows 2012 R2 Server,Windows 2016 Server,
      - SUSE LINUX Enterprise Server 9 SP1, 10 SP2, 11 SP1, SLED 12
      - RedHat Linux 5.3, 5,4, 5.5
  - サーバ管理
      - NetWare 5.1, NetWare 6, NetWare 6.5
      - Windows 2000 Server, Windows Server 2003
      - SUSE LINUX Enterprise Server 8 / 9
      - Red Hat Advanced Server 2.1, Red Hat Enterprise Server 2.1
      - Red Hat Enterprise Linux AS 3 / 4, Red Hat Enterprise Linux ES 3 / 4
  - Linux管理
      - SUSE LINUX Enterprise Server 9 SP1 x86 / SLES 11 / SLES 12 / SLES for SAP Applications 12, SLES 15 / SLES For SAP Applications 15 / Open Enterprise Server 11 / Open Enterprise Server 2015 / Open Enterprise Server 2018 / openSUSE Leap 42.3、42.4 / 15
  - ハンドヘルド管理
      - Windows 2000 server / workstation
      - Windows Server 2003
  - 構成管理
      - Windows 2000 Server
      - Windows 2003 Server
      - SuSE Linux Enterprise Server 10 SP1
      - Open Enterprise Server 2 (Linux)

### サポートされているディレクトリサービス

  - [NetIQ eDirectory](https://ja.wikipedia.org/wiki/NetIQ_eDirectory "wikilink")
  - [Microsoft Active Directory](https://ja.wikipedia.org/wiki/Active_Directory "wikilink")
  - [Lightweight Directory Access Protocol](../Page/Lightweight_Directory_Access_Protocol.md "wikilink") LDAP v3

## 脚注

## 参考文献

  -
  -
  -
  -
  -
## 関連項目

  - [システム管理](../Page/システム管理.md "wikilink")

## 外部リンク

  - [ZENworks 製品ページ](https://www.microfocus.com/ja-jp/products/zenworks/)

[Category:システム管理](https://ja.wikipedia.org/wiki/Category:システム管理 "wikilink") [Category:遠隔管理ソフトウェア](https://ja.wikipedia.org/wiki/Category:遠隔管理ソフトウェア "wikilink")

1.  <https://www.novell.com/ja-jp/documentation/zenworks-2017-update-4/pdfdoc/zen_system_requirements/zen_system_requirements.pdf>
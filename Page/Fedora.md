> この記事は[Fedora](https://ja.wikipedia.org/wiki/Fedora)から翻訳されています。


**Fedora**（フェドラ - [国際発音記号](https://ja.wikipedia.org/wiki/国際発音記号 "wikilink") \[\]）は、[レッドハット](../Page/レッドハット.md "wikilink")が支援するコミュニティー「[Fedora Project](https://ja.wikipedia.org/wiki/Fedora_Project "wikilink")」によって開発されている[RPM系](https://ja.wikipedia.org/wiki/RPM_Package_Manager "wikilink")[Linuxディストリビューション](../Page/Linuxディストリビューション.md "wikilink")である。バージョン6までは**Fedora Core**と呼ばれていた。特定のバージョンを指す場合は「Fedora 9」のように、バージョン番号を添えて呼ばれることもある。

## 概要

Fedoraは最新の技術を積極的に取り込む事で知られている。現在はRawhideと呼ばれる[ローリング・リリース](https://ja.wikipedia.org/wiki/ローリング・リリース "wikilink")版も用意している。また開発目的として「rapid progress of Free and Open Source software（フリー／オープンソースソフトウェアの世界を迅速に発展させること）」を謳っており\[1\]、[フリーソフトウェア](../Page/フリーソフトウェア.md "wikilink")を厳格に重視した一面も持っている。

[2003年](../Page/2003年.md "wikilink")末、開発が終了した[Red Hat Linuxの後継を開発するためにFedora](../Page/Red_Hat_Linux.md "wikilink") Projectが結成された。レッドハットは企業向けの[Red Hat Enterprise Linux](https://ja.wikipedia.org/wiki/Red_Hat_Enterprise_Linux "wikilink") (RHEL) のみをサポートしていくこととなり、Fedoraはコミュニティ主導となった。これにより高度な開発を柔軟に行うことができ、その成果が[RHELに取り込まれる等](https://ja.wikipedia.org/wiki/Red_Hat_Enterprise_Linux "wikilink")、検証目的の位置づけである\[2\]。

## パッケージ管理

パッケージ管理ツールには [DNF](https://ja.wikipedia.org/wiki/DNF_\(ソフトウェア\) "wikilink") または [Yellowdog Updater Modified](https://ja.wikipedia.org/wiki/Yellowdog_Updater_Modified "wikilink") (Yum) が採用されている。Fedora 22よりYumはDNFに置き換えられた。将来的にYumは廃止される予定であり、段階的にDNFへと置き換えられている。

Fedora Core 4まではYumに加えて、Red Hat Linuxのパッケージ更新ツール「[up2date](https://ja.wikipedia.org/wiki/up2date "wikilink")」も利用可能であったがFedora Core 5で削除されている。[Debian](../Page/Debian.md "wikilink")などが採用している[APT](https://ja.wikipedia.org/wiki/APT "wikilink")も使用できるが、[AMD64](https://ja.wikipedia.org/wiki/x64 "wikilink")[アーキテクチャ](https://ja.wikipedia.org/wiki/アーキテクチャ "wikilink")で必要となる「マルチアーキテクチャ環境」（対象アーキテクチャの異なるパッケージが混在する環境）に対応していないので使用は推奨されていない。[Mandriva Linuxなどで採用している](https://ja.wikipedia.org/wiki/Mandriva_Linux "wikilink")[Smart も使用可能である](https://ja.wikipedia.org/wiki/Mandriva_Linux#Smartパッケージ・マネージャ "wikilink")。

## リポジトリ

初めから利用できる公式のリポジトリの他に、RPM FusionやLivna等のコミュニティによって運営されているリポジトリ、[Adobe](https://ja.wikipedia.org/wiki/Adobe "wikilink")や[Dropbox](https://ja.wikipedia.org/wiki/Dropbox "wikilink")などの[サードパーティー](https://ja.wikipedia.org/wiki/サードパーティー "wikilink")製リポジトリもある。

  - Fedora Core/Extras

Fedora 7以前にはレッドハットの開発者により運営される公式リポジトリ**Fedora Core**（ディストリビューション名ではなくリポジトリ名）とは別に、コミュニティで運営される**Fedora Extras**というリポジトリが存在した。中核のパッケージはCoreで提供し、Extrasでは「追加パッケージ」を提供する位置づけであった。新規パッケージが簡単に追加できたため、従来非公式なリポジトリで提供されていた数多くのパッケージがここに収録された。当初はCoreしかレポジトリ登録されていなかったが、Fedora Core 3以降ではExtrasも利用可能となった。Fedora Core 4以降はYumにデフォルトで登録され、インストールすればすぐ利用できるようになっていた。Fedora 7でCoreと統合され、同時に名称が現在の**Fedora**に変更された。

  - RPM Fusion

Core統合後もFedoraの「フリーソフトウェア精神」に反する、あるいはアメリカ国内法に違反する恐れがあるために収録が見送られたコミュニティベースのリポジトリには「Dribble」「Freshrpms」「Livna」があったが、2008年にごく一部のパッケージを残して**RPM Fusion**として統合された。Fedora本体とは無関係にメンテナンスされている非公式のリポジトリである。オープンソースの「free」とそれ以外の「nonfree」に分かれてメンテナンスされており、後者には主に[GPU](https://ja.wikipedia.org/wiki/GPU "wikilink")ドライバなどの[プロプライエタリ](https://ja.wikipedia.org/wiki/プロプライエタリ "wikilink")ソフトウェア、または[MP3](../Page/MP3.md "wikilink")や動画再生関連のライブラリなどが収録されている。

## 非難

2007年2月、OSIの創設者である[エリック・レイモンド](../Page/エリック・レイモンド.md "wikilink")はFedoraの開発メーリングリストに「*Goodbye, Fedora*」と題するメールを投稿した\[3\]。ガバナンスがうまくいっていない、RPM開発を停滞させておりYumを遅くバグの多いままにしている、プロプライエタリなフォーマット非対応の問題が処理できていない等の非難があり、近年台頭してきた[Ubuntu](https://ja.wikipedia.org/wiki/Ubuntu "wikilink")への支持が表明された。これは大きな議論を引き起こした。レッドハットのグレッグ・デ・コーニグズバーグはFedoraとUbuntuの方向性の違いを指摘し、Ubuntuがプロプライエタリなコードをサポートしていることで多くの犠牲を払っていると反論している\[4\]。

## バージョン履歴

  - Fedora Core 1
    コードネーム: Yarrow, Cambridge
    最初のバージョンのFedoraであり、[2003年](../Page/2003年.md "wikilink")[11月6日](../Page/11月6日.md "wikilink")にリリースされた。コードネーム"Yarrow"は英語で[セイヨウノコギリソウ](https://ja.wikipedia.org/wiki/セイヨウノコギリソウ "wikilink")のこと。Red Hat Linux 9から改善されたシステム環境はYumによる自動アップデート、プレリンクによるプログラムの起動時間を短縮、主にノートパソコン用の[ACPIや](https://ja.wikipedia.org/wiki/Advanced_Configuration_and_Power_Interface "wikilink")[cpufreq](https://ja.wikipedia.org/wiki/cpufreq "wikilink")をサポートするなどがあり、[NPTLに対応したカーネルを採用している](https://ja.wikipedia.org/wiki/Native_POSIX_Thread_Library "wikilink")。翌年には[x86 64用もリリースされた](https://ja.wikipedia.org/wiki/x64 "wikilink")。
  - Fedora Core 2
    コードネーム: Tettnang
    [2004年](https://ja.wikipedia.org/wiki/2004年 "wikilink")[5月17日](../Page/5月17日.md "wikilink")にリリースされ、コードネーム"Tettnang"はドイツ南部の町の名前である。[Linuxカーネル](../Page/Linuxカーネル.md "wikilink")のバージョンが2.6にあげられ、[強制アクセス制御](https://ja.wikipedia.org/wiki/強制アクセス制御 "wikilink")である[SELinuxの実装が施された](https://ja.wikipedia.org/wiki/Security-Enhanced_Linux "wikilink")。このバージョンからデフォルトの[インプットメソッド](../Page/インプットメソッド.md "wikilink")フレームワークに[IIIMF](https://ja.wikipedia.org/wiki/IIIMF "wikilink")が採用された。
  - Fedora Core 3
    コードネーム: Heidelberg
    [2004年](https://ja.wikipedia.org/wiki/2004年 "wikilink")[11月8日](../Page/11月8日.md "wikilink")にリリースされ、コードネーム"[Heidelberg](../Page/ハイデルベルク.md "wikilink")"はドイツの都市の名前である。[ブート](https://ja.wikipedia.org/wiki/ブート "wikilink")ローダが[LILO](https://ja.wikipedia.org/wiki/LILO "wikilink")から[GRUBに切り替えられ](https://ja.wikipedia.org/wiki/GNU_GRUB "wikilink")、[ウェブブラウザ](../Page/ウェブブラウザ.md "wikilink")に[Mozilla Firefoxを採用した](../Page/Mozilla_Firefox.md "wikilink")。また、SELinuxが既定で有効になるように設定が改められた。
  - Fedora Core 4
    コードネーム: Stentz
    [2005年](https://ja.wikipedia.org/wiki/2005年 "wikilink")[6月13日](../Page/6月13日.md "wikilink")にリリースされた。準備期間に[Linuxカーネル](../Page/Linuxカーネル.md "wikilink")の不具合が発見されたため大幅にリリースが遅れ、[2005年](https://ja.wikipedia.org/wiki/2005年 "wikilink")[4月11日](../Page/4月11日.md "wikilink")にテスト版を公開、同年[6月](../Page/6月.md "wikilink")のリリースとなった。[PowerPC](../Page/PowerPC.md "wikilink")に対応し[Macintosh](../Page/Macintosh.md "wikilink")においても動作が可能になった。
  - Fedora Core 5
    コードネーム: Bordeaux
    [2006年](https://ja.wikipedia.org/wiki/2006年 "wikilink")3月20日にリリースされ、コードネーム"[Bordeaux](../Page/ボルドー.md "wikilink")"はフランス南西部の都市の名前である。[GCC](../Page/GNUコンパイラコレクション.md "wikilink") 4.1, [GNOME](../Page/GNOME.md "wikilink") 2.14が採用されたほか、リリース4で不十分だった[Xenのサポートが改善されている](https://ja.wikipedia.org/wiki/Xen_\(仮想化ソフトウェア\) "wikilink")。また、[IIIMF](https://ja.wikipedia.org/wiki/IIIMF "wikilink")に代わって[SCIM](https://ja.wikipedia.org/wiki/SCIM "wikilink")がデフォルトのインプットメソッドフレームワークとなり、併せてかな漢字変換エンジン[Anthy](https://ja.wikipedia.org/wiki/Anthy "wikilink")が採用されて日本語入力環境も大きく改善された。オープンソースの.NET処理系である[Monoも収録されている](https://ja.wikipedia.org/wiki/Mono_\(ソフトウェア\) "wikilink")。その他無線LANサポート、電源管理、ソフトウェアサスペンド、[Beagle](https://ja.wikipedia.org/wiki/Beagle "wikilink")の追加等様々な改良が加えられた。
  - Fedora Core 6
    コードネーム: Zod
    [2006年](https://ja.wikipedia.org/wiki/2006年 "wikilink")[10月24日](../Page/10月24日.md "wikilink")リリースされた。[GNOME](../Page/GNOME.md "wikilink") 2.16の採用。[ウィンドウマネージャ](https://ja.wikipedia.org/wiki/ウィンドウマネージャ "wikilink")に[Compiz](https://ja.wikipedia.org/wiki/Compiz "wikilink")([AIGLX](https://ja.wikipedia.org/wiki/AIGLX "wikilink")上で動作)を採用し、3Dの画面効果が得られる。また、インストーラ[Anacondaに大幅な改善がなされた](https://ja.wikipedia.org/wiki/Anaconda_\(インストーラー\) "wikilink")。[Intel Macをサポート](https://ja.wikipedia.org/wiki/Intel_Mac "wikilink")。
  - Fedora 7
    コードネーム: Moonshine
    [2007年](https://ja.wikipedia.org/wiki/2007年 "wikilink")[5月31日](../Page/5月31日.md "wikilink")リリースされ、コードネーム"Moonshine"は「月光」のこと。Fedora ExtrasがFedora Coreに吸収され、パッケージ分類を一本化した。これに伴いOSの名称はFedoraに変更された。ディスクイメージはDVDのみとなり、CDについてはLiveCDのみが配布された。GNOME 2.18、KDE 3.5.6、Xorg 7.2.0が採用された。
  - Fedora 8
    コードネーム: Werewolf
    [2007年](https://ja.wikipedia.org/wiki/2007年 "wikilink")[11月8日](../Page/11月8日.md "wikilink")リリースされ、コードネーム"Werewolf"は「[狼男](https://ja.wikipedia.org/wiki/狼男 "wikilink")」のこと。オープンソースの[Java](https://ja.wikipedia.org/wiki/Java "wikilink")開発環境「[IcedTea](https://ja.wikipedia.org/wiki/IcedTea "wikilink")」を収録。GNOME 2.20.1、KDE 3.5.8、Xorg 7.3.0が採用。
  - Fedora 9
    コードネーム: Sulphur
    [2008年](https://ja.wikipedia.org/wiki/2008年 "wikilink")[5月14日](../Page/5月14日.md "wikilink")にリリースされ、コードネーム"Sulphur"は「[硫黄](../Page/硫黄.md "wikilink")」のこと。[ext4](https://ja.wikipedia.org/wiki/ext4 "wikilink")ファイルシステムのサポート、インストール時のパーティションサイズ変更機能、Gnome 2.21、KDE 4.0が採用された。
  - Fedora 10
    コードネーム: Cambridge
    [2008年](https://ja.wikipedia.org/wiki/2008年 "wikilink")[11月25日](../Page/11月25日.md "wikilink")にリリースされ、コードネーム"Cambridge"は[イギリス](https://ja.wikipedia.org/wiki/イギリス "wikilink")の都市[ケンブリッジ](https://ja.wikipedia.org/wiki/ケンブリッジ "wikilink")のこと。[無線LAN](../Page/無線LAN.md "wikilink")接続や[モバイルブロードバンド](https://ja.wikipedia.org/wiki/モバイルブロードバンド "wikilink")接続を、ほかのユーザーと無線LANで共有できる機能などの新機能を搭載し、仮想化の強化、OS起動の高速化を実現している。Linuxカーネル2.6.27、OpenOffice 3.0、GNOME 2.24.1、GIMP 2.6が採用された。
  - Fedora 11
    コードネーム: Leonidas
    [2009年](../Page/2009年.md "wikilink")[6月9日](../Page/6月9日.md "wikilink")にリリースされ、コードネーム"Leonidas"は[古代ギリシア](../Page/古代ギリシア.md "wikilink")の[スパルタ王](https://ja.wikipedia.org/wiki/スパルタ王 "wikilink")のこと。
  - Fedora 12
    コードネーム: Constantine
    [2009年](../Page/2009年.md "wikilink")[11月17日](../Page/11月17日.md "wikilink")にリリースされた。
    PowerPC版はこれが最後のリリースとなった。
  - Fedora 13
    コードネーム: Goddard
    [2010年](https://ja.wikipedia.org/wiki/2010年 "wikilink")[5月25日](../Page/5月25日.md "wikilink")にリリースされ、コードネーム"Goddard"は[アメリカ](https://ja.wikipedia.org/wiki/アメリカ "wikilink")のロケット開発者[ロバート・ゴダード](https://ja.wikipedia.org/wiki/ロバート・ゴダード "wikilink")のこと。
  - Fedora 14
    コードネーム: Laughlin
    [2010年](https://ja.wikipedia.org/wiki/2010年 "wikilink")[11月2日](../Page/11月2日.md "wikilink")にリリースされ、コードネーム"Laughlin"は[アメリカ](https://ja.wikipedia.org/wiki/アメリカ "wikilink")の理論物理学者[ロバート・B・ラフリン](https://ja.wikipedia.org/wiki/ロバート・B・ラフリン "wikilink")のこと。
  - Fedora 15
    コードネーム: Lovelock
    [2011年](../Page/2011年.md "wikilink")[5月24日](../Page/5月24日.md "wikilink")にリリースされ、コードネーム"Lovelock"は[アメリカ](https://ja.wikipedia.org/wiki/アメリカ "wikilink")ネバダ州の都市の名前である。Linuxカーネル2.6.38、GNOME 3が採用された。
  - Fedora 16
    コードネーム: Verne
    [2011年](../Page/2011年.md "wikilink")[11月8日](../Page/11月8日.md "wikilink")にリリースされ、コードネーム"Verne"は[フランス](https://ja.wikipedia.org/wiki/フランス "wikilink")の小説家[ジュール・ヴェルヌ](../Page/ジュール・ヴェルヌ.md "wikilink")のこと。Linuxカーネル3.1、GNOME 3.2が採用された。
  - Fedora 17
    コードネーム: Beefy Miracle
    [2012年](../Page/2012年.md "wikilink")[5月29日](../Page/5月29日.md "wikilink")リリース。コードネーム"Beefy Miracle"は「力強い奇跡」を意味する。Linuxカーネル3.3.4、GNOME 3.4が採用された。
  - Fedora 18
    コードネーム: Spherical Cow
    [2013年](../Page/2013年.md "wikilink")[1月15日](../Page/1月15日.md "wikilink")リリース。コードネーム"Spherical Cow"は「[球形の牛](https://ja.wikipedia.org/wiki/球形の牛 "wikilink")」を意味する。Linuxカーネル3.6.10、GNOME 3.6が採用された。試験的な[パッケージ管理システム](https://ja.wikipedia.org/wiki/パッケージ管理システム "wikilink")として、[DNFが導入された](https://ja.wikipedia.org/wiki/DNF_\(ソフトウェア\) "wikilink")（標準としての本格的な搭載は、Fedora 22からである）。
  - Fedora 19
    コードネーム: Schrödinger's Cat
    [2013年](../Page/2013年.md "wikilink")[7月2日](../Page/7月2日.md "wikilink")リリース。コードネーム"Schrödinger's Cat"は量子論の思考実験「[シュレーディンガーの猫](../Page/シュレーディンガーの猫.md "wikilink")」より。Linuxカーネル3.9.5、GNOME 3.8が採用された。
  - Fedora 20
    コードネーム: Heisenbug
    [2013年](../Page/2013年.md "wikilink")[12月17日](../Page/12月17日.md "wikilink")リリース。コードネーム"Heisenbug"はソフトウェア[バグ](https://ja.wikipedia.org/wiki/バグ "wikilink")の一種である「[ハイゼンバグ](https://ja.wikipedia.org/wiki/特異なバグ "wikilink")」より。Linuxカーネル3.11.10、GNOME 3.10が採用された。
  - Fedora 21
    [2014年](../Page/2014年.md "wikilink")[12月9日](../Page/12月9日.md "wikilink")(米国時間)リリース。コードネームは廃止された\[5\]。Fedoraのモジュラー化を進める「Fedora.next」イニシアティブで開発された初のバージョン。Linuxカーネル3.17、GNOME 3.14が採用された。
  - Fedora 22
    [2015年](../Page/2015年.md "wikilink")[5月26日](../Page/5月26日.md "wikilink")(米国時間)リリース。標準の[パッケージ管理システム](https://ja.wikipedia.org/wiki/パッケージ管理システム "wikilink")として、[DNFが採用された](https://ja.wikipedia.org/wiki/DNF_\(ソフトウェア\) "wikilink")。Linuxカーネル4.0、GNOME 3.16が採用された。
  - Fedora 23
    [2015年](../Page/2015年.md "wikilink")[11月3日](https://ja.wikipedia.org/wiki/11月3日 "wikilink")(米国時間)リリース。「[Wayland](https://ja.wikipedia.org/wiki/Wayland "wikilink")」をオプションで有効にできるようになった。Linuxカーネル4.2、GNOME 3.18が採用された。

<!-- end list -->

  - Fedora 24
    [2016年](../Page/2016年.md "wikilink")[6月21日](../Page/6月21日.md "wikilink")(米国時間)リリース。一度ビルドしたデスクトップアプリケーションを他のLinuxディストリビューション上でもインストール/動作可能な状態にする[Flatpak](https://ja.wikipedia.org/wiki/Flatpak "wikilink")（旧名"xdg-app"）機能が追加された\[6\]。Linuxカーネル4.5.7、GNOME 3.20が採用された。なお当初予定されていたLinuxカーネル4.6系の対応については、6月30日にLinux 4.6.3へのバージョンアップのパッチにて対処されている\[7\]。

<!-- end list -->

  - Fedora 25
    [2016年](../Page/2016年.md "wikilink")[11月22日](https://ja.wikipedia.org/wiki/11月22日 "wikilink")(米国時間)リリース。従来の「[X Window System](../Page/X_Window_System.md "wikilink")」に替わる新しい[ウィンドウシステム](https://ja.wikipedia.org/wiki/ウィンドウシステム "wikilink")である「[Wayland](https://ja.wikipedia.org/wiki/Wayland "wikilink")」が正式に実装された\[8\]。Linuxカーネル4.8、GNOME 3.22が採用された。[Docker](https://ja.wikipedia.org/wiki/Docker "wikilink")1.12に対応し、プログラミング言語の[Rustを正式サポートした](https://ja.wikipedia.org/wiki/Rust_\(プログラミング言語\) "wikilink")。

<!-- end list -->

  - Fedora 26
    [2017年](../Page/2017年.md "wikilink")[7月12日](../Page/7月12日.md "wikilink")(米国時間)リリース。パッケージマネージャは「 DNF-2.0 」となり、コンパイラはGCC 7が標準となった\[9\]。Linuxカーネル4.11.8、GNOME 3.24が採用された。なおFedoraの開発の遅れを緩和する施策のひとつとして、Fedora Projectは本バージョンをもって、アルファ版の提供を取りやめることにした為、26が最後のアルファ版の提供が実施されたバージョンとなる\[10\]。

<!-- end list -->

  - Fedora 27
    [2017年](../Page/2017年.md "wikilink")[11月14日](../Page/11月14日.md "wikilink")(米国時間)に「Workstation」エディションと「Atomic」エディションがリリース\[11\]。アプリケーションとディストリビューションのライフサイクルを分離する為、モジュラー化を進めた。Linuxカーネル4.13、GNOME 3.26が採用された。32ビットのUEFIサポートが加わった。[2017年](../Page/2017年.md "wikilink")[12月11日](../Page/12月11日.md "wikilink")(米国時間)に[サーバ](../Page/サーバ.md "wikilink")ー向けエディションの「Server classic」エディションがリリース\[12\]。「Server classic」に関してはモジュラー化は一旦白紙になり、モジュラー化の作業は継続されるものの、基本的には従来のFedora Serverとは別のパッケージリポジトリとして開発される見通し。

<!-- end list -->

  - Fedora 28
    [2018年](../Page/2018年.md "wikilink")[5月1日](../Page/5月1日.md "wikilink")(米国時間)リリース。Linuxカーネル4.16、GNOME 3.28が採用された。「Server」エディションでは、デフォルトのリポジトリで提供されるソフトウェアとは異なるバージョンのソフトウェアを提供する「Modularリポジトリ」が新たに導入された\[13\]。[インテル](https://ja.wikipedia.org/wiki/インテル "wikilink")が開発したハードウェアインターフェイス「[Thunderbolt 3](https://ja.wikipedia.org/wiki/Thunderbolt "wikilink")」にも対応した。Thuderboltデバイスに安全に接続するためのシステムデーモンboltd、デバイス接続に必要なGNOME Shellの変更なども導入している。

<!-- end list -->

  - Fedora 29
    [2018年](../Page/2018年.md "wikilink")[10月30日](../Page/10月30日.md "wikilink")(米国時間)リリース。Linuxカーネル4.18、GNOME 3.30が採用された。サーバー向けの「Fedora 29 Server」、デスクトップの「Fedora 29 Workstation」、コンテナやクラウド向け「Fedora 29 Atomic Host」の3エディションに分かれる\[14\]。全エディションで「モジュラーリポジトリ」が利用できるようになった。これにより、OSを最新のものに維持しつつ、ディストリビューションのデフォルトバージョンが変更されても特定のバージョンのアプリケーションを使い続ける手法が可能となった\[15\]。

<!-- end list -->

  - Fedora 30
    [2019年](../Page/2019年.md "wikilink")[4月29日](../Page/4月29日.md "wikilink")(米国時間)リリース。Linuxカーネル5.0、GNOME 3.32が採用された。

<!-- end list -->

  - Fedora 31
    [2019年](../Page/2019年.md "wikilink")[10月29日](../Page/10月29日.md "wikilink")(米国時間)リリース。Linuxカーネル5.3、GNOME 3.34が採用された。32bit版は提供されなくなった\[16\]。

### バージョンのリスト

短いサイクルでリリースされているFedoraではメンテナンス期間も短くなっている。今日の規程では、あるバージョンについて2つ先のバージョンがリリースされてから1ヶ月後にメンテナンスされなくなる\[17\]。例えばFedora 12のリリースが2009年11月で、ふたつ前のバージョンであるFedora 10はその1ヶ月後の2009年12月にメンテナンスを終えた。バージョンアップは概ね半年ごとに行われているため、リリースされてから約13ヶ月後にメンテナンスが終了する傾向にある。

| 色 | 状況     |
| - | ------ |
|   | サポート終了 |
|   | サポート中  |
|   | 開発中    |

| バージョン | コードネーム            | リリース日       | サポート期限      | カーネルバージョン   |
| ----- | ----------------- | ----------- | ----------- | ----------- |
| 1     | Yarrow            | 2003年11月6日  | 2004年9月20日  | 2.4.22      |
| 2     | Tettnang          | 2004年5月17日  | 2005年4月11日  | 2.6.5       |
| 3     | Heidelberg        | 2004年11月8日  | 2006年1月16日  | 2.6.9       |
| 4     | Stentz            | 2005年6月13日  | 2006年8月7日   | 2.6.11      |
| 5     | Bordeaux          | 2006年3月20日  | 2007年7月2日   | 2.6.15      |
| 6     | Zod               | 2006年10月24日 | 2007年12月7日  | 2.6.18      |
| 7     | Moonshine         | 2007年5月31日  | 2008年6月13日  | 2.6.21      |
| 8     | Werewolf          | 2007年11月8日  | 2009年1月7日   | 2.6.23      |
| 9     | Sulphur           | 2008年5月14日  | 2009年7月10日  | 2.6.25      |
| 10    | Cambridge         | 2008年11月25日 | 2009年12月17日 | 2.6.27      |
| 11    | Leonidas          | 2009年6月9日   | 2010年6月25日  | 2.6.29      |
| 12    | Constantine       | 2009年11月17日 | 2010年12月2日  | 2.6.31      |
| 13    | Goddard           | 2010年5月25日  | 2011年6月24日  | 2.6.33      |
| 14    | Laughlin          | 2010年11月2日  | 2011年12月9日  | 2.6.35      |
| 15    | Lovelock          | 2011年5月24日  | 2012年6月26日  | 2.6.38      |
| 16    | Verne             | 2011年11月8日  | 2013年2月12日  | 3.1         |
| 17    | Beefy Miracle     | 2012年5月29日  | 2013年7月30日  | 3.3         |
| 18    | Spherical Cow     | 2013年1月15日  | 2014年1月14日  | 3.6         |
| 19    | Schrödinger's Cat | 2013年7月2日   | 2015年1月6日   | 3.9         |
| 20    | Heisenbug         | 2013年12月17日 | 2015年6月23日  | 3.11        |
| 21    | \-\[18\]          | 2014年12月9日  | 2015年12月1日  | 3.17        |
| 22    | \-                | 2015年5月26日  | 2016年7月19日  | 4.0         |
| 23    | \-                | 2015年11月3日  | 2016年12月20日 | 4.2         |
| 24    | \-                | 2016年6月21日  | 2017年8月8日   | 4.5.7\[19\] |
| 25    | \-                | 2016年11月22日 | 2017年12月12日 | 4.8         |
| 26    | \-                | 2017年7月11日  | 2018年5月29日  | 4.11        |
| 27    | \-                | 2017年11月14日 | 2018年11月27日 | 4.13        |
| 28    | \-                | 2018年5月1日   | 2019年5月29日  | 4.16        |
| 29    | \-                | 2018年10月30日 | 2019年11月26日 | 4.18        |
| 30    | \-                | 2019年4月29日  |             | 5.0         |
| 31    | \-                | 2019年10月29日 |             | 5.3         |
| 32    | \-                |             |             |             |

Fedoraのバージョン・サポート期限一覧表

<div style="overflow:auto">

{{\#tag:timeline | Define $width = 1120 Define $height = 630 ImageSize = width:$width height:$height PlotArea = right:10 left:30 bottom:70 top:40

DateFormat = dd/mm/yyyy Define $start = 01/01/2003 Define $now = {{\#time: d/m/Y}} Period = from:$start till:$now

Colors =

` id:monthline value:gray(0.9)`
` id:yearline value:gray(0.5)`
` id:Development value:gray(0.55) Legend:Development # from the release of test1 or alpha until general availability`
` id:Support value:rgb(0.24,0.43,0.71) Legend:Support # from general availability until end of support`

TimeAxis = orientation:horizontal Legend = orientation:horizontal ScaleMajor = gridcolor:yearline unit:year increment:1 start:$start ScaleMinor = gridcolor:monthline unit:month increment:3 start:$start

TextData =

` pos:(365,$height)`
` fontsize:XL`
` text:"Fedora Release Timeline"`

PlotData=

` width:18`
` textcolor:white`
` align:center`
` shift:(0,-5)`

` # `<http://fedoraproject.org/wiki/Releases/HistoricalSchedules>

` bar:31`
`   color:Development from:17/09/2019 till:29/10/2019`
`   color:Support from:29/10/2019 till:$now text:"31"`

` bar:30`
`   color:Development from:02/04/2019 till:29/04/2019`
`   color:Support from:29/04/2019 till:$now text:"30"`

` bar:29`
`   color:Development from:25/09/2018 till:30/10/2018`
`   color:Support from:30/10/2018 till:26/11/2019 text:"29"`

` bar:28`
`   color:Development from:03/04/2018 till:01/05/2018`
`   color:Support from:01/05/2018 till:29/05/2019 text:"28"`

` bar:27`
`   color:Development from:03/10/2017 till:14/11/2017`
`   color:Support from:14/11/2017 till:27/11/2018 text:"27"`

` bar:26`
`   color:Development from:04/04/2017 till:11/07/2017`
`   color:Support from:11/07/2017 till:29/05/2018 text:"26"`

` bar:25`
`   color:Development from:30/08/2016 till:22/11/2016`
`   color:Support from:22/11/2016 till:12/12/2017 text:"25"`

` bar:24`
`   color:Development from:29/03/2016 till:21/06/2016`
`   color:Support from:21/06/2016 till:08/08/2017 text:"24"`

` bar:23`
`   color:Development from:11/08/2015 till:03/11/2015`
`   color:Support from:03/11/2015 till:20/12/2016 text:"23"`

` bar:22`
`   color:Development from:10/03/2015 till:26/05/2015`
`   color:Support from:26/05/2015 till:19/07/2016 text:"22"`

` bar:21`
`   color:Development from:23/09/2014 till:09/12/2014`
`   color:Support from:09/12/2014 till:01/12/2015 text:"21"`

` bar:20`
`   color:Development from:24/09/2013 till:17/12/2013`
`   color:Support from:17/12/2013 till:23/06/2015 text:"20 Heisenbug"`

` bar:19`
`   color:Development from:23/04/2013 till:02/07/2013`
`   color:Support from:02/07/2013 till:06/01/2015 text:"19 Schrödinger's Cat"`

` bar:18`
`   color:Development from:18/09/2012 till:15/01/2013`
`   color:Support from:15/01/2013 till:17/01/2014 text:"18 Spherical Cow"`

` bar:17`
`   color:Development from:28/02/2012 till:29/05/2012`
`   color:Support from:29/05/2012 till:30/07/2013 text:"17 Beefy Miracle"`

` bar:16`
`   color:Development from:23/08/2011 till:08/11/2011`
`   color:Support from:08/11/2011 till:12/02/2013 text:"16 Verne"`

` bar:15`
`   color:Development from:08/03/2011 till:24/05/2011`
`   color:Support from:24/05/2011 till:24/06/2012 text:"15 Lovelock"`

` bar:14`
`   color:Development from:24/08/2010 till:02/11/2010`
`   color:Support from:02/11/2010 till:27/11/2011 text:"14 Laughlin"`

` bar:13`
`   color:Development from:09/03/2010 till:25/05/2010`
`   color:Support from:25/05/2010 till:24/06/2011  text:"13 Goddard"`

` bar:12`
`   color:Development from:25/08/2009 till:17/11/2009`
`   color:Support from:17/11/2009 till:02/12/2010 text:"12 Constantine"`

` bar:11`
`   color:Development from:05/02/2009 till:09/06/2009`
`   color:Support from:09/06/2009 till:25/06/2010 text:"11 Leonidas"`

` bar:10`
`   color:Development from:05/08/2008 till:25/11/2008`
`   color:Support from:25/11/2008 till:18/12/2009 text:"10 Cambridge"`

` bar:9`
`   color:Development from:05/02/2008 till:13/03/2008`
`   color:Support from:13/03/2008 till:10/07/2009 text:"9 Sulphur"`

` bar:8`
`   color:Development from:07/08/2007 till:08/11/2007`
`   color:Support from:08/11/2007 till:07/01/2009 text:"8 Werewolf"`

` bar:7`
`   color:Development from:01/02/2007 till:31/03/2007`
`   color:Support from:31/03/2007 till:13/06/2008 text:"7 Moonshine"`

` bar:6`
`   color:Development from:21/06/2006 till:24/10/2006`
`   color:Support from:24/10/2006 till:07/12/2007 text:"6 Zod"`

` bar:5`
`   color:Development from:23/11/2005 till:20/03/2006`
`   color:Support from:20/03/2006 till:02/07/2007 text:"5 Bordeaux"`

` bar:4`
`   color:Development from:15/03/2005 till:13/06/2005`
`   color:Support from:13/06/2005 till:07/08/2006 text:"4 Stentz"`

` bar:3`
`   color:Development from:13/07/2004 till:08/11/2004`
`   color:Support from:08/11/2004 till:16/01/2006 text:"3 Heidelberg"`

` bar:2`
`   color:Development from:12/02/2004 till:18/03/2004`
`   color:Support from:18/03/2004 till:11/04/2005 text:"2 Tettnang"`

` bar:1`
`   color:Development from:21/07/2003 till:05/11/2003`
`   color:Support from:05/11/2003 till:20/09/2004 text:"1 Yarrow"`

}}

</div>

### スクリーンショット

Image:Fedora Core 4 Gnome-sk.jpg|Fedora Core 4 デスクトップ (GNOME) Image:Fedora Core 5 desktop.png|Fedora Core 5 デスクトップ (GNOME) Image:Fedora Core 6 Desktop.png|Fedora Core 6 デスクトップ (GNOME) Image:Fedora7 ja default.png|Fedora 7 デスクトップ (GNOME) Image:Bureau GNOME Fedora 8.png|Fedora 8 デスクトップ (GNOME) 画像:Fedora9ss.png|Fedora 9 デスクトップ (GNOME) 画像:Fedora 10 GNOME.png|Fedora 10 デスクトップ (GNOME) Image:Fedora_11_GNOME.png|Fedora 11 デスクトップ (GNOME) Image:Fedora_12_GNOME.png|Fedora 12 デスクトップ (GNOME) Image:Fedora_13_GNOME.png|Fedora 13 デスクトップ (GNOME) Image:Fedora_14_GNOME.png|Fedora 14 デスクトップ (GNOME) Image:Fedora_15_GNOME.png|Fedora 15 デスクトップ (GNOME)

## 関連プロジェクト

### 活動中

  - Fedora EPEL
    Red Hat Enterprise LinuxでFedoraと同等環境を実現する信頼性の高いパッケージの提供するRHEL用レポジトリ。目標のFedoraと同等環境にはほど遠いものの、多数の有用なパッケージが収録されている。正式名称はExtra Packages for Enterprise Linux。

### 活動停止

  - Fedora Core/Extras

<!-- end list -->

  - Fedora Legacy

旧[Red Hat Linuxとメンテナンスが終了したFedora](../Page/Red_Hat_Linux.md "wikilink") Coreのリリースを保守していた。プロジェクトは慢性的な人手不足に悩まされ、メンテナンス期間中のFedora Coreに比べてアップデートの提供スピードや頻度は低かった。[2007年](https://ja.wikipedia.org/wiki/2007年 "wikilink")[2月](https://ja.wikipedia.org/wiki/2月 "wikilink")にプロジェクトは解散。

## 注釈

## 脚注

## 関連項目

  - [Red Hat Enterprise Linux](https://ja.wikipedia.org/wiki/Red_Hat_Enterprise_Linux "wikilink")
  - [Fedora Project](https://ja.wikipedia.org/wiki/Fedora_Project "wikilink")
  - [CentOS](https://ja.wikipedia.org/wiki/CentOS "wikilink")
  - [Exec Shield](https://ja.wikipedia.org/wiki/Exec_Shield "wikilink")
  - [Linux](https://ja.wikipedia.org/wiki/Linux "wikilink")
  - [Linuxディストリビューションの比較](https://ja.wikipedia.org/wiki/Linuxディストリビューションの比較 "wikilink")
  - [Linuxライブディストリビューションの比較](https://ja.wikipedia.org/wiki/Linuxライブディストリビューションの比較 "wikilink")

## 外部リンク

  - [公式ダウンロードサイト](https://getfedora.org/ja/)
  - [質問フォーラム](https://ask.fedoraproject.org/en/questions/)（英語）
  - [公式リリーススケジュール](https://fedoraproject.org/wiki/Schedule)

[Category:Linuxディストリビューション](https://ja.wikipedia.org/wiki/Category:Linuxディストリビューション "wikilink") [Category:2003年のソフトウェア](https://ja.wikipedia.org/wiki/Category:2003年のソフトウェア "wikilink")

1.
2.  （リンク切れ、2015年11月26日に確認）
3.  <http://www.redhat.com/archives/fedora-devel-list/2007-February/msg01006.html>
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
19. Fedora 24では、当初2016年5月時点での最新カーネルであるLinux 4.6を実装する予定だったが，十分なテスト期間を取ることができなかったため、4.5の最新アップデートであるLinux 4.5.7が採用されている。なお、対応カーネルをLinux 4.6.3にアップデートしたパッチが6月30日に出されている。
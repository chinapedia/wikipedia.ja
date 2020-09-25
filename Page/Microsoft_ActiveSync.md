> この記事は[Microsoft ActiveSync](https://ja.wikipedia.org/wiki/Microsoft_ActiveSync)から翻訳されています。


**Microsoft ActiveSync**（**マイクロソフト アクティブシンク**）は、[マイクロソフト](../Page/マイクロソフト.md "wikilink")が同社の携帯端末向け[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink") (OS) である[Windows Mobile](../Page/Windows_Mobile.md "wikilink")、[Windows CE](../Page/Microsoft_Windows_Embedded_CE.md "wikilink")\[1\]を搭載した[携帯情報端末](../Page/携帯情報端末.md "wikilink") (PDA) と、[Windows搭載の](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")[パソコンを接続して情報のやりとりやソフトウエアのインストールを行うために提供しているソフトウエアである](../Page/パーソナルコンピュータ.md "wikilink")。パソコン上にインストールするほか、同社OS搭載のPDAには通常プリインストールされており、これもActiveSyncと言い、セットで運用される。パソコン版は2008年現在、無償配布のソフトウエアである。

本ソフトは、親となるパソコン上にインストールされている個人情報管理ソフトウエア (Microsoft Outlook) のデータをPDA上のデータベースと同期を取りPDA上で利用できるようにするほか、ファイルの転送やPDA上で扱えるようにファイルを変換したりソフトウエアのインストールを行うこともできる。また、PDAのデータのフルバックアップ機能も一部を除き提供されている。\[2\]さらに、[テザリング](https://ja.wikipedia.org/wiki/テザリング "wikilink")機能のためのホストとしても動作する。

なお、ActiveSyncという名称としてのソフトウエアは2012年現在、後継で同様の機能を提供する **Windows Mobile Device Center（Windows Mobile デバイス センター）** へ移行している。事実上、本ソフトウエアの代替となる後継ソフトウエアであるため、これについても本稿にて触れる。但し本稿の前半はActiveSyncについて詳述したものであるので、これについては後述の「次世代のActiveSync」の項等を参照されたい。

## デスクトップ アプリケーションとの同期

パソコンとの同期の対象となるデータは主に電子メール（受信トレイ）、タスクリスト（仕事）、予定表、連絡先、メモといった[個人情報管理](../Page/Personal_Information_Manager.md "wikilink") (PIM) データである。他に[Internet Explorerのお気に入りの一部や](../Page/Internet_Explorer.md "wikilink")[Microsoft Accessのデータファイル](../Page/Microsoft_Access.md "wikilink")、既定のフォルダにあるファイルの同期もサポートしている。(Windows CEのバージョンによっては一部サポートされない機能がある)

PIMデータの同期には[Microsoft Outlookや](../Page/Microsoft_Outlook.md "wikilink")[Microsoft Exchangeが対象となる](../Page/Microsoft_Exchange_Server.md "wikilink")。よく間違われるが[Outlook Expressとは同期を行うことはできない](https://ja.wikipedia.org/wiki/Outlook_Express "wikilink")。 [サードパーティー](../Page/サードパーティー.md "wikilink")製ソフトウエア（Intellisyncなど）の追加インストールによって、[Lotus Notesなどの他社製PIMソフトウエアとの同期が可能になる場合もある](https://ja.wikipedia.org/wiki/Lotus_Notes "wikilink")。

ActiveSyncをインストールすると、PDAと同期接続中[Windows Media Playerと機能の連携がなされる](../Page/Windows_Media_Player.md "wikilink")。\[3\] また、"マイコンピュータ"に"モバイル デバイス"としてPDAが現れ、ローカルドライブのようにPDA内のファイルを扱うことができる（ファイルシステムにマウントするわけではなく、仮想的なもの）。

## 接続方法とパートナーシップ

ActiveSyncは、[USB](../Page/ユニバーサル・シリアル・バス.md "wikilink")、[シリアルポート](../Page/シリアルポート.md "wikilink")、[IrDA](../Page/IrDA.md "wikilink")、ネットワーク（[イーサネット](../Page/イーサネット.md "wikilink")）、さらに[RAS接続等での接続をサポートしている](https://ja.wikipedia.org/wiki/Remote_Access_Service "wikilink")（少なくともネットワーク接続はバージョン4以降利用できなくなっている）。

使用する際は、利用するPDAをActiveSyncに登録する必要がある。これを行うことで初めてPIMデータなどの同期が行える仕組みになっている。このパソコンとPDAの関係を"パートナーシップ"と呼んでいる。 このソフトウエアのインストール後、PDAとパソコンをUSB、シリアル、赤外線などのいずれかで接続しパートナーシップを作成する。ネットワーク経由やRAS接続ではパートナーシップの作成はできない。これを作成せず、PIMデータの同期を行わない"ゲスト"接続も選択できる。 なお赤外線の場合、一部機種で採用されたFIR (4Mbps) では接続確立後すぐに切断されてしまい接続することが出来ない。 富士通のPocketLOOX FLX3のようにメニューから赤外線通信速度切り替えが出来るものは標準のSIR (115.2Kbps) に切り替えれば接続可能。 速度変更が出来ない（FIRのみの）場合はクレードル等を経由しての接続となる。

パートナーシップは、PDA側から見て2台までのパソコンと作成することができる。パソコン側から見てパートナーシップを作成するPDAの数に制限はない。

ActiveSync を通して一度に接続（通信）できるPDAは1台のみである。同時に2台以上のPDAを接続すると、ActiveSync はそのうちの1台だけを認識する。

## バージョン履歴、過去のソフトウエア

2011年1月現在、最新の(日本語での)バージョンは4.5である。

Windows CE (Windows Mobile) の変遷とともにActiveSyncも各バージョンにおいてそれに追随するようにバージョンアップを繰り返してきた。また、ActiveSyncはバージョン 3.0 からメジャーリリースされており、これ以前の同ソフトウエアはWindows CE Servicesとして、また最初期にはWindows CE 1.0専用としてH/PC Explorer (Handheld PC Explorer) がリリースされていた。通信にTCP/IPスタックを利用するため、この頃の Windows 95/98にはTCP/IPプロトコルを追加インストールする必要があった。

バージョンアップとともに対応する Windows CE (Windows Mobile) のバージョンが追加されてきたが、同時に過去のバージョンは非対応になっていることがあるため、使用する際はCD-ROM等に添付のリリースノートをよく確認する必要がある。たとえば、ActiveSync 3.xはWindows Mobile 2003以降のデバイスはサポートせず、ActiveSync 4.x以降はWindows CE 2.x以前のデバイスのサポートはしない、など。

場合によっては旧バージョンのActive Syncが必要になることもあるが、複数のバージョンを同時にインストールすることはできない。

また、パソコンのOSやMicrosoft Outlookのバージョンにも注意が必要である。たとえば、OSではActiveSync 4.x以降はWindows 9xシリーズはサポートしておらず、Outlookは正式にはActiveSync 4.5でOutlook 2003までのサポートとなっている。\[4\]

## 次世代のActiveSync

2007年2月、本ソフトウエアの後継にあたるWindows Mobile Device Centerが提供開始された。これは先にリリースされたオペレーティングシステム[Windows Vista以降のWindowsに対応しており](https://ja.wikipedia.org/wiki/Microsoft_Windows_Vista "wikilink")、Windows Mobile/Windows Phoneベースの端末との接続環境を提供する。事実上ActiveSyncの後継ソフトウエアであり、メジャーリリースバージョンも6.0からである。

2012年現在の最新バージョンは6.1。XPを含む以前のOSはサポートされていない。Windows 7、Windows 8でも動作するが、正式サポートの声明はない。

以前のH/PC、PalmsizePC、Pocket PC等は全てサポートから外れており、Windows Mobileベース端末からのサポートとなる。対応するOfficeスイートは引き続きMicrosoft Office Outlookである。Vista/7のWindowsメール、Windows 8のメールアプリには対応しない。

基本機能は、ActiveSyncと同様、連絡先、予定表、仕事、メモ、電子メール、そしてモバイルのお気に入り、ファイルである。デバイス内のフィル参照も引き続きサポートする。\[5\]「メディア」は項目から外れたが、Windows Media Player自身で同期を行うよう変更された。メディアの同期は、モバイルデバイスに限らず他の音楽プレイヤーや携帯電話端末と同じく MTP接続によるものに近いようで、Mobile Device Centerとは別個の動作をする（実際の操作もMediaPlayerで行う）。必ずしもMobile Device Center が起動している必要はない。\[6\]

このアプリケーションから、デバイス内のメディアファイル（画像/音楽/ビデオ）をインポートする機能が追加された。

Vista以降のWindowsにはコントロールパネル内に「同期センター」という標準機能が用意されているが、これは原則的にはPC同士のネットワーク上の同期関係を構築するソフトウエア（アプレット）である。ただし、Mobile Device Centerでの同期結果やエラーなどが表示され、ユーザーに報告される。

ActiveSyncと同様、常駐型アプリケーションであり、OSと同時にサービスが起動する。ただし裏で待機はするもののタスクトレイ等に現れず、基本的には任意に起動するアプリケーションとなったが、PIM同期はウインドウを表示せず自動的に行われる。\[7\]

接続方法は、USB接続のほか、COMポート（シリアル接続）、[Bluetooth](../Page/Bluetooth.md "wikilink")\[8\]、IrDA（赤外線）接続もサポートする。何らかのネットワーク経由（[LAN](../Page/Local_Area_Network.md "wikilink")、[Wi-Fi](../Page/Wi-Fi.md "wikilink")等のIP接続）の接続はやはりサポートしない。USBのデバイスドライバはMobile Device Center自身が共通のものを持っているようで、ユーザーは特別に機種ごとのドライバーのインストールを意識する必要はなくなっている。または、Windows Update経由で自動インストールされる。

## ネットワークホストとしての働き

本ソフトウエアまたはWindows Mobile Device Centerは、対象となる端末（[PDAの他](../Page/携帯情報端末.md "wikilink")、[スマートフォン](https://ja.wikipedia.org/wiki/スマートフォン "wikilink")等も含む）を[WANへと接続するためのゲートウエイとしても機能する](../Page/Wide_Area_Network.md "wikilink")。すなわち、親となるPCのIP接続にシリアル接続（USB等）を通じて相乗りする形で実現する機能である。この機能はマイクロソフト関連端末では「USB経由でのインターネット接続」として設定可能な他、[Android端末の一部においては逆に親PCを端末経由でWANへ接続する](../Page/Android_\(オペレーティングシステム\).md "wikilink")[USBテザリングを行う場合に本ソフトウエアがインストールされていることが条件になっていることもあり](https://ja.wikipedia.org/wiki/テザリング "wikilink")、単にWindows Mobileに限らずWindowsにおけるネットワークホストを提供する一種の汎用ゲートウエイとしての機能も有している。但し、一般的にはUSB接続経由での利用が主なようである。

## 脚注

<references/>

## 関連項目

  - [Pocket PC](../Page/Pocket_PC.md "wikilink")
  - [Microsoft Outlook](../Page/Microsoft_Outlook.md "wikilink")
  - [プッシュ型電子メール](../Page/プッシュ型電子メール.md "wikilink")

## 外部リンク

[Category:Microsoft_Windows](https://ja.wikipedia.org/wiki/Category:Microsoft_Windows "wikilink") [Category:Windows_CE](https://ja.wikipedia.org/wiki/Category:Windows_CE "wikilink") [Category:情報機器](https://ja.wikipedia.org/wiki/Category:情報機器 "wikilink")

1.  Windows Mobile、Windows CEや[Pocket PC等は組込みプラットフォームあるいはOSの名称であるが](../Page/Pocket_PC.md "wikilink")、本稿では便宜上いずれもOSとしての意味合いで記述する。詳細は各記事に詳しい。
2.  バックアップ機能はWindows Mobile 2003以前の機種までとなっている (ActiveSync 4.x)
3.  Windows Media Player バージョン7から9までとの組み合わせでは、同ソフトの「デバイスへ転送」でPDAが選択できるようになり、ライセンスを含むコンテンツの転送が実現する。バージョン10とActiveSync 4.xとでは同期項目の「メディア」を利用できる。
4.  ユーザーコミュニティの間ではActiveSync 4.5とOutlook 2007との間での同期の成功が報告されているようである。(利用にあたっては自己責任となる)
5.  ActiveSync同様、Explorerに仮想的にデバイスが現れる。Windows 7/8ではデバイス内でファイルへのショートカットが作成できないなど細かな変更点が見られる。
6.  Windows Media Player 11/12では、リストペインの「同期」タブにて全ての操作が行える。デバイスへのメディアの転送はプレイリスト単位で行われ、PC上で作成されたプレイリストに従って同期が行われる。曲順その他もそのまま転送できる。同期項目として、デバイス名の他そのデバイスに挿入されているストレージが別個に同期対象となる。
7.  ただし、パートナーシップの未作成なデバイスを検出した時のみウインドウを表示する。
8.  ActiveSync専用プロファイルに対応できる場合のみ。
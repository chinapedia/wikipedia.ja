> この記事は[GPE Palmtop Environment](https://ja.wikipedia.org/wiki/GPE_Palmtop_Environment)から翻訳されています。


{{ infobox software | 名称 = GPE Palmtop Environment | 最新版 = 2.8 | 最新版発表日 = [2007年](../Page/2007年.md "wikilink")[8月7日](../Page/8月7日.md "wikilink") | 対応OS = [Linux](https://ja.wikipedia.org/wiki/Linux "wikilink") | 対応プラットフォーム = [携帯情報端末](../Page/携帯情報端末.md "wikilink") | 種別 = [ユーザインタフェース](../Page/ユーザインタフェース.md "wikilink") | ライセンス = [GPL](../Page/GNU_General_Public_License.md "wikilink"), [LGPL](../Page/GNU_Lesser_General_Public_License.md "wikilink") | 公式サイト = <http://gpe.linuxtogo.org/> }}

**GPE Palmtop Environment**（[再帰的頭字語](https://ja.wikipedia.org/wiki/再帰的頭字語 "wikilink")になっていて、略称は**GPE**）は、[Linux](https://ja.wikipedia.org/wiki/Linux "wikilink")の動作する[携帯情報端末](../Page/携帯情報端末.md "wikilink")向けの[GUI環境である](https://ja.wikipedia.org/wiki/グラフィカルユーザインタフェース "wikilink")。[PIM](https://ja.wikipedia.org/wiki/Personal_Information_Manager "wikilink")、オーディオ再生、電子メール、ウェブ閲覧などを携帯機器で実行するためのソフトウェアコンポーネントやアプリケーションが全て含まれた完全な環境になっている。

[GNU General Public Licenseおよび](../Page/GNU_General_Public_License.md "wikilink")[GNU Lesser General Public Licenseでライセンスされており](../Page/GNU_Lesser_General_Public_License.md "wikilink")、[フリーソフトウェア](../Page/フリーソフトウェア.md "wikilink")である。

## サポートしているデバイス

GPE は以下のプラットフォームを対象とした[組み込み](../Page/組み込みLinux.md "wikilink")[Linuxディストリビューション](../Page/Linuxディストリビューション.md "wikilink")にバンドルされている。

  - [シャープ](../Page/シャープ.md "wikilink") [ザウルス](../Page/ザウルス.md "wikilink")
  - [HP](../Page/ヒューレット・パッカード.md "wikilink") [iPAQ](https://ja.wikipedia.org/wiki/iPAQ "wikilink")
  - HP [Jornada](https://ja.wikipedia.org/wiki/Jornada "wikilink") 72x
  - [シーメンス](../Page/シーメンス.md "wikilink") [SIMpad](https://ja.wikipedia.org/wiki/SIMpad "wikilink") SL4

さらに、以下の機器にも移植が行われている。

  - GamePark Holdings [GP2X](https://ja.wikipedia.org/wiki/GP2X "wikilink")
  - [Nokia](https://ja.wikipedia.org/wiki/ノキア "wikilink") 770
  - Nokia N800
  - [パーム](../Page/パーム_\(企業\).md "wikilink") TX
  - [Palm Treo](https://ja.wikipedia.org/wiki/Palm_Treo "wikilink") 650[1](http://www.grack.com/programming/misc/TreoLinux.html)
  - [HTC](https://ja.wikipedia.org/wiki/HTC_\(企業\) "wikilink") Universal
  - HTC Typhoon
  - HTC Tornado
  - HTC Wizard

2007年2月5日、GPEプロジェクトは携帯電話向けの [GPE Phone Edition](http://gpephone.linuxtogo.org/) を発表した\[1\]。

## 開発

GPEは[X Window SystemベースのGUIであり](../Page/X_Window_System.md "wikilink")、インタフェースとして [GTK+](https://ja.wikipedia.org/wiki/GTK+ "wikilink")、[ウィンドウマネージャ](https://ja.wikipedia.org/wiki/ウィンドウマネージャ "wikilink")として[Matchbox](https://ja.wikipedia.org/wiki/Matchbox "wikilink")を使っている。このプロジェクトでは強力なアプリケーションを容易に開発できる基盤を提供するため、[SQLite](https://ja.wikipedia.org/wiki/SQLite "wikilink")、[D-Bus](../Page/D-Bus.md "wikilink")、[GStreamer](https://ja.wikipedia.org/wiki/GStreamer "wikilink")、その他の[freedesktop.org](https://ja.wikipedia.org/wiki/freedesktop.org "wikilink")が定義した標準を利用し、[共有ライブラリやデータベーススキーマといった中核機能を提供している](../Page/ライブラリ.md "wikilink")。

GPEプロジェクトの主な目標は、携帯機器における[フリーソフトウェア](../Page/フリーソフトウェア.md "wikilink")開発を促進し、新技術を試すことにある。

GPE上で開発されたアプリケーションには、以下のようなものがある。

  - *GPE-Contacts* - 連絡先管理
  - *GPE-Calendar* - カレンダー
  - *GPE-Edit* - 単純なテキストエディタ
  - *GPE-Filemanager* - [MIMEタイプをサポートしたリモートアクセス可能なファイルマネージャ](https://ja.wikipedia.org/wiki/メディアタイプ "wikilink")
  - *GPE-Gallery* - [画像ビューア](https://ja.wikipedia.org/wiki/画像ビューア "wikilink")
  - *GPE-Games* - 小さいゲームのコレクション
  - *GPE-Mini-Browser* - [CSSと](../Page/Cascading_Style_Sheets.md "wikilink")[JavaScript](../Page/JavaScript.md "wikilink")をサポートしたWebブラウザ
  - *GPE-Sketchbook* - スケッチが可能なメモ
  - *GPE-Soundbite* - 音声メモツール
  - *GPE-ToDo* - TODOリストマネージャ
  - *GPE-Timesheet* - タスク実行時間計測
  - *Starling* - GStreamerベースのオーディオプレーヤー
  - *[VLC](https://ja.wikipedia.org/wiki/VLCメディアプレーヤー "wikilink")* - [メディアプレーヤー](https://ja.wikipedia.org/wiki/メディアプレーヤー "wikilink")

GPEの[PIMアプリケーション](https://ja.wikipedia.org/wiki/Personal_Information_Manager "wikilink")（GPE-Contacts、GPE-Calendar、GPE-ToDo）は、対応するデスクトップおよびウェブアプリケーション（[Evolution](https://ja.wikipedia.org/wiki/Evolution_\(ソフトウェア\) "wikilink")、[Mozilla Sunbird](https://ja.wikipedia.org/wiki/Mozilla_Sunbird "wikilink")、[Google Calendar](https://ja.wikipedia.org/wiki/Google_Calendar "wikilink") など）と *GPE-Syncd* および[OpenSync](https://ja.wikipedia.org/wiki/OpenSync "wikilink")フレームワークを通して同期できる。

GPEには各種設定を行うGUIユーティリティも含まれている（[IEEE 802.11](https://ja.wikipedia.org/wiki/IEEE_802.11 "wikilink") 無線LAN、[Bluetooth](https://ja.wikipedia.org/wiki/Bluetooth "wikilink")、[IrDA](../Page/IrDA.md "wikilink")、[ファイアウォール](../Page/ファイアウォール.md "wikilink")、[ALSA](https://ja.wikipedia.org/wiki/Advanced_Linux_Sound_Architecture "wikilink")、[Ipkg](https://ja.wikipedia.org/wiki/Ipkg "wikilink") パッケージマネージャなど）。

[Tinymail](https://ja.wikipedia.org/wiki/Tinymail "wikilink")フレームワークに基づく[プッシュ型電子メール](https://ja.wikipedia.org/wiki/プッシュ型電子メール "wikilink")クライアントは開発中である。

## Linuxディストリビューション

GPEは以下の[組み込みLinux](../Page/組み込みLinux.md "wikilink")ディストリビューションでは主要な環境とされている。

  - [Ångström](https://ja.wikipedia.org/wiki/:en:Ångström_distribution "wikilink")
  - [Familiar Linux](https://ja.wikipedia.org/wiki/Familiar_Linux "wikilink")
  - [OpenZaurus](https://ja.wikipedia.org/wiki/OpenZaurus "wikilink")

上掲のディストリビューションほどではないが、GPEは以下のディストリビューションでも利用可能になっている。

  - [Ubuntu](https://ja.wikipedia.org/wiki/Ubuntu "wikilink")
  - [Debian](../Page/Debian.md "wikilink")
  - [Internet Tablet OS](https://ja.wikipedia.org/wiki/Internet_Tablet_OS "wikilink")

## 論争

GPEプロジェクトに関しては、ホスティングサービスの変更、[IRCチャンネルの所有権](https://ja.wikipedia.org/wiki/インターネット・リレー・チャット "wikilink")、商標について論争が続いている\[2\]\[3\]。

### Webホスティング

GPEは2002年4月から[Handhelds.org](http://handhelds.org)でホスティングされていた。しかし、開発者から示唆があり、2006年10月に[Linuxtogo.org](http://linuxtogo.org)に移転した\[4\]。Handhelds.orgは去っていった開発者のユーザアカウントを削除し、元の[GPE Handhelds.org](http://gpe.handhelds.org)サイトにあった新たな[GPE Linuxtogo.org](http://gpe.linuxtogo.org)サイトへのリンクや参照を全て削除した\[5\]。

### IRCチャンネル

上記に関連して、両者が[Freenode](https://ja.wikipedia.org/wiki/Freenode "wikilink").netにある\#gpeという[IRCチャンネルの所有権を主張している](https://ja.wikipedia.org/wiki/インターネット・リレー・チャット "wikilink")。Freenode.netは両者が合意に達するまで、そのチャンネルの事実上閉鎖している。その後、Linuxtogo.orgは\#gpe-projectを使い、Handhelds.orgは\#handhelds-gpeを使っている（共にFreenode.netにある）。

### 商標

Handhelds.orgの管理者George Franceは2007年3月6日、[OPIE](../Page/OPIE.md "wikilink")および[Ipkg](https://ja.wikipedia.org/wiki/Ipkg "wikilink")と共にGPEについても[米国特許商標庁](https://ja.wikipedia.org/wiki/米国特許商標庁 "wikilink")に商標登録を出願した\[6\]。2007年6月25日、米国特許商標庁は Handhelds.orgのGPEの所有権の証拠としてHendhelds.orgのウエブサイトのスクリーンショットを採用できないと判断し、より具体的な「GPE製品」の見本を要求した\[7\]。Handhelds.orgと[OSI評議会メンバーのRuss](../Page/Open_Source_Initiative.md "wikilink") Nelsonは、GPEプロジェクトはHandhelds.orgを足場として開発してきたと主張した\[8\]。

Linuxtogo.orgのGPE開発者らは、彼らがGPEプロジェクトの実体であるとし、Handhelds.orgは単にホスティングを提供していただけだと主張した\[9\]\[10\]。さらに彼らはGPEプロジェクトがHandhelds.orgでホスティングされる以前から存在していた点を指摘した\[11\]。

2008年2月27日、米国特許商標庁はGPEの商標について拒絶査定を下した。George France は出願内容を修正し（[GNU](../Page/GNU.md "wikilink")とLinuxに関する参照を削除）、GPEの商標は2008年6月3日、異議申し立てのために公表された\[12\] 。

これに対して、Linuxtogo.orgのGPE開発チームはHandhelds.orgで開発されたGPE基盤部分を捨てることにした。ブートローダを別のものにし、IpkgからOpkgに乗り換えた。ただし、アプリケーションに対してはほとんど影響はない。\[13\]

## 関連項目

  - [OPIE](../Page/OPIE.md "wikilink")
  - [Palm OS](../Page/Garnet_OS.md "wikilink")
  - [Pocket PC](https://ja.wikipedia.org/wiki/Pocket_PC "wikilink")
  - [Qtopia](https://ja.wikipedia.org/wiki/Qtopia "wikilink")
  - [Windows Mobile](https://ja.wikipedia.org/wiki/Windows_Mobile "wikilink")

## 脚注

## 外部リンク

  - [GPE web site at LinuxToGo](http://gpe.linuxtogo.org/)
  - [GPE web site at Handhelds.org](http://gpe.handhelds.org/)

[Category:グラフィカルユーザインタフェース](https://ja.wikipedia.org/wiki/Category:グラフィカルユーザインタフェース "wikilink") [Category:組み込みOSの製品](https://ja.wikipedia.org/wiki/Category:組み込みOSの製品 "wikilink") [Category:X_Window_System](https://ja.wikipedia.org/wiki/Category:X_Window_System "wikilink") [Category:Linux](https://ja.wikipedia.org/wiki/Category:Linux "wikilink")

1.
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
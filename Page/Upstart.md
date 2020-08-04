> この記事は[Upstart](https://ja.wikipedia.org/wiki/Upstart)から翻訳されています。


**Upstart**は、いくつかの[Unix系](../Page/Unix系.md "wikilink")[コンピュータ](../Page/コンピュータ.md "wikilink")[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink")で起動時にタスクを実行する手法として古くから備わる[init](https://ja.wikipedia.org/wiki/init "wikilink")デーモンの代わりとなるもので、[イベント駆動型である点に特徴がある](../Page/イベント駆動型プログラミング.md "wikilink")。Upstartは、当時[カノニカル](https://ja.wikipedia.org/wiki/カノニカル "wikilink")の従業員であったが開発した。

## 原理の説明

元々古くから備わるinitプロセスは、電源オンの後にコンピュータを通常の起動状態にすることや、シャットダウン前にきちんとサービスを終了することにしか責任を持たなかった。このため、前記の設計により現在のタスクが完了するまで将来のタスクは厳格に[同期化され](../Page/同期_\(計算機科学\).md "wikilink")、さらにブロックされてしまう。さらに準備やクリーンアップ機能による制限を受けるため、これらのタスクはあらかじめ定義されねばならない。これでは現代の[デスクトップコンピュータにおけるスタートアップ以外の](../Page/デスクトップパソコン.md "wikilink")、以下に挙げるような様々なタスクを簡潔に処理できなくなる:

  - マシン起動中における[USBフラッシュドライブ](../Page/USBフラッシュドライブ.md "wikilink")などのポータブルストレージやネットワークデバイスの脱着。
  - システムロックなしの、特にディスクがスキャンされるまで電源すらオンになっていない場合における新規ストレージデバイスの発見とスキャン。
  - デバイス用[ファームウェア](../Page/ファームウェア.md "wikilink")のロード。ロードはデバイスが発見された後かつデバイスが使えない前に行わなければならないはずである。

Upstartのイベント駆動型モデルにより、イベント生成とは非同期にイベント応答ができる\[1\]。

## 設計

Upstartはブート時のタスクとサービスの起動とシャットダウン時のタスクとサービスの停止を非同期に行い、システム動作中にはタスクとサービスの管理も行う。

[System V initとの完全な後方](https://ja.wikipedia.org/wiki/init "wikilink")[互換性](../Page/互換性.md "wikilink")を保ち、容易に移行可能であることが設計目標であった\[2\]。そのため、既存のSystem V init用スクリプトを無修正で実行可能である。いつも正常起動への完全な移行を仮定し要求するが、スタートアップの古くから備わる手法と新しい手法とが混在した環境をサポートしない大半の他のinit代替手法とは（[systemd](https://ja.wikipedia.org/wiki/systemd "wikilink")や[OpenRC](https://ja.wikipedia.org/wiki/OpenRC "wikilink")と比べて）そういった点で異なる\[3\]。

Upstartは多くのイベントやより複雑なイベントをまとめるために、入力カスタム、シングルイベント、またはイベントブリッジ用のinitctlを使うことでイベントモデルを拡張できる.\[4\]。Upstartにはデフォルトでsocket、dbus、udev、fileおよびdconfイベントへのブリッジが含まれる。必要に応じてより多くのブリッジが利用できる\[5\]。

## 採用

Upstartをデフォルトのinitシステムとして使用する、[Linuxカーネル](../Page/Linuxカーネル.md "wikilink")をベースとした[Linuxディストリビューション](../Page/Linuxディストリビューション.md "wikilink")やそれ以外のオペレーティングシステム:

  - UpstartはSystem V initの代替として[2006年](../Page/2006年.md "wikilink")後半、Ubuntu 6.10 (Edgy Eft) リリースで最初に導入された。Ubuntu 9.10 (Karmic Koala) はAlpha 6のネイティブUpstartブートアップを導入した\[6\]。続いてDebianプロジェクトが[2014年](../Page/2014年.md "wikilink")、将来のリリースに[systemd](https://ja.wikipedia.org/wiki/systemd "wikilink")の採用を決めた後、[Mark Shuttleworthは上流との調和を維持するためにsystemd自体へと移行する計画をUbuntuは開始したとアナウンスした](https://ja.wikipedia.org/wiki/Mark_Shuttleworth "wikilink")\[7\]。
  - Upstartは[Google Chrome OSや](https://ja.wikipedia.org/wiki/Google_Chrome_OS "wikilink")[Chromium OSで使われている](https://ja.wikipedia.org/wiki/Chromium_OS "wikilink")\[8\]。

Upstartをある程度サポートするかしていたが、デフォルトinitシステムとしての使用をやめたか既に使用していないLinuxディストリビューション:

  - [Debian](../Page/Debian.md "wikilink")は*jessie*リリース立ち上げ時にデフォルトinitシステムをUpstartへ切り替えることを検討したが\[9\]、systemdへ切り替えることになった\[10\]。Upstartは結局2015年12月にDebianアーカイブから削除された\[11\]。
  - [Ubuntu](../Page/Ubuntu.md "wikilink")は[Ubuntu Touchを除くバージョン](https://ja.wikipedia.org/wiki/Ubuntu_Touch "wikilink")15.04 (Vivid Vervet) において、デフォルトinitシステムのsystemdへの置き換えを完了した\[12\]。
  - [Fedora](../Page/Fedora.md "wikilink") 9でSystem V initはUpstartに置き換えられたが、Fedora 15ではUpstartはsystemdに置き換えられた\[13\]\[14\]。
  - [レッドハット](../Page/レッドハット.md "wikilink")は[Red Hat Enterprise Linux](../Page/Red_Hat_Enterprise_Linux.md "wikilink") (RHEL) 6でUpstartを導入した\[15\]。そのため、[CentOS](../Page/CentOS.md "wikilink")、[Scientific Linuxおよび](../Page/Scientific_Linux.md "wikilink")[Oracle LinuxといったRHEL](../Page/Oracle_Linux.md "wikilink") 6派生でもUpstartが使われている。RHEL 7ではUpstartの代わりにsystemdが使われている\[16\]\[17\]
  - [openSUSE](https://ja.wikipedia.org/wiki/openSUSE "wikilink")はバージョン11.3 Milestone 4でUpstartを導入したが、デフォルトではなかった\[18\]。openSUSE 12.1のデフォルトinitシステムとして、Upstartの代わりにsystemdが使われた\[19\]。
  - Upstartは[HP TouchPad](https://ja.wikipedia.org/wiki/HP_TouchPad "wikilink")[タブレット用や](../Page/タブレット_\(コンピュータ\).md "wikilink")、[Palm Pre](https://ja.wikipedia.org/wiki/Palm_Pre "wikilink")、[Palm Pixi](https://ja.wikipedia.org/wiki/Palm_Pixi "wikilink")（共に[パームがHPに買収される以前より](../Page/パーム_\(企業\).md "wikilink")）、[HP Veerおよび](https://ja.wikipedia.org/wiki/HP_Veer "wikilink")[HP Pre 3スマートフォン用の](https://ja.wikipedia.org/wiki/HP_Pre_3 "wikilink")[HP](../Page/ヒューレット・パッカード.md "wikilink") [webOSで使われている](https://ja.wikipedia.org/wiki/HP_webOS "wikilink")\[20\]。
  - [ノキア](../Page/ノキア.md "wikilink")のインターネットタブレット用の[Maemo](https://ja.wikipedia.org/wiki/Maemo "wikilink") 5ではsysvinitをUpstartに置き換えた\[21\]。

## 関連項目

  - [Initng](../Page/Initng.md "wikilink") — initの非同期型代替実装の1つ
  - [Launchd](https://ja.wikipedia.org/wiki/Launchd "wikilink") — [Mac OS X v10.4でinitなどのシステム起動スクリプトおよび](../Page/Mac_OS_X_v10.4.md "wikilink")[cronの代替として導入された](https://ja.wikipedia.org/wiki/crontab "wikilink")。
  - [OpenRC](https://ja.wikipedia.org/wiki/OpenRC "wikilink")
  - [オペレーティングシステムサービス管理](https://ja.wikipedia.org/wiki/オペレーティングシステムサービス管理 "wikilink")
  - [Service Management Facility](https://ja.wikipedia.org/wiki/Service_Management_Facility "wikilink")
  - [systemd](https://ja.wikipedia.org/wiki/systemd "wikilink")

## 脚注

## 外部リンク

  -
  -
  - [Upstart Cookbook](http://upstart.ubuntu.com/cookbook)

  - [Upstart Cookbook](http://upstart.ubuntu.com/cookbook/upstart_cookbook.pdf)

  - Initシステム比較: [その1](https://lwn.net/Articles/578209/)および[その2](https://lwn.net/Articles/578210/) ([LWN.net](https://ja.wikipedia.org/wiki/LWN.net "wikilink"))

  - [Initシステム比較表](http://wiki.gentoo.org/wiki/Comparison_of_init_systems)

[Category:Ubuntu](https://ja.wikipedia.org/wiki/Category:Ubuntu "wikilink") [Category:UNIXのソフトウェア](https://ja.wikipedia.org/wiki/Category:UNIXのソフトウェア "wikilink")

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
14.
15.
16.
17.
18.
19.
20.
21.
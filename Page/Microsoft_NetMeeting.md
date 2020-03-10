> この記事は[Microsoft NetMeeting](https://ja.wikipedia.org/wiki/Microsoft_NetMeeting)から翻訳されています。


**Microsoft NetMeeting** は、[Microsoft Windows 95](../Page/Microsoft_Windows_95.md "wikilink") OSR2から[Windows XPまでに含まれている](../Page/Microsoft_Windows_XP.md "wikilink")、[T.120](https://ja.wikipedia.org/wiki/:en:T.120 "wikilink") によるデータ会議を多地点で開催する機能と、[H.323](https://ja.wikipedia.org/wiki/H.323 "wikilink") による1対1の[ビデオ会議](../Page/ビデオ会議.md "wikilink")を開催する機能を有するクライアントソフトである。\[1\]

## 概要

[ITU-T](../Page/ITU-T.md "wikilink") 勧告のT.120に準拠しており、他社製品でもT.120に準拠していれば[ホワイトボード](https://ja.wikipedia.org/wiki/ホワイトボード "wikilink")機能、アプリケーション共有、デスクトップ共有、ファイル転送などを用いたデータ会議を多地点で開催可能であり、\[2\]別の手段による多地点の電話会議と組み合わせる事で多地点の[遠隔会議](https://ja.wikipedia.org/wiki/遠隔会議 "wikilink")を実現することができる。

ITU-T 勧告のH.323プロトコルにも対応しておりH.323に準拠している他社製の[ビデオ会議](../Page/ビデオ会議.md "wikilink")装置とも相互通信可能。[Ekiga](https://ja.wikipedia.org/wiki/Ekiga "wikilink")などのH.323対応のクライアントソフトとも接続できる。

NetMeetingにはH.323のMCU機能は組み込まれていないため、[多地点間ビデオ会議に拠点のひとつとして参加する事は可能だが](https://ja.wikipedia.org/wiki/ビデオ会議#多地点間ビデオ会議 "wikilink")、多地点間ビデオ会議を主催するとなるとMCUが別途必要である。\[3\]

[プライベートIPアドレスからは](https://ja.wikipedia.org/wiki/IPアドレス#プライベートIPアドレス "wikilink")[Internet Locator Server](https://ja.wikipedia.org/wiki/:en:Internet_Locator_Server "wikilink")(ILS)を使うことでグローバルIPアドレスに出ることが可能だが、ファイヤーウォールでNetMeetingが使用するポートがブロックされていれば、ILSに到達できないため外部とは通信できない。 、現在も利用可能なサーバーは存在する。\[4\]ILS はWindows 2000で動作させる事も可能であるが\[5\]デフォルトではポート1002を使用するため、ポートを389に変更するにはILSCFG \[servername\] /port 389とする必要がある。\[6\]ポートを変更する必要性に関してはILSの[英語記事を参照の事](https://ja.wikipedia.org/wiki/:en:Internet_Locator_Server "wikilink")。

[Yahoo\! Messengerや](../Page/Yahoo!_Messenger.md "wikilink")[MSN Messengerといった](https://ja.wikipedia.org/wiki/MSN_Messenger "wikilink")[インスタントメッセンジャー](../Page/インスタントメッセンジャー.md "wikilink")による動画サービスが一般化する以前は、NetMeeting によるビデオ会議や[インターネット](https://ja.wikipedia.org/wiki/インターネット "wikilink")上のチャットがよく使われていた（ILSサービスを使うか、IPアドレス直接指定）。

Windows XP リリース時以降、[マイクロソフト](../Page/マイクロソフト.md "wikilink")は[Windows Messengerへの乗り換えを進めているが](https://ja.wikipedia.org/wiki/Windows_Messenger "wikilink")、NetMeeting もデフォルトでインストールされている。Windows MessengerもMSN Messengerも[Windows Live Messengerも](https://ja.wikipedia.org/wiki/Windows_Live_Messenger "wikilink")、アプリケーション共有やデスクトップ共有、ホワイトボード機能などはNetMeetingのコンポーネントを使って実現しているが、通信プロトコルに[H.323](https://ja.wikipedia.org/wiki/H.323 "wikilink")ではなく、IETF標準の[Session Initiation Protocolを採用しており](https://ja.wikipedia.org/wiki/Session_Initiation_Protocol "wikilink")\[7\] \[8\] 互換性は無い。\[9\] [Microsoft Office Communications ServerもSIPベースであるため](https://ja.wikipedia.org/wiki/Microsoft_Office_Communications_Server "wikilink")、NetMeetingとは接続できない。

[Windows Vista](https://ja.wikipedia.org/wiki/Microsoft_Windows_Vista "wikilink") のリリースでNetMeetingはOSから除外され、**[Windows Meeting Space](../Page/Windows_Meeting_Space.md "wikilink")**に置換された。Windows Meeting Spaceはコラボレーション機能のみであり、NetMeetingにあったビデオ会議機能は持っていない。

マイクロソフトは2007年3月22日、サポートはしないもののVista向け[ホットフィックス](https://ja.wikipedia.org/wiki/ホットフィックス "wikilink")を出した。これを適用することでVistaにNetMeetingをインストール可能となり、リモートデスクトップの共有は受信ができないなど制約はあるもののXPベースのPCと連携できたが、既にこのホットフィックスは[マイクロソフトのサイトから削除](http://support.microsoft.com/default.aspx/kb/927853)されダウンロードできない。

ネットでの連携と画面共有としてマイクロソフトは[SharedViewを別途](https://ja.wikipedia.org/wiki/:en:Microsoft_SharedView "wikilink")[リリース](https://www.microsoft.com/downloads/details.aspx?familyid=95AF94BA-755E-4039-9038-63005EE9D33A&displaylang=ja)した。こちらは無償で利用可能だが[Microsoft アカウントとインターネットへの接続が必要で](https://ja.wikipedia.org/wiki/Microsoft_アカウント "wikilink")、ローカルのLANだけでは動作しない。

## 関連項目

  - [Ekiga](https://ja.wikipedia.org/wiki/Ekiga "wikilink")

## 外部リンク

  - [Windows XPでNetMeetingを使用する](http://www.atmarkit.co.jp/fwin2k/win2ktips/168netmeetxp/netmeetxp.html) @IT
  - [Tutorial: Secure Remote Assistance with Netmeeting and Hamachi](http://haris.tv/2007/07/31/remote-assistance-with-netmeeting-hamachi/)
  - [Microsoft SharedView ホーム ページ](https://connect.microsoft.com/content/content.aspx?ContentID=6382&SiteID=94&wa=wsignin1.0)

## 出典

[Category:Windowsのコンポーネント](https://ja.wikipedia.org/wiki/Category:Windowsのコンポーネント "wikilink")

1.  [Product Interoperability](http://technet.microsoft.com/en-us/library/cc767135.aspx) NetMeeting 3.0 Resource Kit (マイクロソフト)
2.  [Understanding the T.120 Standard](http://technet.microsoft.com/en-us/library/cc767136.aspx) NetMeeting 3.0 Resource Kit\] (マイクロソフト)
3.  [遠隔ゼミ支援システムの構築](http://www2.gsis.kumamoto-u.ac.jp/~dlearning/pdf/p01.pdf) 熊本大学社会文化科学研究科
4.  [NetMeetingHQ NetMeeting ILS Servers Directory for Video Chat](http://www.netmeetinghq.com/ils/servers.phtml)
5.  [Site Server ILS サービスをインストールするには](http://www.microsoft.com/windows/windows2000/ja/server/help/TAPI_ILS_install.htm) (マイクロソフト)
6.  [Ilscfg](http://www.microsoft.com/windows/windows2000/ja/server/help/ilscfg.htm) (マイクロソフト)
7.  [Windows Messenger の詳細 ‐ 通信のしくみ](http://technet.microsoft.com/ja-jp/library/bb457041.aspx) (マイクロソフト)
8.  [マイクロソフトがIP電話を面白くする\!? ～いま注目を集める「SIP」の最新トレンドと概要～](http://www.atmarkit.co.jp/fnetwork/trend/20030405/sip.html) @IT
9.  [“XP”と“2000”ではテレビ電話できない？――業界が乗り越えるべき壁](http://plusd.itmedia.co.jp/broadband/0112/26/sip.html) (itmedia)
> この記事は[Virtual Network Computing](https://ja.wikipedia.org/wiki/Virtual_Network_Computing)から翻訳されています。


**Virtual Network Computing**（ヴァーチャル・ネットワーク・コンピューティング、略称**VNC**）は、ネットワーク上の離れたコンピュータを遠隔操作するための[RFB](https://ja.wikipedia.org/wiki/RFB_Protocol "wikilink")[プロトコルを利用する](../Page/通信プロトコル.md "wikilink")、[リモートデスクトップ](https://ja.wikipedia.org/wiki/リモートデスクトップ "wikilink")ソフトである。VNCは[クロスプラットフォーム](../Page/クロスプラットフォーム.md "wikilink")なソフトウェアとして開発されているため、インストールされているマシン同士は[OSなどのプラットフォームの種類に依存することなく通信できる](../Page/オペレーティングシステム.md "wikilink")。

VNCの最初のバージョンは [Olivetti & Oracle Research Lab](https://ja.wikipedia.org/wiki/Olivetti_&_Oracle_Research_Lab "wikilink") によって開発されたが、オリジナル版の[ソースコード](../Page/ソースコード.md "wikilink")が[GPL方式の](../Page/GNU_General_Public_License.md "wikilink")[ライセンス](../Page/ライセンス.md "wikilink")下で[オープンソース](../Page/オープンソース.md "wikilink")として公開されているため、現在では様々な派生ソフトが誕生している。

## 概要

このソフトウェアは[サーバ](../Page/サーバ.md "wikilink")ソフトと、[クライアント](../Page/クライアント_\(コンピュータ\).md "wikilink")（もしくは[ビューア](https://ja.wikipedia.org/wiki/ビューア "wikilink")）ソフトの2つに分かれている。

操作される側でサーバソフトを起動しておき、遠隔操作する側はクライアントソフトを起動させ接続、遠隔操作を行う。

VNCで[通信プロトコル](../Page/通信プロトコル.md "wikilink")として使用される[RFB Protocolは非常に簡素なプロトコルで](https://ja.wikipedia.org/wiki/RFB_Protocol "wikilink")、サーバ側はピクセルデータ化した画面を小さな[長方形](../Page/長方形.md "wikilink")に分け、位置を指定してクライアントに送信するだけである。しかし、この方法は非常に単純であると同時に、大きな帯域幅を使用する。そこで、帯域幅の削減のために様々な方法が編み出された。様々な[エンコード](../Page/エンコード.md "wikilink")形式や[データ圧縮](../Page/データ圧縮.md "wikilink")がこれに該当するが、最も単純な方法は、前の送信と比較して変更された部分のみを送信する方法である。これは[マウスポインタ](../Page/マウスポインタ.md "wikilink")の移動のみが行われた場合などには非常に有効だが、全体的な変化の大きい[動画](../Page/動画.md "wikilink")再生をしている画面などを送信するには適していない。それはネットワークが十分に高速であっても変わらない。なお、このような拡張プロトコルを使用するには、サーバとクライアント双方のソフトウェアがその形式に対応している必要がある。

デフォルトでは[TCPの](../Page/Transmission_Control_Protocol.md "wikilink")5900から5906までの[ポート番号](https://ja.wikipedia.org/wiki/ポート番号 "wikilink")を使用する。また、[ウェブブラウザ](../Page/ウェブブラウザ.md "wikilink")上で動作する[Java版のクライアントは](../Page/Javaプラットフォーム.md "wikilink")、既定で5800から5806までのポートを使用する。これらは設定によって変更可能である。通常はポート毎に（物理デスクトップとも）独立した仮想デスクトップセッションを提供する。同じポートにアクセスする複数のクライアントは同じデスクトップを共有する。

[WindowsはシングルセッションOSのため](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")、5900番以外のポートを使用することは少ない。 クライアント（ビューア）は物理デスクトップのミラリング・イメージを見ることになる。ターミナルサービスと違い、Windowsにログインしているユーザに無関係であり、また仮想デスクトップのサイズは物理デスクトップのサイズになるので両者が異なると[レターボックス](https://ja.wikipedia.org/wiki/レターボックス "wikilink")やスクロールなどの効果が生じる。

## メリット

当項目冒頭にもあるとおり、VNCはマルチプラットフォームでのGUIの遠隔操作が可能である。Linuxの操作をWindowsから、あるいはその逆でWindowsの操作をLinuxからなど、非常に自由度が高い。派生ソフトのMetaVNCにおいてはLinux上のウインドウ毎にVNCビューアを開くことができる。

また、タブレット端末からVNCを利用して自宅のPCを操作し、ファイルの送受信、テレビ録画予約などの用途が広がる。同様に[Wi-Fi](../Page/Wi-Fi.md "wikilink")通信ができる[PDAやLinuxを搭載したものでも同様の可能性がある](../Page/携帯情報端末.md "wikilink")。

[CPU切替器](https://ja.wikipedia.org/wiki/CPU切替器 "wikilink")という商品があり、複数台のPC、複数のOSを一組のモニタ、マウス、キーボードで操作できるが、これをVNCで代用することもできる。

PC操作を教える側、教わる側が傍にいなくても、実際に操作して見せて説明ができる。これに特化したのがMultiVNCと言えるが、他の派生VNCでも充分な場面が多い。

ネットワーク管理者が、施設内の複数のPCのメンテナンスを行う際、時間やコストを削減するのに役立てる場合がある。

外出先から、あるいは前述の管理者がVNCを利用する場合、電源の切れているPCは[Wake-on-LAN](../Page/Wake-on-LAN.md "wikilink")を利用することで電源を入れることができる。こういった複合的な手段で多様な可能性がある。

## デメリット

VNCは通信に[暗号](../Page/暗号.md "wikilink")を用いないため、[パスワード](../Page/パスワード.md "wikilink")等を含め全て[平文](https://ja.wikipedia.org/wiki/平文 "wikilink")で送信される。このため、[Telnet](../Page/Telnet.md "wikilink")等と同じく危険なプロトコルであり、使用には注意が必要である。

ただし、よりセキュリティの高い[SSHや](../Page/Secure_Shell.md "wikilink")[VPNをトンネルして接続することも出来る](../Page/Virtual_Private_Network.md "wikilink")。また、派生バージョンでは、[NTLM認証が可能であったりと](https://ja.wikipedia.org/wiki/NT_LAN_Manager "wikilink")、セキュリティ面の強化が図られているものもある。

全てのサーバソフトウェアと同じように、外部からの使用するポートへの通信が[ファイアウォール](../Page/ファイアウォール.md "wikilink")や[ルーター](../Page/ルーター.md "wikilink")でブロックされていた場合は、VNCを利用することは出来ない。

### VNCループ

以下、いずれも合わせ鏡のような状態を作り出すことによって起こる現象。ただし厳密には、ポート開放など正常な動作を確認するために用いられる場合もある。

  - ひとつのマシン上でクライアントとサーバを起動し自分自身に接続した時。
  - 2台のコンピュータがお互いにもう一方を操作しようとした場合に、**VNCループ**と呼ばれる現象が起こることがある。マシンAで画面変化があった時、それがマシンBに送信され表示されると同時にさらにマシンBの画面変化としてマシンAに送信され…と繰り返す状態。場合によっては[無限ループ](../Page/無限ループ.md "wikilink")に陥ることもあり、マシンパワーを消費しコンピュータの[フリーズ](../Page/フリーズ.md "wikilink")を引き起こす事もあるので注意が必要である。

### 音声

サウンド出力はVNCで送受信できない（将来的可能性がないわけではない）。

## 対応OS

  - サーバ動作OS
    [Windows 98](../Page/Microsoft_Windows_98.md "wikilink")/[Me](https://ja.wikipedia.org/wiki/Microsoft_Windows_Me "wikilink")/[2000](../Page/Microsoft_Windows_2000.md "wikilink")/[XP](../Page/Microsoft_Windows_XP.md "wikilink")/[2003](../Page/Microsoft_Windows_Server_2003.md "wikilink")/[2008](../Page/Microsoft_Windows_Server_2008.md "wikilink")/[Vista](https://ja.wikipedia.org/wiki/Microsoft_Windows_Vista "wikilink")/[7](../Page/Microsoft_Windows_7.md "wikilink")、[macOS](https://ja.wikipedia.org/wiki/macOS "wikilink")、[Linux](../Page/Linux.md "wikilink")、[Solaris](../Page/Solaris.md "wikilink")、[Windows CE](../Page/Microsoft_Windows_Embedded_CE.md "wikilink")
  - クライアント動作OS
    [Windows 98](../Page/Microsoft_Windows_98.md "wikilink")/[Me](https://ja.wikipedia.org/wiki/Microsoft_Windows_Me "wikilink")/[2000](../Page/Microsoft_Windows_2000.md "wikilink")/[XP](../Page/Microsoft_Windows_XP.md "wikilink")/[2003](../Page/Microsoft_Windows_Server_2003.md "wikilink")/[Vista](https://ja.wikipedia.org/wiki/Microsoft_Windows_Vista "wikilink")/[2008](../Page/Microsoft_Windows_Server_2008.md "wikilink")/[7](../Page/Microsoft_Windows_7.md "wikilink")/[2008 R2](https://ja.wikipedia.org/wiki/Microsoft_Windows_Server_2008_R2 "wikilink")、[macOS](https://ja.wikipedia.org/wiki/macOS "wikilink")、[Linux](../Page/Linux.md "wikilink")、[Solaris](../Page/Solaris.md "wikilink")、[Windows CEなど](../Page/Microsoft_Windows_Embedded_CE.md "wikilink")[Java](https://ja.wikipedia.org/wiki/Java "wikilink")が作動するOS全て、[iOS (アップル)](https://ja.wikipedia.org/wiki/iOS_\(アップル\) "wikilink")。

また、TridaVNC、ChromiVNC、µVNC、WinVNC、UltraVNCなどの本家から派生したものがあり、[Palm OS](https://ja.wikipedia.org/wiki/Palm_OS "wikilink")、携帯電話なら[BREW](../Page/BREW.md "wikilink")上でも対応している。

[Mac OS X v10.5では](../Page/Mac_OS_X_v10.5.md "wikilink")、VNCクライアント「画面共有」及びVNCサーバが内蔵されている。

  - VNCクライアントを利用する場合は、Finderのサイドバーの共有に表示されている機器を選択し「画面共有...」を選ぶか、IPアドレスを入力して使う場合は、「/システム/ライブラリ/CoreServices/画面共有("/System/Library/CoreServices/Screen Sharing.app")」を起動する、またはFinderの「移動」メニューから「サーバへ接続...」を選び、サーバアドレスに「vnc://」+ IPアドレスを入力し接続する。
  - VNCサーバを利用する場合、「システム環境設定」→「共有」→「サービス」で出てくるサービス一覧から「画面共有」 をオンにするか、「リモートマネージメント」をONにして画面右下にある「アクセス権…」ボタンを押すと出てくる設定パネル内で「VNC使用者が画面を操作することを許可」をオンし、VNC接続のためのパスワードを右の欄に設定する。

## VNCの派生ソフト

VNCは1999年に開発されたソフトウェアだが、開発者が所属するAT\&T ケンブリッジ研究所の閉鎖に伴いオリジナルのVNCは開発停止。 しかしその後この開発メンバーが新会社を立ち上げ新版を公開、これがRealVNCであり現状の正統なVNCである。 またオリジナル版のソースコードがGPL方式のライセンス下で公開されていたのが幸いし、世界中の多くの開発者が様々な派生ソフトを誕生させている。だが並列的に存在するそれらが個別に開発されている経緯から、その過程で各々の機能の取り込みがしばしば発生し、故に各ソフトの根本的なメリットも混乱に至っているのが現状である。

なお、サーバとクライアントが別のVNCであっても、転送方式さえ同一なら基本的に接続可能である。

  - [VNC](http://www.cl.cam.ac.uk/Research/DTG/attarchive/vnc/)
    現在は開発停止しているオリジナル。様々な環境用に移植開発されており、その内Windows版はWinVNCとも呼ばれる。RealVNCが後を継いでいる。

  - [RealVNC](http://www.realvnc.com/)
    VNCの正統な後継ソフト。VNCと会社は異なるが開発陣が同一でVNCがRealVNCになったと捉えて問題ない。VNCの時と違い有償の高機能版が存在する。

  - [TridiaVNC](http://www.tridiavnc.com/)
    VNCにサポート業務を付加した商業向けVNC。Tridia社は2005年に開発・販売ともに終了している。

  - [ChromiVNC](http://www.chromatix.uklinux.net/vnc/)
    [Classic Mac OS用VNC](../Page/Classic_Mac_OS.md "wikilink")。Mac OS Xには未対応。2001年で開発は停止している。

  - [TightVNC](http://www.tightvnc.com/)
    転送方式にオリジナルのTight Encodingを初めて導入した拡張版VNC。Tight Encodingは高圧縮率で低速回線環境でも動作できる反面その分CPUパワーを必要とする。VNC/RealVNCと比べても対応環境が多いのも特徴。

  - [TigerVNC](http://www.tigervnc.com/)
    TightVNCの派生。TightVNCの高機能をそのまま引き継いだうえ、[OpenGL](../Page/OpenGL.md "wikilink")を利用した高速化を実現している。[Fedora](../Page/Fedora.md "wikilink")など一部の[Linuxディストリビューション](../Page/Linuxディストリビューション.md "wikilink")では標準のVNCクライアント・サーバーソフトとして採用されている。

  - <span id="mvnc">[µVNC](http://new.micro-vnc.jp/)</span>
    マイクロVNCと読む。mVNCとも。VNCの公開ソースを全く利用せずに独自開発したVNC互換クライアントソフト。主に携帯電話向けビューア。ZRLE転送方式や画面の拡大縮小に対応、またSSHクライアントを内包している。µVNCにサーバソフトは存在せず別の派生VNCのサーバ利用を前提とする。また、V2.4.0以降では、動画再生を可能にする独自のZYWRLE転送方法、音声を配信する機能なども内包している。推奨はUltraVNCサーバ。開発・販売は[日立システムアンドサービス](../Page/日立システムアンドサービス.md "wikilink")。2013年9月末日をもって[配布および使用停止措置](http://new.micro-vnc.jp/epilogue/)が取られた。

  - [UltraVNC](http://www.uvnc.com/)
    以前はUltr@VNCとも。なおUltra@VNCは誤り。Windowsに特化し描写の高速化を狙った多機能VNC。ファイル転送や画面拡大縮小、さらにビデオフックドライバによる取り込み高速化などのオリジナル拡張と、他の派生VNCで生まれた転送方式など多くの機能を盛り込んでいる。Windows専用。

  - [Win2VNC](http://win2vnc.sourceforge.net/)
    クライアントに画面を表示しない特殊なVNC。主に一方のマシン(デスクトップのメインPCなど)にあるキーボード・マウスを使ってもう一方のマシン(サブPCやノートPC)を操作する事が目的。マルチディスプレイを扱うかのように画面端から別のマシンへ移動ができる。

  - [MultiVNC](http://www.alpha.co.jp/business/products/multivnc/)
    1対多の接続に特化した特殊なVNC。IT系講習において講師が生徒の画面を確認したり操作する事を目的とする。MultiVNCではクライアントの画面をサーバ側に送るという逆の発想になっている。

  - [MetaVNC](http://metavnc.sourceforge.net/index-j.html)
    アプリケーションのウインドウのみ転送・表示する特殊なVNC。他のマシンにあるアプリケーションをあたかもその場にあるかのように扱うのが目的。Windows2000/XP/Vista版、UNIX/LINUX版、Java版が存在する。例としてLinux上のウインドウ毎にVNCビューアを複数開くことができるのでWindows上にLinux側の必要なウインドウを複数開き、シームレスな操作が可能となる。また、TightVNCのTight Encodingを使えるようになった。

  - [gtk-vnc](http://gtk-vnc.sourceforge.net/)

<!-- end list -->

  -
    GTK用のVNCWidgetとして、提供することを目標として、開発されている。このため、VNCビューワを含むアプリケーションを数十行程度でかける程度のAPIが提供されていることが特徴である。

    また、もう1つの特徴として、Firefoxへのプラグインとして機能することが上げられる。

  - [QEMU](http://bellard.org/qemu/)
    リモートマシンを制御するためのVNCサーバ機能が[QEMU](../Page/QEMU.md "wikilink")には、含まれている。

  - [synergy-plus](http://sourceforge.jp/projects/sfnet_synergy-plus/)

<!-- end list -->

  - [ShowMyPC](https://www.showmypc.com/)
    Windows向け。クライアントソフト版とJava版がある。

### 派生サービス

VNCを使った、商用・非商用のサービス。

中間サーバーによる橋渡しによって、リモート操作する側とされる側を“NAT環境であるか否か”やIPアドレス・ファイアウォールなどのネットワークの知識なしに利用できることなどが主な特徴。 従来、ファイアウォールのポート開放を必要とし、ポートスキャンなどのリスクがあったのに対し、IDによる管理ができるのでセキュリティリスクを管理しやすくする目的もある。

#### かつてあったサービス

  - ハコ箱リモート
    エスケイサイバーパス株式会社が運営していた[オンラインストレージ](../Page/オンラインストレージ.md "wikilink")サービスHakobako.comの会員制（無料）サービスのひとつ。2004年サービス開始。2005年4月にHakobako.comサービス終了。中間サーバーの停止とともに利用不可となった。
    ちなみにHakobako.comが日本向けに提供していた**ハコ箱プレーヤー**は[GOM Playerの日本語版であり](../Page/GOM_Player.md "wikilink")、Hakobako.comサービス終了後まもなく、正式に日本語版のGOM Playerがリリースされた。
    ハコ箱リモートもGOM Player同様、[LGPL](https://ja.wikipedia.org/wiki/LGPL "wikilink")ライセンスへの違反が疑われていた。
    Windows向けのみ。

#### 現行サービス

これまでオープンソースで改良されてきたVNCの様々な技術が盛り込まれている。

  - [CrossLoop](http://www.crossloop.com/)
    2007年サービス開始。サーバーソフトウェアとクライアントソフトウェアが一体型で、リモート操作される側に表示されたランダムな数字を、電話など何らかの方法で操作する側の人に知らせることで接続するのが特徴。
    ランダムな数字は毎回変わるので望まない接続を避けられる。
    インストールから接続までが非常にシンプルなため、初心者でもすぐに使い始められることから、初心者支援のためのVNCという特徴がある。

また、無料のアカウントを作ることで対価を目的としたサービスの提供などができると謳っている。

  -
    ソフトウェアはWindows向けとMacOSX向けがあり、無料版、有料版で機能が違う。
  - [TeamViewer](http://www.teamviewer.com/ja/)
    2008年サービス開始。リモート操作される側に表示されたランダムな数字とパスワードを使って接続するが、毎回変わるわけではないので一人のユーザーが遠隔地のコンピューターを操作したり、サーバーのGUIにアクセスするのに利用可能。

無料のアカウントを使うことでアカウントごとにアクセス権のあるコンピューターを操作できる。

  -
    このほか、ファイル転送や[VPNによる接続ができる](../Page/Virtual_Private_Network.md "wikilink")。

操作される側がデュアルディスプレイの場合、自由に切り替えて操作することもできる。

  -
    ソフトウェアはWindows向けとMacOSX向け、[Linux](../Page/Linux.md "wikilink")向けがあり、無料版、有料版で機能が違う。

    [iPhone](https://ja.wikipedia.org/wiki/iPhone "wikilink")/[iPad](https://ja.wikipedia.org/wiki/iPad "wikilink")向けアプリや[Android](../Page/Android.md "wikilink")向けアプリもあり、リモート操作する側として機能する。

  - [LogMeIn](https://secure.logmein.com/JP/home.aspx)
    ブラウザ経由でリモート操作を行えるサービス。常駐するクライアントアプリさえインストールしておけば、サーバー側のIP変更などに影響されず遠隔操作を簡単に行える。ソフトウェアはWindows、MacOSX向けが無料配布されている。また、ファイル送信などに対応した有料版もある。そして、Android向けなどのスマートフォン用クライアントも販売されている。なお2014年1月をもってlogmein freeによる無償接続サービスは終了し、全てが有料化した。

  - [synergy-plus](http://sourceforge.jp/projects/sfnet_synergy-plus/)

## 関連項目

  - [RFB Protocol](https://ja.wikipedia.org/wiki/RFB_Protocol "wikilink")
  - [Wake-on-LAN](../Page/Wake-on-LAN.md "wikilink")
  - [リモートデスクトップ](https://ja.wikipedia.org/wiki/リモートデスクトップ "wikilink")
      - [Apple Remote Desktop](../Page/Apple_Remote_Desktop.md "wikilink") - macOS向けのVNCベースの複数サーバの同時管理機能を備えたリモート管理ツール
      - [Remote Desktop Protocol](../Page/Remote_Desktop_Protocol.md "wikilink") (RDP) - Microsoft Windowsの[リモートデスクトップ](https://ja.wikipedia.org/wiki/リモートデスクトップ "wikilink")
      - [PC Anywhere](https://ja.wikipedia.org/wiki/PC_Anywhere "wikilink") - [シマンテック](../Page/シマンテック.md "wikilink")社のリモートコントロールソフトウェア
      - [RemoteView](https://ja.wikipedia.org/wiki/RemoteView "wikilink") - [RSUPPORT](https://ja.wikipedia.org/wiki/RSUPPORT "wikilink")社のリモートコントロールソフトウェア
      - [NetOp](https://ja.wikipedia.org/wiki/NetOp "wikilink") - リモートコントロールソフトウェア
      - [WinShare](../Page/WinShare.md "wikilink") - [NECのソフトウェア](../Page/日本電気.md "wikilink")
      - [IgRemote](https://ja.wikipedia.org/wiki/IgRemote "wikilink") - [DirectX](https://ja.wikipedia.org/wiki/DirectX "wikilink")と[GDI+](https://ja.wikipedia.org/wiki/GDI+ "wikilink")を利用した[リモートデスクトップ](../Page/Remote_Desktop_Protocol.md "wikilink")
  - [リモートコントロール](https://ja.wikipedia.org/wiki/リモートコントロール "wikilink")
  - [VirtualGL](https://ja.wikipedia.org/wiki/VirtualGL "wikilink")
  - [Splashtop Streamer](https://ja.wikipedia.org/wiki/Splashtop_Streamer "wikilink") - [リモートデスクトップソフト「Splashtop」がIntel「Sandy Bridge」にバンドル -INTERNET Watch](http://internet.watch.impress.co.jp/docs/news/20111209_497086.html)

## 外部リンク

  - [RealVNC Ltd.](https://www.realvnc.com/en/)
  - [UltraVNC](http://ultravnc.sourceforge.net/)
  - [Bozteck VNC](http://www.vncscan.com)
  - [VNC使い方](http://remomani.com/)

[Category:オープンソースソフトウェア](https://ja.wikipedia.org/wiki/Category:オープンソースソフトウェア "wikilink") [Category:リモートデスクトップ](https://ja.wikipedia.org/wiki/Category:リモートデスクトップ "wikilink")
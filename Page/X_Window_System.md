> この記事は[X Window System](https://ja.wikipedia.org/wiki/X_Window_System)から翻訳されています。


[thumb](https://ja.wikipedia.org/wiki/ファイル:Gnome-2.28.png "wikilink") 2.28\]\] [thumb](https://ja.wikipedia.org/wiki/ファイル:KDE_4.png "wikilink") 4.x\]\] [thumb](https://ja.wikipedia.org/wiki/ファイル:Screenshot-xfce4.6-ja.png "wikilink") 4.6\]\]

**X Window System**（**エックスウィンドウシステム**、別称：「**X11**」・「**X**」など→名称については[後述](https://ja.wikipedia.org/wiki/#名称 "wikilink")）とは、[ビットマップディスプレイ上で](../Page/ビットマップ画像.md "wikilink")[ウィンドウシステム](../Page/ウィンドウシステム.md "wikilink")を提供する表示プロトコルである。[リファレンス実装](../Page/リファレンス実装.md "wikilink")として [X.Org Server](../Page/X.Org_Server.md "wikilink") があり、標準ツールキットとプロトコルを提供し、[Unix系](../Page/Unix系.md "wikilink")[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink") (OS) や[OpenVMS](../Page/OpenVMS.md "wikilink")などでの[グラフィカルユーザインタフェース](https://ja.wikipedia.org/wiki/グラフィカルユーザインタフェース "wikilink") (GUI) を構築するのに使われる。他の多くの汎用OSにも[移植されている](../Page/移植_\(ソフトウェア\).md "wikilink")。

## 概要

Xは1984年、[マサチューセッツ工科大学](../Page/マサチューセッツ工科大学.md "wikilink")が開発した。現在のバージョンであるX11は1987年9月に登場した。現在は[X.Org FoundationがXプロジェクトを主導している](../Page/X.Org_Foundation.md "wikilink")。[リファレンス実装](../Page/リファレンス実装.md "wikilink")であるversion 11 release 7.3（2007年9月6日）は[フリーソフトウェア](../Page/フリーソフトウェア.md "wikilink")として[MIT Licenseおよび類似のライセンスで提供している](../Page/MIT_License.md "wikilink")\[1\]。

Xは、GUI環境構築のための基本フレームワークやプリミティブを提供する。[ウィンドウ](../Page/ウィンドウ.md "wikilink")を画面上に描画したり、移動させたり、マウスやキーボードを使ってやり取りする。Xは[ユーザインタフェース](../Page/ユーザインタフェース.md "wikilink")を規定しない。それは、個々のクライアントプログラムの管理下にある。そのため、Xに基づいた環境の見た目は様々である。[プログラムごとにインタフェースは異なる](../Page/プログラム_\(コンピュータ\).md "wikilink")。XはOSの中核 (kernel) には含まれない。アプリケーション層構築の基盤となっている。

それ以前の表示プロトコルとは異なり、Xは表示機器に付属した（あるいは統合された）システムではない。[ネットワークコネクションを通して使うことを意図して設計している](../Page/コンピュータネットワーク.md "wikilink")。X の特徴は、[Xプロトコル](https://ja.wikipedia.org/wiki/Xプロトコル "wikilink")という、画面表示や入出力時に利用する[プロトコル](../Page/プロトコル.md "wikilink")が[ネットワーク](../Page/コンピュータネットワーク.md "wikilink")[透過だということである](../Page/透過性_\(情報工学\).md "wikilink")。そのため、手元のマシンの表示と遠隔のマシンとの表示で表示方法に差がない。このことは、ネットワークを利用した[UNIX](../Page/UNIX.md "wikilink")[ワークステーション](../Page/ワークステーション.md "wikilink")群でGUI表示を行なうのに便利であり、UNIXマシンの普及と共にXも普及していった。

## アーキテクチャ

Xは[クライアントサーバモデル](../Page/クライアントサーバモデル.md "wikilink")に基づき、**Xサーバ**が各種「クライアント」プログラムと通信する。サーバはグラフィカルな出力要求を受け付け、（[マウス](../Page/マウス_\(コンピュータ\).md "wikilink")、[キーボード](../Page/キーボード_\(コンピュータ\).md "wikilink")、[タッチパネル](../Page/タッチパネル.md "wikilink")などからの）ユーザー入力をクライアントに送信する。Xプロトコル自身はハードウェア環境に依存しない。そのため、X Window Systemが動作するマシンはUNIXマシンだけとは限らない。[Windows上でXサーバを動作させる](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")、通称*PC Xサーバ*という[ソフトウェア](../Page/ソフトウェア.md "wikilink")や、[ハードウェア](../Page/ハードウェア.md "wikilink")（ファームウエア）でXプロトコルを処理する、通称[X端末](../Page/X端末.md "wikilink")も存在する。特にX端末は、UNIXマシンが非常に高価な時代に、GUIだけを安価に表示、処理できる機器として良く利用された。

このクライアントサーバという用語（ユーザーの[端末](../Page/端末.md "wikilink")、[サーバ](../Page/サーバ.md "wikilink")、[クライアントである](../Page/クライアント_\(コンピュータ\).md "wikilink")[アプリケーション](../Page/アプリケーションソフトウェア.md "wikilink")）は、しばしば新規のXユーザーを混乱させる。なぜなら用語が逆に使われているように見えるからである。しかしXはエンドユーザーではなく、むしろアプリケーションからみた考え方をしている。Xは[ディスプレイや](../Page/ディスプレイ_\(コンピュータ\).md "wikilink")[I/Oサービスをアプリケーションに提供している](../Page/入出力.md "wikilink")。そのためサーバである。アプリケーションはこれらのサービスを利用している。そのためアプリケーションはクライアントである。

[thumbと](https://ja.wikipedia.org/wiki/ファイル:X_client_server_example.svg "wikilink")[端末エミュレータ](../Page/端末エミュレータ.md "wikilink")がローカルに動作しており、system updaterがリモートのサーバ上で動作しているが、それを制御しているのはローカルのマシンである。リモート・アプリケーションはローカルに動作するのと何ら変わりなく動作することに注意されたい。\]\]

サーバとクライアント間の[通信プロトコル](../Page/通信プロトコル.md "wikilink")は、[ネットワーク](../Page/コンピュータネットワーク.md "wikilink")[透過性を備える](../Page/透過性_\(情報工学\).md "wikilink")。クライアントとサーバは同じマシン上でも動作するし、別々のマシン上でも動作する。双方の[アーキテクチャやOSが違っていても構わない](../Page/コンピュータ・アーキテクチャ.md "wikilink")。クライアントとサーバ間の通信は、[インターネット](../Page/インターネット.md "wikilink")上でも[トンネリング](../Page/トンネリング.md "wikilink")によって安全に行うことができる。

Xクライアント自体がXサーバを内包し、複数のクライアントに対してサーバとして動作する構成も可能である。これを「Xネスティング」と呼ぶ。[Xnest](../Page/Xnest.md "wikilink")や[Xephyr](https://ja.wikipedia.org/wiki/Xephyr "wikilink")は、Xネスティングをサポートした[オープンソース](../Page/オープンソース.md "wikilink")のクライアントである。

リモートのクライアントプログラムをローカルなサーバで表示するには、[端末エミュレータ](../Page/端末エミュレータ.md "wikilink")のウィンドウを開き、[telnet](https://ja.wikipedia.org/wiki/telnet "wikilink")あるいは[sshでリモートのクライアントアプリケーション](../Page/Secure_Shell.md "wikilink")（あるいは[シェル](../Page/シェル.md "wikilink")）を起動し、入出力先をローカルに指定してクライアントを起動する（すなわち、`export DISPLAY=`*\[ユーザーのマシン\]*`:0` をリモートのマシン上で設定する）。クライアントアプリケーションはローカルサーバと接続され、ローカルマシンのディスプレイと[入力機器](https://ja.wikipedia.org/wiki/入力機器 "wikilink")を使って動作する。またローカルマシンは、リモートマシンに接続しクライアントアプリケーションを起動する小さなプログラムを実行することもできる。

リモートクライアントの実用的な利用例として、次のようなものがある。

  - リモートマシンの管理をグラフィカルに行う。
  - リモートマシンで計算量の多い[シミュレーション](../Page/シミュレーション.md "wikilink")を実行し、ローカルなデスクトップマシンでその結果を表示する。
  - 複数のマシンでグラフィカルなソフトウェアを同時に実行し、その表示を1つのマシンで行い、1人のユーザーが全体を操作する。

## 設計思想

1984年、Bob ScheiflerとJim GettysはXの基本原則を以下のように定めた\[2\]\[3\]。

  - 実際のアプリケーションでどうしても必要という場合以外は、新機能を追加するな。
  - 機構が何でないのかを定義することは、何であるのかを定義するのと同じように重要である。あらゆる要求に答える必要はない。むしろ、互換性を維持した状態で拡張可能にしておけ。
  - 1つでも例を挙げて一般化したほうが、全く例を挙げずに一般化するよりもマシである。
  - 問題が完全に把握できないときは、解決策も提供しないのが最善の方法である。
  - 10%の作業で望みの90%の効果が得られるときには、その解法を使え。
  - 複雑さは可能な限り分離せよ。
  - 方針よりも機構を提供せよ。特にユーザインタフェースについての方針はクライアント側に任せておけ。

先頭の原則は、X11の設計時に「具体的アプリケーションがそれを必要としていることを知っている場合に限って、新たな機能を追加せよ」に修正された。

Xはだいたいにおいてこれらの原則に従ってきた。参考実装は拡張性と改良を視野に入れて開発されており、1987年当時のプロトコルとほぼ完全な互換性を維持している。

## ユーザインタフェース

Xは意図的にアプリケーションの[ユーザインタフェース](../Page/ユーザインタフェース.md "wikilink")の仕様を含まないようにしている。[ボタン](../Page/ボタン_\(GUI\).md "wikilink")、[メニュー](../Page/メニュー_\(コンピュータ\).md "wikilink")、ウィンドウの[タイトルバー](../Page/タイトルバー.md "wikilink")などである。代わりに、[ウィンドウマネージャ](../Page/ウィンドウマネージャ.md "wikilink")、GUI[ウィジェット・ツールキット](../Page/ウィジェット・ツールキット.md "wikilink")、[デスクトップ環境](https://ja.wikipedia.org/wiki/デスクトップ環境 "wikilink")、アプリケーション固有の[グラフィカルユーザインタフェース](https://ja.wikipedia.org/wiki/グラフィカルユーザインタフェース "wikilink")などがそのような詳細を定義し提供している。そのため、典型的なXのインタフェースを示すことは不可能である。

[ウィンドウマネージャ](../Page/ウィンドウマネージャ.md "wikilink")は、アプリケーションのウィンドウの位置と見た目を制御する。そのインタフェースは[Windowsや](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")[Macintosh](../Page/Macintosh.md "wikilink")と似ているものもあるし（[GNOME](../Page/GNOME.md "wikilink")の[Metacity](../Page/Metacity.md "wikilink")、[KDE](../Page/KDE.md "wikilink")の[KWin](../Page/KWin.md "wikilink")、[Xfce](../Page/Xfce.md "wikilink")のXfwmなど）、全く異なるものもある。実用本位のウィンドウマネージャもあれば（[twm](https://ja.wikipedia.org/wiki/twm "wikilink")など）、デスクトップ環境に近い機能を持つものもある（[Enlightenment](https://ja.wikipedia.org/wiki/Enlightenment "wikilink")など）。

多くのユーザーは[デスクトップ環境](https://ja.wikipedia.org/wiki/デスクトップ環境 "wikilink")を通してXを利用している。デスクトップ環境にはウィンドウマネージャ、各種アプリケーションなどが一貫したインタフェースで含まれている。[GNOME](../Page/GNOME.md "wikilink")、[KDE](../Page/KDE.md "wikilink")、[Xfce](../Page/Xfce.md "wikilink")などが主なデスクトップ環境である。[freedesktop.org](https://ja.wikipedia.org/wiki/freedesktop.org "wikilink")はデスクトップ環境間の相互運用性を高めることを目的としている。

Xサーバは、グラフィカルなデスクトップでのキーボードとマウス操作を管理している。そのため、一部の[ショートカットキー](../Page/ショートカットキー.md "wikilink")はXサーバと結び付けられている。Control-Alt-Backspaceは通常、現在動作しているXセッションを終了させる。Control-Altと[ファンクションキー](../Page/ファンクションキー.md "wikilink")の組合せは、一般に[バーチャルコンソール](../Page/バーチャルコンソール.md "wikilink")に連携している。ただし、これは個々のXサーバの実装の詳細であり、常に同じとは限らない。例えば、WindowsやMacintoshで動作するXサーバでは、そのようなショートカットキーは提供されない。

## 実装

[X.Org Serverは](../Page/X.Org_Server.md "wikilink")、[リファレンス実装](../Page/リファレンス実装.md "wikilink")としてX Window Systemの正式な実装として扱われる。[フリーソフトウェア](../Page/フリーソフトウェア.md "wikilink")、[プロプライエタリ・ソフトウェア](../Page/プロプライエタリ・ソフトウェア.md "wikilink")の実装が複数存在する。商用UNIXベンダーはリファレンス実装を採用し、それを自身のハードウェアに合わせて修正し、独自の拡張を様々に凝らすことが多い。

2004年まで、[XFree86](../Page/XFree86.md "wikilink")がフリーな[Unix系](../Page/Unix系.md "wikilink")システムでのX実装の事実上の標準だった。XFree86はXを[80386搭載の](../Page/Intel_80386.md "wikilink")[パーソナルコンピュータ](../Page/パーソナルコンピュータ.md "wikilink") (PC) 上に[移植することから始まり](../Page/移植_\(ソフトウェア\).md "wikilink")、1990年代末ごろにはXの[デファクトスタンダード](../Page/デファクトスタンダード.md "wikilink")の地位を得ていた\[4\]。しかし、2004年に[X.Org ServerがXFree](../Page/X.Org_Server.md "wikilink")86のライセンスの変更を期にして派生し、こちらが主流となっていった。

XとUNIXの組合せはよく知られているが、Xサーバは他のグラフィカル環境用にも存在している。

Windowsや[macOS](https://ja.wikipedia.org/wiki/macOS "wikilink")などの他のウィンドウシステム上でXサーバを動作させる場合、統合のさせ方がソフトウェアによって色々あり、[X.Org ServerではWindowsとmacOSでは以下の方式の最初の](../Page/X.Org_Server.md "wikilink")3つをサポートしている。Unix系ではフルスクリーンだが、それ以外は[Xnest](../Page/Xnest.md "wikilink")によりサポートしている。

  - シングルウィンドウ - X11のルートウィンドウをOSのトップレベルウィンドウにマッピングする。
  - マルチウィンドウ - X11のトップレベルウィンドウをOSのトップレベルウィンドウにマッピングする。
  - ルートレス (rootless) - 本来のウィンドウシステムが背景と基本メニューを提供し、Xのウィンドウの位置を管理する。すなわち、Xのクライアントが表示するウィンドウが、手元のウィンドウシステムで表示されるアプリケーションが出すウィンドウと同じように表示される。X11のウィンドウマネージャが利用される。
  - フルスクリーン

### OpenVMS

[HPEおよびVSIの](https://ja.wikipedia.org/wiki/ヒューレット・パッカード・エンタープライズ "wikilink")[OpenVMS](../Page/OpenVMS.md "wikilink")にはXと[CDE](../Page/Common_Desktop_Environment.md "wikilink") (DECwindows) が標準のデスクトップ環境として含まれている。

### OS-9

[OS-9](../Page/OS-9.md "wikilink")にもかつてメーカー純正のXサーバがあった。

### macOS

X.Org Serverは[macOS](https://ja.wikipedia.org/wiki/macOS "wikilink")での動作をサポートしており、[X11.app](../Page/X11.app.md "wikilink") (XQuartz) として公開されている。[Mac OS X v10.5](../Page/Mac_OS_X_v10.5.md "wikilink")\~[v10.7では標準搭載されていた](https://ja.wikipedia.org/wiki/Mac_OS_X_Lion "wikilink")。

[Mac OS X v10.3では](../Page/Mac_OS_X_v10.3.md "wikilink")、[XFree86](../Page/XFree86.md "wikilink") 4.3とX11R6.6に基づいた[X11.app](../Page/X11.app.md "wikilink")が[Mac OS Xに統合されていた](https://ja.wikipedia.org/wiki/macOS "wikilink")。10.5以降はXFree86ではなく、X.Org Serverになった。古い[Mac OS 7などにも](https://ja.wikipedia.org/wiki/Classic_Mac_OS#Mac_OS_7 "wikilink")[サードパーティー](../Page/サードパーティー.md "wikilink")製のXサーバがある。

### Windows

X.Org Serverは[Cygwin](../Page/Cygwin.md "wikilink")併用の形でWindowsでの動作をサポートしており、[Cygwin/X](https://ja.wikipedia.org/wiki/Cygwin/X "wikilink") (Xwin) として公開されている。

それ以外にも、他のグループによる各種実装が存在する。X.Org Serverから派生した物もあれば、1から実装されている物もある。[フリーソフトウェア](../Page/フリーソフトウェア.md "wikilink")としては、[WeirdMind](http://www.spiro.fisica.unipd.it/servizi/weirdx/weirdmind/weirdmind/)、[WeirdX](http://www.jcraft.com/weirdx/index.html) などがある。プロプライエタリ・ソフトウェアとしては、[ASTEC-X](http://www.astec-x.com/)、[Exceed](http://www.macnica.net/opentext/exceed.html/)、[ReflectionX](http://www.cybernet.co.jp/reflection/products/rx/)、[WiredX](http://www.jcraft.com/wiredx/index.html)、[Xmanager](http://www.netsarang.com/products/xmg_overview.html)、[X-Deep/32](http://www.pexus.com)、[Xming](https://ja.wikipedia.org/wiki/Xming "wikilink")、[X-Win32](http://www.starnet.com/products/xwin32/)、[XVision Eclipse](http://www.air.co.jp/visionfamily/xvision.html) などがある。かつては、Xoftware/32（ネットマネージ製）、DynaWinX、PC-Xware（NCD製、数社が取り扱い）、Super-X（Frontier Technologies製、コンテック扱い）、eXodus for Windows（White Pine Software製、DIT扱い）という商品もあった。これらは通常、リモートのXクライアントを表示・制御するのに使われる。

### スマートフォン・タブレット

[MeeGo](https://ja.wikipedia.org/wiki/MeeGo "wikilink")、[Maemo](https://ja.wikipedia.org/wiki/Maemo "wikilink")、[Tizen](https://ja.wikipedia.org/wiki/Tizen "wikilink")、[Ubuntu Touchなど各種](https://ja.wikipedia.org/wiki/Ubuntu_Touch "wikilink")[Linux](../Page/Linux.md "wikilink")[スマートフォン](https://ja.wikipedia.org/wiki/スマートフォン "wikilink")・[タブレットでもX](../Page/タブレット_\(コンピュータ\).md "wikilink") Window System (X.Org Server) が使われている。

### X端末

[thumb製のNCD](https://ja.wikipedia.org/wiki/ファイル:Network_Computing_Devices_NCD-88k_X_terminal.jpg "wikilink")-88k X端末\]\]

X端末は、Xサーバを実行する[シンクライアント](../Page/シンクライアント.md "wikilink")である。これはUNIX[ワークステーション](../Page/ワークステーション.md "wikilink")が高価だったころ、大きめのサーバを複数人で共有し、各人がグラフィカルな環境を使えるようにする安価の手段として人気となった。また、これはMITのプロジェクトが本来想定していた方向性でもある。

X端末は、ネットワーク上で [X Display Manager Control Protocol](https://ja.wikipedia.org/wiki/Xディスプレイマネージャ#X_Display_Manager_Control_Protocol "wikilink") (XDMCP) を使って利用可能なホスト（クライアントを実行できるマシン）を探す。まず最初のホストで[Xディスプレイマネージャ](../Page/Xディスプレイマネージャ.md "wikilink")を起動する必要がある。

専用ハードウェアとしてのX端末はその後少なくなり、より安価なXサーバ用端末としてPCや新たな[シンクライアント](../Page/シンクライアント.md "wikilink")が使われるようになっている。

## Xの限界と批判

*[UNIX-HATERS Handbook](https://ja.wikipedia.org/wiki/The_Unix-Haters_Handbook "wikilink")*（1994年）は、1つの章を割いてXの問題を論じている\[5\]。*Why X Is Not Our Ideal Window System*（1990年、Gajewska, Manasse, McCormack）は、Xプロトコルの問題を詳細に論じ、改善の方法を示唆している。

### ユーザインタフェース機能

Xはユーザインタフェースの仕様やアプリケーション間通信の仕様を意図的に含まないようにしている。このためそれぞれ全く異なったインタフェースが生まれ、アプリケーション間の連携を阻む原因ともなっている。[ICCCMはクライアントの相互運用に関する仕様だが](../Page/Inter-Client_Communication_Conventions_Manual.md "wikilink")、正しく実装するのが困難なことで有名である。[Motifと](../Page/Motif_\(GUI\).md "wikilink")[CDEも標準化の試みだったが](../Page/Common_Desktop_Environment.md "wikilink")、解決策とはならなかった。この問題は、[プログラマ](../Page/プログラマ.md "wikilink")やユーザーを長い間悩ませてきた\[6\]。2007年現在、アプリケーションの[ルック・アンド・フィール](../Page/ルック・アンド・フィール.md "wikilink")とアプリケーション間通信の一貫性を保つためには、特定のデスクトップ環境あるいは特定のウィジェット・ツールキットを採用してプログラムを作成するのが一般的である。

Xプロトコルは音声を全く扱わない。そのため、[サウンドカード](../Page/サウンドカード.md "wikilink")の制御も含めた部分はOSや[OSSや](https://ja.wikipedia.org/wiki/Open_Sound_System "wikilink")[ALSAなどのオーディオシステムが分担している](https://ja.wikipedia.org/wiki/Advanced_Linux_Sound_Architecture "wikilink")。多くのプログラマはOS固有のサウンド[APIを使っている](../Page/アプリケーションプログラミングインタフェース.md "wikilink")。クライアントサーバ型のサウンドシステムとしては、古くはrplayや[Network Audio Systemがあった](https://ja.wikipedia.org/wiki/Network_Audio_System "wikilink")。その後、[EsounD](https://ja.wikipedia.org/wiki/Enlightened_Sound_Daemon "wikilink") (GNOME)、[aRts](https://ja.wikipedia.org/wiki/aRts "wikilink") (KDE) などが開発された。2001年、X.Orgはこの問題に対処するためMedia Application Server (MAS) の開発を発表した。しかし、これらはいずれも根本的な解決策とはなっていない。

### ネットワーク

[right](https://ja.wikipedia.org/wiki/ファイル:X11_ssh_tunnelling.png "wikilink") XクライアントをあるXサーバからデタッチし、別のXサーバに再アタッチすることはできない。しかし[Virtual Network Computing](../Page/Virtual_Network_Computing.md "wikilink") (VNC) ではそれが可能であり、一部のアプリケーションやツールキットではそのような機能を提供している\[7\]。

XサーバとリモートのXクライアントの間の通信トラフィックは、デフォルトでは暗号化されていない。そのため悪意ある者が[LANアナライザ](../Page/LANアナライザ.md "wikilink")を使えば、それを覗き見ることができるので注意が必要である。

### クライアント/サーバの分離

Xの設計では、クライアントとサーバはそれぞれ独立して動作する。ハードウェアからの独立性やクライアントとサーバの分離などの[オーバーヘッド](https://ja.wikipedia.org/wiki/オーバーヘッド "wikilink")は、OS内にグラフィックス機能が統合されているシステム（Windowsや[Mac OS](https://ja.wikipedia.org/wiki/Mac_OS "wikilink")）にはないものである。Xが適切な性能を発揮するには、4[MBから](../Page/メガバイト.md "wikilink")8MBの[RAMを必要とすると言われている](../Page/Random_Access_Memory.md "wikilink")。これは1990年代中ごろまではWindowsやMac OSに比較すると大きかった。

最近のWindowsやOS Xの[Quartz](../Page/Quartz.md "wikilink")はXのようなクライアントとサーバの分離を行えるようになっている。オーバーヘッドの大半は、ネットワーク上の[ラウンドトリップタイム](https://ja.wikipedia.org/wiki/ラウンドトリップタイム "wikilink")によるものである（つまりプロトコル自体の問題ではなく、[レイテンシ](../Page/レイテンシ.md "wikilink")である）。性能問題を解決するにはそのレイテンシを考慮したアプリケーション設計をする必要がある\[8\]。Xのネットワーク機能が過度に複雑であるために、ローカルで使っても性能に悪影響があるという誤解を持つ人が多いが、現在のXの実装ではローカルな接続では単にソケットと共有メモリを使うので、X固有のオーバーヘッドはほとんどない。

## Xと競合するシステム

Unix系システムでは、グラフィックス表示にはXが使われるのが普通である。しかしXの代替となるシステムを開発しようという試みはいくつかある。歴史的には、[サン・マイクロシステムズ](../Page/サン・マイクロシステムズ.md "wikilink")の[NeWS](../Page/NeWS.md "wikilink")（市場では成功しなかった）、[NeXT](../Page/NeXT.md "wikilink")の[Display PostScript](../Page/Display_PostScript.md "wikilink")（[アップルが](../Page/アップル_\(企業\).md "wikilink")[Quartz](../Page/Quartz.md "wikilink")に置換した）、日本製の[GMW](https://ja.wikipedia.org/wiki/GMW "wikilink")があった。

Quartz開発者の1人であるMike Paquetteは、アップルがDisplay PostScriptからXに移行せずに独自のウィンドウサーバを開発した理由として、アップルが必要とする全ての機能をX11に追加してみたら、X11とは似ても似つかないものになり、他のXサーバとの互換性も失ってしまったと説明した\[9\]。

他にも、FrescoやY Window SystemといったXを置換することを意図したシステムもある。しかしXとの互換性を無視したこれらのシステムは、今のところ広く受けいれられてはいない。[Mir (ディスプレイサーバ)や](https://ja.wikipedia.org/wiki/Mir_\(ディスプレイサーバ\) "wikilink")[Wayland](https://ja.wikipedia.org/wiki/Wayland "wikilink")は互換性を重視している事もあって一応Linuxディストリビューションやプレインストールでの採用実績があるが、大きな流れには至っていない。

ハードウェアを直接操作することでXのオーバーヘッドに対処しようとした競合システムもある（例えば、DirectFBやFrameBuffer UI）。[ダイレクト・レンダリング・インフラストラクチャ](https://ja.wikipedia.org/wiki/ダイレクト・レンダリング・インフラストラクチャ "wikilink") (DRI) は、ほぼ同等の機能をX内で[モジュール](../Page/モジュール.md "wikilink")化したものと言え、それら競合システムの努力が無駄になる可能性もある。しかし、（[RTAI](https://ja.wikipedia.org/wiki/RTAI "wikilink")などを使った）[組み込みシステム](../Page/組み込みシステム.md "wikilink")用LinuxではDRIのリアルタイム性は思わしくなく、そのような応用にXは今のところ不向きと言える。

グラフィックス関連のサービスでネットワーク透過性を達成するその他の手段には、以下のものがある。

  - [SVG Terminal](http://networkimprov.net/airwrx/awscene.html) - [Scalable Vector Graphics](../Page/Scalable_Vector_Graphics.md "wikilink") (SVG) 形式のコンテンツをほぼリアルタイムでブラウザとやりとりして更新するプロトコル。
  - [Virtual Network Computing](../Page/Virtual_Network_Computing.md "wikilink") (VNC) - ネットワーク上で圧縮した[ビットマップを送る](../Page/ビットマップ画像.md "wikilink")。
  - [Citrix Presentation Server](https://ja.wikipedia.org/wiki/Citrix_Presentation_Server "wikilink") - Windows向けのXのような製品。
  - [タランテラは](../Page/タランテラ_\(企業\).md "wikilink")、[ウェブブラウザ](../Page/ウェブブラウザ.md "wikilink")を使う[Java](https://ja.wikipedia.org/wiki/Java "wikilink")クライアントを提供している。
  - RAWT ([Remote AWT](http://www-03.ibm.com/servers/eserver/zseries/software/java/rawt.html)) - [IBM](../Page/IBM.md "wikilink")のJavaによるクライアントサーバシステム

## 歴史

### 先駆的開発

X以前にも、ビットマップディスプレイを使ったシステムは存在していた。[ゼロックス](../Page/ゼロックス.md "wikilink")は[Alto](../Page/Alto.md "wikilink")（1973年）と[Star](../Page/Xerox_Star.md "wikilink")（1981年）を開発している。[アップルは](../Page/アップル_\(企業\).md "wikilink")[Lisa](../Page/Lisa_\(コンピュータ\).md "wikilink")（1983年）と [Macintosh](../Page/Macintosh.md "wikilink")（1984年）を開発した。UNIX関連では[Andrew Project](https://ja.wikipedia.org/wiki/Andrew_Project "wikilink")（1982年）と[ロブ・パイク](../Page/ロブ・パイク.md "wikilink")の[Blit](../Page/Blit.md "wikilink")端末（1984年）がある。

Xの名称は、それ以前の[W Window Systemの後継であることから名づけられた](../Page/W_Window_System.md "wikilink")。W Window Systemは[VというOS上で動作した](../Page/V_\(オペレーティングシステム\).md "wikilink")。Wはネットワークプロトコルを使って端末やグラフィックウィンドウをサポートし、サーバ側でディスプレイリストを管理する。

[thumb](https://ja.wikipedia.org/wiki/ファイル:X-Window-System.png "wikilink")、[xterm](https://ja.wikipedia.org/wiki/xterm "wikilink")、[xbiff](https://ja.wikipedia.org/wiki/xbiff "wikilink")、xload、グラフィカルな[manページ](https://ja.wikipedia.org/wiki/manページ "wikilink")ブラウザなど、MIT X Consortiumのディストリビューションにあったアプリケーションが動作している。\]\]

### 起源と初期の開発

Xの考え方が[MITで生まれたのは](../Page/マサチューセッツ工科大学.md "wikilink")1984年、Jim Gettys（[Project Athena](../Page/Project_Athena.md "wikilink")）とBob Scheifler（[MITコンピュータ科学研究所](https://ja.wikipedia.org/wiki/Project_MAC "wikilink")）によるものであった。ScheiflerはArgusというシステムの[デバッグ](../Page/デバッグ.md "wikilink")用の表示環境を必要としていた。Project Athena（[DEC](../Page/ディジタル・イクイップメント・コーポレーション.md "wikilink")、MIT、IBM によるコンピュータのユーザインタフェースを改善するプロジェクト）ではプラットフォームに依存せず、マルチベンダーシステムで利用できるグラフィックスシステムを必要としていた。当時、[カーネギーメロン大学](https://ja.wikipedia.org/wiki/カーネギーメロン大学 "wikilink")の[Andrew Projectでウィンドウシステムが開発中だったが](https://ja.wikipedia.org/wiki/Andrew_Project "wikilink")、ライセンス提供を受けることができず、他に代案もなかった。

解決策として、ローカルなアプリケーションも動作させることができ、リモートでも動作させることができるプロトコルの開発という考えが生まれた。1983年中ごろ、WがUNIXに移植された（Vのときの5分の1の速度）。1984年5月、Scheiflerは同期型だったWのプロトコルを非同期型に変更し、これがXバージョン 1となった。Xは世界初のハードウェアやベンダーに依存しないウィンドウシステム環境となった。

Scheifler、Gettys、Ron Newmanが開発を進め、Xは急速に進化していった。1985年1月にはバージョン 6をリリース。当時[Ultrix](../Page/Ultrix.md "wikilink")を搭載したワークステーションをリリースしようとしていたDECは、Xの搭載を決断した。DECの技術者がX6をDECのQVSSディスプレイ付き[MicroVAXに移植した](../Page/VAX.md "wikilink")。

1985年第二四半期、Xは[カラーをサポートし](../Page/X11の色名称.md "wikilink")、DEC [VAX](../Page/VAX.md "wikilink")station-II/GPXで動作した。これがバージョン 9となる。MITはX6を外部グループに料金を徴収してライセンスしていたが、X9リリース時点から[MIT Licenseを適用することとした](../Page/MIT_License.md "wikilink")。X9は 1985年9月にリリースされた。

[ブラウン大学](../Page/ブラウン大学.md "wikilink")のグループが[IBM RT-PCにX](../Page/IBM_RT-PC.md "wikilink")9を移植したが、整列されていないデータの読み込みで問題が発生し、プロトコルに非互換となる変更が必要となった。このため、1985年末にバージョン 10となった。1986年には外部からXについての問合せが増えてきた。X10R2は1986年1月、X10R3は1986年2月にリリース。X10R3では広く製品に採用されるようになった。DECとヒューレット・パッカードはX10R3ベースの製品をリリースし、他のグループが [アポロコンピュータ](../Page/アポロコンピュータ.md "wikilink")のマシンや[サン・マイクロシステムズ](../Page/サン・マイクロシステムズ.md "wikilink")のワークステーションへの移植を行い、IBM [PC/AT](https://ja.wikipedia.org/wiki/PC/AT "wikilink")への移植も行われた。このころ、Autofactという見本市でXを使った商用アプリケーションが初めてデモンストレーションされた（Cognition Inc.の機械系CAEシステム）。X10の最後のバージョンはX10R4で、1986年12月にリリースされた。

[Virtual Network Computing](../Page/Virtual_Network_Computing.md "wikilink") (VNC) がデスクトップの共有を可能にしているように、Xサーバをそのように拡張する試みはこのころから既に行われていた。例えば、Philip J. Gustの[SharedX](https://ja.wikipedia.org/wiki/SharedX "wikilink")ツールがある。

X10は強力な機能を持っていたが、Xプロトコルはさらに広く使われるようになる前に、もっとハードウェア中立となるよう再設計する必要があることがわかってきた。しかし、MIT だけではそのような全面的な再設計をするだけのリソースがなかった。そこでDECのWestern Software Laboratory (WSL) がこのプロジェクトに参加を申し出た。DEC WSLのSmokey WallaceとJim Gettysは、DEC WSLがX11を開発し、それをX9やX10と同じ条件でフリーにリリースすることを提案した。設計は1986年5月に開始され、8月にはプロトコルが完成した。アルファテストは1987年2月に開始され、ベータテストは1987年5月に開始された。X11のリリースは、[1987年](https://ja.wikipedia.org/wiki/1987年 "wikilink")[9月15日](../Page/9月15日.md "wikilink")に行われた。

Scheiflerが中心となって行われたX11プロトコルの設計は、USENETのニュースグループとオープンなメーリングリスト上で盛んに議論しながら進められた。したがって、Xは最初の大規模[フリーソフトウェア](../Page/フリーソフトウェア.md "wikilink")プロジェクトと言われることもある。

### MIT X ConsortiumとX Consortium, Inc.

1987年、X11の成功が明らかになると、MITはXの運営責任を放棄したいと考えるようになった。しかし、1987年6月に9社の主なベンダーが集まった会議で、各社はMITに対してXをまとめていくには中立的な団体が管理する必要があることを訴えた。1988年1月、*MIT X Consotium*が非営利の業界団体として設立された。責任者はScheiflerで、今後のX開発の方向性を業界と学界の動向を加味して決定することとなった。1988年1月にはJim Fulton、1988年3月には[キース・パッカード](https://ja.wikipedia.org/wiki/キース・パッカード "wikilink")が参加し、Jim は[Xlib](https://ja.wikipedia.org/wiki/Xlib "wikilink")/フォント/ウィンドウマネージャ/ユーティリティの開発、キースはサーバの再実装を分担するようになった。Donna ConverseとChris D. Petersonが同年末までに参加し、ツールキットとウィジェットを分担し、Project AthenaのRalph Swickと連携して作業を行った。MIT X ConsortiumはX11のリビジョンをいくつかリリースしていった。最初のX11R2は1988年2月にリリースされた。

1993年、MIT X Consortiumの後継としてX Consortium, Inc.（非営利組織）が設立された。そして、[1994年](../Page/1994年.md "wikilink")[5月16日](../Page/5月16日.md "wikilink")にX11R6をリリース。1995年には、[Motifツールキットと](../Page/Motif_\(GUI\).md "wikilink")[Common Desktop Environmentの開発管理も行うようになった](../Page/Common_Desktop_Environment.md "wikilink")。X Consortium, Inc.は1996年末には解散し、X11R6.3を最後にリリースした。コンソーシアム参加各社による囲い込みのような状況になったことが解散の原因とされている\[10\]\[11\]。

### The Open Group

1997年中ごろ、X Consortium, Inc.はXの管理運営を[The Open Groupに移管した](../Page/The_Open_Group.md "wikilink")。これは、[Open Software Foundationと](../Page/Open_Software_Foundation.md "wikilink")[X/Open](https://ja.wikipedia.org/wiki/X/Open "wikilink")が1996年初めに合併して結成された業界団体である。

The Open Groupは1998年初めにX11R6.4をリリースした。しかし、The Open GroupはXの開発資金を確かなものとするため、これまでのライセンス条件を変更し、これが議論を呼んだ\[12\]。新たな条件では、多くのプロジェクト（[XFree86](../Page/XFree86.md "wikilink")など）やいくつかの商用ベンダーでの採用が困難であった。これを受けてXFree86が分裂しそうになると、The Open Groupは1998年9月にX11R6.4を改めて従来のライセンス条件でリリースした\[13\]。The Open Groupの最後のリリースはX11R6.4 patch 3であった。

### X.OrgとXFree86

[XFree86](../Page/XFree86.md "wikilink")の起源は、Thomas RoellとMark W. Snitilyが1991年に書いた[PC/AT互換機](https://ja.wikipedia.org/wiki/PC/AT互換機 "wikilink")向けのX11R5であるX386 serverに遡る。Snitily Graphics Consulting Services (SGCS) はこれを1992年にMIT X Consortiumに寄贈した。XFree86は時と共に進化していき、Xの実装としての[デファクトスタンダード](../Page/デファクトスタンダード.md "wikilink")となった\[14\]。

1999年5月、The Open GroupはX.Orgを設立した（後の[X.Org Foundationとは異なる](../Page/X.Org_Foundation.md "wikilink")）。X.Orgは当時進行中だったX11R6.5.1のリリースを実施した。当時のX開発は壊滅寸前であった\[15\]。X Consortium, Inc.が解散した後の技術的進歩の多くはXFree86プロジェクトで生まれた\[16\]。1999年、XFree86はX.Orgの（会費を払わない）名誉会員となり\[17\]、XFree86とLinuxを製品に使いたいと思っていた多くのハードウェア企業がこれを歓迎した\[18\]。

2003年までにLinuxとXの組合せが非常に一般的になってきても、X.Orgは活発にはならず\[19\]、やはり開発の中心はXFree86であった。しかし、ここでXFree86内で大きな意見の相違が発生した。XFree86は、あまりにも[伽藍的開発モデルであり](../Page/伽藍とバザール.md "wikilink")、開発者は[CVSにコミットアクセスできず](../Page/Concurrent_Versions_System.md "wikilink")\[20\]\[21\]、ベンダーは多数の[パッチ](../Page/パッチ.md "wikilink")を保守する必要があった\[22\]。2003年3月、XFree86からキース・パッカードが追い出された。彼はMIT X Consortiumの消滅後にXFree86に参加していた\[23\]\[24\]\[25\]。

X.OrgとXFree86は、Xの開発を推進するための組織改編についての議論を開始した\[26\]\[27\]\[28\]。Jim Gettysは2000年ごろからオープンな開発モデルが必要であることを強調していた\[29\]。GettysとPackardは他の何人かと共に効率的なXのオープン開発の要求仕様について議論を開始した。

そしてX11R6.4のライセンス問題の結果、XFree86 version 4.4はより制限されたライセンスで2004年2月にリリースされ、Xを使っている多くのプロジェクトでこれを使うのが困難になった\[30\]。追加された条項は[BSDライセンス](../Page/BSDライセンス.md "wikilink")の宣伝条項に基づいており、[フリーソフトウェア財団](../Page/フリーソフトウェア財団.md "wikilink")も[Debian](../Page/Debian.md "wikilink")もこれを[GNU General Public License](../Page/GNU_General_Public_License.md "wikilink") (GPL) と非互換であるとした\[31\]。このライセンス問題とソース修正の困難さから、多くの人が分裂の機が熟したと感じていた\[32\]。

### X.Org Foundation

2004年初め、 X.Orgと[freedesktop.org](https://ja.wikipedia.org/wiki/freedesktop.org "wikilink")の様々な人々が集まり[X.Org Foundationが結成され](../Page/X.Org_Foundation.md "wikilink")、The Open Groupは`x.org`というドメイン名の権利を譲渡した。これにより、Xの管理運営は大きく変化した。1988年以来（前のX.Orgも含めて）Xの開発運営は業界団体が行っていた。しかし、X.Org Foundationはソフトウェア開発者が主導し、[バザールモデルに基づいたコミュニティによる開発であり](../Page/伽藍とバザール.md "wikilink")、外部からの参加に依存している。個人参加も可能で、企業がスポンサーとして参加することも可能である。現在、ヒューレット・パッカードなどの企業がX.Org Foundationに援助している。

FoundationはX開発における監督的役割を担う。技術的判断はコミュニティでの合意形成によってなされ、何らかの委員会で決定されるわけではない。これは[GNOME Foundationの非干渉主義的開発モデルに非常に近い](../Page/GNOME_Foundation.md "wikilink")。Foundationは開発者を雇っていない。

2004年4月、X.Org FoundationがXFree86 4.4RC2にX11R6.6の変更をマージしたX11R6.7をリリースした。GettysとPackardは、従来のライセンスのXFree86の最新版をベースとしてオープンな開発モデルを採用しGPLとの互換性を維持することで、かつてのXFree86開発者の多くを呼び戻した\[33\]。

2004年9月、X11R6.8がリリースされた。これには多くの新機能が追加された（透明なウィンドウサポート、その他の視覚効果のサポート、3次元表示サポートなど）。また、外部アプリケーションとして、[コンポジット型ウィンドウマネージャ](https://ja.wikipedia.org/wiki/コンポジット型ウィンドウマネージャ "wikilink")と呼ばれるもので見た目のポリシーを提供できるようになった。

[2005年](../Page/2005年.md "wikilink")[12月21日](../Page/12月21日.md "wikilink")、X.Orgは従来からのユーザー向けにモノリシックな[ソースコード](../Page/ソースコード.md "wikilink")であるX11R6.9と、同じコードをモジュール化して分割したX11R7.0をリリースした\[34\]\[35\]。[2006年](../Page/2006年.md "wikilink")[5月22日](../Page/5月22日.md "wikilink")、多数の機能強化を施したX11R7.1をリリースした\[36\]。

## 今後

X.Org Foundationとfreedesktop.orgにより、Xの中核部分の開発が再び加速された。これらの開発者は、単にベンダーによる製品化のベースとしてだけでなく、使用可能な最終製品として今後のバージョンをリリースしようとしている。

ハードウェアやOSとの関係を限定するため、X.Orgは表示用ハードウェアへのアクセスを[OpenGL](../Page/OpenGL.md "wikilink")と[ダイレクト・レンダリング・インフラストラクチャ](https://ja.wikipedia.org/wiki/ダイレクト・レンダリング・インフラストラクチャ "wikilink") (DRI) だけにすることを予定している。DRIはXFree86 version 4.0で登場し、X11R6.7以降で標準となった\[37\]。多くのOSがハードウェア操作のための[カーネル](../Page/カーネル.md "wikilink")サポートの追加を開始している。

## 名称

開発元のX.Org Foundationは、このソフトウェアを以下のいずれかの名前で呼ぶことを求めている\[38\]。

  - **X**
  - **X Window System**
  - **X Version 11**
  - **X Window System, Version 11**
  - **X11**

かつてはよく間違われたが、X Window Systemは「"X Window"というシステム」ではなく、「"X"というウィンドウシステム」である。また、X Window<span style="text-decoration:underline;">**s**</span>という表記は誤りである。

## Xで利用可能なウィジェット・ツールキット

  - [FLTK](../Page/FLTK.md "wikilink")

  - [GTK+](https://ja.wikipedia.org/wiki/GTK+ "wikilink")

  - [Motif](../Page/Motif_\(GUI\).md "wikilink")

  - [Qt](../Page/Qt.md "wikilink")

  - [Tk](../Page/Tk_\(ツールキット\).md "wikilink")

  - ([Project Athenaによるもの](../Page/Project_Athena.md "wikilink"))

  -
## リリース履歴

<table>
<thead>
<tr class="header">
<th><p>バージョン</p></th>
<th><p>リリース日</p></th>
<th><p>最も重要な変更</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>X1</p></td>
<td><p><a href="../Page/1984年.md" title="wikilink">1984年</a>6月</p></td>
<td><p>以前のシステムWから大幅に変更されたと言う意味で、最初のソフトウェアはXと呼ばれる。</p></td>
</tr>
<tr class="even">
<td><p>X6</p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/1985年" title="wikilink">1985年</a>1月</p></td>
<td><p>いくつかの企業にライセンスされる</p></td>
</tr>
<tr class="odd">
<td><p>X9</p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/1985年" title="wikilink">1985年</a>9月</p></td>
<td><p>色機能追加。<a href="../Page/MIT_License.md" title="wikilink">MIT License下で初めてリリース</a></p></td>
</tr>
<tr class="even">
<td><p>X10</p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/1985年" title="wikilink">1985年</a>後半</p></td>
<td><p><a href="../Page/IBM_RT-PC.md" title="wikilink">IBM RT-PC</a>、<a href="https://ja.wikipedia.org/wiki/PC/AT" title="wikilink">PC/AT</a>（の<a href="../Page/DOS_(OS).md" title="wikilink">DOS上</a>）等の<a href="https://ja.wikipedia.org/wiki/マシン" title="wikilink">マシン</a>での動作</p></td>
</tr>
<tr class="odd">
<td><p>X10R2</p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/1986年" title="wikilink">1986年</a>1月</p></td>
<td></td>
</tr>
<tr class="even">
<td><p>X10R3</p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/1986年" title="wikilink">1986年</a>2月</p></td>
<td><p>MIT の外部に初めてリリース。<a href="https://ja.wikipedia.org/wiki/uwm" title="wikilink">uwm</a>が標準のウィンドウマネージャ。</p></td>
</tr>
<tr class="odd">
<td><p>X10R4</p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/1986年" title="wikilink">1986年</a>12月</p></td>
<td><p>X10 の最後のリリース番号</p></td>
</tr>
<tr class="even">
<td><p>X11</p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/1987年" title="wikilink">1987年</a>9月15日</p></td>
<td><p>X11の最初のリリースであり、この時のバージョンのXプロトコルが基本的には2018年現在も使われている。</p></td>
</tr>
<tr class="odd">
<td><p>X11R2</p></td>
<td><p><a href="../Page/1988年.md" title="wikilink">1988年</a>1月</p></td>
<td><p>Xコンソーシアムによる最初のリリース。<a href="http://www.linuxdocs.org/HOWTOs/XWindow-User-HOWTO-2.html">1</a></p></td>
</tr>
<tr class="even">
<td><p>X11R3</p></td>
<td><p><a href="../Page/1988年.md" title="wikilink">1988年</a>10月25日</p></td>
<td><p><a href="../Page/X_Window_Display_Manager.md" title="wikilink">XDM</a>。</p></td>
</tr>
<tr class="odd">
<td><p>X11R4</p></td>
<td><p><a href="../Page/1989年.md" title="wikilink">1989年</a>12月22日</p></td>
<td><p>アプリケーションの改善、新しいフォント、<a href="https://ja.wikipedia.org/wiki/twm" title="wikilink">twm</a>が標準のウィンドウマネージャとして搭載される。</p></td>
</tr>
<tr class="even">
<td><p>X11R5</p></td>
<td><p><a href="../Page/1991年.md" title="wikilink">1991年</a></p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/PHIGS" title="wikilink">PHIGS</a>、カラーマネジメント、X386。<a href="../Page/国際化と地域化.md" title="wikilink">国際化機能</a></p></td>
</tr>
<tr class="odd">
<td><p>X11R6</p></td>
<td><p><a href="../Page/1994年.md" title="wikilink">1994年</a>5月16日</p></td>
<td><p><a href="../Page/Inter-Client_Communication_Conventions_Manual.md" title="wikilink">ICCCM</a> v2.0、<a href="../Page/ICE.md" title="wikilink">ICE</a>、Xセッションマネジメント、X同期拡張、Xイメージ拡張、XTEST拡張、Xインプット、X Big-Request拡張、XC-MISC、XFree86の変更。</p></td>
</tr>
<tr class="even">
<td><p>X11R6.1</p></td>
<td><p><a href="../Page/1996年.md" title="wikilink">1996年</a>3月14日</p></td>
<td><p>Xダブルバッファ拡張、Xキーボード拡張、X Record拡張。</p></td>
</tr>
<tr class="odd">
<td><p>X11R6.2<br />
X11R6.3 (Broadway)</p></td>
<td><p><a href="../Page/1996年.md" title="wikilink">1996年</a>12月23日</p></td>
<td><p>Web機能、 <a href="https://ja.wikipedia.org/wiki/LBX" title="wikilink">LBX</a>。Xコンソーシアムによる最後のリリース。X11R6.2はX11R6.3の部分機能バージョン。R6.1からの新機能はXPrintと、Xlibにおける縦書きと、ユーザー定義文字のサポートのみ。<a href="http://www.xfree86.org/3.3.6/RELNOTES1.html">2</a></p></td>
</tr>
<tr class="even">
<td><p>X11R6.4</p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/1998年" title="wikilink">1998年</a>3月31日</p></td>
<td><p><a href="../Page/Xinerama.md" title="wikilink">Xinerama</a>。<a href="http://www.opengroup.org/tech/desktop/Press_Releases/x11r6.4ga.htm">3</a></p></td>
</tr>
<tr class="odd">
<td><p>X11R6.5</p></td>
<td></td>
<td><p>X.orgの内部リリース。公開するためのものではない。</p></td>
</tr>
<tr class="even">
<td><p>X11R6.5.1</p></td>
<td><p><a href="../Page/2000年.md" title="wikilink">2000年</a>8月20日</p></td>
<td></td>
</tr>
<tr class="odd">
<td><p>X11R6.6</p></td>
<td><p><a href="../Page/2001年.md" title="wikilink">2001年</a>4月4日</p></td>
<td><p>バグ修正、XFree86変更。</p></td>
</tr>
<tr class="even">
<td><p>X11R6.7.0</p></td>
<td><p><a href="../Page/2004年.md" title="wikilink">2004年</a>4月6日</p></td>
<td><p>初めて X.Org 財団としてリリース、XFree86 4.4rc2 に統合。完全なエンドユーザー向け配布。XIE、PEX、libxml2の除去。 <a href="http://lwn.net/Articles/79302/">4</a></p></td>
</tr>
<tr class="odd">
<td><p>X11R6.8.0</p></td>
<td><p><a href="../Page/2004年.md" title="wikilink">2004年</a>9月8日</p></td>
<td><p>ウィンドウ透過、<a href="https://ja.wikipedia.org/wiki/XDamage" title="wikilink">XDamage</a>、<a href="https://ja.wikipedia.org/wiki/Distributed_Multihead_X" title="wikilink">Distributed Multihead X</a>、<a href="https://ja.wikipedia.org/wiki/XFixes" title="wikilink">XFixes</a>、Composite、<a href="https://ja.wikipedia.org/wiki/XEvIE" title="wikilink">XEvIE</a>。</p></td>
</tr>
<tr class="even">
<td><p>X11R6.8.1</p></td>
<td><p><a href="../Page/2004年.md" title="wikilink">2004年</a>9月17日</p></td>
<td><p><a href="../Page/XPM.md" title="wikilink">libxpmセキュリティ修正</a></p></td>
</tr>
<tr class="odd">
<td><p>X11R6.8.2</p></td>
<td><p><a href="../Page/2005年.md" title="wikilink">2005年</a>2月10日</p></td>
<td><p>バグ修正、ドライバのアップデート</p></td>
</tr>
<tr class="even">
<td><p>X11R6.9<br />
X11R7.0</p></td>
<td><p>2005年12月21日</p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/EXA" title="wikilink">EXA</a>、モジュール化及びビルド方式に関する大規模な<a href="../Page/リファクタリング_(プログラミング).md" title="wikilink">リファクタリング</a>。両者はソースコード自体は基本的には同一であるが、これまでのモノリシックな構成と<a href="https://ja.wikipedia.org/wiki/imake" title="wikilink">imake</a>によるコンフィグはこの6.9で凍結とされ、7.0からはモジュラー化され<a href="../Page/Autotools.md" title="wikilink">Autotools</a>を使用している。</p></td>
</tr>
<tr class="odd">
<td><p>X11R7.1</p></td>
<td><p>2006年5月22日</p></td>
<td><p>EXAの改良、<a href="https://ja.wikipedia.org/wiki/KDrive" title="wikilink">KDrive</a>の統合、<a href="../Page/AIGLX.md" title="wikilink">AIGLX</a>、BSD等のサポート。</p></td>
</tr>
<tr class="even">
<td><p>X11R7.2</p></td>
<td><p>2007年2月15日</p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/LBX" title="wikilink">LBX</a>とビルトインのキーボードドライバの除去。<a href="https://ja.wikipedia.org/wiki/XACE" title="wikilink">XACE</a>、<a href="../Page/XCB.md" title="wikilink">XCB</a>、autoconfigの改良、クリーンアップ。[39]</p></td>
</tr>
<tr class="odd">
<td><p>X11R7.3</p></td>
<td><p>2007年9月6日</p></td>
<td><p><a href="../Page/X.Org_Server.md" title="wikilink">XServer 1.4</a>、入力機器の<a href="https://ja.wikipedia.org/wiki/ホットプラグ" title="wikilink">ホットプラグ</a>、出力機器のホットプラグ (<a href="../Page/XRandR.md" title="wikilink">RandR</a> 1.2), <a href="../Page/DTrace.md" title="wikilink">DTrace</a>プローブ、<a href="../Page/Peripheral_Component_Interconnect.md" title="wikilink">PCIドメインのサポート</a>。[40]</p></td>
</tr>
<tr class="even">
<td><p>X11R7.4</p></td>
<td><p>2008年9月23日</p></td>
<td><p><a href="../Page/X.Org_Server.md" title="wikilink">XServer 1.5.1</a>、 XACE、PCIサブシステムのリワーク、EXAの高速化、_X_EXPORT、<a href="../Page/GLX.md" title="wikilink">GLX</a> 1.4、より高速なスタートアップとシャットダウン。[41]</p></td>
</tr>
<tr class="odd">
<td><p>X11R7.5</p></td>
<td><p>2009年10月26日</p></td>
<td><p><a href="../Page/X.Org_Server.md" title="wikilink">XServer 1.7</a>、Xi 2、XGE、E-<a href="https://ja.wikipedia.org/wiki/EDID" title="wikilink">EDID</a>のサポート、<a href="../Page/XRandR.md" title="wikilink">RandR</a> 1.3、<a href="https://ja.wikipedia.org/wiki/Multi-Pointer_X" title="wikilink">MPX</a>、予測可能なポインタのアクセラレーション、<a href="https://ja.wikipedia.org/wiki/ダイレクト・レンダリング・インフラストラクチャ" title="wikilink">DRI2メモリマネージャー</a>、SELinuxセキュリティモジュール、古くなったライブラリや拡張のさらなる除去。[42]</p></td>
</tr>
<tr class="even">
<td><p>X11R7.6</p></td>
<td><p>nowrap | 2010年12月20日</p></td>
<td><p><a href="../Page/X.Org_Server.md" title="wikilink">XServer 1.9</a>、XCBを要求。[43]</p></td>
</tr>
<tr class="odd">
<td><p>X11R7.7</p></td>
<td><p>nowrap | 2012年6月6日</p></td>
<td><p><a href="../Page/X.Org_Server.md" title="wikilink">XServer 1.12</a>、Sync extension 3.1 Fenceオブジェクト追加、Xi 2.2マルチタッチ、XFixes 5.0ポインターバリアー[44]</p></td>
</tr>
</tbody>
</table>

## 出典・脚注

## 関連項目

  - [ウィンドウマネージャ](../Page/ウィンドウマネージャ.md "wikilink")
  - [デスクトップ環境](https://ja.wikipedia.org/wiki/デスクトップ環境 "wikilink")
  - [XRender](../Page/XRender.md "wikilink")
  - [Xlib](https://ja.wikipedia.org/wiki/Xlib "wikilink")
  - [XCB](../Page/XCB.md "wikilink")
  - [W Window System](../Page/W_Window_System.md "wikilink")

## 参考文献

  - Hania Gajewska, Mark S. Manasse and Joel McCormack, [Why X Is Not Our Ideal Window System](http://www.std.org/~msm/common/protocol.pdf) [PDF](../Page/Portable_Document_Format.md "wikilink"), *Software — Practice & Experience* vol 20, issue S2 (October 1990)
  - Linda Mui and Eric Pearce, *X Window System Volume 8: X Window System Administrator's Guide for X11 Release 4 and Release 5, 3rd edition* O'Reilly and Associates, July 1993; softcover ISBN 0-937175-83-8
  - [The X-Windows Disaster](http://www.art.net/~hopkins/Don/unix-haters/x-windows/disaster.html) *UNIX-HATERS Handbook*
  - Robert W. Scheifler and James Gettys: *X Window System: Core and extension protocols: X version 11, releases 6 and 6.1*, Digital Press 1996, ISBN 1-55558-148-X
  - [The Evolution of the X Server Architecture](http://keithp.com/~keithp/talks/Xarchitecture/Talk.htm) キース・パッカード、1999年
  - [The means to an X for Linux: an interview with David Dawes from XFree86.org](http://web.archive.org/web/20060916213448/http://www.cat.org.au/maffew/cat/xfree-dawes.html) Matthew Arnison, CAT TV, June 1999
  - [Lessons Learned about Open Source](http://www.usenix.org/publications/library/proceedings/usenix2000/invitedtalks/gettys_html/Talk.htm) Jim Gettys, [USENIX](../Page/USENIX.md "wikilink") 2000 での X の歴史に関する講演資料
  - [On the Thesis that X is Big/Bloated/Obsolete and Should Be Replaced](http://cbbrowne.com/info/xbloat.html) Christopher B. Browne
  - [Open Source Desktop Technology Road Map](http://freedesktop.org/~jg/roadmap.html) Jim Gettys, [2003年](../Page/2003年.md "wikilink")[12月9日](../Page/12月9日.md "wikilink")
  - [X Marks the Spot: Looking back at X11 Developments of Past Year](http://www.osnews.com/story.php?news_id=6157) Oscar Boykin, *OSNews*, [2004年](../Page/2004年.md "wikilink")[2月25日](../Page/2月25日.md "wikilink")
  - [Getting X Off The Hardware](http://keithp.com/~keithp/talks/xserver_ols2004/) キース・パッカード、2004年7月 Ottawa Linux Symposium での講演資料
  - [Why Apple didn't use X for the window system](http://developers.slashdot.org/comments.pl?sid=75257&cid=6734612) Mike Paquette, Apple Computer
  - [X Man Page](http://ftp.x.org/pub/X11R6.8.2/doc/X.7.html) [2007年](../Page/2007年.md "wikilink")[2月2日](../Page/2月2日.md "wikilink")閲覧
  - [SNAP Computing and the X Window System](http://www.freedesktop.org/~jg/Papers/ols2005.pdf) Jim Gettys, [2005年](../Page/2005年.md "wikilink")

## 外部リンク

  - [XFree86](http://www.xfree86.org/)
  - [X.Org Foundation](http://www.x.org/)
  - [Xi Graphics,Inc.](http://www.xig.com/) (Accelerated-X の開発元)
  - [The X Window System: A Brief Introduction](http://www.linfo.org/x.html)
  - [Window managers for X](http://xwinman.org/)
  - [The State of Linux Graphics](http://jonsmirl.googlepages.com/graphics.html) Jon Smirl, [2005年](../Page/2005年.md "wikilink")[8月30日](../Page/8月30日.md "wikilink")
  - [Writing a Graphics Device Driver and DDX for the DIGITAL UNIX X Server](http://h30097.www3.hp.com/docs/dev_doc/DOCUMENTATION/HTML/AR5NHATE/TOC.HTM)
  - [Kenton Lee: Technical X Window System and Motif WWW Sites](http://www.rahul.net/kenton/xsites.html)
  - RFC 1198 - FYI on the X Window System

[Category:X_Window_System](https://ja.wikipedia.org/wiki/Category:X_Window_System "wikilink") [Category:ウィンドウシステム](https://ja.wikipedia.org/wiki/Category:ウィンドウシステム "wikilink") [Category:リモートデスクトップ](https://ja.wikipedia.org/wiki/Category:リモートデスクトップ "wikilink") [Category:UNIX](https://ja.wikipedia.org/wiki/Category:UNIX "wikilink")

1.  {{ cite web | url = <http://ftp.x.org/pub/X11R7.0/doc/html/LICENSE.html> | title = Licenses | work - X11 documentation | publisher = X.org | date = 2005-12-19 | accessdate = 2007-10-23 }}
2.  Robert W. Scheifler and James Gettys: X Window System: Core and extension protocols: X version 11, releases 6 and 6.1, Digital Press 1996,
3.
4.  [Announcement: Modification to the base XFree86(TM) license.](http://www.xfree86.org/pipermail/forum/2004-February/003945.html) 02 Feb 2004
5.  ["The X-Windows Disaster"](http://www.art.net/~hopkins/Don/unix-haters/x-windows/disaster.html)
6.  [Re: X is painful](http://lists.debian.org/debian-user/1996/11/msg00637.html) 15 Nov 1996
7.  [SNAP Computing and the X Window System](http://www.freedesktop.org/~jg/Papers/ols2005.pdf) 2005
8.  [An LBX Postmortem](http://keithp.com/~keithp/talks/lbxpost/paper.html) 2001-1-24
9.  [Why Apple didn't use X for the window system](http://developers.slashdot.org/comments.pl?sid=75257&cid=6734612) August 19, 2007
10. [Financing Volunteer Free Software Projects](http://www.advogato.org/article/844.html) 10 Jun 2005
11. [Lessons Learned about Open Source](http://www.usenix.org/publications/library/proceedings/usenix2000/invitedtalks/gettys_html/) 2000
12. [X statement](http://old.lwn.net/lwn/1998/0409/xstate.html) 02 Apr 1998
13. [X11R6.4 Sample Implementation Changes and Concerns](http://cbbrowne.com/info/x11r6.4.html)
14. [Announcement: Modification to the base XFree86(TM) license.](http://www.xfree86.org/pipermail/forum/2004-February/003945.html) 02 Feb 2004
15. [Q\&A: The X Factor](http://www.computerworld.com/softwaretopics/software/appdev/story/0,10801,67861,00.html) February 04, 2002
16. [The Evolution of the X Server Architecture](http://keithp.com/~keithp/talks/Xarchitecture/Talk.htm) 1999
17. [A Call For Open Governance Of X Development](http://xfree86.org/pipermail/forum/2003-March/000418.html) 23 Mar 2003
18. [XFree86 joins X.Org as Honorary Member](http://slashdot.org/articles/99/12/01/1342251.shtml) Dec 01, 1999
19. [Another teleconference partial edited transcript](http://xfree86.org/pipermail/forum/2003-April/003127.html) 13 Apr 2003
20. [Keith Packard issue](http://www.xfree86.org/pipermail/forum/2003-March/002018.html) 20 Mar 2003
21. [Cygwin/XFree86 - No longer associated with XFree86.org](http://cygwin.com/ml/cygwin-xfree/2003-10/msg00328.html) 27 Oct 2003
22. [On XFree86 development](http://www.advogato.org/person/mharris/diary.html?start=5) 9 Jan 2003
23. [Invitation for public discussion about the future of X](http://www.xfree86.org/pipermail/forum/2003-March/001997.html) 20 Mar 2003
24. [A Call For Open Governance Of X Development](http://www.xfree86.org/pipermail/forum/2003-March/002165.html) 21 Mar 2003
25. [Notes from a teleconference held 2003-3-27](http://www.xfree86.org/pipermail/forum/2003-April/003016.html) 03 Apr 2003
26. [A Call For Open Governance Of X Development](http://www.xfree86.org/pipermail/forum/2003-March/000554.html) 24 Mar 2003
27. [A Call For Open Governance Of X Development](http://www.xfree86.org/pipermail/forum/2003-March/002415.html) 23 Mar 2003
28. [Discussing issues](http://xfree86.org/pipermail/forum/2003-April/003144.html) 14 Apr 2003
29. [Lessons Learned about Open Source](http://www.usenix.org/publications/library/proceedings/usenix2000/invitedtalks/gettys_html/Talk.htm) 2000
30. [XFree86 4.4: List of Rejecting Distributors Grows](http://yro.slashdot.org/article.pl?sid=04/02/18/131223) Feb 18, 2004
31. [Appendix A: The Cautionary Tale of XFree86](http://www.dwheeler.com/essays/gpl-compatible.html#xfree86) June 5, 2002
32. [X Marks the Spot: Looking back at X11 Developments of Past Year](http://www.osnews.com/story.php/6157/X-Marks-the-Spot-Looking-back-at-X11-Developments-of-Past-Year/) Feb 25, 2004
33. [Appendix A: The Cautionary Tale of XFree86](http://www.dwheeler.com/essays/gpl-compatible.html#xfree86) June 5, 2002
34. [X11R6.9 and X11R7.0 Officially Released](http://xorg.freedesktop.org/wiki/Other/Press/X11R6970Released?action=show&redirect=PressReleases%2FX11R6970Released) December 21 2005
35. [Modularization Proposal](http://wiki.x.org/wiki/ModularizationProposal) 2005-03-31
36. [Proposed Changes for X11R7.1](http://xorg.freedesktop.org/wiki/ChangesForX11R71) 2006-04-21
37. [Getting X Off The Hardware](http://keithp.com/~keithp/talks/xserver_ols2004/) July, 2004
38. [X - a portable, network-transparent window system](http://ftp.x.org/pub/X11R6.8.2/doc/X.7.html) 2005年2月
39. [Releases/7.2](http://www.x.org/wiki/Releases/7.2)
40. [Releases/7.3](http://www.x.org/wiki/Releases/7.3)
41. [Releases/7.4](http://www.x.org/wiki/Releases/7.4)
42. [Releases/7.5](http://www.x.org/wiki/Releases/7.5)
43. [Releases/7.6](http://www.x.org/wiki/Releases/7.6)
44. [Releases/7.7](http://www.x.org/wiki/Releases/7.7)
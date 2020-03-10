> この記事は[VirtualBox](https://ja.wikipedia.org/wiki/VirtualBox)から翻訳されています。


**Oracle VM VirtualBox** （オラクル ブイエム バーチャルボックス）とは、[x86](https://ja.wikipedia.org/wiki/x86 "wikilink")ならびに[AMD64/Intel64にかかる仮想化ソフトウェア](https://ja.wikipedia.org/wiki/x64 "wikilink")・パッケージの一つ\[1\]。現在の開発は[米国](https://ja.wikipedia.org/wiki/米国 "wikilink")[オラクルが行っている](https://ja.wikipedia.org/wiki/オラクル_\(企業\) "wikilink")。

## 概要

既存のオペレーティング・システム（**ホストOS**）上にアプリケーションの一つとしてインストールされ、この中で追加のオペレーティング・システム（**ゲストOS**）を実行することができる。例えば、[Microsoft Windowsが](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")「ホストOS」として動作しているマシン上で、[Linux](https://ja.wikipedia.org/wiki/Linux "wikilink")をゲストとすることができる。あるいは、[Solaris](../Page/Solaris.md "wikilink")が実行されているマシン上で、[Microsoft Windowsを](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")「ゲストOS」として実行することができる。

サポートされるホストOSは[Linux](https://ja.wikipedia.org/wiki/Linux "wikilink")、[macOS](https://ja.wikipedia.org/wiki/macOS "wikilink")、[Microsoft Windows](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")、そしてSolaris。また後述するようにソースコードが配布されているため、他の[Unix系](../Page/Unix系.md "wikilink")のOSでも導入できる。例えば[FreeBSD](../Page/FreeBSD.md "wikilink")ではportsで導入することができる。

ゲストOSとしてサポートされるのは、FreeBSD、Linux、[OpenBSD](../Page/OpenBSD.md "wikilink")、[OS/2 Warp](https://ja.wikipedia.org/wiki/OS/2 "wikilink")、Windows、[Mac OS X Server](https://ja.wikipedia.org/wiki/macOS_Server "wikilink")\[2\]、Solarisなど多岐にわたる\[3\]が、x86/x64アーキテクチャのOSであれば基本的には動作する。

DesktopLinux.com の2007の調査によると、VirtualBoxは、Linuxデスクトップ上でWindowsプログラム群を走らせる三番目に人気のあるソフトウェア・パッケージであった\[4\]。

### 歴史

当初は[プロプライエタリ・ソフトウェア](../Page/プロプライエタリ・ソフトウェア.md "wikilink")・ライセンスで提供され、製品*VirtualBox*のある版は、個人的あるいは評価の使用に対してのみ無料であり、「VirtualBox Personal Use and Evaluation Licence (PUEL)」が適用された。\[5\] 2007年1月、数年の開発の後、VirtualBox OSE（Open Source Edition）が[フリーソフトウェア](../Page/フリーソフトウェア.md "wikilink")として、商用と個人的な使用のためにリリースされ、[GNU General Public License](../Page/GNU_General_Public_License.md "wikilink") (GPL) version 2が適用された\[6\]。

VirtualBoxの開発元であったinnotekは、[コネクティクス](https://ja.wikipedia.org/wiki/コネクティクス "wikilink")の仮想化製品（後に[マイクロソフト](../Page/マイクロソフト.md "wikilink")により買収）に対して、[OS/2](https://ja.wikipedia.org/wiki/OS/2 "wikilink")と[Linux](https://ja.wikipedia.org/wiki/Linux "wikilink")の仮想化のサポートの開発\[7\]や、OS/2への移植\[8\] にも貢献した。特に、innotekは[Microsoft Virtual PCと](https://ja.wikipedia.org/wiki/Microsoft_Virtual_PC "wikilink")[Microsoft Virtual Serverの両方に含まれる](../Page/Microsoft_Virtual_Server.md "wikilink")「付加」コードを開発し、これはホスト・ゲスト間の相互作用を大いに進歩させた。OS/2は拡張された[リングプロテクション](https://ja.wikipedia.org/wiki/リングプロテクション "wikilink")が複雑であり、仮想化で実行するのは困難だった。

2008年2月にInnotekは[サン・マイクロシステムズ](../Page/サン・マイクロシステムズ.md "wikilink")により買収され\[9\]\[10\]\[11\]、これに伴ってバージョン1.6より製品表記がSun xVM VirtualBoxに改められた。

その後、2010年1月にサンもオラクルに買収された。これに伴ってバージョン3.20より権利表記の変更が再び行われ、また製品表記が**Oracle VM VirtualBox**に改められ、現在に至っている。

### 配布形態の変遷

バージョン4.0以降のVirtualBoxは[GNU General Public License](../Page/GNU_General_Public_License.md "wikilink") (GPL) Version 2でライセンスされる完全なオープンソースソフトウェア（OSS）であるが、バージョン3.x以前ではプロプライエタリ版とOSS版の2つの配布形態があった。

プロプライエタリ版はバイナリのみの配布で、個人や教育あるいは評価目的の製品の利用は無料であった\[12\]。商業目的のためのライセンスはサン及びオラクルから購入することができた。

OSS版は*VirtualBox Open Source Edition (OSE) - オープンソース版*と呼ばれ、GNU GPLの元に公開されている[フリーソフトウェア](../Page/フリーソフトウェア.md "wikilink")であった。4.x以降はこちらがベースとなっている。プロプライエタリ版と比較すると、特許等の都合でソースが非公開となっている機能が欠けていた\[13\]。

バージョン4.0よりOSS版にプラグイン機能が搭載され、機能の追加が可能となった。これに伴い、オラクルにより提供されていた上記二つの版は統合され、本体をオープンソースで、追加機能をプラグイン（ライセンスは提供元の都合でプロプライエタリでもオープンソースでも良い）として提供する形態となった。3.x以前でプロプライエタリ版のみに含まれていた機能はオラクルから「Oracle VM VirtualBox Extension Pack」として提供されている（詳細は後述）。

## 機能

[thumb](https://ja.wikipedia.org/wiki/ファイル:Virtualbox-web-interface-console.png "wikilink") VirtualBox本体により提供される基本機能は次の通り。

  - スナップショット
  - シームレス・モード
  - クリップボード
  - 共有フォルダ
  - シリアルデバイスと、システム間の切替えを支援するユーティリティ
  - コマンドラインからの操作（GUIに追加）
      - GUIでサポートされていない機能が一部ある。
  - リモート・ディスプレイ（ヘッドレス：モニターのないホストマシンの場合に有用）

<!-- end list -->

  - 64ビット・ゲスト
  - [AMD-V](https://ja.wikipedia.org/wiki/x86仮想化 "wikilink") と [VT-xのための](../Page/インテル_バーチャライゼーション・テクノロジー.md "wikilink")、入れ子(ネステッド)・[ページング](https://ja.wikipedia.org/wiki/ページング "wikilink")
  - 3Dアクセラレーション（ゲストOSが32ビットの[Windows XPおよび](https://ja.wikipedia.org/wiki/Windows_XP "wikilink")[Vistaの場合](https://ja.wikipedia.org/wiki/Microsoft_Windows_Vista "wikilink")）

3Dアクセラレーションはバージョン2.0で追加され、3.0で実験的に[DirectX](https://ja.wikipedia.org/wiki/DirectX "wikilink") 9のサポートがなされている。ただし、では32ビットのWindows XPおよびVistaゲスト環境に限定されており、64ビット環境ではサポートされない（[Windows 7の](https://ja.wikipedia.org/wiki/Windows_7 "wikilink")64bit版から起動した場合はWindows XPのゲスト環境でDirectX 9が一応動作する）。また、4.0系まではWindowsゲスト環境におけるビデオドライバが[WDDM](https://ja.wikipedia.org/wiki/WDDM "wikilink")のものではないため、Windows Vista以降の[Desktop Window Managerによるデスクトップコンポジション機能や](https://ja.wikipedia.org/wiki/Desktop_Window_Manager "wikilink")[Aeroテーマを動作させることはできなかったが](../Page/Windows_Aero.md "wikilink")、4.1系から実験的にWDDMドライバサポートが開始されている。

## エミュレートされる環境

複数のゲストOSを管理・起動することができ、同時に起動することもできる。それぞれのゲストOSは、独立して開始、稼働の一時停止、起動したままの状態を保っての保存と復帰（後述のGuest Additionsを入れないと時間同期の問題が生じる場合がある）、終了することができる。

複数のオペレーティング・システムを同時に走らせる場合、使用可能なメモリ量が重要な要素となる。理論上の割り当て限界はホストOS側のメモリ容量までとなるが、実際はシステムやホストOS側で動作しているアプリもあるので、そのぶんを計算して割り当てる必要がある。割り当て論理CPUコア数やメモリ割り当て容量は仮想マシン停止中であれば容易に調整可能である。

※ただしWindowsXPの場合、OSインストール後はCPUコア数は通常の方法では変更できないので、OSインストール時にあらかじめCPUコア数を設定してインストールを行うのが最も簡単な方法である。（ちなみにインストール後の変更には適切なドライバのインストールやboot.iniの編集などいくらかの手間のかかる方法で行う必要がある。）

※サポートされていないＯＳであってもx86/x64アーキテクチャのOSであれば基本的には動作することから、ゲストに Windows98, SEなどをインストールする記事を見るが、入手困難であるＣＤ起動の「９８SE」を使用している例が多い。「９８」と「ＳＥ」のファイルを合成してインストール成功したとの記事を「Windows98」欄で見受けた。

### ハードウェア・エミュレーション

VirtualBoxは、ハードウェアによる仮想化支援機能として、[VT-x](https://ja.wikipedia.org/wiki/インテル_バーチャライゼーション・テクノロジー#VT-x "wikilink")（[インテル](https://ja.wikipedia.org/wiki/インテル "wikilink")）と、[AMD-V](https://ja.wikipedia.org/wiki/x86仮想化 "wikilink")（[AMD](https://ja.wikipedia.org/wiki/アドバンスト・マイクロ・デバイセズ "wikilink")）への対応を含む。対応当初はデフォルトでどちらも有効となっていなかったが\[14\]、現在のバージョンで提供される機能の一部（x86_64対応、マルチコア対応）には、これらの仮想化支援機能を必要とするものがある。バージョン5.0より[KVMが選択可能になり](https://ja.wikipedia.org/wiki/Kernel-based_Virtual_Machine "wikilink")、[Linux](https://ja.wikipedia.org/wiki/Linux "wikilink")においてハードウェアエミュレーションのオーバーヘッドが削減可能になった。なお、VirtualBox用のチップセットのエミュレーションにはインテルの[82441FXチップセットが用いられている](https://ja.wikipedia.org/wiki/Intel_440FX "wikilink")。

#### ハードディスク

ハードディスクドライブは、通常「仮想ディスク・イメージ (Virtual Disk Images)」と呼ばれる他の仮想化ソリューションとは互換性のない特別なコンテナ・フォーマットとしてエミュレートされる。これらは、ホストOS上のシステムファイル（拡張子 .vdi）として格納される。別の方法として、VirtualBoxは[iSCSI](https://ja.wikipedia.org/wiki/iSCSI "wikilink")ターゲットとの接続が可能で、それらを仮想ハードディスク群として使用することが出来る。

この他、他の仮想マシンソフトウェアで用いられる、vmdk形式 ([VMware](https://ja.wikipedia.org/wiki/VMware "wikilink"))、vhd形式 ([Microsoft Virtual PC](https://ja.wikipedia.org/wiki/Microsoft_Virtual_PC "wikilink"))、hdd形式 ([Parallels](../Page/パラレルス.md "wikilink")) などの仮想ディスクイメージにも対応する。ただし、これらディスクイメージは本来VirtualBox向けのフォーマットではない為、フォーマットのバージョンとVirtualBoxのバージョンの対応など、利用に当たっては互換性の面における注意が必要であるが、有志によりコンバートユーティリティがいくつか開発されており、（当然無保証となるが）これらの仮想ディスク形式において相互変換可能な環境がそろいつつある。

#### 光学ドライブ

CDやDVDドライブとして[ISOイメージ](https://ja.wikipedia.org/wiki/ISOイメージ "wikilink")が使用できる。例えば、LinuxディストリビューションのDVDイメージをダウンロードして、直接 VirtualBoxで使用することが出来る。その場合、ISOイメージをCD-RやDVD-RWといった物理メディアに焼き込む必要がない。また、物理的ディスクを仮想マシンから直接的にマウントすることも可能である。

#### グラフィック機能

標準で16MBのVRAMを搭載する[VESA](../Page/VESA.md "wikilink")カードをグラフィック機能として提供する（VRAMの値は128MBを上限として調節可能）。ゲストOSとしてWindows、macOS、Linux あるいはSolarisを使用する場合、Guest Additionsとして提供される追加のグラフィック・ドライバにより、描画性能の向上と機能の追加が可能である。例として、ホストOS上で仮想マシンのウインドウサイズを変更した場合、ゲストOSの解像度が動的に変更される。また、バージョン2.1以降においては、追加のグラフィック・ドライバにより、[OpenGL](../Page/OpenGL.md "wikilink")やDirectX 9などの3D描画に対応する（停止中に3D/2Dアクセラレーションフラグを有効にする必要がある）。

#### ネットワーク機能

[イーサネット・アダプタとして](https://ja.wikipedia.org/wiki/ネットワークカード "wikilink")、AMD PCnet-PCI II (Am79C970A), AMD PCnet-FAST III (Am79C973), Intel PRO/1000 MT Desktop (82540EM), Intel PRO/1000 T Server (82543GC), Intel PRO/1000 MT Server (82545EM) のいずれかを仮想化する。これらの仮想化されたアダプタによる外部との接続手段として、[NAT](../Page/ネットワークアドレス変換.md "wikilink")（ホストOSによるNAPT機能）、ブリッジアダプタ（ホストOSの物理インターフェースとのブリッジ機能）、内部ネットワーク（ゲストOS同士を接続する内部的なネットワーク）、ホストオンリーアダプタ（ホストOS上の仮想Ethernetアダプタと直接的に接続する）が提供される。 新規作成される仮想マシンは、いずれかのアダプタとNATの組み合わせが設定される。ゲストOS上のアプリケーションは、これによりホストOSを経由して外部との通信が可能となる。NATを提供するホストOSは、一般的なブロードバンドルータと同様の動作を行う。

バージョン5.0から[準仮想化](../Page/準仮想化.md "wikilink")機能が搭載され始め、''準仮想化ネットワーク (virtio-net) ''が選択可能になった。この仮想ネットワークインターフェースを利用することで、VirtualBoxがvirtio-netのドライバを持つOSのカーネルと協調してVirtualBox上のゲストOSと物理ネットワークインターフェースの間で直接データを受け渡しすることが可能になり、ネットワークにおけるエミュレーションのオーバーヘッドを削減することが可能になる。

#### オーディオ機能

オーディオ・カードとして、VirtualBoxは、[Intel HDオーディオ](https://ja.wikipedia.org/wiki/High_Definition_Audio "wikilink")、[ICH AC'97](../Page/Audio_Codec_97.md "wikilink")（デフォルト）、[SoundBlaster 16カードのいずれかを仮想化する](https://ja.wikipedia.org/wiki/SoundBlaster_16 "wikilink")（ただし、Intel HDオーディオは、対応するゲストOSに制限がある）。

### 追加の機能

バージョン4.0より、Extension Packageと呼ばれる機能拡張プラグインが導入された。これは、4.0よりVirtualBox本体がGPLライセンスとなったために、プロプライエタリ・ソフトウェアによる機能を標準で実装することができなくなったために設けられたものである。

Oracleから「Oracle VM VirtualBox Extension Pack」と呼ばれる機能拡張プラグインを配布しており、これにより以下の機能が提供される。

  - USB 2.0 コントローラ （EHCI）
  - USB 3.0 コントローラ （xHCI）（バージョン5.0から追加）
  - [Remote Desktop Protocol](../Page/Remote_Desktop_Protocol.md "wikilink")（RDP）による遠隔制御機能 （マイクロソフトおよびシトリクスにより開発された、プロプライエタリな遠隔制御プロトコル。つまりWindowsの[リモートデスクトップ](https://ja.wikipedia.org/wiki/リモートデスクトップ "wikilink")クライアントや[rdesktop](https://ja.wikipedia.org/wiki/rdesktop "wikilink")ソフトウェアから接続することが可能）
  - ホストのウェブカメラのパススルー機能（ゲスト側からホストのウェブカメラを透過的に使用できるようにする機能、バージョン4.3から追加）
  - LinuxホストにおけるPCIバスパススルー機能（バージョン6.0まで。ゲスト側からPCIデバイスを透過的に使用可能にする機能、実験的機能）
  - Intelカードによる[PXEブート機能](https://ja.wikipedia.org/wiki/Preboot_Execution_Environment "wikilink")
  - シームレスモード （ホストOSとゲストOSのデスクトップの操作を統合する機能）
  - ゲスト仮想ディスクの暗号化（バージョン5.0から追加）

初回のみ別途ダウンロード及びインストールが必要。一度インストールすればVirtualBox本体をアップデートしたあとの初回起動時にExtension Packのアップデートをするか聞かれ、応じればそのままアップデート作業に入るため別途ダウンロードの必要はない。またインストール後はパッケージを削除するか聞かれるので、応じれば自動的に削除される仕様となっている。

## phpVirtualBox

[phpVirtualBox](https://ja.wikipedia.org/wiki/phpVirtualBox "wikilink")とは、VirtualBoxをWebブラウザで操作するためのウェブサービスソフトウェア。その名のとおりサーバサイトは[PHPで記述されている他](../Page/PHP_\(プログラミング言語\).md "wikilink")、インターフェースまわりに[Ajax](https://ja.wikipedia.org/wiki/Ajax "wikilink")が用いられている。動作にはPHP動作をサポートするWebサーバ、PHP、VirtualBoxが必要。GUIでできることはほぼすべてできるようになっている。

## 技術解説

VirtualBoxは[Intel VTか](../Page/インテル_バーチャライゼーション・テクノロジー.md "wikilink")[AMD AMD-Vかいずれかのハードウェア仮想化をサポートするCPU上で効率的かつ安全な仮想化を実現する](https://ja.wikipedia.org/wiki/x86仮想化 "wikilink")\[15\]。 その一方で、これら2つの仮想化技術のいずれもサポートしていないCPUについてはソフトウェア的な仮想化を行う（バージョン6.0まで。6.1からはハードウェア仮想化必須）。 高性能なソフトウェア仮想化を実現するために、VirtualBoxはゲストコードの実行時分析や実行時改変を含む複雑なメカニズムを実装する。 性能上の大きな問題となるのは、最高の特権レベルであるリング0で実行されるべき特権命令のエミュレーションである。 ハードウェア仮想化を使用しない場合、ゲストコードをリング0で実行できないので代替実行手段が必要になる。 特権命令が不適切な特権レベルで実行される度に発生するトラップを捉えて対応するナイーブな対策は、性能低下が著しく現実的ではない。 そこで、VirtualBoxは実行時に必要に応じてリング0で実行されるべきコード片を分析し、特権命令をエミュレーション用コードで置き換えた効率的に実行可能なコード片を用意する。 この改変済みコード片は再利用可能なので、実行時コード改変のコストは多くの状況で償却し、全体的な性能向上が実現する。

[macOS](https://ja.wikipedia.org/wiki/macOS "wikilink")版では、ネットワーク・ブリッジ（ホストインターフェース）がサポートされていなかったが、バージョン2.0でサポートされた。

## 関連項目

  - [w:Comparison of virtual machines](https://ja.wikipedia.org/wiki/w:Comparison_of_virtual_machines "wikilink") - 仮想マシンの比較
  - [x86仮想化](https://ja.wikipedia.org/wiki/x86仮想化 "wikilink")
      - [VMware](https://ja.wikipedia.org/wiki/VMware "wikilink")
      - [Hyper-V](../Page/Hyper-V.md "wikilink")
  - [Vagrant](https://ja.wikipedia.org/wiki/Vagrant_\(ソフトウェア\) "wikilink")

## 脚注

## 外部リンク

  - [Virtualbox Project Page](https://www.virtualbox.org/)
  - [Oracle's Virtualization Blog](https://blogs.oracle.com/virtualization/)  - 開発者ブログ
  - [phpVirtualBox](https://sourceforge.net/projects/phpvirtualbox/)

[Category:仮想化](https://ja.wikipedia.org/wiki/Category:仮想化 "wikilink") [Category:オープンソースソフトウェア](https://ja.wikipedia.org/wiki/Category:オープンソースソフトウェア "wikilink") [Category:サン・マイクロシステムズ](https://ja.wikipedia.org/wiki/Category:サン・マイクロシステムズ "wikilink") [Category:オラクル](https://ja.wikipedia.org/wiki/Category:オラクル "wikilink") [Category:Qtを使用するソフトウェア](https://ja.wikipedia.org/wiki/Category:Qtを使用するソフトウェア "wikilink") [Category:エミュレーションソフトウェア](https://ja.wikipedia.org/wiki/Category:エミュレーションソフトウェア "wikilink")

1.  [1](http://web.archive.org/web/20191125193335/https://www.virtualbox.org/)
2.  すべてのホスト向けでゲストOSとしてリストされているが、Apple製のハードウェア以外で動かすことはライセンス違反になる。
3.  [VirtualBoxウェブサイトのページ "Status: Guest OSes"](https://www.virtualbox.org/wiki/Guest_OSes)
4.
5.  [VirtualBox_PUEL - VirtualBox](https://www.virtualbox.org/wiki/VirtualBox_PUEL)
6.  <https://www.virtualbox.org/wiki/GPL> "The VirtualBox Open Source Edition is licensed under the GPL V2."
7.  [Microsoft Virtual PC Additions Version History](https://groups.google.com.au/group/microsoft.public.virtualpc/msg/1dbfbc16da8ac9af)
8.  [Connectix Announces First Virtual Computing Solution for OS/2 User](http://archive.is/20120711113943/findarticles.com/p/articles/mi_m0EIN/is_2002_July_1/ai_88090458)
9.
10. [Ecommerce Article about the acquisition by Sun, 13 February 2008](http://www.ecommercetimes.com/story/61661.html)
11.
12. [VirtualBox license page](https://www.virtualbox.org/wiki/VirtualBox_PUEL)
13. ["Editions" page on VirtualBox website](https://www.virtualbox.org/wiki/Editions)
14. ["Developer FAQ" page on VirtualBox website](https://www.virtualbox.org/wiki/Developer_FAQ)
15. ["Technical Background" page on VirtualBox website](https://www.virtualbox.org/manual/ch10.html#idp96960240)
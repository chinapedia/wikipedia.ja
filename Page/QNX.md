> この記事は[QNX](https://ja.wikipedia.org/wiki/QNX)から翻訳されています。


**QNX**（キューエヌエックス、またはキューニックスと発音）は商用の[リアルタイム](../Page/リアルタイムオペレーティングシステム.md "wikilink")[Unix系](../Page/Unix系.md "wikilink")オペレーティングシステムであり、[POSIX](../Page/POSIX.md "wikilink")と[POSIX 1003.1bに対応している](https://ja.wikipedia.org/wiki/POSIX_1003.1b "wikilink")。主に[組み込みシステム](../Page/組み込みシステム.md "wikilink")向けに販売されている。元々はカナダの企業QNXソフトウェアシステムズが開発していたが、同社は後にリサーチ・イン・モーション（現[ブラックベリー](https://ja.wikipedia.org/wiki/ブラックベリー_\(企業\) "wikilink")）が取得した。

## 詳細

[マイクロカーネル](https://ja.wikipedia.org/wiki/マイクロカーネル "wikilink")OSとして、QNXではOSのほとんどが「サーバ」と呼ばれる小さなタスクとして動作する。この点は従来からのモノリシックな[カーネル](../Page/カーネル.md "wikilink")を採用したOSと大きく異なる。[モノリシックカーネル](../Page/モノリシックカーネル.md "wikilink")OSでは機能の大部分はひとつの大きなプログラムに含まれ、例えば不要な機能をOFFにしたい時などにはOS自体を変更（再[リンク](../Page/リンク.md "wikilink")など）する必要がある。それに対しQNXではユーザや開発者はサーバを停止させることで簡単に不要な機能をOFFにすることができる。

QNXのシステムは非常に小さく、[フロッピーディスク](../Page/フロッピーディスク.md "wikilink")1枚に納まるシステムでGUIが使えウェブがブラウズできるというデモシステムすらある\[1\]。そして非常に高速であり機能的にも完備されている。

[2001年](../Page/2001年.md "wikilink")にリリースされた QNX Neutrinoは現在組み込み市場で使われているほとんどの[CPU](../Page/CPU.md "wikilink")で動作する。例えば、[x86](https://ja.wikipedia.org/wiki/x86 "wikilink")ファミリ、[MIPS](../Page/MIPSアーキテクチャ.md "wikilink")、[PowerPC](../Page/PowerPC.md "wikilink")、[SH-4](../Page/SuperH.md "wikilink")、[ARM](../Page/ARMアーキテクチャ.md "wikilink")、[StrongARM](../Page/StrongARM.md "wikilink")、[XScale](../Page/XScale.md "wikilink")などである。

2007年9月12日、非商用利用のためのライセンスも用意するようになった。

QNXを現在所有しているのは[ブラックベリーであり](https://ja.wikipedia.org/wiki/ブラックベリー_\(企業\) "wikilink")、同社の[タブレットコンピュータ用](../Page/タブレット_\(コンピュータ\).md "wikilink")[モバイルOSの](https://ja.wikipedia.org/wiki/モバイルオペレーティングシステム "wikilink")[BlackBerry Tablet OSおよび](https://ja.wikipedia.org/wiki/BlackBerry_Tablet_OS "wikilink")[BlackBerry 10はQNXベースである](https://ja.wikipedia.org/wiki/BlackBerry_10 "wikilink")。

## 歴史

[1980年](https://ja.wikipedia.org/wiki/1980年 "wikilink")、[ウォータールー大学](../Page/ウォータールー大学.md "wikilink")の学生だったGordon BellとDan Dodgeは一般[計算機科学](../Page/計算機科学.md "wikilink")課程でオペレーティングシステム設計を学び、その中で基本的なリアルタイムカーネルを作成した。彼らは、このようなシステムに需要があると考え、同年 *Quantum Software Systems* 社を設立した。[1982年](../Page/1982年.md "wikilink")、最初のQNXを[8088](../Page/Intel_8088.md "wikilink")[マイクロプロセッサ](../Page/マイクロプロセッサ.md "wikilink")向けにリリースした。

最初にQNXが広く使われたのは組み込みシステムではなく、[オンタリオ州](../Page/オンタリオ州.md "wikilink")の教育システムに採用された [Unisys](../Page/ユニシス.md "wikilink") [ICON](https://ja.wikipedia.org/wiki/:en:Unisys_ICON "wikilink") のOSとしてである。当時としては、44KバイトのOSは組み込みシステムには大きすぎたため、もっと大きなシステムで主に使われたのである。このシステムは信頼性が高いと評判が良く、いくつかの工業アプリケーションに採用されるようになっていった。

[1980年代](../Page/1980年代.md "wikilink")末、Quantum社は市場が[POSIX](../Page/POSIX.md "wikilink")モデルに素早く移行しつつあるのを見て、カーネルの互換性を高めるための書き換えを決定した。そしてリリースされたのが QNX 4 である。このころインターンとして働いていた Patrick Hayden と正社員だった Robin Burgener が新たなコンセプトのウィンドウシステムを開発（）。それを製品に生かして、組み込み可能な[GUIであるPhoton](https://ja.wikipedia.org/wiki/グラフィカルユーザインタフェース "wikilink") microGUIがOSに加えられた。同時に QNX 用の [X Window System](../Page/X_Window_System.md "wikilink") も用意された。QNX 4では[POSIX](../Page/POSIX.md "wikilink")準拠で[UNIX](../Page/UNIX.md "wikilink")や[BSD](../Page/BSD.md "wikilink")用ソフトウェアの移植が容易となった。

Quantum Software Systemsは1990年代初期にQNXソフトウェアシステムズと改称して[ハードディスク企業の](https://ja.wikipedia.org/wiki/ハードディスクドライブ "wikilink")[クアンタムと混同されないようにした](../Page/クアンタム_\(企業\).md "wikilink")。1990年代末 QNX RTOS の全面的な書き換えを行い、[SMP対応し](../Page/対称型マルチプロセッシング.md "wikilink")、マイクロカーネルを維持しつつ既存の [POSIX](../Page/POSIX.md "wikilink") [API](../Page/アプリケーションプログラミングインタフェース.md "wikilink") を全てサポートし、新たな POSIX API にもいち早く対応。その結果、2001年に QNX Neutrino RTOS をリリースすることになった。

Neutrino カーネルと同時にQNXソフトウェアシステムズは開発ツールの充実にも熱心に取り組み、[Eclipseコンソーシアムの創立メンバーにもなった](../Page/Eclipse_\(統合開発環境\).md "wikilink")。2002年、Eclipseワークベンチと関連プラグインをまとめたQNX Momentics Tool Suiteをリリース。

[2004年](../Page/2004年.md "wikilink")末、同社は[ハーマン・インターナショナル](https://ja.wikipedia.org/wiki/ハーマン・インターナショナル "wikilink")に売却されることとなった。QNXは既に自動車業界で[テレマティクス](../Page/テレマティクス.md "wikilink")システム向けに広く使われていた。ハーマンに買収されると、200以上の車種やモデルの[自動車](../Page/自動車.md "wikilink")向けに設計を行い、テレマティクスだけでなく情報娯楽用途やナビゲーション用途でも使われるようになっていった。2011年中ごろ時点で、2000万台の自動車でQNX CAR Application Platformが動作している\[2\]。また、QNX Aviage Multimedia Suite、QNX Aviage Acoustic Processing Suite、QNX HMI Suiteといった[ミドルウェア](../Page/ミドルウェア.md "wikilink")製品もいくつかリリースしてきた。

2007年9月、ソースコードの一部を公開することを発表\[3\]。

2010年4月9日、ハーマン・インターナショナルからリサーチ・イン・モーションへの譲渡に両社が合意したと発表\[4\]。同日、QNXのソースコードへのアクセスが制限されるようになった\[5\]。2010年9月、[タブレットコンピュータ](../Page/タブレット_\(コンピュータ\).md "wikilink") [BlackBerry PlayBook](https://ja.wikipedia.org/wiki/BlackBerry_PlayBook "wikilink") とQNXをベースとするそのOS (BlackBerry Tablet OS) を発表\[6\]。

[シスコシステムズ](../Page/シスコシステムズ.md "wikilink")が2004年から2005年ごろに開発したIOS-XR （[IOSの超高稼動版](../Page/Cisco_IOS.md "wikilink")）\[7\]はQNXベースである\[8\]。また、2006年に登場したIOS Software Modularityも同様である\[9\]。

## 技術

QNXカーネルには、CPU[スケジューリング](../Page/スケジューリング.md "wikilink")、[プロセス間通信](../Page/プロセス間通信.md "wikilink")、[割り込み処理](../Page/割り込み_\(コンピュータ\).md "wikilink")、タイマーだけが含まれる。その他はユーザープロセスとして実装され、例えばプロセス生成、[メモリ管理](../Page/メモリ管理.md "wikilink")を管轄する **proc** という特殊なプロセスはマイクロカーネルと協調して動作する。これを可能にしているのは、[サブルーチン](../Page/サブルーチン.md "wikilink")呼び出し型のプロセス間通信と、[ブート](../Page/ブート.md "wikilink")ローダがカーネルだけでなく複数のユーザープログラムや[共有ライブラリを含めたイメージをロードできる機能があるからである](../Page/ライブラリ.md "wikilink")。カーネル内には[デバイスドライバ](../Page/デバイスドライバ.md "wikilink")が存在しない。通信プロトコルスタックは[NetBSD](../Page/NetBSD.md "wikilink")のコードをベースとしている\[10\]。独自開発のドライバ群、古い *io-net manager* サーバ向けに書かれたドライバ群、NetBSDから移植したドライバ群をサポートしている\[11\]。

QNXのプロセス間通信は、プロセスからプロセスにメッセージを送り、応答を待つ。メッセージはカーネルが送信側の[アドレス空間](../Page/アドレス空間.md "wikilink")から受信側プロセスのアドレス空間にコピーする。受信プロセスがメッセージを待っていた場合、同時に受信側プロセスにCPUの制御が渡され、この際にスケジューラを経由しない。従って、メッセージを送信して返事を待つまで、全く無駄な点がない。このようなメッセージパッシングとCPUスケジューリングの密接な結合が鍵となって、QNXのメッセージパッシングが強力となっているのである。[UNIX](../Page/UNIX.md "wikilink")や[Linux](../Page/Linux.md "wikilink")の多くのプロセス間通信は、このような強力な機能ではない。LinuxにはQNX風のメッセージング機能を実装した例がある\[12\]。この点の設計がまずいことが、初期の[Mach](../Page/Mach.md "wikilink")など多くのマイクロカーネルの性能が期待はずれとなっている原因である。

[マイクロカーネル](https://ja.wikipedia.org/wiki/マイクロカーネル "wikilink")アーキテクチャであるため、QNXは[分散OSでもある](https://ja.wikipedia.org/wiki/分散オペレーティングシステム "wikilink")。Dan Dodge と Peter van der Veen の[特許](http://patft.uspto.gov/netacgi/nph-Parser?Sect1=PTO1&Sect2=HITOFF&d=PALL&p=1&u=%2Fnetahtml%2FPTO%2Fsrchnum.htm&r=1&f=G&l=50&s1=6,697,876.PN.&OS=PN/6,697,876&RS=PN/6,697,876) は QNX の分散処理機能に関するものであり、マーケティング上は[透過分散処理](https://ja.wikipedia.org/wiki/#透過分散処理 "wikilink") (Transpatrent Distributed Processing, TDP) と呼ばれている。

全ての入出力、ファイルシステム操作、ネットワーク操作は、上記の手段を使ってデータのやり取りを行っており、メッセージパッシングの際にコピーされている。性能強化のため、QNXは途中のバージョンから一部プロセスの統合を行い、[プロトコルスタック](../Page/プロトコルスタック.md "wikilink")の統合や他の機能ブロックの統合をしている。

メッセージ処理は[スレッドの優先度に従って優先順位付けされる](../Page/スレッド_\(コンピュータ\).md "wikilink")。入出力もメッセージ処理を使っているため、優先度の高いスレッドが入出力の結果を受け取るのも優先される傾向がある（[リアルタイムシステム](https://ja.wikipedia.org/wiki/リアルタイムシステム "wikilink")なのでそれが基本である）。

ブートローダも重要なシステムの一部である。ユーザープログラムをブートイメージに含めることができ、カーネルの他にデバイスドライバ群や各種ライブラリをブートイメージに含めることが多い。また、ブートイメージを[ROMに格納することでディスクのない組み込みシステムでも利用可能となっている](https://ja.wikipedia.org/wiki/Read_Only_Memory "wikilink")。

Neutrinoは[プロセッサ親和性](https://ja.wikipedia.org/wiki/プロセッサ親和性 "wikilink")を考慮した[対称型マルチプロセッシング](../Page/対称型マルチプロセッシング.md "wikilink")をサポートしており、QNXの用語ではこれを「限定型マルチプロセッシング (BMP, bound multiprocessing)」と呼ぶ。BMPはマルチプロセッサ対応でないアプリケーションを容易にマルチプロセッサのハードウェアに移行でき、キャッシュヒット率も高く維持できる。

Neutrinoは厳密に優先度に基づくプリエンプティブ・スケジューリングを行い、アダプティブ・パーティション・スケジューリング (APS) をサポートしている。APSは、他に多くの高い優先度のパーティション（スレッド群のグループ）があったとしても、全てのパーティションに最小限のCPUを割り当てることを保証する。高負荷であっても[リソーススタベーション](https://ja.wikipedia.org/wiki/リソーススタベーション "wikilink")に陥らず、重要なスレッドが厳密にリアルタイムで動作できるようにしている。

### 透過分散処理

透過分散処理 (TDP, Transparent Distributed Processing) は、QNXのネットワーク分散アーキテクチャの名称である。[マイクロカーネル](https://ja.wikipedia.org/wiki/マイクロカーネル "wikilink")であるため本質的にネットワーク分散が可能であり、TDPとは言ってみればQNXのネットワークスタックに[通信プロトコル](../Page/通信プロトコル.md "wikilink")モジュールをプラグインする仕組みである。qnetと呼ばれるプロトコルモジュールがネットワーク上の複数の[マイクロカーネル](https://ja.wikipedia.org/wiki/マイクロカーネル "wikilink")間をリンクすると、実際にどのノードにあるかを気にせずにOSサービスにアクセスできるようになる\[13\]。

## Foundry27

Foundry27は同社がQNXコミュニティ向けに作ったウェブサイトである。QNX Neutrino開発に関するハブとなっており、開発者が登録でき、ライセンスを選択でき、ソースコードや関連ツールキットを取得できる\[14\]。2010年4月9日にリサーチ・イン・モーションに取得されると、QNXのソースコード全体が自由に入手できるという状態ではなくなった\[15\]。

## 競合OS

組み込み市場での主な競合OSは、

  - POSIXリアルタイムOS
      - [LynxOS](../Page/LynxOS.md "wikilink")
  - 組み込み（にも使われる）Unix系OS
      - Linux
  - その他リアルタイムOS
      - [VxWorks](../Page/VxWorks.md "wikilink"), [THEOS](https://ja.wikipedia.org/wiki/THEOS "wikilink"), [OS-9](../Page/OS-9.md "wikilink"), [SCIOPTA](https://ja.wikipedia.org/wiki/SCIOPTA "wikilink"), [ITRON](../Page/ITRON.md "wikilink")
  - その他組み込みOS
      - [Windows CE](https://ja.wikipedia.org/wiki/Windows_CE "wikilink")

である。

## 競合OSの比較

分散処理、MMUの強化を図る場合、メッセージパッシング方式のリアルタイムOSである必要性がある。するとSCIOPTA, OSEなどが同じコンセプトのアーキテクチャである。

## 脚注

## 参考文献

  -
## 外部リンク

  - [QNX日本語公式サイト](http://www.qnx.co.jp/)
  - [Foundry27](http://community.qnx.com/)
  - [QNX User Community（英語）](http://www.openqnx.com/)
  - [Open source applications（英語）](http://www.sf.net/projects/openqnx)
  - [GUIdebook \> GUIs \> QNX](http://www.aresluna.org/guidebook/guis/qnx)
  - [QNX used for Canadian Nuclear Power Plants](http://www.itbusiness.ca/it/client/en/CDN/News.asp?id=40793)

[Category:Unix系オペレーティングシステム](https://ja.wikipedia.org/wiki/Category:Unix系オペレーティングシステム "wikilink") [Category:リアルタイムオペレーティングシステム](https://ja.wikipedia.org/wiki/Category:リアルタイムオペレーティングシステム "wikilink") [Category:組み込みオペレーティングシステム](https://ja.wikipedia.org/wiki/Category:組み込みオペレーティングシステム "wikilink") [Category:モバイルオペレーティングシステム](https://ja.wikipedia.org/wiki/Category:モバイルオペレーティングシステム "wikilink") [Category:1982年のソフトウェア](https://ja.wikipedia.org/wiki/Category:1982年のソフトウェア "wikilink") [Category:分散オペレーティングシステム](https://ja.wikipedia.org/wiki/Category:分散オペレーティングシステム "wikilink")

1.
2.  [QNX CAR Application Platform](http://www.qnx.com/products/qnxcar/)
3.  QNX Press Releases: [source code availability](http://www.qnx.com/news/pr_2471_1.html)
4.
5.  [wiki4376: UpdatedQNXSourceAccessPolicyFAQ](http://community.qnx.com/sf/wiki/do/viewPage/projects.community/wiki/UpdatedQNXSourceAccessPolicyFAQ)
6.  [RIM Unveils The BlackBerry PlayBook](http://www.marketwire.com/press-release/RIM-Unveils-The-BlackBerry-PlayBook-NASDAQ-RIMM-1325727.htm), official press release, September 27, 2010
7.
8.  [CRS-1 and IOS XR Operational Best Practices](http://www.cisco.com/en/US/products/ps5763/products_tech_note09186a0080772675.shtml#a2)
9.
10. Core Networking 6.4: Neutrino’s Next Gen Networking Stack and Foundry27 [1](http://community.qnx.com/sf/docman/do/downloadDocument/projects.networking/docman.root/doc1280)
11. [Foundry27: Project Networking - Driver wiki page](http://community.qnx.com/sf/wiki/do/viewPage/projects.networking/wiki/Drivers_wiki_page)
12. [SIMPL-Synchronous Interprocess Messaging](http://sourceforge.net/projects/simpl/)
13. [U.S. Patent 5,745,759](http://www.patentstorm.us/patents/5745759-fulltext.html)
14. QNX Press Releases: [Foundry27](http://www.qnx.com/news/pr_2471_2.html)
15. Updated QNX Source Access Policy FAQ: [2](http://community.qnx.com/sf/wiki/do/viewPage/projects.community/wiki/UpdatedQNXSourceAccessPolicyFAQ)
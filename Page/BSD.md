> この記事は[BSD](https://ja.wikipedia.org/wiki/BSD)から翻訳されています。


**BSD**（ビーエスディー、**B**erkeley **S**oftware **D**istribution）とは、1977年から1995年まで[カリフォルニア大学バークレー校](https://ja.wikipedia.org/wiki/カリフォルニア大学バークレー校 "wikilink") (University of California, Berkeley, UCB) の [Computer Systems Research Group](https://ja.wikipedia.org/wiki/Computer_Systems_Research_Group "wikilink") (CSRG) が開発・配布したソフトウェア群、および[UNIX](../Page/UNIX.md "wikilink")[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink") (OS)を言う。なお、今日「BSD」という名称は同OSを元に開発された[BSDの子孫](../Page/BSDの子孫.md "wikilink")の総称として使われることもあるが、この項では主に前述のUCBによるソフトウェア群およびOSについて述べる。

元となったコードベースと設計は[AT\&T](../Page/AT&T.md "wikilink")のUNIXと共通であるため、歴史的にはBSDはUNIXの支流 "BSD UNIX" とみなされてきた。1980年代、[ワークステーション](../Page/ワークステーション.md "wikilink")クラスのシステムベンダーがプロプライエタリなUNIXとしてBSDを広く採用していた。例えば、[DECの](../Page/ディジタル・イクイップメント・コーポレーション.md "wikilink")[Ultrix](https://ja.wikipedia.org/wiki/Ultrix "wikilink")、[サン・マイクロシステムズ](../Page/サン・マイクロシステムズ.md "wikilink")の[SunOS](https://ja.wikipedia.org/wiki/SunOS "wikilink")などである。これは、ライセンス条件の容易だったためと、当時の多くの技術系企業の創業者がBSDを熟知していたためである。

それらプロプライエタリ (proprietary：非公開 ) なBSD派生OSは、1990年代には[UNIX System V Release 4と](https://ja.wikipedia.org/wiki/UNIX_System_V "wikilink")[OSF/1](https://ja.wikipedia.org/wiki/OSF/1 "wikilink")に取って代わられ（どちらもBSDのコードを取り入れており、他の現代のUnixシステムの基盤となった）、後期のBSDリリースはいくつかの[オープンソース](../Page/オープンソース.md "wikilink")開発プロジェクトの基盤となった。例えば、[FreeBSD](../Page/FreeBSD.md "wikilink")、[NetBSD](../Page/NetBSD.md "wikilink")、[OpenBSD](../Page/OpenBSD.md "wikilink")、[DragonFly BSDなどが今も開発中である](https://ja.wikipedia.org/wiki/DragonFly_BSD "wikilink")。さらにそれら（の全部あるいは一部）が最近のプロプライエタリなOSにも採用されている。例えば、[Windowsの](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")[TCP/IPコード](https://ja.wikipedia.org/wiki/インターネット・プロトコル・スイート "wikilink")（IPv4のみ）や[アップルの](../Page/アップル_\(企業\).md "wikilink")[macOS](https://ja.wikipedia.org/wiki/macOS "wikilink")である。

## 歴史

[Unix_history-simple.png](https://ja.wikipedia.org/wiki/File:Unix_history-simple.png "fig:Unix_history-simple.png")

### PDP-11版

[ベル研究所](../Page/ベル研究所.md "wikilink")は1970年代に初期のUnixを[ソースコード](../Page/ソースコード.md "wikilink")も含めて配布し、[大学](../Page/大学.md "wikilink")の研究者らがUnixを修正・拡張できるようにした。バークレーでの最初のUnixシステムは[PDP-11](https://ja.wikipedia.org/wiki/PDP-11 "wikilink")を使ったもので、1974年にインストールされ、[計算機科学](../Page/計算機科学.md "wikilink")科が様々な研究に使用した。

他の大学はバークレーで改良されたソフトウェアに関心を寄せるようになり、当時バークレーの大学院生だった[ビル・ジョイ](https://ja.wikipedia.org/wiki/ビル・ジョイ "wikilink")が1977年、それらを **first Berkeley Software Distribution** (**1BSD**) としてまとめ始め、1978年3月9日にリリースした\[1\]。1BSDは独立した完全なOSというよりも [Sixth Edition Unix](https://ja.wikipedia.org/wiki/Version_6_Unix "wikilink") へのアドオンであり、その主なコンポーネントは[Pascal](../Page/Pascal.md "wikilink")[コンパイラ](../Page/コンパイラ.md "wikilink")とジョイが開発した[ラインエディタ](https://ja.wikipedia.org/wiki/ラインエディタ "wikilink")  だった。

1979年5月にリリースとなった **Second Berkeley Software Distribution** (**2BSD**)\[2\]は、1BSDのソフトウェアの更新版だけでなくジョイが新たに開発した [vi](https://ja.wikipedia.org/wiki/vi "wikilink") エディタ（exの[スクリーンエディタ版](../Page/テキストエディタ.md "wikilink")）と [C Shell](https://ja.wikipedia.org/wiki/C_Shell "wikilink") も含まれていた。

2BSDの後のリリースでは、PDP-11アーキテクチャから[VAX](https://ja.wikipedia.org/wiki/VAX "wikilink")ベースへとプラットフォームが変化している。1983年の2.9BSDには4.1cBSDからのコードを含んでおり、それまでアプリケーションとパッチの集まりだったものが初めて完全なOS（[Version 7 Unix](https://ja.wikipedia.org/wiki/Version_7_Unix "wikilink") の修正版）のリリースとなった。2BSDの最終版は1992年にリリースされた **2.11BSD** である。2008年現在、2BSD用のパッチ447が2008年12月31日にリリースされており、ボランティアによる保守が続いている\[3\]。

### VAX版

1978年、Unixを[VAX](https://ja.wikipedia.org/wiki/VAX "wikilink")アーキテクチャに[移植した](https://ja.wikipedia.org/wiki/移植_\(ソフトウェア\) "wikilink") [UNIX/32V](https://ja.wikipedia.org/wiki/UNIX/32V "wikilink") がバークレーのVAXにインストールされたが、これはVAXの[仮想記憶](../Page/仮想記憶.md "wikilink")機能を生かしたものではなかった。32Vの[カーネル](../Page/カーネル.md "wikilink")をバークレーの学生達が大幅に書きかえて仮想記憶を実装し、2BSDのユーティリティ群をVAXに移植したものと32V由来のユーティリティ群をまとめて完全なOSとしたものが **3BSD** として1979年末にリリースされた。3BSDは、Virtual VAX/UNIX または VMUNIX (Virtual Memory Unix) とも呼ばれ、BSDのカーネルイメージは4.4BSDまで `/vmunix` と呼ばれるようになった。

3BSDに注目した[国防高等研究計画局](../Page/国防高等研究計画局.md "wikilink") (DARPA) は、バークレーの [Computer Systems Research Group](https://ja.wikipedia.org/wiki/Computer_Systems_Research_Group "wikilink") (CSRG) に資金提供することを決め、CSRGにDARPAの研究プロジェクトである [VLSI Project](https://ja.wikipedia.org/wiki/:en:VLSI_Project "wikilink") のための標準Unixプラットフォームを開発させることにした。1980年、CSRGは3BSDに様々な改良を加えた **4BSD** をリリースした。

**4BSD**（1980年11月）が3BSDに加えた改良としては、既にリリース済みだった[cshでの](https://ja.wikipedia.org/wiki/C_Shell "wikilink")、[delivermail](https://ja.wikipedia.org/wiki/:en:delivermail "wikilink")（[sendmail](https://ja.wikipedia.org/wiki/sendmail "wikilink")の前身）、高信頼の[シグナル](https://ja.wikipedia.org/wiki/シグナル_\(Unix\) "wikilink")、[curses](https://ja.wikipedia.org/wiki/curses "wikilink")ライブラリなどがある。

**4.1BSD**（1981年6月）は、VAXの主要OSである[VMSに比べてBSDの性能が悪いという批判に応えたものだった](https://ja.wikipedia.org/wiki/OpenVMS "wikilink")。[ビル・ジョイ](https://ja.wikipedia.org/wiki/ビル・ジョイ "wikilink")は4.1BSDカーネルがVMSといくつかの[ベンチマーク](https://ja.wikipedia.org/wiki/ベンチマーク "wikilink")で互角になるまで体系的に性能強化を施した。当初 5BSD と呼ぶ予定だったが、[AT\&T](../Page/AT&T.md "wikilink")が [UNIX System V](https://ja.wikipedia.org/wiki/UNIX_System_V "wikilink") との混同を恐れて異議を唱えたため、4.1BSD となった\[4\]。

**4.2BSD**はいくつかの大きな改修を行い、リリースまで2年以上かかった。4.2BSDがリリースされるまでに中間バージョンが3度リリースされている。*4.1a* は[BBNの予備的な](https://ja.wikipedia.org/wiki/BBNテクノロジーズ "wikilink")[TCP/IP実装を導入している](https://ja.wikipedia.org/wiki/インターネット・プロトコル・スイート "wikilink")。*4.1b* は[マーシャル・カーク・マキュージック](https://ja.wikipedia.org/wiki/マーシャル・カーク・マキュージック "wikilink")が実装した [Berkeley Fast File System](https://ja.wikipedia.org/wiki/Unix_File_System "wikilink") を導入した。*4.1c* は4.2BSDの数カ月前にリリースされた中間バージョンである。

4.2BSDの設計方針を決定するため、[DARPA](../Page/国防高等研究計画局.md "wikilink") は運営委員会を立ち上げた。委員には[UCBからボブ](https://ja.wikipedia.org/wiki/カリフォルニア大学バークレー校 "wikilink")・ファブリー、[ビル・ジョイ](https://ja.wikipedia.org/wiki/ビル・ジョイ "wikilink")、サム・レフラー、BBNからアラン・ネメス、ロブ・ガーウィッツ、[ベル研究所](../Page/ベル研究所.md "wikilink")から[デニス・リッチー](../Page/デニス・リッチー.md "wikilink")、[スタンフォード大学](../Page/スタンフォード大学.md "wikilink")からキース・ランツ、[カーネギーメロン大学](https://ja.wikipedia.org/wiki/カーネギーメロン大学 "wikilink")から[リチャード・ラシッド](https://ja.wikipedia.org/wiki/リチャード・ラシッド "wikilink")、[MITからバート](../Page/マサチューセッツ工科大学.md "wikilink")・ハルステッド、[ISIからダン](https://ja.wikipedia.org/wiki/情報科学研究所 "wikilink")・リンチ、[UCLAから](../Page/カリフォルニア大学ロサンゼルス校.md "wikilink")[ジェラルド・J・ポペック](https://ja.wikipedia.org/wiki/ジェラルド・J・ポペック "wikilink")が参加した。この委員会は1981年4月から1983年6月まで会合を開いていた。

4.2BSDは1983年8月に正式リリースされた。実は、リリース前の1982年にはビル・ジョイが大学を離れて[サン・マイクロシステムズ](../Page/サン・マイクロシステムズ.md "wikilink")を共同創業している。その後はマイク・カレルズと[マーシャル・カーク・マキュージック](https://ja.wikipedia.org/wiki/マーシャル・カーク・マキュージック "wikilink")がプロジェクトリーダー的役割を果たした。また、4.2BSDのリリースと同時に[ジョン・ラセター](https://ja.wikipedia.org/wiki/ジョン・ラセター "wikilink")の描いた[BSDデーモン](https://ja.wikipedia.org/wiki/BSDデーモン "wikilink")というマスコットもデビューした。最初の登場は[USENIX](https://ja.wikipedia.org/wiki/USENIX "wikilink")で配布されたマニュアルの表紙である。

### 4.3BSD

**4.3BSD** は1986年6月にリリースされた。主な改良点は性能であり、4.2BSDは4.1BSDほど性能をチューニングできていなかった。そのリリース前に、BSDでのTCP/IPの実装はBBNの公式実装から大幅に変更されていた。DARPAは数カ月かけてそれを試験し、BBN版より4.2BSD版が優れていると結論付け、それがそのまま4.3BSDで採用された。

4.3BSDリリース後、BSDのプラットフォームを古くなったVAXから新たなプラットフォームへ移行することが決まった。当初 [Computer Consoles Inc.](https://ja.wikipedia.org/wiki/:en:Computer_Consoles_Inc. "wikilink") の68kベースの Power 6/32（コード名 "Tahoe"）が候補となったが、間もなく開発者らがそれをやめた。それでも **4.3BSD-Tahoe** という移植版（1988年6月）は貴重であり、BSDにおける機種依存コードと機種共通コードの分離をもたらし、将来の移植性向上に寄与した。

移植性以外にも、CSRGは[OSIネットワークプロトコルスタックの実装](https://ja.wikipedia.org/wiki/開放型システム間相互接続 "wikilink")、カーネルの仮想記憶システムの改良、インターネットの成長に対応した（[LBLの](https://ja.wikipedia.org/wiki/ローレンス・バークレー国立研究所 "wikilink")[バン・ジェイコブソン](https://ja.wikipedia.org/wiki/バン・ジェイコブソン "wikilink")による）TCP/IPアルゴリズムの改良といった改良も行っている\[5\]。

それまでBSDの全バージョンでAT\&TのプロプライエタリなUnixのコードが含まれており、AT\&Tのソフトウェアライセンスを必要としていた。ソースコードライセンスは非常に高価で、第三者からはAT\&Tとは無関係に開発されたネットワーク関連コードだけをリリースして欲しいと要望されることもあった。そこで生まれたのが **Networking Release 1** (**Net/1**) で、AT\&Tのライセンスが不要なコードのみで構成されており、[BSDライセンス](https://ja.wikipedia.org/wiki/BSDライセンス "wikilink")で[フリーソフトウェア](../Page/フリーソフトウェア.md "wikilink")として自由に再配布可能とされた。これが1989年6月にリリースされている。

**4.3BSD-Reno**は1990年初めにリリースされた。4.4BSDとして開発中のバージョンの中間リリース的性格のリリースであり、その使用は一種の[ギャンブルだという意味でギャンブルの街](../Page/賭博.md "wikilink")[リノの名を冠している](https://ja.wikipedia.org/wiki/リノ_\(ネバダ州\) "wikilink")。このリリースは明確に[POSIX](https://ja.wikipedia.org/wiki/POSIX "wikilink")準拠を目指しており\[6\]、ある面ではBSDの精神からかけ離れているとされることもある（というのも、POSIXは System V ベースとなっている部分が多く、Reno はそれまでのリリースに比べるとかなり肥大化している）。が移植した[NFSも新機能として含まれていた](https://ja.wikipedia.org/wiki/Network_File_System "wikilink")。

2006年8月、*Information Week* 誌は4.3BSDを「これまでに書かれた最も偉大なソフトウェア」と評した\[7\]。コメントには「BSD 4.3 はインターネットの単独で最大の理論的下支えを代表している」とある。

### Net/2 と訴訟問題

Net/1リリース後、BSD開発者は、BSDのAT\&Tとは無関係な部分をさらにNet/1と同じライセンスでリリースしようと提案した。そして彼はUnixの標準ユーティリティをAT\&Tのコードを使わずに再実装するプロジェクトを開始。例えば、[vi](https://ja.wikipedia.org/wiki/vi "wikilink")はAT\&T由来の [ed](https://ja.wikipedia.org/wiki/ed "wikilink") をベースにしていたので、全く新たに [nvi](https://ja.wikipedia.org/wiki/nvi "wikilink") (new vi) を書いた。18カ月でAT\&T由来のユーティリティを全て再実装して置換し、カーネルにもAT\&T由来のファイルは数えるほどしかない状態となった。それらのファイルを削除し、1991年6月、自由に再配布可能なほぼ完全なOSである **Networking Release 2 (Net/2)** をリリースした。

Net/2 は [Intel 80386](../Page/Intel_80386.md "wikilink") アーキテクチャへの2つの独立したBSD移植プロジェクトの基盤となった。1つは[ウィリアム・ジョリッツ](https://ja.wikipedia.org/wiki/ウィリアム・ジョリッツ "wikilink")らによるフリーな[386BSD](../Page/386BSD.md "wikilink")で、もう1つは  (BSDi) の[プロプライエタリな](https://ja.wikipedia.org/wiki/プロプライエタリ・ソフトウェア "wikilink")[BSD/386](https://ja.wikipedia.org/wiki/BSD/OS "wikilink")（後にBSD/OSに改称）である。386BSD自体は短命に終わったが、間もなくそれをベースとして[NetBSD](../Page/NetBSD.md "wikilink")と[FreeBSD](../Page/FreeBSD.md "wikilink")のプロジェクトが始まった。

BSDiは System V の[著作権](../Page/著作権.md "wikilink")と UNIX の[商標](../Page/商標.md "wikilink")を所有する AT\&T の [UNIX Systems Laboratories](https://ja.wikipedia.org/wiki/UNIX_Systems_Laboratories "wikilink") (USL) との間で訴訟に見舞われることになった。USLとBSDiの訴訟 ([en](https://ja.wikipedia.org/wiki/:en:USL_v._BSDi "wikilink")) は1992年に始まり、この訴訟が解決するまで、Net/2の配布は[差し止められることになった](https://ja.wikipedia.org/wiki/差止命令 "wikilink")。

この訴訟問題で約2年間、BSD系のPC-Unix開発にはブレーキがかかり、[Linux](https://ja.wikipedia.org/wiki/Linux "wikilink")の急激な支持の原因を作った。リリースされたのは1992年だが、[386BSD](../Page/386BSD.md "wikilink")はLinuxより前から開発されていた。[リーナス・トーバルズ](../Page/リーナス・トーバルズ.md "wikilink")は、386BSDか [GNU Hurd](../Page/GNU_Hurd.md "wikilink") が当時利用可能だったら、自分でLinuxカーネルをつくろうとはしなかっただろうと述べている\[8\]\[9\]。

### 4.4BSD と派生

訴訟の過程ではAT\&T由来のコードがNet/2にまだ含まれていることが明らかとなったが、同時にAT\&Tが販売している[UNIX System VにもBSD由来のコードがライセンスに違反して使用されていたことから](https://ja.wikipedia.org/wiki/UNIX_System_V "wikilink")、[ノベルがUSLを買い取った後の](../Page/ノベル_\(企業\).md "wikilink")1994年に関係者は和解。1994年1月、訴訟は主としてバークレー側に有利な形で決着した。バークレーの配布物である18,000個のファイルのうち、3個のファイルの削除が命じられ、70個のファイルにUSLの著作権表示を加えることが命じられた。さらに和解条件として、近々リリースされる4.4BSDでのバークレーの所有するコードのユーザーやディストリビュータに対してUSLが訴訟を起こさないと約束している。

1994年6月、**4.4BSD**は2つの形でリリースされた。AT\&Tのライセンスに抵触しない **4.4BSD-Lite** と従来通りのライセンスを要する **4.4BSD-Encumbered** である。

バークレーからの最後のリリースは1995年の **4.4BSD-Lite Release 2** で、その後 CSRG は解散となり、バークレーでのBSD開発は終了した。それ以降、4.4BSD-Lite を直接あるいは間接的にベースとしている派生OS（[FreeBSD](../Page/FreeBSD.md "wikilink")、[NetBSD](../Page/NetBSD.md "wikilink")、[OpenBSD](../Page/OpenBSD.md "wikilink")、[DragonFly BSD](https://ja.wikipedia.org/wiki/DragonFly_BSD "wikilink") など）が開発・保守されている。

さらに、[BSDライセンス](https://ja.wikipedia.org/wiki/BSDライセンス "wikilink")の[許容型の性質により](https://ja.wikipedia.org/wiki/フリーソフトウェアライセンス#許容型とコピーレフト型 "wikilink")、フリーなものもプロプライエタリなものも含めて様々なOSでBSDのコードが利用されている。例えば、[WindowsはBSD由来のコードをTCP](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")/IP実装に使用し、BSDの[コマンドラインのネットワークツールをリコンパイルしたものを](../Page/キャラクタユーザインタフェース.md "wikilink") Windows 2000で導入した\[10\]。アップルの[macOS](https://ja.wikipedia.org/wiki/macOS "wikilink")の基盤となった[Darwinも](../Page/Darwin_\(オペレーティングシステム\).md "wikilink")4.4BSD-Lite2とFreeBSDから派生したものである。[Solaris](../Page/Solaris.md "wikilink")などの商用UNIXもBSDコードを含んでいる。

## 技術

BSDはUNIXとして初めて [TCP/IPスタック](https://ja.wikipedia.org/wiki/インターネット・プロトコル・スイート "wikilink")（Berkeley[ソケット](https://ja.wikipedia.org/wiki/ソケット_\(BSD\) "wikilink")）を搭載した。ソケットをUnixの[ファイル記述子](https://ja.wikipedia.org/wiki/ファイル記述子 "wikilink")と統合したことで、[ネットワーク経由のデータの読み書きをディスクアクセスのように容易に行えるようになった](https://ja.wikipedia.org/wiki/コンピュータネットワーク "wikilink")。それに対してAT\&Tは [STREAMS](https://ja.wikipedia.org/wiki/STREAMS "wikilink") をリリース。機能的には同等でアーキテクチャはSTREAMSの方が優れていたが、ソケットの方が先に普及しており、意図的に使用する[システムコール](https://ja.wikipedia.org/wiki/システムコール "wikilink")を別の名前にしたためBSD系ではそれらシステムコールがサポートされず、結果的に[APIとして普及しなかった](../Page/アプリケーションプログラミングインタフェース.md "wikilink")。Berkeleyソケットを[Turbo Pascalで書き直したものがのちに](../Page/Turbo_Pascal.md "wikilink")[Windows 95に取り込まれ](../Page/Microsoft_Windows_95.md "wikilink")、現在の[Winsock](https://ja.wikipedia.org/wiki/Winsock "wikilink")2の元となった。

今でもBSDは大学などで技術的叩き台として使われている。商用製品やフリーな製品でもよく使われており、[組み込みシステム](../Page/組み込みシステム.md "wikilink")での採用もある。ソースコードの品質が一般に高く、文書（特に[manページ](https://ja.wikipedia.org/wiki/manページ "wikilink")と言われるオンラインマニュアル）も揃っているため、様々な用途に利用可能である。

BSD系OSは、バイナリ[互換レイヤー](https://ja.wikipedia.org/wiki/互換レイヤー "wikilink")を使って同一[アーキテクチャの異なるOSのソフトウェアを動作させることができる](../Page/コンピュータ・アーキテクチャ.md "wikilink")。これは[エミュレータ](https://ja.wikipedia.org/wiki/エミュレータ "wikilink")よりも高速で単純であり、例えば[Linux](https://ja.wikipedia.org/wiki/Linux "wikilink")向けのアプリケーションをほぼ性能低下なく動作させることができる。

最近のBSD系OSは[IEEE](../Page/IEEE.md "wikilink")、[ANSI](../Page/米国国家規格協会.md "wikilink")、[ISO](https://ja.wikipedia.org/wiki/国際標準化機構 "wikilink")、[POSIX](https://ja.wikipedia.org/wiki/POSIX "wikilink")などの標準に準拠しつつ、BSDの伝統的振る舞いを維持している。AT\&Tのもともとの[UNIX](../Page/UNIX.md "wikilink")と同様[モノリシックカーネル](../Page/モノリシックカーネル.md "wikilink")であり、[デバイスドライバ](../Page/デバイスドライバ.md "wikilink")は[特権モードでカーネルと共に動作する](https://ja.wikipedia.org/wiki/リングプロテクション "wikilink")。

## BSDの主な子孫

[right](https://ja.wikipedia.org/wiki/ファイル:Bsd_distributions_usage.svg "wikilink")（2005年）\[11\]。複数回答がありうるので、合計は100%を超えている。\]\]  BSDは様々なオペレーティングシステムの基盤となった。最もよく知られているのは[オープンソース](../Page/オープンソース.md "wikilink")の FreeBSD、NetBSD、OpenBSD であり、それらはいずれも[386BSD](../Page/386BSD.md "wikilink")と 4.4BSD-Lite を起源としている。NetBSDとFreeBSDは1993年にプロジェクトを開始しており、当初は386BSDをベースとしていたが、1994年に 4.4BSD-Lite のコードベースに移行した。OpenBSDは1995年にNetBSDから[フォークした](https://ja.wikipedia.org/wiki/フォーク_\(ソフトウェア開発\) "wikilink")。この3つのBSDの子孫からさらに様々な子孫が分岐しており、[DragonFly BSD](https://ja.wikipedia.org/wiki/DragonFly_BSD "wikilink")、[FreeSBIE](https://ja.wikipedia.org/wiki/FreeSBIE "wikilink")、、[DesktopBSD](https://ja.wikipedia.org/wiki/DesktopBSD "wikilink")、[TrueOS](https://ja.wikipedia.org/wiki/TrueOS "wikilink")などがある。これらはそれぞれターゲットとするシステムが異なり、政府機関、大学、企業などで普通に使われている。BSDまたはその子孫を起源とする商用OSもいくつかあり、[サンの](../Page/サン・マイクロシステムズ.md "wikilink")[SunOS](https://ja.wikipedia.org/wiki/SunOS "wikilink")、[アップルの](../Page/アップル_\(企業\).md "wikilink")[macOS](https://ja.wikipedia.org/wiki/macOS "wikilink")などが挙げられる。

最近のBSD系OSの多くはmacOSを除けば[オープンソース](../Page/オープンソース.md "wikilink")であり、[BSDライセンス](https://ja.wikipedia.org/wiki/BSDライセンス "wikilink")で利用できる。macOSとDragonfly BSDはモノリシックとマイクロカーネルの中間である[ハイブリッドカーネル](https://ja.wikipedia.org/wiki/ハイブリッドカーネル "wikilink")だが、多くのBSD系OSは[モノリシックカーネル](../Page/モノリシックカーネル.md "wikilink")である。オープンソースのBSDプロジェクトでは、カーネルと[ユーザーランドのプログラムやライブラリを一緒に開発していることが多く](../Page/オペレーティングシステム.md "wikilink")、ソースのリポジトリはそれらを共通して管理している。

BSDはかつてプロプライエタリなUNIXの基盤としても使われていた。例えば、[サンの](../Page/サン・マイクロシステムズ.md "wikilink")[SunOS](https://ja.wikipedia.org/wiki/SunOS "wikilink")、[シークエントの](https://ja.wikipedia.org/wiki/シークエント・コンピュータ "wikilink") Dynix、[NeXT](../Page/NeXT.md "wikilink")の[NeXTSTEP](https://ja.wikipedia.org/wiki/NEXTSTEP "wikilink")、[DECの](../Page/ディジタル・イクイップメント・コーポレーション.md "wikilink")[Ultrix](https://ja.wikipedia.org/wiki/Ultrix "wikilink")と OSF/1 AXP（後の [Tru64 UNIX](https://ja.wikipedia.org/wiki/Tru64_UNIX "wikilink")）がある。例に挙げたうち、今も本来の形態でサポートされているのは最後の1つ (Tru64 UNIX) だけである。NeXT のソフトウェアの一部はmacOSの基盤の一部となった。商業的に最も成功したBSDの子孫はmacOSといえる。

以下にBSDの子孫である[Unix系](https://ja.wikipedia.org/wiki/Unix系 "wikilink")OSの例を挙げる。

  - [FreeBSD](../Page/FreeBSD.md "wikilink") - 性能向上を主目的とした主要なオープンソース版。[x86](https://ja.wikipedia.org/wiki/x86 "wikilink")プラットフォームが主体。
      - [DragonFly BSD](https://ja.wikipedia.org/wiki/DragonFly_BSD "wikilink") - FreeBSDからのフォーク。設計方針が異なり、[SMP対応などに強い](https://ja.wikipedia.org/wiki/対称型マルチプロセッシング "wikilink")。
      - [TrueOS](https://ja.wikipedia.org/wiki/TrueOS "wikilink") と [DesktopBSD](https://ja.wikipedia.org/wiki/DesktopBSD "wikilink") - デスクトップやノート型PC向けにインタフェースと使いやすさを強化した[FreeBSDディストリビューション](https://ja.wikipedia.org/wiki/FreeBSDディストリビューション "wikilink")。
      - [FreeNAS](https://ja.wikipedia.org/wiki/FreeNAS "wikilink") - [NASサーバ構築向けの](../Page/ネットワークアタッチトストレージ.md "wikilink")[FreeBSDディストリビューション](https://ja.wikipedia.org/wiki/FreeBSDディストリビューション "wikilink")。
      - [Nokia IPSO](https://ja.wikipedia.org/wiki/:en:Nokia_IPSO "wikilink") (IPSO SB) - FreeBSDベースのOSで、[ノキア](https://ja.wikipedia.org/wiki/ノキア "wikilink")のファイアウォール機器で使用。
      - JunOS - [ジュニパーネットワークス](https://ja.wikipedia.org/wiki/ジュニパーネットワークス "wikilink")のルーター用OSで、FreeBSDベース。
      - ONTAP GX - [ネットアップ](https://ja.wikipedia.org/wiki/ネットアップ "wikilink")のストレージ製品のOSで、FreeBSDベース。
      - [F5ネットワークス](https://ja.wikipedia.org/wiki/F5ネットワークス "wikilink")の F5 BIGIP アプライアンスもFreeBSDベースのOSを採用していたが、バージョン9.0から[Linux](https://ja.wikipedia.org/wiki/Linux "wikilink")ベースに移行した。
  - [NEXTSTEP](https://ja.wikipedia.org/wiki/NEXTSTEP "wikilink")と[OPENSTEP](https://ja.wikipedia.org/wiki/OPENSTEP "wikilink") - [NeXT](../Page/NeXT.md "wikilink")の開発したOS。Machカーネルと4BSDをベースにしている。後の[macOS](https://ja.wikipedia.org/wiki/macOS "wikilink")の元となった。
      - [Darwin](../Page/Darwin_\(オペレーティングシステム\).md "wikilink")、[macOS](https://ja.wikipedia.org/wiki/macOS "wikilink")、[iOS](https://ja.wikipedia.org/wiki/iOS_\(アップル\) "wikilink") - [アップルのOS](../Page/アップル_\(企業\).md "wikilink")。[XNU](https://ja.wikipedia.org/wiki/XNU "wikilink")カーネル（[Mach](../Page/Mach.md "wikilink")、FreeBSD、アップル独自コードがベース）を中核とし、ユーザーランドの大部分はFreeBSDベースである。
  - [NetBSD](../Page/NetBSD.md "wikilink") - 移植性とクリーン設計を指向したオープンソース版。
      - [アラクサラネットワークス](https://ja.wikipedia.org/wiki/アラクサラネットワークス "wikilink")はNetBSDベースのOSをスイッチで使用。
      - [OpenBSD](../Page/OpenBSD.md "wikilink") - NetBSDから1995年に[フォーク](https://ja.wikipedia.org/wiki/フォーク_\(ソフトウェア開発\) "wikilink")。移植性、標準化、正しい思想、先制的なセキュリティ、暗号化機能の統合といった目標を設定している。
  - [Ultrix](https://ja.wikipedia.org/wiki/Ultrix "wikilink") - DECが [PDP-11](https://ja.wikipedia.org/wiki/PDP-11 "wikilink")、VAX、[DECstation](https://ja.wikipedia.org/wiki/DECstation "wikilink") というシステム向けにリリースした公式版Unix。
  - [OSF/1](https://ja.wikipedia.org/wiki/OSF/1 "wikilink") - [Mach](../Page/Mach.md "wikilink")カーネルと4BSDをベースとして [Open Software Foundation](https://ja.wikipedia.org/wiki/Open_Software_Foundation "wikilink") が開発した[マイクロカーネル](https://ja.wikipedia.org/wiki/マイクロカーネル "wikilink")ベースのUNIX。
      - [Tru64 UNIX](https://ja.wikipedia.org/wiki/Tru64_UNIX "wikilink")（以前は DEC OSF/1 AXP あるいは Digital UNIX） - [OSF/1](https://ja.wikipedia.org/wiki/OSF/1 "wikilink") を [DEC Alpha](https://ja.wikipedia.org/wiki/DEC_Alpha "wikilink") ベースのシステムに移植したもの。[DEC](../Page/ディジタル・イクイップメント・コーポレーション.md "wikilink")、[コンパック](https://ja.wikipedia.org/wiki/コンパック "wikilink")、[HP](../Page/ヒューレット・パッカード.md "wikilink") のシステムで動作。
  - [SunOS](https://ja.wikipedia.org/wiki/SunOS "wikilink") の初期のバージョン（SunOS 4.1.4 まで） - [サン・マイクロシステムズ](../Page/サン・マイクロシステムズ.md "wikilink")による4BSDの強化版。[モトローラ](../Page/モトローラ.md "wikilink")の[68kベースの](../Page/MC68000.md "wikilink") [Sun-2](https://ja.wikipedia.org/wiki/Sun-2 "wikilink")/[Sun-3](https://ja.wikipedia.org/wiki/Sun-3 "wikilink")システム、[SPARC](https://ja.wikipedia.org/wiki/SPARC "wikilink")ベースのシステム、[x86](https://ja.wikipedia.org/wiki/x86 "wikilink")ベースの [Sun386i](https://ja.wikipedia.org/wiki/Sun386i "wikilink")システムなどで動作。
  - [386BSD](../Page/386BSD.md "wikilink") - 最初のオープンソース版BSDであり、その後の多くのBSDシステムの源流となった。
  - [DEMOS](https://ja.wikipedia.org/wiki/:en:DEMOS "wikilink") - [ソビエト連邦](https://ja.wikipedia.org/wiki/ソビエト連邦 "wikilink")製BSDクローン。
  - [BSD/OS](https://ja.wikipedia.org/wiki/BSD/OS "wikilink") - かつて存在したPC向けのプロプライエタリなBSD。

## 脚注

## 参考文献

  -   - （邦訳）

  -
  -
  -
  - Chris DiBona, Mark Stone, Sam Ockman, Open Source (Organization), Brian Behlendorf and J. Scott Bradner, *Open Sources: Voices from the Open Source Revolution*. [O'Reilly & Associates](https://www.oreilly.com/), 1999. Trade paperback, 272 pages. ISBN 978-1-56592-582-3. Online [version](https://www.oreilly.com/openbook/opensources/book/); [Marshall Kirk McKusick](https://ja.wikipedia.org/wiki/マーシャル・カーク・マキュージック "wikilink"), chapter on BSD, [*"Twenty Years of Berkeley Unix - From AT\&T-Owned to Freely Redistributable"*](https://www.oreilly.com/openbook/opensources/book/kirkmck.html)

  - Peter H. Salus, *The Daemon, the GNU & The Penguin* (Reed Media Services, September 1, 2008; ISBN 978-0-9790342-3-7)

  - Peter H. Salus, *Casting the Net* (Addison-Wesley, March 1995; ISBN 978-0-201-87674-1)

## 関連項目

  - [BSDデーモン](https://ja.wikipedia.org/wiki/BSDデーモン "wikilink")
  - [BSDライセンス](https://ja.wikipedia.org/wiki/BSDライセンス "wikilink")
  - [BSDの子孫](../Page/BSDの子孫.md "wikilink")（BSD系UNIX）
  - [OpenDarwin](https://ja.wikipedia.org/wiki/OpenDarwin "wikilink")
  - [ローグ](https://ja.wikipedia.org/wiki/ローグ "wikilink")
  - [Charlie Root (オペレーティングシステム)](https://ja.wikipedia.org/wiki/Charlie_Root_\(オペレーティングシステム\) "wikilink")
  - [Mach](../Page/Mach.md "wikilink")
  - [Σプロジェクト](https://ja.wikipedia.org/wiki/Σプロジェクト "wikilink")

## 外部リンク

  - [A timeline of BSD and Research UNIX](https://svnweb.freebsd.org/base/head/share/misc/bsd-family-tree)
  - [UNIX History](https://www.levenez.com/unix/)
  - [The Design and Implementation of the 4.4BSD Operating System](https://www.freebsd.org/doc/en_US.ISO8859-1/books/design-44bsd/)

[Category:BSD](https://ja.wikipedia.org/wiki/Category:BSD "wikilink") [Category:Unix系オペレーティングシステム](https://ja.wikipedia.org/wiki/Category:Unix系オペレーティングシステム "wikilink") [Category:フリーソフトウェアOS](https://ja.wikipedia.org/wiki/Category:フリーソフトウェアOS "wikilink") [Category:1977年のソフトウェア](https://ja.wikipedia.org/wiki/Category:1977年のソフトウェア "wikilink") [Category:OSファミリ](https://ja.wikipedia.org/wiki/Category:OSファミリ "wikilink")

1.  Peter H. Salus, *A Quarter Century of UNIX* (Addison Wesley, June 1, 1994; ISBN 978-0-201-54777-1), p. 142
2.
3.
4.  M.K. McKusick in [*Open Sources*](http://oreilly.com/catalog/opensources/book/kirkmck.html), O'Reilly.
5.  M.K. McKusick, M.J. Karels, Keith Sklower, Kevin Fall, Marc Teitelbaum and Keith Bostic (1989). Current Research by The Computer Systems Research Group of Berkeley. Proc. European Unix Users Group.
6.
7.
8.
9.
10.
11.
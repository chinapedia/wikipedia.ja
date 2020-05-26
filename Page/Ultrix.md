> この記事は[Ultrix](https://ja.wikipedia.org/wiki/Ultrix)から翻訳されています。


**Ultrix**（正式には **ULTRIX**）は、[ディジタル・イクイップメント・コーポレーション](../Page/ディジタル・イクイップメント・コーポレーション.md "wikilink") (DEC) が開発した[UNIX](../Page/UNIX.md "wikilink")のブランド名。*ultrix* は[ラテン語](../Page/ラテン語.md "wikilink")で「復讐者」という意味であり、この名称は単に音だけで選ばれた。

## 歴史

UNIXの初期の開発はDECの製品（DEC [PDP-7](../Page/PDP-7.md "wikilink") と [PDP-11](../Page/PDP-11.md "wikilink")システム）上で行われた。その後の[VAX](../Page/VAX.md "wikilink")システムなどのDEC製コンピュータもUNIXを動作させるプラットフォームとしては一般的であった。[VAX](../Page/VAX.md "wikilink")への最初の移植は[UNIX/32V](https://ja.wikipedia.org/wiki/UNIX/32V "wikilink")であり、[1978年](https://ja.wikipedia.org/wiki/1978年 "wikilink")に完成した（VAX自体のリリースは[1977年](../Page/1977年.md "wikilink")[10月](https://ja.wikipedia.org/wiki/10月 "wikilink")である）。しかし、DEC自身は独自の[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink")[VMSを提供しており](../Page/OpenVMS.md "wikilink")、UNIXを認めるには時間がかかったのである。

社内にUNIXを持ち込むきっかけとして、Bill MunsonはDEC内にUnix Engineering Group (UEG) を立ち上げた。当初のメンバーには、DECの顧客サービス技術部門のJerry BrennerとFred Canter、[ケース・ウェスタン・リザーブ大学](../Page/ケース・ウェスタン・リザーブ大学.md "wikilink")のBill Shannon、[ベル研究所](../Page/ベル研究所.md "wikilink")のArmando Stettnerらがいる。その後のメンバーとしては、Joel Magid、Bill Doll、Jim Barclay らがDEC内の様々なマーケティング部門や製品管理部門から集められた。

Canterの指揮の下、UEGチームは**V7M**をリリースした。[Version 7 Unixの修正版である](../Page/Version_7_Unix.md "wikilink")。

### BSD

ShannonとStettnerはUNIX/32Vの[CPU](../Page/CPU.md "wikilink")周りやドライバサポートに当初取り組んだが、間もなく[カリフォルニア大学バークレー校](../Page/カリフォルニア大学バークレー校.md "wikilink")の[4BSD開発グループと共に働くことに集中するようになった](../Page/BSD.md "wikilink")。バークレーの[ビル・ジョイ](../Page/ビル・ジョイ.md "wikilink")は[ニューハンプシャー州](../Page/ニューハンプシャー州.md "wikilink")に乗り込んで Shannon や Stettner と合流し、UEGによるCPU周りとドライバを含めてBSDリリースをまとめ、最終的な開発とテストをDECの様々なシステム構成で行った。また、3人はVMS開発グループの使用しているメインのVAXでの最終評価も行った。翌朝、端末にUNIXのプロンプトが表示されてもVMS開発者からは何のコメントもなかったという。UEGのマシンで最初の新しいUNIXが動作し、4.5BSDとラベルを貼ったテープをビル・ジョイが持っていった。次のバージョンは5BSDになると考えられていたが、大学の弁護士は4.1BSDという名称にすることを勧めた。4.1BSDが完成すると、ビル・ジョイはバークレーを辞めて[サン・マイクロシステムズ](../Page/サン・マイクロシステムズ.md "wikilink")設立に関わることになる。Bill Shannon も後にニューハンプシャーを後にしてサンに合流した。

ちなみにUEGのメインのVAX (decvax) は [UUCP](../Page/Unix_to_Unix_Copy_Protocol.md "wikilink") と [Usenetネットワークの主要ノードのひとつであった](../Page/ネットニュース.md "wikilink")。米国西海岸のUCバークレー (ucbvax) と東海岸の[デューク大学](../Page/デューク大学.md "wikilink") (duke) の[電子メール](../Page/電子メール.md "wikilink")と[ネットニュース](../Page/ネットニュース.md "wikilink")を初めてリアルタイムで接続した。後にネットニュースに圧縮機能が追加されると、decvaxはヨーロッパ（アムステルダムのVrije Universiteit）やオーストラリア（[メルボルン大学](../Page/メルボルン大学.md "wikilink")）にも接続され、少なくとも1日に2回通信を行った。

Armando StettnerはBill Dollとの立ち話で、そろそろDECが自身の製品としてVAX用UNIXを顧客にリリースすべきであると提案した。Bill Munsonへの提案書が作られ、彼はそれを[ケン・オルセン](https://ja.wikipedia.org/wiki/ケン・オルセン "wikilink")に提案した。オルセンはUNIXのライセンスプレートをつかみ、誰かの胸をそれで叩きながら「やろう」と言ったといわれている。Ultrixの始まりである。

UNIXのライセンスプレートとは、Stettnerが作った[自動車](../Page/自動車.md "wikilink")の[ナンバープレート](../Page/ナンバープレート.md "wikilink")状のプレートである。ニューハンプシャー州には "Live Free or Die" というモットーがあり、ナンバープレートにはそれが書かれていた。その言葉とUNIXの精神の類似を感じて、Stettnerはそのようなプレートを作ったといわれている。彼はこれを[Usenix](https://ja.wikipedia.org/wiki/Usenix "wikilink")で配っていた。

### 最初のリリース

最初のUltrix-32は4.2BSDベースで、[System Vからいくつかの機能を持ち込み](../Page/UNIX_System_V.md "wikilink")、[1984年](../Page/1984年.md "wikilink")にリリースされた。その目的はDEC自身がVAX用UNIXをサポートすることにあった。また、decvaxをUUCP/ネットニュースで使っていた経験も生かして、いくつか改造が加えられた。後にUltrix-32は[DECnet](../Page/DECnet.md "wikilink")をサポートし、[DEC LATなどのDEC独自のプロトコルもサポートすることになった](https://ja.wikipedia.org/wiki/DEC_LAT "wikilink")。[コンピュータ・クラスター](../Page/コンピュータ・クラスター.md "wikilink")はサポートしなかった。その後すぐにV7Mをベースとした製品も提供した。[AT\&T](../Page/AT&T.md "wikilink")のライセンス規定により、DEC（も他社も）バイナリのみを配布することしかできなかった。従って、様々な構成に合わせた設定ができるように柔軟な設定機能を追加することに力が注がれた。

後にDECは3つのプラットフォーム向けにUNIXを提供した。[PDP-11](../Page/PDP-11.md "wikilink")（様々なOSが既にあり、その1つとして）、[VAX](../Page/VAX.md "wikilink")（2つの主要OSの1つとして）、そしてDECの最初の[RISC](../Page/RISC.md "wikilink")システムである[DECstation](../Page/DECstation.md "wikilink")ワークステーションと[DECsystem](https://ja.wikipedia.org/wiki/DECsystem "wikilink")サーバである（唯一のOSとしてUltrixが使われた）。DECstation は[MIPSアーキテクチャ](../Page/MIPSアーキテクチャ.md "wikilink")のプロセッサを使用したもので、後の[Alphaではない](https://ja.wikipedia.org/wiki/DEC_Alpha "wikilink")。

本来は *Ultrix-11* と *Ultrix-32* というようにプラットフォーム毎に名称が違っていたが、PDP-11が使われなくなると単に *Ultrix* として知られるようになった。*Buglix* とか *Scrofulix* と中傷されることもあった。[MIPS版Ultrixがリリースされると](../Page/MIPSアーキテクチャ.md "wikilink")、VAX版との違いを示すためVAX/ULTRIXとRISC/ULRTIXと呼ばれるようになった。技術的な重点はサポータビリティと信頼性の向上に置かれ、CPUやデバイスドライバサポートの改良（これはバークレーにも送られた）、ハードウェア故障サポートと復旧や[エラーメッセージ](../Page/エラーメッセージ.md "wikilink")の改善など、様々な改良が施された。Ultrix-32には4.3BSDの機能、[DECnet](../Page/DECnet.md "wikilink")、[TCP/IP](https://ja.wikipedia.org/wiki/TCP/IP "wikilink")、[SMTPなどが追加されていった](../Page/Simple_Mail_Transfer_Protocol.md "wikilink")。

UltrixにはSystem Vの[プロセス間通信](../Page/プロセス間通信.md "wikilink") (IPC) 機能（名前つきパイプ、メッセージ、[セマフォ](../Page/セマフォ.md "wikilink")、[共有メモリ](../Page/共有メモリ.md "wikilink")）も実装された。[SVR4がサンとAT](../Page/UNIX_System_V.md "wikilink")\&Tの共同開発によって[1986年](https://ja.wikipedia.org/wiki/1986年 "wikilink")末に開発され、これにはBSDの機能が取り入れられたわけだが、DECは逆にSystem Vの機能をBSDに取り入れたのである（[UNIX戦争](../Page/UNIX戦争.md "wikilink")参照）。

VAXのワークステーション向けに Ultrix-32 はUWS (Ultrix Workstation Software) と呼ばれる[デスクトップ環境](https://ja.wikipedia.org/wiki/デスクトップ環境 "wikilink")を持っていた。これは[X Window Systemに基づくものである](../Page/X_Window_System.md "wikilink")。後にX11ベースとなりDECwindowsと呼ばれるようになったが、UWSに似せたルック・アンド・フィールが使われた。その後、DECwindowsには [Motif](../Page/Motif_\(GUI\).md "wikilink") のルック・アンド・フィールも追加された。

UltrixはVAXやDECsystemの[マルチプロセッサ](https://ja.wikipedia.org/wiki/マルチプロセッサ "wikilink")システム上で動作した。[カーネル](../Page/カーネル.md "wikilink")は[対称型マルチプロセッシング](../Page/対称型マルチプロセッシング.md "wikilink")をサポートしていたが、完全な[マルチスレッドではなかった](../Page/スレッド_\(コンピュータ\).md "wikilink")。一部のタスクは特定のCPUでのみ動作した（[割り込み処理など](../Page/割り込み_\(コンピュータ\).md "wikilink")）。これは当時の他の[SMP実装](../Page/対称型マルチプロセッシング.md "wikilink")（[SunOS](../Page/SunOS.md "wikilink")など）とは異なる。このように Ultrix は他社と比較してUNIXの最新機能をサポートするのが遅かった（例えば、[共有ライブラリは最後までサポートされず](https://ja.wikipedia.org/wiki/ライブラリ#共有ライブラリ "wikilink")、4.3BSDの[システムコール](../Page/システムコール.md "wikilink")や数学ライブラリなどの[ライブラリ](../Page/ライブラリ.md "wikilink")のサポートも遅かった）。また、様々な問題に悩まされ、特にファイルシステムは不安定だった（4.3BSDのファイルシステムに関する修正は取り入れられなかった）。

### 最後のリリース

OSFへの関与の一環で、DECは Ultrix-32 を [OSF/1](https://ja.wikipedia.org/wiki/OSF/1 "wikilink")で置き換えた。これはAlphaベースのシステムが登場する少し前にリリースされた。OSF/1は[Mach](../Page/Mach.md "wikilink")ベースのカーネルを使い、Ultrixにはない様々な機能を備えていた。UEG（当時は Ultrix Engineering Group）は OSF/1ベースの Digital Unix(後の[Tru64 UNIX](../Page/Tru64_UNIX.md "wikilink")) がDECのハードウェア上で動作するよう信頼性と保守性を重視しつつ開発をおこなった。

Ultrixの最後のメジャーリリースは[1995年](https://ja.wikipedia.org/wiki/1995年 "wikilink")のバージョン4.5であり、DECstationとVAX向けである。その後、[Y2Kパッチがいくつか出ている](../Page/2000年問題.md "wikilink")。

## 外部リンク

いずれも英文

  - [Ultrix FAQ](http://www.supelec.fr/decus/faq/faq-ultrix.html)
  - [Info on Ultrix from OSdata](http://www.osdata.com/oses/ultrix.htm) （最終更新は2002年4月10日）

[Category:BSD](https://ja.wikipedia.org/wiki/Category:BSD "wikilink") [Category:ディジタル・イクイップメント・コーポレーション](https://ja.wikipedia.org/wiki/Category:ディジタル・イクイップメント・コーポレーション "wikilink") [Category:1984年のソフトウェア](https://ja.wikipedia.org/wiki/Category:1984年のソフトウェア "wikilink")
> この記事は[MS-DOS](https://ja.wikipedia.org/wiki/MS-DOS)から翻訳されています。


[thumb](https://ja.wikipedia.org/wiki/ファイル:MS-DOS_6.2V_floppy_disks.jpg "wikilink") **MS-DOS**（エムエス-ディーオーエス、エムエスドス\[1\]）は、[マイクロソフト](../Page/マイクロソフト.md "wikilink")が開発・販売していた、[パーソナルコンピュータ](../Page/パーソナルコンピュータ.md "wikilink")向けの[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink")である。

## 概要

MS-DOSは、1981年発売の[IBM PC用の](../Page/IBM_PC.md "wikilink")[ディスクオペレーティングシステムとして開発されて](../Page/DOS_\(OS\).md "wikilink")「[IBM PC DOS](https://ja.wikipedia.org/wiki/IBM_PC_DOS "wikilink")」として発売されたが、1982年よりマイクロソフトがIBMとの共同開発契約に基づき[コンパック](../Page/コンパック.md "wikilink")等のIBM以外のメーカーに「MS-DOS」名称で[OEM](../Page/OEM.md "wikilink")提供を開始した（ただしマイクロソフトは現在では「MS-DOS」は1981年発売と説明している）。MS-DOSは[CP/M](https://ja.wikipedia.org/wiki/CP/M "wikilink")類似のオペレーティングシステムだが、IBM PCの成功により[16ビット](../Page/16ビット.md "wikilink")パーソナルコンピュータ市場で[デファクトスタンダード](../Page/デファクトスタンダード.md "wikilink")となった。

MS-DOSは主に[Intel 8086系のパーソナルコンピュータ向けのオペレーティングシステムだが](../Page/Intel_8086.md "wikilink")、後に[8ビット](../Page/8ビット.md "wikilink")など各種の[CPU](../Page/CPU.md "wikilink")やコンピュータ用にも移植され、また各種の[組み込み](https://ja.wikipedia.org/wiki/組み込み "wikilink")機器でも使用された。

MS-DOSは基本的には[コマンドラインインタフェースや](../Page/キャラクタユーザインタフェース.md "wikilink")[UNIX](../Page/UNIX.md "wikilink")風の階層型の[ファイルシステム](../Page/ファイルシステム.md "wikilink")を持つ[シングルタスク](https://ja.wikipedia.org/wiki/シングルタスク "wikilink")のオペレーティングシステムだが、各種アプリケーションや、バージョン4\[2\]より付属の[DOSSHELLや](../Page/MS-DOS_Shell.md "wikilink")、別売の[Microsoft Windows 2.0などの併用により](../Page/Microsoft_Windows_2.0.md "wikilink")、[グラフィカルユーザインタフェース](https://ja.wikipedia.org/wiki/グラフィカルユーザインタフェース "wikilink")や疑似[マルチタスク](../Page/マルチタスク.md "wikilink")も使用可能となった。ただしMS-DOS自体は画面描画に関わる[アプリケーションプログラミングインタフェース](../Page/アプリケーションプログラミングインタフェース.md "wikilink")を持たないため、多くのMS-DOS用アプリケーションは機種依存であり、異なる機種間では稼働せず、また移植も容易ではなかった\[3\]。

MS-DOSと互換性を持つオペレーティングシステムには、共同開発のIBM PC DOSの他、[DR-DOS](../Page/DR-DOS.md "wikilink") (Novell DOS)、[オープンソース](../Page/オープンソース.md "wikilink")の[FreeDOS](../Page/FreeDOS.md "wikilink")などがあり、またMicrosoft Windowsのコマンドプロンプトなどの互換環境がある。

バージョン6からはIBMとマイクロソフトのOS共同開発契約が終了し、MS-DOSとIBM PC DOSは並行して開発販売が続けられたが、マイクロソフトはMicrosoft Windows、IBMは[OS/2](https://ja.wikipedia.org/wiki/OS/2 "wikilink")に移行してゆき、2001年頃迄にはMS-DOSおよびIBM PC DOSの各サポートは終了した。

## 歴史

### 開発の経緯

[1980年](https://ja.wikipedia.org/wiki/1980年 "wikilink")7月頃、IBMは後にIBM PCとなるパーソナルコンピュータの開発に着手した\[4\]。しかし、IBMの主力商品である[汎用コンピュータに比べるとごく少数のスタッフとわずかな予算しか与えられなかった](../Page/メインフレーム.md "wikilink")。プロジェクトリーダーのは、可及的速やかに商品化にこぎ着けるためにソフトウェアは自社開発せず、すべて外部から調達する方針を立てた\[5\]。

当時のマイクロソフトは[BASIC](../Page/BASIC.md "wikilink")[インタプリタ](../Page/インタプリタ.md "wikilink")や[アセンブラならびに各種言語の](../Page/アセンブリ言語.md "wikilink")[コンパイラ](../Page/コンパイラ.md "wikilink")等を開発しており、それらの製品のほとんどが当時のパーソナルコンピュータ市場における[デファクトスタンダード](../Page/デファクトスタンダード.md "wikilink")OSである[デジタルリサーチ](../Page/デジタルリサーチ.md "wikilink")のCP/M上で動作するものであった。

IBMはマイクロソフトに対し当初はBASICなどの言語製品の開発を依頼していた\[6\]。OSについても8086対応版のCP/Mをマイクロソフトに開発してもらおうとした\[7\]。しかし彼らはCP/Mのソースの権利を持っていなかった為、[ビル・ゲイツ](../Page/ビル・ゲイツ.md "wikilink")のアドバイスに従ってデジタルリサーチと交渉することにした\[8\]。ところがデジタルリサーチとの交渉はうまくいかず、再びマイクロソフトに開発の依頼を持ち込んだ。\[9\]\[10\]\[11\]\[12\]

マイクロソフトは「M-DOS」というOSを開発した経験はあるが、販売したことはなかった\[13\]。IBMから要求された期日は1年以内という厳しいもので、言語製品の開発に加えてOSにまで手を回す余裕はなかった\[14\]。同じ頃、[シアトル・コンピュータ・プロダクツ](https://ja.wikipedia.org/wiki/シアトル・コンピュータ・プロダクツ "wikilink")はCP/Mが8086に移植されない事に業を煮やし、[ティム・パターソン](https://ja.wikipedia.org/wiki/ティム・パターソン "wikilink")がわずか6週間で開発した[QDOSを](../Page/86-DOS.md "wikilink")、86-DOSとして販売した。基本的には8080/Z80用に作られた[デジタルリサーチ](../Page/デジタルリサーチ.md "wikilink")の[CP/M](https://ja.wikipedia.org/wiki/CP/M "wikilink")クローンであり、[8086に移植して](../Page/Intel_8086.md "wikilink")、ディスク読み込み処理のバッファ管理を改良し、ファイルシステムを新規開発した[FAT12にしたものである](../Page/File_Allocation_Table.md "wikilink")。ファーストバージョンは1980年8月に出荷された\[15\]。

[IBM PC用のOSを必要としていたマイクロソフトは](../Page/IBM_PC.md "wikilink")\[16\]\[17\]、1981年5月にティム・パターソンを雇い\[18\]\[19\]\[20\]、同年7月に86-DOS 1.10を$75,000で購入した。マイクロソフトはバージョンナンバーを変更せず、名前をMS-DOSに変更した。1981年8月にMS-DOS 1.10/1.14を[PC DOS](https://ja.wikipedia.org/wiki/IBM_PC_DOS "wikilink") 1.0としてIBMに提供し、[IBM 5150や](../Page/IBM_PC.md "wikilink")[IBM PCで動作する](../Page/IBM_PC.md "wikilink")3つのOSの1つ\[21\]となった\[22\]。

### 各メーカーへのOEM供給

IBMは当初「PC DOS」名称でIBMのみへの供給を主張し、マイクロソフトはIBM以外のメーカーへのOEM供給を主張した結果、「IBM用はPC DOS名称。マイクロソフトによる各メーカーへのOEM供給も認めて普及を図る」という役割分担となったと言われる。この役割分担は後の[OS/2](https://ja.wikipedia.org/wiki/OS/2 "wikilink") Ver. 1.Xでも同様となる。

リスクを軽減化するために買い取りを避けIBM PCの出荷台数に対して使用料を支払うという[ライセンス](../Page/ライセンス.md "wikilink")契約をしたこと、そしてマイクロソフトから各メーカーへの自由なOEM供給を認めた事が後のマイクロソフトの躍進の原動力と言え、また見方を変えれば、最終的に「軒先を貸して母屋を取られた」IBMの大失策であるとも言えるが、MS-DOS（およびPC DOS）の普及（デファクトスタンダード化）を決定づけたとも言える。

1982年、マイクロソフトはバージョン1.25からIBM以外のメーカーにMS-DOSのOEM供給を開始した。のSB-DOS\[23\]、[コンパック](../Page/コンパック.md "wikilink")のCompaq-DOS\[24\]、のZ-DOS\[25\]\[26\]\[27\]など、供給先メーカーは70社以上に及んだ\[28\]。1983年のバージョン2.0より、IBM以外の各メーカーへのOEM供給品は「MS-DOS」名称に一本化された。OEM供給品に自社の商標（MS）をつけ「MS-DOS」名称としたのは、OEM先メーカーが独自の名前をつけて混乱することを避けるために整理する意味があった。ただし、その後も富士通[FM TOWNSの](../Page/FM_TOWNS.md "wikilink")[TownsOSや各種制御機器など](https://ja.wikipedia.org/wiki/FM_TOWNS#TownsOS "wikilink")、内部的にMS-DOSがOEM提供されている場合には「MS-DOS」の名称はユーザーには見えない場合があった。

MS-DOSは8086系CPUを搭載したパソコンで動作させることが前提の設計だった。各パソコンには専用のハードウェアがあり、MS-DOSもそれぞれ別のバージョンが作られ、その状況は既存のCP/Mと同様で、[CP/Mと同じ方法でハードウェアをエミュレーションして違いを吸収した](https://ja.wikipedia.org/wiki/CP/M#Basic_Input_Output_System "wikilink")。これを実現するためMS-DOSはプライマリディスクドライブやコンソールなどの最小限の内蔵ドライバや内蔵カーネルをブートローダーで読み込み、それ以外のデバイスドライバを起動時に動的に読み込めるモジュール方式を採用した。[OEM](../Page/OEM.md "wikilink")各社はマイクロソフトが提供した開発キットを用い、基本的なI/Oドライバとマイクロソフトの標準カーネルを組み合わせて独自のMS-DOSを作ることができ、普通はハードに添付するディスクの形でユーザーへ届けられた。従って各ハードウェアごとに異なるバージョンのMS-DOSが存在することになり、IBM互換機とMS-DOSマシンの2種類に大きく分類された。のような一部のパソコンはMS-DOS互換だったがIBM互換ではなく、特定のハードやIBM PCのアーキテクチャに依存しないMS-DOS専用に作られたソフトウェアを実行できた。

このデザインはアプリケーションの互換性を高めるのに役立ち、MS-DOSのサービスだけを使ってデバイスI/Oにアクセスする場合は特に有効で、このデザイン方針は後のWindows NTにも影響を及ぼした([Hardware Abstraction Layerを参照](../Page/Hardware_Abstraction_Layer.md "wikilink"))。しかし当時はハードに直接アクセスすることでパフォーマンスを稼ぐアプリが主流を占め、特にゲームではこれが顕著で、各社は次第に、1つのMS-DOSがどの会社のパソコンでも動作するようになった。

### DOSの限界と開発の終焉

DOSは標準で[グラフィカルユーザインターフェース](https://ja.wikipedia.org/wiki/グラフィカルユーザインターフェース "wikilink")や[マルチタスク](../Page/マルチタスク.md "wikilink")機能や[仮想記憶](../Page/仮想記憶.md "wikilink")を持たず、[80386などの](../Page/Intel_80386.md "wikilink")[32ビット](../Page/32ビット.md "wikilink")環境でも「高速な[8086](../Page/Intel_8086.md "wikilink")」としか使用できなかったため、DOSの拡張や次世代OSが待望された。

1985年には[DOSエクステンダー](https://ja.wikipedia.org/wiki/DOSエクステンダー "wikilink")である[DESQview](../Page/DESQview.md "wikilink")\[29\]、同年にDOS上で稼働する「オペレーティング環境」としてMicrosoft Windowsが登場した\[30\]。更に1987年には本格的なDOSの後継OSとしてIBMとマイクロソフトから OS/2 Ver. 1.0 が登場した\[31\]\[32\]。OS/2はDOSと同様に、IBMおよびマイクロソフトの両者から供給されたが、性能やDOS互換環境の問題もあり広く普及しなかったためDOSは継続して使われた\[33\]。

1990年に日本ではIBM DOSのバージョン4からDOS/Vが生まれ、マイクロソフトもバージョン5からDOS/VのOEM供給を開始したため\[34\]、日本でもPC/AT互換機の市場が立ち上がり始めた\[35\]。

1993年のバージョン6からは、IBMとマイクロソフトのOS共同開発契約（OSクロスライセンス契約）が終了したため以後はIBMまたはマイクロソフトの単独開発となった\[36\]。両者は基本部分の互換性は保たれているが、付属ユーティリティの相違などが広がった。マイクロソフトはこのMS-DOS 6を単体販売の最終バージョンとし、1995年の[Microsoft Windows 95以降は単体のDOSも不要となった](../Page/Microsoft_Windows_95.md "wikilink")\[37\]。IBMはDOSの改良を続けたが、1998年のPC DOS 2000が最終バージョンとなり、2001年にはサポートも終了した\[38\]。

## 機能

MS-DOSと名付けられているように、マイクロソフトのパーソナルコンピュータ向けのDOS（ディスク・オペレーティング・システム）であり、主にディスクの管理を行うシングルタスクOSであった。開発当初のCPUにマルチタスク機能・メモリ保護機能がなかったためMS-DOSも対応しておらず、CPUにそれらの機能が搭載された後もMS-DOSが対応することはなかった。またグラフィック画面やサウンドの操作・ネットワーク機能などは、Microsoft Windowsや[LAN Managerのほかアプリケーションが直接I](https://ja.wikipedia.org/wiki/LAN_Manager "wikilink")/Oを操作するか[デバイスドライバ](../Page/デバイスドライバ.md "wikilink")などで提供されていた。

### ファイル管理

ファイルの管理は、[FATと](../Page/File_Allocation_Table.md "wikilink")[クラスタにより構成される](https://ja.wikipedia.org/wiki/クラスタ_\(記憶媒体\) "wikilink")。

ファイル名は[8.3形式](https://ja.wikipedia.org/wiki/8.3形式 "wikilink")、つまり、8バイトまでのベース名と3バイトまでの[拡張子](../Page/拡張子.md "wikilink")の合計最大11バイト（拡張子の前の「[.](../Page/終止符.md "wikilink")」を数えれば12バイト）で表す。アルファベットの[大文字](../Page/大文字.md "wikilink")と[小文字](../Page/小文字.md "wikilink")は区別しない（全て大文字と見なされる）。

バージョン2以降では、[ディレクトリ](../Page/ディレクトリ.md "wikilink")の作成が可能となり、[ファイル属性にも対応した](../Page/属性.md "wikilink")。

### 起動順序

起動順序はバージョンによって若干違うが、概ね以下の通りである。

1.  コンピュータのROM [BIOSやディスクの](https://ja.wikipedia.org/wiki/Basic_Input/Output_System "wikilink")[マスターブートレコード](../Page/マスターブートレコード.md "wikilink")からディスクのセクタ0にある[ブートセクタ](../Page/ブートセクタ.md "wikilink")を読み込んで実行。
2.  ディスクから[`IO.SYS`](../Page/IO.SYS.md "wikilink")と[`MSDOS.SYS`](https://ja.wikipedia.org/wiki/MSDOS.SYS "wikilink")がメモリ中にロードされる。
3.  `IO.SYS`を起動し、その後`MSDOS.SYS`に制御を移行する。
4.  [`CONFIG.SYS`](../Page/CONFIG.SYS.md "wikilink")が起動ドライブの[ルートディレクトリ](../Page/ルートディレクトリ.md "wikilink")にあれば、そこに記述されたデバイスドライバを読み込む。
5.  [バッチ処理](../Page/バッチ処理.md "wikilink")のための[コマンドインタプリタ](https://ja.wikipedia.org/wiki/コマンドインタプリタ "wikilink")でもある標準[シェル](../Page/シェル.md "wikilink")の[`COMMAND.COM`](../Page/COMMAND.COM.md "wikilink")を起動する。
6.  [`AUTOEXEC.BAT`](../Page/AUTOEXEC.BAT.md "wikilink")が起動ドライブのルートディレクトリにあれば、その内容を実行し、[環境変数](../Page/環境変数.md "wikilink")の設定や起動時に実行すべきコマンド等の呼び出し、場合によっては[アプリケーションの起動なども行う](../Page/アプリケーションソフトウェア.md "wikilink")。

`COMMAND.COM`では、各ドライブを`A:`から最大`Z:`まで\[39\]の[ドライブレター](../Page/ドライブレター.md "wikilink")で管理し、内部コマンドではファイル・ディレクトリ一覧の参照、ファイルとディレクトリの作成・コピー・名前変更、コンピュータの時刻や環境変数および[パス](../Page/パス.md "wikilink")の設定参照などができるほか、外部コマンドやアプリケーションなどの[実行形式のファイルの起動が行えた](../Page/実行ファイル.md "wikilink")。またVer.2以降ではUNIXを意識した入出力の[リダイレクト機能や](https://ja.wikipedia.org/wiki/リダイレクト_\(CLI\) "wikilink")[パイプ機能なども利用できたが](../Page/パイプ_\(コンピュータ\).md "wikilink")、MS-DOS上のパイプやリダイレクトはいずれもテンポラリファイルを介した擬似的な実装に留まっていた。

### 実行ファイル

MS-DOSにおける[実行ファイル](../Page/実行ファイル.md "wikilink")の形式は、現在のUNIX系環境で言う[シェルスクリプトに類似したコマンドのバッチ処理を記述する](https://ja.wikipedia.org/wiki/シェル#シェルスクリプト "wikilink")[バッチファイル](../Page/バッチファイル.md "wikilink")(拡張子は`BAT`)と、[CPU](../Page/CPU.md "wikilink")が直接実行するバイナリファイルに大別することができる。

このうちバイナリファイルには、単一の[セグメントを使う](../Page/セグメント方式.md "wikilink")[`COM`](../Page/COMファイル.md "wikilink")形式、複数のセグメントが使用される場合の[`EXE`](../Page/EXEフォーマット.md "wikilink")形式、さらにデバイスドライバとして`SYS`形式が存在し、それぞれ同名の拡張子を持つ。

`COM`形式の実行ファイルは、バイナリ読み込み時に設定されるコード・データ・エクストラ・スタックの各セグメントレジスタの値が同一アドレスに設定され、プログラム内部でセグメントレジスタを操作しない場合は単一セグメント、最大64KBのメモリ空間を操作する。CP/M 80用に書かれた[8080用のアセンブリ言語のソースコードを](../Page/Intel_8080.md "wikilink")8086へコンバートした場合を想定したメモリモデルであるが、`COM`形式のバイナリであってもプログラム側で適切にセグメントレジスタを操作することで64KB以上の空間へのアクセスが可能である。

このうち.`SYS`形式のバイナリは、原則的に起動時に一度だけ実行される`CONFIG.SYS`に記述する以外の方法では直接読み込むことができない\[40\]。

### システムコール

[システムコール](../Page/システムコール.md "wikilink") は、[ソフトウェア割り込みにより呼び出されるが](https://ja.wikipedia.org/wiki/割り込み_\(コンピュータ\)#ソフトウェア割り込み "wikilink")、8080や[Z80](../Page/Z80.md "wikilink")などの8ビットのコンピュータではメジャーな存在だったCP/Mとの互換性、特に8080用にアセンブリ言語で書かれたソースコードを8086にコンバートして用いる場合を想定し、call 5でも利用可能としてCP/M 80からの移行を促した\[41\]。

### メモリ管理

MS-DOSにおいて、DOS自身のカーネルを含むプログラムの実行に確保できるメモリ空間（ユーザーメモリ、コンベンショナル・メモリ）は、8086のアドレス空間の最大1MBである。ほとんどのコンピュータでは、この空間にBIOS ROMや[メモリマップドI/O](https://ja.wikipedia.org/wiki/メモリマップドI/O "wikilink")、[VRAM](../Page/VRAM.md "wikilink")などの空間も存在するため、バンク切替えや様々なメモリ拡張手段などを用いずに一時にアクセス可能なメモリ空間は最大でも640KBから768KB程度\[42\]であった。

[日本語入力用の](../Page/日本語入力システム.md "wikilink")[FEP](https://ja.wikipedia.org/wiki/FEP "wikilink")などの常駐型のデバイスドライバを使用すると一度に使用できるユーザーメモリはさらに減少するため、ユーザーはEMSや[XMS](../Page/XMS.md "wikilink")、[HMAや](https://ja.wikipedia.org/wiki/XMS#HMA "wikilink")[UMBなどの拡張メモリの管理機能を利用して](https://ja.wikipedia.org/wiki/XMS#UMB "wikilink")、[辞書や常駐部やMS](../Page/辞典.md "wikilink")-DOSシステムの一部をそれらへ配置し、コンベンショナルメモリの圧迫を少しでも避けることが重視されるようになった。

そのため、RAMディスクドライブやディスクキャッシュなどは[バンクメモリや](../Page/バンク切り換え.md "wikilink")[EMS](../Page/Expanded_Memory_Specification.md "wikilink")、[プロテクトメモリ](../Page/プロテクトモード.md "wikilink")（[80286](../Page/Intel_80286.md "wikilink")/[386以降](../Page/Intel_80386.md "wikilink")）の機能を用いて、コンベンショナルメモリ以外の領域を使用するのが一般的であった。

これらのメモリ配分の設定は`CONFIG.SYS`や`AUTOEXEC.BAT`を記述することで行い、事実上ユーザーに一任されていた。

バージョン3まではメモリドライバやデバイスドライバはOSには付属せず[サードパーティー](../Page/サードパーティー.md "wikilink")製のメモリドライバ等を使用する必要があったが、バージョン5では標準機能としてOSに付属するようになった。また、これらの環境設定を半自動的に行う設定アプリケーションも添付された。

各種デバイスドライバには自動でインストールを行うスクリプトやプログラムが整備され、動く状態を作るだけであればエンドユーザーがこれらを直接操作する必要はなくなったが、全ての環境に対応するのは難しく最適な設定や問題発生時の対応など初心者にとっては設定のハードルは高かった。

### Windows 9x

従来の[Windows 3.xはMS](../Page/Microsoft_Windows_3.x.md "wikilink")-DOSから起動するアプリケーションであったが、[Windows 9x系では互換性のためにMS](../Page/Windows_9x系.md "wikilink")-DOS相当の機能が一部内部に組み込まれているものの「MS-DOSを必要としないWindowsという単体のOS」となった。Windows 95・98などのWindows本体を起動している状態では[プロテクトモード](../Page/プロテクトモード.md "wikilink")の完全なマルチタスク（プリエンプティブマルチタスク）で稼働しているが、シングルタスクのMS-DOSモード（[DOSプロンプト](../Page/DOSプロンプト.md "wikilink")とは異なる）に切り替えることが可能である。Windows上で起動するDOSプロンプトもMS-DOSと互換性があるが一部動作しないアプリケーションがあり、この問題を解決するための機能がMS-DOSモードで、完全な[CUI表示となり](../Page/キャラクタユーザインタフェース.md "wikilink")、MS-DOSアプリケーションのみが動作し、DOSプロンプト上では[ロングファイルネーム](https://ja.wikipedia.org/wiki/ロングファイルネーム "wikilink")で表示されるVFATであっても8文字+拡張子3文字のショートファイルネーム形式のファイル名で表示され、MS-DOSとほぼ同じ状態になる。

## バージョン

### バージョン一覧

MS-DOSとPC DOSの主要なバージョンの一覧は以下の通り。

<table>
<thead>
<tr class="header">
<th><p>バージョン</p></th>
<th><p>nowrap="" |出荷開始</p></th>
<th><p><a href="../Page/IBM.md" title="wikilink">IBM</a></p></th>
<th><p><a href="../Page/マイクロソフト.md" title="wikilink">マイクロソフト</a></p></th>
<th><p>備考</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>1</p></td>
<td><p>nowrap="" |<a href="../Page/1981年.md" title="wikilink">1981年</a></p></td>
<td><p>nowrap="" |PC DOS 1.0</p></td>
<td><p>nowrap="" |(MS-DOS) 1.25</p></td>
<td><p>1981年 <a href="../Page/IBM_PC.md" title="wikilink">IBM PC用にPC</a> DOSが登場。1982年 マイクロソフトがIBM以外に1.25以降の<a href="../Page/OEM.md" title="wikilink">OEM</a>供給を開始（名称は供給先により異なる）。</p></td>
</tr>
<tr class="even">
<td><p>2</p></td>
<td><p>nowrap="" |<a href="https://ja.wikipedia.org/wiki/1983年" title="wikilink">1983年</a></p></td>
<td><p>nowrap="" |PC DOS 2.0</p></td>
<td><p>nowrap="" |MS-DOS 2.0</p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/PC/XT" title="wikilink">PC/XT</a>用に登場、階層ディレクトリなど。マイクロソフト版の名称が「MS-DOS」に一本化された。日本では<a href="../Page/PC-9800シリーズ.md" title="wikilink">PC-9801などに日本語MS</a>-DOSのOEM供給を開始。</p></td>
</tr>
<tr class="odd">
<td><p>3</p></td>
<td><p>nowrap="" |<a href="../Page/1984年.md" title="wikilink">1984年</a></p></td>
<td><p>nowrap="" |PC DOS 3.0</p></td>
<td><p>nowrap="" |MS-DOS 3.0</p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/PC/AT" title="wikilink">PC/AT</a>用に登場、FAT16など。広く普及し事実上の標準に。同時期に<a href="https://ja.wikipedia.org/wiki/DR_DOS" title="wikilink">DR DOS</a> 4も出荷。</p></td>
</tr>
<tr class="even">
<td><p>4</p></td>
<td><p>nowrap="" |<a href="../Page/1988年.md" title="wikilink">1988年</a></p></td>
<td><p>nowrap="" |IBM DOS 4.0</p></td>
<td><p>nowrap="" |MS-DOS 4.0</p></td>
<td><p>IBM版が名称変更。<a href="https://ja.wikipedia.org/wiki/DOSシェル" title="wikilink">DOSシェル</a>など。IBM版4.05より日本で<a href="https://ja.wikipedia.org/wiki/DOS/V" title="wikilink">DOS/V</a>（IBM DOS J4.05/V）も登場。</p></td>
</tr>
<tr class="odd">
<td><p>5</p></td>
<td><p>nowrap="" |<a href="../Page/1991年.md" title="wikilink">1991年</a></p></td>
<td><p>nowrap="" |IBM DOS 5.0</p></td>
<td><p>nowrap="" |MS-DOS 5.0</p></td>
<td><p>メモリ管理機能強化。IBMとマイクロソフトのOS共同開発の最終版。マイクロソフト版は初めて単体の直接販売が開始される。日本ではマイクロソフト版DOS/V（MS-DOS 5.0/V）も登場し、各社<a href="https://ja.wikipedia.org/wiki/PC/AT互換機" title="wikilink">PC/AT互換機</a>に広く採用される。同時期にDR DOS 6.0 出荷。</p></td>
</tr>
<tr class="even">
<td><p>6</p></td>
<td><p>nowrap="" |<a href="../Page/1993年.md" title="wikilink">1993年</a></p></td>
<td><p>nowrap="" |PC DOS 6.1<br />
PC DOS 6.3</p></td>
<td><p>nowrap="" |MS-DOS 6.0<br />
MS-DOS 6.2</p></td>
<td><p>IBM版が名称再変更。PC DOSとMS-DOSは付属ユーティリティの違いが拡大。MS-DOSは単体販売の最終版。同時期に<a href="../Page/ノベル_(企業).md" title="wikilink">Novell</a> DOS（DR DOS） 7出荷。</p></td>
</tr>
<tr class="odd">
<td><p>7</p></td>
<td><p>nowrap="" |<a href="https://ja.wikipedia.org/wiki/1995年" title="wikilink">1995年</a></p></td>
<td><p>nowrap="" |（なし）</p></td>
<td><p>nowrap="" |MS-DOS 7.0<br />
MS-DOS 7.1</p></td>
<td><p>Windows 95/98/98SEの内部バージョン。PC DOS 7 とは全く別物。7.1はWindows 95 OSR2 以降で、<a href="https://ja.wikipedia.org/wiki/File_Allocation_Table#FAT32" title="wikilink">FAT32に対応した</a>。</p></td>
</tr>
<tr class="even">
<td><p>nowrap="" |1995年</p></td>
<td><p>nowrap="" |PC DOS 7<br />
PC DOS 2000</p></td>
<td><p>nowrap="" |（なし）</p></td>
<td><p>IBM版のみ。スクリプト言語の<a href="../Page/REXX.md" title="wikilink">REXX</a>をサポート。MS-DOS 7 とは全く別物。</p></td>
<td></td>
</tr>
<tr class="odd">
<td><p>8</p></td>
<td><p>nowrap="" |<a href="../Page/2000年.md" title="wikilink">2000年</a></p></td>
<td><p>nowrap="" |（なし）</p></td>
<td><p>nowrap="" |MS-DOS 8</p></td>
<td><p>Windows Meの内部バージョン。MS-DOSの最終版。</p></td>
</tr>
</tbody>
</table>

### バージョン1

CP/M程度の機能しか持たない、基本的なディスクオペレーティングシステム。ファイルシステムは後のバージョンで実装された階層構造を持っておらず、ディレクトリが利用できない。CP/Mとの大きな違いは、汎用化の為などで、[入出力](../Page/入出力.md "wikilink")デバイスなど、機種依存する部分を分離するという方向性である。MSDOS.SYSとIO.SYSという2つのファイルがあることにあらわれている（前者が非依存なモジュール、後者が依存が大きいモジュールである。なお、機種や機能によって、IO.SYSが機能を抱えるか、BIOSに依存するかは異なっており、例えばディスクIOは多くの機種でBIOS依存だが、文字表示位置の制御などはIBM PCではBIOSだが、PC-98ではIO.SYSが行っている）。

このバージョンが使われていた頃は、8086またはその互換プロセッサ（8088等）を利用したパーソナルコンピュータ市場もそれほど大きくなかった為、出荷本数の大半はIBM PCにバンドルされた分だった\[43\]。

  - バージョン1.0（1981年8月）\[44\]- IBM PC（初代）出荷と同時にリリース。64KBのメモリ空間のうち約12KB（そのうちシェルが5KB）を占有した。また、160KBの[5.25インチフロッピーディスク](../Page/フロッピーディスク.md "wikilink") (1D) をサポートしていた。シアトル・コンピュータ・プロダクツの86-DOS 1.14と同等\[45\]。PC DOSのみ。
  - バージョン1.1（1982年5月）\[46\]- 360KB 5.25インチフロッピーディスク (2D) サポートの他、一部のバグフィクス。PC DOSのみ。
  - バージョン1.25（1982年5月）\[47\]- マイクロソフトが、8086プロセッサを利用したパーソナルコンピュータ、更には[IBM PC互換機向けに](https://ja.wikipedia.org/wiki/PC/AT互換機 "wikilink")、IBM以外のメーカーへのOEM提供を開始。日本では当時マイクロソフトの代理店であった[アスキーが日本語版MS](../Page/アスキー_\(企業\).md "wikilink")-DOSを開発している最中で、それに先駆けて複数のメーカーが各自で日本語処理機能を実装して販売していた\[48\]。

### バージョン2

IBM [PC/XTの仕様に合わせ](https://ja.wikipedia.org/wiki/PC/AT#PC_XT "wikilink")、[HDDや](https://ja.wikipedia.org/wiki/ハードディスクドライブ "wikilink")360KB 5.25インチフロッピーディスク (2D) をサポートしている。階層構造ディレクトリ、`CONFIG.SYS`によるデバイスドライバの追加機能、UNIXライクなパイプ等の機能が追加された。アセンブラの[MASMが付属していた](https://ja.wikipedia.org/wiki/Microsoft_Macro_Assembler "wikilink")。

マイクロソフト版はこのバージョンより名称が「MS-DOS」に一本化された。

  - バージョン2.0（1983年3月）\[49\] - PC/XT 出荷と同時にリリースされた。
  - バージョン2.01(1983年5月) \[50\] - 日本では「日本語MS-DOS 2.0」としてリリースされ、[パソピア](../Page/パソピア.md "wikilink")16などに採用された\[51\]\[52\]。
  - バージョン2.1（1983年10月）\[53\] - IBM [PCjr](https://ja.wikipedia.org/wiki/PC/AT#PCjr "wikilink") 向け。
  - バージョン2.11（1983年10月）\[54\] - バージョン2.01とバージョン2.1を統合。アジアやヨーロッパなど多言語市場を意識し、文字セットや日付表示のローカライズをサポート。各社のx86パーソナルコンピュータ向けに広く利用された他\[55\]、日本ではアスキーの市場戦略の関係で、市販ソフトウェアに[サブセット](https://ja.wikipedia.org/wiki/サブセット "wikilink")版の[バンドル](https://ja.wikipedia.org/wiki/バンドル "wikilink")が許されていた\[56\]。
  - バージョン2.25（1985年10月）\[57\] - 東アジア市場向けに2バイト言語に対応を図った「アジアバージョン」。

### バージョン3

当初 IBM [PC/AT](https://ja.wikipedia.org/wiki/PC/AT "wikilink") 用に発売。主として[ネットワーク対応と大容量HD対応の為の](../Page/コンピュータネットワーク.md "wikilink")16ビットFATが追加された\[58\]。本来80286が標準の[PC/AT](https://ja.wikipedia.org/wiki/PC/AT "wikilink")向けだったが、互換性確保目的で80286のプロテクトモードを利用した新機軸は敢えて盛り込まれなかったためサードパーティー製の各種ユーティリティによって機能拡張するユーザが多かった。

ベンダーによる独自拡張などで方言が多くバージョン番号の体系も大きく乱れている\[59\]\[60\]。必要十分なスペックと安定性が評価され、またバージョン4以降の仕様変更の影響を避けるために一部ではかなりの長期間にわたって愛用されていた。

  - バージョン3.0（1984年8月）\[61\] - PC/ATの発売と同時にリリースされた。1.2MB 5.25インチフロッピーディスク (2HD) 及び32MBまでのHDをサポート。HDの論理ボリュームはひとつのみ。
  - バージョン3.1（1984年11月）\[62\] - 3.0のバグフィックス版。別売のまたはで[トークンリング](../Page/トークンリング.md "wikilink")に対応したネットワーク機能が供給された。但し、性能が低く専ら[ノベルの](../Page/ノベル_\(企業\).md "wikilink")[NetWare](https://ja.wikipedia.org/wiki/NetWare "wikilink")などの[NOSが一般的に用いられた](../Page/ネットワークオペレーティングシステム.md "wikilink")\[63\]。日本ではマイクロソフトから日本語版が供給され、日本国内メーカーの多くのパソコンに採用された\[64\]。また、NECのPC-98LT、Handy98、にはROMで内蔵された。
  - バージョン3.20（1986年1月）\[65\] - 720KB 3.5インチフロッピーディスク (2DD) をサポート。フォーマットプログラムの機種依存ルーチンを`IO.SYS`に移したことで移植性を高めている。
  - バージョン3.21 - 3.20のアジアバージョン。2バイトコードに対応し、日本ではAXなどに採用された\[66\]。
      - MS-DOS 3.3（PC-98版） - バージョン3.21を独自拡張\[67\]\[68\]。マイナーバージョンに3.3A～3.3D\[69\]が存在。
  - バージョン3.22（1989年10月）\[70\] - ROM化に対応。同年8月にデジタルリサーチがROM化可能なDR DOSを開発している\[71\]。
  - バージョン3.3（[IBM PS/2版](https://ja.wikipedia.org/wiki/IBM_PS/2 "wikilink")）（1987年4月）\[72\] - IBM主導で開発された。1.44MB 3.5インチディスク (2HD) をサポート。多言語対応の為、コードページが採用された。HDにおいて複数の論理ドライブを扱えるようになった。
  - バージョン3.3（OEM版）（1987年8月）\[73\] - IBM版の同バージョンと同等。

### バージョン4（1986年）

バージョン3.20から派生し、8086上で限定的な[擬似マルチタスク環境を実現したもの](https://ja.wikipedia.org/wiki/マルチタスク#ノンプリエンプティブ・マルチタスク "wikilink")\[74\]。マイクロソフトが開発したが不十分であるとしてIBMには採用されず、にネットワークOSとしてOEMされた他、僅かの用途に留まり絶滅亜種になってしまった\[75\]\[76\]。非同期I/O対応やバックグラウンドタスク規約など資産の一部は [Windows 2.x](../Page/Microsoft_Windows_2.0.md "wikilink") に流用され、また80286プロテクトモードを前提に並行開発されていたもの（当初バージョン5と呼ばれていた）はIBM主導で大幅に改訂され、世に出た時にはOS/2バージョン1.0になっていた。

### バージョン4

IBM主導で開発されたバージョン\[77\]。OS/2色が濃くなり、[IFS](https://ja.wikipedia.org/wiki/IFS "wikilink")やラージバッファ等の追加のみならず管理セクタ数が増やされた事に伴いHDは理論上最大2GBの領域を扱うことができるようになった（実際にはBIOSの制限があった）他、添付ユーティリティを利用すると最大512MBのパーティションまで作成可能になったが\[78\]、その反面余りに多くの変更がファイルシステムに加えられたため非互換性の問題も生じてしまった。

情報が全部公開されていなかったものの、2バイトコードによるユニバーサルランゲージ対応が内部的に完了したのも本バージョンからである\[79\]。従来のバンクメモリに代るEMSの標準サポートによって扱えるメモリ領域が1MB以上に拡張された\[80\]。

互換OSの[DR DOSで好評を博していた](https://ja.wikipedia.org/wiki/DR_DOS "wikilink")「[GEM](https://ja.wikipedia.org/wiki/Graphical_Environment_Manager "wikilink")」に類似のグラフィカルユーザインタフェース環境、「[DOSシェル](../Page/MS-DOS_Shell.md "wikilink")」が添付された\[81\]。これはマウスオペレーションやグラフィカルなメニューによる直感的な操作が行えるもので、依然シングルタスクながらも複数のアプリケーションを重複起動して切替動作させることができ（いわゆるタスクスイッチャ）、GUIもキャラクタベースによる簡易なものとグラフィック画面とテキスト画面を組み合わせたもの（表示が美しく、ポインタの動作もスムーズになる）とを選択できた。DOSシェルのデザインはIBM [Systems Application Architecture](../Page/Systems_Application_Architecture.md "wikilink") [Common User Accessに準拠していた](../Page/Common_User_Access.md "wikilink")\[82\]。

本バージョンには性急な複雑化に伴う非常に多くのバグが存在し、またOS自体が消費するメモリが過大だったため、メーカーによってDOS 3.30 を拡張した DOS 3.31 を採用するなどして4.0を採用しないところが有った\[83\]。特に日本ではコンベンショナルメモリの空き容量が日本語処理アプリケーションの稼動に大きく影響を与えるため、大手メーカーであるNEC、富士通などが3.21系の拡張版のみを販売し続けた。

  - MS-DOS 4.0（マイクロソフト版）（1988年7月）\[84\]
  - IBM DOS 4.0（IBM版、PC DOSより改称）（1988年7月）\[85\]
      - IBM DOS J4.05/V（1990年11月）（日本のみ）\[86\] - いわゆる「DOS/V」の最初のバージョン。末尾の「V」は[VGAを意味し](../Page/Video_Graphics_Array.md "wikilink")、漢字ROMがなくても日本語表示が出来るように拡張されたもので、専用ハードウェアを付加することなく日本語対応が可能になったため日本国内外のPC/AT互換機メーカーが日本市場に参入する契機になった\[87\]。
  - MS-DOS 4.01（マイクロソフト版）（1988年12月）\[88\] - バグフィクス。

### バージョン5

再びマイクロソフト主導で開発された\[89\]。バージョン4で付加された中途半端なユーティリティの多くが削除された一方、80386、[80486等に備わる](https://ja.wikipedia.org/wiki/Intel_486 "wikilink")[仮想86モード](../Page/仮想86モード.md "wikilink")の活用と [Windows 3.0](../Page/Microsoft_Windows_3.x.md "wikilink") との親和性を主眼にほぼ全面的に再コードされたため、[パソコン通信](../Page/パソコン通信.md "wikilink")等を介した約1年にわたる大規模なベータテストを経て市販開始された。IBMの製品へのバンドルに限定せず、巷に溢れるPC/AT互換機へのフル対応を初めからうたいインストーラ込みで発売された最初のMS-DOS（PC DOS）でもある。

メモリ消費は少ないものの大容量ドライブが扱えないバージョン3、その逆で大容量ドライブが使えるがメモリ消費が大きいバージョン4というジレンマを抱えていたが、限りあるメモリ領域の消費を抑える機能を追加することでそれまでの問題を払拭するに至った。このバージョンによりDOSはほぼ完成を見たが8086～80286とその互換CPU上の動作には制約が強まり、結局のところ巧妙なアップグレード戦略の下でハードウエアの買い替え需要が喚起された。

XMSによってDOS本体の一部をHMAに、デバイスドライバやアプリケーションの一部をUMBに待避させることが可能で、コンベンショナルメモリが大きく取れるようになった。またタスクスイッチ規約が明確に定義され、DOSシェルの機能拡張（Windows 3.0 のサブセット化）が図られた。各種LAN対応も進められ、コマンドにヘルプが付されるなど利便性も向上した。

[テキストエディタ](../Page/テキストエディタ.md "wikilink")は、過去のバージョンに標準添付されていた[ラインエディタ](https://ja.wikipedia.org/wiki/ラインエディタ "wikilink")「[`EDLIN`](../Page/EDLIN.md "wikilink")」に加えスクリーンエディタ「」が添付された\[90\]。開発環境として、コマンドラインエディタに加え独自に拡張された構造化BASICコンパイラ[QuickBASIC](../Page/QuickBASIC.md "wikilink")が標準添付されていた。

それまで未公開だったファンクションの多くがユーザに解放されたためカスタマイズやデバイスドライバ開発が更に容易になった。日本ではマイクロソフトがDOS/VのOEM供給を開始し、PC/AT互換機をベースに独自の拡張を行っていたAX陣営や東芝 ([J-3100](https://ja.wikipedia.org/wiki/ダイナブック_\(東芝\) "wikilink"))もこの頃よりDOS/Vへのシフトを進めるようになった\[91\]。また、世界のデファクトスタンダードであるPC/AT互換機のハードウェアでそのまま日本語版OSを使えるようになった為に日本国外のメーカーが積極的に日本市場へ参入し始め、NECの独擅場であった日本市場は大きく変貌することとなった\[92\]。

  - MS-DOS 5.0（1991年6月）\[93\]
  - IBM DOS 5.0（1991年6月）\[94\] - 他マイナーバージョンアップやローカライズ版多数

### バージョン6

[ディスク最適化や](../Page/デフラグメンテーション.md "wikilink")[ディスク圧縮](../Page/ディスク圧縮.md "wikilink")機能（後述）、[コンピュータウイルス](https://ja.wikipedia.org/wiki/コンピュータウイルス "wikilink")検出・除去など、CD-ROMアクセスに必要なMSCDEXの付属等付加機能の充実が主。MS-DOS単体としての最終版。

デジタルリサーチからMS-DOS互換の DR-DOS 6.0 が発売された\[95\]。大きな特徴は補助ユーティリティの大幅な増強である。その為、IBMおよびマイクロソフトでも基本仕様はほとんど変えずに補助ユーティリティを追加する事でバージョン6を発売することになった。IBMは6.1、それに続くマイクロソフトは6.2と、先に出た競合相手よりバージョン番号はそれぞれ0.1だけ大きい。

起動時に特定のキーを押すと`CONFIG.SYS`・`AUTOEXEC.BAT`の一部の行を実行したり、全てバイパスする機能があった。

マイクロソフト版は同時期に発売された [Windows 3.1](../Page/Microsoft_Windows_3.x.md "wikilink") の普及を促すという販売戦略からDOSシェルを廃止したと見られた\[96\]\[97\]。テキストエディタは日本語に対応して共通の`EDIT`となった（PC-98版は`SEDIT`が付属\[98\]\[99\]）。

  - MS-DOS 6.0（1993年3月）\[100\]
  - PC DOS 6.1（IBM DOSより改称）（1993年6月）\[101\] - IBMの独自ビルド。初期のバージョンにはディスク圧縮ユーティリティは添付されておらず、後のPC DOS 6.1 with Compressionでアドスター社の「SuperStor/DS」が添付された（日本語版PC DOS J6.1/V は最初から圧縮ユーティリティ添付）。
  - MS-DOS 6.2（1993年11月）\[102\] - ディスク圧縮ユーティリティ「DoubleSpace」のバグフィクス等\[103\]\[104\]。「DoubleSpace」は、ディスク容量を圧縮し、圧縮されたまま読み書きを可能にするもの。このユーティリティに用いられている技術の一部がスタック・エレクトロニクス社の特許を侵害しているものとして、訴訟を起こされた。 MS-DOS 6.0 のユーザはオンラインの無償アップデートパッケージを入手することで MS-DOS 6.2 にアップグレードできた。
      - MS-DOS 6.2/V（1993年12月） - 日本ではマイクロソフトが自社ブランドで発売した唯一の日本語版MS-DOS単体パッケージ\[105\]。IBM DOS J5.0/VまたはMS-DOS 5.0/Vからのアップグレードのみ。5.0/Vと同様にOEMでも供給。
  - MS-DOS 6.21（1994年2月）- マイクロソフトによるスタック・エレクトロニクス社の特許侵害が一部認められた為、「DoubleSpace」を除去したもの。\[106\]\[107\]
  - PC DOS 6.3（1994年4月）\[108\] - IBMの独自ビルド。MS-DOS 6.2 同様、オンラインの無償アップデートパッケージを入手してPC DOS 6.1 から 6.3 にアップグレードできた。
  - MS-DOS 6.22（1994年6月） - スタック・エレクトロニクス社の特許を侵害しない形で作成されたものが「DriveSpace」として改めて添付された（但し、日本語版には関係ない）。なお、DoubleSpaceとDriveSpaceの圧縮機能には互換性がなく、そのままでは互いに圧縮されたパーティションにアクセスすることができない。\[109\]\[110\]

### バージョン7（マイクロソフト版）

Windows 95/98/98SE に含まれているバージョン。ファイルシステムでは長いファイル名がサポートされたのが最大の特徴。従来の`MSDOS.SYS`は名前こそ同じであるがプログラムではなく設定ファイルとなった。`IO.SYS`が実行する標準シェルはWindowsを起動するための`WIN.COM`であるが、MSDOS.SYSを編集することでWindows 95/98ではWindowsを起動せずにMS-DOSモード（`COMMMAND.COM`）で起動することができた。Windows 95のOSR2以降では[FAT32にも対応しているバージョン](https://ja.wikipedia.org/wiki/File_Allocation_Table#FAT32 "wikilink")7.1である\[111\]。

### バージョン7（IBM版）

1995年リリース。IBM版のみ。開発環境として「[REXX](../Page/REXX.md "wikilink")」を標準添付。ディスク圧縮ユーティリティは「SuperStor/DS」から「Stacker4.0」に変更された\[112\]。MS-DOS 7（マイクロソフト版）とは異なりGUIとの融合はされなかったが、当時[インターネット](../Page/インターネット.md "wikilink")の普及が進んでいた中で[Palm Top PC 110の人気を受けてPC](../Page/Palm_Top_PC_110.md "wikilink") DOS用[ウェブブラウザ](../Page/ウェブブラウザ.md "wikilink")「[WebBoy](https://ja.wikipedia.org/wiki/WebBoy "wikilink")」が開発された\[113\]。

  - PC DOS 7（1995年4月）\[114\]
  - PC DOS 2000（1998年5月）\[115\] - PC DOS 7 をベースに、[ユーロ記号](../Page/ユーロ記号.md "wikilink")の表示や西暦[2000年問題](../Page/2000年問題.md "wikilink")に対応したもの。VERコマンドではPC DOS Version 7.0 Revision 1と表示される。日本語版は製品名から「/V」が外れたが、「DOS/V」部分を含んでいる。これがPC DOS(IBM DOS)およびMS-DOS全体の事実上の最終バージョンとなる（互換OSは除く）。2001年にはサポートが終了した\[116\]。

### バージョン8（マイクロソフト版）

[Windows Meに含まれているバージョン](../Page/Microsoft_Windows_Millennium_Edition.md "wikilink")。`IO.SYS`に`HIMEM.SYS`および`SMARTDRV`（ディスクキャッシュ）の機能を統合した最終版であり、MS-DOSモードでの起動も廃止されWindowsの[ブートローダ](https://ja.wikipedia.org/wiki/ブートローダ "wikilink")の機能のみとなった\[117\]。Windows Meや[Windows XP以降で起動ディスクを作成するとこのMS](../Page/Microsoft_Windows_XP.md "wikilink")-DOSが書き込まれる。

## MS-DOSとの互換性を持つオペレーティングシステム

### MS-DOSとバイナリ互換性を持つオペレーティングシステム

  - [DR-DOS](../Page/DR-DOS.md "wikilink")
  - [PC-Engine](https://ja.wikipedia.org/wiki/PC-Engine_\(オペレーティングシステム\) "wikilink")（[PC-88VA](https://ja.wikipedia.org/wiki/PC-8800シリーズ "wikilink")）
  - [TownsOS](https://ja.wikipedia.org/wiki/FM_TOWNS#TownsOS "wikilink")（FM TOWNS）
  - [FreeDOS](../Page/FreeDOS.md "wikilink")
  - [PTS-DOS](https://ja.wikipedia.org/wiki/PTS-DOS "wikilink")(試用版)
  - [RxDOS](https://ja.wikipedia.org/wiki/RxDOS "wikilink")

またPC-9800シリーズ全盛期には、ゲームソフトの組み込み用として下位互換（INT21系のサブセットのみ互換）の「MEG-DOS」などがあった。[アリスソフト](../Page/アリスソフト.md "wikilink")の「ALICE-DOS」は、もともとゲームソフト本体はMS-DOSをインストールした[ハードディスクドライブ](https://ja.wikipedia.org/wiki/ハードディスクドライブ "wikilink")上で動かすことを前提としあくまでもフロッピー単体でも起動するようサポート用に作られたものであったため、バッチファイルを動かす機能も有していた。

### MS-DOSの影響を受けつつもバイナリ互換性の無いオペレーティングシステム

  - [Human68k](../Page/Human68k.md "wikilink")（[ハドソン](../Page/ハドソン.md "wikilink")、[シャープ](../Page/シャープ.md "wikilink")） - [X68000](https://ja.wikipedia.org/wiki/X68000 "wikilink")、ファイルシステムにFAT12/16のサブセットを採用、`COMMAND.COM`に酷似したコマンドラインインタプリタや、システムコールのファンクションにもINT21Hを真似た設計が見られる等、影響を（主に開発工期の短縮などの側面から）強く受け模倣していることは明らかではあるが、その他は全く別個の実装であり、CPU自体にも互換性は無い。
  - [Carry日本語DOS](https://ja.wikipedia.org/wiki/Carry日本語DOS "wikilink")（[キャリーラボ](../Page/キャリーラボ.md "wikilink")） - [PC-8800シリーズ](https://ja.wikipedia.org/wiki/PC-8800シリーズ "wikilink")/[X1](https://ja.wikipedia.org/wiki/X1シリーズ "wikilink")。通称CDOS-II。ファイルシステムのみFAT12に対応したOSで、CP/Mエミュレータが存在した。Z80を前提としたCP/Mのバリアント（変種）であり、MS-DOSの移植ではない。当然MS-DOS用のバイナリも動作しない。パソコン通信ソフトの一部としても使用され、PC-8800シリーズ版はJET-TERMに、X1シリーズ版はJETターボターミナル（[SPS発売](../Page/エス・ピー・エス.md "wikilink")）に付属する。PC-8800シリーズ版はOSのみのフリー版がある。前身であるCarryDOS(CDOS)とはファイルシステム、システムコールともに互換性はない。
  - [MSX-DOS](../Page/MSX-DOS.md "wikilink") （マイクロソフト、アスキー）\[118\] - [MSX](https://ja.wikipedia.org/wiki/MSX "wikilink")、FAT12のサブセットに対応し、MS-DOSの`COMMAND.COM`に酷似したコマンドインタプリタがある、CP/M互換OS。CDOS-IIと同様にCP/Mのバリアントであり、MS-DOS用のバイナリは動作しない。表計算アプリケーション[Multiplan](https://ja.wikipedia.org/wiki/Multiplan "wikilink")の一部として、PC-8800シリーズ、X1シリーズ、[MZ-2500](https://ja.wikipedia.org/wiki/MZ-2500 "wikilink")にもサブセット版がある。
  - [IDOS](https://ja.wikipedia.org/wiki/IDOS "wikilink")（[ソフトバンク](https://ja.wikipedia.org/wiki/ソフトバンク "wikilink")） - PC-8800シリーズ、[PC-8000シリーズ](../Page/PC-8000シリーズ.md "wikilink")、ファイルシステムのみFAT12に対応した、CP/M互換OS。

## 脚注

### 注釈

### 出典

## 関連項目

  - [マイクロソフトの歴史](../Page/マイクロソフトの歴史.md "wikilink")
  - [Windows 9x系](../Page/Windows_9x系.md "wikilink")
  - [仮想DOSマシン](../Page/仮想DOSマシン.md "wikilink")
  - [Win32コンソール](https://ja.wikipedia.org/wiki/Win32コンソール "wikilink")

## 外部リンク

  - [DOSの歴史セミナ（Altair☆）](https://hp.vector.co.jp/authors/VA000199/history.html)

  - [パソコン産業およびパソコン技術の歴史関連URL](https://www.sanosemi.com/history_of_PC_refURL.htm)

  - [DOSの系譜を辿る](http://www.os.rim.or.jp/~ppp/msdos/SD/)（「Software Design」1998年6月号に掲載されたものを、編集部の許可のもと転載）

  - [PC DOS 7 の修正入手先](ftp://ftp.boulder.ibm.com/ps/products/dos/fixes/dos7.0/)

  - [日本IBM・PC DOS 2000](http://www-01.ibm.com/common/ssi/ShowDoc.wss?docURL=/common/ssi/rep_ca/3/760/PSP98003/index.html&lang=ja&request_locale=ja)

  -
[Category:MS-DOS・Windows3.x・9x系](https://ja.wikipedia.org/wiki/Category:MS-DOS・Windows3.x・9x系 "wikilink") [Category:MS-DOS](https://ja.wikipedia.org/wiki/Category:MS-DOS "wikilink") [Category:IBMのオペレーティングシステム](https://ja.wikipedia.org/wiki/Category:IBMのオペレーティングシステム "wikilink") [Category:パソコンの歴史](https://ja.wikipedia.org/wiki/Category:パソコンの歴史 "wikilink") [Category:1981年のソフトウェア](https://ja.wikipedia.org/wiki/Category:1981年のソフトウェア "wikilink")

1.  日本国商標登録番号第2016333号
2.  一部メーカー用はバージョン5
3.
4.
5.
6.  Manes & Andrews (1993). *Gates*, Doubleday, ISBN 0-385-42075-7.
7.
8.
9.  Evans, Harold (2004). *They Made America*, Little, Brown and Company. ISBN 0-316-27766-5 ISBN 0-316-01385-4.
10. [Operational Choice](https://books.google.com/books?id=w_OhaFDePS4C&pg=PA50), *PC Magazine* Charter Issue, February–March 1982
11. Hamm, Steve; Jay Greene (October 25, 2004). ["The Man Who Could Have Been Bill Gates"](http://www.businessweek.com/magazine/content/04_43/b3905109_mz063.htm). BusinessWeek.
12.
13.
14.
15.
16.
17.
18. このやり方を進言したのは当時同社役員でもあった[西和彦](../Page/西和彦.md "wikilink")と言われている
19.
20.
21.
22.
23.
24. Duncan, Ray (1988). *The MS-DOS Encyclopedia*, Microsoft Press. ISBN 1-55615-049-0.
25. [Zenith's new Z100 has something for everybody](https://books.google.com/books?id=KTAEAAAAMBAJ&pg=PA10), *InfoWorld*, July 12, 1982
26. [Zenith challenges IBM's share of micro market](https://books.google.com/books?id=EDAEAAAAMBAJ&pg=PA35), *InfoWorld*, September 13, 1982
27. [Review: Zenith Z-100](https://books.google.com/books?id=0C8EAAAAMBAJ&pg=PA91), *InfoWorld*, November 7, 1983
28.
29. [AST memory board to come with Quarterdeck Desqview](https://books.google.com/books?id=a8FBzsfoBZEC&pg=PA22), *Computerworld*, November 4, 1985
30. [Microsoft Focuses Efforts On Direct Corporate Sales](https://books.google.com/books?id=OC8EAAAAMBAJ&pg=PA8), *InfoWorld*, November 18, 1985
31. [IBM Ships OS/2 Four Months Early](https://books.google.com/books?id=Az8EAAAAMBAJ&pg=PA1), *InfoWorld*, December 7, 1987
32. [Zenith First to Ship Microsoft OS/2](https://books.google.com/books?id=AT8EAAAAMBAJ&pg=PA1), *InfoWorld*, December 21, 1987
33. [Vendors Decide Against Bundling OS/2 With PCs](https://books.google.com/books?id=BD8EAAAAMBAJ&pg=PA5), *InfoWorld*, November 30, 1987
34. 『日経バイト』 1991年12月号、p.160.。
35.
36.
37. Windows 95以降ではDOSは技術的には内部に存在しているが、製品としてバンドルされている。
38.
39. <span data-ve-clipboard-key="0.5142649835640344-16">ドライブレターの数</span>はCONFIG.SYSの`LASTDRIVE`で変更可。
40. <span data-ve-clipboard-key="0.1444910571201179-4"> ただし、</span>PC-98版のMS-DOS 3.1以降では`ADDDRV.EXE`と登録を記述したファイルの組み合わせにより登録し、`DELDRV.EXE`で外せる。この方法を使用できるのは[キャラクタデバイス](https://ja.wikipedia.org/wiki/キャラクタデバイス "wikilink")のみであり、`CONFIG.SYS`で一度登録したデバイスドライバは外せない。IBM PC用では何種類かサードパーティで同様のプログラムが作成されている。
41. [FAR JMP instruction for CP/M-style calls](http://www.ctyme.com/intr/rb-5797.htm)
42. ユーザーメモリは、IBM PC互換機およびPC-9800シリーズ等では640KB、[PC-H98シリーズ](../Page/PC-H98シリーズ.md "wikilink")やFMRシリーズ・FM TOWNS等は768KB。
43.
44. [IBM Press Release announcing the PC](http://www-03.ibm.com/ibm/history/documents/pdf/pcpress.pdf) August 12, 1981
45.
46. [IBM enhances Personal Computer with 2-sided drives](https://books.google.com/books?id=XDAEAAAAMBAJ&pg=PA3), *InfoWorld*, June 7, 1982
47. Duncan, Ray (1988). *Advanced MS-DOS Programming*, Microsoft Press. ISBN 1-55615-157-8.
48. 「Unix風の機能を持ち込んだ日本語MS-DOS2.0の機能と内部構造」『日経エレクトロニクス』 1983年12月19日号、pp.165-190。
49. Allen, Paul (2011). *Idea Man*, Penguin, ISBN 978-1-59184-382-5.
50.
51.
52.
53. IBM. *PC DOS 2.1 Announcement Letter*. 1983-11-01 ([\[3\]](http://www-01.ibm.com/common/ssi/ShowDoc.wss?docURL=/common/ssi/rep_ca/9/897/ENUS283-389/index.html&lang=en&request_locale=en)).
54.
55. Allan, Roy A. (2001). *A History of the Personal Computer*, Allan Publishing, ISBN 0-9689108-0-7. [eBook on archive.org.](https://ja.wikipedia.org/wiki/iarchive:A_History_of_the_Personal_Computer "wikilink") [Appendix B: Versions of DOS](https://archive.org/download/A_History_of_the_Personal_Computer/eBookAB.pdf)
56. 服部雅幸「トピック・レポート：機能不足が表面化、老兵「MS-DOS2.11」」『日経パソコン』 1991年1月21日号、pp.178-182。
57.
58. もっとも、管理できるセクタ数は65535個であったため、32MB以上のパーティションを切ることは出来なかった。
59. 富士通 FMRシリーズ及びFM TOWNS用MS-DOS 3.1の後期バージョンでは米国版の3.2／3.3の機能の一部が取り入れられていた。PC-98版MS-DOS 3.1は同一のバージョン番号で複数の版が存在し、互換性の問題が生じたことでユーザーやソフトハウスを混乱させた。
60.
61.
62. [IBM Rolls out New PC: Networking products, windowing software also announced](https://books.google.com/books?id=Hy8EAAAAMBAJ&pg=PA11), *InfoWorld*, Sep 10, 1984
63.
64.
65. [PC-DOS upgrade supports 3-in. floppy disk drives](https://books.google.com/books?id=MskyBf-SNfUC&pg=PA2), *Computerworld*, March 24, 1986
66.
67. NECがマイクロソフトから日本語版MS-DOS 3.21の供給を受けてMS-DOS 3.3として販売していた。
68. 光田一徳「トピック・レポート：混乱するMS-DOS―こんなにあるバージョン」『日経パソコン』 1988年12月5日号、pp.183-188。
69. PC-98版のバージョン3.3Dはバージョン5.0と同時発売。見かけ上のセクタサイズを1KB若しくは2KBとすることで最大128Mのパーティションを管理することが出来た。
70. 「米マイクロソフト、ROM化可能なOS―省電力・小型機向け発売。」『日経産業新聞』1989年10月5日、7面。
71. 「デジタル・リサーチ、ROM化可能なOS発売―「MS-DOS」とも互換性」『日経産業新聞』1989年8月29日、9面。
72. IBM. *Operating System/2 Standard Edition Announcement Letter*. 1987-04-02 ([\[19\]](http://www-01.ibm.com/common/ssi/ShowDoc.wss?docURL=/common/ssi/rep_ca/9/897/ENUS287-099/index.html&lang=en&request_locale=en)).
73. [Microsoft to Release Own DOS 3.3](https://books.google.com/books?id=1zsEAAAAMBAJ&pg=PA3), *InfoWorld*, August 3, 1987
74.
75. [MS-DOS 4.0 in U.K.; U.S. Waiting for 5.0](https://books.google.com/books?id=lS8EAAAAMBAJ&pg=PA1), *InfoWorld*, March 24, 1986
76. Larry Osterman. [Did you know that OS/2 wasn't Microsoft's first non Unix multitasking operating system?](http://blogs.msdn.com/b/larryosterman/archive/2004/03/22/94209.aspx) MSDN Blogs
77.
78. [Incompatibilities Hinder Useful DOS 4.0 Features](https://books.google.com/books?id=ZzoEAAAAMBAJ&pg=PA1), *InfoWorld*, August 15, 1988
79. それまでの日本語版DOSはマイクロソフトが日本市場向けに改変したもので、世界共通の仕様ではなかった。また、バージョン3までの英語版DOSをDOS/V化するとファイル名の扱いなどで不具合が生じる場合がある
80.
81.
82.
83. [Users Still Slow to Accept DOS 4.0](https://books.google.com/books?id=tjAEAAAAMBAJ&pg=PT14), *InfoWorld*, July 31, 1989
84.
85. IBM. *PC DOS 4.0 Announcement Letter*. 1988-07-19 ([\[22\]](http://www-01.ibm.com/common/ssi/ShowDoc.wss?docURL=/common/ssi/rep_ca/0/897/ENUS288-380/index.html&lang=en&request_locale=en)).
86. 「MIXハイライト：PC AT互換パソコンでDOS/Vが動いた」『日経バイト』 1991年1月号、pp.326-328。
87.
88. [Microsoft Releases Updated DOS 4; Some OEMs Ship Versions This Month](https://books.google.com/books?id=ADoEAAAAMBAJ&pg=PT16), *InfoWorld*, November 28, 1988
89.
90. PC/AT互換機用の英語版のみ。PC-98版は`SEDIT`（バージョン3.3Dにも付属）、EPSON PC版は`MEDIT`、富士通版（FMRシリーズ、FM TOWNS用）は`EDIAS`と各社ばらばらのコマンド名・機能のエディタが添付された。
91. 「問：東芝のパソコンはDOS/Vパソコンなの？」『日経パソコン』 1994年1月31日号、pp.202-203。
92.
93.
94. IBM. *IBM DOS Version 5.00 and Upgrade*. 1991-06-11 ([\[25\]](http://www-01.ibm.com/common/ssi/ShowDoc.wss?docURL=/common/ssi/rep_ca/2/877/ENUSZP91-0432/index.html&lang=en&request_locale=en)).
95. *Software Developer Caldera sues Microsoft for Antitrust practices alleges monopolistic acts shut its DR DOS operating system out of market* Caldera News, 1996-07-24 ([\[3\]](http://www.maxframe.com/DR/Info/fullstory/ca_sues_ms.html)).
96. 別売のサプリメンタルディスクで配布された。PC-98版には従来どおり付属。
97.
98. [メガソフト](https://ja.wikipedia.org/wiki/メガソフト "wikilink")社の[MIFESのサブセット版](https://ja.wikipedia.org/wiki/Mifes "wikilink")
99. 藤山哲人「PC-9801開発現場の8つの秘密」、『月刊アスキー別冊 蘇るPC-9801伝説 永久保存版 第2弾』、アスキー、2007年4月9日初版、138ページ
100. [MS-DOS 6 hype doesn't match analyst forecasts](https://books.google.com/books?id=PTwEAAAAMBAJ&pg=PA8), *InfoWorld*, March 29, 1993
101. IBM. *IBM PC DOS Version 6.1*. 1993-06-29 ([\[27\]](http://www-01.ibm.com/common/ssi/ShowDoc.wss?docURL=/common/ssi/rep_ca/7/897/ENUS293-347/index.html&lang=en&request_locale=en)).
102. [Notes From the Field](https://books.google.com/books?id=8ToEAAAAMBAJ&pg=PT122), Robert X. Cringely, *InfoWorld*, Nov 8, 1993, p. 122
103. [MS-DOS 6.2 lets users uncompress DoubleSpace volumes;protects data](https://books.google.com/books?id=6joEAAAAMBAJ&pg=PA3), *InfoWorld*, November 1, 1993
104. [MS-DOS 6.2 Addresses DoubleSpace Concerns, Adds Features](https://books.google.com/books?id=E9TvMcu1mIwC&pg=PA37), *PC Magazine*, January 11, 1994
105. 「マイクロソフト、MS-DOS最新版、自社ブランドで発売。」『日経産業新聞』 1993年12月7日、6面。
106. [Microsoft settles for piece of the Stac](https://books.google.com/books?id=x_1p1FQCWXkC&pg=PA30), *Computerworld*, June 27, 1994
107. [The DOS heavyweights go another round](https://books.google.com/books?id=jjgEAAAAMBAJ&pg=PA87), *InfoWorld*, August 29, 1994
108. IBM. *IBM PC DOS Version 6.3*. 1994-04-27 ([\[28\]](http://www-01.ibm.com/common/ssi/ShowDoc.wss?docURL=/common/ssi/rep_ca/3/897/ENUS294-263/index.html&lang=en&request_locale=en)).
109. [Judge rules against Microsoft](https://books.google.com/books?id=QZtKFFB8weQC&pg=PA10#v=onepage&q&f=false), *Computerworld*, June 13, 1994
110. [MS-DOS recall order may disrupt supply line of PCs](https://books.google.com/books?id=fzgEAAAAMBAJ&pg=PA5), *InfoWorld*, June 20, 1994
111.
112. [PC DOS 7 beats its disappearing competitors](https://books.google.com/books?id=oToEAAAAMBAJ&pg=PA68), *InfoWorld*, April 10, 1995
113.
114. IBM. *IBM PC DOS Version 7*. 1995-02-28 ([\[29\]](http://www-01.ibm.com/common/ssi/ShowDoc.wss?docURL=/common/ssi/rep_ca/4/897/ENUS295-074/index.html&lang=en&request_locale=en)).
115. IBM. *IBM PC DOS 2000 Can Ease Your Transition to the Year 2000*. 1998-05-26 ([\[31\]](http://www-01.ibm.com/common/ssi/ShowDoc.wss?docURL=/common/ssi/rep_ca/9/897/ENUS298-169/index.html&lang=en&request_locale=en)).
116.
117.
118.
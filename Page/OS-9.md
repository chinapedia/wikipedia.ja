> この記事は[OS-9](https://ja.wikipedia.org/wiki/OS-9)から翻訳されています。


**OS-9**（**オーエスナイン**）は、[マイクロウェアシステム](https://ja.wikipedia.org/wiki/マイクロウェアシステム "wikilink")によって[モトローラ](../Page/モトローラ.md "wikilink")の[8ビット](../Page/8ビット.md "wikilink")[MPUである](../Page/マイクロプロセッサ.md "wikilink")[6809のために開発された](../Page/MC6809.md "wikilink")[リアルタイムオペレーティングシステム](../Page/リアルタイムオペレーティングシステム.md "wikilink")（以下、RTOS）である。 当時マイクロウェアシステムはモトローラの依頼により共同でプログラミング言語[Basic09](https://ja.wikipedia.org/wiki/Basic09 "wikilink")を開発していた。この言語の開発・実行環境としてマイクロウェアが開発したのがOS-9である。

その後[680x0に移植され](https://ja.wikipedia.org/wiki/MC68000#680x0ファミリ "wikilink")、さらに[x86](https://ja.wikipedia.org/wiki/x86 "wikilink")、[PowerPC](../Page/PowerPC.md "wikilink")、[SH](../Page/SuperH.md "wikilink")、[ARMなど幅広い](../Page/ARMアーキテクチャ.md "wikilink")[CPU](../Page/CPU.md "wikilink")に対応した。 2001年にラディシス社によってマイクロウェアシステムが買収されて一部門となり、2013年に販社グループに売却されてマイクロウェアLP社として独立した。

## 特徴

### プリエンプティブ・マルチタスク

OS-9は、[プリエンプティブ・マルチタスク](https://ja.wikipedia.org/wiki/マルチタスク#プリエンプティブ・マルチタスク "wikilink")（詳細は[プリエンプションも参照のこと](https://ja.wikipedia.org/wiki/プリエンプション#プリエンプティブ・マルチタスク "wikilink")）をおこなうRTOSである。

### マルチプロセス

多くの組み込み用RTOSでは、全ての実行コードを単一のロードイメージにリンクして[メモリに展開](../Page/記憶装置.md "wikilink")・実行するので、並行実行されるタスクは[スレッドモデルであることが一般的だが](../Page/スレッド_\(コンピュータ\).md "wikilink")、OS-9では各タスクは独立したプログラムイメージ（プログラムテキストは複数タスクで共有可）を実行する[プロセス](../Page/プロセス.md "wikilink")モデルである。

プロセスモデルでは各タスクは論理的に独立しているのでタスク間のデータの共有や通信にコストがかかりがちだが、OS-9では「データモジュール」と呼ばれる一種の共有メモリ機能で高速なプロセス間通信を提供している。ただし、タスク間通信に不可欠な[セマフォ](../Page/セマフォ.md "wikilink")が提供されたのはかなり後のことである。また後のバージョンでは[POSIX](../Page/POSIX.md "wikilink")に準拠したプロセス内の複数スレッドをサポートする。

OS-9/6809レベル2では[MMUを使った仮想](../Page/メモリ管理ユニット.md "wikilink")[アドレス空間](../Page/アドレス空間.md "wikilink")をサポートしたが、その他のバージョンでは単一のアドレス空間しか持たないフラットメモリモデルである。OS-9/6809レベル2及びOS-9/68030以降のバージョンでは[ハードウェア](../Page/ハードウェア.md "wikilink")によるプロセス間のメモリ保護機能がある。

OS-9での新プロセス作成は[UNIX](../Page/UNIX.md "wikilink")流の現在のプロセスのコピーではなく、（仮想アドレス空間を持つOS-9/6809レベル2でさえ）実行プログラムを指定する[Windowsの](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")「spawn」に近いモデルである。これは、ベース（セグメント）[レジスタを持たないCPUアーキテクチャでフラットメモリモデルを採用する限りある程度必然であり](../Page/レジスタ_\(コンピュータ\).md "wikilink")、UNIXでも多くの場合せっかくコピーした子プロセスの元の実行イメージは捨てられてexecで新しい実行イメージに置き換えられることを考えれば効率的でもある（マイクロウェアはこれを逆手にとって「OS-9のforkはUNIXよりX倍速い」と喧伝していた）。

### モジュール構造

OS-9を構成するすべての部分は、[モジュール](../Page/モジュール.md "wikilink")と呼ばれる統一された構造を持っており、必要な機能だけを選択して使用することができ、 自由度の高い構造になっている。これにより、OS-9は以下の特徴を有する。

  - [移植性](../Page/移植性.md "wikilink")が高い
    [移植に必要なモジュールだけを新たに作成すればよい](../Page/移植_\(ソフトウェア\).md "wikilink")。個々のモジュールも容易に作成可能。
  - アップグレードが簡単
    対象モジュールのみ交換可能。再起動を必ずしも必要としない。
  - 外部[プログラムを主記憶に常駐させる事が簡単](../Page/プログラム_\(コンピュータ\).md "wikilink")
    [主記憶](../Page/主記憶装置.md "wikilink") ([ROM](../Page/Read_only_memory.md "wikilink")/[RAM](../Page/Random_Access_Memory.md "wikilink")) 上のモジュールはモジュールディレクトリと呼ばれる[ファイルシステム](../Page/ファイルシステム.md "wikilink")の[ディレクトリ](../Page/ディレクトリ.md "wikilink")に似た構造で管理される。外部記憶上のプログラムも予めロードする事によりROM化されたモジュールと同様に主記憶上に常駐した状態にすることが可能\[1\]\[2\]。
  - [セキュリティに強い](../Page/コンピュータセキュリティ.md "wikilink")
    各モジュールに[CRCがあり](../Page/巡回冗長検査.md "wikilink")、モジュールをモジュール[ディレクトリ](../Page/ディレクトリ.md "wikilink")へ登録する際にチェックされるため、正当なモジュールのみメモリにロード可能\[3\]。
  - デバッグが簡単
    OS自体が構造化されているため、問題点の切り分けが行いやすい。
  - リビジョン/エディション
    モジュールにはリビジョン番号とエディション番号があり、同一名のモジュールがメモリ中に複数ある場合、最新のモジュールのみ有効となる。ROM化されたシステムをアップグレードする場合、古いモジュールを削除することなく、新しいモジュールのROMを追加するだけでよい(あるいは外部記憶上の新しいモジュールをRAMへロードするだけでも良い)。
  - [ROM化可能](https://ja.wikipedia.org/wiki/Read_Only_Memory "wikilink")
    すべてのモジュールが[リロケータブル](../Page/リロケータブル.md "wikilink")（かつリエントラント）であることからROM化特有のアドレスを意識しないでプログラミングしたものを、そのままROM化できる。各モジュール（プログラム）は、すべて主記憶空間内のROM上で直接実行が可能である。
    プログラムが使用する変数・スタック領域はカーネルによって実行時に動的に割り当てられる。
  - 再入可能（[リエントラント](../Page/リエントラント.md "wikilink")）
    プログラムがリエントラントであることはOS-9において必須の条件であり、リエントラントでないコードは利用できない\[4\]。プログラムは自身を実行中に書き換えてはならない（自己書き換えコードはリエントラントではない）。
  - メモリ使用効率が高い
    プログラムがリエントラントであるため、コード領域を各プロセスで共有することが可能になり、メモリの利用効率が高くなる。また、OS自身がモジュールの集合であるので、必要なモジュールのみをロード（あるいはROM化）すればよい。
  - 遅い
    汎用性は高いが、専用に設計されたモノリシックOSに比べるとオーバヘッドが生じる。例えば[デバイスドライバ](../Page/デバイスドライバ.md "wikilink")はそれぞれ固有のスタティックストレージと呼ばれる大域変数領域を持つため、カーネルの機能を利用する際には単純な関数呼び出しではなく原則として[ソフトウェア割り込み](https://ja.wikipedia.org/wiki/ソフトウェア割り込み "wikilink")を伴う[システムコール](../Page/システムコール.md "wikilink")を用いる必要がある。

#### OS-9のモジュールの種類

  - カーネルモジュール
      - kernel（6809版を除くカーネル本体）
      - OS9p1 拡張モジュール（6809版ではカーネルのうち起動に最小限必要部分）
      - OS9p2（6809版ではカーネルのうちOS9p1に含まれない残り部分）
      - OS9p3（[漢字変換処理等の拡張で](../Page/インプットメソッド.md "wikilink")[日本語](../Page/日本語.md "wikilink")版のみ）
  - ioman - I/Oシステムの総合管理（後に68000版でkernelに吸収されモジュールとしては存在しなくなったが、OS-9000では再び独立したモジュールとしてkernelから分離された）
  - [ファイルマネージャモジュール](../Page/ファイル_\(コンピュータ\).md "wikilink")
      - RBF - Random Block File Manager （[ディスク](https://ja.wikipedia.org/wiki/ディスク "wikilink")）
      - SCF - Sequencial Character File Manager （[コンソール](../Page/コンソール.md "wikilink")など）
      - SBF - Sequencial Block File Manager （[テープ](../Page/磁気テープ.md "wikilink")）
      - PipeMan - Pipe File Manager （[パイプ](../Page/パイプ_\(コンピュータ\).md "wikilink")）
      - IBF - [IEEE 488](../Page/IEEE_488.md "wikilink") Interface Bus File Manager （エーアールケーコーポレーション製）
      - PCF - PC-DOS equivarent File Manager（[PC-DOS](https://ja.wikipedia.org/wiki/PC-DOS "wikilink")ファイルの操作）
      - NVFM - non-volatile File Manager（CD-iのデータ保存のための、ディレクトリを持たず、[バッファ](../Page/バッファ.md "wikilink")リングしない[ファイルシステム](../Page/ファイルシステム.md "wikilink")）
      - CDFM - Compact Disc File Manager
      - NRF - Non-Volatile RAM File Manager
      - UCM - User Communication File Manager
      - DSM - Display Support Manager
      - GFM - Graphics File Manager
      - MFM - MAUI File Manager
      - NFM - Network File Manager
      - SOCKMAN - Socket File Manager（OS-9/ISP - Internet Support Package に含まれている）
      - IFMAN - 通信インターフェース・ファイル・マネージャ
      - PKMAN - 仮想キーボード・ファイル・マネージャ
      - SPF - Stacked Protocol File Manager（LANComm/SoftStax ネットワーク・サブシステム）
  - デバイスドライバモジュール
      - （例）sc6821 - MC6821用汎用コンソールドライバ
  - デバイスディスクリプタモシュール
      - （例）t0 - デバイスのアドレス、設定値などを保持
  - プログラムモジュール
      - （例）shell、標準ユーティリティプログラム
      - cc - Microware C Compiler\[5\] / ucc - Ultra C Compiler\[6\]
  - データモジュール
      - （例）init - システム初期化定数などを保持
  - BASIC中間コードモジュール
  - 共有ライブラリモジュール（サブルーチンモジュール）
      - runb - MW-BASIC/Basic09ランタイムライブラリ
      - cio - Microware C Compiler 用入出力ライブラリ・サブルーチン・モジュール
      - csl - C language shared library\[7\]
      - psl - presentation support library（CD-i用）
  - システム・モジュール
      - cache - メモリ・キャッシュの効率的使用
      - ssm - System Security Module - MMU等を利用したメモリ保護機能
      - fpu - 浮動小数点コプロセッサの利用（または演算ライブラリ）
      - vector - ハードウェア割り込み管理 (OS-9000)
      - ティッカ・ドライバ - 定周期割り込み
      - RTCドライバ - 時刻の取得・設定
      - align - [アライメントエラーに相当するメモリアクセスの支援](https://ja.wikipedia.org/wiki/データ構造アライメント "wikilink")

### ダイナミックローディング

[カーネル](../Page/カーネル.md "wikilink")以外の多くのモジュールが、システムの稼動中、任意の時点で追加、削除、更新が可能である。例えば[デバイスドライバ](../Page/デバイスドライバ.md "wikilink")は任意の時点でメモリにリンク（ロード）/アンリンク（アンロード）が可能であるため、デバッグ中もカーネルを壊さない限りシステムの再起動を必ずしも必要としない。

またモジュールをメモリにリンク（ロード）するときにリンクカウントがインクリメントされるほか、モジュールを利用（オープン）する度にリンクカウントがインクリメントされ、プロセスでモジュールの利用が終わるとリンクカウントがデクリメントされる仕組みがある。よってモジュールを利用しているプロセスがある間は、故意にアンリンクしようとしてもアンリンク（アンロード）されない。またリンクカウントがゼロになるとモジュールがメモリからアンリンク（アンロード）される。

### メモリ保護

ハードウェアが[MMUを持つ場合](../Page/メモリ管理ユニット.md "wikilink")、メモリ保護機能が有効となる。システム空間とユーザ空間が分離され、また、各ユーザプロセス間も分離される。デバッグ中のユーザープロセスが他のプロセスやシステムを破壊することがない。OS-9/6809では特にLevel2と呼び、最大2MBのメモリを管理できる。

### マルチユーザ

組み込み用途だけではなく、一般のコンピュータとして使用可能であり、UNIXと同様のマルチユーザの機能を備えた[TSSの環境がある](../Page/タイムシェアリングシステム.md "wikilink")。ユーザ、グループ別にファイルやプロセスのアクセス権がある。なお、PC用のOSとして見た場合、8bitや16bit時代の一般的なユーザには、マルチタスク・マルチユーザのメリットが理解されなかった。

### UNIXライク

以上のようなRTOSの上で、[UNIXライクな開発環境が構築されている](../Page/Unix系.md "wikilink")。簡易なものであるが[シェル](../Page/シェル.md "wikilink")も実装されており、[ファイルシステム](../Page/ファイルシステム.md "wikilink")も階層構造を始めとしてUNIXに近い機能を実現している（ユニファイドI/O）。

### OS-9LAN

OS-9には独自の[LANとして](../Page/Local_Area_Network.md "wikilink")[OS-9LAN](https://ja.wikipedia.org/wiki/OS-9LAN "wikilink")がある。LAN上の他のコンピュータの資源に対して、透過的にアクセスが可能な優れたものである。フルパスリストの先頭にコンピュータ名を追加するだけで、そのコンピュータの[ファイルやデバイスにアクセス可能で](../Page/ファイル_\(コンピュータ\).md "wikilink")、例えばシェルからリダイレクトして、LAN上の他のコンピュータに接続されたプリンタに出力可能である。

なお、開発は当初[星光電子](../Page/星光電子.md "wikilink")により、OS-9/6809と[富士通](../Page/富士通.md "wikilink")[FM-11](../Page/FM-11.md "wikilink")+[ARCNetという構成でおこなわれた](https://ja.wikipedia.org/wiki/アークネット "wikilink")。

X68000用のOS-9LANは、[マイクロボード](https://ja.wikipedia.org/wiki/マイクロボード "wikilink")より販売されていた。

### ウィンドウシステム

OS-9/680x0には以下のような[ウィンドウシステム](../Page/ウィンドウシステム.md "wikilink")が発売された。

  - [X Window System](../Page/X_Window_System.md "wikilink"):マイクロウェアが移植。[Motifも付属](../Page/Motif_\(GUI\).md "wikilink")。
  - Personal-Window:マイクロウェアジャパンが、X68000のために開発。
  - G-Windows: ドイツのGESPAC（代理店：フォークス）が開発。
  - XiBase9: ドイツのXiSysが開発。

### 欠点

  - UNIXと異なり、[仮想記憶](../Page/仮想記憶.md "wikilink")機能が存在しないため、搭載された主記憶容量以上の記憶空間が使えない（もっとも、仮想記憶を利用するとリアルタイム性が担保できなくなるため、RTOSとしての意義がなくなる）。
  - 製品として販売した場合、極めて容易に分析、解析が可能である。また、実際にメモリ上にあるモジュールを保存することでコピーが可能であるため、いわゆる[コピープロテクト](https://ja.wikipedia.org/wiki/コピープロテクト "wikilink")が原理的に不可能である。
  - ユーザプログラムがハードウェア資源に直接アクセスできる[CP/M](https://ja.wikipedia.org/wiki/CP/M "wikilink")や[MS-DOS](../Page/MS-DOS.md "wikilink")などのOSに慣れたユーザは、アドレス空間をユーザとスーパバイザに分離したOSにおいて、ハードウェアへのアクセスにドライバが必要なことに不満を述べることが多い（アドレス空間を分離するか否かは、OS-9のレベルやバージョン、使用するハードウェアによる）。
  - プロセス[優先順位の逆転](../Page/優先順位の逆転.md "wikilink")現象\[8\]が存在し、マイクロウェア社が顧客向けに発行する機関紙 "Microware Pipelines" においては、優先したいプロセスのプライオリティを極端に低く設定する事例が頻繁に紹介されていた。
  - 2013年現在、OS-9単独では[対称型マルチプロセッシング](../Page/対称型マルチプロセッシング.md "wikilink")をサポートしていない。

## OS-9/680x0

OS-9は、モトローラの16ビットCPU[68000に移植された](../Page/MC68000.md "wikilink")。以後、6809用はOS-9/6809、68000用はOS-9/68000と呼称されるようになった。その後、68000が[68020](../Page/MC68020.md "wikilink")、[68030とシリーズ展開されるようになると](../Page/MC68030.md "wikilink")、それらに最適化したOS-9/68020、OS-9/68030が開発された。

これらOS-9/680x0は、産業用RTOSとして高いシェアを占めていた。これは、20世紀末には、産業用システムのMPU (CPU) に[680x0が広く採用されていたこと](https://ja.wikipedia.org/wiki/MC68000#680x0ファミリ "wikilink")、ハードウェア資源を効率的に扱う多くの特徴を持っていること、OS-9自体の[移植](../Page/移植_\(ソフトウェア\).md "wikilink")（ポーティング）が容易なことから必然的にそうなったのである。

例えば、ドライバ・モジュールのサンプルコードが多数提供されたことで、個別のハードウェアに対するドライバ・モジュールの移植が容易であり、ドライバモジュールの中であれば[割り込み処理を通常のサブルーチンまたは関数として記述できるなど制約が少なく](../Page/割り込み_\(コンピュータ\).md "wikilink")、安全で柔軟なシステム設計ができた。

また、アプリケーションをセルフで開発できることも評価されていた。ある程度規模の大きな産業用システムでは[VMEバス](../Page/VMEバス.md "wikilink")ベースのシステムが採用されることが多かったが、これら自体によるセルフ開発が可能である。OS-9は数少ない、ターゲット上でセルフ開発が出来るRTOSであった（ただし、登場時のUNIXと同程度の[CUIを利用する必要があった](../Page/キャラクタユーザインタフェース.md "wikilink")。その後、クロス開発環境が一般的になるにつれ、[CodeWarrior](../Page/CodeWarrior.md "wikilink")が採用された時期もあった。現在ではWindowsで動作する[GUIのクロス開発環境Microware](https://ja.wikipedia.org/wiki/グラフィカルユーザインタフェース "wikilink") Hawkもしくは[Eclipse](https://ja.wikipedia.org/wiki/Eclipse "wikilink")によるクロス開発のみ）。

様々な機能の追加による肥大化もあって、多機能版カーネル（デバッグ機能つき）と小型版カーネル（アトミックカーネル）の2種類に分化した。

（68000版を除いて）Ver.3からは[セマフォ](../Page/セマフォ.md "wikilink")、[マルチスレッド](https://ja.wikipedia.org/wiki/マルチスレッド "wikilink")機能も追加され、必要な場合は[POSIX](../Page/POSIX.md "wikilink")スレッドを使用することも可能となった。

## OS-9000（マルチプラットフォーム化）

その後、OS-9は全体が[C言語](../Page/C言語.md "wikilink")で書き直され、[OS-9000](https://ja.wikipedia.org/wiki/OS-9000 "wikilink")として[Intel 80386](../Page/Intel_80386.md "wikilink")、[MIPS](../Page/MIPSアーキテクチャ.md "wikilink")、[SPARC](../Page/SPARC.md "wikilink")、[PowerPC](../Page/PowerPC.md "wikilink")、[ARM](../Page/ARMアーキテクチャ.md "wikilink")、[日立 SH-3、SH-4、SH-5等に移植された](../Page/SuperH.md "wikilink")。アメリカではCで書き直されたOS-9000/68000も発売されたが、市場からは全く相手にされず短期間で販売を終了した。

現在商標は統一され、OS-9のみとなっている\[9\]。6809用、680x0用OS-9の実体は従来の[アセンブリ言語](../Page/アセンブリ言語.md "wikilink")で書かれたOS-9、その他CPU用OS-9の実体はOS-9000である。

## OS-9の稼動する汎用のコンピュータ

日本では、OS-9/6809が富士通[FM-7](../Page/FM-7.md "wikilink")/[8シリーズ](../Page/FM-8.md "wikilink")、[FM-11](../Page/FM-11.md "wikilink")シリーズに移植され富士通から発売、[日立製作所](../Page/日立製作所.md "wikilink")の[ベーシックマスター](../Page/ベーシックマスター.md "wikilink")レベル3シリーズやMB-S1にも移植された（開発はどちらも星光電子）。また、[シャープ](../Page/シャープ.md "wikilink")の[X68000](https://ja.wikipedia.org/wiki/X68000 "wikilink")シリーズには、独自のウインドウシステム (Personal Window) を装備したOS-9/680x0 Ver.2.4が、OS-9/X68000としてシャープから販売された（開発は[マイクロウェアジャパン](https://ja.wikipedia.org/wiki/マイクロウェアジャパン "wikilink")）。その後継製品として、マイクロウェアから、[X68030用のOS](https://ja.wikipedia.org/wiki/X68000#X68030 "wikilink")-9/X68030 Ver.2.4.3も発売された。

他に、[フォークス](https://ja.wikipedia.org/wiki/フォークス "wikilink")から、FM-11や[FM-16β](https://ja.wikipedia.org/wiki/FM-16β "wikilink")、[PC-9801](https://ja.wikipedia.org/wiki/PC-9801 "wikilink")に68000ボードを搭載してOS-9/68000を稼動させる製品、[FM-R](https://ja.wikipedia.org/wiki/FM-R "wikilink")に68020ボードを搭載してOS-9/68020を稼動させる製品が発売されていた。

初期のOS-9/68000の開発環境として著名なものが、星光電子を始めとした国内のデベロッパーが広く使用していた[マイクロボード](https://ja.wikipedia.org/wiki/マイクロボード "wikilink")（マイクロウェアジャパンの親会社）の製品である。同社のVMEバスボードを筐体に収めてセット販売したもので、いわば純正品(?)である。同社からはVMEバスの各種カードが産業用として発売されたが、それ以外にも、PC/ATマザーボードと同規格の基板に[68030を載せたPCスタイルの製品も発売された](../Page/MC68030.md "wikilink")。

また、マイクロボード以外にも多くのメーカーの[VMEバス](../Page/VMEバス.md "wikilink")([VXIバス](../Page/VXIバス.md "wikilink"))、[マルチバス](https://ja.wikipedia.org/wiki/マルチバス "wikilink")、[PCI](../Page/Peripheral_Component_Interconnect.md "wikilink")/[CompactPCI](https://ja.wikipedia.org/wiki/CompactPCI "wikilink")バスのボードがOS-9に対応していた（いる）。例えば、[モトローラ](../Page/モトローラ.md "wikilink")（代理店：[丸文](https://ja.wikipedia.org/wiki/丸文 "wikilink")）、[アドバネット](https://ja.wikipedia.org/wiki/アドバネット "wikilink")、[アバールデータ](https://ja.wikipedia.org/wiki/アバールデータ "wikilink")、[オムロン](../Page/オムロン.md "wikilink")、[シャープ](../Page/シャープ.md "wikilink")、[橘テクトロン](https://ja.wikipedia.org/wiki/橘テクトロン "wikilink")、[タンバック](https://ja.wikipedia.org/wiki/タンバック "wikilink")、[電産](https://ja.wikipedia.org/wiki/電産 "wikilink")、[東京エレクトロン デバイス](../Page/東京エレクトロン_デバイス.md "wikilink")、[フォークス](https://ja.wikipedia.org/wiki/フォークス "wikilink")、[フォース・コンピュータ](https://ja.wikipedia.org/wiki/フォース・コンピュータ "wikilink")（代理店：[インターニックス](https://ja.wikipedia.org/wiki/インターニックス "wikilink")）、[マイクロクラフト](https://ja.wikipedia.org/wiki/マイクロクラフト "wikilink")などの製品である。（五十音順）

米国では、[Apple II用の](../Page/Apple_II.md "wikilink")6809カード (The Mill) がOS-9/6809を標準OSとしていた他、[タンディカラーコンピュータ](https://ja.wikipedia.org/wiki/ラジオシャック#タンディ時代 "wikilink") (CoCo)、MM/1等、また、PC/ATに68020カード（[アルプス電気](https://ja.wikipedia.org/wiki/アルプス電気 "wikilink")製）を搭載してOS-9/68020を稼動させる製品が発売されていた。また、[Macintosh](../Page/Macintosh.md "wikilink")用OS-9/68000も発売されていた。これは、すべてがスーパバイザモードで動作する当時のMacintosh OSをうまく利用し、TOOLBOXを利用可能としていた。

## OS-9が採用された代表的な機器

  - モトローラの[PDA](../Page/携帯情報端末.md "wikilink")。
  - デジタルサンプリング・シンセサイザー（[電子楽器](../Page/電子楽器.md "wikilink")） - [フェアライトCMI](../Page/フェアライトCMI.md "wikilink") (Fairlight CMI)。
  - [BMW](../Page/BMW.md "wikilink")・[750iシリーズ純正カーナビゲーションシステム](../Page/BMW・7シリーズ.md "wikilink")。
  - [マスプロ電工](../Page/マスプロ電工.md "wikilink") カーナビゲーションシステム。
  - [ソニー](../Page/ソニー.md "wikilink")と[フィリップス](../Page/フィリップス.md "wikilink")が提唱した[CD-i](../Page/CD-i.md "wikilink")（セットトップボックスの統一規格で、OS部分は[CD-RTOS](https://ja.wikipedia.org/wiki/CD-RTOS "wikilink")と呼ばれた）。
  - 日立製作所の銀行用[ATM](../Page/現金自動預け払い機.md "wikilink")。
  - [レーザープリンター](../Page/レーザープリンター.md "wikilink")用エンジン。
  - TCP/IP用[ルーター](../Page/ルーター.md "wikilink")。
  - 情報端末機器 - [サクサホールディングス](../Page/サクサホールディングス.md "wikilink")SAXA(TAMRA) DT-300 (OS-9/SH3,MAUIを搭載)。
  - [携帯電話](../Page/携帯電話.md "wikilink")。
  - [POS端末](../Page/販売時点情報管理.md "wikilink")。
  - [パチンコ](https://ja.wikipedia.org/wiki/パチンコ "wikilink")台および玉の供給システム。
  - [ボウリング](../Page/ボウリング.md "wikilink")ピン制御。
  - かつて[メダルゲーム](../Page/メダルゲーム.md "wikilink")機を製造するシグマが開発したビデオスロット、ビデオポーカー、メカニカルスロットのゲーム基板(6809を2つ搭載)。

## 評価と現状

もともとオペレーティングシステムではなく[マルチメディア](../Page/マルチメディア.md "wikilink")関連の[ミドルウェア](../Page/ミドルウェア.md "wikilink")が目当てでマイクロウェアを[2001年](../Page/2001年.md "wikilink")に買収したRadisysのウェブサイトでOS-9は\[Microware OS-9\]として紹介され、ライセンスの販売（そしておそらくはサポートも）は古くからOS-9を手がけてきたシステムビルダ3社による代理販売となっていたが、Radisysは最終的に[2013年](../Page/2013年.md "wikilink")3月にOS-9とMicrowareに関わるブランドを含む全権利をこの3社による共同事業体 (Microware LP) に譲渡した。 誕生から30余年を経たOS-9は[2015年](../Page/2015年.md "wikilink")現在も開発が続けられており、OS-9 v6.0のリリースが予定されている。

## 関連書籍

### 洋書

  -
  -
  -
  -
  -
  -
  -
### 和書

  -
  -
  -
  -
  -
  -
  -
  -
  -
  -
  -
  -
  -
  -
  -
## 外部リンク

  - [マイクロウェアオフィシャルサイト](https://www.microware.com/)
  - [株式会社ルネサステクノロジ - リアルタイムOS](http://www.renesas.com/jpn/products/mpumcu/tools/partner/rtos/os_radisys_preliminary.htm)
  - [株式会社エーアイコーポレーション - 「OS-9向けに組込み用電源断対応ファイルシステム『RTFiles』の供給を開始」](http://www.aicp.co.jp/news/20040610_rtfiles.shtml)
  - [nikkeibp.jp - 「日通工、電話やLANに接続できるタッチパネル式情報端末『Addシリーズ』を発売」](http://bizns.nikkeibp.co.jp/cgi-bin/search/wcs-bun.cgi?ID=52076&FORM=biztechnews)
  - [NECインフロンティア株式会社 - テレデータターミナル Addシリーズ](http://www.necinfrontia.co.jp/products/add/2_2_02.htm)
  - [Sun Java Platform Resellers Deliver Java Technology for Embedded Devices - Microware](http://java.sun.com/products/consumer-embedded/whitepapers/javaresellers-wp.html#microware)
  - [Real-Time Services Inc. - OS-9 World Wide Archive](http://os9archive.rtsi.com/index.html)
  - [ARK Systems USA(旧ページ)](http://www.arkusa.com/www/price_list.html)
  - [Embedded業界紳士録 - 星 光行](http://www.caravan.net/eis/Cover/hoshi.html)
  - [富士通株式会社 - 富士通ミュージアム - FM-11AD2+](http://jp.fujitsu.com/museum/products/computer/personalcomputer/fm11ad2.html)
  - [情報処理学会 - コンピュータ博物館 - 【富士通】FM-11](http://museum.ipsj.or.jp/computer/personal/0008.html)
  - [株式会社フォークス](http://www.forks.co.jp/)
  - [サクサ株式会社 - ディスプレイターミナル DT300](http://www.saxa.co.jp/product/card/dt300.html)

## 脚注

[Category:リアルタイムオペレーティングシステム](https://ja.wikipedia.org/wiki/Category:リアルタイムオペレーティングシステム "wikilink") [Category:組み込みオペレーティングシステム](https://ja.wikipedia.org/wiki/Category:組み込みオペレーティングシステム "wikilink") [Category:1980年のソフトウェア](https://ja.wikipedia.org/wiki/Category:1980年のソフトウェア "wikilink")

1.  ROM化されたモジュールはカーネルが起動時にROM領域を検索してモジュールディレクトリに登録する。
2.  1つのディレクトリにファイル名が同じファイルを複数置けないのと同様に、モジュールディレクトリにモジュール名が同じモジュールを置く事が出来ない。モジュールディレクトリがシステムにひとつしかないOS-9（6809版と68000版）ではマルチユーザで運用する際に時々問題となったが、この対策としてOS-9000ではモジュールディレクトリに階層構造がサポートされた。
3.  6809のような8ビットCPUにはモジュールのCRCチェックは重い負荷であったため、外部プログラムの実行開始がもたつく事があったが、必要なモジュールを予めロードすることでCRCチェックを先に済ませておく事が出来た
4.  富士通FM77AVシリーズの日本語カード用漢字変換のようにOS-9のモジュールでない外部プログラムコードを利用していたケースがある。
5.  当時、マイクロウェアはMicroware C Compiler をANSI準拠と称していた。実際にパーサーも改良され、ANSI準拠のライブラリも準備されたが、最期までプロトタイプが実装されず、実質はK\&R準拠のCコンパイラであった。
6.  Ultra C Compiler は ANSI X3.159-1989準拠のコンパイラである。
7.  ANSI C準拠ライブラリモジュール。Micoware Ultra Cでコンパイルされたモジュールを実行するのに必要となる。
8.  OS-9ではプロセスのプライオリティはタイムスライス事に加算されるエイジの初期値であり、スケジューラはエイジの値によって次にアクティブにするプロセスを決定する。CPU時間が割り当てられたプロセスのエイジは初期化されるが、優先度が高いプロセスは優先度の低いプロセスより大きなエイジ値が維持されやすいのでCPU時間が割り当てられる可能性が高い。優先度の低いプロセスもCPU時間が割り当てられない事でエイジ値が大きくなり、どこかの時点で優先度の高いプロセスのエイジ値を上回る事になる。この「優先度の低いプロセスにもいつかは必ずCPU時間が割り当てられる」事がOS-9のスケジューラの特徴であり、優先度が高いプロセスがレディ状態であってもより優先度が低いプロセスがアクティブになる事がある理由である(この点からOS-9はリアルタイムOSではないとする主張もある)。後にシステム変数によって優先度の低いプロセスのエイジ値の上限を設定できるようになり、ある程度の制御は出来るようになった。
9.  OS-9 Ver.3よりOS-9の名で[RISC](../Page/RISC.md "wikilink")プロセッサをサポート。
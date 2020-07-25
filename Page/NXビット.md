> この記事は[NXビット](https://ja.wikipedia.org/wiki/NXビット)から翻訳されています。


**NXビット** (No eXecute bit) は、[ノイマン型](../Page/ノイマン型.md "wikilink")アーキテクチャの[コンピュータ](../Page/コンピュータ.md "wikilink")において特定のメモリ領域（に置かれたデータ）に付与する実行不可[属性](https://ja.wikipedia.org/wiki/属性#コンピュータ分野 "wikilink")、またはその属性付与機能を指す。

## 概要

NXビットは、端的に言えば「[データ](../Page/データ.md "wikilink")の誤実行」を防ぐために用いられる。そのしくみは、メモリをコード（プロセッサ命令）領域とデータ領域とに分離し、データを配置したメモリ領域にあらかじめ特別な印（属性）を付与することで、この領域のデータを実行しないようにする（実行を試みた際に例外＝[エラー](../Page/エラー.md "wikilink")を発行する）ものである。

典型的には、[バッファオーバーラン](https://ja.wikipedia.org/wiki/バッファオーバーラン "wikilink")攻撃（後述）等に代表される、[ヒープ](../Page/ヒープ.md "wikilink")や[スタック](../Page/スタック.md "wikilink")領域等に置かれたデータを破壊ないしは書き換えて任意のコードを挿入し実行を誘う攻撃を、[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink")と[CPU](../Page/CPU.md "wikilink")の協調により保護するために用いられる機能である。 その機能自体は、[汎用機や](../Page/メインフレーム.md "wikilink")[ワークステーション](../Page/ワークステーション.md "wikilink")等の分野では既に特に目新しいものではなかったが、[パーソナルコンピュータ](../Page/パーソナルコンピュータ.md "wikilink")用に最も普及した[IA-32](../Page/IA-32.md "wikilink")/[AMD64アーキテクチャにおける](https://ja.wikipedia.org/wiki/x64 "wikilink")[実装](../Page/実装.md "wikilink")は比較的最近の出来事であり、最初に実装したAMD64系列が搭載したものを"NXbit"と呼称したため、一般にはこの名称が普及した。

ノイマン型アーキテクチャのコンピュータでは、プログラムをメモリ上にデータとして読み込み、逐次実行する。メモリを読み取った際それがデータであるかプログラムであるのかを、単にメモリ上のデータのみをもって判断することは、ノイマン型では本質的に不可能である。バッファオーバーラン（バッファーオーバーフロー）等と呼ばれる攻撃は、ノイマン型コンピュータのこのような性質を悪用して行われる。

なお、[インテル](https://ja.wikipedia.org/wiki/インテル "wikilink")はこの機能を**XDビット** (eXecute Disable) と称している。しかしながら、インテルのXDビットとAMDのNXビットは同一の機能を持ち、従って名称以外は全く同一のものである。

## ハードウェアの背景

[x86](https://ja.wikipedia.org/wiki/x86 "wikilink")プロセッサは[80286以来](../Page/Intel_80286.md "wikilink")[セグメント](../Page/セグメント.md "wikilink")レベルで実装された近い機能を持っていた。しかしこのメモリ管理モデルは特にフラットメモリモデルを採用する近年のソフトウェアで使うには粗末なものであり、セグメントではなくページ単位で実行を制御する新しい機構が求められていた。

このページレベルの機構は、ここ数年で[サン・マイクロシステムズ](../Page/サン・マイクロシステムズ.md "wikilink")の[SPARC](../Page/SPARC.md "wikilink")、[DECの](../Page/ディジタル・イクイップメント・コーポレーション.md "wikilink")[Alpha](https://ja.wikipedia.org/wiki/DEC_Alpha "wikilink")、[IBM](../Page/IBM.md "wikilink")の[PowerPC](../Page/PowerPC.md "wikilink")といったx86プロセッサでない他のアーキテクチャのCPUで装備されてきた。インテルは[2001年](../Page/2001年.md "wikilink")に[IA-64](../Page/IA-64.md "wikilink")アーキテクチャの[Itanium](../Page/Itanium.md "wikilink")（コードネーム"[Merced](https://ja.wikipedia.org/wiki/マーセド "wikilink")"）プロセッサで同様の機能を装備したが、より一般的なx86プロセッサ（[Pentium](https://ja.wikipedia.org/wiki/Pentium "wikilink")、[Celeron](https://ja.wikipedia.org/wiki/Celeron "wikilink")、[Xeon](../Page/Xeon.md "wikilink")など）には装備しなかった。x86プロセッサの機能としては[AMDがAMD](https://ja.wikipedia.org/wiki/アドバンスト・マイクロ・デバイセズ "wikilink")64シリーズ（[Athlon 64](../Page/Athlon_64.md "wikilink")、[Opteron](https://ja.wikipedia.org/wiki/Opteron "wikilink")など）で実装し、「NXビット」と呼んでいる。「NXビット」という用語は現在、他のプロセッサの似た技術を指し示す場合にも使われるようになってきた。

AMDがx86プラットホームを強化するという決定の後、インテルもインテルのx86プラットフォームも強化する事を決定し、Prescottコアを持ち[LGA775](https://ja.wikipedia.org/wiki/LGA775 "wikilink")ソケットを実装した[Pentium 4プロセッサから近い機能を装備した](../Page/Pentium_4.md "wikilink")。

NXビットはx86プロセッサの[ページテーブル](../Page/ページテーブル.md "wikilink")エントリ内の63番目ビットを明確に参照する（最後のビット、[64ビット](../Page/64ビット.md "wikilink")整数で最初のビットが0で始まる場合）。このビットが0にセットされていればコードはそのページから実行される。1にセットされていれば、コードはそのページから実行することはできず、そのページの全てはデータとして扱われる。またこれらのページはx86本来のページテーブルフォーマットではなく、[物理アドレス拡張](../Page/物理アドレス拡張.md "wikilink")ページテーブルフォーマットに準拠している必要がある。

## 機能のソフトウェアエミュレーション

この機能がハードウェアに搭載される前には、数々のオペレーティングシステムが、W^XまたはExec Shieldなど、ソフトウェアを通してこの機能を実現しようとした。これらはこの記事の最後の方で解説される。

NXビットの機能を利用可能、もしくは[エミュレート可能な](../Page/エミュレータ.md "wikilink")[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink") (OS) は、スタックもしくはヒープメモリ領域が実行可能になる事から保護し、実行可能メモリが書き込み可能になる事から保護できる。これはスタックオーバーフロー攻撃、特にSasserやBlasterワームのようなプログラムが挿入されて実行される事から保護する。これらの攻撃はメモリのある部分（通常はスタック）が書き込み可能でありかつ実行可能である事に依存している。よって、この条件を満たしていなければ攻撃は失敗する。

## オペレーティングシステムにおける実装

多くのオペレーティングシステム (OS) がNXの手段を実装もしくは保持しており、また数種のOSはNXエミュレーションを実装もしくは保持している。これはアルファベット順のOSリストである。それぞれ、技術は新しいものから古いものへの順となっている。

それぞれのOSの最初には、それぞれの技術がサポートする主要な機能が掲載されたデータ表がある。これらのOSの本質がその本質に関する情報の好都合な拡散を保証するので、これらの表は下記を要約するために提供されている。表は下記の構成となっている。

  - ハードウェアでサポートしているプロセッサ:（カンマで区切られたプロセッサの一覧）
  - エミュレーション:（なし）または（アーキテクチャ依存）または（カンマで区切られたプロセッサの一覧）
  - その他のサポート:（なし）または（カンマで区切られたプロセッサの一覧）
  - 標準で搭載されているか:（はい）または（いいえ）または（この技術を搭載しているディストリビューションまたはバージョンのカンマで区切られた一覧）
  - リリース日:（最初にリリースされた日）

アーキテクチャ依存エミュレーションを供給するOSはハードウェアでサポートしていない全てのプロセッサ上で機能する。「その他のサポート」行はまだ明白ではない手段、たとえば明確なNXビットを搭載していないハードウェアが何らかの方法で機能を実現しているプロセッサのためにある。

### OpenBSD

#### W^X

[OpenBSD](../Page/OpenBSD.md "wikilink")オペレーティングシステムの技術として知られるW^X (Write XOR Execute)\[1\] はAMD64ポートで、このようなシステムにW^Xを最大限活用させるためにNX技術を利用している。W^Xは現在のOpenBSDではNXビットをサポートしていないCPUのW^Xもサポートする。

W^XはAlpha、AMD64、[PA-RISC](../Page/PA-RISC.md "wikilink")およびSPARCプロセッサのNXビットをサポートする（しかしインテルの[Intel 64は当初NX機能がなかったためこれをサポートしていないことは特筆に値する](https://ja.wikipedia.org/wiki/x64 "wikilink")）。

OpenBSD 3.3は[2003年](../Page/2003年.md "wikilink")[5月1日](../Page/5月1日.md "wikilink")にリリースされ、これが最初にW^Xを含んだものである。

  - ハードウェアでサポートしているプロセッサ: Alpha、AMD64、PA-RISC、SPARC
  - エミュレーション: IA-32 (x86)
  - その他のサポート: なし
  - 標準で搭載されているか: はい
  - リリース日: 2003年5月1日

### NetBSD

[NetBSD](../Page/NetBSD.md "wikilink") 2.0およびそれ以降の時点では（2004年12月9日）、NXビットをサポートするアーキテクチャは実行可能ではないスタックとヒープを持つ。

AMD64、SPARC64、SPARC (sun4m, sun4d)、PowerPC (ibm4xx)、Alpha、[SH5および](../Page/SuperH.md "wikilink")[PA-RISC](../Page/PA-RISC.md "wikilink")よりなるこれらはページ毎の粒度をもつ。

PowerPC（例:macppc）、[80386はリージョン粒度のみをサポートする](../Page/Intel_80386.md "wikilink")。

NetBSDはデフォルトではNXビットの機能を提供するいかなるソフトウェアも使用していないため、他のアーキテクチャは実行可能でないスタックやヒープからの恩恵は受けない。

### Linux

[Linux](../Page/Linux.md "wikilink")自身は標準のハードウェアNXをサポートする。現在は[64ビット](../Page/64ビット.md "wikilink")CPUにおいてもNXをサポートする64ビットモードと同様にIngo MolnarのNX有効化パッチにより32ビットモードでもサポートしている。これには現在のAMDの64ビットCPUとインテル、[トランスメタ](../Page/トランスメタ.md "wikilink")および[VIAから発表のあった将来のCPUも含まれる](../Page/VIA_Technologies.md "wikilink")。[リーナス・トーバルズ](../Page/リーナス・トーバルズ.md "wikilink")はNXパッチに興味を持ち、標準で有効とされるべきだと考え2.6.8 releaseからは標準装備となった。これは32ビットのx86CPUおよび64ビットのx86互換CPUにて実行する32ビットのx86[カーネル](../Page/カーネル.md "wikilink")においては重要である。32ビットのx86カーネルはAMD64やIA-64が提供するNXビットを通常予期しない。NX有効化パッチはカーネルがもしNXビットが存在したら使用するようにさせる。 このパッチ時点では、LinuxはIntel, AMD, TransmetaおよびVIAが提供するNXビットをサポートしたCPUにおいてはハードウェアNXを完全に活用している。このNXパッチはLinux Kernel Mailing Listにおいて[2004年](../Page/2004年.md "wikilink")[6月](../Page/6月.md "wikilink")に提供された。 同様の技術はx86でないCPU向けに多数のリリースにおいて存在している。

#### Exec Shield

[レッドハット](../Page/レッドハット.md "wikilink")のカーネル開発者Ingo MolnarはExec Shieldという32ビットx86CPUでLinuxがNX機能を活用できるようにするLinuxカーネルパッチを提供した。後にMolnarは32ビットカーネル上でハードウェアNXをサポートするLinux NXパッチを提供した。

Exec Shieldパッチは2003年[5月2日](../Page/5月2日.md "wikilink")にLinux Kernel Mailing Listに提供された。このパッチは、複雑なエミュレーションを実現するために基礎的なコードに重大な改変を加えるためカーネルには取り込まれなかった。

  - ハードウェアでサポートしているプロセッサ: NXをサポートするLinuxがサポートする全てのプロセッサ
  - エミュレーション: NXの模倣は、IA-32 (x86) および互換品のコードセグメント制限を使用する
  - その他のサポート: なし
  - 標準で搭載されているか: [Red Hat Linux](../Page/Red_Hat_Linux.md "wikilink")
  - リリース日: 2003年5月2日

#### PaX

[PaX](../Page/PaX.md "wikilink")のNX技術はNXビットもしくはNX機能をエミュレートもしくはハードウェアのNXビットを使用することができる。PaXは32ビットのx86のようにNXビットを持っていないx86 CPUで使用することができる。

PaXプロジェクトは2000年の[10月1日](../Page/10月1日.md "wikilink")に開始された。これは後に2.6にポートされ、この記事を記載している時点では開発中である。

2004年5月現在ではLinuxカーネルはPaXを組み込んでリリースされていない。パッチは手動で統合する必要がある。

  - ハードウェアでサポートしているプロセッサ: Alpha、AMD64、IA-64、[MIPS](../Page/MIPSアーキテクチャ.md "wikilink")（32ビット及び64ビット）、PA-RISC、PowerPC、SPARC
  - エミュレーション: IA-32 (x86)
  - その他のサポート: PowerPC（32ビット及び64ビット）、SPARC（32ビット及び64ビット）
  - 標準で搭載されているか: Adamantix, Hardened Gentoo
  - リリース日: 2000年10月1日

### Solaris

[Solaris](../Page/Solaris.md "wikilink") 10がNXビットをサポートしているプロセッサで起動した時、自動的に保護は有効となる。プログラムのスタックセグメントの過去の32ビット[ABIの取り扱いは例外となる](../Page/Application_Binary_Interface.md "wikilink")。ほとんどのプログラムは変更なしに動作する。しかし既存のアプリケーションの起動時にSIGSEGVが発生する場合には、eeprom (1M) を使用してenforce-prot-execをoffにし再起動することによりNX機能を無効化することができる。バグはアプリケーションに対して報告することができるから、適切にPROT_EXECを使用するために更新することができる。詳細はeeprom(1M)のマニュアルページ及びmmap(2)マニュアルページのPROT_EXECを参照すること。

### Windows

[Windows XP](../Page/Microsoft_Windows_XP.md "wikilink") Service Pack 2と[Windows Server 2003](../Page/Microsoft_Windows_Server_2003.md "wikilink") Service Pack 1から、x86アーキテクチャでは初めてNX機能が実装された。

Windowsでは重要なWindowsのサービスのみにNXによる保護が使用される。Windows XPもしくはServer 2003では、この機能は**[データ実行防止](../Page/データ実行防止.md "wikilink")** (DEP) と呼ばれ、「マイ コンピュータ」の「詳細設定」より設定できる。もしx86プロセッサがハードウェアでこの機能をサポートしている場合、NX機能はWindows XP/Server 2003ではデフォルトで有効となる。機能がサポートされていない場合には、保護は提供されない。

「ソフトウェアDEP」はNXビットに関係なく、[マイクロソフト](../Page/マイクロソフト.md "wikilink")が「安全な例外ハンドラ」に付けた名称である。「ソフトウェアDEP」や「安全な例外ハンドラ」は、アプリケーションの[ファンクションテーブル](https://ja.wikipedia.org/wiki/ファンクションテーブル "wikilink")に例外が登録されていることを確認し、プログラムがそのように設計されていることを要求するものである。これは、DEPがNXフォールトを扱う方法により悪用可能な弱点を対策するものである。他の対策法がそのままプログラムを終了するのに対し、DEPは例外を発生させる。プログラムの流れは復旧不可能に破壊されているため、プログラムが攻撃から回復できるものではない。

他のほとんどの保護手法とは異なり、DEPは[ASLR](https://ja.wikipedia.org/wiki/アドレス空間配置のランダム化 "wikilink")（アドレス空間レイアウト無作為化）を提供しない。これは[return-to-libc攻撃](https://ja.wikipedia.org/wiki/return-to-libc攻撃 "wikilink")を許し、攻撃中にDEPを無効化するのに使用される可能性がある。Windowsでこれが実行可能であることは未だ証明されていないが、PaXの文書はなぜASLRが必要かを詳述している。もし破損した画像や[MP3](../Page/MP3.md "wikilink")などの用意されたデータのアドレスが、攻撃者によって知られている場合には攻撃を成功させる可能性がある。ASLRは[Windows Vistaから提供された](https://ja.wikipedia.org/wiki/Microsoft_Windows_Vista "wikilink")。

x86以外では、インテルのIA-64で動作するWindows向けNXのバージョンが存在する。

  - ハードウェアでサポートしているプロセッサ: AMD64、IA-64、[Efficeon](https://ja.wikipedia.org/wiki/Crusoe#Efficeon "wikilink")、Intel 64、[Pentium M](../Page/Pentium_M.md "wikilink")（後期リビジョン）、[Sempron](../Page/Sempron.md "wikilink")（後期リビジョン）
  - エミュレーション: なし
  - その他のサポート: なし
  - 標準で搭載されているか: Windows XP Service Pack 2, Windows Server 2003 Service Pack 1, Windows Vista
  - リリース日: 2004年[8月6日](../Page/8月6日.md "wikilink")

## 同等技術間の機能的比較

ここでは、NX技術の機能を比較対照する。

一般的に、NXビットのエミュレーションはx86CPUでのみ可能である。別に述べない限りこのセクションでのエミュレーションへの言及はx86CPUのみを対象としている。

あるNXビットエミュレーションの方法は大変低い[オーバーヘッド](https://ja.wikipedia.org/wiki/オーバーヘッド "wikilink")を持っていることが証明されているが、そのような方法は不正確であるとも証明されている。一方、他のあるエミュレーション方法は大変高いオーバーヘッドを持っているかもしれないが、おそらく絶対に正確である。処理能力、正確性、仮想メモリ空間の代償なしにオーバーヘッドを減らす方法は現在では開発されていない。

### オーバーヘッド

オーバーヘッドはそれぞれの技術が機能するために必要な追加のCPU処理能力の事である。これはこのような技術をエミュレートもしくはNXビットを提供する事は通常測定可能なほどのオーバーヘッドを生じるために重要である。全てのNX技術はあらゆる領域のメモリのためにNXビットの状態を制御するために追加のプログラミングロジックのためにオーバーヘッドを作り出す。しかし、ハードウェアNXビットが存在すれば演算は通常CPU自身で行われ、オーバーヘッドは生じない。

ハードウェアNXビットを提供するCPUでは、特に明記する場合を除いてはリストされている全てのNX技術においてオーバーヘッドを生じない。

## 脚注

### 注釈

### 出典

[Category:CPU](https://ja.wikipedia.org/wiki/Category:CPU "wikilink") [Category:コンピュータセキュリティ](https://ja.wikipedia.org/wiki/Category:コンピュータセキュリティ "wikilink")

1.  ある場所のメモリを書き込み可能かつ実行可能の状態に置かず、書き込みのみか実行のみかどちらか一方だけにに制限すること。
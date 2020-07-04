> この記事は[UNIX](https://ja.wikipedia.org/wiki/UNIX)から翻訳されています。


**UNIX** （ユニックス、**Unix**、\[1\]）は、[コンピュータ](../Page/コンピュータ.md "wikilink")用の[マルチタスク](../Page/マルチタスク.md "wikilink")・[マルチユーザー](https://ja.wikipedia.org/wiki/マルチユーザー "wikilink")の[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink")の一種である。公式な[商標](../Page/商標.md "wikilink")は「UNIX」だが、商標以外の意味として「Unix」、または[スモールキャピタル](../Page/スモールキャピタル.md "wikilink")を使用して「<span style="font-variant: small-caps;">Unix</span>」などとも書かれる。Unixは[1969年](https://ja.wikipedia.org/wiki/1969年 "wikilink")、[AT\&T](../Page/AT&T.md "wikilink")の[ベル研究所](../Page/ベル研究所.md "wikilink")にて、[ケン・トンプソン](../Page/ケン・トンプソン.md "wikilink")、[デニス・リッチー](../Page/デニス・リッチー.md "wikilink")らが開発を開始した。

当初は[アセンブリ言語](../Page/アセンブリ言語.md "wikilink")のみで開発されたが、1973年にほぼ全体を[C言語](../Page/C言語.md "wikilink")で書き直した。このため、Unixは歴史上、初めて**[高水準言語](../Page/高水準言語.md "wikilink")で書かれたOS**であると言われることがある。\[2\]。

1973年の段階では[PDP-11](../Page/PDP-11.md "wikilink")に依存したコードが多く、移植性は低かったが、その後徐々にPDP-11に依存したコードを減少させ、1978年に[Interdata 8/32への移植に成功して以降](https://ja.wikipedia.org/wiki/Interdata_8/32 "wikilink")、徐々に他のプラットフォームにも移植されていった。

現在では「Unix」という語は、Unix標準に準拠するあらゆるオペレーティングシステムの総称でもある。現在ではUnixシステムは多数の系統に分かれており、AT\&Tの開発停止後も、多数の商用ベンダーや[非営利組織などによって](../Page/非営利団体.md "wikilink")[開発が続けられている](../Page/ソフトウェア開発.md "wikilink")。

[1970年代](../Page/1970年代.md "wikilink")から[1980年代](../Page/1980年代.md "wikilink")の初期にかけて、Unixは大学や研究所などの教育機関で広範囲に採用され、特に[カリフォルニア大学バークレー校](../Page/カリフォルニア大学バークレー校.md "wikilink")をオリジナルとする[BSD](../Page/BSD.md "wikilink")系統が誕生した。また [Version 7 Unix](../Page/Version_7_Unix.md "wikilink") や [UNIX System V](../Page/UNIX_System_V.md "wikilink") の特徴を持つオペレーティングシステムは「伝統的なUNIX」(traditional Unix)とも呼ばれる。

[2007年](../Page/2007年.md "wikilink")に、「UNIX」の商標の所有者である[標準化団体](../Page/標準化団体.md "wikilink")の[The Open Groupは](../Page/The_Open_Group.md "wikilink")、[Single UNIX Specificationを完全に満たすと認証を受けたシステムのみが](../Page/Single_UNIX_Specification.md "wikilink")「UNIX」の商標を得られるとした。このためそれ以外のシステムは（ずっと以前から、AT\&T版およびBSD以外を指して使われていた用語だが）「Unixシステムライク」または「**[Unixライク（Unix系）](../Page/Unix系.md "wikilink")**」と呼ばれるようになった。ただし The Open Groupはその呼称を気に入っていない\[3\]。

現在では多く使われているUnixとしては[macOS](https://ja.wikipedia.org/wiki/macOS "wikilink")、[AIX](../Page/AIX.md "wikilink")、[HP-UX](../Page/HP-UX.md "wikilink")、[Solaris](../Page/Solaris.md "wikilink")などがある（いずれも商用）。また認証を受けていない[Unix系](../Page/Unix系.md "wikilink")としては[Linux](../Page/Linux.md "wikilink")（派生OSに[Android](../Page/Android.md "wikilink")他）や[MINIX](../Page/MINIX.md "wikilink")、[BSD](../Page/BSD.md "wikilink")の派生OS（[FreeBSD](../Page/FreeBSD.md "wikilink")、[NetBSD](../Page/NetBSD.md "wikilink")、[OpenBSD](../Page/OpenBSD.md "wikilink")、[DragonFly BSDなど](../Page/DragonFly_BSD.md "wikilink")）がある\[4\]。

## 概説

[Unix-history.svg](https://ja.wikipedia.org/wiki/File:Unix-history.svg "fig:Unix-history.svg") Unixオペレーティングシステムは、[サーバ](../Page/サーバ.md "wikilink")や[ワークステーション](../Page/ワークステーション.md "wikilink")だけでなく、[携帯機器](../Page/携帯機器.md "wikilink")でも広く使われている\[5\]。またUnix環境と[クライアントサーバモデル](../Page/クライアントサーバモデル.md "wikilink")は、個々のコンピュータによるコンピュータ処理を、[コンピュータネットワーク](../Page/コンピュータネットワーク.md "wikilink")で連係されたコンピュータ処理に変革し、[インターネット](../Page/インターネット.md "wikilink")構築の重要な要素ともなった。

もともとUnixはベル研究所内部の開発プロジェクトであった。1973年のOSに関するシンポジウム以降、このOSはベル研究所外部にも知られるようになる。特に1980年代には、教育機関等でUnixが広がり、ユーザーが自前のツールをその上で作り、それを同僚などと共有する形が定着した\[6\]。

Unixは当初は、MulticsのようなマルチタスクOSではなく、一度に一つのプログラムしか動かせないシングルタスクOSであった。当初はパイプの概念もなかった。その後の発展の中で、徐々に「パイプ」「マルチタスク」などが実装されていった。また、Unixは当初は移植性は低かったが、徐々に特定のプラットフォームへの依存性を減少させ、1978年には、PDP-11以外のプラットフォームで動作するようになった。その後移植が徐々に進み、Unixが動作するプラットフォームが増えていった。

Multicsで用いられていたコンピュータであるGE-645は約2MBのメモリを有していたが、最初にUnixが動作したコンピュータである[PDP-7](../Page/PDP-7.md "wikilink")は約16KBのメモリしか有していなかった。このため、Unixの実装にあたっては、メモリ上に載せられる機能は制限され、当初Multicsで予定されていた多くの機能を諦めざるをえなかった。また、メモリ上でUnixの[カーネル](../Page/カーネル.md "wikilink")が占める領域を除くと、各種の[ユーティリティやアプリケーションが使えるメモリは数KBしか残っていなかった](../Page/ユーティリティソフトウェア.md "wikilink")\[7\]。このため、高機能でサイスの大きいアプリケーションを動かすことは不可能であり、単機能で小さいアプリケーションを作成し、それらを順につないでいく方法をとらざるをえなかった。 このような、簡単なプログラムを[コマンドラインインタプリタ](../Page/コマンドラインインタプリタ.md "wikilink")の[パイプ等を使ってつないでいくという方法は](../Page/パイプ_\(コンピュータ\).md "wikilink")、単一の多機能プログラムで同等機能を実装するのとは逆の発想である。これらのコンセプトは[UNIX哲学](../Page/UNIX哲学.md "wikilink")という言葉で表現されることがある。しかしながら、Unixの開発者であるトンプソンやリッチーは、Unixの開発にあたって何らかの「哲学」や「開発理念」があったとは語っていない。むしろ、理念が先にあったのではなく、メモリ制約等の現実的問題があり、それに適合するために、そのような方法にならざるをえなかったという側面が強い。 また、商用Unixの中には、単一で多機能なアプリケーションも見られ、"Unix哲学"が一貫してUnixに関するすべての関係者で共有・実現されていたわけでもない。

その後、メモリの低価格化・大容量化によって、Unixは多くの機能を実現することが可能となった。今日のUnixは[移植性](../Page/移植性.md "wikilink")、[マルチタスク](../Page/マルチタスク.md "wikilink")、[タイムシェアリング方式による](../Page/タイムシェアリングシステム.md "wikilink")[マルチユーザ](https://ja.wikipedia.org/wiki/マルチユーザ "wikilink")などを重視して設計されている。Unixでは、「オペレーティングシステム」は主となる制御プログラムであるカーネルと、多数のユーティリティより構成される。カーネルは、プログラムの開始や停止、[ファイルシステム](../Page/ファイルシステム.md "wikilink")の取り扱い、他の多くのプログラムが共用する共通的な「低レベル」のタスク、そして重要な[スケジューリング](../Page/スケジューリング.md "wikilink")などのサービスを提供する。これらのアクセスを調停するために、カーネルはシステムへの特権を持ち、システムは「ユーザー領域」と「カーネル領域」に分けられる。

カーネルの肥大化の潮流を逆転させ、より少ないユーティリティで最大のタスクを実行できるシステムに戻る目的で、[マイクロカーネル](https://ja.wikipedia.org/wiki/マイクロカーネル "wikilink")のコンセプトが登場した。またコンピュータが1つの[ハードディスクと入出力用の](https://ja.wikipedia.org/wiki/ハードディスクドライブ "wikilink")[端末](../Page/端末.md "wikilink")から構成されていた時代には、Unixのファイルモデル（ストリーミングデータ）は最適な入出力として働いた。しかし現代のシステムではネットワークや新しい装置が求められ、[グラフィカルユーザインタフェース](https://ja.wikipedia.org/wiki/グラフィカルユーザインタフェース "wikilink")が開発され、ファイルモデルは[マウスなどが発生させる非同期イベントの取り扱いのタスクには不適当と判明し](../Page/マウス_\(コンピュータ\).md "wikilink")、[1980年代](../Page/1980年代.md "wikilink")には[非同期入出力や](https://ja.wikipedia.org/wiki/非同期IO "wikilink")[IPCのメカニズムに加えて](../Page/プロセス間通信.md "wikilink")、[ソケット](../Page/ソケット_\(BSD\).md "wikilink")、[共有メモリ](../Page/共有メモリ.md "wikilink")、[メッセージキュー](../Page/メッセージキュー.md "wikilink")、[セマフォ](../Page/セマフォ.md "wikilink")などが追加された。また[通信プロトコル](../Page/通信プロトコル.md "wikilink")などの機能はカーネルの外に移動した。

Unixは現在では、[サーバ](../Page/サーバ.md "wikilink")ーや[パーソナルコンピュータ](../Page/パーソナルコンピュータ.md "wikilink")の一部に加え、[携帯電話](../Page/携帯電話.md "wikilink")などの[組み込みシステム](../Page/組み込みシステム.md "wikilink")から、[メインフレーム](../Page/メインフレーム.md "wikilink")や[スーパーコンピュータ](../Page/スーパーコンピュータ.md "wikilink")などの一部にも使われている。

## 歴史

[Ken_Thompson_(sitting)_and_Dennis_Ritchie_at_PDP-11_(2876612463).jpg](https://ja.wikipedia.org/wiki/File:Ken_Thompson_\(sitting\)_and_Dennis_Ritchie_at_PDP-11_\(2876612463\).jpg "fig:Ken_Thompson_(sitting)_and_Dennis_Ritchie_at_PDP-11_(2876612463).jpg")で作業している[ケン・トンプソン](../Page/ケン・トンプソン.md "wikilink") (座っている人物)と[デニス・リッチー](../Page/デニス・リッチー.md "wikilink")\]\]

Unixの歴史は、1960年代中ごろに、[マサチューセッツ工科大学](../Page/マサチューセッツ工科大学.md "wikilink")(MIT)、[ベル研究所](../Page/ベル研究所.md "wikilink")、[General Electric](https://ja.wikipedia.org/wiki/General_Electric "wikilink")(GE)がGEの[メインフレーム](../Page/メインフレーム.md "wikilink")コンピュータ[GE-645用に](../Page/GE-600シリーズ.md "wikilink")[Multics](../Page/Multics.md "wikilink")と呼ばれる[タイムシェアリング](https://ja.wikipedia.org/wiki/タイムシェアリング "wikilink")オペレーティングシステムを共同開発していたことにさかのぼる\[8\]。 Multicsは多くの[革新的技術を導入したが](https://ja.wikipedia.org/wiki/Multics#Nove "wikilink")、同時に、多くの問題を抱えてもいた。 Multics の目指すものに賛同しても、巨大で複雑なものになっていくことに嫌気がさしたベル研究所は、プロジェクトから徐々に距離をおくようになった。

最後までMulticsに関与して いた[ケン・トンプソン](../Page/ケン・トンプソン.md "wikilink")等はファイルシステムを担当していたが、設計が行われただけで実装されていない段階であった。トンプソン等は、実際にファイルシステムを実装してみたいと考えた。この作業は、当時ベル研究所内に使われない状態でおいてあった[PDP-7](../Page/PDP-7.md "wikilink")を借りて行われた。ファイルシステムが完成すると、それを活用するためのユーティリティを作成していった。こうして、おおむねOSの機能を有するものができあがった\[9\]。 この時点では、OSの開発はベル研究所に認知されたものではなく、彼らの私的な活動であった。研究所からの資金提供はなく、OSには名前も付けられていなかった。

できあがったOSは、MulticsのようなマルチタスクOSではなく、後の[MS-DOS](../Page/MS-DOS.md "wikilink")のような、一度に一つのプログラムしか動かせないシングルタスクのOSであった\[10\]。この特徴から、新しいOSは、[ブライアン・カーニハン](../Page/ブライアン・カーニハン.md "wikilink")によって、MulticsのMulti(多数の)をUni(単一の)に変えてUnicsと名付けられた\[11\]\[12\]\[13\]\[14\] 。後につづりがUnixと変更された。このつづりの変更の経緯について、カーニハンは「思い出せない」と言っているが、当時の開発グループ内では比較的年長者であったピーター・ノイマンは「法務上の理由であろう」と語っている\[15\]。

PDP-7は古いマシンであり問題が多かった。このため、開発グループでは、当時の最新機種であった[PDP-11](../Page/PDP-11.md "wikilink")を購入し、その上でUnixが動作するようになった。 1971年のUnixバージョン1はPDP-11/20上で動作した。 バージョン3までのUnixは[アセンブリ言語](../Page/アセンブリ言語.md "wikilink")で開発された。1973年に公開されたバージョン4において、Unixは[C言語](../Page/C言語.md "wikilink")で書き直された\[16\]。 この時点でのUnixはPDP-11に依存したコードが多く含まれており、移植性は低かった。UnixがPDP-11以外のコンピュータに移植されるまでには5年間を要し、 1978年に、[Interdata 8/32上で動作するようになった](https://ja.wikipedia.org/wiki/Interdata_8/32 "wikilink")\[17\]。

ベル研究所ではその後もUnixの改良が続けられ、パイプやマルチタスクなどの機能が追加されていった。これらの、ベル研究所で開発された初期のUnixは、現在では[Research Unixと呼ばれている](../Page/Research_Unix.md "wikilink")。

1970年代末から1980年代初頭にかけて、Unixは学術分野だけではなく産業分野でも使われるようになっていき、[HP-UX](../Page/HP-UX.md "wikilink"), [Solaris](../Page/Solaris.md "wikilink"), [AIX](../Page/AIX.md "wikilink"), [Xenix](https://ja.wikipedia.org/wiki/Xenix "wikilink")等のOSが作られた。 1980年代の末には、[AT\&T Unixシステムズ・ラボラトリーズと](https://ja.wikipedia.org/wiki/UNIX_Systems_Laboratories "wikilink")[サン・マイクロシステムズ](../Page/サン・マイクロシステムズ.md "wikilink")が共同で[UNIX System V Release 4](https://ja.wikipedia.org/wiki/Unix_System_V "wikilink") (SVR4)を開発した。これは、後の多くの商用Unixの母体となった。

1990年代には、[BSD](../Page/BSD.md "wikilink")や[Linux](../Page/Linux.md "wikilink")といったUnixあるいはUnix系OSが、コンピュータ・ネットワークを通じて世界中の開発者の協力を得て開発され、人気を得ることになった。 2000年には、アップル社がUnixに基づいて[Darwinというコアに基づくMac](../Page/Darwin_\(オペレーティングシステム\).md "wikilink") OS Xを開発した \[18\]。

今日、Unixは[サーバ](../Page/サーバ.md "wikilink")ー、[ワークステーション](../Page/ワークステーション.md "wikilink")、[モバイル機器](https://ja.wikipedia.org/wiki/モバイル機器 "wikilink")などで広く使われている\[19\]。

## 標準化

1980年代後半から始まったオペレーティングシステム標準化の動きは[POSIX](../Page/POSIX.md "wikilink")となって結実し、あらゆるオペレーティングシステムの共通のベースラインとなっている。[IEEE](../Page/IEEE.md "wikilink")は主要なUnixシステムに共通する構造からPOSIXを作り、1988年に最初のPOSIX標準を公表した。1990年代初め、よく似た標準化が業界団体[Common Open Software Environment](../Page/Common_Open_Software_Environment.md "wikilink") (COSE) イニシアティブによって開始され、[The Open Groupの管理する](../Page/The_Open_Group.md "wikilink")[Single UNIX Specificationとなった](../Page/Single_UNIX_Specification.md "wikilink")。1998年、POSIXとSingle UNIX Specificationの共通定義を提供するため、IEEEとThe Open Groupは[Austin Groupを立ち上げた](https://ja.wikipedia.org/wiki/:en:Austin_Group "wikilink")。

1999年、互換性を達成するため、いくつかのUnixシステムベンダーはSVR4の[Executable and Linkable Format](../Page/Executable_and_Linkable_Format.md "wikilink") (ELF) を[オブジェクトファイル](../Page/オブジェクトファイル.md "wikilink")および[実行ファイル](../Page/実行ファイル.md "wikilink")の標準規格とすることに合意した。これによって、同一CPUアーキテクチャでの各種Unixシステムでバイナリ互換性の大部分が確保されることになった。

Unix系オペレーティングシステム（特に[Linux](../Page/Linux.md "wikilink")）におけるディレクトリ構成の標準としては[Filesystem Hierarchy Standardがある](https://ja.wikipedia.org/wiki/Filesystem_Hierarchy_Standard "wikilink")。

## コンポーネント

Unixシステムは複数のコンポーネントから成っている。[カーネル](../Page/カーネル.md "wikilink")に加えて、開発環境、ライブラリ群、文書、ソースコードなどが含まれる。Unixは自己完結的ソフトウェアシステムだった。そのため重要な学習ツールとして頭角を現し、幅広い影響を及ぼすことになった。

各種コンポーネントを含めても初期のシステムは大きくはなかった。V7 UNIXの場合、全バイナリと全ソースにマニュアルなどの文書を含めても10MB以下であり、9トラックの[磁気テープ](../Page/磁気テープ.md "wikilink")一本で事足りた。文書を印刷したものも2巻にまとまっていた。

Unixコンポーネントの名前やファイルシステム上の位置は歴史と共に変化している。それでもV7の実装は多くの場合初期の正規な構造と見なされている。

  - **カーネル** – /usr/sys配下にソースコードがあり、以下のようなサブコンポーネントから成る。
      - *conf* – ブート用コードを含む、コンフィギュレーションとマシン依存の部分
      - *dev* – ハードウェア（及び擬似ハードウェア）の制御用[デバイスドライバ](../Page/デバイスドライバ.md "wikilink")群
      - *sys* – カーネル本体。[メモリ管理](../Page/メモリ管理.md "wikilink")、[スケジューリング](../Page/スケジューリング.md "wikilink")、[システムコール](../Page/システムコール.md "wikilink")など。
      - *h* – [ヘッダファイル](../Page/ヘッダファイル.md "wikilink")群。システム内のデータ構造やシステム定数を定義している。
  - **開発環境** – 初期のUnixには、ソースコードからシステム全体を作りなおせる程度の開発環境が含まれていた。
      - *cc* – [C言語](../Page/C言語.md "wikilink")コンパイラ（V3 UNIXから）
      - *as* – アセンブラ
      - *ld* – リンカ（[リンケージエディタ](../Page/リンケージエディタ.md "wikilink")）
      - *lib* – [ライブラリ](../Page/ライブラリ.md "wikilink")（/libまたは/usr/libにインストールされる）。*[libc](../Page/標準Cライブラリ.md "wikilink")*はC言語のライタイムをサポートするシステムライブラリ。他に数学ライブラリ (*libm*) などの各種用途のライブラリがある。V7 UNIX では、システムライブラリの一部として標準入出力ライブラリ*stdio*が初めて導入された。その後機能が追加されるにしたがってライブラリの数も膨大なものになっていった。
      - *[make](https://ja.wikipedia.org/wiki/make "wikilink")* – [ビルドマネージャ](https://ja.wikipedia.org/wiki/ビルド_\(ソフトウェア\) "wikilink")（[PWB/UNIX](https://ja.wikipedia.org/wiki/PWB/UNIX "wikilink")から）。
      - *include* – ソフトウェア開発用[ヘッダファイル](../Page/ヘッダファイル.md "wikilink")群。標準インタフェースとシステム定数を定義している。
      - *その他の言語* – V7 UNIXには、[FORTRAN 77コンパイラ](../Page/FORTRAN.md "wikilink")、[任意精度演算](../Page/任意精度演算.md "wikilink")言語（[bc](https://ja.wikipedia.org/wiki/bc_\(UNIX\) "wikilink")、dc）、[スクリプト言語](../Page/スクリプト言語.md "wikilink")[AWK](../Page/AWK.md "wikilink")が含まれており、その後のバージョンでさらに言語処理系が追加されていった。初期のBSDでは[Pascal](../Page/Pascal.md "wikilink")関連のツール群があり、最近のシステムでは[GNUコンパイラコレクション](../Page/GNUコンパイラコレクション.md "wikilink")がある。
      - *他のツール群* – ファイルアーカイバ ([ar](https://ja.wikipedia.org/wiki/ar_\(UNIX\) "wikilink"))、[シンボルテーブル](../Page/シンボルテーブル.md "wikilink")を表示するツール ([nm](https://ja.wikipedia.org/wiki/nm_\(UNIX\) "wikilink"))、コンパイラ開発ツール ([lex](https://ja.wikipedia.org/wiki/lex "wikilink"), [yacc](https://ja.wikipedia.org/wiki/yacc "wikilink"))、デバッグ用ツールなどがある。
  - **コマンド** – コマンドはUnixにおけるユーザープログラムの総称で、システム管理用（[cronなど](https://ja.wikipedia.org/wiki/crontab "wikilink")）、汎用ユーティリティ（[grep](https://ja.wikipedia.org/wiki/grep "wikilink")など）、テキストフォーマットや組版のパッケージといったアプリケーションに近いものなどが含まれる。
      - *[sh](../Page/Bourne_Shell.md "wikilink")* – 「[シェル](https://ja.wikipedia.org/wiki/Unixシェル "wikilink")」はプログラム可能な[コマンドラインインタプリタ](../Page/コマンドラインインタプリタ.md "wikilink")であり、ウィンドウシステムが登場する以前はUnixの主たるユーザインタフェースだった。GUIが主流となってからもよく使われている。
      - *ユーティリティ* – [cp](https://ja.wikipedia.org/wiki/cp_\(UNIX\) "wikilink")、[ls](https://ja.wikipedia.org/wiki/ls_\(UNIX\) "wikilink")、[grep](https://ja.wikipedia.org/wiki/grep "wikilink")、[find](https://ja.wikipedia.org/wiki/find "wikilink") などUnixの中心的ツール群。さらに以下のように分類される。
          - *システムユーティリティ* – 、[fsck](https://ja.wikipedia.org/wiki/fsck "wikilink") などのシステム管理ツール群
          - *ユーザーユーティリティ* – [passwd](https://ja.wikipedia.org/wiki/passwd "wikilink")、[kill](https://ja.wikipedia.org/wiki/kill "wikilink") などの環境管理ツール群
      - *文書整形* – Unixは当初から文書作成と組版のシステムとして使われてきた。[nroff](https://ja.wikipedia.org/wiki/nroff "wikilink")、[troff](https://ja.wikipedia.org/wiki/troff "wikilink")、、*、*、[pic](https://ja.wikipedia.org/wiki/Pic言語 "wikilink") といったコマンドがある。最近のUnixシステムでは、[TeX](../Page/TeX.md "wikilink")や[Ghostscript](../Page/Ghostscript.md "wikilink")のパッケージもある。
      - *グラフィックス* – *plot*サブシステムは単純なベクター描画をデバイスに依存しない形で生成し、デバイス対応のインタプリタが実際の描画を行う。現代のUnixシステムでは標準ウィンドウシステムおよび[GUIとして](https://ja.wikipedia.org/wiki/グラフィカルユーザインタフェース "wikilink")[X11を含んでいることが多く](../Page/X_Window_System.md "wikilink")、また[OpenGL](../Page/OpenGL.md "wikilink")をサポートしていることも多い。
      - *通信* – 初期のUnixシステムにはシステム間通信機能は含まれていなかったが、ユーザー間の通信機能として *mail* と *write* があった。V7 UNIX でシステム間通信のための[UUCPが導入され](../Page/Unix_to_Unix_Copy_Protocol.md "wikilink")、BSD 4.1c で[TCP/IPユーティリティが追加された](../Page/インターネット・プロトコル・スイート.md "wikilink")。
  - **文書** – Unix は付随する文書を全てオンラインの機械が読める形で含めた最初のOSである。
      - *[man](../Page/Manページ.md "wikilink")* – 各コマンド、ライブラリ関数、[システムコール](../Page/システムコール.md "wikilink")、[ヘッダファイル](../Page/ヘッダファイル.md "wikilink")などのマニュアル。
      - *doc* – 主要サブシステムについての長めの文書。C言語やtroffに関するものなどがある。

## 影響

Unixシステムは他のオペレーティングシステムに大きな影響を及ぼした。成功の要因は以下の通りである。

  - 直接的な対話
  - IBMやDECといった大きなベンダーの支配下にならなかった点
  - 当初、AT\&Tが無料で提供していた点
  - 安価なハードウェアで動作する点
  - 採用が容易で、他のマシンへの移行が容易

初期の実装では必須とされていた[アセンブリ言語](../Page/アセンブリ言語.md "wikilink")ではなく高水準言語で書かれている。先例として [Multics](../Page/Multics.md "wikilink") や [バロース B5000](../Page/バロース_B5000.md "wikilink") があるが、このアイデアを一般化したのはUnixである。

当時の他のOSに比べて大幅に単純化したファイルモデルを採用しており、あらゆるファイルを単純なバイト列として扱っている。ファイルシステムの階層にサービスやデバイス（[プリンター](https://ja.wikipedia.org/wiki/プリンター "wikilink")、[端末](../Page/端末.md "wikilink")、[ディスクドライブ](../Page/ディスクドライブ.md "wikilink")など）が含まれており、一様なインタフェースを提供しているが、単純なバイトストリームモデルに適さないハードウェア機能にアクセスする場合は、[ioctl](https://ja.wikipedia.org/wiki/ioctl "wikilink")とモードフラグなどの追加機構を必要とすることがある。なお[Plan 9ではこのモデルをさらに推し進め](../Page/Plan_9_from_Bell_Labs.md "wikilink")、追加機構を不要にしている。

Unixはまた、Multicsで導入された階層型ファイルシステムを一般化させた。当時の主要なOSでもストレージを複数のディレクトリやセクションに分割していたが、その階層レベルは固定で、1レベルということが多かった。いくつかの主要OSもMulticsにならってサブディレクトリを再帰的に追加する機能を備えるようになった。DECの[RSX-11](https://ja.wikipedia.org/wiki/RSX-11 "wikilink")Mは "group, user" 型階層を採用し、それが[VMSのディレクトリに進化した](../Page/OpenVMS.md "wikilink")。[CP/M](https://ja.wikipedia.org/wiki/CP/M "wikilink")ではボリューム単位であってディレクトリ階層がなかったが、[MS-DOS](../Page/MS-DOS.md "wikilink") 2.0 以降でサブディレクトリが利用可能となった。HPの[MPE](https://ja.wikipedia.org/wiki/MPE "wikilink")における group.account 型階層や、IBMの[SSPや](https://ja.wikipedia.org/wiki/:en:System_Support_Program "wikilink")[OS/400](https://ja.wikipedia.org/wiki/OS/400 "wikilink")のライブラリシステムもある。それらシステムがまとめられ、より広範囲なPOSIXのファイルシステム仕様となった。

Multicsはまた、[コマンドラインインタプリタ](../Page/コマンドラインインタプリタ.md "wikilink")を通常のユーザーレベルのプログラムとし追加コマンドを個別のプログラムで提供したが、Unixがその方式を一般化させた。[Unixシェル](https://ja.wikipedia.org/wiki/Unixシェル "wikilink")はコマンドの対話的使用にも[スクリプト言語](../Page/スクリプト言語.md "wikilink")としても使える（[シェルスクリプト](../Page/シェルスクリプト.md "wikilink")。IBMの[JCLのようなジョブ制御専用言語は存在しない](../Page/Job_Control_Language.md "wikilink")）。シェルもOSコマンド群もそれぞれ独立したプログラムなので、ユーザーはシェルを選べるし、自分で書くこともできる。新たなコマンドを追加してもシェルを修正する必要はない。また、Unixの独創的なコマンドライン構文により、[パイプでコマンド同士を連結して使用することが可能となった](../Page/パイプ_\(コンピュータ\).md "wikilink")。後のコマンドラインインタプリタの多くはUnixシェルに触発されている。

Unixの根本的な単純化想定は、ほぼあらゆるファイルフォーマットに[改行コード](../Page/改行コード.md "wikilink")で分割された[ASCII](../Page/ASCII.md "wikilink")テキストを採用した点である。初期のUnixにはバイナリエディタはなく、システムの設定は全てシェルスクリプトというテキストファイルで行われていた。入出力もバイト単位が基本であり、[Record-oriented filesystemとは異なる](../Page/Record-oriented_filesystem.md "wikilink")。ほとんどあらゆるものをテキストで表したことでパイプの有効性が高まり、単純で汎用的なツール群を開発するだけで、それらを連結して複雑な処理が可能となった。テキストとバイトに集中したことで、他のシステムよりもスケーラビリティと移植性が遥かに向上した。その後、テキストに基づくインタフェースは様々に応用可能と判明し、印刷言語（[PostScript](../Page/PostScript.md "wikilink")や[ODF](../Page/OpenDocument.md "wikilink")）や[インターネット・プロトコル・スイート](../Page/インターネット・プロトコル・スイート.md "wikilink")上のアプリケーション層のプロトコル（[FTP](../Page/File_Transfer_Protocol.md "wikilink")、[SMTP](../Page/Simple_Mail_Transfer_Protocol.md "wikilink")、[HTTP](../Page/Hypertext_Transfer_Protocol.md "wikilink")、[SOAP](../Page/SOAP_\(プロトコル\).md "wikilink")、[SIPなど](../Page/Session_Initiation_Protocol.md "wikilink")）に採用されている。

Unixは[正規表現](../Page/正規表現.md "wikilink")を一般化させるのにも一役買っており、今では様々な場面で正規表現が見られる。

[C言語](../Page/C言語.md "wikilink")はUnix以上に広がり、今ではシステムプログラミングやアプリケーションプログラミングで広く使われている。

初期のUnix開発者らは、[モジュール](../Page/モジュール.md "wikilink")性と再利用性の概念を[ソフトウェア工学](../Page/ソフトウェア工学.md "wikilink")に導入する重要な役目を果たし、「ソフトウェアツール」という考え方を生み出すことになった。

Unixは比較的安価なコンピュータにTCP/IPプロトコルをもたらし、それが[インターネット](../Page/インターネット.md "wikilink")の爆発的な広がりに貢献するとともに、他のプラットフォームへのTCP/IP実装の手本となった。これによりネットワークの実装における多数のセキュリティホールが明らかとなった。

当初からUnixがオンライン文書を揃え、ソースコードへのアクセスを可能にしていたことは、プログラマの期待を高めることにつながり、1983年の[フリーソフトウェア運動](../Page/フリーソフトウェア運動.md "wikilink")立ち上げに貢献した。

Unixの主要な開発者ら（およびUnix上で開発されたプログラム群）は、ソフトウェア開発の文化的規範を徐々に確立していき、その規範群がUnixのテクノロジー自体と同じくらい重要で有力なものとなっていった。それを[UNIX哲学](../Page/UNIX哲学.md "wikilink")と呼ぶ。

### フリーなUnix系OS

UNIXが商用の「閉じた」OSとなっていく中で、現在につながる[フリーソフトウェア](../Page/フリーソフトウェア.md "wikilink")/[オープンソース](../Page/オープンソース.md "wikilink")のムーブメントが勃興し、UNIX同様の操作性と機能を提供するフリーなOSが生み出された。

多くのUNIX系OSがオープンソースで開発されているが、以下に挙げるOSは、ライセンスなどの問題からUNIXとは公称しない。

#### GNU/Linux

[1983年](https://ja.wikipedia.org/wiki/1983年 "wikilink")に[リチャード・ストールマン](../Page/リチャード・ストールマン.md "wikilink")は[フリーソフトウェア財団](../Page/フリーソフトウェア財団.md "wikilink") (Free Software Foundation; FSF) を設立し、[GNU (**G**nu's **N**ot **U**nix) プロジェクトを開始した](../Page/GNUプロジェクト.md "wikilink")。このプロジェクトの目的は、再配布自由・改変自由なUNIXクローンのOSを作成することであった。このプロジェクトにより、多くのUNIXシステム上で動作するソフトウェア、例えば[Emacs](../Page/Emacs.md "wikilink")や[GCC等が作成され](../Page/GNUコンパイラコレクション.md "wikilink")、これらソフトウェアは多くのUNIXシステムで使用されるようになった。しかしながら、OSの中核をなす "[Hurd](../Page/GNU_Hurd.md "wikilink")" の完成に手間取った（Hurdは現在も開発中）。

[1991年](../Page/1991年.md "wikilink")に[リーナス・トーバルズ](../Page/リーナス・トーバルズ.md "wikilink")が[Linuxカーネル](../Page/Linuxカーネル.md "wikilink")を開発した。Linuxカーネルの特徴として、[POSIX](../Page/POSIX.md "wikilink")に準拠するように設計されたこと、GNUプロジェクトによって開発された様々なツールが動作するように作成されたこと、またライセンスに[GPLが採用されたこと等が挙げられる](../Page/GNU_General_Public_License.md "wikilink")。その結果、GNUプロジェクトの開発したソフトウェア等と共に、完全フリーのUNIXクローンとして利用されるようになった。有名な商用[ディストリビューションとしてかつて](../Page/Linuxディストリビューション.md "wikilink")[Red Hat Linuxが存在し](../Page/Red_Hat_Linux.md "wikilink")、現在では[Red Hat Enterprise Linuxや](../Page/Red_Hat_Enterprise_Linux.md "wikilink")[SUSE Linux等がある](../Page/SUSE.md "wikilink")。

なおLinuxという名称は本来カーネルのみの名称にすぎず、OSとして完成させるための他のシステムの多くはGNUプロジェクトの産物である。そのためFSF側ではOSとしての名称は「[GNU/Linux](https://ja.wikipedia.org/wiki/GNU/Linux "wikilink")」とすべきだと主張しており、この名称を採用した最も有名かつ完全に[フリーなディストリビューションのひとつとして](../Page/フリーソフトウェア.md "wikilink")「[Debian](../Page/Debian.md "wikilink") GNU/Linux」、およびそこから派生した「[Ubuntu](../Page/Ubuntu.md "wikilink")」などがある。ただし、Ubuntuにはフリーなソフトウェアの精神と相容れない仕様が多いため、[フリーソフトウェア信奉者から批判されることも少なくない](https://ja.wikipedia.org/wiki/Ubuntu#フリーソフトウェア財団からの批判 "wikilink")。

Linuxカーネルを利用した派生OSに[Android](../Page/Android.md "wikilink")他がある。

#### オープンソース系BSD

4.3BSD Network Release 2 (Net/2) に起源を持つのが[FreeBSD](../Page/FreeBSD.md "wikilink")・[NetBSD](../Page/NetBSD.md "wikilink")・[OpenBSD](../Page/OpenBSD.md "wikilink")・[DragonFly BSD](../Page/DragonFly_BSD.md "wikilink")・[TrueOS](../Page/TrueOS.md "wikilink")のいわゆる[BSD系Unixである](../Page/BSDの子孫.md "wikilink")。FreeBSDは安定性重視、NetBSDは新機能対応と移植性に優れ、OpenBSDはセキュリティを重視し、DragonFly BSDはマルチCPU構成での高性能という特徴を有し、TrueOSはカジュアルユーザにおいて簡単に導入して使えることを目指しており、特にFreeBSDは[ウェブ・ホスティング](https://ja.wikipedia.org/wiki/ウェブ・ホスティング "wikilink")などで標準的に使用されている。

USLとの和解以降これらBSD系UNIXはライセンス問題を排除した4.4BSD-Lite2をベースに移行し、いずれもフリーなOSとなっている。

オープンソース系BSDをベースとした商用OSとしては[アップルの](../Page/アップル_\(企業\).md "wikilink")「[macOS](https://ja.wikipedia.org/wiki/macOS "wikilink")」が知られており、中核部分を「[Darwin](../Page/Darwin_\(オペレーティングシステム\).md "wikilink")」としてソース公開している。

### 2038年問題

Unixでは、[システム時刻](https://ja.wikipedia.org/wiki/システム時刻 "wikilink")の値を1970年1月1日の午前0時0分0秒からの秒数で表しており、これを[UNIX時間](https://ja.wikipedia.org/wiki/UNIX時間 "wikilink")と呼ぶ。この値のデータ型は `time_t` で、歴史的に「符号つき long」と定義されている。[32ビット](../Page/32ビット.md "wikilink")のシステムでは、2038年1月19日にこの値が1個の0に31個の1が続く最大値 (`0x7FFFFFFF`) となり、1秒後には1個の1と31個の0が続く値 (`0x80000000`) となる。するとシステム時刻は、実装によって（符号ビットを無視するか否かによって）1901年または1970年にリセットされる。

1970年より前の時刻を[UNIX時間](https://ja.wikipedia.org/wiki/UNIX時間 "wikilink")で表すことは滅多にないため、`time_t` を符号なし32ビット整数と定義し直すという対策が考えられる。しかし、それでは単に問題を2106年2月7日に遅延させるだけであり、時刻の差を計算するソフトウェアでバグを生じる可能性がある。

この問題に対処しているバージョンもある。例えば、SolarisやLinuxの64ビット版では、`time_t` は64ビットとなっており、OS自身も64ビットのアプリケーション群も約2920億年間正しく動作する。64ビット版Solarisで既存の32ビットアプリケーションを動作させることもできるが、その場合は問題が残ったままである。一部ベンダーは標準の `time_t` はそのままにして、64ビットの代替データ型とそれを使用する[APIを別途用意している](../Page/アプリケーションプログラミングインタフェース.md "wikilink")。[NetBSD](../Page/NetBSD.md "wikilink")では、次のメジャーバージョンである 6.x で32ビット版でも `time_t` を64ビットに拡張することを決定した。従来の32ビットの `time_t` を使用しているアプリケーションは、バイナリ互換性レイヤーを作って対応する。

### ARPANET

1975年5月、[DARPAは](../Page/国防高等研究計画局.md "wikilink")、[ARPANET](../Page/ARPANET.md "wikilink")で使用するOSとしてなぜUnixが選ばれたのかを詳細に説明するRFC 681を文書化している。評価過程も文書化されている。当時のUnixのライセンス料は教育機関以外には2万ドル、教育機関には150ドルとなっていた。ARPAネットワーク全体でライセンス供与を受けるという提案に対して、ベル研究所はそういった示唆についてオープンだったと記されている。

その中で特に長所とされたのは、以下の点である。

  - ローカルな処理ファシリティ
  - [コンパイラ](../Page/コンパイラ.md "wikilink")
  - [テキストエディタ](../Page/テキストエディタ.md "wikilink")
  - [roff](https://ja.wikipedia.org/wiki/roff "wikilink")
  - 効率的なファイルシステムとアクセス制御
  - パーティションのマウント機能
  - [デバイスファイル](../Page/デバイスファイル.md "wikilink")による周辺機器の抽象化
  - [Network Control Program](../Page/Network_Control_Program.md "wikilink") (NCP) が統合されている点
  - ネットワークコネクションをスペシャルファイルとして扱え、標準的なI/O用[システムコール](../Page/システムコール.md "wikilink")でアクセスできる点
  - プログラム終了時に、オープンしていたファイルが全て自動的にクローズされる点

## ブランディング

1993年10月、Unix System Vのソースについての権利を保有していた[ノベルは](../Page/ノベル_\(企業\).md "wikilink")、登録[商標](../Page/商標.md "wikilink")の権利を[X/Open](https://ja.wikipedia.org/wiki/X/Open "wikilink")（現在の[The Open Group](../Page/The_Open_Group.md "wikilink")）に移管し\[20\]、1995年にはUNIX関連事業を[SCO](../Page/SCO.md "wikilink")に売却した\[21\]。ノベルが実際のソフトウェアの[著作権](../Page/著作権.md "wikilink")もSCOに売却したのかについては2006年に裁判となり、最終的にノベルが勝利した。SCO側は控訴したが、2011年8月30日に裁判所が棄却したため、裁判は終結した\[22\]。

アメリカなどで、登録商標としてのUNIXは[The Open Group](../Page/The_Open_Group.md "wikilink") が保有している。現在、日本における「UNIX」という商標は複数の区分で登録されており、電子計算機関連において[アメリカン テレフォン アンド テレグラム カムパニーやエックス](../Page/AT&T.md "wikilink")/オープン・カンパニー・リミテッドの登録もある。

日本では、[日本マランツ](../Page/日本マランツ.md "wikilink")（現在は合併して[ディーアンドエムホールディングス](../Page/ディーアンドエムホールディングス.md "wikilink")）が、電気機器分野でUNIXという名前で先行して商標登録を行なっていたため、UNIXという商標の権利関係がはっきりしていなかったことがあった。このことから、書籍などでの商品名などの登録商標についての断り書き一覧などで「UNIXオペレーティングシステムは,AT\&Tのベル研究所が開発し,AT\&Tがライセンスしています.」（『Life with UNIX』邦訳版での例）などのように書かれたことがあった。現在も日本マランツは音響機器用に「unix」を使用している。他の国でも同様に分野を限定して同じ商標を別の意味で登録することができ、本棚、インクペン、瓶詰めの膠（にかわ）、おむつ、ヘアドライヤー、食品コンテナなどで登録された例がある\[23\]。

[Single UNIX Specificationに完全に準拠しているとThe](../Page/Single_UNIX_Specification.md "wikilink") Open Groupに認められたシステムだけが*UNIX*を名乗ることができる。そのため認証を受けていないシステムは「[Unix系](../Page/Unix系.md "wikilink")」と呼ばれる。

The Open Groupは "UNIX" を特定のOS実装ではなく、OSのクラスを指すものと定義している。すなわち、Single UNIX Specificationに準拠しているとThe Open Groupに認められたシステムのみが[UNIX 98や](../Page/Single_UNIX_Specification.md "wikilink")[UNIX 03といった登録商標を付けることを許されており](../Page/Single_UNIX_Specification.md "wikilink")、そのためにベンダーは認証料と毎年のロイヤルティを支払わなければならない\[24\]。認証を受けたOSとしては、[AIX](../Page/AIX.md "wikilink")、[HP-UX](../Page/HP-UX.md "wikilink")、[IRIX](../Page/IRIX.md "wikilink")、[Solaris](../Page/Solaris.md "wikilink")、[Tru64](../Page/Tru64_UNIX.md "wikilink")（かつての "Digital UNIX"）、[A/UX](https://ja.wikipedia.org/wiki/A/UX "wikilink")、[macOS](https://ja.wikipedia.org/wiki/macOS "wikilink")\[25\]\[26\]、[z/OS](https://ja.wikipedia.org/wiki/z/OS "wikilink")の一部などがある。

認証を受けていないシステムを表すため、（また、[ジャーゴンファイル](../Page/ジャーゴンファイル.md "wikilink")のUN\*Xの項目によれば、商標であることを標示するための「<sup>TM</sup>」を避けるために）、「UN\*X」のように[グロブ](https://ja.wikipedia.org/wiki/グロブ "wikilink")記法を使って表記されることがある。ジャーゴンファイルの記述によれば、法的にはUNIXと書いても<sup>TM</sup>を付けることは強制されないのだが、この記法は広く使われてしまっている（ジャーゴンファイル訳本の『ハッカーズ大辞典』初版にある「逆にアスタリスクを使うと権利侵害になるらしい」という記述は誤訳なので注意）。

The Open Groupは[商標の普通名称化](../Page/商標の普通名称化.md "wikilink")を防ぐため、*UNIX* という語には常に「システム」などの語をつけて使って欲しいとしている。

本来の形は "Unix" なのだが、<span style="font-variant: small-caps;">Unix</span> という形もよく使われている。これについて[デニス・リッチー](../Page/デニス・リッチー.md "wikilink")は、[Association for Computing Machinery](../Page/Association_for_Computing_Machinery.md "wikilink") (ACM) の開催した第3回OSシンポジウムにUnixの論文を送る際「[troffと新たな組版システムを開発したばかりでスモールキャピタルを印字できることに興奮して](https://ja.wikipedia.org/wiki/roff "wikilink")、それを使ってしまったため」だとしている\[27\]。当時の多くのOSは大文字のみで名称を記述するのが一般的だったため、多くの人は習慣的に大文字のみで "UNIX" と記述した。

UnixやUnix系の複数のブランドを総称するため、Unixの複数形が時折使われることがある。最も一般的な複数形は *Unixes* だが、Unixを[ラテン語](../Page/ラテン語.md "wikilink")の名詞の第3格変化として扱い複数形を *Unices* する例もよく見られる。[古英語](../Page/古英語.md "wikilink")的に *Unixen* とする例はまれだが、ときおり見かける。

## 主なUnix系OS

### フリーなもの

  - [BSD](../Page/BSD.md "wikilink")および[BSDの子孫](../Page/BSDの子孫.md "wikilink")
    現在主要なものに、[FreeBSD](../Page/FreeBSD.md "wikilink")、[NetBSD](../Page/NetBSD.md "wikilink")がある。いずれも[386BSD](../Page/386BSD.md "wikilink")から生まれた。
      - [FreeBSD](../Page/FreeBSD.md "wikilink")
        [BSDの子孫](../Page/BSDの子孫.md "wikilink")。多くの[派生版がある](../Page/FreeBSDディストリビューション.md "wikilink")（中には有償のものも含まれる）。
          - [Darwin](../Page/Darwin_\(オペレーティングシステム\).md "wikilink")
            アップルがDarwinプロジェクトによってオープンソース化したmacOSの中核。FreeBSDのソースコードをベースとし、中核には[Mach](../Page/Mach.md "wikilink")が使われている。
          - [DragonFly BSD](../Page/DragonFly_BSD.md "wikilink")
            FreeBSDから派生した[BSDの子孫](../Page/BSDの子孫.md "wikilink")。[ハイブリッドカーネル](https://ja.wikipedia.org/wiki/ハイブリッドカーネル "wikilink")を採用している。
      - [NetBSD](../Page/NetBSD.md "wikilink")
        [BSDの子孫](../Page/BSDの子孫.md "wikilink")。58以上のアーキテクチャに対応している。
          - [OpenBSD](../Page/OpenBSD.md "wikilink")
            NetBSDから派生した[BSDの子孫](../Page/BSDの子孫.md "wikilink")。
  - [GNU/Linux](https://ja.wikipedia.org/wiki/GNU/Linux "wikilink")
    [Linux](../Page/Linux.md "wikilink")カーネルから派生した、[Linuxディストリビューション](../Page/Linuxディストリビューション.md "wikilink")全般やELIKSを言う。中には有償のものも含まれる。Linux Standard Base仕様を元に設計されるため、ほぼ[POSIX](../Page/POSIX.md "wikilink")準拠となる。Linuxカーネルを利用した派生OSに[Android](../Page/Android.md "wikilink")他がある。
  - [GNU/Hurd](../Page/GNU_Hurd.md "wikilink")
    [GNU](../Page/GNU.md "wikilink")プロジェクトの公式OSとして現在開発中である。中核には[Mach](../Page/Mach.md "wikilink")が使われている。
  - [Solaris](../Page/Solaris.md "wikilink")/[OpenSolaris](../Page/OpenSolaris.md "wikilink")
    サン・マイクロシステムズのOS。現在、最新版のSolaris 11が提供されているが、以前の版も最終リリースのものがダウンロード可能である([Solaris 8](http://www.sun.com/software/solaris/8/), [Solaris 9](http://www.sun.com/software/solaris/9/))。もともとは有償版しかなかったが、[SPARC](../Page/SPARC.md "wikilink")版が無償化され、ついで[x86](https://ja.wikipedia.org/wiki/x86 "wikilink")版も（一度有償に戻ったが）無償化された。また、カーネル等の主要コンポーネントをオープンソース化した[OpenSolaris](../Page/OpenSolaris.md "wikilink")もリリースされ、そこから多くの派生ディストリビューションも生まれている。
  - [MINIX](../Page/MINIX.md "wikilink")
    [IBM PCでも動作すること目的に開発された教育用Unix系OS](../Page/IBM_PC.md "wikilink")。[80386の仮想記憶には対応していなかったため](../Page/Intel_80386.md "wikilink")、Linuxが開発されるきっかけとなった事でも有名。なお、当初はフリーではないライセンスでリリースされていたが、[2000年](../Page/2000年.md "wikilink")にバージョン 2.0.2 が [BSDライセンス](../Page/BSDライセンス.md "wikilink")のもとでリリースされ、フリーなOSとなった。
  - [Haiku](../Page/Haiku_\(オペレーティングシステム\).md "wikilink")
    [BeOS](../Page/BeOS.md "wikilink")互換のオープンソースOS。[POSIX](../Page/POSIX.md "wikilink")に準拠するよう開発されている。

### フリーではないもの

  - [AIX](../Page/AIX.md "wikilink")
    [IBM](../Page/IBM.md "wikilink")の、SVR4とBSD4.4をベースとしたUNIX。現在、最新版のAIX 7.2が提供されている。

  -
    [IBM](../Page/IBM.md "wikilink")が6100RT/PCシリーズ用に提供していた4.2BSDベースのOS。アカデミック分野の顧客にのみ提供された。AT\&T UNIXと[BSD](../Page/BSD.md "wikilink")のライセンスを持つ顧客にはソースコードも提供された。

  - [AOS](https://ja.wikipedia.org/wiki/AOS "wikilink")
    [IBM](../Page/IBM.md "wikilink")が6100RT/PCシリーズ用に4.3BSDを移植したもの。アカデミック分野の顧客にのみ提供された。AT\&T UNIXと[BSD](../Page/BSD.md "wikilink")のライセンスを持つ顧客にはソースコードも提供された。

  - [Domain/OS](https://ja.wikipedia.org/wiki/Domain/OS "wikilink")
    [アポロコンピュータ](../Page/アポロコンピュータ.md "wikilink")が開発したワークステーションに搭載されたUNIXの機能も持つ独自OS。マイクロカーネル上のOS MiddlewareとしてBSD4.3とSVR3を搭載し同時独立動作を可能とした。[ヒューレット・パッカード](../Page/ヒューレット・パッカード.md "wikilink") (HP) に買収されたその後は市場から姿を消した。

  - [Ultrix](../Page/Ultrix.md "wikilink")
    [DECが同社の](../Page/ディジタル・イクイップメント・コーポレーション.md "wikilink")[VAX](../Page/VAX.md "wikilink")やDECstation向けに出していた4.2BSD/4.3BSDベースのOS。初の[64ビット](../Page/64ビット.md "wikilink")実装を行ったUNIXとしても知られている

  - [Tru64 UNIX](../Page/Tru64_UNIX.md "wikilink")
    DECが開発した、[Alphaアーキテクチャのサーバ](https://ja.wikipedia.org/wiki/DEC_Alpha "wikilink")/ワークステーション用のOS。当初は「OSF/1」と呼ばれ「Digital UNIX」を経て Tru64 UNIX となった。DECの買収とともに、[コンパック](../Page/コンパック.md "wikilink")、[ヒューレット・パッカード](../Page/ヒューレット・パッカード.md "wikilink") (HP) へと引き継がれ、現在も販売されている。

  -
    DataGeneralのサーバ/ワークステーション用のOS製品の商標。System-V系をベースにしているが、一部BSD系の機能を付加

  - [HP-UX](../Page/HP-UX.md "wikilink")
    ヒューレット・パッカード (HP) の[PA-RISC](../Page/PA-RISC.md "wikilink")アーキテクチャによるサーバ/ワークステーション用のOS製品の商標。[OSF/1への移行を前提にSVR](https://ja.wikipedia.org/wiki/Tru64_UNIX#OSF/1 "wikilink")3系をベースに実装されたが、そのまま発展したOS。HP-UX V10以降はSVR4ベースとなる。2002年リリースのHP-UX 11i v1.6では業界で初めて[インテル](https://ja.wikipedia.org/wiki/インテル "wikilink")[Itanium](../Page/Itanium.md "wikilink")プロセッサに対応する商用OSを提供した

  - [OpenServer](https://ja.wikipedia.org/wiki/OpenServer "wikilink")
    [SCO](../Page/SCO.md "wikilink")がマイクロソフトから引き継いだ[XENIX](../Page/XENIX.md "wikilink")を発展させた[IBM PC用のUNIX](../Page/IBM_PC.md "wikilink")。一時期はPC用UNIXのトップシェアを誇っていた。

  - [OS/390](https://ja.wikipedia.org/wiki/OS/390 "wikilink"), [z/OS](https://ja.wikipedia.org/wiki/z/OS "wikilink")
    [メインフレーム](../Page/メインフレーム.md "wikilink")専用OSであるOS/390およびz/OSはPOSIX準拠OSである。通常UNIXと呼ばれないが、標準のUNIX環境(Unix System Services - USS)により、OS/390やz/OSのネイティブアプリケーションとPOSIX準拠アプリケーションを同時稼働できる。

  - [macOS](https://ja.wikipedia.org/wiki/macOS "wikilink")
    独自改良の[Mach](../Page/Mach.md "wikilink")マイクロカーネルと[FreeBSD](../Page/FreeBSD.md "wikilink")のユーザランドによって実現されたOS (Darwin) 上に[Cocoa](../Page/Cocoa.md "wikilink"), [Carbon](../Page/Carbon.md "wikilink"), [Core Foundationなどを実装した](../Page/Core_Foundation.md "wikilink")[Macintosh](../Page/Macintosh.md "wikilink")用OS。なお、2007年10月に出荷された[Mac OS X v10.5以降](../Page/Mac_OS_X_v10.5.md "wikilink")、2018年9月にリリースされた[macOS MojaveはThe](https://ja.wikipedia.org/wiki/macOS_Mojave "wikilink") Open Groupの認証を受けたUNIXである\[28\]。また、同じくDarwinを実装した派生OSに[iOSがある](https://ja.wikipedia.org/wiki/iOS_\(アップル\) "wikilink")。

  - [A/UX](https://ja.wikipedia.org/wiki/A/UX "wikilink")
    [アップルコンピュータが開発した](../Page/アップル_\(企業\).md "wikilink")、SVR2ベースの[Macintosh](../Page/Macintosh.md "wikilink")用OS。X11やコンソールのほかに、Mac OSによく似たインターフェイスのウィンドウシステムを備えていた。当時のMacintoshはMac OS以外をブートできないため、いったんSystem7が起動する。

  - [MachTen](https://ja.wikipedia.org/wiki/MachTen "wikilink")
    MachマイクロカーネルとFreeBSDをベースとした、Mac OS内で起動するOS。

  - [BeOS](../Page/BeOS.md "wikilink")
    BeのワークステーションであるBeBox、またはPower Mac、[PC/AT互換機](https://ja.wikipedia.org/wiki/PC/AT互換機 "wikilink")で動作するUNIX互換OS。メディアOSとしてマルチメディアを扱うのに長けた。マイクロカーネルにはMachを使用しているが、ユーザカーネルなどのソースコードはオリジナルUNIXは使用せず、POSIX仕様をベースに新しくフルスクラッチされた。

  - [BSD/OS](https://ja.wikipedia.org/wiki/BSD/OS "wikilink")
    初期BSDから分岐し商業プロダクトとなったUNIX。[BSDi](https://ja.wikipedia.org/wiki/BSDi "wikilink")が開発、後に組込み系でリアルタイム制御に対応したUNIX互換OS「LINX」を開発・販売していたWind Riverがソフトウェア部門ごと買収。当初の名前はBSD/386

  - [XENIX](../Page/XENIX.md "wikilink")
    [マイクロソフト](../Page/マイクロソフト.md "wikilink")がSVR2をベースに開発・販売していた[IBM PC向けUNIX](../Page/IBM_PC.md "wikilink")。仮想メモリをもたない[8086とFDで動作するシンプルなシステム](../Page/Intel_8086.md "wikilink")。教育用および安価なUNIX環境として高いインストールベースを誇った。[1983年](https://ja.wikipedia.org/wiki/1983年 "wikilink")、[SCO](../Page/SCO.md "wikilink")から販売されていたが、マイクロソフトがサーバOS戦略を独自路線（[OS/2](https://ja.wikipedia.org/wiki/OS/2 "wikilink") → Windows NT）へ切り替えたため、後にSCOへ売却された。

  - [PANIX](https://ja.wikipedia.org/wiki/PANIX "wikilink")
    エー・アイ・ソフトが、SVR4をPC/AT互換機・[PC-9800シリーズ](../Page/PC-9800シリーズ.md "wikilink")に移植して発売していたもの

  - [UnixWare](../Page/UnixWare.md "wikilink")
    USLの純正SVR4が[ノベルに売却され](../Page/ノベル_\(企業\).md "wikilink")、ノベルの技術（Netwareのサポートなど）を取り入れられたUNIX。その後SCOへ売却される。

  - [IRIX](../Page/IRIX.md "wikilink")
    [シリコン・グラフィックス](https://ja.wikipedia.org/wiki/シリコン・グラフィックス "wikilink") (SGI) のUNIX。GUIに優れる。映像製作分野でのシェアが高い。SVR4.2系

  - [NeXT](../Page/NeXT.md "wikilink")STEP/OPENSTEP
    NeXT ComputerのOS。当初は同社のワークステーション専用のOSで、Machに4.3BSD相当の機能を搭載したものであった。後にPC/AT互換機などで動作するOSとして単体販売もされた。

  -
    Marc Williams製。UNIXライクなOS。

  - [UNICOS](https://ja.wikipedia.org/wiki/UNICOS "wikilink")
    Crayのスーパーコンピュータ用のUNIX。

  - [RISC/os](https://ja.wikipedia.org/wiki/RISC/os "wikilink")
    [ミップス・コンピュータシステムズのUNIXワークステーション](../Page/ミップス・テクノロジーズ.md "wikilink")/サーバ専用のUNIX。日本ではクボタコンピュータ（株）が代理店をしていた。

  - [Σ](../Page/Σプロジェクト.md "wikilink")
    通産省主導の国策プロジェクトとして開発されたOS。開発当初はBSD系だったが後にSystem V (Release2) 系に路線変更。プロジェクト的には失敗に終わったとされ、また、その後も少なからず他の国策プロジェクトに悪影響を与えたとされる。

  - [HI-UX](../Page/HI-UX.md "wikilink")
    [日立製作所](../Page/日立製作所.md "wikilink")のワークステーション、サーバで動作する。当初は68000系ワークステーションで稼働したSystem V系独自OSであったが、後にハードウェアアーキテクチャの変更(PA-RISC)に伴い、HP-UXをベースとした製品へ変更となった。

  - [NEWS-OS](https://ja.wikipedia.org/wiki/NEWS_\(ソニー\) "wikilink")
    [ソニー](../Page/ソニー.md "wikilink")製の[NEWSワークステーション専用のUNIX](https://ja.wikipedia.org/wiki/NEWS_\(ソニー\) "wikilink")。当初は4.2BSDベースであったが、後に4.3BSDベースとなる。終末期にはSVR4.2ベースとなった(NEWS-OS6.x)。

  - [OA/UX](https://ja.wikipedia.org/wiki/OA/UX "wikilink")
    [シャープ](../Page/シャープ.md "wikilink")製のOAシリーズ、IXシリーズのオフコン/ワークステーション専用のUNIX。当初はSystemIIIベースであったが、後にSystemVベースとなる。コンソール画面での漢字表示、オンボードの辞書ROMを用いたかな漢変換など独自の日本語化が行われていた。

  - [UniOS-U/UniOS-B/UniOS-Σ](https://ja.wikipedia.org/wiki/UniOS-U/UniOS-B/UniOS-Σ "wikilink")
    [オムロン](../Page/オムロン.md "wikilink")が開発・販売していた[LUNAワークステーションのうちMC](../Page/Luna_\(ワークステーション\).md "wikilink")68030を用いたモデル専用のUNIX。SystemV系、BSD系、Σ準拠の3種類が供給された。MC88000を搭載したLUNA88k-WSのOSは[Mach](../Page/Mach.md "wikilink")マイクロカーネル（ユーザカーネルは4.xBSD）であった。

  - [EWS-UX](../Page/EWS-UX.md "wikilink")([UX/4800](https://ja.wikipedia.org/wiki/UX/4800 "wikilink"))
    [日本電気](../Page/日本電気.md "wikilink") (NEC) 製の[EWS4800](../Page/EWS4800.md "wikilink")ワークステーション専用のUNIX。SVR3系の[CISC](../Page/CISC.md "wikilink")版とSVR4（当初は、SVR4.0,後にSVR4.2、4.2MP）系の[RISC](../Page/RISC.md "wikilink")版が存在する。その後、[UP-UX](../Page/UP-UX.md "wikilink")をOSとするUP4800サーバ・シリーズが発売になり、これらが統合されて[UX/4800](https://ja.wikipedia.org/wiki/UX/4800 "wikilink")に名前が変更となった。CPUをR10000シリーズ（64ビット）としたモデルの発売に伴い、32ビット版と64ビット版が提供されている。

  - [PC/UX](https://ja.wikipedia.org/wiki/PC/UX "wikilink")
    [NEC製](../Page/日本電気.md "wikilink")[PC-9800シリーズ](../Page/PC-9800シリーズ.md "wikilink")（[80286ベースのもの](../Page/Intel_80286.md "wikilink")）専用のUNIX。SVR2ベース。

  - [SUPER-UX](../Page/SUPER-UX.md "wikilink")
    NEC製[SXスーパーコンピュータ向けのUNIX](https://ja.wikipedia.org/wiki/SXシリーズ "wikilink")。なお、[地球シミュレータ](../Page/地球シミュレータ.md "wikilink")向けには、このOSを地球シミュレータ向けに拡張したものが利用されている。

  - [SX/A](https://ja.wikipedia.org/wiki/SX/A "wikilink")
    [富士通](../Page/富士通.md "wikilink")製ワークステーションのAシリーズ（A30など）・Σ-Station（Σプロジェクトとは無関係）シリーズ専用のUNIX。純正SVR3をベースに4.2BSDのTCP/IP機能を盛り込まれていた。

  - [UXP/DS](https://ja.wikipedia.org/wiki/UXP/DS "wikilink")
    富士通[DS/90](https://ja.wikipedia.org/wiki/DS/90 "wikilink")・[GP7000D](https://ja.wikipedia.org/wiki/GP7000D "wikilink")シリーズ専用のUNIX、USL純正のSVR4をベースに開発された。

  - [UXP/M](https://ja.wikipedia.org/wiki/UXP/M "wikilink")
    富士通製汎用機（[FACOM](../Page/FACOM.md "wikilink")後継機であるMシリーズ、GS (Gloval Server) シリーズ）で動作するSVR4互換のUNIX。他の富士通汎用機のOS (MSP/VSP) と同様に、VM上で稼動する。

  - [RTU](https://ja.wikipedia.org/wiki/RTU "wikilink")

    製リアルタイムUNIX、世界で初めてUNIXをリアルタイム化したUNIX。SVR3系カーネルをベースに4.2BSDのTCP/IPを利用していた。[コンカレント・コンピュータ](https://ja.wikipedia.org/wiki/コンカレント・コンピュータ "wikilink")に買収後名前は消えるが、機能性は現在も継承されている。

  - [CX/UX](https://ja.wikipedia.org/wiki/CX/UX "wikilink")
    [ハリスコンピュータ](https://ja.wikipedia.org/wiki/ハリスコンピュータ "wikilink")製NHxxxxシリーズで動作する、SVR3系リアルタイムUNIX。SVR3系カーネルをベースに4.2BSDのTCP/IPを利用していた。[コンカレント・コンピュータ](https://ja.wikipedia.org/wiki/コンカレント・コンピュータ "wikilink")に買収後名前は消えるが、機能性は現在も継承されている。

  - [PowerMAX OS](https://ja.wikipedia.org/wiki/PowerMAX_OS "wikilink")
    [コンカレント・コンピュータ](https://ja.wikipedia.org/wiki/コンカレント・コンピュータ "wikilink")製PowerHawk、NightHawk、TurboHawkシリーズで動作する。SVR4ES/MP純正カーネル（USLのカーネルベース）に[POSIX1003.1b](https://ja.wikipedia.org/wiki/POSIX1003.1b "wikilink")（リアルタイム）、POSIX1003.1c（[POSIXスレッド](https://ja.wikipedia.org/wiki/POSIXスレッド "wikilink")）の拡張を行い、XPG4の認定も受けている。事実上、最後の商用UNIXにおけるリアルタイムUNIXである。（2011年現在、販売中）

  - [NCR UNIX](https://ja.wikipedia.org/wiki/NCR_UNIX "wikilink")
    [NCRの発売するUNIX](../Page/NCR_\(企業\).md "wikilink")。

## UNIX環境を提供するソフトウェア

OSではないが、UNIXに相当する環境を提供するソフトウェア。

  - [BSD on Windows](https://ja.wikipedia.org/wiki/BSD_on_Windows "wikilink")
  - [Cygwin](../Page/Cygwin.md "wikilink")
  - [Interix](https://ja.wikipedia.org/wiki/Interix "wikilink") ([Services for UNIX](https://ja.wikipedia.org/wiki/Services_for_UNIX "wikilink"))
  - [Windows NT系](../Page/Windows_NT系.md "wikilink")
      -
        Windows NT系はPOSIX準拠のサブシステムをもつ。[Windows 2000では](../Page/Microsoft_Windows_2000.md "wikilink")[Interix](https://ja.wikipedia.org/wiki/Interix "wikilink")サブシステムを導入することで、UNIX環境を構築することができる。[Windows XPおよび](../Page/Microsoft_Windows_XP.md "wikilink")[Windows Server 2003ではPOSIXサブシステムが](../Page/Microsoft_Windows_Server_2003.md "wikilink")[Services for UNIXとして別配布である](https://ja.wikipedia.org/wiki/Services_for_UNIX "wikilink")。Windows Server 2003 R2、[Windows Vista](https://ja.wikipedia.org/wiki/Microsoft_Windows_Vista "wikilink") (Ultimate、Enterprise) および[Windows Server 2008では](../Page/Microsoft_Windows_Server_2008.md "wikilink")、Subsystem for Unix-based Applications として、標準搭載されている。Windows 10 Anniversary Update以降は[Windows Subsystem for Linuxとして搭載されている](https://ja.wikipedia.org/wiki/Windows_Subsystem_for_Linux "wikilink")。\[29\]

## 脚注

## 参考文献

  -
  - Ritchie, D.M.; Thompson, K., *[The UNIX Time-Sharing System](http://pdos.csail.mit.edu/6.828/2004/readings/ritchie74unix.pdf)* (The Bell System Technical Journal, July–August 1978, Vol. 57, No. 6, Part 2)

  - \- Unix系オペレーティングシステムの詳細な系図、関係する人物の公式サイトや関連資料へのリンクなど

  -
  -
  - Lions, John: *Lions' [Commentary on the Sixth Edition UNIX Operating System](http://www.lemis.com/grog/Documentation/Lions/) with Source Code*, Peer-to-Peer Communications, 1996; ISBN 1-57398-013-7

<!-- end list -->

  -
## 関連文献

  - 書籍

<!-- end list -->

  - Salus, Peter H.: *A Quarter Century of UNIX*, Addison Wesley, 1 June 1994; ISBN 0-201-54777-5

<!-- end list -->

  - 映像

<!-- end list -->

  - Computer Chronicles (1985). "[UNIX](http://www.archive.org/details/UNIX1985)".
  - Computer Chronicles (1989). "[Unix](http://www.archive.org/details/unix_2)".

## 関連項目

  - [POSIX](../Page/POSIX.md "wikilink")
  - [Mach](../Page/Mach.md "wikilink")
  - [C言語](../Page/C言語.md "wikilink")
  - [UNIX時間](https://ja.wikipedia.org/wiki/UNIX時間 "wikilink")
  - [Plan 9 from Bell Labs](../Page/Plan_9_from_Bell_Labs.md "wikilink")

## 外部リンク

  - [The UNIX System](http://www.unix.org), at [The Open Group](../Page/The_Open_Group.md "wikilink").

  - [The Evolution of the Unix Time-sharing System](http://cm.bell-labs.com/cm/cs/who/dmr/hist.html)

  - [The Creation of the UNIX Operating System](http://www.bell-labs.com/history/unix/)

  - [The Unix Tree: files from historic releases](http://minnie.tuhs.org/UnixTree/)

  -
  - [The Unix 1st Edition Manuals](http://man.cat-v.org/unix-1st/).

  - [The UNIX System](http://techchannel.att.com/play-video.cfm/2012/2/22/AT&T-Archives-The-UNIX-System) - 1982年のUNIXに関する映画。デニス・リッチー、ケン・トンプソン、ブライアン・カーニハン、アルフレッド・エイホらが出演している。

  - [A History of UNIX before Berkeley: UNIX Evolution: 1975-1984](http://www.darwinsys.com/history/hist.html)

  - [Unix and Linux Forums](http://www.unix.com) - free technical support for unix and linux operating systems

[Category:UNIX](https://ja.wikipedia.org/wiki/Category:UNIX "wikilink") [Category:オペレーティングシステム](https://ja.wikipedia.org/wiki/Category:オペレーティングシステム "wikilink") [Category:アセンブリ言語](https://ja.wikipedia.org/wiki/Category:アセンブリ言語 "wikilink") [Category:1969年のソフトウェア](https://ja.wikipedia.org/wiki/Category:1969年のソフトウェア "wikilink") [Category:OSファミリ](https://ja.wikipedia.org/wiki/Category:OSファミリ "wikilink")

1.  英語の発音は「U」にアクセントを置くので、「**ユー**ニクス」に近い発音となる。『[ジャーゴンファイル](../Page/ジャーゴンファイル.md "wikilink")』でも「U」にアクセントを置いて発音するとしている（→Eric S. Raymond (ed.) (2004年10月4日). “[Unix](http://www.catb.org/%7Eesr/jargon/html/U/Unix.html)”. *The Jargon File, version 4.4.7*. 2010年12月15日閲覧）。しかし日本人のアクセントは異なることがある（「ニ」にアクセント）。
2.  実際にはMulticsを書くのにPL/I（のサブセット）が使われた、といったような先行例はある。
3.  [What is a "Unix-like" operating system?](http://www.unix.org/questions_answers/faq.html#7a) Unix.org FAQ
4.
5.
6.
7.
8.
9.
10.
11.
12.
13.
14.
15.
16.
17.
18.
19.
20.
21.
22.
23.
24.
25.
26.
27.
28. [The Open GroupのOS XへのUNIX 03製品認証](http://www.opengroup.org/openbrand/register/apple.htm)
29.
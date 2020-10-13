> この記事は[PDP-11](https://ja.wikipedia.org/wiki/PDP-11)から翻訳されています。


**PDP-11** は、[ディジタル・イクイップメント・コーポレーション](../Page/ディジタル・イクイップメント・コーポレーション.md "wikilink")(DEC)が[1970年代](../Page/1970年代.md "wikilink")から[1980年代](../Page/1980年代.md "wikilink")に販売した[16ビット](../Page/16ビット.md "wikilink")[ミニコンピュータ](../Page/ミニコンピュータ.md "wikilink")シリーズ\[1\]\[2\]。PDP-11 は DECの[PDPシリーズ](../Page/PDPシリーズ.md "wikilink")の[PDP-8](../Page/PDP-8.md "wikilink")[コンピュータ](../Page/コンピュータ.md "wikilink")の主に[リアルタイムシステム](https://ja.wikipedia.org/wiki/リアルタイムシステム "wikilink")の後継であるが、両シリーズは10年間以上並存した。革新的機能をいくつか持ち、従来よりも[プログラミングが容易になっていた](https://ja.wikipedia.org/wiki/プログラミング_\(コンピュータ\) "wikilink")。ミッドレンジのミニコンピュータとしての後継は[32ビット](../Page/32ビット.md "wikilink")の[VAX](../Page/VAX.md "wikilink")である。

その設計上の特徴は、[モトローラ](../Page/モトローラ.md "wikilink")の[MC68000](../Page/MC68000.md "wikilink")などのマイクロプロセッサの設計に影響を及ぼしている。またPDP-11上の[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink") (OS) の設計は他のOS、例えば[CP/M](https://ja.wikipedia.org/wiki/CP/M "wikilink")\[3\]や[MS-DOS](../Page/MS-DOS.md "wikilink")\[4\]の設計に影響を及ぼしている。最初の公式に[UNIX](../Page/UNIX.md "wikilink")と名付けられたバージョンのOSは、1970年に PDP-11/20 上で動作した。PDP-11のプログラミング上の低レベルな特徴と[C言語](../Page/C言語.md "wikilink")の言語要素の類似は非常によく言われてはいるが\[5\]、意図的にそのように設計したわけではない\[6\]。たとえば、C言語の ++ や -- は、PDP-11より古い、PDP-7に実装したB言語に由来していて、ハードウェアの持っていた機能からの影響もあるだろうが、いくつかの特徴はハードウェアからというよりもトンプソンのオリジナルであろうとリッチーが書き残している（[:en:Increment and decrement operators\#Historyを参照](https://ja.wikipedia.org/wiki/:en:Increment_and_decrement_operators#History "wikilink")）。

[thumb](https://ja.wikipedia.org/wiki/ファイル:Pdp-11-40.jpg "wikilink")

## 歴史

DECが16ビットのPDP-11を開発するきっかけとなったのは、[データゼネラル](../Page/データゼネラル.md "wikilink")が発売した[データゼネラルNova](../Page/データゼネラルNova.md "wikilink") である。Novaはワード長16ビットだが、DECが当時主力としていた[PDP-8](../Page/PDP-8.md "wikilink")のワード長は12ビットだった。PDP-11ファミリは1970年1月に発表され、同年前半に出荷が開始された。最終的な売り上げ台数は不明であるが、販売開始後の8年間で5万台が売れたことが知られている\[7\]。当初は[TTLのICで構成されていたが](../Page/Transistor-transistor_logic.md "wikilink")、1975年にはやや大規模な[集積回路](../Page/集積回路.md "wikilink")を使いCPUをワンボード化している。1979年にはマルチチップモジュール化したプロセッサ J-11 を開発。シリーズ最後の機種である PDP-11/94 と PDP-11/93 は1990年に登場した\[8\]。

## PDP-11シリーズの特徴

### 命令セット

[プログラマ](../Page/プログラマ.md "wikilink")がPDP-11を好むのは、その[直交性](https://ja.wikipedia.org/wiki/直交性 "wikilink")の高い[命令セット](../Page/命令セット.md "wikilink")によって[命令の種類とメモリアクセス方法を分けて考えることができるからである](../Page/命令_\(コンピュータ\).md "wikilink")。任意のメモリアクセス方法([アドレッシングモード](../Page/アドレッシングモード.md "wikilink"))を任意の命令に使用でき、他の命令セットのように例外事項を覚えておく必要がない。例えば、多くの命令セットでは `load` と `store` があるが、PDP-11には `move` 命令しかなく、転送元と転送先のどちらの[オペランドでもメモリもレジスタも指定可能である](https://ja.wikipedia.org/wiki/被演算子 "wikilink")。また、入出力専用の命令がなく、直交性によって入力デバイスから出力デバイスへ直接データ転送することも可能である。同様に加算命令も任意のオペランド（メモリ、レジスタ、デバイス）を加える数としても計算結果の格納先としても使える。

PDP-11の命令セットアーキテクチャは[B言語](../Page/B言語.md "wikilink")の慣習的構文に影響を与えていると言われているが、間違いである。[レジスタ](../Page/レジスタ_\(コンピュータ\).md "wikilink")[インクリメント](../Page/インクリメント.md "wikilink")やデクリメントを行うアドレッシングモードが C言語の `−−i` とか `i++` といった式に対応していると言われている。もし `i` も `j` もレジスタ変数なら、`*(−−i) = *(j++)` といった式は1個の[機械語](../Page/機械語.md "wikilink")命令に[コンパイルできる](../Page/コンパイラ.md "wikilink")。[デニス・リッチー](../Page/デニス・リッチー.md "wikilink")は、B言語設計時にPDP-11は存在しなかったのだからこの伝説は間違いだと、明確に否定した。ただし、[PDP-7](../Page/PDP-7.md "wikilink")の自動インクリメントセルがPDP-11のアドレッシングモードに影響している可能性はあるが、B言語そのものはPDP-7のその機能も使っていないと述べている\[9\]。それでも、[C言語](../Page/C言語.md "wikilink")はPDP-11で実装する際にPDP-11の持つ細かい利点を活用しており、そのために後のプロセッサの設計に影響を与えた可能性はある\[10\]。

論理的には、アドレッシングモードと命令セットによってベースが提供されていると言える。2オペランド命令は、2つの6[ビット](../Page/ビット.md "wikilink")フィールドでオペランドを指定し(3ビットがレジスタ指定で、3ビットがアドレッシングモード指定)、4ビットで命令コードを指定する。1オペランド命令は、6ビットでオペランドを指定し、10ビットで命令コードを指定する。どの命令でもオペランド指定フィールドには任意のアドレッシングモードを指定できる。8本のレジスタ(0番から7番まで)で、7本のレジスタは任意の用途に使用可能だが、6番のレジスタはいくつかの命令では[スタック](../Page/スタック.md "wikilink")[ポインタとして認識され](../Page/ポインタ_\(プログラミング\).md "wikilink")、7番のレジスタは[プログラムカウンタ](https://ja.wikipedia.org/wiki/プログラムカウンタ "wikilink")である。プログラムカウンタがプログラマから見えているという発明とアドレッシングモードの組合せで、絶対アドレス指定と相対アドレス指定が可能となった。アドレッシングモードとしては、レジスタ、即値、絶対アドレス指定、相対アドレス指定、間接アドレス指定、インデックス付きアドレッシングがあり、さらにレジスタの自動インクリメント/自動デクリメント（バイト操作なら1、ワード操作なら2）を指定できる。相対アドレス指定を使えば、機械語プログラムを[位置独立にできる](https://ja.wikipedia.org/wiki/位置独立コード "wikilink")。

### PDPエンディアン

PDP-11の[エンディアン](https://ja.wikipedia.org/wiki/エンディアン "wikilink")は独特であった。16ビット[ワード](../Page/ワード.md "wikilink")はリトルエンディアンで格納される。すなわち下位バイトがアドレスの小さいほうに格納される。32ビットワードを構成する2個の16ビットワードは、ビッグエンディアンで格納される。すなわち上位16ビットワードがアドレスの小さいほうに格納される。ここで、各16ビットワード内は前述のようにリトルエンディアンである。PDP-11が非常に一般化したため、この形式を **PDPエンディアン** と呼ぶことがある。

このような[ミドルエンディアンにまつわる問題を](https://ja.wikipedia.org/wiki/エンディアン#ミドルエンディアン "wikilink")「問題」と言う。これは  という文字列をPDPエンディアンの順序で並べ替えたものに由来する。 を他機種に移植した際、最初の起動メッセージ（しばしば、本格的な初期化に入る前、最小限のブートが完了したことを示すため、短い文字列を出力することがある）として「」ではなく「」と出力されたことがあった、と言われている。

（なお、コンピュータ中のデータの並べ方について「エンディアン」という語を使う提案は1980年になされたものであるため、初期のPDP-11についてエンディアンという語を使うのは後付けということになる）

### I/O専用バスの無い構成

他の初期のコンピュータとの大きな違いとして、初期の PDP-11 は[入出力](../Page/入出力.md "wikilink")専用[バスを持たず](../Page/バス_\(コンピュータ\).md "wikilink")、[Unibus](../Page/Unibus.md "wikilink") というメモリバスしか持たない。そのため入出力機器はメモリ空間にマッピングされ、特殊な I/O (入出力) 命令を必要としない。また、それぞれに割り込みベクターと割り込み優先度が設定される。プロセッサのアーキテクチャが可能にしたこの柔軟性の高いフレームワークにより、新たなバスデバイスを容易に考案でき、当初予想もしていなかった新たなハードウェアの制御も可能である。DECはこのUnibusの基本仕様を公開し、バスインタフェース回路基板のプロトタイプも提供し、ユーザーが独自のUnibus対応ハードウェアを開発できるようにしていた。

これにより、PDP-11は特注の周辺機器の制御を得意とした。[アルカテル・ルーセント](../Page/アルカテル・ルーセント.md "wikilink")の前身の1つである Bell Telephone Manufacturing Company が開発した[X.25](https://ja.wikipedia.org/wiki/X.25 "wikilink")ネットワーク・パケット交換機 BTMC DPS-1500 は管理システムとしてPDP-11と組み合わせて配備され、Unibus経由で直接接続されていた。

PDP-11ファミリの上位機種であるPDP-11/45やPDP-11/83システムは、この単一バス方式をやめている。その代わり、[CPU](../Page/CPU.md "wikilink")筐体内だけでCPUとメモリ間の専用インタフェース回路を使用し、UnibusやQ-busはI/O専用とした。PDP-11/70ではさらに、磁気ディスク装置や磁気テープ装置とメモリ間を新たな専用バス  で接続した。入出力機器はこういった構成でもメモリアドレス空間にマッピングされ続けたが、追加されたバスインタフェースの設定のためのコードを追加する必要があった。

### 割り込み

[割り込みシステムはなるべく単純になるよう設計され](../Page/割り込み_\(コンピュータ\).md "wikilink")、割り込みシーケンスでイベントを逃さないことを保証している。デバイスが割り込みを発生する場合、4本の優先度ラインのいずれかをアサートする。プロセッサは優先度毎の割り込みデイジーチェインに応答する(デイジーチェインはイベントを順番に並べる一種の論理回路である。最初の論理ゲートが最初に処理される。デイジーチェインはその優先度でのデバイス間の優先順位に従って設定される)。

PDP-11の設計では、この割り込み応答順はデバイスが物理的に[CPU](../Page/CPU.md "wikilink")に近い順番になっている。CPUが応答すると、デバイスはそのベクターアドレスをバスに出力する。これは4バイトのメモリブロックのアドレスである。CPUは[ステータスレジスタ](../Page/ステータスレジスタ.md "wikilink")とプログラムカウンタをベクターテーブルからロードする。このときのステータスレジスタの値は割り込みを不可とするようになっている。プログラムカウンタにロードされるアドレスは[割り込みハンドラ](https://ja.wikipedia.org/wiki/割り込みハンドラ "wikilink")のスタートアドレスである。割り込みハンドラがデバイスに関する処理を行い、その過程で割り込んできたデバイスの割り込み信号を再設定する。最後に特殊なRTI (Return From Interrupt) 命令でCPUが割り込まれた箇所に戻る。戻ったところが低優先度の割り込みの処理中の場合もあり、割り込み処理の入れ子が可能である。このような処理によって割り込みを受け付けそこなうことを防いでいる。未処理の割り込みはどの段階であってもそのまま存在していて、次のサイクルで処理可能である。割り込み処理が間違って起動されるとCPUはタイムアウトとなり、特殊な擬似割り込みを発生してユーザーに対してハードウェア故障を警告する。

### 大量生産のための設計

PDP-11は工場でそれなりに熟練した労働者が生産できるよう設計された。あらゆる観点から個々の工程の危険性を低減している。[ワイヤラッピング](../Page/ワイヤラッピング.md "wikilink")式の[バックプレーン](../Page/バックプレーン.md "wikilink")を使用し、[プリント基板](../Page/プリント基板.md "wikilink")をバックプレーン上のコネクタに差し込むようになっている。バックプレーン上のコネクタ同士はワイヤラッピングで接続される。ワイヤの被覆(テフロン)を剥いだ銅線(鍍金された硬い単芯線)が端子(四角柱の角)に巻かれて食い込むことで密着する。このコネクタ部分は電話の交換機などとよく似ている。

## LSI-11

[thumb](https://ja.wikipedia.org/wiki/ファイル:PDP-11-M7270.jpg "wikilink") [thumb](https://ja.wikipedia.org/wiki/ファイル:KL_DEC_F11.jpg "wikilink") [thumb](https://ja.wikipedia.org/wiki/ファイル:KL_DEC_J11.jpg "wikilink") 1975年2月に登場した LSI-11 (PDP-11/03)\[11\] は[大規模集積回路を使用した最初のPDP](../Page/集積回路.md "wikilink")-11である。[CPU](../Page/CPU.md "wikilink")は[ウェスタン・デジタル](https://ja.wikipedia.org/wiki/ウェスタン・デジタル "wikilink")製の4個の[LSIチップ](../Page/集積回路.md "wikilink")(MCP-1600チップセット)で構成される。Unibusによく似た[Q-bus](../Page/Q-bus.md "wikilink")を使用。大きな違いは Q-bus のアドレスバスとデータバスが物理的には同じ線を共有していることである（[マルチプレクサ](../Page/マルチプレクサ.md "wikilink")）。[I/Oデバイスのアドレッシングも若干異なり](../Page/入出力.md "wikilink")、22ビットの物理アドレス（Unibusでは 18ビット）とブロック転送モード（Unibusにはない）をサポートし、全体的には性能が大幅に向上している。

CPUの[マイクロコードには直接](../Page/マイクロプログラム方式.md "wikilink")[RS-232](../Page/RS-232.md "wikilink")Cまたはで端末と通信できる[デバッガ](../Page/デバッガ.md "wikilink")が組み込まれている。当時、そのようなデバッグには制御パネルのスイッチとランプを使うのが普通だったが、端末からコマンドを入力して指定したメモリアドレスやレジスタの内容を[八進数で表示できた](../Page/八進法.md "wikilink")。このデバッガはコンピュータの[レジスタを調べたり](../Page/レジスタ_\(コンピュータ\).md "wikilink")、[メモリや入出力機器を調べるために使われた](../Page/主記憶装置.md "wikilink")。従って、CPUが機能しない場合でもコンピュータの内部状態を調査して修理することが可能であった。

マイクロコードには汎用[ブート](../Page/ブート.md "wikilink")ストラップが含まれ、[DEC製の全てのディスクドライブを使用可能であった](../Page/ディジタル・イクイップメント・コーポレーション.md "wikilink")。

これら2つの発明はコンピュータが動作中は使われない。ハードディスクからブートできないとき、フロッピーからのブートを試すなど、全く起動しないときデバッガを使うといった使い方になる。これによって信頼性が向上し、全体としてコストを低減させている。

後期のQ-busベースのシステム（LSI-11/23、/73、/83 など）はDECが独自設計したチップセットを使用している。また、Unibus対応のPDP-11も後々まで継続し、CPUはQ-bus仕様のプロセッサカードを採用しつつ、アダプタでUnibusと接続してUnibus用[周辺機器](../Page/周辺機器.md "wikilink")が使えるようにしており、中には特別なメモリバスを採用して性能向上させた機種もある。

Q-bus系機種では他にも大きな技術革新があった。例えば、PDP-11/03の派生システムではシステム全体の [Power On Self Test](../Page/Power_On_Self_Test.md "wikilink") (POST) を導入している。

## PDP-11の衰退とその後

基本設計は非常に優れていて、最新技術も次々に取り入れていった。しかし、UnibusやQ-busの[スループット](../Page/スループット.md "wikilink")がシステム性能の[ボトルネック](../Page/ボトルネック.md "wikilink")となっていき、最終的に16[ビット](../Page/ビット.md "wikilink")[アーキテクチャではどうがんばっても超えられない限界が見えてきた](../Page/コンピュータ・アーキテクチャ.md "wikilink")。一部機種では物理アドレス空間を拡張したが、全てのプログラムは16ビットの仮想[アドレス空間](../Page/アドレス空間.md "wikilink")（64[K](../Page/キロ.md "wikilink")[バイト](../Page/バイト_\(情報\).md "wikilink")）に制限されていた。1980年代にメモリチップが低価格化していったが、PDP-11上の[ソフトウェア](../Page/ソフトウェア.md "wikilink")は大容量メモリを簡単には使えなかった。

DECがPDP-11の後継とした32ビットの[VAX](../Page/VAX.md "wikilink")（Virtual Address Extension; PDP-11の仮想アドレス拡張という意味）はこのような問題に対応したが、当初は[ハイエンド](https://ja.wikipedia.org/wiki/ハイエンド "wikilink")の[タイムシェアリング市場をターゲットとした](../Page/タイムシェアリングシステム.md "wikilink")。初期のVAXにはPDP-11互換モードがあり、32ビットのソフトウェアと同時に既存ソフトウェアも使用可能だった。

[インテル](https://ja.wikipedia.org/wiki/インテル "wikilink")の[8086などは](../Page/Intel_8086.md "wikilink")[セグメント方式](../Page/セグメント方式.md "wikilink")による拡張で16ビットのアドレス空間を超え、32ビット化などという大層なことをしなくても 1Mバイトまでのメモリを扱えた。これは成長過程にあった IBM PC 互換機市場には十分だったが、[80286が登場する前に](../Page/Intel_80286.md "wikilink")1Mバイトの限界が問題となってきた。80286はセグメントアドレス空間を拡大し、[80386では](../Page/Intel_80386.md "wikilink")32ビットのリニアなアドレス空間がサポートされた。

技術者がより大きなアドレス空間をサポートするアーキテクチャに移っていったころ、[MC68020](../Page/MC68020.md "wikilink") (1984) や[Intel 80386](../Page/Intel_80386.md "wikilink") (1985) のような32ビット[マイクロプロセッサ](../Page/マイクロプロセッサ.md "wikilink")が登場してきた。量産効果でこれらのマイクロプロセッサは低価格化し、PDP-11はコスト面でも太刀打ちできなくなった。PDP-11ベースの[パーソナルコンピュータ](../Page/パーソナルコンピュータ.md "wikilink") [DEC Professional](https://ja.wikipedia.org/wiki/DEC_Professional "wikilink") などの試みも失敗に終わった。

1994年、DECはPDP-11システムのソフトウェアの権利を Mentec Inc. （LSI-11ボードを [Q-bus](../Page/Q-bus.md "wikilink") およびパソコン用に製造する会社）に売却した\[12\]。そして1997年にはPDP-11ファミリの生産を終了させた。Mentecは数年間、PDP-11アーキテクチャの新プロセッサを製造していた。

1980年代、[IBM PC](../Page/IBM_PC.md "wikilink") とその互換機が小型コンピュータ市場を席巻したが、DECはそれにうまく対抗策を打ち出せなかった。

1990年代後半には[DECを初めとする](../Page/ディジタル・イクイップメント・コーポレーション.md "wikilink")[ミニコンピュータ](../Page/ミニコンピュータ.md "wikilink")業界は壊滅し、[UNIX](../Page/UNIX.md "wikilink")と[Windowsの](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")[サーバ](../Page/サーバ.md "wikilink")やワークステーションに取って代わられたのである。

しかし、2008年時点でも現役で使用されているPDP-11も存在している。[1](http://www.field-one.com/support/faq.html)

2010年7月までに、[VHDL](../Page/VHDL.md "wikilink")で実装したPDP-11/70の[IPコア](../Page/IPコア.md "wikilink")が[OpenCoresにて公開された](https://ja.wikipedia.org/wiki/:en:OpenCores "wikilink")。\[13\]ライセンスは[GPL](../Page/GNU_General_Public_License.md "wikilink")。2006年にPDP-11のマニュアルを発掘した有志の開発者により実装され、2007年までに[FPGA](../Page/FPGA.md "wikilink")搭載ボード(Digilent S3BOARD)上で初めて動作。2009年までに[UNIX 5th Editionおよび](../Page/Research_Unix.md "wikilink")[2.11 BSDのブートに成功](../Page/BSD.md "wikilink")。

## アーキテクチャ詳細

以下の情報はDECの<cite>PDP-11 Processor Handbook</cite>にある。([ゴードン・ベル](../Page/ゴードン・ベル.md "wikilink")の[1969 edition](http://research.microsoft.com/users/GBell/Digital/PDP%2011%20Handbook%201969.pdf)を参照)

### メモリ管理

PDP-11のアドレスは16ビットであり、64[KBまでのアドレス範囲を指定できる](../Page/キロバイト.md "wikilink")。PDP-11からVAXに移行するころ、8ビットのバイトと16進表記が一般的になっていたが、PDP-11では八進表記が普通で、搭載メモリ容量はワード数で表記されるのが普通だった。したがって、基本論理アドレス空間は32Kワードだが、上位4Kワード（アドレス 160000 から 177777 まで）は周辺機器のレジスタのマッピング用に予約されており、メモリはマッピングされない。したがって、初期のPDP-11の最大メモリ容量は28Kワードだった。

この制約に対して、以下のような技法が使われた。

  - 後期のPDP-11では、[仮想記憶](../Page/仮想記憶.md "wikilink")をサポートするメモリ管理ユニットが使われた。物理アドレスは18ビットまたは22ビットに拡張され、256KBまたは4MBのメモリを扱えるようになったが、1つの論理アドレス空間は16ビット（32Kワード）に制限されたままだった。
  - PDP-11/45をはじめとする機種では、命令用論理空間（32Kワード）とデータ用論理空間（32Kワード）を設定可能とした。初期のUNIXなどはこの機能を使っていた。
  - 例えば [Modula-2](https://ja.wikipedia.org/wiki/Modula-2 "wikilink") の実装では、実行環境が論理空間を8kBのページに分割して制御し、ユーザーからは隠蔽した形で[バンク切り換え](../Page/バンク切り換え.md "wikilink")のような操作を行っていた（外部リンク参照）。

### アドレッシングモード

多くの命令で6ビットで1オペランドを構成しており、3ビットで8本ある汎用レジスタのいずれかを指定し、3ビットで8種類ある[アドレッシングモード](../Page/アドレッシングモード.md "wikilink")のいずれかを指定する。このため八進表記が自然に使われた。

以下では仮の1オペランド命令をOPRで表し、アセンブリ言語でのアドレッシングモードの表現を示す。Rnは汎用レジスタを意味し、R0からR7まである。コードの "n" はレジスタ番号である。

#### 汎用レジスタのアドレッシングモード

任意の汎用レジスタに適用できる8種類の[アドレッシングモード](../Page/アドレッシングモード.md "wikilink")を下表に示す。なお、R6（スタックポインタ）とR7（プログラムカウンタ）については別に解説する。

| コード | 名称          | 例          | 説明                                               |
| --- | ----------- | ---------- | ------------------------------------------------ |
| 0n  | レジスタ        | OPR Rn     | Rnにオペランドがある。                                     |
| 1n  | レジスタ間接      | OPR (Rn)   | Rnにオペランドのアドレスがある。                                |
| 2n  | 自動インクリメント   | OPR (Rn)+  | Rnにオペランドのアドレスがあり、命令実行後にRnの内容をインクリメントする。          |
| 3n  | 自動インクリメント間接 | OPR @(Rn)+ | Rnにオペランドへのポインタのアドレスがあり、命令実行後にRnの内容を2だけインクリメントする。 |
| 4n  | 自動デクリメント    | OPR −(Rn)  | 命令実行前にRnをデクリメントし、それをオペランドのアドレスとして使用する。           |
| 5n  | 自動デクリメント間接  | OPR @−(Rn) | 命令実行前にRnを2だけデクリメントし、それをオペランドへのポインタのアドレスとして使用する。  |
| 6n  | インデックス      | OPR X(Rn)  | Rn+X がオペランドのアドレス。Xはこの命令に続くワード。                   |
| 7n  | インデックス間接    | OPR @X(Rn) | Rn+X がオペランドへのポインタのアドレス。Xはこの命令に続くワード。             |

2オペランド命令では両方のオペランドでこれらのモードを使える。インデックスおよびインデックス間接モードは命令に続くワードも命令の一部として使用するので、2オペランド命令は3ワードになる場合がある。

自動インクリメントと自動デクリメントはバイト命令なら1ずつ、ワード命令なら2ずつインクリメント/デクリメントする。間接モードの場合、ポインタ1つ分のインクリメント/デクリメントになるので、2ずつとなる。

#### プログラムカウンタのアドレッシングモード

R7（プログラムカウンタ）を使用する場合、以下の4つのアドレッシングモードが意味のある効果を発揮する。

| コード | 名称      | 例        | 説明                                             |
| --- | ------- | -------- | ---------------------------------------------- |
| 27  | イミディエート | OPR \#n  | オペランドは命令内にある。                                  |
| 37  | 絶対      | OPR @\#a | オペランドの絶対アドレスが命令内にある                            |
| 67  | 相対      | OPR a    | 命令に続くワードの内容 a を PC+2 に加算したものをアドレスとして使用する。      |
| 77  | 相対間接    | OPR @a   | 命令に続くワードの内容 a を PC+2 に加算したものをアドレスのアドレスとして使用する。 |

絶対モードは例えば、固定のアドレスにマッピングされたI/Oレジスタのアクセスに使用する。相対モードはプログラムの変数を参照する場合や分岐先を指定する場合に使用する。相対モードや相対間接モードのみを使ったプログラムは[位置独立となる](https://ja.wikipedia.org/wiki/位置独立コード "wikilink")。つまり、プログラムを配置するアドレスが仮定されていないので、任意の位置にロードでき、移動させることも可能である（[リロケータブルバイナリ](../Page/リロケータブルバイナリ.md "wikilink")）。

イミディエートモードと絶対モードは通常の自動インクリメントモードと自動デクリメント間接モードに対応している。上の表にあるように補助ワードを「命令内」にあるとするか、命令の次のワードと考えるかは立場によって異なる。なお、PCは常に次々と命令を指していくので、常に2ずつ自動インクリメントされる。

#### スタックのアドレッシングモード

R6はSPと表記されることもあり、トラップや割り込みの際のハードウェアスタックのスタックポインタとして使われる。このスタックは、アドレスの小さい方に向かって成長する。SPまたはプログラマがソフトウェアスタックのスタックポインタとして選択した任意のレジスタには、次のようなアドレッシングモードがある。

| コード | 名称          | 例      | 説明                                         |
| --- | ----------- | ------ | ------------------------------------------ |
| 16  | 間接          | (SP)   | オペランドはスタックのトップにある。                         |
| 26  | 自動インクリメント   | (SP)+  | オペランドはスタックのトップにあり、それを使用後にポップする。            |
| 36  | 自動インクリメント間接 | @(SP)+ | オペランドへのポインタがスタックのトップにある。それを使用後にポップする。      |
| 46  | 自動デクリメント    | −(SP)  | 値をスタックにプッシュする。                             |
| 66  | インデックス      | X(SP)  | スタックのトップからの相対位置でスタック内の任意のアイテムを参照する。        |
| 76  | インデックス間接    | @X(SP) | スタックのトップからの相対位置でスタック内の任意のポインタの指すアイテムを参照する。 |

ソフトウェアスタックはバイトも積むことができるが、SPの場合はワードしか積まない。従ってSPの自動インクリメント/自動デクリメントは常に2ずつである。

### 命令セット

PDP-11はバイト（群）やワード（群）を操作する。バイト（群）はレジスタ番号で指定され、そのレジスタの下位バイトを直接操作するか、そのレジスタでメモリ位置を指す。ワード（群）もレジスタ番号で指定され、そのレジスタの内容を直接操作するか、そのレジスタでメモリ位置を指す。ワードは偶数番地境界になければならない。オペランドのあるほとんどの命令で、ビット15がセットされているものはバイトアドレッシングで、ビット15がクリアされているものはワードアドレッシングである。以下の表で示すとおり、[ニーモニック](https://ja.wikipedia.org/wiki/ニーモニック "wikilink")の最後尾に "B" をつけるとバイト操作を意味する（例えば、MOV と MOVB）。

#### 2オペランド命令

命令の先頭4ビットが命令コードである（特にビット15でワードアドレッシングかバイトアドレッシングかを示す）。6ビットで1オペランドとなっており、2オペランドある。オペランドの内容については上述のアドレッシングモードを参照。

<table>
<tbody>
<tr class="odd">
<td><p>nowrap style="width:2em"|15</p></td>
<td><p>nowrap style="width:2em"|14</p></td>
<td><p>nowrap style="width:2em"|13</p></td>
<td><p>nowrap style="width:2em"|12</p></td>
<td><p>nowrap style="width:2em"|11</p></td>
<td><p>nowrap style="width:2em"|10</p></td>
<td><p>nowrap style="width:2em"|9</p></td>
<td><p>nowrap style="width:2em"|8</p></td>
<td><p>nowrap style="width:2em"|7</p></td>
<td><p>nowrap style="width:2em"|6</p></td>
<td><p>nowrap style="width:2em"|5</p></td>
<td><p>nowrap style="width:2em"|4</p></td>
<td><p>nowrap style="width:2em"|3</p></td>
<td><p>nowrap style="width:2em"|2</p></td>
<td><p>nowrap style="width:2em"|1</p></td>
<td><p>nowrap style="width:2em"|0</p></td>
</tr>
<tr class="even">
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
</tbody>
</table>

| 命令コード | ニーモニック | 説明                                     |
| ----- | ------ | -------------------------------------- |
| 01    | `MOV`  | 転送: `dest = src`                       |
| 11    | `MOVB` |                                        |
| 02    | `CMP`  | 比較: `src − dest` を計算し、フラグだけセットする。      |
| 12    | `CMPB` |                                        |
| 03    | `BIT`  | ビットテスト: `dest & src` を計算し、フラグだけをセットする。 |
| 13    | `BITB` |                                        |
| 04    | `BIC`  | ビットクリア: `dest &= ~src`                 |
| 14    | `BICB` |                                        |
| 05    | `BIS`  | ビットセット（論理和）: `dest \|= src`            |
| 15    | `BISB` |                                        |
| 06    | `ADD`  | 加算: `dest += src`                      |
| 16    | `SUB`  | 減算: `dest −= src`                      |

`ADD`命令と`SUB`命令はワードアドレッシングであり、バイトを対象とするバージョンは存在しない。

一部の2オペランド命令は、一方のオペランドにレジスタしか指定できない。

<table>
<tbody>
<tr class="odd">
<td><p>nowrap style="width:2em"|15</p></td>
<td><p>nowrap style="width:2em"|14</p></td>
<td><p>nowrap style="width:2em"|13</p></td>
<td><p>nowrap style="width:2em"|12</p></td>
<td><p>nowrap style="width:2em"|11</p></td>
<td><p>nowrap style="width:2em"|10</p></td>
<td><p>nowrap style="width:2em"|9</p></td>
<td><p>nowrap style="width:2em"|8</p></td>
<td><p>nowrap style="width:2em"|7</p></td>
<td><p>nowrap style="width:2em"|6</p></td>
<td><p>nowrap style="width:2em"|5</p></td>
<td><p>nowrap style="width:2em"|4</p></td>
<td><p>nowrap style="width:2em"|3</p></td>
<td><p>nowrap style="width:2em"|2</p></td>
<td><p>nowrap style="width:2em"|1</p></td>
<td><p>nowrap style="width:2em"|0</p></td>
</tr>
<tr class="even">
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
</tbody>
</table>

ここで、レジスタペアが使われる。「`(R,R+1)`」のように記述し、Rレジスタが上位ワードであって偶数番目でなければならない。2つ目のレジスタは下位ワード（または余り）である。乗算ではRが奇数番目のレジスタであってもよいが、その場合の積の上位ワードはレジスタに保持されない。

| 命令コード | ニーモニック    | 説明                                                                       |
| ----- | --------- | ------------------------------------------------------------------------ |
| 070   | `MUL`     | 乗算: (R,R+1) = R × src                                                    |
| 071   | `DIV`     | 除算: (R,R+1) ÷ src を計算。商を R、余りを R+1 へ                                     |
| 072   | `ASH`     | 算術シフト: `R <<= src` を行う。シフトするビット数は −32 から 31 まで指定可能。                      |
| 073   | `ASHC`    | 連鎖算術シフト: `(R,R+1) <<= src` を行い、シフトするビット数は −32 から 31 まで指定可能               |
| 074   | `XOR`     | 排他的論理和: `dest ^= reg` （ワードのみ）                                            |
| 075   | （浮動小数点演算） |                                                                          |
| 076   | （システム命令）  |                                                                          |
| 077   | `SOB`     | デクリメントし、分岐: レジスタをデクリメントし、結果がゼロでない場合はPC相対で後方へ分岐する。分岐できる範囲は 0 から 63 ワードまで。 |

#### 1オペランド命令

命令の先頭10ビットが命令コードで、特にビット15はワードアドレッシングかバイトアドレッシングかを示す。先頭4ビットの組合せのほとんどが2オペランド命令で使われているため、命令コードが9ビットであっても、それほど命令の種類は多くない。残り6ビットで1オペランドを表す。

|    |   |   |   |    |        |      |          |  |   |   |  |   |   |  |   |
| -- | - | - | - | -- | ------ | ---- | -------- |  | - | - |  | - | - |  | - |
| 15 |   |   |   | 11 | 10     |      |          |  | 6 | 5 |  | 3 | 2 |  | 0 |
| B  | 0 | 0 | 0 | 1  | Opcode | Mode | Register |  |   |   |  |   |   |  |   |

| 命令コード | ニーモニック       | 説明                           |
| ----- | ------------ | ---------------------------- |
| 0003  | SWAB         | バイトスワップ: ワードを8ビットローテート       |
| 004r  | （サブルーチンコール）  |                              |
| 104x  | （エミュレータトラップ） |                              |
| 0050  | CLR          | クリア: dest = 0                |
| 1050  | CLRB         |                              |
| 0051  | COM          | 補数: dest = \~dest            |
| 1051  | COMB         |                              |
| 0052  | INC          | インクリメント: dest += 1           |
| 1052  | INCB         |                              |
| 0053  | DEC          | デクリメント: dest −= 1            |
| 1053  | DECB         |                              |
| 0054  | NEG          | 符号反転: dest = −dest           |
| 1054  | NEGB         |                              |
| 0055  | ADC          | キャリー加算: dest += C            |
| 1055  | ADCB         |                              |
| 0056  | SBC          | キャリー減算: dest −= C            |
| 1056  | SBCB         |                              |
| 0057  | TST          | テスト: src をロードし、フラグのみセットする    |
| 1057  | TSTB         |                              |
| 0060  | ROR          | 1ビット右ローテート                   |
| 1060  | RORB         |                              |
| 0061  | ROL          | 1ビット左ローテート                   |
| 1061  | ROLB         |                              |
| 0062  | ASR          | 右シフト: dest \>\>= 1           |
| 1062  | ASRB         |                              |
| 0063  | ASL          | 左シフト: dest \<\<= 1           |
| 1063  | ASLB         |                              |
| 0064  | MARK         | サブルーチンから復帰。0から63個の命令ワードをスキップ |
| 1064  | MTPS         | ステータスレジスタへ転送: PS = src       |
| 0065  | MFPI         | 前のI空間から転送: −(SP) = src       |
| 1065  | MFPD         | 前のD空間から転送: −(SP) = src       |
| 0066  | MTPI         | 前のI空間へ転送: dest = (SP)+       |
| 1066  | MTPD         | 前のD空間へ転送: dest = (SP)+       |
| 0067  | SXT          | 符号拡張: dest = （Nフラグを16個コピー）   |
| 1067  | MFPS         | ステータスレジスタから転送: dest = PS     |

SWAB命令は指定したワードの上位バイトと下位バイトを入れ替えるもので、バイトアドレッシングは存在しない。

#### 条件分岐命令

多くの分岐命令は、PSW（ステータスレジスタ）の条件コードの状態に基づいて分岐するか否かを決定する。一般に直前にCMP命令、BIT命令、TST命令などを行って条件コードをセットする。算術演算命令や論理演算命令も条件コードをセットする。[インテル](https://ja.wikipedia.org/wiki/インテル "wikilink")の[x86](https://ja.wikipedia.org/wiki/x86 "wikilink")とは異なり、MOV命令も条件コードをセットする。したがって、転送した値がゼロか否か、負か否かで条件分岐することもできる。

命令の上位8ビットが命令コードである。下位8ビットで現在のプログラムカウンタからの相対オフセットを指定する。オフセットはワード数であり、分岐先アドレスはそれを2倍してPCに加えたものとなる。またオフセットは符号付整数なので、前方にも後方にも分岐できる。

|    |   |   |   |    |        |        |   |   |  |  |  |  |  |  |   |
| -- | - | - | - | -- | ------ | ------ | - | - |  |  |  |  |  |  | - |
| 15 |   |   |   | 11 | 10     |        | 8 | 7 |  |  |  |  |  |  | 0 |
| x  | 0 | 0 | 0 | 0  | Opcode | Offset |   |   |  |  |  |  |  |  |   |

| 命令コード  | ニーモニック          | 説明                     |
| ------ | --------------- | ---------------------- |
| 0000xx | （システム命令）        |                        |
| 0004xx | BR              | 無条件分岐                  |
| 0010xx | BNE             | 等しくないとき分岐 (Z=0)        |
| 0014xx | BEQ             | 等しいとき分岐 (Z=1)          |
| 0020xx | BGE             | 大きいか等しいとき分岐 (N|V = 0)  |
| 0024xx | BLT             | 小さいとき分岐 (N|V = 1)      |
| 0030xx | BGT             | 大きいとき分岐 (N^V = 1)      |
| 0034xx | BLE             | 小さいか等しいとき分岐 (N^V = 0)  |
| 1000xx | BPL             | 正のとき分岐 (N=0)           |
| 1004xx | BMI             | 負のとき分岐 (N=1)           |
| 1010xx | BHI             | 高いとき分岐 (C|Z = 0)       |
| 1014xx | BLOS            | 低いか同じとき分岐 (C|Z = 1)    |
| 1020xx | BVC             | オーバーフローしていないとき分岐 (V=0) |
| 1024xx | BVS             | オーバーフローしているとき分岐 (V=1)  |
| 1030xx | BCC             | キャリーがないとき分岐 (C=0)      |
| BHIS   | 高いか同じとき分岐 (C=0) |                        |
| 1034xx | BCS             | キャリーがあるとき分岐 (C=1)      |
| BLO    | 低いとき分岐 (C=1)    |                        |

2オペランド命令の表にある SOB (subtract one and branch) も条件分岐命令である。レジスタオペランドをデクリメントし、結果がゼロでないとき命令の下位6ビットを符号なしオフセットと解釈して後方に分岐する。

分岐できる範囲が限られているため、コードが成長していくとこれらの命令では分岐先に到達できなくなる可能性がある。その場合2ワードを必要とするJMP命令に書き換え、JMP命令は無条件分岐なので、例えば元が BEQ だった場合は BNE に書き換えてJMP命令をスキップするようにする。

#### ジャンプとサブルーチン関連

  - JMP （ジャンプ）
  - JSR （サブルーチンコール）
  - RTS （サブルーチンから復帰）
  - MARK （復帰時のスタックのクリーンアップ）
  - EMT （エミュレータトラップ）
  - TRAP, BPT （ブレークポイントトラップ）
  - IOT （入出力トラップ）
  - RTI & RTT （割り込みからの復帰）

JSR命令は任意のレジスタをスタック上にセーブできる。セーブすべきレジスタがない場合はPCを指定し (JSR PC,address)、サブルーチンから復帰する際も RTS PC とする。例えば、"JSR R4, address" としてサブルーチンを呼び出すと、R4の元の値がスタックのトップに置かれ、リターンアドレス（JSR命令の次の命令のアドレス）が R4 に格納される。リターンアドレスの位置にはコードではなくデータを置いておいて (R4)+ で読み込んだり、ポインタを置いておいて @(R4)+ で読み込む。すると自動インクリメントでデータ部分を飛ばすことになり、R4が真のリターンアドレスになる。そこで RTS R4 を実行すれば正しい位置に復帰できる。

#### その他の命令

  - HALT, WAIT （割り込みを待ち合わせる）
  - RESET （Unibusをリセット）

#### 条件コード操作

  - CLC, CLV, CLZ, CLN, CCC （対応する条件コードをクリア）
  - SEC, SEV, SEZ, SEN, SCC （対応する条件コードをセット）

ステータスレジスタ (PSW) には以下の4つの条件コードがある。

  - N - 負値であることを示す。
  - Z - ゼロ（比較結果が等しい）であることを示す。
  - V - オーバーフローが発生したことを示す。
  - C - キャリーが発生したことを示す。

SCCとCCCはこれら4つを全てクリアまたはセットする。

#### オプションの命令セット

  - 拡張命令セット（、EIS）
    PDP-11/35、11/40、11/03 でのオプション。後期機種では標準となった。
      - `MUL`、`DIV` - 乗算と除算
      - `ASH`、`ASHC` - 算術シフト
  - 浮動小数点命令セット （、FIS）
    PDP-11/35、11/40、11/03 でのオプション。
      - `FADD`、`FSUB`、`FMUL`、`FDIV` - [単精度](https://ja.wikipedia.org/wiki/単精度 "wikilink")のみ。レジスタオペランドの指すスタック上の浮動小数点数を対象とする。
  - 浮動小数点プロセッサ （、FPP）
    PDP-11/45およびその後の多くの機種でのオプション。
      - 単精度または[倍精度](https://ja.wikipedia.org/wiki/倍精度 "wikilink")についての全ての浮動小数点演算。どちらになるかは浮動小数点ステータスレジスタ内のビット設定による。
      - 単精度浮動小数点数の形式は [IEEE 754](../Page/IEEE_754.md "wikilink") 以前のものだが、符号ビット、8ビット指数、23ビット仮数（けち表現）となっている。
  - ビジネス命令セット （、CIS）
    11/23 と 11/24 ではマイクロコードによるオプション、11/44では追加モジュール、11/74では一部バージョンでサポート。 と  で使用する各種文字列命令と十進命令をサポート。
  - PSWアクセス命令
    PSWはメモリアドレス 177 776 にマッピングされているが、最初期の機種以外では以下のような命令があって、PSWにより直接的にアクセスできる。
      - `SPL` - 優先度レベルの設定
      - `MTPS` - PSWへ転送
      - `MFPS` - PSWから転送
  - 他のメモリ空間へのアクセス命令
    命令論理空間とデータ論理空間を複数提供する後期機種において、他の論理空間にアクセスするための命令群で、直交性がない。例えば、オペレーティングシステム内のランタイムサービス（[システムコール](../Page/システムコール.md "wikilink")）ルーチンが呼び出し側と情報交換するのに用いた。
      - `MTPD`（）
      - `MTPI`（）
      - `MFPD`（）
      - `MFPI`（）

## アセンブリ言語によるプログラミング例

[thumb](https://ja.wikipedia.org/wiki/ファイル:Papertape.jpg "wikilink")\]\] RT-11で動作するマクロアセンブラによる  プログラムである:

<code>`        .TITLE  HELLO WORLD`
`        .MCALL  .TTYOUT,.EXIT`
`HELLO:: MOV     #MSG,R1 ;STARTING ADDRESS OF STRING`
`1$:     MOVB    (R1)+,R0 ;FETCH NEXT CHARACTER`
`        BEQ     DONE    ;IF ZERO, EXIT LOOP`
`        .TTYOUT         ;OTHERWISE PRINT IT`
`        BR      1$      ;REPEAT LOOP`
`DONE:   .EXIT`

`MSG:    .ASCIZ /Hello, world!/`
`        .END    HELLO`</code>

この[プログラムの](../Page/プログラム_\(コンピュータ\).md "wikilink")[ファイル名を](../Page/ファイル_\(コンピュータ\).md "wikilink")`HELLO.MAC`としたとき、アセンブルしてリンクして実行するときのコンソールの表示は以下のようになる:

<code>`.MACRO HELLO`
`ERRORS DETECTED:  0`

`.LINK HELLO`

`.R HELLO`
`Hello, world!`
`.`</code>

（RT-11のコマンドプロンプトは「`.`」である）

のコードのもっと複雑な例としては、ケビン・ミュレル\[14\]の [](http://www.ps8computing.co.uk/PDP11/kpun_mac.htm) やファーバ・リサーチ\[15\]の [JULIAN](http://www.farbaresearch.com/examples/julian.htm) ルーチンがある。その他の用コードの[ライブラリ](../Page/ライブラリ.md "wikilink")として [](http://www.ibiblio.org/pub/academic/computer-science/history/pdp-11/) や [](http://pdp-11.trailing-edge.com/) アーカイブがある。

これらのコードを  [エミュレータ](../Page/エミュレータ.md "wikilink")で実行してみることもできる。ボブ・スプニク\[16\]の [SIMH](https://ja.wikipedia.org/wiki/SIMH "wikilink") はだけでなく各種[アーキテクチャをエミュレートでき](../Page/コンピュータ・アーキテクチャ.md "wikilink")、それらアーキテクチャの[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink")のソフトウェアキットを含む（RT-11もある）。

## PDP-11 の機種

PDP-11プロセッサは[I/Oバスの種類などでいくつかのグループに分類される](../Page/入出力.md "wikilink")。いずれのグループも各機種には[OEM](../Page/OEM.md "wikilink")版とエンドユーザー版がある。どの機種であっても命令セットは同じだが、後期機種には新命令が追加されており、一部命令の動作が若干異なる。アーキテクチャの進化の伴い、プロセッサのステータス/コントロールレジスタ群の扱い方も変化している。

### Unibus 機種

[thumb](https://ja.wikipedia.org/wiki/ファイル:Digital_PDP11-IMG_1498.jpg "wikilink") [thumb](https://ja.wikipedia.org/wiki/ファイル:Pdp-11-70-panel.jpg "wikilink") [thumb](https://ja.wikipedia.org/wiki/ファイル:PDP-11-70-DDS570.jpg "wikilink")

以下の機種は主要バスとして [Unibus](../Page/Unibus.md "wikilink") を使用:

  - **PDP-11**(後に **PDP-11/20** に改名), **PDP-11/15** - 最初の機種。[マイクロプログラム方式](../Page/マイクロプログラム方式.md "wikilink")でないプロセッサを使用。ジェームス・オラフリン\[17\]が設計。[浮動小数点数](../Page/浮動小数点数.md "wikilink")はオプション。
  - **PDP-11/35**, **11/40** - /20 をマイクロプログラム方式にした後継。ジェームス・オラフリンが設計チームを率いた。
  - **PDP-11/45**, **11/50**, **11/55** - [磁気コアメモリ](../Page/磁気コアメモリ.md "wikilink")と同時に半導体メモリ（最大256[kB](../Page/キロバイト.md "wikilink")）を使用可能とした高速なマイクロプログラム方式プロセッサ。FP11 [FPU](../Page/FPU.md "wikilink") をオプションでサポートし、浮動小数点数のフォーマットがこれによって確立された。
  - **PDP-11/70** - 11/45 のアーキテクチャを物理メモリ4[MBまで拡大し](../Page/メガバイト.md "wikilink")、専用メモリバスを装備し、2Kバイトの[キャッシュメモリ](../Page/キャッシュメモリ.md "wikilink")を備え、Massbus で 高速I/Oデバイスを接続。
  - **PDP-11/05**, **11/10** - 11/20のコスト低減版
  - **PDP-11/34**, **11/04** - 11/35と11/05のコスト低減版。PDP-11/34 のコンセプトはボブ・アームストロング\[18\]によるもの。11/34はUnibusメモリを最大256kBまでサポート。11/34a ではFPUオプションをサポートし、11/34c では[キャッシュメモリ](../Page/キャッシュメモリ.md "wikilink")オプションをサポート。
  - **PDP-11/60** - ユーザーが書き込み可能なマイクロプログラム記憶装置を持つ PDP-11。ジェームス・オラフリンが率いる別のチームの設計
  - **PDP-11/44** - 11/45と11/70の後継。標準で[キャッシュメモリ](../Page/キャッシュメモリ.md "wikilink")と[浮動小数点ユニットを装備したもの](../Page/浮動小数点数.md "wikilink")。このマシンには洗練されたシリアル・コンソールを装備し、4MBの物理メモリをサポート。設計チームは John Sofio が率いた。複数ICでCPUを構成した最後の機種。
  - **PDP-11/24** - Unibus使用のPDP-11で初のVLSI版 PDP-11。Fonz-11 (F11) チップセットとUnibusアダプタを使用
  - **PDP-11/84** - VLSI Jaws-11(J11) チップセットとUnibusアダプタを使用
  - **PDP-11/94** - J11ベースで 11/84 よりも高速

### Q-bus 機種

[thumb](https://ja.wikipedia.org/wiki/ファイル:DEC_LSI11-23.jpg "wikilink") 以下の機種は主要バスとして [Q-bus](../Page/Q-bus.md "wikilink") を使用:

  - **PDP-11/03** (**LSI-11/03**) - 最初の[LSI版](../Page/集積回路.md "wikilink") PDP-11。[ウェスタン・デジタル](https://ja.wikipedia.org/wiki/ウェスタン・デジタル "wikilink")社のチップセットを使用し、60kBまでのメモリをサポート。
  - **PDP-11/23** - 第2世代のLSI (F-11) を使用。初期のユニットのメモリ容量は 248Kバイトだが、後に 4Mバイトまでサポートするようになった。
  - **PDP-11/23+**/**MicroPDP-11/23** - プロセッサカード上の機能を強化した 11/23
  - **MicroPDP-11/73** - 第3世代LSI-11。高速な Jaws-11 (J-11) チップセットを使用し、最大4MBのメモリをサポート。
  - **MicroPDP-11/53** - オンボードメモリを持つ低速版 11/73
  - **MicroPDP-11/83** - PMI(private memory interconnect)を使った高速版 11/73
  - **MicroPDP-11/93** - さらに高速。Q-bus を使用した最後の PDP-11
  - **Mentec M100** - Mentecが再設計した 11/93．J-11チップセットを 19.66MHz で駆動し、4個のオンボード・シリアルポート、最大4MBのオンボードメモリ、オプションのFPUがある。
  - **Mentec M11** - プロセッサアップグレードボード。Mentec による PDP-11マイクロコードの実装で、[テキサス・インスツルメンツ](../Page/テキサス・インスツルメンツ.md "wikilink")の TI 8832 ALU と TI 8818 マイクロシーケンサを使用。
  - **Mentec M1** - プロセッサアップグレードボード。Mentec による PDP-11マイクロコードの実装で、[Atmelの](https://ja.wikipedia.org/wiki/:en:Atmel "wikilink")0.35[μm版](../Page/マイクロメートル.md "wikilink")[ASIC](../Page/ASIC.md "wikilink")を使用\[19\]。
  - **Quickware QED-993** --高性能 PDP-11/93 プロセッサアップグレードボード

### 標準以外のバスを採用した機種

[thumb](https://ja.wikipedia.org/wiki/ファイル:DEC-PDT-11-150.jpg "wikilink")

  - PDT-11/110
  - PDT-11/130
  - PDT-11/150

PDTシリーズは「スマート(賢い)端末」としてマーケティングされたデスクトップシステムである。/110 と /130 は[VT100](../Page/VT100.md "wikilink")端末と同じ筐体だった。/150は8インチFDDを2つ、非同期シリアルポートを3つ、プリンターポートを1つ、モデムポートを1つ、同期シリアルポートを1つ備えた装置で、端末そのものは別途接続する必要がある。どれもLSI-11/03と同じ4つのチップで構成されるチップセットを使用している。/150と[VT105を組み合わせたシステムは](https://ja.wikipedia.org/wiki/VT100#後継シリーズ "wikilink") **MiniMINC** として販売された。

  - PRO-325
  - PRO-350
  - PRO-380

DEC Professional シリーズは [IBM](../Page/IBM.md "wikilink")の [8088](../Page/Intel_8088.md "wikilink") や [80286](../Page/Intel_80286.md "wikilink") ベースの初期の[パーソナルコンピュータ](../Page/パーソナルコンピュータ.md "wikilink")に対抗しようとしたデスクトップ機である。5.25インチ[フロッピーディスク](../Page/フロッピーディスク.md "wikilink")ドライブを装備し、325 以外は[ハードディスク](https://ja.wikipedia.org/wiki/ハードディスク "wikilink")も装備していた。CPU は LSI-11 で、[RSX-11](https://ja.wikipedia.org/wiki/RSX-11 "wikilink")M+ にメニューシステムを追加した P/OS が動作した。既存のPDP-11とのソフトウェア互換を意図的に阻害したため、（DEC以外の人々に予想された通り）市場では全く振るわなかった。また、[RT-11](https://ja.wikipedia.org/wiki/RT-11 "wikilink")も移植された。DEC内部では[RSTS/E](https://ja.wikipedia.org/wiki/RSTS/E "wikilink")も移植されたが、外部にはリリースされなかった。325と350は DCF-11 (Fonz) チップセットを採用しており、PDP-11/23などと同じである。380は DCJ-11 (Jaws) チップセットを採用しており、MicroPDP-11/53 などと同じだが、周辺チップセットの制約からクロック周波数は10MHzに制限されていた。

### 実際には商品化されなかった機種

  - PDP-11/27 - 主要I/Oバスとして VAXBIバス([VAX](../Page/VAX.md "wikilink")用32ビットバス)を使った Jaws-11 を使った実装
  - PDP-11/68 - 物理メモリ4MバイトをサポートするPDP-11/60の後継
  - PDP-11/74 - PDP-11/70を[マルチプロセッサ](https://ja.wikipedia.org/wiki/マルチプロセッサ "wikilink")化したもの。最大4個のプロセッサを相互接続し、ケーブルの取り回しが非常に難しくなった。また、ビジネス向きの[命令セット](../Page/命令セット.md "wikilink")拡張も行われている。いくつかのプロトタイプが組み立てられ、少なくとも2台のマルチプロセッサシステムがユーザーサイトでベータテストを受けたが、公式には出荷されることはなかった。4プロセッサシステムは RSX-11 オペレーティングシステム開発チームがテストし、シングルプロセッサ機は開発チーム全体のタイムシェアリング環境として使われた。11/74は32ビット機 VAX 11/780 と同時期に計画された。フィールドでの保守の問題でキャンセルされた\[20\]。いずれにしてもDECはPDP-11ユーザー全部をVAXに移行させることはできなかった。その原因は性能ではなく、PDP-11のリアルタイム性の良さにある。

### 特殊バージョン

[thumb](https://ja.wikipedia.org/wiki/ファイル:GT40_Lunar_Lander.jpg "wikilink") [thumb](https://ja.wikipedia.org/wiki/ファイル:DEC-MINC-23.jpg "wikilink")

  - GT40 - PDP-11/05をベースとした[ベクターグラフィック端末](https://ja.wikipedia.org/wiki/ベクターイメージ "wikilink")
  - GT42 - PDP-11/10をベースとしたベクターグラフィック端末
  - GT44 - PDP-11/40をベースとしたベクターグラフィック端末
  - GT62 - PDP-11/34aをベースとしたベクターグラフィック端末
  - H-11 - LSI-11/03の Heathkit社 OEM版
  - VT20 - PDP-11/05ベースのテキスト端末（ダイレクトマップ方式）で、テキスト編集と組版用
  - VT71 - LSI-11/03ベースのテキスト端末（ダイレクトマップ方式）で、テキスト編集と組版用
  - [VT103](../Page/VT100.md "wikilink") - LSI-11を搭載したバックプレーン内蔵の[VT100](../Page/VT100.md "wikilink")端末
  - VT173 - PDP-11/03をベースとしたハイエンド端末。ホストからシリアル接続で編集ソフトウェアをダウンロードして使用できる。出版社などで使われた。
  - [MINC-11](../Page/LINC.md "wikilink") -- PDP-11/03 または 11/23 をベースとした実験用システム\[21\]。11/23ベースのものは MINC-23 として販売されたが、MINC-11からMINC-23へのフィールドアップグレードが可能だった。命令セットが微妙に変更されており、MINC-23用ソフトウェアは11/23では動作できないことがあった。後期モデルでは互換性を確保していた。
  - [C.mmp](https://ja.wikipedia.org/wiki/:en:C.mmp "wikilink") -- [カーネギーメロン大学](https://ja.wikipedia.org/wiki/カーネギーメロン大学 "wikilink")による[マルチプロセッサ](https://ja.wikipedia.org/wiki/マルチプロセッサ "wikilink")システム

### 海賊版クローン

PDP-11は非常に人気があったため、[鉄のカーテン](../Page/鉄のカーテン.md "wikilink")の向こう側で無許可のクローンが何種類か製造された。一部は[DECのPDP](../Page/ディジタル・イクイップメント・コーポレーション.md "wikilink")-11とピン互換があり、周辺機器や[システムソフトウェア](../Page/システムソフトウェア.md "wikilink")を流用することができた。以下のような機種が知られている:

  - SM-4、SM-1420、SM-1600、[エレクトロニカBKシリーズ](https://ja.wikipedia.org/wiki/エレクトロニカBKシリーズ "wikilink")、[Electronika 60](https://ja.wikipedia.org/wiki/Electronika_60 "wikilink")、[DVK](https://ja.wikipedia.org/wiki/DVK "wikilink")、[UKNC](https://ja.wikipedia.org/wiki/UKNC "wikilink")（[ソビエト連邦](https://ja.wikipedia.org/wiki/ソビエト連邦 "wikilink")、PDP-11(PDP-11スキイ)とも呼ばれ、DECの米国内の生産台数より多かったと推定されている）。Elektronika 85、90は、いわゆる[ポケットコンピューター](https://ja.wikipedia.org/wiki/ポケットコンピューター "wikilink")のような極小のフォームファクタで製品化されていた。
  - SM-4、SM-1420、IZOT-1016、および周辺装置（[ブルガリア](../Page/ブルガリア.md "wikilink")）
  - SM-1620、SM-1630（[東ドイツ](../Page/ドイツ民主共和国.md "wikilink")）
  - MERA-60（[ポーランド](../Page/ポーランド.md "wikilink")）
  - SM-4、TPA-1140\[22\]、TPA-1148\[23\]、TPA-11/440\[24\]（[ハンガリー](../Page/ハンガリー.md "wikilink")）
  - CalData CDP-XI — アメリカ製で、DEC製OSが全て動作した\[25\]。

## オペレーティングシステム

PDP-11では以下のような[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink")(OS)が使用可能であった。

DEC製:

  - [BATCH-11/DOS-11](https://ja.wikipedia.org/wiki/:en:DEC_BATCH-11/DOS-11 "wikilink") - PDP-11ファミリ用の最初のOSだが、後に登場したRT-11に取って代わられた。
  - DSM-11 (Digital Standard [MUMPS](../Page/MUMPS.md "wikilink")) - [MUMPS](../Page/MUMPS.md "wikilink")環境のDECによる実装。
  - [RSTS/E](https://ja.wikipedia.org/wiki/RSTS/E "wikilink") - マルチユーザー・[タイムシェアリングシステム](../Page/タイムシェアリングシステム.md "wikilink")
  - [RSX-11](https://ja.wikipedia.org/wiki/RSX-11 "wikilink") - [リアルタイムオペレーティングシステム](../Page/リアルタイムオペレーティングシステム.md "wikilink")。[VMS](https://ja.wikipedia.org/wiki/VMS "wikilink")や[Windows NT系を設計した](../Page/Windows_NT系.md "wikilink")、[デヴィッド・カトラー](../Page/デヴィッド・カトラー.md "wikilink")が初めて設計したOS。[Windows NT](https://ja.wikipedia.org/wiki/Windows_NT "wikilink") の遠い祖先にあたる。
      - IAS - Interactive Application System、1975年ごろ登場したOSでRSX-11から派生。
      - P/OS - PDP-11ベースの[パーソナルコンピュータ](../Page/パーソナルコンピュータ.md "wikilink")用OS、RSX-11から派生。
  - [RT-11](https://ja.wikipedia.org/wiki/RT-11 "wikilink") - シングルユーザー・[リアルタイムオペレーティングシステム](../Page/リアルタイムオペレーティングシステム.md "wikilink")
  - [Ultrix](../Page/Ultrix.md "wikilink")-11 - [DEC自身によって移植された](../Page/ディジタル・イクイップメント・コーポレーション.md "wikilink")[UNIX](../Page/UNIX.md "wikilink")

サードパーティ製:

  - [ANDOS](https://ja.wikipedia.org/wiki/:en:ANDOS "wikilink") - ソビエト連邦製。ファイルシステムは[FAT12互換](../Page/File_Allocation_Table.md "wikilink")。
  - [CSI-DOS](https://ja.wikipedia.org/wiki/:en:CSI-DOS "wikilink") - ソビエト連邦製。
  - [DEMOS](https://ja.wikipedia.org/wiki/:en:DEMOS "wikilink") - ソビエト連邦製。[Unix系](../Page/Unix系.md "wikilink")。
  - Duress - [イリノイ大学アーバナ・シャンペーン校](../Page/イリノイ大学アーバナ・シャンペーン校.md "wikilink")とDatalogicsが開発。\[26\]
  - [Fuzzball](https://ja.wikipedia.org/wiki/:en:Fuzzball_router "wikilink") - LSI-11ベースの[ルーター](../Page/ルーター.md "wikilink")。[NSFnetの初期のバックボーンを形成した](../Page/全米科学財団ネットワーク.md "wikilink")。
  - [MERT](https://ja.wikipedia.org/wiki/:en:Multi-Environment_Real-Time "wikilink")\[27\] - [ベル研究所](../Page/ベル研究所.md "wikilink")が[UNIX](../Page/UNIX.md "wikilink")から派生させた[マイクロカーネル](https://ja.wikipedia.org/wiki/マイクロカーネル "wikilink")的なOS。
  - [MK-DOS](https://ja.wikipedia.org/wiki/:en:MK-DOS "wikilink") -ソビエト連邦製。
  - [MONECS](https://ja.wikipedia.org/wiki/:en:MONECS "wikilink") - [モナシュ大学](../Page/モナシュ大学.md "wikilink")で開発。教育用であり、言語処理系が豊富。
  - [MUMPS](../Page/MUMPS.md "wikilink") - 医療情報処理環境。
  - PC11 - [ピルキントン](../Page/ピルキントン.md "wikilink")が開発したプロセス制御OS。\[28\]
  - polyForth - Forth Inc. による[Forth](../Page/Forth.md "wikilink")環境。
  - Solo - [Concurrent Pascal](https://ja.wikipedia.org/wiki/:en:Concurrent_Pascal "wikilink") で書かれたシングルユーザーOS\[29\]
  - [TRIPOS](https://ja.wikipedia.org/wiki/TRIPOS "wikilink") - [ケンブリッジ大学](../Page/ケンブリッジ大学.md "wikilink")の実験的OS。PDP-11以外にも[データゼネラル](../Page/データゼネラル.md "wikilink") Nova や[MC68000](../Page/MC68000.md "wikilink")で動作した。
  - [TSX-Plus](https://ja.wikipedia.org/wiki/:en:TSX-Plus "wikilink") - RT-11ベースのマルチユーザーOS
  - [UCSD p-System](../Page/UCSD_p-System.md "wikilink") - [UCSD Pascal](../Page/UCSD_Pascal.md "wikilink") の開発環境を発展させたOS。
  - [UNIX](../Page/UNIX.md "wikilink") - 様々なバージョンがあり、主なものとして [Version 6 Unix](../Page/Version_6_Unix.md "wikilink")、[Version 7 Unix](../Page/Version_7_Unix.md "wikilink")、[UNIX System III](../Page/UNIX_System_III.md "wikilink")、[2BSD](https://ja.wikipedia.org/wiki/BSD#PDP-11版 "wikilink")、[Venix](https://ja.wikipedia.org/wiki/:en:Venix "wikilink") がある。
  - [Xinu](https://ja.wikipedia.org/wiki/Xinu "wikilink") - 教育用[Unix系](../Page/Unix系.md "wikilink")OS。

## 使用

[IUE_Control_and_Display_-_Udvar-Hazy_Center.JPG](https://ja.wikipedia.org/wiki/File:IUE_Control_and_Display_-_Udvar-Hazy_Center.JPG "fig:IUE_Control_and_Display_-_Udvar-Hazy_Center.JPG")の制御システム。PDP-11/35が組み込まれている。\]\] PDP-11ファミリは様々な用途で使われた。標準ミニコンピュータとして、[タイムシェアリングシステム](../Page/タイムシェアリングシステム.md "wikilink")、科学技術計算、教育、ビジネスなどに使われた。また[リアルタイムシステム](https://ja.wikipedia.org/wiki/リアルタイムシステム "wikilink")として、[プロセス制御](../Page/プロセス制御.md "wikilink")や[ファクトリーオートメーション](../Page/ファクトリーオートメーション.md "wikilink")にも使われた。

[OEM](../Page/OEM.md "wikilink")版は大規模システムの制御用[組み込みシステム](../Page/組み込みシステム.md "wikilink")として使われることが多かった。交通信号システム、医療システム、[CNC](https://ja.wikipedia.org/wiki/CNC "wikilink")[機械加工](https://ja.wikipedia.org/wiki/機械加工 "wikilink")、ネットワーク管理などに使われた。例えば、パケット交換網の管理に使われた例がある。1980年代のイギリスの[航空交通管制](../Page/航空交通管制.md "wikilink")でのレーダー情報処理には、PDP-11/34をベースとしたシステムが使われていた。放射線療法機器[セラック25](../Page/セラック25.md "wikilink")はPDP-11/23を組み込んでいた\[30\]。

は[半導体試験装置](../Page/半導体試験装置.md "wikilink")のテストプログラム格納用にPDP-11を採用していた。組み込みシステムで使われたPDP-11は、ソフトウェアの[2000年問題](../Page/2000年問題.md "wikilink")で使用不可能になるまで使われ続けたものが多い。アメリカ海軍は、パイロットの空間識失調状態の訓練を行うシミュレータで、2007年までPDP-11/34を使い続けていた。今ではPDP-11のソフトウェアをPC上のエミュレータで実行している\[31\]。

## 脚注

## 参考文献

  -
  -
## 関連文献

  -
  - Michael Singer, *PDP-11. Assembler Language Programming and Machine Organization*, John Wiley & Sons, NY: 1980.

## 外部リンク

  - [The PDP-11 FAQ](http://www.village.org/pdp11/faq.html)
  - [Preserving the PDP-11 Series of 16-bit minicomputers](http://www.pdp11.org)
  - [ゴードン・ベル](../Page/ゴードン・ベル.md "wikilink")と Bill Strecker の1975年の論文, [What We Learned From the PDP-11](http://research.microsoft.com/users/GBell/Digital/Bell_Strecker_What_we%20_learned_fm_PDP-11c%207511.pdf)
  - その他の論文やリンクは [Gordon Bell's site](http://research.microsoft.com/users/GBell/Digital/DECMuseum.htm).
  - [The Fuzzball](http://www.eecis.udel.edu/~mills/gallery/gallery10.html)
  - [On LSI-11, RT-11, Megabytes of Memory and Modula-2/VRS](http://www.modulaware.com/history/Vrsmot.pdf) by Günter Dotzel, [ModulaWare.com](http://www.modulaware.com) - Modula-2 コンパイラ/リンカ開発でPDP-11のアドレス空間の制限をどのように克服したかという論文。初出: *DEC Professional: the magazine for DEC users*, Professional Press, Spring House, PA. U.S.A., January 1986.
  - [dpuadweb.depauw.edu/dharms_web/pdp11/](http://dpuadweb.depauw.edu/dharms_web/pdp11/). [デポー大学](https://ja.wikipedia.org/wiki/デポー大学 "wikilink")。PDP-11/10でのプログラミングを紹介した動画。
  - [pdp11.co.uk](http://pdp11.co.uk/) PDP-11 の保存と復元を主題としたサイト
  - [electronica-60.ucoz.com](http://electronica-60.ucoz.com/) ロシア版PDP-11についてのサイト
  - [PDP-11/70 CPU core and SoC](http://opencores.org/project,w11), OpenCores - PDP-11/70のCPU、メモリ管理ユニットなどをFPGA上に再現

[Category:ミニコンピュータ](https://ja.wikipedia.org/wiki/Category:ミニコンピュータ "wikilink") [Category:コンピュータ_(歴代)](https://ja.wikipedia.org/wiki/Category:コンピュータ_\(歴代\) "wikilink") [Category:ディジタル・イクイップメント・コーポレーション](https://ja.wikipedia.org/wiki/Category:ディジタル・イクイップメント・コーポレーション "wikilink") [Category:コンピュータ史](https://ja.wikipedia.org/wiki/Category:コンピュータ史 "wikilink")

1.
2.
3.
4.
5.  Bakyo, John. ["DEC PDP-11, benchmark for the first 16/32 bit generation. (1970)"](http://www.cpushack.com/CPU/cpu3.html) in *Great Microprocessors of the Past and Present (V 13.4.0)*, Section Three, Part I. Accessed 2011-03-04
6.  ["The Development of the C Language"](http://cm.bell-labs.com/who/dmr/chist.html) in section **More History**, by [Dennis M. Ritchie](../Page/デニス・リッチー.md "wikilink"). Accessed August 5, 2011.
7.  [PDP-11は何台売れたのか](http://ftrcrblog.g2.xrea.com/7.html)
8.
9.
10. Bakyo, John. ["DEC PDP-11, benchmark for the first 16/32 bit generation. (1970)"](http://www.cpushack.com/CPU/cpu3.html) in *Great Microprocessors of the Past and Present (V 13.4.0)*, Section Three, Part I. Accessed 2011-03-04
11.
12. [Press Release re transfer of Operating Systems](http://groups.google.com/group/biz.digital.announce/tree/browse_frm/month/1994-07?_done=%2Fgroup%2Fbiz.digital.announce%2Fbrowse_frm%2Fmonth%2F1994-07%3F&)
13. [PDP-11/70 CPU core and SoC :: Overview](http://opencores.org/project,w11)。2014年8月15日閲覧。
14.
15.
16.
17.
18.
19. [Development Project Report](http://www.fuse-network.com/fuse/demonstration/30/24675/24675.pdf)
20.
21. [Binary Dinosaurs - Digital MINC-11](http://www.binarydinosaurs.co.uk/Museum/Digital/minc/index.php)
22. [TPA-1140](http://hampage.hu/tpa/e_tpa1140.html)
23. [TPA-1148](http://hampage.hu/tpa/e_tpa1148.html)
24. [TPA-11/440](http://hampage.hu/tpa/e_tpa11440.html)
25. [CalData_brochure](http://www.bitsavers.org/pdf/calData/CalData_Brochures_1974.pdf)
26. <http://www.village.org/pdp11/faq.pages/pdpOSes.html>
27.
28.
29.
30. Leveson, Nancy G., and Clark S. Turner. "An Investigation of the Therac-25 Accidents." *Computer* July 1993: 18-41.
31.
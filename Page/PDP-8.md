> この記事は[PDP-8](https://ja.wikipedia.org/wiki/PDP-8)から翻訳されています。


[thumbに展示されている](https://ja.wikipedia.org/wiki/ファイル:PDP-8.jpg "wikilink") PDP-8。初期のトランジスタを使用したPDP-8で、*Straight 8*と呼ばれる。\]\] **PDP-8**は、世界で初めて商業的に成功した[12ビット](https://ja.wikipedia.org/wiki/12ビット "wikilink")[ミニコンピュータ](https://ja.wikipedia.org/wiki/ミニコンピュータ "wikilink")であり、[1960年代](../Page/1960年代.md "wikilink")に[ディジタル・イクイップメント・コーポレーション](../Page/ディジタル・イクイップメント・コーポレーション.md "wikilink") (DEC) が製造した。[1965年](../Page/1965年.md "wikilink")3月22日に登場し、5万システムを売り上げ、DECの[PDPシリーズ](../Page/PDPシリーズ.md "wikilink")でも当時最も成功した[コンピュータ](../Page/コンピュータ.md "wikilink")となった\[1\]。最初のPDP-8の設計を指揮したは、後に[データゼネラル](../Page/データゼネラル.md "wikilink")を創業した\[2\]。

最初のPDP-8機種（非公式に "Straight-8" と呼ばれている）は [diode-transistor logic](https://ja.wikipedia.org/wiki/diode-transistor_logic "wikilink") (DTL) を採用した基板で構成されており、小型冷蔵庫ほどの大きさだった。

その後、デスクトップ型とラックマウント型のPDP-8/Sが登場。1ビット直列[ALU実装で](../Page/演算装置.md "wikilink")、小型化と低価格化を実現したが、最初のPDP-8に比べると性能がかなり低い。PDP-8/Sに接続可能な唯一のストレージがDF32というディスク装置（容量32Kワード）だった。

その後のシステム（PDP-8/I、/L、/E、/F、/M、/A）は並列実装で高速になった（元に戻った）が、[TTL](../Page/Transistor-transistor_logic.md "wikilink")[ICを使用し](../Page/集積回路.md "wikilink")、DTLより安価になっている。現存するPDP-8の多くはこの世代の機種である。中でもPDP-8/Eは豊富な各種周辺機器が接続可能で、よく使われていた。汎用コンピュータとしてもよく使われていた。

1975年、安価な[マイクロプロセッサ](../Page/マイクロプロセッサ.md "wikilink")を使った [Altair 8800](https://ja.wikipedia.org/wiki/Altair_8800 "wikilink") などの初期のパーソナルコンピュータが登場し、その後 [TRS-80](../Page/TRS-80.md "wikilink") や [Apple II](../Page/Apple_II.md "wikilink") が登場すると、小型汎用コンピュータの市場はそれらに奪われることになった。

1979年にリリースされた PDP-8 の最後の機種は特製の[CMOS](../Page/CMOS.md "wikilink")マイクロプロセッサを使用しており、"CMOS-8s" などと呼ばれた。価格は他のマイクロプロセッサを使ったコンピュータと競合するような設定ではなく、市場には受け入れられなかった。1981年に登場した [IBM PC](https://ja.wikipedia.org/wiki/IBM_PC "wikilink") がCMOS-8sにとどめを刺した。[インターシル](https://ja.wikipedia.org/wiki/インターシル "wikilink")がこの集積回路を1982年まで [Intersil 6100](https://ja.wikipedia.org/wiki/:en:Intersil_6100 "wikilink") として販売していた。CMOSであるため低電力であり、いくつかの軍用[組み込みシステム](../Page/組み込みシステム.md "wikilink")に採用された。

## 概要

技術史的観点からもPDP-8は重要な位置を占めている。[入出力](../Page/入出力.md "wikilink")機構、[ソフトウェア](../Page/ソフトウェア.md "wikilink")開発、[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink")設計などに影響を与えた。[Apple IIのような](../Page/Apple_II.md "wikilink")[マイクロコンピュータ](../Page/マイクロコンピュータ.md "wikilink")が一般化するまで、PDP-8は世界で最も販売台数の多いコンピュータであった。

PDP-8はいくつかの12ビット機の先例を参考にしており、特に [W.A. Clark](https://ja.wikipedia.org/wiki/:en:Wesley_A._Clark "wikilink") と [C.E. Molnar](https://ja.wikipedia.org/wiki/:en:Charles_Molnar "wikilink") が設計した[LINC](https://ja.wikipedia.org/wiki/LINC "wikilink")に影響を受けている。LINC自体は、[シーモア・クレイ](../Page/シーモア・クレイ.md "wikilink")が設計したミニコンピュータ [CDC 160](https://ja.wikipedia.org/wiki/:en:CDC_160A "wikilink") に影響を受けている\[3\]。

単純な (PIO) バスを備え、それに加えて[DMAチャネルがある](../Page/Direct_Memory_Access.md "wikilink")。PIOバスは、[プリンター](https://ja.wikipedia.org/wiki/プリンター "wikilink")、[テレタイプ端末](../Page/テレタイプ端末.md "wikilink")、[紙テープ](../Page/紙テープ.md "wikilink")パンチ/リーダーといった低速から中速の周辺機器を接続するのが一般的で、一方DMAは[ライトペン](../Page/ライトペン.md "wikilink")付きの[ブラウン管](../Page/ブラウン管.md "wikilink")スクリーン、[アナログ-デジタル変換回路](../Page/アナログ-デジタル変換回路.md "wikilink")、[デジタル-アナログ変換回路](../Page/デジタル-アナログ変換回路.md "wikilink")、[磁気テープドライブ](https://ja.wikipedia.org/wiki/テープドライブ "wikilink")、[ディスクドライブ](../Page/ディスクドライブ.md "wikilink")などで使用する。

[ワード](../Page/ワード.md "wikilink")長は12ビットで、符号なし整数で0から4095までの範囲を扱え、単純な機械の制御には十分である。また、符号付整数なら -2048 から +2047 まで扱える。これは[計算尺](../Page/計算尺.md "wikilink")より高精度だし、多くの[アナログコンピュータ](https://ja.wikipedia.org/wiki/アナログコンピュータ "wikilink")にも引けを取らない。12ビットはまた、[ASCII](https://ja.wikipedia.org/wiki/ASCII "wikilink")のサブセットを6ビットで表せば、1ワードに2文字を格納できる。

コスト削減のため、他のコンピュータなら[フリップフロップ](../Page/フリップフロップ.md "wikilink")で構成するレジスタも安価な主記憶を使う設計になっていた\[4\]。

PDP-8の基本構成では、主記憶容量は4,096[ワード](../Page/ワード.md "wikilink")で、オプションのメモリ拡張ユニットでさらに拡張する場合は、後述のIOT命令で[バンク切り換え](../Page/バンク切り換え.md "wikilink")をして使用する。

当初、ソフトウェアから見てPDP-8は8種類の[命令しかなく](https://ja.wikipedia.org/wiki/命令セット "wikilink")、[レジスタも](../Page/レジスタ_\(コンピュータ\).md "wikilink")2本（12ビットの[アキュムレータ](https://ja.wikipedia.org/wiki/アキュムレータ_\(コンピュータ\) "wikilink") AC と[キャリービットに相当するリンクレジスタ](https://ja.wikipedia.org/wiki/ステータスレジスタ#キャリー "wikilink") L）しか持たない。主記憶は[磁気コアメモリ](../Page/磁気コアメモリ.md "wikilink")でクロックサイクルは1.5μ秒である。典型的には1命令で命令とデータにアクセスするため2サイクルかかり、性能は0.333[MIPS](https://ja.wikipedia.org/wiki/MIPS "wikilink")となる。1974年の Pocket Reference Card では基本命令実行時間は1.2μ秒、メモリ参照命令の場合は2.6μ秒となっている。後期の機種では新たなレジスタが追加され(積/商レジスタ、MQ)、乗算命令と除算命令が追加された。

PDP-8は設計の単純さを重視して設計が最適化されている。直列化ALUを採用したPDP-8/Sでは、[論理ゲート](https://ja.wikipedia.org/wiki/論理ゲート "wikilink")を519個しか使っていない。2008年現在、最も規模の小さいマイクロコントローラでも1万5千ゲート以上使っている。他のマシンと比較すると必須ではない部分がそぎ落とされ、可能な限り論理回路を共用する設計になっている。命令は自動インクリメントや自動クリアや間接アクセスを利用して性能向上を図りつつメモリ使用量を削減している。PDP-8のCPUには12ビットレジスタが4本しかない（アキュムレータ、プログラムカウンタ、メモリバッファレジスタ、メモリアドレスレジスタ）。これらのレジスタは処理サイクルの各時点で様々な用途に使われている。例えば、メモリバッファレジスタは算術演算のオペランドを供給し、[磁気コアメモリ](../Page/磁気コアメモリ.md "wikilink")に書き出すべきデータを一時的に保持する（また、磁気コアメモリからの読み出しで破壊されたデータを書き戻すのにも使われる）。このように基本は単純にも関わらず、モジュールを小型化するために価格は高くなった。PDP-8/Sは電源電圧を2種類使っているが、これは [diode-transistor logic](https://ja.wikipedia.org/wiki/diode-transistor_logic "wikilink") (DTL) での[ファンアウト数を大きくする安価な技法である](https://ja.wikipedia.org/wiki/デジタル回路#ファン・アウト "wikilink")\[5\]。

## PDP-8のバージョン

[thumb前面の外観](https://ja.wikipedia.org/wiki/ファイル:PDP_8_e_Trondheim.jpg "wikilink")。全容を撮したもの。PDP-8より格段に薄型化した。）\]\] [PDPシリーズ](../Page/PDPシリーズ.md "wikilink")のベストセラーPDP-8ファミリーの総売上台数は300,000台を超えると推定されている。以下のような機種が製造された。

  - PDP-8 - 16,000ドル、机上据え置き型

  -
  - PDP-8/S - Small （PDP-8の次機種。小型化[IC化前PDPシリーズ最後のトランジスタ回路機](../Page/集積回路.md "wikilink")、驚異の「1万＄コンピュータ」と言われた画期的低価格で日米欧市場で歓迎された。ラックマウント型。）

  - PDP-8/I - PDPシリーズ初[IC化](../Page/集積回路.md "wikilink")

  - PDP-8/L - Low Cost

  - PDP-12

  - PDP-8/E - Economy（外観寸法は8/Sと同じ）。日本では[1970年](https://ja.wikipedia.org/wiki/1970年 "wikilink")に[理経](https://ja.wikipedia.org/wiki/理経 "wikilink")産業より$4,990（、4kワード、TTY無）で発売\[6\]。

  - PDP-8/F

  - PDP-8/M

  - PDP-8/A

  - [Intersil](https://ja.wikipedia.org/wiki/インターシル "wikilink") [6100](https://ja.wikipedia.org/wiki/:en:Intersil_6100 "wikilink") はシングルチップのPDP-8互換[マイクロプロセッサ](../Page/マイクロプロセッサ.md "wikilink")（VT78端末に使われた）

  - Harris 6120 は、CMOS版シングルチップのPDP-8互換マイクロプロセッサ（ワープロ機DECmateに使われた）

### 後の実装例

PDP-8のアーキテクチャは非常に単純なので、それをエミュレートするのは容易である。愛好家がPDP-8全体を1個の[FPGA](../Page/FPGA.md "wikilink")で実装した例もある。

インターネット上にはPDP-8をシミュレート/エミュレートするソフトウェアもいくつか存在する。うまく実装されたものはDECのOSや診断プログラムを実行可能である。後期のPDP-8に可能な限りの周辺機器を接続した状態をシミュレートすることが多い。そこまでしても、現代のパーソナルコンピュータのリソースのほんの一部しか占めない。

## 入出力

I/O（[入出力](../Page/入出力.md "wikilink")）システムはPDP-8の頃に大きな変化を迎えた。初期のPDP-8の入出力は、フロントパネル、[紙テープ](../Page/紙テープ.md "wikilink")リーダー、[テレタイププリンタ](../Page/テレタイプ端末.md "wikilink")（[ASR-33](../Page/ASR-33.md "wikilink")/KSR-33）、そしてオプションの紙テープパンチャーで構成されていた。その後、[磁気テープ](../Page/磁気テープ.md "wikilink")、[RS-232](../Page/RS-232.md "wikilink")Cなどによるダム(dumb)[端末](../Page/端末.md "wikilink")、[パンチカード](https://ja.wikipedia.org/wiki/パンチカード "wikilink")リーダー、固定ヘッド式磁気ディスク装置などが追加されていった。最後のころには[フロッピーディスク](../Page/フロッピーディスク.md "wikilink")や[ハードディスク](https://ja.wikipedia.org/wiki/ハードディスク "wikilink")が一般的になっていた。最近 の愛好家は[IDEアダプターを](../Page/Advanced_Technology_Attachment.md "wikilink")（本物あるいはシミュレートされた）PDP-8に接続している。

I/Oは以下のようないくつかの手段でサポートされている:

  - [バックプレーン](../Page/バックプレーン.md "wikilink")上の専用I/Oコントローラ
  - "Negative" I/Oバス(Lo電圧が1)
  - "Positive" I/Oバス(Hi電圧が1)
  - Omnibus（専用でないバックプレーン上のスロット） がPDP-8/Eで導入された。

基本的な[DMA方式](../Page/Direct_Memory_Access.md "wikilink") (three-cycle data break) がサポートされている。これにはプロセッサの支援が必要だった。本来ならば各I/Oデバイスが持つべき回路を共通化してプロセッサ側に置き、プロセッサがDMAアドレスレジスタとワードカウントレジスタを設定する。その後の3メモリサイクルでプロセッサはワードカウントを更新し、転送アドレスを更新し、最後に実際のI/Oデータワードをやりとりする。初期のPDP-8から備えられていた機能であるが、PDP-8/Eのころにはこの回路は非常に安価になったので、"one-cycle data break"が一般化した。これは個々のI/Oデバイス側に[ハードウェア](../Page/ハードウェア.md "wikilink")によるDMAアドレスレジスタとワードカウントレジスタを持たせ、[ディスクドライブ](../Page/ディスクドライブ.md "wikilink")や[磁気テープ](../Page/磁気テープ.md "wikilink")など高速I/Oデバイスと[メモリ間でプロセッサを介さず直接メモリへの読み](../Page/記憶装置.md "wikilink")・書きをするDMAを行うものであり、実質3倍の[転送](https://ja.wikipedia.org/wiki/転送 "wikilink")性能となった。

## プログラミング環境

PDP-8の最も基本的な[ソフトウェア](../Page/ソフトウェア.md "wikilink")開発システムは、[機械語](../Page/機械語.md "wikilink")を[バイナリ](../Page/バイナリ.md "wikilink")形式でフロントパネルから入力するものであった。その後、PAL-8[アセンブリ言語](../Page/アセンブリ言語.md "wikilink")の[ソースコード](../Page/ソースコード.md "wikilink")を紙テープに格納し、[メモリにロードし](../Page/主記憶装置.md "wikilink")、紙テープにセーブし、紙テープからアセンブルされてメモリに格納されるようになった。紙テープ方式の[プログラミング言語](../Page/プログラミング言語.md "wikilink")としては他に [FOCAL](https://ja.wikipedia.org/wiki/:en:FOCAL_\(programming_language\) "wikilink") [インタプリタ](../Page/インタプリタ.md "wikilink")や 4K [FORTRAN](../Page/FORTRAN.md "wikilink")[コンパイラ](../Page/コンパイラ.md "wikilink")などがある。最終的には OS/8 や COS-310 といった[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink")によって、[ラインエディタ](https://ja.wikipedia.org/wiki/ラインエディタ "wikilink")やコマンドライン[コンパイラ](../Page/コンパイラ.md "wikilink")といった開発システムが構築された。サポート言語としては、PAL-IIIアセンブリ言語、[FORTRAN](../Page/FORTRAN.md "wikilink")、[BASIC](../Page/BASIC.md "wikilink")、[DIBOLなどがある](https://ja.wikipedia.org/wiki/:en:DIBOL "wikilink")。

初期のPDP-8システムには[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink")がなく、フロントパネルのスイッチしかなかった。様々な紙テープ式「オペレーティングシステム」が開発されたが、いずれもシングルユーザー方式であった。最後期には先進的な[RTOSや](../Page/リアルタイムオペレーティングシステム.md "wikilink")[プリエンプティブ・マルチタスク](https://ja.wikipedia.org/wiki/プリエンプション "wikilink")/マルチユーザーシステムが利用可能となった。例えば RTOSの RTS-8、マルチユーザーシステムの COS-300 や COS-310、シングルユーザー用ワードプロセッシングシステム WPS-8 などがある。

[タイムシェアリングシステム](../Page/タイムシェアリングシステム.md "wikilink") [TSS-8](https://ja.wikipedia.org/wiki/:en:TSS-8 "wikilink") も使用可能であった。TSS-8 では複数のユーザーが110ボーの端末からシステムにログインすることができ、[プログラムのエディット](../Page/プログラム_\(コンピュータ\).md "wikilink")/[コンパイル](../Page/コンパイラ.md "wikilink")/[デバッグ](../Page/デバッグ.md "wikilink")が同時にできた。言語としては、[BASIC](../Page/BASIC.md "wikilink")の特別バージョン、FORTRANのサブセット([サブルーチン](https://ja.wikipedia.org/wiki/サブルーチン "wikilink")を書けない)、[ALGOL](../Page/ALGOL.md "wikilink")のサブセット版、FOCAL、PAL-Dアセンブラなどが利用可能である。

[DECUS](https://ja.wikipedia.org/wiki/:en:DECUS "wikilink") (Digital Equipment Computer User Society) はPDP-8用にユーザーが寄贈した相当量のソフトウェアを保有している。

## 命令セット

12ビットの命令ワードの先頭3ビット（ビット0から2）が命令コードである。ビット5から11までの7ビットのオフセット部でアクセスするメモリを示す。ビット4がセットされていたら、[プログラムカウンタ](https://ja.wikipedia.org/wiki/プログラムカウンタ "wikilink") (PC) の上位5ビットとオフセットを連結してアドレスを完成させる。そのビットがゼロならアドレスの上位はゼロとする。ビット3は間接かどうかを示す。セットされていたら、それまでに得られたアドレスはメモリ上にある実効アドレスのある位置を示していることになる。[JMP命令は](https://ja.wikipedia.org/wiki/分岐命令 "wikilink")、間接指定されていない場合はメモリワードを読み込むわけではないが、命令のフォーマットは同じである。

|           |   |   |        |   |   |  |  |  |  |  |    |
| --------- | - | - | ------ | - | - |  |  |  |  |  | -- |
| 0         |   | 2 | 3      | 4 | 5 |  |  |  |  |  | 11 |
| Operation | I | Z | Offset |   |   |  |  |  |  |  |    |

### メモリページ

このように命令はアドレスの下位7ビットだけを直接指定するので、4,096ワードのメモリは128ワードの「ページ」に分割されることになり、命令のビット4でカレントページかページ0（アドレス範囲を[八進法](https://ja.wikipedia.org/wiki/八進法 "wikilink")で示すと 0000 から 0177）を指定する。ページ0に変数を置くと、どのページを実行中でもそれにアクセスできるため、ページ0のメモリは特別である。また、アドレス 0000 は割り込み処理ルーチンのスタートアドレスでもある。また、アドレス 0010 から 0017 までは自動インクリメント機構という特殊性がある。

標準的アセンブラは算術用定数をカレントページに置く。同様に、ページ間ジャンプやサブルーチンコールはカレントページ内から間接アドレス指定で行う（つまりアドレスがカレントページ内に置かれている）。

ページをまたいだ参照や分岐は余分なワードを必要とするため、ルーチンを128ワードのページ境界に収まるように書くか、なるべくページからページへの移行が少なくなるように書くことが重要だった。そのため、何ワードかをいかに節約するかに頭を悩ませることが多かった。PCのインクリメントで自動的に次のページに移行できるため、プログラムを意図的にページの最後尾に置くことが多かった。

### 基本命令

  -
    000 - AND - メモリオペランドと AC の [AND](https://ja.wikipedia.org/wiki/ビット演算 "wikilink") （ACは[アキュムレータの略](https://ja.wikipedia.org/wiki/アキュムレータ_\(コンピュータ\) "wikilink")）
    001 - TAD - メモリオペランドと \<L,AC\>（ACのビット値とLのキャリー）の[加算](https://ja.wikipedia.org/wiki/加法 "wikilink")（[2の補数](../Page/2の補数.md "wikilink")とみなす、つまり符号付）
    010 - ISZ - メモリオペランドをインクリメントし、結果がゼロならば次の命令をスキップする
    011 - DCA - ACをメモリオペランド位置に保存し、ACをクリアする
    100 - JMS - [サブルーチン](https://ja.wikipedia.org/wiki/サブルーチン "wikilink")へジャンプ(サブルーチンの先頭ワードにリターンアドレスを保持する)
    101 - JMP - ジャンプ
    110 - IOT - 入出力転送（後述）
    111 - OPR - マイクロコード化操作（後述）

### IOT（入出力転送）命令

PDP-8はIOT命令をほとんど定義せず、単に枠組みを提供している。多くのIOT命令がどう作用するかは個々の周辺機器によって異なる。

|       |        |          |   |  |  |  |  |   |   |  |    |
| ----- | ------ | -------- | - |  |  |  |  | - | - |  | -- |
| 0     |        | 2        | 3 |  |  |  |  | 8 | 9 |  | 11 |
| 6=IOT | Device | Function |   |  |  |  |  |   |   |  |    |

  - Device
    IOT命令のビット3からビット8でI/Oデバイスを指定する。一部は利便性のために標準化されていた。
      - 00 - プロセッサが処理し、I/Oデバイスには送られない。例えば ION (6001) は割り込み処理のイネーブル、IOFF (6002) は同処理のディセーブルである。
      - 01 - 通常、高速紙テープリーダー
      - 02 - 高速紙テープパンチ
      - 03 - コンソールのキーボード（および付属する低速紙テープリーダー）
      - 04 - コンソールのプリンター（および付属する低速紙テープパンチ）
  - Function
    IOT命令のビット9からビット11までで、そのデバイスで実行すべき機能を指定する。紙テープリーダー/パンチやコンソールなどの単純な機器では、次のように解釈する。
      - ビット11 - 指定した周辺機器がレディ状態なら次の命令をスキップする。
      - ビット10 - AC をクリア
      - ビット9 - その周辺機器とACの間で1ワードを転送し、次のI/O転送を開始し、機器のレディフラグを落とす。
    複数のビットをセットすると、適切な順序でそれらが行われる。
    ディスクドライブなどのより複雑な周辺機器では、それぞれ固有の機能をこの3ビットで表す。一般に8種類の機能コードを設定できる。

### OPR (OPeRate) 命令

条件付き操作のほとんどを含め、多くの操作はOPR命令として実行される。OPR命令ではメモリ位置をアドレスで示すということがない。条件付き操作は1命令をスキップするか否かを判断する命令であり、通常はその1命令をJMP命令とすることで条件分岐として機能させる。

OPR命令はマイクロコード化されている。これは[マイクロプログラム方式](../Page/マイクロプログラム方式.md "wikilink")だということを意味しているのではなく、命令語の各ビットがそれぞれ特定の動作に対応しており、複数のビットをセットすることでそれらを1命令で実行できる場合があることを意味している。アセンブリ言語で記述する際には複数のニーモニックを並列に書く。するとアセンブラがそれらのコードを[ORして](../Page/論理和.md "wikilink")1命令にする。上述のIOT命令も周辺機器がマイクロコード化している。

マイクロコード化された動作の実行順序は決まっており、多くの組合せが最も便利になるような順序で実行される。

OPR命令にはいくつかのグループがある。ビット3、ビット8、ビット11 でグループが識別され、異なるグループのマイクロコード化操作は1命令で指定できない。

#### グループ1

`           00 01 02 03 04 05 06 07 08 09 10 11`
`           ___________________________________`
`          | 1| 1| 1| 0|  |  |  |  |  |  |  |  |`
`          |__|__|__|__|__|__|__|__|__|__|__|__|`
`                      |CLA   CMA   RAR   BSW`
`                          CLL   CML   RAL   IAC`
`  `
`       Execution order  1  1  2  2  4  4  4  3`

  -
    7200 – CLA - AC クリア
    7100 –­ CLL - L ビットのクリア
    7040 – CMA - ACの 1の補数
    7020 – CML - L ビットの反転
    7010 – RAR - \<L,AC\> の右ローテート
    7004 – RAL - \<L,AC\> の左ローテート
    7002 – BSW – 6ビットの「バイト」のバイトスワップ（PDP-8/E以降）
    7001 – IAC - \<L,AC\>のインクリメント
    7012 – RTR - \<L,AC\> の右ローテート(2回)
    7006 – RTL - \<L,AC\> の左ローテート(2回)

多くの場合操作は順次行われ、多くの組合せが最も便利な形で可能である。例えば CLA (CLear Accumulator) と CLL (CLear Link) と IAC (Increment ACcumulator) を組み合わせると、まずACとLINKをクリアし、次にアキュムレータをインクリメントするので、ACの値は1になる。これにさらに RAL を加えると、アキュムレータをクリアし、インクリメントし、左にローテートするので、ACの値は2になる。このようにしてアキュムレータに小さい整数定数を1命令で置くことができる。

CMAとIACを組み合わせると、アセンブラではこれをCIAと略記できるが、ACの値を算術的に符号反転できる（つまり、2の補数）。PDP-8には減算命令がなく符号付加算命令 (TAD) しかないので、2つの数の差を求めるには一方の数の符号を反転させるしかない。

グループ1のOPR命令で、マイクロコード化されたビットを全くセットしない場合、何も行われない。そういった命令を[NOP](../Page/NOP.md "wikilink")命令として使用することができる。

#### グループ2、Orグループ

`           00 01 02 03 04 05 06 07 08 09 10 11`
`           ___________________________________`
`          | 1| 1| 1| 1|  |  |  |  | 0|  |  | 0|`
`          |__|__|__|__|__|__|__|__|__|__|__|__|`
`                      |CLA   SZA      OSR`
`                          SMA   SNL      HLT`
`  `
`                        2  1  1  1    3  3`

  -
    7600 – CLA - ACをクリア
    7500 – SMA - AC \< 0 のとき次命令をスキップ (or group)
    7440 – SZA - AC = 0 のとき次命令をスキップ (or group)
    7420 – SNL - L ≠ 0 のとき次命令をスキップ (or group)
    7404 – OSR - ACとフロントパネルスイッチの間の[論理和](https://ja.wikipedia.org/wiki/ビット演算 "wikilink")
    7402 – HLT - 停止

ビット8がセットされていない場合、指定された条件のいくつかが真ならばスキップを行う（条件はORされる）。例えば、"SMA SZA" 命令コード 7540 の場合、AC ≤ 0 ならスキップする。

グループ2のOPR命令もマイクロコード化ビットが全くセットされていない場合、NOP命令として扱われる。

#### グループ2、Andグループ

`           00 01 02 03 04 05 06 07 08 09 10 11`
`           ___________________________________`
`          | 1| 1| 1| 1|  |  |  |  | 1|  |  | 0|`
`          |__|__|__|__|__|__|__|__|__|__|__|__|`
`                      |CLA   SNA      OSR`
`                          SPA   SZL      HLT`
`  `
`                        2  1  1  1    3  2`

  -
    7410 – SKP - 無条件に次命令をスキップ
    7610 – CLA – ACをクリア
    7510 – SPA - AC \>= 0 のとき次命令をスキップ (and group)
    7450 – SNA - AC ≠ 0 のとき次命令をスキップ (and group)
    7430 – SZL - L = 0 のとき次命令をスキップ (and group)

ビット8がセットされている場合、スキップ条件はOrグループのときと逆であり、いずれかの条件が真でないときスキップは行わない。つまり、指定された条件が全て真となる必要がある（条件はANDされる）。例えば "SPA SNA" 命令コード 7550 は AC \> 0 のときスキップする。ビット5からビット7が全くセットされない場合、無条件でスキップする。

#### グループ3

これまでのグループで使われていないビットの組合せのOPR命令はグループ3に分類され、多くは MQ (Multiplier/Quotient) レジスタに関連する。

`           00 01 02 03 04 05 06 07 08 09 10 11`
`           ___________________________________`
`          | 1| 1| 1| 1|  |  |  |  |  |  |  | 1|`
`          |__|__|__|__|__|__|__|__|__|__|__|__|`
`                      |CLA   SCA   _    _/`
`                      |   MQA   MQL  CODE`
`  `
`                        1* 2  2  2     3`

  -
    7601 – CLA – ACをクリア
    7501 – MQA – Multiplier/Quotient を AC に[ORする](../Page/論理和.md "wikilink")
    7441 – SCA – ステップカウンタをACにロード
    7421 – MQL – AC を Multiplier/Quotient にロードし、ACをクリア
    7621 – CAM – CLA + MQL なので、ACとMQを共にクリア

通常、CLAとMQAを組み合わせてMQの中身をACに転送する。MQAとMQLの組合せも便利で、ACとMQの中身を交換する。

ビット8からビット10までの3ビットで以下のいずれかの命令が実行される。

  -
    7401 – 何もしない
    7403 – SCL – ACからステップカウンタへのロード（即値ワードが後置される。PDP-8/Iかそれ以降）
    7405 – MUY – 乗算
    7407 – DVI – 除算
    7411 – NMI – 正規化
    7413 – SHL – 左シフト（即値ワードが後置される）
    7415 – ASR – 算術右シフト
    7417 – LSR – 論理右シフト

## メモリ制御

[thumb](https://ja.wikipedia.org/wiki/ファイル:PDP-8I-core.jpg "wikilink") 12ビットワードは4,096種類の値をとることができ、それは最初のPDP-8がワードポインタで間接的にアドレス指定できる最大のワード数でもあった。プログラムが複雑化し、メモリ価格が下落してくると、この制限を拡張することが望ましくなってきた。

既存プログラムとの互換性を保つため、当初設計になかった新ハードウェアはプログラムが生成する実効アドレスにさらに上位のビット群を追加した。メモリ拡張コントローラはアドレス指定範囲を8倍にし、32,768ワードまで扱えるようにした。当時の磁気コアメモリは1ワード当たり50セントのコストであり、32Kワードを実装するとCPUと同程度のコストになるため、この程度の拡張で十分だとされた。

4Kワードぶんのメモリをフィールドと呼ぶ。メモリ拡張コントローラは、DF (Data Field) と IF (Instruction Field) という2つの3ビットレジスタを備えている。それらのレジスタはデータアクセスや命令フェッチの際にどのフィールドにアクセスするかを指定するもので、アドレスは実質15ビットに拡張される。IFレジスタは命令フェッチと直接メモリ参照の際のフィールドを指定する。DFレジスタは間接データアクセスの際のフィールドを指定する。あるフィールドで動作中のプログラムは、直接アドレッシングでは同じフィールドにアクセスし、間接アドレッシングでは別のフィールドにアクセスできる。

IOT命令の 6200 から 6277 までの範囲がメモリ拡張コントローラに対応しており、DFレジスタとIFレジスタへのアクセスが可能である。62X1 命令 (CDF, Change Data Field) はDFレジスタの値をXにする。同様に62X2 (CIF) 命令はIFレジスタの値をXに、62X3 命令は両方をXにセットする。既存プログラムはCIFもCDFも実行しない。DFもIFも同じフィールドを指すので、既存プログラムは単一フィールドだけで動作する。CIF命令の効果は、次のJMPまたはJMS命令まで遅延されるので、CIF命令によって即座にジャンプするわけではない。

フィールド境界とDF/IFレジスタの関係を考えると、複数フィールドを使うプログラムはさらに複雑化する。単純に15ビットのアドレスを生成するのではなく、12ビット・アーキテクチャとの一貫性と互換性を保つよう設計されているためである。後の [Intel 8086](../Page/Intel_8086.md "wikilink") では、[Intel 8080](../Page/Intel_8080.md "wikilink") で16ビットだったアドレスを20ビットに拡張したが、拡張部分は[セグメントレジスタで指定する方式だった](../Page/セグメント方式.md "wikilink")。

このメモリ拡張方式により、既存のプログラムを少し修正するだけで扱えるメモリ範囲を拡大することができた。例えば、4K [FOCAL](https://ja.wikipedia.org/wiki/:en:FOCAL_\(programming_language\) "wikilink") は、自身のコードが3Kあってユーザープログラムやデータに使えるメモリは1Kしかなかった。そのFOCALに若干パッチを当てるだけで、ユーザープログラムとデータに別の4Kフィールドを割り当てることができる。さらに、4Kフィールドを別のユーザーに割り当てることもでき、マルチユーザーのタイムシェアリングシステムを構成できる。

### 仮想化

PDP-8/Eとその後の機種では、メモリ拡張コントローラは[仮想化](../Page/仮想化.md "wikilink")も可能なように拡張された。PDP-8の全リソースを使用するようなプログラムが1台のPDP-8上に複数並存でき、仮想機械マネージャの制御下で動作可能だった。このマネージャは（メモリ拡張コントローラの操作も含む）全IO命令に対してトラップが可能である（割り込みを起こしてマネージャがそれを処理できる）。そのようにしてマネージャがデータや命令のフィールドのマッピングを制御でき、入出力を他のデバイスにリダイレクトできる。それぞれのゲストプログラムは、マネージャが提供する「仮想機械」への完全なアクセスを持つ。

新たなIOT命令で、メモリ拡張コントローラのDF/IFレジスタの現在値を読み出すことができ、トラップ前後のマシンの状態をセーブ/リストアできる。しかし、CIF命令の効果が遅延している状態（CIF命令を実行後、最初の分岐を行うまでの状態）かどうかは判別できない。マネージャは完全なPDP-8エミュレータを含んでいる必要がある（8命令のマシンなので難しくはない）。CIF命令をトラップした際、マネージャは次のジャンプ命令までの命令列をエミュレートする必要がある。実際、ジャンプ命令はCIF命令の直後にあるのが一般的で、エミュレーションで性能が大きく低下することはないが、小さな設計上の欠陥への対策としては大きい。

PDP-8/Aのころメモリ価格はさらに下落し、32Kワード以上も可能なレベルとなった。そこでPDP-8/Aでは8フィールド以上を扱える新たな命令群が追加された。フィールド番号は命令に[ハードコーディング](https://ja.wikipedia.org/wiki/ハードコーディング "wikilink")されるのではなく、ACで指定できるようになった。しかし、そのころにはPDP-8は市場から消えつつあり、この新機能を使うよう修正された主要ソフトウェアはごく一部だけだった。

## コーディング例

PDP-8の[アセンブリ言語](../Page/アセンブリ言語.md "wikilink")[プログラムを例として示す](../Page/プログラム_\(コンピュータ\).md "wikilink")。以下のコード例はPAL-IIIアセンブラによる。

### 2つの数の比較

単に2つの数を比較するだけでどれだけのコードが必要となるかを示したコード断片。

<code>

`   /Compare numbers in memory at OPD1 and OPD2`
`           CLA CLL     /Must start with 0 in AC and link`
`           TAD OPD1    /Load first operand into AC (by adding it to 0); link is still clear`
`           CIA         /Complement, then increment AC, negating it`
`           TAD OPD2    /AC now has OPD2-OPD1; if OPD2≥OPD1, sum overflows and link is set`
`           SZL         /Skip if link is clear`
`           JMP OP2GT   /Jump somewhere in the case that OPD2≥OPD1;`
`                       /Otherwise, fall through to code below.`

</code>

見ての通り、PDP-8の典型的なプログラムは作者が意図したアルゴリズムよりも低レベルな機構に集中する傾向がある。また、可読性を損なうもう1つの問題として、条件分岐部分のコーディングがある。上の例で判るとおり条件判断命令（JMP命令をスキップしている命令）は、注目している条件とは反対の条件判断をしなければならない。

### 文字列出力

PDP-8で ["Hello, world"](../Page/Hello_world.md "wikilink") をテレタイプ端末に出力するアセンブリ言語のプログラム。

<code>

`   *10                   / Set current assembly origin to address 10,`
`   STPTR,    STRNG-1     / An auto-increment register (one of eight at 10-17)`
` `
`   *200                  / Set current assembly origin to program text area`
`   HELLO,  CLA CLL       / Clear AC and Link again (needed when we loop back from tls)`
`           TAD I Z STPTR / Get next character, indirect via PRE-auto-increment address from the zero page`
`           SNA           / Skip if non-zero (not end of string)`
`           HLT           / Else halt on zero (end of string)`
`           TLS           / Output the character in the AC to the teleprinter`
`           TSF           / Skip if teleprinter ready for character`
`           JMP .-1       / Else jump back and try again`
`           JMP HELLO     / Jump back for the next character`
` `
`   STRNG,  310           / H`
`           345           / e`
`           354           / l`
`           354           / l`
`           357           / o`
`           254           /,`
`           240           / (space)`
`           367           / w`
`           357           / o`
`           362           / r`
`           354           / l`
`           344           / d`
`           241           / !`
`           0             / End of string`
`   $HELLO                /DEFAULT TERMINATOR`

</code>

### サブルーチン

PDP-8では汎用[スタック](../Page/スタック.md "wikilink")を[アーキテクチャ上サポートしていないため](../Page/コンピュータ・アーキテクチャ.md "wikilink")、[サブルーチン](https://ja.wikipedia.org/wiki/サブルーチン "wikilink")を呼び出すときや[割り込みが発生したときのコンテキスト](../Page/割り込み_\(コンピュータ\).md "wikilink")(プログラムカウンタやACなどのレジスタ値)をセーブする方法が確立されていない。その代わり、リターンアドレスとしてのプログラムカウンタ値がターゲットサブルーチンの先頭[ワード](../Page/ワード.md "wikilink")に格納される。従って、間接ジャンプ命令でサブルーチンから戻ることができる。

以下のプログラムはサブルーチンを使うように改造した "Hello world" である。JMS命令でサブルーチンに飛び込むと、OUT1:の位置にある0が書き換えられる。

<code>

`   *200                    / Set assembly origin (load address)`

`   HELLO,  CLA CLL         / Clear the AC and the Link bit`
`           TAD (DATA-1)    / Point AC just *BEFORE* the data (accounting for later pre-increment behavior)`
`           DCA 10          / Put that into one of ten auto-pre-increment memory locations`
`   LOOP,   TAD I 10        / Pre-increment mem location 10, fetch indirect to get the next character of our message`
`           SNA             / Skip on non-zero AC`
`           HLT             / Else halt at end of message`
`           JMS OUT1        / Write out one character`
`           JMP LOOP        / And loop back for more`

`   OUT1,   0               / Will be replaced by caller's updated PC`
`           TSF             / Skip if printer ready`
`           JMP .-1         / Wait for flag`
`           TLS             / Send the character in the AC`
`           CLA CLL         / Clear AC and Link for next pass`
`           JMP I OUT1      / Return to caller`

`   DATA,  "H               / A well-known message`
`          "e               /`
`          "l               / NOTE:`
`          "l               /`
`          "o               /   Strings in PAL-8 and PAL-III were "sixbit"`
`          ",               /   To use ASCII, we'll have to spell that out, character by character`
`          "                /`
`          "w               /`
`          "o               /`
`          "r               /`
`          "l               /`
`          "d               /`
`          "!               /`
`          015              /`
`          012              /`
`          0                / Mark the end of our .ASCIZ string ('cause .ASCIZ hadn't been invented yet!)`

</code>

[リエントラント](../Page/リエントラント.md "wikilink")性や[再帰呼び出し](https://ja.wikipedia.org/wiki/再帰呼び出し "wikilink")を実現しようとすると、[プログラマ](../Page/プログラマ.md "wikilink")は自分で[コールスタック](https://ja.wikipedia.org/wiki/コールスタック "wikilink")を用意し、リターンアドレスをスタックにセーブしなければならない。また、[ROMを使うのも困難である](https://ja.wikipedia.org/wiki/Read_Only_Memory "wikilink")(プログラムが書き換え可能でないとサブルーチンを使えないため)。ROMにプログラムを格納する場合、以下のような回避方法があった。

  - 実行時にはRAMにコピーする
  - RAMも一部内蔵したROMを使い、各ワードにフラグを設定してRAMを代替に使用するかどうかを指定する（要するに非常に特殊なメモリを使用する）。
  - サブルーチンを全く使わない。またはJMS命令の代わりに次のようなコードを使い、書き換え可能なメモリにリターンアドレスを置く。

<code>

`   JUMPL, DCA TEMP         / Deposit the accumulator in some temporary location`
`          TAD JUMPL+3      / Load the return address into the accumulator: hard coded`
`          JMP SUBRO        / Go to the subroutine, and have it handle jumping back`
`          JUMPL+4          / Return address`

</code>

JMS命令を使用すると[デバッグ](../Page/デバッグ.md "wikilink")が難しくなる。例えば、リターンアドレスの書き換えによって無限ループに陥ることもあるし、サブルーチンのアドレスを間違うとサブルーチンの先頭ではないワードをリターンアドレスで書き換えてしまうこともある。こういった誤りは実行してみないとわからないこともある。

### ソフトウェアスタック

PDP-8 は[スタック](../Page/スタック.md "wikilink")をハードウェアでサポートしていないが、ソフトウェアでの実装は可能である。以下はPUSHとPOPというサブルーチンの実装例だが、単純化するためスタックのオーバーフローやアンダーフローはチェックしていない。

<code>

`   PUSH, 0`
`         DCA DATA`
`         CLA CMA     / -1`
`         TAD SP`
`         DCA SP`
`         TAD DATA`
`         DCA I SP`
`         JMP I PUSH     /Return`

`   POP,  0`
`         CLA CLL`
`         TAD I SP`
`         ISZ SP`
`         JMP I POP`

`   DATA, 0`
`   SP, 0`

</code>

以下は、"Hello World" を "OUT" というサブルーチンとこのスタックを使って実装したものである。

<code>

`   *200`
`   MAIN,  CLA CLL         /Set the message pointer`
`          TAD (MESSG      /To the beginning of the message (literal)`
`          DCA SP`

`   LOOP,  JMS POP`
`          SNA             /Stop execution if zero`
`          HLT`
`          JMS OUT         /Otherwise, output a character`
`          JMP LOOP`

`   MESSG, "H`
`          "e`
`          "l`
`          "l`
`          "o`
`          ",`
`          "`
`          "w`
`          "o`
`          "r`
`          "l`
`          "d`
`          "!`
`          015`
`          012`
`          0`

`   OUT,    0               / Will be replaced by caller's updated PC`
`           TSF             / Skip if printer ready`
`           JMP .-1         / Wait for flag`
`           TLS             / Send the character in the AC`
`           CLA CLL         / Clear AC and Link for next pass`
`           JMP I OUT      / Return to caller`

</code>

### 連結リスト

PDP-8での[連結リスト](../Page/連結リスト.md "wikilink")の実装例。

<code>

`    GETN, 0     /Gets the number pointed to and moves the pointer`
`    CLA CLL     /Clear accumulator`
`    TAD I PTR   /Gets the number pointed to`
`    DCA TEMP    /Save current value`
`    ISZ    PTR     /Increment pointer`
`    TAD I PTR   /Get next address`
`    DCA PTR     /Put in pointer`
`    JMP I GETN  /return`
`    PTR,  0`
`    TEMP, 0`

</code>

## 割り込み

PDP-8の[入出力](../Page/入出力.md "wikilink")バスには1本の[割り込みラインがあり](../Page/割り込み_\(コンピュータ\).md "wikilink")、割り込みが発生すると割り込み不可状態となって 0番地の[サブルーチン](https://ja.wikipedia.org/wiki/サブルーチン "wikilink")を呼び出すように動作する。サブルーチンと同様、割り込みもリエントラント性は無く、割り込みを不可とした状態で[割り込みハンドラ](https://ja.wikipedia.org/wiki/割り込みハンドラ "wikilink")が動作し、`JMP I 0` 命令で割り込まれた箇所に戻るとき割り込み可とする。

I/Oバスの割り込みラインが1本なので、割り込み発生源が何かということは分からない。そのため、割り込み処理ルーチンは順に各デバイスのステータスをポーリングしてチェックし、割り込み元を識別した。この処理は条件スキップ[命令が並ぶので](../Page/命令_\(コンピュータ\).md "wikilink") "skip chain" と呼ばれた。skip chain の最後まで実行しても割り込み元が見つからないことは珍しいことではなかった。相対的な割り込みの優先順位は skip chain でチェックする順番で決定され、先に見つかった割り込みの処理が優先される。

## 脚注

## 参考文献

  -
## 外部リンク

  - [pdp-8 Documentation: The Small Computer Handbook (1966 Edition), Sections 1 and 2](http://highgate.comm.sfu.ca/pdp8/) and others are available from [Simon Fraser University](../Page/サイモンフレーザー大学.md "wikilink")

  - [PDP-8 Frequently Asked Questions](http://www.faqs.org/faqs/dec-faq/pdp8/), FAQS.ORG

  - [pdp8online.com](http://www.pdp8online.com/) has a running PDP8 that anyone can control through a Java applet, plus a webcam to show the results

  - [dpa](http://www.telegraphics.com.au/sw/#dpa) ポータブルなPDP-8クロスアセンブラ

  - [SBC6120](http://www.sparetimegizmos.com/Hardware/SBC6120-2.htm) PDP-8互換マシン販売サイト

  - [Still working Classic 8, PDP 8e and 8i](http://www.technikum29.de/en/computer/early-computers.shtm) in a German computer museum

  - [PDP-8/E Simulator](http://www.bernhard-baehr.de/pdp8e/pdp8e.html) for Macintosh (Bernhard Baehr)

  - Willem van der Mark's [PDP-8/E Simulator](http://www.vandermark.ch/pdp8/index.php?n=PDP8.Emulator) in Java

  - <http://simh.trailing-edge.com/> 各種OSで動作する非常にポータブルなPDP-8シミュレータ

  - [The Digital Equipment Corporation PDP-8, 1965](http://americanhistory.si.edu/collections/comphist/objects/pdp8.htm) - [スミソニアン博物館](../Page/スミソニアン博物館.md "wikilink")のコレクション

  - <http://www.pdp8.co.uk/> Blogs the restoration of PDP-8 computers

  - <http://www.grc.com/pdp-8/pdp-8.htm> Steve Gibson's explanation on how the PDP-8 works and how to program it.

  - [YouTube](http://www.youtube.com/watch?v=DPioENtAHuY&feature=related) has a video series showing the PDP-8

  -
[Category:ミニコンピュータ](https://ja.wikipedia.org/wiki/Category:ミニコンピュータ "wikilink") [Category:コンピュータ_(歴代)](https://ja.wikipedia.org/wiki/Category:コンピュータ_\(歴代\) "wikilink") [Category:コンピュータ史](https://ja.wikipedia.org/wiki/Category:コンピュータ史 "wikilink") [Category:ディジタル・イクイップメント・コーポレーション](https://ja.wikipedia.org/wiki/Category:ディジタル・イクイップメント・コーポレーション "wikilink") [Category:トランジスタ・コンピュータ](https://ja.wikipedia.org/wiki/Category:トランジスタ・コンピュータ "wikilink")

1.
2.  [The ultimate entrepreneur: the story of Ken Olsen and Digital Equipment Corporation](http://books.google.nl/books?id=S22mQgAACAAJ) entry in [Google Books](https://ja.wikipedia.org/wiki/Google_ブックス "wikilink"), by Glenn Rifkin, George Harrar, 1988, ISBN 978-1-55958-022-9
3.
4.
5.  PDP-8/S Maintenance Manual, DEC, 1971
6.  『Computer Report』Vol.10 No.10、日本経営科学研究所、1970年
> この記事は[CASL](https://ja.wikipedia.org/wiki/CASL)から翻訳されています。


**CASL**（キャスル）は、[情報処理技術者試験](../Page/情報処理技術者試験.md "wikilink")における[プログラミング能力試験のために](https://ja.wikipedia.org/wiki/プログラミング_\(コンピュータ\) "wikilink")、[CAP-X](../Page/CAP-X.md "wikilink")の後継として1986年仕様策定した[アセンブリ言語](../Page/アセンブリ言語.md "wikilink")である\[1\]。

## 概要

[第二種情報処理技術者試験](https://ja.wikipedia.org/wiki/第二種情報処理技術者試験 "wikilink")（現・[基本情報技術者試験](../Page/基本情報技術者試験.md "wikilink")）にはプログラミング能力試験という試験がある。この試験は幾つかの[プログラミング言語](../Page/プログラミング言語.md "wikilink")別に分かれており、受験者はそれぞれが最も得意とする言語による試験を選択することで、特定の言語のプログラマが有利になることを防いでいる。

この試験で使用する[アセンブリ言語](../Page/アセンブリ言語.md "wikilink")としてCASLを開発した。アセンブリ言語は[ハードウェア](../Page/ハードウェア.md "wikilink")の[アーキテクチャとの関連性が強い](../Page/コンピュータ・アーキテクチャ.md "wikilink")。特定の実在するアーキテクチャを試験に採用した場合、それを利用する受験者に有利に働いてしまうという問題がある。このため、実在するどのアーキテクチャとも関連性がない単純化した仮想の計算機[COMP-X](https://ja.wikipedia.org/wiki/COMP-X "wikilink")と、そのアセンブリ言語の仕様[CAP-X](../Page/CAP-X.md "wikilink")を策定することで、この問題を解消した。その後継の仮想計算機を**COMET**と呼び、アセンブリ言語の仕様をCASLと名付けた。

COMETは、最低限の機能のみを実装した仮想機械であり、そのためCASLも非常に簡素なアセンブリ言語となっている、初期の仕様ではCOMETの各[機械語](../Page/機械語.md "wikilink")命令を除けば4種類の擬似命令と3種類の[マクロしかない](../Page/マクロ_\(コンピュータ用語\).md "wikilink")。COMETとCASLの仕様は試験実施者が予め発表するほか、試験問題中にも示し、試験中にその場で仕様を理解し解答することも可能である。[基本情報技術者試験](../Page/基本情報技術者試験.md "wikilink")に出題されるコンピュータ言語の中では、同じく架空のソフトウェアである[表計算ソフト](../Page/表計算ソフト_\(情報処理技術者試験\).md "wikilink")\[2\]と並び習得しやすい言語と言われることが多い。

[2001年](../Page/2001年.md "wikilink")に第二種情報処理技術者試験が基本情報処理技術者試験に改訂された折りに、COMETとCASLの仕様改訂も行われており、改訂後はそれぞれ**COMET II**、**CASL II**と呼ばれる。なお情報処理技術者試験センターから、Java環境で動作するCASL-II[シミュレータ](https://ja.wikipedia.org/wiki/シミュレータ "wikilink")が学習用に提供されている。

情報処理技術者試験の開始当初には、同様に[CAP-X](../Page/CAP-X.md "wikilink")および**COMP-X**が用いられていたが、主にマイクロプロセッサの登場と普及に伴う主流アーキテクチャの変化にともない、変化に対応した新しいアセンブリ言語および仮想計算機としてCASLおよびCOMETが定義された。

### 主なシミュレーター

  - 公式のシミュレーター
      - CASL II シミュレータ - [情報処理推進機構](../Page/情報処理推進機構.md "wikilink")が制作した、Windowsで動作するシミュレーター。[1](https://www.jitec.ipa.go.jp/1_20casl2/casl2dl_001.html)

<!-- end list -->

  - 非公式のシミュレーター
      - [ベクター (企業)](../Page/ベクター_\(企業\).md "wikilink") - 情報処理用 CASL・COMET[2](https://www.vector.co.jp/vpack/filearea/win/prog/casl/)
      - CASL II シミュレータ - WebとWindowsで動作するシミュレーター。[3](http://www.chiba-fjb.ac.jp/fjb_labo/casl/index.html)
      - CASLシミュレータ （CASL II 対応） - Webで動作するシミュレーター。[4](https://www.officedaytime.com/dcasl2/pguide/index.html)
      - DCasl2 CASL II 開発環境 - Windowsで動作するシミュレーター、シェアウェア。[5](https://www.officedaytime.com/dcasl2/index.html)
      - WCASL-II -[Java](https://ja.wikipedia.org/wiki/Java "wikilink")で操作するシミュレーター。[6](http://www.ics.teikyo-u.ac.jp/wcasl2/)
      - InfoCASL - Windowsで動作するシミュレーター。[7](https://www.rs.kagu.tus.ac.jp/infoserv/j-siken/infocasl/)
      - CCaslII - Windows・[Linux](../Page/Linux.md "wikilink")で動作するシミュレーター。[8](http://hyamag1979.wp.xdomain.jp/hysoft/ccasl2_linux.html)
      - YCASL2 - [macOS](https://ja.wikipedia.org/wiki/macOS "wikilink")・Linuxで動作するシミュレーター。[9](http://www.j8takagi.net/yacasl2/)

## COMET の仕様

ここでは、COMET IIに改訂される前のCOMETの仕様について述べる。COMET IIとの違いについては[\#仕様改訂による変更点](https://ja.wikipedia.org/wiki/#仕様改訂による変更点 "wikilink")を参照されたい。

COMETは、1[ワード](../Page/ワード.md "wikilink")長が16[ビット](../Page/ビット.md "wikilink")の固定長語で表現され、処理の対象となるデータは全てワード単位で行われる。1ワードを構成するビットの並びは、[最上位ビット](https://ja.wikipedia.org/wiki/最上位ビット "wikilink")を0番、[最下位ビット](../Page/最下位ビット.md "wikilink")を15番とする（COMET IIで変更されている）。制御方式は逐次処理方式であり、[命令語](https://ja.wikipedia.org/wiki/命令語 "wikilink")は2ワードの固定長で表現される。扱うデータは算術データ、論理データ、文字データの3種類がある、算術データは 1ワードのデータを[2の補数](../Page/2の補数.md "wikilink")表現で表現し、論理データは符号無し整数として扱う。文字データは[JIS X 0201規格を採用している](https://ja.wikipedia.org/wiki/JIS_X_0201 "wikilink")。

[レジスタは次の通り](../Page/レジスタ_\(コンピュータ\).md "wikilink")。

  - 汎用レジスタ GR0、GR1、GR2、GR3、GR4
    16ビットのレジスタ。算術演算と論理演算、比較およびシフト演算に用いる。このうち GR1からGR4 は指標（インデックス）レジスタとしても用いる。GR4は[スタックポインタとして用いる](https://ja.wikipedia.org/wiki/レジスタ_\(コンピュータ\)#スタックポインタ "wikilink")。スタックポインタには[スタック](../Page/スタック.md "wikilink")の最上段のアドレスが保持される。
  - プログラムカウンタ PC
    実行中の命令語の先頭アドレスを保持し、命令が終了すると次に実行される命令語の先頭アドレスが設定される。上述のようにCOMETの命令語は2ワード固定長なので分岐命令のように次に実行するアドレスを指定するもの以外の場合は保持しているアドレスに 2 を加算する。
  - フラグレジスタ FR
    2ビットのレジスタで、実行された命令が算術演算や論理演算命令の場合、実行結果が負なら10、正なら00、零なら01が設定される。比較演算命令も同様に比較結果に応じて値が設定される。

前述の通りCASLは命令語を2ワードの固定長として扱う。命令語の構成は先頭から順に OPフィールド（8ビット）、GRフィールド（4ビット）、XRフィールド（4ビット）、ADRフィールド（16ビット）のデータアドレスと続く。COMETの前身であるCOMP-Xと同様の構成だが各フィールドのビット数が違うことに注意されたい。

OP フィールドは命令の種類を表すコード（[オペコード](../Page/オペコード.md "wikilink")部）であり、初期のCOMETでは23種類の[命令が用意されており](../Page/命令_\(コンピュータ\).md "wikilink")、COMET IIでは 28種類に拡張されている。GR フィールドでは演算で使用する GR の番号が指定される。分岐命令やスタック操作の場合は GRを指定することはないので、これらの命令ではこの部分は無視される（何を指定しても問題ない）。XR フィールドではアドレス修飾を行う GR の番号が指定され、内容が0の場合はGR0を意味するのではなく、GR によるアドレス修飾をしないGRフィールドと同様、アドレス修飾を持たない命令においては無視される。ADRフィールドは処理対象となるアドレスが指定され、このアドレスにXRフィールドのアドレス修飾を施したものが実行アドレスとして使用される。

なお、COMP-Xと異なり、COMETでは命令の具体的なオペコードは定義されていない（定義の後に、定義の一部でないと明示のうえで参考資料として示されている）。

[命令コードと各](../Page/機械語.md "wikilink")[命令の概要は以下の通り](../Page/命令_\(コンピュータ\).md "wikilink")。なお、書き方の\[\]は省略可能を意味している。

  - LD GR, adr\[, XR\] - LoaD
    有効アドレスの内容を指定した GRアドレスに設定する。
  - ST GR, adr\[, XR\] - STore
    GRレジスタに設定された内容を実行アドレスに格納する。
  - LEA GR, adr\[, XR\] - Load Effective Address
    有効アドレスの番地をGRに格納する。実行後、格納された値に応じて、FRに01、10、00を設定する。COMET IIの改訂後にこの命令は廃止され、代わりにFRレジスタを更新しないLAD命令が追加された。
  - ADD GR, adr\[, XR\] - ADD arithmetic
    GRの内容と有効アドレスの内容を加算し、結果をGRに格納する。このとき、FRの設定も行う。COMET IIの改訂後に、名称をADDAと改称している。
  - SUB GR, adr\[, XR\] - SUBtract arithmetic
    GRの内容から有効アドレスの内容を減算し、結果をGRに格納する。このとき、FRの設定も行う。ADDと同様、COMET IIの改訂後に名称をSUBAと改称している。
  - AND GR, adr\[, XR\]
    GRの内容と有効アドレスの内容の[論理積](../Page/論理積.md "wikilink")をGRに格納する。このとき、FRの設定も行う。
  - OR GR, adr\[, XR\]
    GRの内容と有効アドレスの内容の[論理和](../Page/論理和.md "wikilink")をGRに格納する。このとき、FRの設定も行う。
  - EOR GR, adr\[, XR\] - Exclusive OR
    GRの内容と有効アドレスの内容の[排他的論理和](../Page/排他的論理和.md "wikilink")をGRに格納する。このとき、FRの設定も行う。COMET IIの改訂後に、名称をXORと改称している。
  - CPA GR, adr\[, XR\] - ComPare Arithmetic
    GRの内容と有効アドレスの内容を算術比較し、GRの内容の方が大きければ、FRに00を、等しければ01を、小さければ10を設定する。
  - CPL GR, adr\[, XR\] - ComPare Logic
    CPAと同様だが、内容を算術データではなく論理データとして扱う。
  - SLL GR, adr\[, XR\] - Shift Left Logic
    左に有効アドレス分シフトする、シフトにより欠落したデータは捨てられ、空いたビットには0が入る。シフト後の内容により、FRに値が設定される。
  - SLA GR, adr\[, XR\] - Shift Left Arithmetic
    符号を表すビット（第0ビット、COMET IIでは第15ビット）を除いて左に有効アドレス分シフトする。シフトにより欠落したデータは捨てられ、空いたビットには 0が入る。シフト後の内容により、FRに値が更新される。
  - SRL GR, adr\[, XR\] - Shift Right Logic
    SLLの右シフト版。
  - SRA GR, adr\[, XR\] - Shift Right Arithmetic
    SLAの右シフト版。
  - JPZ adr\[, XR\] - Jump on Plus or Zero
    FRの値が00か01の場合は有効アドレスに分岐する。COMET IIの改訂により廃止される。
  - JMI adr\[, XR\] - Jump on MInus
    FRの値が10の場合は有効アドレスに分岐する。
  - JNZ adr\[, XR\] - Jump on Non Zero
    FRの値が10か01の場合は有効アドレスに分岐する。
  - JZE adr\[, XR\] - Jump on ZEro
    FRの値が00の場合は有効アドレスに分岐する。
  - JMP adr\[, XR\] - unconditional JuMP
    無条件に有効アドレスに分岐する。
  - PUSH adr\[, XR\] - PUSH effective address
    有効アドレスをスタックに格納する。このとき GR4にスタックの先頭アドレスが設定される。
  - POP GR - POP up
    スタックの先頭に格納されているアドレスを GRに設定する。GR4に新しいスタックの先頭アドレスが設定される。
  - CALL adr\[, XR\] - CALL subroutine
    [サブルーチン](../Page/サブルーチン.md "wikilink")を呼び出す。
  - RET - RETurn form subroutine
    サブルーチンから呼び出し、呼び出し元に復帰する。

## CASL の仕様

CASL は1行に、[ラベル](https://ja.wikipedia.org/wiki/ラベル_\(プログラミング\) "wikilink")、命令コード、オペランドの順に記述する。ラベルは記述しない場合もある。ラベルは3文字以内で、先頭は英大文字、それ以外は英大文字または数字である。オペランドでアドレスを指定する際に数値の代わりにラベルを記述できる。

CASL には次の擬似命令がある。

  - START \[実行開始番地\]
    プログラムの先頭に必ず書かれる。実行開始番地は\[エントリーポイント\]が指定される、省略された場合は先頭から実行を開始する。
  - END
    プログラムの終了を意味する。プログラムの最後に必ず書かれなければならない。
  - DC n - Define Constant
    nで指定した10進数の数値を1ワードの2進数データとして格納する。ただし、n が算術データの範囲（－32768から32767まで）に無い場合は、下位16ビットが格納される。
  - DS n - Define Storage
    nワード語長の領域を確保する。

また、CASLには入出力を表すマクロ命令が用意されている。内容は以下の通り

  - IN 入力領域, 入力文字長
    この命令が実行されると入力待ちが発生する。データが入力されると入力されたデータを文字型として入力領域に入力する、入力は1文字を1ワードに格納する。COMETでは文字データは[JIS X 0201](https://ja.wikipedia.org/wiki/JIS_X_0201 "wikilink")（8ビット）のため、1文字1ワード（16ビット）では空きが発生することになるが、入力データは 8ビット目以降に入力され、0から7ビット目までには0が格納される。また入力長には入力したデータの長さが格納される。入力領域、入力長はともにラベル名で指定する。
  - OUT 出力領域, 出力文字長
    出力領域に格納されているデータを出力文字長分、文字として表示する。IN 命令と同様 1ワード1文字に対応する。
  - EXIT
    プログラムの実行を終了する。CASL IIの改訂により廃止される。

## 仕様改訂による変更点

[2001年](../Page/2001年.md "wikilink")のCOMET II、CASL IIの改訂によってCASL COMETに比べていくつかの変更が行われている。具体的には以下の通り、

  - ビットの数え方が変更されている。COMETでは最上位ビットを0番、最下位ビットを15番としていたが、COMET IIでは最上位ビットが15番、最下位ビットが0番である。
  - GRの数がGR0からGR7までに拡張されている。
  - スタックポインタ専用のレジスタ SPが追加されている。これにより、スタックポインタとGR4の関係が無くなった。
  - FRが3ビットに変更される。最上位ビットにあたる部分が算術命令等で[算術オーバーフロー](https://ja.wikipedia.org/wiki/算術オーバーフロー "wikilink")が発生した場合は1、それ以外が0が格納されるフラグとして追加される。
  - ADD、SUBがそれぞれADDA、SUBAという名称に変更される。
  - EORがXORという名称に変更される。
  - JMPがJUMPという名称に変更される。
  - レジスタ同士の演算が可能になった。具体的には "命令 GR1, GR2"という書き方で有効アドレスではなく GR2の内容から演算を行う。この書き方が採用された命令は以下の通り。
      - LD
      - ADDA(ADD)
      - SUBA(SUB)
      - AND
      - OR
      - XOR(EOR)
      - CPA
      - CPL
  - LD 命令の実行後 FRが設定されるようになる。
  - COMETのLEAとJPZ命令、CASLのEXIT命令が廃止される。
  - COMET II、CASL II共に追加された命令がある。

COMET IIに追加された命令は以下の通り

  - LAD GR, adr\[, XR\] - Load ADress
    廃止された LEA 命令と同様の機能を持つ、ただし実行後に FRレジスタを更新しない点が異なる。
  - ADDL GR, adr\[, XR\]、ADDL GR1, GR2 - ADD Logic
    ADDA と同様だがデータを算術データではなく論理データ（符号無し整数）として扱う。
  - SUBL GR, adr\[, XR\]、SUBL GR1, GR2 - SUBtract Logic
    SUBA と同様だがデータを算術データではなく論理データ（符号無し整数）として扱う。
  - JPL adr\[, XR\] - Jump on PLus
    FRの値が \*00 の場合、有効アドレスに分岐する。
  - JOV adr\[, XR\] - Jump on OVerflow
    FRの値が 1\*\* の場合、有効アドレスに分岐する。
  - SVC adr\[, XR\] - SuperVisor Call
    実行アドレスを引数として[システムコール](../Page/システムコール.md "wikilink")を行う。実行後のGRとFRは不定となる。
  - NOP - No OPeration
    何もしない命令、[NOP](../Page/NOP.md "wikilink")も参照のこと。

CASL IIに追加された命令は以下の通り

  - RPUSH
    GR1からGR7の順で内容をスタックに順次格納する。
  - RPOP
    スタックから順次値を取り出し、GR7からGR1の順に格納する。

## サンプルコード

以下は CASL II による[再帰呼び出し](https://ja.wikipedia.org/wiki/再帰呼び出し "wikilink")を用いて[ハノイの塔](../Page/ハノイの塔.md "wikilink")を解くサンプルコードの一例である。

`; ハノイの塔を解くプログラム`
`MAIN   START`
`       LD      GR0,N`
`       LD      GR1,A`
`       LD      GR2,B`
`       LD      GR3,C`
`       CALL    HANOI       ; hanoi(3, A, B, C)`
`       RET`

`; hanoi(N, X, Y, Z)`
`HANOI  CPA     GR0,=1      ; if N == 1 then`
`       JZE     DISP        ;  move it, return`
`       SUBA    GR0,=1      ; N - 1`
`       PUSH    0,GR2       ; swap GR2 GR3`
`       LD      GR2,GR3`
`       POP     GR3`
`       CALL    HANOI       ; hanoi(N-1, X, Z, Y)`
`       ST      GR1,MSG1`
`       ST      GR2,MSG2    ; now GR2 holds Z`
`       OUT     MSG,LNG     ; 'from X to Z'`
`       PUSH    0,GR2       ; rotate registers`
`       LD      GR2,GR1`
`       LD      GR1,GR3`
`       POP     GR3`
`       CALL    HANOI       ; hanoi(N-1, Y, X, Z)`
`       PUSH    0,GR2       ; restore registers`
`       LD      GR2,GR1`
`       POP     GR1`
`       ADDA    GR0,=1      ; also N has restored`
`       RET`

`DISP   ST      GR1,MSG1    ; 'from X to Z'`
`       ST      GR3,MSG2`
`       OUT     MSG,LNG`
`       RET`

`N      DC      3   ; 輪の総数`
`LNG    DC      11  ; メッセージの長さ`
`A      DC      'A'`
`B      DC      'B'`
`C      DC      'C'`
`MSG    DC      'from '`
`MSG1   DS      1`
`       DC      ' to '`
`MSG2   DS      1`
`       END`

このコードを実行すると以下の結果が得られる（ここで、from A to C は A　の一番上にある円盤を C に移すことを意味している）。

`from A to C`
`from A to B`
`from C to B`
`from A to C`
`from B to A`
`from B to C`
`from A to C`

## 参考文献

  - 日高哲郎 著、『第二種情報処理技術者試験 CASL演習』、[共立出版](../Page/共立出版.md "wikilink")、1995年、ISBN 4-320-02744-2
  - 土屋純一　著、『CASLアセンブラ言語の基礎と学習』第2版、[啓学出版](https://ja.wikipedia.org/wiki/啓学出版 "wikilink")、1992年、ISBN 4-7665-1086-0
  - 八鍬幸信 著、『基本情報技術者試験 らくらく突破 CASL II』、[技術評論社](../Page/技術評論社.md "wikilink")、2006年、ISBN 4-7741-1606-8

## 脚注

## 外部リンク

  - [情報処理技術者試験センター](http://www.jitec.jp/index.html)
  - [情報処理技術者試験出題範囲](http://www.jitec.jp/1_13download/hani20061107.pdf) （PDF形式 p26以降に仕様）

[Category:プログラミング言語](https://ja.wikipedia.org/wiki/Category:プログラミング言語 "wikilink") [Category:アセンブリ言語](https://ja.wikipedia.org/wiki/Category:アセンブリ言語 "wikilink") [Category:基本情報技術者試験](https://ja.wikipedia.org/wiki/Category:基本情報技術者試験 "wikilink")

1.  CASLプログラミング―1・2種情報処理技術者試験, 甘利直幸, オーム社, 1986
2.  [基本情報技術者試験](../Page/基本情報技術者試験.md "wikilink")は[国家試験](../Page/国家試験.md "wikilink")であるため、特定のベンダーが取り扱っている製品に関する内容を出題することができない。そのため試験に登場する[表計算ソフトは試験センターが独自に仕様策定した仮想のオリジナルソフトウェアと定義されている](../Page/表計算ソフト_\(情報処理技術者試験\).md "wikilink")。しかしながら、出題される[関数および機能は](../Page/サブルーチン.md "wikilink")[Microsoft Excelのものに近いと言われている](https://ja.wikipedia.org/wiki/Microsoft_Excel "wikilink")。なお、基本情報技術者試験の表計算ソフトの問題では、[擬似言語](https://ja.wikipedia.org/wiki/擬似言語 "wikilink")を用いた[マクロ定義の内容も出題されるため](../Page/マクロ_\(コンピュータ用語\).md "wikilink")、ソフトウェアの関数および機能だけでなく、[アルゴリズム](../Page/アルゴリズム.md "wikilink")の知識も必要となる。
> この記事は[Job Control Language](https://ja.wikipedia.org/wiki/Job_Control_Language)から翻訳されています。


**Job Control Language**（**JCL**、ジョブ制御言語）とは、[メインフレーム](../Page/メインフレーム.md "wikilink")コンピュータで使われる[ジョブ制御用の](../Page/ジョブ管理システム.md "wikilink")[スクリプト言語](../Page/スクリプト言語.md "wikilink")である。処理系により**JCS**(Job Control Statement)、**ECL**（Executive Control Language）とも呼ぶ。

## 概要

ジョブ制御言語（JCL）は、[メインフレーム](../Page/メインフレーム.md "wikilink")の[ジョブ管理システム](../Page/ジョブ管理システム.md "wikilink")（ジョブ入力サブシステム）に対して、[バッチ処理](../Page/バッチ処理.md "wikilink")や常駐[プロセス](../Page/プロセス.md "wikilink")起動時の指定をする[スクリプト](../Page/スクリプト.md "wikilink")言語である。

通常は、ジョブ名、ジョブの実行クラス（優先順位など）、ステップ名、使用するプログラム名、そのプログラムが格納されているライブラリー、使用する仮想メモリーの容量、使用する物理ファイル名（[データセット名](../Page/データセット_\(IBMメインフレーム\).md "wikilink")）やその属性（格納場所、新規作成の場合の容量など）、およびジョブ内（ステップ間）の制御を行う。なおジョブ間（ジョブフロー、ジョブストリーム）の制御を自動化する場合は、JCLではできないためジョブスケジューラなどで行う。

大半のメインフレームでは、プログラムから見えるコンピュータは仮想化されており、プログラムは物理ファイル名などを認識することはできない（従って記述もできない）ため、JCLによってはじめて、プログラム内の論理ファイル名と、実際の物理ファイル名などが、関連づけられる。

[オープン系](https://ja.wikipedia.org/wiki/オープン系 "wikilink")では各種の[シェルスクリプト](../Page/シェルスクリプト.md "wikilink")が相当するが、メインフレームでのJCLは必須であり、プログラマ（プログラム）とオペレータ（運用管理）を分離している。このため運用管理担当者は、各プログラムの仕様を知ること無く、各ジョブがどの物理ファイル（[データセット](../Page/データセット_\(IBMメインフレーム\).md "wikilink")）を使用するか（しないか）を全て把握し、容易に変更できる。またプログラムが不測の物理ファイル（[データセット](../Page/データセット_\(IBMメインフレーム\).md "wikilink")）をアクセスしたり作成する事が無い。

JCLは、[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink")（OS）やバージョンによって機能や構文が異なる。JCLを持つ主なOSには、以下がある。

  - MVS系
      - [IBM](../Page/IBM.md "wikilink")のMVS系（[OS/360](https://ja.wikipedia.org/wiki/OS/360 "wikilink")、OS/VS、MVS、MVS/XA、MVS/ESA、OS/390、[z/OS](https://ja.wikipedia.org/wiki/z/OS "wikilink")）
      - [富士通](../Page/富士通.md "wikilink")の[MSP](https://ja.wikipedia.org/wiki/MSP "wikilink")（MVS互換OS。JCLもMVSベースだが独自の拡張あり）
      - [日立製作所](../Page/日立製作所.md "wikilink")の[VOS3](../Page/VOS3.md "wikilink")（MVS互換OS。JCLもMVSベースだが独自の拡張あり）

<!-- end list -->

  - VSE系
      - [IBM](../Page/IBM.md "wikilink")のVSE系（DOS/VSE、VSE/ESA、[z/VSE](https://ja.wikipedia.org/wiki/z/VSE "wikilink")。**JCS**(Job Control Statement)と呼び、機能・構文もMVS系とは異なる）

<!-- end list -->

  - [富士通](../Page/富士通.md "wikilink")のXSP（機能・構文もMSPとは異なる）

<!-- end list -->

  - [GCOS](../Page/GCOS.md "wikilink")系（多機能で一般のシェルスクリプトに近い）
      - [Bull](../Page/Bull.md "wikilink")の[GCOS](../Page/GCOS.md "wikilink")
      - [日本電気](../Page/日本電気.md "wikilink")の[ACOS](https://ja.wikipedia.org/wiki/ACOS "wikilink")

<!-- end list -->

  - [ユニシス](../Page/ユニシス.md "wikilink")の[OS2200](https://ja.wikipedia.org/wiki/OS2200 "wikilink") (**EXEC制御文**(EXECutive制御文)と呼ぶため、厳密には**ECL**（Executive Control Language） と称されるが、JCLという呼称が一般化されている)

<!-- end list -->

  - [ユニシス](../Page/ユニシス.md "wikilink")の[MCP](https://ja.wikipedia.org/wiki/MCP "wikilink")

なおメインフレーム専用OSでも、対話型志向のIBM [z/VM](https://ja.wikipedia.org/wiki/z/VM "wikilink")などにはJCLは存在しない（ゲストOSの各ユーザーが[REXX](../Page/REXX.md "wikilink")などのスクリプト言語を使用して自動化できるが、必須ではなく[UNIX](../Page/UNIX.md "wikilink")などに近い）。またメインフレームでUNIXやLinuxなどを稼働させる場合も、もちろんJCLは存在しない。

## MVS系のJCL

JCLは、[バッチ処理](../Page/バッチ処理.md "wikilink")をどのように動かすか、サブシステムをどのように起動させるかを、ジョブエントリーシステム（[Job Entry Subsystem 2/3](https://ja.wikipedia.org/wiki/Job_Entry_Subsystem_2/3 "wikilink")、JES2 または JES3）に対して指示するものである。

JCLの各行の先頭2文字は、"`//`" で始まる。このスラッシュは、パンチカードを使ってJCLを読み込ませ[ジョブ](https://ja.wikipedia.org/wiki/ジョブ "wikilink")を投入していたときの名残である。誤ってパンチカードを後ろからカードリーダーに挿入してしまった場合（代わりにシーケンス番号が先頭に来ることになるだろう）、リーダーは "`//`" が先頭にないことを読み取って、そのカードを拒絶するようになっていた。

互換性（[上位互換](https://ja.wikipedia.org/wiki/上位互換 "wikilink")、[下位互換](https://ja.wikipedia.org/wiki/下位互換 "wikilink")）のために、[z/OS](https://ja.wikipedia.org/wiki/z/OS "wikilink") で使う JCL の文法は、[1960年](../Page/1960年.md "wikilink")代から基本的には変わっていない。[OS/360](https://ja.wikipedia.org/wiki/OS/360 "wikilink") で動いたものと同じ JCL が z/OS でも動いている。

### 文法

JCL ステートメントの1行の長さは80[バイトで](../Page/バイト_\(情報\).md "wikilink")、1行またはそれ以上のステートメントで1本の JCL が構成される。

JCL ステートメントは1カラム目から71カラム目までを使用する（コメントは除く）。73カラム目から80カラム目は、しばしばシーケンス番号が記述される。

71文字を超えて1つのステートメントを記述する場合には（コメントは除く）、先の行の最後はカンマで終わり、次の行は4カラム目から16カラム目の間から始める（もちろん、全ての行の先頭2文字は "`//`" である）。

#### Identifierフィールド、Identifier欄

JCLは、1カラム目から2カラム目の "`//`" から始まる。下記を除く：

  - "`/*`" もしくはユーザー定義の別の delimiter
  - "`//*`" は、その行全てがコメントであることを指示する。

#### 名前フィールド、名前欄

名前フィールドは、1つのステートメントである。だから、他のステートメントがそのステートメントを指し示す・言及することができる。3カラム目から始まり、8文字以内の長さでなければならない。アルファベットと数字、"\#" や "@" や "$" などの文字が使用できる。名前の先頭は、数字であってはならない。ジョブ名、ステップ名、プロシージャ名、DD名を記述する。

#### オペレーションフィールド、オペレーション欄

オペレーションフィールドは、実行すべきコマンド、オペレーション（"JOB"、"EXEC"、"DD" など）を記述する。少なくとも1文字の空白が先におかれなければならない。

#### パラメータ/オペランドフィールド、パラメータ/オペランド欄

キーワードパラメータの順序は決まっていない。パラメータとパラメータの間に空白は置かない。空白の後はコメントになる。行内のパラメータの記述の左側、パラメータの前には、可読性を高めるための空白が入る。

#### コメントフィールド、注釈欄

JCL のステートメントのパラメータフィールドの後ろにインラインコメントを記述する場合には、少なくとも1文字の空白を入れてステートメントとコメントを分ける。71カラム目を超えてコメントを記述する場合には、72カラム目を空白にしない（通常、"`X`" が使われる）。次の行は "`//`" の後1カラム目から3カラム目の間からコメントの記述を続ける。

### ジョブ

1つの**ジョブ**(JOB)はジョブステートメント（ジョブ文）で始まり、 "`//`" だけの空行（空文）で終わる。1つの**ジョブ**(JOB)の中の各々の**ステップ**(STEP)は、1つの**エグゼキュート**(EXEC)ステートメント（EXEC文）と複数の**データディファニッション**(DD)ステートメント（DD文）、各々のDDステートメントに1つのアクセスする[データセットで構成される](../Page/データセット_\(IBMメインフレーム\).md "wikilink")。

### JOB文

`//jobname JOB (accounting information),CLASS=x,MSGCLASS=x,REGION=nK,TIME=(m,s),NOTIFY=XXXXXX`

CPU や I/O など、コンピュータ資源を使用した分の使用料を使用した部署に請求するために、必要な会計上の情報が、カッコやクオーテーションマークで区切られて記述される。

CLASS パラメータは、ジョブがどのイニシエータで走るかを決める。その他、ジョブの優先度を指定するパラメータなどがある。

MSGCLASS パラメータはジョブの実行結果をどこに出力するかを指定する。出力クラスは個別のプリンタや、指定のファイルなどに割り振られていて、ユーザーは希望の出力先を指定する。

REGION パラメータは、ジョブが使用できる[仮想記憶](../Page/仮想記憶.md "wikilink")の最大量、リージョンのサイズを決める。キロやメガという単位を用いて指定できる。指定できる大きさは、システムを構築するときにジョブクラス毎に設定される。

TIME パラメータは、CPU を使用できる最大時間を決める。分、秒で指定する。ジョブの全てのステップが使用する時間を指定する。使用できる最大時間は、1439分59秒（TIME=(1439,59)）。1440分を指定すると時間制限なしとなる。

### EXEC PGM文

`//stepname EXEC PGM=progname,PARM="parm",COND=condition,REGION=nK,TIME=(m,s)`

progname は、実行するプログラムを指定する。プログラムがシステム標準指定のリンクリスト、ライブラリに無い場合、JOBLIB か STEPLIB を DD ステートメントに記述して、格納してあるライブラリを指定する。

COND パラメータは、条件を満足する場合は当該ジョブステップを迂回する、実行しない、という指定である。このパラメータはしばしば、条件を満足したら通る、実行する IF ステートメントと混同され、混乱を招く。最近リリースされたオペレーティングシステムでは、この COND 指定の記述法は IF 指定の記述法に置き換わっている。

### EXEC PROC文

`//procstepname EXEC PROC=procname,param1=foo, ...`

または

`//procstepname EXEC procname,param1=foo, ...`

procname は、カタログされた、あるいは in-stream （流れ内）のプロシージャ名を指定する。param1 以下の指定は、プロシージャに定義されたシンボリックキーワードに依る。プロシージャは、予め定義された JCL（の集まり）である。慣例上、上記例の2つめ、「PROC=」を省いた形を用いる場合が多い。

### DD文

`//ddname DD DSN=datasetname,DISP=disposition,UNIT=unit,VOL=SER=volser,SPACE=space,DSORG=dsorg,DCB=dcb`

または

`//ddname DD *`

または

`//ddname DD DATA,DLM=@@`

または

`//ddname DD SYSOUT=msgclass`

DSN パラメータには、アクセスまたはアロケートするデータセット名を指定する。そのデータセットがカタログされていない場合、さらに UNIT パラメータと VOL パラメータが必要である。区分データセットの中の1つのメンバーを参照・指定・言及する場合には、カッコで括って記述する。たとえば MY.LIBRARY(MYPROGRM) というように。もしデータセット名を指定しなかった場合は、システムは1つ、データセットを割り当てる。このデータセットは当該ステップの中でのみ維持され、使用できる。ステップを跨って使用するが、ジョブが終了したら不要な一時データセット、テンポラリデータセットを指定するときは、データセット名の先頭に「&&」を記述する。たとえば DSN=&\&TEMPNAME のように。

DISP パラメータは、データセットをそこで作成するのか、既に存在するのか、ジョブが正常終了したときデータセットを保存しておくのか消してしまうのか、ジョブが失敗に終わったときにデータセットを保存しておくのか消してしまうのか、を指定する。この DISPOSITON パラメータは、カッコで括って3つのサブパラメータがある。例：

  - DISP=(OLD,DELETE,KEEP) － データセットは既存で、ステップが成功したら削除され、失敗したら保存される。
  - DISP=SHR － データセットは既存で、同じタイミング、時刻に別のタスクが読みに来るかもしれない場合。
  - DISP=(NEW,CATLG,DELETE) － データセットを新規に作成し、カタログする。ステップが失敗したら、削除されカタログははずされる。

なにも指定しない場合の初期値は (NEW,DELETE) である。

UNIT パラメータと VOL パラメータは、併せて記述できる。しかしここでは、シンプルな記述例を示す：

  - UNIT=SYSDA － ダイレクトアクセスデバイス全般を意味する。テンポラリファイル（一時データセット）への指定の場合が多い。
  - UNIT=3390,VOL=SER=ABC123 － 特定の（指定の）ダスドのパック ABC123 にアロケーションすることを指定。

SPACE パラメータは、[ブロック](../Page/ブロック_\(データ\).md "wikilink")、トラック、シリンダー単位で、1次割り振り量と2次割り振り量を指定する。および、区分データセットのディレクトリブロックの大きさを指定する。例：

  - SPACE=(TRK,1) － 1トラックだけ割り振る。2次割り振りはしない。
  - SPACE=(CYL,(50,25)) － まず最初に50シリンダー割り振り（1次割り振り）、足りなければ25シリンダーを15回まで割り振っていく（2次割り振り）。（それでも足りなければ容量不足でジョブは異常終了する）
  - SPACE=(4096,(10000),ROUND,RLSE) － 4096バイトのブロックが10000ブロック分になるように、シリンダーのサイズに近い値で割り振る。使わない余ったスペースが生じたら、ジョブステップが終了したときに空き部分を解放する。

DSORG パラメータは、データセットの編成方法を指定する。PS（物理順次、順次データセット）か、DA（ダイレクトアクセス）か、IS（ISAM、現在はサポートされていない）か、PO（区分データセット）を指定する。

DCB パラメータには、プログラムがデータコントロールブロックにてこの DD ステートメント宛てに指定したどのサブパラメータも指定できる。通常は、RECFM サブパラメータによって、レコードフォーマットが指定されることが多い。FB（ブロック化された固定長）、U（未定義）、V（可変長）など。

DD \* は、そこから先は80バイトのカードイメージのデータである、という指定である。このデータは、1カラム目から2カラム目に /\* と記述するか、次のJCLステートメント（1カラム目から2カラム目が "`//`" ）の記述が始まることで終了する。（この記法は一種の[ヒアドキュメント](https://ja.wikipedia.org/wiki/ヒアドキュメント "wikilink")とも考えられる）

DD DATA は、DD \* と同じだが、JCL ステートメントに含まれる。それは、1カラム目から2カラム目に @@ が記述される行または JCL の終了をもって終了される。

DD SYSOUT=msgclass は、プリントを出力する先を指定する。 SYSOUT=\* と指定すると、ジョブカードに指定した MSGCLASS に出力される。

入力データ用の DD ステートメントは、下記のように連結して指定できる（コンカチ）。

`//STEPLIB DD DSN=MY.TEST.LIBRARY,DISP=SHR`
`//        DD DSN=MY.TEAM.LIBRARY,DISP=SHR`
`//        DD DSN=MY.LIVE.LIBRARY,DISP=SHR`

### プロシージャ

プロシージャは、JCL のスケルトンである。通常、置き換えることでデータセット名を指定できるようなシンボルを含む。これらのシンボル名は、プロシージャが実際に使われるときに、本当のデータセット名に置き換わる。プロシージャは、JCL に[マクロ機能を可用にする](../Page/マクロ_\(コンピュータ用語\).md "wikilink")。

[MVS](../Page/Multiple_Virtual_Storage.md "wikilink") の古いバージョンでは、プロシージャは SYS1.PROCLIB に予め格納/カタログされていなければならなかった（カタログ式プロシージャ、カタプロ）。新しいバージョンでは、ユーザーが定義したライブラリに格納したプロシージャも使えるようになった。

通常、プロシージャは、上記のような proclib と称されるプロシージャライブラリから呼び出されて実行される。一方、実行するそのジョブそのものの中に定義することもできる。これは流れ内 (inline, in-stream) プロシージャと呼ばれ、普通は、proclib に登録する前にプロシージャをテストする際に用いられる。

最初の行は必ず PROC ステートメントで始まる。そこにはプロシージャ名と、シンボリックの初期値を定義する。例：

`//MYPROC  PROC &LIB="MY.TEST.LIBRARY"`

あるジョブがこのプロシージャをコールするとき、たとえば以下のように記述する:

`//FIRST       EXEC MYPROC`
`//SECOND  EXEC MYPROC,LIB="FREDS.TEST.LIBRARY"`

FIRST の例では、MYPROC プロシージャ中のシンボル LIB は初期値 "MY.TEST.LIBRARY" に置換される。SECOND の例では、MYPROC プロシージャ中のシンボル LIB はコール時に指定した "FREDS.TEST.LIBRARY" に置換される。

流れ内プロシージャを終了するステートメントは:

`//     PEND`

### 条件処理

JCL は、if-then-else-endif ステートメントを用いた初歩的な条件処理をサポートする。例：

`//TESTCOND IF (RC = 8 | RC = 10) THEN`
`…`
`//ELSECOND ELSE`
`…`
`//ENDCOND  ENDIF`

### JCL記述例

過去の遺産を継いでいることから、JCL のオペレーション/記述はほかのオペレーティングシステムのジョブ制御よりも複雑である。

下記は、既存のデータセット (IS198.TEST.INPUT) を読んでプログラムABCDEFGHが何か処理を行い、新しくデータセット (IS198.TEST.OUTPUT) を作成してそこに出力するジョブの JCL ステートメントの例である。

`//IS198PRS JOB (IS198T30500),'DATA KAKOU',CLASS=L,MSGCLASS=X,NOTIFY=ADM00011`
`//STEP01   EXEC PGM=ABCDEFGH`
`//SYSPRINT DD  SYSOUT=*`
`//INPUT    DD  DSN=IS198.TEST.INPUT,DISP=SHR`
`//OUTPUT   DD  DSN=IS198.TEST.OUTPUT,`
`//           DISP=(NEW,CATLG,DELETE),`
`//           SPACE=(CYL,(40,5),RLSE),`
`//           DCB=(RECFM=FB,LRECL=115,BLKSIZE=0),`
`//           VOL=SER=VOL001`
`//`

## VSE系のJCS

JCSは、[バッチ処理](../Page/バッチ処理.md "wikilink")をどのように動かすか、サブシステムをどのように起動させるかを、ジョブエントリーシステム（VSE/POWER）に対して指示するものである。

MVS系と比較すると、JCSの各行の先頭2文字が"`//`" で始まるのは同じで、機能もほぼ同等だが、各ステートメントの構文はかなり異なる。

なおJCSでは無いが、VSE/POWERに対する指示を行うコマンドはJECL（ジョブ入力制御言語）であり、MVS系のJESコマンドに相当する。

### JOB文

` // JOB jobname`

ジョブの先頭に必要。ジョブ名は8文字以内の英数字。

### EXEC PGM文

`// EXEC progname,SIZE=nn,PARM=parm`

プログラムの実行。プログラムが必要な記憶域やパラメータを指定できる。

### EXEC PROC文

`// EXEC progname,SIZE=,PARM=parm`

プロシージャー（一連のJCSを事前登録したもの）の実行。

### ASSIGN文

`// ASSIGN devicename,address`

入出力装置の指定。プログラム内の論理装置名と、物理装置のアドレスを関連づける。

### DLBL/EXTENT文

`// DLBL file-name,'file-id'`

および

`// EXTENT device-name,volser,,,start-address,capacity`

磁気ディスク装置上のファイルの関連づけ。順次ファイルの場合のみEXTENTも必要。

### LIBDEF文

`// LIBDEF type,SEARCH=librarylost`

VSEのライブラリーを指定。

### TLBL文

`// TLBL file-name,file-id,date,file-serial-no,volume-sequence-no,file-sequence-no`

標準ラベル(Standard Label、SL)付きの磁気テープ使用時に指定。

### UPSI文

`// UPSI xxxxxxxx`

CPUの外部スイッチ・シミュレーション。

### OPTION文

`// OPTION`

コンパイラーに対する出力形態の指示。

### IF-GOTO文

`// IF $RC または $MRC ...`
`// GOTO label`

ステップの戻りコード検査および制御。実行されたステップの戻りコードに応じて、後続のステップをスキップするなどができる。MVS系の COND パラメータに相当。

### 終了文

`/&`

ジョブの終わりであることを示す。

### JCS記述例

`//JOB   JOB12345`
`//ASSGN SYS005,241`
`//ASSGN SYS010,DISK,VOL=VOL555`
`//DLBL FILEA,'SAMPLE.FILE'`
`//EXTENT`
`//EXEC PROGA,SIZE=xxx,PARM=ABCDE`

## XSPのJCL

### JCL記述例

`\         JOB　JOB1234,ACCT='USER001',PRTY=(1,1),LIST=A `
`\STEP0001 EX　PROG1234,COND=10 `
`\         FD PRGLIB=DA,FILE=SYSPRG `
`\         FD CF=DA,FILE=TEST.FILEA `
`\         FD SYSDBOUT=DA,VOL=VOL1,TRK=(2,1,RLSE),SOUT=A`

## GCOSのJCL

### JCL記述例

  - 例1

`$ IDENT 00123,USER-01,DEBUG,TEST`
`$ OBJECT`
`.`
`. Object File`
`.`
`$ DKEND`
`$ EXECUTE ON3,DUMP`
`$ LIMITS 5,,,5000`

  - 例2

`$$j,talk`
`$$select(ident)`
`$ program progabc `
`$ limit ,24k`
`$ prmfl **,q,r,netex/adpl.x/exec/testabc `
`$ privity`

## 関連項目

  - [メインフレーム](../Page/メインフレーム.md "wikilink")
  - MVS
      - [OS/360](https://ja.wikipedia.org/wiki/OS/360 "wikilink")
      - [Multiple Virtual Storage](../Page/Multiple_Virtual_Storage.md "wikilink")
      - [データセット (IBMメインフレーム)](../Page/データセット_\(IBMメインフレーム\).md "wikilink")
      - [IBM メインフレーム ユーティリティプログラム](../Page/IBM_メインフレーム_ユーティリティプログラム.md "wikilink")（JCL記述例あり）
  - VSE
      - [z/VSE](https://ja.wikipedia.org/wiki/z/VSE "wikilink")
  - GCOS
      - [GCOS](../Page/GCOS.md "wikilink")
      - [ACOS](https://ja.wikipedia.org/wiki/ACOS "wikilink")

## 外部リンク

  - MVS関連（MVS、OS/390、z/OS）
      - [MVS便利帳](http://www33.ocn.ne.jp/~yfuku/mvs/mvsindex.html)（JCL簡易解説あり）
      - [サンプルJCL集](http://mvsjcl.web.fc2.com/)
      - [z/OS MVS JCLユーザーズガイド](http://www-1.ibm.com/support/docview.wss?uid=pub3sa88857000)
      - [z/OS MVS JCL Reference](http://publibz.boulder.ibm.com/bookmgr_OS390/libraryserver/zosv1r9/index.html?DOCNUM/SA22-7597/CCONTENTS?FS=TRUE&TB=SCRIPT&BOOKMARK=TRUE&PATH=/bookmgr_OS390/libraryserver/zosv1r9/)（英文。z/OS各バージョン）

<!-- end list -->

  - VSE関連
      - [z/VSE V4R1.1 System Control Statements マニュアル](http://publibz.boulder.ibm.com/cgi-bin/bookmgr_OS390/BOOKS/IESSOE41/CCONTENTS?SHELF=IESVSE63&DN=SC33-8305-01)（英文）
      - [IBM - z/VSEマニュアル（英文）](http://www-03.ibm.com/servers/eserver/zseries/zvse/documentation/)

<!-- end list -->

  - MSP/XSP関連
      - [ジョブフロー作成ツール「ＪＥＴ-Ｗｉｎ」の富士通MSP/XSPのJCLサンプル](http://www.kcs.co.jp/products/jet-win/sample.html)

<!-- end list -->

  - GCOS関連
      - [GCOS 8 JCL Reference Manual](http://support.bull.com/ols/product/system/gcos8/sys/doc/docf/g/67X4A2CD25/doc/rg30a11a.pdf)（英文）
      - [AN INTRODUCTION TO GCOS BATCH PROCESSING](http://www.thinkage.ca/english/gcos/expl/batc/guid/guid.html#Section3)（英文）

<!-- end list -->

  - その他
      - [JCL & Mainframe related Discussion group](http://groups.yahoo.com/group/mvstips)

[Category:スクリプト言語](https://ja.wikipedia.org/wiki/Category:スクリプト言語 "wikilink") [Category:IBM](https://ja.wikipedia.org/wiki/Category:IBM "wikilink")
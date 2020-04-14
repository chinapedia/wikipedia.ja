> この記事は[IBM メインフレーム ユーティリティプログラム](https://ja.wikipedia.org/wiki/IBM_メインフレーム_ユーティリティプログラム)から翻訳されています。


**IBM Mainframe Utility Programs**（IBMメインフレーム[ユーティリティプログラム](https://ja.wikipedia.org/wiki/ユーティリティプログラム "wikilink")）とは、[MVSのような](../Page/Multiple_Virtual_Storage.md "wikilink")[IBM](../Page/IBM.md "wikilink")[メインフレーム](../Page/メインフレーム.md "wikilink")[コンピュータ](../Page/コンピュータ.md "wikilink")用の[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink")向けに供給されている、[データセットの操作](../Page/データセット_\(IBMメインフレーム\).md "wikilink")、データセットとデータセットを結びつけることを実施するプログラム群のことである。

## ICKDSF

ICKDSF はDASDをインストールしたり、初期化したり、保守するのに用いられる。オペレーティングシステムに繋いでいても、切り離されていても使用できる。

`サンプル (`[`VTOC`](https://ja.wikipedia.org/wiki/VTOC "wikilink")をデフォルトサイズで作成`)`
`//ICKDSF1 JOB (ICKDSF,,TEST),'DISK INIT',CLASS=A,MSGCLASS=A,`
`//         MSGLEVEL=(1,1)`
`//ICKDSF01 EXEC PGM=ICKDSF`
`//SYSPRINT DD  SYSOUT=*`
`//SYSIN    DD  *`
`  INIT UNIT(unitaddr) NOVERIFY VOLID(volume) VTOC(END)`
`/*`

## IDCAMS

IDCAMS は [VSAM](https://ja.wikipedia.org/wiki/Virtual_storage_access_method "wikilink") データセットを生成したり、変更を加えたりするのに用いる。

`サンプル(DB2の一時`[`表領域`](https://ja.wikipedia.org/wiki/表領域 "wikilink")の作成をしている`)`
`//WRKFILE EXEC PGM=IDCAMS`
`//SYSPRINT DD SYSOUT=*   `
`//SYSIN DD *             `
` DEFINE  CLUSTER -`
`       ( NAME(DSNCAT.DSNDBC.WRKFILE.DSN4K01.I0001.A001) -`
`         LINEAR -`
`         REUSE -`
`         VOLUMES(volume)  -`
`         CYLINDERS(1000 50) -`
`         SHAREOPTIONS(3 3) ) -`
`    DATA -`
`       ( NAME(DSNCAT.DSNDBD.WRKFILE.DSN4K01.I0001.A001) ) - `
`    CATALOG -`
`       ( DSNCAT )`

## IEBCOMPR

IEBCOMPR は順次データセットまたは区分データセットを比較（コンペア）するのに用いる。

`サンプル(順編成ファイルの比較している)`
` //STEP001  EXEC PGM=IEBCOMPR`
` //SYSPRINT DD  SYSOUT=*`
` //SYSUT1   DD  DISP=SHR,DSN=COMPARE.DATA`
` //          UNIT=3390,VOL=SER=WRKVOL`
` //SYSUT2   DD  DISP=SHR,DSN=TARGET.DATA`
` //          UNIT=3390,VOL=SER=GYOVOL`
` //SYSIN    DD  *`
`    COMPARE   TYPORG=PS`
` /*`

## IEBCOPY

IEBCOPY は区分データセットをコピー、圧縮（コンプレス）、合併（マージ）するのに用いられる。コピーする際、メンバーの選択 (select, exclude)、メンバー名の変更 (rename)、メンバーの置換 (replace) ができる。

`サンプル(メンバーコピー)`
` //STEP01   EXEC PGM=IEBCOPY,REGION=4M`
` //SYSPRINT DD SYSOUT=*`
` //SYSUT3   DD SPACE=(CYL,400),UNIT=SYSDA`
` //SYSUT4   DD SPACE=(CYL,400),UNIT=SYSDA`
` //I1       DD DISP=SHR,DSN=USER.LIBRARY1`
` //O1       DD DISP=SHR,DSN=USER.LIBRARY2`
` //SYSIN    DD *`
`   COPY I=I1,O=O1`
`     S M=(PGM001)`
` /*`

## IEBDG

IEBDG ('Data Generator') は、パターン化されたデータから成るテストデータセットを作成する。

## IEBEDIT

IEBEDIT は、[JCL](../Page/Job_Control_Language.md "wikilink") の一部分をコピーする。

## IEBGENER

IEBGENER は、順次データセットのレコードをコピーする。あるいは、区分データセットに格納する。

`サンプル(順次データのコピー)`
` //STEP01   EXEC PGM=IEBGENER,REGION=4M`
` //SYSPRINT DD SYSOUT=*`
` //SYSUT1   DD DISP=SHR,DSN=USER.SEQDETA1`
` //SYSUT2   DD DSN=USER.SEQDATA2,`
` //          DISP=(NEW,KEEP,DELETE),UNIT=3390,VOL=SER=volume,`
` //          SPACE=(TRK,(850,100),RLSE)`
` //SYSIN    DD DUMMY`

## IEBIMAGE

IEBIMAGE は IBM 3800 プリントサブシステムのロードモジュールを扱う。

## IEBISAM

IEBISAM は ISAM データセットの印刷やデータのロード、アンロードを行う。

## IEBPTPCH

IEBPTPCH は順次データセットまたは区分データセットを印刷、またはパンチする。

## IEFBR14

IEFBR14 はダミープログラムで、通常はデータセットのアロケーション（作成）やデリート（削除）に使用する。IEFBR14 は最初、[機械語](../Page/機械語.md "wikilink")の[命令の](../Page/命令_\(コンピュータ\).md "wikilink")1つ "Branch to Register" 14 のみで出来ていた。IBMの[アセンブリ言語](../Page/アセンブリ言語.md "wikilink")では記憶するのに BR 命令を使用した。そこから、IEF BR 14 の名が付いた。この命令が1つだけのプログラムは、エラーを内包する。それはリターンコードをセットしない、というものだ。そこで、リターンコードをクリアするために2つめの命令が付け加えられた。現在では、正しいステータスとともに終了する。

## IEBUPDTE

IEBUPDTE は順次データセットと区分データセットの変換を実施する。

## IEHINITT

IEHINITT ('INIT Tape') は、ラベルを書き込むことによってテープを初期化する。

## IEHLIST

IEHLIST はデータセットのリストを取る。

## IEHMOVE

IEHMOVE は、データの集まりを移動したりコピーしたりするのに用いる。

## IEHPROGM

IEHPROGM はシステム制御データを作成したり (build) 保守したりするのに用いる。また、データセットを消したり (scratch) 、名前を変更する (rename) のに用いられる。

## 関連項目

  - [Job Control Language](../Page/Job_Control_Language.md "wikilink")
  - [Multiple Virtual Storage](../Page/Multiple_Virtual_Storage.md "wikilink")
  - [データセット (IBMメインフレーム)](../Page/データセット_\(IBMメインフレーム\).md "wikilink")

[Category:IBMのソフトウェア](https://ja.wikipedia.org/wiki/Category:IBMのソフトウェア "wikilink")
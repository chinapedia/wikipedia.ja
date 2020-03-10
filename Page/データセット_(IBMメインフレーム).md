> この記事は[ \(IBM\)](https://ja.wikipedia.org/wiki/_\(IBM\))から翻訳されています。


**データセット** (data set, dataset) という言葉は、[IBM](../Page/IBM.md "wikilink")[メインフレーム](../Page/メインフレーム.md "wikilink")[コンピュータ](../Page/コンピュータ.md "wikilink")で扱う[ファイルについて言及するときに使われる言葉である](../Page/ファイル_\(コンピュータ\).md "wikilink")。

それらは、[record-oriented file](https://ja.wikipedia.org/wiki/Record-oriented_filesystem "wikilink") である。[DASD](https://ja.wikipedia.org/wiki/Direct_access_storage_device "wikilink") や[磁気テープ](../Page/磁気テープ.md "wikilink")に[ストア](https://ja.wikipedia.org/wiki/ストア "wikilink")される。データセットという言葉は [OS/360](https://ja.wikipedia.org/wiki/OS/360 "wikilink") で使い始められ、[MVS](../Page/Multiple_Virtual_Storage.md "wikilink")、[OS/390](https://ja.wikipedia.org/wiki/OS/390 "wikilink")、[z/OS](https://ja.wikipedia.org/wiki/z/OS "wikilink") に至るまで使い続けられている。

[UNIX](../Page/UNIX.md "wikilink") システム上で使われるファイルとは違い、それらは構造化されていない [bytes](https://ja.wikipedia.org/wiki/w:byte "wikilink") の羅列ではない。論理的に様々な形に編成された[レコード](../Page/レコード.md "wikilink")であり、DCB ( Data Control Block ) の[パラメーター](https://ja.wikipedia.org/wiki/パラメーター "wikilink") DSORG ( data set organization ) や RECFM ( record format ) などとして構造化されたブロックとして定義されたものである。[DCB](https://ja.wikipedia.org/wiki/w:Data_Control_Block "wikilink") はデータセットにアクセスする際に用いる構造化されたデータの姿である。これらのパラメーターは [JCL](../Page/Job_Control_Language.md "wikilink") の DD ステートメントにも指定されていて、データセットをアロケート（配置、割り当て）するのに用いられる。

## データセット編成 ( Dataset Organization )

OS/360 では、DCB の DSORG パラメーターは、データセットの編成方法を指定した。

PS ファイル ( physically sequential )、IS ファイル ( indexed sequential )、区分データセット（ PO ファイル、partitioned data set ）、DA ファイル ( Direct Access ) などである。磁気テープに記録されるのは DSORG=PS 、PS ファイルのみである。どの編成を選ぶかは、その[データ](../Page/データ.md "wikilink")がどのようにアクセスされるか、とりわけ、どのように更新されるかによって決める。

## レコードフォーマット ( Record Format, RECFM )

どの編成方法であるかにかかわらず、各々のレコードの物理的な構造は基本的にみな同じであり、データセットを通して一定の形式となっている。それは DCB の RECFM ( record format ) パラメーターによって指定される。

RECFM=F はレコードの固定長 ( fixed length ) を意味し、LRECL ( logical record length ) パラメーターによって長さが指定される。RECFM=V は可変長 ( variable-length ) を意味する。可変長のレコードは、先頭に長さの情報を持っている ( Record Descriptor word )。RECFM=FB はブロック化された固定長 ( fixed-blocked ) を、RECFM=VB はブロック化された可変長 ( variable-blocked ) を意味する。このことは、多様な論理レコードが磁気テープや磁気ディスク上の1つの物理的なブロックにグループされることを意味する。BLKSIZE ( block size ) パラメーターはブロックの最大の長さを指定する。RECFM パラメーターにはまた、FBS ( Fixed-blocked-standard ) という指定もある。これは最後のレコードを除き、フルレングスであることを要求する。RECFM=VBS は、複数のブロックに渡ってレコードが格納される ( Variable-blocked-spanned ) ことを意味する。RDW に記録されたフラグにより レコードのセグメントが次のブロックに続いているか、前のブロックから続いているか を示すことによって、1つの論理レコードが2つ以上のブロックに跨って格納される。

レコードフォーマットのメカニズムは、レコードを分けるための[区切り符号](https://ja.wikipedia.org/wiki/区切り文字 "wikilink") ( delimiter ) を用いる必要性を除去する。いかなる区切り符号をも不要とする。IBMメインフレームコンピュータにおいて、ファイルという言葉は、レコードの集まりを抽象したものである。このことは、[Unix](../Page/UNIX.md "wikilink") や [Windows](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink") や [Mac OS](https://ja.wikipedia.org/wiki/Mac_OS "wikilink") などの小さな[コンピュータ](../Page/コンピュータ.md "wikilink")の[システム](../Page/システム.md "wikilink")に見られる構造化されない[バイトの流れ](../Page/バイト_\(情報\).md "wikilink") ( stream of bytes ) とは対照をなすものである。これは、誤ったレコードの終わりに遭遇することなしに、データに、バイナリの整数、浮動小数点、文字列を問わず、いかなるタイプであることも許容するものである。

## 区分データセット ( Partitioned Datasets, PDS )

**区分データセット** ( **PDS**, **Partitioned Data Set** )は、 1つのデータセットの中に複数の**メンバー** ( **member** ) 、データセットを分けたサブデータセットを含むデータセットである。

PDS は、他の[ファイルシステム](../Page/ファイルシステム.md "wikilink")の[ディレクトリ](../Page/ディレクトリ.md "wikilink")に似ている。このタイプのデータセットは、実行形式のプログラム、**ロードモジュール** を保持したりするのに使われる。PDS はまた、[ソース](../Page/ソース.md "wikilink")プログラムをストアしておく[ライブラリ](../Page/ライブラリ.md "wikilink")として、またアセンブラのマクロ定義を格納しておくライブラリとして用いられる。

1つの 区分データセットは1つのディレクトリ（登録簿）と、ディレクトリ（登録簿）と関連付けたデータセットの中にまとめられた小さなシーケンシャルファイルの集まりとから成っている。各々の小さいシーケンシャルファイルは区分データセットのメンバーとして認知され、区分データセットの持つディレクトリを使ってダイレクトにアクセスされる。メンバーは一度位置を突きとめられたら、メンバーに格納されているデータは PS ファイル（シーケンシャルファイル）と同様に扱われる。

メンバーが削除されても、そのスペースは他のデータによって利用することは出来ない。また、メンバーが更新されたら、そのメンバーは PDS の後ろのほうにある新しい空間にストアされ、元在った場所はデッドスペースとして残される。これを解決するには、全てのメンバーを移動してデータセットのスペースの先頭から並べていき後ろの方に不使用スペースを残すコンプレスという操作を行わなければならない。それもしばしば。PDS ファイルは、個々のメンバーにアクセスするのにディレクトリ構造を使うために、ディスクの上にしか記録出来ない。PDS ファイルは、実行する JCL を保存するのに、[IBM メインフレーム ユーティリティプログラムのコントロールステートメントを保存するのに](../Page/IBM_メインフレーム_ユーティリティプログラム.md "wikilink")、実行モジュールを保存するのに、最もよく使われる。

MVS/XA から、PDSE ファイル ( Partitioned DATA set Extended, PDS/E ) も使われる。PDSE ファイルの構造はPDS ファイルとよく似ており、また同じタイプのデータをストアするのに用いられる。しかしながら、PDSE ファイルは、定義の際にディレクトリブロックのアロケーションを要求しないという、改善されたディレクトリ構造を持つ。このため、もしディレクトリブロックに充分な量を指定しなくても、ディレクトリブロックを使い尽くすということがない。PDSE ファイルはまた、メンバーをストアするにあたってデッドスペースを再生するコンプレスを必要としない。PDS ファイルと同様に、個々のメンバーにアクセスするのにディレクトリ構造を使うため、ディスクの上にしか記録出来ない。PDSE ファイルはまたライブラリとも呼ばれる。

## 関連項目

  - [ファイル編成法](../Page/ファイル編成法.md "wikilink")
  - [Multiple Virtual Storage](../Page/Multiple_Virtual_Storage.md "wikilink")

[Category:IBM](https://ja.wikipedia.org/wiki/Category:IBM "wikilink") [Category:ファイル_(コンピュータ)](https://ja.wikipedia.org/wiki/Category:ファイル_\(コンピュータ\) "wikilink")
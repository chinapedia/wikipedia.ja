> この記事は[Virtual Storage Access Method](https://ja.wikipedia.org/wiki/Virtual_Storage_Access_Method)から翻訳されています。


**Virtual Storage Access Method** ( **VSAM**、ぶいさむ、仮想記憶アクセス方式) は、[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink") [OS/VS2](https://ja.wikipedia.org/wiki/OS/360#その後の開発 "wikilink") で初めて使われ、後に [MVS](../Page/Multiple_Virtual_Storage.md "wikilink") 、z/OSで使われ続けている [IBM](../Page/IBM.md "wikilink") が提案した[ディスク](../Page/ディスクメディア.md "wikilink")[ファイル](../Page/ファイル_\(コンピュータ\).md "wikilink")[ストレージ](https://ja.wikipedia.org/wiki/ストレージ "wikilink")の方式 ([ファイル編成法](../Page/ファイル編成法.md "wikilink")) である。

VSAMは当初からトランザクショナルファイルとしてメインフレームのデフォルトの Resource Manager（RM）を構成していた。IBMメインフレームでは Transaction Manager（TM）さえ付加すれば VSAM でトランザクション処理が可能だった。そのためにz/OSは非常に高価なライセンス料だった。IBMは[2002年](../Page/2002年.md "wikilink")にz/OSの低価格版z/OS.eをリリースするに当たって、わざわざUNIX系OSと同じように、TMとしてCICS、IMSを　RMとして直接にVSAMを利用できない仕様を作った。

VSAM は、次の[アクセス](https://ja.wikipedia.org/wiki/アクセス "wikilink")方式を含む：

  - キー・シーケンス・[データセット](../Page/データセット_\(IBMメインフレーム\).md "wikilink") ( [Key Sequenced Data Set](https://ja.wikipedia.org/wiki/w:Key_Sequenced_Data_Set "wikilink"), KSDS )
  - 相対レコードデータセット ( [Relative Record Data Set](https://ja.wikipedia.org/wiki/w:Relative_Record_Data_Set "wikilink"), RRDS )
  - エントリー・シーケンス・データセット ( [Entry Sequenced Data Set](https://ja.wikipedia.org/wiki/w:Entry_Sequenced_Data_Set "wikilink"), ESDS )
  - 線形データセット ( [Linear Data Set](https://ja.wikipedia.org/wiki/w:Linear_Data_Set "wikilink"), LDS ) 。

VSAM のレコードには、固定長も可変長も含むことができる。レコードは、コントロール・インターバル ( CI ) と呼ばれる固定長のブロックに編成され、コントロール・インターバルはコントロール・エリア ( CA ) と呼ぶより大きな区切りに格納される。コントロール・インターバル ( CI ) のサイズは、たとえば 4K, 4096 などと[バイトで測られ](../Page/バイト_\(情報\).md "wikilink")、コントロール・エリア ( CA ) のサイズはトラック数やシリンダー数といった[ディスク](https://ja.wikipedia.org/wiki/磁気ディスク "wikilink") ( DASD ) の容量の単位で測られる。

VSAM [データセットの](../Page/データセット_\(IBMメインフレーム\).md "wikilink") 削除と定義 ( delete and define, DELDEF ) には、IDCAMS という[プログラムが使われる](../Page/プログラム_\(コンピュータ\).md "wikilink")（[IBM メインフレーム ユーティリティプログラム参照](../Page/IBM_メインフレーム_ユーティリティプログラム.md "wikilink")）。（ユーザが作成した）[アプリケーションプログラムからのアクセスは](../Page/アプリケーションソフトウェア.md "wikilink")、[JCL](../Page/Job_Control_Language.md "wikilink") の DD文に指定するか、あるいは [CICS](../Page/CICS.md "wikilink") ( Customer Information Control Systems ) のオンライン・リージョンなどを通して行う。

[IMS](../Page/IMS.md "wikilink")/DB と（IBMの[メインフレーム](../Page/メインフレーム.md "wikilink")で扱う）[DB2](https://ja.wikipedia.org/wiki/DB2 "wikilink")のDB はどちらも VSAM の上に実装され、その[データ構造](../Page/データ構造.md "wikilink")を用いる。

## 外部リンク

  - [redbooks.ibm.comのVSAM](http://www.redbooks.ibm.com/redbooks/SG246105/wwhelp/wwhimpl/js/html/wwhelp.htm)
  - [日本IBM，メインフレームの低価格モデルを出荷](http://itpro.nikkeibp.co.jp/free/NOS/NEWS/20020225/3/)

## 関連著作

  - 『VSAM』 著 [Doug Lowe](https://ja.wikipedia.org/wiki/w:Doug_Lowe_\(author\) "wikilink")　Mike Murach & Associates Inc　ISBN 091162533X

## 関連項目

  - [ファイル編成法](../Page/ファイル編成法.md "wikilink")
  - [IMS](../Page/IMS.md "wikilink")
  - [CICS](../Page/CICS.md "wikilink")
  - [JCL](https://ja.wikipedia.org/wiki/JCL "wikilink")
  - [ISAM](../Page/Indexed_Sequential_Access_Method.md "wikilink")
  - [レコード・オリエンテッド・ファイルシステム](../Page/Record-oriented_filesystem.md "wikilink")

[Category:IBM](https://ja.wikipedia.org/wiki/Category:IBM "wikilink") [Category:OSのファイルシステム](https://ja.wikipedia.org/wiki/Category:OSのファイルシステム "wikilink") [Category:データベース](https://ja.wikipedia.org/wiki/Category:データベース "wikilink")
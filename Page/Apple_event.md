> この記事は[Apple event](https://ja.wikipedia.org/wiki/Apple_event)から翻訳されています。


**Apple event**（アップルイベント）は、[アップルの](../Page/アップル_\(企業\).md "wikilink")[Mac OSで採用されている](https://ja.wikipedia.org/wiki/Mac_OS "wikilink")[プロセス間通信](../Page/プロセス間通信.md "wikilink")の[プロトコル](../Page/プロトコル.md "wikilink")**Apple Event Interprocess Messaging Protocol** (AEIMP) で送受信される高水準[イベントである](../Page/イベント_\(プログラミング\).md "wikilink")。System 7（日本語版は漢字Talk7）で初めて採用された。

Apple eventで扱われる「高水準なイベント」とはマウス座標の変化やキーボードの押下といった低水準なものではなく、処理の目的や人間の意向により近い内容を扱うものである。Apple eventは[Finder](https://ja.wikipedia.org/wiki/Finder "wikilink")からの[アプリケーションの起動や書類のオープンなどの日常的な操作のほか](../Page/アプリケーションソフトウェア.md "wikilink")、[AppleScript](../Page/AppleScript.md "wikilink")でも利用されている。

[macOS](https://ja.wikipedia.org/wiki/macOS "wikilink")では[Open Scripting Architecture](https://ja.wikipedia.org/wiki/Open_Scripting_Architecture "wikilink") (OSA) の一部として提供されており、Apple eventは[Mach](../Page/Mach.md "wikilink")メッセージ機構を用いて[プロセス](../Page/プロセス.md "wikilink")間を搬送される。

## 概要

Apple eventはプロセスが自身に対して送信することもできるが、基本的にプロセス間でやりとりされるものである。各プロセスは、システムの機能である**Apple Event Manager**を介してApple eventの送受信を行う。Apple eventは単に送信されるだけでなく、送信されたApple eventに対する返答（結果）を送り主に戻すこともできる。送信先は同一のコンピュータ上のプロセスのほか、[ネットワーク内のコンピュータ上のプロセスも指定でき](https://ja.wikipedia.org/wiki/コンピュータネットワーク "wikilink")、ネットワーク経由の通信は**リモートApple event**または**プログラムリンク**とも呼ばれ、[AppleTalk](https://ja.wikipedia.org/wiki/AppleTalk "wikilink")ネットワークまたは[TCP/IP](https://ja.wikipedia.org/wiki/TCP/IP "wikilink")ネットワークで利用でき、[TCPおよび](../Page/Transmission_Control_Protocol.md "wikilink")[UDPでは](../Page/User_Datagram_Protocol.md "wikilink")3031番の[ポート番号](https://ja.wikipedia.org/wiki/ポート番号 "wikilink")が使われる。

## データ構造

Apple eventには**属性**と**パラメタ**という2種類の情報が格納される。属性はイベントの役割を記したものであり、パラメタはイベントで用いられるデータである。属性とパラメタはApple eventに複数格納でき、[4バイトキャラクタのキーワードによって各項目が識別される](https://ja.wikipedia.org/wiki/FourCC "wikilink")。Apple eventの属性には最低限「**対象プロセス**」と「**イベントクラス**」と「**イベントID**」を特定する情報がなくてはならない。イベントクラスとはイベントの内容をおおまかに分類するものであり、イベントIDとはイベントクラスをさらに細かく分類するものである。Apple eventを言葉に例えるならば、対象プロセスは話しかける相手、イベントクラスとイベントIDは動詞に相当するもの、パラメタは名詞に相当するものと言える。

イベントクラスには基本的な処理を扱う**コアイベントクラス**が定義されており、アプリケーションは最低限、次のようなイベントIDに対応することが推奨されている（注：コアイベントクラスのイベントIDは下記のほかにもある）。

  - kAEOpenApplication ('oapp') - アプリケーションを起動する
  - kAEQuitApplication ('quit') - アプリケーションを終了する
  - kAEOpenDocuments ('odoc') - 書類を開く
  - kAEPrintDocuments ('pdoc') - 書類を印刷する

Apple eventによって扱われるデータは、すべて**Apple eventデスクリプタ**と呼ばれる構造に格納される。Apple eventデスクリプタには、データの種類を識別する「**デスクリプタタイプ**」と、データの本体が格納される。Apple eventデスクリプタに格納できるデータの種類は任意であるが、あらかじめ多くのデスクリプタタイプ（数値、文字列、ファイル参照、オブジェクト指定子など）が定義されているほか、Apple eventデスクリプタはリスト（[配列](../Page/配列.md "wikilink")）やレコード（4バイトキャラクタのキーワードによって項目が識別される[連想配列](../Page/連想配列.md "wikilink")）を格納したり、[入れ子にもできる](https://ja.wikipedia.org/wiki/ネスティング "wikilink")。プログラムで扱われるApple event（送信前のもの、受信したもの）も、レコード型のApple eventデスクリプタの[派生型](../Page/派生型.md "wikilink")である。

## イベント駆動

Apple eventはシステムやプロセスから送信されるほかに、[OSAによっても利用される](https://ja.wikipedia.org/wiki/Open_Scripting_Architecture "wikilink")。Mac OSの[スクリプト言語](../Page/スクリプト言語.md "wikilink")であるAppleScriptもOSAに準拠した言語であり、Apple eventとの関係が密接である。AppleScriptの命令文やオブジェクト参照は、OSAのAppleScriptコンポーネントにより、システム内蔵またはアプリケーション内蔵の**スクリプティング用語辞書**に基づいてApple eventに変換され、対象のアプリケーションへと送信される。よって、アプリケーションがAppleScript（やOSA準拠のスクリプト）での制御に対応するには、それぞれの命令と対称するApple eventのイベントクラスとイベントIDに対応する必要がある。

[プログラミングにおいては](https://ja.wikipedia.org/wiki/プログラミング_\(コンピュータ\) "wikilink")、Apple eventはイベントハンドラ（とりわけ**Apple eventハンドラ**と呼ばれる[プロシージャ](https://ja.wikipedia.org/wiki/プロシージャ "wikilink")）によって、[イベントループ時に受信される](../Page/イベント駆動型プログラミング.md "wikilink")。Apple eventハンドラを実装する必要がある状況は、ほとんどの場合、前述のコアイベントクラスに対応させる時か、AppleScriptに対応させる時である。[Cocoa](../Page/Cocoa.md "wikilink")フレームワークにおいてはApple eventハンドラを意識する必要は少なく、[Mac OS X v10.3以降では](../Page/Mac_OS_X_v10.3.md "wikilink")**Cocoaスクリプティングアーキテクチャ**により、AppleScriptからのApple eventを[キー値コーディング](https://ja.wikipedia.org/wiki/キー値コーディング "wikilink") (KVC) によって処理することも可能になった。

## 関連項目

  - [プロセス間通信](../Page/プロセス間通信.md "wikilink")
  - [Open Scripting Architecture](https://ja.wikipedia.org/wiki/Open_Scripting_Architecture "wikilink")
  - [AppleScript](../Page/AppleScript.md "wikilink")

## 外部リンク

  - [Apple Events Programming Guide](http://developer.apple.com/documentation/AppleScript/Conceptual/AppleEvents/intro_aepg/chapter_1_section_1.html)
  - [Inside Macintosh:Interapplication Communication](http://developer.apple.com/documentation/mac/IAC/IAC-2.html)

[Category:OSのプロセス管理](https://ja.wikipedia.org/wiki/Category:OSのプロセス管理 "wikilink") [Category:Mac_OS](https://ja.wikipedia.org/wiki/Category:Mac_OS "wikilink")
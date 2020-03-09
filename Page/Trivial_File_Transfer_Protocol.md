> この記事は[Trivial File Transfer Protocol](https://ja.wikipedia.org/wiki/Trivial_File_Transfer_Protocol)から翻訳されています。


**Trivial File Transfer Protocol**（トリビアル ファイル トランスファー プロトコル、**TFTP**）は、[UDPを用いてコンピュータ間で](../Page/User_Datagram_Protocol.md "wikilink")[ファイルを転送するための](https://ja.wikipedia.org/wiki/ファイル_\(コンピュータ\) "wikilink")[プロトコル](../Page/プロトコル.md "wikilink")である。[FTPに比べて軽量](../Page/File_Transfer_Protocol.md "wikilink")・単純なプロトコルである。[認証](../Page/認証.md "wikilink")機能が無いためにユーザ名やパスワードを必要としない。[ポート番号](https://ja.wikipedia.org/wiki/ポート番号 "wikilink")69を[デフォルトとして使用する](https://ja.wikipedia.org/wiki/デフォルト_\(コンピュータ\) "wikilink")。

(RIS)や[Preboot Execution Environment](https://ja.wikipedia.org/wiki/Preboot_Execution_Environment "wikilink")(PXE)などのネットワーク・ブート環境において、ディスクレスマシンがブートする際、[BOOTPや](https://ja.wikipedia.org/wiki/Bootstrap_Protocol "wikilink")[DHCPで構成情報を取得した後に](https://ja.wikipedia.org/wiki/Dynamic_Host_Configuration_Protocol "wikilink")、実際のOSコードをサーバから取得する際に利用される。また、ルータなどの設定の読み取りや書き込みなどにも用いられる。

TFTPは1981年に初めて標準化され\[1\]、最新のプロトコルの仕様は RFC 1350 で確認できる。

## 概要

TFTPはシンプルな設計であるため、小さな[メモリー・フットプリント](https://ja.wikipedia.org/wiki/メモリー・フットプリント "wikilink")のコードで簡単に実装できる。そのため、[BOOTP](https://ja.wikipedia.org/wiki/BootP "wikilink")、[PXE](https://ja.wikipedia.org/wiki/PXE "wikilink")、などの[ネットワークブート](https://ja.wikipedia.org/wiki/ネットワークブート "wikilink")の最初のステージのプロトコルとして採用されている。リソースが潤沢なコンピュータから、 [シングルボードコンピュータ](https://ja.wikipedia.org/wiki/シングルボードコンピュータ "wikilink")（Single-board computers; SBC）や[System on a Chip](https://ja.wikipedia.org/wiki/System-on-a-chip "wikilink")（SoC）などのリソースが非常に制限されたコンピュータに至るまで、幅広い対象で使われている。また、[ファームウェア](../Page/ファームウェア.md "wikilink")イメージの転送や、[ルーター](https://ja.wikipedia.org/wiki/ルーター "wikilink")、[ファイアウォール](https://ja.wikipedia.org/wiki/ファイアウォール "wikilink")、[IP電話](https://ja.wikipedia.org/wiki/IP電話 "wikilink")などのネットワーク機器に設定ファイルを転送するためにも使用される。今日では、事実上、インターネット上のデータ転送の用途には使用されていない。

TFTPの設計は、それ以前からある、[プロトコル・スイート](https://ja.wikipedia.org/wiki/プロトコル・スイート "wikilink")の一部であるプロトコルに影響を受けている。TFTPは1980年に 133によって定義された\[2\]。1981年6月、TFTPプロトコル（Revision 2）がRFC783として公開され、その後、1992年7月に公開されたRFC1350でアップデートされ、特に、が修正された。1995年3月、TFTP Option Extension RFC 1782が1998年5月にRFC 2347によってアップデートされ、TFTPの元の仕様と一致する、オプションのネゴシエーションメカニズムを定義した。このメカニズムを使用することで、転送に先立って、ネゴシエーションされるべきファイル転送オプションのためのフレームワークを確立することができる。

TFTPは、番号69を使用してプロトコル上に実装された、ファイル転送用のシンプルなプロトコルである。TFTPは、小型で実装が容易なように設計されているため、その他のより堅牢なファイル転送プロトコルで提供される高度な機能のほとんどが存在しない。TFTPはリモートサーバ間で個々のファイルの読み書きのみを行うため、ファイルやディレクトリを一覧表示、削除、名前変更することはできない。また、ユーザー認証に関しても規定されていない。そのため、現在では、TFTPは通常、[ローカルエリアネットワーク](../Page/Local_Area_Network.md "wikilink")（LAN）でのみ使用される。

## 詳細

[Tftp-wrq.svg](https://ja.wikipedia.org/wiki/File:Tftp-wrq.svg "fig:Tftp-wrq.svg") [Tftp-ack0.svg](https://ja.wikipedia.org/wiki/File:Tftp-ack0.svg "fig:Tftp-ack0.svg") [Tftp-dat1-up.svg](https://ja.wikipedia.org/wiki/File:Tftp-dat1-up.svg "fig:Tftp-dat1-up.svg") [Tftp-rrq.svg](https://ja.wikipedia.org/wiki/File:Tftp-rrq.svg "fig:Tftp-rrq.svg") [Tftp-dat1-dwn.svg](https://ja.wikipedia.org/wiki/File:Tftp-dat1-dwn.svg "fig:Tftp-dat1-dwn.svg") [Tftp-ack1.svg](https://ja.wikipedia.org/wiki/File:Tftp-ack1.svg "fig:Tftp-ack1.svg")

TFTPでは、転送はクライアントがサーバ上の特定のファイルを読み書きする要求を発行することによって開始される。要求には、 RFC 2347 で指定された条件の下で、転送パラメータをオプションで含むことができる。サーバが要求を承認すると、クライアントはファイルを送信する。ファイルは、デフォルトで512バイトの固定長ブロック、または RFC 2348 で定義されているblocksize negotiatedオプションで指定されたバイト数で送信される。[IPフラグメンテーション](https://ja.wikipedia.org/wiki/IPフラグメンテーション "wikilink")を回避するために、通常、単一のIPパケット内で搬送される転送データの各ブロックは、次のブロックが送信される前に確認パケットによって確認応答されなければならない。512バイト（またはオプションで指定されたブロックサイズ）未満のデータパケットそ送信することにより、転送の終了を知らせる。パケットがネットワーク内で紛失した場合には、再送処理が行われる。送信側でデータ転送後に確認パケットの受信がタイムアウトした場合、直前のデータブロックを再送する。受信側で確認パケット送信後に次のデータブロックの受信がタイムアウトした場合、直前の確認応答を再送する。このようなの確認応答によって、それまでに送信した全てのパケットが正しく受信されたことが保証される。送信側は再送信用に1つのパケットのみを保持する必要がある。TFTPにおいては、転送に関与する両方のデバイスが、送信者・受信者のどちらの立場にもなる。一方はデータを送信して確認応答を受信し、もう一方は確認応答を送信してデータを受信する。

TFTPでは、netascii、octet、mailの3つの転送モードを定義する。

1.  netascii転送モードは、 RFC 764 で定義されている[ASCII](https://ja.wikipedia.org/wiki/ASCII "wikilink")の修正形式である。これは、0x20から0x7Fまでの7ビットASCII文字空間の8ビット拡張（印刷可能文字とスペース）および8つの[制御文字](https://ja.wikipedia.org/wiki/制御文字 "wikilink")で構成されている。許容される制御文字には、ヌル（0x00）、改行（LF、0x0A）、キャリッジリターン（CR、0x0D）がある。netasciiでは、ホスト上の行末マーカーを転送のために"CR LF"に変換し、すべてのCRの後にLFまたはヌルを付ける必要がある。
2.  octet転送モードは、任意の生の8ビットバイトの転送を可能にし、受信ファイルは結果として送信されたものとバイト対バイトで同じになる。より正確には、ホストがオクテットファイルを受信してそれを返した場合、返されたファイルは元のファイルと同一でなければならない\[3\]。
3.  mail転送モードはnetascii転送を使用するが、ファイル名として受信者のEメールアドレスを指定することで、ファイルはEメール受信者に送信される。 RFC 1350 では、この転送モードは廃止したと宣言された。

TFTPは[トランスポート層](https://ja.wikipedia.org/wiki/トランスポート層 "wikilink")プロトコルとして[UDPを使用する](../Page/User_Datagram_Protocol.md "wikilink")。転送要求は常に[ポート](https://ja.wikipedia.org/wiki/ポート_\(コンピュータネットワーク\) "wikilink")69を対象として開始されるが、データ転送に使用するポートは、転送の初期化中に送信側と受信側によって個別に選択される。ポート番号は、ネットワーキングスタックのパラメータに従って、通常は[エフェメラルポート](https://ja.wikipedia.org/wiki/エフェメラルポート "wikilink")の範囲からランダムに選択される\[4\]。

1.  開始ホストAは、ポート番号69でホスト名SにRRQ（読み取り要求）またはWRQ（書き込み要求）パケットを送信する。このパケットには、ファイル名、転送モードのほか、オプションで RFC 2347 の規定に基づく任意のネゴシエーションオプションが含まれる。
2.  Sは、オプションが使用された場合にはオプションACK、WRQに対してはACK（確認応答）パケットを送信し、RRQに対しては直接データパケットを送信することで応答する。パケットはランダムに割り当てられたエフェメラルポートから送信され、これ以降のホストSへのパケットは全てこのポートに転送される。
3.  送信元ホストは、番号付きのデータパケットを送信先ホストに送信する。最後のパケット以外には、フルサイズのデータブロック（デフォルトでは512バイト）が含まれている。宛先ホストは、すべてのデータパケットに対して番号付きのACKパケットで応答する。
4.  最後のデータパケットは、フルサイズのデータブロック以下でなければならない。これによって、それが最後のデータパケットであることを相手に知らせる。転送されたファイルのサイズがブロックサイズの正確な倍数である場合は、送信元は最後に0バイトのデータを含むデータパケットを送信する。
5.  受信側は、対応するデータパケットと同じ番号をつけたACKパケットを送信することで、データパケットに対し確認応答する。送信側は、受信したACKパケットに対し、次のデータパケットを送信することで確認応答する。
6.  ACKパケットが受信されず、再送信タイマーがタイムアウトした場合、データパケットを再送信する。

TFTPは常にネットワーク起動に関連付けられている。1984年に公開されたTFTP標準を使用したブートストラップロード RFC 906 では、1981年に公開されたTrivial File Transfer Protocol標準 RFC 783をブートストラップロードの標準ファイル転送プロトコルとして使用することを定めている。1985年に公開された[Bootstrap Protocol](https://ja.wikipedia.org/wiki/Bootstrap_Protocol "wikilink")(BOOTP)標準 RFC 951により、ディスクレスクライアントマシンが自身のIPアドレス、TFTPサーバのアドレス、ネットワークブートストラッププログラム(NBP)の名前をTFTP転送し、メモリにロードして実行することができるようになった。1997年に発行された[Dynamic Host Configuration Protocol](https://ja.wikipedia.org/wiki/Dynamic_Host_Configuration_Protocol "wikilink")(DHCP)標準 RFC 2131では、BOOTP機能を改善した。最後に、[Preboot Execution Environment](https://ja.wikipedia.org/wiki/Preboot_Execution_Environment "wikilink")(PXE)バージョン2.0が1998年12月にリリースされ、ファイル転送プロトコルとしてTFTPを利用するアップデート2.1が1999年9月に公表された\[5\]。インテルは最近、新しい[UEFIの仕様内でPXEを広くサポートすることを決定した](https://ja.wikipedia.org/wiki/Unified_Extensible_Firmware_Interface "wikilink")。これは、TFTPへの対応を全てのEFI/UEFI環境に拡張するものである\[6\]\[7\]。

元のプロトコルでは、転送ファイルサイズの上限は512バイト/ブロック×65535ブロック = 32 MBである。1998年には、TFTP Blocksize Option RFC 2348 によってこの制限は65535バイト/ブロック×65535ブロック = 4.294 GBに拡張された。定義されたブロックサイズがネットワークパスにおける最小の[MTUを超えるIPパケットサイズを生成する場合](https://ja.wikipedia.org/wiki/Maximum_transmission_unit "wikilink")、IPの断片化と再構成が発生し、オーバーヘッドが増える\[8\]だけでなく、ホストのBOOTPに最小のIPスタックが実装されたかPXE ROMがIPの断片化と再構成を実装していないときに転送が失敗する\[9\]。

TFTPパケットを標準のイーサネットMTU（1500）以内に保持する必要がある場合、ブロック値は1500からTFTPのヘッダ（4バイト）、UDPヘッダ（8バイト）、IPヘッダ（20バイト）を引いて1468バイト/ブロックと計算され、制限は1468バイト/ブロック×65535ブロック = 92 MBとなる。今日、ほとんどのサーバとクライアントはブロック番号のロールオーバー（65535の後にブロックカウンタが0または1に戻る\[10\]）に対応しており、これにより、本質的に無制限の転送ファイルサイズを与えることができる。

TFTPはUDPを利用するため、独自のトランスポート層およびセッション層のサポートを提供する必要がある。TFTPを介して転送された各ファイルは、独立した交換を構成する。古典的には、この転送はロックステップで実行され、1つのパケット （データブロックまたは確認応答）だけがネットワーク上を随時送信される。大量のデータブロックを送信してから転送を一時停止して確認応答を待つ（ウィンドウイング）のではなく、単一のデータブロック戦略を取ることにより、TFTPでは[スループット](../Page/スループット.md "wikilink")が低く[レイテンシ](https://ja.wikipedia.org/wiki/レイテンシ "wikilink")が大きくなる。Microsoftは、Windows 2008にWindows展開サービス(WDS)の一部としてウィンドウ化TFTPを導入し、2015年1月にTFTP Windowsize Option RFC 7440 が公開された。これにより、Blocksize Option RFC 2348 \[11\]で時々見られるIPフラグメンテーションの副作用なしに、PXEブートなどをする際のパフォーマンスをかなり改善する。

## セキュリティ上の注意点

TFTPにはログインやアクセスのコントロールを行うメガニズムが実装されていない。TFTPでファイル転送する際に、認証、アクセスコントロール、秘密保持、完全性のチェックが必要な場合には、補助的な処理が必要になる。こうした機能は、TFTPが実行される上下のいずれかのレイヤーで実装することは可能ではあるが、TFTPは通常、パブリックな読み込みアクセスが可能なファイルのインストールにしか使われない。また、ファイルの一覧、削除、名前変更、書き込みは通常不可能である。プロトコル固有の制限が問題となる場合には、TFTPを使用したファイル転送は推奨されない\[12\]。

## IETF標準ドキュメント

| RFC番号    | タイトル                                            | 公開日     | 著者             | 廃止・更新情報                                                                 |
| -------- | ----------------------------------------------- | ------- | -------------- | ----------------------------------------------------------------------- |
| RFC 783  | The TFTP Protocol (Revision 1)                  | 1981年6月 | K. Sollins     | RFC 1350 により廃止された                                                       |
| RFC 906  | Bootstrap Loading using TFTP                    | 1984年6月 | Ross Finlayson | \-                                                                      |
| RFC 951  | Bootstrap Protocol                              | 1985年9月 | Bill Croft     | RFC 1395、RFC 1497、RFC 1532、RFC 1542、RFC 5494 により更新された                   |
| RFC 1350 | The TFTP Protocol (Revision 2)                  | 1992年7月 | K. Sollins     | RFC 1782、RFC 1783、RFC 1784、RFC 1785、RFC 2347、RFC 2348、RFC 2349 により更新された |
| RFC 1782 | TFTP Option Extension                           | 1995年3月 | G. Malkin      | RFC 2347 により廃止された                                                       |
| RFC 2131 | Dynamic Host Configuration Protocol             | 1997年3月 | R. Droms       | RFC 3396、RFC 4361、RFC 5494、RFC 6842 により更新された                            |
| RFC 2347 | TFTP Option Extension                           | 1998年5月 | G. Malkin      | \-                                                                      |
| RFC 2348 | TFTP Blocksize Option                           | 1998年5月 | G. Malkin      | \-                                                                      |
| RFC 2349 | TFTP Timeout Interval and Transfer Size Options | 1998年5月 | G. Malkin      | \-                                                                      |
| RFC 5505 | Principles of Internet Host Configuration       | 2009年5月 | B. Aboba       | \-                                                                      |
| RFC 7440 | TFTP Windowsize Option                          | 2015年1月 | P. Masotta     | \-                                                                      |
|          |                                                 |         |                |                                                                         |

## 関連項目

  -
  - [Preboot Execution Environment](https://ja.wikipedia.org/wiki/Preboot_Execution_Environment "wikilink")

## RFCへのリンク

  - RFC 1350 - THE TFTP PROTOCOL (REVISION 2) (RFC 783 を廃止)
  - RFC 1785 - TFTP Option Negotiation Analysis
  - RFC 2347 - TFTP Option Extension (RFC 1782 を廃止)
  - RFC 2348 - TFTP Blocksize Option (RFC 1783 を廃止)
  - RFC 2349 - TFTP Timeout Interval and Transfer Size Options (RFC 1784 を廃止)

## 出典

<references />

[Category:RFC](https://ja.wikipedia.org/wiki/Category:RFC "wikilink") [Category:ファイル転送プロトコル](https://ja.wikipedia.org/wiki/Category:ファイル転送プロトコル "wikilink")

1.  RFC 783
2.
3.  RFC 1350, page 5.
4.
5.
6.
7.
8.  RFC 2348, page 3.
9.  RFC 5505, page 7.
10.
11. RFC 7440, page 1.
12. RFC 7440, page 7.
> この記事は[File Transfer Protocol](https://ja.wikipedia.org/wiki/File_Transfer_Protocol)から翻訳されています。


**File Transfer Protocol**（ファイル・トランスファー・プロトコル、**FTP**、ファイル転送プロトコル）は、[コンピュータネットワーク](../Page/コンピュータネットワーク.md "wikilink")上の[クライアントとサーバの間で](../Page/クライアントサーバモデル.md "wikilink")[ファイル転送](https://ja.wikipedia.org/wiki/ファイル転送 "wikilink")を行うための[通信プロトコル](../Page/通信プロトコル.md "wikilink")の一つである。

## 概説

[インターネット](../Page/インターネット.md "wikilink")初期の頃から存在するプロトコルで、今でもインターネットでよく使用される[通信プロトコル](../Page/通信プロトコル.md "wikilink")の1つである。FTPはクライアントサーバモデルのアーキテクチャとして設計されており、クライアントとサーバの間で制御用とデータ転送用の2つの別のコネクションを使用する\[1\]。

FTPでは、[認証](../Page/認証.md "wikilink")のためのユーザ名・パスワードや転送データは[暗号化](https://ja.wikipedia.org/wiki/暗号化 "wikilink")されず、[平文](../Page/平文.md "wikilink")でやり取りされる。そのため現在では、FTPの通信を[SSL/TLSにより保護した](../Page/Transport_Layer_Security.md "wikilink")[FTPS](../Page/FTPS.md "wikilink")や、[SSHの仕組みを利用した](../Page/Secure_Shell.md "wikilink")[SSH File Transfer Protocol](../Page/SSH_File_Transfer_Protocol.md "wikilink")(SFTP)などの代替のプロトコルに置き換えられている。

用途としては

  - ウェブページ用各種データファイル（[HTMLソース](../Page/HyperText_Markup_Language.md "wikilink")、[画像](../Page/画像.md "wikilink")など）のクライアントのパソコンから[ウェブサーバへのアップロード](../Page/Webサーバ.md "wikilink")
  - パソコンソフト配布サイトや、データが入っているFTPファイルサーバからクライアントへのファイルのダウンロード

などに使われる。 ダウンロードについては、[アップロード](../Page/アップロード.md "wikilink")についてはFTPクライアントソフトや[CUIコマンドが必要となる](../Page/キャラクタユーザインタフェース.md "wikilink")。多くの[ブラウザソフトにはダウンロードに特化したFTPクライアントソフトの機能が実装されている](../Page/ウェブブラウザ.md "wikilink")。

初期の[FTPクライアント](../Page/FTPクライアント.md "wikilink")は、[OSが](../Page/オペレーティングシステム.md "wikilink")[GUIを持っていなかった時期に開発された](https://ja.wikipedia.org/wiki/グラフィカルユーザインタフェース "wikilink")[コマンドラインプログラムであり](../Page/キャラクタユーザインタフェース.md "wikilink")、今でもほとんどのOSに同梱されている\[2\]\[3\]。多くのFTPクライアントや自動化ユーティリティが開発されており、また、[HTMLエディタ](https://ja.wikipedia.org/wiki/HTMLエディタ "wikilink")などの生産性アプリケーションにも組み込まれてきた。

## 歴史

FTPの元の仕様は[アバイ・ブーシャン](https://ja.wikipedia.org/wiki/アバイ・ブーシャン "wikilink")によって書かれ、1971年4月16日にとして公開された。1980年まで、FTPは[TCP/IP](https://ja.wikipedia.org/wiki/TCP/IP "wikilink")の前身である[NCPで実行されていた](../Page/Network_Control_Program.md "wikilink")\[4\]。（1980年6月）と（1985年10月）によりFTPはTCP/IP上で動くバージョンに修正され、これが現行のFTPの仕様の元となっている。その後、（1994年2月）で[ファイアウォール](../Page/ファイアウォール.md "wikilink")内からでも使用できるパッシブモードが追加され、（1997年6月）ではセキュリティ拡張が提案された。（1998年9月）では[IPv6](https://ja.wikipedia.org/wiki/IPv6 "wikilink")に対応し、新しい種類のパッシブモードが定義された\[5\]。

## プロトコルの概要

### 通信とデータ転送

[Passive_FTP_Verbindung.svg](https://ja.wikipedia.org/wiki/File:Passive_FTP_Verbindung.svg "fig:Passive_FTP_Verbindung.svg") FTPの動作モードには、データ転送用コネクションの確立方法の違いにより**アクティブモード**(active mode)と**パッシブモード**(passive mode)がある\[6\]。どちらの場合でも、データ転送用コネクションとは別に制御用コネクションを使用する。制御用コネクションは、クライアント側が、特権付きでないランダムな[ポート番号Nから](../Page/ポート_\(コンピュータネットワーク\).md "wikilink")、サーバのポート21へのTCPのコネクションとして確立する。

  - アクティブモード（ポートモードとも言う）では、クライアントが制御用コネクションでFTPコマンド"PORT M"（Mはポート番号）をサーバに送信してポート番号を通知し、通知したポートMでサーバからのデータ転送用コネクションの接続を待ち受ける。サーバはポート20（FTPサーバのデータポート）からクライアントへのデータ転送用コネクションを確立する。
  - [ファイアウォール](../Page/ファイアウォール.md "wikilink")や[NAT](../Page/ネットワークアドレス変換.md "wikilink")（[IPマスカレード](https://ja.wikipedia.org/wiki/IPマスカレード "wikilink")）などを使った環境では場合によってはアクティブモードでは接続できないこともある。この場合はパッシブモードを使用する。このモードでは、クライアントは制御用コネクションで"PASV"コマンドをサーバに送信してパッシブモードを利用することを通知し、サーバはクライアントにサーバ側のIPアドレスとポート番号を通知する\[7\]。クライアントはサーバから通知されたIPアドレスとポート番号へデータ転送用コネクションを確立する\[8\]。

1998年9月に、両方のモードは[IPv6](https://ja.wikipedia.org/wiki/IPv6 "wikilink")に対応するために更新され、パッシブモードには変更が加えられて拡張パッシブモード(extended passive mode)となった\[9\]。

サーバは、制御用コネクションを介してASCIIの3桁の数字のステータスコードで応答する。ステータスコードにはテキストによるメッセージがつくことがある。例えば、"200"（または "200 OK"）は、最後のコマンドが成功したことを意味する。数字は応答のコードを表し、追加のテキストは人間が読める説明または要求を表す\[10\]。データ転送用コネクションを介したファイルデータの転送中、制御用コネクションを介して割り込みメッセージを送信することによって転送を中止することができる。

データ転送には以下の4つのデータ表現が利用できる\[11\]\[12\]\[13\]。

  - [ASCII](../Page/ASCII.md "wikilink")モード: テキストデータに使用される。必要に応じて、送信側で送信ホストの文字表現から[拡張ASCII](../Page/拡張ASCII.md "wikilink")に変換され、受信側では受信ホストの文字表現に変換される。そのため、このモードはプレーンテキスト以外のデータを含むファイルには不適切である。
  - バイナリモード（イメージモードとも言う）: 送信側のマシンは各ファイルを[バイト単位で送信し](../Page/バイト_\(情報\).md "wikilink")、受信側はを保存する。送信側・受信側ともデータの変換を行わない。FTPの全ての実装に対してバイナリモードの対応が推奨されている。
  - [EBCDIC](https://ja.wikipedia.org/wiki/EBCDIC "wikilink")モード: EBCDIC文字セットを使用しているホスト間のプレーンテキストに使用される。
  - ローカルモード: 同じ設定の2台のコンピュータが独自のフォーマットでデータをASCIIに変換することなく送信できるようにする。

データ転送は以下の3つのモードのいずれかで行うことができる\[14\]\[15\]。

  - ストリームモード: データは連続したストリームとして送信される。FTPとしては処理は行わず、全ての処理を[TCPに任せる](../Page/Transmission_Control_Protocol.md "wikilink")。 データがレコードに分割されていない限り、[End-of-file](https://ja.wikipedia.org/wiki/End-of-file "wikilink")標識は必要ない。
  - ブロックモード: FTPはデータをいくつかのブロック（ブロックヘッダ、バイト数、データフィールドから構成される）に分割してからTCPに渡す\[16\]。
  - 圧縮モード: 単純なアルゴリズム（通常は[連長圧縮](../Page/連長圧縮.md "wikilink")）でデータを圧縮してからTCPに渡す。

FTPソフトウェアの中には、「モードZ」と呼ばれる[Deflate](../Page/Deflate.md "wikilink")を使用した圧縮モードを実装しているものがある。このモードは[インターネットドラフト](https://ja.wikipedia.org/wiki/インターネットドラフト "wikilink")に記載されているが、標準化はされていない\[17\]。

### ログイン

FTPログインは、アクセスを許可するために通常のユーザ名とパスワードのスキームを使用する\[18\]。ユーザ名はUSERコマンドを使用してサーバに送信され、パスワードはPASSコマンドを使用して送信される\[19\]。この一連のやり取りは[暗号化](https://ja.wikipedia.org/wiki/暗号化 "wikilink")されていないため、に対して脆弱である\[20\]。クライアントから提供された情報がサーバによって受け入れられた場合、サーバはクライアントにグリーティングを送信し、セッションが開始される\[21\]。

### Anonymous FTP

FTPサービスを提供するホストは、専らファイル（主に無償の[フリーソフトなど](../Page/フリーウェア.md "wikilink")）を配布する目的で\[22\]、[匿名](../Page/匿名.md "wikilink")でアクセスできるAnonymousアクセスを提供することができる\[23\]。この場合でも形式上認証が必要であり、ユーザ名として"anonymous"または"ftp"を指定する。パスワードは通常何でもよいが、配布したソフトに瑕疵があった場合などにサーバ管理者が連絡をとることができるよう、ユーザの[電子メールアドレスを指定するのがマナー](../Page/メールアドレス.md "wikilink")（[ネチケット](../Page/ネチケット.md "wikilink")）とされてきた（メールアドレスの[ドメインがクライアントの](../Page/ドメイン名.md "wikilink")[IPアドレス](../Page/IPアドレス.md "wikilink")の逆引きなどから明らかな場合は、"foo@"のようにドメインを省略することも多い）\[24\]。サーバによっては、パスワードがメールアドレスの形式を満たさないと利用できないこともある。しかし、近年では[スパム（迷惑メール）などの問題により](../Page/スパム_\(メール\).md "wikilink")、むやみにメールアドレスを公開しない風潮が高まっていることから、このマナーは廃れつつある。また、現在ではFTPクライアント機能を備えた[ウェブブラウザ](../Page/ウェブブラウザ.md "wikilink")で匿名FTPサーバにアクセスすることも多く、この場合パスワードは特に指定しない限りブラウザのデフォルト設定（[Internet Explorerであれば](../Page/Internet_Explorer.md "wikilink")"IEuser@"など）が使われ、メールアドレスとして意味のあるものにはならない。

### NATやファイアウォールの通過

FTPは通常、クライアントがPORTコマンドを送信し、サーバがクライアントの通知されたポートに接続することによってデータを転送する。これは、インターネット側から内部ホストへの接続を許可しない[NATや](../Page/ネットワークアドレス変換.md "wikilink")[ファイアウォール](../Page/ファイアウォール.md "wikilink")において問題となる\[25\]。NATの場合、PORTコマンドで通知するIPアドレスとポート番号は、NATによる変換後のものではなく、変換前のものとなる。

この問題を解決するには2つの方法がある。1つは、PASVコマンドを使用してパッシブモードに移行する方法である。これにより、FTPクライアント側からサーバへデータ転送用コネクションが確立される\[26\]。これは現代のFTPクライアントにおいて広く使われている。もう1つは、NATがを使用してPORTコマンドの値を書き換える方法である\[27\]。

### HTTPとの違い

FTPでは、Webページでよく見られるような多くの小さな一時的な転送に使用するのが不便であり、[HTTPではそれを修正している](../Page/Hypertext_Transfer_Protocol.md "wikilink")。

FTPには、現在の作業ディレクトリと他のフラグを保持するステートフルな制御用コネクションがあり、転送するファイルごとに、データを転送するための別のコネクションを必要とする。パッシブモードでは、この別のコネクションはクライアントからサーバへの接続であるが、デフォルトのアクティブモードでは、このコネクションはサーバからクライアントへの接続である。アクティブモードにおけるこの役割の逆転、および全ての転送において使用されるポート番号がランダムであることが、ファイアウォールやNATゲートウェイを通してFTPを使用することを困難にしている。HTTPはステートレスであり、クライアントからサーバへの、Well-knownなポート番号による単一のコネクションを介して、制御とデータを多重化する。これにより、NATゲートウェイやファイアウォールの通過が簡単になる。

FTPの制御用コネクションの設定は、必要な全てのコマンドを送信して応答を待つまでに往復遅延があるため、非常に遅くなる。そのため、毎回セッションを破棄して再確立するのではなく、制御用コネクションを確立した後、それを複数のファイル転送のために開いたままにするのが一般的である。これとは対照的に、HTTPはその方が安価であるため、元々転送ごとにコネクションを切断していた。その後、HTTPには複数の転送に1つのTCP接続を再利用する機能が追加されたが、概念モデルとしてはセッションではなく独立した要求である。

FTPがデータ用コネクションを介して転送している間、制御用コネクションはアイドル状態である。転送に時間がかかりすぎると、ファイアウォールやNATは制御用コネクションが無効であると判断してそれを追跡しなくなり、事実上接続が切断されてしまう。HTTP接続においてはアイドル状態となるのは要求と要求の間のみであり、タイムアウトした後にコネクションがドロップされるのは正常で、予期されたものである。

## Webブラウザの対応

ほとんどの一般的な[Webブラウザ](https://ja.wikipedia.org/wiki/Webブラウザ "wikilink")は、FTPサーバに格納されているファイルを取得することができる。ただし[FTPS](../Page/FTPS.md "wikilink")などのプロトコル拡張には対応していない場合もある\[28\]\[29\]。HTTPではなくFTPの[URL](https://ja.wikipedia.org/wiki/URL "wikilink")が指定された場合、リモートサーバ上のアクセス可能なコンテンツは他のWebコンテンツに使用されているものと同様の方法で表示される。[Firefox](https://ja.wikipedia.org/wiki/Firefox "wikilink")には、と呼ばれるフル機能のFTPクライアントの[プラグイン](../Page/プラグイン.md "wikilink")が存在する。

### URLの表記

FTPのURLの構文はで定義されており、[`ftp://[user`](ftp://%5Buser)`[:password]@]host[:port]/url-path`の形となる（括弧で囲まれた部分はオプション）。

例えば、ftp://public.ftp-servers.example.com/mydirectory/myfile.txtというURLは、FTPサーバ*public.ftp-servers.example.com*上のディレクトリ*mydirectory*にあるファイル*myfile.txt*を表す。ftp://user001:secretpassword@private.ftp-servers.example.com/mydirectory/myfile.txtというURLでは、このFTPサーバへのアクセスに必要となるユーザ名(*user001*)とパスワード(*secretpassword*)の指定が追加されている。

ユーザ名とパスワードの指定に関する詳細は、ブラウザのドキュメントにある（[Firefox](https://ja.wikipedia.org/wiki/Firefox "wikilink")\[30\]、[Internet Explorer](../Page/Internet_Explorer.md "wikilink")\[31\]）。デフォルトでは、ほとんどのWebブラウザは、ファイアウォールをより簡単に通過できるようにするために、パッシブモードを使用する。

## セキュリティ

FTPは、インターネット初期から存在する古いプロトコルであり、[セキュア](https://ja.wikipedia.org/wiki/情報セキュリティ "wikilink")（安全）なプロトコルとして設計されていない。ユーザ名やパスワードなどの認証情報を含むすべての通信内容を暗号化せずに転送するなどの問題の他、数多くのセキュリティ脆弱性が指摘されている\[32\]。（1999年5月）では、以下の脆弱性が列挙されている。

  - [総当たり攻撃](../Page/総当たり攻撃.md "wikilink")

  -
  - [パケットキャプチャ](https://ja.wikipedia.org/wiki/パケットキャプチャ "wikilink")

  - Port stealing（次に開いているポートを推測して正当なコネクションを奪う）

  - [スプーフィング攻撃](https://ja.wikipedia.org/wiki/スプーフィング攻撃 "wikilink")

  - ユーザ名保護

  - [DoS攻撃](../Page/DoS攻撃.md "wikilink")

FTPは通信内容を暗号化できない。全ての送信は平文で行われるため、通信経路上でパケットを[キャプチャすることで](https://ja.wikipedia.org/wiki/パケットキャプチャ "wikilink")、ユーザ名・パスワード・コマンド・データといった情報を容易に盗聴できる\[33\]\[34\]。この問題は、[TLS/SSLなどの暗号化メカニズムが開発される前に設計された他のインターネットプロトコル仕様](../Page/Transport_Layer_Security.md "wikilink")（[SMTP](https://ja.wikipedia.org/wiki/SMTP "wikilink")、[Telnet](../Page/Telnet.md "wikilink")、[POP](../Page/Post_Office_Protocol.md "wikilink")、[IMAP](https://ja.wikipedia.org/wiki/IMAP "wikilink")など）でも同様である\[35\]。

この問題に対する一般的な解決策は、次の通りである。

1.  安全なバージョンのプロトコルを使用する。例えば、FTPの代わりに[FTPS](../Page/FTPS.md "wikilink")、Telnetの代わりにTelnetSを使用する。
2.  [SSH File Transfer Protocol](../Page/SSH_File_Transfer_Protocol.md "wikilink")(SFTP)や[Secure Copy Protocol](https://ja.wikipedia.org/wiki/Secure_Copy_Protocol "wikilink")(SCP)など、ジョブを処理できるより安全なプロトコルを使用する。
3.  [Secure Shell](../Page/Secure_Shell.md "wikilink")(SSH)や[VPNなどのセキュアトンネルを使用する](../Page/Virtual_Private_Network.md "wikilink")。

FTPは、[Gumblar](https://ja.wikipedia.org/wiki/Gumblar "wikilink")などのコンピュータウイルスの標的にもされた。そのため、現在では、FTPではなく前述の [FTPS](../Page/FTPS.md "wikilink") (SSL/TLSを使ったFTP) や [SFTP](https://ja.wikipedia.org/wiki/SFTP "wikilink") ([SSH](../Page/Secure_Shell.md "wikilink") File Transfer Protocol)、[SCP](../Page/Secure_copy.md "wikilink")、[SSH上での](../Page/Secure_Shell.md "wikilink")[rsync](https://ja.wikipedia.org/wiki/rsync "wikilink")、など暗号化された手法を用いることが強く推奨される。

### FTP over SSH

FTP over SSHは、[Secure Shell接続を介して通常のFTPセッションをトンネリングする方法である](../Page/Secure_Shell.md "wikilink")\[36\]。FTPは複数のTCP接続を使用するため、SSHを介してトンネリングすることは特に困難である。多くのSSHクライアントでは、制御チャネル（ポート21による最初のクライアントとサーバの間の接続）用にトンネルを設定しようとすると、そのチャネルだけが保護される。データを転送するときは新しいTCP接続（データチャネル）を確立するため、[機密性](https://ja.wikipedia.org/wiki/機密性 "wikilink")や[完全性の保護はない](../Page/データ完全性.md "wikilink")。

そのため、SSHクライアントソフトウェアがFTPプロトコルの情報を持ち、FTP制御チャネルのメッセージを監視して書き換え、FTPデータチャネルのための新しいパケット転送を自律的に開く必要がある。

## 派生プロトコル

### FTPS

明示的FTPS(Explicit FTPS)は、クライアントがFTPセッションの暗号化を要求できるようにするFTP標準の拡張である。これは、"AUTH TLS"コマンドを送ることによって行われる。サーバには、TLSを使用しない接続の許可・拒否のオプションがある。このプロトコル拡張は、で定義されている。

暗黙的FTPS(Implicit FTPS)は、SSL/TLS接続の使用を必要するFTPの古い標準であり、通常のFTPとは異なるポートを使用するように指定されていた。

### SFTP

SSH File Transfer Protocol(SFTP)は、ファイル転送に[Secure Shell](../Page/Secure_Shell.md "wikilink")(SSH)プロトコルを使用する。FTPとは異なり、コマンドとデータの両方を暗号化し、パスワードや機密情報がネットワークを介して公に送信されるのを防ぐ。FTPサーバやクライアントとは相互運用できない。

### TFTP

Trivial File Transfer Protocol(TFTP)は、クライアントがリモートホストからファイルを取得したり、リモートホストにファイルを保存したりすることを可能にする単純なロックステップのFTPである。TFTPは認証を行わないため実装が非常に簡単であり、主に[ネットワークブート](https://ja.wikipedia.org/wiki/ネットワークブート "wikilink")の初期段階で使用される。TFTPは1981年に最初に標準化された。TFTPの現在の仕様はである。

### Simple File Transfer Protocol

Simple File Transfer Protocolは、TFTPとFTPの中間的なレベルの複雑さを持つ（セキュアではない）FTPとして提案された。で定義されている。このプロトコルもSSH File Transfer Protocolと同様"SFTP"と略称されるが、この略称を持つプロトコルの中ではSimple File Transfer Protocolの方が先に標準化されている。このプロトコルはインターネットで広く受け入れられず、このRFCは[IETFによって](../Page/Internet_Engineering_Task_Force.md "wikilink")"Historic"（歴史的文書）の状態とされている。

ポート115を介して実行され、多くの場合SFTPの初期設定を受信する。11のコマンドと、ASCII・バイナリ・連続の3つのデータ転送を持つ。 ワードサイズが8ビットの倍数であるシステムでは、バイナリモードと連続モードの実装は同じである。このプロトコルは、ユーザーIDとパスワードによるログイン、階層フォルダーとファイル管理（名前の変更、削除、アップロード、ダウンロード、上書きダウンロード、追加ダウンロード）に対応する。

## その他の同様の目的に使えるプロトコル

  - [HTTP](../Page/Hypertext_Transfer_Protocol.md "wikilink")/[WebDAV](../Page/WebDAV.md "wikilink")
  - [Secure copy](../Page/Secure_copy.md "wikilink")(SCP)
  - [Rcp](https://ja.wikipedia.org/wiki/Rcp "wikilink")
  - [rsync](https://ja.wikipedia.org/wiki/rsync "wikilink")
  - [Network File System](../Page/Network_File_System.md "wikilink")(NFS)
  - [Server Message Block](../Page/Server_Message_Block.md "wikilink")(SMB)/[CIFS](../Page/Server_Message_Block.md "wikilink") ([Samba](../Page/Samba.md "wikilink"))

## FTPコマンド

## FTPリターンコード

FTPサーバから返されるリターンコードはで標準化されている。リターンコードは3桁の数値である。

1桁目は、成功、失敗、エラー・不完全な応答のいずれかを示す。

  - 2yz – 成功応答
  - 4yz, 5yz – 失敗応答
  - 1yz, 3yz – エラー・不完全な応答

2桁目は、エラーの種類を表す。

  - x0z – 構文。構文エラーを表す。
  - x1z – 情報。情報の要求に応答する。
  - x2z – コネクション。制御用コネクションやデータ用コネクションに関するエラーを表す。
  - x3z – 認証とアカウント。ログインプロセスとアカウントに関するエラーを表す。
  - x4z – 未定義。
  - x5z – ファイルシステム。サーバのファイルシステムからのステータスコードを中継する。

3桁目は、2桁目で定義されている各カテゴリの詳細情報を提供するために使用される。

## 関連項目

  - [FTPサーバ](../Page/FTPサーバ.md "wikilink")

  - [FTPクライアント](../Page/FTPクライアント.md "wikilink")

  -
  - [File eXchange Protocol](https://ja.wikipedia.org/wiki/File_eXchange_Protocol "wikilink") (FXP)

  - (FSP)

  - [FTAM](https://ja.wikipedia.org/wiki/FTAM "wikilink")

  -
  - [Archie](../Page/Archie.md "wikilink")

  -
  - [OBEX](../Page/OBEX.md "wikilink")

  - [共有資源](https://ja.wikipedia.org/wiki/共有資源 "wikilink")

  - [TCP Wrapper](../Page/TCP_Wrapper.md "wikilink")

## 脚注

## 参考文献

  - – CWD Command of FTP. July 1975.

  - – (Standard) File Transfer Protocol (FTP). J. Postel, J. Reynolds. October 1985.

  - – (Informational) Firewall-Friendly FTP. February 1994.

  - – (Informational) How to Use Anonymous FTP. May 1994.

  - – FTP Operation Over Big Address Records (FOOBAR). June 1994.

  - – Uniform Resource Locators (URL). December 1994.

  - – (Proposed Standard) FTP Security Extensions. October 1997.

  - – (Proposed Standard) Feature negotiation mechanism for the File Transfer Protocol. August 1998.

  - – (Proposed Standard) Extensions for IPv6, NAT, and Extended passive mode. September 1998.

  - – (Informational) FTP Security Considerations. May 1999.

  - – (Proposed Standard) Internationalization of the File Transfer Protocol. July 1999.

  - – (Proposed Standard) Extensions to FTP. P. Hethmon. March 2007.

  - – (Proposed Standard) FTP Command and Extension Registry. March 2010.

  - – (Proposed Standard) File Transfer Protocol HOST Command for Virtual Hosts. March 2014.

  - [IANA FTP Commands and Extensions registry](https://www.iana.org/assignments/ftp-commands-extensions/ftp-commands-extensions.xhtml) – The official registry of FTP Commands and Extensions

## 外部リンク

  -
  - \[//servertest.online/ftp FTP Server Online Tester\] Authentication, encryption, mode and connectivity.

[Category:File_Transfer_Protocol](https://ja.wikipedia.org/wiki/Category:File_Transfer_Protocol "wikilink") [Category:アプリケーション層プロトコル](https://ja.wikipedia.org/wiki/Category:アプリケーション層プロトコル "wikilink") [Category:インターネット標準](https://ja.wikipedia.org/wiki/Category:インターネット標準 "wikilink") [Category:RFC](https://ja.wikipedia.org/wiki/Category:RFC "wikilink")

1.
2.
3.
4.
5.
6.
7.
8.   (Standard) File Transfer Protocol (FTP). Postel, J. & Reynolds, J. (October 1985).
9.   (Proposed Standard) Extensions for IPv6, NAT, and Extended Passive Mode. Allman, M. & Metz, C. & Ostermann, S. (September 1998).
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
28.
29.
30.
31.  Written for IE versions 6 and earlier. Might work with newer versions.
32.
33.
34.
35.
36.
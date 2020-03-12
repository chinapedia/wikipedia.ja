> この記事は[FTPS](https://ja.wikipedia.org/wiki/FTPS)から翻訳されています。


**FTPS** (File Transfer Protocol over SSL/TLS) は、[FTPで送受信するデータを](../Page/File_Transfer_Protocol.md "wikilink")[TLSまたはSSLで](../Page/Transport_Layer_Security.md "wikilink")[暗号化](https://ja.wikipedia.org/wiki/暗号化 "wikilink")する[通信プロトコル](../Page/通信プロトコル.md "wikilink")。[IETFにより](../Page/Internet_Engineering_Task_Force.md "wikilink")、RFC 2228 や RFC 4217 で標準化されている。

既定の[Well-known Portは](../Page/ポート_\(コンピュータネットワーク\).md "wikilink")、990/tcp。

SFTP ([SSH File Transfer Protocol](../Page/SSH_File_Transfer_Protocol.md "wikilink")) はSSHの上でFTPとは別個のプロトコルにてファイル転送を実現するコマンドである。そのためSFTPはSSHのポートを使い既定の[Well-known Portは](https://ja.wikipedia.org/wiki/ポート番号 "wikilink")22/tcpであり、FTPSとは全くの別物である。

## 概要

FTPの認証で送信されるユーザ名と[パスワード](../Page/パスワード.md "wikilink")の電文は、暗号化されていない状態（[クリアテキスト](https://ja.wikipedia.org/wiki/クリアテキスト "wikilink")）であるため、第三者に[盗聴](../Page/盗聴.md "wikilink")・侵入される危険性がある。FTPSはその危険性を回避するために制定された。

## 暗号化の種類

FTPSには、[認証コマンド](https://ja.wikipedia.org/wiki/認証コマンド "wikilink")（AUTHコマンド）実行後に暗号化通信を開始する**Explicitモード**と、[FTPSサーバ](https://ja.wikipedia.org/wiki/FTPSサーバ "wikilink")接続開始時点から暗号化通信を開始する**Implicitモード**の2種類が存在する。このExplicitモードは特にFTPESとも呼ばれる。

### Explicit（明示的）モード

いわゆる[STARTTLS](https://ja.wikipedia.org/wiki/STARTTLS "wikilink")に相当する。

サーバの21/tcpポートに接続した後に[クライアントがAUTHコマンドを実行して](../Page/クライアント_\(コンピュータ\).md "wikilink")、使用するプロトコル（SSLまたはTLS）のネゴシエーションをおこない、適合したプロトコルでの[ハンドシェイク](https://ja.wikipedia.org/wiki/ハンドシェイク "wikilink")完了後に暗号化された通信がおこなわれる。 つまりExplicitモードの場合、クライアントがAUTHコマンドを実行しなければ通常のFTPとして機能する。

### Implicit（暗黙的）モード

サーバの990/tcpポートに接続した直後にSSLまたはTLSによるハンドシェイクがおこなわれる。 Implicitモードで動作するサーバに接続する場合、クライアントはサーバが採用している暗号化プロトコルに適合したFTPSクライアントソフトを使用する必要がある。 また、データ転送[チャネル](https://ja.wikipedia.org/wiki/チャネル "wikilink")（PORTまたはPASVコマンドで作成されるチャネル）での通信を暗号化する場合、PROTコマンドを用いて保護レベルをP (Private) に設定する必要がある。

なお、ImplicitモードはRFC 4217がドラフトだった頃に[第7版](https://tools.ietf.org/html/draft-murray-auth-ftp-ssl-07)まで掲載されていたが、[第8版](https://tools.ietf.org/html/draft-murray-auth-ftp-ssl-08)で削除されており、正式なRFCには掲載されていない。

## SFTPと比較したFTPSのメリット、デメリット

SFTPと比較したFTPSのメリットとして、ASCII/BINARY モードのサポートやフォルダ単位での転送がある。

デメリットとしては、サーバー運用側でSSL証明書の購入コストがかかることであるが、これについては[ワイルドカード証明書](https://ja.wikipedia.org/wiki/ワイルドカード証明書 "wikilink")で登録すれば、自社SSLサイト([HTTPS](../Page/HTTPS.md "wikilink"))と共通の証明書を利用可能。

## 利用するアプリケーション

FTPSを利用できるアプリケーションには、以下のものが存在する。アルファベット順に列挙する。

### 対応クライアント

  - [Core FTP](https://ja.wikipedia.org/wiki/Core_FTP "wikilink")
  - [CuteFTP](https://ja.wikipedia.org/wiki/CuteFTP "wikilink")
  - [Cyberduck](https://ja.wikipedia.org/wiki/Cyberduck "wikilink")
  - [FFFTP](../Page/FFFTP.md "wikilink")
  - [FileZilla](https://ja.wikipedia.org/wiki/FileZilla "wikilink")
  - [FireFTP](https://ja.wikipedia.org/wiki/FireFTP "wikilink") （[Firefox](https://ja.wikipedia.org/wiki/Firefox "wikilink")のアドオン）
  - [FlashFXP](https://ja.wikipedia.org/wiki/FlashFXP "wikilink")
  - [FTP Voyager](https://ja.wikipedia.org/wiki/FTP_Voyager "wikilink")
  - [gFTP](https://ja.wikipedia.org/wiki/gFTP "wikilink")
  - [lftp](https://ja.wikipedia.org/wiki/lftp "wikilink")
  - [NextFTP](https://ja.wikipedia.org/wiki/NextFTP "wikilink")
  - [Secure FTP](https://ja.wikipedia.org/wiki/Secure_FTP "wikilink")
  - [SmartFTP](../Page/SmartFTP.md "wikilink")
  - [Ultimate FTP](https://ja.wikipedia.org/wiki/Ultimate_FTP "wikilink")
  - [WinSCP](../Page/WinSCP.md "wikilink")

### 対応サーバー

  - [Apache FtpServer](https://ja.wikipedia.org/wiki/Apache_FtpServer "wikilink")
  - [Bftpd](https://ja.wikipedia.org/wiki/Bftpd "wikilink")
  - [Cerberus FTP Server](https://ja.wikipedia.org/wiki/Cerberus_FTP_Server "wikilink")
  - [CrossFTP Server](https://ja.wikipedia.org/wiki/CrossFTP_Server "wikilink")
  - [DrFTPD](https://ja.wikipedia.org/wiki/DrFTPD "wikilink")
  - [edtFTPD](https://ja.wikipedia.org/wiki/edtFTPD "wikilink")
  - [FileZilla Server](https://ja.wikipedia.org/wiki/FileZilla_Server "wikilink")
  - [Independent FTP Daemon](https://ja.wikipedia.org/wiki/Independent_FTP_Daemon "wikilink")
  - [ProFTPD](../Page/ProFTPD.md "wikilink")
  - [Pure-FTPd](https://ja.wikipedia.org/wiki/Pure-FTPd "wikilink")
  - [vsftpd](https://ja.wikipedia.org/wiki/vsftpd "wikilink")
  - [War FTP Daemon](https://ja.wikipedia.org/wiki/War_FTP_Daemon "wikilink")
  - [Internet Information Services](../Page/Internet_Information_Services.md "wikilink") （IIS7以降）

## 外部リンク

  - [FileZilla](http://sourceforge.net/projects/filezilla/)
  - [WinSCP](http://winscp.net/jp/)
  - [FFFTP](http://sourceforge.jp/projects/ffftp/)
  - [Cyberduck](http://cyberduck.ch/)
  - [SmartFTP](http://www.smartftp.com/?lang=ja-jp)
  - [NextFTP](http://www.toxsoft.com/nextftp/)
  - [FlashFXP](http://www.flashfxp.com/)
  - [Advanced Technology Partner, Inc.](http://www.atp-inc.net/)

[Category:File_Transfer_Protocol](https://ja.wikipedia.org/wiki/Category:File_Transfer_Protocol "wikilink") [Category:Transport_Layer_Security](https://ja.wikipedia.org/wiki/Category:Transport_Layer_Security "wikilink") [Category:インターネット標準](https://ja.wikipedia.org/wiki/Category:インターネット標準 "wikilink") [Category:RFC](https://ja.wikipedia.org/wiki/Category:RFC "wikilink")
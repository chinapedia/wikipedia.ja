> この記事は[FTP](https://ja.wikipedia.org/wiki/FTP)から翻訳されています。


**FTPサーバ**とは、[FTPを使用してファイルの送受信を行う](../Page/File_Transfer_Protocol.md "wikilink")[サーバ](../Page/サーバ.md "wikilink")のことである。

ファイルの[アップロード](../Page/アップロード.md "wikilink")・[ダウンロード](https://ja.wikipedia.org/wiki/ダウンロード "wikilink")には[FTPクライアント](../Page/FTPクライアント.md "wikilink")ソフトウェアが必要だが、最近の[ウェブブラウザ](../Page/ウェブブラウザ.md "wikilink")にはこれが組み込まれている場合が多い。

大量のファイルを転送する際に利用されることが多いが、規格が古いためあまり転送スピードがでないことがある。その場合は分割するとスピードがあがる。[ウェブサイト](../Page/ウェブサイト.md "wikilink")用のファイルを[Webサーバ](../Page/Webサーバ.md "wikilink")に置くために、Webサーバと一台で連動させている場合も少なくない。

[フリーウェア](../Page/フリーウェア.md "wikilink")や[シェアウェア](../Page/シェアウェア.md "wikilink")などの[コンピュータプログラムを大勢の人に提供するためにもFTPサーバは利用される](../Page/プログラム_\(コンピュータ\).md "wikilink")。本来はFTPサーバはユーザーアカウントと[パスワード](../Page/パスワード.md "wikilink")による認証が必要だが、このような目的で提供されるサーバは匿名で転送 (たいていダウンロードだけに限定) できる。この際、伝統的にユーザーアカウントには**Anonymous**（英語で[匿名](../Page/匿名.md "wikilink")の意味）や**ftp**、パスワードには自分の[電子メール](../Page/電子メール.md "wikilink")アドレスを入力することが多い。

FTPによる通信は暗号化されていないため、暗号化していない機密情報をそのまま送受信することになると、危険である。[SSHに対応しているサーバの多くは](../Page/Secure_Shell.md "wikilink")、[SSH File Transfer Protocol](https://ja.wikipedia.org/wiki/SSH_File_Transfer_Protocol "wikilink") (SFTP) で暗号化した方式で安全にファイル転送することができる。[SSL/TLSのうえでFTPのやりとりをする](../Page/Transport_Layer_Security.md "wikilink")[FTPS](../Page/FTPS.md "wikilink")といった方式をサポートしているサーバもある。しかし、従来の習慣から、旧来のFTPを利用しているユーザーは多い。

## FTPサーバソフトウェア一覧

### 商用

  - [Axway SecureTransport](https://ja.wikipedia.org/wiki/Axway_SecureTransport "wikilink")
  - [Cerberus FTP Server](https://ja.wikipedia.org/wiki/Cerberus_FTP_Server "wikilink") (Windows)
  - [CrushFTP Server](https://ja.wikipedia.org/wiki/CrushFTP_Server "wikilink")
  - [DataExpress Open Platform](https://ja.wikipedia.org/wiki/DataExpress_Open_Platform "wikilink") (DXOP)
  - [File COPA](https://ja.wikipedia.org/wiki/File_COPA "wikilink") (Windows)
  - [Microsoft Internet Information Services](../Page/Internet_Information_Services.md "wikilink")（Windows）
  - [RaidenFTPD](https://ja.wikipedia.org/wiki/RaidenFTPD "wikilink") Windows, SSL, UTF8, UPnP, Mode-Z
  - [Rumpus](https://ja.wikipedia.org/wiki/Rumpus "wikilink") (MacOS)
  - [SecurFTP](https://ja.wikipedia.org/wiki/SecurFTP "wikilink")
  - [Serv-U File Transfer Server](https://ja.wikipedia.org/wiki/Serv-U_File_Transfer_Server "wikilink") (Windows)
  - [Sterling Commerce Managed File Transfer](https://ja.wikipedia.org/wiki/Sterling_Commerce_Managed_File_Transfer "wikilink")
  - [Sysax Multi Server](https://ja.wikipedia.org/wiki/Sysax_Multi_Server "wikilink") (Windows)
  - [WS_FTP Server](https://ja.wikipedia.org/wiki/WS_FTP_Server "wikilink")

### 非商用

  - [Bftpd](https://ja.wikipedia.org/wiki/Bftpd "wikilink") (GNU GPL)
  - [BSDftpd-ssl](https://ja.wikipedia.org/wiki/BSDftpd-ssl "wikilink") (BSD Revised)
  - [ColoradoFTP](https://ja.wikipedia.org/wiki/ColoradoFTP "wikilink") (GNU GPL)
  - [DrFTPD](https://ja.wikipedia.org/wiki/DrFTPD "wikilink") (Apache, GNU GPLv2)
  - [FileZilla Server](https://ja.wikipedia.org/wiki/FileZilla_Server "wikilink") オープンソース（Windows）
  - [iFTPd](https://ja.wikipedia.org/wiki/iFTPd "wikilink") (GNU GPL)
  - [Mina](https://ja.wikipedia.org/wiki/Apache_Mina "wikilink") (Apache)
  - [MuddleFTPD](https://ja.wikipedia.org/wiki/MuddleFTPD "wikilink") (GNU GPLv2)
  - [ProFTPD](../Page/ProFTPD.md "wikilink") オープンソース（Linux、BSD、Mac OS Xなど）
  - [publicfile](https://ja.wikipedia.org/wiki/publicfile "wikilink") オープンソース（Linux、BSDなど）
  - [Pure-FTPd](https://ja.wikipedia.org/wiki/Pure-FTPd "wikilink") オープンソース（Linux、BSD、Mac OS Xなど）
  - [vsftpd](https://ja.wikipedia.org/wiki/vsftpd "wikilink") オープンソース（Linux、BSDなど）
  - [War FTP Daemon](https://ja.wikipedia.org/wiki/War_FTP_Daemon "wikilink") フリーソフトウェア（Windows）
  - [WU-FTPD](https://ja.wikipedia.org/wiki/WU-FTPD "wikilink") オープンソース（Linux、BSDなど）

### デュアル・ライセンス

  - [NcFTPd Server](https://ja.wikipedia.org/wiki/NcFTPd_Server "wikilink")
  - [zFTPServer](https://ja.wikipedia.org/wiki/zFTPServer "wikilink") （Windows）

[Category:FTPサーバ](https://ja.wikipedia.org/wiki/Category:FTPサーバ "wikilink")
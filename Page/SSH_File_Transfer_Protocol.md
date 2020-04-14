> この記事は[SSH File Transfer Protocol](https://ja.wikipedia.org/wiki/SSH_File_Transfer_Protocol)から翻訳されています。


**SSH File Transfer Protocol**(SFTP)は、信頼性の高い上での[ファイル転送](https://ja.wikipedia.org/wiki/ファイル転送 "wikilink")や[ファイル管理を提供する](https://ja.wikipedia.org/wiki/ファイルマネージャ "wikilink")[通信プロトコル](../Page/通信プロトコル.md "wikilink")である。[Internet Engineering Task Force](../Page/Internet_Engineering_Task_Force.md "wikilink")(IETF)によって、安全なファイル転送機能を提供するために[Secure Shellバージョン](../Page/Secure_Shell.md "wikilink")2.0(SSH-2)の拡張として設計された。IETFの[インターネットドラフト](https://ja.wikipedia.org/wiki/インターネットドラフト "wikilink")では、このプロトコルはSSH-2に関連付けて説明されているが、TLS([Transport Layer Security](../Page/Transport_Layer_Security.md "wikilink"))経由の安全なファイル転送や、[VPNアプリケーションの管理情報の転送など](../Page/Virtual_Private_Network.md "wikilink")、さまざまなアプリケーションで使用できると述べられている。

このプロトコルは、SSHなどので実行されること、サーバが既にクライアントを認証していること、クライアントユーザのIDがプロトコルで利用可能であることを前提としている。

## 概要

[Secure copy](../Page/Secure_copy.md "wikilink")(SCP)がファイル転送のみが可能であるのに対して、SFTPでは、リモート[ファイルシステム](../Page/ファイルシステム.md "wikilink")プロトコルのようにリモートファイルに対する一連の操作が可能である。SFTPクライアントの追加機能には、中断された転送の再開、ディレクトリリスト、、リモートファイルの削除がある\[1\]。

SFTPはSCPと比べてできるだけプラットフォームに依存しないように設計されている。例えば、SCPではクライアントが指定した[ワイルドカードの拡張はサーバの実装次第であるが](../Page/ワイルドカード_\(情報処理\).md "wikilink")、SFTPの設計ではこの問題を回避できる。SCPサーバの実装はUNIXプラットフォームで行われることが多いが、SFTPサーバはほとんどのプラットフォームで利用可能である。SFTPと比較して、SCPでのファイル転送は高速である。SFTPでは、他のメカニズムのようにセッションを終了することなく、ファイル転送のみを簡単に終了できる。

SFTPは、[SSH上で実行される](../Page/Secure_Shell.md "wikilink")[FTPではなく](../Page/File_Transfer_Protocol.md "wikilink")、IETF SECSHワーキンググループによってゼロから設計された新しいプロトコルである。同じ略称の[Simple File Transfer Protocolと混同される場合がある](https://ja.wikipedia.org/wiki/Simple_File_Transfer_Protocol "wikilink")\[2\]。

SFTPのプロトコル自体は認証とセキュリティを提供せず、基礎となるプロトコルがこれを保護することを期待している。SFTPは、同じワーキンググループによって設計されたSSHバージョン2(SSH-2)実装のサブシステムとして最もよく使用される。ただし、SSH-1や他のデータストリームでも実行できる。SSH-1はサブシステムの概念に対応していないため、SFTPサーバをSSH-1上で実行させることはプラットフォームに依存する。SSH-1サーバに接続しようとするSFTPクライアントは、サーバ側のSFTPサーババイナリへのパスを知る必要がある。

アップロードされたファイルは、ローカル側のタイムスタンプなどの基本的な属性を引き継ぐ場合がある。これは、一般的なFTPプロトコルよりも優れている点である。

## 開発の歴史

IETFのワーキンググループ"Secsh"は、過去に[Secure Shellバージョン](../Page/Secure_Shell.md "wikilink")2(RFC 4251)の開発を担当しており、同グループは安全なファイル転送機能の標準の拡張案を作成しようとした。[インターネットドラフト](https://ja.wikipedia.org/wiki/インターネットドラフト "wikilink")が作成され、以降、逐次新しいバージョンに改訂されていった\[3\]。ソフトウェア業界は、ドラフトが標準化される前の様々なバージョンで実装を開始した。開発作業が進むにつれて、Secshファイル転送プロジェクトの範囲が拡大し、ファイルアクセスとファイル管理が含まれるようになった。

最終的には、一部の委員会メンバーがSFTPを単なるファイルアクセスプロトコルあるいはファイル転送プロトコルではなく「ファイルシステムプロトコル」であると見なし、ワーキンググループの範囲を超えてSFTPの開発に当たるようになり、開発が停滞した\[4\]。7年間の休止の後の2013年、バージョン3ドラフトをベースラインとして、SFTPの開発作業を再開しようとした。

### バージョン0{{～}}2

IETFが関与する前は、SFTPはの独自プロトコルで、1997年にSami Lehtinenの支援を受けてTatu Ylönenによって設計された.\[5\]。バージョン0{{～}}2とバージョン3との違いは、[section 10 of draft-ietf-secsh-filexfer-02のsection 10](http://tools.ietf.org/html/draft-ietf-secsh-filexfer-02#section-10)に列挙されている。

### バージョン3

IETF Secure Shell File Transferプロジェクトの立ち上げ時に、Secshワーキンググループは、SFTPの目的は、信頼できるデータストリーム上で安全なファイル転送機能を提供し、SSH-2プロトコルで使用する標準のファイル転送プロトコルにすることであると表明している。

インターネットドラフトのDraft 00 - 02では、プロトコルのバージョン3が定義されている。

  - [SSH File Transfer Protocol, Draft 00, January 2001](http://tools.ietf.org/html/draft-ietf-secsh-filexfer-00)
  - [SSH File Transfer Protocol, Draft 01, March 2001](http://tools.ietf.org/html/draft-ietf-secsh-filexfer-01)
  - [SSH File Transfer Protocol, Draft 02, October 2001](http://tools.ietf.org/html/draft-ietf-secsh-filexfer-02)

### バージョン4

インターネットドラフトのDraft 03 - 04では、プロトコルのバージョン4が定義されている。

  - [SSH File Transfer Protocol, Draft 03, October 2002](http://tools.ietf.org/html/draft-ietf-secsh-filexfer-03)
  - [SSH File Transfer Protocol, Draft 04, December 2002](http://tools.ietf.org/html/draft-ietf-secsh-filexfer-04)

### バージョン5

インターネットドラフトのDraft 05では、プロトコルのバージョン5が定義されている。

  - [SSH File Transfer Protocol, Draft 05, January 2004](http://tools.ietf.org/html/draft-ietf-secsh-filexfer-05)

### バージョン6

インターネットドラフトのDraft 06 - 13では、プロトコルのバージョン6が定義されている。

  - [SSH File Transfer Protocol, Draft 06, October 2004](http://tools.ietf.org/html/draft-ietf-secsh-filexfer-06)
  - [SSH File Transfer Protocol, Draft 07, March 2005](http://tools.ietf.org/html/draft-ietf-secsh-filexfer-07)
  - [SSH File Transfer Protocol, Draft 08, April 2005](http://tools.ietf.org/html/draft-ietf-secsh-filexfer-08)
  - [SSH File Transfer Protocol, Draft 09, June 2005](http://tools.ietf.org/html/draft-ietf-secsh-filexfer-09)
  - [SSH File Transfer Protocol, Draft 10, June 2005](http://tools.ietf.org/html/draft-ietf-secsh-filexfer-10)
  - [SSH File Transfer Protocol, Draft 11, January 2006](http://tools.ietf.org/html/draft-ietf-secsh-filexfer-11)
  - [SSH File Transfer Protocol, Draft 12, January 2006](http://tools.ietf.org/html/draft-ietf-secsh-filexfer-12)
  - [SSH File Transfer Protocol, Draft 13, July 2006](http://tools.ietf.org/html/draft-ietf-secsh-filexfer-13)

## ソフトウェア

### SFTPクライアント

**SFTP** (sftp)という言葉は、このプロトコルのクライアント部分を実装するコマンドラインプログラムを指すこともある。例えば、[OpenSSH](../Page/OpenSSH.md "wikilink")にはsftpコマンドがサブシステムとして含まれる\[6\]。

[`scp`](../Page/Secure_copy.md "wikilink")クライアントの一部の実装は、サーバが対応するものに応じて、ファイル転送を実行するためにSFTPプロトコルとSCPプロトコルの両方に対応する。

このSFTPを利用できるアプリケーションには、コマンドライン形式のsftpコマンドだけでなく、以下のものが存在する。

  - [WinSCP](../Page/WinSCP.md "wikilink")
  - [FileZilla](https://ja.wikipedia.org/wiki/FileZilla "wikilink")
  - [EmFTP](https://ja.wikipedia.org/wiki/EmFTP "wikilink")
  - [Cyberduck](https://ja.wikipedia.org/wiki/Cyberduck "wikilink")
  - [Transmit](https://ja.wikipedia.org/wiki/Transmit "wikilink")

### SFTPサーバ

FTPサーバの一部にはSFTPプロトコルを実装しているものもあるが、SFTPプロトコルへの対応は通常、SSHサーバの実装によって提供される。これは、SFTPプロトコルがデフォルトの[ポート](../Page/ポート_\(コンピュータネットワーク\).md "wikilink")22を他のSSHサービスと共有するためである。

## 関連項目

  -
  -
  - [Files transferred over shell protocol](../Page/Files_transferred_over_shell_protocol.md "wikilink")(FISH)

  - [FTPS](../Page/FTPS.md "wikilink")

  - [:Category:FTPクライアント](https://ja.wikipedia.org/wiki/Category:FTPクライアント "wikilink")

## 脚注

## 外部リンク

  - [Chrooted SFTP with Public Key Authentication](https://archive.is/20130103130850/http://www.ipsure.com/blog/2010/chrooted-sftp-with-public-key-authentication) – Integrating SFTP into FreeBSD production servers using the public key cryptography approach
  - [User-based chrooted SFTP in GNU/Linux](http://wiki.gilug.org/index.php/How_to_mount_SFTP_accesses)
  - [OpenSSH](http://www.openssh.com/)
  - [WinSCP](http://winscp.net/)
  - [filezilla](http://sourceforge.net/projects/filezilla/)
  - [EmFTP](http://www.emftp.com/jp/)

[Category:暗号化プロトコル](https://ja.wikipedia.org/wiki/Category:暗号化プロトコル "wikilink") [Category:ファイル転送プロトコル](https://ja.wikipedia.org/wiki/Category:ファイル転送プロトコル "wikilink") [Category:Secure_Shell](https://ja.wikipedia.org/wiki/Category:Secure_Shell "wikilink")

1.
2.
3.
4.
5.  <ftp://ftp.ietf.org/ietf-mail-archive/secsh/2012-09.mail>
6.
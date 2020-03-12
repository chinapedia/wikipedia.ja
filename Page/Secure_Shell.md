> この記事は[Secure Shell](https://ja.wikipedia.org/wiki/Secure_Shell)から翻訳されています。


**Secure Shell**（セキュアシェル、**SSH**）は、[暗号](../Page/暗号.md "wikilink")や[認証](../Page/認証.md "wikilink")の技術を利用して、安全にリモートコンピュータと[通信](../Page/通信.md "wikilink")するための[プロトコル](../Page/プロトコル.md "wikilink")。[パスワード](../Page/パスワード.md "wikilink")などの認証部分を含むすべての[ネットワーク上の通信が暗号化される](../Page/コンピュータネットワーク.md "wikilink")。

## 概要

Secure Shell は、そもそも[Telnet](../Page/Telnet.md "wikilink")や[rsh](https://ja.wikipedia.org/wiki/rsh "wikilink")、[rlogin](https://ja.wikipedia.org/wiki/rlogin "wikilink")などといった、リモートホストの[シェル](../Page/シェル.md "wikilink")を利用するための既存のプロトコルを代用する手段として考えられていた。Telnetや[FTPは](../Page/File_Transfer_Protocol.md "wikilink")、ネットワーク上に[平文](../Page/平文.md "wikilink")でパスワードを送信してしまうため、パスワードをネットワーク経路上でのぞき見されてしまう（これを[盗聴](../Page/盗聴.md "wikilink")と呼ぶ）危険性が高く、商業的なインターネット空間では問題が大きかった。Telnet同様に、リモートホスト間でのファイルコピー用のコマンド[rcp](https://ja.wikipedia.org/wiki/rcp "wikilink")を代用する[scpや](../Page/Secure_copy.md "wikilink")、FTPを代用するための[sftpも用意されている](../Page/SSH_File_Transfer_Protocol.md "wikilink")。

SSHの暗号通信は、鍵交換アルゴリズム（[ディフィー・ヘルマン鍵共有](../Page/ディフィー・ヘルマン鍵共有.md "wikilink")など）を用いて共通鍵暗号で使用するセッション鍵を生成し、[共通鍵暗号](../Page/共通鍵暗号.md "wikilink")（[トリプルDES](../Page/トリプルDES.md "wikilink")、[AESなど](../Page/Advanced_Encryption_Standard.md "wikilink")）を用いて通信を暗号化し、[公開鍵暗号](../Page/公開鍵暗号.md "wikilink")（[RSAや](../Page/RSA暗号.md "wikilink")[DSA](https://ja.wikipedia.org/wiki/Digital_Signature_Algorithm "wikilink")）を用いてホスト認証やユーザ認証を行なう、いわゆる[ハイブリッド暗号](https://ja.wikipedia.org/wiki/ハイブリッド暗号 "wikilink")である。また、なりすましを防止するための認証の仕組みも充実している。認証方式も[公開鍵](../Page/公開鍵暗号.md "wikilink")[認証](../Page/認証.md "wikilink")の他にも、[パスワード](../Page/パスワード.md "wikilink")[認証](../Page/認証.md "wikilink")、[ワンタイムパスワード](https://ja.wikipedia.org/wiki/ワンタイムパスワード "wikilink")などが提供されており、個々の[情報セキュリティポリシー](../Page/情報セキュリティポリシー.md "wikilink")に合わせて選択できる。

現在は、バージョン1とバージョン2の2種類のプロトコルが共存している。脆弱性が発見されているため、バージョン1の利用は推奨されない。商用アプリケーションや[フリーソフトウェア](../Page/フリーソフトウェア.md "wikilink")など幾つかの実装があり、特許や互換性の問題などでやや混乱があったが、[2006年](../Page/2006年.md "wikilink")にSSHのプロトコルおよびその関連技術が[RFCとして制定された](../Page/Request_for_Comments.md "wikilink")\[1\]。ただ、2008年の時点でもっとも一般に普及しているのは、[オープンソース](../Page/オープンソース.md "wikilink")で開発されている[OpenSSH](../Page/OpenSSH.md "wikilink")で\[2\]、[Linux](../Page/Linux.md "wikilink")などでも標準的に利用されているため、現在では単にSSHと言った場合、OpenSSHの実装系を指すことが多い。

## SSHサーバ

  - [OpenSSH](../Page/OpenSSH.md "wikilink") (マルチプラットフォーム)
  - SSH Tectia Server (マルチプラットフォーム)
  - [Reflection for Secure IT (マルチプラットフォーム)](http://www.attachmate.jp/Products/Security/security.htm)

## SSHクライアント

  - [OpenSSH](../Page/OpenSSH.md "wikilink") (マルチプラットフォーム)
  - [PuTTY](../Page/PuTTY.md "wikilink") (Windows, UNIX)
  - [Xshell](https://www.netsarang.com) (Windows)
  - [Tera Term](../Page/Tera_Term.md "wikilink") (Windows)
  - [Poderosa](../Page/Poderosa.md "wikilink") (Windows)
  - [RLogin](https://ja.wikipedia.org/wiki/RLogin "wikilink") (Windows)
  - SSH Tectia Client (マルチプラットフォーム)
  - [Reflection for Secure IT (マルチプラットフォーム)](http://www.attachmate.jp/Products/Security/security.htm)
  - [WebSSH](http://webssh.uni.me)

## SSHのセキュリティリスク

SSHクライアントの利用者がサーバ鍵の指紋を確認しない場合、意図しないリモートコンピュータに接続していても気づかず、通信内容を盗聴される恐れがある。

また、SSHサーバによっては、設定次第では[ブルートフォースアタックによって](../Page/総当たり攻撃.md "wikilink")[シェル](../Page/シェル.md "wikilink")へのアクセスを許してしまう場合がある。例えば、[IPAが発表している不正アクセスの届け出状況では](../Page/情報処理推進機構.md "wikilink")、SSHポート経由でパスワードクラッキングが行われた例が繰り返して発表されている\[3\]\[4\]。これらの事例を元に、「パスワード管理の徹底」「セキュリティパッチの適用」「アクセスログの監視による、攻撃の迅速な発見」のような対策に加えて、SSHサーバ運用時にはログインに公開鍵認証を採用することをIPAは推奨している 。

## 脚注

<references/>

## 関連項目

  - [TLS](../Page/Transport_Layer_Security.md "wikilink")
  - [Telnet](../Page/Telnet.md "wikilink")
  - [File Transfer Protocol](../Page/File_Transfer_Protocol.md "wikilink")
  - [SSH File Transfer Protocol](../Page/SSH_File_Transfer_Protocol.md "wikilink")
  - [Secure copy](../Page/Secure_copy.md "wikilink")
  - [sshfs](https://ja.wikipedia.org/wiki/sshfs "wikilink")（[FUSEの応用](../Page/Filesystem_in_Userspace.md "wikilink")）
  - [FISH](../Page/Files_transferred_over_shell_protocol.md "wikilink")
  - [ポートフォワーディング](https://ja.wikipedia.org/wiki/ポートフォワーディング "wikilink")

[Category:Secure_Shell](https://ja.wikipedia.org/wiki/Category:Secure_Shell "wikilink") [Category:アプリケーション層プロトコル](https://ja.wikipedia.org/wiki/Category:アプリケーション層プロトコル "wikilink") [Category:暗号ソフトウェア](https://ja.wikipedia.org/wiki/Category:暗号ソフトウェア "wikilink") [Category:RFC](https://ja.wikipedia.org/wiki/Category:RFC "wikilink")

1.  RFC 4250、RFC 4251、RFC 4252、RFC 4253、RFC 4254、RFC 4255、RFC 4256 を参照。
2.
3.
4.
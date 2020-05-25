> この記事は[OpenVPN](https://ja.wikipedia.org/wiki/OpenVPN)から翻訳されています。


**OpenVPN**は、[サーバ](../Page/サーバ.md "wikilink")間に[暗号](../Page/暗号.md "wikilink")化されたトンネルを作成するための[オープンソース](../Page/オープンソース.md "wikilink")の[Virtual Private Network](../Page/Virtual_Private_Network.md "wikilink")（VPN）ソフトウェアである。James Yonanが開発し、[GNU General Public Licenseでリリースされている](../Page/GNU_General_Public_License.md "wikilink")。

## 概要

OpenVPNは、事前に共有しておいた秘密鍵、[公開鍵証明書](../Page/公開鍵証明書.md "wikilink")、[ユーザ名](../Page/ハンドルネーム.md "wikilink")/[パスワード](../Page/パスワード.md "wikilink")を使って[Peer to Peerの相互の](../Page/Peer_to_Peer.md "wikilink")[認証](../Page/認証.md "wikilink")を行う。[OpenSSL](https://ja.wikipedia.org/wiki/OpenSSL "wikilink")や[SSLv3/TLSv1](../Page/Transport_Layer_Security.md "wikilink")[プロトコルを利用する](../Page/通信プロトコル.md "wikilink")。[Solaris](../Page/Solaris.md "wikilink")、[Linux](../Page/Linux.md "wikilink")、[OpenBSD](../Page/OpenBSD.md "wikilink")、[FreeBSD](../Page/FreeBSD.md "wikilink")、[NetBSD](../Page/NetBSD.md "wikilink")、[macOS](https://ja.wikipedia.org/wiki/macOS "wikilink")、[Windows](https://ja.wikipedia.org/wiki/Windows "wikilink")などで動作する。様々なセキュリティ機能や制御機能を持つ。 他のVPNシステムとの接続には対応しない。[クライアント側も](../Page/クライアント_\(コンピュータ\).md "wikilink")[サーバ](../Page/サーバ.md "wikilink")側も1個の[バイナリ](../Page/バイナリ.md "wikilink")とオプションの[設定ファイル](../Page/設定ファイル.md "wikilink")から構成され、使用する認証方式によって、いくつかの鍵ファイルが必要となる。

## 暗号

OpenVPNは[OpenSSL](https://ja.wikipedia.org/wiki/OpenSSL "wikilink")ライブラリを使って、データチャンネルと制御チャンネルの両方の[暗号](../Page/暗号.md "wikilink")化を行う。暗号化と認証処理はOpenSSLに任されており、OpenSSLパッケージに含まれる任意の暗号方式を使うことができる。[HMAC](../Page/HMAC.md "wikilink")パケット認証機能を付加的に使用して、コネクション時のセキュリティを強化することもできる（開発者はこれをHMAC Firewallと称している）。さらに、暗号化をハードウェアによって行い、性能を強化することもできる。

## 認証

相互の[認証](../Page/認証.md "wikilink")は、いくつかの方法がある。OpenVPNが推奨している方法は、事前共有した秘密鍵、公開鍵証明書、ユーザ名/パスワードを使った認証である。事前共有した秘密鍵が最も簡単であり、公開鍵証明書が最も頑健で機能が豊富である。ユーザ名/パスワードを使った方法は新しい機能（バージョン 2.0）であり、クライアント側の認証を不要とすることもできる（サーバ側は必須）。ソースの[tarballには](../Page/Tar.md "wikilink")、[Perl](../Page/Perl.md "wikilink")スクリプトによるユーザ名/パスワード検証（[PAM](https://ja.wikipedia.org/wiki/PAM "wikilink")）と[C言語](../Page/C言語.md "wikilink")によるPAMの例が含まれている。

## ネットワーク

OpenVPNは全ての通信を1つのIPポートに多重化する。[UDP](../Page/User_Datagram_Protocol.md "wikilink")（デフォルト、推奨）でも[TCPでも利用可能である](../Page/Transmission_Control_Protocol.md "wikilink")。ほとんどの[プロキシ](../Page/プロキシ.md "wikilink")サーバを経由しても大丈夫で、[ネットワークアドレス変換](../Page/ネットワークアドレス変換.md "wikilink")経由でもファイアウォール経由でも通信可能である。サーバ側からクライアント側に特定のネットワーク設定を送信することもできる（IPアドレス、ルーティングコマンド、その他コネクションオプション）。OpenVPNは、[TUN/TAP](https://ja.wikipedia.org/wiki/TUN/TAP "wikilink")ドライバ経由のネットワーキング方法を2種類提供する。ネットワーク層でのIPトンネルまたはデータリンク層でのイーサネットTAPのどちらかを使うことができ、後者では任意の種類のイーサネットのトラフィックをやりとりできる。また、オプションで[LZO](https://ja.wikipedia.org/wiki/Lempel-Ziv-Oberhumer "wikilink")[データ圧縮](../Page/データ圧縮.md "wikilink")ライブラリで転送データを圧縮することもできる。[IANAは](../Page/Internet_Assigned_Numbers_Authority.md "wikilink")、ポート 1194を公式にOpenVPNに割り当てている。新しいバージョンではデフォルトでそのポートを使用するようになっている。バージョン 2.0では、1つのプロセスで複数のトンネルを同時に管理できる。従来は、トンネルごとにプロセスが必要だった。

## セキュリティ

OpenVPNはいくつかのセキュリティ機能も内蔵している。完全にユーザ空間で動作するため、[カーネル](../Page/カーネル.md "wikilink")でのIPスタック操作が不要である。OpenVPNは、root特権の禁止機能、[mlockall](http://www.opengroup.org/onlinepubs/009695399/functions/mlockall.html)による重要データのスワップアウト禁止機能、初期化後に[chroot](https://ja.wikipedia.org/wiki/chroot "wikilink")によってルートとされたディレクトリ以外にアクセスできなくする機能などがある。

OpenVPNは、[PKCS](../Page/PKCS.md "wikilink")ベースの暗号トークンによる[ICカード](../Page/ICカード.md "wikilink")サポートも行う。

## 脚注

<references/>

## 関連項目

  - [OpenSSH](../Page/OpenSSH.md "wikilink") - ネットワーク層/データリンク層のトンネルベースのVPNを実装している。
  - [stunnel](https://ja.wikipedia.org/wiki/stunnel "wikilink") - SSL上の任意のTCPコネクションの暗号化を行う。
  - [UDPホールパンチング](../Page/UDPホールパンチング.md "wikilink") - ファイアウォールやNATを経由してUDP「コネクション」を確立する技法

## 外部リンク

  - [OpenVPN project 公式サイト](http://openvpn.net/)

[Category:セキュリティソフト](https://ja.wikipedia.org/wiki/Category:セキュリティソフト "wikilink") [Category:オープンソースソフトウェア](https://ja.wikipedia.org/wiki/Category:オープンソースソフトウェア "wikilink") [Category:UNIXのソフトウェア](https://ja.wikipedia.org/wiki/Category:UNIXのソフトウェア "wikilink") [Category:コンピュータ・ネットワーク・セキュリティ](https://ja.wikipedia.org/wiki/Category:コンピュータ・ネットワーク・セキュリティ "wikilink") [Category:VPN](https://ja.wikipedia.org/wiki/Category:VPN "wikilink") [Category:トンネリング](https://ja.wikipedia.org/wiki/Category:トンネリング "wikilink")
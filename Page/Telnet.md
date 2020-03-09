> この記事は[Telnet](https://ja.wikipedia.org/wiki/Telnet)から翻訳されています。


**Telnet**（**テルネット Teletype network**）とは、[IPネットワークにおいて](../Page/Internet_Protocol.md "wikilink")、遠隔地にある[サーバ](../Page/サーバ.md "wikilink")や[ルーター](https://ja.wikipedia.org/wiki/ルーター "wikilink")等を[端末](../Page/端末.md "wikilink")から操作する[通信プロトコル](https://ja.wikipedia.org/wiki/通信プロトコル "wikilink")、またはそのプロトコルを利用するソフトウェアである。RFC 854で規定されている。

## 概要

Telnetクライアントは、Telnetサーバとの間で[ソケットを開き](https://ja.wikipedia.org/wiki/ソケット_\(BSD\) "wikilink")、単純なテキストベースの通信を行う。基本的には[ポート番号](https://ja.wikipedia.org/wiki/ポート番号 "wikilink")23番を使用する。

## 脆弱性

認証も含めすべての通信を[暗号化](https://ja.wikipedia.org/wiki/暗号化 "wikilink")せずに[平文](https://ja.wikipedia.org/wiki/平文 "wikilink")のまま送信するため、パスワードの窃取は比較的容易である。同様の機能を有する代替プロトコルとしては、情報を暗号化して送信する[SSHが知られている](../Page/Secure_Shell.md "wikilink")。

## その他

[UNIX](../Page/UNIX.md "wikilink")は当初から[ホストを複数のユーザが同時に使用することを前提に開発されており](https://ja.wikipedia.org/wiki/ホスト_\(ネットワーク\) "wikilink")、IPネットワークやTelnetの登場以前から、[シリアルポート](https://ja.wikipedia.org/wiki/シリアルポート "wikilink")等に複数の端末を接続して使用できた。この端末とホストの通信を、IPのネットワーク上で担ったのがTelnetクライアントプログラムと、その通信手順を規定したTelnetプロトコルである。

なお、クライアントによっては[VT100](https://ja.wikipedia.org/wiki/VT100 "wikilink")などの[端末エミュレータ](https://ja.wikipedia.org/wiki/端末エミュレータ "wikilink")として動作し、テキストモードだけでなく画面モードを実現するものもある。さらに、Telnetプロトコルをバイナリモードで使用し、[IBM 3270のデータストリームを転送することでIBM](https://ja.wikipedia.org/wiki/IBM_3270 "wikilink") 3270端末をエミュレートするためのTN3270プロトコルも開発された。

## 代表的なTelnetクライアント

  - [Tera Term](https://ja.wikipedia.org/wiki/Tera_Term "wikilink")

  - [Xshell](https://www.netsarang.com)

  -
  - [PuTTY](https://ja.wikipedia.org/wiki/PuTTY "wikilink")

## TELNETに関連するRFC

  - RFC 215 - NCP、ICP、and TELNET [1971年](https://ja.wikipedia.org/wiki/1971年 "wikilink")8月
  - RFC 736 - TELNET SUPDUP Option [1977年](../Page/1977年.md "wikilink")10月
  - RFC 764 - TELNET PROTOCOL SPECIFICATIONS [1980年](https://ja.wikipedia.org/wiki/1980年 "wikilink")6月
  - RFC 854 - TELNET PROTOCOL Specification [1983年](https://ja.wikipedia.org/wiki/1983年 "wikilink")5月
  - RFC 855 - TELNET OPTION SPECIFICATIONS 1983年5月
  - RFC 884 - TELNET TERMINAL TYPE OPTION 1983年12月
  - RFC 1205 - 5250 Telnet Interface [1991年](https://ja.wikipedia.org/wiki/1991年 "wikilink")2月
  - RFC 1372 - Telnet Remote Flow Control Option [1992年](https://ja.wikipedia.org/wiki/1992年 "wikilink")10月
  - RFC 1408 - Telnet Environment Option [1993年](../Page/1993年.md "wikilink")1月
  - RFC 1412 - Telnet Authentication:SPX 1993年2月
  - RFC 1416 - Telnet Authentication Option 1993年2月
  - RFC 2355 - TN3270 Enhancements 1998年6月
  - RFC 2946 - Telnet Data Encryption Option 2000年9月

[Category:アプリケーション層プロトコル](https://ja.wikipedia.org/wiki/Category:アプリケーション層プロトコル "wikilink") [Category:インターネット標準](https://ja.wikipedia.org/wiki/Category:インターネット標準 "wikilink") [Category:RFC](https://ja.wikipedia.org/wiki/Category:RFC "wikilink") [Category:telnet](https://ja.wikipedia.org/wiki/Category:telnet "wikilink")
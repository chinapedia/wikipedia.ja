> この記事は[Rlogin](https://ja.wikipedia.org/wiki/Rlogin)から翻訳されています。


**rlogin**（アールログイン）は、[UNIX](../Page/UNIX.md "wikilink")で[ネットワーク経由で遠隔の](../Page/コンピュータネットワーク.md "wikilink")[サーバ](../Page/サーバ.md "wikilink")にログインする[ソフトウェア](../Page/ソフトウェア.md "wikilink")・ユーティリティであり、[TCP](../Page/Transmission_Control_Protocol.md "wikilink")[ポート番号](https://ja.wikipedia.org/wiki/ポート番号 "wikilink") 513 を使う。[4.2BSDで最初に実装された](../Page/BSD.md "wikilink")。rlogin はそのソフトウェアで使われているアプリケーション層の[通信プロトコル](../Page/通信プロトコル.md "wikilink")名でもあり、[TCP/IP](https://ja.wikipedia.org/wiki/TCP/IP "wikilink")[プロトコルスタック](../Page/プロトコルスタック.md "wikilink")の一部である。認証されたユーザーは、あたかもそのコンピュータに物理的に存在しているかのように振舞うことができる。RFC 1258 における定義によれば、「rlogin 機能は、遠隔でエコー制御され、ローカルにフロー制御された仮想端末を提供し、出力は適正にフラッシュされる」とある。rlogin は遠隔ホスト上の[デーモン](../Page/デーモン_\(ソフトウェア\).md "wikilink") **rlogind** と通信する。rlogin は [telnet](https://ja.wikipedia.org/wiki/telnet "wikilink") コマンドとよく似ているが、カスタマイズが不可能であり、UNIX 以外のホストに接続できない。

rlogin は企業や大学のネットワーク内で主に使われる。そのような環境では、ネットワーク上の各UNIXマシンのユーザーアカウント情報が（[NISを使って](../Page/ネットワーク・インフォメーション・サービス.md "wikilink")）共有されている。これは、ネットワーク基盤や各マシンが信頼できるからこそ可能なことであり、rlogin プロトコルはそのような信頼の上に成り立っている。遠隔ホストが /etc/hosts.equiv ファイルに登録されていれば、あるいはユーザーが[ホームディレクトリ](../Page/ホームディレクトリ.md "wikilink")に .rhosts ファイルを持っていれば、rlogin はパスワード入力なしでログインできる（ホームディレクトリは [NFS](../Page/Network_File_System.md "wikilink") で共有することが多い）。

rlogin にはいくつか非常に重大なセキュリティ問題がある。

  - パスワードも含めた全ての情報が暗号化されずに転送される（容易に覗き見できる）。
  - .rlogin（または .rhosts）ファイルの使用法を間違いやすい（誰でもパスワードなしでログインできるように設定してしまいやすい）。このため、企業のアドミニストレータは .rlogin ファイルの使用を禁止することが多い。
  - このプロトコルは、発信元がホスト名やポート番号を偽らないことに一部依存している。したがって、悪意あるクライアントがサーバを騙してアクセスを得ることができる。すなわち、rlogin プロトコルには相手のマシンの識別を認証する手段がなく、それが信頼されたマシン上の真の rlogin クライアントであることを保証する手段がない。
  - NFS によるホームディレクトリのマウントは普通に行われるが、それによって偽の .rhosts ファイルを使った攻撃が可能となる。

このような問題があるため、rlogin は（インターネットのような）信頼できないネットワークでは使われない。さらに、UNIXや[Linux](../Page/Linux.md "wikilink")もデフォルトでは rlogin が使えないようにしているものが多く、限定的な利用も減ってきている。かつては rlogin や telnet を使っていたネットワークは、[SSH](../Page/Secure_Shell.md "wikilink") と rlogin 相当の slogin を使うようになっている。

BSDのオリジナルのパッケージには、rlogin と共に [rcp](https://ja.wikipedia.org/wiki/rcp "wikilink")（リモートコピー、ネットワーク経由のファイルコピー機能）と [rsh](../Page/リモートシェル.md "wikilink")（リモートシェル、ログインせずに遠隔マシン上でコマンドを実行する機能）が含まれていた。これらは hosts.equiv と .rhosts によるアクセス制御を共有しており（接続に使われるデーモンは rshd であり、rlogind とは異なる）、同様のセキュリティ問題を抱えている。SSH にはこれらを置換する機能も含まれている（rcp の代替としては scp、rsh と rlogin は SSH 自体が代替する）。

## 外部リンク

  - [rlogin(1): The Untold Story (PDF)](http://www.cert.org/archive/pdf/98tr017.pdf)
  - RFC 1282 - BSD Rlogin
  - [Manpage of RLOGIN](https://linuxjm.osdn.jp/html/netkit/man1/rlogin.1.html) JMプロジェクト
  - [rlogin(1)](https://docs.oracle.com/cd/E19683-01/816-3946/network-2/index.html) man page（SunOS リファレンスマニュアル）
  - [rlogin(1)](https://nixdoc.net/man-pages/HP-UX/man1/rlogin.1.html) man page（HP-UX リファレンス）
  - [RLogin](https://ja.wikipedia.org/wiki/RLogin "wikilink") [ターミナルエミュレータ](https://ja.wikipedia.org/wiki/ターミナルエミュレータ "wikilink")

[Category:インターネットのプロトコル](https://ja.wikipedia.org/wiki/Category:インターネットのプロトコル "wikilink") [Category:インターネット標準](https://ja.wikipedia.org/wiki/Category:インターネット標準 "wikilink") [Category:UNIXのソフトウェア](https://ja.wikipedia.org/wiki/Category:UNIXのソフトウェア "wikilink") [Category:RFC](https://ja.wikipedia.org/wiki/Category:RFC "wikilink")
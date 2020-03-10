> この記事は[Inetd](https://ja.wikipedia.org/wiki/Inetd)から翻訳されています。


**inetd**（アイネットディー）は、多くの[UNIX](../Page/UNIX.md "wikilink")システムで採用された[インターネット](https://ja.wikipedia.org/wiki/インターネット "wikilink")サービスを管理する型[デーモンである](https://ja.wikipedia.org/wiki/デーモン_\(ソフトウェア\) "wikilink")。InternetDaemonの略。[4.3BSDで初めて採用され](../Page/BSD.md "wikilink")\[1\]、通常`/usr/sbin/inetd` にある。 後継のスーパーサーバ型デーモンとしては、[xinetd](https://ja.wikipedia.org/wiki/xinetd "wikilink")がある。

## 経緯

inetd登場以前は、1台のサーバで複数のサービス（FTPサーバ、TELNETサーバ等）を稼働させておくには、それぞれのサービスのデーモン（ftpd、tftpd等）を起動しておき、それぞれのデーモンが、それぞれの待ち受け[ポートを監視する](../Page/ポート_\(コンピュータネットワーク\).md "wikilink") - というスタイルだった。しかし、この方法では、監視するポートの数だけデーモンが起動していることとなるため、実際にそのサービスが利用されていない時には、実質、メモリの無駄遣いということとなる。そこで、待ち受けポートを監視する専用の中継デーモンを用意し、待ち受けポートに要求がきた時には、あらかじめ決められたデーモン（ftpd、tftpd等）を起動させるという動作が用意されるようになった。

  - メリット
    メモリの浪費解消
  - デメリット
    inetdが中継動作することとなるので、動作レスポンスが遅れる。
    そのため、httpd等はinetdを経由させず、常時起動させておくことが多い。　　　　　　

## 機能

inetdは、[FTP](../Page/File_Transfer_Protocol.md "wikilink")、[POP3](../Page/Post_Office_Protocol.md "wikilink")、[telnet](https://ja.wikipedia.org/wiki/telnet "wikilink") といったインターネットサービスが使うポート番号を（指定されて）監視する。監視対象のポートに[TCPパケットあるいは](../Page/Transmission_Control_Protocol.md "wikilink")[UDPパケットが届くと](../Page/User_Datagram_Protocol.md "wikilink")、inetdは対応するサーバプログラムを起動し、コネクションを制御させる。この方式では、必要にならない限りサービスが起動されないため、メモリ利用効率がよい。さらに、個々のサーバデーモンは[ソケットが](../Page/ソケット_\(BSD\).md "wikilink")[標準入出力および標準エラー出力にフックされた状態で起動されるため](https://ja.wikipedia.org/wiki/標準ストリーム "wikilink")、ネットワークに関するコードを必要としない。トラフィックの多い[HTTPやPOP](../Page/Hypertext_Transfer_Protocol.md "wikilink")3などのプロトコルでは、直接トラフィックを受け付ける専用サーバの方が望ましい（頻繁にサーバプロセスを起動する無駄を避けるため）。

## 設定

ポート番号とサービス名の対応付けは`/etc/services`というファイルで行われ、サービス名とサーバ名の対応付けは`/etc/inetd.conf` というファイルで行われる。例えば、23番のポートにTCP要求が来る場合、`/etc/services`には次のように記述される。

`telnet          23/tcp`

`/etc/inetd.conf`には、これに対応して次の行が記述される（以下の内容は[AIX](https://ja.wikipedia.org/wiki/AIX "wikilink") 5.1の動作するマシンから取得）。

`telnet  stream  tcp6    nowait  root    /usr/sbin/telnetd      telnetd -a`

これによると、inetdは`/usr/sbin/telnetd`というプログラムを`telnetd -a`という引数付きで起動する。inetdは標準入出力および標準エラー出力をソケットにフックした状態でサーバプログラムを起動する。

一般にTCPソケットは個別のサーバをコネクション毎に並行して起動することで制御される。UDPソケットは一般に単一のサーバインスタンスがそのポート番号の全パケットを扱う。

echoなどの単純なサービスはinetd自身が扱い、別にサーバを起動することはない。

## inetd サービスの生成

以下のコードは[C言語](../Page/C言語.md "wikilink")で書かれた単純なinetdサービスの一例である。オプションでファイル名を引数として受け取り、それを[ログファイル名とし](https://ja.wikipedia.org/wiki/サーバログ "wikilink")、そのソケット経由で送られてきた文字列を全てそのログファイルに記録する。これは例えば、異なるマシン上の複数のプロセスからメッセージを受け付けて、[分散コンピューティング](../Page/分散コンピューティング.md "wikilink")における[ロギングサービスを実現するものである](../Page/データログ.md "wikilink")。`inetd`サービスをロギングメッセージ受信に使うことで、全てのマシンがメッセージを1つのマシンに送り、単一のログファイルにそれらを格納できる。

``` c
#include <stdio.h>
#include <stdlib.h>
#include <unistd.h>
#include <string.h>

int main(int argc, char **argv)
{
  /* メッセージのログ用バッファ */
  char str[4096];

  /* ログファイルへのポインタ */
  FILE *fp = NULL;

  /* inetdが引数を渡してきた場合は、それをファイル名として使用 */
  if(argc == 2)
    fp = fopen(argv[1], "at");
  else
    /* さもなくば、/tmpディレクトリでファイルをオープン */
    fp = fopen("/tmp/errorLog.txt", "at");

  /* ログファイルをオープンできない場合は異常終了 */
  if(fp == NULL)
    return -1;

  while(!feof(stdin))
  {
    /* 改行まで読み込む。最大4095文字。
       fgetsは文字列をNULLでターミネートする。 */
    fgets(str, 4096, stdin);

    /* ログファイルに文字列を書き込み、フラッシュする。 */
    fprintf(fp, "%s", str);
    fflush(fp);
  }

  /* ログファイルをクローズし、終了する。 */
  fclose(fp);
  return 0;
}
```

この場合、全メッセージを単一のファイルに記録したいので、サービスは1つのインスタンスのみで全要求に応えるようにしたい。従って、使うプロトコルとしてはUDPが適切である。まず、使っていないポート番号を選択する。ここでは9999が使われていなかったものとし、それを使うことにする。`/etc/services` には次のような一行が書かれる。

`errorLogger 9999/udp`

そして`/etc/inetd.conf`には次のように書かれる。

`errorLogger dgram udp wait root /usr/local/bin/errlogd errlogd /tmp/logfile.txt`

これによりinetdは `/usr/local/bin/errlogd` というプログラムを`errlogd /tmp/logfile.txt`という引数で起動する（inetd.confの他のフィールドの意味については、inetd.confの[manページ](https://ja.wikipedia.org/wiki/manページ "wikilink")を参照されたい）。第1引数は常に実行ファイル名であり、第2引数はログファイルのファイル名`/tmp/logfile.txt`である。inetdは必要に応じてサービスを起動し、入出力ストリームをポート番号9999にアタッチし、そのポートに送られた全文字列がログファイルに記録される。**wait**と指定することで、全要求を単一のサーバインスタンスで扱うことを inetdに知らせる。上で示した[telnet](https://ja.wikipedia.org/wiki/telnet "wikilink")の場合とは異なる（telnetは要求が来るたびに新たなサーバが起動される）。

なお、この例で示したような機能は通常[syslog](https://ja.wikipedia.org/wiki/syslog "wikilink")を使って実装される。そのサーバであるsyslogdはinetdサービスではなく、inetdとは独立に起動される。

## 代替実装

inetdはセキュリティへの配慮が乏しいため、最近では代替実装として[xinetd](https://ja.wikipedia.org/wiki/xinetd "wikilink")、rlinetd、[ucspi-tcp](https://ja.wikipedia.org/wiki/ucspi-tcp "wikilink")などがよく使われている。[Linux](https://ja.wikipedia.org/wiki/Linux "wikilink")の対応はディストリビューションによって様々である。[macOS](https://ja.wikipedia.org/wiki/macOS "wikilink")は（[Mac OS X v10.2](../Page/Mac_OS_X_v10.2.md "wikilink") 以降）xinetdを使っていた。[Mac OS X v10.4では](../Page/Mac_OS_X_v10.4.md "wikilink")、inetdの機能は[launchd](https://ja.wikipedia.org/wiki/launchd "wikilink")に統合されている。

inetdが提供するサービスは完全に切捨て可能である。これは、マシンを単機能サーバとする場合によく使われるようになりつつある。例えば、HTTPサーバは、[httpdだけを起動するよう設定し](../Page/Webサーバ.md "wikilink")、他のポートを全くオープンしないようにできる。[ファイアウォール](../Page/ファイアウォール.md "wikilink")専用マシンは全くサービスを起動しないようにできる。

## セキュリティ問題

サービスディスパッチャとしてのinetdはセキュアでないというわけではないが、inetdが提供するサービスの長いリストはセキュリティ専門家でも正しく保つのが難しい。サービスに潜在的なセキュリティ問題がある可能性などを考慮する必要がある。このため不要なサービスをデフォルトではOFFにしておくのが一般化している。/etc/inetd.confのほぼ全てのサービスがコメントアウトされたディストリビューションも珍しくない。

## 関連項目

  - [TCP Wrapper](../Page/TCP_Wrapper.md "wikilink")

## 脚注

## 参考文献

  - [inetd(8)](https://kaworu.jpn.org/doc/FreeBSD/jman/man8/inetd.8.php) FreeBSD版マニュアル
  - [inetd(8)](https://linuxjm.osdn.jp/html/netkit/man8/inetd.8.html) Linux版マニュアル（JM Project）
  - [inetd(1M)](https://docs.oracle.com/cd/E56342_01/html/E54076/inetd-1m.html) man page (Solaris 10 Reference Manual)
  - [inetd(1M)](https://nixdoc.net/man-pages/HP-UX/man1m/inetd.1m.html) man page（HP-UX リファレンス）

[Category:UNIXのソフトウェア](https://ja.wikipedia.org/wiki/Category:UNIXのソフトウェア "wikilink")

1.  [inetd(8)](http://www.freebsd.org/cgi/man.cgi?query=inetd) FreeBSD Man Pages、History節を参照
> この記事は[ \(BSD\)](https://ja.wikipedia.org/wiki/_\(BSD\))から翻訳されています。


**ソケット**（，**通信端点**\[1\]\[2\]）とは、[BSD](../Page/BSD.md "wikilink")系[UNIX](../Page/UNIX.md "wikilink")を起源とする[APIであり](../Page/アプリケーションプログラミングインタフェース.md "wikilink")、[C言語](../Page/C言語.md "wikilink")によるアプリケーション開発での[プロセス間通信](../Page/プロセス間通信.md "wikilink")、特に[コンピュータネットワーク](https://ja.wikipedia.org/wiki/コンピュータネットワーク "wikilink")に関する[ライブラリ](../Page/ライブラリ.md "wikilink")を構成する。その起源を強調して**BSDソケット**、**バークレーソケット**などとも呼ばれる。

[1983年](https://ja.wikipedia.org/wiki/1983年 "wikilink")にリリースされた[UNIX](../Page/UNIX.md "wikilink")[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink") (OS) 4.2BSD で初めて API として実装された。ネットワークの[抽象化インタフェースとしての](../Page/抽象化_\(計算機科学\).md "wikilink")[デファクトスタンダード](../Page/デファクトスタンダード.md "wikilink")となっている。伝統的なSocket APIはC言語を対象とするが、他の[プログラミング言語](../Page/プログラミング言語.md "wikilink")でも類似のインタフェースを用意している事が多い。

ソケットの代替となるAPIとして、[STREAMS](https://ja.wikipedia.org/wiki/STREAMS "wikilink")ベースの [Transport Layer Interface](https://ja.wikipedia.org/wiki/Transport_Layer_Interface "wikilink") (TLI) がある。しかし、BSDソケットは比較にならないほど普及しており、数多くの実装が存在する。

## BSDソケットインタフェース

BSDソケットは、[ホスト間の通信や](../Page/サーバ.md "wikilink")1つのコンピュータ上の[プロセス](../Page/プロセス.md "wikilink")間の通信を可能とする。通信媒体としては様々な[入出力](../Page/入出力.md "wikilink")機器や[デバイスドライバ](../Page/デバイスドライバ.md "wikilink")を利用可能だが、その部分は[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink")の実装に依存する。このインタフェース実装は[TCP/IP](https://ja.wikipedia.org/wiki/TCP/IP "wikilink")を利用する際にはほとんどの場合で必要とされ、[インターネット](https://ja.wikipedia.org/wiki/インターネット "wikilink")を支える基盤技術の一つとなっている。当初、[カリフォルニア大学バークレー校](../Page/カリフォルニア大学バークレー校.md "wikilink")でUNIX向けに開発された。最近の全てのオペレーティングシステムには間違いなくBSDソケットが何らかの形で実装されており、インターネットへの接続の標準インタフェースとなっている。

プログラマの観点から見ると、ソケットインタフェースは3つのレベルでアクセス可能である。最も強力で基本的なレベルは RAW（生）ソケットレベルである。RAWソケットが可能とする通信制御の自由度を必要とするアプリケーションは稀であり、インターネット関連技術の開発でのみ使われるべきとされている。

## ヘッダファイル

BSDソケットにはいくつかの[ヘッダファイル](https://ja.wikipedia.org/wiki/ヘッダファイル "wikilink")がある。

  - `<sys/socket.h>`
    BSDソケットの中核となる関数とデータ構造
  - `<netinet/in.h>`
    AF_INET と AF_INET6 アドレスファミリ。インターネット上で広く使われ、IPアドレスとTCP/[UDP](https://ja.wikipedia.org/wiki/UDP "wikilink")のポート番号が含まれる。
  - `<sys/un.h>`
    AF_UNIX アドレスファミリ。同一コンピュータ上で動作するプログラム間のローカルな通信に使用。ネットワーク上では使われない。
  - `<arpa/inet.h>`
    数値としてIPアドレスを操作する機能の定義
  - `<netdb.h>`
    プロトコル名とホスト名を数値アドレスに変換する機能の定義。ローカルなデータやDNSを検索する。

## TCP

[TCP](../Page/Transmission_Control_Protocol.md "wikilink") はコネクションの概念を提供する。TCPソケットを生成するには `socket()` 関数で `AF_INET` または `AF_INET6` と `SOCK_STREAM` を引数に指定する。

### サーバ

単純なTCPサーバの設定は、以下のように行われる。

  - TCPソケットを生成（`socket()`呼び出し）
  - そのソケットを listen（コネクション確立要求待ち受け）[ポートにバインド](../Page/ポート_\(コンピュータネットワーク\).md "wikilink")（`bind()`呼び出し）。`bind()` を呼び出す前に、`sockaddr_in` 構造体を宣言し、その中身をクリアし（`bzero()` または `memset()`）、その `sin_family` フィールドを `AF_INET` か `AF_INET6` に設定し、`sin_port` フィールドに listen 対象ポート番号を[ネットワークバイトオーダで設定する](https://ja.wikipedia.org/wiki/エンディアン "wikilink")。`short int` をネットワークバイトオーダに変換するには、`htons()` 関数を使う。
  - そのソケットをコネクションの listen に使用するため、`listen()` を呼び出す。
  - 入ってきたコネクションを `accept()` 呼び出しで受け付ける。これはコネクションが受信されるまでブロックし、受信したコネクションのソケット記述子を返す。最初の記述子は listen 用記述子のままであり、`accept()` はそのソケットをクローズするまで何度でも呼び出せる。
  - 遠隔のホストと通信を行う。`send()`と`recv()`、または`write()`と`read()`を使用する。
  - 不要になったら、`close()` を使ってオープンされた各ソケットをクローズする。なお、`fork()` が行われた場合、各プロセスは見えているソケットを全てクローズしなければならず、複数のプロセスが同じソケットを同時に使ってはならない。

[C99](../Page/C99.md "wikilink") でのサーバー側のソースコード。

``` c
#include <stdio.h>
#include <string.h>
#include <unistd.h>
#include <sys/types.h>
#include <sys/socket.h>
#include <netinet/in.h>
#include <arpa/inet.h>

int main(void)
{
    // サーバーソケット作成
    int sock = socket(AF_INET, SOCK_STREAM, 0);
    if (sock == -1)
    {
        perror("socket");
        return 1;
    }

    // struct sockaddr_in 作成
    struct sockaddr_in sa = {0};
    sa.sin_family = AF_INET;
    sa.sin_port = htons(1100);
    sa.sin_addr.s_addr = htonl(INADDR_ANY);

    // バインド
    if (bind(sock, (struct sockaddr*) &sa, sizeof(struct sockaddr_in)) == -1)
    {
        perror("bind");
        goto bail;
    }

    // リッスン
    if (listen(sock, 128) == -1)
    {
        perror("listen");
        goto bail;
    }

    while (1)
    {
        // クライアントの接続を待つ
        int fd = accept(sock, NULL, NULL);
        if (fd == -1)
        {
            perror("accept");
            goto bail;
        }

        // 受信
        char buffer[4096];
        int recv_size = read(fd, buffer, sizeof(buffer) - 1);
        if (recv_size == -1)
        {
            perror("read");
            close(fd);
            goto bail;
        }

        // 受信内容を表示
        buffer[recv_size] = '\0';
        printf("message: %s\n", buffer);

        // ソケットのクローズ
        if (close(fd) == -1)
        {
            perror("close");
            goto bail;
        }
    }

bail:
    // エラーが発生した場合の処理
    close(sock);
    return 1;
}
```

### クライアント

TCPクライアントの設定は、以下のように行われる。

  - TCPソケットを生成する（`socket()`呼び出し）
  - `connect()` でサーバに接続する。このとき、`sockaddr_in` 構造体の `sin_family` フィールドは `AF_INET` か `AF_INET6` とし、`sin_port` には通信相手が listen しているはずのポート番号をネットワークバイトオーダで設定し、`sin_addr` にもネットワークバイトオーダで相手の（IPv4 か IPv6 の）アドレスを設定する。
  - サーバと通信する。`send()`と`recv()`、または`write()`と`read()`を使用する。
  - コネクションの終了と削除処理を `close()` で行う。なお、`fork()` が行われた場合、各プロセスは見えているソケットを全てクローズしなければならず、複数のプロセスが同じソケットを同時に使ってはならない。

[C99](../Page/C99.md "wikilink") でのクライアント側のソースコード。

``` c
#define _BSD_SOURCE

#include <stdio.h>
#include <string.h>
#include <unistd.h>
#include <netdb.h>
#include <sys/types.h>
#include <sys/socket.h>
#include <netinet/in.h>
#include <arpa/inet.h>

#define MESSAGE "Hello World!"

int main(void)
{
    // ソケット作成
    int sock = socket(AF_INET, SOCK_STREAM, 0);
    if (sock == -1)
    {
        perror("socket");
        return 1;
    }

    // struct sockaddr_in 作成
    struct sockaddr_in sa = {0};
    sa.sin_family = AF_INET;
    sa.sin_port = htons(1100);

    // localhost の IP アドレスを引く
    struct hostent *hostent = gethostbyname("localhost");
    if (hostent == NULL)
    {
        herror("gethostbyname");
        goto bail;
    }
    memcpy(&sa.sin_addr, hostent->h_addr_list[0], sizeof(sa.sin_addr));

    // 接続
    if (connect(sock, (struct sockaddr*) &sa, sizeof(struct sockaddr_in)) == -1)
    {
        perror("connect");
        goto bail;
    }

    // 送信
    if (write(sock, MESSAGE, strlen(MESSAGE)) == -1)
    {
        perror("write");
        goto bail;
    }

    // クローズ
    close(sock);
    return 0;

bail:
    // エラーが発生した場合の処理
    close(sock);
    return 1;
}
```

上記のソースコードは gcc の場合 `-std=c99` をつけることによりコンパイル可能であるが、`-std=gnu99` を使用した場合は最初から定義されているので `#define _BSD_SOURCE` はあっても無くてもどちらでも良い。`#define _BSD_SOURCE` が無いと `herror()` が使えない。

## UDP

[UDP](../Page/User_Datagram_Protocol.md "wikilink") はコネクションレスのプロトコルであり、パケットが必ず相手に届くことは保証されない。UDPパケットは順序通りに届くとは限らず、1つのパケットが複数個届くこともありうるし、全く届かないこともある。このようにほとんど何も保証されないため、UDP は TCP に比べてオーバヘッドが小さい。コネクションレスであるとは、2つのホスト間にコネクションやストリームといったものがなく、データが単に個々のパケット（datagram）として届けられることを意味している。

UDP のアドレス空間、すなわちUDPポート番号は、TCPポートとは別物である。

### サーバ

[C99](../Page/C99.md "wikilink") でのサーバ側のソースコード。ポート番号 7654 で UDP サーバを開く。

``` c
#include <stdio.h>
#include <string.h>
#include <unistd.h>
#include <sys/socket.h>
#include <sys/types.h>
#include <netinet/in.h>

int main(void)
{
    // ソケット作成
    int sock = socket(AF_INET, SOCK_DGRAM, 0);
    if (sock == -1)
    {
        perror("socket");
        return 1;
    }

    // struct sockaddr_in 作成
    struct sockaddr_in sa = {0};
    sa.sin_family = AF_INET;
    sa.sin_port = htons(7654);
    sa.sin_addr.s_addr = htonl(INADDR_ANY);

    // バインド
    if (bind(sock, (struct sockaddr *) &sa, sizeof(struct sockaddr_in)) == -1)
    {
        perror("bind");
        goto bail;
    }

    while (1)
    {
        // 受信
        char buffer[4096];
        socklen_t addrlen = sizeof(struct sockaddr_in);
        ssize_t recv_size = recvfrom(sock, (void *) buffer, sizeof(buffer) - 1, 0, (struct sockaddr *) &sa, &addrlen);
        if (recv_size == -1)
        {
            perror("recvfrom");
            goto bail;
        }

        // 受信内容表示
        buffer[recv_size] = '\0';
        printf("datagram: %s\n", buffer);
    }

bail:
    // エラーが発生した場合の処理
    close(sock);
    return 1;
}
```

`bind()` は、ソケットとアドレス/ポートを結びつける。

最後の無限ループは `recvfrom()` を使ってポート番号 7654 からのUDPパケットを受信する。引数は以下の通り。

  - ソケット
  - バッファへのポインタ
  - バッファの大きさ
  - フラグ（read などの他のソケット受信関数と同じ）
  - アドレス構造体
  - アドレス構造体の大きさ

### クライアント

[C99](../Page/C99.md "wikilink") でのクライアント側のソースコード。ポート 7654、アドレス 127.0.0.1 に "Hello World\!" という内容の UDP パケットを送る。

``` c
#include <stdio.h>
#include <string.h>
#include <unistd.h>
#include <sys/socket.h>
#include <sys/types.h>
#include <netinet/in.h>
#include <arpa/inet.h>

#define MESSAGE "Hello World!"

int main(void)
{
    // ソケット作成
    int sock = socket(AF_INET, SOCK_DGRAM, 0);
    if (sock == -1)
    {
        perror("socket");
        return 1;
    }

    // struct sockaddr_in 作成
    struct sockaddr_in sa = {0};
    sa.sin_family = AF_INET;
    sa.sin_port = htons(7654);
    sa.sin_addr.s_addr = inet_addr("127.0.0.1");

    // 送信
    int bytes_sent = sendto(sock, MESSAGE, strlen(MESSAGE), 0, (struct sockaddr*) &sa, sizeof(struct sockaddr_in));
    if (bytes_sent == -1)
    {
        perror("sendto");
        goto bail;
    }

    // クローズ
    close(sock);
    return 0;

bail:
    // エラーが発生した場合の処理
    close(sock);
    return 1;
}
```

## UNIXドメインソケット

IP の場合は IP アドレス＋ポート番号で接続先を指定するのに対して、UNIXドメインソケットの場合はファイルパスで指定する。

## 関数

### socket()

`socket()` は通信の一方の終端を作成し、それを表す[ファイル記述子](https://ja.wikipedia.org/wiki/ファイル記述子 "wikilink")を返す。`socket()` には以下の3つの引数がある。

  - <var>domain</var> - 生成するソケットのプロトコルファミリを指定する。
      - `AF_INET` - [IPv4](https://ja.wikipedia.org/wiki/IPv4 "wikilink")
      - `AF_INET6` - [IPv6](https://ja.wikipedia.org/wiki/IPv6 "wikilink")
      - `AF_UNIX` - [UNIXドメインソケット](https://ja.wikipedia.org/wiki/UNIXドメインソケット "wikilink")
  - <var>type</var> - ソケットのタイプ指定。
      - `SOCK_STREAM` - 信頼性のあるストリーム指向サービス（TCPに対応）
      - `SOCK_DGRAM` - データグラムサービス（UDPに対応）
      - `SOCK_SEQPACKET` - `SOCK_STREAM`とほぼ同じだが、受信したパケットを読み出す際にパケット全体を読み出さないと、残りを破棄する。
      - `SOCK_RAW` - IPレベルのプロトコル処理をユーザー側で用意するときに使用
  - <var>protocol</var> - 通常 0 を指定し、デフォルトの物が選ばれる。トランスポート層のプロトコルは、<var>domain</var> と <var>type</var> で指定されるが（[TCPの場合](../Page/Transmission_Control_Protocol.md "wikilink")、`AF_INET` または `AF_INET6` と `SOCK_STREAM`、[UDPの場合](../Page/User_Datagram_Protocol.md "wikilink")、同様の `AF_` 値と `SOCK_DGRAM`）、明示的に指定することも可能で、その値は \<netinet/in.h\> に定義されている。

エラーが発生すると -1 を返す。そうでない場合、新たに確保された記述子を表す整数を返す。

``` c
# include <sys/types.h>
# include <sys/socket.h>
int socket(int domain, int type, int protocol);
```

### gethostbyname() と gethostbyaddr()

`gethostbyname()` と `gethostbyaddr()` は名前やアドレスで指定されたインターネット上のホストを表す <var>struct hostent</var> というデータ構造へのポインタを返す。その中には、ネームサーバから得られた情報、/etc/hosts ファイルから得られた情報などが格納されている。ローカルにネームサーバが動作していない場合、/etc/hosts ファイルを参照する。以下の引数がある。

  - <var>name</var> - ホスト名を指定。例えば "www.wikipedia.org"
  - <var>addr</var> - <var>struct in_addr</var> へのポインタ。中身としてホストのアドレスを指定。
  - <var>len</var> - <var>addr</var> の長さをバイト数で指定。
  - <var>type</var> - アドレスのドメイン型を指定。例えば、AF_INET

エラーが発生するとNULLポインタを返し、<var>h_errno</var> を見れば詳しいエラーの原因（再試行すべきか否か）がわかる。そうでない場合、有効な <var>struct hostent \*</var> が返される。

``` c
struct hostent *gethostbyname(const char *name);
struct hostent *gethostbyaddr(const void *addr, int len, int type);
```

### connect()

`connect()` はコネクションの確立に成功すると 0 を返し、エラーが発生すると -1 を返す。

コネクションレスのソケットの場合（[User Datagram Protocol](../Page/User_Datagram_Protocol.md "wikilink")）、`connect()` は送受信の相手を指定するのに使われ、`send()` と `recv()` をコネクションレスのソケットで使えるようになる。

``` c
# include <sys/types.h>
# include <sys/socket.h>
int connect(int sockfd, const struct sockaddr *serv_addr, socklen_t addrlen);
```

### bind()

`bind()` はソケットにアドレスを設定する。`socket()` で生成された時点では、ソケットはアドレスファミリは指定されているが、アドレスは設定されていない。ソケットは、コネクションを受け付ける前にバインド（アドレス設定）される必要がある。以下の引数がある。

  - `sockfd` - バインドすべきソケットの記述子
  - `serv_addr` - バインドすべきアドレスを表す `sockaddr` 構造体へのポインタ
  - `addrlen` - `sockaddr` 構造体の大きさ

成功すると 0 を返し、エラーが発生すると -1 を返す。

``` c
# include <sys/types.h>
# include <sys/socket.h>
int bind(int sockfd, struct sockaddr *my_addr, socklen_t addrlen);
```

### listen()

`listen()` はバインドされたソケットでコネクション確立要求を待ち受ける。`SOCK_STREAM` または `SOCK_SEQPACKET` の場合のみ有効。以下の引数がある。

  - `sockfd` - ソケット記述子
  - `backlog` - ある時点でペンディングにできる（キューイングできる）最大コネクション数。一般にOSが上限を設けている。

コネクションは `accept()` されるとデキューされる。成功すると 0 を返す。エラーが発生すると -1 を返す。

``` c
# include <sys/socket.h>
int listen(int sockfd, int backlog);
```

### accept()

`accept()` は、リモートホストからのコネクション確立要求を受け付ける。以下の引数がある。

  - `sockfd` - listen していたソケットの記述子
  - `cliaddr` - クライアントのアドレス情報を `accept()` の中で格納するための sockaddr 構造体へのポインタ
  - `addrlen` - `cliaddr` が指す sockaddr 構造体の大きさを格納する `socklen_t` へのポインタ。`accept()` から戻ったとき、実際に格納されたデータ構造のサイズに更新されている。

コネクションが確立された場合、それに対応したソケット記述子を返す。エラーが発生すると -1 を返す。

``` c
# include <sys/types.h>
# include <sys/socket.h>
int accept(int sockfd, struct sockaddr *cliaddr, socklen_t *addrlen);
```

## ブロッキングとノンブロッキング

BSDソケットは、ブロッキングとノンブロッキングという2つのモードを持つ。ブロッキング・ソケットは指定されたデータを全て送受信し終わるまで呼び出したライブラリ関数から戻ってこない。これは、ソケットで listen を続けたい場合に困ったことになる。プログラムは決して届かないデータを待って動けなくなる可能性がある。

ブロッキングかノンブロッキングかを指定するには、`fcntl()` か [`ioctl`](https://ja.wikipedia.org/wiki/ioctl "wikilink")`()` 関数を使う。

## 注意点

`socket()` で確保されたリソースは `close()` を使うまで解放されない。これは、`connect()` が成功するまで再試行を繰り返すような実装で注意が必要となる。`socket()` を呼び出したら必ず対応する `close()` を呼び出す必要がある。close を使うには \<unistd.h\> をインクルードする必要がある。

## 参考文献

ソケットインタフェースの正当な標準定義は以下の POSIX 標準に含まれている。

  - IEEE Std. 1003.1-2001 Standard for Information Technology -- Portable Operating System Interface (POSIX).
  - Open Group Technical Standard: Base Specifications, Issue 6, December 2001.
  - ISO/IEC 9945:2002

この標準に関する情報と現在進行の作業については、[the Austin website](http://www.opengroup.org/austin/) にある。

ソケットAPIの[IPv6](https://ja.wikipedia.org/wiki/IPv6 "wikilink")拡張は、RFC 3493 と RFC 3542 にある。

## 脚註

### 出典

## 関連項目

  - [コンピュータネットワーク](https://ja.wikipedia.org/wiki/コンピュータネットワーク "wikilink")
  - [Winsock](../Page/Winsock.md "wikilink")

## 外部リンク

  -
  -
  -
  -
  -
  -
  -
  -
  - [Porting Berkley Socket programs to Winsock](http://msdn.microsoft.com/en-us/library/ms740096.aspx) - [MSDN](https://ja.wikipedia.org/wiki/MSDN "wikilink")

[Category:インターネット技術](https://ja.wikipedia.org/wiki/Category:インターネット技術 "wikilink") [Category:プロセス間通信](https://ja.wikipedia.org/wiki/Category:プロセス間通信 "wikilink") [Category:BSD](https://ja.wikipedia.org/wiki/Category:BSD "wikilink") [Category:UNIXのシステムコール](https://ja.wikipedia.org/wiki/Category:UNIXのシステムコール "wikilink") [Category:API](https://ja.wikipedia.org/wiki/Category:API "wikilink")

1.
2.
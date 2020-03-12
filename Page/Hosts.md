> この記事は[Hosts](https://ja.wikipedia.org/wiki/Hosts)から翻訳されています。


**hosts**（ホスツ）とは、[TCP/IP](https://ja.wikipedia.org/wiki/TCP/IP "wikilink")を利用する[コンピュータ](../Page/コンピュータ.md "wikilink")における[ホスト名](../Page/ホスト名.md "wikilink")のデータベースで、[IPアドレス](../Page/IPアドレス.md "wikilink")とホスト名の対応を記述したテキストファイルである。hosts のフォーマットは、[4.2BSDで登場した](../Page/BSD.md "wikilink")。インターネットの初期には、集中的に管理されている hosts ファイルをコピー（ダウンロード）して、各ノードで使用する、といった単純な運用が行われていた時代もあったが、[DNSが一般的になった以後は](../Page/Domain_Name_System.md "wikilink")、hosts ファイルには各ノードでローカルに必要な最低限の対応のみ記述し、外部へのアクセスに必要な名前解決はもっぱらDNSで行う、という運用が普通となっている。

## 書式

hostsファイルはテキストファイルで、1行ごとに以下のような書式で書く。

`IPアドレス ホスト名...`

IPアドレスやホスト名の区切りには[スペース](../Page/スペース.md "wikilink")または[タブを用いる](../Page/タブキー.md "wikilink")。 ホスト名は1行に複数書くことができ、もっとも左のものが「正式」とみなされる。IPアドレスからホスト名への変換の際には「正式」のホスト名が返される。

以下に例を示す。

`127.0.0.1 localhost`
`211.115.107.162 ja.wikipedia.org commons.wikimedia.org`

この例では、localhostのIPアドレスが127.0.0.1（ループバックアドレス）であり、ja.wikipedia.orgとcommons.wikimedia.orgのIPアドレスが211.115.107.162であると定義している。

## 動作原理

TCP/IPを利用するアプリケーションを実行すると、そこから呼び出される[リゾルバ](../Page/リゾルバ.md "wikilink")ライブラリがhostsを読み込み、その内容にしたがってIPアドレスとホスト名の相互変換（[名前解決](https://ja.wikipedia.org/wiki/名前解決 "wikilink")）を行う。

hostsの変更を有効にするために、アプリケーションの再起動が必要となる場合がある。

## hostsの用途

今日ではDNSが広く用いられているため、hostsの用途は限定的・副次的なものである。

### 起動時に最低限必要なホスト名

DNSはネットワークが稼動していなければ参照できないが、hosts はディスクが読めれば参照できる。 したがって、OSの起動時に最低限必要となるホスト名とIPアドレスの対応をhostsに書くことが一般的である。

ほとんどの場合、OSをインストールした時点で最初からlocalhostが記述されている。 IPアドレスを固定で設定してあるコンピュータの場合は、それも書くことが多い。 場合によっては、LAN内の[サーバ](../Page/サーバ.md "wikilink")や[ルーター](../Page/ルーター.md "wikilink")などを書くこともある。

### DNS不調時の代替

DNSが不調でホスト名が解決できない場合に、hostsファイルで代用することができる。 特定のホストのIPアドレスがわかっていて、とりあえずそこにアクセスできればよいという場合には、一時しのぎとして有効である。

たとえば、ウィキペディアのDNSが不調の場合、前記の例のように記述しておけば、ja.wikipedia.orgやcommons.wikimedia.orgにアクセスできるようになる。

DNSの特性上、特定ホストのIPアドレスが変更されると外部DNSのデータベースが即座に更新されないため接続できなくなる事がある。この場合にも一時的な対策として使用される。

ただし、外部のホスト名やIPアドレスはいつ変更されるかわからないので、平素からこのような使い方をすることは避けるべきである。

### ウイルスチェックなど

[アンチウイルスソフトウェア](../Page/アンチウイルスソフトウェア.md "wikilink")が[電子メール](../Page/電子メール.md "wikilink")をスキャンするために、hosts を利用することがある。

たとえば、[電子メールクライアント](../Page/電子メールクライアント.md "wikilink")の[POPサーバの設定がmail](../Page/Post_Office_Protocol.md "wikilink").example.ne.jpとなっており、hostsファイルにはlocalhostのみが記述されているものとする。 ここにアンチウイルスソフトウェアをインストールして、電子メールスキャンを有効にすると、アンチウイルスソフトは常駐してPOP[プロキシ](../Page/プロキシ.md "wikilink")として機能するとともに、hostsを以下のように書き換える。

`127.0.0.1 localhost mail.example.ne.jp`

こうすると、電子メールクライアントはmail.example.ne.jpにアクセスしているつもりが、実はローカルプロキシとして機能しているアンチウイルスソフトにアクセスすることになる。アンチウイルスソフトは本物のmail.example.ne.jpからメールを受信し、ウイルスチェックを行って電子メールクライアントに渡す。

このような仕組みをとることで、電子メールクライアントの設定を変更せずに、電子メールクライアントとPOPサーバの間に介入することができる。 ただし、アンチウイルスソフトが動作していなかったり、アンインストールが正常に完了せずhostsファイルが書き換えられたまま残ったりすると、メールを受信できない事態になる。

なお、これは一例であり、電子メールをスキャンするすべてのアンチウイルスソフトがこのような仕組みを用いているとは限らない。

### NISマップ

NISのhostsマップを使用している場合、NISサーバは配布する情報をhostsに保持しておく必要がある。 通常は、LAN内の各コンピュータの情報が含まれる。

UNIXのみで構成されたネットワークでない限り、NISをホスト名の解決に用いることは稀なので、今日ではこのような利用法はあまり一般的ではない。

## 格納場所

hostsファイルは一般に"hosts"というファイル名であるが、格納場所は[OSによって異なる](../Page/オペレーティングシステム.md "wikilink")。

| OS名                                                                     | 格納場所                                        |
| ----------------------------------------------------------------------- | ------------------------------------------- |
| [UNIX](../Page/UNIX.md "wikilink")/[Linux](../Page/Linux.md "wikilink") | /etc/hosts                                  |
| [Windows NT系列](../Page/Microsoft_Windows_NT.md "wikilink")              | %SystemRoot%\\System32\\drivers\\etc\\hosts |
| [Windows 95系列](../Page/Microsoft_Windows_95.md "wikilink")              | %WINDOWS%\\hosts                            |
| [macOS](https://ja.wikipedia.org/wiki/macOS "wikilink")                 | /etc/hosts（シングルユーザーモードでのみ有効）                |
| [BeOS](../Page/BeOS.md "wikilink")                                      | /boot/beos/etc/hosts                        |

## 類似機能との関係

ホスト名とIPアドレスの対応をとる機能は、hosts のほかにDNSがある。 また、[NISのhostsマップも用いられることがある](https://ja.wikipedia.org/wiki/Network_Information_Service "wikilink")。 これらのうちいくつかを利用している環境では、その優先順位が問題となる。

現代的なUNIXでは、/etc/nsswitch.confなどの定義ファイルで優先順位を定義することができる。 Windowsにおいては、hostsが優先され、次にDNSが参照される。

## セキュリティ上の問題

ウイルスや[スパイウェア](https://ja.wikipedia.org/wiki/スパイウェア "wikilink")などの[マルウェア](../Page/マルウェア.md "wikilink")が hosts を書き換えて、ユーザを偽のホストへ誘導することがある（[ファーミング](../Page/ファーミング.md "wikilink")詐欺）。これは hosts が一般にDNSより優先して参照されることを悪用したものである。

対策としては、以下のようなことが考えられる。

  - hosts の属性を書込み禁止にする。（ただしマルウェアが管理者権限で動作していれば無効）
  - hosts の変更を監視するようなセキュリティソフトを利用する。
  - hosts の内容をときどきチェックする。
  - オンラインショッピング・オンラインバンキング・ソフトウェアダウンロードなどのサイトでは、正しいサーバかどうかよく確認する。

## 参考文献

  - [hostsファイルとは？](https://web.archive.org/web/20140207051648/http://swedish-cloud.com/)（2014年2月7日時点の[アーカイブ](../Page/インターネットアーカイブ.md "wikilink")） - 平易な言葉で書かれたhostsファイルの解説。

## 関連項目

  - [LMHOSTS](https://ja.wikipedia.org/wiki/LMHOSTS "wikilink")

[Category:UNIX](https://ja.wikipedia.org/wiki/Category:UNIX "wikilink") [Category:Domain_Name_System](https://ja.wikipedia.org/wiki/Category:Domain_Name_System "wikilink")
> この記事は[TCP Wrapper](https://ja.wikipedia.org/wiki/TCP_Wrapper)から翻訳されています。


**TCP Wrapper** は、[Linux](https://ja.wikipedia.org/wiki/Linux "wikilink")や[BSD](../Page/BSD.md "wikilink")系の（[Unix系](../Page/Unix系.md "wikilink")）[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink")上の[TCP/IP](https://ja.wikipedia.org/wiki/TCP/IP "wikilink")サーバへのネットワークアクセスをフィルタリングするホストベースの[ACLシステムである](https://ja.wikipedia.org/wiki/アクセス制御リスト "wikilink")。ホストまたはサブネットの[IPアドレス](../Page/IPアドレス.md "wikilink")、[ホスト名](../Page/ホスト名.md "wikilink")、[Identプロトコル](https://ja.wikipedia.org/wiki/Identプロトコル "wikilink")のクエリ応答などを[アクセス制御](https://ja.wikipedia.org/wiki/アクセス制御 "wikilink")のためのフィルタのトークンとして使う。

元のコードを書いたのは Wietse Venema で、[1990年](https://ja.wikipedia.org/wiki/1990年 "wikilink")から[1995年](https://ja.wikipedia.org/wiki/1995年 "wikilink")にかけて[オランダ](https://ja.wikipedia.org/wiki/オランダ "wikilink")の[アイントホーヘン工科大学](https://ja.wikipedia.org/wiki/アイントホーヘン工科大学 "wikilink")に在籍中に開発した。[2001年](../Page/2001年.md "wikilink")[6月1日](../Page/6月1日.md "wikilink")、このプログラムは[BSDライセンス](https://ja.wikipedia.org/wiki/BSDライセンス "wikilink")でリリースされた。

TCP Wrapper の[tarボールには](../Page/Tar.md "wikilink") **[libwrap](https://ja.wikipedia.org/wiki/libwrap "wikilink")** という[ライブラリ](../Page/ライブラリ.md "wikilink")が含まれ、これに実際の機能が実装されている。当初は[inetd](https://ja.wikipedia.org/wiki/inetd "wikilink")のような[スーパーサーバ](https://ja.wikipedia.org/wiki/スーパーサーバ "wikilink")から起動されるサービスだけに対応していて、そのための **tcpd** というプログラムがあった。しかし、現在ではネットワークサービスを提供する[デーモンの多くは](https://ja.wikipedia.org/wiki/デーモン_\(ソフトウェア\) "wikilink")、直接 libwrap を[リンクできる](../Page/リンケージエディタ.md "wikilink")。これによりスーパーサーバから起動させる形式でないデーモンにも対応でき、単一プロセスで複数のコネクションを制御する場合にも対応できる。さもなくば、最初のコネクションだけがACLに対してチェックされる。

デーモンの構成ファイルにもアクセス制御ディレクティブを書ける場合があるが、TCP Wrapper の場合、実行中にACLの再構成が可能という利点がある（サービスを停止して再起動する必要がない）。

これにより、[BlockHosts](https://ja.wikipedia.org/wiki/BlockHosts "wikilink")、[DenyHosts](https://ja.wikipedia.org/wiki/DenyHosts "wikilink")、[Fail2ban](https://ja.wikipedia.org/wiki/Fail2ban "wikilink") といった[ワーム対策スクリプトが使いやすくなる](https://ja.wikipedia.org/wiki/ワーム_\(コンピュータ\) "wikilink")。つまり、コネクション数が異常に増えたり、ログイン失敗が発生したときに、クライアントのブロックを追加したり、やめたりといった制御が簡単である。

元々は、[TCPおよび](../Page/Transmission_Control_Protocol.md "wikilink")[UDPのサービスを対象としていたが](../Page/User_Datagram_Protocol.md "wikilink")、例えば特定の[ICMPパケット](../Page/Internet_Control_Message_Protocol.md "wikilink")（例えば、pingd を使う ping 要求）をフィルタリングすることもできる。

## トロイの木馬（1999年）

[1999年](../Page/1999年.md "wikilink")[1月](https://ja.wikipedia.org/wiki/1月 "wikilink")、アイントホーヘン工科大学の配布パッケージがすりかえられるという事件が発生した。すりかえ後のパッケージは[トロイの木馬になっていて](https://ja.wikipedia.org/wiki/トロイの木馬_\(ソフトウェア\) "wikilink")、インストールしたサーバ上に容易に侵入できる仕掛けをするようになっていた。すりかえの数時間後には発見され、元のパッケージに置き換えられた。これほど素早く発見されたのは、[オープンソース](../Page/オープンソース.md "wikilink")だったからだとの指摘が多数なされている。\[1\]

## 関連項目

  - [DNSBL](https://ja.wikipedia.org/wiki/DNSBL "wikilink")
  - [ファイアウォール](../Page/ファイアウォール.md "wikilink")

## 脚注

## 参考文献

  - Wietse Venema: [<cite>TCP WRAPPER Network monitoring, access control, and booby traps.](http://www.vtcif.telstra.com.au/pub/docs/security/tcp_wrapper.txt) [1992年](../Page/1992年.md "wikilink")6月15日
  - Lee Brotzman: [<cite>Wrap a Security Blanket Around Your Computer</cite>](http://www.linuxjournal.com/article/2180) Linuxjournal の記事 [1997年](https://ja.wikipedia.org/wiki/1997年 "wikilink")8月1日

## 外部リンク

  - [ITSO: TCP Wrappers overview](http://itso.iu.edu/TCP_Wrappers)
  - [HP: TCP Wrappers Information](http://docs.hp.com/en/5991-4837)
  - [Example of 'pingd' with libwrap support](http://artofhacking.com/files/phrack/phrack52/P52-07.TXT)

[Category:UNIXのソフトウェア](https://ja.wikipedia.org/wiki/Category:UNIXのソフトウェア "wikilink") [Category:オープンソースソフトウェア](https://ja.wikipedia.org/wiki/Category:オープンソースソフトウェア "wikilink") [Category:セキュリティソフト](https://ja.wikipedia.org/wiki/Category:セキュリティソフト "wikilink") [Category:ネットワークソフト](https://ja.wikipedia.org/wiki/Category:ネットワークソフト "wikilink") [Category:Transmission_Control_Protocol](https://ja.wikipedia.org/wiki/Category:Transmission_Control_Protocol "wikilink")

1.  [CERT/CC Advisory](http://www.cert.org/advisories/CA-1999-01.html)
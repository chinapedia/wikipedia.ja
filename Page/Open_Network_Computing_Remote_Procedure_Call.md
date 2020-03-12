> この記事は[Open Network Computing Remote Procedure Call](https://ja.wikipedia.org/wiki/Open_Network_Computing_Remote_Procedure_Call)から翻訳されています。


**Open Network Computing Remote Procedure Call** (**ONC RPC**) は[遠隔手続き呼出し](../Page/遠隔手続き呼出し.md "wikilink") (RPC) システムの一種。ONC RPC は[サン・マイクロシステムズ](../Page/サン・マイクロシステムズ.md "wikilink")が[Network File Systemの一部として開発したもので](../Page/Network_File_System.md "wikilink")、**Sun ONC** あるいは **Sun RPC** とも呼ばれる（以下では単に**ONC**と略記）。

ONCは[UNIX](../Page/UNIX.md "wikilink")と[C言語](../Page/C言語.md "wikilink")の[呼出規約](https://ja.wikipedia.org/wiki/呼出規約 "wikilink")に基づいている。[XDR](../Page/XDR.md "wikilink")を使ってデータを[シリアライズ](../Page/シリアライズ.md "wikilink")したり、場合によってはアクセスすべきファイル上のデータのエンコード/デコードをしたりする。そして、ONCはXDRでまとめられた内容を[UDPか](../Page/User_Datagram_Protocol.md "wikilink")[TCPを使って送信する](../Page/Transmission_Control_Protocol.md "wikilink")。あるマシン上のRPCサービスへのアクセスには[ポートマッパー](https://ja.wikipedia.org/wiki/ポートマッパー "wikilink")を使う。ポートマッパーはよく知られたポートで[クエリ](https://ja.wikipedia.org/wiki/クエリ "wikilink")を待ち受ける。一般にUDPやTCPの111番が使われる。

ONCはほとんどの[Unix系](../Page/Unix系.md "wikilink")システムに実装されている。[マイクロソフト](../Page/マイクロソフト.md "wikilink")は [Windows向けの実装を](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")[Services for UNIXで提供している](https://ja.wikipedia.org/wiki/Services_for_UNIX "wikilink")。さらに、Windows向けのONC実装はいくつかの[サードパーティー](../Page/サードパーティー.md "wikilink")が提供しており、C言語、[C++](../Page/C++.md "wikilink")、[Java](https://ja.wikipedia.org/wiki/Java "wikilink")、[.NET向けの実装がある](https://ja.wikipedia.org/wiki/.NET_Framework "wikilink")（外部リンク参照）。

ONC RPCはRFC 1831で記述されている。ONC RPCの認証機構はRFC 2695、RFC 2203、RFC 2623で記述されている。

## 関連項目

  - [Distributed Computing Environment](../Page/Distributed_Computing_Environment.md "wikilink") (DCE)
  - [XDR](../Page/XDR.md "wikilink")
  - [XML-RPC](../Page/XML-RPC.md "wikilink")

## 外部リンク

  - [ONC/RPC Implementation of the University of Aachen (Germany)](http://www.plt.rwth-aachen.de/index.php?id=258)
  - [Remote Tea (LGPL Java Implementation)](http://remotetea.sourceforge.net/)
  - [Distinct Corporation's ONC RPC for Windows](http://www.onc-rpc-xdr.com/)
  - [Linux Journal article on ONC RPC](http://www.linuxjournal.com/article/2204)

[Category:アプリケーション層プロトコル](https://ja.wikipedia.org/wiki/Category:アプリケーション層プロトコル "wikilink") [Category:インターネット標準](https://ja.wikipedia.org/wiki/Category:インターネット標準 "wikilink") [Category:遠隔手続き呼出し](https://ja.wikipedia.org/wiki/Category:遠隔手続き呼出し "wikilink") [Category:RFC](https://ja.wikipedia.org/wiki/Category:RFC "wikilink") [Category:長大な項目名](https://ja.wikipedia.org/wiki/Category:長大な項目名 "wikilink")
> この記事は[XDR](https://ja.wikipedia.org/wiki/XDR)から翻訳されています。


**XDR** (External Data Representation) とは、データ交換用の[シリアライズ](../Page/シリアライズ.md "wikilink")形式の一つ。

主に[ONC RPC](../Page/Open_Network_Computing_Remote_Procedure_Call.md "wikilink") (SunRPC) の[プレゼンテーション層](../Page/プレゼンテーション層.md "wikilink")として使われる。

## 歴史

[サン・マイクロシステムズ](../Page/サン・マイクロシステムズ.md "wikilink")によって、1987年に[RFC1014](https://ja.wikipedia.org/wiki/rfc:1014 "wikilink")、1995年に[RFC1832として](https://ja.wikipedia.org/wiki/rfc:1832 "wikilink") ONC RPCと同時に規格化され、現在は2006年の[RFC4506が最新となっている](https://ja.wikipedia.org/wiki/rfc:4506 "wikilink")。（RFC4506はRFC1832からの[技術的な変更点はない](https://ja.wikipedia.org/wiki/rfc:4506#section-2 "wikilink")）

## 特徴

[DCE/RPC](https://ja.wikipedia.org/wiki/DCE/RPC "wikilink") で使われている [DCE/NDR](http://pubs.opengroup.org/onlinepubs/9629399/chap14.htm) （及び [MS RPC](https://ja.wikipedia.org/wiki/:en:Microsoft_RPC "wikilink")/NDR）に比べ、常に統一した表現形式に[正規化](../Page/正規化.md "wikilink")する点が特徴となっている。

  - 整数（32/64bit）はネットワークバイトオーダー（[ビッグエンディアン](https://ja.wikipedia.org/wiki/ビッグエンディアン "wikilink")）に正規化。（DCE/NDRではビッグエンディアンと[リトルエンディアン](https://ja.wikipedia.org/wiki/リトルエンディアン "wikilink")の両形式をサポート）
  - [浮動小数点数](../Page/浮動小数点数.md "wikilink")（32/64/128bit）は[IEEE形式に正規化](../Page/IEEE_754.md "wikilink")。（DCE/NDRではIEEE/VAX/Cray/IBM形式）
  - 文字列は[ASCII](../Page/ASCII.md "wikilink")に正規化。（DCE/NDRではASCII/[EBCDIC](https://ja.wikipedia.org/wiki/EBCDIC "wikilink")の2形式、MS RPC/NDRでは[UTF16もサポート](../Page/UTF-16.md "wikilink")）
  - 32bit単位にアラインされるよう、必要に応じてパディングされる。

上記の特徴のため、個々の環境では内部形式と統一された正規化形式との変換ルーチンのみ用意すればよい。（DCE/NDRでは各サポート形式と内部形式との変換ルーチンが必要）

その反面、マシンの内部フォーマットと正規化形式と違う場合、同じアーキテクチャ同士のデータ交換でも常に変換オーバーヘッドが発生する。

  - 例）　[IA-32](../Page/IA-32.md "wikilink")/[64系](../Page/IA-64.md "wikilink")（リトルエンディアン）同士の通信では、常にエンディアン変換が発生する。（Sun Workstation同士の通信の場合、ビッグエンディアンのため、エンディアン変換は発生しない）

rpcgenというスタブ・コンパイラを使うと、整列化・非整列化するプログラムが自動的に生成される。

共用ファイルのデータフォーマットとしてXDRのみを使うこともある。

## XDRを利用しているプロトコル・システム

  - [ONC RPC](../Page/Open_Network_Computing_Remote_Procedure_Call.md "wikilink")
  - [NFS](https://ja.wikipedia.org/wiki/Network_File_System_\(protocol\) "wikilink")
  - [R言語](../Page/R言語.md "wikilink")
  - [SpiderMonkey](https://ja.wikipedia.org/wiki/SpiderMonkey "wikilink") (Javascriptエンジン)
  - [sFlow](https://ja.wikipedia.org/wiki/sFlow "wikilink") （ネットワークモニタ用プロトコル）
  - [libvirt](https://ja.wikipedia.org/wiki/libvirt "wikilink")

## 関連項目

  - [ONC RPC](../Page/Open_Network_Computing_Remote_Procedure_Call.md "wikilink")
  - [DCE/NDR](http://pubs.opengroup.org/onlinepubs/9629399/chap14.htm)

[Category:データシリアライゼーションフォーマット](https://ja.wikipedia.org/wiki/Category:データシリアライゼーションフォーマット "wikilink") [Category:RFC](https://ja.wikipedia.org/wiki/Category:RFC "wikilink")
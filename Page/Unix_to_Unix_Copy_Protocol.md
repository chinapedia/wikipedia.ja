> この記事は[Unix to Unix Copy Protocol](https://ja.wikipedia.org/wiki/Unix_to_Unix_Copy_Protocol)から翻訳されています。


**Unix to Unix Copy Protocol**（ユニックス トゥ ユニックス コピー プロトコル、**UUCP**）は、[UNIX](../Page/UNIX.md "wikilink")マシン同士でデータ転送を行う[通信プロトコル](../Page/通信プロトコル.md "wikilink")の一種。初期の[インターネット](../Page/インターネット.md "wikilink")の通信手段として広く使われていた。

料金[定額制](../Page/定額制.md "wikilink")の電話回線において、または電話料金が安い夜間だけに、ファイルを転送したり、転送すべきデータが一定以上蓄積されたら転送するなど、[ダイヤルアップで使うことが想定されている](../Page/ダイヤルアップ接続.md "wikilink")。

[専用線](../Page/専用線.md "wikilink")が非常に高価であった初期のインターネットでは広く使われていたが、インターネットプロトコルとして[TCP/IPが採用され](../Page/インターネット・プロトコル・スイート.md "wikilink")、さらに通信料金が安くなり、インターネット接続が高速化され、また[定額制](../Page/定額制.md "wikilink")・[常時接続](../Page/常時接続.md "wikilink")が当たり前になった現在では、そのような環境にない国や地域を除いて、あまり使われない。

UUCPが依然使われている例として、[通信衛星](../Page/通信衛星.md "wikilink")による非常に高価な通信手段しかない洋上の[船舶](https://ja.wikipedia.org/wiki/船舶 "wikilink")におけるメール交換が上げられる。

UUCP全盛の時代においては、**[バケツリレー](https://ja.wikipedia.org/wiki/バケツ#バケツリレー "wikilink")**と言う名でしばしば比喩される仕組みによって、[メールや](../Page/電子メール.md "wikilink")[ネットニュース](../Page/ネットニュース.md "wikilink")が各組織に配信されていた。すなわち、ある組織A（研究機関、大学、企業など）からある組織Dにメッセージを送信または配信したい場合、組織Aから組織Dまでのインターネット経路上にある複数の組織の間で、UUCPによるメッセージ配信を順次リレーして（例えば組織A→組織B→組織C→組織Dの順に）、目的の組織までメッセージを届けていたのである。

メールやネットニュースのメッセージの形式は、通信に利用するレイヤに基本的には依存しないので、現在一般的なTCP/IPと、UUCP間でのやりとりも可能である（UUCP over TCP/IP）。

## 関連項目

  - [uuencode](https://ja.wikipedia.org/wiki/uuencode "wikilink")
  - [パソコン通信](../Page/パソコン通信.md "wikilink")
  - [パケット通信 (アマチュア無線)](../Page/パケット通信_\(アマチュア無線\).md "wikilink") - [RBBS](https://ja.wikipedia.org/wiki/RBBS "wikilink")、[AX.25](https://ja.wikipedia.org/wiki/AX.25 "wikilink")等
  - [ダイヤルアップ接続](../Page/ダイヤルアップ接続.md "wikilink")
  - [ストアアンドフォワード](../Page/ストアアンドフォワード.md "wikilink")
  - [インターネット](../Page/インターネット.md "wikilink")

## 外部リンク

  - RFC 976: UUCP Mail Interchange Format Standard

[Category:通信プロトコル](https://ja.wikipedia.org/wiki/Category:通信プロトコル "wikilink") [Category:ファイル転送プロトコル](https://ja.wikipedia.org/wiki/Category:ファイル転送プロトコル "wikilink") [Category:UNIXのソフトウェア](https://ja.wikipedia.org/wiki/Category:UNIXのソフトウェア "wikilink") [Category:RFC](https://ja.wikipedia.org/wiki/Category:RFC "wikilink")
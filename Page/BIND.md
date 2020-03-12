> この記事は[BIND](https://ja.wikipedia.org/wiki/BIND)から翻訳されています。


**BIND**（バインド、*Berkeley Internet Name Domain*、以前の呼名は*Berkeley Internet Name Daemon*）はインターネットでもっとも利用されている\[1\] \[2\][DNSサーバ](../Page/DNSサーバ.md "wikilink")である。[Unix系](../Page/Unix系.md "wikilink")システムにおいては特にその傾向が著しい。現在は[ISCによって開発](https://ja.wikipedia.org/wiki/Internet_Systems_Consortium "wikilink")・サポートされているが、元は[ポール・ヴィクシー](../Page/ポール・ヴィクシー.md "wikilink")が[DECに在籍中の](../Page/ディジタル・イクイップメント・コーポレーション.md "wikilink")[1988年](../Page/1988年.md "wikilink")に作り上げたソフトウェアである。

現在使われているBIND9は、それまでの古いバージョン、BIND4、BIND8のコードが保守しづらくなったことと、DNSSEC([DNS Security Extensions](https://ja.wikipedia.org/wiki/DNS_Security_Extensions "wikilink"))への対応のためにゼロから書き起こされ、2000年にリリースされた。BIND9の特徴としては、TSIG、DNS notify、nsupdate、[IPv6](https://ja.wikipedia.org/wiki/IPv6 "wikilink")、rndc flush、view、マルチプロセッサのサポート、そしてアーキテクチャーの移植性の向上がある。

## 歴史

BINDは元々80年代の初期に[DARPAの資金で開発されていたものだった](../Page/国防高等研究計画局.md "wikilink")。1980年代の中頃にDECの社員がBINDの開発を引き継いだ。開発を引き継いだ社員の一人がポール・ヴィクシーであり、DECを離れた後もBINDの開発を続けたのだった。彼はやがてISCの立ち上げに関わるようになり、そのISCがBINDのメンテナンスに責任を持つようになるのである。

BIND9の開発は民間および軍の両方と契約の元に行なわれている。ほとんどのBIND9の機能は、BINDが[マイクロソフト](../Page/マイクロソフト.md "wikilink")のDNSと競争力を持つソフトであり続けることを望む[UNIX](../Page/UNIX.md "wikilink")ベンダーの出資で実現したものであるが、DNSSECの機能はDNSのセキュリティを重視する米軍の出資によるものである。

2009年にISCは新しくBIND10を開発すると発表した。また、BIND10マスコット選定委員会により、マスコットBundyが選定されたりもした。2013年2月21日には初版であるBIND 10 1.0.0がリリースされたものの、その後の開発は難航。2017年2月に今後はBIND9を[リファクタリング](https://ja.wikipedia.org/wiki/リファクタリング "wikilink")していくとのアナウンスを行い、事実上スクラッチから再開発していくことを断念したことを表明した。\[3\]現在はBIND9がメンテナンスされ続けている。

## 脚注

## 外部リンク

  - [ISC BIND](https://www.isc.org/bind/) 公式ページ

[Category:DNSソフトウェア](https://ja.wikipedia.org/wiki/Category:DNSソフトウェア "wikilink") [Category:サーバ](https://ja.wikipedia.org/wiki/Category:サーバ "wikilink") [Category:インターネット技術](https://ja.wikipedia.org/wiki/Category:インターネット技術 "wikilink")

1.
2.
3.  <http://news.mynavi.jp/news/2017/02/16/275/> 再開発を断念、BIND 9のリファクタリングへシフト(マイナビニュース2017/2/16日付記事)
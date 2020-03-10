> この記事は[RC4](https://ja.wikipedia.org/wiki/RC4)から翻訳されています。


**RC4**（あるいは**ARCFOUR**）とは、[SSLや](https://ja.wikipedia.org/wiki/Secure_Sockets_Layer "wikilink")[WEPなどで広く使われている](../Page/Wired_Equivalent_Privacy.md "wikilink")[ストリーム暗号](https://ja.wikipedia.org/wiki/ストリーム暗号 "wikilink")である。

## 概要

RC4は[ロナルド・リベスト](../Page/ロナルド・リベスト.md "wikilink")により[1987年](https://ja.wikipedia.org/wiki/1987年 "wikilink")に開発された[ストリーム暗号](https://ja.wikipedia.org/wiki/ストリーム暗号 "wikilink")であり、このアルゴリズムで発生させた疑似乱数列と平文との排他的論理和が暗号文となる。RC4は[WEPのように利用方法によっては安全性を保てない](../Page/Wired_Equivalent_Privacy.md "wikilink")。RC4はWEP、[WPA](../Page/Wi-Fi_Protected_Access.md "wikilink")、[MPPE](https://ja.wikipedia.org/wiki/MPPE "wikilink") (Microsoft Point to Point Ecryption)、[Winny](../Page/Winny.md "wikilink")、[TLS/SSL](../Page/Transport_Layer_Security.md "wikilink")（オプション）、[SSH](../Page/Secure_Shell.md "wikilink")（オプション）で[暗号](../Page/暗号.md "wikilink")化をするのに使われている。

2015年現在では、[NSAのような機関であればTLS](../Page/アメリカ国家安全保障局.md "wikilink")/SSLを利用したとしてもRC4を解読可能であるとの疑惑があり\[1\]、[マイクロソフト](../Page/マイクロソフト.md "wikilink")ではRC4を無効化することを推奨している\[2\]\[3\]\[4\]。2015年2月、TLSのすべてのバージョンにおいてRC4の利用を禁止する RFC 7465 が公開された。

## 歴史

RC4は、1987年に[RSAセキュリティ](../Page/RSAセキュリティ.md "wikilink")社で[ロナルド・リベスト](../Page/ロナルド・リベスト.md "wikilink")によって開発された。公式には "Rivest Cipher 4" と呼ばれるが、"Ron's Code" の略語とされることもある。参照：[RC2](https://ja.wikipedia.org/wiki/RC2 "wikilink")、[RC5](https://ja.wikipedia.org/wiki/RC5 "wikilink")、[RC6](https://ja.wikipedia.org/wiki/RC6 "wikilink")。

RC4は当初は営業秘密 (trade secret) であった。ところが[1994年](../Page/1994年.md "wikilink")9月に何者かが[匿名](../Page/匿名.md "wikilink")で[Cypherpunks](https://ja.wikipedia.org/wiki/Cypherpunks "wikilink")の[メーリングリスト](../Page/メーリングリスト.md "wikilink")にRC4の解説を流してしまった。この解説は直ぐにニューズグループ sci.crypt にポストされて、[インターネット](../Page/インターネット.md "wikilink")に広がった。[アルゴリズム](../Page/アルゴリズム.md "wikilink")が公知になったので、RC4は営業秘密ではなくなったが、"RC4" の名称は[商標](../Page/商標.md "wikilink")である。従って、、RC4の名称を使うことはできない。それで、RC4はしばしば、[商標](../Page/商標.md "wikilink")問題を回避するために "ARCFOUR"（Alleged-RC4, なぜならば、RSA社は公式にはアルゴリズムをリリースしていないから）という名前が使用されることがある。

そして "ARCFOUR" は、無線通信のための[WEPや](../Page/Wired_Equivalent_Privacy.md "wikilink")[WPA](../Page/Wi-Fi_Protected_Access.md "wikilink")、あるいは[TLSや](../Page/Transport_Layer_Security.md "wikilink")[Winny](../Page/Winny.md "wikilink")などの良く使用されている暗号化プロトコルとその標準の一部となった。

## 安全性

TLS/SSLにおいてRC4を用いたCipher Suiteについては、その脆弱性に対処されており安全であると考えられていた。2011年には、ブロック暗号のCBCモードの取り扱いに関する脆弱性であったBEAST攻撃への対応策の一つとして、ストリーム暗号であるためその影響を受けないRC4に切り替えることが推奨されていた\[5\]。しかし、2013年にTLS/SSLでのRC4への効果的な攻撃が報告され、BEASTへの対応としてRC4を用いることは好ましくないとされた\[6\]。RC4に対する攻撃は、AlFardan、Bernstein、Paterson、Poettering、Schuldtによって報告された。新たに発見されたRC4の鍵テーブルにおける統計的な偏り\[7\]を利用し、平文の一部を回復可能であるというものである\[8\]\[9\]。この攻撃では、13 × 2<sup>20</sup>の暗号文を用いることで128ビットのRC4が解読可能であることが示され、2013年の[USENIX](../Page/USENIX.md "wikilink")セキュリティシンポジウムにおいて「実現可能」と評された\[10\]\[11\]。

## 関連項目

  - [ストリーム暗号](https://ja.wikipedia.org/wiki/ストリーム暗号 "wikilink")
  - [暗号理論](../Page/暗号理論.md "wikilink")

## 脚注

<references/>

## 外部リンク

  - [IETF draft - A Stream Cipher Encryption Algorithm "Arcfour"](https://tools.ietf.org/html/draft-kaukonen-cipher-arcfour-03)
  - RFC 4345 - Improved Arcfour Modes for the Secure Shell (SSH) Transport Layer Protocol
  - RFC 6229 - Test Vectors for the Stream Cipher RC4
  - RFC 7465 - Prohibiting RC4 Cipher Suites
  - [SCAN's entry for RC4](http://www.users.zetnet.co.uk/hopwood/crypto/scan/cs.html#RC4)
  - [Attacks on RC4](http://www.wisdom.weizmann.ac.il/~itsik/RC4/rc4.html)
  - [RC4 - Cryptology Pointers by Helger Lipmaa](http://research.cyber.ee/~lipmaa/crypto/link/stream/rc4.php)
  - [RSA Security Response to Weaknesses in Key Scheduling Algorithm of RC4](http://www.rsasecurity.com/rsalabs/node.asp?id=2009)

<!-- end list -->

1.
2.
3.
4.
5.  [security – Safest ciphers to use with the BEAST? (TLS 1.0 exploit) I've read that RC4 is immune – Server Fault](http://serverfault.com/questions/315042/)
6.
7.
8.
9.
10.
11.
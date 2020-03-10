> この記事は[HMAC](https://ja.wikipedia.org/wiki/HMAC)から翻訳されています。


**HMAC** (**H**ash-based **M**essage **A**uthentication **C**ode) とは、[メッセージ認証符号](https://ja.wikipedia.org/wiki/メッセージ認証符号 "wikilink") (MAC; Message Authentication Code) の一つであり、[秘密鍵](https://ja.wikipedia.org/wiki/秘密鍵 "wikilink")とメッセージ（データ）と[ハッシュ関数](../Page/ハッシュ関数.md "wikilink")をもとに計算される。

1997年2月、IBMのKrawczykらにより提唱され、RFC 2104として公開されている。 また、FIPS PUB 198にも採用されている。

## 概要

MACは認証及び改竄検出技術の核となるアルゴリズムである。 MAC値の算出時にHMACアルゴリズムの中で用いられるハッシュアルゴリズムは、[MD5](../Page/MD5.md "wikilink")や[SHA-1](https://ja.wikipedia.org/wiki/SHA-1 "wikilink")など任意の繰返し型ハッシュ関数が適用可能であり、それぞれHMAC-MD5、HMAC-SHA1などと呼ばれる。

HMACは次のように定義される：

  -
    \(\mathit{HMAC}_K(m) = h \left( (K \oplus opad) \;||\; h((K \oplus ipad) \;||\; m) \right).\)

ここで、"h" は繰返し型ハッシュ関数、"K" は秘密鍵で、もしハッシュ関数 "h" のブロック長より短い場合は "K" を先頭に寄せて末尾に0x00でパディングを行う。"m" は認証対象メッセージである。"||" は連結、"\(\oplus\)"は排他的論理和を表す。2つの定数 "ipad" と "opad" は、各々ハッシュ関数 "h" のブロック長と同じ長さの埋め草で、"ipad" = 0x363636...3636 と "opad" = 0x5c5c5c...5c5c と定義する。つまり、ハッシュ関数 "h" のブロック長が 512ビット（64オクテット\[1\]）の場合ならば、埋め草の "ipad" と "opad" は、それぞれ64オクテットの 0x36 や 0x5c の連続である。

HMACにより算出された値はMAC値と呼ばれる。

## 脚注

<references />

## 参考文献

  - Mihir Bellare, Ran Canetti and Hugo Krawczyk, "Keying Hash Functions for Message Authentication", CRYPTO'96, pp1–15, 1996.

## 外部リンク

  - RFC 2104
      - [HMAC： メッセージ認証のための鍵付ハッシング (HMAC: Keyed-Hashing for Message Authentication)](http://www.ipa.go.jp/security/rfc/RFC2104JA.html) — [IPAによる日本語訳](../Page/情報処理推進機構.md "wikilink")

[Category:暗号](https://ja.wikipedia.org/wiki/Category:暗号 "wikilink") [Category:誤り検出訂正](https://ja.wikipedia.org/wiki/Category:誤り検出訂正 "wikilink") [Category:メッセージ認証コード](https://ja.wikipedia.org/wiki/Category:メッセージ認証コード "wikilink") [Category:RFC](https://ja.wikipedia.org/wiki/Category:RFC "wikilink")

1.  RFC 2104では、octetでなく、byteと書いてある。
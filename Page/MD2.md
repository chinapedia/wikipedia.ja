> この記事は[MD2](https://ja.wikipedia.org/wiki/MD2)から翻訳されています。


**MD2**（Message Digest Algorithm 2）とは、[1989年](../Page/1989年.md "wikilink")に[ロナルド・リベスト](../Page/ロナルド・リベスト.md "wikilink")が開発した[暗号学的ハッシュ関数](https://ja.wikipedia.org/wiki/暗号学的ハッシュ関数 "wikilink")\[1\]\[2\]。このアルゴリズムは[8ビット](../Page/8ビット.md "wikilink")コンピュータ向けに最適化されている。MD2 の仕様は [RFC 1319](../Page/Request_for_Comments.md "wikilink") で示されている。MD2は既に安全でないことが示されているが、 2014年現在も[RSA暗号](../Page/RSA暗号.md "wikilink")と共に[公開鍵証明書](../Page/公開鍵証明書.md "wikilink")を発行する[公開鍵基盤](https://ja.wikipedia.org/wiki/公開鍵基盤 "wikilink")として使われ続けている。

## 概要

任意のメッセージのハッシュ値が、コンピュータ上のブロック長（128ビット/16[バイト](../Page/バイト_\(情報\).md "wikilink")）の倍数になるようパディングされ、16バイトの[チェックサム](../Page/チェックサム.md "wikilink")を追加した状態で計算される。実際の計算では、48バイトの補助ブロックと[円周率](https://ja.wikipedia.org/wiki/円周率 "wikilink")の小数部分の数列から間接的に生成された256バイトの[Sテーブルを使用する](../Page/Sボックス.md "wikilink")。そのアルゴリズムは、処理される16個の入力バイトそれぞれについて、補助ブロックの各バイトを18回並べ替えるループを使用する。パディングされたメッセージの全ブロックの処理が終わると、補助ブロックの最初の不完全ブロックがそのメッセージのハッシュ値になる。

Sテーブルの値を16進数で表すと次のようになる。

`0x29, 0x2E, 0x43, 0xC9, 0xA2, 0xD8, 0x7C, 0x01, 0x3D, 0x36, 0x54, 0xA1, 0xEC, 0xF0, 0x06, 0x13, `
`0x62, 0xA7, 0x05, 0xF3, 0xC0, 0xC7, 0x73, 0x8C, 0x98, 0x93, 0x2B, 0xD9, 0xBC, 0x4C, 0x82, 0xCA, `
`0x1E, 0x9B, 0x57, 0x3C, 0xFD, 0xD4, 0xE0, 0x16, 0x67, 0x42, 0x6F, 0x18, 0x8A, 0x17, 0xE5, 0x12, `
`0xBE, 0x4E, 0xC4, 0xD6, 0xDA, 0x9E, 0xDE, 0x49, 0xA0, 0xFB, 0xF5, 0x8E, 0xBB, 0x2F, 0xEE, 0x7A, `
`0xA9, 0x68, 0x79, 0x91, 0x15, 0xB2, 0x07, 0x3F, 0x94, 0xC2, 0x10, 0x89, 0x0B, 0x22, 0x5F, 0x21,`
`0x80, 0x7F, 0x5D, 0x9A, 0x5A, 0x90, 0x32, 0x27, 0x35, 0x3E, 0xCC, 0xE7, 0xBF, 0xF7, 0x97, 0x03, `
`0xFF, 0x19, 0x30, 0xB3, 0x48, 0xA5, 0xB5, 0xD1, 0xD7, 0x5E, 0x92, 0x2A, 0xAC, 0x56, 0xAA, 0xC6, `
`0x4F, 0xB8, 0x38, 0xD2, 0x96, 0xA4, 0x7D, 0xB6, 0x76, 0xFC, 0x6B, 0xE2, 0x9C, 0x74, 0x04, 0xF1, `
`0x45, 0x9D, 0x70, 0x59, 0x64, 0x71, 0x87, 0x20, 0x86, 0x5B, 0xCF, 0x65, 0xE6, 0x2D, 0xA8, 0x02, `
`0x1B, 0x60, 0x25, 0xAD, 0xAE, 0xB0, 0xB9, 0xF6, 0x1C, 0x46, 0x61, 0x69, 0x34, 0x40, 0x7E, 0x0F, `
`0x55, 0x47, 0xA3, 0x23, 0xDD, 0x51, 0xAF, 0x3A, 0xC3, 0x5C, 0xF9, 0xCE, 0xBA, 0xC5, 0xEA, 0x26, `
`0x2C, 0x53, 0x0D, 0x6E, 0x85, 0x28, 0x84, 0x09, 0xD3, 0xDF, 0xCD, 0xF4, 0x41, 0x81, 0x4D, 0x52, `
`0x6A, 0xDC, 0x37, 0xC8, 0x6C, 0xC1, 0xAB, 0xFA, 0x24, 0xE1, 0x7B, 0x08, 0x0C, 0xBD, 0xB1, 0x4A, `
`0x78, 0x88, 0x95, 0x8B, 0xE3, 0x63, 0xE8, 0x6D, 0xE9, 0xCB, 0xD5, 0xFE, 0x3B, 0x00, 0x1D, 0x39, `
`0xF2, 0xEF, 0xB7, 0x0E, 0x66, 0x58, 0xD0, 0xE4, 0xA6, 0x77, 0x72, 0xF8, 0xEB, 0x75, 0x4B, 0x0A, `
`0x31, 0x44, 0x50, 0xB4, 0x8F, 0xED, 0x1F, 0x1A, 0xDB, 0x99, 0x8D, 0x33, 0x9F, 0x11, 0x83, 0x14`

## MD2 ハッシュ値

128ビット（16バイト）の MD2 のハッシュ値（これを *message digests* とも呼ぶ）は、通常32桁の[16進数で表される](https://ja.wikipedia.org/wiki/十六進記数法 "wikilink")。以下に 43バイトの [ASCII](https://ja.wikipedia.org/wiki/ASCII "wikilink")を入力として MD2 のハッシュ値を得る様子を示す。

` MD2("The quick brown fox jumps over the lazy dog")`
`  = 03d85a0d629d2c442e987525319fc471`

メッセージに微妙な修正を施した場合でも、完全に異なるハッシュ値が生成される。ここでは、`dog` が `cog` に修正されている。

` MD2("The quick brown fox jumps over the lazy cog")`
`  = 6b890c9292668cdbbfda00a4ebf31f05`

長さ 0 のメッセージのハッシュ値は次のようになる。

` MD2("") = 8350e5a3e24c153df2275c9f80692773`

## セキュリティ

Rogier と Chauvaud (1997年) は MD2 の圧縮関数でのコリジョンを見出した。ただし、彼らも MD2 全体への攻撃には成功しなかった。

[2004年](../Page/2004年.md "wikilink")、2<sup>104</sup> の圧縮関数評価と等価な[時間複雑性の](https://ja.wikipedia.org/wiki/計算複雑性理論 "wikilink")[原像攻撃](https://ja.wikipedia.org/wiki/原像攻撃 "wikilink")で MD2 の脆弱性が明らかとなった（Muller、2004年）。「MD2 はもはや安全な単方向のハッシュ関数とは言えない」

2008年、2<sup>73</sup> の圧縮関数評価と等価な[時間複雑性および](https://ja.wikipedia.org/wiki/計算複雑性理論 "wikilink") 2<sup>73</sup> のメッセージブロックのメモリ容量による[原像攻撃](https://ja.wikipedia.org/wiki/原像攻撃 "wikilink")が示された\[3\]。

2009年、2<sup>63.3</sup> の圧縮関数評価と等価な[時間複雑性および](https://ja.wikipedia.org/wiki/計算複雑性理論 "wikilink") 2<sup>52</sup> のハッシュ値のメモリ容量による[衝突攻撃](https://ja.wikipedia.org/wiki/衝突攻撃 "wikilink")で MD2 の脆弱性が示された。これは2<sup>65.5</sup>の圧縮関数評価が必要と見積もられている[誕生日攻撃](https://ja.wikipedia.org/wiki/誕生日攻撃 "wikilink")よりも若干よい値である\[4\]。

2009年、[OpenSSL](https://ja.wikipedia.org/wiki/OpenSSL "wikilink")、[GnuTLS](https://ja.wikipedia.org/wiki/GnuTLS "wikilink")、[Network Security Services](https://ja.wikipedia.org/wiki/Network_Security_Services "wikilink") においてMD2を使用不可にするセキュリティアップデートが発行された\[5\]。

## 参考文献

  - Burt Kaliski, RFC 1319 - MD2 Message Digest Algorithm, April 1992.
  - N. Rogier, Pascal Chauvaud, The compression function of MD2 is not collision free, *Selected Areas in Cryptography - SAC'95 Ottawa*, Canada, May 18–19, 1995 (workshop record).
  - N. Rogier, Pascal Chauvaud, MD2 is not Secure without the Checksum Byte, *Designs, Codes and Cryptography*, 12(3), pp245–251, 1997.
  - Frédéric Muller, The MD2 Hash Function is Not One-Way, ASIACRYPT 2004, pp214–229.
  - Lars R. Knudsen and John Erik Mathiassen, Preimage and Collision Attacks on MD2. FSE 2005.

## 脚注

## 関連項目

  - [ハッシュ関数](../Page/ハッシュ関数.md "wikilink")
  - [MD4](../Page/MD4.md "wikilink")
  - [MD5](../Page/MD5.md "wikilink")
  - [Secure Hash Algorithm](../Page/Secure_Hash_Algorithm.md "wikilink")

## 外部リンク

  - RFC 1319, The MD2 Message-Digest Algorithm
  - RFC 6149, MD2 to Historic Status
  - [Online MD2 Calculator over HTTPS](http://quickhash.com/md2)
  - [Serversniff.net](http://serversniff.net/hash.php?algo=md2) 文字列の MD2 などのハッシュ値を計算するオンラインツール
  - テキスト、16進、2進、Base64などの相互変換と同時にMD2その他のハッシュ値を計算するオンラインツール [1](http://www.paulschou.com/tools/xlate/)

[Category:ハッシュ関数](https://ja.wikipedia.org/wiki/Category:ハッシュ関数 "wikilink") [Category:RFC](https://ja.wikipedia.org/wiki/Category:RFC "wikilink")

1.
2.
3.
4.  <http://www.springerlink.com/content/qn746388035614r1/>
5.  [CVE-2009-2409](http://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2009-2409)
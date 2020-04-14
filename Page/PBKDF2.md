> この記事は[PBKDF2](https://ja.wikipedia.org/wiki/PBKDF2)から翻訳されています。


**PBKDF2** (**Password-Based Key Derivation Function 2**) は、[鍵導出関数](https://ja.wikipedia.org/wiki/鍵導出関数 "wikilink")である。計算コストを変動させることが可能であり、[暗号](../Page/暗号.md "wikilink")化する際に、[総当たり攻撃](../Page/総当たり攻撃.md "wikilink")に対する[脆弱性](../Page/脆弱性.md "wikilink")を軽減することを目的として使用される。

PBKDF2は、導出鍵が160[ビット](../Page/ビット.md "wikilink")以下に制限されるPBKDF1に続いて\[1\]、[PKCS](../Page/PKCS.md "wikilink") \#5 v2.0 ([RSA](../Page/RSAセキュリティ.md "wikilink"))、RFC2898 ([IETF](https://ja.wikipedia.org/wiki/IETF "wikilink")) として規定された。2017年に公開された[RFC](../Page/Request_for_Comments.md "wikilink") 8018 (PKCS \#5 v2.1)は、パスワードのハッシュ化には、PBKDF2を利用することを推奨している\[2\]。

## 目的 

PBKDF2は、[HMAC](../Page/HMAC.md "wikilink")などの[疑似乱数](https://ja.wikipedia.org/wiki/疑似乱数 "wikilink")関数や、[ソルトを付加した](https://ja.wikipedia.org/wiki/ソルト_\(暗号\) "wikilink")[パスワード](../Page/パスワード.md "wikilink")やパスフレーズを用いる。また、鍵導出処理を何度も繰り返して、前回の処理で導出した鍵を次回の処理のパスワードとして用いることで、導出鍵を解読困難にする。この繰り返し処理は、ストレッチングと呼ばれる。

2000年に公開されたPKCS \#5 v2.0におけるストレッチングの推奨回数は、最低1000回であった。しかしながら、[CPU](../Page/CPU.md "wikilink")処理速度の向上に伴って、ストレッチングの推奨回数も増加しており、2005年に公開されたRFC 4120での推奨回数は、4096回である\[3\]。[Apple](https://ja.wikipedia.org/wiki/Apple "wikilink")の[iOS](https://ja.wikipedia.org/wiki/iOS_\(アップル\) "wikilink") 3では2000回、iOS 4では10,000回のストレッチングを行っており\[4\]、[LastPass](https://ja.wikipedia.org/wiki/LastPass "wikilink")は、2011年時点で、[サーバ](../Page/サーバ.md "wikilink")側での100,000回のストレッチングに加えて、[クライアント側での](../Page/クライアント_\(コンピュータ\).md "wikilink")5000回のストレッチングも行っている\[5\]。

[Pbkdf2_nist.png](https://ja.wikipedia.org/wiki/File:Pbkdf2_nist.png "fig:Pbkdf2_nist.png")

ソルトをパスワードに付加することで、攻撃者は複数のパスワードを一度に試行できなくなるため、ハッシュ値の事前計算（[レインボーテーブル](../Page/レインボーテーブル.md "wikilink")）の効果を下げることができる。PKCS \#5では、ソルトの長さを最低でも64ビットにすることを推奨しており\[6\]、[アメリカ国立標準技術研究所](../Page/アメリカ国立標準技術研究所.md "wikilink")は、128ビットのソルトを推奨している\[7\]。

## 鍵導出の処理 

鍵導出関数PBKDF2は、5つの引数を持つ\[8\]。

`DK = PBKDF2(PRF, Password, Salt, c, dkLen)`

ここで、

  - *PRF* は、出力値の長さが*hLen* であり、2つの引数を持つ疑似乱数関数 (HMACなど)
  - *Password* は、鍵導出のためのマスターパスワード
  - *Salt* は、ソルト
  - *c* は、ストレッチング回数
  - *dkLen* は、導出鍵のビット長
  - *DK* は、導出鍵

である。

*hLen* ビットのブロックT<sub>i</sub>は、次式で求められる。ただし、`+`は、文字列連結を意味する。

`DK = T`<sub>`1`</sub>` + T`<sub>`2`</sub>` + ... + T`<sub>`dklen/hlen`</sub>
`T`<sub>`i`</sub>` = F(Password, Salt, c, i)`

関数*F* は、PRFの*c* 回の[XOR](https://ja.wikipedia.org/wiki/XOR "wikilink") (^) の繰り返しである。

`F(Password, Salt, c, i) = U`<sub>`1`</sub>` ^ U`<sub>`2`</sub>` ^ ... ^ U`<sub>`c`</sub>

最初のPRFは、*Password* を鍵とし、ビッグエンディアンの32ビット整数*i* と連結した*Salt* を入力値とする。ただし、*i* は1始まりとする。次回以降は、*Password* を鍵とし、前回のPRFの出力値を入力値とする。

`U`<sub>`1`</sub>` = PRF(Password, Salt + INT_32_BE(i))`
`U`<sub>`2`</sub>` = PRF(Password, U`<sub>`1`</sub>`)`
`...`
`U`<sub>`c`</sub>` = PRF(Password, U`<sub>`c-1`</sub>`)`

例えば、[WPA2](https://ja.wikipedia.org/wiki/WPA2 "wikilink")では、

` DK = PBKDF2(HMAC−SHA1, passphrase, ssid, 4096, 256)`

を用いている。

なお、PBKDF1は、PBKDF2より単純な鍵導出関数である。最初の*U* (PBKDF1では*T*とされる) は、`PRF(Password + Salt)`によって生成され、次回以降は、単に`PRF(U`<sub>`previous`</sub>`)`である。導出鍵は、最終的に算出されたハッシュ値の最初の*dkLen* ビットとする。このため、PBKDF1の導出鍵の長さは、*hLen* ビット以下に制限される\[9\]。

## HMACの衝突

PBKDF2は、HMACを疑似乱数関数として用いるとき、導出鍵が[衝突する異なるパスワードの組を容易に得ることが可能である](https://ja.wikipedia.org/wiki/衝突_\(計算機科学\) "wikilink")\[10\]。HMACの中で用いられるハッシュ関数のブロック長よりパスワードが長いとき、パスワードをハッシュ化したものをパスワードとして用いる。例えば、疑似乱数関数として、HMAC-[SHA1](https://ja.wikipedia.org/wiki/SHA1 "wikilink")を用いると、

  - **パスワード**:

は、

  - **SHA1** (16進数): `65426b585154667542717027635463617226672a`
  - **SHA1** (ASCII): `eBkXQTfuBqp'cTcar&g*`

となる。よって、PBKDF2-HMAC-SHA1は、次の2つの異なるパスワード

  - "plnlrtfpijpuhqylxbgqiiyipieyxvfsavzgxbbcfusqkozwpngsyejqlmjsytrmd"
  - "eBkXQTfuBqp'cTcar\&g\*"

から、ソルトやストレッチングに関係なく、同じ鍵を導出する。例えば、

  - **PRF**: HMAC-SHA1
  - **ソルト**: A009C1A485912C6AE630D3E744240B04
  - **ストレッチング回数**: 1,000回
  - **導出鍵の長さ**: 16バイト

とすると、2つの関数

`PBKDF2-HMAC-SHA1("plnlrtfpijpuhqylxbgqiiyipieyxvfsavzgxbbcfusqkozwpngsyejqlmjsytrmd", ...)`
`PBKDF2-HMAC-SHA1("eBkXQTfuBqp'cTcar&g*", ...) `

は、同じ導出鍵`17EB4014C8C461C300E9B61518B9A18B`を生成する。ただし、パスワードのハッシュ値を得るためには、パスワードも得る必要があるため、導出鍵の衝突は、PBKDF2やHMACの脆弱性を示唆するものではない\[11\]。

## PBKDF2の代替

PBKDF2は、ストレッチング回数を調整することで、計算時間を変動させること可能である。しかしながら、短いコード量、少ないメモリ量で実装できるため、[ASIC](../Page/ASIC.md "wikilink")や[GPUを用いた総当たり攻撃に弱い](../Page/Graphics_Processing_Unit.md "wikilink")\[12\]パスワードハッシュ関数の[bcrypt](https://ja.wikipedia.org/wiki/bcrypt "wikilink")は、計算時間は固定であるものの、計算に多くのメモリ量を必要とするため、PBKDF2より総当たり攻撃に強い。\[13\]その後に開発された鍵導出関数のscryptは、任意の大きさのメモリ量を使うことができ、ASCIやGPUによる攻撃に対する耐性が高い\[14\]。

安全なパスワードハッシュ化手法を開発することを目的として、2013年にが開催された。2015年7月20日にパスワードハッシュ関数[Argon2](https://ja.wikipedia.org/wiki/Argon2 "wikilink")の優勝が決まり、他に4つの関数Catena、Lyra2、yescryptおよびMakwaが特別賞として選ばれた\[15\]。

## 出典

## 外部リンク 

  - [RSA PKCS \#5](https://www.emc.com/collateral/white-papers/h11302-pkcs5v2-1-password-based-cryptography-standard-wp.pdf) – RSAによるPKCS \#5 v2.1.
  - RFC 2898 – PKCS \#5 v2.0の仕様書
  - RFC 6070 – HMAC-SHA1を用いたPBKDF2のテストデータ
  - [NIST Special Publication 800-132 Recommendation for Password-Based Key Derivation](http://nvlpubs.nist.gov/nistpubs/Legacy/SP/nistspecialpublication800-132.pdf)

[Category:ハッシュ関数](https://ja.wikipedia.org/wiki/Category:ハッシュ関数 "wikilink") [Category:公開鍵基盤](https://ja.wikipedia.org/wiki/Category:公開鍵基盤 "wikilink") [Category:パスワード管理](https://ja.wikipedia.org/wiki/Category:パスワード管理 "wikilink")

1.
2.
3.
4.
5.
6.
7.
8.
9.
10. <https://mathiasbynens.be/notes/pbkdf2-hmac>
11. <https://crypto.stackexchange.com/questions/26510/why-is-hmac-sha1-still-considered-secure>
12. 。 Colin Percival. [scrypt](http://www.tarsnap.com/scrypt.html). ["Stronger Key Derivation via Sequential Memory-Hard Functions"](http://www.tarsnap.com/scrypt/scrypt.pdf). 2009年5月、BSDCan'09にて公開.
13.
14.
15. ["Password Hashing Competition"](https://password-hashing.net)
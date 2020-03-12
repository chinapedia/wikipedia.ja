> この記事は[Secure Hash Algorithm](https://ja.wikipedia.org/wiki/Secure_Hash_Algorithm)から翻訳されています。


**Secure Hash Algorithm**（セキュアハッシュアルゴリズム）、略称**SHA**は、一群の関連した[暗号学的ハッシュ関数](https://ja.wikipedia.org/wiki/暗号学的ハッシュ関数 "wikilink")であり、[アメリカ国立標準技術研究所](../Page/アメリカ国立標準技術研究所.md "wikilink")（NIST）によって標準のハッシュ関数**Secure Hash Standard**に指定されている。

## 概要

（2017年現在）SHA-0、[SHA-1](https://ja.wikipedia.org/wiki/SHA-1 "wikilink")、[SHA-2](https://ja.wikipedia.org/wiki/SHA-2 "wikilink")、[SHA-3](../Page/SHA-3.md "wikilink")の4種類（ないし、SHA-0はSHA-1に含めて3種類）に大別される。SHA-2までは[MD5](../Page/MD5.md "wikilink")などと同じ Merkle–Damgård construction（[:en:Merkle–Damgård construction](https://ja.wikipedia.org/wiki/:en:Merkle–Damgård_construction "wikilink")）のバリエーションと言える構造だが、SHA-3 は全く別の構造となっている。SHA-2 以降はハッシュサイズを大きくしたバリエーションが用意されており、SHA-2には、SHA-224、SHA-256、SHA-384、SHA-512、SHA-512/224、SHA-512/256 があり、SHA-3には、SHA3-224、SHA3-256、SHA3-384、SHA3-512、SHAKE128、SHAKE256 がある。

SHA-1、SHA-256、SHA-384、SHA-512は2002年8月の[FIPS](https://ja.wikipedia.org/wiki/Federal_Information_Processing_Standards "wikilink") Publication 180-2の初版に含まれている。SHA-224はChange Notice 1として、2004年2月に同規格に追加された。SHA-512/224、SHA-512/256は2012年のFIPS 180-4で追加された。

SHA-3については、2015年8月にNISTがSecure Hash Standard (SHS) とは独立した標準としてSHA-3を含むFIPS 202を発行した\[1\]。

SHA-0およびSHA-1が最も古く、（さらにそれ以前の[MD5](../Page/MD5.md "wikilink")を置き換えて）以前は[TLS](../Page/Transport_Layer_Security.md "wikilink")、[SSL](../Page/Transport_Layer_Security.md "wikilink")、[PGP](../Page/Pretty_Good_Privacy.md "wikilink")、[SSH](../Page/Secure_Shell.md "wikilink")、[S/MIME](https://ja.wikipedia.org/wiki/S/MIME "wikilink")、[IPSec](https://ja.wikipedia.org/wiki/IPSec "wikilink")など、さまざまな[アプリケーションソフトウェア](../Page/アプリケーションソフトウェア.md "wikilink")や[プロトコル](../Page/プロトコル.md "wikilink")に採用されていたが、2004年のCRYPTO2004におけるXiaoyun Wang（王小雲）らの発表以降、広く知られるようになった研究の進展により、2017年2月には実際に衝突攻撃の成功が示されている。よって、2017年初頭の段階でこれらを[情報セキュリティ](https://ja.wikipedia.org/wiki/情報セキュリティ "wikilink")の目的で使用しているのは無謀である。

SHA-2までは[国家安全保障局](../Page/アメリカ国家安全保障局.md "wikilink") (NSA) によって開発された。

1993年に発表された最初のものは、公式には単にSHAと呼ばれていた。しかし現在は、その後のものと区別するためにもっぱらSHA-0と呼ばれている。1995年に弱点を修正したSHA-1が発表された。

SHA-2は、Merkle–Damgård construction を採用している点は同じだが、SHA-1 とは異なり、2016年末の時点で有望な攻撃法は発表されていない。2001年に発行されたのは SHA-224、SHA-256、SHA-384、SHA-512という4種類のバリエーションで、2012年には SHA-512/224、SHA-512/256 も加えられた。

SHA-3は、これまでのものとは異なり[アメリカ国立標準技術研究所](../Page/アメリカ国立標準技術研究所.md "wikilink") (NIST) による公募によるもので、Keccakが新しいハッシュ関数として選出された。前述のCRYPTO2004によってMerkle–Damgård constructionそのものが不安視されたことから別の構造を採用しているが、前述のようにSHA-2への攻撃は進展しなかったため、SHA-3の普及はほとんど進んでいない。

[MD4](../Page/MD4.md "wikilink")とMD5は、前述のCRYPTO2004によって衝突の実例が示された。SHA-0はそれらより強いことが期待されていたハッシュ関数であったが、同様に衝突の実例が示された。SHA-1は修正版であるため、それらよりは強かったものの有効な攻撃法の研究が2004年から発展し、2017年には衝突の実例が示された。

### SHA-0

SHA-0はSHAシリーズの最初の規格である。発表から間もなくして欠点が発見された。ハッシュ値の長さは、160[ビット](../Page/ビット.md "wikilink")。

### SHA-1

SHA-0の欠点を修正した。SHA-1のハッシュ値の長さは、SHA-0と同じく160ビット。

2017年に、衝突攻撃の成功と実例が報告された。

### SHA-2

SHA-1を改良し、また、出力されるハッシュ値の長さも長くしたものがSHA-2である。

SHA-256、SHA-512は、それぞれ32ビット、64ビットの[ワード](../Page/ワード.md "wikilink")サイズを持ち、出力されるハッシュ値の長さは256ビット、512ビットである。SHA-224、SHA-384はそれぞれSHA-256、SHA-512を切り詰めたものであり、ワードサイズはそれぞれ32ビット、64ビット、出力長はそれぞれ224ビット、384ビットである。SHA-512/224、SHA-512/256はSHA-512を切り詰めたものであり、ワードサイズは64ビット、出力長はそれぞれ224ビット、256ビットである。

### SHA-3

SHA-3としてKeccakが、[アメリカ国立標準技術研究所](../Page/アメリカ国立標準技術研究所.md "wikilink") (NIST) による公募において、2012年10月2日に選出された\[2\]。2015年8月に、正式版が発行された。これまでのSHAの Merkle–Damgård construction（[:en:Merkle–Damgård construction](https://ja.wikipedia.org/wiki/:en:Merkle–Damgård_construction "wikilink")）とは異なり、ハッシュ値よりも大きな内部状態を持ち、ハッシュ値はその内部状態から「絞り出される」という、「スポンジ構造」を採用している。

SHAシリーズでは初めて開発に[国家安全保障局](../Page/アメリカ国家安全保障局.md "wikilink") (NSA) が関わっていない。

SHA-3は64ビットの[ワード](../Page/ワード.md "wikilink")サイズを持ち、出力されるハッシュ値の長さは224ビット、256ビット、384ビット、512ビットの4種類、もしくは可変長（SHAKE128、SHAKE256 の2種類が選択可能）である。

## 比較

## 関連項目

  - [MD2](../Page/MD2.md "wikilink")
  - [MD4](../Page/MD4.md "wikilink")
  - [MD5](../Page/MD5.md "wikilink")
  - [HMAC](../Page/HMAC.md "wikilink")

## 脚注

<references />

## 外部リンク

  - [FIPS PUB 180-1, *SECURE HASH STANDARD*](http://www.itl.nist.gov/fipspubs/fip180-1.htm)
  - (PDF) [FIPS PUB 180-2, *SECURE HASH STANDARD*](http://csrc.nist.gov/publications/fips/fips180-2/fips180-2.pdf)
  - [SHA-0、MD5、 MD4にコリジョン発見、reduced SHA-1も](http://slashdot.jp/security/article.pl?sid=04/08/18/0257220) [スラッシュドット](../Page/スラッシュドット.md "wikilink")ジャパン
  - [オンラインでSHA256ハッシュ関数ツール](http://www.convertstring.com/ja/Hash/SHA256)
  - [オンラインでSHA512ハッシュ関数ツール](http://www.convertstring.com/ja/Hash/SHA512)
  - [SHA1, SHA-256, SHA-384, SHA-512 Online Calculator](http://www.webutils.pl/SHA1_Calculator) Calculate SHA file hashes using an on-line web form.

[Category:ハッシュ関数](https://ja.wikipedia.org/wiki/Category:ハッシュ関数 "wikilink") [Category:暗号](https://ja.wikipedia.org/wiki/Category:暗号 "wikilink")

1.
2.
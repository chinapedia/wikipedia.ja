> この記事は[SEED \(\)](https://ja.wikipedia.org/wiki/SEED_\(\))から翻訳されています。


**SEED**（シード）とは、[1998年](https://ja.wikipedia.org/wiki/1998年 "wikilink")に韓国情報保護振興院 (KISA) で開発されたブロック暗号である。

## 概要

SEEDは、[Feistel構造](../Page/Feistel構造.md "wikilink")を採用したブロック長128[ビット](../Page/ビット.md "wikilink")、処理の繰り返し段数16段のブロック暗号で、[鍵長](https://ja.wikipedia.org/wiki/鍵長 "wikilink")としては128ビットしか選択できない。

日本の暗号評価プロジェクト[CRYPTREC](../Page/CRYPTREC.md "wikilink")より総当たり以外に有効な解読方法がないと評価されつつも、PCでの処理速度についてはやや遅いグループにあると評価されている\[1\]。

一方、欧州の暗号評価プロジェクト[NESSIE](../Page/NESSIE.md "wikilink")からはソフトウェアでの実装にて[Camellia](../Page/Camellia.md "wikilink")よりも高速に動くプラットホームがあるという評価もされている\[2\]。

SEEDは韓国情報通信標準規格 (KICS)、[S/MIME](https://ja.wikipedia.org/wiki/S/MIME "wikilink") (RFC 4010)、[TLS/SSL](../Page/Transport_Layer_Security.md "wikilink") (RFC 4162)、[IPsec](https://ja.wikipedia.org/wiki/IPsec "wikilink") (RFC 4196)、[ISO/IEC 18033](https://ja.wikipedia.org/wiki/ISO/IEC_18033 "wikilink") ([ISO/IEC 18033-3:2010](http://www.iso.org/iso/home/store/catalogue_ics/catalogue_detail_ics.htm?csnumber=54531)) の標準暗号として採用されている。

なお、SEEDは韓国国内では広く使われているが、それ以外の国では滅多に使われない。SEEDが韓国国内でしか使われないのは、40ビット SSLの安全性が危惧されていたおりに、128ビットSSLの仕様決定を待たずにKISAがSEEDを標準と定めたからである。しかし、この標準化は韓国国内で用いられるウェブブラウザにしか影響が無く、主要なSSLライブラリやウェブブラウザはSEEDをサポートしていない。このため、韓国国内のユーザーはInternet Explorer上でActiveXコンポーネントを使うことでしか安全にウェブサイトにアクセスすることができない\[3\]。

[NSSがSEEDをサポートし](https://ja.wikipedia.org/wiki/Network_Security_Services "wikilink")\[4\]、[Mozilla Firefoxのバージョン](../Page/Mozilla_Firefox.md "wikilink")3.5.4以降において[TLS/SSLの暗号方式としてSEEDをサポートしている](../Page/Transport_Layer_Security.md "wikilink")\[5\]。しかし、依然として上述の韓国におけるSEEDを用いたActiveXへの依存が解消されないこと、他のブラウザがSEEDをサポートしないことから、Firefox 27以降においてSEEDのサポートは既定で無効とされた\[6\]\[7\]。これはFirefoxなどのソフトウェアレベルでのものであり、ライブラリであるNSSは引き続きSEEDをサポートする。

## 脚注

<references />

## 関連項目

  - [ブロック暗号](https://ja.wikipedia.org/wiki/ブロック暗号 "wikilink")
  - [共通鍵暗号](../Page/共通鍵暗号.md "wikilink")
  - [暗号理論](../Page/暗号理論.md "wikilink")

## 外部リンク

  - [SEED - KISA](http://seed.kisa.or.kr/iwt/ko/sup/EgovSeedInfo.do) (公式サイト、英語)
  - [SEED official specification document](http://seed.kisa.or.kr/html/egovframework/iwt/ds/ko/ref/%5B2%5D_SEED+128_Specification_english_M.pdf) (英語)
  - RFC 4269: The SEED encryption algorithm (obsoletes RFC 4009)
  - RFC 4010: Use of the SEED Encryption Algorithm in Cryptographic Message Syntax (CMS)
  - RFC 4162: Addition of SEED Cipher Suites to Transport Layer Security (TLS)
  - RFC 4196: The SEED Cipher Algorithm and Its Use with IPsec
  - [ISO/IEC 18033-3:2010](http://www.iso.org/iso/home/store/catalogue_ics/catalogue_detail_ics.htm?csnumber=54531) Information technology -- Security techniques -- Encryption algorithms -- Part 3: Block ciphers
  - [CRYPTREC暗号技術評価結果 ～平成13年度で評価を終了した暗号技術～](http://www.ipa.go.jp/security/enc/CRYPTREC/fy14/cryptrec20021128_endedeval.html)

[Category:RFC](https://ja.wikipedia.org/wiki/Category:RFC "wikilink")

1.  <http://www.ipa.go.jp/security/fy13/report/cryptrec/c01.pdf>
2.  <http://www.kisa.or.kr/seed/data/Document_pdf/SEED_Justification_for_Inclusion_of_SEED_in_ISOIEC18033-3.pdf>
3.
4.
5.
6.
7.
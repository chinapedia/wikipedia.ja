> この記事は[Camellia](https://ja.wikipedia.org/wiki/Camellia)から翻訳されています。


**Camellia**（カメリア）とは、[2000年](../Page/2000年.md "wikilink")に[NTTと](https://ja.wikipedia.org/wiki/日本電信電話 "wikilink")[三菱電機](../Page/三菱電機.md "wikilink")により共同開発された[ブロック暗号](https://ja.wikipedia.org/wiki/ブロック暗号 "wikilink")である。名称の由来は植物の[ツバキ](../Page/ツバキ.md "wikilink")（[ツバキ属](https://ja.wikipedia.org/wiki/ツバキ属 "wikilink")：*Camellia*）。

Camelliaは[Feistel構造](../Page/Feistel構造.md "wikilink")を採用したブロック長128[ビット](../Page/ビット.md "wikilink")の[ブロック暗号](https://ja.wikipedia.org/wiki/ブロック暗号 "wikilink")で、[鍵長](https://ja.wikipedia.org/wiki/鍵長 "wikilink")として[AESと同じ](../Page/Advanced_Encryption_Standard.md "wikilink")128ビット、192ビット、256ビットの3つを選択できる。また、CamelliaはAESと同等の安全性を保ちつつ[ハードウェア](../Page/ハードウェア.md "wikilink")での低消費電力で高速な[暗号化](https://ja.wikipedia.org/wiki/暗号化 "wikilink")・[復号](https://ja.wikipedia.org/wiki/復号 "wikilink")に優れている。

## 構造

Camelliaの入出力[インタフェース](https://ja.wikipedia.org/wiki/インタフェース "wikilink")は[AES互換で](../Page/Advanced_Encryption_Standard.md "wikilink")、ブロック長は128ビット固定、鍵長は128 / 192 / 256ビットの3つを選択できる。

全体構造は、AESでは[SPN構造](https://ja.wikipedia.org/wiki/SPN構造 "wikilink")が採用されたのと違い、[DESと同じ](../Page/Data_Encryption_Standard.md "wikilink")[Feistel構造](../Page/Feistel構造.md "wikilink")を採用している。ラウンド段数は、鍵長が128ビットのときは18段、192ビット・256ビットのときは24段で、6段毎に「副変換部」と呼ばれる全単射関数FLとFL-1が挿入されている。また、最初と最後にホワイトニング（拡大鍵との排他的論理和）が設けられている。

ラウンド関数はバイト（8ビット）を単位とした処理になっていて、拡大鍵との[排他的論理和](../Page/排他的論理和.md "wikilink")の後、8ビット入力-8ビット出力の[Sボックス](../Page/Sボックス.md "wikilink")（4種類ある）と、[FEAL](https://ja.wikipedia.org/wiki/FEAL "wikilink")にも似た阿弥陀籤型のP関数によって構成される。Sボックスは4種類あるが、テーブル1つと、入出力のビットシフト等の組合せで実装することもできる。

鍵スケジューラは、ラウンド関数2段で、鍵を"暗号化"して中間鍵を生成し、中間鍵の一部分を取り出すことで拡大鍵を作り出す。具体的には中間鍵をラウンド毎に定義された分だけシフトして、右64ビット（または左64ビット）を取り出す。CamelliaはFeistel構造を採用して、暗号化と復号の違いはラウンド関数等で使用される拡大鍵の順番のみになるように設計されている。そこで鍵スケジューラは、拡大鍵を1番目から順番に求めることも、最後から逆順に求めることも、どちらも同様な手間で実現できるように設計されている。

## 安全性

Camelliaは解読可能なラウンド数と最低限安全性を保てるラウンド数を元にした指標である[セキュリティーマージン](https://ja.wikipedia.org/wiki/セキュリティーマージン "wikilink")にて[AESを上回る](../Page/Advanced_Encryption_Standard.md "wikilink")1.8～2.0を確保している\[1\]。これに加え、Camelliaは[CRYPTREC](../Page/CRYPTREC.md "wikilink")および[NESSIE](../Page/NESSIE.md "wikilink")においてAESと同等の安全性と効率を兼ね備えているという評価もされている。

## 性能

開発者や第三者による実装報告によると、パソコンで使用されている汎用[CPU](../Page/CPU.md "wikilink")では1 [Gbps](https://ja.wikipedia.org/wiki/Gbps "wikilink")、専用[LSI](https://ja.wikipedia.org/wiki/LSI "wikilink")では2 Gbpsを超える[スループット](../Page/スループット.md "wikilink")がある。

一方、組込み機器で使用される8ビットCPUなどの処理能力が低いプロセッサでも、極端なメモリサイズ増加は生じず、[ハードウェア](../Page/ハードウェア.md "wikilink")実装した場合には、暗号化と復号や鍵スケジューラで回路を共用できるため10,000ゲート以下でも実装可能であることが確認されている。

### ソフトウェア実装

  - 組込み機器等での性能（8ビットCPU）
      - 7.19 msec (ENC) / 7.51 msec (DEC) - Z80 (5 MHz), ROM 1,268バイト, RAM 60バイト (NTT)
      - 5.68 msec (ENC) / 1.03 msec (KeyGen) - Z80 ( ), ROM 1,698バイト, RAM 63バイト (NTT)
      - 10.22 msec (ENC/DEC) - 8051 (12 MHz), ROM 990バイト, RAM 32バイト (1st NESSIE Workshop)

<!-- end list -->

  - パソコンなどでの性能（32/64ビットCPU）
      - 1,134.6 Mbps - Intel Pentium 4 (3.2 GHz), Windows XP SP2, 鍵長128ビット (Oda, et al., SCIS 2006)
      - 1,158.8 Mbps - AMD Athlon 64 3500+ Winchester (2.2 GHz), Windows XP 64-Bit Edition, ビットスライス実装, 鍵長128ビット (Fukuda, et al., SCIS 2006)

### ハードウェア実装

  - [ASIC](../Page/ASIC.md "wikilink")
      - 325.76 Mbps - IBM 0.13 μm, 6,511 unit, Loop arch, 鍵長128ビット (Satoh, et al., ISC 2003)
      - 2,154.88 Mbps - IBM 0.13 μm, 29,809 unit, Loop arch, 鍵長128ビット (Satoh, et al., ISC 2003)

<!-- end list -->

  - [FPGA](../Page/FPGA.md "wikilink")
      - 128.58 Mbps - Xilinx Virtex-E , 908 Slice, Loop arch, 鍵長128ビット (Satoh, et al., ISC 2003)
      - 393.24 Mbps - Xilinx Virtex-E , 2,833 Slice, Loop arch, 鍵長128ビット (Satoh, et al., ISC 2003)

## 歴史

  - 2000年3月10日 Camelliaの公開：NTTと三菱電機による共同開発がニュースリリースされる。
  - 2001年4月17日 Camelliaの基本特許の無償化が宣言される。
  - 2003年2月20日 日本の暗号評価プロジェクト[CRYPTREC](../Page/CRYPTREC.md "wikilink")による電子政府推奨暗号リストにCamelliaも推奨される。
  - 2003年2月27日 欧州の暗号評価プロジェクト[NESSIE](../Page/NESSIE.md "wikilink")にて、128ビットブロック暗号として、AESと共にCamelliaも選定される。
  - 2005年7月15日 国際標準規格[ISO/IEC 18033](https://ja.wikipedia.org/wiki/ISO/IEC_18033 "wikilink") Part 3の128ビットブロック暗号に、他の2つの暗号（AES、SEED）と共にCamelliaも採用される。（5月27日にニュースリリース）
  - 2005年7月20日 SSL/TLS、S/MIME、XMLなどの標準規格で、暗号方式としてCamelliaが追加される。
  - 2006年4月13日 Camelliaのオープンソースが公開される。
  - 2006年11月8日 OpenSSLにCamelliaが追加される。
  - 2007年6月7日 FreeBSD ProjectがCamelliaへの対応を発表する。
  - 2008年6月17日 [ウェブブラウザ](../Page/ウェブブラウザ.md "wikilink")として初採用した[Mozilla Firefox](../Page/Mozilla_Firefox.md "wikilink") 3がリリースされた（後に、バージョン33において既定で無効化され\[2\]、バージョン37でサポート終了\[3\]）。
  - 2013年3月1日 CRYPTRECによって改訂された電子政府推奨暗号リストに、日本初のブロック暗号として唯一Camelliaが推奨される。

## 標準化

Camelliaは、欧州の[NESSIE](../Page/NESSIE.md "wikilink")プロジェクトや日本の[CRYPTREC](../Page/CRYPTREC.md "wikilink")が作成した「電子政府推奨暗号リスト」に採用されている。

また、[TLS/SSLや](../Page/Transport_Layer_Security.md "wikilink")[IPsec](https://ja.wikipedia.org/wiki/IPsec "wikilink")をはじめとして、[IETF](https://ja.wikipedia.org/wiki/IETF "wikilink")や[ISO/IECなど多くの標準化団体に採用されている](https://ja.wikipedia.org/wiki/ISO/IEC_JTC_1 "wikilink")。主な標準化実績は以下の通りである\[4\]。

  - [CRYPTREC](../Page/CRYPTREC.md "wikilink")
  - [NESSIE](../Page/NESSIE.md "wikilink")
  - [IETF](https://ja.wikipedia.org/wiki/IETF "wikilink")
      - アルゴリズム
          - RFC 3713: A Description of the Camellia Encryption Algorithm
          - RFC 5528: Camellia Counter Mode and Camellia Counter with CBC-MAC Mode Algorithms
      - [S/MIME](https://ja.wikipedia.org/wiki/S/MIME "wikilink")
          - RFC 3657: Use of the Camellia Encryption Algorithm in Cryptographic Message Syntax (CMS)
      - [XML暗号化](https://ja.wikipedia.org/wiki/XML暗号化 "wikilink")
          - RFC 4051: Additional XML Security Uniform Resource Identifiers (URIs)
      - [TLS/SSL](../Page/Transport_Layer_Security.md "wikilink")
          - RFC 4132: Addition of Camellia Cipher Suites to Transport Layer Security (TLS)
          - RFC 5932: Camellia Cipher Suites for TLS
          - RFC 6367: Addition of the Camellia Cipher Suites to Transport Layer Security (TLS)
      - [IPsec](https://ja.wikipedia.org/wiki/IPsec "wikilink")
          - RFC 4312: The Camellia Cipher Algorithm and Its Use With IPsec
          - RFC 5529: Modes of Operation for Camellia for Use with IPsec
      - [OpenPGP](https://ja.wikipedia.org/wiki/OpenPGP "wikilink")
          - RFC 5581: The Camellia Cipher in OpenPGP
      - [RSA-KEM](../Page/RSA暗号.md "wikilink") in [CMS](https://ja.wikipedia.org/wiki/暗号メッセージ構文 "wikilink")
          - RFC 5990: Use of the RSA-KEM Key Transport Algorithm in the Cryptographic Message Syntax (CMS)
      - [PSKC](https://ja.wikipedia.org/wiki/Portable_Symmetric_Key_Container "wikilink")
          - RFC 6030: Portable Symmetric Key Container (PSKC)
      - [スマートグリッド](https://ja.wikipedia.org/wiki/スマートグリッド "wikilink")
          - RFC 6272: Internet Protocols for the Smart Grid
  - [ISO/IEC](https://ja.wikipedia.org/wiki/ISO/IEC_JTC_1 "wikilink")
      - [ISO/IEC 18033](https://ja.wikipedia.org/wiki/ISO/IEC_18033 "wikilink") ([ISO/IEC 18033-3:2010](http://www.iso.org/iso/home/store/catalogue_ics/catalogue_detail_ics.htm?csnumber=54531)) Information technology -- Security techniques -- Encryption algorithms -- Part 3: Block ciphers
  - [ITU-T](../Page/ITU-T.md "wikilink")
      - security mechanisms and procedures for [NGN](https://ja.wikipedia.org/wiki/Next_Generation_Network "wikilink") (Y.2704)
  - [RSA Laboratories](../Page/RSAセキュリティ.md "wikilink")
      - approved cipher in the [PKCS](../Page/PKCS.md "wikilink")\#11
  - [TV-Anytime Forum](https://ja.wikipedia.org/wiki/TV-Anytime_Forum "wikilink")
      - approved cipher in TV-Anytime Rights Management and Protection Information for Broadcast Applications
      - approved cipher in Bi-directional Metadata Delivery Protection

## 脚注

## 関連項目

  - [ブロック暗号](https://ja.wikipedia.org/wiki/ブロック暗号 "wikilink")
  - [共通鍵暗号](../Page/共通鍵暗号.md "wikilink")
  - [暗号理論](../Page/暗号理論.md "wikilink")

## 外部リンク

  - [Camellia公式サイト](https://info.isl.ntt.co.jp/crypt/camellia/index.html)
  - [リファレンスコード](https://embeddedsw.net/Cipher_Reference_Home.html)
  - RFC 3657 Use of the Camellia Encryption Algorithm in Cryptographic Message Syntax (CMS)
  - RFC 3713 A Description of the Camellia Encryption Algorithm
      - 日本語訳：[Camellia暗号アルゴリズムの説明](https://www.ipa.go.jp/security/rfc/RFC3713JA.html)
  - RFC 4051 Additional XML Security Uniform Resource Identifiers (URIs)
  - RFC 4132 Addition of Camellia Cipher Suites to Transport Layer Security (TLS)
  - RFC 4312 The Camellia Cipher Algorithm and Its Use With IPsec
  - RFC 5528 Camellia Counter Mode and Camellia Counter with CBC-MAC Mode Algorithms
  - RFC 5529 Modes of Operation for Camellia for Use with IPsec
  - RFC 5581 Certification of Camellia Cipher as IETF standard for OpenPGP
  - RFC 5932 Camellia Cipher Suites for TLS
  - RFC 5990 Use of the RSA-KEM Key Transport Algorithm in the Cryptographic Message Syntax (CMS)
  - RFC 6030 Portable Symmetric Key Container (PSKC)
  - RFC 6272 Internet Protocols for the Smart Grid
  - RFC 6367 Addition of the Camellia Cipher Suites to Transport Layer Security (TLS)
  - [ISO/IEC 18033-3:2010](https://www.iso.org/standard/54531.html) Information technology -- Security techniques -- Encryption algorithms -- Part 3: Block ciphers

[Category:三菱電機](https://ja.wikipedia.org/wiki/Category:三菱電機 "wikilink") [Category:RFC](https://ja.wikipedia.org/wiki/Category:RFC "wikilink")

1.  [Camelliaユーザーズガイド](http://info.isl.ntt.co.jp/crypt/camellia/dl/CamelliausersguideV1.0_070704.pdf)
2.
3.
4.
> この記事は[CRYPTREC](https://ja.wikipedia.org/wiki/CRYPTREC)から翻訳されています。


**CRYPTREC**（くりぷとれっく、Cryptography Research and Evaluation Committees) とは、電子政府推奨暗号の安全性を評価・監視し、暗号技術の適切な実装法・運用法を調査・検討するプロジェクトである\[1\]。

## 活動内容

[暗号](../Page/暗号.md "wikilink")の安全性に関する情報を提供することを目的として、[共通鍵暗号](https://ja.wikipedia.org/wiki/共通鍵暗号 "wikilink")、[公開鍵暗号](../Page/公開鍵暗号.md "wikilink")、[ハッシュ関数](../Page/ハッシュ関数.md "wikilink")、[擬似乱数](../Page/擬似乱数.md "wikilink")生成系の4種類の暗号技術に対し公募を行い、それぞれに対して国内外の[暗号研究者による評価を行い](https://ja.wikipedia.org/wiki/暗号研究者の一覧 "wikilink")、評価レポートや推奨可能な暗号のリストを作成した。リストは2013年に改訂され、既存の4種類に加え[暗号利用モード](https://ja.wikipedia.org/wiki/暗号利用モード "wikilink")、[メッセージ認証コード](https://ja.wikipedia.org/wiki/メッセージ認証コード "wikilink")、[エンティティ認証](https://ja.wikipedia.org/wiki/エンティティ認証 "wikilink")に対しても評価を行った。

プロジェクトは2000年に活動開始し、当初は「暗号技術検討会」と「暗号技術評価委員会」で構成されていた。それぞれの事務局は[総務省](../Page/総務省.md "wikilink")/[経済産業省](../Page/経済産業省.md "wikilink")、情報処理振興事業協会（IPA、現 [情報処理推進機構](https://ja.wikipedia.org/wiki/情報処理推進機構 "wikilink")）/通信・放送機構（TAO、現 NICT=[情報通信研究機構](https://ja.wikipedia.org/wiki/情報通信研究機構 "wikilink")）。2003年、2009年、2013年と組織変更が行われ、2013年11月現在では「暗号技術検討会」をトップとし、その下に「暗号技術評価委員会」と「暗号技術活用委員会」を置く体制となった。それぞれ委員長は高木剛（[東京大学](https://ja.wikipedia.org/wiki/東京大学 "wikilink")教授）及び[松本勉](https://ja.wikipedia.org/wiki/松本勉 "wikilink")（[横浜国立大学](../Page/横浜国立大学.md "wikilink")大学院教授）（2020年2月現在）。

## 電子政府における調達のために参照すべき暗号のリスト

**電子政府における調達のために参照すべき暗号のリスト**は、CRYPTRECが選定し、[総務省](../Page/総務省.md "wikilink")と[経済産業省](../Page/経済産業省.md "wikilink")が共同で所管する、[電子政府](../Page/電子政府.md "wikilink")での利用が推奨される[暗号](../Page/暗号.md "wikilink")方式のリスト。[平成](../Page/平成.md "wikilink")15年（[2003年](../Page/2003年.md "wikilink")）[2月20日](../Page/2月20日.md "wikilink")に**電子政府推奨暗号リスト**として初版が発表され、行政情報システム関係課長連絡会議において、「各府省は情報システムの構築に当たり暗号を利用する場合は、可能な限り、電子政府推奨暗号リストに掲載された暗号の利用を推進する」旨が定められた。2012年度にリストの改定が行われ、[2013年](../Page/2013年.md "wikilink")[3月1日](../Page/3月1日.md "wikilink")に**電子政府における調達のために参照すべき暗号のリスト**として3種類のリスト（改訂した電子政府推奨暗号リスト、推奨候補暗号リスト、運用監視暗号リスト）が公表された。

### 2013年の改訂

2003年に発表された初版\[2\]では、64ビットブロック暗号として（[NEC](../Page/日本電気.md "wikilink")）・（[東芝](https://ja.wikipedia.org/wiki/東芝 "wikilink")）・[MISTY1](https://ja.wikipedia.org/wiki/MISTY1 "wikilink")（[三菱電機](https://ja.wikipedia.org/wiki/三菱電機 "wikilink")）、128ビットブロック暗号として[Camellia](https://ja.wikipedia.org/wiki/Camellia "wikilink")（[NTT](https://ja.wikipedia.org/wiki/日本電信電話 "wikilink")、三菱電機）・（NEC）・（東芝）・（[富士通](../Page/富士通.md "wikilink")）、ストリーム暗号として[MUGI](https://ja.wikipedia.org/wiki/MUGI "wikilink")・（いずれも[日立製作所](../Page/日立製作所.md "wikilink")）と、日本の企業によって開発された暗号方式が多く採用されていた。

2013年の改訂\[3\]においてリストは「推奨暗号リスト」「推奨候補暗号リスト」「運用監視暗号リスト」の3つに分けられ、改訂前に採用されていた日本において開発された暗号方式は、Camelliaを除いてすべて「推奨暗号リスト」から「推奨候補暗号リスト」に移動された。また、128ビットブロック暗号として（[ソニー](../Page/ソニー.md "wikilink")）、ストリーム暗号として[KCipher-2](https://ja.wikipedia.org/wiki/KCipher-2 "wikilink")（[KDDI](../Page/KDDI.md "wikilink")）・[Enocoro-128v2](https://ja.wikipedia.org/wiki/Enocoro-128v2 "wikilink")（日立製作所）が新規に応募されていたが、推奨暗号として採用されたのはKCipher-2のみであった。このように、日本発の暗号方式の多くが推奨暗号から外されたのは、従来のリストに対して「多くの選択肢が掲載されていたため、ユーザーがどの暗号方式を選べばよいのか分かりにくい」との批判があったためである\[4\]。このため、安全性の評価だけではなく市販製品・オープンソースプロジェクト・政府系システム・国際規格での採用実績の評価も行われ、採用実績に乏しい暗号方式は「推奨暗号リスト」ではなく「推奨候補暗号リスト」への採用にとどまった\[5\]\[6\]。「推奨候補暗号リスト」に掲載された暗号方式については、採用実績が十分となった場合には「推奨暗号リスト」に掲載される可能性がある\[7\]。

また、128ビット[RC4](https://ja.wikipedia.org/wiki/RC4 "wikilink")、[SHA-1](https://ja.wikipedia.org/wiki/SHA-1 "wikilink")といった、これまで広く利用されてきたが脆弱性が指摘されている暗号方式は、「運用監視暗号リスト」に移動された。これは「推奨すべき状態ではなくなった暗号技術のうち、互換性維持のために継続利用を容認するもの」であり、これらの暗号方式を利用しているシステムは対応を迫られることとなった\[8\]。

### 電子政府推奨暗号リスト

CRYPTRECにより安全性及び実装性能が確認され、市場における利用実績が十分であるか、今後の普及が見込まれると判断された暗号技術である。CRYPTRECにより、これらの暗号技術の利用が推奨されている。

| 暗号の種類                                                                                                                                                                       | 暗号技術                                                                                                                  |
| --------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------- |
| [公開鍵暗号](../Page/公開鍵暗号.md "wikilink")                                                                                                                                        | [署名](https://ja.wikipedia.org/wiki/電子署名 "wikilink")                                                                   |
| [ECDSA](https://ja.wikipedia.org/wiki/楕円曲線DSA "wikilink"): Certicom                                                                                                         |                                                                                                                       |
| [RSA](../Page/RSA暗号.md "wikilink")-PSS\[9\]: [PKCS](https://ja.wikipedia.org/wiki/PKCS "wikilink") \#1, [RSAセキュリティ](https://ja.wikipedia.org/wiki/RSAセキュリティ "wikilink")     |                                                                                                                       |
| RSASSA-PKCS1-v1_5\[10\]: PKCS \#1, RSAセキュリティ                                                                                                                               |                                                                                                                       |
| 守秘                                                                                                                                                                          | RSA-[OAEP](https://ja.wikipedia.org/wiki/Optimal_Asymmetric_Encryption_Padding "wikilink")\[11\]: PKCS \#1, RSAセキュリティ |
| 鍵共有                                                                                                                                                                         | [DH](https://ja.wikipedia.org/wiki/ディフィー・ヘルマン鍵共有 "wikilink"): NIST SP 800-56A Revision 1                              |
| [ECDH](https://ja.wikipedia.org/wiki/楕円曲線ディフィー・ヘルマン鍵共有 "wikilink"): NIST SP 800-56A Revision 1                                                                              |                                                                                                                       |
| [共通鍵暗号](https://ja.wikipedia.org/wiki/共通鍵暗号 "wikilink")                                                                                                                     | 64ビット[ブロック暗号](https://ja.wikipedia.org/wiki/ブロック暗号 "wikilink")\[12\]                                                  |
| 128ビットブロック暗号                                                                                                                                                                | [AES](../Page/Advanced_Encryption_Standard.md "wikilink"): NIST FIPS PUB 197                                          |
| [Camellia](https://ja.wikipedia.org/wiki/Camellia "wikilink"): [NTT](https://ja.wikipedia.org/wiki/日本電信電話 "wikilink")、[三菱電機](https://ja.wikipedia.org/wiki/三菱電機 "wikilink") |                                                                                                                       |
| [ストリーム暗号](https://ja.wikipedia.org/wiki/ストリーム暗号 "wikilink")                                                                                                                 | [KCipher-2](https://ja.wikipedia.org/wiki/KCipher-2 "wikilink"): [KDDI](../Page/KDDI.md "wikilink")                   |
| [ハッシュ関数](../Page/ハッシュ関数.md "wikilink")                                                                                                                                      | [SHA-2](https://ja.wikipedia.org/wiki/SHA-2 "wikilink")56: NIST FIPS PUB 180-4                                        |
| [SHA-384](https://ja.wikipedia.org/wiki/SHA-2 "wikilink"): NIST FIPS PUB 180-4                                                                                              |                                                                                                                       |
| [SHA-512](https://ja.wikipedia.org/wiki/SHA-2 "wikilink"): NIST FIPS PUB 180-4                                                                                              |                                                                                                                       |
| [暗号利用モード](https://ja.wikipedia.org/wiki/暗号利用モード "wikilink")                                                                                                                 | 秘匿モード                                                                                                                 |
| [CFB](https://ja.wikipedia.org/wiki/暗号利用モード#CFB "wikilink"): NIST SP 800-38A                                                                                                |                                                                                                                       |
| [CTR](https://ja.wikipedia.org/wiki/暗号利用モード#CTR "wikilink"): NIST SP 800-38A                                                                                                |                                                                                                                       |
| [OFB](https://ja.wikipedia.org/wiki/暗号利用モード#OFB "wikilink"): NIST SP 800-38A                                                                                                |                                                                                                                       |
| 認証付き秘匿モード                                                                                                                                                                   | [CCM](https://ja.wikipedia.org/wiki/Counter_with_CBC-MAC "wikilink"): NIST SP 800-38C                                 |
| [GCM](https://ja.wikipedia.org/wiki/Galois/Counter_Mode "wikilink")\[13\]: NIST SP 800-38D                                                                                  |                                                                                                                       |
| [メッセージ認証コード](https://ja.wikipedia.org/wiki/メッセージ認証符号 "wikilink")                                                                                                            | [CMAC](https://ja.wikipedia.org/wiki/CMAC "wikilink"): NIST SP 800-38B                                                |
| [HMAC](https://ja.wikipedia.org/wiki/HMAC "wikilink"): NIST FIPS PUB 198-1                                                                                                  |                                                                                                                       |
| [エンティティ認証](https://ja.wikipedia.org/wiki/エンティティ認証 "wikilink")                                                                                                               | ISO/IEC 9798-2: ISO/IEC 9798-2:2008                                                                                   |
| ISO/IEC 9798-3: ISO/IEC 9798-3:1998, ISO/IEC 9798-3:1998/Amd 1:2010                                                                                                         |                                                                                                                       |

### 推奨候補暗号リスト

CRYPTRECにより安全性および実装性能は確認されているが、現時点では十分な採用実績がないと評価された暗号技術である。

<table>
<thead>
<tr class="header">
<th><p>暗号の種類</p></th>
<th><p>暗号技術</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>公開鍵暗号</p></td>
<td><p>署名</p></td>
</tr>
<tr class="even">
<td><p>守秘</p></td>
<td><p>該当なし</p></td>
</tr>
<tr class="odd">
<td><p>鍵共有</p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/PSEC-KEM" title="wikilink">PSEC-KEM</a>[14]: NTT</p></td>
</tr>
<tr class="even">
<td><p>共通鍵暗号</p></td>
<td><p>64ビットブロック暗号[15]</p></td>
</tr>
<tr class="odd">
<td><p>: <a href="https://ja.wikipedia.org/wiki/東芝" title="wikilink">東芝</a></p></td>
<td></td>
</tr>
<tr class="even">
<td><p><a href="https://ja.wikipedia.org/wiki/MISTY1" title="wikilink">MISTY1</a>: 三菱電機</p></td>
<td></td>
</tr>
<tr class="odd">
<td><p>128ビットブロック暗号</p></td>
<td><p>: 日本電気</p></td>
</tr>
<tr class="even">
<td><p>: <a href="../Page/ソニー.md" title="wikilink">ソニー</a></p></td>
<td></td>
</tr>
<tr class="odd">
<td><p>: 東芝</p></td>
<td></td>
</tr>
<tr class="even">
<td><p>: <a href="../Page/富士通.md" title="wikilink">富士通</a></p></td>
<td></td>
</tr>
<tr class="odd">
<td><p>ストリーム暗号</p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/MUGI" title="wikilink">MUGI</a>: <a href="../Page/日立製作所.md" title="wikilink">日立製作所</a></p></td>
</tr>
<tr class="even">
<td><p><a href="https://ja.wikipedia.org/wiki/Enocoro-128v2" title="wikilink">Enocoro-128v2</a>: 日立製作所</p></td>
<td></td>
</tr>
<tr class="odd">
<td><p>[16]: 日立製作所</p></td>
<td></td>
</tr>
<tr class="even">
<td><p>ハッシュ関数</p></td>
<td><p>該当なし</p></td>
</tr>
<tr class="odd">
<td><p>暗号利用モード</p></td>
<td><p>秘匿モード</p></td>
</tr>
<tr class="even">
<td><p>認証付き秘匿モード</p></td>
<td><p>該当なし</p></td>
</tr>
<tr class="odd">
<td><p>メッセージ認証コード</p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/PC-MAC-AES" title="wikilink">PC-MAC-AES</a>: NEC</p></td>
</tr>
<tr class="even">
<td><p>エンティティ認証</p></td>
<td><p>ISO/IEC 9798-4: ISO/IEC 9798-4:1999</p></td>
</tr>
</tbody>
</table>

### 運用監視暗号リスト

実際に解読されるリスクが高まるなど、推奨すべき状態ではなくなった暗号技術である。互換性維持の目的以外での利用は推奨されない。

| 暗号の種類                                                                              | 暗号技術                                                                                                           |
| ---------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------- |
| 公開鍵暗号                                                                              | 署名                                                                                                             |
| 守秘                                                                                 | RSAES-PKCS1-v1_5\[17\]\[18\]: PKCS \#1, RSAセキュリティ                                                             |
| 鍵共有                                                                                | 該当なし                                                                                                           |
| 共通鍵暗号                                                                              | 64ビットブロック暗号\[19\]                                                                                              |
| 128ビットブロック暗号                                                                       | 該当なし                                                                                                           |
| ストリーム暗号                                                                            | 128-bit [RC4](https://ja.wikipedia.org/wiki/RC4 "wikilink")\[20\]: RSAセキュリティ                                   |
| ハッシュ関数                                                                             | [RIPEMD](https://ja.wikipedia.org/wiki/RIPEMD "wikilink")-160: Hans Dobbertin, Antoon Bosselaers, Bart Preneel |
| [SHA-1](https://ja.wikipedia.org/wiki/SHA-1 "wikilink")\[21\]: NIST FIPS PUB 180-4 |                                                                                                                |
| 暗号利用モード                                                                            | 秘匿モード                                                                                                          |
| 認証付き秘匿モード                                                                          |                                                                                                                |
| メッセージ認証コード                                                                         | [CBC-MAC](https://ja.wikipedia.org/wiki/CBC-MAC "wikilink")\[22\]: ISO/IEC 9797-1:2011                         |
| エンティティ認証                                                                           | 該当なし                                                                                                           |

### 注

## 脚注

## 関連項目

  - [暗号理論](../Page/暗号理論.md "wikilink")
  - [Advanced Encryption Standard](../Page/Advanced_Encryption_Standard.md "wikilink")
  - [NESSIE](../Page/NESSIE.md "wikilink")
  - [情報処理推進機構](https://ja.wikipedia.org/wiki/情報処理推進機構 "wikilink")
  - [情報通信研究機構](https://ja.wikipedia.org/wiki/情報通信研究機構 "wikilink")

## 外部リンク

  - [独立行政法人 情報通信研究機構 NICT](https://www.nict.go.jp/)
  - [独立行政法人 情報処理推進機構 IPA](https://www.ipa.go.jp/)
  - [CRYPTREC](https://www.cryptrec.go.jp/)
  - [CRYPTREC暗号リスト(電子政府推奨暗号リスト)](https://www.cryptrec.go.jp/list.html)
  - [CRYPTREC報告書](https://www.cryptrec.go.jp/report.html)

[Category:暗号技術](https://ja.wikipedia.org/wiki/Category:暗号技術 "wikilink") [Category:研究プロジェクト](https://ja.wikipedia.org/wiki/Category:研究プロジェクト "wikilink")

1.
2.
3.
4.
5.
6.
7.
8.
9.  「[政府機関の情報システムにおいて使用されている暗号アルゴリズム SHA-1 及び RSA1024 に係る移行指針](https://www.nisc.go.jp/active/general/pdf/angou_ikoushishin.pdf)」 を踏まえて利用すること。
10.
11.
12. より長いブロック長の暗号が利用できるのであれば、128 ビットブロック暗号を選択することが望ましい。
13. 初期化ベクトル長は 96 ビットを推奨する。
14. KEM (Key Encapsulating Mechanism)–DEM (Data Encapsulating Mechanism)構成における利用を前提とする。
15.
16. 平文サイズは64 ビットの倍数に限る。
17. 「[政府機関の情報システムにおいて使用されている暗号アルゴリズム SHA-1 及び RSA1024 に係る移行指針](https://www.nisc.go.jp/active/general/pdf/angou_ikoushishin.pdf)」 を踏まえて利用すること。
18. SSL 3.0 / TLS 1.0, 1.1, 1.2で利用実績があることから当面の利用を認める。
19.
20. 互換性維持のために継続利用をこれまで容認してきたが、今後は極力利用すべきでない。SSL/TLSでの利用を含め、電子政府推奨暗号リストに記載された暗号技術への移行を速やかに検討すること。
21.
22. 安全性の観点から、メッセージ長を固定して利用すべきである。
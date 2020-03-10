> この記事は[X.509](https://ja.wikipedia.org/wiki/X.509)から翻訳されています。


[暗号](../Page/暗号.md "wikilink")において、**X.509**とは、[ITU-T](../Page/ITU-T.md "wikilink")の[公開鍵基盤](https://ja.wikipedia.org/wiki/公開鍵基盤 "wikilink") (PKI)の規格である。X.509は、[公開鍵証明書](../Page/公開鍵証明書.md "wikilink")の標準形式やなどを定めている。

## 歴史と用法

**X.509**の第1版は、[1988年](../Page/1988年.md "wikilink")[7月3日](../Page/7月3日.md "wikilink")に[X.500](../Page/X.500.md "wikilink")標準と関連して公開された。証明書を発行するための[認証局](../Page/認証局.md "wikilink")(CA)の厳密な階層構造を規定している。[PGP](https://ja.wikipedia.org/wiki/PGP "wikilink")のような、特別な認証局だけではなく誰でも署名や他人の公開鍵の真正の確認ができる[web of trustモデルと対照的である](https://ja.wikipedia.org/wiki/web_of_trust "wikilink")。第2版は[1994年](../Page/1994年.md "wikilink")に公開され、証明書の形式はv2となったが、ほとんど使用されていない。[1997年](https://ja.wikipedia.org/wiki/1997年 "wikilink")の第3版で、証明書の形式がv3となり、[証明書失効リスト](../Page/証明書失効リスト.md "wikilink")の形式がv2となった。[2000年](../Page/2000年.md "wikilink")に第4版が公開され、標準拡張フィールドが 1 つ追加されたが、証明書や証明書失効リストの形式は第3版と同じである。X.509 v3の証明書は、[ブリッジ](../Page/ブリッジ.md "wikilink")や[メッシュネットワーク](https://ja.wikipedia.org/wiki/メッシュネットワーク "wikilink")(RFC 4158)などの他のトポロジをサポートする柔軟性を備えている。[OpenPGP](https://ja.wikipedia.org/wiki/OpenPGP "wikilink")のようなピアツーピア方式の[web of trustモデルもサポートしているが](https://ja.wikipedia.org/wiki/web_of_trust "wikilink")、[2004年](../Page/2004年.md "wikilink")現在でもほとんど使われていない。X.500システムは今まで完全に実装されたことがない。

実際のところ、*X.509証明書*という言葉は大抵の場合[IETF](https://ja.wikipedia.org/wiki/IETF "wikilink")の RFC 5280 Internet X.509 Public Key Infrastructure Certificate and Certificate Revocation List (CRL) Profile（[インターネットX.509 PKI： 証明書と CRL のプロファイル](https://www.ipa.go.jp/security/rfc/RFC5280-00JA.html)）のことを指す。これを意味する用語として、**PKIX**も用いられる。PKIXは、RFC 5280の3. Overview of Approachにおいて、Public-Key Infrastructure using X.509の略として登場している\[1\]。

## 証明書

X.509体系では、認証局は公開鍵を特定の[X.500](../Page/X.500.md "wikilink")の識別名もしくは[メールアドレス](https://ja.wikipedia.org/wiki/メールアドレス "wikilink")や[DNSエントリのような別の名前に関連付ける証明書を発行する](../Page/Domain_Name_System.md "wikilink")。

組織の信頼された[ルート証明書](../Page/ルート証明書.md "wikilink")は全従業員に配布可能であるため、従業員は社内PKIシステムを使うことができる。[Internet Explorer](../Page/Internet_Explorer.md "wikilink"), [Netscape](https://ja.wikipedia.org/wiki/Netscape "wikilink")/[Mozilla](../Page/Mozilla.md "wikilink"), [Opera](https://ja.wikipedia.org/wiki/Opera "wikilink"), [Safari](../Page/Safari.md "wikilink")のようなブラウザはインストール済みのルート証明書とともに配布されるため、大手ベンダーから入手した[SSL証明書はすぐに動作する](https://ja.wikipedia.org/wiki/Secure_Sockets_Layer "wikilink")。事実上、ブラウザの所有者が、どの証明機関をブラウザのユーザーにとっての信頼できる第三者にするかを決定している。ルート証明書は削除することも無効にすることもできるが、ユーザーがそれを行うことは極めてまれである。

X.509は[証明書失効リスト](../Page/証明書失効リスト.md "wikilink")(CRL)実装に関する標準も含んでいる。[証明書失効リスト](../Page/証明書失効リスト.md "wikilink")はPKIシステムのしばしば無視される側面のひとつである。[IETF](https://ja.wikipedia.org/wiki/IETF "wikilink")が承認している証明書の有効性の検証方法はOCSP（[Online Certificate Status Protocol](../Page/Online_Certificate_Status_Protocol.md "wikilink")）である。Firefox 3ではOCSPによる検証はデフォルトで有効になっている。

### 証明書の構造

X.509 v3 [デジタル証明書](https://ja.wikipedia.org/wiki/デジタル証明書 "wikilink") の構造は、次のとおり。

  - 証明書
      - バージョン
      - 通し番号
      - アルゴリズムID
      - 発行者
      - 有効期間
          - 開始
          - 満了
      - 主体者
      - 主体者の公開鍵情報
          - 公開鍵アルゴリズム
          - 主体者の公開鍵
      - 発行者の一意な識別子 (予備)
      - 主体者の一意な識別子 (予備)
      - 拡張 (予備)
          - ...
  - 証明書の署名アルゴリズム
  - 証明書の署名

発行者、主体者の一意な識別子はVersion 2で、拡張はVersion 3で、導入された。

### 証明書ファイルの拡張子

一般的なX.509証明書の拡張子は、次のとおり。

  - `.CER` - [CER](https://ja.wikipedia.org/wiki/Canonical_Encoding_Rules "wikilink") で符号化された証明書、ときによっては証明書群の列
  - `.DER` - [DER](https://ja.wikipedia.org/wiki/Distinguished_Encoding_Rules "wikilink") で符号化された証明書
  - `.PEM` - [Base64](../Page/Base64.md "wikilink") で符号化された証明書で、「`-----BEGIN CERTIFICATE-----`」と「`-----END CERTIFICATE-----`」で囲まれている
  - `.P7B` - `.p7c`参照
  - `.P7C` - 被署名データのない [PKCS](../Page/PKCS.md "wikilink")\#7 のSignedData構造で、証明書 (群) やCRL (群) がある
  - `.PFX` - `.p12`参照
  - `.P12` - (公開鍵や、パスワードで保護された) 私有鍵を含む [PKCS](../Page/PKCS.md "wikilink")\#12

[PKCS](../Page/PKCS.md "wikilink") \#7 は、データの署名や暗号化 (公式には「"enveloping"」) の標準である。 証明書は、署名されたデータの検証に必要なので、SignedData構造に含めることができる。 `.P7C`ファイルは、署名されるべきデータをもたないという、縮退したSignedData構造である。

PFX (Personal inFormation eXchange) 標準から発展した [PKCS](../Page/PKCS.md "wikilink") \#12 は、単一ファイルでの公開鍵と私有鍵の交換に使われる。

`.PEM`ファイルは、証明書や私有鍵を含むことがあり、このとき`BEGIN`と`END` (と`CERTIFICATE`や`RSA PRIVATE KEY`の組合せ) の行で囲まれている。

## X.509証明書の例

以下の例は[OpenSSL](https://ja.wikipedia.org/wiki/OpenSSL "wikilink")でデコードされた、`www.freesoft.org`のX.509証明書である。実際の証明書のサイズは約1KBである。証明書は、発行者フィールドに記載されているとおり、[Thawte](https://ja.wikipedia.org/wiki/Thawte "wikilink")（[VeriSignに買収された](../Page/ベリサイン.md "wikilink")）により発行された。主体者フィールドは多くの個別の情報を含んでいるが、最も重要な部分はcommon name (CN)である。これは認証されるホスト名と(ふつう大文字小文字の差を無視して)一致する必要がある。次に[RSA公開鍵](../Page/RSA暗号.md "wikilink")(法と公開指数)が含まれる。次にくるのは署名である。署名は証明書の最初の部分の[MD5](../Page/MD5.md "wikilink")ハッシュをThawteのRSA秘密鍵によって暗号化することにより計算される。

`Certificate:`
`   Data:`
`       Version: 1 (0x0)`
`       Serial Number: 7829 (0x1e95)`
`       Signature Algorithm: md5WithRSAEncryption`
`       Issuer: C=ZA, ST=Western Cape, L=Cape Town, O=Thawte Consulting cc,`
`               OU=Certification Services Division,`
`               CN=Thawte Server CA/emailAddress=server-certs@thawte.com`
`       Validity`
`           Not Before: Jul  9 16:04:02 1998 GMT`
`           Not After : Jul  9 16:04:02 1999 GMT`
`       Subject: C=US, ST=Maryland, L=Pasadena, O=Brent Baccala,`
`                OU=FreeSoft, CN=www.freesoft.org/emailAddress=baccala@freesoft.org`
`       Subject Public Key Info:`
`           Public Key Algorithm: rsaEncryption`
`           RSA Public Key: (1024 bit)`
`               Modulus (1024 bit):`
`                   00:b4:31:98:0a:c4:bc:62:c1:88:aa:dc:b0:c8:bb:`
`                   33:35:19:d5:0c:64:b9:3d:41:b2:96:fc:f3:31:e1:`
`                   66:36:d0:8e:56:12:44:ba:75:eb:e8:1c:9c:5b:66:`
`                   70:33:52:14:c9:ec:4f:91:51:70:39:de:53:85:17:`
`                   16:94:6e:ee:f4:d5:6f:d5:ca:b3:47:5e:1b:0c:7b:`
`                   c5:cc:2b:6b:c1:90:c3:16:31:0d:bf:7a:c7:47:77:`
`                   8f:a0:21:c7:4c:d0:16:65:00:c1:0f:d7:b8:80:e3:`
`                   d2:75:6b:c1:ea:9e:5c:5c:ea:7d:c1:a1:10:bc:b8:`
`                   e8:35:1c:9e:27:52:7e:41:8f`
`               Exponent: 65537 (0x10001)`
`   Signature Algorithm: md5WithRSAEncryption`
`       93:5f:8f:5f:c5:af:bf:0a:ab:a5:6d:fb:24:5f:b6:59:5d:9d:`
`       92:2e:4a:1b:8b:ac:7d:99:17:5d:cd:19:f6:ad:ef:63:2f:92:`
`       ab:2f:4b:cf:0a:13:90:ee:2c:0e:43:03:be:f6:ea:8e:9c:67:`
`       d0:a2:40:03:f7:ef:6a:15:09:79:a9:46:ed:b7:16:1b:41:72:`
`       0d:19:aa:ad:dd:9a:df:ab:97:50:65:f5:5e:85:a6:ef:19:d1:`
`       5a:de:9d:ea:63:cd:cb:cc:6d:5d:01:85:b5:6d:c8:f3:d9:f7:`
`       8f:0e:fc:ba:1f:34:e9:96:6e:6c:cf:f2:ef:9b:bf:de:b5:22:`
`       68:9f`

この証明書を検証するには、この証明書の発行者(Thawteサーバー証明書発行局)にマッチする証明書が必要である。はじめに、検証者は2つ目の証明書が認証局のものである、すなわち他の証明書を発行するのに使用できることを検証する。この動作は*X509v3 extension*セクションにある*CA*属性の値を調べることによって行われる。次に、認証局の証明書から取得したRSA公開鍵が、最初の証明書の署名をデコードしてMD5ハッシュを得るために使用される。このMD5ハッシュは証明書の残りの部分から計算された実際のMD5ハッシュと一致しなければならない。以下は認証局の証明書である。

`Certificate:`
`   Data:`
`       Version: 3 (0x2)`
`       Serial Number: 1 (0x1)`
`       Signature Algorithm: md5WithRSAEncryption`
`       Issuer: C=ZA, ST=Western Cape, L=Cape Town, O=Thawte Consulting cc,`
`               OU=Certification Services Division,`
`               CN=Thawte Server CA/emailAddress=server-certs@thawte.com`
`       Validity`
`           Not Before: Aug  1 00:00:00 1996 GMT`
`           Not After : Dec 31 23:59:59 2020 GMT`
`       Subject: C=ZA, ST=Western Cape, L=Cape Town, O=Thawte Consulting cc,`
`                OU=Certification Services Division,`
`                CN=Thawte Server CA/emailAddress=server-certs@thawte.com`
`       `**`Subject``   ``Public``   ``Key``   ``Info`**`:`
`           Public Key Algorithm: rsaEncryption`
`           RSA Public Key: (1024 bit)`
`               Modulus (1024 bit):`
`                   00:d3:a4:50:6e:c8:ff:56:6b:e6:cf:5d:b6:ea:0c:`
`                   68:75:47:a2:aa:c2:da:84:25:fc:a8:f4:47:51:da:`
`                   85:b5:20:74:94:86:1e:0f:75:c9:e9:08:61:f5:06:`
`                   6d:30:6e:15:19:02:e9:52:c0:62:db:4d:99:9e:e2:`
`                   6a:0c:44:38:cd:fe:be:e3:64:09:70:c5:fe:b1:6b:`
`                   29:b6:2f:49:c8:3b:d4:27:04:25:10:97:2f:e7:90:`
`                   6d:c0:28:42:99:d7:4c:43:de:c3:f5:21:6d:54:9f:`
`                   5d:c3:58:e1:c0:e4:d9:5b:b0:b8:dc:b4:7b:df:36:`
`                   3a:c2:b5:66:22:12:d6:87:0d`
`               Exponent: 65537 (0x10001)`
`       X509v3 extensions:`
`           X509v3 Basic Constraints: critical`
`               `**`CA:TRUE`**
`   Signature Algorithm: md5WithRSAEncryption`
`       07:fa:4c:69:5c:fb:95:cc:46:ee:85:83:4d:21:30:8e:ca:d9:`
`       a8:6f:49:1a:e6:da:51:e3:60:70:6c:84:61:11:a1:1a:c8:48:`
`       3e:59:43:7d:4f:95:3d:a1:8b:b7:0b:62:98:7a:75:8a:dd:88:`
`       4e:4e:9e:40:db:a8:cc:32:74:b9:6f:0d:c6:e3:b3:44:0b:d9:`
`       8a:6f:9a:29:9b:99:18:28:3b:d1:e3:40:28:9a:5a:3c:d5:b5:`
`       e7:20:1b:8b:ca:a4:ab:8d:e9:51:d9:e2:4c:2c:59:a9:da:b9:`
`       b2:75:1b:f6:42:f2:ef:c7:f2:18:f9:89:bc:a3:ff:8a:23:2e:`
`       70:47`

これは自己署名証明書の例であり、発行者と主体者が同一である。この証明書を自分自身に対して検証する以外に、この証明書を検証する方法はない。代わりに、これらのトップレベル証明書はブラウザによって保持される。Thawteは[マイクロソフト](../Page/マイクロソフト.md "wikilink")と[Netscape両方に認められているルート証明書発行局の](https://ja.wikipedia.org/wiki/ネットスケープ "wikilink")1つである。この証明書はウェブブラウザと一緒に出荷され、デフォルトで信頼される。この証明書は、X509v3 Basic Constraintsセクションに制約の無い、あらゆる物に署名できる長期的かつ世界的に信頼された証明書であるため、対になる秘密鍵は厳重に保護される必要がある。

## セキュリティ

PKIの問題については数多くの出版物がある<ref name="schneier">

` `

</ref><ref name="pkinotdead">

` `

</ref><ref name="gutmann1">

` `

</ref>。

2005年、[Arjen Lenstraと](https://ja.wikipedia.org/wiki/Arjen_Lenstra "wikilink")[Benne de Wegerは](https://ja.wikipedia.org/wiki/Benne_de_Weger "wikilink")"公開鍵のみが異なる同一署名をもつ2つのX.509証明書を構築するためにハッシュ衝突を使用する方法"を公開した。[MD5](../Page/MD5.md "wikilink")ハッシュ関数に対する[衝突攻撃](https://ja.wikipedia.org/wiki/衝突攻撃 "wikilink") (collision attack)を使用して達成している。[1](http://www.win.tue.nl/~bdeweger/CollidingCertificates/ddl-full.pdf)

## 認証局

認証局(CA, certificate authority, certification authority)は他者が使うためのデジタル証明書を発行するエンティティである。これは[信頼できる第三者機関](https://ja.wikipedia.org/wiki/trusted_third_party "wikilink")(TTP, Trusted Third Party)の一例である。認証局は多くの公開鍵基盤の特徴となっている。

これらのサービスを料金を取って行う商用の認証局が多く存在している。いくつかの団体や政府は独自の認証局を運営している。また、[Let's Encryptのように無償の認証局もある](https://ja.wikipedia.org/wiki/Let's_Encrypt "wikilink")。

## 公開鍵基盤 (X.509) ワーキング・グループ

公開鍵基盤 (X.509) ワーキング・グループ（PKIXワーキンググループ）は[Internet Engineering Task Forceの](../Page/Internet_Engineering_Task_Force.md "wikilink")[ワーキンググループ](https://ja.wikipedia.org/wiki/ワーキンググループ "wikilink")である。X.509証明書に基づいた公開鍵基盤に関連する[RFCを開発している](../Page/Request_for_Comments.md "wikilink")。PKIXワーキング・グループは1995年の秋に設立された。

## X.509証明書関連のプロトコル、標準

  - [Transport Layer Security](../Page/Transport_Layer_Security.md "wikilink") (TLS/SSL)
  - [S/MIME](https://ja.wikipedia.org/wiki/S/MIME "wikilink")
  - [IPsec](https://ja.wikipedia.org/wiki/IPsec "wikilink")
  - [SSH](../Page/Secure_Shell.md "wikilink")
  - [スマートカード](https://ja.wikipedia.org/wiki/スマートカード "wikilink")
  - [HTTPS](../Page/HTTPS.md "wikilink")
  - [Extensible Authentication Protocol](https://ja.wikipedia.org/wiki/Extensible_Authentication_Protocol "wikilink")
  - [LDAP](../Page/Lightweight_Directory_Access_Protocol.md "wikilink")
  - [Trusted Computing Group](https://www.trustedcomputinggroup.org/faq/TNCFAQ/) (TNC TPM NGSCB)
  - [CableLabs](https://www.cablelabs.com/) (North American Cable Industry Technology Forum)
  - [WS-Security](../Page/WS-Security.md "wikilink")

## 参考文献

  - [ITU-T Recommendation X.509](http://www.itu.int/rec/T-REC-X.509-200508-I) (2005): Information Technology - Open Systems Interconnection - The Directory: Authentication Framework, 08/05.
  - Housley, R., W. Ford, W. Polk and D. Solo, "Internet X.509 Public Key Infrastructure: Certificate and CRL Profile", RFC 2459, January 1999.
  - Housley, R., W. Ford, W. Polk and D. Solo, "Internet X.509 Public Key Infrastructure: Certificate and CRL Profile", RFC 3280, April 2002.
  - David Cooper, et al., "Internet X.509 Public Key Infrastructure Certificate and Certificate Revocation List (CRL) Profile", RFC 5280, May 2008.
  - Arjen Lenstra, Xiaoyun Wang and Benne de Weger, On the possibility of constructing meaningful hash collisions for public keys, full version, with an appendix on colliding X.509 certificates, 2005 [2](https://www.win.tue.nl/~bdeweger/CollidingCertificates/) (see also [3](https://eprint.iacr.org/2005/067)).

## 関連項目

  - [デジタル証明書](https://ja.wikipedia.org/wiki/デジタル証明書 "wikilink")
  - [デジタル署名](../Page/デジタル署名.md "wikilink")
  - [公開鍵](https://ja.wikipedia.org/wiki/公開鍵 "wikilink")
  - [公開鍵基盤](https://ja.wikipedia.org/wiki/公開鍵基盤 "wikilink") (PKI)
  - [認証局](../Page/認証局.md "wikilink") (CA)
  - [Pretty Good Privacy](../Page/Pretty_Good_Privacy.md "wikilink") (PGP)
  - [証明書ポリシー](https://ja.wikipedia.org/wiki/:en:Certificate_Policy "wikilink")
  - [オンライン証明書検証プロトコル](https://ja.wikipedia.org/wiki/OCSP "wikilink") (OCSP)
  - [CRL](../Page/証明書失効リスト.md "wikilink")

## 脚注

## 外部リンク

  - RFC 5280
      - [インターネットX.509 PKI： 証明書と CRL のプロファイル](https://www.ipa.go.jp/security/rfc/RFC5280-00JA.html) — [IPAによる日本語訳](../Page/情報処理推進機構.md "wikilink")
  - Peter Gutmannの[X.509スタイル・ガイド](https://www.cs.auckland.ac.nz/~pgut001/pubs/x509guide.txt)
  - [PKIXのサイト](https://datatracker.ietf.org/group/pkix/about/)

[Category:公開鍵基盤](https://ja.wikipedia.org/wiki/Category:公開鍵基盤 "wikilink") [Category:ITU-T勧告](https://ja.wikipedia.org/wiki/Category:ITU-T勧告 "wikilink") [Category:暗号化プロトコル](https://ja.wikipedia.org/wiki/Category:暗号化プロトコル "wikilink")

1.
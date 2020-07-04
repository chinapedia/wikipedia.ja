> この記事は[PKCS](https://ja.wikipedia.org/wiki/PKCS)から翻訳されています。


**PKCS** (Public-Key Cryptography Standards) は、[RSAセキュリティ](../Page/RSAセキュリティ.md "wikilink")により考案され公開された[公開鍵暗号](../Page/公開鍵暗号.md "wikilink")標準のグループを示す。

[RSAセキュリティ](../Page/RSAセキュリティ.md "wikilink")は、[RSA暗号](../Page/RSA暗号.md "wikilink")アルゴリズムの（2000年に期限が切れた）[特許](../Page/特許.md "wikilink")に対するライセンス権を割り当て、幾つかの他の鍵に関する特許（例：[Schnorr](https://ja.wikipedia.org/wiki/Schnorr "wikilink")特許）も同様に取得した。このように、[RSAセキュリティ](../Page/RSAセキュリティ.md "wikilink")および、その研究部門である RSA Labs は、公開鍵技術利用の普及と促進に関心を持っており、その結果、RSA は PKCS 標準を開発した。RSA は彼らが必要であると考えた変更や改良は行うと告知し、PKCS 標準を管理し続けた。そのため PKCS 標準は多くの意味において、その名前にかかわらず本当の産業標準ではなかった。全てではないが、近年になって PKCS の一部は一つ以上の標準化組織（有名なところでは[IETF](https://ja.wikipedia.org/wiki/IETF "wikilink") [PKIX](https://ja.wikipedia.org/wiki/PKIX "wikilink") ワーキンググループ）により'標準化'手続きに入っている。

<table>
<caption>PKCS 標準の一覧</caption>
<thead>
<tr class="header">
<th></th>
<th><p>バージョン</p></th>
<th><p>名前</p></th>
<th><p>説明</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><p>2.2</p></td>
<td><p>RSA暗号標準</p></td>
<td><p>RFC 8017 参照。RSA暗号鍵、公開鍵および秘密鍵のフォーマットの規定。Not encrypted.</p></td>
</tr>
<tr class="even">
<td><p>PKCS #2</p></td>
<td><p>-</p></td>
<td><p><em>廃案</em></p></td>
<td><p>現在、無効。メッセージダイジェストのRSA暗号を扱っていたが、PKCS#1に統合された。</p></td>
</tr>
<tr class="odd">
<td><p>PKCS #3</p></td>
<td><p>1.4</p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/Diffie-Hellman鍵共有" title="wikilink">Diffie-Hellman鍵共有</a>標準</p></td>
<td><p>お互いに事前知識を持たない2つの組織が連携して安全でない通信チャンネルを上でも共通鍵を確立できるようにする暗号プロトコル。</p></td>
</tr>
<tr class="even">
<td><p>PKCS #4</p></td>
<td><p>-</p></td>
<td><p><em>廃案</em></p></td>
<td><p>現在、無効。RSA 鍵の構文を扱っていたが、PKCS#1に統合された。</p></td>
</tr>
<tr class="odd">
<td><p>PKCS #5</p></td>
<td><p>2.1</p></td>
<td><p>パスワードに基づく暗号化の標準</p></td>
<td><p>RFC 8018 および <a href="../Page/PBKDF2.md" title="wikilink">PBKDF2</a> を参照。</p></td>
</tr>
<tr class="even">
<td><p>PKCS #6</p></td>
<td><p>1.5</p></td>
<td><p>拡張された証明書構文の標準</p></td>
<td><p>古い<a href="../Page/X.509.md" title="wikilink">X.509</a>v1証明書の仕様に対する拡張を規定。X.509v3により破棄。</p></td>
</tr>
<tr class="odd">
<td><p><a href="https://ja.wikipedia.org/wiki/PKCS7" title="wikilink">PKCS #7</a></p></td>
<td><p>1.5</p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/暗号メッセージ構文" title="wikilink">暗号メッセージ構文</a>標準</p></td>
<td><p>RFC 2315 参照。<a href="https://ja.wikipedia.org/wiki/公開鍵基盤" title="wikilink">PKI</a> の下でメッセージを署名や暗号化するのに使用される。証明書の配布のためにも用いられる（例えば、PKCS #10メッセージの応答として）。現在、RFC 3852 に基づいている <a href="https://ja.wikipedia.org/wiki/S/MIME" title="wikilink">S/MIME</a> の基礎を構成し、<a href="https://ja.wikipedia.org/wiki/暗号メッセージ構文" title="wikilink">暗号メッセージ構文</a>標準 (CMS) として更新されている。</p></td>
</tr>
<tr class="even">
<td></td>
<td><p>1.2</p></td>
<td><p>秘密鍵情報構文の標準</p></td>
<td><p>RFC 5958 参照。</p></td>
</tr>
<tr class="odd">
<td><p>PKCS #9</p></td>
<td><p>2.0</p></td>
<td><p>選択された属性タイプ</p></td>
<td><p>RFC 2985 参照。PKCS #6 証明書拡張、PKCS #7 デジタル署名メッセージ、PKCS #8 秘密鍵情報、および PKCS #10 証明書署名要求で利用される属性タイプの選択された定義。</p></td>
</tr>
<tr class="even">
<td><p>PKCS #10</p></td>
<td><p>1.7</p></td>
<td><p><a href="../Page/証明書署名要求.md" title="wikilink">証明書署名要求</a></p></td>
<td><p>RFC 2986 参照。公開鍵の認証を要求するために<a href="../Page/認証局.md" title="wikilink">認証局</a>へ送信されるメッセージのフォーマット。<a href="../Page/証明書署名要求.md" title="wikilink">証明書署名要求</a>を参照。</p></td>
</tr>
<tr class="odd">
<td></td>
<td><p>2.40</p></td>
<td><p>暗号トークンインタフェース (Cryptoki)</p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/暗号トークン" title="wikilink">暗号トークン</a>への汎用インタフェースを定義する<a href="../Page/アプリケーションプログラミングインタフェース.md" title="wikilink">API</a>。（<a href="https://ja.wikipedia.org/wiki/ハードウェアセキュリティモジュール" title="wikilink">ハードウェアセキュリティモジュール</a>も参照の事）</p></td>
</tr>
<tr class="even">
<td></td>
<td><p>1.1</p></td>
<td><p>個人情報交換構文の標準</p></td>
<td><p>RFC 7292 参照。パスワードに基づく<a href="https://ja.wikipedia.org/wiki/共通鍵" title="wikilink">鍵（暗号）により保護された</a><a href="https://ja.wikipedia.org/wiki/秘密鍵" title="wikilink">秘密鍵</a>と、それに関連する<a href="../Page/X.509.md" title="wikilink">公開鍵証明書を保管するために一般に利用されるファイルフォーマットの定義</a>。PFXは PKCS#12 の旧称である。</p>
<p>これは、複数の組み込みオブジェクト、例えば複数の証明書を格納できるコンテナフォーマットである。通常、パスワードにより保護/暗号化される。</p>
<p>Java の鍵ストアのフォーマットとして利用できる。Tomcat では利用できるが Apache では利用<strong>できない</strong>。</p></td>
</tr>
<tr class="odd">
<td><p>PKCS #13</p></td>
<td><p>–</p></td>
<td><p><a href="../Page/楕円曲線暗号.md" title="wikilink">楕円曲線暗号</a>の標準</p></td>
<td><p>（策定中）98年の提案から進展なし。</p></td>
</tr>
<tr class="even">
<td><p>PKCS #14</p></td>
<td><p>–</p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/擬似乱数生成器" title="wikilink">擬似乱数</a></p></td>
<td><p>（策定中）EMCのサイトからは削除されている。</p></td>
</tr>
<tr class="odd">
<td><p>PKCS #15</p></td>
<td><p>1.1</p></td>
<td><p>暗号トークン情報フォーマットの標準</p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/暗号トークン" title="wikilink">暗号トークン</a>のユーザが、アプリケーションの Cryptoki の実装 (PKCS #11) や他のAPIに依存せず、アプリケーションに対し自身を特定できるようにするための標準の規定。RSA は、この標準のICカードに関する部分を ISO/IEC 7816-15に対し譲渡した。<a href="http://www.rsasecurity.com/rsalabs/node.asp?id=2141">1</a></p></td>
</tr>
</tbody>
</table>

## 関連項目

  - [暗号メッセージ構文](https://ja.wikipedia.org/wiki/暗号メッセージ構文 "wikilink") (CMS)
  - [ASN.1 (Abstract Syntax Notation One)](../Page/Abstract_Syntax_Notation_One.md "wikilink")

## 注釈・参考文献

  - Jean-Sébastien Coron, Marc Joye, [David Naccache](https://ja.wikipedia.org/wiki/David_Naccache "wikilink"), and Pascal Paillier, New Attacks on PKCS \#1 v1.5 Encryption, [EUROCRYPT](https://ja.wikipedia.org/wiki/EUROCRYPT "wikilink") 2000, pp. 69-381. [2](http://www.gemplus.com/smart/rd/publications/pdf/CJNP00pk.pdf)

## 外部リンク

  - [EMC内RSA Laboratories PKCS](http://www.emc.com/emc-plus/rsa-labs/standards-initiatives/public-key-cryptography-standards.htm)
  - [PSS (Probabilistic Signature Scheme)](http://www.emc.com/emc-plus/rsa-labs/standards-initiatives/what-is-pss-pss-r.htm)
  - [PKCS\#12 FAQ](http://www.drh-consultancy.demon.co.uk/pkcs12faq.html), [OpenSSL](https://ja.wikipedia.org/wiki/OpenSSL "wikilink")のStephen Hensonによる

[Category:暗号技術](https://ja.wikipedia.org/wiki/Category:暗号技術 "wikilink")
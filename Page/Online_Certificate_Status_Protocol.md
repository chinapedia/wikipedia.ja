> この記事は[Online Certificate Status Protocol](https://ja.wikipedia.org/wiki/Online_Certificate_Status_Protocol)から翻訳されています。


**Online Certificate Status Protocol**（**OCSP**）は、[X.509](https://ja.wikipedia.org/wiki/X.509 "wikilink")[公開鍵証明書](https://ja.wikipedia.org/wiki/公開鍵証明書 "wikilink")の失効状態を取得するための[通信プロトコル](../Page/通信プロトコル.md "wikilink")である。RFC 6960 で規定されており、[インターネット標準](../Page/インターネット標準.md "wikilink")トラック上にある。[証明書失効リスト](https://ja.wikipedia.org/wiki/証明書失効リスト "wikilink") (CRL) の代替として策定されたもので、CRLを[公開鍵基盤](https://ja.wikipedia.org/wiki/公開鍵基盤 "wikilink") (PKI) で使う際の問題に対応している。OCSP のメッセージは [ASN.1](../Page/Abstract_Syntax_Notation_One.md "wikilink") で符号化されており、主に [HTTP](../Page/Hypertext_Transfer_Protocol.md "wikilink") を使ってやり取りされる。要求/応答型メッセージであることから、OCSPの[サーバ](../Page/サーバ.md "wikilink")を「OCSPレスポンダ」と呼ぶ。

## CRL との比較

  - OCSP応答は典型的なCRLよりも情報が少ないため、OCSPは証明書の失効状態をよりタイムリーに提供できる。しかし、[クライアントが応答を](../Page/クライアント_\(コンピュータ\).md "wikilink")[キャッシュしないと](https://ja.wikipedia.org/wiki/キャッシュ_\(コンピュータシステム\) "wikilink")、要求回数の増大によって利点が生かせなくなる可能性がある。
  - OCSPを使えば、クライアントがCRLを[構文解析](../Page/構文解析.md "wikilink")する必要がなくなり、クライアント側の複雑さが低減される。しかし、これもキャッシュを保持する必要性によって相殺される。実際には、X.509 関連の機能をアプリケーションが独自に実装することは滅多になく、サードパーティ製[ライブラリ](../Page/ライブラリ.md "wikilink")を使うため、このような考慮はあまり意味がない。
  - CRL は[クレジットカード](../Page/クレジットカード.md "wikilink")会社の「悪質顧客リスト」のようなものと考えられるかもしれない。つまり、知らせる必要のない情報まで公開しているとも考えられる。
  - OCSPは特定のネットワークホストが特定の時間に特定の証明書を使っただろうことをレスポンダに明らかにする。OCSPは暗号化を強制していないので、この情報は第三者に横取りされるかもしれない。

## 基本的なPKI実装

1.  [アリスとボブ](https://ja.wikipedia.org/wiki/アリスとボブ "wikilink")は、[認証局](https://ja.wikipedia.org/wiki/認証局 "wikilink") (CA) であるイバンの発行した[公開鍵証明書](https://ja.wikipedia.org/wiki/公開鍵証明書 "wikilink")を持っている。
2.  アリスはボブと取引したいので、彼に自身の公開鍵証明書を送る。
3.  ボブはアリスの秘密鍵が失効していないかを確認するため、アリスの公開鍵の[メッセージダイジェスト](https://ja.wikipedia.org/wiki/メッセージダイジェスト "wikilink")を含むOCSP要求を作成し、イバンに送る。
4.  OCSPレスポンダであるイバンはアリスの証明書の失効状態をCAデータベースで参照する。アリスの秘密鍵が失効しているかどうかについて信頼できる記録があるのは、CAデータベースだけである。
5.  イバンはアリスの証明書の有効性を確認すると、[デジタル署名](../Page/デジタル署名.md "wikilink")付きのOCSP応答をボブに返す。
6.  ボブは応答の署名を検証し（ボブはイバンの公開鍵を持っており、イバンは信頼できるレスポンダである）、それが最新のものであることを確認する。
7.  ボブはアリスとの取引を実行する。

## プロトコルの詳細

OCSPレスポンダは要求の中で指定された証明書について「有効」、「失効」、「不明」のいずれかの応答を署名付きで返す。要求を処理できない場合は、エラーコードを返すこともある。

OCSP要求のフォーマットには付加的な拡張がある。これにより、特定のPKI方式にカスタマイズすることが可能である。

OCSPは[反射攻撃](https://ja.wikipedia.org/wiki/反射攻撃 "wikilink")に対して耐性がある。署名された「有効」な応答を悪意ある第三者が横取りした場合、その証明書が失効になった後でクライアントに対してそれを使う攻撃である。OCSPでは、[Nonce](https://ja.wikipedia.org/wiki/Nonce "wikilink")（使い捨ての数字）を要求に含め、対応する応答に同じものを含めなければならないとすることで対処している。

しかし、反射攻撃は1つの可能性ではあるが、認証システムでは主要な脅威ではない。これはその脆弱性を利用した攻撃の手順に起因する。攻撃者は以下のことをしなければならない。

1.  トラフィックを監視して、その後にそのトラフィックに応答する。
2.  証明書の状態を監視して、それが変更されたことを確認する。
3.  応答の妥当な時間内に証明書の状態を要求するトランザクションを実施する。

失効した証明書が有効になることは滅多にないので（停止されているだけならば可能性はある）、攻撃者は有効な応答を捉え、証明書が失効するのを待ち、それを使う必要がある。

OCSPは複数レベルのCAをサポートできる。OCSP要求をレスポンダ間で連鎖させ、発行元のCAがその証明書を発行するのに適切かどうかを調べることができる。レスポンダは自身のOCSP要求を使ってルートCAに対して相互の妥当性を保証する。

OCSPレスポンダは、[Delegated Path Validation](https://ja.wikipedia.org/wiki/Delegated_Path_Validation "wikilink") (DPV) サーバから失効情報を要求されることがある。OCSP自身は供給された証明書についてDPVを実行することはない。

## ブラウザでのサポート状況

  - [Internet Explorer](../Page/Internet_Explorer.md "wikilink") は Windows Vista（XPではない）上の version 7 で OCSP チェックのサポートを開始した。
  - [Firefox](../Page/Mozilla_Firefox.md "wikilink") は全バージョンで OCSP チェックをサポートしている。Firefox 3 では既定でチェックが有効となる。
  - Mac OS X 上の Safari は OCSP チェックをサポートしている。
  - Opera の最新版は OCSP チェックをサポートしている。
  - Google Chrome は待ち時間やプライバシーの問題を理由に、2012年に OCSP チェックをデフォルトでは無効にした\[1\]。

## 脚注

<references />

## 外部リンク

  -
  - [RFC 6960, X.509 Internet Public Key Infrastructure Online Certificate Status Protocol - OCSP](http://tools.ietf.org/html/rfc6960)

  - [RFC 2560, X.509 Internet Public Key Infrastructure Online Certificate Status Protocol - OCSP](http://tools.ietf.org/html/rfc2560)

      - [X.509インターネット PKIオンライン証明書状態プロトコル（OCSP）](https://www.ipa.go.jp/security/rfc/RFC2560JA.html) — [IPAによる日本語訳](https://ja.wikipedia.org/wiki/情報処理推進機構 "wikilink")

[Category:インターネットのプロトコル](https://ja.wikipedia.org/wiki/Category:インターネットのプロトコル "wikilink") [Category:インターネット標準](https://ja.wikipedia.org/wiki/Category:インターネット標準 "wikilink") [Category:暗号化プロトコル](https://ja.wikipedia.org/wiki/Category:暗号化プロトコル "wikilink") [Category:長大な項目名](https://ja.wikipedia.org/wiki/Category:長大な項目名 "wikilink") [Category:公開鍵基盤](https://ja.wikipedia.org/wiki/Category:公開鍵基盤 "wikilink") [Category:Transport_Layer_Security](https://ja.wikipedia.org/wiki/Category:Transport_Layer_Security "wikilink") [Category:RFC](https://ja.wikipedia.org/wiki/Category:RFC "wikilink")

1.  <https://www.imperialviolet.org/2012/02/05/crlsets.html>
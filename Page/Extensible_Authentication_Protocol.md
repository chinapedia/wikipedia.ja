> この記事は[Extensible Authentication Protocol](https://ja.wikipedia.org/wiki/Extensible_Authentication_Protocol)から翻訳されています。


**Extensible Authentication Protocol**（**拡張認証プロトコル**：EAP：イーエーピー，イープ）は[認証](../Page/認証.md "wikilink")プロトコルの一つであり、各種の拡張認証方式を利用するための手続きをまとめたものである。主に[PPPや](../Page/Point-to-Point_Protocol.md "wikilink")[イーサネット](../Page/イーサネット.md "wikilink")などのデータリンク層での認証に利用される。実際に利用する認証方式についてはきわめて多岐に渡り、各メーカーによる独自拡張も許されている。

## 代表的な認証方式

  - EAP-MD5
    ユーザー名と[パスワード](../Page/パスワード.md "wikilink")による認証だが、平文を流さないために[MD5](../Page/MD5.md "wikilink")ハッシュを用いる。[クライアント側のみ認証される](../Page/クライアント_\(コンピュータ\).md "wikilink")。
  - EAP-TLS ()
    [サーバ](../Page/サーバ.md "wikilink")、[クライアント双方に](../Page/クライアント_\(コンピュータ\).md "wikilink")[電子証明書](https://ja.wikipedia.org/wiki/電子証明書 "wikilink")を準備し、これによって認証を行う。[Transport Layer Securityのサーバー認証](../Page/Transport_Layer_Security.md "wikilink")・クライアント認証の仕組みを用いる。
  - EAP-TTLS ()
    サーバ側にのみ電子証明書を準備してサーバ認証済みのTLS通信路を構築し、その暗号化通信路を通してパスワードによるクライアント認証を行う。
  - EAP-PEAP ()
    サーバ側にのみ電子証明書を準備してサーバ認証済みのTLS通信路を構築し、その暗号化通信路を通してさらにEAP通信を行い、クライアントを認証する。この際クライアントの認証はパスワードやキートークンなど、電子証明書以外の認証手段を利用する事が一般的である。

## 利用例

EAPは[LANにおけるユーザー認証の規格である](../Page/Local_Area_Network.md "wikilink")[IEEE 802.1Xに採用されている](https://ja.wikipedia.org/wiki/IEEE_802.1X "wikilink")。 特に[無線LAN](../Page/無線LAN.md "wikilink")においては、電波を通信媒体としている為に無断利用が問題視されており、この解決方法として[IEEE 802.11i等の規格に採用された](https://ja.wikipedia.org/wiki/IEEE_802.11#IEEE_802.11i "wikilink")。

## 関連項目

  - [ネットワークアクセスサーバ](https://ja.wikipedia.org/wiki/ネットワークアクセスサーバ "wikilink")
  - [Protocol for Carrying Authentication for Network Access](https://ja.wikipedia.org/wiki/Protocol_for_Carrying_Authentication_for_Network_Access "wikilink") (PANA)

## 外部リンク

  - RFC 3748 Extensible Authentication Protocol (EAP)

[Category:RFC](https://ja.wikipedia.org/wiki/Category:RFC "wikilink") [Category:認証プロトコル](https://ja.wikipedia.org/wiki/Category:認証プロトコル "wikilink") [Category:モバイルネットワーク](https://ja.wikipedia.org/wiki/Category:モバイルネットワーク "wikilink") [Category:長大な項目名](https://ja.wikipedia.org/wiki/Category:長大な項目名 "wikilink")
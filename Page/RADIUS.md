> この記事は[RADIUS](https://ja.wikipedia.org/wiki/RADIUS)から翻訳されています。


**RADIUS**（**ラディウス**、**ラディアス**、**Remote Authentication Dial In User Service**）は、ネットワーク資源の利用の可否の判断（[認証](../Page/認証.md "wikilink")）と、利用の事実の記録（アカウンティング）を、[ネットワーク上の](../Page/コンピュータネットワーク.md "wikilink")[サーバ](../Page/サーバ.md "wikilink")[コンピュータ](../Page/コンピュータ.md "wikilink")に一元化することを目的とした、[IP上の](../Page/Internet_Protocol.md "wikilink")[プロトコル](../Page/プロトコル.md "wikilink")である。名称に「ダイヤルイン」という言葉を含むことからわかるように、元来は[ダイヤルアップ・インターネット接続サービスを実現することを目的として開発された](../Page/ダイヤルアップ接続.md "wikilink")。しかし、常時接続方式の[インターネット](../Page/インターネット.md "wikilink")接続サービス、[無線LAN](../Page/無線LAN.md "wikilink")、[VLAN](../Page/Virtual_Local_Area_Network.md "wikilink")、[コンテンツ](../Page/コンテンツ.md "wikilink")提供サービスなどのサービス提供者側設備において、認証とアカウンティングを実現するプロトコルとして幅広く利用されている。

## クライアントサーバモデル

RADIUSプロトコルは、[クライアントサーバモデル](../Page/クライアントサーバモデル.md "wikilink")に基づいたプロトコルである。RADIUSプロトコルにおける[クライアントは](../Page/クライアント_\(コンピュータ\).md "wikilink")、利用者（人またはコンピュータ）に対してネットワーク接続サービスなどのサービスを提供する機材であり、サーバに対して認証およびアカウンティングを要請する。サーバは、クライアントからの要請に応じて認証およびアカウンティングを行い、応答する。常にクライアントが要求し、サーバが応答する。利用者へのサービスの停止させることなど、サーバがクライアントに対して要求を開始することはできない。クライアントおよびサーバを、一般に「RADIUSクライアント」および「RADIUSサーバ」と呼ぶ。

## RADIUSクライアントの例

インターネット接続サービスにおいては、ダイヤルアップ着信装置や[ブロードバンドアクセスサーバ](https://ja.wikipedia.org/wiki/ブロードバンドアクセスサーバ "wikilink")（BAS、Broadband Access Server）などの着信装置（[NAS](https://ja.wikipedia.org/wiki/ネットワークアクセスサーバ "wikilink")、Network Access Server）がRADIUSクライアントである（「サーバ」という名称であっても、RADIUSプロトコルの観点ではクライアントである）。無線LANにおいては、[無線LANアクセスポイントである](../Page/アクセスポイント_\(無線LAN\).md "wikilink")。VLANにおいては、VLANスイッチである。コンテンツ提供サービスにおいては、[ウェブサーバがRADIUSクライアントとして機能するだろう](../Page/Webサーバ.md "wikilink")。

## プロトコルの概要

クライアントがサーバに「RADIUS要求パケット」を送信し、サーバがクライアントに「RADIUS応答パケット」を送信する。いずれの方向の通信も、IP上の[UDPパケットによって行う](../Page/User_Datagram_Protocol.md "wikilink")。

いずれのパケットも、ヘッダ部分20[オクテットと](../Page/8ビット.md "wikilink")、「属性」部分とからなる。ヘッダ部分は、種別コード（Code）1オクテット、識別子（Identifier）1オクテット、パケット全体の長さ2オクテット、「認証符号（オーセンティケータ、Authenticator）」16オクテットからなる。識別子は、クライアントが決めて要求パケットに設定し、サーバが応答パケットにコピーする。クライアントが、受信した応答パケットと過去に送信した要求パケットとの対応付けを行うために使用する。クライアントの実装では1ずつ増加する数値とするのが一般的であるが、[シリアル番号](../Page/シリアル番号.md "wikilink")であるとは規定されていない。認証符号とは、送信者の詐称と改竄（かいざん）の無いことの証明を行うデータである。属性部分は、属性値ペア (Attribute Value Pair) を任意の回数繰り返したものである。属性値ペアは、属性番号1オクテット、長さ1オクテット、属性の値からなる。値としては、4オクテットの整数値、4オクテットの[IPアドレス](../Page/IPアドレス.md "wikilink")、1 - 253オクテットの文字列などを与えることができる。

属性番号ごとに、属性値ペアの値の意味が[RFC文書において規定されている](../Page/Request_for_Comments.md "wikilink")。属性番号に対する意味を新たに定義することによって使用目的を増やすことができることが、RADIUSプロトコルの柔軟性の源であり、最大の特徴である。機器のベンダが独自に属性番号の意味を定義して独自の目的に使用することは推奨されない。ベンダ独自の機能に対応するためには、属性番号26番 (Vendor Specific) の値として、ベンダ番号を含むデータを与えることが推奨される。属性番号26番の属性値ペアを、一般にVSA (Vendor Specific Attribute) と呼ぶ。ベンダ番号は、[IANAが管理および付与している](../Page/Internet_Assigned_Numbers_Authority.md "wikilink")。

属性値ペアにさまざまな情報を含めることによって、認証とアカウンティングを行う。認証のために、ユーザ名、パスワードのための属性番号が用意されている。ダイヤルアップ・インターネット接続において[PPPを使用する場合のため](../Page/Point-to-Point_Protocol.md "wikilink")、PPP用の認証プロトコルである[PAP](../Page/PAP.md "wikilink")、[CHAP](https://ja.wikipedia.org/wiki/CHAP "wikilink")、[EAPのそれぞれに適した属性番号が用意されている](https://ja.wikipedia.org/wiki/PPP_Extensible_Authentication_Protocol "wikilink")。アカウンティングのために、利用秒数、送受信データ量などの属性番号が用意されている。これからわかるように、属性番号によって、認証とアカウンティングのどちらで利用できるのか、どちらでも利用できるのかの違いがある。

RADIUSパケットの最大長は、RADIUS認証プロトコルにおいては4096オクテット、RADIUSアカウンティングプロトコルにおいては4095オクテットである。RADIUSアカウンティングプロトコルが4096オクテットでなく4095オクテットであることには特に意味がないようである（RFCの執筆者によれば、タイプミスがそのまま規格になってしまったとのことである）。

## AAAモデル

「RADIUSプロトコルは、[AAAモデル](https://ja.wikipedia.org/wiki/AAAモデル "wikilink")([AAA プロトコル](https://ja.wikipedia.org/wiki/AAA_プロトコル "wikilink"))に基づいたプロトコルである」という表現をすることがある。AAAモデルとは、サービスの提供から記録までの流れを、[認証](../Page/認証.md "wikilink") (Authentication)、[承認](https://ja.wikipedia.org/wiki/認可_\(セキュリティ\) "wikilink") (Authorization)、アカウンティング (Accounting) の3つの段階に分けて考えるモデルである。**認証**とは、利用者が誰であるかを識別することである。この点では、認証よりも「**利用者の識別**」と言ったほうが適切かもしれない。一番単純な認証は、ユーザ名とパスワードの組み合わせが正しいことを確認する方法だろう。**承認**とは、認証済みの利用者に対してサービスを提供するか否かを判断することである。たとえば、利用の時刻、発信者電話番号などによる利用場所、前払い利用料金の残額などによって判断するだろう。「認可」「許可」と訳されることもある。**アカウンティング**とは、利用の事実を記録することである。

RADIUSプロトコル自体は、AAAモデルという考え方が確立するよりも前に開発されたものである。そのため、RADIUSプロトコルにおいては、認証と承認を区別せず、あわせて「認証」として取り扱っている。実際、RADIUSクライアントは、利用が拒否された理由がパスワードの間違いなのか、権限の不足なのかを知ることができない。

## 共有鍵

UDPは[TCPと異なり](../Page/Transmission_Control_Protocol.md "wikilink")、送信者の詐称、データの改竄を検出することができない。このため、通信相手のIPアドレスだけで通信の内容を信頼することはできない。詐称と改竄を防ぐため、RADIUSクライアントとサーバの間で[共有鍵](../Page/共通鍵暗号.md "wikilink") (Shared secret) と呼ぶ鍵文字列を共有し、パケットの内容と共有鍵から得た[ダイジェスト情報を認証符号および属性値ペアに配置している](../Page/ハッシュ関数.md "wikilink")。共有鍵は、RADIUSクライアントとサーバの組み合わせごとに1個を用意すべきである。RADIUSサーバごとに1個だけ用意し、全てのRADIUSクライアントで同じ共有鍵を使うことは、セキュリティ上の大きなリスクとなる。また、セキュリティの観点から、共有鍵の内容が第三者に漏洩することは大きな問題である。

## プロキシ

RADIUSサーバでありながら、実際の認証とアカウンティングの処理を他のRADIUSサーバに依頼するものを「RADIUS[プロキシ](../Page/プロキシ.md "wikilink")サーバ」と呼ぶ。つまり、RADIUSサーバでありながら、RADIUSクライアントでもある。要求を「転送する」ともいう。

ユーザ名文字列を判断して、要求の転送先を変えることもできる。たとえば、ユーザ名として[電子メール](../Page/電子メール.md "wikilink")アドレスのように「[@](https://ja.wikipedia.org/wiki/アットマーク "wikilink")」マークと[ドメイン名](../Page/ドメイン名.md "wikilink")を含んだ文字列を使用し、ドメイン名の部分の文字列に従って異なるRADIUSサーバに転送することができる。このような技術は、[ISP](https://ja.wikipedia.org/wiki/インターネットサービスプロバイダ "wikilink")（インターネット接続サービスプロバイダ）間の[ローミング](../Page/ローミング.md "wikilink")や、[NTTの](../Page/NTTグループ.md "wikilink")[フレッツ](../Page/フレッツ.md "wikilink")サービスのようなアクセス網提供サービスとISPとの分業など、広く利用されている。上記の例でのドメイン名の部分のように、転送先を判断する根拠とする部分を、一般に「レルム(Realm)」と呼ぶ。

## IEEE 802.1X

[IEEE 802.1Xは](../Page/IEEE_802.1X.md "wikilink")、[LANの利用の可否を制御する](../Page/Local_Area_Network.md "wikilink")、[イーサネット](../Page/イーサネット.md "wikilink")上のプロトコルである。IEEE 802.1Xにおいては、EAPプロトコルとRADIUSプロトコルを利用することによって、RADIUSサーバによって認証された利用者のみに対してLANを利用させることができる。もちろん、このためにはIEEE 802.1Xに対応した無線LANアクセスポイントまたはスイッチが必要である。なお、「802.1x」というように「X」を小文字で記述しても誤りではないが、大文字で記述するのが主流である。これは、小文字の「x」が数学で使う「\(x\)」のように、「xの部分に入る文字を規定しない」という意味に誤解されることを防ぐためである。

IEEE 802.1XおよびRADIUSプロトコルのいずれも、実際の認証手順については規定していない。実際の認証は、[EAP-TLS](https://ja.wikipedia.org/wiki/EAP-TLS "wikilink")、[PEAP](https://ja.wikipedia.org/wiki/PEAP "wikilink")、[EAP-TTLS](https://ja.wikipedia.org/wiki/EAP-TTLS "wikilink")などEAP上の認証手順によって行う。ベンダ独自の認証手順をEAP上に実現することも可能である。EAPによる認証のためのデータのやりとりを、利用者端末とアクセスポイントまたはスイッチの間のイーサネットではEAPoL（EAP over LAN)、アクセスポイントまたはスイッチとRADIUSサーバの間ではRADIUSプロトコルによって中継する。

EAP-TLSは、[TLSに基づいてデジタル証明書による相互認証](../Page/Transport_Layer_Security.md "wikilink")（サービス提供者の詐称をも防止する）を行うという点で重要であるが、デジタル証明書の運用と管理の負担が大きいという点で、一般の事業所等では敬遠される傾向がある。PEAPおよびEAP-TTLSは、TLSによる[暗号](../Page/暗号.md "wikilink")化した通信路を形成したうえでパスワード情報のやりとりを行う認証手順である。EAP-TLS、PEAP・EAP-TTLSの対比は、[ウェブブラウザ](../Page/ウェブブラウザ.md "wikilink")のTLSでデジタル証明書による相互認証を行うのか、SSL上でパスワード認証を行うかの違いを考えるとわかりやすいだろう。

## ソフトウェア

古くから、RADIUSプロトコルの開発者であるLivingston Enterprises社（後にLucent Technologies社に買収された）によるRADIUSサーバの実装と、この実装から派生した実装が多用されてきた。近年では、[オープンソース](../Page/オープンソース.md "wikilink")ソフトウェア、商用ソフトウェアともに、さまざまな実装が存在する。

## 利用事例

  - [インターネット・サービス・プロバイダ](https://ja.wikipedia.org/wiki/インターネット・サービス・プロバイダ "wikilink")
  - アクセス網提供サービス（ネットワークインフラサービス）
  - [携帯電話](../Page/携帯電話.md "wikilink")によるネット接続サービス
  - 無線LAN、VLAN
  - ウェブによる有料コンテンツ提供サービス

## 規定

以下のRFC文書をはじめ、多くのRFCによって規定されている\[1\]。

  - RFC 2865 - Remote Authentication Dial In User Service (RADIUS) <https://tools.ietf.org/html/rfc2865>
  - RFC 2866 - RADIUS Accounting(RADIUS会計) <https://tools.ietf.org/html/rfc2866>
  - RFC 2867 - RADIUS Accounting Modifications for Tunnel Protocol Support(トンネル規約対応RADIUS会計拡張) <https://tools.ietf.org/html/rfc2867>
  - RFC 2868 - RADIUS Attributes for Tunnel Protocol Support(トンネル規約対応RADIUS属性) <https://tools.ietf.org/html/rfc2868>
  - RFC 2869 - RADIUS Extensions(RADIUS拡張) <https://tools.ietf.org/html/rfc2869>
  - RFC 3162 - RADIUS and IPv6(IPv6とRADIUS) <https://tools.ietf.org/html/rfc3162>
  - RFC 3575 - IANA Considerations for RADIUS(Remote Authentication Dial In User Service) <https://tools.ietf.org/html/rfc3575>
  - RFC 3579 - RADIUS (Remote Authentication Dial In User Service) Support For Extensible Authentication Protocol (EAP)RADIUSプロトコルでのEAP (RFC 2284) の使用 <https://tools.ietf.org/html/rfc3579>
  - RFC 3580 - IEEE 802.1X Remote Authentication Dial In User Service (RADIUS) Usage Guidelines(IEEE 802.1XでのRADIUS利用ガイドライン) <https://tools.ietf.org/html/rfc3580>
  - RFC 4072 - Diameter Extensible Authentication Protocol (EAP) Application <https://tools.ietf.org/html/rfc4072>
  - RFC 5080 - Common Remote Authentication Dial In User Service (RADIUS) Implementation Issues and Suggested Fixes <https://tools.ietf.org/html/rfc5080>
  - RFC 5997 - Use of Status-Server Packets in the Remote Authentication Dial In User Service (RADIUS) Protocol <https://tools.ietf.org/html/rfc5997>
  - RFC 6158 - RADIUS Design Guidelines <https://tools.ietf.org/html/rfc6158>
  - RFC 6572 RADIUS Support for Proxy Mobile IPv6 <https://tools.ietf.org/html/rfc6572>
  - RFC 6929 - Remote Authentication Dial-In User Service (RADIUS) Protocol Extensions <https://tools.ietf.org/html/rfc6929>
  - RFC 7268 - RADIUS Attributes for IEEE 802 Networks <https://tools.ietf.org/html/rfc7268>
  - RFC 8044 - Data Types in RADIUS <https://tools.ietf.org/html/rfc8044>

## 脚注

## 関連項目

  - [DIAMETER](https://ja.wikipedia.org/wiki/DIAMETER "wikilink")

## 外部リンク

  - [IEEE 802.1X](http://standards.ieee.org/getieee802/download/802.1X-2001.pdf)

<!-- end list -->

  -
    *Copyright (c) 2004 by Accense Technology, Inc.*
    *Permission is granted to copy, distribute and/or modify this document under the terms of the GNU Free Documentation License Version 1.1 published by the Free Software Foundation.*
    *この文書をGNU Free Documentation License Version 1.1に規定された条件のもとで、複製、配布、変更することを許諾します。*

[Category:認証プロトコル](https://ja.wikipedia.org/wiki/Category:認証プロトコル "wikilink") [Category:コンピュータ・ネットワーク・セキュリティ](https://ja.wikipedia.org/wiki/Category:コンピュータ・ネットワーク・セキュリティ "wikilink") [Category:インターネット標準](https://ja.wikipedia.org/wiki/Category:インターネット標準 "wikilink") [Category:RFC](https://ja.wikipedia.org/wiki/Category:RFC "wikilink")

1.  RadiusのRFCを読む。 <https://qiita.com/kaizen_nagoya/items/2d17342b9abfac945a1c>
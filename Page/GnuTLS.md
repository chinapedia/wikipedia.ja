> この記事は[GnuTLS](https://ja.wikipedia.org/wiki/GnuTLS)から翻訳されています。


**GnuTLS**（[GNU](../Page/GNU.md "wikilink") Transport Layer Security; グヌーティーエルエス）は[SSL/TLSと](../Page/Transport_Layer_Security.md "wikilink")[DTLS](https://ja.wikipedia.org/wiki/Datagram_Transport_Layer_Security "wikilink")[プロトコルの](../Page/通信プロトコル.md "wikilink")[フリーなライブラリー実装のひとつである](../Page/フリーソフトウェア.md "wikilink")。アプリケーションがネットワーク通信層を越えて安全な通信プロトコルを利用できるよう[APIを提供することを目的とする](../Page/アプリケーションプログラミングインタフェース.md "wikilink")。GnuTLSには以下の機能がある \[1\]。

  - SSL 3.0、TLS (1.0, 1.1, 1.2, 1.3)、DTLS (1.0, 1.2) プロトコルのサポート

  - [DANE](https://ja.wikipedia.org/wiki/DNS-based_Authentication_of_Named_Entities "wikilink")

  - [OCSP](../Page/Online_Certificate_Status_Protocol.md "wikilink")

  - [RSA暗号](../Page/RSA暗号.md "wikilink")、[楕円曲線暗号](../Page/楕円曲線暗号.md "wikilink")を含む公開鍵アルゴリズム

  - : TLS認証における (Secure remote password、SRP)

  - : TLS認証における (Pre-shared key、PSK)

  - [AES](../Page/Advanced_Encryption_Standard.md "wikilink")、[Camellia](../Page/Camellia.md "wikilink")を含む共通鍵アルゴリズム

  - /dev/cryptoを経由した暗号アクセラレータ

  - [スマートカード](https://ja.wikipedia.org/wiki/スマートカード "wikilink")を含む暗号トークン

  - TLS Extension

  - TLS Compression

  - [X.509](../Page/X.509.md "wikilink")と[OpenPGP](https://ja.wikipedia.org/wiki/OpenPGP "wikilink")の[公開鍵証明書](../Page/公開鍵証明書.md "wikilink")の取扱い

  - 証明書のパス検証

当初はその名の通り[GNU](../Page/GNU.md "wikilink")プロジェクトの一環として開発されていたが、2012年末にGNU傘下から離脱しGNUから独立して開発が行われることになった。\[2\]

GnuTLSは[GNU LGPLのライセンス下にあるが](../Page/GNU_Lesser_General_Public_License.md "wikilink")、いくつかの部分は [GPLのライセンスを受けている](../Page/GNU_General_Public_License.md "wikilink")。

GnuTLSはTLSのようなプロトコルを[GNUプロジェクト](../Page/GNUプロジェクト.md "wikilink")のアプリケーションで扱えるようにすることを目的として作成された。既に[OpenSSL](https://ja.wikipedia.org/wiki/OpenSSL "wikilink")は開発されていたが、OpenSSLのライセンスはGPLに対し非互換\[3\]であるため、GPLの下にあるソフトウェアはOpenSSLを使えなかった。

GnuTLSは[GNOME](../Page/GNOME.md "wikilink")や、[CenterIM](https://ja.wikipedia.org/wiki/CenterIM "wikilink")、[Exim](https://ja.wikipedia.org/wiki/Exim "wikilink")、[Mutt](../Page/Mutt.md "wikilink")、[Slrn](https://ja.wikipedia.org/wiki/Slrn "wikilink")、[Lynx](../Page/Lynx_\(ウェブブラウザ\).md "wikilink")、[CUPS](../Page/Common_Unix_Printing_System.md "wikilink")\[[http://www.gnu.org/software/gnutls/programs.html\]で用いられている](http://www.gnu.org/software/gnutls/programs.html%5Dで用いられている)。

## 脚注

<references/>

## 関連項目

  - [Transport Layer Security](../Page/Transport_Layer_Security.md "wikilink")
  - [TLS実装の比較](https://ja.wikipedia.org/wiki/TLS実装の比較 "wikilink")

## 外部リンク

  -
  - [GnuTLSの開発者であるNikos Mavroyanopoulosのインタビュー（2003年）](http://www.network-theory.co.uk/articles/mavroyanopoulus.html)

[Category:GNUプロジェクト](https://ja.wikipedia.org/wiki/Category:GNUプロジェクト "wikilink") [Category:ライブラリ_(プログラミング)](https://ja.wikipedia.org/wiki/Category:ライブラリ_\(プログラミング\) "wikilink") [Category:Transport_Layer_Security](https://ja.wikipedia.org/wiki/Category:Transport_Layer_Security "wikilink") [Category:オープンソースソフトウェア](https://ja.wikipedia.org/wiki/Category:オープンソースソフトウェア "wikilink")

1.
2.
3.
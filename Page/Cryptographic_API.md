> この記事は[Cryptographic API](https://ja.wikipedia.org/wiki/Cryptographic_API)から翻訳されています。


**Cryptographic API**（**CryptoAPI**、**CAPI**）は、[Microsoft Windows](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink") [オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink")の[APIの](../Page/アプリケーションプログラミングインタフェース.md "wikilink")1つであり、Windows での[暗号](../Page/暗号.md "wikilink")を使ったセキュアなアプリケーション開発のためのサービスを提供する。一種の[抽象化レイヤー](../Page/抽象化レイヤー.md "wikilink")を提供する一連の[ダイナミックリンクライブラリ](../Page/ダイナミックリンクライブラリ.md "wikilink")で構成され、データの暗号化を行うコードをアプリケーションから分離する。

CryptoAPI は[公開鍵暗号](../Page/公開鍵暗号.md "wikilink")と[共通鍵暗号](../Page/共通鍵暗号.md "wikilink")をサポートしている。データの暗号化/復号機能、[公開鍵証明書](https://ja.wikipedia.org/wiki/公開鍵証明書 "wikilink")を使った[認証](../Page/認証.md "wikilink")機能を含む。また、[暗号論的擬似乱数生成器](../Page/暗号論的擬似乱数生成器.md "wikilink")関数 [CryptGenRandom](https://ja.wikipedia.org/wiki/:en:CryptGenRandom "wikilink") も含まれる。

CryptoAPI はマシン上にインストールされた CSP ([Cryptographic Service Provider](https://ja.wikipedia.org/wiki/Cryptographic_Service_Provider "wikilink")）を使って動作する。CSP は実際のデータの暗号化/復号を行うモジュールである。

[Windows Vista](https://ja.wikipedia.org/wiki/Microsoft_Windows_Vista "wikilink") では、CryptoAPI が **Cryptography API: Next Generation (CNG)** に更新された。使える暗号化アルゴリズムが増え、[アメリカ国家安全保障局](../Page/アメリカ国家安全保障局.md "wikilink") (NSA) [Suite B](http://web.archive.org/20051128182632/www.nsa.gov/ia/industry/crypto_suite_b.cfm) の一部の新しいアルゴリズムを含んでいる。また、プラグイン形式で独自暗号APIを追加できる柔軟性を備えている。CNG は[カーネルモード](https://ja.wikipedia.org/wiki/カーネルモード "wikilink")でも[ユーザーモード](https://ja.wikipedia.org/wiki/ユーザーモード "wikilink")でも動作し、従来の CryptoAPI での全アルゴリズムをサポートしている。CNG を実装したマイクロソフト製プロバイダは Bcrypt.dll にある。

CNG はRSAよりも短い鍵でセキュアな[楕円曲線暗号](../Page/楕円曲線暗号.md "wikilink")もサポートしている[1](http://msdn.microsoft.com/en-us/library/aa375534.aspx)。CNG API は、Base Smart Card Cryptographic Service Provider (Base CSP) モジュールを使うことで[ICカード](../Page/ICカード.md "wikilink")用のAPIも提供する。

## 関連項目

  - [公開鍵暗号](../Page/公開鍵暗号.md "wikilink")

## 外部リンク

  - [Cryptography Reference](http://msdn2.microsoft.com/en-us/library/aa380256.aspx) on MSDN

[Category:セキュリティソフト](https://ja.wikipedia.org/wiki/Category:セキュリティソフト "wikilink") [Category:マイクロソフトのAPI](https://ja.wikipedia.org/wiki/Category:マイクロソフトのAPI "wikilink")
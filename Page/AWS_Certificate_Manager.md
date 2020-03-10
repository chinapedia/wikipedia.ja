> この記事は[AWS Certificate Manager](https://ja.wikipedia.org/wiki/AWS_Certificate_Manager)から翻訳されています。


**AWS Certificate Manager**（略称はACM）は、[Amazon Web Services](https://ja.wikipedia.org/wiki/Amazon_Web_Services "wikilink")(AWS) のサービスの一つ。AWS利用者が、[TLS用の](../Page/Transport_Layer_Security.md "wikilink")[公開鍵証明書](../Page/公開鍵証明書.md "wikilink")を無償で利用することができる機能等を提供する\[1\]\[2\]。

## 概要

2016年1月にサービス開始\[3\]。

AWSのいくつかのサービス・機能（Elastic Load Balancer、Amazon CloudFront ディストリビューションや Amazon API Gateway の API）とACMは統合させることが可能であり、統合により利用者は容易にパブリック証明書を用いることができる\[4\]。

ACM自身が[認証局](../Page/認証局.md "wikilink")となり証明書を発行する方式ほかに、他の認証局が発行した証明書を持ち込む（インポート）こともできる。また、ACMが発行する証明書は、インターネット上のリソースを特定するための「**パブリック証明書**」ならびにそれ以外の「**プライベート証明書**」がある。ACMにプライベート証明書を発行させるために、大前提としてユーザはACM上で「**プライベートCA**」を作成することとなる\[5\]。

## 出典

[Category:認証局](https://ja.wikipedia.org/wiki/Category:認証局 "wikilink") [Category:Amazon.com](https://ja.wikipedia.org/wiki/Category:Amazon.com "wikilink")

1.  <https://www.atmarkit.co.jp/ait/articles/1601/26/news054.html> (web.archive.orgにアーカイブが存在)
2.  <https://cloud.watch.impress.co.jp/docs/news/758027.html> (web.archive.orgにアーカイブが存在)
3.
4.  <https://aws.amazon.com/jp/certificate-manager/features/> (web.archive.orgにアーカイブが存在)
5.
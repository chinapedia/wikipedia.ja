> この記事は[Web Services Interoperability](https://ja.wikipedia.org/wiki/Web_Services_Interoperability)から翻訳されています。


**Web Services Interoperability**（**WS-I**）は、[Webサービス](https://ja.wikipedia.org/wiki/Webサービス "wikilink")仕様の相互運用を促進することを目的として2002年に結成された業界団体（[コンソーシアム](../Page/コンソーシアム.md "wikilink")）。

創立メンバー（[IBM](../Page/IBM.md "wikilink")、[マイクロソフト](../Page/マイクロソフト.md "wikilink")、[BEAシステムズ](../Page/BEAシステムズ.md "wikilink")、[SAP](https://ja.wikipedia.org/wiki/SAP "wikilink")、[オラクル](https://ja.wikipedia.org/wiki/オラクル_\(企業\) "wikilink")、[富士通](../Page/富士通.md "wikilink")、[ヒューレット・パッカード](../Page/ヒューレット・パッカード.md "wikilink")、[インテル](https://ja.wikipedia.org/wiki/インテル "wikilink")）と2者の選抜メンバー（現在は[サン・マイクロシステムズ](../Page/サン・マイクロシステムズ.md "wikilink")と webMethods）からなる運営委員会によって運営されていた。

2011年からはOSAISのWS-Iメンバーセクションとして活動。2017年12月に活動を終了した。\[1\]

成果物としては、[プロファイル](https://ja.wikipedia.org/wiki/プロファイル_\(工学\) "wikilink")、そのプロファイルを使ったサンプルアプリケーション、プロファイル準拠状況を確認するためのテストツール、がある。

## WS-I プロファイル

WS-I によれば、プロファイルとは、

> 一連のWebサービス仕様であり、相互運用可能なWebサービスを実装可能とするために、どのように仕様を使うかを示した相互運用と実装のガイドラインを備えたもの。

である。以下のようなプロファイルがある。

  - [WS-I Basic Profile](https://ja.wikipedia.org/wiki/WS-I_Basic_Profile "wikilink")
  - WS-I Basic Security Profile
  - Simple Soap Binding Profile

## WS-I テストツール

WS-I は2004年に2つのテストツールを発行した。

  - [SOAPメッセージをインターセプトするモニターと](../Page/SOAP_\(プロトコル\).md "wikilink")、そのためにテスト中に使われるHTTPヘッダ。この機能は、[中間者の原理を使うことで保証される](https://ja.wikipedia.org/wiki/中間者攻撃 "wikilink")。
  - Webサービスの生成物について、プロファイル準拠状況を分析するよう設計されたアナライザ。プロファイルは Test Assertion Document (\*.TAD) ファイルで選択される。分析対象としては以下のものがある。
      - Webサービス記述ファイル。[WSDLファイルなど](https://ja.wikipedia.org/wiki/Web_Services_Description_Language "wikilink")。
      - Webサービス検索サービス。[UDDI](https://ja.wikipedia.org/wiki/UDDI "wikilink")エントリなど。
      - テストセッションで交換され、テストツールによって収集されるメッセージと対応するエンベロープ。

これらのテストツールは完全な認証ツールとして設計されたものではない。テストツールにバンドルされているユーザーガイド (*WS-I Testing Tools version 1.1 User Guide*) に記述されているように\[2\]、プロファイル準拠のインジケータとしてのみ利用できる。

> **問**: テストツールはWebサービスがプロファイルに準拠していることを保証できますか?
> **答**: ツールはテスト中にWebサービスが生成するものの準拠状況を確認できるだけです。それはWebサービスの定義 (WSDL) であったり、実行時のWebサービスの振る舞いの観測結果だったりします。Webサービスのあらゆる振る舞いをテストすることは、そのWebサービスのアプリケーションレベルの詳細を理解している必要があるため、非常に困難です。このため、WS-I テスティング・ワーキンググループでは認証規準を提供しません。

> 従ってこのテストツールは、Webサービスの生成物に基づいた、選択されたプロファイルへの準拠のインジケータとなります。そして、同じプロファイルに準拠することをテストしたビジネスパートナーとの相互運用性のインジケータにもなります。

## WS-I プロファイルのコンプライアンス

WS-I は認証機関ではないので、各ベンダーは独自にプロファイル準拠であることを主張できる。ただし、各ベンダーは準拠を主張する前にテストツールを使うことを要求される。\[3\]

2003年のインタビューで、WS-Iのスポークスマンは、各社は不誠実に準拠を主張することも可能だが、それぞれ誠実に行動することを期待しているとして、次のように述べた。

> 「我々はブランドが市場主導で形成されることを期待している。我々は誰も嘘の主張をしていると言われる最初の企業になりたくないと思っているだろうと考えている」 \[4\]

## 関連項目

  - [WSRF](https://ja.wikipedia.org/wiki/Web_Services_Resource_Framework "wikilink")

## 脚注

## 外部リンク

  - [WS-I Home Page](http://www.ws-i.org/)

[Category:World_Wide_Web](https://ja.wikipedia.org/wiki/Category:World_Wide_Web "wikilink") [Category:ソフトウェアアーキテクチャ](https://ja.wikipedia.org/wiki/Category:ソフトウェアアーキテクチャ "wikilink")

1.   OASIS|url=[https://www.oasis-open.org/news/pr/oasis-announces-successful-completion-of-web-services-interoperability-ws-i-member-section|website=www.oasis-open.org|accessdate=2019-04-22](https://www.oasis-open.org/news/pr/oasis-announces-successful-completion-of-web-services-interoperability-ws-i-member-section%7Cwebsite=www.oasis-open.org%7Caccessdate=2019-04-22)}}
2.  [Deliverables from the Testing Tools Working Group](http://www.ws-i.org/deliverables/workinggroup.aspx?wg=testingtools) WS-I
3.  詳しくは [こちらの文書（WS-I Trademark and Compliance Claim Requirements）](http://www.ws-i.org/docs/20031021_trademark.pdf)を参照。
4.  [WS-I Publishes Basic Profile 1.0](http://www.internetnews.com/dev-news/article.php/2247551) internetnews.com、2003年8月12日
> この記事は[Enterprise application integration](https://ja.wikipedia.org/wiki/Enterprise_application_integration)から翻訳されています。


**Enterprise Application Integration**（以下、**EAI**）とは、企業内における多種多様な[コンピュータ](../Page/コンピュータ.md "wikilink")システム群や各種ビジネス[パッケージ](../Page/パッケージ.md "wikilink")群を有機的に連携/統合（例えば、営業支援サービスと財務システム、顧客管理システムを連携させ、[CRMシステムの機能を拡充させるなど](../Page/顧客関係管理.md "wikilink")）させ再構築し、より戦略的な機能や情報として提供する機能及び[ミドルウェア](../Page/ミドルウェア.md "wikilink") / [アプリケーションパッケージや統合技術のこと](../Page/アプリケーションソフトウェア.md "wikilink")。 基幹システムと電子商取引システムの接続\[1\]や、企業間の合併に伴うシステム統合手段としても活用される。

## 歴史と概要

EAIが提唱され始めたのは、1990年代終盤であり、この頃にトレンドだった[TPモニター技術や](../Page/トランザクションモニター.md "wikilink")[サーバ](../Page/サーバ.md "wikilink")間[メッセージキュー](../Page/メッセージキュー.md "wikilink")イング及び、まだ十分な機能を提供できない[WebAPサーバなどを連携してシステムを構築する事が多かった](../Page/アプリケーションサーバ.md "wikilink")。また、当時の通信ベースでトレンドであった[CORBA](https://ja.wikipedia.org/wiki/CORBA "wikilink")や[MQ](https://ja.wikipedia.org/wiki/MQ "wikilink")なども、実装するには大きな費用が必要であり、当然、対象となるシステムも大きな作り込みを必要とし、比較的大規模なものが多く、EAIにより新設されるサービスの利用者数も大きな設定となっていた。このため、EAIの共通キーワードとして、個々のシステムを有機的に結びつけるEAIパッケージを載せるサーバをハブサーバと称し、高度な機能と高性能を持つUNIXサーバの最上機種を使用する事も多かった。

このような特性から、EAI開発の費用や提供価格も嵩み、導入に至るケースが非常に少なかった。日本国内においても提供サービスにEAIを載せるIT企業群も多かったが、実際のシステム提供まで至る案件数は大企業に限られたため非常に少なく、言葉自体も立ち消えとなりつつあった。

しかし、インターネットやイントラネットの発展によりシステム同士を繋いで自動化するニーズが企業側から顕在化するにいたり、インターネット標準技術を使用した製品が開発され普及を始めた。また、技術的にも[XMLや](../Page/Extensible_Markup_Language.md "wikilink")[RSS](../Page/RSS.md "wikilink")といったインターネット技術や、[オープンソース](../Page/オープンソース.md "wikilink")製品や[Struts](https://ja.wikipedia.org/wiki/Struts "wikilink")や[Ruby on Railsなどのオープンな](../Page/Ruby_on_Rails.md "wikilink")[フレームワーク](https://ja.wikipedia.org/wiki/フレームワーク "wikilink")による各種機能部品が簡単に入手できるようになり、Web間のシステム連携が普通のことになり出した2000年代中盤において、機能的に反復使用されるような部品的な機能の集合としてEAI製品が活用され、個々の部門サーバなどに導入されるようになってきている。

さらに近年では、[Webサービス](../Page/Webサービス.md "wikilink")を技術基盤とした[ESB](https://ja.wikipedia.org/wiki/ESB "wikilink") (Enterprise Service Bus) という手法によりアプリケーション統合も普及を始め、各種EAI製品は、ESB機能を組み込み始めており、製品カテゴリとしてEAIとESBの区別は消滅しつつある。

## 主な製品

  - ActiveMatrix BusinessWorks（[TIBCO Software](https://www.nttcoms.com/service/TIBCO/)）
  - AquaLogic Integration Server（[日本オラクル](../Page/日本オラクル.md "wikilink")）
  - ASTERIA（[インフォテリア](https://ja.wikipedia.org/wiki/インフォテリア "wikilink")）
  - BizTalk Server（[マイクロソフト](../Page/マイクロソフト.md "wikilink")）
  - DataSpider Servista（アプレッソ）
  - eGate Integrator（[サン・マイクロシステムズ](../Page/サン・マイクロシステムズ.md "wikilink")）
  - Netweaver XI（[SAP](https://ja.wikipedia.org/wiki/SAP "wikilink")）
  - webMethods Enterprise Service Bus（[ソフトウェア・エー・ジー](https://ja.wikipedia.org/wiki/ソフトウェア・エー・ジー "wikilink")）
  - Websphere Enterprise Service Bus（[日本アイ・ビー・エム](../Page/日本アイ・ビー・エム.md "wikilink")）
  - Fiorano SOA Platform（[フィオラノ ソフトウェア](http://find-it.jp/se/product/index.html?productId=8373)）
  - [Guaraná DSL](http://www.tdg-seville.info/rzfrantz/Guaran%c3%a1+DSL)

## 脚注

## 関連項目

  - [アプリケーションソフトウェア](../Page/アプリケーションソフトウェア.md "wikilink")
  - [ミドルウェア](../Page/ミドルウェア.md "wikilink") - [メッセージ指向ミドルウェア](../Page/メッセージ指向ミドルウェア.md "wikilink")
  - [パッケージソフトウェア](../Page/パッケージソフトウェア.md "wikilink")
  - [ダウンサイジング](../Page/ダウンサイジング.md "wikilink")

[Category:システムソフトウェア](https://ja.wikipedia.org/wiki/Category:システムソフトウェア "wikilink")

1.  株式会社エクス コラム 「[社内のデータが”つながる”EAIツールとは](https://xeex-products.jp/extelligence/eai-tool/)」　2017年12月19日閲覧
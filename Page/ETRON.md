> この記事は[ETRON](https://ja.wikipedia.org/wiki/ETRON)から翻訳されています。


**eTRON**（イートロン、**Entity and Economy TRON**）とは、[貨幣](../Page/貨幣.md "wikilink")や各種証書、[証券](../Page/証券.md "wikilink")、チケットなどの価値情報を[インターネット](../Page/インターネット.md "wikilink")などのオープンな通信基盤上で、安全に流通させるための広域分散システム[アーキテクチャ](../Page/アーキテクチャ.md "wikilink")である。

特定の[暗号](../Page/暗号.md "wikilink")、[ハッシュ](https://ja.wikipedia.org/wiki/ハッシュ "wikilink")、認証方式などのアルゴリズムや特定のアプリケーションに依存しない、汎用的な枠組みを提供するものである。

## アーキテクチャ

eTRONアーキテクチャは以下の要素から構成される。

### eTRONノード

eTRONアーキテクチャ内で有効なユニークな128bit長の識別子 (eTRON ID) を持ち、価値情報を保持、操作を行う。eTRONコンテンツホルダとeTRONサービスクライアントの2つがある。この2つの機能を同時に有するノードもある。

  - eTRONコンテンツホルダ
      -
        価値情報を安全に格納するもの。実装方法に応じて、[ICカード](../Page/ICカード.md "wikilink")型のeTRONカード、携帯端末に埋め込むためのeTRONチップ、据え置き型のeTRONボックスなどがある。
  - eTRONサービスクライアント
      -
        eTRONコンテンツホルダに格納する価値情報を発行、回収、変更、譲渡などの操作を行う。

### エンティティ転送プロトコル

Entity Transfer Protocol、eTPとも呼ばれる。eTRONサービスクライアントがeTRONコンテンツホルダ内の価値情報を安全に操作するためのセッション層[プロトコル](../Page/プロトコル.md "wikilink")。

### eTP基盤

eTRONコンテンツホルダとeTRONサービスクライアントの間をeTPで通信するメカニズムを提供する。

  - eTRON暗号認証基盤 (eTRON Authentication/Encryption Infrastructure, AEI)
      -
        eTRONアーキテクチャが認証や暗号の処理を行うときに用いられるPKIである。
  - eTRON応用ネットワーク基盤 (eTRON Application Network Infrastructure, ANI)
      -
        eTRONアーキテクチャを使って、価値情報を扱うユーザサービスを提供する、サービス依存ネットワーク基盤システム。

### eTRONチップ

eTRONノードを構成する価値情報を格納するセキュリティチップ。を持ったハードウェアが想定されている。

## 特徴

eTRONは以下の特徴をもつ。

  - 分散環境ノード
      -
        セッション層のeTPをサポートし、ネットワーク上のサーバや他のeTRONカードと、eTP基盤のネットワークを介してeTPでPeer-to-Peer通信を行う。
  - eTRON IDで特定する相互認証方式
      -
        eTRONチップはユニークな識別子 (eTRON ID) を持つ。eTRONチップと通信セッションを構築する際には相互認証がなされ、相互にeTRON IDが把握される。このeTRON IDの正当性の確認は、eTRONカードに与えられたAEIの認証局が付与した証明書とその署名を確認することでなされる。
  - eTRON IDに基づいたアクセス制御リスト方式による統合的な資源保護機構
      -
        eTRONチップにはチップ固有のeTRON IDが割り振られており、相互認証によって通信相手を識別できる。eTRON IDに基づいたアクセス制御リストを提供する。このアクセス制御リストを用いて、eTRONチップ内の資源へのアクセスを限定し、価値情報を保護する。
  - 転々流通のためのチップ間通信
      -
        サーバを介さず、eTRONノード間で直接価値情報を交換できる。
  - ロールバック可能なトランザクション機構
      -
        価値情報の作成、削除を安全に行えるために、トランザクション機構を持つ。

## 関連項目

  - [TRONプロジェクト](../Page/TRONプロジェクト.md "wikilink")

## 外部リンク

  - [Ubiquitous ID Center](http://www.uidcenter.org/japanese.html)
  - [T-Engineフォーラム](http://www.t-engine.org/japanese.html)

[Category:TRONプロジェクト](https://ja.wikipedia.org/wiki/Category:TRONプロジェクト "wikilink") [Category:コンピュータアーキテクチャ](https://ja.wikipedia.org/wiki/Category:コンピュータアーキテクチャ "wikilink")
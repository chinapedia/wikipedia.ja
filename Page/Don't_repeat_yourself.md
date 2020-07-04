> この記事は[Don\'t repeat yourself](https://ja.wikipedia.org/wiki/Don\'t_repeat_yourself)から翻訳されています。


**Don't repeat yourself** (DRY) あるいはは、特に[コンピューティング](../Page/コンピューティング.md "wikilink")の領域で、重複を防ぐ考え方である。この哲学は、[情報](https://ja.wikipedia.org/wiki/情報 "wikilink")の重複は変更の困難さを増大し透明性を減少させ、不一致を生じる可能性につながるため、重複するべきでないことを強調する。

DRY は、 と  の著書 ** (邦題:達人プログラマー) において中心となる原則である。 彼らはこの原則を、[データベース](../Page/データベース.md "wikilink")スキーマ、[テスト計画](https://ja.wikipedia.org/wiki/:en:test_plan "wikilink")、[ビルドシステムや](https://ja.wikipedia.org/wiki/ビルド_\(ソフトウェア\) "wikilink")、[ドキュメンテーションにいたるまで非常に幅広く適用している](../Page/ソフトウェアドキュメンテーション.md "wikilink") \[1\]。

DRY 原則がうまく適用されたとき、システムに対するいかなる要素の変更も、論理的に関連のない他の要素の変更にはつながらない。さらに、論理的に関連した要素は予測できる形で統一的に変更され、したがってそれらの変更は[同期](../Page/同期.md "wikilink")が取れたものとなる。

## Once and Only Once 原則との対比

DRY はアプリケーションに必要な情報（通例は設定情報）に対して言及しているという点で **Once and Only Once** (OAOO) 原則とは区別される。比較すると OAOO はコードの機能的な振る舞いについて言及しており、[構造体](../Page/構造体.md "wikilink")や[オブジェクト指向言語における](../Page/オブジェクト指向プログラミング.md "wikilink")[継承の実現が必要な理由となっている](../Page/継承_\(プログラミング\).md "wikilink")。

たとえば、DRY はファイルの集合の場所はアプリケーションの中で一箇所に格納されるべきと主張するが、これらのファイルからデータを取り出す処理をアプリケーションの異なる箇所で記述する回数については寛容である。OAOO の原則は、これに対して、ファイルからデータを取得するコードは一度のみ書かれるよう求めるが、アプリケーション内でこれらのファイルを配置する場所が何箇所あるかについては寛容である。

さらに混乱を招きやすいのは、アプリケーションの中で[オブジェクトは変数として格納され](../Page/オブジェクト_\(プログラミング\).md "wikilink")、オブジェクトは情報の一部として見られる点であり、それゆえに DRY はオブジェクトに対して適用される([インスタンスを一つだけ持つ](../Page/オブジェクト_\(プログラミング\).md "wikilink")) のに対して、OAOO は[クラスに対して適用される](../Page/クラス_\(コンピュータ\).md "wikilink")。(アプリケーション内で、オブジェクトのクラス[テンプレートに同じ目的を持つほかのコードがない](../Page/テンプレート_\(プログラミング\).md "wikilink"))という点である。

## DRY 原則が有用でない場合

  -
  - 小規模のコンテキストでは、DRY に基づき設計する労力は、二つの別々のデータのコピーを維持管理する労力よりはるかに大きくなる。

  - DRY 原則を厳守するような標準の強要は、[wikiなどのコミュニティの参加に高い価値があるようなコンテキストでは](../Page/ウィキ.md "wikilink")、コミュニティの参加を阻害してしまう。

  - [構成管理](../Page/構成管理.md "wikilink")と[バージョン管理は](../Page/バージョン管理システム.md "wikilink")、DRY 原則を逸脱することなく同じコードのコピーを許容する。たとえば、良い例として開発用の環境、[テスト用の環境](../Page/ソフトウェアテスト.md "wikilink")、製品版コード用の環境を構築し、進行中の開発とテストが製品のコードに影響を与えないようにする方法がある。

  - 人間が読むことができる文書(コードのコメントから印刷されたマニュアルまで)は、通常はコードの内部まで読んで理解する能力や時間がない人のための推敲、説明を加えてコードの内部にあるものを再度記述している。しかし、DRY では、人間が読むことができるドキュメントはフォーマットの変更を除けば何の価値もなく、すなわち記述されるのではなく生成されるべきとしている。

  - [ソースコードの生成](../Page/自動プログラミング.md "wikilink") - 重複の禁止はソースコード生成には役立つが、それは出力結果に対してではなく、重複した情報が人間や他のコードによって変更されない場合のみである。

  - [単体テスト](../Page/単体テスト.md "wikilink") - ソースコードとの矛盾を見つけ出すのが目的であり\[2\]、ソースコードから自動生成すべきではない。ただし、ソースコメントやドキュメントから自動生成する事はありうる。\[3\]

  - Abel Avramは、DRYを過度に追求する事で[疎結合の原則が破られる例を示し](../Page/結合度.md "wikilink")、DRYはあくまで他の原則との兼ね合いの元で守られるべきだと述べている。\[4\]

## 関連項目

  - [コードの再利用](https://ja.wikipedia.org/wiki/コードの再利用 "wikilink")
  - [関係の正規化](https://ja.wikipedia.org/wiki/関係の正規化 "wikilink")
  - [KISS原則](https://ja.wikipedia.org/wiki/KISS原則 "wikilink")
  - [関心の分離](../Page/関心の分離.md "wikilink")
  - [トランザクション処理](../Page/トランザクション処理.md "wikilink")（内部情報の不一致を防ぐための方法論が関連）
  - [YAGNI](https://ja.wikipedia.org/wiki/YAGNI "wikilink")
  - [重複コード](../Page/重複コード.md "wikilink")

## 参考文献

## 外部リンク

  - [Orthogonality and the DRY Principle](http://www.artima.com/intv/dry.html)
  - [List of Pragmatic Programmer rules](http://www.pragmaticprogrammer.com/ppbook/extracts/rule_list.html)
  - [c2.com the original](http://c2.com/cgi/wiki?DontRepeatYourself)
  - [Once and Only Once (c2.com)](http://c2.com/cgi/wiki?OnceAndOnlyOnce)

[Category:プログラミングパラダイム](https://ja.wikipedia.org/wiki/Category:プログラミングパラダイム "wikilink") [Category:プログラミング原則](https://ja.wikipedia.org/wiki/Category:プログラミング原則 "wikilink") [Category:ソフトウェア工学のフォークロア](https://ja.wikipedia.org/wiki/Category:ソフトウェア工学のフォークロア "wikilink") [Category:プログラミング・フォークロア](https://ja.wikipedia.org/wiki/Category:プログラミング・フォークロア "wikilink")

1.
2.
3.
4.
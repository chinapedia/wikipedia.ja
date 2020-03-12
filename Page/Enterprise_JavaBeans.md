> この記事は[Enterprise JavaBeans](https://ja.wikipedia.org/wiki/Enterprise_JavaBeans)から翻訳されています。


**Enterprise JavaBeans** (**EJB**) とは、[JavaBeans](../Page/JavaBeans.md "wikilink")仕様と同様のものを、[ネットワーク分散型ビジネスアプリケーションのサーバサイドで実現した](../Page/分散コンピューティング.md "wikilink")[仕様](../Page/仕様.md "wikilink")のこと。[セキュリティ機能などを備える](../Page/コンピュータセキュリティ.md "wikilink")。[Sunが](../Page/サン・マイクロシステムズ.md "wikilink")[JavaEE仕様の中で](../Page/Java_Platform,_Enterprise_Edition.md "wikilink")[ビジネスロジック](../Page/ビジネスロジック.md "wikilink")をモデル化およびデータの[永続化のために作成した](../Page/永続性.md "wikilink")。[データベース](../Page/データベース.md "wikilink")やアプリケーションサーバーなどで実装されている。

## 歴史

EJBは元々、[OMGの](../Page/Object_Management_Group.md "wikilink")[CORBAやSunの](../Page/Common_Object_Request_Broker_Architecture.md "wikilink")[RMIといった分散オブジェクトに由来する技術であり](../Page/Java_Remote_Method_Invocation.md "wikilink")、RMIをベースにビジネスロジックを実装するコンポーネントとして誕生した。最初の実装は[Java](https://ja.wikipedia.org/wiki/Java "wikilink")の誕生から3年後の[1998年](https://ja.wikipedia.org/wiki/1998年 "wikilink")頃に登場している。こうした経緯から、当初策定されたEJBはリモートアクセスを想定した複雑な実装が必須となっており、デプロイメント記述子と呼ばれるXMLの設定ファイルもかかせないものだった。また、EJB 1.0では主要な要素としてセッションBeanのみが定義されており、エンティティBeanはオプションという扱いであった。[2003年](../Page/2003年.md "wikilink")のJ2EE 1.4で定義されたEJB 2.0では、EJBが分散オブジェクトとして使われることは稀であるという実情を踏まえ、ローカルインタフェースの追加が行われている。またメッセージ駆動型Beanが仕様に組み込まれた。\[1\]

しかしEJBの仕様は依然複雑なものであり、EJBに代わってより軽量な[Spring Frameworkや](https://ja.wikipedia.org/wiki/Spring_Framework "wikilink")[POJOといった考え方を用いる動きが活発化する](../Page/Plain_Old_Java_Object.md "wikilink")。こうした流れを受け、[2007年](../Page/2007年.md "wikilink")のJava EE 5で定義されたEJB 3.0では、[DIやPOJOといった考え方を取り入れる形で仕様の全面的な見直しが行われる](../Page/依存性の注入.md "wikilink")。EJBの各クラスは単なるPOJOとなり、J2SE 5.0で導入された[アノテーション](../Page/アノテーション.md "wikilink")によりEJBとしての宣言を行う形式とされた。設定ファイルも不要となり、エンティティBeanは独立した永続化フレームワークである[Java Persistence APIに置き換えられた](../Page/Java_Persistence_API.md "wikilink")。\[2\]

その後も改良は続けられており、[2009年](../Page/2009年.md "wikilink")のJava EE 6で定義されたEJB 3.1では、シングルトンセッションBeanの追加や、セッションBeanを中心とするコンポーネントのみを抽出したEJB Liteと呼ばれるサブセットの定義が行われており\[3\]、[2013年](../Page/2013年.md "wikilink")のJava EE 7で定義されたEJB 3.2では、非同期処理のEJB Liteへの導入や不要となったエンティティBeanが仕様から取り除かれるなどしている\[4\]。

## EJBの種類

EJBは、大きく以下の三つの種類の[Beansに分けられる](../Page/JavaBeans.md "wikilink")。

  - セッションBean (Session Bean)
    [セッション](../Page/セッション.md "wikilink")を保持し、一時的なロジックを保存する[オブジェクト](https://ja.wikipedia.org/wiki/オブジェクト "wikilink")。以下のような種類がある。
      - ステートフルセッションBean (Stateful Session Bean) : クライアントごとの状態 (State) を保持するセッションBean。
      - ステートレスセッションBean (Stateless Session Bean) : クライアントごとの状態を保持しないセッションBean。
      - シングルトンセッションBean (Singleton Session Bean) : 常に同じインスタンスへのアクセスが保証されている[シングルトンなセッションBean](../Page/Singleton_パターン.md "wikilink")。\[5\]

<!-- end list -->

  - メッセージ駆動型Bean (Message Driven Bean)
    非同期処理の記述など。

<!-- end list -->

  - エンティティBean (Entity Bean)
    永続的なデータを保存するオブジェクト。EJB 3.2で廃止。

## 例

EJBの簡単な例を以下に示す。

``` java
@Stateless
public class CustomerService {

  @PersistenceContext
  private EntityManager entityManager;

  public void addCustomer(Customer customer) {
    entityManager.persist(customer);
  }
}
```

上記のコードは、[O/Rマッピングを使用して顧客](../Page/オブジェクト関係マッピング.md "wikilink") (Customer) オブジェクトを[永続化](../Page/永続性.md "wikilink")（[DBに保存](../Page/データベース.md "wikilink")）するサービスクラス（セッションBean）である。EJBが永続コンテキスト (Persistence context) の管理を行うため、実際にデータを登録するaddCustomer()[メソッドは](../Page/メソッド_\(計算機科学\).md "wikilink")、[デフォルトで](../Page/デフォルト_\(コンピュータ\).md "wikilink")[トランザクション](../Page/トランザクション.md "wikilink")管理された[スレッドセーフ](../Page/スレッドセーフ.md "wikilink")なメソッドとなる。上記のコードは、EJBの[ビジネスロジック](../Page/ビジネスロジック.md "wikilink")と永続化に焦点を当てたもので、EJBの特徴的な機能の数々は使用していない。

こうしたEJBのセッションBeanは、以下のように他のクラスから呼び出して使用することができる。以下はWeb層からの呼び出し例である。

``` java
@Named
@RequestScoped
public class CustomerBacking {
   @EJB
   private CustomerService customerService;

   public String addCustomer(Customer customer) {
      customerService.addCustomer(customer);
      context.addMessage(...); // （省略）メッセージ出力など
      return "customer_overview";
   }
}
```

上記のコードは、EJBのセッションBeanを@EJB[アノテーション](../Page/アノテーション.md "wikilink")により[注入した](../Page/依存性の注入.md "wikilink")、[JavaServer Faces](https://ja.wikipedia.org/wiki/JavaServer_Faces "wikilink") (JSF) の管理Bean (Managed Bean) である。今度のaddCustomer()メソッドは、[UIコンポーネントにおけるボタン操作などを表現している](../Page/ユーザインタフェース.md "wikilink")。EJBのセッションBeanとは逆に、この管理Beanにはビジネスロジックに関するコードも永続化に関するコードも含まれていないが、EJBのコードを呼び出すことでそうした処理を実現している。EJBはプレゼンテーション層に依存せず、それらの役割は管理Beanが担う。

## EJBコンテナ

EJBを管理し、動作させるための実行環境はEJBコンテナと呼ばれる。EJBコンポーネントが動作するときに利用するデータベースへのコネクションやトランザクションの管理も同時に行う。

EJBコンテナの代表例として[JBoss](../Page/JBoss.md "wikilink")などが挙げられる。またJavaEEサーバーはEJBコンテナを含んでいる。

## 脚注

## 関連項目

  - [Java Persistence API](../Page/Java_Persistence_API.md "wikilink")
  - [Spring Framework](https://ja.wikipedia.org/wiki/Spring_Framework "wikilink")

## 外部リンク

  - [JSR 905: Enterprise JavaBeans<small><sup>TM</sup></small> Specification Version 1.1, Errata Sheet, 5/4/2000](http://jcp.org/en/jsr/detail?id=905)
  - [JSR 19: Enterprise JavaBeans<small><sup>TM</sup></small> 2.0](http://jcp.org/en/jsr/detail?id=19)
  - [JSR 153: Enterprise JavaBeans<small><sup>TM</sup></small> 2.1](http://jcp.org/en/jsr/detail?id=153)
  - [JSR 220: Enterprise JavaBeans<small><sup>TM</sup></small> 3.0](http://jcp.org/en/jsr/detail?id=220)
  - [JSR 318: Enterprise JavaBeans<small><sup>TM</sup></small> 3.1](http://jcp.org/en/jsr/detail?id=318)

[Category:Java](https://ja.wikipedia.org/wiki/Category:Java "wikilink") [Category:Java_specification_requests](https://ja.wikipedia.org/wiki/Category:Java_specification_requests "wikilink") [Category:Java_enterprise_platform](https://ja.wikipedia.org/wiki/Category:Java_enterprise_platform "wikilink")

1.
2.
3.
4.
5.
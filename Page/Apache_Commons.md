> この記事は[Apache Commons](https://ja.wikipedia.org/wiki/Apache_Commons)から翻訳されています。


**Apache Commons**（アパッチ コモンズ）は、[Apacheソフトウェア財団](../Page/Apacheソフトウェア財団.md "wikilink")の傘下にある再利用可能なJavaコンポーネントをまとめたApacheのトッププロジェクト。Commonsの目的は再利用可能な[オープンソース](../Page/オープンソース.md "wikilink")[Java](https://ja.wikipedia.org/wiki/Java "wikilink")ソフトウェアを提供することである。Commonsは三つの部分、proper（プロパー）, sandbox（サンドボックス）, dormant（活動休止）から構成されている。

Commonsには[java.lang](https://ja.wikipedia.org/wiki/java.lang "wikilink")パッケージの機能を拡張するLang、Javaの[コレクションフレームワーク](https://ja.wikipedia.org/wiki/コレクションフレームワーク "wikilink")を拡張するクラス群を集めたCollectionsなどがある。

## Commons Proper

The Commons Properは役立つ[Javaコンポーネントを開発維持すること専用に作られている](../Page/Javaプラットフォーム.md "wikilink")。Common Properは[コラボレーション](../Page/コラボレーション.md "wikilink")と[シェアリング](https://ja.wikipedia.org/wiki/シェアリング "wikilink")の役割を持っているが、Jakartaコミュニティの至る所からの[ディベロッパー](https://ja.wikipedia.org/wiki/ディベロッパー "wikilink")がJakartaプロジェクトとJakartaユーザによってシェアされるためにプロジェクトで共に活動できる。

Commonディベロッパーはコンポーネントが他の[ソフトウェアライブラリに最小限に依存することを保証するよう努力する](../Page/ライブラリ.md "wikilink")。それで、これらのコンポーネントは容易に[デプロイ（配備）できる](../Page/ソフトウェアデプロイメント.md "wikilink")。加えて、Commonsコンポーネントは可能な限り[インタフェースを保つ](../Page/インタフェース_\(情報技術\).md "wikilink")。それで、(他のJakartaサブプロジェクトを含む)Jakartaユーザはこれらのコンポーネントを、将来変更される心配無く実装することができる。

[2006年](../Page/2006年.md "wikilink")8月にはこれらはCommons Properでは30以上のプロジェクトになり、5つの一般カテゴリに分類されている。

| コンポーネントカテゴリ | 例                                                                                                                                                                                                                                                                                                                                              |
| ----------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Web関連       | [FileUpload](http://jakarta.apache.org/commons/fileupload), [HTTPClient](http://jakarta.apache.org/commons/httpclient), and [Net](http://jakarta.apache.org/commons/net)                                                                                                                                                                       |
| XML関連       | [Betwixt](http://jakarta.apache.org/commons/betwixt), [Digester](http://jakarta.apache.org/commons/digester), [Jelly](http://jakarta.apache.org/commons/jelly), and [JXPath](http://jakarta.apache.org/commons/jxpath)                                                                                                                         |
| ユーティリティ     | [BeanUtils](http://jakarta.apache.org/commons/beanutils), [Configuration](http://jakarta.apache.org/commons/configuration), [Logging](http://jakarta.apache.org/commons/logging), [DBCP](http://jakarta.apache.org/commons/dbcp), [Pool](http://jakarta.apache.org/commons/pool), and [Validator](http://jakarta.apache.org/commons/validator) |
| パッケージ       | [Codec](http://jakarta.apache.org/commons/codec) and [Modeler](http://jakarta.apache.org/commons/modeler)                                                                                                                                                                                                                                      |
| ありふれたもの     | [CLI](http://jakarta.apache.org/commons/cli), [Discovery](http://jakarta.apache.org/commons/discovery), [Lang](http://jakarta.apache.org/commons/lang), and [Collections](http://jakarta.apache.org/commons/collections)                                                                                                                       |

Commons Proper の一般カテゴリ一覧

*からの表*

### サブプロジェクト

  - BCEL - [Javaバイトコード](https://ja.wikipedia.org/wiki/Javaバイトコード "wikilink")を扱うライブラリ。
  - BeanUtils - [Java Beansをサポート](https://ja.wikipedia.org/wiki/Java_Beans "wikilink")。
  - BSF
  - Chain - [GoF](https://ja.wikipedia.org/wiki/ギャング・オブ・フォー_\(情報工学\) "wikilink")[デザインパターンの一つ](https://ja.wikipedia.org/wiki/デザインパターン_\(ソフトウェア\) "wikilink")、[Chain of Responsibility パターンをサポート](../Page/Chain_of_Responsibility_パターン.md "wikilink")。
  - CLI
  - Codec
  - [Collections](../Page/Apache_Commons_Collections.md "wikilink") - [java.util](https://ja.wikipedia.org/wiki/java.util "wikilink")パッケージにある[コレクションフレームワーク](https://ja.wikipedia.org/wiki/コレクションフレームワーク "wikilink")を拡張するクラス群。
  - Compress - [tar](https://ja.wikipedia.org/wiki/tar "wikilink"), [ZIP](https://ja.wikipedia.org/wiki/ZIP "wikilink"), [bzip2](https://ja.wikipedia.org/wiki/bzip2 "wikilink")をサポート。
  - Configuration - クラスのような設定ファイルを弄るクラス群。
  - CSV
  - Daemon
  - DBCP - [関係データベースの](../Page/関係データベース管理システム.md "wikilink")[コネクションプーリング](https://ja.wikipedia.org/wiki/コネクションプーリング "wikilink")をサポート。
  - [DBUtils](https://ja.wikipedia.org/wiki/Apache_Commons_DBUtils "wikilink") - [JDBC](../Page/JDBC.md "wikilink")をサポートする。
  - Digester
  - Discovery
  - EL
  - [Email](../Page/Apache_Commons_Email.md "wikilink") - [メールライブラリ](../Page/電子メール.md "wikilink")
  - Exec
  - FileUpload - [Java Servlet](../Page/Java_Servlet.md "wikilink")/[JSPでのファイルアップロードをサポート](../Page/JavaServer_Pages.md "wikilink")。
  - [IO](https://ja.wikipedia.org/wiki/Apache_Commons_IO "wikilink") - [java.io](https://ja.wikipedia.org/wiki/java.io "wikilink")パッケージをサポート。
  - JCI
  - Jelly
  - Jexl
  - JXPath
  - [Lang](../Page/Apache_Commons_Lang.md "wikilink") - [java.lang](https://ja.wikipedia.org/wiki/java.lang "wikilink")パッケージを拡張する。StringUtilsほか、, , , [メソッド](https://ja.wikipedia.org/wiki/メソッド "wikilink")の[オーバーライド](../Page/オーバーライド.md "wikilink")を支援するクラスなどが存在する。
  - Launcher
  - Logging - ひとつのプログラムで[Java Logging API](https://ja.wikipedia.org/wiki/Java_Logging_API "wikilink")([java.util.logging](https://ja.wikipedia.org/wiki/java.util.logging "wikilink")パッケージ)や[Jakarta Log4Jを併用し](https://ja.wikipedia.org/wiki/Jakarta_Log4J "wikilink")、簡単に複数の[ロギング](https://ja.wikipedia.org/wiki/ロギング "wikilink")APIを切り替えるときに便利なAPI。
  - [Math](../Page/Apache_Commons_Math.md "wikilink") - クラスや[java.math](https://ja.wikipedia.org/wiki/java.math "wikilink")パッケージにはない数学ライブラリを提供。[複素数](../Page/複素数.md "wikilink")や[行列](https://ja.wikipedia.org/wiki/行列 "wikilink")演算、[統計学](../Page/統計学.md "wikilink")などのライブラリが揃っている。
  - Modeler
  - Net - [java.net](https://ja.wikipedia.org/wiki/java.net "wikilink")パッケージを拡張する。[FTPなどの](../Page/File_Transfer_Protocol.md "wikilink")[プロトコルを扱うことができる](../Page/通信プロトコル.md "wikilink")。
  - Pool - Javaでの[オブジェクトプーリング](https://ja.wikipedia.org/wiki/オブジェクトプーリング "wikilink")をサポート。
  - Primitives
  - Proxy
  - SCXML
  - Validator
  - VFS
  - Weaver

### Commons Lang

Commons Lang には java.lang を拡張した物が入っている。

#### 例1

`Object.equals()` を拡張した物。nullが入っていても比較が可能である。

``` java
String s1 = null;
String s2 = "abc";
if(ObjectUtils.equals(s1, s2)) {
    System.out.println("equal");
}
```

#### 例2

Java のデフォルトの `Object.toString()` はメンバ変数の内容まで表示してくれないが、リフレクションを使用して、メンバ変数の内容を表示する形で、`Object.toString()` を実装する。

``` java
public String toString() {
    return ToStringBuilder.reflectionToString(this);
}
```

### Commons Collections

[Apache Commons Collections](../Page/Apache_Commons_Collections.md "wikilink") には、主に、java.util の Collection 関係の拡張した物が入っている。

#### 例

Java 6 には[クロージャ](../Page/クロージャ.md "wikilink")がないが、`Predicate` を実装することで、条件を満たす物を探すことができる。以下、リストから、a で始まる物を見つけ出す。

``` java
ArrayList<String> list = new ArrayList<String>();
list.add("apple");
list.add("banana");
list.add("ant");
Collection<?> aList = CollectionUtils.select(list, new Predicate() {
    public boolean evaluate(Object obj) {
        return ((String)obj).startsWith("a");
    }
});
```

## Commons Sandbox

The *Commons Sandbox*はJakarta[コントリビュータ](https://ja.wikipedia.org/wiki/コントリビュータ "wikilink")がCommons Properに含まれていないプロジェクトで協業し実験する作業環境である。サンドボックスにあるプロジェクトはCommons Properの推進に関するJakartaのメンバによって支持されており、[ディベロッパー](https://ja.wikipedia.org/wiki/ディベロッパー "wikilink")のグループは彼らが推進に関して基準に満たすまでサンドボックスを一層よくするために活動している。

Apache CommonsにはCommons Sandboxのプロジェクトの現在のリストが存在する [Sandbox page](http://jakarta.apache.org/commons/sandbox/index.html)。

## Commons Dormant

Commons Dormantは最近の開発活動が矮小化していることが原因で不活性と宣告されたコンポーネントの集合である。これらの[コンポーネント](https://ja.wikipedia.org/wiki/コンポーネント "wikilink")は役に立つかも知れないが、あなた自身で[ビルドしなければならない](https://ja.wikipedia.org/wiki/ビルド_\(ソフトウェア\) "wikilink")。これらのコンポーネントは近い将来リリースされないと思ったほうが良い。

Apache Commonsには利用できるCommons Dormantプロジェクトの現在のリストが存在する[Dormant page](http://jakarta.apache.org/commons/dormant/index.html)。

## 関連項目

  - [Google Guava](https://ja.wikipedia.org/wiki/Google_Guava "wikilink") - [Google](../Page/Google.md "wikilink")によって開発されているオープンソースのJavaユーティリティライブラリ群。後方互換性の確保を担保しているApache Commonsと違い、JDK 1.6以降を対象として開発されている。

## 参考

## 外部リンク

  - [Apache Commons](http://commons.apache.org/)

[Category:Javaプラットフォーム](https://ja.wikipedia.org/wiki/Category:Javaプラットフォーム "wikilink") [Category:オープンソースソフトウェア](https://ja.wikipedia.org/wiki/Category:オープンソースソフトウェア "wikilink") [Category:Apacheソフトウェア財団](https://ja.wikipedia.org/wiki/Category:Apacheソフトウェア財団 "wikilink")
> この記事は[Apache Commons Collections](https://ja.wikipedia.org/wiki/Apache_Commons_Collections)から翻訳されています。


**Apache Commons Collections**（アパッチ コモンズ・コレクションズ）は、[Apacheのトッププロジェクトである](../Page/Apacheソフトウェア財団.md "wikilink")[Apache Commonsにある](../Page/Apache_Commons.md "wikilink")、[Java](https://ja.wikipedia.org/wiki/Java "wikilink")のjava.utilパッケージのCollection関係を拡張するライブラリである。

## 使用例

Java 6 には[クロージャ](../Page/クロージャ.md "wikilink")がないが、`Predicate` を実装することで、条件を満たす物を探すことができる。以下、リストから、a で始まる物を見つけ出す。

    ArrayList<String> list = new ArrayList<String>();
    list.add("apple");
    list.add("banana");
    list.add("ant");
    Collection<String> aList = CollectionUtils.select(list, new Predicate<String>() {
        public boolean evaluate(String str) {
            return str.startsWith("a");
        }
    });

## 外部リンク

  - [Apache Commons Collections](http://commons.apache.org/collections/)

[Category:Javaプラットフォーム](https://ja.wikipedia.org/wiki/Category:Javaプラットフォーム "wikilink") [Category:オープンソースソフトウェア](https://ja.wikipedia.org/wiki/Category:オープンソースソフトウェア "wikilink") [Category:Apacheソフトウェア財団](https://ja.wikipedia.org/wiki/Category:Apacheソフトウェア財団 "wikilink")
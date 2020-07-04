> この記事は[Apache Commons Lang](https://ja.wikipedia.org/wiki/Apache_Commons_Lang)から翻訳されています。


**Apache Commons Lang**（アパッチ・コモンズ・ラング）は、[Apacheのトッププロジェクトである](../Page/Apacheソフトウェア財団.md "wikilink")[Apache Commonsにある](../Page/Apache_Commons.md "wikilink")、[Java](https://ja.wikipedia.org/wiki/Java "wikilink")のjava.langパッケージを拡張するライブラリである。

## 使用例

### 例1

`Object.equals()` を拡張した物。nullが入っていても比較が可能である。

    String s1 = null;
    String s2 = "abc";
    if(ObjectUtils.equals(s1, s2)) {
        System.out.println("equal");
    }

### 例2

Java のデフォルトの `Object.toString()` はメンバ変数の内容まで表示してくれないが、リフレクションを使用して、メンバ変数の内容を表示する形で、`Object.toString()` を実装する。

    public String toString() {
        return ToStringBuilder.reflectionToString(this);
    }

### 例3

文字列の配列を受け取って区切り文字で連結して返す。

    String[] array = new String[]{"Java", "Perl", "Lisp"};
    String joined = StringUtils.join(array, ":");

    // joined は "Java:Perl:Lisp" となる

このような「数行の処理でしかないが、実際書くのは煩わしい。」 「どこかで誰かが書いていて、誰が書いても似たようなコードになる。」 「この前も書いた。今回も書いた。次もきっと書く。」 と言った簡潔・頻出な処理は Commons Lang の得意とするところである。

## 脚注

## 外部リンク

  - [Apache Commons Lang](http://commons.apache.org/lang/)

[Category:Javaプラットフォーム](https://ja.wikipedia.org/wiki/Category:Javaプラットフォーム "wikilink") [Category:オープンソースソフトウェア](https://ja.wikipedia.org/wiki/Category:オープンソースソフトウェア "wikilink") [Category:Apacheソフトウェア財団](https://ja.wikipedia.org/wiki/Category:Apacheソフトウェア財団 "wikilink")
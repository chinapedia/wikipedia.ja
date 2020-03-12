> この記事は[Flyweight ](https://ja.wikipedia.org/wiki/Flyweight_)から翻訳されています。


**Flyweight パターン**（フライウェイト・パターン）とは、[GoFによって定義された](https://ja.wikipedia.org/wiki/ギャング・オブ・フォー_\(情報工学\) "wikilink")[デザインパターンの](https://ja.wikipedia.org/wiki/デザインパターン_\(ソフトウェア\) "wikilink")1つである。 等価な[インスタンス](../Page/インスタンス.md "wikilink")を別々の箇所で使用する際に、一つのインスタンスを再利用することによってプログラムを省リソース化することを目的とする。

## クラス図

Flyweight パターンの[クラス図](../Page/クラス図.md "wikilink")を以下に挙げる。

[500px](https://ja.wikipedia.org/wiki/ファイル:Flyweight_UML_class_diagram.svg "wikilink")

## 概要

Flyweight パターンで設計された [API](../Page/アプリケーションプログラミングインタフェース.md "wikilink") では、利用者は `Flyweight` クラスにあたるインスタンスを取得する場合に、直接そのクラスのコンストラクタを呼び出す代わりに `FlyweightFactory#getFlyweight()` にアクセスする。 一方、呼び出された `FlyweightFactory` オブジェクトは、状況に応じて以下のように振舞う。

  - その時点で対象のインスタンスが生成されていない場合:

<!-- end list -->

1.  対象のインスタンスを新たに生成する。
2.  生成したインスタンスをプールする（言い換えると、メンバのコンテナオブジェクトに格納する）。
3.  生成されたインスタンスを返す。

<!-- end list -->

  - 対象のインスタンスが既に生成されていた場合:

<!-- end list -->

1.  対象のインスタンスをプールから呼び出す。
2.  対象のインスタンスを返す。

このように `FlyweightFactory` では状況によって異なる処理が行われるが、利用者側が得る結果は全く同じであるため、利用者は `FlyweightFactory` の内部構造を意識せずに使うことが出来るという点が特徴である。

Flyweight パターンを採用すべき典型的な例は、不変なクラスを扱う場合である。不変なクラスとはインスタンスが生成された後にそのインスタンスの状態が変化しないようなクラスであり、[Java](https://ja.wikipedia.org/wiki/Java "wikilink") では  や  などが挙げられる。詳しくは[イミュータブル](../Page/イミュータブル.md "wikilink")を参照。

## 利用例

[Java](https://ja.wikipedia.org/wiki/Java "wikilink") による Flyweight パターンの例を挙げる。 このソースコードは JDK1.5 以降のバージョンで動作する。

``` java
import java.util.Map;
import java.util.HashMap;
import java.util.List;
import java.util.ArrayList;

class Stamp {
    char type;
    Stamp(char type){
        this.type = type;
    }
    void print(){
        System.out.print(this.type);
    }
}

class StampFactory {
    Map<Character, Stamp> pool;
    StampFactory(){
        this.pool = new HashMap<Character, Stamp>();
    }
    Stamp get(char type){
        Stamp stamp = this.pool.get(type);
        if(stamp == null) {
            stamp = new Stamp(type);
            this.pool.put(type, stamp);
        }
        return stamp;
    }
}

public class FlyweightTest {
    public static void main(String[] args) {
        StampFactory factory = new StampFactory();
        List<Stamp> stamps = new ArrayList<Stamp>();
        stamps.add(factory.get('た'));
        stamps.add(factory.get('か'));
        stamps.add(factory.get('い'));
        stamps.add(factory.get('た'));
        stamps.add(factory.get('け'));
        stamps.add(factory.get('た'));
        stamps.add(factory.get('て'));
        stamps.add(factory.get('か'));
        stamps.add(factory.get('け'));
        stamps.add(factory.get('た'));
        for(Stamp s : stamps){
            s.print();
        }
    }
}
```

ソースコードとクラス図の対応関係を示す。

  - Flyweight:[Stamp](https://ja.wikipedia.org/wiki/#Stamp "wikilink")
    FlyweightFactory:[StampFactory](https://ja.wikipedia.org/wiki/#StampFactory "wikilink")
    FlyweightFactory\#getFlyweight():[StampFactory\#get()](https://ja.wikipedia.org/wiki/#StampFactory-get "wikilink")

このプログラムを実行すると「たかいたけたてかけた」（高い竹立て掛けた）という文字列を出力する。 `FlyweightTest#main()` 内で `StampFactory#get()` を 10 回参照しているが、 そのうち実際に生成されたインスタンスは 5 つ（「た」、「か」、「い」、「け」、「て」）だけであり、 インスタンスが共有されていることが分かる。

## 注意点

一度 `FlyweightFactory` に保存されたインスタンスは、たとえ不要になった場合でも[ガベージコレクション](../Page/ガベージコレクション.md "wikilink")されることがないため、場合によっては明示的に `FlyweightFactory` から削除する必要がある。

## 関係するパターン

  - [Singleton パターン](../Page/Singleton_パターン.md "wikilink"):`FlyweightFactory` は Singleton として実装されることが多い。

## 関連項目

  - [デザインパターン](https://ja.wikipedia.org/wiki/デザインパターン_\(ソフトウェア\) "wikilink")
  - [ガベージコレクション](../Page/ガベージコレクション.md "wikilink")
  - [イミュータブル](../Page/イミュータブル.md "wikilink")

## 外部リンク

  - [Javaの理論と実践: 可変性か、不変性か?](http://www.ibm.com/developerworks/jp/java/library/j-jtp02183/)

[Category:デザインパターン_(ソフトウェア)](https://ja.wikipedia.org/wiki/Category:デザインパターン_\(ソフトウェア\) "wikilink") [Category:コンピュータの最適化](https://ja.wikipedia.org/wiki/Category:コンピュータの最適化 "wikilink")
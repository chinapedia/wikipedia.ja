> この記事は[NullPointerException](https://ja.wikipedia.org/wiki/NullPointerException)から翻訳されています。


**NullPointerException**（ヌル・ポインタ・エクセプション、ナル-）は、[プログラミング言語](../Page/プログラミング言語.md "wikilink")[Java](https://ja.wikipedia.org/wiki/Java "wikilink")における[例外の一つである](../Page/例外処理.md "wikilink")。

## 解説

[null値](https://ja.wikipedia.org/wiki/Null "wikilink")（定義されていない値）の参照型変数を参照しようとした時に発生する。NullPointerExceptionは実行時例外と呼ばれる クラスのサブクラスであるため、try-catch節による[例外処理](../Page/例外処理.md "wikilink")を書かなくても[コンパイル](https://ja.wikipedia.org/wiki/コンパイル "wikilink")エラーは発生しない。

## コード例

``` java
// NullPointerExceptionSample.java
public class NullPointerExceptionSample {
    public static void main(String[] args) {
        try {
            Integer i = null;

            // ここで NullPointerException がスローされる。
            i.toString();

        // ここで NullPointerException がキャッチされる。
        } catch (NullPointerException e) {
            e.printStackTrace();
        }
    }
}
```

### 出力例

    java.lang.NullPointerException
            at NullPointerExceptionSample.main(NullPointerExceptionSample.java:7)

## 関連項目

  - [例外](../Page/例外.md "wikilink")
  - [例外処理](../Page/例外処理.md "wikilink")
  - [ヌルポインタ](https://ja.wikipedia.org/wiki/ヌルポインタ "wikilink")
  - [ぬるぽ](../Page/ぬるぽ.md "wikilink")

## 外部リンク

  -
  - [NullPointerException クラス](http://docs.oracle.com/javase/jp/6/api/java/lang/NullPointerException.html)

[Category:Java](https://ja.wikipedia.org/wiki/Category:Java "wikilink")
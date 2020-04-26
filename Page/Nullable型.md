> この記事は[Nullable型](https://ja.wikipedia.org/wiki/Nullable型)から翻訳されています。


**Nullable型**、**Null許容型**(Nullable type)は一部の[プログラミング言語](../Page/プログラミング言語.md "wikilink")の機能であり、 [データ型](../Page/データ型.md "wikilink")の通常可能な値の代わりに、値を特殊な値 **NULL** に設定できる。 静的に型付けされた言語では、Nullable型はOption型だが、動的に型付けされた言語（値には型があるが変数にはない）では、単一のnull値を持つことで同等の動作が提供される。

NULLは、 [SQL](../Page/SQL.md "wikilink")におけるNULLのように、返されなかった関数やデータベースのフィールドの欠落などから、欠落した値または無効な値を表すためによく使用される 。

[整数](../Page/整数.md "wikilink")や[ブーリアン型](../Page/ブーリアン型.md "wikilink")などの[プリミティブ型](../Page/プリミティブ型.md "wikilink")は通常nullにすることはできないが、対応するNullable型（Nullable整数およびNullableブーリアン型）もNULL値をとることができる。

## 例

整数変数は整数を表すが、0 (ゼロ) は特殊なケースである。これは、多くのプログラミング言語で0が "false" を意味する場合があるためである。 またこれは、変数が空であると言う概念を私たちに与えない。それは多くの状況では必要になる。 この必要性は、Nullable型で実現できる。 [C\#](../Page/C_Sharp.md "wikilink")2.0などのプログラミング言語では、たとえば、Nullable整数は疑問符 *int? x* で宣言できる。 \[1\] [C\#](../Page/C_Sharp.md "wikilink") 1.0のようなプログラミング言語では、Nullable型は外部ライブラリ\[2\]によって新しい型として定義される (たとえば、NullableInteger、NullableBoolean)。 \[3\]

ブール変数は効果をより明確にする。 その値は "true" または "false" のいずれかだが、Nullableブール値には "undecided"(未決定)の表現も含まれる場合がある。 ただし、そのような変数を含む論理演算の解釈または処理は、言語によって異なる。

## nullポインタと比較

対照的に、ほとんどの一般的な言語では、デフォルトで[オブジェクト](https://ja.wikipedia.org/wiki/オブジェクト "wikilink")[ポインタを](../Page/ポインタ_\(プログラミング\).md "wikilink")[NULLに設定できる](https://ja.wikipedia.org/wiki/ヌルポインタ "wikilink")。これは、ポインタまたは参照がどこも指さないこと、オブジェクトが割り当てられないこと (変数がオブジェクトを指さないこと)を意味しする。 Nullable参照は、1965年に[アントニー・ホーア](../Page/アントニー・ホーア.md "wikilink")によってAlgol W言語の一部として発明された。 ホーアは後に彼の発明を「10億ドルの間違い」と表現した。 \[4\] これは、NULLの可能性があるオブジェクトポインタは、ユーザがポインタを使用する前に確認する必要があり、オブジェクトポインタがNULLの場合を処理するために特定のコードが必要になるためである。

[Java](https://ja.wikipedia.org/wiki/Java "wikilink")には、Integer、Boolean、Floatなどのスカラー値に対応するクラスがある。[自動ボックス化](../Page/ボックス化.md "wikilink")（オブジェクトと値の間の使用法に基づく自動変換）と組み合わせると、スカラー値にnullを使用できる変数を効果的に使用できる <sup>\[*[<span title="This claim needs references to reliable sources. (July 2019)">引用が必要</span>](https://ja.wikipedia.org/wiki/Wikipedia:「要出典」をクリックされた方へ "wikilink")*\]</sup>。

## Option型と比較

Nullable型の実装は通常、[nullオブジェクトパターンに従う](https://ja.wikipedia.org/wiki/Null_object_パターン "wikilink")。

Nullable型の概念を拡張する、より一般的で正式な概念がある。これは、例外的なケースの明示的な処理を強制するOption型からのものである。 Option型の実装は、通常、特殊なケースパターンに従う\[5\] 。

## 言語ごとのサポート

次のプログラミング言語は、Nullable型をサポートしている。

ネイティブでのnullサポートのある静的型付け言語には、次のものがある。

  - [Ballerina](https://ja.wikipedia.org/wiki/Ballerina "wikilink") \[6\]

  - [Kotlin](https://ja.wikipedia.org/wiki/Kotlin "wikilink") \[7\]

  - [Ceylon](https://ja.wikipedia.org/wiki/Ceylon "wikilink")

  - [SQL](../Page/SQL.md "wikilink")

  - （欠損値）

ライブラリがnullをサポートする静的型付け言語には、次のものがある。

  - [C＃](../Page/C_Sharp.md "wikilink") （バージョン2以降）
  - [VB.NET](../Page/Visual_Basic_.NET.md "wikilink")
  - [Java](https://ja.wikipedia.org/wiki/Java "wikilink") （バージョン8以降）
  - [Swift](https://ja.wikipedia.org/wiki/Swift_\(プログラミング言語\) "wikilink")
  - [Scala](../Page/Scala.md "wikilink")
  - [Oxygene](https://ja.wikipedia.org/wiki/Oxygene "wikilink")
  - [F\#](../Page/F_Sharp.md "wikilink")
  - 静的に型付けされた[CLI言語](../Page/共通言語基盤.md "wikilink")

nullを含む動的型付け言語には、次のものがある。

  - [Perl](../Page/Perl.md "wikilink"): スカラー変数のデフォルトでは`undef`あり、 `undef`に設定できる
  - [PHP](https://ja.wikipedia.org/wiki/PHP "wikilink"): NULL型、is_null()メソッド、バージョン7.1のネイティブnull可能型\[8\]
  - [Python](../Page/Python.md "wikilink"):`None`値がある\[9\]
  - [Ruby](../Page/Ruby.md "wikilink"): nil値とNilClassタイプ
  - [JavaScript](../Page/JavaScript.md "wikilink"): `null`値がある

## 関連項目

  - [Null合体演算子](https://ja.wikipedia.org/wiki/Null合体演算子 "wikilink")

  -
  - [共用体](https://ja.wikipedia.org/wiki/共用体 "wikilink")

  -
## 参考

[Category:型理論](https://ja.wikipedia.org/wiki/Category:型理論 "wikilink")

1.
2.
3.
4.  <http://www.infoq.com/presentations/Null-References-The-Billion-Dollar-Mistake-Tony-Hoare>
5.
6.  <https://ballerina.io/learn/by-example/optional-type.html>
7.  <https://kotlinlang.org/docs/reference/null-safety.html>
8.  <https://wiki.php.net/rfc/nullable_types>
9.  <https://docs.python.org/3/library/constants.html#None>
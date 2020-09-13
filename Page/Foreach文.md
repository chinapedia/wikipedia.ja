> この記事は[Foreach文](https://ja.wikipedia.org/wiki/Foreach文)から翻訳されています。


**foreach文**（フォーイーチぶん）とは[プログラミング言語](../Page/プログラミング言語.md "wikilink")において[リストや](https://ja.wikipedia.org/wiki/線形リスト "wikilink")[連想配列](../Page/連想配列.md "wikilink")などの「コレクション」と呼ばれる[データ構造](../Page/データ構造.md "wikilink")の各[要素](https://ja.wikipedia.org/wiki/要素 "wikilink")に対して与えられた[文の実行を繰り返すという](https://ja.wikipedia.org/wiki/文_\(プログラミング\) "wikilink")[ループを記述するための文である](../Page/ループ_\(プログラミング\).md "wikilink")。foreach文はしばしば[for文](https://ja.wikipedia.org/wiki/for文 "wikilink")の一部という位置付けにある。for文と異なり要素の参照順序が定義されないこともある。

## 処理の流れ

基本的な構文 ([Perl](../Page/Perl.md "wikilink")) は以下のようになる。

``` perl
foreach 変数 (リスト) {
    文
}
```

このループはだいたい次のような手順で実行される。

1.  変数にリストの中のある要素への参照を代入する。
2.  文を実行する。
3.  リストの全要素を参照し終わっていない場合は、変数に未参照の要素を代入して文の実行へ戻る。

ここで、[線形リスト](https://ja.wikipedia.org/wiki/線形リスト "wikilink")や[配列](../Page/配列.md "wikilink")など要素の順序が決まっているものは、通常その順序でループが実行されるので、この場合以下とほぼ同様である。

``` perl
for ( my $i = 0; $i < @list; $i++ ) {
    変数 = $list[$i];
    文
}
```

ただし、[ハッシュテーブル](../Page/ハッシュテーブル.md "wikilink")（[連想配列](../Page/連想配列.md "wikilink")）については要素の順序関係が決定できないこともあるため、一般に参照順序は不定である。

## 文法

### [awk](https://ja.wikipedia.org/wiki/awk "wikilink")

awkにおいても[連想配列](../Page/連想配列.md "wikilink")の処理を可能にしている。

``` awk
for (変数 in 配列)
{
    文
}
```

### [C\#](../Page/C_Sharp.md "wikilink")

``` csharp
foreach (変数 in コレクション)
{
    文
}
```

コレクションは配列のほか、IEnumerableもしくはIEnumerable<T>を実装したオブジェクトでもよい。

### [C++](../Page/C++.md "wikilink")

C++は、2011年での規格改定（通称[C++11](https://ja.wikipedia.org/wiki/C++11 "wikilink")）にて、[範囲ベースの for ループが言語仕様として追加されている](https://ja.wikipedia.org/wiki/C++11#範囲に基づく_for_ループ "wikilink")。

``` cpp
for (変数 : コレクション)
{
  文
}
```

上記で「コレクション」と記した箇所には、配列のほか、std::vectorやstd::arrayのような標準ライブラリにおいて**コンテナ**に分類される各種のオブジェクトなども使用できる。

そのほか、1998年の標準規格化当初からC++標準ライブラリにfor_eachアルゴリズム（関数テンプレート）が存在する。

``` cpp
関数オブジェクト = std::for_each(
  先頭イテレータ,
  末尾イテレータ,
  関数オブジェクト
);
```

C++11では、C\#同様に[型推論および](https://ja.wikipedia.org/wiki/C++11#型推論 "wikilink")[ラムダ式を組み合わせることで](https://ja.wikipedia.org/wiki/C++11#ラムダ関数とラムダ式 "wikilink")、上記の構文が威力を発揮するようになる。

なお、[C++/CLI](https://ja.wikipedia.org/wiki/C++/CLI "wikilink")言語および[Microsoft Visual C++ 2005以降の独自拡張機能では](../Page/Microsoft_Visual_C++.md "wikilink")、`for each`文を使用できるが、不安定で正常に動作しない場合がある。また、これは[C++11](https://ja.wikipedia.org/wiki/C++11 "wikilink")における範囲ベース for ループとは互換性を持たない。

``` cpp
for each (変数 in コレクション)
{
  文
}
```

### [D](../Page/D言語.md "wikilink")

式を評価し、その結果は静的配列、動的配列、連想配列、構造体、クラスでなければいけない。式部分が配列である場合は、変数は複数宣言することができる。

``` d
foreach (変数 ; 式) {
  文
}
```

### [Java](https://ja.wikipedia.org/wiki/Java "wikilink") 5.0以降

拡張[For文](../Page/For文.md "wikilink")などと呼び、Java 5.0 で導入された。For文の特殊なものとして捉えられるが、Foreach文に相当する。

``` java
for (変数 : コレクション) {
  文
}
```

### [JavaScript](../Page/JavaScript.md "wikilink"), [ActionScript](../Page/ActionScript.md "wikilink")

オブジェクトの反復処理にはfor-in文を用いる。変数にはプロパティ名（連想配列で言うキー）が代入されるので、プロパティの値は式 `オブジェクト[変数]` で取得する。

``` javascript
for (var 変数 in オブジェクト) {
    文
}
```

JavaScriptのfor-in文は、ユーザー定義のプロパティについて、プロトタイプチェーンをさかのぼって反復処理を行う。このため、特に配列に対してfor-in文を用いると、他の言語とは異なる挙動をすることがある。

``` javascript
var array = new Array(3);
var output = "";
for (var key in array) { output += key + " "; }
// このとき array.length === 3 であるが、
// array にユーザー側からプロパティ（配列要素）を定義していないので、
// output === "" である。

// 配列もオブジェクトなので、数値以外のプロパティを設定できる。
array.foo = "foo"

output = "";
for (var key in array) { output += key + " "; }
// このとき output === "foo " である。

// オブジェクトに新しいインスタンスメソッドを追加してみる。
Object.prototype.myMethod = function () {};

output = "";
for (var key in array) { output += key + " "; }
// 配列もオブジェクトなので、このとき output === "foo myMethod " である。

// なおもちろん、この時点でも array.length === 3 である。
```

ECMA-262第5版 (JavaScript 1.6, ActionScript 3.0) からは、ArrayインスタンスにforEachメソッドが追加された。

``` javascript
array.forEach(function (変数) {
    文
});
```

ECMA-262第6版からは、配列などのiterableオブジェクトの値で反復処理をするfor-of文も導入された。

``` javascript
for (変数 of オブジェクト) {
    文
}
```

### [Perl](../Page/Perl.md "wikilink")

しばしばforが代用とされる。Perlにおいて、forとforeachは同義語である。

``` perl
foreach 変数 (コレクション) {
  文
}
```

### [PHP](../Page/PHP_\(プログラミング言語\).md "wikilink")

``` php
foreach (配列 as 変数) {
  文
}
```

``` php
foreach (配列 as 変数1 => 変数2) {
  文
}
```

前者の場合、処理手順は他の言語と同様だが、後者の場合、変数1に配列の添字が、変数2に要素が代入される。

### [Python](../Page/Python.md "wikilink")

Pythonにおける[For文](../Page/For文.md "wikilink")とは、他の言語におけるForeach文と同等である。

``` python
for 変数 in コレクション :
    文
```

### [Ruby](../Page/Ruby.md "wikilink")

``` ruby
for 変数 in コレクション
  文
end
```

これは以下の[イテレータ](../Page/イテレータ.md "wikilink")構文と、変数のスコープを除いて等価である。

``` ruby
コレクション.each do |変数|
  文
end
```

なお、Rubyに関してはもっぱら後者の構文が好まれる傾向にある。

### [Smalltalk](../Page/Smalltalk.md "wikilink")

``` smalltalk
コレクション do:
[ :変数 |
 文
].
```

SmalltakはLispの影響を受けており、言語構文として反復構文が存在せず、\#do:セレクターとブロックオブジェクトを使ったメッセージで表現する。上記ではメッセージを受け取るレシーバーをコレクションと表記しているが、\#do:は下記の条件を満たしていれば良く、入力ストリームや0回か1回しか実行しないオブジェクト、無限数列などもレシーバーとして指定できる。また、\#do:のために反復状態を持つ専用のクラスが必要なく\#do:のメソッドだけで完結するため、C++のような方式に比べ実装が単純になっている。またフィルターも容易であり、フィルター用のクラスも多数存在する。\#do:は列挙プロトコルに属しており、\#do:を実装しCollectionあるいはIterableを継承したオブジェクトは、\#select:, \#collect:, \#detect:, \#inject:into:といったその他の列挙プロトコルが同時に使えるようになる。

  - 戻り値を返さない。(Smalltalkの制約上、正確にはselfを返す)
  - \#do:の引数としてValueAdapter (\#value:を送ることができるオブジェクト) を指定する。(ブロックはValueAdapterの一種)
  - 引数として指定したValueAdapterが0回以上の反復に対応している。

<!-- end list -->

``` smalltalk
(1 to: 100) do:
[ :each |
  文
].
```

例えば一定回数反復したい場合も\#do:を使い、上記のようになる。

Smalltalkは後発の無名関数を備えたオブジェクト指向言語に広く影響を与えており、Ruby、ECMAScript、Java、C\#も同様のライブラリを備えつつある。

### [Visual Basic](../Page/Visual_Basic.md "wikilink")

``` vb
For Each 変数 In コレクション
  文
Next 変数
```

### [PowerShell](../Page/PowerShell.md "wikilink")

``` powershell
foreach (変数 in コレクション) {
  文
}
```

### [HSP](../Page/Hot_Soup_Processor.md "wikilink")

`foreach 変数`
`  文`
`loop`

### [なでしこ](../Page/なでしこ_\(プログラミング言語\).md "wikilink")

`(リスト)を反復。`
`　　文`

変数は「それ」に代入される。

### [シェルスクリプト](../Page/シェルスクリプト.md "wikilink")

[csh](https://ja.wikipedia.org/wiki/csh "wikilink")ではforeachと書き、[shではforと書く](../Page/Bourne_Shell.md "wikilink")。実用上リストの部分にはワイルドカードを含むファイル列を書くことが多い。

csh系

``` csh
foreach 変数 ( リスト )
  文
end
```

sh系

``` sh
for 変数 in リスト
do
  文
done
```

## 番外編

### [PL/SQL](https://ja.wikipedia.org/wiki/PL/SQL "wikilink")

OracleのPL/SQLにも、カーソルというForEachと似たような機能が実装されている。 カーソルは用途が限定されているため、番外編として紹介する。

SELECT文でとってきた複数レコードを、カーソルを使って順繰り出力するPL/SQL文を示す。

``` sql
DECLARE
    CURSOR C IS
        SELECT
             *
        FROM
            TBL1
        WHERE
            TBL1.FIELD1 >= 100;
BEGIN
    FOR D IN C LOOP
        DBMS_OUTPUT.PUT_LINE(D.FIELD1 || ' ' || D.FIELD2 || ' ' || D.FIELD3);
    END LOOP;
END;
```

## 関連項目

  - [for文](https://ja.wikipedia.org/wiki/for文 "wikilink")
  - [while文](https://ja.wikipedia.org/wiki/while文 "wikilink")
  - [goto文](https://ja.wikipedia.org/wiki/goto文 "wikilink")
  - [イテレータ](../Page/イテレータ.md "wikilink")

[ru:Цикл просмотра](https://ja.wikipedia.org/wiki/ru:Цикл_просмотра "wikilink")

[Category:制御構造](https://ja.wikipedia.org/wiki/Category:制御構造 "wikilink")
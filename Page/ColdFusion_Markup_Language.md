> この記事は[ColdFusion Markup Language](https://ja.wikipedia.org/wiki/ColdFusion_Markup_Language)から翻訳されています。


**ColdFusion Markup Language**（**CFML**）は、[アドビシステムズ](../Page/アドビシステムズ.md "wikilink")の [ColdFusion](../Page/ColdFusion.md "wikilink") で使われている[マークアップ言語](../Page/マークアップ言語.md "wikilink")である。他にも、BlueDragon、Coral Web Builder、IgniteFusion、Railo などで使われている。タグを使っている点、形式にこだわらない点、マークアップ内にスクリプトを組み込める点などが [HTML](../Page/HyperText_Markup_Language.md "wikilink") に類似している。

## 構文

中核部に含まれるタグの名前には常に *cf* が前置され、その後にユニークな識別文字列が続く。CFML で書かれたカスタムタグには *cf_* が前置されるが、他にも呼び出し方が存在する。

手続き的な関数は、 を通して利用可能である。

CFML は一般に[動的プログラミング言語](../Page/動的プログラミング言語.md "wikilink")と見なされている。しかし、各種タグで入力パラメータの型チェックが可能である（cffunction、cfparam、cfqueryparam など。ただし、プログラマが型を指定した場合）。型チェックが使われているか否かに関わらず実行時に失敗が発生するのだが、これがよい方式かどうかについては異論もある。

CFML は大文字と小文字を区別しない。

CFML では [C++](../Page/C++.md "wikilink") の map コンテナのようなデータ構造を多用する。キーは常に文字列だが、値の型は特に指定されない。値はドット記法でアクセスされることが多いが、CFML の実装によっては手続き的関数からアクセスできたり、一種のオブジェクトのように扱って *get* メソッドで値を取り出す形式もある。

最近の CFML 実装では、コンポーネントとしてオブジェクトをサポートしている。コンポーネント定義はファイル内にあり、*cfcomponent* タグで囲まれている。

コンポーネント間の[メッセージパッシング](https://ja.wikipedia.org/wiki/メッセージパッシング "wikilink")もドット記法で行われる。これは[Java](https://ja.wikipedia.org/wiki/Java "wikilink")などの[オブジェクト指向言語](https://ja.wikipedia.org/wiki/オブジェクト指向言語 "wikilink")と似た記法である。メソッド呼び出しの括弧を省略すると、ColdFusion ではその関数を値オブジェクトの map とみなす。これによりメソッドが一種の[第一級オブジェクト](../Page/第一級オブジェクト.md "wikilink")として扱われる。

CFML は形式にこだわらない。タグに本体がないのが普通である場合、文法的にもそのタグを閉じる必要がない。例えば、

    <cfset value = "hello">

と書いても

    <cfset value = "hello"/>

と書いても正しい。どちらを使うべきかという議論もよく発生する。

## カスタムタグ

CFML はカスタムタグという形で言語の拡張が可能である。カスタムタグはタグとして呼び出される通常ファイルであるが、テンプレートをカスタムタグおよび通常のテンプレートとして扱うことも可能である。

テンプレートがカスタムタグとして呼び出された場合、そのタグを呼び出すのに使われた属性が特殊なデータ構造 *attributes* に格納され、呼び出したページにある変数は *caller* 構造体を通してそれにアクセスできる。例えば、2つの属性をとり、それらを加算する *add* タグを書くとき、add.cfm ページは次のようになる。

    <cfset caller.sum = attributes.first + attributes.second / >

このタグは次のように呼び出される。

    <cf_sum first="1" second="2">

このとき、テンプレートとタグは同じディレクトリにあるものとする。

## CFMLサーバ

  - [ColdFusion](../Page/ColdFusion.md "wikilink")
  - [BlueDragon](http://www.newatlanta.com/products/bluedragon/index.cfm)
  - [Railo](http://www.railo.ch/en/)
  - [Smith](http://www.smithproject.org/index.cfm)
  - [Ignite Fusion](http://www.ignitefusion.com/)
  - [Coral](http://www.pcaonline.com/prod/index.cfm?loc=coral)
  - [link Camuffo](http://sourceforge.net/projects/camuffo)

[Category:スクリプト言語](https://ja.wikipedia.org/wiki/Category:スクリプト言語 "wikilink")
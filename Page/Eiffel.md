> この記事は[Eiffel](https://ja.wikipedia.org/wiki/Eiffel)から翻訳されています。


**Eiffel**（アイフェル、エッフェル）は頑健なソフトウェアの生産に注力した[オブジェクト指向](../Page/オブジェクト指向プログラミング.md "wikilink")[プログラミング言語](../Page/プログラミング言語.md "wikilink")である。

## 概要

[1985年](https://ja.wikipedia.org/wiki/1985年 "wikilink")に[バートランド・メイヤー](../Page/バートランド・メイヤー.md "wikilink")（）によって考案された。その文法は[Pascal](../Page/Pascal.md "wikilink")を連想させるものである。Eiffelは静的な型指定を強く指向しており、かつ動的なメモリ管理（一般的に[ガベージコレクション](../Page/ガベージコレクション.md "wikilink")により実装される）を備えている。

少し前、オブジェクト指向の教科書的言語といえば、[Smalltalk](../Page/Smalltalk.md "wikilink")かEiffelか、という状況で、[手続き型言語](https://ja.wikipedia.org/wiki/手続き型言語 "wikilink")でのPascalのような存在であった。[多重継承](https://ja.wikipedia.org/wiki/多重継承 "wikilink")、[ガベージコレクション](../Page/ガベージコレクション.md "wikilink")といった特徴があるが、設計者によって[ライブラリ](../Page/ライブラリ.md "wikilink")の[メンテナンス](../Page/メンテナンス.md "wikilink")が重視されており、[契約による設計](../Page/契約プログラミング.md "wikilink")（*[{{Lang](../Page/契約プログラミング.md "wikilink")*）の概念が全面に打ち出されている。同じくオブジェクト指向を取り入れた言語である[Java](https://ja.wikipedia.org/wiki/Java "wikilink")ほどは普及していない。[Assertionなど](../Page/表明.md "wikilink")、Javaが追いかけているところもあるが、[インタフェースによる](../Page/インタフェース_\(情報技術\).md "wikilink")[継承](../Page/継承_\(プログラミング\).md "wikilink")、[GCあり](../Page/ガベージコレクション.md "wikilink")、とかぶるところが多い。

また、C/[C++](../Page/C++.md "wikilink")のようにネイティブコードを直接生成するのではなく、C言語やJavaのコードを生成する、という特徴ももっている。

言語名の由来は、[エッフェル塔](../Page/エッフェル塔.md "wikilink")ではなく、その設計者[ギュスターヴ・エッフェル](../Page/ギュスターヴ・エッフェル.md "wikilink")である。

## 基本構成

Eiffel のソースは以下のように記述する。

``` eiffel
 -- コメント
 class クラス名

 inherit
   継承元のクラス（継承しない場合は省略可）

 creation
  コンストラクタの宣言（コンストラクタが必要ない場合は省略可）

 feature{アクセス権限}
   メンバ変数、メンバ関数の記述

 end
```

Eiffel は「[クラスとは](../Page/クラス_\(コンピュータ\).md "wikilink")[オブジェクトの生成機である](../Page/オブジェクト_\(プログラミング\).md "wikilink")」という考え方が徹底しており、このため両者の概念を混同するような[クラス変数](../Page/クラス変数.md "wikilink")や[クラスメソッドの機能は存在しない](https://ja.wikipedia.org/wiki/メソッド_\(計算機科学\)#静的メソッド "wikilink")。このことは「[クラスもオブジェクトの一種である](../Page/メタクラス.md "wikilink")」と考える Smalltalk とは対照的である。

また「クラス」に対する考え方も独特で、例えば Java ではソースファイルを[コンパイル](https://ja.wikipedia.org/wiki/コンパイル "wikilink")すると「[クラスファイル](https://ja.wikipedia.org/wiki/Javaクラスファイル "wikilink")」という[ファイルを作るのを見てわかるように](../Page/ファイル_\(コンピュータ\).md "wikilink")、一般的には「[ソースコード](../Page/ソースコード.md "wikilink")」は「クラスの設計図」という概念であるのに対し、Eiffel では「クラス」とは「ソースコードそのものである」という考え方である。コンパイルして生成されるファイルは「クラス（ソースコード）によって作られた[インスタンス](../Page/インスタンス.md "wikilink")」という考え方であり、このため Eiffel では[メインルーチンに相当する処理を](https://ja.wikipedia.org/wiki/エントリーポイント "wikilink")[コンストラクタ](../Page/コンストラクタ.md "wikilink")で行う。

コンストラクタは`creation`下で宣言された[メンバ関数](https://ja.wikipedia.org/wiki/メンバ関数 "wikilink")が使用される、このメンバ関数はどんな名称でも構わないが慣例的に`make`とする場合が多い。作成したクラスを使用する場合は

``` eiffel
x :（クラス名）
!!x.（コンストラクタ名）
```

でインスタンスを作成する（コンストラクタが指定されているクラスは上記の構文中で必ずコンストラクタを呼び出さなければならない）。

クラスの継承を省略した場合は ANY というクラスの継承クラスとして扱われる。入出力などのグローバルな機能は ANY クラス内で定義されており、各 Eiffel のクラスではこれらの機能の実装に関して考慮をする必要性がないようになっている。

なお、Eiffelはクラス名は全て大文字で書かなければならないという命名規則がある。

## rename と redefine

Eiffel の特徴の一つとして、継承における細かい指定が可能ということが挙げられる。例えば

``` eiffel
 class A
 feature
   method1 is
     io.put_string("Hello from A")
     io.new_line
   end
 end
```

``` eiffel
 class B
 inherit
   A
 feature
   method1 is
     io.put_string("Hello from B")
     io.new_line
   end
 end
```

というコードがあるとする（ioは標準入出力を扱うインスタンスで、ANYクラスのメンバである）。これは A というクラスを継承した B というクラスに同じ名前のメソッドがある場合である。このとき

``` eiffel
  class  C
  creation
    make
  feature
    a : A
    b : B

    make is
    do
      !!b
      a := b
      b.method1
      a.method1
    end
 end
```

というコードを実行したとき。b.method1 はおそらく B で定義されたメソッドが動くと誰もが期待するだろうが、a.method1 で実行されるメソッドは A と B どちらで定義されたものだろうか?この場合の処理は言語によって異なっており例えば[C++](../Page/C++.md "wikilink")の場合は A で定義されたメソッドが実行され、[Java](https://ja.wikipedia.org/wiki/Java "wikilink")の場合は B のメソッドが実行される。すなわち言語によって動作が違うため作成者の勘違いなどによって混乱を招くおそれがある。

Eiffelでは実のところ、どちらが実行されるか以前に上記のような例では[コンパイル](https://ja.wikipedia.org/wiki/コンパイル "wikilink")することができないことになっている。すなわち Eiffelのメソッドは全てデフォルトでは継承不可である。しかしこれでは、あまりに制約が強すぎるため、同名のメソッドを定義する必要性があるときは、継承クラスの作成者がどちらを実行するかを指定することが出来る。

具体的には rename と redefine という機能があり、上記の例では A で定義されたメソッドを実行したい場合は

``` eiffel
 class B
 inherit
   A
   rename
     method1 as method2
   end
```

とする。この場合クラス B では A のメソッドを method2 という名前に改名させて、名前の衝突を防いでいる。B のインスタンスでも、クラス A のインスタンスとして扱われた場合（上記の例のような場合）は A の method1 が実行され、クラス B のインスタンスとして扱われた場合は B のmethod1 が実行される。B のインスタンスとして扱われた状態で A の method1 を実行するには上記の例では b.method2 とすればよい。これらの改名による効果は継承先と継承元の他、多重継承時のメソッド同士の衝突にも使用できる。

逆に A のインスタンスとして扱われる場合でも B の method1 を実行したい場合は以下のようにする。

``` eiffel
 class B
 inherit
   A
   redefine
     method1
   end
```

この場合、クラス B はクラス A の method1 を継承時に破棄しクラス B で再定義することを示している。クラス B のインスタンスは A、B どちらで扱われても method1 はクラス B のものが実行され、クラス A の method1 はもはや実行されることは無い。なお再定義を宣言された method1 は必ずクラス B で再定義しなければならず、再定義していない場合はコンパイルエラーとなる。

このように、Eiffel ではクラスの継承時に継承クラスの作成者がメソッドの扱いを自由に設定することができる。

## コンストラクタの非継承

Eiffel の特徴の一つとして[多重継承をサポートしていることが挙げられる](https://ja.wikipedia.org/wiki/継承_\(プログラミング\)#多重継承と仮想継承 "wikilink")。

多重継承時に問題となるものの一つとして、継承した二つの（あるいはそれ以上）のクラスのどちらにもコンストラクタが定義されている場合、二つのクラスのどちらのコンストラクタが実行されるか?というものがある。Eiffel の他に多重定義をサポートしている [C++](../Page/C++.md "wikilink")や [Python](../Page/Python.md "wikilink") では継承元のコンストラクタの実行順に複雑な規則が導入されている。

Eiffelではコンストラクタは継承されないことになっている。このためコンストラクタの実行手順といったものは原理的に存在しない。どうしても継承元のコンストラクタを使用する必要がある場合は、継承時に rename でコンストラクタとして宣言されているメソッドを改名し、改名したメソッドをコンストラクタ内で実行することで実装できる。

## 脚注

## 外部リンク

  - [Eiffel.org](https://www.eiffel.org/)

  -
  - [SmartEiffel The GNU Eiffel Compiler](http://smarteiffel.loria.fr/) - SmartEiffel （[GNUプロジェクト](../Page/GNUプロジェクト.md "wikilink")によるフリーのEiffel[コンパイラ](../Page/コンパイラ.md "wikilink")）配布ページ

[Category:形式仕様記述言語](https://ja.wikipedia.org/wiki/Category:形式仕様記述言語 "wikilink") [Category:オブジェクト指向言語](https://ja.wikipedia.org/wiki/Category:オブジェクト指向言語 "wikilink") [Category:エポニム](https://ja.wikipedia.org/wiki/Category:エポニム "wikilink")
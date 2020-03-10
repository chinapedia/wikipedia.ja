> この記事は[Common Lisp Object System](https://ja.wikipedia.org/wiki/Common_Lisp_Object_System)から翻訳されています。


（コモン リスプ オブジェクトシステム、略称 **CLOS**）は、ANSI [Common Lisp](https://ja.wikipedia.org/wiki/Common_Lisp "wikilink") (CL) の一部をなす[オブジェクト指向プログラミング](../Page/オブジェクト指向プログラミング.md "wikilink")機能であり、他の類似の言語（[EuLisp](https://ja.wikipedia.org/wiki/EuLisp "wikilink") や [Emacs Lisp](../Page/Emacs_Lisp.md "wikilink")）にも導入されている\[1\]。当初アドオンとして提案され、[ANSI](https://ja.wikipedia.org/wiki/ANSI "wikilink")の標準に組み込まれた。CLOS は*強い型付け*をもつ(無名クラスは許されない)[動的](https://ja.wikipedia.org/wiki/動的プログラミング言語 "wikilink")(実行時に定義を変更できる)オブジェクトシステムであり、[C++](../Page/C++.md "wikilink")や[Java](https://ja.wikipedia.org/wiki/Java "wikilink")のような静的なオブジェクト指向言語とは大きく異なる。初期のLISPオブジェクトシステム（MIT [Flavors](https://ja.wikipedia.org/wiki/Flavors "wikilink") や [Common LOOPS](https://ja.wikipedia.org/wiki/Common_LOOPS "wikilink")）に影響されているが、より汎用的である。

LISPにオブジェクト指向を導入することは簡単である。2ページ程度のコードがあれば実現できる（Graham, 1994）。一方、オブジェクト指向LISPを柔軟で拡張性に富んだものに設計するのはより困難であった。CLOS は完全なオブジェクトシステムであり、オブジェクト指向風に実装されている。CLOS のオブジェクト指向実装は CLOS Metaobject Protocol (MOP) と呼ばれ、これによってカスタマイズや拡張が可能となっている。\[2\]

[フレーム](https://ja.wikipedia.org/wiki/ファイル:Method-combination.png "wikilink")

## 特徴

### 多重ディスパッチ

CLOS は[多重ディスパッチ](https://ja.wikipedia.org/wiki/多重ディスパッチ "wikilink")システムである。すなわち、引数の[データ型](https://ja.wikipedia.org/wiki/データ型 "wikilink")によって[メソッドを用意できる](https://ja.wikipedia.org/wiki/メソッド_\(計算機科学\) "wikilink")。多くのオブジェクト指向言語は単一ディスパッチであり、メソッドは第一引数のデータ型でしか多重化できない。CLOS のメソッドは[総称関数](https://ja.wikipedia.org/wiki/総称関数 "wikilink")にグループ化される。総称関数は同じ名前と引数構造を持つ（ただし個々の引数のデータ型が異なる）メソッドを集めたものである。後の例によりこのことをより良く説明する。

### 弱いカプセル化

多くの動的オブジェクト指向言語（[Python](../Page/Python.md "wikilink")など）と同様、CLOS では[カプセル化](https://ja.wikipedia.org/wiki/カプセル化 "wikilink")が行われない。任意のデータ（スロット）に`slot-value` 関数でアクセス可能である。

データ構造や関数管理にあたっては、CL のプログラマはパッケージ機能を用いる。その意味で、カプセル化はファイル単位やクラス単位ではなくパッケージ単位で行われる。具体的には、スロットの名前を外部に公開するか否かを選ぶことによって未知のプログラムからオブジェクトの中身を保護する。

``` lisp
;;;; パッケージaでa-classを定義する ;;;;
(in-package :a)
(defclass a-class ()
  ((a-slot :initarg :a)))
(export '(a-class))        ;; a:a-slot は公開されない。

;;;; パッケージbでb-classを定義する ;;;;
(in-package :b)
(defclass b-class ()
  ((b-slot :initarg :b)))
(export '(b-class b-slot)) ;; b:b-slot は公開される。

;;;; パッケージcでパッケージaとbをインポートする。
;;;; その中からa-slotとb-slotを呼び出してみる。
(in-package :c)
(use :a) ;; a のシンボルをインポートする
(use :b) ;; b のシンボルをインポートする

(slot-value (make-instance 'a-class :a 1) 'a-slot)
;; --> slot-missing 'a-slot
;; ここでアクセスされているのは c:a-slot である。
;; a:a-slot はインポートされていないので、a-slot は暗黙的に現在のパッケージ c:a-slot として解釈される。
;; 処理系はインスタンスの中の c:a-slot を探すが、そのようなスロットはもちろん存在しない。

(slot-value (make-instance 'b-class :b 2) 'b-slot)
;; --> 2
;; b:b-slot は公開されているため、インポートによってシンボル c:b-slot は b:b-slot と同一オブジェクトとなる。
;; そのため、処理系はインスタンスの中の b:b-slot を見つけることができる。
```

### 多重継承

CLOS は[多重継承](https://ja.wikipedia.org/wiki/多重継承 "wikilink")を許している。[菱形継承](https://ja.wikipedia.org/wiki/菱形継承 "wikilink")問題は、メソッド結合度の戦略によって異なる解決法を選ぶことができる。デフォルトのメソッド結合(**メソッド・コンビネーション**)は、菱形継承問題を**左から右**の規則で処理する。

### 動的クラス変更

CLOSでのオブジェクトのクラスは動的であり、オブジェクトの内容だけでなく「構造」を実行時に変更できる。インスタンスが属するクラスを変更する関数は `(change-class INSTANCE NEW-CLASS-NAME &rest INITARGS)` である。

また、CLOS は実行時に（既にそのクラスがインスタンスを持っていても）クラス定義を変更できる。具体的には、`defclass`を再度評価してクラス定義を変更した際、CLOSは`(make-instances-obsolete CLASS)`を呼び出す。`make-instances-obsolete`は指定されたクラスのすべてのインスタンスに対して`update-instance-for-redefined-class`を呼び出す。`update-instance-for-redefined-class`は新たに追加されたスロットや削除されたスロットの情報を引数として受けとり、同じく引数として受け取ったインスタンスから新しい定義に基づいて新たに作ったインスタンスへ値をコピーする。これら３つのメソッドは継承によりユーザーが書き換え・追加を行うことができる。

### クラスベース

CLOS は[プロトタイプベース](https://ja.wikipedia.org/wiki/プロトタイプベース "wikilink")ではない。インスタンスをあるクラスのメンバーとして作成するには事前に`defclass`によってそのクラスを定義しなければならない。

### MOP : Meta Object Protocol

ANSI 標準の範囲外だが、CLOS の実装に広く採用されている拡張として[メタオブジェクト](https://ja.wikipedia.org/wiki/メタオブジェクト "wikilink")プロトコル([The Common Lisp Object System MetaObject Protocol](http://alu.org/mop/index.html))がある。MOP は CLOS 実装基盤に標準インタフェースを定義し、クラスを[メタクラス](https://ja.wikipedia.org/wiki/メタクラス "wikilink")のインスタンスとして扱い、新たなメタクラスを定義したり、基底クラスの振る舞いを修正したりできる。CLOS MOP は[アスペクト指向プログラミング](../Page/アスペクト指向プログラミング.md "wikilink")の先取りとも言え、実際同じ技術者（Gregor Kiczales など）が関わっている。代表的な機能は*`Generic``   ``Function`*`  (class-slots class) `、*`Class`*`  standard-slot-definition `、など。

MOPは実装系によって扱いが異なるが、その重要性のため、可搬性を担保する試みが行われている。結果、現在では、インターフェースを共通にするライブラリ [Closer to MOP](http://common-lisp.net/project/closer/closer-mop.html) がデファクトスタンダードとなっている\[3\]。

## 実行メソッドの形成

総称関数を呼び出した時、実行する手続きの内容は、その実行時に動的に決定される。コンパイラによる最適化がある場合もある。`declare`宣言によってタイプをコンパイラに指定しない場合、すべての型判定とメソッドの形成が実行時に行われるため、速度は非常に遅くなる。

### 適用可能メソッドを並べる

引数の型と継承関係に応じて、適用してよいメソッドを集める。

クラス`person`がクラス`animal`を継承しているとする。p1とp2は共に`person`のインスタンスである。総称関数`reaction`の以下のような呼び出し

``` lisp

(reaction p1 p2)
```

について、メソッドが以下のように定義されている場合、

``` lisp

(defmethod reaction ((a1 animal) (a2 animal)) (foo)) ; 1
(defmethod reaction ((a1 person) (a2 animal)) (bar)) ; 2
(defmethod reaction ((a1 animal) (a2 person)) (baz)) ; 3
(defmethod reaction ((a1 person) (a2 person)) (bab)) ; 4
```

上の4つはすべて適用可能メソッドである。

### クラス継承順によるメソッドの並べ替え

これら4つのメソッドは、引数オブジェクトの**継承順序(Precedence Order)**に従ってソートされる。 上の例では、呼び出す際のp1とp2が共にクラスpersonのインスタンスであるため、それに最もマッチしている4番目のメソッドが最も高い継承順序を持つ。 継承順序は通常、左側の引数から順に計算される。従って上の例では、2番目と3番目のメソッドを比べた場合、第一引数の適用度が優先されることから、2番目の適用度のほうが高くなる。\[4\]\[5\] 結果的に、メソッドらは4,2,3,1の順でソートされる。

### メソッド結合(メソッド・コンビネーション)

CLOSでは、上のソートによって作られたメソッドのリストに一定の戦略を適用することで、最終的に実際に行う動作を決定する。この戦略のことを**メソッド結合**と呼ぶ。いくつかのバリエーションが標準で定義されている。

他の言語において、あるインスタンスのメソッドを呼び出すときの動作について考えてみよう。そのインスタンスのクラスが親クラスを持つとき、例えばJavaのような言語においては、継承されたメソッドは**上書き**されてしまう。一方,CLOSではそのような通常の**上書き(オーバーライド)**戦略だけにとどまらず、多種多様な戦略がANSI標準で定義され、かつ自由に定義できる。 (ただし、javaは`super`という特殊なメソッドを備えているため、子クラスのメソッドから親のメソッドを呼ぶことができ、言語の柔軟性を高めている。)

メソッド結合法則は総称関数の定義ごとに指定する。**標準メソッド結合**以外のメソッド結合法則を指定した場合、メソッド定義の際には**メソッド指定子(Qualifier)**を指定して、結合法則に固有の機能を使うことを指定しなくてはいけない。それぞれのメソッド結合は複数のメソッド指定子を持つ。なお、すべてのメソッド結合は**`:around`メソッド結合**を持たなくてはならないと定義されている。

#### standard メソッドコンビネーション / 標準メソッド結合

これはjavaのもつ継承戦略と共通点がある。標準メソッド結合では、指定子を指定しない( *unspecified method qualifier* )メソッドのことをプライマリ・メソッド ( *Primary method* )と呼び、これには上書き戦略を用いる。また、その他に:around,:before,:afterメソッド結合を持つ。

メソッド定義の中では、(call-next-method)という特殊な関数を呼ぶことができ、これは次に適用すべきメソッドを呼び出す。このページの上部に、この関係を記した図がある。

#### \+ メソッド結合

これは、すべての適用可能メソッドを実行し、それらの返した値を足し合わせて全体の値として返すという結合方法である。同様のメソッド結合として標準で定義されているものに、`list`,`progn`,`append`などがある。

#### max メソッド結合

これは、すべての適用可能メソッドを実行し、それらの返した値の最大値を全体の値として返すという結合方法である。 同様のメソッド結合として標準で定義されているものに`min`がある。

#### 新たなメソッド結合の定義

`define-method-combination`\[6\]は、ユーザーに、新たなメソッド結合を定義する自由を与える。

## 例

以下に、CLOSを用いて複数のクラスでメソッドを適用する例を示す.

### クラス定義

動物、野生の犬、ペットの犬、人間、ステュワーデス、男というクラスを定義した。

``` lisp
(defclass animal ()
  ((sex :reader sex-of :initarg :sex)))
;; 初期値を設定するためのキーワード引数を :sex に指定する

(defclass named-mixin ()
  ((name :type string :reader name-of :initarg :name)))
;; 名前を持つオブジェクトのmixin
;; :reader 指定により、スロット読み出し用の関数が自動で定義される

(defclass wild-dog (animal)
  ((food :initform :anything)))
(defclass pet-dog (animal named-mixin)
  ((food :initform :dog-food)))
;; :initformにより、インスタンス作成時に値を設定しない場合の初期値を定める

(defclass person (animal named-mixin)
  ((address :accessor adress-of)))
;; accessor指定により、読み書き両方の関数が作られる

(defclass male-mixin ()
  ((sex :initform :male)))
(defclass female-mixin ()
  ((sex :initform :female)))
(defclass stewardess (person female-mixin)
  ())
```

### スタンダード・メソッドコンビネーション

それぞれの継承順に基づいて、何かを言わせてみる。

``` lisp

(defun say (sound)
  (format t sound))
;; 標準出力に書き込む

(defgeneric saysomething (animal))

(defmethod saysomething ((ani animal))
  (say "aaaaa!"))
;; 通常、動作は継承により上書きされる

(defmethod saysomething :before ((p person))
  (say "hi!"))
;; :before 指定により、子孫クラスのメソッドをあとに続いて実行できる

(defmethod saysomething ((st stewardess))
  (say "welcome aboard!"))
;; stewardess は person クラスを継承するので、:before 指定に従い
;;  hi! と言った後に welcome aboard! という
```

### list メソッドコンビネーション

多重ディスパッチと`list`メソッドコンビネーションを用いて、何かが何かに出会った時の反応をリストにして書き出させてみる。

``` lisp

(defgeneric reaction (of to)
  (:method-combination :list))
;; 第一引数がとる第二引数への反応を返す。
;; メソッド結合をstandardからlistへ変更する。
;; そのため、それぞれのメソッドの返り値がlistにまとめられて返る


(defmethod reaction list ((a1 animal) (a2 animal))
  :look)

(defmethod reaction list ((a1 wild-dog) (a2 wild-dog))
  (if (in-same-group a1 a2)
      :sniff  ;; くんくん嗅ぐ
      :bark)) ;; 吠える

(defmethod reaction list ((wild wild-dog) (pet pet-dog))
  :bark-strongly)
(defmethod reaction list ((pet pet-dog) (wild wild-dog))
  :run-away)

(defmethod reaction list ((pet pet-dog) (p person))
  :escort)

(defmethod reaction list ((p person) (pet pet-dog))
  :go-for-a-walk)

(defmethod reaction list ((p1 person) (p2 person))
  :greetings)

(defmethod reaction list ((st stewardess) (p person))
  :welcome-aboard)

(defmethod reaction list ((f1 female-mixin) (p person))
  :watch-clothes)

(defmethod reaction list ((m male-mixin) (f female-mixin))
  :watch-hip-tits-and-waist)

(reaction (make-instance 'animal)
      (make-instance 'animal))
;; --> (:LOOK)


(reaction (make-instance 'man)
      (make-instance 'stewardess))
;; --> (:GREETINGS :LOOK :WATCH-HIP-TITS-AND-WAIST)


(reaction (make-instance 'stewardess)
      (make-instance 'man))
;; --> (:WELCOME-ABOARD :GREETINGS :LOOK :WATCH-CLOTHES)


(reaction (make-instance 'wild-dog)
      (make-instance 'man))
;; --> (:LOOK)

(reaction (make-instance 'pet-dog)
          (make-instance 'man))
;; --> (:ESCORT :LOOK)


(reaction (make-instance 'pet-dog)
      (make-instance 'wild-dog))
;; --> (:RUN-AWAY :LOOK)
```

## 参考文献

  - "[CommonLoops: merging Lisp and object-oriented programming](http://portal.acm.org/citation.cfm?id=28700)", by Daniel G. Bobrow, Kenneth Kahn, Gregor Kiczales, Larry Masinter, Mark Stefik, Frank Zdybel. 1986, Portland, Oregon, United States. Pages 17 - 29 of the *Conference on Object Oriented Programming Systems Languages and Applications*, ISSN 0362-1340.
  - "A History and Description of CLOS", by Jim **Veitch**. Pages 107-158 of *Handbook of Programming Languages, Volume IV: Functional and Logic Programming Languages*, ed. Peter H. Salus. 1998 (1st edition), Macmillian Technical Publishing; ISBN 1-57870-011-6
  - Gregor Kiczales, Jim des Rivieres, and Daniel G. Bobrow, *The Art of the Metaobject Protocol*, 1991, MIT Press. ISBN 0-262-61074-4
  - Sonya Keene, *Object-Oriented Programming in Common Lisp: A Programmer's Guide to CLOS*, 1988, Addison-Wesley. ISBN 0-201-17589-4.

## 脚注

<references/>

## 外部リンク

  - [The Common Lisp Object System: An Overview](http://www.dreamsongs.com/NewFiles/ECOOP.pdf) by Richard P. Gabriel and Linda DeMichiel
  - *Common Lisp HyperSpec*, [Chapter 7: *Objects*](http://www.lispworks.com/documentation/HyperSpec/Body/07_.htm)

[Category:LISP](https://ja.wikipedia.org/wiki/Category:LISP "wikilink") [Category:オブジェクト指向](https://ja.wikipedia.org/wiki/Category:オブジェクト指向 "wikilink")

1.  「CLOS は標準規格である。複数のベンダーがCLOSを提供している。CLOS やその一部は他のLISP系言語である EuLisp や EmacsLisp にオブジェクト指向を導入するのに使われている」 p. 110 （Veitch 1998）
2.  p. 108 （Veitch 1998）
3.  <http://www.cliki.net/Current%20recommended%20libraries>
4.  ただし、このオプションは`defgeneric`の`:argument-precedence-order`というオプションによって逆順に変更できる。
5.  <http://www.lispworks.com/documentation/HyperSpec/Body/07_ffab.htm>
6.  <http://www.lispworks.com/documentation/HyperSpec/Body/m_defi_4.htm#define-method-combination>
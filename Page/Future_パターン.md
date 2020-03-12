> この記事は[Future ](https://ja.wikipedia.org/wiki/Future_)から翻訳されています。


**future**, **promise**, **delay** とは、[プログラミング言語](../Page/プログラミング言語.md "wikilink")における[並列処理](https://ja.wikipedia.org/wiki/並列処理 "wikilink")の[デザインパターン](https://ja.wikipedia.org/wiki/デザインパターン_\(ソフトウェア\) "wikilink")。何らかの処理を別の[スレッドで処理させる際](../Page/スレッド_\(コンピュータ\).md "wikilink")、その処理結果の取得を必要になるところまで後回しにする手法。処理を[パイプライン化させる](../Page/パイプライン処理.md "wikilink")。[1977年](../Page/1977年.md "wikilink")に考案され、現在ではほとんどのプログラミング言語で利用可能。

## 概要

[カール・ヒューイット](../Page/カール・ヒューイット.md "wikilink")は、2つの点で future の方が promise よりも適した用語であるとしている。第一に promise（約束）は必ずしも将来の時点のことを意味しないため、future（未来）よりも曖昧である。第二に promise は単なる言語表現だが、future は現物（actuals）に対する先物（futures）という意味もある（つまり、実際の物に対する代用品）。

future という構文が最初に紹介されたのは[1977年](../Page/1977年.md "wikilink")、Henry Baker と[カール・ヒューイット](../Page/カール・ヒューイット.md "wikilink")の論文でのことであった。future（promise）の使用により、[分散システムにおける遅延を劇的に減少させることができる](../Page/分散コンピューティング.md "wikilink")。例えば[アクターモデル](../Page/アクターモデル.md "wikilink")のようにメッセージのパイプライン化が可能であり、これを[E言語](https://ja.wikipedia.org/wiki/E言語 "wikilink")や[Aliceでは](https://ja.wikipedia.org/wiki/Alice_\(プログラミング言語\) "wikilink") **promise pipelining** と呼ぶ[1](http://www.erights.org/elib/distrib/pipeline.html)。

## パイプライン化

一般的なRPCで次のような式を考える。

`t3 := (x.a()).c(y.b())`

これは、次のように展開できる。

`t1 := x.a(); t2 := y.b(); t3 := t1.c(t2)`

これを解釈すると、`t1` および `t2` の値が定まらないと `t3` の値は計算できない。future を使うとこの式が次のように表される。

`t3 := `*`future`*` (`*`future`*` x.a()).c(`*`future`*` y.b())`

これを展開すると次のようになる。

`t1 := `*`future`*` x.a(); t2 := `*`future`*` y.b(); t3 := `*`future`*` t1.c(t2)`

このようにすると `t3` は即座に計算される。ただし、`t3` から情報を得ようとすると待たされる。

## 実装

future構文は MultiLisp や Act1 といったプログラミング言語で実装された。[並行論理プログラミング](https://ja.wikipedia.org/wiki/並行論理プログラミング "wikilink")言語における論理変数もよく似ている。これは当初 Prolog with Freeze や IC Prolog で使われ、Relational Language、[Concurrent Prolog](https://ja.wikipedia.org/wiki/Concurrent_Prolog "wikilink")、[PARLOG](https://ja.wikipedia.org/wiki/PARLOG "wikilink")、[GHC](https://ja.wikipedia.org/wiki/Guarded_Horn_Clauses "wikilink")、[KL1](https://ja.wikipedia.org/wiki/KL1 "wikilink")、[Strand](https://ja.wikipedia.org/wiki/Strand "wikilink")、Vulcan、Janus、[Mozart/Oz](../Page/Oz_\(プログラミング言語\).md "wikilink")、Flow Java、Alice といった言語で真の並行性プリミティブとなった。Concurrent ML のような単一代入規則型[データフロー言語](https://ja.wikipedia.org/wiki/データフロー言語 "wikilink")の I-var は並行論理変数とよく似ている。

future による遅延最小化のようなパイプライン化技法はまず[アクターモデル](../Page/アクターモデル.md "wikilink")で生み出され、1988年に[バーバラ・リスコフ](../Page/バーバラ・リスコフ.md "wikilink")が再発明し、1989年ごろには[ザナドゥ計画](../Page/ザナドゥ計画.md "wikilink")でも再発明されている。

future, promise, 並行論理変数, データフロー変数, I-var をサポートする言語:

  - ABCL/f\[1\]
  - Act1
  - [Alice ML](https://ja.wikipedia.org/wiki/Alice_ML "wikilink")
  - [AmbientTalk](https://ja.wikipedia.org/wiki/AmbientTalk "wikilink") (first-class resolvers と read-only promises を含む)
  - [Clojure](https://ja.wikipedia.org/wiki/Clojure "wikilink")\[2\]
  - [C++](../Page/C++.md "wikilink") ([C++11](https://ja.wikipedia.org/wiki/C++11 "wikilink")以降の std::future と std::promise)
  - [C\#](../Page/C_Sharp.md "wikilink") (C\# 5.0以降の await キーワード)
  - [Concurrent Prolog](https://ja.wikipedia.org/wiki/Concurrent_Prolog "wikilink")
  - [Dart](https://ja.wikipedia.org/wiki/Dart "wikilink")
  - [Flow Java](https://ja.wikipedia.org/wiki/:w:Flow_Java "wikilink")
  - Glasgow [Haskell](../Page/Haskell.md "wikilink") (I-vars and M-vars only)
  - [GHC](https://ja.wikipedia.org/wiki/Guarded_Horn_Clauses "wikilink")
  - [Id](https://ja.wikipedia.org/wiki/Id_\(programming_language\) "wikilink") (I-vars and M-vars only)
  - [Io](../Page/Io_\(プログラミング言語\).md "wikilink") \[3\]
  - [Java](https://ja.wikipedia.org/wiki/Java "wikilink") -  より
  - [JavaScript](../Page/JavaScript.md "wikilink") - [ECMAScript](../Page/ECMAScript.md "wikilink") 2015 (ES6) より
  - [KL1](https://ja.wikipedia.org/wiki/KL1 "wikilink")（その実装として[KLIC](http://www.klic.org/software/klic/index.ja.html)がある）
  - [Lucid](https://ja.wikipedia.org/wiki/Lucid "wikilink") (データフローのみ)
  - [MultiLisp](https://ja.wikipedia.org/wiki/MultiLisp "wikilink")
  - [Oxygene](https://ja.wikipedia.org/wiki/Oxygene "wikilink")
  - [Oz](../Page/Oz_\(プログラミング言語\).md "wikilink") version 3\[4\]（その実装として[Mozart Programming System](http://www.mozart-oz.org/)がある）
  - [Python](../Page/Python.md "wikilink") 3.2, [PEP 3148](http://www.python.org/dev/peps/pep-3148/) で提案
  - [R](../Page/R.md "wikilink") (promises for lazy evaluation - still single threaded)
  - [Racket](https://ja.wikipedia.org/wiki/Racket "wikilink")\[5\]
  - [Scala](../Page/Scala.md "wikilink")
  - [Scheme](../Page/Scheme.md "wikilink")
  - [Visual Basic .NET](../Page/Visual_Basic_.NET.md "wikilink") (VB.NET 11以降の Await キーワード)
  - [μC++](https://ja.wikipedia.org/wiki/μC++ "wikilink")
  - C\#やVB.NETなどの[.NET Framework言語全般](https://ja.wikipedia.org/wiki/.NET_Framework "wikilink"): .NET 4以降のタスク並列ライブラリ ([Parallel Extensions](https://ja.wikipedia.org/wiki/:w:Parallel_Extensions "wikilink"))

加えて、promise pipelining をサポートする言語:

  - [Joule言語](http://www.erights.org/history/joule/)
  - [E言語](http://erights.org/)

非標準ライブラリによる実装:

  - [Common Lisp](../Page/Common_Lisp.md "wikilink"): [Eager Future2](http://common-lisp.net/project/eager-future/), [PCall](http://marijnhaverbeke.nl/pcall/)
  - C++: [Boost library](http://www.boost.org/doc/libs/release/doc/html/thread.html), [Dlib C++ Library](http://dlib.net/api.html#thread_pool)
  - [Groovy](../Page/Groovy.md "wikilink"): [GPars](http://gpars.codehaus.org)
  - [JavaScript](../Page/JavaScript.md "wikilink"):
      - [Cujo.js](http://cujojs.com) - [CommonJS Promises/A](http://wiki.commonjs.org/wiki/Promises/A) に基づく promise を [when.js](https://github.com/cujojs/when) が提供
      - [Dojo Toolkit](https://ja.wikipedia.org/wiki/Dojo_Toolkit "wikilink") - [promises](http://dojotoolkit.org/documentation/tutorials/1.6/promises/) と Twisted style Deferred を提供
      - [jQuery](https://ja.wikipedia.org/wiki/jQuery "wikilink") - [CommonJS Promises/A](http://wiki.commonjs.org/wiki/Promises/A) に基づく物を [Deferred Object](http://api.jquery.com/category/deferred-object/) で提供
      - [node-promise](https://github.com/kriszyp/node-promise)
      - [Q](http://documentup.com/kriskowal/q)
      - [RSVP.js](https://github.com/tildeio/rsvp.js)
  - [Java](https://ja.wikipedia.org/wiki/Java "wikilink"): [JQuery](https://ja.wikipedia.org/wiki/JQuery "wikilink").Deferred に似た振る舞いを [JDeferred](http://jdeferred.org) の Deferred/Promise API が提供
  - [Objective-C](../Page/Objective-C.md "wikilink"): [MAFuture](https://github.com/mikeash/MAFuture) ([reference](http://www.mikeash.com/pyblog/friday-qa-2010-02-26-futures.html))
  - [OCaml](../Page/OCaml.md "wikilink"): [Lazy](http://caml.inria.fr/pub/docs/manual-ocaml/libref/Lazy.html) モジュールが lazy explicit future を実装
  - [Perl](../Page/Perl.md "wikilink"): [Future](http://metacpan.org/module/Future), [Reflex](http://metacpan.org/module/Reflex/)
  - [PHP](../Page/PHP_\(プログラミング言語\).md "wikilink"): [React/Promise](https://github.com/reactphp/promise)
  - [Python](../Page/Python.md "wikilink"): [pythonfutures](http://code.google.com/p/pythonfutures/), [Twisted's](https://ja.wikipedia.org/wiki/:w:Twisted_\(software\) "wikilink") [Deferreds](http://twistedmatrix.com/documents/current/core/howto/defer.html)
  - [Ruby](../Page/Ruby.md "wikilink"): [Promise](http://rubygems.org/gems/promise) gem

## 参考文献

  - Henry Baker and Carl Hewitt **The Incremental Garbage Collection of Processes** Proceeding of the Symposium on Artificial Intelligence Programming Languages. SIGPLAN Notices 12, August 1977.
  - Henry Lieberman. **Thinking About Lots of Things at Once without Getting Confused: Parallelism in Act 1** MIT AI memo 626. May 1981.
  - Henry Lieberman. **A Preview of Act 1** MIT AI memo 625. June 1981.

## 脚注

<references/>

## 外部リンク

  - [Portland Pattern Repository](http://c2.com/ppr/)
      - [Future Value](http://c2.com/cgi/wiki?FutureValue)
      - [Promise Pipelining](http://c2.com/cgi/wiki?PromisePipelining)

[Category:分散処理](https://ja.wikipedia.org/wiki/Category:分散処理 "wikilink") [Category:並行計算](https://ja.wikipedia.org/wiki/Category:並行計算 "wikilink") [Category:アクターモデル](https://ja.wikipedia.org/wiki/Category:アクターモデル "wikilink") [Category:プログラミング言語の構文](https://ja.wikipedia.org/wiki/Category:プログラミング言語の構文 "wikilink")

1.
2.
3.
4.
5.
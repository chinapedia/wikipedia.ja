> この記事は[Pyrex](https://ja.wikipedia.org/wiki/Pyrex)から翻訳されています。


**Pyrex** は、[Python](../Page/Python.md "wikilink")の拡張[モジュール](https://ja.wikipedia.org/wiki/モジュール "wikilink")の作成を補助する目的で開発された[プログラミング言語](../Page/プログラミング言語.md "wikilink")である。Python は拡張モジュールを記述するための[C言語](../Page/C言語.md "wikilink")の[APIを提供している](../Page/アプリケーションプログラミングインタフェース.md "wikilink")。[関数と](https://ja.wikipedia.org/wiki/サブルーチン "wikilink")[データ型](https://ja.wikipedia.org/wiki/データ型 "wikilink")をC言語で記述することができ、記述したモジュールは Python からアクセスすることができる。既存の C [ライブラリ](../Page/ライブラリ.md "wikilink") の関数とデータ型を Python オブジェクトとしてラップし、Python から利用可能にすることもできる。

こうしたプロセスの自動化を補助する [SWIG](https://ja.wikipedia.org/wiki/SWIG "wikilink") のようなツールも存在するが、Python から外部のライブラリを利用可能にすることに限定されており、API の変更が必要な場合、再度グルーコードを手で記述する必要がある。このような場合に Pyrex は適している。Pyrex ではユーザーが C コードに直接アクセス可能な Python に似た言語を用いて、拡張モジュールを記述することを可能にする。

Pyrex と Python の文法が似ているため、Python のモジュールを記述するのは容易であり、C や C++ などの異なる言語を習得する必要がない。また、グルーコードを書く必要もない。C のヘッダファイルと、拡張モジュールでアクセスする必要のある[列挙型](../Page/列挙型.md "wikilink")、データ型、関数を指定するだけでよい。Pyrex コンパイラが必要なグルーコードを自動的に生成し、Pyrex コードを動作する Python モジュールにコンパイルしてくれる。

## 関連項目

  - [Python](../Page/Python.md "wikilink")
  - [Cython](https://ja.wikipedia.org/wiki/Cython "wikilink")

## 外部リンク

  - [Official homepage](http://www.cosc.canterbury.ac.nz/~greg/python/Pyrex/)
  - [Python.org](http://www.python.org/)
  - [Pyrex Installation on Windows](http://wiki.python.org/moin/PyrexOnWindows)
  - [Cython, the next version of Pyrex](http://www.cython.org/)

[Category:Python](https://ja.wikipedia.org/wiki/Category:Python "wikilink")
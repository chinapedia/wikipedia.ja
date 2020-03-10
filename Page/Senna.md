> この記事は[Senna](https://ja.wikipedia.org/wiki/Senna)から翻訳されています。


**Senna**（せな、Senna: An Embeddable Fulltext Search Engine）は、[未来検索ブラジル](https://ja.wikipedia.org/wiki/未来検索ブラジル "wikilink")によって開発されている[オープンソース](../Page/オープンソース.md "wikilink")の[全文検索](../Page/全文検索.md "wikilink")エンジンである。検索速度が高速なことから、「音速の貴公子」と呼ばれた[アイルトン・セナ](../Page/アイルトン・セナ.md "wikilink")にちなんで名づけられた。

## 概要

[MeCab](../Page/MeCab.md "wikilink")による[形態素解析](../Page/形態素解析.md "wikilink")の結果を用いた単語ベースのインデックスと、[N-gramによるトークン抽出を用いたインデックスの両方を作成することができる](https://ja.wikipedia.org/wiki/全文検索#N-Gram "wikilink")。

ライセンスは[LGPL](https://ja.wikipedia.org/wiki/LGPL "wikilink")。[UNIX](../Page/UNIX.md "wikilink")系OS及び[Windows](https://ja.wikipedia.org/wiki/Windows "wikilink")で動作する。

バグフィックスを除いた新たな開発は事実上終了しており、開発元の未来検索ブラジルでは、後継となる検索エンジンとして『[groonga](https://ja.wikipedia.org/wiki/groonga "wikilink")』（ぐるんが）の開発を進めている。

## 特徴

  - 高速なインデックスの更新
      -
        一般的に、作成済みの全文検索インデックスに対する新たなレコードの追加は負荷がかかる。Sennaでは更新のためにバッファを設けたり、[転置インデックス](https://ja.wikipedia.org/wiki/転置インデックス "wikilink")の[データ構造](../Page/データ構造.md "wikilink")を工夫して、高速な更新を実現している。
  - 高精度な検索
      -
        単語ベースのインデックスを作成することにより、単語境界と一致する文書を優先的に検索する。よって、適合率の高い検索を行うことができる。適合率の高い検索とは、ノイズの少ない検索のことを指す。
        また、[転置インデックス](https://ja.wikipedia.org/wiki/転置インデックス "wikilink")のキーとして、部分一致が可能な単語表を採用している。よって、単語境界と一致しない文書も検索することができる。よって、再現率の高い検索を行うことができる。再現率の高い検索とは、漏れの少ない検索のことを指す。
  - 組み込み型ライブラリ
      -
        Sennaは単体では機能しない、ライブラリ形式として提供される。
        [MySQL](https://ja.wikipedia.org/wiki/MySQL "wikilink")に[パッチ](../Page/パッチ.md "wikilink")を当てることによって、MySQLの全文検索機能でSennaを利用することが可能となる。MySQLの全文検索機能は、バージョン5.1までは日本語に対応していないが、Sennaを利用することによって、高速な日本語検索が可能となる。
        [PostgreSQL](https://ja.wikipedia.org/wiki/PostgreSQL "wikilink")も、[Ludia](https://ja.wikipedia.org/wiki/Ludia "wikilink")もしくは[textsearch_senna](http://textsearch-ja.projects.postgresql.org/textsearch_senna.html)を利用することにより、Sennaによる全文検索が可能となる。

## バインディング

  - [Ruby](../Page/Ruby.md "wikilink")
      - Sennaを利用できる[Ruby](../Page/Ruby.md "wikilink")バインディングが標準で附属している。
  - [Perl](../Page/Perl.md "wikilink")
      - [CPAN::Senna](http://search.cpan.org/dist/Senna/)
      - [CPAN::Tie::Senna](http://search.cpan.org/dist/Senna/)
  - [Python](../Page/Python.md "wikilink")
      - [Pyrost](http://www.void.in/wiki/SWIG-senna)
      - [PySenna](http://sourceforge.jp/projects/pysenna/)
  - [Java](https://ja.wikipedia.org/wiki/Java "wikilink")
      - [Senna-Java](http://sourceforge.jp/projects/senna-java/)

[PHPバインディングはメンテナンスされておらず](../Page/PHP_\(プログラミング言語\).md "wikilink")、現在のSennaでは利用できない。現在対応版が開発中であり、Sennaのバージョン1.1から利用可能になるとされている。

## 利用されているアプリケーション

  - [MySQL](https://ja.wikipedia.org/wiki/MySQL "wikilink")
      - [Tritonn](http://qwik.jp/tritonn/)を用いて全文検索を行うことができる。
  - [PostgreSQL](https://ja.wikipedia.org/wiki/PostgreSQL "wikilink")
      - [Ludia](https://ja.wikipedia.org/wiki/Ludia "wikilink"): [NTTデータ](https://ja.wikipedia.org/wiki/NTTデータ "wikilink")が開発したPostgreSQLの組み込み全文検索。[LGPLに沿ってソースコードが公開されている](../Page/GNU_Lesser_General_Public_License.md "wikilink")。
      - [textsearch_senna](http://textsearch-ja.projects.postgresql.org/textsearch_senna.html): PostgreSQL 8.3 以降にも対応した組み込み全文検索。

## 利用されているWebサービス

以下のWebサービスにおいて、Sennaが利用されている。

  - [GREE](http://gree.jp)
  - [はてな検索](http://search.hatena.ne.jp/keyword?mode=top)
  - [タワーレコード商品検索](http://search.tower.jp/)
  - [八重山毎日新聞](http://www.y-mainichi.co.jp/)
  - [freeml](http://sns.freeml.com/)
  - [○×ソーシャル コトノハ](http://kotonoha.cc)
  - [iYappo 携帯サイト検索](http://i.yappo.jp/)
  - [MyWiki](http://mywiki.jp/)
  - [C-BoX](http://cbox.ryne.jp/s.php)
  - [pixiv](http://www.pixiv.net/)

## 関連項目

  - [Namazu](../Page/Namazu.md "wikilink")
  - [Hyper Estraier](../Page/Hyper_Estraier.md "wikilink")
  - [Lucene](https://ja.wikipedia.org/wiki/Lucene "wikilink")

## 参考文献

  - [オープンソースマガジン 2006年4月号 いざ、次世代検索エンジンへ](http://qwik.jp/senna/publication.html#94012e0c753d8dcd580ba3eb0fa0ea8a)
  - [ACM SIGMOD日本支部第35回大会 発表資料](http://qwik.jp/senna/publication.html#853589e862b4645883fe9ff31a7f714a)

## 外部リンク

  - [Senna 組み込み型全文検索エンジン](http://qwik.jp/senna/FrontPageJ.html)

[Category:全文検索](https://ja.wikipedia.org/wiki/Category:全文検索 "wikilink") [Category:オープンソースソフトウェア](https://ja.wikipedia.org/wiki/Category:オープンソースソフトウェア "wikilink")
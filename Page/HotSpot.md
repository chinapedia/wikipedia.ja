> この記事は[HotSpot](https://ja.wikipedia.org/wiki/HotSpot)から翻訳されています。


**HotSpot**（ホットスポット）は[オラクル](https://ja.wikipedia.org/wiki/オラクル_\(企業\) "wikilink")（旧[サン・マイクロシステムズ](../Page/サン・マイクロシステムズ.md "wikilink")）が提供している[Java仮想マシン](../Page/Java仮想マシン.md "wikilink")で使われている高速化のための技術の名称。デスクトップ向け・サーバ向け・組み込み環境向け ([Java ME](../Page/Java_Platform,_Micro_Edition.md "wikilink")\[1\]) がある。[性能](https://ja.wikipedia.org/wiki/性能 "wikilink")を改善するために[ジャストインタイムコンパイル方式](https://ja.wikipedia.org/wiki/ジャストインタイムコンパイル方式 "wikilink")、[適応的最適化](https://ja.wikipedia.org/wiki/適応的最適化 "wikilink") ([adaptive optimization](https://ja.wikipedia.org/wiki/:en:Adaptive_optimization "wikilink")) などの技術を使っている。

## 歴史

HotSpotは、[1999年](../Page/1999年.md "wikilink")[4月27日](../Page/4月27日.md "wikilink")に最初にリリースされ、[1994年](../Page/1994年.md "wikilink")に設立された小さな新興企業[Animorphic](https://ja.wikipedia.org/wiki/Animorphic "wikilink")の名前で事業経営中だった有限会社 Longview Technologies によって独自に開発された。[1997年](https://ja.wikipedia.org/wiki/1997年 "wikilink")には有限会社 Lonview Technologies（Animorphicの名前で事業経営中）はサンに買収された。当初Java 1.2で[アドオン](https://ja.wikipedia.org/wiki/アドオン "wikilink")として利用可能だったHotSpotはJava 1.3からサンの標準のJava仮想マシンとなった\[2\]\[3\]。

その名前は[Javaバイトコード](https://ja.wikipedia.org/wiki/Javaバイトコード "wikilink")を実行する際の挙動に由来する。HotSpotは頻繁に繰り返し実行されるコード領域すなわち「[ホットスポット](../Page/ホットスポット.md "wikilink")」\[4\]を絶えず解析する。これらは、性能に重大な影響を与えるコードを標的として[最適化を重点的に行い](../Page/最適化_\(情報工学\).md "wikilink")、その他のコードには最小限の最適化で済ませることで[オーバーヘッド](https://ja.wikipedia.org/wiki/オーバーヘッド "wikilink")を小さくし、高性能な実行を実現する。HotSpotはJava仮想マシンの中でも最高性能が得られると極めて高い評価を得ている。実際にはまれだが、理論上はJava仮想マシンの adaptive optimization が[C++](../Page/C++.md "wikilink")あるいは[アセンブリ言語](../Page/アセンブリ言語.md "wikilink")を用いた手動最適化に勝る場合もある\[5\]。

## 設計

サンの[JREによれば](../Page/Java_Runtime_Environment.md "wikilink")、HotSpotはクライアント版およびサーバ版と呼ばれる二つの互換実装からなる。クライアント版は必要不可欠なクラスやメソッドのみを素速くロードしコンパイルするようチューニングする。サーバ版は、よりゆっくりロードを行うが、より高性能な高度に最適化された[JITコンパイル結果を産出することに](https://ja.wikipedia.org/wiki/ジャストインタイムコンパイル方式 "wikilink")、より尽力する。

## ライセンス

[2006年](../Page/2006年.md "wikilink")[11月13日](../Page/11月13日.md "wikilink")にはサンのJava仮想マシンと[JDKは](../Page/Java_Development_Kit.md "wikilink")[GPLライセンスの下で利用できるようになった](../Page/GNU_General_Public_License.md "wikilink")。

## 脚注

### 注釈

### 出典

## 関連項目

  - [Java仮想マシンの一覧](https://ja.wikipedia.org/wiki/Java仮想マシンの一覧 "wikilink") ([:en:List of Java virtual machines](https://ja.wikipedia.org/wiki/:en:List_of_Java_virtual_machines "wikilink"))

## 外部リンク

  - [Java SE HotSpot at a Glance](http://www.oracle.com/technetwork/java/javase/tech/index-jsp-136373.html) - Oracle

  - [Java HotSpot VM Options](http://www.oracle.com/technetwork/java/javase/tech/vmoptions-jsp-140102.html) - Oracle

      - [和訳](https://kuromoyo.hatenadiary.org/entry/20120101/1325358083)

  - [Java HotSpot VM オプション](http://docs.oracle.com/cd/E19683-01/816-3973/6ma7ftaqh/index.html) - Java 2 SDK 開発ガイド (Solaris 編)(注意: 2010年作成) - Oracle

  - [HotSpot VM FAQ](http://www.oracle.com/technetwork/java/hotspotfaq-138619.html) - Oracle

  - [The History of the Strongtalk Project](http://strongtalk.org/history.html)

  -
  - [Java仮想マシン(JVM)のチューニング](http://docs.oracle.com/cd/E28613_01/web.1211/b65905/jvm_tuning.htm) - Oracle (Oracle 12cリリース1用)

[Category:Java仮想マシン](https://ja.wikipedia.org/wiki/Category:Java仮想マシン "wikilink")

1.  [Java ME テクノロジー － CDC](https://www.oracle.com/technetwork/jp/java/javame/tech/cdc-329738-ja.html)
2.
3.  [Java HotSpot(TM) Client Virtual Machine および Java HotSpot(TM) Server Virtual Machine](https://docs.oracle.com/javase/jp/1.3/guide/performance/hotspot.html)
4.  、「人気のある場所」の意味。直訳すると「熱い場所」。
5.
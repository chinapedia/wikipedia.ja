> この記事は[Bridge ](https://ja.wikipedia.org/wiki/Bridge_)から翻訳されています。


**Bridge パターン**（ブリッジ・パターン）とは、[GoF](https://ja.wikipedia.org/wiki/ギャング・オブ・フォー_\(情報工学\) "wikilink")（Gang of Four; 4人のギャングたち）によって定義された[デザインパターンの](https://ja.wikipedia.org/wiki/デザインパターン_\(ソフトウェア\) "wikilink")1つである。 「橋渡し」のクラスを用意することによって、クラスを複数の方向に拡張させることを目的とする。

## クラス図

Bridge パターンの[クラス図](../Page/クラス図.md "wikilink")を以下に挙げる。

[500px](https://ja.wikipedia.org/wiki/ファイル:Bridge_UML_class_diagram.svg "wikilink")

## 利用例

Bridge パターンの適用が望ましいクラス構造は、例えば以下のようなものである。

[center](https://ja.wikipedia.org/wiki/ファイル:Bridge-adoptable_UML_class_diagram_example.svg "wikilink")

この例では、まず Dishware（食器）クラスから Plate（皿）と Bowl（ボウル）クラスが派生している。 さらに、Plate からは WoodenPlate（木製の皿）と GlassPlate（ガラス製の皿）が、 Bowl からは WoodenBowl（木製のボウル）と GlassBowl（ガラス製のボウル）が派生している。

このクラス階層は、以下に挙げる問題をはらんでいる。

  - クラスの追加が困難である。仮にプラスチック製の食器を新たにサポートしようとする場合、Plate クラスと Bowl クラスのそれぞれを[継承しなければならない](../Page/継承_\(プログラミング\).md "wikilink")。あるいは Dishware クラスのサブクラスとして例えば Cup クラスを追加する場合、WoodenCup や GlassCup を同時に作成しなければならない。
  - コードの複製が発生する。例に挙げた WoodenPlate と WoodenBowl, GlassPlate と GlassBowl はそれぞれ同じ材質の食器であるため、内部的に似たような性質を持っているかもしれない。しかしながら、継承関係の都合上これらのクラスはすべて個別に定義しなければならず、結果として同じようなコードを別途に記述しなければならなくなる。

この問題が起こる理由は、クラス階層の中に複数の継承関係が混在していることである。 上の例において、Dishware と Plate および Bowl の関係は、**食器の種類**による継承関係とみなすことができ、 一方で Plate と WoodenPlate および GlassPlate の関係は、**食器の材質**による継承関係とみなすことができる。 このように複数の継承関係が存在することにより、一つの継承関係が他の継承関係に悪影響を及ぼすことになる。

このクラス構造は、Bridge パターンを適用することによって以下のように改善することができる。

[center](https://ja.wikipedia.org/wiki/ファイル:Bridge-adopted_UML_class_diagram_example.svg "wikilink")

このクラス図では Dishware から派生する継承関係は食器の種類のみであり、材質に関する情報は Material（素材）クラスに[委譲](../Page/委譲.md "wikilink")している。 この構造により、種類と材質はそれぞれ独立して拡張することができ、クラスの数も減らすことが出来る。

## 関連項目

  - [デザインパターン](https://ja.wikipedia.org/wiki/デザインパターン_\(ソフトウェア\) "wikilink")
  - [継承](../Page/継承_\(プログラミング\).md "wikilink")

[Category:デザインパターン_(ソフトウェア)](https://ja.wikipedia.org/wiki/Category:デザインパターン_\(ソフトウェア\) "wikilink")
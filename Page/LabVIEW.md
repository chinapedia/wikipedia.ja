> この記事は[LabVIEW](https://ja.wikipedia.org/wiki/LabVIEW)から翻訳されています。


**LabVIEW**は[グラフィック型言語](https://ja.wikipedia.org/wiki/グラフィック型言語 "wikilink")によってプログラミングすることのできる開発環境であり、主に計測用に用いられる。**Lab**oratory **V**irtual **I**nstrumentation **E**ngineering **W**orkbenchを略したもの。

LabVIEW では、通常の言語でいう関数にあたるVI（Virtual Instruments）を表す[アイコン](../Page/アイコン.md "wikilink")をウィンドウ平面上に配置し、VIとVIの間を配線することによってデータフローを表す。[for文](https://ja.wikipedia.org/wiki/for文 "wikilink")や[if文](https://ja.wikipedia.org/wiki/if文 "wikilink")などのプログラム構造は長方形の枠を描画して構成する。このように作成されたプログラムは、単独で実行させることも、新たなVIとして他のプログラム上で再利用することも可能である。

各 VI の実行順序はデータフローによって決定される。すなわち、各 VI を実行するために必要な入力データがそろった時点で実行される。互いに依存しないデータフローがあり、かつ、それが適切である場合、LabVIEW 実行システムは、それらのデータフローを個別のスレッドで実行しようとする。たとえば、データを共有しない 2 つの While ループがある場合、それらのループは別個のスレッドで実行される。マルチコア CPU 上で動作する Windows XP や Vista は複数スレッドが渡された際に、各スレッドを別々のコアで実行しようとするので、各 While ループが別個のコアで実行されることが期待できる。

LabVIEW は、機能や入出力関係、データフローが直感的に把握できる点でテキスト型言語に対し優れている。また、データフローによって自動的に並列処理が実行されることも、大きな違いである。一方、静的型付けする言語であるため、実行時に型が決定するようなコードを記述することは難しい。また、開発環境と実行システムが分離できないため、C 言語などのようなマクロ定義ができない。

## 関連項目

  - [データフロー言語](https://ja.wikipedia.org/wiki/データフロー言語 "wikilink")
  - [ビジュアルプログラミング言語](../Page/ビジュアルプログラミング言語.md "wikilink")
  - [NAG数値計算ライブラリ](../Page/NAG数値計算ライブラリ.md "wikilink")

## 脚注

## 外部リンク

  - [LabVIEWグラフィカル開発環境](http://www.ni.com/labview/ja/)
  - [LabVIEW™からNAG数値計算ライブラリを利用する方法](http://www.nag-j.co.jp/naglib/usingDLL/usingDLLfromLabview.htm)

[Category:プログラミング言語](https://ja.wikipedia.org/wiki/Category:プログラミング言語 "wikilink") [Category:Linux向け数値解析ソフトウェア](https://ja.wikipedia.org/wiki/Category:Linux向け数値解析ソフトウェア "wikilink")
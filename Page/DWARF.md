> この記事は[DWARF](https://ja.wikipedia.org/wiki/DWARF)から翻訳されています。


**DWARF** とは、広く使われている[デバッグ](../Page/デバッグ.md "wikilink")用データフォーマットの規格である。当初[ELFと共に設計されたが](https://ja.wikipedia.org/wiki/Executable_and_Linkable_Format "wikilink")、[オブジェクトファイル](https://ja.wikipedia.org/wiki/オブジェクトファイル "wikilink")のフォーマットとは独立している\[1\]。名称は "[ELF](https://ja.wikipedia.org/wiki/Executable_and_Linkable_Format "wikilink")" から発想した駄洒落だが、「Debug With Attributed Record Format の頭字語」という説もある\[2\]。

## 歴史

DWARF の最初のバージョンは過剰な容量を必要とするものだったため、様々な符号化手法によってサイズを削減した互換性のない DWARF-2 に置き換えられた。当初はすぐには広まらなかった。例えば、[サン・マイクロシステムズ](../Page/サン・マイクロシステムズ.md "wikilink")は[Solaris](../Page/Solaris.md "wikilink")への移行の際に[ELFを採用したが](https://ja.wikipedia.org/wiki/Executable_and_Linkable_Format "wikilink")、従来からある [stabs](https://ja.wikipedia.org/wiki/stabs "wikilink") の継続使用を選択し、この組合せを "stabs-in-elf" と称した。[Linux](https://ja.wikipedia.org/wiki/Linux "wikilink")もこれに倣い、DWARF-2 は1990年代末までデフォルトにはならなかった。

[2005年](https://ja.wikipedia.org/wiki/2005年 "wikilink")[12月20日](../Page/12月20日.md "wikilink")にDWARF 3.0がリリースされ\[3\]、[C++](../Page/C++.md "wikilink")の名前空間のサポート、[Fortran 90](https://ja.wikipedia.org/wiki/FORTRAN#Fortran_90 "wikilink") の `alloctable` データのサポート、[コンパイラ最適化](https://ja.wikipedia.org/wiki/コンパイラ最適化 "wikilink")技法への対応などが追加された。DWARF標準化委員会の委員長 Michael Eager はデバッグ用フォーマットとDWARF-3について *Introduction to the DWARF Debugging Format* という文書を書いている\[4\]。

[2010年](https://ja.wikipedia.org/wiki/2010年 "wikilink")[6月10日](../Page/6月10日.md "wikilink")にDWARF 4、[2017年](../Page/2017年.md "wikilink")[2月15日](../Page/2月15日.md "wikilink")にDWARF 5が発表になった。

## 構造

DWARFは Debugging Information Entry (DIE) という[データ構造](../Page/データ構造.md "wikilink")を使って、変数、データ型、プロシージャなどを表す。DIE にはタグ（例えば、`DW_TAG_variable`、`DW_TAG_pointer_type`、`DW_TAG_subprogram` など）と属性（キーと値の対）があり、DIE同士の入れ子が可能で、[木構造を形成できる](../Page/木構造_\(データ構造\).md "wikilink")。DIEの属性には同じ木構造上の他のDIEへの参照を格納できる。例えば、変数を表すDIEの属性 `DW_AT_type` が、その変数のデータ型を表す DIE を指すといった使い方をする。

シンボリックな[デバッガ](../Page/デバッガ.md "wikilink")は一般に、行番号テーブルとコールフレーム情報テーブルという大きなテーブルを必要とする。記憶領域を節約するため、これらのテーブルは単純な専用[有限状態機械用の](https://ja.wikipedia.org/wiki/有限オートマトン "wikilink")[バイトコード](../Page/バイトコード.md "wikilink")命令列で表される。行番号テーブルはオブジェクトのコードの位置とソースコード上の位置の対応表であり、どの命令が[関数プロローグ](https://ja.wikipedia.org/wiki/関数プロローグ "wikilink")やエピローグに属するかも示す。コールフレーム情報テーブルは、[コールスタック](https://ja.wikipedia.org/wiki/コールスタック "wikilink")上のフレームの位置をデバッガに知らせるものである。

## 脚注

## 外部リンク

  - 標準:
      - [DWARF 公式サイト](http://dwarfstd.org/)
      - [DWARF 5 Standard](http://dwarfstd.org/Dwarf5Std.php) 2017年2月15日
      - [DWARF 4 Standard](http://dwarfstd.org/Dwarf4Std.php) 2010年6月10日
      - [DWARF 3.0 Standard](http://dwarfstd.org/Dwarf3Std.php) 2005年12月20日
      - [DWARF Debugging Information Format Specification Version 2.0](http://dwarfstd.org/doc/dwarf-2.0.0.pdf) 1993年7月27日
  - ツール:
      - [David A's DWARF Page](https://www.prevanders.net/dwarf.html) ライブラリ libdwarf、ツール dwarfdump、その他の関連情報がある。
      - [DWARF2-XML](http://www.sde.cs.titech.ac.jp/~gondow/dwarf2-xml/) DWARFおよびELF情報をXMLに変換するツールとそれを使ったコールグラフ生成ツール
  - 記事:
      - [DWARF2 debugging information format](http://ratonland.org/?entry=39)

[Category:プログラミング](https://ja.wikipedia.org/wiki/Category:プログラミング "wikilink") [Category:ファイルフォーマット](https://ja.wikipedia.org/wiki/Category:ファイルフォーマット "wikilink")

1.
2.
3.
4.
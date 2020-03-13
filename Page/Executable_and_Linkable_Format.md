> この記事は[Executable and Linkable Format](https://ja.wikipedia.org/wiki/Executable_and_Linkable_Format)から翻訳されています。


(ELF) とは、コンパイラが生成する[オブジェクト](../Page/オブジェクトファイル.md "wikilink")、および、ライブラリとリンクされた[実行ファイル](../Page/実行ファイル.md "wikilink")の[ファイルフォーマット](../Page/ファイルフォーマット.md "wikilink")である。[a.outフォーマット](https://ja.wikipedia.org/wiki/a.outフォーマット "wikilink")、[COFFの後継として広く採用されている](https://ja.wikipedia.org/wiki/Common_Object_File_Format "wikilink")。セクション数の制限が緩く、メモリ上で連続していないファイルや、ロードされる場所と実行される場所が違う箇所を含む場合にも対応が可能な柔軟な設計となっている。

[System V](../Page/UNIX_System_V.md "wikilink") が採用し、[GNUツールチェーン](https://ja.wikipedia.org/wiki/GNUツールチェーン "wikilink")がサポートしている。今では[BSD](../Page/BSD.md "wikilink")派生OSや[Linux](../Page/Linux.md "wikilink")をはじめとするフリーなOSにおける実行ファイルフォーマットや、ゲーム機等を含む組み込み機器開発にも数多く使われている。

## ヘッダ

ELFには以下の3種類のヘッダがある。 [thumb](https://ja.wikipedia.org/wiki/ファイル:Elf-layout--en.png "wikilink")

  - ELFヘッダ
    ファイルの先頭に存在し、ELF識別子、アーキテクチャ情報および、他の2つのヘッダへの情報を持つ。
  - プログラムヘッダ
    ファイル上のどの部分(セグメント)がどのような属性で何処に読み込まれるかを保持するヘッダであり、ファイルローダによって扱われる。実行時にELFヘッダに続いてディスクから何らかの形で読み込まれるセグメントの数だけ存在する。直接読み込まれるわけではないオブジェクトファイルには存在しないことがある。
  - セクションヘッダ
    オブジェクトファイルの論理的な構造を記述する部分で、ヘッダと名前がついているが実際にはファイルの最後あたりに置かれていることが多い。ここは[リンカや](../Page/リンケージエディタ.md "wikilink")[デバッガ](../Page/デバッガ.md "wikilink")によって参照されることがある。セクションはセクション名があるが、それは特殊なセクションに置かれ何番目の文字列かという指し方を行う。このことによって、エントリそのものは固定長にしつつセクション名の長さ制限を取り払っている。

## 共有ライブラリ

共有ライブラリにも対応しており、しかるべき属性のセグメント内にある、Procedure Location Tableや、Global Offset Tableを利用して、間接的に参照することになる。

## デバッグ情報ファイル

デバッグ情報のフォーマットは定義されていないが、ELF(妖精)をもじったDebug With Arbitrary Record Format略して[DWARF](../Page/DWARF.md "wikilink")(小人)と呼ばれる形式のフォーマットがよく使われる。

## 関連項目

  - [位置独立コード](https://ja.wikipedia.org/wiki/位置独立コード "wikilink")

## 外部リンク

  -
[Category:オブジェクトファイルフォーマット](https://ja.wikipedia.org/wiki/Category:オブジェクトファイルフォーマット "wikilink") [Category:UNIX](https://ja.wikipedia.org/wiki/Category:UNIX "wikilink") [Category:Wii](https://ja.wikipedia.org/wiki/Category:Wii "wikilink") [Category:ニンテンドーゲームキューブ](https://ja.wikipedia.org/wiki/Category:ニンテンドーゲームキューブ "wikilink")
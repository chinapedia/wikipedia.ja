> この記事は[Standard Triangulated Language](https://ja.wikipedia.org/wiki/Standard_Triangulated_Language)から翻訳されています。


**STL**は三次元形状を表現するデータを保存する[ファイルフォーマット](../Page/ファイルフォーマット.md "wikilink")のひとつである。名称の由来は[光造形法](https://ja.wikipedia.org/wiki/光造形法 "wikilink")を意味する  である。後付けだが、 や  の略称とされることもある。

[米国の](https://ja.wikipedia.org/wiki/アメリカ合衆国 "wikilink")によって開発された三次元[CAD](../Page/CAD.md "wikilink")ソフト用のファイルフォーマット。多くのソフトにサポートされており、特に[ラピッドプロトタイピング](https://ja.wikipedia.org/wiki/ラピッドプロトタイピング "wikilink")システムのファイルフォーマットとして利用されている。

## 特徴

三次元形状を小さな三角形の集合体として表現するシステムで、色やトポロジーデータなどは表現することはできない。またカーブ形状などの表現も行うことが出来ない。しかしデータ構造が簡単であることから[ラピッドプロトタイピング](https://ja.wikipedia.org/wiki/ラピッドプロトタイピング "wikilink")の分野では標準フォーマットとなっており、各種ラピッドプロトタイピングシステムで使用可能である。

オブジェクトの形状は、三つの頂点の座標と法線ベクトルにより定義される三角形[ポリゴン](../Page/ポリゴン.md "wikilink")であるファセット(facet)の集合により表現する。面以外の点や線といった要素の定義や、色、面間の連続性、その他の特性の定義については、標準的にはできないが、一部のソフトウェアにおいては、バイナリSTLにおいてファセット番号を定義する2バイト分を転用することで、色の指定を行っている場合がある。

## データ形式

[プレーンテキスト](../Page/プレーンテキスト.md "wikilink")で記述されたASCII STL形式と、バイナリSTL形式がある。どちらのファイル形式でも、三角形の法線ベクトル（長さ１の単位ベクトル）と、面の表裏を示すために右ねじの法則に従って並んだ三角形の座標データを三角形の数だけ含む。このような冗長性のため面の表裏は、法線ベクトルと座標（右ねじの法則）の二通りで知ることができる。

### ASCII形式

ASCII形式は可読性が高いがバイナリ形式と比較してファイルサイズが大きくなるという弱点がある。

ASCII形式の文法は非常に簡単である。すべての行が以下の形式を満たす。:

` キーワード 　[半角1文字スペース]  データ`

最初の行は以下の文で始まる。:

` solid `*`name`*

nameはオプションだが、省いた場合にも必ず半角スペースが必要である。 このあとに三角形データが続く。:

` facet normal `*`n`<sub>`i`</sub>`   ``n`<sub>`j`</sub>`   ``n`<sub>`k`</sub>*
`   outer loop`
`     vertex `*`v1`<sub>`x`</sub>`   ``v1`<sub>`y`</sub>`   ``v1`<sub>`z`</sub>*
`     vertex `*`v2`<sub>`x`</sub>`   ``v2`<sub>`y`</sub>`   ``v2`<sub>`z`</sub>*
`     vertex `*`v3`<sub>`x`</sub>`   ``v3`<sub>`y`</sub>`   ``v3`<sub>`z`</sub>*
`   endloop`
` endfacet`

[法線ベクトル](https://ja.wikipedia.org/wiki/法線ベクトル "wikilink")は英語でと表記される。ここでは`facet normal`で三角形の法線ベクトルを意味する。法線ベクトルは大きさ１の単位ベクトルである。三角形の座標(`vertex`)は反時計回りに回る順番となる。数学的には三角形の座標から法線ベクトルは決定されるのだが(逆に法線ベクトルからは座標はわからない。後述するように法線ベクトルデータが直接扱われることは少ない)、三角形の法線ベクトルも同時に表示する規格となっている。 n<sub>i</sub> - n<sub>k</sub> とv1<sub>x</sub> - v3<sub>z</sub> は[浮動小数点](https://ja.wikipedia.org/wiki/浮動小数点 "wikilink")であり、e表記法(例：1.000000e+01 ）で表記される。 `facet normal` と `outer loop` の間のスペースは必要である。法線ベクトルの成分はマイナスを取りえるが、座標の成分はプラスのみである。

ファイルの最後は以下の文で終了する:

` endsolid `*`name`*

### バイナリ形式

ASCII形式のSTLファイルは非常に大きくなるため、STLにはバイナリー形式も用意されている。バイナリーSTLファイルは80バイトの任意の文字列で開始される（通常内容は無視される。ただし、*`solid`* から記載を始めた場合にASCII形式であると誤認識するソフトウェアが存在するため、注意を要する）。次に4バイトの整数でファイルに含まれる三角形の枚数が示される。そのあとに、それぞれの三角形のデータが枚数分続くという構造になっている。終了コードは特にない。最後の三角形のデータを示した後、単純に終了となる。

それぞれの三角形は12個の32ビット[浮動小数点](https://ja.wikipedia.org/wiki/浮動小数点 "wikilink")で示される。ASCII形式のSTLファイルと同様に、最初に三角形の法線ベクトル(3個)、次に三角形の各座標(3x3=9個)が X/Y/Zの順番で示される。その後2バイトの未使用データが続く。ほとんどのソフトはこの部分を評価しないので通常はゼロである。

浮動小数点の表記方法はIEEE方式([IEEE 754](https://ja.wikipedia.org/wiki/IEEE_754 "wikilink"))である。[エンディアン](https://ja.wikipedia.org/wiki/エンディアン "wikilink")は、仕様文書に明示されていないがリトルエンディアンである。

`UINT8[80]         -   ヘッダー（任意の文字列）`
`UINT32            -   ファイルに含まれる三角形の数`

` foreach triangle`
`  REAL32[3]       -    法線ベクトル`
`  REAL32[3]       -    座標 1`
`  REAL32[3]       -    座標 2`
`  REAL32[3]       -    座標 3`
`  UINT16          -    未使用データ`
`end`

## 法線ベクトルの取り扱い

STLフォーマットの規格では、ASCII形式においてもバイナリ形式においても法線ベクトルは物体の外側を示す単位ベクトルでなくてはならない。特にRPシステムでは法線ベクトルは内外を表示する情報として扱われることがあるため、重要な情報となる。変換ミスで逆になった場合は反転三角としてRP作成時のエラーの原因となる。Magicsなどの各種STL編集ソフトでそのような間違いを修正することができる。 一部のソフト(例:[SolidWorks](../Page/SolidWorks.md "wikilink"))では[シェーディング](https://ja.wikipedia.org/wiki/シェーディング "wikilink")効果に法線ベクトルを利用する。そのためこのようなソフトでは三角形の面に対する真の法線ベクトルとはならない。

## 外部リンク

  - STLファイルフォーマット(個人による日本語メモ) [1](http://www.hiramine.com/programming/3dmodelfileformat/stlfileformat.html)
  - The STL Format - Standard Data Format for Fabbers: [The STL Format](http://www.ennex.com/~fabbers/StL.asp)
  - [Free STL Viewer for Google Chrome](https://chrome.google.com/webstore/detail/3dview/hhngciknjebkeffhafnaodkfidcdlcao)

[Category:CADファイルフォーマット](https://ja.wikipedia.org/wiki/Category:CADファイルフォーマット "wikilink")
> この記事は[XCF](https://ja.wikipedia.org/wiki/XCF)から翻訳されています。


**XCF**（eXperimental Computing Facility）ファイル形式は、[GIMP](../Page/GIMP.md "wikilink")画像編集プログラムのネイティブな画像形式である。各レイヤ、現在の選択、チャネル、透明度、パスおよびガイドの保存をサポートする。しかしながら、[PSDファイルと異なり](../Page/Adobe_Photoshop.md "wikilink")、やり直しの履歴はXCFファイルに保存されない。

保存される画像データは単純な[RLEアルゴリズムによってのみ圧縮されるが](https://ja.wikipedia.org/wiki/連長圧縮 "wikilink")、GIMPは[gzip](https://ja.wikipedia.org/wiki/gzip "wikilink")と[bzip2](https://ja.wikipedia.org/wiki/bzip2 "wikilink")のどちらを使った圧縮ファイルもサポートしている。圧縮されたファイルは通常の画像ファイルと同じように開ける。

XCFファイル形式はほとんどの場合[後方互換である](https://ja.wikipedia.org/wiki/下位互換 "wikilink")。たとえば、GIMP 2.0は文章を文章レイヤに保存できるが、GIMP 1.2はできない。GIMP 2.0で保存された文章レイヤはGIMP 1.2では通常の画像レイヤとして開かれる。

GIMPの開発者はXCFをデータ交換形式として使うことを勧めていない。なぜならばこの形式はGIMPの内部データ構造を反映しており、将来のバージョンで小さな形式変更があるかもしれないからである。それゆえGIMP自身の (自由に利用可能な) ソースコードが画像形式の参照文書となる。加えて、GIMP開発者と[Krita](https://ja.wikipedia.org/wiki/Krita "wikilink")開発者の間で新しい画像形式を設計するために共同作業の努力が進行中である。この新しい形式は[OpenDocument Formatをモデルとし](https://ja.wikipedia.org/wiki/OpenDocument "wikilink")、両方のアプリケーションの将来のバージョンで採用される予定のラスタファイル形式である。しかしながら、Henning Makholm (下記のXCFToolsを参照) はこの形式を完全に文書化した、現時点では草案形式の[仕様書](http://henning.makholm.net/xcftools/xcfspec.txt)を書き上げた。

## ソフトウェアの対応状況

XCFはGIMPに加えて他のプログラムでもファイル形式として使われている:

  - [SeashoreはMac](https://ja.wikipedia.org/wiki/Seashore_\(software\) "wikilink") OS Xネイティブの軽量な画像編集プログラムであり、GIMPを基に作られた。
  - [CinePaint](https://ja.wikipedia.org/wiki/CinePaint "wikilink")はGIMPからのフォークであり、16ビットと32ビットの浮動小数点チャネルおよび16ビット整数チャネルのサポートを追加している。CinePaintのファイル形式をXCFから変更する[計画](http://www.linuxdevcenter.com/pub/a/linux/2004/04/29/cinepaint.html?page=2)が存在する。CinePaintで使われているXCFファイル形式はGIMPのネイティブ形式から分岐しているので、GIMPで作成したXCFファイルをCinepaintで開くこと (またはその逆) はできない。

いくつかの[画像ビューア](https://ja.wikipedia.org/wiki/画像ビューア "wikilink")と変換ソフトウェアはこの形式を読めるが、対応の度合いはまちまちである:

  - [ImageMagick](../Page/ImageMagick.md "wikilink")にはXCF読み取りモジュールがあり、単一レイヤのインデックスカラーでない画像を読める。
  - [Krita](https://ja.wikipedia.org/wiki/Krita "wikilink")はGraphicsMagickライブラリを使ってXCFファイルをインポートする。
  - [ShowImg](https://ja.wikipedia.org/wiki/ShowImg "wikilink")は複数レイヤのインデックスカラーでない画像を表示できる。
  - [Gwenview](https://ja.wikipedia.org/wiki/Gwenview "wikilink")は複数レイヤのインデックスカラーでない画像を表示できる。
  - [GImageView](https://ja.wikipedia.org/wiki/GImageView "wikilink")は複数レイヤのインデックスカラーでない画像を表示できる\[1\]。
  - [IrfanView](../Page/IrfanView.md "wikilink")は4.32リリースでXCFのサポートを追加した。
  - [XnView](https://ja.wikipedia.org/wiki/XnView "wikilink")は単一レイヤのインデックスカラーでない画像を表示できる。
  - [Inkscape](https://ja.wikipedia.org/wiki/Inkscape "wikilink")は0.44リリースでXCFエクスポートのサポートを追加した\[2\]。
  - Henning Makholmによる**XCFTools**はXCF画像の変形や合成を行うユーティリティのセットである\[3\]。個々のレイヤ、もしくは合成した画像全体を、PNGや[PNMとして抽出することもできる](https://ja.wikipedia.org/wiki/PNM_\(画像フォーマット\) "wikilink")。

## 脚注

[Category:画像ファイルフォーマット](https://ja.wikipedia.org/wiki/Category:画像ファイルフォーマット "wikilink")

1.
2.  [Release Notes of Inkscape 0.44](http://sourceforge.net/project/shownotes.php?release_id=426990&group_id=93438)
3.
> この記事は[ImageMagick](https://ja.wikipedia.org/wiki/ImageMagick)から翻訳されています。


**ImageMagick**（イメージマジック）は画像を操作したり表示したりするためのソフトウェアスイートである。[GIF](../Page/Graphics_Interchange_Format.md "wikilink")、[JPEG](../Page/JPEG.md "wikilink")、[JPEG 2000](../Page/JPEG_2000.md "wikilink")、[PNG](../Page/Portable_Network_Graphics.md "wikilink")、[PDF](../Page/Portable_Document_Format.md "wikilink")、[Photo CD](https://ja.wikipedia.org/wiki/フォトCD "wikilink")、[TIFF](../Page/Tagged_Image_File_Format.md "wikilink")、[DPXなど](https://ja.wikipedia.org/wiki/Digital_Picture_Exchange "wikilink")100種類以上の[画像ファイルフォーマット](https://ja.wikipedia.org/wiki/画像ファイルフォーマット "wikilink")に対応している\[1\]。[GPL互換でより制限が緩い独自ライセンスが適用されている](../Page/GNU_General_Public_License.md "wikilink")\[2\]。

## 利用方法

ImageMagick は[コマンドラインから利用する方法と](https://ja.wikipedia.org/wiki/コマンドラインインタプリタ "wikilink")、他のプログラムから呼び出して使う方法がある。

### コマンドラインからの利用方法

ImageMagickは多数のコマンドラインツールを含んでおり、[バッチ処理](https://ja.wikipedia.org/wiki/バッチ処理 "wikilink")などで[GUI](https://ja.wikipedia.org/wiki/GUI "wikilink")を使わずに画像処理したい場合に有用である\[3\]。

  - 画像を表示 - `display input_file`
  - スクリーンショット - `import [ options ... ] output file`
  - 画像変換 - `convert [ options ... ] input_file output_file`
      - （例） `convert -delay 100 -loop 0 magick[1-2].gif magick-anime.gif`

### プログラムからの利用方法

ImageMagick は様々な言語から利用できる。以下に言語ごとの実装を示す\[4\]。

<table>
<caption>言語ごとの実装</caption>
<thead>
<tr class="header">
<th><p>言語</p></th>
<th><p>実装名</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><a href="../Page/Ada.md" title="wikilink">Ada</a></p></td>
<td><p>G2F</p></td>
</tr>
<tr class="even">
<td><p><a href="../Page/C言語.md" title="wikilink">C言語</a></p></td>
<td><p>MagickCore<br />
MagickWand</p></td>
</tr>
<tr class="odd">
<td><p>Ch</p></td>
<td><p>ChMagick</p></td>
</tr>
<tr class="even">
<td><p><a href="../Page/Component_Object_Model.md" title="wikilink">COM+</a></p></td>
<td><p>ImageMagickObject</p></td>
</tr>
<tr class="odd">
<td><p><a href="../Page/C++.md" title="wikilink">C++</a></p></td>
<td><p>Magick++</p></td>
</tr>
<tr class="even">
<td><p><a href="https://ja.wikipedia.org/wiki/Go_(プログラミング言語)" title="wikilink">GO</a></p></td>
<td><p>GoImagick</p></td>
</tr>
<tr class="odd">
<td><p><a href="https://ja.wikipedia.org/wiki/Java" title="wikilink">Java</a></p></td>
<td><p>JMagick</p></td>
</tr>
<tr class="even">
<td><p><a href="../Page/LabVIEW.md" title="wikilink">LabVIEW</a></p></td>
<td><p>LVOOP ImageMagick</p></td>
</tr>
<tr class="odd">
<td><p><a href="https://ja.wikipedia.org/wiki/Lisp" title="wikilink">Lisp</a></p></td>
<td><p>L-Magick</p></td>
</tr>
<tr class="even">
<td><p><a href="https://ja.wikipedia.org/wiki/Lua" title="wikilink">Lua</a></p></td>
<td><p>magick</p></td>
</tr>
<tr class="odd">
<td><p>Neko/<a href="https://ja.wikipedia.org/wiki/haXe" title="wikilink">haXe</a></p></td>
<td><p>NMagick</p></td>
</tr>
<tr class="even">
<td><p><a href="https://ja.wikipedia.org/wiki/.NET_Framework" title="wikilink">.NET</a></p></td>
<td><p>MagickNet</p></td>
</tr>
<tr class="odd">
<td><p><a href="../Page/Pascal.md" title="wikilink">Pascal</a></p></td>
<td><p>PascalMagick</p></td>
</tr>
<tr class="even">
<td><p><a href="../Page/Perl.md" title="wikilink">Perl</a></p></td>
<td><p>PerlMagick</p></td>
</tr>
<tr class="odd">
<td><p><a href="../Page/PHP_(プログラミング言語).md" title="wikilink">PHP</a></p></td>
<td><p>MagickWand for PHP<br />
IMagick</p></td>
</tr>
<tr class="even">
<td><p><a href="../Page/Python.md" title="wikilink">Python</a></p></td>
<td><p>PythonMagick</p></td>
</tr>
<tr class="odd">
<td><p><a href="https://ja.wikipedia.org/wiki/REALbasic" title="wikilink">REALbasic</a></p></td>
<td><p>MBS Realbasic ImageMagick</p></td>
</tr>
<tr class="even">
<td><p><a href="../Page/Ruby.md" title="wikilink">Ruby</a></p></td>
<td><p>RMagick</p></td>
</tr>
<tr class="odd">
<td><p><a href="https://ja.wikipedia.org/wiki/Rust" title="wikilink">Rust</a></p></td>
<td><p>RustWand</p></td>
</tr>
<tr class="even">
<td><p><a href="https://ja.wikipedia.org/wiki/Tcl/Tk" title="wikilink">Tcl/Tk</a></p></td>
<td><p>TclMagick</p></td>
</tr>
<tr class="odd">
<td><p><a href="https://ja.wikipedia.org/wiki/XML-RPC" title="wikilink">XML-RPC</a></p></td>
<td><p>RemoteMagick</p></td>
</tr>
</tbody>
</table>

## 出典

<references />

## 外部リンク

  -
[Category:グラフィックデザイン](https://ja.wikipedia.org/wiki/Category:グラフィックデザイン "wikilink") [Category:画像処理ソフト](https://ja.wikipedia.org/wiki/Category:画像処理ソフト "wikilink") [Category:オープンソースソフトウェア](https://ja.wikipedia.org/wiki/Category:オープンソースソフトウェア "wikilink") [Category:クロスプラットフォームのソフトウェア](https://ja.wikipedia.org/wiki/Category:クロスプラットフォームのソフトウェア "wikilink")

1.  [ImageMagick: Formats](http://www.imagemagick.org/script/formats.php)
2.  [ImageMagick: License](http://www.imagemagick.org/script/license.php)
3.  [ImageMagick: Command-line Tools](http://imagemagick.org/script/command-line-tools.php)
4.  [ImageMagick: Application Program Interfaces](http://www.imagemagick.org/script/api.php)
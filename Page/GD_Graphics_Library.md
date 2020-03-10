> この記事は[GD Graphics Library](https://ja.wikipedia.org/wiki/GD_Graphics_Library)から翻訳されています。


**GD グラフィック ライブラリ** (GD Graphics Library) は[トーマス・ボーテル](https://ja.wikipedia.org/wiki/トーマス・ボーテル "wikilink") (Thomas Boutell) 他によって作られた[イメージ](https://ja.wikipedia.org/wiki/イメージ "wikilink")を動的に操作する[ライブラリ](../Page/ライブラリ.md "wikilink")である。本来の[プログラミング言語](../Page/プログラミング言語.md "wikilink")は[ANSI](../Page/米国国家規格協会.md "wikilink") [Cであるが](../Page/C言語.md "wikilink")、他の多くのプログラミング言語との[インタフェースが作成されている](../Page/インタフェース_\(情報技術\).md "wikilink")。[GIF](../Page/Graphics_Interchange_Format.md "wikilink")、[JPEG](../Page/JPEG.md "wikilink")、[PNG](../Page/Portable_Network_Graphics.md "wikilink")、[WBMP](https://ja.wikipedia.org/wiki/Wireless_Application_Protocol_Bitmap_Format "wikilink") を生成できる。

[1999年](../Page/1999年.md "wikilink")に米[ユニシス](https://ja.wikipedia.org/wiki/ユニシス "wikilink")がGIFに使用されている [LZW圧縮法の非商業的な](../Page/Lempel–Ziv–Welch.md "wikilink")[ソフトウェア](../Page/ソフトウェア.md "wikilink")・プロジェクトに許可していた無償のライセンスを取り消したことにより、GIF を操作する機能は削除された。[2004年](../Page/2004年.md "wikilink")[7月7日](https://ja.wikipedia.org/wiki/7月7日 "wikilink")、ユニシスの特許が世界中で失効した時に、GIFを操作する機能が再び実装された。

GDは元来、「GIFを描く (GIF Draw)」を表していた。しかしユニシスが無償ライセンスを取り消した後は非公式に、「グラフィックを描く (Graphics Draw)」を表すこととなった。

GDは、直線、弧、テキスト（プログラムで指定したフォントを使用する）から成るイメージ、その他のイメージと複数の色を作成できる。

バージョン2.0以降では、トゥルーカラー (Truecolor) イメージ、アルファ・チャネル、 [リサンプリング](https://ja.wikipedia.org/wiki/リサンプリング "wikilink")（トゥルーカラーイメージの滑らかなリサイズが可能となる）と他の多くの大きな機能に対するサポートが追加された。

GDは[C](../Page/C言語.md "wikilink")、[PHP](../Page/PHP_\(プログラミング言語\).md "wikilink")、[Perl](../Page/Perl.md "wikilink")、[OCaml](../Page/OCaml.md "wikilink")、[Tcl](https://ja.wikipedia.org/wiki/Tcl "wikilink")、[Lua](../Page/Lua.md "wikilink")、[Pascal](../Page/Pascal.md "wikilink")、[GNU Octaveと](../Page/GNU_Octave.md "wikilink")[REXX](https://ja.wikipedia.org/wiki/REXX "wikilink")を含む多くのプログラミング言語をサポートしている。また、どんな言語からでもコマンドラインを通してGDへアクセスすることができるプログラム**fly**がある。

GDはPHPで広く使われ、PHP 4.3 以降のバージョンでは[デフォルトの拡張機能となっている](../Page/デフォルト_\(コンピュータ\).md "wikilink")。それ以前は[オプション](https://ja.wikipedia.org/wiki/オプション "wikilink")であった。

## 開発者の交代

[2007年](../Page/2007年.md "wikilink")[1月4日](../Page/1月4日.md "wikilink")に、有名なPHP開発者であるPirre Joyeにプロジェクトが引き継がれた。 プロジェクトは幾月かの停滞した後、新開発者によって多くの修正を含んだ新バージョンが発表されると思われる。

## 例

以下は、3D円グラフ（PHP GDドキュメントのimagefilledarc（））出力例。

``` php
<?php
    // Create an image
    $image = imagecreatetruecolor(100, 100);

    // Allocate some colors
    $white    = imagecolorallocate($image, 0xFF, 0xFF, 0xFF);
    $gray     = imagecolorallocate($image, 0xC0, 0xC0, 0xC0);
    $darkgray = imagecolorallocate($image, 0x90, 0x90, 0x90);
    $navy     = imagecolorallocate($image, 0x00, 0x00, 0x80);
    $darknavy = imagecolorallocate($image, 0x00, 0x00, 0x50);
    $red      = imagecolorallocate($image, 0xFF, 0x00, 0x00);
    $darkred  = imagecolorallocate($image, 0x90, 0x00, 0x00);

    // Make the 3D effect
    for ($i = 60; $i > 50; $i--) {
        imagefilledarc($image, 50, $i, 100, 50, 0,   45, $darknavy, IMG_ARC_PIE);
        imagefilledarc($image, 50, $i, 100, 50, 45,  75, $darkgray, IMG_ARC_PIE);
        imagefilledarc($image, 50, $i, 100, 50, 75, 360, $darkred,  IMG_ARC_PIE);
    }

    imagefilledarc($image, 50, 50, 100, 50,  0,  45, $navy, IMG_ARC_PIE);
    imagefilledarc($image, 50, 50, 100, 50, 45,  75, $gray, IMG_ARC_PIE);
    imagefilledarc($image, 50, 50, 100, 50, 75, 360, $red,  IMG_ARC_PIE);

    // Flush the image
    header('Content-type: image/png');
    imagepng($image);
    imagedestroy($image);
?>
```

## 関連項目

  - [ImageMagick](../Page/ImageMagick.md "wikilink")
  - [Netpbm](https://ja.wikipedia.org/wiki/Netpbm "wikilink")
  - [cairo](https://ja.wikipedia.org/wiki/cairo "wikilink")

## 脚注

<references/>

## 外部リンク

  - [GD Graphics Library](https://www.libgd.org/)（現在の開発サイト）
  - [GD Graphics Library](https://boutell.com/gd/)（古い開発サイト）
  - [Image Functions (PHP)](https://www.php.net/manual/ja/book.image.php), support in PHP

イメージ機能 (PHP)、PHPのサポート

[Category:グラフィックライブラリ](https://ja.wikipedia.org/wiki/Category:グラフィックライブラリ "wikilink") [Category:オープンソースソフトウェア](https://ja.wikipedia.org/wiki/Category:オープンソースソフトウェア "wikilink")
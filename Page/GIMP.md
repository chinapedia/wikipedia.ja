> この記事は[GIMP](https://ja.wikipedia.org/wiki/GIMP)から翻訳されています。


**GIMP**（ギンプ、ジンプ、**G**NU **I**mage **M**anipulation **P**rogram）は、[GNU GPL](../Page/GNU_General_Public_License.md "wikilink") の下で配布されている[ビットマップ画像](../Page/ビットマップ画像.md "wikilink")編集・加工ソフトウェア（[ペイントソフト](../Page/ペイントソフト.md "wikilink")）。

## 概要

[Gimp_brushes.png](https://ja.wikipedia.org/wiki/File:Gimp_brushes.png "fig:Gimp_brushes.png")におけるブラシダイアログ\]\] [Layers_Channels_Paths.gif](https://ja.wikipedia.org/wiki/File:Layers_Channels_Paths.gif "fig:Layers_Channels_Paths.gif") [gimp_2.2.8_Mac.png](https://ja.wikipedia.org/wiki/File:gimp_2.2.8_Mac.png "fig:gimp_2.2.8_Mac.png") 環境下で実行中\]\] GIMPは[1995年](https://ja.wikipedia.org/wiki/1995年 "wikilink")に Spencer Kimball と Peter Mattis が開発を始めた。

フリーソフトでありながら有料のグラフィック編集ソフトウェアと比べても遜色のないレベルの機能を備えている。レイヤー、トーンカーブ、ヒストグラム、画像の形状からの切り抜き、ブラシエディタ、パスの編集、多種多様なプラグインなどに加え、モザイク編集や、アニメーション合成（[GIFアニメーション](../Page/GIFアニメーション.md "wikilink")）を行うなどといったフィルタ機能も数多く備えており、これ一つで、コンピュータ上のほとんどの[画像編集](../Page/画像編集.md "wikilink")は行える。しかし多機能性を外部プラグインやスクリプトなどに頼っているため起動時の読み込み量が多く、時間がかかる。

もともとウェブ用のグラフィック編集を想定して開発されたソフトウェアであるため、[CMYK](../Page/CMYK.md "wikilink")カラーをネイティブサポートしていない\[1\]など、本格的な印刷業務には向いていないという面もある。

基本的には、パレット上のツールボックスから機能を選択して画像の編集を行うというオーソドックスなソフトウェアだが、[SDIで](https://ja.wikipedia.org/wiki/Single_Document_Interface "wikilink")、かつ、いくつもボックスを持つなど、長らくインターフェイスに癖があった。しかし、2.6からはユーティリティウィンドウが実装され、今までのツールボックス等のウィンドウを、一つの親ウィンドウで管理できるようになり、2.8からはすべてを一つのウインドウに統合する「シングルウインドウモード」が実装された。

対話的な使い方の他にも[Scheme](../Page/Scheme.md "wikilink")を使った「Script-Fu」を用いてスクリプトを作り自動化することができる。なお、Script-Fuの名は[カンフー](../Page/功夫.md "wikilink") (Kung-fu) からきている。現在では[Perl](../Page/Perl.md "wikilink")、[Python](../Page/Python.md "wikilink")、[Tcl](https://ja.wikipedia.org/wiki/Tcl/Tk "wikilink")、[Rubyなどの言語でスクリプトを書く環境もある](https://ja.wikipedia.org/wiki/Ruby_\(代表的なトピック\) "wikilink")。このスクリプト処理は完全に非対話的な自動処理も書ける。[ImageMagick](../Page/ImageMagick.md "wikilink")の方が簡単にすばやく自動化処理を行えるが、GIMPの方がはるかに強力な画像編集機能を使える。

カラーマネジメント対応については、バージョン2.4より作業中の画像に対して[カラープロファイルの割り当て](https://ja.wikipedia.org/wiki/カラーマネージメントシステム#ICCプロファイル "wikilink")（埋め込み）が可能になったほか、プロファイルが埋め込まれた画像のカラーを適切に画面上で確認するための仕組みが整備された\[2\]。同様に、CMYK出力時の色味をシミュレートするソフトプルーフの機能も提供されている。カラープロファイルが埋め込まれた画像ファイルの読み込み・保存は、各形式に対応するプラグインの実装に依存しており、従来よりJPEG、TIFF、PNG形式でサポートされていた。バージョン2.4以降はカラーマネジメント関連機能の整備に伴い、ネイティブ形式である XCF形式でもサポートされるようになった。

GIMPは[X Window System向けに制作され](../Page/X_Window_System.md "wikilink")、多くのデスクトップ向け[Unix系](../Page/Unix系.md "wikilink")OS上ではデフォルトで同梱されている。現在は[Windows版や](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")[macOS](https://ja.wikipedia.org/wiki/macOS "wikilink")版も利用可能である。macOS版はバージョン2.8.2からmacOSにネイティブ対応し、X11環境が不要になった。開発元の The GIMP Team は公式のバイナリを提供せず、各プラットフォーム向けのバイナリ配布は有志の手によって行われている\[3\]。

[GTK+](https://ja.wikipedia.org/wiki/GTK+ "wikilink")は本来はGIMPのために制作されたライブラリでありGIMPの一部だったが、ここから派生して現在では広く使われるGUI向けのライブラリになっている。

[gettext](https://ja.wikipedia.org/wiki/gettext "wikilink")の仕組みを使って多言語対応している。

## 歴史

  - [1996年](../Page/1996年.md "wikilink")[1月](https://ja.wikipedia.org/wiki/1月 "wikilink") - 最初の公式リリースとなる GIMP 0.54 がリリースされた\[4\]。
  - [1998年](https://ja.wikipedia.org/wiki/1998年 "wikilink")[6月2日](../Page/6月2日.md "wikilink") - 最初の正式版リリースとなる GIMP 1.0 がリリースされた\[5\]。
  - [2000年](../Page/2000年.md "wikilink")12月25日 - GIMP 1.2.0リリース\[6\]。
  - [2004年](../Page/2004年.md "wikilink")
      - [3月24日](../Page/3月24日.md "wikilink") - GIMP 2 最初のリリースとなる GIMP 2.0 がリリースされた\[7\]。
      - 12月19日 - GIMP 2.2.0 リリース\[8\]。
  - [2007年](../Page/2007年.md "wikilink")10月24日 - GIMP 2.4.0 がリリースされた\[9\]。
  - [2008年](https://ja.wikipedia.org/wiki/2008年 "wikilink")10月1日 - GIMP 2.6.0 がリリースされた\[10\]。
  - [2012年](../Page/2012年.md "wikilink")5月3日 - GIMP 2.8.0 がリリースされた\[11\]。このバージョンからシングルウインドウモードが導入された。
  - [2018年](../Page/2018年.md "wikilink")4月27日 - GIMP 2.10.0 がリリースされた\[12\]。ユーザーインターフェースが更新され、イニシャルHiDPIが導入された。

## ファイル形式

GIMP は以下の[ファイル形式を開いたり保存したりすることができる](../Page/ファイルフォーマット.md "wikilink")\[13\]。

  - GIMP [XCF](../Page/XCF.md "wikilink")、ネイティブ形式（.xcf、もしくは.xcf[.gzや](https://ja.wikipedia.org/wiki/gzip "wikilink").xcf[.bz2として圧縮されたもの](../Page/Bzip2.md "wikilink")）
  - [Autodesk](../Page/オートデスク.md "wikilink") flic動画 (.fli)
  - [DICOM](../Page/DICOM.md "wikilink")（.dcmもしくは.dicom）
  - [PostScript](../Page/PostScript.md "wikilink")文書（.ps、.ps.gzおよび.eps）
  - [FITS](https://ja.wikipedia.org/wiki/FITS "wikilink")天文画像（.fits、もしくは.fit）
  - [Scalable Vector Graphics](../Page/Scalable_Vector_Graphics.md "wikilink")、パスのエクスポート用 (.svg)
  - Microsoft Windows の[アイコン](https://ja.wikipedia.org/wiki/ICO_\(ファイルフォーマット\) "wikilink") (.ico)
  - Microsoft の無圧縮[AVIビデオ](../Page/Audio_Video_Interleave.md "wikilink") (.avi)
  - [Windows bitmap](../Page/Windows_bitmap.md "wikilink") (.bmp)
  - [Corel Paint Shop Pro画像](../Page/Corel_Paint_Shop_Pro.md "wikilink")（.pspまたは.tub）
  - [Adobe Photoshop文書](../Page/Adobe_Photoshop.md "wikilink") (.psd、.pdd)
  - [PNM画像](https://ja.wikipedia.org/wiki/PNM_\(画像フォーマット\) "wikilink")（.pnm、.ppm、.pgm、および.pbm）
  - Compuserve [Graphics Interchange Format画像と動画](../Page/Graphics_Interchange_Format.md "wikilink") (.gif)
  - [Joint Photographic Experts Group画像](../Page/JPEG.md "wikilink")（.jpeg、.jpg、もしくは.jpe）
  - [Portable Network Graphics](../Page/Portable_Network_Graphics.md "wikilink") (.png)
  - [KISSのセル](../Page/KISekae_Set_system.md "wikilink") (.cel)
  - [Tagged Image File Format](../Page/Tagged_Image_File_Format.md "wikilink")（.tiffか.tif）
  - [TARGA](../Page/TGA.md "wikilink") (.tga)
  - [X](../Page/X_Window_System.md "wikilink") bitmap画像（.xbm、.icon、もしくは.bitmap）
  - X pixmap画像 (.xpm)
  - X Windowダンプ (.xwd)
  - Zsoft [PCX](../Page/PCX.md "wikilink") (.pcx)

GIMP は以下の形式をインポートできる（開けるが保存できない）:

  - Adobe [PDFファイル](../Page/Portable_Document_Format.md "wikilink") (.pdf)
  - [RAW画像](../Page/RAW画像.md "wikilink")（多数の拡張）

GIMP は以下の形式をエクスポートできる（保存できるが開けない）:

  - [HTML](../Page/HyperText_Markup_Language.md "wikilink")、色つきのセルを使った表として (.html)
  - [C言語](../Page/C言語.md "wikilink")のソースファイル、配列として（.cまたは.h）
  - [Multiple-image Network Graphics](../Page/Multiple-image_Network_Graphics.md "wikilink")、レイヤ付き画像ファイル (.mng)
  - [アスキーアート](../Page/アスキーアート.md "wikilink")もしくはHTML、画像を構成する文字や記号で

## マスコット

[thumb](https://ja.wikipedia.org/wiki/ファイル:Exquisite-gimp2_0.png "wikilink") 「ウィルバー (Wilber)」がGIMPの[マスコット](../Page/マスコット.md "wikilink")である。

## 派生品

GIMP をベースにしたいくつかの派生バージョンやカスタマイズパッケージが存在する。

  - [GIMPshop](https://www.gimpshop.com/)
    [Adobe Photoshop](../Page/Adobe_Photoshop.md "wikilink") とメニューの並び順を同じにしている。
  - [Seashore](https://sourceforge.net/projects/seashore/)
    [macOS](https://ja.wikipedia.org/wiki/macOS "wikilink") 向けにシンプル化したもの。

## 競合製品

  - [Adobe Photoshop](../Page/Adobe_Photoshop.md "wikilink")、[Corel Paint Shop Pro](../Page/Corel_Paint_Shop_Pro.md "wikilink")、[Corel PHOTO-PAINT](../Page/Corel_PHOTO-PAINT.md "wikilink") との比較

<!-- end list -->

  - Photoshop、Photo-Paint には Pantone カラーマッチングシステムが含まれる
  - Photoshop はシェアが高いためプラグインやアドオンが製品も含め多く存在する
      - GIMP は無償で手に入るため、簡単に GIMP の制御ができる Script-Fu が数多く公開されている
  - GIMP は SGI形式の画像を編集できる
  - GIMP は spot color に対応していない
  - GIMP は多くのプラットフォームに対応している
  - GIMP は無償で入手が可能である

## 脚注

## 関連項目

  - [G'MIC](https://ja.wikipedia.org/wiki/G'MIC "wikilink") - GIMPプラグインの一つ
  - [GNOME](../Page/GNOME.md "wikilink")
  - [Inkscape](../Page/Inkscape.md "wikilink")、[Krita](../Page/Krita.md "wikilink") -オープンソースで開発されている[ドローソフト](../Page/ドローソフト.md "wikilink")
  - [Adobe Photoshop](../Page/Adobe_Photoshop.md "wikilink")
  - [Corel Paint Shop Pro](../Page/Corel_Paint_Shop_Pro.md "wikilink")
  - [Corel PHOTO-PAINT](../Page/Corel_PHOTO-PAINT.md "wikilink")
  - [Tango Desktop Project](../Page/Tango_Desktop_Project.md "wikilink") - GIMP のメニュー画面のアイコンは、このプロジェクトによるガイドラインに沿って開発されている。

## 外部リンク

### 公式

  - [GIMP](https://www.gimp.org/)
  - [GIMP Help](https://docs.gimp.org/)
  - [GIMP Plug-In Registry](https://www.gimp.org/registry/)
  - [GIMP Developer Resources](https://developer.gimp.org/)
  - [Gimp and OpenOffice Draw](http://wiki.gimp.org/gimp/OpenOfficeConvertion)

### GIMP コミュニティー

  - 日本語ページ

<!-- end list -->

  - \- GIMP 2 の紹介。Windows 用portable 版も配布

  - [Gimp wiki](http://twist.jpn.org/gimpwiki/)

  - [GIMPで画像編集](http://kumacrow.blog111.fc2.com/blog-category-24.html) - GIMP 2 の使い方。（初心者向け）

  - [GIMPの使い方](http://gimp2.web.fc2.com/) - GIMP 2 の使い方を解説。

  - [GIMP思い込みチュートリアル](http://gimp.blog.shinobi.jp/) - GIMP 2 の使い方。チュートリアルなど。

<!-- end list -->

  - 英語ページ

<!-- end list -->

  - [GIMP for Windows](https://www.gimp.org/downloads/)  Windows用パッケージ（多言語対応）の公開サイト
  - [GIMP User Group](http://gug.criticalhit.dk/)
  - [gimpuser.com](http://www.gimpusers.com/)
  - [GIMP Professional Presets Archives](http://www.gimpppa.org/)
  - GIMP for Windows user mailing list（現在は稼働していない）の ([Read-only archive](http://www.spinics.net/lists/gimpwin/))

[Category:オープンソースソフトウェア](https://ja.wikipedia.org/wiki/Category:オープンソースソフトウェア "wikilink") [Category:グラフィックデザイン](https://ja.wikipedia.org/wiki/Category:グラフィックデザイン "wikilink") [Category:画像処理ソフト](https://ja.wikipedia.org/wiki/Category:画像処理ソフト "wikilink") [Category:ペイントソフト](https://ja.wikipedia.org/wiki/Category:ペイントソフト "wikilink") [Category:GTK+を使用するソフトウェア](https://ja.wikipedia.org/wiki/Category:GTK+を使用するソフトウェア "wikilink") [Category:1996年のソフトウェア](https://ja.wikipedia.org/wiki/Category:1996年のソフトウェア "wikilink")

1.  プラグインの追加によりTIFF形式でのインポート、TIFF/JPEG/PSD形式でのエクスポートは可能
2.  ディスプレイフィルタと呼ばれる種類のモジュールによって実現されている
3.  公式サイトにある Windows、および Mac OS 向けのダウンロードページには、バイナリ配布を行っている外部サイトへのリンクが記載されている。また、Mac OS 向けバイナリは[2.2系](http://gimp-app.sourceforge.net/)、[2.4系](http://darwingimp.sourceforge.net/)、[2.6系](http://gimp.lisanet.de/Website/Overview.html)でそれぞれ配布元が異なる
4.  <http://gimp.org/about/ancient_history.html>
5.
6.  <http://gimp.org/about/history.html>
7.
8.
9.
10. [ANNOUNCE: GIMP 2.6.0](http://lists.xcf.berkeley.edu/lists/gimp-announce/2008-October/000104.html)（2008年10月1日18時56分（UTC））
11. [GIMP 2.8 Release Notes](http://www.gimp.org/release-notes/gimp-2.8.html)
12. [GIMP 2.10 Release Notes](https://www.gimp.org/release-notes/gimp-2.10.html)
13.
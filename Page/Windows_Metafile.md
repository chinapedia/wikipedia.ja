> この記事は[Windows Metafile](https://ja.wikipedia.org/wiki/Windows_Metafile)から翻訳されています。


**Windows Metafile**（**WMF**、ウィンドウズ メタファイル）は[Microsoft Windows上の](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")[画像ファイルフォーマット](https://ja.wikipedia.org/wiki/画像ファイルフォーマット "wikilink")の1つであり、1990年代初期に設計された。[ベクトル画像](https://ja.wikipedia.org/wiki/ベクトル画像 "wikilink")フォーマットであり、[ビットマップ画像](../Page/ビットマップ画像.md "wikilink")を内部に含むことも可能となっている。基本的にWMFファイルはWindowsのグラフィックス[API層である](https://ja.wikipedia.org/wiki/Application_Programming_Interface "wikilink")[GDIが実行すべき関数呼び出しのリストであって](../Page/Graphics_Device_Interface.md "wikilink")、それによって[画像](../Page/画像.md "wikilink")が再生される。GDI関数の中には[例外処理](../Page/例外処理.md "wikilink")のために[コールバック関数の](../Page/コールバック_\(情報工学\).md "wikilink")[ポインタを引数にとるものがあるため](../Page/ポインタ_\(プログラミング\).md "wikilink")、WMFファイルには実行可能コードが含まれることがある。その設計手法は[UNIX](../Page/UNIX.md "wikilink")における[PostScript](../Page/PostScript.md "wikilink")に似ている。

Windows 3.0で最初に導入されたWMFは16ビット形式であった。後に追加された32ビット版ではコマンドが追加されており、**Enhanced Metafile** (**EMF**) と呼ばれる。EMFは[プリンター](https://ja.wikipedia.org/wiki/プリンター "wikilink")[ドライバーのグラフィックス言語としても使われている](https://ja.wikipedia.org/wiki/デバイスドライバー "wikilink")。

2018年現在、WMFはリビジョン15.0の仕様書がオンラインで参照およびダウンロードできる\[1\]。

また2018年現在、EMFはリビジョン14.0の仕様書がオンラインで参照およびダウンロードできる\[2\]。

## 仕様と特許

オリジナルの16bit WMFファイル形式は1992年のWindows 3.1 SDKの\[3\]4巻に定義された。しかし仕様の一部は詳細があいまいな部分があった。これらのマニュアルは書籍として買い求めることができる。EULAや特別なライセンスの制限などは課されていない。（ソフトウエアの一部であり....という一般的な文言のみがあった）

時が経つにつれてこの歴史的な仕様書の存在は忘れられ、WMFファイルに対するリバースエンジニアリングが行われるようになったが、これには困難が伴い、正確さも欠いていた。 2006年9月にMicrosoftは再度WMFファイル形式の仕様を[Microsoft Open Specification Promiseの一環として公開](https://ja.wikipedia.org/wiki/Microsoft_Open_Specification_Promise "wikilink")\[4\]し、これを実装する者に対して特許権を行使しないことを約束した。

## 派生物

1993年に32bit版のWin32/GDIによる*Enhanced Metafile* (EMF) が登場し、これには数点のコマンドの拡張が含まれた。EMFはプリンタドライバーとやりとりするグラフィックス言語としても利用された。Microsoftは、WMFはほぼ使用されず、拡張フォーマット (EMF) で代替することを推奨している。 [Windows XPの公開に合わせて](https://ja.wikipedia.org/wiki/Windows_XP "wikilink")*Enhanced Metafile Format Plus Extensions* (EMF+) フォーマットが登場した。これには[GDI+](https://ja.wikipedia.org/wiki/GDI+ "wikilink") APIコールのシリアライズ機能が WMF/EMF と同様の方法で追加されている。

他に圧縮された形式の*Compressed Windows Metafile* (WMZ) と*Compressed Enhanced Windows Metafile* (EMZ) も存在する\[5\]。

EMZはEMFファイル形式をgzip圧縮したものである。

## SetAbortProcの脆弱性問題

2005年11月、"SetAbortProc" GDI関数に[脆弱性](../Page/脆弱性.md "wikilink")が発見された。この関数は印刷の[スプーリング](../Page/スプーリング.md "wikilink")をキャンセルしたときのエラー処理ハンドラを登録するもので、ユーザーの許可なしで実行できる任意のコードをWMFファイルに追加可能にしている。

マイクロソフトは公式のパッチ (MS06-001) を2006年1月5日にリリースし、詳細は "マイクロソフト セキュリティ アドバイザリ 912840 Graphics Rendering Engine の脆弱性によりコードが実行される可能性がある" (912919)\[6\]で見ることができる。 古いバージョンのWindowsについてはパッチを提供していない。

セキュリティ専門家のは、この脆弱性がマイクロソフトが故意にWMFに仕込んだ[バックドア](../Page/バックドア.md "wikilink")であると主張した。しかし、他のセキュリティ専門家はこれに異を唱えており、バックドアと呼ぶにはマイクロソフトが実際にこの脆弱性を利用して秘密裏にコンピュータにアクセスしたことを実証しなければならないとしている\[7\]。マイクロソフトの従業員である[Mark Russinovichは](https://ja.wikipedia.org/wiki/Mark_Russinovich "wikilink")、Gibsonの分析はいくつかの誤解に基づいていると説明している。

## 代替実装

WMFフォーマットはWindowsの[GDIで実行されることで](../Page/Graphics_Device_Interface.md "wikilink")[画像](../Page/画像.md "wikilink")を再生する。しかし、WMF形式のファイルにはその画像を構成するGDIのグラフィックプリミティブの定義も含まれているので、他のライブラリを使ってWMFのバイナリファイルを描画させたり、他の画像フォーマットに変換できる。

一例として、[Batik](https://ja.wikipedia.org/wiki/Batik "wikilink")ライブラリはWMFファイルを描画したり、[SVGに変換したりできる](../Page/Scalable_Vector_Graphics.md "wikilink")。[FreeHEP](https://ja.wikipedia.org/wiki/FreeHEP "wikilink") [Java](https://ja.wikipedia.org/wiki/Java "wikilink")ライブラリのVector Graphicsパッケージでは、[Java 2Dで描画されたものをEMFファイルとして保存できる](../Page/Java_2D.md "wikilink")。[Inkscape](../Page/Inkscape.md "wikilink")と[XnView](https://ja.wikipedia.org/wiki/XnView "wikilink")もWMFとEMF形式でのエクスポートができる。

## 脚注

<references/>

## 関連項目

  - [Scalable Vector Graphics](../Page/Scalable_Vector_Graphics.md "wikilink") (SVG)
  - [PostScript](../Page/PostScript.md "wikilink")
  - [メタファイル](../Page/メタファイル.md "wikilink")

## 外部リンク

### チュートリアルなど

  - [マイクロソフトによる Windows Metafile Format 仕様](https://msdn.microsoft.com/ja-jp/library/cc215212.aspx)
  - \[<https://msdn.microsoft.com/ja-jp/library/dd145051(v=vs.85>).aspx Windows GDI-Metafiles\]
  - [Windows GDI](http://msdn2.microsoft.com/en-us/library/ms534274.aspx)

<!-- end list -->

  - [File Format Summary at fileformat.info](http://www.fileformat.info/format/wmf/)
  - [WMF operand documentation](http://wvware.sourceforge.net/caolan/index.html)
  - [FAQ about Windows Metafile](http://www.companionsoftware.com/PR/WMRC/WindowsMetafileFaq.html)

### ライブラリ

  - Batik Java library: [WMF to SVG transcoder package](http://xml.apache.org/batik/javadoc/org/apache/batik/transcoder/wmf/tosvg/package-summary.html) WMFメタファイルから[SVGへの変換が可能](../Page/Scalable_Vector_Graphics.md "wikilink")
  - FreeHEP Java library: [Vector graphics package](http://java.freehep.org/freehep1.x/vectorgraphics/index.html) EMFメタファイルからSVGへの変換およびJava2DからEMFへの変換をサポート
  - [libWMF](http://wvware.sourceforge.net/libwmf.html) WMFメタファイルを読み込むライブラリ。表示や[SVGへの変換が可能](../Page/Scalable_Vector_Graphics.md "wikilink")
  - [libEMF](http://libemf.sourceforge.net/) [POSIX](../Page/POSIX.md "wikilink")システム上でのベクター画像ファイルを生成するための描画ツールキットを提供するC/C++ライブラリ
  - [wmf2svg](http://www.blackdirt.com/graphics/svg/) WMFメタファイルから[SVGへの変換を実装したJava用クラス](../Page/Scalable_Vector_Graphics.md "wikilink")

[Category:画像ファイルフォーマット](https://ja.wikipedia.org/wiki/Category:画像ファイルフォーマット "wikilink") [Category:ベクターグラフィックス](https://ja.wikipedia.org/wiki/Category:ベクターグラフィックス "wikilink") [Category:Microsoft_Windows](https://ja.wikipedia.org/wiki/Category:Microsoft_Windows "wikilink")

1.
2.
3.  Microsoft Windows 3.1 Programmers Reference, Volume 4 Resources, Microsoft Press 1992, ISBN 1-55615-494-1, chapter 3 pp. 21-45
4.
5.  [Officeサポート 挿入および保存できるグラフィックス ファイルの種類](https://support.office.com/ja-jp/article/%E6%8C%BF%E5%85%A5%E3%81%8A%E3%82%88%E3%81%B3%E4%BF%9D%E5%AD%98%E3%81%A7%E3%81%8D%E3%82%8B%E3%82%B0%E3%83%A9%E3%83%95%E3%82%A3%E3%83%83%E3%82%AF%E3%82%B9-%E3%83%95%E3%82%A1%E3%82%A4%E3%83%AB%E3%81%AE%E7%A8%AE%E9%A1%9E-dad53574-3384-4ced-b472-348d37c326a7)
6.  <https://technet.microsoft.com/ja-jp/library/security/912840.aspx> マイクロソフト セキュリティ アドバイザリ 912840 Graphics Rendering Engine の脆弱性によりコードが実行される可能性がある
7.  ['Windows backdoor' theory causes kerfuffle](http://archive.is/20130425152304/http://news.com.com/2061-10789_3-6027130.html) CNET News - News Blogs
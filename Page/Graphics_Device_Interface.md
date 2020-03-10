> この記事は[Graphics Device Interface](https://ja.wikipedia.org/wiki/Graphics_Device_Interface)から翻訳されています。


（グラフィックス・デバイス・インターフェイス、**GDI**）\[1\]とは、[カーネル](../Page/カーネル.md "wikilink")及びユーザー（[ウィンドウマネージャ](https://ja.wikipedia.org/wiki/ウィンドウマネージャ "wikilink")）と協調する [Windows](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink") の3つの主要[コンポーネント](https://ja.wikipedia.org/wiki/コンポーネント "wikilink")（サブシステム）の1つ。

GDI はグラフィカルオブジェクトの表示と、[ディスプレイや](../Page/ディスプレイ_\(コンピュータ\).md "wikilink")[プリンター](https://ja.wikipedia.org/wiki/プリンター "wikilink")のような[出力](https://ja.wikipedia.org/wiki/出力 "wikilink")[機器への転送のための](https://ja.wikipedia.org/wiki/デバイス "wikilink") Windows 規格である。

## GDI

GDI は直線や曲線の描画、[フォント](../Page/フォント.md "wikilink")の[レンダリング](https://ja.wikipedia.org/wiki/レンダリング_\(コンピュータ\) "wikilink")、[パレットの制御といった処理を担当する](../Page/カラーチャート.md "wikilink")（gdi32.dll）。[ウィンドウ](../Page/ウィンドウ.md "wikilink")や[メニューなどのような上位レベルの描画については直接関わらず](https://ja.wikipedia.org/wiki/メニュー_\(コンピュータ\) "wikilink")、より上位の user32.dll にあるユーザーサブシステムに任される。

GDI は[ハードウェア](../Page/ハードウェア.md "wikilink")に直接アクセスするドライバよりも上位に位置し、デバイスの機能的な調整と抽象化が GDI の役目である。GDI を使うことにより、画面やプリンターなどの多様なデバイスに容易に描画でき、そして各デバイスで適切な表示結果を望める。この機能はWindowsの全ての [WYSIWYG](../Page/WYSIWYG.md "wikilink") アプリケーションの要である。

[フリーセル](../Page/フリーセル.md "wikilink")や[マインスイーパ](https://ja.wikipedia.org/wiki/マインスイーパ "wikilink")のような高速な描画が不要なゲームは GDI を使用する。しかし、GDI はアニメーションをうまく表示できず（フレームバッファ同期の概念が無い）、[3D](../Page/3次元コンピュータグラフィックス.md "wikilink") [ラスタライズ](https://ja.wikipedia.org/wiki/ラスタライズ "wikilink")機能がないこともあり、最新のゲームではハードウェアの機能をより活用できる [DirectX](https://ja.wikipedia.org/wiki/DirectX "wikilink") または [OpenGL](../Page/OpenGL.md "wikilink") が使われる。

[Windows Vista](https://ja.wikipedia.org/wiki/Microsoft_Windows_Vista "wikilink") では、GDI アプリケーションは新しい描画エンジンである [Desktop Window Manager](https://ja.wikipedia.org/wiki/Desktop_Window_Manager "wikilink") (DWM) のもとで動作し、GDIコンテンツはいったんシステムメモリ上のビットマップに[CPU](../Page/CPU.md "wikilink")で描画され、[ハードウェアアクセラレーション](../Page/ハードウェアアクセラレーション.md "wikilink")は用いられない。[Windows 7](https://ja.wikipedia.org/wiki/Windows_7 "wikilink") 以降では GDI の一部\[2\]が再びハードウェアアクセラレートされるようになっているが、DWM が有効になっている必要がある\[3\]。

## GDI プリンター

**GDI プリンター**（[Winmodem](https://ja.wikipedia.org/wiki/Winmodem "wikilink") のように **Winprinters** としても知られている）、特に GDI [レーザープリンター](https://ja.wikipedia.org/wiki/レーザープリンター "wikilink")は本来プリンターが行う処理の一部をホストコンピュータ (PC) 側で代行する。ホストコンピュータでビットマップイメージを描写し、プリンターにビットマップを転送する。この方式には以下の2つの利点がある。

  - 描画処理用 [CPU](../Page/CPU.md "wikilink") と [RAM](../Page/Random_Access_Memory.md "wikilink") をプリンターに搭載する費用を節約できる。
  - 受け取ったイメージを印刷することに特化することで性能の最適化ができる。

また、以下の点で不利である。

  - ホストコンピュータの負荷が高くなる。最近のPCでは問題ないが、古いPCで複雑なドキュメントを印刷する場合は非常に遅くなる場合がある。
  - GDI プリンターは通常、プリンターの[ファームウェア](../Page/ファームウェア.md "wikilink")に標準的な印刷機能の[エミュレーションを含まない](../Page/エミュレータ.md "wikilink")（またはそれを処理できる能力を持たない）。[ハイエンド](https://ja.wikipedia.org/wiki/ハイエンド "wikilink")の [PCL](../Page/PCL.md "wikilink") プリンターや [PostScript](../Page/PostScript.md "wikilink")プリンターでは、ソフトウェアの互換性やドライバの[バグ](../Page/バグ.md "wikilink")などの問題があった場合にドライバを更新して対応できるが、GDI プリンターでは対応策がない場合がある。
  - GDIプリンターは一般的に Windows に限り動作する。例外はあるが、他の [OS](../Page/オペレーティングシステム.md "wikilink") では原則的に GDI プリンターを使用できない。

最新の[インクジェットプリンター](../Page/インクジェットプリンター.md "wikilink")の機種は GDI ベース（レーザプリンターでは費用が主要因であるのに対し、ここでは主に性能の理由）であるが、より柔軟な傾向がある。多くが [Mac](../Page/Macintosh.md "wikilink") に対応し、[Linux](../Page/Linux.md "wikilink") コミュニティでは Linux 版ドライバの対応をかなり改善した。一部（特に[セイコーエプソン](../Page/セイコーエプソン.md "wikilink")）ではより伝統的なエミュレーションを予備として提供することが多い。

一般的には安価なレーザプリンターは GDI デバイスであるが、多くのメーカーでは [PCL](https://ja.wikipedia.org/wiki/Printer_Command_Language "wikilink") や [PostScript](../Page/PostScript.md "wikilink") あるいはその両方の機能を持つモデルも製造している。GDI のみに対応するプリンターはどのメーカーにおいても最も安価なモデルとして位置づけられる。

## 詳細

### デバイスコンテキスト

**デバイスコンテキスト**は、描画する対象を抽象化した存在である。画面またはプリンターへ出力するテキスト及びイメージの属性を定義するために使われ、関連付けられたグラフィックスオブジェクトとそれに関連する属性の集合からなる。実際のコンテキストはGDIによって管理される。構造体へのハンドルであるデバイスコンテキストは出力を行う前に取得し、要素が書き込まれた後に解放する。大抵のGDIオブジェクトのように、デバイスコンテキストは直接データにアクセスできないという意味で隠蔽されているが、それを制御し、何かを描画し、情報を取得し、オブジェクトを変更するといったような様々な GDI 関数にデバイスコンテキストを渡すことができる。

デバイスコンテキストには次の種類がある。

  - 画面
  - プリンター
  - メモリ
  - 情報（インフォメーションコンテキスト）

このうち、情報は描画に用いることはできない情報取得専用のデバイスコンテキストである。

### グラフィックスオブジェクト

デバイスコンテキストに関連付けが可能なグラフィクスオブジェクトには次の種類がある。これらは、`SelectObject`関数\[4\]や`SelectPalette`関数\[5\]によってデバイスコンテキストに関連付けさせることが可能である。

  - ビットマップ (HBITMAP)
  - ブラシ (HBRUSH)
  - フォント (HFONT)
  - ペン (HPEN)
  - リージョン (HRGN)
  - パス (リージョンに変換可能)
  - パレット (HPALETTE)

なおGDIオブジェクトの数は、1セッションで65,535個まで、そして1プロセスで10,000個までという上限が設けられている\[6\]。

## GDI+

GDI+ は [Windows XP](../Page/Microsoft_Windows_XP.md "wikilink") で新しく登場したグラフィックスサブシステムである。Windows XP 以降のOSに標準搭載されているほか、Windows 98/NT 4.0 SP6 以降で追加インストールにより使用可能である\[7\] \[8\] \[9\]。

GDI+は高レベルの [2D](https://ja.wikipedia.org/wiki/2次元コンピュータグラフィックス "wikilink") グラフィック環境であり、[アルファブレンド](https://ja.wikipedia.org/wiki/アルファブレンド "wikilink")、グラデーション、[アンチエイリアス](https://ja.wikipedia.org/wiki/アンチエイリアス "wikilink")、より複雑なラインパス管理、（GDI で特に欠けていた）[JPEG](../Page/JPEG.md "wikilink") や [PNG](../Page/Portable_Network_Graphics.md "wikilink") のような新標準の[画像形式の根本的な対応](https://ja.wikipedia.org/wiki/画像ファイルフォーマット "wikilink")、2D 表示のパイプライン上の[アフィン変換の合成に対する統合的な対応といった先進的な機能を追加している](../Page/アフィン写像.md "wikilink")。これらの機能は Windows XP の[ユーザーインターフェイスの様々な箇所に使われており](../Page/ユーザインタフェース.md "wikilink")、このような基本的なグラフィックスレイヤーの表現能力拡張は、[Flash](../Page/Adobe_Flash.md "wikilink") や [SVG](../Page/Scalable_Vector_Graphics.md "wikilink") といった[ベクターグラフィックスシステムの実装を大きく単純化する](https://ja.wikipedia.org/wiki/ベクターイメージ "wikilink")。

基本的にはネイティブ [C++](../Page/C++.md "wikilink") 用のクラスライブラリ ([DLL](https://ja.wikipedia.org/wiki/DLL "wikilink")) のみが提供される形となっているが、[.NET Framework](https://ja.wikipedia.org/wiki/.NET_Framework "wikilink") の基本クラスライブラリでは `System.Drawing` [名前空間](../Page/名前空間.md "wikilink")に GDI+ のマネージラッパーインターフェイスが用意されており\[10\]\[11\]、[Windows Formsなどで標準的に使用されている](../Page/Windows_Forms.md "wikilink")。[Delphi](../Page/Delphi.md "wikilink")においてもGDI+のユニットが利用可能となっている。

なお、Vista で v1.1 となった。C++アプリケーションにおいてGDI+ 1.1の追加機能を使うためには、`<gdiplus.h>`をインクルードする前に`GDIPVER`を`0x0110`として定義し、さらにGdiPlus.dllの[Side-by-Sideアセンブリバージョン](https://ja.wikipedia.org/wiki/分離アプリケーションとSide-by-Sideアセンブリ "wikilink")1.1を使うようにマニフェストを指定しなければならない。

## Direct2D

Windows Vistaでは、ハードウェアによるGDIアクセラレーションが実行されず、GDI描画はすべてCPUで実行されることになる（ただし[BitBltは除く](../Page/Bit_Block_Transfer.md "wikilink")）\[12\]。また、GDI+では飛躍的に表現力や描画品質が向上しているが、内部で使用されているAPIはレガシーなGDIそのものであったりソフトウェア実装であったりするため、描画速度は当然犠牲になる。これらを補完する形でWindows 7とともに登場したのが [Direct2D](https://ja.wikipedia.org/wiki/Direct2D "wikilink") および [DirectWrite](https://ja.wikipedia.org/wiki/DirectWrite "wikilink") である。Direct2D/DirectWrite は、GDI+ のような先進的な機能を [Direct3D](https://ja.wikipedia.org/wiki/Direct3D "wikilink") 10.1 上に構築した [COM](../Page/Component_Object_Model.md "wikilink") ベースの高レベル API で、GDI/GDI+ で問題となっていた描画速度性能を、Direct3D によるハードウェアアクセラレーションを活用することで大幅に改善することが可能となる。さらに、Direct2DはDirect3D上に構築されているため、DWMの使用有無にかかわらずハードウェアアクセラレートされる。また、DirectWriteはGDI+に欠けていた、[OpenType](../Page/OpenType.md "wikilink")フォントへの対応や垂直方向への[ClearType](../Page/ClearType.md "wikilink")アンチエイリアスといった機能を備えている。 なお、Windows 7 および Windows Vista SP2 + Platform Update 以降に提供されている Direct2D 1.0 では、印刷機能（印刷機器への出力機能）に直接対応しないため、印刷時には GDI/GDI+ あるいは XPS ドキュメント API（[XPS](../Page/XML_Paper_Specification.md "wikilink") 作成やそれを用いての印刷などに対応する API）を使用する必要がある。しかし、Windows 8 および Windows 7 SP1 + Platform Update 以降に提供されている Direct2D 1.1 以降であれば、メタデータの出力機能などが追加実装されており、描画内容をプリンターデバイスに出力して印刷することも可能である\[13\]。 さらに、Direct2DにはベースとなっているDirect3Dとの連携機構が確保されており、Direct2D 1.0 APIを使用して[DXGIインターフェイス経由でDirect](https://ja.wikipedia.org/wiki/DirectX_Graphics_Infrastructure "wikilink")3D 10.xテクスチャに直接書き込んだり、またDirect2D 1.1 APIを使用してDirect3D 11.xテクスチャに直接書き込んだりすることが可能となっている。

なお、GDI+での強化点であった各種形式の画像ファイルの読み込みや書き出しといった機能に関しては、Direct2Dコンポーネントは直接サポートせず、代わりにWIC（[Windows Imaging Component](https://ja.wikipedia.org/wiki/Windows_Imaging_Component "wikilink")）が担うことになる。

## 脚注

## 関連項目

  - [WinG](../Page/WinG.md "wikilink")
  - [DirectX](https://ja.wikipedia.org/wiki/DirectX "wikilink")
  - [Windows Graphics Foundation](https://ja.wikipedia.org/wiki/Windows_Graphics_Foundation "wikilink")
  - [ラスターイメージプロセッサ](../Page/ラスターイメージプロセッサ.md "wikilink") (Raster Image Processor)
  - [Direct2D](https://ja.wikipedia.org/wiki/Direct2D "wikilink")
  - [Direct3D](https://ja.wikipedia.org/wiki/Direct3D "wikilink")

## 外部リンク

  - [Windows GDI Start Page](http://msdn.microsoft.com/en-us/library/dd145203.aspx)
  - [GDI+](http://msdn.microsoft.com/en-us/library/ms533798.aspx)

[Category:グラフィックライブラリ](https://ja.wikipedia.org/wiki/Category:グラフィックライブラリ "wikilink") [Category:マイクロソフトのAPI](https://ja.wikipedia.org/wiki/Category:マイクロソフトのAPI "wikilink") [Category:オペレーティングシステムの仕組み](https://ja.wikipedia.org/wiki/Category:オペレーティングシステムの仕組み "wikilink")

1.  [Windows グラフィックス アーキテクチャの概要 (Windows)](https://msdn.microsoft.com/ja-jp/library/windows/desktop/ff684176.aspx)
2.  [GDI rendering in Windows 7 : Comparing Direct2D and GDI Hardware Acceleration | Microsoft Docs](https://docs.microsoft.com/ja-jp/windows/desktop/Direct2D/comparing-direct2d-and-gdi#gdi-rendering-in-windows-7)
3.  [Availability of Hardware Acceleration : Comparing Direct2D and GDI Hardware Acceleration | Microsoft Docs](https://docs.microsoft.com/ja-jp/windows/desktop/Direct2D/comparing-direct2d-and-gdi#availability-of-hardware-acceleration)
4.  [SelectObject function (wingdi.h) | Microsoft Docs](https://docs.microsoft.com/en-us/windows/desktop/api/wingdi/nf-wingdi-selectobject)
5.  [SelectPalette function (wingdi.h) | Microsoft Docs](https://docs.microsoft.com/en-us/windows/desktop/api/wingdi/nf-wingdi-selectpalette)
6.  [Windows の限界に挑む: USER オブジェクトと GDI オブジェクト – 第 2 部](https://technet.microsoft.com/ja-jp/windows/mark_17.aspx)
7.
8.
9.
10. [System.Drawing Namespace | Microsoft Docs](https://docs.microsoft.com/en-us/dotnet/api/system.drawing)
11. [About GDI+ Managed Code | Microsoft Docs](https://docs.microsoft.com/en-us/dotnet/framework/winforms/advanced/about-gdi-managed-code)
12. [GDI and Direct2D hardware acceleration : Comparing Direct2D and GDI Hardware Acceleration | Microsoft Docs](https://docs.microsoft.com/ja-jp/windows/desktop/Direct2D/comparing-direct2d-and-gdi#gdi-and-direct2d-hardware-acceleration)
13. [What's new in Direct2D (Windows)](https://msdn.microsoft.com/en-us/library/windows/desktop/hh802478.aspx)
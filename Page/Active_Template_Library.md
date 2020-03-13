> この記事は[Active Template Library](https://ja.wikipedia.org/wiki/Active_Template_Library)から翻訳されています。


**Active Template Library** (**ATL**) は、[COMプログラミングを簡単に行えるようにするためのマイクロソフトによる](../Page/Component_Object_Model.md "wikilink")[テンプレートベースの](../Page/テンプレート_\(プログラミング\).md "wikilink")[C++](../Page/C++.md "wikilink")専用[ライブラリ](../Page/ライブラリ.md "wikilink")である。様々なCOMオブジェクト、[OLEオートメーション](https://ja.wikipedia.org/wiki/OLEオートメーション "wikilink")サーバ、[ActiveX](../Page/ActiveX.md "wikilink")コントロールを開発できるように作られている。ATL 1.0は1996年に公開され、Microsoft [Visual C++にはバージョン](https://ja.wikipedia.org/wiki/Visual_C++ "wikilink")6.0からATLが標準で付属するようになった（VC 6.0付属のバージョンはATL 3.0）。

インターネット用のコントロールは[MFCも利用できるが](../Page/Microsoft_Foundation_Class.md "wikilink")、ウェブサーバーからネットワーク経由でダウンロードするためにコントロールは小さくコンパクトであることが求められる。MFCアプリケーションは総じてプログラムサイズが巨大になる。ATLでは補助DLLなしで小さなコントロールを作成できるため、ATLはある意味でCOMコントロールの開発環境としてMFCに対する軽量の代替物である。

また、ATLには[Windows APIのラッパーとして利用できるクラスもあり](../Page/Windows_API.md "wikilink")、[WTLと併せて通常のWindows用の](../Page/Windows_Template_Library.md "wikilink")[アプリケーションソフトウェア](../Page/アプリケーションソフトウェア.md "wikilink")作成にも用いることができる。

Visual C++ 7.0 (Visual C++ .NET 2002) 付属のATL 7.0以降はMFCとの統合が図られ、一部のクラスは共通化されている\[1\]。また、Visual C++ .NET 2002以降、バージョン番号はATL、MFCともにVisual C++の内部バージョンと同じになった\[2\]。なおATLのバージョンを表す定義済みシンボルとして、`_ATL_VER`が存在する\[3\]。

Visual C++ 2013以降はDLL版のATLは廃止され、スタティックリンク版のみの提供となっている\[4\]。

[Microsoft Visual Studio](https://ja.wikipedia.org/wiki/Microsoft_Visual_Studio "wikilink") 2012までは、ATLおよびMFCは有償版のエディション（StandardもしくはProfessional以上）のみに付属するライブラリだったが、2014年にリリースされたVisual Studio Community 2013は無償版でありながら機能的にはProfessionalエディション相当となり、ATL/MFCも付属している（ただし利用規約はExpressエディションよりも制約が厳しい\[5\]）。

## 脚注

## 関連項目

  - [Component Object Model](../Page/Component_Object_Model.md "wikilink")
  - [Microsoft Foundation Class](../Page/Microsoft_Foundation_Class.md "wikilink")
  - [Windows Template Library](../Page/Windows_Template_Library.md "wikilink")

[Category:ライブラリ_(プログラミング)](https://ja.wikipedia.org/wiki/Category:ライブラリ_\(プログラミング\) "wikilink") [Category:C++](https://ja.wikipedia.org/wiki/Category:C++ "wikilink") [Category:マイクロソフトのAPI](https://ja.wikipedia.org/wiki/Category:マイクロソフトのAPI "wikilink")

1.  [共有クラス (ATL/MFC)](https://msdn.microsoft.com/ja-jp/library/ekdt199a%28v=vs.71%29.aspx)
2.  [ATL と MFC のバージョン番号](https://msdn.microsoft.com/ja-jp/library/3z02ch3k%28v=vs.90%29.aspx)
3.  [定義済みマクロ](https://msdn.microsoft.com/ja-jp/library/b0084kay.aspx)
4.  [ATL and MFC changes and fixes in Visual Studio 2013 - Visual C++ Team Blog - Site Home - MSDN Blogs](http://blogs.msdn.com/b/vcblog/archive/2013/08/20/atl-and-mfc-changes-and-fixes-in-visual-studio-2013.aspx)
5.  [Visual Studio Community 2013 - Visual Studio](https://www.microsoft.com/ja-jp/dev/products/community.aspx)
> この記事は[DirectDraw](https://ja.wikipedia.org/wiki/DirectDraw)から翻訳されています。


**DirectDraw**は[マイクロソフト](../Page/マイクロソフト.md "wikilink")の[DirectX](https://ja.wikipedia.org/wiki/DirectX "wikilink") [APIの一部である](../Page/アプリケーションプログラミングインタフェース.md "wikilink")。パフォーマンスが重要なアプリケーションで[コンピュータグラフィックス](../Page/コンピュータグラフィックス.md "wikilink")を高速に[レンダリングするために使用する](../Page/レンダリング_\(コンピュータ\).md "wikilink")。DirectDrawアプリケーションはフルスクリーンで動作するほか、一般的な[Windows](https://ja.wikipedia.org/wiki/Windows "wikilink")デスクトップアプリケーションのようにウィンドウ内で動作するようにもできる。[ビデオカード](../Page/ビデオカード.md "wikilink")などのグラフィックスデバイスが持つ[ハードウェアアクセラレーション](../Page/ハードウェアアクセラレーション.md "wikilink")機能を利用できる場合はこれを利用する。DirectDrawは[ビデオメモリ](https://ja.wikipedia.org/wiki/ビデオメモリ "wikilink")、[ハードウェアオーバーレイ](https://ja.wikipedia.org/wiki/ハードウェアオーバーレイ "wikilink")、ハードウェア[ブロック転送](../Page/Bit_Block_Transfer.md "wikilink")、[ページフリップを直接操作できる](https://ja.wikipedia.org/wiki/ダブルバッファ "wikilink")。DirectDrawの[ビデオメモリ](https://ja.wikipedia.org/wiki/ビデオメモリ "wikilink")マネージャは簡単にビデオメモリを操作でき、[ブロック転送をうまく活用でき](../Page/Bit_Block_Transfer.md "wikilink")、様々な[ビデオカード](../Page/ビデオカード.md "wikilink")で様々な色数に対応できる。

DirectDrawは[2次元コンピュータグラフィックス](../Page/2次元コンピュータグラフィックス.md "wikilink")のAPIである。すなわち、2Dレンダリングのためのコマンドが存在するのみで、[3Dハードウェアアクセラレーションはサポートしない](../Page/3次元コンピュータグラフィックス.md "wikilink")。半透明合成処理（アルファブレンド）に関しても同様である。DirectDrawを駆使して[レンダラー](https://ja.wikipedia.org/wiki/レンダラー "wikilink")を実装することで3D映像を描画することもできるが、3Dハードウェアアクセラレーションをサポートする[Direct3D](../Page/Direct3D.md "wikilink")のようなAPIと比較してレンダリングが遅くなる。

DirectXバージョン8.0において、DirectDrawは、Direct3Dに一部のDirectDraw APIを追加しただけの**DirectX Graphics**という新しいパッケージに統合され、事実上DirectDrawは廃止された。DirectDrawはDirectX 8以降と共存可能だが、DirectDrawを使用する場合は、古いバージョンのDirectXインターフェイス (DirectX 7およびそれ以前) を使わなければならない。

## 対応言語

DirectDrawは[COMベースのAPIであり](../Page/Component_Object_Model.md "wikilink")、主に[C++](../Page/C++.md "wikilink")から利用することを想定されている。ただし、DirectX 7ではC++以外に[Visual Basicも正式サポートされた](../Page/Visual_Basic.md "wikilink")\[1\]。

[Microsoft .NET用の](https://ja.wikipedia.org/wiki/.NET_Framework "wikilink")[Managed DirectXにもDirectDrawのサポートが存在する](https://ja.wikipedia.org/wiki/Microsoft_DirectX#Managed_DirectX "wikilink")\[2\]。

## 脚注

## 関連項目

  - [DirectDraw Surface](../Page/DirectDraw_Surface.md "wikilink")
  - [Direct3D](../Page/Direct3D.md "wikilink")
  - [DirectX](https://ja.wikipedia.org/wiki/DirectX "wikilink")

[Category:DirectX](https://ja.wikipedia.org/wiki/Category:DirectX "wikilink") [Category:グラフィックライブラリ](https://ja.wikipedia.org/wiki/Category:グラフィックライブラリ "wikilink")

1.  [Visual Basic で DirectX を使おう](https://msdn.microsoft.com/ja-jp/library/dd148667.aspx)
2.  [Managed DirectX (その 1 DirectDraw)](https://msdn.microsoft.com/ja-jp/library/dd188528.aspx)
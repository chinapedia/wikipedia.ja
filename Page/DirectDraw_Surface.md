> この記事は[DirectDraw Surface](https://ja.wikipedia.org/wiki/DirectDraw_Surface)から翻訳されています。


**DirectDraw Surface** (.dds) は[マイクロソフト](../Page/マイクロソフト.md "wikilink")によって開発された、[テクスチャや](https://ja.wikipedia.org/wiki/テクスチャマッピング "wikilink")[キューブ (環境) マップを格納するために利用される](https://ja.wikipedia.org/wiki/環境マッピング "wikilink")[ファイルフォーマット](../Page/ファイルフォーマット.md "wikilink")であり、圧縮形式と非圧縮形式の両方に対応している。これは、[Microsoft DirectX対応の](https://ja.wikipedia.org/wiki/Microsoft_DirectX "wikilink")[GPUのほか](../Page/Graphics_Processing_Unit.md "wikilink")、[プレイステーション3や](https://ja.wikipedia.org/wiki/PlayStation_3 "wikilink")[Xboxのような家庭用ゲーム機で利用される](../Page/Xbox_\(ゲーム機\).md "wikilink")[DXTC](https://ja.wikipedia.org/wiki/DXTC "wikilink") (S3TC) 圧縮データを格納できるように作られている。

## 歴史

このフォーマットはDirectX 7.0で導入された\[1\]。DirectDraw Surface自体はまた、[DirectDraw](https://ja.wikipedia.org/wiki/DirectDraw "wikilink")および[Direct3D](https://ja.wikipedia.org/wiki/Direct3D "wikilink")における基本的な画像単位を表す概念でもあった\[2\]。DirectX 8.0でボリュームテクスチャがサポートされた。

DirectX 10では`'DX10'`の[FourCC](https://ja.wikipedia.org/wiki/FourCC "wikilink")\[3\]およびDX10拡張ヘッダー\[4\]によりフォーマットが拡張され、追加の[DXGI](https://ja.wikipedia.org/wiki/DXGI "wikilink")フォーマットやテクスチャ配列をサポートするようになった。

元々は[DirectX](https://ja.wikipedia.org/wiki/DirectX "wikilink")のために設計されたが、[OpenGL](../Page/OpenGL.md "wikilink")でも同様に[GL_ARB_texture_compression](https://www.khronos.org/registry/OpenGL/extensions/ARB/ARB_texture_compression.txt), [GL_ARB_texture_compression_bptc](https://www.khronos.org/registry/OpenGL/extensions/ARB/ARB_texture_compression_bptc.txt)拡張によって利用可能である。

## 脚注

## 関連項目

  - [Microsoft DirectX](https://ja.wikipedia.org/wiki/Microsoft_DirectX "wikilink")
  - [Direct3D](https://ja.wikipedia.org/wiki/Direct3D "wikilink")
  - [DirectDraw](https://ja.wikipedia.org/wiki/DirectDraw "wikilink")
  - [DXTC](https://ja.wikipedia.org/wiki/DXTC "wikilink")

[Category:DirectX](https://ja.wikipedia.org/wiki/Category:DirectX "wikilink") [Category:ファイルフォーマット](https://ja.wikipedia.org/wiki/Category:ファイルフォーマット "wikilink")

1.  [DDS - Windows applications | Microsoft Docs](https://docs.microsoft.com/en-us/windows/desktop/direct3ddds/dx-graphics-dds)
2.  [DirectDraw Surfaces - Windows drivers | Microsoft Docs](https://docs.microsoft.com/en-us/windows-hardware/drivers/display/directdraw-surfaces)
3.  [DDS_PIXELFORMAT structure - Windows applications | Microsoft Docs](https://docs.microsoft.com/en-us/windows/desktop/direct3ddds/dds-pixelformat)
4.  [DDS_HEADER_DXT10 structure - Windows applications | Microsoft Docs](https://docs.microsoft.com/en-us/windows/desktop/direct3ddds/dds-header-dxt10)
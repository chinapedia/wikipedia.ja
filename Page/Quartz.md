> この記事は[Quartz](https://ja.wikipedia.org/wiki/Quartz)から翻訳されています。


**Quartz**（クオーツ）は、[アップルの](../Page/アップル_\(企業\).md "wikilink")[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink")  の描画コアエンジン。前身であるの[DPSに代わり](../Page/Display_PostScript.md "wikilink")、[PDFベースの描画モデルを採用したもの](../Page/Portable_Document_Format.md "wikilink")。三次[ベジェ曲線](../Page/ベジェ曲線.md "wikilink")を描画プリミティブとするベクトル型システムで、との互換性はない。なお、QuickDrawは[Carbon](../Page/Carbon.md "wikilink")アプリケーションの互換性のためにも残されている。

細かく言うと、アプリケーションで個々のバッファに描画を行なうプリミティブはと呼び、それらを最終的に[GPUのフレームバッファに合成する部分は](../Page/Graphics_Processing_Unit.md "wikilink")という。単にという場合は大抵の事である。現在のの構造では、、、、の各出力が最終的にによって画面に描画される形になっている。

の機能は、からはを通して、またC/C++言語からはを通して利用できる。またアップルはの[スクリプト言語](../Page/スクリプト言語.md "wikilink")[バインディングのひとつとして](https://ja.wikipedia.org/wiki/言語バインディング "wikilink")のバインディングを公式に用意している。

  - [解像度](../Page/解像度.md "wikilink")非依存の[ベクトルベース](https://ja.wikipedia.org/wiki/ベクトル画像 "wikilink")・システム
  - [浮動小数点](https://ja.wikipedia.org/wiki/浮動小数点 "wikilink")による[数学](../Page/数学.md "wikilink")[座標](../Page/座標.md "wikilink")系
  - 常時[アンチエイリアシング](../Page/アンチエイリアス.md "wikilink")
  - [アルファチャンネル](../Page/アルファチャンネル.md "wikilink")のサポート
  - [オブジェクト指向](../Page/オブジェクト指向.md "wikilink")の[API](../Page/アプリケーションプログラミングインタフェース.md "wikilink")
  - [Unicode](../Page/Unicode.md "wikilink")に対応した多国語文字描画ルーチン ([Apple Type Services for Unicode Imaging](https://ja.wikipedia.org/wiki/Apple_Type_Services_for_Unicode_Imaging "wikilink"))

() 以降では、環境に応じてGPUのジオメトリ演算ユニットを使って、 [CPU](../Page/CPU.md "wikilink")の負荷を軽減するが実装された。これはのバッファ合成をGPU内部で行なうシステムであり、これによりとの混在描画も可能となった。

() ではGPUの[プログラマブルシェーダ](https://ja.wikipedia.org/wiki/プログラマブルシェーダ "wikilink")を使って、描画演算をほぼ全てビデオチップ内で実行できる（()でに名称変更\[1\]）が隠し機能として搭載されている（多くの不具合を抱えたまま実装されオフにされており、正式にはサポートされていない\[2\]）。

## 脚注

## 関連項目

  -
  - （PDF）

  - [ベジェ曲線](../Page/ベジェ曲線.md "wikilink")

  - [アフィン変換](https://ja.wikipedia.org/wiki/アフィン変換 "wikilink")

  -
[Category:グラフィックライブラリ](https://ja.wikipedia.org/wiki/Category:グラフィックライブラリ "wikilink") [Category:MacOS](https://ja.wikipedia.org/wiki/Category:MacOS "wikilink")

1.
2.
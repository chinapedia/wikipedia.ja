> この記事は[ClearType](https://ja.wikipedia.org/wiki/ClearType)から翻訳されています。


[thumb](https://ja.wikipedia.org/wiki/ファイル:Liquid_Crystal_Display_Macro_Example_zoom.jpg "wikilink")

**ClearType**（クリアタイプ）は、[Microsoft Windows XP以降の](../Page/Microsoft_Windows_XP.md "wikilink")[Windows](https://ja.wikipedia.org/wiki/Windows "wikilink")が搭載する、[ディスプレイ文字の](https://ja.wikipedia.org/wiki/ディスプレイ_\(コンピュータ\) "wikilink")[アンチエイリアシング](https://ja.wikipedia.org/wiki/アンチエイリアシング "wikilink")技術である。

## 解説

[液晶ディスプレイ](https://ja.wikipedia.org/wiki/液晶ディスプレイ "wikilink")の構造である1[ピクセル](https://ja.wikipedia.org/wiki/ピクセル "wikilink")が[R、G、Bの](https://ja.wikipedia.org/wiki/RGB "wikilink")3サブピクセルで構成される点に着目し、R、G、Bの各サブピクセルを個別に発色させて横方向の見かけ[解像度を向上させ](https://ja.wikipedia.org/wiki/画面解像度 "wikilink")、実解像度以上の精細な文字表示を可能とする[サブピクセルレンダリング](https://ja.wikipedia.org/wiki/サブピクセルレンダリング "wikilink")\[1\]技術である。

[OSである](../Page/オペレーティングシステム.md "wikilink")[Windows上の](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")1ピクセルとディスプレイ上の1ピクセルが個対応する[液晶ディスプレイ](https://ja.wikipedia.org/wiki/液晶ディスプレイ "wikilink")で最も効果的だが、階調レベルの制御により[アパーチャーグリル](https://ja.wikipedia.org/wiki/アパーチャーグリル "wikilink")管など一般的な[CRTディスプレイでも実用的な効果を得る](https://ja.wikipedia.org/wiki/ブラウン管 "wikilink")。ClearTypeとほぼ同様の技術は[1998年](https://ja.wikipedia.org/wiki/1998年 "wikilink")に登場した[Mac OS 8.5などでも使われ](https://ja.wikipedia.org/wiki/Mac_OS "wikilink")、[Adobe](https://ja.wikipedia.org/wiki/Adobe "wikilink")が開発したも同様のサブピクセルレンダリング技術である\[2\]。

ClearTypeによる視認性の向上は使用する[フォント](https://ja.wikipedia.org/wiki/フォント "wikilink")に依存するため、単一色の中間階調で補完する標準アンチエイリアスとは異なる。

ClearTypeの根幹技術に[ヒンティングとスムージングがある](https://ja.wikipedia.org/wiki/フォントヒンティング "wikilink")。ヒンティングは文字を構成する線の太さと幅を調整して見かけの向上を図る技術で、制御情報はフォントに内包される。スムージングはアンチエイリアス同様に、発色の違いで[ジャギー](https://ja.wikipedia.org/wiki/ジャギー "wikilink")の平滑化を図る技術である。

## バージョン

[GDIによるClearTypeと](https://ja.wikipedia.org/wiki/Graphics_Device_Interface "wikilink")、[DirectWrite](https://ja.wikipedia.org/wiki/DirectWrite "wikilink")によるNatural ClearTypeに大別される。

### Windows XP

[thumb](https://ja.wikipedia.org/wiki/ファイル:ClearType_rendering_on_Windows_XP.png "wikilink")。\]\]

Windows XPはWindowsで最初にClearTypeを搭載したバージョンで、ClearTypeは初期状態で無効であり手動で有効にする必要がある\[3\]。日本語版Windows XPは、和文の[プリインストール](https://ja.wikipedia.org/wiki/プリインストール "wikilink")[フォント](https://ja.wikipedia.org/wiki/フォント "wikilink")である[MS ゴシック・MS Pゴシック・MS UI Gothic](https://ja.wikipedia.org/wiki/MS_ゴシック "wikilink")・[MS 明朝・MS P明朝が](https://ja.wikipedia.org/wiki/MS_明朝 "wikilink")、それぞれ小サイズの画面表示用に内蔵する[ビットマップフォント](https://ja.wikipedia.org/wiki/ビットマップフォント "wikilink")を表示するためにClearTypeは効果しない。[Microsoft Office付属の](https://ja.wikipedia.org/wiki/Microsoft_Office "wikilink")[HGフォントはビットマップを内包しておらずClearTypeが利用可能である](https://ja.wikipedia.org/wiki/HG#HGフォント "wikilink")。

[Windows Vistaのリリース後に配布されたフォントの](https://ja.wikipedia.org/wiki/Windows_Vista "wikilink")[メイリオ](https://ja.wikipedia.org/wiki/メイリオ "wikilink")\[4\]をインストールして[インターフェイスフォントに指定すれば](../Page/キャラクタユーザインタフェース.md "wikilink")、Windows Vistaと同様にClearTypeが有効な日本語インターフェイスが実現するが、メイリオは初期設定のMS UI Gothicよりも文字幅が広いため、システム画面で有効化するとメニュー表示の長尺化によるスクロールやダイアログボックスの画面外逸脱などが発生する場合があり、テーマの詳細設定を修正してデザインを変更する必要がある。

### WPFにおけるClearType

[Windows Presentation Foundation (WPF)](https://ja.wikipedia.org/wiki/Windows_Presentation_Foundation "wikilink") は、従来の水平方向のサブピクセル[レンダリングに加えて垂直方向のアンチエイリアス処理も施す](https://ja.wikipedia.org/wiki/レンダリング_\(コンピュータ\) "wikilink")\[5\]。WPFの新しいClearTypeを利用するために[アプリケーションが](../Page/アプリケーションソフトウェア.md "wikilink")[APIを呼び出す必要があり](https://ja.wikipedia.org/wiki/アプリケーションプログラミングインターフェイス "wikilink")、WPFを含む[.NET Framework 3.0以降をインストールしても](https://ja.wikipedia.org/wiki/.NET_Framework_3.0 "wikilink")、従来のアプリケーションやWindowsのインターフェイスは垂直方向のアンチエイリアスが有効とならないが、WPF 4は変更されてDirectWriteを用いる\[6\]。

### Windows Vista

Windows Vistaは、ビットマップを含まないフォントである[Segoe UIを](https://ja.wikipedia.org/wiki/Segoe_UI "wikilink")、日本語版は[メイリオ](https://ja.wikipedia.org/wiki/メイリオ "wikilink")をそれぞれ新たに採用し、[コントロールパネル](https://ja.wikipedia.org/wiki/コントロールパネル_\(Windows\) "wikilink")、[エクスプローラー](https://ja.wikipedia.org/wiki/Windows_Explorer "wikilink")、標準メッセージボックスなどインターフェイスの一部にClearTypeを使った文字を採用する。プロパティページなどの各種[ダイアログボックス](https://ja.wikipedia.org/wiki/ダイアログボックス "wikilink")はMS UI Gothicを用いるため、内蔵ビットマップが表示されてClearTypeは有効とならない。

### Windows 7

[Windows 7は](https://ja.wikipedia.org/wiki/Microsoft_Windows_7 "wikilink")、Windows Vista以前の[GDI](https://ja.wikipedia.org/wiki/Graphics_Device_Interface "wikilink")・[GDI+に代わる](https://ja.wikipedia.org/wiki/Graphics_Device_Interface#GDI+ "wikilink")[2DグラフィックスAPIとして](https://ja.wikipedia.org/wiki/2次元コンピュータグラフィックス "wikilink")[Direct2D](https://ja.wikipedia.org/wiki/Direct2D "wikilink")・DirectWriteが追加されている。テキスト描画に関するDirectWriteのClearTypeは、WPFと同様に垂直方向のアンチエイリアスが追加されたほか\[7\]\[8\]、文字間隔の最適化なども調整されて従来のClearTypeに対して「Natural ClearType」と称する\[9\]が、利用するためにWPFと同様にアプリケーションがDirectWriteの機能を呼び出す必要がある。Windows 7のインターフェイス（コモンコントロール）はGDIによる従来のClearTypeを用いるが、機能が向上した[ClearType Tunerを標準搭載する](https://ja.wikipedia.org/wiki/ClearType#ClearType_Tuner "wikilink")。Windows 7とWindows Vistaに提供される[Internet Explorer](../Page/Internet_Explorer.md "wikilink") 9は、[ウェブページの描画にGDIではなくDirect](https://ja.wikipedia.org/wiki/Webページ "wikilink")2D・DirectWriteを用いる。メイリオを元にした字幅が狭いフォントの[Meiryo UIを新たに標準搭載するが](https://ja.wikipedia.org/wiki/Meiryo_UI "wikilink")、MS UI Gothicを完全に置き換えるものではなくインターフェイスの一部に用いている。

### Windows 8

[Windows 8日本語版は](https://ja.wikipedia.org/wiki/Microsoft_Windows_8 "wikilink")、インターフェイスにこれまでMS UI Gothicを用いた部分もMeiryo UIを用い、全体の視認性やインターフェイスの統一感が向上している。Windows 8に標準搭載されてWindows 7にも提供されるInternet Explorer 10もインターフェイスにSegoe UIとMeiryo UIを使用している。

### Windows 10

[Windows 10日本語版は](https://ja.wikipedia.org/wiki/Microsoft_Windows_10 "wikilink")、ClearTypeの描画を前提にデザインされたフォントの[Yu Gothic UIを採用した](https://ja.wikipedia.org/wiki/游書体#游ゴシック体 "wikilink")。スタートメニューや設定アプリなどのテキスト描画は[グレースケール](https://ja.wikipedia.org/wiki/グレースケール "wikilink")[レンダリングで](https://ja.wikipedia.org/wiki/レンダリング_\(コンピュータ\) "wikilink")、描画品質が背景色に左右されるClearTypeのサブピクセルレンダリングは用いない。

## 短所

非常に小さなフォントサイズで、ビットマップフォントに比べて視認性が低下することがある。

GDIのClearTypeは、水平方向（X方向）のみをアンチエイリアス処理する。[ラテン文字](https://ja.wikipedia.org/wiki/ラテン文字 "wikilink")は、画数が少なく高さが揃っており垂直方向のアンチエイリアスを行わなくとも問題が少なく、斜線や曲線による造形が主であるため文字幅も狭くてイタリック表記も一般的など、水平方向のサブピクセルレンダリングの恩恵を受けやすく、緩やかな曲線の多い[ブラーフミー系文字](https://ja.wikipedia.org/wiki/ブラーフミー系文字 "wikilink")も親和性が高い。一方、漢字などの複雑な字体は、線分が接合、もしくは表示されないなどの問題を生じ、大きな[ポイント](https://ja.wikipedia.org/wiki/ポイント "wikilink")の文字はフォントの造型にかかわらず緩やかな曲線などで[ジャギー](https://ja.wikipedia.org/wiki/ジャギー "wikilink")が生ずる。WPFやDirectWriteのClearTypeは、垂直方向（Y方向）もアンチエイリアス処理する\[10\]\[11\]ために上記の問題は改善されている。漢字など複雑な字体は、CoolTypeなど「水平方向のサブピクセルレンダリング+垂直方向のアンチエイリアシング」を組み合わせるレンダリングの効果が高い。

Microsoft Office System 2007は、大きなポイントのフォントはClearTypeを使わずに標準アンチエイリアスをグレースケールモードで用いる。Office 2013はGDIに代わってDirectWriteを採用した\[12\]が、アンチエイリアスはグレースケールモードを用いる。

メイリオは膨大なヒンティング情報を格納することでデザイナーが意図する字形を表示するが、[アウトラインのジャギーや文字不均高などを生ずるフォントもあり](https://ja.wikipedia.org/wiki/フォント#アウトライン形式 "wikilink")、ClearTypeの奏功はフォントの造形や実装に左右される。

画面上の表示を前提としているため、[スクリーンショット](https://ja.wikipedia.org/wiki/スクリーンショット "wikilink")の印刷や、ディスプレイで拡大や縮小など設定と異なる解像度で表示する場合のほか、ディスプレイを回転して表示する場合もソフトウェアが対応していない限りサブピクセルの並びが逆になり、表示が不自然になる。

ClearTypeはサブピクセルレンダリングの特性から背景色に描画品質が左右され、透明な[DIB](../Page/Windows_bitmap.md "wikilink")[バッファ](https://ja.wikipedia.org/wiki/バッファ "wikilink")にClearTypeを適用してテキストを描画すると予期しない合成結果となることがある。WPFやDirect2Dは、アルファモードに応じて自動的にアンチエイリアス方式をグレースケールモードに変更して対処している\[13\]\[14\]\[15\]。

メイリオやSegoe UIなどClearTypeに最適化されたフォントを使用する場合、ClearTypeを無効にすると表示が淡くなり視認性が低下する\[16\]。

## ClearType Tuner

[マイクロソフト](../Page/マイクロソフト.md "wikilink")がWindows XP用に提供する[フリーウェア](../Page/フリーウェア.md "wikilink")で、文字の濃淡やR・G・Bの並び順をディスプレイに最適化するなど微調整を可能とする。インストールしてコントロールパネル内で表示するものと、[ActiveX](https://ja.wikipedia.org/wiki/ActiveX "wikilink")を利用して[ブラウザ](https://ja.wikipedia.org/wiki/ブラウザ "wikilink")で操作するものがあり、Windows Vista・[Windows Server](https://ja.wikipedia.org/wiki/Windows_Server "wikilink") 2003/2008でも使用できる。

Windows 7 以降はClearType テキストチューナーが標準搭載され、上記の機能に加えてサブピクセルの発色の微調整などより細かい設定が可能である。サブピクセル発色を使わず[モノクローム](../Page/モノクローム.md "wikilink")のスムージングも可能だが、縦方向のスムージングは行わず標準アンチエイリアスとは異なる。

## 脚注

## 関連項目

  - [メイリオ](https://ja.wikipedia.org/wiki/メイリオ "wikilink")

  - [DirectWrite](https://ja.wikipedia.org/wiki/DirectWrite "wikilink")

  - [アンチエイリアス](https://ja.wikipedia.org/wiki/アンチエイリアス "wikilink")

  - [サブピクセルレンダリング](https://ja.wikipedia.org/wiki/サブピクセルレンダリング "wikilink")

  - [FreeType](https://ja.wikipedia.org/wiki/FreeType "wikilink")

  -
  - [:en:Subpixel rendering](https://ja.wikipedia.org/wiki/:en:Subpixel_rendering "wikilink")

## 外部リンク

  - [What is ClearType? - Microsoft Typography](https://www.microsoft.com/typography/WhatIsClearType.mspx)
  - \[<https://msdn.microsoft.com/ja-jp/library/ms749295(v=vs.110>).aspx ClearType の概要 - Microsoft\]（WPFでのClearTypeについての説明）
  - [ClearType Tuner](http://www.microsoft.com/typography/cleartype/tuner/Step1.aspx)（ブラウザ版）

[Category:グラフィカルユーザインタフェース](https://ja.wikipedia.org/wiki/Category:グラフィカルユーザインタフェース "wikilink") [Category:書体](https://ja.wikipedia.org/wiki/Category:書体 "wikilink") [Category:Microsoft_Windows](https://ja.wikipedia.org/wiki/Category:Microsoft_Windows "wikilink")

1.
2.
3.
4.  [Windows XP 向け ClearType 対応日本語フォント](http://www.microsoft.com/downloads/details.aspx?FamilyID=f7d758d2-46ff-4c55-92f2-69ae834ac928&DisplayLang=ja) - マイクロソフト ダウンロード センター（[WGA認証が必要](https://ja.wikipedia.org/wiki/Windows_Genuine_Advantage "wikilink")）
5.
6.
7.
8.
9.
10.
11.
12.
13.
14.
15.
16.
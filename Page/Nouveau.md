> この記事は[Nouveau](https://ja.wikipedia.org/wiki/Nouveau)から翻訳されています。


[Gallium3D_vs_DRI_graphics_driver_model.svg](https://ja.wikipedia.org/wiki/File:Gallium3D_vs_DRI_graphics_driver_model.svg "fig:Gallium3D_vs_DRI_graphics_driver_model.svg") and [Gallium3D](https://ja.wikipedia.org/wiki/Gallium3D "wikilink") have different driver models. Both share a lot of [free and open-source](https://ja.wikipedia.org/wiki/free_and_open-source_software "wikilink") code\]\] [Linux_Graphics_Stack_2013.svg](https://ja.wikipedia.org/wiki/File:Linux_Graphics_Stack_2013.svg "fig:Linux_Graphics_Stack_2013.svg") graphics stack\]\] [Gallium3D_example_matrix.svg](https://ja.wikipedia.org/wiki/File:Gallium3D_example_matrix.svg "fig:Gallium3D_example_matrix.svg") **nouveau**（ヌーヴォー）は [X.Org Foundation](../Page/X.Org_Foundation.md "wikilink") と [freedesktop.org](https://ja.wikipedia.org/wiki/freedesktop.org "wikilink") のプロジェクトである。当初は、[フリーで](../Page/フリーソフトウェア.md "wikilink")[オープンソース](../Page/オープンソース.md "wikilink")ではあるが、[ソースコード](../Page/ソースコード.md "wikilink")がややこしく2D機能のみの "nv" ドライバーに基づくものだった。現在は [NVIDIA](https://ja.wikipedia.org/wiki/NVIDIA "wikilink") の[プロプライエタリな](../Page/プロプライエタリ・ソフトウェア.md "wikilink") Linux 用ドライバを[リバースエンジニアリング](https://ja.wikipedia.org/wiki/リバースエンジニアリング "wikilink")して、 [NVIDIA](https://ja.wikipedia.org/wiki/NVIDIA "wikilink") の[ビデオカード](../Page/ビデオカード.md "wikilink")用のフリーな[ドライバを開発することを狙いとしている](../Page/デバイスドライバ.md "wikilink")。

## 概要

[X.Org](../Page/X.Org_Server.md "wikilink") 用の他の3Dグラフィックスドライバのように、nouveau は[モジュール](https://ja.wikipedia.org/wiki/モジュール "wikilink")として実装され [MIT ライセンスのもとで配布されている](https://ja.wikipedia.org/wiki/MIT_License "wikilink")。元々は[3次元コンピュータグラフィックス](../Page/3次元コンピュータグラフィックス.md "wikilink")をレンダリングするために [Graphics Processing Unit](../Page/Graphics_Processing_Unit.md "wikilink") を使って3Dの描画を高速化する [Mesa 3D](../Page/Mesa_3D.md "wikilink") の[ダイレクト・レンダリング・インフラストラクチャ](https://ja.wikipedia.org/wiki/ダイレクト・レンダリング・インフラストラクチャ "wikilink") (DRI) を使っていたが、2008年2月に DRI への働き掛けをやめて新しい [Gallium3D](https://ja.wikipedia.org/wiki/Gallium3D "wikilink") に移行した\[1\]\[2\]。

## ツール

[リバースエンジニアリング](https://ja.wikipedia.org/wiki/リバースエンジニアリング "wikilink")のためプロジェクトでは mmio-trace や REnouveau のようないくつかの特別なツールを利用している。

### REnouveau

[right](https://ja.wikipedia.org/wiki/ファイル:Renouveau-screenshot-on-debian-with-kde.png "wikilink") REnouveau はほとんどのリバースエンジニアリングの作業を支えている。プロプライエタリな NVIDIA のドライバを持っているユーザは NVIDIA カードのハードウェア情報を提供することで nouveau の開発を助けることができる。これはコンピュータ上で REnouveau を動作させることによって行なわれる。REnouveau は現在のグラフィックカードの [MMIO](https://ja.wikipedia.org/wiki/メモリマップドI/O "wikilink") レジスタ空間をコピーし、グラフィックの一部を描画し MMIO のもう一つのコピーを取り、違いをテキストファイルに出力することにより動作する。コンピュータのユーザは REnouveau で70強の異なるテストを走らせ、[tar](https://ja.wikipedia.org/wiki/tar "wikilink").bz2 のアーカイブを作って[メールで送信する](../Page/電子メール.md "wikilink")。自動的に送信したアーカイブはプロジェクトの FTP サーバに送られ、開発者がそれを解析する。

REnouveau は [GPL](../Page/GNU_General_Public_License.md "wikilink") のもとで配布されており [SDL](../Page/SDL.md "wikilink") のレンダリング技術を基にしている。

## 脚注

## 外部リンク

  -
  - [REnouveau](http://nouveau.freedesktop.org/wiki/REnouveauDumps)

  - [nouveau の SourceForge プロジェクト](http://sourceforge.net/projects/nouveau)

[Category:デバイスドライバ](https://ja.wikipedia.org/wiki/Category:デバイスドライバ "wikilink") [Category:Freedesktop.org](https://ja.wikipedia.org/wiki/Category:Freedesktop.org "wikilink")

1.
2.
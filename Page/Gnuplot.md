> この記事は[Gnuplot](https://ja.wikipedia.org/wiki/Gnuplot)から翻訳されています。


[Gnuplot-in-action.png](https://ja.wikipedia.org/wiki/File:Gnuplot-in-action.png "fig:Gnuplot-in-action.png")

**gnuplot**（ニュープロット しばしばグニュープロットとも）は、2[次元](../Page/次元.md "wikilink")もしくは3次元の[グラフを作成するための](../Page/グラフ_\(関数\).md "wikilink")[アプリケーションソフトウェア](../Page/アプリケーションソフトウェア.md "wikilink")である。[インターネット](../Page/インターネット.md "wikilink")において無料で配布されている[フリーウェア](../Page/フリーウェア.md "wikilink")である。[1986年](../Page/1986年.md "wikilink")に最初のバージョンが開発された。現在では、[Linux](../Page/Linux.md "wikilink")、[UNIX](../Page/UNIX.md "wikilink")、[Windows](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")、[macOS](https://ja.wikipedia.org/wiki/macOS "wikilink")などの多くの[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink") (OS) に対応したバージョンが開発されている。

[オープンソースソフトウェア](../Page/オープンソースソフトウェア.md "wikilink")として公開されており、高機能・高精度であることから、特に学術研究に広く利用されている。また、使い方を解説したWebサイトも数多く存在する。過去には[GNU Octaveのプロットエンジンとしても利用されていた](../Page/GNU_Octave.md "wikilink")。

## 機能

入力したデータや[数式](../Page/数式.md "wikilink")等を元に、[画面](https://ja.wikipedia.org/wiki/画面 "wikilink")もしくは[画像](../Page/画像.md "wikilink")[ファイルへグラフを生成する](../Page/ファイル_\(コンピュータ\).md "wikilink")。画像ファイルの[フォーマットは](../Page/ファイルフォーマット.md "wikilink")、[PNG](../Page/Portable_Network_Graphics.md "wikilink"), [EPS](../Page/Encapsulated_PostScript.md "wikilink"), [SVG](https://ja.wikipedia.org/wiki/SVG "wikilink"), [JPEG](../Page/JPEG.md "wikilink")などの多くの形式に対応している。

用途によって[バッチファイル](../Page/バッチファイル.md "wikilink")としてまとめて処理を行わせる方式と、逐次[命令文](https://ja.wikipedia.org/wiki/命令文 "wikilink")を入力してグラフを描画させる方式とを使い分けることが出来る。

## 名称とライセンス

名前に「*gnu*」と冠されてこそいるが、[GNUプロジェクト](../Page/GNUプロジェクト.md "wikilink")とは関係がなく、独自の[ライセンス](../Page/ライセンス.md "wikilink")形態をとっている。

[ソースコード](../Page/ソースコード.md "wikilink")を[コピーないし改変することは許されているが](../Page/複写.md "wikilink")、改変を加えたバージョンの配布は[パッチ](../Page/パッチ.md "wikilink")形式でのみ可能である。したがって[GPLと互換性がない](../Page/GNU_General_Public_License.md "wikilink")。

## 使用例

[thumb](https://ja.wikipedia.org/wiki/ファイル:Logarithmic_spiral.png "wikilink") 使用したコマンドと結果として出力された画像を示す。

``` gnuplot
# Output to png file:
set terminal png small color
set output "logarithmic_spiral.png"

# Same scale for both axes, half-size output:
set size ratio -1 0.5, 0.5

# More sample points to produce smoother picture:
set samples 170

# Axes in the center, no tick marks:
set zeroaxis
set noxtics
set noytics
set noborder
set polar

# set title "Logarithmic spiral (pitch 10 degrees)"

plot [-4*pi:4*pi] [-8:10] [-8:6] 1.19**t notitle
```

## 関連ソフトウエア

gnuplotを対話的に使いやすくするためのGUIフロントエンドアプリケーションも以下のように多数存在する。

  - Cueplot
  - Xgfe
  - Qgfe
  - UnigPlot
  - RubyPlot
  - QPlot

## 外部リンク

  -

  - [gnuplot マニュアルの日本語訳](http://takeno.iee.niit.ac.jp/~foo/gp-jman/)

  - [mw:Extension:Gnuplot](https://ja.wikipedia.org/wiki/mw:Extension:Gnuplot "wikilink") - gnuplotを[MediaWiki](../Page/MediaWiki.md "wikilink")で使用するための[extension](https://ja.wikipedia.org/wiki/meta:MediaWiki_extensions "wikilink")

[Category:オープンソースソフトウェア](https://ja.wikipedia.org/wiki/Category:オープンソースソフトウェア "wikilink") [Category:グラフ作成ソフト](https://ja.wikipedia.org/wiki/Category:グラフ作成ソフト "wikilink")
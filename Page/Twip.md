> この記事は[Twip](https://ja.wikipedia.org/wiki/Twip)から翻訳されています。


**Twip**(s)（トゥイップ）とは、主に[マイクロソフト](../Page/マイクロソフト.md "wikilink")社の製品・技術で利用されている[長さの単位](../Page/長さの単位.md "wikilink")。

[Microsoft Visual Basic](https://ja.wikipedia.org/wiki/Microsoft_Visual_Basic "wikilink")、[Microsoft Visual C++](../Page/Microsoft_Visual_C++.md "wikilink")、[リッチテキストフォーマット](https://ja.wikipedia.org/wiki/リッチテキストフォーマット "wikilink")等において、ウインドウやレポートのサイズとして用いられる。

1Twipは1/20[ポイント](../Page/ポイント.md "wikilink")であり、1/1440[インチ](../Page/インチ.md "wikilink")に相当する。「**Tw**entieth of an **I**nch **P**oint」から、Twipと名づけられた。

[Microsoft Windowsの標準のシステム解像度である](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")96[dpi](https://ja.wikipedia.org/wiki/dpi "wikilink")の環境下では15Twipsで1[ピクセル](../Page/ピクセル.md "wikilink")、120dpiの環境下では12Twipsで1ピクセルの長さと等しい。

Visual Basic 1.0から6.0まで使われていたが、後継のVisual Basic .NET 2002以降ではピクセル単位での指定しかできなくなっている。

## 意義

[WYSIWYG](../Page/WYSIWYG.md "wikilink")の考え方では、画面上に表現される文字と印刷した文字の大きさは一致しているべきである。そのためにWindowsをはじめ多くのグラフィック環境では、使用しているディスプレイ装置の解像度（dpi値）をシステムに設定しておき、同じ大きさ（たとえば11ポイント）の文字でも、ディスプレイ装置の解像度に応じて異なるピクセル数で文字を表現することで、画面上の文字の実測サイズを印刷時のサイズと同じにできるように考えられている。

これは文書だけでなく、ソフトウェアの画面においても同じことが言え、解像度の異なるディスプレイ装置を使用した場合でも画面上に表現される文字やウインドウの大きさが同じになるよう調整することで、「高解像度のディスプレイではウインドウが小さすぎて使いにくい」などの問題を避けることができる。

これを実現しようとするとき、ウインドウの大きさをピクセル単位で設定していたのでは、画面の解像度をもとに必要なピクセル数を計算してセットしてやる必要があり、いささか面倒である。インチ、ポイント、ミリメートルなどの単位で指定し、システム側でピクセル値に変換することが望まれるが、ポイントやミリメートルなどより細かい指定ができるよう、1/1440インチ（約0.018ミリ）という細かな単位としてTwipが使われている。

[Category:グラフィカルユーザインタフェース](https://ja.wikipedia.org/wiki/Category:グラフィカルユーザインタフェース "wikilink") [Category:長さの単位](https://ja.wikipedia.org/wiki/Category:長さの単位 "wikilink") [Category:ヤード・ポンド法](https://ja.wikipedia.org/wiki/Category:ヤード・ポンド法 "wikilink")
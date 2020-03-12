> この記事は[Mission Control](https://ja.wikipedia.org/wiki/Mission_Control)から翻訳されています。


**Mission Control**（前身の**Exposé**（エクスポゼ）は、[Mac OS X v10.3](../Page/Mac_OS_X_v10.3.md "wikilink")(Panther)より導入）はOS X Lionにて導入された、デスクトップ上のウィンドウを一時的に整列する機能のこと。

他の[ウィンドウシステム](../Page/ウィンドウシステム.md "wikilink")でもウィンドウの並べ替えや最大・最小化といった機能は存在するが、Exposéではウィンドウが縮小表示されて一覧できる点や、モードの終了後にウィンドウが元の位置に戻る点が異なる。

## 機能の概要

Exposéには3つの整列モードがある。この3つのモードは、デフォルト設定ではファンクションキーに割り当てられているが、設定を変更することでカーソルを画面の角に持っていくことで発動させるようにしたり、マウスのボタンによって動作するようにできる。

1.  **全ウィンドウ整列**。動作中の全てのウィンドウが画面上に並べられる。デフォルトではF9キーに対応。実行中にtabキーを押すと、「アプリケーションウィンドウ整列」に切り替わる。
2.  **アプリケーションウィンドウ整列**。前面のアプリケーションが管理するウィンドウが、画面上に並べられる（他のアプリケーションのウィンドウは薄暗く表示される）。デフォルトではF10キーに対応。
3.  **デスクトップ表示**。全てのウィンドウが画面外に退避して[デスクトップ](https://ja.wikipedia.org/wiki/デスクトップ "wikilink")の全面表示になる。デフォルトではF11キーに対応。

全ウィンドウ整列とアプリケーションウィンドウ整列では、ウィンドウが適当な大きさに縮小されて、画面内に全てが収まるように調整される（この時ウィンドウが縮小表示されることになるが、Mac OS X v10.5までは元のウィンドウ同士の大きさの比率を損なわないようになっている。Mac OS X v10.6以降は元のウィンドウ同士の大きさの比率は無視されタイル状に整列されて表示される）。配置は、重心の位置などから自然な配置が計算される。その後特定のウィンドウをクリックするとそれが前面に出現し、ウィンドウが元の位置に戻される。

非常に派手な機能であるにも関わらず、動作は極めて高速で、[Quartz Extreme対象外の](https://ja.wikipedia.org/wiki/Quartz_Extreme "wikilink")[G3マシンでも快適に機能する](../Page/PowerPC.md "wikilink")。これはMac OS Xのウィンドウサーバの構造が、個々のウィンドウの描画内容を独立に計算した後、結果の集計を画面上に合成するという構造を取っているがゆえに、等倍表示であれ縮小表示であれ、負荷に大きな違いがないためである。

[Mac OS X v10.4](../Page/Mac_OS_X_v10.4.md "wikilink")(Tiger)では、[Dashboard](../Page/Dashboard.md "wikilink")が搭載されている。これはExposéを応用して設計されたものである。

## 関連項目

  - [ズーミングユーザインタフェース](https://ja.wikipedia.org/wiki/ズーミングユーザインタフェース "wikilink")

## 外部リンク

  - [Mac で Mission Control を使う](https://support.apple.com/ja-jp/HT204100)
  - [Mac ハンドブック：Exposé](http://support.apple.com/kb/HT2503?viewlocale=ja_JP&locale=ja_JP)

[Category:MacOS](https://ja.wikipedia.org/wiki/Category:MacOS "wikilink")
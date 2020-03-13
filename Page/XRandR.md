> この記事は[XRandR](https://ja.wikipedia.org/wiki/XRandR)から翻訳されています。


**XRandR**（エックス・アール・アンド・アール）は、[X Window System](../Page/X_Window_System.md "wikilink") を再起動せずに解像度の変更や、画面の回転、表示モニターの切替え、[マルチモニター](../Page/マルチモニター.md "wikilink")の設定など、を行うことを容易にする[ライブラリ](../Page/ライブラリ.md "wikilink")と[コマンドである](../Page/キャラクタユーザインタフェース.md "wikilink")。XRandRは、X Window System Resize and Rotate Extension を略したもの。

最初の [X11](../Page/X_Window_System.md "wikilink") の設計では動的なサイズ変更の要望を予想しておらず、変更を行うには [Xサーバを再起動する必要があった](../Page/X_Window_System.md "wikilink")。RandR 拡張[フレームワークによりXセッションの再起動なしでディスプレイの特徴を変えることができるようになった](../Page/アプリケーションフレームワーク.md "wikilink")。拡張フレームワークによって[ラップトップや手持ちサイズのコンピュータで](../Page/ラップトップパソコン.md "wikilink")、組込みのスクリーンではなく異なる[解像度](../Page/解像度.md "wikilink")の外部モニターを駆動するようにスクリーンサイズを変更できるようになる\[1\]。現在の[プロトコル](../Page/プロトコル.md "wikilink")仕様のバージョンは1.2である。

使っている[デスクトップ環境](https://ja.wikipedia.org/wiki/デスクトップ環境 "wikilink")がこの機能と相互作用するグラフィカルツールを提供していなくても、**xrandr** [コマンドラインツールが使える](../Page/キャラクタユーザインタフェース.md "wikilink")。

## コマンドの使用例

  - モニターと可能な設定の表示

> `xrandr`

  - 全てのモニターを最高解像度で、同じ画面を表示する。

> `xrandr --auto`

  - 内蔵モニターの右側に外部モニターを表示。モニターの名前は、上の xrandr で調べられる。ここでは 内部モニター：LVDS、外部モニター：VGA とする。

> `xrandr --output VGA --right-of LVDS`

  - 内蔵モニターの上側に外部モニターを表示。

> `xrandr --output VGA --above LVDS`

マルチモニターを使用する場合、X11の設定ファイル：通常 /etc/X11/xorg.conf で、仮想スクリーンの範囲を大きく取っておく。 例：

> `Virtual 2048 2048`

## 脚注

## 関連項目

  - [X Window System](../Page/X_Window_System.md "wikilink")

## 外部リンク

  - [X.org における XRandR プロジェクトページ](http://www.x.org/wiki/Projects/XRandR)
  - [XRandRの使用法の解説（英文）](http://wiki.debian.org/XStrikeForce/HowToRandR12)
  - [XRandRプロトコル仕様書](http://cgit.freedesktop.org/xorg/proto/randrproto/tree/randrproto.txt)

[Category:API](https://ja.wikipedia.org/wiki/Category:API "wikilink") [Category:X_Window_System](https://ja.wikipedia.org/wiki/Category:X_Window_System "wikilink")

1.  ["The X Resize and Rotate Extension"](http://keithp.com/~keithp/talks/randr/) (Jim Gettys and [Keith Packard](https://ja.wikipedia.org/wiki/キース・パッカード "wikilink"), Usenix Technical Conference 2001)
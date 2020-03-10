> この記事は[GNUstep](https://ja.wikipedia.org/wiki/GNUstep)から翻訳されています。


**GNUstep**（グニューステップ）は、[NeXT](../Page/NeXT.md "wikilink")の[OPENSTEP](../Page/OPENSTEP.md "wikilink") [Objective-C](../Page/Objective-C.md "wikilink") ライブラリ(フレームワーク)、[ウィジェット・ツールキット](https://ja.wikipedia.org/wiki/ウィジェット・ツールキット "wikilink")、アプリケーション開発ツール群を[フリーソフトウェア](../Page/フリーソフトウェア.md "wikilink")として実装したものである。[Unix系](../Page/Unix系.md "wikilink")[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink")だけでなく[Microsoft Windowsでも動作する](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")。[GNUプロジェクト](../Page/GNUプロジェクト.md "wikilink")の一部でもある。

GNUstepは、[NeXTのOPENSTEP仕様に完全互換なプラットフォームにまたがったオブジェクト指向開発環境を備えている](../Page/NEXTSTEP.md "wikilink")（NeXT社は[アップルコンピュータに買収された](../Page/アップル_\(企業\).md "wikilink")）。アップルと同様GNUstepは[Java](https://ja.wikipedia.org/wiki/Java "wikilink")インターフェイスを持ち、同時に[Ruby](../Page/Ruby.md "wikilink")\[1\]や[Scheme](../Page/Scheme.md "wikilink")とも接続できる。 GNUstepの[アプリケーション](../Page/アプリケーションソフトウェア.md "wikilink")[インタフェースは](../Page/インタフェース_\(情報技術\).md "wikilink")[macOS](https://ja.wikipedia.org/wiki/macOS "wikilink")の[Cocoa](../Page/Cocoa.md "wikilink")のインタフェースと根幹は同じ（NeXTとOPENSTEP）である。GNUstepの発祥はCocoaより先であった。

GNUstepはOPENSTEPの仕様を満たすことを目指して開発され、macOSが実装している[フレームワークの多くを欠いているが](https://ja.wikipedia.org/wiki/ソフトウェアフレームワーク "wikilink")、GNUstepの開発者は互換性を保つため、アップルのCocoaの追加機能に追随しようとしている。ただし、CocoaとGNUstepは[ABIが全く異なるため](../Page/Application_Binary_Interface.md "wikilink")、アプリケーションの[バイナリ](../Page/バイナリ.md "wikilink")レベルの互換性は期待できない。

## 歴史

GNUstepの開発が始まったのは、[スタンフォード線形加速器センターの](../Page/SLAC国立加速器研究所.md "wikilink") Paul Kunz らが[NEXTSTEP](../Page/NEXTSTEP.md "wikilink")の HippoDraw を他のプラットフォームに移植したいと考えたのがきっかけであった。HippoDrawを一から書き直してアプリケーションとしての設計だけを活用するのではなく、アプリケーションが依存しているNeXTSTEPの[オブジェクト層を書き換えようと考えた](../Page/オブジェクト指向.md "wikilink")。そしてできたのが最初の*libobjcX*である。これを使って彼らは HippoDraw を全く書き換えることなくUNIXシステムの[X Window System上に移植できた](../Page/X_Window_System.md "wikilink")。OPENSTEPの仕様が[1994年](../Page/1994年.md "wikilink")に公開されると、彼らは新たな[APIにも対応する](../Page/アプリケーションプログラミングインタフェース.md "wikilink")*objcX*を作ることを決めた。そのソフトウェアが"GNUstep"として知られるようになるのである。

## パラダイム

GNUstepはOPENSTEPと似ており、OPENSTEPの設計規則を継承するとともに[Objective-C](../Page/Objective-C.md "wikilink")言語を使っている。

  - [Model View Controller](../Page/Model_View_Controller.md "wikilink") パラダイム
  - Target-Action
  - [ドラッグ・アンド・ドロップ](../Page/ドラッグ・アンド・ドロップ.md "wikilink")
  - [委譲](../Page/委譲.md "wikilink")
  - (NSInvocationを通した)[メッセージ転送](../Page/メッセージ_\(コンピュータ\).md "wikilink")

## クラスの機能

### ファウンデーションキット

（デバイスに依存しないクラス群とプログラミング機能）

  - 文字列
  - 集合（配列、セット、辞書）と順序子 (enumerators)
  - ファイル管理
  - オブジェクト・アーカイブ
  - 拡張されたデータ操作
  - 分散オブジェクトとプロセス間通信
  - URL処理
  - 通知 (notifications) および分散通知
  - 簡単なマルチスレッド
  - タイマー
  - ロック
  - 例外処理

### アプリケーションキット

（GUI系クラスの集まり）

  - [ユーザインタフェース](../Page/ユーザインタフェース.md "wikilink")の要素(テーブルビュー、ブラウザ、マトリックス、スクロールビュー)
  - グラフィックス（[WYSIWYG](../Page/WYSIWYG.md "wikilink")、ポストスクリプト風グラフィックス、ベジェ曲線、イメージ処理、グラフィカル・コンテキスト）
  - カラー管理(較正色と物理色(CMYK,RGB,HSB)、グレイと名前付きカラー表現、アルファブレンディング)
  - テキスト：多様なテキストフォーマット、アタッチメント、レイアウトマネージャ、タイプセッター、ルール、段落スタイル、フォント管理、スペル
  - 文書管理
  - 印刷機能：印刷操作、印刷パネルとページレイアウト
  - ヘルプ管理
  - ペーストボード（[クリップボード](../Page/クリップボード.md "wikilink")のようなもの）
  - スペルチェッカー
  - アプリケーションのワークスペース束縛
  - ドラッグ・アンド・ドロップ操作
  - アプリケーション間の共通サービス

## 関連項目

  - [NEXTSTEP](../Page/NEXTSTEP.md "wikilink")
  - [OPENSTEP](../Page/OPENSTEP.md "wikilink")
  - [Window Maker](../Page/Window_Maker.md "wikilink")
  - [プロパティリスト](../Page/プロパティリスト.md "wikilink")([defaults](http://manpages.ubuntu.com/manpages/intrepid/man1/defaults.1.html))

## 脚注

<references />

## 外部リンク

  - [The GNUstep Project Homepage(英語)](http://www.GNUstep.org/)
  - [GNUstepはOpenStepの代替フリーソフトウェア](http://www.codereading.com/notebook/moin.cgi/GNUstep%E3%81%AFOpenStep%E3%81%AE%E4%BB%A3%E6%9B%BF%E3%83%95%E3%83%AA%E3%83%BC%E3%82%BD%E3%83%95%E3%83%88%E3%82%A6%E3%82%A7%E3%82%A2)

[Category:GNUプロジェクト](https://ja.wikipedia.org/wiki/Category:GNUプロジェクト "wikilink") [Category:デスクトップ環境](https://ja.wikipedia.org/wiki/Category:デスクトップ環境 "wikilink") [Category:オープンソースソフトウェア](https://ja.wikipedia.org/wiki/Category:オープンソースソフトウェア "wikilink") [Category:X_Window_System](https://ja.wikipedia.org/wiki/Category:X_Window_System "wikilink") [Category:MacOS](https://ja.wikipedia.org/wiki/Category:MacOS "wikilink") [Category:ウィジェット](https://ja.wikipedia.org/wiki/Category:ウィジェット "wikilink")

1.  <http://www.gnustep.org/experience/RIGS.html>
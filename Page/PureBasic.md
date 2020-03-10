> この記事は[PureBasic](https://ja.wikipedia.org/wiki/PureBasic)から翻訳されています。


**PureBasic**（**ピュアベーシック**）は、[Fantaisie Software](http://www.purebasic.com)製の商用の[BASIC](../Page/BASIC.md "wikilink")言語およびその[統合開発環境](../Page/統合開発環境.md "wikilink") (IDE) であり、[Microsoft Windows](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")（[32ビット](../Page/32ビット.md "wikilink")、[64ビット](https://ja.wikipedia.org/wiki/64ビット "wikilink")）、[Linux](../Page/Linux.md "wikilink")（32ビット、64ビット）、[macOS](https://ja.wikipedia.org/wiki/macOS "wikilink")で動作する。[AmigaOS](https://ja.wikipedia.org/wiki/AmigaOS "wikilink")版は開発中止となり、[オープンソース](../Page/オープンソース.md "wikilink")化されている。

## 概要

PureBasicは、標準のシステムライブラリの他に[ランタイムライブラリ](../Page/ランタイムライブラリ.md "wikilink")を要しない、非常にコンパクトな[実行ファイル](https://ja.wikipedia.org/wiki/実行ファイル "wikilink")や[DLLを生成する](../Page/ダイナミックリンクライブラリ.md "wikilink")。プラットフォーム特有の[APIを用いずに開発すれば](../Page/アプリケーションプログラミングインタフェース.md "wikilink")、複数のプラットフォームで同じソースファイルをほとんど、あるいはまったく修正することなく使用できる。

[インラインアセンブラ](https://ja.wikipedia.org/wiki/インラインアセンブラ "wikilink")に対応しているため、PureBasicで宣言した[変数を用いてPureBasicのソースコード中で](https://ja.wikipedia.org/wiki/変数_\(プログラミング\) "wikilink")[FASM](https://ja.wikipedia.org/wiki/FASM "wikilink")のコマンドを扱うことが可能である。したがって、高速な動作が求められる場合には、プログラマの能力次第で速度を追求することができる。

1000以上のネイティブなコマンドが用意されている他、OSの大半のAPIに直接アクセス可能である。エディタはプロジェクト管理を完全サポートしている。[コンパイラ](../Page/コンパイラ.md "wikilink")は[スレッドセーフ](https://ja.wikipedia.org/wiki/スレッドセーフ "wikilink")に対応し、[ブレークポイント](https://ja.wikipedia.org/wiki/ブレークポイント "wikilink")をサポートする強力な[デバッガ](../Page/デバッガ.md "wikilink")を持つ。このデバッガは、ステップモード、変数ビューア／ウォッチャなど、BASIC言語の主要製品に共通したデバッグ機能を備えている。また、PureBasicは[OGRE 3Dを統合している](https://ja.wikipedia.org/wiki/OGRE "wikilink")。[Irrlichtなど](https://ja.wikipedia.org/wiki/Irrlicht_Engine "wikilink")、他の3Dエンジンにも非公式ではあるが対応している。

## デモ版

デモ版は無料でデバッグ機能をOFFにしたコンパイルが出来ない、ソースコードの行数が限られる等の機能制限はあるが、試用期限はない。代金を支払うとユーザー登録され、製品版をダウンロードできるようになる。そのため、広義の[シェアウェア](../Page/シェアウェア.md "wikilink")に分類される。

ユーザー登録すると、どのプラットフォーム向けのPureBasicもすべて自由に使用できる。商用使用も自由である。また、以後のバージョンアップは無料であることが宣言されている。

## [Hello worldの例](../Page/Hello_world.md "wikilink")

[コンソール](https://ja.wikipedia.org/wiki/コンソール "wikilink")画面に表示

`OpenConsole()`
`PrintN("こんにちは世界")`

PureBasicのコマンドで[ダイアログボックス](../Page/ダイアログボックス.md "wikilink")に表示

`MessageRequester("サンプル", "こんにちは世界")`

インラインで[Windows APIを用いてダイアログボックスに表示](https://ja.wikipedia.org/wiki/Windows_API "wikilink")

`MessageBox_(0, "こんにちは世界", "サンプル", 0)`

ウィンドウに表示

`If OpenWindow(0, 0, 0, 150, 50, "サンプル")`
`  TextGadget(0, 40, 15, 100, 20, "こんにちは世界")`
`  Repeat : Until WaitWindowEvent() = #PB_Event_CloseWindow`
`EndIf`

## リリース状況

AmigaOS版は、使用者の減少に伴い、2002年2月23日のVer.2.90リリースを最後に暫くバージョンアップされていなかった。2006年末にVer.4.00がリリースされたが、今後の継続的なバージョンアップは困難であることが予想され、実質的に開発とサポートを続けられる手段としてオープンソース化された。これはAmigaOS版だけの限定措置である。

Windows版、Linux版、Mac OS X版については、Ver.4.10以降一斉リリースとなっており、今後もその方針である。

| 製品バージョン        | OS       | リリース年月日     | 備考                   |
| -------------- | -------- | ----------- | -------------------- |
| PureBasic 1.60 | AmigaOS  | 2000年9月9日   |                      |
| PureBasic 2.00 | Windows  | 2000年12月17日 | Windows版初回リリース       |
| PureBasic 2.00 | AmigaOS  | 2001年1月18日  |                      |
| PureBasic 2.32 | Linux    | 2001年7月8日   | Linux版初回リリース（プレビュー版） |
| PureBasic 2.90 | AmigaOS  | 2002年2月23日  |                      |
| PureBasic 3.00 | Windows  | 2002年4月4日   |                      |
| PureBasic 3.30 | Linux    | 2002年9月22日  |                      |
| PureBasic 3.94 | Mac OS X | 2005年10月5日  | Mac OS X版初回リリース      |
| PureBasic 4.00 | Windows  | 2006年5月8日   |                      |
| PureBasic 4.00 | AmigaOS  | 2006年12月10日 | オープンソース化             |
| PureBasic 4.00 | Linux    | 2007年4月15日  |                      |
| PureBasic 4.10 | 全OS      | 2007年11月9日  | 最初の全OS一斉リリース         |
| PureBasic 4.20 | 全OS      | 2008年5月23日  |                      |
| PureBasic 4.30 | 全OS      | 2008年12月16日 |                      |
| PureBasic 4.40 | 全OS      | 2009年12月1日  |                      |
| PureBasic 4.41 | 全OS      | 2010年2月1日   |                      |
| PureBasic 4.50 | 全OS      | 2010年6月7日   |                      |
| PureBasic 4.51 | 全OS      | 2010年9月8日   |                      |
| PureBasic 4.60 | 全OS      | 2011年11月7日  |                      |
| PureBasic 5.00 | 全OS      | 2012年11月5日  |                      |
| PureBasic 5.31 | 全OS      | 2014年10月27日 |                      |
| PureBasic 5.60 | 全OS      | 2017年3月2日   |                      |

主なリリースの履歴

## 関連項目

  - [BASIC](../Page/BASIC.md "wikilink")

[Category:BASIC](https://ja.wikipedia.org/wiki/Category:BASIC "wikilink")
> この記事は[Vi](https://ja.wikipedia.org/wiki/Vi)から翻訳されています。


**vi**（ヴィーアイ）は、[Emacs](../Page/Emacs.md "wikilink")と共に[UNIX](../Page/UNIX.md "wikilink")環境で人気がある[テキストエディタ](../Page/テキストエディタ.md "wikilink")。[ビル・ジョイ](https://ja.wikipedia.org/wiki/ビル・ジョイ "wikilink")によって開発された。名の由来は**VI**sual editorないし**V**isual **I**nterfaceとされる\[1\]\[2\]。後発の[Unix系](https://ja.wikipedia.org/wiki/Unix系 "wikilink")OSに搭載されているviは、上位互換の[Vim](https://ja.wikipedia.org/wiki/Vim "wikilink")や[nvi](https://ja.wikipedia.org/wiki/nvi "wikilink")であることが多い（viコマンドでvimやnviが起動する）。

## 創始

[BSD](https://ja.wikipedia.org/wiki/BSD "wikilink")の創始者である[ビル・ジョイ](https://ja.wikipedia.org/wiki/ビル・ジョイ "wikilink")が、最初のBSDを公開するにあたり開発していた[Pascal](../Page/Pascal.md "wikilink")[コンパイラ](../Page/コンパイラ.md "wikilink")を快適に作成するために開発したのが始まりである。当初はそのPascalの[ソースコード](../Page/ソースコード.md "wikilink")に同封され、その奥底に埋もれていたため、単体のソフトウェアとしての提供は認知されていなかった。この段階ではexと呼ばれる[ラインエディタ](https://ja.wikipedia.org/wiki/ラインエディタ "wikilink")であり、まだ現在のような[スクリーンエディタではなかった](../Page/テキストエディタ.md "wikilink")。

後に[カリフォルニア大学バークレイ校](https://ja.wikipedia.org/wiki/カリフォルニア大学バークレイ校 "wikilink")にLear Siegler [ADM3A](https://ja.wikipedia.org/wiki/ADM3A "wikilink")端末装置が導入されたのを機に、ビル・ジョイ自身により更なる改良を加えられたものが、現在のviと呼ばれるエディタである。

## 特徴

### 他のテキストエディタと異なる点

  - マウスを使わない（viの開発当時、マウスは発明されていたが普及していなかった）
  - カーソルキーを使わない（開発端末である[ADM3A](https://ja.wikipedia.org/wiki/ADM3A "wikilink")には、専用のカーソルキーが設けられていなかった\[3\]）
  - 命令を覚える必要がある（画面上に命令表示領域が無い）

このような特徴は一見欠点にも見えるが、慣れにより素早いカーソルの移動や編集操作ができ、作業効率が上がるようになる。また、マウスカーソルやカーソルキーの使用を強制していないため、それらが利用できないハードウェア上でも利用することが出来る。（Vimのようなviクローンの中にはGUIや[IBM-PCの一般化により](https://ja.wikipedia.org/wiki/PC/AT互換機 "wikilink")、使用できるものも存在する。）

### 設計思想

viはラインエディタのexを祖先に持ち、多くの特徴を受け継いでいる。

ラインエディタでは、目的の行を抽出、編集、更新というサイクルで編集を行う。現在主流のスクリーンエディタと異なり、内容の閲覧/編集はそれぞれ独立した機能であり、インタラクト（対話的）に動作しない。しかしそれだけでは利用が困難なので、exでは「特定のパターンにマッチする行内で内容を置換」「外部コマンドによるフィルタ」などのプログラム[インタプリタ](../Page/インタプリタ.md "wikilink")的な支援機能が充実している（[sedは同様の背景をルールマッチ型に](../Page/Sed_\(コンピュータ\).md "wikilink")[解釈](../Page/解釈.md "wikilink")した[フィルタ記述インタプリタである](https://ja.wikipedia.org/wiki/フィルタ_\(ソフトウェア\) "wikilink")）。

viはexのスーパーセットであり、閲覧・抽出に相当する部分をフルスクリーン/インタラクトに拡張して独立の移動コマンド体系を与えたものである。従って分類上はスクリーンエディタに含まれるが、設計思想はビュワーを伴うラインエディタに近い。

そのような背景から、特にWYSIWYGに慣れたユーザーに対して戸惑いを与えるユニークさが多い。有名なのは、初期状態で、打鍵した文字がテキストとして入力されるのではなく、編集コマンドとして解釈される点である。この理由で「viはモードを持つエディタ」と呼ばれる場合が多い。

### exコマンド

viはexのスーパーセットなので、exの編集機能はすべてviでも使用できる。これをexコマンドと呼び、コマンドモードで **:** に続いて入力されるものが当たる。

例えばファイルを保存する **:w** やエディタを終了する **:q** など、編集の[メタ](https://ja.wikipedia.org/wiki/メタ "wikilink")レベルに関わるもの、特定の行番号や正規表現にマッチする行アドレスに対して編集を行うもの、上記のマクロ機能などが含まれる。

（厳密にはiやaなどのインサートモードへ移行するコマンドもexコマンドの略記と見なされる）

### その他の特徴

viはコンパクトで負荷が小さいため、作業中にテキストファイルの一部を書き換えたり、通信速度の遅いネットワークの先にあるマシンで編集したりといった作業に向いている。 また、コンパクトで負荷が小さいという利点から、最低限のUNIX環境でも含まれている事が多く、スマートフォン、無線LANルータ、液晶テレビなど、コアシステムとしてLinuxを採用しているハードウェアの多くにviもしくはvi互換のエディタが搭載されている。

## vi互換エディタ

[PC-UNIX](https://ja.wikipedia.org/wiki/PC-UNIX "wikilink")においては現在はオリジナルのviが使われることはあまり一般的ではなく、模倣して作られたvi互換エディタ（クローン）の利用が一般的である。一般的なディストリビューションではviのシンボリックリンクがviの本来のパスに置かれ、互換エディタにリンクしている。また、[オープンソース](../Page/オープンソース.md "wikilink")プロジェクトによる開発が多いため、UNIXの1つであるmacOS、AndroidなどのLinuxはもとより、本来互換性のない独自環境である[MS-DOS](../Page/MS-DOS.md "wikilink")や[Windowsといった他のプラットフォーム上で実行可能な互換エディタも存在する](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")。

  - [nvi](https://ja.wikipedia.org/wiki/nvi "wikilink"): nex/nviは、[4.4BSDにおいてex](https://ja.wikipedia.org/wiki/BSD "wikilink")/viの代替として[カリフォルニア大学バークレー校](https://ja.wikipedia.org/wiki/カリフォルニア大学バークレー校 "wikilink")がオリジナルに配布した。[BSDライセンス](https://ja.wikipedia.org/wiki/BSDライセンス "wikilink")で提供され本家viの動作とのバグも含めた互換性がある。
  - [Vim](https://ja.wikipedia.org/wiki/Vim "wikilink"): viを改善した、高度にさまざまな設定が可能なエディタ。多くの[Linux](https://ja.wikipedia.org/wiki/Linux "wikilink")[ディストリビューション](https://ja.wikipedia.org/wiki/ディストリビューション "wikilink")や[macOS](https://ja.wikipedia.org/wiki/macOS "wikilink")に標準搭載されており、その場合のviコマンドはVimのviモードへのシンボリックリンクになっている。
  - [elvis](https://ja.wikipedia.org/wiki/elvis "wikilink"): Steve Kirkendallにより書かれた強力なex/viクローン。
  - [ViVi](https://ja.wikipedia.org/wiki/ViVi_\(エディタ\) "wikilink"): viコマンドをサポートするWindows用エディタ
  - WinVi: Windows用の軽量なviエディタ。(同名の海外作者版もあるが、それとは別の国産エディタ)
  - POSIX標準: viはその原型であるexと共にPOSIXで標準化されている<ref name="posix"> - viの手引き (POSIX標準)


 - exの手引き (POSIX標準)</ref>。

## 関連項目

  - [ビル・ジョイ](https://ja.wikipedia.org/wiki/ビル・ジョイ "wikilink")
  - [エディタ戦争](https://ja.wikipedia.org/wiki/エディタ戦争 "wikilink")
  - [テキストエディタ](../Page/テキストエディタ.md "wikilink")
  - [Vim](https://ja.wikipedia.org/wiki/Vim "wikilink")
  - [nvi](https://ja.wikipedia.org/wiki/nvi "wikilink")

## 脚注

## 参考文献

  - [Linda Lamb](https://ja.wikipedia.org/wiki/リンダ・ラム "wikilink")、[Arnold Robbins](https://ja.wikipedia.org/wiki/アーノルド・ロビンス "wikilink")『[入門 vi 第6版](https://www.oreilly.co.jp/books/4873110831/)』[福崎俊博](https://ja.wikipedia.org/wiki/福崎俊博 "wikilink")訳、[オライリー・ジャパン](https://ja.wikipedia.org/wiki/オライリー・ジャパン "wikilink")、2002年5月、ISBN 4-87311-083-1
  - [Arnold Robbins](https://ja.wikipedia.org/wiki/アーノルド・ロビンス "wikilink")『[viデスクトップリファレンス](https://www.oreilly.co.jp/books/490090094X/)』[日本ルーセント・テクノロジー株式会社](https://ja.wikipedia.org/wiki/日本ルーセント・テクノロジー株式会社 "wikilink")訳、[オライリー・ジャパン](https://ja.wikipedia.org/wiki/オライリー・ジャパン "wikilink")、1999年6月、ISBN 4-900900-94-X

## 外部リンク

  -
  - [Vi Lovers Home Page](https://thomer.com/vi/vi.html)

  - [viを使い倒そう](http://archive.linux.or.jp/JF/JFdocs/vi-user-usage.html)（[テキスト版](http://archive.linux.or.jp/JF/JFdocs/vi-user-usage.txt)）テキストエディタ vi の使い方の簡単な解説書

[Category:オープンソースソフトウェア](https://ja.wikipedia.org/wiki/Category:オープンソースソフトウェア "wikilink") [Category:テキストエディタ](https://ja.wikipedia.org/wiki/Category:テキストエディタ "wikilink") [Category:UNIXのソフトウェア](https://ja.wikipedia.org/wiki/Category:UNIXのソフトウェア "wikilink") [Category:1976年のソフトウェア](https://ja.wikipedia.org/wiki/Category:1976年のソフトウェア "wikilink")

1.  大木敦雄監修 小島範幸・北浦訓行著 『はじめてのvi\&Vim』 [技術評論社](https://ja.wikipedia.org/wiki/技術評論社 "wikilink")、2009年、23頁。「viの名前の由来は、VIsual Editorです。」
2.   - [ジャーゴンファイル](../Page/ジャーゴンファイル.md "wikilink")のviの項で \[from ‘Visual Interface’\] と明記されている。
3.  、 および [キーボードレイアウト図](https://ja.wikipedia.org/wiki/:File:KB_Terminal_ADM3A.svg "wikilink") - ADM3Aのキーh、j、k、lの上に、カーソルを示す刻印が設けられている。
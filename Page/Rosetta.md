> この記事は[Rosetta](https://ja.wikipedia.org/wiki/Rosetta)から翻訳されています。


**Rosetta**（ロゼッタ）は、[Mac OS Xの基盤技術の一つ](https://ja.wikipedia.org/wiki/macOS "wikilink")。[インテル](https://ja.wikipedia.org/wiki/インテル "wikilink")アーキテクチャへの移行に伴い、[PowerPC](../Page/PowerPC.md "wikilink")バイナリの互換性を維持するために、PowerPC用プログラムコードをインテル用コードに適宜変換する措置 (dynamic recompilation) を行なう。アップルの発注を受け[仮想化ミドルウエア開発で実績のある米](../Page/仮想機械.md "wikilink")[Transitiveの技術が導入された](https://ja.wikipedia.org/wiki/トランジティブ "wikilink")\[1\]。

インテルアーキテクチャ向けに対応した[v10.4 "Tiger"で初めて搭載されたものの](../Page/Mac_OS_X_v10.4.md "wikilink")、[v10.6 "Snow Leopard"ではインストールが任意化](../Page/Mac_OS_X_v10.6.md "wikilink")\[2\]及び最後の対応となり、[v10.7 "Lion"で廃止された](https://ja.wikipedia.org/wiki/Mac_OS_X_Lion "wikilink")\[3\]。

## 仕組みとパフォーマンス

どの程度のサイズのバイナリコードが変換されるかは動的に変化する（[キャッシュメモリ](../Page/キャッシュメモリ.md "wikilink")と同じような概念で、必要なプログラムコードを任意の容量読み込んだ上でx86コードに変換するため、逐一命令を変換する[エミュレータとはいささか趣を異にする](../Page/エミュレータ_\(コンピュータ\).md "wikilink")）。アプリケーションのコード全体をインテル用コードに変換してから実行する機能はない。[ユニバーサルバイナリ](https://ja.wikipedia.org/wiki/ユニバーサルバイナリ "wikilink")対応のソフトでは自動的にインテル用コードが実行される。

Rosetta環境下で実行されるPowerPCバイナリはx86コードへと変換され、ユーザー側からはCPU種別を意識することなくアプリケーションを実行できる。ただし、前述の動作方法ゆえに速度の低下は避けられず、シングルコアG5より高速と言われるIntel Core Duoで同クロックのG4の50～80%以下の速度になる(メモリ容量や周辺ハードウェアの違いに左右されるため一概には言えない)といわれている。当初RosettaはG3互換の環境とされていたが、実際には[AltiVec](../Page/AltiVec.md "wikilink")に対応したG4互換の環境として出荷された。G5ネイティブのコードについては最後までサポートされなかった。

Rosettaを利用した場合、たとえ最新の[Core i7でも](https://ja.wikipedia.org/wiki/Intel_Core_i7 "wikilink")、PowerPC時代のPower Macと比べても性能はそれほど伸びない。PowerPCアプリケーションのほぼ全てが[エンディアン](https://ja.wikipedia.org/wiki/エンディアン "wikilink")をビッグエンディアンに揃えていて、それをIntelシステム上で動くコードに置き換えるとき、リトルエンディアンへのバイトスワップとアライメント調整を行うコードを大量に出力してしまうのが最大の原因と言われている。メモリの読み書きはCPUにとって基本的な機能であり、そこに足かせがつけられてしまうのはアプリケーション性能に重大な影響を与えてしまう。逆を言えばバイトスワップが発生しないバイトオーダーの処理がメインのアプリケーションでは非常に優れたパフォーマンスを発揮し得る。しかしそのようなソフトウエアは少なく、例えば画像処理など基本的にバイトオーダーで処理するソフトウエアでもワードアクセスした後バンドル処理を行うといったチューニングが施されているため、Rosettaの上で動かそうとすると裏目に出る結果となる。

なお、Rosettaは[Classic環境をサポートせず](https://ja.wikipedia.org/wiki/Classic_\(ソフトウェア\) "wikilink")、スクリーンセーバやシステム環境設定など、非アプリケーションのバイナリも実行できない。PowerPCコードとx86コードの混在した[プロセス](../Page/プロセス.md "wikilink")も処理できず、[アプリケーションソフトウェア](../Page/アプリケーションソフトウェア.md "wikilink")のPowerPC対応プラグインを使用するには、アプリケーション全体をRosettaで起動しなくてはならない（なお、[Dashboard](https://ja.wikipedia.org/wiki/Dashboard "wikilink")ウィジェットは[ダイナミックHTML](../Page/ダイナミックHTML.md "wikilink")ベースであるため、CPUの違いの影響を受けない）。この点はMixed Mode Managerにより[68kコードとPowerPCコードの混在したプロセスを処理可能としていた](../Page/MC68000.md "wikilink")[Mac OSのコード変換機構と異なり](https://ja.wikipedia.org/wiki/Mac_OS "wikilink")、注意が必要である。

## 脚注

<references />

[Category:アップルのソフトウェア](https://ja.wikipedia.org/wiki/Category:アップルのソフトウェア "wikilink")

1.  [86系に乗り換えるApple社の秘策，「Rosetta」の概要が明らかに](http://techon.nikkeibp.co.jp/article/NEWS/20050610/105646/)
2.  [話題のユキヒョウを追う「Snow Leopard、ココに注目」(3) - 互換性の謎を解く](https://news.mynavi.jp/articles/2009/09/03/macosx_snowleopard/)
3.  [新機能のポイントをチェック\! アップル「OS X Lion」速攻レビュー(後編)](https://news.mynavi.jp/articles/2011/07/27/lion02/002.html)
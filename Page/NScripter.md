> この記事は[NScripter](https://ja.wikipedia.org/wiki/NScripter)から翻訳されています。


**NScripter**（エヌスクリプター）は、[高橋直樹が開発](https://ja.wikipedia.org/wiki/高橋直樹_\(シナリオライター\) "wikilink")・公開している[スクリプトエンジンである](../Page/スクリプトエンジン_\(ゲーム\).md "wikilink")。動作環境は[Windows](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")。**N**は作者の「直樹」から取られた。高橋の手による**Scripter3** がその前身にあたる。後継エンジンとして、[2009年](../Page/2009年.md "wikilink")12月より[NScripter2](https://ja.wikipedia.org/wiki/NScripter2 "wikilink")の公開が始まっている。

Windows以外の[プラットフォームで動作する](../Page/プラットフォーム_\(コンピューティング\).md "wikilink")、非公式の互換エンジンが公開されている。

## 概要

Windows環境上で動作するスクリプトエンジンである。特に[アドベンチャーゲーム](../Page/アドベンチャーゲーム.md "wikilink")や[ビジュアルノベル](../Page/ビジュアルノベル.md "wikilink")といった、テキスト表現を主体とするゲームの実行を得意とする。文法の平易さと高度な演出能力に加え、広範な利用実績によるエンジンの信頼性や安定性も、高く評価されている。

また、開発コンセプトとして、専属[プログラマ](../Page/プログラマ.md "wikilink")の存在しない中小零細ソフトハウスにおいても、[ゲームシナリオライター](https://ja.wikipedia.org/wiki/ゲームシナリオライター "wikilink")自らが[演出](../Page/演出.md "wikilink")およびスクリプティングを担当し、[ゲーム制作が可能となる事が挙げられている](../Page/パソコンゲーム.md "wikilink")。

[商用](https://ja.wikipedia.org/wiki/市販ソフトウェア "wikilink")・[同人を問わず](../Page/同人ソフト.md "wikilink")、テキストを主体としたゲーム作品のエンジンとして、[日本](https://ja.wikipedia.org/wiki/日本 "wikilink")で広く利用されていた。[2009年](../Page/2009年.md "wikilink")4月公開のVer2.93より[DLLによる機能追加が行われ](../Page/ダイナミックリンクライブラリ.md "wikilink")、[スクリプト言語](../Page/スクリプト言語.md "wikilink")[Lua](../Page/Lua.md "wikilink")を使用してエンジンの[フレームワークの振る舞いをユーザーが自由に改変可能な柔軟性が取り入れられている](https://ja.wikipedia.org/wiki/ソフトウェアフレームワーク "wikilink")。

2009年9月公開のVer2.95が[Windows 98](../Page/Microsoft_Windows_98.md "wikilink")/[me](../Page/Microsoft_Windows_Millennium_Edition.md "wikilink")/[2000対応最終版で](../Page/Microsoft_Windows_2000.md "wikilink")、[2011年](../Page/2011年.md "wikilink")12月公開のVer2.96以降は[Windows XP以降専用となった](../Page/Microsoft_Windows_XP.md "wikilink")。なお、NScripterの全てのバージョンにセキュリティ問題が存在するため、[2015年](../Page/2015年.md "wikilink")8月に[脆弱性に対応したVer](../Page/セキュリティホール.md "wikilink")3.00が\[1\]、同年9月には[バグ](../Page/バグ.md "wikilink")フィックス版の3.03が公開されている。

### 特徴

[スクリプト](../Page/スクリプト.md "wikilink")はエンジンにより[インタプリタ](../Page/インタプリタ.md "wikilink")で実行される。文法は、[BASIC](../Page/BASIC.md "wikilink")に似たもので非常に平易。[テキスト](../Page/テキスト.md "wikilink")や[CGの表示と演出](../Page/コンピュータグラフィックス.md "wikilink")、音楽の演奏、選択肢の処理など、アドベンチャーゲームの製作に必要な機能は、基本[APIとしてエンジンに組み込まれている](../Page/アプリケーションプログラミングインタフェース.md "wikilink")。このため、それらを呼び出すスクリプトを記述するだけで、高度な[アドベンチャーゲーム](../Page/アドベンチャーゲーム.md "wikilink")を構築できる。

また、システムカスタマイズと呼ばれる方法で、独自仕様の[セーブ](../Page/セーブ_\(コンピュータ\).md "wikilink")・ロード機能の実装や、基本APIには用意されていない複雑な演出の実行、といったエンジンの振る舞いそのものを変更する手段も用意されている。[ムービー](../Page/ムービー.md "wikilink")の再生、[スプライト等を利用した演出処理](../Page/スプライト_\(映像技術\).md "wikilink")、外部DLLによる機能拡張等も可能。これらの機能を応用し、[シミュレーション](../Page/シミュレーション.md "wikilink")タイプのゲーム等を製作する事も可能となっている。

反面、Ver2.92以前は[オブジェクト指向](../Page/オブジェクト指向.md "wikilink")的な要素は取り入れられておらず、各種[タスク](https://ja.wikipedia.org/wiki/タスク "wikilink")の同時並行進行のような処理は苦手としていた。[構造化プログラミング](../Page/構造化プログラミング.md "wikilink")については、defsub命令を用意する事によって、擬似的にこれを実現している。全体として、テキストを主体としたアドベンチャーゲームを、平易に効率良く開発する事に特化した仕様となっている。

### Luaによる拡張

2009年4月にリリースされたVer2.93から、スクリプト言語Luaを使用したフレームワークの拡張が可能となっている。LuaはDLLの形で実装され、NScripter本体から起動される。従来のNScripterスクリプトからLuaの機能を呼び出す事はもちろん、Lua側からNScripterの機能を呼び出す事によって、ゲーム本体の記述をほぼ完全にLuaに移行させる事も出来る。従来のNScripterでは不可能だった複雑な数値演算に加え、[ファイル操作](../Page/ファイル_\(コンピュータ\).md "wikilink")、[ブロック](../Page/ブロック_\(プログラミング\).md "wikilink")・[スコープ](../Page/スコープ.md "wikilink")、テーブル・メソッド、モジュール・ライブラリ等、本格的なスクリプト言語の機能を利用した開発が可能となっている。これまでは不可能だった、ゲーム内の各要素の同時並行操作が可能となり、テキスト表示のスプライト化処理が可能になるなど演出と機能が大幅に強化されている。また、システムカスタマイズと呼ばれる方法を用いて実現していた、様々な拡張機能の記述がLuaにより大幅に高度化・簡素化され、ゲーム終了時の挙動の変更などフレームワークの動作その物を改変できる柔軟性が取り入れられている。ただしLuaの使用は強制ではなく、旧来のシステムカスタマイズによる方法も残されている。

### 利用環境

PC中級者以上の知識があれば、有志により運営される各種講座サイトを利用する事によって、数時間程度で基本的な使用方法を習得する事ができる。また、ゲームの製作方法を解説した各種の公式書籍も出版されている。ユーザー製作の機能拡張用DLLやサンプルスクリプトも多数公開されており、利用環境は充実している。

反面、エンジンの利用そのものを指南するオフィシャルサイトは存在しない。また、エンジン本体に同梱されているマニュアルも、各種機能拡張の結果、かなり複雑な物となっている。このため利用に当たっては、ユーザー自身が積極的な情報収集に努める必要がある。

公式サイトでは最新版実行ファイルとは別に「NScripterドキュメント / 旧ツール」が配布されている。最新版の同梱マニュアルは、機能拡張に伴い内容が未整備な状態にあるため、新規利用にあたっては別途「NScripterドキュメント / 旧ツール」もダウンロードしておく必要がある。

### ライセンス

ライセンスについては、非商業用途での利用、及び同人流通作品なら無料で使用できる。

[2013年](../Page/2013年.md "wikilink")に使用条件が簡略化され、ゲーム・その他の[コンテスト](https://ja.wikipedia.org/wiki/コンテスト "wikilink")に応募した場合は入賞賞金の有無や入賞作品の流通形態に関わらず、無料で使用できるようになった。また、無料配布であれば[法人](../Page/法人.md "wikilink")・[個人](../Page/個人.md "wikilink")の区別や配布方法を問わずに無料で使用できる。[雑誌](../Page/雑誌.md "wikilink")の[付録](https://ja.wikipedia.org/wiki/付録 "wikilink")に[フリーウェア](../Page/フリーウェア.md "wikilink")・[シェアウェア](../Page/シェアウェア.md "wikilink")として収録する場合についても、無料となった。

ただし、商業流通作品として販売する場合は、使用料を支払う必要がある。同人やフリーソフトの場合でも、使用料を支払えば商用扱いとして**「サポート対象」**となる。その際、小規模の機能追加（独自の機能拡張や作品個別の暗号化処理など）であれば、使用料の範疇で対応する。

## 非公式の互換エンジン

NScripterはWindows上でしか動作しないが、非公式ながら他のプラットフォームでも動作する互換エンジンが開発されている。それらを使用すればNScripterを使用したゲームをWindows以外で動作させることが可能になる。

また、[吉里吉里2](../Page/吉里吉里2.md "wikilink")などの他のスクリプトエンジンを使用したゲームをNScripterで動作するように変換するソフトウェアも存在する。これは、Windowsでしか動作しないスクリプトエンジンから互換エンジンが存在するNScripterへ変換することで、Windows以外のプラットフォームでゲームを動作させることを意図したものが多い。ただし、変換するとオリジナルであった一部の特殊効果等が失われてしまうことがある。変換に使用したソフトウェアがその特殊効果を再現する所まで対応しきれていないためである。

以下に具体的な互換エンジンを挙げる。

### ONScripter

[PDA](../Page/携帯情報端末.md "wikilink")、[ゲーム機](../Page/ゲーム機.md "wikilink")などを含め、多くのプラットフォームに対応する。[オープンソース](../Page/オープンソース.md "wikilink")で開発されている。独自のセーブファイルを出力するが、NScripterと互換性のあるセーブファイルを扱うことも出来る\[2\]。

  - [Windows](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")
  - [Linux](../Page/Linux.md "wikilink")（含 [Android](../Page/Android.md "wikilink")）
  - [Zaurus](../Page/ザウルス.md "wikilink")
  - [NetWalker](https://ja.wikipedia.org/wiki/NetWalker "wikilink") (Ubuntu, Linux)
  - [macOS](https://ja.wikipedia.org/wiki/macOS "wikilink")
  - [Classic Mac OS](../Page/Classic_Mac_OS.md "wikilink")
  - [iOS](https://ja.wikipedia.org/wiki/iOS_\(アップル\) "wikilink") ([iPhone](https://ja.wikipedia.org/wiki/iPhone "wikilink"), [iPod touch](https://ja.wikipedia.org/wiki/iPod_touch "wikilink"), [iPad](https://ja.wikipedia.org/wiki/iPad "wikilink"))
  - [iPod](https://ja.wikipedia.org/wiki/iPod "wikilink")（[iPodLinux](https://ja.wikipedia.org/wiki/iPodLinux "wikilink")導入済みのもの）
  - [FreeBSD](../Page/FreeBSD.md "wikilink")
  - [Solaris](../Page/Solaris.md "wikilink")
  - [OS/2](https://ja.wikipedia.org/wiki/OS/2 "wikilink")
  - [Brain (電子辞書)](https://ja.wikipedia.org/wiki/Brain_\(電子辞書\) "wikilink")
  - [Dreamcast](../Page/ドリームキャスト.md "wikilink")
  - [プレイステーション3](https://ja.wikipedia.org/wiki/PlayStation_3 "wikilink")
  - [PSP](../Page/PlayStation_Portable.md "wikilink")
  - [Wii](https://ja.wikipedia.org/wiki/Wii "wikilink")
  - [PNaCl](https://ja.wikipedia.org/wiki/Google_Native_Client "wikilink")(Chrome Apps)\[3\]\[4\]

### CCScripter

[Mac OS Xで動作する互換エンジンとして開発されていたが](https://ja.wikipedia.org/wiki/macOS "wikilink")、2004年に公開されたバージョンを最後に更新・サポートが終了している\[5\]。代替として、上記のONScripterを使用することができる。

### NscPlayer

[Google Chromeで動作する](https://ja.wikipedia.org/wiki/Google_Chrome "wikilink")。PNaCL ONScripterが元になっている。

### PNaCL ONScripter

## 関連書籍

  - NScripterオフィシャルガイド\[6\]
      - 著：畔田英明、森皿尚行 / 監修：高橋直樹 / 発行：[秀和システム](../Page/秀和システム.md "wikilink") / 2004年9月11日発売 / ISBN 4-7980-0867-2
  - あどばんすどNScripterオフィシャルガイド\[7\]
      - 著：畔田英明、森皿尚行 / 監修：高橋直樹 / 発行：秀和システム / 2005年7月9日発売 / ISBN 4-7980-1104-5
  - 改訂版NScripterオフィシャルガイド\[8\]
      - 著：畔田英明、森皿尚行 / 監修：高橋直樹 / 発行：秀和システム / 2007年12月21日発売 / ISBN 978-4-7980-1852-2
  - NScripterではじめる ノベルゲーム制作\[9\]
  - 著：高橋直樹、桂ともえ、下地和彦、株式会社ユニゾン / イラスト：桂ともえ / 発行：[新紀元社](../Page/新紀元社.md "wikilink") / 2006年9月1日発売 / ISBN 4-7753-0496-8

## 関連項目

  - [吉里吉里2](../Page/吉里吉里2.md "wikilink")

## 脚注

## 外部リンク

  - [nscripter.com](http://www.nscripter.com/)（公式[サイト](../Page/ウェブサイト.md "wikilink")）
  - [高橋直樹の仕事と日常の日記](https://ntakahashi-work.hatenadiary.org/) Nscripterの最新版及びβ版、更新状況など

[Category:アドベンチャーゲーム](https://ja.wikipedia.org/wiki/Category:アドベンチャーゲーム "wikilink") [Category:ゲームエンジン](https://ja.wikipedia.org/wiki/Category:ゲームエンジン "wikilink") [Category:コンピュータゲーム制作ソフト](https://ja.wikipedia.org/wiki/Category:コンピュータゲーム制作ソフト "wikilink")

1.  [旧バージョンNScripterのセキュリティ問題について](http://www.nscripter.com/201508doc.html)、nscripter.com
2.
3.
4.
5.
6.
7.
8.
9.
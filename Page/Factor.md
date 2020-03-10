> この記事は[Factor](https://ja.wikipedia.org/wiki/Factor)から翻訳されています。


**Factor** は、動的型付けの連鎖性（concatenative）[プログラミング言語](../Page/プログラミング言語.md "wikilink")であり、が設計と実装を行った。Factor に影響を与えた言語として、、[Forth](../Page/Forth.md "wikilink")、[LISP](https://ja.wikipedia.org/wiki/LISP "wikilink")、[Self](../Page/Self.md "wikilink") がある。2014年11月現在の最新バージョンは 0.97。

## 概要

他の連鎖性言語と同様、Factor も[逆ポーランド記法](../Page/逆ポーランド記法.md "wikilink")構文であり、[関数の名前を書く前にその引数を記述する](https://ja.wikipedia.org/wiki/サブルーチン "wikilink")。例えば、Factor での [Hello world](../Page/Hello_world.md "wikilink") は次のようになる。

``` factor
 "Hello world" print
```

Factor は[動的型付けであり](https://ja.wikipedia.org/wiki/型システム "wikilink")、そこにユニークな[オブジェクトシステムが伴っている](../Page/オブジェクト指向プログラミング.md "wikilink")。Factor の[プリミティブ型](../Page/プリミティブ型.md "wikilink")は数少なく、ユーザーや標準ライブラリでは[タプル](https://ja.wikipedia.org/wiki/タプル "wikilink")などの機構を使って独自のクラスを作成できる。[継承はサポートされていないが](https://ja.wikipedia.org/wiki/継承_\(プログラミング\) "wikilink")、Self のような[委譲](https://ja.wikipedia.org/wiki/委譲 "wikilink")がサポートされている。また、型やタプル以外の[クラスを作る方法もあり](../Page/クラス_\(コンピュータ\).md "wikilink")、述語（predicate）クラスや共用体（union）クラスがサポートされている。Factor の組み込み複合データ型としては、固定長および可変長の[配列](../Page/配列.md "wikilink")と[ハッシュテーブル](../Page/ハッシュテーブル.md "wikilink")がある。[浮動小数点数](../Page/浮動小数点数.md "wikilink")もサポートされていて、任意長の整数もある。[連結リスト](../Page/連結リスト.md "wikilink")、[複素数](../Page/複素数.md "wikilink")、[分数](../Page/分数.md "wikilink")は標準ライブラリで実装されている。

当初は[インタプリタ](../Page/インタプリタ.md "wikilink")だけだったが、現在では完全な[コンパイラ](../Page/コンパイラ.md "wikilink")がある（非最適化コンパイラは、基本的にインタプリタのループを展開しただけのものである\[1\]\[2\]）。最適化された機械語を生成するコンパイラは全てFactorで書かれている。実行ファイル形式の出力はせず、[Smalltalk](../Page/Smalltalk.md "wikilink")のようなイメージファイルとして[機械語](../Page/機械語.md "wikilink")コードをセーブする。このイメージファイルを実行するための最小限の機能（VMなど）を持つ配布ツールと共に配布する。

スタックシステムでは不十分な場合のために、[静的スコープ](https://ja.wikipedia.org/wiki/静的スコープ "wikilink")と[動的スコープ](https://ja.wikipedia.org/wiki/動的スコープ "wikilink")もサポートされている。Factorには様々なライブラリがあり、[ボキャブラリ](https://ja.wikipedia.org/wiki/モジュール "wikilink")、[継続](https://ja.wikipedia.org/wiki/継続 "wikilink")、[HTTPサーバとWebフレームワーク](../Page/Webサーバ.md "wikilink")、[OpenGL](../Page/OpenGL.md "wikilink")[バインディング](https://ja.wikipedia.org/wiki/束縛_\(情報工学\) "wikilink")、[GUIライブラリ](https://ja.wikipedia.org/wiki/グラフィカルユーザインタフェース "wikilink")、[XMLパーサ](../Page/Extensible_Markup_Language.md "wikilink")、などがある。

Factor は対話型の[テスト駆動開発](https://ja.wikipedia.org/wiki/テスト駆動開発 "wikilink")に適した言語となることも目標としており、そのためにFactorは根本的にはForthの安全なバージョンとなっている。動的型付けだが、コンパイラはスタックの深さをコンパイル時に把握している。

## LISP的機能

Factor は[LISP](https://ja.wikipedia.org/wiki/LISP "wikilink")の機能も数多く採り入れている。同図像性（homoiconicity）構文、[ガベージコレクション](../Page/ガベージコレクション.md "wikilink")、[高階関数](https://ja.wikipedia.org/wiki/高階関数 "wikilink")、コンパイル時評価、read-eval-printループ、treeshaker などである。

ただし、表面的な見た目は逆ポーランド記法であるため、LISPとは逆に見える。つまり関数呼び出しの入れ子は、LISPの場合外側の関数が前に記されるが、Factorでは逆に後になる。これは、連鎖性言語であることの本質的性質である。

## 処理系

これまで、[Java](https://ja.wikipedia.org/wiki/Java "wikilink")による実装と[C言語](../Page/C言語.md "wikilink")による実装がされている。ただし、Javaによる実装はあまり使われず、既に保守されていない。C言語版は、徐々に[セルフホスティング](../Page/セルフホスティング.md "wikilink")によって Factor に置き換えられつつあり、C言語で書かれた部分は少なくなっている。

Factor はC言語のような標準仕様は存在しないが、言語仕様文書は豊富である。

## 脚注

## 外部リンク

  - [Factorの誕生](http://tech.groups.yahoo.com/group/concatenative/message/1756)
  - [Factor公式サイト](http://factorcode.org/)
      - [日本語訳(あしたのオープンソース研究所)](http://oss.infoscience.co.jp/factor/factorcode.org/)
  - [Factorメーリングリスト](https://lists.sourceforge.net/lists/listinfo/factor-talk)
  - [Logs of \#concatenative](http://www.ircbrowse.com/cdates.html?channel=concatenative) 主に Factor について議論するための[IRCチャンネル](https://ja.wikipedia.org/wiki/インターネット・リレー・チャット "wikilink")。[freenode](https://ja.wikipedia.org/wiki/freenode "wikilink")にある。
  - [Factor文書](http://factorcode.org/responder/help/)
  - [planet-factor](http://planet.factorcode.org/) [フィードリーダー](https://ja.wikipedia.org/wiki/フィードリーダー "wikilink")

[Category:プログラミング言語](https://ja.wikipedia.org/wiki/Category:プログラミング言語 "wikilink")

1.  [Two-tier compilation comes to Factor](http://factor-language.blogspot.com/2007/09/two-tier-compilation-comes-to-factor.html) 2007年9月10日
2.  [Compiler overhaul](http://factor-language.blogspot.com/2008/01/compiler-overhaul.html) 2008年1月8日
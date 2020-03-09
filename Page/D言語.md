> この記事は[D](https://ja.wikipedia.org/wiki/D)から翻訳されています。


**D言語**（ディーげんご、**D programming language**）は、プログラミング言語のひとつ。[C言語](../Page/C言語.md "wikilink")をベースとし[ABI互換を保ちつつも](https://ja.wikipedia.org/wiki/Application_Binary_Interface "wikilink")、[テンプレートによる](https://ja.wikipedia.org/wiki/テンプレート_\(プログラミング\) "wikilink")[ジェネリックプログラミング](https://ja.wikipedia.org/wiki/ジェネリックプログラミング "wikilink")や[オブジェクト指向](../Page/オブジェクト指向.md "wikilink")プログラミング、[関数型プログラミング](https://ja.wikipedia.org/wiki/関数型プログラミング "wikilink")などをサポートする[マルチパラダイムプログラミング言語](https://ja.wikipedia.org/wiki/マルチパラダイムプログラミング言語 "wikilink")である。

## 概要

[型推論](https://ja.wikipedia.org/wiki/型推論 "wikilink")や[ガベージコレクション](../Page/ガベージコレクション.md "wikilink")（明示的なメモリ管理も可能である）、スライスが可能な動的（および静的）[配列](../Page/配列.md "wikilink")、[連想配列](../Page/連想配列.md "wikilink")など効率的なプログラミングを可能にする言語機能を備えている。[単体テスト](https://ja.wikipedia.org/wiki/単体テスト "wikilink")、事前・事後条件のチェックや[不変条件](https://ja.wikipedia.org/wiki/不変条件 "wikilink")のチェック（[契約プログラミング](https://ja.wikipedia.org/wiki/契約プログラミング "wikilink")）、debug 識別子の導入など、プログラムのデバッグ・保守に対しても重点的にサポートしている。並列処理との親和性も重視しており、明示しない限りグローバル変数が[スレッド局所記憶](https://ja.wikipedia.org/wiki/スレッド局所記憶 "wikilink")であり、不変なデータ型（[イミュータブル](https://ja.wikipedia.org/wiki/イミュータブル "wikilink")）がサポートされている。また、標準ライブラリであるPhobosにも[メッセージパッシング等を用いた並列](https://ja.wikipedia.org/wiki/メッセージ_\(コンピュータ\) "wikilink")（および並行）処理が実装されている。

[C++](../Page/C++.md "wikilink")のような[テンプレートや](https://ja.wikipedia.org/wiki/テンプレート_\(プログラミング\) "wikilink")[メタプログラミング](https://ja.wikipedia.org/wiki/メタプログラミング "wikilink")機構を備えているが、テンプレート構文が簡潔な形に再設計されているなどの違いがある。コンパイル時関数実行を備えていることも特徴である。

D言語は[システムプログラミング言語としての側面も持つ](https://ja.wikipedia.org/wiki/システムソフトウェア#システムプログラミング "wikilink")。分かりやすいコードが高速かつ安全に動作するという言語設計を目指しているが、一方でパフォーマンスが要求される箇所では、[インラインアセンブラ](https://ja.wikipedia.org/wiki/インラインアセンブラ "wikilink")や[ポインタ演算などを利用できる](https://ja.wikipedia.org/wiki/ポインタ_\(プログラミング\) "wikilink")。これらの機能や、危険な[型変換](https://ja.wikipedia.org/wiki/型変換 "wikilink")などを用いたコードは関数の属性によって安全なコードと分離されるようになっている（関数の属性には、この他にも純粋な関数を示すものなどがある）。

## コード例

  - Hello, world\!

<!-- end list -->

``` D
import std.stdio;  // モジュールを読み込む

void main()  // プログラムのエントリーポイントは C と同じ main
{
    writeln("Hello, world!");

    // void main() 関数から抜けると適切な終了コードが返る
}
```

  - 引数の和

<!-- end list -->

``` D
import std.stdio, std.conv : to;

void main(string[] args)  // D の配列は要素数の情報を持っている
{
    int sum;              // 値型はコンパイラにより 0 で初期化される
    foreach(arg; args[1..$])  // 変数 arg は型推論により string 型になる
    {                         // 配列のスライシングも組込みでサポートされる
        sum += to!(int)(arg);  // to はテンプレート関数
    }
    writeln(sum);
}
```

[高階関数](https://ja.wikipedia.org/wiki/高階関数 "wikilink")を用いて書く事も可能である。標準ライブラリに含まれるmap, reduce関数を利用する例を示す。

``` D
import std.algorithm;
import std.conv;
import std.stdio;

void main(string[] args)
{
    writeln(args[1 .. $].map!(to!int).reduce!((a, b) => a + b));
}
```

## 特徴的な言語機能

### 統一関数呼び出し構文(Uniform Function Call Syntax, UFCS)

オブジェクト指向におけるメソッド呼び出しと同じ構文でフリー関数（グローバルレベルで宣言された関数）を呼び出すことができる機能。 関数の左側に置かれた値が第1引数として評価され、一般に「メソッドチェイン」と呼ばれる記述を可能にする。

[プログラミング言語Nimにも同様の言語機能が存在する](https://ja.wikipedia.org/wiki/Nim "wikilink")。

``` D
import std.stdio;

void main()
{
    // 以下の2つは同じ結果となる
    writeln(square(square(2))); // 8
    2.square().square().writeln(); // 8
}

// 引数を二乗して返す関数
int square(int n)
{
    return n * n;
}
```

## 歴史

  - [1999年](../Page/1999年.md "wikilink")12月 - ウォルター・ブライトが考案。
  - [2001年](../Page/2001年.md "wikilink")12月 - 初期バージョンがリリースされる。
  - [2007年](https://ja.wikipedia.org/wiki/2007年 "wikilink")1月 - バージョン1.0リリース。
  - [2007年](https://ja.wikipedia.org/wiki/2007年 "wikilink")6月 - バージョン2の開発が開始される。
  - [2007年](https://ja.wikipedia.org/wiki/2007年 "wikilink")8月 - D言語の第1回国際カンファレンス\[[http://d.puremagic.com/conference2007/\]がアメリカ合衆国のシアトルで開催された](http://d.puremagic.com/conference2007/%5Dがアメリカ合衆国のシアトルで開催された)。
  - [2012年](../Page/2012年.md "wikilink")12月 - バージョン1.0の最終リリース (1.076)。
  - [2013年](../Page/2013年.md "wikilink")5月 - DConf2013\[[http://dconf.org/2013/\]がシリコンバレーのFacebook社屋を借りて開催された。以後、場所を変えつつ年1度開催されている](http://dconf.org/2013/%5DがシリコンバレーのFacebook社屋を借りて開催された。以後、場所を変えつつ年1度開催されている)。
  - [2015年](../Page/2015年.md "wikilink") - 米国ワシントン州にてD言語財団設立。
  - [2015年](../Page/2015年.md "wikilink") - DMDのフロントエンド部の実装がC++からD言語に置換えられた。(2.069)
  - [2017年](../Page/2017年.md "wikilink") - DMD実装のコード共用箇所の権利問題が解決し、オープンソース(Boost Software License)になった。[1](https://mag.osdn.jp/17/04/11/170000)
  - [2018年](../Page/2018年.md "wikilink")5月 - [GNUコンパイラコレクション](../Page/GNUコンパイラコレクション.md "wikilink")のバージョン9.1からD言語がサポートされるようになった。(2.076相当)[2](https://mag.osdn.jp/19/05/08/163000)

### D1とD2

D1は、機能的には成熟したとされ、メンテナンスモードに移行している。標準ライブラリの非力さを補うため[Tango](http://www.dsource.org/projects/tango)ライブラリとセットで利用されることが多い。なお、D1は2012年いっぱいでのサポート停止がアナウンスされた。

当初D2は、新しい機能を積極的に取り込むための開発系バージョンとして分離された。標準ライブラリPhobosが強化され、また言語仕様の面では文字列型 (string) が変更不可能な配列となり、スレッド局所変数がデフォルトとなったなど、言語機能のさまざまな変更\[1\]が行われ、D1の上位互換ではない。互換性より言語やライブラリの改良を重視し、言語機能やライブラリの破壊的変更が頻繁に起きるのも特徴の一つであった。現在では、推奨されない、あるいは廃止される機能としてコンパイル時に警告が表示され、また公式ドキュメントなどで事前に告知されるようになっている\[2\]。

## 開発ツール

デバッガはC言語やC++と同じobjectフォーマットを使用するためCやC++用に書かれたものが使える。GDBなど、D言語に対するサポートを含んでいるものもある。既存の[開発ツールについては以下のページが詳しい](https://ja.wikipedia.org/wiki/プログラミングツール "wikilink")。

<https://wiki.dlang.org/IDEs> <https://wiki.dlang.org/Editors>

  - Visual D[3](http://rainers.github.io/visuald/visuald/StartPage.html)

<!-- end list -->

  -
    [マイクロソフト](../Page/マイクロソフト.md "wikilink")の[統合開発環境](../Page/統合開発環境.md "wikilink")[Visual Studio向けのプラグイン](https://ja.wikipedia.org/wiki/Microsoft_Visual_Studio "wikilink")。無償利用可能なVisual Studio Shellにも対応。

## 脚注

## 関連項目

  - [ABA Games](https://ja.wikipedia.org/wiki/ABA_Games "wikilink") - D言語を使用したゲーム開発で有名
  - [Eclipse](../Page/Eclipse_\(統合開発環境\).md "wikilink") - プラグインを利用することでD言語の開発環境として利用できる
  - [Code::Blocks](https://ja.wikipedia.org/wiki/Code::Blocks "wikilink") - D言語開発環境としても利用可能

## 外部リンク

  - [D Programming Language](https://dlang.org/index.html) - D言語公式ウェブサイト
  - [プログラミング言語 D](http://www.kmonos.net/alang/d/) - 上記サイトの日本語訳。公式ウェブサイトは頻繁に更新されているが、こちらは長らく更新されておらず情報が古いため注意が必要である。
  - [GDC - D Programming Language for GCC](http://gdcproject.org/) - [GCC版Dコンパイラ](../Page/GNUコンパイラコレクション.md "wikilink")
  - [LDC](https://wiki.dlang.org/LDC) - [LLVM](https://ja.wikipedia.org/wiki/LLVM "wikilink")を使用するDコンパイラ

### ライブラリ

  - [DUB registry](https://code.dlang.org/) - 公式のパッケージマネージャDUBで使用可能なパッケージの一覧

### リソース

  - [D Wiki](https://wiki.dlang.org/) - 公式Wiki
  - [わかったつもりになるD言語](http://www.kmonos.net/alang/wnd/)（通称わなD。D memoの2007年版）
  - [C/C++に疲れた人のD言語2.0](http://rayerd.plala.jp/pukiwiki/ingwiki/index.php?C%2FC%2B%2B%E3%81%AB%E7%96%B2%E3%82%8C%E3%81%9F%E4%BA%BA%E3%81%AED%E8%A8%80%E8%AA%9E2.0)
  - [D言語の四方山話](http://hp.vector.co.jp/authors/VA028375/d/)
  - [D言語入門](http://wisdom.sakura.ne.jp/programming/d/index.html)
  - [D language site](http://shinh.skr.jp/d/)

### その他

  - [Walter Bright's Homepage](http://www.walterbright.com/)

[Category:プログラミング言語](https://ja.wikipedia.org/wiki/Category:プログラミング言語 "wikilink")

1.  [D 2.0 の 1.0 からの違い - プログラミング言語 D 2.0](http://www.kmonos.net/alang/d/2.0/features2.html)
2.  [Deprecated Features](https://dlang.org/deprecate.html)
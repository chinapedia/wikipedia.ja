> この記事は[ActiveBasic](https://ja.wikipedia.org/wiki/ActiveBasic)から翻訳されています。


**ActiveBasic**（**アクティブ ベーシック**、*AB*）は、[1999年](../Page/1999年.md "wikilink")に[N88-BASIC](../Page/N88-BASIC.md "wikilink")互換の[インタプリタ言語](https://ja.wikipedia.org/wiki/インタプリタ言語 "wikilink")として、山本大祐が個人で開発した[BASIC](../Page/BASIC.md "wikilink")言語である。近年のBASIC派生の言語である[Visual Basic等とは別に独自の進化を遂げてきた](https://ja.wikipedia.org/wiki/Microsoft_Visual_Basic "wikilink")。

[2002年](../Page/2002年.md "wikilink")に登場したバージョン2.5からは、[RADツールを搭載](https://ja.wikipedia.org/wiki/RAD_\(計算機プログラミング環境\) "wikilink")。[2003年](../Page/2003年.md "wikilink")のバージョン3.0からは、ネイティブ[コンパイラ](../Page/コンパイラ.md "wikilink")を搭載し[インタプリタ](../Page/インタプリタ.md "wikilink")方式からコンパイラ方式に変わるなど、年々より本格的な仕様になってきている。また、ActiveBasicは[フリーウェア](../Page/フリーウェア.md "wikilink")である。[2005年](../Page/2005年.md "wikilink")、[DirectX](https://ja.wikipedia.org/wiki/DirectX "wikilink")や[オブジェクト指向](../Page/オブジェクト指向.md "wikilink")に対応したバージョン4.0が公開された。

また作者は、バージョン5.0で64ビット[コンパイラ](../Page/コンパイラ.md "wikilink")を搭載し、[Windows Vistaへの完全対応をアナウンスしていたが](https://ja.wikipedia.org/wiki/Microsoft_Windows_Vista "wikilink")、その[コンパイラ](../Page/コンパイラ.md "wikilink")の公開を前倒しし、バージョン4.20から64ビットコンパイラが搭載された。（32ビットコンパイラが無くなったわけではない）

[2008年](https://ja.wikipedia.org/wiki/2008年 "wikilink")7月以降、バージョンアップは行われていない。

## 特徴

### 言語仕様

基本的にバージョン3以降は[C言語](../Page/C言語.md "wikilink")や、バージョン4になってくると[C++](../Page/C++.md "wikilink")そして[Java](https://ja.wikipedia.org/wiki/Java "wikilink")などの影響を強く受けている。具体的には、従来のBASICに見られない機能として次のようなものがある。

  - [ポインタ](../Page/ポインタ_\(プログラミング\).md "wikilink") : 特にポインタ演算や関数へのポインタの存在。[malloc/free関数やNew](https://ja.wikipedia.org/wiki/標準Cライブラリ#一般ユーティリティ_\<stdlib.h\> "wikilink")/Delete演算子も存在する。
    [クラス](../Page/クラス_\(コンピュータ\).md "wikilink") : 特にバージョン5からは[単一継承及び](../Page/継承_\(プログラミング\).md "wikilink")[インタフェースの多重継承という](../Page/インタフェース_\(情報技術\).md "wikilink")[Java](https://ja.wikipedia.org/wiki/Java "wikilink")に近い仕組みが搭載されるとアナウンスされている。
    /\* 〜 \*/による[ブロックコメント](../Page/コメント_\(コンピュータ\).md "wikilink") : **'** （シングルクォーテーション）による1行コメントは無くなっていないが、バージョン3からREMは廃止された。
    [プリプロセッサ](../Page/プリプロセッサ.md "wikilink") : ただし条件コンパイルなどが中心でマクロ置換はない。
    [ガベージコレクション](../Page/ガベージコレクション.md "wikilink") : 評価版であるAB5 CP3より保守的GCが搭載された。

なお、現在、評価版としてActiveBasic 5.0 Customer Preview 5 (AB5 CP5)が公開されている。

### [Hello world](../Page/Hello_world.md "wikilink")

`#prompt`
`Print "Hello, world"`

\#promptはN88BASIC風の画面へのテキストの読み書きとグラフィックスを使用する指定である。（\#N88BASICとしても同じである）なお、\#consoleを指定するとWindowsコンソールアプリケーションを作成できる。その場合はグラフィックス機能は使えない。

`MessageBox(0, "Hello, world", "Hello", MB_OK)`

こちらはWindows APIを用いたものである。\#promptなどを指定しなければWindowsアプリケーションとなり、特に指定すべきことはない。

## 開発史

  - [1999年](../Page/1999年.md "wikilink") - バージョン1.0

<!-- end list -->

  -
    前身VersatileBasicの後継
    [N88-BASIC](../Page/N88-BASIC.md "wikilink")互換のインタプリタ言語として登場。

<!-- end list -->

  - [2000年](../Page/2000年.md "wikilink") - バージョン1.5

<!-- end list -->

  -
    [中間言語](../Page/中間言語.md "wikilink")コンパイラを搭載。

<!-- end list -->

  - [2001年](../Page/2001年.md "wikilink") - バージョン2.0

<!-- end list -->

  -
    [構造化プログラミング](../Page/構造化プログラミング.md "wikilink")に対応。

<!-- end list -->

  - [2002年](../Page/2002年.md "wikilink") - バージョン2.5

<!-- end list -->

  -
    RADツールを搭載、[Win32 APIに一部対応](https://ja.wikipedia.org/wiki/Win32_API "wikilink")。

<!-- end list -->

  - [2003年](../Page/2003年.md "wikilink") - バージョン3.0

<!-- end list -->

  -
    ネイティブコンパイラを搭載し[コンパイラ](../Page/コンパイラ.md "wikilink")言語となる。Win32 APIに完全対応。

<!-- end list -->

  - [2005年](../Page/2005年.md "wikilink") - バージョン4.0リリース。[オブジェクト指向](../Page/オブジェクト指向.md "wikilink")・[DirectX](https://ja.wikipedia.org/wiki/DirectX "wikilink")・[COM](../Page/Component_Object_Model.md "wikilink")・64ビット整数型に対応。

<!-- end list -->

  -
    コード補完機能を搭載。

<!-- end list -->

  - [2006年](../Page/2006年.md "wikilink") - バージョン4.2リリース。64ビットコンパイラの搭載。

<!-- end list -->

  - [2008年](https://ja.wikipedia.org/wiki/2008年 "wikilink") - バージョン5.0リリース。

なお、現在公開されている最新の版はバージョン5.0.0.5である。

## 関連項目

  - [BASIC](../Page/BASIC.md "wikilink")

## 関連書籍

  - 『ActiveBasicオフィシャルユーザーズガイド』 毎日コミュニケーションズ ISBN 4-8399-1456-7

## 外部リンク

  - [activebasic.com](http://www.activebasic.com/) （Activebasic公式Webサイト）
  - [NoVVest](http://www5e.biglobe.ne.jp/~imanisi/) （完全定義ファイルの配布）

[Category:BASIC](https://ja.wikipedia.org/wiki/Category:BASIC "wikilink") [Category:統合開発環境](https://ja.wikipedia.org/wiki/Category:統合開発環境 "wikilink") [Category:コンパイラ](https://ja.wikipedia.org/wiki/Category:コンパイラ "wikilink") [Category:フリーウェア](https://ja.wikipedia.org/wiki/Category:フリーウェア "wikilink") [Category:オブジェクト指向言語](https://ja.wikipedia.org/wiki/Category:オブジェクト指向言語 "wikilink")
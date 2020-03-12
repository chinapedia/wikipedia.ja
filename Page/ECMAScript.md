> この記事は[ECMAScript](https://ja.wikipedia.org/wiki/ECMAScript)から翻訳されています。


**ECMAScript**（エクマスクリプト）は、[JavaScript](../Page/JavaScript.md "wikilink")の標準であり、[Ecma Internationalのもとで標準化手続きなどが行われている](https://ja.wikipedia.org/wiki/Ecma_International "wikilink")。

Ecma Internationalのほか、[ISO/IEC JTC 1からもISO](https://ja.wikipedia.org/wiki/ISO/IEC_JTC_1 "wikilink")/IEC 16262として標準化されている。日本もJIS X 3060として[JIS化している](https://ja.wikipedia.org/wiki/日本工業規格 "wikilink")。

__TOC__

## バージョン

ECMAScript仕様は、Ecma InternationalにてECMA-262という規格番号で標準化されている。改訂にあたっては版 (edition) が更新されている。

6th editionから、「ECMAScript 2015」仕様の名称に発行年が付加されることになった。以降、ECMAScriptは毎年改訂されることになり、以降特定の版を指す場合は、edition名ではなく年号つきの仕様書名で呼ばれることが推奨されている\[1\]。

| Edition   | 公開日      | 以前のバージョンとの違い                                                                                                                                                                                                                                                                                                                                                  | 編集者                                                       |
| --------- | -------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------- |
| 1         | 1997年6月  | 初版                                                                                                                                                                                                                                                                                                                                                            | [Guy L. Steele, Jr.](../Page/ガイ・スティール・ジュニア.md "wikilink") |
| 2         | 1998年6月  | Editionとしての仕様はそのままであり、ISO/IEC 16262 international standardに完全な対応をした                                                                                                                                                                                                                                                                                           | Mike Cowlishaw                                            |
| 3         | 1999年12月 | 正規表現、よりよい文字列の取り扱い、新しいコントロール構文、try/catch例外処理、より厳格なエラー処理、数字のその他の書式化フォーマット                                                                                                                                                                                                                                                                                       | Mike Cowlishaw                                            |
| 4         | 放棄       | 4th Editionは放棄された。言語の複雑化に関する政治的な差異による。いくつかの成果は5thの基礎として採用され、いくつかは6thの基礎となっている。                                                                                                                                                                                                                                                                                |                                                           |
| 5         | 2009年12月 | "strictモード"、初期化時に発生しがちなエラーを回避するための追加仕様の追加。多くの曖昧な部分、および仕様に準拠しつつも現実世界の実装の融通の利く振る舞いを明確にした。いくらかの新機能、getterやsetter、[JSON](../Page/JavaScript_Object_Notation.md "wikilink")[ライブラリ](../Page/ライブラリ.md "wikilink")のサポート、より完全な[オブジェクトの](../Page/オブジェクト_\(プログラミング\).md "wikilink")[属性](../Page/属性.md "wikilink")の[リフレクション](../Page/リフレクション_\(情報工学\).md "wikilink")\[2\] | Pratap Lakshman, Allen Wirfs-Brock                        |
| 5.1       | 2011年6月  |                                                                                                                                                                                                                                                                                                                                                               | Pratap Lakshman, Allen Wirfs-Brock                        |
| 6 (2015)  | 2015年6月  | [クラス](../Page/クラス_\(コンピュータ\).md "wikilink")、[モジュール](../Page/モジュール.md "wikilink")、イテレータ、for/ofループ、[Python](../Page/Python.md "wikilink")スタイルのジェネレータ、アロー関数、2進数および8進数の整数リテラル、Map、Set、WeakMap、WeakSet、プロキシ、テンプレート文字列、let、const、型付き配列、デフォルト引数、Symbol、Promise、分割代入、可変長引数                                                                                            | Allen Wirfs-Brock                                         |
| 7 (2016)  | 2016年6月  | 冪乗演算子、Array.prototype.includes                                                                                                                                                                                                                                                                                                                                | Brian Terlson                                             |
| 8 (2017)  | 2017年6月  | 非同期関数 (async/await)、SharedArrayBufferとAtomics、String.padStart/padEnd、Object.values/entries、Object.getOwnPropertyDescriptors、関数の引数における末尾のカンマ許容                                                                                                                                                                                                                 |                                                           |
| 9 (2018)  | 2018年6月  |                                                                                                                                                                                                                                                                                                                                                               | Brian Terlson                                             |
| 10 (2019) | 2019年6月  |                                                                                                                                                                                                                                                                                                                                                               | Brian Terlson, Bradley Farias, Jordan Harband             |

ECMAScriptにはいくつかの拡張が存在する。

  - ECMA-357 ([ECMAScript for XML](https://ja.wikipedia.org/wiki/ECMAScript_for_XML "wikilink")) - 2004年公開、E4Xとして知られる
  - ECMA-402（国際化API） - 2012年公開
  - ECMA-404 (JSON) - 2013年公開

EcmaはECMAScriptのための "Compact Profile" も定義した — ES-CP、あるいはECMA 327として知られる — リソースの厳しいデバイス用にデザインされている。ECMAScriptのいくつかの動的な機能(『eval』関数など)はオプションにされている。これにより、処理系はプログラムの振る舞いに対してより多くの仮定ができるようになり、その結果、より良いパフォーマンス・トレードオフを実行時に得ることができるようになる。 [HD DVD](../Page/HD_DVD.md "wikilink") standardはECMAScript Compact Profileに準拠し、完全なECMAScriptの支援をより少ないメモリのデバイスで実行できるよう採用している。

## 文法

## 方言およびその呼称

ECMAScript は、[ウェブブラウザ](../Page/ウェブブラウザ.md "wikilink")をはじめとする多くの[アプリケーションでサポートされている](../Page/アプリケーションソフトウェア.md "wikilink")。[DOMとの連携はドキュメントの操作を可能にする](../Page/Document_Object_Model.md "wikilink")。

<table>
<thead>
<tr class="header">
<th><p>アプリケーション</p></th>
<th><p>呼称</p></th>
<th><p>最新バージョン</p></th>
<th><p>対応するECMAScriptリビジョン</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><a href="../Page/Mozilla.md" title="wikilink">Mozilla</a>およびその派生品</p></td>
<td><p><a href="../Page/JavaScript.md" title="wikilink">JavaScript</a></p></td>
<td><p>1.8.5</p></td>
<td><p>ECMA-262 5.1 edition<br />
ECMA-357[3]</p></td>
</tr>
<tr class="even">
<td><p><a href="../Page/Internet_Explorer.md" title="wikilink">Internet Explorer</a></p></td>
<td><p><a href="../Page/JScript.md" title="wikilink">JScript</a>（IE8まで）</p></td>
<td><p>5.8</p></td>
<td><p>ECMA-262 3rd edition</p></td>
</tr>
<tr class="odd">
<td><p><a href="../Page/JavaScript.md" title="wikilink">JavaScript</a> (Chakra)</p></td>
<td><p>11.0</p></td>
<td><p>ECMA-262 5.1 edition</p></td>
<td></td>
</tr>
<tr class="even">
<td><p><a href="https://ja.wikipedia.org/wiki/Google_Chrome" title="wikilink">Google Chrome</a><br />
<a href="https://ja.wikipedia.org/wiki/Opera" title="wikilink">Opera</a></p></td>
<td><p>JavaScript</p></td>
<td></td>
<td><p>ECMA-262 5.1 edition</p></td>
</tr>
<tr class="odd">
<td><p><a href="../Page/Safari.md" title="wikilink">Safari</a> (JSCore)</p></td>
<td><p>JavaScript</p></td>
<td></td>
<td><p>ECMA-262 5.1 edition</p></td>
</tr>
<tr class="even">
<td><p><a href="../Page/Konqueror.md" title="wikilink">Konqueror</a> (KJS)</p></td>
<td><p>JavaScript</p></td>
<td></td>
<td><p>ECMA-262 3rd edition</p></td>
</tr>
<tr class="odd">
<td><p><a href="https://ja.wikipedia.org/wiki/iCab" title="wikilink">iCab</a></p></td>
<td><p>InScript</p></td>
<td></td>
<td><p>ECMA-262 3rd edition</p></td>
</tr>
<tr class="even">
<td><p><a href="https://ja.wikipedia.org/wiki/.NET_Framework" title="wikilink">Microsoft .NET</a></p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/JScript_.NET" title="wikilink">JScript .NET</a></p></td>
<td><p>10.0</p></td>
<td><p>ECMA-262 4th草案 [4]</p></td>
</tr>
<tr class="odd">
<td><p><a href="../Page/Adobe_Flash.md" title="wikilink">Adobe Flash</a></p></td>
<td><p><a href="../Page/ActionScript.md" title="wikilink">ActionScript</a></p></td>
<td><p>3</p></td>
<td><p>ECMA-262 4th草案 [5]<br />
ECMA-357</p></td>
</tr>
<tr class="even">
<td><p><a href="../Page/Adobe_Acrobat.md" title="wikilink">Adobe Acrobat</a></p></td>
<td><p>JavaScript</p></td>
<td><p>1.5</p></td>
<td><p>ECMA-262 3rd edition</p></td>
</tr>
<tr class="odd">
<td><p><a href="../Page/Adobe_Creative_Suite.md" title="wikilink">Adobe Creative Suite</a></p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/ExtendScript" title="wikilink">ExtendScript</a></p></td>
<td></td>
<td><p>ECMA-262 3rd edition</p></td>
</tr>
<tr class="even">
<td><p><a href="https://ja.wikipedia.org/wiki/DMDScript" title="wikilink">DMDScript</a></p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/DMDScript" title="wikilink">DMDScript</a></p></td>
<td></td>
<td><p>ECMA-262 3rd edition</p></td>
</tr>
<tr class="odd">
<td><p><a href="../Page/Qt.md" title="wikilink">Qt</a></p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/QtScript" title="wikilink">QtScript</a></p></td>
<td></td>
<td><p>ECMA-262 3rd edition</p></td>
</tr>
<tr class="even">
<td><p><a href="https://ja.wikipedia.org/wiki/Max/MSP" title="wikilink">Max/MSP</a></p></td>
<td><p>JavaScript</p></td>
<td><p>1.5</p></td>
<td><p>ECMA-262 3rd edition</p></td>
</tr>
</tbody>
</table>

## ECMAScript 4

ECMAScript 4は過去2回仕様作成が挑戦されたが、仕様がまとまらず、失敗に終わっている。

### 1回目

2000年〜2003年ごろ行われた。主に、旧Netscape社と[マイクロソフト](../Page/マイクロソフト.md "wikilink")によって行われたが、意見がまとまらずに、打ち切りとなった。この時の案は[ActionScript](../Page/ActionScript.md "wikilink")へと引き継がれた。

  - <https://www-archive.mozilla.org/js/language/old-es4> - 昔のNetscape草案

### 2回目

2007年〜2008年ごろ、2回目の仕様作成が行われた。大きく機能を追加される予定であったが、意見がまとまらず、[2008年](https://ja.wikipedia.org/wiki/2008年 "wikilink")[8月13日](../Page/8月13日.md "wikilink")に、小規模の改善にとどまる、ECMAScript 3.1を進めることとなった\[6\]。仕様は、http://www.ecmascript.org/docs.php にて公開されている。

以下のような予定があった。

  - 大規模・大人数開発のための機能の追加
  - 型に関する機能の追加
  - [ジェネリックプログラミング](../Page/ジェネリックプログラミング.md "wikilink")の機能の追加
  - ECMAScript 3 が下位互換だが、互換でない仕様が一部に入る
  - ActionScript 3 の上位互換だが、互換でない仕様が一部に入る

## 脚注

## 関連項目

  - [ECMAScript for XML](https://ja.wikipedia.org/wiki/ECMAScript_for_XML "wikilink") (E4X)
  - [JavaScript Object Notation](../Page/JavaScript_Object_Notation.md "wikilink") (JSON)
  - [CommonJS](https://ja.wikipedia.org/wiki/CommonJS "wikilink")
  - [TypeScript](https://ja.wikipedia.org/wiki/TypeScript "wikilink")

## 外部リンク

  - [ECMAScript](https://www.ecma-international.org/)
  - ECMAScript言語仕様
      - [Standard ECMA-262](https://www.ecma-international.org/publications/standards/Ecma-262.htm)
          - [ECMA-262 ECMAScript Language Specification 3rd edition (December 1999)](https://www.ecma-international.org/publications/files/ECMA-ST-ARCH/ECMA-262,%203rd%20edition,%20December%201999.pdf)
          - [ECMA-262 ECMAScript Language Specification 5th edition (December 2009)](https://www.ecma-international.org/publications/files/ECMA-ST-ARCH/ECMA-262%205th%20edition%20December%202009.pdf)
          - [ECMA-262 ECMAScript Language Specification 5.1 edition (June 2011)](https://www.ecma-international.org/ecma-262/5.1/index.html)
          - [Standard ECMA-262 6th Edition / June 2015 ECMAScript 2015 Language Specification](https://www.ecma-international.org/ecma-262/6.0/index.html)
      - [Standard ECMA-290 ECMAScript Components Specification (June 1999)](https://www.ecma-international.org/publications/standards/Ecma-290.htm)
      - [Standard ECMA-327 ECMAScript 3rd Edition Compact Profile (June 2001)](https://www.ecma-international.org/publications/standards/Ecma-327.htm)
      - [Under Translation of ECMA-262 3rd Edition(日本語訳)](http://www2u.biglobe.ne.jp/~oz-07ams/2002/ecma262r3/index.html)
  - ECMAScript実装
      - [SpiderMonkey](https://ja.wikipedia.org/wiki/SpiderMonkey "wikilink") ([SpiderMonkey](http://www.mozilla.org/js/spidermonkey/)) - C - Firefox/Mozillaブラウザで使われている
      - [KJS](http://webcvs.kde.org/kdelibs/kjs/) - C++ - KDEのKonquerorブラウザで使われている
      - [JavaScriptCore](http://developer.apple.com/darwin/projects/webcore/) - C++ - MAC OS XのSafariブラウザやdashboardで使われている。KJSベース
      - [V8](https://ja.wikipedia.org/wiki/V8_\(JavaScriptエンジン\) "wikilink") - C++ - Google Chromeブラウザで使われている
      - [NJS](http://www.njs-javascript.org/) - C
      - [SEE - Simple ECMAScript Engine](http://www.adaptive-enterprises.com.au/~d/software/see/) - C
      - [ixlib](http://ixlib.sourceforge.net/) - C++
      - [QSA - Qt Script for Applications](http://www.trolltech.com/products/qsa/) - C++
      - [DMDScript](http://www.digitalmars.com/dscript/) - C++/D
      - [DMonkey](http://sourceforge.jp/projects/dmonkey/) - Delphi
      - [Rhino](../Page/Rhino.md "wikilink") ([Rhino](http://www.mozilla.org/rhino/)) - Java
      - [FESI - Free EcmaScript Interpreter](http://www.lugrin.ch/fesi/) - Java
      - [Scriptonite](http://scriptonite.sourceforge.net/) - Java
      - [xwt](http://www.xwt.org/) - Java
      - [JANET](http://janet-js.sourceforge.net/) - Java
      - [Epimetheus](http://www.mozilla.org/js/language/Epimetheus.html) - C++ - Mozillaプロジェクトによる以前のECMAScript Edition 4草案の実装
      - [Narcissus](https://ja.wikipedia.org/wiki/Narcissus "wikilink") - JavaScript

[Category:JavaScript](https://ja.wikipedia.org/wiki/Category:JavaScript "wikilink") [Category:スクリプト言語](https://ja.wikipedia.org/wiki/Category:スクリプト言語 "wikilink") [Category:Ecma](https://ja.wikipedia.org/wiki/Category:Ecma "wikilink")

1.  <http://www.wirfs-brock.com/allen/posts/778>
2.  [JavaScriptの変更, Part 1: EcmaScript 5](http://www.youtube.com/watch?v=Kq4FpMe6cRs)
3.  Mozillaは[1.8 Beta 1](http://www.mozilla.org/releases/mozilla1.8b1/README.html)以降で[E4Xをサポートしている](https://ja.wikipedia.org/wiki/ECMAScript_for_XML "wikilink")。
4.  2001年頃の[マイクロソフト](../Page/マイクロソフト.md "wikilink")の草案であり、独自に開発を進めたもので、現在のECMAScript 4草案とは大きく異なる。
5.  2001年頃のNetscapeの草案に近く、現在のECMAScript 4草案のサブセットに近い。
6.  <https://mail.mozilla.org/pipermail/es-discuss/2008-August/003400.html>
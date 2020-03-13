> この記事は[ActionScript](https://ja.wikipedia.org/wiki/ActionScript)から翻訳されています。


**ActionScript**（アクションスクリプト）とは、[アドビシステムズ](../Page/アドビシステムズ.md "wikilink")社の製品である [Flash](../Page/Adobe_Flash.md "wikilink") に使用される[プログラミング言語](../Page/プログラミング言語.md "wikilink")である。[ECMAScript](../Page/ECMAScript.md "wikilink") を拡張した物である。これを用いることにより、動画や音声のプレイヤーの作成など、[コンテンツ](../Page/コンテンツ.md "wikilink")に複雑な処理や双方向性を持たせ Flash 作品を作ることが可能である。

## 概要

ActionScript が初めて搭載されたのが2000年に発売された Flash 5 で、後継バージョンである Flash MX 2004（Flash 7）からは 2.0 が、Flash CS3（Flash 9）では 3.0 が搭載されている。Flash 4 やそれ以前にもスクリプト機能は搭載されていたが、それは、ActionScript とは呼ばれておらず、ECMAScript ベースでもなかった。

初代 ActionScript は単純で覚えやすい[スクリプト言語](../Page/スクリプト言語.md "wikilink")であり、[プロトタイプベース](../Page/プロトタイプベース.md "wikilink")の[オブジェクト指向](../Page/オブジェクト指向.md "wikilink")言語だったが、ActionScript 2.0、3.0ではより大規模開発に適した[クラスベース](../Page/クラスベース.md "wikilink")のオブジェクト指向言語を搭載した。

ActionScript は主に SWF ファイルの開発用ソフトウェアである Adobe Flash および [Adobe Flex](https://ja.wikipedia.org/wiki/Adobe_Flex "wikilink") でスクリプトとして記述する。

## 文法

ActionScript 1.0は文法が JavaScript に似ているが、ActionScript 2.0 からはクラスベースのオブジェクト指向言語になりJavaに似通っている。ActionScript ではすべてのデータをオブジェクトと見なしている。Flash ではプログラミングコードを記述する場所が複数あり、タイムラインのフレーム上に書いた場合とクラスとして外部ファイルに書いた場合と記述の仕方が若干異なる。また、ActionScript 2.0（Flash 8）まではムービークリップまたはボタン上にプログラミングコードを記述できたが、 ActionScript 3.0（Flash CS3）で廃止された。ここでは ActionScript 3.0の文法を説明していく。

### 変数の宣言

変数の宣言は下記の書式で記述する。

``` ActionScript
var 変数名 : 変数の型
```

例えば、

``` ActionScript
var num : int ;
```

### 関数の宣言

関数の宣言は下記の書式で記述する。

``` ActionScript
function 関数名 (引数1:引数1の型, 引数2:引数2の型, ...) : 戻り値の型
  {
  実行するコード1
  実行するコード2
        :
  }
```

例えば、

``` ActionScript
function sum (a:Number, b:Number) : Number
  {return a + b ;}
```

戻り値がない場合は戻り値の型を `void` とする\[1\]。`void`と宣言した場合、戻り値は `undefined` になる。

### クラスの宣言

クラスの構文は Java に似通っている。クラスとコンストラクタは必ず `public` にしなければならない。コンストラクタは省略可能である。ファイル名は「`クラス名.as`」とし、パッケージと同じディレクトリに置かなければならない。

``` ActionScript
package パッケージ名
  {
  public class クラス名
    {
    //コンストラクタ
    public function クラス名 ()
      {
      }
    }
  }
```

## 統合開発環境

### アドビシステムズ社

ActionScript を編集するためにアドビシステムズ社が提供する各種アプリケーションは、一般的に使われている統合開発環境とは異なる点が多く、それらに慣れたプログラマーには評判が悪い傾向がある。[Adobe Flex](https://ja.wikipedia.org/wiki/Adobe_Flex "wikilink") Builder では、[Eclipseプラグインの形で編集環境を提供しており](../Page/Eclipse_\(統合開発環境\).md "wikilink")、別言語の修得者は差異に悩むことなく開発を行える。また Adobe Flex SDK がアドビシステムズから無償で提供されている。これら以外の統合開発環境では [FlashDevelop](https://ja.wikipedia.org/wiki/FlashDevelop "wikilink") などがある。

### その他

無償のオープンソースの物や、アドビシステムズ以外の会社が提供する Flash 開発用ソフトウェアも発売されている。それらのソフトにも ActionScript に対応しているものがある。オープンソースの Motion-Twin ActionScript 2 Compiler\[2\] はアドビシステムズ社の製品よりもコンパイルが速いと謳われている。

またオープンソースのコンパイラを利用して ActionScript から SWF ファイルを作る、「FAME」「FAMES」「FLAMES」等と呼ばれる開発環境/開発手法が注目されている。

<table>
<thead>
<tr class="header">
<th><p>製品名</p></th>
<th><p>備考</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><a href="https://ja.wikipedia.org/wiki/LiveSwif" title="wikilink">LiveSwif</a>[3]</p></td>
<td><p>タイムライン式。ActionScript に対応している。</p></td>
</tr>
<tr class="even">
<td><p><a href="../Page/ParaFla!.md" title="wikilink">ParaFla!</a></p></td>
<td><p>イベント式。ActionScript に対応している。</p></td>
</tr>
<tr class="odd">
<td><p>[4]</p></td>
<td><p>タイムライン式。ActionScript に対応している。</p></td>
</tr>
<tr class="even">
<td><p><a href="https://ja.wikipedia.org/wiki/wonderfl" title="wikilink">wonderfl</a></p></td>
<td><p>ブラウザから ActionScript を入力し、サーバサイドでコンパイルを行うことで無償で開発を行うことができる。</p></td>
</tr>
<tr class="odd">
<td><p><a href="https://ja.wikipedia.org/wiki/CodeDrive" title="wikilink">CodeDrive</a>[5]</p></td>
<td></td>
</tr>
<tr class="even">
<td><p>ActionScript 3/Flash IDE</p></td>
<td></td>
</tr>
<tr class="odd">
<td><p><a href="https://ja.wikipedia.org/wiki/FlashDevelop" title="wikilink">FlashDevelop</a></p></td>
<td><p>Adobe AIR 製ソフトや Flash コンテンツを作成できる無償の開発環境</p></td>
</tr>
</tbody>
</table>

## Flash における ActionScript の歴史

### スクリプト未搭載

| 公開日   | 製品      | 備考 |
| ----- | ------- | -- |
| 1996年 | Flash 1 |    |

### ActionScript 前

| 公開日   | 製品      | 備考                                                                                   |
| ----- | ------- | ------------------------------------------------------------------------------------ |
| 1997年 | Flash 2 | ボタン機能搭載と共に「ボタンアクション」「フレームアクション」搭載。`getURL()` や `gotoAndPlay()` などが可能。フレーム間の移動が可能になる。 |
| 1998年 | Flash 3 | 複数のスクリプトの記述が可能になった。`loadMovie()`、`fscommand()`など実装。                                  |
| 1999年 | Flash 4 | 「アクション」機能大幅高度化。変数、四則演算、文字列処理、条件分岐などが追加。関数呼び出しに相当するのは、フレームの移動である、`call()` である。        |

### ActionScript 1

処理系は ActionScript Virtual Machine 1 である。

| 公開日   | 製品       | 備考                                                              |
| ----- | -------- | --------------------------------------------------------------- |
| 2000年 | Flash 5  | ECMAScript ベースとなり、関数が作れるようになる。                                  |
| 2002年 | Flash MX | イベントハンドラメソッド」搭載。`instanceof` や `===` が導入され、より ECMAScript 準拠となる。 |

### ActionScript 2

| 公開日   | 製品            | 備考                             |
| ----- | ------------- | ------------------------------ |
| 2003年 | Flash MX 2004 | クラスベースのオブジェクト指向が導入される。例外処理を追加。 |
| 2005年 | Flash 8       |                                |

### ActionScript 3

処理系が ActionScript Virtual Machine 2 となった。フレームワークも全面的に改装され、立体、透視の実装や、新しいディスプレイオブジェクトとディスプレイオブジェクトコンテイナーの体制が取り入れた。文法では、関数を直接にイベントの使用することなどが出来なくなり、3D モデリングソフトウェアのように自動的に物体の「深さ」（デプス）をレンダリングできないので、これ以前の版に慣れているプログラマーには難しいかもしれない。そのために、色々なライブラリ（3D、フィルターなど）がウェブ上で公開されている。

| 公開日         | 製品        | 備考 |
| ----------- | --------- | -- |
| 2006年7月28日  | Flex 2.0  |    |
| 2007年3月27日  | Flash CS3 |    |
| 2008年2月25日  | Flex 3.0  |    |
| 2008年2月25日  | AIR 1.0   |    |
| 2008年12月19日 | Flash CS4 |    |

## 脚注

<references />

## 関連項目

  - [Adobe Flash](../Page/Adobe_Flash.md "wikilink")
  - [Adobe Flex](https://ja.wikipedia.org/wiki/Adobe_Flex "wikilink")
  - [Adobe Integrated Runtime](https://ja.wikipedia.org/wiki/Adobe_Integrated_Runtime "wikilink")
  - [ECMAScript for XML](https://ja.wikipedia.org/wiki/ECMAScript_for_XML "wikilink")

[Category:Adobe_Flash](https://ja.wikipedia.org/wiki/Category:Adobe_Flash "wikilink") [Category:JavaScript](https://ja.wikipedia.org/wiki/Category:JavaScript "wikilink") [Category:スクリプト言語](https://ja.wikipedia.org/wiki/Category:スクリプト言語 "wikilink")

1.  ActionScript 2.0では `Void`。
2.  <http://tech.motion-twin.com/mtasc.html>
3.  <http://www.liveswif.net/>
4.  <http://www.cty-net.ne.jp/~uzgensho/>
5.  <http://www.codedrive.com/>
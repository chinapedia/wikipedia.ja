> この記事は[QuickBASIC](https://ja.wikipedia.org/wiki/QuickBASIC)から翻訳されています。


**QuickBASIC**(クイックベーシック)は、[マイクロソフト](../Page/マイクロソフト.md "wikilink")が開発した[統合開発環境](../Page/統合開発環境.md "wikilink")。また、そこで用いられる[プログラミング言語](../Page/プログラミング言語.md "wikilink")。 [Microsoft Visual Basicの前身でもある](https://ja.wikipedia.org/wiki/Microsoft_Visual_Basic "wikilink")。[MS-DOS](../Page/MS-DOS.md "wikilink")版と[Macintosh](../Page/Macintosh.md "wikilink")版がある。

MS-DOS版の開発環境はMS-DOS上での動作ながら非常に高機能で、かつ文字ベースで[GUI](https://ja.wikipedia.org/wiki/GUI "wikilink")を[エミュレート](https://ja.wikipedia.org/wiki/エミュレート "wikilink")していたため視覚的に操作できた。

## 開発環境

### [コンパイラ](../Page/コンパイラ.md "wikilink")・[インタプリタ](../Page/インタプリタ.md "wikilink")

  - コンパイラは、実行ファイルのサイズが小さいランタイム版、実行が高速な独立版のバイナリをそれぞれ生成することができた。
  - インタプリタ実行の場合、後述するデバッガを利用することができた。
  - 複数のソースファイルの分割コンパイル、リンクができた。プロジェクトの作成にも対応していた。

### エディタ

  - [ソースコード](../Page/ソースコード.md "wikilink")の入力中に文法エラーを検出して指摘する機能があった。
  - テキストの範囲指定、コピー、ペースト、検索、置換、インデント調整など豊富な編集機能があった。
  - サブルーチン単位で画面に表示して編集することができた。
  - ソースファイルの読み込み及び保存は、テキスト形式に加え[N88-BASIC](../Page/N88-BASIC.md "wikilink")のバイナリ形式でも行えた(PC-9801版のみ)。

### オンラインヘルプ

  - [ソースコード](../Page/ソースコード.md "wikilink")の編集を中断せずに、[オンラインヘルプ](../Page/オンラインヘルプ.md "wikilink")を閲覧することができた。

`  CALL mdreceived(path&, &HFF, 22, 1, 84, db1(1), ret3%)`

### [デバッガ](../Page/デバッガ.md "wikilink")

主に以下のような機能があった。

  - [ブレークポイント](https://ja.wikipedia.org/wiki/ブレークポイント "wikilink")
  - ステップ実行
  - ウォッチ(変数や式の値の確認)

## 言語

[構造化](https://ja.wikipedia.org/wiki/構造化 "wikilink")に対応して大きく機能拡張されているのが特徴。（このため旧世代の[BASIC](../Page/BASIC.md "wikilink")とは、まったく別物に見える。）

### [データ型](../Page/データ型.md "wikilink")

  - [整数](../Page/整数.md "wikilink")
  - (単精度および倍精度)[浮動小数点](https://ja.wikipedia.org/wiki/浮動小数点 "wikilink")
  - [文字列](../Page/文字列.md "wikilink")
  - (多次元)[配列](../Page/配列.md "wikilink")
  - [構造体](../Page/構造体.md "wikilink")

### [変数](../Page/変数_\(プログラミング\).md "wikilink")

グローバル変数とローカル変数、スタティック変数と[C言語](../Page/C言語.md "wikilink")で言うauto変数があった。

### 制御構造

#### ループ

  - `for`
  - `while ... wend`
  - `do ... loop`

最後の `do ... loop` がもっとも柔軟に書ける形式である。

<table>
<tbody>
<tr class="odd">
<td><p><code>do while 条件</code><br />
<code>    ...</code><br />
<code>loop</code></p></td>
<td><p><code>do until 条件</code><br />
<code>    ...</code><br />
<code>loop</code></p></td>
</tr>
<tr class="even">
<td><p><code>do</code><br />
<code>    ...</code><br />
<code>loop while 条件</code></p></td>
<td><p><code>do</code><br />
<code>    ...</code><br />
<code>loop until 条件</code></p></td>
</tr>
</tbody>
</table>

#### 分岐

  - 一行`if`

`if 条件 then 真のとき else 偽のとき`

  - 複数行`if`

`if 条件 then`
`   真のとき`
`else`
`   偽のとき`
`end if`

  - `select case`
    C言語の`switch`文に似ているが、整数以外の値も使用でき、範囲などの条件を記述することもできた。

#### 関数・サブルーチン

  - サブルーチンを記述することができた。値を返す場合は関数、値を返さない場合はサブルーチンであった。
  - C言語のreturnに相当する `Exit Sub` ・ `Exit Function` ステートメントがそれぞれあった。
  - 再帰呼び出しが可能だった。

#### 割り込み処理

以下のようなタイミングで割り込み処理を行うことができた。

  - エラー発生
  - キー押下
  - タイマー
  - 音楽演奏バッファ

エラーに対する割り込み処理を行った場合、`resume`ステートメントで元の処理を再開することもできた。

## 関連項目

  - [FreeBASIC](../Page/FreeBASIC.md "wikilink")
  - [QB64](https://www.portal.qb64.org/)

[Category:BASIC](https://ja.wikipedia.org/wiki/Category:BASIC "wikilink") [Category:コンパイラ](https://ja.wikipedia.org/wiki/Category:コンパイラ "wikilink") [Category:マイクロソフトの開発ツール](https://ja.wikipedia.org/wiki/Category:マイクロソフトの開発ツール "wikilink") [Category:マイクロソフトのプログラミング言語](https://ja.wikipedia.org/wiki/Category:マイクロソフトのプログラミング言語 "wikilink") [Category:1985年のソフトウェア](https://ja.wikipedia.org/wiki/Category:1985年のソフトウェア "wikilink")
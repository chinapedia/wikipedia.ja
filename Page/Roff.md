> この記事は[Roff](https://ja.wikipedia.org/wiki/Roff)から翻訳されています。


**roff** とは [UNIX](../Page/UNIX.md "wikilink") に於ける文書整形を行うコマンド、ただし今日ではこの名称のコマンドは廃棄されており、主に troff、nroff の総称として使われる。また GNU による [groff](https://ja.wikipedia.org/wiki/groff "wikilink") がある。

## 概要

roff とは文書の整形、清書を行うコマンドである。roff の名称の由来は「to <u>r</u>un <u>off</u> a copy（コピーを取り出す）」の略である。

roff は通常のテキストファイルに整形用要素を加えたファイルを読み込み、ドキュメントを生成する。roff 自身の基本機能は非常に単純であるが幾つかの機能を組み合わせた[マクロパッケージを生成することが出来る](https://ja.wikipedia.org/wiki/マクロ_\(コンピュータ用語\) "wikilink")。この考え方は UNIX のシステム記述言語でもある[C言語](../Page/C言語.md "wikilink")などの考え方とも共通する。roff の機能には変数、制御構造といったものも存在するため最初期の[マークアップ言語](../Page/マークアップ言語.md "wikilink")ということもできる。[チューリング完全](https://ja.wikipedia.org/wiki/チューリング完全 "wikilink")性を備えている。

## 歴史

roff の起源は古く最初期の UNIX から存在しており、概念に関しては[1960年代](../Page/1960年代.md "wikilink")にまでさかのぼる。[1961年](https://ja.wikipedia.org/wiki/1961年 "wikilink")に初めて実演された [CTSS](https://ja.wikipedia.org/wiki/CTSS "wikilink") に既に **RUNOFF** と呼ばれる文書整形プログラムが存在していた。UNIX の前身でもある [Multics](https://ja.wikipedia.org/wiki/Multics "wikilink") ではこの RUNOFF を参考にして **runoff** というプログラムを作成し、文書整形やヘルプファイルの記述に使用された。roff はこの runoff を参考にしてにより UNIX 上で動作するように開発されたものである。

[1973年](../Page/1973年.md "wikilink")に最初の roff がリリースされた。このプログラムは [PDP-11](https://ja.wikipedia.org/wiki/PDP-11 "wikilink") アセンブラで記述されていたが、後に[C言語](../Page/C言語.md "wikilink")で書き直されたバージョンが[1975年](../Page/1975年.md "wikilink")にリリースされている。最初期の roff は3つのフォーマットプログラムを持ち、それぞれ nroff、troff、roff というコマンド名であった。この内 nroff は画面上での表示、troff は印刷文書上での表示形式であり roff というコマンドは Multics の runoff の再実装として開発されていた。しかし後のバージョンで roff コマンドは廃棄されており、現在では roff という単語は nroff、troff とこのシステムの派生作品を含めた総称として主に使われている。

## nroff

nroff は new roff の略である。roff で作る文書を端末[ディスプレイ等にテキストデータで表示する際の書式を設定する目的でジョー](../Page/ディスプレイ_\(コンピュータ\).md "wikilink")・オサンナにより開発された。nroff が最も使用される場面として UNIXの [man](https://ja.wikipedia.org/wiki/Manページ "wikilink") コマンドが挙げられる。このコマンドは各コマンドの説明文書を画面上に呼び出す機能であるが、各文書は nroff 形式で保存されており、man コマンドが実行されると nroff によって整形され[ページャ](https://ja.wikipedia.org/wiki/ページャ "wikilink")を通して画面に出力されるという動作が行われている。

## troff

troff は主に[写植機](https://ja.wikipedia.org/wiki/写植機 "wikilink")（あるいは[プリンタ](https://ja.wikipedia.org/wiki/プリンター "wikilink")）に文書を印刷する際の書式設定を行う roff である。もともとは [C/A/T](https://ja.wikipedia.org/wiki/C/A/T "wikilink") という写植機用の印刷データを生成する目的で開発されており、この写植機上で使用する特有のコマンドセットが数多く定義されている。初期のバージョンはジョー・オサンナを中心に開発が行われていたが、[1977年](../Page/1977年.md "wikilink")にジョー・オサンナが心臓麻痺で他界して後は主に[ブライアン・カーニハン](../Page/ブライアン・カーニハン.md "wikilink")が中心になって開発が継続された。[1979年](../Page/1979年.md "wikilink")に C/A/T 以外のフォトタイプセットを扱えるようにしたり、一般的なインターフェイスを備えるなど大幅に改良を施したバージョンが発表された。

## roff のプリプロセッサ

roff におけるプリプロセッサとは roff のフォーマットに変換し出力を生成するプログラムの事を指す。各プリプロセッサはそれぞれ独自の言語で策定されており、ファイルをプリプロセッサに通すと、roff のフォーマットに変換を行う。このような言語で記述された部分は一般に roff の文書に埋め込み、プリプロセッサを通してから roff に通すことで文書を作成する、ほとんどのプリプロセッサはファイルの内容の中で自分自身のものと判断した部分のみを抽出して変換を行い、それ以外の場所は無視するので命令等が一致しないなら複数のプリプロセッサの書式を同一ファイル内に記述することができる。以下に代表的な roff のプリプロセッサを挙げる。

  - [eql](https://ja.wikipedia.org/wiki/eql "wikilink")
    数式を roff 形式のフォーマットに変換する。
  - [tbl](https://ja.wikipedia.org/wiki/tbl "wikilink")
    表を含む文書を roff 形式のフォーマットに変換する。
  - [pic](https://ja.wikipedia.org/wiki/pic言語 "wikilink")
    roff 形式の文書に図を埋め込むプリプロセッサ。
  - [refer](https://ja.wikipedia.org/wiki/refer "wikilink")
    roff の文書に[参考文献](../Page/参考文献.md "wikilink")の部分を自動生成するプリプロセッサ（[LaTeX](../Page/LaTeX.md "wikilink") における thebibliography 環境に近い）。

## 関連項目

  - [manページ](https://ja.wikipedia.org/wiki/manページ "wikilink")

## 参考文献

  - シェリー・パワーズ他著、『[Unix パワーツール 第3版](https://www.oreilly.co.jp/books/4873111420/)』、ドキュメントシステム訳、[オライリー・ジャパン](https://ja.wikipedia.org/wiki/オライリー・ジャパン "wikilink")、2003年、ISBN 4-87311-142-0

[Category:UNIXのソフトウェア](https://ja.wikipedia.org/wiki/Category:UNIXのソフトウェア "wikilink") [Category:マークアップ言語](https://ja.wikipedia.org/wiki/Category:マークアップ言語 "wikilink") [Category:1973年のソフトウェア](https://ja.wikipedia.org/wiki/Category:1973年のソフトウェア "wikilink")
> この記事は[Forsyth-Edwards Notation](https://ja.wikipedia.org/wiki/Forsyth-Edwards_Notation)から翻訳されています。


**Forsyth-Edwards Notation**（略称：**FEN**）は、[チェス](../Page/チェス.md "wikilink")における駒配置の標準的な表記法。また、その情報を記述したテキストファイル（拡張子は.fen）。

## 概要

スコットランドの新聞記者、デービッド・フォーサイスが発案した。19世紀頃に一般に用いられるようになり、スティーブン・J・エドワーズがコンピューターで利用できるように拡張した。盤面の初期状態をコンパクトに表記できるため、[Portable Game Notationにとってなくてはならないものになっている](../Page/Portable_Game_Notation.md "wikilink")。ただし、[千日手](../Page/千日手.md "wikilink")についての情報を持たせることはできない。

## 定義

FENは6つのフィールドに分かれる。各フィールドはスペース記号で区切られる。

1.  駒配置。
      - 8ランクから始まり、1ランクで終わる。各ランクはスラッシュ記号で区切られる。
      - 各ランクはaファイルから始まり、hファイルで終わる。
      - 8つのマスに入っている駒を順に1つずつ記述する。白のポーン=P、ナイト=N、ビショップ=B、ルーク=R、クイーン=Q、キング=K。黒の駒は小文字で書く。
      - 空いているマスがある場合、その数を数字で直接書く。例えばあるランクが全て空ならば"8"になる。（aファイルから順に）6つの空きマス、白ポーン、1つの空きマスならば"6P1"になる。
2.  手番。白の番ならばwを、黒の番ならばbを書く。
3.  キャスリングの可否。以下のうち、可能なものを全て書き並べる。どれも不可能ならばハイフン記号を1つ置く。
      - K：白はキングサイドにキャスリング可能
      - Q：白はクイーンサイドにキャスリング可能
      - k：黒はキングサイドにキャスリング可能
      - q：黒はクイーンサイドにキャスリング可能
4.  アンパッサン可能な位置。ポーンが2マス進んだ直後である場合、そのポーンが通過したマスを書く。存在しない場合はハイフン記号を1つ置く。
5.  最後のポーンの移動または駒取りがあってから経過したプライ（半手）数。白黒いずれかの指し手によって1増え、通常の手数の約2倍となる。これは[50手ルール](https://ja.wikipedia.org/wiki/50手ルール "wikilink")に対応するためである。
6.  手数。黒の指し手の後に1増える、通常の手数。

## 例

初期配置はこのように表記される。

`rnbqkbnr/pppppppp/8/8/8/8/PPPPPPPP/RNBQKBNR w KQkq - 0 1`

1\. e4 の直後

`rnbqkbnr/pppppppp/8/8/4P3/8/PPPP1PPP/RNBQKBNR b KQkq e3 0 1`

1\. ... c5 の直後

`rnbqkbnr/pp1ppppp/8/2p5/4P3/8/PPPP1PPP/RNBQKBNR w KQkq c6 0 2`

2\. Nf3 の直後

`rnbqkbnr/pp1ppppp/8/2p5/4P3/5N2/PPPP1PPP/RNBQKB1R b KQkq - 1 2`

## チェス960

[チェス960](../Page/チェス960.md "wikilink")のような変則チェスでは、駒の初期配置を指定することが不可欠であるため、FENは大きな役割を果たす。しかし、キングとクイーンの位置関係はランダムに変化するので、上述の3番目のフィールドにK、Q、k、qという文字を使うことは不適切である。そこでShredderやFritzといったチェスソフトではK、Q、k、qの代わりにA、H、a、hの文字を使う。これをShredder-FENと呼ぶことがある。

## 外部リンク(英語)

  - [Forsyth–Edwards Expanded Notation specification and implementation guide(リンク切れ)](https://developer.sashite.com/documents/feen/1.0.0)
  - [PGNとFENの棋譜書式指定と実装ガイド](http://www.thechessdrum.net/PGN_Reference.txt)

[Category:チェス](https://ja.wikipedia.org/wiki/Category:チェス "wikilink") [Category:コンピュータチェス](https://ja.wikipedia.org/wiki/Category:コンピュータチェス "wikilink") [Category:ファイルフォーマット](https://ja.wikipedia.org/wiki/Category:ファイルフォーマット "wikilink")
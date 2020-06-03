> この記事は[Portable Game Notation](https://ja.wikipedia.org/wiki/Portable_Game_Notation)から翻訳されています。


**Portable Game Notation**(PGN)とは、[コンピュータ](../Page/コンピュータ.md "wikilink")上で[チェス](../Page/チェス.md "wikilink")の[棋譜](../Page/棋譜.md "wikilink")を保存するための[ファイルフォーマット](../Page/ファイルフォーマット.md "wikilink")の一つ。拡張子は".pgn"。

[ASCII](../Page/ASCII.md "wikilink")文字のみによって記述されるため、多くのチェスプログラムが対応しており、事実上の標準形式となっている。座標式をそのまま書いているので、人間が直接読み書きすることも容易である。

## 概要

PGNには「インポート」と「エクスポート」の2種類のフォーマットがある。前者は人間が手で書くことを想定しており、したがって一定の表記の揺れが許される。後者はプログラムが生成するもので、出力したのがどのようなプログラムであれ、同じ内容の棋譜ならば[バイト単位で厳密に一致しなければならない](../Page/バイト_\(情報\).md "wikilink")。また、PGNに対応したプログラムは、どちらも取り扱うことができなければならない。

記述内容は、指し手、タグ、コメントの三つに分けられる。

## 指し手

実際の手を[座標式で](https://ja.wikipedia.org/wiki/棋譜#座標式 "wikilink")「手数、白の手、黒の手」の順で記述してゆく。改行は任意の位置に入れることができるが、1行は255バイト以下でなくてはならない。可読性のため、80バイトに抑えることが推奨されている。たとえば以下のようになる。

`1.e4 e5 2.Nf3 Nc6`
`3.Bb5 {This opening is called Ruy Lopez.} a6`
`4.Ba4`

ただし、手数の数字は存在しなくても構わない(人間が読みやすくするために書く)。記録が黒の手から始まる場合は、白の手の代わりにピリオド3つを置く。

`4... Nf6`
`5.O-O Be7`

書式は一般的な座標式がそのまま採用される。キャスリング("O-O"や"O-O-O")、プロモーション(例えば"b8=Q")等もそのまま書く。[妙手](https://ja.wikipedia.org/wiki/妙手 "wikilink")(指し手の後ろに"\!")、チェック("+")、チェックメイト("\#")等も書いて構わないが、一般的なソフトウェアには無視される。また、どちらかの勝利またはドローで試合が終了した場合、その結果が最終手の後に追記される。

`42.g4 Bd3`
`43.Re6 1/2-1/2`

## タグ

対局者の名前や駒の初期配置といった、対局についての情報を記録する部分である。以下のような内容になる。

`[Event "F/S Return Match"]`
`[Site "Belgrade, Serbia JUG"]`

全体が大カッコ(\[と\])で囲まれ、その中にタグの名前と値が入る。タグの値は2重引用符(")で囲まれ、[ISO/IEC 8859-1の文字によってのみ記述され](https://ja.wikipedia.org/wiki/ISO/IEC_8859-1 "wikilink")、また制御文字や改行コードが入ってはならない。余計なスペースは無視される。エクスポートフォーマットの場合、以下に挙げた7つのタグが必須である。これらは先頭に置かれ、また順序もこの通りでなければならない。

### 基本的なタグ

この7つのタグはSeven Tag Roster(STR)と呼ばれる。

  - Event: 大会の名前。
  - Site: 対局が行われた場所。"(地名), (地域名) (国名)"で記述される。なお、国名は[国際オリンピック委員会](../Page/国際オリンピック委員会.md "wikilink")が採用している3文字の国名コードが用いられる。例："New York City, NY USA"
  - Date: 対局が**始まった**日付。"YYYY.MM.DD"の形式。不詳の場合は"??"となる。例："1992.08.31"、"1993.??.??"
  - Round: この対局が何試合目かを示す。例："1"、"3.1"
  - White: 白の名前。ラストネーム・ファーストネームの順に書く。複数人いる場合、全てのプレーヤーの名前をアルファベット順にコロン(:)で並べて書く。
  - Black: 黒の名前。白と同様。
  - Result: 結果。以下の4通りの値のみが許される。"1-0"(白の勝ち)、"0-1" (黒の勝ち)、"1/2-1/2"(ドロー)、"\*"(その他。中断された場合等)。

### プレーヤーに関するタグ

  - WhiteTitle: 白が持つタイトルを記述する。"FM"、"IM"、"GM"等がある。タイトルを持っていない場合はハイフン1つを置く。白が複数人いる場合、名前と同じ順でコロンで区切って並べる。例："<IM:-:GM>"(3人が順にInternational Master、タイトルなし、Grand Masterである場合)
  - WhiteElo: 白が持つ[FIDE](https://ja.wikipedia.org/wiki/FIDE "wikilink")のEloレート。整数でなければならない。レートを持っていない場合はハイフン1つを置く。
  - WhiteUSCF: 白が持つ[USCFのレート](https://ja.wikipedia.org/wiki/アメリカ合衆国チェス連盟 "wikilink")。
  - WhiteNA: 白のメールアドレス(もしくはその他ネット上のアドレス)。存在しない場合はハイフン1つを置く。
  - WhiteType: 白が人間であるならば"human"、プログラムであるならば"program"となる。

黒についても同じタグがある。内容は同様なので省略する。

### 大会に関するタグ

  - EventDate: 大会の始まった日付。Dateと同じく"YYYY.MM.DD"の形式。
  - EventSponsor: 大会のスポンサー。
  - Section: 試合の形式について記述する。"Open"、"Reserve"等が入る。
  - Stage: 大会が複数の段階に分かれる場合に置く。"Preliminary"、"Semifinal"等。
  - Board: これらだけでは対局が特定できないとき、対局が行われたチェス盤の通し番号を示す。

### オープニングに関するタグ

  - Opening: この対局で用いられたオープニングの名前。
  - Variation: バリエーションの名前。
  - SubVariation: サブ・バリエーションの名前。
  - ECO: この対局で用いられたオープニングの[ECOコード](../Page/ECO_\(チェス\).md "wikilink")。例："D06"
  - NIC: この対局で用いられたオープニングのNICコード。

### 日付・時刻に関するタグ

  - Time: 対局が始まった現地時刻。"HH:MM:SS"の形式。
  - UTCTime: 対局が始まった[UTC時刻](../Page/協定世界時.md "wikilink")。"HH:MM:SS"の形式。
  - UTCDate: UTC時刻における、対局が開始された日の日付。

### 駒の初期配置に関するタグ

  - SetUp: 駒の初期配置が通常のものであった場合は0を置く。そうでなかった場合は1を置く。FENタグが存在する場合、このタグの値は必ず1になる。
  - FEN: 駒の初期配置を[FEN形式で記述する](../Page/Forsyth-Edwards_Notation.md "wikilink")。対局の途中から記録が始まる場合、[フィッシャー・ランダム・チェスのように特殊な駒配置から始まる場合などに用いられる](../Page/チェス960.md "wikilink")。

### 試合結果に関するタグ

  - Termination: 対局がどのようにして終了したかを示す。"abandoned"(試合放棄)、"adjudication"(判定)、"death"(対局者の死亡)、"emergency"(緊急事態)、"normal"(正常な決着)、"rules infraction"(反則)、"time forfeit"(時間切れ)、"unterminated"(継続中)等がある。

### その他

  - Annotator: 棋譜解説者の名前を示す。
  - Mode: どのような形式でこの対局が行われたかを示す。"OTB" (over the board:盤面を挟んだ直接対局)、"PM"(paper mail:手紙)、"EM" (electronic mail:Eメール)、"ICS" (Internet Chess Server:ネット対局)、"TC" (general telecommunication:その他通信手段)等がある。
  - PlyCount: この対局が何手で行われたかを示す。

ソフトによってはこれ以外に独自のタグをつけることもある。

## コメント

任意の場所にコメントを挿入することができる。セミコロン(;)の後は改行するまでコメントとなる。中カッコで囲んだ部分({...})もコメントとなる。ネストは許されない。つまり、コメントの中にコメントを書くことはできない。

## 例

以下は完全なPGNフォーマットの例を示す。

`[Event "F/S Return Match"]`
`[Site "Belgrade, Serbia JUG"]`
`[Date "1992.11.04"]`
`[Round "29"]`
`[White "Fischer, Robert J."]`
`[Black "Spassky, Boris V."]`
`[Result "1/2-1/2"]`
` `
`1.e4 e5 2.Nf3 Nc6 3.Bb5 {This opening is called Ruy Lopez.} a6 4.Ba4 Nf6`
`5.O-O Be7 6.Re1 b5 7.Bb3 d6 8.c3 O-O 9. h3 Nb8 10.d4 Nbd7 11.c4 c6`
`12.cxb5 axb5 13.Nc3 Bb7 14.Bg5 b4 15.Nb1 h6 16.Bh4 c5 17.dxe5 Nxe4`
`18.Bxe7 Qxe7 19.exd6 Qf6 20.Nbd2 Nxd6 21.Nc4 Nxc4 22.Bxc4 Nb6 23.Ne5`
`Rae8 24.Bxf7+ Rxf7 25.Nxf7 Rxe1+ 26.Qxe1 Kxf7 27.Qe3 Qg5 28.Qxg5 hxg5`
`29.b3 Ke6 30.a3 Kd6 31.axb4 cxb4 32.Ra5 Nd5 33. f3 Bc8 34.Kf2 Bf5 35.Ra7`
`g6 36.Ra6+ Kc5 37.Ke1 Nf4 38.g3 Nxh3 39.Kd2 Kb5 40.Rd6 Kc5 41.Ra6 Nf2`
`42.g4 Bd3 43.Re6 1/2-1/2`

## 変則チェス

駒の名前がアルファベット1文字で表せる限り、変則チェスの棋譜もPGNフォーマットを使って記録することができる。しかし、対応していないソフトウェアも多い。

## ファイルの拡張

PGNでは駒を複数の字で表したり、棋譜をどこまで再生したかなどを記録することは出来ない。また文字コードが[ISO/IEC 8859-1と規定されているため](https://ja.wikipedia.org/wiki/ISO/IEC_8859-1 "wikilink")\[1\]、日本語を挿入したりすると、ソフトによってはファイルを開けなくなることがある。そのため一部のデータベースソフトなどでは、PGNの他にソフト独自のファイルを組み合わせることで、これらを実現している。

## 脚注

## 外部リンク(英語)

  - [PGN specification by Steven J. Edwards (HTML by Thomas Stahl)](http://www.very-best.de/pgn-spec.htm)
  - [Portable Game Notation Specification and Implementation Guide, Steven J. Edwards](http://www.chessclub.com/help/PGN-spec)
  - [PGN Standards](http://www.saremba.de/chessgml/standards/pgn/pgn-complete.htm)
  - [PGN viewer](http://www.lutanho.net/pgn/pgnviewer.html)
  - [Online PGN viewer at ICC](http://www.chessclub.com/chessviewer/pgnform.html)

[Category:チェス](https://ja.wikipedia.org/wiki/Category:チェス "wikilink") [Category:コンピュータチェス](https://ja.wikipedia.org/wiki/Category:コンピュータチェス "wikilink") [Category:ファイルフォーマット](https://ja.wikipedia.org/wiki/Category:ファイルフォーマット "wikilink")

1.
> この記事は[Ed](https://ja.wikipedia.org/wiki/Ed)から翻訳されています。


**ed**（イーディー）は、[UNIX](../Page/UNIX.md "wikilink")オペレーティングシステム上の標準的な[テキストエディタ](../Page/テキストエディタ.md "wikilink")である。オリジナルの作者は[ケン・トンプソン](../Page/ケン・トンプソン.md "wikilink")で、世界初の[正規表現](../Page/正規表現.md "wikilink")の実装のひとつでもある（それ以前には正規表現は数学の論文に出ていただけであった）。edはケン・トンプソンの出身校である[カリフォルニア大学バークレー校](../Page/カリフォルニア大学バークレー校.md "wikilink")の[QEDから影響を受け](../Page/QED_\(テキストエディタ\).md "wikilink")、その後およびそこから派生した[vi](https://ja.wikipedia.org/wiki/vi "wikilink")に影響を及ぼした。UNIXコマンド[grep](https://ja.wikipedia.org/wiki/grep "wikilink")と[sedはedのよく使われる使い方に影響されており](https://ja.wikipedia.org/wiki/sed_\(コンピュータ\) "wikilink")（例えば[使用例の置換コマンドはsedの使用法にそっくりである](https://ja.wikipedia.org/wiki/#使用例 "wikilink")）、これらの影響はプログラミング言語[AWK](../Page/AWK.md "wikilink")の中にもよく見て取れる。

## 概要

edはその簡潔さで有名で、結果を表示するということがほとんどない。例えば、edがエラー検出時やセーブせずに終了してよいか確認するときに生成するメッセージは単に"?"である。現在のファイル名や行番号は表示されず、要求されない限りテキストに変更を加えた結果すら表示しない。このような簡潔さは初期のUNIXにとっては適切であった。というのも、コンソールは[テレタイプ端末](../Page/テレタイプ端末.md "wikilink")だったし、[モデム](https://ja.wikipedia.org/wiki/モデム "wikilink")は低速で、[ハードディスク](https://ja.wikipedia.org/wiki/ハードディスク "wikilink")や[メモリは高価だったからである](../Page/Random_Access_Memory.md "wikilink")。その処理の遅さは、文書の文字が表示される過程が見える程である。技術進歩によってこれらの制約がなくなるにつれて、より視覚的なエディタが標準となっていった。

最近ではedを対話的に使用することは滅多に無いが、[シェルスクリプト](../Page/シェルスクリプト.md "wikilink")で使われることはある。対話的使用に関しては、[1980年代](../Page/1980年代.md "wikilink")にsam、[vi](https://ja.wikipedia.org/wiki/vi "wikilink")、[Emacs](../Page/Emacs.md "wikilink")に取って代わられた。edは事実上全てのバージョンのUNIXと[Linux](../Page/Linux.md "wikilink")に装備されており、様々なバージョンのUNIXで作業する人にとっては便利である。問題が発生したとき、edは使用可能な唯一のエディタである場合もある。そのような場合に限ってedは対話的に使用される。

edのコマンド群は他のラインエディタで模倣されている。例えば初期の[MS-DOS](../Page/MS-DOS.md "wikilink")の[EDLIN](https://ja.wikipedia.org/wiki/EDLIN "wikilink")は似たような文法を採用しているし、多くの[MUD](../Page/MUD.md "wikilink")（[LPMud](https://ja.wikipedia.org/wiki/LPMud "wikilink")など）のテキストエディタもed風の文法を採用している。しかし、これらのエディタはedよりも一般に機能が限定されている。

[2008年](https://ja.wikipedia.org/wiki/2008年 "wikilink")[8月23日](../Page/8月23日.md "wikilink")、[GNUプロジェクト](../Page/GNUプロジェクト.md "wikilink")の開発によるedがバージョン1.0を迎えた\[1\]。

## 使用例

以下に ed を使用した例を示す。

`a`
`ed is the standard Unix text editor.`
`This is line number two.`
`.`
`2i`
`  `
`.`
`1,$l`
`ed is the standard Unix text editor.$`
`$`
`This is line number two.$`
`3s/two/three/`
`1,$l`
`ed is the standard Unix text editor.$`
`$`
`This is line number three.$`
`w text`
`65`
`q`

以上の結果として作成されるテキストファイルの内容は次の通りである。

`ed is the standard Unix text editor.`
`  `
`This is line number three.`

空ファイルの状態で開始し、*a* コマンド（ed のコマンドは全て1文字)でテキストの追加(append)を行う。これにより ed は入力状態(input mode)となり、その後の入力文字列をファイルに追加していき、1つのドットだけからなる行を入力することで終了となる。この例ではドットで入力を終了するまでに2行のテキストが入力された。*2i* コマンドも入力状態に移行するコマンドであり、2行目の前にテキストを挿入する（この例では空行を入力）。コマンドには数値を前につけることができ、操作するテキストの行番号を指定する。

*1,$l* の l はリスト(List)コマンドである。このコマンドは範囲指定が前に付けられており、二つの行番号をカンマで区切って指定する（*$* は最終行を意味する）。このコマンドを入力するとこれまでの入力内容が全て表示される。各行はドルマークで終わっており、各行末に空白が存在しても即座にわかるようになっている。

3行目の間違いは、置換(substitution)コマンド *3s/two/three/* で訂正できる。ここで *3* は訂正する行を示し、コマンドの後には置換元の文字列と置換先の文字列を指定する。再度全体を表示するために *1,$l* を使用すると、内容が修正されている。

*w text* はバッファの内容を "text" というファイルに書き込み、書き込んだ文字数を示す *65* という表示を出力する。*q* は ed の使用を終了する。

## ビル・ジョイと vi と ed

[エディタ戦争](../Page/エディタ戦争.md "wikilink")において、[Emacs](../Page/Emacs.md "wikilink")信奉者は「[ビル・ジョイ](../Page/ビル・ジョイ.md "wikilink")すら、もうviを使っていない」と言った。[1984年](../Page/1984年.md "wikilink")のインタビュー\[2\]において、ビル・ジョイはこのことについて説明している。そこで彼は[サン・マイクロシステムズ](../Page/サン・マイクロシステムズ.md "wikilink")内では初期のDTPソフト[Interleaf](https://ja.wikipedia.org/wiki/Interleaf "wikilink")を使い、サン以外の場所を訪れたときには古いedを使っていたと述べている。viはほとんどどこにでもあったが、それら(独自に修正が加えられた)ローカルバージョンのviは彼にとって期待通りに動くと信頼できなかったのである。一方でedは修正が加えられたことがないので思った通り動作することが期待できた。そこで彼は（しぶしぶながら）viを使わずにedを使ったというわけである。

## 脚注・出典

## 参考文献

  -
  -
## 関連項目

  - [エディタ戦争](../Page/エディタ戦争.md "wikilink")
  - [テキストエディタの一覧](https://ja.wikipedia.org/wiki/テキストエディタの一覧 "wikilink")
  - [vi](https://ja.wikipedia.org/wiki/vi "wikilink")

## 外部リンク

  - [GNU ed homepage](https://www.gnu.org/software/ed/ed.html)（英語）
  - [Unix Editors I](https://web.archive.org/web/20040825015310/http://snap.nlc.dcccd.edu/learn/nlc/ed.html)（英語）
  - [ed Humor](https://www.gnu.org/fun/jokes/ed-msg.html)（英語）
  - [Manpages of ED](https://linuxjm.osdn.jp/html/GNU_ed/man1/ed.1.html) JM Project （日本語）
  - [ed(1)](https://docs.oracle.com/cd/E19455-01/816-3518/6m9ptvqv5/index.html) man page（SunOS リファレンスマニュアル）
  - [ed(1)](https://nixdoc.net/man-pages/HP-UX/man1/ed.1.html) man page（HP-UX リファレンス）
  - [quiz(6) function ed-command の日本語訳](https://web.archive.org/web/20080820021643/http://www.bsddiary.net/quiz/)
      -
        ed(1) 好きなあなたに 53 の質問

[Category:テキストエディタ](https://ja.wikipedia.org/wiki/Category:テキストエディタ "wikilink") [Category:標準UNIXプログラム](https://ja.wikipedia.org/wiki/Category:標準UNIXプログラム "wikilink") [Category:1971年のソフトウェア](https://ja.wikipedia.org/wiki/Category:1971年のソフトウェア "wikilink")

1.
2.
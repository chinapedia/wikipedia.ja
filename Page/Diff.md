> この記事は[Diff](https://ja.wikipedia.org/wiki/Diff)から翻訳されています。


**diff**（ディフ）とは [ファイルの比較を行うための](https://ja.wikipedia.org/wiki/ファイル_\(コンピュータ\) "wikilink")[コマンドで](https://ja.wikipedia.org/wiki/コマンド_\(コンピュータ\) "wikilink")2つのファイル間の違いを出力できるプログラム。diffプログラムは[行](https://ja.wikipedia.org/wiki/行 "wikilink")単位で[テキストファイル](https://ja.wikipedia.org/wiki/テキストファイル "wikilink")間の差異を表示する。最近の実装では[バイナリファイル](https://ja.wikipedia.org/wiki/バイナリファイル "wikilink")もサポートしている。プログラムからの出力も「diff」（ディフ）と呼ばれるが出力をそのまま[`patch`](https://ja.wikipedia.org/wiki/patch "wikilink")プログラムで適用できるため、「**patch**」（**パッチ**）との呼称も一般的である。また、diffコマンド以外からの出力であっても差分表示プログラムの出力はdiffと呼ばれることがある。"[grep](https://ja.wikipedia.org/wiki/grep "wikilink")"が文字列探索そのものの代名詞になっているように、"diff"という語も差分検出一般を指す[ジャーゴン](https://ja.wikipedia.org/wiki/ジャーゴン "wikilink")となっている。

## 歴史

**diff**プログラムは1970年代初頭に、ニュージャージー州マーレイ・ヒルにあった[AT\&T](../Page/AT&T.md "wikilink")の[ベル研究所](../Page/ベル研究所.md "wikilink")で開発された[UNIX](../Page/UNIX.md "wikilink")上で開発されたもので、1974年のUNIX第5版に同梱され最初に公開された最終バージョンは[ダグラス・マキルロイ](https://ja.wikipedia.org/wiki/ダグラス・マキルロイ "wikilink")が開発したものであった。このバージョンのdiff実装については1976年にdiffの初期のプロトタイプ実装を行ったジェームズ・W・ハントとの共著による論文の中で研究成果として発表された。

マキロイの研究は[スティーブ・ジョンソン](https://ja.wikipedia.org/wiki/スティーブ・ジョンソン "wikilink")による[GCOS](https://ja.wikipedia.org/wiki/GCOS "wikilink")上の比較プログラムや[マイク・レスク](https://ja.wikipedia.org/wiki/マイク・レスク "wikilink")による**proof**プログラムの先行する研究の影響を受けたものだった。**proof**は元々UNIX上で開発されdiffのような行単位の変更箇所を出力するもので、行の挿入・削除を示すのにブラケット（\<、\>）による出力も用いられていた。これらの初期のアプリケーションでは[ヒューリスティクス](../Page/ヒューリスティクス.md "wikilink")が使われていたが、その出力の安定性は低いものだった。ファイル比較ツールの潜在的な有用性に触発されたマキロイはより頑健で様々な対象に使用でき、かつ[PDP-11](https://ja.wikipedia.org/wiki/PDP-11 "wikilink")のハードウェア的な制約上でもうまく動作するようなツールの研究、設計に取り組んだ。このアプローチによる研究にはベル研の同僚であった[アルフレッド・エイホ](../Page/アルフレッド・エイホ.md "wikilink")、エリオット・ピンソン、[ジェファーソン・ウルマン](https://ja.wikipedia.org/wiki/ジェファーソン・ウルマン "wikilink")、ハロルド・S・ストーンの研究者らとの協力を受けて取り組んだ。

Unixにおいては、[ed](https://ja.wikipedia.org/wiki/ed "wikilink")ラインエディタの利用が「編集スクリプト」機能という概念と自然に結びつくようなdiff機能を提供することとなった。edによる編集スクリプトと元ファイルとを両方保存しておけば、**ed**コマンドだけで変更後のファイルを完全に再構成できることになる。これを利用することによりファイルの複数改版履歴を保存するのに必要なディスク容量を相当減らすことができる。マキロイは元々様々な形式で出力できるようなdiffを作りその出力を処理できるようなポストプロセッサを作ろうと考えていたが、文法そのものをdiff形式として規定してしまい、さらにedコマンドが解釈できるような逆順入力に対応するようなdiffコマンドを実装する方がずっと単純で楽にできると判断した。1985年には[ラリー・ウォール](https://ja.wikipedia.org/wiki/ラリー・ウォール "wikilink")がこのdiff出力を入力として受け取ってファイルを変更するというアイデアを一般化、拡張して別コマンドとして[patch](https://ja.wikipedia.org/wiki/patch "wikilink")を作成した。

diffが作られてしばらくは、ソフトウェアコードや技術文書のマークアップのソース部分の変更箇所を比較する、プログラムのデバッグ出力の検証、ファイルシステム中のファイル一覧の比較といった使い方が一般的であった。**ed**用の出力により、ファイルへの一連の変更をひとまとめにしてファイル容量を節約するというアイデアが出てきた。[Source Code Control System](https://ja.wikipedia.org/wiki/Source_Code_Control_System "wikilink")（SCCS）はそのようなアイデアを実装したものとして1970年代後半に実装がなされた。

diffは概念的には[ザナドゥ計画](https://ja.wikipedia.org/wiki/ザナドゥ計画 "wikilink")（Project Xanadu）の思想を受けたものである。Xanaduは1960年に出現したハイパーテキストプロジェクトでその「相互参照ウィンドウ」機能に必要な履歴版の管理・追跡という概念を示していた。ファイルの相違点の提示はこの機能の一部としてより広い用語「[トランスクルージョン](https://ja.wikipedia.org/wiki/トランスクルージョン "wikilink")（transclusion）」に含まれていた。トランスクルージョンとはある文書が他の文書もしくは他の版の一部の中に含まれることを指す。

電子化時代の人文科学においては、コンピュータによる比較ツールは過去に大部で出版された文学作品に対しても用いられている。

## 使用法

以下のようにコマンドラインで2つのファイル名を指定して実行する。

`diff `*`original`*` `*`new`*

コマンドからの出力はファイル *original* をファイル *new* に変更するのに必要な箇所を示す。

*original* と *new* がディレクトリを指していた場合diffは両ディレクトリに存在するファイル個々について実行されることになる。オプション`-r`を指定するとさらにサブディレクトリ以下を全て辿りディレクトリ内のファイル間についての差分を出力する。

## 利用例

以下、2つのファイル（*original* と *new*）を例に説明する:  *original*:

**`1`**`  This part of the`
**`2`**`  document has stayed the`
**`3`**`  same from version to`
**`4`**`  version.  It shouldn't`
**`5`**`  be shown if it doesn't`
**`6`**`  change.  Otherwise, that`
**`7`**`  would not be helping to`
**`8`**`  compress the size of the`
**`9`**`  changes.`
**`10`**` `
**`11`**` This paragraph contains`
**`12`**` text that is outdated.`
**`13`**` It will be deleted in the`
**`14`**` near future.`
**`15`**` `
**`16`**` It is important to spell`
**`17`**` check this dokument. On`
**`18`**` the other hand, a`
**`19`**` misspelled word isn't`
**`20`**` the end of the world.`
**`21`**` Nothing in the rest of`
**`22`**` this paragraph needs to`
**`23`**` be changed. Things can`
**`24`**` be added after it.`

*new*:

**`1`**`  This is an important`
**`2`**`  notice! It should`
**`3`**`  therefore be located at`
**`4`**`  the beginning of this`
**`5`**`  document!`
**`6`**`  `
**`7`**`  This part of the`
**`8`**`  document has stayed the`
**`9`**`  same from version to`
**`10`**` version.  It shouldn't`
**`11`**` be shown if it doesn't`
**`12`**` change.  Otherwise, that`
**`13`**` would not be helping to`
**`14`**` compress anything.`
**`15`**` `
**`16`**` It is important to spell`
**`17`**` check this document. On`
**`18`**` the other hand, a`
**`19`**` misspelled word isn't`
**`20`**` the end of the world.`
**`21`**` Nothing in the rest of`
**`22`**` this paragraph needs to`
**`23`**` be changed. Things can`
**`24`**` be added after it.`
**`25`**` `
**`26`**` This paragraph contains`
**`27`**` important new additions`
**`28`**` to this document.`

コマンド `diff original new` を実行すると、以下の通常のdiff出力が生成される:

``` diff
0a1,6
> This is an important
> notice! It should
> therefore be located at
> the beginning of this
> document!
>
8,14c14
< compress the size of the
< changes.
<
< This paragraph contains
< text that is outdated.
< It will be deleted in the
< near future.
---
> compress anything.
17c17
< check this dokument. On
---
> check this document. On
24c24,28
< be added after it.
---
> be added after it.
>
> This paragraph contains
> important new additions
> to this document.
```

この伝統的な出力形式では、**a** は追加（*added*）、**d** は削除（*deleted*）、**c** は変更（*changed*）を意味する。a/d/cの各文字の前には元ファイルでの行番号が書かれ、後ろに変更後ファイルでの行番号が出力される。行頭の[山括弧](https://ja.wikipedia.org/wiki/山括弧 "wikilink")はその行が追加されたのか、または削除されたのかを示している。追加行とは新しいファイルで新たに出現した部分、つまり元のファイルに付け加えられた部分のことで、削除行は新しいファイルでは無くなった、つまり元ファイルから除かれた行のことを指す。

標準では新旧両ファイルに共通する箇所は出力されない。行を移動した場合は新しい場所へは追記として示され、以前の箇所では削除行として示される。

## 変種

大半のdiff実装の仕様は1975年以来ほとんど変わらずにそのままである。主な変更点としてはコアアルゴリズムの改良、コマンドとして便利な機能の追加、新出力形式の設計がある。基本的なアルゴリズムは論文 "An O(ND) Difference Algorithm and its Variations"（Eugene W. Myers著）および "A File Comparison Program" （Webb Miller and Myers著）で説明されている。このアルゴリズムはこれとは別に独立してE.ウッコネンが発見して、 "Algorithms for Approximate String Matching" （E. Ukkonen著）において説明している。diffプログラムの最初のバージョンはテキストファイルの行単位での比較用に設計された。ここでの行は[改行コード](https://ja.wikipedia.org/wiki/改行コード "wikilink")によって区切られていることを前提としていた。1980年までにはバイナリファイルへの対応も加えられた。

ポストプロセッサ **sdiff** は個々のdiff項目を並べて出力するものであり、 **diffmk** の方は印刷文書に変更箇所マークを挿入するためのものである。両者とも1981年以前にベル研外で開発されたものである。

[Berkeley distribution of Unix](../Page/BSD.md "wikilink") ではコンテキスト形式（-C）の追加とファイルシステム中のディレクトリ構造を辿る機能（-r）が加わった。これらの機能は1981年7月にリリースされた2.8BSDから加わった。とりわけバークレーでコンテキスト形式が開発されたことによって、微細な変更が行われただけのソースコードへの改変をパッチの形で配布するような活動ができるようになった。

[diff3](https://ja.wikipedia.org/wiki/diff3 "wikilink")コマンドは1ファイルを他の2つのファイルと比較する。これは1つのソースファイルを2人の人が変更したものを処理するためポール・ジェンセンが最初に開発した。直接実行されることはあまりなく大半は[merge](https://ja.wikipedia.org/wiki/merge "wikilink")プログラムから呼び出されて起動される。同様に、他の多くの[履歴管理システム](https://ja.wikipedia.org/wiki/履歴管理システム "wikilink")でも内部的に使われている。

Wdiffはテキスト中の単語単位・フレーズ単位での変更を見るためのツールであり、特に行折り返しや表幅などに相違がある場合に効果を発揮する\[1\]。Spiff はさらに、浮動小数の精度桁数の違いやプログラムファイルでの空白やコメントなどを無視した比較ができる\[2\]。

### コンテキスト形式（Context format）

「コンテキスト形式」の出力では変更された行部分に加えてその前後の変更されていない数行も示される。この呼称は、変更されていない行を加えることが「文脈（コンテキスト）」をパッチに与えることによる。この出力形式が[patch](https://ja.wikipedia.org/wiki/patch "wikilink")プログラムへの入力として使用される。また人間にとってもこの形式は読みやすく、パッチの適用にも適している。2ファイル間で変更のなかった箇所の行も出力されるため変更後のファイルでの変更箇所を特定するのが容易になる。これにより行番号の対応が取れなかったとしても変更点を追いやすくなり、変更を適用すべきかどうかの判断も行いやすくなる。

「変更内容の出力部」の上下に出力される変更のなかった行を何行分表示されるかはユーザが指定でき、全く出力しない「0」指定も可能であるが、標準では3行が出力される。変更箇所提示部において非変更行のコンテキストが隣接する変更箇所部分と重なる場合は、非変更箇所を2重に提示することはせず変更箇所を一つにまとめて提示する。

「\!」から始まる行は2ファイル間での変更があった行、「+」から始まる行は行の挿入、行頭がスペースから始まる行は非変更行を示す。パッチの先頭行にはファイルの[パスや](https://ja.wikipedia.org/wiki/ファイル名 "wikilink")[タイムスタンプ](https://ja.wikipedia.org/wiki/タイムスタンプ "wikilink")といったファイルに関する情報が書かれる。各変更箇所の先頭にはそれぞれのファイルにおける変更箇所の対応行番号が書かれる。3つのアスタリスク（\*\*\*）から始まる行では変更前ファイルでの行番号に対応する数字が出力され、3つのダッシュ（---）から始まる行では変更後ファイルでの行番号が出力される。出力行番号の数値はそれぞれのファイルにおける変更箇所の先頭行の行番号と先頭行からの行数を示す。

`diff -c original new`というコマンドを実行した際は、以下のような出力が行われる。

``` diff
*** /path/to/original ''timestamp''
--- /path/to/new      ''timestamp''
***************
*** 1,3 ****
--- 1,9 ----
+ This is an important
+ notice! It should
+ therefore be located at
+ the beginning of this
+ document!
+
  This part of the
  document has stayed the
  same from version to
***************
*** 5,20 ****
  be shown if it doesn't
  change.  Otherwise, that
  would not be helping to
! compress the size of the
! changes.
!
! This paragraph contains
! text that is outdated.
! It will be deleted in the
! near future.

  It is important to spell
! check this dokument. On
  the other hand, a
  misspelled word isn't
  the end of the world.
--- 11,20 ----
  be shown if it doesn't
  change.  Otherwise, that
  would not be helping to
! compress anything.

  It is important to spell
! check this document. On
  the other hand, a
  misspelled word isn't
  the end of the world.
***************
*** 22,24 ****
--- 22,28 ----
  this paragraph needs to
  be changed. Things can
  be added after it.
+
+ This paragraph contains
+ important new additions
+ to this document.
```

### ユニファイド形式 (Unified format)

ユニファイド形式（*unified format*、*unidiff*とも呼ぶ）はコンテキスト形式における技術的改良を継承し、より少量の出力でより読みやすい形式を追求し生まれた。通常、ユニファイド形式は「-u」[オプション](https://ja.wikipedia.org/wiki/オプション "wikilink")により指定される。この出力形式は[patch](https://ja.wikipedia.org/wiki/patch "wikilink")プログラムへの入力形式として使われることが多い。現在、多くのプロジェクトにおいてdiff出力によるパッチを投稿する際にはこのユニファイド形式を使うよう推奨している。このため、このユニファイド形式がソフトウェア開発者の間でのいわば共通形式となっている。

ユニファイド形式diffを最初に開発したのはウェイン・デイヴィソンで、1990年8月のことであった（comp.sources.miscのVolume 14に**unidiff**として投稿）。[リチャード・ストールマン](../Page/リチャード・ストールマン.md "wikilink")が[GNUプロジェクト](../Page/GNUプロジェクト.md "wikilink")のdiffコマンドにこの機能を1ヶ月後に加え、1991年1月リリースの**GNU diff** 1.15から使えるようになった。GNU diffではその後任意の形式のdiff出力を扱えるようコンテキスト出力サポートの拡張が進められた。GNU diffおよびdiff3は現在他のdiff系ツールや[patch](https://ja.wikipedia.org/wiki/patch "wikilink")系ツールと共に**diffutils**パッケージに含まれている。[Emacs](../Page/Emacs.md "wikilink")には[Ediff](https://ja.wikipedia.org/wiki/Ediff "wikilink")ツールとしてパッチが変更する内容を表示しユーザが動的にパッチファイルの変更点を編集・マージすることができるインタフェースを持っている。

ユニファイド出力形式ではヘッダの2行はコンテキスト形式と同一のもので始まるものの、元ファイルは「---」で示され新ファイルは「+++」で示される。これに続く変更箇所ではファイル間の相違が示されるが、非変更箇所は「 」(スペース)、挿入行は「+」、削除行は「-」で始まる行で示される。

変更箇所ではその範囲を示す行番号・行数の情報に続いて行の挿入・削除、非変更箇所などが出力される。範囲を示す情報は2つの[@](https://ja.wikipedia.org/wiki/@ "wikilink")マークで囲まれて出力され、前述のコンテキスト出力で示された内容は1行にまとめられた形で出力される。変更箇所の範囲情報の出力形式を以下に示す:

`@@ -R +R @@`

変更箇所の範囲情報は2つの範囲についての情報を含んでいる。一方はマイナス記号が頭に付いた元ファイルにおける変更箇所を示すものであり、もう一方はプラス記号が頭に付いた変更後のファイルにおける変更箇所を示している。範囲を示す*R*は*l,s*という形式となり、*l*は変更箇所の開始行、*s*はそれぞれのファイルにおける変更箇所の行数を示している。GNU diffの大半のバージョンでは、*R*において*s*がデフォルトの1である場合にはカンマ以降を省略した形式も使える。

元ファイルの変更箇所の範囲を示す情報では非変更箇所行・削除行についての行数分も含んだ情報が提示される。一方、変更後ファイルにおける範囲情報でも非変更箇所行・挿入行の分も含んだ情報が出力される。変更箇所における行数と範囲情報が示している行数が一致しない場合、その出力は不正な形式として拒絶される。

ある行が変更された場合、削除+挿入として表現される。元ファイルと変更後ファイルの変更箇所が同一の場所に現われ相互に隣り合って出力されることになる。以下のその一例を示す。

`-check this dokument. On`
`+check this document. On`

`diff -u original new`というコマンドを実行した際は、以下のような出力が行われる。:

``` diff
--- /path/to/original ''timestamp''
+++ /path/to/new      ''timestamp''
@@ -1,3 +1,9 @@
+This is an important
+notice! It should
+therefore be located at
+the beginning of this
+document!
+
 This part of the
 document has stayed the
 same from version to
@@ -5,16 +11,10 @@
 be shown if it doesn't
 change.  Otherwise, that
 would not be helping to
-compress the size of the
-changes.
-
-This paragraph contains
-text that is outdated.
-It will be deleted in the
-near future.
+compress anything.

 It is important to spell
-check this dokument. On
+check this document. On
 the other hand, a
 misspelled word isn't
 the end of the world.
@@ -22,3 +22,7 @@
 this paragraph needs to
 be changed. Things can
 be added after it.
+
+This paragraph contains
+important new additions
+to this document.
```

diff出力形式の中には特定のプログラムや一定の利用法の中で変更や拡張が加えられているものもある。例えば[バージョン管理システム](../Page/バージョン管理システム.md "wikilink")では、diffのヘッダ出力部分のタイプスタンプの箇所に版番号・バージョン番号や「ワーキングコピー」その他のコメント類を出力する場合もある。また複数のdiff出力を一つにまとめた形式が使えるものもある。この場合各変更ファイルのヘッダとして以下のような形式が使われる。:

``` diff
 Index: path/to/file.cpp
 ===================================================================
```

## 実装

### GNU Diffutils

[GNU](../Page/GNU.md "wikilink")ではDiffutilsパッケージが製作されている。この中には、以下のものが含まれている。

  - [cmp](https://ja.wikipedia.org/wiki/cmp "wikilink")
  - diff
  - [diff3](https://ja.wikipedia.org/wiki/diff3 "wikilink")
  - [patch](https://ja.wikipedia.org/wiki/patch "wikilink")

## 脚注

<references/>

## 関連項目

  - [編集距離](https://ja.wikipedia.org/wiki/編集距離 "wikilink")
  - [差分符号化](https://ja.wikipedia.org/wiki/差分符号化 "wikilink")
  - [rsync](https://ja.wikipedia.org/wiki/rsync "wikilink")
  - [マージ (バージョン管理システム)](https://ja.wikipedia.org/wiki/マージ_\(バージョン管理システム\) "wikilink")

## 参考文献

  -
  -
  -
  -
  -
  -
  - [diff.c （ソースコード）](http://www.ioplex.com/~miallen/libmba/dl/src/diff.c) - MyersのSES/LCSアルゴリズムにHirschbergの改良アルゴリズムを加えた一般的な実装

  - [Unified Diff Format](https://www.artima.com/weblogs/viewpost.jsp?thread=164293) by [Guido van Rossum](https://ja.wikipedia.org/wiki/グイド・ヴァンロッサム "wikilink"), June 14, 2006

## 外部リンク

  - [GNU Diff utilities](https://www.gnu.org/software/diffutils/diffutils.html) - [Free Software Foundation提供](https://ja.wikipedia.org/wiki/Free_Software_Foundation "wikilink")
  - [オンライン版*diff*プログラム](http://www.iconv.com/diff.htm)
  - [difff《ﾃﾞｭﾌﾌ》](https://difff.jp/) - 日本語対応で簡単に差分が確認できるテキスト比較ツール
  - [diffj](https://github.com/jpace/diffj) - [Java](https://ja.wikipedia.org/wiki/Java "wikilink")用のdiffライブラリ

[Category:標準UNIXプログラム](https://ja.wikipedia.org/wiki/Category:標準UNIXプログラム "wikilink") [Category:1974年のソフトウェア](https://ja.wikipedia.org/wiki/Category:1974年のソフトウェア "wikilink") [Category:オープンソースソフトウェア](https://ja.wikipedia.org/wiki/Category:オープンソースソフトウェア "wikilink") [Category:ファイル比較ツール](https://ja.wikipedia.org/wiki/Category:ファイル比較ツール "wikilink") [Category:データ差分](https://ja.wikipedia.org/wiki/Category:データ差分 "wikilink")

1.  <http://www.gnu.org/software/wdiff/wdiff.html>
2.  <http://hpux.cs.utah.edu/hppd/hpux/Text/spiff-1.0>
> この記事は[ROT13](https://ja.wikipedia.org/wiki/ROT13)から翻訳されています。


[right](https://ja.wikipedia.org/wiki/ファイル:ROT13.png "wikilink") **ROT13** または **ROT-13**、**rot13** は[単換字式暗号](https://ja.wikipedia.org/wiki/単換字式暗号 "wikilink")（[シーザー暗号](../Page/シーザー暗号.md "wikilink")）の一つである。アルファベットを一文字毎に13文字後のアルファベットに置き換える。<span style="font-family:monospace;">A</span>は <span style="font-family:monospace;">N</span>に、 <span style="font-family:monospace;">B</span> は <span style="font-family:monospace;">O</span> に置き換えられ、以下同様である。英語の "**Rot**ate by **13** places" の略。ネットワーク上のやりとり（電子掲示板、ネットニューズ、フォーラム等）で[冗談の](https://ja.wikipedia.org/wiki/ジョーク "wikilink")[落ち](../Page/落ち.md "wikilink")、パズルの解法、ネタばれ情報、不快表現等を隠すのに用いられる変換である。暗号化と復号の両方が全く同じ変換であるという特徴がある。実際のところ、（現代の感覚では）全く「暗号」というほどのものではないが、ちょっと見に読んでしまうという事態は避けられる。雑誌などでクイズの正解を上下逆さまに印刷したりするのが見られるが、それと似たようなものである。

以下、「文字」は特記しない限りローマ字のアルファベットを指す。

## 概要

**ROT13**という呼称は1980年代の初めに[Usenet](https://ja.wikipedia.org/wiki/Usenet "wikilink")で用いられ始め、[デファクトスタンダード](../Page/デファクトスタンダード.md "wikilink")となった。英語のアルファベットを、その並び順で26文字のちょうど半分である13文字ぶんずらすものである。暗号と言えないこともないが、強度は無きに等しい。アルファベット文字のみが対象であるため、それ以外の文字を暗号化するのには使えず、もし対象を広げたい場合は他の手法が必要である。

## 方法

ROT13を適用するには、文章中の各文字をとりあげ、アルファベット順に13番後の文字に置き換える。Zを超えた場合はAに戻って数える。一般に、大文字小文字の関係は保存するという実装が多い。<span style="font-family:monospace;">a</span> は <span style="font-family:monospace;">n</span>、 <span style="font-family:monospace;">B</span> は <span style="font-family:monospace;">O</span>、以下同様に <span style="font-family:monospace;">Z</span>は <span style="font-family:monospace;">M</span>になる。数字、記号等はそのまま残す。ラテンアルファベットには26 (= 2 × 13 ) 文字あるので、ROT13変換を二回行うと元に戻る。つまりROT13を関数とみると、自分自身の逆関数となっている:

\[\mbox{ROT}_{13}(\mbox{ROT}_{13}(x))=\mbox{ROT}_{26}(x)=x\], for any text *x*.

数学では変換のこの種の性質を[対合](../Page/対合.md "wikilink")と呼ぶことがある。

### 対照表による実装

以下のようなルックアップテーブルを用いると簡単に変換することができる。

|                                                      |
| ---------------------------------------------------- |
| ABCDEFGHIJKLMNOPQRSTUVWXYZabcdefghijklmnopqrstuvwxyz |
| NOPQRSTUVWXYZABCDEFGHIJKLMnopqrstuvwxyzabcdefghijklm |
|                                                      |

例えば次のような文章を隠したいとする:

`How can you tell an extrovert from an`
`introvert at `[`NSA`](../Page/アメリカ国家安全保障局.md "wikilink")`? In the elevators,`
`the extroverts look at the OTHER guy's shoes.`

（[NSAで外向的な人と内向的な人とをどうやって見分ければいいか](../Page/アメリカ国家安全保障局.md "wikilink")。エレベーターの中で他人の靴を見ているならそれは外向的な人である。)

ROT13を用いると、 次のようになる。

`Ubj pna lbh gryy na rkgebireg sebz na`
`vagebireg ng AFN? Va gur ryringbef,`
`gur rkgebiregf ybbx ng gur BGURE thl'f fubrf.`

もう一度ROT13を用いると、元の文字列に戻る。

## 歴史

ROT13 は1980年代初めに[ネットニューズの](../Page/ネットニュース.md "wikilink")[ニューズグループ](https://ja.wikipedia.org/wiki/ニューズグループ "wikilink")の一つ [net.jokes](http://groups.google.com/group/net.jokes) から始まった（[\#脚注](https://ja.wikipedia.org/wiki/#脚注 "wikilink")参照）。一部の購読者に不快をもたらす冗談を隠す手段として、あるいは単に冗談の落ちをうっかり読ませないために一時的に隠す手段として、自発的に用いられるようになった。一旦は不快な冗談を特定のニューズグループに隔離しようとしたのだが、専用の場所などを用意するとその種の投稿を大目に見ていると思われると恐れたサイト管理者の反対にあって失敗した。ROT13は単純さの故に優れた解決法だった。

一般的でない文字はニューズリーダに誤動作を惹起することがあったが、ROT13はアルファベットの文字を他のアルファベットの文字に置換するだけの方法なので、ニューズリーダに問題をもたらすことがなかった。ローテートする数として他でもない13が選ばれたのはエンコーディングとデコーディングを同じ方法でできる数が13のみだったからである。これは26文字からなる言語のみで有効であって、ポーランド語のように26を超える文字を持つ場合やハワイ語のように26未満の場合は条件が異なる。たまたま英語が26文字を使用しているので、例えばROT-**15**ではなくROT-13が好ましかったのである。

エンコードやデコードを手で行うこともできるが、計算機プログラムに行わせるほうが便利である。[UNIX](../Page/UNIX.md "wikilink")には**[tr](../Page/Tr_\(UNIX\).md "wikilink")** (transliterate) という[ユーティリティ](https://ja.wikipedia.org/wiki/ユーティリティ "wikilink")があり、次のように使うとROT13のエンコーディングができる。

  -
    `tr A-Za-z N-ZA-Mn-za-m`

ニューズリーダに自動復号機能が組み込まれるのに時間はかからなかった。1990年代の初めから、[FidoNet](../Page/FidoNet.md "wikilink")のフォーラムでもROT13が用いられるようになったので、FidoNetのメーラにもROT13自動暗号／復号機能が含まれることがしばしばである。

## 暗号技術としてのROT13

ROT13を[暗号](../Page/暗号.md "wikilink")としてみると、古典的な暗号である「シーザー暗号」という単換字式暗号の一種に属する。真面目にセキュリティーを求める場合には用いられない。一定のシフト値 (13) を用いるため、[暗号鍵なしで簡単に解読することができる](../Page/鍵_\(暗号\).md "wikilink")。解読するにはROT13が用いられているということさえわかればいい。それどころか、ROT13が使われていることがわからなくても、他の単換字式暗号と同様、（[エドガー・アラン・ポー](../Page/エドガー・アラン・ポー.md "wikilink")の『黄金虫』に出てくるような）頻度分析やパターンとなる語 (pattern word) の追求だけで解読できる。

ROT13の実際の効果は、読者が自覚的にソフトを操作するなどして（ROT13復号コマンドを実行する等）読まなければならないという点である。信書を権利のない読み手から守ることではなく、うっかり読者の目に入ってしまうことを避けるための安全装置として、書籍や映画のネタばれ批評のような場合に用いられる。

セキュリティーを求める用途にはあまりに不適なため、ROT13は弱い暗号の代名詞として用いられるようになった。たとえば「今日では、56ビットのDESはROT13並だ」等。「二重ROT13」「ROT26」「2ROT13」（要するに全然暗号化していない平文のこと）という用語もユーモアを込めて用いられる。中には贋学術論文をでっちあげた人までいる（"On the 2ROT13 Encryption Algorithm" [(PDF)](http://phoenix.clifford.at/~ak/2rot13.pdf)）。ROT26は[アメリカ合衆国](https://ja.wikipedia.org/wiki/アメリカ合衆国 "wikilink")の[デジタルミレニアム著作権法](../Page/デジタルミレニアム著作権法.md "wikilink") (DMCA) をからかうためにも用いられた。あるネットワークユーザ達はネットワーク上のフォーラムに投稿する文章に「この文書はROT26で暗号化されている。回避操作は告訴対象である」 ("Encoded with ROT26 — circumvention will be prosecuted\!") という警告文をつけた。DMCAは複製防止システムを回避する事（コピーガード外し）を広範に禁止したが、複製防止システムの中にはもともとセキュリティー的に甘い暗号を用いたものがしばしば見られるのである。[トリプルDES](../Page/トリプルDES.md "wikilink")にからんで「三重ROT13」も時折見る。もちろんROT13そのものである。

2001年にロシア人暗号研究者のドミトリ・スクリャーロフ (Dmitry Sklyarov) が逮捕された。[eBook](https://ja.wikipedia.org/wiki/eBook "wikilink")の複製防止システムの弱点について詳細を発表した後のことであった。eBookはデジタル的な（電気的な）書物のフォーマットであるが、著作権を守るための技術的手段を含むことがある。eBook出版社の一つ、New Paradigm Research Group (NPRG) は自分たちの報告書を暗号化する方法としてROT13を用いていた。アドビはeBookソフトウェア開発キット (SDK) にROT13を用いた玩具的例題を含めているが、NPRGがこれを誤解して、ROT13をまともな暗号法とでも思ったのだろう ( [1](http://techupdate.zdnet.com/techupdate/stories/main/0,14179,2801118-2,00.html)) 。

## 豆知識

<table>
<tbody>
<tr class="odd">
<td><table>
<tbody>
<tr class="odd">
<td><p>abcdefghijklmnopqrstuvwxyz</p></td>
</tr>
<tr class="even">
<td><p>NOPQRSTUVWXYZABCDEFGHIJKLM</p></td>
</tr>
<tr class="odd">
<td></td>
</tr>
</tbody>
</table></td>
</tr>
<tr class="even">
<td><p>aha ↔︎ nun</p></td>
</tr>
<tr class="odd">
<td><p>balk ↔︎ onyx</p></td>
</tr>
<tr class="even">
<td><p>barf ↔︎ ones</p></td>
</tr>
<tr class="odd">
<td><p>bin ↔︎ ova</p></td>
</tr>
<tr class="even">
<td><p>envy ↔︎ rail</p></td>
</tr>
<tr class="odd">
<td><p>errs ↔︎ reef</p></td>
</tr>
<tr class="even">
<td><p>fur ↔︎ she</p></td>
</tr>
<tr class="odd">
<td><p>gnat ↔︎ tang</p></td>
</tr>
<tr class="even">
<td><p>clerk ↔︎ pyrex</p></td>
</tr>
</tbody>
</table>

ROT13は文字遊びの素材としても用いることができる。単語によっては、ROT13変換した結果もまた意味をもつ単語になることがある。この種の単語の中で英語で知られている最長のものは7文字の<span style="font-family:monospace;">abjurer</span> と <span style="font-family:monospace;">nowhere</span>の組、 <span style="font-family:monospace;">chechen</span> と <span style="font-family:monospace;">purpura</span> の組である。他の例は表に示した。

ROT13変換で逆転する綴りもある。<span style="font-family:monospace;">ravine</span> をROT13変換すると <span style="font-family:monospace;">enivar</span>になる。後者は英単語ではないが、丁度逆転する。普通の英単語では <span style="font-family:monospace;">gnat</span> と <span style="font-family:monospace;">tang</span>の組だけが知られている（「ブヨ」と「舌」）。

ROT13変換しても意味が変わらないものもある。<span style="font-family:monospace;">vex</span> は同義語の <span style="font-family:monospace;">irk</span> になる（「うんざりさせる」）。<span style="font-family:monospace;">terra</span> と <span style="font-family:monospace;">green</span>の組もお似合いである。

1989年の [International Obfuscated C Code Contest](https://ja.wikipedia.org/wiki/IOCCC "wikilink") (IOCCC) （国際多義Cコードコンテスト）で受賞した Brian Westleyの例がある。WetleyのソースコードはROT13変換しても逆転しても正常にコンパイルできた。しかも生成されたオブジェクトコードはROT13変換または入力を逆順にするプログラムとして動作した（ [2](http://www.ioccc.org/1989/westley.c)、[3](http://www.ioccc.org/1989/westley.hint)）。

ニューズグループ alt.folklore.urban は <span style="font-family:monospace;">furrfu</span>という単語を生んだ。これはよくエンコードされるつぶやき "sheesh" （「ちぇっ」「へっ」「をいをい」） のROT13変換である。 "<span style="font-family:monospace;">Furrfu</span>"が生まれたのは1992年の半ばである。同グループに対し[都市伝説](https://ja.wikipedia.org/wiki/都市伝説 "wikilink")にまつわる記事が繰り返し投稿された。新参者に対するこの手のつぶやきが多数投稿されると、購読者の中には「Sheesh\!と言い過ぎだ」と主張する人々が出てきた。そこで現れたのが問題の投稿であった（ [4](http://foldoc.doc.ic.ac.uk/foldoc/foldoc.cgi?furrfu)）。

## 変法

例数は少ないが、ROT13に類似した他の方法が同様の目的で用いられることがある。ROT13は文字だけを変換し、数字や空白は変換しない。そのため、例えば謎解きの答えが数字である場合や、任意の二進データを扱う場合には不適当である。

### ROT47

**ROT47** はROT13の変種で、基本的なアルファベットだけではなく、数字や他の多くの記号も変換する。ROT47はローテートするのにA-Zの範囲だけではなく、ASCIIで定義された文字コードのうちより広い範囲を用いる。ASCIIでは 0 - 127 の数を用いてアルファベットの文字、数字、句点他の通常用いられる記号をマップしている。ASCIIコードで見ると、ROT13は 65 - 90及び97 - 122の範囲をカバーしている。一方ROT47は <span style="font-family:monospace;">\!</span> （[感嘆符](https://ja.wikipedia.org/wiki/感嘆符 "wikilink")、ASCIIコード 33）から <span style="font-family:monospace;">\~</span> （[波線](https://ja.wikipedia.org/wiki/波線 "wikilink")、ASCIIコード 126） をカバーし、47文字ローテートする。用いられる文字コードの範囲が広いので、ROT47の結果はROT13よりさらにわけがわからない印象になる。しかしROT47はROT13に比べ、はるかにサポートされていない。

先ほどの例をROT47変換すると:

`w@H 42? J@F E6== 2? 6IEC@G6CE 7C@> 2?`
`:?EC@G6CE 2E }$pn x? E96 6=6G2E@CD[`
`E96 6IEC@G6CED =@@< 2E E96 ~%wt# 8FJVD D9@6D]`

となる。UNIXコマンド **tr** によってROT47変換するには:

  -
    `tr '!-~' 'P-~!-O'`

とする。

#### Pascalによる原理的実装

以下は変換アルゴリズムに従って[Pascal](../Page/Pascal.md "wikilink")で記述した例である。文字コードはASCIIであることを前提としている。

    procedure ROT47Codec(var s : CharString; len : integer);
    var i : integer;

      function ROT47(c : char) : char;
      var ic : integer;
      begin
        if c in ['!'..'~'] then begin
           ic := ord(c) - ord('!');
           ic := (ic  + 47) mod 94 + ord('!');
          ROT47 := chr(ic)
        end else
          ROT47 := c
      end;

    begin
      for i := 1 to len do s[i] := ROT47(s[i])
    end;

CharString型 は文字列を格納するための添字が1から始まる適当な長さの char 型変数の配列である。s に文字列そのもの、lenには文字列の長さを入れる。前述のように、この手続きは暗号化、復号両方に用いることができる。

### memfrob()関数

[GNU C ライブラリ](https://ja.wikipedia.org/wiki/GNU_C_ライブラリ "wikilink")（計算機プログラミング用に用意された標準的なルーチンの集合）には **`memfrob()`** という名前の関数がある ([5](http://www.gnu.org/software/libc/manual/html_node/Trivial-Encryption.html))。このルーチンはROT13と同じ目的で用いられるが、任意の二進データに利用可能である（ユーモアをこめて、「意味不明化」([:en:frobnicate](https://ja.wikipedia.org/wiki/:en:frobnicate "wikilink"))関数と呼ばれる）。このルーチンではデータの各8-bitバイトをとり、二進数の00101010（十進表記では42。[生命、宇宙、そして万物についての究極の疑問の答え](https://ja.wikipedia.org/wiki/生命、宇宙、そして万物についての究極の疑問の答え "wikilink")参照）との間のビット毎の[排他的論理和](../Page/排他的論理和.md "wikilink") (XOR) を計算する。この手法は単純な排他的論理和による暗号法[:en:simple XOR cipherで](https://ja.wikipedia.org/wiki/:en:simple_XOR_cipher "wikilink")、やはり弱い。ROT13と同様、再度適用すると元のデータが得られる。

## 脚注

GoogleのUSENETアーカイブを検索すると、初期のROT13利用例として1982年10月8日にニューズグループ <span style="font-family:monospace;">net.jokes</span> に投稿されたものが見つかる（ [6](http://groups.google.com/groups?selm=bnews.desoto.299)[7](http://groups.google.com/groups?selm=bnews.utcsrgv.596)）。

## 参考文献

  - Eric S. Raymond (Editor), the [Jargon File](https://ja.wikipedia.org/wiki/Jargon_File "wikilink"), [8](http://www.catb.org/~esr/jargon/html/R/rot13.html).
  - [ブルース・シュナイアー](https://ja.wikipedia.org/wiki/ブルース・シュナイアー "wikilink")著,[山形浩生](../Page/山形浩生.md "wikilink")監訳,『暗号技術大全』,ソフトバンク,2003年6月6日,12ページ,ISBN 4-7973-1911-9 （原書：Bruce Schneier, Applied Cryptography, 2nd edition, Wiley, 1996, p11. ISBN 0-471-11709-9）

## 関連項目

  - [シーザー暗号](../Page/シーザー暗号.md "wikilink")
  - [暗号解読](https://ja.wikipedia.org/wiki/暗号解読 "wikilink")

## 外部リンク

  - [Google online ROT13 encoder/decoder](http://rot13page.googlepages.com/)
  - [Words with interesting properties under ROT13](http://www.furrfu.org/rot13words.html)
  - [Online ROT13 encoder](http://www.rot13.com/)
  - [Another online ROT13 encoder/decoder in JavaScript](http://tools.geht.net/rot13.html)
  - [Bilingual (Portuguese/English) page with explanations, links and software information](http://www.dantas.com/rot13)
  - [ROT13 Bookmarklet](http://www.squarefree.com/bookmarklets/pagedata.html#rot13_selection)
  - [Software for ROT13 in a large number of languages](http://www.miranda.org/~jkominek/rot13/) — includes a patch to [SSH](../Page/Secure_Shell.md "wikilink") to add support for ROT13, and a cryptanalysis tool to automatically distinguish ROT13 text from plaintext.
  - [A description of ROT13](http://www.everything2.org/index.pl?node=ROT13) — on the [Everything2](https://ja.wikipedia.org/wiki/Everything2 "wikilink") website
  - [ROT47 encoding/decoding](http://www.senses0.org.mv/popzees/rot/rotn.php)
  - [ROT47 and ROT13 encoding/decoding](http://www.just-stuart.com/cgi-bin/ur13)
  - [This Firefox extension supports ROT13 conversions and typing](http://leetkey.mozdev.org)

[Category:暗号](https://ja.wikipedia.org/wiki/Category:暗号 "wikilink")
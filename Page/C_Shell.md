> この記事は[C Shell](https://ja.wikipedia.org/wiki/C_Shell)から翻訳されています。


**C shell**（シーシェル、**csh**）は、[カリフォルニア大学バークレー校](../Page/カリフォルニア大学バークレー校.md "wikilink")の大学院生だった[ビル・ジョイ](../Page/ビル・ジョイ.md "wikilink")が1970年代後半に開発した[Unixシェル](https://ja.wikipedia.org/wiki/Unixシェル "wikilink")である。1978年にジョイが配布を始めた 2BSD という [BSD](../Page/BSD.md "wikilink") UNIX のリリースで広く配布されることになった\[1\]\[2\]。他にアイデアやコードに貢献した者としては、マイケル・ウベル、[エリック・オールマン](../Page/エリック・オールマン.md "wikilink")、マイク・オブライエン、ジム・カルプがいる\[3\]。[UNIX](../Page/UNIX.md "wikilink") V6 の /bin/sh を元に作られたもので、[Bourne shell](https://ja.wikipedia.org/wiki/Bourne_shell "wikilink") (UNIX V7)と共通の先祖を持つ。

通常テキストウィンドウ内で動作する[コマンドラインインタプリタ](../Page/コマンドラインインタプリタ.md "wikilink")であり、ユーザーがコマンドを入力するとそれに応じた処理が実行される。また[シェルスクリプト](../Page/シェルスクリプト.md "wikilink")と呼ばれるファイルからコマンド群を読み込むこともできる。他のUnixシェルと同様、ファイル名の[ワイルドカード](../Page/ワイルドカード_\(情報処理\).md "wikilink")、[パイプ](../Page/パイプ_\(コンピュータ\).md "wikilink")、[ヒアドキュメント](https://ja.wikipedia.org/wiki/ヒアドキュメント "wikilink")、、[変数](../Page/変数_\(プログラミング\).md "wikilink")、条件分岐やループなどの[制御構造](../Page/制御構造.md "wikilink")をサポートしている。cshが1980年代の他のシェルと異なっていた点は、対話向けの機能と全体的なスタイルである。新機能によって他のシェルよりも容易に素早く使うことができた。言語としての全体的スタイルは[C言語](../Page/C言語.md "wikilink")によく似ており、Unixユーザーにとっては読みやすかった。

[macOS](https://ja.wikipedia.org/wiki/macOS "wikilink") や [Red Hat Linux](../Page/Red_Hat_Linux.md "wikilink") など多くのシステムのcshは実際には改良版の[tcsh](https://ja.wikipedia.org/wiki/tcsh "wikilink")である。tcshの実行ファイルは "csh" と "tcsh" の両方に[ハードリンク](../Page/ハードリンク.md "wikilink")されていて、どちらの名前でも同じ改良版のtcshが呼び出される。

[Ubuntu](../Page/Ubuntu.md "wikilink")ではcshとtcshの2種類のパッケージを用意しており、前者はオリジナルのBSD版csh\[4\]、後者は改良版のtcsh\[5\]となっている。

tcshには、ファイル名やコマンドの補完機能、[Tenexシステムに由来するコマンド行編集があり](https://ja.wikipedia.org/wiki/TOPS-20#TENEX "wikilink")、名称の先頭の "t" は Tenex に因んでいる\[6\]。tcshは機能を追加しただけでオリジナルのcshを修正したわけではないので、[後方互換](https://ja.wikipedia.org/wiki/後方互換 "wikilink")を保っていた\[7\]。当初はジョイが作ったオリジナルのソースツリーからの脇枝だったが、今ではtcshが主な枝となっていて、開発が継続されている。tcshは非常に安定しているが、主に細かいバグ修正のため、およそ1年に1回の頻度で新たなリリースがなされている\[8\]。

## 設計目標と機能

C shell の主たる設計目標は、[C言語](../Page/C言語.md "wikilink")に似せることと、対話型利用での改良であった。

### C言語風のスタイル

Unixシステムはほとんど全体がCで書かれているため、C shell の第一の目標はスタイル上システム全体と一貫性のあるコマンド言語とすることだった。キーワード、括弧の利用、組み込みの式の文法、配列サポートなどは全てCの影響を強く受けている。

今ではC言語によく似た文法の[スクリプト言語](../Page/スクリプト言語.md "wikilink")がいくつもあり、それらに比べればcshはそれほどC言語に似ているとは言えない。しかし80年代から90年代にかけて、特に[AT\&T](../Page/AT&T.md "wikilink")で[スティーブン・ボーン](https://ja.wikipedia.org/wiki/スティーブン・ボーン "wikilink")が開発した[shと比べたときの違いは著しいと見られていた](../Page/Bourne_Shell.md "wikilink")。次の例は、C shell の[演算子](../Page/演算子.md "wikilink")や構文のわかりやすさを示したものである。

<table>
<thead>
<tr class="header">
<th><p>Bourne shell</p></th>
<th></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><div class="sourceCode" id="cb1"><pre class="sourceCode bash"><code class="sourceCode bash"><span id="cb1-1"><a href="#cb1-1"></a><span class="co">#!/bin/sh</span></span>
<span id="cb1-2"><a href="#cb1-2"></a><span class="kw">if</span><span class="bu"> [</span> <span class="va">$days</span> <span class="ot">-gt</span> 365<span class="bu"> ]</span></span>
<span id="cb1-3"><a href="#cb1-3"></a><span class="kw">then</span></span>
<span id="cb1-4"><a href="#cb1-4"></a>   <span class="bu">echo</span> This is over a year.</span>
<span id="cb1-5"><a href="#cb1-5"></a><span class="kw">fi</span></span></code></pre></div></td>
<td><div class="sourceCode" id="cb2"><pre class="sourceCode csh"><code class="sourceCode tcsh"><span id="cb2-1"><a href="#cb2-1"></a><span class="co">#!/bin/csh</span></span>
<span id="cb2-2"><a href="#cb2-2"></a><span class="cf">if</span> <span class="kw">(</span> <span class="ot">$days</span> <span class="ot">&gt;</span> 365 <span class="kw">)</span> <span class="cf">then</span></span>
<span id="cb2-3"><a href="#cb2-3"></a>   <span class="kw">echo</span> This is over a year.</span>
<span id="cb2-4"><a href="#cb2-4"></a><span class="cf">endif</span></span></code></pre></div></td>
</tr>
</tbody>
</table>

shには[式の文法が存在しない](../Page/式_\(プログラミング\).md "wikilink")。角括弧で囲まれた条件式は、外部のというプログラムで評価する必要がある。つまり、shのifコマンドは[子プロセス](../Page/子プロセス.md "wikilink")を起動して引数を別のコマンドとして実行させる。その子プロセスが終了したときの[リターンコード](https://ja.wikipedia.org/wiki/リターンコード "wikilink")がゼロならthen節を探し（then節はifとは別の文だが、セミコロンをはさんで一行で書かれることが多い）、入れ子になったブロックを実行する。リターンコードがゼロ以外ならelse節を実行する。testプログラムを "`test`" と "`[`" の両方に[ハードリンク](../Page/ハードリンク.md "wikilink")することで、角括弧表記の利点が生まれ、testの機能があたかもshの一部であるかのような錯覚を与える。shで制御ブロックの終端にキーワードを逆に綴ったものを置くのは、[ALGOL 68](../Page/ALGOL.md "wikilink") のスタイルを踏襲したものである\[9\]。

対照的にcshは自前で式を評価でき、高速である。[可読性](../Page/可読性.md "wikilink")もよいと言われている。演算子や構文の多くはC言語のものをそのまま使っている。キーワードを逆に綴ることもなく、全体としてよりC言語に近いスタイルである。

次の例は、2の1乗から10乗までを計算するスクリプトを比較したものである。

<table>
<thead>
<tr class="header">
<th><p>Bourne shell</p></th>
<th><p>C shell</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><div class="sourceCode" id="cb1"><pre class="sourceCode bash"><code class="sourceCode bash"><span id="cb1-1"><a href="#cb1-1"></a><span class="co">#!/bin/sh</span></span>
<span id="cb1-2"><a href="#cb1-2"></a><span class="va">i=</span>2</span>
<span id="cb1-3"><a href="#cb1-3"></a><span class="va">j=</span>1</span>
<span id="cb1-4"><a href="#cb1-4"></a><span class="kw">while</span><span class="bu"> [</span> <span class="va">$j</span> <span class="ot">-le</span> 10<span class="bu"> ]</span></span>
<span id="cb1-5"><a href="#cb1-5"></a><span class="kw">do</span></span>
<span id="cb1-6"><a href="#cb1-6"></a>   <span class="bu">echo</span> <span class="st">&#39;2 **&#39;</span> <span class="va">$j</span> = <span class="va">$i</span></span>
<span id="cb1-7"><a href="#cb1-7"></a>   <span class="va">i=</span><span class="kw">`</span><span class="fu">expr</span> <span class="va">$i</span> <span class="st">&#39;*&#39;</span> 2<span class="kw">`</span></span>
<span id="cb1-8"><a href="#cb1-8"></a>   <span class="va">j=</span><span class="kw">`</span><span class="fu">expr</span> <span class="va">$j</span> + 1<span class="kw">`</span></span>
<span id="cb1-9"><a href="#cb1-9"></a><span class="kw">done</span></span></code></pre></div></td>
<td><div class="sourceCode" id="cb2"><pre class="sourceCode csh"><code class="sourceCode tcsh"><span id="cb2-1"><a href="#cb2-1"></a><span class="co">#!/bin/csh</span></span>
<span id="cb2-2"><a href="#cb2-2"></a><span class="kw">set</span> i = 2</span>
<span id="cb2-3"><a href="#cb2-3"></a><span class="kw">set</span> j = 1</span>
<span id="cb2-4"><a href="#cb2-4"></a><span class="cf">while</span> <span class="kw">(</span> <span class="ot">$j</span> <span class="kw">&lt;</span>= 10 <span class="kw">)</span></span>
<span id="cb2-5"><a href="#cb2-5"></a>   <span class="kw">echo</span> <span class="st">&#39;2 **&#39;</span> <span class="ot">$j</span> = <span class="ot">$i</span></span>
<span id="cb2-6"><a href="#cb2-6"></a>   @ i *= 2</span>
<span id="cb2-7"><a href="#cb2-7"></a>   @ j++</span>
<span id="cb2-8"><a href="#cb2-8"></a><span class="cf">end</span></span></code></pre></div></td>
</tr>
</tbody>
</table>

やはりshには式の文法が存在しないため、shのスクリプトはと[expr](https://ja.wikipedia.org/wiki/expr "wikilink")コマンドを使っている。C shell の @ 文（コマンド）は一種の[駄洒落](../Page/駄洒落.md "wikilink")であり、"at-sign-ment" すなわち代入文を意味している。

最後の例は、[switch文](https://ja.wikipedia.org/wiki/switch文 "wikilink")のスタイルの違いを示したものである。

<table>
<thead>
<tr class="header">
<th></th>
<th><p>C shell</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><div class="sourceCode" id="cb1"><pre class="sourceCode bash"><code class="sourceCode bash"><span id="cb1-1"><a href="#cb1-1"></a><span class="co">#!/bin/sh</span></span>
<span id="cb1-2"><a href="#cb1-2"></a><span class="kw">for</span> <span class="ex">i</span> in d*</span>
<span id="cb1-3"><a href="#cb1-3"></a><span class="kw">do</span></span>
<span id="cb1-4"><a href="#cb1-4"></a>   <span class="kw">case</span> <span class="va">$i</span><span class="kw"> in</span></span>
<span id="cb1-5"><a href="#cb1-5"></a>      d?<span class="kw">)</span> <span class="bu">echo</span> <span class="va">$i</span> is short <span class="kw">;;</span></span>
<span id="cb1-6"><a href="#cb1-6"></a>      <span class="ex">*</span>) <span class="bu">echo</span> <span class="va">$i</span> is long <span class="kw">;;</span></span>
<span id="cb1-7"><a href="#cb1-7"></a>   <span class="kw">esac</span></span>
<span id="cb1-8"><a href="#cb1-8"></a><span class="kw">done</span></span></code></pre></div></td>
<td><div class="sourceCode" id="cb2"><pre class="sourceCode csh"><code class="sourceCode tcsh"><span id="cb2-1"><a href="#cb2-1"></a><span class="co">#!/bin/csh</span></span>
<span id="cb2-2"><a href="#cb2-2"></a><span class="cf">foreach</span> i <span class="kw">(</span> d* <span class="kw">)</span></span>
<span id="cb2-3"><a href="#cb2-3"></a>   <span class="cf">switch</span> ( <span class="ot">$i</span> )</span>
<span id="cb2-4"><a href="#cb2-4"></a>      case d?:</span>
<span id="cb2-5"><a href="#cb2-5"></a>         echo <span class="ot">$i</span> is short</span>
<span id="cb2-6"><a href="#cb2-6"></a>         breaksw</span>
<span id="cb2-7"><a href="#cb2-7"></a>      default:</span>
<span id="cb2-8"><a href="#cb2-8"></a>         echo <span class="ot">$i</span> is long</span>
<span id="cb2-9"><a href="#cb2-9"></a>   <span class="kw">endsw</span></span>
<span id="cb2-10"><a href="#cb2-10"></a><span class="cf">end</span></span></code></pre></div></td>
</tr>
</tbody>
</table>

shのスクリプトでは、"`;;`" で各ケースの終りを示す。通常は空文を許さないため、これはケースの終りを目立たせるためである。

### 対話型利用のための改良点

C shell の第二の設計目標は、対話型利用の改良だった。そのため、[ユーザビリティ](../Page/ユーザビリティ.md "wikilink")や入力の高速性を追求したいくつかの新機能を導入している。必要な結果を得るのに打ち込まなければならないキーストローク数を減らすことで、高速性を実現している。特に重要なのは、ヒストリとその編集機構、エイリアス、ディレクトリスタック、チルダ記法、cdpath、ジョブコントロール、パスハッシングである。これら新機能は人気となり、多くが他のUnixシェルにも採用された。

  - ヒストリ
    素早いキーストロークで以前に入力したコマンド行を呼び出して再実行することができる。例えば、[感嘆符](../Page/感嘆符.md "wikilink")を2つ "`!!`" と入力すると、直前に入力したコマンドを再実行できる。他にも "`!$`" と入力すると直前のコマンド行の最後の引数に置換される。
  - 編集機構
    編集はヒストリ内のコマンドのテキストだけでなく、様々な置換が可能である。編集用作用素としては、単純な文字列検索/置換からファイルのパス名を構文解析して特定の部分を取り出すなどがある。
  - エイリアス
    ユーザーが定義した何らかの文字列の別名（エイリアス）を設定でき、その別名を打ち込むと C shell がそれをユーザー定義文字列に置換する。例えば "[`fgrep`](../Page/Grep.md "wikilink")" コマンドのエイリアスとして "`f`" を設定しておくとキーストロークが少なくなって高速化でき、スクリプトを作るよりも簡単である。
  - ディレクトリスタック
    ディレクトリ[スタック](../Page/スタック.md "wikilink")は、[カレントディレクトリ](https://ja.wikipedia.org/wiki/カレントディレクトリ "wikilink")をスタックにプッシュまたはポップでき、ファイルシステム内の複数個所で少ないキーストロークで行き来することができる。
  - チルダ記法
    [ホームディレクトリ](../Page/ホームディレクトリ.md "wikilink")を "[`~`](https://ja.wikipedia.org/wiki/~ "wikilink")" で記述でき、ホームからの相対パスでファイルを指定できる。
  - 対話的ファイル名補完
    [Escキー](https://ja.wikipedia.org/wiki/Escキー "wikilink")を対話的に使用し、入力中のコマンド行の最後尾のファイル名を補完する可能性のある候補を示すことができる。
  - cdpath
    コマンド検索パス（[環境変数](../Page/環境変数.md "wikilink")のPATH）の記法で、[cdコマンドを拡張するシェル変数](https://ja.wikipedia.org/wiki/cd_\(UNIX\) "wikilink")。cdコマンドで指定されたディレクトリが[カレントディレクトリ](https://ja.wikipedia.org/wiki/カレントディレクトリ "wikilink")にない場合、cdpathに指定されているディレクトリ群も調べる。
  - ジョブコントロール
    1980年代、多くのユーザーは単純なキャラクタ[端末](../Page/端末.md "wikilink")を使っていた。shの場合、一度に1つのことしかできなかった。ウィンドウを別に開くということができなかったため、ファイルの編集を開始するには、それまで行っていたことを終了させるなどする必要があった。C shell のジョブコントロールはこの問題を解決するもので、Ctrl-Z を押下することで現在実行中のジョブをサスペンドし、新たな C shell のインスタンスを生成することができる。そして、`fg` コマンドで複数のジョブを切り換えることができる。アクティブなジョブはフォアグラウンドジョブと呼ぶ。それ以外のジョブはサスペンド状態かまたはバックグラウンド状態となる。
  - パスハッシング
    パスハッシングとは、実行可能ファイルの検索を高速化する機能である。PATHに示されたディレクトリを順に見ていくのではなく、C shell 内部に構築したハッシュテーブルから実行可能ファイルを探す。"rehash" コマンドはそのハッシュテーブルをリフレッシュするもので、新たに実行可能ファイルを作成した場合などに使用する。

## スクリプト言語としての C Shell

C shell は行単位で操作する。各行を[字句解析](../Page/字句解析.md "wikilink")して空白、括弧、パイプやリダイレクトを表す記号、セミコロン、アンパサンド等で区切られた単語の並びとして認識する。

### 基本構文

基本の文は単にコマンドを実行するものである。先頭の単語がコマンド名として認識され実行される。"`echo`" などの内部コマンドの場合と外部コマンドの場合がある。それに続く単語列は、そのコマンドの引数として渡される。

基本構文レベルでは、以下のような文法の機能が存在する。

  - [ワイルドカード](../Page/ワイルドカード_\(情報処理\).md "wikilink")
    他のUnixシェルと同様、任意のコマンド行引数にワイルドカードを使用できる。ワイルドカード文字を含む単語がある場合、それをパターンとし、マッチするファイル名の一覧と置換する。
      -
        `*` は、任意長の文字列とマッチする。
        `?` は、任意の1つの文字とマッチする。
        `[`...`]` は、角括弧内の任意の文字とマッチする。ハイフンで範囲指定することもできる。
        `[!`...`]` は、角括弧内の文字以外の任意の文字とマッチする。
    cshではいくつか便利な記法を導入しており、他のUnixシェルにも採用されている。
      -
        *abc*`{`*def*`,`*ghi*`}` は、*abcdef* または *abcghi* に展開される。
        `~` は、カレントユーザーのホームディレクトリを意味する。
        `~`*user* は、その *user* のホームディレクトリを意味する。
    複数ディレクトリレベルのワイルドカード、例えば "`*/*.c`" といった記述も可能である。
    ワイルドカード処理をシェルが行うようにしたことは、Unixにおける重要な決定の1つである。つまり、どのコマンドでも同じようにワイルドカードが使え、シェルだけがワイルドカード処理に必要なコードを備えていればよい。しかし、そのために[子プロセス](../Page/子プロセス.md "wikilink")生成時の[exec](https://ja.wikipedia.org/wiki/exec "wikilink")システムコールには非常に長い引数を効率的に渡す必要が生じた。対照的に[Windowsはコマンド行を](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")[Unicode](../Page/Unicode.md "wikilink")でおよそ32K文字までに制限しており、ワイルドカード処理は各アプリケーションが行うようになっている（実際にはC言語の`main()`関数を実行する前にCのランタイムコードが自動的に行う）。これは[MS-DOS](../Page/MS-DOS.md "wikilink")からの伝統である。MS-DOSではアプリケーションに渡せるコマンド行は128バイトに制限されていたため、ワイルドカード処理をコマンドプロンプト側で行うのは非現実的だった。
  - 入出力[リダイレクト](https://ja.wikipedia.org/wiki/リダイレクト_\(CLI\) "wikilink")
    cshでコマンドを実行する場合、デフォルトではcshの[標準入力](https://ja.wikipedia.org/wiki/標準ストリーム "wikilink")/[標準出力](https://ja.wikipedia.org/wiki/標準ストリーム "wikilink")/[標準エラー出力をそのまま継承し](https://ja.wikipedia.org/wiki/標準ストリーム "wikilink")、それらはcshが動作している端末（または[端末エミュレータ](../Page/端末エミュレータ.md "wikilink")）を指しているのが普通である。入出力リダイレクトを行うことで入力または出力に端末ではなくファイルを使うよう設定できる。
      -
        `>`*file* は、標準出力が *file* に書かれることを意味する。既存ファイルの場合は上書きし、無ければ新規作成する。エラーはシェルのウィンドウに表示される。
        `>&`*file* は、標準出力と標準エラー出力の両方が *file* に書かれることを意味する。既存ファイルの場合は上書きし、無ければ新規作成する。
        `>>`*file* は、標準出力が *file* の最後尾に追記されることを意味する。
        `>>&`*file* は、標準出力と標準エラー出力の両方が *file* の最後尾に追記されることを意味する。
        `<`*file* は、*file* から標準入力に読み込むことを意味する。
        `<<`*string* は、[ヒアドキュメント](https://ja.wikipedia.org/wiki/ヒアドキュメント "wikilink")である。*string* にマッチする行が入力されるまでの入力内容を標準入力として読み込む。
  - 連結
    コマンドは、次のような手段で1行に複数個連結することができる。
      -
        `;` は、1つめのコマンドを実行し、次に2つめのコマンドを実行することを意味する。
        `&&` は、1つめのコマンドを実行し、その[リターンコード](https://ja.wikipedia.org/wiki/リターンコード "wikilink")が0（成功）の場合、2つめのコマンドを実行する。
        `||` は、1つめのコマンドを実行し、リターンコードが0以外（失敗）の場合に2つめのコマンドを実行する。
  - [パイプ](../Page/パイプ_\(コンピュータ\).md "wikilink")
    複数のコマンドをパイプで接続でき、あるコマンドの出力を次のコマンドの入力とすることができる。この場合、2つのコマンドは並行して動作する。
      -
        `|` は、前のコマンドの標準出力を次のコマンドの標準入力に接続する。エラーはシェルのウィンドウに表示される。
        `|&` は、前のコマンドの標準出力と標準エラー出力を次のコマンドの標準入力に接続する。
  - [変数置換](https://ja.wikipedia.org/wiki/変数置換 "wikilink")
    単語にドル記号 "`$`" がある場合、それに続く文字列を変数名と解釈し、その変数の値で置換する。変数にパス名を入れておくと、ヒストリの編集機構を使って特定部分（ファイル拡張子やファイル名本体のみなど）を取り出すこともできる。
  - 引用符とエスケープ
    引用機構は、空白、ワイルドカード、括弧、ドル記号など通常なら特殊な意味を持つ文字を[リテラル](../Page/リテラル.md "wikilink")テキストとして扱えるようにする。
      -
        `\` は、続く文字を通常のリテラル文字として扱う。
        `"`*string*`"` は弱い引用である。空白やワイルドカードはリテラルとして扱われるが、変数やコマンド置換はそのまま機能する。
        `'`*string*`'` は強い引用である。囲まれた文字列全体がリテラルとして扱われる。
  - コマンド置換
    コマンド置換は、あるコマンドの出力を別のコマンドの引数として使えるようにする。
      -
        `` ` ``*command*`` ` `` は *command* を実行し、その出力でコマンド行の当該部分を置換する。
  - バックグラウンド実行
    通常、コマンドを実行開始するとそれが終わるのを待ち合わせ、次のコマンドを実行するか、ユーザーのコマンド入力を促すプロンプトを表示する。
      -
        *command*`&` は、*command* をバックグラウンドで実行開始し、即座に次のコマンドを受け付けられるようにする。
  - サブシェル
    サブシェルはシェルの子プロセスであり、現在の状態を継承しているが、それを変更することもできる。例えば、カレントディレクトリを変更しても親のカレントディレクトリは変化しない。
      -
        `(`*commands*`)` は、*commands* をサブシェルで実行することを意味する。

### 制御構造

csh は[条件分岐と](../Page/If文.md "wikilink")[反復という](../Page/イテレータ.md "wikilink")[制御構造](../Page/制御構造.md "wikilink")を提供している。条件分岐としては `if` 文と `switch`文がある。反復としては、`while` 文、`foreach` 文、`repeat` 文がある。

#### `if` 文

`if` 文には2つの形式がある。短い形式は1行で済むが、式が真の場合に実行できるコマンドはひとつだけである。

``` csh
if (式) コマンド
```

長い形式は `then`、`else`、`endif` というキーワードを使いコマンドの並んだブロックを形成でき、その中でさらに条件分岐を入れ子にすることもできる。

``` csh
if (式1) then
  コマンド11
  コマンド12
  コマンド13
  ...
else if (式2) then
  コマンド21
  コマンド22
  コマンド23
  ...
else
  コマンドn1
  コマンドn2
  コマンドn3
  ...
endif
```

`else` と `if` が同じ行に出現する場合、csh はそれを入れ子というよりも連鎖として扱う。つまり `endif` はひとつでよい。

#### `switch` 文

`switch` 文は文字列をパターンの一覧と比較する。パターンにはワイルドカード文字を含んでもよい。どれもマッチしない場合 `default` アクションを実行し、マッチすればその部分を実行する。

``` csh
switch (文字列)
  case パターン1:
    コマンド列11
    コマンド列12
    コマンド列13
         :
  breaksw
  case パターン2:
    コマンド列21
    コマンド列22
    コマンド列23
         :
  breaksw
     :
  default:
    コマンド列n1
    コマンド列n2
    コマンド列n3
         :
endsw
```

#### `while` 文

`while` 文は式を評価する。その結果が真なら続くコマンド群を実行し、再び式の評価に戻る。

``` csh
while (式)
  コマンド1
  コマンド2
  コマンド3
  ...
end
```

#### `foreach`文

`foreach` 文は値の一覧（通常はワイルドカードで生成されたファイル名一覧）をとり、それぞれの値について値をループ変数に設定し、続くコマンド群を実行する。

``` csh
foreach ループ変数 (値1 値2 値3 ... 値n)
  コマンド1
  コマンド2
  コマンド3
  ...
end
```

#### repeat文

repeat文は「整数値」で指定された回数だけ「コマンド」（ひとつのコマンド）を繰り返し実行する。

``` csh
repeat 整数値 コマンド
```

### 変数

csh はシェル変数と[環境変数](../Page/環境変数.md "wikilink")を実装している。環境変数は setenv 文で生成でき、その値は常に単純な文字列であり、`exec` システムコール経由任意の[子プロセス](../Page/子プロセス.md "wikilink")に引き継がれる。

シェル変数は `set` 文や `@` 文で生成され csh 内部で使われる。子プロセスには渡されない。シェル変数は単純な文字列の場合と文字列の配列の場合がある。事前定義されたシェル変数もいくつかあり、csh 内部の各種オプションの制御に使われる。例えば、ワイルドカードが何にもマッチしなかった際の動作などを設定できる。

現在のバージョンの csh では、変数に格納できる文字列の長さは任意であり、数百万文字でもよい。

### 式

C shell はC言語の演算子を流用した文法で32ビット整数の式を評価する機能を実装している。他に文字列比較の演算子やファイルシステムのテスト演算子（あるファイルが存在するかどうかのテスト）もある。演算子とオペランドは空白で区切らなければならない。変数は `$`*name* の形式で参照する。

[演算子の優先順位](https://ja.wikipedia.org/wiki/演算子の優先順位 "wikilink")もC言語を踏襲しているが、優先順位の等しい演算子が並んでいるときの演算順序の曖昧さを解決する演算子の結合性はC言語とは異なる。C言語では多くの演算子で左から右へ結合していくのに対し、C shell では右から左に結合していく。以下に例を示す。

C shell での括弧はビットシフト演算子と入出力リダイレクトを混同しないために使用している。どちらの言語でも括弧を使えば評価順序を明確化できる。なお先述した通り、シェル変数の値は文字列であり、@ 文などの式の中でだけ文字列を数値に変換して評価し、結果を文字列に変換して変数に格納している。

## 批判

いくつもの革新的機能により対話型利用では人気となったが、csh はスクリプト言語としては人気を獲得することはなかった。当初から1980年代末まで、cshはあらゆるUnixシステムに実装されていたわけではなく、shならばあらゆるUnixシステムに存在することが確実だった。したがって、様々なシステムで動作する可能性のあるスクリプトはshで書くのが賢明だった。1990年代中ごろにはcshも広く利用可能となったが、[POSIX](../Page/POSIX.md "wikilink")の委員会からcshをスクリプト言語として使用することに対して批判の声が挙がった\[10\]。すなわち、対話用とスクリプト用の推奨シェルは1つであるべきだとし、POSIXとしては [KornShell](../Page/KornShell.md "wikilink") を推奨するとしたのである。C shell は他にも、文法上の欠陥、機能不足、実装のまずさといった点で批判された\[11\]\[12\]。

  - 文法上の欠陥
    言語定義上、不必要な矛盾が生じている。例えば、`set`、`setenv`、`alias` というコマンドは、ある名前と文字列または単語の並びを結びつけるという基本的に同じ機能を有している。しかし、それらには全く不必要な若干の差異がある。`set` では等号を必要とするが、`setenv` や `alias` では等号は使わない。`set` では単語の並びを括弧で囲む必要があるが、`setenv` と `alias` ではそうではない。同様に、`if` の最後は `endif`、`switch` の最後は `endsw`、ループ系構文では最後が `end` というように意味も無く一貫性がない文法になっている。
  - 機能不足
    よく言われるのは、[標準入力ファイルハンドルの操作機能と関数サポートの欠如である](https://ja.wikipedia.org/wiki/Fgetc "wikilink")。Bourne shell は局所変数は使えないが関数は定義できるのに対し、csh で関数に相当する機能はエイリアスしかなく、1行のコードしか定義できず、しかも制御構文の多くは途中に改行を必要とする。結果としてスタイルは似ていてもC言語のプログラムの機能をそのまま C shell で実装するのは困難である。そのため、大きなプロジェクトほどC言語や Bourne shell のスクリプトを使う傾向がある。
  - 実装のまずさ
    [構文解析](../Page/構文解析.md "wikilink")は場当たり的であり、多くの批判を浴びている。1970年代初めには[コンパイラ](../Page/コンパイラ.md "wikilink")技術はそれなりに成熟しており\[13\]、多くの言語は[トップダウンまたは](../Page/トップダウン構文解析.md "wikilink")[ボトムアップ構文解析](../Page/ボトムアップ構文解析.md "wikilink")器を使って完全に再帰的な[文法を認識できるように実装されていた](../Page/形式文法.md "wikilink")。C shell で場当たり的な設計となった理由は不明である。ジョイは2009年のインタビューで「Unixに関して作業を始めたとき、私は優秀なプログラマではなかった」と述べており、単にそれが答えかもしれない\[14\]。しかし、場当たり的な設計を選択したせいで C shell は完全再帰的ではなくなった。したがって、実現できる処理の複雑さには限度がある。

対話的にコマンドを入力して実行するぶんには快適だが、複雑なコマンドを実行させようとスクリプトを書いてみると時間がかかり、しかもよく失敗し、暗号のようなエラーメッセージを表示するか、好ましくない結果を生じることになる。例えば、C shell では制御構造間のパイプは不可能である。例えば `foreach` の出力をパイプで [`grep`](https://ja.wikipedia.org/wiki/grep "wikilink") コマンドに送り込もうとしても単に機能しない。ワークアラウンドとしては、`foreach` を使った部分を別のスクリプトにして構文解析の問題を回避するという手段がある。こうすれば、そのスクリプトは別のcshのプロセスとして動作するのでパイプで接続することも自由である。

別の好ましくない動作の例としてコード断片を示す。下記のスクリプトはどちらも「'myfile' が存在しないなら、'mytext' をそこに書き込む形で生成せよ」という意味である。しかし、右側の例では常に空ファイルが生成される。何故なら C shell の評価順序はコマンド行単位であり、まず入出力リダイレクトを評価することになっているためで、myfile がその際に作られてしまい、ファイルの存在を調べたときには既に存在しているためである。

また、エラーメッセージが貧弱だという点もよく批判されている。例えば "0 event not found" というメッセージからは何が問題なのかもわからない。

## 影響

ヒストリ機構、エイリアス、チルダ記法、対話的ファイル名補完、シェル内での式評価などといった機能は大きな成功だったと言え、他のUnixシェルでも採用された。しかし[kshや](../Page/KornShell.md "wikilink")[bash](https://ja.wikipedia.org/wiki/bash "wikilink")など多数の独立したクローンが生まれた[shとは対照的に](../Page/Bourne_Shell.md "wikilink")、cshのクローンとして知られているものは2つしかない（tcshはcshと独立して開発されたわけではなく、クローンとは言えない。tcshはビル・ジョイの書いたオリジナルのコードをベースとして機能を追加しただけである）。

の1986年の著書 *On Command: Writing a Unix-Like Shell for [MS-DOS](../Page/MS-DOS.md "wikilink")*\[15\] では、"SH" という名前のプログラムを解説しているが、これはshではなくcshの機能と言語設計をコピーしたものである。関連するフロッピーディスクにはSHと基本的なUnix風コマンド（cat、cp、grep など）のソースコードが格納されていて、それぞれ25ドルと30ドルで販売されていた。ホーラブのSHの制御構造、式の文法、ヒストリ機構などは全て C shell と同一だった。

1988年、Hamilton Laboratories が[OS/2](https://ja.wikipedia.org/wiki/OS/2 "wikilink")向けに [Hamilton C shell](https://ja.wikipedia.org/wiki/:en:Hamilton_C_shell "wikilink") を発売した\[16\]。1992年には [Windows NT](../Page/Microsoft_Windows_NT.md "wikilink") 版をリリース\[17\]。Windows版はその後も活発にサポートされているが\[18\]、OS/2版は2003年でサポート終了している。Hamilton C shell は Nicole Hamilton が書いたもので、cshクローンとUnixユーティリティ群を含んでいる。初期のクイックリファレンスによれば\[19\]、「（ジョブコントロールを除く）C shell 言語全体に完全準拠」としているが、言語仕様には若干の改良が見られ、UnixとPCの差異にも対応している。最大の改良点は[トップダウン構文解析](../Page/トップダウン構文解析.md "wikilink")を採用した点で、[制御構造](../Page/制御構造.md "wikilink")の入れ子やパイプ連結が可能となっている。また、プロシージャを定義でき、ブロック構造に局所変数を定義でき、浮動小数点演算もサポートしている。PC向けの改良点としては、ファイル名などのPCにおける慣習に従っており、[スレッドの生成で済む部分は子プロセスを生成するのではなくスレッドで対応している](../Page/スレッド_\(コンピュータ\).md "wikilink")。

[音声認識](../Page/音声認識.md "wikilink")研究の分野では C shell がスクリプト言語としてよく使われている。これはHTKというツール\[20\]がcshスクリプトを使っていることと関連している。

## 脚注

## 参考文献

  -
  -
  -
  -
  -
  -
## 関連項目

  - [コマンドラインインタプリタ](../Page/コマンドラインインタプリタ.md "wikilink")

## 外部リンク

  - [有害な csh プログラミング](http://www.speech-lab.org/~hiroki/csh-whynot.euc)
  - [Cシェルプログラミング](https://www2.yukawa.kyoto-u.ac.jp/~kanehisa.takasaki/edu/c/cshell.txt)
  - [*An Introduction to the C shell*](http://www.kitebird.com/csh-tcsh-book/csh-intro.pdf) by [William Joy](../Page/ビル・ジョイ.md "wikilink").
  - [Linux in a Nutshell: Chapter 8. csh and tcsh](https://docstore.mik.ua/orelly/linux/lnut/ch08_01.htm).
  - [tcsh home page.](https://www.tcsh.org/)
  - [historical 2BSD csh source code](https://minnie.tuhs.org/cgi-bin/utree.pl?file=2BSD/src/csh) dated February 2, 1980.
  - [The Unix Tree](https://minnie.tuhs.org/cgi-bin/utree.pl), complete historical Unix distributions.

[Category:Unixシェル](https://ja.wikipedia.org/wiki/Category:Unixシェル "wikilink") [Category:BSD](https://ja.wikipedia.org/wiki/Category:BSD "wikilink") [Category:1978年のソフトウェア](https://ja.wikipedia.org/wiki/Category:1978年のソフトウェア "wikilink")

1.  Harley Hahn, [Harley Hahn's Guide to Unix and Linux](http://unix.harley.com/instructors/timeline.html).
2.  [Berkeley Engineering Lab Notes, Volume 1, Issue 2, October 2001](http://coe.berkeley.edu/labnotes/history_unix.html).
3.  [*An Introduction to the C shell*](http://www.kitebird.com/csh-tcsh-book/csh-intro.pdf) by [Bill Joy](../Page/ビル・ジョイ.md "wikilink").
4.  <http://packages.ubuntu.com/oneiric/shells/csh>
5.  <http://packages.ubuntu.com/oneiric/shells/tcsh>
6.
7.  [tcsh(1) man page](http://www.tcsh.org/tcsh.html/DESCRIPTION.html)
8.  Fixes file in tcsh-6.17.00.
9.  [*Re: Late Bloomers Revisited*](http://groups.google.com/group/comp.lang.misc/msg/d58db4799c33e093?hl=en&dmode=source) USENET post to comp.lang.misc by Piercarlo "Peter" Grandi, Dept of CS, UCW Aberystwyth, UK, Dec 17, 1989.
10. *IEEE Standard for Information Technology, Portable Operating System Interface (POSIX), Part 2: Shell and Utilities, Volume 2*. IEEE Std 1003.2-1992, pp. 766-767. ISBN 1-55937-255-9.
11. [*Csh Programming Considered Harmful*](http://www.faqs.org/faqs/unix-faq/shell/csh-whynot/) by Tom Christiansen
12. [*Top Ten Reasons not to use the C shell*](http://www.grymoire.com/Unix/CshTop10.txt) by Bruce Barnett
13. David Gries (1971). *Compiler Construction for Digital Computers.* John Wiley & Sons. ISBN 0-471-32776-X.
14. [Bill Joy in Conversation with Brent Schlender, Churchill Club, Santa Clara, CA, Feb 11, 2009](http://fora.tv/2009/02/11/Bill_Joy_in_Conversation_with_Brent_Schlender).
15.
16.
17. [Hamilton C shell for Windows Release Notes 4.0](http://hamiltonlabs.com/ReleaseNotes.htm), retrieved June 19, 2010.
18.
19.
20. [htk](http://htk.eng.cam.ac.uk/)
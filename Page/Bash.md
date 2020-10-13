> この記事は[Bash](https://ja.wikipedia.org/wiki/Bash)から翻訳されています。


**Bash**は[Unixシェル](https://ja.wikipedia.org/wiki/Unixシェル "wikilink")かつであり、[GNUプロジェクト](../Page/GNUプロジェクト.md "wikilink")における[Bourne Shellの](../Page/Bourne_Shell.md "wikilink")[フリーソフトウェア](../Page/フリーソフトウェア.md "wikilink")による代替としてによって作成された\[1\]\[2\]。Bashは1989年に初めてリリースされ\[3\]、ほとんどの[Linuxディストリビューション](../Page/Linuxディストリビューション.md "wikilink")や[アップルの](../Page/アップル_\(企業\).md "wikilink")[macOS](https://ja.wikipedia.org/wiki/macOS "wikilink")におけるデフォルトの[ログイン](https://ja.wikipedia.org/wiki/ログイン "wikilink")シェルとして広く普及している。[Windows 10における](https://ja.wikipedia.org/wiki/Microsoft_Windows_10 "wikilink")[Windows Subsystem for Linuxでも利用可能である](https://ja.wikipedia.org/wiki/Windows_Subsystem_for_Linux "wikilink")\[4\]。

Bashは[コマンドプロセッサであり](../Page/コマンドラインインタプリタ.md "wikilink")、通常はアクションを発生させるコマンドをユーザーがタイプするテキストウィンドウで起動する。Bashは[スクリプトと呼ばれるファイルからコマンドを読み込んで実行することも可能である](../Page/シェルスクリプト.md "wikilink")。Bashはそれ以外の全てのUnixシェルと同様に、ファイル名の[グロブ](https://ja.wikipedia.org/wiki/グロブ "wikilink")（[ワイルドカードによるマッチング](../Page/ワイルドカード_\(情報処理\).md "wikilink")）、[パイプ](../Page/パイプ_\(コンピュータ\).md "wikilink")、[ヒアドキュメント](https://ja.wikipedia.org/wiki/ヒアドキュメント "wikilink")、、[変数](../Page/変数_\(プログラミング\).md "wikilink")、そして[条件テストや](https://ja.wikipedia.org/wiki/if文 "wikilink")のための[制御構造](../Page/制御構造.md "wikilink")をサポートする。Bashの[予約語](../Page/予約語.md "wikilink")や[構文などの](https://ja.wikipedia.org/wiki/シンタックス "wikilink")[言語の基本的要素は全て](../Page/形式言語.md "wikilink")[Bourne shellからコピーされており](https://ja.wikipedia.org/wiki/Bourne_shell "wikilink")、ヒストリなどBourne shell以外の機能は[C Shellや](../Page/C_Shell.md "wikilink")[KornShell](../Page/KornShell.md "wikilink")からコピーされている。Bashは[POSIX](../Page/POSIX.md "wikilink")準拠のシェルであるが、数多くの拡張がされている。

Bashという名前は  の[頭字語](../Page/頭字語.md "wikilink")であり、Bashの置換対象であるBourne Shell\[5\]と、現代アメリカのキリスト教において精神的な再生を意味する （[新生](../Page/新生_\(キリスト教\).md "wikilink")）に引っ掛けた駄洒落である\[6\]\[7\]\[8\]\[9\]。

## 歴史

ブライアン・フォックスは1988年1月10日にBashの[コーディングを開始した](https://ja.wikipedia.org/wiki/プログラミング_\(コンピュータ\) "wikilink")\[10\]が、これは彼の前任開発者に進歩が見られなかったことに[リチャード・ストールマン](../Page/リチャード・ストールマン.md "wikilink")が不満を抱くようになってからのことである\[11\]。ストールマンと[フリーソフトウェア財団](../Page/フリーソフトウェア財団.md "wikilink") (FSF) は、BSDやGNUのコードからビルドされた完全にフリーなシステムにとって既存のシェルスクリプトを実行できるフリーなシェルは戦略上非常に重要であると考えていたため、Bashは彼らが自ら創設した数少ないプロジェクトのうちの1つとなり、フォックスはFSFの従業員としてその作業を引き受けた\[12\]\[13\]。フォックスは1989年6月8日にBashの[ベータ版](../Page/ベータ版.md "wikilink")であるバージョン.99をリリースし\[14\]、1992年中頃\[15\]から彼がFSFから去る\[16\]1994年中頃\[17\]の間のある期間まで主要なメンテナであった。フォックスが去った後、彼の責務はもう一人の初期貢献者であるChet Rameyへと移された\[18\]\[19\]\[20\]。

それ以降BashはLinuxユーザーの間で最も有名なシェルとなり、様々な[Linuxディストリビューション](../Page/Linuxディストリビューション.md "wikilink")やアップルのmacOSにおけるデフォルトインタラクティブシェルとなっている\[21\]\[22\]\[23\]（ただしデフォルトのスクリプトシェルが[Almquist ShellであるLinuxディストリビューションもある](../Page/Almquist_Shell.md "wikilink")）。Bashは[Microsoft Windowsにも移植されて](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")[Cygwin](../Page/Cygwin.md "wikilink")や[MinGW](../Page/MinGW.md "wikilink")の一部として配布されており、プロジェクトにより[DOSにも移植され](../Page/DOS_\(OS\).md "wikilink")、[NetWare](https://ja.wikipedia.org/wiki/NetWare "wikilink")にも移植され、さらに様々な端末エミュレータを通じて[Androidにも移植されている](../Page/Android_\(オペレーティングシステム\).md "wikilink")。

2014年9月、UNIX/Linux・ネットワーク・テレコム専門家でありイギリスで働いているStéphane Chazelas\[24\]は、プログラム内にを発見した。このバグは最初9月24日に公開されて[シェルショックと命名され](https://ja.wikipedia.org/wiki/2014年シェルショック脆弱性 "wikilink")、[CVE-2014-6271](http://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2014-6271), CVE-2014-6277\[25\]および[CVE-2014-7169](http://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2014-7169)のナンバーが割り当てられた。Bashを使用した[CGIスクリプトで](../Page/Common_Gateway_Interface.md "wikilink")[任意コード実行](https://ja.wikipedia.org/wiki/任意コード実行 "wikilink")が可能となり攻撃されやすくなるため、シェルショックは深刻なバグとみなされた。シェルショックは、Bashが[環境変数](../Page/環境変数.md "wikilink")を通じてサブシェルに関数定義を渡す方法と関係していた\[26\]。

## 機能

Bashの[コマンド構文は](https://ja.wikipedia.org/wiki/コマンド_\(コンピュータ\) "wikilink")、Bourne shellのコマンド構文のスーパーセットである。構文の前処理においてBashと異なって解釈される振る舞いに偶然遭遇してしまったり、新しくBashに組み込まれたコマンドと同じ名前のシステムコマンドを起動しようとするBourne shellスクリプトを除いて、Bashは大量に存在するBourne shellスクリプトのほとんどを修正せずに実行可能である。Bashのコマンド構文には、コマンドライン編集、、ディレクトリスタック、変数 `$RANDOM`や変数 `$PPID`、およびPOSIXの構文である`$(`<var>`コマンド`</var>`)`など、KornShellやC shellから引用したアイデアが含まれる。

ユーザーがインタラクティブコマンドシェルで[タブキー](../Page/タブキー.md "wikilink")を押した場合、Bashは途中までタイプされたプログラム名やファイル名などの様々な名前をマッチさせるを自動で行う。Bashのコマンドライン補完システムは大変融通が利きカスタマイズ可能であるため、特定のプログラムやタスク用の引数やファイル名を補完する関数とまとめてパッケージングされることが多い。

Bashの構文には、Bourne shellにはない拡張が多く存在する。Bashは他のプロセスを生成せずに整数演算ができる。この演算のためにBashは `((`<var>`数式`</var>`))` コマンドと `$((`<var>`数式`</var>`))` 変数構文を利用する。Bashの構文は[入出力リダイレクトを単純化する](https://ja.wikipedia.org/wiki/リダイレクト_\(CLI\) "wikilink")。例えば、Bashでは `&>` 演算子を使用することで、[標準出力と](https://ja.wikipedia.org/wiki/標準ストリーム#標準出力_\(stdout\) "wikilink")[標準エラー出力を同時にリダイレクトすることができ](https://ja.wikipedia.org/wiki/標準ストリーム#標準エラー出力_\(stderr\) "wikilink")、Bourne shellにおいてこれに相当するコマンドである <var>`コマンド`</var>`  > file 2>&1 ` よりも簡単にタイプできる。Bashは`<(`<var>`コマンド`</var>`)`および`>(`<var>`コマンド`</var>`)`構文を使用することにより、をサポートする。この構文は、通常のリダイレクトではファイル名が記述される箇所にある<var>`コマンド`</var>の出力（または入力）を引数の代用とする（これは名前なしパイプをサポートするシステムならば `/proc/fd/` の名前なしパイプにより実装され、[名前付きパイプ](../Page/名前付きパイプ.md "wikilink")が必要ならば一時的な名前付きパイプにより実装されている）。

`function` キーワードを使用する場合、Bashの関数宣言はBourne・Korn・POSIXスクリプトと互換性がない（KornShellでも `function` を使用する場合に同様の問題が起こる）が、BashはBourne shellやKornShellの関数宣言構文を受け入れるためPOSIX準拠である。これ以外にも違いがあるため、互換性確保を配慮せず書かれたBashのシェルスクリプトをBourneやKornShellのインタプリタで起動できることは滅多にないが、Linuxが普及するにつれて互換性確保を配慮せずに書くことは少なくなっている。ただしPOSIXモードにおいては、Bashはより密接にPOSIXに準拠している\[27\]。

Bashは[ヒアドキュメント](https://ja.wikipedia.org/wiki/ヒアドキュメント "wikilink")をサポートする。Bashはバージョン2.05bより、`<<<`演算子を使った「ヒア文字列」から標準入力へのリダイレクトが可能である。

Bash3.0では[Perl](../Page/Perl.md "wikilink")言語を思い起こさせる構文を使用した、シェル組み込みの[正規表現](../Page/正規表現.md "wikilink")をサポートする\[28\]\[29\]。

Bash4.0では[連想配列](../Page/連想配列.md "wikilink")のサポートが導入された\[30\]\[31\]。連想配列により、[AWK](../Page/AWK.md "wikilink")と類似の方法で多次元配列を疑似的にサポート可能となる:

``` console
$ declare -a aa        # 疑似的二次元インデックス配列である'aa'という連想配列を宣言。
$ i=1; j=2             # インデックス初期化。
$ aa[$i,$j]=5          # キー "$i,$j"（つまり "1,2"）における連想配列の値に"5"を保存。
$ echo ${aa[$i,$j]}    # キー "$i,$j" に保存された値を出力。
5
```

### ブレース展開

ブレース展開はオルターネイションとも呼ばれ、C shellから取り入れた機能である<ref> C shellとBashのブレース展開は要素がひとつの時の挙動が異なる。

``` console
% csh -c 'echo a{p}e'
ape
% bash -c 'echo a{p}e'
a{p}e
```

</ref>。ブレース展開は取り得る組み合わせのセットを生成する。生成された結果はファイルとして存在する必要はない。展開された各文字列結果はソートされておらず、保存された順に左から右へと並んでいる:

``` console
$ echo a{p,c,d,b}e
ape ace ade abe
$ echo {a,b,c}{d,e,f}
ad ae af bd be bf cd ce cf
```

Bourne shellではBashと同じ出力を返さないため、ユーザーは移植するためのシェルスクリプトでブレース展開を使うべきではない。

``` console
$ # 伝統的なシェルはBashと同じ出力を返さない。
$ /bin/sh -c 'echo a{p,c,d,b}e'
a{p,c,d,b}e
```

ブレース展開がワイルドカードと組み合わされた場合、最初に括弧が展開されてから通常通りワイルドカードが置換される。したがって、カレントディレクトリにある拡張子が `.jpg` または `.jpeg` または `.png` のファイル群を獲得するには以下のようにする:

``` bash
ls *.{jpg,jpeg,png}    # *.jpg *.jpeg *.pngが展開されてから
                       # ワイルドカード処理がなされる。
echo *.{png,jp{e,}g}   # echoだけでもブレース展開が可能で、さらに括弧内の括弧も可能。
```

ブレース展開は取り得る全ての組み合わせだけではなく、連続した範囲に対して適用することも可能である。範囲は2つの整数や文字の間を、2つのドットで区切って指定する。Bashの新しいバージョンでは、範囲の終点を指定する2つ目の整数の後にさらに2つのドットと3つ目の整数を指定することで、範囲の増分を指定することも可能である。

``` console
$ echo {1..10}
1 2 3 4 5 6 7 8 9 10
$ echo file{1..4}.txt
file1.txt file2.txt file3.txt file4.txt
$ echo {a..e}
a b c d e
$ echo {1..10..3}
1 4 7 10
$ echo {a..j..3}
a d g j
```

ブレース展開を変数展開と組み合わせると、ブレース展開が先に行われ変数展開がその後に行われてしまうため、場合によっては`eval`ビルトインが必要になる可能性もある:

``` console
$ start=1; end=10
$ echo {$start..$end}  # Brace expansionが変数展開より先に評価されてしまうため展開に失敗。
{1..10}
$ eval echo {$start..$end} # 先に変数展開をして、その結果の文字列に対してのブレース展開を評価。
1 2 3 4 5 6 7 8 9 10
```

### 起動スクリプト

Bashは起動の際、様々なのコマンドを実行する。Bashが使用する初期化ファイルは、実行権限が与えられてかつ `#!/bin/bash` のような[シバンが記述されたBashのシェルスクリプトコマンドと似てはいるものの](../Page/シバン_\(Unix\).md "wikilink")、実行権限とインタプリタディレクティブのどちらも必要ない。

#### 起動ファイルの実行順序

| 条件                     | 順序                                                                                                                                                                                                              |
| ---------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| インタラクティブな非ログインシェルとして起動 | Bashは`/bash.bashrc`を読み込んで実行してから、（存在する場合）`~/.bashrc`を読み込んで実行する。これは `--norc` オプションを使うことで禁止することができる。` --rcfile  `<var>`ファイル`</var>オプションにより、`~/.bashrc` の代わりに <var>`ファイル`</var> からコマンドを読み込んで実行するようBashに強制させることができる。 |
| インタラクティブなログインシェルとして起動  | Bashは（存在する場合）`/etc/profile`（ファイル名を`/etc/bash.bashrc`と改名されることが多い）を読み込み実行する。このファイルを読み込んだ後、`~/.bash_profile`、`~/.bash_login`、および`~/.profile`をこの順番で調べ、存在しかつ読み込めるもののうち最初のものを読み込んで実行する。                               |
| ログインシェルを終了した場合         | Bashは（存在する場合）`~/.bash_logout`を読み込んで実行する。                                                                                                                                                                        |

#### Bourne shellやC shellの起動シーケンスとの比較

Bashの各要素はBourne shellやC shellからの派生である。このため、制限付きながら起動ファイルをBourne shellと共用でき、さらにC shellユーザーには馴染みのあるいくつかの起動シーケンスを提供する。

<table>
<thead>
<tr class="header">
<th><p>項目</p></th>
<th><p>違い</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>継承可能な環境変数の設定</p></td>
<td><p>Bourne shellはサブプロセス化されてから継承する環境変数を設定するため、ログイン時に<code>~/.profile</code>を使用する。Bashでも、Bash固有の<code>~/.bash_profile</code>や<code>~/.bash_login</code>に以下の行を記述して、それらから明示的に<code>~/.profile</code>を実行することでBourne shellと互換性を保つことが可能となる。Bash固有の構文を<code>~/.profile</code>に記述しないことで、Bourne shellとの後方互換性を保つことが可能となる。</p>
<div class="sourceCode" id="cb1"><pre class="sourceCode bash"><code class="sourceCode bash"><span id="cb1-1"><a href="#cb1-1"></a><span class="bu">.</span> <span class="ex">~/.profile</span></span></code></pre></div></td>
</tr>
<tr class="even">
<td><p>エイリアスと関数</p></td>
<td><p>C shell由来の<a href="../Page/エイリアス.md" title="wikilink">エイリアス</a>という機能が存在するが、その大部分を置き換えるBourne shell由来の関数という機能はエイリアスよりも一般的である。これら2つの機能は通常ログインシェルから継承することはできず、ログインシェルによって生み出されたサブシェル毎に再定義する必要があった。この問題の対処に利用可能な環境変数 <code>ENV</code> が存在するが、C shellとBashではこの問題に直接的を絞ったサブシェル毎の起動ファイルをサポートする。Bashでは <code>~/.bashrc</code> がインタラクティブサブシェルのために呼び出される[32]。<code>~/.bashrc</code> にあるユーザー定義関数がログインシェルでも必要な場合、以下の行を <code>~/.bash_login</code> へ必要な環境変数の設定後に記述する:</p>
<div class="sourceCode" id="cb2"><pre class="sourceCode bash"><code class="sourceCode bash"><span id="cb2-1"><a href="#cb2-1"></a><span class="bu">.</span> <span class="ex">~/.bashrc</span></span></code></pre></div></td>
</tr>
<tr class="odd">
<td><p>ログイン時のみやログアウト時のみに実行するコマンド</p></td>
<td><p>C shellは最初のログイン時のみに実行されるタスクのための <code>~/.login</code> ファイルをサポートする。このようなタスクにはシステムのロード、ディスクステータス、電子メールが来たかの有無などの表示や、ログイン時間のロギングなどがある。Bourne shellは <code>~/.profile</code> でこのファイルを模倣できるが、ファイル名は事前に定義されていない。C shellモデルに似たセマンティクスを実現するため、<code>~/.bash_profile</code> では環境設定や関数設定の後に以下の様に記述できる:</p>
<div class="sourceCode" id="cb3"><pre class="sourceCode bash"><code class="sourceCode bash"><span id="cb3-1"><a href="#cb3-1"></a><span class="bu">.</span> <span class="ex">~/.bash_login</span></span></code></pre></div>
<p>同様に、C shellはログインシェルを終了した場合のみに起動される <code>~/.logout</code> ファイルを持つ。Bashでこれに相当するのは <code>~/.bash_logout</code> であり、特殊な設定は必要ない。Bourne shellでは、似たような効果を得るためには組み込みコマンド <a href="../Page/トラップ.md" title="wikilink"><code>trap</code></a> を使用できる。</p></td>
</tr>
</tbody>
</table>

##### レガシー互換なBash起動例

以下の `~/.bash_profile` コードはBourne shellと互換性があり、`~/.bashrc` と `~/.bash_login` に対してC shellと似たセマンティクスを提供する。` [ -r  `<var>`ファイル名`</var>`  ] `は指定した <var>ファイル名</var> のファイルが存在し読み込めるかどうかを調べるテストであり、存在しない場合 `&&` の後の部分は評価（実行）されない（⇒ [短絡評価](../Page/短絡評価.md "wikilink")）。

``` bash
[ -r ~/.profile ] && . ~/.profile             # 環境設定で、かつてはBourne Shell限定の構文
if [ -n "$PS1" ] ; then                       # インタラクティブか?
   [ -r ~/.bashrc     ] && . ~/.bashrc        # インタラクティブシェル用のtty/プロンプト/関数設定
   [ -r ~/.bash_login ] && . ~/.bash_login    # ログインシェル専用のログイン時タスク
fi                                            # "if" ブロック終了
```

#### Bash起動におけるオペレーティングシステムの問題

[UNIX](../Page/UNIX.md "wikilink")や[Linux](../Page/Linux.md "wikilink")のバージョンの中には、`/etc` ディレクトリ配下にBashシステム起動スクリプトが存在するものもある。Bashはこれらのスクリプトを、Bashの通常の初期化の一部として呼び出すが、それ以外の起動ファイルをBash起動シーケンスの記述と異なる順序で読み込むこんでしまう可能性がある。さらにシステムが新しいユーザーアカウントに設定を提供するスケルトンファイルのように、ルート・ユーザーのファイル内におけるデフォルトの内容に問題がある可能性もある。[ウィンドウマネージャ](../Page/ウィンドウマネージャ.md "wikilink")の起動前にユーザーがBash起動スクリプトで自身の環境変数を準備しようとすると、[X Window Systemの起動スクリプトにより予想外の問題が発生する可能性がある](../Page/X_Window_System.md "wikilink")。これらの問題は、`~/.profile` を読み込むために `~/.xsession` や `~/.xprofile` ファイルを使う場合に発生する可能性が高い。これらのファイルは[xterm](https://ja.wikipedia.org/wiki/xterm "wikilink")や [GNOME 端末などの](../Page/GNOME_端末.md "wikilink")、ウィンドウマネージャから生み出されたBashシェルウインドウが必要とする環境変数を提供する。

### 移植性

`--posix`オプションを付けてBashを呼び出したり、スクリプトに`set -o posix`を記述すると、Bashは[POSIX](../Page/POSIX.md "wikilink") 1003.2 standardに非常に良く準拠する\[33\]。[移植を前提としたBashシェルスクリプトは](../Page/移植_\(ソフトウェア\).md "wikilink")、最低でもBashをBourne Shellで置き換えた場合を考慮しなければならない。伝統的なBourne ShellにはないがBashには搭載されている機能は以下である\[34\]:

  - 特定の拡張呼び出しオプション
  - `$(`<var>`コマンド`</var>`)` 記法を使ったコマンド代替（ただしこの機能はPOSIX1003.2規格の一部）
  - ブレイス展開
  - 特定の配列演算と連想配列
  - テストコンストラクトを拡張する二重括弧
  - 二重括弧の算術評価コンストラクト
  - 特定の文字列操作操作
  - プロセス代替
  - 正規表現マッチング演算子
  - Bash特有の組み込み機能
  - コプロセス

とは、Bash以外のUnixシェルでは適切に動作しないBashコードの部分を指す\[35\]。

### キーボードショートカット

Bashはデフォルトの ([Emacs](../Page/Emacs.md "wikilink")) キーバインディングを利用して編集するためのコマンドライン用キーボードショートカットを提供するために、Readlineを利用する。`set -o vi`を起動すれば[Vi](../Page/Vi.md "wikilink")バインディングが利用可能となる\[36\]。

### プロセス管理

Bashにはコマンドに対する実行モードとして、バッチモードと並行実行モードの2つがある。

バッチモードつまりコマンドを逐次的に実行するためには、コマンドを「`;`」文字や別の行で分割する必要がある:

``` bash
コマンド1; コマンド2
```

上記の例では、<var>`コマンド1`</var> が完了した後で <var>`コマンド2`</var> が実行される。

<var>`コマンド1`</var> と <var>`コマンド2`</var> を並行実行するには、以下の方法で実行する必要がある:

``` bash
コマンド1 & コマンド2
```

上記の例では、<var>`コマンド1`</var> がバックグラウンド（シンボル `&`）で実行され、フォアグラウンドで <var>`コマンド2`</var> を実行するシェルへとすぐに制御が戻される。

プロセスはフォアグラウンド状態とバックグラウンド状態だけでなく、停止状態にすることも可能である。プロセスがフォアグラウンドで実行されていれば、これはをタイプすることで行える。バックグラウンドプロセスおよび停止されたプロセスの全てを一覧するには`jobs`を起動することで行える:

``` console
$ jobs
[1]-  Running                  コマンド1 &
[2]+  Stopped                  コマンド2
```

上記の出力では、括弧内の数はジョブIDを示している。プラス記号は `bg` や `fg` に対応するデフォルトプロセスを指し示す。RunningおよびStoppedという表示は、を指し示す。最後の文字列はプロセスを開始したコマンドである。

プロセスの状態は様々なコマンドを使うことで変更できる。`fg` コマンドはプロセスをフォアグラウンドにして、`bg` は停止されたプロセスをバックグラウンドで実行するよう設定する。`bg` と `fg` は最初の引数に処理するプロセスを指定するジョブIDを渡すことができる。引数がない場合、`jobs` の出力でプラス記号が付いたデフォルトプロセスに対して処理が行われる。プロセスに[シグナルを送って中断するためには](../Page/シグナル_\(Unix\).md "wikilink")、[`kill`](https://ja.wikipedia.org/wiki/kill "wikilink")コマンドを使うことができる。ジョブIDはパーセント記号 「`%`」の後に指定する必要がある:

``` bash
kill -s SIGKILL %1
```

### 条件付き実行

Bashは先行するコマンドにより設定された[終了コードに応じてコマンドを実行する](https://ja.wikipedia.org/wiki/終了ステータス "wikilink")、「条件付き実行」コマンド区切り文字を提供する。以下にその例を示す:

``` bash
cd ディレクトリー・パス && ./何かのコマンド || echo "エラーが発生しました。" >&2
```

`./`<var>`何かのコマンド`</var> は、`cd` コマンドが「成功」した（終了ステータスとして `0` を返した）場合のみ実行され、`echo` コマンドは `cd` か `./`<var>`何かのコマンド`</var> コマンドのどちらかがエラーを返した（終了ステータスが `0` 以外を返した）場合のみ実行される。

全てのコマンドに対して、終了ステータスは特殊な変数である `$?` に保存される。Bashは条件コマンド評価の形式として、 や  もサポートする。

### バグ報告

`bashbug` と呼ばれる外部コマンドはBashのバグを報告する。このコマンドが呼び出されると、フォームが入力された状態でユーザーのデフォルトエディタが表示される。このフォームはBashのメンテナ（またはオプションでそれ以外のメールアドレス）にメールされる\[37\]\[38\]。

## 脚注

## 関連項目

  -
## 外部リンク

  -
  - [bash(1)](https://manpages.debian.org/unstable/manpages-ja/bash.1.ja.html) - [Debian](../Page/Debian.md "wikilink")リファレンスマニュアル（日本語）

[Category:Unixシェル](https://ja.wikipedia.org/wiki/Category:Unixシェル "wikilink") [Category:GNUプロジェクト](https://ja.wikipedia.org/wiki/Category:GNUプロジェクト "wikilink") [Category:オープンソースソフトウェア](https://ja.wikipedia.org/wiki/Category:オープンソースソフトウェア "wikilink") [Category:ドメイン固有言語](https://ja.wikipedia.org/wiki/Category:ドメイン固有言語 "wikilink") [Category:1989年のソフトウェア](https://ja.wikipedia.org/wiki/Category:1989年のソフトウェア "wikilink")

1.
2.
3.
4.  [How to install Bash shell command-line tool on Windows 10](http://www.windowscentral.com/how-install-bash-shell-command-line-windows-10)
5.  [C Programming](http://www.ddj.com/cpp/184404693) by Al Stevens, [Dr. Dobb's Journal](https://ja.wikipedia.org/wiki/Dr._Dobb's_Journal "wikilink"), July 1, 2001
6.
7.
8.
9.
10.
11.
12.
13.
14.
15.
16.
17.
18.
19.
20.
21.
22.
23.
24. <https://www.linkedin.com/pub/st%C3%A9phane-chazelas/7/2a2/834>
25. <https://cve.mitre.org/cgi-bin/cvename.cgi?name=2014-6277>
26.
27.
28.
29. The syntax matches that shown on the [`regex(7)`](http://www.tin.org/bin/man.cgi?section=7&topic=regex) [manページ](https://ja.wikipedia.org/wiki/manページ "wikilink").
30.
31. "The shell provides associative array variables, with the appropriate support to create, delete, assign values to, and expand them." <http://tiswww.case.edu/php/chet/bash/NEWS>
32. C shellでは `~/.cshrc` がインタラクティブサブシェルのために呼び出される。また、[tcsh](https://ja.wikipedia.org/wiki/tcsh "wikilink") では `~/.tcshrc` が、その後 `~/.cshrc` がインタラクティブサブシェルのために呼び出される。
33.
34.
35. <https://linux.die.net/man/1/checkbashisms>
36.
37. [bashbug(1)](http://linux.die.net/man/1/bashbug), die.net
38. ["Linux / Unix Command: bashbug"](https://developer.apple.com/library/prerelease/mac/documentation/Darwin/Reference/ManPages/man1/bashbug.1.html), apple.com
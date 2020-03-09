> この記事は[Vim](https://ja.wikipedia.org/wiki/Vim)から翻訳されています。


**Vim**（**ヴィム**。「ヴィアイエム」という読み方は誤り\[1\]\[2\]）は、[vi](https://ja.wikipedia.org/wiki/vi "wikilink") から派生し、発展した高機能な[テキストエディタ](../Page/テキストエディタ.md "wikilink")である。

## 概要

Vimはオランダ人のプログラマーBram Moolenaarによって[Amiga](../Page/Amiga.md "wikilink")向けに開発された。のちに[Windowsを含むさまざまな環境に移植され](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")、特に[Unix系](https://ja.wikipedia.org/wiki/Unix系 "wikilink")オペレーティングシステム (OS) では[Emacs](../Page/Emacs.md "wikilink")と並んで広く使用されているテキストエディタとなっている。

Vimという名称は、オリジナルの[vi](https://ja.wikipedia.org/wiki/vi "wikilink")エディタに近づくことを目標として、開発当初**V**i **IM**itation（viの模倣）の略とされていた。しかし、やがてviを超えることを目指して**V**i **IM**proved（viの改良）とされるようになり、今日ではオリジナルのviを大きく上回る機能を持つに至っている。

Vimは[GUIを必要とせず](https://ja.wikipedia.org/wiki/グラフィカルユーザインタフェース "wikilink")[CUIでも動くため](../Page/キャラクタユーザインタフェース.md "wikilink")、Unix系OSに標準のエディタとして搭載されていることが多い。コンピュータの大容量化と高速化にともない、2000年以降のOSでは viに代わってより高機能な Vim、あるいはその機能劣化版が標準装備されるようになってきている。このため、コマンドライン上でviを実行すると代わりにVimが起動するディストリビューションが一般的となった。

Vimは基本的にCUIで動作するが、GUIで動くVimのことを特に**GVim**（gVim, gvim, ジーヴィム）と呼び区別している。マウス操作など、X GUI (Unix, Linux) /Windows GUI (Windows) であることを生かしたGVimにしかない機能もある。

viエディタと同様、キーボードのみで操作されることを前提としていたため、キーボードのみですべての操作が可能になっている。その基本的な操作方法はviと同じで、状況に応じてモードを使い分けることでテキストを編集していき、小さなコマンドの組み合わせをその場で作ることによって多種多様な機能を実現する。

Windows系エディタ（[メモ帳](https://ja.wikipedia.org/wiki/メモ帳 "wikilink")など）などの他のエディタとは操作方法がまるで異なるため、一通りのテキスト編集作業ができるようになるまで慣れが必要となる。しかしながら、一旦慣れてしまえばメモ帳などとは比較にならないほどのテキスト編集速度を得ることができるため、数多くのVim愛好家が存在する。Vimの他の機能と併せて、プログラムコードやシステム設定ファイルを編集するのに特化しているため、特にプログラマーやシステム管理者に利用者が多い。

vi系 (vi, Vim, [nvi](https://ja.wikipedia.org/wiki/nvi "wikilink")) のキーボード操作法は、エディタをはじめ、各種ビューワや、[ブラウザ](https://ja.wikipedia.org/wiki/ブラウザ "wikilink")のプラグインにいたるまでその後のソフトウェアの操作方法に強い影響を与えていった。

[Vim-split.png](https://ja.wikipedia.org/wiki/File:Vim-split.png "fig:Vim-split.png") Vimの大きな特徴として高いカスタマイズ性を挙げることができる。オリジナルのviがどんな環境でも設定なしですべての機能が利用できる万人向けのエディタだったのに対し、Vimでは設定ファイルを用いることでより個人の好みにあったエディタに[カスタマイズ](https://ja.wikipedia.org/wiki/カスタマイズ "wikilink")することができる。

エディタの詳細設定は主に `~/.vimrc`（Windows版では `%USERPROFILE%_vimrc`）というファイルに書いておき、起動時にVimがそれを読み込むことで設定が反映される仕組みになっている。Vimは独自のスクリプト言語 ([Vim script](https://ja.wikipedia.org/wiki/Vim_script "wikilink")) を用いて自身の機能を拡張することができ、かなり幅広い機能強化を行うことが可能である。有志らによって書かれた有用なスクリプトはプラグインとして [www.vim.org](http://www.vim.org/) 上や個人のブログ上で公開されている。`~/.vim`（windows版では `%USERPROFILE%\vimfiles`）フォルダ以下にこれらのプラグインファイルを置くことで機能を拡張できる。

Vimは、多言語、多コーデックを扱うことができ、[iconv](https://ja.wikipedia.org/wiki/iconv "wikilink")で対応しているものならばたいてい利用できる。しかし日本語などのマルチバイト文字を書くには不便が多く、もっぱら英文編集での利用が一般的である。

ライセンス形態は、GPL互換のチャリティウェアとなっており、いわゆるフリーでオープンソースなソフトウェアとして配布されており、Vimを起動すると[ウガンダ](https://ja.wikipedia.org/wiki/ウガンダ "wikilink")の子供たちへの援助を募るメッセージが表示される。

## モード切替

は複数のモードを用いてテキストの編集を行う。この独特な機能は初学者を混乱させやすい。

あらゆるエディタは、テキストの挿入とエディタに与えるコマンド指示を区別するという意味でモードを持つと言えるが、他のほとんどのエディタはこのモードを全く異なる方法で実装している。 は  と同様、モード毎にキー割り当ても切替わるという点において独自性を持つ。これによって、マウスやメニューを全く使わず、最低限の[メタキー](https://ja.wikipedia.org/wiki/メタキー "wikilink")の使用だけで全ての編集機能を使えるようになっている。

には6つの基本モードと5つの派生モードが存在する。しかしながら実質使用されるのは次の4つのモードであり、その他のモードは重要ではなく、特に意識されていない。

| モード        | 状態                                  |
| ---------- | ----------------------------------- |
| ノーマルモード    | カーソル移動やテキストの削除、コピー、ペーストなどの簡単な指示を行う。 |
| ビジュアルモード   | テキストを選択するだけのモード。                    |
| 挿入モード      | 実際にテキストを入力するモード。                    |
| コマンドラインモード | ファイルを開いたり、検索・置換などの様々な指示を行う。         |

その他のモード

  - 選択モード

      - 文字選択モード
      - 行選択モード
      - 矩形選択モード

  - モード

  - オペレータ待機モード

  - 置換モード

      - 仮想置換モード

  - (挿入モード)

      - 挿入ノーマルモード
      - 挿入ビジュアルモード
      - 挿入セレクトモード

  - (ビジュアルモード)

      - 文字ビジュアルモード
      - 行ビジュアルモード
      - 矩形ビジュアルモード

もっとも簡単な使い方の例としては、

1.  コマンドラインモードでファイルを開き、
2.  ノーマルモードでカーソルを移動させ、
3.  挿入モードでテキストを入力し、（ キーで再度ノーマルモードに戻り）
4.  コマンドラインモードでファイルを保存する。

### ノーマルモード

普通の編集コマンドを全て入力することができる。 カーソルの移動をしたり、いくつかのキーを押すことでショートカットのように編集することができる。

<table>
<thead>
<tr class="header">
<th><p>キーボード操作</p></th>
<th><p>コマンド表現</p></th>
<th><p>機能</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><p><code>j</code></p></td>
<td><p>下にカーソル移動</p></td>
</tr>
<tr class="even">
<td></td>
<td><p><code>k</code></p></td>
<td><p>上にカーソル移動</p></td>
</tr>
<tr class="odd">
<td></td>
<td><p><code>h</code></p></td>
<td><p>左にカーソル移動</p></td>
</tr>
<tr class="even">
<td></td>
<td><p><code>l</code></p></td>
<td><p>右にカーソル移動</p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p><code>dw</code></p></td>
<td><p>単語を削除</p></td>
</tr>
<tr class="even">
<td><p></p></td>
<td><p><code>yy</code></p></td>
<td><p>一行コピー</p></td>
</tr>
<tr class="odd">
<td><p>+</p></td>
<td></td>
<td><p>1ページ下にスクロール</p></td>
</tr>
</tbody>
</table>

エディタの起動時にはこのモードで始まり、他のモードはこのモードから起動する。全ての操作の中心となる重要なモード。他のモード中に  か +、+ を押すことでこのモードに移行できる。操作中にどのモードにいるのか分からなくなった場合は  を押すとノーマルモードに移行できる。

#### 演算子未解決モード

ノーマルモードの派生モード。「実行範囲の指示が必要なコマンド」を実行した場合にVimが指示を待っている状態。

例えば、ノーマルモードで キー\[3\]を押すとこのモードに入る。続けて  キーを押した場合は一行削除、\[4\]を押した場合は一単語削除、（行末の意）を押した場合は行末までを削除、となる。   とキーボード操作すると、カーソル位置から5行分の削除となる。

### ビジュアルモード

テキストの部分選択を行うだけのモード。選択後に別途コマンドを与えることにより、選択領域のコピーや削除を始めとしたテキスト処理を行う事が出来る。

テキスト選択中にも移動コマンドなどを行う事ができ、選択範囲を素早く変更できる。移動コマンド以外のコマンドを使うと選択領域に対してそのコマンドが実行される。

ノーマルモードから下記の操作でこのモードに移行できる。その区別は、

<table>
<thead>
<tr class="header">
<th><p>キーボード操作</p></th>
<th><p>コマンド表現</p></th>
<th><p>機能</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><p><code>v</code></p></td>
<td><p>文字単位のビジュアルモードに移行</p></td>
</tr>
<tr class="even">
<td></td>
<td><p><code>V</code></p></td>
<td><p>行単位のビジュアルモードに移行</p></td>
</tr>
<tr class="odd">
<td><p>+</p></td>
<td></td>
<td><p>矩形選択ビジュアルモードに移行</p></td>
</tr>
<tr class="even">
<td><p></p></td>
<td><p><code>gv</code></p></td>
<td><p>前回選択した範囲をもう一度選択</p></td>
</tr>
</tbody>
</table>

このモードの時にはコマンドラインに「」と表示される。

#### セレクトモード

ほとんどビジュアルモードと同じだが、印字可能文字が入力されると選択範囲を削除して挿入モードに入る。 の選択モードに似ている。

ノーマルモードから  、 で移行できる。また、ビジュアルモード時に + で移行できる。

このモードの時はコマンドラインに「」と表示される。

#### 挿入ビジュアルモード

挿入モードでビジュアル選択を開始したときのモード。

例えば + 、+ 、+ + を実行するとこのモードに入る。

このモードの時にはコマンドラインに「」と表示される。

#### 挿入セレクトモード

挿入モードでセレクトモードを開始したときのモード。

例えばマウスをドラッグしたり、+ を押したときこのモードに入る。

このモードの時にはコマンドラインに「」と表示される。

### 挿入モード

このモードでは、タイプされたテキストがそのまま書き込まれる（ のメモ帳などでテキストを入力する場合と同じ）。ノーマルモードから 、、、、、 などをタイプすることで挿入モードに移行できる。

<table>
<thead>
<tr class="header">
<th><p>キーボード操作</p></th>
<th><p>コマンド表現</p></th>
<th><p>機能</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><p><code>i</code></p></td>
<td><p>カーソル位置の前から挿入モードを開始する。</p></td>
</tr>
<tr class="even">
<td></td>
<td><p><code>I</code></p></td>
<td><p>行の先頭から挿入モードを開始する。</p></td>
</tr>
<tr class="odd">
<td></td>
<td><p><code>a</code></p></td>
<td><p>カーソル位置の後から挿入モードを開始する。</p></td>
</tr>
<tr class="even">
<td></td>
<td><p><code>A</code></p></td>
<td><p>行末から挿入モードを開始する。</p></td>
</tr>
<tr class="odd">
<td></td>
<td><p><code>o</code></p></td>
<td><p>カーソルの下に空行を挿入し、その先頭から挿入モードを開始する</p></td>
</tr>
<tr class="even">
<td></td>
<td><p><code>O</code></p></td>
<td><p>カーソルの上に空行を挿入し、その先頭から挿入モードを開始する</p></td>
</tr>
</tbody>
</table>

他にもこのモードに移行するためのコマンドがいくつかある。

このモード時にはコマンドラインに「」と表示される。

#### 挿入ノーマルモード

挿入モード時に一度だけノーマルモードのコマンドを実行できる。挿入モード時に +（または  キー）を押すのが面倒なときに使用される。

挿入モード時に、 + で挿入ノーマルモードに入る。

このモードの時にはコマンドラインに「」と表示される。

#### 置換モード

ノーマルモードからRでこのモードに移行する。文字をタイプするとその分文字が置換されていく。 抜けるには + を押す。

### コマンドラインモード

ウインドウの下部に一行のテキストを入力できる。

コマンドや関数の実行、検索、置換処理など多様な処理を行うことができる。

ノーマルモードから 、、を押すことで移行できる。

<table>
<thead>
<tr class="header">
<th><p>キーボード操作</p></th>
<th><p>機能</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><p>コロンに続けてコマンドを打ち込み、 キーで実行する。補完機能あり。ヘルプテキストには「<code>:sort</code>」などとコロンで始まるテキストで書いてある。</p></td>
</tr>
<tr class="even">
<td></td>
<td><p>前方検索を行う。続けて検索したい文字列のパターンを正規表現で入力し、 キーで検索を開始する。インクリメンタルサーチ可。</p></td>
</tr>
<tr class="odd">
<td></td>
<td><p>後方検索を行う。続けて検索したい文字列のパターンを正規表現で入力し、 キーで検索を開始する。インクリメンタルサーチ可。</p></td>
</tr>
<tr class="even">
<td></td>
<td><p>外部コマンドでフィルタ処理する。続けて実行するコマンド文字列を入力し、 キーでコマンド実行を開始する。</p></td>
</tr>
</tbody>
</table>

#### モード

コマンドラインモードの変種。コマンドラインモードとは次の点で異なる。

  - 毎回 （コロン）を押す必要がない。
  - コマンド実行後もモードに留まる。
  - コマンドを実行するごとに画面が更新されない。
  - 通常のコマンドライン編集機能が使えない。
  - マップと短縮入力が使えない。

ノーマルモードから 、  でモードに移行できる。  の場合はコマンドライン編集や補完が使えるようになる。 モードを抜けるときは `:vi`（または `:visual`）を使う。

## 起動と終了

### 起動方法

コマンドライン上で、次のコマンドを実行する。 下のコマンドは  のコマンドラインで動作するが、 版も基本的に同様のコマンドで起動できる。

| コマンド                                           | 概要        |
| ---------------------------------------------- | --------- |
| `vim [`*`options`*`] [`*`file``   ``..`*`]`    | ファイルを編集する |
| `vim -g [`*`options`*`] [`*`file``   ``..`*`]` | ファイルを編集する |
| `gvim [`*`options`*`] [`*`file``   ``..`*`]`   | ファイルを編集する |

詳しいコマンドラインオプションについて知りたいならば、次のいずれかのコマンドを実行する。

| コマンド         | 概要             |
| ------------ | -------------- |
| `man vim`    | `vim`のマニュアルを読む |
| `vim --help` | `vim`のヘルプを出力   |

`vim` について初めて学ぶ者は次のコマンドを実行するとチュートリアルを起動できる。

<table>
<thead>
<tr class="header">
<th><p>コマンド</p></th>
<th><p>概要</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><code>vimtutor [-g] [</code><em><code>言語</code></em><code>]</code></p></td>
<td><ul>
<li><code>-g</code> オプションで <code>gvim</code> 起動。</li>
<li><em>言語</em>を <code>ja</code> にすると日本語でチュートリアルを始められる。</li>
</ul></td>
</tr>
</tbody>
</table>

以下に  関連のコマンドをまとめる。

<table>
<thead>
<tr class="header">
<th><p>コマンド</p></th>
<th><p>概要</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li><code>vim</code></li>
</ul></td>
<td><p>通常起動。デフォルト。</p></td>
</tr>
<tr class="even">
<td><ul>
<li><code>ex</code></li>
</ul></td>
<td><p>モードで起動。ノーマルモードに戻るには <code>:vi</code> を実行。 <code>-e</code> オプションを付けた場合と同じ。</p></td>
</tr>
<tr class="odd">
<td><ul>
<li><code>view</code></li>
</ul></td>
<td><p>読み取り専用（リードオンリー）モードで起動。<code>-R</code> オプションを付けた場合と同じ。</p></td>
</tr>
<tr class="even">
<td><ul>
<li><code>gvim</code></li>
<li><code>gview</code></li>
</ul></td>
<td><p>GUIバージョン。<code>-g</code> オプションを付けた場合と同じ。</p></td>
</tr>
<tr class="odd">
<td><ul>
<li><code>evim</code></li>
<li><code>eview</code></li>
</ul></td>
<td><p>GUIバージョンのイージー（簡単）モードで起動。<code>-y</code> オプションを付けた場合と同じ。</p></td>
</tr>
<tr class="even">
<td><ul>
<li><code>rvim</code></li>
<li><code>rview</code></li>
<li><code>rgvim</code></li>
<li><code>rgview</code></li>
</ul></td>
<td><p>制限版。<code>-Z</code> オプションを付けた場合と同じ。</p></td>
</tr>
<tr class="odd">
<td><ul>
<li><code>vimtutor</code></li>
</ul></td>
<td><p>チュートリアルを起動。</p></td>
</tr>
</tbody>
</table>

実際には、`vim` コマンド以外はほぼ `vim` のオプションで代替できるので、環境によっては用意されていないこともある。

### 終了方法

Vimを終了させたい時は、

<table>
<thead>
<tr class="header">
<th><p>キーボード操作</p></th>
<th><p>コマンド表現</p></th>
<th><p>機能</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p> </p></td>
<td><p><code>:q</code></p></td>
<td><p>バッファを一つ閉じる。<code>:quit</code> と同じ。他に開いているウインドウがあればアプリケーション自体は閉じない。</p></td>
</tr>
<tr class="even">
<td><p>  </p></td>
<td><p><code>:qa</code></p></td>
<td><p>開いているバッファを全て閉じる。<code>:qall</code>、<code>:quitall</code> と同じ。 保存して終了させたい時は、</p></td>
</tr>
<tr class="odd">
<td><p>  </p></td>
<td><p><code>:wq</code></p></td>
<td><p>現在のバッファを保存して閉じる。</p></td>
</tr>
<tr class="even">
<td><p> </p></td>
<td><p><code>:x</code></p></td>
<td><p><code>:wq</code> とほぼ同だが、書き込みが行われるのは変更点がある時だけである。</p></td>
</tr>
<tr class="odd">
<td><p>   </p></td>
<td><p><code>:wqa</code></p></td>
<td><p>全てのバッファを保存して閉じる。</p></td>
</tr>
<tr class="even">
<td><p>  </p></td>
<td><p><code>:xa</code></p></td>
<td><p><code>:wqa</code> とほぼ同じだが、書き込みが行われるのは変更点がある時だけである。</p></td>
</tr>
</tbody>
</table>

中断したい時は、ノーマルモードで + を押す。 ではタスクバーに最小化されるが、端末版ではプロセスをバックグラウンドに移す。

また、ノーマルモード時に   で保存せずに終了、ノーマルモード時に   で保存して終了となる。

## 機能

### 概要

前身である[vi](https://ja.wikipedia.org/wiki/vi "wikilink")が機能を絞ったコンパクトな印象を一般に持たれているのと比べると、Vimはかなり巨大なアプリケーションである。 Vimはバージョンを重ねるごとに積極的に機能を追加する傾向があり、実装されている機能の種類、数は公開されているエディタの中でもトップクラスに多い。ただし設定によりviに近い操作性に戻すことも可能であり、いくつかのLinuxディストリビューションでは機能を絞ったvimをviとして配布しているものもある。

以下に示す機能の中には設定でオフにしたり、好みに合わせてカスタマイズ可能なものが多く、必ずしも説明と一致しない場合があることに注意。

### テキスト編集機能

テキストエディタとして基本的な機能は揃っている。

  - 多段階アンドゥ（元に戻す）とリドゥ（やり直す）
  - コピー（ヤンク）＆ペースト
  - 豊富なカーソル移動
  - 豊富な選択方法（語選択・行選択・矩形選択・段落選択）
  - スペルチェック

#### オペレータと範囲指定

オペレータとは、コピー（: yank）、削除（: delete）、変更（: change）、選択（: visual）といった操作の意味を決定づけるキーである。ただし、このキー単独では操作は完結せず、ここに範囲を指定するコマンドが続くことで、単語の削除や、カッコ内の選択、パラグラフのコピーなどの多彩なアクションが可能になる。

範囲を指定するコマンドには、移動系のキー（     など）や、テキストオブジェクト（`iw`, `i"`, `a"`, `a(`など）がある。

Vimでは、その場で適切なオペレータと範囲指定コマンドの組み合わせを考え、実行していくことで編集を行っていく。

例えば、コマンド`ggVG`は、分解すると「一番上に移動（`gg`）して行選択（`V`）を一番下まで（`G`）」となるので、「すべて選択」の意味になる。

| コマンド  | オペレータ | 範囲指定              |
| ----- | ----- | ----------------- |
| `y$`  | コピー（） | カーソル位置から行末まで（）    |
| `daw` | 削除（）  | カーソル下の単語（ ）       |
| `ci"` | 変更（）  | `""`で囲まれたテキスト（ ）  |
| `vip` | 選択（）  | 空行で挟まれたパラグラフ全体（ ） |

#### マーク

文章中の特定の位置にマークを付け、カーソルを移動する際の目印にすることができる。

ノーマルモード中に+(適当なアルファベット1文字) を入力すると、現在のカーソル位置を記憶する。

ノーマルモード中に+(先ほど指定したアルファベット1文字) を入力すると、先ほど記憶したカーソル位置にジャンプする。

#### レジスタ

レジスタとは、テキストの断片を一時保存しておく場所のことで、[クリップボード](https://ja.wikipedia.org/wiki/クリップボード "wikilink")とほぼ同じ概念だが、複数個のスペースが用意されている点が異なる。アルファベット一文字に1スペースが割り当てられており、ノーマルモード中に+(適当なアルファベット1文字) を入力することでレジスタにアクセスできる。例えば   でレジスタaにカーソルから文末までヤンク（コピー）することができ、   で貼り付けられる。

#### マクロ

[マクロとは](https://ja.wikipedia.org/wiki/マクロ_\(コンピュータ用語\) "wikilink")、操作を記録して別の場所で同じ操作を繰り返し行うときに有用な機能である。

ノーマルモード中に+(適当なアルファベット1文字) を入力すると記録状態になり、再びを打ち込むまでの間のタイプしたキーが保存される。

ノーマルモード中に+(先ほど指定したアルファベット1文字) を入力すると記録された操作を再生できる。

#### ジャンプ

Vimではカーソル位置が大きく動き、バッファ間でも頻繁に移動することが多い。そのため、カーソル位置の履歴を記憶している。

直前のカーソル位置に戻りたい場合ノーマルモードでを押す。逆に進みたい場合はを押す。

外部コマンド`ctags`でタグリストを予め作成しておけば、カーソル下の単語の意味や関数の定義を調べたい場合に、を押すことで、その定義元にジャンプすることができる。これを特にタグジャンプと呼ぶ。

### インデントとタブ

ファイルタイプごとに、適切な自動改行（オートインデント）を行うことができる。Vimではデフォルトで40以上のプログラミング言語の自動改行に対応している。自動入力されるスペース（またはタブ文字）の数は任意に決めることが可能で、後述するハイライト機能によって可視化することもできる。 また、タブ文字は`:expandtab`でスペースに一括変換することもできる。

### 検索・置換・ソート

バッファ内の特定のテキストを検索および置換することができる。検索にマッチした単語はハイライトできる。 検索単語には正規表現を用いることができ、複雑なテキストにもマッチさせることができる。

ノーマルモード中にまたはを押すと、バッファ内の単語を検索できる。

ノーマルモード中にまたはを押すと、カーソル下の単語を検索できる。

コマンドモードで `:s/OLD/NEW/` を入力することで OLDをNEWに置換することができる。

コマンドモードで `:sort` を入力することでテキストを行単位で並べ替えることができる。

### 補完

[screenshot_vim7_word_completion.png](https://ja.wikipedia.org/wiki/File:screenshot_vim7_word_completion.png "fig:screenshot_vim7_word_completion.png")

挿入モード中に, を押すと、文中の単語をポップアップ表示、補完することができる。 コマンドモード中でも補完はでき、機能名がうろ覚えでもサジェストしてくれる（`:help wildmenu`）。 プラグインを用いれば、コードスニペットや、時刻、関数名などの自由度の高い補完も可能になる。

### ファイル管理

  - 保存時に自動バックアップ
  - エディタが強制終了した場合でも、直前の場所から編集を再開できる（`:help swapfile`, `:help viminfo`）。

### ユーザーインターフェイス

[Screenshot-vim2.png](https://ja.wikipedia.org/wiki/File:Screenshot-vim2.png "fig:Screenshot-vim2.png")

  - 行番号やルーラー（横目盛）を表示
  - ステータスバーの表示内容変更
  - ビジュアルベル
  - カーソル行の強調
  - フォントの変更（gVimのみ）
  - アイコン付きツールバー（gVimのみ）
  - マウスの利用（gVimおよび対応した端末のみ）

### 強調表示（シンタックスハイライト）

ソースコード・テキストファイルの色分けを行い見やすく表示する。Vimでは非常に多くの文法を色分けすることが可能であり、デフォルトで400種類以上用意されている。この数は他のテキストエディタと比較しても群を抜いている。特にVimでは、UNIXの設定ファイルを編集するケースが多いことから`/etc`配下の多くのファイルが色分け表示される。この機能は、gVimだけでなく、カラー表示が可能な端末上でも利用できる。

このシンタックスの定義ファイルは、正規表現を駆使することで必要に応じて拡張できる。 また、色分けのカラースキームも自由に変更することができ、自分の好みに応じて様々に使い分けることができる。

#### 折り畳み（フォールディング）

プログラマ支援機能の一つで、長い段落・関数などは折りたたんで、コンパクトに表示したほうが俯瞰しやすくなる。 いくつかの折り畳み方法があり、自分で範囲を指定して折り畳むことも可能だが、自動で判別して折り畳ませることもできる。

### マルチバッファ・ウインドウ分割・タブページ

[Vim-(logiciel)-script-calendar.png](https://ja.wikipedia.org/wiki/File:Vim-\(logiciel\)-script-calendar.png "fig:Vim-(logiciel)-script-calendar.png")

一つのVimウインドウの中で、複数のテキストを同時並行で編集することができる。 ウインドウを上下左右、任意の個数に分割して使い分けることができる。 これを利用して、片側にファイルツリーを表示したり、シェルを表示したり、ヘルプを表示したりすることが可能になる。

#### 差分表示

[Vim-(logiciel)-diff-repli.png](https://ja.wikipedia.org/wiki/File:Vim-\(logiciel\)-diff-repli.png "fig:Vim-(logiciel)-diff-repli.png")

ファイルの変更点を分かりやすく比較するために、ウインドウを左右に分割して差分表示を行う機能がある。 このとき変更点は色分け・折り畳みがなされ、左右画面ともに同時スクロールする。

#### Quickfix

[統合開発環境](../Page/統合開発環境.md "wikilink")と同様、ソースファイルを編集した後Vimから直接[コンパイル](https://ja.wikipedia.org/wiki/コンパイル "wikilink")できる。[コンパイルエラーが発生したときには](../Page/コンパイラ.md "wikilink")、Quickfixと呼ばれるもう一つのウィンドウが表示される。[エラーメッセージ](https://ja.wikipedia.org/wiki/エラーメッセージ "wikilink")に基づいて、直接他のウィンドウ内に表示されたソースファイルのエラーの出た箇所へジャンプすることができる（`:help quickfix`参照）。

### キーマッピングの変更・コマンド定義

ノーマル・挿入・ビジュアル・コマンドモードのキーマッピングを自由に変更できる。 特に長くて記憶できないが有用なキーバインドを短く定義し直すのに使われる。 独自の処理を行うコマンドも定義することができ、役に立つものはプラグインとして公開されている。

### ヘルプ

[Vim-(logiciel)-aide.png](https://ja.wikipedia.org/wiki/File:Vim-\(logiciel\)-aide.png "fig:Vim-(logiciel)-aide.png")

Vimにはテキスト形式の膨大な[ドキュメントが存在する](https://ja.wikipedia.org/wiki/文書 "wikilink")。`:helpgrep`か`:help`コマンドを用いれば、ユーザはヘルプ全体の中から単語を探すことがでる。このヘルプテキストはあちこちにタグ名が記載されており、Wikiのようにタグジャンプを駆使して分からない単語の説明に移動できる。

## カスタマイズ

は  とは異なり、個人の好みに合わせて徹底的に[カスタマイズできる](https://ja.wikipedia.org/wiki/カスタム "wikilink")。 は環境非依存で特に設定せずに使うのが一般的だが、プログラマ向けの  は設定を多用して各個人向けに使いやすくするのが一般的である。その設定の範囲は基本的な[インタフェースから](https://ja.wikipedia.org/wiki/インタフェース_\(情報技術\) "wikilink")、キーボードマクロまで幅広い。

は、後述する独自のスクリプト言語（スクリプト、`:help vim-script-intro`）を持っており、カスタマイズ処理は主にこの言語で記述する。 や個人のブログ上で、便利なスクリプトが[プラグイン](../Page/プラグイン.md "wikilink")として公開されている。

の初期設定は主に `~/.vimrc`\[5\]というテキストファイルで行い、`~/.vim` ディレクトリ\[6\]に多数のプラグインスクリプトを配置することによって機能拡張を実現する。個人の設定は多種多様だがほとんどのユーザーは、`~/.vimrc` には[オプション](https://ja.wikipedia.org/wiki/オプション "wikilink")（`:help options`）やキーマップの変更などを記述する。

`set` コマンドでオプションを設定する。 オプションの名前に `no` を付けるとその否定になる。

<table>
<thead>
<tr class="header">
<th><p>コマンド</p></th>
<th><p>意味</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><code>set nocompatible</code></p></td>
<td><p>と互換モードにしない</p></td>
</tr>
<tr class="even">
<td><p><code>set number</code></p></td>
<td><p>行番号を表示する</p></td>
</tr>
<tr class="odd">
<td><p><code>set autoindent smartindent</code></p></td>
<td><p>プログラミング用に自動インデントする</p></td>
</tr>
<tr class="even">
<td><p><code>set expandtab</code></p></td>
<td><p>タブ文字をスペース文字に変換する</p></td>
</tr>
<tr class="odd">
<td><p><code>set nobackup</code></p></td>
<td><p>バックアップをとらない。</p></td>
</tr>
<tr class="even">
<td><p><code>syntax on</code></p></td>
<td><p>構文強調表示機能を有効にする</p></td>
</tr>
<tr class="odd">
<td><p><code>nnoremap ; :</code></p></td>
<td><p>キーマップの変更。</p></td>
</tr>
<tr class="even">
<td><p><code>vnoremap ; :</code></p></td>
<td><p>キーマップの変更。</p></td>
</tr>
<tr class="odd">
<td><p><code>inoremap </code><C-a><code> </code><C-o><code>0</code></p></td>
<td><p>キーマップの変更。</p></td>
</tr>
<tr class="even">
<td><p><code>inoremap </code><C-e><code> </code><C-o><code>$</code></p></td>
<td><p>キーマップの変更。</p></td>
</tr>
</tbody>
</table>

`~/.vim` 以下はある程度用途ごとにディレクトリが分けられている。 ダウンロードしたプラグインは指定されたディレクトリに置くことで動作する。

細かい説明は[ のディレクトリ構成](http://vim-jp.org/vim-users-jp/2009/06/30/Hack-34.html)を参照。

    ~/.vimrc
    ~/.vim/
        after/
        autoload/
        compiler/
        colors/
        doc/
        plugin/
        ftdetect/
        ftplugin/
        syntax/
        indent/
        macros/

### Vimスクリプト

Vimには独自の[スクリプト言語](../Page/スクリプト言語.md "wikilink")（**Vimスクリプト**, 言語に着目した場合**VimL**とも略される, 詳細は[Vim script](https://ja.wikipedia.org/wiki/Vim_script "wikilink")）が備わっており、それを用いれば[マクロで対応するのが難しいような複雑な作業を自動化できる](https://ja.wikipedia.org/wiki/マクロ_\(コンピュータ用語\) "wikilink")。Vimの設定ファイル類（vimrc、プラグイン、インデント定義、シンタックス定義、カラースキーム、ファイルタイプ判別）はすべてVimスクリプトであり、変更すれば挙動を細かくカスタマイズできる。通常はユーザーのホームディレクトリ以下の設定ファイル群でこれらの設定を上書きして利用する。Vimのコマンドモードとは、このVimスクリプトを一行実行しているにすぎない。`:normal`を使うことでノーマルモードのコマンドもVimスクリプト上で利用できる。

Vimスクリプトは、[Javascript](https://ja.wikipedia.org/wiki/Javascript "wikilink")に近い言語仕様を採用しており、[while文](https://ja.wikipedia.org/wiki/while文 "wikilink")や[if文](https://ja.wikipedia.org/wiki/if文 "wikilink")などの一般的な制御構文から、リストやハッシュなどのデータ構造までをサポートしているが、オブジェクト指向言語のように厳密な[クラス](https://ja.wikipedia.org/wiki/クラス "wikilink")や[継承](https://ja.wikipedia.org/wiki/継承 "wikilink")の概念はない。しかしながら、モード概念と絡んでいることもあって文法が複雑であり、文法や挙動に一貫性が無い部分もある（例：`.`演算子など）。このため、Vimスクリプトでバグの少ないプラグインを書くのは慣れが必要となる。また、Vimスクリプトは、[Python](../Page/Python.md "wikilink")や[Lisp](https://ja.wikipedia.org/wiki/Lisp "wikilink")、[Lua](https://ja.wikipedia.org/wiki/Lua "wikilink")などといった他のスクリプト言語と比較すると、パフォーマンスが悪いケースが多いが、これはスクリプトを行ごとに逐次実行していることによる。

コンパイル時に  に追加できる  や  や  などのインタフェースを使用すれば、Vimスクリプトの中でインラインに他言語を利用することもできる。ただし、Vimの機能にアクセスするためにはVimスクリプトの関数をevalするなどして間接的に呼び出すしかなく、完全な代替にはなっていない。

VimスクリプトはVimのカスタマイズ性の中核を担っているが、上述した文法や性能の問題から弱点を認め、他言語への転換を図ることを目的の一つとしてNeovimがフォークしている。

## プラグイン

プラグインのVimスクリプトは、`~/.vim`以下の適当な場所に配置することで動作する。Vim.orgでホストされているVimのプラグインは、もともと小さな機能をもったスクリプトが多かった。しかしながら、2000年代後半以降Vimには高性能で多機能なプラグインが急激に増加してきた。その背景には、コンピュータの高性能化や、Vimスクリプトのハックが進んだことなどが挙げられる。しかし、Vim.org からダウンロードしてきた第三者によるプラグインファイル（しばしば複数のファイルから成る）は、自分で解凍して複数のディレクトリに配置しなければならなかった。このため、自分の書いた設定ファイルと、第三者の書いたプラグインとが混在し、プラグインが増加するにつれて管理が複雑化することが多かった。

### プラグインの管理

#### Vimball による管理

プラグイン管理の負担を軽減するために、Vimがバージョン7になると、**Vimball**（ヴィムボール）と呼ばれる機能が搭載されるようになった。これはプラグインをVimballという形式に圧縮して単一のファイルでプラグインを提供しようとするものである。このVimballを使うことでプラグインのインストール・アンインストールを簡便に行う事ができ、プラグインのインストール面での負担が軽減された。Vimball形式で提供されているプラグインをインストールするには、Vim.org からダウンロードしてきたファイル（拡張子 **.vba**）を手持ちのVimエディタで開き、`:so %` を実行することで自動的に展開・インストールされる。このときインストールしたプラグイン情報も同時に記録されるのでアンインストールもできる。アンインストールするには`:RmVimball [プラグインの名前]`を入力する（使用方法の詳細は`:help vimball`）。

しかしながらVimball形式に対応したスクリプトが非常に少なかったことや、プラグインのバージョン管理まで面倒を見てくれなかったことから、プラグイン管理の負担が劇的に改善されることはなく、現在は主流の管理方法ではなくなってきており、[Git](https://ja.wikipedia.org/wiki/Git "wikilink")を用いた方法に移行しつつある。

#### GitHub による管理

2000年代後半になるとプラグインの管理方法は大きく変わりはじめた。それは[GitHub](https://ja.wikipedia.org/wiki/GitHub "wikilink")の登場によって多数のプラグインが、分散型バージョン管理システム[Git](https://ja.wikipedia.org/wiki/Git "wikilink")で管理されるようになってきたためである。GitHubが個人に無料でスペースを提供したため、自分の設定ファイル群である `~/.vim` (`dotvim`, `vimfiles`) をGitHub上で管理する者が増加し、プラグイン管理もすべてGitで管理したいという需要が出てきた。

まず、pathogen（パソゲン、Tim Pope作）というプラグインが登場した。これは自分の`~/.vim`全体をGitで管理し、第三者プラグインはGitのsubmodule機能によって管理するようにした。これのプラグインの登場により、第三者プラグインと自分の書いたプラグインとを別々に管理できるようになったことで、Vimball形式の時の問題点はほとんど解決され、プラグイン管理の負担を劇的に低減させることに成功した。さらにGitを使った利点として、自分で好きなようにフォークして変更できることも大きなメリットであった。

しかし、Gitによってプラグインの更新が楽になったとはいえ、その更新もインストールもプラグインごとに管理しなければならない点は変わらなかった。2010〜2011年になると、その部分を自動化し改良したVimスクリプトが登場し始める。このようなスクリプトの代表例としてVundle（バンドル、gmarik作）が挙げられる。これらのスクリプトを用いることで使いたいプラグインの名前やレポジトリを列挙するだけで、コマンドひとつで一括インストール、一括更新が可能になった。これに呼応する形でVim.orgにアップロードされていたプラグインもその殆どがGitHub上に移植された\[7\]。

これらのプラグイン管理用のプラグインが整備されたことにより、初期（数年前まで）の管理方法に比較するとVimのプラグイン管理の環境は格段に向上した。

## 歴史

誕生のきっかけは、ブラム・ムーリナー\[8\]が1980年代の終わりにコンピュータを購入したことによる。彼はエディタとしてを使おうとしたが、当時用のは存在しなかった。そこでviのクローンを元にしてのバージョン1.0を開発した。最初の第一目標はの機能をまねることだったので、その頃の は （の模造品）の略とされていた。1991年にのバージョン1.14がいわゆる「 ディスク \#591」という用の[フリーウェア](../Page/フリーウェア.md "wikilink")集に収録され、公開されることとなった。

<table>
<thead>
<tr class="header">
<th><p>日時</p></th>
<th><p>バージョン</p></th>
<th><p>変更点</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>nowrap|1987年7月</p></td>
<td><p>N/A</p></td>
<td><p>ティム・トンプソンが  向けに  クローン [9]を公開した。ソースコードは [10][11]に投稿された。</p></td>
</tr>
<tr class="even">
<td><p>nowrap|1988年6月</p></td>
<td><p>N/A</p></td>
<td><p>トニー・アンドリュースが  を改良し、とに移植し、バージョン3.10として[12][13]に投稿した。</p></td>
</tr>
<tr class="odd">
<td><p>nowrap|1988年</p></td>
<td><p>1.0</p></td>
<td><p>ブラム・ムーリナーが  を元にして  向けに[14]を開発した。ただし非公開。</p></td>
</tr>
<tr class="even">
<td><p>nowrap|1991年11月2日</p></td>
<td><p>1.14[15]</p></td>
<td><p>がの #591[16]に収録された。</p></td>
</tr>
<tr class="odd">
<td><p>nowrap|1992年</p></td>
<td><p>1.22[17]</p></td>
<td><p>とに移植された。</p></td>
</tr>
<tr class="even">
<td><p>nowrap|1993年11月14日</p></td>
<td><p>2.0</p></td>
<td><p>このバージョンから  は  の略称とされた。</p></td>
</tr>
<tr class="odd">
<td><p>nowrap|1994年8月12日</p></td>
<td><p>3.0[18]</p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/Windows" title="wikilink">Windows</a>をサポート。複数バッファ機能。</p></td>
</tr>
<tr class="even">
<td><p>nowrap|1996年5月29日</p></td>
<td><p>4.0[19][20]</p></td>
<td><p>版の公開</p></td>
</tr>
<tr class="odd">
<td><p>nowrap|1998年2月19日</p></td>
<td><p>5.0[21][22]</p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/シンタックスハイライト" title="wikilink">シンタックスハイライト</a>とスクリプト言語（ユーザ定義関数、コマンド）のサポート</p></td>
</tr>
<tr class="even">
<td><p>nowrap|1998年4月6日</p></td>
<td><p>5.1</p></td>
<td><p>バグ修正と様々な改良</p></td>
</tr>
<tr class="odd">
<td><p>nowrap|1998年4月27日</p></td>
<td><p>5.2</p></td>
<td><p>長期サポート、ファイルブラウザ、ダイアログ、ポップアップメニュー、セレクトモード、ユーザ定義関数、ユーザ定義コマンド、のサポートなど</p></td>
</tr>
<tr class="even">
<td><p>nowrap|1998年8月31日</p></td>
<td><p>5.3</p></td>
<td><p>バグ修正</p></td>
</tr>
<tr class="odd">
<td><p>nowrap|1999年7月25日</p></td>
<td><p>5.4</p></td>
<td><p>簡単なファイル暗号化、様々な改良</p></td>
</tr>
<tr class="even">
<td><p>nowrap|1999年9月19日</p></td>
<td><p>5.5</p></td>
<td><p>バグ修正と様々な改良</p></td>
</tr>
<tr class="odd">
<td><p>nowrap|2000年1月16日</p></td>
<td><p>5.6</p></td>
<td><p>新しいシンタックスファイル。バグ修正など。</p></td>
</tr>
<tr class="even">
<td><p>nowrap|2000年6月24日</p></td>
<td><p>5.7</p></td>
<td><p>同上</p></td>
</tr>
<tr class="odd">
<td><p>nowrap|2001年5月31日</p></td>
<td><p>5.8</p></td>
<td><p>同上</p></td>
</tr>
<tr class="even">
<td><p>nowrap|2001年9月26日</p></td>
<td><p>6.0[23][24]</p></td>
<td><p>折りたたみ、プラグイン、多言語サポート、垂直分割ウインドウなど。</p></td>
</tr>
<tr class="odd">
<td><p>nowrap|2002年3月24日</p></td>
<td><p>6.1</p></td>
<td><p>バグ修正</p></td>
</tr>
<tr class="even">
<td><p>nowrap|2003年6月1日</p></td>
<td><p>6.2</p></td>
<td><p>GTK2、アラビア語のサポート、バグ修正など</p></td>
</tr>
<tr class="odd">
<td><p>nowrap|2004年6月7日</p></td>
<td><p>6.3</p></td>
<td><p>マーク機能、翻訳、バグ修正など</p></td>
</tr>
<tr class="even">
<td><p>nowrap|2005年10月15日</p></td>
<td><p>6.4</p></td>
<td><p>外部スクリプト言語インタフェースの追加（、、）、多数のバグ修正など</p></td>
</tr>
<tr class="odd">
<td><p>nowrap|2006年5月7日</p></td>
<td><p>7.0 [25]</p></td>
<td><p>スペルチェック、自動補完、タブページ、ハイライト機能の強化、アンドゥー機能の改良など</p></td>
</tr>
<tr class="even">
<td><p>nowrap|2007年3月12日</p></td>
<td><p>7.1</p></td>
<td><p>シンタックスファイルの追加、ランタイムファイル、バグ修正など</p></td>
</tr>
<tr class="odd">
<td><p>nowrap|2008年8月9日</p></td>
<td><p>7.2 [26]</p></td>
<td><p>スクリプトでの浮動小数点のサポート、スクリーン描画のコードのリファクタング、シンタックスファイルの追加、など</p></td>
</tr>
<tr class="even">
<td><p>nowrap|2010年8月15日</p></td>
<td><p>7.3</p></td>
<td><p>スクリプト言語と3をサポート。 暗号化、 制限なしアンドゥーとリドゥー</p></td>
</tr>
<tr class="odd">
<td><p>2013年8月10日</p></td>
<td><p>7.4</p></td>
<td><p>新しい高速な正規表現エンジン</p></td>
</tr>
<tr class="even">
<td><p>2016年9月12日</p></td>
<td><p>8.0</p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/非同期IO" title="wikilink">非同期IO</a>、ジョブ管理、ラムダ演算とクロージャ、標準設定の強化、Windows版での<a href="https://ja.wikipedia.org/wiki/DirectWrite" title="wikilink">DirectWrite</a>対応、GTK+3対応、テストフレームワークなど[27]</p></td>
</tr>
<tr class="odd">
<td><p>2018年5月18日</p></td>
<td><p>8.1</p></td>
<td><p>バグフィックス、ドキュメント更新、ターミナルウィンドウなど</p></td>
</tr>
<tr class="even">
<td><p>2019年12月12日</p></td>
<td><p>8.2</p></td>
<td><p>ポップアップ・ウィンドウ(情報のフローティング表示が可能に)、テキストプロパティ、Language Server Protocol(LSP)対応の強化、スクリプトの機能強化など[28]</p></td>
</tr>
</tbody>
</table>

### 移植された環境

エディタはもともと上でしか動作しなかったが、は （公開時のプラットフォーム）だけでなく、、、、[{{lang](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")、[IBM](../Page/IBM.md "wikilink")  と [OS/390](https://ja.wikipedia.org/wiki/OS/390 "wikilink")、、、[QNX](https://ja.wikipedia.org/wiki/QNX "wikilink")、、、、[BSD](https://ja.wikipedia.org/wiki/BSD "wikilink")、\[29\]、[{{lang](https://ja.wikipedia.org/wiki/macOS "wikilink")\[30\]など、多数のプラットフォームに移植されてきた。

また、独立した移植版が\[31\]と[iOS](https://ja.wikipedia.org/wiki/iOS_\(アップル\) "wikilink")\[32\]でも動作する。

## Vimの派生エディタ

Viをモデルとした派生物には[nvi](https://ja.wikipedia.org/wiki/nvi "wikilink")や[Elvis](https://ja.wikipedia.org/wiki/Elvis "wikilink")があり、中でも最も機能的に発展したのがVimである。そのVimをモデルとしたプロジェクトもいくつかあるが、Vimの機能群は巨大なため、全てを模倣するのは困難であることから、結局Viクローンと同程度の機能実装にとどまっている。逆にVimの機能を制限して操作の敷居を低くした[Creamという派生物もある](https://ja.wikipedia.org/wiki/Cream_\(テキストエディタ\) "wikilink")。

### Neovim

現在、派生物の中で最も精力的に開発されているプロジェクトはNeovim (nvim)であり、Vimの[リファクタリングプロジェクトであることから](https://ja.wikipedia.org/wiki/リファクタリング_\(プログラミング\) "wikilink")、基本的な部分はVimとほぼ変わらないものの、新機能の追加やもはや使われなくなった機能の削除などが行われている。GUIアーキテクチャの改善や、スクリプトの高速化、他アプリケーションへの埋め込みが容易になることが謳われている。

## Vimと似た操作体系をもつアプリケーション

ViおよびVimの操作体系は、数多くのソフトウェアに継承もしくはエミュレートされている。ここでは一部の例を挙げる。

他のテキストエディタにおいてもショートカットキーの薄いラッパーのような形でプラグイン化される例が多い。

  - [Atom](https://ja.wikipedia.org/wiki/Atom_\(テキストエディタ\) "wikilink")（Vim-modeプラグイン）
  - [Sublime Text](https://ja.wikipedia.org/wiki/Sublime_Text "wikilink")（Vintage, Vintageousプラグイン）
  - [Emacs](../Page/Emacs.md "wikilink")（Evilプラグイン）
  - [Eclipse](../Page/Eclipse_\(統合開発環境\).md "wikilink")（Vrapperプラグイン）
  - [Kate](https://ja.wikipedia.org/wiki/Kate "wikilink")（VI Input mode）
  - [Xcode](https://ja.wikipedia.org/wiki/Xcode "wikilink")（Xvimプラグイン）

また、片指で移動ができることはPDF・画像ビューワーやブラウザと相性がよい。

  - [Mozilla Firefox](../Page/Mozilla_Firefox.md "wikilink")（[Vimperator](https://ja.wikipedia.org/wiki/Vimperator "wikilink")・[Pentadactyl](https://ja.wikipedia.org/wiki/Pentadactyl "wikilink")・[VimFx](https://ja.wikipedia.org/wiki/VimFx "wikilink")[アドオン](https://ja.wikipedia.org/wiki/アドオン "wikilink")）
  - [Google Chrome](https://ja.wikipedia.org/wiki/Google_Chrome "wikilink")（[Vimium](https://ja.wikipedia.org/wiki/Vimium "wikilink")拡張）
      - [Gmail](https://ja.wikipedia.org/wiki/Gmail "wikilink")や[Google Driveなど](https://ja.wikipedia.org/wiki/Google_Drive "wikilink")[Google](https://ja.wikipedia.org/wiki/Google "wikilink")が提供するWebサービスは，Vimに似た[ショートカット](https://ja.wikipedia.org/wiki/ショートカット "wikilink")機能を持つ。（例えばで一つ下の内容に移動する）
  - [Vivaldi](https://ja.wikipedia.org/wiki/Vivaldi_\(ウェブブラウザ\) "wikilink")（[Vimium](https://ja.wikipedia.org/wiki/Vimium "wikilink")拡張）
  - [Safari](../Page/Safari.md "wikilink")（Vimari拡張）
  - [W3m](../Page/W3m.md "wikilink") - テキストブラウザ
  - [MuPDF](https://ja.wikipedia.org/wiki/mupdf "wikilink") - PDF閲覧
  - [feh](https://ja.wikipedia.org/wiki/feh "wikilink") - 画像閲覧
  - [bash](https://ja.wikipedia.org/wiki/bash "wikilink")（`set -o vi`でViモード），[zsh](https://ja.wikipedia.org/wiki/zsh "wikilink")，[fish](https://ja.wikipedia.org/wiki/fish "wikilink")等のシェル

## 脚注

### 注釈

### 出典

## 参考文献

  - Steve Oualline『Vi IMproved‐Vim完全バイブル』[高橋則利](https://ja.wikipedia.org/wiki/高橋則利 "wikilink")訳、[技術評論社](https://ja.wikipedia.org/wiki/技術評論社 "wikilink")、2004年5月、ISBN 4-7741-2018-9

## 関連項目

  - [テキストエディタの一覧](https://ja.wikipedia.org/wiki/テキストエディタの一覧 "wikilink")
  - [VimConf](https://ja.wikipedia.org/wiki/VimConf "wikilink")

## 外部リンク

  -
  - [vim-jp](https://vim-jp.org/)（日本語対応 Windows、macOS版Vimの配布）

  - [Vim 日本語ドキュメント](https://vim-jp.org/vimdoc-ja/)

  - [KaoriYa](https://www.kaoriya.net/)（日本語対応 Windows 版 Vim の作者サイト）

[Category:テキストエディタ](https://ja.wikipedia.org/wiki/Category:テキストエディタ "wikilink") [Category:ファイル比較ツール](https://ja.wikipedia.org/wiki/Category:ファイル比較ツール "wikilink") [Category:オープンソースソフトウェア](https://ja.wikipedia.org/wiki/Category:オープンソースソフトウェア "wikilink") [Category:クロスプラットフォームのソフトウェア](https://ja.wikipedia.org/wiki/Category:クロスプラットフォームのソフトウェア "wikilink") [Category:1991年のソフトウェア](https://ja.wikipedia.org/wiki/Category:1991年のソフトウェア "wikilink")

1.  [Vim documentation: intro - pronounce](http://vimdoc.sourceforge.net/htmldoc/intro.html#pronounce)
2.  [Vim日本語ドキュメント intro - pronounce](http://vim-jp.org/vimdoc-ja/intro.html#pronounce)
3.   の意
4.   の意
5.  ヴィムアールシー、Windows版では `_vimrc`
6.  版では `vimfiles`
7.  例: [vim-scripts - GitHub](https://github.com/vim-scripts)
8.
9.   の頭文字から命名
10.
11.
12.
13.
14.
15.
16. [](http://cd.textfiles.com/fredfish/v1.6/FF_Disks/571-600/FF_591/Contents)
17.
18.
19.
20.
21.
22.
23.
24.
25.
26. [](http://groups.google.com/group/vim_announce/browse_thread/thread/2c89671dd928812f)
27.
28.
29. [`:help sys-file-list`](http://vimdoc.sourceforge.net/htmldoc/help.html#sys-file-list)
30.
31.
32.
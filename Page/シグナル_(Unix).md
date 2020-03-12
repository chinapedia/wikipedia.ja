> この記事は[ \(Unix\)](https://ja.wikipedia.org/wiki/_\(Unix\))から翻訳されています。


**シグナル**（）とは、[Unix系](../Page/Unix系.md "wikilink")（[POSIX](../Page/POSIX.md "wikilink")標準に類似の）[OSにおける](../Page/オペレーティングシステム.md "wikilink")、限定的な[プロセス間通信](../Page/プロセス間通信.md "wikilink")の形式を使って、[プロセス](../Page/プロセス.md "wikilink")に対し、非同期で、イベントの発生を伝える機構である。シグナルが送信された際、OSは宛先プロセスの正常な[処理の流れに割り込む](../Page/制御構造.md "wikilink")。どんな[不可分でない処理の間でも割り込むことができる](../Page/不可分操作.md "wikilink")。受信プロセスが以前に**シグナルハンドラ**を登録しておけば、シグナル受信時にそのルーチンが実行される。さもなくば、デフォルトのシグナル処理が行われる。（同様なものは他のTSSなどでも開発されてはいるが、UNIXのシグナルは）1970年ごろ[ベル研究所](../Page/ベル研究所.md "wikilink")で[UNIX](../Page/UNIX.md "wikilink")に実装された。後に[POSIX](../Page/POSIX.md "wikilink")である程度は標準化されているが、標準化が諦められているような振舞などもいくつかあり、特に他の幾つかの要素（fork等）とマルチスレッドとシグナルが絡むと実装毎の対処にプログラミングが大変になることがある。

## シグナル送信

以下のような操作によりシグナルが送信される。

  - ユーザーがあるプロセスの[端末](../Page/端末.md "wikilink")のキーを押下したとき、端末がシグナルを発生する。
      - \+（古いUNIXでは DEL キー）を押下すると、SIGINT を送信し、デフォルトではそのプロセスを終了させる。

      - \+ を押下すると、SIGTSTP を送信し、デフォルトではプロセスの実行を中断（一時停止）させる。

      - \+ を押下すると、SIGQUIT を送信し、デフォルトではプロセスを終了させ[コアダンプ](../Page/コアダンプ.md "wikilink")させる。

      - （なお、これらのキーの組み合わせは  コマンドで変更可能である）
  - `kill(2)` [システムコール](../Page/システムコール.md "wikilink")を使うと、権限があれば指定したプロセス（群）に指定したシグナルを送信できる。同様に [`kill(1)`](https://ja.wikipedia.org/wiki/Kill "wikilink") コマンドでユーザーがプロセス（群）にシグナルを送信することもできる。また、`raise(3)` を使えばカレントプロセス（またはスレッド）に指定したシグナルを送信できる。
  - [ゼロ除算](../Page/ゼロ除算.md "wikilink")（SIGFPE）、[セグメンテーション違反](../Page/セグメンテーション違反.md "wikilink")（SIGSEGV）などの[例外によってもシグナルが発生する](../Page/例外処理.md "wikilink")。経験の浅いプログラマはポインタに不正アドレスを入れてしまい、SIGSEGVを発生させることが多い。これらはデフォルトではプログラムを終了させ、コアダンプを生じる。
  - カーネルはプロセスに何らかのイベントを通知するためにシグナルを発生させることができる。例えば、プロセスが[パイプに書き込んだとき読み込み側プロセスが既にパイプをクローズしている場合にSIGPIPEが送信される](../Page/パイプ_\(コンピュータ\).md "wikilink")。この場合、デフォルトではそのプロセスは終了となるが、パイプをシェルが構築した場合、終了させるのが最も便利である。

## シグナル処理

`signal()`やシステムコールは「シグナルハンドラ」を設定するのに使われる。シグナルハンドラが設定されていないシグナルの場合、デフォルトのハンドラが使われる。さもなくば、シグナルは捉えられ、シグナルハンドラが呼び出される。プロセスはハンドラを設定しなくとも2種類のデフォルト動作を指定できる。シグナルを無視するか（SIG_IGN）、デフォルトのハンドラを使うか（SIG_DFL）である。SIGKILLとSIGSTOPは、捉えることもハンドラで処理することもできないシグナルである。

### 問題

ハンドラによるシグナル処理は[競合状態](../Page/競合状態.md "wikilink")に弱い。シグナルは非同期イベントなので、あるシグナルをハンドラで処理中に別のシグナル（同じ種類ということもある）がそのプロセスに送られてくることがある。このような状態を防ぐため、 を使ってシグナル配送のブロック/アンブロックが可能である。

シグナルは処理中のシステムコールを中断することがあり、アプリケーションは非透過的な再実行をしなければならない。つまり、実行中のシステムコールはEINTRというエラーを返し、要求した処理はシグナル受信によって中断されて結果を得られていないことを示す。そのため、処理を続行するには再度同じシステムコールを実行しなければならない。

シグナルハンドラは通常の処理に割り込んで呼び出されるので、不要な副作用を起こさないように注意が必要である。例えば、大域変数である `errno` を変化させてはならない。シグナルマスクを変化させてはならない。シグナル処理方法を変化させてはならない。その他の[プロセス](../Page/プロセス.md "wikilink")の大域的な属性を変化させてはならない。[`malloc`](https://ja.wikipedia.org/wiki/malloc "wikilink")、[`printf`](https://ja.wikipedia.org/wiki/printf "wikilink")といった非同期シグナル安全(async‐signal‐safe)でない関数を使うのも安全ではない\[1\]。

## ハードウェア例外との関係

[プロセス](../Page/プロセス.md "wikilink")の実行によってハードウェア[例外が発生することがある](../Page/例外処理.md "wikilink")。例えば、プロセスが[ゼロ除算](../Page/ゼロ除算.md "wikilink")を行おうとしたときや、[TLBミスを引き起こしたときなどである](../Page/トランスレーション・ルックアサイド・バッファ.md "wikilink")。[Unix系](../Page/Unix系.md "wikilink")OSでは、ハードウェア例外が発生すると[コンテキストを自動的に切り替えて](../Page/コンテキストスイッチ.md "wikilink")[カーネル](../Page/カーネル.md "wikilink")の[例外ハンドラを実行開始する](../Page/例外処理.md "wikilink")。[ページフォールト](../Page/ページフォールト.md "wikilink")などの一部の例外の場合、カーネルはそのイベントを処理するのに十分な情報を持っているので、プロセスの実行を再開させることができる。しかし他の例外ではカーネルはうまく処理できず、代わりに例外を発生させた処理を行っていたプロセスに例外処理を委任しなければならない。シグナルはこの委任のための機構としても機能し、カーネルからプロセスに対してその例外に対応したシグナルを送信する。例えば、[x86](https://ja.wikipedia.org/wiki/x86 "wikilink") [CPU](../Page/CPU.md "wikilink") でゼロ除算を行おうとした場合 *divide error* 例外が発生し、カーネルがそのプロセスにSIGFPEというシグナルを送信する。同様に、あるプロセスが自身の[仮想アドレス空間の範囲外のメモリアドレスにアクセスしようとした場合](../Page/仮想記憶.md "wikilink")、カーネルはSIGSEGVシグナルを送信する。ハードウェア例外の種類は[CPU](../Page/CPU.md "wikilink")のアーキテクチャによって異なるので、ある例外が発生したときどういうシグナルが送信されるかは厳密にはCPUアーキテクチャやカーネルの実装に依存する。

## 個々のシグナル

[Single UNIX Specification](../Page/Single_UNIX_Specification.md "wikilink") では、以下のシグナルを `<signal.h>` で定義すべきものとして指定している。

DFは、シグナル受信時のデフォルト動作を示しており、以下のような処理がある\[2\]:

  - T: プロセスの異常終了。`exit()` システムコールを実行したのと同様の終了の仕方だが、`wait()`または`waitpid()`でそのプロセスの終了を待ち合わせていたプロセスには、シグナル受信で終了したことを示す異常終了コードが返される。
  - A: プロセスの異常終了。設定されていれば[コアダンプ](../Page/コアダンプ.md "wikilink")を生成する。
  - I: シグナルを無視する。
  - S: プロセスの実行を中断（一時停止）する。
  - C: 中断されていたプロセスの実行を再開する。中断されていないプロセスでは無視する。

下記表のシグナル番号は Linux x86 の場合であり\[3\]、他のOS・他のCPUでは異なる。Linux ARM もシグナル番号は同じ。

<table style="width:145%;">
<colgroup>
<col style="width: 10%" />
<col style="width: 25%" />
<col style="width: 50%" />
<col style="width: 45%" />
<col style="width: 15%" />
</colgroup>
<thead>
<tr class="header">
<th><p>シグナル名</p></th>
<th><p>説明</p></th>
<th><p>DF</p></th>
<th><p>解説</p></th>
<th><p>Linux x86での<br />
シグナル番号[4]</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>SIGABRT</p></td>
<td><p>プロセスが中断された</p></td>
<td><p>A</p></td>
<td><p><code>abort()</code>をプロセス自身が実行することによって発生する。ハンドラによるキャッチ可能。ブロック不可。シグナルハンドラから戻るとプロセスは終了させられる。何らかの不正な状況に陥ったが通常の処理の流れでは終了前のクリーンアップ処理ができないときに使用。</p></td>
<td><p>6</p></td>
</tr>
<tr class="even">
<td><p>SIGALRM</p></td>
<td><p><code>alarm()</code> によるシグナル</p></td>
<td><p>T</p></td>
<td><p><code>alarm()</code>システムコールで、設定した実時間<a href="../Page/タイマー.md" title="wikilink">タイマー</a>がタイムアウトしたことを知らせる。</p></td>
<td><p>14</p></td>
</tr>
<tr class="odd">
<td><p>SIGBUS</p></td>
<td><p>「未定義メモリ領域へのアクセス」(SUS)による<a href="../Page/バスエラー.md" title="wikilink">バスエラー</a></p></td>
<td><p>A</p></td>
<td><p>以下のような不正なメモリ操作により発生。ハンドラでキャッチできるが、ハンドラから戻った後の動作はシステムに依存する（通常プロセスの終了）。</p>
<ul>
<li>アドレス境界不正：CPUはデータのサイズによって配置可能なアドレスに制限があることが多い。例えば32bit整数を4バイト境界（4で割り切れるアドレス）以外に置こうとしたなど。</li>
<li>存在しない物理アドレス：<a href="../Page/ページフォールト.md" title="wikilink">ページフォールト</a>に似ているが物理アドレスに関して発生。</li>
<li>オブジェクト固有エラー：例えば、<a href="https://ja.wikipedia.org/wiki/mmap" title="wikilink">mmap</a>でマッピングされたファイルが切り捨てられたために仮想アドレスに対応する実体が存在しなくなった場合など。</li>
</ul></td>
<td><p>7</p></td>
</tr>
<tr class="even">
<td><p>SIGCHLD</p></td>
<td><p>子プロセスが終了、停止（または再開*）した</p></td>
<td><p>I</p></td>
<td><p><a href="../Page/子プロセス.md" title="wikilink">子プロセス</a>の状態変化に応じて発生。親プロセスは無視することもできる。</p></td>
<td><p>17</p></td>
</tr>
<tr class="odd">
<td><p>SIGCONT</p></td>
<td><p>停止していれば再開</p></td>
<td><p>C</p></td>
<td><p><a href="../Page/プロセスグループ.md" title="wikilink">プロセスグループ</a>を参照。</p></td>
<td><p>18</p></td>
</tr>
<tr class="even">
<td><p>SIGFPE</p></td>
<td><p>浮動小数点例外 -- 「不正な算術操作」(SUS)</p></td>
<td><p>A</p></td>
<td><p><a href="../Page/浮動小数点数.md" title="wikilink">浮動小数点演算で</a><a href="../Page/ゼロ除算.md" title="wikilink">ゼロ除算</a>やオーバーフローなどが発生したときに発生。Signaling <a href="../Page/NaN.md" title="wikilink">NaN</a>が発生したときも同様。また、整数のオーバーフローなどでも発生する。ハンドラでキャッチ可能だが、適切に処理しないとプロセスがハングアップ（無限ループ）に陥る可能性がある。（ここでいう適切な処理とは、シグナルハンドラが受け取る例外発生時のレジスタの内容を書き換えて例外が発生しないようにすることであり、例外発生箇所のコードを解析してどのレジスタが使われていたのかを調べたり、内容を書き換えることで計算結果が不正にならないか判断したりといった非常に高度な対応が必要とされる。また、Signaling NaN 以外では処理続行はほぼ不可能）</p></td>
<td><p>8</p></td>
</tr>
<tr class="odd">
<td><p>SIGHUP</p></td>
<td><p>ハングアップ</p></td>
<td><p>T</p></td>
<td><p>本来は端末の回線が切れたときに発生。現在では<a href="https://ja.wikipedia.org/wiki/擬似端末" title="wikilink">擬似端末</a>をクローズしたときにその端末から起動された<a href="../Page/プロセスグループ.md" title="wikilink">プロセスグループ</a>に送られる。<a href="../Page/シェル.md" title="wikilink">シェル</a>の nohup 機能を使えば<a href="https://ja.wikipedia.org/wiki/バックグラウンド_(ソフトウェア)" title="wikilink">バックグラウンドのプロセスがSIGHUPを受け付けないようにできる</a>。</p></td>
<td><p>1</p></td>
</tr>
<tr class="even">
<td><p>SIGILL</p></td>
<td><p>不正命令</p></td>
<td><p>A</p></td>
<td><p>通常、命令でないメモリ領域にジャンプしたときに発生（<a href="https://ja.wikipedia.org/wiki/コールスタック" title="wikilink">コールスタック</a>のリターンアドレスが破壊されたときなど）。他に特権レベルが高くないと実行できない命令を実行しようとしたときなどにも発生する。</p></td>
<td><p>4</p></td>
</tr>
<tr class="odd">
<td><p>SIGINT</p></td>
<td><p>割り込み</p></td>
<td><p>T</p></td>
<td><p>端末から割り込みキー（通常 CTRL + C）を押下したときに発生。</p></td>
<td><p>2</p></td>
</tr>
<tr class="even">
<td><p>SIGKILL</p></td>
<td><p>強制終了(kill)</p></td>
<td><p>T</p></td>
<td><p>killコマンドなどで明示的に発生させる。キャッチしたり無視したりできない。<a href="https://ja.wikipedia.org/wiki/ゾンビプロセス" title="wikilink">ゾンビプロセス</a>は既に終了しているのでSIGKILLを受けても消滅しない。スリープ中プロセスはスリープ解除されたときにSIGKILLを受け付ける。<a href="https://ja.wikipedia.org/wiki/init" title="wikilink">init</a>はSIGKILLを無視できる。</p></td>
<td><p>9</p></td>
</tr>
<tr class="odd">
<td><p>SIGPIPE</p></td>
<td><p>読み手のいないパイプへの書き込み</p></td>
<td><p>T</p></td>
<td></td>
<td><p>13</p></td>
</tr>
<tr class="even">
<td><p>SIGPOLL*, SIGIO</p></td>
<td><p>poll可能イベント</p></td>
<td><p>T</p></td>
<td><p><a href="../Page/ファイル記述子.md" title="wikilink">ファイル記述子</a>に対して<code>fcntl()</code>システムコールでシグナル発生を指示すると、ポール可能イベントに伴ってSIGPOLLが発生する。一般に通信ポートに対応するファイル識別子に使用し、完全な非同期I/Oを実現する。ただし、コードが複雑化することから、最近では専用の非同期I/Oシステムコールを使用することが推奨されている。</p></td>
<td><p>29</p></td>
</tr>
<tr class="odd">
<td><p>SIGPROF*</p></td>
<td><p>プロファイリングタイマーがタイムアウト</p></td>
<td><p>T</p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/プロファイラ" title="wikilink">プロファイラ</a>で使用。このときのタイマーはプロセスの全実行時間に対応する（<a href="../Page/CPUモード.md" title="wikilink">CPUモード</a>に関わらず計時する）。</p></td>
<td><p>27</p></td>
</tr>
<tr class="even">
<td><p>SIGPWR</p></td>
<td><p>電源喪失</p></td>
<td><p>T</p></td>
<td></td>
<td><p>30</p></td>
</tr>
<tr class="odd">
<td><p>SIGQUIT</p></td>
<td><p>終了とコアダンプ</p></td>
<td><p>A</p></td>
<td><p>通常、端末からの終了キー（CTRL + \）で発生。</p></td>
<td><p>3</p></td>
</tr>
<tr class="even">
<td><p>SIGSEGV</p></td>
<td><p><a href="../Page/セグメンテーション違反.md" title="wikilink">セグメンテーション違反</a></p></td>
<td><p>A</p></td>
<td><p><a href="../Page/ページフォールト.md" title="wikilink">ページフォールト</a>のうち不正なメモリアクセスによるものの場合に発生。しかし、例えばヒープ領域の拡張をSIGSEGV発生を受けてオンデマンドで行うライブラリなどもある。</p></td>
<td><p>11</p></td>
</tr>
<tr class="odd">
<td><p>SIGSTKFLT</p></td>
<td><p>数値演算プロセッサにおけるスタックフォルト</p></td>
<td><p>A</p></td>
<td></td>
<td><p>16</p></td>
</tr>
<tr class="even">
<td><p>SIGSTOP</p></td>
<td><p>実行中断</p></td>
<td><p>S</p></td>
<td><p><a href="../Page/プロセスグループ.md" title="wikilink">プロセスグループ</a>の実行中断のためのシグナル。キャッチも無視もできない。SIGCONT シグナルで実行再開する。</p></td>
<td><p>19</p></td>
</tr>
<tr class="odd">
<td><p>SIGSYS*, SIGUNUSED</p></td>
<td><p>不正 <a href="../Page/システムコール.md" title="wikilink">システムコール</a></p></td>
<td><p>A</p></td>
<td><p>一般にシステムコールの番号や引数が不正だったときは単にエラーを返すことで済むので、このシグナルは滅多に使われない。</p></td>
<td><p>31</p></td>
</tr>
<tr class="even">
<td><p>SIGTERM</p></td>
<td><p>強制終了</p></td>
<td><p>T</p></td>
<td><p>killコマンドがデフォルトで発生するシグナル。しかし、このシグナルをキャッチしたり無視したりすることも可能。</p></td>
<td><p>15</p></td>
</tr>
<tr class="odd">
<td><p>SIGTRAP*</p></td>
<td><p>トレース/<a href="https://ja.wikipedia.org/wiki/ブレークポイント" title="wikilink">ブレークポイント</a>による</p></td>
<td><p>A</p></td>
<td><p>何らかのデバッグ機能で使用される（アーキテクチャによって異なる）。</p></td>
<td><p>5</p></td>
</tr>
<tr class="even">
<td><p>SIGTSTP</p></td>
<td><p>端末からの中断シグナル</p></td>
<td><p>S</p></td>
<td><p>フォアグラウンドの<a href="../Page/プロセスグループ.md" title="wikilink">プロセスグループ</a>を実行中断させる（通常、CTRL + Z 押下）。</p></td>
<td><p>20</p></td>
</tr>
<tr class="odd">
<td><p>SIGTTIN</p></td>
<td><p>バックグラウンドプロセスが端末から読もうとした</p></td>
<td><p>S</p></td>
<td><p>バックグラウンドのプロセスグループがユーザー入力待ちとなって停止。シェルの機能を使ってフォアグラウンドにすることで入力が可能。</p></td>
<td><p>21</p></td>
</tr>
<tr class="even">
<td><p>SIGTTOU</p></td>
<td><p>バックグラウンドプロセスが端末に書き込もうとした</p></td>
<td><p>S</p></td>
<td><p>バックグラウンドのプロセスグループが端末への表示待ちとなって停止。シェルの機能を使ってフォアグラウンドにすることで表示可能。</p></td>
<td><p>22</p></td>
</tr>
<tr class="odd">
<td><p>SIGURG</p></td>
<td><p>ソケット上に緊急データがある</p></td>
<td><p>I</p></td>
<td><p>非同期I/O機能で使用。</p></td>
<td><p>23</p></td>
</tr>
<tr class="even">
<td><p>SIGUSR1</p></td>
<td><p>ユーザー定義シグナル 1</p></td>
<td><p>T</p></td>
<td><p>POSIXでは未定義。<a href="../Page/Linux.md" title="wikilink">Linux</a>ではスレッド間同期に使用。<a href="https://ja.wikipedia.org/wiki/dd_(UNIX)" title="wikilink">ddコマンドが受信すると操作の状況が表示される</a>。</p></td>
<td><p>10</p></td>
</tr>
<tr class="odd">
<td><p>SIGUSR2</p></td>
<td><p>ユーザー定義シグナル 2</p></td>
<td><p>T</p></td>
<td><p>POSIXでは未定義。Linuxではスレッド間同期に使用。</p></td>
<td><p>12</p></td>
</tr>
<tr class="even">
<td><p>SIGVTALRM*</p></td>
<td><p>仮想時間をカウントするタイマによるシグナル -- 「仮想タイマのタイムアウト」(SUS)</p></td>
<td><p>T</p></td>
<td><p>プロファイラなどで使用。このときのタイマーはプロセスの<a href="https://ja.wikipedia.org/wiki/ユーザーモード" title="wikilink">ユーザーモード</a>での実行時間を計時するもの。SIGPROFと組み合わせると、プロセスの<a href="https://ja.wikipedia.org/wiki/カーネルモード" title="wikilink">カーネルモード</a>での実行時間がわかる。</p></td>
<td><p>26</p></td>
</tr>
<tr class="odd">
<td><p>SIGWINCH</p></td>
<td><p>ウィンドウ リサイズ シグナル</p></td>
<td><p>I</p></td>
<td></td>
<td><p>28</p></td>
</tr>
<tr class="even">
<td><p>SIGXCPU*</p></td>
<td><p>CPU時間制限を越えた</p></td>
<td><p>A</p></td>
<td><p>プロセス実行時間（スリープしていた時間やスケジューリング待ち時間は除く）がある値を超えると発生。</p></td>
<td><p>24</p></td>
</tr>
<tr class="odd">
<td><p>SIGXFSZ*</p></td>
<td><p>ファイルサイズ制限を越えた</p></td>
<td><p>A</p></td>
<td><p>ファイルサイズが<a href="../Page/ファイルシステム.md" title="wikilink">ファイルシステム</a>（あるいは<a href="../Page/オペレーティングシステム.md" title="wikilink">オペレーティングシステム</a>）の制限を越えようとしたとき、それを引き起こしたプロセスに送信される。</p></td>
<td><p>25</p></td>
</tr>
</tbody>
</table>

注：アスタリスク付の項目は、[X/Open](https://ja.wikipedia.org/wiki/X/Open "wikilink") System Interfaces (XSI) による拡張を示す。(SUS)とある部分はSUS\[5\]にある表現の引用（を和訳したもの）。

上述以外に、プロセスは擬似シグナル（番号0）を送信することもできる。これは実際にはシグナルを送信せずにシグナル送信時のエラーチェックをし、例えば宛先プロセスが存在するかどうかをチェックするのに便利である。

## 脚注

## 関連項目

  - [標準Cライブラリ](../Page/標準Cライブラリ.md "wikilink")

## 外部リンク

  -
  - [システムプログラム(第5週)](http://www.coins.tsukuba.ac.jp/~syspro/2005/No5.html) 筑波大学講義

  - [Introduction to Unix Signals Programming](http://users.actcom.co.il/~choo/lupg/tutorials/signals/signals-programming.html)

  - [Another Introduction to Unix Signals Programming](http://www.linuxprogrammingblog.com/all-about-linux-signals)

  - [UNIX and Reliable POSIX Signals](http://www.enderunix.org/docs/signals.pdf) by Baris Simsek

  - [Signal Handlers](http://www.openbsd.org/papers/opencon04/index.html) by Henning Brauer

[Category:プロセス間通信](https://ja.wikipedia.org/wiki/Category:プロセス間通信 "wikilink") [Category:OSのプロセス管理](https://ja.wikipedia.org/wiki/Category:OSのプロセス管理 "wikilink") [Category:制御構造](https://ja.wikipedia.org/wiki/Category:制御構造 "wikilink")

1.
2.
3.
4.
5.
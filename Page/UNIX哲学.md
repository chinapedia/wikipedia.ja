> この記事は[UNIX哲学](https://ja.wikipedia.org/wiki/UNIX哲学)から翻訳されています。


**UNIX哲学**とは、[ソフトウェア](../Page/ソフトウェア.md "wikilink")開発に関する文化的な規範と哲学的アプローチのまとまりであり、[UNIX](../Page/UNIX.md "wikilink") [OSの開発者たちの](../Page/オペレーティングシステム.md "wikilink")[経験](../Page/経験.md "wikilink")に基づくものとされている。 その内容は、発言者によって異なるが、以下の点に留意が必要である。

  - いずれもUNIXが開発された1971年から10年以上が経過してからなされた発言である
  - 発言者には、UNIX開発との関わり合いが希薄な人物も含まれている
  - UNIXを生み出したケン・トンプソンやデニス・リッチーは"simplicity"や"easy to use"といった標準的な用語しか用いておらず、"哲学"(philosophy)という表現をしていない
  - 商用UNIXには大規模で多機能なアプリケーションソフトウエアーが含まれている場合がある

すなわち、"UNIX哲学"が、一貫したものとして当初から存在し続けているわけではなく、UNIXに関わる全ての人に共通認識として受け入れられているわけでもなく、UNIXの置かれている現在や過去の状況を必ずしも的確に表現し得ているわけでもない。また、そこで表現されている手法の妥当性や有効性が、普遍的に立証されているわけでもない。

ある意味では、"UNIX哲学"とは、UNIXに関心を示す人々のうちの一部が抱く、希望や願望あるいは理想を表明したものにすぎない。

## マキルロイ: UNIXの四半世紀

[パイプの発明者でありUNIX創始者の一人でもある](../Page/パイプ_\(コンピュータ\).md "wikilink")[マキルロイは](https://ja.wikipedia.org/wiki/ダグラス・マキルロイ "wikilink")、この哲学を以下のように要約した。

この哲学はしばしば、「一つのことを、うまくやれ」とさらに厳格に要約される。

3つの教義のうち第3のものだけがUNIX特有であるが、UNIXの開発者はしばしば3つの教義すべてを他の開発者よりも重要視する。

## パイク: Cプログラミングに関する覚え書き

（注意: これは直接にはUNIX哲学ではない。強い結びつきのあるC言語についての記述ではあるが。現在英語版のこの記事には、この節に対応する節はない）

[ロブ・パイク](../Page/ロブ・パイク.md "wikilink")は *Notes on Programming in C* \[1\]の中で、以下のようなルールをプログラミングの格言として提案している。これはまたUNIX哲学のポイントとも共通点がある。

  - ルール1: プログラムがどこで時間を消費することになるか知ることはできない。ボトルネックは驚くべき箇所で起こるものである。したがって、どこがボトルネックなのかをはっきりさせるまでは、推測を行ったり、スピードハックをしてはならない。Rule 1. You can't tell where a program is going to spend its time. Bottlenecks occur in surprising places, so don't try to second guess and put in a speed hack until you've proven that's where the bottleneck is.
  - ルール2: 計測すべし。計測するまでは速度のための調整をしてはならない。コードの一部が残りを圧倒しないのであれば、なおさらである。Rule 2. Measure. Don't tune for speed until you've measured, and even then don't unless one part of the code overwhelms the rest.
  - ルール3: 凝った(Fancy)[アルゴリズム](../Page/アルゴリズム.md "wikilink")は\(n\)が小さいときには遅く、\(n\)はしばしば小さい。凝ったアルゴリズムは大きな定数を持っている\[2\]。\(n\)が頻繁に大きくなることがわかっていないなら、凝ってはいけない（\(n\)が大きくなるときでさえ、ルール2が最初に適用される）。Rule 3. Fancy algorithms are slow when n is small, and n is usually small. Fancy algorithms have big constants. Until you know that n is frequently going to be big, don't get fancy. (Even if n does get big, use Rule 2 first.) For example, binary trees are always faster than splay trees for workaday problems.
  - ルール4: 凝ったアルゴリズムはシンプルなそれよりバグを含みやすく、実装するのも難しい。シンプルなアルゴリズムとシンプルな[データ構造](../Page/データ構造.md "wikilink")を使うべし。Rule 4. Fancy algorithms are buggier than simple ones, and they're much harder to implement. Use simple algorithms as well as simple data structures.
  - ルール5: データはすべてを決定づける。もし、正しいデータ構造を選び、ものごとをうまく構成すれば、アルゴリズムはほとんどいつも自明のものになるだろう。プログラミングの中心は、アルゴリズムではなくデータ構造にある。Rule 5. Data dominates. If you've chosen the right data structures and organized things well, the algorithms will almost always be self­evident. Data structures, not algorithms, are central to programming.
  - ルール6: ルール6は存在しない。Rule 6. There is no Rule 6.

パイクのルール1と2は、[ドナルド・クヌース](../Page/ドナルド・クヌース.md "wikilink")が述べた格言「早すぎる最適化は諸悪の根源である」を言い換えたものである（[最適化 (情報工学)\#最適化する時期も参照](https://ja.wikipedia.org/wiki/最適化_\(情報工学\)#最適化する時期 "wikilink")）。[ケン・トンプソン](../Page/ケン・トンプソン.md "wikilink")はパイクのルール3と4を「疑いがあるときは[総当たり](../Page/力まかせ探索.md "wikilink")（brute force）を使え」と言い換えている。ルール3と4はデザイン哲学[KISSの例である](https://ja.wikipedia.org/wiki/KISS原則 "wikilink")。ルール5は[フレッド・ブルックスが以前に](../Page/フレデリック・ブルックス.md "wikilink")「[人月の神話](../Page/人月の神話.md "wikilink")」の中で述べている。ジョン・ベントレーの *[Programming Pearls](https://ja.wikipedia.org/wiki/:en:Programming_Pearls "wikilink")* は同じデザイン原則について述べた章を含んでいる。ルール5はしばしば「スマートなデータを使うつまらないコードを書け」と短縮され、また「データ構造が十分に良いものなら、それを扱うアルゴリズムは平凡であるべきだ」というガイドラインの実例でもある。ルール6は[モンティ・パイソン](../Page/モンティ・パイソン.md "wikilink")の「ブルース・スケッチ」を愉快に参照しているだけのものだ。Cの文字列では最後の1バイトが[ヌル文字](https://ja.wikipedia.org/wiki/ヌル文字 "wikilink")であり、したがってその文字列の長さを示すことになる。

## ガンカーズ: UNIXの哲学

1994年、マイク・ガンカーズ（[X Window System開発チームの一員](../Page/X_Window_System.md "wikilink")）は、UNIXで得た経験と、同僚プログラマーやUNIXに依存する他分野の人々との議論を活かし、以下の9つの至上命令に集約される「UNIX哲学」を創出した。

1.  小さいものは美しい。
2.  各プログラムが一つのことをうまくやるようにせよ。
3.  できる限り早く原型（プロトタイプ）を作れ。
4.  効率よりも移植しやすさを選べ。
5.  単純な[テキストファイル](../Page/テキストファイル.md "wikilink")にデータを格納せよ。
6.  ソフトウェアを梃子(てこ)として利用せよ。
7.  効率と移植性を高めるために[シェルスクリプト](../Page/シェルスクリプト.md "wikilink")を利用せよ。
8.  拘束的なユーザーインターフェースは作るな。
9.  全てのプログラムはフィルタとして振る舞うようにせよ。

<!-- end list -->

1.  *Small is beautiful.*
2.  *Make each program do one thing well.*
3.  *Build a prototype as soon as possible.*
4.  *Choose portability over efficiency.*
5.  *Store data in flat text files.*
6.  *Use software leverage to your advantage.*
7.  *Use shell scripts to increase leverage and portability.*
8.  *Avoid captive user interfaces.*
9.  *Make every program a Filter.*

以下の重要性が相対的に低い教義は、UNIX哲学の一部として普遍的に合意されるものではなく、場合によっては現在も激しく議論されているものである（例えば[モノリシックカーネルと](https://ja.wikipedia.org/wiki/カーネル#モノリシックカーネル "wikilink")[マイクロカーネルのように](https://ja.wikipedia.org/wiki/カーネル#マイクロカーネル "wikilink")）。

1.  ユーザが環境を設定できるようにせよ。
2.  OSのカーネルは小さく軽量にせよ。
3.  小文字の短い名前を使え。
4.  森林を守れ。
5.  沈黙は金なり。
6.  並行性を考えよ。
7.  部分の集積は全体よりも大きい。
8.  [90パーセントの解決を模索せよ](../Page/パレートの法則.md "wikilink")。
9.  より悪いことは、より良いことだ。
10. 階層的に考えよ。

## より悪いことは、より良いことだ（Worse is better）

リチャード・P・ガブリエルは、UNIXの重要な優位性のひとつは彼が「より悪いことは、より良いことだ」（"Worse is better"）という用語に込めるデザイン哲学を体現しているところにあると述べている。「より悪いことは、より良いことだ」式のデザイン・スタイルでは、インターフェースと実装の**両面が**シンプルであることが、システムにおける他のいかなる特性よりも重視される――正確さ、堅牢さ、完全さよりも、である。ガブリエルは、このデザイン・スタイルが発展のための重要な利点を持っていると論じているが、一方でいくつかの結果の質について疑問を抱いてもいる。

例えば、黎明期のUNIXにおいて、プロセスはカーネル・システムコールをすべてユーザスタック上で実行した。もしカーネル内で長期間のI/Oやsleepによってプロセスがブロックしているときに（例えば`sleep(10*60)`のように）、そのプロセスにシグナルが通知されたら、何が行われるのだろうか？　シグナルはI/Oが完了するまでの間（どれくらいかわからないが、おそらく長い間）遅延されるのか？　プロセスがカーネルモードで動いている場合、シグナル・ハンドラは実行され得ず、スタックには繊細なカーネル・データが残ったままである。カーネルはシステムコールを棄却（バックアウト）し、応答と再始動に備えて保管し、成功裏にシグナルハンドラを完了することを引き受けるべきなのか？

このようなケースでは、[ケン・トンプソン](../Page/ケン・トンプソン.md "wikilink")と[デニス・リッチー](../Page/デニス・リッチー.md "wikilink")は完全性よりもシンプルさを好む。UNIXシステムは機会ごとにシステムコールから素早く復帰し、何もしなかったことを知らせるエラー通知（「*Interrupted System Call* システムコールに割り込みが発生」）を行う。すなわちエラー番号4（EINTR）である。もちろん、このような呼び出しはシグナルハンドラを呼び出すために中断されている。こうしたことは、長期間実行されうる一群のシステムコール（つまり`read()`、`write()`、`open()`、`select()`等）において起こり得る。利点としては、この仕組みはI/Oシステムを何倍もデザインしやすく、理解しやすいものにしている。圧倒的多数のプログラムは影響を受けない。なぜならこうしたプログラムはSIGINT/^C以外のシグナルを扱わず、経験もしないし、SIGINTが発せられたときには正確に終了（die）するからである。それ以外の少数のプログラム（ジョブ制御のキー入力を受け付けるシェルやテキストエディタのようなもの）のためには、システムコールの小さなラッパー（wrapper）を追加することができ、EINTRエラーが起こったらすぐにシステムコールを再試行できるのである。問題はシンプルな方法で解決される。

（現在のUnixクローンでは、カーネルコードがユーザスタックで実行されたりしないし、I/O中のシグナルについて、このようなふるまいであったのは、初期のUNIXやSystemV（あるいは初期のLinux）においてのことである。4.3以降のBSDや現在のLinuxでは、全くI/Oが進行していない状態でシグナルが入った場合、シグナルの処理が終わった後、中断されたI/Oが再開される）

## レイモンド: UNIXプログラミングの技法

[エリック・S・レイモンドは著書](../Page/エリック・レイモンド.md "wikilink")『The Art of UNIX Programming』\[3\]の中で、UNIX哲学を "Keep it Simple, Stupid" （[KISS原則](https://ja.wikipedia.org/wiki/KISS原則 "wikilink")、「シンプルでつまらないものに保て」）という、広く使われている工学哲学として要約した。そしてレイモンドは、彼がいかにこの総体的な哲学がUNIXの文化的規範として適用されていると信じているか述べている。だが以下のルールに深刻に違反した例が実際のUNIXの実践において簡単に発見できるのも驚くべきことではない。

  - [モジュール](../Page/モジュール.md "wikilink")性のルール
    クリーンなインターフェースで接続されるシンプルなパーツを書け。
  - 明瞭さのルール
    明瞭さは独創性よりも良い。
  - 合成のルール
    他のプログラムと接続できるようプログラムをデザインせよ。
  - 分割のルール
    ポリシーをメカニズムから分離せよ。インターフェースをエンジンから分離せよ。
  - シンプルさのルール
    シンプルさを求めてデザインせよ。複雑にしなければならない場合に限り、複雑さを加えよ。
  - 倹約のルール
    他に方法がないことが実験により明らかである場合に限り、大きいプログラムを書け。
  - 透明性のルール
    透明性を求めてデザインせよ。調査とデバッグが簡単になる。
  - 頑丈さのルール
    頑丈さは透明性とシンプルさから生まれる。
  - 代表のルール
    知識をデータに織り込め。するとプログラムのロジックをつまらなくて頑丈なものにできる。
  - [最小限の驚きのルール](../Page/驚き最小の原則.md "wikilink")
    インターフェースデザインにおいては、常に驚きが最小限であるようにせよ。
  - 沈黙のルール
    余計な出力をすべきではない。他の開発者にとってただ邪魔なだけである。
  - 修復のルール
    失敗しなければならないときは、騒がしく、かつできるだけ早く失敗せよ。
  - 経済のルール
    プログラマの時間は貴重である。プログラマの時間をコンピュータの時間より優先して節約せよ。
  - 生成のルール
    hand-hacking\[4\]は避けよ。プログラムを書けるときに、プログラムを書くためにプログラムを書け。
  - [最適化のルール](../Page/最適化_\(情報工学\).md "wikilink")
    洗練させる前に原型（[プロトタイプ](../Page/プロトタイプ.md "wikilink")）を作れ。最適化する前に原型が動くようにせよ。
  - 多様性のルール
    あらゆる「ただ一つの本当の方法」という主張は信じるな。
  - 拡張性のルール
    未来に向けてデザインせよ。未来は思ったよりもすぐにやってくる。

<!-- end list -->

  - Rule of Modularity: Developers should build a program out of simple parts connected by well defined interfaces, so problems are local, and parts of the program can be replaced in future versions to support new features. This rule aims to save time on debugging code that is complex, long, and unreadable.
    Rule of Clarity: Developers should write programs as if the most important communication is to the developer, including him- or herself, who will read and maintain the program rather than the computer. This rule aims to make code readable and comprehensible for whomever works on the code in future.
    Rule of Composition: Developers should write programs that can communicate easily with other programs. This rule aims to allow developers to break down projects into small, simple programs rather than overly complex monolithic programs.
    Rule of Separation: Developers should separate the mechanisms of the programs from the policies of the programs; one method is to divide a program into a front-end interface and back-end engine that interface communicates with. This rule aims to let policies be changed without destabilizing mechanisms and consequently reducing the number of bugs.
    Rule of Simplicity: Developers should design for simplicity by looking for ways to break up program systems into small, straightforward cooperating pieces. This rule aims to discourage developers’ affection for writing “intricate and beautiful complexities” that are in reality bug prone programs.
    Rule of Parsimony: Developers should avoid writing big programs. This rule aims to prevent overinvestment of development time in failed or suboptimal approaches caused by the owners of the program’s reluctance to throw away visibly large pieces of work. Smaller programs are not only easier to optimize and maintain; they are easier to delete when deprecated.
    Rule of Transparency: Developers should design for visibility and discoverability by writing in a way that their thought process can lucidly be seen by future developers working on the project and using input and output formats that make it easy to identify valid input and correct output. This rule aims to reduce debugging time and extend the lifespan of programs.
    Rule of Robustness: Developers should design robust programs by designing for transparency and discoverability, because code that is easy to understand is easier to stress test for unexpected conditions that may not be foreseeable in complex programs. This rule aims to help developers build robust, reliable products.
    Rule of Representation: Developers should choose to make data more complicated rather than the procedural logic of the program when faced with the choice, because it is easier for humans to understand complex data compared with complex logic. This rule aims to make programs more readable for any developer working on the project, which allows the program to be maintained.\[6\]
    Rule of Least Surprise: Developers should design programs that build on top of the potential users' expected knowledge; for example, ‘+’ should always mean addition in a calculator program. This rule aims to encourage developers to build intuitive products that are easy to use.
    Rule of Silence: Developers should design programs so that they do not print unnecessary output. This rule aims to allows other programs and developers to pick out the information they need from a program's output without having to parse verbosity.
    Rule of Repair: Developers should design programs that fail in a manner that is easy to localize and diagnose or in other words “fail noisily”. This rule aims to prevent incorrect output from a program from becoming an input and corrupting the output of other code undetected.
    Rule of Economy: Developers should value developer time over machine time, because machine cycles as of the year 2013 are relatively inexpensive compared to prices in the 1970s. This rule aims to reduce development costs of projects.
    Rule of Generation: Developers should avoid writing code by hand and instead write abstract high-level programs that generate code. This rule aims to reduce humans errors and save time.
    Rule of Optimization: Developers should prototype software before polishing it. This rule aims to prevent developers from spending too much time for marginal gains.
    Rule of Diversity: Developers should design their programs to be flexible and open. This rule aims to make programs flexible, allowing them to be used in other ways than their developers intended.
    Rule of Extensibility: Developers should design for the future by making their protocols extensible, allowing for easy plugins without modification to the program's architecture by other developers, noting the version of the program, and more. This rule aims to extend the lifespan and enhance the utility of the code the developer writes.

これら規範の多くはUNIXコミュニティの外で受け入れられている――最初にUNIXが採用したときはそうでなかったとしても、後にそうなった。また、多くはUNIXコミュニティ独特のものではなく、UNIXコミュニティから生じたわけでもない。にもかかわらず、熟練のUNIXプログラマーはこれらの考え方を組み合わせたものをUNIXスタイルの基礎として受け入れる傾向がある。

## 論争

[GNUプロジェクト](../Page/GNUプロジェクト.md "wikilink")による標準的なUNIXプログラムの代替（diffやfind等）が「Unix哲学」に従うものであるのか、あるいはそれを誤解しているのかは議論の分かれるところである。おそらく、UNIXに古くから関わる人々のうちの少なくともいくらかは後者を主張するであろう。なぜならGNUプロジェクトのツール群はしばしばUNIXと同等のものよりも十分に大きく、また機能も豊富だからである（[GNU](../Page/GNU.md "wikilink")はコーディング標準において、いくつかの点でUNIXと同じにしないことを薦めている）。

GNU以前に1983年にはすでにロブ・パイクによる、Unixの基本的なツールにおいてBSDによって拡張された機能のうちのいくつか（代表例として挙げられたのは、cat に制御コードを文字に変換して可視化させる -v ）の仕様が、Unix的でないとした批判がある\[5\]。確かにUnix哲学に従えば、cat -v の機能は独立したフィルタで果たされるべきであり、本来は「連結」コマンドである cat が単にストリームを読んで書くだけの目的に流用されることが多いとはいえ、それに加えてあれこれと機能を持つべきではない。

しかし、同様にして批判された別の例である、ls コマンドが出力を表示される幅に合わせて整形する機能などは十分に便利ではあり、Unix哲学に従って column コマンドをパイプで繋げるのはどう考えても煩わしい 。そういったわけで、現代では議論されることはあまり見られなくなったものの、普段Linux等を使っている際に当然とされていることが本当に当然なのか、考えさせられる論点がある。

## 引用

  - 「UNIXはシンプルである。必要なのはそのシンプルさを理解する素質だけである。」 - [デニス・リッチー](../Page/デニス・リッチー.md "wikilink")
  - 「UNIXはユーザが愚かなことをするのを止めるために作られたのではない。小器用なことをするのも防いでくれるのだ。」 - ダグ・グウィン
  - 「UNIXはユーザフレンドリーだ。誰彼構わずフレンドリーになるわけではない だけだ。」- スティーブン・キング
  - 「UNIXを理解しない人々は、それを不十分に再発明することになるだろう」 - ヘンリー・スペンサー

## 関連項目

  - [Plan 9 from Bell Labs](../Page/Plan_9_from_Bell_Labs.md "wikilink")
  - [パイプ (コンピュータ)](../Page/パイプ_\(コンピュータ\).md "wikilink")
  - [:en:The Elements of Style](https://ja.wikipedia.org/wiki/:en:The_Elements_of_Style "wikilink") – UNIX哲学の着想の源の一つ。
  - [:en:The UNIX-HATERS Handbook](https://ja.wikipedia.org/wiki/:en:The_UNIX-HATERS_Handbook "wikilink")
  - [ソフトウェア工学](../Page/ソフトウェア工学.md "wikilink")
  - [POSIX中心主義](https://ja.wikipedia.org/wiki/POSIX中心主義 "wikilink")

## 参照

  - *[The Unix Programming Environment](http://cm.bell-labs.com/cm/cs/upe/)* by [Brian Kernighan](../Page/ブライアン・カーニハン.md "wikilink") and [Rob Pike](../Page/ロブ・パイク.md "wikilink"), 1984
  - [*Notes on Programming in C*](http://www.lysator.liu.se/c/pikestyle.html), Rob Pike, September 21, 1989
  - *UNIXの1/4世紀*, Peter H. Salus, Addison-Wesley, May 31, 1994 (ISBN 0-201-54777-5、ISBN 4756136591)
  - [*Philosophy*](http://www.faqs.org/docs/artu/philosophychapter.html) — from [*The Art of Unix Programming*](http://www.catb.org/~esr/writings/taoup), Eric S. Raymond, Addison-Wesley, September 17, 2003 (ISBN 0-13-142901-9、ISBN 4756149480)
  - [Final Report of the Multics Kernel Design Project](http://citeseer.ist.psu.edu/schroeder77final.html) by M. D. Schroeder, D. D. Clark, J. H. Saltzer, and D. H. Wells, 1977.
  - *UNIXという考え方―その設計思想と哲学*, Mike Gancarz, ISBN 4274064069

## 脚註

## 外部リンク

  - [The Unix Philosophy: A Brief Introduction](http://www.linfo.org/unix_philosophy.html) - by The Linux Information Project (LINFO)
  - [Joel on Software - Biculturalism](http://www.joelonsoftware.com/articles/Biculturalism.html)

[Category:UNIX](https://ja.wikipedia.org/wiki/Category:UNIX "wikilink") [Category:ソフトウェア開発哲学](https://ja.wikipedia.org/wiki/Category:ソフトウェア開発哲学 "wikilink") [Category:コンピュータの文化](https://ja.wikipedia.org/wiki/Category:コンピュータの文化 "wikilink")

1.
2.  訳註：凝ったアルゴリズムは、それ自身がすでに大きなコストであるということ。
3.  Addison-Wesley刊 ISBN 978-0-13-142901-7、アスキー刊日本語版 ISBN 978-4-7561-4948-0
4.  <http://www.catb.org/jargon/html/H/hand-hacking.html>
5.  <http://harmful.cat-v.org/cat-v/>
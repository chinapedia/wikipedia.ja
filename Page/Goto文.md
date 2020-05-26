> この記事は[Goto文](https://ja.wikipedia.org/wiki/Goto文)から翻訳されています。


[プログラミング言語](../Page/プログラミング言語.md "wikilink")における**goto文**（ゴートゥぶん、）とは、手続き列中の指定された場所（専ら[ラベルで指定される](https://ja.wikipedia.org/wiki/ラベル_\(プログラミング\) "wikilink")）に無条件にジャンプ（移動）する、という[制御構造](../Page/制御構造.md "wikilink")のひとつである「[文 (プログラミング)](https://ja.wikipedia.org/wiki/文_\(プログラミング\) "wikilink") 」である。古い文献などで "go to" と離していることもあるのは、英語の go to どこそこ、といったような言い回しとの類似のためでもあり、FORTRANではプログラム中の空白は基本的に無視されるので、`goto` でも `go to` でも同じだったからという理由もある（BASICにも、どちらも使えるようにしているものもある）。

## 概要

goto文は、それ単体では働きを持たせることはできず、必ず[ラベルか何かによって飛び先が必要である](https://ja.wikipedia.org/wiki/ラベル_\(プログラミング\) "wikilink")。飛び先のほうにcome fromという文を置き、飛ぶ元にラベルを置く、という「[comefrom文](https://ja.wikipedia.org/wiki/comefrom文 "wikilink")」という（冗談半分\[1\]ではあるが）提案もある（提案自体はジョークだが、同等の機能がある言語は実際にいくつかあり、プログラムの理論上の研究対象にもなっている）。[機械語](../Page/機械語.md "wikilink")における[分岐命令](../Page/分岐命令.md "wikilink")の一種である無条件分岐と、アセンブリ言語のラベルをそのまま[手続き型プログラミング](../Page/手続き型プログラミング.md "wikilink")に持ち込んだものと言え、何らかの条件分岐との組み合わせによって、ループであるとか、コードブロックの飛び越しであるとかいったような機能の一部となることができる。

「以前に実行した場所に戻る」というループ用途なのか、それともこの先にあるコードは別の流れの一部なので「単に飛び越したいだけ」というジャンプ用途なのか、という単純なことすら、goto文ではその見かけからは分からない。[if文](https://ja.wikipedia.org/wiki/if文 "wikilink")や[while文](https://ja.wikipedia.org/wiki/while文 "wikilink")と比較して考えれば、そういった「意図の不明瞭さ」は明白であり、後述のように、if文やwhile文で単純に書けることであれば、gotoは使うべきではない。一方で、深く多重にネストしたループからの脱出など（そもそも、そのようなループ自体に問題があることもあるとは言え）、gotoを使ったほうが単純かつ明確に書ける場合もあり、特にC言語においてはgotoを教条的・無条件に排除するべきではない。

資源の確保と解放などのために、プログラム片の入口と出口が必ず対応している必要がある、といった場合などは、gotoに限らず、いわゆる「途中[return](https://ja.wikipedia.org/wiki/return文 "wikilink")」等の他の多くの技法も制限されるので、以下のgoto文の議論とはきちんと区別すべきであるし、またそういった場合の制限を全てのコーディングに適用するべきではない。

## 構文

次のように、**ラベルの付いた文**と併用する。

``` c
clear:
    x = 0;
……
goto clear;
```

goto文によって、そこからclearラベルの付いた文にジャンプし、そこから処理を続ける。

## 批判

[Cなどの](../Page/C言語.md "wikilink")[構造化プログラミング](../Page/構造化プログラミング.md "wikilink")言語においては、goto文はむやみに使ってはいけないというルールが、プロジェクト等のガイドライン等として定められていることがある。これは、goto文が原始的で自由度の高すぎる機能であるため、安易なgoto文の使用は[プログラムの構造化を妨げ](../Page/プログラム_\(コンピュータ\).md "wikilink")、[デバッグ](../Page/デバッグ.md "wikilink")などが行いにくくなり、[バグ](../Page/バグ.md "wikilink")の発生や、[メンテナンス](../Page/メンテナンス.md "wikilink")性・[可読性](../Page/可読性.md "wikilink")の低下の原因になりやすいからである。

しかし、多重にネストした[for文](https://ja.wikipedia.org/wiki/for文 "wikilink")や[if文](https://ja.wikipedia.org/wiki/if文 "wikilink")、[while文](https://ja.wikipedia.org/wiki/while文 "wikilink")などでエラー処理や例外処理などが複雑になる場合はgoto文を使った方がプログラムがすっきりと書けるケースもあるため、プログラムの構造を熟知した[プログラマ](../Page/プログラマ.md "wikilink")が状況に応じて使い分けるものとされている。

エラー処理や[例外処理](../Page/例外処理.md "wikilink")、[RAII](../Page/RAII.md "wikilink")などの仕組みが充実している言語の場合、goto文が必要になるケースが少ない。この傾向はC言語よりも後発の[オブジェクト指向言語](https://ja.wikipedia.org/wiki/オブジェクト指向言語 "wikilink")で顕著である。そのため、言語仕様として始めから用意されていないケースもある。こうした言語としては、[Java](https://ja.wikipedia.org/wiki/Java "wikilink")などが挙げられる。一方では、[PHPで](../Page/PHP_\(プログラミング言語\).md "wikilink")、[2009年](../Page/2009年.md "wikilink")にリリースされたバージョン5.3からgoto が追加された\[2\]ように、高度化する言語構造の中でgoto文が一定の再評価を受ける例もある。

[BASIC](../Page/BASIC.md "wikilink")の様な言語や低レベルの制御言語ではgoto文は不可欠であり、goto文を利用しないと分岐やループを使ったプログラムが記述出来ないものもある。しかし、拡張されたBASICの中には、goto文がほとんど不必要になってしまっているものもある。

前述のように、goto文の安易な使用はプログラムの可読性を著しく低下させる。こうした可読性の低いコードのことを、制御構造が複雑に絡まっているという意味を込めて、[スパゲティコードと呼ぶことがある](../Page/スパゲティプログラム.md "wikilink")。

### goto文論争

「[構造化プログラミング](../Page/構造化プログラミング.md "wikilink")」を提唱していた[コンピュータ科学](https://ja.wikipedia.org/wiki/コンピュータ科学 "wikilink")者らの一人であった[ダイクストラは](../Page/エドガー・ダイクストラ.md "wikilink")、1968年に**Go To Statement Considered Harmful**（「Go To 文は有害（Harmful）とみなされる」）という刺激的な記事を国際学会[ACMの学会誌Communications](../Page/Association_for_Computing_Machinery.md "wikilink") of the ACMに投稿し（ただし、本人が付けたタイトルは**A Case Against the Goto Statement**という穏便なもので、少なくともタイトルの過激さと、レターとして発表を急いだことは、編集を担当していた[ヴィルトによるものである](../Page/ニクラウス・ヴィルト.md "wikilink")）、こんにちでは構造化プログラミングに関して最も良くその名前だけが知られている論争となっている（その内実は言葉の有名さの割には全く知られていないし、そもそも内容や意味の理解は半世紀という時代の違いによって、かなり難しくなっていることも確かである）。[クヌースの言葉を借りるならば](../Page/ドナルド・クヌース.md "wikilink")、「`go to` 文除去の話の二番目の場面は，多くの人たちが第一幕だと思っている事実である．」\[3\]（という解説自体も1974年に書かれたものである）。

また considered harmful というフレーズはその後、定番ネタとして、しばしば似たような深刻な、あるいは軽妙な論争に関して付けられるものとなっている（英語版[:en:Considered harmfulの記事などを参照](https://ja.wikipedia.org/wiki/:en:Considered_harmful "wikilink")）。

### ダイクストラの主張

“Go To Statement Considered Harmful”\[4\]の趣旨は次の通りである。

  - 人間が時間によって変化するプロセスを把握する能力は、プログラムの静的な関係を把握する能力に比べて劣っているため、静的なプログラムテキストの構造と時間によって変化するプロセスの構造をなるべく近づけるのが重要である。
  - そのためにはプロセスの進捗を表す簡潔な指標が必要である。指標とは例えば実行中の[行番号](../Page/行番号.md "wikilink")・その時点での[スタックトレース](../Page/スタックトレース.md "wikilink")・行番号とループを回った回数のペアなどである。
  - 例えば、1人が部屋に入るごとにカウンタを増やしていくプログラムにおいて、カウンタが室内の人数-1である瞬間はどこにあるのかという問いに答える際に、簡潔な指標があればすぐ答えられるが、簡潔な指標がなければ正確な答えは難しくなる。
  - goto文を無条件に許してしまうと簡潔な指標は得られなくなってしまうため、高水準プログラミング言語においてはgoto文は廃止するべきである。

その一方で[クヌースの指摘](../Page/ドナルド・クヌース.md "wikilink")\[5\]によると、ダイクストラは“Structured Programming”\[6\]においてはgoto文には触れていない。実際に“Structured Programming”においては“sequencing should be controlled by alternative, condtional and repetitive clauses and procedure calls, rather than by statements transferring control to labelled points.”との1文があるのみでそれ以外では触れていない。

また、「3つの基本構造」（後述）についても、“Go To Statement Considered Harmful”においては“I do not claim that the clauses mentioned (引用者註: 順次・分岐・手続き呼び出し・反復) are exhaustive in the sense that they will satisfy all needs”とし、「3つの基本構造」には固執していない。

「構造化プログラミングの観点からgoto文を使うのは望ましくない」ものの「単にgoto文を使わなければ見通しが良くなる」という考えは“Go To Statement Considered Harmful”\[7\]でも否定されており、goto文の有無のみに固執するのは不毛である。構造化プログラミングの本質の一つは、状態遷移の適切な表現方法とタイミングを見極めることである\[8\]。

### 3つの基本構造

「goto文有害説」は、ほとんどの場合、「構造化定理」（[:en:Structured program theorem](https://ja.wikipedia.org/wiki/:en:Structured_program_theorem "wikilink")）に結びつけて主張されたものだと誤解にもとづいて間違って信じられている。構造化定理は、

  - 連接 (sequence): `文1; 文2`
  - 選択 (selection): `if 式 then 文1 else 文2 fi`
  - 繰返し (iteration): `do 文 od`

という、「3つの基本構造」によって、[フローチャート](../Page/フローチャート.md "wikilink")で記述された[計算可能な関数は](../Page/計算可能性理論.md "wikilink")、全て表現できる、というものである。この定理の意味する所は、[チャーチ＝チューリングのテーゼ](../Page/チャーチ＝チューリングのテーゼ.md "wikilink")と同じようなものである。すなわち、計算可能な関数について、それを計算する[チューリングマシン](../Page/チューリングマシン.md "wikilink")を構成することもできるし、[ラムダ計算](../Page/ラムダ計算.md "wikilink")によって計算することもできるし、[帰納的関数](https://ja.wikipedia.org/wiki/帰納的関数 "wikilink")として定義することもできる、といったことと同様に、フローチャートでも、あるいは「3つの基本構造」の組み合わせによってでも表現できる、ということである。

できる、というだけで、そのようにして表現されたものが人間にわかりやすいか否かについては全く何も主張していないにもかかわらず、「この理論に従えばgotoを除去できる」（これは正しい）、「ゆえにわかりやすいプログラムになる」（これは正しくない）というのが、「goto文有害説」であるとして信じられるようになったため、この記事内を含め、そういったような記述がしばしば見られるが、前提の時点で間違っている。

構造化定理に従って「gotoの無いプログラム」に書き換えたプログラムが実際のところどのようなものであるのかは、英語版記事の [:en:Structured program theorem\#Single-while-loop, folk version of the theorem](https://ja.wikipedia.org/wiki/:en:Structured_program_theorem#Single-while-loop,_folk_version_of_the_theorem "wikilink") に示されている。クヌースは「`go to` 文を用いた構造的プログラミング」の中で、これと同様のプログラムを示し「これですべての goto 文を除去できたわけであるが，実際にはすべての構造を失ってしまっている．」と述べ、構造化定理が示すことは、全くの「**非**[構造化プログラミング](../Page/構造化プログラミング.md "wikilink")」であることを警告した。

### goto擁護派

一方、**goto文**を使わずに3つの基本構造による代替を行うと、理論上は同値であっても実際にはプログラムの実行速度や記憶容量の点で性能が劣化する場合があることを示し、goto文を擁護する意見もあった\[9\]。

前の節で述べたように、本来の主張では、goto文は全て3つの基本構造による代替によって書けるのだから、それにより書き換えよう、などという主張ではなかったので、「理論上は同値であっても実際にはプログラムの実行速度や記憶容量の点で性能が劣化する場合があることを示し、goto文を擁護する意見」というものが、そもそも変である。

ACMの年次大会(1972)の討論会では、トップダウンでプログラムを分割するよりgoto文を使う方が適した事例があり、証明には関心がないという意見(William Wait)や、goto文を残せば選択の余地があるが、無くしてしまうと必要になったとき困るだろうという意見(Guy Steel)などが出された\[10\]。

条件文とgoto文を正しく使うことで、FORTRANでもALGOLの基本機能を実現できることを例に挙げ、プログラマは必要な機能がプログラミング言語で直接表現できないとき、どのように実装するか工夫できるべきであるという主張もあった(S.W.スリア)\[11\]。

また、ドナルド・クヌースは「`go to` 文を用いた構造的プログラミング」（『[文芸的プログラミング](../Page/文芸的プログラミング.md "wikilink")』収録）の中で、いくつかのgotoを使ったほうが良いだろうという例を挙げているが、その中には、再帰呼出しのある正当なプログラムを、正当な変形によってループによるプログラムに書き換えた結果「ループの中に飛び込むgoto」になる、といったような例も挙げている\[12\]。

### gotoの現在

現在[C言語](../Page/C言語.md "wikilink")を除く主流派の言語では、そのままのgoto文はほとんど見られなくなった。替わりに[break文](https://ja.wikipedia.org/wiki/break文 "wikilink")、[continue文](https://ja.wikipedia.org/wiki/continue文 "wikilink")、もしくは[例外処理](../Page/例外処理.md "wikilink")のような特殊脱出(去勢されたgotoとも呼ばれる（実際には関数呼出しをまたいだ、いわゆる大域脱出もできるのだから、gotoよりも例外処理のほうが強力である（が、それを理解できない者も多い））)をサポートし、単純な制御構造だけでは弱いと考えられる部分を補っている。さらに[クロージャ](../Page/クロージャ.md "wikilink")や[コードブロック](https://ja.wikipedia.org/wiki/コードブロック "wikilink")、[継続](../Page/継続.md "wikilink")のような強力な制御機構を使い、抽象度の低いgoto文を使う必要性を低くした言語もある。例えば[Haskell](../Page/Haskell.md "wikilink")においてはモナドを利用して例外や非決定性計算などの様々な制御構造を表現できる。また[Smalltalk](../Page/Smalltalk.md "wikilink")や[Ioにおいても制御構造はブロックを扱うメソッドとして表現している](../Page/Io_\(プログラミング言語\).md "wikilink")。Scheme等でサポートされている[継続](../Page/継続.md "wikilink")は「引数付きgoto」と呼ばれることもある。

一方で、例えば1999年から設計された[D言語](../Page/D言語.md "wikilink")はgoto文を含んでいる\[13\]。[PHPにも](../Page/PHP_\(プログラミング言語\).md "wikilink")2009年にリリースされた5.3において制限された形ではあるがgoto文が追加された\[14\]。

### その他の話題

それまでの職人芸的なプログラミングの時代から、構造化プログラミングというパラダイムの提唱によって、プログラミング技法の体系化を試みる[プログラミング工学](https://ja.wikipedia.org/wiki/プログラミング工学 "wikilink")という学問が芽生えたと言っても過言では無いだろう。

なお、論文“Go To Statement Considered Harmful”は、その半ば挑戦的な題名がプログラミング以外の様々な分野に及んで評判となり、それをもじった様々な “～ Considered Harmful”といった論説やジョークが生まれた[:en:Considered harmful](https://ja.wikipedia.org/wiki/:en:Considered_harmful "wikilink") 。極めつきは、何かが有害であることだけが強調される題名の有害性を指摘した“‘Considered Harmful’ Essays Considered Harmful”であろう。 同じく[What led to "Notes on Structured Programming"](http://www.cs.utexas.edu/users/EWD/transcriptions/EWD13xx/EWD1308.html)においてダイクストラは、Millsによって矮小化されたgoto文廃止という概念のもと、IBMが用語としての「構造化プログラミング」を盗用したと語っている。

ダイクストラの著書は、分かりにくいことと誤解を招きやすいことで定評がある\[15\]\[16\]\[17\]。それを憂いたは、ダイクストラ流のプログラミングについて体系化した書籍「プログラミングの科学」(The Science of Programming)を書いた\[18\]。

## gotoとバグ

### gotoを使用しなかったことによる大規模障害

1990年1月15日に起きた、AT\&Tの長距離電話網の停止 (crash) は、break文による脱出先の勘違いによるものであった。[:en:List of software bugs\#Telecommunicationsも参照](https://ja.wikipedia.org/wiki/:en:List_of_software_bugs#Telecommunications "wikilink")。

そもそもソフトウェアの制御パステストを十分に実施していなかったせいで不具合が発見されなかったことが障害につながったのだが\[19\]、適切な名前のラベルを用意し、ループ脱出にgotoを使っていれば避けられたバグでもあった。

### gotoを使用したことによる脆弱性

アップルのSSL/TLS実装で発見された脆弱性CVE-2014-1266には、**goto fail**という通称がある。goto文の誤った記述により、本来必要な署名検証処理が実行されずに処理成功として扱ってしまうというものであった。

ただし、このバグを正確に表現すると以下のような原因の複合であり、gotoは「たまたまそこにあった文がgotoだった」と捉えるのが普通のプログラマの感覚である。すなわち、

1.  if文の帰結節に、ブロック（「複文」）だけでなく、「式文」などの単なる「文」も書ける、というALGOLやC言語の構文
2.  そのために、インデントによる見た目と、真の構造が一致していない、というミスリード状態に気が付きにくいこと
3.  そのために、1個目のgoto文により、一見では到達不能コードに見える2個目のgoto文が、到達可能だったこと
4.  そのために別の、セキュリティ的に絶対に実行されなければならないコードが、到達不能コードになっていたこと
5.  2個目のgoto文は、到達不能コードだと思うのならば、放置せずに削除しなければならなかったこと
6.  一方で、2個目のgoto文は実際には到達不能コードではなかったので、第三者には、その部分を見ただけでは、削除して良いのか判断不可能だったこと

## 脚注

### 注釈

### 出典

## 関連項目

  - [if文](https://ja.wikipedia.org/wiki/if文 "wikilink")
  - [for文](https://ja.wikipedia.org/wiki/for文 "wikilink")
  - [while文](https://ja.wikipedia.org/wiki/while文 "wikilink")
  - [継続](../Page/継続.md "wikilink")
  - [非構造化プログラミング](../Page/非構造化プログラミング.md "wikilink")
  - [制御構造](../Page/制御構造.md "wikilink")

## 外部リンク

  - *Go To Statement Considered Harmful* について
      - [Go To Statement Considered Harmful](http://www.acm.org/classics/oct95/) Edsger W. Dijkstra
      - [Go To Statement Considered Harmful: A Retrospective](http://david.tribble.com/text/goto.html) David R. Tribble
      - [Code Reads \#2: Dijkstra's "Go To Statement Considered Harmful"](http://www.wordyard.com/2006/10/10/dijkstra-goto/) Scott Rosenberg
      - [Radium Software Development - Go To Statement Considered Harmful](http://www.radiumsoftware.com/0612.html#061208)
      - [What led to "Notes on Structured Programming" (EWD1308)](http://www.cs.utexas.edu/users/EWD/transcriptions/EWD13xx/EWD1308.html) Edsger W. Dijkstra

[Category:制御構造](https://ja.wikipedia.org/wiki/Category:制御構造 "wikilink") [Category:コンピュータ史](https://ja.wikipedia.org/wiki/Category:コンピュータ史 "wikilink") [Category:エドガー・ダイクストラ](https://ja.wikipedia.org/wiki/Category:エドガー・ダイクストラ "wikilink")

1.  [ha ha only serious](http://catb.org/~esr/jargon/html/H/ha-ha-only-serious.html)
2.  [PHP: 新機能 - Manual](http://www.php.net/manual/ja/migration53.new-features.php) - PHPマニュアル（2013年12月4日閲覧）
3.  [有澤誠](https://ja.wikipedia.org/wiki/有澤誠 "wikilink")訳『文芸的プログラミング』 p. 45
4.
5.
6.  [E. W. Dijkstra, “Structured Programming”, In *Software Engineering Techniques*, B. Randell and J.N. Buxton, (Eds.), NATO Scientific Affairs Division, Brussels, Belgium, 1970, pp. 84–88.](http://homepages.cs.ncl.ac.uk/brian.randell/NATO/nato1969.PDF)
7.
8.
9.  [Frank Rubin, *"GOTO Considered Harmful" Considered Harmful*, Communications of the ACM, Vol.30, Issue 3, 1987, pp.195-196.](http://web.archive.org/web/20090320002214/http://www.ecn.purdue.edu/ParaMount/papers/rubin87goto.pdf)
10.
11. 金山裕 編, "構造的プログラミング −批判と支持−", *bit*, Vol.7, Issue 7, 1975, pp.6-13, 共立出版.
12.
13. [Language Reference Goto Statement](http://dlang.org/statement.html#GotoStatement)
14. [PHP マニュアル goto](http://php.net/manual/ja/control-structures.goto.php)
15. 木村泉, "GO TO 論争：第3部 解説", *bit*, Vol.7, Issue 5, 1975, pp.27-39, 共立出版.
16. 二木厚吉 監修, *ソフトウェアクリーンルーム手法*, 日科技連, 1997.
17. 木村泉, "ダイクストラ教授とふた付き命令", *bit*, Vol.8, Issue 9, 1976, pp.29-34, 共立出版.
18.
19. [All Circuits are Busy Now: The 1990 AT\&T Long Distance Network Collapse](http://users.csc.calpoly.edu/~jdalbey/SWE/Papers/att_collapse.html)
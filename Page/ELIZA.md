> この記事は[ELIZA](https://ja.wikipedia.org/wiki/ELIZA)から翻訳されています。


[thumbでのELIZAの例](https://ja.wikipedia.org/wiki/ファイル:GNU_Emacs_ELIZA_example.png "wikilink")\]\] **ELIZA**（イライザ）は初期の素朴な[自然言語処理](../Page/自然言語処理.md "wikilink")[プログラムの](../Page/プログラム_\(コンピュータ\).md "wikilink")1つである。対話型（インタラクティブ）であるが 、音声による会話をするシステムではない。スクリプト (script) へのユーザーの応答を処理する形で動作し、スクリプトとしては**DOCTOR**という[来談者中心療法](../Page/来談者中心療法.md "wikilink")のセラピストのシミュレーションが最もよく知られている。人間の思考や感情についてほとんど何の情報も持っていないが、DOCTORは驚くほど人間っぽい対話をすることがあった。[MITの](../Page/マサチューセッツ工科大学.md "wikilink")[ジョセフ・ワイゼンバウム](../Page/ジョセフ・ワイゼンバウム.md "wikilink")が1964年から1966年にかけてELIZAを書き上げた。いわゆる[人工無脳](../Page/人工無脳.md "wikilink")の起源となったソフトウェアである。

ユーザー（患者役）の入力する文がDOCTOR内の非常に小さな知識ベースの範囲外のものだった場合、DOCTORは一般的な応答を返す。例えば、「頭が痛い」と言えば「なぜ、頭が痛いとおっしゃるのですか？」などと返し、「母は私を嫌っている」と言えば「あなたの家族で他にあなたを嫌っている人は？」（この場合「母」が「家族」の下位概念である、という知識ベースは必要である）などと返す。単純な[パターンマッチ技法を使っているが](../Page/パターンマッチング.md "wikilink")、一部のユーザーはワイゼンバウムがその仕組みを説明しても納得せず、ELIZAの応答を真剣に受け止めた。

## 概要

ワイゼンバウムは、DOCTORについて「初期の[精神医学](../Page/精神医学.md "wikilink")的インタビューにおける無指向性精神療法医の反応」の「[パロディ](../Page/パロディ.md "wikilink")」であると述べている\[1\]。彼が精神療法を選んだのは「実世界の知識に関するデータベースをプログラムに入力するという問題を避けるため」であり\[2\]、精神療法という状況は人間同士の対話でありながら、その対話内容に関する知識をほとんど必要としないという特徴があったためである。例えば「好きな作曲家は？」という質問には「あなた自身の好きな作曲家は？」とか「その質問は重要ですか？」などと返すことができ、作曲家に関する知識を必要としない。

ELIZAという名前は[ジョージ・バーナード・ショー](../Page/ジョージ・バーナード・ショー.md "wikilink")の戯曲『[ピグマリオン](../Page/ピグマリオン_\(戯曲\).md "wikilink")』の登場人物[イライザ・ドゥーリトル](https://ja.wikipedia.org/wiki/イライザ・ドゥーリトル "wikilink")にちなんだものである。彼女は[上流階級](../Page/上流階級.md "wikilink")の[アクセント](../Page/アクセント.md "wikilink")での話し方を教えられる労働者階級の役である\[3\]。

ワイゼンバウムは当初、独自のリスト処理言語[SLIPで実装した](https://ja.wikipedia.org/wiki/:en:SLIP_\(programming_language\) "wikilink")。簡単な[構文解析](../Page/構文解析.md "wikilink")を行い、抜き出したキーワードを決まり文句に埋め込む。ユーザーが最初に入力する文章によっては、対話の相手が人間であると言う幻想は即座に消し去られることもあるし、何度かのやり取りを続けることができる場合もある。時には対話が非常にうまくいき、マシンの真の理解力不足が明らかになるまで数分間DOCTORと感情的にやりとりした人々の逸話は数多い。これは全て、人間側がコンピュータの出力した文に独自に意味を読み取った結果である。

1966年当時、対話型コンピューティングは目新しかった。[パーソナルコンピュータ](../Page/パーソナルコンピュータ.md "wikilink")が一般化する約15年前であり、インターネット（[Ask.com](../Page/Ask.com.md "wikilink")）やアプリケーションソフト（[クリッパー](https://ja.wikipedia.org/wiki/Microsoft_Office#Office_アシスタント "wikilink")）での[自然言語処理](../Page/自然言語処理.md "wikilink")が一般化する30年も前のことである。これらのプログラムは長年の研究の成果であるが、ELIZA は人間とマシンの対話を人間と人間の対話に見せかけようとした最初の試みとして記録に残るだろう。

1976年、ワイゼンバウムの書いた記事 "Computer Power and Human Reason" が *[The New Media Reader](https://ja.wikipedia.org/wiki/:en:The_New_Media_Reader "wikilink")* 誌に掲載された。その中でワイゼンバウムは人々がいかに素早くかつ深くそのコンピュータプログラムに感情的に没頭したかを記している。対話の記録を見ようとするとプライバシーの侵害だとして拒んだり、対話中は部屋に一人きりにしてくれと頼んだりといったことがあったという。

## 主な実装

ワイゼンバウムのオリジナルは[SLIPで実装されていたが](https://ja.wikipedia.org/wiki/:en:SLIP_\(programming_language\) "wikilink")、これを Bernie Cosell が[LISP](https://ja.wikipedia.org/wiki/LISP "wikilink")に移植した\[4\]。LISPは当時主流の言語ではなく、どこでも使えるものではなかった。多くの人がELIZAに触れたのは[BASIC](../Page/BASIC.md "wikilink")への移植版が登場してからで、Jeff Shrager が1973年に移植したものを *[Creative Computing](https://ja.wikipedia.org/wiki/:en:Creative_Computing "wikilink")* 誌が1977年に掲載したのが最初である\[5\]。このバージョンが初期の各種パーソナルコンピュータ（特に [Apple II](../Page/Apple_II.md "wikilink") と [IBM PC](../Page/IBM_PC.md "wikilink")）で動作し、そこから様々な言語に移植され派生していった。

ソフトウェア技術者の間で人気となったバージョンとして、[GNU Emacs](../Page/GNU_Emacs.md "wikilink") に当初から組み込まれていたものがある。通常、meta-x-doctor と入力することでアクセスできる。

## ゲームへの影響

ELIZA は[コンピュータゲーム](../Page/コンピュータゲーム.md "wikilink")の[ユーザインタフェース設計](../Page/ユーザインタフェース設計.md "wikilink")にもいくつかの影響を与えた。[Don Daglow](https://ja.wikipedia.org/wiki/:en:Don_Daglow "wikilink") は[1973年](../Page/1973年.md "wikilink")、最初期の[コンピュータRPG](../Page/コンピュータRPG.md "wikilink") *[Dungeon](https://ja.wikipedia.org/wiki/ダンジョン_\(コンピュータゲーム\) "wikilink")*（1975年）を製作する前に[PDP-10](../Page/PDP-10.md "wikilink")上で *Ecala* と呼ばれるELIZAを拡張したプログラムを書いている。[Will Crowther](https://ja.wikipedia.org/wiki/:en:Will_Crowther "wikilink") が作った *[Adventure](https://ja.wikipedia.org/wiki/コロッサル・ケーブ・アドベンチャー "wikilink")*（1975年）という世界初の[アドベンチャーゲーム](../Page/アドベンチャーゲーム.md "wikilink")にも ELIZA の影響が見られる。これらのゲームは ELIZA の9年後に登場した。

日本での影響は[人工無脳](../Page/人工無脳.md "wikilink")を参照されたい。

## アニメ・ドラマへの影響

2008年に放映されたテレビアニメ「[RD 潜脳調査室](../Page/RD_潜脳調査室.md "wikilink")」にてエライザ・ワイゼンバーグという名前のチャットプログラムが登場した。

ドラマ「[ケータイ捜査官7](../Page/ケータイ捜査官7.md "wikilink")」にサーバーの名前として登場した。

SF小説でアニメ化もされた「[BEATLESS](https://ja.wikipedia.org/wiki/BEATLESS "wikilink")」に、人類の知性を超えた超高度AIによって作られたアンドロイド政治家の名前に起用された。

## 反響と遺産

ELIZAへの反響の大きさはワイゼンバウムを悩まし、『コンピュータ・パワー 人工知能と人間の理性』（*Computer Power and Human Reason: From Judgment to Calculation*）という本を書かせる動機となった。この著書で彼はコンピュータの限界を論じ、コンピュータを万能であるかのように見ている人々に人間や生命の重要性を説いた。*[Plug & Pray](https://ja.wikipedia.org/wiki/:en:Plug_&_Pray "wikilink")*（2010年）というドキュメンタリー映画で、ワイゼンバウムはELIZAが画期的だと言ったのは誤解している人々だけだったと述べている\[6\]。

[イスラエル](../Page/イスラエル.md "wikilink")の詩人 [David Avidan](https://ja.wikipedia.org/wiki/:en:David_Avidan "wikilink") は、先端技術が好きで芸術に応用しており、コンピュータを使って文学を生み出そうとしてきた。例えば、ELIZAの[APL](../Page/APL.md "wikilink")版との対話を何度か行い、その内容を *My Electronic Psychiatrist – Eight Authentic Talks with a Computer* と題して出版したことがある。その序文でこれを [constrained writing](https://ja.wikipedia.org/wiki/:en:constrained_writing "wikilink") の一種だとしている\[7\]。

先にあげた*Ecala*以外にも ELIZA の方式に基づいた様々なプログラムが様々な言語で作成されてきた。例えば、[1980年](https://ja.wikipedia.org/wiki/1980年 "wikilink")には、Randy Simon の Don't Ask Software という会社が [Apple II](../Page/Apple_II.md "wikilink")、[アタリ](../Page/アタリ_\(企業\).md "wikilink")、[コモドール](../Page/コモドール.md "wikilink")など向けにELIZA風のプログラム Abuse を開発している。これは名前の通り、ユーザーの入力にののしりで応答するものだった\[8\]。[スペイン](https://ja.wikipedia.org/wiki/スペイン "wikilink")では Jordi Perez が [1993年](../Page/1993年.md "wikilink")に [Clipper 言語で](../Page/Clipper_\(プログラミング言語\).md "wikilink") [MS-DOS](../Page/MS-DOS.md "wikilink") 向けに書かれた ZEBAL というプログラムを開発した。また、ELIZA に基づいて宗教的なバージョンのプログラムも開発された（キリストやブッダと対話するというもの）。1980年のゲーム Prisoner にも ELIZA風の対話が用いられている。

[ジョージ・ルーカス](../Page/ジョージ・ルーカス.md "wikilink")の映画『[THX 1138](../Page/THX_1138.md "wikilink")』（1971年）では、未来の地下社会の住民がストレスを感じたときに利用する[告解](../Page/告解.md "wikilink")室が登場し、キリスト風の顔を表示したコンピュータとELIZAのような対話をするシーンがある。

イギリス人アーティストでワイゼンバウムの友人でもある [Brian Reffin Smith](https://ja.wikipedia.org/wiki/:en:Brian_Reffin_Smith "wikilink") は1988年、フランスの[ブールジュ](../Page/ブールジュ.md "wikilink")にて 'Salamandre' という[インタラクティブアート](../Page/インタラクティブアート.md "wikilink")を展示した。これは[BASIC](../Page/BASIC.md "wikilink")で書かれた 'Critic'（評論家）と 'Artist'（芸術家）というELIZA風プログラムを2台の[Amiga](../Page/Amiga.md "wikilink")に搭載して動作させるもので、観客は一方が表示した文をもう一方に打ち込むことで会話を成り立たせる。実はこの2つのプログラムは全く同じものだった。

[2011年](../Page/2011年.md "wikilink")に発売された[スマートフォン](https://ja.wikipedia.org/wiki/スマートフォン "wikilink")、[iPhone 4Sの日本語版](https://ja.wikipedia.org/wiki/iPhone_4S "wikilink")[Siri](https://ja.wikipedia.org/wiki/Siri "wikilink")(人工知能エンジン)で「イライザ」について質問すると、友人の元精神科医である旨の回答がなされる。また「面白い話をして」「長い話をして」と質問した際に出力される小話の中にも「ELIZA」が登場し、ここでもELIZA風の対話を交わしている。

IPsoftは仮想サービスデスク・アシスタントElizaを開発した。このソフトウェアは顧客の電子メールや電話に応答するもので、約3分の2の問題を人間の助けなしで解決できるという\[9\]。[INGグループ](../Page/INGグループ.md "wikilink")や[モルガン・スタンレー](../Page/モルガン・スタンレー.md "wikilink")が顧客対応にElizaを使っている\[10\]。

## 実装例

  - [Java](https://ja.wikipedia.org/wiki/Java "wikilink")版（ワイゼンバウムの本来の仕様に非常に近い）: <http://chayden.net/eliza/Eliza.html>
  - [プログラム電卓](https://ja.wikipedia.org/wiki/プログラム電卓 "wikilink")[TI-83 シリーズ上で](../Page/TI-83_シリーズ.md "wikilink")[Cを使った実装](../Page/C言語.md "wikilink"): <http://www.ticalc.org/archives/files/fileinfo/354/35463.html>
  - [Perl](../Page/Perl.md "wikilink")モジュール [Chatbot-Eliza](http://search.cpan.org/dist/Chatbot-Eliza/) -- [実装例](http://www.terrence.com/perl/eliza/eliza.cgi)
  - `doctor.el` [1985年](https://ja.wikipedia.org/wiki/1985年 "wikilink")ごろ、[Emacs Lispで実装された](../Page/Emacs_Lisp.md "wikilink")。http://www.cs.cmu.edu/afs/cs/project/ai-repository/ai/areas/classics/eliza/emacs/0.html
  - [Pop-11 Eliza](http://www.cs.bham.ac.uk/research/projects/cogaff/eliza) は[Poplog](https://ja.wikipedia.org/wiki/Poplog "wikilink")システムで動作する。Poplog は[サセックス大学](../Page/サセックス大学.md "wikilink")でAIを学ばせるために使われたシステムであり、現在はフリーなオープンソースシステムの一部である。
  - Trans-Tex Software の Mac OS および OS X 向け実装: <http://www.tex-edit.com/index.html#Eliza>
  - [Tcl版](https://ja.wikipedia.org/wiki/Tcl/Tk "wikilink"): <http://wiki.tcl.tk/9235>
  - [BASIC](../Page/BASIC.md "wikilink")版: <http://www.atariarchives.org/bigcomputergames/showpage.php?page=20>
  - [GNU Guile版](https://ja.wikipedia.org/wiki/GNU_Guile "wikilink"): <https://github.com/apgwoz/chatter>
  - LISP版（Apple II 版がベース）: <http://jeffshrager.org/llisp/26.html>

## 脚注

## 参考文献

  -
  -
  -
  -
  -
## 関連項目

  - [ELIZA効果](../Page/ELIZA効果.md "wikilink")
  - [AIML](../Page/Artificial_Intelligence_Markup_Language.md "wikilink")
  - [チューリングテスト](https://ja.wikipedia.org/wiki/チューリングテスト "wikilink")
  - [ローブナー賞](../Page/ローブナー賞.md "wikilink")
  - [人工意識](../Page/人工意識.md "wikilink")
  - [会話ボット](https://ja.wikipedia.org/wiki/会話ボット "wikilink")
      - [Jabberwacky](../Page/Jabberwacky.md "wikilink")
      - [PARRY](https://ja.wikipedia.org/wiki/PARRY "wikilink")
      - [A.L.I.C.E.](../Page/Artificial_Linguistic_Internet_Computer_Entity.md "wikilink")

## 外部リンク

  - [dialogues with colorful personalities of early AI](http://www.stanford.edu/group/SHR/4-2/text/dialogues.html)、ELIZAとの対話集その他
  - [EllaZ Systems](http://www.ellaz.com) オンライン版chatterbot（ELIZAの一種の拡張）。WWW上のいくつかの情報源を利用して自然言語で対話を行う。
  - [Project Prometheus](http://www.elfqrin.com/promethbox.html) ELIZA風オンラインおしゃべりボット
  - [Eliza JS](http://abcguides.com/abcsoftware/eliza_js.htm) JavaScript版ELIZA。[フレームあり](http://abcguides.com/abcsoftware/eliza_js_frame.htm)と[フレームなし](http://abcguides.com/abcsoftware/eliza_js_noframe.htm)がある。
  - [WEIZENBAUM. REBEL AT WORK](http://www.ilmarefilm.org/W_E_1.htm) - Peter Haas, Silvia Holzinger, ジョセフ・ワイゼンバウムとELIZAに関するドキュメンタリーフィルム
  - [Questsin](http://questsin.net/Avatar.asp) - MSNメッセンジャー版ELIZA
  - [Eliza 日本語版](http://shower.human.waseda.ac.jp/~m-kouki/cgi-bin/eliza/index.html) - 日本語版ELIZA(Java)
  - [CounterCounseling](http://maedanaoki.jp/software/countercounseling/index.html) - C言語版ELIZA [オープンソース](../Page/オープンソース.md "wikilink")
  - [Eliza Chat Bot](http://apps.facebook.com/eliza-chatbot) – facebook上の会話ボット。ワイゼンバウムのオリジナルの仕様に沿った実装。

[Category:人工知能の歴史](https://ja.wikipedia.org/wiki/Category:人工知能の歴史 "wikilink") [Category:自然言語処理](https://ja.wikipedia.org/wiki/Category:自然言語処理 "wikilink") [Category:アプリケーションソフト_(製品)](https://ja.wikipedia.org/wiki/Category:アプリケーションソフト_\(製品\) "wikilink") [Category:チャットボット](https://ja.wikipedia.org/wiki/Category:チャットボット "wikilink")

1.
2.
3.
4.  [Bernie Cosell](http://www.codersatwork.com/bernie-cosell.html)
5.  [ELIZA](http://www.atariarchives.org/bigcomputergames/showpage.php?page=20) - Big Computer Games (1984)
6.  [*Plug & Pray*](http://www.plugandpray-film.de/en/content.html), documentary film featuring Joseph Weizenbaum and [Ray Kurzweil](../Page/レイ・カーツワイル.md "wikilink")
7.
8.
9.  <http://www.economist.com/news/special-report/21569573-attractions-employing-robots-rise-software-machines>
10. <http://www.techwireasia.com/270/forget-siri-meet-eliza-the-siri-of-outsourcing/>
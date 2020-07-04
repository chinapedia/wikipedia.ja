> この記事は[Emacs](https://ja.wikipedia.org/wiki/Emacs)から翻訳されています。


**Emacs** （イーマックス、）は、その[拡張性](../Page/拡張性.md "wikilink")を特徴とした[テキストエディタ](../Page/テキストエディタ.md "wikilink")のファミリーである\[1\]。Emacsの中で最も広く使われている派生物はGNU Emacsである\[2\]が、そのマニュアルにはEmacsを「the extensible, customizable, self-documenting, real-time display editor」（拡張およびカスタマイズが可能で、自己文書化を行い、リアルタイム表示を行うエディタ）であると説明されている\[3\]。最初のEmacs開発が1970年代中盤に開始されてから、その直系の子孫であるGNU Emacsが製作され、その開発がも続いている。

Emacsは[ユーザインタフェース](../Page/ユーザインタフェース.md "wikilink")と10,000を超える組み込みコマンドを持ち、ユーザーは作業自動化のためにこれらのコマンドを[マクロと組み合わせることができる](../Page/マクロ_\(コンピュータ用語\).md "wikilink")。さらに深い拡張性を提供する[LISP](https://ja.wikipedia.org/wiki/LISP "wikilink")[プログラミング言語](../Page/プログラミング言語.md "wikilink")の方言である[Emacs Lisp](../Page/Emacs_Lisp.md "wikilink") (ELisp) はEmacs実装の主な特徴であり、ELispでユーザーや開発者はEmacs用の新しいコマンドやアプリケーションを書くことができる。Emacsの拡張機能として[電子メール](../Page/Gnus.md "wikilink")、[ファイル](../Page/Dired.md "wikilink")、[アウトライン](https://ja.wikipedia.org/wiki/Orgmode "wikilink")、および[RSS](../Page/RSS.md "wikilink")フィードが書かれており\[4\]、それ以外にも[ELIZA](../Page/ELIZA.md "wikilink")、[ポン](../Page/ポン_\(ゲーム\).md "wikilink")、[ライフゲーム](../Page/ライフゲーム.md "wikilink")、[ヘビゲーム](https://ja.wikipedia.org/wiki/ヘビゲーム "wikilink")、および[テトリス](../Page/テトリス.md "wikilink")のクローンもある\[5\]。ユーザーの中にはEmacs内部からテキスト編集だけでなくほとんど全ての作業を行うことができることに気づいた者もいる\[6\]。

原典であるEMACSは[1972年](../Page/1972年.md "wikilink")にCarl Mikkelson、、および[ガイ・L・スティール・ジュニアらにより](../Page/ガイ・スティール・ジュニア.md "wikilink")[TECOエディタ用の](../Page/Text_Editor_and_Corrector.md "wikilink")*Editor MACroS*のセットとして書かれたものであり\[7\]\[8\]\[9\]\[10\]\[11\]、TECOマクロエディタの概念にインスパイアされている\[12\]。

最も有名かつ最も移植されたEmacsは、ストールマンによって[GNUプロジェクト](../Page/GNUプロジェクト.md "wikilink")のために作成された[GNU Emacsである](../Page/GNU_Emacs.md "wikilink")\[13\]。[XEmacs](https://ja.wikipedia.org/wiki/XEmacs "wikilink")は1991年にGNU Emacsから[フォークされた派生物である](../Page/フォーク_\(ソフトウェア開発\).md "wikilink")。GNU EmacsとXEmacsは類似のLISP方言を使い、互いに互換性のある部分が大半である。

Emacsは[vi](https://ja.wikipedia.org/wiki/vi "wikilink") ([Vim](../Page/Vim.md "wikilink")) と並び[UNIX](../Page/UNIX.md "wikilink")文化における伝統的な[エディタ戦争](../Page/エディタ戦争.md "wikilink")の主要な当事者の2つである。Emacsは未だ開発中であるオープンソースプロジェクトの中で最古のものである\[14\]。

## 歴史

[Colorsyntax.png](https://ja.wikipedia.org/wiki/File:Colorsyntax.png "fig:Colorsyntax.png")における[C](../Page/C言語.md "wikilink")[ソースコード](../Page/ソースコード.md "wikilink")の編集\]\] [Cpp_in_GNU_emacs.png](https://ja.wikipedia.org/wiki/File:Cpp_in_GNU_emacs.png "fig:Cpp_in_GNU_emacs.png")から[C++](../Page/C++.md "wikilink")コードを編集してコンパイル\]\] [Space-cadet.jpg](https://ja.wikipedia.org/wiki/File:Space-cadet.jpg "fig:Space-cadet.jpg")の[スペースカデットキーボード](https://ja.wikipedia.org/wiki/スペースカデットキーボード "wikilink")の設計に影響を与えた\[15\]。\]\]

Emacsは1970年代の[MIT人工知能研究所](../Page/MIT人工知能研究所.md "wikilink")（MIT AI研）で産声をあげた。 AI研で使われていた[PDP-6](../Page/PDP-6.md "wikilink")や[PDP-10](../Page/PDP-10.md "wikilink")の[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink")は[Incompatible Timesharing System](../Page/Incompatible_Timesharing_System.md "wikilink") (ITS) であり、そのデフォルトエディタはTECOという[ラインエディタ](https://ja.wikipedia.org/wiki/ラインエディタ "wikilink")であった。TECOは現在の一般的なテキストエディタとは違い、追加・編集・表示用にそれぞれ別々のモードが存在していた。そのため文字を入力しても即座に反映されるわけではなく、代わりにTECOコマンド言語の ('i') 文字を入力して入力モードに切り替えてから必要な文字を入力し、最後に (<esc>) 文字を入力してエディタをコマンドモードに再度切り替える必要があり（上書きが可能なため、同様のテクニックが使われた）、しかも入力モードで編集中の文字は画面に表示されなかった。なおこの振る舞いは現在も使われている[ed](https://ja.wikipedia.org/wiki/ed "wikilink")プログラムと同じである。

リチャード・ストールマンは、1972年と1974年に[スタンフォード人工知能研究所](../Page/スタンフォード人工知能研究所.md "wikilink")を訪れ、Fred Wrightにより書かれたその研究所の「E」エディタを目にした\[16\]。Eの振る舞いは今のエディタの大半で使われている直感的な[WYSIWYG](../Page/WYSIWYG.md "wikilink")であり、ストールマンはその機能に触発されてMITに戻った。 AI研[ハッカー](../Page/ハッカー.md "wikilink")の一人であるCarl Mikkelsenは、利用者がキー操作するたびに画面表示を更新する「Control-R」という表示・編集を組み合わせたモードをTECOに追加していた。ストールマンは、この更新が効率的に動くよう書き直し、任意のキー操作でTECOプログラムが動くように利用者が再定義できる[マクロ機能をTECOの表示](../Page/マクロ言語.md "wikilink")・編集モードに追加した\[17\]。

EにはTECOに不足していたランダムアクセス編集機能が搭載されていた。TECOは[PDP-1](../Page/PDP-1.md "wikilink")の[紙テープ](../Page/紙テープ.md "wikilink")を編集するために設計されたページシーケンシャルエディタであるため、一度に1つの紙テープしか編集することしかできず、さらに紙テープのファイルに存在するページの順に編集しなければならなかった。Eはディスク上のページランダムアクセスを可能にするため、ファイルを構造化するというアプローチを採用していたが、ストールマンはTECOを修正してさらに巨大なバッファを効率的に処理できるようにするというアプローチを採用し、ファイル全体を単一バッファとして読み込み、編集し、書き込めるようにファイル管理方法を変更した。現在ではほとんどのエディタがこのアプローチを用いている。

新しいバージョンのTECOはまたたく間にAI研で評判となり、マクロを意味する「MAC」や「MACS」が語尾に付いた名前のカスタム・マクロの巨大なコレクションが溜まった。さらにその2年後、どんどんばらばらになっていくキーボード・コマンド・セットを1つに統合するプロジェクトを[ガイ・スティール](https://ja.wikipedia.org/wiki/ガイ・スティール "wikilink")が引き受けた\[18\]。ストールマンはスティールとハックしたある夜の後、新しいマクロ・セットの文書化や拡張の機能を含む実装を完成させた\[19\]。こうしてできあがったシステムは*Editing MACroS*や*E with MACroS*を意味するEMACSと呼ばれることになる。ストールマンによると、Emacsとしたのは「当時ITSで\<E\>が略称に使われていなかったから」である\[20\]。作り話である[Hacker koanでは](../Page/ジャーゴンファイル.md "wikilink")[ケンブリッジの人気アイスクリーム店](../Page/ケンブリッジ_\(マサチューセッツ州\).md "wikilink")「」にちなんで名付けられたとしている\[21\]。操作可能な最初のEMACSシステムは1976年後半に姿を現した\[22\]。

ストールマンはEMACSの過度のカスタム化や事実上の分裂の危険に気づいたため、ある使用上の条件をつけた。彼は後に次のような文章を残している\[23\]:

  -
    *「EMACSは、共同参加を基として頒布される。つまり改良点は全て、組み入れて頒布するために、私のところへ戻ってこなければならない」*

原典であるEmacsはTECO同様にPDP-10上だけで動作した。Emacsの振る舞いはTECOのそれとは大きく異なっていてTECOとは独立した別のエディタとみなせるようになり、さらにEmacsは急激にITS上の標準編集プログラムとなった。はEmacsをITSから[TENEXや](https://ja.wikipedia.org/wiki/TOPS-20#TENEX "wikilink")[TOPS-20](../Page/TOPS-20.md "wikilink")オペレーティングシステムに移植した。 初期のEmacsへの貢献者には、このほか、Earl Killian、Eugene Ciccarelliらがいる。1979年までに、EmacsはMIT人工知能研究所やMITコンピュータ科学研究所で使われる主要エディタとなった\[24\]。

### その他の初期実装

その後、他のコンピュータシステム用に多くのEmacs風エディタが書かれた。これらにはMichael McMahonとらが[LISPマシン](../Page/LISPマシン.md "wikilink")用に書いた  (*Eine Is Not Emacs*) とZWEI (*Zwei Was Eine Initally*）\[25\]（なお、ZWEIはドイツ語で「2」の意味でもある。EINEが「1つの」（女性形）にあたるためのもじり。ストールマンの呼ぶEINEは「アイン」のように聞こえるが、ドイツ語の発音は「アイネ」に近い）、そしてOwen Theodore Andersonによって書かれたSINE (*Sine Is Not Emacs*) がある。WeinrebのEINEはLISPで書かれた最初のEmacsである。1978年には[ハネウェル](../Page/ハネウェル.md "wikilink")ケンブリッジ情報システム研究所でによりがほぼ全てを[Multics MACLISPを用いて書かれ](../Page/Maclisp.md "wikilink")、その後とBarry Margolinによりメンテナンスされた。なおRichard SoleyはNILプロジェクト用にNILEというEmacs風エディタを開発し続けていた。GNU Emacsを含むEmacsのバージョンの多くは後に拡張言語としてLISPを採用することになる。UNIXで動作する最初のEmacs風エディタは、後に[NeWS](../Page/NeWS.md "wikilink")や[Java](https://ja.wikipedia.org/wiki/Java "wikilink")の開発で知られることになる[ジェームス・ゴスリング](https://ja.wikipedia.org/wiki/ジェームス・ゴスリング "wikilink")が1981年に書いた[Gosling Emacsであった](../Page/Gosling_Emacs.md "wikilink")。 これは[Cで書かれ](../Page/C言語.md "wikilink")、というLISP風構文の拡張言語を使っていた。Mocklispにはシンボルさえなく\[26\]、構文がLISP風なだけで本当のLISPではない。Gosling Emacsは、現在広く使われている[フリーソフトウェア](../Page/フリーソフトウェア.md "wikilink")の[GNU Emacs や](https://ja.wikipedia.org/wiki/GNU_Emacs\<!--_ループリンク_--\> "wikilink")[Meadow](../Page/Meadow.md "wikilink")とは異なり[プロプライエタリ・ソフトウェア](../Page/プロプライエタリ・ソフトウェア.md "wikilink")であった。プロプライエタリ・ソフトウェアとは、[ソースコード](../Page/ソースコード.md "wikilink")が公開されていないソフトウェアで、プログラムを自由に配布や改変、逆コンパイルをすることができないものを指す用語である。

### GNU Emacs

[Emacs-nw.png](https://ja.wikipedia.org/wiki/File:Emacs-nw.png "fig:Emacs-nw.png")で動く[GNU Emacs](../Page/GNU_Emacs.md "wikilink")\]\]

1984年、リチャード・ストールマンはプロプライエタリ・ソフトウェアであったGosling Emacsのフリーソフトウェアによる代替物を作るべく、GNU Emacsに取り組み始めた。当初GNU EmacsはGosling Emacsをベースとしていたが、ストールマンはMocklisp[インタプリタ](../Page/インタプリタ.md "wikilink")を本物のLISPインタプリタに入れ替えてしまい、ほぼすべてのコードが入れ替わった。GNU Emacsは揺籃期のGNUプロジェクトがリリースした最初のプログラムとなった。GNU EmacsはCで書かれており、Cで実装されたEmacs Lisp (ELisp) を拡張言語として提供する。最初に広く頒布されたGNU Emacsのバージョンは1985年に登場した15.34だった。初期のGNU Emacsのバージョン番号は*1.x.x*のように最初の桁にC coreのバージョンを表すよう採番されていたが、バージョン1.12が出た後にメジャー番号が変わりそうにないため先頭の1をなくすことにしたので、バージョン番号は*1*から*13*にスキップした\[27\]。最初の公開リリースであるバージョン13は1985年[3月](https://ja.wikipedia.org/wiki/3月 "wikilink")に完成した。[2014年](../Page/2014年.md "wikilink")[9月](../Page/9月.md "wikilink")にGNU emacs-develメーリングリストで、GNU Emacsに[ラピッドリリース](https://ja.wikipedia.org/wiki/ラピッドリリース "wikilink")戦略を採用し、将来的にバージョン番号をより迅速に増やしていくことが発表された\[28\]。

GNU Emacsは後にUNIXへ移植され、Gosling Emacsよりも多くの機能を提供した。それらの機能の中で代表的な物は、拡張言語であるフル機能を持ったLISPである。それから瞬く間にGNU EmacsはGosling Emacsに取って代わりUNIXのEmacsエディタのデファクトスタンダードとなった。は彼の1986 cracking spreeで、GNU Emacs電子メールサブシステムのセキュリティ上の弱点を悪用し、UNIXコンピュータ上で[スーパーユーザー](../Page/スーパーユーザー.md "wikilink")アクセス権を取得した\[29\]。

Emacsは、[チューリング完全](../Page/チューリング完全.md "wikilink")な言語を小さい中央コアの頂点で起動する階層型アーキテクチャを使用する。ストックされたEmacs頒布の約3/4（24.4現在では1611k[LOC](https://ja.wikipedia.org/wiki/LOC "wikilink")のうち1266）がElisp拡張言語で書かれており[1](http://www.ohloh.net/p/emacs/analyses/latest/languages_summary)、一度Cによる中核部分（Elispインタプリタを実装し、24.4現在では247kLOCを占める）を移植すればElispコードに実装された機能のセットは存在することになるので、Emacsを新しいプラットフォームに移植することはネイティブコードのみから成る同等のプロジェクトを移植するよりはるかに簡単である。Emacsの移植は理論上中核部のみを新しいプラットフォームへ移植すればよい。このため一度中核部が移植されれば、Cよりも高級な言語で実装された部分は最小限度の作業で済む。

GNU Emacsの開発は*[伽藍とバザール](../Page/伽藍とバザール.md "wikilink")*で*伽藍*式開発の例にあげられていたように、1999年まで比較的閉鎖的だったが、それ以降は公開された開発メーリングリストと匿名[CVSアクセスを採用するようになった](../Page/Concurrent_Versions_System.md "wikilink")。GNU Emacsの開発は2008年までは単一のCVSトランクで行われていたが2009年末より分散型[バージョン管理システム](../Page/バージョン管理システム.md "wikilink")である[Bazaar](https://ja.wikipedia.org/wiki/Bazaar "wikilink")に切り替えられ、さらに2014年11月11日に[Git](../Page/Git.md "wikilink")へと移行した\[30\]。

リチャード・ストールマンは長らくGNU Emacsの主要な管理者を務めていたが、時代と共にその役目から退いていった。2008年から2015年まで管理はStephan MonnierとChong Yidongに引き継がれている\[31\]。2015年にMITにおけるストールマンとの会合の後、John Wiegleyがメンテナとして指名された\[32\]。2014年の時点で、GNU Emacsはその歴史を通じて579人によりコミットされてきた\[33\]。

GNU Emacs のバージョンは 1985年のうちに 17 まであがったが、それ以降は更新は落ち着いた速度で行われている。

### XEmacs

[Xemacs-21.5.b29.png](https://ja.wikipedia.org/wiki/File:Xemacs-21.5.b29.png "fig:Xemacs-21.5.b29.png")上の[XEmacs](https://ja.wikipedia.org/wiki/XEmacs "wikilink") 21.5\]\]

1991年初頭、GNU Emacs 19の初期α版をベースとしてと社の人たちによりLucid Emacsが開発された。コードベースはすぐに2つに分割され、開発チームは単一プログラムとして併合しようとすることをあきらめた\[34\] 。これはフォークしたフリーソフトウェアのうち初期の最も有名な例の1つである。Lucid EmacsはXEmacsと名前を変え、Emacsの中でGNU Emacsに次いで2番目に有名な派生となった。XEmacsの開発は2009年[1月](https://ja.wikipedia.org/wiki/1月 "wikilink")に最新の安定版であるバージョン21.4.22がリリースされてから遅くなっていき、その一方でGNU Emacsは以前はXEmacsにしかなかった機能の多くを実装していった。このため一部のユーザーはXEmacsの死を宣言するようになった\[35\]。

### その他のGNU Emacsのフォーク

XEmacsほど有名ではないGNU Emacsのフォークには以下のものがある:

  - [Meadow](../Page/Meadow.md "wikilink") - [Microsoft Windows用の日本語バージョン](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")\[36\]

  - \- Steve YoungsによるXEmacsのフォーク\[37\]

  - [Aquamacs](../Page/Aquamacs.md "wikilink") - GNU Emacsをベースとし、[Macintosh](../Page/Macintosh.md "wikilink")ユーザインタフェースと統合することに焦点を当てている（Aquamacs 3.2はGNU Emacsバージョン24をベースとし、Aquamacs 3.3はGNU Emacsバージョン25をベースとしている）。

### 様々なEmacsエディタ

[OpenBSD_mg_Editor_Ruby_Goodbye_World.png](https://ja.wikipedia.org/wiki/File:OpenBSD_mg_Editor_Ruby_Goodbye_World.png "fig:OpenBSD_mg_Editor_Ruby_Goodbye_World.png")のソースコードを編集中の、[OpenBSD](../Page/OpenBSD.md "wikilink") 5.3のタイニーEmacs風エディタ**\]\] [Screenshot-Zmacs.png](https://ja.wikipedia.org/wiki/File:Screenshot-Zmacs.png "fig:Screenshot-Zmacs.png")用のEmacsである\]\]

過去においては、各Emacsプロジェクトの目的は肥大化したEmacsの小規模なバージョン作成であった。GNU Emacsは当初、当時のハイエンドであった[32ビット](../Page/32ビット.md "wikilink")フラットアドレス空間と少なくとも1[MiBのRAMを搭載するコンピュータを想定していたが](https://ja.wikipedia.org/wiki/メビバイト "wikilink")、1980年代ではそのようなコンピュータはハイエンドな[ワークステーション](../Page/ワークステーション.md "wikilink")や[ミニコンピュータ](../Page/ミニコンピュータ.md "wikilink")であったので、一般的な[パーソナルコンピュータ](../Page/パーソナルコンピュータ.md "wikilink")のハードウェアで動作するようより小規模に再実装する必要があった。近年では小規模なEmacsクローンはソフトウェアインストールディスクに収まるよう設計されている。

小規模バージョン作成以外のプロジェクトの目的は、ELisp以外のLISP方言やLISPとは全く異なるプログラミング言語によるEmacsの実装である。Emacsクローンを以下に示す。ただし現在その全てが管理されているわけではない:

  - [MicroEMACS](../Page/MicroEMACS.md "wikilink") - Dave Conroyが初めに書き、後にDaniel Lawrenceが開発した、非常に可搬性のある実装である。[リーナス・トーバルズ](../Page/リーナス・トーバルズ.md "wikilink")の使うエディタでもある\[38\]。

  - \- 当初はMicroGNUEmacsといわれていたが後にmg2aといわれるようになった。MicroEMACSのパブリックドメインなフォークでありより密接にGNU Emacsを似ていることを意図された。[OpenBSD](../Page/OpenBSD.md "wikilink")では既定でインストールされる。また、[macOS](https://ja.wikipedia.org/wiki/macOS "wikilink")にプリインストールされていたEmacsは、[2018年](../Page/2018年.md "wikilink")にリリースされた[macOS Mojave (v10.14)の時点でさえ](https://ja.wikipedia.org/wiki/macOS_Mojave "wikilink")11年も前にリリースされたemacs22であったが、[macOS Catalina (v10.15)よりmgに変更されている](https://ja.wikipedia.org/wiki/macOS_Catalina "wikilink")。

  - NotGNU\[39\] - Julie Melbinにより書かれた小さくて高速なプロプライエタリな[フリーウェア](../Page/フリーウェア.md "wikilink")。[MS-DOS](../Page/MS-DOS.md "wikilink")、Win16、Win32、[Linux](../Page/Linux.md "wikilink")版がある。

  - (Jonathan's Own Version of Emacs) - Jonathan Payneによる[Unix系](../Page/Unix系.md "wikilink")システム用の非プログラマブルなEmacs実装である。

  - (MINCE Is Not Complete Emacs) - 製の[CP/M](https://ja.wikipedia.org/wiki/CP/M "wikilink")用のバージョンで後にDOSにも移植された。MINCEはFinal Wordへと進化し、さらにFinal Wordは[ボーランド](../Page/ボーランド.md "wikilink")のとなった。

  - \- [CP/M](https://ja.wikipedia.org/wiki/CP/M "wikilink")実装であり、[Kaypro IIおよびKaypro](https://ja.wikipedia.org/wiki/Kaypro_II "wikilink") IVの最初期のリリースに付属のデフォルトワードプロセッサであるcirca 1982を含んだMINCEが由来。後に[WordStar](../Page/WordStar.md "wikilink")の代替品としてKaypro 10に提供された。

  - \- テキストマクロ拡張ベースの拡張言語を使う[DOS](https://ja.wikipedia.org/wiki/DOS "wikilink")バージョンであり、DOSの64[KiBフラットメモリ限界に収まる](https://ja.wikipedia.org/wiki/キビバイト "wikilink")。

  - [GNU Zile](../Page/GNU_Zile.md "wikilink") - Zileは*<u>Z</u>ile <u>I</u>s [<u>L</u>ossy](../Page/非可逆圧縮.md "wikilink") <u>E</u>macs*の[再帰的頭字語](../Page/再帰的頭字語.md "wikilink")であった\[40\]が、[Lua](../Page/Lua.md "wikilink")で再度書き直されてZile Implements Lua Editorsとして拡張機能を提供する。新しいZileには未だにZemacsと呼ばれるLuaによるEmacs実装が含まれている。Ziと呼ばれるvi実装も含まれる。

  - \- MIT LISPマシンとその子孫用で、ZetaLispで実装されている。

  - \- Zmacsに影響された派生で、[Common Lispで実装されている](../Page/Common_Lisp.md "wikilink")。

  - QEmacs - による、何千MiBものサイズになる巨大なファイルを迅速に編集可能で[UTF-8](../Page/UTF-8.md "wikilink")が使用可能な小規模エディタ\[41\]。

  - \- Lugaru SoftwareによるEmacsクローン。リリースにはDOS、Windows、Linux、[FreeBSD](../Page/FreeBSD.md "wikilink")、[macOS](https://ja.wikipedia.org/wiki/macOS "wikilink")、および[OS/2](https://ja.wikipedia.org/wiki/OS/2 "wikilink")用のバージョンがバンドルされる。EpsilonはCの構文を持つLISPではない拡張言語を使用し、シングルタスクである[MS-DOS](../Page/MS-DOS.md "wikilink")において非常に高速な同時コマンドシェルバッファ実装を使っていた。

  - PceEmacs - 用のEmacsベースエディタ。

  - EmACT - 1986年のChristian JullienによるMicroEmacsのフォーク。EmACTのソースコードは[SourceForgeから利用できる](https://ja.wikipedia.org/wiki/ソースフォージ "wikilink")\[42\]。

  - Amacs - EmacsのApple II ProDOSバージョン。により[6502](../Page/MOS_6502.md "wikilink")[アセンブラで実装された](../Page/アセンブリ言語.md "wikilink")\[43\]\[44\]。

  - \- 元々で書かれていたが、後にCommon Lispとなった。[CMU Common Lispの一部](https://ja.wikipedia.org/wiki/CMU_Common_Lisp "wikilink")。Zmacsに影響された。後に（Helixとして）Lucid Common Lisp、およびプロジェクトによりフォークされた。Hemlockを提供することを狙いとした、Portable Hemlockプロジェクトも存在する。HemlockはいくつかのCommon Lisp実装で動作する。

### Emacsエミュレーションを使うエディタ

  - \- [Haskell](../Page/Haskell.md "wikilink")で書かれHaskellで拡張可能なエディタで、Emacsのエミュレーションモードがある。

  - \- <span style="font-family: monospace, monospace;">jmacs</span>と呼ばれるEmacsキーバインディングをエミュレートする。

  - \- Emacsのエミュレーションモードがある。

  - [Eclipse](../Page/Eclipse_\(統合開発環境\).md "wikilink") - Emacsキーバインディングのセットを提供する。

  - [IntelliJ IDEA](https://ja.wikipedia.org/wiki/IntelliJ_IDEA "wikilink") - Emacsキーバインディングのセットを提供する。

  - \- Emacsエミュレーションをデフォルトとし、viモードをサポートする。

  - \- Emacsと同じ用語を使用し、Emacs操作バインディングを多数理解する。これはネイティブユーザインタフェースが[コントロールキー](../Page/コントロールキー.md "wikilink")の代わりに（Superキーと等価な）[コマンドキー](../Page/コマンドキー.md "wikilink")を使うためである\[45\]。

  - [Sublime Text](https://ja.wikipedia.org/wiki/Sublime_Text "wikilink") - SublemacsPro[プラグイン](../Page/プラグイン.md "wikilink")によりEmacsの振る舞いをいくつか[エミュレートできる](../Page/エミュレータ.md "wikilink")\[46\]。

  - [Visual Studio Emacs Keys](https://github.com/zbrad/emacskeys) - [Visual StudioユーザーにEmacsキーキーバインディングのセットを提供する](https://ja.wikipedia.org/wiki/Microsoft_Visual_Studio "wikilink")。

  - [GNU Readline](https://ja.wikipedia.org/wiki/GNU_Readline "wikilink") - 標準的なEmacs操作のキーバインディングを理解する[ラインエディタ](https://ja.wikipedia.org/wiki/ラインエディタ "wikilink")で、viエミュレーションモードも存在する。

  - \- Emacs用エミュレーションモードを搭載している。

## 機能

Emacsは主に[テキストエディタ](../Page/テキストエディタ.md "wikilink")でありテキスト要素を操作するよう設計されているが、[LaTeX](../Page/LaTeX.md "wikilink")、[Ghostscript](../Page/Ghostscript.md "wikilink")、[ウェブブラウザ](../Page/ウェブブラウザ.md "wikilink")といった外部のプログラムと通信することで、[ワードプロセッサ](../Page/ワードプロセッサ.md "wikilink")のように文書を整形したり印刷することができる。Emacsは[語](../Page/語.md "wikilink")、[文](../Page/文.md "wikilink")、そして[段落](../Page/段落.md "wikilink")といった異なる[セマンティック要素や](../Page/意味論.md "wikilink")、[関数のような](https://ja.wikipedia.org/wiki/サブルーチン#関数 "wikilink")[ソースコード](../Page/ソースコード.md "wikilink")の構成要素を処理したり[様々な色を付けるためのコマンドを提供する](../Page/シンタックスハイライト.md "wikilink")。さらにEmacsは編集コマンドのユーザー定義[バッチ用に](../Page/バッチ処理.md "wikilink")*キーボードマクロ*も提供する。

GNU Emacsは*リアルタイム表示*エディタであるので、編集する度にその編集がオンスクリーンで表示される。これは現在のテキストエディタの標準的振る舞いであるが、EMACSは初期の段階でこの機能を実装していたため、viのように既存のテキストに新しい編集を挿入するために個別のコマンドを実行する必要がなかった。

viが編集のための基本的な機能のみを搭載していたのに対し、Emacsはインクリメンタルサーチ・無制限のアンドゥ・ヤンク（ペースト）用の[スタック](../Page/スタック.md "wikilink")・複数のバッファ・バッファ上でシェルを実行・補完・言語ごとのモードなど、エディタとして考えられる限りの機能を詰め込んでいる。[Vim](../Page/Vim.md "wikilink")ではEmacsと同等のことができるようになっているが、バッファの使い方はEmacsより控えめである。

### 一般的アーキテクチャ

文書への文字列挿入などの基本的な編集操作を含むEmacsの機能はほとんど全て、[LISP](https://ja.wikipedia.org/wiki/LISP "wikilink")の方言で書かれた[関数で行える](../Page/サブルーチン.md "wikilink")。GNU Emacsで使われるLISP方言はEmacs Lisp (ELisp) として知られている。ELisp層はCで書かれた基本的なサービスとプラットフォームを抽象化した概念の、安定したコアの頂点に位置している。LISP環境の[変数と](../Page/変数_\(プログラミング\).md "wikilink")[関数は](../Page/サブルーチン.md "wikilink")、Emacsのリコンパイルや再起動をせずとも一時的に修正できる。

Emacsは追加属性を持つテキストを含んだ*バッファ*と呼ばれる[データ構造](../Page/データ構造.md "wikilink")上で動作する。全てのバッファはその固有の*ポイント*（カーソル位置）と*マーク*（ポイントと併せて、選択された*リージョン*を区切るためのもう1つの位置）、（適用可能な場合）バッファが*訪問*しているファイル名、そして変数で編集や振る舞いを制御する現在の*モード*のセット（正確には1つの「主モード」と複数の「副モード」からなる）を保存している。Elispコードは*コマンド*と名付けられ、インタラクティブに実行できる。コマンドはキープレスにバインドでき、さらに名前でアクセスすることもできる。コマンドの中にはバッファから任意のElispコードを評価するもの（例としては`eval-region`や`eval-buffer`など）もある。

バッファは*ウィンドウ*内に表示される。ウィンドウは端末画面や[GUIウィンドウのタイリングされた部分である](https://ja.wikipedia.org/wiki/グラフィカルユーザインタフェース "wikilink")（その部分はEmacs用語で*フレーム*と呼ばれ、複数のフレームが可能）。特に設定されていない場合、ウィンドウにはスクロールバー、行番号、一番上にある*ヘッダ行*（通常この行にはバッファタイトルやファイル名が表示される）、そして一番下にある*モード行*（通常この行には現在のモードとバッファにおけるポイントの位置のリストが表示される）が含まれる。

同じバッファ上で複数ウィンドウを開くことができるため、例えば1つの長いテキストから異なるパートを見ることができる。さらに複数バッファで同じテキストを共有できるので、例えば言語が混在したファイルで異なる主モードを利用することができる。` M-x  `<mode name>により必要に応じてモードを手動で変更することもできる。

ふつう最下行にある*ミニバッファ*は、Emacsが情報を受け取る場所である。検索対象のテキストや読んだり保存したりするファイルの名前などの情報をミニバッファに入力する。一部の入力ではタブキーを用いて入力を補完することができる。ミニバッファは通常1行しかないが、ここでも通常のバッファと同じ移動・編集コマンドを使うことができる。

### カスタマイズ

  - キーストロークをマクロに記録し、複雑な反復タスクを自動で再現できる。これは使用後に廃棄される各マクロにより[アドホック](../Page/アドホック.md "wikilink")ベースに行われることが多い。ただしマクロを保存したり、後で呼び出すこともできる。
  - 起動時にEmacsは`~/.emacs`と名付けられたEmacs Lispスクリプト（近年のバージョンでは`~/emacs.el`や`~/.emacs.d/init.el`でもよい\[47\]。Emacsは最初に見つけたスクリプトを実行し、それ以外のスクリプトは無視する）を実行する。個人的なカスタマイズファイルは任意の長さや組み合わせでよいが、通常は以下のものが含まれる:
      - Emacsの振る舞いをカスタマイズするための、グローバル変数や関数呼び出しの設定。例としては`(set-default-coding-systems 'utf-8)`など。
      - 標準的な[キーバインディングを上書きしたり](../Page/ショートカットキー.md "wikilink")、ユーザーにとって便利なのにデフォルトでバインドされていないキーを持つコマンド用ショートカットを追加するためのキーバインディング。例 : `(global-set-key (kbd "C-x C-b") 'ibuffer)`
      - Emacsの拡張の読み込み、有効化、および初期化（Emacsには多くの拡張が付属しているが、デフォルトでは極少数しか読み込まれない）。
      - 指定された時間に任意のコードを実行する*イベントフック*の設定。例としてはバッファの保存後に自動でソースコードをリコンパイルする`after-save-hook`など。
      - 任意の複数ファイル実行。通常は長すぎる設定ファイルを管理できるように均等な部分に分割するためのもの（これらの個人的スクリプト用の伝統的な場所は`~/.emacs.d/`と`~/elisp/`である）。
  - 「カスタマイズ」拡張により、ユーザーは`.emacs`に変数を設定するよりもユーザーフレンドリーな方法で、Emacs内部からインタラクティブなカラースキームのような設定プロパティを設定できる。これは検索、説明やヘルプ文、複数選択の入力、デフォルトへのリバート、再起動を必要としない起動中のEmacsインスタンス修正や、他のプログラムにおける好みの機能と類似した他の機能を提供する。カスタマイズされた値は`.emacs`（または他の指定ファイル）に自動で保存される。
  - *テーマ*はフォントや色の選択に影響を与え、elispファイルで定義されカスタマイズ拡張で選択される。

Emacsは、プログラマが単一インターフェースでコードを編集、[コンパイル](https://ja.wikipedia.org/wiki/コンパイル "wikilink")、[デバッグ](../Page/デバッグ.md "wikilink")するような[統合開発環境](../Page/統合開発環境.md "wikilink") (IDE) としても使うことができる。

このような編集機能にとどまらず、Emacs Lispは[TCP/IP通信や外部](../Page/インターネット・プロトコル・スイート.md "wikilink")[プロセス](../Page/プロセス.md "wikilink")の起動などの機能を持っており、テキストエディタとしては一般的でない機能も多くEmacs Lispで記述されている。これらの機能を利用した様々な[アプリケーションソフトウェア](../Page/アプリケーションソフトウェア.md "wikilink")が書かれてきた。Emacsはこれらのアプリケーションソフトウェアを動作させる実行環境となっている。

ライブラリーは、インターネットで見付けることができる。 新しいライブラリーを投稿するための[Usenet](../Page/ネットニュース.md "wikilink")[ニュースグループ](../Page/ニュースグループ.md "wikilink")[gnu.emacs.sources](news://gnu.emacs.sources)まである。一部のライブラリーは、最終的にEmacsに取り込まれて、「標準」ライブラリーとなる。

GNU Emacs 24では、パッケージマネージャが内蔵された。公式のパッケージアーカイブであるGNU ELPA(Emacs Lisp Package Archive)\[48\]のほか、いくつかのアーカイブを扱うことができる。

### 自己文書化

Emacsには最初から各個別のコマンド、変数、内部関数の説明文字列を表示する、強力な*help*ライブラリが付属していた。このため通常の機能や現在の状態の情報をユーザーに提供するので、Emacsは*自己説明的*だと評される。各関数には説明文字列が含まれていて、要求に応じてユーザーに表示される。その後関数に説明文字列をつける習慣は、LISP、[Java](https://ja.wikipedia.org/wiki/Java "wikilink")、[Perl](../Page/Perl.md "wikilink")、および[Python](../Page/Python.md "wikilink")といったさまざまなプログラミング言語に広まった。このヘルプシステムにより、ユーザーは組込みの[ライブラリ](../Page/ライブラリ.md "wikilink")や追加された[サードパーティー](../Page/サードパーティー.md "wikilink")のライブラリのどちらからも各関数用の実際のヘルプコードを取得できる。

Emacsには組み込みの[チュートリアル](https://ja.wikipedia.org/wiki/チュートリアル "wikilink")もある。編集ファイルを指定せずEmacsを起動すると、簡単な編集コマンドの実行方法とチュートリアルを呼出す方法についての説明が表示される。このチュートリアルはStuart Cracraftとリチャード・ストールマンによって作られたものである。

GNU Emacsには組込みの説明文字列のほかにも、リチャード・ストールマンの執筆した*GNU Emacs Manual*の電子コピーがついており、組込みの[Infoブラウザで閲覧することができる](../Page/Texinfo.md "wikilink")。電子版のほかに、3種のマニュアルが[フリーソフトウェア財団](../Page/フリーソフトウェア財団.md "wikilink")から書籍のかたちで刊行されている。

XEmacsの場合、ソフトウェア本体と同時にGNU Emacs Manualからフォークした同様のマニュアルがある他、Bill Lewis、リチャード・ストールマン、Dan Laliberte共著の*Emacs Lisp Reference Manual*、Robert Chassel著の*Programming in Emacs Lisp*も含まれている。

  - [texinfo](https://ja.wikipedia.org/wiki/texinfo "wikilink")はGNU Emacsの標準ドキュメントシステムであり、Emacsのマニュアルはtexinfoでドキュメント化されている。texinfoは[TeX](../Page/TeX.md "wikilink")をベースにしたマークアップ言語を使って記述し、ハイパーテキスト的なブラウジング・検索が可能なオンラインドキュメント[info](https://ja.wikipedia.org/wiki/info "wikilink")として使用することも、TeXを経由して組版されたペーパドキュメントとしても利用することができる。

## 文化

### Emacs教会

[Richard_Stallman_-_Preliminares_2013.jpg](https://ja.wikipedia.org/wiki/File:Richard_Stallman_-_Preliminares_2013.jpg "fig:Richard_Stallman_-_Preliminares_2013.jpg")としてのリチャード・ストールマン\]\] *Emacs教会* () とはEmacsユーザーによって作られたである\[49\]。Emacs教会は[vi](https://ja.wikipedia.org/wiki/vi "wikilink")を「[獣の数字](../Page/獣の数字.md "wikilink")」である（[ローマ数字](../Page/ローマ数字.md "wikilink")ではvi-vi-viは[666](../Page/666.md "wikilink")を表すため）としているが、viのユーザーに反対しているわけではない。むしろ[プロプライエタリ・ソフトウェア](../Page/プロプライエタリ・ソフトウェア.md "wikilink")を[アナテマ](../Page/アナテマ.md "wikilink")と呼んでいる（「viのフリーソフトウェア版を使うことは罪というより苦行である\[50\]」）。このパロディ宗教をサポートするためのEmacs教会の[ニュースグループ](../Page/ニュースグループ.md "wikilink")として<span style="font-family: monospace, monospace;">alt.religion.emacs</span>,\[51\]が存在する。Emacsユーザーの中には「よりよいものを真似る」ことを試みたとして、viの支持者は対抗として*viカルト* () を作成した。

ストールマンは冗談で自身をEmacs教会の聖人 () である[St IGNUciusとしている](https://ja.wikipedia.org/wiki/聖イグヌチウス "wikilink")\[52\]。

### Emacs小指

Emacsの[修飾キー](../Page/修飾キー.md "wikilink")への強い依存がとなるというフォークロアは*Emacs[小指](https://ja.wikipedia.org/wiki/小指 "wikilink")* () と呼ばれる\[53\]。

ユーザーは様々なアプローチでEmacs小指に対処してきた。ソフトウェア側の手段には以下のようなものがある\[54\]:

  - [CapsLockキー](../Page/CapsLockキー.md "wikilink")をコントロールキーの代わりにするようにキーレイアウトをカスタマイズする\[55\]。類似のテクニックにはCapsLockキーを追加のコントロールキーに定義したり、コントロールキーとメタキーを代わりにする。このテクニックもEmacs小指に対して特に推奨されている。
  - Emacsにや組み込みの`type-break-mode`といった、ユーザーに定期的に休息を取らせるようなソフトウェアを入れる。
  - 最初に文字を尋ねてから、カーソルの動きに対応したアクセスキーでその文字が出現するようにする、`ace-jump-mode`\[56\]のようなパッケージや、類似の階層ナビゲーションを提供するelisp拡張を使う。
  - 先進的なVimエミュレーション層の`evil-mode`。
  - Vimのように修飾キーなしでEmacsコマンドを入力するためのモードによるアプローチを提供する`god-mode`。
  - [Spacemacs](https://ja.wikipedia.org/wiki/Spacemacs "wikilink")が提供するカスタマイズされたキーレイアウトの使用。`spacemacs`は制御シーケンス用の主要なキーとして[スペースキー](https://ja.wikipedia.org/wiki/スペースキー "wikilink")を使うプロジェクトであり、`evil-mode`と`god-mode`も二つとも重点的に組み込んでいる\[57\]。
  - キーの組み合わせのキーシーケンスを変えるの使用\[58\]。
  - 基本的なテキスト編集や、さらに進んだ機能のためのEmacsスキーム用にviキーレイアウトを使えるようにする、Emacsの組み込み*`viper-mode`*の使用\[59\]。
  - スペースキーのようなより快適にアクセスできるキーへのもう1つの役割の付与。もう1つの役割を割り当てられたキーは、他のキーと組み合わせて押すことでコントロールキーとして機能する。[エルゴノミクスキーボード](https://ja.wikipedia.org/wiki/エルゴノミクスキーボード "wikilink")や、日本語キーボードのようにスペースキーに隣接するより多くのキーを持つキーボードを使う。日本語キーボードは[メタキー](../Page/メタキー.md "wikilink")や[シフトキー](../Page/シフトキー.md "wikilink")以外の修飾キーの親指操作が可能である\[60\]。
  - 制限されたキーバインディングの人間工学サブセットを使ったり、` M-x  `<command-name>をタイプして他の機能にアクセスする。M-x自体もリバウンドできる。
  - 音声入力によるEmacs操作。
  - Emacsと相互作用せずに毎日のタスクを行うために十分なElispを書く。

ハードウェアによる解決法としては、修飾キーを親指で簡単に操作できる[Kinesis Contoured Keyboardや](https://ja.wikipedia.org/wiki/Kinesis#Kinesis_Contoured_Keyboard "wikilink")、手の平で押せるようキーボードの両側に対称的に手の平で押すことができる巨大な修飾キーを配置したがある\[61\]。フットペダルも利用できる。

Emacsが開発された[スペースカデットキーボード](https://ja.wikipedia.org/wiki/スペースカデットキーボード "wikilink")は、スペースキーに隣接したコントロールキーが巨大で親指が届き易かった\[62\]。

### 用語

英語においてboxenや[VAX](../Page/VAX.md "wikilink")enのように、*emacs*という単語の複数形を*emacsen*と綴ることもある\[63\]。

## 問題点

  - viなどにくらべて起動が遅い。ただし、Emacsは立ちあげっぱなしにしておく使い方をすることが可能であり、長い起動時間は問題にならないという反論もある。
  - Emacsではファイラもオプションの設定画面も通常のエディタ画面と同じ操作が可能であるという特徴があるが、ダイアログボックスなどを使ったGUIに慣れたユーザーにとって、このようなUIはなじみにくい。
  - カスタマイズ可能な機能の数が極端に多く、何を設定したらいいのかわかりづらい。
  - Emacs Lisp により拡張機能が作りやすいため、類似した機能を実現した多数の実装が乱立しやすい。

### 起動の遅さ

EmacsのLispベースの設計の欠点は、Lispコードの読込み、[解釈](../Page/インタプリタ.md "wikilink") に伴う性能への負荷である。 Emacsが最初に実装されたシステムでは大抵、競合するテキストエディタよりかなり遅かった。このことをジョークにした、頭文字による略語がEMACSになる文がいくつか存在する（このようなジョークは他にも存在し、例えばユーザー・インターフェースをネタにした (*Escape Meta Alt Control Shift*) などがある）。

  - *Eight Megabyte And Constantly Swapping*（8MBでちょくちょくスワップ - 8MBのメモリーが広かった時代の話）
  - *Emacs Makes A Computer Slow*（Emacsはコンピュータを遅くする）
  - *Eventually Mallocs All Computer Storage*（結局コンピュータの全記憶装置を[malloc](https://ja.wikipedia.org/wiki/malloc "wikilink")する）
  - *Eventually Makes All Computers Sick*（結局全コンピュータをビョーキにする）

ただし、最近のコンピュータは十分速くなり、以前言われていたほどEmacsを遅いと感じることはめったになくなった。実際、Emacsは最近のワードプロセッサよりも素速く立ち上がる。

さらに、GNU Emacs 23以降はEmacsをサーバープログラムとして立ち上げておく[デーモンモードが追加された](../Page/デーモン_\(ソフトウェア\).md "wikilink")。この場合、Emacs本体はOS起動時に自動的に一度起動するだけなので、速度は問題にならない。

## 関連項目

  -
  - [Conkeror](https://ja.wikipedia.org/wiki/Conkeror "wikilink")

  - [GNU TeXmacs](https://ja.wikipedia.org/wiki/GNU_TeXmacs "wikilink")

  - [テキストエディタの一覧](../Page/テキストエディタの一覧.md "wikilink")

  - [UNIXユーティリティの一覧](https://ja.wikipedia.org/wiki/UNIXユーティリティの一覧 "wikilink")

  - [統合開発環境](../Page/統合開発環境.md "wikilink")

## 注釈

  - [PDF](ftp://publications.ai.mit.edu/ai-publications/pdf/AIM-447.pdf)

  - [PDF](ftp://publications.ai.mit.edu/ai-publications/pdf/AIM-519A.pdf) [HTML](https://www.gnu.org/software/emacs/emacs-paper.html)

  -
  -
  -
  -
  -
  -
  -
## 脚注

## 外部リンク

  -
  - [Reviewed entry](http://directory.fsf.org/wiki/Emacs) in the [Free Software Directory](https://ja.wikipedia.org/wiki/Free_Software_Directory "wikilink").

  - [Wikemacs](http://www.wikemacs.org/index.php)

  - [EmacsWiki](http://www.emacswiki.org/)

  - [EmacsFamily](http://texteditors.org/cgi-bin/wiki.pl?EmacsFamily)

  - [List of Emacs implementations](http://www.finseth.com/emacs.html)

  - [Architectural overview](http://chrismennie.ca/EMACS-Conceptual-Architecture.pdf)

  - [Famous Emacs users](http://wenshanren.org/?p=418)

  - [One of the Oldest Rivalries in Computing: Emacs vs Vi](http://www.slate.com/articles/technology/bitwise/2014/05/oldest_software_rivalry_emacs_and_vi_two_text_editors_used_by_programmers.single.html)

  - [emacs](http://savannah.gnu.org/projects/emacs/) [GNU Savannah](https://ja.wikipedia.org/wiki/GNU_Savannah "wikilink")（サバンナ）

  - [井田昌之](http://www.sociono.net/session-ida/short-bio.html)による[BIT誌上の連載](https://ja.wikipedia.org/wiki/ビット_\(曖昧さ回避\) "wikilink")「Emacs解剖学」（[Internet Archiveのキャッシュ](https://ja.wikipedia.org/wiki/Internet_Archive "wikilink")）

      - [GNUの誕生](https://web.archive.org/web/20041210205259/http://www.sipeb.aoyama.ac.jp/~ida/books/gnu_rms.html)
      - [TecoとEmacs](https://web.archive.org/web/20041210210448/http://www.sipeb.aoyama.ac.jp/~ida/books/teco.html)
      - [Emacsとkeyboard](https://web.archive.org/web/20041125085658/http://www.sipeb.aoyama.ac.jp/~ida/books/emacs-and-keyboard.html)
      - [(続)keyboard](https://web.archive.org/web/20041213185802/http://www.sipeb.aoyama.ac.jp/~ida/books/keyboard2.html)
      - [Gosling Emacs](https://web.archive.org/web/20041211111627/http://www.sipeb.aoyama.ac.jp/~ida/books/gosling.html)
      - [Multics Emacs](https://web.archive.org/web/20041125182250/http://www.sipeb.aoyama.ac.jp/~ida/books/multics-emacs.html)
      - [ソースで遊ぼう](https://web.archive.org/web/20041216123818/http://www.sipeb.aoyama.ac.jp/~ida/books/source.html)
      - [入力の補完](https://web.archive.org/web/20041211105551/http://www.sipeb.aoyama.ac.jp/~ida/books/completion.html)

  - [EmacsWiki](http://www.emacswiki.org/emacs?interface=ja) – Emacsの文書化や議論専用のコミュニティー・サイト

  - [Emacsの実装一覧(Emacs Implementation)](http://www.finseth.com/emacs.html)

[Category:テキストエディタ](https://ja.wikipedia.org/wiki/Category:テキストエディタ "wikilink") [Category:ファイル比較ツール](https://ja.wikipedia.org/wiki/Category:ファイル比較ツール "wikilink") [Category:統合開発環境](https://ja.wikipedia.org/wiki/Category:統合開発環境 "wikilink") [Category:GNUプロジェクト](https://ja.wikipedia.org/wiki/Category:GNUプロジェクト "wikilink") [Category:オープンソースソフトウェア](https://ja.wikipedia.org/wiki/Category:オープンソースソフトウェア "wikilink") [Category:UNIXのソフトウェア](https://ja.wikipedia.org/wiki/Category:UNIXのソフトウェア "wikilink") [Category:1976年のソフトウェア](https://ja.wikipedia.org/wiki/Category:1976年のソフトウェア "wikilink")

1.
2.
3.
4.
5.
6.
7.
8.
9.
10.
11. 他の共同制作者として[リチャード・ストールマン](../Page/リチャード・ストールマン.md "wikilink")がクレジットされることが多いが、は「（TECOベースである）オリジナルのEmacsはガイ・L・スティール・ジュニアとデイビット・ムーンが開発・設計した。彼らがEmacsを動くようにした後で、MIT AI研における標準テキストエディタとして確立されていき、ストールマンがそのメンテナンスを引き継いだ」と記している。ムーン自身は「私が覚えている限り、それは全て真実だ。しかし公正を期して言えば、ストールマンがガイと私からEmacsを『解放した』後、ストールマンがEmacsを大幅に改善したと言わなければならない」と応えた。以下を参照 :
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
24.
25.
26. [RMS Lecture at KTH: Japanese](http://www.gnu.org/philosophy/stallman-kth.ja.html)
27.
28.
29.
30.
31. ; see also ["Stallman on handing over GNU Emacs, its future and the importance of nomenclature"](http://www.networkworld.com/community/node/25360)
32.
33.
34.
35.
36. [FrontPage - Meadow Wiki](http://www.meadowy.org/meadow/pukiwiki-en/)
37.
38. <http://www.stifflog.com/2006/10/16/stiff-asks-great-programmers-answer/>
39.
40.
41.
42.
43.
44.
45.
46.
47.
48. <https://elpa.gnu.org/packages/>
49.
50.
51. [alt.religion.emacs newsgroup](news:alt.religion.emacs)
52. [Saint IGNUcius - Richard Stallman](http://www.stallman.org/saint.html)
53.
54.
55.
56.
57.
58.
59.
60.
61.
62.
63.
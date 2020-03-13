> この記事は[Multics](https://ja.wikipedia.org/wiki/Multics)から翻訳されています。


**Multics**（マルティックス）は[1960年代](../Page/1960年代.md "wikilink")に開発された[タイムシェアリング](../Page/タイムシェアリングシステム.md "wikilink")[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink")であり、後世に多大な影響を与えた。名前は「」に由来している。プロジェクトは1964年に[マサチューセッツ州](../Page/マサチューセッツ州.md "wikilink")ケンブリッジで始まった。最後まで使われていたカナダ国防省のシステムは、2000年10月30日に退役した\[1\]。

## 概要

Multicsの元の計画と開発は[1964年](../Page/1964年.md "wikilink")に、[MIT](../Page/マサチューセッツ工科大学.md "wikilink")（[フェルナンド・J・コルバト](../Page/フェルナンド・J・コルバト.md "wikilink")ら）を中心として、AT\&T[ベル研究所](../Page/ベル研究所.md "wikilink")および[ゼネラル・エレクトリック](../Page/ゼネラル・エレクトリック.md "wikilink") (GE) の独創的な共同プロジェクトとして始まった。しかし1969年にベル研が見切りをつけ脱落（これが結果として[UNIX](../Page/UNIX.md "wikilink")を生んだ）、さらに翌年GEのコンピューター部門が[ハネウェル](../Page/ハネウェル.md "wikilink")にMulticsもろとも買収されている。

MulticsはGEが商品化しようとしており、結果としてハネウェルが商品化したが、あまり成功しなかった。しかし、コンピュータ市場に与えた影響は大きく、様々な斬新で貴重なアイデアが盛り込まれている\[2\]。

高可用性を目指して様々な機能が盛り込まれ、[電話](../Page/電話.md "wikilink")や[電力サービスのような](../Page/電気.md "wikilink")「[コンピュータ・ユーティリティ](../Page/ユーティリティコンピューティング.md "wikilink")」を目標としていた。そのためソフトウェア構造のモジュール化だけでなく、ハードウェアもモジュール化され、必要なリソース(計算機能、主記憶、ディスク装置など)を追加するだけで拡張可能な構造を目指した。ファイル毎の[アクセス制御リスト](../Page/アクセス制御リスト.md "wikilink")によって柔軟な情報共有が可能だが、必要に応じて完全なプライバシーも提供できる。技術者がシステムの性能を分析できる機構も標準で組み込んでいて、様々な性能最適化機構も組み込まれた。

## アイデア

Multicsは[単一レベル記憶](../Page/単一レベル記憶.md "wikilink")と呼ばれるデータアクセス法を実装した。これは、（Multicsではセグメントと呼ばれる）[ファイルと](../Page/ファイル_\(コンピュータ\).md "wikilink")[プロセス](../Page/プロセス.md "wikilink")の[アドレス空間](../Page/アドレス空間.md "wikilink")の明確な区別をなくした考え方である。プロセスのメモリはセグメントをその[アドレス空間](../Page/アドレス空間.md "wikilink")にマップすることで構成される。その読み書きにはプロセスは通常の[CPU](../Page/CPU.md "wikilink")の命令を使い、オペレーティングシステムがその更新内容がディスクに反映されるよう働く。[POSIX](../Page/POSIX.md "wikilink")の用語で言えば、これは全てのファイルが[`mmap`](https://ja.wikipedia.org/wiki/mmap "wikilink")`()`で扱われることと同じである。しかし、MulticsにはUNIXなどにあるようなファイルをマッピングする以外のプロセスのメモリという概念がなかった。「全て」のメモリが何らかのセグメント（ファイル）の一部であり、[ファイルシステム](../Page/ファイルシステム.md "wikilink")に対応する場所が存在する。これはプロセスやカーネルのスタックなどに使われるメモリでも同様である。

この方式の問題点は基本概念の問題ではなく、それが動作していたマシンのアーキテクチャの問題であった。セグメント(ファイル)のサイズが256K×36ビットワード(約1Mバイト)で制限された。従って、それ以上のサイズのファイルを扱うには特別な処理が必要で、これをマルチセグメントファイルと呼んだ。もっとも、巨大なデータベースやグラフィックが使われる以前だったため、この制限にひっかかることはほとんどなかった。

これが[動的リンクを生み出した](https://ja.wikipedia.org/wiki/ライブラリ#動的リンク "wikilink")。動作中のプロセスは新たなセグメントをそのアドレス空間に追加するよう要求でき、そのセグメントにはコードが入っていて実行できる。これにより、アプリケーションは最新版のルーチンを自動的に使用可能となり、各ルーチンは別々のセグメントとなっていて、最初にそのルーチンを呼び出そうとしたときに読み込まれるようになった。異なるユーザーが実行させている異なるプロセスの間では、このようなライブラリセグメントの検索ルールを個別に設定でき、ユーザー毎に異なるバージョンのルーチンを自動的に使用することができた。Multicsのセキュリティ機能を適切に設定すると、あるセグメント内のコードが別のプロセス内のデータ構造にアクセスできるという重要な機能もあった。

従って、[デーモンとして動作しているアプリケーションがあったとき](../Page/デーモン_\(ソフトウェア\).md "wikilink")、別のユーザープロセスが単純に普通の手続き呼び出しを行うと、そのデーモンにアクセスするコードセグメントが動的にリンクされて実行されるといった仕掛けが可能であった。そのようなコードセグメントはデーモンの持つデータ構造を更新することもできる。要求を登録完了したら、制御は元のユーザープロセスのコードに戻される。

Multicsはまた、積極的な[オンライン構成変更をサポートした](../Page/ホットスワップ.md "wikilink")。[CPU](../Page/CPU.md "wikilink")もメモリバンクもディスクドライブもシステム動作中に追加したり削除したりすることが可能だった。MITのシステムではこれが普通に行われていた。ソフトウェアの開発においてマルチプロセッサシステムを二つに論理的に分割し、一方を新たなOSの評価に使用する。このとき、段階的にリソースを削除していって、通常のタイムシェアリングシステムの構成を小さくし、削除したリソースで2台目のシステムを構成する。この間、タイムシェアリングシステムはそのまま動作し続けていた。これは初期の[マルチプロセッサ](https://ja.wikipedia.org/wiki/マルチプロセッサ "wikilink")システムの1つでもあり、今日大型の[サーバ](../Page/サーバ.md "wikilink")などで行われているパーティショニング機能の先駆けでもある。

Multicsは[コンピュータセキュリティ](../Page/コンピュータセキュリティ.md "wikilink")を考慮して設計された最初のオペレーティングシステムの1つである。しかし、初期のMulticsは何度も侵入されている\[3\]。そのためさらなるセキュリティ強化が行われた。第二世代のハードウェアでは[リングプロテクション](../Page/リングプロテクション.md "wikilink")が導入され、侵入はほとんどなくなった。

階層型ファイルシステムを初めて採用しただけでなく\[4\]、ファイル名を任意の長さで自由に設定できるようにもなっている。ファイルやディレクトリは複数の名前を持ち(長い名前と短い名前)、ディレクトリ間のシンボリックリンクもサポートされた。今日では一般的な[カーネル](../Page/カーネル.md "wikilink")内での[プロセス](../Page/プロセス.md "wikilink")毎の[スタック](../Page/スタック.md "wikilink")も初めて採用され、セキュリティリング毎にスタックが分離された。Multicsの主力開発言語は高級言語の[PL/1である](https://ja.wikipedia.org/wiki/PL/I "wikilink")。当時高級言語を用いてOSを記述した例はほとんどなく、それはUNIXの初期の実装がアセンブラ上で行われていたことからも伺える。ただし、[バロース B5000システムはMulticsに先行して](../Page/バロース_B5000.md "wikilink")[ALGOL](../Page/ALGOL.md "wikilink")を使用している\[5\]。

## プロジェクトの経緯

Multicsは当初[GE-645メインフレーム](../Page/GE-600シリーズ.md "wikilink")（[36ビット](https://ja.wikipedia.org/wiki/36ビット "wikilink")システム）上で開発された。後にハネウェル6180シリーズ上で動作している。[UNIX](../Page/UNIX.md "wikilink")初期の歴史についての重要な著作\[6\]がある [Peter H. Salus](https://ja.wikipedia.org/wiki/:en:Peter_H._Salus "wikilink") は、「彼らはMulticsをもっと多用途で柔軟なオペレーティングシステムにしようとしたが、それはみじめに失敗した」と述べている\[7\]。しかしそのような見方は、Multicsでの技術革新の多くが現代の商用システムで採用されている現状から見て的を射ていないとされている\[8\]。

ベル研究所は[1969年](https://ja.wikipedia.org/wiki/1969年 "wikilink")にプロジェクトから撤退した。当時Multicsに関わっていた人々の一部が[UNIX](../Page/UNIX.md "wikilink")システムの開発に移行した。Multicsの開発はMITとGEで続けられた。

1970年、[ハネウェル](../Page/ハネウェル.md "wikilink")はGEのコンピュータ部門を買い取り、[1985年](https://ja.wikipedia.org/wiki/1985年 "wikilink")ごろまでGEの設計に基づいたシステムを開発し続けた。約80ヶ所の大学や研究所や政府機関でMulticsシステムが稼動した。（[Bull](../Page/Bull.md "wikilink")とハネウェルの関係で）フランスの大学で[1980年代](../Page/1980年代.md "wikilink")初期にいくつか導入されている。ハネウェルが Multics のサポートをやめると、ユーザーはUNIXなど他のシステムに移行していった。最後まで使われていたカナダ国防省のシステムは、2000年10月30日に退役した。

1985年、[NSAのNCSC](../Page/アメリカ国家安全保障局.md "wikilink")（国立コンピュータ保安センター）の策定したセキュリティ評価基準 Trusted Computer System Evaluation Criteria（通称[オレンジブック](https://ja.wikipedia.org/wiki/オレンジブック_\(セキュリティ\) "wikilink")）のB2レベルのセキュリティを実装したOSであると認証された。このレベルの認証を受けたのはMulticsが最初である。

[Bull](../Page/Bull.md "wikilink")は1975年から2000年までヨーロッパでMulticsを販売し、Bull HN Information Systems Inc. がアメリカで販売した。2006年、Bull SAS がMulticsのいくつかのバージョンを[オープンソース](../Page/オープンソース.md "wikilink")化した\[9\]。

## 回顧

当時としては巨大と思われたMulticsの[カーネル](../Page/カーネル.md "wikilink")は、135Kバイト以上のコードで構成されていた。MITに最初に設置されたGE-645の主記憶容量は 512Kワードであり(約2Mバイト)、Multicsはその約10分の1を占めていたに過ぎない。

他の方法で測定すると、OS以外のPL/1コンパイラやユーザーコマンドやライブラリを含めた全コードは1500個のソースモジュールから構成されている。各モジュールが約200行と仮定すると、コンパイルによって生成されるコードは約4.5Mバイトとなる。これは2006年現在の感覚では小さいが、当時としては巨大だった。

Multics のコンパイラはCPU性能を引き出すことよりもコードサイズを小さくするよう最適化されていた。例えば、「オペレータ」と呼ばれる小さなサブルーチンを多用している。コードサイズを小さくするという選択は Multics のような主記憶が高価な[マルチユーザー](https://ja.wikipedia.org/wiki/マルチユーザー "wikilink")システムでは良い選択であった。

UNIXに[2038年問題](../Page/2038年問題.md "wikilink")があるが、Multicsには1900年1月1日午前0時からのマイクロ秒を刻む52ビットのカウンタがあり、1971年5月11日にMSBが0から1になった\[10\]。

## Multicsに関する風説

「Multicsは完成せず出荷されなかった」というのが一般通説だが、これは事実ではない。実際にはGE及びハネウェルから商用製品として販売されており、一定の成果を挙げたようである\[11\]。

またUNIXとの対比で常に挙げられるパフォーマンスの悪さは、後に1970年半ばから1980年代に至ってハードウェア性能の向上により実使用への影響は小さくなっている。Multicsは新奇なアイデアを貪欲に取り込んだ当時としては先進的なOSであり、現実解で立ち上がった後に肥大したUNIXとの比較はそれほど簡単ではない。

## 影響

GEの[GECOS](https://ja.wikipedia.org/wiki/GECOS "wikilink")、ハネウェルの[GCOS](../Page/GCOS.md "wikilink")、[日本電気](../Page/日本電気.md "wikilink")の[ACOSは](../Page/Advanced_Comprehensive_Operating_System.md "wikilink")、Multicsの系統といえるOSである。

### UNIX

Multicsプロジェクトで仕事をしていた[ケン・トンプソン](../Page/ケン・トンプソン.md "wikilink")と[デニス・リッチー](../Page/デニス・リッチー.md "wikilink")が最初に開発したUNIXは、コマンドの命名法まで含めた多くの領域でMulticsの影響を示している。例えば、[lsコマンドは](https://ja.wikipedia.org/wiki/ls_\(UNIX\) "wikilink") "list segments" の略であり、Multicsのセグメントを一覧表示するものとして命名された。

最初のUNIXはDECの[PDP-7](../Page/PDP-7.md "wikilink")上で実装された。このPDP-7はメモリが8キロワードしかなく、2メガバイトのメモリを有するGE-645にくらべると極めて貧弱な環境であった。このハードウエアー制約のため、UNIXはMulticsで予定されていた機能の大部分を削り、最小限度のシンプルなものにならざるを得なかった。

当初のUNIXはMulticsのようなマルチタスクオペレーティングシステムではなく、一度に一つのプログラムしか実行できないシングルタスクのオペレーティングシステムであった\[12\]。この特徴から、このOSはカーニハンによって、MulticsのMultiをUniに変えてUnicsと名付けられた\[13\]。後につづりがUNIXへと変更された。

「UNIXはMuticsを否定するものである」あるいは「正反対の設計思想に基づいて作られた」といわれることがあるが、トンプソンやリッチーはそのような発言をしていない。むしろ、「Multicsで得られた利便性を失いたくなかった」と述べており、Multicsを一部でも取り戻そうとしようとしていたことがわかる\[14\]。「正反対の設計思想」にしても、そもそも「設計思想」自体があったとも述べられておらず、UNIXがシンプルなものになったのは、ハードウエアー上の制約に適合した結果に過ぎない。

[ケン・トンプソン](../Page/ケン・トンプソン.md "wikilink")は2007年のインタビューで\[15\]Multicsについて「設計も開発も何もかもが過剰だった。およそ実用的ではなかった。彼ら (MIT) は未だに大きな成功だったと主張しているが、明らかにそうではない」と述べている。しかし同時に「私が（Multicsの中で）十分採用に値すると考えた機能は、階層型ファイルシステムとシェルだ。シェルはプロセスとして独立していて、好きなものと取り替えることができる」と認めている。

### 他のOS

のオペレーティングシステムを、同社の創業者は「靴箱の中のMultics」(Multics in a shoebox) と称した。ポドスカは後に[アポロコンピュータ](../Page/アポロコンピュータ.md "wikilink")を創業し、そこでAEGISと[Domain/OS](https://ja.wikipedia.org/wiki/Domain/OS "wikilink")というオペレーティングシステムを開発したが、それを「マッチ箱の中のMultics」(Multics in a matchbox) と呼んだりした。Domain/OSはMulticsにネットワークとグラフィックス機能を加えたものである。

ストラタスコンピュータ（現[ストラタステクノロジー](https://ja.wikipedia.org/wiki/ストラタステクノロジー "wikilink")）のオペレーティングシステム  はMulticsの強い影響を受けており、ユーザインタフェースも内部構造もよく似ている。Multicsの高信頼性・可用性・セキュリティ機能を強化したもので、高信頼[トランザクション処理](../Page/トランザクション処理.md "wikilink")をサポートする[フォールトトレラントシステム](../Page/フォールトトレラントシステム.md "wikilink")で採用されている。VOSはMulticsの直接の子孫として、今も活発に開発が続けられている。

## 参考文献

Multicsに関しては様々な文献がある。完全なリストは[ここ](http://www.multicians.org/biblio.html)にある。最も重要な文献を以下に挙げる。

  - F. J. Corbató, V. A. Vyssotsky, [*Introduction and Overview of the Multics System*](http://www.multicians.org/fjcc1.html) (AFIPS 1965年) システムに関する良い紹介資料
  - F. J. Corbató, C. T. Clingen, J. H. Saltzer, [*Multics -- The First Seven Years*](http://www.multicians.org/f7y.html) (AFIPS, 1972年) 長年の使用と改良を経た時点での素晴らしいレビュー

### 技術詳細に関する参考文献

  - Jerome H. Saltzer, *[Introduction to Multics](http://www.lcs.mit.edu/publications/specpub.php?id=691)* (MIT Project MAC, 1974年) 実ユーザーによる非常に長いシステム紹介
  - Elliott I. Organick, *The Multics System: An Examination of Its Structure* (MIT Press, 1972年) 初期のバージョンに関する標準的資料。ただしここに記されている機能の一部は結局実装されなかった。
  - V. A. Vyssotsky, F. J. Corbató, R. M. Graham, *[Structure of the Multics Supervisor](http://www.multicians.org/fjcc3.html)* (AFIPS 1965年) Multicsカーネルの基本構造
  - Jerome H. Saltzer, *Traffic Control in a Multiplexed Computer System* (MIT Project MAC, 1966年6月) カーネルスタック切り替えに関する最初の記述; 情報工学の古典的論文
  - R. C. Daley, P. G. Neumann, *[A General Purpose File System for Secondary Storage](http://www.multicians.org/fjcc4.html)* (AFIPS, 1965年) ファイルシステム、アクセス制御、バックアップ機構について
  - R. J. Feiertag, E. I. Organick, *[The Multics Input/Output System](http://www.multicians.org/rjf.html)*. 入出力部の詳細について implementation.
  - A. Bensoussan, C. T. Clingen, R. C. Daley, *[The Multics Virtual Memory: Concepts and Design](http://www.multicians.org/multics-vm.html)*, ([ACM](../Page/Association_for_Computing_Machinery.md "wikilink") SOSP, 1969年) Multicsのメモリ管理の詳細
  - Paul Green, *[Multics Virtual Memory - Tutorial and Reflections](ftp://ftp.stratus.com/pub/vos/multics/pg/mvm.html)* Multicsのストレージシステムについての良い資料
  - Roger R. Schell, *Dynamic Reconfiguration in a Modular Computer System* (MIT Project MAC, 1971年) 構成変更機能について

### セキュリティに関する参考文献

  - Paul A. Karger, Roger R. Schell, *[Multics Security Evaluation: Vulnerability Analysis](http://csrc.nist.gov/publications/history/karg74.pdf)* (Air Force Electronic Systems Division, 1974年) 「タイガーチーム」によるMulticsのセキュリティ破りについて
  - Jerome H. Saltzer, Michael D. Schroeder, *[The Protection of Information in Computer Systems](http://cap-lore.com/CapTheory/ProtInf/)* (Proceedings of the [IEEE](../Page/IEEE.md "wikilink"), 1975年9月) 最初のセキュリティアップグレードの背景となる基本思想について; もう1つの古典的論文
  - M. D. Schroeder, D. D. Clark, J. H. Saltzer, D. H. Wells. *Final Report of the Multics Kernel Design Project* (MIT LCS, 1978年) さらなるセキュリティ強化について
  - Paul A. Karger, Roger R. Schell, *[Thirty Years Later: Lessons from the Multics Security Evaluation](http://www.acsac.org/2002/papers/classic-multics.pdf)* (IBM, 2002年) 数十年前のセキュリティ機能が今日の厳しい環境で役に立つかどうかを考察している。Multicsが2002年の多くの商用システムよりもセキュリティが強いと断定している。

## 脚注

## 関連項目

  - [フェルナンド・J・コルバト](../Page/フェルナンド・J・コルバト.md "wikilink") - MITが関与していた間、Multicsプロジェクトのリーダーを務めた。
  - [ピーター・J・デニング](../Page/ピーター・J・デニング.md "wikilink")
  - [ルイ・プザン](https://ja.wikipedia.org/wiki/ルイ・プザン "wikilink") - Multicsのコマンド言語を「シェル」と名付けた。
  - [J・C・R・リックライダー](../Page/J・C・R・リックライダー.md "wikilink") - [Project MAC](https://ja.wikipedia.org/wiki/Project_MAC "wikilink") の責任者 (1968-1971)
  - [デニス・リッチー](../Page/デニス・リッチー.md "wikilink")

## 外部リンク

  - [Multicians.org](http://www.multicians.org/) に様々なデータがある
      - [Multics papers online](http://www.multicians.org/papers.html)
      - [Multics glossary](http://www.multicians.org/mga.html)
      - [Myths](http://www.multicians.org/myths.html) Multicsに関するいくつかの風説の詳細。「失敗した」「巨大で遅かった」などなど。一部誤解もある。
      - [Multics security](http://www.multicians.org/security.html)
      - [Unix and Multics](http://www.multicians.org/unix.html)
      - [Multics general info and FAQ](http://www.multicians.org/general.html) Multicsの影響を受けたシステムについての包括的概要がある。
  - [Multics repository](http://www.mit.edu:8001/afs/net/user/srz/www/multics.html)
  - [Multics repository at Stratus Computer](ftp://ftp.stratus.com/pub/vos/multics/multics.html)
  - [Multics at Universitaet Mainz](http://www.vaxman.de/historic_computers/multics/multics.html)
  - [Official source code archive at MIT](http://web.mit.edu/multics-history/)
  - [Active project to emulate the Honeywell 6180 Multics CPU](http://sourceforge.net/projects/h6180/)
  - [Various scanned Multics manuals](http://bitsavers.org/pdf/honeywell/multics/)
  - [Multicians.org and the History of Operating Systems](http://www.cbi.umn.edu/iterations/haigh.html)

[Category:フリーソフトウェアOS](https://ja.wikipedia.org/wiki/Category:フリーソフトウェアOS "wikilink") [Category:1969年のソフトウェア](https://ja.wikipedia.org/wiki/Category:1969年のソフトウェア "wikilink")

1.  [Multics History](http://www.multicians.org/history.html)
2.  [Myths about Multics](http://www.multicians.org/myths.html)
3.
4.  [Multicians Glossary: File system](http://www.multicians.org/mgf.html#filesystem)
5.  [The Multics PL/1 Compiler](http://www.multicians.org/pl1-raf.html) R. A. Freiburghouse, General Electric Company, Cambridge, Massachusetts, 1969.
6.
7.
8.
9.  [Multics history](http://stuff.mit.edu/afs/athena/reference/multics-history/) MIT
10. [unix time](http://parametron.blogspot.com/2011/05/unix-time.html)
11.
12.
13.
14.
15. Peter Seibel. Coders at Work: Reflections on the Craft of Programming. APress Publications, 2007. ISBN 978-1-4302-1948-4
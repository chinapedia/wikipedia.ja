> この記事は[BPEL](https://ja.wikipedia.org/wiki/BPEL)から翻訳されています。


**BPEL**（）とは、実行可能な[ビジネスプロセスモデリング](https://ja.wikipedia.org/wiki/ビジネスプロセスモデリング "wikilink")言語である。しかし、BPELは特定のセマンティックやプロセス構造の要素を持っていないため、考えられるすべてのビジネスプロセスをモデル化し実行することは不可能である。このため、BPEL はたとえば Java のようなプログラミング言語とともに用いられたり、ワークフロー統合ブローカーエンジンなどの商用製品に備わっている独自のスクリプト言語によって拡張されることが多い。

BPEL の起源は [WSFL](https://ja.wikipedia.org/wiki/Web_Services_Flow_Language "wikilink") と [XLANGにさかのぼることができる](https://ja.wikipedia.org/wiki/Xlang "wikilink")。BPEL は [XML](../Page/Extensible_Markup_Language.md "wikilink") によってシリアライズ可能で、*[大規模プログラミング](https://ja.wikipedia.org/wiki/大規模プログラミング "wikilink")*の概念を実現するものである。大規模プログラミングと*[小規模プログラミング](https://ja.wikipedia.org/wiki/小規模プログラミング "wikilink")*の概念は、[ビジネスプロセス](../Page/ビジネスプロセス.md "wikilink")で典型的に見ることができる長時間継続する非同期のプロセスを記述する際の二つの側面によって分類することができる。

BPEL が [IBM](../Page/IBM.md "wikilink") とマイクロソフトによって開発されたのは、BPMI.org が開発した初期の言語[BPML](https://ja.wikipedia.org/wiki/BPML "wikilink")に対抗するためであった。この背景については幾つかの議論があるが、おそらく、さまざまなグループで詳細について合意できない性格によるものと思われる。[ワークフロー](../Page/ワークフロー.md "wikilink")理論が先祖である BPEL とは異なり、BPML は[Pi calculusから着想された](https://ja.wikipedia.org/wiki/Pi_calculus "wikilink")。このため、BPML は完全で定式化された文法を持つことになり、市場には強力なBPMLの製品が登場することとなった。このため、アプリケーションサーバ開発を統一する標準に対して統制力を持ちたいと考えていた IBM とマイクロソフトは懸念を持った。

今日では、過去の BPEL と BPML との違いはほぼ学術的なものになっている。BPEL の文法が勝利を収め、BPML の意味論が勝利を収めた。IBM とマイクロソフトの力により、今日 BPEL の名前が残っている。BPEL は徐々にBPML へと近づく方向に進化している。BPML が形式上完全であるため、これは不可避である。

## 目的

**大規模プログラミング**は、抽象度の高いプロセスのことであり、BPELではこのようなプロセスを抽象プロセスと呼んでいる。BPELの抽象プロセスは、規格化された方法で表現された振る舞いを表している。抽象プロセスは、メッセージを待つ、メッセージを送信する、失敗したトランザクションの補償をするなどの処理が記述されている。それとは対照的に、**小規模プログラミング**は、1つのトランザクションで終わるような、生存期間の短い振る舞いを扱う。**小規模プログラミング**と**大規模プログラミング**では異なった言語が必要であるという発想からBPELは生まれた。

## BPELの設計目標

BPELにはもともと10の設計目標があった:

1.  外部の実体に対して[WSDL](https://ja.wikipedia.org/wiki/WSDL "wikilink") 1.1を用いて定義された[Webサービス](../Page/Webサービス.md "wikilink")の操作を介してやりとりし、自身を WSDL 1.1を用いて定義された Webサービスとして宣言するビジネスプロセスを定義すること。やりとりは、portType の定義に依存しポートの定義には依存しないという意味で "抽象的" であること。
2.  XMLに基づいた言語によりビジネスプロセスを定義すること。プロセスのグラフィカルな表現方法を定義したり、プロセスのための特定の設計手法を提供したするものでないこと。
3.  ビジネスプロセスの外部（抽象的）および内部（実行可能）ビューの両方で用いるための、Webサービスを組織化の概念を定義すること。そのようなビジネスプロセスは、ひとつの自律的な存在の振る舞いを定義し、技術的には似たような相手と総合作用を行う。それぞれの使い方のパターン（すなわち抽象ビューと実行可能ビュー）はいくつかの専門化された拡張を必要とするが、これらの拡張は最小限に保たれ、import/exportや、二つの使い方のパターンを結ぶリンクが仕様に準拠する、などの要求に対してテストされていなければならない。
4.  階層的な、またグラフ的な制御の方式を提供し、両方の使い方を可能な限りシームレスに融合させること。これによりプロセスモデリング空間の分断を減少させる。
5.  プロセスのデータや制御フローを定義するために必要な、単純なデータ操作の機能をサポートする。
6.  インスタンス識別子の定義をアプリケーションレベルのメッセージレベルで許可するプロセスインスタンスの識別メカニズムをサポートする。インスタンスの識別子パートナーによって定義され、変更される可能性がある。
7.  暗黙的なプロセスインスタンスの生成と消滅を基本的なライフサイクル機構としてサポートする。"suspend"や"resume"のような高度なライフサイクル操作はライフサイクル管理のための将来のリリースで追加される可能性がある。
8.  弁済のアクションや、長期にわたって有効なビジネスプロセスの一部のためのエラー回復機能をサポートするため問題判定 (scoping) のような、証明された技術に基づいた、長期にわたって有効なトランザクションモデルを定義する。
9.  Webサービスをプロセスの分解と結合のモデルとして用いる。
10. Webサービスの標準（認証され提案されたもの）の上に、可能な限り組み立て可能な方法で構築される。

## BPEL言語

BPELは[オーケストレーション言語であり](../Page/オーケストレーション_\(コンピュータ\).md "wikilink")、コレオグラフィ\[1\]言語ではない（[:en:Web Service Choreography参照](https://ja.wikipedia.org/wiki/:en:Web_Service_Choreography "wikilink")）。オーケストレーションとコレオグラフィの主な違いはその範囲である。コレオグラフィモデルがある参加者からのビュー（たとえばピアツーピアモデル）に焦点を置いているが、オーケストレーションモデルはすべての関係者と関連したやりとりを含み、システムの全体的なビューを与える。オーケストレーションとコレオグラフィの区別は次のようにたとえられる：オーケストレーションが、オーケストラの指揮者のような集中管理の振る舞いを記述し、コレオグラフィーは振り付けされた (choreographed) ダンスで、ダンサーが互いのペアの振る舞いに反応するように、それぞれの参加者が外部のイベントに基づいた処理を実行する、分散制御の振る舞いを記述する。

BPELの現代的な[ビジネスプロセス](../Page/ビジネスプロセス.md "wikilink")に対する焦点、さらに[WSFL](https://ja.wikipedia.org/wiki/WSFL "wikilink")および[XLANG](https://ja.wikipedia.org/wiki/XLANG "wikilink")の歴史から、BPELは[Webサービス](../Page/Webサービス.md "wikilink")を外部の通信メカニズムとして採用することになった。 そのため、BPEL のメッセージング能力は、入出力される[メッセージ](../Page/メッセージ.md "wikilink")を記述するための[WSDL](../Page/Web_Services_Description_Language.md "wikilink")1.1の使い方に依存する。

メッセージの送信受信を行える能力を提供することに加えて、BPELプログラミング言語は下記の項目をサポートする：

  - プロパティに基づくメッセージ間関連機構
  - XML および WSDL の型に基づく変数
  - 表現や問い合わせを複数の言語で書くことができるようにするための、拡張可能な言語プラグインモデル：BPELは[XPath](../Page/XML_Path_Language.md "wikilink")1.0をデフォルトでサポートしている
  - 連接\[2\]、分岐\[3\]、反復\[4\]、並列\[5\]を含む[構造化プログラミング](../Page/構造化プログラミング.md "wikilink")要素
  - [ローカル変数](../Page/ローカル変数.md "wikilink")、障害[ハンドラー](https://ja.wikipedia.org/wiki/ハンドラー "wikilink")、補償ハンドラー、[イベントハンドラー](https://ja.wikipedia.org/wiki/イベントハンドラー "wikilink")を用いたロジックのカプセル化を可能とするスコープシステム
  - [変数への並行的なアクセスを制限するためのシリアライズされたスコープ](../Page/変数_\(プログラミング\).md "wikilink")

## WS-BPEL 2.0 での変更点

  - 新しいアクティビティの型: repeatUntil, validate, forEach（並列、直列）, rethrow, extensionActivity, compensateScope
  - 名称の変更されたアクティビティ: switch/case は if/else に、terminate は exitに改名された
  - ターミネーションハンドラーが、明示的な終了のアクティビティに適用するために追加された
  - 変数の初期化
  - 変数変換のための XSLT（新しい XPath 拡張関数 bpws:doXslTransform）
  - 変数のデータへの XPath アクセス（XPath 変数の文法 $variable\[.part\]/location）
  - Webサービスアクティビティにおける XML スキーマ変数 (WS-I doc/lit スタイルサービス用)
  - ローカルに定義された messageExchange (受信アクティビティと返信アクティビティの内部的な対応)
  - 抽象プロセスの明文化(文法および意味)
  - それぞれのアクティビティにおいて記述言語の変更を可能にした

## BPEL への '小規模プログラミング' のサポートの追加

BPEL の分岐や反復などの制御構造や、変数操作の機能は、ロジックを提供するための'小規模プログラミング'言語を使うことに依存している。すべての BPEL 実装は[XPath](../Page/XML_Path_Language.md "wikilink") 1.0 をデフォルトの言語としてサポートしなければならないが、BPEL の設計はシステム構築者が異なる言語も使用できるよう考える必要がある。 [BPELJ](http://ftpna2.bea.com/pub/downloads/ws-bpelj.pdf) は、Java が BPEL 内の'小規模プログラミング'として機能できるようにするための[JSR 207](http://www.jcp.org/en/jsr/detail?id=207) に関連した試みである。

## 歴史

[IBM](../Page/IBM.md "wikilink") とマイクロソフトは、それぞれが定義したかなりよく似た'大規模プログラミング'言語[WSFL](https://ja.wikipedia.org/wiki/Web_Services_Flow_Language "wikilink") と [XLANGを持っていた](https://ja.wikipedia.org/wiki/Xlang "wikilink")。BPMLの評判と、登場、BPMI.org の成功、[Intalio](https://ja.wikipedia.org/wiki/Intalio "wikilink") Inc. にリードされたオープンな BMPS への推進活動 により、IBM とマイクロソフトは互いの言語をひとつの新しい言語 BPEL4WS に統合することを決定した。 2003年4月、[BEAシステムズ](../Page/BEAシステムズ.md "wikilink")、IBM、マイクロソフト、[SAP](../Page/SAP_\(企業\).md "wikilink")、[Siebel Systems](https://ja.wikipedia.org/wiki/Siebel_Systems "wikilink") は、[Web Services BPEL Technical Committee](http://www.oasis-open.org/committees/tc_home.php?wg_abbrev=wsbpel)を介して [OASIS](https://ja.wikipedia.org/wiki/OASIS_\(organization\) "wikilink") に BPEL4WS 1.1 を提出した。 [BPEL4WS](https://ja.wikipedia.org/wiki/BPEL4WS "wikilink")は 1.0 と 1.1 の両方のバージョンで登場したが、OASIS WS-BPEL 技術委員会[1](http://www.choreology.com/external/WS_BPEL_issues_list.html#Issue98) は [2004年](../Page/2004年.md "wikilink")[9月14日](../Page/9月14日.md "wikilink") に、その仕様を [WS-BPEL](https://ja.wikipedia.org/wiki/WS-BPEL "wikilink") 2.0 と呼ぶことを投票により決定した。この名称の変更は、BPEL を、WS-で始まる他の Webサービス標準の命名規則にあわせ、**BPEL4WS** 1.1 と **WS-BPEL** 2.0 との間の大幅な仕様の強化を表すために行われた。ただし特定のバージョンについて議論していなければ、**BPEL**だけで十分である。

2007年6月、Active Endpoints、[アドビシステムズ](../Page/アドビシステムズ.md "wikilink")、BEAシステムズ、IBM、[オラクル](https://ja.wikipedia.org/wiki/オラクル_\(企業\) "wikilink")、SAP は[BPEL4People](https://ja.wikipedia.org/wiki/BPEL4People "wikilink") および WS-HumanTask 仕様をリリースした。これは、BPEL プロセスにおいて人間の活動をどのように取り込むか記述するものである。

BPEL の開発の方向については徐々に論争が巻き起こってきている。WS-HumanTask の形態で BPEL にセマンティックを追加するなどの要求は、BPEL が完全な言語でないという事実を強調するのみである。逆に、実用的なアプリケーションでは、ほぼ常に、ほかのプログラミングツールで言語を拡張する必要がある。完全な言語である BPML では、BPEL を拡張する際必要なように XML に新しいタグを追加するのではなく、新しい[セマンティクス](https://ja.wikipedia.org/wiki/セマンティクス "wikilink")をプロセスとして実現することができる。そのため、いわゆる BPEL準拠の製品を使う際には、ベンダーが主張するのがどのバージョンの BPEL であるのかに非常な注意が必要である。BPEL準拠の製品は、BPELだけでは、必ずしもひとつのビジネスプロセスすら実現できない。これが意味するところは、現場でのみ明らかになる。たとえて言うなら、演算子がないために完全なコードを書けないプログラム言語を持っているようなものである。

## BPEL の BPMN との関係

OASIS技術委員会がスコープ外としたため、WS-BPELのためのグラフィカルな記法に標準はない。いくつかのベンダーはそれぞれのグラフィカルな記法を生み出している。これらの記法はほとんどの BPEL 要素がブロック構造である（たとえば sequence, while, pick, scopeなど）であることを利用している。この機能により、BPEL記述を 昔の [Nassi-Shneiderman diagram](https://ja.wikipedia.org/wiki/Nassi-Shneiderman_diagram "wikilink") における *structograms* を思い起こすような形態で直接ビジュアルに表現することができる。

まったく異なる[ビジネスプロセスモデリング](https://ja.wikipedia.org/wiki/ビジネスプロセスモデリング "wikilink")言語、[Business Process Modeling Notation](https://ja.wikipedia.org/wiki/Business_Process_Modeling_Notation "wikilink") ([BPMN](https://ja.wikipedia.org/wiki/BPMN "wikilink")) を、BPELプロセス記述を表現するグラフィカルなフロントエンドとして用いることを提案している者もいる。この方法の実現性を示すものとして、BPMN仕様には非公式で部分的ではあるがBPMN から BPEL 1.1 への [マッピング](http://www.bpmn.org/Documents/Mapping%20BPMN%20to%20BPEL%20Example.pdf)が含まれている。

BPMNからBPELへのより詳細なマッピングは、[BPMN2BPEL](http://www.bpm.fit.qut.edu.au/projects/babel/tools/)などオープンソースのものを含む複数のツールにより実現されている。しかし、これらのツールの開発により BPMN と BPEL の間の根本的な違いが明らかになり、BPMNモデルから人間が理解できる BPEL コードを生成するのは非常に困難、場合によってはまったく不可能であることがわかった。さらに困難なのは、BPMN と BPEL の間の*ラウンドトリップ*技術、つまり片方に加えた変更がもう片方に反映されるように、BPMNの図からBPELコードを生成し、オリジナルのBPMNモデルを維持しつつ、生成された BPEL コードを同期させることである。

## 脚注

<references/>

## 関連項目

  - [プロセスモデル](../Page/プロセスモデル.md "wikilink")
  - [XML Process Definition Language](../Page/XML_Process_Definition_Language.md "wikilink")（XPDL）
  - [YAWL](../Page/YAWL.md "wikilink")
  - [BPEL4People](https://ja.wikipedia.org/wiki/BPEL4People "wikilink")
  - [Business Process Management](https://ja.wikipedia.org/wiki/Business_Process_Management "wikilink")
  - [Business Process Modeling Notation](https://ja.wikipedia.org/wiki/Business_Process_Modeling_Notation "wikilink")
  - [Web Services Conversation Language](https://ja.wikipedia.org/wiki/WSCL "wikilink")
  - [WS-CDL](https://ja.wikipedia.org/wiki/Web_Services_Choreography_Description_Language "wikilink") [2](http://www.w3.org/TR/ws-cdl-10/)
  - [Workflow](https://ja.wikipedia.org/wiki/Workflow "wikilink")

## 外部リンク

### 標準規格

  - [WS-BPEL 2.0 specification (OASIS standard)](http://docs.oasis-open.org/wsbpel/2.0/wsbpel-v2.0.pdf)
  - [OASIS WSBPEL TC Webpage](http://www.oasis-open.org/committees/tc_home.php?wg_abbrev=wsbpel)
  - [OASIS WSBPEL TC Issues List](http://www.choreology.com/external/WS_BPEL_issues_list.html)
  - [Latest editor's copies of OASIS WSBPEL TC Specs](http://wsbpeltc.cvs.sourceforge.net/wsbpeltc/specifications/)
  - [The BPEL4WS 1.1 specification](http://www-128.ibm.com/developerworks/library/specification/ws-bpel/)

### BPEL およびビジネスプロセスのサイト

  - [The Eclipse STP BPMN Diagram Editor](http://www.eclipse.org/stp/bpmn/)
  - [Orchestra, Open source BPEL Engine, designer, admin and real time monitoring tool](http://orchestra.objectweb.org/)
  - [ActiveBPEL, Open source BPEL server and BPEL samples](http://www.activebpel.org/)
  - [Business Process Management Initiative Web Site](http://www.bpmi.org/)
  - [Business Modeling Forum](http://www.BusinessModelingForum.com)
  - [BPEL Resource Guide](http://www.bpelsource.com/bpel_info/defined.html)
  - [Service Interaction Patterns (with BPEL code samples)](http://www.serviceinteraction.com)
  - [Service Interaction Patterns (with BPMN diagrams that match BPEL code samples)](http://www.eclarus.com/bpel_bpmn_examples.html)
  - [The Open Source BPMS (Eclipse and Apache-based)](http://www.intalio.com)
  - [Apache ODE, Open source BPEL server](http://ode.apache.org/)
  - [NetBeans Enterprise Pack](http://www.netbeans.org/products/enterprise/)
  - [BPEL for Windows Workflow Foundation](http://www.microsoft.com/downloads/details.aspx?FamilyID=6D0DAF00-F689-4E61-88E6-CBE6F668E6A3&displaylang=en)

### BPEL 関連の記事

  - [BPEL BluePrints: Web Services Orchestration Using BPEL - presented by the Java BluePrints Solutions Catalog](http://blueprints.dev.java.net/bpcatalog/ee5/soa/)
  - ["SOA Best Practices: The BPEL Cookbook" - BPEL howto's from Oracle](http://www.oracle.com/technology/pub/articles/bpel_cookbook/index.html)
  - ["Pattern-based Evaluation of Oracle BPEL"](http://is.tm.tue.nl/research/patterns/download/Oracle_BPEL_v.10.1.2.pdf)
  - ["What is BPEL and Why is it so important to my business?" - BPEL Primer from SoftCare](http://www.softcare.com/whitepapers/wp_whatis_bpel.php)
  - [Description of the upcoming changes from BPEL 1.1 to BPEL 2.0](http://webservices.sys-con.com/read/155617.htm)
  - [Oracle Article: Weaving Web Services Together](http://www.oracle.com/technology/oramag/oracle/04-jul/o44dev_web.html)
  - [BPEL for Programmers and Architects](http://www.bptrends.com/publicationfiles/BPEL4ProgArchies.pdf) *(slides)*
  - [The Promise of Portable Business Processes](http://ftpna2.bea.com/pub/downloads/BPEL4WS_WSJ.PDF)
  - [BPEL and Java](http://www.theserverside.com/tt/articles/article.tss?l=BPELJava)
  - [Process-centric realization of SOA: BPEL moves into the limelight](http://webservices.sys-con.com/read/46870.htm?CFID=131177&CFTOKEN=141F4729-FFA1-12C2-68DED6CB7C6E5134)
  - [Validating BPEL Specifications using OCL](http://www.cs.kent.ac.uk/pubs/2004/2027/content.pdf)
  - [IBM Article: Business Process Choreography in WebSphere: Combining the Power of BPEL and J2EE](http://www.research.ibm.com/journal/sj/432/kloppmann.html)
  - [BPEL Primer](http://web.archive.org/20051224043316/elementallinks.typepad.com/bmichelson/2005/09/view_bpel_proce.html)
  - [WS-BPEL Extension for Sub-processes, BPEL-SPE](http://www.sdn.sap.com/irj/servlet/prt/portal/prtroot/docs/library/uuid/5cbf3ac6-0601-0010-25ae-ccb3dba1ef47)
  - [Analysis of Web Services Composition Languages: The Case of BPEL4WS](http://eprints.qut.edu.au/archive/00001776)
  - [BPEL Begone - How useful is this Standard?](http://blog.whatfettle.com/2007/01/13/bpel-begone/)
  - [Pattern-based Evaluation of IBM WebSphere BPEL](ftp://ftp.informatik.uni-stuttgart.de/pub/library/medoc.ustuttgart_fi/STUD-2052/STUD-2052.pdf)
  - [A Close Look at BPEL 2.0 @ SYS-CON Media](http://www.sys-con.com/read/434430.htm)
  - [BPEL in SCA assembly model](http://khanderaotech.blogspot.com/2007/02/bpel-in-sca-assembly-model.html)

[Category:XML-based_standards](https://ja.wikipedia.org/wiki/Category:XML-based_standards "wikilink") [Category:Specification_languages](https://ja.wikipedia.org/wiki/Category:Specification_languages "wikilink") [Category:Web_service_specifications](https://ja.wikipedia.org/wiki/Category:Web_service_specifications "wikilink") [Category:Workflow_technology](https://ja.wikipedia.org/wiki/Category:Workflow_technology "wikilink") [Category:Process_management](https://ja.wikipedia.org/wiki/Category:Process_management "wikilink") [Category:XMLベースの技術](https://ja.wikipedia.org/wiki/Category:XMLベースの技術 "wikilink") [Category:ソフトウェア工学](https://ja.wikipedia.org/wiki/Category:ソフトウェア工学 "wikilink") [Category:ビジネスソフト](https://ja.wikipedia.org/wiki/Category:ビジネスソフト "wikilink")

1.
2.
3.  `if`-`then`-`elseif`-`else`
4.  `while`
5.  、コマンドを並列に実行する。
> この記事は[XML Process Definition Language](https://ja.wikipedia.org/wiki/XML_Process_Definition_Language)から翻訳されています。


**[XML](../Page/Extensible_Markup_Language.md "wikilink") Process Definition Language**（**XPDL**）とは、[ワークフロー](https://ja.wikipedia.org/wiki/ワークフロー "wikilink")製品間（モデリングエンジンやワークフローエンジン）で[ビジネスプロセス](https://ja.wikipedia.org/wiki/ビジネスプロセス "wikilink")定義を交換するために定義された標準形式であり、Workflow Management Coalition (WfMC) が策定した。XPDL はワークフローの宣言部を記述するためのXMLスキーマを定義している。

XPDL はビジネスプロセスのワークフローを視覚的にも意味的にも定式化して交換するために設計された。XPDL には、活動ノードの2次元座標やノード間の接続のための線の座標といった情報を含んでいる。XPDL がこのような図としての情報を持つ点が類似の形式である [BPEL](https://ja.wikipedia.org/wiki/BPEL "wikilink") と大きく異なる点である。BPEL はむしろプロセスの実行的側面に注目した形式であり、ワークフローを図示することは考慮していない。

## 歴史

1993年8月、Workflow Management Coalition (WfMC) が設立され、Workflow Reference Model の定義を開始した（1995年発表）。これは、ワークフロー管理システムが持つべき5つのインタフェースの概要を示したものである。インタフェース 1 はビジネスプロセスの定義のためのインタフェースで、2つの部分からなる。プロセス定義言語とプロセス定義をワークフロー管理システムとやり取りするためのプログラム的なインタフェースである。

最初のプロセス定義言語は Workflow Process Definition Language (WPDL) と呼ばれ、1998年に発表された。このプロセスメタモデルには、URLエンコーディングも含めたワークフロー自動化に必要なあらゆる概念が含まれている。相互運用デモも行われ、プロセスモデルの交換の利便性が示された。

1998年、最初の標準をXMLベースにしたものが登場した。交換言語のベースとしてXMLの文法を使ったユーティリティである。WfMC Working Group 1 は XML Process Definition Language (XPDL) 1.0 を作成した。この第二版は WPDL と同じコンセプトを保ちつつ XML ベースになっており、一部改良もなされている。XPDL 1.0 は 2002年に WfMC の承認を受け、多くのワークフロー製品や[BPM製品で採用された](../Page/ビジネスプロセス管理.md "wikilink")。XPDL を中心としたワークフローに関する研究も盛んに行われている。特に XPDL 1.0 が登場した時点ではプロセスモデル交換の標準と言える言語は XPDL しかなかったのである。

WfMC はその後もプロセス定義（交換）言語の改良と更新を続けた。2004年、WfMC は [BPMN](https://ja.wikipedia.org/wiki/BPMN "wikilink") を承認した。これはプロセス定義の視覚的表現の標準である。XPDL は BPMN が表現できる図を XML 上で全て記述することを目標として拡張された。第三版は [XPDL 2.0](http://www.wfmc.org/standards/XPDL.htm) として2005年10月に WfMC の承認を受けた。

## 参考文献

  - Wil M.P. van der Aalst, "Business Process Management Demystified: A Tutorial on Models, Systems and Standards for Workflow Management", Springer Lecture Notes in Computer Science, Vol 3098/2004.

  - Wil M.P. van der Aalst, "Patterns and XPDL: A Critical Evaluation of the XML Process Definition Language", Eindhoven University of Technology, [pdf file](http://is.tm.tue.nl/research/patterns/download/ce-xpdl.pdf)

  - Jiang Ping, Q. Mair, J. Newman, "Using UML to design distributed collaborative workflows: from UML to XPDL", Twelfth IEEE International Workshops on Enabling Technologies: Infrastructure for Collaborative Enterprises, 2003. WET ICE 2003. Proceedings. ISBN 0-7695-1963-6

  - W.M.P. van der Aalst, "Don’t go with the flow: Web services composition standards exposed", IEEE Intelligent Systems, Jan/Feb 2003

  - Jürgen Jung, "Mapping Business Process Models to Workflow Schemata An Example Using Memo-ORGML And XPDL", Universität Koblenz-Landau, April 2004, [PDF](http://www.wi-inf.uni-duisburg-essen.de/FGFrank/documents/Arbeitsberichte_Koblenz/Nr47.pdf)

  - Volker Gruhn, Ralf Laue, ["Using Timed Model Checking for Verifying Workflows"](http://ebus.informatik.uni-leipzig.de/papers/paperuploads/Using_Timed_Model_Checking_for_Verifying_WorkflowsVolker_Gruhn__Ralf_Laue7538.pdf), Jose Cordeiro and Joaquim Filipe (Ed.): Proceedings of the 2nd Workshop on [Computer Supported Activity Coordination, Miami](http://www.informatik.uni-trier.de/~ley/db/conf/csac/csac2005.html), USA, 23.05.2005 - 24.05.2005, 75-88. Insticc Press ISBN 972-8865-26-0

  - Nicolas Guelfi, Amel Mammar, "A formal framework to generate XPDL specifications from UML activity diagrams", Proceedings of the 2006 ACM symposium on Applied computing, 2006,

  - Peter Hrastnik, "Execution of business processes based on web services", International Journal of Electronic Business, Volume 2, Number 5 / 2004,

  - Petr Matousek, "An ASM Specication of the XPDL Language Semantics", Symposium on the Effectiveness of Logic in Computer Science, March 2002, [PS](http://www.mpi-sb.mpg.de/conferences/elics02/report/matousek.ps)

  - F. Puente, A. Rivero, J.D. Sandoval, P. Hernández, and C.J. Molina, "Improved Workflow Management System based on XPDL", Editor(s): M. Boumedine, S. Ranka, Proceedings of the The IASTED Conference on Knowledge Sharing and Collaborative Engineering, St. Thomas, US Virgin Islands, November 29-December 1, 2006, ISBN 0-88986-433-0

  - Petr Matousek, "Verification method proposal for business processes and workflows specified using the XPDL standard language", PhD thesis, Jan 2003

  -
  -
  -
  - Thomas Hornung, Agnes Koschmider, Jan Mendling, "Integration of Heterogeneous BPM Schemas: The Case of XPDL and BPEL", Technical Report JM-2005-03, Vienna University of Economics and Business Administration. 2006. [PDF](http://www.aifb.uni-karlsruhe.de/Forschungsgruppen/BIK/wi2007/Caise_Forum.pdf)

  - Wei Ge, Baoyan Song, Derong Shen, Ge Yu, "e_SWDL : An XML Based Workflow Definition Language for Complicated Applications in Web Environments" Web Technologies and Applications: 5th Asia-Pacific Web Conference, APWeb 2003, Xian, China, April 23-25, 2003. Proceedings,

## 関連項目

  - [ビジネスプロセス管理](../Page/ビジネスプロセス管理.md "wikilink")
  - [BPMN](https://ja.wikipedia.org/wiki/BPMN "wikilink")

## 外部リンク

  - [XPDL 2.0](http://www.wfmc.org/standards/XPDL.htm)
  - [XPDL & Workflow Patterns](http://is.tm.tue.nl/research/patterns/xpdl.htm) [PDF](http://is.tm.tue.nl/research/patterns/download/ce-xpdl.pdf)
  - [critical comments on XPDL 1.0](http://www.ebpml.org/xpdl.htm)
  - [Enterprise Workflow National Project](http://www.workflownp.org.uk/project/default_introduction.asp) イギリスでは政府機関での WfMC 使用を推進している。
  - [JaWE](http://www.enhydra.org/workflow/jawe/index.html) オープンソースの XPDL エディタ
  - [Bonita](http://wiki.bonita.objectweb.org/xwiki/bin/view/Main/WebHome) オープンソースの XPDL エディタ/エンジン
  - [JPEd](http://jped.sourceforge.net) オープンソースの XPDL エディタ
  - [WfMOpen](http://wfmopen.sourceforge.net) オープンソースの XPDL エンジン

[Category:XMLベースの技術](https://ja.wikipedia.org/wiki/Category:XMLベースの技術 "wikilink") [Category:ビジネスソフト](https://ja.wikipedia.org/wiki/Category:ビジネスソフト "wikilink") [Category:モデリング言語](https://ja.wikipedia.org/wiki/Category:モデリング言語 "wikilink")
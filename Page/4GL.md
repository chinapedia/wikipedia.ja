> この記事は[4GL](https://ja.wikipedia.org/wiki/4GL)から翻訳されています。


**4GL** とは、第四世代言語 (**4th generation language**)の略である。[FORTRAN](../Page/FORTRAN.md "wikilink")や[COBOL](../Page/COBOL.md "wikilink")のような手続き型言語より、より高機能な[プログラム言語](https://ja.wikipedia.org/wiki/プログラム言語 "wikilink")を一般的に指す。主に[アプリケーションプログラムを開発する際に用いられる](../Page/アプリケーションソフトウェア.md "wikilink")。

4GL言語は単体で存在することよりも、特定のアプリケーション開発システム(たとえばデータベースシステム)と組になって提供されることが多い。たとえば、データベースアクセスや報告書作成用言語やDBMSの言語\[1\]、[Oracleの](../Page/Oracle_Database.md "wikilink")[PL/SQL](https://ja.wikipedia.org/wiki/PL/SQL "wikilink")などである。

第四世代言語はプログラマーだけではなく、[エンドユーザー](../Page/エンドユーザー.md "wikilink")でも簡単なパラメーターを対話形式で指定するだけで、表計算のような業務処理を行ったり、あるいはプログラムを作成したり出来るようになっているのが特徴である。

第四世代というのは、[機械語](../Page/機械語.md "wikilink")を第一世代、[アセンブリ言語](../Page/アセンブリ言語.md "wikilink")を第二世代、[手続き型言語一般を第三世代と解釈するからである](../Page/手続き型プログラミング.md "wikilink")。

4GLの定量的定義は、Capers Jones が[ファンクションポイント法](https://ja.wikipedia.org/wiki/ファンクションポイント法 "wikilink")の研究の一環として行った。それによると、プログラミング言語の世代は開発者の生産性で決まり、[人月](../Page/人月.md "wikilink")当たりのファンクションポイント数(FP)で表される。4GLは、12 FP/人月から 20 FP/人月となる言語である。これを[ソースコードの行数に換算すると](https://ja.wikipedia.org/wiki/SLOC "wikilink")、ファンクションポイント当たり16行から27行でコーディングできるのが4GLだということになる。

4GLは[ドメイン固有言語](../Page/ドメイン固有言語.md "wikilink")(DSL)とよく比較される。研究者によっては、4GLはDSLのサブセットだとする者もいる\[2\]。[アセンブリ言語](../Page/アセンブリ言語.md "wikilink")が最新の開発環境（MS Studio）にもあることから、今後も各世代の言語が混在して利用されると予想する者もいる。

[Forth](../Page/Forth.md "wikilink")は、4番目の言語という意味が名前の由来である。しかし4GLではない。

## 歴史

それ以前から論文や会話で「4GL」という単語は使われていたが、最初に公式に使ったのは[1982年](../Page/1982年.md "wikilink")のの著書 *Applications Development Without Programmers* であった\[3\]。同書では、手続き型でない高級[仕様記述言語](../Page/仕様記述言語.md "wikilink")を指していた。最初の原始的な4GLとしては、[IBM](../Page/IBM.md "wikilink")の[RPG](../Page/RPG_\(プログラム言語\).md "wikilink")（1960年）が挙げられる。その後、Informatics の [MARK-IV](https://ja.wikipedia.org/wiki/MARK-IV "wikilink")（1967年）、[スペリー](https://ja.wikipedia.org/wiki/スペリー "wikilink")の[MAPPER](https://ja.wikipedia.org/wiki/MAPPER "wikilink")（1969年から社内で使用、1979年外部リリース）が登場した。

4GL という用語が生き延びてきた原因はいくつかある。まずこの用語は非常に広範囲のソフトウェア製品に適用される。また、ある種の特徴や実装能力を求める手法全体を表すとも考えられる。3GLはプログラマに大きな力を与えたが、同様に4GLは一般の人々に開発環境を開放した。

ある意味では4GLは[ブラックボックス](https://ja.wikipedia.org/wiki/ブラックボックス "wikilink")処理の例であり、世代が後になるほど機械そのものから遠くなっている。このため、4GLはエラーが発生した場合に理解するのが困難で[デバッグ](../Page/デバッグ.md "wikilink")しづらい傾向がある。4GLはビジネス分野で主に使われ、技術分野でも一部使われている。機械そのものから遠いということは、応用分野に近くなっていることを意味する。

初期の4GLでサポートされていたデータ入力方法は、[パンチカード](../Page/パンチカード.md "wikilink")での入力を考慮して、1行72桁に制限されていた。4GLは少ないパンチカードで各種処理が可能になっており、当時の3GLのプログラムのカードデッキに比較すると、枚数が非常に少なくて済んだ\[4\]。その後、コンピュータのメモリが増え、パンチカードから端末入力に変わっても、72桁のパンチカードのメタファーがそのまま使われ続けた。それでも、非常に洗練されたアプリケーションがサポートされた。インタフェースが改善され、より長い文が入力可能となり、文法に沿った改行などが可能になると、さらに能力がもたらされた。例えば[Nomadには](https://ja.wikipedia.org/wiki/:en:Nomad_software "wikilink")、以下のような一節がある。

  -
    もう1つのNormadの能力を示す例として、Nicholas Rawlings はコンピュータ歴史博物館のNCSS社に関する展示へのコメントがある。それによると、[ジェームズ・マーチン](https://ja.wikipedia.org/wiki/ジェームズ・マーチン "wikilink")は自身が *Engineer's Problem* と呼ぶ標準問題（職務格付けが平均で7以上の技術者に6%の昇給を与える）をNomadで解く方法をRawlingsに尋ねた。マーチンはCOBOLのプログラムが書かれた数十枚の紙と、Informatics社の MARK-IV で書かれた1、2枚の紙を提示した。Rawlings は同じ処理を行うプログラムを次の1行で提示した……

4GLの発展はいくつかの要因に影響を受けており、特にハードウェアとオペレーティングシステムの制限は大きな影響を与えた。4GLが登場したころ、ハードウェアやオペレーティングシステムが違えば、アプリケーション開発環境はシステム固有なものにならざるを得なかった。例えば、[スペリー](https://ja.wikipedia.org/wiki/スペリー "wikilink")の[MAPPER](https://ja.wikipedia.org/wiki/MAPPER "wikilink")がそれである。MAPPERは様々なアプリケーションに有効であることを証明し、最新のプラットフォームに移植されてきた。最新版は[ユニシス](https://ja.wikipedia.org/wiki/ユニシス "wikilink")のBISに含まれている\[5\]。MARK-IV は現在では[CAから](https://ja.wikipedia.org/wiki/CA_\(企業\) "wikilink") VISION:BUILDER として販売されている。

[アッチソン・トピカ・アンド・サンタフェ鉄道](../Page/アッチソン・トピカ・アンド・サンタフェ鉄道.md "wikilink")はシステム開発に[MAPPER](https://ja.wikipedia.org/wiki/MAPPER "wikilink")を使った。これは4GLを使った[ソフトウェアプロトタイピング](../Page/ソフトウェアプロトタイピング.md "wikilink")であり、エンドユーザーによるプログラム開発プロジェクトの例である\[6\]。この場合の考え方は、鉄道の専門家にMAPPERの使い方を習得させる方が、プログラマに「鉄道操作の複雑な事情」を教えるよりも簡単だ、というものであった\[7\]。

その後コンピュータの発展に伴って、4GLはデータベースシステムと関連付けられるようになり、初期の4GLとはかけ離れた技法やリソースを使うようになった。

## 具体例

  - 汎用
      - [DataFlex](https://ja.wikipedia.org/wiki/DataFlex "wikilink")
      - [Forte 4GL](https://ja.wikipedia.org/wiki/Forte_4GL "wikilink")
      - IBM [Cross System Product](https://ja.wikipedia.org/wiki/Cross_System_Product "wikilink")
      - [IBM VisualAgen/VisualAge Generator](http://www-306.ibm.com/software/awdtools/visgen/)
      - [PowerBuilder](http://www.powerbuilder.jp/)
      - [WinDev](https://ja.wikipedia.org/wiki/WinDev "wikilink")
      - [Visual DataFlex](http://www.visualdataflex.com/Home.asp?pageid=569)（Microsoft Windows のみ）
  - データベース[問い合わせ言語](https://ja.wikipedia.org/wiki/問い合わせ言語 "wikilink")
      - [FOCUS](http://www.informationbuilders.com/products/focus/overview.html)
      - [Informix-4GL](http://www-06.ibm.com/jp/software/data/informix/tools/4gl/)
      - [NATURAL](http://www.softwareag.com/Corporate/products/natural/default.asp)
      - [Progress OpenEdge](http://www.progress.com/openedge/index.ssp)
      - [SQL](../Page/SQL.md "wikilink")
  - 報告書生成
      - [BuildProfessional](http://www.todaysystems.com/content/web/bp_overview.htm)
      - [LINC](http://www.unisys.co.jp/linc/)
      - [METAFONT](../Page/METAFONT.md "wikilink")
      - [NATURAL](http://www.softwareag.com/Corporate/products/natural/default.asp)
      - [Oracle Reports](http://www.oracle.com/technology/global/jp/products/reports/index.html)
      - [PostScript](../Page/PostScript.md "wikilink")
      - [Progress OpenEdge](http://www.progress.com/openedge/index.ssp)
      - [RPG-II](../Page/RPG_\(プログラム言語\).md "wikilink")
  - データ操作/解析/報告
      - [Ab Initio](http://www.abinitio.com/abinitio/ab.nsf/abinitio_products)
      - [ABAP](https://ja.wikipedia.org/wiki/ABAP "wikilink")
      - [Audit Command Language](http://www.acl.com/products/)
      - [Clarion Programming Language](http://www.softvelocity.com/)
      - [FOCUS](http://www.informationbuilders.com/products/focus/overview.html)
      - [IDL](https://ja.wikipedia.org/wiki/IDL_\(プログラミング言語\) "wikilink")
      - [IGOR Pro](../Page/IGOR_Pro.md "wikilink")
      - [Informix-4GL](http://www-06.ibm.com/jp/software/data/informix/tools/4gl/)
      - [LabVIEW](../Page/LabVIEW.md "wikilink")
      - [Mathematica](../Page/Mathematica.md "wikilink")
      - [MATLAB](https://ja.wikipedia.org/wiki/MATLAB "wikilink")
      - [NATURAL](http://www.softwareag.com/Corporate/products/natural/default.asp)
      - [PL/SQL](https://ja.wikipedia.org/wiki/PL/SQL "wikilink")
      - [Progress OpenEdge](http://www.progress.com/openedge/index.ssp)
      - [R言語](https://ja.wikipedia.org/wiki/R言語 "wikilink")
      - [S言語](../Page/S言語.md "wikilink")
      - [SAS](../Page/SAS_Institute.md "wikilink")
      - [SPSS](../Page/SPSS.md "wikilink")
      - [Stata](http://www.stata.com/)
      - [XBase++](http://www.alaska-software.com/products/xpp/xpp.shtm)
  - データベース駆動型GUIアプリケーション開発
      - [Genexus](http://www.genexus.com/portal/hgxpp001.aspx?2)
      - [UNIFACE](http://www.compuware.com/products/uniface/)
  - 画面生成
      - [FOURGEN](http://www.fourgen.com./)
      - [Oracle Forms](http://www.oracle.com/technology/global/jp/products/forms/index.html)
  - [GUI生成](https://ja.wikipedia.org/wiki/グラフィカルユーザインタフェース "wikilink")
      - [4th Dimension](http://www.4d.com/)
      - [MATLAB](https://ja.wikipedia.org/wiki/MATLAB "wikilink") の GUIDE
      - [Omnis Studio](http://www.omnis.net/index.html?detail=overview)
      - [OpenROAD](http://www.ingres.com/products/openroad.php)
      - [Revolution](http://www.runrev.com/home/product-family/)
  - ウェブ開発
      - [ColdFusion](../Page/ColdFusion.md "wikilink")
      - [Ruby on Rails](../Page/Ruby_on_Rails.md "wikilink")

## 関連項目

  - [ドメイン固有言語](../Page/ドメイン固有言語.md "wikilink")
  - [RAD](https://ja.wikipedia.org/wiki/RAD_\(計算機プログラミング環境\) "wikilink")

## 脚注

## 外部リンク

  - [Fourth Generation Environments](http://www.soi.city.ac.uk/~tony/dbms/4ges.html)
  - [Aubit project](http://aubit4gl.sourceforge.net/) GPL/GNU の4GLオープンソース開発ツールのプロジェクト
  - [Domain-Specific Languages for Software Engineering](http://csdl2.computer.org/comp/proceedings/hicss/2002/1435/09/14350279.pdf) 4GL と DSL の比較

[Category:プログラミング言語](https://ja.wikipedia.org/wiki/Category:プログラミング言語 "wikilink")

1.
2.  35th Hawaii International Conference on System Sciences - 1002 [Domain-Specific Languages for Software Engineering](http://csdl2.computer.org/comp/proceedings/hicss/2001/0981/09/09819071.pdf)
3.  Martin, James. *Application Development Without Programmers.* Prentice-Hall, 1981. ISBN 0-13-038943-9.
4.  [Columbia University Computing History: IBM Cards](http://www.columbia.edu/acis/history/cards.html)
5.  [Unisys](https://ja.wikipedia.org/wiki/ユニシス "wikilink"). [Business Information Server](http://www.unisys.com.hk/products/software/application__development/business__information__server/features.htm) (BIS).
6.  Louis Schlueter, User-Designed Computing: The Next Generation, 1988. \[book on report generator and MAPPER systems\]
7.  McNurlin & Sprague. [Technologies for Developing Systems](http://telaga.cs.ui.ac.id/WebKuliah/IKI42400/2004/McNurlin-5ed-ch09.pdf) Information Systems Management in Practice. Prentice Hall, 2003. ISBN 0-13-101139-1
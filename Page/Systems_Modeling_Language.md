> この記事は[Systems Modeling Language](https://ja.wikipedia.org/wiki/Systems_Modeling_Language)から翻訳されています。


**Systems Modeling Language**（**SysML**）は、[システムズエンジニアリング](https://ja.wikipedia.org/wiki/システムズエンジニアリング "wikilink")のための[ドメイン固有モデリング](../Page/ドメイン固有モデリング.md "wikilink")言語である。各種システムや「システムのシステム」の仕様記述、分析、設計、検証、評価に使うことができる。SysML は本来[オープンソース](../Page/オープンソース.md "wikilink")のプロジェクトとして開発され、オープンソースとしての配布および利用ライセンスもある。SysML は[統一モデリング言語](../Page/統一モデリング言語.md "wikilink")(UML)のサブセットに[UMLのプロファイル機構を使って拡張したものと定義できる](https://ja.wikipedia.org/wiki/プロファイル_\(UML\) "wikilink")。

## 概要

SysML はソフトウェア向きの傾向がある UML にシステム工学向けの改善を施している。改善点には以下のようなものがある:\[1\]

  - SysML の意味論はより柔軟で表現豊かとなっている。SysML は UML のソフトウェア向けの制限を撤廃し、新たな2種類の図（リクワイアメント図とパラメトリック図）を追加した。リクワイアメント図は[要求管理](https://ja.wikipedia.org/wiki/要求管理 "wikilink")に使われ、パラメトリック図は性能分析と定量的解析に使われる。この結果、SysML は様々なシステム（ハードウェア、ソフトウェア、情報、製造ライン、人員管理、設備管理）のモデル化に利用可能となっている。
  - SysML は小型の言語であり、学習も利用も容易である。SysML は UML のソフトウェア向けの構成要素を省いてあるので、言語全体としては小型化している。
  - SysML のアロケーションテーブルは様々な割り当てを表現するのに使える。UML は表をほとんど使わないが、SysML はアロケーションテーブルを使って要求仕様割り当て、機能割り当て、構造的割り当てなどを記述できる。これによって自動的な検証と評価、ギャップ分析などが可能となる。
  - SysMLモデル管理はモデル、ビュー、ビューポイントをサポートする。これは UML を[IEEE 1471向けに拡張したものである](../Page/IEEE_1471.md "wikilink")。

SysML は UML 2.0 の13種類の図のうち 7 種類を利用し、2種類の図（リクワイアメント図とパラメトリック図）とアロケーションテーブルを追加している。アロケーションテーブルは他の図から動的に導き出すことが可能である。SysML と UML 2.0 の比較表が [SysML FAQ](http://www.sysmlforum.com/faq/) にある。

SysML の UML に対するシステム工学上の優位性は、自動車システムなどの具体例を考えれば明らかとなる。SysML では、機能や性能やインターフェイスに関する要求仕様をリクワイアメント図で効率的に記述できるが、UML では[ユースケース図](https://ja.wikipedia.org/wiki/ユースケース図 "wikilink")しかない。また、SysML では、最大加速/総重量/空調機能/車内の雑音レベルといった値の制限をパラメトリック図で記述できる。UML はこのような性能や機構についての情報を直接的に扱う機構を持たない。

自動車システムの例をさらに使用すると、SysMLではアクティビティ図や状態遷移図を拡張して車載コンピュータの[組み込みソフトウェアのロジックを記述できる](../Page/組み込みシステム.md "wikilink")。他にもSysMLの図で自動車工場をモデル化したり、各工場の組織の相互関係をモデル化したりすることができる。

## 歴史

2001年1月、International Council on Systems Engineering (INCOSE) の Model Driven Systems Design ワークグループが UML をシステム工学向けにカスタマイズするために SysML イニシアティブを組織することを決定した。その後 INCOSE と UML 仕様を管理する [Object Management Group](https://ja.wikipedia.org/wiki/Object_Management_Group "wikilink") (OMG) は共同でワークグループ(SE DSIG)を2001年6月に発足させた。SE DSIG は INCOSE および ISO AP 233 ワークグループと協力してモデリング言語の要求仕様を策定し、OMG がこれを *UML for Systems Engineering Request for Proposal* として2003年3月に公表した\[2\]。

2003年、Cris Kobryn と Sanford Friedenthal は *SysML Partners* という非公式な業界団体を組織した\[3\]。独自の技術貢献者やSysMLの1.0aの仕様の共著者はLaurent Balmelli、Conrad Bock、Rick Steiner、Alan Moore と Roger Burkhartでした。ここで、OMG の *UML for Systems Engineering Request for Proposal* に従ってSysMLのオープンソース仕様策定を行った\[4\]。SysML Partners は2004年にオープンソースのSysML仕様ドラフト版を公開し、2005年11月に OMG に SysML 1.0a を送った。

### OMG SysML

SysML仕様に関するいくつかのプロポーザルを検討したうえで、2006年4月、"SysML Merge Team" の案が OMG に提出された\[5\]。この案に対して OMG で投票が行われ、2006年6月に [*OMG SysML*](http://www.omgsysml.org) として採用され、元となったオープンソース版と区別するためにOMGの商標とされた。現在の OMG SysML仕様は Final Adopted Specification というステータスである\[6\]。OMG Finalization Task Force は OMG SysML の最終版を2007年4月に完成させることを計画しており、その後さらに投票が行われて公式な仕様となる予定である。

OMG SysML は本来のオープンソースのSysMLから派生したものであるため、配布と利用に関してオープンソースライセンスもある。

## ツール

一部ツールベンダーは既に SysML サポートを表明しており、OMG SysML 仕様に適合するようツールを更新中である。OMG SysML サポートを表明しているツールベンダーのリストは [Official OMG SysML Website](http://www.omgsysml.org) にある。

### モデル交換

OMG UML 2.0 のプロファイルとして、SysMLモデルは最新の[XML Metadata Interchange](https://ja.wikipedia.org/wiki/XML_Metadata_Interchange "wikilink")(XMI)を使って交換可能である。さらに SysML は策定中の[ISO 10303](https://ja.wikipedia.org/wiki/ISO_10303 "wikilink")（Standard for the Exchange of Product model data）の AP-233 とも整合するようになっている。これは、[システム工学](../Page/システム工学.md "wikilink")ソフトウェアアプリケーションやツールでの情報交換と情報共有のための標準規格である。

## 参考文献

<div class="references-small">

<references/>

</div>

## 外部リンク

  - [SysML Open Source Specification Project](http://www.sysml.org) SysML オープンソース仕様関連情報など
  - [Official OMG SysML Website](http://www.omgsysml.org) OMG SysML 仕様関連情報
  - [SysML Forum](http://www.SysMLforum.com) SysMLコミュニティ。ツールなど各種情報がある。
  - [SysML Forum mailing list](http://groups.google.com/group/SysMLforum) モデレータ付きメーリングリスト
  - [Visio Stencil and Template for SysML 1.0](http://www.softwarestencils.com/sysml/index.html)
  - 記事 "[SysMLに関する＠ITの記事（2006年9月22日）](http://www.atmarkit.co.jp/im/carc/serial/redge49/redge49a.html)"

[Category:システムモデリング言語](https://ja.wikipedia.org/wiki/Category:システムモデリング言語 "wikilink") [Category:統一モデリング言語](https://ja.wikipedia.org/wiki/Category:統一モデリング言語 "wikilink") [Category:システム工学](https://ja.wikipedia.org/wiki/Category:システム工学 "wikilink") [Category:モデリング言語](https://ja.wikipedia.org/wiki/Category:モデリング言語 "wikilink")

1.
2.
3.
4.
5.  [OMG document ad/06-03-01](http://www.omg.org/docs/ad/06-03-01.pdf)
6.  [OMG document ptc/06-05-04](http://www.omg.org/docs/ptc/06-05-04.pdf)
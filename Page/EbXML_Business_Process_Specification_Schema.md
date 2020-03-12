> この記事は[EbXML Business Process Specification Schema](https://ja.wikipedia.org/wiki/EbXML_Business_Process_Specification_Schema)から翻訳されています。


**ebXML Business Process Specification Schema**（**BPSS**または**ebBP**と略される）は、[ebXML](https://ja.wikipedia.org/wiki/ebXML "wikilink")の仕様のひとつで、企業間電子商取引のプロセスを[XML形式で記述する言語である](../Page/Extensible_Markup_Language.md "wikilink")。

BPSSは2001年にバージョン1.01が公開された後、[OASIS](../Page/OASIS_\(組織\).md "wikilink") ebXML Business Process TCで次期版の標準化が行われ、2006年12月にバージョン2.0.4がOASIS標準として承認された。

## 特徴

「[ビジネスプロセス](../Page/ビジネスプロセス.md "wikilink")」を記述する言語は複数存在するが、BPSSで特徴的なのは、記述の対象が外部から観察可能なメッセージ交換の順序のみであり、取引を行う企業の内部のロジックは記述の対象外であることである。つまり、メッセージ送受信の順序さえBPSSでの記述に則っていれば、企業内での処理のロジックは自由に実装して良いということである。こうした記述方式は、ひとつの企業内からの視点で処理制御を記述するモデルと対比して**グローバルモデル**あるいは**コレオグラフィ**（choreography、振り付けの意）などと呼ばれることもある。

このような特徴から、BPSSは企業間でどのようにメッセージを送りあうかを合意する用途に適している。また、業界における標準のプロセスを記述するのに使うこともできる。電機・電子業界における電子商取引標準のひとつ[RosettaNet](../Page/RosettaNet.md "wikilink")では、メッセージのやり取り(Partner Interface Process, PIP)の記述にBPSSが用いられている。

BPSSはその[メタモデル](../Page/メタモデル.md "wikilink")において、[UN/CEFACT Modelling Methodology](https://ja.wikipedia.org/wiki/UN/CEFACT_Modelling_Methodology "wikilink") (UMM)をベースにしている。ビジネスプロセス作成の方法論としてもUMMを用いることが推奨されている。

プロセス定義を図示する記法は、BPSS仕様では規定されていない。ただし、仕様の構成上、[UMLアクティビティ図との親和性が高い](https://ja.wikipedia.org/wiki/Unified_Modeling_Language "wikilink")。

## プロセス定義の構成

この節ではBPSSバージョン1.01に基づいてプロセス定義の概略を記す。

BPSSによるプロセス定義の構成要素は、主に、Business Document、Business Transaction、Binary Collaboration、Multi-party Collaborationである。

**Business Document**は、企業間で交換される伝票の定義である。外部に存在する[XML Schemaを参照して名前をつける形で定義する](https://ja.wikipedia.org/wiki/XML_Schema "wikilink")。

**Business Transaction**は、一回の伝票交換を表現する。例えば、注文伝票を出し、その注文に対する回答を返すといった定義を行う。交換する伝票は上述のBusiness Documentの定義を参照する。

**Binary Collaboration**は、取引企業2社の間での伝票交換の順序を表現する。これがいわゆる「プロセス」らしい部分であり、UMLアクティビティ図に近い形式で上記Business Transactionの実行を順序付ける。Binary Collaborationの各ステップで実行するアクティビティは、Business Transactionを実行するBusiness Transaction Activityか、他のBinary Collaborationを[サブルーチン](../Page/サブルーチン.md "wikilink")的に呼び出すCollaboration Activityのいずれかである。

**Multi-party Collaboration**は、3社以上の間の取引プロセスの記述になるが、仕様が不完全なため実際にはまだ使うことはできない。

## 外部リンク

  - [OASIS ebXML Business Process TC](http://www.oasis-open.org/committees/tc_home.php?wg_abbrev=ebxml-bp)
  - [BPSS 1.01仕様書](http://www.ebxml.org/specs/ebBPSS.pdf)
  - [BPSS 2.0.4仕様書](http://docs.oasis-open.org/ebxml-bp/2.0.4/)
  - [ebXML Business Process Specification Schema (BPSS)技術解説](http://www.xmlconsortium.org/websv/kaisetsu/C34/content.html)

[Category:XMLベースの技術](https://ja.wikipedia.org/wiki/Category:XMLベースの技術 "wikilink") [Category:電子商取引](https://ja.wikipedia.org/wiki/Category:電子商取引 "wikilink") [Category:長大な項目名](https://ja.wikipedia.org/wiki/Category:長大な項目名 "wikilink")
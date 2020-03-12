> この記事は[EbXML Collaboration Protocol Profile and Agreement](https://ja.wikipedia.org/wiki/EbXML_Collaboration_Protocol_Profile_and_Agreement)から翻訳されています。


**ebXML Collaboration Protocol Profile and Agreement** (**ebCPPA**) は、企業間[電子商取引](../Page/電子商取引.md "wikilink")において、プロトコル上の能力や取引の役割に関して、取引当事者のプロファイルを記述し、また、取引を行う2者間の合意を記述するための[XML言語である](../Page/Extensible_Markup_Language.md "wikilink")。[ebXML](https://ja.wikipedia.org/wiki/ebXML "wikilink")の仕様のひとつであり、[OASISで標準化されている](../Page/OASIS_\(組織\).md "wikilink")。また、[ISOによってISO](https://ja.wikipedia.org/wiki/国際標準化機構 "wikilink")/TS 15000-1として承認されている。

CPPAは実際には、CPP (Collaboration Protocol Profile) とCPA (Collaboration Protocol Agreement) の2つの言語を規定する。この2つの言語は共通点が多いため、その文法は1つの[XML Schema定義で規定されている](https://ja.wikipedia.org/wiki/XML_Schema "wikilink")。

CPPは、ある取引当事者 (企業) についての記述である。その企業が、どのような業務プロセスのどの役割を担当可能であるか、また、取引を行うにあたってどのようなプロトコルが使用可能かを記述する。

CPAは、実際に取引を行う際に作成されるもので、取引を行う2者がそれぞれどのプロセスのどの役割を担うか、また、メッセージ交換のプロトコルに何を使うかを具体的に指定する。CPAは、2者のCPPを合成して作成することが想定されている (ただし、CPAを作るにあたっては本当にCPPを合成する手順を踏む必要はない)。

作成されたCPAは、企業間取引のメッセージング ([ebXML Message Service等](https://ja.wikipedia.org/wiki/ebXML_Message_Service "wikilink")) のハンドラへの設定ファイルとみなすことができる。メッセージハンドラはCPAにしたがってプロトコルやパラメタ等の設定を行う。

## ebXMLの他の仕様との関連

  - [ebXML Message Serviceを実装したソフトウェアは](https://ja.wikipedia.org/wiki/ebXML_Message_Service "wikilink")、CPAに対応していることが多い。
  - CPPAは、[ebXML BPSSで記述された取引プロセスを実施するにあたり](https://ja.wikipedia.org/wiki/ebXML_Business_Process_Specification_Schema "wikilink")、具体的にどのようなメッセージング技術で実行するかを指定する
  - CPPは企業の情報として[ebXML Registryに登録され](https://ja.wikipedia.org/wiki/ebXML_Registry "wikilink")、随時参照可能とするような運用が考えられる

## 外部リンク

  - [OASIS ebXML Collaboration Protocol Profile and Agreement (CPPA) TC](http://www.oasis-open.org/committees/tc_home.php?wg_abbrev=ebxml-cppa)
  - [ebXML CPPA 2.0仕様書](http://www.oasis-open.org/committees/ebxml-cppa/documents/ebcpp-2.0.pdf)
  - [ebXML CPP/CPA解説](http://www.xmlconsortium.org/websv/kaisetsu/C32/content.html)

[Category:電子商取引](https://ja.wikipedia.org/wiki/Category:電子商取引 "wikilink") [Category:XMLベースの技術](https://ja.wikipedia.org/wiki/Category:XMLベースの技術 "wikilink") [Category:長大な項目名](https://ja.wikipedia.org/wiki/Category:長大な項目名 "wikilink")
> この記事は[Service Data Objects](https://ja.wikipedia.org/wiki/Service_Data_Objects)から翻訳されています。


**Service Data Objects**（サービスデータオブジェクト、**SDO**）とは、様々なデータを統一的にアクセスできるようにする技術である。2004年、[BEAシステムズ](../Page/BEAシステムズ.md "wikilink")と[IBM](../Page/IBM.md "wikilink")が共同で開発し、[Java Community Process](../Page/Java_Community_Process.md "wikilink") が承認した。2005年11月、[Service Component Architectureの一部としてバージョン](https://ja.wikipedia.org/wiki/Service_Component_Architecture "wikilink")2.0が登場した。

## 他の技術との関連

当初 **Web Data Objects**（ウェブデータオブジェクト、**WDO**）と呼ばれ、[IBM WebSphere Application Server](../Page/WebSphere_Application_Server.md "wikilink") 5.1 と IBM WebSphere Studio Application Server 5.1.2 の一部としてリリースされた\[1\]。他の類似の技術としては、[JDO](../Page/Java_Data_Objects.md "wikilink"), [EMF](https://ja.wikipedia.org/wiki/Eclipse_Modeling_Framework "wikilink"), [JAXB](../Page/Java_Architecture_for_XML_Binding.md "wikilink"), [ADO.NET](../Page/ADO.NET.md "wikilink") がある。

## 設計

Service Data Objects は言語に依存しないデータ構造を利用し、各種サービス提供実体間の通信を可能にする。[木構造とその上での走査](../Page/木構造_\(データ構造\).md "wikilink")（幅優先/深さ優先）方法を提供し、クライアントプログラムが要素を操作できるようにする。オブジェクトは静的（フィールド数固定）でも、無制限のフィールドを持てる動的な構造でもよい。仕様では、全フィールドに[メタデータ](../Page/メタデータ.md "wikilink")が定義され、オブジェクトのグラフについて変更サマリーを提供することで、プログラムがデータをより効率的に扱えるようにする。

## 開発元

2007年4月以降、仕様は[OASISの](../Page/OASIS_\(組織\).md "wikilink") Open CSA\[2\]が策定しており、BEAシステムズ・IBM・Rouge Wave・[オラクル](../Page/オラクル_\(企業\).md "wikilink")・[SAP](../Page/SAP_\(企業\).md "wikilink")・Siebel・[Sybase](../Page/Sybase.md "wikilink")・Xcalia・Software AGと[サン・マイクロシステムズ](../Page/サン・マイクロシステムズ.md "wikilink")が参加している。それ以前からある非公式な協業組織 Open SOA\[3\] もこれに協力している。

## 実装

  - Rogue Wave Software (HydraSDO)
  - CodeFutures Software (FireStorm/SDO)
  - Xcalia （Java および .Net）
  - BEA (AquaLogic Data Services Platform)
  - IBM (Virtual XML Garden)
  - IBM (WebSphere Process Server)

[オープンソース](../Page/オープンソース.md "wikilink")実装としては、以下のものがある。

  - [Apache Tuscany](http://incubator.apache.org/tuscany/)（Java および C++）
  - [SOA PHP](http://www.osoa.org/display/PHP/SOA+PHP+Homepage)

## 出典

## 外部リンク

  - [OASIS Open CSA](http://www.oasis-opencsa.org/sdo) SDOの公式サイト
  - [Service Data Objects](http://www.osoa.org/display/Main/Service+Data+Objects+Home)
  - [SDO Specifications at OpenSOA](http://www.osoa.org/display/Main/Service+Data+Objects+Specifications)
  - [Introduction to Service Data Objects](http://www.codefutures.com/service-data-object/)
  - [Introducing Service Data Objects for PHP](http://www.zend.com/pecl/tutorials/sdo.php)
  - [Service Data Objects Tutorial](http://www.codesuccess.com/tutorials/sdo/)

[Category:コンピュータネットワーク](https://ja.wikipedia.org/wiki/Category:コンピュータネットワーク "wikilink") [Category:プログラミングパラダイム](https://ja.wikipedia.org/wiki/Category:プログラミングパラダイム "wikilink") [Category:情報技術](https://ja.wikipedia.org/wiki/Category:情報技術 "wikilink") [Category:対象](https://ja.wikipedia.org/wiki/Category:対象 "wikilink")

1.  [Introduction to Service Data Objects](http://www.ibm.com/developerworks/java/library/j-sdo/)
2.  [OASIS Open CSA](http://www.oasis-opencsa.org/)
3.  [Open SOA](http://www.osoa.org)
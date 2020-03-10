> この記事は[Common Information Model](https://ja.wikipedia.org/wiki/Common_Information_Model)から翻訳されています。


**Common Information Model**（**CIM**）とは、[IT環境における管理対象を典型的な](../Page/情報技術.md "wikilink")[オブジェクトとその関係で表現する方法を定義した](../Page/オブジェクト_\(プログラミング\).md "wikilink")[オープン標準](https://ja.wikipedia.org/wiki/オープン標準 "wikilink")である。これにより、そうした管理対象をメーカーに関わらず一貫して[管理することを意図している](../Page/システム管理.md "wikilink")。

## 概要

CIMの別の説明として、管理対象に関する管理情報を相互にやり取り可能にするものとも言われる。しかしこの説明では、CIM が管理対象とその管理情報を表現するだけでなく、それらを制御・管理する手段を提供する点を説明できていない。情報の共通モデルを使うことで、一度管理ソフトウェアを開発すれば、そのモデルに則った各種実装に対応可能となり、情報が失われることもない。

CIM標準は [Distributed Management Task Force](https://ja.wikipedia.org/wiki/Distributed_Management_Task_Force "wikilink") (DMTF) が定義し公表している。関連する標準である [Web-Based Enterprise Management](../Page/Web-Based_Enterprise_Management.md "wikilink")（WBEM、こちらも DMTF による）には、CIM実装を発見しアクセスするためのプロトコルが含まれている。

## CIM標準に含まれるもの

CIM標準には **CIM Infrastructure Specification** と **CIM Schema** が含まれる。

  - CIM Infrastructure Specification
    CIM のアーキテクチャとコンセプトを定義したもの。CIM Schema を定義する言語の仕様、CIM を他の情報モデル（例えば [SNMP](../Page/Simple_Network_Management_Protocol.md "wikilink")）にマッピングする方法も含まれる。CIM アーキテクチャは[UMLに基づいており](../Page/統一モデリング言語.md "wikilink")、オブジェクト指向である。管理対象は CIM [クラスで表され](../Page/クラス_\(コンピュータ\).md "wikilink")、それらの関係は CIM [関連で表される](https://ja.wikipedia.org/wiki/クラス図#関連 "wikilink")。[継承によって典型的管理対象を特殊化して](https://ja.wikipedia.org/wiki/継承_\(プログラミング\) "wikilink")、特定の管理対象を表すことができる。
  - CIM Schema
    [IT環境における管理対象の基盤となるオブジェクト群とその関連を定義した](../Page/情報技術.md "wikilink")[概念スキーマ](https://ja.wikipedia.org/wiki/概念スキーマ "wikilink")である。現在IT環境で想定される管理対象をほぼ網羅しており、例えば、[コンピュータシステム](../Page/コンピュータシステム.md "wikilink")、[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink")、[コンピュータネットワーク](https://ja.wikipedia.org/wiki/コンピュータネットワーク "wikilink")、[ミドルウェア](https://ja.wikipedia.org/wiki/ミドルウェア "wikilink")、[サービス](https://ja.wikipedia.org/wiki/デーモン_\(ソフトウェア\) "wikilink")、[ストレージなどが定義されている](../Page/補助記憶装置.md "wikilink")。CIM Schema はそれら管理対象を表現するための共通基盤を与えている。多くの管理対象は固有の振る舞いをするため、CIM Schema は各管理対象のベンダーが自分の製品向けに拡張できるようになっている。

CIM は DMTF による（[WBEM](../Page/Web-Based_Enterprise_Management.md "wikilink") や [SMASH](https://ja.wikipedia.org/wiki/Systems_Management_Architecture_for_Server_Hardware "wikilink") など）各種標準のベースとなっている。また、ストレージ管理のための標準である [SMI-S](../Page/SMI-S.md "wikilink") のベースでもある。

## CIMの最新バージョン

  - CIM Specificationの最新版 2.2は[1999年](../Page/1999年.md "wikilink")6月14日にリリースされている。
  - CIM Compliance Specificationの最新版は2.3は[2005年](https://ja.wikipedia.org/wiki/2005年 "wikilink")10月4日にリリースされている。
  - CIM Infrastructure Specification の最新版 2.3 は[2005年](https://ja.wikipedia.org/wiki/2005年 "wikilink")10月4日にリリースされている。
  - CIM Schema の最新版 2.50.0 は[2018年](../Page/2018年.md "wikilink")1月4日にリリースされている。

## CIM 実装例

  - [SAN業界の団体](../Page/ストレージエリアネットワーク.md "wikilink") [SNIA](https://ja.wikipedia.org/wiki/SNIA "wikilink") は CIM と WBEM に基づいて [SMI-S](../Page/SMI-S.md "wikilink") というストレージ管理標準を策定した。
  - 多くの[サーバ](../Page/サーバ.md "wikilink")製造業者は DMTF の [SMASH](https://ja.wikipedia.org/wiki/Systems_Management_Architecture_for_Server_Hardware "wikilink") イニシアティブに参加し、CIM に基づいたサーバ管理を定義している。
  - DMTF は CIM ベースの[デスクトップパソコン](../Page/デスクトップパソコン.md "wikilink")管理を定義するべく DASH イニシアティブを結成している。
  - 多くのオペレーティングシステムは CIM 実装を提供している。例えば、[Microsoft Windows](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink") では [Windows Management Instrumentation](https://ja.wikipedia.org/wiki/Windows_Management_Instrumentation "wikilink") (WMI) API で CIM を実装している。[Linux](https://ja.wikipedia.org/wiki/Linux "wikilink") では [SourceForge.net](https://ja.wikipedia.org/wiki/SourceForge.net "wikilink") での SBLIM プロジェクトで CIM 実装が行われている。
  - 例えば、VMwareでは、CIMプロバイダによりデバイスの監視を行う。そして、SMASHインターフェースにより、ゲストOS等の制御をおこなうことが出来る。

CIM 関連のツール市場も成長しつつある。

## 関連項目

  - [SNMP](../Page/Simple_Network_Management_Protocol.md "wikilink")
  - [DMTF](https://ja.wikipedia.org/wiki/Distributed_Management_Task_Force "wikilink")
  - [SNIA](https://ja.wikipedia.org/wiki/SNIA "wikilink")
  - [WBEM](../Page/Web-Based_Enterprise_Management.md "wikilink")
  - [SMASH](https://ja.wikipedia.org/wiki/Systems_Management_Architecture_for_Server_Hardware "wikilink")
  - [SMI-S](../Page/SMI-S.md "wikilink")
  - [WMI](https://ja.wikipedia.org/wiki/Windows_Management_Instrumentation "wikilink")

## 外部リンク

  - 仕様など
      - [DMTF教育資材](http://www.dmtf.org/education/)
      - [DMTF CIM Standard](http://www.dmtf.org/standards/cim/)(CIM SchemaやCIM Infrastructure Specなど)
      - [CIM Specifications](http://www.dmtf.org/standards/published_documents/)(Profileなど)
      - [CIM Tutorial from WBEM Solutions](http://www.wbemsolutions.com/tutorials/CIM/cim.html)
      - [VMに関する仕様策定状況](http://www.dmtf.org/about/committees/SVPCWGCharter.pdf)
  - 実装など
      - [OpenPegasus](http://www.openpegasus.org/)
          - [機能実装状況](http://www.openpegasus.org/page.tpl?CALLER=index.tpl&ggid=799)
      - [SBLIM project on sourceforge](http://sourceforge.net/projects/sblim)
  - 実装(プロバイダー)
      - [libvirt-CIM VMMのCIM実装](http://libvirt.org/CIM/)
      - [Xen-CIMとの接続ツール(Kensho)](http://community.citrix.com/display/xs/Kensho)
  - その他
      - [CIM知識ベースを活用したシステム運用管理のインテリジェント化](http://www.nri.co.jp/opinion/g_souhatsu/pdf/gs20040107.pdf)(PDF)-[野村総合研究所](../Page/野村総合研究所.md "wikilink")

[Category:コンピュータネットワーク](https://ja.wikipedia.org/wiki/Category:コンピュータネットワーク "wikilink") [Category:情報技術](https://ja.wikipedia.org/wiki/Category:情報技術 "wikilink")
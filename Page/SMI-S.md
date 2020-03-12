> この記事は[SMI-S](https://ja.wikipedia.org/wiki/SMI-S)から翻訳されています。


**SMI-S**（Storage Management Initiative - Specification）とは、[SNIA](https://ja.wikipedia.org/wiki/SNIA "wikilink") (Storage Networking Industry Association) が開発・保守している[ストレージに関する標準である](../Page/補助記憶装置.md "wikilink")。[ANSI](https://ja.wikipedia.org/wiki/ANSI "wikilink")標準 [ANSI INCITS 388-2004](http://webstore.ansi.org/ansidocstore/product.asp?sku=ANSI+INCITS+388-2004) として承認されている。SMI-S は [Distributed Management Task Force](../Page/Distributed_Management_Task_Force.md "wikilink") が定義した [Common Information Model](../Page/Common_Information_Model.md "wikilink") や [Web-Based Enterprise Management](../Page/Web-Based_Enterprise_Management.md "wikilink") に基づいている。

SMI-S の主な目的は、ストレージにおける異機種混在システムでの相互運用性を高めることである。現在のバージョンは SMI-S V1.1.0。18社の SNIAメンバー企業の 280 以上の製品が SMI-S 1.0.2 準拠の認証を受けている\[1\]。SMI-S 準拠ストレージシステムの開発・マーケティングについてのチュートリアルが WBEM Solutions のサイトにある\[2\]。

## 基本概念

SMI-S は、ストレージシステムに関する [DMTF](../Page/Distributed_Management_Task_Force.md "wikilink") 管理[プロファイルを定義している](https://ja.wikipedia.org/wiki/プロファイル_\(工学\) "wikilink")。SMI-S はプロファイルとサブプロファイルから構成されている。プロファイルは、自律・自己完結型管理ドメインの振る舞いを記述したものである。SMI-S には、[ディスクアレイ](../Page/ディスクアレイ.md "wikilink")、[スイッチングハブ](../Page/スイッチングハブ.md "wikilink")、ストレージ・ビジュアライザ、ボリューム管理など様々なドメインのプロファイルを含む。DMTF の用語では、特定のプロファイルの実装をプロバイダーと呼ぶ。サブプロファイルは、あるドメインに含まれる多くのプロファイルで共通な部分を記述したものである。

SMI-S の実体は以下の2種類に分類される。

  - クライアント
    管理ソフトウェア。プロバイダーとの物理的なリンクさえあれば、ネットワーク上のどこにあってもよい。
  - プロバイダー
    ストレージ・ファブリック（ネットワーク）内の管理対象デバイス。

クライアントとしては、ホストシステムベースの管理アプリケーション、エンタープライズ管理アプリケーション、[SANアプライアンスベースの管理アプリケーションなどがある](../Page/ストレージエリアネットワーク.md "wikilink")。プロバイダーは、ディスクアレイ、ホストバスアダプター、スイッチ、テープ装置などである。

## 年表

  - [2002年](../Page/2002年.md "wikilink") - BlueFin が生まれ、後に SMI-S に改称された。
  - [2003年](../Page/2003年.md "wikilink") - SNIA により SMI-S 1.0 が公表された。また、SNIA Conformance Testing Program も作られた。
  - [2004年](../Page/2004年.md "wikilink") - SMI-S 1.0.2 が [ANSI](https://ja.wikipedia.org/wiki/ANSI "wikilink") 標準となった。SMI-S 1.1.0 の開発が始まる。
  - [2005年](../Page/2005年.md "wikilink") - SMI-S 1.0.2 が [ISO](https://ja.wikipedia.org/wiki/国際標準化機構 "wikilink") に提出された。SMI-S 1.1.0 リリース。

## 関連項目

  - [CIM](../Page/Common_Information_Model.md "wikilink") - Common Information Model
  - [WBEM](../Page/Web-Based_Enterprise_Management.md "wikilink") - Web Based Enterprise Management
  - [SNIA](https://ja.wikipedia.org/wiki/SNIA "wikilink") - Storage Networking Industry Association

## 脚注

<references />

## 外部リンク

  - [SNIA SMI-S Homepage](http://www.snia.org/smi/home)
  - [SMI Specification](http://www.snia.org/tech_activities/standards/curr_standards/smi)

[Category:コンピュータネットワーク](https://ja.wikipedia.org/wiki/Category:コンピュータネットワーク "wikilink") [Category:情報技術](https://ja.wikipedia.org/wiki/Category:情報技術 "wikilink") [Category:ANSI標準](https://ja.wikipedia.org/wiki/Category:ANSI標準 "wikilink")

1.  [SMI Timeline](http://www.wbemsolutions.com/tutorials/snia/SMI/Marketing/smi-timeline.html) from SMI Marketing Tutorial
2.  [SMI Tutorials](http://www.wbemsolutions.com/tutorials/snia/) SMI-S 準拠ストレージシステムの開発とマーケティングについて
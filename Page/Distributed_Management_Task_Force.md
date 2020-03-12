> この記事は[Distributed Management Task Force](https://ja.wikipedia.org/wiki/Distributed_Management_Task_Force)から翻訳されています。


**Distributed Management Task Force**（**DMTF**）は、企業やインターネットにおける[IT環境の](../Page/情報技術.md "wikilink")[システム管理](../Page/システム管理.md "wikilink")のための標準を策定・保守する[標準化団体](../Page/標準化団体.md "wikilink")である。当初、"Desktop Management Task Force" と称していた。

## 概要

DMTF は[1992年](../Page/1992年.md "wikilink")に創設された。オープンな団体であり、営利企業でも非営利組織でも個人でも参加できる。[2005年](../Page/2005年.md "wikilink")現在、DMTF には 200 以上の企業や組織から 3500 人が参加している。

DMTF 内でワーキンググループが結成され、標準の策定と保守が行われている。DMTF は他の標準化団体や学会とも連携して標準化作業を行っている。

DMTF が策定した標準は、[プラットフォームに依存しない中立的な](../Page/プラットフォーム_\(コンピューティング\).md "wikilink")[システム管理](../Page/システム管理.md "wikilink")の基盤となっており、各種IT機器間のシステム管理面での相互運用を実現している。

## 主なメンバー企業

団体の取締役企業として[ブロードコム](../Page/ブロードコム.md "wikilink")、[CAテクノロジーズ](../Page/CAテクノロジーズ.md "wikilink")、[デル](../Page/デル.md "wikilink")、[ヒューレット・パッカード](../Page/ヒューレット・パッカード.md "wikilink")、[日立製作所](../Page/日立製作所.md "wikilink")、[インテル](https://ja.wikipedia.org/wiki/インテル "wikilink")、[レノボ](../Page/レノボ.md "wikilink")、[ネットアップ](../Page/ネットアップ.md "wikilink")、、、[VMware](../Page/VMware.md "wikilink")が名を連ねている\[1\]。

## DMTFが策定した標準

  - [Common Information Model](../Page/Common_Information_Model.md "wikilink") (CIM)
    IT環境における管理対象（[コンピュータ](../Page/コンピュータ.md "wikilink")や[ストレージエリアネットワーク](../Page/ストレージエリアネットワーク.md "wikilink")）を共通の[オブジェクトとオブジェクト間の関係で表現する](../Page/オブジェクト_\(プログラミング\).md "wikilink")[概念スキーマ](https://ja.wikipedia.org/wiki/概念スキーマ "wikilink")とその基盤である。実際の機器固有の拡張を施すことが可能となっている。CIM は[UMLに基づいたモデルでスキーマを定義しており](../Page/統一モデリング言語.md "wikilink")、DMTFによる他の標準の基盤となっている。
  - [Common Diagnostic Model](https://ja.wikipedia.org/wiki/Common_Diagnostic_Model "wikilink") (CDM)
    CIMスキーマの一部であり、診断機能と管理基盤との関係を定義している。
  - [Web-Based Enterprise Management](../Page/Web-Based_Enterprise_Management.md "wikilink") (WBEM)
    CIMに基づいたシステム管理基盤コンポーネント間のプロトコル定義。
  - [Systems Management Architecture for Server Hardware](https://ja.wikipedia.org/wiki/Systems_Management_Architecture_for_Server_Hardware "wikilink") (SMASH)
    CIM基盤とやり取りするための[コマンド行プロトコルと](../Page/キャラクタユーザインタフェース.md "wikilink")、サーバハードウェア管理のためのDMTF管理プロファイルが定義されている。
  - [System Management BIOS](../Page/SMBIOS.md "wikilink") (SMBIOS)
    [x86](https://ja.wikipedia.org/wiki/x86 "wikilink")システムの[BIOSインタフェースをCIM](https://ja.wikipedia.org/wiki/Basic_Input/Output_System "wikilink")（とDMI）で表現する方法の定義。
  - [Alert Standard Format](https://ja.wikipedia.org/wiki/Alert_Standard_Format "wikilink") (ASF)
    OSのない環境での遠隔制御と警報インタフェースの定義（例えば、[PCのマザーボードコントローラなど](../Page/パーソナルコンピュータ.md "wikilink")）。
  - Directory enabled networking (DEN)
    CIMで管理される要素に[LDAPディレクトリがアクセスする方法を定義し](../Page/Lightweight_Directory_Access_Protocol.md "wikilink")、CIMスキーマの一部としてCIMからLDAPへのマッピングを定義している。
  - [Desktop Management Interface](../Page/Desktop_Management_Interface.md "wikilink") (DMI)
    最初に定義されたデスクトップ管理標準。CIMなどによる管理技法の発展により、DMTFはDMIの寿命を 2005年3月31日までとした。

## CIM関連標準

DMTF以外で策定された標準として以下のようなものがある。

  - [SNIA](https://ja.wikipedia.org/wiki/SNIA "wikilink") は、[ストレージエリアネットワーク](../Page/ストレージエリアネットワーク.md "wikilink")に関する DMTF 管理プロファイルを定義するものとして **[SMI-S](../Page/SMI-S.md "wikilink")** を策定・保守している。
  - [The Open Group](../Page/The_Open_Group.md "wikilink") は、CIMプロバイダの[C言語](../Page/C言語.md "wikilink")/[C++](../Page/C++.md "wikilink") [API](../Page/アプリケーションプログラミングインタフェース.md "wikilink") として **CMPI** を策定・保守している。
  - [Java Community Process](../Page/Java_Community_Process.md "wikilink") は、CIMクライアントアプリケーションの[Java](https://ja.wikipedia.org/wiki/Java "wikilink")APIとして JSR-48 を策定中。

## CIM/WBEM関連製品など

CIM/WBEM をサポートする製品や[オープンソース](../Page/オープンソース.md "wikilink")プロジェクトとして以下のものがある。

  - **[Windows Management Instrumentation](../Page/Windows_Management_Instrumentation.md "wikilink")** (**WMI**) - [Microsoft Windows](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink") での CIM/WBEM の実装
  - **[SBLIM](http://sblim.sourceforge.net/)** - [Linux](../Page/Linux.md "wikilink")での CIM/WBEM 実装のオープンソースプロジェクト
  - **[OpenPegasus](http://www.openpegasus.org/)** - C++ で書かれた CIM オブジェクトマネージャ（CIMとWBEMの中心となるコンポーネント）のオープンソースプロジェクト
  - **[WBEM Services](http://wbemservices.sourceforge.net/)** - Java で書かれた CIM オブジェクトマネージャのオープンソースプロジェクト
  - **[OpenWBEM](http://openwbem.sourceforge.net/)** - C++ で書かれたもう1つの CIM オブジェクトマネージャのオープンソースプロジェクト

## 脚注

## 外部リンク

  - [DMTF Homepage](http://www.dmtf.org/)

[Category:ネットワーク管理](https://ja.wikipedia.org/wiki/Category:ネットワーク管理 "wikilink") [Category:標準化団体](https://ja.wikipedia.org/wiki/Category:標準化団体 "wikilink")

1.  <https://www.dmtf.org/about>
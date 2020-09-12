> この記事は[Desktop Management Interface](https://ja.wikipedia.org/wiki/Desktop_Management_Interface)から翻訳されています。


**Desktop Management Interface** (DMI) は、[DMTFが](../Page/Distributed_Management_Task_Force.md "wikilink")[リソース情報管理](../Page/計算資源.md "wikilink")[アプリケーションソフトウェア](../Page/アプリケーションソフトウェア.md "wikilink")用に規定した[インタフェース仕様の総称である](../Page/インタフェース_\(情報技術\).md "wikilink")。[企業](../Page/企業.md "wikilink")[情報システム](../Page/情報システム.md "wikilink")を構成する[パーソナルコンピュータ](../Page/パーソナルコンピュータ.md "wikilink")などの資産管理情報、いわゆる「[インベントリ](../Page/インベントリ.md "wikilink")」に関する情報を集中管理する目的で規定された。

## 仕様内容

[リソース情報を管理する為の](../Page/計算資源.md "wikilink")[アプリケーションソフトウェア](../Page/アプリケーションソフトウェア.md "wikilink")を開発する際に使用する。仕様を規定しているのはDMTF ([Distributed Management Task Force](../Page/Distributed_Management_Task_Force.md "wikilink")) で、最新の仕様書は[1998年](https://ja.wikipedia.org/wiki/1998年 "wikilink")[6月](../Page/6月.md "wikilink")に作成された「DMIversion2.0s」である。

DMIでは、特定の[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink")や[ハードウェア](../Page/ハードウェア.md "wikilink")に依存しないこと、既存の[ネットワーク管理](../Page/コンピュータネットワーク.md "wikilink")[プロトコル](../Page/プロトコル.md "wikilink")と組み合わせて利用できる事、管理の対象を容易に指定できること、といった要件を定めている。DMIの構成要素は以下のとおり。

  - DMIを利用して動作するアプリケーションソフトウェア
  - アプリケーションソフトが呼び出す[API](../Page/アプリケーションプログラミングインタフェース.md "wikilink") (MI:Management Interface)
  - [MIF](https://ja.wikipedia.org/wiki/MIF "wikilink")(Management Information Format)で記述された管理情報[データベース](../Page/データベース.md "wikilink")
  - 管理対象の[コンポーネント](https://ja.wikipedia.org/wiki/コンポーネント "wikilink")と管理情報の間のインタフェース (CI:Component Interface)
  - MIとCIの間のインタフェース調停と[データベース](../Page/データベース.md "wikilink")を管理する (SL: Service Layer)

## 目的

DMIにより、管理対象になる「インベントリ」などに関する情報が[データベース](../Page/データベース.md "wikilink")化され、アプリケーションソフトウェアから利用できるようになる。

## 廃止

DMTF は [Common Information Model](../Page/Common_Information_Model.md "wikilink") (CIM) などへの移行を促進するため、DMIの寿命を 2005年3月31日までと定めた\[1\]。

## 出典

## 関連項目

  - [Web-Based Enterprise Management](../Page/Web-Based_Enterprise_Management.md "wikilink") (WBEM)
  - [SMBIOS](../Page/SMBIOS.md "wikilink")

[Category:ネットワーク管理](https://ja.wikipedia.org/wiki/Category:ネットワーク管理 "wikilink")

1.  [DMTF Announces End of Life for DMI](https://web.archive.org/web/20050206074338/http://www.dmtf.org/standards/dmi/self_cert)（2005年2月6日時点の[アーカイブ](../Page/インターネットアーカイブ.md "wikilink")）
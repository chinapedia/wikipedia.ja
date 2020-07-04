> この記事は[XAdES](https://ja.wikipedia.org/wiki/XAdES)から翻訳されています。


**XAdES** (*XML Advanced Electronic Signatures*)は高度電子署名に対応するために行った[XML署名](https://ja.wikipedia.org/wiki/XML署名 "wikilink")への拡張の集合である。

## 説明

[XML署名](https://ja.wikipedia.org/wiki/XML署名 "wikilink")は、[XMLドキュメントに対してデジタル署名を行う汎用的なフレームワークであるが](../Page/Extensible_Markup_Language.md "wikilink")、XAdESはEU電子署名指令1999/93/ECの意味における、適格電子署名(qualified electronic signature)で利用するための[XML署名](https://ja.wikipedia.org/wiki/XML署名 "wikilink")の詳細なプロファイルを規定している。XAdESの一つの重要な利点は、たとえ使用されている暗号アルゴリズムが破られたとしても電子的に署名された文書が長期間において有効であり続けることができるということにある。

## フォーマット

XAdESでは、提供される保護レベルの異なる6つのフォーマットを規定している。

  - **XAdES**, 高度署名(advanced signature)に関する欧州指針を単に満足するための基本フォーマット
  - **XAdES-T** (timestamp), 署名行為の否認に対して保護するために[タイムスタンプ](https://ja.wikipedia.org/wiki/タイムスタンプ "wikilink")を追加する。
  - **XAdES-C** (complete), オフライン検証や将来的な検証ができるように(証明書や[証明書失効リスト](../Page/証明書失効リスト.md "wikilink")などの)検証データへの参照情報を署名文書に追加する。(しかしながら、実際の検証情報は保存しない)
  - **XAdES-X** (extended), 将来、チェーン中の証明書が危殆化する可能性から保護するために、XAdES-Cで導入された参照情報に対してタイムスタンプを追加する。
  - **XAdES-X-L** (extended long-term), 証明書や証明書失効リストの配布元が利用できなくなったとしても、将来検証できるように署名文書に証明書や失効リストそのものを追加する。
  - **XAdES-A** (archival), 長期に渡る保存期間において署名が脆弱になることによる危殆化を避けるために、アーカイブされたドキュメントに対し定期的(例えば毎年)にタイムスタンプを追加する。

## 関連用語

  - [XML署名](https://ja.wikipedia.org/wiki/XML署名 "wikilink")
  - [電子署名](../Page/電子署名.md "wikilink")
  - [欧州電気通信標準化機構](../Page/欧州電気通信標準化機構.md "wikilink")(ETSI)
  - [World Wide Web Consortium(W3C)](../Page/World_Wide_Web_Consortium.md "wikilink")
  - [日本工業規格の一覧](https://ja.wikipedia.org/wiki/日本工業規格の一覧 "wikilink")
  - [CAdES](https://ja.wikipedia.org/wiki/CAdES "wikilink"), CMS Advanced Electronic Signature
  - [PAdES](https://ja.wikipedia.org/wiki/PAdES "wikilink"), PDF Advanced Electronic Signature

## 外部リンク

  - [W3C Note XML Advanced Electronic Signatures (XAdES), 20 Feb 2003](http://www.w3.org/TR/XAdES/) version 1.1.1 from 2003
  - [ETSI TS 101 903 XAdES](http://webapp.etsi.org/workprogram/Report_WorkItem.asp?WKI_ID=20533) version 1.2.2 from 2004
  - [ETSI TS 101 903 XAdES](http://webapp.etsi.org/workprogram/Report_WorkItem.asp?WKI_ID=21353) version 1.3.2 from 2006-03
  - [OpenXAdES](http://www.openxades.org/)

[Category:XML](https://ja.wikipedia.org/wiki/Category:XML "wikilink") [Category:暗号技術](https://ja.wikipedia.org/wiki/Category:暗号技術 "wikilink") [Category:コンピュータ・ネットワーク・セキュリティ](https://ja.wikipedia.org/wiki/Category:コンピュータ・ネットワーク・セキュリティ "wikilink") [Category:XMLベースの技術](https://ja.wikipedia.org/wiki/Category:XMLベースの技術 "wikilink")
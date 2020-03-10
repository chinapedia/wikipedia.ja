> この記事は[BioAPI](https://ja.wikipedia.org/wiki/BioAPI)から翻訳されています。


**BioAPI**（**Biometric Application Programming Interface**、バイオエーピーアイまたはバイオアピー） は、[生体認証](https://ja.wikipedia.org/wiki/生体認証 "wikilink")([バイオメトリクス](https://ja.wikipedia.org/wiki/バイオメトリクス "wikilink")認証)に関連する[アプリケーションのプログラミングインタフェース仕様の](../Page/アプリケーションプログラミングインタフェース.md "wikilink")[国際標準規格](https://ja.wikipedia.org/wiki/国際標準規格 "wikilink")。

## 経緯

1990年代前半以前のバイオメトリクス認証業界は、まだ市場が未成熟でスタンドアローン運用が主体であったため、APIの互換性は全く考慮されていなかった。

1990年代後半頃になると、市場の拡大により応用製品が増えてきて、ベンダーの異なる応用製品を相互運用できる様にするため、幾つかの汎用APIが発表された。HA-API(Human Authentication API)、BAPI(Biometric API)等である。

その後、[米国標準技術局](https://ja.wikipedia.org/wiki/アメリカ国立標準技術研究所 "wikilink")(NIST)がサポートする業界団体[BioAPIコンソーシアム](https://ja.wikipedia.org/wiki/BioAPIコンソーシアム "wikilink")により、それら汎用APIを統合するBioAPIの開発が始まった。また2001年の[アメリカ同時多発テロ事件](https://ja.wikipedia.org/wiki/アメリカ同時多発テロ事件 "wikilink")をうけて米国においてホームランドセキュリティ強化の機運が高まり、これが標準化作業を加速する一因となった。 この様にして開発されたBioAPI 1.1は2002年に[ANSI](https://ja.wikipedia.org/wiki/ANSI "wikilink")規格として発行された。(ANSI/INCITS 358-2002)

その後、BioAPIを国際標準とするため[ISO/IEC JTC 1](https://ja.wikipedia.org/wiki/ISO/IEC_JTC_1 "wikilink")/SC 37/WG 2に作業が移管された。BioAPIを国際標準の場に持ち込んだ米国はファストトラック手順(迅速手順)によりBioAPI 1.1をそのままの形で早期に国際標準にすることを目指したが、結局はBioAPI 1.1を叩き台として改めて仕様を練り直すことになった。 こうして開発されたBioAPI 2.0は2006年にISO/IEC規格として発行された。

現在も仕様の改訂や多数の関連仕様の開発がSC 37/WG 2で進められている。

## BioAPI 1.1 (ANSI規格)

ANSI/NISTが発行するアメリカ国内ローカル規格。

3階層構造（アプリケーション層、フレームワーク層、サービスプロバイダ層）を採用する。

BioAPI 1.1の仕様の不具合を修正したBioAPI 1.2と称するバージョンのサンプルソースコードがBioAPIコンソーシアムのウェブサイトに存在するが、このバージョンは正式に発行されたものではない。

## BioAPI 2.x (ISO/IEC規格)

ISO/IECが発行する国際規格。

4階層構造（アプリケーション層、フレームワーク層、サービスプロバイダ層、ファンクションプロバイダ層）を採用する。

BioAPI 2.0 は BioAPI 1.1 をベースに様々な改良を施して策定されたものであり、基本的な枠組みや主要な関数やデータ構造の定義はよく似ているが、細かい部分ではきわめて多数の相違点が存在する。このため、ソースレベルにおいてもバイナリレベルにおいても、両バージョン間の相互互換性は無い。

### BioAPI 2.0

  - ISO/IEC 19784-1:2006
    BioAPI Part 1: BioAPI specification「BioAPI 2.0仕様書」

<!-- end list -->

  - ISO/IEC 19784-2:2007
    BioAPI Part 2: Biometric archive function provider interface (BAFPI)「生体認証アーカイブ機能プロバイダインタフェース」
    BioAPIのデータベース管理機能のみをモジュール化して独立させるためのAPI。

### BioAPI 2.1

BioAPI 2.0にGUI関連など幾つかの修正を加えた仕様。

  - ISO/IEC 19784-1:2006/Amd 1:2007
    BioGUI specification「BioGUI仕様書」
    (この仕様書は追補仕様なのでBioAPI 2.0からの差分のみが記載されている)

### BioAPI 2.2

Framework-Free BioAPI と呼ばれるサブセット仕様。

フレームワーク層を飛ばして、アプリケーション層からサービスプロバイダ層を直接呼び出せる様に仕様を簡易化したもの。

  - ISO/IEC 19784-1:2006/Amd 2:2009
    Framework-free BioAPI Specification
    (この仕様書は追補仕様なのでBioAPI 2.1からの差分のみが記載されている)

### BioAPI 2.3

[ACBio](https://ja.wikipedia.org/wiki/ACBio "wikilink")などセキュリティに関する仕様を追加したもの。 現時点では未発行。

## 関連する国際標準規格

### Conformance testing for BioAPI

BioAPIのための適合性試験

  - ISO/IEC 24709-1:2007
    Part 1: Methods and procedures「方法及び手順」

<!-- end list -->

  - ISO/IEC 24709-2:2007
    Part 2: Test assertions for biometric service providers「生体認証サービス提供者(BSP)のための試験仕様」

### CBEFF

共通生体認証交換フォーマットフレームワーク(Common Biometric Exchange Formats Framework)。 生体認証に用いる様々なデータをプラットフォームに依存せずに交換するためのデータフォーマットを定義する。 ただし、CBEFFはあらゆる生体認証に共通するヘッダー情報と枠組み(SBH,BDB,SB)を定義するのみで、個々の生体特徴に固有の情報はISO/IEC 19794シリーズにて定義される。

  - ISO/IEC 19785-1:2006
    Part 1: Data element specification 「データ要素(ヘッダー情報)仕様」
    ヘッダーに記載すべき要素などが定義されているだけで、具体的なフォーマットはPart 3に記述される。

<!-- end list -->

  - ISO/IEC 19785-2:2006
    Part 2: Procedures for the operation of the Biometric Registration Authority「生体認証登録当局の運用の手順」

<!-- end list -->

  - ISO/IEC 19785-3:2007
    Part 3: Patron format specifications「パトロンフォーマット仕様」
    ヘッダーの具体的なフォーマットを定義。

### Biometric Data Interchange Formats

ISO/IEC 19794シリーズは、指紋・顔・虹彩・静脈など個々の生体特徴に固有のフォーマット定義である。 CBEFF(ISO/IEC 19785シリーズ)ではブラックボックスとして扱っているBDBの中身を具体的に定義する。

  - ISO/IEC 19794-1:2006
    Part 1: Framework「第1部：フレームワーク」

<!-- end list -->

  - ISO/IEC 19794-2:2005
    Part 2: Finger minutiae data「第2部：指紋 特徴データ」

<!-- end list -->

  - ISO/IEC 19794-3:2006
    Part 3: Finger pattern spectral data「第3部：指紋 パターンスペクトルデータ」

<!-- end list -->

  - ISO/IEC 19794-4:2005
    Part 4: Finger image data「第4部：指紋 画像データ」

<!-- end list -->

  - ISO/IEC 19794-5:2005
    Part 5: Face image data「第5部：顔 画像データ」

<!-- end list -->

  - ISO/IEC 19794-6:2005
    Part 6: Iris image data「第6部：虹彩 画像データ」

<!-- end list -->

  - ISO/IEC 19794-8:2006
    Part 8: Finger pattern skeletal data「第8部：指紋 骨格データ」

<!-- end list -->

  - ISO/IEC 19794-9:2007
    Part 9: Vascular image data「第9部：血管(静脈) 画像データ」

## 外部リンク

  - 　[BioAPI Consortium](http://www.bioapi.org/)
  - 　[IBIA(International Biometric Industry Association)](http://www.ibia.org/)

## 関連項目

  - [生体認証](https://ja.wikipedia.org/wiki/生体認証 "wikilink")

[Category:生体認証](https://ja.wikipedia.org/wiki/Category:生体認証 "wikilink") [Category:認証技術](https://ja.wikipedia.org/wiki/Category:認証技術 "wikilink") [Category:ISO/IEC標準](https://ja.wikipedia.org/wiki/Category:ISO/IEC標準 "wikilink") [Category:情報セキュリティの規格と制度](https://ja.wikipedia.org/wiki/Category:情報セキュリティの規格と制度 "wikilink")
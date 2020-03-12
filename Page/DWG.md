> この記事は[DWG](https://ja.wikipedia.org/wiki/DWG)から翻訳されています。


**DWG**（ディー・ダブル・ジー）は、[オートデスク](../Page/オートデスク.md "wikilink")社製の[CAD](../Page/CAD.md "wikilink")[ソフトウェア](../Page/ソフトウェア.md "wikilink")、[AutoCAD](../Page/AutoCAD.md "wikilink")の標準[ファイル形式](../Page/ファイルフォーマット.md "wikilink")。**d**ra**w**in**g**の略。[拡張子](../Page/拡張子.md "wikilink")として"dwg"を用いる。

## 概要

DWGはオートデスク社が策定する図面ファイル形式である。[AutoCAD](../Page/AutoCAD.md "wikilink")シリーズ（AutoCAD LT、AutoCAD Mechanicalなど）の標準ファイル形式として開発されたことから、AutoCADと共に業界の[デファクトスタンダード](../Page/デファクトスタンダード.md "wikilink")として利用されている。

その仕様は非公開であるため、ネイティブ対応しているのはオートデスク社製品および同社ライセンス製品のみである。一方で、DWGのリバースエンジニアリングの成果として提供される[ソフトウェア開発キット](../Page/ソフトウェア開発キット.md "wikilink")[DWGdirect](https://ja.wikipedia.org/wiki/DWGdirect "wikilink")によってDWGの読み書きを実現する互換CAD製品が数多く存在する。

DWGとは別に、他のCADソフトウェアとのファイル交換を容易にするため、オートデスクが定義した形式が**[DXF](https://ja.wikipedia.org/wiki/DXF "wikilink")**（AutoCADファイル交換形式）である。DXFは公開された仕様と可読性の高いテキスト形式（バイナリ形式に圧縮することも可能）という特徴により、サポートするサードパーティ製のソフトウェアも開発しやすくなっている。ただし、仕様の解釈やデータ構造の違いによって、CADソフトウェア間（Autodesk製品間を除く）で図面の再現が完全に実現できないケースも目立っている。

## ファイルに含まれる情報

DWG形式のファイルには以下のような情報が含まれる。

  - グラフィカルデータ（エンティティ、図形情報）
    3DFACE（3D 面）、3DSOLID（3D ソリッド）、ACAD_PROXY_ENTITY（ACAD プロキシ図形）、ARC（円弧）、ATTDEF（属性定義）、ATTRIB（属性）、BODY（ボディ）、CIRCLE（円）、DIMENSION（寸法）、ELLIPSE（楕円）、HATCH（ハッチング）、HELIX（らせん）、IMAGE（イメージ）、INSERT（ブロック挿入）、LEADER（引出線）、LIGHT（光源）、LINE（線分）、LWPOLYLINE（ライト ウェイト ポリライン）、MESH（メッシュ）、MLINE（マルチライン）、MLEADER（マルチ引出線）、MLEADERSTYLE（マルチ引出線スタイル）、MTEXT（マルチテキスト）、OLEFRAME（OLE フレーム）、OLE2FRAME（OLE2 フレーム）、POINT（点）、POLYLINE（ポリライン）、RAY（放射線）、REGION（リージョン）、SECTION（断面）、SEQEND（シーケンス終了）、SHAPE（シェイプ）、SOLID（2D 塗り潰し）、SPLINE（スプライン）、SUN（日照）、SURFACE（サーフェス）、TABLE（表）、TEXT（文字）、TOLERANCE（幾何交差）、TRACE（太線）、UNDERLAY（アンダーレイ）、VERTEX（頂点）、VIEWPORT（ビューポート）、WIPEOUT（ワイプアウト）、XLINE（構築線）
  - 非グラフィカルデータ（格納テーブル情報）
    APPID（アプリケーション ID）、BLOCK_RECORD（ブロック レコード）、DIMSTYLE（寸法スタイル）、LAYER（画層）、LTYPE（線種）、STYLE（文字スタイル）、UCS（ユーザ座標系）、VIEW（ビュー）、VPORT（ビューポート）
  - 非グラフィカルデータ（標準ディクショナリ、拡張レコード情報）
    ACAD_PROXY_OBJECT（ACAD プロキシ オブジェクト）、DATATABLE（データ テーブル）、DICTIONARY（ディクショナリ）、DICTIONARYVAR（ディクショナリ変数）、DIMASSOC（自動調整管理）、FIELD（フィールド）、GEODATA（地理的データ）、GROUP（グループ）、IDBUFFER（ID バッファ）、IMAGEDEF（イメージ定義）、IMAGEDEF_REACTOR（イメージ定義リアクタ）、LAYER_INDEX（画層インデックス）、LAYER_FILTER（画層フィルタ）、LAYOUT（レイアウト）、LIGHTLIST（光源一覧）、MATERIAL（マテリアル）、MLINESTYLE（マルチライン スタイル）、OBJECT_PTR（オブジェクト プリンタ）、PLOTSETTINGS（印刷設定）、RASTERVARIABLES（ラスター変数）、RENDER（レンダリング）、SECTION（断面）、SPATIAL_INDEX（空間インデックス）、SPATIAL_FILTER（空間フィルタ）、SORTENTSTABLE（SORTENTS テーブル）、TABLESTYLE（表スタイル）、UNDERLAYDEFINITION（アンダーレイ定義）、VISUALSTYLE（表示スタイル）、VBA_PROJECT（VBA プロジェクト）、WIPEOUTVARIABLES（WIPEOUT 変数）、XRECORD（拡張レコード）
  - その他の[メタデータ](../Page/メタデータ.md "wikilink")
    作成日時、図面編集時間、作者、タイトルなどの図面のプロパティ、図面を開く際の[パスワード](../Page/パスワード.md "wikilink")、図面への[デジタル署名](../Page/デジタル署名.md "wikilink")、サムネール画像(bmp)

また、AutoCADが標準で含む情報以外にも、アドオンアプリケーション（[プラグイン](../Page/プラグイン.md "wikilink")ソフトウェア）が任意に拡張情報を付加できるため、拡張エンティティデータや拡張レコード、カスタム・オブジェクトなどが含まれることがある。

なお、DWGのバージョンによっては含まれないデータもあるので注意が必要である。

## バージョン

DWG形式はAutoCADと共にバージョンアップを重ねている。

AutoCADやその互換製品は一般に[後方互換性](https://ja.wikipedia.org/wiki/後方互換性 "wikilink")を備えているため古いバージョンのDWGファイルを扱えるが、[前方互換性](https://ja.wikipedia.org/wiki/前方互換性 "wikilink")はないため新しいバージョンのDWGファイルを扱うことはできない。

DWG形式の各バージョンは、AutoCADのリリースバージョンか、ファイルの先頭6文字の識別コードで区別される\[1\]\[2\]。

| AutoCADバージョン（日本発売名称）                         | DWGバージョン      | 識別コード  |
| -------------------------------------------- | ------------- | ------ |
| AutoCAD 2018                                 | 2018/LT2018   | AC1032 |
| AutoCAD 2013 / 2014 / 2015 / 2016 / 2017     | 2013/LT2013   | AC1027 |
| AutoCAD 2010 / 2011 / 2012                   | 2010/LT2010   | AC1024 |
| AutoCAD 2007 / 2008 / 2009                   | 2007/LT2007   | AC1021 |
| AutoCAD 2004 / 2005 / 2006                   | 2004/LT2004   | AC1018 |
| AutoCAD 2000 / 2000i / 2002                  | 2000/LT2000   | AC1015 |
| AutoCAD Release 14 (14J) / LT98 / LT97       | R14/LT98/LT97 | AC1014 |
| AutoCAD Release 13 (13J) / LT95              | R13/LT95      | AC1012 |
| AutoCAD Release 11 (GX-5) / Release 12 (12J) | R11/R12       | AC1009 |
| AutoCAD Release 10 (GX-III)                  | R10           | AC1006 |
| AutoCAD Release 9（日本未発売）                     | R9            | AC1004 |
| AutoCAD Version 2.6 (EX-II)                  | R2.6          | AC1003 |
| AutoCAD Version 2.5 (ADE-3EX)                | R2.5          | AC1002 |
| AutoCAD Version 2.1 (ADE-3)                  | R2.1          | \-     |
| AutoCAD Version 2.0 (2)                      | R2.05         | \-     |

AutoCAD バージョンと DWG 形式の対比

## サポート製品

AutoCADとAutoCADをベースとする業種別製品（AutoCAD Architecture、AutoCAD Mechanical、AutoCAD Electrical、AutoCAD Civil 3D、AutoCAD Map 3D、AutoCAD P\&ID）、AutoCAD LT が、[ネイティブ](https://ja.wikipedia.org/wiki/ネイティブ "wikilink")にDWG形式へのファイル保存と読み込みをサポートする。また、AutoCADとは異なる[アーキテクチャ](../Page/アーキテクチャ.md "wikilink")を持つAutodesk Inventor、Autodesk Revit、Autodesk 3ds Maxといった他のオートデスク社の製品も、DWG形式でのファイルの読み込みと書き出しをサポートしている。これらCAD製品とは別に、DWG形式のファイルを閲覧するためのビューアソフトウェアとして、オートデスク社は[DWG TrueView](http://www.autodesk.co.jp/dwgtrueview)を無償で配布している。

他のCADソフトウェアでは、AutoCAD互換の[IntelliCAD](https://ja.wikipedia.org/wiki/IntelliCAD "wikilink")やIntelliCADをベースとする[Bricscad](https://ja.wikipedia.org/wiki/Bricscad "wikilink")、[ZWCAD](https://ja.wikipedia.org/wiki/ZWCAD "wikilink")もDWG形式をサポートしている。これらのCADソフトウェアは、[Open Design Alliance](http://www.opendesign.com/)（英語）によって設立された[IntelliCAD Technology Consortium](http://www.intellicad.org/)（英語）が[オープンソース](../Page/オープンソース.md "wikilink")化している。

CAD以外のソフトウェアでは、[Adobe](../Page/アドビシステムズ.md "wikilink") [Illustratorのバージョン](../Page/Adobe_Illustrator.md "wikilink")9以降、[Microsoft VisioなどもDWG形式のファイルの読み書きが可能である](../Page/Microsoft_Visio.md "wikilink")。

このようなソフトウェアや、IntelliCAD以外の国産CADは、[Open Design Alliance](http://www.opendesign.com/)（英語）がDWGファイルの[リバースエンジニアリング](../Page/リバースエンジニアリング.md "wikilink")によって作成・提供している[ソフトウェア開発キット](../Page/ソフトウェア開発キット.md "wikilink")[DWGdirect](https://ja.wikipedia.org/wiki/DWGdirect "wikilink")によって、DWG形式の読み書きを実装しているケースが多い。

オートデスク社は、自社製品のDWG形式の入出力に[ソフトウェア開発キット](../Page/ソフトウェア開発キット.md "wikilink") [RealDWG](http://www.autodesk.co.jp/realdwg)を利用しており、サードパーティにもライセンス供与している。

## TrustedDWG

オートデスク社は、AutoCADが実行中に [クラッシュした場合](https://ja.wikipedia.org/wiki/クラッシュ_\(コンピュータ\) "wikilink")、メモリの状況をサーバーに自動送信するCustomer Error Reporting機能があり、この機能によって蓄積した情報を解析したところ、下位バージョン互換のケースとは別に、オートデスク製の製品以外から保存されたDWGファイルには、データ構造上に欠損のあるものがあり、編集中のCADソフトウェアを不安定にするケースが報告されている、としている。

このため、AutoCAD 2007以降のAutoCADでは、オートデスク社製品から保存されたDWGファイルを **TrustedDWG**として区別するようになっている。オートデスク社のCADソフトウェアや、オートデスクがライセンス供与した[RealDWG](http://www.autodesk.co.jp/realdwg)や[AutoCAD OEM](http://www.autodesk.co.jp/developoem)を使ったソフトウェア製品以外が保存したDWGファイルを開こうとすると、警告メッセージが表示されるようになっている。

オートデスク社によれば、RealDWGやAutoCAD OEMは、競合するCADベンダーやサードパーティには供与されないとなっている。

## 脚注

## 関連項目

  - [AutoCAD](../Page/AutoCAD.md "wikilink")
  - [DWF](https://ja.wikipedia.org/wiki/DWF "wikilink")
  - [DWGdirect](https://ja.wikipedia.org/wiki/DWGdirect "wikilink")
  - [DXF](https://ja.wikipedia.org/wiki/DXF "wikilink")
  - [MCD](https://ja.wikipedia.org/wiki/MCD "wikilink")

## 外部リンク

  - [オートデスク](http://www.autodesk.co.jp/)
  - [信頼できるDWG](http://www.autodesk.co.jp/dwg)
  - [RealDWG](http://www.autodesk.co.jp/realdwg)
  - [AutoCAD OEM](http://www.autodesk.co.jp/developoem)
  - [DWGSee JP](http://www.autodwg.com/dwg-viewer/dwg_viewer_jp.htm)
  - [.DWG File Extension](http://www.fileinfo.com/extension/dwg)
  - [Between the Lines: AutoCAD Release History](http://autodesk.blogs.com/between_the_lines/autocad-release-history.html)

[Category:オートデスク](https://ja.wikipedia.org/wiki/Category:オートデスク "wikilink") [Category:CADファイルフォーマット](https://ja.wikipedia.org/wiki/Category:CADファイルフォーマット "wikilink")

1.  [DWG ファイルを開かずに保存バージョンを確認する方法はありますか | AutoCAD | Autodesk Knowledge Network](https://knowledge.autodesk.com/ja/support/autocad/troubleshooting/caas/sfdcarticles/sfdcarticles/kA230000000u0Sv.html)
2.  [Help:Autodesk.AutoCAD.DatabaseServices.DwgVersion Enumeration](http://help.autodesk.com/view/OARX/2018/ENU/?guid=OREFNET-Autodesk_AutoCAD_DatabaseServices_DwgVersion)
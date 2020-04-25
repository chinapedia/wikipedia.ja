> この記事は[BOM \(部品表\)](https://ja.wikipedia.org/wiki/BOM_\(部品表\))から翻訳されています。


**BOM**（）とは、[製造業](../Page/製造業.md "wikilink")で用いられる部品表の一形態である。[製品](../Page/製品.md "wikilink")を組み立てる時の[部品](https://ja.wikipedia.org/wiki/部品 "wikilink")の一覧と、場合によっては[階層構造](../Page/階層構造.md "wikilink")を表す。製品の[見積](../Page/見積.md "wikilink")もり時点から、[設計](../Page/設計.md "wikilink")、[調達](https://ja.wikipedia.org/wiki/調達 "wikilink")、[製造](https://ja.wikipedia.org/wiki/製造 "wikilink")、[メンテナンス](../Page/メンテナンス.md "wikilink")にまで利用され、多岐にわたる近年の[ものづくり](../Page/ものづくり.md "wikilink")において、BOMは極めて重要である。

## 種類

BOMは、[業種](../Page/業種.md "wikilink")、[業態](../Page/業態.md "wikilink")によって様々な形態があるが、[企業](../Page/企業.md "wikilink")によっては、以下のようなBOMが作成されることがある。パーツリスト(P/L: Parts List)は、設計BOM、製造BOM、サービスBOMに該当する。

  - マスターBOM
    以下のBOMを総括するBOM。設計から製造、購買、[保守サービスまでを構成する](../Page/メンテナンス.md "wikilink")。故に[データベース](../Page/データベース.md "wikilink")は時として非常に巨大なものとなる。以下のBOMを作成しない企業の場合、このマスターBOMを単にBOMや、[部材マスターなどと呼ぶことがある](https://ja.wikipedia.org/wiki/材料 "wikilink")。
  - 設計BOM（E-BOM）
    設計部門が設計を行う場合に用いるBOM。最終製品が出来上がる為に必要となる部品の構成と数量が全て網羅されている。形としてはフラット型と階層型がある。設計者は顧客の求める機能を製品に反映させる為、E-BOMにおける階層型は機能としての分類がなされているのが通常である。従ってE-BOMには製造する為の情報は含まれないことになる。[定格](../Page/定格.md "wikilink")値や[誤差](../Page/誤差.md "wikilink")、機能の詳細などの技術情報や仕様、代替可能部品などの情報が判るようにサポートされていることがある。M-BOMの前段階で作製される。
  - 製造BOM（M-BOM）
    製造部門が製造、組み立てを行う場合に用いるBOM。生産に必要になる部品総数などを正確に把握する為に、組み立てに使用される[ユニット](../Page/ユニット.md "wikilink")や[基板](../Page/基板.md "wikilink")単位に構成される。製造は設計で造られたE-BOMを基に行われるが、E-BOMには製造方法が入っていない為、一般的には[生産技術](../Page/生産技術.md "wikilink")などと言った部門でどの[工程](https://ja.wikipedia.org/wiki/工程 "wikilink")を流して製造させるか決めた上で[製造ラインにのせる事になる](../Page/ライン生産方式.md "wikilink")。この際E-BOMの機能中心で出来た階層構造と実際に生産する[親子](../Page/親子.md "wikilink")構成が全く違ってくるのが一般的である。組み立ての際に作業しやすいように組み立て順に番号が振られていることがある。
  - 購買BOM
    購買部門が発注を行う場合に用いるBOM。発注作業に不要な部分（組立配線や基板実装に必要なロケーション番号）は使用されず、見積・発注作業に必要な、購入単位数量や、仕入先ごとの購入価格リスト、代替品種のリストなどをサポートしていることがある。
  - サービスBOM
    製品サービス、保守メンテナンスを行う際に用いるBOM。メンテナンスに便利な様に、よく[消耗する部品](https://ja.wikipedia.org/wiki/消耗品 "wikilink")（[Oリング](../Page/Oリング.md "wikilink")や[グリース](https://ja.wikipedia.org/wiki/グリース "wikilink")、[電力ヒューズ](../Page/電力ヒューズ.md "wikilink")、[感熱紙](../Page/感熱紙.md "wikilink")のロールペーパーなど）を特に取り上げている。

## BOMを構成する要素

以下のような内容で構成される。

  - 品名
      -
        一目で内容が理解できるもので、簡単に表記されることが多い。
        例：前面パネル、[ねじ](../Page/ねじ.md "wikilink")、熱収縮チューブ、[LED](https://ja.wikipedia.org/wiki/LED "wikilink")、[FPGA](../Page/FPGA.md "wikilink")、[プリント基板](../Page/プリント基板.md "wikilink")（PWB）、[A4](../Page/紙の寸法.md "wikilink")[ファイルなど](../Page/ファイル_\(文具\).md "wikilink")
  - 型式
      -
        品名では表示しきれない、部材そのものを特定できる型式を指す。大抵は40文字以内に収まるが、時には70文字を超える事もある。
        例：熱収縮チューブならSUMITUBE F(Z) 8[ファイなど](https://ja.wikipedia.org/wiki/径#直径記号 "wikilink")、[LEDならTLR](../Page/発光ダイオード.md "wikilink")123など、A4ファイルなら975Gなど
  - メーカー名
      -
        製品を製造しているメーカー名。
  - 数量
      -
        数量項目は、設計、製造、購買のBOMで利用される。
    <!-- end list -->
      - 使用数量
          -
            1ユニット（パネルや基板）単位に使用される部材の数を示す。
      - 購入単位数量
          -
            ある部材を購入しようとしたとき購入の単位になる数量を示す。
  - [ロケーション](https://ja.wikipedia.org/wiki/ロケーション "wikilink")番号
      -
        プリント基板の場合、部品を実装する場所を示した[シルクと対になる関係にある](../Page/シルクスクリーン.md "wikilink")。[リファレンス](https://ja.wikipedia.org/wiki/リファレンス "wikilink")番号などと呼ばれることもある。
        例：[抵抗器](../Page/抵抗器.md "wikilink")の場合R1など
  - 仕様
      -
        購入仕様書番号や、納入仕様書番号、[JIS規格番号が入力されている](https://ja.wikipedia.org/wiki/日本工業規格 "wikilink")。
        抵抗器や、[コンデンサ](../Page/コンデンサ.md "wikilink")の場合、定格、値、誤差、[チップ](../Page/チップ.md "wikilink")[サイズなど](https://ja.wikipedia.org/wiki/寸法 "wikilink")
        ねじの場合、JIS B 0205など
  - 材質
      -
        部材を主として構成する材質をあらわす。
        [金属](../Page/金属.md "wikilink")[加工](https://ja.wikipedia.org/wiki/加工 "wikilink")部品などの場合[SUS304など](https://ja.wikipedia.org/wiki/ステンレス "wikilink")、[樹脂成形品の場合は](../Page/射出成形.md "wikilink")[ABSなど](../Page/ABS樹脂.md "wikilink")

## 関連項目

  - [生産管理](../Page/生産管理.md "wikilink")
  - [メンテナンス](../Page/メンテナンス.md "wikilink")
  - [部品](https://ja.wikipedia.org/wiki/部品 "wikilink")
  - [ロット管理](../Page/ロット管理.md "wikilink")
  - [PDM](../Page/製品情報管理.md "wikilink")

[Category:製造](https://ja.wikipedia.org/wiki/Category:製造 "wikilink")
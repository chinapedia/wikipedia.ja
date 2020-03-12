> この記事は[CiRCUS](https://ja.wikipedia.org/wiki/CiRCUS)から翻訳されています。


**CiRCUS**（サーカス、treasure **C**asket of **i**-mode service, high **R**eliability platform for **CUS**tomer）は、[NTTドコモ](https://ja.wikipedia.org/wiki/NTTドコモ "wikilink")の[メール送受信](../Page/電子メール.md "wikilink")/配信システムおよび[iモード](https://ja.wikipedia.org/wiki/iモード "wikilink")ゲートウェイシステムである。ドコモ[川崎](https://ja.wikipedia.org/wiki/川崎 "wikilink")オフィス内にあり、4600平方メートルの敷地に[日本電気](../Page/日本電気.md "wikilink")（NEC） NX7000 [HP-UX](../Page/HP-UX.md "wikilink")が約600台ある。

[日経コンピュータ2007年7月23日版の特集](http://itpro.nikkeibp.co.jp/article/NC/20070713/277556/)で、本システムの耐高負荷の堅牢さが評価されている。

## 概要/性能

性能面では[Webサイト参照](../Page/ウェブサイト.md "wikilink")5万件/秒、メール送受信2万5千件/秒の処理能力を有し、信頼面は国内にメインセンターと[バックアップ](../Page/バックアップ.md "wikilink")センターを備え、各構成要素がすべて[冗長化](../Page/冗長化.md "wikilink")されていることで、稼働率は99.99998パーセントでユーザ1人当たりの年間停止時間は6.93秒である。

都内のオペレーションセンター「**CARNiVAL**（カーニバル、**CAR**ing for the **N**ew **i**-mode **VAL**ue-platform 24hours-a-day）」で、24時間365日体制で運用されている。

NEC/[ヒューレット・パッカード](../Page/ヒューレット・パッカード.md "wikilink")が[協業して](../Page/アライアンス.md "wikilink")、NEC/[NTTデータ](../Page/NTTデータ.md "wikilink")とイコールパートナとして[統合され](../Page/システムインテグレーション.md "wikilink")、HP-UXサーバ600台と[EMCのストレージを主軸に構築されている](https://ja.wikipedia.org/wiki/EMCコーポレーション "wikilink")。

[2006年](../Page/2006年.md "wikilink")3月に、[2006年](../Page/2006年.md "wikilink")1月1日時点のiモード加入者数4568万人、が世界最大のワイヤレス[プロバイダ](https://ja.wikipedia.org/wiki/プロバイダ "wikilink")として[ギネスブックに認定された](https://ja.wikipedia.org/wiki/ギネス・ワールド・レコーズ "wikilink")。

## 経緯

ドコモは[通商産業省の](../Page/経済産業省.md "wikilink")[Σプロジェクト](../Page/Σプロジェクト.md "wikilink")制定に関わった[NTTと](../Page/NTTグループ.md "wikilink")[NTTデータ](../Page/NTTデータ.md "wikilink")に関連し、[サン・マイクロシステムズ](../Page/サン・マイクロシステムズ.md "wikilink")の[Solaris](../Page/Solaris.md "wikilink")など[UNIX](../Page/UNIX.md "wikilink")の[SVR4を優先的に使用してきた](../Page/UNIX_System_V.md "wikilink")。

[1999年](../Page/1999年.md "wikilink")2月に運用を開始したサン/[伊藤忠テクノサイエンスによる第](../Page/伊藤忠テクノソリューションズ.md "wikilink")1世代ゲートウェイ「**GRIMM**（グリム、**G**ateway Service **R**epresentative **I**nternet **M**arket **M**obile Access Exchange）」システムは、すでに7月に通信障害を生じ、[2000年](../Page/2000年.md "wikilink")3月28日に全国規模で接続不能で端末600万台が影響し、4月以降は不安定度を増して障害が続発して新聞主要各紙の1面で取り上げられ、国会でも質問された。

GRIMMの障害状況と改善されない運用に痺れを切らしたドコモは、数十億円を投じたシステムの破棄を決定して多くの[SIerに提案を要求した](../Page/システムインテグレーター.md "wikilink")。機能面を重視した入札の結果、NECとNTTデータによるHPサーバを使用した次世代ゲートウェイシステムの構築が決定され、システム検討と構築は1年間と短期間だが無事に運用を開始した。

実際の基盤設計や要件定義以降は、NEC[府中にあるUNIX](../Page/府中市_\(東京都\).md "wikilink")、特にHP-UXの技術を持つ部門から中核を担う人間が設計し、[MC/ServiceGuard](https://ja.wikipedia.org/wiki/MC/ServiceGuard "wikilink")や[LVMといった高負荷用パッケージを担当する主任技術職らも尽力した](../Page/論理ボリュームマネージャ.md "wikilink")。

GRIMMとCIRCUSは、サンとHPのサーバに対する基本設計、NECと伊藤忠テクノサイエンスのシステム構築や運用に関する経験値、がそれぞれ異なる。

| \-           | GRIMM （サン/CTC）                                                    | CiRCUS （HP/NTTデータ・NEC）                                                             |
| ------------ | ----------------------------------------------------------------- | ---------------------------------------------------------------------------------- |
| 設計思想         | 中小規模のシステムにおいて最大の効果を狙う                                             | 大規模システムでの運用を中心とする                                                                  |
| ハードウェアの信頼性   | 中規模上位･大規模エントリーモデルのハードウェア障害が多発                                     | 少々コストが高いが、ハードウェアの信頼性が高い                                                            |
| OSの実装/信頼性    | Solarisには標準LVMが無い。 （[VERITAS](../Page/VERITAS.md "wikilink")製を購入） | HP-UX用LVMを標準実装。 （HPがVERITAS製LVMを[ソースレベルで購入し](../Page/ソースコード.md "wikilink")、完全社製品化） |
| OSの改修や対応     | 標準のSolarisを使用。                                                    | HPのアライアンスによりHP-UX 11iを開発・先行投入。最優先で対応。 （11iのiはinternet-enabledのi）                   |
| クラスタパッケージ    | VCSによる（大規模システムの実績が乏しい）                                            | MC/ServiceGuardによる（大規模システムの実績が豊富）                                                  |
| 大規模システムの構築経験 | 少ない                                                               | [汎用機](https://ja.wikipedia.org/wiki/汎用機 "wikilink")からの蓄積経験あり                       |

**GRIMMとCiRCUSの比較**

## 海外展開

ドコモは本システムの普遍化を図り、iモードシステムを海外へ有償で展開するために複数の海外携帯キャリアへ投資したが、[3Gインフラの高額さなどから採用数増加は得られなかった](../Page/第3世代移動通信システム.md "wikilink")。後に無償化して、iモードとCiRCUSシステムの廉価版がドイツ、オランダ、ベルギー、フランス、スペイン、台湾、イタリア、ギリシャ、オーストラリア、イスラエル、イギリス、シンガポールなど26の国で採用されている。

## 外部リンク

  - [NTTドコモによるCiRCUSの紹介(PDF)](http://www.docomo.biz/img/pressdata/pdf/sxm_dsquare02.pdf)
  - [NTTデータによるニュースリリース](http://www.nttdata.co.jp/release/2003/042800.html)

[Category:電子メール](https://ja.wikipedia.org/wiki/Category:電子メール "wikilink") [Category:携帯電話_(NTTドコモ)](https://ja.wikipedia.org/wiki/Category:携帯電話_\(NTTドコモ\) "wikilink") [Category:携帯電話ブラウジング](https://ja.wikipedia.org/wiki/Category:携帯電話ブラウジング "wikilink")
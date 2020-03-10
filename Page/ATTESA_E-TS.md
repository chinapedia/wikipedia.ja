> この記事は[ATTESA E-TS](https://ja.wikipedia.org/wiki/ATTESA_E-TS)から翻訳されています。


**ATTESA E-TS**（アテーサ イーティーエス）とは、[日産自動車](../Page/日産自動車.md "wikilink")が開発した電子制御トルクスプリット[四輪駆動](../Page/四輪駆動.md "wikilink")システムの名称。「**A**dvanced **T**otal **T**raction **E**ngineering **S**ystem for **A**ll **E**lectronic - **T**orque **S**plit」の略である。

かつてはHPやカタログ上でも「ATTESA E-TS」と表記されていたが、V36型スカイライン以降の日産のウェブサイトやカタログ上では「**アテーサE-TS**」の表記が主になった（ただし、2008年2月にマイナーチェンジした[シーマ後期型のカタログでは一部ATTESA](https://ja.wikipedia.org/wiki/日産・シーマ "wikilink") E-TSと表記されている箇所もある）。

## 解説

ATTESA E-TSは、基本的には後輪を常時駆動（FR駆動）し、走行条件に応じて前輪に[トルク](../Page/トルク.md "wikilink")を0:100 - 50:50の範囲で配分する（実質的にはFR駆動）。そのため、後輪へは直結状態で駆動力を伝え（センタースルー）、前輪へは[トランスファー](../Page/トランスファー.md "wikilink")で分岐させている。トランスファーに組み込まれた湿式多板[クラッチ](https://ja.wikipedia.org/wiki/クラッチ "wikilink")の押し付け力を[油圧](../Page/油圧.md "wikilink")の変化で増減し、前輪へ伝達されるトルクの大きさを変化させる。そのため、センターデフは装備していない。要するに、分類上は切り替え操作の不要な「フルタイム4WD」であるが、駆動力の伝わり方は「[スタンバイ4WD](https://ja.wikipedia.org/wiki/四輪駆動#スタンバイ式 "wikilink")」である。もちろん、運転者自身が任意で駆動方式を切り替えることもできないため、単なる切り替え式であるパートタイム式とも異なる。

このクラッチを放した状態では後輪駆動、クラッチを結合した状態ではリジッド4駆になり、この間を電子制御で無段階に変化させている。

さらに、このシステムには、前後4輪の車輪速度センサと、横[Gをアナログ的に検出するG](../Page/重力.md "wikilink")[センサ](../Page/センサ.md "wikilink")を備えている。これらセンサからの入力信号を受け、コントローラが油圧多板クラッチの圧着力を変化させ、前輪へのトルク配分を決定する。

したがって、通常の後輪駆動状態から、後輪にかかる駆動トルクの増大で、後輪の[スリップ量が大きくなると](../Page/空転.md "wikilink")、前輪へも駆動トルク伝達を行う。前輪へ伝達する駆動トルクの大きさは、横Gの大きさと前後輪の回転速度差に応じて変化する方式としている。

例えば、[アイスバーンのように](../Page/路面凍結.md "wikilink")、タイヤの[摩擦係数μ（ミュー）の低い路面で](https://ja.wikipedia.org/wiki/摩擦力 "wikilink")、[操舵角に対して横Gが小さかったり](../Page/ステアリング.md "wikilink")、後輪のスリップ量が大きい場合は、前輪へのトルク伝達を増やす。

一方、ドライ路面でのコーナリングのように、[横Gが非常に大きい状態では](../Page/遠心力.md "wikilink")、ホイールスピンが起こっていても前輪へ伝達するトルクをあまり増やさない。 これは、後輪側の駆動トルクを大きくし、かつ前輪の駆動トルクを小さく配分することにより、後輪をアクセルワークによって積極的にコントロールするマージン（[ドリフトコントロール性](../Page/ドリフト走行.md "wikilink")）と、前輪の操縦性（[アンダーステア](https://ja.wikipedia.org/wiki/アンダーステア "wikilink")対策）を確保している。

さらに、[ABSとの総合制御も実現している](../Page/アンチロック・ブレーキ・システム.md "wikilink")。4輪それぞれに設けられた車輪速度センサやGセンサにより、作動タイミングをきめ細かくコントロールできるため、より自然な制動性能を確保している。急制動時には、4輪すべてに適切な割合で[エンジンブレーキ](../Page/エンジンブレーキ.md "wikilink")力を割り振り、ブレーキ性能とアンチスキッド性も高めている。

スカイラインGT-RのR33型Vスペック、同R34型Vスペックなどでは、後輪に多板クラッチ電子制御式LSD（[リミテッドスリップデフ](https://ja.wikipedia.org/wiki/リミテッドスリップデフ "wikilink")）を組み合わせた「**ATTESA E-TS PRO**」へと発展した。

## 逸話

開発最終段階で、当時[スカイラインGTS-R](https://ja.wikipedia.org/wiki/日産・スカイライン#7代目_R31型（1985年-1989年） "wikilink")[グループA](../Page/グループA.md "wikilink")仕様で[全日本ツーリングカー選手権に参戦していた](https://ja.wikipedia.org/wiki/全日本ツーリングカー選手権_\(1985年-1993年\) "wikilink")[鈴木亜久里](https://ja.wikipedia.org/wiki/鈴木亜久里 "wikilink")に、同型車へ当システムが組み込まれたプロトタイプを事実関係を伏せたままテスト走行させたところ、ピットに戻ると同時に「何、この車、どうなっちゃったの、こんなトラクションかけられるタイヤができあがったの?」と、驚愕の感想をスタッフへ語ったという。

## 搭載車種

  - [スカイライン](https://ja.wikipedia.org/wiki/日産・スカイライン "wikilink")
      - [GT-R](../Page/日産・スカイラインGT-R.md "wikilink")：R32型 - R34型
      - 標準車：R32型（GTS-4）・R33型（GTS-4）・R34型（GT-FOUR/GT-X FOUR）・[NV35](https://ja.wikipedia.org/wiki/日産・スカイラインセダン_V35 "wikilink")・[NV36](https://ja.wikipedia.org/wiki/日産・スカイラインセダン_V36 "wikilink")・[HNV37](https://ja.wikipedia.org/wiki/日産・スカイラインセダン_V37 "wikilink")）
  - [GT-R](../Page/日産・GT-R.md "wikilink")（R35型）
  - [スカイラインクロスオーバー](https://ja.wikipedia.org/wiki/日産・スカイラインクロスオーバー "wikilink")（NJ50型）
  - [レパード](https://ja.wikipedia.org/wiki/日産・レパード "wikilink")（JY33型）
  - [ステージア](https://ja.wikipedia.org/wiki/日産・ステージア "wikilink")（WGNC34型 － NM35型）
  - [セドリック](https://ja.wikipedia.org/wiki/日産・セドリック "wikilink")・[グロリア](../Page/日産・グロリア.md "wikilink")（Y33型 - Y34型）
  - [フーガ](https://ja.wikipedia.org/wiki/日産・フーガ "wikilink")([PNY50](../Page/日産・フーガ_Y50.md "wikilink")・[KNY51](https://ja.wikipedia.org/wiki/日産・Y51 "wikilink"))
  - [シーマ](https://ja.wikipedia.org/wiki/日産・シーマ "wikilink")（FY32型 － F50型）

## 関連項目

  - [オールモード4X4](../Page/オールモード4X4.md "wikilink")
  - [ATTESA](../Page/ATTESA.md "wikilink")
  - [ポルシェ・959](https://ja.wikipedia.org/wiki/ポルシェ・959 "wikilink")
  - [日産・MID4](../Page/日産・MID4.md "wikilink")

[Category:自動車トランスミッション技術](https://ja.wikipedia.org/wiki/Category:自動車トランスミッション技術 "wikilink") [Category:日産自動車](https://ja.wikipedia.org/wiki/Category:日産自動車 "wikilink")
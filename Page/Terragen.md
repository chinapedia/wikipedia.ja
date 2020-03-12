> この記事は[Terragen](https://ja.wikipedia.org/wiki/Terragen)から翻訳されています。


[thumb](https://ja.wikipedia.org/wiki/画像:Landbyriver.jpg "wikilink") [thumb](https://ja.wikipedia.org/wiki/画像:Mandelbrot_island.jpg "wikilink") [thumb](https://ja.wikipedia.org/wiki/画像:Terragen_render.jpg "wikilink")

**Terragen（テラジェン）**とは、Matt Fairclaughらが経営するPlanetside Software社によって開発された景観[3DCGソフトウェア](https://ja.wikipedia.org/wiki/3DCGソフトウェア "wikilink")である。

## 概要

写真のように、空気感を再現した非常にリアルなグラフィックを作成することが可能である。Terragenは、v.0.9.43以前の旧バージョンであるTerragen ClassicとTerragen 2以降の新バージョンの2種類に大別できる。 新バージョンではプレビュー画面でリアルタイム[レンダリングが行われたり](../Page/レンダリング_\(コンピュータ\).md "wikilink")、各種パラメタ等を[ノード](https://ja.wikipedia.org/wiki/ノード "wikilink")を用いて設定するなど、[ユーザインターフェース](https://ja.wikipedia.org/wiki/ユーザインターフェース "wikilink")や設定方法等が大きく異なる。 Terragen 4は商用利用以外では無料となっているが、無料版にはレンダリングサイズなどの以下のような制限がある\[1\]。

  - レンダリングサイズ　最大：1280×900
  - Render Detail　最大：0.6
  - アンチエイリアス　最大：6
  - Rendered Populationsの数　最大：3
  - Render Detail for Micropolygon Export 最大: 0.1
  - アニメーション作成機能なし

商用版はフル機能のProfessional版が699ドル、一部制限のあるCreative版が349ドルで販売されている。またオブジェクトの素材データなどを同梱したパッケージも存在する。

Terragenの基礎技術は[デジタルドメイン](https://ja.wikipedia.org/wiki/デジタルドメイン "wikilink")において研究されており、コマーシャル、テレビゲームまたは映画で何度も使用されている。映画では[タイムマシン](https://ja.wikipedia.org/wiki/タイムマシン "wikilink")(2002年)、[ネメシス/S.T.X](https://ja.wikipedia.org/wiki/ネメシス/S.T.X "wikilink")(2002年)、[ステルス](../Page/ステルス.md "wikilink")(2004年)、[硫黄島からの手紙](../Page/硫黄島からの手紙.md "wikilink")(2006年)、[デイ・アフター・トゥモロー](../Page/デイ・アフター・トゥモロー.md "wikilink")、[スター・ウォーズシリーズ](../Page/スター・ウォーズシリーズ.md "wikilink")、[怪盗グルーのミニオン大脱走](https://ja.wikipedia.org/wiki/怪盗グルーのミニオン大脱走 "wikilink")など、実際の業務CG制作に使用されている\[2\]。

## Terragen のレンダリング要素

新バージョンのTerragenでは、大きく分けて以下のような要素ごとにパラメタを設定し、それらをノードネットワークで関連付けることでフォトリアルな画像をレンダリングすることができる。

### オブジェクト

外部からインポートしたオブジェクトを配置することができる。単体で設置できる他、同じ物体または何種類かの物体を大量に配置することができる。

### 地形

ハイトフィールドを設定することで地形を作ることができる。[フラクタル](../Page/フラクタル.md "wikilink")を用いて自動的に生成する他、[DEM](https://ja.wikipedia.org/wiki/DEM "wikilink")等を用いてリアルな地形を生成することもできる。

### シェーダー

地面の色等を設定することができる。高度や領域別に設定したり、ランダム性のあるノイズを加えることによってリアルな岩肌や草原などを表現できる。

### 水域

[湖](https://ja.wikipedia.org/wiki/湖 "wikilink")のような水域を設定することができる。水の透明度や反射率などを設定することによってリアルな表現を求めることができる。ただしある一定の高度、領域までを水で満たすような水域しか設定できないため、[山](../Page/山.md "wikilink")岳地形に沿って存在する[河川のような水域の設定は困難である](../Page/川.md "wikilink")。

### 大気

大気の質感や雲などを設定することができる。カメラからの距離に応じた光源の透過率や[レイリー散乱](../Page/レイリー散乱.md "wikilink")における色の変化などを設定することで水蒸気量の違いによる空気感の違いや夕焼け空などを表現できる。また雲の厚さや雲量などを設定できる。

### 光源

光源の強さや色を設定することができる。いわゆる太陽光の位置や仰角の他、複数の太陽光源を設定したり、影の落とし方の設定や全体から均等に照らす環境光などを設定できる。

### カメラ

レンダリングする際のカメラの画角や位置などを設定することができる。[魚眼レンズ](../Page/魚眼レンズ.md "wikilink")などの効果や[ぼかし](https://ja.wikipedia.org/wiki/ぼかし "wikilink")、露光量などを調整できる。

### レンダリング

レンダリングする際の解像度などを設定することができる。地形や雲などの要素別にレンダリングの可否を設定できる他、[アンチエイリアス](../Page/アンチエイリアス.md "wikilink")の有無などを設定できる。

## Terragen 4

[2016年](../Page/2016年.md "wikilink")9月23日にTerragen 3から正式にメジャーバージョンアップがなされた。[オゾン層](https://ja.wikipedia.org/wiki/オゾン層 "wikilink")による太陽光吸収の変化を取り入れたり、ボクセルを用いた雲の表現力の向上、外部から読み込むモデルのレンダリングについての改良がなされた\[3\]。

### エディション

  - Free
  - Creative
  - Professional

## Terragen 2

Terragen 2はTerragenの次世代バージョンであり、TG2と略されていた。TG2はTerragenがまだバージョン1.0に満たない頃から開発されていた。 Terragen D/TGDとTG2を混同されている場合もあるが、TGDは単に新しいレンダリングエンジンの名前のことである。Terragen 2では、新機能として、星や植物（オブジェクト）もレンダリング可能となった。 [2007年](../Page/2007年.md "wikilink")から[2008年](https://ja.wikipedia.org/wiki/2008年 "wikilink")にかけて*'Technology Preview 1～5 **、2008年11月に**Deep Edition Beta（商用利用ベータ版）**、12月に**Free (Non-Commercial) Edition Beta（無料ベータ版）*'とリリースされ、[2009年](../Page/2009年.md "wikilink")4月2日にBeta版ではなく購入者向けに先行リリースされ、次いで、一般ユーザー向けにリリースされた。

### システム要件

Windows 2000/XP/Vista

  - メモリ 必須1GB 　推奨4GB
  - CPU 　必須1GHz 推奨2GHz Dual Core

Mac OS X 10.4 以降

  - メモリ 必須1GB 　推奨4GB
  - CPU 　必須1GHz 推奨 Intel Dual Core 2GHz

### エディション

  - Free Non-Commercial Edition
  - Deep Edition
  - Deep Edition with Animation

## Terragen Classicのレンダリング要素

旧バージョンであるTerragen Classicは、基本的に「地形」「表面」「光源/大気」「水面」の4つの構成要素に基づいている。

### 地形

風景の形を表現するために、Terragenではハイトマップを使用している。高度はその節、地形において各ポイントに割り当てられる。これらのハイトマップは単に通常地形と呼ばれる。

### 表面

表面構成は、Terragen内部のサーフェースシステム(エンジン)上で行われる。表面は複数のレイヤーで表現する。山腹のスロープと高さ、色などによって、個々のレイヤーを管理することができ、例として、草を生やすためのレイヤーを何重にも作れば、平坦な場所において、それが山の谷にある本物のような草に見える。

### 光源/大気

大気は、簡単にはランダムで雲を生成したり、テクスチャーレイヤーまたは立体物を用いて表現することができる。 そのうえ、世界の雰囲気を大きく変えることができ、この項目で詳細に管理すれば、沈みかけの赤い日没や濃霧などの景観が可能になる。

### 水面

水面は、Terragenで最も高価でありリアルな特徴のうちの1つである。リアルな反射と透明性を表現でき、かつ、描かれた自然の波は、海岸線で泡立つことができるようにシミュレートされる。

## バージョンの変遷

  - [2005年](../Page/2005年.md "wikilink")9月7日 Terragen Ver.0.9.43 をリリース。
  - [2006年](../Page/2006年.md "wikilink") Terragen 2 を発表。
  - 2006年12月15日 Terragen 2 Technology Preview(Build 1.8.64.0) をリリース。
  - [2007年](../Page/2007年.md "wikilink")3月16日 Terragen 2 Technology Preview アップデート。 (Build 1.8.76.0)
  - 2007年9月28日 Terragen 2 Technology Preview アップデート。 (Build 1.9.04.1)
  - [2008年](https://ja.wikipedia.org/wiki/2008年 "wikilink") Terragen 2 Technology Preview 2 をリリース。
  - 2008年4月29日 Terragen 2 Technology Preview 3 (Build 1.9.88.1) をリリース。
  - 2008年6月30日 Terragen 2 Technology Preview 4 (Build 1.9.98.1) をリリース。
  - 2008年7月18日 Terragen 2 Technology Preview 5 (Build 1.9.99.1) をリリース。
  - 2008年11月10日 Terragen 2 Deep Edition Beta (Build 1.10.23.1) をリリース。
  - 2008年12月6日 Terragen 2 Free Non-Commercial Edition Beta (Build 1.10.23.1) をリリース。
  - [2009年](../Page/2009年.md "wikilink")4月2日 購入者向けに Terragen 2 Deep Edition、Deep Edition with Animation (Build 2.0.1.1) をリリース。
  - 2009年4月12日 購入者向けに Terragen 2 アップデート。(Build 2.0.2.1)
  - 2009年4月27日 一般ユーザー向けに Terragen 2 Free Non-Commercial Edition (Build 2.0.3.1) リリース。
  - 2009年12月15日 購入者向けに Terragen 2.1 (Build 2.1.18.1) リリース。
  - [2010年](https://ja.wikipedia.org/wiki/2010年 "wikilink")3月1日 一般ユーザー向けに Terragen 2.1 Free Non-Commercial Edition (Build 2.1.18.1) リリース。
  - 2010年11月27日 購入者向けに Terragen 2.2 リリース。
  - [2011年](../Page/2011年.md "wikilink")1月31日 一般ユーザー向けに Terragen 2.2 Free Non-Commercial Edition リリース。
  - 2011年4月21日 購入者向けに Terragen 2.3 リリース。
  - 2011年7月1日 一般ユーザー向けに Terragen 2.3 Free Non-Commercial Edition リリース。

<!-- end list -->

  - [2013年](../Page/2013年.md "wikilink")8月23日 Terragen 3.0.10.0 リリース。
  - [2014年](../Page/2014年.md "wikilink")2月23日 Terragen 3.1 リリース。
  - 2014年2月23日 Terragen 3.2 リリース。
  - [2015年](../Page/2015年.md "wikilink")8月8日 Terragen 3.3 リリース。
  - [2016年](../Page/2016年.md "wikilink")3月17日 Terragen 3.4 リリース。
  - 2016年9月23日 Terragen 4.0 リリース。
  - 2016年9月23日 Terragen 4.0.01.0 リリース。
  - 2016年11月2日 Terragen 4.0.04 リリース。
  - [2017年](../Page/2017年.md "wikilink")7月25日 Terragen 4.1.11 リリース。
  - [2018年](../Page/2018年.md "wikilink")7月10日 Terragen 4.2.10 リリース。
  - 2018年11月16日 Terragen 4.3.16 リリース。

## 関連項目

  - [3DCGソフトウェア](https://ja.wikipedia.org/wiki/3DCGソフトウェア "wikilink")
  - [レンダリング (コンピュータ)](../Page/レンダリング_\(コンピュータ\).md "wikilink")
  - [フラクタル地形](../Page/フラクタル地形.md "wikilink")

## 脚注

## 外部リンク

  - [Planetside](http://www.planetside.co.uk/)
  - [Planetside公式フォーラム](http://forums.planetside.co.uk/)
  - [Terragen 4 日本語 wiki](https://www65.atwiki.jp/terragen/)

[Category:3DCGソフトウェア](https://ja.wikipedia.org/wiki/Category:3DCGソフトウェア "wikilink")

1.
2.
3.
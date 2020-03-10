> この記事は[MODEL2](https://ja.wikipedia.org/wiki/MODEL2)から翻訳されています。


**MODEL2**（モデルツー）は[1993年](../Page/1993年.md "wikilink")にセガ（後の[セガ・インタラクティブ](https://ja.wikipedia.org/wiki/セガ・インタラクティブ "wikilink")）によって開発された[アーケードゲーム](../Page/アーケードゲーム.md "wikilink")用[システム基板](https://ja.wikipedia.org/wiki/システム基板 "wikilink")である。

## 概要

[MODEL1](../Page/MODEL1.md "wikilink")と同じく、セガと[米国の](https://ja.wikipedia.org/wiki/アメリカ合衆国 "wikilink")[マーティン・マリエッタ](https://ja.wikipedia.org/wiki/マーティン・マリエッタ "wikilink")が共同で開発した。リアルタイム3DCGの黎明期のハードだったため当時としては非常に高価だった。

MODEL1の後継機という位置付けではあるが、完全な新規設計によりMODEL1との構造的な共通点はない。メインCPUに[インテル](https://ja.wikipedia.org/wiki/インテル "wikilink")の[i960](https://ja.wikipedia.org/wiki/Intel_i960 "wikilink")。描画プロセッサは[富士通](../Page/富士通.md "wikilink")のMB86234。MODEL1と同様、音源制御に[MC68000](../Page/MC68000.md "wikilink")を採用。28チャンネルの[PCM音源](../Page/PCM音源.md "wikilink")を搭載する。

MODEL2のレンダリング機能はMODEL1にも実装された[フラットシェーディング](https://ja.wikipedia.org/wiki/フラットシェーディング "wikilink")と、限定的ではあるが[テクスチャマッピング機能が追加された](https://ja.wikipedia.org/wiki/テクスチャーマッピング "wikilink")。1枚のテクスチャあたり使用可能な色数は1色のみで、同一テクスチャ内では、それを16階調のトーンのみで表現するという非常に限定的な仕様であったため、色の境界でポリゴンを分割しなければならなかった。また、半透明なテクスチャが扱えず、メッシュによる表現で代替せざるを得なかった。しかし、ゲーム開発にあたっては、デザイナーの工夫(高精細なモデルをテクスチャに落とし込む)によってMODEL1では不可能だったリアルな質感表現を実現し、MODEL1のゲームと比べキャラクターモデルあたりのポリゴン数を減じる事も可能となった。

描画能力も約30万ポリゴン/秒と、MODEL1から見てもほぼ倍に増えた。その性能向上分は1秒あたりの描画フレーム数を増やすという方向で使われ、MODEL1より滑らかな動きのリアルタイムCGを表現することに成功した。『[デイトナUSA](https://ja.wikipedia.org/wiki/デイトナUSA "wikilink")』では、60fpsで描画しているにもかかわらず最大で40台ものストックカーがサーキット上を同時に走ることが可能となっている。

MODEL2を使用した第一弾タイトルは『デイトナUSA』。MODEL2基板を使用したゲームは次々にヒットし、セガの90年代におけるアーケード黄金時代を支えた基板といえる。

また、MODEL2は、MODEL2/2A/2B/2Cの4つのバージョンが存在するが、それぞれ互換性はない（一部のタイトルは、2A用と2B用にリリースされたが、セキュリティICに互換性が無いので、ROMキットは各バージョン専用となっている）。 初代のMODEL2のみ、MODEL1同様にサウンド機能は別基板となっており、MODEL1のサウンドボードをそのまま流用していたが、2A以降はサウンド機能が統合された。2A/2B/2Cの違いは、設計の効率化と、周辺DSPの高速化が主体である。

部品調達難に伴い、2017年3月31日を以って修理サポートが終了した\[1\]。

## 主なスペック

  - CPU
    Intel i960(32bitRISC) @ 25MHz
  - 数値演算
    DSP（32bit） @ 50MHz
    3Dマトリックス・軸回転・浮動小数点演算機能搭載
  - RAM
    1MB + 128KB（ROM：90MB）
  - VRAM
    5,984 KB (Model 2/2A-CRX)
    14,596 KB (Model 2B/2C-CRX)
  - 3Dグラフィックエンジン
    最大300,000ポリゴン/秒（色付きグレースケールテクスチャーマッピング可）
    パースペクティブテクスチャーマッピング・フラットシェーディング機能搭載
    鏡面・拡散反射モード内蔵
  - 発色数
    65,536色 1,024カラーパレット（16,777,216色中）
    スクロール：32,768色（2面）
    ウインドウ：32,768色（2面）
    共に水平方向ラインスクロール可能
  - 解像度
    496(H) x 384(V)　水平周波数24kHz
  - その他
    通信機能拡張、[MIDI](../Page/MIDI.md "wikilink")によるサウンド通信

## 開発されたゲーム

### MODEL2基板

  - [デイトナUSA](https://ja.wikipedia.org/wiki/デイトナUSA "wikilink")（1994年）
  - [バーチャコップ](https://ja.wikipedia.org/wiki/バーチャコップ "wikilink")（1994年）
  - [デザートタンク](https://ja.wikipedia.org/wiki/デザートタンク "wikilink")（1994年、セガ/[マーティン・マリエッタ](https://ja.wikipedia.org/wiki/マーティン・マリエッタ "wikilink")※）

### MODEL2A基板

  - [バーチャファイター2](../Page/バーチャファイター2.md "wikilink")（1994年）
  - バーチャコップ2（[1995年](https://ja.wikipedia.org/wiki/1995年 "wikilink")）
  - [ファイティングバイパーズ](https://ja.wikipedia.org/wiki/ファイティングバイパーズ "wikilink")：ロケテストver（1995年）
  - [セガラリーチャンピオンシップ](https://ja.wikipedia.org/wiki/セガラリーチャンピオンシップ "wikilink")（1995年 DXタイプは別途サウンドボードにて4ch出力）
  - [スカイターゲット](https://ja.wikipedia.org/wiki/スカイターゲット "wikilink")(1995年)
  - [マンクスTT スーパーバイク](https://ja.wikipedia.org/wiki/マンクスTT_スーパーバイク "wikilink")（1995年）
  - [モーターレイド](https://ja.wikipedia.org/wiki/モーターレイド "wikilink")（[1997年](https://ja.wikipedia.org/wiki/1997年 "wikilink")）

### MODEL2B基板

  - [レールチェイス2](https://ja.wikipedia.org/wiki/レールチェイス2 "wikilink")（[1994年](../Page/1994年.md "wikilink")）
  - [バーチャストライカー](https://ja.wikipedia.org/wiki/バーチャストライカー "wikilink")（1994年）
  - [ファイティングバイパーズ](https://ja.wikipedia.org/wiki/ファイティングバイパーズ "wikilink")（1995年）
  - [インディ500](https://ja.wikipedia.org/wiki/インディ500_\(アーケードゲーム\) "wikilink")（1995年）
  - [ガンブレードNY](../Page/ガンブレードNY.md "wikilink")（1995年）
  - [ソニック・ザ・ファイターズ](https://ja.wikipedia.org/wiki/ソニック・ザ・ファイターズ "wikilink")（[1996年](../Page/1996年.md "wikilink")）
  - [ラストブロンクス](https://ja.wikipedia.org/wiki/ラストブロンクス "wikilink")-東京番外地-（1996年）
  - [電脳戦機バーチャロン](../Page/電脳戦機バーチャロン.md "wikilink")（1995年）
  - スーパーGT24H（1996年、[ジャレコ](../Page/ジャレコ.md "wikilink")）
  - ロイヤルアスコット2（メダルゲームのメインモニターに使用：50インチ3画面）
  - ロイヤルアスコット2 スタンダード（1画面バージョン）

### MODEL2A/B両方

ROMキットに互換性は無いので注意が必要。

  - [ダイナマイトベースボール](https://ja.wikipedia.org/wiki/ダイナマイトベースボール "wikilink")（1996年）
  - [ダイナマイトベースボール'97](https://ja.wikipedia.org/wiki/ダイナマイトベースボール'97 "wikilink")（1997年）
  - [ダイナマイト刑事2](https://ja.wikipedia.org/wiki/ダイナマイト刑事2 "wikilink")（[1998年](https://ja.wikipedia.org/wiki/1998年 "wikilink")）- セガがMODEL2で開発した最後のゲーム。
  - [デッド オア アライブ](https://ja.wikipedia.org/wiki/デッド_オア_アライブ "wikilink")（1996年、[テクモ](../Page/テクモ.md "wikilink")）
  - [ゼロガンナー](https://ja.wikipedia.org/wiki/ゼロガンナー "wikilink")（1997年、[彩京](https://ja.wikipedia.org/wiki/彩京 "wikilink")）
  - [パイロットキッズ](https://ja.wikipedia.org/wiki/パイロットキッズ "wikilink")（[1999年](../Page/1999年.md "wikilink")、彩京）- MODEL2で発売された最後のゲーム。

### MODEL2C基板

  - [セガツーリングカーチャンピオンシップ](https://ja.wikipedia.org/wiki/セガツーリングカーチャンピオンシップ "wikilink")（1996年）
  - [セガ スキースーパーG](https://ja.wikipedia.org/wiki/セガ_スキースーパーG "wikilink")（1996年）
  - [ウェーブランナー](https://ja.wikipedia.org/wiki/ウェーブランナー "wikilink")（1996年）
  - [セガ ウォータースキー](https://ja.wikipedia.org/wiki/セガ_ウォータースキー "wikilink")（1997年）
  - [ザ・ハウス・オブ・ザ・デッド](https://ja.wikipedia.org/wiki/ザ・ハウス・オブ・ザ・デッド "wikilink")（1997年）
  - [トップスケーター](https://ja.wikipedia.org/wiki/トップスケーター "wikilink")（1997年）
  - [ビハインドエネミーラインズ](https://ja.wikipedia.org/wiki/ビハインドエネミーラインズ "wikilink")（1998年、セガ/[Real3D](https://ja.wikipedia.org/wiki/Real3D "wikilink")\[2\]）

## 脚注

<references />

## 関連項目

  - [MODEL1](../Page/MODEL1.md "wikilink")
  - [MODEL3](https://ja.wikipedia.org/wiki/MODEL3 "wikilink")
  - [NAOMI](https://ja.wikipedia.org/wiki/NAOMI "wikilink")
  - [SEGAHIKARU](https://ja.wikipedia.org/wiki/SEGAHIKARU "wikilink")
  - [LINDBERGH](https://ja.wikipedia.org/wiki/LINDBERGH "wikilink")

[en:List of Sega arcade system boards\#Sega Model 2](https://ja.wikipedia.org/wiki/en:List_of_Sega_arcade_system_boards#Sega_Model_2 "wikilink")

[Category:セガのアーケードゲーム基板](https://ja.wikipedia.org/wiki/Category:セガのアーケードゲーム基板 "wikilink")

1.  [弊社製品保守対応の終了について](https://www2.sls-net.co.jp/cms/sls/pdf/news/201611_p_maintenance.pdf)セガ・インタラクティブ、セガ・ロジスティクスサービス 2016年11月
2.  [GE](https://ja.wikipedia.org/wiki/ゼネラル・エレクトリック "wikilink") Aerospace社が[1992年](https://ja.wikipedia.org/wiki/1992年 "wikilink")、マーティンマリエッタに吸収されたもの。後に、[ロッキード](../Page/ロッキード.md "wikilink")との合併により、民需向けに特化、Real 3Dと改名した。1999年にインテルに売却され、解散した。
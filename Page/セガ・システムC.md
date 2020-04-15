> この記事は[セガ・システムC](https://ja.wikipedia.org/wiki/セガ・システムC)から翻訳されています。


[thumb](https://ja.wikipedia.org/wiki/画像:sega_system_c2_pcb.jpg "wikilink")

**System C**/**System C2**とは、セガ（後の[セガ・インタラクティブ](https://ja.wikipedia.org/wiki/セガ・インタラクティブ "wikilink")）が開発した[アーケードゲーム基板](../Page/アーケードゲーム基板.md "wikilink")である。

## 概要

本機は家庭用ゲーム機[メガドライブ](../Page/メガドライブ.md "wikilink")の[アーキテクチャ](../Page/アーキテクチャ.md "wikilink")をベースに、一部機能の拡張と簡略化を図った小型機用タイトル向けのシステム基板である。同時代の業務用システム基板としてはローコストであり、それまでのセガ製システム基板とは違い配線もJAMMA配列を採用する等、小店舗でも安価で導入しやすかったのが特徴。

家庭用のメガドライブと比較した場合、[CPU](../Page/CPU.md "wikilink")（[68000](../Page/MC68000.md "wikilink")）動作クロックの高速化\[1\]、[VDP](../Page/VDP.md "wikilink")のカラーパレットの拡張、サンプリング音声発声用に[ADPCM](https://ja.wikipedia.org/wiki/ADPCM "wikilink")の追加等の機能強化が行われている。 また、この基板は2枚接続しての通信対戦機能、同社筐体「メガロ50」のムービングシートの制御などができる等、I/O周りも業務用途を考慮して機能が拡張されていた。

主に家庭用のメガドライブへの移植を前提として、業務用先行で開発リリースされたゲームや、メガドライブに参入していた[サードパーティー](../Page/サードパーティー.md "wikilink")製の業務用タイトルなどが多く供給された。また、ビデオゲームの他にも[プリント倶楽部](../Page/プリント倶楽部.md "wikilink")やキッズマシン等でも多く使用されていた。 ヒットタイトルには[コラムス](../Page/コラムス.md "wikilink")、[ぷよぷよ](../Page/ぷよぷよ.md "wikilink")、[ぷよぷよ通](../Page/ぷよぷよ通.md "wikilink")、[タントアール](../Page/タントアール.md "wikilink")等がある。パズル系のゲームにヒット作が多く、プリント倶楽部は社会現象レベルで大ヒットする等、ローコストのシステム基板としては大成功した部類に入る。

部品調達難に伴い、2017年3月31日を以って修理サポートが終了した\[2\]。

## SYSTEM C・C2 仕様

システムCとC2の差異はサンプリング音声発声用に[ADPCM](https://ja.wikipedia.org/wiki/ADPCM "wikilink")の追加の有無でその他は共通

  - CPU：MC68000|68000（8.948862MHz駆動）

<!-- end list -->

  - ワークRAM：64KB
  - VDP：315-5313
      - 解像度：320（256）ドット×224ライン
      - VRAM：64KB
      - BG：2画面+ウインドウ機能
      - スプライト：1画面に最大80個表示。サイズ8×8～32×32。横に20個まで表示可能
      - 同時発色数：32768色中128色（BGとスプライトに16色のカラーパレットが各4本）
  - サウンド：[YM3438](../Page/FM音源.md "wikilink") (OPN2C) 4オペレータFM音源 6ch　SN76496（[PSG](../Page/Programmable_Sound_Generator.md "wikilink")）矩形波3ｃｈ+ノイズ1ｃｈ　μPD7759 [ADPCM](https://ja.wikipedia.org/wiki/ADPCM "wikilink")1ch\[3\]
  - 通信対戦およびIO制御用ポート

## 主なタイトル

特記事項無しのものはシステムC2

  - コラムス（システムC）
  - コラムスII（システムC）
  - タントアール
  - [イチダントアール](../Page/イチダントアール.md "wikilink")
  - スタックコラムス
  - ポトポト
  - [ブロクシード](../Page/ブロクシード.md "wikilink")（システムC / 海外輸出版のみ、国内版は[セガ・システム18](https://ja.wikipedia.org/wiki/セガ・システム18 "wikilink")を使用）
  - リビット！/ 蝦蟇の園（国内ではロケテストのみで販売は無し）
  - ツインスカッシュ（国内未発売）
  - ボレンチ（ロケテストのみで未発売）

### サードパーティー製

  - サンダーフォースAC（テクノソフト）
  - ぷよぷよ（コンパイル）
  - ぷよぷよ通（コンパイル)
  - ずんずん教の野望（港技研）
  - OOPARTS（サクセス 未発売）

### その他

  - セガ製キディライド（モニター部分のみ）

<!-- end list -->

  -
    ※わくわくソニックパトカー、わくわくマリンなど

<!-- end list -->

  - セガ製ポップコーン自動販売機（モニター部分のみ）

<!-- end list -->

  -
    ※それいけ！アンパンマン ポップコーンこうじょう、セガソニック ポップコーンショップなど

<!-- end list -->

  - [プリント倶楽部](../Page/プリント倶楽部.md "wikilink")（[アトラス](../Page/アトラス_\(ゲーム会社\).md "wikilink")・セガ共同開発）

<!-- end list -->

  -
    ※初代、Vol.2ウインターバージョン、Vol.3スプリングバージョン、Vol.4、サマーバージョン、Vol.5オータムバージョンまで使用。本作はビデオキャプチャ機能に合わせて表示クロックを微調整する等カスタマイズがされており完全な互換性はない。

## 脚注

[en:List of Sega arcade system boards\#Sega_System_C-2](https://ja.wikipedia.org/wiki/en:List_of_Sega_arcade_system_boards#Sega_System_C-2 "wikilink")

[Category:セガのアーケードゲーム基板](https://ja.wikipedia.org/wiki/Category:セガのアーケードゲーム基板 "wikilink")

1.  メガドライブにあったサブCPUのZ80は載っておらず、処理は全てMC68000のみで行う。
2.  [弊社製品保守対応の終了について](https://www2.sls-net.co.jp/cms/sls/pdf/news/201611_p_maintenance.pdf)セガ・インタラクティブ、セガ・ロジスティクスサービス 2016年11月
3.  ADPCMはSYSTEM C2のみに実装
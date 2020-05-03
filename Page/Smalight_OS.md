> この記事は[Smalight OS](https://ja.wikipedia.org/wiki/Smalight_OS)から翻訳されています。


**Smalight OS**（スマライトオーエス、SMArt & LIGHT Operating System）は、[マクセルフロンティア株式会社が製造](https://ja.wikipedia.org/wiki/マクセルシステムテック "wikilink")・販売している[組み込み用](../Page/組み込みシステム.md "wikilink")[リアルタイムオペレーティングシステム](../Page/リアルタイムオペレーティングシステム.md "wikilink")のこと。

## 特徴

[μITRON](https://ja.wikipedia.org/wiki/μITRON "wikilink")仕様ライク\[1\]な[APIを持つ](../Page/アプリケーションプログラミングインタフェース.md "wikilink")、[ローエンド](https://ja.wikipedia.org/wiki/ローエンド "wikilink")な[マイクロコンピュータ](../Page/マイクロコンピュータ.md "wikilink")向け[リアルタイムオペレーティングシステム](../Page/リアルタイムオペレーティングシステム.md "wikilink")。小容量の[メモリ](https://ja.wikipedia.org/wiki/メモリ "wikilink")([ROM](https://ja.wikipedia.org/wiki/Read_Only_Memory "wikilink"), [RAM](../Page/Random_Access_Memory.md "wikilink"))で動作することを目的としたコンパクトさが特徴である。 [μITRON](https://ja.wikipedia.org/wiki/μITRON "wikilink")仕様のうち、タスクの動的管理機能、[ミューテックス](../Page/ミューテックス.md "wikilink")、[メールボックス](../Page/メッセージキュー.md "wikilink")、メッセージバッファ、(メモリー管理機能)、といった機能が削除された縮小サブセットを採用している。

## 主な機能

### タスク管理

タスクはプライオリティタスク（Priority Task）とローテーションタスク（Rotation Task）に分類する。プライオリティタスクは優先的に実行し、プライオリティタスク数と同じ数のタスク優先度レベルが存在する（同一のタスク優先度レベルに複数のタスクを登録できない）。ローテーションタスクは一番低い優先度で実行するタスクで、同じタスク優先度レベルに複数のタスクを登録できる。

### 同期通信機能

標準対応する同期通信機能には、次の3種類が存在する。

  - [セマフォ](../Page/セマフォ.md "wikilink")

  -
  - [データキュー](../Page/キュー_\(コンピュータ\).md "wikilink")

### 時間管理機能

標準対応する時間管理機能は次の2種類が存在する。

  - システム時刻管理
  - 周期ハンドラ

### コンフィグレーション

タスクやイベントフラグ等の定義をコンフィグレーションファイルに記述して、静的なオブジェクトを生成する。動的APIは対応しない。

## 主なサポートCPU

  - [H8 Tiny,H8/300H-SLP, H8/300L, H8/300L-SLP](../Page/H8.md "wikilink")/300H
  - [SH/Tiny,SH-2,SH-2A](../Page/SuperH.md "wikilink")
  - [H8S](https://ja.wikipedia.org/wiki/H8S "wikilink")
  - [H8SX](https://ja.wikipedia.org/wiki/H8SX "wikilink")
  - [M16C](https://ja.wikipedia.org/wiki/M16C "wikilink")/2x,3x,6x
  - [R8C/Tiny](https://ja.wikipedia.org/wiki/R8C/Tiny "wikilink")
  - [RL78](https://ja.wikipedia.org/wiki/RL78 "wikilink")
  - [RX](https://ja.wikipedia.org/wiki/RXアーキテクチャ "wikilink")
  - [RZ](https://ja.wikipedia.org/wiki/RZ/A "wikilink")

## 参考文献

  -
  -
## 外部リンク

  - [Smalightホームページ](https://www.frontier.maxell.co.jp/dms/solution/smalight-index/index.html)

## 注釈

<references group="*" />

## 脚注

[Category:リアルタイムオペレーティングシステム](https://ja.wikipedia.org/wiki/Category:リアルタイムオペレーティングシステム "wikilink") [Category:組み込みオペレーティングシステム](https://ja.wikipedia.org/wiki/Category:組み込みオペレーティングシステム "wikilink")

1.  完全な[μITRON](https://ja.wikipedia.org/wiki/μITRON "wikilink")仕様準拠ではなく縮小サブセットである。
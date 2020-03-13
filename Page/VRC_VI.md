> この記事は[VRC VI](https://ja.wikipedia.org/wiki/VRC_VI)から翻訳されています。


[thumb](https://ja.wikipedia.org/wiki/画像:VRC_VI_03.jpg "wikilink")」実装例\]\] **VRC VI** (ヴィーアールシー シックス、Virtual Rom Controller 6) は[1989年](../Page/1989年.md "wikilink")に[コナミ](../Page/コナミホールディングス.md "wikilink")（後に[コナミデジタルエンタテインメント](../Page/コナミデジタルエンタテインメント.md "wikilink")へ分社）が開発した[ファミリーコンピュータ](https://ja.wikipedia.org/wiki/ファミリーコンピュータ "wikilink") (ファミコン) 用の[ROM](https://ja.wikipedia.org/wiki/Read_Only_Memory "wikilink")[バンクコントロール](../Page/バンク切り換え.md "wikilink")[チップ兼](../Page/集積回路.md "wikilink")、音源[LSIである](../Page/集積回路.md "wikilink")。

また、本項ではVRC VIの派生版にあたる**VRC VII** (ヴィーアールシー セブン、Virtual Rom Controller 7)についても記述する。

## VRC VI

### 仕様

  - プログラムROMとキャラクターROMを[バンク切り換え](../Page/バンク切り換え.md "wikilink")可能
  - 音声出力：8ビットデジタル出力（[矩形波](../Page/矩形波.md "wikilink") 2ch + [鋸波](../Page/のこぎり波.md "wikilink") 1ch） - ラスター位置を検出して、IRQ[割り込みを発生させる](../Page/割り込み_\(コンピュータ\).md "wikilink")。
  - [パッケージ](../Page/パッケージ_\(電子部品\).md "wikilink")：48ピン[DIP](https://ja.wikipedia.org/wiki/パッケージ_\(電子部品\)#DIP_\(Dual_Inline_Package\) "wikilink") - パッケージ形状や表面の印刷、文字形状、[ロット管理](../Page/ロット管理.md "wikilink")番号などから[東芝](../Page/東芝.md "wikilink")製と思われる。

### 音源部分

  - 矩形波(2ch) : ファミコン音源では4種類だった[デューティ比](https://ja.wikipedia.org/wiki/デューティ比 "wikilink")が、VRC VIでは8種類(1:15から1:1まで)
  - 鋸波(1ch) : 音声出力はデジタル出力であるが、[ROMカートリッジ内に実装されているR](../Page/ロムカセット.md "wikilink")-2R方式の抵抗ラダーにより[D/A変換され](../Page/デジタル-アナログ変換回路.md "wikilink")、ファミコンのカートリッジスロットの外部音声入力端子を経由してファミコン内部でファミコン内蔵音源と音声[ミキシング](../Page/ミキシング.md "wikilink")され、音声出力される。

### VRC VI搭載ゲーム

  - RC845 [悪魔城伝説](../Page/悪魔城伝説.md "wikilink")
  - RC846 [魍魎戦記MADARA](../Page/魍魎戦記MADARA.md "wikilink")
  - RC861 [エスパードリーム2 新たなる戦い](https://ja.wikipedia.org/wiki/エスパードリーム2_新たなる戦い "wikilink")

## VRC VII

VRC VIIは VRC VIの派生品。基本仕様はVRC VIと同等であるが、音源部が[FM音源](https://ja.wikipedia.org/wiki/FM音源#音源チップ一覧 "wikilink") （[YM2413](https://ja.wikipedia.org/wiki/YM2413 "wikilink")（OPLL）類似、6ch） 仕様となっている。OPLLとの違いは、リズム音源の削除、リズム音源未使用時でもFM音源の同時発音数が6音に削減、内蔵音色パラメータを独自のものに差し替えである。レジスタ配置はOPLLとの互換性がある。

### VRC VII搭載ゲーム

  - RC851 [ラグランジュポイント](../Page/ラグランジュポイント_\(ゲーム\).md "wikilink")
  - RV051 タイニートゥーンアドベンチャー2(日本国内版のみ。バンクコントローラとしての使用であり、拡張音源は未使用)

## 関連項目

  - [Virtual Rom Controller (VRC)](https://ja.wikipedia.org/wiki/Virtual_Rom_Controller "wikilink")
      - [VRC IV](https://ja.wikipedia.org/wiki/VRC_IV "wikilink")
  - [SCC](../Page/SCC.md "wikilink")

[Category:ファミリーコンピュータ](https://ja.wikipedia.org/wiki/Category:ファミリーコンピュータ "wikilink") [Category:コナミデジタルエンタテインメント](https://ja.wikipedia.org/wiki/Category:コナミデジタルエンタテインメント "wikilink") [Category:音源チップ](https://ja.wikipedia.org/wiki/Category:音源チップ "wikilink") [Category:メモリ管理](https://ja.wikipedia.org/wiki/Category:メモリ管理 "wikilink")
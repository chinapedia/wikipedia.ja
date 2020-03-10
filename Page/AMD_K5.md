> この記事は[AMD K5](https://ja.wikipedia.org/wiki/AMD_K5)から翻訳されています。


| Am5x86                           |
| -------------------------------- |
| 製造元                              |
| 種類                               |
| [周波数](../Page/周波数.md "wikilink") |
| FSB                              |
| 1次キャッシュ                          |
| 2次キャッシュ                          |
| 拡張命令                             |
| プロセス                             |
| トランジスタ数                          |
| プラットホーム                          |
| パッケージ                            |

[thumb](https://ja.wikipedia.org/wiki/ファイル:AMDK5Diagram.png "wikilink") [thumb](https://ja.wikipedia.org/wiki/ファイル:AMD5k86-P90_SSA5-90ABQ.jpg "wikilink") [thumb](https://ja.wikipedia.org/wiki/ファイル:AMD_K5_PR166_Front.jpg "wikilink")

**K5**は、[AMDが開発した](https://ja.wikipedia.org/wiki/アドバンスト・マイクロ・デバイセズ "wikilink")[マイクロプロセッサ](../Page/マイクロプロセッサ.md "wikilink")。[インテル](https://ja.wikipedia.org/wiki/インテル "wikilink")の[x86](https://ja.wikipedia.org/wiki/x86 "wikilink")命令セットを採用したAMDの第5世代の互換プロセッサである。K5の5は第5世代を表す。Kは[クリプトン](../Page/クリプトン.md "wikilink")の頭文字だとされているが、製品内容との関係は全くない。当時のインテル製品の開発呼称はPと数字と組み合わせたもので、それに倣ったと考えられる。

インテルの同じく第5世代プロセッサである[Pentiumプロセッサへの対抗として](../Page/Intel_Pentium_\(1993年\).md "wikilink")[1993年](../Page/1993年.md "wikilink")に発表された製品であるが、実際の発売は遅れて[1996年](../Page/1996年.md "wikilink")になった。設計は[Am29000開発チームが手がけ](https://ja.wikipedia.org/wiki/AMD_29000 "wikilink")、そのマイクロアーキテクチャをインテルのそれと比較するとPentiumシリーズのP5マイクロアーキテクチャよりも[P6マイクロアーキテクチャ](../Page/P6マイクロアーキテクチャ.md "wikilink")（[Pentium Pro](../Page/Pentium_Pro.md "wikilink")）に近く、Am29000の流れを汲む[RISC](../Page/RISC.md "wikilink")コア（[FPU](../Page/FPU.md "wikilink")を含む）にx86命令デコーダを組み合わせた構造となっている。430万[トランジスタ](../Page/トランジスタ.md "wikilink")で構成されている。開発時期の関係でPentiumプロセッサの後期製品で実装された[MMX](../Page/MMX.md "wikilink")命令はK5には実装されておらず、次世代の[K6プロセッサを待つこととなる](../Page/AMD_K6.md "wikilink")。

Pentiumとの相対的な性能指標としてPレーティングを採用している。例えばP100はPentium 100 MHz相当の製品という意味を持つ。

## 特徴

  - 5個の整数演算ユニット（ALU\*2個、分岐1個、ロードストア2個）を持ち、[アウト・オブ・オーダー実行](../Page/アウト・オブ・オーダー実行.md "wikilink")機能を実現。また、浮動小数点ユニットをひとつ持つ。
  - 分岐ターゲットバッファはPentiumの4倍のサイズであるが、K5は1BitカウンターであるためPentitumよりは精度が落ちる(Pentiumは2Bit、Pentium Proは4Bitカウンター)、また分岐先予測用のアドレスを保持するバッファを持ってないなどの欠点がある。
  - [レジスタ・リネーミング](../Page/レジスタ・リネーミング.md "wikilink")により並列実行性能を向上させている。
  - [投機的実行](../Page/投機的実行.md "wikilink")により[パイプラインストールを減らしている](https://ja.wikipedia.org/wiki/命令パイプライン "wikilink")。
  - [リオーダーバッファ](https://ja.wikipedia.org/wiki/リオーダーバッファ "wikilink")は16エントリー、[リザベーションステーション](https://ja.wikipedia.org/wiki/リザベーションステーション "wikilink")は11エントリーであった。
  - 命令キャッシュは16Kバイト、4ウェイ・セットアソシアティブで、Pentiumは8Kバイト、2ウェイ・セットアソシアティブであった。
  - [データキャッシュは](../Page/キャッシュメモリ.md "wikilink")8Kバイト4ウェイ・セットアソシアティブである。Pentiumは8Kバイト2ウェイ・セットアソシアティブであった。

## 経過

K5プロジェクトによるAMDの目的は技術上のリーダーシップをインテルから奪うことだった。インテルの次世代マイクロアーキテクチャの構造を先取りしていることから方向性は妥当だったと言えるが、製造の面でそれを実現できるだけの量産設備をAMDは持っていなかった。Am29000から流用されたFPUによる浮動小数点演算能力は[Cyrix 6x86より優れていたが](https://ja.wikipedia.org/wiki/Cyrix_6x86 "wikilink")、Pentiumには劣っていた。整数演算ではCyrix 6x86の方が優れていた。開発が難航し、発売が大きく延期されたことから競合他社はより高性能化していたことが成功しなかった大きな理由である。K5には前期版の社内コード名**SSA/5**と後期版の同じく**5k86**の2種類のバージョンが存在する。製品名は当初**5k86**だったが、社内コードが**5k86**に変更されてからは、旧モデルも含めて全て**K5**に改名された。 商業的には成功したとは言い難いが、Pentium向けSocket 5/7搭載マザーボードにおける動作互換性はライバルのCyrix 6x86と比較して格段に高く、内部構造の相違から生ずる命令実行クロック数の差異に起因するソフトウェアのごく僅かな動作不具合が発生した程度に留まる。スクラッチから新規に開発されたプロセッサとしては非常に完成度の高い製品であったと言えよう。 K5は、成功した[Am486](../Page/Am486.md "wikilink") や [AMD K6-2のようにシェアを獲得することはできなかったが](../Page/AMD_K6-2.md "wikilink")、[Pentium FDIV バグの影響によりPentiumが買い控えられた時期には](../Page/Pentium_FDIV_バグ.md "wikilink")、代わりにK5が一時的にではあるがシェアを確保することができた。

## 各モデル詳細

### SSA/5

  - 製品名：**5K86** P75～P100、後に **K5** PR75～PR100
  - プロセス：430万トランジスタ、0.5un または 0.35um
  - 一次キャッシュ：8 + 16 KB (データ + 命令)
  - 接続：[Socket 5](https://ja.wikipedia.org/wiki/Socket_5 "wikilink") および [Socket 7](../Page/Socket_7.md "wikilink")
  - 電源電圧：VCore 3.52V
  - 外部バス：50 (PR75), 60 (PR90), 66 MHz (PR100)
  - リリース時期：[1996年](../Page/1996年.md "wikilink")3月27日
  - 動作周波数：75, 90, 100 MHz

### 5k86

  - 製品名：**K5** PR120～PR166 (200)
  - プロセス：430万トランジスタ、350nm
  - 一次キャッシュ：8 + 16 KB (データ + 命令)
  - 接続：[Socket 5](https://ja.wikipedia.org/wiki/Socket_5 "wikilink") および [Socket 7](../Page/Socket_7.md "wikilink")
  - 電源電圧：VCore 3.52V
  - 外部バス：60 (PR120/150), 66 MHz
  - リリース時期：[1996年](../Page/1996年.md "wikilink")10月7日
  - 動作周波数：90 (PR120), 100 (PR133), 105 (PR150), 116.6 (PR166), 133 MHz (PR200)

注：PR200は計画されたものの、後継であるK6の製品化が迫っていたことから発売には至らなかった。

## 脚注

## 外部リンク

  - [AMD-K5プロセッサの概要](http://www.amd.com/jp-ja/Processors/ProductInformation/0,,30_118_1260_1264,00.html)

[Category:AMDのマイクロプロセッサ](https://ja.wikipedia.org/wiki/Category:AMDのマイクロプロセッサ "wikilink")
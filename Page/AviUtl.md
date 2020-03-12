> この記事は[AviUtl](https://ja.wikipedia.org/wiki/AviUtl)から翻訳されています。


**AviUtl**（エーブイアイユーテル,エーブイアイユーティル）は、KENくんによって開発されている\[1\][動画編集ソフトウェア](https://ja.wikipedia.org/wiki/動画編集ソフトウェア "wikilink")である。

## 概要

[AVIファイル](../Page/Audio_Video_Interleave.md "wikilink")を[編集したり](../Page/ノンリニア編集.md "wikilink")、各種[コーデック](../Page/コーデック.md "wikilink")で[圧縮することができる](../Page/エンコード.md "wikilink")。[フリーウェア](../Page/フリーウェア.md "wikilink")として公開されている。

動作には[MMX](../Page/MMX.md "wikilink")が使える[CPU](../Page/CPU.md "wikilink")が必要\[2\]。

AviUtl本体のみで編集は可能であるが、公式サイトに公開されている拡張編集プラグインを使用することでより高度な編集をすることができる。

拡張編集プラグインは[Lua](../Page/Lua.md "wikilink")を用いて複雑なアニメーションを作成する[スクリプト](../Page/スクリプト.md "wikilink")機能があり、有志により多数のスクリプトが公開されている。

有志により開発された[プラグイン](../Page/プラグイン.md "wikilink")を追加することで、各種エンコーダー（[x264](https://ja.wikipedia.org/wiki/x264 "wikilink")等）の使用が可能になる。

version1.10rc2からは、4GB以上のメモリーも利用出来るようになっている。

version0.99aからは[マルチスレッド](https://ja.wikipedia.org/wiki/マルチスレッド "wikilink")対応となり、主要なプラグインのマルチスレッド化が促進され[SIMD](../Page/SIMD.md "wikilink")最適化、[GPUの利用ができるようになる](../Page/Graphics_Processing_Unit.md "wikilink")。

[AviSynth](https://ja.wikipedia.org/wiki/AviSynth "wikilink")とはプラグインの相互利用が可能であるしかし、AviUtl側からAviSynthのプラグインを利用する際にプラグインがYUV各12ビットのフォーマットをサポートしていない場合、データの精度に変化が生じる場合がある。

[nicotalk](http://www.nicotalk.com/nicotalk.html)のように、AviUtlと連携したソフトウェアも存在する。

## 歴史

  - [1997年](https://ja.wikipedia.org/wiki/1997年 "wikilink")[11月](../Page/11月.md "wikilink") - 開発が始まる
  - [2003年](../Page/2003年.md "wikilink")[8月16日](../Page/8月16日.md "wikilink") - version0.99がリリース。
  - [2007年](../Page/2007年.md "wikilink")[11月3日](https://ja.wikipedia.org/wiki/11月3日 "wikilink") - version0.99aがリリース。
  - [2008年](https://ja.wikipedia.org/wiki/2008年 "wikilink") - 「拡張編集プラグイン」がリリース。
  - [2013年](../Page/2013年.md "wikilink")[4月1日](../Page/4月1日.md "wikilink") - Version1.00がリリース。
  - [2019年](../Page/2019年.md "wikilink")[8月18日](../Page/8月18日.md "wikilink") - Version1.10rc1がリリース。
  - [2019年](../Page/2019年.md "wikilink")[9月1日](../Page/9月1日.md "wikilink") - Version1.10rc2がリリース。
  - [2019年](../Page/2019年.md "wikilink")[10月3日](../Page/10月3日.md "wikilink") - Version1.10がリリース。

## プラグイン

Aviutlでは非常に多くのサード・パーティー製のプラグインが配布されており、これらを使用することで機能を拡張できる。

プラグインの拡張子は、「.dll」をリネームしただけで、以下の種類に分類されている。

|           |      |                  |
| --------- | ---- | ---------------- |
| フィルタプラグイン | .auf | 画像の加工編集          |
| 入力プラグイン   | .aui | 他のファイル形式を読み込む    |
| 出力プラグイン   | .auo | 他のファイル形式に出力      |
| 色変換プラグイン  | .auc | 画像データ入出力時の色空間を変換 |
| 言語拡張リソース  | .aul | 対応言語を拡張          |

## 注釈

<references group="注釈" />

## 出典

<references/>

## 関連項目

  - [AviSynth](https://ja.wikipedia.org/wiki/AviSynth "wikilink")
  - [Audio Video Interleave](../Page/Audio_Video_Interleave.md "wikilink") (AVI)
  - [コーデック](../Page/コーデック.md "wikilink")

## 外部リンク

  - [AviUtlのお部屋](http://spring-fragrance.mints.ne.jp/aviutl/) 公式サイト

[Category:フリーウェア](https://ja.wikipedia.org/wiki/Category:フリーウェア "wikilink") [Category:1997年のソフトウェア](https://ja.wikipedia.org/wiki/Category:1997年のソフトウェア "wikilink") [Category:映像編集・合成ソフト](https://ja.wikipedia.org/wiki/Category:映像編集・合成ソフト "wikilink")

1.
2.  [1](http://spring-fragrance.mints.ne.jp/aviutl/)
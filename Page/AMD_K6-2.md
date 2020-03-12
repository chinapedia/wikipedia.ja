> この記事は[AMD K6-2](https://ja.wikipedia.org/wiki/AMD_K6-2)から翻訳されています。


**AMD K6-2**は、[AMDが開発した](https://ja.wikipedia.org/wiki/アドバンスト・マイクロ・デバイセズ "wikilink")[x86](https://ja.wikipedia.org/wiki/x86 "wikilink")互換の[マイクロプロセッサ](../Page/マイクロプロセッサ.md "wikilink")である。

## 概要

[thumb](https://ja.wikipedia.org/wiki/ファイル:AMD-K6-2_350AMZ.jpg "wikilink") K6-2は[K6プロセッサをベースにAMD独自の](../Page/AMD_K6.md "wikilink")[SIMD](../Page/SIMD.md "wikilink")拡張命令である[3DNow\!](../Page/3DNow!.md "wikilink")を実装したプロセッサ。最初の[Super Socket 7](https://ja.wikipedia.org/wiki/Super_Socket_7 "wikilink") ([Socket 7の](../Page/Socket_7.md "wikilink")[FSBを](../Page/フロントサイドバス.md "wikilink")100 MHzに強化したもの) の製品となった。1次[キャッシュはデータ](../Page/キャッシュメモリ.md "wikilink")32Kバイトと命令32Kバイトの合計64Kバイト。[トランジスタ](../Page/トランジスタ.md "wikilink")数は930万個。クロック周波数は 300MHz / 333MHz / 350MHz / 366MHz / 380MHz / 400MHz / 450MHz / 475MHz / 500MHz / 533MHz / 550MHz。 前のCPUであるK6から[MMX](../Page/MMX.md "wikilink")演算性能が強化されており、MMXユニットが、レジスターXパイプライン、レジスタYパイプラインの両方にぶら下がっており、MMX命令が同時2命令発行に改良された。また、MMX乗算、MMXシフトはXY両レジスターパイプラインから共用される。それと同時に、二つのショートデコーダで[MMX](../Page/MMX.md "wikilink")命令のデコードが行えるように改良された(K6では片側のショートデコーダのみで行えた)。

350MHz以上のクロックの製品で、[Windows 95](../Page/Microsoft_Windows_95.md "wikilink") OSR2.x 起動時に「Windows 保護エラー」とメッセージを出して起動できないことがある。これに対する[パッチ](../Page/パッチ.md "wikilink")は[マイクロソフト](../Page/マイクロソフト.md "wikilink")側から提供された\[1\]。

## 各世代についての詳細

### K6-3D (Chomper)

  - 製造プロセス: 0.25 マイクロメートル
  - トランジスタ数: 930万個
  - 一次キャッシュ: データ 32 KB + 命令 32 KB
  - 拡張命令: MMX, 3DNow\!
  - バス: Socket 7 (Super Socket 7)
  - FSB: 66/100 MHz
  - クロック: 233/266/300/333/350 MHz
  - リリース時期: [1998年](https://ja.wikipedia.org/wiki/1998年 "wikilink")3月28日
  - 電圧: 2.2 V

### K6-3D (Chomper Extended)

  - 製造プロセス: 0.25 マイクロメートル
  - トランジスタ数: 930万個
  - 一次キャッシュ: データ 32 KB + 命令 32 KB
  - 拡張命令: MMX, 3DNow\!
  - バス: Socket 7 (Super Socket 7)
  - FSB: 66/95/97/100 MHz
  - クロック: 266 ～ 550 MHz
  - リリース時期: 1998年11月16日
  - 電圧: 2.2/2.3/2.4 V

### K6-2+（モバイルのみ）

K6-2+は、K6-IIIから2次キャッシュを半減させた製品で、名称にK6-2とあるが[K6-IIIの派生製品である](../Page/AMD_K6-III.md "wikilink")。K6-IIIは2次キャッシュをダイ上に実装したことで性能が向上したが、ダイサイズが大きくなったことから歩留まりが悪化してしまい、余裕の無かったAMDの製造能力をさらに逼迫させてしまうことになった。そこで性能と歩留まりのバランスをとるため、2次キャッシュを半減させることとなった。

  - 製造プロセス: 0.18 マイクロメートル
  - 1次キャッシュ: データ 32 KB + 命令 32 KB
  - 2次キャッシュ: 128 KB
  - 拡張命令: MMX, Enhanced 3DNow\!
  - バス: Socket 7 (Super Socket 7)
  - FSB: 100MHz
  - クロック: 450/475/500/533/550/570 MHz
  - リリース時期: [2000年](../Page/2000年.md "wikilink")4月18日
  - 電圧: 2.0 V

## 脚注

## 外部リンク

[AMD-K6-2プロセッサ](http://www.amd.com/jp-ja/Processors/ProductInformation/0,,30_118_1260_1217,00.html)

[Category:AMDのマイクロプロセッサ](https://ja.wikipedia.org/wiki/Category:AMDのマイクロプロセッサ "wikilink")

1.
> この記事は[AMD K6-III](https://ja.wikipedia.org/wiki/AMD_K6-III)から翻訳されています。


**AMD K6-III**は、[AMDが開発した](https://ja.wikipedia.org/wiki/アドバンスト・マイクロ・デバイセズ "wikilink")[x86](https://ja.wikipedia.org/wiki/x86 "wikilink")互換の[マイクロプロセッサ](../Page/マイクロプロセッサ.md "wikilink")である。

## 概要

**K6-III**は[AMD-K6-2プロセッサをベースに](../Page/AMD_K6-2.md "wikilink")2次[キャッシュを実装したプロセッサ](../Page/キャッシュメモリ.md "wikilink")。[3DNow\!](https://ja.wikipedia.org/wiki/3DNow! "wikilink")に対応、1次キャッシュはデータ32KB、命令32KBの合計64KB、[Super Socket 7](https://ja.wikipedia.org/wiki/Super_Socket_7 "wikilink")（[Socket 7](https://ja.wikipedia.org/wiki/Socket_7 "wikilink") のFSB 100MHz版）という点はK6-2に準じている。

Socket 7としては初めて2次キャッシュを実装し、その容量は256Kバイト。またCPUコアの動作周波数と同じ周波数で動作する。競合する[Pentium IIや](../Page/Pentium_II.md "wikilink")[Pentium IIIの](../Page/Pentium_III.md "wikilink")2次キャッシュは512KバイトであったがCPUコアの動作周波数の半分であり、また[Celeron](https://ja.wikipedia.org/wiki/Celeron "wikilink")はコアと等速ではあったが128Kバイトだった。2次キャッシュの実装により、従来の[マザーボード](https://ja.wikipedia.org/wiki/マザーボード "wikilink")上のキャッシュは3次キャッシュとして利用できる。その機能をAMDはマーケティング上の理由からTriLevelCacheと命名し、3次キャッシュとしてサポートされる外部SRAM容量は最大2Mバイトとなったが、当時市販されていたK6-III対応マザーボードおよびその[チップセット](../Page/チップセット.md "wikilink")で2MBのキャッシュメモリを実装あるいはサポートしたものはほぼ皆無で、大半は512KBあるいは1MB搭載であった。

K6-IIIは、AMDおよびSocket 7のプロセッサの中で最も高速なプロセッサとなった。「パフォーマンスはPentium IIIの1つ上のクロック周波数の製品と同等を実現している」とAMDは主張している。その根拠は、AMDの調査ではPentium IIIに比べWinstone 99を使用したベンチマークで[Windows 98上で](../Page/Microsoft_Windows_98.md "wikilink")6％、[Windows NT上で](../Page/Microsoft_Windows_NT.md "wikilink")4％高速、CPUMark 32ではインテルPentium IIIよりK6-IIIは30％高速であるとしている。実際は同一クロックのPentium IIIを上回った程度だとの見方が強い。これは、K6-IIIでは[浮動小数点演算](https://ja.wikipedia.org/wiki/浮動小数点演算 "wikilink")性能よりも整数演算性能の向上を重視した実装が行われた結果、[ベンチマーク](../Page/ベンチマーク.md "wikilink")テストにおいて浮動小数点演算能力がPentiumIIIより劣ると判断されたためである。

しかし、パーソナルコンピュータ (PC) 上でもっとも多く使用されている[アプリケーションソフトウェア](../Page/アプリケーションソフトウェア.md "wikilink")である[ワープロ](../Page/ワープロソフト.md "wikilink")・[表計算](../Page/表計算ソフト.md "wikilink")・[メーラーなどの](../Page/電子メールクライアント.md "wikilink")[オフィス系ソフトでは浮動小数点演算性能は使用感の向上にはほとんど寄与せず](../Page/オフィススイート.md "wikilink")、整数演算性能やクロックの向上、それにメモリアクセス性能の改善が体感性能に直接的な影響を及ぼす。このため、大容量の2次キャッシュを実装し浮動小数点演算能力の重視よりも使用頻度の高いオフィス系ソフトの使用感を向上させることを念頭に置いたこのプロセッサは、特にSocket 7マシンのままで実用的な性能の向上を求めるユーザー層に強く支持された。

もっとも、K6-IIIはK6-2のコアに[SRAMを付加した設計となったために](../Page/Static_Random_Access_Memory.md "wikilink")[トランジスタ](../Page/トランジスタ.md "wikilink")数は2130万と大規模化し、当時AMDのチップ製造ラインで使用可能であった製造プロセスの制約から、そのシリコンダイのサイズをK6-2の81mmから118mm\[1\]へと巨大化せざるを得なかった。それゆえ、このチップは量産時の製造歩留まりの改善が困難であったと伝えられている。その結果、価格もK6-2とは比較にならないほど高価に設定されており、既存Socket 7系マシンのアップグレード手段としては歓迎されたものの、メーカー製PCにおいてはこのCPUを採用する例はほぼ皆無であった。

K6-2およびK6-IIIは、AMDが独自に定義したマルチメディア拡張命令セットである3DNow\!を使用することで同クロックのPentiumIIIを凌駕する浮動小数点演算能力を発揮する。だが、この3DNow\!を利用するためのソフトウェア開発環境が整備されておらず、AMDによる支援策は[ライブラリ](../Page/ライブラリ.md "wikilink")の提供にとどまったため、この命令セットを利用するソフトウェアはあまり普及しなかった。もっとも、[グラフィックカード](https://ja.wikipedia.org/wiki/グラフィックカード "wikilink")などの[ドライバではこの新命令セットを積極的に活用する例が見られ](../Page/デバイスドライバ.md "wikilink")、当時3Dグラフィックチップの雄として知られた[3dfx](../Page/3dfx.md "wikilink")社のVoodooシリーズ用ドライバがこの命令への対応を明言していたことが知られている。

このCPUは、次世代CPU ([K7](https://ja.wikipedia.org/wiki/K7 "wikilink")) である[Athlon](../Page/Athlon.md "wikilink")が発売されたことで、Athlonの性能と[K6-2の価格との狭間で存在意義が薄れ](../Page/AMD_K6-2.md "wikilink")、より収益の大きいAthlonの製造数を確保するためにメインストリーム向けの生産が打ち切られた。ただし、製造プロセスを縮小して歩留まりの問題を改善したK6-III+（0.18μm版K6-III）やK6-III+の内蔵2次キャッシュ容量を半減したK6-2+といった同系の後継製品が主にモバイル向けとして出荷された。

これらについてはK6-IIIに比して内蔵2次キャッシュの[レイテンシ](../Page/レイテンシ.md "wikilink")が若干増やされており、このためK6-III+は同一クロックのK6-IIIと比較すると処理速度がやや劣る。ただし、製造プロセスのシュリンクによって動作クロック周波数がK6-IIIの最大450MHzから最大550MHz（公称）\[2\]に引き上げられ、3DNow\!命令もAthlon向けの改良を反映して多少の修正が加わったEnhanced 3DNow\!となっており、また製造プロセス変更による低発熱化も実現されているため、総合的には改良あるいは改善されていることになる。

## 各世代についての詳細

### "Sharptooth"（K6-3D+）

  - プロセス：0.25マイクロメートル
  - トランジスタ：2130万個
  - 一次キャッシュ：データ32KB,命令32KB
  - 二次キャッシュ：256KB
  - 拡張命令：MMX,3DNow\!
  - バス：Socket 7 (Super 7)
  - FSB：100MHz
  - クロック：400／450MHz
  - リリース時期：[1999年](../Page/1999年.md "wikilink")2月22日
  - 電圧：2.2／2.4V

### K6-III+（モバイルのみ）

  - プロセス：0.18マイクロメートル
  - トランジスタ：2130万個
  - 一次キャッシュ：データ32KB,命令32KB
  - 二次キャッシュ：256KB
  - 拡張命令：MMX,Enhanced 3DNow\!
  - バス：Socket 7 (Super 7)
  - FSB：100MHz
  - クロック：450／475／500／550MHz
  - リリース時期：[2000年](../Page/2000年.md "wikilink")4月18日
  - 電圧：2.0V

## 脚注

## 外部リンク

  - [AMD-K6-IIIプロセッサ](http://www.amd.com/jp-ja/Processors/ProductInformation/0,,30_118_1260_1288,00.html)
  - [CPU World内のコンテンツ](http://www.cpu-world.com/CPUs/K6-III/)（K6-IIIの画像が掲載されている）

## 関連項目

  - [AMD K6](../Page/AMD_K6.md "wikilink")
  - [AMD K6-2](../Page/AMD_K6-2.md "wikilink")
  - [Athlon](../Page/Athlon.md "wikilink")
  - [アドバンスト・マイクロ・デバイセズ](https://ja.wikipedia.org/wiki/アドバンスト・マイクロ・デバイセズ "wikilink")

[Category:AMDのマイクロプロセッサ](https://ja.wikipedia.org/wiki/Category:AMDのマイクロプロセッサ "wikilink")

1.
2.  K7系製品との競合を避けるマーケティング戦略上の配慮から公称動作クロック周波数は550MHzに抑えられた。ただし、バッファローが限定的に販売したCPUアクセラレータでは選別品を搭載したとして、600MHz駆動を製品レベルの定格値として行っている。
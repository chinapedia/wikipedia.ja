> この記事は[NCUBE](https://ja.wikipedia.org/wiki/NCUBE)から翻訳されています。


**nCUBE**は、[超並列](https://ja.wikipedia.org/wiki/並列コンピューティング "wikilink")[コンピュータ](../Page/コンピュータ.md "wikilink")のシリーズ名であるとともにそれを開発した企業名でもある。初期のハードウェアは独自の[マイクロプロセッサ](../Page/マイクロプロセッサ.md "wikilink")を使っていた。その後、独自のマイクロプロセッサの設計をやめて、サーバ向けの他社製チップで[超並列マシン](../Page/超並列マシン.md "wikilink")を作成。最近まで[ストリーミング](../Page/ストリーミング.md "wikilink")配信（[ビデオ・オン・デマンド](../Page/ビデオ・オン・デマンド.md "wikilink")）に特化したサーバとして販売していた。現在はC-CORというネットワーク関連の企業に買収されている。

## 歴史

  - [1983年](https://ja.wikipedia.org/wiki/1983年 "wikilink") - [インテル](https://ja.wikipedia.org/wiki/インテル "wikilink")の社員が、インテルが[並列コンピューティング](https://ja.wikipedia.org/wiki/並列コンピューティング "wikilink")市場になかなか踏み出さないことに欲求不満を感じ、nCUBE社を設立した（インテルはその後[1989年](../Page/1989年.md "wikilink")に市場に参入）。
  - [1985年](https://ja.wikipedia.org/wiki/1985年 "wikilink")12月 - 最初のnCUBEの[ハイパーキューブマシン](../Page/超立方体.md "wikilink")**nCUBE 10**がリリースされる。
  - [1988年](../Page/1988年.md "wikilink") - [オラクル社の](https://ja.wikipedia.org/wiki/オラクル_\(企業\) "wikilink")[ラリー・エリソン](../Page/ラリー・エリソン.md "wikilink")はnCUBEに興味を持ち大株主となった。nCUBE社の本社はオラクル社のすぐ近くに移転されることとなった。
  - [1989年](../Page/1989年.md "wikilink")6月 - 第二世代のマシン**nCUBE 2**をリリース。
  - [1994年](../Page/1994年.md "wikilink") - nCUBEは株式上場するまでに成長した。
  - [1995年](https://ja.wikipedia.org/wiki/1995年 "wikilink") - 第三世代のマシン**nCUBE 3**をリリース。
  - [1996年](../Page/1996年.md "wikilink") - エリソンは nCUBE を縮小（上場廃止）させ、CEOに就任してオラクル社の[ネットワークコンピュータ](https://ja.wikipedia.org/wiki/ネットワークコンピュータ "wikilink")部門に編入した。その後、nCUBE社は完全にストリーミング配信サーバのメーカーとなる。
  - [1999年](../Page/1999年.md "wikilink") - nCUBE社はストリーミング配信とそれにCMを挿入するソフトウェアを開発していた SkyConnect というベンチャー企業を買収した後、再度株式公開にこぎつけた。
  - [2000年](../Page/2000年.md "wikilink") - SeaChange International社から特許侵害で訴えられる。
  - [2001年](../Page/2001年.md "wikilink")
      - 再度、上場廃止。
      - 4月：ITバブル崩壊と法廷闘争の負担から、nCUBE社は 17%の従業員をレイオフ（解雇）。
      - エリソンがCEOを辞めた。
  - [2002年](../Page/2002年.md "wikilink") - Foster Cityのオフィスを閉鎖。
  - [2003年](../Page/2003年.md "wikilink") - Louisvilleのオフィスを閉鎖。
  - [2005年](../Page/2005年.md "wikilink") - C-COR社に買収される。
  - [2007年](../Page/2007年.md "wikilink") - Arris社に買収される。

## 詳細

### nCUBE 10（1985年）

  - 最大1024個のプロセッサモジュールを10次元の[ハイパーキューブと呼ばれる形のネットワークで接続している](../Page/超立方体.md "wikilink")。
  - プロセッサモジュール詳細
      - [CPU](../Page/CPU.md "wikilink"): 32ビット、2[MIPS](https://ja.wikipedia.org/wiki/MIPS "wikilink")
      - [FPU](../Page/FPU.md "wikilink"): 64ビット、[単精度](https://ja.wikipedia.org/wiki/単精度 "wikilink") 500K[FLOPS](../Page/FLOPS.md "wikilink")、[倍精度](https://ja.wikipedia.org/wiki/倍精度 "wikilink") 300KFLOPS
      - メモリ: 128Kバイト [RAM](../Page/Random_Access_Memory.md "wikilink")
      - [オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink"): Vertexが各モジュールで動作
  - 一部のプロセッサモジュールは入出力用として周辺デバイスと接続されている。
  - nCUBE 10同士を接続することも可能

### nCUBE 2（1989年）

  - 最大4096個のプロセッサを12次元のハイパーキューブ接続で構成。
  - プロセッサモジュール詳細
      - CPU: 32ビット、7MIPS
      - FPU: 64ビット、3.5MFLOPS
      - メモリ: 4～16Mバイト RAM（I/O用プロセッサモジュールはRAMが少ない）
      - 13本のI/Oチャネル（各20Mビット/s）のうち12本がプロセッサ間のハイパーキューブ接続に使用され、1本をI/Oに使用。[ワームホール・ルーティング](https://ja.wikipedia.org/wiki/ワームホール・ルーティング "wikilink")でCPU間メッセージを転送。
      - オペレーティングシステム: nCX[マイクロカーネル](https://ja.wikipedia.org/wiki/マイクロカーネル "wikilink")
      - 1プロセッサモジュール、2プロセッサモジュール、4プロセッサモジュールがある。
  - 入出力: [SCSI](../Page/Small_Computer_System_Interface.md "wikilink")、[HIPPI](../Page/HIPPI.md "wikilink")など

フロントエンドとして[サン・マイクロシステムズ](../Page/サン・マイクロシステムズ.md "wikilink")などの[ワークステーション](../Page/ワークステーション.md "wikilink")を使用する。**nCX**マイクロカーネルは200Kバイトで、ファイル操作を最大96分割して96個のCPUが並行して処理することができる。[C言語](../Page/C言語.md "wikilink")と[C++](../Page/C++.md "wikilink")、NQS、Linda、ParasoftのExpressなどが動作した。オラクル社と共同で[Oracle Databaseも移植され](../Page/Oracle_Database.md "wikilink")、高性能データベースマシンとしても販売された。このときの技術がのちの[Oracle 10gの](../Page/Oracle_Database.md "wikilink")[グリッド・コンピューティング](../Page/グリッド・コンピューティング.md "wikilink")技術につながっている。実際に納入された最大のnCUBE 2システムは Sandia National Laboratories の 1024プロセッサモデルで、1.91GFLOPSの性能を記録している。

### nCUBE 3（1995年）

  - 最大65536個のプロセッサを16次元のハイパーキューブ接続で構成。
  - プロセッサは64ビットで50MHzで動作し、[スーパースケーラ](https://ja.wikipedia.org/wiki/スーパースケーラ "wikilink")機能と16Kバイトの命令[キャッシュ](../Page/キャッシュメモリ.md "wikilink")、[MMUを内蔵して仮想記憶をサポート](../Page/メモリ管理ユニット.md "wikilink")。
  - I/Oチャネルは18本でそれぞれ100Mビット/sである。従来（シリアル）と異なり2ビットパラレルとなったため、ルーティングにフォールトトレラント性を持たせることもできた。
  - 最大構成のnCUBE 3は3TIPS（MIPSの100万倍）、6.5TFLOPSの性能となるが、もちろん最大構成のマシンが納入されたことはない。

## 関連項目

  - [トランスピュータ](../Page/トランスピュータ.md "wikilink")
  - [iWarp](https://ja.wikipedia.org/wiki/iWarp "wikilink")

## 外部リンク

  - [A Quantum Multicomputer](http://www.tera.ics.keio.ac.jp/person/rdv/quantum/quantum-multicomputer.html) （英語） - Cosmic Cubeの写真がある
  - [Parallel Computing Hardware](http://www.pact.sscc.ru/hardware/computer/) （英語） - いろいろな並列コンピュータの写真が並んでいる。とくに超並列マシンは個性的な形をしたものが多い。nCUBE2Sの写真もある。

[Category:スーパーコンピュータ](https://ja.wikipedia.org/wiki/Category:スーパーコンピュータ "wikilink") [Category:並列コンピューティング](https://ja.wikipedia.org/wiki/Category:並列コンピューティング "wikilink") [Category:かつて存在したアメリカ合衆国のコンピュータ企業](https://ja.wikipedia.org/wiki/Category:かつて存在したアメリカ合衆国のコンピュータ企業 "wikilink")
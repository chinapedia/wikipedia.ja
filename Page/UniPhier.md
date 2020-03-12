> この記事は[UniPhier](https://ja.wikipedia.org/wiki/UniPhier)から翻訳されています。


**UniPhier**（ユニフィエ）とは、松下電器（現[パナソニック](https://ja.wikipedia.org/wiki/パナソニック "wikilink")）が開発した[デジタル家電向けの統合プラットフォームの名称で](../Page/デジタル家庭電化製品.md "wikilink")、[株式会社ソシオネクスト](https://ja.wikipedia.org/wiki/株式会社ソシオネクスト "wikilink")の[登録商標](https://ja.wikipedia.org/wiki/登録商標 "wikilink")である（日本第4810847号。ただし読みは「ユニフィアー，ユニファイアー」で登録）。

## 概要

[CPU](../Page/CPU.md "wikilink")とビデオコーデック等を内蔵した[システムLSI](../Page/システムLSI.md "wikilink")と、[OSと](../Page/オペレーティングシステム.md "wikilink")[ミドルウェア](../Page/ミドルウェア.md "wikilink")等から成る[ソフトウェア](../Page/ソフトウェア.md "wikilink")プラットフォームで構成されるデジタル家電用の統合プラットフォーム。その名称は、"Universal Platform for High-quality Image Enhancing Revolution"の略である。 CPUには[ARMアーキテクチャ](../Page/ARMアーキテクチャ.md "wikilink")またはパナソニック独自アーキテクチャ（AMシリーズ）を採用している。

[スクウェア・エニックス](../Page/スクウェア・エニックス.md "wikilink")もミドルウェア・[SEAD Engine](https://ja.wikipedia.org/wiki/SEAD_Engine "wikilink")（Square Enix Application on Demand Engine）を提供している。

従来は[携帯電話](../Page/携帯電話.md "wikilink")や[DVDレコーダー](../Page/DVDレコーダー.md "wikilink")、デジタル[テレビ](../Page/テレビ.md "wikilink")など各製品群ごとに[ハードウェア](../Page/ハードウェア.md "wikilink")を用意し、そこから[マイクロコードやOS](../Page/マイクロプログラム方式.md "wikilink")、ミドルウェア、[アプリケーションソフトウェア](../Page/アプリケーションソフトウェア.md "wikilink")などを個別に開発してきたが、UniPhierによる統合プラットフォームでは、ベースハードウェアの上に各製品固有なソフトウェアを開発するだけで済むため、ソフトウェア開発効率を高めることができる。設計開発はパナソニック株式会社 デバイス社が行っている。

UniPhierには、高品位[AV](https://ja.wikipedia.org/wiki/オーディオ・ビジュアル "wikilink")（パナソニックの高画質、高音質技術集約）、低[消費電力](https://ja.wikipedia.org/wiki/消費電力 "wikilink")（AV機器の長時間動作）、[リアルタイム処理](https://ja.wikipedia.org/wiki/リアルタイムシステム "wikilink")（複数のAV処理でもスムーズ動作）、セキュア機構（AVコンテンツ、個人データ保護）などの特徴があり、低消費電力を求められる携帯電話分野、高性能な[コーデック](../Page/コーデック.md "wikilink")処理を要求されるホームAV機器など、製品分野に最適なシステムLSIとして選択できる。

[VIERA](../Page/VIERA.md "wikilink")に搭載している画質改善エンジン「PEAKS[プロセッサ](../Page/プロセッサ.md "wikilink")」なども順次UniPhierに統合された。

## プロセッサ

### 携帯電話用

  - UniPhier　M

<!-- end list -->

  -
    P901iTVに搭載

<!-- end list -->

  - UniPhier 3M

<!-- end list -->

  -
    P903i、P903iTV、P903iX、P904iなどに搭載

<!-- end list -->

  - UniPhier 4M

<!-- end list -->

  -
    65nmプロセスで製造されており省電力化されている。また、P905i、P906iなどに搭載

<!-- end list -->

  - UniPhier 4MBB+

<!-- end list -->

  -
    45nmプロセスで製造されており、HSDPA 7.2Mbpsに対応。P-01Aなどに搭載

### カーAV/ホームAV用

  - PH1-Lite II

<!-- end list -->

  -
    デジタルテレビ向け。派生LSIとしてPH1-Lite IIS、PH1-Lite IIPが存在

<!-- end list -->

  - PH1-Pro(品番：MN2WS0030）

<!-- end list -->

  -
    65nmプロセスで製造されている。CPUコアのクロックは300MHz。DMR-BW200などに搭載

<!-- end list -->

  - PH1-Pro II(品番：MN2WS0038)

<!-- end list -->

  -
    45nmプロセスで製造されており、CPUコアのクロックを350MHzまで向上、H.264HP enc/decを搭載させながら省電力化している。
    またメモリはDDR2-800に対応させ、新たに周辺機能としてIEEE1394を統合した。DMR-BW800などに搭載

<!-- end list -->

  - PH1-Pro IIP(品番：MN2WS0043)

<!-- end list -->

  -
    45nmプロセスで製造されている。BDプレーヤー向け。H.264HPエンコーダが省かれている。

<!-- end list -->

  - UniPhier4H-DTV1(品番：MN2WS0052)

<!-- end list -->

  -
    45nmプロセスで製造されている。デジタルテレビ向け。グローバル対応、H264デコーダ搭載、HE-AAC対応。

<!-- end list -->

  - PH1-Pro 3(品番：MN2WS0140)

<!-- end list -->

  -
    45nmマルチVtプロセスで製造されており、CPUコアのクロックは最大500MHzまで向上、従来のキャッシュメモリにあたるL1キャッシュは命令/データ共に2倍の32KBとし、L2キャッシュを128KB内蔵した。
    外部メモリはDDR3-1333に対応、周辺機能としてUSBやEthernetコントローラを統合し、シリアルATAとSDカードの同時接続数をそれぞれx2、x3と増やしている。DMR-BWT3000などに搭載

<!-- end list -->

  - BDP用システムLSI（品番：MN2WS0150）

<!-- end list -->

  -
    32nmゲートファースト・マルチVthプロセスで製造され、High-k/メタルゲートトランジスタの採用、CPUコアのクロックは486MHz。
    MPEG-4 MVC対応・周辺機能の強化をしながら、LSI消費電力で約40％、実装面積で約30％の削減が謳われている。

<!-- end list -->

  - スマートテレビ用UniPhier-DTV（品番：MN2WS0220）

<!-- end list -->

  -
    45nmプロセスで製造。メインCPUを独自開発の「AM34」の2CPU構成から、ARMの「Cortex-A9」のデュアルコア構成へと変更、最大1.4GHzで動作する。
    メディアプロッサは従来同様UniPhierプロセッサだが、実行ユニットがIPP3となり、L2キャッシュをメインCPUと共有化、800MHzで動作する。
    グラフィックスはOpenGL ES 2.0、OpenGL ES 1.1対応。AV入出力機能として2D-3D変換、3Dフォーマッタなどの表示制御機能を搭載し、4ポートまでのHDMIに対応。
    外部メモリはDDR3-1600対応。メインCPU、メディアプロッサ、グラフィックス回路の間で共有するユニファイドメモリアーキテクチャとなっている。

<!-- end list -->

  - PH1-Pro4（品番：MN2WS0230）

<!-- end list -->

  -
    MN2WS0220をベースに4K・多チャンネル同時処理に対応した高画質・多チャンネル対応配信向けシステムLSI。

<!-- end list -->

  - Blu-rayプレーヤ用システムLSI（品番：MN2WS0260）

<!-- end list -->

  -
    光ディスクコントローラやDRC、タイマなどのフロントエンド部、HDMI (ver1.4) 等の周辺IFを統合。外付けメモリのデータバス幅32-bit化。CPUはAM34-SMP x2、486 MHz。

<!-- end list -->

  - 高性能・合理化対応スマート端末用システムLSI PH1-sLD8(品番：MN2WS0270シリーズ)

<!-- end list -->

  -
    シングルコアのARM Cortex-A9と高速並列メディア処理プロセッサ (IPP3) を搭載し、新たに分散処理ソフトアーキテクチャを採用した、普及型スマート端末向けシステムLSI。

<!-- end list -->

  - PH1-Pro5（品番：MN2WS0300）

<!-- end list -->

  -
    CPUにARM Cortex-A9 1.2GHz クアッドコア、メディアプロセッサにIPP 3.3 1.2GHzを搭載。HEVC(H.265)形式4K/60p動画のリアルタイムデコードや8K4Kへのアップコンバートに対応。

<!-- end list -->

  - 4Kメディア再生用 1チップLSI (品番：MN2WS03101AA)

<!-- end list -->

  -
    HDCP2.2対応 HDMI2.0 Tx/ Rx のPHY内蔵。Blu-rayプレーヤーなど4K映像ボックスシステム用のアプリケーションLSI。PH1-Pro5と同じアーキテクチャを使用。

## 搭載製品

  - [VIERA](../Page/VIERA.md "wikilink")
  - [DIGA](https://ja.wikipedia.org/wiki/DIGA "wikilink")
  - [携帯電話](../Page/携帯電話.md "wikilink")
      - [P901iTV](../Page/P901iTV.md "wikilink") パナソニックの携帯電話としては初めて搭載した機種。
      - [P903iTV](../Page/P903iTV.md "wikilink")
      - [P905i](../Page/P905i.md "wikilink")
      - [P905iTV](../Page/P905iTV.md "wikilink")
      - [P906i](https://ja.wikipedia.org/wiki/P906i "wikilink")
      - [P-01A](https://ja.wikipedia.org/wiki/P-01A "wikilink")
      - [P-07A](https://ja.wikipedia.org/wiki/P-07A "wikilink")
  - [デジタルビデオカメラ](https://ja.wikipedia.org/wiki/デジタルビデオカメラ "wikilink")
  - [REAL Blu-ray](../Page/リアル_\(三菱電機\).md "wikilink") [三菱電機](../Page/三菱電機.md "wikilink")の[ブルーレイディスクレコーダーであるが](https://ja.wikipedia.org/wiki/BDレコーダー "wikilink")、基幹システムとして搭載されている。

## 関連項目

  - [VIERA](../Page/VIERA.md "wikilink")
  - [VIERAケータイ](../Page/VIERAケータイ.md "wikilink")

## 外部リンク

  - [UniPhierの紹介（セミコンダクター社）](http://www.semicon.panasonic.co.jp/jp/products/systemlsis/uniphier/index.html)
  - [松下、デジタル家電用の統合プラットフォーム「UniPhier」 - AV Watch](http://www.watch.impress.co.jp/av/docs/20040901/pana1.htm)(2004.9)
  - [UniPhier®（ユニフィエ）上にシームレス・コンテンツの開発および利用環境を共同構築（松下電器、2006.4）](http://panasonic.co.jp/corp/news/official.data/data.dir/jn060407-1/jn060407-1.html) - スクウェア・エニックスも開発に参画

[Category:パナソニックの製品](https://ja.wikipedia.org/wiki/Category:パナソニックの製品 "wikilink") [Category:AV機器](https://ja.wikipedia.org/wiki/Category:AV機器 "wikilink") [Category:携帯電話端末_(パナソニック_モバイルコミュニケーションズ)](https://ja.wikipedia.org/wiki/Category:携帯電話端末_\(パナソニック_モバイルコミュニケーションズ\) "wikilink") [Category:登録商標](https://ja.wikipedia.org/wiki/Category:登録商標 "wikilink")
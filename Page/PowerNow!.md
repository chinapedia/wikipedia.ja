> この記事は[PowerNow!](https://ja.wikipedia.org/wiki/PowerNow!)から翻訳されています。


**PowerNow\!**とは[アドバンスト・マイクロ・デバイセズ](https://ja.wikipedia.org/wiki/アドバンスト・マイクロ・デバイセズ "wikilink")(AMD)の開発した[CPU](../Page/CPU.md "wikilink")に搭載されている省電力技術のことである。システムに対する負荷に応じて動作周波数を最大定格よりも下方に修正することで省電力化を実現できる。同様の技術としてTransmeta社の[LongRun](https://ja.wikipedia.org/wiki/LongRun "wikilink")がある。拡張PowerNow\!はサーバ及びワークステーション向けのプロセッサに搭載されるが、同社の[Cool'n'Quiet](https://ja.wikipedia.org/wiki/Cool'n'Quiet "wikilink")との明確な技術的差はあまり認められない。このためこの項目では無印PowerNow\!のについて主に解説する。

## 技術の使用目的

モバイル向けのプロセッサの場合、性能と消費電力との兼ね合いが重要になってくる。これはたとえ高性能であってもバッテリという足かせがあり、さらに長時間の稼動できなければモバイル向けのコンピュータには採用できないからである。このPowerNow\!の技術が導入される前まではOSの稼動中に動作周波数を変更することは不可能であった。このため、ノートパソコンをコンセントにつないで消費電力の幅に許容が生まれた場合であっても、デスクトップパソコン並みに[CPU](../Page/CPU.md "wikilink")の性能を上げるには一回再起動を行い、[BIOSで](https://ja.wikipedia.org/wiki/Basic_Input/Output_System "wikilink")[FSBの再設定を行う必要があった](https://ja.wikipedia.org/wiki/フロントサイドバス "wikilink")。しかし、この技術を導入することによって、稼動中でも動作周波数の変更が出来るようになった。このためユーザーは、モバイルのときは消費電力を下げるために低周波数で、コンセント接続時で潤沢に電源が取れる場合は高周波数で、という状況に応じた作業を意識せずとも、自動的に行えるようになった。

## 3つのモード

これらの機能を有効利用できるのは特定のチップセット、BIOS及び対応するOSが必要である。また当然AMDの提供するドライバも必要である。

1.  ハイパフォーマンスモード
      - バッテリー稼動状態でもコンセントからの電源供給状態でも、電源の状況いかんにかかわらずそのプロセッサの最大の性能を発揮できるようなモード。当然バッテリのもちは悪くなる。
2.  バッテリーセーフモード
      - バッテリー稼動状態のときプロセッサの消費電力を最小に抑え、長時間駆動を可能にするモード。当然バッテリのもちは良くなるが、それに対し性能は落ちる。
3.  オートマティックモード
      - システムの負荷に応じて多段階に動作周波数を変化させるモード。長時間駆動とプロセッサ性能のバランスを配慮したモード。AMDではこのモードを奨励している。

## AMD PowerNow\!テクノロジが搭載されたCPU

もともとモバイル向けに開発されたものであることが製品名からも伺える。

  - Mobile [K6-2+](https://ja.wikipedia.org/wiki/AMD_K6-2 "wikilink")
  - Mobile [K6-III+](https://ja.wikipedia.org/wiki/AMD_K6-III "wikilink")
  - Mobile [Athlon 4](../Page/Athlon.md "wikilink")
  - Mobile [Duron](../Page/Duron.md "wikilink")
  - Mobile [Athlon XP-M](https://ja.wikipedia.org/wiki/Athlon#モバイルAthlon_XP-M "wikilink")
  - Mobile [Sempron](https://ja.wikipedia.org/wiki/Sempron "wikilink")

## 拡張 AMD PowerNow\!テクノロジが搭載されているCPU

現在このブランドが使われているのはモバイル向けとサーバ向けのプロセッサである。

  - AMD [Turion X2 Ultra](../Page/Turion_X2_Ultra.md "wikilink")
  - AMD [Turion 64 X2](https://ja.wikipedia.org/wiki/Turion_64_X2 "wikilink")
  - AMD Turion X2
  - AMD Athlon 64 X2 Dual-Core for Notebooks
  - AMD Athlon X2 Dual-Core for Notebooks (Turion X2 Ultraベースを除く)
  - AMD Sempron for Notebooks
  - AMD [Opteron](https://ja.wikipedia.org/wiki/Opteron "wikilink") (Quad Core)

## 関連項目

  - [Cool'n'Quiet](https://ja.wikipedia.org/wiki/Cool'n'Quiet "wikilink")
  - [Intel SpeedStep テクノロジ](https://ja.wikipedia.org/wiki/Intel_SpeedStep_テクノロジ "wikilink")

## 外部リンク

  - [AMD Opteron 電力効率](http://www.amd.com/jp-ja/0,,3715_12353,00.html)
  - [AMD PowerNow\!概要](http://www.amd.com/jp-ja/Processors/ProductInformation/0,,30_118_10220_10221%5E964,00.html)

[Category:マイクロプロセッサ](https://ja.wikipedia.org/wiki/Category:マイクロプロセッサ "wikilink")
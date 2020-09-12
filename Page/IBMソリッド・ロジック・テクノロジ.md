> この記事は[IBMソリッド・ロジック・テクノロジ](https://ja.wikipedia.org/wiki/IBMソリッド・ロジック・テクノロジ)から翻訳されています。


[サムネイル](https://ja.wikipedia.org/wiki/ファイル:Slt1.jpg "wikilink") [サムネイルの展示](https://ja.wikipedia.org/wiki/ファイル:IBM_SLT_wafers.agr.JPG "wikilink")。 \]\] [サムネイル](https://ja.wikipedia.org/wiki/ファイル:IBM_SLT_cards,_three.agr.jpg "wikilink") [サムネイル](https://ja.wikipedia.org/wiki/ファイル:SLT_Card_Frame.corestore.jpg "wikilink") [サムネイルのSLTモジュール](https://ja.wikipedia.org/wiki/ファイル:IBM_129_SLT_modules.jpg "wikilink") \]\] **ソリッド・ロジック・テクノロジ (Solid Logic Technology** = **SLT)** は、[IBM](../Page/IBM.md "wikilink")が1964年にIBM [System/360](https://ja.wikipedia.org/wiki/System/360 "wikilink")シリーズと関連機器で導入した電子回路をパッケージングするためのの手法である。\[1\] IBMは、セラミック基板上に[シルクスクリーン](../Page/シルクスクリーン.md "wikilink")印刷された[抵抗器](../Page/抵抗器.md "wikilink")を使用してSLTモジュールを形成し、ディスクリート・[フリップチップ](https://ja.wikipedia.org/wiki/フリップチップ "wikilink")実装、[ガラス](https://ja.wikipedia.org/wiki/ガラス "wikilink")封印された[トランジスタ](../Page/トランジスタ.md "wikilink")と[ダイオード](../Page/ダイオード.md "wikilink")を使用したカスタム[ハイブリッド回路](https://ja.wikipedia.org/wiki/ハイブリッド回路 "wikilink")を設計することを選択した。 回路は、プラスチックで封印されているか、金属製の蓋で覆われていた。これらのSLTモジュールのいくつか（右の画像では20個）を小型の多層[プリント基板](../Page/プリント基板.md "wikilink")に実装してSLTカードを作った。各SLTカードの片方の端にはソケットがあり、コンピューターの[バックプレーン](../Page/バックプレーン.md "wikilink")のピンに差し込むようになっていた（他のほとんどの会社のモジュールの実装方法とは逆）。

IBMは当時、[モノリシック集積回路技術はあまりにも未熟であると考えていた](../Page/集積回路.md "wikilink")\[2\] 。SLTは1964年の画期的な技術で、[標準モジュラーシステム](https://ja.wikipedia.org/wiki/IBM標準モジュラーシステム "wikilink")(Standard Modular System = SMS) のような初期のパッケージング技術よりもはるかに高い回路密度と信頼性の向上を実現した。この技術は、1960年代にIBM System/360メインフレーム・ファミリーを圧倒的な成功に導いた。SLTの研究はボールチップアセンブリ、ウェハーバンピング、トリミングされた厚膜抵抗器、印刷されたディスクリート機能、チップコンデンサ、およびハイブリッド厚膜技術の大量使用の一つを生み出した。

SLTは、それ以前の標準モジュラーシステムに取って代わったが、その後のSMSカードの中にはSLTモジュールを搭載したものもあった。

## 詳細

SLTでは、シリコン製の平面ガラス封止型トランジスタとダイオードを使用している。\[3\]

SLTは、デュアルダイオードチップと、それぞれ約0.025インチ角の個別のトランジスタチップを使用している\[4\] 。チップは0.5インチ角の基板上にシルクスクリーン印刷された抵抗器と印刷された接続部でマウントされる。全体は0.5インチ角モジュールを形成するためにカプセル化されている。各カードには6〜36個のモジュールが搭載されている。カードは、フレームを形成するゲートを形成する基板に接続されている。

SLTの電圧レベルは、ロジック・ローからロジック・ハイまで、回路速度によって変化する:\[5\] 。

  -
    高速 (5-10 ns) 0.9〜3.0V
    中速 (30 ns) 0.0〜3.0V
    低速 (700 ns) 0.0〜12.0V

## その後の開発

[サムネイル](https://ja.wikipedia.org/wiki/ファイル:Modulo_per_computer_tipo_SLT_\(Solid_Logic_Technology\)_-_Museo_scienza_tecnologia_Milano_D1188.jpg "wikilink") IBMが徐々にモノリシック集積回路の使用に移行してゆく中で、SLTに取って代わるデバイスにも同じ基本的なパッケージング技術 (デバイスとモジュールの両方) が使用された。

  - Solid Logic Dense (SLD) は、ディスクリートのトランジスタとダイオードを基板の上側に、抵抗を下側に実装することで、パッケージング密度と回路性能を向上させた \[6\] 。SLDの電圧はSLTと同じであった。

<!-- end list -->

  - Advanced Solid Logic Technology (ASLT)は、2枚の基板を同じパッケージに積層することで、パッケージ密度と回路性能を向上させた。ASLTは、 [電流ステアリング・ロジックで使用される](../Page/エミッタ結合論理.md "wikilink")[エミッタ・フォロワ結合スイッチをベースにしている](../Page/エミッタ結合論理.md "wikilink")。 ASLTの電圧レベルは、\> +235 mV がハイ、\<-239 mVがローとした。

<!-- end list -->

  - Monolithic System Technology (MST)は、ディスクリートのトランジスタとダイオードを1〜4個のモノリシック集積回路 (抵抗器がモジュール上のパッケージから外付けになった) に置き換えることで、パッケージング密度と回路性能を向上させた。 各MSTチップには約5つの回路が搭載されており、SLTカードとほぼ同じ大きさとなっている。  回路には[NPNトランジスタが使用されていた](../Page/バイポーラトランジスタ.md "wikilink")。

## 参考文献

<references />

## 外部リンク

  -
  - [IBMのSolid Logic Technology（SLT）1964-1968](http://www.chipsetc.com/the-ibm-slt---solid-logic-technology.html) , Vintage Computer Chipsには、自動製造プロセスのビデオが含まれてる。

[Category:IBMのメインフレーム](https://ja.wikipedia.org/wiki/Category:IBMのメインフレーム "wikilink")

1.
2.
3.
4.  [Logic Blocks Automated Logic Diagrams SLT, SLD, ASLT, MST](http://www.bitsavers.org/pdf/ibm/logic/SY22-2798-2_LogicBlocks_AutomatedLogicDiagrams_SLT,SLD,ASLT,MST_TO_Oct71.pdf) (PDF) 86 pages
5.  [Logic Blocks Automated Logic Diagrams SLT, SLD, ASLT, MST](http://www.bitsavers.org/pdf/ibm/logic/SY22-2798-2_LogicBlocks_AutomatedLogicDiagrams_SLT,SLD,ASLT,MST_TO_Oct71.pdf) (PDF) 86 pages
6.  [Logic Blocks Automated Logic Diagrams SLT, SLD, ASLT, MST](http://www.bitsavers.org/pdf/ibm/logic/SY22-2798-2_LogicBlocks_AutomatedLogicDiagrams_SLT,SLD,ASLT,MST_TO_Oct71.pdf) (PDF) 86 pages
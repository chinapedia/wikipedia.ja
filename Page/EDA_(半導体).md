> この記事は[EDA \(半導体\)](https://ja.wikipedia.org/wiki/EDA_\(半導体\))から翻訳されています。


**EDA**（）、**DA**（）とは、電子機器、半導体など電子系の設計作業を自動化し支援するためのソフトウェア、ハードウェアおよび手法の総称。半導体の設計工程とその製造工程、さらにそれを部品として実装する[プリント基板](../Page/プリント基板.md "wikilink")設計の自動化で使われる用語である。それぞれの製造工程、検査工程での[データ処理](../Page/データ処理.md "wikilink")技術を意味するともいえる。

従来から単体で存在した電子系の[CAD](../Page/CAD.md "wikilink")や[CAE](../Page/CAE.md "wikilink")を包含した用語として使われるようになった。実際のシステムのことをEDAツールといい、開発・販売業者をEDAベンダーという。電子・半導体メーカーなどが内製する場合もある。

## 歴史

### 1960年代

回路シミュレータ[SPICEが](../Page/SPICE_\(ソフトウェア\).md "wikilink")[カリフォルニア大学](../Page/カリフォルニア大学.md "wikilink")バークレーで開発された。当時の[プラットフォームとしては](../Page/プラットフォーム_\(コンピューティング\).md "wikilink")[メインフレーム](../Page/メインフレーム.md "wikilink")が主流であった。その後各所で派生版が生まれ、改良されながら2008年現在も使用されている。

### 1970年代

半導体レイアウト設計用のCADシステムとして、アメリカのカルマー社（Calma）、アプリコン社（Aplilicon）などのシステムが登場した。いずれも[ミニコンをホストコンピュータとした](../Page/ミニコンピュータ.md "wikilink")[ターンキーシステム](https://ja.wikipedia.org/wiki/ターンキーシステム "wikilink")であった。両社ともその後の買収などを経たのち消滅したが、カルマー社の[フォトマスク](../Page/フォトマスク.md "wikilink")のデータ形式であるGDS2（[ストリーム](https://ja.wikipedia.org/wiki/ストリーム "wikilink")）形式は現在に至るまで使用されている。日本では[セイコー電子工業や](../Page/セイコーホールディングス.md "wikilink")[図研](../Page/図研.md "wikilink")のシステムも登場している。

当時のCADは高価なものであったため設計者が直接使用せず専任オペレータがデータ入力、修正するといった使われ方をした。

### 1980年代

[論理回路](https://ja.wikipedia.org/wiki/論理回路 "wikilink")設計用のCAEシステムとして[メンター・グラフィックス](../Page/メンター・グラフィックス.md "wikilink")、デイジー、バリッドなどが登場する。プラットフォームには汎用のエンジニアリングワークステーション（[EWS](https://ja.wikipedia.org/wiki/ワークステーション#エンジニアリングワークステーション "wikilink")）を使用したもの（メンター）と専用のハード・OSを使用していたものがあった（後の2社）が、その後[UNIX](../Page/UNIX.md "wikilink")ベースのEWSとOSが一般的になった。

これらのツールは論理回路入力をするエディターとその動作検証をシミュレータなどを一体としたものである。またこのあたりから設計者一人ひとりが占有して使うという形態が一般的になってくる。

レイアウトCADで作成データと論理設計ツールのデータを比較するツールも登場する（ECAD社、後にCadence社） 回路図をもとにレイアウトデータの自動配置配線を行うツールも出てきた。当初はゲートアレイなどの[セミカスタム半導体を対象したが](../Page/ASIC.md "wikilink")、より汎用性の高いものへと進化していった。この種のツールにおいては多数の図形データを処理する必要があるが、[計算幾何学](../Page/計算幾何学.md "wikilink")の成果も取り入れ性能の向上が図られていった。

複数のベンダーが各種ツールを発表した結果、データの互換がとれない等の問題も生じている。当時2大ベンダーであった[ケイデンス社](../Page/ケイデンス・デザイン・システムズ.md "wikilink")（Cadence）とメンター社（Mentor）がそれぞれフレームワークという枠組みに他社製品を取り込んで統合しようとの動きもあったが成功していない。またデータを交換する共通フォーマットとして[EDIF](../Page/EDIF.md "wikilink")の研究が始まった。

#### ハードウェア記述言語の登場

[カーバー・ミード](../Page/カーバー・ミード.md "wikilink")と[リン・コンウェイ](../Page/リン・コンウェイ.md "wikilink")の著書『超LSIシステム入門』で、プログラミング言語のコンパイルによって回路を生成することが提唱された。これは論理合成として後に実用化される。

1980年代半ばに、回路図ではなくプログラム言語に似た[ハードウェア記述言語](../Page/ハードウェア記述言語.md "wikilink")（HDL）の一つである[Verilog](../Page/Verilog.md "wikilink")とそのシミュレータが登場、回路図に代わって言語記述で設計する手法が始まった。1980年代後半には、そのHDLから論理回路（ネットリスト）を自動生成するシステムが実用化された。この技術は[論理合成](../Page/論理合成.md "wikilink")と呼ばれ、[シノプシス](../Page/シノプシス.md "wikilink")により製品化された。

### 1990年以降

それぞれのツールの性能向上が続くなかで、半導体製造工程の微細化による様々な問題を解決するためのツールが各種登場する。シミュレーションを行わずにタイミングの問題を検証するツール（静的タイミング解析）、複数の回路の等価性を比較するツール（[形式等価判定](../Page/形式等価判定.md "wikilink")）、配線遅延や負荷を考慮しながらクロック配線網を生成するツール（クロックツリー合成）など各種のものが登場している。また実際[ウェハー](../Page/ウェハー.md "wikilink")にパターンを露光する際、光の波長に近づき近接効果が無視できなくなってきたため、あらかじめ補正する光学近接効果補正技術（、OPC）も使われるようになった。

1990年代後半よりHDLより抽象度の高い記述を可能とする言語の開発が始まった。[C](../Page/C言語.md "wikilink")/[C++](../Page/C++.md "wikilink")を元にした[SystemC](../Page/SystemC.md "wikilink")、SpecCや既存のVerilogの拡張である[SystemVerilog](../Page/SystemVerilog.md "wikilink")などである。これらはシステム記述言語などと呼ばれる。

プラットフォームは[サン・マイクロシステムズ](../Page/サン・マイクロシステムズ.md "wikilink")を中心とした各種ワークステーションのシェア向上が続いたが、PCの性能向上により[Linux](../Page/Linux.md "wikilink")を使う動きがでてきた。[Windows NTおよび後継のサポートもされるようになってきた](../Page/Microsoft_Windows_NT.md "wikilink")。2000年以降、ハードウェアとして[PC/AT互換機](https://ja.wikipedia.org/wiki/PC/AT互換機 "wikilink")を、OSとしてWindowsやLinuxを使う動きが加速している。

## 製品種別、守備範囲

実際の設計フローにしたがって各製品の種別と守備範囲を示す。

### デバイス・プロセス設計

  - プロセス工程設計
      -
        実際の半導体プロセス条件の最適化を行う[プロセスシミュレーション](https://ja.wikipedia.org/wiki/プロセスシミュレーション "wikilink")。
  - デバイス設計
      -
        デバイスの構造から特性の計算を行う[デバイスシミュレーション](../Page/デバイスシミュレーション.md "wikilink")。適切なデバイスの構造の条件を決定する。プロセス工程の設計とリンクした設計が可能。近年では、半導体製造を専門に請け負う[ファウンドリ](../Page/ファウンドリ.md "wikilink")の登場により、デバイス・プロセス設計、モデルパラメータ抽出が不要となる場合が多い。
  - モデルパラメータ抽出
      -
        測定結果やデバイスシミュレーションの結果から[回路設計](https://ja.wikipedia.org/wiki/回路設計 "wikilink")において必要なモデルパラメータを決定する。各種のモデル抽出用のCADツールを使用する。

### システム、回路設計

  - システム、アーキテクチャ設計
      -
        全体のシステムの要求より、構成するブロックと各ブロックの要求性能を決定する。この際に行われるシミュレーションを[システムシミュレーション](https://ja.wikipedia.org/wiki/システムシミュレーション "wikilink")という。
  - 個別ブロック設計
      -
        各ブロックは[シミュレーション](../Page/シミュレーション.md "wikilink")を利用して、個別に要求性能を満たす設計を行う。デジタル回路のブロックは[Verilog](../Page/Verilog.md "wikilink")・[VHDL](../Page/VHDL.md "wikilink")等を用いた論理記述で、アナログ回路はSPICEネットリスト等を利用した記述で回路図へ変換を行う。必要に応じて[IPを利用する](../Page/IPコア.md "wikilink")。
    <!-- end list -->
      - [IP](../Page/IPコア.md "wikilink")（）
          -
            知的財産権をもった既製品の回路ブロックのこと。
      - [シミュレーション](../Page/シミュレーション.md "wikilink")
          -
            [回路シミュレーション](https://ja.wikipedia.org/wiki/回路シミュレーション "wikilink")・[論理シミュレーション](https://ja.wikipedia.org/wiki/論理シミュレーション "wikilink")・アナログデジタル混載シミュレーション（）・故障シミュレーション・プロセスシミュレーション・デバイスシミュレーション・システムシミュレーション等がある。
  - DFT （） / DFM （）
      -
        DFTは製造時の製品の欠陥を検出する仕組みを、あらかじめチップの回路に作りこんでおく手法で、[バウンダリスキャン](https://ja.wikipedia.org/wiki/w:en:Boundary_scan "wikilink")、 （）、ATPG（）などの欠陥検出回路を追加する。DFMは欠陥があることを前提として歩留まりを向上させる仕組みを、あらかじめ作りこんでおく手法。

### マスク設計、検証作業

  - 配置配線、マスク作成
      -
        デジタル系の場合、回路ブロックの配置決定と自動配線を行う。アナログ系回路の場合、高周波になるほど完全な自動配置配線は困難であるため、手作業でのマスク作成が生じる。
  - 物理検証
      -
        設計が回路図と一致するか、あるいは物理的な設計基準を満たしているかの検証。前者は[LVS](../Page/Layout_versus_schematic.md "wikilink")、後者を[DRCという](../Page/デザインルールチェック.md "wikilink")。
  - 寄生素子抽出、再シミュレーション
      -
        作成したマスクにおける寄生素子（容量、抵抗、インダクタ等）の抽出を行いその情報を元の回路に付加し、再度回路、論理シミュレーションを行い、正常に動作し目的の性能を満たすか確認する。この[寄生素子](https://ja.wikipedia.org/wiki/寄生素子 "wikilink")抽出と付加作業をバックアノテーションと呼ぶ。
  - マスクデータ生成
      -
        設計データから実際に半導体チップを製造するための[フォトマスク](../Page/フォトマスク.md "wikilink")用データに変換する。近年の微細化プロセスでは、この時点で光の干渉による影響のシミュレーションを行い、マスクデータの補正を行う。

### 基板設計、評価

  - 評価用基板設計
      -
        プリント基板設計CADを用いて、基板の設計を行い、自動配置配線で配線を引く。周波数が高い場合は、専用のシミュレーションで配線間の干渉などを確認する。
  - テスト
      -
        半導体チップ製造後の不良品検出のために実際に動作させる。その時に使用するテストデータは前述の故障シミュレーションで作成したものである。

なお、仕様から[回路設計](https://ja.wikipedia.org/wiki/回路設計 "wikilink")、シミュレーションを行いマスクを作成するまでの工程をフロントエンド、それ以降をバックエンドと呼ぶ場合もある。

## ベンダー

2012年現在、EDAベンダーは図研・シノプシス・ケイデンス・メンターが4強と呼ばれ、4社の[寡占](../Page/寡占.md "wikilink")状態にある。新しいツールをベンチャー企業が次々開発する状況は続いているが、経営不振や出口戦略のため、大手4社のいずれかに買収されてしまう場合も多い。

  - [図研](../Page/図研.md "wikilink") - 2015年、[ワイ・ディ・シー](https://ja.wikipedia.org/wiki/ワイ・ディ・シー "wikilink")のEDA「CADVANCE」を取得\[1\]。

<!-- end list -->

  - [シノプシス](../Page/シノプシス.md "wikilink")　（売上高：1535.6百万米ドル） - 2011年、Extreme DA及びを買収し、2012年、SpringSoftを買収し、2015年、Atrentaを買収した。
  - [ケイデンス・デザイン・システムズ](../Page/ケイデンス・デザイン・システムズ.md "wikilink")　（売上高：1149.8百万米ドル） - 2010年、Denali Softwareを買収し、2011年、Azuroを買収した。
  - [メンター・グラフィックス](../Page/メンター・グラフィックス.md "wikilink")　（売上高：1014.6百万米ドル）- 2013年、Oasys Design SystemsのEDA「RealTime」を買収し、2015年、Tanner EDAを買収した。2017年、[シーメンス](../Page/シーメンス.md "wikilink")により買収された。同年、訴訟により破産したATopTechの資産を買収した\[2\]ほか、親会社のシーメンスがSolido Design Automationを買収した。2018年、シーメンスがAustemper Design Systemsの買収を発表した。

売上はFY2011

  - [ANSYS](https://ja.wikipedia.org/wiki/ANSYS "wikilink") - 2011年、Apache Designを買収。

  - Real Intent

  - Incentia Design Systems

  - [キーサイト・テクノロジー](https://ja.wikipedia.org/wiki/キーサイト・テクノロジー "wikilink")

  - [シルバコ](../Page/シルバコ.md "wikilink") - 2018年、NanGateを買収。

  - [ジーダット](https://ja.wikipedia.org/wiki/ジーダット "wikilink")

  - (旧Protel) - 1998年、Accolade Design Automationを買収し、2017年、を買収した。

### ソフト

  - CR-5000

  -
  -
  -
  -
  -
  - SX-Meister

  -
#### FPGA関連

  - [Xilinx](https://ja.wikipedia.org/wiki/Xilinx "wikilink")

      - (の後継)

  - [インテル](https://ja.wikipedia.org/wiki/インテル "wikilink") - 2015年、[アルテラ](../Page/アルテラ.md "wikilink")を買収。

      - (旧Altera Quartus)

  - [ラティスセミコンダクター](https://ja.wikipedia.org/wiki/ラティスセミコンダクター "wikilink")

      - Lattice Diamond
      - iCEcube2

  - \- 2010年、を買収した。2018年、[マイクロチップ・テクノロジー](https://ja.wikipedia.org/wiki/マイクロチップ・テクノロジー "wikilink")に買収された。

      - Libero SoC (Libero IDEの後継)

#### オープンソース

  -
  - [KiCad](https://ja.wikipedia.org/wiki/KiCad "wikilink")

### 催し

EDAツールの新製品の発表の場として年1回 （通称[DAC](https://ja.wikipedia.org/wiki/DAC "wikilink")、ダック）という会議、展示会がアメリカで開かれる。この名称は、前述のようにDAという言葉の名残である。

日本での同種の催しとして新製品の展示会  が毎年開催されている。また、DACのアジア版となる国際会議 ASP-DAC も毎年開催され、近年は日本での開催が隔年となっている。

## 関連項目

  - [TCAD](../Page/TCAD.md "wikilink")
  - [集積回路設計](../Page/集積回路設計.md "wikilink")
  - [形式等価判定](../Page/形式等価判定.md "wikilink")
  - [Sequence-pair](https://ja.wikipedia.org/wiki/Sequence-pair "wikilink")

## 脚注

## 外部リンク

  - [EDA コンソーシアム（英語）](http://www.edac.org/)
  - [EDA 産業ワーキンググループ（英語）](http://www.eda.org)
  - [Design Automation Conference](http://www.dac.com/)
  - [Electronic Design and Solution Fair](http://www.edsfair.com/)
  - [ASP-DAC](http://www.aspdac.com/)

[Category:コンピュータの利用](https://ja.wikipedia.org/wiki/Category:コンピュータの利用 "wikilink") [Category:電子工学](https://ja.wikipedia.org/wiki/Category:電子工学 "wikilink") [Category:EDAソフト](https://ja.wikipedia.org/wiki/Category:EDAソフト "wikilink") [Category:回路設計](https://ja.wikipedia.org/wiki/Category:回路設計 "wikilink")

1.  [ボード設計用EDAの「CADVANCE」、図研がYDCから取得](http://techon.nikkeibp.co.jp/article/NEWS/20150601/421052/) 日経BP 2015年6月1日
2.  [Company Overview of ATopTech, Inc.](https://www.bloomberg.com/research/stocks/private/snapshot.asp?privcapId=28677093) Bloomberg
> この記事は[ECU-TEST](https://ja.wikipedia.org/wiki/ECU-TEST)から翻訳されています。


**ECU-TEST**は、 [ドイツ](https://ja.wikipedia.org/wiki/ドイツ "wikilink")の [ドレスデン](../Page/ドレスデン.md "wikilink")に設立されたTraceTronic GmbHが開発した[組み込みシステム](../Page/組み込みシステム.md "wikilink")の [テストおよび検証用のソフトウェアツールです](../Page/ソフトウェアテスト.md "wikilink") 。 2003年のECU-TESTの最初のリリース以来、\[1\] このソフトウェアは自動車用[ECU](../Page/エンジンコントロールユニット.md "wikilink")\[2\]\[3\]\[4\]の 開発で標準ツールとして使用され、 [重機](../Page/建設機械.md "wikilink") \[5\]\[6\]および[工場自動化](../Page/ファクトリーオートメーション.md "wikilink")\[7\]開発でますます使用されています。 ソフトウェアの開発は、コントロールユニットの体系的なテストに関する研究プロジェクト内で開始され、 [TU DresdenからのTraceTronic](https://ja.wikipedia.org/wiki/ドレスデン工科大学 "wikilink") GmbHのスピンオフの基礎を築きました。 ECU-TESTは、 テストケースの仕様、実装、文書化、実行、評価を目的としています。 さまざまな[テスト自動化](https://ja.wikipedia.org/wiki/テスト自動化 "wikilink")方法により、ツールはテストケースの作成、実行、評価に必要なすべてのアクティビティの効率的な実装を保証します。\[8\]

## 機能性

### 方法論

ECU-TESTは、テスト環境全体の制御を自動化し、幅広いテストツールをサポートします。 測定量のさまざまな抽象化レイヤーにより、MILのコンテキスト、SIL、HIL 、実際のシステム（ループ内の車両とドライバー）など、さまざまな[テストレベルでのアプリケーションが可能になります](../Page/ソフトウェアテスト.md "wikilink")。 ECU-TESTを使用したテストケースの作成はグラフィカルに行われ、プログラミングスキルは必要ありません。 テストケースの説明には一般的な形式があり、広範なパラメーター化と構成オプションにより、すべてのテストツールに均一にアクセスできるため、複数の開発フェーズで既存のテストを簡単に再利用できます。

### 構造

ECU-TESTは4つの部分で構成されています。

  - エディターおよびプロジェクトマネージャー
  - コンフィギュレーター
  - テストエンジン
  - アナライザーとプロトコルジェネレーター

テストケースを作成するには、エディターを使用して1つ以上のテストステップのシーケンスとそのパラメーター化を指定します。 テストステップには、テストオブジェクトの測定量の読み取りと評価、テスト環境の操作、診断機能と制御構造の実行が含まれます。 プロジェクトマネージャーを使用して、複数のテストケースを整理できます。 コンフィギュレーターを使用して、テストオブジェクトとテスト環境の追加設定を行うことができます。 テストケースの実行は、マルチステージテストエンジンを使用して実行されます。 生成された[ログデータは](../Page/伐採.md "wikilink")、テストレポート作成の基礎として機能します。 テストの実行に続いて、記録された測定量のオプションのチェックがアナライザーで実行されます。 テスト実行とその後のチェックの結果から、プロトコルジェネレーターは詳細なテストレポートを作成します。このレポートは対話形式で表示され、ファイルやデータベースにアーカイブできます。

## インターフェース

ECU-TESTは、既存のテストおよび検証プロセスでの拡張および統合のための明確なインターフェースを提供しました。 大量のテストハードウェアとソフトウェアがデフォルトでサポートされています。 ユーザー定義のテストステップ、 [プラグイン](../Page/プラグイン.md "wikilink") 、 [Python](../Page/Python.md "wikilink")スクリプトを使用して、追加のツールを簡単に統合できます。 特定の[client-server-architectureを通して](../Page/クライアントサーバモデル.md "wikilink")、分散テスト環境の複数のテストベンチコンピューターのソフトウェアツールに対処できます。 [COMインターフェイスを使用して](../Page/Component_Object_Model.md "wikilink")、 [要件管理](../Page/要求管理.md "wikilink") 、 改訂管理 、 [モデルベースのテストなどのツールを統合できます](../Page/モデルベーステスト.md "wikilink")。 ECU-TESTは、次のハードウェアおよびソフトウェアツールをサポートし、次の標準に基づいています：\[9\]

### サポートされているハードウェアとソフト



  - [dSPACE](https://ja.wikipedia.org/wiki/:en:DSPACE_GmbH "wikilink") ControlDesk, ControlDesk Next Generation, ControlDesk Failure Simulation, Real-Time Interface CAN Multi-Message Blockset, SCALEXIO
  - dSPACE VEOS® (offline-simulation platform by dSPACE)
  - D2T MORPHEE
  - EA UTA12
  - ETAS [INCA](https://ja.wikipedia.org/wiki/:en:INCA_\(Software\) "wikilink") and LabCar Operator
  - [Ethernet](https://ja.wikipedia.org/wiki/:en:Ethernet "wikilink") (SOME/IP-SD in-vehicle Ethernet communication)
  - Hard\&Soft fault simulation
  - ITI [SimulationX](https://ja.wikipedia.org/wiki/:en:SimulationX "wikilink")
  - IXXAT FlexRay CCM
  - MathWorks [MATLAB](https://ja.wikipedia.org/wiki/:en:MATLAB "wikilink") and [Simulink](https://ja.wikipedia.org/wiki/:en:Simulink "wikilink")
  - MicroNova NovaSim
  - National Instruments [LabVIEW](https://ja.wikipedia.org/wiki/:en:LabVIEW "wikilink") and VeriStand
  - OPAL-RT RT-LAB
  - PEAK CAN-Interfaces
  - pls UDE
  - QTronic Silver
  - QUANCOM relay, optocoupler, A/D and D/A transformer cards
  - RA Consulting DiagRA
  - Softing Diagnostic Tool Set and EDIABAS
  - TTTech TTX Connexion
  - Vector CAN interfaces, [CANape](https://ja.wikipedia.org/wiki/:en:CANape "wikilink"), [CANoe](https://ja.wikipedia.org/wiki/:en:CANoe "wikilink") and [CANalyzer](https://ja.wikipedia.org/wiki/:en:CANalyzer "wikilink")
  - X2E Xoraya Data Logger

### サポートされている標準

  - [CAN](https://ja.wikipedia.org/wiki/Controller_Area_Network "wikilink")
  - Field Bus Exchange Format (FIBEX)
  - [FlexRay](https://ja.wikipedia.org/wiki/FlexRay "wikilink")
  - HiL-API
  - LIN
  - MCD 2（A2L）およびMCD 3

## 参照資料

## 外部リンク

  - [TraceTronic WebサイトのECU-TEST製品ページ](https://web.archive.org/web/20140531082529/http://www.tracetronic.com/products/ecu-test.html) 。 2015年1月12日検索。
  - [TraceTronic GmbH](http://www.tracetronic.de/) 。 2015年1月12日検索。
  - [株式会社GAFS](http://www.gafs.co.jp) 。　2020年1月06日検索。

[Category:制御工学](https://ja.wikipedia.org/wiki/Category:制御工学 "wikilink") [Category:自動車電子技術](https://ja.wikipedia.org/wiki/Category:自動車電子技術 "wikilink")

1.  H.-C. Reuss, R. Deutschmann, J. Liebl, F. Munk, C. Schmidt: Automatic ECU Test with HiL-Simulation. 5th Stuttgart International Symposium on Automotive and Engine Technology“. Expert, 2003.
2.  Rocco Deutschmann, Frank Günther, Matthias Roch, Hans-Christian Reuss, Frank Kessler, Wolfram Bohne, Carsten Krug: New strategies and solutions for automated test of embedded software. 6th Stuttgart International Symposium on Automotive and Engine Technology. Expert, 2005.
3.  Wolfgang Schlüter, Franz Dengler: HiL-Testsysteme für den BMW Hydrogen 7. 7th Conference on „Hardware-in-the-Loop-Simulation“. Haus der Technik, 2007.
4.  Daniel Brückner, Michael Kahle: OTX als Test- und Applikationssprache in der On-Board-Diagnose. 6th Conference on „Diagnose in mechatronischen Fahrzeugsystemen“. Expert, 2012.
5.  Thomas Neubert, Rocco Deutschmann: Automated software test using HiL technology. 13th ITI Symposium, 2010.
6.  Thomas Borchert, Rocco Deutschmann, René Müller, Andreas Abel, Torsten Blochwitz: Simulation and Testing of Off-Road Vehicles in Virtual Reality - Development of a Validation Framework for Multi-Purpose Vehicles. 13th ITI Symposium, 2010.
7.  Klaus Kabitzsch, André Gellrich, Jens Naake: Automatisierte Steuerungstests vereinfachen die virtuelle Inbetriebnahme in der Fabrikautomation. atp edition, 2012.
8.  Rocco Deutschmann: Semi-formal methods for the automated test of embedded systems. Doctoral thesis, TU Dresden, 2007.
9.  ECU-TEST data sheet  (PDF; 372 kB). Retrieved 12 January 2015.
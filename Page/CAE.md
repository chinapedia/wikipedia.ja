> この記事は[CAE](https://ja.wikipedia.org/wiki/CAE)から翻訳されています。


**CAE**（）は、[コンピュータ](../Page/コンピュータ.md "wikilink")によって支援された、[製品](../Page/製品.md "wikilink")の[設計](../Page/設計.md "wikilink")・[製造](https://ja.wikipedia.org/wiki/製造 "wikilink")や[工程](https://ja.wikipedia.org/wiki/工程 "wikilink")設計の事前検討などといったエンジニアリングの作業、あるいはそのツール等を指す場合もある。要素技術としては、[シミュレーション](../Page/シミュレーション.md "wikilink")（[コンピュータシミュレーション](https://ja.wikipedia.org/wiki/コンピュータシミュレーション "wikilink")）[数値解析](https://ja.wikipedia.org/wiki/数値解析 "wikilink")、などがある。

## 概要

製品の設計時の検討は、コンピュータが発達する以前は、工学便覧に載っているような簡易計算でおこなっており、実物ができるまでその設計の細かな良し悪しがわからなかった。そのため、[量産品を作る前に](../Page/大量生産.md "wikilink")[試作品を作り](../Page/プロトタイプ.md "wikilink")、その際に製造方法の妥当性を検証したり、また耐久試験などを行って製品の性能が十分かを検証していた。このような方法では、[コスト](https://ja.wikipedia.org/wiki/コスト "wikilink")も[リードタイム](https://ja.wikipedia.org/wiki/リードタイム "wikilink")も多く必要とし、また試作できる回数も限られることから最適な設計の追求も十分ではなかった。

コンピュータ技術の進歩により、以下のようなニーズが高まっていった。

  - 設計の[CAD](../Page/CAD.md "wikilink")化によって容易に作れるようになった製品データの、コンピュータ計算への再利用。
  - [CAM](../Page/CAM.md "wikilink")の普及により複雑な形状加工が実現したが、従来の机上計算では予測困難な製品形状の性能予測の実施。
  - 製品に対する要求性能が高まり、最適な設計条件を求めることが必要となる。
  - 投資、リードタイム圧縮のために試作を廃止したり、回数を減らす必要が高まる。

上記ニーズを満たすツールとして、各種CAEツールが登場し、設計における事前検討行為の一つとして普及していった。また、微細加工などの分野では、実験での科学的なデータ収集が困難なものも多く、実験の事前検討としての使用ではなく、現象の理論的な考察に使用される事も多い。

## CAE作業の流れ

CAEの作業のフローは、以下の順番で行う。

1.  解析する現象を予測し、[解析](../Page/解析.md "wikilink")内容を決定する
2.  解析条件の整理
3.  必要なデータの収集、CADで作成
4.  [プリプロセッサ](../Page/プリプロセッサ.md "wikilink")にて、解析用データを作成（[計算格子](https://ja.wikipedia.org/wiki/計算格子 "wikilink")の生成など）
5.  [ソルバー](https://ja.wikipedia.org/wiki/ソルバー "wikilink")を実行して、[シミュレーション](../Page/シミュレーション.md "wikilink")を行う
6.  [ポストプロセッサ](https://ja.wikipedia.org/wiki/ポストプロセッサ "wikilink")にて結果を分析

その結果を分析して実物を作る前に設計の妥当性、性能試験、最適形状や最適条件を検討して、製品の問題点の洗い出しを行う。必要に応じてこのフローを何回か回し、目標性能を達成させて製品設計を推進する。最後に試作品にてCAE結果の妥当性を確認して、量産品製造に着手する。業界によっては量産前の試作品を全く作らずに、CAE結果をもって量産品着手を行うことも多い。

## 解析手法

以下の3つが代表的である。

  - [有限要素法](../Page/有限要素法.md "wikilink")
  - [有限差分法](https://ja.wikipedia.org/wiki/有限差分法 "wikilink")
  - [境界要素法](../Page/境界要素法.md "wikilink")

## 主な適用分野

CAEの適用分野は[機械工学](../Page/機械工学.md "wikilink")、[電気工学](../Page/電気工学.md "wikilink")、[電子工学](../Page/電子工学.md "wikilink")、[建築工学](https://ja.wikipedia.org/wiki/建築工学 "wikilink")、[土木工学](../Page/土木工学.md "wikilink")、[化学工学](../Page/化学工学.md "wikilink")など多岐に渡る。

## 主なメーカー

  - [TOYOTA SYSTEMS](https://ja.wikipedia.org/wiki/トヨタシステムズ "wikilink") - TopCAST（鋳造シミュレーションソフトウェア）\[1\]を開発・販売している。

  - \- 2015年、溶接解析および積層造形のSimufact社を買収し\[2\]、2016年、流体解析のSoftware Cradle社を買収した\[3\]。2017年、[ヘキサゴン社に買収された](https://ja.wikipedia.org/wiki/ヘキサゴン_\(スウェーデンの企業\) "wikilink")。ヘキサゴンは2020年、電気機械解析のRomax Technology社を買収した。

  - [Dassault Systèmes](https://ja.wikipedia.org/wiki/ダッソー・システムズ "wikilink") - 2005年、社 (後のDassault Systèmes Simulia社) を買収し\[4\]、2006年、1D-CAEのDynasim社を買収し、2011年、複合材解析のSimulayt社を買収し、2013年、疲労寿命予測解析のSafe Technology社を買収し、同年、SFE社を買収し、2016年、CST社を買収し、同年、流体解析のNext Limit Dynamics (子会社) を買収し\[5\]、2017年、Exa Corporationを買収し、2018年、Opera Simulation Softwareを買収した。

  - [ANSYS](https://ja.wikipedia.org/wiki/ANSYS "wikilink") - 2003年、流体解析のCFX社を買収し、2006年、流体解析のFluent社を買収し、2008年、電磁界解析のAnsoft社を買収し、2017年、積層造形の3DSIM社を買収し、2018年、光学解析の[OPTIS社を買収し](https://ja.wikipedia.org/wiki/Optis "wikilink")、2019年、自動設計信頼性解析のDfR Solutions社および[マルチフィジックス](https://ja.wikipedia.org/wiki/マルチフィジックス "wikilink")のLivermore Software Technology Corporation (LSTC) 社を買収し、2020年、光量子解析のLumericalを買収した。

  - [Autodesk](https://ja.wikipedia.org/wiki/Autodesk "wikilink") - 2008年、射出成形の社を買収し、2009年、構造解析および流体解析のを買収した。

  - [シーメンス](../Page/シーメンス.md "wikilink") - 2007年、UGS社 (現) を買収し、2011年、複合材解析の社を買収し、2012年、LMS Internationalを買収し、2016年、CD-adapco社を買収し、2017年、[Mentor Graphics社を買収し](../Page/メンター・グラフィックス.md "wikilink")、同年、電磁界解析のInfolytica社を買収し、2019年、複合材解析のを買収した。

  - [Altair Engineering](https://ja.wikipedia.org/wiki/アルテアエンジニアリング "wikilink") - 2006年、構造解析のMECALOG社を買収し、同年、電波伝搬解析のAWE Communications社を買収し、2010年、FEM解析のSimLab社を買収し、2011年、流体解析のACUSIM Software社を買収し、2014年、電磁気解析のEM Software & Systems社を買収し、2017年、複合材解析のComponeering社を買収し、2018年、GPU流体解析のFluiDyna社および構造解析のSIMSOLID社を買収し、2019年、Cambridge Collaborative社の騒音・振動解析ソフトウェアSEAMを買収し、同年、粉体解析のDEM Solutions社を買収し、2020年、電磁気解析のnewFASANT社を買収し、同年、発泡成形解析のS\&WISE社を買収した。

  - \- 2011年、電磁界解析のEfield社を買収し、2013年、1D-CAE「CyModelica」開発元であるCyDesign Labsを買収し、2015年、AMOEBA社より流体解析のPRESTOを買収し、同年、流体解析のCiespace社の資産を買収し\[6\]、2016年、1D-CAEのITI社を買収し、2017年、オープンソースソフトウェア「[Scilab](../Page/Scilab.md "wikilink")」(1D-CAEモジュールのXcosを含む) の開発元Scilab Enterprisesを買収した。

  - \- 2018年、流体解析のFlowkit社を買収した。

  - \- 1986年、KTHの大学院生3名で創業、1996年、MATLABの物理シミュレーションアドオンPDE Toolbox発売、1998年、FEMLAB発売、2005年、製品名をCOMSOL Multiphysicsに変更した。

  - AMPS Technologies

  - 株式会社アライドエンジニアリング - 1981年創業。構造解析ソフトウェア「ADVENTURECluster」を開発する。[SCSK](../Page/SCSK.md "wikilink")の子会社。

  - 株式会社計算力学研究センター

  - 株式会社くいんと - 1985年創業。構造最適設計ソフトウェア「OPTISHAPE」等を開発する。

  - 株式会社先端力学シミュレーション研究所 - 1999年創業の[理研ベンチャー](https://ja.wikipedia.org/wiki/理研ベンチャー "wikilink")。創業者は[牧野内昭武](https://ja.wikipedia.org/wiki/牧野内昭武 "wikilink")。

  - アドバンスソフト株式会社

  - 株式会社科学技術研究所

  - ムラタソフトウェア株式会社 - 設計者向けCAEソフトウェア「Femtet」を開発する。[村田製作所](../Page/村田製作所.md "wikilink")の子会社。

  - ファンクションベイ株式会社

  - [プロメテック・ソフトウェア](https://ja.wikipedia.org/wiki/プロメテック・ソフトウェア "wikilink")株式会社 - 2004年創業の東大発ベンチャー。粒子法流体解析ソフトウエア「Particleworks」や粉体解析ソフトウェア「Granuleworks」を開発する。

  - [株式会社JSOL](../Page/JSOL.md "wikilink") - 電磁界解析ソフトウェア「[JMAG](https://ja.wikipedia.org/wiki/JMAG "wikilink")」を開発する。

## 主な解析の種類

（括弧内はCAEソフト）

  - 構造解析（[Advance/FrontSTR](https://ja.wikipedia.org/wiki/Advance/FrontSTR "wikilink")、[MSC Nastran](https://ja.wikipedia.org/wiki/Nastran "wikilink")、ANSYS、SIMULIA [Abaqus](https://ja.wikipedia.org/wiki/Abaqus "wikilink") 、ANSYS Discovery Live、AMPS Designer 、MPACT 、[CATIA Analysis](../Page/CATIA.md "wikilink")、MSC [SimDesigner](https://ja.wikipedia.org/wiki/SimDesigner "wikilink")、MSC Apex Structures、[シーメンスNX](../Page/UGS_NX.md "wikilink") 、LMS Virtual.Lab Structures 、[ADVENTURECluster](https://ja.wikipedia.org/wiki/ADVENTURECluster "wikilink")、[Femtet](https://ja.wikipedia.org/wiki/Femtet "wikilink") 、Altair [RADIOSS](https://ja.wikipedia.org/wiki/RADIOSS "wikilink")、Altair [Opti Struct](https://ja.wikipedia.org/wiki/Opti_Struct "wikilink")、Altair SimSolid 、Altair SimLab 、Autodesk Fusion 360、PTC Creo Simulate (旧Pro/Mechanica) 、 、）

　※NX、Fusion 360など、最近の3D CADシステムには線形領域での構造解析機能を持ったものも多く、設計者自らが思考の過程でCAE結果を参考にすることが可能となっている．

  - 応力解析（[Advance/FrontSTR](https://ja.wikipedia.org/wiki/Advance/FrontSTR "wikilink")、MSC SimDesigner、ANSYS、[CATIA Analysis](../Page/CATIA.md "wikilink")、AMPS Designer 、SIMULIA [Abaqus](https://ja.wikipedia.org/wiki/Abaqus "wikilink") 、Femtet、Altair [OptiStruct](https://ja.wikipedia.org/wiki/OptiStruct "wikilink")、Autodesk Fusion 360、）
  - 振動解析（SIMULIA [Abaqus](https://ja.wikipedia.org/wiki/Abaqus "wikilink") 、Altair Seam 、ANSYS、MSC Nastran、LMS Virtual.Lab Noise and Vibration 、[CATIA Analysis](../Page/CATIA.md "wikilink")、[シーメンスNX](../Page/UGS_NX.md "wikilink") 、PERMAS、Altair [OptiStruct](https://ja.wikipedia.org/wiki/OptiStruct "wikilink")、）
  - 超音波解析([ComWAVE](http://www.engineering-eye.com/ComWAVE/index.html)、)
  - 音響解析（[Advance/FrontNoise](https://ja.wikipedia.org/wiki/Advance/FrontNoise "wikilink")、WAON、LMS Virtual.Lab Acoustics 、LMS SYSNOISE Auto-SEA 、ANSYS、Femtet、FINE/Acoustics 、、Altair [OptiStruct](https://ja.wikipedia.org/wiki/OptiStruct "wikilink")）
  - 衝撃解析（Pam-Crash、ANSYS [LS-DYNA](https://ja.wikipedia.org/wiki/LS-DYNA "wikilink") 、SIMULIA [Abaqus](https://ja.wikipedia.org/wiki/Abaqus "wikilink") 、Altair [RADIOSS](https://ja.wikipedia.org/wiki/RADIOSS "wikilink") 、AMPS Designer 、 ）
  - [流体解析](https://ja.wikipedia.org/wiki/流体解析 "wikilink")（[OpenFOAM](https://ja.wikipedia.org/wiki/OpenFOAM "wikilink")、[Advance/FrontFlow/red](https://ja.wikipedia.org/wiki/Advance/FrontFlow/red "wikilink")、[FrontFlow/Blue](https://ja.wikipedia.org/wiki/FrontFlow/Blue "wikilink")、[STAR-CD](https://ja.wikipedia.org/wiki/STAR-CD "wikilink") 、[FLOW-3D](https://ja.wikipedia.org/wiki/FLOW-3D "wikilink") 、[ANSYS Fluent](https://ja.wikipedia.org/wiki/ANSYS_Fluent "wikilink")、ANSYS CFX 、ANSYS Discovery AIM (旧ANSYS AIM)、ANSYS Discovery Live、[STREAM](https://ja.wikipedia.org/wiki/STREAM "wikilink") 、[SCRYU/Tetra](https://ja.wikipedia.org/wiki/SCRYU/Tetra "wikilink") 、[PHOENICS](https://ja.wikipedia.org/wiki/PHOENICS "wikilink") 、[Pam-Flow](https://ja.wikipedia.org/wiki/Pam-Flow "wikilink") 、 、 、ESI-PRESTO 、[DYNAFLOW](https://ja.wikipedia.org/wiki/DYNAFLOW "wikilink") 、[シーメンスNX](../Page/UGS_NX.md "wikilink")、[PowerFlow](https://ja.wikipedia.org/wiki/PowerFlow "wikilink") 、[e-flow](https://ja.wikipedia.org/wiki/e-flow "wikilink")、[Particleworks](https://ja.wikipedia.org/wiki/Particleworks "wikilink")、[MPS-RYUJIN](https://ja.wikipedia.org/wiki/MPS-RYUJIN "wikilink")、Altair [AcuSolve](https://ja.wikipedia.org/wiki/AcuSolve "wikilink") 、Altair ultraFluidX 、Altair nanoFluidX 、Altair SimLab 、KeyFlow 、SIMULIA XFlow 、SOLIDWORKS Flow Simulation 、Autodesk CFD 、FloEFD 、FINE/Turbo 、FINE/Open with OpenLabs 、FINE/Marine 、OMNIS/LB 、FINE/FSI-OOFELIE 、）
  - 粉体解析（Granuleworks、Altair EDEM 、Rocky DEM）
  - 伝熱解析 (ANSYS (Icepak機能)、MSC Sinda、Altair SimLab 、ThermoSYS 、Femtet、)
  - [電磁場解析](https://ja.wikipedia.org/wiki/電磁場解析 "wikilink")（PHOTO-Series 、MagNet 、[JMAG](https://ja.wikipedia.org/wiki/JMAG "wikilink") 、PAM-CEM 、Efield Solution 、ANSYS、ANSYS HFSS 、Femtet、 、Opera 、[Poynting](https://ja.wikipedia.org/wiki/Poynting "wikilink")、、OOFELIE::Multiphysics 、[PetaMagnetic](http://petamagnetic.appspot.com/)、Altair [FEKO](https://ja.wikipedia.org/wiki/FEKO "wikilink") 、newFASANT 、Altair SimLab ）
  - 電磁波解析 (KeyFDTD 、[MAGNA/TDM](http://www.engineering-eye.com/MAGNA_TDM/)、Altair [FEKO](https://ja.wikipedia.org/wiki/FEKO "wikilink") 、Femtet、)
  - 光学解析 ([Zemax OpticStudio](https://ja.wikipedia.org/wiki/Zemax_OpticStudio "wikilink") 、[LensMechanix](https://ja.wikipedia.org/wiki/Zemax_LensMechanix "wikilink")、SPEOS 、CODE V 、LightTools 、Lumicept (旧INSPIRER) 、TracePro 、ASAP 、 、)
  - 光量子解析 (DEVICE Suite )
  - 機構解析（MSC Adams、LMS Virtual.Lab Motion (旧LMS DADS\[7\])、FunctionBay RecurDyn、[シーメンスNX](../Page/UGS_NX.md "wikilink") 、Altair [MotionSolve](https://ja.wikipedia.org/wiki/MotionSolve "wikilink")、）
  - 圧電解析（ANSYS、Femtet、、OOFELIE::Multiphysics 、）
  - 半導体解析、バイポーラトランジスタ、FET、IGBT、GaN（）
  - MEMS/NEMS/マイクロフルイディクス/MicroTAS解析（）
  - 化学反応解析（）
  - 電気化学解析（）
  - プラズマ解析、CVD（）
  - Li-ion電池・[全固体電池](https://ja.wikipedia.org/wiki/全固体電池 "wikilink")・燃料電池解析（）
  - 腐食・めっき解析（、[PetaMagnetic](http://petamagnetic.appspot.com/)）
  - 溶接解析 (Simufact Welding 、Virfac Welding Designer 、ESI SYSWELD 、Visual Assembly )
  - 複合材解析 (FiberSIM 、Altair ESAComp 、CATIA Composites Fiber Modeler 、SOLIDWORKS Simulation Premium、MSC Apex\[8\]、MultiMechanics 、ESI PAM-COMPOSITES、)
  - [騒音・振動・ハーシュネス](https://ja.wikipedia.org/wiki/騒音・振動・ハーシュネス "wikilink") (NVH) 解析 (Altair NVH Director、SFE AKUSMOD 、Romax Spectrum )
  - 1次元解析 ([Simulink](../Page/Simulink.md "wikilink") 、 、 、 、CyModelica 、 、[Wolfram SystemModeler](https://ja.wikipedia.org/wiki/Wolfram_SystemModeler "wikilink") 、 、[Scilab](../Page/Scilab.md "wikilink") )
  - 着氷解析 (ANSYS FENSAP-ICE)
  - 疲労寿命予測解析 (FEMFAT 、MSC Fatigue、Altair HyperLife、SIMULIA fe-safe 、ANSYS nCode DesignLife、LMS Virtual.Lab Durability )
  - 自動設計信頼性解析 (ANSYS Sherlock )
  - ベアリング解析 (Romax Spin )
  - 発泡成形解析 (3D TIMON - FoamMolding 、Foam Simulator 、Rem3D )

[金型](../Page/金型.md "wikilink")分野への適用も非常に多い

  - [樹脂](https://ja.wikipedia.org/wiki/樹脂 "wikilink")金型・樹脂流動解析（3D TIMON 、Autodesk Moldflow、SIMPOE、Moldex3D）
  - [プレス金型](https://ja.wikipedia.org/wiki/プレス加工 "wikilink")（Pam-Stamp、JSTAMP-Works、AutoForm、DYNAFORM、Altair [RADIOSS](https://ja.wikipedia.org/wiki/RADIOSS "wikilink")、Altair [HyperForm](https://ja.wikipedia.org/wiki/HyperForm "wikilink")）
  - [鋳造](../Page/鋳造.md "wikilink")金型（ADSTEFAN、MAGMASOFT、Procast、ConiferCast、JSCAST、CAPCAST、Pam-Cast、AnyCASTING、[Click2Cast](https://ja.wikipedia.org/wiki/Click2Cast "wikilink")）
  - 砂ブロー造型金型（ArenaFlow）
  - [鍛造](../Page/鍛造.md "wikilink")金型（Simufact Forming (旧MSC.SuperForge） 、DEFORM、FORGE3、Altair [HyperForm](https://ja.wikipedia.org/wiki/HyperForm "wikilink")）

積層造形 (Additive Manufacturing) 向けのものも登場した

  - 積層造形 (Autodesk Netfabb 、Virfac Additive Manufacturing 、Amphyon 、ANSYS Additive Print、ANSYS Additive Suite (3DSIM exaSIM の後継\[9\])、Simufact Additive )

[農業](https://ja.wikipedia.org/wiki/農業 "wikilink")分野への応用も始った

  - [施設園芸](https://ja.wikipedia.org/wiki/施設園芸 "wikilink")園芸施設内熱気流解析（KeyAGri）

[地球物理](https://ja.wikipedia.org/wiki/地球物理 "wikilink")、[土木](https://ja.wikipedia.org/wiki/土木 "wikilink")、[地下水流](https://ja.wikipedia.org/wiki/地下水流 "wikilink")分野への適用もある

  - ジオメカニクス、地下水流解析（）

[バイオテクノロジー](https://ja.wikipedia.org/wiki/バイオテクノロジー "wikilink")、[医用工学](https://ja.wikipedia.org/wiki/医用工学 "wikilink")分野への適用

  - バイオ、メディカル解析（）

[食品](../Page/食品.md "wikilink")分野への適用

  - 熱流体解析、フリーズドライ、マイクロ波加工（）

[無線通信](../Page/無線通信.md "wikilink")分野への適用

  - 電波伝搬解析、無線ネットワークプランニング (Altair WinProp 、Raplab 、Wireless InSite 、iBwave Design 、GRASS-RaPlaT)

## 脚注

## 関連項目

  - [製造に関する記事一覧](../Page/製造に関する記事一覧.md "wikilink")

  - [計算科学](../Page/計算科学.md "wikilink")

  - [シミュレーション](../Page/シミュレーション.md "wikilink")

  - [数値解析](https://ja.wikipedia.org/wiki/数値解析 "wikilink")

  -
  -
[Category:製造](https://ja.wikipedia.org/wiki/Category:製造 "wikilink") [Category:コンピュータの利用](https://ja.wikipedia.org/wiki/Category:コンピュータの利用 "wikilink") [Category:スーパーコンピュータ](https://ja.wikipedia.org/wiki/Category:スーパーコンピュータ "wikilink") [Category:CAD](https://ja.wikipedia.org/wiki/Category:CAD "wikilink") [Category:CAE](https://ja.wikipedia.org/wiki/Category:CAE "wikilink")

1.  [TopCAST（鋳造シミュレーションソフトウェア）](https://www.toyotasystems.com/product/cae/detail/topcast.html) トヨタシステムズ 2019年2月24日
2.  [CAEの専門家ではなくても使いやすい溶接シミュなどを本格展開](http://monoist.atmarkit.co.jp/mn/articles/1503/06/news020.html) ITmedia 2015年3月6日
3.  [米MSC、国産CFDソフトベンダー クレイドルを買収](http://monoist.atmarkit.co.jp/mn/articles/1612/26/news027.html) ITmedia 2016年12月26日
4.  [PLM雌伏の10年、これからは飛躍の10年となるか (1/4)](http://monoist.atmarkit.co.jp/mn/articles/1709/20/news008.html) ITmedia 2017年9月20日
5.  [流体解析ソフトウェア「XFlow」の開発元を買収](http://techfactory.itmedia.co.jp/tf/articles/1701/26/news001.html) ITmedia 2017年01月26日
6.  [Company Overview of Ciespace Corporation](https://www.bloomberg.com/research/stocks/private/snapshot.asp?privcapId=36661684) Bloomberg
7.  『Präzisere Echtzeit-Flugsimulation kleiner Nutzflugzeuge durch Integration feingranularer Teilmodelle』 P.22  Wolfram Meyer-Brügel 2019年9月17日 ISBN 978-3798330580
8.  [複合材解析を分かりやすくするCAE「MSC Apex Harris Hawk」](http://monoist.atmarkit.co.jp/mn/articles/1804/03/news089.html) ITmedia 2018年4月3日
9.  [Frustum and ANSYS: 3D Software Solutions on Display at RAPID + TCT](https://www.3dprint.com/212008/frustum-ansys-at-rapid-2018/) 3DR Holdings 2018年5月1日
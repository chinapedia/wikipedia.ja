> この記事は[CAM](https://ja.wikipedia.org/wiki/CAM)から翻訳されています。


**CAM**（キャム）とは、**コンピュータ支援製造** () の略語。製品の製造を行うために、[CAD](../Page/CAD.md "wikilink")で作成された形状データを入力データとして、加工用の[NCプログラム作成などの生産準備全般を](../Page/NC加工.md "wikilink")[コンピュータ](../Page/コンピュータ.md "wikilink")上で行う為のシステムであり、出力されたデータは、[CNC](https://ja.wikipedia.org/wiki/CNC "wikilink")化された[工作機械](../Page/工作機械.md "wikilink")に送られて実際の加工が行われる。

狭義では、**CAD/CAM**の設計分野CADとの対比で製造分野の事をさすが、製造分野に最適化されている**CAD/CAM**システムや、テキストベースの**自動プログラミング装置**など、NCプログラムを出力するシステムをすべて**CAM**と呼ぶ事もある。

## 歴史

### CAM黎明期

[1956年](../Page/1956年.md "wikilink")[マサチューセッツ工科大学](../Page/マサチューセッツ工科大学.md "wikilink")にて**APT**(アプト)と呼ばれるNCプログラム言語が開発された。日本では[1972年](../Page/1972年.md "wikilink")に純国産のNCプログラム言語が開発された（後に**Lanc**(ランク)と命名）。また、APT言語から派生したFAPT言語やHAPT言語、MINIAPT言語も実用化されている。総称して**自動プログラミング装置**(自動プロ)と呼ばれていた。これらは、言語専用の命令を記述したプログラムを工作機械用のNCデータに変換する、[コンパイラ](../Page/コンパイラ.md "wikilink")として実装されていた。以降のCAMとの最大の違いは言語ベースのために[WYSIWYG](../Page/WYSIWYG.md "wikilink")ではないことである。2008年現在でも、APT言語は、いくつかの海外製CAMのCL(カッターロケーション)ファイルとして使用されている。一方、Lanc言語もCAM同様のインターフェースを纏って使用され続けている。

### CAM運用環境の変遷

CAMの分野では、歴史的に[Unix](https://ja.wikipedia.org/wiki/Unix "wikilink")が多く利用されてきたが、これは比較的重い計算を繰り返す為に、安定したマルチタスク性を持つOSが必要な事が主な理由である。しかし、[Windows](https://ja.wikipedia.org/wiki/Windows "wikilink")系コンピュータのCPU性能が飛躍的に向上したために、計算時間短縮とコスト低下を目的としてWindows系OSへの移行が進み、現在では大部分のCAMシステムがWindows系をプラットホームとしている。また、UnixからWindowsへの移行の流れの中で檜舞台から去っていったCAMシステムも数多くある。

Unixは既にCAMの流れの本流では無くなっているが、持ち前の安定性とマルチタスク性能を望む声も多く、[Linux](../Page/Linux.md "wikilink")への展開も少なからず始まっている。これは、数多くのCAMベンダーがWindows上での動作にデュアルCPUを推奨しているのに対し、同等のシステムがUnix上では、シングルCPUで良好なレスポンスを実現していたこととも無関係ではない。

## 加工形状

加工形状による分類

CADは2Dを使用するタイプと3Dを使用するタイプがある。

### 2D CAM

**平面的なポケット加工や輪郭加工及び穴あけ加工**のための2軸同時移動データを出力する。 加工機側で工具径補正(G41,G42)が可能であり、プログラムの汎用性に優れ、輪郭の直線(G01)と円弧(G02/G03)をそのまま使用するので、精度が高い加工が可能なため、機械部品加工などに多用されている。形状データはCADからの2次元図面データを使用する。NC制御器に内蔵されている対話型は、ほとんどこのタイプである。

NC旋盤、ワイヤーEDM、レーザー加工機、プラズマ加工機などにも使用される。

### 2.5D CAM

**2Dに加えて、平面輪郭に断面を付加した加工及び、側面から見た輪郭形状加工**のための2軸同時移動データを出力する。自由曲面以外のあらゆる形状が加工可能(身近な例: キーボードのキートップ)であり、2D同様に精度が高い加工が可能である反面、作業者のスキルによって形状に差違がでる場合がある。

ワイヤーEDMの上下任意形状加工も、これに分類される。この場合は、断面ではなく上面と下面の双方の輪郭を用いて形状定義をして、4軸以上の同時移動データを出力する。

### 3D CAM

**自由曲面を含む加工**のための2軸同時から3軸以上の同時移動データを出力する。CADで定義可能な形状をすべて扱えるため、デザイン性の高い製品に多用される(身近な例: マウスの筐体)が、工具定義をCAM側で行う為、プログラムは定義した工具専用となり汎用性は低く、また、形状を直線近似で加工する為、精度が低下する場合が多い。 形状データはCADからの3次元データを使用する。 一般に2Dと2.5Dの機能を含んでいるが、3D専用の物もあり、また、自由曲面上での輪郭動作に制限のあるCAMを2.8Dと呼ぶ場合もある。

積層型のラピッドプロトタイピング(RP)に用いられるシステムも、出力は2.5D的ではあるが、このタイプに分類される。

4/5軸割出し加工、4軸同時制御加工、5軸同時制御加工などは3DCAMのオプションとして用意されている。

複合旋盤にも用いられている。

## 内部データ形式

形状の保持方法による分類

### フィーチャ型

形状の幾何情報と意図情報を併せ持ち、加工方法や加工条件の決定に利用する物で、主に穴あけ加工を含む2D加工を中心に、複雑な工程を必要とする部品加工などに用いられている。

多くの場合はソリッドCADのフィーチャ情報を引き継ぐことが多いが、 独自のフィーチャ型形状入力をするタイプもある。

### サーフィス型

3D加工用の形状を曲面として保持している物で、 曲面からの計算誤差のみを考慮すれば良いので、加工精度を上げやすい反面、計算速度が遅くなる。

### ポリゴン型

3D加工用の形状を、例えば球面をミラーボールとして近似するように、微細平面の集まりとして近似する手法。平面への変換時に誤差が発生するため高い精度を保つのが難しく、計算時の精度だけを上げると、球面のはずが高精度なミラーボールになる。反面、計算速度が速い利点がある。 ファセット型とも呼ばれる。

CGモデラーのポリゴンデータを取り込むことが容易なため、CGモデルを直接使用した試作やモックアップ作製に利用されることもある。

## ソフト構成

CADとの構成による分類

### CAD+CAM

多くのソリッドCADシステムが、オプションとして、CAMモジュールを持っている。 CAM部分に重点を置くシステムでは、サーフィスCAD+CAMの構成もある。 2D、2.5DCAMもこのタイプとなる。

### CAM単体

多くの場合は、全自動タイプとなる。 CAD部分を持たないために、データコンバートが前提となり、ポリゴン変換を行ってパス計算に利用するものが多い。

## 工具軸

工具軸の扱いによる分類

### 工具軸固定

通常、2D～3D CAMと言えば、このタイプを指す。

### 工具軸傾斜固定

固定5軸,傾斜軸,3D+2などと呼ばれ、位置決め動作のみに5軸同時動作を行い、切削時には2軸同時から3軸同時データを出力する。

加工物の高さによって、側面又は斜め方向からの方が加工し易い場合に使用し、斜め方向の穴あけなどにも使用される。

回転軸の移動を伴わないために、リニアライゼーションによる精度低下が起こらないので、同時5軸制御の工作機でも、あえて傾斜固定を使用する場合もある。

### 工具軸傾斜連続的変化

同時5軸などと呼ばれ、3軸同時移動データに加え、工具軸を傾斜させるための回転軸のデータを出力する。

連続した曲面のアンダーカットがある形状を加工する場合や側面などの加工をする場合に有効。

主な用途は、プロペラやタービン形状の加工だが、一部金型業界でも利用されている。

3軸ツールパスを自動で同時5軸ツールパスに変換するソフトウェアもある。 \[1\]

### 多軸もしくは複合軸

複合旋盤に代表される、複数の工具を複数加工軸で並列的に制御して加工するデータを出力する。

## CAM操作例

切削系のCAM作業の流れ

### 形状データの入力

CAD/CAMタイプのCAD部分で形状を作成した場合は、単にCAMモードへの移行となる。

形状を作成したCADが異なる場合は、データの変換が必要。

### 形状の精査

加工上問題になる箇所を確認する。

不都合がある場合は修正するが、CAD機能を持っていない場合は、作成元のCADに戻って変更が必要。

一部自動で修正出来るCAMもある。

### 加工法の検討

CAMの種類により加工法に制限があるので、CAMごとに異なる加工法になる場合が多い。

CAMによって、数種類ないし数十種類の加工モードを持ち、その使いこなしのスキルが加工結果に大きく影響する。

### 加工条件の入力

CAMが加工条件のデータベースを持っている場合もあるが、千差万別の加工に対応しているわけではないので、大部分は作業者のノウハウによる。

### 切削工具の移動経路の作成

**カッターパス**又は**CL(カッターロケーション)**と呼ばれるCAM独自のフォーマットを出力する。

単純に工具中心軌跡を出力するCAMや、同時に工具長さの算出やジグ類との干渉をチェックを行うCAMがある。

CAMの計算時間と言った場合は、この部分の経過時間を指す。

### 移動経路を[シミュレーション](../Page/シミュレーション.md "wikilink")などで確認

経路の線画による物と、加工結果をオブジェクトとして見る物がある。

### NC機械用の加工データ生成

POST処理とも呼ばれる。NC機械ごとに調整されたデータを出力する。

5軸加工用のデータなどで、CAM自体のシミュレーション機能の不備や、POST処理後まで軸移動が確定しない場合などに、出力したNCデータを、さらにシミュレーションソフトにて主軸機構などの干渉チェックを行う場合もある。

## データ互換

形状を作成した[CAD](../Page/CAD.md "wikilink")と**CAM**が異なるシステムの場合は、データの変換による精度の低下や形状情報の欠落が問題となる。

幾何データの変換には**IGES**や **STEP**などが使用されるが、問題がある場合は**ダイレクトコンバータ**が使用される。また、異なるシステムでも、同じ**カーネル**（内部データベース方式)を持つ物なら、**カーネル**形式を使用して、精度の落ちないデータの受け渡しが可能である。(**parasolid**や**acis**など)

## 主なCAMソフトウェア

  - [ダッソー・システムズ](https://ja.wikipedia.org/wiki/ダッソー・システムズ "wikilink"): [CATIA](../Page/CATIA.md "wikilink")\[2\]

  - [シーメンス](../Page/シーメンス.md "wikilink"): [NX](../Page/UGS_NX.md "wikilink")\[3\]

  - [ヘクサゴン](https://ja.wikipedia.org/wiki/ヘキサゴン_\(スウェーデンの企業\) "wikilink") (社を買収): AlphaCAM、EdgeCAM、Machining Strategist、PEPS、SurfCAM、VISI、WorkNC / Dental

  - [Autodesk](https://ja.wikipedia.org/wiki/Autodesk "wikilink"): Inventor CAM (旧HSM)、、FeatureCAM、Fusion 360

  - (Geometric社を買収): CAMWorks\[4\]

  - OPEN MIND Technologies:

  - Tebis Technische Informationssysteme:

  - CNC Software:

  - [3D Systems](../Page/3D_Systems.md "wikilink") (社を買収): Cimatron、GibbsCAM

  - [PTC](https://ja.wikipedia.org/wiki/パラメトリック・テクノロジー・コーポレーション "wikilink"): [PTC Creo](https://ja.wikipedia.org/wiki/PTC_Creo_Parametric "wikilink")

  - CGTech:

  - Missler Software: [TopSolid](https://ja.wikipedia.org/wiki/TopSolid "wikilink")

  - SPRUT Technology: 、SprutCAM Robot

  - Scanvec Amiable:

  - Gravotech: TYPE EDIT、LASERTYPE

  - MecSoft Corporation: VisualCAD/CAM\[5\]、RhinoCAM ([Rhinoceros 3D向け](../Page/Rhinoceros_3D.md "wikilink"))、VisualCAM for SOLIDWORKS ([SolidWorks](../Page/SolidWorks.md "wikilink")向け)、AlibreCAM (向け)、FreeMill

  - C\&G Systems: CAM-TOOL

  - SolidCAM: SolidCAM

  - [NTTデータエンジニアリングシステムズ](https://ja.wikipedia.org/wiki/NTTグループ#NTTデータ "wikilink"): Space-E

  - BobCAD-CAM: -CAM

## 関連項目

  - [工作機械](../Page/工作機械.md "wikilink")
  - [CNC](https://ja.wikipedia.org/wiki/CNC "wikilink")

## 出典・脚注

[Category:CAD](https://ja.wikipedia.org/wiki/Category:CAD "wikilink") [Category:製造](https://ja.wikipedia.org/wiki/Category:製造 "wikilink") [Category:ITマネジメント](https://ja.wikipedia.org/wiki/Category:ITマネジメント "wikilink") [Category:コンピュータの利用](https://ja.wikipedia.org/wiki/Category:コンピュータの利用 "wikilink")

1.  MCADCafé. *[Sescoi's WorkNC 5-Axis and Auto 5 - a competitive advantage at ALLIO](http://www10.mcadcafe.com/nbc/articles/view_article.php?articleid=612505&interstitial_displayed=Yes)*.
2.  <http://www.3ds.com/investors/earnings/earnings-details/fiscal-year-2015-quarter-4-and-full-year-2015/>
3.  <http://www.engineering.com/PLMERP/ArticleID/12946/PLM-This-Week-CIMdata-Report-Shows-Dassault-Systemes-is-a-PLM-Revenue-Leader-in-2015.aspx>
4.  <http://geometricglobal.com/media-section/2016-media-release/geometrics-revenues-grow-11-6-in-fy16/>
5.  CADのVisualCAD及びCAMのVisualMillモジュール、VisualTURNモジュール、VisualNESTモジュール、VisualARTモジュールを含む
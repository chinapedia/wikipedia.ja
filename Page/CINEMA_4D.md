> この記事は[CINEMA 4D](https://ja.wikipedia.org/wiki/CINEMA_4D)から翻訳されています。


**CINEMA 4D**（シネマフォーディー）は[ドイツ](https://ja.wikipedia.org/wiki/ドイツ "wikilink")のMAXON Computer社による[3次元コンピュータグラフィックス](../Page/3次元コンピュータグラフィックス.md "wikilink")[ソフトウェア](../Page/ソフトウェア.md "wikilink")。 一般的に**C4D**（シーフォーディー）と略される。

## 概要

同種の商用[3DCGソフトウェア](https://ja.wikipedia.org/wiki/3DCGソフトウェア "wikilink")のように、ポリゴンや[NURBSを用いたモデリング](https://ja.wikipedia.org/wiki/:en:Non-uniform_rational_B-spline "wikilink")、レイアウト、キャラクタアニメーション、物理シミュレーション、物理ベースレンダリングなどが可能な機能を備えており、また[3ds Maxや](../Page/3ds_Max.md "wikilink")[Maya](../Page/Maya.md "wikilink")などの他の3DCGソフトウェアとの間でデータのインポート/エクスポートが可能である。CAD形式のインポートにも対応している。

元々、CINEMA 4Dは1990年代初頭に[Amiga](../Page/Amiga.md "wikilink")向けとして開発されたソフトウェアであり、バージョン2まではAmigaのみがサポートされていた。 しかし、[コモドール](../Page/コモドール.md "wikilink")の倒産以降はAmigaの将来性に対する不安から、MAXONはWindowsおよびMacintoshにおいても動作するCINEMA 4Dをリリースする事となり、V4以降からはAmigaのサポートが行われなくなった。

R11.5までは各種拡張機能をモジュールとして追加購入可能で予算に応じた構成が選択できたが、R12からは拡張機能の分売は行われず4種類のグレードに簡素化され、R21でサブスクリプション導入と共にグレードが廃止されて一本化された (詳細は[後述](https://ja.wikipedia.org/wiki/#エディション/モジュール/プラグイン/外部ツール "wikilink"))。

## エディション/モジュール/プラグイン/外部ツール

R21以降、以下のエディションが提供されている。

  - **Cinema 4D** - サブスクリプションと永久ライセンスが存在する
  - **Cinema 4D with Redshift** - Redshift Rendererが付属している

R23以降は以下も提供されている\[1\]。

  - **Maxon One** - Redshift RendererとRed Giant Completeが付属している

サブスクリプションでは様々なプラグインの付属するチュートリアルサービスCineversityが利用可能となる。Cineversityのプラグインを管理するプラグインとしてCV Toolboxがある。

### プラグイン/外部ツール

Cinema 4Dには高度な外部スカルプトモデラーの[ZBrush](../Page/ZBrush.md "wikilink")と連携可能なGo Zbrush (GoZ)機能\[2\]、高度なプロシージャルマテリアル作成ツールのSubstance Designerと連携可能なSubstance Engineなどが標準で内蔵されている\[3\]。 またゲームエンジンのUnityと連携するためのCineware for Unityプラグインが無料頒布されている\[4\]。

Cinema 4Dに搭載されていないUDIM、流体シミュレーション、VRプレビュー、高度なペイントなどに対応するサードパーティー製プラグインとしてGameLogicDesign製のPlugins 4D Pro Bundleがある。Pro Bundleのペイント部分は4D Paintとして無料提供されている\[5\]。

またサードパーティーの流体シミュレーションプラグインには、TurbulenceFD、 | Cinema 4D、X-Particles、FumeFXなどもある\[6\]。

### 過去のエディション/モジュール

R11.5までのCINEMA 4Dは以下のようなモジュールによる機能拡張が可能であった。

  - Advanced Render - [グローバル・イルミネーション](../Page/グローバル・イルミネーション.md "wikilink")、[HDRI](../Page/ハイダイナミックレンジイメージ.md "wikilink")、コースティクス、アンビエントオクルージョン、空のシミュレートが可能なレンダラー
  - BodyPaint 3D - UVWマップへ直接ペイント可能なツール。現在は本体に統合されている。実質的な機能としてはCINEMA 4D PrimeとBodyPaint 3Dは同一であるが、初期設定のUIに差がある。
  - Dynamics - [剛体](../Page/剛体.md "wikilink")およびソフトボディの物理演算モジュール
  - Hair - 髪や草のシミュレータ
  - MOCCA - キャラクタアニメーションや衣服のシミュレータ
  - MoGraph - モーショングラフィックスにおけるモデリングやアニメーションを簡略化するモジュール
  - NET Render - レンダーファームのようにネットワークで接続されたコンピュータ間で分散レンダリングを行うためのモジュール
  - PyroCluster - 煙および炎のシミュレータ（R10より、PyroClusterはAdvanced Renderに統合された）
  - Sketch & Toon - [トゥーンレンダリング](../Page/トゥーンレンダリング.md "wikilink")を行うモジュール
  - Thinking Particles - 拡張された[パーティクル](https://ja.wikipedia.org/wiki/パーティクル "wikilink")シミュレータ

R12以降はこれらのモジュール単位による機能拡張が廃止され、以下の4つのグレードとBodyPaint 3Dに統合されることとなった。

  - Prime（CINEMA 4D本体部分のみ）
  - Broadcast（本体に加え、映像・モーショングラフィックス向けの機能を含む）
  - Visualize（本体に加え、建築パース用途向けの機能を含む）
  - Studio（全機能を含む最上位グレード）

R21以降はサブスクリプションの導入と共にグレードが廃止され、通常版がStudio版相当となった。

## スクリプト/プラグイン開発

以前は独自のスクリプト言語であるを使うことでCinema 4Dを制御することが可能であったが、R12以降は3DCGソフトウェアで一般的に使われている[Python](../Page/Python.md "wikilink")にも対応し、R20でC.O.F.F.E.E.は廃止となった。R23ではPython 2.xからPython 3.xへと移行した。

またSDKにより[C++](../Page/C++.md "wikilink")言語でCinema 4D用のプラグインを開発することも可能となっている。

## バージョンの変遷

<table>
<thead>
<tr class="header">
<th><p>1990</p></th>
<th><ul>
<li>ChristianとPhilip Loschが<a href="../Page/レイトレーシング.md" title="wikilink">レイトレーシング</a>レンダラをKickstart誌の月間プログラミングコンテストに投稿し、優勝する。</li>
</ul></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>1991</p></td>
<td><ul>
<li>FastRay (CINEMA 4Dの初期の名称) がAmiga向けにリリースされる。</li>
</ul></td>
</tr>
<tr class="even">
<td><p>1993</p></td>
<td><ul>
<li>CINEMA 4D V1がAmiga向けにリリースされる。</li>
</ul></td>
</tr>
<tr class="odd">
<td><p>1994</p></td>
<td><ul>
<li>CINEMA 4D V2がAmiga向けにリリースされる。</li>
</ul></td>
</tr>
<tr class="even">
<td><p>1995</p></td>
<td><ul>
<li>CINAMA 4D V3がAmiga向けにリリースされる。V3はAmiga向けの最終バージョンとなる。</li>
<li>CINAMA 4DをWindows/Macintosh向けにリリースする計画が立てられ、開発が開始される。</li>
</ul></td>
</tr>
<tr class="odd">
<td><p>1996</p></td>
<td><ul>
<li>CINEMA 4D V4 がWindows, Alpha NT, Macintosh向けにリリースされる.
<ul>
<li>マルチプロセッサのサポートが開始される。</li>
</ul></li>
</ul></td>
</tr>
<tr class="even">
<td><p>1997</p></td>
<td><ul>
<li>CINEMA 4D XL V5がリリースされる。</li>
</ul></td>
</tr>
<tr class="odd">
<td><p>1998</p></td>
<td><ul>
<li>CINEMA 4D SE V5がリリースされる。</li>
</ul></td>
</tr>
<tr class="even">
<td><p>1999</p></td>
<td><ul>
<li>CINEMA 4D GO V5 および CINEMA 4D NETがリリースされる。</li>
</ul></td>
</tr>
<tr class="odd">
<td><p>2000</p></td>
<td><ul>
<li>CINEMA 4D XL V6がリリースされる。</li>
<li>BodyPaint 3Dが利用可能になる。CINEMA 4Dに統合されたものと他の3DCGアプリケーション向けのスタンドアロン版の2種類が用意された。</li>
</ul></td>
</tr>
<tr class="even">
<td><p>2001</p></td>
<td><ul>
<li>CINEMA 4D ARTが導入される。</li>
<li>PyroClusterとDynamicsモジュールが導入される。</li>
<li>CINEMA 4D XL R7が海外市場へ輸出される。</li>
</ul></td>
</tr>
<tr class="odd">
<td><p>2002</p></td>
<td><ul>
<li>CINEMA 4D R8がリリースされる。
<ul>
<li>Advanced Render、PyroCluster、MOCCA、Thinking Particlesなどの新規モジュールが用意された。</li>
</ul></li>
</ul></td>
</tr>
<tr class="even">
<td><p>2003</p></td>
<td><ul>
<li>CINEMA 4D R8.5がリリースされる。</li>
<li>BodyPaint 3D R2がリリースされ、Sketch and Toonモジュールが導入される。</li>
</ul></td>
</tr>
<tr class="odd">
<td><p>2004</p></td>
<td><ul>
<li>CINEMA 4D R9がリリースされる。</li>
</ul></td>
</tr>
<tr class="even">
<td><p>2005</p></td>
<td><ul>
<li>CINEMA 4D R9.5がリリースされる。
<ul>
<li>Hairモジュールが導入される。</li>
</ul></li>
</ul></td>
</tr>
<tr class="odd">
<td><p>2006</p></td>
<td><ul>
<li>CINEMA 4D R9.6がリリースされる。
<ul>
<li>MoGraphモジュールが導入される。</li>
</ul></li>
<li>BodyPaint 3Dと統合されたCINEMA 4D R10がリリースされる。</li>
</ul></td>
</tr>
<tr class="even">
<td><p>2007</p></td>
<td><ul>
<li>CINEMA 4D R10.5がリリースされ、Hairモジュールの最適化と同様にMOCCAとMoGraphの機能アップグレードがなされた。</li>
</ul></td>
</tr>
<tr class="odd">
<td><p>2008</p></td>
<td><ul>
<li>CINEMA 4D R11がリリースされる。
<ul>
<li>Apple G5およびIntelベースのMacにおける64bit環境をサポート。</li>
<li>Advanced Renderにおけるグローバル・イルミネーションの品質向上が実施される。</li>
</ul></li>
</ul></td>
</tr>
<tr class="even">
<td><p>2009</p></td>
<td><ul>
<li>CINEMA 4D R11.5がリリースされる。
<ul>
<li>画像を正方形に分割してレンダリングするバケットレンダリングのサポートによって所要時間の短縮やメモリ管理の効率化が図られた。</li>
</ul></li>
</ul></td>
</tr>
<tr class="odd">
<td><p>2010</p></td>
<td><ul>
<li>CINEMA 4D R12がリリースされる。
<ul>
<li>ダイナミクスおよびレンダラ関連の改善が実施された。また、リニアワークフローやライトにおけるIESデータ、OpenGL 3がサポートされた。</li>
<li><a href="../Page/Python.md" title="wikilink">Python</a>が統合された。</li>
<li><a href="../Page/PowerPC.md" title="wikilink">PowerPC</a>のサポートが打ち切られた。</li>
</ul></li>
</ul></td>
</tr>
<tr class="even">
<td><p>2011</p></td>
<td><ul>
<li>CINEMA 4D R13がリリースされる。
<ul>
<li>フィジカルレンダーが搭載された。</li>
</ul></li>
</ul></td>
</tr>
<tr class="odd">
<td><p>2012</p></td>
<td><ul>
<li>CINEMA 4D R14がリリースされる[7]。
<ul>
<li>スカルプトモデリングが可能となった[8]。</li>
</ul></li>
</ul></td>
</tr>
<tr class="even">
<td><p>2013</p></td>
<td><ul>
<li><a href="../Page/Adobe_After_Effects.md" title="wikilink">Adobe After Effects</a> CC(Creative Cloud)において、CINEMA 4DとAfter Effects間の3Dライブパイプライン「CINEWARE」とCINEMA 4Dの機能制限版である「CINEMA 4D Lite」が搭載される。[9]</li>
<li>CINEMA 4D R15がリリースされる。
<ul>
<li>レンダリング、タイポグラフィ関連の処理などが改善された。</li>
</ul></li>
</ul></td>
</tr>
<tr class="odd">
<td><p>2014</p></td>
<td><ul>
<li>CINEMA 4D R16がリリースされる[10]。
<ul>
<li>3Dカメラトラッキングが可能となった[11]。</li>
</ul></li>
</ul></td>
</tr>
<tr class="even">
<td><p>2015</p></td>
<td><ul>
<li>CINEMA 4D R17がリリースされる[12]。
<ul>
<li><a href="../Page/SketchUp.md" title="wikilink">SketchUp</a>形式 (SKP) の読み込みに対応した[13]。</li>
</ul></li>
<li>Cinema 4D向けの<a href="../Page/Houdini.md" title="wikilink">Houdini</a> Engineがリリースされる[14]。</li>
</ul></td>
</tr>
<tr class="odd">
<td><p>2016</p></td>
<td><ul>
<li>CINEMA 4D R18がリリースされる[15]。
<ul>
<li>Allegorithmic (後にAdobeが買収) のマテリアルエンジンであるSubstance Engineが統合された[16]。</li>
<li>オープンソースの細分割曲面ライブラリであるOpenSubdivが導入された[17]。</li>
</ul></li>
</ul></td>
</tr>
<tr class="even">
<td><p>2017</p></td>
<td><ul>
<li>CINEMA 4D R19がリリースされる[18]。
<ul>
<li>GPU対応のオープンソースレンダラーであるAMD Radeon ProRenderが搭載された[19]。</li>
</ul></li>
</ul></td>
</tr>
<tr class="odd">
<td><p>2018</p></td>
<td><ul>
<li>CINEMA 4D R20がリリースされる[20]。
<ul>
<li>オープンソースの疎ボリュームライブラリであるが導入された[21]。</li>
<li>様々なCAD形式 (<a href="../Page/CATIA.md" title="wikilink">CATIA</a> V5、、<a href="../Page/SolidWorks.md" title="wikilink">SolidWorks</a>、<a href="../Page/ISO_10303.md" title="wikilink">STEP</a>、<a href="https://ja.wikipedia.org/wiki/IGES" title="wikilink">IGES</a>) の読み込みに対応した[22]。</li>
</ul></li>
</ul></td>
</tr>
<tr class="even">
<td><p>2019</p></td>
<td><ul>
<li>CINEMA 4D R21がリリースされる。
<ul>
<li>Redshift Rendererのバンドル版が用意された。</li>
</ul></li>
</ul></td>
</tr>
<tr class="odd">
<td><p>2020</p></td>
<td><ul>
<li>CINEMA 4D S22がサブスクリプションのみでリリースされる[23]。
<ul>
<li><a href="https://ja.wikipedia.org/wiki/macOS" title="wikilink">macOS</a>版において<a href="https://ja.wikipedia.org/wiki/Metal_(API)" title="wikilink">Metal APIへと対応した</a>[24]。</li>
<li>Webで良く使われている<a href="https://ja.wikipedia.org/wiki/glTF" title="wikilink">glTF</a>形式への書き出しに対応した[25]。</li>
<li>ゲームエンジンのQuel Solaarで使われているUV展開技術「Ministry of Flat」が統合された[26]。</li>
</ul></li>
<li>CINEMA 4D R23がリリースされる[27]。
<ul>
<li>Redshift Renderer及びRed Giant Completeのバンドル版「Maxon One」が用意された[28]。</li>
<li>Python 3.xへと移行した[29]。</li>
<li>合併したRed Giant社の<a href="../Page/カラー・コレクション.md" title="wikilink">カラー・コレクション</a>ツールMagic Bullet Looksが統合された[30]。</li>
<li>オープンソースの自動リトポロジーライブラリであるInstant Meshesが導入された[31]。</li>
<li><a href="https://ja.wikipedia.org/wiki/Universal_Scene_Description" title="wikilink">Universal Scene Description形式の読み書きに対応した</a>[32]。</li>
<li>仮想ウォークスルー、AMD Radeon ProRender、サウンドシステムが削除された[33]。</li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>

## 無償学生版

2010年6月1日\[34\]から日本市場においてMAXON Computer Japanが中学校、高等学校、大学、大学院、専門学校（全日制）の学生を対象に最上位エディションのStudioを非商用利用に限定した上で無償配布しており、対象となる学生は郵送にて申請し、後日メールでシリアルキーとダウンロードURLを受け取ることによってCINEMA 4Dを利用することができた。2012年9月以降からはドイツのMAXON Computer本社が全世界で学生への無償配布を開始した\[35\]ため、日本市場独自の無償配布は終了しドイツの本社へWeb上で申請する形式に変更となった。（メールでシリアルキーとダウンロードURLを受け取る点に変更はない。）\[36\]無償学生版に機能制限は殆どないが、シリアルを必要とするプラグインは利用できない\[37\]ことに加え、タイトルバーに氏名と「無償学生版」の文字列が表示され、起動時および終了時にも学生版の商用利用は禁止である旨のダイアログボックスが表示されるなど、通常版といくつかの差異がある。また、バージョンについても基本的には最新のものが提供されるが、通常版のリリースからは数か月～1年遅れて配布される。同様の取り組みはライバル企業の[Autodeskでも行われている](../Page/オートデスク.md "wikilink")。

## CINEBENCH

CINEMA 4Dのレンダラーをベースにしたベンチマークソフト **CINEBENCH** （シネベンチ）もMAXON公式サイトにて配布されている。

### R15以前

CPU性能やグラフィックスカードのOpenGL性能を計測することが可能であり、特定のハードウェアに最適化されておらず、Windowsと汎用ビデオカードの組み合わせでもOpenGLの性能低下が発生しないため、CINEMA 4Dを導入しようと検討しているユーザだけでなく、自作PC関係の雑誌やコミュニティ上でハードウェアの絶対的な性能を比較する目的でとても重宝されている。 2010年2月にR11.5がリリース\[38\]されてから長らくバージョンアップが行われず、2013年9月にR15がリリースされたように、CINEMA 4Dの最新版とCINEBENCHの最新版が必ずしも連動しているわけではない。

  - ベンチマーク計測項目

<!-- end list -->

  - CPU性能 - 約28万ポリゴンあるシーン（静止画）のフォトリアルレンダリング処理におけるパフォーマンスを計測する。結果はポイントとして表される\[39\]。
  - グラフィックスカードのOpenGL性能 - カーチェイスシーン（動画）におけるOpenGLリアルタイムレンダリングのパフォーマンスを計測する。結果は1秒あたりのフレーム数（フレームレート）で表される\[40\]。

R11.5とR15のテスト内容は同一であるが、アルゴリズムが変更されているためベンチマークのスコアは双方の間で比較することができない\[41\]。複数の環境を比較する場合はバージョンを揃える必要がある。

### R20以降

レイレーシングライブラリのIntel Embreeが採用されたほか、GPUベンチマークが廃止された\[42\]。

## 脚注

## 関連項目

  - [3ds Max](../Page/3ds_Max.md "wikilink")
  - [Maya](../Page/Maya.md "wikilink")
  - [ZBrush](../Page/ZBrush.md "wikilink")
  - [Blender](../Page/Blender.md "wikilink")

## 外部リンク

  - [MAXON Computer Japan（日本語）](http://www.maxon.net/ja/home.html)
  - [MAXON Computer (英語)](http://www.maxon.net/)
  - [MAXON SDK SUPPORT - Development Support](https://developers.maxon.net/)

[Category:3DCGソフトウェア](https://ja.wikipedia.org/wiki/Category:3DCGソフトウェア "wikilink") [Category:MacOSのソフトウェア](https://ja.wikipedia.org/wiki/Category:MacOSのソフトウェア "wikilink") [Category:1991年のソフトウェア](https://ja.wikipedia.org/wiki/Category:1991年のソフトウェア "wikilink")

1.
2.  [Maxon ships Cinema 4D S22](http://www.cgchannel.com/2020/04/maxon-ships-cinema-4d-s22/) CG Channel 2020年4月21日
3.
4.  [Download Maxon’s free Cineware for Unity plugin](http://www.cgchannel.com/2020/03/download-maxons-free-cineware-for-unity-plugin/) CG Channel 2020年3月10日
5.  [Download Cinema 4D painting add-on 4D Paint for free](http://www.cgchannel.com/2020/07/download-cinema-4d-painting-plugin-4d-paint-for-free/) CG Channel 2020年7月21日
6.  [How to Animate Fluids in C4D Without Plugins](https://lesterbanks.com/2019/08/how-to-animate-fluids-in-c4d-without-plugins/) Lesterbanks 2019年8月14日
7.  [Maxon ships Cinema 4D R14](http://www.cgchannel.com/2012/09/maxon-announces-cinema-4d-r13/) CG Channel 2012年9月3日
8.
9.  [CINEWARE - MAXON公式サイト（日本語版）](http://www.maxon.net/ja/products/cineware/overview.html)
10. [Maxon releases Cinema 4D R16](http://www.cgchannel.com/2014/09/maxon-announces-cinema-4d-r16/) CG Channel 2014年9月3日
11.
12. [Maxon ships Cinema 4D R17](http://www.cgchannel.com/2015/09/maxon-announces-cinema-4d-r17/) CG Channel 2015年
13.
14.
15. [Maxon ships Cinema 4D R18](http://www.cgchannel.com/2016/09/maxon-unveils-cinema-4d-r18/) CG Channel 2016年9月1日
16.
17.
18. [Maxon ships Cinema 4D R19](http://www.cgchannel.com/2017/09/maxon-unveils-cinema-4d-r19/) CG Channel 2017年9月1日
19.
20. [Maxon ships Cinema 4D R20](http://www.cgchannel.com/2018/09/maxon-unveils-cinema-4d-r20/) CG Channel 2018年9月3日
21.
22.
23. [Maxon ships Cinema 4D S22](http://www.cgchannel.com/2020/04/maxon-ships-cinema-4d-s22/) CG Channel 2020年4月21日
24.
25.
26.
27. [Maxon unveils Cinema 4D R23](http://www.cgchannel.com/2020/09/maxon-unveils-cinema-4d-r23/) GG Channel 2020年9月9日
28.
29.
30.
31.
32.
33. [R23 - Removed features (Virtual Walkthrough, ProRender, Sound System)](https://support.maxon.net/kb/faq.php?id=108) MAXON
34. [MAXONは、学生に対してCINEMA 4D R11.5 Studio Bundleを無償配布することを発表](https://www.tmsmedia.co.jp/phpbb/viewtopic.php?f=2&t=22)
35. [CINEMA 4D R14 Student Version](http://www.maxon.net/en/products/general-information/general-information/student-versions.html)
36. [CINEMA 4D無償学生版について](http://www.cinema4d-student.jp/?page_id=90)
37. [よくある質問 - CINEMA 4D アカデミックサイト](http://www.cinema4d-student.jp/?p=11)
38. [MAXON、最大64スレッド対応の「CINEBENCH R11.5」](http://pc.watch.impress.co.jp/docs/news/20100212_348678.html) - PC Watch（2010年 2月 12日）
39.
40.
41.
42. [ベンチマークソフト「Cinebench R20」が登場、ストアアプリとして配布](https://pc.watch.impress.co.jp/docs/news/1173388.html) Impress 2019年3月7日
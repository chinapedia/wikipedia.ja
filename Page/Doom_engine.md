> この記事は[Doom engine](https://ja.wikipedia.org/wiki/Doom_engine)から翻訳されています。


**Doom engine**（ドゥームエンジン）と呼ばれる**id Tech 1**は、[id Softwareの](https://ja.wikipedia.org/wiki/id_Software "wikilink")[コンピュータゲーム](../Page/コンピュータゲーム.md "wikilink")『[Doom](../Page/DOOM.md "wikilink")』および『[Doom II：Hell on Earth](../Page/Doom_II.md "wikilink")』を動作させる[ゲームエンジン](../Page/ゲームエンジン.md "wikilink")。本エンジンは『Heretic』『Hexen: Beyond Heretic』『Strife: Quest for the Sigil』『Hacx: Twitch 'n Kill』『Freedom』のほか、ライセンス提供により制作されたゲームにおいても使用されている。これは、[ジョン・カーマックによって作成され](https://ja.wikipedia.org/wiki/ジョン・D・カーマック "wikilink")、マイク・アブラッシュ、ジョン・ロメロ、デイブ・テイラーおよびポール・ラデックによって書かれた補助機能を搭載している。元々は[NeXT](../Page/NeXT.md "wikilink")コンピュータで開発されたが、Doomの最初の発売のためにDOSに[移植され](../Page/移植_\(ソフトウェア\).md "wikilink")、その後いくつかの[ゲーム機](../Page/ゲーム機.md "wikilink")や[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink")に移植された。

[Linux](../Page/Linux.md "wikilink")版Doomのソースコードは1997年12月23日に非商用利用の権利を認めたライセンスの下で公開され、その約一週間後の1997年12月29日にLinux版Doom IIのソースコードも公開された\[1\]。その後、このソースコードは1999年10月3日に[GNU General Public Licenseに基づいて再公開された](../Page/GNU_General_Public_License.md "wikilink")\[2\]\[3\]。それ以降に数十の非公式の[Doomソース移植が制作され](../Page/Doomのソース移植一覧.md "wikilink")、それによりこれまでサポートされていなかったオペレーティングシステム上でDoomを実行でき、時には新しい機能でエンジンの機能を根本的に拡張する。

エンジンは3D空間をレンダリングするが、その空間は2次元の[平面図から投影される](https://ja.wikipedia.org/wiki/間取り図 "wikilink")。視線は常に床と平行であり、壁は床に対して垂直でなければならず、立体構造や傾斜エリア（角度の異なる床と天井）を作成することはできない。これらの制限にもかかわらず、エンジンはidの以前のWolfenstein 3Dエンジンからの技術的飛躍を示している。Doomエンジンは、id Softwareの長いゲームエンジンのリストに分類するために、後に「id Tech 1」と改名された\[4\]\[5\]。

## ゲームの世界

Doomエンジンは、レンダリングをゲームの他の部分から分離する。グラフィックエンジンは可能な限り高速で動作するが、ゲームの世界はハードウェアに関係なく35フレーム/秒で動作するため、性能の異なるコンピューターを使用して複数のプレイヤーが対戦することができる\[6\] 。

## ステージ構造

<div style="float: right; margin: 0 0 1em 1em; padding: 0.5em; background: #fffff4; border: 1px solid #ddddbb; width: 250px;">

`Doomがステージを内部的にどのように表しているのかを示す簡単な構成 `[`サムネイル`](https://ja.wikipedia.org/wiki/ファイル:Doom-map-format-map.svg "wikilink")

</div>

トップダウンから見ると、すべてのDoomのステージは実際には2次元であり、Doomエンジンの主要な制限の一つ、部屋の上に部屋を重ねる（room-over-room）ことが不可能であることを示している。ただし、この制限には希望の兆しがある。右側の最初の画像のように壁とプレイヤーの位置を表す「マップモード」を簡単に表示できる。

### 基本オブジェクト

基底単位は[頂点](https://ja.wikipedia.org/wiki/頂点 "wikilink")であり、単一の2D点を表す。次に、頂点（または内部的に参照される「頂点」）を結合して、「linedefs」と呼ばれる[線を形成する](../Page/直線.md "wikilink")。各linedefには、「sidedefs」と呼ばれる1つまたは2つの側面がある。次にSidedefをグループ化して[ポリゴンを形成する](../Page/多角形.md "wikilink")。これらは「セクター」と呼ばれる。セクターはステージの特定の領域を表す。

### セクター

各セクターには、床の高さ、天井の高さ、光のレベル、床の[テクスチャ](../Page/テクスチャマッピング.md "wikilink") 、天井のテクスチャなど、いくつかのプロパティが含まれている。たとえば、特定のエリアで異なるライトレベルを使用するには、そのエリアに異なるライトレベルで新しいセクターを作成する必要がある。したがって、片側のlinedefは無地の壁を表し、両側のlinedefはセクター間のブリッジラインを表す。

### Sidedefs

Sidedefは壁の[テクスチャを格納するために使用される](../Page/テクスチャマッピング.md "wikilink")。これらは、床や天井のテクスチャから完全に分離している。 各sidedefは3つのテクスチャを持つことができ、これらは中央、上部、下部テクスチャと呼ばれる。片側のlinedefでは、中央テクスチャのみが壁のテクスチャに使用される。両面linedefでは、状況はより複雑である。下部と上部テクスチャは、隣接するセクターの床と天井の高さが異なる場合に隙間を埋めるために使用される。たとえば、下部のテクスチャはステップに使用される。sidedefは中央テクスチャを持つこともできるが、ほとんどない。これは、テクスチャを空中にぶら下げるために使用される。たとえば、透明な棒のテクスチャがケージを形成している場合、これは両面linedefの中央テクスチャの一例である。

## バイナリ空間分割

Doomは、[バイナリ空間分割](https://ja.wikipedia.org/wiki/バイナリ空間分割 "wikilink")（BSP）と呼ばれるシステムを利用している\[7\]\[8\]。ツールを使用して、事前にステージのBSPデータを生成する。このプロセスは大きなステージではかなり時間がかかる場合があるため、Doomでは壁を移動することはできない。ドアとリフトは上下に動くが、どれも横には動かない。

レベルは[バイナリツリーに分割される](../Page/二分木.md "wikilink")。ツリー内の各位置はステージの特定の領域を表す「ノード」である（ルートノードはステージ全体を表す）。ツリーの各分岐には、ノードの領域を2つのサブノードに分割する分割線がある。同時に、この分割線はlinedefを「seg」と呼ばれるラインセグメントに分割する\[9\]。

ツリーの葉には[凸多角形](https://ja.wikipedia.org/wiki/凸多角形 "wikilink")があり、ステージをさらに分割する必要はない。これらの凸多角形はサブセクター（または「Sセクター」）と呼ばれ、特定のセクターにバインドされる。各サブセクターには、関連するsegのリストがある\[10\]。

BSPシステムは、サブセクターをレンダリングに適した順序に並べ替える。アルゴリズムはかなり単純である：

1.  ルートノードから開始する。
2.  このノードの子ノードを再帰的に描画する。カメラに最も近い子ノードは、スキャンラインアルゴリズムを使用して最初に描画される。これは、カメラがノードの分割線のどちら側にあるかを見ることで分かる。
3.  サブセクターに達したら、そのサブセクターを描画する\[11\]。

ピクセルの列全体が満たされる（つまり、これ以上隙間が残らなくなる）と、プロセスは完了する。この順序付けにより、表示されていないオブジェクトの描画に時間を費やすことがなくなり、その結果、速度のペナルティなしにマップを非常に大きくすることができる。

## レンダリング

### 壁の描写

Doomの壁はすべて垂直に描かれており、そのために上下を正しく見ることができない。「y-shearing」を使ってルックアップ/ダウンを行うことが可能で、多くの最新のDoomのソース移植や、『Heretic』のようなエンジンを使用する後のゲームでも同様に行える。本質的には、画面内で水平線を上下に移動させることで機能し、事実上より高い表示領域に「窓」を提供する。窓を上下に動かすことで、上下を見ているような錯覚を与えることができる。しかし、これでは、プレイヤーがさらに上下に見たときに視界が歪んでしまう。

Doom エンジンは、BSPツリーを横断する際に壁をレンダリングし、最も近いsegが最初に描画されるように、カメラからの距離順にサブセクターを描画する。segが描画されると、リンクされたリストに保存される。これは、後からレンダリングされる他のsegをクリップして、オーバードローを減らすために使用される。これは後にスプライトのエッジをクリップするときにも使われる。

エンジンが特定の x 座標で固体（片面）の壁に到達したら、その領域にはもう線を引く必要はない。クリッピングのために、エンジンは固体の壁に達した画面の領域の「マップ」を保存する。これにより、プレイヤーから見えないステージの遠くの部分を完全にクリッピングできる。

Doomのグラフィックフォーマットは、壁のテクスチャを垂直列のセットとして格納する。これは、本質的に、テクスチャの垂直列をたくさん描くことによって壁をレンダリングするレンダラーにとって便利である。

### 床と天井

床と天井（「フラット」）を描画するシステムは、壁に使用されるシステムよりも簡潔ではない。フラットは、塗りつぶしのようなアルゴリズムで描画されるため、不良なBSPビルダーを使用すると、床または天井が画面の端まで流れ落ちる「穴」ができてしまう場合がある。これは、プレイヤーが[noclipチートを使用してステージ外に移動した場合](../Page/Noclipモード.md "wikilink")、床と天井が空のスペースの上にステージからはみ出して見える理由でもある。

床と天井は「visplanes」として描画される。これらは、特定の高さ、光レベル、テクスチャ床または天井からのテクスチャの水平方向の流れを表している（2つの隣接するセクターがまったく同じ床を持つ場合、これらは1つのvisplaneに統合される）。 visplaneの各x位置には、描画されるテクスチャの特定の垂直線がある。

各x位置に1本の垂直線を描画するこの制限のため、visplaneを複数のvisplaneに分割する必要がある場合がある。たとえば、2つの同心円の正方形で床を表示することを検討する。内側の正方形は、周囲の床を垂直に分割する。内側の四角形が描かれるその水平範囲では、周囲の床に2つのvisplaneが必要となる。

これが、長い間、多くのマッパーを苛立たせてきたDoomの古典的な制限の一つにつながる。Doomには、visplanesの数に静的な制限が含まれており、それを超過すると、「visplaneオーバーフロー」が発生し、「No more visplanes！」または「visplane overflow （128 or higher）」という2つのメッセージのいずれかと共にゲームは終了してDOSに戻る。 visplane制限を呼び出す最も簡単な方法は、多数のvisplaneを生成する大きな市松模様の床パターンである。

segがレンダリングされると、segのエッジから画面の垂直エッジに向かって延びるvisplanesも追加される。これらは、既存のvisplaneに到達するまで延長する。このように機能するため、このシステムは、segがエンジン全体によって順番にレンダリングされるという事実に依存している。遠くにある他の人が「カットオフ」できるように、最初により近いvisplaneを描画する必要がある。前述のように、停止していない場合、床または天井は画面の端まで「流れ出てしまう」。 最終的に、visplaneは、特定のテクスチャを描画する画面の特定の領域の「マップ」を形成する。

visplaneは本質的に垂直の「ストライプ」から構築されるが、実際の低レベルのレンダリングはテクスチャの水平の「スパン」の形で実行される。すべてのvisplaneが構築された後、それらはスパンに変換され、画面にレンダリングされる。visplaneを垂直ストライプとして作成する方が簡単ですが、床と天井のテクスチャがどのように表示されるかという性質上、水平ストライプとして描画する方が簡単というトレードオフの関係になっている。

### モノ（スプライト）

ステージ内の各セクターには、そのセクターに格納されているもののリンクされたリストがある。各セクターが描画されると、スプライトは描画されるスプライトのリストに配置される。視野内にない場合、これらは無視される。

スプライトのエッジは、以前に描画されたsegのリストをチェックすることによってクリップされる。Doomのスプライトは壁と同じ列ベースのフォーマットで保存されているので、これもレンダラーにとって役立つ。壁の描画に使われているのと同じ関数がスプライトの描画にも使用される。

サブセクターの順序は保証されているが、サブセクター内のスプライトはそうではない。Doomは、描画するスプライト（「vissprites」）のリストを保存し、レンダリング前にリストをソートする。遠くのスプライトは、近くのスプライトより先に描画される。これにより多少のオーバードローが発生するが、通常は無視できる。

たとえば、透明なバーで使用される2辺のラインにある中央テクスチャの最後の問題がある。これらは他の壁ではなく、レンダリングプロセスの最後にスプライトと混合されて描画される。

## Doomエンジンを使用するゲーム

Doomエンジンは、ファーストパーソン・シューティングゲーム『DOOM』を動作させたことで名声を博し、他のいくつかのゲームでもエンジンが使用された。Doomエンジンのゲームの「ビッグ4」 は、『Doom』『Heretic』『Hexen: Beyond Heretic』『Strife: Quest for the Sigil』と一般的に考えられている。

  - Doomエンジンで直接制作されたゲーム

<!-- end list -->

  - 『[Doom](../Page/DOOM.md "wikilink")』 （1993）
      - 『[The Ultimate Doom](../Page/Doomの公式版.md "wikilink")』（1995）
  - 『[Doom II：Hell on Earth](../Page/Doom_II.md "wikilink")』（1994）
      - 『[Master Levels for Doom II](../Page/Doom_II.md "wikilink")』（1995）
  - 『[Final Doom](../Page/Final_Doom.md "wikilink")』 （1996）
  - 『Heretic』（1994）
      - 『Heretic: Shadow of the Serpent Riders』（1996）
  - 『Hexen: Beyond Heretic』（1995）
      - 『Hexen: Deathkings of the Dark Citadel』（1996）
  - 『Strife: Quest for the Sigil』（1996）
  - 『[Chex Quest](../Page/Chex_Quest.md "wikilink")』（1996）
      - 『[Chex Quest 2：Flemoids Take Chextropolis](../Page/Chex_Quest.md "wikilink")』（1997）

<!-- end list -->

  - DoomまたはDoom IIコードに基づくゲーム

<!-- end list -->

  - 『[Doom 64](https://ja.wikipedia.org/wiki/Doom_64 "wikilink")』（1997）
  - 『[Hacx：Twitch 'n Kill](../Page/Doomの改造.md "wikilink")』（1997）

## 関連項目

  - [Quake Engine](../Page/Quake_Engine.md "wikilink")

## 参考資料

  - [GLノードの仕様](http://glbsp.sourceforge.net/specs.php)
  - [DoomおよびDoom2の編集ユーティリティ](https://web.archive.org/web/20070305204905/http://www.doomworld.com/classicdoom/utils/editors.php)
  - Fabien Sanglardによる[Doomエンジンコードのレビュー](http://fabiensanglard.net/doomIphone/doomClassicRenderer.php)

## 脚注

## 外部リンク

  - [Doom](https://doomwiki.org/wiki/Doom_engine) [Wiki](https://doomwiki.org)の[Doomエンジン](https://doomwiki.org/wiki/Doom_engine)
  - [Doom](https://doomwiki.org/wiki/Doom_rendering_engine) [Wiki](https://doomwiki.org)の [Doomレンダリングエンジン](https://doomwiki.org/wiki/Doom_rendering_engine)
  - [Doomエンジンの完全なゲームリスト](http://www.uvlist.net/groups/info/doomengine)
  - [Doomエンジンのソースコード](https://github.com/id-Software/DOOM)

[Category:1993年のソフトウェア](https://ja.wikipedia.org/wiki/Category:1993年のソフトウェア "wikilink") [Category:ゲームエンジン](https://ja.wikipedia.org/wiki/Category:ゲームエンジン "wikilink") [Category:Doom_(フランチャイズ)](https://ja.wikipedia.org/wiki/Category:Doom_\(フランチャイズ\) "wikilink")

1.
2.  [The *Doom* source code](ftp://ftp.idsoftware.com/idstuff/source/) - released in 1997, now under the [GNU General Public License](../Page/GNU_General_Public_License.md "wikilink") from Id Software's FTP Site
3.  [The *Doom* source code from 3ddownloads.com](http://www.3ddownloads.com/showfile.php3?file_id=7430)  - released in 1997, now under the [GNU General Public License](../Page/GNU_General_Public_License.md "wikilink")
4.
5.
6.
7.
8.
9.
10.
11.
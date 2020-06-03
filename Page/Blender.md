> この記事は[Blender](https://ja.wikipedia.org/wiki/Blender)から翻訳されています。


**Blender**（ブレンダー）とは、[オープンソース](../Page/オープンソース.md "wikilink")の統合型[3DCGソフトウェア](https://ja.wikipedia.org/wiki/3DCGソフトウェア "wikilink")の一つであり、3Dモデル作成、レイアウト、[アニメーション](https://ja.wikipedia.org/wiki/コンピュータアニメーション "wikilink")、シミュレーション、[レンダリング](../Page/レンダリング_\(コンピュータ\).md "wikilink")、[デジタル合成](../Page/デジタル合成.md "wikilink") (コンポジット)などの機能を備えている。

また、バージョン2.8以降は2D Animationテンプレートを持っており、[2Dアニメーション制作ソフトとして使うことも容易となっている](https://ja.wikipedia.org/wiki/2Dアニメーション制作ソフト一覧 "wikilink")。

## 特徴

[ワークステーション](../Page/ワークステーション.md "wikilink")が必要でライセンス料も高価なプロフェッショナル向けの3DCGソフトウェアと比較し、市販の[パソコン](https://ja.wikipedia.org/wiki/パソコン "wikilink")で動作し無償で利用出来ることから、アマチュアを中心に普及が進んでいる\[1\]。

プロ向けは[Maya](../Page/Maya.md "wikilink")、[3ds Max](../Page/3ds_Max.md "wikilink")、[Softimage](../Page/Softimage.md "wikilink")が標準となっているが\[2\]、近年では機能が強化されたことで利用する動きもある\[3\]。[カラーとその子会社であるプロジェクトスタジオQは従来使用してきた](../Page/カラー_\(アニメ制作会社\).md "wikilink")[3ds MaxからBlenderへの移行を進めており](../Page/3ds_Max.md "wikilink")、制作中の『[シン・エヴァンゲリオン劇場版<nowiki>](https://ja.wikipedia.org/wiki/シン・エヴァンゲリオン劇場版 "wikilink"):』においてもBlenderの「実地検証」を実施している\[4\]。また、両社はBlender財団への賛同と開発資金の提供を発表した\[5\]\[6\]。

画面描画の[バックエンド](https://ja.wikipedia.org/wiki/バックエンド "wikilink")に[OpenGL](../Page/OpenGL.md "wikilink") 3.3以降を採用している\[7\]。

操作体系面では、バージョン2.7x系までは「オブジェクト(個々の3Dモデル)は右クリックで選択」が基本という、他の大半のソフトウェアと異なる点が特徴の一つ(選択に用いる際のマウスボタンクリックの右と左を入れ替える事は、バージョンを問わずユーザー設定にて可能)であったが、バージョン2.8x以降は「左クリックで選択・右クリックでサブメニュー」という、一般的なソフトウェアの操作に倣っている。その他、プレビュー表示でGPU機能を多用する関係もあり、例えば[nVidia](https://ja.wikipedia.org/wiki/nVidia "wikilink")のグラフィックカードであればGeForce 200やそれ以降の製品が必須となる→[Supported GPUs in Blender 2.80](https://code.blender.org/2019/04/supported-gpus-in-blender-2-80/)。

### Grease Pencil

3Dベクターペイント機能。3Dモデリングのための下書き、ストーリーボード\[8\]\[9\]、手描きアニメーションなどに使うことが出来る。またストロークのリギング機能があり、カットアウトアニメーションを作ることも可能となっている\[10\]。

2Dアニメーションに向けて2D Animationテンプレートが付属している。

### モデリング

ツール毎に独自の操作ウィジェットを持つポリゴンモデリング機能、非破壊モデリングのためのモディファイア機能、高度なスカルプトモデリング機能などを備えている。スカルプトモデリングの専用テンプレートが搭載されている。

またモデリング用として様々なアドオンが存在する。

### アニメーション

単純なアニメーション、Python式を使った連動アニメーション (ドライバー\[11\])、[スケルタルアニメーション](https://ja.wikipedia.org/wiki/スケルタルアニメーション "wikilink") (ボーンアニメーション)などに対応している。

スケルタルアニメーションでは (FK・順運動学)、 (IK・逆運動学)の両方に対応している。IKソルバーにはBlender独自のものとiTaSCベースのもの\[12\]が搭載されている。を含む様々な拘束が可能。

### シミュレーション

シミュレーションにはBulletベースの剛体シミュレーション\[13\]、独自の布・軟体・ヘアシミュレーション、Mantaflowベースの流体シミュレーション (液体・気体)\[14\]などが搭載されている。

### レンダリング

現行の内蔵レンダラーにはWorkbench、Eevee、Cyclesが存在する。Workbenchはビューポート向けの作業用レンダラーであり、Eeveeは高度なリアルタイムレンダラーとなっている。CyclesはGPU/対応のパストレーシングレンダラーであり、オフラインレンダリング向けとなっている。レンダリング手法が異なることもあり、CyclesとEeveeの間にはマテリアルなどの非互換性が多少存在する\[15\]。

また、過去のレンダラーには[スキャンライン](https://ja.wikipedia.org/wiki/3次元コンピュータグラフィックス#スキャンライン "wikilink")/[レイトレーシング](../Page/レイトレーシング.md "wikilink")ハイブリッドレンダラーのBlender Internalが存在した。Blender Internalはバージョン2.8で削除された。

### コンポジティング

ノードベースのコンポジット機能を搭載しており、様々な画像処理が可能となっている。OpenCLによるGPU処理に対応している。ディープコンポジティングには対応していない。

### 動画編集

動画編集用の Video Sequence Editor (VSE) 機能が搭載されている。動画のサムネイルは表示されない 。プロキシ編集に対応している。

### ゲームエンジン

2.7xまではゲームエンジン機能を内蔵しており、ロジックノードや[Python](../Page/Python.md "wikilink")[スクリプト](../Page/スクリプト.md "wikilink")を利用することでインタラクティブな[コンテンツ](../Page/コンテンツ.md "wikilink")を制作することが可能であった。2.8ではゲームエンジン機能が一旦削除されたものの、今後インタラクティブモードが再度追加される予定となっている。

なお、2.8xで旧来のゲームエンジンが使用できる派生版のUPBGEも存在する。

## バージョン履歴

2004年、2.33から物理ライブラリのライセンス問題によりオープンソース化してから長く取り外されていたゲームエンジンが再統合された。

バージョン2.5系列では、UIの一新、Maya FluidやFume FXのような本格的な流体システムに加え、ほぼ全機能の近代化改修、ブラッシュアップが行われ、2011年4月に初の安定版がリリースされた。

バージョン2.6系列では、2.61において[レンダラ](https://ja.wikipedia.org/wiki/レンダラ "wikilink")であるCyclesやダイナミックペイント、海洋シミュレーション、カメラトラッキング等、他のハイエンドツールにも匹敵する機能を追加し、また、2.63では新しい[メッシュ編集構造であるBMeshの統合もされた](https://ja.wikipedia.org/wiki/ポリゴンメッシュ "wikilink")。

### 国際化と地域化

日本語環境は2.49aまでは貧弱だったが、2.49bにて[2ちゃんねる](../Page/2ちゃんねる.md "wikilink")のBlenderスレッドの有志が制作・配布した詳細な日本語翻訳テーブルが公式採用された事で強化された。 その後、バージョン2.5系列で[国際化がなくなり日本語環境での使用はできなくなっていたが](../Page/国際化と地域化.md "wikilink")、GSoC2011にて国際化され、平行して日本の有志により再び日本語対応が行われ、バージョン2.60にて公式に日本語環境が復活した。

## 歴史

Blenderの前身である**Traces**は、オランダの[CG](https://ja.wikipedia.org/wiki/CG "wikilink")スタジオ、NEOGEO社の共同創設者の一人であるトン・ローセンダール (Ton Roosendaal) によって、[AmigaOS](../Page/AmigaOS.md "wikilink")向けのレイトレーシングレンダラーとして開発され、後にSGI [IRIX](../Page/IRIX.md "wikilink")へと移植された。その後、Tracesのソースコードは書き直されて、Blenderとなった。

[1998年](https://ja.wikipedia.org/wiki/1998年 "wikilink")、トン・ローセンダールはインハウス・ツールとして使用されてきたBlenderの開発・外販を行う為に社を設立した。Windows版も用意され、[ラジオシティ](../Page/ラジオシティ.md "wikilink")機能などを実装した有料版と無料版の二種を展開した。

2001年、NaN社は、Web3Dに向けて、Blender Webプラグインのベータ版をリリースした\[16\]が、セキュリティの問題から頓挫した。[2002年](../Page/2002年.md "wikilink")、[インターネット・バブル](https://ja.wikipedia.org/wiki/インターネット・バブル "wikilink")の崩壊と共にNaN社は[倒産](../Page/倒産.md "wikilink")し、Blenderの[ソースコード](../Page/ソースコード.md "wikilink")は債権者の手に渡ってしまう。しかし開発途上にあったBlenderを手放すことができなかったトン・ローセンダールはを設立するため、"ソースコード解放"を合言葉に大々的な[募金](https://ja.wikipedia.org/wiki/募金 "wikilink")キャンペーンを行い半年で10万[ユーロ](../Page/ユーロ.md "wikilink")を世界中から集結させ、ソースコードを再びその手に取り戻した。

そして現在までBlenderは、GPLの下にオープンソースウェアとして開発・無償配布されている。ソースコードのコメントが[オランダ語](../Page/オランダ語.md "wikilink")で書かれている上に、プログラム自体が定石から外れた組み方をしているため、開発を引き次いだ有志は他[OSへの移植などで苦戦したという](../Page/オペレーティングシステム.md "wikilink")。

2008年、UI一新などを目的とするBlender 2.5の開発が開始された。バージョン2.4系は2009年のBlender2.49をもって開発終了し、2011年に2.5系の初の安定板となるバージョン2.57がリリースされた。バージョン2.5系は2018年の2.79bをもって開発終了し、2019年7月にリアルタイムレンダラ「Eevee」やフィジカルベースドレンダリング（PBR）などに対応した2.8系の初の安定版となるバージョン2.80がリリースされた。特定の版における機能の凍結と長期サポート（Long-term support）を求める企業ユーザーからの要望により、2.8系は2020年5月リリースの2.83が「LTS版」として凍結され、2.9系に移行する予定。

2020年4月現在、アセットマネージメントなど次世代3DCGソフトに求められる機能の全てを搭載するのはさらに先になる予定が示されているが、LTS版の導入によって最新版での実験的機能の投入がやりやすくなるとのことで、2021年には21年ぶりのメジャーバージョンアップとなるバージョン3.0系のリリースが予定されている。2018年2月に「Blender 2.8 Code Quest」が開始され、開発資金を集めるためのグッズの販売や、スポンサーの募集などを行っている。

## 動作環境

[`Windows`](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")`（バージョン7、8、10）、`[`macOS`](https://ja.wikipedia.org/wiki/macOS "wikilink")`（10.12以上）、`[`Linux`](../Page/Linux.md "wikilink")など`、多`[`OS`](../Page/OS.md "wikilink")環境で動作する` `[`クロスプラットフォーム`](../Page/クロスプラットフォーム.md "wikilink")が特徴である`。ZIP版と`[`インストーラー`](https://ja.wikipedia.org/wiki/インストーラー "wikilink")版が用意されている`。ファイルの`[`拡張子`](../Page/拡張子.md "wikilink")は`『.blend』となる。`

| 最小限動作環境                                                          | 推薦動作環境                                                               | 快適動作環境              |
| ---------------------------------------------------------------- | -------------------------------------------------------------------- | ------------------- |
| 64ビットデュアルコア 2Ghz CPU（SSE2）                                       | 64ビット [クアッドコア](https://ja.wikipedia.org/wiki/クアッドコア "wikilink")CPU   | 64-bit 8コアCPU       |
| 4 GB RAM                                                         | 16 GB RAM                                                            | 32 GB RAM           |
| 1280×768ドット表示                                                    | [Full HD](https://ja.wikipedia.org/wiki/1080p "wikilink")（1920×1080） | 複数のFull HD表示        |
| マウス・トラックパッド・ペン/タブレット                                             | 3ボタンマウス又はペン/タブレット                                                    | 3ボタンタブレットとペン/タブレット  |
| メモリ1GB以上のグラフィックカード（[OpenGL](../Page/OpenGL.md "wikilink") 3.3以上） | メモリ4GB以上のグラフィックカード                                                   | メモリ12GB以上のグラフィックカード |

## 参考画像

## 脚注

### 注釈

### 出典

## 外部リンク

  -
  - [Blender Foundation](http://www.blender.org/blenderorg/blender-foundation/)

  - [BlenderArtists](http://www.blenderartists.org/)（ほぼ公式のコミュニティサイト）

  - [BlenderNation](http://www.blendernation.com/)（ほぼ公式ニュースサイト）

  -
  -
  -
  -
[Category:Windowsのソフトウェア](https://ja.wikipedia.org/wiki/Category:Windowsのソフトウェア "wikilink") [Category:MacOSのソフトウェア](https://ja.wikipedia.org/wiki/Category:MacOSのソフトウェア "wikilink") [Category:1995年のソフトウェア](https://ja.wikipedia.org/wiki/Category:1995年のソフトウェア "wikilink") [Category:オープンソースソフトウェア](https://ja.wikipedia.org/wiki/Category:オープンソースソフトウェア "wikilink") [Category:クロスプラットフォームのソフトウェア](https://ja.wikipedia.org/wiki/Category:クロスプラットフォームのソフトウェア "wikilink") [Category:映像編集・合成ソフト](https://ja.wikipedia.org/wiki/Category:映像編集・合成ソフト "wikilink") [Category:3DCGソフトウェア](https://ja.wikipedia.org/wiki/Category:3DCGソフトウェア "wikilink") [Category:視覚効果ソフトウェア](https://ja.wikipedia.org/wiki/Category:視覚効果ソフトウェア "wikilink") [Category:Blender_Foundation](https://ja.wikipedia.org/wiki/Category:Blender_Foundation "wikilink")

1.  [初めての3DCGから本格ゲーム開発まで予算10万円台"Blender"向けPCを MUGENUPが検証\!](https://cgworld.jp/interview/201812-unitcom.html) - CGWORLD.jp
2.
3.  [User Stories — blender.org](https://www.blender.org/features/user-stories/)
4.
5.
6.
7.  [Requirements — blender.org](https://www.blender.org/download/requirements/)
8.  [Blender 2.73 – A New Storyboard Workflow](https://gooseberry.blender.org/blender-2-73-a-new-storyboard-workflow/) The Gooseberry Open Movie Project 2015年1月15日
9.  [Storyboarding with Grease Pencil](http://www.blendernation.com/2016/08/17/storyboarding-grease-pencil/) BlenderNation 2016年8月17日
10. [Grease Pencil » Grease Pencil Weight Paint Mode » Introduction](https://docs.blender.org/manual/en/2.83/grease_pencil/modes/weight_paint/introduction.html) Blender Foundation
11. 2.4x以前はIpo Driver
12. 『Simulation, Modeling, and Programming for Autonomous Robots - Second International Conference, SIMPAR 2010』 P.16 Noriako Ando, et al. 2010年11月 ISSN 0302-9743
13. [Blender 2.66 adds Bullet physics, Dynamic Topology](http://www.cgchannel.com/2013/02/blender-2-66-adds-bullet-physics-dynamic-topology/) CG Channel 2013年2月22日
14. [Blender Foundation releases Blender 2.82](http://www.cgchannel.com/2020/02/blender-foundation-releases-blender-2-82/) CG Channel 2020年2月14日
15. [Rendering » Eevee » Limitations](https://docs.blender.org/manual/en/latest/render/eevee/limitations.html) Blender Foundation
16. [Blender - news - Web Plug-in](http://download.blender.org/documentation/oldsite/oldsite.blender3d.org/202_Blender%20news%20Web%20Plug-in.html) NaN 2001年8月16日
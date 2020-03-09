> この記事は[Blender](https://ja.wikipedia.org/wiki/Blender)から翻訳されています。


**Blender**（ブレンダー）とは、[オープンソース](../Page/オープンソース.md "wikilink")の統合型[3DCGソフトウェア](https://ja.wikipedia.org/wiki/3DCGソフトウェア "wikilink")の一つであり、3Dモデル作成、レイアウト、[アニメーション](https://ja.wikipedia.org/wiki/コンピュータアニメーション "wikilink")、シミュレーション、[レンダリング](https://ja.wikipedia.org/wiki/レンダリング_\(コンピュータ\) "wikilink")、[デジタル合成](https://ja.wikipedia.org/wiki/デジタル合成 "wikilink") (コンポジット)などの機能を備えている。

また、バージョン2.8以降は2D Animationテンプレートを持っており、[2Dアニメーション制作ソフトとして使うことも容易となっている](https://ja.wikipedia.org/wiki/2Dアニメーション制作ソフト一覧 "wikilink")。

## 特徴

特徴的で独自の[ユーザインタフェース](../Page/ユーザインタフェース.md "wikilink") (UI) を持つ。

。

画面描画の[バックエンド](https://ja.wikipedia.org/wiki/バックエンド "wikilink")に[OpenGL](https://ja.wikipedia.org/wiki/OpenGL "wikilink")を採用している\[1\]。

様々な機能と柔軟性から、徐々にプロフェッショナルの現場で使用されはじめている\[2\]。[カラーとその子会社であるプロジェクトスタジオQは従来使用してきた](https://ja.wikipedia.org/wiki/カラー_\(アニメ制作会社\) "wikilink")[3ds MaxからBlenderへの移行を進めており](https://ja.wikipedia.org/wiki/3ds_Max "wikilink")、制作中の『[シン・エヴァンゲリオン劇場版<nowiki>](https://ja.wikipedia.org/wiki/シン・エヴァンゲリオン劇場版 "wikilink"):』においてもBlenderの「実地検証」を実施している\[3\]。また、両社はBlender財団への賛同と開発資金の提供を発表した\[4\]\[5\]。

### モデリング

ツール毎に独自の操作ウィジェットを持つポリゴンモデリング機能、非破壊モデリングのためのモディファイア機能、高度なスカルプトモデリング機能などを備えている。スカルプトモデリングの専用テンプレートが搭載されている。

またモデリング用として様々なアドオンが存在する。

### シミュレーション

シミュレーションにはBulletベースの剛体シミュレーション\[6\]、独自の布・軟体・ヘアシミュレーション、Mantaflowベースの流体シミュレーション (液体・気体)\[7\]などが搭載されている。

### レンダリング

現行の内蔵レンダラーにはWorkbench、Eevee、Cyclesが存在する。Workbenchはビューポート向けの作業用レンダラーであり、Eeveeは高度なリアルタイムレンダラーとなっている。CyclesはGPU対応のパストレーシングレンダラーであり、オフラインレンダリング向けとなっている。レンダリング手法が異なることもあり、CyclesとEeveeの間にはマテリアルの非互換性が多少存在する。

また、過去のレンダラーには[スキャンライン](https://ja.wikipedia.org/wiki/3次元コンピュータグラフィックス#スキャンライン "wikilink")/[レイトレーシング](../Page/レイトレーシング.md "wikilink")ハイブリッドレンダラーのBlender Internalが存在した。Blender Internalはバージョン2.8で削除された。

### コンポジティング

ノードベースのコンポジット機能を搭載している。2.81で高度なデノイズが可能となった。

### ゲームエンジン

2.7xまではゲームエンジン機能を内蔵しており、[Python](../Page/Python.md "wikilink")[スクリプト](https://ja.wikipedia.org/wiki/スクリプト "wikilink")などを利用することでインタラクティブな[コンテンツ](../Page/コンテンツ.md "wikilink")を制作することが可能であった。2.8ではゲームエンジン機能が一旦削除されたものの、今後インタラクティブモードが再度追加される予定となっている。

## バージョン履歴

2004年、2.33から物理ライブラリのライセンス問題によりオープンソース化してから長く取り外されていたゲームエンジンが再統合された。

バージョン2.5系列では、UIの一新、Maya FluidやFume FXのような本格的な流体システムに加え、ほぼ全機能の近代化改修、ブラッシュアップが行われ、2011年4月に初の安定版がリリースされた。

バージョン2.6系列では、2.61において[レンダラ](https://ja.wikipedia.org/wiki/レンダラ "wikilink")であるCyclesやダイナミックペイント、海洋シミュレーション、カメラトラッキング等、他のハイエンドツールにも匹敵する機能を追加し、また、2.63では新しい[メッシュ編集構造であるBMeshの統合もされた](https://ja.wikipedia.org/wiki/ポリゴンメッシュ "wikilink")。

### 国際化と地域化

日本語環境は2.49aまでは貧弱だったが、2.49bにて[2ちゃんねる](https://ja.wikipedia.org/wiki/2ちゃんねる "wikilink")のBlenderスレッドの有志が制作・配布した詳細な日本語翻訳テーブルが公式採用された事で強化された。 その後、バージョン2.5系列で[国際化がなくなり日本語環境での使用はできなくなっていたが](https://ja.wikipedia.org/wiki/国際化と地域化 "wikilink")、GSoC2011にて国際化され、平行して日本の有志により再び日本語対応が行われ、バージョン2.60にて公式に日本語環境が復活した。

## 歴史

Blenderの前身である**Traces**は、オランダの[CG](https://ja.wikipedia.org/wiki/CG "wikilink")スタジオ、NEOGEO社の共同創設者の一人であるトン・ローセンダール (Ton Roosendaal) によって、[AmigaOS](https://ja.wikipedia.org/wiki/AmigaOS "wikilink")向けのレイトレーシングレンダラーとして開発され、後にSGI [IRIX](https://ja.wikipedia.org/wiki/IRIX "wikilink")へと移植された。その後、Tracesのソースコードは書き直されて、Blenderとなった。

[1998年](https://ja.wikipedia.org/wiki/1998年 "wikilink")、トン・ローセンダールはインハウス・ツールとして使用されてきたBlenderの開発・外販を行う為に社を設立した。Windows版も用意され、[ラジオシティ](../Page/ラジオシティ.md "wikilink")機能などを実装した有料版と無料版の二種を展開した。

2001年、NaN社は、Web3Dに向けて、Blender Webプラグインのベータ版をリリースした\[8\]が、セキュリティの問題から頓挫した。[2002年](../Page/2002年.md "wikilink")、[インターネット・バブル](https://ja.wikipedia.org/wiki/インターネット・バブル "wikilink")の崩壊と共にNaN社は[倒産](../Page/倒産.md "wikilink")し、Blenderの[ソースコード](../Page/ソースコード.md "wikilink")は債権者の手に渡ってしまう。しかし開発途上にあったBlenderを手放すことができなかったトン・ローセンダールはを設立するため、"ソースコード解放"を合言葉に大々的な[募金](https://ja.wikipedia.org/wiki/募金 "wikilink")キャンペーンを行い半年で10万[ユーロ](../Page/ユーロ.md "wikilink")を世界中から集結させ、ソースコードを再びその手に取り戻した。

そして現在Blenderは、GPLの元にオープンソースウェアとして開発・無償配布されている。ソースコードのコメントが[オランダ語](../Page/オランダ語.md "wikilink")で書かれている上に、プログラム自体が定石から外れた組み方をしているため、開発を引き次いだ有志は他[OSへの移植などで苦戦したという](../Page/オペレーティングシステム.md "wikilink")。

2008年、UI一新などを目的とするBlender 2.5の開発が開始された。バージョン2.4系は2009年のBlender2.49をもって開発終了し、2011年に2.5系の初の安定板となるバージョン2.57がリリースされた。バージョン2.5系は2018年の2.79bをもって開発終了し、2019年7月にリアルタイムレンダラ「Eevee」やフィジカルベースドレンダリング（PBR）などに対応した2.8系の初の安定版となるバージョン2.80がリリースされた。

2019年9月現在、アセットマネージメントなど次世代3DCGソフトに求められる機能の全てを搭載するのはさらに先になる予定が示されている。2018年2月に「Blender 2.8 Code Quest」が開始され、開発資金を集めるためのグッズの販売や、スポンサーの募集などを行っている。

## 参考画像

## 脚注

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

1.  [Requirements — blender.org](https://www.blender.org/download/requirements/)
2.  [User Stories — blender.org](https://www.blender.org/features/user-stories/)
3.
4.
5.
6.  [Blender 2.66 adds Bullet physics, Dynamic Topology](http://www.cgchannel.com/2013/02/blender-2-66-adds-bullet-physics-dynamic-topology/) CG Channel 2013年2月22日
7.  [Blender Foundation releases Blender 2.82](http://www.cgchannel.com/2020/02/blender-foundation-releases-blender-2-82/) CG Channel 2020年2月14日
8.  [Blender - news - Web Plug-in](http://download.blender.org/documentation/oldsite/oldsite.blender3d.org/202_Blender%20news%20Web%20Plug-in.html) NaN 2001年8月16日
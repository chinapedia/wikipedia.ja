> この記事は[Quest3D](https://ja.wikipedia.org/wiki/Quest3D)から翻訳されています。


**Quest3D**は[3Dエンジンであり](https://ja.wikipedia.org/wiki/ゲームエンジン "wikilink")、その開発プラットフォームである。
主な用途は、建築物、プロダクト、デザインのビジュアライゼーションやコンピューターゲーム、トレーニング用シミュレータ等である。

Mayaや3D Studio Max、[AutoCAD](https://ja.wikipedia.org/wiki/AutoCAD "wikilink")などの3Dソフトウェアや[CAD](../Page/CAD.md "wikilink")ソフトウェアで制作された3Dモデルを利用し、インタラクティブなリアルタイム3Dアプリケーションを作成することができる。 Quest3DはオランダのAct-3D B.V.によって開発されており、2001年9月にリリースされた。

## 開発環境

Quest3Dの最も重要な特徴の一つがそのプログラミングの方法である。

[C++](../Page/C++.md "wikilink")などのプログラム言語による通常のプログラミングとは異なり、Quest3Dではほとんどのプログラミングをグラフィカルに行うことができる。 また、実際にアプリケーションを実行しながらリアルタイムにプログラムを開発することができることも大きな特徴の一つである。 これは通常のプログラム環境とは異なり、コンパイルを必要としないということを意味する。

### 3Dアプリケーションの作成方法

Quest3Dでは、"Channel"と呼ばれるコンポーネントをつなぎ合わせることでアプリケーションを構築していく。

[コンポーネント](https://ja.wikipedia.org/wiki/コンポーネント "wikilink")はツリー状につなぎ合わされ、これが実際のプログラム構造を表す。 エンジンは毎フレームごとにツリー内を駆動し、つなぎ合わされたチャンネルを実行していく。 このことにより、リアルタイムに動作するアプリケーションが構築される。 全てのチャンネルはコンパイル済みのコードで構成されており、アプリケーションの実行にはコンパイルが必要ない。 このため、作成されたアプリケーションのパフォーマンスはコンパイル済みのコードとの差がない。 ただし、仮想機械でアプリケーションが実行された場合はこの限りではない。

### エディタ

Quest3Dはいくつかのエディタから構成される。

エディタにはチャンネルグラフを構築するもの、3Dオブジェクトやアニメーションを編集するもの、HLSLシェーダや[LUAスクリプトを](https://ja.wikipedia.org/wiki/lua "wikilink") 記述するものなどがある。

### パブリッシュ

Quest3Dで作成されたアプリケーションは、[スタンドアローン](https://ja.wikipedia.org/wiki/スタンドアローン "wikilink")の[Windows実行ファイルや](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")[Webページに書き出すことができる](../Page/ウェブサイト.md "wikilink")。 サポートされる[Webブラウザは](../Page/ウェブブラウザ.md "wikilink")[Internet Explorerと](../Page/Internet_Explorer.md "wikilink")[Firefoxである](../Page/Mozilla_Firefox.md "wikilink")。

## 動作環境

Some functionality of the engine requires other hardware specifications.

  - [Windows 2000](../Page/Microsoft_Windows_2000.md "wikilink"), [Windows XP](../Page/Microsoft_Windows_XP.md "wikilink"), [Vista及び](https://ja.wikipedia.org/wiki/Microsoft_Windows_Vista "wikilink")[7共に](../Page/Microsoft_Windows_7.md "wikilink")64Bit OSまたは32Bit OS
  - [DirectX9](https://ja.wikipedia.org/wiki/Direct_X "wikilink")
  - 1GB以上の[RAM](../Page/Random_Access_Memory.md "wikilink")
  - 1Ghz以上のプロセッサ
  - DirectXをサポートした[ビデオカード](../Page/ビデオカード.md "wikilink")
  - 高度な機能ではShader Model 3.0をサポートするグラフィックカード
  - 500MB以上空きのある[ハードディスク](https://ja.wikipedia.org/wiki/ハードディスクドライブ "wikilink")

## ライセンス

商用ライセンスの他、教育用ライセンスがある。

## 用途

コンピュータゲーム、建築ビジュアライゼーション、シリアスゲーム、シミュレーション、TV番組や映画

## ゲームタイトル

  - [Audiosurf](https://ja.wikipedia.org/wiki/:en:Audiosurf "wikilink") by Invisible Handlebar.
  - [Ship simulator](https://ja.wikipedia.org/wiki/:en:Ship_simulator "wikilink") by [VSTEP](https://ja.wikipedia.org/wiki/:en:VSTEP "wikilink")
  - [Leo der Haze](http://www.leo-dasspiel.at) by [Ovos real-time 3D](http://www.ovos.at)
  - [Chicken Football](http://www.chickenfootball.com) by [Paladin Studios](http://www.paladinstudios.com)
  - [The Endless Forest](http://endlessforest.org/community) by [Tale of Tales](http://tale-of-tales.com)
  - [Twinners](http://www.twinners.com) [Spanish demo](http://nl.youtube.com/watch?v=sgrmk-ftpOU)

## リファレンス

  - [DevMaster.net](http://www.devmaster.net/engines/list.php?search_id=327a4470492779db51b5319eca124643) Quest3D specifications
  - [Gamasutra](http://www.gamasutra.com/php-bin/news_index.php?story=16549) "Rapid gameplay iterations are crucial to me, so I use Quest3D for everything else.", [Dylan Fitterer](https://ja.wikipedia.org/wiki/:en:Dylan_Fitterer "wikilink") インタビュー in "The road to IGF"

## 外部リンク

  - [Quest3D公式サイト](http://www.quest3d.com)
  - [Quest3Dブログ](http://www.rgb255.nl/questlog)

[Category:ゲームエンジン](https://ja.wikipedia.org/wiki/Category:ゲームエンジン "wikilink") [Category:Windowsのソフトウェア](https://ja.wikipedia.org/wiki/Category:Windowsのソフトウェア "wikilink")
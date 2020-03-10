> この記事は[PhysX](https://ja.wikipedia.org/wiki/PhysX)から翻訳されています。


**PhysX**（フィジックス/フィジクス\[1\]）とは[NVIDIA](https://ja.wikipedia.org/wiki/NVIDIA "wikilink")が開発・提供している、リアルタイムの[物理演算エンジン](https://ja.wikipedia.org/wiki/物理演算エンジン "wikilink")。

## 概要

ソフトウェアがPhysXの[ハードウェアアクセラレーション](../Page/ハードウェアアクセラレーション.md "wikilink")に対応している場合、[CUDA](https://ja.wikipedia.org/wiki/CUDA "wikilink")が使用可能な[GeForce](https://ja.wikipedia.org/wiki/GeForce "wikilink")（[8シリーズ以降の製品](https://ja.wikipedia.org/wiki/NVIDIA_GeForce#GeForce_8_Series "wikilink")）のうち、32以上のコア、256MB以上のグラフィックスメモリを搭載する製品でハードウェアアクセラレートが可能である\[2\]。

PhysXのハードウェアアクセラレーションは、日夜進化を続ける[コンピュータゲーム](../Page/コンピュータゲーム.md "wikilink")における 物理演算を[CPU](../Page/CPU.md "wikilink")から肩代わりする事で動作スピードの上昇を目指したものである。汎用プロセッサである[CPU](../Page/CPU.md "wikilink")のパフォーマンスでは不可能に近い「爆発によって飛び散った破片を毎回ランダムに演算する」等の複雑かつ高負荷な描写を、事前作成済み動画の読み出しなどではなく、実際にその場で演算してリアルタイムに描写することが可能になるとされている。対抗とされる物理演算システムとしては[Havok](https://ja.wikipedia.org/wiki/Havok "wikilink")が挙げられる。

PhysXは様々なプラットフォームで500以上のゲームに使われている\[3\]。

## 歴史

開発元は米[カリフォルニア州](../Page/カリフォルニア州.md "wikilink")に本拠を置いていた社。[2008年](https://ja.wikipedia.org/wiki/2008年 "wikilink")[2月4日](../Page/2月4日.md "wikilink")に、[NVIDIA GeForceシリーズを開発する](../Page/NVIDIA_GeForce.md "wikilink")[NVIDIA](https://ja.wikipedia.org/wiki/NVIDIA "wikilink")がAgeiaを買収し、PhysXとGeForceシリーズの統合が発表された\[4\]。NVIDIAによる買収後は、専用チップおよび専用ボードは生産されていない。

PhysX SDK 2.8.3から(PPU)のサポートが打ち切られた\[5\]。

## 対応プラットフォーム

PhysXは以下のプラットフォーム上で動作する\[6\]。

  - PC ([Windows](https://ja.wikipedia.org/wiki/Windows "wikilink")/[Linux](../Page/Linux.md "wikilink")/[macOS](https://ja.wikipedia.org/wiki/macOS "wikilink"))
  - [PlayStation 3](https://ja.wikipedia.org/wiki/PlayStation_3 "wikilink")
  - [PlayStation 4](https://ja.wikipedia.org/wiki/PlayStation_4 "wikilink")
  - [Xbox 360](../Page/Xbox_360.md "wikilink")
  - [Xbox One](https://ja.wikipedia.org/wiki/Xbox_One "wikilink")
  - [Wii](https://ja.wikipedia.org/wiki/Wii "wikilink")
  - [Android](../Page/Android.md "wikilink")
  - [iOS](https://ja.wikipedia.org/wiki/iOS_\(アップル\) "wikilink")

いずれのプラットフォーム用SDKも無料で配布されている。これらのうち、PC用のSDKは[NVIDIA](https://ja.wikipedia.org/wiki/NVIDIA "wikilink")社のPhysX SDK ダウンロードページ\[7\]より直接入手する事ができる。[NVIDIA](https://ja.wikipedia.org/wiki/NVIDIA "wikilink")社スタッフによるサポート及び開発支援ツールが有償で提供されているが、これらを利用しない限りは商用利用を含めて無料である。

PhysXは[Unreal Engineや](../Page/Unreal_Engine.md "wikilink")[Unity (ゲームエンジン)にも統合されている](https://ja.wikipedia.org/wiki/Unity_\(ゲームエンジン\) "wikilink")。

## PhysXの機能

PhysXでは、以下の機能がサポートされている。

  - 剛体物理
      - 衝突判定
      - 各種関節
      - [ラグドール](https://ja.wikipedia.org/wiki/ラグドール物理 "wikilink")
      - 摩擦力の考慮
      - 衝突の検知
      - オブジェクトをグループ化し、衝突判定のON・OFF切り替え
      - 1軸方向のみに物理作用を限定
      - 接触通知
  - 先進的なキャラクタコントロール
  - 乗り物のための動力学
  - [マルチスレッド](https://ja.wikipedia.org/wiki/マルチスレッド "wikilink")・[マルチプラットフォーム](https://ja.wikipedia.org/wiki/マルチプラットフォーム "wikilink")
  - 流体[シミュレーション](../Page/シミュレーション.md "wikilink")
  - 布[シミュレーション](../Page/シミュレーション.md "wikilink")
  - 軟体の表現
  - フォースフィールドの表現

## 問題点と今後

PhysXの発表当初、以下のような問題があった。

  - 導入しても対応しているゲームの挙動に影響があるだけでPC自体のパフォーマンス向上には関係ないこと
  - ゲームが対応していなければPhysXチップの導入には意味が無いこと
  - ゲームはPhysXに「対応している」以上のことができないこと

たとえば、PhysXによって爆発の破片によるダメージ判定なども出来るが、それはネット対戦などにおいては全てのプレーヤーがPhysXを導入していなければ対応が難しい。(ゲームソフトとは別に物理演算ボードを購入する必要があった。)

  - 限られたユーザーしか利用可能でないため、デベロッパは安易にPhsyXを**必須動作条件**に入れることができない。

これらの問題点はNVIDIAがAGEIAを買収した事により一定の解決を見る。ただしそれによって新たなデメリットも生じた。

  - メリット
      - 広いシェアを持つGeForceシリーズのグラフィックボードで動作するようになったため、利用可能ユーザーが爆発的に増加した。
      - 専用ボードを別途購入する必要がなくなった。
          - 古いビデオカードの更新、再生支援や[HDCP](https://ja.wikipedia.org/wiki/HDCP "wikilink")を利用して[ブルーレイや](../Page/Blu-ray_Disc.md "wikilink")[地デジ](https://ja.wikipedia.org/wiki/地デジ "wikilink")を楽しむといった別の用途で購入したとしてもPhysX対応となる。
  - デメリット
      - 本来、グラフィック描画に用いられるはずのユニファイドシェーダーの一部を物理演算に割く事になるため、結果としてグラフィックパフォーマンスが低下する。また、NVIDIA社が提唱するPhysXエフェクトの採用はそのまま破片、水滴など描画対象の爆発的増殖と一体である。その為、物理効果が現れれば同時に膨大な描画負荷やリソース消費が発生する事になり、やはりパフォーマンスは大きく低下してしまう。以上の点から、現実問題として、単独VGAでのPhysX利用はフレームレート維持の観点から実用的ではない（演算専用のサブグラフィックスデバイスを別途用意しなければならない）。これはPhysX本格採用タイトルのCryostasis等で特に顕著である。
      - AGEIA買収当時においても、NVIDIA社と[AMD社の関係上](https://ja.wikipedia.org/wiki/アドバンスト・マイクロ・デバイセズ "wikilink")、またPhysXとHavokの関係上[AMD RadeonのようなAMD製GPUに対応する可能性は著しく低かったが](https://ja.wikipedia.org/wiki/AMD_Radeon "wikilink")、AGEIA社のPPU、或いは8X00以降のNVIDIA製VGAを別途搭載する事により、ハードウェアPhysXをAMD社製VGA搭載機でも利用する事が出来た。だが、同社がリリースした186番台以降のデバイスドライバーは、AMD社製グラフィックシステムを検知すると、たとえPhysX対応ハードウェアがPCにインストールされていても、それらの物理演算機能を強制的に停止させてしまう[1](http://www.guru3d.com/news/nvidia-disables-physx-when-ati-card-is-present/)。これにはAGEIA社のPPUも含まれる。
  - 2009年10月現在、MODドライバーや非公認パッチによって、AMD系VGA搭載システムでもPhysXの利用は変則的にではあるものの、可能となっている。[2](http://www.hardforum.com/showthread.php?t=1456964)

しかし、AMDはIntel社の[Havok](https://ja.wikipedia.org/wiki/Havok "wikilink")と提携し[3](http://news.cnet.com/8301-10784_3-9967088-7.html)、なおかつ独自にオープンソースベースの物理エンジン[Bullet Physicsにも着手している為](https://ja.wikipedia.org/wiki/Bullet "wikilink")[4](http://www.amd.com/us/press-releases/Pages/amd-announces-new-levels-of-realism-2009sept30.aspx)、物理エンジンにおけるAMDとNVIDIAの歩み寄りは、既に非現実的なものとなりつつある。

[:en:List of games with hardware-accelerated PhysX supportのリストのとおり](https://ja.wikipedia.org/wiki/:en:List_of_games_with_hardware-accelerated_PhysX_support "wikilink")、ハードウェアによるPhysXアクセラレーションに対応したゲームタイトルの数はソフトウェアによるPhysX利用タイトルの数に比べると限定的である。

## 脚注

## 関連項目

  - [NVIDIA GeForce](../Page/NVIDIA_GeForce.md "wikilink")
  - [Graphics Processing Unit](../Page/Graphics_Processing_Unit.md "wikilink")
  - [GPGPU](https://ja.wikipedia.org/wiki/GPGPU "wikilink")

## 外部リンク

  - [ゲーマー向けPhysX公式サイト](http://www.geforce.com/hardware/technology/physx)（英語）

  - [開発者向けPhysX公式サイト](http://developer.nvidia.com/physx-games)（英語）

  - （英語）

  - （英語）

  - （英語）

  - [Projects using PhysX SDK](http://physxinfo.com/)（英語）

  -
[Category:ゲームエンジン](https://ja.wikipedia.org/wiki/Category:ゲームエンジン "wikilink")

1.  [ASCII.jp：アキバで恥をかかないための最新パーツ事情2009【ビデオカード編】 (4/7)｜アキバで恥をかかないための最新パーツ事情2009](http://ascii.jp/elem/000/000/414/414317/index-4.html)
2.
3.
4.  [NVIDIA，「PhysX」のAGEIA Technologiesを買収](http://www.4gamer.net/games/022/G002233/20080205001/)
5.
6.  [PhysX SDK | NVIDIA Developer](https://developer.nvidia.com/physx-sdk)
7.  [PhysX SDK Downloads，PhysX SDK ダウンロードページ](http://developer.nvidia.com/object/physx_downloads.html)
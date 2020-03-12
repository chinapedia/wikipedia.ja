> この記事は[AMD Catalyst](https://ja.wikipedia.org/wiki/AMD_Catalyst)から翻訳されています。


**AMD Radeon Software** (エーエムディー レイディオン ソフトウェア) は、[AMD](https://ja.wikipedia.org/wiki/アドバンスト・マイクロ・デバイセズ "wikilink")（旧[ATI](../Page/ATI_Technologies.md "wikilink")）の[GPUである](../Page/Graphics_Processing_Unit.md "wikilink")[AMD Radeon](../Page/AMD_Radeon.md "wikilink") (旧ATI Radeon) シリーズ、[AMD FirePro](https://ja.wikipedia.org/wiki/AMD_FirePro "wikilink")/AMD Radeon Pro (旧ATI FireGLおよび旧ATI FirePro) シリーズ用の[ドライバーソフトと](../Page/デバイスドライバ.md "wikilink")[ユーティリティ](https://ja.wikipedia.org/wiki/ユーティリティ "wikilink")ソフトの集合体で、[Microsoft Windowsと](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")[Linux](../Page/Linux.md "wikilink")に対応している。また、[AMD APUのグラフィックスドライバーとしての役割も果たしている](https://ja.wikipedia.org/wiki/AMD_Accelerated_Processing_Unit "wikilink")。旧称は**ATI Catalyst**/**AMD Catalyst** (カタリスト)。

提供されるソフトウェアのバージョン番号は「(公開された年の下1桁、2010からは下2桁).(公開された月)」となっている。ただし、これらはドライバーの内部バージョンとは異なる。

FirePro/Radeon Proシリーズ用のドライバーは、ワークステーション向けのドライバーであり、[OpenGL](../Page/OpenGL.md "wikilink")や各種プロフェッショナル向けグラフィックス[アプリケーションソフトウェア](../Page/アプリケーションソフトウェア.md "wikilink")への最適化がなされている\[1\]。

## Radeon Software/FirePro Software

2015年11月にはCatalystの後継として、品質の向上やユーザーインターフェイスを刷新した新たなソフトウェア「**Radeon Software** Crimson Edition」（通称Crimson）がリリースされた。Crimsonは2015年から2016年にかけてのメジャーバージョン名となる\[2\]。2017年には別の「赤」にちなんだメジャーバージョン名が付けられることが予定されている\[3\]。なお、Crimsonが対応するハードウェアは[Graphics Core Next](https://ja.wikipedia.org/wiki/Graphics_Core_Next "wikilink") (GCN) アーキテクチャを採用した製品のみとなることが予定されていたが\[4\]、その後非GCNの旧世代GPUに対応するCrimsonも別途リリースされた\[5\]。

バージョン16.3からは、ローレベルグラフィックスAPIである[Vulkanにも対応している](https://ja.wikipedia.org/wiki/Vulkan_\(API\) "wikilink")\[6\]。

なおFireProのドライバースイートに関しては、かつて「**Catalyst Pro**」というブランド名が使用されていた\[7\]が、バージョン16.Q4からは、Catalyst Proの後継として「**FirePro and Radeon Pro Software**」という名称となった。

## Catalystに含まれるもの

  - Catalystディスプレイドライバー ([Direct3D](../Page/Direct3D.md "wikilink")/[OpenGL](../Page/OpenGL.md "wikilink")/[Mantle](https://ja.wikipedia.org/wiki/Mantle_\(API\) "wikilink"))
  - [OpenCL](../Page/OpenCL.md "wikilink")ドライバー
  - [DisplayPort](../Page/DisplayPort.md "wikilink")/[HDMI](https://ja.wikipedia.org/wiki/HDMI "wikilink")用オーディオドライバー
  - Catalyst Control Center（カタリスト・コントロール・センター、略称CCC）- 動作には[.NET Frameworkの導入が必要](https://ja.wikipedia.org/wiki/.NET_Framework "wikilink")\[8\]
  - AVIVO - [HDのGPU支援プログラム](https://ja.wikipedia.org/wiki/高精細度テレビジョン放送 "wikilink")。
  - Hydravision （ハイドラビジョン）- マルチディスプレイ用ドライバソフトウェア
  - Multi-Media Center (MMC) and Remote Wonder (RW)

## 3D設定

記述のドライバはデスクトップ版Catalyst 10.6とする。なお、AMD690G/780G/880Gなどの[チップセット](../Page/チップセット.md "wikilink")統合型グラフィックスでは性能的な制約から一部の3D設定が適用出来ない様になっているが基本的な設定項目に変わりはない。

全体の設定として、パフォーマンス - 画質の間で調整可能であり、レベルは「最適パフォーマンス」「ハイパフォーマンス」「バランス」「パフォーマンス」「高画質」「最適画質」の6通りあり、左に調整するほど画質が荒く高速に描画され、右に調整するほど画質が向上し描画負荷が増大する。

### アンチエイリアシング

フィルターレベルは「Box」「Narrow-tent」「Wide-tent」「Edge-detect」の4つがあり、倍率を上昇させることで画質が向上するが相応して描写負荷が増大する。

### 適応アンチエイリアシング

  - 「スーパーサンプリング」は軽負荷＋中画質の「パフォーマンス」と、高負荷＋高画質の「画質」設定がある。
  - 「マルチサンプリング」は「滑らか」「鮮明」の間に調整箇所が4つあり、左に調整する程軽負荷＋中画質になり、右に調整する程高負荷＋高画質になる。

### 異方性フィルタリング

1ピクセルごとのサンプル数を2x - 16xの間で調整出来、値が大きい程高画質になり奥行き感が増すが、高負荷になる。

### Catalyst A.I

ドライバがサポートするアプリケーションが起動した時に、それに最適化された動作設定を呼び出すので、無効化されているとAAが効かないケースもある。ただし古いゲームでは無効化しないと動作不安定になる事もある。

### ミップマップ詳細レベル

「パフォーマンス」と「画質」の間に調整箇所が4つあり、左に調整する程軽負荷＋中画質になり、右に調整する程高負荷＋高画質になる。

### 垂直リフレシュを待機

垂直リフレッシュは描画速度に関わるもので一般的にはV-Sync（垂直同期信号）と呼ばれる。「オフ」設定にするとフレームレートの上限を解除し高速に描画させる。ただしアプリケーション側で設定出来る場合は無効化される事がある。基本的には「アプリケーション側で指定しない限りオフ」が推奨される。設定によってはアプリケーションデザインに意図しない高速化（オーバーラップ）やパフォーマンスの低下を招く。

## AVIVO ビデオコンバータ

動画を高速に別の形式に変換を行うソフトウェア。Catalyst Control Centerの基本モード内から動作することができる。詳細モードからは動作させることはできない。変換処理の一部に[GPUアクセラレーション技術を用いることにより高速な](https://ja.wikipedia.org/wiki/GPGPU "wikilink")[エンコード](../Page/エンコード.md "wikilink")を可能にしている。以下の形式への変換に対応する。おおまかな画質設定([ビットレート](../Page/ビットレート.md "wikilink"))のみ可能であり、ユーザーによる細かい出力設定はサポートされていない。また、1パスのエンコードのみが可能であり、複数パスエンコードは行えない。

  - [MPEG-1](../Page/MPEG-1.md "wikilink")
  - [MPEG-2](../Page/MPEG-2.md "wikilink")
  - [MPEG-4](../Page/MPEG-4.md "wikilink") ([DivX](https://ja.wikipedia.org/wiki/DivX "wikilink")互換)
  - [Windows Media Video](../Page/Windows_Media_Video.md "wikilink")

以下は特定機種向けの設定のため、画像サイズの変換も行われる。括弧内は (形式, 横解像度x縦解像度) の順。

  - [iPod](https://ja.wikipedia.org/wiki/iPod "wikilink")ビデオ ([H.264](../Page/H.264.md "wikilink"), 320x240)
  - [Portable Media Center](../Page/Windows_Media_Center.md "wikilink") ([WMV9](https://ja.wikipedia.org/wiki/WMV9 "wikilink"), 320x240)
  - [DVD](../Page/DVD.md "wikilink") (MPEG-2, 720x480)
  - [ビデオCD](../Page/ビデオCD.md "wikilink") (MPEG-1, 352x240)
  - [スーパービデオCD](../Page/スーパービデオCD.md "wikilink") (MPEG-2, 480x480)
  - [Sony ポータブルゲームデバイス](../Page/PlayStation_Portable.md "wikilink") (MPEG-4, 320x240)

## AVIVO

[HDのGPU支援プログラムであり](https://ja.wikipedia.org/wiki/高精細度 "wikilink")、動画のデコード、エンコード、解像度変更支援やインターレース解除機能などで構成される。一部機能はハードウェア固定機能を用いる。[DirectShow](https://ja.wikipedia.org/wiki/DirectShow "wikilink")フィルタとして提供されている。これらは一部のみ利用することも可能であり、これらの組み合わせに限定されない。

### 主なフィルタ

  - ATI MPEG Video Decoder (MPEGまたはWindowsMediaVideo形式の映像デコード)
  - ATI MPEG Video Encoder (映像エンコード)
  - ATI MPEG Audeo Decoder (MPEGオーディオ形式の音声デコード)
  - ATI MPEG Audio Encoder (音声エンコード)
  - ATI Video Scaler Filter (映像サイズ変換)

対応ソフトウェアまたはAVIVOビデオコンバータを用いることで動作が可能。

## AMD OverDrive

オーバークロック機能として**AMD OverDrive**\[9\] (旧称ATI Overdrive) を搭載している\[10\]。鍵マークのロックアイコンをクリックし、ロック解除後に操作可能となるが、利用は自己責任となる\[11\]。カスタムクロックをテストして最適なオーバークロックの値を抽出する機能を搭載しており、手軽にGPUクロック、メモリクロックを上げることができる。これにより、グラフィックスカードに搭載されたGPUのパフォーマンスを引き上げることができるとされる。

グラフィックスカードに内蔵された温度センサーによりGPUの温度を表示させる機能を搭載しており、必要に応じてファンの回転速度を手動調整することも可能（カードのモデルによって異なる）。また、GPUの温度が極度に上昇すると安全な温度まで自動的にクロック速度を落とし、破損の危険を回避する機能も搭載している。プロファイルマネージャを使い、3Dアプリケーションの実行時のみ、AMD OverDriveが動作する設定にすることも可能とされる。

AMD OverDriveの後継として、**Radeon WattMan**と呼ばれる電力管理ユーティリティがリリースされた\[12\]。WattManはRadeon RX 400シリーズと互換性がある\[13\]。

## Switchable Graphics

メーカー製ノートPCにはCPU内蔵GPUと（AMD製の）単体GPUを切り替えることのできるものが存在する\[14\]。Catalyst Control Centerには、切り替えの設定を変更できるページが設けられており\[15\]、アプリケーションごとのGPU選択や、外部電源接続／非接続時のGPU選択を設定することが可能である。

## CrossFire/CrossFireX

AMD CrossFire/[CrossFireX](../Page/CrossFireX.md "wikilink")は、複数のGPUを協調動作させて分散レンダリング処理を行なう技術である。Catalyst Control Centerで詳細設定が可能となっている\[16\]。

## 脚注

## 関連項目

  - [アドバンスト・マイクロ・デバイセズ](https://ja.wikipedia.org/wiki/アドバンスト・マイクロ・デバイセズ "wikilink")
  - [AMD Radeon](../Page/AMD_Radeon.md "wikilink")
  - [AMD FirePro](https://ja.wikipedia.org/wiki/AMD_FirePro "wikilink")
  - [CrossFireX](../Page/CrossFireX.md "wikilink")
  - [Direct3D](../Page/Direct3D.md "wikilink")
  - [OpenGL](../Page/OpenGL.md "wikilink")
  - [OpenCL](../Page/OpenCL.md "wikilink")
  - [Mantle (API)](https://ja.wikipedia.org/wiki/Mantle_\(API\) "wikilink")
  - [Vulkan (API)](https://ja.wikipedia.org/wiki/Vulkan_\(API\) "wikilink")

## 外部リンク

  - [AMD Radeon Software Adrenalin Edition](https://www.amd.com/ja/technologies/radeon-software)
  - [AMD Radeon Software Adrenalin Edition](https://www.amd.com/en/technologies/radeon-software)
  - [AMD Radeon Pro Software Adrenalin Edition for Enterprise](https://www.amd.com/ja/technologies/radeon-pro-software)
  - [AMD Radeon Pro Software Adrenalin Edition for Enterprise](https://www.amd.com/en/technologies/radeon-pro-software)
  - [AMDドライバーとサポート](https://www.amd.com/ja/support)
  - [AMD Drivers and Support](https://www.amd.com/en/support)
  - [デバイスドライバダウンロード(4Gamer.net)](http://www.4gamer.net/games/017/G001762/FC20110422001/)
  - [一問一答「ATI Catalyst」。AMDのドライバ担当者にいろいろ聞いてみた(4Gamer.net)](http://www.4gamer.net/games/022/G002212/20080905042/)

[Category:グラフィックカード](https://ja.wikipedia.org/wiki/Category:グラフィックカード "wikilink") [Category:アドバンスト・マイクロ・デバイセズ](https://ja.wikipedia.org/wiki/Category:アドバンスト・マイクロ・デバイセズ "wikilink") [Category:デバイスドライバ](https://ja.wikipedia.org/wiki/Category:デバイスドライバ "wikilink")

1.  [Professional Graphicsの市場を積極的に狙いたいAMD - FireProシリーズに関する説明会を開催 (1) FireProシリーズをざっくりと紹介 | マイナビニュース](http://news.mynavi.jp/articles/2013/05/17/firepro/)
2.  [「Radeon Software」ついに公開。新世代グラフィックスドライバで何が変わるのか，AMDの担当者が語る - 4Gamer.net](http://www.4gamer.net/games/022/G002212/20151124113/)
3.  [ASCII.jp：AMD、次世代GPUドライバー「Radeon Software」を配信](http://ascii.jp/elem/000/001/082/1082286/)
4.  [「Radeon Software Crimson Edition 15.11」の更新内容まとめ。一部に謎が残るも，文句なしに大規模アップデートだ - 4Gamer.net](http://www.4gamer.net/games/022/G002212/20151125018/)
5.  [「Radeon Software Crimson Edition 16.1 Hotfix」が，大量のバグ修正を含んで登場 - 4Gamer.net](http://www.4gamer.net/games/022/G002212/20160108039/)
6.  [AMD Radeon Software Crimson Edition 16.3 Release Notes](http://support.amd.com/en-us/kb-articles/Pages/AMD_Radeon_Software_Crimson_Edition_16.3.aspx)
7.  [Previous ATI FireGL™, AMD FirePro™, AMD FireMV™ Unified Display Drivers](http://support.amd.com/en-us/download/workstation/previous?os=Windows%2010%20-%2064)
8.  Radeon Softwareにて、CCCの後継として導入された「Radeon Settings」はネイティブコードにより実装されており、.NET Frameworkは不要となっている。
9.  [AMD OverDrive™ Technology](http://www.amd.com/en-us/innovations/software-technologies/technologies-gaming/over-drive)
10. [自作PCをよくするワザ、教えます(6) ～ビデオカード編～ - AKIBA PC Hotline\!](http://akiba-pc.watch.impress.co.jp/docs/dosv/20141111_675358.html)
11. [ASCII.jp：ビデオカードもオーバークロックできる！ (5/7)｜Windows 7で行なうオーバークロック](http://ascii.jp/elem/000/000/485/485543/index-5.html)
12. [ASCII.jp：「Radeon RX 480」は迷えるゲーマーを導く極星となるか？ (4/8)｜最新パーツ性能チェック](http://ascii.jp/elem/000/001/185/1185460/index-4.html)
13. [Radeon WattMan](http://www.amd.com/ja-jp/innovations/software-technologies/technologies-gaming/radeon-wattman)
14. [HP ノートブック PC - スイッチャブル・グラフィックスまたはデュアルGPUの概要 | HP® Customer Support](http://support.hp.com/us-en/document/c04094179)
15. [Laptop Support](http://support.amd.com/en-us/kb-articles/Pages/LaptopsFAQ.aspx)
16. [AMD CrossFire™ FAQ](http://support.amd.com/en-us/kb-articles/pages/amdcrossfirefaq.aspx)
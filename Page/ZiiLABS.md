> この記事は[ZiiLABS](https://ja.wikipedia.org/wiki/ZiiLABS)から翻訳されています。


[thumb](https://ja.wikipedia.org/wiki/ファイル:3dlabs_permedia_2v.jpg "wikilink") **ZiiLABS**は[シンガポール](https://ja.wikipedia.org/wiki/シンガポール "wikilink")の[コンピュータ](../Page/コンピュータ.md "wikilink")周辺機器ハードウェアメーカー。

[アメリカで](https://ja.wikipedia.org/wiki/アメリカ合衆国 "wikilink")[GPU及び](../Page/Graphics_Processing_Unit.md "wikilink")[ビデオカード](../Page/ビデオカード.md "wikilink")を生産していたが、[2006年](https://ja.wikipedia.org/wiki/2006年 "wikilink")にGPUから撤退。

[2009年](../Page/2009年.md "wikilink")に**3Dlabs**から社名を変え、現在は主にモバイル向けSoCの製造を行なっている。

## 概要

3Dlabsは[OpenGL](../Page/OpenGL.md "wikilink")に特化したビデオカードを製造していたハードウェアメーカーであり、[1990年代](../Page/1990年代.md "wikilink")にはプロフェッショナル向けの**GLINT**シリーズとコンシューマ向けの**Permedia**シリーズを、また[2000年代](../Page/2000年代.md "wikilink")以降は**Wildcat**シリーズを展開していた。

同社のGPUはOpenGLに関しては非常に高い処理能力を発揮するが、[DirectXの処理はあまり得意でないため](https://ja.wikipedia.org/wiki/Microsoft_DirectX "wikilink")、ゲームなどには向かず、3Dアニメーションの制作など、OpenGLを利用した専門性の高い分野を得意としていた。一般に販売されているビデオカードの中でもとりわけ高価な事や、消費電力の大きさなど、様々な観点から見ても、プロフェッショナルに向けた製品群であった。

3DLabsはOpenGLの[API策定に関与しており](../Page/アプリケーションプログラミングインタフェース.md "wikilink")、OpenGLのAPI策定に歩調を合わせて製品をリリースしていた。そのため、特定ベンダが売り込んだDirectXの新規APIファンクションのサポートなどは、次の世代のGPUでサポートされることが多く、また、演算・レンダリング精度を重視しているために、マルチメディア処理のパフォーマンスや、あるいはゲーム固有のバグを吸収するためのドライバ最適化などを原則行わなかった。そのためにDirectXに弱いという評価をなされることが多かった\[1\]が、そもそもDirectXの普及がまだ途上であった1990年代中頃にはそれほど問題とされず、特に[1997年](https://ja.wikipedia.org/wiki/1997年 "wikilink")に発売された**Permedia2**はその高いピクセル描画性能で大ヒットとなった。

しかしDirectXが急速に浸透する1990年代後半以降、DirectXの最新APIへの対応の遅れや[Direct3D](https://ja.wikipedia.org/wiki/Direct3D "wikilink")の実行性能の遅さのために、急速にコンシューマでのシェアを低下させた。それでもOpenGLが重視されるプロフェッショナル向けGPUでは高いシェアを誇っていたが、2000年代に入るとコンシューマ向けGPUで性能競争を激化させた[NVIDIA](https://ja.wikipedia.org/wiki/NVIDIA "wikilink")と[ATIがプロフェッショナル向けGPUのシェアをも食うに至って](https://ja.wikipedia.org/wiki/ATI_Technologies "wikilink")、業績が悪化。

[2002年](../Page/2002年.md "wikilink")[3月](https://ja.wikipedia.org/wiki/3月 "wikilink")に[クリエイティブテクノロジー](https://ja.wikipedia.org/wiki/クリエイティブテクノロジー "wikilink")によって買収された。そして2006年[2月24日](https://ja.wikipedia.org/wiki/2月24日 "wikilink")、親会社のクリエイティブテクノロジーがプロフェッショナルワークステーショングラフィックス事業から撤退させると発表し、メディアプロセッサの開発に転換した。

2009年には**ZiiLABS**と社名を変え、自社のGPUを[ARMプロセッサと組み合わせたモバイル向けSoCである](https://ja.wikipedia.org/wiki/ARMアーキテクチャ "wikilink")「ZMS」の開発を行なっており、主にクリエイティブ製品に採用されている。

[2012年](../Page/2012年.md "wikilink")[11月](../Page/11月.md "wikilink")に開発チームが[インテル](https://ja.wikipedia.org/wiki/インテル "wikilink")に譲渡された。

## ビデオチップ

### Permedia

[thumb](https://ja.wikipedia.org/wiki/ファイル:Diamond_Multimedia_FireGL1000_PCI.jpg "wikilink"))\]\] **Permedia**は3Dlabsがコンシューマ向けとして販売していたビデオチップのシリーズ。PermediaおよびPremediaNTはOpenGLの[CAD](../Page/CAD.md "wikilink") API専用のジオメトリエンジンとして**GLINT Delta**を搭載した。コンシューマ向けとされているが、[Windows 95に対応しなかった](../Page/Microsoft_Windows_95.md "wikilink")。

### Permedia2

[thumb](https://ja.wikipedia.org/wiki/ファイル:3dlabs_oxygen_acx_permedia_2_pci_card.jpg "wikilink") **Permedia2**はPermediaで別チップで構成されていたジオメトリエンジンを統合しワンチップ化を行った。これはNVIDIAなど他社より先んじていた。128ビットグラフィックコアと64ビットメモリバスを持ち、メモリは8MBまでのSGRAMをサポートする。[インタフェースは](../Page/インタフェース_\(情報技術\).md "wikilink")[AGP 1xまたは](https://ja.wikipedia.org/wiki/AGP "wikilink")[PCI](../Page/Peripheral_Component_Interconnect.md "wikilink")。[RAMDAC](https://ja.wikipedia.org/wiki/RAMDAC "wikilink")を統合するが、外部RAMDACもサポートする。 このPermedia2は多くベンダーにチップの供給を行っており、1997年には多くのベンダーがOpenGLとDirectXのサポートと銘打ってビデオカードを発売した。後期にはマイナーチェンジ版の**Permedia2V**が発売されている。 このPermedia2は、同社がコンシューマ市場で成功した唯一の製品である。

OpenGLは、バージョン1.2以前をサポート。 DirectXは、DirectX5以前のファンクションは概ね正常に動作する。ドライバは、DirectX6までサポートする。テクスチャのアルファブレンディングの仕様により、ビルボードの透過が正しく扱えないことがある。

### Permedia3・GLINT R3

[thumb](https://ja.wikipedia.org/wiki/ファイル:3dlabs_oxygen_vx1_agp4x.jpg "wikilink") **Permedia3**はPermedia2後継のコンシューマ向け製品として、**GLINT R3**はプロフェッショナルワークステーション向け製品として[1999年](../Page/1999年.md "wikilink")に発表された。ほぼ同じチップであるが、Permedia3はドライバのマルチスレッド非対応化がされている。 128ビットのメモリバスで接続されるSGRAMを32MBまでサポートする。インタフェースはAGP 2xまたは[PCI](../Page/Peripheral_Component_Interconnect.md "wikilink")。後にAGP 4x対応版が発売された。[MCによる動画再生支援機能に対応する](https://ja.wikipedia.org/wiki/フレーム間予測#動き補償 "wikilink")。 機能的にはコンパニオンチップとして**GLINT G1**ジオメトリプロセッサをサポートし、対応アプリケーションでは[座標変換](https://ja.wikipedia.org/wiki/座標変換 "wikilink")処理および[光源](../Page/光源.md "wikilink")処理を低負荷で高速に実行できる。 また、メインメモリ上にテクスチャを展開する**Virtual Textures**機能に対応しており、搭載する[VRAM](../Page/VRAM.md "wikilink")以上の容量のテクスチャを扱える。

OpenGLは、1.3以前をサポート。 DirectXは、DirectX6以前のファンクションは概ね対応する。 ドライバは、DirectX8.1まで対応。 ただし、DX7のHWT\&L、DX8でのHWT\&Lとプログラマブルシェーダは、いずれもサポートしない（GLINT G1は、DirectXを非サポート）。

  - 主な搭載製品

:\* Permedia3 Create\!

:\* Oxygen VX1

:\* Oxygen GVX1

### P10

  - 主な搭載製品

:\* WildCat 4

### P9

  - 主な搭載製品

:\* WildCat VP560

## 脚注

<references />

## 関連項目

  - [OpenGL](../Page/OpenGL.md "wikilink")
  - [CAD](../Page/CAD.md "wikilink")
  - [GPU](../Page/Graphics_Processing_Unit.md "wikilink")
  - [ビデオカード](../Page/ビデオカード.md "wikilink")

## 外部リンク

  -
[Category:コンピュータ周辺機器企業](https://ja.wikipedia.org/wiki/Category:コンピュータ周辺機器企業 "wikilink") [Category:シンガポールの企業](https://ja.wikipedia.org/wiki/Category:シンガポールの企業 "wikilink")

1.  なおDirectX系とされるGPUにしても、初期の製品を除けば、DirectXのAPI仕様を再現できる汎用DSP/プロセサであり、APIそのものを直接GPUで実行しているわけではない。そのため、OpenGL向きのGPUだからハードウェア的にDirectXに弱い、というのは厳密には正しくない。
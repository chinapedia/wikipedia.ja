> この記事は[VDP](https://ja.wikipedia.org/wiki/VDP)から翻訳されています。


**VDP**（ぶいでぃーぴー）とは Video Display Processor の略称であり、[コンピュータ](../Page/コンピュータ.md "wikilink")の機能ブロックとして[映像](https://ja.wikipedia.org/wiki/映像 "wikilink")出力全般を担う[プロセッサ](../Page/プロセッサ.md "wikilink")に対する呼称の一つである。

## 概要

VDPという名称はテキサスインスツルメンツ社のチップ（[TMS9918](../Page/TMS9918.md "wikilink")など）で主に用いられた言葉だが、その後、[ヤマハ](../Page/ヤマハ.md "wikilink")（[V9938](../Page/V9938.md "wikilink")、[V9958](../Page/V9958.md "wikilink")など）をはじめとして各社がこの言葉を使うようになった。 同様の概念としては[CRTC](../Page/CRTC_\(LSI\).md "wikilink")（Cathode Ray Tube Controller）や[GPU](../Page/Graphics_Processing_Unit.md "wikilink")（Graphic Processing Unit）、[GDC](https://ja.wikipedia.org/wiki/GDC "wikilink")（Graphics Display Controller）などが存在する。

## 特徴

CRTCを用いたシステムでは、原則としてCPUから[VRAM](../Page/VRAM.md "wikilink")に[バスが繋がっており](../Page/バス_\(コンピュータ\).md "wikilink")、VRAM自体の操作をCPUが直接行うことが前提であるアーキテクチャが多い事に対し、VDPではVRAMはVDPに直結され、VRAMの操作はVDPのみが行う[アーキテクチャ](../Page/アーキテクチャ.md "wikilink")を取る場合が多い。CPUからの操作を受け付ける場合でも、VDPを介して間接的に操作する例が多い。

[TMS9918](../Page/TMS9918.md "wikilink")/[V9938](../Page/V9938.md "wikilink")/[V9958](../Page/V9958.md "wikilink")とその他の画像出力[LSI](https://ja.wikipedia.org/wiki/LSI "wikilink")との大きな違いとしては、VDPが[RGB](../Page/RGB.md "wikilink")信号（R,G,B,VSYNC,HSYNC）のほかにもNTSC/PAL[コンポジット映像信号](../Page/コンポジット映像信号.md "wikilink")（=複合映像信号=ビデオ信号）そのもの、またはそれに近い信号を直接出力している点にある。これは、CRTCやGPUではパソコン等の高解像度[ディスプレイを接続する前提となっているのに対し](../Page/ディスプレイ_\(コンピュータ\).md "wikilink")、VDPが[テレビ](../Page/テレビ.md "wikilink")に直接画像を出力するためである。CRTCなどでは外部にビデオ[D/Aコンバータ](https://ja.wikipedia.org/wiki/D/Aコンバータ "wikilink")や[ビデオ信号](https://ja.wikipedia.org/wiki/ビデオ信号 "wikilink")生成[回路](https://ja.wikipedia.org/wiki/回路 "wikilink")を構成しなければならないことが多い。なお、CRTCでも[リコー](../Page/リコー.md "wikilink")製RP5C16Yなどのように、NTSC信号の[インタレース](https://ja.wikipedia.org/wiki/インタレース "wikilink")表示のみではあるがコンポジット映像信号出力を行っているものがある。

## 応用例

汎用チップであることから、入門用の8bitホビーパソコンや、同世代の[ゲーム機](../Page/ゲーム機.md "wikilink")、[カーナビ](https://ja.wikipedia.org/wiki/カーナビ "wikilink")や[ケーブルテレビ](../Page/ケーブルテレビ.md "wikilink")の[セットトップボックス](../Page/セットトップボックス.md "wikilink")、[パチンコ](https://ja.wikipedia.org/wiki/パチンコ "wikilink")台や[携帯電話](../Page/携帯電話.md "wikilink")、映像機器等への内蔵等、多岐に渡る。

## 関連項目

  - [CRT](../Page/ブラウン管.md "wikilink")
  - [CRTC](../Page/CRTC_\(LSI\).md "wikilink")
  - [Graphics Processing Unit](../Page/Graphics_Processing_Unit.md "wikilink")
  - [VRAM](../Page/VRAM.md "wikilink")
  - [ウィンドウアクセラレータ](https://ja.wikipedia.org/wiki/ウィンドウアクセラレータ "wikilink")
  - [グラフィックアクセラレータ](../Page/グラフィックアクセラレータ.md "wikilink")
  - [スプライト](../Page/スプライト_\(映像技術\).md "wikilink")
  - [ディスプレイ](../Page/ディスプレイ_\(コンピュータ\).md "wikilink")
  - [TMS9918](../Page/TMS9918.md "wikilink")：NTSCビデオ信号が出力可能なVDP
  - [V9938](../Page/V9938.md "wikilink")：TMS9918A/TMS9928A/TMS9929A互換の上位VDP
  - [V9958](../Page/V9958.md "wikilink")：V9938上位互換のVDP
  - [V9990](https://ja.wikipedia.org/wiki/V9990 "wikilink")：V9938/V9958の後継を目指し、開発されたVDP
  - [セガ・マークIII](../Page/セガ・マークIII.md "wikilink")
  - [メガドライブ](../Page/メガドライブ.md "wikilink")
  - [セガサターン](../Page/セガサターン.md "wikilink")

[en:Video Display Processor](https://ja.wikipedia.org/wiki/en:Video_Display_Processor "wikilink")

[Category:VDP](https://ja.wikipedia.org/wiki/Category:VDP "wikilink") [Category:コンピュータアーキテクチャ](https://ja.wikipedia.org/wiki/Category:コンピュータアーキテクチャ "wikilink") [Category:グラフィックカード](https://ja.wikipedia.org/wiki/Category:グラフィックカード "wikilink")
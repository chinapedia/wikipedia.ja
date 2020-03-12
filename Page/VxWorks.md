> この記事は[VxWorks](https://ja.wikipedia.org/wiki/VxWorks)から翻訳されています。


{{ infobox OS | logo = | screenshot = | caption= | developer= [ウインドリバー・システムズ](https://ja.wikipedia.org/wiki/ウインドリバー・システムズ "wikilink") | source_model = | kernel_type= [モノリシックカーネル](../Page/モノリシックカーネル.md "wikilink") | supported_platforms= [x86](https://ja.wikipedia.org/wiki/x86 "wikilink"){{\*}}[x86-64](https://ja.wikipedia.org/wiki/x86-64 "wikilink"){{\*}}[MIPS](../Page/MIPSアーキテクチャ.md "wikilink"){{\*}}[PowerPC](../Page/PowerPC.md "wikilink"){{\*}}[SH-4](../Page/SuperH.md "wikilink"){{\*}}[ARM](../Page/ARMアーキテクチャ.md "wikilink"){{\*}}[SPARC Version 8 (V8)](../Page/SPARC.md "wikilink") | ui = | family = [リアルタイムオペレーティングシステム](../Page/リアルタイムオペレーティングシステム.md "wikilink") | released =  | latest_release_version = 7 | latest_release_date=  | latest_test_version= | latest_test_date = | marketing_target = [組み込みシステム](../Page/組み込みシステム.md "wikilink") | programmed_in= | prog_language= [Ada](../Page/Ada.md "wikilink"){{\*}}[C言語](../Page/C言語.md "wikilink"){{\*}}[C++](../Page/C++.md "wikilink"){{\*}}[Java](https://ja.wikipedia.org/wiki/Java "wikilink") | language = | updatemodel= | package_manager= | working_state= 開発中 | license= [使用許諾契約書 (EULA)](https://ja.wikipedia.org/wiki/EULA "wikilink") | website=  }} **VxWorks**(ブイエックスワークス) は、[アメリカ合衆国](https://ja.wikipedia.org/wiki/アメリカ合衆国 "wikilink") [WindRiver](https://ja.wikipedia.org/wiki/WindRiver "wikilink")社が開発・販売する[組み込みシステム](../Page/組み込みシステム.md "wikilink")向け[リアルタイムオペレーティングシステム](../Page/リアルタイムオペレーティングシステム.md "wikilink")。

## 概要

VxWorksは、高い安全性が要求される航空・宇宙・防衛の分野で広く使われている。[NASAは長年このOSを火星探査機に使ってきた](../Page/アメリカ航空宇宙局.md "wikilink")。[1997年](https://ja.wikipedia.org/wiki/1997年 "wikilink")の[マーズ・パスファインダー](../Page/マーズ・パスファインダー.md "wikilink")や[2004年](../Page/2004年.md "wikilink")の[マーズ・エクスプロレーション・ローバー](https://ja.wikipedia.org/wiki/マーズ・エクスプロレーション・ローバー "wikilink")上の制御ソフトウエアはVxWorks上で動いている。

このカテゴリとしては比較的規模の大きいOSではあるが、[QNX](../Page/QNX.md "wikilink")などのような「リアルタイムUnix」ではない。VoIP、ルータ、基幹ネットワーク、ロボット、産業機器、防衛航空宇宙、車載機器など、比較的大型の機器で使用されている。ゲームセンター用の大型筐体ゲームにも利用されている例がある。近年では、組込み向けコンピュータの高性能化に伴い、デジタル[家電](https://ja.wikipedia.org/wiki/家電 "wikilink")製品など比較的小型の機器にも用いられるようになってきている。

リアルタイムカーネル、[UNIX](../Page/UNIX.md "wikilink")ライクな機能のライブラリでのサポートやその他のライブラリ、[CPU](../Page/CPU.md "wikilink")コアと周辺を管理するBSP()などから成る。BSPを含めてスーパーバイザモードで動作し、アプリケーションからカーネルを関数コールで呼び出すため極めて高速に動作する、シェルからあらゆる関数をコマンドのように呼び出すことができ、デバッグが容易で、バグ等で発生したエラーはトラップして動作を回復させスタックを解析して関数の呼び出し履歴を表示する機能等があり、極めて開発効率が高い。

2001年、WindRiver社が[BSDI](https://ja.wikipedia.org/wiki/BSDI "wikilink")社を買収し、しかし顧客は優れたUNIXでなく、オープンな[Linux](../Page/Linux.md "wikilink")を求めていることを知り、WindRiver社はLinuxに方針転換をした。BSDIのエンジニアの貢献でファイルシステム(と呼ばれるUNIX系ファイルシステムで一種の[ジャーナリングファイルシステム](../Page/ジャーナリングファイルシステム.md "wikilink"))、I/Oシステム(XBD)、ネットワーク(MUX)、ドライバ(VxBUS)の根幹をなすフレームワークが確立され最先端の技術レベルとなった。

マルチコアに対する対応も、不可能といわれたSMPに対応、SMPハードウエアをAMPやAMP/SMP混在可能にしたり、 ハイパーバイザ技術も発表しシングルCPU上でLinuxとVxWorksの仮想化も可能にしている。

## 開発環境

VxWorksは、組み込みシステム向けとしては早くから、[Tornado](https://ja.wikipedia.org/wiki/Tornado "wikilink")（トルネード）と呼ばれる独自開発の[統合開発環境](../Page/統合開発環境.md "wikilink")が提供されており、ターゲットサーバーと呼ばれる技術が、ICEやツールの拡張性を高め、そのコンセプトが利点として知られてきた。

VxWorksは、バージョン6から、Tornadoを捨て[EclipseベースのWorkbench](../Page/Eclipse_\(統合開発環境\).md "wikilink")（ワークベンチ）と呼ばれる統合開発環境に移行した。蓄積された技術、アーキテクチャは踏襲され、近年、急激に需要を増したマルチコアの技術に呼応しツールの対応を進めている。特に組み込み開発特有のワークフローに着目し最適化を行い使いやすさを追求している。

## 関連項目

  - [EPICS](../Page/EPICS.md "wikilink")

## 外部リンク

  - [WindRiver](http://www.windriver.com/)（英語）
  - [ウインドリバー株式会社](http://www.windriver.com/japan/)（日本語）

<!-- end list -->

  - <http://www.creative-biolabs.com/Chimeric-Antigen-Receptor-CAR-construction-Service.html>

[Category:リアルタイムオペレーティングシステム](https://ja.wikipedia.org/wiki/Category:リアルタイムオペレーティングシステム "wikilink") [Category:組み込みオペレーティングシステム](https://ja.wikipedia.org/wiki/Category:組み込みオペレーティングシステム "wikilink") [Category:ロボット工学ソフトウェア](https://ja.wikipedia.org/wiki/Category:ロボット工学ソフトウェア "wikilink") [Category:ロボットOS](https://ja.wikipedia.org/wiki/Category:ロボットOS "wikilink")
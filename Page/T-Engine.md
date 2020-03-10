> この記事は[T-Engine](https://ja.wikipedia.org/wiki/T-Engine)から翻訳されています。


**T-Engine**（ティー・エンジン）は、組込みシステムの開発効率向上のためにミドルウェアの流通を目的として作られたプロジェクト。

## 概要

T-EngineプロジェクトはT-Engineフォーラムにより推進されている。T-Engineフォーラムは[TRONとT](../Page/TRONプロジェクト.md "wikilink")-Engineの提唱者である[坂村健](../Page/坂村健.md "wikilink")を会長として[2002年](../Page/2002年.md "wikilink")に発足した非営利任意団体で、T-Engineの趣旨に賛同する国内の主要な半導体メーカー、セットメーカー、流通、サービス、自治体、学術団体をはじめとして、海外からも多くの企業、研究機関が参加している（[2006年](../Page/2006年.md "wikilink")4月26日現在476団体）。

TRONプロジェクトでは、これまでにも[ITRON](../Page/ITRON.md "wikilink")と呼ばれるリアルタイムOSでサービスコールの仕様の標準化（「弱い標準化」）を進め、携帯電話やFAX、コピー機といったさまざまな家電製品からATM、カラオケマシンといった業務用機器、さらには自動車のエンジン制御といった多様な分野で、非常に多くの製品に採用されてきた実績がある。しかし、より高機能で、ネットワーク対応が進む組込み機器やユビキタス・コンピューティング環境の開発効率を向上させるため、T-Engineでは各種の[ハードウェア](../Page/ハードウェア.md "wikilink")仕様やドライバのインタフェース、オブジェクトフォーマットなどについても標準化（「強い標準化」）を行うことにより、ソフトウェア資産の共通化と有効活用を図ることを目標にしている。

具体的な開発プラットフォームとして[SHや](../Page/SuperH.md "wikilink")[MIPS](https://ja.wikipedia.org/wiki/MIPSアーキテクチャ "wikilink")、[ARMさらには](https://ja.wikipedia.org/wiki/ARMアーキテクチャ "wikilink")[FPGA](../Page/FPGA.md "wikilink")上のソフトコアなど、各種CPUに対応した[「T-Engine開発キット」](http://www.t-engine4u.com/)が入手できる。また、応用製品として[「Teacube」](http://www.t-engine4u.com/products/tcvr5701.html)などもある。これらの開発環境上でソフト開発を行う一方、並行してハードウェアの開発を進め、最終的にT-Engine上で開発したソフトをターゲットハードウェアに移植する、といった開発手法をとることで、最終製品のTime-to-Marketの短縮を目的としている。

## 仕様

[2006年](../Page/2006年.md "wikilink")現在、制定されている仕様は以下の通り。

### ハードウェア仕様

#### 標準T-Engine

携帯情報端末など比較的高度な[ユーザインタフェース](../Page/ユーザインタフェース.md "wikilink")を持つ機器のための開発用プラットフォーム。[CPU](../Page/CPU.md "wikilink")ボードのサイズは75mm×120mmと規格で決められている。[LCD](https://ja.wikipedia.org/wiki/液晶ディスプレイ "wikilink")、拡張ボードなどを接続できるようになっている。具体的なパッケージとして各種CPUに対応した[「T-Engine開発キット」](http://www.t-engine4u.com)がある。

#### μT-Engine（マイクロ・ティーエンジン）

[家電や計測機器などで必ずしも](../Page/家庭用電気機械器具.md "wikilink")[GUIを必要としない機器のための開発用プラットフォーム](https://ja.wikipedia.org/wiki/グラフィカルユーザインタフェース "wikilink")。[CPU](../Page/CPU.md "wikilink")ボードのサイズは60mm×85mmと規格で決められている。具体的なパッケージとして各種CPUに対応した[「μT-Engine開発キット」](http://www.t-engine4u.com)がある。

#### nT-Engine（ナノ・ティーエンジン）

小型家電機器等に適用するための、コイン大のプラットフォーム。標準T-EngineやμT-Engineといった開発用のプラットフォームではなく、デリバリを目的とした規格である。

#### pT-Engine（ピコ・ティーエンジン）

照明器具、スイッチ、センサー、[錠](../Page/錠前.md "wikilink")、[バルブ](../Page/バルブ.md "wikilink")など、[ユビキタスコンピューティング](../Page/ユビキタスコンピューティング.md "wikilink")環境の最小単位に適用する機器のためのプラットフォーム。nT-Engine同様、デリバリを目的とした規格である。

### ソフトウェア仕様

#### T-Kernel

T-Engine用の[組み込みオペレーティングシステム](../Page/組み込みオペレーティングシステム.md "wikilink")。従来からのITRONと同様、スタティックメモリアロケーションによるカーネルベースでのプログラミングが可能。しかし、T-Engine本来の目的である「ミドルウェアの流通」を実現するためには、ダイナミックメモリアロケーションが可能でプロセスベースでのプログラミングも可能なT-Kernel/Standard Extensionを使いこなすことが望まれる。2013年9月に打ち上げられた国産ロケット[イプシロンと](../Page/イプシロンロケット.md "wikilink")、それに搭載された観測衛星[ひさき](../Page/ひさき.md "wikilink")に、μITRONとT-Kernelがそれぞれ使われた\[1\]。[2014年](../Page/2014年.md "wikilink")12月3日に[H-IIAロケット](../Page/H-IIAロケット.md "wikilink")で打ち上げられた[はやぶさ2](../Page/はやぶさ2.md "wikilink")の制御システムにT-Kernel2.0が用いられた\[2\]。

2017年12月11日、μT-Kernel2.0を[IEEE](../Page/IEEE.md "wikilink")に著作権譲渡契約を結んだと発表された\[3\]。

2018年9月11日、「μT-Kernel 2.0」ベースの「IEEE 2050-2018」が、[IEEE](../Page/IEEE.md "wikilink")標準として正式に成立した\[4\]。

#### T-Monitor

OSの起動やデバッグを行うためのモニタソフトウェア。

## 応用製品

  - [Teacube](https://ja.wikipedia.org/wiki/Teacube "wikilink") - T-Engine＋T-Kernel+T-Shell（BTRON仕様OS「[超漢字](../Page/超漢字.md "wikilink")」に似たGUIミドルウェア）の実装例。コンシューマ用ではなく、組込みエンジニア向けにT-Kernelの評価用機器として発売されている。

## 脚注

<references/>

## 外部リンク

  - [T-Engineフォーラム](http://www.t-engine.org/ja/)
  - [パーソナルメディアT-Engineソリューション](http://www.t-engine4u.com/)
  - [SH/M32R T-Engine Home Page](http://www.superh-tkernel.org/jpn/)

[Category:TRONプロジェクト](https://ja.wikipedia.org/wiki/Category:TRONプロジェクト "wikilink") [Category:組み込みオペレーティングシステム](https://ja.wikipedia.org/wiki/Category:組み込みオペレーティングシステム "wikilink")

1.  [\[T-Engine Forum Japan](http://www.t-engine.org/ja/2014/mail-magazine-201401-1.html/)【2014.1】トロンプロジェクト30周年\]
2.
3.
4.
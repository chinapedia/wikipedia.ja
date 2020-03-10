> この記事は[SCADA](https://ja.wikipedia.org/wiki/SCADA)から翻訳されています。


**SCADA**（Supervisory Control And Data Acquisition の略。読み方はスキャダ）は、産業制御システムの一種であり、コンピュータによるシステム監視とプロセス制御を行う。対象プロセスは、以下のような生産工程やインフラや設備に関するものである。

  - [製造](../Page/製造業.md "wikilink")、[生産](../Page/大量生産.md "wikilink")、[発電](https://ja.wikipedia.org/wiki/発電 "wikilink")、組み立て、[精錬](https://ja.wikipedia.org/wiki/精錬 "wikilink")などを含む工業プロセスであり、連続モード、バッチモード、反復モード、離散モードなどがある。
  - 水処理、水道、排水、[下水処理](https://ja.wikipedia.org/wiki/下水処理場 "wikilink")、石油やガスのパイプライン、送電網、大規模通信システムなどのインフラ。
  - ビルディング、空港、船舶、宇宙ステーションなどの設備。[空調](../Page/空気調和.md "wikilink")、アクセス、エネルギー消費などを監視し制御する。

SCADA システムは一般に次のようなサブシステムから構成される。

  - [ユーザインタフェース](../Page/ユーザインタフェース.md "wikilink") - 対象プロセスのデータを人間のオペレータに提示し、人間のオペレータがプロセスを監視し制御できるようにする機構。
  - 監視制御（コンピュータ）システム - プロセス上のデータを収集し、プロセスに対してコマンドを送る。
  - 遠方監視制御装置 (RTU:Remote Terminal Unit) - プロセス内に設置されたセンサと接続し、センサの信号をデジタルのデータに変換し、そのデジタルデータを監視制御システムに送る装置。
  - [通信](../Page/通信.md "wikilink")基盤 - 監視制御システムと遠方監視制御装置 (RTU) を接続する。

SCADA と[分散制御システム](../Page/分散制御システム.md "wikilink") (DCS) を混同している場合がある。一般に SCADA システムはプロセスを調整するが、[実時間で制御はしない](https://ja.wikipedia.org/wiki/リアルタイムシステム "wikilink")。実時間制御という話は、新たな通信技術によって高信頼な低レイテンシで高速な通信が広域で可能になるにつれて、焦点がぼやけてしまう。SCADA と分散制御システム (DCS) の違いは主に文化的なもので、ほとんど無視できる。通信基盤が発達するにつれて、両者の違いは薄れる傾向にある。

## システムの概念

SCADA という用語は一般に、1つのサイト全体や地理的に分散したシステム群を集中的に監視制御するシステムを指す。制御のほとんどは遠方監視制御装置 (RTU) または[プログラマブルロジックコントローラ](https://ja.wikipedia.org/wiki/プログラマブルロジックコントローラ "wikilink") (PLC) が自動的に行う。ホストの制御機能は監督的な介入や優先的なものに限られることが多い。例えば、PLCが工業プロセスにおける冷却水の流量を制御する場合、フィードバック制御ループ自体はRTUやPLCでほぼ完結している。これに対し、SCADAシステムはそれらループの状態を監視するシステムという位置づけで、具体的には、SCADAシステムによりオペレータが流量の設定値を変更出来たり、警報発生条件（不正な流量や高温）を変更出来たり、現在の状態をオペレータに対して表示し記録する機能を提供する。

[ファイル:SCADA schematic overview-s.png](https://ja.wikipedia.org/wiki/ファイル:SCADA_schematic_overview-s.png "wikilink")

データ収集はRTUやPLCのレベルで行われ、必要に応じてSCADAに送られる。SCADAでは、収集されたデータを監視室のオペレータが見て監督的決定を行えるような形にして提示する。データは普通の[データベース管理システム](../Page/データベース管理システム.md "wikilink")上に構築された履歴システムにも送られ、傾向などの分析に使われる。

SCADAシステムでは通常、「タグデータベース」と呼ばれる[分散データベース](https://ja.wikipedia.org/wiki/分散データベース "wikilink")を実装している。これは、「タグ」または「ポイント」と呼ばれるデータ要素を格納するものである。1つのポイントは、1つの入力信号（監視データ）または1つの出力信号（制御コマンド）に対応している。ポイントには「ハード」と「ソフト」がある。ハードポイントはシステム内の実際の入出力に対応し、ソフトポイントは他のポイント群の値を使って計算や論理で得られるものである（多くの実装では、ハードポイントもソフトポイントの一種とされており、単に1つのデータだけを使ってそのまま出力するソフトポイントになっている）。ポイントは通常、値とタイムスタンプの対で格納され、この場合のタイムスタンプは記録または計算した時刻を表している。一連の値とタイムスタンプの対によって、そのポイントの履歴が得られる。タグに付加的な[メタデータ](https://ja.wikipedia.org/wiki/メタデータ "wikilink")を格納することも多く、対応する機器やPLCレジスタへの経路、設計時コメント、警報情報などが記述される。

## ヒューマンマシンインタフェース

[Scada_std_anim_no_lang.gif](https://ja.wikipedia.org/wiki/File:Scada_std_anim_no_lang.gif "fig:Scada_std_anim_no_lang.gif") [ヒューマンマシンインタフェース](https://ja.wikipedia.org/wiki/ヒューマンマシンインタフェース "wikilink")（HMI）は、人間のオペレータにプロセスのデータを提示する機構であり、また人間のオペレータがプロセスを制御する際にもそれを経由する。

HMI は通常 SCADA システムの[データベース](../Page/データベース.md "wikilink")やソフトウェアプログラムとリンクしており、傾向を見るためのデータや診断データ、保守手続きの予定などの管理情報、ロジスティック情報、特定のセンサや機械の詳細図、[エキスパートシステム](https://ja.wikipedia.org/wiki/エキスパートシステム "wikilink")による[トラブルシューティング](../Page/トラブルシューティング.md "wikilink")などが提供される。

HMI はそれらの情報を操作者にグラフィカルに提示する。すなわち、制御対象のプラントの図解の形で提示される。例えば、ポンプとそれに接続されたパイプが図示され、ポンプの稼働状況やパイプの流量が表示される。オペレータはポンプを停止させることができる。パイプの流量の変化は実時間で示される。図解は機器の写真を使ったり、アニメーション化された記号を使うこともある。

SCADAシステム用HMIパッケージには、オペレータなどが図を修正できる描画プログラムが含まれることが多い。HMIの図は単純なものから、超高層ビルの全エレベータの現在位置を示すとか、鉄道の全列車の現在位置を示すといった複雑なものまで様々である。

多くのSCADA実装で最も重要な点は、警報である。警報は何らかの状態値が異常になったときに発せられる。自動車の燃料タンクが空であることを示すライトも警報の一種である。警報を発する際には、[電子メール](../Page/電子メール.md "wikilink")が所定の管理者に送られることもある。

## ハードウェア

SCADA は[分散制御システム](../Page/分散制御システム.md "wikilink") (DCS) と共に構成されることが多い。マスタコンピュータの関与なしで自律的に単純な論理プロセスを実行できる RTU や PLC が使われることが増えている。RTU や PLC 上で動作するプログラムは [IEC 61131-3](https://ja.wikipedia.org/wiki/IEC_61131-3 "wikilink") で定義されている言語を使っていることが多い。[C言語](../Page/C言語.md "wikilink")や[FORTRAN](../Page/FORTRAN.md "wikilink")などの手続き型言語とは異なり、IEC 61131-3 はリレーによる制御回路の記述に似せてあるため、この分野の人にとっては訓練が少なくて済む利点がある。これによって、SCADAシステムの技術者はRTUやPLC上で実行されるプログラムの設計や実装も可能となっている。1998年ごろには、ほぼ全てのPLC製造企業が HMI/SCADA 統合システムを提供しており、その多くがオープンな通信プロトコルを採用している。サードパーティ製の HMI/SCADA パッケージの多くは、各社の主なPLCと互換性があり、制御対象のシステムの技術者が直接HMIを設定可能になっている。

### 遠方監視制御装置 (RTU)

RTUは実際の装置と接続される。RTUはその装置から得た電気信号（[スイッチや](../Page/開閉器.md "wikilink")[バルブ](https://ja.wikipedia.org/wiki/バルブ "wikilink")の開閉状態、圧力・流量・電圧・電流などの測定値など）をデジタルの値に変換する。逆にデジタルなコマンドを電気信号に変換して装置に送ることで、その装置を制御する（スイッチやバルブを開閉したり、[ポンプ](../Page/ポンプ.md "wikilink")の速度を設定するなど）。

高品質の SCADA RTU は以下のような特性を持つ。

  - データネットワーク機能
  - データ信頼性
  - データセキュリティ

### 監視制御ステーション

監視制御ステーションとは、各種装置（RTU、PLC など）と通信するソフトウェアおよび[サーバ](../Page/サーバ.md "wikilink")と、制御室内の[ワークステーション](../Page/ワークステーション.md "wikilink")などで動作するHMIソフトウェアを総称したものである。小型のSCADAシステムでは、1台の[パーソナルコンピュータ](../Page/パーソナルコンピュータ.md "wikilink")で動作する。大規模なSCADAシステムでは、複数台のサーバ上で分散ソフトウェアが動作し、災害リカバリ用の別サイトも用意される。システムの保全性を高めるため、各サーバを冗長構成またはホットスタンバイ構成にし、サーバ故障時にも連続的な制御や監視が行えるようにすることが多い。

かつては、[UNIX](../Page/UNIX.md "wikilink")や[OpenVMS](https://ja.wikipedia.org/wiki/OpenVMS "wikilink")が使われることが多く、[Linux](https://ja.wikipedia.org/wiki/Linux "wikilink")などはあまり使われなかったが、最近では主要な[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink")がサーバにもHMIワークステーションにも利用可能となっている。

#### 運用方針

実際の運用では、制御システムの障害が多大な損失を生じることがある。場合によっては人命に関わることもある。SCADA用ハードウェアは、温度変化・振動・電圧変動などに耐性があるものが使われるが、特に信頼性を要求される場合はハードウェアや通信路を冗長化し、場合によっては制御センターそのものを複数用意する。故障した箇所は素早く特定され、その機能はバックアップハードウェアで即座に代替される。故障箇所はプロセスを止めることなく交換可能となっていることが多い。このようなシステムの信頼性は、統計的に故障までの時間で表される（[平均故障間隔](https://ja.wikipedia.org/wiki/平均故障間隔 "wikilink")）。高信頼システムの平均故障間隔は、数百年のオーダーになることもある。

### 通信基盤と通信方法

SCADA システムの通信には従来から無線や[シリアル通信](https://ja.wikipedia.org/wiki/シリアル通信 "wikilink")が使われてきたが、鉄道や発電所などの大規模なサイトでは [SONET / SDH](https://ja.wikipedia.org/wiki/Synchronous_Optical_Network "wikilink") 上の IP やイーサネットも使われる。SCADAシステムの遠隔管理/監視機能は[テレメトリと呼ばれることがある](https://ja.wikipedia.org/wiki/遠隔測定法 "wikilink")。

SCADAのデータを既存の企業内ネットワークを使って転送するとか、他のアプリケーションとネットワークを共有させるといった動きもある。しかし初期の低帯域のプロトコルも未だに使われ続けている。SCADAのプロトコルは非常にコンパクトに設計され、マスタ側がRTUに要求しないと情報が送信されないようになっている。古くからあるSCADAプロトコルとしては、[Modbus](https://ja.wikipedia.org/wiki/Modbus "wikilink")、RP-570、[Profibus](https://ja.wikipedia.org/wiki/Profibus "wikilink")、Conitel などがある。これらはいずれもベンダー固有の通信プロトコルである。標準プロトコルとしては、[IEC 60870-5-101 または 104](https://ja.wikipedia.org/wiki/:en:IEC_60870-5 "wikilink")、[IEC 61850](https://ja.wikipedia.org/wiki/:en:IEC_61850 "wikilink")、[DNP3](https://ja.wikipedia.org/wiki/:en:DNP3 "wikilink") がある。これらは主要な業者の多くが採用している。これらのプロトコルの多くは、拡張として[TCP/IP上での運用が可能になっている](../Page/インターネット・プロトコル・スイート.md "wikilink")。セキュリティを考慮して、SCADAシステムは[インターネット](https://ja.wikipedia.org/wiki/インターネット "wikilink")に接続しないことが多い。

標準規格は後から生まれたものであるため、それまでに様々な制御プロトコルが考案され、使われてきた。また、[ベンダロックイン](https://ja.wikipedia.org/wiki/ベンダロックイン "wikilink")を意図して独自プロトコルを作った例もある。

最近では、異なるハードウェアやソフトウェア間の通信手法として [OLE for Process Control](https://ja.wikipedia.org/wiki/OLE_for_Process_Control "wikilink") (OPC) が広く採用されつつあり、元々産業ネットワークに接続することを考慮していない機器との通信も可能にしている。

## 最近の傾向

PLC と HMI/SCADA ソフトウェアは統合される傾向にある。1990年代中ごろ、データ収集装置は [RS-485のような物理キャリア上の独自プロトコルを使って通信するものが多かった](https://ja.wikipedia.org/wiki/EIA-485 "wikilink")。特定ベンダーの製品を使っているユーザーは、何らかの変更を必要としたとき（システム拡張、性能向上など）、選択肢があまりないことに気づかされる。そのような問題を緩和するべく、IEC870-5-101/104 や DNP 3.0 といったオープンな通信プロトコルの採用が広がっていった。[オープンアーキテクチャ](https://ja.wikipedia.org/wiki/オープンアーキテクチャ "wikilink")のSCADAシステムは、複数ベンダーの製品を組み合わせることができ、単一ベンダーに制限されている場合よりも良いソリューションを開発できる可能性がある。

1990年代末には、個々のI/O装置製造業者にもオープン化の流れが広まった。2000年までに多くのI/Oメーカーが Modicon MODBUS over TCP/IP のようなオープンなインタフェースを採用するようになった。

SCADAシステムは、ネットワーク技術の標準化と共に進化してきた。[イーサネット](../Page/イーサネット.md "wikilink")とTCP/IPに基づくプロトコルは、古い独自規格を置換しつつある。一部の分野ではイーサネットの採用は限定的だが、市場の大部分はHMI/SCADAにイーサネットによるネットワークを採用した。

OPC-UA、Wonderware の Archestra、Rockwell Automation の FactoryTalk などの次世代プロトコルは、[XML](../Page/Extensible_Markup_Language.md "wikilink")、[Webサービス](https://ja.wikipedia.org/wiki/Webサービス "wikilink")などの最新Web技術を生かしたものとなっている。

ソフトウェア業界で [Software as a Service](https://ja.wikipedia.org/wiki/SaaS "wikilink") の考え方が生まれ、[インターネット](https://ja.wikipedia.org/wiki/インターネット "wikilink")上の遠隔プラットフォーム上でSCADAシステムのホスティングをするベンダーが出現している（PumpView、MultiTrode など）。これは、ユーザーがシステムをインストールして設定する必要を無くすもので、インターネット技術として既にある [VPN](../Page/Virtual_Private_Network.md "wikilink") や [SSL](../Page/Transport_Layer_Security.md "wikilink") といったセキュリティ機能を利用する。しかし、セキュリティ\[1\]、信頼性、レイテンシを問題視する向きもある。

SCADAシステムは益々遍在するようになっている。[シンクライアント](https://ja.wikipedia.org/wiki/シンクライアント "wikilink")、Webポータル、[Webベースの製品が主要なベンダーで一般化しつつある](https://ja.wikipedia.org/wiki/ウェブアプリケーション "wikilink")。遠隔からプロセスを監視でき、便利にはなったが、セキュリティ上の懸念も増大している。

## セキュリティ問題

独自技術からより標準的でオープンな方式に移行することで、SCADAシステムはオフィスのネットワークや[インターネット](https://ja.wikipedia.org/wiki/インターネット "wikilink")との接続も増え、攻撃に対して脆弱になりつつある。結果として、サーバーテロ攻撃に対して無防備だと考えられるようになり、SCADAベースのシステムのセキュリティが問題視されるようになった\[2\]\[3\]。

特に、以下のような点が懸念されている。

  - 設計上、セキュリティや認証が考慮されていない。また、既存のSCADAネットワークでは運用上もセキュリティが考慮されていないことが多い。
  - SCADAシステムは一般に馴染みがない技術なので、特殊なプロトコルやインタフェースを使っているから安全だという間違った信念を持っていることがある。
  - SCADAシステムは物理的に安全だという間違った信念を持っていることがある。
  - SCADAシステムはインターネットとは接続されていないので安全だという間違った信念を持っていることがある。

SCADAシステムの多くは重要な設備で使われているため、攻撃を受けた場合、多大な経済的損失や人命の危険を生じる可能性がある。このような懸念から、重要な設備にSCADAよりも安全なアーキテクチャを採用するという動きが生じるかどうかはまだ不明である。最近では、Byres Security, Inc.、Industrial Defender Inc.、[チェック・ポイント・ソフトウェア・テクノロジーズ](https://ja.wikipedia.org/wiki/チェック・ポイント・ソフトウェア・テクノロジーズ "wikilink")、Innominate、N-Dimension Solutions といった複数のセキュリティベンダーが、TCP/IPベースのSCADAネットワークのための[ファイアウォール](../Page/ファイアウォール.md "wikilink")や[VPNを開発することで](../Page/Virtual_Private_Network.md "wikilink")、こういった問題に対処を開始している。

また、ISA Security Compliance Institute (ISCI) は早ければ2009年にも SCADA セキュリティテストを策定開始する予定である。ベンダーによるセキュリティ認証は既に2007年ごろから行われている。最終的には ISA SP99 WG4 が標準化を行う予定だが、完成するのは2011年以降になる。

## 脚注

## 関連項目

  - [産業制御システム](https://ja.wikipedia.org/wiki/産業制御システム "wikilink")
  - [遠隔測定法](https://ja.wikipedia.org/wiki/遠隔測定法 "wikilink")

## 参考文献

  - [NIST 800-82: Guide Industrial Control Systems Security, Supervisory Control and Data Acquisition (SCADA) Systems, Distributed Control Systems (DCS), and Other Control System Configurations such as Programmable Logic Controllers (PLC)](http://nvlpubs.nist.gov/nistpubs/SpecialPublications/NIST.SP.800-82r2.pdf)

## 国産SCADA

  - [計測監視制御ソフトウェアCraftPad](http://www.craftpat.com/)
  - [SCADA/HMI開発用ソフトウェア「看太郎」](http://www.tsubakimoto.jp/ecob/dp/dp01.html)
  - [IoT対応遠隔監視プラットフォーム「MitaMon®」](http://www.tsubakimoto.jp/other-products/iot/mitamon-starter/)
  - [現場力アップ支援システム「PlantPAD」](http://www.eng.nssmc.com/news/upload/docs/release_20111101.pdf)

[Category:制御工学](https://ja.wikipedia.org/wiki/Category:制御工学 "wikilink") [Category:ファクトリーオートメーション](https://ja.wikipedia.org/wiki/Category:ファクトリーオートメーション "wikilink") [Category:情報システム](https://ja.wikipedia.org/wiki/Category:情報システム "wikilink")

1.   (*Note: Donald Wallace is COO of M2M Data Corporation, a SCADA vendor.*)
2.
3.
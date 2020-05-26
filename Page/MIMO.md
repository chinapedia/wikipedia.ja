> この記事は[MIMO](https://ja.wikipedia.org/wiki/MIMO)から翻訳されています。


[thumb](https://ja.wikipedia.org/wiki/ファイル:MIMO_SIMO_MISO_SISO_explanation_without_confusion.svg "wikilink")

**MIMO** (**multiple-input and multiple-output**、マイモ)とは、[無線通信](../Page/無線通信.md "wikilink")において、送信機と受信機の双方で複数のアンテナを使い、通信品質を向上させることをいう。[スマートアンテナ](https://ja.wikipedia.org/wiki/スマートアンテナ "wikilink")技術の一つ。なお、"input" および "output" との言い方はアンテナを装備した機器を基準とするのではなく、信号を伝送する無線[伝送路](../Page/伝送路.md "wikilink")を基準としている（伝送路から見て入力となる送信側が "input"、伝送路から見て出力となる受信側が "output" となる）。

帯域幅や送信出力を強化しなくともデータのスループットやリンクできる距離を劇的に改善するということで、[無線通信](../Page/無線通信.md "wikilink")業界で注目されているテクノロジーである。周波数帯域の利用効率が高く（帯域幅1ヘルツ当たりのビットレートが高くなる）、リンクの信頼性または多様性を高めている（[フェージング](../Page/フェージング.md "wikilink")を低減）。以上からMIMOは、[IEEE 802.11n](https://ja.wikipedia.org/wiki/IEEE_802.11n "wikilink") (Wifi)、[4G](../Page/第4世代移動通信システム.md "wikilink")、[3GPP Long Term Evolution](https://ja.wikipedia.org/wiki/Long_Term_Evolution "wikilink")、[WiMAX](https://ja.wikipedia.org/wiki/WiMAX "wikilink")、[HSPA](../Page/HSPA.md "wikilink")+といった最近の無線通信規格の重要な一部となっている。

## 歴史

### 背景

この分野で最初期のアイデアとしては、A.R. Kaye と D.A. George（1970年）、W. van Etten（1975年、1976年）まで遡る。[ベル研究所](../Page/ベル研究所.md "wikilink")の Jack Winters と Jack Salz は1984年と1986年に[ビームフォーミング](https://ja.wikipedia.org/wiki/ビームフォーミング "wikilink")に関する応用についての論文を発表した\[1\]。

### 原理の考案

[Arogyaswami Paulraj](https://ja.wikipedia.org/wiki/:en:Arogyaswami_Paulraj "wikilink") と [Thomas Kailath](https://ja.wikipedia.org/wiki/:en:Thomas_Kailath "wikilink") は1993年、MIMOを使った [空間多重化](https://ja.wikipedia.org/wiki/空間多重化 "wikilink") (SM, spatial multiplexing) の概念を提唱した。1994年には空間多重化に関する特許（）を申請しており\[2\]、特に無線放送での応用を強調している。

1996年、Greg Raleigh と [Gerard J. Foschini](https://ja.wikipedia.org/wiki/:en:Gerard_J._Foschini "wikilink") はMIMOテクノロジーの新たなアプローチを考案し、リンクのスループットを効果的に改善すべく、一つの送信機に複数のアンテナを設置した構成を検討した\[3\]\[4\]。

1998年、ベル研究所はMIMO通信システムの性能を改善する主要テクノロジーである空間多重化の実験室レベルでのプロトタイプ開発に成功した\[5\]。

### 無線規格

世界初の実用化は2001年のことで、Iospan Wireless Inc. がMIMOと[直交周波数分割多元接続](https://ja.wikipedia.org/wiki/直交周波数分割多元接続 "wikilink")テクノロジー (MIMO-OFDMA) を使ったシステムを開発した。Iospanの技術は、ダイバーシティコーディングと空間多重化の両方をサポートしていた。2005年、[Airgo Networks](https://ja.wikipedia.org/wiki/:en:Airgo_Networks "wikilink") はMIMOに関する特許に基づき、まだ規格策定中だった [IEEE 802.11n](https://ja.wikipedia.org/wiki/IEEE_802.11n "wikilink") をいち早く実装した。翌2006年には、数社（[ブロードコム](../Page/ブロードコム.md "wikilink")、[インテル](https://ja.wikipedia.org/wiki/インテル "wikilink")、[マーベル他](https://ja.wikipedia.org/wiki/マーベル・テクノロジー・グループ "wikilink")）がMIMO-OFDMを採用し、まだ規格が確定していない802.11nの実装を行っている。同じく2006年、数社（Beceem Communications、[サムスン電子](../Page/サムスン電子.md "wikilink")、Runcom Technologies 他）がMIMO-OFDMAを採用し[WiMAX](https://ja.wikipedia.org/wiki/WiMAX "wikilink")（IEEE 802.16e）の実装を行った。今後の[4GシステムもMIMOテクノロジーを採用する予定である](../Page/第4世代移動通信システム.md "wikilink")。研究レベルでは1Gbit/sのプロトタイプも登場している。

## 機能

MIMOの主な機能は、プリコーディング、空間多重化 (SM)、[ダイバーシティ](../Page/ダイバーシティ.md "wikilink")コーディングの3つに分類される。

  - プリコーディング ([en](https://ja.wikipedia.org/wiki/:en:Precoding "wikilink"))
    プリコーディングとは狭義には、マルチストリームの[ビームフォーミング](https://ja.wikipedia.org/wiki/ビームフォーミング "wikilink")を意味する。広義には送信におけるあらゆる空間処理を意味する。（単一層の）ビームフォーミングにおいては、同じ信号をそれぞれの送信アンテナから適当な位相（および時には適当な利得）に重み付けして送信し、受信側で信号のパワーが最大になるようにする。ビームフォーミングの利点は受信側の信号利得を増大させることであり、そのために異なるアンテナから放射された信号を構築的に加算することができ、[多重伝送による](../Page/マルチパス.md "wikilink")[フェージング](../Page/フェージング.md "wikilink")の影響を低減させる。散乱がなければビームフォーミングは良い指向性パターンを示すが、典型的な携帯電話のビームとは異なる。受信側が複数のアンテナを持つ場合、送信側によるビームフォーミングで全受信アンテナの信号レベルを同時に最大化することはできず、マルチストリームのプリコーディングが使われる。なおプリコーディングを行うには、送信側で[チャネル状態情報](https://ja.wikipedia.org/wiki/チャネル状態情報 "wikilink") (CSI) についての知識を持っていることが要求される。
  - 空間多重化 ([en](https://ja.wikipedia.org/wiki/:en:Spatial_multiplexing "wikilink"))
    空間多重化にはMIMO型のアンテナ構成を必要とする。高転送レートの信号を低転送レートの複数のストリームに分割し、それぞれのストリームをそれぞれの送信アンテナから同じ周波数チャネルに発信する。受信側のアンテナ・アレイで個々のアンテナの空間特性が十分に異なるなら、それらの信号がそれぞれのアンテナによって受信され、並列のチャネルとしてそれらのストリームを分離することができる。空間多重化は、高い[SN比](../Page/SN比.md "wikilink")で[通信路容量](../Page/通信路容量.md "wikilink")を増大させる非常に強力な技法の1つである。空間ストリームの最大数は、送信側または受信側のアンテナ数の少ないほうに制限される。空間多重化には伝送路についての知識は必ずしも必須ではない。空間多重化を複数の受信機への同時送信に使うこともでき、それを[空間分割多元接続](https://ja.wikipedia.org/wiki/空間分割多元接続 "wikilink") (SDMA) と呼ぶ。
  - ダイバーシティコーディング ([en](https://ja.wikipedia.org/wiki/:en:Diversity_Coding "wikilink"))
    送信側にチャネル状態情報についての知識が全くない場合の技法。空間多重化とは異なり単一のストリームを送信するが、その信号は[時空間符号化](https://ja.wikipedia.org/wiki/時空間符号化 "wikilink")という技法で符号化される。その信号を（ほぼ）完全な直交符号としてそれぞれの送信アンテナから発信する。ダイバーシティコーディングは、複数アンテナリンクにおける個々のフェージングを利用して、信号の[ダイバーシティ](../Page/ダイバーシティ.md "wikilink")を強化する。チャネルについて知識がないため、ダイバーシティコーディングでビームフォーミングを行うことはできない。

送信側でチャネルについての知識があれば、空間多重化とプリコーディングを組合わせることができ、復号の信頼性とのトレードオフで空間多重化とダイバーシティコーディングを組合わせることもできる。

## 形態

### マルチアンテナ型

802.11n 製品などはマルチアンテナ型（シングルユーザーMIMO）の実装である。MIMOが縮退するとSISO (single input and single output)/SIMO/MISOとなる。受信側が単一アンテナとなる縮退状態がMISO (multi input and single output) で、送信側が単一アンテナとなる縮退状態が SIMO (single input and multi output) である。SISOは送信側も受信側も単一アンテナの通常の無線通信を意味する。

シングルユーザーMIMOの基本技法として、次の具体例がある。

  - [Bell Laboratories Layered Space-Time (BLAST)](https://ja.wikipedia.org/wiki/:en:Bell_Laboratories_Layered_Space-Time "wikilink"), Gerard. J. Foschini (1996)
  - Per Antenna Rate Control (PARC), Varanasi, Guess (1998), Chung, Huang, Lozano (2001)
  - Selective Per Antenna Rate Control (SPARC), Ericsson (2004)

アンテナの配置間隔はなるべく広い方が望ましく、基地局では[波長](../Page/波長.md "wikilink")の何倍という値になる。アンテナの配置は携帯型の送受信機では重大な問題であり、設計とアルゴリズムによる対策の両面で検討が進められている。

### マルチユーザーMIMO

近年、マルチユーザーMIMO技術の研究が盛んになっている。完全なマルチユーザーMIMO（ネットワーク型MIMO）は高い可能性を秘めており、部分的なマルチユーザーMIMOの実用化研究が盛んである。

  - マルチユーザーMIMO (MU-MIMO, [en](https://ja.wikipedia.org/wiki/:en:Multi-user_MIMO "wikilink"))
    MU-MIMOは高いスループット能力を実現しつつ、SU-MIMOよりも受信アンテナ数が少なく機器の複雑性も小さくて済むため、[3GPP](../Page/3GPP.md "wikilink")と[WiMAX](https://ja.wikipedia.org/wiki/WiMAX "wikilink")の最近の規格では、サムスン、インテル、クアルコム、エリクソン、TI、ファーウェイ、フィリップス、アルカテル・ルーセント、フリースケールといった多くの企業が仕様を実現するための技術候補の1つとしてMU-MIMOを挙げている。
    シングルユーザーMIMOのスケジューリングが単独のユーザーだけに割り当てるのに対して、[PU<sup>2</sup>RC](https://ja.wikipedia.org/wiki/:en:PU2RC "wikilink") (Per-User Unitary Rate Control) ではネットワークがそれぞれのアンテナを異なるユーザーに割り当てることを可能にする。ネットワークはコードブックベースの空間ビームまたは仮想アンテナを通してユーザーデータを送信することができる。空間的に識別可能なユーザーとコードブックベースの空間ビームをペアにするなどの効率的なユーザースケジューリングは、無線ネットワークの単純化という観点で議論が進められている。PU<sup>2</sup>RC は IEEE 802.16m (WiMAX2) の system description documentation (SDD) に含まれている。
  - 協調MIMO (CO-MIMO)
    分散して存在する異なるユーザーのものであるアンテナ群を利用するMIMO。
  - MIMO [ルーティング](../Page/ルーティング.md "wikilink")
    MIMOルーティングとはクラスター単位のルーティングであり、各クラスターは1つ以上のノードからなる。従来の(SISO)ルーティングはノードからノードへのルーティングであるのに対して、MIMOルーティングはクラスター単位である点が異なる\[6\]。

## 用途

空間多重化技法は受信機を非常に複雑化させるため、一般に変調方式として[マルチパス](../Page/マルチパス.md "wikilink")に起因する問題を効率的に扱える[直交周波数分割多重方式](../Page/直交周波数分割多重方式.md "wikilink") (OFDM) または[直交周波数分割多元接続](https://ja.wikipedia.org/wiki/直交周波数分割多元接続 "wikilink") (OFDMA) と組合わせて使用する。IEEE 802.16e ではMIMO-OFDMAを採用している。2009年10月にリリースされた IEEE 802.11n はMIMO-OFDMを推奨している。

[移動体通信](../Page/移動体通信.md "wikilink")でも、[3GPP](../Page/3GPP.md "wikilink")や[3GPP2](../Page/3GPP2.md "wikilink")の最近の規格でMIMOが採用されている。3GPPでは、[HSPA](../Page/HSPA.md "wikilink")+および [Long Term Evolution (LTE)](https://ja.wikipedia.org/wiki/Long_Term_Evolution "wikilink") でMIMOを取り入れている。さらに携帯電話環境でMIMOを完全サポートするため、[IST-MASCOT](http://www.ist-mascot.org/) などの研究コンソーシアムはより進んだマルチユーザーMIMOの開発を提案している。

MIMOは無線通信だけに限定される概念ではない。有線通信でも活用可能である。例えば Binder MIMO Channels に基づいた新たな[DSL技術](../Page/デジタル加入者線.md "wikilink")（ギガビットDSL）が提案されている。

## 数学的解説

[thumb](https://ja.wikipedia.org/wiki/ファイル:Kanalmatrix_MIMO.png "wikilink") MIMOシステムでは、送信機が複数の送信アンテナを使って複数のストリームを送信する。送信ストリームは送信機側の \(N_t\) 個の送信アンテナと受信機側の \(N_r\) 個の受信アンテナの間の全部で \(N_t N_r\) 個の伝送路から成る[行列](https://ja.wikipedia.org/wiki/行列 "wikilink")チャネルを通る。受信機は複数の受信アンテナで信号[ベクトルを受信し](https://ja.wikipedia.org/wiki/ベクトル空間 "wikilink")、それら信号ベクトルを復号して元の情報を得る。[ナローバンド](../Page/ナローバンド.md "wikilink")のフラット[フェージング](../Page/フェージング.md "wikilink")型MIMOシステムは次の式でモデル化される。

\[\mathbf{y} = \mathbf{H}\mathbf{x} + \mathbf{n}\] ここで \(\scriptstyle\mathbf{y}\) と \(\scriptstyle\mathbf{x}\) は受信と送信のベクトルで、\(\scriptstyle\mathbf{H}\) と \(\scriptstyle\mathbf{n}\) はそれぞれチャネル行列とノイズベクトルである。

[情報理論](../Page/情報理論.md "wikilink")によれば、送信側も受信側も[チャネル状態情報](https://ja.wikipedia.org/wiki/チャネル状態情報 "wikilink") (CSI) を完全かつ即時に把握しているMIMOシステムの[エルゴード的](../Page/エルゴード理論.md "wikilink")[通信路容量](../Page/通信路容量.md "wikilink")は次の式で表される\[7\]。

\[C_\mathrm{perfect-CSI} = E\left[\max_{\mathbf{Q}; \, \mbox{tr}(\mathbf{Q}) \leq 1} \log_2 \det\left(\mathbf{I} + \rho \mathbf{H}\mathbf{Q}\mathbf{H}^{H}\right)\right] = E\left[\log_2 \det\left(\mathbf{I} + \rho \mathbf{D}\mathbf{S} \mathbf{D} \right)\right]\] ここで \(()^H\) は[随伴作用素](https://ja.wikipedia.org/wiki/随伴作用素 "wikilink")を意味し、\(\rho\) は送信出力とノイズ出力の比（すなわち送信側での[SN比](../Page/SN比.md "wikilink")）である。最適な信号共分散 \(\scriptstyle \mathbf{Q}=\mathbf{VSV}^H\) はチャネル行列 \(\scriptstyle\mathbf{UDV}^H \,=\, \mathbf{H}\) と最適な対角線出力配分行列 \(\scriptstyle \mathbf{S}=\textrm{diag}(s_1,\ldots,s_{\min(N_t, N_r)},0,\ldots,0)\) の[特異値分解](../Page/特異値分解.md "wikilink")から得られる。最適な出力配分は[注水定理](https://ja.wikipedia.org/wiki/注水定理 "wikilink") (water-filling) アルゴリズムで得られ、つぎのようになる\[8\]。

\[s_i = \left(\mu - \frac{1}{\rho d_i^2} \right)^+, \quad \textrm{for} \,\, i=1,\ldots,\min(N_t, N_r),\] ここで \(d_1,\ldots,d_{\min(N_t, N_r)}\) は \(\scriptstyle \mathbf{D}\) の対角線要素であり、\((\cdot)^+\) はその引数が負ならゼロになることを意味し、\(\mu\) は \(s_1+\ldots+s_{\min(N_t, N_r)}=N_t\) となるよう選択する。

送信機が統計的な[チャネル状態情報](https://ja.wikipedia.org/wiki/チャネル状態情報 "wikilink")しか持たない場合、信号共分散 \(\scriptstyle \mathbf{Q}\) は次のように平均[相互情報量](../Page/相互情報量.md "wikilink")によってのみ最適化され、エルゴード的[通信路容量](../Page/通信路容量.md "wikilink")が減少する\[9\]。

\[C_\mathrm{statistical-CSI} = \max_{\mathbf{Q}} E\left[\log_2 \det\left(\mathbf{I} + \rho \mathbf{H}\mathbf{Q}\mathbf{H}^{H}\right)\right].\] チャネルの[空間相関](https://ja.wikipedia.org/wiki/空間相関 "wikilink")は、統計情報に基づくエルゴード的[通信路容量](../Page/通信路容量.md "wikilink")に重大な影響を与える。

送信機が[チャネル状態情報](https://ja.wikipedia.org/wiki/チャネル状態情報 "wikilink")を全く持たない場合、最悪ケースの統計量における通信路容量を最大化するよう信号共分散 \(\scriptstyle \mathbf{Q}\) を選択でき、結局 \(\scriptstyle \mathbf{Q}=1/N_t \mathbf{I}\) となり、次の式で表される。

\[C_\mathrm{no-CSI} = E\left[\log_2 \det\left(\mathbf{I} + \frac{\rho}{N_t}\mathbf{H}\mathbf{H}^{H}\right)\right].\]

チャネルの統計的特性にも依存するが、エルゴード的容量はSISOシステムのそれに比べると大抵の場合 \(\scriptstyle\min(N_t, N_r)\) 倍となる。

## MIMOテスト

MIMO信号テストは第一に送信機/受信機システムを対象とする。副搬送波信号の無作為な位相により瞬時に様々なパワーレベルを作り出すことができ、それによって信号圧縮や瞬間的な歪みを生み出し、最終的にシンボルエラーを引き起こすことができる。**PAR**（ピーク対平均値パワー比）の大きい信号は、送信機での処理過程での信号圧縮が予測できない。OFDM信号は非常にダイナミックで、ノイズのような性質があるために圧縮問題を検出するのが困難である。

信号チャネルの品質を知ることも重要である。チャネルエミュレータはセルエッジでの機器の振る舞いをシミュレートでき、ノイズを追加したり、転送速度によるチャネルの変化をシミュレートできる。受信機の性能を完全に評価する場合、ベクトル信号発生器 (VSG) のような較正された送信機とチャネルエミュレータを使って様々な条件で受信機をテストする。逆に様々な条件下での送信機の性能を評価するには、チャネルエミュレータとベクトル信号アナライザ (VSA) のような較正された受信機を使えばよい。

チャネルを理解することで、個々の送信機での位相と振幅を操作してビームを形成できる。正しくビームを形成するには、送信機がチャネルの特性を理解している必要がある。その過程を「チャネルサウンディング」または「チャネル推定」と呼ぶ。チャネル環境の像を描けるモバイル機器に既知の信号を送る。その機器が送信機側にチャネル特性などの情報を送り返す。送信機はその情報を使って位相や振幅を調整し、うまくビームを形成することができる。これを閉ループMIMOシステムと呼ぶ。ビームフォーミングの場合は、個々の送信機の位相と振幅を調整する必要がある。

## 文献

### 一次研究資料

Gerard J. Foschini と Michael J. Gans の論文\[10\]、Foschiniの論文\[11\]、Emre Telatar の論文\[12\]で、MIMOシステムの[通信路容量](../Page/通信路容量.md "wikilink")（システムのスループットの理論的上限）がアンテナ数を増やすと共に向上し、送信/受信アンテナの少ない方の数に比例することを示した。[情報理論](../Page/情報理論.md "wikilink")におけるこれらの発見により、MIMOシステム実用化研究の爆発的発展が生じた。この分野の入門書としては A. Paulraj、R. Nabar、D. Gore の著書がある\[13\]。

### ダイバーシティと多重化のトレードオフ (DMT)

MIMOシステムの[ダイバーシティ](../Page/ダイバーシティ.md "wikilink")と多重化には根本的なトレードオフ関係がある(Zheng and Tse, 2003)\[14\]。

## 脚注・出典

## 参考文献

  - Claude Oestges, Bruno Clerckx, "[Wireless Communications : From Real-world Propagation to Space-time Code Design,](http://www.amazon.com/MIMO-Wireless-Communications-Real-World-Propagation/dp/0123725356MIMO)" Academic, 2007.07.16, 448p, ISBN 0123725356.

## 関連項目

  - [チャネルボンディング](https://ja.wikipedia.org/wiki/チャネルボンディング "wikilink")
  - [フェーズドアレイレーダー](../Page/フェーズドアレイレーダー.md "wikilink")
  - [IEEE 802.11](../Page/IEEE_802.11.md "wikilink")
  - [WiMAX](https://ja.wikipedia.org/wiki/WiMAX "wikilink") (IEEE 802.16)

## 外部リンク

  - [GEDOMIS® (GEneric hardware DemOnstrator for MIMO Systems)](http://wikieng.cttc.es/index.php/GEDOMIS)
  - [NIST UWB-MIMO Channel Propagation Measurements in the 2-8 GHz Spectrum](http://www-x.antd.nist.gov/uwb/main.html)
  - D. Gesbert, M. Kountouris, R. W. Heath, Jr., C.-B. Chae, and T. Salzer, [Shifting the MIMO Paradigm: From Single User to Multiuser Communications](http://www.eurecom.fr/%7Egesbert/papers/TutorialMUMIMOv3.pdf), IEEE Signal Processing Magazine, vol. 24, no. 5, pp. 36–46, Oct., 2007
  - [Links to suggested readings in MIMO](http://wcsp.eng.usf.edu/MIMO_links.html) - WCSP Group — University of South Florida (USF)
  - [Introduction to Wireless MIMO - Theory and Applications](http://www.ieee.li/pdf/viewgraphs/wireless_mimo.pdf)
  - [Introduction to Orthogonal Frequency Division Multiplexing (covers OFDM and MIMO radio configurations)](http://www.ieee.li/pdf/viewgraphs/introduction_orthogonal_frequency_division_multiplex.pdf)
  - [Introduction to MIMO](http://www.ece.ualberta.ca/~HCDC/mimohistory.html)
  - Computerworld QuickStudy [MIMO](http://www.computerworld.com/action/article.do?command=viewArticleBasic&articleId=109410)
  - [Developing Strategies for MIMO Testing](http://www.mwjournal.com/Journal/article.asp?HH_ID=AR_7230)
  - [Meeting The Test Challenges Of 4G LTE](http://www.rfglobalnet.com/article.mvc/Meeting-The-Test-Challenges-Of-4G-LTE-0001)
  - [The Basics Of OFDM](http://www.rfglobalnet.com/article.mvc/The-Basics-Of-OFDM-0001)
  - [MIMO: The Future Of Wireless: Test Challenges For WiMAX, HSPA+, And LTE](http://www.rfglobalnet.com/article.mvc/MIMO-The-Future-Of-Wireless-0001)
  - [OFDM Will Soon Be Dominant Form Of Digital Modulation](http://www.mwrf.com/Articles/Index.cfm?ArticleID=18032)
  - [The challenges of moving to MIMO systems](http://mobiledevdesign.com/hardware_news/radio_challenges_moving_mimo/)
  - [RF test system tackles 4 x 4 MIMO signals](http://rfdesign.com/microwave_millimeter_tech/test_and_measurement/711RFD30.pdf)
  - [The Role Of EVM Measurements In Characterizing Amplifier Modulation Performance](http://www.rfglobalnet.com/article.mvc/EVM-Measurements-In-Amplifier-Modulation-0001)
  - [Industry Views: 4G Systems Bring New Design And Testing Challenges](http://www.rfglobalnet.com/article.mvc/Industry-Views-4G-Systems-Bring-New-Design-An-0002)
  - [Test System Pushes MIMO Standards Into The Spotlight](http://electronicdesign.com/Articles/Index.cfm?ArticleID=17368)

[Category:IEEE_802](https://ja.wikipedia.org/wiki/Category:IEEE_802 "wikilink") [Category:情報理論](https://ja.wikipedia.org/wiki/Category:情報理論 "wikilink") [Category:通信工学](https://ja.wikipedia.org/wiki/Category:通信工学 "wikilink")

1.  J. Salz, “Digital transmission over cross-coupled linear channels,” AT\&T Technical Journal, vol. 64, no. 6, pp. 1147-1159, July–August 1985.
2.  <http://patft.uspto.gov/netacgi/nph-Parser?Sect2=PTO1&Sect2=HITOFF&p=1&u=%2Fnetahtml%2FPTO%2Fsearch-bool.html&r=1&f=G&l=50&d=PALL&RefSrch=yes&Query=PN%2F5345599>
3.  Gregory G. Raleigh and John M. Cioffi, “Spatio-temporal coding for wireless communication,” IEEE Transactions on Communications, vol. 46, no. 3, pp. 357-366, March 1998.
4.  G. J. Foschini, “Layered space–time architecture for wireless communication in a fading environment when using multiple antennas,” Bell Labs Syst. Tech. J., vol. 1, p. 41–59, Autumn 1996.
5.  G. D. Golden, G. J. Foschini, R. A. Valenzuela, and P. W. Wolniansky, “Detection algorithm and initial laboratory results using V-BLAST space–time communication architecture,” Electron. Lett., vol. 35, pp.\~14–16, Jan. 1999.
6.
7.  D. Love, R. Heath, V. Lau, D. Gesbert, B. Rao and M. Andrews, [An overview of limited feedback in wireless communication systems](http://www.eurecom.fr/~gesbert/papers/JSAC_limitedfeedback_tutorial.pdf), IEEE Journal on Selected Areas Communications, vol 26, pp. 1341-1365, 2008.
8.  D. Tse and P. Viswanath, [Fundamentals of Wireless Communication](http://www.eecs.berkeley.edu/~dtse/book.html), Cambridge University Press, 2005.
9.
10.
11.
12. [Capacity of Multi-antenna Gaussian Channels](http://web.mit.edu/6.454/www/www_fall_2004/alex_o/Telatar99.pdf#search=%22telatar%22)
13.
14.
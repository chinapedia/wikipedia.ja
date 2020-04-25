> この記事は[ARPANET](https://ja.wikipedia.org/wiki/ARPANET)から翻訳されています。


[Arpanet_logical_map,_march_1977.png](https://ja.wikipedia.org/wiki/File:Arpanet_logical_map,_march_1977.png "fig:Arpanet_logical_map,_march_1977.png") **ARPANET**（アーパネット、**A**dvanced **R**esearch **P**rojects **A**gency **NET**work、高等研究計画局ネットワーク）は、世界で初めて運用された[パケット通信](../Page/パケット通信.md "wikilink")[コンピュータネットワーク](../Page/コンピュータネットワーク.md "wikilink")であり、[インターネット](../Page/インターネット.md "wikilink")の起源でもある。[アメリカ国防総省](../Page/アメリカ国防総省.md "wikilink")の[高等研究計画局](../Page/国防高等研究計画局.md "wikilink")（略称ARPA、後にDARPA）が資金を提供し、いくつかの大学と研究機関でプロジェクトが行われた。ARPANETのパケット交換は[イギリス](https://ja.wikipedia.org/wiki/イギリス "wikilink")の科学者[ドナルド・デービス](https://ja.wikipedia.org/wiki/ドナルド・ワッツ・デービス "wikilink")\[1\]\[2\]と[リンカーン研究所](https://ja.wikipedia.org/wiki/リンカーン研究所 "wikilink")の[ローレンス・ロバーツ](https://ja.wikipedia.org/wiki/ローレンス・ロバーツ "wikilink")\[3\]の設計に基づいていた。

## 歴史

パケット交換は今日データ通信の基盤として世界中で使われているが、ARPANETの構想が持ち上がった当時は新しい概念だった。パケット交換が登場する以前、音声通信やデータ通信は[回線交換](https://ja.wikipedia.org/wiki/回線交換 "wikilink")が基本であり、電話の回線網のように電話をかけるたびに通信局から通信局まで専用の電気的接続がなされていた。この場合の通信局は電話やコンピュータである。この（一時的な）専用回線は多数の中継局間の回線から構成されており、発信局から受信局までを結ぶようになっている。パケット交換では、データシステムは単一の通信リンクを使って複数のマシンと通信する。データは[データグラム](https://ja.wikipedia.org/wiki/データグラム "wikilink")に分割され、[パケット](../Page/パケット.md "wikilink")としてそのネットワークのリンク上を転送される。パケットは小さいので、リンクはすぐに空き状態となり、別のパケットを転送可能となる。そのため、[郵便ポスト](../Page/郵便ポスト.md "wikilink")が様々な宛先の手紙を出すのに使えるようにリンクを共有できるだけでなく、各パケットはそれぞれ独自の経路で転送される\[4\]。

### 概念の提唱

ARPANETに直接影響を及ぼしたコンピュータネットワークの概念の提唱を行ったのは[BBNテクノロジーズ](../Page/BBNテクノロジーズ.md "wikilink")の[J・C・R・リックライダー](../Page/J・C・R・リックライダー.md "wikilink")による[タイムシェアリングシステム](../Page/タイムシェアリングシステム.md "wikilink")によるネットワークである。リックライダーの1960年の論文、「人間とコンピュータの共生」\[5\]の中で早くもリソースを共有するためのタイムシェアリングシステムのネットワークの可能性について言及している箇所が見られる。又リックライダーがARPAのIPTO\[6\]部長に就任した後の1963年にIPTOの助成機関宛に送ったメモランダム「銀河間コンピュータネットワークメモランダム」\[7\]の中ではIPTOの将来的な目標として相互の研究内容の情報を共有するためにコンピュータネットワークを構築することの提案を行っている。これには現在のインターネットを構成するほとんど全てのアイデアが含まれていた。リックライダーは計画が実施される前にARPAを去ったが、その構想は[アイバン・サザランド](../Page/アイバン・サザランド.md "wikilink")、[ロバート・テイラーといった彼がIPTOに入社した彼の後継者達によって受け継がれる事になった](../Page/ロバート・テイラー_\(情報工学者\).md "wikilink")\[8\]。

### ネットワークの実験

サザランドとテイラーはそのようなコンピュータネットワークを構築することに関心を持ち続け、ARPAが資金提供しているアメリカ各地の様々な企業や[大学](../Page/大学.md "wikilink")の研究者たちがARPAの資金で開発されたコンピュータ群にアクセスできるようにし、ソフトウェアなどの[計算機科学](../Page/計算機科学.md "wikilink")の成果を素早く広めたいと考えていた\[9\]。テイラーのオフィスには3つのコンピュータ端末があり、それぞれ別々の（ARPAが資金提供した）コンピュータに接続されていた。1つは[サンタモニカ](../Page/サンタモニカ.md "wikilink")の [System Development Corporation](https://ja.wikipedia.org/wiki/:en:System_Development_Corporation "wikilink") (SDC) にある[AN/FSQ-32](https://ja.wikipedia.org/wiki/:en:AN/FSQ-32 "wikilink")\[10\]、2つめは[カリフォルニア大学バークレー校](../Page/カリフォルニア大学バークレー校.md "wikilink")の[Project GENIE](../Page/Project_GENIE.md "wikilink")、3つめは[MITの](../Page/マサチューセッツ工科大学.md "wikilink")[Multics](../Page/Multics.md "wikilink")である。これについてテイラーは後に次のように回想している。

> 「この3台の端末はそれぞれユーザーコマンド群が異なっていた。だから私が S.D.C. の誰かとオンラインで話をしていて、バークレーあるいはMITの誰かと話したいとき、S.D.C. との端末から離れて、別の端末にログインして連絡する必要があった。（中略）何をするのかは明らかだが、私はそんなことをしたくない。インタラクティブ・コンピューティングが可能なら、1つの端末でどこにでも接続できるべきだ。このアイデアが ARPANET だ」\[11\]

1964年にリックライダーがIPTOの部長を退いた後、彼の役職を継いだサザランドはリックライダーが提唱したコンピュータネットワークの実験を行ってみる事にした。1965年にUCLAの2つのコンピュータをネットワークで接続してみる事になったが、この実験は通信方式に問題があったために失敗した。

### ARPANETの開発

1966年にサザランドの次にIPTO部長に就任したテイラーは更に一歩進めて本格的なコンピューターネットワークを構築しようと試み、ARPA本体から予算を取り付けた。ただしテイラーはリックライダーと同じ音響心理学者でコンピュータ工学のエンジニアではなかった。このためネットワークを実際に構築できる技術者を必要としていた。こうして[マサチューセッツ工科大学](../Page/マサチューセッツ工科大学.md "wikilink")の[リンカーン研究所](https://ja.wikipedia.org/wiki/リンカーン研究所 "wikilink")から半ば脅される形でIPTOにリクルートされてきたのが[ローレンス・ロバーツ](https://ja.wikipedia.org/wiki/ローレンス・ロバーツ "wikilink")である。ロバーツは1967年にこれまでリックライダーやサザランド、タイラーが概念として述べてきた事を「指示書」のような形でまとめた。これが"Multiple Computer Network and Intercomputer Communication"\[12\]である。この「指示書」の中ではARPANETの基本的な「仕様」が以下のように示されている。

1.  負荷共有
2.  メッセージサービス
3.  情報の共有
4.  プログラム共有
5.  遠隔ログイン

タイムシェアリングシステム本体にコミュニケーションの管理を行わせる事に対してはコンピュータの管理者から否定的な意見が出されていた。このためロバーツはリンカーン研究所のの助言を受け入れタイムシェアリングシステムにコミュニケーションの管理を専門に行わせる小さいコンピュータを接続させることにした。この結果開発されたのが、現在の[ルーター](../Page/ルーター.md "wikilink")の前身ともいえる[Interface Message Processor](../Page/Interface_Message_Processor.md "wikilink")（IMP）である。

1968年中ごろまでにテイラーはコンピュータネットワークの計画を完成させ、ARPAの承認を得た。そして、契約者となる可能性のある140の組織などに見積依頼を送った。多くのコンピュータ企業はARPAとテイラーの提案を絵空事だとみなして考慮せず、送り返されてきたネットワーク構築の見積もりは12だけだった。ARPAはそこから4社を契約候補に選んだ。同年末には2社に絞り込み、最終的に1969年4月7日、[BBNテクノロジーズ](../Page/BBNテクノロジーズ.md "wikilink")とネットワーク構築の請負契約を結んだ。BBNでは当初7人のチームを結成しフランク・ハートが指揮した。ARPAの見積依頼は技術的にも詳細で、チームはすぐさまネットワーク接続用のコンピュータを構築できた。BBNの提案したネットワークはARPAの計画に沿ったもので、IMPという小型コンピュータでネットワークを形成してIMPをゲートウェイ（今日の[ルーター](../Page/ルーター.md "wikilink")）として機能させ、ローカルなリソースと相互接続するというものだった。各サイトではIMPが[ストアアンドフォワード](../Page/ストアアンドフォワード.md "wikilink")型のパケット交換機として機能し、IMP同士は[モデム](https://ja.wikipedia.org/wiki/モデム "wikilink")を介して[専用線](../Page/専用線.md "wikilink")（当初50kbit/s）で相互接続した。ホストコンピュータとIMPは独自の[シリアル通信](https://ja.wikipedia.org/wiki/シリアル通信 "wikilink")インタフェースで接続された。このシステムのハードウェアとパケット交換ソフトウェアは、9カ月で設計・構築された\[13\]。

第一世代のIMPはBBNが[ハネウェル](../Page/ハネウェル.md "wikilink")のDDP-516というコンピュータをベースとして構築した。主記憶（[磁気コアメモリ](../Page/磁気コアメモリ.md "wikilink")）は24[キロバイト](../Page/キロバイト.md "wikilink")（拡張可能）で、16チャネルの Direct Multiplex Control (DMC) という[DMAユニットを備えていた](../Page/Direct_Memory_Access.md "wikilink")\[14\]。DMCはホストコンピュータやモデムとのインタフェースに使われた。フロントパネルのランプ群に加えて、DDP-516にはIMPの通信チャネルの状態を示す24個の表示ランプがある。IMPは最大4台のホストコンピュータを接続でき、最大6台のIMPと専用線で相互接続できる。パケット転送の機構は[ストアアンドフォワード](../Page/ストアアンドフォワード.md "wikilink")型として設計された。また、各ルータは2秒毎に経路情報を送信し、最小のトランジットタイムを持つ経路を評価すると共に、0.5秒毎に経路表を各送信先までのトランジットタイムを最小にするように更新する、動的なルーティング・アルゴリズムも実装された\[15\]。このアルゴリズムは以前にポール・バランが考案していたものであった。

ほぼ同じころ、他の人々も（それぞれ独自に）「パケット交換」について研究を行っており、まず1968年8月5日に[イギリス国立物理学研究所](https://ja.wikipedia.org/wiki/イギリス国立物理学研究所 "wikilink") (NPL) が公開デモンストレーションを行った\[16\]。

### 設計目的についての議論

ARPANETは[核攻撃](https://ja.wikipedia.org/wiki/核攻撃 "wikilink")にも耐えるよう設計されたネットワークだ、という言い伝えが広まっているが、[インターネット協会](https://ja.wikipedia.org/wiki/インターネット協会 "wikilink")は否定している。その方式が1960年代前半に[アメリカ空軍](https://ja.wikipedia.org/wiki/アメリカ空軍 "wikilink")の[シンクタンク](../Page/シンクタンク.md "wikilink")である[ランド研究所](../Page/ランド研究所.md "wikilink")の[ポール・バラン](../Page/ポール・バラン.md "wikilink")によって提唱された核攻撃下でも生き残れるコミュニケーション方式であるという点を持ち上げて冷戦構造全体の中で技術としての「インターネット」を議論するべきなのか、それともロバーツの言うとおりパケット通信はバランの研究とは全く関係の無い[イギリス国立物理学研究所](https://ja.wikipedia.org/wiki/イギリス国立物理学研究所 "wikilink")の[ドナルド・デービスの研究成果を反映したもので](https://ja.wikipedia.org/wiki/ドナルド・ワッツ・デービス "wikilink")「インターネット」の誕生は新しいコミュニケーションツールとしての側面から評価してよいという議論までかなりの幅が見られる。[インターネット協会](https://ja.wikipedia.org/wiki/インターネット協会 "wikilink")は *A Brief History of the Internet* の中でARPANETを生み出した技術的アイデアの融合について次のように記している。

> ARPANETが核戦争に耐えられるネットワーク構築と何らかの関係があると主張する間違った噂が始まったのは、[ランド研究所](../Page/ランド研究所.md "wikilink")の研究からである。ランド研究所では核戦争を考慮した秘密音声通信を研究していたが、ARPANETはそれとは全く無関係である。しかし、後の[インターネットワーキング](https://ja.wikipedia.org/wiki/インターネットワーキング "wikilink")作業の展開においては、ネットワークの大きな部分が失われてもインターネットワークが機能し続けるなど、その頑健性と生存可能性を強調したことがあるのも事実である。\[17\]

一方で、ARPANETの開発のほとんどの請求書に署名を行なったDARPAの副局長 (1967-1971)・局長（1971-1974）のステファン・J・ルカシックは次のように述べている。

> 目的は新しいコンピュータ技術を利用して、核の脅威に対する軍事的指揮と制御のニーズを満たし、米国の核兵器の存続可能な制御を達成し、軍事戦術と管理の意思決定を改善することでした。\[18\]

ARPANETは、ルーティングテーブルの分散計算や頻繁な再計算を組み込んだことでネットワークの存続可能性が向上したが、自動ルーティングは技術的に困難だった。また、下位ネットワークが失われても機能し続けるよう設計されているが、これは核攻撃を受けなかったとしても交換ノードとネットワークリンクの信頼性が低かったためである。ARPANET構築を促進させたリソース不足について、ARPA局長 (1965–1967) のチャールズ・ヘルツフェルトはつぎのように述べた。

> ARPANETは核攻撃に耐える指揮統制システムを作るために始まったのではない。そのようなシステムの構築は明らかに軍にとって大きな要望ではあったが、それはARPAの任務ではなかった。実際、我々がそれを試みていれば、厳しく批判されただろう。むしろARPANETは、わが国にある大規模で強力な研究用コンピュータの数が限られていて、それらを使いたいと思っている研究者の多くは地理的に離れたところにいるという我々の欲求不満が出発点である。\[19\]

ARPANETは、1990年まで、20年間軍隊によって運営された。\[20\]\[21\]

当時のIPTO責任者であったテイラーは、1994年7月にアメリカ・[タイム誌](https://ja.wikipedia.org/wiki/タイム誌 "wikilink")で、「インターネットは核攻撃下でのコミュニケーションの生き残りを想定して開発された」\[22\]という記事が掲載されたときに事実とは異なる旨、正式な抗議をタイム誌に対して行っている。

[パケット通信](../Page/パケット通信.md "wikilink")の先駆者[ポール・バラン](../Page/ポール・バラン.md "wikilink")は次のように述べている。

> テイラーはそれぞれ異なるマシンに接続したいくつかの端末を持っていた。彼が考え付いたのは、1つの端末がそれらコンピュータのどれとも接続できるネットワークを構築することだった。それがARPANETの本当の起源だ。当時、そういった相互接続の方法は未解決の問題だった。\[23\]

[村井純](../Page/村井純.md "wikilink")は、「ARPANETは軍事用に開発され、それが民間に転用された」という説に関し、「ARPA基金の方針が非主流非軍事だが将来性を求め、軍事直結の基金は国防総省と区別がある」、「アメリカ軍は湾岸戦争のとき、様々な通信技術を運用した結果、TCP/IP技術の高い有用性を初めて認識した」とコメントし、さらに「中東派遣軍総司令官の[ノーマン・シュワルツコフ](../Page/ノーマン・シュワルツコフ.md "wikilink")は技術を『禁輸にすべきだ』とまで言い出した」というエピソードとともに、次のように答えている。

> ARPANETが最初から軍の独占技術だったとしたら、こんなことをする必要はまったくなかったでしょう。それどころか、すべてが軍の機密情報として扱われ、インターネットはそれこそ誰も知らないものになっていたはずです。\[24\]\[25\]

### ARPANETの始動

ARPANETは、次の4カ所のIMPを相互接続する形で始まった\[26\]。

  - [カリフォルニア大学ロサンゼルス校](../Page/カリフォルニア大学ロサンゼルス校.md "wikilink") (UCLA) - [レナード・クラインロック](https://ja.wikipedia.org/wiki/レナード・クラインロック "wikilink")が Network Measurement Center を創設し、SDS Sigma 7 というコンピュータを最初にARPANETに接続した。
  - [スタンフォード研究所の](../Page/SRIインターナショナル.md "wikilink") Augmentation Research Center - [ダグラス・エンゲルバート](../Page/ダグラス・エンゲルバート.md "wikilink")が初期の重要な[ハイパーテキスト](../Page/ハイパーテキスト.md "wikilink")システムである[NLS](../Page/NLS.md "wikilink")を開発した場所である。ARPANETにはそのNLSが動作した [SDS 940](https://ja.wikipedia.org/wiki/SDS_940 "wikilink")（愛称は"Genie"）が最初に接続された。
  - [カリフォルニア大学サンタバーバラ校](../Page/カリフォルニア大学サンタバーバラ校.md "wikilink") (UCSB) - Culler-Fried Interactive Mathematics Center の[IBM](../Page/IBM.md "wikilink") [360/75](https://ja.wikipedia.org/wiki/System/360 "wikilink")（OSは[OS/MVT](https://ja.wikipedia.org/wiki/:en:Multiprogramming_with_a_Variable_number_of_Tasks "wikilink")）を接続した。
  - [ユタ大学](../Page/ユタ大学.md "wikilink")の計算機科学科 - [アイバン・サザランド](../Page/アイバン・サザランド.md "wikilink")がARPAからこちらに移ってきており、[DEC](../Page/ディジタル・イクイップメント・コーポレーション.md "wikilink") [PDP-10](../Page/PDP-10.md "wikilink")（OSは[TENEX](../Page/TOPS-20.md "wikilink")）を接続した。

発足当初のメンバーには以後のネットワークの歴史や文化に大きな影響を与えることになる[ジョン・ポステル](../Page/ジョン・ポステル.md "wikilink")や[ヴィント・サーフが含まれていた](../Page/ヴィントン・サーフ.md "wikilink")。

ARPANET上で最初に送信されたメッセージは、UCLAの学生プログラマであるチャーリー・クラインが送ったものである。1969年10月29日午後10:30、UCLAの Boelter Hall 3420号室からのことだった\[27\]。クラインは同大学の[SDS Sigma 7からスタンフォード研究所の](https://ja.wikipedia.org/wiki/:en:SDS_Sigma_7 "wikilink")[SDS 940へとメッセージを送った](https://ja.wikipedia.org/wiki/SDS_940 "wikilink")。その内容は "login:" というテキストだったが、"lo" まで送信したところでシステムがクラッシュした。したがってARPANET初のメッセージは実際には "lo" である。これは1文字ずつ送信元から送信先に対して電話確認を行いながらの送信であった。約1時間後クラッシュから復旧させ、当初のテキストメッセージ全体の送信を成功させた。ARPANETの恒久的リンクが確立したのは1969年11月21日のことで、UCLAとスタンフォード研究所のIMP間のことである。1969年12月5日には、4ノード相互のネットワークが完成した\[28\]。

### 発展と進化

[Arpanet_1974.svg](https://ja.wikipedia.org/wiki/File:Arpanet_1974.svg "fig:Arpanet_1974.svg") 1970年3月、[マサチューセッツ州](../Page/マサチューセッツ州.md "wikilink")[ケンブリッジにある](../Page/ケンブリッジ_\(マサチューセッツ州\).md "wikilink")[BBNにあるIMPが接続され](../Page/BBNテクノロジーズ.md "wikilink")、ARPANETはアメリカ東海岸にまで広がった。その後、1970年6月にはIMPが9台、1970年12月には13台、1971年9月には18台（この時点で接続ホスト数は大学や政府機関を含めて23台）、1972年8月には29台\[29\]\[30\]1973年9月には40台となった。1974年6月にはIMPが46台となり、1975年7月には57台のIMPが相互接続された。1981年までに213台のホストコンピュータが接続され、およそ20日に1台の割合で新たなホストが接続されるという状況になった\[31\]。

1973年、[NORSAR](https://ja.wikipedia.org/wiki/:en:NORSAR "wikilink") (Norwegian Seismic Array)\[32\]が人工衛星の通信リンクでARPANETと接続され、ノルウェーはアメリカ以外で初めてARPANETと接続した国となった\[33\]。また、同時期にロンドンのIMPも地上回線で接続されている。

1975年、ARPANETは稼働状態にあると宣言された。本来、高度な研究への出資が仕事であるARPAはこの時点で手を引き、[アメリカ国防情報システム局](../Page/アメリカ国防情報システム局.md "wikilink")が運営を引き継いだ\[34\]。

[1980年](https://ja.wikipedia.org/wiki/1980年 "wikilink")、ARPANET初の負荷適応型のリンクステート型ルーティングアルゴリズムである[BBN](../Page/BBNテクノロジーズ.md "wikilink") ARPANETルーティングアルゴリズムが[BBN社から提案され](../Page/BBNテクノロジーズ.md "wikilink")、実験が開始された。このアルゴリズムは実験開始直後に激しいルートフラッピングを起こし、負荷適応型ルーティングアルゴリズムの実運用が困難であることが世界で初めて知られるようになった。

[1981年](../Page/1981年.md "wikilink")、日本で初めてのARPANETとの接続は[東北大学](https://ja.wikipedia.org/wiki/東北大学 "wikilink")が[ALOHAnet](../Page/ALOHAnet.md "wikilink")に参加し、これを経由して接続されたのが最初であった\[35\]。これは米国本土までの距離に比較して、地理的にも近い[ハワイ](https://ja.wikipedia.org/wiki/ハワイ "wikilink")までの[専用線](../Page/専用線.md "wikilink")の料金が、より安価に済んだことも理由である。

1983年、ARPANETの[アメリカ軍](../Page/アメリカ軍.md "wikilink")関係部分を分離して、機密には分類されない軍事関係の通信を担う[MILNETとした](https://ja.wikipedia.org/wiki/:en:MILNET "wikilink")。その後これを包含する形で [Defense Data Network](https://ja.wikipedia.org/wiki/:en:Defense_Data_Network "wikilink") (DDN) として発展\[36\]。軍関連が分離したことで113ノードあったARPANETは68ノードに縮小している。MILNETは後に[NIPRNet](https://ja.wikipedia.org/wiki/NIPRNet "wikilink")となった。

### 規則とエチケット

政府とのつながりのため、ある種のトラフィックは抑制または禁止されていた。[MIT人工知能研究所](../Page/MIT人工知能研究所.md "wikilink")で発行された1982年のコンピューティングについてのハンドブックでは、ネットワークでのエチケットについて次のように記している\[37\]。

### 技術

1970年にはIMP間の回線として 230.4 kbit/s までをサポートしたが、コストと[IMPの処理能力を考えれば](../Page/Interface_Message_Processor.md "wikilink")、そこまでの通信容量を使い切ることはなかった。

1971年には、堅牢化をしない（そのため非常に軽量な）[Honeywell 316](https://ja.wikipedia.org/wiki/Honeywell_316 "wikilink") を使ったIMPが登場した。これは[端末サーバ](https://ja.wikipedia.org/wiki/端末サーバ "wikilink") Terminal Interface Processor (TIP) としても構成でき、ホストと最大63台の[ASCII](../Page/ASCII.md "wikilink")シリアル端末を接続できた\[38\]。316は516より集積化が進んでおり、安価で保守が容易だった。TIPとしての316は40kBの磁気コアメモリを搭載していた。メモリ容量は1973年に拡大され、IMP用には32kB、TIP用には56kBを搭載した。1981年、BBNは自社製のC/30というコンピュータ上で動作するIMPソフトウェアを導入した。

1983年、資金提供を行っていた国防省側の方針で、[NCP](../Page/Network_Control_Program.md "wikilink")\[39\]を[TCP/IP](../Page/インターネット・プロトコル・スイート.md "wikilink")\[40\]に切り換えることになり、ARPANETは初期のインターネットのサブネットとなった。これが今日のインターネットにおけるTCP/IPの使用にとって決定的な条件のひとつを作ったと考えられている。

### ARPANETの退役と後世への影響

[NSFNetの拡大にともなってARPANETは縮小していき](../Page/全米科学財団ネットワーク.md "wikilink")、IMPやTIPも消えていったが、一部のIMPは1989年までサービスを継続した\[41\]。

[BBNと](../Page/BBNテクノロジーズ.md "wikilink")[ARPAが共同で出版した](../Page/国防高等研究計画局.md "wikilink") *ARPANET Completion Report* では、次のように結論付けている。

1990年2月28日にARPANETが正式に退役した後、[ヴィントン・サーフ](../Page/ヴィントン・サーフ.md "wikilink")は「ARPANETの挽歌」(Requiem of the ARPANET) と題して、次のように哀悼の意を表した\[42\]。

1988年、UCLAの計算機科学教授[レナード・クラインロック](https://ja.wikipedia.org/wiki/レナード・クラインロック "wikilink")を議長とする委員会の国会への報告を受け、上院議員[アル・ゴア](../Page/アル・ゴア.md "wikilink")は [High Performance Computing and Communication Act of 1991](https://ja.wikipedia.org/wiki/:en:High_Performance_Computing_and_Communication_Act_of_1991 "wikilink") という法案を作成。この法案が1991年12月9日に可決され、[National Information Infrastructure](https://ja.wikipedia.org/wiki/:en:National_Information_Infrastructure "wikilink") (NII) が生まれ、これをアル・ゴアが「[情報スーパーハイウェイ](../Page/情報スーパーハイウェイ構想.md "wikilink")」と呼んだ。2009年、[IEEEマイルストーン](../Page/IEEEマイルストーン.md "wikilink")にARPANET関連で2件が選ばれた\[43\]\[44\]。

## ソフトウェアとプロトコル

1969年に始まったARPANETでの[ホスト間](https://ja.wikipedia.org/wiki/ホスト_\(ネットワーク\) "wikilink")[通信プロトコル](../Page/通信プロトコル.md "wikilink")は、[1822 protocol](https://ja.wikipedia.org/wiki/:en:BBN_Report_1822 "wikilink") であり、IMPへのメッセージ転送を定義したものである\[45\]。そのメッセージ形式は様々なコンピュータアーキテクチャにおいても曖昧さが生じないよう設計された。1822メッセージは、メッセージ種別、数値による[ホストアドレス](https://ja.wikipedia.org/wiki/ホストアドレス "wikilink")、データフィールドで構成される。データメッセージを他のホストに送信するには、送信側でデータの中身と宛先ホストのアドレスからメッセージをフォーマットし、1822ハードウェアインタフェースを通してそれを送信する。IMPはメッセージにある宛先アドレスに従って、IMP間でメッセージを転送したり、宛先ホストに配達したりする。最終的に宛先ホストにメッセージを配達したIMPは、*Ready for Next Message* (RFNM) を送信元のIMPに向けて[肯定応答](https://ja.wikipedia.org/wiki/肯定応答 "wikilink")として送信する。

現代のインターネットの[データグラム](https://ja.wikipedia.org/wiki/データグラム "wikilink")とは異なり、ARPANETは信頼性を持って1822メッセージを転送するよう設計されており、メッセージを喪失した場合はホストコンピュータにそれを通知するようになっていた。一方[IPは信頼できないプロトコルであり](https://ja.wikipedia.org/wiki/Internet_Protocol#信頼性 "wikilink")、その上の[TCPが信頼性を担っている](../Page/Transmission_Control_Protocol.md "wikilink")。それにもかかわらず、1822プロトコルは1つのホストコンピュータ内に複数の異なるアプリケーションがあって、複数のコネクションを扱おうとしたときにうまく処理できないことが判明した。これに対処したのが [Network Control Program](../Page/Network_Control_Program.md "wikilink") (NCP) で、各種ホストコンピュータの各種プロセス間で、信頼でき[フロー制御](https://ja.wikipedia.org/wiki/フロー制御 "wikilink")された双方向通信リンクを確立する標準手段を提供した。NCPインタフェースは[アプリケーションソフトウェア](../Page/アプリケーションソフトウェア.md "wikilink")がARPANET経由で接続することを可能にしており、上位層の[通信プロトコル](../Page/通信プロトコル.md "wikilink")を実装したものといえる。[OSI参照モデル](../Page/OSI参照モデル.md "wikilink")のようなプロトコルの階層化の初期の例である\[46\]。

1983年、[TCP/IPがNCPおよび](../Page/インターネット・プロトコル・スイート.md "wikilink")1822プロトコルに取って代わった\[47\]。

### ネットワークの応用

NCPが標準のネットワークサービスを提供したことで、単一のホストコンピュータ上で複数アプリケーションが動作可能になった。これにより、その上でアプリケーション層のプロトコルが下層とはある程度独立に動作できるようになり、各種応用が生まれることにつながった。1983年にARPANETがインターネットに移行した際、主なアプリケーションプロトコルもTCP/IP上に移植された。

  - 電子メール
    1971年、[BBNの](../Page/BBNテクノロジーズ.md "wikilink")[レイ・トムリンソン](../Page/レイ・トムリンソン.md "wikilink")が世界初のネットワーク経由の[電子メール](../Page/電子メール.md "wikilink")を送信した (RFC 524, RFC 561)\[48\]。1973年には、ARPANETのトラフィックの75%が電子メールだった。
  - ファイル転送
    1973年、[File Transfer Protocol](../Page/File_Transfer_Protocol.md "wikilink") (FTP) の仕様が定義され (RFC 354)、実装され、ARPANET上でのファイル転送が可能となった。
  - 音声トラフィック
    1977年、[Network Voice Protocol](https://ja.wikipedia.org/wiki/:en:Network_Voice_Protocol "wikilink") (NVP) の仕様が定義され (RFC 741)、実装されたが、技術的欠点があったため、ARPANET上で[電話会議](https://ja.wikipedia.org/wiki/電話会議 "wikilink")が機能することはなかった。現代の[VoIP](../Page/VoIP.md "wikilink")が登場するのは、そのずっと後のことである。

## 映画その他のメディアにおけるARPANET

### 当時の記録

  - \- 30分のドキュメンタリー映画。[フェルナンド・J・コルバト](../Page/フェルナンド・J・コルバト.md "wikilink")、[J・C・R・リックライダー](../Page/J・C・R・リックライダー.md "wikilink")、[ローレンス・ロバーツ](https://ja.wikipedia.org/wiki/ローレンス・ロバーツ "wikilink")、[ロバート・カーン](../Page/ロバート・カーン.md "wikilink")、[ドナルド・デービスらが出演している](https://ja.wikipedia.org/wiki/ドナルド・ワッツ・デービス "wikilink")。

  - *Scenario* (1985) - アメリカの[シチュエーション・コメディ](../Page/シチュエーション・コメディ.md "wikilink")番組 *[Benson](https://ja.wikipedia.org/wiki/:en:Benson_\(TV_series\) "wikilink")* の1エピソード（シーズン6、エピソード20）。ARPANETにアクセスするシーンがあり、アメリカの普通のテレビ番組で初めてARPANETが登場した\[49\]。

### 後世の作品

  - *[Let the Great World Spin](https://ja.wikipedia.org/wiki/:en:Let_the_Great_World_Spin "wikilink")* (2009) - の小説。[ワールドトレードセンターの](../Page/ワールドトレードセンター_\(ニューヨーク\).md "wikilink")2つのタワーの間を大道芸人[フィリップ・プティ](https://ja.wikipedia.org/wiki/フィリップ・プティ "wikilink")が綱渡りでわたる様子を聞くため、[パロアルトからARPANET経由でニューヨークの電話ボックスに接続するシーンがある](../Page/パロアルト_\(カリフォルニア州\).md "wikilink")。
  - 「[メタルギアソリッド3](../Page/メタルギアソリッド3.md "wikilink")」(2004) - ゲーム。シギントという登場人物はゲーム内で描かれた事件の後、ARPANET開発に携わったという設定である。
  - *[Blue Box](https://ja.wikipedia.org/wiki/:en:Blue_Box_\(Doctor_Who\) "wikilink")* (2003) - [ドクター・フー](https://ja.wikipedia.org/wiki/ドクター・フー "wikilink")の小説版。1981年が舞台となっており、2000年にはARPANETに400台のマシンが接続されているだろうと予言する人物が登場する。
  - 『[Xファイル](https://ja.wikipedia.org/wiki/Xファイル "wikilink")』では、ARPANETに言及するエピソードが多数存在し、多くの場合「ローン・ガンメン」が侵入（ハック）する。例えば "アンユージュアルサスペクツ"（シーズン４、エピソード3）がある。
  - 『[LAヴァイス](https://ja.wikipedia.org/wiki/LAヴァイス "wikilink")』(2009) - [トマス・ピンチョン](../Page/トマス・ピンチョン.md "wikilink")の小説。1970年ごろの南カリフォルニアが舞台で、"ARPAnet"にアクセスする人物が全編に渡って登場する。

## 脚注

## 参考文献

  -
  -
  -
  -
  -
  -
  -
  -
### 関係者インタビュー

  -
  -
  -
  -
  -
  -
### 技術的詳細

  -
  -
  -
  -
  -
  -
  -
  -
  -
  -
  -
## 関連項目

  - [インターネットの歴史](https://ja.wikipedia.org/wiki/インターネットの歴史 "wikilink")
  - [ミサイル・ギャップ論争](../Page/ミサイル・ギャップ論争.md "wikilink")
  - [スプートニク・ショック](../Page/スプートニク・ショック.md "wikilink")
  - [DARPA](../Page/国防高等研究計画局.md "wikilink")
  - [.arpa](../Page/.arpa.md "wikilink")
  - [ネットニュース](../Page/ネットニュース.md "wikilink")
  - [サイバーシン計画](../Page/サイバーシン計画.md "wikilink")
  - [SRIインターナショナル](../Page/SRIインターナショナル.md "wikilink")

## 外部リンク

  -
  -
  - 年表

  -
  - \- ARPANET上の最初のメッセージに関する逸話

  -
  - 年表

[Category:インターネットの歴史](https://ja.wikipedia.org/wiki/Category:インターネットの歴史 "wikilink") [Category:UNIXに関連する組織](https://ja.wikipedia.org/wiki/Category:UNIXに関連する組織 "wikilink") [Category:国防高等研究計画局](https://ja.wikipedia.org/wiki/Category:国防高等研究計画局 "wikilink")

1.  <http://www.thocp.net/biographies/davies_donald.htm>
2.  <http://www.internethalloffame.org/inductees/donald-davies>
3.
4.  ["Packet Switching History"](http://www.livinginternet.com/i/iw_packet_inv.htm), Living Internet, retrieved 26 August 2012
5.  [](http://medg.lcs.mit.edu/people/psz/Licklider.html) 「人間とコンピュータの共生」 1960年3月
6.
7.  [](http://www.kurzweilai.net/meme/frame.html?main=/articles/art0366.html?m%3D7)「銀河間コンピュータネットワークメモランダム」 1963年4月
8.  「[](http://www.livinginternet.com/i/ii_licklider.htm)」リビング・インターネット
9.  ["IPTO – Information Processing Techniques Office"](http://www.livinginternet.com/i/ii_ipto.htm), Living Internet
10. [SAGE用コンピュータ](../Page/半自動式防空管制組織.md "wikilink")[AN/FSQ-7をトランジスタ化したもの](https://ja.wikipedia.org/wiki/:en:AN/FSQ-7 "wikilink")
11.
12. [*Multiple Computer Network and Intercomputer Communication*](http://www.lroberts.us/files/multi-net-inter-comm.html) 1967年
13. ["IMP – Interface Message Processor"](http://www.livinginternet.com/i/ii_imp.htm), Living Internet
14.
15. F. E. HEART, R. E. KAHN, S. 1\\II. ORNSTEIN, W. R. CROWTHER and D. C. WALDEN, <http://dl.acm.org/citation.cfm?id=1477021>, The interface message processor for the ARPA computer network, Spring Joint Computer Conference, 1970.
16.
17.
18.
19.
20. Janet Abbate (2000) *Inventing the Internet* pp.194-5
21. Vernon W. Ruttan (2005) [*Is War Necessary for Economic Growth?*](https://books.google.com/books?id=Eopn-pYI1tsC&pg=PA125) p.125
22. "[BATTLE FOR THE SOUL OF THE INTERNET](http://www.efc.ca/pages/time.25jul94.txt)". TIME, 1994年7月25日。
23.
24. 仕事インタビュー私の職務経歴書 第49回インターネットの父・村井純の場合 [1](http://c.filesend.to/ct/?p=8277&page=4「インターネットは軍事用に開発された」という間違った伝説)
25.
26. ["ARPANET – The First Internet"](http://www.livinginternet.com/i/ii_arpanet.htm), Living Internet
27.
28.
29. 当時の伝送速度は50kbpsの専用線。8096bit以下で１パケットを構成する。
30. 1972年12月には接続数が45台だったという（全部を示した接続系統図がある）。当時の伝送速度は50kbpsの専用線。
31.
32. 地震波を検出するため、アメリカとノルウェーが合意して建設した基地
33.
34.
35.
36.
37.
38.
39. ["NCP – Network Control Program"](http://www.livinginternet.com/i/ii_ncp.htm), Living Internet
40. ["TCP/IP Internet Protocol"](http://www.livinginternet.com/i/ii_tcpip.htm), Living Internet
41. ["NSFNET – National Science Foundation Network"](http://www.livinginternet.com/i/ii_nsfnet.htm), Living Internet
42.
43.
44.
45. [*Interface Message Processor: Specifications for the Interconnection of a Host and an IMP*](http://www.bitsavers.org/pdf/bbn/imp/BBN1822_Jan1976.pdf), Report No. 1822, Bolt Beranek and Newman, Inc. (BBN)
46.
47.
48.
49. ["Scenario"](http://www.imdb.com/title/tt0789851/), *Benson*, Season 6, Episode 132 of 158, American Broadcasting Company (ABC), Witt/Thomas/Harris Productions, 22 February 1985
> この記事は[Berkeley Open Infrastructure for Network Computing](https://ja.wikipedia.org/wiki/Berkeley_Open_Infrastructure_for_Network_Computing)から翻訳されています。


**Berkeley Open Infrastructure for Network Computing**（バークレー オープン インフラストラクチャ フォー ネットワーク コンピューティング）とは、[分散コンピューティング](../Page/分散コンピューティング.md "wikilink")プロジェクトの[プラットフォームとして](../Page/プラットフォーム_\(コンピューティング\).md "wikilink")[開発](../Page/開発.md "wikilink")された[クライアント・サーバ型の](../Page/クライアントサーバモデル.md "wikilink")[ソフトウェア](../Page/ソフトウェア.md "wikilink")である。開発元は[カリフォルニア大学バークレー校](../Page/カリフォルニア大学バークレー校.md "wikilink")。略称は **BOINC**。

[SETI@home](../Page/SETI@home.md "wikilink") の運用実績をもとに、より柔軟で汎用的なシステムを目指している。BOINC の公開後、SETI@home は BOINC ベースへと移行し、BOINC を使用しない単独プログラム用 SETI@home は[2005年](../Page/2005年.md "wikilink")[12月](https://ja.wikipedia.org/wiki/12月 "wikilink")に運用を終了した。

BOINCはその開発に際し、[アメリカ国立科学財団](../Page/アメリカ国立科学財団.md "wikilink")（NSF）の支援を受けている。(認可番号 AST-0307956 および SPNR 0138346)

## BOINC の特徴

### 参加者側からみた特徴

参加者が最初に導入するのは、後述する*' BOINC クライアント*'であるが、ここではクライアント側ソフトウェアの構造から説明を始める。 まず、参加者側に配置される[クライアント](../Page/クライアント_\(コンピュータ\).md "wikilink")・ソフトウェアが稼動するのに必須な部分は以下の2つである。

  - (a) **アプリケーション**: [分散コンピューティング](../Page/分散コンピューティング.md "wikilink")・プロジェクトのそれぞれが目的とする計算をする部分
  - (b) **コア・クライアント**: どのプロジェクトでも使う共通部分（運用サーバとの送受信機能や 上記の(a)部分から呼び出すライブラリ機能）

前者(a)**アプリケーション**は、各プロジェクトのサーバから参加者側へダウンロードされて複数プロジェクトが共存できる。

上記の必須部分 (a)+(b) に加えて、操作を楽にするための GUI が追加できる。GUI 部分と、(a)、そして(b)はこのように構造上分離されているが、今ではほとんどのプラットフォーム向けにそれぞれ GUI が用意されている。このため参加者からみると GUI がオプションであるとは意識されていないことがほとんどである。配布に際しても (b)**コア・クライアント**と GUI は一体として配られているので、コア・クライアント+ GUI を*' BOINC クライアント*'と呼ぶことが多い。つまり、

  - (c) *' BOINC クライアント*': コア・クライアント+ GUI 部分

である。たとえば、[Windows用や](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")、[macOS](https://ja.wikipedia.org/wiki/macOS "wikilink")用の標準[GUI版の](https://ja.wikipedia.org/wiki/グラフィカルユーザインターフェース "wikilink") BOINC クライアントがある。GUI の中には、機能を絞ったシンプルな画面と細かい操作のできる Advanced View の 2層構造になっているものもある。 **コア・クライアント**には、スクリーンセイバーを組込む仕組みが用意されており、旧来の SETI@home でもあったようなグラフィカルな動作画面が表示される。スクリーンセイバーは **アプリケーション**ごとに用意するものなので、スクリーンセイバーが表示されないプロジェクトもある。以下では**BOINC クライアント**を、主にコア・クライアント + GUI の意味で使うが、さらにおおまかに、(a)も集合的に含めたクライアント側ソフトウェア全体を意味することもある。

BOINC ベースの分散コンピューティングプロジェクトへの参加者は、まず BOINC クライアントを入手し、プロジェクトへの参加登録は BOINC クライアントを通じて行う \[1\]。参加登録が終わるとただちにそのプロジェクトのアプリケーションと最初の仕事が自動的にダウンロードされ、運用が始まる仕組みである。アプリケーションの新しいバージョンがリリースされた際も、BOINC クライアントが自動的にダウンロードする。稼動の一時停止や再開、プロジェクトからの脱退は、BOINC クライアント上で指示できる。

複数のプロジェクトに同時に参加する場合も、BOINC クライアント上から参加手続きをすればよい。同時に稼動できるプロジェクトは CPUコア1つ(INTELCPUのHTが有効時は二分の一つ)につき一プロジェクトのみだが、一定時間ごとに BOINC クライアントが自動的にプロジェクトを切り替える。

BOINC クライアントの設定や各プロジェクトの設定、プロジェクト間の稼動比率の設定は、現状では BOINC クライアント上からは設定できない。プロジェクトのウェブサイトに設けられたユーザーページ上で設定変更し、後ほど変更情報を BOINC クライアントに取り込む方法が採られている。

### プロジェクト側からみた特徴

サーバ運用の手法が確立しているため、新たにプロジェクトを起こす際に一から[インフラ部分を整備する労力を要しない](../Page/インフラストラクチャー.md "wikilink")。また、関連プログラムは[オープンソース](../Page/オープンソース.md "wikilink")化されている。

SETI@home で得られた分散コンピューティングの運用ノウハウを他の科学研究にも役立てることを主眼としているため、サーバ運用の省力化を念頭に置いて開発されている。通常、分散コンピューティングでは計算結果の信頼性を高めるため、同一の仕事を複数の参加者に配布して返却された計算結果を比較している。この、仕事の複製 → 配布 → 計算結果の回収 → 真偽判定 → 参加者への功績値の付与 → 不要ファイルの抹消、という一連の運用が自動化されている。

旧SETI@home では、終了直前の仕事を複製しておき不正に功績値を稼ぐ[チート](../Page/チート.md "wikilink")行為が問題となったが、個々の仕事がどの参加者のどのコンピュータに配布されたかを把握している BOINC ではこのようなことはない。

BOINC クライアントでは、自身が走っているコンピュータの情報を細かく調べてプロジェクト側に申告している。これにより、特定のプラットフォームや CPU の計算能力、プロジェクトに提供するメモリやハードディスク容量の多寡によって、参加の可否や配布する仕事の軽重を選択できるようになっている。

## アーキテクチャ

BOINCは、プロジェクト主催者が運営するサーバに対し、参加マシンはコアクライアントを通して[HTTPを用いてアプリケーションおよび計算ユニットを取得し](../Page/Hypertext_Transfer_Protocol.md "wikilink")、ローカルに処理するモデルとなっている。

幅広くボランティアを募って行うプロジェクトの場合、扱うデータ量に対するCPUによる計算量の比が大きい処理が好ましい。商用インターネット接続はコストが掛かりまたネットワーク帯域が必ずしも広くないため、特に一日あたり1Gバイト以上のデータを送受信するようなアプリケーションでは、自組織内のコンピュータクラスタを用いたほうが安価である\[2\]。

### プロジェクトサーバ

プロジェクト主催者のサーバは、次のような構成をとる。

  - プロジェクト バックエンドサーバ
      -
        参加クライアントに配布するプログラムや計算ユニットをデータサーバに供給する、また参加者から送られてきた計算結果を処理するサーバ
  - BOINCサーバ群
      - スケジューリングサーバ群
          -
            参加クライアントと通信を行う。
      - 計算ユニット、計算結果、参加者アカウントを管理する[関係データベース](https://ja.wikipedia.org/wiki/関係データベース "wikilink")サーバ
      - バックエンドサーバとBOINCサーバ群を連携するユーティリティ
      - プロジェクト参加者や開発者のためのWebインタフェース
      - データサーバ群
          -
            参加クライアントへのファイル配信と計算結果の収集を行う。これらの通信は[HTTPを使って行う](../Page/Hypertext_Transfer_Protocol.md "wikilink")。

### アプリケーション

## 歴史

  - 2000年 - SETI@homeの今後の計画として、SETI@home IIを計画中であることを表明。
  - 2002年8月 - BOINCを開発中であることを表明。
  - 2003年4月 - [United Devices社](../Page/United_Devices.md "wikilink")(UD)から、BOINCのソースコードの公開差し止めを求めて訴訟を起こされる。開発主任のデビッド・アンダーソン博士がかつてUD社に勤めていたことを理由に、UD社の企業秘密を流用してUD社の脅威となるソフトウェアを開発していると主張。
  - 2003年7月 - UD社との和解が成立。完全なオープンソースでの配布を断念し、商用利用を不可とするライセンスにすることで合意。\[3\]
  - 2004年6月 - SETI@home/BOINCを一般公開。
  - 2004年6月 - Climateprediction.netがBOINCを採用。
  - 2004年6月 - Predictor@homeがBOINCを採用。
  - 2004年9月 - LHC@homeがBOINCを採用。
  - 2004年11月 - Einstein@HomeがBOINCを採用。
  - 2005年1月 - UD社との和解が期限切れを迎え、[Lesser GPLのライセンスでの配布が可能となる](../Page/GNU_Lesser_General_Public_License.md "wikilink")。
  - 2005年6月 - Rosetta@homeがBOINCを採用。
  - 2005年6月 - SETI@homeのウェブサイトをSETI@home/BOINCのものに差し替え。半年の移行期間を設けてSETI@homeクラシックを運用終了することを宣言。
  - 2005年11月 - SETI@homeクラシックを1ヶ月後に運用終了すると表明。
  - 2005年12月 - SETI@homeクラシックが運用終了。
  - 2013年7月 - Android用BOINCクライアント公開\[4\]\[5\]。

## プロジェクト一覧

### 現在アカウント作成・稼働可能なもの

オープンβのプロジェクトも含む。

#### 天文学

  - [Einstein@home](https://ja.wikipedia.org/wiki/Einstein@home "wikilink")

      - [重力波の検出を試みる](../Page/重力波_\(相対論\).md "wikilink")。

  -   - [宇宙マイクロ波背景放射の非等方性についての研究](https://ja.wikipedia.org/wiki/宇宙背景放射 "wikilink")。観測結果により良く適合する[宇宙モデル](https://ja.wikipedia.org/wiki/宇宙モデル "wikilink")を構築する。

  - [MilkyWay@home](https://ja.wikipedia.org/wiki/MilkyWay@home "wikilink")

      - [天の川銀河の進化モデルを構築](../Page/銀河系.md "wikilink")。[スローン・デジタル・スカイサーベイ](https://ja.wikipedia.org/wiki/スローン・デジタル・スカイサーベイ "wikilink")\[[http://www.sdss.org/\]によってもたらされたデータを基とし、天の川銀河の精密な三次元モデルを構築する。また、銀河同士の衝突により天の川銀河が作られた過程や渦巻構造が作られた方法についての知見を得る](http://www.sdss.org/%5Dによってもたらされたデータを基とし、天の川銀河の精密な三次元モデルを構築する。また、銀河同士の衝突により天の川銀河が作られた過程や渦巻構造が作られた方法についての知見を得る)。

  - [Orbit@home](https://ja.wikipedia.org/wiki/Orbit@home "wikilink")

      - [地球近傍小惑星](../Page/地球近傍小惑星.md "wikilink")の[軌道をモニタリング](../Page/軌道_\(力学\).md "wikilink")。

  - [SETI@home](../Page/SETI@home.md "wikilink")

      - [地球外知的生命体探査](../Page/地球外知的生命体探査.md "wikilink")。[天球](../Page/天球.md "wikilink")上の一点から届く狭帯域信号を検出する。
      - SETI@home beta
          - SETI@home 次期バージョンの[ベータ版](../Page/ベータ版.md "wikilink")。

#### 気候学

  -   - 長期的気候予測技術の改善・[気候変動](../Page/気候変動.md "wikilink")調査
      - CPDN Beta
          - Climateprediction.net 次期バージョンのβテスト。

#### 地震学

  - [Quake-Catcher Network Seismic Monitoring](https://ja.wikipedia.org/wiki/Quake-Catcher_Network "wikilink")
      - 簡易[地震計](../Page/地震計.md "wikilink")ネットワークを構築する。

#### 数学

  - [Collatz Conjecture](http://boinc.thesonntags.com/collatz/)

      - [数論](../Page/数論.md "wikilink")の未解決問題の一つ、[コラッツの問題](../Page/コラッツの問題.md "wikilink")を解決する。

  - [Goldbach's Conjecture](http://goldbach.pl/)

      - [ゴールドバッハの予想](../Page/ゴールドバッハの予想.md "wikilink")で2\*10^1346以下のものを解く。

  - [PrimeGrid](https://ja.wikipedia.org/wiki/PrimeGrid "wikilink")

      - [素数](../Page/素数.md "wikilink")探索全般。

  - [Rectilinear Crossing Number](http://dist.ist.tugraz.at/cape5/)

      - 幾何学的な命題のひとつ、線分の交わる個数の最も少なくなるような頂点の配置を求める。

  -   - 11次元までの一般化された2進数系 (generalized binary number system) の探索。

  - WEP-M+2

      - [メルセンヌ数](../Page/メルセンヌ数.md "wikilink")+2の形式の素数を探索。

#### 物理学

  - [AQUA@home](https://ja.wikipedia.org/wiki/AQUA@home "wikilink")
      - 超伝導断熱量子コンピュータの性能予測。
  - [LHC@home](https://ja.wikipedia.org/wiki/LHC@home "wikilink")
      - [粒子加速器](https://ja.wikipedia.org/wiki/粒子加速器 "wikilink")の改善。[欧州原子核研究機構](../Page/欧州原子核研究機構.md "wikilink") (CERN) の[大型ハドロン衝突型加速器](../Page/大型ハドロン衝突型加速器.md "wikilink") (LHC) の稼動シミュレーションを行う。
  - [μFluids@Home](https://ja.wikipedia.org/wiki/μFluids@Home "wikilink")
      - [微小重力状態での](../Page/無重量状態.md "wikilink")[流体工学研究](../Page/流体力学.md "wikilink")。

#### 化学

  - [Hydrogen@home](http://hydrogenathome.org/)

      - [水素](https://ja.wikipedia.org/wiki/水素 "wikilink")生産の研究。

  -   - [古典力学](../Page/古典力学.md "wikilink")全般。現在は[分子動力学法](../Page/分子動力学法.md "wikilink")に基づく水分子の運動モデルの検証が主。

  - [Magnetism@home](http://kinetic.dnsalias.org/magnetism/)

      - ナノスケールの磁気現象を研究。

  -   - [モンテカルロ法](../Page/モンテカルロ法.md "wikilink")を用いて[量子化学](../Page/量子化学.md "wikilink")方程式を解く。

  -   - [分子磁石](https://ja.wikipedia.org/wiki/分子磁石 "wikilink")およびナノスケールの磁気現象を研究。

#### 構造生物学

  - [Docking@Home](https://ja.wikipedia.org/wiki/Docking@Home "wikilink")

      - タンパク質の[リガンド](https://ja.wikipedia.org/wiki/リガンド "wikilink")を探索、および探索方法そのものの新規開拓。

  - [GPUGRID](https://ja.wikipedia.org/wiki/GPUGRID "wikilink")

      - [CUDA](../Page/CUDA.md "wikilink")対応の[GPUやLinuxを導入した](../Page/Graphics_Processing_Unit.md "wikilink")[プレイステーション3を用いて](https://ja.wikipedia.org/wiki/PlayStation_3 "wikilink")[分子動力学に基づくシミュレーションを行う](../Page/分子動力学法.md "wikilink")。

  -   - [タンパク質構造予測](../Page/タンパク質構造予測.md "wikilink")。

  -   - タンパク質構造予測。

  - [Rosetta@home](https://ja.wikipedia.org/wiki/Rosetta@home "wikilink")

      - タンパク質構造予測。
      - RALPH@home
          - Rosetta@home次期バージョンのαテスト。

  - [SIMAP](https://ja.wikipedia.org/wiki/SIMAP "wikilink")

      - タンパク質の[相似性データベースの構築](https://ja.wikipedia.org/wiki/相似#生物における相似 "wikilink")。

  -   - タンパク質構造予測、ほか[分子生物学](../Page/分子生物学.md "wikilink")全般。

#### 分子生物学

  - [Superlink@Technion](http://cbl-boinc-server2.cs.technion.ac.il/superlinkattechnion/)
      - [糖尿病](../Page/糖尿病.md "wikilink")、[高血圧](../Page/高血圧.md "wikilink")、[癌](../Page/悪性腫瘍.md "wikilink")、[統合失調症](https://ja.wikipedia.org/wiki/統合失調症 "wikilink")などの原因となる[遺伝子](https://ja.wikipedia.org/wiki/遺伝子 "wikilink")を発見する。

#### 疫学

  - [Malaria Control Project](https://ja.wikipedia.org/wiki/Malaria_Control_Project "wikilink")
      - [臨床疫学](https://ja.wikipedia.org/wiki/臨床疫学 "wikilink")の確率論的なモデリング。

#### 認知科学

  -   - MindModeling@homeのβテスト。[ACT-R](../Page/ACT-R.md "wikilink")上での認知モデルの構築とその評価を行う。

#### 計算機科学

  - [DistrRTgen](http://boinc.freerainbowtables.com/distrrtgen/)
      - [ハッシュ関数](../Page/ハッシュ関数.md "wikilink")の逆引きを可能とする、巨大な[レインボーテーブル](../Page/レインボーテーブル.md "wikilink")の作成。
  - [Enigma@home](http://www.enigmaathome.net/)
      - [M4 ProjectにBOINCクライアントから参加できるように仲介するラッピングプロジェクト](https://ja.wikipedia.org/wiki/M4_Project "wikilink")。ナチス・ドイツの暗号機「[エニグマ](../Page/エニグマ_\(暗号機\).md "wikilink")」で作成された未解読の暗号文を解読する。
  - [FreeHAL@home](http://freehal.net/freehal_at_home/)
      - [人工無能](https://ja.wikipedia.org/wiki/人工無能 "wikilink")の研究。構文解析やタグ付けを行っている。
  - [Genetic Life](http://genlife.is-a-geek.org/genlife/)
      - [進化的アルゴリズム](../Page/進化的アルゴリズム.md "wikilink")の研究。[Tierraを分散コンピューティング上で動作させる](../Page/Tierra_\(コンピュータプログラム\).md "wikilink")。
  - [SHA-1 Collision Search Graz](http://boinc.iaik.tugraz.at/sha1_coll_search)
      - [SHA-1](https://ja.wikipedia.org/wiki/SHA-1 "wikilink")[ハッシュ関数](../Page/ハッシュ関数.md "wikilink")の脆弱性を見つけ出す。

#### アニメーションレンダリング

  -   - 3Dアニメーション[レンダリングの公共システム開発](../Page/レンダリング_\(コンピュータ\).md "wikilink")。

#### パズル

  - [NQueens Project](http://nqueens.ing.udec.cl/)
      - チェスの盤面を使ったパズル「[Nクイーン問題](../Page/エイト・クイーン.md "wikilink")」の解を求める。
  - [Sudoku](http://dist2.ist.tugraz.at/sudoku/)
      - [ペンシルパズル](../Page/ペンシルパズル.md "wikilink")の[ナンバープレース（数独）における数学的命題](../Page/数独.md "wikilink")、問題として成立する最も少ない初期配置を求める。

#### テスト、その他

  - [Gerasim@home](http://www.gerasim.boinc.ru/Gerasim/)
  - Pirates@Home
      - テストプロジェクト。もともとはEinstein@homeのスクリーンセーバ用画像を制作するプロジェクトだったが、現在は分散コンピューティングについて理解するための学習教材に転用されている。
  - [VTU@home](http://boinc.vgtu.lt/vtuathome/)
      - テストプロジェクト。本格的なプロジェクトを立ち上げる前の運用習熟で、素因数分解の単純な総当り式による素数探索を行うダミーワークが配布されている。

#### オムニバス

  - World Community Grid

      - [\#World Community Gridを参照](https://ja.wikipedia.org/wiki/#World_Community_Grid "wikilink")。

  - [yoyo@home](http://www.rechenkraft.net/yoyo/)

      - BOINCを採用していない分散コンピューティングプロジェクトに対し、BOINC クライアントで参加できるよう仲介するラッピングプロジェクト。以下のプロジェクトに対応している。

      - [distributed.net](https://ja.wikipedia.org/wiki/distributed.net "wikilink") の OGR (最短ゴロム定規) 探索プロジェクト

          - 最短[ゴロム定規](https://ja.wikipedia.org/wiki/ゴロム定規 "wikilink")を求める。

      - ECM

          - [素因数分解](../Page/素因数分解.md "wikilink")のに関する研究。

      -   - [進化](../Page/進化.md "wikilink")の研究。[マラーのラチェットの定量化を試みる](https://ja.wikipedia.org/wiki/有性生殖#マラーのラチェット "wikilink")。

      - Muon1 Distributed Particle Accelerator Design

          - [ミュー粒子](../Page/ミュー粒子.md "wikilink")の研究。粒子加速器のシミュレーションを行う。

  -   - 複数の分散コンピューティングの受け皿となるプロジェクト。
      - adsorcion
      - docking
      - fusion
      - nanoluz
      - nanotest
      - neurosim
      - materiales (16、32、64、128、24、48)

  - [AlmereGrid Boinc Grid](http://boinc.almeregrid.nl/)

      - 複数の分散コンピューティングの受け皿となるプロジェクト。世界最初の**市営**分散コンピューティングプロジェクトでもある。運営元はオランダ・[フレヴォラント州](../Page/フレヴォラント州.md "wikilink")にある町[アルメレ](../Page/アルメレ.md "wikilink")である。
      - [AlmereGrid TestGrid](http://server1.almeregrid.nl/testgrid/)
          - AlmereGridのαテスト
      - Statistical analysis of twins - test version

### 参加者の募集を停止中のもの

クローズドβ、あるいは参加者数を限定して運用しているプロジェクト群。

  - [Chess960@home](http://www.chess960athome.org/alpha/)
      - [変則チェス](../Page/変則チェス.md "wikilink")の一種、[チェス960](../Page/チェス960.md "wikilink")での[定跡を探る](../Page/定石.md "wikilink")。
  - [Climateprediction.net Beta](http://climateapps1.oucs.ox.ac.uk/beta/)
      - Climateprediction.net次期バージョンのβテスト。オープンβは別サイトに移動した。
  - [IMP@home](http://impfarm.imp.org/boinc/)
      - 既に終了したプロジェクトIMPFarmの後続。
  - [BRaTS@home](http://maxwell.dhcp.umsl.edu/brats/)
      - [重力レンズ](../Page/重力レンズ.md "wikilink")風の視覚効果を用いた[レイトレーシング](../Page/レイトレーシング.md "wikilink")を作成。
  - [Superlink@clusters](http://cbl-boinc-server1.cs.technion.ac.il/superlinkatclusters/)
      - Superlink@Technionのαテスト。一般の参加はできない。
  - [MindModeling@home](http://mindmodeling.org/boinc/)
      - [認知科学](../Page/認知科学.md "wikilink")の研究。[ACT-R](../Page/ACT-R.md "wikilink")上での認知モデルの構築とその評価を行う。現在はβテスト専用のプロジェクトでのみ運用。
  - [BOINC Alpha](http://isaac.ssl.berkeley.edu/alpha/)
      - BOINC自体のαテスト。一般の参加はできない。
  - [DockTest@Home](http://docktest.cis.udel.edu/)
      - Docking@Homeのテスト。

### 運用にむけて準備中のもの

参加者登録は可能なものの、まだワークの配布が始まっていないプロジェクト。

  - [NCSSM Grid Computing Project](http://grid.ncssm.edu/ncssm_grid/)
  - [NNSIMU Project](http://193.144.240.190/nnsimu/)
  - [Satisfaction@home](http://sat.math.umu.se/sat/)
  - [DECS](http://evil.podzone.org/decs/)
  - [MapTheGap Project](http://www.mapthegap.com/)
  - [CancerGrid](http://cancergrid.lpds.sztaki.hu/cancergrid/)
  - [Bioinfo@Home](http://140.110.240.195/bioinfo/)
  - [Prob](http://sctr.i3a.uclm.es/prob/)
  - [EON](http://eon.raunvis.hi.is/EON2v1/)
  - [EAPS@HOME](http://eaps-at-home-alpha.gotdns.org/eaps/)
  - [UNCW's Distributed Data Analysis System](http://elm.cis.uncw.edu/ddas/)
  - [Volunteer Computing Platform](http://202.191.56.60/VCP/)

### 活動を休止中のもの

長期に渡って運用停止していたり、運営側が休止を宣言したプロジェクト。

  - [ABC@home](https://ja.wikipedia.org/wiki/ABC@home "wikilink")

      - [数学上の未解決問題](../Page/数学上の未解決問題.md "wikilink")の一つ、[ABC予想](https://ja.wikipedia.org/wiki/ABC予想 "wikilink")を解く。

  - [APS@home](http://www.apsathome.org/)

      - 生態系から発するガスなどの流動体が、計測地点に到達するまでにどのような軌跡を辿ったかを求める。

  -   - 将来の大規模な[人工知能](../Page/人工知能.md "wikilink")システム構築の参考にするため、巨大な[ニューラルネットワーク](../Page/ニューラルネットワーク.md "wikilink")を構築する。

  - BBC Climate Change Experiment

      - [\#BBC Climate Change Experiment参照](https://ja.wikipedia.org/wiki/#BBC_Climate_Change_Experiment "wikilink")。

  - [BCL@Home](http://boinc.vanderbilt.edu/CSB/)

      - タンパク質構造予測。新薬候補の探索を主眼においている。

  - Cels@home

      - [細胞接着](../Page/細胞接着.md "wikilink")のメカニズムを、それを原因とした疾患（癌細胞の転移やウイルス感染、[HIV感染など](../Page/ヒト免疫不全ウイルス.md "wikilink")）を防止する観点から研究する。

  - [climateprediction.net Seasonal Attribution Project](http://attribution.cpdn.org/)

      - climateprediction.net の1プロジェクト。2000年秋に英国で発生した[洪水](../Page/洪水.md "wikilink")のシミュレーションを試みる。

  - [Cunning Plan](http://isaac.ssl.berkeley.edu/cplan/)

  - [DepSpid](http://www.depspid.net/)

      - [ウェブクローラーを分散コンピューティングで構築](../Page/クローラ.md "wikilink")。

  - Distributed Rainbow Table Generator

      - [ハッシュ関数](../Page/ハッシュ関数.md "wikilink")の逆引きを可能とする、巨大な[レインボーテーブル](../Page/レインボーテーブル.md "wikilink")の作成。

  - [EternityII.net](http://eternity2.net/)

      - 懸賞金の掛けられたパズルの早解きを行う。

  -   - [MD5](../Page/MD5.md "wikilink")ハッシュ関数の脆弱性を見つけ出す。

  - [NanoHive@home](http://www.nanohive-1.org/atHome/)

      - [ナノテクノロジー](../Page/ナノテクノロジー.md "wikilink")の研究。

  - pPot Tables

      - [ポーカー](../Page/ポーカー.md "wikilink") ([テキサス・ホールデム](../Page/テキサス・ホールデム.md "wikilink")) に強い[AIを作成するための](../Page/人工知能.md "wikilink")[ルックアップテーブル](../Page/ルックアップテーブル.md "wikilink")を構築する。

  -   - タンパク質構造予測。

  - Project Neuron

      - 分散コンピューティングプロジェクトの効率性評価手法の確立。

  - [Ramsey@home](http://www.ramseyathome.com/ramsey/)

      - [ラムゼー数の探索](../Page/ラムゼーの定理.md "wikilink")。

  - RenderFarm@home

      - アニメーションのレンダリングを行うプロジェクト。

  - Reversi

      - [リバーシの最善手を探索し](../Page/オセロ_\(遊戯\).md "wikilink")、完全に解くことを目指す。

  - [Riesel Sieve](https://ja.wikipedia.org/wiki/Riesel_Sieve "wikilink")

      - 509203よりも小さい[リーゼル数が存在するかを探索](https://ja.wikipedia.org/wiki/シェルピンスキー数#リーゼル数 "wikilink")。

  - RND@home

      - [無線基地局の効率よい配置](https://ja.wikipedia.org/wiki/基地局 "wikilink")・運用を行うためのシミュレーション。

  - [SciLINC](http://www.scilinc.org/SciLINC/)

      - [植物学](../Page/植物学.md "wikilink")に関する膨大な文献をデータベース化する。

  - [TANPAKU](https://ja.wikipedia.org/wiki/TANPAKU "wikilink")

      - タンパク質の構造と機能をを用いて研究。

  - [TSP](http://bob.myisland.as/tsp/)

      - [巡回セールスマン問題](../Page/巡回セールスマン問題.md "wikilink")の研究。[遺伝的アルゴリズム](../Page/遺伝的アルゴリズム.md "wikilink")のほか、さまざまな検索アルゴリズムをテストする。

  - [UCT : malariacontrol.net](http://boinc.cs.uct.ac.za/malaria/)

      - malariacontrol.netのβテスト。

  - [UH Second Computing](http://vcsc.cs.uh.edu/second-computing/)

      - 複数の分散コンピューティングの受け皿となるプロジェクト。

  - [Virtual Prairie](http://vcsc.cs.uh.edu/virtual-prairie/)

      - 広大な[プレーリー](../Page/プレーリー.md "wikilink")全体をシミュレートし、繰り返される放牧や伐採といった[擾乱](../Page/擾乱.md "wikilink")に対して生態学的にどれほどの復元力があるかの知見を得る。

  -   - 分散コンピューティングのパフォーマンス向上を目的とした BOINC 自体の研究・分析。

  - Zebra RSA Bruteforce

      - [スマートカード](https://ja.wikipedia.org/wiki/スマートカード "wikilink")で使われる[RSA暗号](../Page/RSA暗号.md "wikilink")を[ブルートフォース（総当たり）によって無力化](../Page/総当たり攻撃.md "wikilink")。

  - Zivis Superordenador Ciudadano

## BOINCの技術をベースにした分散コンピューティングプロジェクト

### World Community Grid

IBM社の支援の下、複数の医療系プロジェクトを展開している。既にいくつかのプロジェクトが完了、もしくはフェーズ2に移行している。[World Community Gridの項も参照のこと](../Page/World_Community_Grid.md "wikilink")。

[United Devices社のシステムで運用されているプロジェクトであったが](../Page/United_Devices.md "wikilink")、UD社のクライアントのサポートは2008年6月で中止され\[6\]、一方これと平行して2005年11月からBOINCクライアントからも参加できるようになり、現在はBOINCクライアントのみのサポートとなった\[7\]。当初は脇役的な扱いでBOINCからの参加方法も解りづらかったが、[grid.org](../Page/United_Devices_Cancer_Research_Project.md "wikilink") の終了前後から主客が逆転し、ウェブサイトでの参加登録後に現れるクライアントダウンロードページでも BOINCクライアントが上位に表示されるなど、UDクライアントの方が脇へと追いやられているという変遷もあった。

WCGサイトからの参加手続きは通常とは若干異なるが、これは初心者に対する配慮からWCGプロジェクトに参加した状態でのインストールになっていることによる。そのため、BOINCでWCGに参加する場合は、WCGサイトからインストールするのが最も簡単で手間がかからない。またBOINCクライアントは最新版が使用されており、インストール後にWCG以外のプロジェクトを追加する場合も特に制限はなく、別途BOINCに参加した人との差異はないと言って良い。

[2007年](../Page/2007年.md "wikilink")10月3日BOINCクライアントからの功績値は68.8%に達し、[2008年](https://ja.wikipedia.org/wiki/2008年 "wikilink")6月26日には100%となり、UDクライアントは使命を終えた。

特徴としてはBOINCでの功績値（クレジット）とは別に、過去のUDクライアントによる功績値との整合性を取る必要性からポイント（1クレジット＝7ポイント）による功績値集計を行っている。なおBOINC Stats等では、BOINCクライアントによる功績値のみが通常のクレジットで集計される。

グラフィック表示可能。（ただしグラフィックサイズは640×480px）

BOINCと違い、プロジェクト単位でのユーザー登録ではなく、World Community Gridで1つのアカウントを作成する仕組みである。1つのアカウントの元でWCG全てのプロジェクトに参加するか、個々のプロジェクトに参加するかの選択設定も行える。またWCGでは新規プロジェクトの始動と終了が比較的に頻繁に行われるが、新規プロジェクトを自動的に追加する設定がプロファイル設定に存在し、これにより自動で参加プロジェクトを増やせる。

  - FightAIDS@Home （[2005年](../Page/2005年.md "wikilink")[11月21日](../Page/11月21日.md "wikilink")発足）- [HIVの新しい候補薬の特定](../Page/ヒト免疫不全ウイルス.md "wikilink")。
  - Human Proteome Folding - Phase 2（ヒトたんぱく質解析フェーズ 2 [2006年](../Page/2006年.md "wikilink")[6月23日](../Page/6月23日.md "wikilink")発足） - 特定の[ヒト](../Page/人間.md "wikilink")・タンパク質と病原タンパク質の分解構造を得ることとタンパク質構造予測の限界探索。生物学的なことと生物物理的なことへも対処。
  - Help Conquer Cancer（がん撲滅支援 2007年[11月6日](../Page/11月6日.md "wikilink")発足） - [がん治療のためのたんぱく質解析](../Page/悪性腫瘍.md "wikilink")。
  - Help Fight Childhood Cancer（[ファイト\!小児がんプロジェクト](https://ja.wikipedia.org/wiki/ファイト!小児がんプロジェクト "wikilink") [2009年](../Page/2009年.md "wikilink")[3月16日](../Page/3月16日.md "wikilink")発足） - [神経芽腫に関連する](https://ja.wikipedia.org/wiki/神経芽細胞腫 "wikilink")3つの特定のタンパク質と、それを不活化させる為の薬剤候補との仮想結合実験。[千葉県がんセンター](https://ja.wikipedia.org/wiki/千葉県がんセンター "wikilink")及び[千葉大学](https://ja.wikipedia.org/wiki/千葉大学 "wikilink")の研究者が主宰。
  - Help Cure Muscular Dystrophy - Phase 2（[筋ジストロフィー](../Page/筋ジストロフィー.md "wikilink")治療支援フェーズ2 2009年[5月13日](../Page/5月13日.md "wikilink")発足） - 神経筋疾患を引き起こす遺伝子に対応するタンパク質の分子モデリング解析。
  - The Clean Energy Project - Phase （2010年6月30日発足） - 炭素ベースの光発電効率を高める新素材の探索。[ハーバード大学](https://ja.wikipedia.org/wiki/ハーバード大学 "wikilink")の化学・生物化学部が主催。当初はLinux版のみで開始。
  - Computing for Clean Water：（2010年9月20日発足） - 新たなフィルター素材での効率的な[水](../Page/水.md "wikilink")[分子](../Page/分子.md "wikilink")の流れの様相探索。低価格、高効率の水浄化フィルター開発を目標とする。
  - Drug Search for Leishmaniasis （2011年9月7日発足）- [リーシュマニア症](../Page/リーシュマニア症.md "wikilink")の治療法に結びつく有望な合成物の探索。[コロンビア](../Page/コロンビア.md "wikilink")共和国[メデジン](../Page/メデジン.md "wikilink")市の[アンティオキア大学](https://ja.wikipedia.org/wiki/アンティオキア大学 "wikilink")の研究者が主催。

なお、最新のプロジェクト状況については[World Community Gridを参照](../Page/World_Community_Grid.md "wikilink")。

### cell computing βirth

BOINCをベースに運用されている商用プロジェクト。2008年3月末をもってすべての活動を終了した。[cell computing βirthの項も参照のこと](../Page/Cell_computing.md "wikilink")。

BOINC標準クライアントからの参加はできないが、cell computing βirthのクライアントから各BOINCプロジェクトへの参加は可能。ただしクライアントがBOINCクライアント ver.4をベースとしているため、ver.5以降のクライアントを前提としたBOINCプロジェクトには参加できない。

  - CHRONOS
      - ヒトゲノム染色体間法則性解明プロジェクト

<!-- end list -->

  - sekigahara（セキガハラ）
      - 関ヶ原の合戦映像製作プロジェクト

### BBC Climate Change Experiment

ClimatePrediction.netの[BBC協賛版](../Page/英国放送協会.md "wikilink")。1920年から2080年までの160年間もの気候変動をシミュレートする。

ウェブサイトでは独自クライアントをダウンロードするよう誘導されるが、BOINC標準クライアントからも問題なく参加できる。

ワークの配布は2007年1月で打ち切られ、運用結果をもとにイギリス本国で特番が放映された。（ダイジェスト版は [YouTube](https://ja.wikipedia.org/wiki/YouTube "wikilink") で閲覧できる。\[8\]既に参加者登録は終了しており、現在は解析中ワークの返却のみ受け付けている。

## 関連項目

  - [分散コンピューティング](../Page/分散コンピューティング.md "wikilink")
  - [cell computing βirth](../Page/Cell_computing.md "wikilink")
  - [World Community Grid](../Page/World_Community_Grid.md "wikilink")

## 脚注

<references/>

## 外部リンク

  - [Berkeley Open Infrastructure for Network Computing](http://boinc.berkeley.edu/)
      - BOINC の開発元サイト。BOINC クライアントの配布のほか、BOINC に関する詳細な解説を参加者・プロジェクト運営者双方にむけて公開している。
  - SETI@homeによるBOINC開発時の記事
      - [Future directions of SETI@home](http://seticlassic.ssl.berkeley.edu/setifuture.html)([日本語訳](http://www.planetary.or.jp/setiathome/setifuture.html))
  - [惑星協会](../Page/惑星協会.md "wikilink")によるBOINC 開発時の記事
      - [SETI@homeが他の分野にインターネット分散コンピューティングをもたらす](http://www.planetary.or.jp/setiathome/UPDATES/Update_091602.htm)
      - [新しい，改良された SETI@home が分散コンピューティング ネットワークのバックボーンを形成するだろう](http://www.planetary.or.jp/setiathome/UPDATES/Update_092503.htm)

### チュートリアル(使い方の指導)

  - [Team 2ch - BOINC Team 2ch Wiki](http://team2ch.info/)
      - [2ちゃんねらー](../Page/2ちゃんねらー.md "wikilink")有志のチーム「[Team 2ch](../Page/Team2ch.md "wikilink")」のうち、[UDがん研究プロジェクトの運営終了をきっかけにBOINCに移ってきた一派が拠点とするサイト](../Page/United_Devices_Cancer_Research_Project.md "wikilink")。なお、SETI@homeクラシックからBOINCに移ってきた一派については別に拠点サイトがある。[2](http://setiathome.web.fc2.com/)

<!-- end list -->

  - [Flashを使った BOINC チュートリアル](http://www.kd-web.info/clanky.php)
  - [BOINCでの分散コンピューティング、BOINCとは](http://www.kameson.com/climateprediction.htm)

### 外部統計サイト

  - [BOINCstats](http://boincstats.com/)
      - 各 BOINC プロジェクトが XML データで提供する貢献値データを定期収集し、個人別・チーム別・国別でのランキング、貢献値獲得の履歴やランキング変動履歴の提供を行う統計サイトのひとつ。プロジェクト横断での功績値合算にも対応しており完成度が高い。
  - [All Project Stats](http://www.allprojectstats.com/)
  - [BOINC Statistics for the WORLD](http://www.boincsynergy.com/stats/)

[Category:分散コンピューティングプロジェクト](https://ja.wikipedia.org/wiki/Category:分散コンピューティングプロジェクト "wikilink") [Category:ネットワークソフト](https://ja.wikipedia.org/wiki/Category:ネットワークソフト "wikilink") [Category:GPGPU](https://ja.wikipedia.org/wiki/Category:GPGPU "wikilink") [Category:長大な項目名](https://ja.wikipedia.org/wiki/Category:長大な項目名 "wikilink")

1.  BOINC クライアントのバージョン4までは、まずプロジェクトのウェブサイト上で参加登録を行い、メールで送られてきたアカウントキーを BOINC クライアントに入力する必要があった。一部プラットフォームではバージョン5 以降の BOINC クライアントが提供されておらず、ウェブサイト上での参加登録ページは現在も残されている。
2.  [Overview of BOINC](http://boinc.berkeley.edu/trac/wiki/BoincIntro)
3.  [1](http://boinc.berkeley.edu/legal.html)
4.
5.
6.
7.
8.
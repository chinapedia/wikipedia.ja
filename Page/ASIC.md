> この記事は[ASIC](https://ja.wikipedia.org/wiki/ASIC)から翻訳されています。


[SSDTR-ASIC_technology.jpg](https://ja.wikipedia.org/wiki/File:SSDTR-ASIC_technology.jpg "fig:SSDTR-ASIC_technology.jpg") **ASIC**（、**特定用途向け集積回路**）は電子部品の種別の1つで、特定の用途向けに複数機能の回路を1つにまとめた[集積回路](../Page/集積回路.md "wikilink")の総称である。通常は「エーシック」と発音され、表記する場合は日本でも「ASIC」である。

## 概要

ASICは機密となる回路構成を隠し、故障しやすいデバイス同士の接続箇所を大幅に減らせ、実装面積及び大量生産時のコストを低減するために作られた。単機能ICと高性能演算用IC以外のほとんどすべての半導体製品を含んでいるため、多種多様なものが存在する。[デジタル回路](../Page/デジタル回路.md "wikilink")が一般的であるが、アナログ回路を含んだりアナログ回路だけのASICもある。[1990年代](../Page/1990年代.md "wikilink")後半よりDRAM内蔵も可能となりFlashメモリ搭載のASICなど各社の得意分野が分かれるようになってきた。

## 長所と短所

ASICは単体の半導体である[標準ロジックIC](https://ja.wikipedia.org/wiki/標準ロジックIC "wikilink")や標準メモリーIC、回路設計を書き換える[プログラマブルロジックデバイス](../Page/プログラマブルロジックデバイス.md "wikilink")や[FPGA](https://ja.wikipedia.org/wiki/FPGA "wikilink")などと比べて以下の点で優れている。

  - 実装面積の縮小
  - 消費電力の低減
  - 動作速度の向上
  - 単価が安い

以下の点が短所である。

  - 開発費が高い
  - 開発期間が長い
  - 回路設計の誤りの修正が困難（メタル修正や造り直し）

## 課題

  - 設計上の失敗時に[フォトマスク](https://ja.wikipedia.org/wiki/フォトマスク "wikilink")製作から作り直す費用と時間が非常に大きい。設計変更の多い機器には、本質的に不向きである
  - 高価な製造用フォトマスクなどによって、少量生産では単価が非常に高くなる
  - 製造工程に時間がかかり、納期が長い
  - 全てが個別設計のため設計に関わる人の人件費がコストを高める
  - 製造工程がいくぶん複雑になることによるコスト上昇がある

## 分類

  - [ゲートアレイ](https://ja.wikipedia.org/wiki/ゲートアレイ "wikilink") ()
    基本となる論理回路（ゲート回路）を一面に敷き詰めた「下地」を予め製造しておき、個別品種向けの配線層のみ注文に応じて作りこんで製品とする。配線層の製造工程だけで済むため製造期間が短く、下地は大量に製造するためコスト的に有利。反面、標準ゲートの組み合わせで回路を構成するため集積度・性能は劣る。
  - セルベース ()
    設計済みの機能ブロックを配置し、それ以外の個別ロジック回路とこれらの間の配線層を作りこんで製品とする。集積度・性能ともゲートアレイより有利だが、下地から作る分製造期間・コストは不利。
  - エンベデッドアレイ ()
    ゲートアレイの下地の一部の代わりに、設計済みの機能ブロックを埋め込み、残りのロジックはゲートアレイ部分を利用して配線するもの。ゲートアレイとセルベースの折衷型である。
  - スタンダードセル ()
    上記3種を総称する場合、セルベースICを指す場合など集積回路ベンダによって使い方が異なる。
  - ストラクチャードASIC（）
    開発期間を短縮するために、ゲートアレイの下地に加えSRAMやクロック用PLL、入出力インターフェースなどの汎用機能ブロックを予め組み込み、最小限の個別設計で対応できるようにしたもの。クロック分配回路などは製造者側で専用配線層を用いて配線するなど、ユーザの設計負担を減らす工夫が見られる。各ベンダで提供する機能はかなり異なる。

## ASICの設計方法

デジタル[回路設計](https://ja.wikipedia.org/wiki/回路設計 "wikilink")では、論理回路図を描いて設計していたが、 又は、[VHDL](https://ja.wikipedia.org/wiki/VHDL "wikilink")と呼ばれる[ハードウェア記述言語](https://ja.wikipedia.org/wiki/ハードウェア記述言語 "wikilink")の登場によって、入出力条件を中心にソフトウェア・プログラミングのように文字的な記述を行なう事で、最終的に内部回路図まで設計することが主流となった。 これらの言語は、回路情報を論理の連なりとして扱い、LSI開発効率を向上するために開発された言語である。 旧来のASIC開発では、、、、FF等の論理回路記号を回路図ベースで組み合わせて設計していた。(スケマティック/ゲートレベル) しかし、現在の  によるRTL記述では、組み合わせ回路の論理と順序回路のタイミング条件を記述するだけでよく、ゲートレベルに比べ抽象度の高い記述が可能になって設計の開発効率が向上した。RTL記述の回路はそのままでは実際のLSIの回路に適用できないため、ゲートレベルに変換する[論理合成](https://ja.wikipedia.org/wiki/論理合成 "wikilink")プログラム(例：[シノプシス](https://ja.wikipedia.org/wiki/シノプシス "wikilink")社製  等)を使用する。詳細は[EDA](https://ja.wikipedia.org/wiki/EDA "wikilink")を参照。

FPGAとASICは同一の論理記述言語を使う。そのため、プロトタイピングや試験量産段階ではFPGAを使い、可能な限りNREコストを抑え、ASICが得意とする大量生産に適した時点でFPGAからASICへの切り替えを行う手法が提案されている。この為、ピンアサインがFPGAとASICで共通化された下地や、組み込みブロックの共有化等も進められている。しかし、依然として顧客の手に届いた後で設計変更を行うリワークには対応できないのでFPGAをASICに完全に置き換える事はできない（これは特に、デジタル放送用大型テレビに顕著である）。今日、製品サイクルの短縮から生産予測は困難さを増している為、このハイブリッドソリューションはASICに対する転機として現在、市場を広げている。

## 用途

ASICの用途は非常に多岐に渡り、一部の例を以下に示す。家庭用・産業用・事務用といった多様な電気製品に使用されている。

  - 通信分野
    通信帯域の増加と通信量の増加から、高速処理を要求されるネットワーク通信機器などに特に利用されている。[ルータ](https://ja.wikipedia.org/wiki/ルータ "wikilink")、L3～L7[スイッチ](https://ja.wikipedia.org/wiki/レイヤ3スイッチ "wikilink")、[ファイアウォール](https://ja.wikipedia.org/wiki/ファイアウォール "wikilink")、[負荷分散](https://ja.wikipedia.org/wiki/負荷分散 "wikilink")（[SLB](https://ja.wikipedia.org/wiki/Server_Load_Balancing "wikilink")/[NLB](https://ja.wikipedia.org/wiki/NLB "wikilink")）装置、[パケット](https://ja.wikipedia.org/wiki/パケット "wikilink")処理装置などで、ASICが良く利用されている。
  - 画像処理
    コンピュータ用の[3Dグラフィックス](../Page/3次元コンピュータグラフィックス.md "wikilink")[レンダリングエンジンとなるLSIなどにも利用されている](https://ja.wikipedia.org/wiki/レンダリング_\(コンピュータ\) "wikilink")。また、[デジタルスチルカメラ](https://ja.wikipedia.org/wiki/デジタルスチルカメラ "wikilink")、[デジタルビデオカメラ](https://ja.wikipedia.org/wiki/デジタルビデオカメラ "wikilink")などでの画像補正、画像圧縮の処理に専用ASICを開発しているメーカー（例：[キヤノン](https://ja.wikipedia.org/wiki/キヤノン "wikilink")の[DIGIC](https://ja.wikipedia.org/wiki/DIGIC "wikilink")など）もある。
    高速な[コピー機](https://ja.wikipedia.org/wiki/コピー機 "wikilink")などの[複合機](https://ja.wikipedia.org/wiki/複合機 "wikilink")でも、高速な画像処理が必要な装置では、画像処理専用ASICを搭載しているものもある。[DVDレコーダー](../Page/DVDレコーダー.md "wikilink")に代表される動画圧縮/再生処理も、専用の[MPEG](../Page/Moving_Picture_Experts_Group.md "wikilink")[エンコーダ](https://ja.wikipedia.org/wiki/エンコーダ "wikilink")/[デコーダ](https://ja.wikipedia.org/wiki/デコーダ "wikilink")用ASICが開発されている。[デジタル放送](https://ja.wikipedia.org/wiki/デジタル放送 "wikilink")対応の大型[FPD](https://ja.wikipedia.org/wiki/FPD "wikilink")テレビには、上記MPEGデコーダASICが搭載されることもあるが、将来的な圧縮方式の規格変更に対応可能なように、[FPGA](https://ja.wikipedia.org/wiki/FPGA "wikilink")で構成されているものもある。
  - コンピュータシステム全般
    [CPU](../Page/CPU.md "wikilink")や[マイクロコントローラ](https://ja.wikipedia.org/wiki/マイクロコントローラ "wikilink")などのプロセッサも、専用マスクを作成して生産するという点では広義のASICの定義に該当するが、これらは常に別分類として扱われる。各種CPU用の[チップセット](../Page/チップセット.md "wikilink")や、汎用標準バス制御（[PCI](../Page/Peripheral_Component_Interconnect.md "wikilink")[バスブリッジ](https://ja.wikipedia.org/wiki/バスブリッジ "wikilink")など）のLSIはASICといえる。

## プロセス技術

ASICは半導体種別として多様であるばかりでなく、半導体プロセス技術の世代においても幅の広い世代を使用している。例えば、台湾 は2008年末から40nmプロセスでの生産を開始しており、台湾 （UMC）は45nmプロセスでの試作製造に成功し、中国 （SMIC）は2009年から45nmプロセスでの生産を準備中といった具合で、ASICを手がける世界的なファンウンドリーの多くが、米インテル社や米AMD社、米社などが使用する最新のプロセス技術からは1世代ほど遅れながらもしっかり追随しているが、その一方では例えば、台湾UMCでも、2008年第3四半期での全売上高に占めるプロセス世代での割合は、65nm世代では7%しかなく、90nm世代で31%、130nm世代で20%、150nmで21%、250-350nm世代で16%、500nm以上の世代でも5%もあった。これは、よく言われるように最新のプロセス技術はマスク代だけでも高価であり、例えば65nmでは1セットで100万米ドル弱であるのに、130nmではマスク代に設計・試験・検証のコストを加えファウンドリーへ支払う開発コストまで含めても40万米ドルで済むため、最先端のプロセス技術による高性能化が求められず、従来製品の細かな修正で済むASIC製品には古くは7世代も前のプロセスを使用しているのが現状である\[1\]。

## 脚注

### 出典

## 関連項目

  - [論理回路](https://ja.wikipedia.org/wiki/論理回路 "wikilink")
  - [システムLSI](https://ja.wikipedia.org/wiki/システムLSI "wikilink")
  - [EDA (半導体)](https://ja.wikipedia.org/wiki/EDA_\(半導体\) "wikilink")
  - [FPGA](https://ja.wikipedia.org/wiki/FPGA "wikilink")
  - [シャトル・サービス](https://ja.wikipedia.org/wiki/シャトル・サービス "wikilink")

[Category:集積回路](https://ja.wikipedia.org/wiki/Category:集積回路 "wikilink") [Category:電子工学](https://ja.wikipedia.org/wiki/Category:電子工学 "wikilink")

1.  木村雅秀著　『ASICの微細化に急ブレーキ 45nm世代で壁に直面』　「日経エレクトロニクス 2009年3月9日号」　p.94-98
> この記事は[ISDN](https://ja.wikipedia.org/wiki/ISDN)から翻訳されています。


**ISDN**（アイエスディーエヌ、**Integrated Services Digital Network**、**サービス総合ディジタル網**\[1\]\[2\]）とは[交換機](../Page/交換機.md "wikilink")・中継回線・[加入者線](https://ja.wikipedia.org/wiki/加入者線 "wikilink")まで全て[デジタル](../Page/デジタル.md "wikilink")化された、[パケット通信](../Page/パケット通信.md "wikilink")・[回線交換](https://ja.wikipedia.org/wiki/回線交換 "wikilink")[データ通信](../Page/データ通信.md "wikilink")にも利用できる[公衆交換電話網](../Page/公衆交換電話網.md "wikilink")である。[ITU-T](../Page/ITU-T.md "wikilink")（電気通信標準化部門）によって世界共通のIシリーズ規格として定められている。

音声は、0.3 - 3.4[kHzを](https://ja.wikipedia.org/wiki/キロヘルツ "wikilink")64k[bpsの回線交換でISDN網内を伝送しているため](../Page/ビット毎秒.md "wikilink")、[VoIP](../Page/VoIP.md "wikilink")よりも音声品質が安定している。また北米・日本は[μ則](https://ja.wikipedia.org/wiki/μ-lawアルゴリズム "wikilink")、その他の国々では[A則が](https://ja.wikipedia.org/wiki/A-lawアルゴリズム "wikilink")[PCM](https://ja.wikipedia.org/wiki/PCM "wikilink")非直線[符号化に使用されているため北米](../Page/符号化方式.md "wikilink")・日本側の関門[電話交換機](https://ja.wikipedia.org/wiki/電話交換機 "wikilink")で変換している。

データ通信では、通信相手が[電話番号](../Page/電話番号.md "wikilink")で特定でき、回線交換は通信速度が、パケット通信は[QoS](../Page/Quality_of_Service.md "wikilink")（サービスの品質）が保証されている。

## ISDNの構想

情報通信の要素には音声・データ・画像などがあるが、1970年代から80年代になるまで音声通信は電話網、データ通信はデータ通信網で行われ、通信方式もアナログが全盛であった\[3\]。しかしディジタル技術の台頭とともに通信網にどのようにその技術を導入するかが検討されるようになり、加入者線の部分もディジタル化することで音声・データ・画像を同一伝送路で扱うことができるように考え出されたのがISDNである\[4\]。

1972年、[CCITTのジュネーブ総会でISDNの基本概念が発表された](../Page/ITU-T.md "wikilink")。

ISDNの構想は1977年から国際電気通信連合で取り上げられ、1984年に暫定勧告、1988年に本格勧告が承認された\[5\]。

1985年4月、[シンガポール](https://ja.wikipedia.org/wiki/シンガポール "wikilink")において[富士通](../Page/富士通.md "wikilink")製のデジタル[電話交換機](https://ja.wikipedia.org/wiki/電話交換機 "wikilink")で、世界初のIインタフェースによる実環境を用いた試験が開始された。

## ISDNの構成

### 機器の接続

日本では一般的な基本速度TCM-ISDNは[ヨーロッパ](../Page/ヨーロッパ.md "wikilink")・[アジア](../Page/アジア.md "wikilink")の基本速度Euro-ISDNと加入者線インタフェースが異なるため、回線終端装置 (DSU) の互換性は無い。また、一次群速度加入者線インタフェースについても地域によって異なっている。

DSU以外の部分は、ソフトウエアの変更のみで各国対応となる機器が多い。

#### S点インタフェース機器

基本インタフェースのNTの端末側（S点・T点）は終端された4線式のバス配線であり、ポイント・マルチポイント構成と呼ばれる1本当たり最大8台の端末の接続が可能である。

次の2種類がある。

  - 短距離受動バス配線
    最大ケーブル長が200m以下の配線であり、任意の場所に端末接続用のモジュラージャックを設置できる。
  - 延長受動バス配線
    最大ケーブル長が500m以下の配線であり、末端部付近に集中して端末接続用のモジュラージャックを設置できる。

また端末接続用のモジュラージャックはバス配線に直接取り付けるか、長さ1m以内のスタブを介して取り付ける。モジュラージャックから端末までのコードは原則は10m以内に制限されているが、ポイント・ポイント構成の場合に限り25mまで延長できる。

一次群速度インタフェースのNTの端末側（S点・T点）は4線式の配線であり、ポイント・ポイント構成と呼ばれる1本当たり1台のみの端末の接続が可能である。

伝送路から伝送された信号を回線終端装置 (NT1) でS点インタフェースに変換し、超高速伝送の可能な[ルータ](https://ja.wikipedia.org/wiki/ルータ "wikilink")・[G4 FAXなどのS点インタフェース機器](https://ja.wikipedia.org/wiki/ファクシミリ#規格 "wikilink") (TE1) を接続する。また、[構内交換機](https://ja.wikipedia.org/wiki/構内交換機 "wikilink") (NT2) などを使用し内線通信などを可能にすることもある。

`|TE1|--S点--|NT2|--T点--|NT1|-- (LI) U点--加入者線`

#### アナログ電話回線機器など

S点インタフェースが複雑なために実際にS点インタフェースを備えた端末機器（G4 FAXやISDN対応電話機）は少なく、[ターミナルアダプタ](../Page/ターミナルアダプタ.md "wikilink") (TA) で変換して従来のアナログ[電話機](https://ja.wikipedia.org/wiki/電話機 "wikilink")・ファクシミリ (TE2) や[LAN](../Page/Local_Area_Network.md "wikilink")・[コンピュータ](../Page/コンピュータ.md "wikilink")機器を接続して利用する形態が一般的に行われている。

ターミナルアダプタは、ISDN回線からの給電のみでは動作しない。そのため、乾電池などで停電補償を行うものがある。

`|TE2|--R点--|TA|--S点--|NT2|--T点--|NT1|-- (LI) U点--加入者線`

NT2とTAの機能を持ったターミナルアダプタの場合

`|TE2|--R点--|TA + NT2|--T点--|NT1|-- (LI) U点--加入者線`

また、NT1、NT2、TAの機能を全て備えたターミナルアダプタの場合は以下のようになる。

`|TE2|--R点--|TA + NT2 + NT1|-- (LI) U点--加入者線`

#### 機能群

  - NT1
    回線終端装置 (DSU: Digital Service Unit) - 加入者線の終端・Iインタフェースへの変換・端末機器などへの給電を行う。
  - NT2
    端末制御装置・[構内交換機](https://ja.wikipedia.org/wiki/構内交換機 "wikilink") (PBX: Private automatic Branch eXchange) - 端末装置間の通信手順制御・交換・多重化・集線などを行う。
  - TE1
    S点インタフェース端末装置
  - TE2
    S点インタフェース以外の端末装置
  - TA
    ターミナルアダプタ

#### 参照点

  - (LI) U点
    伝送路インタフェース規定点 - 基本速度インタフェースの場合はNT1のRJ-11の電話用6極[モジュラージャックまたはねじ止め部分](../Page/Registered_jack.md "wikilink")、一次群速度インタフェースの場合は、NT1の光コネクタ部分である。
  - T点
    ISDNユーザー網インタフェース規定点 - 基本速度インタフェースの場合はNT1の[RJ-45の](../Page/8P8C.md "wikilink")8極モジュラージャックまたはねじ止め部分、一次群速度インタフェースの場合は、NT1のねじ止め部分である。
  - S点
    NT2のRJ-45の8極モジュラージャックまたはねじ止め部分である。
  - R点
    TEの電話用6極モジュラージャック部分である。

#### 分界点

[端末](../Page/端末.md "wikilink")設備と電気通信回線設備との最初の接続点が分界点となる。具体的には基本速度インタフェースの場合は[保安器](../Page/保安器.md "wikilink")または[主配線盤](../Page/主配線盤.md "wikilink")の端末側ねじ止め部分、一次群速度インタフェースの場合は配線盤の光コネクタ部分である。

### 回線構成

ISDNにはBとDの2つのチャネルがある。

  - Bチャネル - データ用（64kbpsが2チャネル）。データリンク層のプロトコルはLAPD。
  - Dチャネル - 信号・制御用（パケットデータ通信にも利用可能、16kbps、64kbps）。データリンク層のプロトコルはPPP、HDLC。

Bチャネルを束ねたチャネルも定義されている。

  - H<sub>01</sub>チャネル - Bチャネルを6個束ねたもの。
  - H<sub>11</sub>チャネル - Bチャネルを24個束ねたもの。
  - H<sub>12</sub>チャネル - Bチャネルを30個束ねたもの。

ISDNには、基本速度インタフェースと一次群速度インタフェースの2種類がある。

### 基本速度インタフェース

基本速度[インタフェース](../Page/インタフェース_\(情報技術\).md "wikilink") (BRI: Basic Rate Interface) は64kbpsの2個のデータチャネルと16kbpsの信号チャネルから構成され、2B+Dなどと表記される。基本速度インタフェースはSOHO、個人、バックアップ回線として利用される。

加入者線伝送方式として、アナログ電話回線と同じ2芯[ツイストペアケーブル](../Page/ツイストペアケーブル.md "wikilink")[通信線路](../Page/通信線路.md "wikilink")が使用されることが多い。電話局設置の[電話交換機](https://ja.wikipedia.org/wiki/電話交換機 "wikilink")からDSUの動作と[音声通話](https://ja.wikipedia.org/wiki/音声通話 "wikilink")に必要な最低限の給電が行われる。

伝送方式は、地域や[電気通信事業者](../Page/電気通信事業者.md "wikilink")によって異なっている。

#### TCM-ISDN

TCM-ISDNは、日本の[NTT東日本](../Page/東日本電信電話.md "wikilink")・[西日本の](../Page/西日本電信電話.md "wikilink")「[INSネット](https://ja.wikipedia.org/wiki/INSネット "wikilink")64」で使用されている。

ピンポン伝送とも呼ばれる時分割方向制御方式 (Time Compression Multiplexing) でAMI[符号化による](../Page/符号化方式.md "wikilink")[ベースバンド伝送](../Page/ベースバンド伝送.md "wikilink")を行っている。使用する[周波数](../Page/周波数.md "wikilink")帯域が広くなるが、伝送装置が単純となる。また加入者線間でタイミングを合わせて送受信を切り替えるため近端漏話が無く遠端漏話のみとなり、細い加入者線で長距離伝送が可能である。

日本国内において遍く提供されているように思われているがINSネット64の場合（メタル線）、収容局から加入者宅までのメタル線路長が8 - 10kmを超えるような場合には、サービス提供が困難であると言う問題がある。また、[基礎的電気通信役務](../Page/基礎的電気通信役務.md "wikilink")でも無いためNTT東日本・西日本は日本全国に遍く提供する義務も無い。

周波数帯域が重なってしまうため[ADSL](../Page/ADSL.md "wikilink")回線と加入者線（ISDN回線）の同時使用は不可能である。また相互干渉を抑えるAnnex C規格の採用や同じより対線の組にISDNとADSLを収容しないようにする収容代えが必要であるなど、日本国内の一部からはADSL普及を阻害したと批判されたこともあった。

#### Euro-ISDN

日本におけるEuro-ISDNは、[電力系通信事業者](../Page/電力系通信事業者.md "wikilink")のISDNにて使用されている。また[平成電電](https://ja.wikipedia.org/wiki/平成電電 "wikilink")のISDNサービスもEuro-ISDNを採用していた。

[ヨーロッパ](../Page/ヨーロッパ.md "wikilink")・[アジア](../Page/アジア.md "wikilink")諸国で使用されているEuro-ISDNは[エコーキャンセラを用い](../Page/エコー除去.md "wikilink")、上り下りを同じ周波数帯域の[デジタル変調](../Page/デジタル変調.md "wikilink")で伝送している。使用する周波数帯域が狭くなるが、伝送装置が複雑となる。

Annex B のADSLと加入者線の同時使用が可能である。

### 一次群速度インタフェース

一次群速度インタフェース (PRI: Primary Rate Interface) は、より多くのチャネルから構成される。企業やプロバイダの回線として利用される。

構成は、地域によって異なっている。

  - 北米及び日本（NTTの「INSネット1500」）
    23B+D (64kbps)（他の回線とDチャネルを共用する場合は24Bも可能）で、通信速度は1.544 Mbit/s (T1)
  - ヨーロッパ、及びオーストラリア
    30B+D (64kbps) で、通信速度は 2.048 Mbit/s (E1)

加入者線伝送方式として、2芯の[光ケーブル](../Page/光ケーブル.md "wikilink")が使用されることが多い。給電が行われないため、加入者側で電源の確保が必要である。

### B-ISDNインタフェース

一次群速度インタフェースよりも高速な回線インタフェースである。

開発や試験サービスが行われていたが安価な常時接続で定額料金の[IP加入者線サービスが提供されるようになり](../Page/Internet_Protocol.md "wikilink")、一般家庭向けの商用サービス化は行われなかった。

## 各国の通信事業とISDN

### 日本

#### 電話番号

[電話番号](../Page/電話番号.md "wikilink")は、通常の[市外局番](../Page/市外局番.md "wikilink")と同じものが、Dチャネル1つあたり1つ割り当てられる。また「[ダイヤルイン](https://ja.wikipedia.org/wiki/ダイヤルイン "wikilink")」や「[i・ナンバー](https://ja.wikipedia.org/wiki/i・ナンバー "wikilink")」を申し込むことにより、電話番号の追加が有料で可能である。

ダイヤルインを利用した番号の追加はDチャネル毎に与えられた1つの番号を含めて最大で9999番号、i・ナンバーを利用した番号の追加はDチャネル毎に与えられた1つの番号を含めて最大3番号で番号の利用は回線につながったISDN[ターミナルアダプタ](../Page/ターミナルアダプタ.md "wikilink")に番号を設定する事で、Iインターフェースに2チャネルあるBチャネルと1チャネルあるDチャネルで自由に利用することが出来る。

また、ダイヤルインやi・ナンバーの電話番号は通常の市外局番の電話番号以外に、[フリーダイヤル](../Page/フリーダイヤル.md "wikilink")の0120や0800で始まる番号や情報提供料を発信者に課金する[ダイヤルQ2](../Page/ダイヤルQ2.md "wikilink")の0990で始まる番号、\#ダイヤル（着信短縮ダイヤルサービス）の番号などの割り当てを受けることも可能。

ISDN相互間の通信の場合、[サブアドレス](https://ja.wikipedia.org/wiki/サブアドレス "wikilink")という付加番号を電話番号の後に付け同じ電話番号の中から特定の端末を指定しての呼び出しが可能である。またサービスクラスと呼ばれる可能な通信方法を呼び出し時に知らせる機能により、[ファクシミリ](https://ja.wikipedia.org/wiki/ファクシミリ "wikilink")からの発信の場合にファクシミリのみ応答させるといったことが可能である。

なお、日本では総合デジタル通信回線に端末設備等を接続するための工事には[電気通信設備工事担任者](../Page/電気通信設備工事担任者.md "wikilink")のAI種（**A**nalog・**I**SDN）の所持者が直接工事を行うか実地に監督をする必要がある\[6\]。

#### 料金

回線交換方式の場合、接続時間と通信地点間距離とで課金される。日本では、アナログ電話網と同じ料金である（[離島特例通信](https://ja.wikipedia.org/wiki/離島特例通信 "wikilink")を除く）。

バーチャルコール方式の[パケット通信](../Page/パケット通信.md "wikilink")の場合、接続時間に関係なく[パケット](../Page/パケット.md "wikilink")の長さと数のみで定まるデータ量課金である。

月額基本料金は、アナログ電話回線2回線分より安く設定されている。

### 米国

米国ではISDN(128kbps)は2000年頃までブロードバンドの定義に含まれていた\[7\]。しかし、ADSLやケーブルモデムの出現により米国議会やFCC報告書などでは375Kbps以上をブロードバンドと定義するものが多くなった\[8\]。

2001年の時点ではISDN回線が市場シェア35％を占めていたが、そのシェアは急速に低下しADSLやSDSLが普及した\[9\]。

## 脚注

## 関連項目

  - [INSネット](https://ja.wikipedia.org/wiki/INSネット "wikilink") : 日本でのサービス
  - [H.320](https://ja.wikipedia.org/wiki/H.320 "wikilink")
  - [ターミナルアダプタ](../Page/ターミナルアダプタ.md "wikilink")
  - [ダイヤルアップルーター](https://ja.wikipedia.org/wiki/ルーター#ダイヤルアップルーター "wikilink")

## 外部リンク

  - [電子情報通信学会 知識ベース ISDN](http://www.ieice-hbkb.org/files/05/05gun_06hen_01.pdf#page=15)

[Category:電話網](https://ja.wikipedia.org/wiki/Category:電話網 "wikilink") [Category:ITU-T勧告](https://ja.wikipedia.org/wiki/Category:ITU-T勧告 "wikilink") [Category:コンピュータネットワーク](https://ja.wikipedia.org/wiki/Category:コンピュータネットワーク "wikilink")

1.  日本ITU協会による[CCITT勧告和訳本の表記による](../Page/ITU-T.md "wikilink")。また[NTT東日本](../Page/東日本電信電話.md "wikilink")、[NTT西日本](../Page/西日本電信電話.md "wikilink")、[KDDI](../Page/KDDI.md "wikilink")などの商用ISDNサービスの解説でもこの表記を用いている。
2.  [シスコシステムズ](../Page/シスコシステムズ.md "wikilink")による[インターネットワーキング用語・略語集](http://www.cisco.com/japanese/warp/public/3/jp/service/info/tips/terms/AI.shtml)では**サービス総合ディジタルネットワーク**と解説しているなど、他の日本語表記も多く見られる。
3.
4.
5.  加納貞彦、北見憲一、[「開発物語 ISDNの標準化」](https://doi.org/10.1587/bplus.5.63) 『電子情報通信学会　通信ソサイエティマガジン』 2011年 5巻 1号 p.63-69,
6.  [電気通信事業法 第71条](https://elaws.e-gov.go.jp/search/elawsSearch/elaws_search/lsg0500/detail?lawId=359AC0000000086&openerCode=1)
7.  [ITフォーラム](https://www.nttcom.co.jp/comzine/archive/forum/sep4.html) - NTTコムウェア
8.
9.
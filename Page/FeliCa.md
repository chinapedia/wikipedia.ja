> この記事は[FeliCa](https://ja.wikipedia.org/wiki/FeliCa)から翻訳されています。


[サムネイル](https://ja.wikipedia.org/wiki/ファイル:Iccard.gif "wikilink") **FeliCa**（フェリカ）は、[ソニー](../Page/ソニー.md "wikilink")（現・[ソニーイメージングプロダクツ&ソリューションズ](https://ja.wikipedia.org/wiki/ソニーイメージングプロダクツ&ソリューションズ "wikilink")）が開発した非接触型[ICカード](../Page/ICカード.md "wikilink")の技術方式、および同社の登録商標である。

名称は、元々ソニーが保有していた商標の中から適当なものを選んで命名されたもの\[1\]である。後付ではあるものの、「至福」を意味する「**Feli**city」と「**Ca**rd」を組み合わせた[かばん語](https://ja.wikipedia.org/wiki/かばん語 "wikilink")として、「至福をもたらすカード」という意味も込められている。

## 概要

FeliCaは、非接触型ICカードのための[通信](../Page/通信.md "wikilink")技術として、ソニーが開発した。非接触型ICカードは、リーダ・ライタから[キャリアを送信して](https://ja.wikipedia.org/wiki/搬送波 "wikilink")[電磁誘導](../Page/電磁誘導.md "wikilink")によりICカードに電力を供給し、キャリアの[変調](https://ja.wikipedia.org/wiki/変調 "wikilink")によりリーダ・ライタとカード間で通信を行う。例えば[ISO/IEC 14443で規格化されているTYPE](https://ja.wikipedia.org/wiki/ISO/IEC_14443 "wikilink") B方式は、[ASK](https://ja.wikipedia.org/wiki/振幅偏移変調 "wikilink")10%で変調を行い、[NRZ符号を採用しているのに対してFeliCaの方式は変調が](https://ja.wikipedia.org/wiki/Non-return-to-zero "wikilink")[ASK](https://ja.wikipedia.org/wiki/ASK "wikilink")10%と同じであるが、マンチェスタ (Manchester) 符号を採用しているところが異なる。

当初、[国際標準化機構](https://ja.wikipedia.org/wiki/国際標準化機構 "wikilink")にISO/IEC 14443 TYPE Cとして提案を行った。同時にTYPE D〜Gまでが提案されたが「[近距離無線通信](https://ja.wikipedia.org/wiki/近距離無線通信 "wikilink")規格の乱立になる」として、[国際規格](https://ja.wikipedia.org/wiki/国際規格 "wikilink")議論が停止され採用されなかった。その後、FeliCaと上位互換性のある方式が[ISO/IEC 18092 (Near Field Communication, NFC TYPE-F)](https://ja.wikipedia.org/wiki/近距離無線通信 "wikilink") として規格化された。[日本](https://ja.wikipedia.org/wiki/日本 "wikilink")では、[JICSAP](https://www.jicsap.com/)（[一般社団法人 ID認証技術推進協会](https://ja.wikipedia.org/wiki/ID認証技術推進協会 "wikilink")） ICカード仕様V2.0「第4部 高速処理用ICカード」や、[日本鉄道サイバネティクス協議会](https://ja.wikipedia.org/wiki/日本鉄道サイバネティクス協議会 "wikilink")でのICカード規定として規格化されている。

FeliCaは通常のICカードと同様に、キャッシュカードやIDカードなどに適用可能な技術である。特に高速処理が求められる、[自動改札機](https://ja.wikipedia.org/wiki/自動改札機 "wikilink")や建物入館の[セキュリティゲート](https://ja.wikipedia.org/wiki/セキュリティゲート "wikilink")や、[キャッシュレジスター](https://ja.wikipedia.org/wiki/キャッシュレジスター "wikilink")のアプリケーション向けに特化したコマンド体系になっている。そのため、ISO 7816-3の基本コマンドとは互換性はない。また、ICチップ内部のメモリは16バイト固定長のレコードのみがサポートされていて、で規定されているファイル構造との互換性はない。

[暗号処理](https://ja.wikipedia.org/wiki/暗号処理 "wikilink")としては、相互認証に[トリプルDES](https://ja.wikipedia.org/wiki/トリプルDES "wikilink")、通信路に[DESもしくはトリプルDESを利用している](https://ja.wikipedia.org/wiki/Data_Encryption_Standard "wikilink")。Dualカードタイプ（接触/非接触）では[公開鍵暗号](https://ja.wikipedia.org/wiki/公開鍵暗号 "wikilink")方式の処理が可能なものがある。

2011年6月には、相互認証と通信路に[AESも利用できるFeliCaチップが発表された](https://ja.wikipedia.org/wiki/Advanced_Encryption_Standard "wikilink")\[2\]。

1枚のカード（1つのチップ）に[乗車カード](../Page/乗車カード.md "wikilink")、電子マネー、社員証など複数のサービスを搭載可能であるが、サービス利用時には、個々のサービス毎にアクセス鍵（共通鍵）を使って相互認証を行うのではなく、複数のアクセス鍵から「縮退鍵」と呼ばれる[暗号化](https://ja.wikipedia.org/wiki/暗号化 "wikilink")された[鍵を合成し](https://ja.wikipedia.org/wiki/鍵_\(暗号\) "wikilink")、この縮退鍵を用いて、一度に最大16のサービスについて相互認証することが可能となっている。縮退された鍵から元の鍵は生成できない。このことから、セキュリティレベルを落とすことなく処理速度の高速化を実現している。

## FeliCaチップの搭載

FeliCaチップは、ICカードのICチップとして使用される他、携帯電話や腕時計などでFeliCaチップを搭載したものがある。

当初はソニーでのみ製造されていたが、[インフィニオン・テクノロジーズ](https://ja.wikipedia.org/wiki/インフィニオン・テクノロジーズ "wikilink")と共同開発（[2001年](../Page/2001年.md "wikilink")11月発表）、[日立製作所](https://ja.wikipedia.org/wiki/日立製作所 "wikilink")の採用（[2002年](../Page/2002年.md "wikilink")6月発表）など、複数のチップメーカーが供給できるようになった。

モトローラの中価格帯スマートフォンMoto Zシリーズ用の拡張モジュールmoto mods開発時の試算では、moto modsにNFCを搭載する場合のライセンス料は2,3ドル程度だが、高機能なFeliCaを搭載すると1万円になるという\[3\]。

### ICカードへの搭載

1992年末、香港の交通事業者6社から成るジョイントベンチャーのICカードの競争入札に参加し、要求に沿う形で仕様が決められていき、1997年9月に[香港](https://ja.wikipedia.org/wiki/香港 "wikilink")で「[オクトパス](https://ja.wikipedia.org/wiki/八達通 "wikilink")」として[世界](https://ja.wikipedia.org/wiki/世界 "wikilink")で初めて採用された\[4\]。この時の競合相手はミクロン社。その後、2001年11月に日本でICカード乗車券「[Suica](../Page/Suica.md "wikilink")」、2002年4月に[シンガポール](https://ja.wikipedia.org/wiki/シンガポール "wikilink")の「[EZ-link](https://ja.wikipedia.org/wiki/EZ-link "wikilink")」で採用されてきた。

また、Edy付きのeLIOがポイントカードと一体化した[ヨドバシカメラ](https://ja.wikipedia.org/wiki/ヨドバシカメラ "wikilink")の「ゴールドポイントカードIC eLIO」や、ICキャッシュカードの付加機能としてEdyが採用されたり、クレジットカードとSuicaが一体化した「VIEW Suica」がさらにビックカメラのポイントカードと合体した「ビックカメラSuicaカード」などサービスの融合も行われている。

過去には、[1999年](../Page/1999年.md "wikilink")から[2003年](../Page/2003年.md "wikilink")まで、[東京臨海副都心](https://ja.wikipedia.org/wiki/東京臨海副都心 "wikilink")・[青海の](https://ja.wikipedia.org/wiki/青海_\(江東区\) "wikilink")[パレットタウン](https://ja.wikipedia.org/wiki/パレットタウン "wikilink")内にある[MEGAWEB](https://ja.wikipedia.org/wiki/MEGAWEB "wikilink")で発行されていた「MEGA WEB Member's Card」や[2000年](../Page/2000年.md "wikilink")から[2002年](../Page/2002年.md "wikilink")まで、[東京臨海副都心](https://ja.wikipedia.org/wiki/東京臨海副都心 "wikilink")・[お台場](https://ja.wikipedia.org/wiki/お台場 "wikilink")の[ソニーグループ](https://ja.wikipedia.org/wiki/ソニーグループ "wikilink")の[エンターテインメント](../Page/エンターテインメント.md "wikilink")施設[メディアージュ](https://ja.wikipedia.org/wiki/メディアージュ "wikilink")で発行されていた「メディアージュ ファンカード」にも採用されていた。

ソニーが販売しているICカードにはRC-S860と853/854などがあり、RC-S860はEdyで使用、RC-S853/854はサイバネ規格に準拠したカードでSuicaで使用されている。

#### 主な規格

下記の規格を満たしたカード・半導体が、各社から販売されている。

  - FeliCa Standard - フルバージョンのカード。暗号方式がトリプル[Data Encryption Standard](https://ja.wikipedia.org/wiki/Data_Encryption_Standard "wikilink")（DES）のみ対応の旧版、DES・[Advanced Encryption Standard](https://ja.wikipedia.org/wiki/Advanced_Encryption_Standard "wikilink")（AES）両対応\[5\]のカード、AESのみ対応のカードの3種類がある\[6\]。
  - FeriCa lite - セキュリティ機能を簡易化・ICチップを小型化したカード\[7\]。
  - FeriCa lite-S - FeriCa liteよりもセキュリティを強化・省電力化したカード。
  - モバイルFeliCa ICチップ - モバイル機器組み込み用のICチップ。[おさいふケータイ](https://ja.wikipedia.org/wiki/おさいふケータイ "wikilink")・カードリーダーなどで使用\[8\]。
  - FeliCa Plug - 機器組み込み用の無線インターフェースモジュール。スマートフォン・カードリーダーなどで使用\[9\]。

#### アンテナの形状

[thumb](https://ja.wikipedia.org/wiki/ファイル:Defaced_EZ-Link_Card.jpg "wikilink") ICカードに搭載した場合のアンテナの形状は、[Suica](../Page/Suica.md "wikilink")と[Edyでは異なる](https://ja.wikipedia.org/wiki/楽天Edy "wikilink")。また、[トランセカード](https://ja.wikipedia.org/wiki/トランセカード "wikilink")はこれらとも異なる形状をしている。

  - RC-S860 四角 (Edy)
  - RC-S853/854 円弧 (Suica)

Edy用のRC-S860のアンテナはカードの端に沿って四角型に配置される。Suica等の定期券入れ等に入れて他のFeliCaカードと重ねたまま使われることが想定されるRC-853/854では、アンテナは干渉の影響を減少させるために木の葉の輪郭のような形状になっている。これにより、より電波を受信しやすくできるほか、[アンチコリジョン](https://ja.wikipedia.org/wiki/アンチコリジョン "wikilink")機能が施されているFeliCaカードならば、3枚まで重ねてもそれぞれのカードを認識できる。

### 携帯電話・PHSへの搭載

[NTT_DoCoMo_FOMA_F901iC_open_back.jpg](https://ja.wikipedia.org/wiki/File:NTT_DoCoMo_FOMA_F901iC_open_back.jpg "fig:NTT_DoCoMo_FOMA_F901iC_open_back.jpg")を搭載した初期の携帯電話「[F901iC](https://ja.wikipedia.org/wiki/F901iC "wikilink")」（2004年12月発売）。バッテリーカバーにあるFeliCaプラットフォームマークを読み取り機器にかざしては使用する。\]\] [携帯電話](../Page/携帯電話.md "wikilink")用のFeliCaチップは**モバイルFeliCa ICチップ**またはモバイルFeliCaチップと呼ばれている。ソニーと[NTTドコモ](https://ja.wikipedia.org/wiki/NTTドコモ "wikilink")の合弁会社である[フェリカネットワークス](https://ja.wikipedia.org/wiki/フェリカネットワークス "wikilink")が開発した。

[2004年](https://ja.wikipedia.org/wiki/2004年 "wikilink")7月にはFeliCaチップを搭載した携帯電話が発売開始された。携帯電話にFeliCaチップを搭載することで、EdyやSuica（モバイルSuica）などを携帯電話で利用できる。モバイルFeliCaチップを利用したサービスをいち早く開始したNTTドコモの登録商標である「[おサイフケータイ](https://ja.wikipedia.org/wiki/おサイフケータイ "wikilink")」が、事業者をまたいでのサービスブランドとして定着している。モバイルFeliCaチップはソニー1社が製造していたが、次期モバイルFeliCaチップは東芝とルネサス テクノロジを加えた3社から供給されることが[2006年](https://ja.wikipedia.org/wiki/2006年 "wikilink")5月に発表された。この新世代のモバイルFeliCaチップ (FeliCa ver.2) は、容量の拡大や通信機能の搭載など機能強化を行ったもので、2006年10月にこれを搭載した携帯電話が発表された。

  - 「[iモードFeliCa](https://ja.wikipedia.org/wiki/iモードFeliCa "wikilink")」（[NTTドコモ](https://ja.wikipedia.org/wiki/NTTドコモ "wikilink")）
  - 「[EZ FeliCa](https://ja.wikipedia.org/wiki/EZ_FeliCa "wikilink")」（[KDDI](../Page/KDDI.md "wikilink")・[沖縄セルラー電話](https://ja.wikipedia.org/wiki/沖縄セルラー電話 "wikilink")）
  - 「[S\!FeliCa](https://ja.wikipedia.org/wiki/S!FeliCa "wikilink")（旧称・ボーダフォンライブ\!FeliCa）」（[ソフトバンクモバイル](https://ja.wikipedia.org/wiki/ソフトバンクモバイル "wikilink")）
  - 「[ウィルコムICサービス](https://ja.wikipedia.org/wiki/ウィルコムICサービス "wikilink")」（ソフトバンクモバイル・[ウィルコム沖縄](https://ja.wikipedia.org/wiki/ウィルコム沖縄 "wikilink")（旧・ワイモバイル←[ウィルコム](https://ja.wikipedia.org/wiki/ウィルコム "wikilink")））
  - 「おサイフケータイ」（ソフトバンクモバイル・ウィルコム沖縄（旧・ワイモバイル←イー・アクセス））

携帯電話での普及状況は、[おサイフケータイ](https://ja.wikipedia.org/wiki/おサイフケータイ "wikilink")の項もあわせて参照の事。

FeliCa用のリーダーライターについては[PaSoRi](https://ja.wikipedia.org/wiki/PaSoRi "wikilink")を参照。

### その他

[thumbの](https://ja.wikipedia.org/wiki/画像:Speedpass%2B_Key_Tag.jpg "wikilink")[Speedpass+](https://ja.wikipedia.org/wiki/Speedpass#Speedpass+ "wikilink")。
円形のRC-S893が組み込まれている。\]\]

  - [フィギュア](https://ja.wikipedia.org/wiki/フィギュア "wikilink")の台座部分にFeliCaチップを搭載したものが開発されており\[10\]、実際に[楽天Edy](https://ja.wikipedia.org/wiki/楽天Edy "wikilink")用などに製品化された（[楽天Edy\#変わり種](https://ja.wikipedia.org/wiki/楽天Edy#変わり種 "wikilink")を参照）。
  - 2006年シーズンから、[ハワイウインターベースボールリーグの入場チケットには](https://ja.wikipedia.org/wiki/:en:Hawaii_Winter_Baseball "wikilink")[キーホルダー](https://ja.wikipedia.org/wiki/キーホルダー "wikilink")型のFeliCaが採用されている\[11\]。
  - [高雄捷運](https://ja.wikipedia.org/wiki/高雄捷運 "wikilink")では、日本の乗車券にあたる單程票において、コイン型のFeliCaが採用されている。

## セキュリティ

### FeliCaチップの安全性

FeliCaチップを搭載したカードRC-S860は、2001年にEAL3の評価を受け、2002年3月4日に英国CESGCから[ISO/IEC 15408](https://ja.wikipedia.org/wiki/コモンクライテリア "wikilink") EAL4の認定を受けている。ただし、この認定には、PP/9806などのICカード用システムLSIの主要なProtection Profileで要求されているAVA_VLA.4やSOF-highが含まれていなかったが、後にEAL4+の認定を受けている。

### 安全性についての論争

経営者向けの直販誌「[FACTA](https://ja.wikipedia.org/wiki/FACTA "wikilink")」の2006年9月号に、FeliCaに脆弱性が存在するとの記事が掲載された\[12\]。さらに、同誌2007年1月号は、FeliCaチップの内部を見ることができ、その改変も可能であるとした\[13\]。

これに対して、情報の出所が明らかでなく具体的な記述もないという理由で、[ITmedia](https://ja.wikipedia.org/wiki/ITmedia "wikilink")が批判を加えた\[14\]。[ITmedia](https://ja.wikipedia.org/wiki/ITmedia "wikilink")によれば、[情報処理推進機構](https://ja.wikipedia.org/wiki/情報処理推進機構 "wikilink") (IPA) は、情報が提供された事実を認め、経済産業省にもその情報を伝えたが、IPAではソフトウェア脆弱性を取り扱っているものの、ハードウェアシステムの脆弱性は対象外ということもあり、提供された情報についてIPAでは検証はしていない、という\[15\]。もっとも、IPAは、「ソフトウエア製品脆弱性関連情報」として、「ICカード等のソフトウエアを組み込んだハードウエア等に対する脆弱性」関連情報に関する届出を受け付けてはいる\[16\]。

なお、この件について[ソニー](../Page/ソニー.md "wikilink")は、暗号解読の事実はない、とコメントした\[17\]。

FACTAはゴシップ誌としての性質があり、この記事はソニー批判のシリーズ記事の一つであること、内容はすべて伝聞調で書かれていること、また記事中の技術的な説明に複数の誤りがみうけられるなど、記事の内容にも不審点はある。 そもそも脆弱性の検証を行うことができるほどの情報が公開されておらず、解読したとされる研究者も名乗りを上げておらず、また報道から10年以上たっても信用するに足りる組織による脆弱性・被害の報告はないことから、この脆弱性の信憑性は低いとされている。

### IDm偽装

無線部分の仕様は公開されており、カード固有番号のIDmは偽装することが可能であるため、IDmだけを使って認証することは危険である。一部のFeliCaチップを搭載したデバイスにおけるカードエミュレーションモードでは、ソフトウェアから自由にIDmを指定することが可能である。

そのため、セキュリティやプライバシーが必要なサービスやデバイスにおいては、セキュアエレメントを使用したチャレンジレスポンス方式による相互認証を行うことが必須となる。

### プライバシー問題

カード固有番号やフリー領域へのアクセスは誰でもできるため、悪意あるカードリーダーの設置やカード読み取り等によってプライバシー情報が抜き取られる恐れがある。

## FeliCaに関する規格・知的財産権

  - JIS X 6319-4: ICカード実装仕様-第4部：高速処理用ICカード（日本工業標準調査会）\[18\]
  - 特許3709946\[19\]（相互認証・通信路暗号化）

<!-- end list -->

  - 特許4268690\[20\]（相互認証用縮退鍵）

<!-- end list -->

  - [電波法](https://ja.wikipedia.org/wiki/電波法 "wikilink")上、FeliCaのリーダ・ライタは、「高周波利用設備（誘導式読み書き通信設備）」に該当し、あらかじめ[総務大臣](https://ja.wikipedia.org/wiki/総務大臣 "wikilink")から[技術基準適合証明](https://ja.wikipedia.org/wiki/技術基準適合証明 "wikilink")していることの指定（型式指定）を受ける必要がある\[21\]。

## 歴史

  - 1988年 - [ソニー](../Page/ソニー.md "wikilink")が無線ICの開発を開始。
  - 1994年 - 名称がFeliCaに決定。
  - 1994年 - 香港の[オクトパス社が採用を決定](https://ja.wikipedia.org/wiki/八達通 "wikilink")。世界で初の採用事例。
  - 1997年 - オクトパスカードが正式導入される。世界で初の本格的な導入事例\[22\]。
  - 1998年 - 広島の[スカイレールサービス](https://ja.wikipedia.org/wiki/スカイレールサービス "wikilink")が「IC定期券」として採用。国内の交通系で初めての採用\[23\]。
  - 1999年
      - ソニーがソニーファイナンスインターナショナルをはじめとした数社と共同でFeliCaを用いた電子マネー「[Edy](https://ja.wikipedia.org/wiki/楽天Edy "wikilink")」のモニターテストを[ゲートシティ大崎](https://ja.wikipedia.org/wiki/ゲートシティ大崎 "wikilink")にて実施。なお、当初は「Edy\!」の名称を使用。
      - [パレットタウン](https://ja.wikipedia.org/wiki/パレットタウン "wikilink")（東京[お台場](https://ja.wikipedia.org/wiki/お台場 "wikilink")）内の[MEGAWEB](https://ja.wikipedia.org/wiki/MEGAWEB "wikilink")にて「MEGA WEB Member's Card」の発行を開始。FeliCaを利用した館内独自のプリペイド型電子マネーサービスをはじめ、日本で初めて事前に決済クレジットカードを登録して使用する後払の「リンク式ポストペイ（後払）」方式による館内独自のクレジット型電子マネーを導入。2003年3月までカード発行と関連サービスを実施、リンク式ポストペイ方式の電子マネーは、後に[QUICPay](https://ja.wikipedia.org/wiki/QUICPay "wikilink")などに採用される。
  - 2000年
      - [JR東日本が採用を決定](../Page/東日本旅客鉄道.md "wikilink")。
      - 4月 - [メディアージュ](https://ja.wikipedia.org/wiki/メディアージュ "wikilink")（東京お台場）にて「メディアージュファンカード」の発行を開始。FeliCaを利用した館内独自の電子マネーサービスをはじめ、映画館やエンターテイメントアトラクションなどの電子チケットサービス、会員制のポイントカードサービスなどが開始される。2002年3月までカード発行と関連サービスを実施。
  - 2001年11月 - JR東日本が[Suica](../Page/Suica.md "wikilink")を導入。また、同時期にソニーグループの[ビットワレット](https://ja.wikipedia.org/wiki/ビットワレット "wikilink")がEdyの正式サービスを開始。
  - 2002年4月 - [シンガポール](https://ja.wikipedia.org/wiki/シンガポール "wikilink")の[EZ-link](https://ja.wikipedia.org/wiki/EZ-link "wikilink")が導入する（2009年にFeliCa利用中止しNFC Type A/Bへ移行済み）。
  - 2004年
      - [フェリカネットワークス](https://ja.wikipedia.org/wiki/フェリカネットワークス "wikilink")が設立される。
      - モバイルFeliCaを搭載した初めての携帯電話が[NTTドコモ](https://ja.wikipedia.org/wiki/NTTドコモ "wikilink")から発売される。当初は「[SO506iC](https://ja.wikipedia.org/wiki/SO506iC "wikilink")」「[P506iC](https://ja.wikipedia.org/wiki/P506iC "wikilink")」「[SH506iC](https://ja.wikipedia.org/wiki/SH506iC "wikilink")」「[F900iC](https://ja.wikipedia.org/wiki/F900iC "wikilink")」の4機種。
  - 2005年10月 - FeliCa ICチップの累計出荷個数が1億個を突破\[24\]。
  - 2006年12月 - 月刊誌「FACTA」2007年1月号に "ソニー激震—— 暗号破られた「電子マネー」" という記事が掲載される。
  - 2007年 - [神奈川大学](https://ja.wikipedia.org/wiki/神奈川大学 "wikilink")の[松下昭](https://ja.wikipedia.org/wiki/松下昭 "wikilink")教授らが、非接触ICカード技術の[特許](https://ja.wikipedia.org/wiki/特許 "wikilink")を巡り、計20億円の[損害賠償](https://ja.wikipedia.org/wiki/損害賠償 "wikilink")を請求。しかし2009年3月に[知的財産高等裁判所](https://ja.wikipedia.org/wiki/知的財産高等裁判所 "wikilink")が請求棄却の判決を出し\[25\]、松下は[最高裁判所への上告を断念したため](https://ja.wikipedia.org/wiki/最高裁判所_\(日本\) "wikilink")、ソニーおよびJR東日本の勝訴が[確定した](https://ja.wikipedia.org/wiki/確定判決 "wikilink")。
  - 2010年 - 日本の[Android](https://ja.wikipedia.org/wiki/Android "wikilink")スマートフォンでモバイルFeliCaが搭載される\[26\]。
  - 2016年9月16日 - [Apple](https://ja.wikipedia.org/wiki/アップル_\(企業\) "wikilink") [iPhone 7](https://ja.wikipedia.org/wiki/iPhone_7 "wikilink")、iPhone 7 Plus、Apple Watch Series 2が発売され、[NXPセミコンダクターズ](https://ja.wikipedia.org/wiki/NXPセミコンダクターズ "wikilink")のNFC A, BおよびFeliCaに対応するチップ67V04が内蔵されている。2016年発売時では、日本国内でのみFeliCaによる[Apple Payに対応したシステムとなっていた](https://ja.wikipedia.org/wiki/Apple_Pay "wikilink")。

## 脚注

### 注釈

### 出典

## 関連項目

  - [おサイフケータイ](https://ja.wikipedia.org/wiki/おサイフケータイ "wikilink")
  - [フェリカネットワークス](https://ja.wikipedia.org/wiki/フェリカネットワークス "wikilink")
  - [RFID](https://ja.wikipedia.org/wiki/RFID "wikilink")
  - [MIFARE](https://ja.wikipedia.org/wiki/MIFARE "wikilink") - 主に欧米で利用されている非接触ICカード通信規格
      - [taspo](https://ja.wikipedia.org/wiki/taspo "wikilink") - 日本で使われている[たばこ](https://ja.wikipedia.org/wiki/たばこ "wikilink")の[自動販売機](https://ja.wikipedia.org/wiki/自動販売機 "wikilink")成人認証用カード
  - [FeliCaポート](https://ja.wikipedia.org/wiki/FeliCaポート "wikilink")
      - [PaSoRi](https://ja.wikipedia.org/wiki/PaSoRi "wikilink")
  - [TransferJet](https://ja.wikipedia.org/wiki/TransferJet "wikilink")
  - [ISO/IEC 18092 (Near Field Communication, NFC)](https://ja.wikipedia.org/wiki/近距離無線通信 "wikilink") - NFC Type Fとして規格化
  - [ガラパゴス化](https://ja.wikipedia.org/wiki/ガラパゴス化 "wikilink")
  - [ガラパゴススマートフォン](https://ja.wikipedia.org/wiki/ガラパゴススマートフォン "wikilink")

## 外部リンク

  - [Sony Japan | FeliCaホームページ](https://www.sony.co.jp/Products/felica/)
  - [フェリカネットワークス株式会社](https://www.felicanetworks.co.jp/)
  - [FeliCa互換性技術情報サイト](http://www.felicatech.org)

[Category:ソニー](https://ja.wikipedia.org/wiki/Category:ソニー "wikilink") [Category:電子マネー](https://ja.wikipedia.org/wiki/Category:電子マネー "wikilink") [Category:非接触型決済](https://ja.wikipedia.org/wiki/Category:非接触型決済 "wikilink") [Category:電子決済](https://ja.wikipedia.org/wiki/Category:電子決済 "wikilink") [Category:RFID](https://ja.wikipedia.org/wiki/Category:RFID "wikilink") [Category:ICカード](https://ja.wikipedia.org/wiki/Category:ICカード "wikilink") [Category:登録商標](https://ja.wikipedia.org/wiki/Category:登録商標 "wikilink")

1.  [交通系ICカードのイノベーション](https://www.b.kobe-u.ac.jp/papers_files/2012_27.pdf) 『日経エレクトロニクス』2011年6月18日号 110頁
2.
3.
4.
5.  「ニュースリリース　[非接触ICカード用の次世代FeliCa ICチップを開発 〜新たに高セキュリティー暗号方式AESを採用〜](https://www.sony.co.jp/SonyInfo/News/Press/201106/11-066/)」『Sony Japan』 ソニー株式会社、2011年6月10日
6.  FeliCa事業部「FeliCa カード ユーザーズマニュアル 抜粋版　Version 2.01」 ソニーイメージングプロダクツ＆ソリューションズ株式会社、2017年4月
7.  「ニュースリリース　[非接触ICカード技術　“FeliCa”の使用用途を拡大 無線インターフェースモジュール“FeliCa Plug”、及び“FeliCa Lite” ICカードチップを開発](https://www.sony.co.jp/SonyInfo/News/Press/200812/08-152/)」 ソニー株式会社、2008年12月16日
8.  「[おサイフケータイについて](https://www.felicanetworks.co.jp/osaifu/)」『FeliCa Networks』 フェリカネットワークス株式会社
9.
10. [“かざすと楽しい”をFeliCaで実現――ソニーブース](http://www.itmedia.co.jp/news/articles/0903/05/news121.html) ITmedia 2009年3月5日
11. [米国進出の第1歩――FeliCaハワイプロジェクトとは](http://plusd.itmedia.co.jp/mobile/articles/0712/05/news064_2.html) ITmedia 2007年12月5日
12. [ケータイクレジットに致命的な弱点](https://facta.co.jp/article/200609061.html) FACTA 2006年9月号
13. [2007年1月号の読みどころ　ソニー激震――暗号破られた「電子マネー」](https://facta.co.jp/article/note/200701.shtml) FACTA 2007年1月号
14. [FeliCaの暗号が破られた？――ソニーは完全否定](http://www.itmedia.co.jp/news/articles/0612/20/news103.html) ITmedia 2006年12月20日 - 記事内容は非常に曖昧と指摘。
    [議論すべき時が来た組み込み機器のセキュリティ](http://www.itmedia.co.jp/news/articles/0612/26/news053.html) ITmedia 2006年12月26日 - 具体的かつ合理的な説明に欠けると指摘。
15. [議論すべき時が来た組み込み機器のセキュリティ](http://www.itmedia.co.jp/news/articles/0612/26/news053.html)、高橋睦美、ITmedia、2006年12月26日
16.  - 「届出の対象」の (1)。
17. [FeliCaの暗号が破られた?――ソニーは完全否定](http://www.itmedia.co.jp/news/articles/0612/20/news103.html)、吉岡綾乃、ITmedia、2006年12月20日
    [ソニー、「FeliCaの暗号は解読されていない」と説明](https://k-tai.watch.impress.co.jp/cda/article/news_toppage/32524.html)、関口聖、ケータイ Watch、2006年12月21日
18. [JIS X 6319](https://www.jisc.go.jp/app/jis/general/GnrJISNumberNameSearchList?show&jisStdNo=X6319)
19. [特許3709946](https://www.j-platpat.inpit.go.jp/web/PU/JPB_3709946/BEB388F33D5B56E7A9DD29A01A3A4F5C)
20. [特許4268690](https://www.j-platpat.inpit.go.jp/web/PU/JPB_4268690/5D79E8BFD08E48C70C39AA5FD14DDB1B)
21.
22.
23.
24.
25.
26.
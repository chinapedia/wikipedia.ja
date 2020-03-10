> この記事は[ETCS](https://ja.wikipedia.org/wiki/ETCS)から翻訳されています。


**ETCS** (European Train Control System) は、[ヨーロッパ](../Page/ヨーロッパ.md "wikilink")の[鉄道](../Page/鉄道.md "wikilink")における統一列車制御システムの名称である。

ETCSは、[欧州連合](https://ja.wikipedia.org/wiki/欧州連合 "wikilink") (EU) が中心になって開発している“[ERTMS](https://ja.wikipedia.org/wiki/ERTMS "wikilink")”（European Rail Traffic Management System）の一部と位置づけられている。

ETCS[プロジェクト](../Page/プロジェクト.md "wikilink")に参加しているのはヨーロッパの[鉄道事業者](https://ja.wikipedia.org/wiki/鉄道事業者 "wikilink")、鉄道産業界、鉄道関係の[研究機関](https://ja.wikipedia.org/wiki/研究機関 "wikilink")、EUや各国[政府機関](../Page/政府機関.md "wikilink")など多岐にわたっており、非常に大きなプロジェクトとなっている。

## 背景

[ヨーロッパ](../Page/ヨーロッパ.md "wikilink")の[鉄道](../Page/鉄道.md "wikilink")は、各国で個別に構築され発展してきたという歴史的背景から、[車両](../Page/車両.md "wikilink")や[線路の規格](https://ja.wikipedia.org/wiki/線路_\(鉄道\) "wikilink")、[電化方式](../Page/鉄道の電化.md "wikilink")、[信号システテムから](../Page/鉄道信号機.md "wikilink")[複線](https://ja.wikipedia.org/wiki/複線 "wikilink")での進行方向に至るまで、様々な部分で国による相違がある。そのため、複数の国にまたがって運行される国際列車は、ヨーロッパ共通規格の[客車](../Page/客車.md "wikilink")（RIC規格）や[貨車](../Page/貨車.md "wikilink")（RIV規格）を使用して、[国境](../Page/国境.md "wikilink")を越える際には牽引する[機関車](https://ja.wikipedia.org/wiki/機関車 "wikilink")を[国境駅](https://ja.wikipedia.org/wiki/国境駅 "wikilink")で付け替える方式で長年にわたって運行されてきた。

しかし、この方法では国境を越える毎に機関車を付け替えなければならず、その手間がかかることや、スピードアップの障害となる。そこで、ヨーロッパの鉄道では、国境を越えて自由に列車が行き来できる[相互運用性](https://ja.wikipedia.org/wiki/相互運用性 "wikilink")（インターオペラビリティ）を確保する努力が続けられてきた。機関車や[電車](../Page/電車.md "wikilink")や[気動車](../Page/気動車.md "wikilink")を、多くの国で運用可能なように規格を共通化することや、複数の[電源](https://ja.wikipedia.org/wiki/電源 "wikilink")方式に対応した[複電圧式の電車](../Page/複電圧車.md "wikilink")・[電気機関車](../Page/電気機関車.md "wikilink")の開発が、それである。

信号システムに関しては、電化方式や規格以上に国ごとの共通性がなく、しかも一つの国に複数の信号システムが存在する場合もあり、一つの機関車に、その機関車が運用される国の全ての信号システムを搭載しなければならない場合も数多く存在する。

ヨーロッパの鉄道における相互運用性の向上のためには、ヨーロッパで統一された信号システムの開発が必須であり、その結果、1990年代前半から、[世界鉄道連合](https://ja.wikipedia.org/wiki/世界鉄道連合 "wikilink")（UIC）が中心となって、ヨーロッパ統一信号システムの仕様策定と開発に着手することになった。これが“ETCS”である。

## ETCSの「レベル」

ETCSには「レベル」という概念が存在する。「レベル」によって機能は異なるが、各レベルは[上位互換](https://ja.wikipedia.org/wiki/上位互換 "wikilink")性が確保されることが条件となっている。即ち、上位レベルのシステムは下位レベルの機能を全て含む必要がある。

  - ETCS Level 0
    ETCSを搭載した車両がETCS対応の地上設備を備えていない路線を走行している状態をETCS Level 0と呼ぶ。この状態ではETCSの車上装置は車両の最高速度の監視のみを行い、運転士が地上信号を監視して運転を行う。
  - ETCS Level STM
    従来の信号保安装置とETCSの車上装置をSTM（Specific Transmission Module）と呼ぶ装置で繋ぎ、情報を読み替えてETCS車上装置を動作させる。既存の信号保安装置からETCSへの移行に用いるためのレベル。
  - ETCS Level 1
    地車間通信に[トランスポンダ](https://ja.wikipedia.org/wiki/トランスポンダ "wikilink")（地上子）を利用した方式で、日本の[ATS-Pに相当する](../Page/自動列車停止装置.md "wikilink")。ATS-Pと異なり、標準では[車内信号](../Page/車内信号.md "wikilink")方式であるが、地上の[信号機を存置することもできる](../Page/鉄道信号機.md "wikilink")。地上と車上の通信は「ユーロバリーズ」（Eurobalise）と呼ばれるトランスポンダを介して行う。
    車両側には“European Vital Computer（EVC）”と呼ばれる車載[コンピュータ](../Page/コンピュータ.md "wikilink")を搭載し、“ETCS Trainborne”と呼ばれる車載側システムで、地上から受け取った信号現示や開通している進路の情報を元に[ブレーキパターン](https://ja.wikipedia.org/wiki/ブレーキパターン "wikilink")を計算して保持し、列車制御を行う。列車の位置検出は[軌道回路](../Page/軌道回路.md "wikilink")によって行う。
    なお、[列車](../Page/列車.md "wikilink")の運転間隔を詰めるためEurobalise同士をループ回線で結び、進行現示時に直近のEurobaliseからブレーキパターンをキャンセルできるような構成も仕様として定義されている。
  - ETCS Level 2
    地車間通信に[デジタル無線](https://ja.wikipedia.org/wiki/デジタル無線 "wikilink")を利用した方式で、ETCS Level 1の上位互換システムである。日本の[デジタルATCに相当する](https://ja.wikipedia.org/wiki/自動列車制御装置#デジタルATC "wikilink")。デジタルATCではレール伝送により通信を行うが、ETCS Level 2では地上の[無線基地局](https://ja.wikipedia.org/wiki/無線基地局 "wikilink")（RBC：Radio Block Center）と車載[アンテナ](../Page/アンテナ.md "wikilink")の間で、[GSM-R](https://ja.wikipedia.org/wiki/GSM-R "wikilink")と呼ばれる[GSM](https://ja.wikipedia.org/wiki/GSM "wikilink")を鉄道用に改良したデジタル無線によって行う。
    列車の位置検出は[加速度センサや](https://ja.wikipedia.org/wiki/加速度計 "wikilink")[速度発電機](https://ja.wikipedia.org/wiki/速度発電機 "wikilink")などによって車上で行われ、Eurobaliseは位置情報を補正するために使用される。
    列車の現在位置情報を常に無線基地局に報告することによって信号システムが動作する。ただし、車両の遺留検知のために軌道回路は残される。
  - ETCS Level 3
    ETCS Level 2の上位互換システムである。日本の[ATACS](https://ja.wikipedia.org/wiki/ATACS "wikilink")に相当する。列車制御に必要な情報は全て車両側に搭載し、地上の無線基地局とGSM-Rで通信することにより[移動閉塞](https://ja.wikipedia.org/wiki/移動閉塞 "wikilink")を実現する。軌道回路や[ケーブルや地上の信号機は不要となる](../Page/電線.md "wikilink")。車両の遺留検知機能は車上側に移され、各列車は編成分離が発生していないことを保証しなければならない。
    Eurobaliseは列車の位置情報を補正するために使用する。

2006年現在、ETCS Level 1とETCS Level 2が実用段階に入っている。

## 採用路線

### スイス連邦鉄道(SBB)\[1\]

  - ETCS Level 2

<!-- end list -->

  - Mattstetten-Rothrist線
  - [レッチュベルクベーストンネル](../Page/レッチュベルクベーストンネル.md "wikilink")
  - [ゴッタルドベーストンネル](https://ja.wikipedia.org/wiki/ゴッタルドベーストンネル "wikilink")
  - [チェネリベーストンネル](../Page/チェネリベーストンネル.md "wikilink")

## 業界団体UNISIG

UNISIGとは、ETCSシステムの開発・製作・販売・サポートを行う業界団体である。現在、以下の6社が加盟している。カッコ内は製品名。

  - [アルカテル](https://ja.wikipedia.org/wiki/アルカテル "wikilink")（AlTrac ETCS）
  - [アルストム](https://ja.wikipedia.org/wiki/アルストム "wikilink")（ATLAS）
  - [アンサルド](https://ja.wikipedia.org/wiki/アンサルド "wikilink")
  - [インベンシス](https://ja.wikipedia.org/wiki/インベンシス "wikilink")
  - [シーメンス](../Page/シーメンス.md "wikilink")（Trainguard）
  - [ボンバルディア](../Page/ボンバルディア.md "wikilink")（INTERFLO）

## 日本国内の対応

[国際鉄道連合](../Page/国際鉄道連合.md "wikilink")（UIC）では、鉄道技術の国際標準化の動きを進めており、この一環としてETCS/ERTMSを信号保安システムの世界標準としようという動きがある。これが実現すると、日本の鉄道技術、特に信号保安技術が世界標準から外されて打撃を受けるという強い懸念がある。このため、これに対抗して[東日本旅客鉄道](../Page/東日本旅客鉄道.md "wikilink")（JR東日本）が開発した[ATACS](https://ja.wikipedia.org/wiki/ATACS "wikilink")の標準化を進めようという動きがある\[2\]。

一方、[日立製作所](../Page/日立製作所.md "wikilink")のヨーロッパにおける鉄道事業部門では、日本の[首都圏や](https://ja.wikipedia.org/wiki/首都圏_\(日本\) "wikilink")[新幹線](../Page/新幹線.md "wikilink")向けに開発した[自動列車保安装置](../Page/自動列車保安装置.md "wikilink")をベースにETCS互換の保安装置を開発し、[イギリス](https://ja.wikipedia.org/wiki/イギリス "wikilink")の[ネットワーク・レール](https://ja.wikipedia.org/wiki/ネットワーク・レール "wikilink")と共同で[2010年](https://ja.wikipedia.org/wiki/2010年 "wikilink")から[2011年](../Page/2011年.md "wikilink")にかけて実証実験を行うことを発表している\[3\]

## ヨーロッパ以外の展開と国際規格化

アジアでは、中国ではLevel1,2、インド、台湾、韓国、トルコではLevel1を採用する動きがある。 中国では、広州〜深圳〜香港の高速旅客専用線において、日立製作所と現地の業者との共同開発による上下一体のETCSが、採用、製造される模様。

## 脚注

## 関連項目

  - [ERTMS](https://ja.wikipedia.org/wiki/ERTMS "wikilink")
  - [GSM-R](https://ja.wikipedia.org/wiki/GSM-R "wikilink")
  - [ATS](../Page/自動列車停止装置.md "wikilink")
  - [ATC](../Page/自動列車制御装置.md "wikilink")

## 外部リンク

  - [ERTMS](http://www.ertms.com/)
  - [UICのETCSウェブサイト](http://etcs.uic.asso.fr/)

[Category:自動列車保安装置](https://ja.wikipedia.org/wiki/Category:自動列車保安装置 "wikilink")

1.  [スイス連邦鉄道ホームページ Train Safety ETCS](http://www.sbb.ch/en/corporation/sbb-keeps-switzerland-moving/sbb-and-safety/train-safety-etcs.html)
2.  [列車制御・輸送管理と国際規格 JR EAST Technical Review No.20 pp.3 - 6](http://www.jreast.co.jp/development/tech/pdf_20/Tech-20-03-06.pdf)（PDFファイル）
3.  [Hitachi and Network Rail collaborate on ETCS-compatible signalling demonstration](http://www.hitachi-eu.com/about/PRDetail.jsp?prid=280)
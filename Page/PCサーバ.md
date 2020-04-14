> この記事は[PCサーバ](https://ja.wikipedia.org/wiki/PCサーバ)から翻訳されています。


**PCサーバ**（ぴーしーサーバ）とは、[パーソナルコンピュータ](../Page/パーソナルコンピュータ.md "wikilink")(PC)をベースとした[サーバ](../Page/サーバ.md "wikilink")ーのこと。一般にはサーバーの中では簡易的・低価格なものが多いが、サーバー用途向けに一部機能を拡張したものもある。多くは[CPU](../Page/CPU.md "wikilink")に[インテル](https://ja.wikipedia.org/wiki/インテル "wikilink")系の[x86](https://ja.wikipedia.org/wiki/x86 "wikilink")系のプロセッサを使用し、**IAサーバ**や**x86サーバ**などとも呼ばれる。

## 特徴

### ハードウェア

基本的な設計は一般に用いられているPCとほぼ同じであるが、サーバに必要な性能や信頼性、[可用性](../Page/可用性.md "wikilink")を高めるために拡張や改良など、いくつか異なる点がある\[1\]。信頼性などに悪影響のない範囲で一般用PCと共通の部品を用いているが、おおむね上質の部品が採用される。 2018年現在の状況を以下に示す。

  - プロセッサ
    [マイクロプロセッサ](../Page/マイクロプロセッサ.md "wikilink") (CPU) は、多くのPCと同様に[インテル](https://ja.wikipedia.org/wiki/インテル "wikilink")の[x86](https://ja.wikipedia.org/wiki/x86 "wikilink")類の[アーキテクチャを源流とする](../Page/コンピュータ・アーキテクチャ.md "wikilink") "x86"系統と呼ばれるものが採用されており、特にCPU大手の米インテル社と米[AMDは](https://ja.wikipedia.org/wiki/アドバンスト・マイクロ・デバイセズ "wikilink")、それぞれ"[Xeon](../Page/Xeon.md "wikilink")"と"[EPYC](https://ja.wikipedia.org/wiki/Ryzen "wikilink")"という、"x86"の中でもサーバ向けに信頼性を高めたハイエンドなCPUファミリーを提供しており、これらがPCサーバに広く採用されている。
  - マザーボード
    通常のPCが1枚のマザーボードに1個のCPUを搭載しているのに対して、一般的なミドル/ハイエンド向けサーバ用マザーボードは1枚に2個や4個のCPUを搭載可能なものが多い。また、2000年代の中頃以降にCPUが[マルチコア](../Page/マルチコア.md "wikilink")化したことで、PCサーバ機用のマザーボードに搭載可能なCPUコア数の上限が数十個ほどに上昇した。
    普通のPCに存在せず、サーバ独特の管理機構がマザーボード上に実装されている。「マネジメントコントローラー」や「サービスプロセッサ」などの名称で呼ばれているこのICは、主CPUを含めたサーバ全体の動作について外部から遠隔操作と管理を行うための[独立したコンピュータであり](../Page/System-on-a-chip.md "wikilink")、サーバの異常時に対する非常操作や平常時の起動／停止などの管理業務を専用ネットワーク回線を通じて行えるようになっている\[2\]。この管理機構によって多数のサーバを容易に運用管理できる\[3\]。
  - メモリ
    主記憶装置である半導体メモリには、[ECC機能付きの](../Page/誤り検出訂正.md "wikilink")[DDR4 SDRAMが採用されていることが多い](https://ja.wikipedia.org/wiki/DDR4_SDRAM "wikilink")。搭載容量は1GBから32GBまでと、サーバ機の用途や要求能力によって比較的多様である\[4\]。
  - 拡張バス
    マザーボード上に小さな基板を挿入することで追加機能を加えるための拡張バスとして、[PCI Expressが一般的に採用されている](../Page/PCI_Express.md "wikilink")。サーバ機の用途によっては多くの挿入スロットとレーンを持つものや、ごく少数しか持たないもの、全く持たないものなど多様である。
  - 補助記憶装置
    基本的に全てのPCサーバが補助記憶装置である[HDDを内蔵している](https://ja.wikipedia.org/wiki/ハードディスクドライブ "wikilink")。記憶容量と速度性能はサーバ機の用途に大きく左右される。一般的な傾向としては、マルチタスク処理が主体となるアプリケーション・サーバやデータベース・サーバなど、ディスクへの断片的で高頻度な読み書き要求に対応して高速度のアクセス／転送能力がある[SASインターフェースを備えた高価格](../Page/Serial_Attached_SCSI.md "wikilink")・高性能なSASディスクが採用される傾向があり\[5\]、エントリクラスの汎用サーバやファイルサーバ、Webサーバのような比較的読み書き頻度が少ないか、連続したファイルへのアクセスが主体となる用途には、一般的なPCでも広く採用されている廉価なSATAディスクが採用されている\[6\]。HDDは電子機器の部品の中でも劣化や故障が起きる可能性が最も高いものの1つであり、コストとの兼ね合いであるが、[RAID](../Page/RAID.md "wikilink")（RADI1か5以上）や[ホットスペア](https://ja.wikipedia.org/wiki/ホットスペア "wikilink")といった機能により複数のHDDを備えて並列運用することで冗長性・信頼性を高めることが多い。また、冗長運用の有無に関わらず、故障したHDDを電源を切らずに交換可能な[ホットスワップ](../Page/ホットスワップ.md "wikilink")機能が備わっているものが多い\[7\]。
    近年の[SSD価格低下や容量増大](../Page/ソリッドステートドライブ.md "wikilink")、品質改良などにより、一部ではSSDを搭載可能なメーカオプションもある\[8\]。
  - 電源
    ローエンドPCサーバを除けば、ほとんどの電源がユニット化によって2重や3重といった多重化されており、HDDと同様に通電状態を維持したまま可動中のPCサーバから異常電源を活線挿抜できるようになっているものが多い。
  - 冷却機構
    外部から導入した冷気が単方向に流れるよう空冷ファン群が配置されており、いずれかの動作異常時にはセンサーが検知できるようになっている。
  - 筐体
    19インチラックにマウントすることを前提とした[ラックマウント型サーバ](../Page/ラックマウント型サーバ.md "wikilink")と、一般的なPCと同じようなケースに収められたものが存在する。

### ソフトウェア

稼働させる[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink")は、1980年代には[NetWare](https://ja.wikipedia.org/wiki/NetWare "wikilink")、[OS/2](https://ja.wikipedia.org/wiki/OS/2 "wikilink") LAN Server、[OpenServer](https://ja.wikipedia.org/wiki/OpenServer "wikilink")などが有力であったが、[1990年代](../Page/1990年代.md "wikilink")後半からは[Windows NT](../Page/Microsoft_Windows_NT.md "wikilink") Serverに始まる[Windows NT系のサーバ向けバージョンである](../Page/Windows_NT系.md "wikilink")[Windows Serverシリーズ](../Page/Windows_Server.md "wikilink")、あるいは[PC-UNIX](https://ja.wikipedia.org/wiki/PC-UNIX "wikilink")でもある[Linux](../Page/Linux.md "wikilink")や[FreeBSD](../Page/FreeBSD.md "wikilink")などをサーバ用にカスタマイズしたディストリビューションが主流となっている。

### 信頼性

[メインフレーム](../Page/メインフレーム.md "wikilink")や[UNIX](../Page/UNIX.md "wikilink")サーバなどと比較すると信頼性は低い。しかし多数のベンダーが参入し競争が激しく、信頼性も向上しつつある。UNIXサーバが担う大企業の基幹システムの一部や中堅企業の中核サーバとして使用できる。

### 価格

サーバとしては低価格である。日本での価格は大型機が300万円以上。最小型が50万円未満である\[9\]。2009年度の出荷台数は、約32万台（JEITA調べ）\[10\]から約50万台\[11\]。約1割は[ブレードサーバ](../Page/ブレードサーバ.md "wikilink")である（JEITA調べ）\[12\]。 保守契約を前提に24時間・365日のオンサイト保守（現地修理）が用意されている場合がある。

|          | 1998年度   | 2002年度 | 2007年度 |
| -------- | -------- | ------ | ------ |
| メインフレーム  | 51%      | 38%    | 25%    |
| UNIXサーバ  | 25%      | 41%    | 33%    |
| IAサーバ    | 9%       | 15%    | 38%    |
| 独自OSサーバ他 | 15%      | 7%     | 4%     |
| 全体の出荷金額  | 1兆4710億円 | 9867億円 | 6701億円 |

出荷金額ベースの構成比率\[13\]

日本市場でのシェア（2008年4月 - 2009年3月、出荷金額ベース、JEITA未参加も含む）は以下の通り\[14\]。

  -
    {|

| [日本電気](../Page/日本電気.md "wikilink") |24.8% | |- | [日本HP](../Page/ヒューレット・パッカード.md "wikilink") |19.7% | |- | [富士通](../Page/富士通.md "wikilink") |19% | |- | [DELL](../Page/デル.md "wikilink") |14.1% | |- | [日本IBM](../Page/日本アイ・ビー・エム.md "wikilink") |11.9% | |- | その他 |10.6% | |}

## 種類

### x86サーバ

[x86](https://ja.wikipedia.org/wiki/x86 "wikilink")系（[IA-32](../Page/IA-32.md "wikilink")系）のCPUとアーキテクチャを採用したサーバでは、現在ではx86を[64ビット](https://ja.wikipedia.org/wiki/64ビット "wikilink")に拡張したx64（[AMD64および](https://ja.wikipedia.org/wiki/x64 "wikilink")[Intel 64](https://ja.wikipedia.org/wiki/x64 "wikilink")）が主流である。主要メーカーの主な製品には以下がある。

  - [HP](../Page/ヒューレット・パッカード.md "wikilink") [ProLiant](https://ja.wikipedia.org/wiki/ProLiant "wikilink")シリーズ
  - [DELL](../Page/デル.md "wikilink") [PowerEdge](../Page/PowerEdge.md "wikilink")シリーズ
  - [IBM](../Page/IBM.md "wikilink") [System x](../Page/System_x.md "wikilink") シリーズ
  - [SUN](../Page/サン・マイクロシステムズ.md "wikilink") Fire X シリーズ
  - [富士通](../Page/富士通.md "wikilink") [PRIMERGY](https://ja.wikipedia.org/wiki/PRIMERGY "wikilink")シリーズ、[PRIMEQUEST](../Page/PRIMEQUEST.md "wikilink") シリーズ （現在のモデル）
  - [日立](../Page/日立製作所.md "wikilink") [HA8000シリーズ](../Page/日立アドバンストサーバHA8000.md "wikilink") （[日本ユニシス](https://ja.wikipedia.org/wiki/日本ユニシス "wikilink")に[OEM](../Page/OEM.md "wikilink")供給）
  - [NEC](../Page/日本電気.md "wikilink") [Express5800](../Page/Express5800.md "wikilink") シリーズ （現在の大多数のモデル [東芝](../Page/東芝.md "wikilink")、[三菱電機](../Page/三菱電機.md "wikilink")などに[OEM](../Page/OEM.md "wikilink")供給）
  - [ユニシス](../Page/ユニシス.md "wikilink") [ES7000](https://ja.wikipedia.org/wiki/ES7000 "wikilink") シリーズ

### IA-64サーバ

インテル独自の[64ビット](https://ja.wikipedia.org/wiki/64ビット "wikilink")アーキテクチャである[IA-64](../Page/IA-64.md "wikilink")系のCPU（[Itanium](../Page/Itanium.md "wikilink")）を搭載したサーバである。広義の「PCサーバ」では、IA-64サーバを含む場合がある。当初はインテル系CPUを採用したサーバとしては高性能・高信頼性・高価格なハイエンドサーバであったが、現在では上述のx64（[AMD64および](https://ja.wikipedia.org/wiki/x64 "wikilink")[Intel 64](https://ja.wikipedia.org/wiki/x64 "wikilink")）の性能が向上して市場の主流となったため、IA-64サーバは[ニッチ市場](../Page/ニッチ市場.md "wikilink")化が進んだ。またインテルも2006年の[Intel 64命名後は](https://ja.wikipedia.org/wiki/x64 "wikilink")「IA-64」の名称の使用が減っている。主要メーカーの主な製品には以下がある。

  - [HP Integrity](../Page/HP_Integrity.md "wikilink") シリーズ （[NEC](../Page/日本電気.md "wikilink")、[日立](../Page/日立製作所.md "wikilink")、[三菱電機](../Page/三菱電機.md "wikilink")などに[OEM](../Page/OEM.md "wikilink")供給）
  - 富士通 [PRIMEQUEST](../Page/PRIMEQUEST.md "wikilink") シリーズ （過去のモデル）
  - NEC [Express5800](../Page/Express5800.md "wikilink") シリーズ （過去のハイエンドモデルのみ）
  - ユニシス [ES7000](https://ja.wikipedia.org/wiki/ES7000 "wikilink") シリーズ (過去の一部モデル）

## 参照・出典

## 関連項目

  - [サーバ](../Page/サーバ.md "wikilink")
  - [x86](https://ja.wikipedia.org/wiki/x86 "wikilink")
      - [IA-32](../Page/IA-32.md "wikilink")
      - [AMD64](https://ja.wikipedia.org/wiki/x64 "wikilink")
      - [Intel 64](https://ja.wikipedia.org/wiki/x64 "wikilink")
  - [IA-64](../Page/IA-64.md "wikilink")
      - [Itanium](../Page/Itanium.md "wikilink")
      - [Itanium 2](https://ja.wikipedia.org/wiki/Itanium_2 "wikilink")
  - [オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink")
      - [Windows Server](../Page/Windows_Server.md "wikilink")
      - [PC-UNIX](https://ja.wikipedia.org/wiki/PC-UNIX "wikilink")
      - [Linux](../Page/Linux.md "wikilink")
      - [CentOS](../Page/CentOS.md "wikilink")

## 外部リンク

  - [x86サーバ に関する情報 - ZDNet Japan](http://japan.zdnet.com/tag/x86%E3%82%B5%E3%83%BC%E3%83%90/)

[Category:サーバ_(ハードウェア)](https://ja.wikipedia.org/wiki/Category:サーバ_\(ハードウェア\) "wikilink")

1.  通常、一般的なPCが備えるがPCサーバでは省かれている機能に、音声出力がある。また、映像出力やUSBについても省かれている機種があり、これらでは、映像出力やキーボードやマウスを用いるためには、増設カードを別途購入する必要がある。
2.
3.  このサーバ専用の管理機構が備わる以前のPCサーバは一般的なPCに近い構成であり、設定などの管理は1台ごとに[シリアルポート](../Page/シリアルポート.md "wikilink")を経由してキーボード／ディスプレイを備えた[VT100](../Page/VT100.md "wikilink")のような[ビデオ表示端末](https://ja.wikipedia.org/wiki/ビデオ表示端末 "wikilink")を接続して運用する必要があった。
4.
5.  SASディスクはインターフェースの違いを示すが、実製品では高い回転数やコントローラの高機能化、経年劣化の低減などの高性能化・高信頼性化・長寿命化が図られており、特にアクセス性能を求めるものでは「3.5インチ型」と呼ばれる外形のまま、内部の磁気記録円盤（プラッタ）を2.5インチへ縮小して高回転化した製品がある。このようにSASディスクは、記憶容量の大きなものはあまり存在しない。
6.  [サーバーを特徴付けるハードウェアのいろいろ](http://ascii.jp/elem/000/000/571/571154/index-2.html) - ASCIIjp
7.  安価なローエンドのPCサーバでも単純なRAID構成を当初から、またはオプションで採れるようになっている。
8.  [HP社の例](http://h50146.www5.hp.com/products/servers/proliant/storage/diskstorage.html)
9.
10. 国内シェア・トップ5のうちDELLと日本HPは自主統計に未参加であり、含まれていない。
11.
12.
13.
14.
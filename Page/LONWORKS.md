> この記事は[LONWORKS](https://ja.wikipedia.org/wiki/LONWORKS)から翻訳されています。


**LONWORKS**（ロンワークス）とは、[アメリカ合衆国](https://ja.wikipedia.org/wiki/アメリカ合衆国 "wikilink")エシェロン社が開発した[ネットワーク](../Page/コンピュータネットワーク.md "wikilink")[技術](../Page/技術.md "wikilink")で、[設備](../Page/設備.md "wikilink")の[知的分散制御を行う技術である](https://ja.wikipedia.org/wiki/デジタル制御工学#分散形 "wikilink")。

主に、[ビル](https://ja.wikipedia.org/wiki/ビルディング "wikilink")[設備管理](../Page/設備管理.md "wikilink")の[オートメーション](https://ja.wikipedia.org/wiki/オートメーション "wikilink")、[産業](../Page/産業.md "wikilink")設備のオートメーション、[エネルギー](https://ja.wikipedia.org/wiki/エネルギー "wikilink")の監視・制御などといった設備制御のオートメーションシステム等において用いられる。

LONWORKSは、[オープンシステムであるため](../Page/オープンシステム_\(コンピュータ\).md "wikilink")、[センサ](../Page/センサ.md "wikilink")、制御ユニット、手元スイッチ、監視装置などの[制御システム](../Page/制御システム.md "wikilink")に繋がる機器の[マルチベンダー](https://ja.wikipedia.org/wiki/マルチベンダー "wikilink")化（複数メーカーで機器を販売すること）が可能となる。そのため、様々な[メーカー](https://ja.wikipedia.org/wiki/メーカー "wikilink")の制御機器の中から利用者や設計者が機器を選択し、組み合わせることによって最適な制御システムを構築することができる。

日本では、非営利活動法人であるLONMARK JAPAN が、LONWORKSを中心としたネットワークシステムの標準化、普及促進等を行っている。

## 起源

LonWorks はエシェロン社の集積回路、撚線対通信技術、ルーター、ネットワーク管理ソフトウェアなどの製品に基づいた技術である。1999年、LonWorks の通信プロトコル **LonTalk** は[ANSI](https://ja.wikipedia.org/wiki/ANSI "wikilink")に提出され、標準規格として採用された（**ANSI/EIA709.1-B**）。エシェロンの電力線/撚線対通信技術も ANSI に提出され標準規格として採用されている。

## 浸透と利用

ANSI/EIA709.1 は IEEE 1473-L の基盤として採用され、[アメリカ鉄道協会](https://ja.wikipedia.org/wiki/アメリカ鉄道協会 "wikilink") (AAR) の列車用ブレーキシステム、IFSF（ガソリンスタンドの欧州標準規格）、SEMI（半導体製造業界団体）、EN14908（欧州ビル自動化標準規格）などに採用された。[ASHRAE](../Page/アメリカ暖房冷凍空調学会.md "wikilink")/ANSI のビル自動化の標準規格 [BACnet](../Page/BACnet.md "wikilink") のデータリンク層と物理層にも採用されている。また、中国はこの技術を制御規格 GB/Z 20177.1-2006 および、ビル自動化通信規格 GB/T 20299.4-2006 として採用した。2007年、[CECEDはこのプロトコルを家電機器の制御監視の](https://ja.wikipedia.org/wiki/欧州家電機器委員会 "wikilink") AIS (Application Interworking Specification) 規格の一部として採用した。

2006年までに約6000万台の機器で LonWorks 技術が実装されている。

## 技術的詳細

物理層としては撚線対と電力線搬送通信が LonWorks 技術を含む各種標準規格で利用されている。また、LonWorks プラットフォームでは[IPトンネリング規格](../Page/Internet_Protocol.md "wikilink") **EIA-852** を使って LonWorks ベースのネットワークとIPベースのネットワークの接続を行っている。LonWorks ベースの制御システムでは何らかのIPとの接続があることが多く、ユーザーインタフェースレベルや制御基盤にIPが使われる。

当初、エシェロンの設計した8ビットプロセッサ "Neuron chip" が LonTalk ノードを実装するのに不可欠であり、LonWorks ベースのハードウェアのほとんどで使われている。その後、汎用プロセッサでプロトコルを実装可能となった。しかし、まだ実際に使用された例は少ない。

## 利用例

  - [半導体素子](../Page/半導体素子.md "wikilink")[製造業](../Page/製造業.md "wikilink")
  - 照明制御システム
  - 電力制御システム
  - [暖房](../Page/暖房.md "wikilink")および空調システム
  - セキュリティシステム
  - [ホームオートメーション](../Page/ホームオートメーション.md "wikilink")
  - [家電機器](https://ja.wikipedia.org/wiki/家電機器 "wikilink")
  - [街灯](../Page/街灯.md "wikilink")と監視・制御
  - ガソリンスタンド制御 (IFSF)

## SNVTs (Standard Network Variable Types)

LonWorks を使ったシステムでの相互運用性の鍵となるのは、物理的実体を表す変数の標準化である。この標準リストは [LonMark International](http://www.lonmark.org/) が保守しており、これを Standard Network Variable Types (SNVTs) と呼ぶ。例えば温度SNVTを使ったサーモスタットは0から65535の値を生成し、それが摂氏 -274度から 6279.5度の温度を表している。

## 関連項目

  - [中央監視装置](../Page/中央監視装置.md "wikilink")
  - [制御工学](../Page/制御工学.md "wikilink")
  - [デジタル制御工学](../Page/デジタル制御工学.md "wikilink")
  - [プログラマブルロジックコントローラ](../Page/プログラマブルロジックコントローラ.md "wikilink")

## 参考文献

  - [IEC - LonWorks Technology tutorial](http://www.ieclon.com/LonWorks/LonWorksTutorial.html)
  - LonWorks Protocol information
  - [Additional Neuron C Data Element Storage Information](http://www.microsym.com/editor/assets/Neuron_C_storage.pdf)

## 外部リンク

  - [LONMARK JAPAN](http://lmjapan.org/)
  - [Echelon Corporation](http://www.echelon.com/)
  - [LonMark International](http://www.lonmark.org/)
  - [Cypress Semiconductor Neuron Chip](http://www.cypress.com/?id=1353)
  - [東芝セミコンダクター](http://www.semicon.toshiba.co.jp/openb2b/websearch/resultDo.jsp) LON用LSI
  - [DTI - Examples of mixed ethernet and lonworks architectures](http://www.dti-be.com/lon/en/architecture.htm)

[Category:制御工学](https://ja.wikipedia.org/wiki/Category:制御工学 "wikilink") [Category:ファクトリーオートメーション](https://ja.wikipedia.org/wiki/Category:ファクトリーオートメーション "wikilink") [Category:ビルオートメーション](https://ja.wikipedia.org/wiki/Category:ビルオートメーション "wikilink") [Category:ホームオートメーション](https://ja.wikipedia.org/wiki/Category:ホームオートメーション "wikilink")
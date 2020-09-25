> この記事は[CLUSTERPRO](https://ja.wikipedia.org/wiki/CLUSTERPRO)から翻訳されています。


**CLUSTERPRO**（クラスタープロ）は、[NECによる汎用オープン系高可用](../Page/日本電気.md "wikilink")[クラスターパッケージのこと](https://ja.wikipedia.org/wiki/コンピュータ・クラスタ "wikilink")。

## 機能概要

[Linux](../Page/Linux.md "wikilink"),[Solaris](../Page/Solaris.md "wikilink")及び[WindowsNT系OSにおいて](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")、各種アプリケーションを簡易なシェルによってラッピングし、クラスタ対応アプリケーションとして動作させる事が可能な高可用クラスターパッケージ。一般的なディスクハートビートと、その資源確保によるサバイバルノードの決定プリミィティブ（ロックディスク)を採用しており、確実な[スプリットブレインシンドローム](../Page/スプリットブレインシンドローム.md "wikilink")を抑止する機能を持つ。

## 経緯

90年代中頃、NECとして[UNIX](../Page/UNIX.md "wikilink")[サーバ](../Page/サーバ.md "wikilink")は自社サーバの[UX/4800](https://ja.wikipedia.org/wiki/UX/4800 "wikilink")＆[MC-SAVER](https://ja.wikipedia.org/wiki/MC-SAVER "wikilink")によるクラスターと[HP社からの](../Page/ヒューレット・パッカード.md "wikilink")[OEM](../Page/OEM.md "wikilink")サーバ＆[MC/ServiceGuard](https://ja.wikipedia.org/wiki/MC/ServiceGuard "wikilink")により競争力を維持していたが、ビジネス上の牙城であるPC系サーバ(旧オフコンやミニコン)の[Microsoft Windows NT系](../Page/Microsoft_Windows_NT.md "wikilink")[OSに向け](../Page/オペレーティングシステム.md "wikilink")、同等の機能を持つクラスターパッケージを欲していた。

[PC-9801時代から対](../Page/PC-9800シリーズ.md "wikilink")[IBM](../Page/IBM.md "wikilink")として共闘的な関係にあり、関係の深い[マイクロソフト](../Page/マイクロソフト.md "wikilink")からのクラスターサーバ (MSCS) が出される直前であったが、期待していた機能や信頼性が提供されない事で自社パッケージの開発に踏み切った。 当初はWindows向けに作成されたものであったが、機能的に商用UNIX用のクラスターパッケージに劣り、特に目立つ物ではなかった。

その後、NEC自体が商用UNIXの自社開発から手を引き、OEMした[HP-UX](../Page/HP-UX.md "wikilink")への機能強化・ロバスト化、業界全体のLinuxへの傾注や[汎用機技術のUNIX](../Page/メインフレーム.md "wikilink")/Linuxミドルウェアへの転用という方針変更が行われ、Windows版と共に、いち早く[Linux](../Page/Linux.md "wikilink")サポートへと動き出した。

その動きの中で、MC-SAVERでの実装技術やMC/ServiceGuardでの運用経験などのオープンシステムの高可用ノウハウ(例えばデータベースやアプリケーションサーバを管理するエージェントをオプション提供)が取り込まれ、非常に競争力のあるパッケージとして実績を積み上げている。

元々、NECの自社ブランドサーバである[Express5800](../Page/Express5800.md "wikilink")シリーズでの動作をサポートしていたが、[日立製作所](../Page/日立製作所.md "wikilink")/[三菱電機](../Page/三菱電機.md "wikilink")/[日本IBM](https://ja.wikipedia.org/wiki/日本IBM "wikilink")/[DELL](https://ja.wikipedia.org/wiki/DELL "wikilink")/[EMCといった他大手HWベンダがOEMにて販売しており](https://ja.wikipedia.org/wiki/EMCコーポレーション "wikilink")、金融系でのLinuxクラスタパッケージの主流となっている。 この中で、日本IBMと日立は東芝の[ClusterPerfect](https://ja.wikipedia.org/wiki/ClusterPerfect "wikilink")と[サイオステクノロジー](../Page/サイオステクノロジー.md "wikilink")（旧スチールアイテクノロジー）の[LifeKeeper](https://ja.wikipedia.org/wiki/LifeKeeper "wikilink")との並列したマルチOEM体制で販売している。

そのため、日本国内では高可用クラスターパッケージとして、大きなシェアを確保している。

海外については[英語](../Page/英語.md "wikilink")版（おもに[アメリカ](https://ja.wikipedia.org/wiki/アメリカ合衆国 "wikilink")、[ヨーロッパ](../Page/ヨーロッパ.md "wikilink")向け）と[中国語](../Page/中国語.md "wikilink")版、[韓国語](https://ja.wikipedia.org/wiki/韓国語 "wikilink")版が存在するが、英語版については商標権の問題により商標名を「ExpressCluster」としている。中国語版、韓国語版は[サムスン](https://ja.wikipedia.org/wiki/サムスン "wikilink")などへのOEM製品がメインであり、NECの社名や「CLUSTERPRO」の名称を出していない場合もある。

## 製品名の遷移

  - (ver4.xまで) ActiveRecoveryManager (あくてぃぶ りかばりー まねーじゃ)
  - (ver5.0～8.0) CLUSTERPRO (くらすたーぷろ)
  - (ver1.0＝旧ver9.0) CLUSTERPRO X (くらすたーぷろ えっくす)
  - CLUSTERPRO D (くらすたーぷろ でぃ)

## 関連項目

  - [密結合クラスター](../Page/密結合クラスター.md "wikilink")
  - [コンピュータ・クラスター](../Page/コンピュータ・クラスター.md "wikilink")

## 外部リンク

  - [シグマグリッド](http://www.sw.nec.co.jp/products/sigmagrid/)
  - [Express5800シリーズ](http://www.express.nec.co.jp/pcserver/index.html)
  - [クラスタープロホームページ](http://www.nec.co.jp/pfsoft/clusterpro/)
  - [NEC ExpressCluster](http://www.necam.com/entsw/ExpressCluster/) （NEC-AM（アメリカ））

[Category:日本電気の製品](https://ja.wikipedia.org/wiki/Category:日本電気の製品 "wikilink") [Category:システムソフトウェア](https://ja.wikipedia.org/wiki/Category:システムソフトウェア "wikilink")
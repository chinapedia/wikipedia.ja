> この記事は[VERITAS](https://ja.wikipedia.org/wiki/VERITAS)から翻訳されています。


**VERITAS**（**ベリタス**）とは、アメリカの情報管理を中心としたIT企業である**Veritas Technologies**（**ベリタス・テクノロジーズ**）のこと。元々の源流は、後に、[フェイスブック](https://ja.wikipedia.org/wiki/フェイスブック "wikilink")のコンサルタントとして引き抜かれるジェフ・ロスチャイルドらにより、[UNIX](../Page/UNIX.md "wikilink")系の各種基幹系[ミドルウェア](../Page/ミドルウェア.md "wikilink")の開発・販売を中心にビジネス展開をしていた**VERITAS Software**である。

2004年に[シマンテック](../Page/シマンテック.md "wikilink")に買収合併されたが、2015年にシマンテックから情報管理部門が分割化される際、**VERITAS**の名前が復活することとなった。当初の社名は **Tolerant Systems**（**トレラント・システムズ**）。シマンテックからの買収後、引き抜かれる迄は、悠々自適な生活を送っていた。

## トレラント・システムズ時代

**トレラント・システムズ**（**Tolerant Systems**）は、Eli Alon と Dale Shipely （共に元[インテル](https://ja.wikipedia.org/wiki/インテル "wikilink")従業員）が1983年に設立した[フォールトトレラントシステム](../Page/フォールトトレラントシステム.md "wikilink")型コンピュータの製造会社。そのシステムは小さな機能ブロックを積み重ねて構築するというものだった。

トレラント社は当初[ナショナル・セミコンダクタ](https://ja.wikipedia.org/wiki/ナショナル・セミコンダクタ "wikilink")の[NS32016](../Page/NS320xx.md "wikilink")[マイクロプロセッサ](../Page/マイクロプロセッサ.md "wikilink")を使用していたが、完全な32ビットプロセッサである[NS32032が使用可能になるとそちらにアップグレードした](../Page/NS320xx.md "wikilink")。各機能ブロックにはOS用プロセッサとI/O用プロセッサ（共に320xx）が搭載されている。OS用プロセッサ上では *TX* と呼ばれる[UNIX](../Page/UNIX.md "wikilink")系OSが動作し、I/O用プロセッサ上ではトレラント独自の[リアルタイム](../Page/リアルタイム.md "wikilink")カーネルが動作していた。

各機能ブロックは2本の[イーサネット](../Page/イーサネット.md "wikilink")接続口を持ち、他の機能ブロックと接続することでフォールトトレラントシステムを構築する。さらに独自のI/Oシステムも開発し、最大16台の周辺装置を接続可能（総延長50フィートまで）で、3Mバイト/s という高速なインターフェイスであった。トレラントはこのI/Oシステム向けにディスク・コントローラ、通信インターフェイスプロセッサ(CIP)、磁気テープコントローラなども独自開発した。

通信インターフェイスプロセッサ(CIP)もNS32016プロセッサをベースとしており、12または16個のシリアルポートを制御する。CIP上でソフトウェアを実行し、接続した端末群をインテリジェントに利用することが可能となっていた。

ソフトウェアは[フォールトトレラント性](https://ja.wikipedia.org/wiki/フォールトトレラント性 "wikilink")を持たせるためにチェックポインティング技術を使用している。ハードウェアの故障時に別のプロセッサでアプリケーションをロールバックして実行するには、アプリケーション内にチェックポイントを埋め込んで強化する必要があった。

トレラントは今日の[RAID](../Page/RAID.md "wikilink")システムの先駆けとなる[ジャーナルファイルシステム](https://ja.wikipedia.org/wiki/ジャーナルファイルシステム "wikilink")とディスクの内容の多重化を行うシステムも開発した。

## 旧VERITAS時代

1989年、トレラント・システムズはハードウェア事業を捨て、既に開発済みのジャーナルファイルシステムをベースとした製品をNTおよびUNIXシステム向けに開発販売する会社となり、社名を VERITAS Software（ベリタス・ソフトウェア）に変更した。

1980年代終盤に商用UNIXにおける論理ボリュームマネージャ及びジャーナルファイルシステム製品をいち早く提供すべく、AT\&T [UNIX Systems Laboratoriesの協力を得て](https://ja.wikipedia.org/wiki/UNIX_Systems_Laboratories "wikilink")、自社のハイアベイラビリティ・オペレーティングシステムから[UNIX System V](../Page/UNIX_System_V.md "wikilink") Release 4向けに価値あるコードを抽出し、製品化した。これが[VxFS](https://ja.wikipedia.org/wiki/VxFS "wikilink")である。

この機能に各商用UNIXベンダが目を付け、1990年にIBMが[AIX](../Page/AIX.md "wikilink")V3に、1992年に日立の[HI-UX](../Page/HI-UX.md "wikilink")に、1993年にHPの[HP-UX](../Page/HP-UX.md "wikilink")/NECの[UX/4800](https://ja.wikipedia.org/wiki/UX/4800 "wikilink")に、1994年にOracle(アライアンス)とそれぞれの製品及び商用UNIXでのサポート契約を結び、多くのUNIXに実装されている。

このジャーナルファイルシステム及びボリュームマネージャ機能([VxVM](https://ja.wikipedia.org/wiki/VxVM "wikilink"))により、UNIXの信頼性/可用性は急速に高まり、UNIXが[Windows系](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")[OSより遥かに信頼性が高いという神話を作り上げる過程の一端を担っていた会社である](../Page/オペレーティングシステム.md "wikilink")。 (当時Windows3.1の時代でありボリュームマネージャを有しておらず,ジャーナルファイルシステムもWindowsNT以外では利用できなかった)

[SUNサーバにて高可用クラスターを構成する際にも](../Page/サン・マイクロシステムズ.md "wikilink")、Sun製のSunClusterを使わずにVERITAS社のClusterServerを標準的に使うなど、UNIXにてビジネスシステムを構築した経験を持つ人間は、必ずこの会社のパッケージを目にしている。

VERITASのソフトウェア製品は主にストレージ管理の領域に特化している。最初の商用[ジャーナルファイルシステム](https://ja.wikipedia.org/wiki/ジャーナルファイルシステム "wikilink")である[VxFS](https://ja.wikipedia.org/wiki/VxFS "wikilink")、小規模バックアップソフトウェア Backup Exec、企業レベルの大規模[バックアップ](../Page/バックアップ.md "wikilink")ソフトウェアNetBackupなどがある。1997年にOpenVision Technologiesを買収し、1999年に[シーゲイト・テクノロジー](../Page/シーゲイト・テクノロジー.md "wikilink")のネットワーク/ストレージ管理部門を買収。これによってVERITASは世界でも五本の指に入るソフトウェア企業となった。

2004年、VERITASとシマンテックは135億ドルと見積もられる合併計画を発表した。これはソフトウェア企業同士の合併としては史上最大規模であった。2005年6月24日、両社の株主は合併を了承し、同年7月2日に合併を完了。社名はシマンテックとなった。

## 新生VERITAS時代

2014年10月、シマンテックは情報管理部門とセキュリティ部門の二つに会社を分割することを発表した。\[1\]2015年1月、シマンテックは新たに設立される情報管理部門の会社名をVeritas Technologies（ベリタス・テクノロジーズ）と発表した。\[2\]

2015年8月、シマンテックはVeritas Technologiesを[カーライル・グループ](../Page/カーライル・グループ.md "wikilink")主導で投資家に80億ドルで売却し、2016年1月1日までに売却手続きを完了させると見込むことを発表した。\[3\]

## 脚注

## 外部リンク

いずれも英文

  - [Official website of VERITAS](http://www.veritas.com/)
  - [Symantec Corp](http://www.symantec.com/)

[Category:シマンテック](https://ja.wikipedia.org/wiki/Category:シマンテック "wikilink") [Category:かつて存在したアメリカ合衆国のソフトウェア会社](https://ja.wikipedia.org/wiki/Category:かつて存在したアメリカ合衆国のソフトウェア会社 "wikilink")

1.
2.
3.
> この記事は[GCOS](https://ja.wikipedia.org/wiki/GCOS)から翻訳されています。


**GCOS**（ジーコス、***G**eneral **C**omprehensive **O**perating **S**ystem*）は、[メインフレーム](../Page/メインフレーム.md "wikilink")向けの[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink") (OS) のファミリー。[1962年](../Page/1962年.md "wikilink")、[ゼネラル・エレクトリック](https://ja.wikipedia.org/wiki/ゼネラル・エレクトリック "wikilink") (GE) が開発したものが起源となっており、当初の名称は GECOS (*the **G**eneral **E**lectric **C**omprehensive **O**perating **S**upervisor*)であった。

今日でもごく一部で使用されている。このOS上の[プログラムは](../Page/プログラム_\(コンピュータ\).md "wikilink") GMAP[アセンブラ](../Page/アセンブリ言語.md "wikilink")、[COBOL](../Page/COBOL.md "wikilink")、[FORTRAN](../Page/FORTRAN.md "wikilink")、[ALGOL](../Page/ALGOL.md "wikilink")などで書かれることが多い。[日本電気](../Page/日本電気.md "wikilink")の[ACOS](https://ja.wikipedia.org/wiki/ACOS "wikilink")はGCOSから派生したOSである。

## システムアーキテクチャとコンセプト

GCOSでは[プロセス](../Page/プロセス.md "wikilink")という概念を使用する。これは[プロセッサ](../Page/プロセッサ.md "wikilink")上で実行される命令列と対応するデータの集合である。[マルチスレッド](https://ja.wikipedia.org/wiki/マルチスレッド "wikilink")の概念もある。また、[プロセスグループ](../Page/プロセスグループ.md "wikilink")に相当する概念もあり、同時にロードされスケジュールされるプロセス群を意味する（その意味では、UNIXのプロセスグループではなく、ギャングスケジューリングに近い。→[スケジューリング](../Page/スケジューリング.md "wikilink")）。GCOSには[セマフォ](https://ja.wikipedia.org/wiki/セマフォ "wikilink")もあり、プロセス間の[同期に使用する](https://ja.wikipedia.org/wiki/同期_\(情報工学\) "wikilink")。

各プロセスは自身の[アドレス空間](../Page/アドレス空間.md "wikilink")を持ち、そこでのアクセス権は*READ*、*WRITE*、*EXECUTE*の混合である。[アドレス空間](../Page/アドレス空間.md "wikilink")は[セグメント化されており](../Page/セグメント方式.md "wikilink")、プロセス間で[データ](../Page/データ.md "wikilink")を共有することもできる。特権管理は[リングプロテクション](../Page/リングプロテクション.md "wikilink")である。各プロセスはいずれかのリングに属し、低いリングであれば、より高い特権を持つことになる。

このOSは[対称型マルチプロセッシング](../Page/対称型マルチプロセッシング.md "wikilink")をサポートしている。これは[ファームウェア](../Page/ファームウェア.md "wikilink")に組み込まれた[マイクロカーネル](https://ja.wikipedia.org/wiki/マイクロカーネル "wikilink")に基づくものである。また、ファームウェアにその機能が無くともエミュレーションで実現してもそれほど性能は低下しない。

## 歴史

GEは36ビットの[GE-635向けに](../Page/GE-600シリーズ.md "wikilink") GECOS-IIを開発した（[1962年](../Page/1962年.md "wikilink")〜[1964年](../Page/1964年.md "wikilink")）。噂に反して GECOS は[System/360](https://ja.wikipedia.org/wiki/System/360 "wikilink")のクローンではなかった（[ジャーゴンファイル](../Page/ジャーゴンファイル.md "wikilink")では噂を真に受けて「System/360の素早く汚いクローン」としていたため、この噂が長生きしてしまった）。GE-635 のアーキテクチャは360とは全く異なり、GCOSも360のOSとは全く違う。その差が歴然とするのは、第二世代で[タイムシェアリングシステム](../Page/タイムシェアリングシステム.md "wikilink") (TSS) と[バッチ処理](https://ja.wikipedia.org/wiki/バッチ処理 "wikilink")を同時にサポートした点である。

GEのコンピュータ部門が[ハネウェル](https://ja.wikipedia.org/wiki/ハネウェル "wikilink")のものとなった後、GECOS-IIIはGCOS-3に改名された。対応ハードウェアもハネウェル6000シリーズとなった。[1974年](../Page/1974年.md "wikilink")、ハネウェルは自社の従来からのコンピュータなどとの統一性をもたせるため、「シリーズ60」という名称で統一し、6000シリーズはその中の「レベル66」とされた。ハネウェルの[ヨーロッパ](../Page/ヨーロッパ.md "wikilink")での系列会社[ハネウェル-ブルは同じシリーズ](https://ja.wikipedia.org/wiki/Bull "wikilink")60の「レベル64」という新しい系列の開発を開始した（後に DPS-7 となった）。

それに伴ってGCOSという名称は、ハネウェルの全製品で使われることになった。

  - GCOS-3:レベル66(つまりGE-600シリーズの後継)用。[DTSS](../Page/DTSS.md "wikilink")の影響がある。[ACOS-6](../Page/ACOS-6.md "wikilink")に相当。
    GCOS-64:レベル64用。ハネウェルとハネウェル-ブルの開発。新たに開発されたシリーズであり、GCOS-3をベースとしている。[ACOS-4](../Page/ACOS-4.md "wikilink")に相当。
    GCOS-62:レベル62用。[イタリア](../Page/イタリア.md "wikilink")で開発された32ビット小型機向けOS。[ACOS-2](../Page/ACOS-2.md "wikilink")に相当。
    GCOS-61:レベル61用。[フランス](https://ja.wikipedia.org/wiki/フランス "wikilink")で開発した卓上機向けOS
    GCOS-6:レベル6用。16ビット[ミニコンピュータ](https://ja.wikipedia.org/wiki/ミニコンピュータ "wikilink")用OS

1979年、再度シリーズ名称の変更が行われた。

  - レベル66→**DPS-8**:対応OSは GCOS-3→**GCOS-8**
  - レベル64→**DPS-7**:対応OSは GCOS-64→**GCOS-7**
  - レベル62→**DPS-4**:対応OSは GCOS-62→**GCOS-4**
  - レベル6→**DPS-6**:対応OSは **GCOS-6**

この改称は顧客を混乱させることになった。例えば、突然GCOS-8となったGCOS-3は、この発表後も数年間GCOS-3の名前でも保守が行われた。なお、GCOS-61（レベル61）は[マイクロプロセッサ](../Page/マイクロプロセッサ.md "wikilink")の登場と共に消えた。

GCOS-3（と後継のGCOS-7およびGCOS-8）は[CODASYL](../Page/CODASYL.md "wikilink")[データベース](../Page/データベース管理システム.md "wikilink") Integrated Data Store (IDS) を備えていた。これは後にさらに成功した[IDMS](https://ja.wikipedia.org/wiki/IDMS "wikilink")のモデルとなった。

いくつかのトランザクション処理モニター（TPモニター）がGCOS-3およびGCOS-8向けに設計された。最初のGCOS-3での試みは、[UNIX](../Page/UNIX.md "wikilink")風に言えば各[トランザクション](../Page/トランザクション.md "wikilink")を処理するために新たに[プロセス](../Page/プロセス.md "wikilink")を生成する方式である。IBMの顧客はもっと効率的な方式、すなわちマルチスレッドで[リソース](https://ja.wikipedia.org/wiki/リソース "wikilink")を共有して[メッセージを待ち受ける方式を望んだ](https://ja.wikipedia.org/wiki/メッセージ_\(コンピュータ\) "wikilink")。このような機能はサブシステムとして実装された。

GCOS-3は間もなくもっと適切なTPモニター Transaction Driven System (TDS) を装備した。TDS はハネウェルの開発したものである。これは後にTP8としてGCOS-8上で拡張された。TDSとその開発は、同様のアーキテクチャであるIBMの[CICS](../Page/CICS.md "wikilink")より先行しており、成功した機能であった。同様の機能がGCOS-7にもTDSとして組み込まれた。

GCOS-6およびGCOS-4は、[MC68000](../Page/MC68000.md "wikilink")ベースの[UNIX](../Page/UNIX.md "wikilink")系OSの動作するミニコンピュータで置き換えられた。さらに、その後[PowerPC](../Page/PowerPC.md "wikilink")ベースのサーバとなっている。GCOS-6は[AIX](https://ja.wikipedia.org/wiki/AIX "wikilink")上の[エミュレータ](../Page/エミュレータ.md "wikilink")で動作した。GCOS-7の動作するDPS-7シリーズはDPS-7000ハードウェアに発展した。日本電気 (NEC) は[ACOS-4](../Page/ACOS-4.md "wikilink")のCPUをこのシリーズに供給したことがある。

1980年代後半、ハネウェルは主にハードウェア面で開発の遅れが目立っていたコンピュータ部門をNECおよびBullと共同出資する合弁会社という形で手放した。 開発の遅れを挽回しメインフレーム市場での競争力を維持するため、NECは[ハイエンド](https://ja.wikipedia.org/wiki/ハイエンド "wikilink") ([ACOS-6](../Page/ACOS-6.md "wikilink")) のメインフレームACOS1000とACOS2000の[OEM](../Page/OEM.md "wikilink")供給を行う。 （ACOS1000シリーズはDPS90、ACOS2000シリーズはDPS9000として全世界で販売されNECの生産台数を大きく伸ばすことになる） この過程では特許技術の回避やGCOS8の拡張機能への対応など、単純なOEM供給ではないハードウェア、ソフトウェア両面での作業が必要となった。 最終的にこの合弁会社はBullが取得している。

[1990年代](../Page/1990年代.md "wikilink")終盤から[2000年代](../Page/2000年代.md "wikilink")にかけて、Bullはハードウェアベースを1つに統一しようと、[インテル](https://ja.wikipedia.org/wiki/インテル "wikilink")のチップを使ったシステムに集中するようになった。[Itanium 2ベースで](https://ja.wikipedia.org/wiki/Itanium_2 "wikilink")、[Microsoft Windowsと](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")[Linux](../Page/Linux.md "wikilink")が動作する。ただし、[エミュレータ](../Page/エミュレータ.md "wikilink")でGCOS-7とGCOS-8がこのプラットフォーム上で動作するようにした。Bullは現在もGCOS-7とGCOS-8をサポートするための開発費用を出費し続けており、いくつかの国に顧客がいる。

## こぼれ話

[ベル研究所](../Page/ベル研究所.md "wikilink")では、初期のUNIXシステムでGCOSマシンをプリンタスプーラとして接続していた。このため "/etc/passwd" にGCOSと接続するためのID情報を書いておくフィールド "GCOSフィールド"が作られた。このフィールドは今日でも "pw_gecos" として残っており、現在では人間が読んで理解できるユーザー単位の情報（フルネームとか所属など）を書くのに使われている。

## 関連項目

  - [Multics](https://ja.wikipedia.org/wiki/Multics "wikilink")
  - [GE-600シリーズ](../Page/GE-600シリーズ.md "wikilink")
  - [GE-200シリーズ](https://ja.wikipedia.org/wiki/GE-200シリーズ "wikilink")
  - [ACOS](../Page/Advanced_Comprehensive_Operating_System.md "wikilink")

## 外部リンク

  - [日本のコンピュータ・メーカと7人の小人(1)](http://museum.ipsj.or.jp/guide/pdf/magazine/IPSJ-MGN440812.pdf) 情報処理 2003年8月、[高橋茂](../Page/高橋茂.md "wikilink")

以下、英文

  - [From GECOS to GCOS8](http://febcm.club.fr/english/gecos_to_gcos8_part_1.htm) （GCOSの（[Bull](https://ja.wikipedia.org/wiki/Bull "wikilink")から見た）歴史）
  - [Bull GCOS8 Mainframes](http://www.bull.com/servers/gcos8/)
  - [Bull GCOS8 Documentation](http://support.bull.com/ols/product/system/gcos8/sys/doc/docf/g/67X4A2CD25-SR6.1)（リンク先の "click here" をクリックすると、PDFマニュアルが参照できる）

[Category:メインフレームのオペレーティングシステム](https://ja.wikipedia.org/wiki/Category:メインフレームのオペレーティングシステム "wikilink") [Category:ゼネラル・エレクトリック](https://ja.wikipedia.org/wiki/Category:ゼネラル・エレクトリック "wikilink") [Category:1962年のソフトウェア](https://ja.wikipedia.org/wiki/Category:1962年のソフトウェア "wikilink")
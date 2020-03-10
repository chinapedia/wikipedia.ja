> この記事は[Intel 815](https://ja.wikipedia.org/wiki/Intel_815)から翻訳されています。


**Intel 815** (i815) は、ローエンドからパフォーマンスPC向けとして[2000年](../Page/2000年.md "wikilink")[8月](../Page/8月.md "wikilink")に[インテル](https://ja.wikipedia.org/wiki/インテル "wikilink")社が発表・発売した[インテル チップセットの製品およびそのファミリ名である](../Page/インテル_チップセット.md "wikilink")。

## 概要

Intel 815はインテル社として初めてPC133 [SDRAM](https://ja.wikipedia.org/wiki/SDRAM "wikilink")をサポートするチップセットとして発表された。

当時のインテルはPC100 SDRAMの次世代PC用メモリとして[Intel 820をもって](../Page/Intel_820.md "wikilink")[RDRAM](../Page/RDRAM.md "wikilink")の普及を推進していたが、その活動は実質的に頓挫した状態にあり、市場では安価かつ最新鋭の133MHz [FSBにマッチングするPC](https://ja.wikipedia.org/wiki/フロントサイドバス "wikilink")133 SDRAMを推進する[VIA Technologiesが躍進しつつあった](../Page/VIA_Technologies.md "wikilink")。

このためインテルは一時的にIntel 820によるRDRAM普及計画を停止し、市場の声に応えるべくローエンド向けチップセットとして成功していた[Intel 810をベースとしてパフォーマンスPC向けに開発されたのがIntel](../Page/Intel_810.md "wikilink") 815である。

開発経緯により、Intel 815は同じくパフォーマンスPC向けとして開発されたIntel 820より、ローエンド向けであるIntel 810との共通点が多く、Intel 815とIntel 810をまとめて**Intel 81x系**という呼び方もされた。

チップセットの構成はベースとなったIntel 810同様にハブ・アーキテクチャ (Hub Architecture) による2チップ構成を採り、ノースブリッジに相当する**GMCH (Graphics Memory Controller Hub)** としてIntel 82815を、サウスブリッジに相当する**[ICH (I/O Controller Hub)](https://ja.wikipedia.org/wiki/I/O_コントローラー・ハブ "wikilink")** にはICHとICH2の2種類が準備され、ICH2を採用した上位モデルは**Intel 815E**と命名された。これらは帯域幅266MB/sの**ハブ・リンク (Hub Link)** で接続されている。また、管理機能としてIntel 820で採用された**アラート オン LAN**を引き続き採用しているものの、[プロセッサ シリアル ナンバーの](https://ja.wikipedia.org/wiki/プロセッサ_シリアル_ナンバー "wikilink")[プライバシー](../Page/プライバシー.md "wikilink")問題により**ランダム・ナンバ・ジェネレータ**は省略されている。

特徴としては**PC133 SDRAMと[AGP2.0準拠の外部AGPスロットをサポート](../Page/Accelerated_Graphics_Port.md "wikilink")**したことである。これにより、安価なPC133 SDRAMを使用してハイパフォーマンスPCの構築が可能となった。

しかしインテルはIntel 815をあくまでIntel 810とIntel 820の中間の製品であると位置づけていた。このため、**[SMP](https://ja.wikipedia.org/wiki/マルチCPU "wikilink")**の非サポートやメモリ容量が最大でも512MBと前世代の[Intel 440BXと比較しても半分しか搭載できないなど](../Page/Intel_440BX.md "wikilink")、従来のパフォーマンスPC向けチップセットと比較すると貧弱な点が弱点として指摘されていた。例外的に、2000年10月にEpoxが、DualCPUに対応したマザーボードを結果的に発売することがなかったものの、参考展示\[[http://pc.watch.impress.co.jp/docs/article/20001019/wpe10.htm\]しており、2001年に815E/PEでデュアルCPUに対応した製品\[https://news.mynavi.jp/articles/2001/08/17/21/bench/index.html\]がAcorpから、発表されている。ただし、これらはIntel非公式の実装であり、2013年現在での最新チップセットドライバでは無効になるようになっている](http://pc.watch.impress.co.jp/docs/article/20001019/wpe10.htm%5Dしており、2001年に815E/PEでデュアルCPUに対応した製品%5Bhttps://news.mynavi.jp/articles/2001/08/17/21/bench/index.html%5DがAcorpから、発表されている。ただし、これらはIntel非公式の実装であり、2013年現在での最新チップセットドライバでは無効になるようになっている)。

それにも関わらずIntel 815自体は広く普及したため、市場のニーズに合わせ[グラフィック機能を削減した](../Page/オンボードグラフィック.md "wikilink")**Intel 815P**、外部AGPを削減した**Intel 815G**、モバイル向けに低消費電力化と[SpeedStep](https://ja.wikipedia.org/wiki/SpeedStep "wikilink")への対応を行った**Intel 815EM**などのバリエーションモデルも開発され市場に投入された。

Intel 815シリーズは[CPU](../Page/CPU.md "wikilink")インターフェースにAGTL+を採用していた**Coppermine**コアの[Pentium IIIおよび](../Page/Pentium_III.md "wikilink")[Celeron](https://ja.wikipedia.org/wiki/Celeron "wikilink")との組合わせが想定されていたが、後に登場した**Tualatin**コアでは互換性の無いAGTLに変更されたため、Intel 815シリーズもステッピング変更によりAGTLへの対応が行われている。AGTLに対応したモデルは**B0ステッピング**と呼称され、一部では**Intel 815E-B**のような表記もされた。

### Intel 810との相違点

Intel 815の発表後、一部では「Intel 810＋外部AGP＝Intel 815である」という言い方がされる場合もあった。しかし実際にはIntel 815ファミリの中でもIntel 815Gでは外部AGPをサポートしておらず、正確な理解とは言えない。これはIntel 815の発表当初はIntel 815Gは存在しなかったことに加え、チップセットを強く意識する[自作PC](https://ja.wikipedia.org/wiki/自作PC "wikilink")市場においては外部AGPが重視されIntel 815Gがほぼ普及しなかったため、「Intel 815ファミリ＝外部AGP付き」という誤った固定認識がされたことによる。

Intel 815とIntel 810の明確な相違点はむしろPC133 SDRAMサポートの有無であり、この一点以外は非常に似た製品となっている。

## GMCH

[thumb](https://ja.wikipedia.org/wiki/ファイル:Intel_82815_GMCH.jpg "wikilink") GMCHであるIntel 82815はAGP2.0準拠のAGP 4xスロットをサポートする他、[IGTコアを統合し](../Page/Intel_740.md "wikilink")[2D/3Dグラフィックス機能を搭載している](../Page/オンボードグラフィック.md "wikilink")。これらは同時使用は出来ない仕様であり、外部AGP使用時には統合グラフィックス機能が自動的に無効になる。

当初発表されたi815は外部AGPと統合グラフィックスの両方をサポートしていたが、市場のニーズにこたえる形で統合グラフィックスを省略し外部AGP使用に特化したIntel 815P、逆に外部AGPを省略し統合グラフィックスでの使用に特化したIntel 815Gがそれぞれ廉価版として登場している。

メインメモリとして512MBまでのPC100または133の[SDRAM](https://ja.wikipedia.org/wiki/SDRAM "wikilink")をサポートする。ただしPC100使用時には6バンクまで使用可能であるが、PC133使用時には4バンクまでに制限される。

### 統合グラフィック機能

Intel 815/815Gに統合されるグラフィックス機能は内部的にAGP2x相当で接続された[Intel 752をベースとした](https://ja.wikipedia.org/wiki/Intel_740#Intel_752 "wikilink")**Intel Graphics Technology**(IGT)コアであり、Intel 810で採用されているものと同等であるが、GPUコアクロックが引き上げられ133MHzとなっている。32bitレンダリングをサポートせず、2D/3D共に当時のビデオカードと比較して貧弱な性能ではあったが、[DirectX](https://ja.wikipedia.org/wiki/DirectX "wikilink") 6世代の[Direct3D](https://ja.wikipedia.org/wiki/Direct3D "wikilink")に対応し、[MCによる動画再生支援にも対応するなど](https://ja.wikipedia.org/wiki/動き補償#フレーム間予測 "wikilink")、当時のビジネス・ホームユーザーには十分な機能を有しており、メーカー製PCを中心に広く採用された。

#### AIMM

[thumb](https://ja.wikipedia.org/wiki/ファイル:AIMM_for_Intel815_\(GPA_4MB\).jpg "wikilink") Intel 815でのIGTコアはIntel 810と同様にフレームバッファとして専用の[ビデオメモリ](https://ja.wikipedia.org/wiki/ビデオメモリ "wikilink")をサポートせず、メインメモリと共有するUMA (Unified Memory Architecture) を採用している。これは低価格化・省スペース化には有利であるが、性能的には不利であった。

この問題の解決策としてIntel 815はオプションとして**AGP In-Line Memory Module (AIMM)** と呼称される**Graphics Performance Accelerator (GPA)** カードをサポートしている。これは[Zバッファ](https://ja.wikipedia.org/wiki/Zバッファ "wikilink")専用の4MB SDRAMを搭載しAGPスロットに接続する拡張カードであり、メモリ負荷の高いZバッファを専用メモリに展開することでメインメモリの負荷軽減と3Dパフォーマンスの向上を図っている。先行するIntel 810ではオンボード接続でサポートされていたDisplay Cacheの外部AGP接続版に相当する。

ただしDisplayCache同様にあくまでZバッファ専用であるため、2D性能の向上には全く寄与しない。

### 省電力機能

モバイル版のIntel 815EMでは**Intel Speed Step Technology**をサポートしている。

これはシステムがACアダプタ駆動かバッテリー駆動かを判断し、バッテリー駆動時にはプロセッサの動作周波数を下げることで、バッテリー駆動時間の延長を図る機能である。

## ICH

Intel 815に接続されるICHとしては、ICH2 (Intel 82801AB) またはICH (Intel 82801AA) が準備された。このうち、ICH2を採用したモデルが上位であり、ICH2を採用したモデルには型番に**E**が付与されている (Intel 815E, Intel 815EP, Intel 815EG)。いずれも従来のサウスブリッジ同様に[ATA](../Page/Advanced_Technology_Attachment.md "wikilink")・[USBや各種レガシコントローラを搭載する他](../Page/ユニバーサル・シリアル・バス.md "wikilink")、[AC'97対応のサウンドコントローラや](../Page/Audio_Codec_97.md "wikilink")[ネットワークの](https://ja.wikipedia.org/wiki/Ethernet "wikilink")[論理層も統合している](../Page/OSI参照モデル.md "wikilink")。この為、コーデックチップ又は物理層チップを追加するだけで、安価にサウンド/ソフトウェア[モデム](https://ja.wikipedia.org/wiki/モデム "wikilink")機能・[ネットワーク機能を](../Page/Local_Area_Network.md "wikilink")[オンボード](../Page/オンボード.md "wikilink")で実現できるようになった。これに伴いセットメーカーがオプションのバリエーションを採用しやすくするため、ICH2では[CNRスロットがサポートされている](https://ja.wikipedia.org/wiki/Communication_and_Networking_Riser "wikilink")（ICHでは[AMRスロットがサポートされている](https://ja.wikipedia.org/wiki/Audio_and_Modem_Riser "wikilink")）。

## 評価と影響

Intel 815は開発発表当時からすでに目新しい技術は何一つ無い製品だったが、ローエンドからパフォーマンスデスクトップまでを幅広くカバーする製品となり大きな成功を収めた。

これはIntel 815の搭載していた機能が当時のユーザーのニーズに合致しており、かつIntel 815発表前のインテルにはそれを満たす製品が無かったからである。 不足な点も指摘されていたもののIntel 815は概ねIntel 440BXの後継製品として市場に認められた。本来パフォーマンスPC向けとして期待されていたIntel 820はIntel 815の登場で過去の存在となり、ローエンド向けとして成功を収めていたIntel 810さえも後にはIntel 815Gにその立場を譲った。

インテルは当初、Intel 815の後継としてTualatinコアに対応した[Intel 830チップセットの投入を予定していたが](https://ja.wikipedia.org/wiki/Intel_830 "wikilink")、[NetBurst](https://ja.wikipedia.org/wiki/NetBurst "wikilink")[マイクロアーキテクチャ](../Page/マイクロアーキテクチャ.md "wikilink")を採用した[Pentium 4シリーズの普及を前倒しする狙いからデスクトップ向けのIntel](../Page/Pentium_4.md "wikilink") 830はキャンセルされた。しかし初期のNetBurstマイクロアーキテクチャ対応チップセットではエントリーPC向けの需要を満たすことが出来ず、旧式ながら使い勝手の良いIntel 815は2002年の[Intel 845Gの登場に至るまでインテル主力チップセットの座に留まることになる](https://ja.wikipedia.org/wiki/Intel_845 "wikilink")。

反面、SMPの非サポートや最大メモリ容量の乏しさといった弱点によりあくまでデスクトップPC向けに留まり、Intel 440BXやIntel 820のような[エントリーサーバや](../Page/サーバ.md "wikilink")[ワークステーション](../Page/ワークステーション.md "wikilink")向けとしては普及しなかった。このため、これら市場ではVIA technologiesのAppolo Pro 266などの製品が普及していくことになった。

Intel 810発表前のグラフィックス統合チップセットは完全にローエンド向けの位置付けであったが、Intel 810およびIntel 815でパフォーマンスデスクトップ向けとしての需要も見出されたことで、以後のチップセットではパフォーマンスPC向けチップセットでも統合グラフィック機能＋ディスクリート[ビデオカード](../Page/ビデオカード.md "wikilink")に対応した製品が一般化していくことになった。

SMP非対応など従来のパフォーマンスPC向けチップセットより1ランク下の機能でありながら、統合グラフィックス機能と外部AGPの柔軟な構成が可能なIntel 815の成功は、以後のチップセットの基本モデルとなったと言える。

## ラインナップ

| 製品名   | 対応FSB         | 対応メモリ     | メモリ容量 | 外部AGP | 内部グラフィック | ICH    | ATA    | USB  | PCI | SMP |
| ----- | ------------- | --------- | ----- | ----- | -------- | ------ | ------ | ---- | --- | --- |
| 815   | 66/100/133MHz | PC100/133 | 512MB | 有     | 有        | ICH    | ATA66  | 2ポート | 6   | 非対応 |
| 815E  | 66/100/133MHz | PC100/133 | 512MB | 有     | 有        | ICH2   | ATA100 | 4ポート | 6   | 非対応 |
| 815P  | 66/100/133MHz | PC100/133 | 512MB | 有     | 無        | ICH    | ATA66  | 2ポート | 6   | 非対応 |
| 815EP | 66/100/133MHz | PC100/133 | 512MB | 有     | 無        | ICH2   | ATA100 | 4ポート | 6   | 非対応 |
| 815G  | 66/100/133MHz | PC100/133 | 512MB | 無     | 有        | ICH    | ATA66  | 2ポート | 6   | 非対応 |
| 815EG | 66/100/133MHz | PC100/133 | 512MB | 無     | 有        | ICH2   | ATA100 | 4ポート | 6   | 非対応 |
| 815EM | 66/100MHz     | PC100/133 | 512MB | 有     | 有        | ICH2-M | ATA100 | 4ポート | \-  | 非対応 |

  - 加えて、これらモデル全てにAGTLに対応したB0ステッピングが存在する。

## 関連項目

  - [Intel 740](../Page/Intel_740.md "wikilink")
  - [インテル チップセット](../Page/インテル_チップセット.md "wikilink")
      - [Intel 810](../Page/Intel_810.md "wikilink")
      - [Intel 820](../Page/Intel_820.md "wikilink")
  - [Integrated Graphics Processor](../Page/Integrated_Graphics_Processor.md "wikilink")
      - [AMD 690 チップセットシリーズ](../Page/AMD_690_チップセットシリーズ.md "wikilink")

[Category:インテルのチップセット](https://ja.wikipedia.org/wiki/Category:インテルのチップセット "wikilink") [Category:オンボードグラフィック](https://ja.wikipedia.org/wiki/Category:オンボードグラフィック "wikilink")
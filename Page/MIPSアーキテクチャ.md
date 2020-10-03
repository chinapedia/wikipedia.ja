> この記事は[MIPSアーキテクチャ](https://ja.wikipedia.org/wiki/MIPSアーキテクチャ)から翻訳されています。


**MIPSアーキテクチャ**は、ミップス・コンピュータシステムズ（現[ミップス・テクノロジーズ](../Page/ミップス・テクノロジーズ.md "wikilink")）が開発した[RISC](../Page/RISC.md "wikilink")マイクロプロセッサの[命令セット](../Page/命令セット.md "wikilink")・アーキテクチャ (ISA) である。

## 概要

**MIPS**は "Microprocessor without Interlocked Pipeline Stages"（[(命令)パイプラインのステージに](https://ja.wikipedia.org/wiki/命令パイプライン "wikilink")「インターロックされたステージ」がない[マイクロプロセッサ](../Page/マイクロプロセッサ.md "wikilink")）に由来しており、R2000の頃の[マイクロアーキテクチャ](../Page/マイクロアーキテクチャ.md "wikilink")の特徴からの命名である（が、その後そのような特徴が薄れていったのも、他のRISCと同様である）。[MIPS](https://ja.wikipedia.org/wiki/MIPS "wikilink")値にも掛けている。

当初は[32ビット](../Page/32ビット.md "wikilink")幅の[レジスタとデータバスを持つ](../Page/レジスタ_\(コンピュータ\).md "wikilink")[32ビット](../Page/32ビット.md "wikilink")の構成だったが、後に[64ビット](../Page/64ビット.md "wikilink")に拡張された。MIPSアーキテクチャには[下位互換](https://ja.wikipedia.org/wiki/下位互換 "wikilink")のある複数の[命令セット](../Page/命令セット.md "wikilink")が存在する。それぞれ、MIPS I、MIPS II、MIPS III、MIPS IV、MIPS 32、MIPS 64 と称する。現行版は MIPS 32（32ビット実装）と MIPS 64（64ビット実装）である\[1\]\[2\]。MIPS 32 と MIPS 64では命令セットだけでなく制御レジスタについても定義している。

いくつかのアドオン拡張も用意されている。例えば、MIPS-3D は、3Dタスクで一般的な処理を行うための浮動小数点[SIMD](../Page/SIMD.md "wikilink")命令のシンプルなセットである\[3\]。また、MDMX (MaDMaX) は、より広範な整数[SIMD](../Page/SIMD.md "wikilink")命令セットで、64ビット浮動小数点レジスタを流用する。その他、MIPS16e は命令列を圧縮してプログラム格納域を小さくするための拡張である ([ARMアーキテクチャ](../Page/ARMアーキテクチャ.md "wikilink")のThumbエンコーディングに対抗したもの) \[4\]。また、MIPS MT は、米[インテル](https://ja.wikipedia.org/wiki/インテル "wikilink")社が[ハイパースレッディング・テクノロジー](../Page/ハイパースレッディング・テクノロジー.md "wikilink")として普及させた技術と同等の、[マルチスレッディングに適した拡張である](../Page/スレッド_\(コンピュータ\).md "wikilink")\[5\]。

命令セットが非常にきれいなので、[アメリカ合衆国](https://ja.wikipedia.org/wiki/アメリカ合衆国 "wikilink")では[コンピュータ・アーキテクチャ](../Page/コンピュータ・アーキテクチャ.md "wikilink")を学校で教えるときに教材としてMIPSアーキテクチャを使うことが多い\[6\]。MIPSのデザインは、もうひとつの初期のRISCであるバークレーRISC（[:en:Berkeley RISC](https://ja.wikipedia.org/wiki/:en:Berkeley_RISC "wikilink")）と共に、後発のRISCに影響を及ぼした。

MIPSプロセッサは、[SGIのコンピュータ製品群に使われていた](../Page/シリコングラフィックス.md "wikilink")。日本では、[ソニー](../Page/ソニー.md "wikilink")の[NEWSや](https://ja.wikipedia.org/wiki/NEWS_\(ソニー\) "wikilink")[日本電気](../Page/日本電気.md "wikilink") (NEC) の[EWS4800](../Page/EWS4800.md "wikilink")で使われた。また、米[DEC社は](../Page/ディジタル・イクイップメント・コーポレーション.md "wikilink")、ごく短期間だけMIPSを使った[ワークステーションを製品化していた](../Page/DECstation.md "wikilink")\[7\]。また、機器組み込み分野で成功し、[Windows CE製品](https://ja.wikipedia.org/wiki/Microsoft_Windows_CE "wikilink")、[シスコシステムズ](../Page/シスコシステムズ.md "wikilink")の[ルーター](../Page/ルーター.md "wikilink")、[プリンタのエンジンなどに使われた](https://ja.wikipedia.org/wiki/プリンター "wikilink")。[ゲーム機](../Page/ゲーム機.md "wikilink")分野でも成功を収め、[NINTENDO64](../Page/NINTENDO64.md "wikilink")、[ソニー・コンピュータエンタテインメント](https://ja.wikipedia.org/wiki/ソニー・コンピュータエンタテインメント "wikilink")の[PlayStation](../Page/PlayStation_\(ゲーム機\).md "wikilink")、[PlayStation 2](../Page/PlayStation_2.md "wikilink")、[PlayStation PortableでもMIPSアーキテクチャのプロセッサが使われた](../Page/PlayStation_Portable.md "wikilink")。[1990年代](../Page/1990年代.md "wikilink")後半、RISCマイクロプロセッサの出荷個数ベースで3分の1がMIPSアーキテクチャの製品だったと見積もられている\[8\]。

## 歴史

### RISCの先駆者

1981年、[スタンフォード大学](../Page/スタンフォード大学.md "wikilink")の[ジョン・L・ヘネシー](https://ja.wikipedia.org/wiki/ジョン・L・ヘネシー "wikilink")率いるチームは、後に最初のMIPSプロセッサを生むプロジェクトを開始した。基本コンセプトは、[命令パイプライン](https://ja.wikipedia.org/wiki/命令パイプライン "wikilink")を深くすることで劇的に性能を向上させることである。[IBM 801](../Page/IBM_801.md "wikilink") などの研究や先例でこの手法はよく知られていたが、その可能性が完全に解明されていなかった。一般に[プロセッサ](../Page/プロセッサ.md "wikilink")は、命令デコーダ、[演算論理装置](https://ja.wikipedia.org/wiki/演算論理装置 "wikilink") (ALU)、メモリとやりとりするロード/ストア・ユニットといった部分で構成されている。パイプライン化されていない従来の「[マイクロプロセッサ](../Page/マイクロプロセッサ.md "wikilink")の」設計では、1つの命令の処理を（ほぼ）完了させないと次の命令の処理を開始できず、内部ではほとんどの時間を処理に関与せずに待機するだけの回路が多くなる。これに対して「従来のマイクロプロセッサ」ではない、例えば1960年代の[IBM 7030の頃には実現されていた命令パイプライン方式では](../Page/IBM_7030.md "wikilink")、1つの命令の処理過程を複数のステージ（段階）に分割し、各ステージを順次、次のサブユニットに送って、複数のサブユニットがオーバラップして動作できるようにする。1つ目の命令の最初のステージの処理が終わると、次のステージの処理へ引き継がれると同時に、2つ目の命令の最初のステージの処理が平行して実行される。3つ目の命令が入ると1つ目の命令は3ステージ先、2つ目の命令は2ステージ先、3つ目の命令は最初のステージで、3つの処理が同時に行われる。すべてが最も効率的に動けば、複数に分割した処理過程の内容に関わらず、1ステージの処理ごとに1つの命令が完了できることになる。

命令パイプラインでは、乗算・除算命令のように命令の実行に長い時間がかかる場合、パイプラインに次の命令を取り込むのを待つ必要がある。この問題の解決策として、パイプラインの各ステージが処理中であることを示せるようにして、パイプラインをインターロックして、次の命令のステージが進行しないように止めなければならない。これがストールである。分岐命令を実行すると、後続の命令が途中のステージまで進行していたものを取り消さなければならず、ストールに加えて無駄となった処理時間分も加わる。これらがインターロックのロスとなる\[9\]。ストールが発生しインターロックがかかると命令パイプラインは足踏みするため、性能向上は望めないと考えられていた。MIPSの設計上では、すべての命令を単純化して実行処理が1クロックサイクル内で完了するよう計画された。そうできればインターロックをなくすことができる。

このような設計にすることで掛け算や割り算などの複雑な命令が1つの命令では実行できなくなるが、単純な命令だけであれば、プロセッサに与えるクロックを高速にでき早く動作させて、性能が向上すると予想された。また、インターロック回路を加えると半導体チップの面積（ダイサイズ）が増えて、クロックを上げることが困難になるため、クロックの高速化のためにはインターロックを排除することも必要だった。

複雑だが有用だった命令を排除することは議論の中心になった。多くの人が「複雑な掛け算を単純な多くの足し算にして、どうして速度が向上するのか」と、この設計手法、そしてRISC一般の謳い文句に懐疑的で誇大広告だと言った。しかし、これらの意見は、この設計における速度向上のポイントが命令の機能にあるのではなく、パイプラインにあるということを無視したものだった。時間のかかる処理にまつわる問題は、[ディレイスロット](https://ja.wikipedia.org/wiki/ディレイスロット "wikilink")で一応解決された。例えば、2クロックサイクルかかる命令があった場合、次の命令をディレイスロットとし、そこに、前の命令と依存関係の無い、つまり前の命令の結果を必要とせず、かつ前の命令に関わっているレジスタを使用しない命令を配置することで、パイプラインを止めないようにした。これを実現するためには、プロセッサに与える命令列を生成する[コンパイラ](../Page/コンパイラ.md "wikilink")が、あらかじめ各命令ごとのクロックサイクル数を把握して、可能な限りディレイスロットを有効な命令で埋めるようにする必要があった。それでも大部分の命令は1クロックサイクルで実行できた。また、コンパイラ技術の進展はディレイスロットの活用頻度を向上させた。

初期のMIPSと並び、RISCの典型であり代表とされるバークレーRISC（[:en:Berkeley RISC](https://ja.wikipedia.org/wiki/:en:Berkeley_RISC "wikilink")、[SPARC](../Page/SPARC.md "wikilink")への影響が大きい）と比べると、[サブルーチン](../Page/サブルーチン.md "wikilink")コールの扱い方が大きく異なる。バークレーRISCは頻繁に実行され性能への影響が大きいサブルーチンコールの性能向上を図るために、大きなレジスタファイルを持つと同時に[レジスタ・ウィンドウ](../Page/レジスタ・ウィンドウ.md "wikilink")というメカニズムを導入したが、それによってサブルーチンコールの入れ子段数が制限されている。サブルーチンコールは、それぞれのルーチンで専用に用いるローカルのレジスタ群を必要とし、その割り当てをハードウェアでサポートするということはチップにさらなるリソースを必要とし、設計も複雑化することを意味する。ヘネシーは、賢いコンパイラであればハードウェアでの実装に頼らずに使っていないレジスタを見つけ出すことができ、単にレジスタを有効利用できるだけでなく、あらゆるタスクの性能向上にも寄与すると考えた。

MIPSは最も典型的なRISCのひとつだとされる、というよりも、RISCの提唱者であるヘネシーとパターソンのそれぞれが設計した命令セット（命令セットアーキテクチャ）であるということを理由に、MIPSとバークレーRISCの設計が「典型的なRISC」だとされ、それらの特徴を以て「RISCの定義」だとされているためであり、「MIPSは最も典型的なRISC」だという言明はその逆になっている。

命令語のビット数を節約するために、命令数を抑えることで、命令フォーマット中の[オペコード](../Page/オペコード.md "wikilink")部として必要となるビット数を抑えている。基本オペコードは、命令語32ビットの中の6ビットを使用し\[10\]、残りの部分の構成の違いにより数種類の分類がある。命令語の残りの26ビットの部分について、26ビットの分岐先アドレスとする命令フォーマット、5ビットのフィールド4個で3つのレジスタとシフト値を指定し、残り6ビットを追加のオペコードとする命令フォーマット、2つのレジスタと16ビットの即値を指定する命令フォーマットがある。このような設計で、実行すべき命令と必要なデータ（[オペランド](https://ja.wikipedia.org/wiki/被演算子 "wikilink")）を1サイクルでロードできるようになった（正確には、必要なデータはレジスタの中にあるのであり、もし1サイクルで全てを揃えたいのなら特殊な技法が必要になる。細かく言うと、「オペコードとオペランド指定子」を（1サイクルで32ビットをメモリからロードできるように他の部分が設計されていば）1サイクルでロードできる）。

### 最初のハードウェア

[1984年](../Page/1984年.md "wikilink")、ヘネシーは、将来商業レベルとなる可能性のあるデザインを確立し、教え子、友人らとミップス・コンピュータシステムズを設立する。[1985年](https://ja.wikipedia.org/wiki/1985年 "wikilink")、彼らは、最初のデザインである[R2000](../Page/R2000.md "wikilink")を完成させた。また、[1988年](../Page/1988年.md "wikilink")には、それを進化させた[R3000](../Page/R3000.md "wikilink")を完成させた。これらの32ビットCPUによって、ミップス・コンピュータシステムズは、[1980年代](../Page/1980年代.md "wikilink")に基盤を築くことができた。なお、これらの商用デザインにおいては、スタンフォード大学での学術研究的な設計方針とは異なり、ハードウェアにインターロック機構を装備し、掛け算も割り算もサポートしていた。なぜなら、単にひとつのプログラムを実行するだけなら、上述のディレイスロットの考え方で何とかなるが、商用としてはマルチタスクや割り込みへの対応は必須であり、インターロック機構の付加は必然だったからである。また、半導体プロセス技術の急速な進歩がそれを可能にしていった。インターロック機構を備えたとしても、インターロックをなるべく発生させないコンパイラ技術は高速化に必須である。これらのプロセッサは、[SGI](../Page/シリコングラフィックス.md "wikilink")、DEC DECstation、ソニー NEWS、NEC EWS4800などに使われた。これらの設計にはソフトウェアアーキテクトのアール・キリアンも参加している。彼は後に MIPS III 64ビット命令セットを設計し、R4000の[マイクロアーキテクチャ](../Page/マイクロアーキテクチャ.md "wikilink")開発にも関わった\[11\]\[12\]。

1991年、ミップス・コンピュータシステムズ社は、最初の64ビットマイクロプロセッサ[R4000](https://ja.wikipedia.org/wiki/R4000 "wikilink")をリリースした\[13\]\[14\]。R4000は仮想アドレスだけでなく仮想空間IDを格納できる進んだ[TLBを採用していた](../Page/トランスレーション・ルックアサイド・バッファ.md "wikilink")。それによって頻繁な[コンテキストスイッチ](../Page/コンテキストスイッチ.md "wikilink")の度にTLBをフラッシュする必要性をなくし、他の競合するアーキテクチャ（Pentium、PowerPC、Alpha）に対して劣っていた[マイクロカーネル](https://ja.wikipedia.org/wiki/マイクロカーネル "wikilink")実装時の大きな性能問題を低減させることができた\[15\]。

しかし、ミップス社は、R4000を市場に提供しようとしたころ、財政危機に陥った。そこで、当時のミップス社の最大の顧客であった米[SGI社は](../Page/シリコングラフィックス.md "wikilink")、[1992年](../Page/1992年.md "wikilink")にミップス社を買い取り、これによりMIPSアーキテクチャの存続が保証された。こうしてミップス・コンピュータシステムズ社はSGIの子会社となり、社名もミップス・テクノロジーズと変更された。

### アーキテクチャのライセンス供与

[1990年](https://ja.wikipedia.org/wiki/1990年 "wikilink")初頭、ミップス・テクノロジーズ社は、プロセッサの設計を[サードパーティー](../Page/サードパーティー.md "wikilink")にライセンス供与しはじめた。プロセッサ・コア、つまり主要な演算部分の単純さによって、これは「MIPSコア」として成功を収め、従来は同等のゲート数と価格の[CISC](../Page/CISC.md "wikilink")プロセッサが占めていた様々な分野でMIPSコアが使われるようになった。ゲート数と価格は密接な関係があり、CPUの価格はキャッシュメモリ領域を除けば、ゲート数とピン数でほぼ決まっていた。[サン・マイクロシステムズ](../Page/サン・マイクロシステムズ.md "wikilink")も追随して[SPARC](../Page/SPARC.md "wikilink")コアのライセンス供与を開始したが、成功したとは言い難い。[1990年代](../Page/1990年代.md "wikilink")後半にはMIPSは機器[組み込み用プロセッサ分野の勝者となっていた](../Page/組み込みシステム.md "wikilink")。1997年、4800万個目のMIPSベースのチップが出荷され、MIPS CPUファミリは[モトローラ](../Page/モトローラ.md "wikilink")の[MC68000](../Page/MC68000.md "wikilink")ファミリを出荷個数で抜いた。この成功により、SGI社はミップス・テクノロジーズを[1998年](https://ja.wikipedia.org/wiki/1998年 "wikilink")に[スピンオフ](../Page/スピンオフ.md "wikilink")させた。ミップス・テクノロジーズの収入の半分はライセンス料であり、残りはサードパーティーが生産するコアの設計から来ている。

[1999年](../Page/1999年.md "wikilink")、ミップス・テクノロジーズ社はライセンス体系を整理し、32ビットの**MIPS32**（MIPS II にそれ以降の新規機能を追加したもの）と64ビットの**MIPS64**（MIPS V ベース）に分けた。このアナウンスと同時に、NEC、[東芝](../Page/東芝.md "wikilink")、SiByte（後に[ブロードコム](../Page/ブロードコム.md "wikilink")が買収）がMIPS64のライセンス供与を受けた。[フィリップス](../Page/フィリップス.md "wikilink")、[LSIロジック](https://ja.wikipedia.org/wiki/LSIロジック "wikilink")、[IDT](../Page/IDT.md "wikilink")もすでに参加している。成功に成功が続き、MIPSはコンピュータに近い機器（[ハンドヘルドコンピュータ](../Page/ハンドヘルドコンピュータ.md "wikilink")や[セットトップボックス](../Page/セットトップボックス.md "wikilink")など）の市場で最も使われているヘビー級CPUコアとなっている。モトローラ社も[セットトップボックス](../Page/セットトップボックス.md "wikilink")に自社の[PowerPC](../Page/PowerPC.md "wikilink")ではなくMIPSコアを採用した。

いくつかの[ベンチャー](../Page/ベンチャー.md "wikilink")企業もミップス・テクノロジーズ社よりアーキテクチャ・ライセンスの供与を受けて参入してきた。最初にMIPSプロセッサを設計したベンチャー企業は[Quantum Effect Devicesだった](../Page/Quantum_Effect_Devices.md "wikilink")。MIPS社で**[R4300i](https://ja.wikipedia.org/wiki/R4200 "wikilink")**を設計したチームはSandCraft社を設立し、NEC向けに**R5432**を設計し、後に**SR7100**を作った。これは、組み込み分野向けの最初の[アウト・オブ・オーダー実行](../Page/アウト・オブ・オーダー実行.md "wikilink")プロセッサである。DECで最初に[StrongARM](../Page/StrongARM.md "wikilink")を設計したチームはふたつのMIPS関連ベンチャーを設立した。ひとつはSiByteで**SB-1250**というMIPSベースで最初のSystem-on-a-chip (SOC) を実現した製品を作った。もうひとつのAlchemy Semiconductorは**Au-1000**という低電力のSOCを作った。SiByteはブロードコムに買収された。Alchemyは[AMDに買収されたが](https://ja.wikipedia.org/wiki/アドバンスト・マイクロ・デバイセズ "wikilink")、後にAMDはAlchemyをRaza Microelectronics (RMI) に売却した。LexraはMIPSに似たアーキテクチャをベースにDSP機能を付加したチップをオーディオ機器市場向けに、マルチスレッド機能を付加したチップをネットワーク機器市場向けに出している。LexraはMIPSからライセンス供与を受けていなかったため、MIPSとの間で2件の訴訟となった。1件はLexraがMIPS互換であることを宣伝しないという条件ですぐさま解決した。2件目は長引き、両社を疲弊させた。結局、ミップス・テクノロジーズがLexraに対してフリーライセンスと賠償金を払うことで決着した。

MIPSアーキテクチャを使った[マルチコア](../Page/マルチコア.md "wikilink")デバイスを構築することに特化した企業も2社登場している。[Raza Microelectronics, Inc.](https://ja.wikipedia.org/wiki/:en:RMI_Corporation "wikilink") は低迷していたSandCraftから製品ラインを買い取り、通信およびネットワーク市場向けに8コアの製品を提供した。[Cavium Networks](https://ja.wikipedia.org/wiki/:en:Cavium_Networks "wikilink") は元々はセキュリティ・プロセッサのベンダーだったが、こちらも同じ市場向けに8CPUコアを集積したデバイスを開発し、後に最大32コア版を開発している。両社ともに社内でコアを設計しており、MIPSからコア設計を買うのではなくアーキテクチャのライセンス供与だけを受けている。

### デスクトップ市場を失う

MIPSプロセッサを使った[ワークステーション](../Page/ワークステーション.md "wikilink")システムを製造していた企業として、[SGI](../Page/シリコングラフィックス.md "wikilink")、[ミップス・コンピュータシステムズ](../Page/ミップス・テクノロジーズ.md "wikilink")、[Whitechapel Workstations](https://ja.wikipedia.org/wiki/:en:Whitechapel_Computer_Works "wikilink")、[オリベッティ](../Page/オリベッティ.md "wikilink")、[Siemens-Nixdorf](https://ja.wikipedia.org/wiki/:en:Siemens_Nixdorf_Informationssysteme "wikilink")、[エイサー](../Page/エイサー_\(企業\).md "wikilink")、[DEC](../Page/ディジタル・イクイップメント・コーポレーション.md "wikilink")、[NEC](../Page/日本電気.md "wikilink")、[ソニー](../Page/ソニー.md "wikilink")、[DeskStation](https://ja.wikipedia.org/wiki/:en:DeskStation_Technology "wikilink") があった。またMIPSアーキテクチャ上に移植された[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink")として、SGIの[IRIX](../Page/IRIX.md "wikilink")、[マイクロソフト](../Page/マイクロソフト.md "wikilink")の[Windows NT](../Page/Microsoft_Windows_NT.md "wikilink")（v4.0まで）、[Windows CE](../Page/Microsoft_Windows_Embedded_CE.md "wikilink")、[Linux](../Page/Linux.md "wikilink")、[BSD](../Page/BSD.md "wikilink")、[UNIX System V](../Page/UNIX_System_V.md "wikilink")、[QNX](../Page/QNX.md "wikilink")、ミップス自身の[RISC/os](https://ja.wikipedia.org/wiki/RISC/os "wikilink")などがある。

1990年代初頭、インテルプロセッサベースのPCに対抗してMIPSプロセッサベースのコンピューティング環境を作るために、[コンパック](../Page/コンパック.md "wikilink")他多数の企業によって [Advanced Computing Environment](https://ja.wikipedia.org/wiki/:en:Advanced_Computing_Environment "wikilink") (ACE) というコンソーシアムが設立された。当時、MIPSなどの強力な[RISC](../Page/RISC.md "wikilink")プロセッサがインテルの[IA-32](../Page/IA-32.md "wikilink")アーキテクチャに取って代わるだろうという予測がなされていた。[マイクロソフト](../Page/マイクロソフト.md "wikilink")の [Windows NT](../Page/Microsoft_Windows_NT.md "wikilink") が当初、[Alpha](https://ja.wikipedia.org/wiki/DEC_Alpha "wikilink")、MIPS、[PowerPC](../Page/PowerPC.md "wikilink")などのRISCアーキテクチャに対応したこともその予測を裏付ける形となった。しかし[インテル](https://ja.wikipedia.org/wiki/インテル "wikilink")が[PentiumクラスのCPUをリリースすると](../Page/Intel_Pentium_\(1993年\).md "wikilink")、マイクロソフトの Windows NT v4.0 では対応するアーキテクチャをIA-32とAlphaのみに絞った。後にSGIが[Itanium](../Page/Itanium.md "wikilink")や[IA-32](../Page/IA-32.md "wikilink")アーキテクチャへの移行を決定すると、デスクトップ市場ではMIPSプロセッサはほぼ完全に姿を消した\[16\]。

### 組み込み市場

[thumbの一例である](https://ja.wikipedia.org/wiki/ファイル:Ingenic_JZ4730.JPG "wikilink")。\]\] 1990年代を通して、MIPSアーキテクチャは[コンピュータネットワーク](../Page/コンピュータネットワーク.md "wikilink")、[電気通信](../Page/電気通信.md "wikilink")、[アーケードゲーム](../Page/アーケードゲーム.md "wikilink")、[ゲーム機](../Page/ゲーム機.md "wikilink")、[プリンター](https://ja.wikipedia.org/wiki/プリンター "wikilink")、デジタル[セットトップボックス](../Page/セットトップボックス.md "wikilink")、[デジタルテレビ](../Page/デジタルテレビ放送.md "wikilink")、[DSLモデムや](../Page/デジタル加入者線.md "wikilink")[ケーブルモデム](../Page/ケーブルモデム.md "wikilink")、[携帯情報端末](../Page/携帯情報端末.md "wikilink")といった組み込み市場で広く採用された。

MIPSの組み込み向け実装は低消費電力と低発熱を特徴とし、組み込み向けの開発ツールも充実しており、知識の蓄積もあることから、今も組み込み市場で人気を保っている。

### 組み込み市場向けの合成可能なコア

最近ではMIPSアーキテクチャは[IPコア](../Page/IPコア.md "wikilink")として、組み込み用プロセッサの設計に使える形で利用されることが多い。[1999年](../Page/1999年.md "wikilink")の時点で、[32ビット](../Page/32ビット.md "wikilink")と[64ビット](../Page/64ビット.md "wikilink")の基本コアが提供されており、それぞれ **MIPS32 4K** と **MIPS64 5K** と呼ばれている。それらのコアと[FPU](../Page/FPU.md "wikilink")、[SIMD](../Page/SIMD.md "wikilink")システム、各種I/Oデバイスなどを組み合わせてチップを設計できる。

MIPSコアは商業的に成功を収め、様々な機器で利用されている。例えば、[シスコシステムズ](../Page/シスコシステムズ.md "wikilink")や[リンクシス](../Page/リンクシス.md "wikilink")などのルーター、[ケーブルモデム](../Page/ケーブルモデム.md "wikilink")、[ADSL](../Page/ADSL.md "wikilink")モデム、[ICカード](../Page/ICカード.md "wikilink")、[レーザープリンター](../Page/レーザープリンター.md "wikilink")、[セットトップボックス](../Page/セットトップボックス.md "wikilink")、[ロボット](../Page/ロボット.md "wikilink")、[ソニー・コンピュータエンタテインメント](https://ja.wikipedia.org/wiki/ソニー・コンピュータエンタテインメント "wikilink")の[PlayStation 2や](../Page/PlayStation_2.md "wikilink")[PlayStation Portableなどで使われている](../Page/PlayStation_Portable.md "wikilink")。携帯電話やPDAの分野では競合する[ARMアーキテクチャ](../Page/ARMアーキテクチャ.md "wikilink")の座を奪うことはできなかった。

MIPSアーキテクチャの組み込み用プロセッサとして

  - IDT RC32438
  - [ATI](../Page/ATI_Technologies.md "wikilink") Xilleon
  - Alchemy Au1000/1100/1200
  - Broadcom Sentry5
  - RMI XLR7xx
  - Cavium Octeon CN30xx/CN31xx/CN36xx/CN38xx/CN5xxx
  - [インフィニオン・テクノロジーズ](../Page/インフィニオン・テクノロジーズ.md "wikilink") EasyPort/Amazon/Danube/ADM5120/WildPass/INCA-IP/INCA-IP2
  - Microchip Technology PIC32
  - [NEC](https://ja.wikipedia.org/wiki/ルネサス_エレクトロニクス "wikilink") EMMA/EMMA2/VR4181A/VR4121/VR4122/VR4181A/VR5432/VR5500
  - Oak Technologies Generation
  - [PMC-Sierra](https://ja.wikipedia.org/wiki/PMC-Sierra "wikilink") RM11200
  - QuickLogic QuickMIPS ESP
  - [東芝](../Page/東芝.md "wikilink") Donau/TMPR492x/TX4925/TX9956/TX7901

などがある。

### 映像組み込みでの利用

2008年の時点で、MIPSはデジタルテレビで68%、DVDレコーダーで72%、Blu-Rayレコーダーで77%、ケーブルテレビのセットトップボックスで70%、IPテレビのセットトップボックスで77%のシェアがあり、動画のデコーダ・エンコーダを必要とする映像関係で広く使われている\[17\]。

### MIPSベースのスーパーコンピュータ

MIPSアーキテクチャは[超並列型の](../Page/超並列マシン.md "wikilink")[スーパーコンピュータ](../Page/スーパーコンピュータ.md "wikilink")にも採用された。[シリコングラフィックス](../Page/シリコングラフィックス.md "wikilink") (SGI) は1990年代前半からデスクトップ型のグラフィックス・ワークステーションだけでなく[高性能計算](../Page/高性能計算.md "wikilink")市場にも注力するようになった。R4400や[R8000](https://ja.wikipedia.org/wiki/R8000 "wikilink")を使った Challenge シリーズというサーバシステムで成功を収め、後に[R10000](https://ja.wikipedia.org/wiki/R10000 "wikilink")も採用している。その後SGIはさらに強力なシステムの開発に注力するようになる。R10000を採用した Origin 2000 は[NUMA](../Page/NUMA.md "wikilink")型で最大1024個のプロセッサを相互接続するものだった。さらにそこからR14000やR16000を最大1024個構成できる Origin 3000 を開発。しかし、SGIは2005年に[IA-64](../Page/IA-64.md "wikilink")アーキテクチャへの移行を決定し、MIPSベースのスーパーコンピュータの開発をやめた。

高性能計算のベンチャー企業[SiCortex](https://ja.wikipedia.org/wiki/SiCortex "wikilink")は、2007年にMIPSベースの[超並列マシン](../Page/超並列マシン.md "wikilink")を発表した。MIPS64アーキテクチャをベースとし、[カウツグラフ](https://ja.wikipedia.org/wiki/カウツグラフ "wikilink")のトポロジーを使って高性能インターコネクトでノードを相互接続する。消費電力が小さく計算能力が高い。計算ノードはMIPS64コアを8個集積した[マルチコア](../Page/マルチコア.md "wikilink")であり、メモリコントローラ、DMAエンジン、ギガビット・イーサネット、[PCI Express](../Page/PCI_Express.md "wikilink") コントローラなどがシングルチップに集積されていて、消費電力はわずか10ワットでありながら、浮動小数点演算性能はピークで6GFLOPSとされている。最大構成のSC5832はそのようなノードチップ972個で構成されており、MIPS64コアが5832個ある。ピーク性能は8.2テラFLOPSとされている。

### 龍芯

[龍芯](https://ja.wikipedia.org/wiki/龍芯 "wikilink")は[中国科学院](../Page/中国科学院.md "wikilink")が設計したMIPS互換の[マイクロプロセッサ](../Page/マイクロプロセッサ.md "wikilink")であるが、当初はミップス・テクノロジーよりライセンスを受けていなかった。その[マイクロアーキテクチャ](../Page/マイクロアーキテクチャ.md "wikilink")は中国が独自に設計したもので、初期の設計ではMIPSアーキテクチャにある4つの命令が実装されていなかった\[18\]。2009年6月、中国科学院はミップス・テクノロジーズから直接、MIPS32およびMIPS64アーキテクチャのライセンス供与を受けた\[19\]。

2006年から各社が龍芯をベースとしたコンピュータをリリースしており、低消費電力の[ネットブック](https://ja.wikipedia.org/wiki/ネットブック "wikilink")やネットトップもある\[20\]\[21\]。

## MIPS IV

MIPS IV は4番目のアーキテクチャである。MIPS III のスーパーセットであり、それまでの全てのアーキテクチャと互換性がある。MIPS IV は1994年の[R8000](https://ja.wikipedia.org/wiki/R8000 "wikilink")で初めて実装された。MIPS IV で追加された点は次の通りである。

  - 浮動小数点数のロード/ストア命令で「レジスタ + レジスタ」形式（インデックスつき）の[アドレス指定を追加](../Page/アドレッシングモード.md "wikilink")
  - [単精度](https://ja.wikipedia.org/wiki/単精度 "wikilink")および[倍精度](https://ja.wikipedia.org/wiki/倍精度 "wikilink")の[浮動小数点数](../Page/浮動小数点数.md "wikilink")の[積和演算](../Page/積和演算.md "wikilink")命令を追加
  - 条件転送命令（整数レジスタと浮動小数点レジスタ）を追加
  - FPUの制御/ステータスレジスタに新たな条件ビットを追加し、全部で8ビットとした。

## MIPS V

MIPS V は5番目のアーキテクチャで、1996年10月21日の Microprocessor Forum 1996 で発表された\[22\]。主に3次元グラフィックスの性能向上を目的としている。1990年代中ごろ、組み込み用途以外では主にSGIがグラフィックス・ワークステーションにMIPSマイクロプロセッサを使っていたためである。MIPS V と同時にそれを補完する MIPS Digital Media Extensions (MDMX) というマルチメディア拡張（整数のみ）も発表された\[23\]。

MIPS V を実装した製品は結局登場しなかった。1997年、SGIはコード名 "H1" または "Beast" と、"H2" または "Capitan" というマイクロプロセッサを発表した。前者は最初の MIPS V 実装で、1999年に出荷予定とされた。"H1" と "H2" のプロジェクトは後に統合され、最終的に1998年に中止となった。

MIPS V は pair-single (PS) と呼ばれる新たなデータ型を追加していた。これは[単精度](https://ja.wikipedia.org/wiki/単精度 "wikilink")（32ビット）浮動小数点数のペアを64ビットのFPUレジスタに格納するものである。算術演算命令、比較命令、条件転送命令ではPSデータをSIMD風に扱う。またPSデータのロード、配置変更、変換などの命令が追加されている。既存リソースで浮動小数点SIMDを実現しようという試みだった\[24\]。

## MIPS CPU ファミリ

[thumb](https://ja.wikipedia.org/wiki/ファイル:MIPS_Architecture_\(Pipelined\).svg "wikilink")

初の商用モデル**[R2000](../Page/R2000.md "wikilink")**は1985年に発表された。実行に複数サイクルを要する乗算と除算命令の処理部をチップ上にやや独立したユニットとして追加した。乗除算の結果は直接汎用レジスタには入らず、専用のレジスタに出力されるため、それを汎用レジスタに持ってくる命令も追加された。その命令を乗除算の完了前に発行するとパイプラインがインターロックする。

R2000は起動時に[ビッグエンディアン](https://ja.wikipedia.org/wiki/ビッグエンディアン "wikilink")と[リトルエンディアン](https://ja.wikipedia.org/wiki/リトルエンディアン "wikilink")のどちらかを選んで動作する。32ビット汎用レジスタを32本持つが、[コンディションコードレジスタを持たない](../Page/ステータスレジスタ.md "wikilink")。設計者はそれがボトルネックになる可能性を考慮したためで、条件判断は指定した2つのレジスタの値の比較を行い、その結果で分岐の可否を判断する。レジスタに入っている値で条件判断するのは[AMD Am29000](../Page/AMD_Am29000.md "wikilink") や [DEC Alpha](https://ja.wikipedia.org/wiki/DEC_Alpha "wikilink") とよく似ている。なお、[プログラムカウンタ](https://ja.wikipedia.org/wiki/プログラムカウンタ "wikilink")には直接アクセスできない。

R2000は最大4個のコプロセッサをサポートしており、そのうち1つは主CPUに組み込まれていて、[例外処理](../Page/例外処理.md "wikilink")、トラップ処理、メモリ管理などを行う。したがって、実際に外付けできるコプロセッサは3個までである。オプションの **R2010** [FPU](../Page/FPU.md "wikilink")をコプロセッサとして接続できる。R2010は32ビットの浮動小数点レジスタを32本持ち、[倍精度](https://ja.wikipedia.org/wiki/倍精度 "wikilink")演算では64ビットレジスタ16本として使用できる。

R2000の後継として**[R3000](../Page/R3000.md "wikilink")**が1988年に登場した。命令およびデータ向けにそれぞれ32KB（間もなく64KBに拡大）のキャッシュを追加し、[マルチプロセッシング](../Page/マルチプロセッシング.md "wikilink")のための[キャッシュコヒーレンシ](https://ja.wikipedia.org/wiki/キャッシュコヒーレンシ "wikilink")にも配慮していた。そのマルチプロセッササポートには欠陥があったが、R3000で何とかマルチプロセッサ構成にした製品がいくつか存在した。R3000には当時の他のマイクロプロセッサと同様に[メモリ管理ユニット](../Page/メモリ管理ユニット.md "wikilink") (MMU) も組み込まれていた。R3000にもR2000のときと同様に **R3010** FPUが存在した。MIPSアーキテクチャのプロセッサとしては初めて市場で成功を収め、累計100万個以上が生産された。改良によって最高40MHzで動作する**R3000A**が登場し、32[VUPs (VAX Unit of Performance)の性能を発揮した](https://ja.wikipedia.org/wiki/MIPS "wikilink")。R3000A互換の **R3051** は[ソニー・コンピュータエンタテインメント](https://ja.wikipedia.org/wiki/ソニー・コンピュータエンタテインメント "wikilink")の[PlayStationに採用され](../Page/PlayStation_\(ゲーム機\).md "wikilink")、33.8688MHzで動作した。サードパーティはR3000AとR3010をワンチップ化したものを設計しており、Performance Semiconductor の**PR3400**、IDTの**R3500**、NECの**VR3600**がある。[東芝](../Page/東芝.md "wikilink")の**TX3900**は[SoCであり](../Page/System-on-a-chip.md "wikilink")、[Windows CE](../Page/Microsoft_Windows_Embedded_CE.md "wikilink") の動作する[ハンドヘルドPC向けに開発された](../Page/ハンドヘルドコンピュータ.md "wikilink")。航空宇宙分野向けに電磁波耐性を強化した[Mongoose-VもR](https://ja.wikipedia.org/wiki/:en:Mongoose-V "wikilink")3000とR3010をワンチップ化していた。

**[R4000](https://ja.wikipedia.org/wiki/R4000 "wikilink")**シリーズは1991年に登場した。命令セットを完全な64ビット対応に拡張し、FPUをCPUチップに統合し、従来よりずっと高いクロック周波数で動作した（当初は100MHz）。しかし、クロック周波数を上げるために一次キャッシュは命令とデータそれぞれ8KBに減らされ、キャッシュアクセスに3サイクルかかるようになった。動作周波数を上げるため、[スーパーパイプライン](https://ja.wikipedia.org/wiki/スーパーパイプライン "wikilink")と呼ばれるパイプライン段数を増やす工夫を行っている。改良版の**R4400**は1993年に登場。一次キャッシュが16KBに倍増され、64ビット関連のバグ（エラッタ）が一掃され、より大きな二次キャッシュをサポートしている。

SGIの一部門となったミップスは外部バスを32ビットに縮小した低価格の**[R4200](https://ja.wikipedia.org/wiki/R4200 "wikilink")**を設計し、さらに安価な**[R4300i](https://ja.wikipedia.org/wiki/R4200#R4300i "wikilink")**のベースとなった。R4300iをベースとして[NECが開発したVR](../Page/日本電気.md "wikilink")4300はゲーム機の[NINTENDO64](../Page/NINTENDO64.md "wikilink")に採用された\[25\]。

[thumb](https://ja.wikipedia.org/wiki/ファイル:IDT_R4700_diephoto2.jpg "wikilink") が設計し、[IDT](../Page/IDT.md "wikilink")が製造した。\]\] [thumb](https://ja.wikipedia.org/wiki/ファイル:KL_IDT_R4700_MIPS_Microprocessor.jpg "wikilink") ミップスの元従業員が創業した [Quantum Effect Devices](../Page/Quantum_Effect_Devices.md "wikilink") (QED) は、**[R4600](https://ja.wikipedia.org/wiki/R4600 "wikilink")** *Orion*、**R4700** *Orion*、**R4650**、**[R5000](https://ja.wikipedia.org/wiki/R5000 "wikilink")**を設計した。R4000がクロック周波数を上げるためにキャッシュ容量を犠牲にしたのに対して、QEDは2サイクルでアクセスできる大きなキャッシュを搭載し、シリコンの面積の効率的利用を達成した。R4600とR4700は SGI Indy の低価格版で採用され、シスコのルーター（36x0、7x00など）でもMIPSアーキテクチャとして初めて採用された。R4650は[WebTV](../Page/WebTV.md "wikilink")のセットトップボックスで採用された。R5000は[単精度](https://ja.wikipedia.org/wiki/単精度 "wikilink")浮動小数点演算性能を向上させており、同クロック周波数のR4400を搭載した同型機（SGI Indy）よりもグラフィックス描画が高速になった。SGIは同じグラフィックスボードでもR5000向けは名称を変更し、性能が高いことを強調した。QEDはその後、ネットワーク機器やレーザープリンターなどの組み込み市場向けに**RM7000**と**RM9000**というファミリーを設計した。RM7000は256KBの二次キャッシュをチップ上に搭載し、三次キャッシュのコントローラも備えていた。RM9xx0は[SOCファミリーで](../Page/System-on-a-chip.md "wikilink")、CPUに[メモリコントローラ](https://ja.wikipedia.org/wiki/メモリコントローラ "wikilink")、[PCIコントローラ](../Page/Peripheral_Component_Interconnect.md "wikilink")、[ギガビット・イーサネット](../Page/ギガビット・イーサネット.md "wikilink")のコントローラ、[HyperTransport](../Page/HyperTransport.md "wikilink")ポートなどの高速I/Oといった[ノースブリッジ](../Page/ノースブリッジ.md "wikilink")機能を集積している。QEDは2000年8月、半導体企業 [PMC-Sierra](https://ja.wikipedia.org/wiki/PMC-Sierra "wikilink") に買収され、PMC-SierraがMIPSアーキテクチャのプロセッサ開発を継続している。

[R8000](https://ja.wikipedia.org/wiki/R8000 "wikilink")（1994年）はミップスの設計による初の[スーパースケーラ](https://ja.wikipedia.org/wiki/スーパースケーラ "wikilink")方式で、複数の命令を同時に実行可能となった。ワンチップではなく、CPU+一次キャッシュ（命令・データそれぞれ16KB）、FPU、二次キャッシュのタグRAMチップ×3（2個はキャッシュアクセス用、1つはバススヌープ用）、キャッシュコントローラの6個のチップで構成されている。完全にパイプライン化された加算・乗算ユニットを2つ持ち、外付けの4MBの二次キャッシュからFPUが直接データを取ってくる設計である。SGIの POWER Challenge サーバで採用され、後に POWER Indigo2 ワークステーションでも採用された。しかし浮動小数点演算性能は高いが整数演算性能はあまり高くないため科学技術計算などにしか向かず、また複数チップで構成されるためコストが高く、SGI以外では採用例がない。

1995年**[R10000](https://ja.wikipedia.org/wiki/R10000 "wikilink")**がリリースされた。シングルチップでR8000よりも高いクロック周波数で動作し、一次キャッシュは命令・データ共に32KBと大きい。スーパースケーラ設計だが、最大の改良点は[アウト・オブ・オーダー実行](../Page/アウト・オブ・オーダー実行.md "wikilink")を採用した点である。メモリ・パイプラインは1つしかなく、FPUもR8000より単純だが、整数演算性能が大幅に強化されており、低コストでもあったため、市場で成功を収めた。

その後の設計は全てR10000コアをベースとしている。**[R12000](https://ja.wikipedia.org/wiki/R10000#R12000 "wikilink")**は0.25μmプロセスを採用してチップを縮小し、クロック周波数を高めている。それを改良した**[R14000](https://ja.wikipedia.org/wiki/R10000#R14000 "wikilink")**でもクロック周波数を向上させると共に、外付けの二次キャッシュに [DDR](../Page/DDR_SDRAM.md "wikilink") [SRAM](../Page/Static_Random_Access_Memory.md "wikilink") を利用可能にした。その後もクロック周波数を向上させ内蔵キャッシュ容量を増加させた**[R16000](https://ja.wikipedia.org/wiki/R10000#R16000 "wikilink")**と**R16000A**がリリースされた。

他にもMIPSファミリーには**[R6000](https://ja.wikipedia.org/wiki/R6000 "wikilink")**（1991年）がある。[ECLで実装したもので](../Page/エミッタ結合論理.md "wikilink")、Bipolar Integrated Technology が製造した。R6000では MIPS II 命令セットが初めて採用された。[TLBとキャッシュのアーキテクチャが他のMIPSファミリーとは大きく異なる](../Page/トランスレーション・ルックアサイド・バッファ.md "wikilink")。発表したとおりの性能を発揮できなかったが、[CDCがサーバに採用した](../Page/コントロール・データ・コーポレーション.md "wikilink")。しかし、すぐに市場から姿を消した。

### MIPS マイクロプロセッサの仕様

<table>
<thead>
<tr class="header">
<th><p>モデル</p></th>
<th><p>動作周波数[MHz]</p></th>
<th><p>登場年</p></th>
<th><p>プロセス[μm]</p></th>
<th><p>トランジスタ[百万]</p></th>
<th><p>ダイサイズ[mm<sup>2</sup>]</p></th>
<th><p>ピン数</p></th>
<th><p>電力[W]</p></th>
<th><p>電圧[V]</p></th>
<th><p>データキャッシュ[kB]</p></th>
<th><p>命令キャッシュ[kB]</p></th>
<th><p>2次キャッシュ</p></th>
<th><p>3次キャッシュ</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><a href="../Page/R2000.md" title="wikilink">R2000</a></p></td>
<td><p>8 - 16.67</p></td>
<td><p>1985</p></td>
<td><p>2.0</p></td>
<td><p>0.11</p></td>
<td><p>--</p></td>
<td><p>--</p></td>
<td><p>--</p></td>
<td><p>--</p></td>
<td><p>32</p></td>
<td><p>64</p></td>
<td><p>none</p></td>
<td><p>none</p></td>
</tr>
<tr class="even">
<td><p><a href="../Page/R3000.md" title="wikilink">R3000</a></p></td>
<td><p>12 - 40</p></td>
<td><p>1988</p></td>
<td><p>1.2</p></td>
<td><p>0.11</p></td>
<td><p>66.12</p></td>
<td><p>145</p></td>
<td><p>4</p></td>
<td><p>--</p></td>
<td><p>64</p></td>
<td><p>64</p></td>
<td><p>0-256KB （外付）</p></td>
<td><p>none</p></td>
</tr>
<tr class="odd">
<td><p><a href="https://ja.wikipedia.org/wiki/R4000" title="wikilink">R4000</a></p></td>
<td><p>100</p></td>
<td><p>1991</p></td>
<td><p>0.8</p></td>
<td><p>1.35</p></td>
<td><p>213</p></td>
<td><p>179</p></td>
<td><p>15</p></td>
<td><p>5</p></td>
<td><p>8</p></td>
<td><p>8</p></td>
<td><p>1MB （外付）</p></td>
<td><p>none</p></td>
</tr>
<tr class="even">
<td><p><a href="https://ja.wikipedia.org/wiki/R4400" title="wikilink">R4400</a></p></td>
<td><p>100-250</p></td>
<td><p>1992</p></td>
<td><p>0.6</p></td>
<td><p>2.3</p></td>
<td><p>186</p></td>
<td><p>179</p></td>
<td><p>15</p></td>
<td><p>5</p></td>
<td><p>16</p></td>
<td><p>16</p></td>
<td><p>1-4MB （外付）</p></td>
<td><p>none</p></td>
</tr>
<tr class="odd">
<td><p><a href="https://ja.wikipedia.org/wiki/R4600" title="wikilink">R4600</a></p></td>
<td><p>100-133</p></td>
<td><p>1994</p></td>
<td><p>0.64</p></td>
<td><p>2.2</p></td>
<td><p>77</p></td>
<td><p>179</p></td>
<td><p>4.6</p></td>
<td><p>5</p></td>
<td><p>16</p></td>
<td><p>16</p></td>
<td><p>512KB （外付）</p></td>
<td><p>none</p></td>
</tr>
<tr class="even">
<td><p><a href="https://ja.wikipedia.org/wiki/R4600" title="wikilink">R4650</a></p></td>
<td><p>133-180</p></td>
<td><p>1994</p></td>
<td><p>0.64</p></td>
<td><p>2.2?</p></td>
<td><p>77?</p></td>
<td><p>179?</p></td>
<td><p>4.6?</p></td>
<td><p>5</p></td>
<td><p>16</p></td>
<td><p>16</p></td>
<td><p>512KB （外付）</p></td>
<td><p>none</p></td>
</tr>
<tr class="odd">
<td><p><a href="https://ja.wikipedia.org/wiki/R4600" title="wikilink">R4700</a></p></td>
<td><p>100-200</p></td>
<td><p>1996</p></td>
<td><p>0.5</p></td>
<td><p>2.2?</p></td>
<td><p>--</p></td>
<td><p>179</p></td>
<td><p>--</p></td>
<td><p>--</p></td>
<td><p>16</p></td>
<td><p>16</p></td>
<td><p>外付</p></td>
<td><p>none</p></td>
</tr>
<tr class="even">
<td><p><a href="https://ja.wikipedia.org/wiki/R5000" title="wikilink">R5000</a></p></td>
<td><p>150-200</p></td>
<td><p>1996</p></td>
<td><p>0.35</p></td>
<td><p>3.7</p></td>
<td><p>84</p></td>
<td><p>223</p></td>
<td><p>10</p></td>
<td><p>3.3</p></td>
<td><p>32</p></td>
<td><p>32</p></td>
<td><p>1MB （外付）</p></td>
<td><p>none</p></td>
</tr>
<tr class="odd">
<td><p><a href="https://ja.wikipedia.org/wiki/R8000" title="wikilink">R8000</a></p></td>
<td><p>75-90</p></td>
<td><p>1994</p></td>
<td><p>0.7</p></td>
<td><p>2.6</p></td>
<td><p>299</p></td>
<td><p>591+591</p></td>
<td><p>30</p></td>
<td><p>3.3</p></td>
<td><p>16</p></td>
<td><p>16</p></td>
<td><p>4MB （外付）</p></td>
<td><p>none</p></td>
</tr>
<tr class="even">
<td><p><a href="https://ja.wikipedia.org/wiki/R10000" title="wikilink">R10000</a></p></td>
<td><p>150-200</p></td>
<td><p>1996</p></td>
<td><p>0.35, 0.25</p></td>
<td><p>6.7</p></td>
<td><p>299</p></td>
<td><p>599</p></td>
<td><p>30</p></td>
<td><p>3.3</p></td>
<td><p>32</p></td>
<td><p>32</p></td>
<td><p>512KB-16MB （外付）</p></td>
<td><p>none</p></td>
</tr>
<tr class="odd">
<td><p><a href="https://ja.wikipedia.org/wiki/R10000" title="wikilink">R12000</a></p></td>
<td><p>270-400</p></td>
<td><p>1998</p></td>
<td><p>0.25, 0.18</p></td>
<td><p>6.9</p></td>
<td><p>204</p></td>
<td><p>600</p></td>
<td><p>20</p></td>
<td><p>4</p></td>
<td><p>32</p></td>
<td><p>32</p></td>
<td><p>512KB-16MB （外付）</p></td>
<td><p>none</p></td>
</tr>
<tr class="even">
<td><p>RM7000</p></td>
<td><p>250-600</p></td>
<td><p>1998</p></td>
<td><p>0.25, 0.18, 0.13</p></td>
<td><p>18</p></td>
<td><p>91</p></td>
<td><p>304</p></td>
<td><p>10, 6, 3</p></td>
<td><p>3.3, 2.5, 1.5</p></td>
<td><p>16</p></td>
<td><p>16</p></td>
<td><p>256KB （内蔵）</p></td>
<td><p>1MB （外付）</p></td>
</tr>
<tr class="odd">
<td><p>MIPS32 4K</p></td>
<td><p>138</p></td>
<td><p>1999</p></td>
<td><p>0.18</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>MIPS64 5K</p></td>
<td></td>
<td><p>1999</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>MIPS64 20K</p></td>
<td></td>
<td><p>2000</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p><a href="https://ja.wikipedia.org/wiki/R10000" title="wikilink">R14000</a></p></td>
<td><p>500-600</p></td>
<td><p>2001</p></td>
<td><p>0.13</p></td>
<td><p>7.2</p></td>
<td><p>204</p></td>
<td><p>527</p></td>
<td><p>17</p></td>
<td><p>--</p></td>
<td><p>32</p></td>
<td><p>32</p></td>
<td><p>512KB-16MB （外付）</p></td>
<td><p>none</p></td>
</tr>
<tr class="odd">
<td><p><a href="https://ja.wikipedia.org/wiki/R10000" title="wikilink">R16000</a></p></td>
<td><p>700-1000</p></td>
<td><p>2002</p></td>
<td><p>0.11</p></td>
<td><p>--</p></td>
<td><p>--</p></td>
<td><p>--</p></td>
<td><p>20</p></td>
<td><p>--</p></td>
<td><p>64</p></td>
<td><p>64</p></td>
<td><p>512KB-16MB （外付）</p></td>
<td><p>none</p></td>
</tr>
<tr class="even">
<td><p>MIPS32 24K</p></td>
<td><p>400(130nm)<br />
750(65nm)<br />
1468(40nm)</p></td>
<td><p>2003</p></td>
<td><p>40nm 〜 130nm</p></td>
<td><p>--</p></td>
<td><p>0.83 （コアのみ）</p></td>
<td><p>--</p></td>
<td><p>--</p></td>
<td><p>--</p></td>
<td><p>64</p></td>
<td><p>64</p></td>
<td><p>4-16MB （外付）</p></td>
<td><p>none</p></td>
</tr>
<tr class="odd">
<td><p>MIPS32 34K</p></td>
<td><p>500(90nm)<br />
1454(40nm)</p></td>
<td><p>2006</p></td>
<td><p>90nm<br />
65nm<br />
40nm</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>MIPS32 74K</p></td>
<td><p>1080</p></td>
<td><p>2007</p></td>
<td><p>65nm</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>MIPS32 1004K</p></td>
<td><p>1.1GHz</p></td>
<td><p>2008</p></td>
<td><p>65nm</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>MIPS32 1074K</p></td>
<td><p>1.5GHz</p></td>
<td><p>2010</p></td>
<td><p>40nm</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>microAptiv</p></td>
<td></td>
<td><p>2012</p></td>
<td><p>90nm～65nm</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>interAptiv</p></td>
<td></td>
<td><p>2012</p></td>
<td><p>65nm～40nm</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>proAptiv</p></td>
<td></td>
<td><p>2012</p></td>
<td><p>40nm～22nm</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
</tbody>
</table>

注意：主なプロセッサの仕様のみ掲載。

## MIPS I の命令形式

命令は R、I、Jの3種類に分類される。どの命令も先頭に6ビットのオペコードがある。Rタイプではオペコードの次に3本のレジスタを指定するフィールドがあり、シフト量を指定するフィールド、機能を指定するフィールドが続く。Iタイプでは2つのレジスタを指定するフィールドと16ビットの即値のフィールドがある。 Jタイプでは、オペコードに続いて26ビットで分岐先アドレスを指定する\[26\]\[27\]。

次表は主要な命令セットの3種類の形式を示したものである。

| タイプ   | \-31-                                 フォーマット (ビット数)                                 -0- |
| ----- | --------------------------------------------------------------------------------------- |
| **R** | オペコード (6)                                                                               |
| **I** | オペコード (6)                                                                               |
| **J** | オペコード (6)                                                                               |

## MIPS アセンブリ言語

アセンブリ言語には、直接ハードウェア実装に対応した命令以外に複数命令の列に変換される「擬似命令」が存在する。

  - 以下の表で、*d*、*t*、*s* といった文字はレジスタの番号や名前のためのプレースホルダーとなっている。
  - *C* は定数（即値）を示す。
  - オペコード及び機能のコードは16進数である。
  - MIPS32命令セットでは Add や Subtract 命令で使われる *unsigned* という用語が誤解を生みやすいとしている。それらの命令の *signed* と *unsigned* の違いはオペランドを[符号拡張](../Page/符号拡張.md "wikilink")をするかしないかではなく、オーバーフロー発生時にトラップを起こすか *(e.g. Add)* 無視するか *(Add unsigned)* である。それらの命令の即値オペランド CONST は常に符号拡張される。

### 整数

MIPSアーキテクチャは32本の整数レジスタを持つ。算術処理を行うにはデータがレジスタ上になければならない。レジスタ$0は常に0であり、レジスタ$1はアセンブラが一時的に使用する（擬似命令や大きな定数を扱う場合）。

エンコーディングは命令語の各ビットが命令のどの部分と対応しているかを示している。ハイフン (-) はそのビットが無視されることを意味する。

<table>
<thead>
<tr class="header">
<th><p>種類</p></th>
<th><p>名称</p></th>
<th><p>構文</p></th>
<th><p>意味</p></th>
<th><p>形式/オペコード/機能コード</p></th>
<th><p>注記/エンコーディング</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>算術</p></td>
<td><p>Add</p></td>
<td><p>add $d,$s,$t</p></td>
<td><p>$d = $s + $t</p></td>
<td><p>R</p></td>
<td><p>0</p></td>
</tr>
<tr class="even">
<td><p>Add unsigned</p></td>
<td><p>addu $d,$s,$t</p></td>
<td><p>$d = $s + $t</p></td>
<td><p>R</p></td>
<td><p>0</p></td>
<td><p>21<sub>16</sub></p></td>
</tr>
<tr class="odd">
<td><p>Subtract</p></td>
<td><p>sub $d,$s,$t</p></td>
<td><p>$d = $s - $t</p></td>
<td><p>R</p></td>
<td><p>0</p></td>
<td><p>22<sub>16</sub></p></td>
</tr>
<tr class="even">
<td><p>Subtract unsigned</p></td>
<td><p>subu $d,$s,$t</p></td>
<td><p>$d = $s - $t</p></td>
<td><p>R</p></td>
<td><p>0</p></td>
<td><p>23<sub>16</sub></p></td>
</tr>
<tr class="odd">
<td><p>Add immediate</p></td>
<td><p>addi $t,$s,C</p></td>
<td><p>$t = $s + C (signed)</p></td>
<td><p>I</p></td>
<td><p>8<sub>16</sub></p></td>
<td><p>-</p></td>
</tr>
<tr class="even">
<td><p>Add immediate unsigned</p></td>
<td><p>addiu $t,$s,C</p></td>
<td><p>$t = $s + C (signed)</p></td>
<td><p>I</p></td>
<td><p>9<sub>16</sub></p></td>
<td><p>-</p></td>
</tr>
<tr class="odd">
<td><p>Multiply</p></td>
<td><p>mult $s,$t</p></td>
<td><p>LO = (($s * $t) &lt;&lt; 32) &gt;&gt; 32;<br />
HI = ($s * $t) &gt;&gt; 32;</p></td>
<td><p>R</p></td>
<td><p>0</p></td>
<td><p>18<sub>16</sub></p></td>
</tr>
<tr class="even">
<td><p>Divide</p></td>
<td><p>div $s, $t</p></td>
<td><p>LO = $s / $t     HI = $s % $t</p></td>
<td><p>R</p></td>
<td><p>0</p></td>
<td><p>1A<sub>16</sub></p></td>
</tr>
<tr class="odd">
<td><p>Divide unsigned</p></td>
<td><p>divu $s, $t</p></td>
<td><p>LO = $s / $t     HI = $s % $t</p></td>
<td><p>R</p></td>
<td><p>0</p></td>
<td><p>1B<sub>16</sub></p></td>
</tr>
<tr class="even">
<td><p>データ転送</p></td>
<td><p>Load double word</p></td>
<td><p>ld $t,C($s)</p></td>
<td><p>$t = Memory[$s + C]</p></td>
<td><p>I</p></td>
<td><p>23<sub>16</sub></p></td>
</tr>
<tr class="odd">
<td><p>Load word</p></td>
<td><p>lw $t,C($s)</p></td>
<td><p>$t = Memory[$s + C]</p></td>
<td><p>I</p></td>
<td><p>23<sub>16</sub></p></td>
<td><p>-</p></td>
</tr>
<tr class="even">
<td><p>Load halfword</p></td>
<td><p>lh $t,C($s)</p></td>
<td><p>$t = Memory[$s + C] (signed)</p></td>
<td><p>I</p></td>
<td><p>21<sub>16</sub></p></td>
<td><p>-</p></td>
</tr>
<tr class="odd">
<td><p>Load halfword unsigned</p></td>
<td><p>lhu $t,C($s)</p></td>
<td><p>$t = Memory[$s + C] (unsigned)</p></td>
<td><p>I</p></td>
<td><p>25<sub>16</sub></p></td>
<td><p>-</p></td>
</tr>
<tr class="even">
<td><p>Load byte</p></td>
<td><p>lb $t,C($s)</p></td>
<td><p>$t = Memory[$s + C] (signed)</p></td>
<td><p>I</p></td>
<td><p>20<sub>16</sub></p></td>
<td><p>-</p></td>
</tr>
<tr class="odd">
<td><p>Load byte unsigned</p></td>
<td><p>lbu $t,C($s)</p></td>
<td><p>$t = Memory[$s + C] (unsigned)</p></td>
<td><p>I</p></td>
<td><p>24<sub>16</sub></p></td>
<td><p>-</p></td>
</tr>
<tr class="even">
<td><p>Store double word</p></td>
<td><p>sd $t,C($s)</p></td>
<td><p>Memory[$s + C] = $t</p></td>
<td><p>I</p></td>
<td></td>
<td><p>-</p></td>
</tr>
<tr class="odd">
<td><p>Store word</p></td>
<td><p>sw $t,C($s)</p></td>
<td><p>Memory[$s + C] = $t</p></td>
<td><p>I</p></td>
<td><p>2B<sub>16</sub></p></td>
<td><p>-</p></td>
</tr>
<tr class="even">
<td><p>Store half</p></td>
<td><p>sh $t,C($s)</p></td>
<td><p>Memory[$s + C] = $t</p></td>
<td><p>I</p></td>
<td><p>29<sub>16</sub></p></td>
<td><p>-</p></td>
</tr>
<tr class="odd">
<td><p>Store byte</p></td>
<td><p>sb $t,C($s)</p></td>
<td><p>Memory[$s + C] = $t</p></td>
<td><p>I</p></td>
<td><p>28<sub>16</sub></p></td>
<td><p>-</p></td>
</tr>
<tr class="even">
<td><p>Load upper immediate</p></td>
<td><p>lui $t,C</p></td>
<td><p>$t = C &lt;&lt; 16</p></td>
<td><p>I</p></td>
<td><p>F<sub>16</sub></p></td>
<td><p>-</p></td>
</tr>
<tr class="odd">
<td><p>Move from high</p></td>
<td><p>mfhi $d</p></td>
<td><p>$d = HI</p></td>
<td><p>R</p></td>
<td><p>0</p></td>
<td><p>10<sub>16</sub></p></td>
</tr>
<tr class="even">
<td><p>Move from low</p></td>
<td><p>mflo $d</p></td>
<td><p>$d = LO</p></td>
<td><p>R</p></td>
<td><p>0</p></td>
<td><p>12<sub>16</sub></p></td>
</tr>
<tr class="odd">
<td><p>Move from Control Register</p></td>
<td><p>mfcZ $t, $s</p></td>
<td><p>$t = Coprocessor[Z].ControlRegister[$s]</p></td>
<td><p>R</p></td>
<td><p>0</p></td>
<td></td>
</tr>
<tr class="even">
<td><p>Move to Control Register</p></td>
<td><p>mtcZ $t, $s</p></td>
<td><p>Coprocessor[Z].ControlRegister[$s] = $t</p></td>
<td><p>R</p></td>
<td><p>0</p></td>
<td></td>
</tr>
<tr class="odd">
<td><p>論理</p></td>
<td><p>And</p></td>
<td><p>and $d,$s,$t</p></td>
<td><p>$d = $s &amp; $t</p></td>
<td><p>R</p></td>
<td><p>0</p></td>
</tr>
<tr class="even">
<td><p>And immediate</p></td>
<td><p>andi $t,$s,C</p></td>
<td><p>$t = $s &amp; C</p></td>
<td><p>I</p></td>
<td><p>C<sub>16</sub></p></td>
<td><p>-</p></td>
</tr>
<tr class="odd">
<td><p>Or</p></td>
<td><p>or $d,$s,$t</p></td>
<td><p>$d = $s | $t</p></td>
<td><p>R</p></td>
<td><p>0</p></td>
<td><p>25<sub>16</sub></p></td>
</tr>
<tr class="even">
<td><p>Or immediate</p></td>
<td><p>ori $t,$s,C</p></td>
<td><p>$t = $s | C</p></td>
<td><p>I</p></td>
<td><p>D<sub>16</sub></p></td>
<td><p>-</p></td>
</tr>
<tr class="odd">
<td><p>Exclusive or</p></td>
<td><p>xor $d,$s,$t</p></td>
<td><p>$d = $s ^ $t</p></td>
<td><p>R</p></td>
<td><p>0</p></td>
<td><p>26<sub>16</sub></p></td>
</tr>
<tr class="even">
<td><p>Nor</p></td>
<td><p>nor $d,$s,$t</p></td>
<td><p>$d = ~ ($s | $t)</p></td>
<td><p>R</p></td>
<td><p>0</p></td>
<td><p>27<sub>16</sub></p></td>
</tr>
<tr class="odd">
<td><p>Set on less than</p></td>
<td><p>slt $d,$s,$t</p></td>
<td><p>$d = ($s &lt; $t)</p></td>
<td><p>R</p></td>
<td><p>0</p></td>
<td><p>2A<sub>16</sub></p></td>
</tr>
<tr class="even">
<td><p>Set on less than immediate</p></td>
<td><p>slti $t,$s,C</p></td>
<td><p>$t = ($s &lt; C)</p></td>
<td><p>I</p></td>
<td><p>A<sub>16</sub></p></td>
<td><p>-</p></td>
</tr>
<tr class="odd">
<td><p>シフト</p></td>
<td><p>Shift left logical</p></td>
<td><p>sll $d,$t,C</p></td>
<td><p>$d = $t &lt;&lt; C</p></td>
<td><p>R</p></td>
<td><p>0</p></td>
</tr>
<tr class="even">
<td><p>Shift right logical</p></td>
<td><p>srl $d,$t,C</p></td>
<td><p>$d = $t &gt;&gt; C</p></td>
<td><p>R</p></td>
<td><p>0</p></td>
<td><p>2<sub>16</sub></p></td>
</tr>
<tr class="odd">
<td><p>Shift right arithmetic</p></td>
<td><p>sra $d,$t,C</p></td>
<td><p><span class="math inline">$\scriptstyle \$d = \$t &gt;&gt; C + \left(\left(\sum_{n=1}^{\text{CONST}}2^{31-n}\right)\cdot \$2&gt;&gt;31\right)$</span></p></td>
<td><p>R</p></td>
<td><p>0</p></td>
<td><p>3<sub>16</sub></p></td>
</tr>
<tr class="even">
<td><p>条件分岐</p></td>
<td><p>Branch on equal</p></td>
<td><p>beq $s,$t,C</p></td>
<td><p>if ($s == $t) go to PC+4+4*C</p></td>
<td><p>I</p></td>
<td><p>4<sub>16</sub></p></td>
</tr>
<tr class="odd">
<td><p>Branch on not equal</p></td>
<td><p>bne $s,$t,C</p></td>
<td><p>if ($s != $t) go to PC+4+4*C</p></td>
<td><p>I</p></td>
<td><p>5<sub>16</sub></p></td>
<td><p>-</p></td>
</tr>
<tr class="even">
<td><p>無条件ジャンプ</p></td>
<td><p>Jump</p></td>
<td><p>j C</p></td>
<td><p>PC = PC+4[31:28] . C*4</p></td>
<td><p>J</p></td>
<td><p>2<sub>16</sub></p></td>
</tr>
<tr class="odd">
<td><p>Jump register</p></td>
<td><p>jr $s</p></td>
<td><p>goto address $s</p></td>
<td><p>R</p></td>
<td><p>0</p></td>
<td><p>8<sub>16</sub></p></td>
</tr>
<tr class="even">
<td><p>Jump and link</p></td>
<td><p>jal C</p></td>
<td><p>$31 = PC + 8; PC = PC+4[31:28] . C*4</p></td>
<td><p>J</p></td>
<td><p>3<sub>16</sub></p></td>
<td><p>-</p></td>
</tr>
</tbody>
</table>

注: MIPSのアセンブリ言語のコード上、分岐命令での分岐先アドレスはラベルで表現される。

注: "load lower immediate" 命令は存在しない。これは addi 命令や ori 命令でレジスタ $0 を使うことで実現される。例えば、`addi $1, $0, 100` も `ori $1, $0, 100` もレジスタ$1に100という値が格納される。

注: 即値を減算するには、その値の否定を即値として加算すればよい。

### 浮動小数点数

MIPSアーキテクチャには32本の浮動小数点レジスタがある。2本のレジスタで[倍精度](https://ja.wikipedia.org/wiki/倍精度 "wikilink")の数値を表す。奇数番目のレジスタで倍精度の数値を指定することはできない。

| 種類                                    | 名称                                    | 構文                                                         | 意味                                                         | 形式/オペコード/機能 | 注記/エンコーディング |
| ------------------------------------- | ------------------------------------- | ---------------------------------------------------------- | ---------------------------------------------------------- | ----------- | ----------- |
| 算術                                    | FP add single                         | add.s $x,$y,$z                                             | $x = $y + $z                                               |             |             |
| FP subtract single                    | sub.s $x,$y,$z                        | $x = $y - $z                                               |                                                            |             |             |
| FP multiply single                    | mul.s $x,$y,$z                        | $x = $y \* $z                                              |                                                            |             |             |
| FP divide single                      | div.s $x,$y,$z                        | $x = $y / $z                                               |                                                            |             |             |
| FP add double                         | add.d $x,$y,$z                        | $x = $y + $z                                               |                                                            |             |             |
| FP subtract double                    | sub.d $x,$y,$z                        | $x = $y - $z                                               |                                                            |             |             |
| FP multiply double                    | mul.d $x,$y,$z                        | $x = $y \* $z                                              |                                                            |             |             |
| FP divide double                      | div.d $x,$y,$z                        | $x = $y / $z                                               |                                                            |             |             |
| データ転送                                 | Load word coprocessor                 | lwcZ $x,CONST ($y)                                         | Coprocessor\[Z\].DataRegister\[$x\] = Memory\[$y + CONST\] | I           |             |
| Store word coprocessor                | swcZ $x,CONST ($y)                    | Memory\[$y + CONST\] = Coprocessor\[Z\].DataRegister\[$x\] | I                                                          |             |             |
| 論理（比較）                                | FP compare single (eq,ne,lt,le,gt,ge) | c.lt.s $f2,$f4                                             | if ($f2 \< $f4) cond=1; else cond=0                        |             |             |
| FP compare double (eq,ne,lt,le,gt,ge) | c.lt.d $f2,$f4                        | if ($f2 \< $f4) cond=1; else cond=0                        |                                                            |             |             |
| 分岐                                    | branch on FP true                     | bc1t 100                                                   | if (cond == 1) go to PC+4+100                              |             |             |
| branch on FP false                    | bc1f 100                              | if (cond == 0) go to PC+4+100                              |                                                            |             |             |

### 擬似命令

MIPSアセンブラは以下の命令を受け付けるが、これらは実際にはMIPSの命令セットに存在しない。アセンブラが同等の命令列に変換し、その際に $1 ($at) レジスタを一時的に使用することがある。

<table>
<thead>
<tr class="header">
<th><p>名称</p></th>
<th><p>構文</p></th>
<th><p>実際の命令列</p></th>
<th><p>意味</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Move</p></td>
<td><p>move $rt,$rs</p></td>
<td><p>addi $rt,$rs,0</p></td>
<td><p>R[rt]=R[rs]</p></td>
</tr>
<tr class="even">
<td><p>Load Address</p></td>
<td><p>la $at, LabelAddr</p></td>
<td><p>lui $at, LabelAddr[31:16]; ori $at,$at, LabelAddr[15:0]</p></td>
<td><p>$at = Label Address<br />
リンカがアドレスを決定した際に命令を書き換える。</p></td>
</tr>
<tr class="odd">
<td><p>Load Immediate</p></td>
<td><p>li $at, IMMED[31:0]</p></td>
<td><p>lui $at, IMMED[31:16]; ori $at,$at, IMMED[15:0]</p></td>
<td><p>$at = 32ビット即値</p></td>
</tr>
<tr class="even">
<td><p>Branch if greater than</p></td>
<td><p>bgt $rs,$rt,Label</p></td>
<td><p>slt $at,$rt,$rs; bne $at,$zero,Label</p></td>
<td><p>if(R[rs]&gt;R[rt]) PC=Label</p></td>
</tr>
<tr class="odd">
<td><p>Branch if less than</p></td>
<td><p>blt $rs,$rt,Label</p></td>
<td><p>slt $at,$rs,$rt; bne $at,$zero,Label</p></td>
<td><p>if(R[rs]&lt;R[rt]) PC=Label</p></td>
</tr>
<tr class="even">
<td><p>Branch if greater than or equal</p></td>
<td><p>bge $rs,$rt,Label</p></td>
<td><p>slt $at,$rs,$rt; beq $at,$zero,Label</p></td>
<td><p>if(R[rs]&gt;=R[rt]) PC=Label</p></td>
</tr>
<tr class="odd">
<td><p>Branch if less than or equal</p></td>
<td><p>ble $rs,$rt,Label</p></td>
<td><p>slt $at,$rt,$rs; beq $at,$zero,Label</p></td>
<td><p>if(R[rs]&lt;=R[rt]) PC=Label</p></td>
</tr>
<tr class="even">
<td><p>Branch if greater than unsigned</p></td>
<td><p>bgtu $rs,$rt,Label</p></td>
<td></td>
<td><p>if(R[rs]=&gt;R[rt]) PC=Label</p></td>
</tr>
<tr class="odd">
<td><p>Branch if greater than zero</p></td>
<td><p>bgtz $rs,$rt,Label</p></td>
<td></td>
<td><p>if(R[rs]&gt;0) PC=Label</p></td>
</tr>
<tr class="even">
<td><p>Multiplies and returns only first 32 bits</p></td>
<td><p>mul $1, $2, $3</p></td>
<td><p>mult $2, $3; mflo $1</p></td>
<td><p>$1 = $2 * $3</p></td>
</tr>
</tbody>
</table>

### その他の命令

  - [NOP](../Page/NOP.md "wikilink")命令。通常 `sll $0,$0,0` という命令を使い、その機械語コードは 0x00000000 となる。
  - break命令。[デバッガ](../Page/デバッガ.md "wikilink")でのブレークポイント設定で使用する。
  - syscall命令。[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink")の[システムコール](../Page/システムコール.md "wikilink")に使われ、ユーザーモードからカーネルモードに移行する。

## コンパイラのレジスタ使用規則

ハードウェアのアーキテクチャにより、以下のことが定められている。

  - 汎用レジスタ $0 は常に 0 という値を返す。このレジスタに値を書いても変化はしないし、書いた値は消失する。
  - 汎用レジスタ $31 は jal (jump and link) 命令でリンクレジスタとして使われる。
  - HIおよびLOレジスタは乗除算の結果へのアクセスに使われ、mfhi (move from high) 命令と mflo 命令がそのためにある。

汎用レジスタを使う際のハードウェア上の制限はこれだけである。

各種MIPSツールチェーンでは、レジスタをどのように使うかについて[呼出規約](https://ja.wikipedia.org/wiki/呼出規約 "wikilink")を定めている。これはツールチェーンのソフトウェアが定めているもので、ハードウェアにそのような制限があるわけではない。

<table>
<caption><strong>レジスタ</strong></caption>
<thead>
<tr class="header">
<th><p>名称</p></th>
<th><p>番号</p></th>
<th><p>用途</p></th>
<th><p>呼び出された側が内容を保存する必要があるか?</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>$zero</p></td>
<td><p>$0</p></td>
<td><p>常に 0</p></td>
<td><p>N/A</p></td>
</tr>
<tr class="even">
<td><p>$at</p></td>
<td><p>$1</p></td>
<td><p>アセンブラが一時的に使用</p></td>
<td></td>
</tr>
<tr class="odd">
<td><p>$v0–$v1</p></td>
<td><p>$2–$3</p></td>
<td><p>関数の戻り値や式を評価した結果</p></td>
<td></td>
</tr>
<tr class="even">
<td><p>$a0–$a3</p></td>
<td><p>$4–$7</p></td>
<td><p>関数の引数</p></td>
<td></td>
</tr>
<tr class="odd">
<td><p>$t0–$t7</p></td>
<td><p>$8–$15</p></td>
<td><p>一時変数</p></td>
<td></td>
</tr>
<tr class="even">
<td><p>$s0–$s7</p></td>
<td><p>$16–$23</p></td>
<td><p>一時変数だがセーブされる</p></td>
<td></td>
</tr>
<tr class="odd">
<td><p>$t8–$t9</p></td>
<td><p>$24–$25</p></td>
<td><p>一時変数</p></td>
<td></td>
</tr>
<tr class="even">
<td><p>$k0–$k1</p></td>
<td><p>$26–$27</p></td>
<td><p>OSのカーネル用に予約</p></td>
<td></td>
</tr>
<tr class="odd">
<td><p>$gp</p></td>
<td><p>$28</p></td>
<td><p>広域（グローバル）ポインタ</p></td>
<td></td>
</tr>
<tr class="even">
<td><p>$sp</p></td>
<td><p>$29</p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/スタックポインタ" title="wikilink">スタックポインタ</a></p></td>
<td></td>
</tr>
<tr class="odd">
<td><p>$fp($s8)</p></td>
<td><p>$30</p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/コールスタック" title="wikilink">フレームポインタ</a></p></td>
<td></td>
</tr>
<tr class="even">
<td><p>$ra</p></td>
<td><p>$31</p></td>
<td><p>リターンアドレス</p></td>
<td><p>N/A</p></td>
</tr>
</tbody>
</table>

呼び出された側が保存すると定められているレジスタは、サブルーチンや関数の呼び出しや[システムコール](../Page/システムコール.md "wikilink")でも保持される。例えば、$s-レジスタをルーチン内で使うときは、その内容をスタックに一時的に退避させなければならない。$sp と $fp はルーチンに入ってきたときにセーブされ、それぞれルーチン固有の固定値でインクリメントされる。そして、そのルーチンから戻るときに元の値に戻す。一方 $ra は jal 命令でルーチンに飛び込むときに自動的に変更される。$t-レジスタはサブルーチンを呼び出すと内容が破壊されるので、必要なら呼び出す側がセーブしておかなければならない。

## シミュレータ

Open Virtual Platforms (OVP)\[28\] では、非商用利用に限って無料で使えるシミュレータ [OVPsim](https://ja.wikipedia.org/wiki/:en:OVPsim "wikilink")、プロセッサや周辺機器やプラットフォームのモデルのライブラリ、ユーザーが独自のモデルを開発できるAPIなどを提供している。ライブラリに含まれるモデルは[オープンソース](../Page/オープンソース.md "wikilink")で[C言語](../Page/C言語.md "wikilink")で書かれており、MIPSの 4K, 24K, 34K, 74K, 1004K, 1074K, M14K といったコアが揃っている。それらのモデルの開発と保守は Imperas が行っており\[29\]、ミップス・テクノロジーズの協力の下で評価し MIPS-Verified (tm) というマークをもらっている。MIPSベースのプラットフォームのモデルとしては、非常に単純なものとLinuxのバイナリイメージをブートできるものが用意されている。それらのプラットフォーム・エミュレータはソースとバイナリの形で提供されており、高速で使いやすい。

また、教育向けのMIPS32（当初はR2000/R3000をシミュレートしていた）のフリーなシミュレータ SPIM がある\[30\]。EduMIPS64\[31\] は、GPLライセンスのグラフィカルなMIPS64シミュレータで、Java/Swingで書かれている。MIPS64 ISA の大部分をカバーするサブセットをサポートしており、アセンブリ言語で書かれたプログラムを実行したときCPU内のパイプラインで何が起きているかをグラフィカルに表示する。こちらも教育向けで、世界各地の大学で利用されている。

MARS\[32\] もGUIベースのMIPSエミュレータで教育向けに作られており、特にヘネシーの『コンピュータの構成と設計』を教科書として使う際に役立つよう設計されている。

より実用的なフリーなエミュレータとして[GXemulや](https://ja.wikipedia.org/wiki/:en:GXemul "wikilink")[QEMU](../Page/QEMU.md "wikilink")プロジェクトのものがある。MIPS III および IV のプロセッサをエミュレートでき、コンピュータシステム全体のエミュレートも可能である。

商用のシミュレータは主に組み込み用MIPSプロセッサを対象としたものが存在する。例えば、Virtutech [Simics](https://ja.wikipedia.org/wiki/:en:Simics "wikilink") (MIPS 4Kc and 5Kc, PMC RM9000, QED RM7000)、VaST Systems (R3000, R4000)、[CoWare](https://ja.wikipedia.org/wiki/:en:Coware "wikilink") (MIPS4KE, MIPS24K, MIPS25Kf, MIPS34K) がある。

## 脚注

### 注釈

### 出典

## 参考文献

  -   -
      -
      - プロセッサを中心としたコンピュータの設計全般に関する書籍で、命令セットの例としてMIPSアーキテクチャを取り上げている。MIPS開発者であるジョン・L・ヘネシーも著者の一人である。

  -   - MIPSアーキテクチャについての決定版的な本。ハードウェアアーキテクチャだけでなく、コンパイラやOSについても詳述している。

  -
## 関連項目

  - [μClinux](https://ja.wikipedia.org/wiki/μClinux "wikilink")
  - [PlayStation](../Page/PlayStation_\(ゲーム機\).md "wikilink") - CPUとしてR3000Aを搭載。

## 外部リンク

  - [MIPS Architectures](http://www.mips.com/products/architectures/) at [MIPS Technologies](../Page/ミップス・テクノロジーズ.md "wikilink")
  - [Full overview of MIPS architecture](http://www.langens.eu/tim/ea/mips_en.php)
  - [Patterson & Hennessy - Appendix A](http://www.cs.wisc.edu/~larus/HP_AppA.pdf)
  - [Summary of MIPS assembly language](http://logos.cs.uic.edu/366/notes/MIPS%20Quick%20Tutorial.htm)
  - [MIPS Instruction reference](http://www.mrc.uidaho.edu/mrc/people/jff/digital/MIPSir.html)
  - [MARS (MIPS Assembler and Runtime Simulator)](http://courses.missouristate.edu/KenVollmar/MARS/)
  - [MIPS processor images and descriptions at cpu-collection.de](http://www.cpu-collection.de/?tn=1&l0=cl&l1=MIPS%20Rx000)
  - [A programmed introduction to MIPS assembly](http://chortle.ccsu.edu/AssemblyTutorial/)
  - [Mips bitshift operators](http://www.cs.umd.edu/class/spring2003/cmsc311/Notes/Mips/bitshift.html)
  - [MIPS software user's manual](http://www.it.uu.se/edu/course/homepage/datsystDV/ht04/Project/tools/machinedata/4KcProgMan.pdf)
  - [MIPS Architecture history diagram](http://meld.org/library/education/mips-architectures)
  - [MIPS Open initiative](https://wavecomp.ai/mipsopen) \# 2018年12月17日(米国時間)にWave Computing社はMIPS Open(MIPS命令セットアーキテクチャ(ISA)のオープンソース化プログラム)を発表。

[Category:コンピュータアーキテクチャ](https://ja.wikipedia.org/wiki/Category:コンピュータアーキテクチャ "wikilink") [Category:MIPSのマイクロプロセッサ](https://ja.wikipedia.org/wiki/Category:MIPSのマイクロプロセッサ "wikilink") [Category:命令セットアーキテクチャ](https://ja.wikipedia.org/wiki/Category:命令セットアーキテクチャ "wikilink")

1.
2.
3.
4.
5.
6.
7.  MIPS社のR4000が登場する頃には、DEC社は自社製RISCマイクロプロセッサ[Alphaを完成させてこれに切り替えた](https://ja.wikipedia.org/wiki/DEC_Alpha "wikilink")。
8.
9.
10. Morgan Kaufmann Publishers, *Computer Organization and Design*, [David A. Patterson](../Page/デイビッド・パターソン_\(計算機科学者\).md "wikilink") & [John L. Hennessy](https://ja.wikipedia.org/wiki/ジョン・L・ヘネシー "wikilink"), Edition 3, ISBN 1-55860-604-1, page 63
11.
12.
13. R4000は、スーパーパイプラインを世界で最初に導入した市販のマイクロプロセッサである。しかし、これによって、"Microprocessor **with** Interlocked Pipeline Stages" パイプライン・ステージがインターロックされるマイクロプロセッサと揶揄されることになった。
14. 神保進一著、『マイクロプロセッサ テクノロジ』、日経BP社、1999年12月6日第1版第1刷発行、ISBN 4822209261
15. Jochen Liedtke(1995). On micro kernel construction. 15th Symposium on Operating Systems Principles, Copper Mountain Resort, Colorado.
16.
17. [CPUコアベンダからの脱却 - 変貌するMIPS Technologiesの実像を探る](https://news.mynavi.jp/articles/2009/03/05/mips_technologies/001.html)
18. <http://www.mdronline.com/mpr/h/2006/0626/202602.html> China's Microprocessor Dilemma
19. [China’s Institute of Computing Technology Licenses Industry-Standard MIPS Architectures](http://www.mips.com/news-events/newsroom/release-archive-2009/6_15_09.dot)
20.
21.  (*LinuxDevices*, Oct. 22, 2008)
22.
23. [Gwennap, Linley (18 November 1996). "Digital, MIPS Add Multimedia Extensions".](http://studies.ac.upc.edu/ETSETB/SEGPAR/microprocessors/mdmx%20\(mpr\).pdf) *Microprocessor Report*. pp. 24–28.
24.
25. [NEC Offers Two High Cost Performance 64-bit RISC Microprocessors](http://www.nec.co.jp/press/en/9801/2002.html)
26. [MIPS R3000 Instruction Set Summary](http://www.mrc.uidaho.edu/mrc/people/jff/digital/MIPSir.html)
27. [MIPS Instruction Reference](http://www.xs4all.nl/~vhouten/mipsel/r3000-isa.html)
28. [Welcome Page | Open Virtual Platforms](http://www.OVPworld.org)
29. [Welcome to Imperas | Imperas](http://www.imperas.com)
30.
31. [EduMIPS64](https://www.edumips.org)
32. [MARS MIPS simulator - Missouri State University](http://courses.missouristate.edu/KenVollmar/MARS/)
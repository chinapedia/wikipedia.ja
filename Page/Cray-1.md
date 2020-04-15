> この記事は[Cray-1](https://ja.wikipedia.org/wiki/Cray-1)から翻訳されています。


[thumbに保管されているCray](https://ja.wikipedia.org/wiki/ファイル:Cray-1-deutsches-museum.jpg "wikilink")-1\]\] [thumbのCray](https://ja.wikipedia.org/wiki/ファイル:Cray_1_IMG_9126.jpg "wikilink")-1\]\] **Cray-1**（クレイ ワン）は、[シーモア・クレイ](../Page/シーモア・クレイ.md "wikilink")率いる[クレイ](../Page/クレイ.md "wikilink")・リサーチ社が設計したベクトル型[スーパーコンピュータ](../Page/スーパーコンピュータ.md "wikilink")である。この種類のコンピュータの基本構成を確立し、当時世界最高速であった。最初のCray-1システムは[ロスアラモス国立研究所](../Page/ロスアラモス国立研究所.md "wikilink")に [1976年](../Page/1976年.md "wikilink")に納入された。Cray-1のアーキテクトは[シーモア・クレイ](../Page/シーモア・クレイ.md "wikilink")、主任技術者はクレイ・リサーチの共同創設者であるレスター・デーヴィスだった\[1\]。

## 歴史

1970年代初め、シーモア・クレイは[CDCで](../Page/コントロール・データ・コーポレーション.md "wikilink") [CDC 8600](../Page/CDC_8600.md "wikilink") という新しいマシンの開発に従事していた。8600はクレイがかつて設計した [CDC 6600](../Page/CDC_6600.md "wikilink") や [CDC 7600](../Page/CDC_7600.md "wikilink") の後継機である。8600は4台の7600をひとつの筐体に収めたもので、追加された特別なモードによって全体で[SIMD](../Page/SIMD.md "wikilink")的な動作をすることができるものであった。

クレイの初期設計のパートナーだったジム・ソーントンはさらに先進的な [CDC STAR-100](../Page/CDC_STAR-100.md "wikilink") と呼ばれるプロジェクトを開始した。8600の力ずくの性能向上手法とは異なり、STARは全く異なる方法を採用した。STARのメインプロセッサは7600よりも性能が悪かったが、科学技術計算の性能向上のための特別なハードウェアと命令を追加していた。

1972年に、開発中の8600はマシンがあまりにも複雑であったために、部品のどれかひとつが故障してもシステム全体が動作できなくなり、正常に動作させることができなかった。そこでクレイはCDC社長の[ウィリアム・ノリス](https://ja.wikipedia.org/wiki/ウィリアム・ノリス "wikilink")と会い、設計を最初からやり直す必要があることを告げた。しかし当時のCDCは深刻な財政的問題を抱えており、また並行するSTAR－100の開発もあったため、社長ノリスは8600へのこれ以上の追加投資ができないとして開発中止を決定した。

結果として、クレイはCDCを辞め、CDCの研究所のすぐ近くに新たな会社を設立した。に土地を購入し、彼とCDCの元従業員らはアイデアを探し始めた。当初、小規模なベンチャー企業にはスーパーコンピュータの構築は不可能と思われたが、クレイの[最高技術責任者](../Page/最高技術責任者.md "wikilink")が[ウォール街](../Page/ウォール街.md "wikilink")に行ってみると、多くの投資家がクレイへの出資に意欲を見せた。彼らに必要なのは設計だけであった。

1975年、クロック80MHzでピーク性能160MFLOPSのCray-1が発表された。反響は大きく、[ローレンスリバモア国立研究所](https://ja.wikipedia.org/wiki/ローレンスリバモア国立研究所 "wikilink")と[ロスアラモス国立研究所](../Page/ロスアラモス国立研究所.md "wikilink")が第一号機（SN-1）の争奪戦を繰り広げたほどである。結局、後者が勝ち、半年後の1976年に第一号機が納入された。クレイ・リサーチ社の公式の最初の顧客は[アメリカ大気研究センター](../Page/アメリカ大気研究センター.md "wikilink")（NCAR）であり、1977年7月に886万ドルを支払い（790万ドルが本体、100万ドルがディスクの代金である）、3号機を入手した。NCARのマシンは1989年1月まで使用された\[2\]。クレイ・リサーチ社は1ダースほどの販売を予定していたが、実際にはCray-1は80台以上販売されて、価格は500万から800万ドルであった。このマシンによってクレイは名士となり、会社は1990年代の凋落までは成功を収めたのである。

80MFLOPS(ピーク160MFLOPS)のCray-1の後継機は、1982年の800M[FLOPS](../Page/FLOPS.md "wikilink")の [Cray X-MP](../Page/Cray_X-MP.md "wikilink") である。これはクレイ社初のマルチプロセッサ機であり、X-MP/48 は Cray-1 の次の世界最高速のスーパーコンピュータとなった。1985年、後継機として革新的な[Cray-2](../Page/Cray-2.md "wikilink")が登場した。ピーク性能は 1.9GFLOPSであったが、商業的にはあまり成功しなかった。 その理由は、高い理論ピーク性能に比べて実際のアプリケーションを動作させたときの性能が（メモリバンド幅がネックとなり）十分には発揮できなかったからである。そのため、Cray-1や Cray X-MP を基にして拡張した [Cray Y-MP](../Page/Cray_Y-MP.md "wikilink") が1988年に投入されることになった。

## 背景

典型的な科学技術計算は大きなデータセットを読み込み、何らかの変換を加え、書き戻すというものである。通常、変換はデータセット内のデータそれぞれに等しく適用される。例えば、百万個の数値それぞれに 5 を加算するというようなプログラムが考えられる。一般的なコンピュータでは、百万回ループして個々の数値に5を加算していく。つまり、

`a = add b, c `

のような命令を百万個生成するようなものである。コンピュータ内部では、この命令を実行するためにいくつかの過程を踏む。まず、命令を読み込んで解読（デコード）する。次に必要な追加情報を集める。この命令の場合、数値 b と c を集めることになる。そして加算を実行して結果を格納する。

### ベクトル計算機

STARでは、新たな命令でループを表す。まず「数値の大きな列」がメモリのどこにあるのかをマシンに教え、ひとつの命令

`a(1..1000000) = addv b(1..1000000), c(1..1000000) `

を実行させる。一見してあまり変化がないようにも思われるが、この場合マシンは百万個ではなくひとつの命令を読み込んで解読すればよい。そのため全体の約4分の1の時間が節約される。

しかし実際の時間短縮はそれほどはっきりしていない。コンピュータの[CPU](../Page/CPU.md "wikilink")は、特定の仕事をするいくつかの部分から構成される。例えば加算を実行する部分やメモリを読み込む部分などである。命令を処理する場合、CPUの一部分だけが働いていて、命令処理はCPUの中の部分から部分へと流れていくのである。しかし、[命令パイプライン](https://ja.wikipedia.org/wiki/命令パイプライン "wikilink")の追加によってこれが変わった。CPUは先読みをして、前の命令を処理中に次の命令を読み込む。この流れ作業的手法では、ひとつの命令は時間がかかっているが、全体としてみれば命令が次々と処理されていくのである。

[ベクタープロセッサは](../Page/ベクトル計算機.md "wikilink")、これにあるトリックを追加して使用する。データの配置は分かっているので（メモリ上に順番に数値が並んでいる）、データ読み込み性能を上げるようにパイプラインを調整する。ベクトル命令を受け付けると、特別なハードウェアを指定された配列を読み込むように設定し、プロセッサに数値を次々と送り込むのである。

CDCがSTARで使用した手法は、今日では「メモリ・メモリ・アーキテクチャ」として知られている。これはデータを集める方法を意味していて、パイプラインは直接メモリを読み書きするように設定される。この場合、いかなる長さのベクトルでも使用可能で、非常に汎用的である。しかし、遅いメモリにアクセスしてもパイプラインが埋まるようにするために、パイプラインの段数が極めて長くないと性能が出せない。これは、ベクトル演算から通常の命令処理への切り替えに時間がかかることを意味する。さらに通常の命令処理の性能が悪いため、ベクトルからの切り替え時間との相乗効果で通常の命令処理は極めて性能が低下する。結果的に実際のアプリケーション性能は残念なものとなった。これは、設計者が[アムダールの法則](../Page/アムダールの法則.md "wikilink")を考慮していれば最初からわかったことかもしれない。

### クレイの手法

クレイはSTARの技術的失敗を見て学ぶことが出来た。彼はベクトル処理の高速化に加えて、一般のスカラー命令も高速化することを決断した。そうすれば、マシンのモードが切り替えられても高速に動作できる。さらに彼らはベクトルを格納するレジスタを導入することで性能を劇的に向上できることに気づいた。

初期のマシンは演算を行うたびにメモリ上のデータを頻繁に読み書きしていたため、無自覚にSTARでも同様にベクトル演算がベクトルの要素に演算を施すたびにメモリへ繰り返しアクセスするように実装してしまった。しかし、まとめてデータをベクトル用のレジスタに読み込んで、まとめて演算を施し、まとめて演算結果を書き込むならば性能はさらに向上する（まとめたことで、データ１語あたりのメモリへのアクセスレイテンシが減らせるほかに、パイプライン化された演算器のレイテンシも遮蔽できる）。回路としてはコストが高いレジスタは、無制限に実装するわけにはいかないので、クレイの設計ではベクトルレジスタ内部の要素数は64語に制限された。STARではベクトルは任意長でもよいがメモリアクセスが何度も発生するのに対して、クレイの設計したマシンでは長いベクトルデータに対してはその一部（64語以内の）だけをまとめて読み込む。しかし、そのひとかたまりに対して要素ごとに同じ演算処理をまとめて実行できるのである。一般的な処理においてより長いベクトルを扱う場合にはそれを64語ずつに区切ってメモリアクセスを何回かに分けても性能向上を期待できるとクレイは考えた。

一般的なベクトル処理は小さなデータのかたまりをベクターレジスタに読み込んで、それに対していくつかの演算を行うが、この新しいベクトルシステムは独立した演算パイプラインを持つよう設計され、乗算器と加算器は独立したハードウェアとして実装されたので、内部でふたつの演算処理をつないで、例えば加算の結果を次の乗算で使用することがパイプライン上でできた。これをクレイでは *chaining* （チェイニング）と呼び、これをプログラマが意識して用いることで複数の命令をつないで使うことでベクトルレジスタとメモリの間の読み書きを減らすことにより高い性能を引き出すことができた。

## 詳細

Cray-1はクレイにとって初めて[集積回路](../Page/集積回路.md "wikilink")(IC)を使ったマシンである。ICは1960年代から実用化されていたが、1970年代に入ってから高速性を要求される用途にも使えるものになったのである。Cray-1で使用しているICは、[ECLによる](../Page/エミッタ結合論理.md "wikilink")[NANDゲート](https://ja.wikipedia.org/wiki/NANDゲート "wikilink")2個（1つは5入力、もう1つは4入力）を実装したもの\[3\]、アドレス出力に使用するやや低速なMECLによるNANDゲートIC、レジスタ用の高速小容量（6ns, 16×4ビット）[SRAM](../Page/Static_Random_Access_Memory.md "wikilink")、主記憶用の1024×1ビットのSRAM（50ns）の4種類だけだった\[4\]。それらのICは[フェアチャイルドセミコンダクター](../Page/フェアチャイルドセミコンダクター.md "wikilink")および[モトローラ](../Page/モトローラ.md "wikilink")製である。Cray-1は全体で約20万ゲートで構成されている。

ICは5層の[プリント基板](../Page/プリント基板.md "wikilink")上に実装され、基板1枚に最大144個のICが搭載されている。基板は冷却のために背中合わせに実装され、24台の28インチ高のラックに72組の背中合わせの基板がセットされた。モジュール（個別の演算ユニット）は1枚か2枚の基板で構成される。マシン全体では113種類、1,662モジュールが使われている。

モジュール間のケーブルは[ツイストペアケーブル](../Page/ツイストペアケーブル.md "wikilink")とし、長さも緻密に計算して[パルスの反射を低減し](https://ja.wikipedia.org/wiki/反射#電流の反射 "wikilink")、[定常波による誤動作が起きないようにした](https://ja.wikipedia.org/wiki/定常波#反射波による定常波 "wikilink")。ECL回路の生成する信号は差動形であり、[2つの信号が均衡を保つようになっている](../Page/平衡接続.md "wikilink")。したがって消費電力はさらに一定となり、電圧変動が低減される。電源から見ればコンピュータシステム全体が単純な抵抗器のように見える。

[ECL回路は高速であり](../Page/エミッタ結合論理.md "wikilink")、全体として発熱が非常に大きかった。クレイの設計者は多くの時間を冷却システムに費やした。このために2枚の基板の間に銅板を挟んで背中合わせにした。銅板は熱をケースの端へ送り出すので、そこに[フロンの通るパイプを設置して熱を交換し](../Page/フロン類.md "wikilink")、筐体下部の冷却装置でフロンを冷却した。最初のCray-1の完成が6カ月遅れたのは、この冷却機構に問題が生じたためである。コンプレッサのためにフロンに混ぜられていた潤滑剤が漏れて、回路がショートしてしまったのである。パイプの溶接に新たな技術を導入して漏れを防いだ。Cray-1について出願された特許は冷却システムの設計に関するものだけだった。

配線の長さを少しでも短くするため、筐体は "C" のような形に配置された。速度に影響するものはその形の内側の端に置かれ、配線の長さを少しでも短くした。これによりサイクル時間は12.5ns（80MHz）まで短縮された。彼があきらめた8600の8nsよりも長いが、[CDC 7600](../Page/CDC_7600.md "wikilink") やSTARよりずっと高速である。NCARはシステムのスループット計測結果を概算で CDC 7600 の4.5倍と推定した。

Cray-1は[64ビット](https://ja.wikipedia.org/wiki/64ビット "wikilink")システムであり、7600/6600の60ビットとは異なる（8600でも同様の変更がなされる予定だった）。アドレスは[24ビット](https://ja.wikipedia.org/wiki/24ビット "wikilink")であり、最大で1,048,571の64ビットワード（1Mワード）の主記憶を扱える。各ワードには8ビットのパリティビットが付属し、1ワードは実際には72ビットとなっている\[5\]。[メモリインターリーブ](https://ja.wikipedia.org/wiki/メモリインターリーブ "wikilink")により16バンクに分割され、それぞれ50nsのサイクル時間であり、1サイクルで4ワードを読み込むことができる。より小さい構成では、主記憶を0.25Mワードあるいは0.5Mワードとすることも可能である。

メインレジスタセットは 8本の64ビット・スカラー(S)レジスタと8本の24ビット・アドレス(A)レジスタから構成される。これらレジスタを一時退避するそれぞれ64本のレジスタ（T および B と呼ばれた）があり、こちらは演算ユニットからは見えない。ベクトル機構には別に 64本の64ビット・ベクター(V)レジスタとベクター長(VL)レジスタ、ベクターマスク(VM)レジスタがある。そして、64ビットのリアルタイムクロック・レジスタと4本の64ビット命令バッファがあり、各命令バッファには[16ビット](../Page/16ビット.md "wikilink")の命令が4つ格納される。ハードウェアは1サイクル毎に1ワード分をベクターレジスタに供給し、アドレスおよびスカラーレジスタには1サイクル毎に2ワード分を供給する。一方、16ワードの命令バッファ全体を4サイクルで満たすことができる。

システムは12個のパイプライン型機能ユニットがある。24ビットのアドレス演算に加算ユニット1つと乗算ユニット1つを使用する。システムのスカラー部には加算ユニット、論理演算ユニット、[ハミング重み](https://ja.wikipedia.org/wiki/ハミング重み "wikilink")計算ユニット、前置ゼロ計数ユニット、シフト演算ユニットがある。ベクター部には、加算ユニット、論理演算ユニット、シフト演算ユニットがある。浮動小数点演算ユニット群はスカラー部とベクター部で共有しており、加算ユニット、乗算ユニット、逆数近似ユニットからなる。

システムは12個の機能ユニットがあるが、並列性には制限がある。1サイクルに1命令がユニットにフェッチされるが、実行は並列に行われ、1サイクル毎に最大で2個の命令が完了する。理論上の性能は160MIPS（80MHz×2命令）だが、制限により実際の[浮動小数点演算性能は](../Page/浮動小数点数.md "wikilink")136MFLOPSである。しかし、ベクター命令を注意深く使用してchainを作るようにすれば最高で250MFLOPSの性能を出すことができる。

Cray-1は大きなデータセットを処理するよう設計されているため、[I/O回路の設計にも時間がかけられた](../Page/入出力.md "wikilink")。クレイがCDCで設計したものにはI/O専用のコンピュータが含まれていたが、それは必要とされなかった。代わりにCray-1は4台の6[チャネル・コントローラ](../Page/チャネル・コントローラ.md "wikilink")を持ち、各コントローラが4サイクルに1回メモリにアクセスできるようにした。チャネルは16ビット幅で、制御ビットとして3ビット、エラー訂正用に4ビットを使用する。最大転送速度は100nsに1ワードであり、マシン全体では500Kワード/sとなる。

最初のモデル**Cray-1A**は、フロン冷却システムを含めて重量5.5[トン](../Page/トン.md "wikilink")であった。RAMを100万ワード搭載した場合、消費電力は115kWであった。冷却システムと外部記憶装置を入れるとその倍の電力消費となる。保守用のフロントエンドとして[データゼネラル](../Page/データゼネラル.md "wikilink")社の[SuperNova S/200が使われた](https://ja.wikipedia.org/wiki/Nova_\(コンピュータ\) "wikilink")。これを使って起動時に[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink")を本体に送り込み、動作中のCPUを監視し、オプションとして操作用としても使用した。これは後に[Eclipseに置き換えられた](../Page/Eclipse_\(コンピュータ\).md "wikilink")。

## Cray-1S

次のモデル**Cray-1S**（1979年）は、クロック周波数が若干上がって12.0nsとなり、メインメモリは100万/200万/400万ワードである。主記憶の大容量化は、25nsのアクセス時間で動作する4096ビットのバイポーラRAM集積回路によって実現できた\[6\]。データゼネラルのマシンは独自の16ビットマシン（80MIPS）に置き換えられた。I/Oシステムはメインのマシンとは分離され、6MB/sの制御チャネルと100MB/sの高速データ転送チャネルで接続された。この分離によって1Sの外観はCray-1Aをふたつに分けて少し離したように見えた。これによりI/Oシステムは必要に応じて拡張できるようになった。システムはいくつかの構成から選ぶことができた。S/500はI/O無しで0.5Mワードメモリであり、S/4400は4Mワードメモリで4台のI/Oプロセッサを持つ。

## Cray-1M

Cray-1S の次には**Cray-1M**（1982年）が登場した\[7\]。"M"は低価格な[MOS](https://ja.wikipedia.org/wiki/MOS "wikilink")ベースのRAMをI/Oシステムに使用していることを表す。1Mは3つのバージョンがあり、メインメモリの容量だけで分けられている。M/1200は 1Mワード（8バンク）、M/2200 は2Mワード（16バンク）、M/4200は4Mワード（16バンク）である。いずれもI/Oプロセッサは2～4台であり、高速データチャネルがもうひとつ追加された。ユーザはMOSベースのRAMを8から32Mワード分追加して[ソリッドステートドライブ](../Page/ソリッドステートドライブ.md "wikilink")として使用することができた。

## ソフトウェア

[1978年](https://ja.wikipedia.org/wiki/1978年 "wikilink")、Cray-1リリース時の最初のソフトウェアは以下の3製品から構成されていた。

  - Cray Operating System (COS)。Cray-1と[Cray X-MPで使用された](../Page/Cray_X-MP.md "wikilink")[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink")。1984年に[UNIX](../Page/UNIX.md "wikilink")系統の[UNICOS](https://ja.wikipedia.org/wiki/UNICOS "wikilink")に置き換えられた。
  - Cray Assembler Language (CAL)
  - Cray FORTRAN (CFT)。最初の自動ベクトル化[FORTRAN](../Page/FORTRAN.md "wikilink")コンパイラ

[アメリカ合衆国エネルギー省](../Page/アメリカ合衆国エネルギー省.md "wikilink")が出資している[ローレンス・リバモア国立研究所](../Page/ローレンス・リバモア国立研究所.md "wikilink")、[ロスアラモス国立研究所](../Page/ロスアラモス国立研究所.md "wikilink")、[サンディア国立研究所](../Page/サンディア国立研究所.md "wikilink")、[アメリカ国立科学財団](../Page/アメリカ国立科学財団.md "wikilink")の[スーパーコンピュータ](../Page/スーパーコンピュータ.md "wikilink")センター（高エネルギー物理学向け）は、ローレンス・リバモア国立研究所が開発した  (CTSS) を採用している。CTSSはもともと Livermore Time Sharing System として [CDC 7600](../Page/CDC_7600.md "wikilink") 向けに開発されたもので、LRLTRANという[FORTRAN](../Page/FORTRAN.md "wikilink")が動作していた。CTSSではCray-1向けにベクトル処理対応を加えた CVC というFORTRANが動作する。

NCARは独自のオペレーティングシステム NCAROS を開発した。

[アメリカ国家安全保障局](../Page/アメリカ国家安全保障局.md "wikilink")も独自のOSとプログラミング言語を開発したが、詳しいことは不明である。

クレイ・リサーチが提供したライブラリは、後の[Netlib](https://ja.wikipedia.org/wiki/Netlib "wikilink")の一部となった。

他にもOSが開発されているが、プログラミング言語の多くはFORTRAN系である。[ベル研究所](../Page/ベル研究所.md "wikilink")では試験的に[C言語](../Page/C言語.md "wikilink")コンパイラを開発した（ベクトル非対応）。このおかげで、クレイ・リサーチは[ETAシステムズ](../Page/ETAシステムズ.md "wikilink")より6カ月先行して [Cray-2](../Page/Cray-2.md "wikilink") 向けUNIXを完成させることができ、[ルーカスフィルム](../Page/ルーカスフィルム.md "wikilink")は初のCGI試験フィルム *The Adventures of André and Wally B.* の制作に Cray-1 用C言語を利用した。

アプリケーションの多くは機密（核開発用、暗号解読用など）あるいは[プロプライエタリ](https://ja.wikipedia.org/wiki/プロプライエタリ "wikilink")（石油貯蔵施設のモデリングなど）である。大学の顧客が少なく、顧客間でアプリケーションソフトウェアを共有することがほとんどなかったためである。数少ない例外として、気象や気候に関するプログラムがある。

## 日本における導入実績

日本では[1980年](https://ja.wikipedia.org/wiki/1980年 "wikilink")1月にCray-1の日本第1号機が[センチュリ リサーチ センタの東京本社に](https://ja.wikipedia.org/wiki/CRCソリューションズ "wikilink")\[8\]、同年7月に第2号機が[三菱総合研究所](../Page/三菱総合研究所.md "wikilink")に設置された\[9\]。

## 博物館

Cray-1は以下のような場所で展示されている。

  - Bradbury Science Museum（[ロスアラモス国立研究所](../Page/ロスアラモス国立研究所.md "wikilink")内）
  - [コンピュータ歴史博物館](https://ja.wikipedia.org/wiki/コンピュータ歴史博物館 "wikilink")（[マウンテンビュー](../Page/マウンテンビュー.md "wikilink")）
  - [DigiBarn Computer Museum](https://ja.wikipedia.org/wiki/:en:DigiBarn_Computer_Museum "wikilink")
  - [ドイツ博物館](../Page/ドイツ博物館.md "wikilink")（[ミュンヘン](../Page/ミュンヘン.md "wikilink")）
  - [アメリカ大気研究センター](../Page/アメリカ大気研究センター.md "wikilink")（[ボルダー](../Page/ボルダー_\(コロラド州\).md "wikilink")）
  - [サイエンス・ミュージアム](../Page/サイエンス・ミュージアム.md "wikilink")（[ロンドン](../Page/ロンドン.md "wikilink")）
  - [国立航空宇宙博物館](../Page/国立航空宇宙博物館.md "wikilink")（[ワシントンD.C.](../Page/ワシントンD.C..md "wikilink")）\[10\]
  - Chippewa Falls Museum of Industry and Technology（[ウィスコンシン州](../Page/ウィスコンシン州.md "wikilink")チッペワフォールズ）
  - [スイス連邦工科大学ローザンヌ校](../Page/スイス連邦工科大学ローザンヌ校.md "wikilink")（[スイス](../Page/スイス.md "wikilink")、[ローザンヌ](../Page/ローザンヌ.md "wikilink")）
  - （[アメリカ国立暗号博物館](https://ja.wikipedia.org/wiki/アメリカ国立暗号博物館 "wikilink")内）

## Cray-1の画像

[File:Cray-1-p1010225.jpg|回路基板群](File:Cray-1-p1010225.jpg%7C回路基板群) [File:Cray-1-p1010227.jpg|タワー内部](File:Cray-1-p1010227.jpg%7Cタワー内部) [File:Cray-1-p1010237.jpg|冷却機構](File:Cray-1-p1010237.jpg%7C冷却機構) [File:Cray-1-p1010230.jpg|筐体上部](File:Cray-1-p1010230.jpg%7C筐体上部) [File:Cray-1-p1010233.jpg|回路基板のクローズアップ](File:Cray-1-p1010233.jpg%7C回路基板のクローズアップ) [File:Cray-1A-A1621b.jpg|Cray-1A](File:Cray-1A-A1621b.jpg%7CCray-1A) の電源部 <File:Cray-1> (1).jpg|Cray-1（[コンピュータ歴史博物館](https://ja.wikipedia.org/wiki/コンピュータ歴史博物館 "wikilink")） <File:Cray-1-Computer> History Museum-20070512.jpg|Cray-1（[コンピュータ歴史博物館](https://ja.wikipedia.org/wiki/コンピュータ歴史博物館 "wikilink")） <File:CRAY> X-MP IMG 9135.jpg|Cray-XMP48（[スイス連邦工科大学ローザンヌ校](../Page/スイス連邦工科大学ローザンヌ校.md "wikilink")）

## 脚注・出典

## 外部リンク

  - [*CRAY-1 Computer System Hardware Reference Manual*, Publication No. 2240004 Rev.C 11/77 (first three chapters)（英語）](http://ed-thelen.org/comp-hist/CRAY-1-HardRefMan/CRAY-1-HRM.html) – From [DigiBarn（英語）](http://www.digibarn.org) / Ed Thelen
  - [*CRAY-1 Computer System Hardware Reference Manual*, Publication No. 2240004 Rev.C 11/77 (full, scanned, PDF)](http://bitsavers.trailing-edge.com/pdf/cray/2240004C-1977-Cray1.pdf)
  - [Cray Channels Magazine @ The Centre for Computing History](http://www.computinghistory.org.uk/sec/3017/Cray-Channels/)
  - [Cray Manuals & Documentation @ The Centre for Computing History](http://www.computinghistory.org.uk/sec/2257/Cray-Computer-Manuals/)
  - [Cray Users Group Publications @ The Centre for Computing History](http://www.computinghistory.org.uk/sec/2459/Cray-Users-Group/)
  - [NCAR Supercomputer Gallery](http://cisl.ucar.edu/computers/gallery/index.jsp)
  - [Collection of on-line Cray manuals & documentation @ Bitsavers](http://bitsavers.org/pdf/cray/)
  - [Verilog definition of Cray-1A CPU logic](http://chrisfenton.com/wp-content/uploads/2010/08/cray1_r2.zip)

[Category:スーパーコンピュータ](https://ja.wikipedia.org/wiki/Category:スーパーコンピュータ "wikilink") [Category:クレイのハードウェア](https://ja.wikipedia.org/wiki/Category:クレイのハードウェア "wikilink") [Category:コンピュータ史](https://ja.wikipedia.org/wiki/Category:コンピュータ史 "wikilink")

1.  C.J. Murray, ["The ultimate team player,"](http://www.designnews.com/article/14035-The_ultimate_team_player.php) *[Design News](https://ja.wikipedia.org/wiki/:en:Design_News "wikilink")*, 6 Mar. 1995.
2.
3.  Fairchild Semiconductor, ["Fairchild 11C01 ECL Dual 5-4 Input OR/NOR Gate,"](http://doc.chipfind.ru/fairchild/11c01.htm) Fairchild ECL Databook, c1972.
4.  R.M. Russell, "The CRAY-1 Computer System," *[Comm. ACM](https://ja.wikipedia.org/wiki/:en:Communications_of_the_ACM "wikilink")*, Jan. 1978, pp. 63–72.
5.
6.  J.S. Kolodzey, "CRAY-1 Computer Technology," *IEEE Trans. Components, Hybrids, and Manufacturing Technology*, vol. 4, no. 3, 1981, pp. 181–186.
7.  ["Cray Cuts Price,"](http://www.nytimes.com/1982/09/14/business/cray-cuts-price.html) *[The New York Times](../Page/ニューヨーク・タイムズ.md "wikilink")*, 14 Sep. 1982.
8.  「センチュリリサーチセンタ、わが国で初めてスーパーコンピューター導入。」『日経産業新聞』 1980年1月21日、4面。
9.  「三菱総研、米のスーパーコンピューター「CRAY-1」の設置完了。」「日経産業新聞」 1980年7月10日、4面。
10.
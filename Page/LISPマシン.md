> この記事は[LISPマシン](https://ja.wikipedia.org/wiki/LISPマシン)から翻訳されています。


**LISPマシン**は、[LISP](https://ja.wikipedia.org/wiki/LISP "wikilink")を主要な[プログラミング言語](../Page/プログラミング言語.md "wikilink")として効率的に実行することを目的として設計された汎用の[コンピュータ](../Page/コンピュータ.md "wikilink")である。ある意味では、最初の商用シングルユーザー[ワークステーション](../Page/ワークステーション.md "wikilink")と言うこともできる。それほど数量的に大成功を収めたとはいえないが（1988年までに約7000台が出荷された\[1\]）、その後よく使われることになる様々な技術を商用化する先駆けとなった。例えば、効率的[ガベージコレクション](../Page/ガベージコレクション.md "wikilink")、[レーザープリンター](../Page/レーザープリンター.md "wikilink")、[ウィンドウシステム](../Page/ウィンドウシステム.md "wikilink")、[コンピュータマウス](../Page/マウス_\(コンピュータ\).md "wikilink")、高解像度[ビットマップグラフィックス](../Page/ビットマップ画像.md "wikilink")、などのネットワーキングにおける技術革新などである。1980年代に[シンボリックス](../Page/シンボリックス.md "wikilink")（3600、3640、XL1200、MacIvoryなど）、LMI（[Lisp Machines Incorporated](https://ja.wikipedia.org/wiki/:en:Lisp_Machines "wikilink")、LMI Lambda）、[テキサス・インスツルメンツ](../Page/テキサス・インスツルメンツ.md "wikilink")（[Explorer](https://ja.wikipedia.org/wiki/:en:TI_Explorer "wikilink")、MicroExplorer）、[ゼロックス](../Page/ゼロックス.md "wikilink")（[InterLisp-D搭載ワークステーション](../Page/Interlisp.md "wikilink")）といった企業がLISPマシンを製造販売した。[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink")は  や[Interlisp](../Page/Interlisp.md "wikilink")（ゼロックスの場合）で書かれ、後に一部は [Common Lisp](../Page/Common_Lisp.md "wikilink") で書かれた。

## 歴史

### 背景

1960年代から1970年代にかけて、[人工知能](../Page/人工知能.md "wikilink")[プログラムは当時の基準では非常に多くのプロセッサ時間とメモリ空間を消費するものだった](../Page/プログラム_\(コンピュータ\).md "wikilink")。当時の研究機関で使われていたコンピュータは高価であるために多くのユーザーが共有して使用するのが一般的だった。1960年代から1970年代にかけての[集積回路](../Page/集積回路.md "wikilink")技術の進展は[コンピュータ](../Page/コンピュータ.md "wikilink")のサイズとコストを小さくしていったが、AIプログラムが使用するメモリ量は一般的な当時の研究用コンピュータ（[DECの](https://ja.wikipedia.org/wiki/デジタル・イクイップメント・コーポレーション "wikilink")[PDP-10](../Page/PDP-10.md "wikilink")）のアドレス空間を越えようとしていた。研究者たちは、巨大な[人工知能](../Page/人工知能.md "wikilink")プログラムを開発し動作させるのに最適化した新しいコンピュータを設計することを検討し始め、[LISP](https://ja.wikipedia.org/wiki/LISP "wikilink")[プログラミング言語](../Page/プログラミング言語.md "wikilink")の実行に最適化されたマシンを作った。その[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink")を単純にするために、LISPマシンはシングルユーザー用のマシンとなった。

### 初期の開発

[thumb](https://ja.wikipedia.org/wiki/ファイル:LISP_machine.jpg "wikilink") [1973年](../Page/1973年.md "wikilink")、[MIT](../Page/マサチューセッツ工科大学.md "wikilink") [AI研究所のプログラマ](../Page/MIT人工知能研究所.md "wikilink")、[リチャード・グリーンブラット](https://ja.wikipedia.org/wiki/リチャード・グリーンブラット "wikilink")とは MIT LISPマシンプロジェクトを立ち上げた。これは、基本的なLISPの機能がハード的に動作するコンピュータを構築するもので、24ビットのタグ付きアーキテクチャを採用していた。また、このマシンはインクリメンタルな[ガベージコレクション](../Page/ガベージコレクション.md "wikilink")を採用していた。LISPの変数はコンパイル時ではなく実行時に型付けされるので、普通のハードウェアでは2つの変数の加算に通常の5倍の時間がかかる（型チェックと型ごとの分岐のため）。LISPマシンでは通常の加算命令で型チェックを同時に行う。型チェックが失敗した場合、並行して行っていた加算結果を捨て、再計算する。従って、多くの場合、単純な加算だけで済むので高速化される。このようなチェックを並行して行う手法は、配列の境界チェックなどのメモリ管理関連でも行われている。

Symbolics 3600シリーズでは、32ビットワードを36ビットワードに拡張することで型チェックがさらに強化・自動化された\[2\]。これは後にさらに40ビットワード以上に強化されている（型チェックが関係しない場合、余分なビットは[誤り検出訂正](../Page/誤り検出訂正.md "wikilink")に使われた）。追加ビットの一部はデータ型を保持するのに使われ（タグ付きアーキテクチャ）、その他は（リストに要するメモリを約半分にする方式）の実装や[ガベージコレクション](../Page/ガベージコレクション.md "wikilink")に使われた。さらなる改善として、2つのマイクロコード命令でLISPの関数呼び出しをサポートし、（一部のシンボリックスの実装では）関数呼び出し当たりのコストを20クロックサイクルに削減している。

最初のマシンは CONS（LISPのリスト作成演算子にちなんだ名称）と呼ばれた。CONSはトム・ナイトが修士論文のテーマとしたことから「ナイト・マシン」とも呼ばれた。その後、さらに改良された CADR（LISPの `cadr` 関数 = CAR + CDR に由来）と呼ばれるバージョンが完成した。アーキテクチャは基本的には同じである。25台の CADR マシンがMIT内外に約5万ドルで販売された。[ハッカー](../Page/ハッカー.md "wikilink")の間で人気となり、すぐさま各種ツールが移植されていった（例えば、[Emacs](../Page/Emacs.md "wikilink") は 1975年に [ITS](../Page/Incompatible_Timesharing_System.md "wikilink") から移植された）。1978年にMITで開催されたAI会議で好評を博し、[DARPAはその開発に資金提供を開始した](../Page/国防高等研究計画局.md "wikilink")。

### 派生

1979年、（AI研究所の管理者、後にシンボリックス社を創業）はLISPマシンが商業的にも将来性があると確信し、グリーンブラットにその技術の商業化の提案書を書かせた。根っからのハッカーであったグリーンブラットにとって商業化はポリシーに反することではあったが、AI研究所の雰囲気をそのまま持ち込んだような会社が作れるのではないかと考え、反対はしなかった。しかし、ノフツカーの考えはそれとは全く違っていた。両者は長時間にわたって話し合ったが、合意には至らなかった。AI研究所のハッカー達の全面的な支援がなければこの事業が成り立たないのは明らかであったため、ノフツカーを選ぶかグリーンブラットを選ぶかはハッカー達自身に任されることになった。

その後の議論により、研究所は2つの派閥に分裂する事態となった。1979年2月、大多数のハッカーはグリーンブラットの自己満足的な企業よりもノフツカーの考える企業の方が将来性があると判断した。グリーンブラットは負けたのである。

ノフツカーの企業[シンボリックス](../Page/シンボリックス.md "wikilink")社が徐々に形を成し（彼は給料を払っていたが、作業のための建物も設備も無かった。そのため、ハッカー達がMITでシンボリックスのための作業を続ける代わりに、その成果をMIT内部には無償で提供するという約束をしていた）、グリーンブラットが消沈していたころ、[CDCのコンサルタントがグリーンブラットを訪ねてきた](../Page/コントロール・データ・コーポレーション.md "wikilink")。CDC は自然言語処理アプリケーションを西海岸のハッカー達と開発しようとしており、それにグリーンブラットのLISPマシンが使えないかとやってきたのであった。ノフツカーと決着のついた話し合いから8ヶ月後のことであった。グリーンブラットはノフツカーに対抗するLISPマシン企業を始めると決めていたが、具体的には何もしていなかった。そのコンサルタント、アレキサンダー・ジェイコブソンはグリーンブラットが会社を興すのを助けることを決め、経営計画などをまとめた。この新たな企業は [LMI](https://ja.wikipedia.org/wiki/LMI "wikilink")（Lisp Machine, Inc.）と名づけられ、ジェイコブソン経由で CDC の資本で設立された。

このころ、シンボリックス社が事業を開始した。ノフツカーがグリーンブラットに対して一年間の猶予を与えると約束したことと、ベンチャーキャピタルからの資金集めが難航したための遅れであった。しかし、AI研究所のハッカー達のうち3、4人はグリーンブラットについたものの、他の14人のハッカーがシンボリックスで働くことになったことで、シンボリックスにとっては有利となった。ただし、[リチャード・ストールマン](../Page/リチャード・ストールマン.md "wikilink")と[マービン・ミンスキー](../Page/マービン・ミンスキー.md "wikilink")の2人はどちらにも与しなかった。ただし、ストールマンはAI研究所を中心としたハッカー文化を衰退させたとしてシンボリックスを非難している。1982年から1983年末までの2年間、ストールマンはシンボリックスのプログラマ達の成果のクローンを作る作業を行い、研究所のコンピュータ群においてシンボリックスが独占状態となるのを防ごうとした\[3\]。

シンボリックスは1980年から1981年にかけて CADR を LM-2 として販売開始し、LMI も LMI-CADR として販売開始した。シンボリックスは新たに開発していた3600ファミリをなるべく早く出荷し、LM-2 の販売を早々にやめる予定だったが、3600の開発は遅れに遅れ、結局7万ドルの LM-2 は約100台出荷された。両社は CADR ベースの第二世代の製品 Symbolics 3600 と LMI-LAMBDA を開発した。約1年後にリリースされた 3600 は、CADR のワード長を 36ビットに拡張して、アドレス空間を 28ビットとし\[4\]、CADR ではマイクロコードで実装されていた機能の一部をハードウェアで実装し高速化したものであった。さらにその1年後（1983年）に登場した LMI-LAMBDA はマイクロコードレベルで CADR と互換性があるが、ハードウェアには差異がある。[テキサス・インスツルメンツ](../Page/テキサス・インスツルメンツ.md "wikilink")(TI)社は、LMI-LAMBDA のライセンス供与を受け、互換マシン TI Explorer を開発した。LMI-LAMBDA と TI Explorer の一部はLISPマシンと[UNIX](../Page/UNIX.md "wikilink")マシンを1つにまとめたデュアルシステムとなっていた。TIはExplorer用にLISPマシンCPUの32ビット[マイクロプロセッサ](../Page/マイクロプロセッサ.md "wikilink")も開発した。このチップは[アップルの](../Page/アップル_\(企業\).md "wikilink") Macintosh II に接続できるNuBusボード型の MicroExplorer にも使われた。

シンボリックス社は 3600 ファミリとそのオペレーティングシステム Genera を開発し続け、シンボリックスのCPUをワンチップ化した Ivory も開発した。1987年には Ivory を使ったいくつかのマシンも開発された。例えば、SunのワークステーションやMac向けの拡張ボード、スタンドアロンのワークステーション、そして組み込みシステムなどにまで利用された。LMI社は CADR アーキテクチャをやめて新たに K-Machine を開発したが\[5\]、リリースする前に倒産した。倒産直前のLMIでは、巨大仮想空間を複数マシン間で共有する分散システムを検討していた\[6\]。

これらのマシンは様々な、コンパイルされたLISPプログラムに必要なプリミティブ的な操作をハードウェアでサポートしており、データ型チェック、CDRコーディング（リスト型のデータ構造を配列的に詰めたもの）、並列and・or並行ガベージコレクションのハードウェアサポートなどがある。これにより、大きなLISPプログラムを非常に効率的に動作させることができた。シンボリックス社のマシンは商用のスーパーミニコンピュータ（[VAX](../Page/VAX.md "wikilink")など）と競合したが、人工知能研究以外の用途に使われることはほとんどなかった。一部の例外的な用途として、シンボリックスのLISPマシンは[コンピュータグラフィックス](../Page/コンピュータグラフィックス.md "wikilink")のモデリングやアニメーションにおけるアルゴリズム研究に用いられた例もある。

MITから派生したLISPマシンは、MITの[MacLisp](https://ja.wikipedia.org/wiki/MacLisp "wikilink")を先祖とする  という方言を主要言語としていた。オペレーティングシステムもLISPで書かれていて、オブジェクト指向による拡張も使われていた。後にLISPマシンは [Common Lisp](../Page/Common_Lisp.md "wikilink")（と[Flavors](https://ja.wikipedia.org/wiki/Flavors "wikilink")や[CLOS](../Page/Common_Lisp_Object_System.md "wikilink")）をサポートするようになった。

### ゼロックスのLISPマシン

[BBNは](../Page/BBNテクノロジーズ.md "wikilink")、独自のLISPマシン Jericho を開発した\[7\]。[InterLisp](https://ja.wikipedia.org/wiki/InterLisp "wikilink")が動作するマシンであったが、市場には出されなかった。それに失望したAIグループのメンバーは同社を辞め、その多くが[ゼロックス](../Page/ゼロックス.md "wikilink")の[パロアルト研究所](../Page/パロアルト研究所.md "wikilink")に雇われることになった。従って、[ゼロックス](../Page/ゼロックス.md "wikilink")社の[パロアルト研究所](../Page/パロアルト研究所.md "wikilink")が開発した [Interlisp](../Page/Interlisp.md "wikilink")（後に[Common Lispも稼動](../Page/Common_Lisp.md "wikilink")）や[Smalltalk](../Page/Smalltalk.md "wikilink")のような言語が動作するよう設計されたマシンは、グリーンブラットらのMITでの開発とは独立している。しかし、ゼロックスは市場参入の時期を誤り、LMI やシンボリックスの後塵を拝することになった。Xerox 1100（ドルフィン）、Xerox 1132（ドラド）、Xerox 1108（ダンデライオン）、Xerox 1109（ダンデタイガー）、Xerox 6085（デイブレイク）などの機種がある。ゼロックスのLISPマシンのオペレーティングシステムは仮想マシンに移植され、[Medley](https://ja.wikipedia.org/wiki/Medley "wikilink")という名前でいくつかのプラットフォーム上で動作した。ゼロックスのLISPマシンは先進的な開発環境で知られており、[Alto](../Page/Alto.md "wikilink")から受け継がれたGUIと[NoteCards](../Page/NoteCards.md "wikilink")（初期の[ハイパーテキスト](../Page/ハイパーテキスト.md "wikilink")アプリケーション）などが有名である。ゼロックスのマシンは商業的には失敗だったが、そのグラフィカルユーザー環境や一部の概念は後にアップルの[Macintosh](../Page/Macintosh.md "wikilink")等さまざまなコンピュータに間接的に影響を与えた。

ゼロックスは[RISC](../Page/RISC.md "wikilink")ベースのLISPマシン Xerox Common Lisp Processor を試作し、1987年に市販することを計画していたが\[8\]、実現しなかった。

### Integrated Inference Machines

1980年代中ごろ、Integrated Inference Machines (IIM) がLISPマシンの試作機 Inferstar を開発している\[9\]。

### アメリカ以外でのLISPマシン開発

1984年から1985年にかけて、イギリスの Racal-Norsk はノルウェーの Norsk Data のミニコンのマイクロプログラムをLISPマシン化して CADR 用のソフトウェア Knowledge Processing System (KPS) を動作させることを試みている\[10\]。

フランスでは2つのLISPマシン・プロジェクト、M3L\[11\]とMAIA\[12\]が実施されている。

ドイツではシーメンスがRISCベースのLISP用コプロセッサCOLIBRIを開発している\[13\]\[14\]。

### 日本でのLISPマシン開発

日本では、1979年に完動した神戸大のTAKITAC-7（FAST LISP）\[15\]をはじめ、理化学研究所のFLATS\[16\]、大阪大学のELVIS\[17\]などが試作された。[富士通](../Page/富士通.md "wikilink")の[FACOM α](https://ja.wikipedia.org/wiki/FACOM_α "wikilink")（メインフレームのバックエンドとして動作。1984年発表）\[18\]、[NTT電気通信研究所のELIS](../Page/日本電信電話.md "wikilink")（TAO/ELIS\[19\]）\[20\]\[21\]、東芝のAIプロセッサ(AIP)\[22\]、日本電気のLIME\[23\]のようにLISPマシン市場への参入を試みた例もある。[青山学院大学](../Page/青山学院大学.md "wikilink")で開発されたALPS/1は、8080の特定の命令実行を横取りし、ハードウェアでデータを処理させる、という仕組みであった。

情報処理学会のコンピュータ博物館サイトの「神戸大LISPマシン」の解説\[24\]の最後に「TAKITAC-7のアーキテクチャは後のFACOM-αとNTTのELISが継承した．」とあるが、いずれもそのまま引き継いでいるわけではない。FACOM αは同社のメインフレームないしミニコンのバックエンドとして動作するものである。またELISについては関係者が執筆した記事によれば、設計者は（神戸大LISPマシンを）32ビットにしただけと言ったりもするが、VLSIチップにすることを前提にそれに適したアーキテクチャとして設計されており\[25\]。、そういった点は独自性が強い。

### その後・現在

RISCワークステーションの性能対価格比の向上により、これらLISPマシンの優位は消え失せ、ミニコンピュータなどともろともに、高水準言語寄りのアーキテクチャは基本的には「過去の遺物」とみなされるようになった。ワークステーションの後にはパーソナルコンピュータが続き、ワークステーションのメーカーも一掃された。現代では、一般のデスクトップPCが特別なハードウェア無しでLISPマシンの何倍も高速にLISPを実行できるようになった。

1990年代初めにはLISPマシンを製造していた企業は商売が成り立たなくなった。ゼロックス以外ではシンボリックスが今も残っている唯一の企業で、LISPマシン環境 Open Genera と 数式処理システム [Macsyma](../Page/Macsyma.md "wikilink") を販売している。

各種LISPマシンの[オープンソース](../Page/オープンソース.md "wikilink")のエミュレータを作る試みがいくつかなされている。

  - CADRのエミュレーション\[26\]
  - シンボリックスのLISPマシンのエミュレーション\[27\]
  - E3プロジェクト（TI Explorer II のエミュレーション）\[28\]
  - Meroko（TI Explorer I のエミュレーション）\[29\]
  - Nevermore（TI Explorer I のエミュレーション）\[30\]

2005年10月3日、MITはCADRのソースコードをオープンソースとして公開した\[31\]。

BitsaversのPDF文書アーカイブには\[32\]、シンボリックスのLISPマシン\[33\]、TI Explorer\[34\]とMicroExplorer\[35\]、ゼロックスのInterLisp-Dマシン\[36\]について、各種文書のPDF版が保管されている。

### その他の高水準言語マシン

日本の[第五世代コンピュータ](../Page/第五世代コンピュータ.md "wikilink")計画では、LISPよりもさらに高水準の、論理推論の操作をハードウェア化し、[Prolog](https://ja.wikipedia.org/wiki/Prolog "wikilink")などの[論理プログラミング](../Page/論理プログラミング.md "wikilink")言語の高速処理を目的としたマシン（逐次推論型マシン PSI、並列推論型マシン PIM）が開発された。また、[Prolog](https://ja.wikipedia.org/wiki/Prolog "wikilink")をより直接的に実装することを意図したプロセッサやコプロセッサが1980年代後半から1990年代前半にかけていくつか開発されている。例えば[カリフォルニア大学バークレー校](../Page/カリフォルニア大学バークレー校.md "wikilink")の VLSI-PLM\[37\]、その後継のPLUM\[38\]、関連するマイクロコード実装\[39\]などがある。設計レベルに留まり、実際にハードウェアが製作されなかった例もいくつかある\[40\]\[41\]。LISPと同様、Prologの基本計算モデルは標準的な命令型設計とは大きく異なるため、計算機科学者や電気工学者は根底にある計算モデルのエミュレートによって生じるボトルネックをなんとか解消しようとしてきた。

[ニクラウス・ヴィルト](../Page/ニクラウス・ヴィルト.md "wikilink")の[Lilith](../Page/Lilith.md "wikilink")プロジェクトでは、[Modula-2](https://ja.wikipedia.org/wiki/Modula-2 "wikilink")言語を指向した独自CPUを採用している\[42\]。

近年の例には、1990年代終盤に最初に構想された[サン・マイクロシステムズ](../Page/サン・マイクロシステムズ.md "wikilink")によるものを代表とする、[Java](https://ja.wikipedia.org/wiki/Java "wikilink")に最適化されたJavaプロセッサ（[:en:Java processor](https://ja.wikipedia.org/wiki/:en:Java_processor "wikilink")）がある。

[エリクソン](../Page/エリクソン.md "wikilink")は[Erlang](../Page/Erlang.md "wikilink")に最適化したプロセッサ ECOMP を開発したが\[43\]、製品化はしていない。

### 用途

LISPマシンは主に[人工知能](../Page/人工知能.md "wikilink")アプリケーションの領域で使われたが、[コンピュータグラフィックス](../Page/コンピュータグラフィックス.md "wikilink")、[医用画像処理](../Page/医用画像処理.md "wikilink")などの分野でも使われた。

1980年代の主要な商用[エキスパートシステム](../Page/エキスパートシステム.md "wikilink")はLISPマシンに移植されている。インテリコープの [Knowledge Engineering Environment](https://ja.wikipedia.org/wiki/:en:KEE "wikilink") (KEE)、The Carnegie Group Inc. の Knowledge Craft、Inference Corporation の ART (Automated Reasoning Tool) などである\[44\]。

## 技術概要

もともとLISPマシンはLISPによるソフトウェア開発のための個人用ワークステーションとして設計された。1人の人間が使用するようになっていて、マルチユーザーモードはない。大きなモノクロのビットマップディスプレイ、キーボード、マウス、ネットワークアダプター、ハードディスク、1MB以上のRAM、シリアルインタフェース、拡張カードスロットなどを備えている。カラーグラフィックス、磁気テープ装置、レーザープリンターなどはオプションである。

プロセッサはLISPを直接実行するわけではなく、コンパイルされたLISPに最適化された命令セットを持つ[スタックマシン](../Page/スタックマシン.md "wikilink")になっている。初期のLISPマシンはマイクロコードで命令セットを実装していた。いくつかの演算で、型チェックとディスパッチがハードウェアで実行時に行われる。例えば、加算命令は1つだけで、各種数値型（整数、浮動小数点数、有理数、複素数）の加算を自動的に行う。そのため、LISPコードをコンパイルしたものは非常にコンパクトになる。

次の例はリスト (list) の要素それぞれに対して述語 (predicate) を作用させ、「真」を返す要素数を数える関数である。

``` lisp
(defun example-count (predicate list)
  (let ((count 0))
    (dolist (i list count)
      (when (funcall predicate i)
        (incf count)))))
```

この関数を（シンボリックスの Ivory マイクロプロセッサ向けに）コンパイルした機械語コードを逆アセンブルしたものを以下に示す。

``` text
Command: (disassemble (compile #'example-count))

  0  ENTRY: 2 REQUIRED, 0 OPTIONAL      ;Creating PREDICATE and LIST
  2  PUSH 0                             ;Creating COUNT
  3  PUSH FP|3                          ;LIST
  4  PUSH NIL                           ;Creating I
  5  BRANCH 15
  6  SET-TO-CDR-PUSH-CAR FP|5
  7  SET-SP-TO-ADDRESS-SAVE-TOS SP|-1
 10  START-CALL FP|2                    ;PREDICATE
 11  PUSH FP|6                          ;I
 12  FINISH-CALL-1-VALUE
 13  BRANCH-FALSE 15
 14  INCREMENT FP|4                     ;COUNT
 15  ENDP FP|5
 16  BRANCH-FALSE 6
 17  SET-SP-TO-ADDRESS SP|-2
 20  RETURN-SINGLE-STACK
```

オペレーティングシステムは[仮想記憶](../Page/仮想記憶.md "wikilink")によって大きなアドレス空間を提供している。OSのメモリ管理機能の一部としてガベージコレクションも行う。全てのコードは単一のアドレス空間を共有している。メモリに格納されているあらゆるデータオブジェクトにはタグが付属しており、実行時にデータ型を判別できる。単一アドレス空間内に複数の実行スレッドがあり、それらを「プロセス」と呼ぶ。

全OSソフトウェアはLISPで書かれている。ゼロックスはInterLisp、シンボリックスとLMIとTIは[Maclisp](../Page/Maclisp.md "wikilink")から派生した Lisp Machine Lisp を使っている。Common Lisp が登場するとLISPマシンでも Common Lisp をサポートするようになり、Common Lisp でソフトウェアが書かれるようになった。

後期のLISPマシン（TI MicroExplorer、Symbolics MacIvory、Symbolics UX400/1200 など）はワークステーションとしてではなく、何らかのホストコンピュータ（Macintosh II や Sun-3/4 など）に組み込むカードの形で製品化された。

Symbolics XL1200 などのLISPマシンは特別なグラフィックスカードを備え、グラフィックス機能が強化されていた。そのようなLISPマシンは医用画像処理、3次元アニメーション、CAD などに使われた。

## 脚注

## 参考文献

  - "[LISP Machine Progress Report](https://dspace.mit.edu/handle/1721.1/5751)", Alan Bawden, Richard Greenblatt, Jack Holloway, Thomas Knight, David Moon, Daniel Weinreb, [AI Lab](../Page/MIT人工知能研究所.md "wikilink") memos, AI-444, 1977.
  - "[CADR](https://hdl.handle.net/1721.1/5718)", Thomas Knight, David A. Moon, Jack Holloway, Guy L. Steele. AI Lab memos, AIM-528, 1979.
  - "[Design of LISP-based Processors, or SCHEME: A Dielectric LISP, or Finite Memories Considered Harmful, or LAMBDA: The Ultimate Opcode](https://hdl.handle.net/1721.1/5731)", [Guy Lewis Steele, Jr.](../Page/ガイ・スティール・ジュニア.md "wikilink"), Gerald Jay Sussman, AI Lab memo, AIM-514, 1979
  - David A. Moon. [*Chaosnet*](https://dspace.mit.edu/handle/1721.1/6353). A.I. Memo 628, Massachusetts Institute of Technology Artificial Intelligence Laboratory, June 1981.
  - "Implementation of a List Processing Machine". Tom Knight, Master's thesis.
  - [Lisp Machine manual](http://bitsavers.org/pdf/mit/cadr/chinual_6thEd_Jan84/), 6th ed. [Richard Stallman](../Page/リチャード・ストールマン.md "wikilink"), Daniel Weinreb, David Moon. 1984.
  - "Anatomy of a LISP Machine", [Paul Graham](../Page/ポール・グレアム.md "wikilink"), *AI Expert*, December 1988
  - *Free as in Freedom: Richard Stallman's Crusade for Free Software*

## 外部リンク

  - [Symbolics](http://www.symbolics-dks.com/)

  - [Medley](http://top2bottom.net/medley.html)

  - Bitsavers にある PDF 文書群

      - [LMI documentation](http://www.bitsavers.org/pdf/lmi)
      - [MIT CONS documentation](http://www.bitsavers.org/pdf/mit/cons)
      - [MIT CADR documentation](http://www.bitsavers.org/pdf/mit/cadr)
      - [Symbolics documentation](http://www.bitsavers.org/pdf/symbolics/)
      - [TI MicroExplorer documentation](http://www.bitsavers.org/pdf/ti/microexplorer/)
      - [TI Explorer documentation](http://www.bitsavers.org/pdf/ti/explorer/)
      - [Xerox Interlisp documentation](http://www.bitsavers.org/pdf/xerox/interlisp)

  - Lisp Machine マニュアルなど

      - ["The Lisp Machine manual, 4th Edition, July 1981"](http://www.bitsavers.org/pdf/mit/cadr/chinual_4thEd_Jul81.pdf)
      - ["The Lisp Machine manual, 6th Edition, HTML/XSL version"](http://common-lisp.net/project/bknr/static/lmman/frontpage.html)
      - ["The Lisp Machine manual"](http://doi.acm.org/10.1145/1056737.1056738)

  - ["Lisp Machine Inc. K-machine: The Deffenbaugh, Marshall, Powell, Willison architecture as remembered by Joe Marshall"](http://fare.tunes.org/tmp/emergent/kmachine.htm)

  - ["My Lisp Experiences and the Development of GNU Emacs"](http://www.gnu.org/gnu/rms-lisp.html) - [リチャード・ストールマン](../Page/リチャード・ストールマン.md "wikilink")による [GNU Emacs](../Page/GNU_Emacs.md "wikilink")、LISP、LISPマシン に関する講演を書き起こしたもの

  - [CADR simulation](http://www.unlambda.com/cadr/index.html)

  - [L-machine simulation](http://www.unlambda.com/l-machine/index.html)

  - [CADR LISP Machine source code released by MIT (Oct 3 2005)](http://www.heeltoe.com/retro/mit/mit_cadr_lmss.html)

  - ["A Few Things I Know About LISP Machines"](http://fare.tunes.org/LispM.html)

  - [LISPMACHINE.NET - Lisp Books and Information](http://www.lispmachine.net/)

  - [Lisp machines timeline](http://www.andromeda.com/people/ddyer/lisp/) LISPマシンの年表

  - [Zeta-C](http://www.cliki.net/Zeta-C)

  - [Picture of a partially disassembled Symbolics 3640](http://www.wired.com/techbiz/media/multimedia/2001/07/45699)

  - ["Présentation Générale du projet M3L"](http://www.limsi.fr/~jps/actions/m3l/doc/m3l.presentation.htm) - フランスでの同様のプロジェクト

[Category:人工知能](https://ja.wikipedia.org/wiki/Category:人工知能 "wikilink") [Category:コンピュータアーキテクチャ](https://ja.wikipedia.org/wiki/Category:コンピュータアーキテクチャ "wikilink") [Category:ミニコンピュータ](https://ja.wikipedia.org/wiki/Category:ミニコンピュータ "wikilink") [Category:ワークステーション](https://ja.wikipedia.org/wiki/Category:ワークステーション "wikilink") [Category:LISP](https://ja.wikipedia.org/wiki/Category:LISP "wikilink")

1.  Newquist, Harvey. *The Brain Makers*, Sams Publishing, 1994. ISBN 0-672-30412-0
2.
3.  Levy,S: *Hackers*. Penguin USA, 1984
4.  Moon 1985
5.
6.  [Moby space](http://www.patentgenius.com/patent/4779191.html) Patent application 4779191
7.
8.
9.
10.
11.
12.
13. Müller-Schloer “Bewertung der RISC-Methodik am Beispiel COLIBRI”, “RISC-Architekturen”, Editor A. Bode, BI-Verlag, 1988
14. Christian Hafer, Josef Plankl, F. J. Schmitt., COLIBRI: Ein RISC-LISP-System, Architektur von Rechensystemen, Tagungsband, 11. ITG/GI-Fachtagung, 7.-9. März 1990, München, Germany 1990
15.
16.
17.
18.
19.
20.
21.
22.
23.
24. <http://museum.ipsj.or.jp/computer/other/0001.html>
25. [竹内郁雄](https://ja.wikipedia.org/wiki/竹内郁雄 "wikilink")の執筆記事「マルチパラダイム言語TAO 第1回 LispマシンELIS」（ <http://www.nue.org/nue/tao/bitao/s001.html> ）による
26.
27.
28.
29.
30.
31.
32.
33.
34.
35.
36.
37.
38.
39.
40.
41.
42.
43. <http://www.erlang.se/euc/00/processor.ppt>
44. Richter,Mark: *AI Tools and Techniques*. Ablex Publishing Corporation USA, 1988, Chapter 3, An Evaluation of Expert System Development Tools
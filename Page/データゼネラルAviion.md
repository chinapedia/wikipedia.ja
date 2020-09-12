> この記事は[データゼネラルAviion](https://ja.wikipedia.org/wiki/データゼネラルAviion)から翻訳されています。


**Aviion** (表現は**AViiON**) は、[データゼネラル](../Page/データゼネラル.md "wikilink")社のコンピュータシリーズで、1980年代後半から同社のサーバ製品が2001年に製造中止になるまで、同社の主力製品であった。初期のAviionモデルでは[Motorola 88000](../Page/MC88000.md "wikilink") [CPU](../Page/CPU.md "wikilink")を使用していたが、1990年代初頭にMotorolaが88000の開発を中止したため、後のモデルではオール[Intelのソリューションに移行した](https://ja.wikipedia.org/wiki/インテル "wikilink")。これらの後期のインテルベースのマシンのいくつかのバージョンでは[Windows NTが動作し](../Page/Microsoft_Windows_NT.md "wikilink")、高価格帯のマシンでは同社独特のUnixである[DG/UX](https://ja.wikipedia.org/wiki/DG/UX "wikilink")が動作した。

## 歴史

データゼネラル(DG)社は、その大部分の歴史で、[価格性能比が優れ競争力のある](https://ja.wikipedia.org/wiki/コストパフォーマンス "wikilink") (しかし、当時の精神では、互換性のない) [ミニコンピュータ](../Page/ミニコンピュータ.md "wikilink")で[DEC社の戦略を基本的に踏襲していた](../Page/ディジタル・イクイップメント・コーポレーション.md "wikilink")。しかし、1980年代になると、データゼネラル社は明らかにDEC社に比べて下向きのスパイラルに陥っていた。カスタム設計されたミニコンピュータCPUの性能が、コモディティ(一般的)なマイクロプロセッサと比べて低下しているため、カスタムソリューションを開発するためのコストはもはや割に合わなくなっていた。より良い解決策は、同じコモディティなプロセッサを使用しながら、コモディティなマシンよりも優れた性能を提供するように組み合わせることであった。

Aviionによって、DGは、純粋に独自仕様のミニコンピュータラインから、急成長しているUnixサーバ市場へと視野をシフトした。新しいラインはMotorola 88000をベースにしたもので、[マルチプロセッシング](../Page/マルチプロセッシング.md "wikilink")をサポートし、特にクリーンなアーキテクチャを持つ高性能[RISC](../Page/RISC.md "wikilink")プロセッサであった。これらのマシンは、DG/UXとして知られている[System V](../Page/UNIX_System_V.md "wikilink") Unixのバリアントを実行し、主に同社のリサーチ・トライアングル・パーク施設で開発された。DG/UXは、同社の[Eclipse MV](https://ja.wikipedia.org/wiki/Eclipse_MV/8000 "wikilink") 32ビットミニコンピュータ ([Novaと](../Page/データゼネラルNova.md "wikilink")16ビット[Eclipseミニの後継機](../Page/Eclipse_\(コンピュータ\).md "wikilink")) ファミリーで動作していたが、Eclipse MVの主力であるとオペレーティングシステムのごく二次的な役割しかなかった。また、この時代の一部のAviionサーバは、独自のMEDITECH MAGICオペレーティングシステムを実行していた\[1\]。

1988年2月から1990年10月まで、Robert E. Cousinsはワークステーション開発部門のマネージャーを務めた。この間、彼らはMaverickプロジェクトと、300、310、400シリーズのワークステーションと4000シリーズのサーバを含むいくつかの後続製品を開発した。

Aviionは1989年の夏から様々なサイズで発売された。これらはピザボックス型ワークステーション (コードネーム「Maverick」)とローラーマウント型とラックマウント型のサーバ (「Topgun」) としてデビューした。その後、スピードアップやスケールアップが行われ、1995年には16 CPU **AV/9500**サーバ、32ウェイ**AV/10000**サーバが発売され、DGは [NUMA (Non-Uniform Memory Access)](../Page/NUMA.md "wikilink") 設計を初めて採用した。ワークステーションはしばらくの間、ラインの一部として残ったが、重点はサーバに移った。

1992年、モトローラは[AIMアライアンスに参加し](https://ja.wikipedia.org/wiki/AIM連合 "wikilink")、[IBM POWER](https://ja.wikipedia.org/wiki/Power_Architecture "wikilink") CPUのデザインをデスクトップマシン用のシングルチップCPUに「切り詰め」たバージョンを開発し、最終的に88000の開発は中止された。このため、DGはMotorolaとの協力関係を断念し、代わりにボリュームマイクロプロセッサの分野ですぐに勝者となるものに取り組み、Intel i386アーキテクチャのCPUを使用することにした。

この結果、最初は[Pentiumをベースにした第](../Page/Intel_Pentium_\(1993年\).md "wikilink")2シリーズのAviionマシンが誕生し、その後、より高速な[Pentium Pro](../Page/Pentium_Pro.md "wikilink")、[Pentium II](../Page/Pentium_II.md "wikilink")、[Pentium III](../Page/Pentium_III.md "wikilink") [Xeon](../Page/Xeon.md "wikilink") CPUが採用された。このコモディティ化されたハードウェアのアプローチにより、DGはIntelから供給された「標準的な大量生産」x86マザーボードにメモリコヒーレント相互接続 (Scalable Coherent Interconnect; SCI)を追加したNUMAサーバを開発した。現在はIBMの一部となっている[シークエント・コンピュータ](../Page/シークエント・コンピュータ.md "wikilink")も、当時は同様の戦略をとっていた。「Manx」というコードネームのシステムは、オリジナルのPentiumとZenithハードウェアをベースにしたNUMAの初期の取り組みで、市場に出ることはなかった。**AV 20000** (「Audubon」) は、32個の Pentium Pro プロセッサ (最大8個のクアッドプロセッサ ビルディングブロック) に接続されていた。後の **AV 25000** (「Audubon 2」) のアップグレードでは、これを 64個の Pentium II (後のPentium III) Xeonに拡張した。

Windows NTの人気が急上昇したため、インテルベースのAviionサーバもAviion x86ラインのOSにWindowsを追加した。その結果、ローエンドでは、特に既存のDG顧客の中でNTへの切り替えを決断した顧客の間で、かなりの割合で収益に貢献した。しかし、ハイエンドでは、Windows NTはNUMAサーバのシングルブロック (つまりクアッドプロセッサ) ビルディングブロック上で効率的に実行できたものの、大規模なシステムで高性能を達成するために必要なプロセッサとメモリの親和性を最適化できなかった。その結果、DGのNUMAサーバ上のWindowsは、技術的な現実よりも、常にマーケティング・ストーリーになっていた。

同じ頃、DGは [Santa Cruz Operations (SCO)](https://ja.wikipedia.org/wiki/Santa_Cruz_Operations "wikilink") などと「業界標準」のUnixオペレーティングシステムに向けて積極的に取り組んでいた。しかし、最初はSCOのデータセンター・アクセラレーション・プログラム(DCAP)を使用し、次に[Project Montereyを使用したが](../Page/Project_Monterey.md "wikilink")、これは実現しなかった。最終的に、DGのNUMAサーバは、業界がCompaq (後にHPに買収)、HP、IBM、Sun Microsystemsといった数社の大手ベンダーのUnixプラットフォームを中心にまとまりつつあった時期に、別の大規模なプロプライエタリなUnixサーバとして終了を迎えた。

1999年にEMCは、主にディスクアレイストレージ製品の ラインと関連ソフトウェアへのアクセスを得るために、データゼネラルを12億ドルで買収した。持分プーリング法の条件の下で、EMCは2年間サーバラインを維持したが、契約条件が許すとすぐに販売を中止し、その時点でAviionは姿を消した。

## ノート

「AViiON」という名前は、しばしば「Nova II」のアナグラム(言葉遊び)であると主張されてきたが、[Nova](../Page/データゼネラルNova.md "wikilink") はDGの最も成功した製品の一つである。新製品の名前を決めるために従業員によるコンペが開催されたが、どの案も商標登録の目的では認められなかった。初期のEclipseシステムのコードネームには「バード(The Bird)」や「ビッグバード(The Big Bird)」などがあったが、飛行にちなんだ名称が適切と考えられた。「Avion」も提案されていたが、商標化できなかった。当時、ヨーロッパの2つの企業が、繰り返し母音を使用したネーミングのトレンドを生み出していた - BaanとBiiNである。Avionは「i」を繰り返し、残りの単語を大文字にしてAViiONとすることで変更された。「*Avion* (または *avión*) 」はフランス語とスペイン語で「航空機」を意味する言葉である。

この「ii」の使用は、CLARiiONとTHiiN Lineの製品ラインにも引き継がれている。

## 脚注

## 外部リンク

  - [The m88k Resource: Data General AViiON](https://web.archive.org/web/20110927073518/http://badabada.org/aviion.html)
  - [Allen Briggs' Data General AViiON information](https://web.archive.org/web/20081118194552/http://www.ninthwonder.com/~briggs/aviion/)
  - [Aviion at m88k.org](https://web.archive.org/web/20090106155831/http://www.m88k.org/systems/folder.2005-02-05.0047476253/)
  - [Unorganized collection of 88k AViiON technical information](https://web.archive.org/web/20131105091115/http://user.dtcc.edu/~ctribo/88k/)

[Category:ワークステーション](https://ja.wikipedia.org/wiki/Category:ワークステーション "wikilink")

1.  ["Network World Apr 23, 1990 P. 26"](https://books.google.com/books?id=cx0EAAAAMBAJ&pg=PA26&dq=aviion+meditech+magic&hl=en&ei=Yp3ZTrmaKMPMtgfwtZztAQ&sa=X&oi=book_result&ct=result&resnum=2&ved=0CEMQ6AEwAQ#v=onepage&q=aviion%20meditech%20magic&f=false)
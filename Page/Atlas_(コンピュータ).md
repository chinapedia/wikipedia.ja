> この記事は[Atlas \(コンピュータ\)](https://ja.wikipedia.org/wiki/Atlas_\(コンピュータ\))から翻訳されています。


**Atlas Computer**（**アトラスコンピュータ**）は、1962年から1971年に稼働した世界初の[スーパーコンピュータ](../Page/スーパーコンピュータ.md "wikilink")の1つ。当時は世界で最も高性能なコンピュータとされた\[1\]。Atlasの稼働が止まるとイギリスが持つ全コンピュータの能力の半分が失われると言われた\[2\]。[ページング方式](../Page/ページング方式.md "wikilink")を使った[仮想メモリ機能](../Page/仮想記憶.md "wikilink")(当時は1レベルストアと呼んだ)を搭載した世界初のマシンとして有名であり、この方式は急速に拡散し、今日では当然なものになった。

Atlasは[真空管](../Page/真空管.md "wikilink")ではなく[電子部品](../Page/電子部品.md "wikilink")の[バイポーラトランジスタ](../Page/バイポーラトランジスタ.md "wikilink")を使用した[第2世代のコンピュータだった](https://ja.wikipedia.org/wiki/計算機の歴史 "wikilink")。[マンチェスター・ビクトリア大学](../Page/マンチェスター大学.md "wikilink")、[フェランティ](../Page/フェランティ.md "wikilink")、[プレッシーが共同でAtlasを開発した](https://ja.wikipedia.org/wiki/:en:Plessey "wikilink")。Atlasは他にも2台あり、うち1台は[ブリティッシュ・ペトロリアムと](../Page/BP_\(企業\).md "wikilink")[ロンドン大学](../Page/ロンドン大学.md "wikilink")のために作られ、もう1台は[オックスフォード](../Page/オックスフォード.md "wikilink")近くのチルトンにある[アトラスコンピュータ研究所に納入された](https://ja.wikipedia.org/wiki/:en:Atlas_Computer_Laboratory "wikilink")。

フェランティは[ケンブリッジ大学](../Page/ケンブリッジ大学.md "wikilink")のために改良版を製作した。これは[TitanまたはAtlas](https://ja.wikipedia.org/wiki/Titan_\(コンピュータ\) "wikilink") 2と呼ばれ\[3\]、メモリ構成が異なり、ケンブリッジ大学コンピュータ研究所が開発した[タイムシェアリングシステム](../Page/タイムシェアリングシステム.md "wikilink")に対応したOSが動作した。Atlas 2は他にも2台あり、1台はケンブリッジの[CAD](../Page/CAD.md "wikilink")センター(後のCADCentreで、さらに後にの[AVEVA](https://ja.wikipedia.org/wiki/アヴィバ "wikilink"))に、もう1台はアルダーマストンにある[イギリス核兵器研究所](https://ja.wikipedia.org/wiki/核兵器機関 "wikilink")(AWRE)に納入された。

マンチェスター大学のAtlasは1971年に撤去された。CADCentreにあった最後のAtlasは1976年の年末に運用を終えた。チルトンのAtlasの部品が[エディンバラ](../Page/エディンバラ.md "wikilink")にある[スコットランド国立博物館](https://ja.wikipedia.org/wiki/スコットランド国立博物館 "wikilink")に保存されている他、2014年7月に発見されたメインコンソールが[オックスフォード](../Page/オックスフォード.md "wikilink")近くのチルトンにある[ラザフォードアップルトン研究所に保管されている](https://ja.wikipedia.org/wiki/ラザフォード・アップルトン・ラボラトリー "wikilink")。

## 歴史

### 背景

1956年はコンピュータの開発でイギリスがアメリカに後れを取っているとの認識が高まっていた。フェンティのB.W.ポラードは4月にコンピュータのカンファレンスで「イギリスには中規模のコンピュータが複数台あり、真に高速なコンピュータはケンブリッジのEDSAC 2とManchester Mark 2だけしかないが、2台ともアメリカで最も早いマシンよりはるかに遅い」と話した。5月にも[科学産業研究省調査会の高速計算機検討委員会で同様の懸念が報告された](https://ja.wikipedia.org/wiki/:en:Department_of_Scientific_and_Industrial_Research_\(United_Kingdom\) "wikilink")。

その頃[マンチェスター大学](../Page/マンチェスター大学.md "wikilink")の[トム・キルバーン](https://ja.wikipedia.org/wiki/トム・キルバーン "wikilink")とそのチームは[トランジスタ](../Page/トランジスタ.md "wikilink")ベースのシステムを試しており、様々な技術を検証するために2台の小さなマシンを製作していた。この技術が非常に優れていたことは明らかで、キルバーンはトランジスタベースのマシンにどのような機能を装備すべきかについて1956年に購入希望者からの聞き取り調査を開始した。商用利用を予定しているユーザーは様々な周辺機器に対応することを希望する一方で、[イギリス原子力エネルキー省は](https://ja.wikipedia.org/wiki/United_Kingdom_Atomic_Energy_Authority "wikilink")1マイクロ秒で1命令を実行できる高速なマシン(現代の表現で1MFLOPSの性能)を希望した。この要求からMicroSecond Engineを意味するMuseの名前が付けられた\[4\]。

数多くの周辺機器をサポートすることと、高速に動作するということは相反する要求だった。例えば[パンチカード](../Page/パンチカード.md "wikilink")リーダーからデータを読み込むプログラムは、リーダーがデータを送信してくるのを待つことにほとんどの時間を費やす。こうした周辺機器をサポートしつつ[CPU](../Page/CPU.md "wikilink")の効率も維持するため、新機種にはデータをバッファリングするための大量のメモリが必要であり、システム上のデータの流れを制御する[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink")(OS)も必要だった。

### MuseからAtlasへ

米国がさらに高速な[UNIVAC LARCと](../Page/LARC.md "wikilink")[IBM STRETCHを開発しているとの情報を得たバーント委員会](../Page/IBM_7030.md "wikilink")(旧高速計算機検討委員会)は、軍用技術の民間への転用を検討する[イギリス研究開発公社(NDRC)に問題を報告した](https://ja.wikipedia.org/wiki/:en:National_Research_Development_Corporation "wikilink")。18ヶ月間かけて見込みユーザー、フェンティや[EMI](../Page/EMI.md "wikilink")の技術者チーム、マンチェスター大学や[イギリス国防省レーダー研究所の設計チームらと会議を重ねた](https://ja.wikipedia.org/wiki/:en:Royal_Radar_Establishment "wikilink")。

こうした努力があったにもかかわらず、NDRCからの資金は1958年夏の時点では提供されていなかった。キルバーンは話を前進させるため、小型のMuseを製作して様々な設計を実験で試してみることにした。マンチェスター大学はMark 1を時間貸しすることによって得られたお金を基金に貯めており、これを原資にして開発が始まった。このプロジェクトが始まってすぐの1958年10月に、フェンティも開発に参加することを決めた。1959年にNDRCからシステム開発費用として30万ポンドの資金が提供された。これはシステムが成功したら返却する約束だった。マシンの名前はプロジェクトの途中でAtlasに変更された。

詳細設計は1959年末に完成し、[コンパイラ](../Page/コンパイラ.md "wikilink")の開発が進んでいた。しかしスーパーバイザ・オペレーティングシステムの開発はかなり遅れていた。フェランティが新たに採用したデビッド・ハワースがチームに参加してプログラマの人数が2人から6人に増えた。パワフルでエネルギッシュなハワーズらが不眠不休の努力を続けた結果、周辺機器の問題を解決する[マルチプログラミング](../Page/マルチタスク.md "wikilink")(マルチタスク)機能を搭載した、[アセンブリ言語](../Page/アセンブリ言語.md "wikilink")で35,000行のスーパーバイザ(OS)が完成した。

### Atlasの設置

Atlasの第1号機は1962年にマンチェスター大学に設置された。[フェランティ・マーキュリー](https://ja.wikipedia.org/wiki/フェランティ・マーキュリー "wikilink")の運用が12月末に終了する予定になっており、設置はこれに間に合わせることが求められた。Atlasは予定通りに設置され、12月7日にAEAのディレクターである[ジョン・コッククロフト](../Page/ジョン・コッククロフト.md "wikilink")に正式に引き渡された。このシステムで動作したのは初期バージョンのスーパーバイザだけで、コンパイラは[Autocodeだけしかなかった](https://ja.wikipedia.org/wiki/:en:Atlas_Autocode "wikilink")。1964年1月に[ALGOL 60と](../Page/ALGOL.md "wikilink")[FORTRAN](../Page/FORTRAN.md "wikilink")を搭載したスーパーバイザの最終バージョンがインストールされるまでこの状況は続いた。

1号機は1日20時間の運用スケジュールで1960年代中頃まで使われ、1000本以上のプログラムが動作した。使用時間はマンチェスター大学とフェランティが共有し、フェランティは1時間500ポンドで顧客企業に使わせた。収益の一部は大学のコンピュータ収益基金に返還された。もし仮に大学がコンピュータ時間を民間企業から借りていたら累計で72万ポンドを支払う必要があったと1969年に推計された。このマシンは1971年11月30日に運用を終えた。

フェランティは2台のAtlasを販売しており、1台は1963年に[ロンドン大学](../Page/ロンドン大学.md "wikilink")と[ブリティッシュ・ペトロリアムの合弁企業に](../Page/BP_\(企業\).md "wikilink")、もう1台は1964年12月に[イギリス核エネルギー研究所](https://ja.wikipedia.org/wiki/:en:Atomic_Energy_Research_Establishment "wikilink")(ハーウェル)に納入された。AEAのマシンは、ハーウェルの敷地からわずか数ヤード離れたチルトンの[アトラスコンピュータ研究所に移設され](https://ja.wikipedia.org/wiki/:en:Atlas_Computer_Laboratory "wikilink")、民有地に設置されて利用しやすくなった。このマシンは拡張され、48ビットで48Kワードの[コアメモリと](../Page/磁気コアメモリ.md "wikilink")32台のテープドライブを搭載する最大のAtlasとなった。コンピュータ時間はイギリスの全大学が占有できた。1974年3月に運用を終了した。

### TitanとAtlas 2

フェランティは1962年2月にAtlasマシンのパーツの一部を[ケンブリッジ大学](../Page/ケンブリッジ大学.md "wikilink")に提供し、その見返りとして大学はシステムのコストダウン版を開発することになった。その成果はTitanとなり1963年夏に稼働した。フェランティはこれをAtlas 2の名前で2台販売し、うち1台を1963年に[イギリス核兵器研究所](https://ja.wikipedia.org/wiki/核兵器機関 "wikilink")(アルダーマストン)に、もう1台を1966年にイギリス政府が支援しているCADセンターに納入した。

### その後

AltasはアメリカのLARCとSTRETCHに対抗するコンピュータとして設計された。いずれもAtlasより先に運用が始まり、LARCは1961年から、STRETCHもAtlasより数か月前から稼働した。AtlasはLARCより4倍高速で、STRETCHより若干遅かった。Atlasに追加された[浮動小数点演算器は](../Page/浮動小数点数.md "wikilink")1.59µsで処理できた一方、STRETCHは同じ仕事を1.38µsから1.5µsで処理できた。LARCの販売は試みられておらず、STRETCHも最終的に何台製造されたのか明らかではない。

1964年に登場した[CDC 6600で初めてAtlasが明らかな敗北を喫した](../Page/CDC_6600.md "wikilink")。CDCは1959年にMuseの解説を読んだことからインスピレーションを得ており、おかげで開発が大幅に加速して当初の予定よりも早く完成したことを後に明らかにした。オーストラリアの科学産業研究所[CSIROは元々Atlasを購入する方向で打ち合わせていたが](../Page/オーストラリア連邦科学産業研究機構.md "wikilink")、結果的にCDCが契約を獲得するに至った。

フェランティは1960年代初頭に深刻な経営難に直面し、1963年にコンピュータ部門を[ICTへ売却した](https://ja.wikipedia.org/wiki/:en:International_Computers_and_Tabulators "wikilink")。ICTはカナダの[Ferranti-Packard 6000をベースにした構成で中型機であるICT](https://ja.wikipedia.org/wiki/:en:Ferranti-Packard_6000 "wikilink") 1900シリーズの販売に注力した。

## 技術解説

### ハードウェア

ハードウェアには数多くの斬新な機能があったが、運用上特に重要な機能のみを以下に示す(ここで示すストレージのサイズはマンチェスター大学に設置されたオリジナルの物であれ、別の場所に設置したマシンでは拡張された)。

  - [48ビット](https://ja.wikipedia.org/wiki/48ビット "wikilink")の[ワード](../Page/ワード.md "wikilink")長。1ワードの内容は「浮動小数点数１つ」「命令1つ」「24ビットのアドレス2つ」「整数2つ」「6ビットの文字コードで8文字」のいずれか。
  - キャリー伝播時間を最小限に抑えるために新しい回路を採用した高速[加算器](../Page/加算器.md "wikilink")。
  - 24ビット (200万ワード、1600万文字)の[アドレス空間](../Page/アドレス空間.md "wikilink")。スーパーバイザ(不可侵)ストア、Vストア、固定ストア、ユーザーストアで構成される。
  - 16[Kワードの](../Page/2進接頭辞.md "wikilink")[コアストア](../Page/磁気コアメモリ.md "wikilink")(96[KBに相当](https://ja.wikipedia.org/wiki/キビバイト "wikilink"))。奇数アドレスと偶数アドレスでインターリーブしている。
  - 8[Kワードの読み取り専用メモリ](../Page/2進接頭辞.md "wikilink")(固定ストア)。ここにはスーパーバイザ(OS)やエクストラコードルーチン(ライブラリ関数)が含まれる。
  - 96Kワードの[ドラムストア](../Page/磁気ドラムメモリ.md "wikilink")(最大576KB相当)。4つのドラムに分割されているが、[仮想メモリ機能により](../Page/仮想記憶.md "wikilink")1つのコアストアとして扱われる。
  - 主に二重修飾命令(インデックス修飾)で使われる128本の高速[インデックスレジスタ](https://ja.wikipedia.org/wiki/インデックスレジスタ "wikilink")(Bライン)。レジスタアドレス空間にはエクストラコード(システムサービスルーチン)のオペランドアドレス(引数として渡すアドレス)を指定するレジスタや、[浮動小数点](../Page/浮動小数点数.md "wikilink")[アキュムレータに指数を渡すレジスタなどの特別なレジスタも含まれる](../Page/アキュムレータ_\(コンピュータ\).md "wikilink")。128本のうち3本は[プログラムカウンタ](https://ja.wikipedia.org/wiki/プログラムカウンタ "wikilink")(PC)レジスタで、第125レジスタはスーパーバイザ(割り込み)のPC、第126レジスタはエクストラコードのPC、第127レジスタはユーザーPCだった。第0レジスタは常に0の値を保持していた。
  - [磁気テープ](../Page/磁気テープ.md "wikilink")などの当時としては最新の[周辺機器](../Page/周辺機器.md "wikilink")を接続可能で、[ダイレクトメモリアクセス（DMA)機能を搭載](../Page/Direct_Memory_Access.md "wikilink")。
  - メモリの一部として参照できるデバイスの配線を読み書きすることによる、Vストアアドレス([メモリマップドI/O](https://ja.wikipedia.org/wiki/メモリマップドI/O "wikilink"))、[割り込み](../Page/割り込み_\(コンピュータ\).md "wikilink")、エクストラコードルーチンによる周辺機器の制御。
  - 目的の仮想メモリがコアストアに存在するかどうかを決定するページアドレスレジスタの[連想メモリ](../Page/連想メモリ.md "wikilink")。
  - [命令パイプライン](https://ja.wikipedia.org/wiki/命令パイプライン "wikilink")

Atlasはクロックによる同期を使わない非同期プロセッサであったため、その処理能力を一言で表すのは難しい。以下に例を示す。

  - [固定小数点数](../Page/固定小数点数.md "wikilink")の[レジスタ加算](../Page/レジスタ_\(コンピュータ\).md "wikilink") – 1.59[µs](https://ja.wikipedia.org/wiki/マイクロ秒 "wikilink")
  - [浮動小数点数](../Page/浮動小数点数.md "wikilink")の加算(修飾なし) – 1.61µs
  - 浮動小数点数の加算(二重修飾) – 2.61µs
  - 浮動小数点数の乗算(二重修飾) – 4.97µs

### エクストラコード

エクストラコードはAtlasの機能の1つで、複雑な命令をソフトウェアで実装する技術だった。エクストラコードルーチンの呼び出しや戻りと、オペランドへのアクセスを、専用のハードウェアで処理した。またエクストラコードルーチンはROMに格納されており、コアストアよりもアクセスが速かった。

48ビット機であるAlrasでは上位10ビットが[オペコード](../Page/オペコード.md "wikilink")だった。最上位ビットが0の命令はハードウェアが直接実行する通常のマシン語命令だった。最上位ビットが1の命令はエクストラコードで、固定ストア([ROM](../Page/Read_only_memory.md "wikilink"))内にある特別な種類の[サブルーチン](../Page/サブルーチン.md "wikilink")ジャンプとして実装され、呼び出し先[アドレスは残りの](../Page/メモリアドレス.md "wikilink")9ビットにより決まった。最大512個のエクストラコードが実装可能であり、うち約250個が実装された。

エクストラコードは現代のコンピュータ用語でいう所の[ソフトウェア割り込みまたは](../Page/割り込み_\(コンピュータ\).md "wikilink")[トラップである](../Page/例外処理.md "wikilink")。[三角関数](../Page/三角関数.md "wikilink")、[対数](../Page/対数.md "wikilink")、[平方根](../Page/平方根.md "wikilink")など、[ハードウェア](../Page/ハードウェア.md "wikilink")で実装すると効率が悪い数学系の[サブルーチン](../Page/サブルーチン.md "wikilink")が定義されていた。しかしエクストラコードの約半分は[OSを処理するスーパーバイザ関数に使われた](../Page/オペレーティングシステム.md "wikilink")。例えば「指定のストリームから特定の文字を印刷する」「論理テープNから512ワードを読み込む」などの指示ができた。エクストラコードはユーザー[プログラムがスーパーバイザと通信できる唯一の手段だった](../Page/プログラム_\(コンピュータ\).md "wikilink")。[フェランティ・オニオンなどの当時のイギリスのマシンはOSのサービスを呼び出すのに同様のメカニズムを採用した](https://ja.wikipedia.org/wiki/:en:Ferranti_Orion "wikilink")。

### ソフトウェア

Atlasは今日のソフトウェアに使われている数多くの概念のパイオニアであり、そのうちの1つである[Atlas Supervisorは現代の定義で言う所のオペレーティングシステムの最初の実装であると考えられている](https://ja.wikipedia.org/wiki/Atlas_Supervisor "wikilink")\[5\]。

Atlasで最初の[高水準言語](../Page/高水準言語.md "wikilink")は[Atlas Autocodeで](https://ja.wikipedia.org/wiki/Atlas_Autocode "wikilink")、[ALGOL 60とは同世代の言語であり](../Page/ALGOL.md "wikilink")、主にトニー・ブルッカーがALGOL 60の欠点を解決する目的で開発した。しかしAtlasはALGOL 60も後にサポートし、[FORTRAN](../Page/FORTRAN.md "wikilink")、[COBOL](../Page/COBOL.md "wikilink")、ABL (Atlas Basic Language、マシン語に近い言語)などもサポートした。数多くの学生が在籍する大学ではOSが保護される形で[マシンコードによる開発ができる開発環境として支持を得ていた](../Page/機械語.md "wikilink")。

一部のコンパイラは[コンパイラ・コンパイラで開発されており](../Page/パーサジェネレータ.md "wikilink")、このやり方で開発された[コンパイラ](../Page/コンパイラ.md "wikilink")としては初期のものと見られている。

SPG (System Program Generator)というプログラミング言語も搭載していた。SPGで書かれたプログラムは実行時に別のプログラムを動的に生成してコンパイルできた。ユーザー定義[マクロ機能があった](../Page/マクロ_\(コンピュータ用語\).md "wikilink")。変数は<山括弧>で括られ、テキストパーサーを備えており、SPGプログラムのソースコードは[バッカス・ナウア記法](../Page/バッカス・ナウア記法.md "wikilink")に似ていた。

### ハードウェアとソフトウェアの統合

Atlasは当初からOSをマシンの一部として考えたスーパーコンピュータとして設計された。ハードウェアにはOSの動作に役立つ特殊な機能が備わっていた。例えばエクストラコードのルーチンと割り込みルーチンはそれぞれ個別に専用のストレージ、レジスタ、プログラムカウンタが割り当てられていたため、ユーザーモードからエクストラモードやエグゼクティブモードへの、またはエクストラモードからエグゼクティブモードへの[コンテキストスイッチ](../Page/コンテキストスイッチ.md "wikilink")は非常に高速だった。

## 注釈

## 出典

## 参考文献

  -
  -
  -
  -
<!-- end list -->

  - *Parallel addition in digital computers: A new fast 'carry' circuit, T. Kilburn, D.B.G. Edwards, D. Aspinall, Proc. IEE Part B September 1959*

  - *The Central Control Unit of the "Atlas" Computer*, F. H. Sumner, G. Haley, E. C. Y. Chen, Information Processing 1962, Proc. IFIP Congress '62

  - *One-Level Storage System*, T. Kilburn, D. B. G. Edwards, M. J. Lanigan, F. H. Sumner, IRE Trans. Electronic Computers April 1962 [Accessed 2011-10-13](https://web.archive.org/web/20080724050906/http://www.cs.utexas.edu/users/dburger/teaching/cs395t-s08/papers/11_virtual.pdf)

  -
  -
  - *The Atlas Supervisor*, T. Kilburn, R .B. Payne, D .J. Howarth, reprinted from *Computers—Key to Total Systems Control*, Macmillan 1962

  - *The Atlas Scheduling System*, D. J. Howarth, P. D. Jones, M. T. Wyld, Comp. J. October 1962

  - *The First Computers: History and Architectures*, edited by Raúl Rojas and Ulf Hashagen, 2000, MIT Press,

  - *A History of Computing Technology*, M. R. Williams, IEEE Computer Society Press, 1997,

## 外部リンク

  - [The Atlas Autocode Reference Manual](http://history.dcs.ed.ac.uk/archive/docs/atlasautocode.html)
  - [The Atlas Supervisor paper (T Kilburn, R B Payne, D J Howarth, 1962)](http://www.chilton-computing.org.uk/acl/technology/atlas/p019.htm)
  - <http://bitsavers.informatik.uni-stuttgart.de/pdf/ict_icl/atlas/>
  - [Ferranti Atlas 1 & 2: List of References](http://www.ourcomputerheritage.org/ccs-f5x5.pdf)

[Category:マンチェスターの歴史](https://ja.wikipedia.org/wiki/Category:マンチェスターの歴史 "wikilink") [Category:トランジスタ・コンピュータ](https://ja.wikipedia.org/wiki/Category:トランジスタ・コンピュータ "wikilink") [Category:コンピュータ史](https://ja.wikipedia.org/wiki/Category:コンピュータ史 "wikilink") [Category:コンピュータ_(歴代)](https://ja.wikipedia.org/wiki/Category:コンピュータ_\(歴代\) "wikilink") [Category:初期のコンピュータ](https://ja.wikipedia.org/wiki/Category:初期のコンピュータ "wikilink")

1.
2.
3.
4.
5.
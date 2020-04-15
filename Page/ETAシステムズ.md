> この記事は[ETAシステムズ](https://ja.wikipedia.org/wiki/ETAシステムズ)から翻訳されています。


**ETAシステムズ** (*ETA Systems*) は、[1983年](https://ja.wikipedia.org/wiki/1983年 "wikilink")に[コントロール・データ・コーポレーション](../Page/コントロール・データ・コーポレーション.md "wikilink") (CDC) からのスピンオフによって設立された[アメリカ合衆国](https://ja.wikipedia.org/wiki/アメリカ合衆国 "wikilink")の[スーパーコンピュータ](../Page/スーパーコンピュータ.md "wikilink")企業。**ETA10**という高性能マシンをリリースすることに成功したが、赤字を出し続けたため、CDCはこの会社を[1989年](../Page/1989年.md "wikilink")にたたんだ。

## 歴史

[CDCは](../Page/コントロール・データ・コーポレーション.md "wikilink")、[シーモア・クレイ](../Page/シーモア・クレイ.md "wikilink")が自らの[クレイ](../Page/クレイ.md "wikilink")・リサーチ社を設立してからは、[スーパーコンピュータ](../Page/スーパーコンピュータ.md "wikilink")市場での立場が弱くなっていった。CDCの[ウィリアム・ノリス](https://ja.wikipedia.org/wiki/ウィリアム・ノリス "wikilink")は、世界最高性能のスーパーコンピュータを作るには大きくなり過ぎた会社では無理だと判断し、[1983年](https://ja.wikipedia.org/wiki/1983年 "wikilink")、開発部門をスピンオフさせたETAシステムズ社を設立した。ETAシステムズは[1986年](https://ja.wikipedia.org/wiki/1986年 "wikilink")までに10[G](../Page/ギガ.md "wikilink")[FLOPS](../Page/FLOPS.md "wikilink")のマシン（[命令サイクル](../Page/命令_\(コンピュータ\).md "wikilink")10[ナノ](https://ja.wikipedia.org/wiki/ナノ "wikilink")秒）を作ることを目標としていた。

この目標を達成するため、ETAは[CMOS](../Page/CMOS.md "wikilink")回路を[液体窒素](../Page/液体窒素.md "wikilink")で冷却することによって高[クロック](../Page/クロック.md "wikilink")で駆動するなどの革新的技術を生み出した。これによってETA10は7ナノ秒の命令サイクルを実現し、ベンチマークでは 10GFLOPSを達成した。しかし、実際のアプリケーションでは最高でも4.5GFLOPSしか出せなかったとも言われている。

その後、30GFLOPSを目標としてETA30が計画されたが、実現することはなかった。[1989年](../Page/1989年.md "wikilink")4月、CDCはETAシステムズをたたみ、CDCに戻すことを決定した。それまでに液冷システムが7台、空冷システムが27台売れた（実際に納入されたのはもっと少ないという説もある）。その時点でETA10はスーパーコンピュータ市場で最高の価格性能比を誇っていた。その後、CDCはスーパーコンピュータからは完全に手を引き、残っていた ETA10マシンをある高校に無料で提供した。

## ETA10

### ハードウェア

[ETA10_logo_and_body.jpg](https://ja.wikipedia.org/wiki/File:ETA10_logo_and_body.jpg "fig:ETA10_logo_and_body.jpg")所蔵。\]\] [ETA10_body.jpg](https://ja.wikipedia.org/wiki/File:ETA10_body.jpg "fig:ETA10_body.jpg")所蔵。\]\] ETA10の[ハードウェア](../Page/ハードウェア.md "wikilink")は、基本的に[CDC Cyber](https://ja.wikipedia.org/wiki/CDC_Cyber "wikilink")-205の[アーキテクチャをベースにしており](../Page/コンピュータ・アーキテクチャ.md "wikilink")、互換性があった。Cyberシリーズと同様、ETA10は[クレイ](../Page/クレイ.md "wikilink")のマシンのような[ベクタープロセッサを使わず](../Page/ベクトル計算機.md "wikilink")、メモリアクセスをパイプライン化して高速な[主記憶装置](../Page/主記憶装置.md "wikilink")（メモリ）を接続していた。共有メモリ型の[マルチプロセッサ](https://ja.wikipedia.org/wiki/マルチプロセッサ "wikilink")機であり、最大8個の[CPU](../Page/CPU.md "wikilink")（と最大16個の[I/Oプロセッサ](../Page/チャネル・コントローラ.md "wikilink")）を接続している。各CPUは1[命令サイクルで](../Page/命令_\(コンピュータ\).md "wikilink") 4つの[倍精度](https://ja.wikipedia.org/wiki/倍精度 "wikilink")演算か 8つの[単精度](https://ja.wikipedia.org/wiki/単精度 "wikilink")演算を実行できる。

ETA10の性能は[液体窒素](../Page/液体窒素.md "wikilink")冷却による動作周波数の高速化によるものである。一般的な[CMOS](../Page/CMOS.md "wikilink")技術で製造されていたが、CPUを冷却することによって 7[ナノ](https://ja.wikipedia.org/wiki/ナノ "wikilink")秒という命令サイクルを実現した\[1\]。ETA10-FとETA10-Gは液冷式の 7ナノ秒命令サイクルのマシンであり、ETA10-QとETA10-Pは空冷式の19ナノ秒命令サイクルのマシンである。後者は "Piper" とも呼ばれた。いずれのマシンでもシングルプロセッサマシンとしてもマルチプロセッサマシンとしても構成可能である。

ETA10のCPUは[CMOS](../Page/CMOS.md "wikilink")[ゲートアレイ](https://ja.wikipedia.org/wiki/ゲートアレイ "wikilink")を250個、44層の[プリント基板](../Page/プリント基板.md "wikilink") (PCB) に実装したものである。個々のゲートアレイは20,000[ゲートを集積しており](https://ja.wikipedia.org/wiki/論理回路 "wikilink")、1.25μmルールで製造されている。当時の一般的なCMOSゲートアレイは3μmから5μmルールだった。当時のスーパーコンピュータでCMOSを採用することは一般的ではなかったが、集積度が高いので配線による遅延を低減できるとの判断でCMOSを採用している。しかし[ECLに比べると遅いため](../Page/エミッタ結合論理.md "wikilink")、[液体窒素](../Page/液体窒素.md "wikilink")で冷却してクロック周波数を上げるという技法を採用した。

各CPUには[SRAMで構成された](../Page/Static_Random_Access_Memory.md "wikilink")400万ワードのローカルメモリが接続されている。それとは別に、[DRAMで構成された](../Page/Dynamic_Random_Access_Memory.md "wikilink")2億5600万ワードの共有メモリがある。また、ETA10ではプロセッサや[I/Oデバイスを](../Page/入出力.md "wikilink")[光ファイバー](../Page/光ファイバー.md "wikilink")で接続していた。1980年代のシステムとしては革新的な技術である。

### ソフトウェア

ETA10の[ソフトウェア](../Page/ソフトウェア.md "wikilink")はひどいものだったと言わざるをえない。1986年に出荷されたとき、完全動作する[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink") (OS) もなかったのである。[プログラムは](../Page/プログラム_\(コンピュータ\).md "wikilink")[アポロコンピュータ](../Page/アポロコンピュータ.md "wikilink")製[ワークステーション](../Page/ワークステーション.md "wikilink")から一度にひとつだけロードして実行する必要があった。そして、次のプログラムを実行するにはETA10をリブートしなければならなかった。当初、CDCはCyber 205のVSOSを移植する予定だったが、[ハードウェア](../Page/ハードウェア.md "wikilink")の性能を引き出すには新しいOSが必要であると判断された。

当時、[UNIX](../Page/UNIX.md "wikilink")が[スーパーコンピュータ](../Page/スーパーコンピュータ.md "wikilink")に導入されて勢力を拡大していたが、ETAシステムズは独自のEOSオペレーティングシステムを開発することを選択した。[1988年](../Page/1988年.md "wikilink")には[UNIX System V](../Page/UNIX_System_V.md "wikilink") Release 3をベースとしたOSが導入されたことで、ETA10はやっと使えるシステムになった。

ETAのソフトウェアの問題はOSの選択だけではなかった。[FORTRAN](../Page/FORTRAN.md "wikilink")[コンパイラ](../Page/コンパイラ.md "wikilink")はほとんど変更を加えずにCDC Cyber 205から持ち込まれた。[ソースコード](../Page/ソースコード.md "wikilink")の互換性が重要視されつつあった時代に、ETA10のコンパイラは独特な[コーディングが必要だった](https://ja.wikipedia.org/wiki/プログラミング_\(コンピュータ\) "wikilink")。さらに、[コンパイラ最適化](../Page/コンパイラ最適化.md "wikilink")技術の進歩には追随していなかった。

## 導入例

全部で25システムが出荷されている。以下に導入例を挙げる。

  - [フロリダ州立大学](../Page/フロリダ州立大学.md "wikilink") - 1号機を1987年1月5日に導入
  - [ジョンソン宇宙センター](../Page/ジョンソン宇宙センター.md "wikilink")
  - ジョン・フォン・ノイマン・スーパーコンピュータセンター
  - [パデュー大学](../Page/パデュー大学.md "wikilink") - ETA10への[UNIX System Vの移植を行った](../Page/UNIX_System_V.md "wikilink")。
  - [東京工業大学](../Page/東京工業大学.md "wikilink") - 液冷の8CPUシステムを導入
  - [明治大学](../Page/明治大学.md "wikilink") - ETA10-Pを1989年に導入
  - [台湾中央研究院](http://www.sinica.edu.tw/main_e.shtml)
  - [ドイツ気象局](https://ja.wikipedia.org/wiki/ドイツ気象局 "wikilink")

[NASAによれば](../Page/アメリカ航空宇宙局.md "wikilink")、ETA10は[エイムズ研究センター](https://ja.wikipedia.org/wiki/エイムズ研究センター "wikilink")での受け入れ試験で不合格になったという\[2\]。

### 東京工業大学への納入

[1988年](../Page/1988年.md "wikilink")、日本の[東京工業大学](../Page/東京工業大学.md "wikilink")はETA10を導入した\[3\]。これは東京工業大学の情報処理センターとしては初めてのスーパーコンピュータの導入である。通常、初めての導入ともなれば失敗しないように実績のあるマシンを選択するものだが、ETA10が選択されたことにはいくつかの要因があった。まずETA10のカタログ性能10GFLOPSは当時としてはずば抜けていた。そして当時、米国と日本は貿易摩擦問題があり、その象徴としてスーパーコンピュータの貿易不均衡について米国が日本に圧力をかけていた（[日米スパコン貿易摩擦](../Page/日米スパコン貿易摩擦.md "wikilink")）。以上のことから導入が決定されたのである\[4\]。

しかし、納入されたETA10は非常に故障が多いため8ウェイの[マルチプロセッサ](https://ja.wikipedia.org/wiki/マルチプロセッサ "wikilink")マシンとしてはなかなか使えず、結果として8台の1.25GFLOPSのシングルプロセッサマシンとして使われていたと言われている。後に東京工業大学はCray C916を導入。こちらは故障もなく稼動し、利用率も高かった。

## 脚注

## 参考文献

  - R.W. Hockney and C.R. Jesshope, *Parallel Computers 2: Architecture, Programming and Algorithms*, Adam Hilger, 1988, pp. 185–190.

## 外部リンク

  - [A description of computer systems at the Waalsdorp museum, including the ETA line](http://www.museumwaalsdorp.nl/computer/en/comp891E.html)
  - [Another page at Waalsdorp, including a block diagram of the ETA architecture](http://www.museumwaalsdorp.nl/computer/en/eta10p.html)
  - [The ETA Saga](http://yarchive.net/comp/eta_peglar.html)
  - [IEEE article about the ETA10 liquid-nitrogen-cooled supercomputer system](http://ieeexplore.ieee.org/xpl/freeabs_all.jsp?arnumber=30952)

[Category:スーパーコンピュータ](https://ja.wikipedia.org/wiki/Category:スーパーコンピュータ "wikilink") [Category:かつて存在したアメリカ合衆国のコンピュータ企業](https://ja.wikipedia.org/wiki/Category:かつて存在したアメリカ合衆国のコンピュータ企業 "wikilink")

1.  もっとも、実際にETA-10Gを利用したことがある[牧野淳一郎](../Page/牧野淳一郎.md "wikilink")は“液体窒素冷却で7nsクロックで動くはずがまだ 10.5nsでしか動かない”機械だった、と[自身の日記](http://jun.artcompsci.org/journal/journal-2007-02.html#17)で述懐しており、当初は7nsでは動かなかったようである
2.  John T. Barton, [A History of the ETA-10Q Acceptance Tests at NAS](http://ntrs.nasa.gov/archive/nasa/casi.ntrs.nasa.gov/19970012375_1997015894.pdf)
3.
4.  平成元年11月10日 第116回国会 決算委員会 <http://kokkai.ndl.go.jp/SENTAKU/syugiin/116/0410/11611100410004c.html>
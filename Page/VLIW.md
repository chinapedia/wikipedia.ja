> この記事は[VLIW](https://ja.wikipedia.org/wiki/VLIW)から翻訳されています。


[Vliwpipeline.png](https://ja.wikipedia.org/wiki/File:Vliwpipeline.png "fig:Vliwpipeline.png")の概念図。4個の並列に動作するEXモジュールを持ち、1ワードあたり4命令を並列に実行する。\]\] **VLIW**（、超長命令語）とは、[プロセッサ](../Page/プロセッサ.md "wikilink")の[命令セット](https://ja.wikipedia.org/wiki/命令セット "wikilink")アーキテクチャ（ISA）の一種類である。

VLIWプロセッサは、その[実行ユニット](https://ja.wikipedia.org/wiki/実行ユニット "wikilink")が並列的に一度に実行できる、ロード・ストア・演算・分岐などの命令の複数個から成る、かなり長い命令語によってー単位の命令が構成されており、それをそのまま実行ユニットに投入する（各命令をatom、まとまったものをmoleculeなどと呼ぶこともある）。実行に複数クロック掛かるような命令もあるかもしれないが、そういったものも含めて、タイミング的に全て差し支えなく実行できるようにVLIWの[機械語](../Page/機械語.md "wikilink")プログラムは書かれていなければならず、依存や順序を解決するような機構をハードウェアでは持たない。一般に、そのようなコードを生成するのは[コンパイラ](../Page/コンパイラ.md "wikilink")の仕事となる。また、どうしても埋められないスロットはNOP(No Operation・何もしない）で埋め、命令語の長さは常に固定長となる。一般にVLIWプロセッサ自身はRISCのコンセプトをより押し進めたような設計であるが、以上のような「複数の機能が詰め込まれた長い固定長の命令」は[マイクロプログラム方式](../Page/マイクロプログラム方式.md "wikilink")における、いわゆる水平型マイクロプログラムを直接外に出したようなもの、といったような感じに近い。なお、「超長命令」の由来は命令語が最低でも（たとえば）128ビットといったように長いものであることからである。

[スーパースカラ](https://ja.wikipedia.org/wiki/スーパースカラ "wikilink")や[アウトオブオーダーなどと異なり](../Page/アウト・オブ・オーダー実行.md "wikilink")、命令列はフェッチされたそのまま[実行ユニット](https://ja.wikipedia.org/wiki/実行ユニット "wikilink")に投入され、投入された後も並列性の分析などといった必要がない為、[ハードウェア](../Page/ハードウェア.md "wikilink")コストの低下や動作の高速化が期待される。反面、VLIWの性能を引き出すにはコンパイラが重要である。その意味でRISCよりもさらに[ソフトウェア](../Page/ソフトウェア.md "wikilink")に依存する側に寄った[アーキテクチャといえる](../Page/コンピュータ・アーキテクチャ.md "wikilink")。

命令セットアーキテクチャではなく、[マイクロアーキテクチャ](../Page/マイクロアーキテクチャ.md "wikilink")を指してVLIWの語が使われることもある。

VLIWの採用例として、サーバ向けとして商品化された[マイクロプロセッサ](../Page/マイクロプロセッサ.md "wikilink")としては、インテルがHPと開発した[IA-64](https://ja.wikipedia.org/wiki/IA-64 "wikilink")（[Itanium](../Page/Itanium.md "wikilink")）の[EPICアーキテクチャ](https://ja.wikipedia.org/wiki/EPICアーキテクチャ "wikilink")があるが（EPICは修正VLIWアーキテクチャである、などとされることもある）、IA-64については（当初もくろんだようにx86の代替としては）普及はしていない。後述するが、組込み用プロセッサではVLIW風の設計の、複数メーカの複数の製品ファミリが継続している。

## 歴史

*VLIW*という用語とそのアーキテクチャの概念は、1980年代初期に当時[イェール大学](../Page/イェール大学.md "wikilink")のによって考案された。

とはいえ1980年前後には顕著であった[集積回路](../Page/集積回路.md "wikilink")の集積度の向上と、CGなどといった膨大な計算量が必要な応用からの要請により\[1\]、似たようなアイディアは他でも独立して考案されており、日本で富田眞治らがQA-1に続き1983年に完成させたQA-2などはVLIWアーキテクチャの先駆であった\[2\]、と、こんにちでは位置付けられている。

フィッシャーは、[ニューヨーク大学](../Page/ニューヨーク大学.md "wikilink")の大学院生のとき、[トレーススケジューリング](https://ja.wikipedia.org/wiki/トレーススケジューリング "wikilink")というVLIWのコンパイル技術を開発した。VLIWが発明される以前には、機能ユニットをあらかじめソフトウェアでスケジューリングし、命令レベルの並列化をするという考え方は、[水平型マイクロコードの開発過程ですでに確立していた](../Page/マイクロプログラム方式.md "wikilink")。フィッシャーの業績は、一般的なプログラミング言語で書かれたプログラムを、水平型マイクロコードに変換するコンパイラを開発したことにある。フィッシャーの行った研究によって、ワイドイシューなマシン上で良いパフォーマンスを出すためには、[基本ブロック](https://ja.wikipedia.org/wiki/基本ブロック "wikilink")の中だけではなく、それを超えて並列性を探す必要があることが分かった。彼は、基本ブロックを超えた並列性を見つけるための[リージョンスケジューリング](https://ja.wikipedia.org/wiki/リージョンスケジューリング "wikilink")も開発した。[トレーススケジューリング](https://ja.wikipedia.org/wiki/トレーススケジューリング "wikilink")も、そうしたスケジューリングテクニックのひとつである。このスケジューリング技術は、最も起こりそうな基本ブロックの経路を最初にスケジューリングする。そして、次に、二番目に起こりそうな経路をスケジューリングするという風に、最後までスケジューリングしていく。それぞれのスケジューリングを行うとき、投機的な動作を扱うコードも必要に応じて、挿入する。

フィッシャーが行った二つ目の革新的な業績は、ターゲットCPUのアーキテクチャは、コンパイラに向くように設計されるべきで、VLIWのコンパイラとアーキテクチャは、協調設計されなくてはならないと概念を主張したことである。このことは、イェール大学でフィッシャーがFPS164のようなアーキテクチャ向けのコンパイラを作ることが難しかったという体験に基づいている。FPS164は、複雑な命令体系を持っているため、コード生成で最適な[命令スケジューリング](https://ja.wikipedia.org/wiki/命令スケジューリング "wikilink")を実現するには、複雑なアルゴリズムを必要とした。フィッシャーは、[セルフドレイン・パイプライン](https://ja.wikipedia.org/wiki/セルフドレイン・パイプライン "wikilink")(self-draining pipelines)・広いマルチポート[レジスタファイル](https://ja.wikipedia.org/wiki/レジスタファイル "wikilink")・といったVLIWの設計を特徴付ける原則を開発していった。これらの原則によって、コンパイラが簡単に高速なコードを生成できる。

最初のVLIWコンパイラは、ジョン・エリスの博士論文(指導教授:フィッシャー)で述べられている\[3\]。 ジョン・ルッテンバーグもまた、スケジューリングに関するある重要なアルゴリズムを開発した。

1984年にイェール大学を離れたフィッシャーは、というスタートアップ会社を設立した。そのときの共同創立者は、ジョン・オドネルとジョン・ルッテンバーグである。Multiflowは、TRACEシリーズというVLIWの[ミニコンを生産し](../Page/ミニコンピュータ.md "wikilink")、1988年頃に販売開始した。MultiflowのVLIWは、28演算を並列に実行できた。TRACEシステムは、MSI (Medium-Scale Integration) / LSI (Large-Scale Integration) / VLSI (Very Large-Scale Integration)という異なる技術を使って実装された。こうした異なる技術を混ぜることは、あまり評判が良くなく、いずれメモリ以外の部品がひとつのチップ上に実装されるようになる。Multiflowは、少し時代を先取りしすぎていたところがある。しかし、主な半導体会社は、Multiflowの技術の価値を認め、コンパイラやアーキテクチャのライセンスを取得していた。

## 後方互換性

シリコン技術が進み、より広い実行ユニットが実装できるようになったが、初期のVLIWプロセッサ用にコンパイルされたバイナリプログラムは、より広い実行ユニットをもつプロセッサでは、実行できない。なぜなら、VLIWの命令セットは、そのプロセッサの実行ユニット数に依存していたからである。

[Transmeta](https://ja.wikipedia.org/wiki/Transmeta "wikilink")では、[x86](https://ja.wikipedia.org/wiki/x86 "wikilink")アーキテクチャのCrusoeという実装において、バイナリ・バイナリソフトウェアレイヤ（*[コードモーフィング](https://ja.wikipedia.org/wiki/バイナリ変換 "wikilink")*）で後方互換性を維持しようとした。Crusoeは、基本的に、実行時にリコンパイル・最適化・x86の[オペコード](../Page/オペコード.md "wikilink")への変換をCPU内部のマシンコードで行うと言われている。したがって、Crusoeは、*内部的には*VLIWプロセッサであるといえる。

インテルの[Itanium](../Page/Itanium.md "wikilink")アーキテクチャでは、もっと一般的な方法で、後方互換性を維持しようとしている。1つの命令は、複数のオペコードを持ち、それぞれのオペコードが、その前のVLIW命令との依存関係を示すビットフィールドが割り当てられている。このビットは、コンパイル時に設定されるので、ハードウェアが依存関係を調べる必要がなくなる。また、こうした依存関係情報を命令列の中に埋め込むことで、実行ユニット数に依存しなくなる。つまり、プロセッサは実行ユニットがもつ分だけ、依存しない命令を並列実行すればよい。

もうひとつのVLIWアーキテクチャの欠点は、常にすべての実行ユニットを使うことができず、[NOP](../Page/NOP.md "wikilink")命令を実行してしまうということである。これは、そのコード内にたくさんの命令の依存関係が存在する場合に起こる。

ひとつのチップ上にのせることができるトランジスタが増えるにつれて、VLIWのこうした欠点は、あまり重要でなくなってきている。VLIWは、アプリケーションごとにカスタマイズしたプロセッサを使用できる組み込み市場で人気が出てきている。組込み向けVLIWプロセッサは、 [富士通](../Page/富士通.md "wikilink")の[FR-V](https://ja.wikipedia.org/wiki/FR-V "wikilink")、[Pixelworks](https://ja.wikipedia.org/wiki/Pixelworks "wikilink")の[BSP15/16](http://www.pixelworks.com/)、[STMicroelectronicsの](../Page/STマイクロエレクトロニクス.md "wikilink")、[NXPの](https://ja.wikipedia.org/wiki/NXPセミコンダクターズ "wikilink")\[4\]、CEVAの、 Improv Systemsの、[Silicon Hive](http://www.siliconhive.com)など、多くのメーカーが開発し発売している。また、テキサス・インスツルメンツのC6xxxファミリーの DSPもVLIWということになる。

## 主なVLIWプロセッサ

  -
  - [Intel i860](https://ja.wikipedia.org/wiki/Intel_i860 "wikilink")

  - [Crusoe](../Page/Crusoe.md "wikilink")

  - [Itanium](../Page/Itanium.md "wikilink")

  - [FR-V](https://ja.wikipedia.org/wiki/FR-V "wikilink")

  - [Radeon](https://ja.wikipedia.org/wiki/Radeon "wikilink") HDシリーズ (HD 2xxx、HD 3xxx、HD 4xxx、HD 5xxx)

## 関連項目

  - [CISC](../Page/CISC.md "wikilink")
  - [EPICアーキテクチャ](https://ja.wikipedia.org/wiki/EPICアーキテクチャ "wikilink")
  - [IA-64](https://ja.wikipedia.org/wiki/IA-64 "wikilink")

## 脚注

[Category:CPU](https://ja.wikipedia.org/wiki/Category:CPU "wikilink") [Category:1980年代](https://ja.wikipedia.org/wiki/Category:1980年代 "wikilink")

1.  1980年代前半に作られたCG用並列計算システムのひとつに、日本で作られた LINKS-1（http://museum.ipsj.or.jp/computer/other/0013.html ）がある。
2.  <http://museum.ipsj.or.jp/computer/other/0010.html>
3.  [ACM Award](http://www.acm.org/awards/dd_citation/1985.html), [ACM](../Page/Association_for_Computing_Machinery.md "wikilink"), [1985年](https://ja.wikipedia.org/wiki/1985年 "wikilink")
4.  [Trimedia](http://www.nxp.com/products/nexperia/home/products/media_processors/index.html)
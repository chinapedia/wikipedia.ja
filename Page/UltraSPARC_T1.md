> この記事は[UltraSPARC T1](https://ja.wikipedia.org/wiki/UltraSPARC_T1)から翻訳されています。


[サン・マイクロシステムズ](../Page/サン・マイクロシステムズ.md "wikilink")'の**UltraSPARC T1**[マイクロプロセッサ](../Page/マイクロプロセッサ.md "wikilink")（[2005年](https://ja.wikipedia.org/wiki/2005年 "wikilink")[11月14日](../Page/11月14日.md "wikilink") の発表までは開発 [コードネーム](../Page/コードネーム.md "wikilink") "**Niagara**" として知られる）は、[マルチスレッド](https://ja.wikipedia.org/wiki/スレッド_\(コンピュータ\)#スレッドとプロセスとタスク "wikilink")・[マルチコア](https://ja.wikipedia.org/wiki/マルチコア "wikilink")の [CPU](../Page/CPU.md "wikilink") である。[サーバのエネルギー消費を下げるべく開発されており](https://ja.wikipedia.org/wiki/サーバ#server_hardware "wikilink")、1.4 GHz で 72 [ワット](../Page/ワット.md "wikilink") の電力を消費する。

T1は全く新しく設計された[SPARC](../Page/SPARC.md "wikilink") マイクロプロセッサの実装で、[UltraSPARC Architecture 2005 specification](http://opensparc-t1.sunsource.net/)に準拠し、 完全な SPARC V9 [命令セット](https://ja.wikipedia.org/wiki/命令セット "wikilink")を実行する。サンはこれまでに[UltraSPARC IVおよび](https://ja.wikipedia.org/wiki/UltraSPARC_IV "wikilink")[UltraSPARC IV+という二つのマルチコアプロセッサを開発したが](https://ja.wikipedia.org/wiki/UltraSPARC_IV+ "wikilink")、T1はサンにとって最初のマルチコア*かつ*マルチスレッドのマイクロプロセッサである。 T1マイクロプロセッサは 4コア、6コア、8コアのものが提供されており、各コアは4つの[スレッドを同時に扱うことができる](../Page/スレッド_\(コンピュータ\).md "wikilink")。すなわちプロセッサ全体で32スレッドを並行して処理することが可能である。

サンのハイエンドの [SMPシステム同様](../Page/対称型マルチプロセッシング.md "wikilink")、UltraSPARC T1もパーティション化して動作することができる。すなわち、複数のコアに一つないし複数のプロセスやスレッドを動作させ、その他のコアがシステムの残りの処理を実行するよう分割することができる。

## 搭載システム

T1 プロセッサーは以下のサンと[富士通](../Page/富士通.md "wikilink")の製品に搭載されている:

  - Sun [SPARC Enterprise](../Page/SPARC_Enterprise.md "wikilink") T1000 と T2000 サーバ
  - [Sun Fire](https://ja.wikipedia.org/wiki/:en:Sun_Fire "wikilink") T1000 と T2000 サーバ
  - Netra T2000 サーバ
  - Netra CP3060 ブレード
  - Sun Blade T6300 サーバモジュール

## 特徴

このCPUは発売当時の汎用CPUが想定する最大内部コア数を凌駕する8コア構成までが用意されており、1コア当たり4本のスレッドを同時に処理できる点において、非常に特異な設計になっている。そのため、[Webサーバ](../Page/Webサーバ.md "wikilink")や、中間層の Java, ERP, CRM アプリケーションサーバなど、多数のアクセスを同時に処理する必要があるような用途に向いている。UltraSPARC T1 設計の欠点の一つは、設計時点のトランジスタ数の制約により各コアの演算ユニットを整数演算に限定し、[FPU](../Page/FPU.md "wikilink")は1個が全コアで共有されていることであり、[科学技術計算](https://ja.wikipedia.org/wiki/科学技術計算 "wikilink")や[コンピュータ・グラフィックス](https://ja.wikipedia.org/wiki/コンピュータ・グラフィックス "wikilink")等、大量の浮動小数点演算を実行するような運用方法には不向きである。

Web やアプリケーションの処理以外に、UltraSPARC T1 は多数のユーザーアカウントを持つ小さなデータベースアプリケーション(言い換えると１つの処理は軽いが高多重度)に適している可能性がある。[サン・マイクロシステムズ](../Page/サン・マイクロシステムズ.md "wikilink")のとある顧客は、UltraSPARC T1 で動作する [MySQL](https://ja.wikipedia.org/wiki/MySQL "wikilink")アプリケーションが、AMD Opteronサーバより 13.5倍高速であることを示す結果を公表している \[1\]。

## 仮想化

T1はハイパーバイザ権限による実行モードをサポートする最初のSPARCプロセッサである。SPARCハイパーバイザはこのモードで動作し、T1システムをそれぞれがオペレーティングシステムのインスタンスを実行可能な32個の[論理ドメインに分割することができる](https://ja.wikipedia.org/wiki/:en:Logical_Domains "wikilink")。

現在、[Solaris](../Page/Solaris.md "wikilink")と[Linux](https://ja.wikipedia.org/wiki/Linux "wikilink")がサポートされており、[FreeBSD](../Page/FreeBSD.md "wikilink")サポートが現在開発中である \[2\]。

## ソフトウェアライセンスの問題

伝統的に、[Oracle Databaseのような商用のソフトウェアスイートは](../Page/Oracle_Database.md "wikilink")、ソフトウェアが動作するプロセッサの個数により顧客に対して課金を行っている。2006年はじめ、[オラクル](https://ja.wikipedia.org/wiki/オラクル_\(企業\) "wikilink") は**プロセッサ係数** (Processor Factor) を導入しライセンスモデルを変更した。T1のプロセッサ係数は0.25であり、8コアのT2000は2CPUのライセンスしか必要でない \[3\]。

2006年第3四半期には、[IBM](../Page/IBM.md "wikilink")がバリューユニット価格 (Value Unit, VU) の概念を導入した。T1の各コアは、標準の100PVU/コアではなく30 PVUとなっている \[4\]。

## T1の欠点

T1はシングルプロセッサの[マザーボード](https://ja.wikipedia.org/wiki/マザーボード "wikilink")のみしかサポートしておらず、大規模のエンタープライズ環境での垂直方向のスケーラビリティが限定されている。サンは後継の[Victoria Falls プロセッサでこの問題を解決することを表明した](https://ja.wikipedia.org/wiki/#UltraSPARC_T2_Plus_プロセッサ "wikilink")。\[5\]また、1個の浮動小数点演算器が全てのコアで共有されているため、科学技術計算などの浮動小数点演算を多用するような用途には向かない。さらに、整数演算に限ってみても、同時代の他のCPUと比較して各コアのシングルスレッド性能はあまり高くはないという欠点がある。

## "Rock" プロセッサ

UltraSPARC T1はシングル CPU システムのみを対象として設計されており、SMPで使用できない。Rockなどの将来のサンのチップ・マルチスレッディング (Chip multithreading; CMT) 対応 UltraSPARCプロセッサは、複数チップのサーバアーキテクチャに対応する。Rockプロセッサはデータベースのような伝統的なデータ処理のワークロードを対象としている。従って、Rock UltraSPARC T1やT2の置き換えではなく、[UltraSPARC IVなどのサンの](https://ja.wikipedia.org/wiki/UltraSPARC_IV "wikilink") SMPプロセッサの後継とみなされている。

RockはUltraSPARC T1と異なり、浮動小数点の処理を対象としている。サンは公式に*[hardware scout](https://ja.wikipedia.org/wiki/:en:hardware_scout "wikilink")*と呼ばれる、Rockプロセッサのマルチスレッドのハードウェアを[プリフェッチ](https://ja.wikipedia.org/wiki/プリフェッチ "wikilink")に用いる機能を公開している。これは[アウト・オブ・オーダー実行](../Page/アウト・オブ・オーダー実行.md "wikilink")の機能の一部である。

## UltraSPARC T2 プロセッサ

コードネーム*Niagara 2*として知られた、UltraSPARC T1の後継となるプロセッサは、コアあたり8スレッドをサポートし、各コアが専用のFPUを持っている。つまり8コア/プロセッサ×8スレッド/コア=64スレッドを同時実行可能である。

## UltraSPARC T2 Plus プロセッサ

2007年2月、サンは年次のアナリストサミットにおいて、"Victoria Falls" というコードネームの第3世代[ハードウェアマルチスレッディング](https://ja.wikipedia.org/wiki/ハードウェアマルチスレッディング "wikilink")設計\[6\]のプロセッサが、2006年10月に[テープアウト](https://ja.wikipedia.org/wiki/テープアウト "wikilink")したことを発表した。2ソケットのサーバ (2[U](https://ja.wikipedia.org/wiki/19インチラック "wikilink")) は128スレッド、16コア、を備え、UltraSPARC III に対して65倍高い性能を持っている \[7\]。

HOT CHIPS 19カンファレンスにおいて、サンはVictoria Fallsが2-wayおよび4-wayになることを発表した。従って、1台の4-way SMPサーバは同時に256のハードウェアスレッドをサポートする \[8\]。

2008年04月09日、サンと富士通はVictoria Fallsのコードネームで知られる「UltraSPARC T2 Plus」を搭載した2CPU型サーバ「SPARC Enterprise T5140」と「SPARC Enterprise T5240」を発表した。T5140は1U、T5240は2Uのサーバ筐体である。出荷開始は、2008年4月中旬を予定\[9\]\[10\]。

## SPARC T3 プロセッサ

2010年に最大クロック数1.67 GHz、16コア、1コアあたり8スレッド（システム全体で最大512スレッド）の処理性能をもつCPUとしてリリースされた。12種類の暗号をサポートした暗号化処理ユニットが組み込まれている。

## SPARC T4 プロセッサ

2011年リリース。前世代のSPARC T3と比較してコア数が半分の8コアになり、ワンチップあたりのスレッド実行数が64スレッドに減少しているが、SPARC Tシリーズとして初のアウトオブオーダ実行を実装し､シングルスレッドのパフォーマンスが前世代の5倍に向上。最大3.0 GHz、1コアあたり8スレッドの処理性能をもつ。16種類の暗号をサポートした暗号化処理ユニット、10GbEによる高速ネットワーキング機能などを組み込んだSoCとしてリリースされた。

## SPARC T5 プロセッサ

2013年 4月リリース。コアのあたりのスレッド数は、SPARC T4 と同じ8だが、コア数が倍の16コアとなり、28 nmプロセスで製造されている\[11\]\[12\]\[13\]。

## オープンな設計

2006年3月21日、サンはUltraSPARC T1 プロセッサの設計を、[GNU General Public Licenseの元で](../Page/GNU_General_Public_License.md "wikilink")、[OpenSPARC](https://ja.wikipedia.org/wiki/OpenSPARC "wikilink")プロジェクトにより公開した。公開された情報には、下記のものが含まれる：

  - UltraSPARC T1設計の[Verilog](https://ja.wikipedia.org/wiki/Verilog "wikilink") ソースコード
  - 検証ツールスイートおよびシミュレーションモデル
  - ISA仕様 (UltraSPARC Architecture 2005)
  - [Solaris](../Page/Solaris.md "wikilink") 10 OSシミュレーションイメージ

## 参考文献

## 外部リンク

  - [Sun Microsystems' official UltraSPARC T1 Processor information](http://www.sun.com/processors/UltraSPARC-T1/)（英語）
  - [サンの OpenSPARC ホームページ](http://www.opensparc.net/)（英語）
  - [OpenSPARC T1 Project home](http://opensparc-t1.sunsource.net/)（英語）
  - [Sun Intros Eight-Core Processor](http://www.reed-electronics.com/electronicnews/article/CA6283640.html) – By Jessica Davis, Electronic News, 14 Nov 2005（英語）
  - [Sun’s Big Splash](http://ogun.stanford.edu/~kunle/publications/niagra_spectrum.pdf) by Linda Geppert, in IEEE Spectrum, January 2005 (英語)
  - [Niagara, a 32-way Multithreaded Sparc Processor](http://ogun.stanford.edu/~kunle/publications/niagra_micro.pdf) by Poonacha Kongetira, Kathirgamar Aingaran, Kunle Olukotun, in IEEE Micro, March-April 2005（英語）
  - [Sun Talks About Victoria Falls](http://www.sun.com/emrkt/innercircle/rss/0407feature.html?cid=222961/) （英語）
  - [Sun PDF Which Includes Victoria Falls Info](http://www.sun.com/processors/UltraSPARC-T2/datasheet.pdf) （英語）

[Category:サン・マイクロシステムズのマイクロプロセッサ](https://ja.wikipedia.org/wiki/Category:サン・マイクロシステムズのマイクロプロセッサ "wikilink") [Category:オープンソースハードウェア](https://ja.wikipedia.org/wiki/Category:オープンソースハードウェア "wikilink")

1.
2.
3.
4.
5.
6.  [同時マルチスレッディング](https://ja.wikipedia.org/wiki/同時マルチスレッディング "wikilink") (Simultaneous Multithreading; SMT) とする誤りが観られるが、NiagaraファミリーとVictoria Fallsは[バレルプロセッサ](https://ja.wikipedia.org/wiki/バレルプロセッサ "wikilink")であるので[ハードウェアマルチスレッディング](https://ja.wikipedia.org/wiki/ハードウェアマルチスレッディング "wikilink")ではあるが、SMTではない。
7.
8.
9.
10.
11.
12. [次世代SPARCプロセッサ「SPARC T5」と「SPARC64 X」](http://pc.watch.impress.co.jp/docs/news/event/20130220_588377.html)
13.
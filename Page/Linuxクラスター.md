> この記事は[Linuxクラスター](https://ja.wikipedia.org/wiki/Linuxクラスター)から翻訳されています。


**Linuxクラスター**（リナックスクラスター）は、[Linux](../Page/Linux.md "wikilink")を利用している[コンピュータ・クラスター](../Page/コンピュータ・クラスター.md "wikilink")である。一般に[疎結合クラスター](https://ja.wikipedia.org/wiki/疎結合クラスター "wikilink")で、[対称型マルチプロセッシング](../Page/対称型マルチプロセッシング.md "wikilink") (SMP) が、CPUとメモリをより密に繋いでいるのに比べると、クラスターの結合は疎である。クラスターの各要素は、完全に独立したコンピュータとして動作しており、高速なLANなどを利用してお互いに接続されている。

要素となるマシンは[Linux](../Page/Linux.md "wikilink")ないし[GNU/Linuxシステム](https://ja.wikipedia.org/wiki/GNU/Linuxシステム "wikilink")を搭載した[コンピュータ](../Page/コンピュータ.md "wikilink")である。

[Linux](../Page/Linux.md "wikilink")を動作させるために必要な[ハードウェア](../Page/ハードウェア.md "wikilink")は、ごく一般的な[パーソナルコンピュータ](../Page/パーソナルコンピュータ.md "wikilink")でよいため、手軽に[スーパーコンピュータ](../Page/スーパーコンピュータ.md "wikilink")を作り始められることが特徴である。また、Linuxはスケーラビリティに優れ、高速のコンピュータ上でも動いている。このため、低速な環境でシステムを構築してから、徐々に高速なコンピュータ環境に向かって進化させることが出来る。

また、各コンピュータを繋ぐのには標準的な[LANを使っているため](../Page/Local_Area_Network.md "wikilink")、接続のハードウェアや技術、[ソフトウェア](../Page/ソフトウェア.md "wikilink")は、従来の物を使うことが出来る。ハードウェアの製作やメンテナンスに特別な部品や技術を使う必要はない。

Linuxは、[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink") (OS) の[ソースコード](../Page/ソースコード.md "wikilink")を始め全ての必要なソフトウェアをソースコードも含めて無料で手にいれることができる。そのため、利用者や研究者が必要に応じてあらゆる部分に手を加えることが出来るのが大きな特徴である。また、使用に当たってコンピュータ毎に支払うOSの[ライセンス料](https://ja.wikipedia.org/wiki/ライセンス料 "wikilink")もない。したがって投資に必要なのはハードウェアなどの物理的な資源と人件費だけということになる。参照：[フリーソフトウェア](../Page/フリーソフトウェア.md "wikilink")、[コピーレフト](../Page/コピーレフト.md "wikilink")なソフトウェア。

## クラスターの目的

Linuxクラスターを作る目的としては、

  - 高速な計算処理
  - 大量の処理要求への対応
  - 安定性や信頼性

などの場合があり、目的に応じて使われる技法も異なる。

### 高速な計算処理を目的とする場合

ごく普通の[パーソナルコンピュータ](../Page/パーソナルコンピュータ.md "wikilink")を多数(場合によっては数百から数千)、高速の[ネットワークで繋いで](../Page/コンピュータネットワーク.md "wikilink")、いわゆる[スーパーコンピュータ](../Page/スーパーコンピュータ.md "wikilink")としての性能を出せることから、場合によっては通常のスーパーコンピュータの性能を10分の1以下の予算で作ることができる。また、研究者が自分達でも作れることから結構流行した。

[マイクロプロセッサ](../Page/マイクロプロセッサ.md "wikilink")の進歩により高速のコンピュータが作られ、高速の[イーサネット](../Page/イーサネット.md "wikilink")によりごく一般的なネットワークの手法でコンピュータ間を接続できることが、Linuxクラスターをもたらした。また、高速のイーサネットを更に複数並行して接続し更に高速なLANを構築する技法も完成されている。現状では転送速度が[ギガ](../Page/ギガ.md "wikilink")ビット/秒のイーサネットが使われることが多い。

非常に高速な処理をする専用のクラスターを構成する場合は、以下の例で示す [Beowulf](../Page/Beowulf.md "wikilink") の技法を使って実現されることが多い。

要素になるコンピュータを個人用のデスクトップや他の目的のサーバにも使い、その余剰の計算能力をお互いにわかちあうような場合には、以下の例で示す [MOSIX](https://ja.wikipedia.org/wiki/MOSIX "wikilink") を使う場合がある。

### 大量の要求への対応を目的とする場合

[ウェブサーバなど](../Page/Webサーバ.md "wikilink")、[インターネット](../Page/インターネット.md "wikilink")全体から大量の要求が同時に発生し、秒のオーダーで結果を返す必要がある。

このための技法には多くの例がある。以下の例で述べる [MOSIX](https://ja.wikipedia.org/wiki/MOSIX "wikilink") もその目的で使うことが出来る。

ちなみに、世界最大の[コンピュータ・クラスター](../Page/コンピュータ・クラスター.md "wikilink")を保有すると言われている[インターネット](../Page/インターネット.md "wikilink")の[検索エンジン](../Page/検索エンジン.md "wikilink")の[グーグルは](../Page/Google.md "wikilink")、Linuxクラスターでできている。[Googleのコンピュータ・クラスター](https://ja.wikipedia.org/wiki/Googleのコンピュータ・クラスター "wikilink")を参照。

### 安定性や信頼性を目的とする場合

この場合は、複数のコンピュータが同じ処理をして、結果を比較しあって異常な結果が出ることを防いだり、通常は別の処理をしているコンピュータの集合から一台が異常になっても、自動的に他の残りのコンピュータが処理を補うような場合である。

  -
    この章は全くのスタブです。

## Linuxクラスターの作り方

普通の[パーソナルコンピュータ](../Page/パーソナルコンピュータ.md "wikilink")で作ることができ、必要な[ソフトウェア](../Page/ソフトウェア.md "wikilink")は[ソースコード](../Page/ソースコード.md "wikilink")も含めて全て無料で手に入り、作るのに必要な情報はほとんど[ウェブ上で即座に無料で手にいれることが出来る](../Page/World_Wide_Web.md "wikilink")[フリーソフトウェア](../Page/フリーソフトウェア.md "wikilink")または[コピーレフト](../Page/コピーレフト.md "wikilink")のソフトウェアである。

実際に[ハードウェア](../Page/ハードウェア.md "wikilink")を使って作る場合と、クラスター用ソフトウェアの構築や開発のために[仮想コンピュータ上に構築する場合がある](../Page/仮想機械.md "wikilink")。

### 実ハードウェア上の構築

  -

    この章は全くのスタブです。

### 仮想コンピュータ上の構築

単にソフトウェアの構築の実験や開発をするだけなら、Linux用の[仮想コンピュータを利用できる](../Page/仮想機械.md "wikilink")。仮想コンピュータは一台の実際に存在するコンピュータを使って、その中に複数のコンピュータを作り出すことが出来る。利用する側から見ると(感じると)全く複数のコンピュータが存在するように見える。実際のコンピュータの資源が許す限り何台でも仮想コンピュータを作ることが出来る。

また、特に[i386系の](../Page/Intel_80386.md "wikilink")[Linux](../Page/Linux.md "wikilink")に限るならば、Linux上で複数の仮想のLinux環境を作り出すための[ソフトウェア](../Page/ソフトウェア.md "wikilink")が[カーネル](../Page/カーネル.md "wikilink")の一部を含め、[ユーザーモードLinux](https://ja.wikipedia.org/wiki/ユーザーモードLinux "wikilink") (UML - User Mode Linux)として提供されている。UMLの一部は既に一般のLinuxに含まれて配付されているため、UMLのソフトウェアを手にいれたら手間を必要とせずに即座に複数の仮想環境を用意することが出来る。UMLもやはり無料で[ソースコード](../Page/ソースコード.md "wikilink")を手にいれることができる。

また、[VMware](../Page/VMware.md "wikilink")など商用の[仮想機械](../Page/仮想機械.md "wikilink")ソフトウェアも用意されている。

以下の例の中に構成するのに必要なソフトウェアや手順が紹介されているので、UML上でクラスターの構築の実験が出来る。(作ったらレポートは[ウィキペディア日本語版](../Page/ウィキペディア日本語版.md "wikilink")に報告されるのが標準的な方法だと主張される場合もある)。

## 使用するソフトウェアや技法の例

  - [Beowulf](../Page/Beowulf.md "wikilink")（方式）:Linuxを使った[コンピュータ・クラスター](../Page/コンピュータ・クラスター.md "wikilink")として有名。[Linux](../Page/Linux.md "wikilink")以外の[カーネル](../Page/カーネル.md "wikilink")の[ソースコード](../Page/ソースコード.md "wikilink")が公開されているフリーの[UNIX](../Page/UNIX.md "wikilink")でも作られる。クラスターを構成する[コンピュータ](../Page/コンピュータ.md "wikilink")はクラスターとしての処理だけに使われる。各コンピュータは高速の専用のネットワークで接続される。"Beowulf"と呼ばれるソフトウェアパッケージはなく、Beowulfを構成するに当たってそれぞれ使うソフトウェアは異なり特に必要な要素となるソフトウエアの部品はない。[1](http://www.beowulf.org/)

<!-- end list -->

  - bproc (Beowulf Distributed Process Space) \[[http://bproc.sourceforge.net/\]Beowulfクラスター上でリモートプロセスを起動するためのツール群。マスターノード上で起動された](http://bproc.sourceforge.net/%5DBeowulfクラスター上でリモートプロセスを起動するためのツール群。マスターノード上で起動された)[プロセス](../Page/プロセス.md "wikilink")がVMADumpによりスレーブノードにコピーされる。スレーブノードはカーネルと必要最小限の[ライブラリ](../Page/ライブラリ.md "wikilink")のみをブート時にダウンロードするディスクレス構成。[NASAのBeowulfプロジェクトで開発され](../Page/アメリカ航空宇宙局.md "wikilink")、現在はロスアラモス国立研究所のクラスターPink（2048CPU）\[[http://www.lanl.gov/projects/pink/\]にも採用されている](http://www.lanl.gov/projects/pink/%5Dにも採用されている)。

<!-- end list -->

  - [SCore](https://ja.wikipedia.org/wiki/SCore "wikilink")（方式/ソフトウェア）:BeowulfがアメリカのNASA主導で策定され、検証された方式/プロジェクトであった様に、1992年から[通商産業省](https://ja.wikipedia.org/wiki/通商産業省 "wikilink")主導による[新情報処理開発機構](https://ja.wikipedia.org/wiki/新情報処理開発機構 "wikilink")(RWCP)にて開発されたクラスター計算機用超並列プログラム実行環境を含むクラスター方式。
    [MOSIX](https://ja.wikipedia.org/wiki/MOSIX "wikilink")（ソフトウェアパッケージ）:Beowulfクラスターではない。一般の[デスクトップコンピュータ](https://ja.wikipedia.org/wiki/デスクトップコンピュータ "wikilink")も時間を制限してクラスターの一部として参加させることが出来る。プロセス単位で走る通常のLinux用ソフトウェアを改造なしてクラスター上で処理させることが出来る。参加するコンピュータは[x86](https://ja.wikipedia.org/wiki/x86 "wikilink")系のCPUを使っていれば、まちまちの仕様のコンピュータでも構わない。[スレッドレベルの処理はサポートしていない](../Page/スレッド_\(コンピュータ\).md "wikilink")。[2](http://www.mosix.org/)
    [グリッド・コンピューティング](../Page/グリッド・コンピューティング.md "wikilink"):[インターネット](../Page/インターネット.md "wikilink")などの広域で共有された[ネットワーク上でコンピュータ資源](../Page/コンピュータネットワーク.md "wikilink")(処理能力、記憶能力)を共有する仕組み。模索中であるが、商用のサービスが行われ始めている。[Globus](../Page/Globus.md "wikilink")ツールキットが事実上の標準になりつつある。特に[Linux](../Page/Linux.md "wikilink")とは限定していない。

## 関連項目

  - [スーパーコンピュータ](../Page/スーパーコンピュータ.md "wikilink")
  - [並列コンピュータ](https://ja.wikipedia.org/wiki/並列コンピュータ "wikilink")
  - [コンピュータ・クラスター](../Page/コンピュータ・クラスター.md "wikilink")

## 外部リンク

  - [連載記事 Linuxクラスタリングへの招待（@IT）](http://www.atmarkit.co.jp/flinux/index/indexfiles/clusterindex.html)

[Category:Linux](https://ja.wikipedia.org/wiki/Category:Linux "wikilink") [Category:スーパーコンピュータ](https://ja.wikipedia.org/wiki/Category:スーパーコンピュータ "wikilink")
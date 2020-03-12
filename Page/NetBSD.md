> この記事は[NetBSD](https://ja.wikipedia.org/wiki/NetBSD)から翻訳されています。


**NetBSD**（ネットビーエスディー）は、[UNIXライクな](../Page/Unix系.md "wikilink")[オープンソース](../Page/オープンソース.md "wikilink")の[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink")である。[FreeBSD](../Page/FreeBSD.md "wikilink")や[OpenBSD](../Page/OpenBSD.md "wikilink")と同じく[BSDの子孫](../Page/BSDの子孫.md "wikilink")の1つである。近代的な[オープンソース](../Page/オープンソース.md "wikilink")[BSD](../Page/BSD.md "wikilink")としては最も古く、[1993年](../Page/1993年.md "wikilink")5月に最初の公式リリースである0.8が公開された。

## 特徴

NetBSDは、幅広い[アーキテクチャに対して移植されている](../Page/コンピュータ・アーキテクチャ.md "wikilink")。このことは、NetBSDの標語である "Of course it runs NetBSD." にも表れている。単一のソースツリーから、58以上のアーキテクチャに対してバイナリが構築可能である。ソースツリーは機種依存部分と機種独立部分を可能な限り分離するように構成されている。これにより、機種独立部分に追加された機能は、全てのアーキテクチャで利用可能となり、再移植が不要である。[ドライバの開発も機種独立である](../Page/デバイスドライバ.md "wikilink")。あるPCIカード向けに書かれたドライバは、[80386](../Page/Intel_80386.md "wikilink")、[Alpha](https://ja.wikipedia.org/wiki/DEC_Alpha "wikilink")、[PowerPC](../Page/PowerPC.md "wikilink")、[SPARC](../Page/SPARC.md "wikilink")など[PCI バスを備えたアーキテクチャであればどれでも使うことができる](../Page/Peripheral_Component_Interconnect.md "wikilink")。それ以外にも、[PCI Expressや](../Page/PCI_Express.md "wikilink")[USB等も同様にアーキテクチャに関係なく実装される](../Page/ユニバーサル・シリアル・バス.md "wikilink")。この機種独立性が、[組み込みシステム](../Page/組み込みシステム.md "wikilink")での開発に大きく寄与している。[コンパイラ](../Page/コンパイラ.md "wikilink")、[アセンブラ](../Page/アセンブリ言語.md "wikilink")、[リンカその他の](../Page/リンケージエディタ.md "wikilink")、[クロスコンパイルに完全対応した](../Page/クロスコンパイラ.md "wikilink")[ツールチェーン](https://ja.wikipedia.org/wiki/ツールチェーン "wikilink")一式を持つNetBSD 1.6以降では、特に顕著である。

"NETBSD"は、[2004年](../Page/2004年.md "wikilink")[4月20日](https://ja.wikipedia.org/wiki/4月20日 "wikilink")をもって、The NetBSD Foundationの登録商標となっている。

## 歴史

NetBSDは[カリフォルニア大学バークレー校](../Page/カリフォルニア大学バークレー校.md "wikilink")の[Computer Systems Research Group](../Page/Computer_Systems_Research_Group.md "wikilink") がリリースした4.3BSDから、Networking/2、および[386BSD](../Page/386BSD.md "wikilink")を介して派生したものである。NetBSDプロジェクトは、386BSDの開発者コミュニティ内の開発のペースや方向性に対する不満から始まった。四人のNetBSDプロジェクトの創始者Chris Demetriou、[テオ・デ・ラート](../Page/テオ・デ・ラート.md "wikilink")、Adam Glass、Charles Hannumは、移植性、きれいで正確なコードを軸とした開かれた開発モデルがプロジェクトに有益であると感じていた。彼らの目的は、統一された、マルチプラットフォームの、製品レベルの品質を持ったBSDベースのオペレーティングシステムを作り出すことであった。"NetBSD"の名称は[インターネット](../Page/インターネット.md "wikilink")などの当時の急速に発展していたネットワークの重要性と、開発が分散した環境で共同で行われるというプロジェクトの性質からラートが提案したものである。

NetBSDのソースコードリポジトリは1993年3月21日に設立され、最初の公式リリースNetBSD 0.8は1993年4月に行われた。このときのコードは386BSD 0.1にバージョン0.2.2の非公式のパッチをあて、386BSDに不足していたいくつかのプログラムをNet/2リリースから再統合し、そのほかいくつかの改良が含まれていた。最初のマルチプラットフォームのリリースNetBSD 1.0は1994年10月に行われた。同年暮れ、創設者の一人テオ・デ・ラートがプロジェクトから追われることとなった。彼は1995年の終わりごろ、NetBSD 1.0のコードからフォークした新しいプロジェクト[OpenBSD](../Page/OpenBSD.md "wikilink")を立ち上げた。1998年、NetBSD 1.3で[pkgsrc](https://ja.wikipedia.org/wiki/pkgsrc "wikilink")パッケージコレクションが導入された。

## 対称マルチプロセッシング

NetBSDは[対称型マルチプロセッシング](../Page/対称型マルチプロセッシング.md "wikilink")(SMP)を2004年リリースのNetBSD 2.0よりサポートしており\[1\]、初期の実装は[ジャイアントロック](https://ja.wikipedia.org/wiki/ジャイアントロック "wikilink")を用いた方法であった。NetBSD 5のリリースに向けた開発サイクルで、SMPのサポートを改善する主要な作業が完了した。カーネルサブシステムの大半の部分がマルチプロセッサでも安全になり、[細粒度のロックを用いるよう修正された](https://ja.wikipedia.org/wiki/fine-grained_locking "wikilink")。新しい[同期機構が導入され](../Page/同期_\(計算機科学\).md "wikilink")、2007年2月に[Scheduler activationsが](https://ja.wikipedia.org/wiki/Scheduler_activations "wikilink")[1:1スレッドモデルに置き換えられた](../Page/スレッド_\(コンピュータ\).md "wikilink")\[2\]。スケーラブルなM2スレッドスケジューラが実装されたが、4.4 BSDのスケジューラがデフォルトで使用されている（これもSMPでスケールするよう変更された）。同期化の性能を向上させるため、スレッド化された[割り込みが実装された](../Page/割り込み_\(コンピュータ\).md "wikilink")。[仮想メモリシステム](../Page/仮想記憶.md "wikilink")、[メモリ割り当て](https://ja.wikipedia.org/wiki/メモリ割り当て "wikilink")、[例外ハンドリング](https://ja.wikipedia.org/wiki/例外ハンドリング "wikilink")がマルチプロセッサでも安全になり、[仮想ファイルシステム](../Page/仮想ファイルシステム.md "wikilink")および主要な[ファイルシステム](../Page/ファイルシステム.md "wikilink")を含むファイルシステムフレームワークもマルチプロセッサ対応になった。2008年4月以降、ジャイアントロックで動作しているのは[ネットワークプロトコル](https://ja.wikipedia.org/wiki/ネットワークプロトコル "wikilink")と大半の[デバイスドライバ](../Page/デバイスドライバ.md "wikilink")のみとなっている。

## バージョンについて

### 最新のバージョン

[2020年](../Page/2020年.md "wikilink")[2月14日](../Page/2月14日.md "wikilink")現在、NetBSD の最新リリース版は9.0である。

### これまでのリリース

  - 2020年
      - 2月14日 - NetBSD 9.0

<!-- end list -->

  - 2019年
      - 5月31日 - NetBSD 8.1

<!-- end list -->

  - 2018年
      - 8月29日 - NetBSD 7.2
      - 7月17日 - NetBSD 8.0
      - 3月15日 - NetBSD 7.1.2

<!-- end list -->

  - 2017年
      - 12月22日 - NetBSD 7.1.1
      - 3月11日 - NetBSD 7.1

<!-- end list -->

  - 2016年
      - 10月21日 - NetBSD 7.0.2
      - 5月28日 - NetBSD 7.0.1

<!-- end list -->

  - 2015年
      - 9月25日 - NetBSD 7.0.0
  - 2014年
      - 11月15日 - NetBSD 5.1.5
      - 11月15日 - NetBSD 5.2.3
      - 9月22日 - NetBSD 6.1.5
      - 9月22日 - NetBSD 6.0.6
      - 4月12日 - NetBSD 6.1.4
      - 4月12日 - NetBSD 6.0.5
      - 1月27日 - NetBSD 6.1.3
      - 1月27日 - NetBSD 6.0.4
      - 1月27日 - NetBSD 5.2.2
      - 1月27日 - NetBSD 5.1.4
  - 2013年
      - 9月30日 - NetBSD 6.1.2
      - 9月30日 - NetBSD 6.0.3
      - 8月22日 - NetBSD 6.1.1
      - 5月18日 - NetBSD 6.1
      - 5月18日 - NetBSD 6.0.2
  - 2012年
      - 12月26日 - NetBSD 6.0.1
      - 12月3日 - NetBSD 5.2
      - 10月17日 - NetBSD 6.0
      - 2月11日 - NetBSD 5.1.2 （5.1.1はリリースされなかった。\[3\]）
  - 2010年
      - 11月19日 - NetBSD 5.1
      - 2月12日 - NetBSD 5.0.2
  - 2009年
      - 8月2日 - NetBSD 5.0.1
      - 4月29日 - NetBSD 5.0
  - 2008年
      - 10月14日 - NetBSD 4.0.1
  - 2007年
      - 12月19日 - NetBSD 4.0
  - 2006年
      - 11月4日 - NetBSD 3.1
      - 11月4日 - NetBSD 3.0.2
      - 7月24日 - NetBSD 3.0.1
  - 2005年
      - 12月23日 - NetBSD 3.0
      - 11月2日 - NetBSD 2.1
      - 10月31日 - NetBSD 2.0.3
      - 4月14日 - NetBSD 2.0.2 （2.0.1はサーバトラブルのためリリースされなかった。）
  - 2004年
      - 12月9日 - NetBSD 2.0
      - 3月1日 - NetBSD 1.6.2
  - 2003年
      - 4月21日 - NetBSD 1.6.1
  - 2002年
      - 9月14日 - NetBSD 1.6
      - 7月22日 - NetBSD 1.5.3
  - 2001年
      - 9月13日 - NetBSD 1.5.2
      - 7月11日 - NetBSD 1.5.1
  - 2000年
      - 12月6日 - NetBSD 1.5
      - 11月25日 - NetBSD 1.4.3
      - 3月19日 - NetBSD 1.4.2
  - 1999年
      - 8月26日 - NetBSD 1.4.1
      - 5月12日 - NetBSD 1.4
  - 1998年
      - 12月23日 - NetBSD 1.3.3
      - 5月29日 - NetBSD 1.3.2
      - 3月9日 - NetBSD 1.3.1
      - 1月4日 - NetBSD 1.3
  - 1997年
      - 5月20日 - NetBSD 1.2.1
  - 1996年
      - 10月4日 - NetBSD 1.2
  - 1995年
      - 11月26日 - NetBSD 1.1
  - 1994年
      - 10月26日 - NetBSD 1.0
  - 1993年
      - 8月23日 - NetBSD 0.9
      - 4月20日 - NetBSD 0.8

## 対応機種

### ポート

  - acorn26
  - acorn32
  - algor
  - alpha
  - amd64
  - amiga
  - amigappc
  - arc
  - atari
  - bebox
  - cats
  - cesfic
  - cobalt
  - dreamcast
  - emips
  - epoc32
  - evbarm
  - evbmips
  - evbppc
  - evbsh3
  - ews4800mips
  - hp300
  - hp700
  - hpcarm
  - hpcmips
  - hpcsh
  - i386
  - ia64
  - ibmnws
  - iyonix
  - landisk
  - luna68k
  - mac68k
  - macppc
  - mipsco
  - mmeye
  - mvme68k
  - mvmeppc
  - netwinder
  - news68k
  - newsmips
  - next68k
  - ofppc
  - pmax
  - prep
  - rs6000
  - sandpoint
  - sbmips
  - sgimips
  - shark
  - sparc
  - sparc64
  - sun2
  - sun3
  - vax
  - x68k
  - xen
  - zaurus

## 関連プロジェクト

### pkgsrc

NetBSDには、独自の[サードパーティー](../Page/サードパーティー.md "wikilink")ソフトウェア集、NetBSD Packages Collection （別名[pkgsrc](https://ja.wikipedia.org/wiki/pkgsrc "wikilink")）がある。[2009年](../Page/2009年.md "wikilink")7月現在、8,000を超えるパッケージが用意されている。

[GNOME](../Page/GNOME.md "wikilink")、[KDE](../Page/KDE.md "wikilink")、[Apache HTTP Serverや](../Page/Apache_HTTP_Server.md "wikilink")[Perl](../Page/Perl.md "wikilink")等をインストールするには、適切なディレクトリに移動して"make install"とタイプするだけである。こうすると、ソースの取り寄せ、展開、configure、構築や、後で削除可能な形でのパッケージのインストールを自動的に行ってくれる。このようなコンパイルを行うかわりに、あらかじめ構築されたバイナリパッケージを使うこともできる。どちらを使うにせよ、事前準備や依存するパッケージのインストールは、パッケージシステムによりすべて自動で行われ、手動での調整は必要ない。

移植性の教義に従い、NetBSD Packages Collection (pkgsrc)は、[Linux](../Page/Linux.md "wikilink")、FreeBSD、OpenBSD、[Solaris](../Page/Solaris.md "wikilink")、[Darwin](../Page/Darwin_\(オペレーティングシステム\).md "wikilink")/[macOS](https://ja.wikipedia.org/wiki/macOS "wikilink")、[IRIX](../Page/IRIX.md "wikilink")、[Interix](https://ja.wikipedia.org/wiki/Interix "wikilink") (Windows Services for UNIX) など、NetBSD以外の多くのオペレーティングシステムに移植されている。

[DragonFly BSDでは標準のパッケージシステムをpkgsrcに変更した](../Page/DragonFly_BSD.md "wikilink")。

## 使用例

[thumbによる](https://ja.wikipedia.org/wiki/ファイル:ISS_on_20_August_2001.jpg "wikilink")[国際宇宙ステーション](../Page/国際宇宙ステーション.md "wikilink")の微小重力を調査するプロジェクトで使用され、また[人工衛星](https://ja.wikipedia.org/wiki/人工衛星 "wikilink")ネットワークにおける[TCPの利用に関する研究にも使用された](../Page/Transmission_Control_Protocol.md "wikilink")\]\]

NetBSD のきれいな設計、高い性能とスケーラビリティ、幅広いアーキテクチャのサポートは組み込み機器やサーバー、特にネットワークや工業用途に適している。

商用の[リアルタイムオペレーティングシステム](../Page/リアルタイムオペレーティングシステム.md "wikilink")[QNX](../Page/QNX.md "wikilink")は、NetBSDのコードから派生したネットワークスタックを使用しており\[4\]、デバイスドライバも NetBSD から多数ポートされている\[5\]。

[フォーステンネットワークス](../Page/フォーステンネットワークス.md "wikilink")はNetBSDを高スケーラビリティのルーターで用いられるFTOS(Force10 Operating System)の基盤OSとして使用している\[6\]。フォーステンはまた2007年、NetBSD財団の更なる発展とオープンな開発コミュニティを助けるため寄付を行っている\[7\]。

[Wasabi Systemsは](https://ja.wikipedia.org/wiki/Wasabi_Systems "wikilink")、組み込みのサーバーやストレージ機器への応用に焦点を置いてNetBSDに商用のエンタープライズ向けの機能拡張を行ったWasabi Certified BSDを提供している\[8\]。

NetBSDは[NASAによる](../Page/アメリカ航空宇宙局.md "wikilink")[国際宇宙ステーション](../Page/国際宇宙ステーション.md "wikilink")の微小重力を調査するプロジェクトで使用され、また[人工衛星](https://ja.wikipedia.org/wiki/人工衛星 "wikilink")ネットワークにおける[TCPの利用に関する研究にも使用された](../Page/Transmission_Control_Protocol.md "wikilink")\[9\]。

2004年には、[SUNET](https://ja.wikipedia.org/wiki/SUNET "wikilink")がNetBSDを用いて[Internet2](../Page/Internet2.md "wikilink")の地上における最高速記録を樹立している。このときNetBSDが選定された理由は「TCPコードのスケーラビリティ」である\[10\]。

[T-Mobile Sidekick](https://ja.wikipedia.org/wiki/T-Mobile_Sidekick "wikilink") LX 2009[スマートフォン](https://ja.wikipedia.org/wiki/スマートフォン "wikilink")のオペレーティングシステムはNetBSDを元にしたものである\[11\]。

## 関連項目

  - [BSDの子孫](../Page/BSDの子孫.md "wikilink")
  - [DragonFly BSD](../Page/DragonFly_BSD.md "wikilink")
  - [FreeBSD](../Page/FreeBSD.md "wikilink")
  - [OpenBSD](../Page/OpenBSD.md "wikilink")
  - [macOS](https://ja.wikipedia.org/wiki/macOS "wikilink")

## 外部リンク

  - [オフィシャルページ](http://www.NetBSD.org/)
  - [Japan NetBSD Users' Group](http://www.jp.NetBSD.org/ja/JP/)
  - [Jibbed](http://www.jibbed.org/) LiveCD

## 参考文献

[Category:NetBSD](https://ja.wikipedia.org/wiki/Category:NetBSD "wikilink") [Category:BSD](https://ja.wikipedia.org/wiki/Category:BSD "wikilink") [Category:オープンソースソフトウェア](https://ja.wikipedia.org/wiki/Category:オープンソースソフトウェア "wikilink") [Category:1993年のソフトウェア](https://ja.wikipedia.org/wiki/Category:1993年のソフトウェア "wikilink")

1.
2.
3.
4.
5.
6.
7.
8.
9.
10.
11.
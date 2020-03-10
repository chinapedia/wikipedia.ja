> この記事は[Linux Standard Base](https://ja.wikipedia.org/wiki/Linux_Standard_Base)から翻訳されています。


[Linux_kernel_interfaces.svg](https://ja.wikipedia.org/wiki/File:Linux_kernel_interfaces.svg "fig:Linux_kernel_interfaces.svg") **Linux Standard Base** (**LSB**) は、複数の[Linuxディストリビューション](../Page/Linuxディストリビューション.md "wikilink")の共同プロジェクトであり、[Linux Foundationを活動母体として](https://ja.wikipedia.org/wiki/Linux_Foundation "wikilink")[Linux](https://ja.wikipedia.org/wiki/Linux "wikilink")系[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink")の内部構造の標準化を行うものである。LSBは[POSIX](../Page/POSIX.md "wikilink")仕様、[Single UNIX Specification](https://ja.wikipedia.org/wiki/Single_UNIX_Specification "wikilink")、その他いくつかのオープン標準に基づいて、特定の分野についてそれらを拡張している。

LSBの目標は次の通りである。

  -
    「LSBの目標は、Linuxディストリビューション間での互換性を向上させ、準拠システム上でのアプリケーションの動作を保証するよう標準規格を策定・振興することである。さらに、ソフトウェアベンダーがLinux向けに製品を移植したり開発する際の調整努力を助ける。」

LSB準拠製品の認証手続きが定められている。認証は[The Open GroupがLinux](../Page/The_Open_Group.md "wikilink") Foundationの協力の下に行う。なお、Linux Foundationは[Free Standards Groupと](https://ja.wikipedia.org/wiki/Free_Standards_Group "wikilink")[Open Source Development Labsが合併して誕生した](https://ja.wikipedia.org/wiki/Open_Source_Development_Labs "wikilink")。

LSBには以下のような点が規定されている。

  - [POSIX](../Page/POSIX.md "wikilink")標準を拡張した、標準[ライブラリ](../Page/ライブラリ.md "wikilink")とコマンド / ユーティリティ群
  - [ファイルシステム](../Page/ファイルシステム.md "wikilink")の階層構造のレイアウト
  - [ランレベル](https://ja.wikipedia.org/wiki/ランレベル "wikilink")の定義
  - [CUPSのようなスプーラーや](https://ja.wikipedia.org/wiki/Common_Unix_Printing_System "wikilink")[Foomatic](https://ja.wikipedia.org/wiki/Foomatic "wikilink")などのツールを含むプリンタシステム
  - [X Window Systemのいくつかの拡張](../Page/X_Window_System.md "wikilink")

## バージョン履歴

  - 1.0: 2001年6月 - 最初のリリース
  - 1.1: 2002年1月 - ハードウェア固有仕様の追加 ([IA-32](https://ja.wikipedia.org/wiki/IA-32 "wikilink"))
  - 1.2: 2002年6月 - ハードウェア固有仕様の追加（[PowerPC](../Page/PowerPC.md "wikilink") 32ビット）。認証は2002年7月から開始
  - 1.2.1: 2002年10月 - ハードウェア固有仕様の追加 ([Itanium](https://ja.wikipedia.org/wiki/Itanium "wikilink"))
  - 1.3: 2002年12月 - ハードウェア固有仕様の追加 (Itanium, Enterprise System Architecture/390, z/Architecture)
  - 2.0: 2004年9月 - モジュール化され、LSB-Core、LSB-CXX、LSB-Graphics、LSB-I18n（リリースされず）に分割。ハードウェア固有仕様の追加（PowerPC 64ビット、[AMD64](https://ja.wikipedia.org/wiki/x64 "wikilink")）。[Single UNIX Specification](https://ja.wikipedia.org/wiki/Single_UNIX_Specification "wikilink") (SUS) バージョン3との同期が行われた。
  - 2.0.1: LSB 2.0のISO版。全ハードウェア固有部分がマージされたもの（ただし、LSB-Grphics は汎用バージョンのみ）
  - 2.1: 2004年
  - 3.0: 2005年7月1日 - ライブラリAPIの更新。特にC++ ABIがgcc 3.4のものになった。中核部はISO POSIX (2003)、Technical Corrigenda 1:2005に基づくよう更新された。
  - 3.1: 2005年10月31日 - ISO/IEC 23360として提出された。
  - 3.2: 2008年1月28日 - ISO/IEC 23360として提出された。
  - 4.0: 2008年11月11日 -このバージョンでは以下の機能が含まれた。
      - [GNU Cライブラリ](https://ja.wikipedia.org/wiki/GNU_Cライブラリ "wikilink") version 2.4
      - LSB 3.xとのバイナリ互換性
      - SDKによる容易化
      - グラフィックライブラリ[GTK](https://ja.wikipedia.org/wiki/GTK "wikilink")と[Cairo](https://ja.wikipedia.org/wiki/Cairo "wikilink")の新しいバージョンのサポート
      - [Java](https://ja.wikipedia.org/wiki/Java "wikilink") (オプションモジュール)
      - LSB準拠のRPMパッケーシを容易に作成する方法
      - Crypto API (ネットワークセキュリティサービスライブラリ) (オプションモジュール)
  - 4.1: 2011年2月16日 -このバージョンでは以下の変更が行われた。
      - Javaの削除
      - LSB 4.0から推奨されてきたマルチメディア([ALSA](https://ja.wikipedia.org/wiki/ALSA "wikilink")), セキュリティ(NSS) そしてデスクトップ関連 (xdg-utils)のトライアルモジュールが必須サブモジュールとして奨励されるように。
      - [GTK+](https://ja.wikipedia.org/wiki/GTK+ "wikilink")、[Cairo](https://ja.wikipedia.org/wiki/Cairo "wikilink")と[CUPSライブラリの更新](https://ja.wikipedia.org/wiki/Common_Unix_Printing_System "wikilink")。
      - 3つの新しいテストスイーツの追加。
  - 5.0: 2015年6月2日 -このバージョンでは以下の変更が行われた。
      - 以前のバージョンとの下位互換性を失う初めてのメジャーリリース(LSB3との互換性、一部の例外を除けばLSB3.1以降とほぼ完全な互換性がある)。
      - [FHS](https://ja.wikipedia.org/wiki/Filesystem_Hierarchy_Standard "wikilink")3.0での変更を組み込む。
      - [Qt](https://ja.wikipedia.org/wiki/Qt "wikilink")3ライブラリの削除。
      - 進化したモジュール戦略。LSBはLSB Core、LSB Desktop, LSB Languages, LSB Imaging, and LSB Trial Useにモジュール化された。

## 後方互換性

LSBは、[バイナリ](../Page/バイナリ.md "wikilink")互換で安定したソフトウェアベンダから独立した[ABI](https://ja.wikipedia.org/wiki/ABI "wikilink")を作るよう設計されている。後方互換性を達成するために、それぞれのそれに続くバージョンは純粋に追加的なものとなっている。言い換えると、インターフェースは加えられるのみで、除去されない。LSBは、LSBからインターフェースが除去されるときのためにアプリケーション開発者に十分な時間を与えるため、インターフェース廃止ポリシーを適用している。

これは、開発者にLSB中の全てのインターフェースに頼ることを許し、驚きなしに変更を計画し、周知する時間のためのものである。インターフェースは、3つのメジャーバージョンか、約11年、"deprecated"とマークされた後にのみ除去される\[1\]。

LSB 5.0は、それ以前のバージョンとの後方互換性を壊した初めてのメジャーバージョンである\[2\]。

## 批判

LSBはメンバー企業以外（特に[Debian](../Page/Debian.md "wikilink")プロジェクト）からの入力を受け付けないことで批判されている。

例えば、LSBではソフトウェアパッケージの配布形式として LSB 準拠のインストーラか、制限された形態\[[http://refspecs.freestandards.org/LSB_3.1.0/LSB-Core-generic/LSB-Core-generic/pkgscripts.html\]の](http://refspecs.freestandards.org/LSB_3.1.0/LSB-Core-generic/LSB-Core-generic/pkgscripts.html%5Dの)[RPM形式を指定している](https://ja.wikipedia.org/wiki/RPM_Package_Manager "wikilink")[1](http://refspecs.freestandards.org/LSB_3.1.0/LSB-Core-generic/LSB-Core-generic/swinstall.html#SWINSTALL-INTRO)。DebianはRPMより以前から[debパッケージ形式を使っており](https://ja.wikipedia.org/wiki/deb_\(ファイルフォーマット\) "wikilink")、Debianの開発者はそのパッケージ形式がRPMより優れていて、LSBに準拠するためにパッケージ形式を変えるのは現実的でないと主張している。Debianのパッケージマネージャとパッケージ形式にはRPMには無い機能があり、逆にRPMにだけ存在する機能もある。従って、Debianのパッケージ形式をRPMにするのは簡単ではない。

これに対処するため、LSBではそのOS自身のパッケージ形式については特に規定せず、単に RPM を追加サポートすることで[サードパーティー](https://ja.wikipedia.org/wiki/サードパーティー "wikilink")が任意のLinuxシステム向けにソフトウェアを配布できるようにするとしている。Debianは既にオプションでLSBをサポートしている（LSB 1.1を "woody" で、2.0を "sarge" で、3.1を "etch" でサポート）が、問題はそれだけでは収まらない。DebianはRPMパッケージをネイティブのパッケージ形式に変換する "alien" というプログラムを用意している。しかし、LSB側は「このことでDebianがLinux Standard Baseに完全準拠していることにはならず、LSB準拠と解釈するべきでない」としている。

また、認証テストスイートもバグが多く不完全であると批判されている。[GNU Cライブラリ主要開発者のUlrich](https://ja.wikipedia.org/wiki/GNU_Cライブラリ "wikilink") DrepperはLSBのテストスイートについて、バグのあるテストに合格するようにした場合、ディストリビューション間で非互換が発生する原因にもなるとしている[2](http://udrepper.livejournal.com/8511.html)。また彼は、ディストリビューションのテストだけではアプリケーションの互換問題は解決されないと指摘し、アプリケーションのテストをしていない点を非難している。

以上挙げた点以外ではLSBは広く受け入れられている。

## 関連項目

  - [Filesystem Hierarchy Standard](https://ja.wikipedia.org/wiki/Filesystem_Hierarchy_Standard "wikilink")
  - [Common Unix Printing System](https://ja.wikipedia.org/wiki/Common_Unix_Printing_System "wikilink")
  - [Linux](https://ja.wikipedia.org/wiki/Linux "wikilink")
  - [POSIX](../Page/POSIX.md "wikilink")

## 脚注

### 出典

## 外部リンク

  - Linux Foundationのサイト

  - [Four Linux Vendors Agree On An LSB Implemenation (slashdot)](http://linux.slashdot.org/article.pl?sid=04/11/17/1427257&tid=185&tid=190&tid=106)

  - 1998年8月26日の[プレスリリース](http://www.debian.org/News/1998/19980826e)

  - [Do you still think the LSB has some value?](http://www.livejournal.com/users/udrepper/8511.html) - Ulrich Drepperによる批判

  - [Yes, the LSB Has Value](http://www.licquia.org/archives/2005/09/27/yes-the-lsb-has-value/) - Jeff LicquiaによるDrepperの批判への回答

[Category:Linux](https://ja.wikipedia.org/wiki/Category:Linux "wikilink")

1.
2.
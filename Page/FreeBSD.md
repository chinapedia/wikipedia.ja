> この記事は[FreeBSD](https://ja.wikipedia.org/wiki/FreeBSD)から翻訳されています。


**FreeBSD**（フリービーエスディー）は、[Unix系](../Page/Unix系.md "wikilink")の[オープンソース](../Page/オープンソース.md "wikilink")の[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink") (OS) である。[SCO](../Page/SCO.md "wikilink")による[Single UNIX Specificationの認証は受けていないものの](../Page/Single_UNIX_Specification.md "wikilink")、[NetBSD](../Page/NetBSD.md "wikilink")や[OpenBSD](../Page/OpenBSD.md "wikilink")と同じく、[AT\&T](../Page/AT&T.md "wikilink")の[UNIX](../Page/UNIX.md "wikilink")から派生した[BSDの子孫](../Page/BSDの子孫.md "wikilink")に当たる。サーバ用途を志向しており、処理速度よりも安定動作に重きを置いている。近代的な[オープンソース](../Page/オープンソース.md "wikilink")の[BSD](../Page/BSD.md "wikilink")としてはNetBSDに次いで古く、[1993年](../Page/1993年.md "wikilink")[12月](https://ja.wikipedia.org/wiki/12月 "wikilink")に最初の公式リリースである1.0が公開された。

## 特徴

FreeBSDの開発者達は、Webサイトにて安定していて高速・高性能でなおかつ安全、先進的な機能や多くのセキュリティ機能を提供していると語っていた。[FreeBSD jail等の機能もレンタルサーバ等に適したシステムであるといえる](../Page/FreeBSD_jail.md "wikilink")。[Linux](../Page/Linux.md "wikilink")と異なり[カーネル](../Page/カーネル.md "wikilink")とユーザランドを含めて一つのOSであり、そしてOS側に[GPLのものを含まないようにしていることも特徴の一つである](../Page/GNU_General_Public_License.md "wikilink")。そして、堅牢性の高いBSDカーネルの設計が最大の特徴として認知されている。

  - OSとしての特性
    カーネルの高負荷耐性が高く、負荷が増大しても安定して動作する特徴がある。また、何千ものユーザーからの同時アクセスにもすばやく応答する\[1\]。
  - デスクトップ環境
    初期状態でツールが一通り揃っているLinuxと違い、ガイダンスに沿って普通にインストールした状態では最小の構成に留められており、CUIからしか操作を行えない。デスクトップ環境を揃えるにはソフトウェアのインストールと設定の作業は必須である。GUI経由の設定よりも手作業で設定ファイルを直接書き換えて設定する事が多く、若干UNIX熟練者向きであるとされる。しかし、サーバー向けとして見た場合には、このシンプルなOSの構成は安定性に大きく寄与していると言える。
  - 最適化
    ソースコードからコンパイルし直すことで、OS全体を特定のCPUに対して最適化する事が可能で、最新のLinuxが動作しないパソコンでも最新版のFreeBSDを実用的な速度で動作させることが可能である。
  - 旧世代ハードウェアのサポート
    ISAバスの拡張カード等、旧世代ハードウェアのドライバが豊富に含まれており、最新機種のみならず、数世代以上前のコンピュータでも動作させることが可能である。(ただし、性能面での制約はより厳しいものとなる)
  - グラフィックスデバイスのサポート
    デスクトップ環境としてみた場合、2D限定あるいは3D機能の一部は[X.Org Serverのドライバが多くのビデオカードに対応しており](../Page/X.Org_Server.md "wikilink")[Xfce](../Page/Xfce.md "wikilink")、[GNOME](../Page/GNOME.md "wikilink")、[KDE](../Page/KDE.md "wikilink")等のデスクトップ環境を使うことができる（フリーのドライバを使う限りでは多少の対応状況の違いはあるもののLinuxとほぼ同様の環境となる）。[NVIDIA](../Page/NVIDIA.md "wikilink")のビデオカードであればメーカーのドライバがサポートされていて[OpenGL](../Page/OpenGL.md "wikilink")で完全な3Dハードウェアアクセラレーションが動作する。
  - 他のプラットフォームのエミュレーション
    カーネルレベルでのLinuxバイナリ互換機能（カーネル2.6.16相当）や、アプリケーションレベルでは[Wine](../Page/Wine.md "wikilink")による[Windows互換環境等を用いてネイティブでないソフトウェアも使うことができる](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")。

## システム要件

### 最小構成

  - [amd64](https://ja.wikipedia.org/wiki/amd64 "wikilink")プロセッサ
  - 96MBの[RAM](https://ja.wikipedia.org/wiki/RAM "wikilink")
  - 1.5GBの[ハードドライブ](https://ja.wikipedia.org/wiki/ハードドライブ "wikilink")空き容量
  - [ネットワークカード](../Page/ネットワークカード.md "wikilink")

### 推奨される設定

  - [amd64](https://ja.wikipedia.org/wiki/amd64 "wikilink")プロセッサ
  - [rEFInd](https://ja.wikipedia.org/wiki/rEFInd "wikilink")をインストールするための[EFI](https://ja.wikipedia.org/wiki/EFI "wikilink")システムパーティション
  - 4GBのRAM
  - デスクトップインストールの場合は8GBのハードドライブ空き容量
  - 3Dアクセラレーション[ビデオカード](../Page/ビデオカード.md "wikilink")
  - ネットワークカード
  - [サウンドカード](../Page/サウンドカード.md "wikilink")

## 歴史

[1991年](../Page/1991年.md "wikilink")、[ウィリアム・ジョリッツ](https://ja.wikipedia.org/wiki/ウィリアム・ジョリッツ "wikilink")によって[4.3BSD Net/2をベースとしたOS](https://ja.wikipedia.org/wiki/4.3BSD_Net/2 "wikilink")、**[386BSD](../Page/386BSD.md "wikilink")**が発表された。

しかし公開後の開発が停滞したため、386BSDのユーザらは「Unofficial 386BSD Patchkit」を製作し、バグの対応などを行っていた。その後386BSDは、ほぼ1年にわたって放っておかれ、やがてパッチキットの量は膨大になってしまった。

そこで、386BSDのユーザらは「386BSDの開発の手助けのため」、パッチキットを適用した状態の「クリーンナップ」スナップショットの製作プロジェクトを進めた。しかし、Jolitzがこのプロジェクトの受け入れを拒否したことにより、プロジェクトは路線変更を余儀なくされた。結局、パッチキットの最後の取りまとめ役であったNate Williams、Rod Grimes、[ジョーダン・ハバード](../Page/ジョーダン・ハバード.md "wikilink")らは、自分達で新しいOSの開発を行う事を決意し、[1993年](../Page/1993年.md "wikilink")にFreeBSDプロジェクトをスタートさせた。「FreeBSD」という名前はDavid Greenmanによって考案されたものである。[1993年](../Page/1993年.md "wikilink")[6月19日](../Page/6月19日.md "wikilink")、ジョーダン・ハバード、Rod GrimesおよびDavid Greenmanは、FreeBSDの開発開始をアナウンスした。

FreeBSDは**4.3BSD Net/2**をベースに開発が行われ、[1993年](../Page/1993年.md "wikilink")12月には最初のリリースであるFreeBSD 1.0が、そして、[1994年](../Page/1994年.md "wikilink")[5月](https://ja.wikipedia.org/wiki/5月 "wikilink")にはFreeBSD 1.1がリリースされた。

しかしこの後、当時**[UNIX](../Page/UNIX.md "wikilink")**のソースコードの権利をもっていた[ノベルと](../Page/ノベル_\(企業\).md "wikilink")[カリフォルニア大学バークレー校](../Page/カリフォルニア大学バークレー校.md "wikilink")との長期に渡った訴訟の和解が成立し、4.3BSD Net/2にUNIXのライセンスに抵触する部分があることが正式に認められた。そのため、FreeBSDはそのまま開発を続けることが不可能となり、[1994年](../Page/1994年.md "wikilink")[7月](https://ja.wikipedia.org/wiki/7月 "wikilink")にリリースされたFreeBSD 1.1.5.1を最後に4.3BSD Net/2をベースにした開発を停止した。

FreeBSDプロジェクトは、UNIXのライセンスに抵触していないことが公式に宣言された[4.4BSD-Lite](https://ja.wikipedia.org/wiki/4.4BSD-Lite "wikilink")を基にしてFreeBSDの開発を再開した。再開後の最初のリリースであるFreeBSD 2.0は[1994年](../Page/1994年.md "wikilink")[11月](../Page/11月.md "wikilink")に発表され、その後、FreeBSDは順調に発展を続けている。

なお、[X Window Systemについては](../Page/X_Window_System.md "wikilink")、当初[XFree86](../Page/XFree86.md "wikilink")を標準として採用していたが、FreeBSD 5.3からは[X.Org](https://ja.wikipedia.org/wiki/X.Org "wikilink")を標準とするように移行した。

## パッケージ管理

FreeBSDの[パッケージ管理システム](../Page/パッケージ管理システム.md "wikilink")は、ビルド済みパッケージをインストールするpackage, pkg(8)とソースをビルドするスタイルのportsがある。OS以外でpackageのインストールしたものは原則として「/usr/local」以下と「/var/db/pkg」以下に入る。つまりOS部分とほぼ分離されているので明示的な管理やバックアップもしやすいが 基本的にライブラリを共用する発想で構成されているのでWindows等でアプリごとにライブラリを用意することに慣れている人には使い辛いと感じることもある。7系から8系等、メジャーバージョンアップの際には使用ライブラリの互換性がなくなるが一部（usbを使うものなど）を除いて「compat7x」を入れることにより動作する。

### package

packageはビルド済みのバイナリをシステムにインストールする仕組みでportsからインストールされたものも含めてバージョンやファイル構成が記録される。

サーバは本家の他日本など各地にある。自分でもpackageを作る事が出来るので複数台同一環境のPCを管理している場合にも使うことができる。

単独のpackageの個別インストールもできるが、「pkg_add -r」コマンドで上位にあるpackageを指定することにより依存packageもインストールされる。しかしpackageとPCの[Perl](../Page/Perl.md "wikilink")等依存ツールやライブラリのバージョンが異なる場合、手動で修正が必要である等の問題があったり、RELEASE版では最新のpackageを取得するために環境変数「PACKAGESITE」を指定しなくてはいけない他、Web上の情報では「FreeBSDはビルドするのが当たり前」という風潮がかつては多かったため新規インストール以外にはあまり使われないように見受けられる。基本的にはports更新後一週間後程度にはstable版に最新のpackageがアップロードされているようだ。packageのバージョンアップ用のサポートツールとしてpkg_replace等がある。

### ports

portsは半自動的にソースコードからpackageのビルド及びインストールを行う方法である。特殊なパッチを当てる当てないの選択肢ダイアログ等が表示される場合もあるが、基本的にはソースコードのダウンロードからコンパイル、package生成、packageインストールまでの一連の流れを自動的に行うことができる。

ただ、実際にはシェルスクリプトだけのものやフォント、NVIDIA等メーカー品バイナリやJava等ビルド不要のものも多い。packageに比べると作業領域を明示的に指定できる長所がある。

基本的には「/usr/ports」に置かれる。portsの最新情報への更新は「portsnap」というコマンドを用いる事で最小限の更新だけで済ませられる（あるいはcsupないしcvsupを用いてportsツリーを更新することも可能。csup/cvsupについては次項参照のこと）。portsに登録されているソフトウェアが新バージョンへ更新した時に一時的にビルドできなくなるなどの問題が発生することもあるので、Perl等の重要なportsの更新時には一定期間(1週間程度)様子を見る必要がある。

portsに登録されているソフトウェアは2013年1月3日の時点で24,000を超えるが日々増加している。そのメンテナンス状況はメンテナと呼ばれる管理者の能力や意欲に左右される面がある。そのため、常時メンテナンスされて高い品質を維持しているportsも多いが、逆にソースファイルのサイトが閉じていたり、ビルドできなかったりあるいは古いバージョンのまま放置されていたりするものがあるという問題点も指摘されている。

日本人メンテナの活動により、日本語環境に関するportsは他言語に比べ比較的良く整備されており、特に日本語版[LaTeX](../Page/LaTeX.md "wikilink")は完全な環境が容易かつ安定してインストールできることは特徴的である。

無駄なportsを増やさないために「/etc/portsnap.conf」で使わないカテゴリを指定できるがあくまでディレクトリ単位でのカテゴリ指定しかできない。安直にメタポートと呼ばれるものをビルドしようとすると依存するものを全てビルドしてしまうのでファイル構成を把握したらベーシックなライブラリから更新するとストレージ使用効率が良い。

portsからインストールしたものは、たとえpackage生成を行わないように指定したとしても、packageからインストールしたものと同等に扱われる。サポートツールとしてpkg_replaceの他portmasterとruby依存のportupgrade等が使われる。pkg_addに起因するportの依存記述には問題がありしばしインストールの妨げになることがある。

### pkg

pkg(8)は、FreeBSD用の次世代のパッケージ管理システム pkgng として開発されてきたものである。従来のバイナリベースパッケージ管理システムである package よりも、手軽なバイナリアップデート、リモートパッケージ検索、依存関係の管理等の機能が強化されている。pkgは、これまでのものとはパッケージのデータベースの管理方法が異なるため現時点ではFreeBSD 9.x までのバージョンでは、pkg(8)の使用がデフォルト設定にはなっておらず、手動で pkg 管理システムに移行しなければならない。FreeBSD 10.0Rからデフォルトのパッケージ管理システムとして採用されている。

## OSのバージョン

FreeBSDでは安定版である**FreeBSD-RELEASE**の他**FreeBSD-CURRENT**と**FreeBSD-STABLE**の2つの開発ブランチが存在する。

CURRENTはまさに最新のFreeBSDのバージョンの開発ブランチで、作業進行中のソースがならび、開発途上のソフトウェアや過渡的な機能などが含まれている。しかし、これがリリース版に採用されるとは限らない。

STABLEは主に開発が終わったCURRENT開発ブランチに対して、分枝されてリリース版(安定版)を作成する開発ブランチである。こちらに移ってからは全ての修正はこの開発ブランチで行われる。1つのバージョン系列の開発が終わるとこのブランチからも外れ、以後一定期間は必要に応じてセキュリティアップデート等の修正が行われる。修正はパッチをあてることで行われ、**8.1-RELEASE-p2**などと最後尾に修正が行われた回数（pはpatch levelのこと）が示される。

なお、いったんSTABLEとして扱われると、1つ上の開発バージョンがCURRENTとして扱われることになる。例外として、FreeBSD 5系では多くの改善や機能追加が行われたために、5.0〜5.2の間はリリース版が出ているのにも関わらずSTABLEとして扱われない状態が続いていたが、6.0がリリースされてからは元の体制に戻った。

### バージョン管理

FreeBSDのSTABLE版とCURRENT版は、subversionを使ってソースコードレベルでOSのバージョン管理を行う。 ソースコードの更新にはかつては「csup」というコマンドが用いられたが（csupは[CVSup](https://ja.wikipedia.org/wiki/CVSup "wikilink")の主要な機能を[C言語](../Page/C言語.md "wikilink")で再実装したものである。これは、CVSupがプログラム言語として一般的でない[Modula-3](https://ja.wikipedia.org/wiki/Modula-3 "wikilink")で実装されており、これが理由でcsupはベースシステムに含まれるがCVSupはportsから導入する）、cvsupによる配布は2013年2月一杯で終了し、以降はsubversionが用いられている。

`/usr/src`以下に展開されたソースコードをmakeすることにより、メジャーバージョンの更新も含めてOS全体のバージョンアップができる。

バイナリで配布されたRELEASE版に対しては「freebsd-update」というコマンドが用いられ定期的なセキュリティパッチ等のバージョンアップができる。GENERICカーネルであればカーネルのアップデートも可能である。通常はセキュリティパッチが入るとカーネルの名称に「p2」等とバージョンがつくがカーネル以外だけの更新の場合カーネル名称は変わらない。

### セキュリティ対応と保証期間

FreeBSDのSTABLE版及びRELEASE版については、リリース後一定期間、セキュリティに関する問題が発生した場合に必要なアドバイザリ及びアップデートがリリースされる保証期間が設けられる。保証期間については以下の3つの区分が存在する\[2\]。なおCURRENT版についてはあくまで開発版という扱いのため、セキュリティアップデートやアドバイザリは提供されない。

  - Early Adopter
    CURRENT版から分岐した最初のRELEASE版に適用されるもの（ただし2012年現在適用例はない）。保証期間はリリース後6ヶ月。
  - Normal
    通常のRELEASE版（STABLE版から分岐したもの）に適用されるもの。保証期間はリリース後1年。
  - Extended
    原則として、メジャーバージョンに対して2番目以降のRELEASE版及びそれに対応するSTABLE版に適用されるもの。保証期間はリリース後2年。

ただし実際には、各RELEASE版に対しNormal及びExtendedのどちらを選択するか、その時点でのRELEASE版のコード品質等を考慮して個別に定められることが多く、時には「古いRELEASEの方が新しいRELEASEよりも保証期間が長い」という逆転現象が起こることがある（例：8.1-RELEASEの保証期間が2012年7月末までなのに対し、8.2-RELEASEの保証期間は2012年2月末まで。また過去には7.1-RELEASEと7.2-RELEASEの間でも同様の逆転現象が発生した。ただし8.2-RELEASEの保守終了予定日は8.1-RELEASE同様2012年7月末まで延長されている）。このため、特にサーバ等で長期に運用する予定の機器では、保証期間の終了時期を踏まえたバージョン選択を行う必要がある。

### 最新のバージョン

現在、セキュリティアップデートなどがサポートされている安定リリース版、及び開発ブランチは以下の通りである。

  - **RELEASE**（リリース版）：
      - **FreeBSD 12.0-RELEASE**（[2018年](../Page/2018年.md "wikilink")[12月11日](../Page/12月11日.md "wikilink")）
      - **FreeBSD 11.2-RELEASE**（[2018年](../Page/2018年.md "wikilink")[6月27日](../Page/6月27日.md "wikilink")）
  - STABLE（安定開発版）：FreeBSD 12-STABLE
  - CURRENT（最新開発版）：N/A

### バージョンごとの特徴

#### FreeBSD 1

「1.0-RELEASE」は、4.3BSD Net/2を基にして1993年11月に開発された。

4.3BSD Net/2にUNIXのライセンスに抵触する部分があるとして、1994年7月5日にリリースされた「1.1.5.1-RELEASE」を最後に4.3BSD Net/2を基にした開発を停止。

#### FreeBSD 2

「2.0-RELEASE」はUNIXのライセンスに抵触していないことが公式に宣言された4.4BSD-Liteを基にして1994年11月22日に発表された。バージョン2の最終版の「2.2.8-RELEASE」は1998年11月29日に発表された。

「2.0-RELEASE」は、AT\&T由来のUNIXソースコードの著作権者ノベルの法的請求権から(将来に渡って)公的に解放された最初のFreeBSDのバージョンである\[3\]。また、インターネットサーバー拡大期の始まりにおいて、広く使われた最初のバージョンでもある。

#### FreeBSD 3

「3.0-RELEASE」は1998年10月16日に発表された。バージョン3の最終版の「3.5-RELEASE」は2000年6月24日に発表された。

「3.0-RELEASE」は**[ジャイアントロック](https://ja.wikipedia.org/wiki/ジャイアントロック "wikilink")**を用いて[SMPシステムをサポートできる最初のブランチである](../Page/対称型マルチプロセッシング.md "wikilink")。「3.1-RELEASE」からは**[USB](../Page/ユニバーサル・シリアル・バス.md "wikilink")**をサポートし、「3.2-RELEASE」から**[ギガビット・イーサネット](https://ja.wikipedia.org/wiki/ギガビット・イーサネット "wikilink")[カード](../Page/ネットワークカード.md "wikilink")**をサポートした。

#### FreeBSD 4

「4.0-RELEASE」は2000年3月13日に発表された。2005年1月25日に出た最終版の「4.11-RELEASE」は2007年1月31日までサポートされていた\[4\]。

バージョン4は、その安定性を賞賛され、最初の[インターネット・バブル](https://ja.wikipedia.org/wiki/インターネット・バブル "wikilink")の時期に[プロバイダと](https://ja.wikipedia.org/wiki/インターネットサービスプロバイダ "wikilink")[ホスティングサーバ](../Page/ホスティングサーバ.md "wikilink")から好まれたオペレーティングシステムであり、[Unix系](../Page/Unix系.md "wikilink")では最も安定した高いパフォーマンスのオペレーティングシステムの一つと広く見なされている\[5\]。バージョン4の新機能では、「4.1-RELEASE」より（後に[NetBSD](../Page/NetBSD.md "wikilink")や[OpenBSD](../Page/OpenBSD.md "wikilink")のシステムの一部となる）**kqueue(2)**のシステムコールを導入した\[6\]。

#### FreeBSD 5

「5.0-RELEASE」は2003年1月14日にCURRENT(最新開発版)として発表された。バージョン5の最初の安定版のリリースは、2004年9月6日に発表された「5.3-RELEASE」である（「5.05-RELEASE」～「5.2.1-RELEASE」は「5-CURRENT」として一般ユーザの利用は勧められていなかった）\[7\]。バージョン5の最終安定版は2006年5月25日に出た「5.5-RELEASE」であった。

バージョン5の最初のブランチとして登場した「5.0-RELEASE」は、先進的な[マルチプロセッサと](../Page/マルチプロセッシング.md "wikilink")[アプリケーション](../Page/アプリケーションソフトウェア.md "wikilink")[スレッディング](../Page/スレッド_\(コンピュータ\).md "wikilink")、**[UltraSPARCと](../Page/UltraSPARC_T1.md "wikilink")[IA-64](../Page/IA-64.md "wikilink")のプラットフォーム対応**等のサポートといった注目度の高い機能を手広く先取りしていた。

  - カーネルロック機構の変更
    バージョン5の最大の[アーキテクチャに関する開発は](../Page/コンピュータ・アーキテクチャ.md "wikilink")、[SMPを改善させる為に低レベルのカーネル](../Page/対称型マルチプロセッシング.md "wikilink")[ロック機構を大きく変更させた点であった](https://ja.wikipedia.org/wiki/ロック_\(情報工学\)#スレッドにおけるロック "wikilink")。これによって、[ジャイアントロック](https://ja.wikipedia.org/wiki/ジャイアントロック "wikilink")からカーネルの大部分のリソースが開放された。複数のプロセスを同時にカーネルモードで実行できるようになった。
  - KSE
    **KSE**（カーネルスケジュールエンティティ、*"Kernel Scheduled Entities"*）は、1 個のプロセスが複数のカーネルレベルスレッドを持てるようにするための機構である\[8\]。原理的には、KSEと同様に"M:N" モデルを用いる、[NetBSD](../Page/NetBSD.md "wikilink")に実装された[Scheduler activationsに似ている](https://ja.wikipedia.org/wiki/Scheduler_activations "wikilink")。KSEは、「5.3-RELEASE」より安定版の実装が始まり、「7.0-RELEASE」で1:1スレッド(1個のカーネルスレッドを1個のユーザーランドスレッドが占有して利用)の実装に置き換えられるまでFreeBSDのデフォルトのスレッド機構だった。
  - GEOM
    Poul-Henning Kampの貢献によって作られた、ディスク[I/O要求を変換する](https://ja.wikipedia.org/wiki/入出力#オペレーティングシステムでの入出力 "wikilink")[モジュール型フレームワークである](https://ja.wikipedia.org/wiki/モジュール#ソフトウエア "wikilink")[GEOM](https://ja.wikipedia.org/wiki/GEOM "wikilink") を実装することで、I/O層の[ブロック](../Page/ブロック_\(データ\).md "wikilink")(記録単位)\[9\]をかなり変更できるようになった。GEOMは、[ミラーリング](../Page/ミラーリング.md "wikilink")（gmirror）\[10\]と[暗号](../Page/暗号.md "wikilink")化（GBDEとGELI）\[11\]などの機能の多くを簡単に作成可能とする。このGEOMの開発は[DARPAによる支援を受けて作成されている](../Page/国防高等研究計画局.md "wikilink")。

#### FreeBSD 6

「6.0-RELEASE」は2005年11月4日にリリースされた。バージョン6の最終版の「6.4-RELEASE」は2008年11月11日にリリースされた。これらのバージョンは、SMPと先進的な[IEEE 802.11の機能性の更なる開発の他に下記のようなものがある](../Page/IEEE_802.11.md "wikilink")。

  - スレッド最適化
    **[VFS](../Page/仮想ファイルシステム.md "wikilink")**の**マルチプロセッサセーフ (MPSAFE)** が有効となり、ジャイアントロックが最小限まで減らされた\[12\]。

<!-- end list -->

  - 著しいネットワーク[スタック](../Page/スタック.md "wikilink")のパフォーマンス強化
    libthrライブラリのlibc_rのデフォルトスタックサイズ が増やされ、パフォーマンス性を高めた。32ビットプラットフォームでは、メインスレッドはデフォルトで2MBのスタックを受け取り他のスレッドではデフォルトで1MBのスタックを受け取る。(64ビットプラットフォームでのデフォルト スタック サイズ は、それぞれ4MBと2MBとなる。)

<!-- end list -->

  - OpenBSM
    TrustedBSD\[13\]プロジェクトによって作成され[BSDライセンス](../Page/BSDライセンス.md "wikilink")の下でリリースされたセキュリティイベントの監査用の**OpenBSM**\[14\]と呼ばれる基本セキュリティモジュール（BSM）監査\[15\]の実装をした。これは[アップルの](../Page/アップル_\(企業\).md "wikilink")[オープンソースの](../Page/オープンソースソフトウェア.md "wikilink")[Darwinに見出したBSM実装に基づいたものである](../Page/Darwin_\(オペレーティングシステム\).md "wikilink")。

その他、[プリエンプティブカーネル](https://ja.wikipedia.org/wiki/プリエンプション#ユーザーモードとカーネルモード "wikilink")（タスクの置き換え）とハードウェアパフォーマンス測定ドライバ(HWPMC)\[16\]のサポート等が挙げられる。

#### FreeBSD 7

「7.0-RELEASE」は2008年2月27日にリリースされた。バージョン7の最終版の「7.4-RELEASE」は2011年2月24日にリリースされた。

新機能は下記の通り多彩に渡る。

  - [SCTP](../Page/Stream_Control_Transmission_Protocol.md "wikilink")
  - [UFSの](../Page/Unix_File_System.md "wikilink")[ジャーナリング](../Page/ジャーナリングファイルシステム.md "wikilink")
  - [サン・マイクロシステムズ](../Page/サン・マイクロシステムズ.md "wikilink")の**[ZFS](../Page/ZFS.md "wikilink")**[ファイルシステム](../Page/ファイルシステム.md "wikilink")の実験的な移植
  - [ARMアーキテクチャ](../Page/ARMアーキテクチャ.md "wikilink")への改良されたサポート
  - jemalloc([Firefox3に移植された](../Page/Mozilla_Firefox.md "wikilink")[並列計算](../Page/並列計算.md "wikilink")\[17\]に最適化された[malloc](https://ja.wikipedia.org/wiki/malloc "wikilink")のこと)\[18\]
  - ネットワーク関連やオーディオの最適化や[SMPのパフォーマンス改善](../Page/対称型マルチプロセッシング.md "wikilink")\[19\]
  - [GCC](../Page/GNUコンパイラコレクション.md "wikilink")4.2.1、X.Org 7.3、KDE 3.5.8、GNOME2.20.2、BIND9.4.2。

ベンチマークは、[Linux](../Page/Linux.md "wikilink")だけでなくFreeBSDの以前のバージョンに比べても著しい速度の向上を示している\[20\]。

  - ULEスケジューラ
    「5.1-RELEASE」から実験的に実装されてきた**ULEスケジューラ**は、「7.0-RELEASE」の新版でカーネルの構築時にスケジューラを調整できるようになるなど大きく改良されていたが、依然「4BSDスケジューラ」と呼ばれる従来のスケジューラが標準で実装されていた\[21\]。「7.1-RELEASE」では、AMD64/i386版で、標準でULEスケジューラが採用された\[22\]。
  - システム情報取得機能「DTrace」
    「7.1-RELEASE」より**[DTrace](../Page/DTrace.md "wikilink")**が実装されてシステムのダイナミックな監視やトラブルシューティングが可能になった\[23\]。「プローブ(probe)」と呼ばれるデータ観測ポイントに、dtraceコマンドを含む「DTraceコンシューマ」という情報所得するプログラムを使って情報を取得する。dtraceコマンドは「D」と呼ばれる[C言語](../Page/C言語.md "wikilink")に似たスクリプト言語で記述することによって実行ができる。これにより、プローブからのデータを取り出したり集計することができる\[24\]。
  - jailによる仮想環境構築
    「7.2-RELEASE」では、**[jail](../Page/FreeBSD_jail.md "wikilink")**というOSレベルでの[仮想化](../Page/仮想化.md "wikilink")機構が実装された。1つのJail仮想環境に対して複数のIPv4/v6アドレスを割り当てたり、IPアドレスを割り当てないで運用したりすることが可能になった\[25\]。

「4.0-RELEASE」より対応していた[DEC Alphaアーキテクチャへの対応は](https://ja.wikipedia.org/wiki/DEC_Alpha "wikilink")、「7.0-RELEASE」より中止となった\[26\]。

#### FreeBSD 8

「8.0-RELEASE」は2009年11月25日にリリースされた\[27\]。2009年8月にトランクからバージョン8は[ブランチした](https://ja.wikipedia.org/wiki/ブランチ_\(ソフトウェア\) "wikilink")。バージョン8の最新版は「8.4-RELEASE」で2013年6月7日にリリースされた\[28\]。

主な機能は、SuperPages対応、**[Xen](../Page/Xen_\(仮想化ソフトウェア\).md "wikilink")**の「ドメインU (domU)」への対応、ネットワークスタックの仮想化、スタックスマッシュプロテクション、新しいTTYレイヤへの置き換え、大幅に更新され、改善されたZFSへの対応、「8.2-RELEASE」で追加された**USB3.0**とそのホストコントローラの規格である[xHCIへの対応](https://ja.wikipedia.org/wiki/ユニバーサル・シリアル・バス#ホストコントローラの種類 "wikilink")、[IGMPv](../Page/Internet_Group_Management_Protocol.md "wikilink")3を含む[マルチキャスト](../Page/マルチキャスト.md "wikilink")のアップデート、(「8.2-RELEASE」で追加された)[インテル](https://ja.wikipedia.org/wiki/インテル "wikilink")[CPU](../Page/CPU.md "wikilink")対応の[NFSv4と](https://ja.wikipedia.org/wiki/Network_File_System#NFS_version_4 "wikilink")[AESの](https://ja.wikipedia.org/wiki/AES-NI "wikilink")[アクセラレータを導入している](../Page/ハードウェアアクセラレーション.md "wikilink")[NFSの](../Page/Network_File_System.md "wikilink")[クライアント・サーバの書き換えである](../Page/クライアントサーバモデル.md "wikilink")。

改良されたデバイスのmmap()の拡張機能によって、x86-64プラットフォーム用の64ビット[NVIDIA](../Page/NVIDIA.md "wikilink")ディスプレイドライバが実装可能となった。プラグイン対応の[輻輳制御](https://ja.wikipedia.org/wiki/輻輳制御 "wikilink")フレームワークと、Linuxの[エミュレーション下で実行されるアプリケーションのシステム情報を取得するDTraceを使用可能とする機能は](../Page/エミュレータ_\(コンピュータ\).md "wikilink")「8.3-RELEASE」で追加された。

#### FreeBSD 9

「9.0-RELEASE」は2012年1月12日にリリースされた\[29\]。「9.1-RELEASE」は2012年12月31日にリリースされた\[30\]。「9.2-RELEASE」は2013年9月30日にリリースされた\[31\]。「9.3-RELEASE」は2014年7月16日にリリースされた\[32\]。

リリースの主な機能は、新しいインストーラ bsdinstall(8) の追加、[UFSのFFS](../Page/Unix_File_System.md "wikilink")(Fast Filesystem)がsoftupdatesジャーナリングに対応、ZFSがバージョン28に更新、ユーザレベルDTraceの導入、NFSサブシステムが、NFSv3およびNFSv2に加えてNFSv4に対応した新しい実装に更新、ファイル保護機能Capsicumをカーネルでサポート\[33\]、FreeBSD/powerpcで[PlayStation 3をサポートなどである](https://ja.wikipedia.org/wiki/PlayStation_3 "wikilink")。

カーネルとベースシステムは**[Clang](https://ja.wikipedia.org/wiki/Clang "wikilink")**を使用して構築することができるようになったが、「9.0-RELEASE」はまだデフォルトで[GCC](../Page/GNUコンパイラコレクション.md "wikilink")4.2を使用している。

  - Orbis OS
    **[PlayStation 4](https://ja.wikipedia.org/wiki/PlayStation_4 "wikilink")**の[ゲーム機](../Page/ゲーム機.md "wikilink")用OSとして、「9.0-RELEASE」から[SCEが](https://ja.wikipedia.org/wiki/ソニー・コンピュータエンタテインメント "wikilink")[フォークした](../Page/フォーク_\(ソフトウェア開発\).md "wikilink")「**Orbis OS**」と呼ばれるFreeBSD派生OSが使用されている\[34\]\[35\]。

#### FreeBSD 10

「10.0-RELEASE」は2014年1月20日にリリースされた\[36\]。「10.1-RELEASE」は2014年11月14日にリリースされた\[37\]。「10.2-RELEASE」は2015年8月13日にリリースされた\[38\]。

  - 非推奨が含まれるGCCをClangに置き換えている。
  - BINDをベースシステムから削除している。
  - デフォルトパッケージ管理ユーティリティとしてpkg(7)を採用している。
  - [iSCSI](https://ja.wikipedia.org/wiki/iSCSI "wikilink")規格の実装

**VirtIO** (準仮想化)ドライバが**[KVM](https://ja.wikipedia.org/wiki/Kernel-based_Virtual_Machine "wikilink")**に対応、**[FUSE](../Page/Filesystem_in_Userspace.md "wikilink")**の実装などである\[39\]。

「10.0-RELEASE」に実装された**[BHyVe](https://ja.wikipedia.org/wiki/BHyVe "wikilink")** (BSDハイパーバイザ)は、まだ実験的なハイパーバイザであるが、仮想マシン内でゲストOSを稼働できる。仮想CPU数・ゲストメモリ・IOコネクティビティなどなどもコマンドラインパラメータで指定できる\[40\]。

「10.3-RELEASE」より、UEFIシステムにおけるroot-on-ZFSインストールに対応した\[41\]。

#### FreeBSD 11

「11.0-RELEASE」は2016年10月10日にリリースされた\[42\]。

FreeBSD 11は新しいサポートモデルの下で、少なくとも2021年9月30日までの5年間の長期サポートが行われるとしている\[43\]。

FreeBSD 11.0-RELEASEのリリースエンジニアリングの終盤でOpenSSLの脆弱性が公開されたため、FreeBSDリリースエンジニアリングチームはこれを修正した「FreeBSD 11.0-RELEASE-p1」を新しくビルドして公開した。今回のリリース対象はこのパッチレベル1が対象となっている。アップグレードする際に「FreeBSD 11.0-RELEASE」がインストールされている場合、早期に「FreeBSD 11.0-RELEASE-p1」以降へアップグレードすることが望まれるとしている。

FreeBSD 11.1-RELEASEは予定通り2017年7月26日リリースされた。

  -
    更新内容と一部としては
    Clang, LLVM, LLD, LLDB, libc++ がバージョン 4.0.0. へ更新された。
    Elf Tool Chain, ACPICA, libarchive(3), ntpd(8), unbound(8), などのサードパーティー・ソフトウェアが更新された。
    blacklistd(8) が [OpenSSH](../Page/OpenSSH.md "wikilink")に追加された。

#### FreeBSD 12

「12.0-RELEASE」は2018年12月11日にリリースされた\[44\]。

安定版ブランチ単位で5年間のサポートを提供することについてビジネスモデルを再評価する必要が出てきたとして、2019年3月31日まで新しいサポートモデルに関して意見を募るとしている\[45\]。

「12.1-RELEASE」は2019年11月4日にリリースされた\[46\]。

### これまでのリリース

掲載しているのはRELEASEのアナウンスがされたバージョンのみ。

| 凡例                          |
| --------------------------- |
| サポート切れ（過去のリリース）             |
| **RELEASE** (サポート中・安定リリース版) |
| **CURRENT** (最新開発版)         |

| バージョン\[47\]      | リリース日\[48\] | サポート終了予定\[49\] | 備考                             |
| ---------------- | ----------- | -------------- | ------------------------------ |
| 1.0-RELEASE      | 1993年11月1日  |                |                                |
| 1.1-RELEASE      | 1994年5月6日   |                |                                |
| 1.1.5-RELEASE    | 1994年6月30日  |                |                                |
| 1.1.5.1-RELEASE  | 1994年7月5日   |                |                                |
| 2.0-RELEASE      | 1994年11月22日 |                |                                |
| 2.0.5-RELEASE    | 1995年6月10日  |                |                                |
| 2.1-RELEASE      | 1995年11月19日 |                |                                |
| 2.1.5-RELEASE    | 1996年7月16日  |                |                                |
| 2.1.6-RELEASE    | 1996年11月15日 |                | FreeBSD 2.1.6.1-RELEASEに置き換え   |
| 2.1.6.1-RELEASE  | 1996年11月26日 |                |                                |
| 2.1.7-RELEASE    | 1997年2月20日  |                |                                |
| 2.1.7.1-RELEASE  | 1997年3月19日  |                |                                |
| 2.2-RELEASE      | 1997年3月16日  |                |                                |
| 2.2.1-RELEASE    | 1997年3月25日  |                |                                |
| 2.2.2-RELEASE    | 1997年5月16日  |                |                                |
| 2.2.5-RELEASE    | 1997年10月22日 |                |                                |
| 2.2.6-RELEASE    | 1998年3月25日  |                |                                |
| 2.2.7-RELEASE    | 1998年7月22日  |                |                                |
| 2.2.8-RELEASE    | 1998年11月30日 |                |                                |
| 3.0-RELEASE      | 1998年10月15日 |                |                                |
| 3.1-RELEASE      | 1999年2月15日  |                |                                |
| 3.2-RELEASE      | 1999年5月18日  |                |                                |
| 3.3-RELEASE      | 1999年9月17日  |                |                                |
| 3.4-RELEASE      | 1999年12月20日 |                |                                |
| 3.5-RELEASE      | 2000年6月24日  |                |                                |
| 4.0-RELEASE      | 2000年3月13日  |                |                                |
| 4.1-RELEASE      | 2000年7月27日  |                |                                |
| 4.1.1-RELEASE    | 2000年9月27日  |                |                                |
| 4.2-RELEASE      | 2000年11月22日 |                |                                |
| 4.3-RELEASE      | 2001年4月20日  |                |                                |
| 4.4-RELEASE      | 2001年9月20日  |                |                                |
| 4.5-RELEASE      | 2002年1月29日  | 2002年12月31日    |                                |
| 4.6-RELEASE      | 2002年6月15日  | 2003年5月        |                                |
| 4.6.2-RELEASE    | 2002年8月15日  | 2003年5月        |                                |
| 4.7-RELEASE      | 2002年10月10日 | 2003年12月       |                                |
| 4.8-RELEASE      | 2003年4月3日   | 2004年3月31日     |                                |
| 4.9-RELEASE      | 2003年10月28日 | 2004年10月31日    |                                |
| 4.10-RELEASE     | 2004年5月27日  | 2006年5月        |                                |
| 4.11-RELEASE     | 2005年1月25日  | 2007年1月31日     |                                |
| 5.0-RELEASE      | 2003年1月14日  | 2003年6月30日     | 6.0が出るまではCURRENT(開発ブランチ)扱いであった |
| 5.1-RELEASE      | 2003年6月9日   | 2004年2月        |                                |
| 5.2-RELEASE      | 2004年1月9日   | 2004年12月31日    |                                |
| 5.2.1-RELEASE    | 2004年2月25日  | 2004年12月31日    |                                |
| 5.3-RELEASE      | 2004年11月6日  | 2006年10月31日    | 5.x系では初めてとなるSTABLEブランチからのリリース  |
| 5.4-RELEASE      | 2005年5月9日   | 2006年10月31日    |                                |
| 5.5-RELEASE      | 2006年5月25日  | 2008年5月31日     |                                |
| 6.0-RELEASE      | 2005年11月4日  | 2007年1月31日     |                                |
| 6.1-RELEASE      | 2006年5月8日   | 2008年5月31日     |                                |
| 6.2-RELEASE      | 2007年1月15日  | 2008年5月31日     |                                |
| 6.3-RELEASE      | 2008年1月18日  | 2010年1月31日     |                                |
| 6.4-RELEASE      | 2008年11月28日 | 2010年11月30日    |                                |
| 7.0-RELEASE      | 2008年2月27日  | 2009年4月30日     |                                |
| 7.1-RELEASE      | 2009年1月4日   | 2011年2月28日     |                                |
| 7.2-RELEASE      | 2009年5月4日   | 2010年6月30日     |                                |
| 7.3-RELEASE      | 2010年3月23日  | 2012年3月31日     |                                |
| 7.4-RELEASE      | 2011年2月24日  | 2013年2月28日     |                                |
| 8.0-RELEASE      | 2009年11月25日 | 2010年11月30日    |                                |
| 8.1-RELEASE      | 2010年7月23日  | 2012年7月31日     |                                |
| 8.2-RELEASE      | 2011年2月24日  | 2012年7月31日     |                                |
| 8.3-RELEASE      | 2012年4月18日  | 2014年4月30日     |                                |
| 8.4-RELEASE      | 2013年6月7日   | 2015年6月30日     |                                |
| 9.0-RELEASE      | 2012年1月12日  | 2013年3月31日     |                                |
| 9.1-RELEASE      | 2012年12月30日 | 2014年12月31日    |                                |
| 9.2-RELEASE      | 2013年9月30日  | 2014年12月31日    |                                |
| 9.3-RELEASE      | 2014年7月16日  | 2016年12月31日    |                                |
| 10.0-RELEASE     | 2014年1月20日  | 2015年2月28日     |                                |
| 10.1-RELEASE     | 2014年11月14日 | 2016年12月31日    |                                |
| 10.2-RELEASE     | 2015年08月13日 | 2016年12月31日    |                                |
| 10.3-RELEASE     | 2016年04月04日 | 2018年04月30日    |                                |
| 10.4-RELEASE     | 2017年10月3日  | 2018年10月31日    |                                |
| 11.0-RELEASE     | 2016年10月10日 | 2017年11月30日    |                                |
| 11.1-RELEASE     | 2017年7月26日  | 2018年9月30日     |                                |
| 11.2-RELEASE     | 2018年6月27日  | 2019年10月31日    |                                |
| **11.3-RELEASE** | 2019年7月9日   |                | 開発ブランチ：stable/11               |
| **12.0-RELEASE** | 2018年12月11日 |                |                                |
| **12.1-RELEASE** | 2019年11月4日  |                | 開発ブランチ：stable/12               |
| バージョン            | リリース日       | サポート終了予定       | 備考                             |

※2006年4月1日には、[エイプリルフール](https://ja.wikipedia.org/wiki/エイプリルフール "wikilink")のネタとしてFreeBSD 2.2.9-RELEASEが発表されている。

#### バージョン別の主な機能変更

  - 1.1-RELEASE<ref name="1.1features">{{cite web|url=

[http://www.freebsd.org/releases/1.1/RELNOTES.FreeBSD|title=RELEASE](http://www.freebsd.org/releases/1.1/RELNOTES.FreeBSD%7Ctitle=RELEASE) NOTES - FreeBSD - Release 1.1|publisher=The FreeBSD Project|accessdate=2011-04-30}}</ref>

  - [386BSD](../Page/386BSD.md "wikilink")のインポートからいくつかの未解決のバグを修正
  - [XFree86](../Page/XFree86.md "wikilink")を移植
  - XViewを移植
  - InterViewsを移植
  - Elm([メールソフト](../Page/電子メールクライアント.md "wikilink"))を移植
  - [NNTPを移植](../Page/Network_News_Transfer_Protocol.md "wikilink")

<!-- end list -->

  - 2.0-RELEASE\[50\]

<!-- end list -->

  - コードのベースをBSD-Lite 4.4に取り換え
  - 新規のインストーラ
  - 新規のブートマネージャ
  - ([FAT](../Page/File_Allocation_Table.md "wikilink")・unionfs・kernfs等)多くのファイルシステム
  - 大規模ファイルシステム用に差し替えた64ビットのコード
  - ロード可能なファイルシステム等のコードの置き換え
  - [NetBSD](../Page/NetBSD.md "wikilink")からロード可能なカーネルモジュールをインポート

<!-- end list -->

  - 2.0.5-RELEASE\[51\]

<!-- end list -->

  - VMシステムの改良
  - 完全版の[NISの](../Page/ネットワーク・インフォメーション・サービス.md "wikilink")[クライアント・サーバ対応](../Page/クライアントサーバモデル.md "wikilink")
  - [TCP](../Page/Transmission_Control_Protocol.md "wikilink")[トランザクション](../Page/トランザクション.md "wikilink")対応
  - [ISDN](../Page/ISDN.md "wikilink")対応
  - [FDDIと](https://ja.wikipedia.org/wiki/Fiber_Distributed_Data_Interface "wikilink")[100メガビット・イーサネット](https://ja.wikipedia.org/wiki/100メガビット・イーサネット "wikilink")アダプタの対応
  - 多言語ドキュメント
  - [インストール](../Page/インストール.md "wikilink")用[メディアの](../Page/電子媒体.md "wikilink")[パッケージ管理システム](../Page/パッケージ管理システム.md "wikilink")のPort機能

<!-- end list -->

  - 2.1.5-RELEASE\[52\]

<!-- end list -->

  - バグとセキュリティの修正
  - [PCIバス解析](../Page/Peripheral_Component_Interconnect.md "wikilink")
  - 一部のドライバの追加

<!-- end list -->

  - 2.1.6-RELEASE\[53\]

<!-- end list -->

  - バグとセキュリティの修正
  - インストール機能の改良

<!-- end list -->

  - 2.1.7-RELEASE\[54\]

<!-- end list -->

  - バグとセキュリティの修正

<!-- end list -->

  - 2.2-RELEASE\[55\]

<!-- end list -->

  - [NFSv3の対応](https://ja.wikipedia.org/wiki/Network_File_System#NFS_version_3 "wikilink")
  - [動的メモリ確保](../Page/動的メモリ確保.md "wikilink")の[関数を](../Page/サブルーチン.md "wikilink")[malloc](https://ja.wikipedia.org/wiki/malloc "wikilink")をphkmallocに取り換え
  - [ELFの完全なLinuxulator](../Page/Executable_and_Linkable_Format.md "wikilink")([Linux](../Page/Linux.md "wikilink")[エミュレータ](../Page/エミュレータ_\(コンピュータ\).md "wikilink"))対応
  - [カーネル](../Page/カーネル.md "wikilink")のルーチン用の[manページ](https://ja.wikipedia.org/wiki/manページ "wikilink")のセクション9の対応

<!-- end list -->

  - 2.2.1-RELEASE\[56\]

<!-- end list -->

  - 2.2用のバグ修正
  - 「[Adaptec](../Page/アダプテック.md "wikilink") 2940」と「[インテル](https://ja.wikipedia.org/wiki/インテル "wikilink")EtherExpress Pro」のドライバのアップデート
  - CD-ROMパッケージのインストーラの修正

<!-- end list -->

  - 2.2.2-RELEASE\[57\]

<!-- end list -->

  - NFSv3が標準実装
  - 仮想FTPサーバ機能

<!-- end list -->

  - 2.2.5-RELEASE\[58\]

<!-- end list -->

  - [サイリックス](../Page/サイリックス.md "wikilink")製と[AMD製マイクロプロセッサの対応品目の更新](https://ja.wikipedia.org/wiki/アドバンスト・マイクロ・デバイセズ "wikilink")
  - 新しい[VGAライブラリ](../Page/Video_Graphics_Array.md "wikilink")

<!-- end list -->

  - 2.2.6-RELEASE\[59\]

<!-- end list -->

  - [ATAPIのフロッピーディスクドライブ](https://ja.wikipedia.org/wiki/Advanced_Technology_Attachment#ATAPI "wikilink")
  - Linuxulatorの改良
  - 新しいサウンドドライバの対応
  - 新しい[(PnP)の対応](../Page/プラグアンドプレイ.md "wikilink")

<!-- end list -->

  - 2.2.7-RELEASE\[60\]

<!-- end list -->

  - [FAT32の対応](https://ja.wikipedia.org/wiki/File_Allocation_Table#FAT32 "wikilink")
  - PC98(※[Windows98や](../Page/Microsoft_Windows_98.md "wikilink")[Windows 2000向けのシステム設計のことを指しており](../Page/Microsoft_Windows_2000.md "wikilink")、[NECのPC](../Page/日本電気.md "wikilink")-98シリーズのことを指しているのではない)の[アーキテクチャ](../Page/アーキテクチャ.md "wikilink")へのアップデート

<!-- end list -->

  - 2.2.8-RELEASE\[61\]

<!-- end list -->

  - [ipfirewall](https://ja.wikipedia.org/wiki/ipfirewall "wikilink")のコンポーネントのdummynet traffic shaper機能
  - マルチインタフェース間のブリッジ機能
  - 8GB以上の[IDEドライブに対応](https://ja.wikipedia.org/wiki/Advanced_Technology_Attachment#IDE "wikilink")

<!-- end list -->

  - 3.0-RELEASE\[62\]

<!-- end list -->

  - [SMP](../Page/対称型マルチプロセッシング.md "wikilink")
  - CAM(コモンアクセスメソッド)[SCSIシステム](../Page/Small_Computer_System_Interface.md "wikilink")
  - 安全な[RPC](../Page/遠隔手続き呼出し.md "wikilink")
  - ATAPI/IDE規格の[CDライティングソフトと](../Page/ライティングソフトウェア.md "wikilink")[テープドライブ](../Page/テープドライブ.md "wikilink")に対応
  - [VESA](../Page/VESA.md "wikilink")規格のビデオモード
  - ベースシステムの[Perl](../Page/Perl.md "wikilink")4を5に置き換え
  - [KerberosIV](../Page/ケルベロス認証.md "wikilink")

<!-- end list -->

  - 3.1-RELEASE\[63\]

<!-- end list -->

  - [USB対応](../Page/ユニバーサル・シリアル・バス.md "wikilink")
  - ユーザー認証システムのPAM(Pluggable Authentication Modules)機能

<!-- end list -->

  - 3.2-RELEASE\[64\]

<!-- end list -->

  - ベースシステムに[Internet Systems Consortiumの](https://ja.wikipedia.org/wiki/Internet_Systems_Consortium "wikilink")[DHCP](https://ja.wikipedia.org/wiki/Dynamic_Host_Configuration_Protocol "wikilink")[クライアントを追加](../Page/クライアント_\(コンピュータ\).md "wikilink")
  - USB対応の拡充
  - ([NTFSへのダイレクト接続](../Page/NT_File_System.md "wikilink")・[ISO 9660\#JolietlISO9660の拡張規格「Joliet」等の](https://ja.wikipedia.org/wiki/ISO_9660#JolietlISO9660の拡張規格「Joliet」 "wikilink"))改良されたファイルシステム対応

<!-- end list -->

  - 3.3-RELEASE\[65\]

<!-- end list -->

  - 改良されたUSB対応
  - [RAID](../Page/RAID.md "wikilink")を実行できるストレージ・マネージャーの「vinum」のメジャーアップデート
  - [IPFWの改良](https://ja.wikipedia.org/wiki/ipfirewall "wikilink")
  - [電源管理インタフェース「APM」](../Page/Advanced_Power_Management.md "wikilink")
  - データリンク層インタフェース「BPF」を標準設定可能にした
  - 多くのドライバを追加

<!-- end list -->

  - 3.4-RELEASE\[66\]

<!-- end list -->

  - Netgraph
  - 「vinum」のRAID-5対応
  - [ICMPとその他のセキュリティ修正](../Page/Internet_Control_Message_Protocol.md "wikilink")

<!-- end list -->

  - 3.5-RELEASE\[67\]

<!-- end list -->

  - 「vinum」の重要なアップデート
  - [オーディオミキサー](../Page/ミキシング・コンソール.md "wikilink")
  - [HTTPインストレーションオプション](../Page/Hypertext_Transfer_Protocol.md "wikilink")

<!-- end list -->

  - 4.0-RELEASE\[68\]

<!-- end list -->

  - [KAMEプロジェクト](../Page/KAMEプロジェクト.md "wikilink")によるBSD標準[IPv6](https://ja.wikipedia.org/wiki/IPv6 "wikilink")スタックとBSD標準[IPsec](../Page/IPsec.md "wikilink")スタック
  - ベースシステムに[OpenSSH](../Page/OpenSSH.md "wikilink")を統合
  - 新しいATA/ATAPIドライバ(全てのATAに準拠したディスクとATAPI準拠の[CD-ROM](../Page/CD-ROM.md "wikilink")・[CD-R](../Page/CD-R.md "wikilink")・[CD-RW](../Page/CD-RW.md "wikilink")・[DVD-ROM](https://ja.wikipedia.org/wiki/DVD#DVD-ROM "wikilink")・[DVD-RAM](../Page/DVD-RAM.md "wikilink")・[LS120](../Page/スーパーディスク.md "wikilink")・[ZIP](../Page/ZIP_\(記憶媒体\).md "wikilink")・テープドライブ)
  - [SVR4](https://ja.wikipedia.org/wiki/UNIX_System_V#SVR4 "wikilink")[バイナリ](../Page/バイナリ.md "wikilink")ファイル用のエミュレータ
  - burncdプログラム
  - USBイーサネットアダプタの対応
  - [accept()フィルタ](https://ja.wikipedia.org/wiki/ソケット_\(BSD\)#accept\(\) "wikilink")
  - [Telnet](../Page/Telnet.md "wikilink")暗号化

<!-- end list -->

  - 4.1-RELEASE\[69\]

<!-- end list -->

  - システムコールKqueue
  - IPsecの改良
  - [DEC Alpha対応を拡大](https://ja.wikipedia.org/wiki/DEC_Alpha "wikilink")
  - 標準インストール作業でのUSB対応

<!-- end list -->

  - 4.1.1-RELEASE\[70\]

<!-- end list -->

  - ブリッジされた環境設定での仮想イーサネットデバイスドライバ
  - [ATA100のコントローラ対応](https://ja.wikipedia.org/wiki/ハードディスクドライブ#過去に製造を行っていた主な企業 "wikilink")

<!-- end list -->

  - 4.2-RELEASE\[71\]

<!-- end list -->

  - 初期的なUSBスキャナーの対応
  - USBモデムの対応
  - バッファオーバーフロー時のバグ修正
  - Portsの再構築

<!-- end list -->

  - 4.3-RELEASE\[72\]

<!-- end list -->

  - サウンドドライバのアップデート
  - TCPのバグ修正
  - システムコールkqueueのデバイス層への拡張

<!-- end list -->

  - 4.4-RELEASE\[73\]

<!-- end list -->

  - 新プロセッサ([Crusoe](../Page/Crusoe.md "wikilink") *et al.*)の検出
  - [SSEの対応](../Page/ストリーミングSIMD拡張命令.md "wikilink")
  - smbfs([CIFS](../Page/Server_Message_Block.md "wikilink"))のカーネル対応
  - [IPv6](https://ja.wikipedia.org/wiki/IPv6 "wikilink")スタックのアップデート

<!-- end list -->

  - 4.5-RELEASE\[74\]

<!-- end list -->

  - [TCPの改良](../Page/Transmission_Control_Protocol.md "wikilink")(スループット・パフォーマンス・[サービス拒否攻撃の鎮静等](../Page/DoS攻撃.md "wikilink"))
  - 標準で[Soft updatesが出来るようになる](../Page/Soft_updates.md "wikilink")
  - Linuxulatorの改良
  - 起動ローダが16Kのディスクブロック長を持つファイルシステムからの起動に対応(それまでは8K)

<!-- end list -->

  - 4.6-RELEASE\[75\]

<!-- end list -->

  - [XFree86](../Page/XFree86.md "wikilink")のバージョンを4.2.0にアップデート
  - ドライバの追加とアップデート

<!-- end list -->

  - 4.6.2-RELEASE\[76\]

<!-- end list -->

  - ATAデバイスにアクセスした時に生じていたエラーを修正
  - セキュリティ関連のバグを修正

<!-- end list -->

  - 4.7-RELEASE\[77\]

<!-- end list -->

  - 新しいUSBデバイスとディスクコントローラ
  - (デフォルトでは無効な)[IPFW](https://ja.wikipedia.org/wiki/ipfirewall "wikilink")2が追加

<!-- end list -->

  - 4.8-RELEASE\[78\]

<!-- end list -->

  - 初期的な[Firewireと](../Page/IEEE_1394.md "wikilink")[ハイパースレッディングの対応](../Page/ハイパースレッディング・テクノロジー.md "wikilink")
  - [OpenBSD](../Page/OpenBSD.md "wikilink")由来の新しいカーネル暗号化フレームワークを統合
  - ata(4)ドライバがCAMレイヤとCAMドライバ( cd(4)・da(4)・st(4)・pass(4))を経由してATAデバイスをSCSIデバイスとしてアクセスできるようにする機能に対応

<!-- end list -->

  - 4.9-RELEASE\[79\]

<!-- end list -->

  - [PAE機能に対応](../Page/物理アドレス拡張.md "wikilink")
  - [IPFW修正](https://ja.wikipedia.org/wiki/ipfirewall "wikilink")

<!-- end list -->

  - 4.10-RELEASE\[80\]

<!-- end list -->

  - USB 2.0に対応
  - Portsにports/CHANGESとports/UPDATINGが追加

<!-- end list -->

  - 4.11-RELEASE\[81\]

<!-- end list -->

  - [XFree86](../Page/XFree86.md "wikilink")のバージョンを4.4.0にアップデート
  - インタフェース単位で制御可能なpolling(4)機能が実装されて全てのネットワークドライバは ifconfig(8) を使って制御できるようになる

<!-- end list -->

  - 5.0-RELEASE\[82\]

<!-- end list -->

  - [UltraSPARCと](../Page/UltraSPARC_T1.md "wikilink")[IA-64](../Page/IA-64.md "wikilink")のプロセッサの対応
  - ([ジャイアントロック](https://ja.wikipedia.org/wiki/ジャイアントロック "wikilink")からカーネルの大部分のリソースが開放された)カーネル[ロック機構を変更したSMPの対応](https://ja.wikipedia.org/wiki/ロック_\(情報工学\)#スレッドにおけるロック "wikilink")
  - GEOM
  - KSE(カーネルスケジュールエンティティ)
  - TrustedBSDから導入された [強制アクセス制御](https://ja.wikipedia.org/wiki/強制アクセス制御 "wikilink")
  - バックグラウンドで動く[fsck](https://ja.wikipedia.org/wiki/fsck "wikilink")
  - [Bluetooth](../Page/Bluetooth.md "wikilink")
  - [ACPI](../Page/Advanced_Configuration_and_Power_Interface.md "wikilink")
  - [CardBus](../Page/PCカード.md "wikilink")
  - [デバイスファイル](../Page/デバイスファイル.md "wikilink")を実行するdevfs
  - [UFS2の対応](../Page/Unix_File_System.md "wikilink")
  - [ユニバーサルディスクフォーマット](../Page/ユニバーサルディスクフォーマット.md "wikilink")の対応
  - [DRIのドライバ](https://ja.wikipedia.org/wiki/ダイレクト・レンダリング・インフラストラクチャ "wikilink")
  - ユーザー認証を行うためのAPIである「Pluggable Authentication Modules」
  - デフォルトカーネルでの[386対応削除](../Page/Intel_80386.md "wikilink")
  - kernfs[UUCPの除去](../Page/Unix_to_Unix_Copy_Protocol.md "wikilink")
  - 従来のBSDゲームをベースシステムからPortsに移動
  - [Perl](../Page/Perl.md "wikilink")をベースシステムから除去
  - [NetBSD](../Page/NetBSD.md "wikilink")から「rc.d」フレームワークを導入
  - BSDPANの追加
  - 標準でcdboot起動ローダを使用

<!-- end list -->

  - 5.1-RELEASE\[83\]

<!-- end list -->

  - [x86-64の実験的なサポート](https://ja.wikipedia.org/wiki/x64 "wikilink")
  - マルチスレッドプロセスの為の実験的な1:1スレッド(1個のカーネルスレッドを1個のユーザーランドスレッドが占有して利用)とM:Nスレッディングライブラリ
  - 実験的な [Name Service Switch](https://ja.wikipedia.org/wiki/Name_Service_Switch "wikilink")
  - [PAE](../Page/物理アドレス拡張.md "wikilink")
  - GEOMとオプションから必須機能になったdevfs
  - Linuxulatorでの[IPv6](https://ja.wikipedia.org/wiki/IPv6 "wikilink")対応
  - 実験的なULEスケジューラ
  - 7年間正常に動作していなかった「XNS([Xeroxネットワークシステム](../Page/ゼロックス.md "wikilink"))」の対応削除
  - CAMレイヤが2<sup>32</sup>個以上のブロックを持つデバイスに対応
  - rcNG(/etcにある起動スクリプトが削除され、[NetBSD](../Page/NetBSD.md "wikilink")から移植された「rc.d」システムに置き換え)
  - [XFree86](../Page/XFree86.md "wikilink")のバージョンを4.3.0にアップデート
  - デンマーク語(da_DK.ISO8859-1)翻訳プロジェクトが発足

<!-- end list -->

  - 5.2-RELEASE\[84\]

<!-- end list -->

  - [x86-64のアーキテクチャが](https://ja.wikipedia.org/wiki/x64 "wikilink")、サポートレベル順位「Tier 1」とされ、ほぼフル対応の対象となった
  - swap pagerの更新
  - カーネルが「Protocol Independent Multicastルーティング」(pim(4))に対応
  - IPv6とIPSec修正と更新がKAMEプロジェクトから統合
  - Bluetoothプロトコルスタックが更新
  - (ata(4)ドライバの ジャイアントカーネルロックが外されて)ata(4)ドライバが大きく書き直された
  - NFSv4クライアントが実装
  - トルコ語(tr_TR.ISO8859-9)翻訳プロジェクトが開始\[85\]
  - i386版で浮動小数点エミュレーションが削除\[86\]
  - IDE・[SATA](https://ja.wikipedia.org/wiki/シリアルATA "wikilink")・[802.11a/b/gデバイスのドライバ対応が追加](../Page/IEEE_802.11.md "wikilink")・改善、実験的なIPトラフィックのフィルタリング機能と転送機能のマルチスレッド化

<!-- end list -->

  - 5.2.1-RELEASE\[87\]

<!-- end list -->

  - バグとセキュリティを修正
  - ATA/IDEおよびSATAの処理の著しい改善

<!-- end list -->

  - 5.3-RELEASE\[88\]

<!-- end list -->

  - ネットワークインターフェースでの[キュー制御をする](../Page/キュー_\(コンピュータ\).md "wikilink")[ALTQ](https://ja.wikipedia.org/wiki/ALTQ "wikilink")
  - ネットワークとソケットサブシステムは、マルチスレッド化され、リエントラント(再入可能)対応となる
  - 新しいデバッグフレームワークKDB(Kernel debugger)の追加
  - [TLSの動的](https://ja.wikipedia.org/wiki/スレッド局所記憶 "wikilink")・静的リンクの対応
  - [OpenBSD](../Page/OpenBSD.md "wikilink")から[PF導入](../Page/PF_\(ファイアウォール\).md "wikilink")
  - GCC 3.4.2、Binutils 2.15、gdb 6.1に更新\[89\]
  - カーネルでWindows [NDISネットワークドライバに対応](../Page/Network_Driver_Interface_Specification.md "wikilink")。i386プラットフォームでバイナリ互換インターフェイスを導入
  - [XFree86](../Page/XFree86.md "wikilink")に替わって、[X.org](../Page/X_Window_System.md "wikilink") 6.7対応
  - サウンドカードのドライバ再構築
  - 暗号処理アクセラレータ

<!-- end list -->

  - 5.4-RELEASE\[90\]

<!-- end list -->

  - [OpenBSD](../Page/OpenBSD.md "wikilink")より[CARP](https://ja.wikipedia.org/wiki/Common_Address_Redundancy_Protocol "wikilink")(サーバ冗長化プロトコル)導入\[91\]

<!-- end list -->

  - 5.5-RELEASE\[92\]

<!-- end list -->

  - デュアルコアプロセッサの両方のコアがカーネルを使用して標準でSMPに対応できる

<!-- end list -->

  - 6.0-RELEASE\[93\]

<!-- end list -->

  - 実験的な[PowerPC](../Page/PowerPC.md "wikilink")対応
  - [無線](../Page/無線.md "wikilink")セキュリティプロトコル[WPA](../Page/Wi-Fi_Protected_Access.md "wikilink")
  - wirelessアダプタのドライバ追加
  - [802.11g/i](../Page/IEEE_802.11.md "wikilink")・[802.1Xと](../Page/IEEE_802.1X.md "wikilink")[WME/WMM完全対応](https://ja.wikipedia.org/wiki/Wireless_Multimedia_Extensions "wikilink")
  - ファイルシステムとディスクへの直接アクセスのパフォーマンスの改良

<!-- end list -->

  - 6.1-RELEASE\[94\]

<!-- end list -->

  - ブート時の特別なオプションがなくともPS/2キーボードとUSBキーボードの共存が可能な「キーボード多重化」\[95\]
  - ファイルシステムの安定性改善
  - 多くのBluetoothデバイスの自動化された環境設定
  - イーサネット対応ドライバ
  - [SAS](../Page/Serial_Attached_SCSI.md "wikilink")/[SATA対応RAIDコントローラ](https://ja.wikipedia.org/wiki/シリアルATA "wikilink")

<!-- end list -->

  - 6.2-RELEASE\[96\]

<!-- end list -->

  - [Xboxのアーキテクチャ対応](../Page/Xbox_\(ゲーム機\).md "wikilink")
  - OpenBSM
  - セキュリティイベント監査
  - [ipfirewall](https://ja.wikipedia.org/wiki/ipfirewall "wikilink")
  - セキュリティ修正とエラーパッチのバイナリアップデート
  - OpenIPMI(公開されたシステム管理の為のインタフェース)

<!-- end list -->

  - 6.3-RELEASE\[97\]

<!-- end list -->

  - [X.orgのバージョンを](../Page/X_Window_System.md "wikilink")7.3にアップデート
  - [UnionFS](https://ja.wikipedia.org/wiki/UnionFS "wikilink")の再実装
  - 「freebsd-update」アップデートツール追加
  - [OpenBSD](../Page/OpenBSD.md "wikilink")/N[NetBSD](../Page/NetBSD.md "wikilink")からlagg(4)ドライバ導入\[98\]

<!-- end list -->

  - 6.4-RELEASE\[99\]

<!-- end list -->

  - 共通鍵ブロック暗号[Camellia cipherに対応](../Page/Camellia.md "wikilink")
  - 起動ローダの変更(USBデバイスからの起動と[GPT対応BIOSからのGPTラベルデバイスの起動が可能となる](../Page/GUIDパーティションテーブル.md "wikilink"))
  - [malloc](https://ja.wikipedia.org/wiki/malloc "wikilink")(9)で割り付けられたメモリのためのバッファ間違いを検出する「RedZone」
  - DVDでの [ISOイメージ](https://ja.wikipedia.org/wiki/ISOイメージ "wikilink")([x86-64と](https://ja.wikipedia.org/wiki/x64 "wikilink")[i386対応](../Page/Intel_80386.md "wikilink"))

<!-- end list -->

  - 7.0-RELEASE\[100\] drop support for [DEC Alpha](https://ja.wikipedia.org/wiki/DEC_Alpha "wikilink")\[101\]

<!-- end list -->

  - 実験的な[ZFS](../Page/ZFS.md "wikilink")と[GPT](https://ja.wikipedia.org/wiki/GUID_Partition_Table "wikilink")
  - 実験的な[SCTPを実装](../Page/Stream_Control_Transmission_Protocol.md "wikilink")\[102\]
  - [ARMアーキテクチャ](../Page/ARMアーキテクチャ.md "wikilink")の追加対応
  - サウンドインターフェースの[HDA対応](https://ja.wikipedia.org/wiki/High_Definition_Audio "wikilink")
  - [mallocの古い実装(phkmalloc)をJason Evansが開発したjemallocに置換](https://ja.wikipedia.org/wiki/malloc#FreeBSDとNetBSD "wikilink")
  - [DEC Alpha対応を終了](https://ja.wikipedia.org/wiki/DEC_Alpha "wikilink")

<!-- end list -->

  - 7.1-RELEASE\[103\]

<!-- end list -->

  - [DTrace](../Page/DTrace.md "wikilink")
  - ULEスケジューラが[i386](../Page/Intel_80386.md "wikilink")/[x86-64版の標準スケジューラとなる](https://ja.wikipedia.org/wiki/x64 "wikilink")

<!-- end list -->

  - 7.2-RELEASE\[104\]

<!-- end list -->

  - [UltraSPARC IIIに対応](../Page/SPARC.md "wikilink")
  - 仮想メモリサブシステムでのsuperpagesのトランスペアレント(利用者にソフトウェアの存在・作用が意識されない)利用
  - [jailの実装](../Page/FreeBSD_jail.md "wikilink")

<!-- end list -->

  - 7.3-RELEASE\[105\]\[106\]

<!-- end list -->

  - 新しいgptzfsboot起動ローダ([GPTと](https://ja.wikipedia.org/wiki/GUID_Partition_Table "wikilink")[ZFS](../Page/ZFS.md "wikilink")に対応)
  - ZFSのバージョンを13にアップデート
  - [Perl](../Page/Perl.md "wikilink")のバージョンを5.10にアップデート
  - [VIA Nanoプロセッサに対応](../Page/VIA_Nano.md "wikilink")

<!-- end list -->

  - 7.4-RELEASE\[107\]

<!-- end list -->

  - [UltraSPARC IV/IV+](../Page/SPARC.md "wikilink")・[SPARC Vプロセッサに追加対応](../Page/SPARC.md "wikilink")64
  - (miibusでの)[IEEE 802.3全二重フローコントロール](../Page/イーサネット.md "wikilink")

<!-- end list -->

  - 8.0-RELEASE\[108\]

<!-- end list -->

  - 新たなUSB実装「USB2」
  - jailが"Vimage Jail"にアップデート\[109\]
  - 改善されたULE3スケジューラ
  - superpages対応
  - NFSv4対応

<!-- end list -->

  - 8.1-RELEASE\[110\]

<!-- end list -->

  - HAST(Highly Available STorage)フレームワーク追加\[111\]
  - [IPFW](https://ja.wikipedia.org/wiki/ipfirewall "wikilink") and dummynet improvements
  - PowerPC G5でのSMPサポート（デフォルトでは無効）
  - MS-DOS用ファイルシステムMP-safe
  - ZFS版対応のブートローダzfsloader追加
  - NFSv4 [ACLが](../Page/アクセス制御リスト.md "wikilink") [UFS版と](../Page/Unix_File_System.md "wikilink")[ZFS](../Page/ZFS.md "wikilink")版に正式対応

<!-- end list -->

  - 8.2-RELEASE\[112\]

<!-- end list -->

  - LinuxulatorにVL4(Video4Linux)をインポート

<!-- end list -->

  - 8.3-RELEASE\[113\]\[114\]

<!-- end list -->

  - graid(8) GEOMクラスを各種BIOSベースのソフトウェアRAIDコントローラー対応のために追加 (ataraid(4)の代替)
  - ZFSのバージョンを28にアップデート
  - [DTrace](../Page/DTrace.md "wikilink")がLinuxulatorバイナリに対応
  - TCP/IPスタックがカーネルモジュール化された輻輳制御フレームワークmod_cc(9)に対応

<!-- end list -->

  - 8.4-RELEASE\[115\]\[116\]\[117\]

<!-- end list -->

  - セキュリティ関連を含むバグ修正
  - ZFSの強化

<!-- end list -->

  - 9.0-RELEASE\[118\]\[119\]

<!-- end list -->

  - ユーザーレベルDTraceの導入
  - [GCCに代わって](https://ja.wikipedia.org/wiki/GNU_Compiler_Collection "wikilink")[Clang](https://ja.wikipedia.org/wiki/Clang "wikilink")と[LLVM](../Page/LLVM.md "wikilink")をベースシステムに追加
  - [USB](../Page/ユニバーサル・シリアル・バス.md "wikilink")3.0に対応
  - [FFSがsoftupdatesジャーナリングに対応](../Page/Unix_File_System.md "wikilink")
  - ATA/SATAドライバーがCAMフレームワークに統合され、AHCIサポート
  - ZFSのバージョンを28にアップデート
  - 新型インストーラーのbsdinstall(8)
  - FreeBSD/ppcが[PLAYSTATION3に対応](https://ja.wikipedia.org/wiki/PLAYSTATION_3 "wikilink")

<!-- end list -->

  - 9.1-RELEASE\[120\]\[121\]

<!-- end list -->

  - GEM/KMSをサポートする新しいIntel GPUドライバ
  - 高速ユーザー空間パケットI/Oフレームワークとして、netmap(4)を追加
  - サウンドドライバのアップデート
  - IPv6の改善
  - LLVM libc++とlibcxxrtを含む、新しいC++11スタック
  - jailがdevfs・nullfs・ZFSに対応
  - sched_ule(4)によるSMTのロードのバランスの改良

<!-- end list -->

  - 9.2-RELEASE\[122\]\[123\]

<!-- end list -->

  - ZFSファイルシステムがLZ4圧縮形式に対応
  - ZFSファイルシステムがSSDのTRIMに対応
  - [Firewireドライバ削除](../Page/IEEE_1394.md "wikilink")
  - [i386](../Page/Intel_80386.md "wikilink")/[x86-64アーキテクチャにvirtio](https://ja.wikipedia.org/wiki/x64 "wikilink")(4)ドライバを追加

<!-- end list -->

  - 10.0-RELEASE\[124\]\[125\]

<!-- end list -->

  - GCCの廃止とclang/LLVMに正式移行 (C/C++コンパイラーおよびライブラリでGPLフリーの達成)
  - bhyve(8)やvirtio(4)の追加など、Microsoft Hyper-V向けの仮想化機能の強化
  - USBをアップデート
  - ファイル保護機能capsicumをカーネルでサポート
  - pkg(7)をデフォルトのパッケージ管理ユーティリティとし、pkg_add(1)、pkg_delete(1)および関連ツールは廃止
  - [DNSサーバ](../Page/DNSサーバ.md "wikilink")の[BIND](../Page/BIND.md "wikilink")廃止
  - LDNS(DNSライブラリ)とDNSキャッシュサーバーとして[Unbound](https://ja.wikipedia.org/wiki/Unbound "wikilink")を採用
  - [Raspberry Pi](https://ja.wikipedia.org/wiki/Raspberry_Pi "wikilink")・[IEEE 802.11s](https://ja.wikipedia.org/wiki/IEEE_802.11s "wikilink")・[FUSEの追加対応](../Page/Filesystem_in_Userspace.md "wikilink")
  - ZFSをサーバーのrootファイルシステムとして利用可能
  - [GNU](../Page/GNU.md "wikilink")のツールを[BSDライセンス](../Page/BSDライセンス.md "wikilink")版に代替

<!-- end list -->

  - 10.1-RELEASE\[126\]\[127\]

<!-- end list -->

  - ユニコードをサポートし、グラフィックモードの利用を改善するシステムコンソールvt(4)の追加\[128\]
  - amd64のみ[UEFIからの起動を初期サポート](https://ja.wikipedia.org/wiki/Unified_Extensible_Firmware_Interface#セキュアブート "wikilink")
  - [IPv4](../Page/IPv4.md "wikilink")および[IPv6](https://ja.wikipedia.org/wiki/IPv6 "wikilink")[スタック](../Page/スタック.md "wikilink")に対し、音声などマルチメディアに適しているとされる（RFC 3828で定義された）[UDP-Lite](https://ja.wikipedia.org/wiki/UDP-Lite "wikilink")[プロトコル](../Page/プロトコル.md "wikilink")サポートを追加\[129\]
  - [ハイパーバイザ](../Page/ハイパーバイザ.md "wikilink")bhyve(4)にzfsファイルシステムからの起動サポート
  - ハイパーバイザbhyve(4)へFreeBSD/i386ゲストのサポート機能を追加
  - ファイルシステムの自動マウント機能であるautofs(5)を導入
  - [armv6カーネルへ](../Page/ARMアーキテクチャ.md "wikilink")[SMPサポート機能を追加](../Page/ヘテロジニアスマルチコア.md "wikilink")

<!-- end list -->

  - 10.2-RELEASE\[130\]\[131\]

<!-- end list -->

  - [Linux](../Page/Linux.md "wikilink")の[CentOS](../Page/CentOS.md "wikilink") 6互換環境を提供するlinux_base-c6をデフォルトで採用
  - Linuxカーネル3.8.13に対応するようにDRMコードを更新し、複数の[X.Org Serverを同時に実行することも可能とする](../Page/X.Org_Server.md "wikilink")
  - [ZFS](../Page/ZFS.md "wikilink")のパフォーマンスと信頼性の改善
  - resolvconfはプライバシー保護機能を強化したバージョン3.7.0に、[GNOME](../Page/GNOME.md "wikilink")は3.14.2に、[KDE](../Page/KDE.md "wikilink")は4.14.3にそれぞれアップデート
  - ARMサポートを強化

<!-- end list -->

  - 10.3-RELEASE\[132\]\[133\]\[134\]

<!-- end list -->

  - [UEFI](https://ja.wikipedia.org/wiki/UEFI "wikilink")システムに自動モードでroot-on-ZFSインストールが作成可能となる
  - rerootの初期実装にrebootが追加
  - [GNOME](../Page/GNOME.md "wikilink")は3.16.2に、[TeX LiveはTL](https://ja.wikipedia.org/wiki/TeX_Live "wikilink")2015に、[X.Org Serverは](../Page/X.Org_Server.md "wikilink")1.17.4にそれぞれアップデート

<!-- end list -->

  - 10.4-RELEASE\[135\]

<!-- end list -->

  - eMMCストレージのフルサポート
  - fsck_ffs(8)ユーティリティにおけるGPTディスクラベルでのオルタネートスーパーブロックのサポート
  - ユーザランドコアダンプにヒューマンリーダブルなクラッシュレポートを報告するイベントを発生させることができる機能を追加(デフォルトでは無効)

<!-- end list -->

  - 11.0-RELEASE\[136\]

<!-- end list -->

  - ZFSディスクの[ホットスペア](https://ja.wikipedia.org/wiki/ホットスペア "wikilink")およびオートリプレースを可能にするzfsd(8)デーモンを導入
  - ハイパーバイザ[bhyve](https://ja.wikipedia.org/wiki/bhyve "wikilink")(8)においてネイティブグラフィック機能をサポート
  - AArch64(arm64)アーキテクチャのサポート追加
  - libblacklist(3)ライブラリおよびアプリケーションを[NetBSD](../Page/NetBSD.md "wikilink")より移植
  - 802.11nワイヤレスのサポート追加
  - [OpenSSH](../Page/OpenSSH.md "wikilink")を7.2.p2へアップデート
  - OpenSSH DSA鍵生成をデフォルトで無効化およびプロトコル1のサポート廃止
  - より多くのワイヤレスネットワークドライバを追加
  - svnlite(1)をバージョン1.9.4へアップデート

<!-- end list -->

  - 11.1-RELEASE\[137\]\[138\]

<!-- end list -->

  - Clang、LLVM、LLD、LLDB、libc++をバージョン4.0.0へアップデート
  - Microsoft Hyper-V Generation 2サポートの追加

<!-- end list -->

  - 11.2-RELEASE\[139\]\[140\]

<!-- end list -->

  - Clang、LLVM、LLDB、compiler-rtをバージョン6.0.0へアップデート
  - 特定のDTraceプローブのトリガプロセスを見るdwatch(1)、EFIブートマネージャーの操作ができるefibootmgr(8)、El Toritoブートカタログ情報を閲覧できるetdump(1)などのユーティリティの追加

<!-- end list -->

  - 12.0-RELEASE\[141\]\[142\]\[143\]

<!-- end list -->

  - Clang、LLVM、LLDB、compiler-rtをバージョン6.0.1へアップデート
  - NUMAオプションがamd64 GENERICとMINIMALカーネル設定でデフォルトで有効となった
  - jail(8)内部におけるbhyve(8)利用のサポート

<!-- end list -->

  - 12.1-RELEASE

<!-- end list -->

  - Cで書かれたSSL/TLSプロトコル（RFC 5246）の実装であるBearSSLをベースシステムにインポートした。OpenSSLはバージョン1.1.1dにアップデート
  - clang、llvm、lld、lldb、compiler-rt、libc++は最新の8.0.1となった。
  - zfsでは、ブックマーク向けのsendサブコマンドと合わせて「-v」、「-n」、「-P」フラグのサポートなどが加わった。

## 対応アーキテクチャ

FreeBSDでは、2018年現在は対応アーキテクチャを「Tier 1～4」までの4段階で管理している\[144\]。

### Tier 1

最新のRELEASE版について、公式サイトにてインストールイメージが配布されている[アーキテクチャ](../Page/コンピュータ・アーキテクチャ.md "wikilink")。いわゆる「フルサポートアーキテクチャ」であり、ドキュメントなどもまずはこの層に属するアーキテクチャ向けに整備される。

  - [i386](../Page/Intel_80386.md "wikilink")（一般的な[x86](https://ja.wikipedia.org/wiki/x86 "wikilink")ベースの32ビット[CPU](../Page/CPU.md "wikilink")）
  - [AMD64](https://ja.wikipedia.org/wiki/x64 "wikilink")（[インテル](https://ja.wikipedia.org/wiki/インテル "wikilink")、[AMD等のCPU向けの一般的な](https://ja.wikipedia.org/wiki/アドバンスト・マイクロ・デバイセズ "wikilink")64ビットCPU）

### Tier 2

開発・サポートプロジェクトが継続しているアーキテクチャ。公式サイトでインストールイメージも配布されているが、熟成度が低いとされて部分的なサポートのみとなっている。

  - [ARM](../Page/ARMアーキテクチャ.md "wikilink")\[145\]
      - 32bitシステムの「arm」と64bitシステムの「arm64(aarch64)」の両方をサポートしている。
      - [Raspberry Pi等の多数の著名な](https://ja.wikipedia.org/wiki/Raspberry_Pi "wikilink")[シングルボードコンピュータ](https://ja.wikipedia.org/wiki/シングルボードコンピュータ "wikilink")も含む。これらは公式でSDカードイメージが配布されている。
  - [SPARC](../Page/SPARC.md "wikilink")
      - 「sparc64」として64bitシステムのみサポートされている。
  - [PowerPC](../Page/PowerPC.md "wikilink")
      - 32bitシステムの「powerpc」と64bitシステムの「powerpc64」の両方をサポートしている。
  - [MIPS](https://ja.wikipedia.org/wiki/MIPS "wikilink")

### Tier 3

試験的に開発が行われているアーキテクチャ。開発状況によっては予告なくFreeBSDのソースツリーから外される可能性がある\[146\]。

  - [RISC-V](https://ja.wikipedia.org/wiki/RISC-V "wikilink")

### Tier 4

完全にサポート外のアーキテクチャ。\[147\]。

### 過去に対応していたアーキテクチャ

  - [DEC Alpha](https://ja.wikipedia.org/wiki/DEC_Alpha "wikilink") - 6.x系までサポート
  - [Xbox](../Page/Xbox_\(ゲーム機\).md "wikilink") - 6.x系で一時開発されていた\[148\]
  - [IA-64](../Page/IA-64.md "wikilink")（インテル [Itanium](../Page/Itanium.md "wikilink")）- 10.x系まで
  - [PC-9800シリーズ](../Page/PC-9800シリーズ.md "wikilink") - 8.x系までTier 1だったが、9.x系以降はTier 2になった。12.x系でTier 4へ移行し、pc98のソースコードは削除された

\[149\]。9.x系以降はpc98のISO Imageはリリースされていない\[150\]。

## ロゴ

長年、FreeBSDのロゴはBeastieとも呼ばれる通常のBSDデーモンであった。しかしながら、Beastieは、FreeBSDに特有のものではなかった。最初に現れたのは[1976年](../Page/1976年.md "wikilink")の[ベル研究所](../Page/ベル研究所.md "wikilink")による[UNIX](../Page/UNIX.md "wikilink")Tシャツであり、最も人気のあるBSDデーモンのバージョンは[アニメ](../Page/アニメ.md "wikilink")[監督](../Page/監督.md "wikilink")の[ジョン・ラセター](../Page/ジョン・ラセター.md "wikilink")によって[1984年](../Page/1984年.md "wikilink")に描かれ始めたものである\[151\]。いくつかのFreeBSDに特有のバージョンは、細川達己によって後に描かれたものである\[152\]。

## 関連プロジェクト、関連ディストリビューション

### FreeSBIEプロジェクト

[FreeSBIE](../Page/FreeSBIE.md "wikilink")プロジェクトは、FreeBSDベースの[Live CD環境を提供している](../Page/Live_CD.md "wikilink")。

### FreeNASプロジェクト

[FreeNAS](https://ja.wikipedia.org/wiki/FreeNAS "wikilink")プロジェクトは、FreeBSDベースの、Webベースでの操作を可能とした[NASファイルサーバ用OS環境を提供している](../Page/ネットワークアタッチトストレージ.md "wikilink")。

### XigmaNAS(旧 NAS4Free)プロジェクト

[XigmaNAS](https://ja.wikipedia.org/wiki/XigmaNAS "wikilink")プロジェクトは、FreeNASプロジェクトから分離したNASファイルサーバ用OS環境プロジェクトである。

### TrueOS（旧PC-BSD）プロジェクト

TrueOS(旧PC-BSD)プロジェクトは、FreeBSDをデスクトップ・サーバと両方に対応したディストリビューションを提供している。

### HardendBSD プロジェクト

[HardenedBSD](https://ja.wikipedia.org/wiki/HardenedBSD "wikilink")は、セキュリティ対策を拡充するため[2014年](../Page/2014年.md "wikilink")にフォークしたディストリビューション。

## 使用例

  - [PlayStation 4](https://ja.wikipedia.org/wiki/PlayStation_4 "wikilink") - 搭載されるOS「Orbis OS」はFreeBSD 9.0ベースである\[153\]。
  - [PlayStation Vita](https://ja.wikipedia.org/wiki/PlayStation_Vita "wikilink") - 搭載されているOSにFreeBSDが使用されている\[154\]\[155\]。
  - [PlayStation 3](https://ja.wikipedia.org/wiki/PlayStation_3 "wikilink") - 搭載されているOSにFreeBSDが使用されている\[156\]\[157\]。
  - [Nintendo Switch](https://ja.wikipedia.org/wiki/Nintendo_Switch "wikilink") - [任天堂](../Page/任天堂.md "wikilink")が公式にアナウンスをしているわけではないが、本体の知的財産表記にFreeBSDカーネルの権利表記が掲載されており、少なくともコンポーネントの一部を用いていることが確認できる。
  - [VIERA](../Page/VIERA.md "wikilink") - インターネットサービス「ビエラ・コネクト」に利用されているOSはFreeBSDベースである\[158\]。
  - [JUNOS](https://ja.wikipedia.org/wiki/JUNOS "wikilink") - OSはFreeBSDカーネルをベースとしている。
  - [OpenServer](https://ja.wikipedia.org/wiki/OpenServer "wikilink") - OpneServer 10よりFreeBSDベースとなった\[159\]。
  - [Apple](https://ja.wikipedia.org/wiki/Apple "wikilink")社の[macOS](https://ja.wikipedia.org/wiki/macOS "wikilink") - 基盤となる[DarwinがFreeBSDの一部機能を取り入れている](../Page/Darwin_\(オペレーティングシステム\).md "wikilink")\[160\]。後に[iOS](https://ja.wikipedia.org/wiki/IOS_\(アップル\) "wikilink")、[watchOS](https://ja.wikipedia.org/wiki/watchOS "wikilink")、[tvOS](https://ja.wikipedia.org/wiki/tvOS "wikilink")に派生。

## 脚注

## 関連項目

  - [FreeBSDディストリビューション](../Page/FreeBSDディストリビューション.md "wikilink")
  - [FreeBSD jail](../Page/FreeBSD_jail.md "wikilink")
  - [BSDの子孫](../Page/BSDの子孫.md "wikilink")
  - [BSD](../Page/BSD.md "wikilink")
  - [macOS](https://ja.wikipedia.org/wiki/macOS "wikilink")
  - [DragonFly BSD](../Page/DragonFly_BSD.md "wikilink")
  - [NetBSD](../Page/NetBSD.md "wikilink")
  - [OpenBSD](../Page/OpenBSD.md "wikilink")
  - [TrueOS](../Page/TrueOS.md "wikilink")
  - [Unix File System](../Page/Unix_File_System.md "wikilink") - FreeBSDのファイルシステム。5.xからはUFS2を採用。
  - [ZFS](../Page/ZFS.md "wikilink") - 新しいファイルシステム。FreeBSD 8.0で正式に搭載されている。
  - [DTrace](../Page/DTrace.md "wikilink") 7.1より採用。
  - [VIMAGE](https://ja.wikipedia.org/wiki/VIMAGE "wikilink") - Network Stack Virtualization。FreeBSD 8.2にて、「VIMAGE(virtualized network stack) is a highly experimental feature」のような「WARNING」を告げられる。FreeBSD 9.1-RELEASEでも「WARNING」は変わらず。主支援は[The FreeBSD Network Stack Virtualization Project](http://imunes.tel.fer.hr/virtnet/)にて。
  - [ジャーナリングファイルシステム](../Page/ジャーナリングファイルシステム.md "wikilink") - FreeBSD 9 以降で、FreeBSD FFSにおいて従来からのSoft Updatesに加えジャーナリング機能が追加されたJournaled Soft Updates (SU+J)が使えるようになっている。
  - [FreeBSDでKDE2にパッチをあてるにはどうすればよいですか?](https://ja.wikipedia.org/wiki/FreeBSDでKDE2にパッチをあてるにはどうすればよいですか? "wikilink") - ロシアで流行した[インターネットスラング](../Page/インターネットスラング.md "wikilink")

## 外部リンク

  - オフィシャルページ
      -
      - [The FreeBSD Forums](https://forums.freebsd.org/)

      - [FreeBSD財団](https://www.freebsdfoundation.org/)

      - [FreeBSD 日本語マニュアル検索](http://www.jp.freebsd.org/man-jp/search.html)

      - [Japan FreeBSD Users Group](http://www.jp.FreeBSD.org/)
  - ニュース
      - [FreeBSD newsflash](https://www.freebsd.org/ja/news/newsflash.html)
      - [FreeBSD in the Press](https://www.freebsd.org/ja/news/press.html)
      - [FreeBSD Daily Topics](https://gihyo.jp/admin/clip/01/fdt)
      - [BSD Planet](http://news.bsdplanet.net/)
      - [BSD Newsletter](http://www.bsdnewsletter.com/)
      - [OSNews.com](https://www.osnews.com/topic/freebsd/)
      - [BSDtalk Podcasts](https://bsdtalk.blogspot.com/)
  - ソフトウェア
      - [FreeBSD Ports](https://www.freebsd.org/ja/ports/)
      - [Fresh Ports](https://www.freshports.org/commits.php)
  - その他
      - [The BSD License](https://www.opensource.org/licenses/bsd-license.php)

      - [FreeBSD Logo](https://www.freebsd.org/logo.html)

      - [FreeBSD Mall](https://www.freebsdmall.com)

      -
[Category:FreeBSD](https://ja.wikipedia.org/wiki/Category:FreeBSD "wikilink") [Category:BSD](https://ja.wikipedia.org/wiki/Category:BSD "wikilink") [Category:オープンソースソフトウェア](https://ja.wikipedia.org/wiki/Category:オープンソースソフトウェア "wikilink") [Category:1993年のソフトウェア](https://ja.wikipedia.org/wiki/Category:1993年のソフトウェア "wikilink")

1.  [About FreeBSD](https://www.freebsd.org/about.html)
2.  [Supported FreeBSD Releases](http://security.freebsd.org/#sup) - FreeBSD Security Information
3.  [BSD\#4.4BSD と派生](https://ja.wikipedia.org/wiki/BSD#4.4BSD_と派生 "wikilink")
4.
5.  [英語版:「FreeBSD」の記事の記述より](https://ja.wikipedia.org/wiki/:en:FreeBSD#Version_history "wikilink")
6.  [\*BSD で kqueue・kevent を使ってみよう - X68000.qed.net](http://x68000.q-e-d.net/~68user/net/c-kqueue-1.html)
7.  [FreeBSD 5.3-RELEASE 公開 | スラッシュドット・ジャパン](http://slashdot.jp/story/04/11/07/1110203/FreeBSD-5.3-RELEASE-%E5%85%AC%E9%96%8B)
8.  [FreeBSD 5.0-RELEASE 初期利用者のための手引き](http://www.freebsd.org/ja/releases/5.0R/early-adopter.html)
9.
10. [FreeBSD/GEOM - 情報科学研究室 - 秋田大学](http://www.is.akita-u.ac.jp/pukiwiki/?FreeBSD%2FGEOM)
11. [16.13. ディスクパーティションの暗号化](http://www.freebsd.org/doc/ja/books/handbook/disks-encrypting.html)
12. [システム旅譚 - FreeBSD 6.0-RELEASEの新機能と変更点を見る](http://news.mynavi.jp/articles/2005/11/07/freebsd/index.html)
13. [TrustedBSD - Lavender PukiWiki](http://www.lavender.org/~mouri/pukiwiki/index.php?TrustedBSD)
14. [OpenBSM: Open Source Basic Security Module (BSM) Audit Implementation](http://www.trustedbsd.org/openbsm.html)
15. [Next: BSM 監査の有効化と使用 - Oracle Documentation](http://docs.oracle.com/cd/E19227-01/821-0424/enablingusingbsmauditing/index.html)OracleによるSolaris OSでのBSM監査の説明でFreeBSDではないが、用語の解説はちゃんとされています。
16. [FreeBSD/pc98 6.0-RELEASE リリースノート](http://www.gulf.or.jp/~too/freebsd/6.0/relnotes-60j.html)
17.
18. [jemallocとかLD_PRELOADについて調べてみた - As a Futurist...](http://www.mew.org/~kazu/material/2008-malloc.pdf)
19.
20.
21.
22.
23.
24.
25.
26.
27.
28.
29.
30. <http://www.freebsd.org/releases/9.1R/schedule.html>
31. <http://www.freebsd.org/releases/9.2R/schedule.html>
32. <http://www.freebsd.org/releases/9.3R/schedule.html>
33. [FreeBSD 9.0-RELEASE 登場 | スラッシュドット・ジャパン オープンソース](http://opensource.slashdot.jp/story/12/01/13/0157258/FreeBSD-9.0-RELEASE-%E7%99%BB%E5%A0%B4)
34.
35.
36.
37.
38.
39.
40.
41.
42.
43.
44.
45.
46. <https://mag.osdn.jp/19/11/05/173000>
47.
48.
49.
50.
51.
52.
53.
54.
55.
56.
57.
58.
59.
60.
61.
62.
63.
64.
65.
66.
67.
68.
69.
70.
71.
72.
73.
74.
75.
76.
77.
78.
79.
80.
81.
82.
83.
84.
85.
86.
87.
88.
89.
90.
91.
92.
93.
94.
95.
96.
97.
98.
99.
100.
101.
102.
103.
104.
105.
106.
107.
108.
109.
110.
111.
112.
113.
114.
115.
116.
117.
118.
119.
120.
121.
122.
123.
124.
125.
126.
127.
128.
129.
130.
131.
132.
133.
134.
135.
136.
137.
138.
139.
140.
141.
142.
143.
144. [Support for Multiple Architectures](https://www.freebsd.org/doc/en_US.ISO8859-1/articles/committers-guide/archs.html)
145. [FreeBSD/ARM プロジェクト](https://www.freebsd.org/ja/platforms/arm.html)
146.
147.
148. [FreeBSD/xbox Project](https://www.freebsd.org/platforms/xbox.html)
149. [FreeBSD/pc98 プロジェクト](https://www.freebsd.org/ja/platforms/pc98.html)
150. [FreeBSD 9.0-RELEASE Announcement](https://www.freebsd.org/releases/9.0R/announce.html)
151.
152.
153.
154.
155.
156.
157.
158.
159.
160.
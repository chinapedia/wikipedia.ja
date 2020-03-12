> この記事は[Rational ClearCase](https://ja.wikipedia.org/wiki/Rational_ClearCase)から翻訳されています。


**Rational ClearCase** は、[ソースコード](../Page/ソースコード.md "wikilink")などの[ソフトウェア開発](../Page/ソフトウェア開発.md "wikilink")資産のための[バージョン管理システム](../Page/バージョン管理システム.md "wikilink")（[構成管理](../Page/構成管理.md "wikilink")、[SCMも含む](../Page/ソフトウェア構成管理.md "wikilink")）である。[IBM](../Page/IBM.md "wikilink") の[ラショナル](../Page/ラショナル.md "wikilink")部門が開発している。ClearCase は中規模以上の大きな商用ソフトウェアプロジェクトでよく使われ、数百人から数千人の開発者を管理できる。

ClearCase 本体にも SCM 機能があるが、それとは別に UCM という SCM 機能もある。[Linux](../Page/Linux.md "wikilink")、[Solaris](../Page/Solaris.md "wikilink")、[Windowsといった様々なプラットフォーム上で動作する](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")。巨大なバイナリファイルや多数のファイル、巨大なリポジトリを扱える。分岐、ラベル付け、ディレクトリのバージョン付けなどが可能。

## 歴史

ClearCase は[1992年](../Page/1992年.md "wikilink")、Atria Software が [UNIX](../Page/UNIX.md "wikilink") 向けに開発し、後に Windows 版もリリースされた。Atria の開発者の一部はそれ以前に[アポロコンピュータ](../Page/アポロコンピュータ.md "wikilink")の *DSEE*（[Domain](https://ja.wikipedia.org/wiki/Domain/OS "wikilink") Software Engineering Environment）の開発に携わっていた。1989年にアポロコンピュータが[ヒューレット・パッカード](../Page/ヒューレット・パッカード.md "wikilink")に買収されると、彼らはアポロを離れ、Atria に移ったのである\[1\]\[2\]。Atria は後に Pure Software と合併して PureAtria となった。それがさらに[ラショナル](../Page/ラショナル.md "wikilink")に吸収され、さらに IBM に買収された。IBM はその後も ClearCase の開発と販売を続けている。ソフトウェア開発企業にとっては ClearCase は有名な製品である。

### DSEE

DSEE には ClearCase に見られる様々な概念が既に導入されていた。[Domain/OS](https://ja.wikipedia.org/wiki/Domain/OS "wikilink") の[ファイルシステム](../Page/ファイルシステム.md "wikilink")では、ファイルアクセス時に特殊なハンドラプログラムを呼び出すことができ、DSEE はそれを使って、特定のファイルがオープンされたときに自動的にバージョン管理されたコピーと入れ替えていた。バージョン機能はユーザー環境に常駐しており、バージョン管理されたファイルへのアクセスは全てリダイレクトされ、印刷やエディタでの参照も例外ではない。

DSEE の中心となるのは、全てのソフトウェアモジュールとそれらの依存関係を記述したファイルである。このファイルは手動で作成する必要があり、大規模システムではその作業が重大な障害となった。しかし、いったん作成できれば、DSEE は[ビルドを行うのに最適な方法を計算でき](https://ja.wikipedia.org/wiki/ビルド_\(ソフトウェア\) "wikilink")、現在のビルドとバージョン指定が同じであるような以前に処理された全モジュールを再利用できた。

DSEE はまた、"version spec" または "thread" の概念を導入した。これはあるユーザー環境やビルドにおいて、含まれても良いバージョンのリストである。重要な点は、thread においてビルドのシグネチャやソフトウェアリリースのシグネチャが利用できるようにした点である。従って、1つの thread に含まれる要素は次のようになる。

  - 編集目的で確保されているコピー（チェックアウト）
  - 最新バージョン（開発者専用）
  - あるファイルの分岐バージョン（開発の別の線上のバージョン）
  - ラベル付きバージョン（特定のリビジョンについて作業する開発者向け）
  - ビルド XYZ でのバージョン
  - ソフトウェアリリース x.y.z でのバージョン

thread はファイルごとに一番上から一番下まで処理された。ある開発者の thread は、一番上に確保されたものがあり、それにラベル付きバージョンが続いているかもしれない。既存リリースを素早くバグ修正する場合、thread は「確保」されたものとリリースのシグネチャ付きのものとなることもある。

Domain/OS のファイルシステムの機能（不可視なリダイレクト）は通常備わっていないため、ClearCase は後述するように MVFS（MultiVersion File System）という仮想ファイルシステムを使う。"thread" の概念は *dynamic view* に対応している。ある view における派生オブジェクト（ビルドによって生成されるオブジェクト）のサポートは、DSEE の考え方に類似している。

## View

ClearCase でバージョン管理されているオブジェクトは、その履歴情報と共にリポジトリに格納されている。このリポジトリを **VOB**（Versioned Object Base）と呼ぶ。ClearCase で特徴的な点は、そのバージョン化ファイルシステム（MVFS）であり、*dynamic view* を通して VOB を仮想ファイルシステムとしてマウントでき、一貫性のあるバージョン群を選んで派生オブジェクトを生成できる。dynamic view はこれを Software Configuration にマップできる。これはリポジトリ/サンドボックス型とは異なり、製造物を初期段階から管理できる（チェックイン前から管理でき、ソースファイルだけでなく派生オブジェクトも管理できる）。

それとは別に、ClearCase は *snapshot view* と呼ばれるものもサポートしており、これは1つまたは複数のVOBにまたがったディレクトリツリーの単なるコピーである。snapshot view は、VOB のデータへのアクセスに仮想ファイルシステムを使用しない。その代わり、snapshot view は VOB データのコピーをローカル（ユーザーのコンピュータ）に保持する。snapshot view はネットワークが切断されていても利用でき、後で接続が確立したときにVOBと同期させることができる。この操作モードは、[CVS](../Page/Concurrent_Versions_System.md "wikilink") (Concurrent Versions System) が一般に使われているモードと似ている。

クライアントコンピュータ上のソフトウェアという観点では、view は別のファイルシステムに見える。view 内で新たなファイルを通常の[OSの手段を使って作成した場合](../Page/オペレーティングシステム.md "wikilink")（コピーやエディタのセーブなど）、ClearCase はそのファイルを "view-private" ファイルとして生成する。そのファイルは他の view からは見えない。このため、開発者各人が同じディレクトリ構成でビルドしていたとしても、個々の開発者の修正は他人の環境には影響を与えない（ただし、dynamic view であれば、ファイルアクセスに[分散ファイルシステム](../Page/分散ファイルシステム.md "wikilink")が絡んでくるので、オーバーヘッドがかかる）。view-private ファイル（あるいはディレクトリ）は任意の時点でバージョン管理される要素に変換でき、それによって他の開発者からも見えるようになる。

各開発者は一般に1つ以上の view を使って作業する。開発者間で view を共有できた方が便利な場合もあるが、ブランチの共有が使われるのが一般的である。ブランチの階層がよく使われ、開発プロジェクト全体で1つの開発ブランチを共有し、その中の小さいチームがサブブランチを共有し、個々の開発者が個人的なブランチを持つ。ある修正がより大きなグループに対しても十分に安定していると判断したとき、それを親ブランチとマージすることができる。

## Configuration specification

ClearCase では、各 view は対応する *configuration specification* で制御される（*config spec* などと呼ぶ）。これは[ドメイン固有言語](../Page/ドメイン固有言語.md "wikilink")の一種でテキストファイルに格納されていて、実行時に自動的にコンパイルされる。config spec には、その view で見えるべき要素（ファイルやディレクトリ）とそれら要素のバージョンが指定されている。ある要素のどのバージョンが見えるべきかを決定する際、ClearCase は configuration specification を先頭から一行ずつ一致が見つかるまで見ていく。configuration specification の例を以下に示す。

    # この view でチェックアウトされた全要素を見せる。他の規則に優先する。
    element * CHECKEDOUT

    # ある要素が 'module2_dev_branch' 上にバージョンを持つ場合、
    # そのブランチの最新バージョンをこの view での見えるバージョンとする。
    element * .../module2_dev_branch/LATEST

    # 'somefile' という名前のファイルは場所に関わらずメインブランチの最新版を見せる。
    element .../somefile /main/LATEST

    ### 実際には、上のコメントは正しくない。この規則は、チェックアウトバージョン
    # がなく（規則1）、/module2_dev_branch 上にもバージョンがない（規則2）場合のみ、
    # somefile@@/main/LATEST を選択する。ClearCase は上位の規則がマッチすれば
    # それ以降を見ないので、最初の2つの規則がマッチしない場合のみ、この規則が適用される。

    # 特定ファイルの特定バージョンを使う。この規則は次の規則より上位におく必要がある。
    element /vobs/project1/module1/a_header.h /main/proj_dev_branch/my_dev_branch1/14

    # 'project1/module1' のパス配下で 'PROJ1_MOD2_LABEL_1' というラベルの付いた要素を見せる。
    # また、このパスでのチェックアウトを禁止する。
    element /vobs/project1/module1/... PROJ1_MOD2_LABEL_1 -nocheckout

    # 'project1/module2' のパス配下で  'ANOTHER_LABEL' というバージョンの全要素を見せる。
    # チェックアウトされたものがあれば、その要素を現在の見えるバージョンからブランチさせ
    # 'module2_dev_branch' というブランチに追加する。
    element /vobs/project1/module2/... ANOTHER_LABEL -mkbranch module2_dev_branch

configuration specification は、'include' 文を使って他の configuration specification を参照できる。

## 独自機能

  - VOB (VERSIONED OBJECT BASE)
    ファイル要素、ディレクトリ要素、派生オブジェクト、およびそれらに関連したメタデータをバージョンごとに格納するリポジトリ。MultiSite を使うと、1つの VOB を別々のサイトに複製することができる。
  - Configuration Record（構成履歴）
    dynamic view でビルドしたとき、ClearCase はビルド中に読み込んだ全ファイルのバージョンを記録する。この処理を build-auditing という。依存関係情報は隠し configuration record に格納されている。configuration record を使って、ビルドで使った全ファイルを見せる新たな view を設定可能である。また、configuration record に記録されている全ファイルにラベルを付けることもできる。
  - ビルド回避
    MVFS を使うと、ある dynamic view で作成された派生オブジェクトを他の dynamic view と共有することができる。共有が可能となるのは両者の configuration record が全く同じ場合である。共有された派生オブジェクトは、物理的には VOB サーバにあり view にはない。
  - Unix/Windows 相互運用性
    UNIX系サーバ上の VOB は Windows クライアント上の view からアクセス可能である。Windows サーバ上の VOB は、UNIX系クライアントからは snapshot view としてしかアクセスできない。
  - 他の製品との連携
    [ラショナル](../Page/ラショナル.md "wikilink")の [ClearQuest](https://ja.wikipedia.org/wiki/ClearQuest "wikilink") や [Rose](https://ja.wikipedia.org/wiki/Rational_Rose "wikilink") といった製品は ClearCase と連携する。他にも [TextPad](../Page/TextPad.md "wikilink")、[Microsoft Visual Studio](https://ja.wikipedia.org/wiki/Microsoft_Visual_Studio "wikilink")、[Code::Blocks](../Page/Code::Blocks.md "wikilink")、[Eclipseなどともプラグインを通して連携する](../Page/Eclipse_\(統合開発環境\).md "wikilink")。[emacs](https://ja.wikipedia.org/wiki/emacs "wikilink")\[3\] や [vim](https://ja.wikipedia.org/wiki/vim "wikilink")\[4\] のプラグインもある。

## 欠点

  - トランザクションが[アトミックでない](../Page/不可分操作.md "wikilink")。
  - コードベースが古く、新規機能追加が遅い。
  - 非常に複雑で、構成設定に注意を要する。
  - 遅い。単純なコミットやチェックアウトが数分かかることも稀ではない。

## 関連項目

  - [バージョン管理システム](../Page/バージョン管理システム.md "wikilink")
  - [ソフトウェア構成管理](../Page/ソフトウェア構成管理.md "wikilink")

## 脚注

## 外部リンク

  - [IBM Rational ClearCase](http://www-06.ibm.com/jp/software/rational/products/scm/cc/) 日本語公式ページ
  - [IBM developerWorks' Rational ClearCase V7.0 site](http://www.ibm.com/developerworks/downloads/r/rcc/?S_TACT=105AGY59&S_CMP=WIKIDL&ca=dtl-13rcconline) - フリーな試用版
  - [Eclipse ClearCase Integration, Open Source](http://eclipse-ccase.sourceforge.net)
  - [ClearCase Web Client, Commercial](https://www.redhat.com/apps/isv_catalog/AppProfile.html?application_id=1554)
  - [Rational ClearCase Commands Reference](http://www.ipnom.com/ClearCase-Commands/)
  - [SRA Rationalホームページ](http://www.sra.co.jp/Rational/product/soft/clearcase.html)

[Category:IBMのソフトウェア](https://ja.wikipedia.org/wiki/Category:IBMのソフトウェア "wikilink") [Category:バージョン管理システム](https://ja.wikipedia.org/wiki/Category:バージョン管理システム "wikilink")

1.
2.  Andrew DeFaria （2004年12月21日）[Re: cvs vs. clearcase?](http://www.mail-archive.com/info-cvs@gnu.org/msg31053.html) info-cvs@gnu.org
3.  [Emacs ClearCase Integration, Open Source](http://vc-clearcase.sourceforge.net/)
4.  [ccase.vim : Script to setup maps/menus to add in using Clearcase.](http://www.vim.org/scripts/script.php?script_id=15) - vim online
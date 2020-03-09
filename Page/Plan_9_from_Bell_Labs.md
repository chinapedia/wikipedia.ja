> この記事は[Plan 9 from Bell Labs](https://ja.wikipedia.org/wiki/Plan_9_from_Bell_Labs)から翻訳されています。


（通称 ）は、主に研究用に使われている[分散オペレーティングシステム](https://ja.wikipedia.org/wiki/分散オペレーティングシステム "wikilink")。[ベル研究所](https://ja.wikipedia.org/wiki/ベル研究所 "wikilink")の  で1980年代中ごろから2002年まで、[UNIX](../Page/UNIX.md "wikilink")の研究上の後継として開発された。Plan 9 は、ネットワークやユーザインタフェースまで含めたあらゆるシステムインタフェースを、個別のインタフェースではなくファイルシステムを通して統一的に表現することを特徴とする。Plan 9 は[9P](https://ja.wikipedia.org/wiki/9P "wikilink")プロトコルを使い、ユーザーにワークステーション毎に独立した作業環境を提供することを目指している。現在もベル研究所とPlan 9コミュニティによって活発に開発がつづいている\[1\]。

Plan 9 は、[UNIX](../Page/UNIX.md "wikilink")の流れを汲む[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink") (OS) の一種であり、開発に当たってUNIXの設計の問題点を改善することを念頭に置かれている\[2\]。

## 名称の由来

Plan 9の"9"には、UNIX version 8の次の版という意味もあると言われている（UNIX version 9と10も作られているが）。

また、フルネームを*Plan9 from Bell Labs*だとしているが、これは[エド・ウッド](https://ja.wikipedia.org/wiki/エド・ウッド "wikilink")の[史上最低の映画と評された](https://ja.wikipedia.org/wiki/B級映画 "wikilink")[SF映画](https://ja.wikipedia.org/wiki/サイエンス・フィクション "wikilink") [Plan 9 from Outer Space](https://ja.wikipedia.org/wiki/プラン9・フロム・アウタースペース "wikilink") から来ている\[3\]。また、プロジェクトのマスコットキャラクターGlendaの名も、同じくエド・ウッド作品[グレンとグレンダ](https://ja.wikipedia.org/wiki/グレンとグレンダ "wikilink")にちなむ。初期の（つまり間に合わせの）ウインドウシステムは（9に足りてない、という意味もあるが）[フェデリコ・フェリーニ](https://ja.wikipedia.org/wiki/フェデリコ・フェリーニ "wikilink")の名画「[8 1/2](https://ja.wikipedia.org/wiki/8_1/2 "wikilink")」に掛けており、[ハッカー](https://ja.wikipedia.org/wiki/ハッカー "wikilink")流ジョークの側面でもUNIXの後継であることを伺わせる。

## 歴史

Plan 9はベル研究所内の主な研究用プラットフォームとしてUNIXを代替し、システムの使用とプログラミングについての本来のUNIXのモデル、特に分散[マルチユーザー](https://ja.wikipedia.org/wiki/マルチユーザー "wikilink")環境にいくつかの変更を加えることの研究対象ともなった。[1980年代](../Page/1980年代.md "wikilink")中ごろに始まった当初、Plan 9はベル研究所内部のプロジェクトだった。

Plan 9は[ベル研究所](https://ja.wikipedia.org/wiki/ベル研究所 "wikilink")の Computing Science Research Center のメンバーが開発した。そのグループは[UNIX](../Page/UNIX.md "wikilink")や[C言語](../Page/C言語.md "wikilink")を開発したグループと同一である。当初チームは[ロブ・パイク](https://ja.wikipedia.org/wiki/ロブ・パイク "wikilink")や[ケン・トンプソン](https://ja.wikipedia.org/wiki/ケン・トンプソン "wikilink")らが率い、Computing Techniques Research Department のリーダーとして[デニス・リッチー](https://ja.wikipedia.org/wiki/デニス・リッチー "wikilink")が支援した。開発には、[ブライアン・カーニハン](https://ja.wikipedia.org/wiki/ブライアン・カーニハン "wikilink")、[ビャーネ・ストロヴストルップ](https://ja.wikipedia.org/wiki/ビャーネ・ストロヴストルップ "wikilink")らも貢献している\[4\]。

[1992年](https://ja.wikipedia.org/wiki/1992年 "wikilink")、大学向けに初めてリリースした。[1995年](https://ja.wikipedia.org/wiki/1995年 "wikilink")、一般向けの商用OSとしてリリースした。[1990年代](../Page/1990年代.md "wikilink")末、ベル研究所を引き継いだ[ルーセント・テクノロジー](https://ja.wikipedia.org/wiki/ルーセント・テクノロジー "wikilink")は、このプロジェクトの商業化を断念。[2000年](../Page/2000年.md "wikilink")、[オープンソース](../Page/オープンソース.md "wikilink")ライセンスで非商用リリースを行った。[2002年](../Page/2002年.md "wikilink")、新たに[フリーソフトウェア](../Page/フリーソフトウェア.md "wikilink")ライセンスで非商用リリースを行った。

[ベル研究所](https://ja.wikipedia.org/wiki/ベル研究所 "wikilink")の研究員や[マサチューセッツ工科大学](https://ja.wikipedia.org/wiki/マサチューセッツ工科大学 "wikilink")などの Plan 9ユーザーコミュニティが、[ISOイメージ](https://ja.wikipedia.org/wiki/ISOイメージ "wikilink")の形で頻繁なマイナーリリースを継続している\[5\]。その開発はいまだにベル研究所がホスティングしている。開発ソースツリーは[9P](https://ja.wikipedia.org/wiki/9P "wikilink")プロトコルか[HTTPプロトコルでアクセスでき](../Page/Hypertext_Transfer_Protocol.md "wikilink")、インストールしたものを最新に保つのに使われている\[6\]。OS本体をISOイメージとしている以外に、アプリケーションやツールのリポジトリもベル研究所がホスティングしている。

## 概要

### UNIXとの違い

UNIXの問題点とは、1つのコンピュータを多くの利用者が共有することを前提に作られており、多くのコンピュータを多くの利用者が共有することは考えられていないことである。その結果、利用者が特定のコンピュータを占有することになり、それらのコンピュータは雑然と管理運営されることになる。

UNIXの当初の環境では、どの端末からコンピュータを使っても同じ環境を再現できた。Plan 9では、それをネットワーク上に繋がった[分散処理環境上で実現する](https://ja.wikipedia.org/wiki/分散コンピューティング "wikilink")。

また、UNIXの開発がローカルな[ファイルシステム](https://ja.wikipedia.org/wiki/ファイルシステム "wikilink")をどう表現するかということをテーマとして始まったのに対して、Plan 9は、ローカルであれリモートであれ、[リソースというものにどうアクセスするかということを課題とする研究として始まった](https://ja.wikipedia.org/wiki/計算資源 "wikilink")。

したがって、UNIXの設計当初になかった[ネットワークの利用を前提とし](https://ja.wikipedia.org/wiki/コンピュータネットワーク "wikilink")、[端末](https://ja.wikipedia.org/wiki/端末 "wikilink")、[CPU](../Page/CPU.md "wikilink")[サーバ](https://ja.wikipedia.org/wiki/サーバ "wikilink")、[ファイルサーバ](https://ja.wikipedia.org/wiki/ファイルサーバ "wikilink")、[認証](https://ja.wikipedia.org/wiki/認証 "wikilink")サーバを分けることで[セキュリティの向上を狙う](https://ja.wikipedia.org/wiki/コンピュータセキュリティ "wikilink")。また、ファイルサーバは毎日のスナップショットを保存し、ユーザーレベルでのバックアップ作業をほぼ不要なものとした。

当初はMOジュークボックスなどの利用を考えており、[ハードディスク](https://ja.wikipedia.org/wiki/ハードディスク "wikilink")はMOジュークボックスの[キャッシュ](https://ja.wikipedia.org/wiki/キャッシュ "wikilink")という考え方だった。最近ではハードディスクの大容量化と低廉化が進んでいるため、MOジュークボックスの代わりにハードディスクを使えるようになりつつある。

### 全てのリソースはファイルである

UNIX以前、多くのオペレーティングシステムはそれぞれのデバイスにアクセスするのに、それぞれ異なる機構を用意していた。例えば、[ディスクドライブ](https://ja.wikipedia.org/wiki/ディスクドライブ "wikilink")にアクセスする[APIは](https://ja.wikipedia.org/wiki/アプリケーションプログラミングインタフェース "wikilink")、シリアルポートでデータ送受信をするためのAPIとは全く異なるし、[プリンター](https://ja.wikipedia.org/wiki/プリンター "wikilink")にデータを送信するAPIとも全く異なっていた。

UNIXはそのような差異をなくそうとし、全ての[入出力](https://ja.wikipedia.org/wiki/入出力 "wikilink")をファイル操作でモデル化しようとした。そのため、全デバイスドライバが制御手段として *read* および *write* 操作に対応する必要に迫られた。こうすることで、[mvや](https://ja.wikipedia.org/wiki/Mv_\(UNIX\) "wikilink")[cpなどのユーティリティで](https://ja.wikipedia.org/wiki/Cp_\(UNIX\) "wikilink")、実装の詳細を気にすることなくデバイスからデバイスにデータを転送することができるようになった。しかし、UNIXでは多くの重要な概念（例えば、プロセス状態の制御など）はファイルにきれいにマッピングされなかった。[ソケットや](https://ja.wikipedia.org/wiki/ソケット_\(BSD\) "wikilink") [X Window System](https://ja.wikipedia.org/wiki/X_Window_System "wikilink") といった新たな機能が追加されたとき、それらはファイルシステムの外に存在するようになった。新たなハードウェア機能（ソフトウェアがCDのイジェクトを制御するなど）も、[ioctl](https://ja.wikipedia.org/wiki/ioctl "wikilink")[システムコール](https://ja.wikipedia.org/wiki/システムコール "wikilink")などのハードウェア固有制御機構を使うようになった。

Plan 9研究プロジェクトは、ファイル中心の見方への回帰を目標とし、それ以外の手法を排除した（その一部は、外のUnixへ与えた影響が限定的であった、ベル研版UNIXのバージョン8, 9, 10から引き継がれたものである）。Plan 9のプログラムから見れば、ネットワークやユーザインタフェースのリソース（ウィンドウなど）も含めたあらゆるリソースが階層型ファイルシステムの一部となっており、それ以外の特別なインタフェースは使わない\[7\]。

### 分散アーキテクチャ

Plan 9は単一のマシンにインストールして、自立したシステムとして使うこともできる。しかし、OSの個々の機能コンポーネントをそれぞれ別のハードウェアプラットフォームに配置することもできる。模範的な配置では、Rioという[GUIを動作させた軽量な端末をユーザーが使い](https://ja.wikipedia.org/wiki/グラフィカルユーザインタフェース "wikilink")、ネットワーク経由でCPUサーバに接続して、そちらで計算量の多いプロセスを実行し、さらに別のマシンに用意した永続的データストレージをファイルサーバとして使う。最近のデスクトップコンピュータでは、複数の[仮想機械](https://ja.wikipedia.org/wiki/仮想機械 "wikilink")を動作させて、この環境を1台のマシン上に再現することができる。

## 設計

Plan 9設計者は[マイクロカーネル](https://ja.wikipedia.org/wiki/マイクロカーネル "wikilink")と似たような目標を掲げていたが、実際のアーキテクチャや実現方法は異なる。Plan 9の設計目標は次の項目を含む。

  - ファイルとしてのリソース
    全ての[リソースを階層型](https://ja.wikipedia.org/wiki/計算資源 "wikilink")[ファイルシステム](https://ja.wikipedia.org/wiki/ファイルシステム "wikilink")内のファイルとして表現する。
  - 名前空間
    アプリケーションから見て、ネットワークは単一で一貫した[名前空間](https://ja.wikipedia.org/wiki/名前空間 "wikilink")であり、それも階層型ファイルシステムとして表現される。しかし、実体はローカルまたはリモートに分離されたリソース群である。各プロセスの名前空間はそれぞれ独立に構築でき、ユーザーは異なる複数の名前空間のアプリケーション群を同時に扱える。
  - 標準通信プロトコル
    [9P](https://ja.wikipedia.org/wiki/9P "wikilink")という標準プロトコルを使い、ローカルやリモートの区別なく、あらゆるリソースにアクセスする。

### ファイルシステム、ファイル、名前

Plan 9では、[ファイルも](https://ja.wikipedia.org/wiki/ファイル_\(コンピュータ\) "wikilink")[画面](https://ja.wikipedia.org/wiki/画面 "wikilink")も[ユーザー](https://ja.wikipedia.org/wiki/ユーザー "wikilink")も[コンピュータ](../Page/コンピュータ.md "wikilink")も、それぞれに固有のパス名が対応している。それらは全て既存のUNIXの手法で操作されるが、それに加えて任意のオブジェクトにパス名としての名前をつけることができる（[World Wide Webの](../Page/World_Wide_Web.md "wikilink")[URIシステムに似ている](https://ja.wikipedia.org/wiki/Uniform_Resource_Identifier "wikilink")）。UNIXでは、例えば[プリンター](https://ja.wikipedia.org/wiki/プリンター "wikilink")などの機器は `/dev` 配下の名前で表されるが、ネットワーク経由のプリンターはそのように表されることはなく、直接接続しているプリンターだけである。Plan 9ではプリンターはファイルとして仮想化され、ネットワーク上のあらゆるプリンターに任意のワークステーションから同じ方法でアクセスできる。

また Plan 9では、実世界では同一のオブジェクトにユーザーごとに異なる名前を付けることができる。各ユーザーは各種オブジェクトを自分の名前空間に集め、個人的環境を生成できる。UNIXでは類似の概念として、別のユーザーからコピーされることでユーザーが特権を得るというコンセプトがあるが、Plan 9 ではそれを全てのオブジェクトに拡張している。ユーザーは容易に自分自身の「クローン」を生成することができ、それに変更を加え、それらが作成されたリソースに影響を与えることなく削除できる。

### Union ディレクトリ

UNIXでは、「リンク」やファイルシステムの「マウント」といった考え方で各種リソース群からファイルシステムを構築できる。それらを利用すると、元々のディレクトリは見えなくなる。例えば、"net" というディレクトリに新たなファイルシステムをマウントすると、元々の "net" ディレクトリ配下の内容にはアクセスできなくなる。

Plan 9は「unionディレクトリ」という考え方を導入した。これは、異なる媒体やネットワークにまたがるリソース群をまとめたディレクトリであり、他のディレクトリと透過的に連結することができる。例えば、他のコンピュータの `/bin` ディレクトリを手元のコンピュータの同名のディレクトリと連結し、ローカルとリモートのアプリケーションに透過的にアクセスできるようにすることができる。同様に、`/dev` に外部のデバイスやリソースをまとめると、全くコードを追加することなくネットワーク経由でデバイスを共有できる。

[Linuxディストリビューション](https://ja.wikipedia.org/wiki/Linuxディストリビューション "wikilink")の[Live CDの多くは](https://ja.wikipedia.org/wiki/Live_CD "wikilink")、この機能の限定版である union mount という機能を実装しているものが増えている。

### /proc

`/proc` ディレクトリには動作中プロセスの一覧があり、それぞれの状態を示している。いわゆる「プロセスファイルシステム（[procfs](https://ja.wikipedia.org/wiki/procfs "wikilink")）」と呼ばれるもので、標準化はされておらず詳細は異なるが、[Linux](https://ja.wikipedia.org/wiki/Linux "wikilink")その他多くのUnixでも採用されている。プロセスは名前付きのオブジェクト（infoファイルやcontrolファイルのあるサブディレクトリ）として `/proc` 配下にあり、他のカーネルリソースと共に動的I/Oチャネルもあり、ユーザーはそれにコマンドを送ったり、データを読み取ったりできる。ユーザーは一部のシステムコールを使ったプログラムをコンパイルしてカーネルとやり取りする必要はなく、[`ls`](https://ja.wikipedia.org/wiki/Ls_\(UNIX\) "wikilink") や [`cat`](https://ja.wikipedia.org/wiki/Cat_\(UNIX\) "wikilink") といったコマンドでプロセスを検索し、操作することができる。

他のマシンの `/proc` ディレクトリは他の特殊なファイルシステムと同様、ユーザーの名前空間にマウントでき、ローカルにあるかのようにそれを使うことができる。これにより、複数のマシンから成る分散コンピューティング環境ができる。ユーザーの机上にある端末、データを格納してあるファイルサーバ、高速CPUや認証や[ゲートウェイ](https://ja.wikipedia.org/wiki/ゲートウェイ "wikilink")などのその他サーバ群などがあり、それら全てがユーザーが見慣れたディレクトリ階層を使っている。ユーザーは[ファイルサーバ](https://ja.wikipedia.org/wiki/ファイルサーバ "wikilink")やサーバで動作中のアプリケーションやネットワーク上のプリンターなどを集め、端末上の個人的名前空間にそれらをまとめることができる。

### /net

Plan 9は多数の通信プロトコルやデバイスドライバのインタフェースとしてのシステムコールを持たない。例えば、`/net` はTCP/IP全体のAPIの役割を担っており、スクリプトやコマンドで操作可能で、制御ファイルに書き込むことでコネクションを読み書きできる。`/net/tcp` や `/net/udp` といったサブディレクトリはそれぞれのプロトコルへのインタフェースとして使うことができる。例えば、[NATを実装する場合](https://ja.wikipedia.org/wiki/ネットワークアドレス変換 "wikilink")、公開IPアドレスを持つ境界線上のマシンの `/net` をマウントし、内部ネットワークで Plan 9 の[9P](https://ja.wikipedia.org/wiki/9P "wikilink")プロトコルを使い、プライベートIPアドレスの内部ネットワークから当該マシンへと接続する。[VPNを実装する場合は](https://ja.wikipedia.org/wiki/Virtual_Private_Network "wikilink")、インターネット上でセキュアな9Pプロトコルを使い、リモートのゲートウェイの `/net` ディレクトリをマウントすればよい。

`/net` で union ディレクトリを使う例を示す。[オブジェクト指向プログラミング](https://ja.wikipedia.org/wiki/オブジェクト指向プログラミング "wikilink")における継承のように、（リモートの） `/special` に対して、別のローカルなディレクトリを連結（重ね合わせ）する。すると同じ名前の制御ファイルはあとから重ねた方で隠され、新たな制御ファイルは追加された状態になる。言ってみれば union ディレクトリは、元の2つの親を継承した子オブジェクトのようなものである。オリジナルの機能は部分的に変更されることがある。これを `/net` ファイルシステムで考えると、`/net/udp` サブディレクトリを更新または隠蔽すると、UDPインタフェースにローカルなフィルタープロセスをかませて制御または拡張でき、`/net/tcp` は元のまま、おそらくリモートマシン上で動作させておくといったことができる。名前空間はプロセス単位に設定可能なので、信頼できないアプリケーションに対して制限を加えた `/net` union ディレクトリを見せることで、ネットワークアクセスを制限することができる。

このような機構は、異なるシステム上で異なる言語で書かれたファイルシステムや「オブジェクト」を容易に連結でき、プログラマからはファイルシステムの名前付けやアクセス制御やセキュリティの大部分が透過的となる。

類似の機構として4.4BSDの portal\[8\]がある。UDPは実装されていない、（慣習であって本質的な違いではないが）マウントポイントが `/net` ではなく `/p` である、といった点が違う。

### ネットワークと分散コンピューティング

Plan 9はUNIXをベースとしているが、通信を中核機能としたシステムを構築できることを示すために開発された。全てのシステムリソースには名前があり、ファイルのようにアクセスでき、動作中の各プログラムに対応して動的に分散システムのビューを定義できる。この手法は、ユーザーやアプリケーションに提示するデータを保持するサーバ群を通常ファイルの集まりのように見せることで、アプリケーション設計の汎用性とモジュール性を改善する。

Plan 9の[ネットワーク透過性サポートの鍵となる部分は](https://ja.wikipedia.org/wiki/透過性_\(情報工学\) "wikilink")、[9P](https://ja.wikipedia.org/wiki/9P "wikilink")というプロトコルである。9Pプロトコルとその実装は、名前付きのネットワークオブジェクト同士を結びつけ、ファイルのようなシステムインタフェースとして提示する。9Pは高速なバイト指向[分散ファイルシステム](https://ja.wikipedia.org/wiki/分散ファイルシステム "wikilink")であり（ブロック指向ではない）、リモートマシン上のNFSサーバが提示するオブジェクトだけでなく、任意のオブジェクトを仮想化できる。このプロトコルはプロセスやプログラムやデータと通信するのに使われ、ユーザインタフェースとネットワークの両方を含んでいる。第4版では 9P2000 に改称された。

### Unicode

Plan 9の内部コードは[UTF-8](https://ja.wikipedia.org/wiki/UTF-8 "wikilink")となっている。このため、多言語の問題は基本的には発生しない。また、そもそもUTF-8自体、Plan 9の研究の過程で[ケン・トンプソン](https://ja.wikipedia.org/wiki/ケン・トンプソン "wikilink")が考案したもので、1992年に全コードがUTF-8対応になった\[9\]。なお、Plan 9 がサポートしているのは、Unicodeの[基本多言語面](https://ja.wikipedia.org/wiki/基本多言語面 "wikilink")だけである。

## 実装

[thumb](https://ja.wikipedia.org/wiki/ファイル:Rio_in_Plan_9_install.png "wikilink") インストール可能な実行環境が[x86](https://ja.wikipedia.org/wiki/x86 "wikilink")向けに用意されている。また、[MIPS](https://ja.wikipedia.org/wiki/MIPSアーキテクチャ "wikilink")、[DEC Alpha](https://ja.wikipedia.org/wiki/DEC_Alpha "wikilink")、[SPARC](https://ja.wikipedia.org/wiki/SPARC "wikilink")、[PowerPC](../Page/PowerPC.md "wikilink")、[ARMなどのアーキテクチャにも移植されている](https://ja.wikipedia.org/wiki/ARMアーキテクチャ "wikilink")。システムは [ISO](https://ja.wikipedia.org/wiki/国際標準化機構 "wikilink")/[ANSI](https://ja.wikipedia.org/wiki/ANSI "wikilink") [C](../Page/C言語.md "wikilink") の方言の一種で書かれている。いくつかのアプリケーションは[Alefという独自の言語で元々は書かれていたが](https://ja.wikipedia.org/wiki/:en:Alef_\(programming_language\) "wikilink")、後でシステムと同じC言語の方言で書き直されたものもある。[POSIX](https://ja.wikipedia.org/wiki/POSIX "wikilink")対応アプリケーションを移植可能であり、[ソケットは](https://ja.wikipedia.org/wiki/ソケット_\(BSD\) "wikilink") ANSI/POSIX Environment APE 経由でエミュレートできる。最近では、Plan 9上で[Linux](https://ja.wikipedia.org/wiki/Linux "wikilink")用バイナリを実行できる *linuxemu* というアプリケーションも開発中である。

[IBM](../Page/IBM.md "wikilink")の[スーパーコンピュータ](https://ja.wikipedia.org/wiki/スーパーコンピュータ "wikilink") [Blue Gene](https://ja.wikipedia.org/wiki/Blue_Gene "wikilink") にも移植されている\[10\]。

## 影響

Plan 9はUNIXの中核的概念——すなわち全てのシステムインタフェースをファイル群で表現するということ——が現代的分散システムとして実装でき、機能することを示した。Plan 9 の一部機能、例えば[UTF-8](https://ja.wikipedia.org/wiki/UTF-8 "wikilink")は他のオペレーティングシステムにも実装された。[Linux](https://ja.wikipedia.org/wiki/Linux "wikilink")などのUnix系オペレーティングシステムは[9P](https://ja.wikipedia.org/wiki/9P "wikilink")、Plan 9 のファイルシステムやシステムコール体系も部分的に実装した。また、Plan 9 のアプリケーションやツールを集めた Plan 9 from User Space はUnix系システムに移植され、ある程度の人気を得ている。Glendix は、Linuxカーネルの周囲の[GNU](../Page/GNU.md "wikilink")のシステムプログラムを Plan 9 内のプログラムで置き換えようとするプロジェクト（あるいは、逆に Plan 9 のカーネルを Linux に置き換えるプロジェクト）である。

しかし、Plan 9はUNIXほどの人気を得ることはなく、研究用ツールという位置づけに終始した。Plan 9に対しては、「オペレーティングシステム研究での興味深い論文を生成するためのデバイスとして主に機能している」という批判もある\[11\]。[エリック・レイモンド](https://ja.wikipedia.org/wiki/エリック・レイモンド "wikilink")は著書 *The Art of Unix Programming* で、Plan 9が広まらない背景について、次のように考察している。

  -
    Plan 9が失敗したのは単に、Unix がそれ以前のシステムを凌駕したほどPlan 9は注目に値する改良ではなかったからである。Plan 9に比べると Unix はガタピシ言って錆付いたところもあるが、与えられた仕事はちゃんとやっており、現在の位置に留まるだけの資格がある。野心的なシステムアーキテクトへの教訓がここにある。よりよいソリューションにとって最も危険な敵は、すでに存在する十分うまく動作するコードベースである。\[12\]

Plan 9の支持者や開発者は、採用を妨げていた問題は既に解決され、当初の目標としていた分散システム、開発環境、研究用プラットフォームには十分な完成度であり、今後徐々に広まっていくだろうと主張している。[Infernoは仮想機械上で動作するため](https://ja.wikipedia.org/wiki/Inferno_\(オペレーティングシステム\) "wikilink")、混在グリッド環境の一部として Plan 9 の技術をもたらす原動力になるとしている\[13\]\[14\]\[15\]\[16\]。

## ライセンス

[GNUプロジェクト](../Page/GNUプロジェクト.md "wikilink")はPlan 9のライセンス\[17\]を[フリーソフトウェア](../Page/フリーソフトウェア.md "wikilink")ライセンスだとは認めていなかったが、2003年6月にそのライセンスに変更が加えられ、[GPLとは整合性を持たないながらも](../Page/GNU_General_Public_License.md "wikilink")、[フリーソフトウェア](../Page/フリーソフトウェア.md "wikilink")と認められるようになった\[18\]。[OSIも](https://ja.wikipedia.org/wiki/Open_Source_Initiative "wikilink")[オープンソース](../Page/オープンソース.md "wikilink")ライセンスと認めており、[Debianフリーソフトウェアガイドライン](https://ja.wikipedia.org/wiki/Debianフリーソフトウェアガイドライン "wikilink")には合格している。[全ソースコード](http://plan9.bell-labs.com/plan9/download.html)がそのライセンスでフリーで入手可能である。

## 関連項目

  - [acme](https://ja.wikipedia.org/wiki/acme "wikilink") - プログラマ用ユーザインタフェース
  - [9P](https://ja.wikipedia.org/wiki/9P "wikilink") - ファイルシステム・プロトコル
  - [Inferno](https://ja.wikipedia.org/wiki/Inferno_\(オペレーティングシステム\) "wikilink") - Plan 9 から派生した分散OS

## 脚注・出典

## 外部リンク

### ベル研究所

  - [Plan 9 from Bell Labs](https://web.archive.org/web/20150831234945/http://plan9.bell-labs.com/plan9/)（公式サイト、[英語](https://ja.wikipedia.org/wiki/英語 "wikilink")）
      - [イメージキャラクター「Glenda」](https://9p.io/plan9/img/plan9bunnywhite.jpg)（[JPEG](https://ja.wikipedia.org/wiki/JPEG "wikilink")画像）
  - [その他の関連文書など（英語）](http://doc.cat-v.org/plan_9/)
  - [README for 2nd Edition](http://doc.cat-v.org/plan_9/2nd_edition/README) by [Brian W. Kernighan](https://ja.wikipedia.org/wiki/ブライアン・カーニハン "wikilink")
  - [Plan 9 projects in the GSoC](http://gsoc.cat-v.org)
  - [Organizations using Plan 9 and Inferno](http://plan9.bell-labs.com/wiki/plan9/organizations_using_plan_9_and_inferno/) Plan 9 や Inferno を使っている組織の不完全な一覧

### レクチャー

  - [Slides](http://cm.bell-labs.com/sources/contrib/uriel/slides/fosdem06/slides.pdf) - [Video](http://ftp.belnet.be/mirror/FOSDEM/2006/FOSDEM2006-plan9.avi) from [FOSDEM 2006](https://ja.wikipedia.org/wiki/FOSDEM "wikilink")
  - [Plan 9 is not dead](http://www.cs.unm.edu/~fastos/05meeting/PLAN9NOTDEADYET.pdf) at [FAST-OS 2005](http://www.cs.unm.edu/~fastos/)

### 他のネイティブ版と仮想版

  - ネイティブ

<!-- end list -->

  - [Plan 9](http://www.vitanuova.com/plan9/index.html) - Vita Nuova Holdings による製品版

<!-- end list -->

  - 仮想

<!-- end list -->

  - [Plan 9](http://www.oszoo.org/wiki/index.php/Category:Plan9_images) - [QEMU](https://ja.wikipedia.org/wiki/QEMU "wikilink")用イメージ
  - [Plan 9](http://www.planb-security.net.nyud.net:8080/plan9) - [VMware](https://ja.wikipedia.org/wiki/VMware "wikilink") Player 用
  - [Plan 9](http://swtch.com/9vx/) - [Vx32拡張環境用](https://ja.wikipedia.org/wiki/:en:Vx32 "wikilink")

### その他

  - [Plan9翻訳プロジェクト](https://sites.google.com/site/plan9jp/)
  - <http://plan9.aichi-u.ac.jp/>
  - [ベル研究所 Plan9の概要](http://www.ascii24.com/24/columns/10102/article/2000/12/27/621511-000.html)（[ASCII24](http://ascii24.com/)のニュース）
  - <http://p9c.cc.titech.ac.jp/plan9/>
  - [9fans](http://mail.9fans.net/listinfo/9fans), メーリングリスト
  - [Ninetimes](http://ninetimes.cat-v.org) Plan 9、Inferno、Unix といったベル研究所製OSに関するニュースサイト
  - ["Plan 9: The Way the Future Was"](http://www.faqs.org/docs/artu/plan9.html) from *The Art of Unix Programming* by [Eric S. Raymond](https://ja.wikipedia.org/wiki/エリック・レイモンド "wikilink")
  - [Reinventing UNIX: An introduction to the Plan 9 operating system](https://doi.org/10.1108/07378830310509772), by Hancock, B., Giarlo, M.J., & Triggs, J. A., published in *Library Hi Tech*, 21(4), 471-476.
  - [Introduction to OS abstractions using Plan 9 from Bell Labs](http://plan9.escet.urjc.es/who/nemo/9.intro.pdf), by Francisco J Ballesteros
  - [Plan B](http://lsub.org/ls/planb.html) - Plan 9 を基盤とした研究用OS
      - [Octopus](http://lsub.org/ls/octopus.html) - Plan B からの派生
  - [Glendix](http://www.glendix.org/) - Plan 9 のユーザー空間ツールをLinuxに移植したもの

[Category:Plan_9_from_Bell_Labs](https://ja.wikipedia.org/wiki/Category:Plan_9_from_Bell_Labs "wikilink") [Category:分散オペレーティングシステム](https://ja.wikipedia.org/wiki/Category:分散オペレーティングシステム "wikilink") [Category:フリーソフトウェアOS](https://ja.wikipedia.org/wiki/Category:フリーソフトウェアOS "wikilink") [Category:Unix系オペレーティングシステム](https://ja.wikipedia.org/wiki/Category:Unix系オペレーティングシステム "wikilink") [Category:1992年のソフトウェア](https://ja.wikipedia.org/wiki/Category:1992年のソフトウェア "wikilink")

1.
2.  [UNIX との違い](http://plan9.aichi-u.ac.jp/unix.html)
3.
4.
5.
6.
7.
8.  [Portals in 4.4BSD](http://static.usenix.org/publications/library/proceedings/neworl/full_papers/stevens.a)
9.
10. [Plan9 BG Presentation](http://go.cs.bell-labs.com/fastos/doc/lanl.bglport.pdf)
11.
12.
13.
14.
15.
16.
17. [Lucent Public License](http://plan9.bell-labs.com/plan9/license.html)
18. [Various Licenses and Comments about Them - GNU Project - Free Software Foundation (FSF)](http://www.gnu.org/licenses/license-list.html)
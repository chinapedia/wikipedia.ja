> この記事は[DBASE](https://ja.wikipedia.org/wiki/DBASE)から翻訳されています。


**dBASE**（ディーベース）は、初期の[マイクロコンピュータ](../Page/マイクロコンピュータ.md "wikilink")に向けて開発され広く使われた最初の[データベース管理システム](../Page/データベース管理システム.md "wikilink") (DBMS) である。[アシュトンテイト](../Page/アシュトンテイト.md "wikilink")によって発売され、[CP/M](https://ja.wikipedia.org/wiki/CP/M "wikilink")、[Apple II](../Page/Apple_II.md "wikilink")、[MS-DOS](../Page/MS-DOS.md "wikilink")搭載の[PC/AT互換機](https://ja.wikipedia.org/wiki/PC/AT互換機 "wikilink")などで動作した。

数年間、世界で最も売れた[ソフトウェア](../Page/ソフトウェア.md "wikilink")となったが、[Microsoft Windowsへの対応はうまくいかず](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")、[Paradox](https://ja.wikipedia.org/wiki/Paradox_\(データベース\) "wikilink")、[Clipper](../Page/Clipper_\(プログラミング言語\).md "wikilink")、[FoxProなどの新たな製品に取って代わられた](https://ja.wikipedia.org/wiki/Microsoft_Visual_FoxPro "wikilink")。dBASEは[1991年](../Page/1991年.md "wikilink")に[ボーランド](../Page/ボーランド.md "wikilink")に売却されたが、[1999年](../Page/1999年.md "wikilink")にボーランドは権利を売却し、新たにdBASE Inc.が設立されている。

1980年代中盤から、他社がdBASEを真似た製品や[プログラミング言語](../Page/プログラミング言語.md "wikilink")を開発している。FoxPro（現在はVisual FoxPro）、Quick－Silver、Clipper、Xbase++、Harbourなどである。これらは非公式ではあるが、まとめて*[xBase](https://ja.wikipedia.org/wiki/xBase "wikilink")*あるいは*XBase*と呼ばれている。

dBASEの[ファイル形式である](../Page/ファイルフォーマット.md "wikilink")**dbf**は構造のあるデータを単純なフォーマットで格納する形式であり、多くの[アプリケーションで使われている](../Page/アプリケーションソフトウェア.md "wikilink")。

dBASEは15年間のサポート保証付で販売されていた。

## 歴史

### リトリーブとJPLDIS・バルカン

dBaseの原型は[1960年代](../Page/1960年代.md "wikilink")中盤までさかのぼる。その頃、ティムシェア社 (Tymshare Corporation) からリトリーブ (RETRIEVE) というデータベースシステムがリリースされていたものの、そのユーザの一つでもある[ジェット推進研究所](../Page/ジェット推進研究所.md "wikilink") (JPL) が、1960年代終盤に[プログラマ](../Page/プログラマ.md "wikilink")のジェブ・ロング (Jeb Long) にリトリーブのカスタマイズ版の作成を依頼した。その結果開発されたのが、[UNIVAC](../Page/UNIVAC.md "wikilink") 1108[汎用機上で](../Page/メインフレーム.md "wikilink")[FORTRAN](../Page/FORTRAN.md "wikilink")言語を使って書かれた**JPLDIS** (*Jet Propulsion Laboratory Display Information System*) である。

[1978年](https://ja.wikipedia.org/wiki/1978年 "wikilink")、ロングの友人でJPLのプログラマだったC・ウェイン・ラトリフ (C. Wayne Ratliff) は、JPLDIS の機能を[CP/M](https://ja.wikipedia.org/wiki/CP/M "wikilink")上に再現するデータベースプログラムを[アセンブリ言語](../Page/アセンブリ言語.md "wikilink")で書き、[スタートレック](../Page/スタートレック.md "wikilink")の[ミスター・スポックの母星にちなんで](../Page/スポック.md "wikilink") **[バルカン (Vulcan)](../Page/バルカン_\(スタートレック\).md "wikilink")** と名づけた。後にラトリフ自身は、フットボール賭博で必勝法を見つけるためにデータベースソフトを作ったと述懐している<ref>1982年の *Popular Computing*誌の記事および''Programmers at Work: Interviews With 19 Programmers Who Shaped the Computer Industry *(ISBN: 1556152116) 収録のインタビューより。</ref>。その後もラトリフは、バルカンの改良と拡張を加えながら「これは売れるかもしれない」と考えて、[1979年](../Page/1979年.md "wikilink")10月から数ヶ月間*BYTE magazine''誌にバルカンの広告を掲載した（販売価格は7000ドル）。しかしユーザーの反応は薄く、[1980年](https://ja.wikipedia.org/wiki/1980年 "wikilink")夏頃にはラトリフ自身プログラマの仕事とバルカンの改良に疲れたために販売を取り止め、既にバルカンを購入してくれたユーザのサポートに専念することになった。

### アシュトンテイトによる買収とdBASE II

[1981年](../Page/1981年.md "wikilink")、ソフトウェア・プラス社の共同経営者だったジョージ・テイト (George Tate) とハル・ラシュリー (Hal Lashlee) が、バルカンの評判を耳にしてラティフの許へ訪問してデモを見せてもらった。ソフトウェア・プラス社はバルカンの独占販売権を取得すると同時に、バルカンの製品名を**dBASE II**（販売価格は695ドル）と変更した\[1\]。最初のバージョンであるにも関わらずわざわざ「II」を付けたのはロサンゼルスで広告コンサルタントをしていたハル・パウルク (Hal Pawluk) のアイデアで、敢えて最初のバージョンである印象を与えない（言い換えれば完成されたソフトであると言える）[ネーミング](https://ja.wikipedia.org/wiki/ネーミング "wikilink")戦略があった。

dBASE IIは、[関係データベース](https://ja.wikipedia.org/wiki/関係データベース "wikilink")と銘打ってはいたものの[エドガー・F・コッド](../Page/エドガー・F・コッド.md "wikilink")の定義する[関係モデル](../Page/関係モデル.md "wikilink")に適合していなかった。それでも、[CP/M](https://ja.wikipedia.org/wiki/CP/M "wikilink")マシン上では初めての複数ファイル製品であり、そのプログラミング環境を使えばほとんどどんなアプリケーションも構築できるなど、当時としては非常に先進的であった。この頃の[ハードウェア](../Page/ハードウェア.md "wikilink")環境はメモリ ([主記憶装置](../Page/主記憶装置.md "wikilink")) や[補助記憶装置](../Page/補助記憶装置.md "wikilink")の容量が貧弱だったが、それにも関わらずdBASEを使って多数の中小規模のタスクを自動化することができた。 とは言うものの当初は売れ行きが伸び悩み、ラティフ自身が売っていた時よりも売り上げが低かったくらいであった。しかし[IBM PCの発売とそのプラットホームがオープンになってからは売り上げが伸び](../Page/IBM_PC.md "wikilink")、dBASE IIは[WordStar](../Page/WordStar.md "wikilink")や[VisiCalc](../Page/VisiCalc.md "wikilink")と並ぶ[キラーアプリの一つにまでなる](../Page/キラーアプリケーション.md "wikilink")。

アシュトンテイトは、ラトリフを技術部門の副社長として迎え入れ**dBASE III**のプロジェクトマネージャとすると共にシステム設計やプログラミングを委ねている。ロングもほぼ同時期に雇われ、IBM PC用にdBASE IIを[Z80](../Page/Z80.md "wikilink")[アセンブリ言語](../Page/アセンブリ言語.md "wikilink")コードから[Intel 8088アセンブリ言語に書き換えた](../Page/Intel_8088.md "wikilink")\[2\]。また、ロングはdBASE内部の[プログラミング言語](../Page/プログラミング言語.md "wikilink")の基本設計に従事し、社の内外でdBASEのリーダーの一人となった。

### サードパーティーの派生

dBASE は複雑な製品であったため、それをサポートする周辺製品を開発・販売する[サードパーティー](../Page/サードパーティー.md "wikilink")が多数生まれた。サードパーティーのアドオンとして特に重要なものとして、dBASE[コンパイラ](../Page/コンパイラ.md "wikilink")がある。これは、dBASE 内部の[スクリプト言語](../Page/スクリプト言語.md "wikilink")で書かれたプログラムを単独で実行できるようにするものであった。これを使うとプログラムの配布が容易になるだけでなく、実行時にdBASE本体をインストールしなくても済んだ。主な dBASE コンパイラとしては[Clipperがあり](../Page/Clipper_\(プログラミング言語\).md "wikilink")、この種のdBASEコンパイラは後に完全なdBASEクローン製品へと発展することになる。

アシュトンテイトは、実行環境のみのdBASEを395ドルで販売していたものの、サードパーティーがコンパイラを提供する様になると売り上げが減ってしまった。テイトの後継CEOだったエド・エスバー (Ed Esber) はこうした事態を看過出来ず、（サードパーティーはdBASEを補完するという意味で重要と考えてもいたが）dBASEの新しいバージョンを開発するたびにサードパーティー製品の機能を取り込んでいった。このため、市場では dBASE の新バージョンが発表されるたびにサードパーティーの製品の売り上げが激減するという現象が起きたが、実際にそのサードパーティーの機能が新バージョンに取り込まれるかどうかに関わらずサードパーティーの売り上げに影響が出るばかりか、場合によっては[ベーパーウェア](https://ja.wikipedia.org/wiki/ベーパーウェア "wikilink")となることもしばしばでアシュトンテイト社とサードパーティー・開発者コミュニティとの間の対立を引き起こす結果となった。終にはアシュトンテイト社外のユーザーグループでdBASEファイル形式の標準化仕様を策定する動きが出る（つまりは誰でもdBASE互換システムを作ることが出来てしまう）と知るや、エスバーが「dBASEクローンを作った者は誰でも訴えてやる\! やれるもんならやってみろ\!」と激昂するに至り、開発者やユーザーまでも敵に回したばかりか法廷闘争にまで発展してしまう（後述）。

### dBASE III

[1984年](../Page/1984年.md "wikilink")6月にアシュトンテイトは、新バージョン**dBASE III**をリリースした。

既に[プログラムが大きくなったことから](../Page/プログラム_\(コンピュータ\).md "wikilink")、保守性と[移植性](../Page/移植性.md "wikilink")を高めるためdBASE IIIは[C言語](../Page/C言語.md "wikilink")で書かれたが、その副作用として古いPCでは性能が悪化することになってしまった。だが[ハードウェア](../Page/ハードウェア.md "wikilink")が高性能化したことに加えハードディスクの大容量化と低価格化が急激に進んだことから、致命的な問題には至らなかった。

さらにキャラクタベースのメニューシステムを導入した**dBASE III+** を1986年にリリースしたものの、直後に大量のデバッグに追われる破目となり、何とか対処して影響を被った顧客企業の間でかえって評判を高める結果となった。dBASE III+ は dBASE II と同様の成功を収め、1987年の売り上げは3億ドルとなった。

### dBASE Mac

この頃[Macintosh](../Page/Macintosh.md "wikilink") (Mac) が登場し、[アップル側からアシュトンテイトに製品移植を打診された](../Page/アップル_\(企業\).md "wikilink")。アシュトンテイトは、Mac登場から数ヶ月後には Mac向けデータベースを作っていた会社を買収し、Mac版のdBASEの製品開発に着手する。**dBASE Mac**は 1987年9月にリリースされGUIを備えていたものの、肝心のデータ互換はPC版とは全く互換性がく、互換性を期待して購入したユーザーは一からアプリケーションを書き直す手間に追われた。また非常に性能が悪く、頻繁にクラッシュするということで悪評が立った。このため1989年にdBASE IIIを完全移植し、DOS版との完全なデータ互換と[インタフェースを備えたバージョンをリリースしている](../Page/インタフェース_\(情報技術\).md "wikilink")。

### dBASE IV: 衰退

dBASEの問題の1つとして、これが[クライアントサーバモデル](../Page/クライアントサーバモデル.md "wikilink")に基づいていないという点が挙げられる。つまり、[コンピュータネットワーク](../Page/コンピュータネットワーク.md "wikilink")経由で複数のユーザーが[データベース](../Page/データベース.md "wikilink")にアクセスするという使い方ができないのである。データベースをネットワーク上で使うには、データベースファイル全体をPC間で転送する必要があった。クライアントサーバ型のデータベースはdBASEのようなスタンドアロンのシングルユーザ向けシステムとは根本的に異なる。従って、それをクライアントサーバ型に作り直すのは大変な作業となってしまう。しかしながらネットワークが企業で当たり前に使われるようになってきたため、アシュトンテイトの製品はその環境にはそぐわなくなってきていた。

dBASEの開発者だったラトリフはエスバーとの確執から既に退社しており、クライアントサーバモデル対応の次世代dBASEの開発ではロングが主任アーキテクトとなった。一方でエスバーは[Microsoft SQL ServerをdBASEのバックエンドとする](https://ja.wikipedia.org/wiki/Microsoft_SQL_Server "wikilink")（逆に言えば、dBASEをMicrosoft SQL Serverの[フロントエンド](../Page/フロントエンド.md "wikilink")にする）という構想をぶち上げ、[マイクロソフト](../Page/マイクロソフト.md "wikilink")の[ビル・ゲイツ](../Page/ビル・ゲイツ.md "wikilink")と共同で記者会見を開いている。これが実現すれば、既存の dBASE 利用者がその資産を生かしつつクライアントサーバ環境に移行できるということになる。アシュトンテイトは1986年のdBASE新バージョンの出荷を予定し、公表していた。この新バージョンは性能や機能が強化され、[Microsoft SQL Serverとの親和性を高めるために](https://ja.wikipedia.org/wiki/Microsoft_SQL_Server "wikilink")[SQL](../Page/SQL.md "wikilink")もサポートし、[コンパイラ](../Page/コンパイラ.md "wikilink")も内蔵する予定だった。

しかし、新バージョンのリリースはプロジェクト管理の失敗により1988年10月にまで遅延した。その結果リリースされた**dBASE IV**も性能が悪く、[バグ](../Page/バグ.md "wikilink")が多かった。dBASE IVの開発はdBASE IIIのコードが基本となっていたが、そのコードは移植に次ぐ移植でいわゆる「スパゲッティコード」になっていて、ある箇所のバグを潰しても別の箇所に影響が出るといった具合で修正は困難を極めた。もっとも修正版を素早くリリースすれば大きな問題とはならないし、実際dBASE IIIのときもアシュトンテイトは同様の状況を乗り切っていた。しかし、dBASE IVにまで至ると余りに仕様変更やバージョンアップすべき箇所・加えて[デバッグ](../Page/デバッグ.md "wikilink")の必要がある箇所が多くなり過ぎて、状況は最悪となった。

しかも、dBASE IVには予定されていたコンパイラ機能が無く、実際に使ってみると何時も間違った答を返し、頻繁にクラッシュしてはデータベースファイルを破壊した。適切なアップデートを行おうにも困難を極め、改良版のdBASE IV 1.1がリリースされたのは実に2年も経った後・エスバーが経営陣から追われた後であった。結局、その間に多くのユーザーが[FoxBaseや](https://ja.wikipedia.org/wiki/Microsoft_Visual_FoxPro "wikilink")[ClipperなどのdBASEクローンを使うようになり](../Page/Clipper_\(プログラミング言語\).md "wikilink")、dBASEのシェアも1988年にはPC用データベース市場の 63%を占めていたのが翌1989年には43%にまで急落した。また、[Microsoft SQL Serverとの連携もうまく行かず](https://ja.wikipedia.org/wiki/Microsoft_SQL_Server "wikilink")、マイクロソフトは代替のフロントエンドとして[Microsoft AccessをリリースすることになりdBASEはますます旗色が悪くなった](../Page/Microsoft_Access.md "wikilink")。

### 法廷闘争

前述した様に標準化をしようとしていたユーザーグループに対しエスバーは訴訟に訴えて妨害を図ったが\[3\]、dBASE IVのデバッグと修正に大慌わになっていた中でdBASEのシェアを食いつつあったdBASEクローンにも頭を悩ませていた。殊にその筆頭であったFoxBase・FoxProは、（ソフトウェア工学を専門としていた大学教授とその学生たちが書いたコードがベースとなっていたため）そのコードのモジュール性と拡張性に注意が払われていたことから、リリースの手早さから市場シェアを伸ばしつつあった\[4\]。

こうしたことから、1990年にエスバーはFoxProの開発元であるFox Softwareを訴え、FoxProの出荷を潰すことで他のクローンも販売できなくでき、結果としてdBASE IVの低迷している売り上げを立て直すことを目論んだ。しかし、dBASEは本来、ジェット推進研究所が使っていた[メインフレーム](../Page/メインフレーム.md "wikilink")用の言語とファイル形式に基づきラトリフがPC向けに開発したものであり、言語やファイル形式の所有権が誰にあるかが問題になった（クローン製品はコードをそのまま使っているわけではなかった）。ラトリフはアシュトンテイトを既に退社していたことからアシュトンテイトに有利な発言をするわけもなく、所有権はJPLにあると判断されてアシュトンテイトは門前払いの格好で裁判を終えざるを得なかった。その後、裁判所は先の決定を覆して言語の所有権の確認のための調停を行うとしたが、既にアシュトンテイトは立ち直れない状況となっていた。

### ボーランドによる買収以後

dBASE IVをめぐる一連の不手際ですっかり経営不振に陥ったアシュトンテイトは1991年に[ボーランド](../Page/ボーランド.md "wikilink")によって買収されたが、そのボーランドには競合製品の[Paradoxがあり](https://ja.wikipedia.org/wiki/Paradox_\(データベース\) "wikilink")\[5\]、そのプログラマたちは dBASE よりも優れていると自負していた。ボーランドを率いていた[フィリップ・カーン](../Page/フィリップ・カーン.md "wikilink")は敢えて双方のチームを残して互いに競わせ、一方でバグが修正されたdBASE IVをより[ハイエンド](https://ja.wikipedia.org/wiki/ハイエンド "wikilink")なプラットフォーム（[Solaris](../Page/Solaris.md "wikilink")、[AIX](../Page/AIX.md "wikilink")、[VMS](https://ja.wikipedia.org/wiki/VMS "wikilink")など）に移植させた。結局、**Borland dBase Compiler for Windows**という[オブジェクト指向](../Page/オブジェクト指向.md "wikilink")版dBASEともいうべき製品も別に開発され、最終的にアシュトンテイトのチームは負けを認めざるを得なかった。またdBase IVも1993年頃まで販売され続けた。

カーンは、dBASEにしろParadoxにしろ真に[Windowsベースとなるよう改良しなければならないと考え](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")、1993年に新製品開発チームを立ち上げた。これはWindowsに対応しているとともにdBASE IVと互換があって[オブジェクト指向](../Page/オブジェクト指向.md "wikilink")インタフェースを備えたものを目標としたが、従来のコードベースではWindowsへの対応が不可能と見て、WordTech社から dBASEクローンの一つDBXL（DBXLは仮想マシン方式で書かれており、多くのプラットフォームへの移植が容易だった）を開発チームごと買取り完成にこぎつけた。

1994年にボーランドは、**dBASE 5**をdBASE for DOSとdBASE for Windowsとしてリリースしたが、既にMicrosoft Accessが市場を席巻しているばかりか相前後してマイクロソフトはFox Softwareを買収して[FoxProをリリース](https://ja.wikipedia.org/wiki/Microsoft_Visual_FoxPro "wikilink")、dBASEクローンの市場はFoxProに収斂する流れが既に出来上がってしまっていた。それでもボーランドは、dBASE 5を**Visual dBASE 5**\[6\]、**Visual dBASE 7**\[7\]とバージョンアップを続けたが、開発者のdBASE離れという流れを止めることはできなかった。ボーランドはこのころすでにDelphiで成功をおさめていた上、[Paradoxに力を入れていたこともあり](https://ja.wikipedia.org/wiki/Paradox_\(データベース\) "wikilink")、dBASEの権利を**dBASE Inc.**に売却した。

dBASE Inc.は製品サポートのための会社だったが、新たなバージョンもリリースしている。Windows向けのオブジェクト指向データベース*dBASE Plus*などだが、現在[SQL](../Page/SQL.md "wikilink")ベースの製品が主流の市場にあってはdBASEはほとんど力がないと言える。

## dBASEプログラミング言語

VulcanをIMSAI 8080やCP/MさらにはMS-DOSに移植した後、ラトリフは画面表示を扱うコマンド群や[制御構造](../Page/制御構造.md "wikilink")（DO WHILE/ENDDO や IF/ENDIF）を追加した。データを扱うため、dBaseにはファイルを操作する様々な機能があり、文字列/数/日付などを操作する各種機能がある。関連するデータを持つ複数のファイルを同時にオープンして操作できることから、アシュトンテイトはdBaseを「[関係データベース](https://ja.wikipedia.org/wiki/関係データベース "wikilink")」と称したが、もちろん[エドガー・F・コッド](../Page/エドガー・F・コッド.md "wikilink")の[関係モデル](../Page/関係モデル.md "wikilink")に準拠しているわけではない。あえて分類するとすれば、関係データベースと[ナビゲーショナルデータベース](../Page/ナビゲーショナルデータベース.md "wikilink")の中間である。

dBaseは[インタプリタ](../Page/インタプリタ.md "wikilink")を備えており、ユーザーはプロンプトにコマンドを打ち込むことでそれを実行させることができる。スクリプト（拡張子はPRG）もDOコマンドを使ってインタプリタで実行され、その中の各コマンドや変数も実行時に評価される。このためdBaseプログラムは簡単に書くことができ、コンパイルなどの手間もかからない。これは、CPUの性能が低い時代には重要な特徴だった。インタプリタはメモリ管理も自動的かつ動的に行うため（メモリ確保などが不要）、プログラミングに不慣れな人でも簡単に使うことができた。

逆に、ユーザーがdBaseの言語に習熟してプロが現れるようになると、その単純さが足かせとなってきた。より複雑で大規模なアプリケーションが開発されるようになって、信頼性と性能のために高度なプログラミング機能が要求されるようになった。

アシュトンテイトと競合するクローンメーカーは、[ユーザー定義関数](https://ja.wikipedia.org/wiki/ユーザー定義関数 "wikilink")、変数スコープ、複雑なデータを扱う配列、パッケージ機能、オブジェクト指向的構文、遠隔のデータベースにアクセスするインタフェースなどのプログラミング機能を導入するようになってきた。アシュトンテイトも同様の機能を導入していった。さらに[SQL](../Page/SQL.md "wikilink")も導入されるようになった。

1980年代後半、dBase言語の標準化が検討された（[IEEE](../Page/IEEE.md "wikilink")1192）。その際にアシュトンテイトの製品と区別するために "[XBase](https://ja.wikipedia.org/wiki/XBase "wikilink")" と呼ばれるようになった。dBaseやXBaseプログラミングについての書籍も数多く出版された。Joseph Carrabis は1980年代後半に dBase に関するマニュアル本をいくつか執筆し\[8\]、著書の販売数で世界でも十指に入ることになった。

今日、dBase言語の[実装](../Page/実装.md "wikilink")は拡張され、様々な機能が追加されている。GUI操作、[分散処理](https://ja.wikipedia.org/wiki/分散処理 "wikilink")、[インターネット](../Page/インターネット.md "wikilink")、最新の周辺機器とのインタフェースなどである。従来互換のためにdBase言語をサポートするアプリケーションはあるが、dBase/XBaseは既に主要な標準とは言えないものとなった。

### プログラミング例

以下の例では、従業員表 ("empl") を開き、"filter" をセットしてマネージャー（部下を持つ人）を選択して表示し、給料を10%上げて、結果を[プリンター](https://ja.wikipedia.org/wiki/プリンター "wikilink")に印刷する。

` USE empl            `
` SET FILTER TO supervises > 0`
` GO TOP`
` IF .NOT.EOF()`
`   BROWSE`
`   REPLACE ALL salary WITH salary * 1.1`
`   GO TOP`
`   LIST fname, lname, salary TO PRINT`
` ELSE`
`   WAIT "該当がありません"`
` ENDIF`
` SET FILTER TO`
` USE`

dBASEは初めて（[Perl](../Page/Perl.md "wikilink")のずっと以前に）ビジネス向けに文字列評価を実装した。

` i = 2`
` myMacro = "i + 10"`
` i = &myMacro.`
` * i now has the value 12 `

"&" は "MyMacro" に格納されている文字列の内容をプログラムコードであるかのように評価する。

## ニッチ

この言語はビジネス用言語としては使われなくなってしまったが、ちょっとしたデータ変換には非常に使いやすい言語である。SQLと違って、データを変換して目に見えるファイル形式にするのも簡単に行える。これは、標準的なRDBMSと配列言語（[APL](../Page/APL.md "wikilink")やその進化形である[J言語や](../Page/J_\(プログラミング言語\).md "wikilink")[K言語](https://ja.wikipedia.org/wiki/K言語 "wikilink")）の中間のようなものとも言われている。

## ファイルフォーマット

dBASEの大きな遺産は`.dbf`ファイル形式であり、多くのアプリケーションで活用されている。たとえば、[地理情報システム](../Page/地理情報システム.md "wikilink")で使われているshapefile形式（[ESRI](../Page/ESRI.md "wikilink")が開発）は.dbfファイル形式で属性データを格納している。この形式をサポートするアプリケーションはXBaseと呼ばれている。

dBASEのデータベースシステムはヘッダー部（ファイル内のデータ構造を記述）を備えた最初のシステムとも言われている。これはつまり、プログラム自身がデータ構造を事前に知らなくてもファイルを扱えるということを意味する。

もう1つのファイル形式`.dbt`はメモフィールド用である。キャラクタフィールドはそれぞれ254文字までに制限されているが、メモフィールドは10バイトのポインタで`.dbt`ファイルを指し、そこにさらに大きなテキストを置くことができる。dBaseでのメモフィールドの処理は限定的だったが、ClipperなどのxBase言語では、メモフィールドをキャラクタフィールドとほぼ同じように操作できる。

dBaseは`.ndx`ファイルをインデックスに使用する。一部のxBase言語では`.ndx`についても互換を保っているが、異なる形式を使う言語としてClipper（`.ntx`形式）やFoxPro（`.cdx`形式）がある。

## 脚注

<references/>

## 外部リンク

  - [Alaska Software The Xbase of today](http://www.alaska-software.com)
  - [dBase Inc.](http://www.dbase.com/)
  - [An interview with C. Wayne Ratliff describing his career and history of Vulcan/dBase](http://www.foxprohistory.org/interview_wayne_ratliff.htm)
  - [Xbase (and dBase) File Format Description](http://www.clicketyclick.dk/databases/xbase/format/index.html)
  - [C2 Wiki Description of "XBase"](http://www.c2.com/cgi/wiki?ExBase)

[Category:データベース管理システム](https://ja.wikipedia.org/wiki/Category:データベース管理システム "wikilink") [Category:デスクトップデータベースアプリケーション開発ツール](https://ja.wikipedia.org/wiki/Category:デスクトップデータベースアプリケーション開発ツール "wikilink") [Category:DOSのソフトウェア](https://ja.wikipedia.org/wiki/Category:DOSのソフトウェア "wikilink") [Category:Windowsのソフトウェア](https://ja.wikipedia.org/wiki/Category:Windowsのソフトウェア "wikilink") [Category:1979年のソフトウェア](https://ja.wikipedia.org/wiki/Category:1979年のソフトウェア "wikilink")

1.  同時に（ラトリフの示した条件によって）社名もアシュトンテイトに改称したが、これはラシュリーが自らの名前を出すのを嫌がった（アシュトンというのはテイトが飼っていたインコの名前と言う説もある）ことと、（パウルクのアイデアで）イギリス風の名前を付けることで格調ある会社の様に見せようとしたと言われている。
2.  この移植作業では自動変換プログラムで半ば機械的に行われたため、アシュトンテイトがその後長年に渡って[ソースコード](../Page/ソースコード.md "wikilink")の保守問題に悩まされることになる。
3.  これに対しユーザーグループ側は、それまでの動きを巧く引き継いで新たな標準 "[xBase](https://ja.wikipedia.org/wiki/xBase "wikilink")" の策定へと動いている。
4.  これらのコードベースは後の[Visual FoxProまで受け継がれている](https://ja.wikipedia.org/wiki/Microsoft_Visual_FoxPro "wikilink")。
5.  このため裁判所はボーランドに対して、合併を認める条件としてdBASE言語の所有権の放棄を求めている。
6.  初期5.0ではdBASE for DOSとdBASE for Windowsという製品名であったが、5.5以降のWindows版はVisual dBASEという名称に変更された。併売されるDOS版にはVisualの冠は付いていない。
7.  リソース不足に悩まされることの多いdBASE 5をリライトする形でWindows専用としてリリースされた。
8.
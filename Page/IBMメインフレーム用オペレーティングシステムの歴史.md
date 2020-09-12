> この記事は[IBMメインフレーム用オペレーティングシステムの歴史](https://ja.wikipedia.org/wiki/IBMメインフレーム用オペレーティングシステムの歴史)から翻訳されています。


**IBMメインフレーム用オペレーティングシステムの歴史**は、世界最大の[メインフレーム機メーカーとして長期に渡り君臨した](https://ja.wikipedia.org/wiki/オペレーティングシステムの歴史 "wikilink")[IBM](../Page/IBM.md "wikilink")の歴史であり、[オペレーティングシステムの歴史](https://ja.wikipedia.org/wiki/オペレーティングシステムの歴史 "wikilink")の中でも特に注目に値する。

IBMが初期に[メインフレーム用としてユーザーに提供していた](../Page/IBMメインフレーム.md "wikilink")[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink")(OS)は、CP-67以降から実装された[仮想マシン以外はそれほど革新的といえるものではなかった](../Page/仮想機械.md "wikilink")。しかし実績のある確かなテクノロジーを優先する同社の姿勢は評判を呼び、コンピュータの購入希望者はIBMのシステムであれば間違いないと納得しやすかった。IBMのメインフレーム用OSである[z/OS](https://ja.wikipedia.org/wiki/z/OS "wikilink")、[z/VM](https://ja.wikipedia.org/wiki/z/VM "wikilink")、 [z/VSE](https://ja.wikipedia.org/wiki/z/VSE "wikilink")、[z/TPFは](../Page/Transaction_Processing_Facility.md "wikilink")、1960年代に開発されたOSの後継[バージョンで](https://ja.wikipedia.org/wiki/後方互換 "wikilink")、大幅に改良されている。

当記事ではIBM提供のOS以外にも、IBM以外が提供したIBMメインフレームで著名なOSについても記載する。

## System/360以前

当初IBMはOSを開発していなかった。[ゼネラルモーターズ](../Page/ゼネラルモーターズ.md "wikilink")は自社が所有するIBM機のために、1955年にGeneral Motors OSを開発し、1956年に[GM-NAA I/Oを開発](https://ja.wikipedia.org/wiki/GM-NAA_I/O "wikilink")、また1962年には同業他社の[バロウズコーポレーションがMCPを](../Page/バロース.md "wikilink")、[ゼネラルエレクトリックが](../Page/ゼネラル・エレクトリック.md "wikilink")[GECOSをユーザー向けに開発した](../Page/GCOS.md "wikilink")\[1\]\[2\]。

IBM機用の最初のOSは、1950年代半ばの相場で200万ドルもする非常に高価なマシンを前にして、計算もさせずにジョブを手入力する時間がもったいないと思い、ジョブのキューを管理する仕組みが欲しいと考えたユーザーが開発したものだった\[3\]。

下記のOSは一部のモデルでのみ動作し、科学技術計算や工学計算にのみ適していた。IBMの別のモデルを持つユーザーや、別のアプリケーションでは、OSなしでなんとかしなければならなかった。しかしIBMの小型機の1つである[IBM 650には](../Page/IBM_650.md "wikilink")、後に[OS/360](https://ja.wikipedia.org/wiki/OS/360 "wikilink")の一部となるある機能があった。もし処理がハード障害を意味する「ランダム処理エラー」で中断された場合、オペレーターが自動でジョブを最初からやり直すのではなく、直近のチェックポイントから自動的に復旧することができた\[4\]。

### ゼネラルモーターズのGM-NAA I/OがIBSYSになるまで

[ゼネラルモーターズ](../Page/ゼネラルモーターズ.md "wikilink")の研究開発部門は、1955年に開発したGM Operating Systemをプロトタイプに、1956年に社内で使っていた[IBM 701用に](https://ja.wikipedia.org/wiki/IBM_701 "wikilink")[GM-NAA I/Oを開発し](https://ja.wikipedia.org/wiki/GM-NAA_I/O "wikilink")、その後701の後継機に対応するようアップデートした。1960年にIBMユーザー互助会SHAREがこれを引き継ぎ、アップデート版の[SHARE OSを開発した](https://ja.wikipedia.org/wiki/SHARE_OS "wikilink")\[5\]。

最終的にIBMがこのプロジェクトを引き継ぎ、拡張したバージョンを[IBSYS](https://ja.wikipedia.org/wiki/IBSYS "wikilink")と名付け、[IBM 7090用や](../Page/IBM_7090.md "wikilink")[IBM 7094用として提供した](../Page/IBM_7090.md "wikilink")。IBSYSは8台の[テープドライブ](../Page/テープドライブ.md "wikilink")が必要だった(システムが1台以上のディスクドライブを持つ場合はこの数を減らすことができた)。[カード方式のジョブ制御言語](../Page/パンチカード.md "wikilink")、[FORTRAN](../Page/FORTRAN.md "wikilink")と[COBOL](../Page/COBOL.md "wikilink")の[コンパイラ](../Page/コンパイラ.md "wikilink")、 [アセンブラ](../Page/アセンブリ言語.md "wikilink")、[ソート](../Page/ソート.md "wikilink")プログラムなどの様々なユーティリティなどが付属した\[6\]\[7\]。

1958年にミシガン大学はコンピュータシステムにGM-NAA I/Oを採用し、学生が書いた小さなジョブを大量に処理するのに適したUMESを開発した。UMESは1967年にMTSタイムシェアリングシステムへ置き換わるまで使われた\[8\]。

### BESYS

ベル研究所はBESYS (別名BELLMON)を開発して1960年代中頃まで使用した。 ベル研究所はこれを無料・無保証で他社にも公開した\[9\]\[10\]。

### FORTRANモニターシステム

IBSYSが登場する前にIBMは[IBM 709](../Page/IBM_709.md "wikilink")、[7090](../Page/IBM_7090.md "wikilink")、[7094の各機種用に](../Page/IBM_7090.md "wikilink")、[FORTRAN](../Page/FORTRAN.md "wikilink")のプログラムを[コンパイルするための単機能OSとしてテープベースのOSであるFMSを開発した](../Page/コンパイラ.md "wikilink")。FMSとFORTRANコンパイラは同じテープの中に格納されていた\[11\]\[12\]。

## 初期のタイムシェアリングシステムと仮想マシンシステム

[MITの](../Page/マサチューセッツ工科大学.md "wikilink")[フェルナンドコルバトは](../Page/フェルナンド・J・コルバト.md "wikilink")、メインフレームの[IBM 704と](../Page/IBM_704.md "wikilink")[IBM 7090を使い](../Page/IBM_7090.md "wikilink")、[CTSS](../Page/CTSS.md "wikilink")などの初期の実験的な[タイムシェアリングシステム](../Page/タイムシェアリングシステム.md "wikilink")を1957年から1960年代初頭に開発した。これらのシステムは[ジョン・マッカーシー](../Page/ジョン・マッカーシー.md "wikilink")から提案されたアイデアに基づいていた\[13\]。IBMは自社の複数の研究所で1960年代にタイムシェアリングシステムの実験をしており、市販のメインフレームをベースにハードウェアと[マイクロコードを修正して](../Page/マイクロプログラム方式.md "wikilink")[仮想メモリをサポートし](../Page/仮想記憶.md "wikilink")、1960年代初頭にIBM M44/44X、1964年から1967年にCP-40、1967年から1972年にCP-67を開発した。CP-67に至っては1968年から1972年までの間に無保証で複数の大手顧客にリリースしていた。CP-40とCP-67には[System/360](https://ja.wikipedia.org/wiki/System/360 "wikilink") [CPU](../Page/CPU.md "wikilink")シリーズに改造が必要だったが、M44/44Xは内部構造が大きく異なる最初期のCPUである[IBM 7044で動作した](https://ja.wikipedia.org/wiki/IBM_7040 "wikilink")\[14\]\[15\]\[16\]。

これらのプロトタイプはIBMが1964年に発売した[System/360](https://ja.wikipedia.org/wiki/System/360 "wikilink")シリーズには間に合わなかったものの、IBMはこれを足掛かりにして1972年に発売した[System/370](https://ja.wikipedia.org/wiki/System/370 "wikilink")で仮想メモリと仮想マシンに対応した\[17\]。

  - M44/44Xの仮想マシンは限定的な物であり、[スラッシング](../Page/スラッシング.md "wikilink")により仮想メモリシステムの速度が大幅に低下する可能性があった。スラッシングとは、物理メモリとディスクの間で仮想メモリページをシャッフルするのに多くの時間が割かれてしまい、システムが非常に遅くなる状態のことである。
  - IBMはCP-40とCP-67の開発を通じてどのようにスラッシング問題に対処すればよいのかを学習した。新たな仮想メモリと仮想マシンのテクノロジーは非常に高速かつ信頼性があり、メインとなる市場での負荷の高い商用システムでの使用に耐えるものだった。自動化された仮想メモリは優秀なプログラマが開発した[オーバーレイ方式のプログラムと同様のパフォーマンスをコンスタントに叩きだせるとしてデビッド](../Page/オーバーレイ_\(コンピュータ用語\).md "wikilink")・セイヤーは会社に採用を迫った\[18\]。

コンピュータソフトウェアシステムという名前のコンサルティング会社は1968年にリリース版のCP-67を用いて商用タイムシェアリングサービスを提供した。同社の技術チームはMITの卒業生であるディック・オレンシュタインとハロルド・ファインリーブの2人を新卒で採用していた(前述のCTSSを参照)。会社の規模拡大に伴い社名をナショナルCSSに改め、サポートを求める有料ユーザーが増えるようにシステムに大幅な改良を加えてOSの名前をVP/CSSに変えた。1980年代初頭にIBMがVM/370(詳細は後述)を投入して市場を奪われるまで、VS/CSSはナショナルCSSの主力商品だった\[19\]\[20\]。

これらの他にも1960年代後半には複数の大学が3つのS/360用タイムシェアリングOSを開発していた。

  - **ミシガンターミナルシステム** (MTS)は[ミシガン大学](../Page/ミシガン大学.md "wikilink")主導のコンソーシアムが1967年に開発したOS。S/360-67以降の仮想メモリ機能を持つ全てのIBMメインフレーム機に対応していた。MTSは1999年まで運用された\[21\]。
  - [モントリオール](../Page/モントリオール.md "wikilink")の[マギル大学](../Page/マギル大学.md "wikilink")は1969年に**MUSIC** (McGill University System for Interactive Computing)の開発を開始した。MUSICはアップグレードを繰り返し、最終版までにテキスト検索、ウェブサーバ、メールサーバ、ソフトウェア開発ツールなどに対応した。IBMはMUSICを同社のメインフレーム機で動作する主に教育機関向けの安価な選択肢として位置付け、1985年にIBMの公式な製品ラインナップ(MUSIC/SP、Multi-User System for Interactive Computing / System Product)として加えた。公式な最終バージョンは1999年にリリースされた\[22\]。
  - **ORVYLとWYLBUR**は[スタンフォード大学](../Page/スタンフォード大学.md "wikilink")が1967-68年にIBM S/360-67向けに開発したOS\[23\]\[24\]。これらによりIBM S/360で初めてタイムシェアリング機能が使えるようになった。

## System/360 オペレーティングシステム

1960年代初頭までIBMのローエンドシステムとハイエンドシステムには互換性がなく、プログラムを別のシステムに移植するのは難しく、各システムはディスクドライブなどの[周辺機器](../Page/周辺機器.md "wikilink")も異なっていることが多かった\[25\]。このためIBMではハードとソフトの設計、開発、製造のコストが高騰し、顧客からのアップグレードの要望に応えきれなくなり、そのために売り上げが頭打ちになった。同社が1964年に発売した[System/360](https://ja.wikipedia.org/wiki/System/360 "wikilink")は全てのマシンで共通の周辺機器を使用でき、プログラムもほぼ共有できることが売りとなった\[26\]。

元々IBMは[バッチ処理](../Page/バッチ処理.md "wikilink")に特化したOSであるOS/360だけをSystem/360に提供するつもりだった。後によりシンプルなバッチ処理専用OSである[DOS/360](https://ja.wikipedia.org/wiki/DOS/360 "wikilink")を開発しており、これを開発した理由には主に以下の2つがあった。

  - System/360のモデルのうち、メモリが少ない小型モデルにはOS/360は大きすぎた\[27\]。
  - OS/360の開発が予想以上に遅れており、System/360のハードウェアの売り上げが落ちて市場が崩壊することを防ぐため、隙間を埋めるラインナップの1つとしてDOS/360を提供した。別のラインナップとしてはBOS/360(小型機用のBasic Operating System)とTOS/360(テープドライブだけしか装備していない機種用のTape Operating System)があった\[28\]。

System/360のOSはこれまでにIBMが開発したOSの中でも特に複雑で、それには以下のような理由があった\[29\]。

  - [マルチタスク](../Page/マルチタスク.md "wikilink")のサポート。ディスクの読み込みなどの[I/O処理が完了するのを現在のアプリケーションがブロック処理で待っている間に別の動作中のアプリケーションへ切り替える](../Page/入出力.md "wikilink")。マルチタスクに対応しなければこのクラスの[CPU](../Page/CPU.md "wikilink")が持つ高い処理能力のほとんどを遅いI/O操作に対する待ち時間で浪費してしまう。従ってシステムを司る心臓部としてOSを位置づけ、アプリケーションに対する正当な要求に全て応じつつ、もしアプリケーションがクラッシュしたり永久ループなどの誤動作が生じた場合は、同時に動作している別のアプリケーションに影響を与えないよう対処することが求められた。
  - 様々なクラスのマシンをサポート。メモリ搭載量が16KBの下位モデルから1MBの上位モデルに対応し、秒間1000命令から50万命令までの命令処理速度に対応した。
  - 様々なアプリケーションの要求に応える。例えばあるアプリケーションではファイルを先頭から最後まで読むだけでよいが、別のアプリケーションでは巨大なファイルの特定のレコードに高速にランダムアクセスする必要があり、また別のアプリケーションでは処理時間のほとんどを計算に費やしておりディスクをほとんど読み書きしなかった。

こうした厳しい要求によりOS/360や他のSystem/360用ソフトウェアの開発は当時としては前人未到の大規模プロジェクトとなり、間もなくIBMは問題に直面し、膨大な時間と費用をかけて大量の[バグ](../Page/バグ.md "wikilink")に対処しなければならなくなった\[30\]。PCがなくクロスコンパイラやエミュレーターもない当時の開発環境では、System/360のOSを実機上で開発してテストしなければならず、問題は大きくなる一方で、IBMはBasic Programming Support / 360 (BPS/360)を先に開発しなければならなくなった\[31\]。BPSはDOS/360やOS/360を開発するのに必要なツールを開発するのに使われ、[FORTRAN](../Page/FORTRAN.md "wikilink")と[COBOL](../Page/COBOL.md "wikilink")の[コンパイラ](../Page/コンパイラ.md "wikilink")や[ソート](../Page/ソート.md "wikilink")などの[ユーティリティ及びこれら全てをビルドするのに必要だった](../Page/ユーティリティソフトウェア.md "wikilink")[アセンブラなどのツールがあり](../Page/アセンブリ言語.md "wikilink")、これらのツールはDOS/360やOS/360にも含まれた\[32\]。

IBMの競合他社はOS/360とSystem/360の開発が遅れたことを利用し、IBM市場の最大の弱点をシステムと捉え、各社ともOSを発表した。IBMはSystem/360のセールスが失敗するのを防ぐため4つの間に合わせのOSを繋ぎでリリースした\[33\]。

  - Basic Operating System / 360 (BOS/360)\[34\] - ディスクドライブまたはテープドライブから起動し、テープドライブと数種類のディスクドライブをサポートする。このシステムはベータテストのユーザーに提供されたもので、DOS/360の初期バージョンと考えることもできる。
  - TOS/360 - テープドライブを装備し、ディスクドライブを装備していない[IBM 1401シリーズのコンピュータを持つユーザーへのアップグレードパスとして提供するべく開発された](../Page/IBM_1401.md "wikilink")。
  - [DOS/360](https://ja.wikipedia.org/wiki/DOS/360 "wikilink") - BOS/360やTOS/360に向けたアプリケーションを開発していたIBMのスモールビジネスコンピュータ部門の開発者がビルドしたもので、その後広く普及して主力のOSとなった[z/VSE](https://ja.wikipedia.org/wiki/z/VSE "wikilink")の祖先。
  - [Operating System/360](https://ja.wikipedia.org/wiki/OS/360 "wikilink") (OS/360)で、マルチタスクをサポートしない[Primary Control Program](https://ja.wikipedia.org/wiki/OS/360 "wikilink") (PCP)の構成で固定されたもの\[35\]。

IBMはS/360-67の発表と同時に、360/67の新しい仮想メモリ機能を活用した[タイムシェアリングOSのTSS](../Page/タイムシェアリングシステム.md "wikilink")/360も発表した。TSS/360のリリースは遅れ、初期バージョンは遅くて不安定だった。当時既にIBMのケンブリッジ科学センターがCP-67を別途開発しており、タイムシェアリング機能としてIBMが一部の大口顧客向けに無保証ながら提供しているほどに上手く動作していた\[36\]。CP-67はVM/370にアップグレードし、最終的には[z/VM](https://ja.wikipedia.org/wiki/z/VM "wikilink")となった。IBMはTSS/360を導入したユーザーにアップグレードパスのTSS/370 PRPQを3度リリースした後にこれを放棄した。

System/360 OSを開発する際に得られた教訓から[ソフトウェア工学](../Page/ソフトウェア工学.md "wikilink")を学問的に整備しようとする機運が高まり、ソフトウェア開発や[プロジェクトマネジメント](../Page/プロジェクトマネジメント.md "wikilink")を科学的に取り扱うようになった。System/360のプロジェクト全体を監督し、後にOS/360の特定パートの責任者となったシニアプロジェクトマネージャーの[フレデリック・ブルックス](../Page/フレデリック・ブルックス.md "wikilink")は、プロジェクト中に遭遇した問題や学んだ教訓をもとにベストセラーとなった*[人月の神話](../Page/人月の神話.md "wikilink")を執筆した*\[37\]*。その教訓とは主に次の2つである。*

  - 問題が発生しているプロジェクトに追加のリソース(主にスタッフ)を追加投入すると、コミュニケーションが困難になり、急に生産性が落ちて逆効果になることがある。これは書籍のタイトルでもある「人月の神話」症候群である。
  - 成功したシステムの後継版は、元のシステムを使った人からの要望を全て取り込もうとして肥大化し、問題が生じやすい。ブルックスはこれを「セカンドシステム効果」と呼び、OS/360を悪い例として全体的に引用している。

### DOS/360

System/360シリーズの中でもハイエンド向けのOSとしてOS/360が推奨された一方で、[DOS/360](https://ja.wikipedia.org/wiki/DOS/360 "wikilink")はローエンド向けの非力なマシンに適した平凡なOSだった。これには一連の[ユーティリティプログラム](../Page/ユーティリティソフトウェア.md "wikilink")、マクロ[アセンブラ](../Page/アセンブリ言語.md "wikilink")、[FORTRAN](../Page/FORTRAN.md "wikilink")や[COBOL](../Page/COBOL.md "wikilink")の[コンパイラ](../Page/コンパイラ.md "wikilink")などが含まれていた。[RPG](../Page/RPG_\(プログラム言語\).md "wikilink")\[38\]\[39\]がサポートされたのは後年で、最終的には[PL/I](https://ja.wikipedia.org/wiki/PL/I "wikilink")のサブセットが追加された。また様々なファイルの構造をサポートし、そのアクセスを制御するインターフェイスが提供された。

  - レコード全体を一度に読み込むのに最適なシーケンシャルデータセット。
  - 各レコードの特定のセクションをキーに検索できるインデックス付きファイルの[ISAM](../Page/Indexed_Sequential_Access_Method.md "wikilink")。
  - アクセスしたいデータのディスク上の物理位置をアプリケーションが自分で指定しなければならないダイレクトアクセスファイルのBDAM。 BDAMのプログラミングは難しく、ユーザーの多くはその使用を望まないが、ディスク上のデータへのアクセスが最も早く、多くのソフトウェア企業は主に[ADABAS](../Page/ADABAS.md "wikilink")、IDMS、IBM製の[DL/I](https://ja.wikipedia.org/wiki/DL/I "wikilink")などの[データベース](../Page/データベース.md "wikilink")マネージメントシステムを用いた。

シーケンシャルファイルとISAMファイルは固定長又は可変長のレコードを格納でき、いずれの組み合わせにおいても複数のディスクボリュームにまたがってデータを格納できる。

DOS/360はまたデータ通信機能としてBTAMも提供しており、今日の基準で見れば大変に使い辛いものだった。しかしBTAMはあらゆる種類の端末と通信でき、通信プロトコルが全く標準化されていなかった当時としては非常に画期的だった。

しかしDOS/360は、System/360機のより大型なモデルで使われた[OS/360](https://ja.wikipedia.org/wiki/OS/360 "wikilink")と比べて制約が大きかった。

  - 最初のバージョンは同時に1つのプログラムしか実行できなかった。後のバージョンでは最大で3つのプログラムを同時に実行できたが、各プログラムのメモリ空間のサイズはDOS/360をインストールする際に各ユーザーがあらかじめ区切った3本のパーティションのサイズに固定された。
  - ジョブの制御に使用するスクリプト言語の[JCLはローエンド機での処理が軽くなるように設計されており](../Page/Job_Control_Language.md "wikilink")、プログラマが読み書きするのは難しかった。
  - [パンチカード](../Page/パンチカード.md "wikilink")やプリンタの処理を効率化するための[スプーラサブシステムがなかった](../Page/スプーリング.md "wikilink")。1960年代後半に独立系ソフトウェア会社がGRASPと呼ばれるスプーラを販売した。
  - DOS/360には[リロケータブルバイナリ](../Page/リロケータブルバイナリ.md "wikilink")ローダがなく、ユーザーは使用するパーティションごとに各プログラムのアドレスを絶対アドレスで指定する[リンク情報を手動で編集しなけばならなかった](../Page/リンケージエディタ.md "wikilink")。
  - 実行プログラムを格納するコアイメージライブラリは、プログラムを削除したり更新したりした場合に、古いプログラムが格納されていたスペースが解放されなかった。コアイメージライブラリがいっぱいになるとユーティリティプログラムで圧縮しなければならず、これにより開発作業が半日潰れることがあった。
  - [アプリケーションプログラミングのインターフェースがOS](../Page/アプリケーションプログラミングインタフェース.md "wikilink")/360と異なっていた。[COBOL](../Page/COBOL.md "wikilink")などの[高水準言語](../Page/高水準言語.md "wikilink")で記述されたDOS/360用のプログラムは、OS/360で使用するには若干の修正が必要で、[アセンブラで記述かれたプログラムは大幅な変更を強いられた](../Page/アセンブリ言語.md "wikilink")。

DOS/360のユーザーはすぐにOS/360へアップグレードするだろうとIBMは考えていたが、制約があったにもかかわらず、DOS/360は世界で最も広く使われるOSになった。それには次のような理由があった。

  - System/360機は非常によく売れた。
  - 販売された360システムの90％以上がローエンドのModel 20、30、40だった。
  - これらの安価なモデルが装備していた[コアメモリはほとんどの場合においてOS](../Page/磁気コアメモリ.md "wikilink")/360の実行に必要な容量には到底足りなかった\[40\]。

DOS/360は中規模の企業が購入できるSystem/360機で不都合なく動作しており、またこのクラスのユーザーたちが過去に持っていたマシンが備えていたどのOSよりもまだマシだった。この結果、その子孫である[z/VSE](https://ja.wikipedia.org/wiki/z/VSE "wikilink")は2005年になっても依然として広く使われている\[41\]。

### OS/360

[OS/360](https://ja.wikipedia.org/wiki/OS/360 "wikilink")は様々なレベルの機能をサポートしており、共通のAPIで、より多くのコードが共通化された。PCPは同時に1つのプログラムだけしか実行できない廉価版で、[MFT](https://ja.wikipedia.org/wiki/OS/360 "wikilink") (一定個数のタスクを実行できる[マルチプログラミング版](../Page/マルチタスク.md "wikilink"))と[MVT](https://ja.wikipedia.org/wiki/OS/360 "wikilink")(タスクを無制限に実行できる[マルチプログラミング版](../Page/マルチタスク.md "wikilink"))は、後継機が発売されてから5年が経過した1970年代後半頃まで使用された\[42\]。PCP、MFT、MVTの3つに分割した理由は明らかではなく、MVTが中間クラスのモデルで使用するにはメモリを喰い過ぎたのか、あるいはIBMがマルチプログラミング版をMFTとして至急リリースしなければならなかったかなどの理由が考えられる。

PCP、MFT、MVTの3つはメモリの管理方法が異なっているが、機能的には非常に似ている(下記参照)。

  - 共通化された[アプリケーションプログラミングインターフェイス](../Page/アプリケーションプログラミングインタフェース.md "wikilink")(API)。アプリケーションプログラムのバイナリは[再コンパイルすることなくPCP](../Page/コンパイラ.md "wikilink")、MFT、MVTで実行できる。
  - DOS/360よりも柔軟で使いやすい同じ[JCL](../Page/Job_Control_Language.md "wikilink")。
  - DOS/360と同じファイルの読み書き方式(シーケンシャル、インデックス、ダイレクト)に対応。データ通信のBTAMにも対応している。
  - 新しいパーティション分けされたファイル構造とアクセスインターフェイスであるBPAMに対応。主にプログラムライブラリの管理に用いられた。パーティションはスペースを解放するために圧縮する必要が相変わらずあったが、PCP、MFT、MVTではパーティションの数に制限がなく、プロジェクトごとに1本以上のパーティションを割り当てることができるため、DOS/360のコアイメージライブラリとは異なり作業が止まって開発作業に支障が出ることがほとんどなかった。
  - ファイルを階層として管理できるようにするファイル名のシステム。*PROJECT.USER.FILENAME*などの命名が可能だった。
  - [スプーラ機能](../Page/スプーリング.md "wikilink") (DOS/360にはない)。
  - アプリケーションがジョブの中でサブタスクを生成できる[マルチタスク](../Page/マルチタスク.md "wikilink")に対応。

OSが256KB未満のシステムにインストールすることは当時の経験から推奨されず\[43\]、これは1960年代にはどこでもよくある制約だった。

#### MFT

ユーザーは[MFTをインストールする際に](https://ja.wikipedia.org/wiki/OS/360 "wikilink")、メモリを最大で4本のパーティションに固定長で区切ることができ、複数のアプリケーションを同時に実行できるように設定できた\[44\]。MFTバージョンII (MFT-II)は最大で52本まで上限を緩和した。

#### MVT

MVTはMFTよりもはるかに巨大かつ複雑であり、そのためSystem/360のハイエンド機で用いられた。OSは全ての未使用メモリを単一のプールとして扱い、そこから連続した領域を並列動作するアプリケーションの数に応じて必要なだけ無制限に割り当てることができた。この方式はMFTよりもはるかに柔軟で、仕組み的にメモリを効率よく利用できたが、断片化しやすい問題があった。この問題が顕在化すると、全体としてはプログラムを実行するのに十分な空き容量があるにもかからず、各領域が分断されてしまい必要なサイズの連続した空き領域がないという状態に陥った\[45\]。

1971年にMVTで使える[タイムシェアリングオプション](https://ja.wikipedia.org/wiki/Time_Sharing_Option "wikilink")(TSO)機能が追加された。バッチジョブ実行機能、ジョブの完了通知機能、レポートが印刷されるのを待たなくても結果を閲覧できる機能などを持つエディタが含まれていたほか、System/360で使われる一部のプログラミング言語で使用できる[デバッガ](../Page/デバッガ.md "wikilink")が含まれていたことから、 TSOはプログラムの開発に広く使われるようになった。TSOはTCAM (Telecommunications Access Method)で端末と通信でき、これまで使われていたQTAM (Queued Telecommunications Access Method)と置き換わった。IBMはデータ通信のスタンダードになることを見越してTCAMと名付けたが、結局TCAMはほぼTSO上でしか使われず、1970年代後半に[VTAM](https://ja.wikipedia.org/wiki/VTAM "wikilink")にほぼ置き換えられた。

### TPモニタ

System/360のハードウェアとOSは実行に何時間もかかる可能性がある極端な[バッチジョブを処理できるように設計されている](../Page/バッチ処理.md "wikilink")。そのため各件の処理時間が30秒から数分程度の処理を1日に数千件こなす[トランザクション処理](../Page/トランザクション処理.md "wikilink")には適していなかった。IBMは1968年にトランザクションを処理するために[IMS](../Page/IMS.md "wikilink")をリリースし、1969年にはIBMグループの従業員がとある顧客のために開発した、よりシンプルなトランザクション処理システムである[CICS](../Page/CICS.md "wikilink")をリリースした。IMSはOS/360とその後継OSでしか利用できなかったが、CICSはDOS/360とその後継OSでも利用できた\[46\]\[47\]。この種の製品は長年に渡り「TP（テレプロセッシング）モニタ」と呼ばれていた。厳密に言えば、TPモニタはOSの構成要素ではなく、アプリケーションを管理するためのアプリケーションに過ぎなかった。1970年代と1980年代には複数のサードパーティ (Taskmaster、Shadow、Intercommなど）がTPモニタをリリースしてCICSと競合したが、IBMは継続的にCICSを改善してゆき、ほとんどの顧客がIBMの純正品を使うようになった\[48\]\[49\]。

### 航空会社専用システム

航空業界は1950年代に急成長していたが、数千件の予約をカードファイルを使って手作業で裁く手間による物理的な制約があったため伸び悩んでいた。IBMは1957年にコンピュータ予約システムを開発する契約を[アメリカン航空](../Page/アメリカン航空.md "wikilink")と結び、後にこのシステムを[SABRE](../Page/SABRE.md "wikilink")と名付けた。1960年にテスト版の稼働を開始し、1964年に全ての予約業務を引き受けるようになり、このプロジェクトでは最初から一貫して[IBM 7090メインフレームが用いられた](../Page/IBM_7090.md "wikilink")。IBMは1960年代初期には他の航空会社とも同様のプロジェクトを開始し、すぐに[System/360](https://ja.wikipedia.org/wiki/System/360 "wikilink")用の共通予約システムであるPARSを開発することを決めた。

SABREや初期バージョンのPARSにはアプリケーションとOSの区別がなかったが、IBMは1968年にアプリケーション部分のPARSとOS部分のACPに分割した。その後ACPはACP/TPFに改名され、また航空業界以外の業界向けに大量のオンライントランザクションを裁けるOSとして[TPF](../Page/Transaction_Processing_Facility.md "wikilink") (Transaction Processing Facility)の名前で提供した。最新バージョンは[z/TPFという名前になっている](../Page/Transaction_Processing_Facility.md "wikilink")。

IBMの汎用OS(DOS/360や[OS/360](https://ja.wikipedia.org/wiki/OS/360 "wikilink"))は1960年代中盤まで[バッチ処理](../Page/バッチ処理.md "wikilink")に特化しており、大量の短いトランザクションを高速に捌くことができず、汎用OSで動作するトランザクションモニタの[IMS](../Page/IMS.md "wikilink")や[CICS](../Page/CICS.md "wikilink")であっても、数百便のフライトの予約を数千の旅行代理店から受け付けるのに十分な処理速度がなかったことから、IBMはACPやその後継版を開発した。

最後のパブリックドメイン版であり無料版のACPはACP 9.2で、1本のミニリールテープで配布され、48インチ幅の棚一列がいっぱいに埋まるほどの数十冊のマニュアルが付属し、IBM 3340のディスクドライブに展開でき、ACPシステムの全機能が完璧に動作する形で提供された。

ACPはマスターカード<sup>®</sup>などの銀行発行カードや、金融機関向けのアプリケーションを主なユーザーとして想定していたが、航空業界用の予約システムにも利用でき、当時としてはACPは多目的な汎用OSだった。

プログラムの開発や、オンライン経由で並行してファイルをメンテナンスしたりするのに使える、VS1という(必要であればVS2も可能な)バーチャルOSをゲストとして利用できるハイパーバイザーモジュール(CHYR)が後期のACPに統合され、まさに汎用的なOSだった。

一部では本番環境もハイパーバイザーモードのVS2で運用され、IMS DBも搭載されることがあった。

### System/360 Model 20

[Model 20はSystem](https://ja.wikipedia.org/wiki/System/360モデル20 "wikilink")/360の周辺機器の一部を利用できたことから、そのシリーズの1モデルに分類されたが、これは[16ビット](../Page/16ビット.md "wikilink")機であり、他のSystem/360シリーズのマシンとはプログラムの完全な互換性がなかった。ドイツにあるIBMの複数の研究所が360/20の複数の構成に対応するよう調整した3つのOS(ディスクを搭載して最小メモリ容量が12KBのDPS、ディスクがなくテープを搭載して最小メモリ構成が8KBのTPS、パンチカード機で最小メモリ構成が4KBのCPS)を開発した\[50\]。IBMは小規模事業者向けに[System/3](https://ja.wikipedia.org/wiki/System/3 "wikilink")シリーズを後に発売し、360/20とはアーキテクチャが異なっていたことから、IBMのメインフレーム機とは周辺機器が異なる360/20の後継機は開発されなかった。

### System/360 Model 44

System/360の周辺機器を使える別アーキテクチャのプロセッサ。360/44は地質学や気象学などのデータ分析に用いられる[浮動小数点計算機能を搭載しており](../Page/浮動小数点数.md "wikilink")、科学技術計算に適した設計だった。内部のアーキテクチャが他機種と異なり、特定の用途に特化した設計であったことから、360/44にはPS/44という専用のOSが提供された\[51\]。Model 44にはSystem/360が持つ命令の一部がなかったが、命令をエミューレーションする機能があり、OS/360を実行することが可能だった。360/44とPS/44の直接的な後継機は作られなかった。

## System/370と仮想メモリOS

1970年に発表された[System/370](https://ja.wikipedia.org/wiki/System/370 "wikilink")は機能的にはSystem/360と同じだったが、System/360の同価格帯のモデル構成と比較して4倍の処理速度があった\[52\]。1972年にIBMが発表したSystem/370 Advanced Functionsは[仮想メモリの対応が目玉機能で](../Page/仮想記憶.md "wikilink")、既に販売したSystem/370に後付けで追加することが可能だった。故にIBMは仮想メモリに対応した強化版OSの販売にも力を入れた\[53\]\[54\]。

新OSのほとんどは旧OSと区別するため名前の最後に/VSを付けていた。VSはバーチャルストレージ(仮想ストレージ)の略で、メモリという言葉にはコンピュータがデータを忘れて紛失してしまうような印象を与える恐れがあったことから、IBMは意図的にバーチャルメモリ(仮想メモリ)という用語を避けていた。

IBMが販売するの今日のメインフレームが搭載するOSの全て([z/TPFを除く](../Page/Transaction_Processing_Facility.md "wikilink"))はこの時発表されたSystem/370 Advanced Functionsの子孫であり、z/TPFはIBMが当初航空会社向けに航空機の予約を大量に捌くべく開発したACPの子孫である。

### DOS/VS

DOS/VSはDOS/360の後継OSであり、仮想メモリを含む同様の機能強化があった。仮想メモリの他にもDOS/VSには下記のような機能の強化があった。

  - メモリパーティションの数を3本から5本に増強。その後すぐに7本まで増強された。
  - リローケーション・ローダー。各プログラムを別のパーティションにロードして実行する際にリンク情報を編集する必要がこれによりなくなった。
  - [スプーラコンポーネントの改良版であるPOWER](../Page/スプーリング.md "wikilink")/VS。

DOS/VSは後に大幅なアップグレードを実施した。DOS/VSEとVSE/SPが1980年代に、VSE/ESAが1991年に、[z/VSE](https://ja.wikipedia.org/wiki/z/VSE "wikilink")が2005年にリリースされた\[55\]\[56\]。

### OS/VS1

OS/VS1は[MFTの後継OSであり](https://ja.wikipedia.org/wiki/OS/360 "wikilink")、仮想メモリを含む同様の機能強化があった\[57\]。IBMは1983年までOS/VS1のマイナーチェンジを続け、1984年にサポートの終了を宣言した。IBMがSystem/370用に開発したOSの中で現代的な最新機能を持つ後継OSがないのはOS/VS1とTSS/370だけである\[58\]。

*Special Real Time Operating System*（SRTOS, 特殊用途用リアルタイムOS）であるProgramming RPQ Z06751は、[リアルタイム処理に対応するよう拡張されたOS](https://ja.wikipedia.org/wiki/リアルタイムシステム "wikilink")/VS1の亜種である。電力会社の電力管理や石油精製プラントなどの業界をターゲットにしていた\[59\]。

### OS/VS2とMVS

OS/VS2リリース1(SVS)は仮想メモリ機能を搭載した[MVTの代替OSで](https://ja.wikipedia.org/wiki/OS/360 "wikilink")、数多くの機能強化があったが、全体的なアーキテクチャは維持された。しかしIBMが1974年にOS/VS2リリース2として発表したOSは、元のOS/VS2 SVSと上位互換性を保ったまま内部が大幅に書き換えられた。システムで最も顕著な拡張は複数の仮想メモリ空間に対応したことだった。これまでは複数のアプリケーションが1つの仮想メモリ空間を共有するのが常識だったが、新OSの仮想メモリ機能ではアプリケーションごとに別々のメモリ空間が割り当てられた\[60\]。この新システムはユーザーの間ですぐに[MVS](../Page/Multiple_Virtual_Storage.md "wikilink") (マルチ仮想ストレージ)と呼ばれるようになり、元のOS/VS2はSVS (シングル仮想ストレージ)と呼ばれるようになった。IBMはこの用語を逆輸入して自社の後継OSにMVS/～の名前を付けるようになった\[61\]。

MVSに搭載された主な新機能には他にも次のようなものがあった。メインのカタログを必ず[VSAMカタログとして扱う](../Page/Virtual_Storage_Access_Method.md "wikilink")。[対称型マルチプロセッシング](../Page/対称型マルチプロセッシング.md "wikilink")のサポート(2つ以上のCPUが同じメモリとOSのコピーを共有する)。優先度の高いジョブのパフォーマンスを低下させることなくユーザーがプロセスを追加でロードできるシステムリソースマネージャ(後のバージョンでワークロードマネージャに改名)。

IBMはMVSを数回アップグレードした。MVS/SE、[MVS/SPバージョン](../Page/Multiple_Virtual_Storage.md "wikilink")1、[MVS/XAを](../Page/Multiple_Virtual_Storage.md "wikilink")1981年に、[MVS/ESAを](../Page/Multiple_Virtual_Storage.md "wikilink")1985年に、[OS/390](https://ja.wikipedia.org/wiki/OS/390 "wikilink")を1991年に、[z/OS](https://ja.wikipedia.org/wiki/z/OS "wikilink")を2001年にリリースしている\[62\]。

### VM/370

VM/370は会話型モニターシステム (CMS)というシングルユーザー用のシステムに[仮想マシン機能を組み合わせたもので](../Page/仮想機械.md "wikilink")、CMSのコピーを各ユーザーの仮想マシン上で実行できる[タイムシェアリング機能がこれにより提供された](../Page/タイムシェアリングシステム.md "wikilink")。CP/CMSはこの構成の直系の子孫である\[63\]。仮想マシン機能によりソフトウェアの開発者は仮想マシンの1つで開発作業を継続しながら別の仮想マシンを使ってテストすることができるようになり、CMSタイムシェアリングシステムはプログラムの開発に広く使われた\[64\]。

VM/370はその後アップグレードが繰り返された。VM/SEPP (Systems Extensions Program Product)、VM/BSEPP (Basic Systems Extensions Program Product)、VM/SP (System Product)、VM/SP HPO (High Performance Option)、VM/XA MA (Extended Architecture Migration Aid)、 VM/XA SF (Extended Architecture System Facility)、VM/XA SP (Extended Architecture System Product)、VM/ESA (Enterprise Systems Architecture)、[z/VM](https://ja.wikipedia.org/wiki/z/VM "wikilink")がリリースされた。またIBMはVMやその後継OS向けに、OSだけしか使えない特権命令をゲストOSに代わって実行する[ハイパーバイザ](../Page/ハイパーバイザ.md "wikilink")ーの[エミュレーション処理を高速化する](../Page/エミュレータ.md "wikilink")、[マイクロコードアシスト機能もオプションで提供した](../Page/マイクロプログラム方式.md "wikilink")。CPハイパーバイザーをさらに高速化する\[65\]Start Interpretive Execution(SIE)命令を追加した\[66\]こともIBMが370/Extended Architectureに加えた機能強化だった。

## 脚注

## 参考文献

  - [Brooks、Jr.、Frederick P.](../Page/フレデリック・ブルックス.md "wikilink") （1975） 「 [The Mythical Man-Month：Essays on Software Engineering](../Page/人月の神話.md "wikilink") 」 Addison-Wesley。 （1982年1月に改訂版）
  - [IBMメインフレームオペレーティングシステム：タイムラインと簡単な説明IBM System / 360以降については](https://web.archive.org/web/20140701185435/http://www.demorton.com/Tech/$OSTL.pdf) Dave Morton。
  - [IBMメインフレームコンピューター専用のWiki](http://ibmmainframes.com/wiki)

## 関連項目

  - [IBMメインフレーム](../Page/IBMメインフレーム.md "wikilink")

  - [オペレーティングシステムの歴史](https://ja.wikipedia.org/wiki/オペレーティングシステムの歴史 "wikilink")

  -
[Category:メインフレーム](https://ja.wikipedia.org/wiki/Category:メインフレーム "wikilink") [Category:IBMのオペレーティングシステム](https://ja.wikipedia.org/wiki/Category:IBMのオペレーティングシステム "wikilink") [Category:ソフトウェアの歴史](https://ja.wikipedia.org/wiki/Category:ソフトウェアの歴史 "wikilink") [Category:コンピュータ史](https://ja.wikipedia.org/wiki/Category:コンピュータ史 "wikilink")

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
12.
13.  describes the origins of [timesharing](../Page/タイムシェアリングシステム.md "wikilink")
14.
15.

16. Melinda Varian, *VM and the VM community, past present, and future,* SHARE 89 Sessions 9059-9061, 1977; available online at [www.princeton.edu/\~melinda](http://www.princeton.edu/~melinda/25paper.pdf) outstanding source for CP/CMS and VM history
17.
18.
19.
20.
21. [MTS History](http://www.everything2.com/index.pl?node_id=1404097&lastnode_id=0) by Dan Boulet for Everything2.com
22.
23. [*ORVYL/370 Timesharing System Functional Description*](http://www.slac.stanford.edu/spires/explain/manuals/ORVMAN.HTML), Stanford University, 1978
24. *WYLBUR Reference Manual*, Stanford University, 1984
25.
26. Chuck Boyer, [*The 360 Revolution*](http://www-306.ibm.com/software/os/zseries/pdf/360Revolution_0406.pdf)
27.
28. Chuck Boyer, [*The 360 Revolution*](http://www-306.ibm.com/software/os/zseries/pdf/360Revolution_0406.pdf)
29.
30.
31.
32.
33. Chuck Boyer, [*The 360 Revolution*](http://www-306.ibm.com/software/os/zseries/pdf/360Revolution_0406.pdf)
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
46.
47.
48.  lists the major 1970s-1980s TP monitors
49.
50.
51.
52.
53.  DPD = Data Processing Division, which was responsible for IBM's medium and large systems.
54.
55.
56.
57.
58. Non-IBM S/370 operating systems such as MTS also have no successors
59.
60.
61.
62.
63.
64.
65.
66.
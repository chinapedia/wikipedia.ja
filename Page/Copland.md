> この記事は[Copland](https://ja.wikipedia.org/wiki/Copland)から翻訳されています。


**Copland Project**（コープランド・プロジェクト）は、[1994年](../Page/1994年.md "wikilink")に[アップルが発表した](../Page/アップル_\(企業\).md "wikilink")[Macintosh](../Page/Macintosh.md "wikilink")用次世代[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink")の開発コードネーム。System 8（後に発売された[Mac OS 8とは別](https://ja.wikipedia.org/wiki/Mac_OS_8 "wikilink")）として1995年に発売される予定であった。開発は難航し[1996年](../Page/1996年.md "wikilink")に当時のCEOである[ギル・アメリオ](../Page/ギル・アメリオ.md "wikilink")と、彼が[ナショナル・セミコンダクターから引き抜いたCTOの](../Page/ナショナル_セミコンダクター.md "wikilink")[エレン・ハンコック](https://ja.wikipedia.org/wiki/エレン・ハンコック "wikilink")の調査・判断によりプロジェクトは中止された。

## 背景

1988年の3月にアップルの技術マネージャー達が今後のMac OSの開発計画を策定した。カラー化の様な短期的に達成が可能なアイデアを青い[インデックスカードに](https://ja.wikipedia.org/wiki/情報カード "wikilink")、マルチタスクといった中長期的な目標をピンクのインデックスカードに、そして実現が難しそうな物を赤色のインデックスカードにまとめた。これを元に、既存のOSを改修するBlueチームと、新OSを開発するPinkチームとの2つのプロジェクトに分かれてそれぞれ開発が行われた。当初は1990年から1991年にかけてBlueチームが既存のOSのアップデートをリリースし、93年頃にPinkチームが新OSをリリースする予定であった。

Blueチームは1991年の5月13日に[System 7を発表したが](https://ja.wikipedia.org/wiki/Classic_Mac_OS#System_7 "wikilink")、一方のPinkチームは仕様が巨大化してしまい収拾がつかなくなる、所謂[セカンドシステム症候群によって遅々として開発が進まずにいた](https://ja.wikipedia.org/wiki/人月の神話#セカンドシステム症候群（第五章） "wikilink")。同年10月2日に[IBM](../Page/IBM.md "wikilink")とアップルの連携が発表され、その契約の1つとして合弁会社「[タリジェント](https://ja.wikipedia.org/wiki/タリジェント "wikilink")」を設立し、Pinkを元にオブジェクト指向型の次世代OSの開発を行うこととなった。この連携はハードウェア的には成功し、RISC型CPUの[PowerPC](../Page/PowerPC.md "wikilink")の開発が行われ新しいMacintoshに搭載された。しかし、ソフトウェア的には失敗し、OSの開発は停滞した。事実上IBMが主導して開発することとなり、アップルの手を離れたタリジェントOSはフレームワークCommonPointと姿を変えていった。1995年12月には提携の解消に至った。

その間にもSystem 7は既に基本設計が古く様々な部分で限界が見えていた（[Classic Mac OSの初版リリースは](../Page/Classic_Mac_OS.md "wikilink")1984年）。問題点として指摘されていたのは、「メモリ保護の欠如」「[プリエンプティブなマルチタスク機構の欠如](https://ja.wikipedia.org/wiki/プリエンプティブマルチタスク "wikilink")」、「[サードパーティー](../Page/サードパーティー.md "wikilink")の基幹部分への機能拡張によるシステムの不安定化」、などが挙げられていた。これらの理由からシステムは非常に不安定なものとなり、クラッシュが頻発することとなった。さらに、PowerPC搭載モデルの[Power Macintosh登場以降もOSコアの部分に残る](../Page/Power_Macintosh.md "wikilink")[68000時代のコードによる制約があり](../Page/MC68000.md "wikilink")、PowerPCのスペックを十分に生かし切れないどころか、それが原因となったクラッシュも多発した。

旧来のMac OSの技術が陳腐化し、さらに次世代OSの開発が停滞する間にも、アップルの創業者である[スティーブ・ジョブズ](../Page/スティーブ・ジョブズ.md "wikilink")率いる[NeXT](../Page/NeXT.md "wikilink")によって開発された[NeXTSTEP](https://ja.wikipedia.org/wiki/NeXTSTEP "wikilink")、 [マイクロソフト](../Page/マイクロソフト.md "wikilink")の[Windows NT](../Page/Microsoft_Windows_NT.md "wikilink")、[サン・マイクロシステムズ](../Page/サン・マイクロシステムズ.md "wikilink")の[Solaris](../Page/Solaris.md "wikilink")など、メモリ保護機構やプリエンプティブマルチタスクを備えた堅牢な次世代OSが市場を席巻しはじめていた。

以上の背景から、次世代OSの開発の必要性に迫られ、当時の開発責任者の[デビッド・ネーゲル](https://ja.wikipedia.org/wiki/デビッド・ネーゲル "wikilink")上級副社長が中心となり、1994年に正式にCopland計画がスタートした。

## 概要

発表された計画によれば、

  - [Nukernel](https://ja.wikipedia.org/wiki/Nukernel "wikilink")と呼ばれる[マイクロカーネル](https://ja.wikipedia.org/wiki/マイクロカーネル "wikilink")を採用したモダンな[メモリ管理](../Page/メモリ管理.md "wikilink")機構
  - 完全な[プリエンプティブ](https://ja.wikipedia.org/wiki/プリエンプティブマルチタスク "wikilink")
  - 先進的な[オブジェクト指向](../Page/オブジェクト指向.md "wikilink")環境
  - 新しいルックアンドフィール
  - 旧Systemとの完全な上位互換性

など、様々な新要素が約束されていた。アピアランスマネージャを搭載し、テーマファイルを切り替えるだけで外観を大胆に変えることができる機能も発表されていた。この他に[Newtonテクノロジーの融合や](../Page/アップル・ニュートン.md "wikilink")[OpenDoc](../Page/OpenDoc.md "wikilink")によるドキュメント環境の改革などが挙げられていた。

なお[CHRP](https://ja.wikipedia.org/wiki/CHRP "wikilink")（Common Hardware Reference Platform; [AIX](../Page/AIX.md "wikilink"), Windows NT, [Mac OSなどの複数OSを実行可能な](https://ja.wikipedia.org/wiki/Mac_OS "wikilink")[PowerPC](../Page/PowerPC.md "wikilink")ハードウェアの構想）は本来Coplandを意識して開発されたものである。

## 歴史

MacintoshのOSは、1984年の出荷以降、System 7まで大幅に強化改良されたものの、基本的な部分はほとんど進化していなかった。1990年代に入ると、マルチメディアやネットワークの時代を迎え、従来はミニコンや大型汎用機のOSの機能であったマルチタスク（プリエンプティブマルチタスク）、メモリプロテクション（メモリ保護）、仮想メモリ、ネットワーク機能を備えた“モダンOS”が、次世代のパソコン用OSに必要だと考えられるようになった。

System 7が提供するマルチタスクも仮想メモリもあくまで擬似的なもので、モダンOSにはほど遠く、継ぎ接ぎで機能を拡張した結果、動作が不安定になりやすいという欠陥を抱えていた。いくら操作性や外観がよくとも、Mac OSは頻繁な強制再起動が強いられる不安定なOSとしての評価を受けることとなってしまう。この問題を解決するために、Apple社内では、幾度にもわたり新しいOSの作成が計画された。当時のSystem 7の機能を拡張してネットワーク機能やGUIを拡張する"Blue"計画は、System 7.5としてリリースされたが、未来志向の“オブジェクト指向OS”を作る“Pink”計画は、IBMも巻き込んで別会社を作り開発し始めたが、要求仕様だけが膨らみ続け、道半ばで頓挫した。

Pink OSの反省からやり直された新OSが開発コード「Copland」で、System 7.x系と互換性を持たせつつ、革新的なGUI、暫定的なマルチタスク機能と暫定的に改良されたメモリ管理機能を提供し、メモリ4MBのMac Plusでも動作するほどコンパクト、というふれこみであった。さらにCoplandの先には、モダンOSの条件を備えた、開発コード「Gershwin」が予定されていると発表された。

1996年5月、Appleは「[Worldwide Developers ConferenceでCoplandを](../Page/Worldwide_Developers_Conference.md "wikilink")『Mac OS 8』として発売する」と発表した。しかし、期待されていたベータ版の配布は行われず、基調講演でアメリオが新しいFinderのデモを見せる程度で終わってしまった。このころ、Coplandは各モジュールがばらばらに開発されている状態で、OSとして組み上げられないという悲惨なものであった。また、Gershwinは名前とコンセプトの触れ込みだけで、開発はまったく手をつけられていなかった。この状況を調べ上げたCTO兼副社長の[エレン・ハンコック](https://ja.wikipedia.org/wiki/エレン・ハンコック "wikilink")は、Coplandが完成する見込みがないと早々に判断を下した。IBMやノベルの撤退でOpenDoc計画も中止になり、Coplandは次第に人々の記憶から消えていった。

アメリオとハンコックはCoplandの開発中止を発表し、予定されていたCoplandの機能は、1年ごとに「Tempo」「Allegro」「Sonata」（いずれも開発コード）として少しずつリリース、その合間にマイナーアップデートを提供すると発表、翌[1997年](https://ja.wikipedia.org/wiki/1997年 "wikilink")1月に、「Mac OS」という呼称を初めて公式に採用したSystem7.5のマイナーアップデート版「Mac OS 7.6」が発売された。7.6登場の前後、PowerPCによる実質的なマッキントッシュ互換機のための仕様である[CHRP](https://ja.wikipedia.org/wiki/CHRP "wikilink")が策定される。CHRPは、PowerPCを搭載するマッキントッシュ上で[Windows NTなどのIBM互換機で動作するOSをネイティブに動かすことができ](https://ja.wikipedia.org/wiki/Windows_NT "wikilink")、以後のOSに対する方向性を打ち出したものだった。しかし、互換機に対する抵抗感があるAppleは二の足を踏むこととなり、1997年にNeXT社を買収したことによるRhapsody（後述）の登場によってCHRPの存在意義がなくなってしまった。

Copland計画を白紙に戻したアメリオとハンコックは、次期Mac OSとなる新たなOSを外部から調達することを決定する。計画中止後、アップルは[NeXT](../Page/NeXT.md "wikilink")を買収し次世代OS計画を "Rhapsody" へと移行させる。後に "Rhapsody" 計画は変更され、代わりに[Mac OS Xの計画が発表される](https://ja.wikipedia.org/wiki/macOS "wikilink")。"Rhapsody"自身は暫定的に[Mac OS X Serverとしてリリースされた](https://ja.wikipedia.org/wiki/Mac_OS_X_Server_1.0 "wikilink")。その間Copland技術のうち転用が可能な部分は順次Mac OS 8、9などに応用された。[ファイルシステム](../Page/ファイルシステム.md "wikilink")の[HFS+や](https://ja.wikipedia.org/wiki/HFS_Plus "wikilink")、アピアランス・マネージャ（ただしプラチナ以外のアピアランスは搭載されず、アピアランスの切り替え機能はあえて使えなくされていた）、キーチェーンなどがこれにあたる。そのうちいくつかの機能は現在の[macOS](https://ja.wikipedia.org/wiki/macOS "wikilink")にも引き継がれた。しかしこれらの機能は、本来Copland用の新しい概念のために設計された技術であり、Mac OS 8 / 9では完全に性能を生かしているとはいいがたかった。

なお、開発中止当時は[Macintosh互換機](../Page/Macintosh互換機.md "wikilink")が市場に登場した時期であった。市場では徐々に互換機が売り上げを伸ばし始めた時期であったが、アップルは再び方針を転換し互換機排除を決定した。この時、アップルと互換機メーカーのライセンス契約がSystem 7 (Mac OS 7) シリーズに限定されていた事を利用し、System 7.7として開発されていた従来型Mac OS（コードネーム:Tempo）にMac OS 8の名を割り当て、ライセンス契約を強行的に打ち切った。

## 開発の迷走と中止

Pinkプロジェクトから遡れば1990年代の初頭からすでに開始されており、実に6年にも亘って開発が行われた。しかし、様々な要因から開発は迷走をつづけた。その原因には以下のような要素が挙げられる。

  - 度重なる最高経営責任者の解任などアップル経営上層部の混乱
  - 既存のToolbox APIが68000に強く依存しており、上位互換を保つ事が技術的に非常に困難であった。
  - 開発チームや[ATGの連携がほとんど行われておらず](https://ja.wikipedia.org/wiki/アップル・アドバンスト・テクノロジー・グループ "wikilink")、個々のチームがバラバラにそれぞれの要素を開発していた
  - 営業サイドからの過大な要求を取り入れたことによって、計画が際限なく肥大化していった
  - 技術マネージャー側も計画を精査することなく、次々と新機能の開発にゴーサインをだしてしまい、リソースが発散してしまった
  - 既にメモリ保護や[プリエンプティブを搭載したWindows](https://ja.wikipedia.org/wiki/プリエンプティブマルチタスク "wikilink") NTがリリースされていた市場からの圧力
  - Coplandとは別に[Taligent](../Page/Taligent.md "wikilink")プロジェクトという別OSの開発計画を併行させた
  - [Newtonや](../Page/アップル・ニュートン.md "wikilink")[General Magicなど](https://ja.wikipedia.org/wiki/General_Magic "wikilink")、別OS/デバイスの開発計画を併行させ、Macの主要開発者が離散したこと

最初にアナウンスされたのは1995年の3月で、同年5月の[WWDC](https://ja.wikipedia.org/wiki/WWDC "wikilink")では1995年中には開発版の配布が始まり、1996年の初旬には正式版がリリースされると発表された。さらにその翌年の1997年には時期大型メジャーアップデート[Gershwin](https://ja.wikipedia.org/wiki/Gershwin "wikilink")が登場すると発表されている。しかし年内に開発版の配布は行われることはなかった。

1996年2月に新CEOにギル・アメリオが就任した。彼は当時アップルにあった300の開発案件を整理統合して50にまとめるなど、当時殆マネジメントがされていなかったアップルの開発現場を立て直そうとした。1996年2月21日、MACWORLD Expo/Tokyoにて、開発担当者のデビッド・ネーゲル上級副社長が、日本語環境のデモを披露した\[1\]が、その時も開発版が配布されることはなかった。4月にデビッド・ネーゲルが辞任すると、7月にナショナル・セミコンダクターから引き抜いたエレン・ハンコックにCTOの権限を与え、炎上したCoplandプロジェクトの収拾に当たらせた。結果、1996年7月にアップルがJDCで配布した資料によればCoplandのマルチタスク環境は暫定的なものとなり、[プリエンプティブに動作するのは](https://ja.wikipedia.org/wiki/プリエンプティブマルチタスク "wikilink")、バックグラウンドタスクのみとのことだった。また、メモリ管理機構もSystem 7の改良版に留まりモダンOSと呼ぶには程遠いものとなった。アップルの発表によれば、約束された完全に刷新されたMacintosh用モダンOSの機能は次期プロジェクトのGershwinに搭載される事となった。しかし、就任後間もなくハンコックはプロジェクトの中止を提案し、翌8月に正式に中止が決定された。1996年の8月に極少数のパートナーに開発版の "Developer Release 0" が配布されたが、まったく何もしないでもクラッシュするような代物で、実用どころか開発にすら耐えうるものでなかった。 プロジェクト打ち切り時、Coplandの構成技術は各プロジェクトチームで別々に開発された為、全てが中止された訳ではなく、プラチナアピアランスや新しいFinder、[HFS Plus等Mac](https://ja.wikipedia.org/wiki/HFS_Plus "wikilink") OS 8以降に採用されたものもある。

またアップルは開発リソースのほとんどをCoplandに注ぎ込んでいた結果、従来のMac OSへのアップデートは場当たり的な物しか行われなくなり、結果としてMacintoshの陳腐化がますます進んでしまった。

## 技術的困難

Coplandの開発にあたっては様々な技術的な困難が発生した。いくつもの要因が指摘されているが、中でも完全なシングルタスクを前提とした[Toolbox](https://ja.wikipedia.org/wiki/Toolbox "wikilink") APIは、[リエントラント](../Page/リエントラント.md "wikilink")にすることが難しかったためだと推測される。結果として[マルチタスク](../Page/マルチタスク.md "wikilink")環境との両立が極めて困難なものとなった（この反省は後の[Carbon](../Page/Carbon.md "wikilink")に生かされた）。

## 脚注

[Category:アップルのオペレーティングシステム](https://ja.wikipedia.org/wiki/Category:アップルのオペレーティングシステム "wikilink") [Category:Mac_OS](https://ja.wikipedia.org/wiki/Category:Mac_OS "wikilink") [Category:オブジェクト指向OS](https://ja.wikipedia.org/wiki/Category:オブジェクト指向OS "wikilink")

1.  [プラットフォームとしての進化 - 基調講演「サイバーメディアへの挑戦」](http://web.archive.org/web/19961202044903/http://www.apple.co.jp/MWT/conferences/manuscript/nagel.html#anchor2121684)
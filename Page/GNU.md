> この記事は[GNU](https://ja.wikipedia.org/wiki/GNU)から翻訳されています。


**GNU**（グヌー、\[1\] \[2\]）とは[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink")\[3\]\[4\]\[5\] であり、かつコンピュータソフトウェアの広範囲に渡るコレクションである。GNUは完全に[フリーソフトウェア](https://ja.wikipedia.org/wiki/フリーソフトウェア "wikilink")から構成されている\[6\]\[7\]\[8\]。

*GNU*は*"GNU's Not Unix\!"*（「GNUはUNIXではない」）の[再帰的頭字語](https://ja.wikipedia.org/wiki/再帰的頭字語 "wikilink")である。この名称が選ばれたのは、GNUは[Unix系](https://ja.wikipedia.org/wiki/Unix系 "wikilink")の設計ではあるが[UNIX](../Page/UNIX.md "wikilink")とは違いフリーソフトウェアでありUNIXに由来する[ソースコード](https://ja.wikipedia.org/wiki/ソースコード "wikilink")を全く使っていないことを示すためである\[9\]\[10\]\[11\]。GNUの正式な発音は「グヌー」である\[12\]。一般的な英語では、gnuは「ヌー」と発音し、ウシカモシカまたは**[ヌー](https://ja.wikipedia.org/wiki/ヌー "wikilink")**と呼ばれる動物をさす言葉である。GNUプロジェクトは自らの名称の呼び方について「it is pronounced g-noo, as one syllable with no vowel sound between the g and the n.」と要請している。

GNUプロジェクトには、元々[フリーソフトウェア財団](https://ja.wikipedia.org/wiki/フリーソフトウェア財団 "wikilink")が焦点を当てていたオペレーティングシステムの[カーネル](https://ja.wikipedia.org/wiki/カーネル "wikilink")である[GNU Hurdが含まれている](../Page/GNU_Hurd.md "wikilink")\[13\]\[14\]\[15\]\[16\]。しかしながらGNU Hurd以外のカーネルもGNUソフトウェアと共に利用できる。そのようなカーネルとして最も有名なものは[Linuxカーネル](https://ja.wikipedia.org/wiki/Linuxカーネル "wikilink")である。GNUのカーネルにLinuxカーネルを用いるのが一般的な理由は、GNUのカーネルがGNUの中で最も成熟していない部分のためである\[17\]\[18\]。GNUソフトウェアとLinuxカーネルを組み合わせたものが一般的に知られる[Linux](https://ja.wikipedia.org/wiki/Linux "wikilink")である（あまり一般的ではないが[GNU/Linuxと呼ばれることがある](https://ja.wikipedia.org/wiki/GNU/Linuxシステム "wikilink")。この呼称については[GNU/Linux名称論争](https://ja.wikipedia.org/wiki/GNU/Linux名称論争 "wikilink")を参照すること）。

GNUには人間が容易にコンピュータにインストールして利用可能な完全なオペレーティングシステムとするためのコンポーネントである、完全な機能を持ったカーネルが未だに欠けたままである。実際には、使用可能なGNUベースオペレーティングシステムのほとんどが[Linuxディストリビューション](https://ja.wikipedia.org/wiki/Linuxディストリビューション "wikilink")である。LinuxディストリビューションにはLinuxカーネル、GNUコンポーネント、およびGNUプロジェクト以外のフリーソフトウェアプロジェクトによるソフトウェアが多く含まれている。

プロジェクトの創設者である[リチャード・ストールマン](../Page/リチャード・ストールマン.md "wikilink")は、GNUを「社会的目的のための技術的手段」として考えている\[19\]。

## 歴史

[Richard_Stallman_-_Fête_de_l'Humanité_2014_-_010.jpg](https://ja.wikipedia.org/wiki/File:Richard_Stallman_-_Fête_de_l'Humanité_2014_-_010.jpg "fig:Richard_Stallman_-_Fête_de_l'Humanité_2014_-_010.jpg")\]\] GNUオペレーティングシステムの開発は[マサチューセッツ工科大学](https://ja.wikipedia.org/wiki/マサチューセッツ工科大学 "wikilink") (MIT) [人工知能研究所でリチャード](https://ja.wikipedia.org/wiki/MITコンピュータ科学・人工知能研究所 "wikilink")・ストールマンにより[GNUプロジェクト](https://ja.wikipedia.org/wiki/GNUプロジェクト "wikilink")として開始され、1983年9月27日にnet.unix-wizardsおよびnet.usoftという[ニュースグループ](https://ja.wikipedia.org/wiki/ニュースグループ "wikilink")で彼が公式に発表した\[20\]\[21\]。ソフトウェア開発が始まったのは1984年1月5日であり、この日はそれまでストールマンが勤務していたMIT人工知能研究所が、GNUの所有権を主張することやフリーソフトウェアとしての配布へ干渉することを阻止するために彼が同研究所を辞めた日でもある\[22\]。ストールマンが選んだGNUという名称には様々な言葉遊びが含まれており、その中には**という歌も含まれている\[23\]。

GNUの目標は、完全にフリーソフトウェアで構成されるオペレーティングシステムを実現することであった。ストールマンは[1960年代](https://ja.wikipedia.org/wiki/1960年代 "wikilink")や[1970年代](https://ja.wikipedia.org/wiki/1970年代 "wikilink")のコンピュータユーザーのように、ユーザーを自由にしたいと考えていた。その自由とは、使っているソフトウェアのソースコードを使って研究できる自由であり、ソフトウェアを他の人々と共有できる自由であり、ソフトウェアを修正できる自由であり、修正版を配布できる自由である。この哲学は後に[GNU宣言](https://ja.wikipedia.org/wiki/GNU宣言 "wikilink")として1985年3月に公表された\[24\]。

GNU宣言の中でストールマンは「基本的カーネルは存在するが、Unixをエミュレートするにはより多くの機能が必要だ」としている。ここでストールマンが想定したカーネルは、マサチューセッツ工科大学が開発した[RPC型カーネル](https://ja.wikipedia.org/wiki/遠隔手続き呼出し "wikilink")である。これは作者がフリーソフトウェアとして配布しており、[Version 7 Unixと互換性があった](https://ja.wikipedia.org/wiki/Version_7_Unix "wikilink")。そして1986年12月、開発者らはこのカーネルに修正を加える作業を開始しようとした。しかし、開発者らはこれが出発点としてはふさわしくないと判断した。何故ならTRIXは「不明確で高価な68000マシン」でしか動作せず、使用するにはまず他のアーキテクチャへの[移植が必須だったからである](https://ja.wikipedia.org/wiki/移植_\(ソフトウェア\) "wikilink")。

ストールマンは[Incompatible Timesharing System](https://ja.wikipedia.org/wiki/Incompatible_Timesharing_System "wikilink") (ITS) に関わっていた。ITSは[PDP-10](https://ja.wikipedia.org/wiki/PDP-10 "wikilink")コンピュータアーキテクチャ用に[アセンブリ言語](https://ja.wikipedia.org/wiki/アセンブリ言語 "wikilink")で書かれた初期のオペレーティングシステムだが、PDP-10自体が開発・製造されなくなったために消えていった。このためストールマンは移植性のあるソフトウェアが必要だと考えていた\[25\]\[26\]。そのため、GNUの開発にはシステムプログラミング言語として[Cと](../Page/C言語.md "wikilink")[LISP](https://ja.wikipedia.org/wiki/LISP "wikilink")を使用し\[27\]、さらにGNUをUNIX互換にする決定がなされた\[28\]。当時UNIXは既に[プロプライエタリなオペレーティングシステムとして広く使われていた](https://ja.wikipedia.org/wiki/プロプライエタリ・ソフトウェア "wikilink")。UNIXの設計はモジュール性が高く、部分ごとに再実装することが可能だった\[29\]。

GNUに必要なソフトウェアの大部分は一から書かれたが、[TeX](../Page/TeX.md "wikilink")[組版](https://ja.wikipedia.org/wiki/組版 "wikilink")システムや[X Window System](https://ja.wikipedia.org/wiki/X_Window_System "wikilink")\[30\]、さらに[Mach](../Page/Mach.md "wikilink")[マイクロカーネル](https://ja.wikipedia.org/wiki/マイクロカーネル "wikilink")といった共有可能な[サードパーティー](https://ja.wikipedia.org/wiki/サードパーティー "wikilink")フリーソフトウェアコンポーネントは既存のものを流用した。なおMachは（GNUの公式カーネルである）GNU Hurdの、[GNU Machコアの基礎を形成している](https://ja.wikipedia.org/wiki/GNU_Mach "wikilink")\[31\]。前述したサードパーティーコンポーネントを除くGNUのコードの大部分はボランティアが書いたものであり、具体的には個人が余暇時間内や会社の業務内で書いた部分\[32\]、および教育機関や非営利団体が書いた部分で構成されている。1985年10月、ストールマンは[フリーソフトウェア財団](https://ja.wikipedia.org/wiki/フリーソフトウェア財団 "wikilink") (FSF) を創設した。[1980年代](../Page/1980年代.md "wikilink")後半から[1990年代](https://ja.wikipedia.org/wiki/1990年代 "wikilink")にはFSFがソフトウェア開発者を雇い、GNUで必要となるソフトウェア作成を行わせた\[33\]\[34\]。

GNUプロジェクトの初期の計画では、[BSD](https://ja.wikipedia.org/wiki/BSD "wikilink") 4.4-Liteのカーネルを採用することになっていた。しかし、[バークレーのプログラマの協力が得られなかったため](https://ja.wikipedia.org/wiki/カリフォルニア大学バークレー校 "wikilink")、ストールマンは1988年に[カーネギーメロン大学](https://ja.wikipedia.org/wiki/カーネギーメロン大学 "wikilink")が開発した[Mach](../Page/Mach.md "wikilink")カーネルを採用することにした。ただし、Machには[AT\&T](https://ja.wikipedia.org/wiki/AT&T "wikilink")由来のコードが使われていたため、それを取り除いてフリーソフトウェアとして使えるようになったのは1990年である。HurdのアーキテクトだったThomas Bushnellは後に、BSDカーネルの採用を見送ったことでプロジェクトは大きく後退しており、そういう意味でもBSDカーネルを採用すべきだったと述べている\[35\]。

カーネルの設計は、GNUの中でもUNIXから最も大きく異なる部分である。GNUのカーネルはマルチサーバ型マイクロカーネルであり、従来のUNIXカーネルの持つ機能をサーバと呼ばれる複数のプログラムで構成している。Machのマイクロカーネルは非常に低レベルのカーネル機能しか提供していないため、GNUプロジェクトではカーネルの上位レベルの部分を一種のユーザープログラムの集合体として開発しなければならなかった。この集合体を当初Alixと呼んでいたが、Thomas BushnellはHurdと呼ぶことを好み、Alixの名はそのサブコンポーネントに移され、最終的には使われなくなった\[36\]。その後、Hurdの開発は技術的問題がいくつも発生し、なかなか進展しない状況になった\[37\]。

GNUが有名になるにつれて、GNUに興味を持つ企業が現れはじめた。それらの企業は開発援助をしたり、GNUのソフトウェアや技術サポートを組み合わせて商売するようになっていった。その中で最も成功した企業としては[シグナスソリューションズ](https://ja.wikipedia.org/wiki/シグナスソリューションズ "wikilink")が知られている\[38\]（同社は現在、[レッドハット](https://ja.wikipedia.org/wiki/レッドハット "wikilink")の一部となっている\[39\]）。

1992年、最重要コンポーネントであるカーネルのGNU Hurdを除く全てのコンポーネントが完成した。1991年には[リーナス・トーバルズ](https://ja.wikipedia.org/wiki/リーナス・トーバルズ "wikilink")が独自にLinuxカーネルの開発を始めており、1992年にはLinuxのバージョン0.12が[GNU General Public Licenseライセンスでリリースされ](https://ja.wikipedia.org/wiki/GNU_General_Public_License "wikilink")、この最後の空白を埋めた。LinuxとGNUを組み合わせることで、世界初の完全にフリーソフトウェアで構成されたオペレーティングシステムとなった。LinuxカーネルはGNUプロジェクトの一部ではないが、その開発には[GCCなどのGNU製プログラミングツールが使われている](https://ja.wikipedia.org/wiki/GNUコンパイラコレクション "wikilink")\[40\]。

2002年にストールマンはGNU/Hurdのリリースについて楽観的声明を発表したが\[41\]、開発は2016年現在も続いている。Hurdの最新リリースはバージョン0.9である。動作はそれなりに安定しており、重要なアプリケーションを使うのでなければ十分使えるレベルである。

## コンポーネント

GNUシステムの基本コンポーネントには[GNUコンパイラコレクション](https://ja.wikipedia.org/wiki/GNUコンパイラコレクション "wikilink") (GCC)、[GNU Cライブラリ](https://ja.wikipedia.org/wiki/GNU_Cライブラリ "wikilink") (glibc) および[GNU Core Utilities](https://ja.wikipedia.org/wiki/GNU_Core_Utilities "wikilink") (Coreutils) だけでなく、[GNUデバッガ](https://ja.wikipedia.org/wiki/GNUデバッガ "wikilink") (GDB)、[GNU Binutils](https://ja.wikipedia.org/wiki/GNU_Binutils "wikilink") (binutils)\[42\]、[GNU Bash](https://ja.wikipedia.org/wiki/Bash "wikilink")[シェル](https://ja.wikipedia.org/wiki/シェル "wikilink")\[43\]\[44\]、および[GNOME](https://ja.wikipedia.org/wiki/GNOME "wikilink")[デスクトップ環境](https://ja.wikipedia.org/wiki/デスクトップ環境 "wikilink")も含まれる\[45\]。GNUの開発者はGNUアプリケーションやユーティリティのLinuxへの移植に貢献しており、それらのアプリケーションやユーティリティは[BSD](https://ja.wikipedia.org/wiki/BSD "wikilink")の派生、[Solaris](https://ja.wikipedia.org/wiki/Solaris "wikilink")そして[macOS](https://ja.wikipedia.org/wiki/macOS "wikilink")といったLinux以外のオペレーティングシステムでも広く利用されている\[46\]。

GNUのプログラムの多くは、[Microsoft Windows](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")\[47\]やmacOS\[48\]といったプロプライエタリプラットフォームを含む他のオペレーティングシステムに移植されている。GNUのプログラムはプロプライエタリUNIX上の相当するソフトウェアよりも信頼性が高いことが示されている\[49\]。

2015年11月の時点で、公式GNU開発サイトにホストされたGNUのパッケージ数は合計で466個存在する（終了したパッケージも含む。それらを除くと383個である）\[50\]。

[GNewSense_screenshot.png](https://ja.wikipedia.org/wiki/File:GNewSense_screenshot.png "fig:GNewSense_screenshot.png")\]\] [Parabola12.png](https://ja.wikipedia.org/wiki/File:Parabola12.png "fig:Parabola12.png")モデルを用いるFSF認定ディストリビューションの例である[Parabola GNU/Linux-libre](https://ja.wikipedia.org/wiki/Parabola_GNU/Linux-libre "wikilink")\]\]

## GNUの派生

GNUプロジェクトの公式カーネルは[GNU Hurdマイクロカーネルである](../Page/GNU_Hurd.md "wikilink")。しかしながら、2012年の時点でLinuxカーネルが[Linux-libre](https://ja.wikipedia.org/wiki/Linux-libre "wikilink")という形で公式にGNUプロジェクトの一部となった。Linux-libreは、Linuxカーネルから全てのプロプライエタリコンポーネントを削除した派生物である\[51\]。

[FreeBSD](../Page/FreeBSD.md "wikilink")のカーネルのようなLinux以外のカーネルも、実用的なオペレーティングシステムを構成するGNUソフトウェアと連携して機能する\[52\]。FSFはGNUツールやユーティリティと共に利用されるLinuxはGNUの派生とみなすべきであると主張しており、そのようなシステムを*GNU/Linux*という用語で表現するよう奨励している（なおこのことが[GNU/Linux名称論争](https://ja.wikipedia.org/wiki/GNU/Linux名称論争 "wikilink")の原因となっている）\[53\]\[54\]\[55\]。GNUプロジェクトは[gNewSense](https://ja.wikipedia.org/wiki/gNewSense "wikilink")、[Trisquelおよび](https://ja.wikipedia.org/wiki/Trisquel_GNU/Linux "wikilink")[Parabola GNU/Linux-libreといったLinuxを用いた派生を支持している](https://ja.wikipedia.org/wiki/Parabola_GNU/Linux-libre "wikilink")\[56\]。カーネルとしてHurdを使用しない派生でLinux以外のカーネルを用いるものとしては、BSDカーネル上にGNUの初期計画を実現した、Debian GNU/kFreeBSDやDebian GNU/NetBSDがある。さらにGNUを[NetBSD](https://ja.wikipedia.org/wiki/NetBSD "wikilink")や[OpenSolaris](https://ja.wikipedia.org/wiki/OpenSolaris "wikilink")などのカーネルで動作させる移植プロジェクトもある。

## コピーライト、GNUライセンスと管理

フリーソフトウェア財団は既存のプロジェクトへの小規模な変更のリリースを[パブリックドメイン](../Page/パブリックドメイン.md "wikilink")とすることが無難だと考えている\[57\]が、GNUプロジェクトでは、その貢献者に対してGNUパッケージの著作権をフリーソフトウェア財団に譲渡することを推奨している\[58\]\[59\]。ただしこれは必須ではない。パッケージのメンテナは自身が維持するGNUパッケージの著作権を維持することができるが、使用される（GNU GPLのような）ライセンスは著作権保持者しか強制させることができないので、この場合はフリーソフトウェア財団ではなく著作権保持者がライセンスを強制する\[60\]。

GNUに必要なソフトウェアの開発のため、ストールマンはユーザーがフリーソフトウェアを共有し変更する自由を保障することを目的とした、[GNU General Public Licenseと呼ばれるライセンスを書いた](https://ja.wikipedia.org/wiki/GNU_General_Public_License "wikilink")（最初はEmacs General Public Licenseと呼ばれた）\[61\]。彼は[ジェームズ・ゴスリン](https://ja.wikipedia.org/wiki/ジェームズ・ゴスリン "wikilink")とのUniPressと呼ばれるプログラムに対するGNU Emacsプログラムにおけるソフトウェアコードの使用についての論争をめぐる経験をふまえてこのライセンスを書いた\[62\]\[63\]。1980年代のほとんどの期間において、Emacs General Public LicenseやGCC General Public LicenseのようにGNUパッケージごとに個別のライセンスが存在した。1989年にFSFはGNUプロジェクトのソフトウェアだけでなく全てのソフトウェアに使用できる単一のライセンスであるGNU General Public License (GPL) を発表した\[64\]\[65\]。

現在GPLはGNUソフトウェアのほとんどで使われており、GNUプロジェクトとは関係のないフリーソフトウェアでもよく使われている。GPLは最も一般的に使用される[フリーソフトウェアライセンス](https://ja.wikipedia.org/wiki/フリーソフトウェアライセンス "wikilink")である\[66\]。GPLでは、著作物の受領者はそれを実行し、複製し、修正し、再配布できるが、その再配布物のライセンスに制限を加えることを許さない。この思想は[コピーレフト](https://ja.wikipedia.org/wiki/コピーレフト "wikilink")と呼ばれることが多い\[67\]。

1991年、[GNU Cライブラリを](https://ja.wikipedia.org/wiki/GNU_Cライブラリ "wikilink")[プロプライエタリ・ソフトウェア](https://ja.wikipedia.org/wiki/プロプライエタリ・ソフトウェア "wikilink")とリンクできるようにするためにLibrary General Public Licenseとして知られる[GNU Lesser General Public License](https://ja.wikipedia.org/wiki/GNU_Lesser_General_Public_License "wikilink") (LGPL) が書かれ\[68\]、さらにGNU GPLのバージョン2がリリースされた。2000年には文書用に[GNU Free Documentation Licenseが書かれた](../Page/GNU_Free_Documentation_License.md "wikilink")\[69\]。GPLとLGPLは2007年にバージョン3に修正され、ユーザーが自身のデバイスで修正されたソフトウェアの実行を妨げるからユーザーを保護するための条項が追加された\[70\]。

GNUプロジェクトのライセンスは、GNU独自のソフトウェアパッケージだけではなく、GNUが直接的には作成していないソフトウェアプロジェクト(あるいはパッケージ)でも使用されている。GNUソフトウェアと組み合わせて使用されることが多いソフトウェア、例えば、Linuxカーネルなどがその代表である。一方、対照的に、Unix系のGUI環境を構築するX Window Systemは、Linuxディストリビューションでも標準的に使用されてきたソフトウェアパッケージであるが、こちらはGNUライセンスではなく、[パーミッシブ・ライセンス](https://ja.wikipedia.org/wiki/パーミッシブ・ライセンス "wikilink")に基づいてライセンスされる。前者が多数派であり、後者は少数派である。

## ロゴ

GNUのロゴは[ヌー](https://ja.wikipedia.org/wiki/ヌー "wikilink")の[頭](https://ja.wikipedia.org/wiki/頭 "wikilink")である。元々はEtienne Suvasaによって描かれ、現在ではAurelio Heckertがデザインした大胆でシンプルなバージョンが好まれている\[71\]\[72\]。これはGNUソフトウェアや印刷されたり電子化されたGNUプロジェクトの文書に表示され、フリーソフトウェア財団のマテリアルにも使われる。

なお本章で示したGNU30周年記念ロゴは公式ロゴの修正バージョンであり、2013年9月にGNUプロジェクト30周年記念としてフリーソフトウェア財団によって作成されたものである\[73\]。

<File:Heckert> GNU white.svg|主にGNUの[ロゴとして用いられる](https://ja.wikipedia.org/wiki/ロゴタイプ "wikilink")「上品(Handsome)な」ヌー [File:Philosophical-gnu-sm.png|主にGNUの思想を論じる際に用いられる「冷静（Philosophical）な」ヌー](File:Philosophical-gnu-sm.png%7C主にGNUの思想を論じる際に用いられる「冷静（Philosophical）な」ヌー) [File:Gnu-30-banner-without-background.svg|GNU30周年記念ロゴ](File:Gnu-30-banner-without-background.svg%7CGNU30周年記念ロゴ)

## 脚注

## 関連項目

  - [クリエイティブ・コモンズ](https://ja.wikipedia.org/wiki/クリエイティブ・コモンズ "wikilink")

  - [フリーソフトウェア財団](https://ja.wikipedia.org/wiki/フリーソフトウェア財団 "wikilink")

  - [フリーソフトウェア運動](https://ja.wikipedia.org/wiki/フリーソフトウェア運動 "wikilink")

  -
  - [GNUパッケージ一覧](https://ja.wikipedia.org/wiki/GNUパッケージ一覧 "wikilink")

## 外部リンク

  -
  - [Microsoft Windows用のGNUユーティリティの移植](http://unxutils.sourceforge.net/)

  - [The daemon, the GNU and the penguin](http://www.verbumvanum.org/pesalus/)

[Category:Unix系オペレーティングシステム](https://ja.wikipedia.org/wiki/Category:Unix系オペレーティングシステム "wikilink") [Category:GNUプロジェクト](https://ja.wikipedia.org/wiki/Category:GNUプロジェクト "wikilink") [Category:フリーソフトウェアOS](https://ja.wikipedia.org/wiki/Category:フリーソフトウェアOS "wikilink")

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
13.
14. Vaughan-Nichols, Steven J. "[Opinion: The top 10 operating system stinkers](http://www.computerworld.com/s/article/9131178/Opinion_The_top_10_operating_system_stinkers)", **, April 9, 2009: "…after more than 25 years in development, GNU remains incomplete: its kernel, Hurd, has never really made it out of the starting blocks. \[…\] Almost no one has actually been able to use the OS; it's really more a set of ideas than an operating system."
15.
16. Lessig, Lawrence. *The Future of Ideas: The Fate of the Commons in a Connected World*, p. 54. Random House, 2001. ISBN 978-0-375-50578-2. About Stallman: "He had mixed all of the ingredients needed for an operating system to function, but he was missing the core."
17.
18.
19. .
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
30.
31.
32.
33.
34.
35.
36. [About the GNU Project - GNU Project - Free Software Foundation (FSF)](http://www.gnu.org/gnu/thegnuproject.html)
37.
38.
39. [Red Hat buys software firm, shuffles CEO - CNET News](http://news.cnet.com/2100-1001-232971.html)
40. [What would you like to see most in minix?](http://groups.google.com/group/comp.os.minix/browse_thread/thread/76536d1fb451ac60/b813d52cbc5a044b) Linus Benedict Torvalds (Aug 26 1991, 2:12 am) - comp.os.minix | Google Groups
41.
42.
43.
44.
45.
46.
47.
48.
49. [Fuzz Revisited: A Re-examination of the Reliability of UNIX Utilities and Services](http://ftp.cs.wisc.edu/pub/paradyn/technical_papers/fuzz-revisited.ps) - October 1995 - Computer Sciences Department,University of Wisconsin
50.
51.
52.
53.
54.
55.
56. .
57.
58.
59.
60.
61. .
62.
63. .
64.
65. .
66.
67.
68. .
69.
70.
71.
72.
73.
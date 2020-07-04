> この記事は[OSx86](https://ja.wikipedia.org/wiki/OSx86)から翻訳されています。


**OSx86**は、[アップル製ではない](../Page/アップル_\(企業\).md "wikilink")[PC/AT互換機](https://ja.wikipedia.org/wiki/PC/AT互換機 "wikilink")で、アップルの[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink")である**[macOS](https://ja.wikipedia.org/wiki/macOS "wikilink")**を動作させようという、[コミュニティを通じた共同作業による](../Page/共同体.md "wikilink")[ハッキング](../Page/ハッキング.md "wikilink")・プロジェクトである。その手法は[インテル](https://ja.wikipedia.org/wiki/インテル "wikilink")製[マイクロプロセッサ](../Page/マイクロプロセッサ.md "wikilink")搭載マシンを対象にしたものが多いが、[コミュニティ](https://ja.wikipedia.org/wiki/コミュニティ "wikilink")の参加者の手により[AMDのマイクロプロセッサや](https://ja.wikipedia.org/wiki/アドバンスト・マイクロ・デバイセズ "wikilink")[VMware](../Page/VMware.md "wikilink")で動作するもの、更にはLiveDVDで動作するものなどがその歴史の中で開発されている。最近では、OSx86を動作させるPCのこと、またはOSx86そのものをさして、”Hackintosh”（HackとMacintoshをもじった造語）とも呼ばれる。 現在、様々な包括ソフトウェアの開発により、プロジェクト始動当初に比べそのハードルは大きく下がったと言える。

## 概要

### 初期の試み

2005年6月の[WWDC](../Page/Worldwide_Developers_Conference.md "wikilink")（Worldwide Developers Conference、ワールドワイド デベロッパーズ カンファレンス）で、アップルがそれまで採用していた[PowerPC](../Page/PowerPC.md "wikilink")マイクロプロセッサを、インテル製品に切り変える計画を発表した直後からこの試みは見られた。初めの頃は、アップルが開発者向けに999ドルで配布した、*Developer Transition Kit* （デベロッパーズ トランジション キット）の[DVD](../Page/DVD.md "wikilink")の一部がコピーされ、出回ったことでこの動きが広まった。 2007年には、Mac OS X v10.4.9をベースにしたインストールDVDがリリースされている。

### 現在

当初はマニア向けの試みであったOSx86プロジェクトであるが、その手法は次第に洗練されてゆく。今では、USBメモリ一1本と実験用のマシン1台、そしてOS Xを買うための1700円があれば誰でも試すことができる。その背景として、OSx86向けのドライバおよびそれをパッケージ化したものが飛躍的に充実してきたことがあげられる。あるものは有志により開発され、あるものは本家Macから移植され、市場の多くのパーツが「OS X対応」になったのである。OSx86インストールの手順を詳しく解説するウェブサイト・個人ブログも増え、大手ブログメディアであるLifehackerまでもがOSx86を紹介した。Mac Pro並の性能を持つハードウェアが格安で手に入ること、安定性の向上などから、OSx86は一部のユーザーのメインマシンにもなっている。

## 各バージョンにおける手法の変遷

### Mac OS X v10.4 "Tiger"

アップルが自社製コンピューターをインテルベースに切り替えることを決定した時点での現行OSであり、OSx86プロジェクトはこのバージョンのMac OSから始まった。 2006年1月10日、アップルは初のインテル製マイクロプロセッサ向け製品として、Mac OS X v10.4.4を[iMac](https://ja.wikipedia.org/wiki/iMac "wikilink")および[MacBook Proとともにリリースした](../Page/MacBook_Pro.md "wikilink")。これらの製品には、ほとんどの[x86](https://ja.wikipedia.org/wiki/x86 "wikilink")[マザーボード](../Page/マザーボード.md "wikilink")に見られる[BIOSに代えて](https://ja.wikipedia.org/wiki/Basic_Input/Output_System "wikilink")、EFI ([Extensible Firmware Interface](../Page/Unified_Extensible_Firmware_Interface.md "wikilink")) が採用された。

2006年2月14日、初の[クラッキング方法が](../Page/クラッキング_\(コンピューター用語\).md "wikilink")、*Maxxuss*というユーザ名のハッカーによりインターネットに流れた。数時間のうちに、アップルは10.4.5アップデータを配布したが、その後また2週間を待たずに*Maxxuss*はこれに対してクラッキングを可能にする[パッチ](../Page/パッチ.md "wikilink")を配布した。2006年4月3日、アップルは 10.4.6 アップデータを配布。するとまた2週間を待たずして、アップデートされたOS Xを非アップル製PCへインストールを可能にするパッチが配布された。このパッチは、*SemjaZa*というハッカーによるもので、*JaS*によってコンパイルされた。*JaS*は同年6月に、10.4.4のカーネルを使用した非アップル製PC向けの10.4.7をリリースした。以降、コミュニティに参加する複数の参加者の手によって、このプロジェクトは進行していく。

10.4.8アップデータに至るまで、すべてのOSx86プロジェクトによるパッチは、10.4.4のカーネルを採用している。より新しいカーネルを採用した取り組みに関しては、10.4.8のOSx86ユーザは、多くの問題点に遭遇している。

アップルはハードウェアに対して、SSE3（[ストリーミングSIMD拡張命令](../Page/ストリーミングSIMD拡張命令.md "wikilink")）拡張命令をより多く採用するようになり、SSE2のみをサポートする[CPU](../Page/CPU.md "wikilink")を採用しているハードウェアでシステムを動かすことを困難にさせている。しかしコミュニティは、この問題も克服して行く。

2007年3月、OSx86コミュニティは、ハードディスクドライブにインストールすることなしに Mac OS X v10.4.8を起動させることができる、Live DVD（[Live CDの](../Page/Live_CD.md "wikilink")[DVD](../Page/DVD.md "wikilink")版）を開発するという特筆すべき進歩を見せた。また同月、OSx86プロジェクトを進めてきた *InsanelyMac*の[ウェブサイト](../Page/ウェブサイト.md "wikilink")が、[イギリス](https://ja.wikipedia.org/wiki/イギリス "wikilink")のFubra Limitedに売却された。一部の人は、このウェブサイトの商業化に反対した。

### Mac OS X v10.5 "Leopard"

*Uphuck*と呼ばれるハッカーが、iATKOSというコードネームでMac OS X Leopard全体を含むDVDイメージインストーラーを、インターネットを通じて配布した。このインストーラーは、アップルのライセンス同意契約に違反している。*Kalyway*と呼ばれるハッキングチームは、[スタンドアローン](../Page/スタンドアローン.md "wikilink")の10.5.1 DVDイメージインストーラーを作成した。*Zephyroth*と呼ばれるハッカーは、10.5.2をAMDベースのPC用にリリースした。

### Mac OS X v10.6 "Snow Leopard"

2009年にMac OS X v10.6 (Snow Leopard) がリリースされると、[OSX86 Project](http://www.osx86project.org/)でSnow Leopardへのアップデート方法が紹介された。10.6.5へのアップデートを経て、2011年1月の10.6.6へのアップデート方法も紹介された。 これまではインストーラーや、インストールパッケージに様々な改変が加えられたISOイメージをP2Pなどでダウンロードする、という形式が主だったのに対し、このバージョンより正規のDVDを用いたインストールが主流となっていった。Vanilla(改変されていない素のソフトウェア)状態のカーネルを利用するため、Appleによるソフトウェアアップデートを即座に受けられたり、より本来のMac OS Xに近い(第三者の手が加わっていない)状態で利用することが可能となった。これは、10.7以降のOS Xの提供方法の変化と相まって、現在のOSx86インストール方法の主流である。

### OS X v10.7 "Lion"

このバージョンのOS Xより、アップデータファイルがApp Storeを通じて販売されるようになり、OSx86のインストール方法にも変化が現れた。tonymacx86と名乗るグループがunibeastと呼ばれるソフトウェアの配布を開始した。このソフトの実態は、App Storeよりダウンロードしたアップデータからディスクイメージを読み出し、USBメモリからインストーラを起動できるようにするスクリプトである。この手法は、次のバージョンであるOS X 10.8 Lionでも有効である。このスクリプトを用いずとも、適切にディスクイメージを展開し、USBメモリなどにコピーすることでインストールディスクを作成できる。

### OS X v10.8 "Mountain Lion"

### OS X v10.9 "Mavericks"

基本的には、前バージョンであるLionと手法に変化はない。tonymacx86にて配布されているMultibeastなどのソフトウェアスイートの適切なバージョンを利用することで、オリジナルのインストーラからインストール可能である。

## OSx86ソフトウェア

### Multibeast

tonymacx86により作成・配布されている、OSx86のためのドライバ等を一括インストールするパッケージである。このパッケージには、OSx86の動作に最低限必要なドライバ、ネットワークドライバ、オーディオドライバ、システムプロファイル、ブートローダーなどが含まれる。自分の環境に合わせた組み合わせでインストールするドライバを選択する。この際、不適切なファイルや、競合する組み合わせを選択すると、システムが起動しなくなる恐れがあるため注意が必要である。

### Unibeast

Mac App Storeより配布されているOS Xのインストーラー内には起動可能なディスクイメージが内蔵されている。このディスクイメージを展開・再編してUSBメモリ上にコピーすることで、起動可能なインストール用のUSBメモリを作成するためのスクリプトである。パッケージ(\*.pkg)として配布されているが、先述の機能がパッケージスクリプトとして実装されている。

### Clover bootloader

Clover bootloaderは、UEFIファームウェアまたはレガシBIOSのためのブートローダである。このブートローダは、Macintoshコンピュータの持つ独自の機能(NVRAM等)をエミュレートし、PC/AT互換機でのmacOSの正常な動作をサポートする。また、テーマ機能をサポートし、オペレーティングシステムやコンピュータに適したテーマの使用が可能である。macOSの他にも、一部のWindowsやLinuxの起動もサポートする。

## 問題点

アップルは、自社製品以外のインテルプロセッサ搭載PCで、[macOS](https://ja.wikipedia.org/wiki/macOS "wikilink")を動かすことは認めないと明言している\[1\]。また、前述の様にクラッキング済みのインストールDVDイメージが[P2Pを通じて](../Page/Peer_to_Peer.md "wikilink")、不正に流通していることは著作権の侵害行為に当たる。また、配布されているドライバやソフトウェアは有志により制作され、その妥当性は保証されず、故意または過失によりユーザーに損害を与えるソフトウェアをインストールしてしまうリスクがある。 技術的な問題として、macOSは本来Macハードウェアに向け設計されたソフトウェアであるため、それを他のPCで起動することによるハードウェアおよびソフトウェアに対して潜在的なリスクが存在する可能性がある。

## 脚注

### 出典

<references/>

## 外部リンク

  - [OSx86 Project home page](http://www.osx86project.org/) (英語)
  - [tonymacx86](http://www.tonymacx86.com/home.php) (英語)

[Category:X86アーキテクチャ](https://ja.wikipedia.org/wiki/Category:X86アーキテクチャ "wikilink") [Category:MacOS](https://ja.wikipedia.org/wiki/Category:MacOS "wikilink")

1.  [「アップル、強権発動か―「OSx86 Project」などの掲示板が閉鎖に」](http://japan.cnet.com/news/media/story/0,2000056023,20096785,00.htm) CNET Japan 2006年2月20日
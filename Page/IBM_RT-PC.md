> この記事は[IBM RT-PC](https://ja.wikipedia.org/wiki/IBM_RT-PC)から翻訳されています。


**IBM RT**は[ISAバスと](../Page/Industry_Standard_Architecture.md "wikilink")[IBM 801からの派生品である](../Page/IBM_801.md "wikilink")[ROMP](https://ja.wikipedia.org/wiki/ROMP "wikilink")[マイクロプロセッサ](../Page/マイクロプロセッサ.md "wikilink")を使った[コンピュータ](../Page/コンピュータ.md "wikilink")システムである。このシステムは[1986年](https://ja.wikipedia.org/wiki/1986年 "wikilink")、**RT PC**(*RISC Technology Personal Computer*)として最初に登場し、**[AIX](https://ja.wikipedia.org/wiki/AIX "wikilink")** 1.x, 2.x または**AOS**(*Academic Operating System*)か Pick operating system が動作した。一般に間違って*PC RT*と覚えている人が多いので注意。後にIBMは名前を単純化した。このマシンはあまり成功せず、全ての機種が[1991年](../Page/1991年.md "wikilink")に値下げされた。しかし開発は拍車がかかり、後に[RS/6000](https://ja.wikipedia.org/wiki/RS/6000 "wikilink")と[POWERのシリーズに引き継がれ](../Page/POWER_\(マイクロプロセッサ\).md "wikilink")、後の[PowerPC](../Page/PowerPC.md "wikilink")へと繋がっていくのである。

## ハードウェア

RTには3つの機種が製造された。**6150**、**6151**、**6152**である。マシンの形状はいわゆるタワー型(6150)とデスクトップ型(6151)である。これらの機種のプロセッサカードは特殊な形状だった。

6150/6151のプロセッサカードには3つのバージョンがある。標準的な032プロセッサカードは170nsのプロセッササイクル時間で、1Mバイトの標準メモリ(1Mバイト、2Mバイト、4Mバイトメモリカードで拡張可能)とオプションの[浮動小数点アクセラレータを搭載可能だった](../Page/浮動小数点数.md "wikilink")。改良型プロセッサカードでは100nsプロセッササイクルで、4Mバイトメモリか[ECCつき](../Page/誤り検出訂正.md "wikilink")4Mバイトメモリを搭載し、20MHzの[MC68881](../Page/MC68881.md "wikilink")浮動小数点プロセッサを搭載していた。拡張改良型プロセッサカードではサイクル時間は80ns、16Mバイトメモリ、さらに標準で改良された浮動小数点アクセラレータが搭載されていた。

6152という番号のマシンは [IBM PS/2](https://ja.wikipedia.org/wiki/IBM_PS/2 "wikilink") model 60 と[マイクロチャネルボードバージョンの](https://ja.wikipedia.org/wiki/Micro_Channel_Architecture "wikilink")032プロセッサのハイブリッドで、そのボードは"クロスボウボード"とあだ名された。こちらはAOSだけが動作し、AOSの動作している6150か6151から[LANを介して](../Page/Local_Area_Network.md "wikilink")[TCP/IP](https://ja.wikipedia.org/wiki/TCP/IP "wikilink")プロトコルでOSをダウンロードして動作した。

典型的な構成としては、[ハードディスクドライブ](https://ja.wikipedia.org/wiki/ハードディスクドライブ "wikilink")が 20MB から 80MB で、1024×1024 ピクセルの 8ビットグレイスケールのグラフィックスプロセッサ、4MB/s [トークンリング](../Page/トークンリング.md "wikilink")アダプターか 10Mbit/s [イーサネット](../Page/イーサネット.md "wikilink")（10Base2）アダプターが装備されていた。

## ソフトウェア

RT での特筆すべき点は、[マイクロカーネル](https://ja.wikipedia.org/wiki/マイクロカーネル "wikilink")の採用であった。キーボード、マウス、ディスプレイ、ディスク装置、ネットワークは全てマイクロカーネルで制御され、その上に複数の[OSを同時に動作させることが可能であった](../Page/オペレーティングシステム.md "wikilink")。特殊なキー操作でOSからOSへ移動することが可能であった。それによって、各OSはキーボードとマウスとディスプレイの制御権を得る。AIX バージョン 2 と Pick OS がマイクロカーネル上に移植された。

RT の主たるOSは AIX バージョン 2 であった。AIX v2 の[カーネル](../Page/カーネル.md "wikilink")の大部分は [PL/I](https://ja.wikipedia.org/wiki/PL/I "wikilink")言語で書かれており、AIX v3 への移行時に問題となった。AIX v2 は [TCP/IP](https://ja.wikipedia.org/wiki/TCP/IP "wikilink") を完全サポートしており、同時に [SNA](https://ja.wikipedia.org/wiki/SNA "wikilink")、2種類の[分散ファイルシステム](../Page/分散ファイルシステム.md "wikilink")（[NFS](../Page/Network_File_System.md "wikilink") と Distributed Services）をサポートしている。Distributed Services (DS) は SNA 上に構築された分散ファイルシステムであり、[AS/400](https://ja.wikipedia.org/wiki/System_i "wikilink") や IBM の[メインフレーム](../Page/メインフレーム.md "wikilink")との連携が可能であった。[GUI](https://ja.wikipedia.org/wiki/グラフィカルユーザインタフェース "wikilink") としては、X10.3、X10.4、X11 の [X Window System](../Page/X_Window_System.md "wikilink") を採用していた。[コンパイラ](../Page/コンパイラ.md "wikilink")としては[FORTRAN](../Page/FORTRAN.md "wikilink")と[C言語](../Page/C言語.md "wikilink")が用意されていた。デスクトップアプリケーションとしては、[Adobe PageMaker](../Page/Adobe_PageMaker.md "wikilink") などが存在した。

RTは[X Window Systemの開発にも重要な役割を果たしている](../Page/X_Window_System.md "wikilink")。[ブラウン大学](../Page/ブラウン大学.md "wikilink")のグループが X バージョン 9 を RT に移植した際に、整列されていないデータが RT 上で障害を引き起こし、それが引き金となってバージョン 10 でプロトコル非互換を伴うバージョンアップをすることになったのである（[1985年](https://ja.wikipedia.org/wiki/1985年 "wikilink"))。

## 市場での状況

IBM RTは当初の発表からは、かなりの変化を経験した。多くの業界関係者にはRTはパワーが足りず、価格が高く、性能が悪いと言われ、多くの人がRTを [IBM PC](../Page/IBM_PC.md "wikilink") の一機種であると思っていた。この混乱はその最初の名前("IBM RT PC")にある。当初、人々は(IBM自身も)これが[ハイエンド](https://ja.wikipedia.org/wiki/ハイエンド "wikilink")のパーソナルコンピュータだと考えていたように思われる。そのためIBMのマシンとしては驚くほどサポートが無かった。IBM のセールスマンが受け取る歩合は PC とほとんど同じであった。典型的な構成で 2万ドルであって、販売は容易ではない。従って、販売部門は RT の販促に消極的であった。

RTシステムの控えめな性能と同じ年に発表された他社のワークステーションを比較して、業界関係者はIBMの方向性に疑問を抱いた。RT 向けの [AIX](https://ja.wikipedia.org/wiki/AIX "wikilink") は IBM にとって初めての [UNIX](../Page/UNIX.md "wikilink") への進出であった。ソフトウェアパッケージが無く、IBM自身もあまりAIXのサポートに熱心でなく、伝統的な UNIX の業界標準では見られない改造がいくつか施してあったため、ソフトウェアベンダーもRTとAIXのサポートにはあまり乗り気ではなかった。RTは [CAD](../Page/CAD.md "wikilink")/[CAM](../Page/CAM.md "wikilink")や[CATIA](../Page/CATIA.md "wikilink")の市場に活路を見出し、科学技術計算や教育分野にも若干進出できた。AOS と教育機関向けの割引を発表してからは特にその傾向がある。Pick OS を搭載したRTは、小売店舗の制御システムやIBMのメインフレームとPOS端末の中継などでもある程度売れた。

RT の総出荷台数は約23000台で、うち4000台はIBM社内で使われた。Pick OS を搭載して出荷されたのは約4000台であった。

## イースター・エッグ

これらのシステムには[イースター・エッグが存在した](../Page/イースター・エッグ_\(コンピュータ\).md "wikilink")。デバッガでCPUのレジスタを見たとき、全ての初期化されていないレジスタの内容は[16進の](https://ja.wikipedia.org/wiki/十六進記数法 "wikilink")[マジックナンバー](../Page/マジックナンバー_\(プログラム\).md "wikilink") `0xdeadbeef` と表示される。

## 外部リンク

  - [IBM RT PC-page](http://www.damage.fi/slas/rt/rt.html)
  - [The IBM RT Information Page](http://www-2.cs.cmu.edu/afs/andrew.cmu.edu/usr/shadow/www/ibmrt.html)
  - [comp.sys.ibm.pc.rt FAQ (as of 1994), archived at Giessen University](http://www.uni-giessen.de/faq/archiv/ibm-rt-faq.aix-v2.part1-4/)

*この文書は[RT/PC FAQ](http://www.damage.fi/slas/rt/faq/)から英語版Wikipediaに掲載されたものを翻訳したものです。*

[Category:IBMのワークステーション](https://ja.wikipedia.org/wiki/Category:IBMのワークステーション "wikilink") [Category:コンピュータ史](https://ja.wikipedia.org/wiki/Category:コンピュータ史 "wikilink") [Category:コンピュータ_(歴代)](https://ja.wikipedia.org/wiki/Category:コンピュータ_\(歴代\) "wikilink")
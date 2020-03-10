> この記事は[DESQview](https://ja.wikipedia.org/wiki/DESQview)から翻訳されています。


**DESQview** は、Quarterdeck Office Systems が開発・販売した[DOSエクステンダ](https://ja.wikipedia.org/wiki/DOSエクステンダ "wikilink")の1種であり、[1980年代](../Page/1980年代.md "wikilink")後半から[1990年代](../Page/1990年代.md "wikilink")初期にそれなりの人気を得た。DESQview は[MS-DOS](../Page/MS-DOS.md "wikilink")などの[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink")上で動作する[マルチタスク](../Page/マルチタスク.md "wikilink")環境（テキストのみ）であり、複数のDOS用プログラムをそれぞれ[ウィンドウ](../Page/ウィンドウ.md "wikilink")に表示し、並行動作させることができる。

## DESQ

DESQview 以前の Quarterdeck の製品として、DESQ と呼ばれる[タスク切り替え製品があった](https://ja.wikipedia.org/wiki/コンテキストスイッチ "wikilink")。これは、複数のプログラムをユーザーが切り替えながら実行できるものであった。この種の製品としては Software Carousel と呼ばれる限定的なウィンドウ機能を持った製品が人気で、DESQ はそれほど売れなかった。Quaterdeck は、マルチタスク機能を搭載し、[IBM TopView](https://ja.wikipedia.org/wiki/IBM_TopView "wikilink") との互換性を持たせ、これを DESQview と改名した。

## DESQview

DESQview は[1985年](https://ja.wikipedia.org/wiki/1985年 "wikilink")7月にリリースされた。これは[マイクロソフト](../Page/マイクロソフト.md "wikilink")が [Windows](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink") の最初のバージョンを発売する4か月前であった。MS-DOS にマルチタスク機能とウィンドウ機能をもたらす最初の製品として受け止められたが、実際にはそれ以前の[1984年](../Page/1984年.md "wikilink")に [IBM TopView](https://ja.wikipedia.org/wiki/IBM_TopView "wikilink") が登場しており、DESQview は TopView のポップアップメニューを踏襲した。

DESQview では、行儀のよいDOSプログラムが、サイズ変更可能でオーバーラップ可能なウィンドウ内で並行動作した。単純なメニューにより、プログラム間の[コピー・アンド・ペースト](../Page/コピー・アンド・ペースト.md "wikilink")が可能である。DESQview には編集可能な単純なマクロも備えていた。Quarterdeck は、ノートパッドやダイヤラーなどの DESQview 向けのユーティリティも開発した。その後のバージョンでは、グラフィックモードのプログラムも動作可能となったが、その場合はフルスクリーンモードで動作した。

DESQview は、完全な[GUI](https://ja.wikipedia.org/wiki/グラフィカルユーザインタフェース "wikilink")[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink")ではなく、DOS上で[リアルモード](https://ja.wikipedia.org/wiki/リアルモード "wikilink")で動作する擬似GUIシェルであった。[Intel 80286](../Page/Intel_80286.md "wikilink") を使った[PC/AT互換機](https://ja.wikipedia.org/wiki/PC/AT互換機 "wikilink")（2MBメモリ）でも動作できるが、[Intel 80386](../Page/Intel_80386.md "wikilink") マシンの方が DOS の 640KB メモリ制限に対してうまく機能した。しかし、どちらにしても[プロテクトモード](https://ja.wikipedia.org/wiki/プロテクトモード "wikilink")ではなくリアルモードで動作するので、プログラムにバグがあるとシステム全体がクラッシュすることとなった。

## DESQview と QEMM

DESQview などのリアルモードのプログラムが 80386 上で 640KB を超えるアドレスにあるメモリにアクセスするには、工夫が必要だった（[XMS](https://ja.wikipedia.org/wiki/XMS "wikilink")、[EMS](https://ja.wikipedia.org/wiki/Expanded_Memory_Specification "wikilink")、[UMA](https://ja.wikipedia.org/wiki/Upper_Memory_Area "wikilink") を参照）。Quarterdeck はそのためのメモリ管理プログラムを開発した。マーケティング担当のマネージャは将来を見通し、それを別製品 **[QEMM](https://ja.wikipedia.org/wiki/QEMM "wikilink")-386** として発売した。これは DESQview よりも人気となり、かなりの売り上げをもたらした（[1987年](https://ja.wikipedia.org/wiki/1987年 "wikilink")から[1994年](../Page/1994年.md "wikilink")まで、毎年1億5000万ドル以上の売り上げ）。[Pentium](https://ja.wikipedia.org/wiki/Pentium "wikilink")がリリースされると、単に **QEMM** と称するようになった。DESQview と QEMM-386 を同梱した製品は DESQview 386 と呼ばれた。

80386の登場により、メモリ管理機能が強化され、プロテクトモードへの移行が進んだが、[仮想86モード](https://ja.wikipedia.org/wiki/仮想86モード "wikilink")によって MS-DOS などのリアルモードのプログラムを拡張メモリにマッピングすることも可能となった。これにより、LIM（[ロータス](../Page/ロータス_\(ソフトウェア\).md "wikilink")、[インテル](https://ja.wikipedia.org/wiki/インテル "wikilink")、[マイクロソフト](../Page/マイクロソフト.md "wikilink")） [EMS](https://ja.wikipedia.org/wiki/Expanded_Memory_Specification "wikilink") も実装された。

DESQview は QEMM を使って LIM EMS の API では不可能なこともでき、コンベンショナルメモリ（640KBまでのメモリ）の大部分を複数の拡張メモリブロックにマッピングし、それぞれが透過的に実行できるようにした。DOS の最初のコピーやネットワークドライバなどは DESQview の前にロードされていなければならない。QEMM と DESQview を組み合わせると、多数のプログラムを同時に実行可能であった。例えば、8MB のシステムでは約12本のフルサイズの MS-DOS プログラムが並行して動作でき、16MB のシステムでは20以上が動作できた。

## DESQview の利用

DESQview は DOS 互換プログラムのほとんどをそれなりの性能と安定性で動作させることができた。また、インタフェースは学習が容易で簡単に使うことができた。

一般的なパーソナルコンピュータのキーボードには、コントロールキー、Altキー、シフトキーが備わっている。これらのキーは他のキーと同時に押下されることで意味を持つ。DESQview はデフォルトでは Alt キーが単独で押下されるのを監視している。Alt キーだけを押下すると、DESQview のメニューが表示され、プログラムの機能にアクセスしたり、新たなタスクを実行させたり、タスク間の切り替えをしたり、画面上のテキストに印を付け、そのテキストを現在のタスクへの入力としてペーストしたり、テキストウィンドウのサイズ変更や移動をしたりといった様々な機能を利用可能である。シフトと Alt を同時に押下すると、DESQview は一連のキー押下をマクロとして学習する。これにより、DESQview は個々のプログラムが使っている[キーバインディング](https://ja.wikipedia.org/wiki/キーバインディング "wikilink")に影響を与えることなく、他のプログラムを実行できる。

DESQview は一部で人気となったが、Quarterdeck の努力にも関わらず、大人気とはならなかった。[ビル・ゲイツ](../Page/ビル・ゲイツ.md "wikilink")を含めたマイクロソフトの人々は、DESQview や他の初期のGUI環境である [VisiOn](../Page/VisiOn.md "wikilink")、[GEM](https://ja.wikipedia.org/wiki/Graphical_Environment_Manager "wikilink") に多大な関心を寄せていたと言われている。

DESQview がその後も長く使われた用途として、マルチユーザ型[電子掲示板](https://ja.wikipedia.org/wiki/電子掲示板 "wikilink") (BBS) がある。ハードウェアが最新でなくても安定したマルチタスクが可能で、複数の通信ポートの扱いが容易だったためである。当時のフリーあるいは低価格の BBS ソフトウェアは、シングルノードで動作するシングルタスクのDOSプログラムであった。通常、そのようなBBSソフトウェアは1度に1つしか動作できないが、DESQview を使えば同時に複数のプログラムを実行可能であり、最新のハードウェアでなくともマルチユーザ型のBBSを構築できたのである。

## DESQview の衰退

DESQview は[GUIではない](https://ja.wikipedia.org/wiki/グラフィカルユーザインタフェース "wikilink")。Quarterdeck はその機能を使うためのソフトウェア開発用のライブラリとユーティリティを提供したが、これは広く使われることはなかった。DESQview の真骨頂は修正なしで既存のプログラムを同時に実行できる点であり、開発ツールのコストの問題もあって、ソフトウェア業者にとっては DESQview 専用の製品を開発するのは有利な選択肢ではなかった。

マイクロソフトは、メモリ管理機能とマルチタスク機能が強化された [Windows 3.0](../Page/Microsoft_Windows_3.x.md "wikilink") をリリースした。DESQview の方が高速で小さく、安定していたが、Windows の方が安価でグラフィック機能をサポートしていた。マイクロソフトは [ISV](https://ja.wikipedia.org/wiki/ISV "wikilink") に圧力をかけて Windows の GUI を使ったソフトウェアを製品化させ、ハードウェア販売業者には Windows を同梱させた。このため、ISV は Windows 上のアプリケーションを開発せざるを得なくなった。このようなマイクロソフトの圧力は、アメリカでの[反トラスト法](https://ja.wikipedia.org/wiki/反トラスト法 "wikilink")違反の訴訟へと発展した。その裁判の過程で、マイクロソフトがハードウェア販売業者からライセンス料としてPCが1台売れる毎に料金を徴収していたことが判明している（そのPCにマイクロソフトのOSがインストールされているか否かは問わない）。

QEMM の衰退は、[1990年](https://ja.wikipedia.org/wiki/1990年 "wikilink")にリリースされた[デジタルリサーチ](../Page/デジタルリサーチ.md "wikilink")の [DR-DOS](https://ja.wikipedia.org/wiki/DR-DOS "wikilink") 5.0 にメモリ管理機能が同梱されたことに始まった。これに追随するため、マイクロソフトは [MS-DOS](../Page/MS-DOS.md "wikilink") 5.0 に [EMM386](https://ja.wikipedia.org/wiki/EMM386 "wikilink") を含めた（EMM386 は、従来、Windows にのみ含まれていたメモリ管理機能）。QEMM は徐々に売れなくなっていった。[1994年](../Page/1994年.md "wikilink")8月、3四半期連続で赤字を計上した後、Quarterdeck は従業員の25%を解雇し、CEO である Terry Myers も退職した。

DESQview から他のプラットフォーム（Windows 3.x や OS/2）へユーザが流れると、サードパーティが DESQview API をエミュレートするプログラムを開発している（Windows 向けとしては TAKE、OS/2 向けとしては OS/2SPEED などがある）。

### DESQview/X

Quarterdeck は、MS-DOS と DESQview 上で動作する [X Window System](../Page/X_Window_System.md "wikilink") の Xサーバ **DESQview/X** をリリースし、同時に X のソフトウェアを移植できるようなGUIを提供した。しかし、当時既に多数の Windows アプリケーションがあり、Windows に移植されていないアプリケーションと言えば、非商用のフリーなものか、非常に高価なものだけだった。また、当時のパーソナルコンピュータは、[UNIX](../Page/UNIX.md "wikilink")[ワークステーション](../Page/ワークステーション.md "wikilink")に比べると非力だった。[Linux](https://ja.wikipedia.org/wiki/Linux "wikilink")もそのころ既に X をサポートしていて、パーソナルコンピュータ上で動作可能となっていた。つまり、DESQview/X には市場は残されていなかったのである。

DESQview/X には3種類のウィンドウマネージャが用意されていた。[Motif](../Page/Motif_\(GUI\).md "wikilink")、[OPEN LOOK](https://ja.wikipedia.org/wiki/OPEN_LOOK "wikilink")、[twm](https://ja.wikipedia.org/wiki/twm "wikilink") である。このうち、twm がデフォルトで、他はオプション製品だった。[NCSA Mosaic](../Page/NCSA_Mosaic.md "wikilink") は DESQview/X に移植された数少ないアプリケーションの1つである。

DESQview/X には、[MS-DOS](../Page/MS-DOS.md "wikilink") や Windows 3.0 のプログラムをネットワーク経由で X プログラムとして実行する機能があった。これにより、パーソナルコンピュータのプログラムを UNIX ワークステーションから実行することが可能となっている。

### その後の DESQview

DESQview 本体の開発も DESQview/X と並行して行われていた。DESQview/X の開発が中止されると、新たな DESQview がリリースされた。QEMM は DESQview が無くなった後も開発され続け、[Windows 98](../Page/Microsoft_Windows_98.md "wikilink") 互換の QEMM がリリースされた。

1990年代中盤、Quarterdeck は[インターネット](https://ja.wikipedia.org/wiki/インターネット "wikilink")企業として再生しようと、Mosaic をリリースしたこともある。最終的に同社は[シマンテック](https://ja.wikipedia.org/wiki/シマンテック "wikilink")に買収された。

## 無料リリース

DESQview はサポートしないという条件付きで[インターネット](https://ja.wikipedia.org/wiki/インターネット "wikilink")上でダウンロード可能となっている。ただし、[シマンテック](https://ja.wikipedia.org/wiki/シマンテック "wikilink")もサイトを運営している CharterSoft もその著作権の状態を明らかにしなかった。

Quarterdeck のライセンス条件は期限付きの特殊なもので、20年または30年間の製品使用を許諾したものであった。

DESQview が「パブリックドメイン」であるという主張には根拠がなく、単に2002年の[こちらの記事](http://slashdot.org/articles/02/01/27/1950244.shtml)での編集者の判断だけによるものと思われる。2001年8月21日の[ネットニュースへの投稿](http://groups.google.com/group/alt.games.wing-commander/browse_thread/thread/c9c20b2cb04ed4ed/3e9278c40a5c8f39?lnk=st&q=DESQview+public+domain&rnum=52&hl=en#3e9278c40a5c8f39)は、DESQview がシマンテックの知的財産であるという考え方を補強するものだが、同社はそれについて明確には述べていない。

## 関連項目

  - [GEM](https://ja.wikipedia.org/wiki/Graphical_Environment_Manager "wikilink")
  - [ViewMAX](https://ja.wikipedia.org/wiki/ViewMAX "wikilink")
  - [GEOS](../Page/GEOS_\(オペレーティングシステム\).md "wikilink")
  - [Windows 1.0](https://ja.wikipedia.org/wiki/Microsoft_Windows_1.0 "wikilink")
  - [VisiOn](../Page/VisiOn.md "wikilink")

## 外部リンク

  - [DESQview download](http://www.chsoft.com/dv.html)
  - [Slashdot article of public domain release of DESQview](http://slashdot.org/articles/02/01/27/1950244.shtml)
  - [DESQview FAQ](http://www.uni-giessen.de/faq/archiv/desqview-faq/msg00000.html)
  - [Screen snapshots of DESQview/X](http://toastytech.com/guis/dvx.html)

[Category:Xディスプレイマネージャ](https://ja.wikipedia.org/wiki/Category:Xディスプレイマネージャ "wikilink") [Category:MS-DOS](https://ja.wikipedia.org/wiki/Category:MS-DOS "wikilink") [Category:システムソフトウェア](https://ja.wikipedia.org/wiki/Category:システムソフトウェア "wikilink")
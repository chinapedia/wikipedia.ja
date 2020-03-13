> この記事は[Expanded Memory Specification](https://ja.wikipedia.org/wiki/Expanded_Memory_Specification)から翻訳されています。


**Expanded Memory Specification** (**EMS**) は、[MS-DOS](../Page/MS-DOS.md "wikilink")上でのメモリ拡張手法。[ロータス](../Page/ロータス_\(ソフトウェア\).md "wikilink")、[インテル](https://ja.wikipedia.org/wiki/インテル "wikilink")、[マイクロソフト](../Page/マイクロソフト.md "wikilink")の3社が提唱したことから、その頭文字を付けて**LIM-EMS**とも呼ばれる。

## 概要

初期のMS-DOSは[Intel 8086向けに作られていたことから](../Page/Intel_8086.md "wikilink")、8086が扱える最大のメモリ空間である1MB以上を扱うことが考慮されていなかった。8086が登場した当初は8ビットプロセッサの最大64KBの空間に比べると余裕があるように見えたが、[ROMや](https://ja.wikipedia.org/wiki/Read_Only_Memory "wikilink")[VRAM](../Page/VRAM.md "wikilink")の為に消費される空間を除いたメインメモリ空間は640KBまたは768KBに制限され、アプリケーションの規模が拡大し、また扱うデータが増大すると1MBでも不足するようになった。

やがて1MBを越えるメモリを扱える上位互換品である[80286や](../Page/Intel_80286.md "wikilink")[80386が登場し](../Page/Intel_80386.md "wikilink")、メモリモジュールが安価に手に入る時代に入ったが、[リアルモード](../Page/リアルモード.md "wikilink")でどうやって使うかが問題になった。プロセッサを[プロテクトモード](../Page/プロテクトモード.md "wikilink")で動作させれば1MBを越えるメモリを扱えたが、当時のMS-DOSおよびそのアプリケーションは、多くの場合リアルモードで動作していた為である。

この壁を乗り越えるハード的な実装は幾つかあったが、代表的なのは後に統一規格として制定された[バンク切り換え](../Page/バンク切り換え.md "wikilink")によるメモリ拡張方式**EMS**である。EMSを使用するソフトではデータを16KB～64KBの窓を通してアクセスする為、データの分解・再結合をしなければならず、またEMSを通常メモリのように透過的に扱う[ライブラリ](../Page/ライブラリ.md "wikilink")も無かった事から、やや煩雑なプログラミングをする必要があった。（コード領域をEMSに展開し、コンベンショナルメモリの負担を軽減するコンパイラはあった）。 80386からは仮想86モードを使ったソフトウエア的なEMSの実装が一般的となった。

## 基本概念

  - "EMSマネージャ"を通じてメモリ空間の取得・開放、[バンク切り換え](../Page/バンク切り換え.md "wikilink")等を行う。
  - 16KBytes単位でバンク切替を行い、これをページと呼ぶ。
  - 8086でアクセス可能な1Mbytesの範囲内に"ページフレーム"区画を設ける。
  - ページフレームは、ほとんどの場合4ページ = 64Kバイト(バージョン4.0)の連続した領域。
  - EMSマネージャは、要求のあったページをページフレームに出現させる。
  - そのため、各種操作は隠蔽され、ユーザは気にする必要が無い。
  - 対応するメモリ総量は32Mバイト(2048ページ)まで。
  - 主な版として3.2, Enhanced EMS 3.2, 4.0がある。4.0では特にWindows 2.x向けの拡張を行った。

[CPU](../Page/CPU.md "wikilink")や[メモリ](../Page/記憶装置.md "wikilink")[バスの変遷に伴い](../Page/バス_\(コンピュータ\).md "wikilink")、いくつかの実装方式があった。

## 実現方法

[サムネイル用](https://ja.wikipedia.org/wiki/ファイル:Buffalo_EMJ-4000_EMS_RAM_board.jpg "wikilink")）\]\]

### ハードウェアEMS

バンク切替機能を持つ、専用メモリカードを拡張バスに接続する。バンク切替等の操作は、ハードウェア的に行われるので高速。また、[8086](https://ja.wikipedia.org/wiki/8086 "wikilink")・[80186](https://ja.wikipedia.org/wiki/80186 "wikilink")・[V30](https://ja.wikipedia.org/wiki/V30 "wikilink")といった、アドレスバスが20bitのCPUでもEMSを使用できる。純粋なハードウェアEMSを80286以降搭載のコンピュータに増設しても、プロテクトメモリとしては使用できず、どちらも使用したい場合は"二重投資"となる。そのため、カード上のスイッチ切り替えにより、"拡張バス接続のプロテクトメモリ"としても使用できるEMSカードも存在した。

### ソフトウェアEMS

[80286](https://ja.wikipedia.org/wiki/80286 "wikilink")以降のCPUで使用可能。[プロテクトメモリ](https://ja.wikipedia.org/wiki/プロテクトメモリ "wikilink")を用いてEMSの[エミュレーション](https://ja.wikipedia.org/wiki/エミュレーション "wikilink")を行う。EMSマネージャは、バンク切替指令を受けると、プロテクトメモリからページフレームにページをコピー/書き戻しする。このオーバーヘッドのため低速である。EMSマネージャを組み込まない場合は、プロテクトメモリはそのまま使用できるので、汎用性がある。

一般的にソフトウェアエミュレーション方式のEMS（ソフトウェアEMS）といえばプロテクトメモリを使ったものを指すことが多いが、その他のエミュレーション方式についても便宜上併記する。

[PC-9800シリーズ](../Page/PC-9800シリーズ.md "wikilink")用の一部のEMSマネージャは、プロテクトメモリの代わりに[I・Oバンクメモリを利用できた](https://ja.wikipedia.org/wiki/%E3%83%90%E3%83%B3%E3%82%AF%E5%88%87%E3%82%8A%E6%8F%9B%E3%81%88#PC-9801.E3.81.AB.E3.81.8A.E3.81.91.E3.82.8B.E3.83.90.E3.83.B3.E3.82.AF.E3.83.A1.E3.83.A2.E3.83.AA "wikilink")(ページフレームのアドレスはハードウェアEMSの有無により異なる)。バンクメモリを利用する場合は8086/V30でも使用できる。

また、プロテクトメモリの代わりに補助記憶装置上のファイルを用いるドライバもある。メモリの代わりにファイルにアクセスするため、さらに低速であるが、ドライバによっては8086/8088などでも使用できる。[HP200LX](../Page/HP200LX.md "wikilink")(CPUは[80C186](../Page/Intel_80186.md "wikilink"))では、この方法によりEMSが使用できる。ページフレームをメインメモリ空間に確保し、補助記憶装置に充分な空き領域があれば、追加ハードウェアは不要である。

  - LXEMM (HP200LX用) など

### 仮想86EMS

[80386](https://ja.wikipedia.org/wiki/80386 "wikilink")以降のCPUで使用可能。[IA-32](../Page/IA-32.md "wikilink")の[仮想86モード](../Page/仮想86モード.md "wikilink")を用いてEMSを実現する。EMSマネージャは、CPUのメモリマッピング機構を用いて、（プログラムから見て）ページフレームにプロテクトメモリ上のページを出現させる。ソフトウェアEMS同様の汎用性があり、ページ切替も高速。また、汎用拡張バスではなくメモリ専用バス上のメモリを使用可能なために最も高速である。ただし、仮想86モードはプロテクトモードの1タスクである（独立した動作モードではない点に注意）ため、プロテクトモードを使用した際に発生するのと同等の処理速度の低下がある。特に割り込みとI/Oポートへのアクセスでこの速度の低下が顕著となる。

MS-DOS用ソフトウェアの互換性のために、[Windows 9x系まではMS](../Page/Windows_9x系.md "wikilink")-DOSモード用に[EMM386](../Page/EMM386.md "wikilink")が用意されていた。また仮想86モードに対応したWindowsの[DOSプロンプト](../Page/DOSプロンプト.md "wikilink")では、Windowsの機能により仮想EMSが提供される。特にMS-DOSモードを持たない[Windows NT系ではDOSプロンプト上で動作するアプリケーションに限られるが](../Page/Windows_NT系.md "wikilink")、その後のWindowsにおいてもEMSの設定項目が存在する。

## 設定上の注意

メインメモリ([コンベンショナルメモリ](https://ja.wikipedia.org/wiki/コンベンショナルメモリ "wikilink"))を圧迫せずにEMSを使用するためには、その範囲外となる空間にページフレームを設定する必要がある。しかし、この空間 ([Upper Memory Area](https://ja.wikipedia.org/wiki/Upper_Memory_Area "wikilink")) はBIOS・拡張カードBIOS・[VRAM](../Page/VRAM.md "wikilink")が使用する空間である。

そのため、EMSを使用する際には、拡張カードBIOSを

  - 本体BIOS・VRAM・他のカードのBIOSと衝突しないように
  - かつ、64KBytesの連続未使用領域が生じるように

設定し、そこをページフレームとしなければならない。

## ラージフレーム

[PC/AT互換機](https://ja.wikipedia.org/wiki/PC/AT互換機 "wikilink")におけるEMSの実装方法として、640KB以降のアッパーメモリにページフレームを設けるだけでなく、コンベンショナルメモリの上位アドレス(256KB:40000H以降など)にもページフレームを設けるラージフレーム方式がある(実装に仮想メモリマネージャを使うことが多かった)。特にWindows 2.0, Windows/286, Windows 3.0リアルモードではこの方法を使って、コンベンショナルメモリに常駐するDLLを切り替えることが可能で、この点において国産の[PC-9801などに比べて快適なOS環境を実装していた](../Page/PC-9800シリーズ.md "wikilink")(日本IBMで発売していたWindows 3.0Aのリアルモードでもこの機能は利用可能である)。

しかしながら下記に示すような欠点があったために[Windows 3.0以降は](../Page/Microsoft_Windows_3.x.md "wikilink")、次第に拡張メモリの標準を[プロテクトメモリ](https://ja.wikipedia.org/wiki/プロテクトメモリ "wikilink")に移行していくことになる。

## EMSの欠点

  - [アドレス空間](../Page/アドレス空間.md "wikilink")そのものを拡張する訳ではないので、同時に参照可能なアドレス空間の大きさは1Mバイトのままである。
  - そのためプログラマはページフレームに出現しているページを常に把握してプログラムを開発する必要がある(メモリ管理に手間がかかる)。
  - 仕様として[マルチタスク](../Page/マルチタスク.md "wikilink")処理に必要なシステム保護機能（タスク毎に読み出し専用属性やコード実行専用属性つける等）が無かったため、マルチタスクおよび擬似マルチタスクOSの基本メモリ仕様としては不向きだった。
  - DOS上で1Mバイトを超えるメモリを使用する方法としては[DOSエクステンダ](../Page/DOSエクステンダ.md "wikilink")等より低速である。(DOSエクステンダは[バンク切り換え](../Page/バンク切り換え.md "wikilink")処理が不要である)
  - 仮想86EMSは、他の[プロテクトモード](../Page/プロテクトモード.md "wikilink")プログラムと共存するためには[VCPI](../Page/VCPI.md "wikilink")等の規格に対応する必要がある。

## 参考文献

  - 『MS-DOSメモリ管理ソフト技法-メモリ常駐ソフト&拡張メモリ活用プログラミング』（CQ出版、1990年）, ISBN 978-4-7898-3484-1
  - 「インターフェース 1990年9月号」（CQ出版）
  - 「インターフェース 1993年10月号」（CQ出版）
  - [Duncan, Ray](https://ja.wikipedia.org/wiki/Duncan,_Ray "wikilink") (1992). *Extending-DOS*:A Programmer's Guide to Protected-Mode DOS (Addison-Wesley), ISBN 0-201-56798-9

## 関連項目

  - [MS-DOS](../Page/MS-DOS.md "wikilink")
  - [Microsoft Windows](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")
  - [DOSエクステンダ](../Page/DOSエクステンダ.md "wikilink")
  - [DPMI](../Page/DPMI.md "wikilink") (DOS Protected Mode Interface)
  - [VCPI](../Page/VCPI.md "wikilink") (Virtual Control Program Interface)
  - [XMS](../Page/XMS.md "wikilink") (Extended Memory Specification)
  - [バンク切り換え](../Page/バンク切り換え.md "wikilink")

[Category:メモリ管理](https://ja.wikipedia.org/wiki/Category:メモリ管理 "wikilink") [Category:MS-DOS](https://ja.wikipedia.org/wiki/Category:MS-DOS "wikilink")
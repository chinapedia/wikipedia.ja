> この記事は[Windows Printing System](https://ja.wikipedia.org/wiki/Windows_Printing_System)から翻訳されています。


**Windows Printing System**（ウィンドウズ プリンティング システム）は、[マイクロソフト](../Page/マイクロソフト.md "wikilink")が提唱していた[プリンター](https://ja.wikipedia.org/wiki/プリンター "wikilink")の規格、およびそれを構成する一連のソフトウェア（[デバイスドライバ](../Page/デバイスドライバ.md "wikilink")）である。**WPS**と略される。ページプリンター（[レーザープリンター](https://ja.wikipedia.org/wiki/レーザープリンター "wikilink")）の低価格化と、[コンピュータ](../Page/コンピュータ.md "wikilink")側での印刷状況の把握を目的として開発された規格である。

通常のページプリンターは、文字や画像のデータを印刷データとして処理するための[CPU](../Page/CPU.md "wikilink")と[メモリ](../Page/記憶装置.md "wikilink")、[フォント](../Page/フォント.md "wikilink")データ（プリンターフォント）などをプリンターに搭載しているが、WPS規格のプリンターでは、コンピュータ側のCPUとメモリ、フォントを利用して[Windows上のプリンタドライバがこれらの処理を行うため](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")、プリンター側に高速なCPUや大容量のメモリを搭載する必要がなくなる。コンピュータからの単純な命令を逐一処理できるだけの機能を搭載すればよいため、プリンターを低価格で製造することができる。印刷データの展開にWindowsの描画システムである[GDIを使用するため](https://ja.wikipedia.org/wiki/Graphics_Device_Interface "wikilink")、**GDIプリンター**とも呼ばれる。

折りしも[Windows 3.1の普及期であり](../Page/Microsoft_Windows_3.x.md "wikilink")、画面で見たままのフォントで印刷できる[WYSIWYG](../Page/WYSIWYG.md "wikilink")の実現が話題となっていた時期でもあったことから、WYSIWIGの実現に役立たないプリンターフォントの搭載が不要になることには一定の合理性があった。

コンピュータ側で印刷データの展開を行うことから、コンピュータとプリンターの間のデータ転送量が爆発的に増加するため、これに対応する[IEEE 1284規格の高速な転送モードに対応したプリンターインタフェースの使用が推奨されている](https://ja.wikipedia.org/wiki/IEEE_1284 "wikilink")。コンピュータ側の[インタフェースが双方向通信機能に対応していれば](../Page/インタフェース_\(情報技術\).md "wikilink")、プリンターの状態（n枚目を印刷中、印刷完了、紙詰まり、トナー切れなど）を、画面上にポップアップ表示されるステータスウィンドウや音声メッセージなどで把握することも可能である。

しかしWPS対応プリンターについてはWindows以外の[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink") (OS) には対応していないこと、Windowsであっても[Windows XPなど後継バージョンのOS用ドライバをプリンターメーカーが開発しなくなったこと](../Page/Microsoft_Windows_XP.md "wikilink")、マイクロソフトとメーカーの間に締結された契約条項が原因で、最新版のドライバを[インターネット](../Page/インターネット.md "wikilink")から[ダウンロード](https://ja.wikipedia.org/wiki/ダウンロード "wikilink")することはできず、最新版ドライバの入手にはメーカーからのメディア送付しか手段がないことなどから利用者に不評であり、WPS対応プリンターの発売から10年以上が経過した現在、実際の利用現場からも急速に姿を消しつつある。

なお、WPSが実現していた状況把握機能については、現在では各社独自の規格によってプリンターからデータを取得することで実現されている。また、[USBや](../Page/ユニバーサル・シリアル・バス.md "wikilink")[LANなどのさらに高速なインタフェースが搭載されるようになり](../Page/Local_Area_Network.md "wikilink")、メモリ単価も大幅に低下していることから、印刷処理のどの程度をプリンターに行わせ、どの程度をコンピュータ側で行うかについては各メーカーの判断により決定されている。

[en:Graphics Device Interface\#GDI_printers](https://ja.wikipedia.org/wiki/en:Graphics_Device_Interface#GDI_printers "wikilink")

[Category:Microsoft_Windows](https://ja.wikipedia.org/wiki/Category:Microsoft_Windows "wikilink")
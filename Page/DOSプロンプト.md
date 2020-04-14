> この記事は[DOSプロンプト](https://ja.wikipedia.org/wiki/DOSプロンプト)から翻訳されています。


**DOSプロンプト** とは、[NT系以前の](../Page/Windows_NT系.md "wikilink")[Windowsにおいて](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")、[MS-DOS](../Page/MS-DOS.md "wikilink")互換環境（いわゆる「DOS窓」）を起動するアプリケーションである。

## 概要

DOSプロンプトを起動するとMS-DOSの標準[シェル](../Page/シェル.md "wikilink")である[コマンドラインインタプリタ](../Page/コマンドラインインタプリタ.md "wikilink")の[COMMAND.COM](../Page/COMMAND.COM.md "wikilink")のプロンプトが表示される。（コマンド）プロンプトとは「C:\\\>」のような記号のことである。

NT系以前のWindows 9xはMS-DOSから起動するもののWindows 9x自身がOSとなってマルチタスクGUI環境を実現している。32bit OSであるWindows 9xで16bitのMS-DOSアプリケーションを直接動作させるのは不可能なためCPUのもつ仮想86モードを利用してDOSプロンプト毎に独立した[仮想DOSマシン](../Page/仮想DOSマシン.md "wikilink")環境を作成することで実現している。しかしながらゲームなどのハードウェアを専有し直接操作していたMS-DOSアプリケーションをWindows環境で他のアプリケーションと協調させて動作させるのは困難で、互換性と速度のために一部Windowsの制御をバイパスさせていたために不安定の要因となっていた。またDOSプロンプトとは別にMS-DOSモードを持っており、これはWindows上で実行DOSプロンプトとは異なり、Windowsを停止させてMS-DOS環境に移行させることで高い互換性を実現している。

## NT系Windows

[NT系 Windowsは](../Page/Windows_NT系.md "wikilink")、NTカーネルというカーネルが中心にあり、その上に互換性の高いMS-DOS互換環境があるため、前述のDOS窓のような環境とは全く異なるものとなっている。[COMMAND.COM](../Page/COMMAND.COM.md "wikilink") など、MS-DOSのコマンド類のいくつかは、おそらく互換性のために残されている。

NT系 Windowsには [cmd.exe](https://ja.wikipedia.org/wiki/cmd.exe "wikilink") という[プログラムもあり](../Page/プログラム_\(コンピュータ\).md "wikilink")、こちらはWinNTネイティブアプリである（アイコンには「[コマンドプロンプト](../Page/コマンドプロンプト.md "wikilink")」とキャプションが付けられている）。cmd.exe は[端末ウィンドウ兼](../Page/端末エミュレータ.md "wikilink")[コマンドライン](../Page/コマンドラインインタプリタ.md "wikilink")[シェル](../Page/シェル.md "wikilink")であり、見た目こそ COMMAND.COM に似てはいるが、多くの拡張がされているなど基本的に別物である。

## OS/2

[OS/2](https://ja.wikipedia.org/wiki/OS/2 "wikilink") 1.xの「DOS互換ボックス」では、1.0では全画面表示のみ、1.1以降では全画面表示またはOS/2プレゼンテーションマネージャー(PM)上のウィンドウ表示を選ぶことができたが、「DOSプロンプト」と同様のものがあった。

OS/2 2.0以降の「MVDM(Multi Virtual DOS Machine)」では、全画面表示またはOS/2ワークプレースシェル(WPS)上のウィンドウ表示で、「DOSプロンプト」と同様のものがあった。

OS/2 1.0からある「OS/2コマンドプロンプト」は、[cmd.exe](https://ja.wikipedia.org/wiki/cmd.exe "wikilink") 同様の、[端末ウィンドウ兼](../Page/端末エミュレータ.md "wikilink")[コマンドライン](../Page/コマンドラインインタプリタ.md "wikilink")[シェル](../Page/シェル.md "wikilink")である。

## 注

<references/>

[Category:MS-DOS・Windows3.x・9x系](https://ja.wikipedia.org/wiki/Category:MS-DOS・Windows3.x・9x系 "wikilink") [Category:OS/2](https://ja.wikipedia.org/wiki/Category:OS/2 "wikilink") [Category:コンピュータのユーザインタフェース](https://ja.wikipedia.org/wiki/Category:コンピュータのユーザインタフェース "wikilink")
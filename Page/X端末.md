> この記事は[X端末](https://ja.wikipedia.org/wiki/X端末)から翻訳されています。


|                                                                                                                                                                                                     |
| --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [Network_Computing_Devices_NCD-88k_X_terminal.jpg](https://ja.wikipedia.org/wiki/File:Network_Computing_Devices_NCD-88k_X_terminal.jpg "fig:Network_Computing_Devices_NCD-88k_X_terminal.jpg") |
| [Xserver_and_display_manager.svg](https://ja.wikipedia.org/wiki/File:Xserver_and_display_manager.svg "fig:Xserver_and_display_manager.svg")                                                      |

**X端末**（エックスたんまつ、X Terminal）はコンピュータの一つ。

[X Window SystemのXプロトコルを用いた通信により](../Page/X_Window_System.md "wikilink")、他のコンピュータ上（ホスト）で実行されたXクライアントアプリケーションの実行結果を表示させる端末である（もちろん入力も出来る）。描画部分（と入力部分）のみを実行するため、処理に負荷がかかる描画処理部分をハードウェア的に分離し、ホストを[アプリケーションの処理に特化することで](../Page/アプリケーションソフトウェア.md "wikilink")、ホストの負荷を軽減できる。

X端末上で実行するXサーバは、X端末上で[ファームウェア](../Page/ファームウェア.md "wikilink")として用意されている場合も、また、ホスト側から何らかの方法で[ダウンロード](https://ja.wikipedia.org/wiki/ダウンロード "wikilink")する方法もある。

X端末は、ホストと比べて[ハードディスク](https://ja.wikipedia.org/wiki/ハードディスク "wikilink")を持たず、かつ、メモリもXサーバが動作するだけの容量さえあればよいので、Xが動作するホスト（通常は[UNIX](../Page/UNIX.md "wikilink")マシン）よりも大幅にコストが下げられる、という利点があった。また、それ自身は、管理のための情報をほとんど持たない（ネットワークに接続するための[IPアドレス](../Page/IPアドレス.md "wikilink")程度）ため、複数台設置しても管理が容易になる、という利点があった。しかし、UNIXマシンの大幅なコストダウンやPCの普及により、専用のX端末というハードウェアをわざわざ用意する必然性が減ってきたため、最近ではハードウェアとしてのX端末は余り使われなくなってきている。X端末を使いたい場合には、PC上でのPC Xサーバソフトウェア（例えば、[Xming](../Page/Xming.md "wikilink")）を導入して実行させるか、あるいは[FreeBSD](../Page/FreeBSD.md "wikilink")や[Linux](../Page/Linux.md "wikilink")などの[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink")上でXを動かす、あるいは、[Microsoft Windowsで](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")[Cygwin](../Page/Cygwin.md "wikilink")のようなUNIX互換システムからXサーバを起動させる方法が取られている。

[Category:コンピュータ端末](https://ja.wikipedia.org/wiki/Category:コンピュータ端末 "wikilink") [Category:コンピュータの形態](https://ja.wikipedia.org/wiki/Category:コンピュータの形態 "wikilink") [Category:X_Window_System](https://ja.wikipedia.org/wiki/Category:X_Window_System "wikilink")
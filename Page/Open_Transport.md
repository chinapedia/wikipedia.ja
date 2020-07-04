> この記事は[Open Transport](https://ja.wikipedia.org/wiki/Open_Transport)から翻訳されています。


**Open Transport** は、[アップルが](../Page/アップル_\(企業\).md "wikilink")[UNIX System Vの](../Page/UNIX_System_V.md "wikilink")[STREAMS](../Page/STREAMS.md "wikilink")を実装したものの名称。それまでの[MacTCP](https://ja.wikipedia.org/wiki/MacTCP "wikilink")を置き換えた。

Open TransportはMentat Portable Streamsという実装に基づいており、[TCP/IP](https://ja.wikipedia.org/wiki/TCP/IP "wikilink")とシリアル通信を制御する\[1\]。さらに、アップルはこれに[AppleTalk](../Page/AppleTalk.md "wikilink")の実装も追加した。

## 歴史

Open Transportは1995年5月、Power Mac 9500で最初に採用された。System 7.5.2 に含まれ、[PCIベースの](../Page/Peripheral_Component_Interconnect.md "wikilink")[Power Macの新製品向けにリリースされたが](../Page/Power_Mac.md "wikilink")、その後古いハードウェアでも利用可能となった。PCIベースの新しいMacではMacTCPがサポートされていなかったが、古いシステムではMacTCPとOpen TransportをNetwork Software Selectorで切り替え可能になっていた。MacTCPにはない機能として、複数の設定を切り替えて使用可能だった。

Open Transportの評価は様々である。高速性と拡張性を評価する者もいたが、初期のOpen TransportのTCP/IP実装はバグが多く不評を買った。また、[C++](../Page/C++.md "wikilink")向けに設計された[APIが問題にされることもあった](../Page/アプリケーションプログラミングインタフェース.md "wikilink")（バイナリ互換問題）。Open Transportのアーキテクチャ（すなわち STREAMS）は、様々な[プロトコルスタック](../Page/プロトコルスタック.md "wikilink")を容易に追加できるのが特徴だが、TCP/IP があらゆる通信で使われるようになるにつれ、オーバースペックで複雑すぎる点が問題となっていった。

このため、Open Transportは[macOS](https://ja.wikipedia.org/wiki/macOS "wikilink")への移行時に捨てられることになった。macOSではより一般的な[ソケットが使われている](../Page/ソケット_\(BSD\).md "wikilink")。Open Transportは[Classic環境で古いアプリケーションを使う際に限定的に使われている](../Page/Classic_\(ソフトウェア\).md "wikilink")。

## 脚注

[Category:Classic_Mac_OS](https://ja.wikipedia.org/wiki/Category:Classic_Mac_OS "wikilink") [Category:ネットワークソフト](https://ja.wikipedia.org/wiki/Category:ネットワークソフト "wikilink")

1.  [Apple Tech Note 1117](http://developer.apple.com/technotes/tn/tn1117.html) - Open Transport STREAMS FAQ
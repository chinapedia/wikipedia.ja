> この記事は[Advanced Power Management](https://ja.wikipedia.org/wiki/Advanced_Power_Management)から翻訳されています。


**Advanced Power Management**（アドバンスド・パワー・マネージメント、**APM**）とは、[PC/AT互換機](https://ja.wikipedia.org/wiki/PC/AT互換機 "wikilink")で使われていた[電源](../Page/電源.md "wikilink")管理[インタフェースの一つである](../Page/インタフェース_\(情報技術\).md "wikilink")。[インテル](https://ja.wikipedia.org/wiki/インテル "wikilink")および[マイクロソフト](../Page/マイクロソフト.md "wikilink")によって[1991年](../Page/1991年.md "wikilink")に策定された。

## 概要

[Basic Input/Output System](https://ja.wikipedia.org/wiki/Basic_Input/Output_System "wikilink")(BIOS)呼出を前提としたインタフェースで、[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink")(OS)側からBIOSを呼び出す事が可能ならばOSに関わり無く使用可能である。BIOS呼び出しのインタフェースとして、[リアルモード](../Page/リアルモード.md "wikilink")からの呼び出し、[仮想86モード](../Page/仮想86モード.md "wikilink")からの呼び出し、そして、32ビットBIOS呼び出しがサポートされているが、32ビットBIOS呼び出しの初期化には前2者のいずれかが必要となる。機能としてはソフトウエアによる電源操作、メモリイメージを保持したまま[CPU](../Page/CPU.md "wikilink")や[周辺機器](../Page/周辺機器.md "wikilink")の電源を切って電源消費を抑えるサスペンド/リジューム機能などや[電池](../Page/電池.md "wikilink")の管理などがある。当初は主に[ノートパソコン](../Page/ノートパソコン.md "wikilink")に搭載されたが、[ソフトウェア](../Page/ソフトウェア.md "wikilink")による電源操作の機能のインタフェースとして[デスクトップパソコン](../Page/デスクトップパソコン.md "wikilink")にも導入された。

## 終焉

[モバイル](https://ja.wikipedia.org/wiki/モバイル "wikilink")用途として開発された[80386SL以降のCPUではAPMの実装を支援する機構がある](../Page/Intel_80386.md "wikilink")。それは、[システムマネジメントモード](../Page/システムマネジメントモード.md "wikilink")という動作モードで、OSからはトラップ出来ない特殊な割り込みを契機に移行し電源管理イベントなどを処理する。APMにおいてはOS側には電源管理イベントは通知されることは無く、OS側が知るにはBIOS呼び出しによって定期的に調査（ポーリング）する必要があった。

APMにおいては、基本的な機能のみが規定されており、一部の周辺機器の電源管理に関しては規定があったものの、様々な補助的な電源管理機能はベンダによって公開されていない[ハードウェア](../Page/ハードウェア.md "wikilink")[レジスタやBIOSインタフェース等を通してアクセスする](../Page/レジスタ_\(コンピュータ\).md "wikilink")[デバイスドライバ](../Page/デバイスドライバ.md "wikilink")などによって提供されており、限界を露呈しつつあった。また、BIOSの実装も複雑でありOSとの競合も起こりやすかった。

[2005年](../Page/2005年.md "wikilink")現在、これらの問題から[ACPIにその地位を明け渡した](../Page/Advanced_Configuration_and_Power_Interface.md "wikilink")。

[Category:ハードウェア](https://ja.wikipedia.org/wiki/Category:ハードウェア "wikilink") [Category:ファームウェア](https://ja.wikipedia.org/wiki/Category:ファームウェア "wikilink") [Category:BIOS](https://ja.wikipedia.org/wiki/Category:BIOS "wikilink")
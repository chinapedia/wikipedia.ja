> この記事は[SX-Window](https://ja.wikipedia.org/wiki/SX-Window)から翻訳されています。


**SX-Window**とは、[SHARP](../Page/シャープ.md "wikilink") [X68000](https://ja.wikipedia.org/wiki/X68000 "wikilink")シリーズに1990年のEXPERT II/PRO II/SUPER HD以降、標準添付されていた[ウィンドウシステム](../Page/ウィンドウシステム.md "wikilink")（[デスクトップ環境](https://ja.wikipedia.org/wiki/デスクトップ環境 "wikilink")）である。別途ソフトウェアのみがパッケージ販売されているため、標準装備になっていない機種や、新しい版のシステムは別途購入し、使用することが可能であった。

SX-WINDOWは標準DOSの[Human68k](../Page/Human68k.md "wikilink")と協調して動作している。したがって、Human68kからみればSX-WINDOWは一[プロセス](../Page/プロセス.md "wikilink")に過ぎない。SX-WINDOWは自プロセス内で各タスクを扱っている。X68000シリーズは[リニアアドレッシング](https://ja.wikipedia.org/wiki/リニアアドレッシング "wikilink")なので素直な構成で作られている。SX-WINDOWは当時の[Windowsや](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")[Macintosh](../Page/Macintosh.md "wikilink")と同様､[イベントドリブンによる](../Page/イベント_\(プログラミング\).md "wikilink")[マルチタスク](../Page/マルチタスク.md "wikilink")である。

画面のデザイン、配色などは[NeXT](../Page/NeXT.md "wikilink")の[GUIに近いイメージで作られていた](https://ja.wikipedia.org/wiki/グラフィカルユーザインタフェース "wikilink")。同時期に[OS/2](https://ja.wikipedia.org/wiki/OS/2 "wikilink")や[Acorn Archimedesが同種のインターフェースを採用しているが](https://ja.wikipedia.org/wiki/Acorn_Archimedes "wikilink")、対象物に対して右ボタンクリックで[コンテキストメニュー](../Page/コンテキストメニュー.md "wikilink")を出すシステムはWindowsや[Mac OSよりもSX](https://ja.wikipedia.org/wiki/Mac_OS "wikilink")-WINDOWの方が先であった。

画面モードはX68000の高解像モードである768\*512実画面1024\*1024の16色が使われていたが、Ver3よりグラフィックウィンドウ導入によって高解像のままで最大512\*512 65536色を出せるようになった。

これはGUI部分をテキスト画面で描画し、グラフィック部をグラフィック画面でウィンドウを描画しているところに、従来はテキストグラフィック双方の解像度を合わせてグラフィック部分も16色に制限されていたのを、テキスト画面とグラフィック画面の画面モードを変えて重ねることでグラフィックウィンドウ内部のみを65536色モードに変えることが可能になった。X68000の持つ[CRTCの柔軟さが生かされている](../Page/CRTC_\(LSI\).md "wikilink")。

[ファイルシステム](../Page/ファイルシステム.md "wikilink")はHuman68kと同一であり、[Macintosh](../Page/Macintosh.md "wikilink")と違いリソースはファイルとして持つので、データファイルは純粋にデータファイルのままである。

後に**シャーペン**という強力なカスタマイズ性と機能を持つテキストエディタが付属した。定義ファイルと内外コマンドによって、エディタ、ワープロ、[コンソールウィンドウと形態を変える事ができる](../Page/コマンドラインインタプリタ.md "wikilink")。シャーペンカスタマイズコンテストも行われ、ユーザー独自の定義ファイル、外部コマンドが応募された。シャーペンの文書ファイルはテキスト部と装飾部に分かれ、装飾部を外すだけで即テキストファイル化が可能であった。装飾部はテキストの最後にEOFコードが付きその後にバイナリで付加される。イメージを貼り付けた場合は、テキスト部で該当する所には「絵」という文字が挿入される。

Ver3.1が最終である。SX-WindowおよびHuman68kはフリーウェアとして公開されている。

[Category:ウィンドウシステム](https://ja.wikipedia.org/wiki/Category:ウィンドウシステム "wikilink") [Category:オペレーティングシステム](https://ja.wikipedia.org/wiki/Category:オペレーティングシステム "wikilink")
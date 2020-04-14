> この記事は[QED \(テキストエディタ\)](https://ja.wikipedia.org/wiki/QED_\(テキストエディタ\))から翻訳されています。


**QED**は[Unix](https://ja.wikipedia.org/wiki/Unix "wikilink")オペレーティングシステムの[テキストエディタ](../Page/テキストエディタ.md "wikilink") [ed](https://ja.wikipedia.org/wiki/ed "wikilink")やexの祖となった[ラインエディタ](https://ja.wikipedia.org/wiki/ラインエディタ "wikilink")である。

## 概要

[SDS 940上の](https://ja.wikipedia.org/wiki/SDS_940 "wikilink")[Berkeley Timesharing System向けとして](https://ja.wikipedia.org/wiki/:en:Berkeley_Timesharing_System "wikilink")[バトラー・ランプソン](../Page/バトラー・ランプソン.md "wikilink")および[L Peter DeutschPeter Deutschにより開発された](https://ja.wikipedia.org/wiki/:en:L_Peter_Deutsch "wikilink")。実装は1965年から1966年にかけて、Deutschと[Dana Angluinが行った](https://ja.wikipedia.org/wiki/:en:Dana_Angluin "wikilink")\[1\]\[2\]。名称は "quick editor" の略\[3\]。[テレタイプ端末](../Page/テレタイプ端末.md "wikilink")での利用を念頭に設計されており、[ビデオ表示端末](https://ja.wikipedia.org/wiki/ビデオ表示端末 "wikilink")では設計上考慮すべき点が大きく異なるため対応していなかった\[4\]。

後に[ケン・トンプソン](../Page/ケン・トンプソン.md "wikilink")が[CTSS](../Page/CTSS.md "wikilink")版を書いている。このバージョンでは[正規表現](../Page/正規表現.md "wikilink")を導入した点が特筆される。トンプソンは[Multics](../Page/Multics.md "wikilink")向けに[BCPL](../Page/BCPL.md "wikilink")でQEDを書き直した。このMultics版は[GE-600システムに移植され](../Page/GE-600シリーズ.md "wikilink")、[ベル研究所](../Page/ベル研究所.md "wikilink")内で[GECOSまたは](../Page/GCOS.md "wikilink")[GCOS](../Page/GCOS.md "wikilink")（[GEのコンピュータ事業を](../Page/ゼネラル・エレクトリック.md "wikilink")[ハネウェル](../Page/ハネウェル.md "wikilink")が取得後）上で1960年代末まで使われた。GECOS-GCOS版は A. W. Winklehoff が書いたI/Oルーチン群を使っている。[デニス・リッチー](../Page/デニス・リッチー.md "wikilink")とケン・トンプソンと[ブライアン・カーニハン](../Page/ブライアン・カーニハン.md "wikilink")がベル研究所内で使用するためのQEDのマニュアルを書いている\[5\]\[6\]\[7\]。彼らが[UNIX](../Page/UNIX.md "wikilink")[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink")の開発者でもあったことから、QEDはUNIXの初期のテキストエディタ[ed](https://ja.wikipedia.org/wiki/ed "wikilink")、[sedに自然に影響を及ぼし](../Page/Sed_\(コンピュータ\).md "wikilink")、さらにそこから派生したやなどにも影響を与えている\[8\]。

QEDの別バージョンとして、[ウォータールー大学](../Page/ウォータールー大学.md "wikilink")でハネウェルのシステム向けに Peter Fraser が書いた[FRED](https://ja.wikipedia.org/wiki/:en:FRED_\(text_editor\) "wikilink") (Friendly Editor) がある。[Tom Duff](https://ja.wikipedia.org/wiki/:en:Tom_Duff "wikilink")、[ロブ・パイク](../Page/ロブ・パイク.md "wikilink")、Hugh Redelmeier、David Tilbrook が結成したトロント大学のチームは[UNIX](../Page/UNIX.md "wikilink")にQEDを移植している。David Tilbrook はQEFというツールセットにQEDを含めている。

ノルウェーの[Norsk Dataのシステムでも](https://ja.wikipedia.org/wiki/:en:Norsk_Data "wikilink")、Nord TSS や [SINTRAN III](https://ja.wikipedia.org/wiki/:en:SINTRAN_III "wikilink") というOS上でQEDをエディタとして使用していた。

## 脚注

## 関連項目

  - [テキストエディタの一覧](https://ja.wikipedia.org/wiki/テキストエディタの一覧 "wikilink")

## 外部リンク

  - [FRED - the friendly editor.](http://www.thinkage.ca/english/gcos/expl/fred/expl.html)
  - [QED as part of QEF tools](http://www.qef.com/html/toolsdesc.html#qed)

[Category:テキストエディタ](https://ja.wikipedia.org/wiki/Category:テキストエディタ "wikilink")

1.  .
2.  *cf*. .
3.  .
4.  , p. 793.
5.  D. M. Ritchie and K. L. Thompson, "QED Text Editor", [MM-70-1373-3](http://cm.bell-labs.com/cm/cs/who/dmr/qedman.pdf) (June 1970), reprinted as "QED Text Editor Reference Manual", MHCC-004, Murray Hill Computing, Bell Laboratories (October 1972).
6.  B. W. Kernighan, "A Tutorial Introduction to the QED Text Editor under GE-TSS", MM-70-1373-6 (June 1970), reprinted as "Tutorial Introduction to QED Text Editor", MHCC-002, Murray Hill Computing, Bell Laboratories (October, 1972).
7.  B. W. Kernighan, "A Guide to the Advanced Use of QED Text Editor", MM-70-1373-7 (July 1970), reprinted as "A Guide to Advanced Use of QED Text Editor", MHCC-003, Murray Hill Computing, Bell Laboratories (October, 1972).
8.  .
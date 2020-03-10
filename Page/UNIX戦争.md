> この記事は[UNIX](https://ja.wikipedia.org/wiki/UNIX)から翻訳されています。


**UNIX戦争**（ゆにっくすせんそう）とは、[UNIX](../Page/UNIX.md "wikilink") [コンピュータ](../Page/コンピュータ.md "wikilink") [オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink")のベンダー間で[1980年代](../Page/1980年代.md "wikilink")後半から[1990年代](../Page/1990年代.md "wikilink")前半にかけて発生した将来のUNIX標準規格を巡る争いである。

[Unix_history.en.svg](https://ja.wikipedia.org/wiki/File:Unix_history.en.svg "fig:Unix_history.en.svg")

## 概要

1980年代中盤、一般的なUNIXのバージョンとして[カリフォルニア大学バークレー校](../Page/カリフォルニア大学バークレー校.md "wikilink")の[BSD](../Page/BSD.md "wikilink")と、[AT\&T](../Page/AT&T.md "wikilink")の[System Vがある](https://ja.wikipedia.org/wiki/UNIX_System_V "wikilink")。どちらも[Version 7 Unixから派生したものであるが](https://ja.wikipedia.org/wiki/Version_7_Unix "wikilink")、大きくかけ離れてしまった（このふたつの衝突もUNIX戦争と言われることがある）。そこからさらに各社のUNIXが派生していき、多かれ少なかれ違いを生じていった。

[1984年](../Page/1984年.md "wikilink")、**[X/Open](https://ja.wikipedia.org/wiki/X/Open "wikilink")**という[標準化グループがあるベンダーグループによって結成される](../Page/オープン標準.md "wikilink")。これは互換性のある[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink")を作ることが目的であり、そのベースとしてUNIXが選択された。

AT\&T は X/Openに注意をひかれた。UNIXの均一性を高めるため、AT\&T と BSD系UNIXベンダーのトップであった[サン・マイクロシステムズ](../Page/サン・マイクロシステムズ.md "wikilink")は[1987年](https://ja.wikipedia.org/wiki/1987年 "wikilink")から共通のシステムを作るための共同開発を開始した。これが後に **System V Release 4**（SVR4）としてリリースされる。

顧客や業界紙からは喝采をもって迎えられたこの決断だが、他のUNIXベンダーはサンが不当に有利になるのではないかと恐れた。彼らは[Open Software Foundation](../Page/Open_Software_Foundation.md "wikilink")（**OSF**）を結成し、[OSF/1](https://ja.wikipedia.org/wiki/OSF/1 "wikilink")をリリースした。これは、もっとBSDに近い実装である。AT\&Tは他のベンダーを結集して[UNIX International](https://ja.wikipedia.org/wiki/UNIX_International "wikilink")（**UI**）を結成する。

技術的な議論は脇に押しやられ、ふたつの「オープン」なUNIXが対決する構図となった。このとき、X/Openは中立的立場を保った。

OSF は、[ウィジェット・ツールキット](https://ja.wikipedia.org/wiki/ウィジェット・ツールキット "wikilink")として[Motifを開発し](../Page/Motif_\(GUI\).md "wikilink")、対抗して UI は、[OpenLook](https://ja.wikipedia.org/wiki/OpenLook "wikilink")を開発した。これは結果的に Motifの勝利となった。商用UNIXのデスクトップ環境として業界標準となった[CDEは](https://ja.wikipedia.org/wiki/Common_Desktop_Environment "wikilink") Motif を使用しており、これは SVR4 にも後に導入され、[Solaris](../Page/Solaris.md "wikilink")でも採用されていた。

[1993年](../Page/1993年.md "wikilink")、AT\&Tは UNIX を[ノベル社に売却し](../Page/ノベル_\(企業\).md "wikilink")、商標権を X/Open に譲渡した。[1996年](../Page/1996年.md "wikilink")、X/Open は OSF と合併し、[The Open Groupを結成した](../Page/The_Open_Group.md "wikilink")。現在、その[Single UNIX Specificationが](https://ja.wikipedia.org/wiki/Single_UNIX_Specification "wikilink")[プロプライエタリなUNIXの唯一の標準規格となっている](../Page/プロプライエタリ・ソフトウェア.md "wikilink")。しかし、既にUNIX市場に与えられたダメージは大きかった。

短期的な勝者はサン・マイクロシステムズであろう。System V の技術を取り込むことができ、SVR4 を採用した他社のシステムを採用した顧客には、互換性を技術的根拠としてリプレースを持ちかける事が容易になった。しかし、それも[オープンソース](../Page/オープンソース.md "wikilink")の大波の前には一時的な勝利でしかなかったと言わざるをえない。

## 比較表

2陣営の標準化競争となった主な技術と参加企業は以下である。

|                                                                  | OSF陣営                                                                                                                                                                                                                                                                                                                                                                                                                             | UI陣営                                                                                                                                                                                                  | 備考                                                                                                                                                       |
| ---------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [標準化団体](https://ja.wikipedia.org/wiki/標準化団体 "wikilink")          | [OSF](../Page/Open_Software_Foundation.md "wikilink")                                                                                                                                                                                                                                                                                                                                                                             | [UI](https://ja.wikipedia.org/wiki/UNIX_International "wikilink")                                                                                                                                     | [X/Open](https://ja.wikipedia.org/wiki/X/Open "wikilink")は中立。合併後の存続団体はOSF。                                                                               |
| [OS](../Page/オペレーティングシステム.md "wikilink")                         | [OSF/1](https://ja.wikipedia.org/wiki/OSF/1 "wikilink")                                                                                                                                                                                                                                                                                                                                                                           | [SVR4](https://ja.wikipedia.org/wiki/System_V#SVR4 "wikilink")                                                                                                                                        | OSF/1の本格採用は[DECと](../Page/ディジタル・イクイップメント・コーポレーション.md "wikilink")[日立製作所](../Page/日立製作所.md "wikilink")のみ                                                   |
| [GUI](https://ja.wikipedia.org/wiki/グラフィカルユーザインタフェース "wikilink") | [Motif](../Page/Motif_\(GUI\).md "wikilink")                                                                                                                                                                                                                                                                                                                                                                                      | [OpenLook](https://ja.wikipedia.org/wiki/OpenLook "wikilink")                                                                                                                                         | 後の[COSEではMotifベースの](../Page/Common_Open_Software_Environment.md "wikilink")[CDEを採用](https://ja.wikipedia.org/wiki/Common_Desktop_Environment "wikilink") |
| 分散処理 ([RPC](https://ja.wikipedia.org/wiki/遠隔手続き呼出し "wikilink"))  | [DCE](../Page/Distributed_Computing_Environment.md "wikilink")                                                                                                                                                                                                                                                                                                                                                                    | [ONC+](../Page/Open_Network_Computing_Remote_Procedure_Call.md "wikilink")                                                                                                                            |                                                                                                                                                          |
| 参加企業                                                             | [アポロコンピュータ](https://ja.wikipedia.org/wiki/アポロコンピュータ "wikilink")、[Bull](https://ja.wikipedia.org/wiki/Bull "wikilink")、[DEC](../Page/ディジタル・イクイップメント・コーポレーション.md "wikilink")、[HP](../Page/ヒューレット・パッカード.md "wikilink")、[IBM](../Page/IBM.md "wikilink")、[ニクスドルフ](https://ja.wikipedia.org/wiki/ニクスドルフ "wikilink")、[シーメンス](../Page/シーメンス.md "wikilink")、[フィリップス](../Page/フィリップス.md "wikilink")、[日立製作所](../Page/日立製作所.md "wikilink")など | [AT\&T](../Page/AT&T.md "wikilink")、[Sun](../Page/サン・マイクロシステムズ.md "wikilink")、[富士通](../Page/富士通.md "wikilink")、[日本電気](../Page/日本電気.md "wikilink")、[東芝](https://ja.wikipedia.org/wiki/東芝 "wikilink")など | [ソニー](../Page/ソニー.md "wikilink")は中立                                                                                                                      |
|                                                                  |                                                                                                                                                                                                                                                                                                                                                                                                                                   |                                                                                                                                                                                                       |                                                                                                                                                          |

## 関連項目

  - [UNIX](../Page/UNIX.md "wikilink")
  - [OSF](https://ja.wikipedia.org/wiki/OSF "wikilink")
  - [UI](https://ja.wikipedia.org/wiki/UI "wikilink")

## 外部リンク

以下はすべて英文。

  - [Unix Wars](http://livinginternet.com/i/iw_unix_war.htm) (Living Internet)
  - [The UNIX Wars](http://www.bell-labs.com/history/unix/wars.html) (Bell Labs)
  - [The UNIX System — History and Timeline](http://www.unix.org/what_is_unix/history_timeline.html) (The Open Group)
  - [Unix Standards](http://www.faqs.org/docs/artu/ch17s02.html) ([エリック・レイモンド](../Page/エリック・レイモンド.md "wikilink"), *The Art of Unix Programming*)
  - [Chapter 11. OSF and UNIX International](http://www.groklaw.net/article.php?story=20050601125916588) (Peter H. Salus, *The Daemon, the GNU and the Penguin*)

[Category:UNIX](https://ja.wikipedia.org/wiki/Category:UNIX "wikilink") [Category:コンピュータ分野における議論と対立](https://ja.wikipedia.org/wiki/Category:コンピュータ分野における議論と対立 "wikilink") [Category:コンピュータ史](https://ja.wikipedia.org/wiki/Category:コンピュータ史 "wikilink") [Category:サン・マイクロシステムズ](https://ja.wikipedia.org/wiki/Category:サン・マイクロシステムズ "wikilink")
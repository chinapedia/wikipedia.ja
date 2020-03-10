> この記事は[WorldWideWeb](https://ja.wikipedia.org/wiki/WorldWideWeb)から翻訳されています。


**WorldWideWeb**（ワールドワイドウェブ）は、世界初の[ウェブブラウザ](../Page/ウェブブラウザ.md "wikilink")であり\[1\]、[WYSIWYG](../Page/WYSIWYG.md "wikilink")の[HTMLエディタ](https://ja.wikipedia.org/wiki/HTMLエディタ "wikilink")である\[2\]。後に [World Wide Web](../Page/World_Wide_Web.md "wikilink") との混同を避けるため **Nexus** と改称している。それが書かれた当時、ウェブを閲覧する手段は WorldWideWeb しかなかった\[3\]。

[ソースコード](../Page/ソースコード.md "wikilink")が1993年に[パブリックドメイン](../Page/パブリックドメイン.md "wikilink")としてリリースされている\[4\]\[5\]。

## 歴史

1990年後半、[CERNに勤務していた](../Page/欧州原子核研究機構.md "wikilink")[ティム・バーナーズ＝リー](../Page/ティム・バーナーズ＝リー.md "wikilink")が[NeXT製コンピュータ上で](../Page/NeXTcube.md "wikilink")\[6\] WorldWideWeb を書き始めた。2カ月後の1990年12月25日、最初の全体の[ビルドが成功した](https://ja.wikipedia.org/wiki/ビルド_\(ソフトウェア\) "wikilink")\[7\]。その後もバーナーズ＝リーや同僚が修正とビルドを繰り返し、インターネットの[ニュースグループ](../Page/ニュースグループ.md "wikilink")で公表したのは1991年8月のことである\[8\]。その時点でプロジェクトには、Bernd Pollermann、[ロバート・カイリュー](../Page/ロバート・カイリュー.md "wikilink")、Jean-Francois Groff\[9\]、[ラインモードブラウザ](https://ja.wikipedia.org/wiki/ラインモードブラウザ "wikilink")を書いた Nicola Pellow といった人々が参加していた\[10\]。

NeXTのシステムから他の[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink")への完全な[移植は難しかったため](../Page/移植_\(ソフトウェア\).md "wikilink")、チームは編集機能を省いた「パッシブ・ブラウザ」を開発した\[11\]。[X Window System](../Page/X_Window_System.md "wikilink") はチーム内の誰も使ったことがなかったため、移植できなかった\[12\]。

バーナーズ＝リーとGroffは多くのWorldWideWebのコンポーネントを[C言語](../Page/C言語.md "wikilink")で書き直し、[libwww](https://ja.wikipedia.org/wiki/libwww "wikilink") [APIを作り上げた](../Page/アプリケーションプログラミングインタフェース.md "wikilink")\[13\]。

他にも [ViolaWWW](https://ja.wikipedia.org/wiki/ViolaWWW "wikilink") のような初期のブラウザもあったが、1993年には [NCSA Mosaic](../Page/NCSA_Mosaic.md "wikilink") がそれら全てに取って代わった。最初の創造に関わった人々は別の仕事に取り掛かっていった。[World Wide Web](../Page/World_Wide_Web.md "wikilink") に関する開発についての標準やガイドラインの制定など（たとえば、[HTMLや](../Page/HyperText_Markup_Language.md "wikilink")、様々な[通信プロトコル](../Page/通信プロトコル.md "wikilink")）である。

1993年4月30日、CERN は WorldWideWeb の[ソースコード](../Page/ソースコード.md "wikilink")を[パブリックドメイン](../Page/パブリックドメイン.md "wikilink")として公開し、[フリーソフトウェア](../Page/フリーソフトウェア.md "wikilink")とした。いくつかのバージョンは [evolt.org's browser archive](https://browsers.evolt.org/?worldwideweb/NeXT) からダウンロード可能である。バーナーズ＝リーは当初これを[GPLライセンスでリリースしようと考えていたが](../Page/GNU_General_Public_License.md "wikilink")、結局商用での利用を考慮してパブリックドメインとした\[14\]\[15\]。

## 技術的情報

WorldWideWebは [NEXTSTEP](../Page/NEXTSTEP.md "wikilink")プラットフォーム上で開発されたため、プログラムはNEXTSTEPのコンポーネントを利用している。たとえば、WorldWideWebの[レイアウトエンジンはNEXTSTEPのText](https://ja.wikipedia.org/wiki/HTMLレンダリングエンジン "wikilink")[クラスを活用している](../Page/クラス_\(コンピュータ\).md "wikilink")\[16\]。

### 機能

WorldWideWebは基本的な[スタイルシート](../Page/スタイルシート.md "wikilink")を表示することができる\[17\]。NeXTシステムのサポートするいかなるファイルタイプ（[PostScript](../Page/PostScript.md "wikilink")\[18\]\[19\]、動画\[20\]、音声\[21\]）でもダウンロードしたりオープンしたりでき、[ニュースグループ](../Page/ニュースグループ.md "wikilink")を閲覧したり、[スペルチェックしたりできる](../Page/スペルチェッカ.md "wikilink")。最初、NEXTSTEPのTextクラスが画像オブジェクトをサポートするまでは、画像は別ウィンドウで表示されていた\[22\]。

このブラウザは[WYSIWYG](../Page/WYSIWYG.md "wikilink")エディタとしても機能する\[23\]\[24\]。複数のウィンドウでウェブページを表示しつつ、同時にそれらを編集したりリンクしたりできる。"Mark Selection" という機能でアンカーを生成し、"Link to Marked" という機能で選択したテキストを直近にマークしたアンカーとリンクすることができる。リモートからページを編集することはできなかった。HTTP PUT メソッドがまだ実装されていなかったためである\[25\]。ファイルはローカルなファイルシステム内で編集され、その後HTTPサーバによってウェブとして公開される。

WorldWideWebの操作パネルにはNextとPreviousというボタンがあり、これにより最後に見たページの次か後のリンクをたどることができる。[Opera](https://ja.wikipedia.org/wiki/Opera "wikilink")の Rewind と Fast Forward ボタンに近い。つまり、リンクの並んだページからあるページを選んで表示させたとき、Previousボタンを押すとリンクの並び順の前のリンクが指しているページが表示される\[26\]。これは当時は便利な機能だった。というのは、多くのページがそのような一覧でリンクされていたからである。しかし World Wide Web が成長するにつれ、そのような習慣はなくなり、後のWebブラウザからもそのようなボタンはなくなった。

WorldWideWebには[ブックマーク](../Page/ブックマーク.md "wikilink")のような機能はないが、似たような機能なら備えていた。あるリンクをセーブしておきたい場合、それをユーザー自身のホームページにリンクしてセーブすることができる。ホームページを階層化してブックマークのフォルダーのようにすることもできる\[27\]。

WorldWideWebは、[FTP](../Page/File_Transfer_Protocol.md "wikilink")\[28\]、[HTTP](../Page/Hypertext_Transfer_Protocol.md "wikilink")（バーナーズ＝リーが[1989年](../Page/1989年.md "wikilink")に発明）\[29\]、[NNTP](../Page/Network_News_Transfer_Protocol.md "wikilink")\[30\]という複数のプロトコルを使っており、[URLでローカルファイルも扱える](../Page/Uniform_Resource_Locator.md "wikilink")。

## 名称

バーナーズ＝リーは当初 *The Mine of Information*\[31\] や *The Information Mesh*\[32\] という名称を提案していたが、最終的に *WorldWideWeb* が選ばれている\[33\]。

## 脚注

## 参考文献

  - *Weaving the Web* (ISBN 0-06-251587-X), Webの概念に関するバーナーズ＝リーの著書

## 外部リンク

  - [Tim Berners-Lee: WorldWideWeb(英語)](https://www.w3.org/People/Berners-Lee/WorldWideWeb)
  - [A Little History of the World Wide Web（英語）](https://www.w3.org/History.html)
  - [Berners-Lee's blog](http://dig.csail.mit.edu/breadcrumbs/blog/4)
  - [World Wide Web downloadable here](https://browsers.evolt.org/?worldwideweb/)
  - [ソースコード](https://www.w3.org/History/1991-WWW-NeXT/Implementation/)
  - [CERN, Where the Web Was "WWW" born](http://info.cern.ch/)

[Category:ウェブブラウザ](https://ja.wikipedia.org/wiki/Category:ウェブブラウザ "wikilink") [Category:インターネットの歴史](https://ja.wikipedia.org/wiki/Category:インターネットの歴史 "wikilink") [Category:オープンソースソフトウェア](https://ja.wikipedia.org/wiki/Category:オープンソースソフトウェア "wikilink") [Category:1990年のソフトウェア](https://ja.wikipedia.org/wiki/Category:1990年のソフトウェア "wikilink")

1.
2.
3.
4.
5.
6.
7.
8.
9.
10.
11.
12.
13.
14.
15.
16.
17.
18.
19.
20.
21.
22.
23.
24.
25.
26.
27.
28.
29.
30.
31.
32.
33.
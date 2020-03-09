> この記事は[Gnutella](https://ja.wikipedia.org/wiki/Gnutella)から翻訳されています。


**Gnutella**（**グヌーテラ**、**ニューテラ**）は[P2P](../Page/Peer_to_Peer.md "wikilink")[プロトコル](https://ja.wikipedia.org/wiki/プロトコル "wikilink")および[ファイル共有](https://ja.wikipedia.org/wiki/ファイル共有 "wikilink")[クライアント](https://ja.wikipedia.org/wiki/クライアント_\(コンピュータ\) "wikilink")。

## 概要

[ナップスター](https://ja.wikipedia.org/wiki/ナップスター "wikilink")などのP2Pクライアントの場合は、中央[サーバ](https://ja.wikipedia.org/wiki/サーバ "wikilink")が存在し、ファイルの[メタデータ](https://ja.wikipedia.org/wiki/メタデータ "wikilink")の管理や検索サービスを提供することにより、P2Pネットワークが機能している。それに対し、グヌーテラはサーバに依存せず、純粋に[ピア](https://ja.wikipedia.org/wiki/ピア "wikilink")間の通信のみでファイルの送受信などの機能を実現している。

P2Pのしくみの分類中、このようなピア間の通信のみによって機能するものを[ピュアP2P](https://ja.wikipedia.org/wiki/ピュアP2P "wikilink")、ナップスターのようにサーバの仲介を必要とするものを、[ハイブリッドP2P](https://ja.wikipedia.org/wiki/ハイブリッドP2P "wikilink")と呼んでいる。

その他には、[KaZaA](https://ja.wikipedia.org/wiki/Kazaa_Lite "wikilink") や [Skype](https://ja.wikipedia.org/wiki/Skype "wikilink")に使われている[スーパーノード型ハイブリッドP2Pがある](https://ja.wikipedia.org/wiki/Peer_to_Peer#スーパーノード型P2P "wikilink")。

## 特徴

ナップスターに代表される[第一世代P2P](https://ja.wikipedia.org/wiki/第一世代P2P "wikilink")(ハイブリッドP2P)は、中央サーバに依存する為、ネットワークへの[トラフィック](https://ja.wikipedia.org/wiki/トラフィック "wikilink")は少ないが、耐障害性が低く、サーバがダウンしたらネットワークが形成できないという弱点があった。それに対してグヌーテラに代表される[第二世代P2P](https://ja.wikipedia.org/wiki/第二世代P2P "wikilink")（ピュアP2P）は、各クライアントがサーバを兼ねる（[サーバント](https://ja.wikipedia.org/wiki/サーバント "wikilink")）為、耐障害性が高い。

製作者の「核戦争でも生き残れるように設計されたもの（*Gnutella is designed to survive nuclear war*）」や、「万一、ニューヨークに核爆弾が投下されたとしても、（それ自体はたいへんなことだが）ニューヨーク以外の『グヌーテラ友達』によってグヌーテラネットは維持されるだろう」といった言葉が、グヌーテラネットワークの特徴をよく表している。

## グヌーテラの仕組み

グヌーテラネットワーク上で交わされているメッセージは、PING、PONG、PUSH、QUERY、QUERY_HITの以上である。

### 接続

中央サーバが存在しないグヌーテラにおいて、最初に接続するときに何処に問い合わせるのか？という問題が出てくる。 グヌーテラ第一世代では、ノード情報を掲示板などで入手する方法が採られていたが、グヌーテラ第二世代になって、GWC（GWebCache）というブートストラップサーバーにより各ノードと接続する方法がとられた。

接続においては、グヌーテラサーバントはまずPINGという接続要求を出す。それに対して、接続相手はPONGという信号を返して、[ハンドシェイク](https://ja.wikipedia.org/wiki/ハンドシェイク "wikilink")を行い接続が完了する。

### 検索

検索はグヌーテラネットワークで行っており、ファイルを求めるサーバントは、QUERYをグヌーテラネットワークに送信し、ヒットしたクエリがQUERY_HITとして検索結果に表示される。

### 転送

グヌーテラでの、ファイルの転送は[HTTP](https://ja.wikipedia.org/wiki/HTTP "wikilink")プロトコルで行われている。 ファイルの転送は、QUERY_HIT識別子に含まれる、[IPアドレス](https://ja.wikipedia.org/wiki/IPアドレス "wikilink")や[ポート番号](https://ja.wikipedia.org/wiki/ポート番号 "wikilink")などによってファイルの所有者にHTTPでの転送命令を出す。 また、ファイル所有者が[ファイアウォール](https://ja.wikipedia.org/wiki/ファイアウォール "wikilink")下にいるサーバントの場合は、PUSH識別子を出し、相手サーバントがHTTPでの転送命令を出す。

## 開発の経緯

[2000年](https://ja.wikipedia.org/wiki/2000年 "wikilink")、[AOL](https://ja.wikipedia.org/wiki/AOL "wikilink")社の一部門である[Nullsoft](https://ja.wikipedia.org/wiki/Nullsoft "wikilink")で、当時社員だった [Justin Frankelと](https://ja.wikipedia.org/wiki/ジャスティン・フランケル "wikilink")[Tom Pepperの二人が](https://ja.wikipedia.org/wiki/Tom_Pepper "wikilink")、最初のグヌーテラクライアントを開発した。

2000年3月14日、二人はNullsoftのサーバー上にプログラムをダウンロードできる形でアップロードした。この出来事は[スラッシュドット](https://ja.wikipedia.org/wiki/スラッシュドット "wikilink")で告知されたため、その日の内に数千人がソフトをダウンロードした。ソースコードについては、後ほど[GPLライセンスの元で提供する予定だった](https://ja.wikipedia.org/wiki/GNU_General_Public_License "wikilink")。

翌日、AOLは法的問題を理由にプログラムの提供を中止し、さらにNullsoft部門にプロジェクトを中止させた。しかしこの措置によっても、グヌーテラを止めることはできなかった。

数日後には、[リバースエンジニアリング](https://ja.wikipedia.org/wiki/リバースエンジニアリング "wikilink")によってプロトコルは解析され、それを元にグヌーテラ互換の[オープンソース](https://ja.wikipedia.org/wiki/オープンソース "wikilink")クローンが登場した。現在でも、様々なグループが グヌーテラ 互換クライアントの開発を続けている。

### グヌーテラ第一世代

シャットダウンから間もなくして、[Brian MaylandがNullsoftのプログラムを入手して](https://ja.wikipedia.org/wiki/Brian_Mayland "wikilink")、グヌーテラプロトコルの動作原理を理解するために[リバースエンジニアリング](https://ja.wikipedia.org/wiki/リバースエンジニアリング "wikilink")した。彼の仕事のおかげでテキストベースの[UNIX](https://ja.wikipedia.org/wiki/UNIX "wikilink")プログラムを作った[Josh Pieperや](https://ja.wikipedia.org/wiki/Josh_Pieper "wikilink")、より使いやすいGUIをもったプログラムを作ろうとした[Gene Kanや](https://ja.wikipedia.org/wiki/Gene_Kan "wikilink")[Spencer Kimballのような人々によってソフトウェア開発がなされることになった](https://ja.wikipedia.org/wiki/Spencer_Kimball "wikilink")。

### グヌーテラ第二世代

ユーザの裾野が広がるにつれ、システムの重大な問題が取り沙汰されはじめた。ネットワークはPINGリクエストで溢れかえり、同時に非常に多くの検索クエリーで高負荷になった。より高速な[ハブとしての役割を果たすコンピュータに接続した低速の](https://ja.wikipedia.org/wiki/ハブ_\(ネットワーク機器\) "wikilink")[モデム](https://ja.wikipedia.org/wiki/モデム "wikilink")といった形でネットワークの[トポロジー](https://ja.wikipedia.org/wiki/トポロジー "wikilink")は非効率的だった。第一世代のソフトウェアの深刻なバグによってパケットがネットワーク上を不明確にさまよっていた。ネットワークは“本来は少数のユーザのために設計されたもので”100人単位から10,000 単位のユーザに膨張しトラブルに見まわれた。「ただ乗り」や「何も提供していないのにファイルを取り出すだけの人々」によってもユーザが探し物をするのを難しくした。

もう一度、情熱的なコミュニティーが救済に乗り出した。[Bob Schmidtが初めてのホストキャッシングシステムを開発した](https://ja.wikipedia.org/wiki/Bob_Schmidt "wikilink")。プログラマー達はGnutella 0.56のコードを修正し、[パケット](https://ja.wikipedia.org/wiki/パケット "wikilink")が適切に運ばれるようにTTLのバグを取り除こうとした。そして、[Jorge Gonzalesはネットワークをダメにする](https://ja.wikipedia.org/wiki/Jorge_Gonzales "wikilink")[スパマー](https://ja.wikipedia.org/wiki/スパマー "wikilink")たちからネットワークを守る行動に出た。

この時点で、物事は個人の開発者が全てをまかなうにはあまりにも複雑になっていた。彼らはコードを書き、報道やユーザやお金の工面をしなければならなかった。 こういった事情で、早急に商業的な努力が介入し、「救済に乗り出す」必要が出てきた。[Clip2](https://ja.wikipedia.org/wiki/Clip2 "wikilink")はgnutellahosts.comを開発し、より良いホストキャッシュの実装し、いくらかナップスターのようなトポロジーをグヌーテラネットワークに組み入れて合体させるようなやり方で動く小さな[サーバ](https://ja.wikipedia.org/wiki/サーバ "wikilink")リフレクターを開発した。

## グヌーテラ互換サーバント

| 名称                                                                        | プラットホーム                                                                         | ライセンス                                                                                                                                                                  |
| ------------------------------------------------------------------------- | ------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [Acquisition](https://ja.wikipedia.org/wiki/:en:Acquisitionx "wikilink")  | [macOS](https://ja.wikipedia.org/wiki/macOS "wikilink")                         | [シェアウェア](https://ja.wikipedia.org/wiki/シェアウェア "wikilink")                                                                                                              |
| Acqlite                                                                   | [macOS](https://ja.wikipedia.org/wiki/macOS "wikilink")                         | [GNU GPL](https://ja.wikipedia.org/wiki/GNU_General_Public_License "wikilink")                                                                                         |
| [BearShare](https://ja.wikipedia.org/wiki/:en:BearShare "wikilink")       | [Microsoft Windows](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink") | シェアウェア [:en:Closed source](https://ja.wikipedia.org/wiki/:en:Closed_source "wikilink")                                                                                 |
| [Phex](https://ja.wikipedia.org/wiki/:en:Phex "wikilink")                 | [Java](https://ja.wikipedia.org/wiki/Java "wikilink")                           | [GNU GPL](https://ja.wikipedia.org/wiki/GNU_General_Public_License "wikilink")                                                                                         |
| [Cabos](https://ja.wikipedia.org/wiki/Cabos "wikilink")                   | [Java](https://ja.wikipedia.org/wiki/Java "wikilink")                           | [GNU GPL](https://ja.wikipedia.org/wiki/GNU_General_Public_License "wikilink")                                                                                         |
| CocoGnut                                                                  | [RISC OS](https://ja.wikipedia.org/wiki/RISC_OS "wikilink")                     | [フリーウェア](https://ja.wikipedia.org/wiki/フリーウェア "wikilink")                                                                                                              |
| [Gnucleus](https://ja.wikipedia.org/wiki/:en:Gnucleus "wikilink")         | [Microsoft Windows](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink") | [GNU GPL](https://ja.wikipedia.org/wiki/GNU_General_Public_License "wikilink"), [GNU LGPL](https://ja.wikipedia.org/wiki/GNU_Lesser_General_Public_License "wikilink") |
| [GTK-Gnutella](https://ja.wikipedia.org/wiki/:en:gtk-gnutella "wikilink") | [UNIX](https://ja.wikipedia.org/wiki/UNIX "wikilink")                           | [GNU GPL](https://ja.wikipedia.org/wiki/GNU_General_Public_License "wikilink")                                                                                         |
| [LimeWire](../Page/LimeWire.md "wikilink")                                | [Java](https://ja.wikipedia.org/wiki/Java "wikilink")                           | [GNU GPL](https://ja.wikipedia.org/wiki/GNU_General_Public_License "wikilink")                                                                                         |
| [mlDonkey](https://ja.wikipedia.org/wiki/:en:mlDonkey "wikilink")         |                                                                                 |                                                                                                                                                                        |
| [Morpheus](https://ja.wikipedia.org/wiki/Morpheus "wikilink")             | [Microsoft Windows](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink") | [:en:Closed source](https://ja.wikipedia.org/wiki/:en:Closed_source "wikilink")                                                                                        |
| [Mutella](https://ja.wikipedia.org/wiki/:en:Mutella "wikilink")           | [UNIX](https://ja.wikipedia.org/wiki/UNIX "wikilink")                           | [GNU GPL](https://ja.wikipedia.org/wiki/GNU_General_Public_License "wikilink")                                                                                         |
| [Poisoned](https://ja.wikipedia.org/wiki/:en:Poisoned "wikilink")         | [macOS](https://ja.wikipedia.org/wiki/macOS "wikilink")                         | [GNU GPL](https://ja.wikipedia.org/wiki/GNU_General_Public_License "wikilink")                                                                                         |
| [Qtella](https://ja.wikipedia.org/wiki/:en:Qtella "wikilink")             | [Linux](https://ja.wikipedia.org/wiki/Linux "wikilink")                         | [GNU GPL](https://ja.wikipedia.org/wiki/GNU_General_Public_License "wikilink")                                                                                         |
| [Shareaza](https://ja.wikipedia.org/wiki/Shareaza "wikilink")             | [Microsoft Windows](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink") | [GNU GPL](https://ja.wikipedia.org/wiki/GNU_General_Public_License "wikilink")                                                                                         |
| [Symella](https://ja.wikipedia.org/wiki/:en:Symella "wikilink")           | [Symbian OS](https://ja.wikipedia.org/wiki/Symbian_OS "wikilink")               | [GNU GPL](https://ja.wikipedia.org/wiki/GNU_General_Public_License "wikilink")                                                                                         |
| [XNap](https://ja.wikipedia.org/wiki/:en:XNap "wikilink")                 | [Java](https://ja.wikipedia.org/wiki/Java "wikilink")                           | [GNU GPL](https://ja.wikipedia.org/wiki/GNU_General_Public_License "wikilink")                                                                                         |
| XFactor                                                                   | [macOS](https://ja.wikipedia.org/wiki/macOS "wikilink")                         | [GNU GPL](https://ja.wikipedia.org/wiki/GNU_General_Public_License "wikilink")                                                                                         |

## 関連項目

  - [Cabos](https://ja.wikipedia.org/wiki/Cabos "wikilink")
  - [Freenet](https://ja.wikipedia.org/wiki/Freenet "wikilink")
  - [LimeWire](../Page/LimeWire.md "wikilink")
  - [Peer to Peer](../Page/Peer_to_Peer.md "wikilink")
  - [Perfect Dark](https://ja.wikipedia.org/wiki/Perfect_Dark "wikilink")
  - [Profes](https://ja.wikipedia.org/wiki/Profes "wikilink")
  - [Share](https://ja.wikipedia.org/wiki/Share_\(ソフトウェア\) "wikilink")
  - [WinMX](https://ja.wikipedia.org/wiki/WinMX "wikilink")
  - [Winny](https://ja.wikipedia.org/wiki/Winny "wikilink")
  - [ヌテラ](https://ja.wikipedia.org/wiki/ヌテラ "wikilink") - [北米](https://ja.wikipedia.org/wiki/北米 "wikilink")や[欧州](https://ja.wikipedia.org/wiki/欧州 "wikilink")で人気のある[スプレッド](https://ja.wikipedia.org/wiki/スプレッド "wikilink")（パンなどに塗る食品）。Gnutellaの[語源](https://ja.wikipedia.org/wiki/語源 "wikilink")とされるものの一つ（[GNU](https://ja.wikipedia.org/wiki/GNU "wikilink") + Nutella）。

## 外部リンク

  - [jnutella](http://www.jnutella.org/)（日本語）
  - [Gnutella Wiki](http://twoget.sourceforge.jp/)（日本語）
  - [@IT : ネットワーク管理者のためのGnutella入門](http://www.atmarkit.co.jp/fwin2k/experiments/gnutella_for_admin/gnutella_for_admin_0.html)（日本語）
  - [GTK-Gnutella](http://gtk-gnutella.sourceforge.net/ja/?page=news)（日本語）
  - [Gnutella Wiki](http://www.the-gdf.org/index.php?title=Main_Page)（英語）
  - [Gnutella Protocol Development](http://rfc-gnutella.sourceforge.net/index.html)（英語）
  - [LIMEWIRE DEVELOPER RESOURCES](http://www.limewire.com/developer/)（英語）

*Gnutella互換サーバント*

  - [360Share](http://www.360share.com/)
  - [Acqlite](http://sourceforge.net/projects/acqlite/)
  - [Acquisition](http://www.acquisitionx.com/)
  - [AquaLime](http://www.unitethecows.com/)
  - [BearFlix](http://www.bearflix.com/)
  - [BearShare](http://www.bearshare.com/)
  - [Cabos](http://cabos.sourceforge.jp/)
  - [Epicea](http://epicea.philix.net/)
  - [eTomiPro](http://www.mp3downloading.com/etomipro/help_guide/help_guide.html)
  - [Foxy](http://www.gofoxy.net/tw/download.jsp)
  - [FreeWire](http://www.freewirep2p.com/download.html#inter)
  - [FrostWire](http://www.frostwire.com/)
  - [giFT-Gnutella](http://gift.sourceforge.net/)
  - [GnuAce](http://www.r66.7-dj.com/~ace/index2.html)
  - [GPU](http://gpu.sourceforge.net/)
  - [GTK-Gnutella](http://gtk-gnutella.sourceforge.net/ja/?page=news)
  - [GnucDNA](http://www.gnucleus.com/GnucDNA/)
  - [Gnucleus](http://www.gnucleus.com/)
  - [iMesh](http://www.imesh.com/)
  - [Kceasy](http://www.kceasy.com/)
  - [LemonWire](http://www.infocentral.jp/daunrodo/lemonwire/65239.htm)
  - [LimeWire](http://www.limewire.com/japanese/content/home.shtml)
  - [LimeWire CVS jum](http://www.gnutellaforums.com/showthread.php?t=10142)
  - [MLDonkey](http://mldonkey.org/)
  - [Morpheus](http://morpheus.com/)
  - [Mutella](http://mutella.sourceforge.net/)
  - [MXIE](http://cn.mxie.com/)
  - [MyNapster](http://www.mynapster.com/)
  - [NeoNapster](http://www.neonapster.com/)
  - [Phex](http://www.phex.org/mambo/)
  - [Shareaza](http://shareaza.sourceforge.net/)
  - [Swapper.NET](http://www.revolutionarystuff.com/swapper/)
  - [TrustyFiles](http://www.trustyfiles.com/)
  - [Vagaa](http://www.vagaa.com/)
  - [XNap](http://xnap.sourceforge.net/)
  - [xolox](http://www.xolox.nl/)
  - [Zultrax](http://www.zultrax.com/)

[Category:P2P](https://ja.wikipedia.org/wiki/Category:P2P "wikilink") [Category:ネットワークソフト](https://ja.wikipedia.org/wiki/Category:ネットワークソフト "wikilink")
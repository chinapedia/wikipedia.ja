> この記事は[SPG-NEWS](https://ja.wikipedia.org/wiki/SPG-NEWS)から翻訳されています。


**SPG-NEWS**は[パケット無線ネットワークFWD](https://ja.wikipedia.org/wiki/パケット無線_\(アマチュア無線\) "wikilink")-NETに対応した[電子メールクライアント](../Page/電子メールクライアント.md "wikilink")ソフトである。

W0RLIやF6FBBに代表される転送型RBBSにクライアントソフトとして接続しメールやニュース（Bulletinと呼ばれるのが一般的だった）の閲覧や書き込みを行う。転送型RBBSのメッセージ交換プロトコルに従い通信を行う機能の他にオートパイロット機能と呼ばれる一般ユーザーが端末からRBBSに対して行う操作を自動化しメッセージの閲覧・書き込みを自動化させる機能を持つ。

また、操作画面は国内初の[GUIを採用した](https://ja.wikipedia.org/wiki/グラフィカルユーザインタフェース "wikilink")。開発当時はパケット無線では[PC-9801などの](../Page/PC-9800シリーズ.md "wikilink")[MS-DOS](../Page/MS-DOS.md "wikilink")マシンが主に使われソフトウェアも[CUIをベースにしたものがほとんどで](../Page/キャラクタユーザインタフェース.md "wikilink")、当時としては操作性・見た目では画期的なものだった。

1990年に[FM TOWNS版がリリースされ](../Page/FM_TOWNS.md "wikilink")、後に[Windows版をリリース](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")。1990年代末に開発・サポートを終了している。(但し、使用することは可能)

## 機能

### 転送型RBBSのクライアント機能

W0RLIが開発した転送型RBBSとのメッセージ転送機能を持つ。メッセージ転送は転送型RBBS側に他の転送型RBBSと同様の転送設定を行わなければならない。

### オートパイロット機能

転送型RBBSに一般ユーザーとして接続し（この場合転送型RBBS側の転送設定は必要ない）、メッセージの一覧を取得し、自分宛のメール・閲覧したいニュースにジャンルを抽出して自動的にダウンロードを行う。また、ユーザーから発信するメールやニュースへの書き込みがある場合は自動的に書き込み処理を行う。

転送型RBBSには複数の種類があり操作コマンドや出力リストのフォーマットが統一化されていないので、転送型RBBS別の設定を行うことでメジャーなすべての転送型RBBSに対応している。

### GUIによる画面操作

全面的にGUIを採用し、現在の電子メールクライアントと同様の操作環境を持つ。国内の公開されているパケット無線ネットワーク用としては最初で最後の試みだった。

### 設定

各種設定はテキストファイルにより記録していたが、ユーザーはすべてGUI画面上で設定できるようにしていた。

## 対応環境

  - FM TOWNS版

<!-- end list -->

  -
    Version 1.0～2.1まではFM TOWNS版

<!-- end list -->

  - Windows版

<!-- end list -->

  -
    Version3.0～4.8まではWindows版
    Windows版は[16ビット](../Page/16ビット.md "wikilink")アプリケーションでVer3.1～Windows 95までは動作保証しているが、Windows NT以降では一部通信系で動作しないことがあり動作保証対象外としている。

## 開発者

木澤朋和　コールサインはJO1SPG(当時。現在は失効中。)

現在は、マイクロソフトの製品や技術を伝えるポッドキャスト番組「WoodStreamのデジタル生活」を配信している。

Microsoft MVP for Windows and Devices for IT(2018/7～2019/6)

## 開発の経緯

[FM TOWNSの熱狂的なユーザーであった作者がFM](../Page/FM_TOWNS.md "wikilink") TOWNSの圧倒的な性能を見せつけるために開発したことが元々の開発理由。1990年のビジネスショウのLotusブースで[cc:Mail](https://ja.wikipedia.org/wiki/cc:Mail "wikilink")を見て感激し、パケット無線ネットワークでも同様のソフトウェアを開発したと言うのが表向きの開発理由。

SPG-NEWSの名称は、作者のアマチュア無線のコールサイン**JO1SPG**をとり JO1**SPG**-**NE**t**W**ork **S**ystemの略である。

### FM TOWNS版

Version1.0はF-BASIC386を使用して開発。後にHigh-C|386とFM TOWNSのGUIライブラリを使用してVersion2.xが開発された。ハムフェアでも展示を行い、当時なかったGUIによる操作画面に注目は浴びたもののFM TOWNSのユーザーがほとんどいなかったことで実際の使用者は数人程度と見られる。(後述のWindows版開発によりTOWNS版は開発終了)

### Windows版

FM TOWNS版に固執し続けた作者に対してPLUG (Packet Radio Users Group) の関係者が「これだけのものがTOWNSというマイナー機種でしか動かないというのはもったいない。是非ともWindows版を開発すべき」と提案があり、開発に着手。 結果的にユーザー数は圧倒的に増えGUIベースのクライアントソフトとしてその地位を揺るぎないものとした。 開発はVisualBasic3.0（英語版）で行われた。（表示はすべて日本語）

## その他

  - オートパイロットソフトは、定期的に転送型RBBSを占有することがありRBBSの管理者(SysOp)からは毛嫌いされる傾向にあった。よって、オートパイロットソフトの使用を拒絶管理者も多くオートパイロットソフト側で連続使用の制限やマニュアルでの注意喚起などが行われていた。特にオートパイロットソフトとして先行して開発されていたATERMや[FPMB](https://ja.wikipedia.org/wiki/FPMB "wikilink")では、先駆者としての苦労があり、後発のSPG-NEWSの作者はこの二つのソフトの作者に最大の敬意を表している。
  - SPG-NEWSの作者は他のソフトの作者に比べて多少ふざけた感があり、自らを架空のソフト開発会社WoodStream Networksの会長兼最高経営責任者を名乗りあたかもマイクロソフトのビル・ゲイツのように振る舞った。サポートやリリースは日**汗**工業新聞なる形式で第三者的な視点で"記事"を書き連絡するかたちをとった。(後日談で作者は"壮大なるビル・ゲイツごっこ"で楽しかったとしている。)
  - その作者のキャラクターを歓迎する者がいる一方、ソフトウェアの品質は決して高いとは言えず、本来の開発に集中しないふざけた振る舞いに対して批判的な意見もあった。
  - SPG-NEWSはVersion4.8(実質的な最終版であるVersion4.5のFWD-IX対応版)の後に、32ビット版インターネットメール版Version5.0(開発コードネーム WoodStream)を開発する予定だったが、あまりにも大風呂敷を広げすぎて開発できず、開発を断念した。

## 外部リンク

  - [パケット無線ネットワーク電子メールシステム SPG-NEWS](http://www.woodstream.gr.jp/spg-news/index.html)
  - [FWD-NETインターネットエクスチェンジについて FWD-IX](http://www.fwnet.jp/index.html?WWW_MENU=m040100)
  - [開発者のポッドキャスト番組「WoodStreamのデジタル生活」](http://windows-podcast.com/podcast/)
  - [開発者のブログ「闘うサンデープログラマー」](http://windows-podcast.com/sundayprogrammer/)
  - [Tomokazu Kizawa Microsoft MVP for Windows and Devices for IT](https://mvp.microsoft.com/en-us/PublicProfile/4029168?fullName=Tomokazu%20Kizawa)

[es:Packet radio](https://ja.wikipedia.org/wiki/es:Packet_radio "wikilink") [nl:Packet-Radio](https://ja.wikipedia.org/wiki/nl:Packet-Radio "wikilink")

[Category:アマチュア無線](https://ja.wikipedia.org/wiki/Category:アマチュア無線 "wikilink")
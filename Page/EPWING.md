> この記事は[EPWING](https://ja.wikipedia.org/wiki/EPWING)から翻訳されています。


**EPWING**（イーピーウィング）は、[電子辞書](../Page/電子辞書.md "wikilink")の標準形式。EPWINGのサブセット(V1相当)が[JIS X 4081](../Page/JIS_X_4081.md "wikilink")「日本語電子出版検索データ構造」として制定されている。

## 成立の経緯

[1987年](https://ja.wikipedia.org/wiki/1987年 "wikilink")（昭和62年）、[富士通](../Page/富士通.md "wikilink")[片岡正弘](https://ja.wikipedia.org/wiki/片岡正弘 "wikilink")は自社のワープロ[OASYS](../Page/OASYS.md "wikilink") 100用の[広辞苑](../Page/広辞苑.md "wikilink")CD-ROMを[岩波書店](../Page/岩波書店.md "wikilink")、[大日本印刷](../Page/大日本印刷.md "wikilink")などと共同で制作し、この仕様を「**WING**」と名づけた。

[1988年](../Page/1988年.md "wikilink")（昭和63年）に[CD-ROM](../Page/CD-ROM.md "wikilink")の論理フォーマットである[ISO 9660が制定されると](../Page/ISO_9660.md "wikilink")、各社はWINGをISO 9660上に移し、より汎用性を持たせた**EPWING**規約(**E**lectronic **P**ublishing-**WING**:*電子出版WING規格*)第1版(V1)を制定。同時に、電子出版物を共通フォーマットで推進することを目的に、それらを制作する企業で構成される[EPWINGコンソーシアム](http://www.epwing.or.jp/member/member.html) を1991年に結成した。この時に参加した企業は [岩波書店](../Page/岩波書店.md "wikilink")、[大日本印刷](../Page/大日本印刷.md "wikilink")、[凸版印刷](../Page/凸版印刷.md "wikilink")、[富士通](../Page/富士通.md "wikilink")、[ソニー](../Page/ソニー.md "wikilink") である。 [電子ブック (EB)も](../Page/電子ブック_\(規格\).md "wikilink")、WING規格をもとにして拡張されたものである。

## 仕様

### Version

EPWINGは、続々と拡張され、計6仕様とEPWING STがある([「バージョン情報」](http://www.epwing.or.jp/lineup/version.html))。EPWING STを除けば、それ以前の仕様は内包している。もちろん、新しくなるほど高機能なわけだが、古い仕様であれば、対応している検索ソフトも多い。

  - EPWING V1
    文字、白黒画像、音声([CD-DA](../Page/CD-DA.md "wikilink"))
  - EPWING V2
    カラー画像、圧縮音声([WAV](../Page/WAV.md "wikilink"))
  - EPWING V3
    動画([MPEG-1](../Page/MPEG-1.md "wikilink"))
  - EPWING V4
    データ圧縮、ハードディスクへのインストール
  - EPWING V5
    [JPEG](../Page/JPEG.md "wikilink")などマルチメディア機能、数式など、表示機能の拡張
  - EPWING V6
    ひらがな・カタカナインデックスの共通化と[データ圧縮](../Page/データ圧縮.md "wikilink")によるサイズ縮小

<!-- end list -->

  - EPWING ST
    対話型コンテンツ再生機能(デモンストレーションや学習用途)

### ファイル構造

EPWINGのCD-ROMの基本構成(V1)を以下に示す。ルートディレクトリにはCATALOGSというファイルが１つあり、CD-ROMに含まれる辞書(複数の辞書・付録等)とその構成を示す。単一の辞書毎にサブディレクトリが(複数)あり、その下にDATAとGAIJIというサブディレクトリがある。DATAの下のHONMONには、本文データ(図版・音声)や検索インデックスが含まれる。GAIJIの下には、[外字](../Page/外字.md "wikilink")データ(ビットマップ)ファイルが置かれる。外字データファイルのファイル名は製品毎に異なる。

[ファイル:EPWING_DIR.jpg](https://ja.wikipedia.org/wiki/ファイル:EPWING_DIR.jpg "wikilink")

規格が進むにつれ(V2～)、ファイル構造も変化し、HONMON2(圧縮), HONMONG(グラフィックス：図版), HONMONS(サウンド：音声)などになっている場合がある。「JIS X 4081」では、理論上は1ファイル約190GBまでの書籍が構築可能である。

## 検索方法

EPWINGの主要な検索方法は以下のとおり。ワイルドカードや正規表現は、基本的には使えない(検索ソフトによっては、ある程度対応している場合がある。([「機能紹介」](http://www.epwing.or.jp/about/function.html))。

  - 前方一致検索
    見出し語の前方に一致する部分だけを入力して、それを構成要素とすることばを検索する。"前方"や"ぜんぽう"で検索すると、"前方"自体だけでなく、"前方不注意"や、"ぜんぽうこうえんふん【前方後円墳】"なども見つかる。
  - 後方一致検索
    見出し語の後方に一致する部分だけを入力して、それを構成要素とすることばを検索する。"方向"や"ほうこう"で検索すると、"方向"自体だけでなく、"双方向"や、"はやしほうこう【林鳳岡】"なども見つかる。
  - クロス検索・クロス条件検索 (見出し語中の語句の条件検索・[見出語条件検索](http://www.epwing.or.jp/about/function.html))
    見出し語中の複合語を構成する各構成語(英字・数字・漢字・かな・カナ等)で検索する。
  - [条件検索](http://www.epwing.or.jp/about/function_03.html) (本文中のキーワード検索)
    本文中のキーワードを指定して、その言葉のふくまれる項目を検索することができる。見出し語ではなく、語釈中(本文)の単語を検索する。ただし、そのタイトル辞書の制作時に特別に切り出した特定の単語に対してインデックスを付与した場合にのみしかマッチしないので、実際に使用した場合には、語釈中に存在する任意の単語が見つからない場合もある。また、そもそもこのインデックス自体を最初から持っていない(インデックスサイズが膨大になり辞書自体のサイズが肥大化する、また、インデックス作業が非常に煩雑になるなどのために省いた)辞書も多くある。
  - 複合検索 ([ジャンル別検索](http://www.epwing.or.jp/about/function_04.html))
    そのタイトルの分野別・カテゴリー別検索方法。例えば漢和辞典であれば、読み・部首・画数のそれぞれを指定して検索する。（製品によっては、ジャンル別検索と呼称することがある)
  - メニュー検索
    本の目次から本文の該当箇所を引くように、階層化されたメニューからその項目を選択することができる。
  - カラーメニュー
    ビジュアルな画面の該当箇所を選択することで、その項目を検索できる。（例：「[広辞苑](../Page/広辞苑.md "wikilink")第5版・第6版」）

[電子ブック(規格)と違い](../Page/電子ブック_\(規格\).md "wikilink")、ワープロ専用機や汎用のコンピュータで使用することを前提にしており、読みだけでなく、漢字でも検索できる。

初期のタイトルでは、音声が[CD-DA](../Page/CD-DA.md "wikilink")で収録されているため、汎用のファイルシステムで扱うことができないが、まれである。

## 主要タイトル

これまでにEPWINGで出版された主要タイトルを示す。（現在販売終了のものも含む [「ラインナップ」](http://www.epwing.or.jp/lineup/lineup.html)）

### 統合辞書

  -

<!-- end list -->

  - スーパー統合辞書2006 富士通 『広辞苑第五版』(23万語)/『リーダーズ英和辞典第2版』(27万語)/『新和英中辞典第5版』/『漢字源』/『現代用語の基礎知識2006年版』/『四字熟語辞典』/『カタカナ新語辞典』
  - 岩波日本語表現辞典 岩波書店 『岩波国語辞典第六版』(6万3千語)/『岩波新漢語辞典第二版』/『類語情報』(4万7千語)
  - 旺文社版マルチ辞書 旺文社 『ニューサンライズ英和・和英辞典』(4万3千語/3万3千語)/『旺文社国語辞典第八版』(7万7千語)/『カタカナ語新辞典第四版』(1万1千語)/『早引きワープロ辞典』※販売終了
  - 三省堂辞典館 三省堂 『新辞林』(15万項目)/『三省堂現代国語辞典』(6万語)/『コンサイス外来語』(3万3千語)/『ニューセンチュリー英和辞典』(4万語)/『新クラウン和英辞典』(3万1千語)/『デイリーコンサイス英和辞典第5版・和英辞典第4版』/『必携故事ことわざ・慣用句・類語実用・用字用語・手紙実用文辞典』/『ワープロ漢字辞典』 ※販売終了
  - 辞典盤97 アスキー 『岩波国語辞典』/『研究社新英和・和英中辞典』/『知恵蔵』/『マイペディア』 ※販売終了

### 国語・漢字・類語

  -

<!-- end list -->

  - 広辞苑第六版\[DVD\] 岩波書店『広辞苑第六版』 (24万語)
  - 広辞苑第五版 富士通/岩波書店/インターチャネル 『広辞苑第五版』 (23万語)
  - 三省堂スーパー大辞林第2版 三省堂 『大辞林第二版』(23万3千語)/『デイリーコンサイス英和辞典第5版・和英辞典第4版』(5万7千語/6万3千語)/漢字辞典※販売終了
  - 学研現代新国語辞典・漢字源 富士通 『学研現代新国語辞典』(6万5千語)/『漢字源』
  - 岩波国語辞典 岩波書店 『岩波国語辞典第六版』
  - 岩波新漢語辞典第二版 岩波書店 『岩波新漢語辞典第二版』
  - 研究社類義語使い分け辞典 研究社 『研究社類義語使い分け辞典』
  - 日本語語彙大系 岩波書店 『岩波日本語語彙大系』

### 現代用語

  -

<!-- end list -->

  - 現代用語の基礎知識 自由国民社/富士通 『現代用語の基礎知識』 ※毎年改訂版が出版される

### 英語

  -

<!-- end list -->

  - 新英和大辞典第6版 研究社 『新英和大辞典第6版』(26万語)
  - 新和英大辞典第5版 研究社 『新和英大辞典第5版』(23万語/25万用例)
  - 新英和・和英中辞典 富士通 『新英和中辞典第7版』(10万語)/『新和英中辞典第5版』(9万7千語)
  - 新英和・和英中辞典 研究社/富士通 『新英和中辞典第6版』(9万語)/『新和英中辞典第4版』(7万語)※販売終了
  - 新編英和活用大辞典 研究社/富士通 『新編英和活用大辞典』(38万用例)
  - 研究社ビジネス英語スーパーパック 研究社 『ビジネス英和辞典』(3万4千項目)/『総合ビジネス英語文例事典』(7千文例)/『リーダーズ英和辞典初版』(26万語) ※販売終了
  - リーダーズ+プラスV2 研究社/富士通 『リーダーズ英和辞典第2版』(27万語)/『リーダーズ・プラス』(19万語)
  - 新英和中辞典 ソースネクスト 『研究社新英和中辞典第7版』(10万語)
  - 新和英中辞典 ソースネクスト 『研究社新和英中辞典第5版』(9万7千語)
  - 新リトル英和・和英辞典 ソースネクスト 『研究社新リトル英和辞典第6版』(6万2千語)/『新リトル和英辞典』(6万3千語)/英和コンピュータ用語辞典(4千2百語)
  - CD-科学技術45万語対訳辞典 英和・和英 日外アソシエーツ 『科学技術45万語対訳辞典 英和・和英』(45万語)
  - CD-180万語対訳大辞典英和・和英 日外アソシエーツ 『180万語対訳大辞典英和・和英』
  - 新グローバル&ニューセンチュリー英和・和英辞典 三省堂 『新グローバル英和辞典』(9万3千語)/『ニューセンチュリー和英辞典』(4万1千語) ※販売終了
  - ジーニアス英和大辞典 大修館書店 『ジーニアス英和大辞典』(25万5千語)
  - ジーニアス英和(第4版)・和英辞典(第2版)\[DVD\] 大修館書店 『ジーニアス英和辞典第4版』(9万6千語)/『ジーニアス和英第2版』(8万2千語)
  - ジーニアス英和(第3版)・和英辞典 大修館書店 『ジーニアス英和辞典第3版』(9万5千語)/『ジーニアス和英辞典』(8万語) ※販売終了
  - 新・実用英語ハンドブック 大修館書店 『実用英語ハンドブック 』
  - CD-NEW斎藤和英大辞典 日外アソシエーツ 『斎藤和英大辞典』(5万語/15万文例)
  - 学研ニューアンカー英和・和英辞典 富士通 『ニューアンカー英和・和英辞典』(5万1千語/2万5千語)
  - 『ビジネス技術実用英語大辞典Ｖ６　英和・和英』 プロジェクトポトス (英和2万4千語/和英2万7千語/用例11万9千件)

### 外国語

  -

<!-- end list -->

  - クラウン独和辞典 三省堂 『クラウン独和辞典』(5万2千語)/『デイリーコンサイス英和辞典第5版』 ※販売終了
  - クラウン仏和辞典 三省堂 『クラウン仏和辞典』(4万4千語)/『デイリーコンサイス英和辞典第5版』 ※販売終了

### 専門

  -

<!-- end list -->

  - 岩波理化学辞典 岩波書店/富士通 『岩波理化学辞典第5版』
  - 岩波生物学辞典 岩波書店 『岩波生物学辞典第4版』
  - 岩波日本史辞典 岩波書店 『岩波日本史辞典』
  - 岩波=ケンブリッジ世界人名辞典 岩波書店 『岩波=ケンブリッジ世界人名辞典』
  - 法律用語辞典 富士通 『自由国民社 法律用語辞典』
  - 研究社理化学英和辞典 研究社 『研究社理化学英和辞典』
  - 研究社医学英和辞典 研究社 『研究社医学英和辞典』
  - 研究社シェイクスピア辞典 研究社 『研究社シェイクスピア辞典』
  - 三省堂模範六法 三省堂 『三省堂模範六法2002年版』※販売終了
  - 心理学辞典 有斐閣 『有斐閣心理学辞典』

## 検索ソフトウェア

EPWINGは電子出版の共通フォーマットであり、さまざまな機種やOS用に検索ソフトが開発されている([「検索ソフト」](http://www.epwing.or.jp/lineup/view/index.html))。ただしソフトウェアによってはEPWINGの上位規格(V2～V6・ST)の全てに対応していないことがある。また、古いソフトは、大容量(honmonサイズが、2GB/4GB を超える)辞書に対応していない場合や、ユーザー側が開発した独自仕様である ebzip形式で圧縮された辞書(honmon.ebz)に対応していないものが多くある。

### 市販EPWING検索ソフトウェア

  - CDView (OASYS/Japanistに付属) - [富士通](../Page/富士通.md "wikilink")(株)
  - ロボワード／訳しマウス！ - (株)テクノクラフト
  - [ViewIng／インターネットViewIng](http://www.est.co.jp/products/viewing/) - イースト(株)
  - ViewIng Light (Freeware) - イースト(株)／ソニー(株)
  - ことといLight (Bundle) - 岩波書店/大日本印刷(株)
  - こととい (95Reader 読み上げ対応) - (株)SSCT
  - 電子辞典ビューア (EGBRIDGE に付属) - (株)[エルゴソフト](../Page/エルゴソフト.md "wikilink")
  - CD-ROM検索ソフトウェア - [NECインターチャネル](https://ja.wikipedia.org/wiki/NECインターチャネル "wikilink")(株)
  - [電辞萬](http://www.kgc.co.jp/denjiman.html) (販売終了) - 計測技研(株)
  - CAT'S EYE 翻訳 - ロジカルテック(株)
  - WordOnSight (Shareware) - [NEC情報システムズ](https://ja.wikipedia.org/wiki/NEC情報システムズ "wikilink")(株)
  - Dr.eye EPWING Viewer (Freeware) - INVENTEC Co.
  - CD検索アクセサリ (VJE-Delta に付属) - (株)バックス
  - MyDic (マイディック) (PC-Talkerなどが必要) - (株)高知システム開発
  - JammingLight (Jammingのライト版) - 今井あさと
  - [対訳君](../Page/対訳君.md "wikilink") (JammingLight搭載) - (株)MCL
  - The翻訳プロフェッショナル/スーパー - [東芝デジタルソリューションズ](../Page/東芝デジタルソリューションズ.md "wikilink")(株)
  - [超漢字](../Page/超漢字.md "wikilink")統合辞書 (OS: BTRON3/超漢字４) - パーソナルメディア(株)
  - 本格翻訳5 シリーズ - [ソースネクスト](../Page/ソースネクスト.md "wikilink")(株)
  - PC-Transer 翻訳スタジオ - (株)[クロスランゲージ](../Page/クロスランゲージ.md "wikilink")
  - CROSSROAD - [日本電気](../Page/日本電気.md "wikilink")(株)

### オンラインソフトウェア (Free/Share/Paid)

  - [Microsoft Windows](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink") - [DDwin](http://homepage2.nifty.com/ddwin), Jamming for Windows(Shareware), [EBView](http://ebview.sourceforge.net), [EBWin4](http://ebstudio.info/manual/EBWin4/EBWin4.html), PDIC(Shareware), EPWING QuickViewer, ALTAIR for Windows, digdic, Dicregate
  - [Mac OS](https://ja.wikipedia.org/wiki/Mac_OS "wikilink")(X) - [コトノコ](http://www.afternooncafe.jp/kotonoko/), Logophile, Jamming for Macintosh(Shareware), CeDar(PPC), 書見台(68K|PPC), かものす, mc (matrix calculator), CalendarMemo, oDictionary, ものしりフクロウ(68K|PPC), PDIC Viewer, qolibri, [Sebastopol EB](http://www.fiveflavors.com/sebastopol/) (「EB4Jライブラリ」使用), [EBMac](http://ebstudio.info/manual/EBMac/)
  - [iOS](https://ja.wikipedia.org/wiki/iOS_\(アップル\) "wikilink")([iPhone](https://ja.wikipedia.org/wiki/iPhone "wikilink")/[iPad](https://ja.wikipedia.org/wiki/iPad "wikilink")) - [EBPocket](http://ebstudio.info/manual/EBPocket_iPhone/) (Professional/Basic), [iDic](http://bigskyflier.com/iDic.aspx) (paid), [iDictPlus](http://sites.google.com/site/idictplus/home) (paid)
  - [MS-DOS](../Page/MS-DOS.md "wikilink")/[UNIX](../Page/UNIX.md "wikilink") - CD-ROM検索ソフト2, Dic, EB, ALTAIR
  - [Pocket PC](../Page/Pocket_PC.md "wikilink")/[Windows CE](https://ja.wikipedia.org/wiki/Windows_CE "wikilink") - [EBPocket](http://ebstudio.info/home/EBPocket.html) (Share/Free), Buckingham EB Player(Charityware)
  - [Zaurus](https://ja.wikipedia.org/wiki/Zaurus "wikilink")/[Linux](../Page/Linux.md "wikilink") - qtjiten, Zten, zten改(ztenv), JustReader+
  - [PalmOS](https://ja.wikipedia.org/wiki/PalmOS "wikilink") - WordSeeker(Shareware), Buckingham EB Player(Charityware)
  - [HP200LX](../Page/HP200LX.md "wikilink") - [EBR](http://homepage2.nifty.com/egweb/eguyan/ebr-up.htm).exm
  - [Mobile Gear](https://ja.wikipedia.org/wiki/Mobile_Gear "wikilink") - Dicmg
  - [Linux](../Page/Linux.md "wikilink")/[FreeBSD](../Page/FreeBSD.md "wikilink") (with GTK) - EBView, gxdic
  - [UNIX](../Page/UNIX.md "wikilink") - eblook, Forest, [Lookup](http://sourceforge.net/projects/lookup)
  - [KDE](../Page/KDE.md "wikilink") - KEBook
  - EPOC - pB
  - [BTRON](../Page/BTRON.md "wikilink") - 海老 (EBI)
  - BeOS/Intel - EBook Viewer
  - [Tcl/Tk](https://ja.wikipedia.org/wiki/Tcl/Tk "wikilink") - BookView
  - [X Window System](../Page/X_Window_System.md "wikilink") - xyaku(英和・和英翻訳ツール), xpopdic
  - Web Application - let me see..., adict
  - [Android](../Page/Android_\(オペレーティングシステム\).md "wikilink") - DroidWing (free/paid) ([aokabi.com](http://jp.androlib.com/android.developer.aokabi-com-jAmi.aspx)), [EBAndrioid](http://jp.androlib.com/android.application.com-nesnet-android-eb-AFAA.aspx) (free)(「EB4Jライブラリ」使用), [EBPocket for Android](http://ebstudio.info/manual/EBPocket_android/) (Pro/Free)

<!-- end list -->

  - [BlackBerry](../Page/BlackBerry.md "wikilink") - [EBBerry](http://cloudhunter.cocolog-nifty.com/blog/ebberry.html) (「EB4Jライブラリ」使用)

### EPWING対応

  - [Yomichan](https://chrome.google.com/webstore/detail/yomichan/ogmnaimimemjmbakcfefmnahgdfhfami) - A browser extension

<!-- end list -->

  - [Rikaisama](https://sourceforge.net/projects/rikaisama) - A Japanese-English popup dictionary

<!-- end list -->

  - [GoldenDict](https://sourceforge.net/projects/goldendict) - Support of multiple dictionary file formats

#### 電子辞書検索ソフト・電子辞書ビューアーの一覧

  - [**EPWING Viewers**](http://maximilk.web.fc2.com/viewers.htm)

## 後継・派生規格

後継・派生規格については仕様はオープンにはなっていない。

[ONESWING](https://ja.wikipedia.org/wiki/ONESWING "wikilink")はEPWINGの後継規格とされるものである。これはマルチプラットフォーム展開、圧縮＆暗号化＆認証機能、高速な全文検索をうたっている\[1\]ものの、最近は[スマートフォン](https://ja.wikipedia.org/wiki/スマートフォン "wikilink")アプリとしてのリリースが多く、デスクトップ向けの商品は少ない。

[ロゴヴィスタ](https://ja.wikipedia.org/wiki/ロゴヴィスタ "wikilink")・[電子辞典シリーズ](http://www.logovista.co.jp/)（旧[システムソフト](../Page/システムソフト.md "wikilink")電子辞典シリーズ）で採用されている辞書データの形式は、同社が[JIS X 4081形式を基本仕様として改良](../Page/JIS_X_4081.md "wikilink")・発展させていったフォーマット。最新版（[『漢字源改訂第四版』](http://www.gakken.jp/jiten/data/detail/1051203/)、2008年12月現在）では独自の拡張方式（既存の未使用の「表の表示タグ」を転用すること）により[ユニコード](https://ja.wikipedia.org/wiki/ユニコード "wikilink")（[JIS第三水準](../Page/JIS_X_0213.md "wikilink")、第四水準、[補助漢字](https://ja.wikipedia.org/wiki/補助漢字 "wikilink")）の表示にも対応した。

2007年（平成19年）5月現在、これらの仕様が統合へ向かう兆候は全く見られず、続々と仕様の乱立(囲い込み)が進んでいると言える状況にあり、その結果としてユーザー側の利便性が大いに損なわれてしまっている。

[株式会社電子辞典](http://www.densijiten.co.jp/) は、株式会社システムソフトを[スピンアウト](https://ja.wikipedia.org/wiki/スピンアウト "wikilink")した開発スタッフが2002年に設立した会社だが、同社の辞典シリーズ(DDViewer)は、EPWING形式でも派生仕様でもないAtom形式なので注意が必要である。

## 脚注

<references />

## 外部リンク

  - [EPWINGコンソーシアム](http://www.epwing.or.jp/about/about.html), [EPWINGとは？](https://web.archive.org/web/20110722120757/http://www.epwing.or.jp/about/about.html) - [Internet Archive](https://ja.wikipedia.org/wiki/Internet_Archive "wikilink")
  - [富士通 EPWING](http://software.fujitsu.com/jp/epwing/) JIS規格「日本語電子出版検索データ構造([JIS X 4081](../Page/JIS_X_4081.md "wikilink"))」準拠の電子辞書です
  - [UNIXで電子辞書をしゃぶりつくそう](http://hp.vector.co.jp/authors/VA000022/unixdic/) 「辞書システムの上手な使い方」
  - [EB Library](http://www.sra.co.jp/people/m-kasahr/eb/index.html) CD-ROM(EB, EBG, EBXA, EBXA-C, S-EBXA および EPWING 形式)書籍にアクセスするための C のライブラリ。EPWING辞書の圧縮・伸長を行う ebzip コマンド等を含む。
  - [EB series support page](http://ebstudio.info/home/) 個人で電子書籍・電子辞書を作成するためのツール集。
  - [鍋田辞書](http://www.nabeta.tk/) EPWINGと[ユニコード](https://ja.wikipedia.org/wiki/ユニコード "wikilink")データ辞書の同時検索が可能な辞書ソフト。
  - [Maximilk](http://hp.vector.co.jp/authors/VA037273/) フリーEPWING電子辞書(EDICT2, WordNet2.0, Webster's 1913, CEDICT, Wadoku, etc.) - [Vector](../Page/ベクター_\(企業\).md "wikilink")
  - [FreePWING](http://www.sra.co.jp/people/m-kasahr/freepwing/) [JIS X 4081](../Page/JIS_X_4081.md "wikilink") 形式の書籍データを生成を行うソフトウェア([Unix](https://ja.wikipedia.org/wiki/Unix "wikilink"), [Linux](../Page/Linux.md "wikilink"), [Cygwin](../Page/Cygwin.md "wikilink"))
  - [wikipedia-fpw](http://ikazuhiro.s206.xrea.com/staticpages/index.php/wikipedia-fpw) [ウィキペディア日本語版](../Page/ウィキペディア日本語版.md "wikilink")(や、その他の言語版)のダンプデータ（[ダウンロードサイト](http://download.wikimedia.org/jawiki/)）をFreePWINGを利用して[JIS X 4081形式に変換するツール](../Page/JIS_X_4081.md "wikilink")
  - [Boookends](http://sites.google.com/site/boookends/) 「FreePWING/Wikipedia-fpw」で変換した、オフライン版「[ウィキペディア日本語版](../Page/ウィキペディア日本語版.md "wikilink")」(EPWING/[JIS X 4081](../Page/JIS_X_4081.md "wikilink"))や、多言語版(ユニコード対応)を配布。
  - [EB4J](http://eb4j.sourceforge.jp/) 「EBライブラリ」を元に、100% Pure Java実装した電子辞書関連クラスライブラリ

[Category:辞典](https://ja.wikipedia.org/wiki/Category:辞典 "wikilink") [Category:ファイルフォーマット](https://ja.wikipedia.org/wiki/Category:ファイルフォーマット "wikilink") [Category:コンピュータのデータ](https://ja.wikipedia.org/wiki/Category:コンピュータのデータ "wikilink") [Category:教育ソフトウェア](https://ja.wikipedia.org/wiki/Category:教育ソフトウェア "wikilink")

1.
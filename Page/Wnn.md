> この記事は[Wnn](https://ja.wikipedia.org/wiki/Wnn)から翻訳されています。


**Wnn**（**うんぬ**、**ウーンヌ**）は、[日本語](../Page/日本語.md "wikilink")の[かな漢字変換](https://ja.wikipedia.org/wiki/かな漢字変換 "wikilink")による[日本語入力システム](../Page/日本語入力システム.md "wikilink")の一つである。元来は[ワークステーション](../Page/ワークステーション.md "wikilink")向けに開発され、後に組込機器向けが主要な用途となった。

## 歴史

1985年から[京都大学](../Page/京都大学.md "wikilink")、[慶應義塾大学](https://ja.wikipedia.org/wiki/慶應義塾大学 "wikilink")、立石電機（現・[オムロン](../Page/オムロン.md "wikilink")）、[アステック](https://ja.wikipedia.org/wiki/アステック "wikilink")（現・[アールワークス](https://ja.wikipedia.org/wiki/アールワークス "wikilink")）によって共同開発され、1987年に完成した。

開発当時は、PCでは連文節変換がすでに実現されていたが、ワークステーションでの日本語入力システムは一般的に、単語ごとまたは文節ごとに変換していた。このシステムは、ワークステーションでも「Watashino Namaeha Nakanodesu」と入力して正しく「私の名前は中野です」と一括変換できるような連文節変換を実現することを目指して開発されたことから、その文字列の頭文字を取ってWnnという名前が付けられた。「中野」は日本語処理開発チームの立石電機側の窓口となっていた人の名前である\[1\]。

Wnnバージョン4(Wnn4.x)は、1990年代のUNIXワークステーションで広く利用され、[X Window Systemにも同梱されるようになった](../Page/X_Window_System.md "wikilink")。ただし、辞書の語彙数や変換率は決して満足の行くものではなかった。Wnn4.2が基本となりワークステーションや組込機器向けにさまざまなバージョンのものが存在している。

## 特徴

ワークステーション型Wnnの大きな特徴は、ネットワーク透過な[クライアント・サーバ](https://ja.wikipedia.org/wiki/クライアント・サーバ "wikilink")型システムである点にある。一般的な日本語入力システムは、すべての処理をローカルで行う。これに対してWnnでは、ユーザーインターフェースを受け持つクライアントと、かな漢字変換エンジンであるサーバが分離しており、両者がネットワーク上で通信することで動作する。サーバはLAN内のいずれかのコンピュータで一つだけ動いていればよく、ローカルのCPU負荷の軽減になる他、単語登録や辞書学習の成果が一元的に蓄積されるというメリットがある。一方で、ネットワークを介することによるレスポンスの低下や、サーバやネットワークがダウンすると処理が不可能になるというデメリットもあるが、これが重大な問題である場合は、ローカルでサーバを動かすという手もある。

この柔軟性に富むアーキテクチャは、当時からネットワーク利用が一般的なUNIXワークステーションならではのものであり、CannaやSj3など他の入力システムにも受け継がれている。

Wnnのサーバプログラムはjserverという。クライアントは以下のものがある。

  - uum（ううむ）
    キャラクタ端末で動作する。端末の最下行を占有し、MS-DOSの日本語入力システムを非インラインで使用するのと同じような操作感である。名称はWnnを180度回転したところから名づけられている。
  - kinput2、xwnmo（えっくすうんも）
    [X Window Systemの](../Page/X_Window_System.md "wikilink")[インプットメソッド](../Page/インプットメソッド.md "wikilink")であり、インラインでの操作が可能である。
  - egg
    NEmacsやMuleに組み込まれている。

また、Wnnには[中国語](../Page/中国語.md "wikilink")・[韓国語バージョンも存在し](../Page/朝鮮語.md "wikilink")、それぞれ以下のような名称になっている。

| 言語                                                     | システム名 | サーバプログラム |
| ------------------------------------------------------ | ----- | -------- |
| 日本語                                                    | Wnn   | jserver  |
| [簡体字](https://ja.wikipedia.org/wiki/簡体字 "wikilink")中国語 | cWnn  | cserver  |
| [繁体字](../Page/繁体字.md "wikilink")中国語                    | tWnn  | tserver  |
| 韓国語                                                    | kWnn  | kserver  |

Wnnの各言語版

## バージョン

### ワークステーション向け

  - Wnn6
    1998年発表。辞書を大幅に拡充し「FI(Flexible Intelligence)変換」技術により変換率を向上させ、UNIXと[Windowsで商品化された](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")\[2\]。
  - Wnn7
    2001年発表。「入力効率の向上」をコンセプトとした機能強化が行われ、入力予測、連想変換、逆引変換、入力補正などの新機能が追加された\[3\]。
  - Wnn8
    2005年発表。入力予測機能の強化、[IIIMF](https://ja.wikipedia.org/wiki/IIIMF "wikilink")対応、[Unicode](../Page/Unicode.md "wikilink")/[JIS X 0213対応などが行われた](../Page/JIS_X_0213.md "wikilink")。2009年に[エムズソリューション](https://ja.wikipedia.org/wiki/エムズソリューション "wikilink")からLinuxディストリビューション「Ubuntu」向けにカスタマイズした「Wnn8 for Ubuntu」も発売されている。
  - FreeWnn
    Wnn4.2をベースにフリーなライセンスを維持したもの\[4\]。

これ以外にOpenWnnなど各種バージョンが存在する。

### 組込機器向け

  - モバイルWnn
    変換エンジン49KB、基本辞書＋付属語＋辞書インデックス（以下「基本辞書その他」と記載）510KB\[5\]。
    連文節変換や頻度学習は備えているものの[入力予測](https://ja.wikipedia.org/wiki/入力予測 "wikilink")には非対応。単語追加はユーザー辞書登録もしくはオプション辞書追加による。
  - ミニWnn
    変換エンジン11KB、基本辞書その他197KB\[6\]。
    メモリに制約のある機器でも搭載可能なようにコンパクトさを志向したバージョン。単文節変換のみに対応しており、辞書学習も行わない。基本辞書の収録語数も最小限に抑えられている。オプション辞書により単語追加は可能だが、ユーザー辞書登録は不可能。
  - モバイルWnn V2
    変換エンジン103KB、基本辞書その他529KB\[7\]。
    モバイルWnnの機能に加え、入力予測や文脈変換、学習性能の向上が行われている。ただ基本辞書サイズはさほど変わらず、[ATOK](../Page/ATOK.md "wikilink")その他と比較して変換精度は劣っていた\[8\]。
  - Advanced Wnn
    変換エンジン113KB、基本辞書3.359MB\[9\]。
    入力予測と変換を一体化させ、変換効率を高めている。口語表現にも対応するようになった。
  - Advanced Wnn V2
    変換エンジン168KB、基本辞書4.2MB\[10\]。
    より形態素解析の性能を改良し、また着信メール内の単語を自動もしくは手動で学習する機能が搭載された。多言語対応した「マルチリンガル Advanced Wnn」もある。
  - iWnn
    変換エンジン280KB、基本辞書4.4MB\[11\]。
    "i"は***i**ntelligent・**i**ndividual・**i**ntegrated・**i**nternational*の4つのiに由来する。文脈や現在の日時から時制や季節を判断する機能、[ワイルドカードにより予測候補を絞り込む機能](../Page/ワイルドカード_\(情報処理\).md "wikilink")（[インクリメンタルサーチ](../Page/インクリメンタルサーチ.md "wikilink")）、多言語対応などAdvanced Wnnと比較して大幅な機能向上が行われている。
  - OpenWnn
    iWnnを[Apache v2ライセンスでオープンソース化したもの](../Page/Apache_License.md "wikilink")。Android Open Source Project上で公開されている\[12\]。

[携帯電話](../Page/携帯電話.md "wikilink")では、[三洋電機](../Page/三洋電機.md "wikilink")（鳥取三洋電機→[三洋電機コンシューマエレクトロニクス](https://ja.wikipedia.org/wiki/三洋電機コンシューマエレクトロニクス "wikilink")を含む）、[京セラ](../Page/京セラ.md "wikilink")、[パナソニック モバイルコミュニケーションズ](../Page/パナソニック_モバイルコミュニケーションズ.md "wikilink")、[シャープ](../Page/シャープ.md "wikilink")（2010年以降発売の機種）、[ソニーモバイルコミュニケーションズ](../Page/ソニーモバイルコミュニケーションズ.md "wikilink")（[POBox](../Page/POBox.md "wikilink")との組み合わせ）、[米国](https://ja.wikipedia.org/wiki/アメリカ合衆国 "wikilink")[モトローラ](../Page/モトローラ.md "wikilink")、[韓](../Page/大韓民国.md "wikilink")[サムスン電子](../Page/サムスン電子.md "wikilink")の製品にWnnシリーズが組み込まれている。

特に[NTTドコモ](https://ja.wikipedia.org/wiki/NTTドコモ "wikilink")の[FOMA](../Page/FOMA.md "wikilink")共通[プラットフォームである](../Page/プラットフォーム_\(コンピューティング\).md "wikilink")[オペレータパック](https://ja.wikipedia.org/wiki/オペレータパック "wikilink")(OPP)には標準でiWnnが採用され、それまでATOKを採用していた[富士通](../Page/富士通.md "wikilink")（現・[富士通モバイルコミュニケーションズ](https://ja.wikipedia.org/wiki/富士通モバイルコミュニケーションズ "wikilink")）、[ケータイShoinを採用していたシャープの機種でもiWnnが採用されるようになった](https://ja.wikipedia.org/wiki/FSKAREN "wikilink")。またソニー・エリクソンの機種では初期にはWnnの辞書部分のみを提供しており、その後基幹部分も含め搭載された。iWnnが搭載されるようになってからもPOBox Proの機能が優先となるためiWnnの機能に対応するのは比較的遅い。例えばワイルドカード予測に対応したのはiWnnの発表から約3年が経過した2011年に発売された[S006](https://ja.wikipedia.org/wiki/S006 "wikilink")搭載のPOBox Pro 5.0Eからだった\[13\]。

[ゲーム機](../Page/ゲーム機.md "wikilink")、[テレビ（プラズマ・液晶）](../Page/薄型テレビ.md "wikilink")、[DVDレコーダー](../Page/DVDレコーダー.md "wikilink")に組み込まれる例も見られる。例えば[ニンテンドー3DS](https://ja.wikipedia.org/wiki/ニンテンドー3DS "wikilink")（[任天堂](../Page/任天堂.md "wikilink")）では日本語入力システムがそれまでの[ニンテンドーDSブラウザー](../Page/ニンテンドーDSブラウザー.md "wikilink")で用いられていたATOKからiWnnに変更されている。

## 搭載機器

詳しくは外部リンクのオムロンソフト公式サイトにある各バージョンの「搭載商品」を参照のこと。

### フィーチャーフォン・PHS

  - **iWnn**
      - NTTドコモ
          - [P-07A](https://ja.wikipedia.org/wiki/P-07A "wikilink")、[P-08A](https://ja.wikipedia.org/wiki/P-08A "wikilink")、[P-09A](https://ja.wikipedia.org/wiki/P-09A "wikilink")、[N-04B](https://ja.wikipedia.org/wiki/N-04B "wikilink")、[F-06B](https://ja.wikipedia.org/wiki/F-06B "wikilink") 、[SH-07B](https://ja.wikipedia.org/wiki/SH-07B "wikilink")、[SH-11C](https://ja.wikipedia.org/wiki/SH-11C "wikilink")、[P-04C](https://ja.wikipedia.org/wiki/P-04C "wikilink")、[P-05C](https://ja.wikipedia.org/wiki/P-05C "wikilink")、[P-06C](https://ja.wikipedia.org/wiki/P-06C "wikilink")、[F-09C](https://ja.wikipedia.org/wiki/F-09C "wikilink")、[F-10C](https://ja.wikipedia.org/wiki/F-10C "wikilink")、[F-11C](https://ja.wikipedia.org/wiki/F-11C "wikilink")、[N-05C](https://ja.wikipedia.org/wiki/N-05C "wikilink")、[P-01D](https://ja.wikipedia.org/wiki/P-01D "wikilink")、[F-01E](https://ja.wikipedia.org/wiki/F-01E "wikilink")、[N-01E](https://ja.wikipedia.org/wiki/N-01E "wikilink")、[P-01E](https://ja.wikipedia.org/wiki/P-01E "wikilink")、[SH-03E](https://ja.wikipedia.org/wiki/SH-03E "wikilink")、[F-06D](https://ja.wikipedia.org/wiki/F-06D "wikilink") Girls'
      - [au](../Page/Au_\(携帯電話\).md "wikilink")（[KDDI](../Page/KDDI.md "wikilink")／[沖縄セルラー電話](../Page/沖縄セルラー電話.md "wikilink")、[iida](https://ja.wikipedia.org/wiki/iida "wikilink")ブランドを含む）
          - [W62K](../Page/W62K.md "wikilink")、[W63K](../Page/W63K.md "wikilink")、[W65K](https://ja.wikipedia.org/wiki/W65K "wikilink")、[安心ジュニアケータイ K001（KY001）](https://ja.wikipedia.org/wiki/K001 "wikilink")、[ベルトのついたケータイ NS01（KYX01）](https://ja.wikipedia.org/wiki/NS01 "wikilink")、[misora](https://ja.wikipedia.org/wiki/misora "wikilink")（KYX02）、[K002](https://ja.wikipedia.org/wiki/K002 "wikilink")（KY002）、[簡単ケータイ K003（KY003）](https://ja.wikipedia.org/wiki/K003 "wikilink")、[E07K](https://ja.wikipedia.org/wiki/E07K "wikilink")、[PRISMOID](https://ja.wikipedia.org/wiki/PRISMOID "wikilink")（KYX03）、[lotta](https://ja.wikipedia.org/wiki/lotta "wikilink")（KYX04）、[簡単ケータイ K004（KY004）](https://ja.wikipedia.org/wiki/K004 "wikilink")、[mamorino（KYY01）](https://ja.wikipedia.org/wiki/Mamorino "wikilink")（漢字入力には非対応）、[簡単ケータイ K005（KY005）](https://ja.wikipedia.org/wiki/K005 "wikilink")、[K006](https://ja.wikipedia.org/wiki/K006 "wikilink")（KY006）、[簡単ケータイ K008（KY008）](https://ja.wikipedia.org/wiki/K008 "wikilink")、[簡単ケータイ K010（KY010）](https://ja.wikipedia.org/wiki/K010 "wikilink")、[SH009](https://ja.wikipedia.org/wiki/SH009 "wikilink")、[SH010](https://ja.wikipedia.org/wiki/SH010 "wikilink")、[SH011](https://ja.wikipedia.org/wiki/SH011 "wikilink")
      - [ソフトバンクモバイル](https://ja.wikipedia.org/wiki/ソフトバンクモバイル "wikilink")
          - [PANTONE3 001SH](https://ja.wikipedia.org/wiki/SoftBank_001SH "wikilink")、[002SH](https://ja.wikipedia.org/wiki/SoftBank_002SH "wikilink")、[004SH](https://ja.wikipedia.org/wiki/SoftBank_004SH "wikilink")
      - [ウィルコム](../Page/ウィルコム.md "wikilink")
          - [WX09K](https://ja.wikipedia.org/wiki/WX09K "wikilink")、[WX05K](https://ja.wikipedia.org/wiki/WX05K "wikilink")、[WX01K](https://ja.wikipedia.org/wiki/WX01K "wikilink")、 [WX340K](https://ja.wikipedia.org/wiki/WX340K "wikilink")、[BAUM](https://ja.wikipedia.org/wiki/BAUM "wikilink")、HONEY BEE 3([WX333K](https://ja.wikipedia.org/wiki/WX333K "wikilink"))、HONEY BEE BOX([WX334K](https://ja.wikipedia.org/wiki/WX334K "wikilink"))、HONEY BEE 4([WX350K](https://ja.wikipedia.org/wiki/WX350K "wikilink"))
  - **Advanced Wnn V2.3**
  - **Advanced Wnn V2 EX Pro**
      - au（KDDI／沖縄セルラー電話）
          - [W53K](../Page/W53K.md "wikilink")、[W61K](../Page/W61K.md "wikilink")、[W64K](../Page/W64K.md "wikilink")
  - **Advanced Wnn V2 EX**
      - au（KDDI／沖縄セルラー電話）
          - [W44K II](../Page/W44K.md "wikilink")/K、[W51K](../Page/W51K.md "wikilink")、[MEDIA SKIN](../Page/MEDIA_SKIN.md "wikilink")（W52K）
  - **Advanced Wnn V2.1**
      - NTTドコモ
          - [P902iS](../Page/P902iS.md "wikilink")、[P903i](../Page/P903i.md "wikilink")
      - au（KDDI／沖縄セルラー電話）
          - [W43K](../Page/W43K.md "wikilink")
  - **Advanced Wnn α**（変換辞書が以前の8倍になった\[14\]）
      - NTTドコモ
          - [SA702i](../Page/SA702i.md "wikilink")
      - au（KDDI／沖縄セルラー電話）
          - [W33SA II](../Page/W33SA.md "wikilink")、[W43SA](../Page/W43SA.md "wikilink")、[W51SA](../Page/W51SA.md "wikilink")、[W52SA](../Page/W52SA.md "wikilink")、[W53SA](../Page/W53SA.md "wikilink")、[INFOBAR2](https://ja.wikipedia.org/wiki/INFOBAR2 "wikilink")（W55SA）、[W62SA](../Page/W62SA.md "wikilink")
  - **Advanced Wnn V2**
      - NTTドコモ
          - [SA700iS](../Page/SA700iS.md "wikilink")、[SA800i](../Page/SA800i.md "wikilink")、[P903i](../Page/P903i.md "wikilink")
      - au（KDDI／沖縄セルラー電話）
          - [W22SA](../Page/W22SA.md "wikilink")、[W31SA](../Page/W31SA.md "wikilink")、[W41K](../Page/W41K.md "wikilink")、[W42K](../Page/W42K.md "wikilink")
      - ウィルコム
          - [WX310K](../Page/WX310K.md "wikilink")
  - **Advanced Wnn 1.31**
      - ウィルコム
          - [9(nine)](../Page/WS009KE.md "wikilink")、[9(nine)+](../Page/WS009KE.md "wikilink")、[WILLCOM 9](../Page/WS018KE.md "wikilink")、[WILLCOM LU](https://ja.wikipedia.org/wiki/WS023T "wikilink")
  - **Advanced Wnn V1.22**
      - ウィルコム
          - [WX320T](../Page/WX320T.md "wikilink")
  - **Advanced Wnn V1.2**
      - ウィルコム
          - [WX310J](../Page/WX310J.md "wikilink")、[WX310SA](../Page/WX310SA.md "wikilink")
  - **Advanced Wnn V1**
  - **モバイルWnn V2**
  - **モバイルWnn V1**

### スマートフォン・スマートブック

  - **iWnn IME**
      - NTTドコモ
          - [HTC](../Page/HTC_\(企業\).md "wikilink")、[シャープ](../Page/シャープ.md "wikilink")(iWnn SH editionとして)、[ソニーモバイルコミュニケーションズ](../Page/ソニーモバイルコミュニケーションズ.md "wikilink")([POBox Touchの変換エンジンとして](../Page/POBox.md "wikilink"))、[パナソニック](https://ja.wikipedia.org/wiki/パナソニック "wikilink")(フィットキーとして)、[サムスン電子](../Page/サムスン電子.md "wikilink")(samsung日本語キーパッドとして)、[LGエレクトロニクス](../Page/LGエレクトロニクス.md "wikilink")(LG日本語キーボードとして)
      - au（KDDI／沖縄セルラー電話）
          - [HTC](../Page/HTC_\(企業\).md "wikilink")、[シャープ](../Page/シャープ.md "wikilink")(iWnn SH editionとして)、[ソニーモバイルコミュニケーションズ](../Page/ソニーモバイルコミュニケーションズ.md "wikilink")([POBox Touchの変換エンジンとして](../Page/POBox.md "wikilink"))、[パナソニック](https://ja.wikipedia.org/wiki/パナソニック "wikilink")(フィットキーとして)、[サムスン電子](../Page/サムスン電子.md "wikilink")(samsung日本語キーパッドとして)、[LGエレクトロニクス](../Page/LGエレクトロニクス.md "wikilink")(LG日本語キーボードとして)、[パンテック](https://ja.wikipedia.org/wiki/パンテック "wikilink")、[京セラ](../Page/京セラ.md "wikilink")、[モトローラ](../Page/モトローラ.md "wikilink")
      - ソフトバンクモバイル
          - [HTC](../Page/HTC_\(企業\).md "wikilink")、[シャープ](../Page/シャープ.md "wikilink")(iWnn SH editionとして)、[パナソニック](https://ja.wikipedia.org/wiki/パナソニック "wikilink")(フィットキーとして)、、[京セラ](../Page/京セラ.md "wikilink")、[モトローラ](../Page/モトローラ.md "wikilink")、[ZTE](../Page/ZTE.md "wikilink")、[DELL](https://ja.wikipedia.org/wiki/DELL "wikilink")([SoftBank 001DLのみ](https://ja.wikipedia.org/wiki/SoftBank_001DL "wikilink"))
      - NTT東日本
          - [光iフレーム](https://ja.wikipedia.org/wiki/光iフレーム "wikilink")

### タブレット

  - **iWnn IME**
      - au（KDDI／沖縄セルラー電話）
          - [XOOM](https://ja.wikipedia.org/wiki/TBi11M "wikilink")
      - [Nexus 7 (2012)](https://ja.wikipedia.org/wiki/Nexus_7_\(2012\) "wikilink")
      - チャレンジタブレット

### BD・DVDレコーダー

[パナソニック](https://ja.wikipedia.org/wiki/パナソニック "wikilink")の[DIGA](https://ja.wikipedia.org/wiki/DIGA "wikilink")にモバイルWnnが搭載されている。

## 脚注

## 外部リンク

  - [オムロンソフトウェア 文字入力技術](https://www.omronsoft.co.jp/products/product_text/)
  - [Wnn関係用語集](http://www.tomo.gr.jp/wnn/wnn-yogo.html)

[Category:日本語入力ソフト](https://ja.wikipedia.org/wiki/Category:日本語入力ソフト "wikilink") [Category:慶應義塾大学](https://ja.wikipedia.org/wiki/Category:慶應義塾大学 "wikilink") [Category:Androidのソフトウェア](https://ja.wikipedia.org/wiki/Category:Androidのソフトウェア "wikilink") [Category:1987年のソフトウェア](https://ja.wikipedia.org/wiki/Category:1987年のソフトウェア "wikilink")

1.
2.  [オムロンソフトウェア、Netscape Navigatorやメールソフトに"インライン"で日本語入力可能な「Wnn6 for Linux/BSD Ver2」を発売](http://www.omronsoft.co.jp/press/wolfv2.html)
3.  [オムロンソフトウェア、Linux対応 日本語入力システム「Wnn7 Personal」7月7日発売開始！](http://www.omronsoft.co.jp/press/wnn7_02.html)
4.  [FreeWnn](http://freewnn.sourceforge.jp/)
5.
6.
7.
8.
9.
10.
11.
12. \[git clone <https://android.googlesource.com/platform/packages/inputmethods/OpenWnn> android Git repositories\]
13.
14.
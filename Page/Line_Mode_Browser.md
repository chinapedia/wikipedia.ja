> この記事は[Line Mode Browser](https://ja.wikipedia.org/wiki/Line_Mode_Browser)から翻訳されています。


**Line Mode Browser**（ラインモードブラウザ、LMB\[1\]、www\[2\]）は、2番目に開発された[ウェブブラウザ](../Page/ウェブブラウザ.md "wikilink")\[3\]。複数の[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink")に[移植された最初のブラウザである](../Page/移植_\(ソフトウェア\).md "wikilink")\[4\]\[5\]。単純な[コマンドラインインタフェースを使用するため](../Page/キャラクタユーザインタフェース.md "wikilink")、様々なコンピュータや[端末](../Page/端末.md "wikilink")から[インターネット](../Page/インターネット.md "wikilink")にアクセスできる。1990年に開発が始まり、その後 [World Wide Web Consortium](../Page/World_Wide_Web_Consortium.md "wikilink") (W3C) が[libwww](https://ja.wikipedia.org/wiki/libwww "wikilink")[ライブラリ](../Page/ライブラリ.md "wikilink")の使用例および評価用コードとして保守してきた\[6\]。

## 歴史

[CERNでの](../Page/欧州原子核研究機構.md "wikilink") "[World Wide Web](../Page/World_Wide_Web.md "wikilink")" プロジェクトの基本的コンセプトのひとつとして「[誰でも読めること](../Page/クロスプラットフォーム.md "wikilink")」があった\[7\]。1990年、[ティム・バーナーズ＝リー](../Page/ティム・バーナーズ＝リー.md "wikilink")は既に世界初のブラウザ [WorldWideWeb](../Page/WorldWideWeb.md "wikilink") を書いていたが、このプログラムは[NeXT](../Page/NeXT.md "wikilink")製コンピュータ上でしか動作せず、NeXTのマシンはあまり普及していなかった\[8\]。[WYSIWYG](../Page/WYSIWYG.md "wikilink")エディタ機能も備えたWorldWideWeb をより一般的だがチームが不慣れな [X Window System](../Page/X_Window_System.md "wikilink") 向けに移植することは困難だった\[9\]。チームはCERNでインターンとして働いていた数学科の学生を新メンバーとし\[10\]、ウェブページの編集機能を省いた基本的なブラウザを書かせ、当時の多くのコンピュータで使えるものにしようと考えた\[11\]。Line Mode Browser という名称は、[テレタイプ端末](../Page/テレタイプ端末.md "wikilink")などの初期のコンピュータ端末でも使えるよう、文字だけを表示し、文字だけを入力するようにしたことに由来する\[12\]\[13\]。

開発は1990年11月に始まり、1990年12月には動作しはじめている\[14\]。開発には、PRIAM (PRojet Interdivisionnaire d'Assistance aux Microprocesseurs) というCERN内のマイクロプロセッサ開発を標準化するプロジェクトの機材を使った\[15\]。開発期間が短かったことの要因として、[C言語](../Page/C言語.md "wikilink")を単純化した方言を使っていた点が挙げられる。当時、標準規格である [ANSI](../Page/米国国家規格協会.md "wikilink") C はまだ全プラットフォームで利用可能という状態ではなかった\[16\]。1991年3月、[VAX](../Page/VAX.md "wikilink")、[RS/6000](../Page/System_p.md "wikilink")、[Sun-4](../Page/Sun-4.md "wikilink")というシステム向けのバージョンが一部にリリースされた\[17\]。一般公開バージョンをリリースする前に、[素粒子物理学](https://ja.wikipedia.org/wiki/素粒子物理学 "wikilink")界でよく使われている  (CERNLIB) に組み込まれている\[18\]\[19\]。最初の[ベータ版](../Page/ベータ版.md "wikilink")が1991年4月8日にリリースとなった\[20\]。1991年6月にはバーナーズ＝リーが[ネットニュース](../Page/ネットニュース.md "wikilink")の *alt.hypertext* にてこのブラウザを紹介している\[21\]\[22\]。[インターネット](../Page/インターネット.md "wikilink")経由で（世界初のウェブサーバでもある） *info.cern.ch* というマシンに[telnet](https://ja.wikipedia.org/wiki/telnet "wikilink")でログインし、誰でもこのブラウザを使うことが可能だった。1991年は [World Wide Web](../Page/World_Wide_Web.md "wikilink") のニュースが世界中に広まっていった年であり、CERNでのプロジェクトや[ドイツ](https://ja.wikipedia.org/wiki/ドイツ "wikilink")の[DESYといった研究所に世界中の注目が集まるようになった](../Page/ドイツ電子シンクロトロン.md "wikilink")\[23\]\[24\]\[25\]。

最初の安定版であるバージョン1.1は、1992年1月にリリースされた\[26\]。1992年10月にリリースされたバージョン1.21から、共通コードをライブラリ化したものを使用するようになった（このライブラリが後の[libwww](https://ja.wikipedia.org/wiki/libwww "wikilink")である）\[27\]。主要開発者であるペローは[MacWWW](https://ja.wikipedia.org/wiki/MacWWW "wikilink")プロジェクトに関与するようになり、2つのブラウザは一部[ソースコード](../Page/ソースコード.md "wikilink")が共通化されるようになった\[28\]。1993年5月の *World Wide Web Newsletter* で、バーナーズ＝リーはこのブラウザを[パブリックドメイン](../Page/パブリックドメイン.md "wikilink")とし、新規クライアントサポート作業を減らすことを発表\[29\]。1995年3月21日、バージョン3.0のリリースをもってCERNは Line Mode Browser 保守の全責任をW3Cに移管した\[30\]。Line Mode Browser と libwww は密接に結び付けられ、ブラウザ単体のリリースは1995年を最後とし、その後はlibwwwの一部とされるようになった\[31\]。

[電子メール](../Page/電子メール.md "wikilink")でウェブページをフェッチして閲覧するは、Line Mode Browser をベースとしている\[32\]。Line Mode Browser は各種OSで動作する唯一のウェブブラウザだったため、ウェブ黎明期には広く使われた。統計によれば、1994年1月から[Mosaicがウェブブラウザの状況を一変させ](../Page/NCSA_Mosaic.md "wikilink")、Line Mode Browser を使って [World Wide Web](../Page/World_Wide_Web.md "wikilink") にアクセスするユーザーは2%にまで減った\[33\]。テキストのみのウェブブラウザとしては、より柔軟性のある[Lynxが登場し](../Page/Lynx_\(ウェブブラウザ\).md "wikilink")、Line Mode Browser はほぼ役目を終えた\[34\]。その後はlibwwwの評価用アプリケーションとなっている。

## 操作モード

Line Mode Browser は単純であり、いくつかの制限がある。任意のOS上で動作するよう設計されており、いわゆる[ダム端末](../Page/ダム端末.md "wikilink")でも使える。[ユーザインタフェース](../Page/ユーザインタフェース.md "wikilink")は可能な限り単純化されている。コマンドラインインタフェースで [Uniform Resource Locator](../Page/Uniform_Resource_Locator.md "wikilink") (URL) を指定して起動する。すると要求したウェブページが[テレタイプ端末](../Page/テレタイプ端末.md "wikilink")のように1行ずつ画面に表示される。[HTMLの最初のバージョンを使ってウェブページを表示する](../Page/HyperText_Markup_Language.md "wikilink")。表示の体裁は、大文字の使用、字下げ、改行で対応している。ヘッダ要素は大文字で表示され、行の中央に字下げされ、通常のテキストとは空行を挟んで表示する\[35\]。

ナビゲーションは[マウスや](../Page/マウス_\(コンピュータ\).md "wikilink")[矢印キー](https://ja.wikipedia.org/wiki/矢印キー "wikilink")などの[ポインティングデバイス](../Page/ポインティングデバイス.md "wikilink")を使用せず、テキストコマンドを入力することで対応している\[36\]。テキスト内の各リンクには括弧で囲まれた番号が表示されており、リンクをたどるにはその番号を入力する。そのため、あるジャーナリストは「ウェブとは、番号をタイプすることで情報を探す手段である」と記事に書いていた\[37\]。空コマンド（[キャリッジ・リターン](https://ja.wikipedia.org/wiki/キャリッジ・リターン "wikilink")）を入力するとページが下に[スクロール](../Page/スクロール.md "wikilink")され、"`u`" というコマンドで上にスクロールできる。"`b`" というコマンドを入力すると閲覧履歴上の前のページに戻ることができ、新たなページを閲覧したい場合は "` g  `<http://>`...`" のようにURLを入力する\[38\]。

このブラウザはウェブページ編集機能を持たず、単に閲覧するだけである。開発者の1人[ロバート・カイリュー](../Page/ロバート・カイリュー.md "wikilink")はこれを問題とし、次のように述べている。

> 「プロジェクト全体の最大の誤りは Line Mode Browser を一般公開したことだったと今にして思う。それによってインターネット・ハッカーたちが素早くアクセスできたが、編集機能のない受動的なブラウザの観点しか提供しなかった」\[39\]

## 機能と特徴

Line Mode Browser は[クロスプラットフォーム](../Page/クロスプラットフォーム.md "wikilink")となるよう設計された。公式に移植されたプラットフォームとしては、[Apollo/Domain](https://ja.wikipedia.org/wiki/Apollo/Domain "wikilink")\[40\]、[IBM RS/6000](../Page/System_p.md "wikilink")\[41\]、[DECstation](../Page/DECstation.md "wikilink")/[Ultrix](../Page/Ultrix.md "wikilink")\[42\]、[VAX](../Page/VAX.md "wikilink")/[VMS](../Page/OpenVMS.md "wikilink")\[43\]、VAX/Ultrix\[44\]、[MS-DOS](../Page/MS-DOS.md "wikilink")\[45\]、[UNIX](../Page/UNIX.md "wikilink")\[46\]\[47\]、[Windows](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")\[48\]、[Mac OS](https://ja.wikipedia.org/wiki/Mac_OS "wikilink")\[49\]、[Linux](../Page/Linux.md "wikilink")\[50\]、[MVS](../Page/Multiple_Virtual_Storage.md "wikilink")\[51\]、[VM/CMS](https://ja.wikipedia.org/wiki/z/VM "wikilink")\[52\]、[FreeBSD](../Page/FreeBSD.md "wikilink")\[53\]、[Solaris](../Page/Solaris.md "wikilink")\[54\]、[Mac OS X](https://ja.wikipedia.org/wiki/macOS "wikilink")\[55\]がある。[File Transfer Protocol](../Page/File_Transfer_Protocol.md "wikilink") (FTP)、[Gopher](https://ja.wikipedia.org/wiki/Gopher "wikilink")、[Hypertext Transfer Protocol](../Page/Hypertext_Transfer_Protocol.md "wikilink") (HTTP)、[Network News Transfer Protocol](../Page/Network_News_Transfer_Protocol.md "wikilink") (NNTP)、[Wide Area Information Server](../Page/Wide_Area_Information_Server.md "wikilink") (WAIS) といった各種プロトコルをサポートしている\[56\]\[57\]\[58\]。

また、[rlogin](https://ja.wikipedia.org/wiki/rlogin "wikilink")\[59\]、[telnet](https://ja.wikipedia.org/wiki/telnet "wikilink")\[60\]、[ハイパーリンク](../Page/ハイパーリンク.md "wikilink")、[キリル文字](../Page/キリル文字.md "wikilink")サポート（1994年11月25日のバージョン2.15で追加）\[61\]、[プロキシ](../Page/プロキシ.md "wikilink")クライアントとしての設定\[62\]といった機能もある。[バックグラウンドプロセスとして起動してファイルのダウンロードを行うこともできる](https://ja.wikipedia.org/wiki/バックグラウンド_\(ソフトウェア\) "wikilink")\[63\]。Line Mode Browser は、[文字実体参照の解釈](../Page/文字参照.md "wikilink")、複数の空白を詰めない、テーブルとフレームのサポートなどの問題がある\[64\]。

## 脚注

## 参考文献

  -
  -
  -
  -
## 外部リンク

  - [The official Line-mode browser Website](http://www.w3.org/LineMode/)
      - [Line Mode Browser Commands](http://www.w3.org/LineMode/User/Commands.html)
      - [Quick Guide for W3C Line Mode Browser](http://www.w3.org/LineMode/User/QuickGuide.html)
      - [Defining a News Server for the Line Mode Browser](http://www.w3.org/LineMode/User/NewsServer.html)
  - [The official Libwww library Website](http://www.w3.org/Library/)
  - [Line Mode Emulator](http://www.dejavu.org/1992win.htm), Deja Vu

[Category:CERNのソフトウェア](https://ja.wikipedia.org/wiki/Category:CERNのソフトウェア "wikilink") [Category:テキストブラウザ](https://ja.wikipedia.org/wiki/Category:テキストブラウザ "wikilink") [Category:クロスプラットフォームのソフトウェア](https://ja.wikipedia.org/wiki/Category:クロスプラットフォームのソフトウェア "wikilink") [Category:1991年のソフトウェア](https://ja.wikipedia.org/wiki/Category:1991年のソフトウェア "wikilink")

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
34.
35.
36.
37.
38.
39.
40.  ログイン必要
41.
42.
43.
44.
45.
46.
47.
48.
49.
50.
51.
52.
53.
54.
55.
56.
57.
58.
59.
60.
61.
62.
63.
64.
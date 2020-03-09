> この記事は[PostScript](https://ja.wikipedia.org/wiki/PostScript)から翻訳されています。


**PostScript**（ポストスクリプト）は、[アドビシステムズ](https://ja.wikipedia.org/wiki/アドビシステムズ "wikilink")が開発している、[1984年](../Page/1984年.md "wikilink")に発表した[ページ記述言語](https://ja.wikipedia.org/wiki/ページ記述言語 "wikilink")。

[スタック](../Page/スタック.md "wikilink")指向型の[プログラミング言語](../Page/プログラミング言語.md "wikilink")で、様々な計算・処理と共に描画命令を実行することができる。事前にデータを[スタック](../Page/スタック.md "wikilink")に格納し、後の命令がデータを処理するというモデルで実行される。そのために記述法が[逆ポーランド記法](https://ja.wikipedia.org/wiki/逆ポーランド記法 "wikilink")で一貫しており、名前は「[追伸](https://ja.wikipedia.org/wiki/追伸 "wikilink")」の英語「post script」に後置記法といった意味を掛けている。

## バージョン

  - [1985年](https://ja.wikipedia.org/wiki/1985年 "wikilink") - PostScript Level 1。初期バージョン。
  - [1990年](https://ja.wikipedia.org/wiki/1990年 "wikilink") - PostScript Level 2。[日本語](../Page/日本語.md "wikilink")やカラー化対応。
  - [1996年](https://ja.wikipedia.org/wiki/1996年 "wikilink") - PostScript 3。PDF形式への対応。（Level 3は正式名称ではない）

## 概要

PostScriptは[1985年](https://ja.wikipedia.org/wiki/1985年 "wikilink")に[アップルコンピュータの](https://ja.wikipedia.org/wiki/アップル_\(企業\) "wikilink")[レーザープリンター](https://ja.wikipedia.org/wiki/レーザープリンター "wikilink")、[LaserWriter](https://ja.wikipedia.org/wiki/LaserWriter "wikilink")に採用された\[1\]。[モトローラ](https://ja.wikipedia.org/wiki/モトローラ "wikilink")[68000プロセッサと](https://ja.wikipedia.org/wiki/MC68000 "wikilink")1.5[メガ](https://ja.wikipedia.org/wiki/メガ "wikilink")[バイトの](https://ja.wikipedia.org/wiki/バイト_\(情報\) "wikilink")[RAMを搭載したこのプリンターは](https://ja.wikipedia.org/wiki/Random_Access_Memory "wikilink")、プリンターでありながら当時の[パーソナルコンピュータ](https://ja.wikipedia.org/wiki/パーソナルコンピュータ "wikilink")と同等の計算能力を持ち、それ自身が PostScript [インタプリタ](https://ja.wikipedia.org/wiki/インタプリタ "wikilink")を実行してページを生成した。同じ年、[ライノタイプによりPostScriptを採用した](https://ja.wikipedia.org/wiki/ライノタイプ_\(企業\) "wikilink")[イメージセッタ](https://ja.wikipedia.org/wiki/イメージセッタ "wikilink")が発表された。

当時はコンピュータとプリンター間の通信速度の遅さが、印刷物の品質向上のネックになっていた。しかし、プリンター自身に高い計算能力を持たせて、プログラミング言語を実行するという大胆な発想により、一気に問題は解決された。PostScript以前は、伝統的な手法より品質が劣るとされてきた電子印刷が、一気に商業印刷のレベルでも使われるようになり、今日では当たり前になっている[DTP](https://ja.wikipedia.org/wiki/DTP "wikilink")が普及するきっかけとなった。

後に印刷以外の用途でも使われ、[ワークステーション](https://ja.wikipedia.org/wiki/ワークステーション "wikilink")である「[NeXT](https://ja.wikipedia.org/wiki/NeXT "wikilink")」は、描画エンジンとして[Display PostScriptを採用していた](https://ja.wikipedia.org/wiki/Display_PostScript "wikilink")。

今日では、パーソナルコンピュータの性能が上がると同時に、コンピュータ・プリンター間の接続速度が向上したため、個人レベルでパーソナルコンピュータにPostScriptインタプリタを搭載し、生成されたイメージをプリンターに送るということも行われる。

## 実装

ほとんどは、[レーザープリンター](https://ja.wikipedia.org/wiki/レーザープリンター "wikilink")に実装されている。「PSプリンター」と呼ばれ、[PDFベースとなった](https://ja.wikipedia.org/wiki/Quartz "wikilink")[Mac OS Xより前の](https://ja.wikipedia.org/wiki/MacOS "wikilink")[Macintosh](https://ja.wikipedia.org/wiki/Macintosh "wikilink")の標準的プリンターであり、[Windowsでも利用されることがあるが](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")、アドビシステムズへのライセンス料が高額なためか、価格が数十万 - 百万円以上と一般のレーザープリンターに比べ高価で、専らDTP用途に限られている。

[ソフトウェア](https://ja.wikipedia.org/wiki/ソフトウェア "wikilink")による実装では、アドビシステムズからライセンスを受けた[ラスターイメージプロセッサ](https://ja.wikipedia.org/wiki/ラスターイメージプロセッサ "wikilink") (RIP) が[エプソンなどいくつかのメーカーから自社製プリンターのために販売されていたが](https://ja.wikipedia.org/wiki/セイコーエプソン "wikilink")、PSプリンターの価格低下もあり、あまり普及していない。なお互換[フリーソフトウェア](https://ja.wikipedia.org/wiki/フリーソフトウェア "wikilink")として[Ghostscript](https://ja.wikipedia.org/wiki/Ghostscript "wikilink")がある。

## サンプルプログラム

以下の内容をPostScriptプリンターに送信すると、文字列「Hello World\!」が印刷される。

``` postscript
 /font /Courier findfont 24 scalefont def
 font setfont
 100 100 moveto
 (Hello World!) show
 showpage
```

以下の内容をPostScriptプリンターに送信すると、長方形と文字列が印刷される。また、テキストファイルとして保存し、Adobe Illustratorなどで開くこともできる。

``` postscript
 %!
 % macro (draw rectangle) ; usage: left top width height RRECT
 /RRECT { newpath 4 copy pop pop moveto dup 0 exch rlineto exch 0 rlineto neg 0 exch rlineto closepath pop pop } def

 100 100 100 150 RRECT
 .5 setgray
 fill

 100 300 moveto
 /Helvetica findfont
 12 scalefont
 setfont
 .5 0 .5 0 setcmykcolor
 (test string) show

 showpage
```

## 参考文献

<references/>

  -
  -
  -
## 関連項目

  - [Encapsulated PostScript (EPS)](https://ja.wikipedia.org/wiki/Encapsulated_PostScript "wikilink")
  - [Forth](../Page/Forth.md "wikilink")
  - [Portable Document Format (PDF)](https://ja.wikipedia.org/wiki/Portable_Document_Format "wikilink")
  - [ラスターイメージプロセッサ](https://ja.wikipedia.org/wiki/ラスターイメージプロセッサ "wikilink")
  - [NeWS](https://ja.wikipedia.org/wiki/NeWS "wikilink")
  - [PostScriptフォント](https://ja.wikipedia.org/wiki/PostScriptフォント "wikilink")
  - [追伸](https://ja.wikipedia.org/wiki/追伸 "wikilink") - 名称の語源
  - [ページ記述言語](https://ja.wikipedia.org/wiki/ページ記述言語 "wikilink")
  - [Scalable Vector Graphics (SVG)](https://ja.wikipedia.org/wiki/Scalable_Vector_Graphics "wikilink") - 他のベクタ形式の画像フォーマット
  - [Windows Metafile (WMF, EMF)](https://ja.wikipedia.org/wiki/Windows_Metafile "wikilink") - 他のベクタ形式の画像フォーマット

## 外部リンク

  - [Adobe Printing Technologies -About PostScript 3](http://www.adobe.com/jp/print/postscript/)（アドビシステムズ）
  - [Adobe PostScript language specifications](http://partners.adobe.com/public/developer/ps/index_specs.html)（アドビシステムズ, 英語）
  - [How to Edit PostScript](http://wwwnucl.ph.tsukuba.ac.jp/~inakura/ps/postscript.html)（日本語）
  - [PostScript実習マニュアル](http://tutorial.jp/graph/ps/psman.pdf) (PDF)

[Category:PostScript](https://ja.wikipedia.org/wiki/Category:PostScript "wikilink") [Category:ページ記述言語](https://ja.wikipedia.org/wiki/Category:ページ記述言語 "wikilink") [Category:アドビシステムズ](https://ja.wikipedia.org/wiki/Category:アドビシステムズ "wikilink") [Category:オープンフォーマット](https://ja.wikipedia.org/wiki/Category:オープンフォーマット "wikilink") [Category:ベクターグラフィックス](https://ja.wikipedia.org/wiki/Category:ベクターグラフィックス "wikilink")

1.   大塚商会|url=[https://www.otsuka-shokai.co.jp/media/it-history/chapter001/postscript-1.html|website=www.otsuka-shokai.co.jp|accessdate=2019-11-06|language=ja](https://www.otsuka-shokai.co.jp/media/it-history/chapter001/postscript-1.html%7Cwebsite=www.otsuka-shokai.co.jp%7Caccessdate=2019-11-06%7Clanguage=ja)}}
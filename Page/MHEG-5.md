> この記事は[MHEG-5](https://ja.wikipedia.org/wiki/MHEG-5)から翻訳されています。


**MHEG-5** は、[マルチメディア](../Page/マルチメディア.md "wikilink")情報の表現に関する国際標準であり、[ISOと](https://ja.wikipedia.org/wiki/国際標準化機構 "wikilink")[IECの合同委員会](../Page/国際電気標準会議.md "wikilink") [ISO/IEC JTC 1](https://ja.wikipedia.org/wiki/ISO/IEC_JTC_1 "wikilink")/SC 29/WG 12 （Multimedia and Hypermedia Experts Group … MHEG) により、 **ISO/IEC 13522-5** として規格化されたものである。日本の対応規格は**JIS X 4345**。[双方向番組](../Page/双方向番組.md "wikilink")サービスを記述する言語として主に使われている。

## 特徴

MHEG-5 は[オブジェクト指向](../Page/オブジェクト指向.md "wikilink")/[宣言型プログラミング](../Page/宣言型プログラミング.md "wikilink")言語であり、テキスト、画像、動画の提示方法を記述するのに使われる。MHEG-5 アプリケーションは、複数の「シーン; scene」から成り、ユーザーはシーン間を移動するような形となる。それぞれのシーンは、表示すべきテキストやグラフィックの要素のリストと事前定義された[イベントへの反応として実行すべき](../Page/イベント駆動型プログラミング.md "wikilink")[手続きコードから構成される](https://ja.wikipedia.org/wiki/プロシージャ "wikilink")。イベントとしては、キーの押下、タイマのタイムアウト、コンテンツのメモリへのロード完了などがある。コードは「基本動作; elementary actions」を要素とする。基本動作としては、テキスト[オブジェクトで表示されるテキストを変更する動作](../Page/オブジェクト_\(プログラミング\).md "wikilink")、ビデオクリップの再生を開始する動作などがある。

MHEG-5 には、アプリケーション開発者が利用可能なクラス階層が存在する。[オブジェクト指向プログラミング](../Page/オブジェクト指向プログラミング.md "wikilink")言語とは異なり、新たなクラスを定義することはできない。標準では、MHEG アプリケーション表現を2種類定義している。1つはテキスト表現であり、もう1つは [ASN.1](../Page/Abstract_Syntax_Notation_One.md "wikilink") による表現である。アプリケーションは通常、テキスト表現で書かれ、MHEGエンジンによって ASN.1 に符号化される。

MHEG-5 は、[双方向番組](../Page/双方向番組.md "wikilink")サービスなどのプログラミングに向いている。

## プロファイル

MHEG-5 言語自体は、単なる言語である。特定のコンテキストで利用するには、言語を[プロファイル化する必要がある](https://ja.wikipedia.org/wiki/プロファイル_\(工学\) "wikilink")。

[イギリス](https://ja.wikipedia.org/wiki/イギリス "wikilink")および[ニュージーランド](../Page/ニュージーランド.md "wikilink")では、MHEG-5 はデジタルテレビの[双方向番組](../Page/双方向番組.md "wikilink")サービスを提供するのに使われている。イギリスでの Freeview プラットフォームのコンテキストにおける MHEG-5 の使い方は、UK Profile of MHEG-5 として規定されている。同様の規定はニュージーランドにもある。

香港では、[無綫電視](../Page/無綫電視.md "wikilink")がデジタル放送チャンネルでの双方向サービスに MHEG-5 ミドルウェアを選択した\[1\]。

MHEG-5 言語の放送プロファイルは[ETSIにより](../Page/欧州電気通信標準化機構.md "wikilink")、ETSI standard ES 202 184 として標準化されている。

日本では、[BSデジタルのデータ放送での採用が検討されたが](https://ja.wikipedia.org/wiki/日本における衛星放送#BSデジタル "wikilink")、結局採用されなかった。

## 関連項目

  - [MHP](../Page/Multimedia_Home_Platform.md "wikilink") - 競合する規格

## 脚注

## 外部リンク

  - [MHEG 公式サイト](http://www.mheg.org)
  - [IMPALA (International MHEG Promotion Alliance)](http://www.impala.org)
  - [Hello World in MHEG-5](http://www.digvid.info/mheg5/hello_world.php)
  - [ASN.1 encoder/decoder + source code](http://lionet.info/asn1c/download.html)
  - [Open Source MHEG-5 engine for Linux](http://redbutton.sourceforge.net/)

[Category:ISO/IEC標準](https://ja.wikipedia.org/wiki/Category:ISO/IEC標準 "wikilink") [Category:ITU-T勧告](https://ja.wikipedia.org/wiki/Category:ITU-T勧告 "wikilink") [Category:テレビ](https://ja.wikipedia.org/wiki/Category:テレビ "wikilink") [Category:プログラミング言語](https://ja.wikipedia.org/wiki/Category:プログラミング言語 "wikilink")

1.  [MHEG-5 A Must To Enjoy “TVB Interactive” Services](http://www.tvb.com/affairs/faq/press/20071128_e.html)
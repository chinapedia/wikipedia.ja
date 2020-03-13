> この記事は[CMOS](https://ja.wikipedia.org/wiki/CMOS)から翻訳されています。


**CMOSイメージセンサ**（シーモスイメージセンサ、）は[CMOS](../Page/CMOS.md "wikilink")を用いた[固体撮像素子](../Page/固体撮像素子.md "wikilink")。[CCDイメージセンサ](../Page/CCDイメージセンサ.md "wikilink")と同様に、[フォトダイオード](../Page/フォトダイオード.md "wikilink")(PD)を使用するが、製造プロセスと信号の読み出し方法が異なる\[1\]。 [Matrixw.jpg](https://ja.wikipedia.org/wiki/File:Matrixw.jpg "fig:Matrixw.jpg")

## 歴史

CMOSイメージセンサの原理が考案されたのは[1960年代](../Page/1960年代.md "wikilink")後半と古いが、実用化されたのは半導体微細加工技術が高度化した[1990年代](../Page/1990年代.md "wikilink")以降である。既存のCMOS半導体の製造プロセスを流用できるため、専用の製造ラインを必要とする[CCDイメージセンサ](../Page/CCDイメージセンサ.md "wikilink")と比較して廉価ではあるものの長らく画質において画素間のばらつきがあるため[CCDイメージセンサ](../Page/CCDイメージセンサ.md "wikilink")の後塵を拝していたが、近年では補正する技術が発展しており、画質においても遜色ないどころか凌駕する製品が増えつつある\[2\]。

## 特徴

[thumb](https://ja.wikipedia.org/wiki/ファイル:CMOS_Image_Sensor_Mechanism_Illustration.svg "wikilink") [thumb](https://ja.wikipedia.org/wiki/ファイル:Equivalent_circuit_of_CMOS_Image_Sensor_pixel.png "wikilink")

単位セルごとに増幅器を持つことで、光変換された電気信号の読み出しによる電気[ノイズ](../Page/ノイズ.md "wikilink")の発生が抑えられるという特徴を持つ。CMOSロジック[LSI](https://ja.wikipedia.org/wiki/LSI "wikilink")製造プロセスの応用で大量生産が可能なため、高電圧アナログ回路を持つ[CCDイメージセンサ](../Page/CCDイメージセンサ.md "wikilink")と比較して安価であり、素子が小さいことから消費電力も少なく、原理的に[スミア](../Page/スミア.md "wikilink")や[ブルーミングが発生しないという長所がある](https://ja.wikipedia.org/wiki/スミア#ブルーミング "wikilink")。数百MHzでの高速読み出しも行なえる。

また、ロジック回路を同一製造プロセスで組み込めることから、画像処理回路をオンチップ化して画像認識デバイス、人工視覚デバイスへの応用が研究されており、一部は商用化されている（人工網膜チップとも呼ばれることがある）。

イメージセンサをピクセルごとに3層を積層し、光の波長による透過の違いを利用してRGBを分別する[Foveon X3も存在する](https://ja.wikipedia.org/wiki/Foveon_X3 "wikilink")。

## 弱点

CCDに対してメリットのある反面、低照度状況では素子そのものが不安定になりやすく、撮影した画像にはノイズが多くなる傾向がある。また、画素毎に固定した増幅器が割り当てられるため、各増幅器の特性差により固定パターンのノイズを持つ性質があり、これを補正する回路が必要になる。近年ではPDの高出力化・低雑音化、PDから増幅器への電荷転送効率の向上、PDの受光面積を相対的に拡大するための[トランジスタ](../Page/トランジスタ.md "wikilink")の複数画素間での共用化、裏面照射型イメージセンサーの民生化など、さまざまな改良により、一般向け[カムコーダ](../Page/カムコーダ.md "wikilink")他、特定の分野においては[S/N比](https://ja.wikipedia.org/wiki/S/N比 "wikilink")がCCDイメージセンサーを凌駕するほどに向上してきた。

電荷化を同時に行えないという構造上、高速に動くものを撮影したときに進行方向に向かって像が歪んだり、ストロボのようなごく短時間の発光があると画像の垂直方向に明暗ができてしまう問題（ローリングシャッター現象\[3\]）がある。この問題には、読み出し速度を向上させること\[4\]\[5\]で改善されている。

## 用途

CMOSイメージセンサはCCDイメージセンサに比べるとより汎用の半導体製造装置を流用できることから、基本的にCCDイメージセンサと比べたときに供給価格が安い。そのため安価なデジタルスチルカメラや[デジタルビデオカメラの分野で盛んに使用され](../Page/ビデオカメラ.md "wikilink")、高価格帯の機器では1980年代～1990年代前半に[日立製作所](../Page/日立製作所.md "wikilink")のビデオカメラで採用されるなど極めて少数派であった。

一方、[ビデオチャットなどで用いられるいわゆる](https://ja.wikipedia.org/wiki/インターネット電話 "wikilink")[Webカメラ](../Page/Webカメラ.md "wikilink")や、携帯電話のカメラはそのほとんどがCMOSを搭載しており、[矢野経済研究所](https://ja.wikipedia.org/wiki/矢野経済研究所 "wikilink")の調査によると[携帯電話](../Page/携帯電話.md "wikilink")へのカメラ機能搭載が普及したこともあり、2004年にはCCDイメージセンサを出荷個数で抜いたとされる\[6\]。

CCDに対して消費電力が少ないことから、近年ではデジタル一眼レフカメラに使われる事が多くなっている。[キヤノン](https://ja.wikipedia.org/wiki/キヤノン "wikilink")は他社での生産に頼ることになるCCDイメージセンサーに対し、自社で開発・製造が可能なCMOSイメージセンサーを2004年春以降デジタル一眼レフの全機種で採用している。また、[ニコン](../Page/ニコン.md "wikilink")や[ソニー](../Page/ソニー.md "wikilink")のデジタル一眼レフでもそれぞれ自社製のCMOSを全面的に採用している。また、ソニーやキヤノンは民生用の小型[HDビデオカメラなどにもCMOSイメージセンサを採用している](https://ja.wikipedia.org/wiki/1080i "wikilink")。

## 新たな技術

### BSI(裏面照射)

2009年当時は[シリコン](https://ja.wikipedia.org/wiki/シリコン "wikilink")基板上に作りこんだ[フォトダイオード](../Page/フォトダイオード.md "wikilink")はその上面に配線層が位置しているため光の有効利用が阻害されていた。これは、[開口率](https://ja.wikipedia.org/wiki/開口率 "wikilink")の問題というよりも斜めから入射する光が配線層の壁で遮蔽されてフォトダイオードまで届かない、まるで深い井戸の底に位置するフォトダイオード受光面を光で照らすような構造になっているためである。この問題はコンパクトカメラのようなダイオードピッチの狭い小さな撮像素子で顕著になる。この構造を改め、シリコン基板の裏面を研磨して薄くし、裏面から受光する構造をもつ**BSI**（裏面照射\[7\]\[8\]）技術を採用したCMOSイメージセンサ製品\[9\]が登場した。[ソニー](../Page/ソニー.md "wikilink")と米オムニビジョン・テクノロジーズ社（製造は台湾の[TSMC](../Page/TSMC.md "wikilink") Co., Ltd.）で量産され\[10\]ている。ただし、S/Nは2倍程度まで改善するが劇的な向上ではないとしてBSI技術への移行を疑問視するメーカーもあった\[11\]。

## 製造メーカー

  - [STMicroelectronics](https://ja.wikipedia.org/wiki/:en:STMicroelectronics "wikilink")
  - [オムニビジョン](https://ja.wikipedia.org/wiki/:en:OmniVision_Technologies "wikilink")
  - [オン・セミコンダクター](https://ja.wikipedia.org/wiki/オン・セミコンダクター "wikilink")
  - [サムスン電子](../Page/サムスン電子.md "wikilink")
  - [シャープ](../Page/シャープ.md "wikilink")
  - [ソニー](../Page/ソニー.md "wikilink")
  - [パナソニック](https://ja.wikipedia.org/wiki/パナソニック "wikilink")
  - [富士フイルム](../Page/富士フイルム.md "wikilink")
  - [浜松ホトニクス](../Page/浜松ホトニクス.md "wikilink")

## 脚注

<references />

[Category:固体撮像素子](https://ja.wikipedia.org/wiki/Category:固体撮像素子 "wikilink") [Category:センサ](https://ja.wikipedia.org/wiki/Category:センサ "wikilink") [Category:デジタルカメラ](https://ja.wikipedia.org/wiki/Category:デジタルカメラ "wikilink")

1.
2.  [CCDからCMOSへ、日本が乗り遅れたセンサーのトレンド](https://news.mynavi.jp/article/machinevision-3/)
3.  [シャッター3種類の使い分けを考える](http://dc.watch.impress.co.jp/docs/review/minirepo/702512.html) , デジカメ Watch
4.  [.オリンパス、毎秒1万コマの超高速イメージセンサーを開発](http://pc.watch.impress.co.jp/docs/news/event/707814.html) , PC Watch
5.  [ソニー、フルHDで1,000fpsの撮影ができるスマホ向けCMOSイメージセンサー](http://pc.watch.impress.co.jp/docs/news/1042881.html) , PC Watch
6.  [矢野経済研究所、2004年にCMOSがCCDを出荷台数で上回ると予測](http://k-tai.impress.co.jp/cda/article/news_toppage/13525.html) , ケータイWatch
7.
8.
9.  [SONY 裏面照射型CMOSイメージセンサ Exmore R](http://www.sony.co.jp/SonyInfo/technology/technology/theme/exmor_r_01.html)
10. 日経エレクトロニクス 2008/06/30 P.11
11. 日経エレクトロニクス 2009/05/18 P.138
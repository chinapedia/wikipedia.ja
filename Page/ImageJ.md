> この記事は[ImageJ](https://ja.wikipedia.org/wiki/ImageJ)から翻訳されています。


**ImageJ**は[オープンソース](../Page/オープンソース.md "wikilink")で[パブリックドメイン](../Page/パブリックドメイン.md "wikilink")の[画像処理ソフトウェア](https://ja.wikipedia.org/wiki/画像処理ソフトウェア "wikilink")である\[1\]\[2\]。[Java](https://ja.wikipedia.org/wiki/Java "wikilink")の[仮想マシン](https://ja.wikipedia.org/wiki/仮想マシン "wikilink")上で動作し、プラグインやマクロによる拡張性が高い。科学研究における画像解析に広く利用され、生物学ではデファクト・スタンダードの解析ツールとなっている。

[デジタルカメラ](../Page/デジタルカメラ.md "wikilink")で撮影した写真などの[画像処理](https://ja.wikipedia.org/wiki/画像処理 "wikilink")に用いられる[写真編集ソフトウェア](https://ja.wikipedia.org/wiki/写真編集ソフトウェア "wikilink")では、誰でも使える直感的な操作性を重視するため、逆に内部の演算がわかりにくくなることがある。これに対してImageJでは、各種画像処理に用いられる数値計算のパラメータが分かりやすい[ユーザーインターフェイスを備えており](../Page/ユーザインタフェース.md "wikilink")、[ピクセル](../Page/ピクセル.md "wikilink")の数値を元に再現性の高い計算処理を行うことが可能である。ユーザーによって書かれたプラグイン群は、さまざまな画像処理・解析の課題に対応している（[\#拡張性](https://ja.wikipedia.org/wiki/#拡張性 "wikilink")の項を参照）。同時にその拡張性の容易さゆえ、画像処理の教育の現場でもポピュラーである\[3\]\[4\]。また、[オープンソース](../Page/オープンソース.md "wikilink")であるため、処理過程をすべて確認することができる。計算過程にブラックボックスがない、という点でも科学研究での使用に適している。[ソースコード](../Page/ソースコード.md "wikilink")は[GitHub](https://ja.wikipedia.org/wiki/GitHub "wikilink")で公開されている\[5\]。

## 動作環境

最新版v1.52\*は[Java](https://ja.wikipedia.org/wiki/Java "wikilink")1.8の[VMがくみこまれており](../Page/Java仮想マシン.md "wikilink")、その環境下で作動する。\[6\]。さまざまなOSに応じたソフトを開発サイトから無料で入手できる\[7\]。ダウンロード[アプリケーションとしての他](../Page/アプリケーションソフトウェア.md "wikilink")、[Javaアプレット](../Page/Javaアプレット.md "wikilink")としても動作する。

## 開発小史

ImageJは、[アメリカ国立衛生研究所](https://ja.wikipedia.org/wiki/アメリカ国立衛生研究所 "wikilink") (NIH) でWayne Rasbandにより開発が始められた。最初のリリースは1997年である。ImageJにはその思想的祖先としてWayne Rasbandが開発を行った[NIH Image](http://rsb.info.nih.gov/nih-image/)がある。NIH Imageの最初のリリースは1987年の春であり、[電気泳動](../Page/電気泳動.md "wikilink")のゲルのバンドを定量化することを目的としていた。開発言語は[Pascal](../Page/Pascal.md "wikilink")であった。開発のきっかけはApple Macintosh IIであり、その拡張性、[GUI](https://ja.wikipedia.org/wiki/GUI "wikilink")、グラフィックス、開発言語Pascalのサポートに刺激をうけた、とWayne Rasband自身が語っている。この草創期のNIH Imageでは、ドラム式スキャナにより画像を入力し、ジョイスティックを使って[ROI](https://ja.wikipedia.org/wiki/ROI "wikilink")の設定を行うというインターフェイスであった。

NIHImageは動作環境がMac OSのみという制約があったため、[サン・マイクロシステムズ](../Page/サン・マイクロシステムズ.md "wikilink")がJava言語をリリースしたことをきっかけとし、90年代後半にJava仮想マシン上で動作するImageJが構想されその開発が始まった。メニューの外見・構成はNIH Imageの多くを継承し、その機能も引き続き科学研究に適した特徴を有している。NIHを退職したWayne Rasbandは2015年現在でも自宅から日々開発を続行しており新たな機能を追加し続けている。

## 基本機能

1/8/16ビット整数グレースケール、32ビット浮動小数グレースケール、および24ビットRGB/32ビットRGBAカラー画像\[8\]を編集、解析、画像処理、保存、および印刷することができる。同時に処理できる画像の数は、物理メモリの搭載量およびOSのアプリケーションメモリ空間の制限に依存する。

  - [TIFF](../Page/Tagged_Image_File_Format.md "wikilink")、[PNG](../Page/Portable_Network_Graphics.md "wikilink")、[GIF](../Page/Graphics_Interchange_Format.md "wikilink")、[JPEG](../Page/JPEG.md "wikilink")、[BMP](../Page/Windows_bitmap.md "wikilink")、[DICOM](https://ja.wikipedia.org/wiki/DICOM "wikilink")、[AVIなどの](https://ja.wikipedia.org/wiki/Audio_Video_Interleave "wikilink")[画像フォーマット](https://ja.wikipedia.org/wiki/画像フォーマット "wikilink")に対応。
  - さまざまな顕微鏡メーカー、カメラメーカーの特殊な画像フォーマット (例えば[Zeiss](https://ja.wikipedia.org/wiki/Zeiss "wikilink")の.lsm、[Leica](https://ja.wikipedia.org/wiki/Leica "wikilink")の.lif) にも対応している。これらの特殊なフォーマットの対応情報は、[Loci Bioformats](http://www.openmicroscopy.org/site/support/bio-formats4/supported-formats.html)のページで確認することができる。
  - [3次元の](../Page/3次元コンピュータグラフィックス.md "wikilink")[スタック画像](https://ja.wikipedia.org/wiki/スタック画像 "wikilink") (multi-tif画像) に対応。
  - [マルチスレッド](https://ja.wikipedia.org/wiki/マルチスレッド "wikilink")処理が実装されており、複数の処理を並行して行う。特にスタック画像ではマルチコアCPUによる並列処理の威力を発揮する。
  - スタック画像の断層図の可視化。
  - ImageJはマウスによる[ROI](https://ja.wikipedia.org/wiki/ROI "wikilink") (Region of Interest) を実装している。ROIの面積、ピクセル値の統計値、形態パラメータを測定することができる。
  - [電気泳動](../Page/電気泳動.md "wikilink")ゲル写真のバンドの[濃度測定](https://ja.wikipedia.org/wiki/濃度測定 "wikilink")機能は開発当初からの機能であり、よく練られた機能のひとつとなっている。
  - ピクセル値に閾値を設定し、選択範囲を指定することができる。基本的な分節化の機能である。
  - 距離や角度の測定。
  - ピクセル値の[ヒストグラム](https://ja.wikipedia.org/wiki/ヒストグラム "wikilink")の表示
  - 任意の直線上のピクセル値の輝度分布（プロファイル）の測定とプロット。測定の数値データはファイルとして取得できる。
  - 画像間の論理演算
  - [コントラスト](https://ja.wikipedia.org/wiki/コントラスト "wikilink")増強
  - [畳み込み](https://ja.wikipedia.org/wiki/畳み込み "wikilink")
  - [フーリエ解析](https://ja.wikipedia.org/wiki/フーリエ解析 "wikilink")
  - [シャープネス](https://ja.wikipedia.org/wiki/画像編集#シャープネス "wikilink")
  - スムーズ処理
  - [エッジ検出](https://ja.wikipedia.org/wiki/エッジ検出 "wikilink")
  - メディアンフィルタ
  - スケール設定
  - 回転、反転
  - メモリの許す限り何枚でも画像を表示することができる。

より詳しい解説は[ImageJ User Guide](http://imagej.nih.gov/ij/docs/guide/index.html)を参照のこと。

## 拡張性

Java[プラグイン](../Page/プラグイン.md "wikilink")や、記録可能な[マクロによる機能拡張が可能である](https://ja.wikipedia.org/wiki/マクロ_\(コンピュータ用語\) "wikilink")。ImageJが内蔵するJava[コンパイラ](../Page/コンパイラ.md "wikilink")を用いて、撮影、解析、画像処理などのさまざまな追加機能を手軽に自作し、[プラグイン](../Page/プラグイン.md "wikilink")の形で導入できる。世界中の研究者が各自の用途に合わせて独自のプラグインを開発しており、これらの多くがImageJホームページにて公開され手軽に入手できる。優秀なプラグインは正式版の機能に加えられることも多い。

## ディストリビューション

さまざまなプラグインをあらかじめ同梱したパッケージも何種類か配布されている。なかでもメジャーなのは[Fiji(Fiji Is Just ImageJ)](http://fiji.sc)である\[9\]。ImageJのコマンドは500ほどであるが、Fijiでは900ほどになる。豊富な3次元画像解析機能の他に、プラグインの自動アップデート機能やスクリプティング機能（[JavaScript](../Page/JavaScript.md "wikilink")、Jython、JRuby、BeanShell、Clojure、ImageJ Macro）とオリジナルのエディタが特徴的である。2018年からFijiはImageJの後継となる通称ImageJ2の開発チームが融合し、事実上ImageJ2の配布プラットフォームともなった。ImageJ2はFijiのチームが開発してきたImglib2を中核としており、スクリプトやプラグインを書くことでその多様でジェネリックな機能を使用することが可能である。

## 論文への引用

ImageJを使って解析した結果・画像を論文に掲載する際には、論文に次の引用を行うことが推奨されている。ダウンロードは無料であるが、こうした形でのクレジットが助成金を得て開発を続行するために今後も必要となる。

1.  Rasband, W.S., ImageJ, U. S. National Institutes of Health, Bethesda, Maryland, USA, <http://imagej.nih.gov/ij/>, 1997-2012.
2.  Schneider, C.A., Rasband, W.S., Eliceiri, K.W. "NIH Image to ImageJ: 25 years of image analysis". Nature Methods 9, 671-675, 2012.\[10\]

## 文献・脚注

## 関連項目

  - [画像処理ソフトウェア](https://ja.wikipedia.org/wiki/画像処理ソフトウェア "wikilink")
  - [パブリックドメインソフトウェア](../Page/パブリックドメインソフトウェア.md "wikilink")

## 外部リンク

  - [配布サイト（英語）](http://rsb.info.nih.gov/ij/)
  - [ImageJ Documentation Wiki](http://imagejdocu.tudor.lu)
  - [Image J で学ぶ実践医用・バイオ画像処理](http://www.innervision.co.jp/01inner/index.html)　ImageJ入門から高次プラグイン開発テクニックまでくわしく解説している。月刊インナービジョン誌で連載中 (2020年2月3日現在、サイトが存在せず。)
  - [テクセル工房(日本語)](http://sites.google.com/site/texelcraft/) - ImageJ Windows日本語版開発とその入門マニュアル、プラグイン開発マニュアルを提供。 (2020年2月3日現在、サイトが存在せず。)
  - [株式会社リジット(日本語)](http://www.lisit.jp/1245612531124881252221830216972477322577.html)- ImageJ-Win日本語版のCD-ROMパッケージ版を販売 (2020年2月3日現在、サイトが存在せず。)
  - [ImageJ](http://hasezawa.ib.k.u-tokyo.ac.jp/zp/Kbi/ImageJ) 東京大学馳澤研究室 (2020年2月3日現在、サイトが存在せず。)
  - [『ImageJではじめる生物画像解析 （2016）』，編著：三浦耕太・塚田祐基，学研秀潤社](https://gakken-mesh.jp/book/detail/9784780909364.html)　ImageJ・Fijiのインストール、初歩的な使い方から、プラグインの開発までを解説した生物画像解析のための教科書。サポートサイトは[こちら](https://sites.google.com/site/imagejjp/)

### ImageJプラグイン配付サイト

  - [ImageJ Plugin ホーム](http://rsb.info.nih.gov/ij/plugins/index.html)

### ImageJプラグイン配付サイト (サードパーティー)

以下のリストは比較的古い内容である。これに限らず日々新しいプラグインが公表されているので、目的に応じて検索することをお勧めする。

  - [ImageJ Plugin Project](http://ij-plugins.sourceforge.net/) [SourceForge.net](https://ja.wikipedia.org/wiki/SourceForge.net "wikilink")
  - [Bio-medical Imaging plugins](http://bij.isi.uu.nl/)
  - [The Image Stabilizer plugin for ImageJ](http://www.kangli.org/code/Image_Stabilizer.html)
  - [OptiNav plugin set](http://www.optinav.com/imagej.html): Aeroacoustics, real time histograms, deconvolutions.
  - Large [set of plugins](http://www.dentistry.bham.ac.uk/landinig/software/software.html) by Gabriel Landini
  - Albert Cardona's [3D editing plugins](http://www.mcdb.ucla.edu/research/hartenstein/software/imagej/index.html).
  - Plugins for [surface assessment](http://www.gcsca.net) from GCSCA
  - [TrakEM2](http://www.ini.unizh.ch/~acardona/trakem2.html): a plugin for morphological data mining, image annotation and 3D modeling.

[Category:画像処理ソフト](https://ja.wikipedia.org/wiki/Category:画像処理ソフト "wikilink") [Category:Javaプラットフォームソフトウェア](https://ja.wikipedia.org/wiki/Category:Javaプラットフォームソフトウェア "wikilink") [Category:オープンソースソフトウェア](https://ja.wikipedia.org/wiki/Category:オープンソースソフトウェア "wikilink")

1.
2.  Collins TJ (July 2007). "ImageJ for microscopy". *BioTechniques*. **43** (1 Suppl): 25–30. [doi](https://ja.wikipedia.org/wiki/Digital_object_identifier "wikilink"):[10.2144/000112517](https://ja.wikipedia.org/wiki/doi:10.2144/000112517 "wikilink"). [PMID](https://ja.wikipedia.org/wiki/PubMed_Identifier "wikilink") [17936939](https://www.ncbi.nlm.nih.gov/pubmed/17936939)
3.  Burger W, Burge M (2007). [*Digital Image Processing: An Algorithmic Approach Using Java*](http://www.imagingbook.com/). [Springer](https://ja.wikipedia.org/wiki/Springer_Science+Business_Media "wikilink"). [ISBN](https://ja.wikipedia.org/wiki/International_Standard_Book_Number "wikilink") [1-84628-379-5](https://ja.wikipedia.org/wiki/特別:BookSources/1-84628-379-5 "wikilink").
4.  Dougherty, G (2009). [*Digital Image Processing for Medical Applications*](http://www.cambridge.org/9780521860857). [Cambridge University Press](https://ja.wikipedia.org/wiki/Cambridge_University_Press "wikilink"). [ISBN](https://ja.wikipedia.org/wiki/International_Standard_Book_Number "wikilink") [978-0-521-86085-7](https://ja.wikipedia.org/wiki/特別:BookSources/978-0-521-86085-7 "wikilink").
5.  [imagej/imagej1: Wayne Rasband's ImageJ 1.x repository, updated once a night. To develop this code, use <https://github.com/imagej/ImageJA>.](https://github.com/imagej/imagej1)
6.  [OSX上でJava1.6で作動する最新バージョンも入手可能である。](https://imagej.nih.gov/ij/download.html)
7.  [macOS](https://ja.wikipedia.org/wiki/macOS "wikilink")、[Classic Mac OS](../Page/Classic_Mac_OS.md "wikilink")、[Windows](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")、[Linux](https://ja.wikipedia.org/wiki/Linux "wikilink")、[ザウルス](../Page/ザウルス.md "wikilink")用の[インストーラ](https://ja.wikipedia.org/wiki/インストーラ "wikilink")がある。
8.  [ImageJ User Guide - IJ 1.46r | Image Types](https://imagej.nih.gov/ij/docs/guide/146-7.html)
9.  <http://www.nature.com/nmeth/journal/v9/n7/full/nmeth.2019.html>
10. Schneider CA, Rasband WS, Eliceiri KW (2012). "NIH Image to ImageJ: 25 years of image analysis". *Nat Methods*. **9** (7): 671–675. [doi](https://ja.wikipedia.org/wiki/Digital_object_identifier "wikilink"):[10.1038/nmeth.2089](https://ja.wikipedia.org/wiki/doi:10.1038/nmeth.2089 "wikilink"). [PMID](https://ja.wikipedia.org/wiki/PubMed_Identifier "wikilink") [22930834](https://www.ncbi.nlm.nih.gov/pubmed/22930834)
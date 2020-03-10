> この記事は[Utah teapot](https://ja.wikipedia.org/wiki/Utah_teapot)から翻訳されています。


[Utah_teapot_simple_2.png](https://ja.wikipedia.org/wiki/File:Utah_teapot_simple_2.png "fig:Utah_teapot_simple_2.png") **Utah teapot**（**ユタ・ティーポット**）は、[コンピュータグラフィックス](../Page/コンピュータグラフィックス.md "wikilink") (CG) の分野において標準的に使われる、[ティーポットの](https://ja.wikipedia.org/wiki/ポット "wikilink")3Dモデルである。

[1975年](../Page/1975年.md "wikilink")、[ユタ大学](https://ja.wikipedia.org/wiki/ユタ大学 "wikilink")の[マーティン・ニューウェル](https://ja.wikipedia.org/wiki/マーティン・ニューウェル "wikilink")（[Martin Newell](https://ja.wikipedia.org/wiki/:en:Martin_Newell_\(computer_scientist\) "wikilink")）によって制作された。制作者の名から、**Newell teapot**（ニューウェル・ティーポット） とも呼ばれる。

## 歴史

### 制作

[Utah_teapot_3dsmax.png](https://ja.wikipedia.org/wiki/File:Utah_teapot_3dsmax.png "fig:Utah_teapot_3dsmax.png") マーティン・ニューウェルは、グラフィックス・プログラミングのパイオニアのひとりである。1975年当時、彼は仕事で使う数学的モデルとして、適度に単純で親しみやすい物体を求めていた。自宅にあったティーポットをモデリングすることを提案したのは、彼の妻のサンドラ（Sandra Newell）である。

ニューウェルは、何枚かの方眼紙と鉛筆を持ってきて、目と手で茶器全体のモデリングの下描き\[1\]をした。それから研究所に戻って、グラフィック端末（テクトロの蓄積管（[:en:Direct-view bistable storage tube](https://ja.wikipedia.org/wiki/:en:Direct-view_bistable_storage_tube "wikilink")）を使っていた）上のエディタで、[ベジェ曲線](../Page/ベジェ曲線.md "wikilink")の制御点を手動でモデリングした（よって、実物を忠実にスキャンした形状ではない）。カップや受け皿、ティースプーンもティーポットと一緒にモデリングされたが、広く使われるようになったのはティーポットだけであった。ミルク差しもまたモデリングされたというが、そのデータは失われたようである。

### 普及

[レンダリング結果だけでなく](https://ja.wikipedia.org/wiki/レンダリング_\(コンピュータ\) "wikilink")、モデリングの数値データもニューウェルは公開したため、他のCG研究者たちの間でたちまちこのモデルが使われるようになった。ティーポットは丸みを帯び、くびれを含み、取っ手には穴が開いている（数学的には「0よりも大きな[種数](https://ja.wikipedia.org/wiki/種数 "wikilink")を持っている」）。また、自身に影を投影でき、また複雑な表面テクスチャなしに見た目もよく表示できる。こうした特性を持ち合わせた3Dモデルは、CGの実験を行うために理想的であり、多くのCG研究者たちが必要としていたためである。

ニューウェルによる元々のモデルは、ティーポットの底に面がなかった。これは、下から覗かれることを想定していなかったためである。後のバージョンで、この問題は修正されている。

その後数十年間に渡って、コンピュータグラフィックスの学術雑誌（[ACMの](../Page/Association_for_Computing_Machinery.md "wikilink")[SIGGRAPH](https://ja.wikipedia.org/wiki/SIGGRAPH "wikilink")の季刊誌など）には、さまざまな特徴のあるティーポットのCGが常に載せられていた。細かく面を刻まれたり、滑らかな影をつけられたり、ワイヤーフレームになったり、でこぼこになったり、半透明になったり、透明で内部で屈折するようになったりしたものがある。豹の皮をかぶせられて、毛皮を生やされたティーポットが作られたことさえあった。

### 現況

[CGfog.jpg](https://ja.wikipedia.org/wiki/File:CGfog.jpg "fig:CGfog.jpg") 技術の進歩にしたがって、ティーポットをレンダリングする行為は、1975年当時と違ってもはやチャレンジングなものではない。しかし、より進化したグラフィックス技術を試すためのサンプルとして、ティーポットは今でも使われ続けている。

ティーポットモデルの様々なバージョンや、それが描かれたシーンは、昨今のレンダリングやモデリングソフトと一緒に配布されていたり、自由に利用できるようになっている。例えば、[AutoCAD](https://ja.wikipedia.org/wiki/AutoCAD "wikilink")や[Lightwave 3D](https://ja.wikipedia.org/wiki/Lightwave_3D "wikilink")、[POV-Ray](../Page/POV-Ray.md "wikilink")、[OpenGL](../Page/OpenGL.md "wikilink")、[Direct3D](https://ja.wikipedia.org/wiki/Direct3D "wikilink")、[3D Studio Maxなどで利用可能である](https://ja.wikipedia.org/wiki/3D_Studio_Max "wikilink")。立方体や球などと一緒に、[GLUT](https://ja.wikipedia.org/wiki/GLUT "wikilink")は `glutSolidTeapot()` というグラフィックス関数を用意している。[Direct3D](https://ja.wikipedia.org/wiki/Direct3D "wikilink")では同様に[D3DX](https://ja.wikipedia.org/wiki/D3DX "wikilink")があり、そこで `D3DXCreateTeapot()` を用意している。OS X TigerとLeopardもまた[Quartz Composerの中にティーポットが入っているが](https://ja.wikipedia.org/wiki/Quartz_Composer "wikilink")、Lepardのティーポットは[バンプマッピング](https://ja.wikipedia.org/wiki/バンプマッピング "wikilink")をサポートしている。[BeOS](../Page/BeOS.md "wikilink")には3Dのティーポットが回転するちょっとしたデモが入っていて、マルチメディア処理に強いプラットフォームの特性を印象付けようとしている。

ティーポットが描かれているシーンは、[レンダラの自己テストと](https://ja.wikipedia.org/wiki/レンダリングエンジン "wikilink")[ベンチマーク](https://ja.wikipedia.org/wiki/ベンチマーク "wikilink")によく使われている。

## CG文化とティーポット

[Siggraph_2013_Teapot.JPG](https://ja.wikipedia.org/wiki/File:Siggraph_2013_Teapot.JPG "fig:Siggraph_2013_Teapot.JPG")で頒布された、2013年版のウォーキング・ティーポット。\]\] このポットのモデルがあまりに広く使われたため、CGに携わる者の間では一種の「内輪ネタ」的なジョークの題材としても用いられる。たとえば、3Dアニメーション映画『[トイ・ストーリー](../Page/トイ・ストーリー.md "wikilink")』では、短いお茶会のシーンにユタ・ティーポットが見られる。また、Microsoftの[Windowsに附属した](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")[スクリーンセーバー](https://ja.wikipedia.org/wiki/スクリーンセーバー "wikilink")の「パイプ」では、継ぎ目にティーポットがまぎれているのを見ることができる\[2\]。[ピクサー社は](https://ja.wikipedia.org/wiki/ピクサー・アニメーション・スタジオ "wikilink")、擬人化されたティーポットのキャラクター「ウォーキング・ティーポット」を、レンダリングソフト [RenderMan](https://ja.wikipedia.org/wiki/RenderMan "wikilink") のマスコットとしており、ぜんまい式で自走可能なウォーキング・ティーポットのモデルが、2003年以来毎年趣向を変えて限定生産されている。

1987年、Jim Arvo と David Kirk は、[レイトレーシング](../Page/レイトレーシング.md "wikilink")に関する論文 "Fast Ray Tracing by Ray Classification" \[3\] をSIGGRAPH に発表した。その付図8として掲げられた「プラトンの立体」と題された画像には、6つの石柱が描かれ、その上に5つの[正多面体](https://ja.wikipedia.org/wiki/正多面体 "wikilink")（[正四面体](../Page/正四面体.md "wikilink")、[正六面体](../Page/正六面体.md "wikilink")、[正八面体](../Page/正八面体.md "wikilink")、[正十二面体](../Page/正十二面体.md "wikilink")、[正二十面体](../Page/正二十面体.md "wikilink")）と、件のティーポットが乗せられている。この図のティーポットは**Teapotahedron**（正ティーポット体）と呼ばれ、画像はいくつかの本や学術雑誌\[4\]の表紙を飾った。

[ジム・ブリン](https://ja.wikipedia.org/wiki/ジム・ブリン "wikilink")がこの件について、IEEE CG\&A 誌 1987年11月号のコラムにジョークとして「6番めの正多面体が発見された」と書いたところ、CGに関する雑学的知識のなかった数学者から当惑の手紙が編集部に送られてきたという。体積（縮小前（後述））は、ほぼ[42だという](https://ja.wikipedia.org/wiki/生命、宇宙、そして万物についての究極の疑問の答え "wikilink")。また、ジム・ブリンは、制作に携わった数学教育用ビデオシリーズ "[Project Mathematics\!](https://ja.wikipedia.org/wiki/:en:Project_Mathematics! "wikilink")" の中の一作（1988年制作の "The Theorem of Pythagoras"）で、[ピタゴラスの定理](../Page/ピタゴラスの定理.md "wikilink")をユニークな方法で説明した。直角三角形のそれぞれの辺に2Dのティーポットを置いたとき、斜辺のティーポットの面積は他の二辺のティーポットの面積を足し合わせたものに等しいというのである。

## ティーポットの実物

[Melitta_teapot.png](https://ja.wikipedia.org/wiki/File:Melitta_teapot.png "fig:Melitta_teapot.png")製のティーポットの実物。ボストンコンピュータ博物館に展示されていた当時の写真 。\]\] モデル化されたティーポットの実物は、[メリタ](https://ja.wikipedia.org/wiki/メリタ "wikilink")社が製造したもので\[5\]、ニューウェルは1974年に[ZCMI](https://ja.wikipedia.org/wiki/ZCMI "wikilink")（[ユタ州](../Page/ユタ州.md "wikilink")[ソルトレイクシティ](../Page/ソルトレイクシティ.md "wikilink")にあるデパート）で購入した。このティーポットは1984年にボストンコンピュータ博物館に寄贈され、1990年まで展示されていた。その後、[カリフォルニア州](../Page/カリフォルニア州.md "wikilink")の[マウンテンビュー](../Page/マウンテンビュー.md "wikilink")にある[コンピュータ歴史博物館](https://ja.wikipedia.org/wiki/コンピュータ歴史博物館 "wikilink")のコレクションとなり（[エフェメラ](../Page/エフェメラ.md "wikilink")に分類されている）\[6\]、展示されている。

実物のティーポットは、我々が見慣れているコンピュータモデルよりも明らかに背が高い。これはニューウェルらの[フレームバッファ](https://ja.wikipedia.org/wiki/フレームバッファ "wikilink")が完全な正方形のピクセルを採用していなかったためであり、それに合わせたデータであったものが、他のシステムを使うユーザーがモデルを共有する際に、そのままになってしまったものとされていた。しかし、[ジム・ブリン](https://ja.wikipedia.org/wiki/ジム・ブリン "wikilink")がIEEE CG\&A誌のコラム（1987年9月）に書いたところによれば、ARPA向けにデモをした際に、彼らがY方向を0.75倍したところ、そのほうがかわいいと思ったので、以後はいつも縮小した方を使うようになったものだという。

CG\&A誌1987年1月号にティーポットの歴史について書かれた記事があるが、曲面のデータについてはジム・ブリンのコラムにあるもののほうが構造化されている。モデルは実物を忠実にディジタイズしたものではない。ジム・ブリンのコラムに掲載されているデータをY方向に1.33333333...倍（\(\tfrac{4}{3}\)倍）すれば、元のデータではキリの良い数値を使っていることがわかる。

## 参照

<references/>

  - ジム・ブリンのコラムについては単行本に再録されており、日本語版も出ている『Jim Blinn's Corner 日本語版 (1) A Trip Down the Graphics Pipeline』 ISBN 4-274-06536-7

## 外部リンク

  - [Utah teapotの画像(コンピュータ歴史博物館への直接リンク)](http://archive.computerhistory.org/resources/still-image/Teapot/src/102630883.jpg)
  - [Utah teapotの簡単な歴史](http://www.sjbaker.org/wiki/index.php?title=The_History_of_The_Teapot)
  - [Javaを使ってレンダリングしたティーポット](http://mrl.nyu.edu/~perlin/experiments/teapot/)
  - [Utah teapotのレンダリング例](http://nis-lab.is.s.u-tokyo.ac.jp/%7Enis/ourworks/tpot/tpot.htm)

[Category:コンピュータグラフィックス](https://ja.wikipedia.org/wiki/Category:コンピュータグラフィックス "wikilink") [Category:コンピュータの文化](https://ja.wikipedia.org/wiki/Category:コンピュータの文化 "wikilink")

1.  次のPDF（ <http://www.sigcis.org/files/ws2013Gaboury_Figures.pdf> ）の14頁に描かれたものがあるが、いわゆる「スケッチ」ではない。
2.  [Windows NT Easter Egg - Pipes Screensaver](http://www.eeggs.com/items/493.html)
3.  [James Arvo and David Kirk, "Fast Ray Tracing by Ray Classification", Apollo Computer Inc. ,1987](http://artis.imag.fr/Members/Cyril.Soler/DEA/Ombres/Papers/Arvo.Sig87.pdf)
4.  たとえばACMの学会誌CACMの Vol. 31, No. 2（1988年2月） <http://cacm.acm.org/magazines/1988/2> など。
5.  [Original Utah Teapot at the Computer History Museum](http://www.computerhistory.org/collections/accession/X398.84)
6.
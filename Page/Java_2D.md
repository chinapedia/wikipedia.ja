> この記事は[Java 2D](https://ja.wikipedia.org/wiki/Java_2D)から翻訳されています。


**Java 2D** は、[Java](https://ja.wikipedia.org/wiki/Java "wikilink")において[2次元コンピュータグラフィックス](https://ja.wikipedia.org/wiki/2次元コンピュータグラフィックス "wikilink")の描画に使われる[APIである](../Page/アプリケーションプログラミングインタフェース.md "wikilink")。Java 2D の描画操作は、図形を描き、それを塗りつぶし、[ディスプレイ上でその結果を合成するものと言える](../Page/ディスプレイ_\(コンピュータ\).md "wikilink")。

## 構成

Java 2D とその文書は JDK 6 の一部としてダウンロード可能である。Java 2D API クラスは JDK 6 の以下のパッケージにある。

  - *java.awt* - Java [Abstract Window Toolkit](../Page/Abstract_Window_Toolkit.md "wikilink") のメインパッケージ
  - *java.awt.geom* - 直線、楕円、四角形などの基本的2次元図形に関する標準ライブラリ
  - *java.awt.font* - [字体](https://ja.wikipedia.org/wiki/字体 "wikilink")操作のためのライブラリ
  - *java.awt.color* - 色を様々な方法で扱うためのツール群
  - *java.awt.image* - 画像を操作するためのライブラリ
  - *java.awt.image.renderable*
  - *java.awt.print* - 印刷のためのツール群

## 基本概念

以下のオブジェクト（インタフェース）は、Java 2D での描画操作に必須の部分である。

### Shape

*shape* は、太さのない境界線で内側と外側を区切ったものである。内側の[ピクセル](../Page/ピクセル.md "wikilink")は描画操作で変更され、外側は影響を受けない。

単なる直線の場合、内側が存在しないので塗りつぶしても何も変化しない。従って、直線を描きたいときは細長い[長方形](../Page/長方形.md "wikilink")を使って内側を塗りつぶす。

### Paint

*paint* は、塗りつぶし操作でピクセルに使用する[色](../Page/色.md "wikilink")を生成する。最も単純な paint は **** であり、全てのピクセルに同じ色を生成する。色の変化を伴う paint や、[画像](../Page/画像.md "wikilink")を描画する paint、任意の色の組合せを生成する paint などもある。円形の shape に黄色の塗りつぶしを施せば、黄色の円が描画される。画像を生成する paint を使って円の塗りつぶしを行えば、その画像を円形に切り取った画像が生成される。

### Composite

描画操作では、*source*（paint が生成しようとしているピクセル群）と *destination*（既に描画されたピクセル群）がある。通常、source は単に destination を上書きするが、*composite* によってその動作を変更できる。

composite に source と destination を指定すると、画面に最終的に現れる画像が生成される。典型的な composite として **** があり、描画するピクセルが半透明であるかのように扱うので、destination のピクセルもある程度見える。

### 塗りつぶし

shape を塗りつぶすとき、各ピクセルが内側なのか外側なのかを判定する必要がある。内側のピクセルは塗りつぶし操作の影響を受ける。境界線上のピクセルは、[アンチエイリアス](https://ja.wikipedia.org/wiki/アンチエイリアス "wikilink")が有効になっていれば、ある程度だけ影響を受けることになる。

paint を使って、各ピクセルに設定すべき色が生成される。単色の塗りつぶしの場合、各ピクセルには同じ色が設定される。

composite が paint によって設定された色と画面上に既にある色とを考慮し、最終的な色を決定する。

## その他のオブジェクト

以下のオブジェクトは、上述の単純なオブジェクトによる描画で必要に応じて使われる。

### Transform

Java 2D の描画操作は、[transformの対象となり](../Page/アフィン写像.md "wikilink")、回転させたり、切り取ったり、拡大・縮小したりできる。最も一般的な transform は *identity transform*であり、何もしない。

transform を使った塗りつぶしは、単に新たな変換された shape を生成し、それを塗りつぶしたように見える。

### Stroke

*fill*（塗りつぶし）操作だけでなく、Java 2D は *draw* 操作も提供している。fill では shape の内側を描画したが、draw では輪郭線を描画する。輪郭線としては、単純な実線もあれば、各線分の端が丸められた破線もある。

輪郭線を生成するオブジェクトは *stroke* である。入力として shape を与えられると、stroke はその形の輪郭線を表す shape を新たに生成する。例えば、太さのない線が stroke によって1ピクセル幅の多角形に変換されたりする。

従って、draw 操作は、 stroke を使って新たな shape を作成し、それを塗りつぶすものと言える。

技術的には、stroke は shape を入力として新たな shape を生成するためだけに必要とされる。Java 2D では輪郭線を描くために stroke が実装されているが、stroke を直接使って任意の図形を生成することも可能である。

## 最適化

概念的には、Java 2D で黒い直線を描くのは、直線の shape を生成し、現在の transform に従って変換し、stroke によって細長い四角形の shape を生成し、その shape に対してピクセル位置を問合せ、**** を使ってピクセルを生成し、composite に従ってそれを画面上に表示するという一連の動作からなる。

しかし、このようなステップを毎回実行するのは効率的でない。Java 2D では、これらのステップを省略できるような最適化を施している。塗りつぶしが単純な単色だった場合、個々のピクセルの色を問い合わせる必要はない。同様に、完全に不透明な重ね合わせの設定なら、composite 操作は不要であり、無駄である。

Java 2D は省略可能な手順は可能な限り省略して、上述の全ステップを実施したのと同じ見た目を生成する。これにより、柔軟性と高速性を両立させている。

## 出力先

以上の説明は、話を単純にするため、出力先がディスプレイであると仮定していた。しかし、実際の出力先はプリンタでも、メモリでもよいし、Java 2D のコマンドを受け取って解釈し[ベクターイメージ](https://ja.wikipedia.org/wiki/ベクターイメージ "wikilink")ファイルを生成するオブジェクトでもよい。

## Java2D と OpenGL の関係

[Java SE 6](../Page/Java_Platform,_Standard_Edition.md "wikilink") の build 51 以降、Java 2D と [OpenGL](../Page/OpenGL.md "wikilink") の連携が可能となった。例えば、ボタンのアイコンとして3次元グラフィックスのアニメーションを使うこともできる。

## 関連項目

  - [Java 3D](https://ja.wikipedia.org/wiki/Java3D "wikilink")

## 外部リンク

  - [Java 2D<sup>TM</sup>](http://sdc.sun.co.jp/java/docs/j2se/1.4/ja/docs/ja/guide/2d/index.html)、[サン・マイクロシステムズ](../Page/サン・マイクロシステムズ.md "wikilink")

[Category:API](https://ja.wikipedia.org/wiki/Category:API "wikilink") [Category:Javaプラットフォーム](https://ja.wikipedia.org/wiki/Category:Javaプラットフォーム "wikilink") [Category:グラフィックライブラリ](https://ja.wikipedia.org/wiki/Category:グラフィックライブラリ "wikilink")
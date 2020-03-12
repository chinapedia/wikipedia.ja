> この記事は[Processing](https://ja.wikipedia.org/wiki/Processing)から翻訳されています。


（プロセシング）は、（）と（）による[オープンソース](../Page/オープンソース.md "wikilink")プロジェクトであり、かつては[MITメディアラボ](../Page/MITメディアラボ.md "wikilink")で開発されていた。電子アートとビジュアルデザインのための[プログラミング言語](../Page/プログラミング言語.md "wikilink")であり、[統合開発環境](../Page/統合開発環境.md "wikilink")(GUI)である。アーティストによるコンテンツ制作作業のために、詳細な設定を行う関数を排除している。 視覚的なフィードバックが即座に得られるため、初心者が[プログラミングを学習するのに適しており](https://ja.wikipedia.org/wiki/プログラミング_\(コンピュータ\) "wikilink")、電子スケッチブックの基盤としても利用できる。 を単純化し、グラフィック機能に特化した言語といえる。

## 機能

[thumb](https://ja.wikipedia.org/wiki/ファイル:Processing-ide.png "wikilink")

にはと呼ばれる必要最小限の[IDEが含まれている](../Page/統合開発環境.md "wikilink")。

でのプログラミングでは、全ての定義されたクラスは  の内部クラスのコードとして扱われ、コンパイルされる。すなわち、クラス内の静的変数や静的メソッドは通常禁じられており、それらを使うにはユーザーが明示的に純粋モードを指定しなければならない。

GPUドライバが提供するAPIが簡略化されてProcessingのAPIとして提供されているため、高度な表現を行う場合には不便に感じやすい。例えば、OpenGLで標準的にサポートされている環境マッピングが、APIとして提供されていないため、独自に実装する必要がある等である。

作成したプログラムをアプリケーションとしてエクスポートすることができる。また、[processing.js](https://ja.wikipedia.org/wiki/processing.js "wikilink")の機能を用いればネット上でコードの実行結果が見られる。

## Examples

### Hello World

``` java
println("Hello World!");
```

上記も正しい プログラムだが、次のようなコードの方が  の雰囲気をよく表している。

``` java
text("Hello World!", 20,50);
```

### 図形を描く

``` java
rect(20, 20, 100, 80);//四角形
ellipse(140, 140, 40, 50);//楕円
```

### 日本地図の塗り分け

ウィキメディアのSVG形式の日本地図の白地図を読み込み、`Prefectures` という配列に記述された番号の県のみ塗り分けるプログラム。英語版の例のように地図データが各県ごとに `name` を持っていれば県名で指定することも可能である。

``` java
PShape japan;
float map_scale=0.25;
int square_len=512;
int [] Prefectures={2,3,5,7,11,13,17,19,23,29,31,37,41,43};  // Prime numbers

void setup() {
  japan=loadShape("http://upload.wikimedia.org/wikipedia/commons/5/56/Blank_map_of_Japan.svg");
  size(square_len,square_len);
  smooth();
  noLoop();
}

void draw() {
  background(color(0, 0, 255));  // blue
  japan.disableStyle();
  japan.getChild("ground").getChild(0).scale(map_scale);
  fill(color(255, 255, 0));  // yellow
  shape(japan.getChild("ground").getChild(0), square_len * map_scale, square_len * map_scale);
  prefecturesColoring(japan ,Prefectures , color(255, 0, 255), map_scale);  // magenta
  saveFrame("map output.png");
}

void prefecturesColoring(PShape nation, int[] prefectures, int c, float n){
  for (int i=0; i < prefectures.length; i++) {
    PShape prefecture=nation.getChild("ground").getChild(0).getChild(prefectures[i]);
    prefecture.disableStyle();  // Disable the colors found in the SVG file
    prefecture.scale(n);
    fill(c);  // Set our own coloring
    noStroke();
    shape(prefecture, square_len * map_scale, square_len * map_scale);  // Draw a single prefecture
  }
}
```

## 関連プロジェクト

から派生したプロジェクトとしてがあり、 の統合開発環境に単純化した[C言語](../Page/C言語.md "wikilink")を組み合わせて、アーティストが[マイクロコントローラ](../Page/マイクロコントローラ.md "wikilink")をプログラムできるようにするものである。 を使ったハードウェアプロジェクトとして [Arduino](https://ja.wikipedia.org/wiki/Arduino "wikilink") がある。また、フランシス・リのは、 を使って書かれたソフトウェアを  を内蔵した携帯機器上で実行させるプロジェクトである。

## 受賞

2005年、レアスとフライは  に関する業績により、[アルス・エレクトロニカ](../Page/アルス・エレクトロニカ.md "wikilink")のゴールデン・ニカ賞（ネットビジョン部門）を受賞した。

## ライセンス

統合開発環境は [GPL](../Page/GNU_General_Public_License.md "wikilink") の条件で公開されている。

アプリケーションやアプレットに含まれるライブラリコードは [LGPL](../Page/GNU_Lesser_General_Public_License.md "wikilink") の条件で提供、開発したプログラムは任意のライセンスで活用可能である。

## 名前

もともとレアスとフライは `processing.org` が取得されていたため `proce55ing.org` というドメインを用いたが、しばらくして [`processing.org`](https://Processing.org) を取得した。`proce55ing.org` から取られた p5 という略称は、名前が変わったにもかかわらずときおり用いられる。

## バージョン

  - 2008年11月24日：初のリリースバージョンである1.0がリリース。
  - 2013年6月：2.0がリリース。
  - 2015年9月：3.0がリリース。

## 関連項目

  - [Processing.js](https://ja.wikipedia.org/wiki/Processing.js "wikilink")　ブラウザ上で動かすためのJavaScriptライブラリ
  - [openFrameworks](https://ja.wikipedia.org/wiki/openFrameworks "wikilink")
  - [cinder](https://ja.wikipedia.org/wiki/:en:cinder_\(programming_library\) "wikilink")
  - [p5.js](https://ja.wikipedia.org/wiki/p5.js "wikilink")

## 外部リンク

  - [公式サイト](http://www.processing.org/)
  - [`processinghacks.com`](http://www.processinghacks.com/)
  - [](http://www.processingblogs.org/)
  - [processing.js](http://processingjs.org)
  - [p5.js.org](https://P5.js.org)

[Category:コンピュータグラフィックス](https://ja.wikipedia.org/wiki/Category:コンピュータグラフィックス "wikilink") [Category:オープンソースソフトウェア](https://ja.wikipedia.org/wiki/Category:オープンソースソフトウェア "wikilink") [Category:プログラミング言語](https://ja.wikipedia.org/wiki/Category:プログラミング言語 "wikilink") [Category:VJ](https://ja.wikipedia.org/wiki/Category:VJ "wikilink")
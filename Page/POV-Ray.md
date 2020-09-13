> この記事は[POV-Ray](https://ja.wikipedia.org/wiki/POV-Ray)から翻訳されています。


[right](https://ja.wikipedia.org/wiki/ファイル:Glasses_800_edit.png "wikilink")、[フォトンマッピング](https://ja.wikipedia.org/wiki/フォトンマッピング "wikilink")、[焦点ブラー](https://ja.wikipedia.org/wiki/焦点ブラー "wikilink")などの表現技法を使用している。\]\]

**POV-Ray**（ポヴレイ、**P**ersistence **o**f **V**ision **Ray**tracer）は、多くのコンピュータプラットフォームで利用できる[レイトレーシング](../Page/レイトレーシング.md "wikilink")[ソフトウェア](../Page/ソフトウェア.md "wikilink")。

プログラムのソースコードが一般に公開されている[オープンソース](../Page/オープンソース.md "wikilink")の3D[レンダリングエンジン](https://ja.wikipedia.org/wiki/レンダリングエンジン "wikilink")（レンダラー）の一つで、独自の[C言語](../Page/C言語.md "wikilink")風の構造化ドキュメントによりデータを入力し、マクロ関数による半自動配置ができるので、[シミュレータとしての利用も可能である](../Page/シミュレーション.md "wikilink")。また、数学的モデリングに強い。

拡張版を自由に作成、配布できるという性格から、学術的な新技法の試験実装にもよく用いられる。公式版（2013年11月現在3.7.0）の他に、v3.5に対応する複数の独自拡張版が公開されている\[1\]。v3.7からはライセンスが[AGPLv3に変更された](https://ja.wikipedia.org/wiki/GNU_Affero_General_Public_License "wikilink")。

## 歴史

1980年代、David Kirk Buckは自身の[Amiga](../Page/Amiga.md "wikilink")に[Unixの](../Page/UNIX.md "wikilink")[レイトレーシング](../Page/レイトレーシング.md "wikilink")ソフトのソースコードをダウンロードし、しばらく検証した上で、独自の[レイトレーシング](../Page/レイトレーシング.md "wikilink")ソフトを作ることを決意した。 名前は彼自身の[イニシャル](../Page/イニシャル.md "wikilink")を取ってDKBTraceと名づけ、需要を見込んで掲示板に投稿した。 1987年にAaron A. CollinsがDKBTraceをダウンロードし、[x86](https://ja.wikipedia.org/wiki/x86 "wikilink")用の開発を開始。David Buck本人と協力して他の機能の追加も行った。ソフトウェアが次第に評価を得て需要と期待が増える中、 彼らだけでは開発が存続できなくなったため、1991年7月にプログラマを集めてチームが結成された。同時にDavidはソフトウェアに自身のイニシャルを含めるのは適切でないと感じ、名前を変更することにした。 「STAR」(Software Taskforce on Animation and Rendering)という候補もあったが、結局「Persistence of Vision Raytracer」(省略形：POV-Ray)に決定した\[2\]。

## 派生レンダラー

  - MegaPOV
    POV-Ray 3.6系の非公式拡張であり、多くのパッチは既にPOV-Ray 3.7に取り込まれている\[3\]\[4\]。
  - UberPOV
    POV-Ray 3.7系の非公式拡張であり、MegaPOVの後継\[5\]\[6\]。

## POV-Ray用モデラー

  - [Blender](../Page/Blender.md "wikilink") - オープンソースの統合3DCGソフトウェア。POV-Ray用アドオンが同梱されており、それを有効にすることでPOV-Rayに対応する。POVコードの直接編集にも対応している。Blender 2.79でPOVコードの[シンタックスハイライト](../Page/シンタックスハイライト.md "wikilink")にも対応した。

### 開発停止中

  - Moray - 古くから存在するPOV-Ray用[モデラー](../Page/モデラー.md "wikilink")。2007年、POV-Rayの開発元が買収した\[7\]。開発停止中。
  - KPovModeler - KDEベースのPOV-Ray用モデラー。オープンソース。開発停止中。
  - Bishop3D - Windows専用のPOV-Ray用モデラー。アニメーションにも対応。シーン記述言語のインポートも可能。オープンソース化された。parametricサーフィス及びisosurface未対応\[8\]。
  - [Structure Synth](https://ja.wikipedia.org/wiki/Structure_Synth "wikilink") - 独自のルール記述によって3D生成を行うソフトウェア。POV-Ray形式でのエクスポートが可能。

## 機能

[right](https://ja.wikipedia.org/wiki/ファイル:PNG_transparency_demonstration_1.png "wikilink")、[屈折](../Page/屈折.md "wikilink")、[焦点ブラー](https://ja.wikipedia.org/wiki/焦点ブラー "wikilink")などの表現技法を使用している。\]\]

POV-Rayの機能は開発当初から充実していたが、近年のバージョンでは以下の機能を搭載している。

  - マクロとループを搭載した[チューリング完全](../Page/チューリング完全.md "wikilink")のSDL (scene description language)\[9\]
  - 背景、テクスチャ、オブジェクトのライブラリ
  - 多くの[幾何プリミティブ](https://ja.wikipedia.org/wiki/幾何プリミティブ "wikilink")と[Constructive Solid Geometryのサポート](https://ja.wikipedia.org/wiki/Constructive_Solid_Geometry "wikilink")
  - 多種の[光源](../Page/光源.md "wikilink")
  - [霧](../Page/霧.md "wikilink")などの大気エフェクトや媒体（[煙](../Page/煙.md "wikilink")、[雲](../Page/雲.md "wikilink")）
  - [フォトンマッピング](https://ja.wikipedia.org/wiki/フォトンマッピング "wikilink")による[反射](../Page/反射.md "wikilink")や[コースティクス](../Page/コースティクス.md "wikilink")（集光模様）
  - [バンプマッピング](../Page/バンプマッピング.md "wikilink")による[しわ](https://ja.wikipedia.org/wiki/しわ "wikilink")、[いぼ](https://ja.wikipedia.org/wiki/いぼ "wikilink")、[波](../Page/波.md "wikilink")などの模様
  - [ラジオシティ](../Page/ラジオシティ.md "wikilink")
  - [TGA](../Page/TGA.md "wikilink")、[PNG](../Page/Portable_Network_Graphics.md "wikilink")、[JPEG](../Page/JPEG.md "wikilink")などの[テクスチャ](https://ja.wikipedia.org/wiki/テクスチャ "wikilink")や出力画像のフォーマットサポート（JPEGは入力のみ）
  - 豊富なドキュメント

POV-Rayには[サードパーティー](../Page/サードパーティー.md "wikilink")によるサポートが多いのが魅力である。多くのツール、テクスチャ、モデル、背景、チュートリアルがWeb上から使用可能である。

## 脚注

## 関連項目

  - [MathMod](https://ja.wikipedia.org/wiki/MathMod "wikilink") - 数学的モデリングソフトウェアであり、parametricサーフィス及びisosurfaceに対応している。しかし、POV-Ray関数への対応は一部のみ。
  - [3D-XplorMath](https://ja.wikipedia.org/wiki/3D-XplorMath "wikilink") - 数学的モデリングソフトウェア。
  - [Functy](https://ja.wikipedia.org/wiki/Functy "wikilink") - 同上。
  - [Shadertoy](https://ja.wikipedia.org/wiki/Shadertoy "wikilink") - GLSL ES言語でのピクセルシェーダーアート環境および共有サービス。距離関数を使用したレイマーチングによる3D表現が可能 。Webベース。
  - [コンピュータグラフィックス](../Page/コンピュータグラフィックス.md "wikilink")
  - [レイトレーシング](../Page/レイトレーシング.md "wikilink")
  - [Constructive Solid Geometry](https://ja.wikipedia.org/wiki/Constructive_Solid_Geometry "wikilink")

## 外部リンク

  -
[Category:3DCGソフトウェア](https://ja.wikipedia.org/wiki/Category:3DCGソフトウェア "wikilink") [Category:オープンソースソフトウェア](https://ja.wikipedia.org/wiki/Category:オープンソースソフトウェア "wikilink")

1.
2.
3.  [MegaPOV Website](http://megapov.inetart.net/) MegaPOV Team
4.  [MegaPOV Website - download](http://megapov.inetart.net/download.html) MegaPOV Team
5.
6.  [UberPOV for Mac](http://megapov.inetart.net/povrayunofficial_mac/uberpov.html) MegaPOV Team
7.  [Persistence of Vision Raytracer acquires the Moray modeller](http://www.povray.org/news/moray-announcement.php) Persistence of Vision Raytracer Pty. 2007年2月1日
8.  [Bishop3D POV-Ray SDL Importer](https://web.archive.org/web/20161220200347/https://www.bishop3d.com/parserdetails.htm) Bishop3D
9.
> この記事は[Mobile 3D Graphics API](https://ja.wikipedia.org/wiki/Mobile_3D_Graphics_API)から翻訳されています。


**Mobile 3D Graphics API** (**M3G**) は、[3次元コンピュータグラフィックス](../Page/3次元コンピュータグラフィックス.md "wikilink")を生成する[Java](https://ja.wikipedia.org/wiki/Java "wikilink")を記述するための[APIを定義した仕様である](../Page/アプリケーションプログラミングインタフェース.md "wikilink")。M3Gは[携帯電話](../Page/携帯電話.md "wikilink")や[PDAのような組み込みデバイス向けのJavaプラットフォームバージョンである](../Page/携帯情報端末.md "wikilink") [Java Platform, Micro Edition](../Page/Java_Platform,_Micro_Edition.md "wikilink") の性能を拡張する。 オブジェクト指向インターフェースは3次元シーン複雑なアニメーションを描画することに使用できる30のクラスで構成している。M3Gは[Java Community Processの下でJSR](../Page/Java_Community_Process.md "wikilink") 184として開発された。2006年現在、現在のM3Gのバージョンは1.1である。

## M3Gの目標

M3Gはモバイルデバイスの特殊な要求に適応するように設計された。モバイルデバイスは[メモリ](https://ja.wikipedia.org/wiki/メモリ "wikilink")、メモリバンド幅およびプロセッサパワーの点で制約されており、しばしばFPUとGPUのようなグラフィックアクセラレーションハードウェアが欠けている。

## M3GはJava3Dではない

M3Gは[Java3D](https://ja.wikipedia.org/wiki/Java3D "wikilink")と間違えるべきではない。Java3Dはstandard Java platformの性能を拡張する。Java3Dはモバイルデバイスよりメモリが多く強力なフロセッサパワー を持ったPC向けに設計されている。 M3GとJava3Dは2つに分かれそれぞれ異なった用途に向けて設計された互換性のないAPIである。

## immediate modeとretained mode

M3Gは開発者が3Dグラフィックを描画するために2の方法(immediate mode, retained mode)を提供している。immediate modeではグラフィック命令はグラフィックパイプラインに直接に入力されレンダリングエンジンが即座に命令を実行する。この方法を使うときは、開発者はレンダリングエンジンにそれぞれのアニメーションフレームごとに描画する内容を特別に伝えるコードを記述しなければならない。

retained modeは[木構造で](../Page/木構造_\(データ構造\).md "wikilink")3D世界の幾何的なオブジェクトをリンクするシーングラフを使用する。 それぞれのオブジェクトに関する幾何学構造、位置、容姿などの高次元の情報はフレーム間で保持される

## その他の特徴

M3G standardはアニメーションデータも含む3Dモデルデータのファイルフォーマットも定義している。

## M3G ユーティリティー

  - [Desktop-M3G](http://code.google.com/p/desktop-m3g/) - M3G for Linux and Android のオープンソース実装
  - [XMM3G](http://xmsoft.co.kr/projects/framework/wiki/XMM3G) - M3G for Windows, WinCE, Linux, Android, iOS, Bada　のオープンソース実装
  - [M3X](http://m3x.dev.java.net) - XML encoding of the .m3g file format and related open-source tools
  - [Wizzer Works M3G Viewer](http://www.wizzerworks.com/index.php?option=com_content&view=category&layout=blog&id=9&Itemid=4) - .m3g ファイルを閲覧・操作するためのオープンそースツールキット
  - [Maya 用の M3GExport](http://www.m3gexport.com)
  - [Mascot Capsule M3G Exporter](http://www.mascotcapsule.com/M3G) for 3ds Max, Maya, Lightwave, and Softimage|XSI
  - [M3G Exporter for Milkshape 3D](http://developer.sonyericsson.com/wportal/devworld/downloads/download/dw-91536-semcm3gexporter10milkshape3d?cc=gb&lc=en) for MilkShape3D
  - [Blender Exporter](http://www.nelson-games.de/bl2m3g) - Blender向けの M3G エクスポーターのオープンソース実装
  - [Blender Converter](http://code.google.com/p/liquidiser/) - Blender向けのオープンソースのファイルレベルコンバーター
  - [M3G Exporter for Metasequoia](http://code.google.com/p/m3g-exporter-for-metasequoia/) - Metasequoia 向けのオープンソースの M3G エクスポーター
  - [M3G Reader Writer](http://code.google.com/p/m3g-reader-writer/) - .m3g ファイルを読み書きするオープンソースの C/C++ ライブラリ

## 外部リンク

  - [JSR 184: Mobile 3D Graphics API for J2ME](http://www.jcp.org/en/jsr/detail?id=184)
  - [Getting Started With the Mobile 3D Graphics API for J2ME](http://www.oracle.com/technetwork/systems/3dgraphics-155829.html)
  - [JSR 239: Java Binding for the OpenGL ES API](http://www.jcp.org/en/jsr/detail?id=239) - 3Dグラフィック使用に関連して

[Category:グラフィックライブラリ](https://ja.wikipedia.org/wiki/Category:グラフィックライブラリ "wikilink") [Category:Java](https://ja.wikipedia.org/wiki/Category:Java "wikilink") [Category:API](https://ja.wikipedia.org/wiki/Category:API "wikilink") [Category:3DCG](https://ja.wikipedia.org/wiki/Category:3DCG "wikilink")
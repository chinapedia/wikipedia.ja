> この記事は[VRML](https://ja.wikipedia.org/wiki/VRML)から翻訳されています。


**Virtual Reality Modeling Language** (**仮想現実モデリング言語**、**VRML**) は、3次元の物体に関する情報を記述するための[ファイルフォーマット](../Page/ファイルフォーマット.md "wikilink")。[WWW上で利用されることを前提に設計された](../Page/World_Wide_Web.md "wikilink")。

## 概要

ファイル形式は[テキストファイル](../Page/テキストファイル.md "wikilink")（[コンパイル](https://ja.wikipedia.org/wiki/コンパイル "wikilink")が不要）であり、[ヘッダ](https://ja.wikipedia.org/wiki/ヘッダ_\(コンピュータ\) "wikilink")、[コメント](https://ja.wikipedia.org/wiki/コメント "wikilink")、ノード（フィールド）、プロトタイプ、ルートの5つの要素から構成される。 3D[ポリゴン](../Page/ポリゴン.md "wikilink")の頂点および線の座標、ポリゴンや色や画像による[テクスチャー](https://ja.wikipedia.org/wiki/テクスチャー "wikilink")、光源による明るさなどを指定できる。 また、[URL](https://ja.wikipedia.org/wiki/URL "wikilink")指定によってインターネット上の別の場所にある画像やVRMLファイルを指定できる。 アニメーションや光源、[視点](https://ja.wikipedia.org/wiki/視点 "wikilink")の設定などといったインタラクティブな効果も設定でき、一種の[仮想空間](https://ja.wikipedia.org/wiki/仮想空間 "wikilink")を構築できる。 さらに、Scriptノードを使って、[Java](https://ja.wikipedia.org/wiki/Java "wikilink")・[JavaScript](../Page/JavaScript.md "wikilink")などの[プログラミング言語](../Page/プログラミング言語.md "wikilink")と連携させた動作を行うことも可能である。

VRMLファイルは「ワールド」とも呼ばれ、.wrl という[拡張子](../Page/拡張子.md "wikilink")が付く（たとえば bird.wrl）。VRMLファイルを閲覧するVRMLブラウザには、Cortona VRML Client [1](http://www.parallelgraphics.com/products/cortona/)、blaxxun Contact [2](http://www.blaxxun.com/en/products/contact/)、PivoronPlayer [3](http://www.neeneenee.de/vrml/desktop.html) などがある。 また、VRMLファイル自体はテキスト形式だが、座標値などの3Dデータを多く含み、ファイル容量が大きくなるため、[gzip](https://ja.wikipedia.org/wiki/gzip "wikilink")を使った圧縮が行われる場合も多い。 たいていの3次元モデリングツールには、VRML形式での保存機能が付いている。

## 歴史

このフォーマットの開発を推進するために[Web3Dコンソーシアム](https://ja.wikipedia.org/wiki/Web3Dコンソーシアム "wikilink")が設立され、規格についての議論などが行われている。

VRMLの最初のバージョン（通称VRML 1.0）は[1994年](../Page/1994年.md "wikilink")[11月](../Page/11月.md "wikilink")に制定された。 このバージョンでは[SGI社により開発されていた](https://ja.wikipedia.org/wiki/Silicon_Graphics "wikilink")[Open Inventorとよばれるツールのファイルフォーマットに良く似た仕様として制定された](https://ja.wikipedia.org/wiki/Open_Inventor "wikilink")。 その後、インタラクティブな動きなどの新しい機能を追加したVRML 97 (ISO/IEC DIS 14772-1, 通称VRML 2.0) 仕様が策定された\[1\]。 現在では、VRMLと呼ぶ場合にはこのVRML 2.0を指すことが多い。

VRML1.0の制定以降、3次元空間を容易に記述できるという点から注目され、[Webブラウザからそのまま使えるさまざまな](../Page/ウェブブラウザ.md "wikilink")[プラグイン](../Page/プラグイン.md "wikilink")も提供され、普及も進んだ。 しかし、VRMLの表現能力の限界やモデリングツールの少なさ、操作の難しさなどから、しだいにあまり使われなくなっている。

VRMLの表現能力の限界などから、次世代の仕様として[XMLベースの](../Page/Extensible_Markup_Language.md "wikilink")[X3D](../Page/X3D.md "wikilink")を一から作成することとなった。

## 脚注

## 関連規格

  - [3DMLW](https://ja.wikipedia.org/wiki/3DMLW "wikilink") (3D Markup Language for Web)
  - [COLLADA](https://ja.wikipedia.org/wiki/COLLADA "wikilink")
  - [U3D](https://ja.wikipedia.org/wiki/Universal_3D "wikilink")
  - [X3D](../Page/X3D.md "wikilink") （VRML 後継者）

## 関連項目

  - [コンピュータ言語](https://ja.wikipedia.org/wiki/コンピュータ言語 "wikilink")
      - [データ記述言語](../Page/データ記述言語.md "wikilink")

## 外部リンク

  - [Web3Dコンソーシアム（英語）](http://www.web3d.org/)
  - [Web3D software to view VRML files without ActiveX plug-in](http://www.viewlife.com)
  - [VRML LABO](http://hp.vector.co.jp/authors/VA004037/)

[Category:ベクターグラフィックス・マークアップ言語](https://ja.wikipedia.org/wiki/Category:ベクターグラフィックス・マークアップ言語 "wikilink") [Category:オープンフォーマット](https://ja.wikipedia.org/wiki/Category:オープンフォーマット "wikilink") [Category:仮想世界](https://ja.wikipedia.org/wiki/Category:仮想世界 "wikilink")

1.
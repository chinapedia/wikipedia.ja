> この記事は[BPCS-Steganography](https://ja.wikipedia.org/wiki/BPCS-Steganography)から翻訳されています。


**BPCS-Steganography**（BPCS-ステガノグラフィ）とは[デジタル・ステガノグラフィ技術の一種である](../Page/ステガノグラフィー.md "wikilink")。

## 概要

BPCS-Steganography(Bit-Plane Complexity Segmentation Steganography)は、秘匿したい情報ファイル（秘匿ファイル）を、Vessel画像（Carrier, Cover, Dummy画像などとも呼ばれる）に埋め込んで隠すものである。通常、Vesselとしては24ビット画像（フルカラー画像）を利用する。この場合の「埋め込み」とは、実際には、Vessel画像の各ビットプレーン上の「複雑な領域」を、秘匿ファイルと置き換える処理のことである。BPCS-Steganographyの最大の特徴は、埋め込み容量が非常に大きいことである。

## 埋込みの原理

人間の視覚は、あまりにも複雑な視覚パターンに対しては「細かな情報を知覚できない」という性質を有している。例えば、均一に広がった砂浜では、「2つの**一辺が10cmの正方形領域**の違い」を見いだすことは不可能であり、どちらも同じに見えるはずである。しかし、実際には2つの領域に存在するそれぞれの砂粒の形状や数はすべて異なっている。すなわち、あまりにも複雑な2つの異なる砂粒の配列に対して、人の目は、「どちらも同じ砂粒の領域である」としか知覚できない。 BPCS-Steganographyは、このような視覚特性を利用して、Vessel画像のビットプレーン上の**複雑な領域**を、別の複雑なパターン（**秘匿ファイルの小片**）と置き換える（埋め込む）。このような埋込をしても人の目には変化が知覚できない。

## 研究・開発の状況

このステガノグラフィ技術は、1997年に日本とアメリカの研究者によって提案されたものである。その実験プログラムは、[Qtech Hide & View](http://www.datahide.org/BPCSj/QtechHV-download-j.html) という名称でWeb上に公開されている。その後、部分的なアルゴリズムの改良や、ステガナリシスへの耐性の研究などが進められている。

## 参考文献

  - [Principle and applications of BPCS-Steganography（PDFファイル）](http://www.datahide.org/BPCSe/Articles/Ref-6.SPIE98.pdf)
  - 画像電子学会編、『電子透かし技術』、[東京電機大学出版局](https://ja.wikipedia.org/wiki/東京電機大学出版局 "wikilink")、2004年、第12章「ディジタル・ステガノグラフィ技術について」、pp.181-195。

## 参考記事

  - [Invitation to BPCS-Steganography](http://www.datahide.org/BPCSj/)

[Category:暗号技術](https://ja.wikipedia.org/wiki/Category:暗号技術 "wikilink")
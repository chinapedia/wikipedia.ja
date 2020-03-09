> この記事は[Graphics Interchange Format](https://ja.wikipedia.org/wiki/Graphics_Interchange_Format)から翻訳されています。


****（グラフィックス・インターチェンジ・フォーマット、略称**GIF**）とは[CompuServe](https://ja.wikipedia.org/wiki/CompuServe "wikilink")のPICSフォーラムで提唱された[画像ファイルフォーマット](https://ja.wikipedia.org/wiki/画像ファイルフォーマット "wikilink")の一つ。[LZW](https://ja.wikipedia.org/wiki/Lempel–Ziv–Welch "wikilink")[特許](https://ja.wikipedia.org/wiki/特許 "wikilink")を使用した画像[圧縮が可能](../Page/データ圧縮.md "wikilink")。一般的に用いられている[拡張子](https://ja.wikipedia.org/wiki/拡張子 "wikilink")は`.gif`。「ギフ\[1\]」または「ジー・アイ・エフ」と読まれることもあるが に "GIF" が選出された際のインタビューにおいて設計者のSteve Wilhiteは「jif（ジフ）」が正しい読み方と述べている\[2\]。

## 特徴

GIFは256色以下の画像を扱うことができる[可逆圧縮](../Page/可逆圧縮.md "wikilink")形式のファイルフォーマットである。圧縮画像ファイルフォーマットでは歴史の長いもののひとつで、[Webブラウザでは](../Page/ウェブブラウザ.md "wikilink")[JPEG](../Page/JPEG.md "wikilink")と並んで標準的にサポートされる。圧縮形式の特性上、同一色が連続する画像の圧縮率が高くなるため、イラストやボタン画像など、使用色数の少ない画像への使用に適している。

GIF規格には[1987年](https://ja.wikipedia.org/wiki/1987年 "wikilink")[6月15日](https://ja.wikipedia.org/wiki/6月15日 "wikilink")に公開された**GIF87a**と[1990年](https://ja.wikipedia.org/wiki/1990年 "wikilink")[7月30日](https://ja.wikipedia.org/wiki/7月30日 "wikilink")に公開された**GIF89a**の2種類があり、GIF89aでは、透過GIFと[GIFアニメーション](https://ja.wikipedia.org/wiki/GIFアニメーション "wikilink")がサポートされた。現在使われている規格はGIF89aである。GIFフォーマットの[著作権](../Page/著作権.md "wikilink")はCompuServeが所有するが、その利用はライセンスフリーであったため、[日本](https://ja.wikipedia.org/wiki/日本 "wikilink")以外での[パソコン通信](../Page/パソコン通信.md "wikilink")をはじめとする画像交換の標準フォーマットとして使われていた（日本ではパソコン通信時代は[MAGや](https://ja.wikipedia.org/wiki/MAGフォーマット "wikilink")[Piが主流だった](https://ja.wikipedia.org/wiki/Pi_\(画像圧縮\) "wikilink")）。ただし、圧縮技術として[LZWを使用しているため](https://ja.wikipedia.org/wiki/Lempel–Ziv–Welch "wikilink")、後述する特許権の問題が発生した。

GIF画像ファイルにはGIF画像識別文字列が埋め込まれており、画像ファイルの最初の6文字は必ず「GIF87a」もしくは「GIF89a」で始まっている。

また、GIFフォーマットは以下の画像をサポートする。

  - 2色モノクロから16777216色 (= 2<sup>24</sup>) 中256色 (= 2<sup>8</sup>) までの色サポート
  - 1x1 から 65535x65535 (= (2<sup>16</sup> − 1)<sup>2</sup>) までの画像サイズのサポート
  - 1つのファイルの中に複数の画像が格納可能

GIFには以下のような特徴的な拡張が行われており、かつWebブラウザでの表示サポートも比較的良好であることから、これらの機能を利用するためにGIF形式が選択されることも多い。

  - 透過GIF - 特定色を透明化し、画像の背景を透過表示する。
  - [GIFアニメーション](https://ja.wikipedia.org/wiki/GIFアニメーション "wikilink") - 複数画像を1つのファイルに収録してアニメーション表示する。
  - [インターレースGIF](https://ja.wikipedia.org/wiki/インターレース#静止画のインターレース "wikilink") - ファイル読み込みの進捗に合わせて段階的に画像を表示する。

なお、ほとんど用いられることはないが、[非可逆圧縮](../Page/非可逆圧縮.md "wikilink")もサポートしている。

また、Webサイトを作成する際、「1x1ピクセルの透過GIF」を利用したデザイン調整をおこなうことがあり、そのような画像はと呼ばれる。

## 特許問題とその顛末

GIFは、データ圧縮アルゴリズムとして、[1984年](../Page/1984年.md "wikilink")に発表された[LZWを使用しているが](https://ja.wikipedia.org/wiki/Lempel–Ziv–Welch "wikilink")、このアルゴリズムについては米[ユニシス](https://ja.wikipedia.org/wiki/ユニシス "wikilink")が特許権を取得していた。この点に関し、ユニシスは当初はGIFにおけるLZWアルゴリズムの利用について利用料を請求しない方針を採っていたが、GIFフォーマットの利用が広まり、Webブラウザで標準的にサポートされるようになると、GIFにおけるLZWの利用について利用料を請求する方針に転換した。

この事により、GIF形式をサポートする画像編集ソフトウェアの制作者のみならず、そのソフトウェアを利用してGIF画像を制作した一般の利用者に対しても特許使用料が賦課される懸念が生じたため、GIF形式の特徴を備えたフリーな代替物として[PNGが開発された](../Page/Portable_Network_Graphics.md "wikilink")。

米国内では[2003年](../Page/2003年.md "wikilink")[6月20日](https://ja.wikipedia.org/wiki/6月20日 "wikilink")にLZWの特許が失効し、日本国内でも[2004年](https://ja.wikipedia.org/wiki/2004年 "wikilink")6月20日に特許が失効した。現在ではGIFは自由に使うことのできるフォーマットであると考えられている。そのため、GIFの利用者は再び増えており、一時的に公開が停止されていたGIFを生成・表示するソフトウェアも再公開されるようになっている。

しかし、[インターネット](https://ja.wikipedia.org/wiki/インターネット "wikilink")の末端接続サービスは既に[ブロードバンド主体になっており](https://ja.wikipedia.org/wiki/ブロードバンドインターネット接続 "wikilink")、また端末である[パソコンの表現能力の飛躍的な向上により](../Page/パーソナルコンピュータ.md "wikilink")、フルカラー対応の圧縮形式（JPEGやPNGなど）の需要が高まり、256色までしか対応できないGIFの使用頻度は減少することとなった。また、GIFアニメーションの代わりに、高画質で[ギミック](https://ja.wikipedia.org/wiki/ギミック "wikilink")を組み込むことのできる[Adobe Flashが利用される例もあった](../Page/Adobe_Flash.md "wikilink")。

以上の理由から、以前より使用頻度は減少傾向にあるものの、長年使われてきたファイルフォーマットであり、対応しているソフトウェアも多いことから、GIFが利用されるケースは少なくない。特に[バナー](https://ja.wikipedia.org/wiki/バナー "wikilink")と呼ばれる広告表示用の画像は、広告媒体の入稿規定により、ファイル容量の上限と共にファイル形式をGIFで指定するものも多い。

いわゆる[ガラケー](https://ja.wikipedia.org/wiki/ガラケー "wikilink")では、[2008年](https://ja.wikipedia.org/wiki/2008年 "wikilink")に日本国内で発売された[携帯電話](../Page/携帯電話.md "wikilink")のうち、[Docomoの端末ではGIF](https://ja.wikipedia.org/wiki/NTTドコモ "wikilink")/JPEGが、[auおよび](https://ja.wikipedia.org/wiki/au_\(携帯電話\) "wikilink")[ソフトバンク](https://ja.wikipedia.org/wiki/ソフトバンク "wikilink")モバイルの端末では搭載ブラウザにてGIF/JPEG/PNGが利用可能であるなど、画像の特性に合わせてGIFも積極的に利用されていた。

## 注

## 関連項目

  - [GNU plotutils](https://ja.wikipedia.org/wiki/GNU_plotutils "wikilink") - LZW の代わりに[ランレングス圧縮を使う](https://ja.wikipedia.org/wiki/連長圧縮 "wikilink")、疑似的なGIF形式を採用している。
  - [フロイド-スタインバーグ・ディザリング](https://ja.wikipedia.org/wiki/フロイド-スタインバーグ・ディザリング "wikilink") - 256色に減色する際によく使われるアルゴリズム。

## 外部リンク

  - [GIF89a仕様書](http://www.w3.org/Graphics/GIF/spec-gif89a.txt)（英語、[W3CWebサイト内](../Page/World_Wide_Web_Consortium.md "wikilink")）
  - [GIF87a仕様書](https://www.w3.org/Graphics/GIF/spec-gif87.txt)（英語、[W3CWebサイト内](../Page/World_Wide_Web_Consortium.md "wikilink")）
  - [GIF 検索/コミュニティー](http://slinky.asia) - 日本語のみ。

[Category:ラスターグラフィックス・ファイルフォーマット](https://ja.wikipedia.org/wiki/Category:ラスターグラフィックス・ファイルフォーマット "wikilink") [Category:オープンフォーマット](https://ja.wikipedia.org/wiki/Category:オープンフォーマット "wikilink")

1.  <http://bits.blogs.nytimes.com/2013/05/23/battle-over-gif-pronunciation-erupts/>
2.  <http://bits.blogs.nytimes.com/2013/05/21/an-honor-for-the-creator-of-the-gif/>
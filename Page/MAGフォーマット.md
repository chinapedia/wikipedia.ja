> この記事は[MAG](https://ja.wikipedia.org/wiki/MAG)から翻訳されています。


**MAGフォーマット**（マグフォーマット）は、[MS-DOS](../Page/MS-DOS.md "wikilink")時代の[日本](https://ja.wikipedia.org/wiki/日本 "wikilink")の[パソコン通信](../Page/パソコン通信.md "wikilink")での[画像ファイルフォーマット](https://ja.wikipedia.org/wiki/画像ファイルフォーマット "wikilink")のひとつ。[ファイル拡張子は](../Page/拡張子.md "wikilink")、**.MAG**。

**MAG**（まぐ）、**鮪**（まぐろ）、ヘッダの文字列からMAKI02、とも呼ばれる。

## 概要

**MAKIフォーマット**の後継の画像圧縮フォーマットとして[Woody-Rinn](https://ja.wikipedia.org/wiki/Woody-Rinn "wikilink")によって、[1991年](../Page/1991年.md "wikilink")に発表された。[草の根BBS](https://ja.wikipedia.org/wiki/草の根BBS "wikilink")「まきちゃんネット」上で、[1991年](../Page/1991年.md "wikilink")[2月13日](../Page/2月13日.md "wikilink")に仕様書が公開。2月27日に草の根BBS「似非」で発表された画像表示プログラム「まぐろーだー」から転じて「鮪だ\!」「[マグロ](https://ja.wikipedia.org/wiki/マグロ "wikilink")」とも呼ばれる。

前身のMAKIフォーマットよりも圧縮率が高く、MAKIフォーマットでは16色のみだったのが256色もサポートする。横640ドット、縦400もしくは200ドットに画像サイズが固定されていたMAKIフォーマットに対して、画像サイズも自由になっている。

フォーマットの仕様書が公開されたこともあり、[パソコンの各機種に移植され](../Page/パーソナルコンピュータ.md "wikilink")、[1990年代](../Page/1990年代.md "wikilink")半ばにインターネットの[WWWが普及するまでは](../Page/World_Wide_Web.md "wikilink")、日本で使われる標準的なグラフィックフォーマットの一つとして、[PIC](https://ja.wikipedia.org/wiki/PIC_\(画像圧縮\) "wikilink")、[Piと共に主流になっていた](https://ja.wikipedia.org/wiki/Pi_\(画像圧縮\) "wikilink")。

[PC-9800シリーズ](../Page/PC-9800シリーズ.md "wikilink")用のMS-DOS環境においてMAG形式は、21世紀における[JPEG](../Page/JPEG.md "wikilink")形式や[GIF形式と同様の地位を築いていた](../Page/Graphics_Interchange_Format.md "wikilink")。同じくWoody-RINNの開発で、MAG形式をサポートする[フリーウェア](../Page/フリーウェア.md "wikilink")の[グラフィックソフト](https://ja.wikipedia.org/wiki/グラフィックソフト "wikilink")「鮪ペイント」の存在も普及に一役買った。「鮪ペイント」は、後に改良が加えられ、1992年には「[マルチペイント](https://ja.wikipedia.org/wiki/マルチペイント "wikilink")」として市販された。

圧縮は[可逆圧縮](../Page/可逆圧縮.md "wikilink")である。基本的なアルゴリズムについて、以下説明する（「フラグA」「フラグB」といった、用語の詳細については「仕様書」を参照のこと）。まず、横4ドット\[1\]のパターンに注目し、既にロードされている左上方向の（設計者による[ヒューリスティクス](../Page/ヒューリスティクス.md "wikilink")により選ばれた）15箇所のどこかに同じパターンがあれば、その位置を表す[4ビット](https://ja.wikipedia.org/wiki/4ビット "wikilink")に符号化・圧縮される（これを「フラグB」と呼んでいる）。「16箇所目」は、同じパターンが存在しない新パターンとして、生のデータとして記録あるいは再生する。さらに直前の行の符号と比較し、同じであれば符号自体を省略し、省略されたかどうかはビット列化して持っている（これを「フラグA」と呼んでいる）。提案者曰く「[2次元](https://ja.wikipedia.org/wiki/2次元 "wikilink")に拡張された[LZSSみたいなもの](https://ja.wikipedia.org/wiki/Lempel–Ziv–Storer–Szymanski "wikilink")」。16色画像の圧縮率は割合高いが、256色の圧縮率はそれほど高くない\[2\]。画像データに特徴的なパターンの圧縮のみに特化\[3\]し、[MPEGなどに見られる](../Page/Moving_Picture_Experts_Group.md "wikilink")、情報理論的な圧縮をフォーマットに含むことはせず、画像配布などにおいては[LHA](../Page/LHA.md "wikilink")などによる圧縮を前提としている。

[1990年代](../Page/1990年代.md "wikilink")後半、マイクロソフトの[Windows 95発売以降](../Page/Microsoft_Windows_95.md "wikilink")、当時の標準機であったPC-9800シリーズの同OSへの対応とともに、それまでの同時画面発色数16色というハードウェア的な制限が緩和されていった結果、より多色表示を標準サポートし、圧縮率の高いグラフィックフォーマットへと主流は移行していった。さらに、[インターネット](../Page/インターネット.md "wikilink")が普及し[ウェブブラウザ](../Page/ウェブブラウザ.md "wikilink")の使う標準画像フォーマットとしてGIFとJPEGが普及するに至り、現在は新規にMAG形式の画像が作成される機会はほとんど無くなっている。

## 参考文献

  - まぐろのすべて―MAGフォーマット開発秘話（1995年10月、まぐろBBS、ソフトバンク、ISBN 4-89052-799-0）

## 注

<references/>

## 関連項目

  - [GIF](../Page/Graphics_Interchange_Format.md "wikilink")
  - [JPEG](../Page/JPEG.md "wikilink")
  - [PIC](https://ja.wikipedia.org/wiki/PIC_\(画像圧縮\) "wikilink")
  - [PIC2](https://ja.wikipedia.org/wiki/PIC2 "wikilink")
  - [Pi](https://ja.wikipedia.org/wiki/Pi_\(画像圧縮\) "wikilink")
  - [Q0](https://ja.wikipedia.org/wiki/Q0 "wikilink")
  - [Q4](https://ja.wikipedia.org/wiki/Q4 "wikilink")
  - [TIFF](../Page/Tagged_Image_File_Format.md "wikilink")

[Category:画像ファイルフォーマット](https://ja.wikipedia.org/wiki/Category:画像ファイルフォーマット "wikilink")

1.  16色の場合。16ビット分。「ピクセル」と仕様書では呼んでいる。
2.  「ピクセル」が2ドットになってしまうことに加え、16色の時と比べ、同じパターンの繰返しが現れにくいため。
3.  詳しく説明すると、次のような考え方である。画像をベタなデータで表現するなどし、それを普通のファイル圧縮などに掛けた場合を想定すると、すぐ真横に隣り合ったドットであればその類似は圧縮のためのデータの関連としても有利に働くが、上下のドット間は関連があっても離れたデータになってしまうため圧縮が効きにくいと予想される。そこでMAGでは、画像データであるという特性を生かし、2次元の広がりから類似性を検出して活用する圧縮法にすることで（作者の言「2次元に拡張された」とはそういうことである）、LHAなどとの併用でより圧縮できるようなものとする。単体での圧縮性能を絶対的に追求したものではなく、当時から既に、単体ではこれを上回るものがあった。
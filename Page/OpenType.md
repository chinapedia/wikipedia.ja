> この記事は[OpenType](https://ja.wikipedia.org/wiki/OpenType)から翻訳されています。


**OpenType**（オープンタイプ）は、[デジタルフォントの規格である](../Page/フォント.md "wikilink")。[アップルが開発した](../Page/アップル_\(企業\).md "wikilink") [TrueType](../Page/TrueType.md "wikilink") の拡張版として、[マイクロソフト](../Page/マイクロソフト.md "wikilink")、[アドビシステムズ](../Page/アドビシステムズ.md "wikilink")により共同で開発され、1997年4月にバージョン1.0が発表された\[1\]\[2\]。OpenType はマイクロソフトの登録商標である\[3\]。

## 規格

[Special_Cyrillics.png](https://ja.wikipedia.org/wiki/File:Special_Cyrillics.png "fig:Special_Cyrillics.png")

OpenType は TrueType を発展させ、[PostScript フォントの CFF/Type 2](https://ja.wikipedia.org/wiki/PostScriptフォント#Compact_Font_Format "wikilink") 形式のアウトラインデータも収録できるようにしたものである\[4\]。

[拡張子](../Page/拡張子.md "wikilink")は、アウトラインデータが CFF (PostScript) 形式のものは「.OTF」（フォントコレクションは「.TTC」「.OTC」）、TrueType 形式のものは「.TTF」「.OTF」（フォントコレクションは「.TTC」）のいずれかとなる\[5\]\[6\]\[7\]\[8\]。

## 特徴

OpenType は下記の特徴を持つ。

  - [Unicode](../Page/Unicode.md "wikilink") に完全対応しており、[異体字などを含む](https://ja.wikipedia.org/wiki/字体#異体字 "wikilink")65536個までの[グリフを収録した多言語フォントを実現可能で](../Page/字体.md "wikilink")、 CID（Character IDentifier, Character ID）を使用できる。
  - [文字組版に関する多数の高度な機能](../Page/組版.md "wikilink")（[合字](../Page/合字.md "wikilink")、字体切替、プロポーショナルメトリクス、ペアカーニング、ベースラインの指定など）が利用できる\[9\]<ref>

</ref>。

  - [クロスプラットフォーム](../Page/クロスプラットフォーム.md "wikilink")\[10\]で、 [Windows](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink") と [macOS](https://ja.wikipedia.org/wiki/macOS "wikilink") の双方で同じフォントファイルが利用できる。ATMフォント、低解像度プリンタフォント、高解像度プリンタフォントなどの区別なく、1つのフォントファイルのみで対応ができる。
  - アウトラインが CFF (PostScript) 形式の場合、TrueType 形式よりフォントファイルのサイズを小さくできる<ref group="注釈">

CFF 形式のアウトラインは、3次[ベジェ曲線](../Page/ベジェ曲線.md "wikilink")で表現され、2次ベジェ曲線に比べ制御点の数を少なくできる。なお、3次ベジェ曲線を2次ベジェ曲線に無劣化で変換することはできない。 </ref>\[11\]。

  - 2016年9月策定の OpenType 1.8 で、同じフォントファミリー内の複数のスタイルを一つのフォントファイルにまとめられるバリアブルフォント\[12\] (OpenType Variable Font) が追加された。この規格に対応するフォントは、1つのフォントファイルのみでウェイトや字幅など文字のスタイルを自由自在に変更することができる。<ref>

</ref>。

  - [PNG画像や](../Page/Portable_Network_Graphics.md "wikilink")[SVG画像の埋め込み](../Page/Scalable_Vector_Graphics.md "wikilink")、あるいは複数の単色グリフアウトラインのベクターレイヤーを利用した、カラー絵文字や色付きのフォント（カラーフォント）をサポートする\[13\]。

Windows では OpenType フォントが使用できないアプリケーションもあり、[GDI+](../Page/Graphics_Device_Interface.md "wikilink") では標準で対応されないため [.NET Framework](https://ja.wikipedia.org/wiki/.NET_Framework "wikilink") の [Windows Forms](../Page/Windows_Forms.md "wikilink") などでは標準で使用できない。[WPF](../Page/Windows_Presentation_Foundation.md "wikilink") は に対応した。[Windows 7以降に標準搭載されている](https://ja.wikipedia.org/wiki/Windows_7 "wikilink")[DirectWrite](https://ja.wikipedia.org/wiki/DirectWrite "wikilink")もOpenTypeに対応しているが、カラーフォントへの対応は[Windows 8.1以降であり](https://ja.wikipedia.org/wiki/Windows_8.1 "wikilink")、また[Windows 10](https://ja.wikipedia.org/wiki/Windows_10 "wikilink") Anniversary Update時点でSVGカラーフォントへの対応は部分的にとどまっている\[14\]。

## 和文 OpenType フォント

[JIS X 0208](../Page/JIS_X_0208.md "wikilink") などの[漢字コードは](../Page/JIS漢字コード.md "wikilink")、微小な字形差の多くが包摂規準により同じ符号位置に統合されているため、微小な字形差を表現し分けることができない。 OpenType は微小な字形差などを含み対応可能な特長を有し、日本ではグリフ集合として [Adobe-Japan1](../Page/Adobe-Japan1.md "wikilink")シリーズを用いることで、微小な字形差を区別していることが多い。

漢字の異体字切替は、フォントに内蔵される GSUB テーブルを利用した切替が [Adobe InDesign](../Page/Adobe_InDesign.md "wikilink") などで実装されているほか、Unicode 5.1 で[異体字セレクタ](../Page/異体字セレクタ.md "wikilink")として IVS (Ideographic Variation Sequences) が導入され、その組み合わせとして2007年12月に Adobe-Japan1 が IVD (Ideographic Variation Database) に登録された\[15\]\[16\]。Unicode 6.3 では、SVS (Standardized Variation Sequences) として[CJK互換漢字](../Page/CJK互換漢字.md "wikilink")の1002通りが追加された\[17\]。フォントの規格では、OpenType が2008年5月策定の OpenType 1.5 で Unicode の異体字セレクタに対応した\[18\]。これによりソフトウェア・フォント共に対応していれば、異体字セレクタを利用して[プレーンテキスト](../Page/プレーンテキスト.md "wikilink")上で異体字を表現できる。

日本語のグリフ集合は、Adobe-Japan1-3(Std) が9,354グリフ、Adobe-Japan1-4(Pro) が15,444グリフ、[アップルが制定し](../Page/アップル_\(企業\).md "wikilink") [Mac OS X v10.1](../Page/Mac_OS_X_v10.1.md "wikilink") で採用した独自のグリフ集合である APGS (Apple Publishing Glyph Set) をサポートした Adobe-Japan1-5(Pr5) は20,317グリフ、そして使用頻度の低い漢字を多数収容した Adobe-Japan1-6(Pr6) で23,058グリフをサポートしている\[19\]。

現在では、アドビシステムズや[モリサワ](../Page/モリサワ.md "wikilink")などいくつかの和文フォントベンダーが Adobe-Japan1-6 に準拠した OpenType フォントを多数販売、アップルは [macOS](https://ja.wikipedia.org/wiki/macOS "wikilink") に[ヒラギノ](../Page/ヒラギノ.md "wikilink") OpenType フォントを標準で採用、アドビシステムズは [DTP](../Page/DTP.md "wikilink") ソフト Adobe InDesign で OpenType の文字組版機能に完全対応するなど各方面で対応が進んでいる。[Windows 2000](../Page/Microsoft_Windows_2000.md "wikilink") 以降の [Windows](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink") などでも利用可能だが、OpenType の特徴である高度な文字組版機能を使用するには対応アプリケーションを要する。

## 出力における従来のフォントとの違い

従来の[OCFフォント](../Page/OCFフォント.md "wikilink")、[CIDフォント](https://ja.wikipedia.org/wiki/CIDフォント "wikilink")はともに、ダイナミックロードの出力は不可能ではないが不安定である。日本語を含む2[バイトフォントのDTP出力は](../Page/バイト_\(情報\).md "wikilink")、[イメージセッタ](https://ja.wikipedia.org/wiki/イメージセッタ "wikilink")や[プリンタなど出力機側に専用のフォントをあらかじめインストールし](https://ja.wikipedia.org/wiki/プリンター "wikilink")、出力時は文字コード情報やフォント名の情報のみを出力機へ送り、文字の形の情報は出力機側で計算させた。かつてコンピュータやネットワークの性能が低い状況で負荷を低減させる利点があったが、機能の向上とともに不要となった。

OpenType は、TrueType 同様にダウンロード出力ができるため、コンピュータ側にフォントがインストールされていれば出力が可能である\[20\]。

## 注釈

## 出典

## 関連項目

  - [TrueType](../Page/TrueType.md "wikilink")
  - [PostScriptフォント](../Page/PostScriptフォント.md "wikilink")
  - [FreeType](../Page/FreeType.md "wikilink") - フリーのフォント描画ライブラリ。OpenType をサポートしている。

## 外部リンク

  - [Microsoft Typography - OpenType Specification](https://www.microsoft.com/en-us/Typography/OpenTypeSpecification.aspx)（英語）（マイクロソフトによる OpenType の規格書）

[Category:DTP](https://ja.wikipedia.org/wiki/Category:DTP "wikilink") [Category:書体](https://ja.wikipedia.org/wiki/Category:書体 "wikilink")

1.
2.
3.
4.
5.  フォントコレクション (Font Collection) は、かつては TrueType Collection の名称で TrueType 形式のアウトラインのみをサポートしたが、2015年3月に策定された OpenType 1.7 で CFF 形式のアウトラインのサポートが追加された。この仕様に準拠したフォントとして [源ノ角ゴシック](https://ja.wikipedia.org/wiki/源ノ角ゴシック "wikilink")（[Noto Sans CJK](https://ja.wikipedia.org/wiki/Noto_Sans_CJK "wikilink")）の OTC 版などがある。
6.  ソフトウェアは拡張子だけを見て、アウトラインが CFF 形式か TrueType 形式かを判断してはならないとされている。
7.
8.
9.
10.
11.
12. 日本語ではバリアブルフォントのほか、可変フォントともいわれる。表記が統一されていないが同一の規格を指す。
13. [OpenTypeカラーフォント：Windows Insider用語解説 - ＠IT](https://www.atmarkit.co.jp/ait/articles/1407/03/news113.html)
14. [Color Fonts - Windows applications | Microsoft Docs](https://docs.microsoft.com/en-us/windows/win32/directwrite/color-fonts)
15.
16.
17.
18.
19.
20.
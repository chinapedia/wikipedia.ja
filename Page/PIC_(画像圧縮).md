> この記事は[PIC \(画像圧縮\)](https://ja.wikipedia.org/wiki/PIC_\(画像圧縮\))から翻訳されています。


**PIC**（ピック）は、日本で使われていた画像圧縮フォーマットの一つ。やなぎさわ考案による[可逆圧縮](../Page/可逆圧縮.md "wikilink")の画像圧縮形式である。

[インターネット](../Page/インターネット.md "wikilink")の普及する以前の[パソコン通信](../Page/パソコン通信.md "wikilink")上での画像交換に使われていたフォーマットの一つで、[シャープ](../Page/シャープ.md "wikilink")の[X68000](https://ja.wikipedia.org/wiki/X68000 "wikilink")シリーズにおける事実上標準画像フォーマットとして使われていた。パソコン通信で流通した豊富なPIC形式の画像資産により、256色以上の画像フォーマットとしても有力な地位にあり、[富士通](../Page/富士通.md "wikilink")の[FM-TOWNS](https://ja.wikipedia.org/wiki/FM-TOWNS "wikilink")シリーズでも用いられたり、標準では16色表示の[NECの](../Page/日本電気.md "wikilink")[PC-9801](https://ja.wikipedia.org/wiki/PC-9801 "wikilink")シリーズにも減色して表示するローダーが開発されるなど、他の機種でも主に鑑賞用に使われた。

PIC形式は、[可逆圧縮](../Page/可逆圧縮.md "wikilink")で色数は8色からフルカラーまでに対応していたが、実際にはサイズは、512x512以下、色数は15bitのX68000の仕様に合わせた画像が9割以上を占めており、画像ローダ、セーバもその仕様に合わせた物がほとんどだった。それ以上のサイズの画像を表示させる場合は、上下に画像ファイルを分割した2画面PICと呼ばれるものが主に利用されていた（中には上下左右に分割した4画面PICなども存在した）。

横512x縦512、15bitモードでのX68000の画像は、1:1ではなく15:9もしくは3:2のアスペクト比で表示されていたため他機種との画像の交換には様々な問題がつきまとった。

[アルゴリズム](../Page/アルゴリズム.md "wikilink")は、[ランレングス](https://ja.wikipedia.org/wiki/ランレングス "wikilink")法を二次元に拡張したものと[Wyle符号](https://ja.wikipedia.org/wiki/Wyle符号 "wikilink")化の組み合わせであり、いわゆる[アニメ](../Page/アニメ.md "wikilink")絵と言われるものに対しては驚異的な圧縮率を誇る反面、自然画の圧縮率はあまり良くないという特性を持つ。また展開時は色境界線部分が先行して表示されるため、その様子が「[稲妻](https://ja.wikipedia.org/wiki/稲妻 "wikilink")走る」と称されていた。

## PIC2

PIC2は、PICを改良したフルカラー向けの[可逆圧縮](../Page/可逆圧縮.md "wikilink")の画像フォーマットである。ハフマン符号化の部分に[算術圧縮](https://ja.wikipedia.org/wiki/算術圧縮 "wikilink")を導入するなど細かい部分の改良が行われており、また[X68000](https://ja.wikipedia.org/wiki/X68000 "wikilink")に依存しないフォーマット仕様に改められている。圧縮の特性はPICに近い。しかしながらPIC2の策定はかなり遅れて始まり、確定にも時間がかかったためにPIC2用のローダやセーバなどが作成できず、そのころには既に[JPEG](../Page/JPEG.md "wikilink")がフルカラー用の画像フォーマットとして主流になっていたためにあまり普及しないうちに消えてしまった。

## 関連項目

  - [GIF](../Page/Graphics_Interchange_Format.md "wikilink")
  - [JPEG](../Page/JPEG.md "wikilink")
  - [PI](https://ja.wikipedia.org/wiki/Pi_\(画像圧縮\) "wikilink")
  - [MAG](https://ja.wikipedia.org/wiki/MAKIchan_Graphic_loader "wikilink")
  - [Q0](https://ja.wikipedia.org/wiki/Q0 "wikilink")
  - [Q4](https://ja.wikipedia.org/wiki/Q4 "wikilink")
  - [TIFF](../Page/Tagged_Image_File_Format.md "wikilink")

[Category:画像ファイルフォーマット](https://ja.wikipedia.org/wiki/Category:画像ファイルフォーマット "wikilink")
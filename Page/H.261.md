> この記事は[H.261](https://ja.wikipedia.org/wiki/H.261)から翻訳されています。


**H.261**はCCITT(現在の[ITU-T](../Page/ITU-T.md "wikilink"))によって策定された[動画](../Page/動画.md "wikilink")[圧縮の規格で](../Page/データ圧縮.md "wikilink")、[1990年](https://ja.wikipedia.org/wiki/1990年 "wikilink")に勧告として承認された。

デジタル動画像の圧縮符号化方式としては、[フレーム間予測](../Page/フレーム間予測.md "wikilink")、[離散コサイン変換](../Page/離散コサイン変換.md "wikilink")(DCT)、[量子化](https://ja.wikipedia.org/wiki/量子化 "wikilink")、[エントロピー符号化](https://ja.wikipedia.org/wiki/エントロピー符号化 "wikilink")を組み合わせて用いた、世界最初の[国際標準](https://ja.wikipedia.org/wiki/国際標準 "wikilink")であり、その後に規格化された[H.263](../Page/H.263.md "wikilink")や[H.264](../Page/H.264.md "wikilink")、[MPEG-1](../Page/MPEG-1.md "wikilink")、[MPEG-2](../Page/MPEG-2.md "wikilink")、[MPEG-4](../Page/MPEG-4.md "wikilink")など、数多くの動画像圧縮方式の基礎としてとらえることができる。

[ISDN](../Page/ISDN.md "wikilink")上でのテレビ会議に利用することが想定されているため、符号化ビットレートは64kbps〜1.92Mbpsの間で64kbps刻みで指定することが規格上定められている。

現在の動画像圧縮方式に比べて非常に原始的な仕組みであり、低ビットレート時の画質があまりよいものではなかったため、画質改善のためにループフィルタを導入している。しかし、1991年に登場した[MPEG-1](../Page/MPEG-1.md "wikilink")以降の方式では、1/2画素(ハーフペル)精度以上の動き補償が導入され、それが平滑化フィルタと同等の役割を果たすため、処理負荷の高いループフィルタはその後採用されなくなっている。(なお、2003年に承認されたITU-T勧告[H.264](../Page/H.264.md "wikilink")では、[ブロックノイズ](../Page/ブロックノイズ.md "wikilink")の発生の抑制に特化したループフィルタを採用している。)

当時は、デジタル動画像の標準的な[画面解像度](../Page/画面解像度.md "wikilink")がまだ存在せず、また、テレビジョンの信号方式が[NTSC](../Page/NTSC.md "wikilink")や[PAL](../Page/PAL.md "wikilink")と複数存在し、国ごとに異なるため、共通の画像フォーマットを策定する必要があった。そこで、現在でも標準フォーマットの一つとして用いられることが多い、352×288画素のCIF([Common Intermediate Format](https://ja.wikipedia.org/wiki/Common_Intermediate_Format "wikilink"))が規格化された。H.261では[QCIF](https://ja.wikipedia.org/wiki/QCIF "wikilink")(Quarter CIF; 176×144画素)ないしCIFを使用することができる。なお、色空間についてはYCbCr 4:2:0が採用されている。

## 関連項目

  - [MPEG-1](../Page/MPEG-1.md "wikilink")
  - [H.263](../Page/H.263.md "wikilink")
  - [データ圧縮](../Page/データ圧縮.md "wikilink")

[Category:コーデック](https://ja.wikipedia.org/wiki/Category:コーデック "wikilink") [Category:ITU-T勧告](https://ja.wikipedia.org/wiki/Category:ITU-T勧告 "wikilink")
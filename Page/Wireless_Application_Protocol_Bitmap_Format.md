> この記事は[Wireless Application Protocol Bitmap Format](https://ja.wikipedia.org/wiki/Wireless_Application_Protocol_Bitmap_Format)から翻訳されています。


**Wireless Application Protocol Bitmap Format**（**Wireless Bitmap** と略記される）とは、[モノクローム](../Page/モノクローム.md "wikilink")の[画像ファイルフォーマット](https://ja.wikipedia.org/wiki/画像ファイルフォーマット "wikilink")であり、携帯機器向けに最適化されている。ファイル拡張子は **.wbmp** であり、**WBMP** と記されることもある。

WBMP 画像はモノクロ（黒と白）であり、ファイルサイズは小さい。黒いピクセルを 0、白いピクセルを 1 で表す。

[WAPでは](../Page/Wireless_Application_Protocol.md "wikilink")、カラー画像としては[GIF](../Page/Graphics_Interchange_Format.md "wikilink")、[JPEG](../Page/JPEG.md "wikilink")、[PNGなどの形式をサポートしている](../Page/Portable_Network_Graphics.md "wikilink")\[1\]。

## Wireless Bitmap ファイルのフォーマット

| フィールド名       | フィールド型                                   | サイズ（バイト） | 用途                                                                                    |
| ------------ | ---------------------------------------- | -------- | ------------------------------------------------------------------------------------- |
| Type         | uintvar                                  | 可変       | 画像のタイプ。0 の場合、モノクロのビットマップを意味する。                                                        |
| Fixed header | [byte](../Page/バイト_\(情報\).md "wikilink") | 1        | 予約されている。常に 0。                                                                         |
| Width        | uintvar                                  | 可変       | 画像の幅をピクセル数で表したもの。                                                                     |
| Height       | uintvar                                  | 可変       | 画像の高さをピクセル数で表したもの。                                                                    |
| Data         | byte array                               | 可変       | 画像データをライン単位に並べたもの。1ビットが1ピクセルに対応する。黒いピクセルは 0、白いピクセルは 1。ラインの幅が8で割り切れない場合、バイト境界まで 0 を補う。 |

なお、unitvar とは、ビット列を7ビットずつに分割し、最後尾の7ビットだけは[最上位ビット](https://ja.wikipedia.org/wiki/最上位ビット "wikilink")を 0、それ以外は最上位ビットを 1 としたバイト列にすることで、可変長整数を表す形式である。

## 具体例

以下の例では、b = 黒、w = 白を意味する。

    行1 - bwb
    行2 - wbw
    行3 - bwb

というビットマップを WBMP で表すと、次のようになる。

    オクテット 1: 00000000 (WBMP type)
    オクテット 2: 00000000 (Fixed header)
    オクテット 3: 00000011 (Width) = 3
    オクテット 4: 00000011 (Height) = 3

オクテット 5-7: 各行が 3 ビットなので、5ビットずつパディングする。

```

オクテット 5: 010 00000 （行1）
オクテット 6: 101 00000 （行2）
オクテット 7: 010 00000 （行3）
```

## 脚注

## 外部リンク

  - [WAP WAE Specification Version 1.1](http://www.wapforum.org/what/technical/SPEC-WAESpec-19990524.pdf) WAP Forum、1999年
  - [Produce WBMP for any platform](http://www.ibm.com/developerworks/wireless/library/wi-wbmp/) IBM

[Category:画像ファイルフォーマット](https://ja.wikipedia.org/wiki/Category:画像ファイルフォーマット "wikilink") [Category:長大な項目名](https://ja.wikipedia.org/wiki/Category:長大な項目名 "wikilink")

1.  [The Wireless FAQ](http://www.thewirelessfaq.com/can_color_images_be_used_in_wap)
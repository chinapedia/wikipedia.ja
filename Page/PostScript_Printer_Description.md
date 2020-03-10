> この記事は[PostScript Printer Description](https://ja.wikipedia.org/wiki/PostScript_Printer_Description)から翻訳されています。


**PostScript Printer Description** (**ポストスクリプト・プリンタ・デスクリプション**) は、 [PostScript](../Page/PostScript.md "wikilink") プリンタで利用可能なすべての機能を記述するためプリンタ・メーカーにより作成・供給されるテキスト・ファイルである。 **PPD** と略称される。

## 概要

PPD は PostScript 言語を開発した[アドビシステムズ](../Page/アドビシステムズ.md "wikilink")によって策定された。 PPD ファイル内には印刷ジョブがその機能を呼び出すために用いられる PostScript のコード (コマンド) が含まれており、プリンタの諸機能に対する統一されたインターフェースを提供することによって、それ自体ですべての PostScript プリンタに対するドライバとして働く。 例えば、あるプリンタに対する PPD ファイルに

`*LanguageLevel: "2"`
`*ColorDevice: True`

という記述が含まれていれば、これはプリンタが PostScript の Level 2 を理解すること、それがカラー・プリンタであることを指定している。 その他にも PPD は印刷可能な紙のサイズ、メモリ構成、プリンタの最小のフォント・セットなどを指定することができ、プリンタ固有の設定に対する[木構造のユーザ](../Page/木構造_\(データ構造\).md "wikilink")・インターフェースを指定することもできる。

## CUPS での利用

[Linux](../Page/Linux.md "wikilink")、[macOS](https://ja.wikipedia.org/wiki/macOS "wikilink") などで利用されている印刷システムである [CUPS](https://ja.wikipedia.org/wiki/Common_Unix_Printing_System "wikilink") は、すべての PostScript プリンタに対して PPD のドライバを用いており、 CUPS のフィルタによりデータを加工することによって非 PostScript プリンタに対しても PPD による操作を可能とするよう概念の拡張がなされている。 このようなファイルはすでに標準の PPD ではないが *CUPS-PPD* とよばれている。

## 外部リンク

  - [Adobe Tech Note 5003: PostScript Printer Description (PPD) File Format Specification](http://partners.adobe.com/public/developer/en/ps/5003.PPD_Spec_v4.3.pdf) (PDF ファイル)
  - [Adobe Tech Note 5645: Update to PPD Specification Version 4.3](http://partners.adobe.com/public/developer/en/ps/5645.PPD_Update.pdf) (PDF ファイル)
  - [CUPS, PPDs, PostScript and GhostScript](http://www.linuxprinting.org/kpfeifle/LinuxKongress2002/Tutorial/III.PostScript-and-PPDs/III.PostScript-and-PPDs.html) (クルト・プファイフレ によるチュートリアル)

[Category:ファイルフォーマット](https://ja.wikipedia.org/wiki/Category:ファイルフォーマット "wikilink") [Category:PostScript](https://ja.wikipedia.org/wiki/Category:PostScript "wikilink")
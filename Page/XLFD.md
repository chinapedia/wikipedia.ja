> この記事は[XLFD](https://ja.wikipedia.org/wiki/XLFD)から翻訳されています。


**XLFD**(X Logical Font Description : X論理フォント名, X論理フォント記述子) は、[X Window Systemで使われるフォントをあらわす記述である](../Page/X_Window_System.md "wikilink")。

## フィールドと意味

XLFDは15のフィールドから成り、各フィールドは-(ハイフン)で区切られる。 FontNameRegistry-Foundry-Family-WeightName-Slant-SetwidthName-AddStyleName-PixelSize-PointSize-ResolutionX-ResolutionY-Spacing-AverageWidth-CharSetRegistry-CharSetEncoding

例 -adobe-courier-bold-o-normal--10-100-75-75-m-60-hp-roman8

### FontNameRegistry

フォント登録者の名前。通常は何も書かない。

### Foundry

フォント製造者の名前。フォント名の場合もある。

### Family

フォントファミリ。フォントの種別を表す。

### WeightName

文字の太さ。以下のいずれかが入る。

<細い> thin (ultralight) - extralight - light - book (semilight,demilight) - medium - demibold (semibold) - bold - heavy (extrabold) - black (ultrabold) <太い>

通常は太字の時bold、それ以外の時はmediumを使う。

### Slant

文字の傾き。rは傾き無し、iは傾き有り。

### SetwidthName

文字の横幅。narrow(狭い)、normal(普通)、wide(広い)など。

### AddStyleName

付加的なフォントスタイル。serifやcursiveなどが入ることもあるが、通常何も書かれない。

### PixelSize

ピクセル単位でのフォントサイズ。

### PointSize

ポイント単位でのフォントサイズ。ただし単位は0.1pointなので、10倍した値を書く。

### ResolutionX

横方向の解像度。単位はdpi(dots per inch)。

### ResolutionY

縦方向の解像度。

### Spacing

文字間隔。Mはモノスペース(等幅)、Pはプロポーショナル(可変幅)を意味する。Cはセルを意味し、境界域を持つ。

### AverageWidth

平均文字幅。単位は0.1point。全角フォントの場合PointSizeと同値。半角の場合1/2になる。

### CharSetRegistry

登録組織、規格名など。和文フォントの場合は[日本工業規格｜](https://ja.wikipedia.org/wiki/日本工業規格｜ "wikilink")の規格番号が入る。

### CharSetEncoding

[Category:書体](https://ja.wikipedia.org/wiki/Category:書体 "wikilink")
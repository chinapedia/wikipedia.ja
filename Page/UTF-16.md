> この記事は[UTF-16](https://ja.wikipedia.org/wiki/UTF-16)から翻訳されています。


**UTF-16** (UCS/Unicode Transformation Format 16\[1\]) とは、[Unicode](../Page/Unicode.md "wikilink")および[ISO/IEC 10646の](https://ja.wikipedia.org/wiki/ISO/IEC_10646 "wikilink")、符号化フォームおよび符号化スキーム（[文字符号化方式](https://ja.wikipedia.org/wiki/文字符号化方式 "wikilink")を参照）のひとつである。

UTF-16では、1[文字](../Page/文字.md "wikilink")が、[16ビット](../Page/16ビット.md "wikilink")の符号単位が1つまたは2つで符号化される。これが「-16」の名の由来である。[基本多言語面](../Page/基本多言語面.md "wikilink")（BMP）内の文字は、符号単位1つの16ビットで表される。BMP以外の文字は、符号単位2つの32ビットで表される。なお、UTF-16は2[バイトコードだと誤解されることがあるが](../Page/バイト_\(情報\).md "wikilink")、このように4バイトのこともあるため間違いである。

Unicodeにおいては、厳密には、文字符号化フォーム（）の1つの名称であり、かつ、UTF-16符号化形式のための文字符号化スキーム（）の1つの名称でもある。UTF-16符号化フォームのための文字符号化スキームには、UTF-16の他に**UTF-16BE**、**UTF-16LE**がある。

## 符号化

UTF-16では、Unicodeの[代用符号位置を除いた符号位置](https://ja.wikipedia.org/wiki/Unicode文字のマッピング#代用符号位置 "wikilink")（Unicodeスカラ値という）を、16ビット符号なし[整数を符号単位とした符号単位列で表す](../Page/整数型.md "wikilink")。符号単位列は1つまたは2つの符号単位からなる。すなわち、合計は16ビットまたは[32ビット](../Page/32ビット.md "wikilink")である。

BMPに含まれるU+0000..U+D7FFとU+E000..U+FFFFは、そのまま符号単位1つで表す。

BMP以外のU+10000..U+10FFFFは、表のようにビットを配分して、符号単位2つで表す。

| スカラ値                       | UTF-16                              | 備考                 |
| -------------------------- | ----------------------------------- | ------------------ |
| `xxxxxxxxxxxxxxxx`         | `xxxxxxxxxxxxxxxx`                  |                    |
| `000uuuuuxxxxxxxxxxxxxxxx` | `110110wwwwxxxxxx 110111xxxxxxxxxx` | `wwww = uuuuu - 1` |

このとき使われる、U+D800 ～ U+DFFF の符号位置を、代用符号位置（Surrogate Code Point）と呼び、BMP外の1つの符号位置を表す連続した2つの代用符号位置のペアを[サロゲートペアと呼ぶ](https://ja.wikipedia.org/wiki/Unicode#サロゲートペア "wikilink")。代用符号位置に使うため、BMPのこの領域には文字が収録されておらず、UTF-16以外の[UTF-8](../Page/UTF-8.md "wikilink")、[UTF-32](../Page/UTF-32.md "wikilink")では使用されない。

Unicodeの符号位置の最大がU+10FFFFなのは、それがUTF-16で表せる最大だからである。

UTF-16符号化フォームで表現された文字は、16ビット符号なし整数の符号単位列でありプログラム内部での処理には都合がよいが、情報交換のためにファイルの読み書きや通信を行う場合は、適当な符号化スキームによりバイト[直列化する必要がある](../Page/シリアライズ.md "wikilink")。

符号化スキームにはUTF-16、UTF-16BE、UTF-16LEの3種類ある。UTF-16BEは16ビット整数をビッグエンディアンで直列化する。UTF-16LEはリトルエンディアンで直列化する。UTF-16BE、UTF-16LEの場合は[バイト順マーク (BOM)](https://ja.wikipedia.org/wiki/バイト順マーク "wikilink") の付与は許されない。UTF-16の場合はBOMでエンディアンを明示するか、上層のプロトコルで指定されておらずBOMも付与しない場合はビッグエンディアンにするよう決められている\[2\]。

## 比較

[UTF-8](../Page/UTF-8.md "wikilink")、[UTF-32](../Page/UTF-32.md "wikilink")と比較して、一般的な日本語が主体の文章ではUnicode符号化方式の中では最小サイズとなる。[追加面](https://ja.wikipedia.org/wiki/追加面 "wikilink")の文字が含まれる場合、バイト順にソートしても符号位置順とはならない。また、UTF-8と違い[ASCII](../Page/ASCII.md "wikilink")互換ではない。

[Shift_JIS](../Page/Shift_JIS.md "wikilink")と比較して、Shift_JISでは1バイト文字と、2バイト文字の1バイト目と2バイト目の値範囲が一部重複しているが、UTF-16では1符号単位文字、サロゲートペアの前半の符号単位、後半の符号単位がすべて異なる値範囲を取る。そのため、Shift_JISであった、例えば「a」で検索すると2バイト目にマッチする場合がある、途中から読みこむと文字の区切りがわからないときがある、1バイト目や2バイト目が欠落した場合、後続の文字すべてが文字化けする可能性がある、などの問題は発生しない。UTF-16では欠落があっても影響を受けるのはその文字だけである\[3\]。

## 利用

UTF-16符号化フォームは、[Windowsや](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")[Java](https://ja.wikipedia.org/wiki/Java "wikilink")（[J2SE](../Page/Java_Platform,_Standard_Edition.md "wikilink") 5.0以上）で、内部表現に使われている。Windowsの内部表現では16ビット符号なし整数を符号単位とするUTF-16符号化フォームとして扱い、ファイルなどではBOMありのUTF-16符号化スキーム（リトルエンディアン）が主である。

[TCP/IPネットワークでは](../Page/インターネット・プロトコル・スイート.md "wikilink")、プロトコルヘッダやMIME等の手段で文字符号化スキームを指定しない場合はビッグエンディアンに決められている。

## 脚注

### 注釈

### 出典

## 参考資料

用語の日本語表記は次を参考にした。

## 関連項目

  - [UTF-8](../Page/UTF-8.md "wikilink")
  - [UTF-32](../Page/UTF-32.md "wikilink")

[Category:文字コード](https://ja.wikipedia.org/wiki/Category:文字コード "wikilink") [Category:Unicode](https://ja.wikipedia.org/wiki/Category:Unicode "wikilink")

1.  UTFは、UnicodeではUnicode Transformation Formatの略、[ISO/IEC 10646ではUCS](https://ja.wikipedia.org/wiki/ISO/IEC_10646 "wikilink") Transformation Formatの略とされる。
2.
3.
> この記事は[Bzip2](https://ja.wikipedia.org/wiki/Bzip2)から翻訳されています。


**bzip2**（ビージップツー）は、[データ圧縮](../Page/データ圧縮.md "wikilink")[プログラムのひとつ](../Page/プログラム_\(コンピュータ\).md "wikilink")、およびその圧縮データの[フォーマットである](../Page/ファイルフォーマット.md "wikilink")。 により開発され、その実装（プログラム）のライセンスは BSD-style である\[1\]。1996年6月に最初に公開され、その後の数年間で動作安定性と人気とが高まった。2000年末にversion 1.0が発表された。bzip2圧縮プログラムを用いて処理されたファイルには、[拡張子](../Page/拡張子.md "wikilink")として標準的には「.bz2」が付けられる。[アーカイブ機能はない](../Page/アーカイブ_\(コンピュータ\).md "wikilink")。

bzip2は、より効率的な圧縮のために[ブロックソート法](https://ja.wikipedia.org/wiki/ブロックソーティング "wikilink")（バロウズ-ホイラー変換）と[MTF (Move-To-Front) 法](https://ja.wikipedia.org/wiki/Move_To_Front "wikilink")、[ハフマン符号](../Page/ハフマン符号.md "wikilink")化法を用いており、従来の[gzip](https://ja.wikipedia.org/wiki/gzip "wikilink")や[ZIPといったデータ圧縮法と比べ](../Page/ZIP_\(ファイルフォーマット\).md "wikilink")、より高い圧縮率を誇っている。また、bzip2の操作法は意図的にgzipに似せてあり、gzipからの移行は容易である。しかしながら、bzip2は処理速度の点でgzipよりも劣っており、gzipを完全に置換するには至らず、また高圧縮率のフォーマットとしては[xzも登場している](https://ja.wikipedia.org/wiki/Xz_\(ファイルフォーマット\) "wikilink")。しかし、[StuffIt](../Page/StuffIt.md "wikilink")や[7-Zip](../Page/7-Zip.md "wikilink")といった高圧縮プログラムと比べれば圧縮率もそこそこ良い割に高速に動作する。

bzip2は、ネットワーク経由で配布される比較的サイズの大きなファイルの圧縮に用いられることが多く、代表的なものとしては、[Linuxカーネル](../Page/Linuxカーネル.md "wikilink")のソースコード群が挙げられる。

bzip2の原型である **bzip** は圧縮[アルゴリズム](../Page/アルゴリズム.md "wikilink")に[算術符号](../Page/算術符号.md "wikilink")を利用しているため、算術符号関係の[特許](../Page/特許.md "wikilink")による制約のために開発が継続不能とされた、という経緯がある。

## 脚注

## 外部リンク

  - [The bzip2 and libbzip2 home page](https://www.sourceware.org/bzip2/)（英語）

[Category:データ圧縮規格](https://ja.wikipedia.org/wiki/Category:データ圧縮規格 "wikilink") [Category:1996年のソフトウェア](https://ja.wikipedia.org/wiki/Category:1996年のソフトウェア "wikilink")

1.
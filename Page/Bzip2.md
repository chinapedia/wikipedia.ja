> この記事は[Bzip2](https://ja.wikipedia.org/wiki/Bzip2)から翻訳されています。


**bzip2**（ビージップツー）は、[データ圧縮](https://ja.wikipedia.org/wiki/データ圧縮 "wikilink")[プログラムのひとつ](https://ja.wikipedia.org/wiki/プログラム_\(コンピュータ\) "wikilink")、およびその圧縮データの[フォーマットである](https://ja.wikipedia.org/wiki/ファイルフォーマット "wikilink")。 により開発され、その実装（プログラム）のライセンスは BSD-style である\[1\]。1996年6月に最初に公開され、その後の数年間で動作安定性と人気とが高まった。2000年末にversion 1.0が発表された。bzip2圧縮プログラムを用いて処理されたファイルには、[拡張子](https://ja.wikipedia.org/wiki/拡張子 "wikilink")として標準的には「.bz2」が付けられる。[アーカイブ機能はない](https://ja.wikipedia.org/wiki/アーカイブ_\(コンピュータ\) "wikilink")。

bzip2は、より効率的な圧縮のために[ブロックソート法](https://ja.wikipedia.org/wiki/ブロックソーティング "wikilink")（バロウズ-ホイラー変換）と[MTF (Move-To-Front) 法](https://ja.wikipedia.org/wiki/Move_To_Front "wikilink")、[ハフマン符号](https://ja.wikipedia.org/wiki/ハフマン符号 "wikilink")化法を用いており、従来の[gzip](https://ja.wikipedia.org/wiki/gzip "wikilink")や[ZIPといったデータ圧縮法と比べ](https://ja.wikipedia.org/wiki/ZIP_\(ファイルフォーマット\) "wikilink")、より高い圧縮率を誇っている。また、bzip2の操作法は意図的にgzipに似せてあり、gzipからの移行は容易である。しかしながら、bzip2は処理速度の点でgzipよりも劣っており、gzipを完全に置換するには至らず、また高圧縮率のフォーマットとしては[xzも登場している](https://ja.wikipedia.org/wiki/Xz_\(ファイルフォーマット\) "wikilink")。しかし、[StuffIt](https://ja.wikipedia.org/wiki/StuffIt "wikilink")や[7-Zip](https://ja.wikipedia.org/wiki/7-Zip "wikilink")といった高圧縮プログラムと比べれば圧縮率もそこそこ良い割に高速に動作する。

bzip2は、ネットワーク経由で配布される比較的サイズの大きなファイルの圧縮に用いられることが多く、代表的なものとしては、[Linuxカーネル](https://ja.wikipedia.org/wiki/Linuxカーネル "wikilink")のソースコード群が挙げられる。

bzip2の原型である **bzip** は圧縮[アルゴリズム](../Page/アルゴリズム.md "wikilink")に[算術符号](https://ja.wikipedia.org/wiki/算術符号 "wikilink")を利用しているため、算術符号関係の[特許](https://ja.wikipedia.org/wiki/特許 "wikilink")による制約のために開発が継続不能とされた、という経緯がある。

## 脚注

## 外部リンク

  - [The bzip2 and libbzip2 home page](https://www.sourceware.org/bzip2/)（英語）

[Category:データ圧縮規格](https://ja.wikipedia.org/wiki/Category:データ圧縮規格 "wikilink") [Category:1996年のソフトウェア](https://ja.wikipedia.org/wiki/Category:1996年のソフトウェア "wikilink")

1.
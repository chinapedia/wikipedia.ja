> この記事は[LZX](https://ja.wikipedia.org/wiki/LZX)から翻訳されています。


**LZX** は、[LZ77](https://ja.wikipedia.org/wiki/LZ77 "wikilink")から派生した[データ圧縮](../Page/データ圧縮.md "wikilink")[アルゴリズム](../Page/アルゴリズム.md "wikilink")の一種。また、そのアルゴリズムを使った[ファイル・アーカイバを指す](../Page/アーカイブ_\(コンピュータ\).md "wikilink")。Jonathan Forbes と Tomi Poutanen が考案した。

## LZXアルゴリズム応用の具体例

### Amiga LZX

LZX は1995年、[Amiga](../Page/Amiga.md "wikilink")用ファイル・アーカイバとしてリリースされた。当時、作者ら（Forbes と Poutanen）は[カナダ](https://ja.wikipedia.org/wiki/カナダ "wikilink")の[ウォータールー大学](../Page/ウォータールー大学.md "wikilink")の学生だった。当時の圧縮ソフトとしては一般的な[シェアウェア](../Page/シェアウェア.md "wikilink")としてのリリースだった。登録版には試用版にはないバグ修正と改良が含まれていた。[1997年](https://ja.wikipedia.org/wiki/1997年 "wikilink")、作者らはキーファイルを無料で公開して以降の開発と登録作業を止めることにし、それによって誰でも登録版を使えるようになった。

### [Microsoft Cabinet](../Page/CAB.md "wikilink") ファイル

1997年、Forbes は[マイクロソフト](../Page/マイクロソフト.md "wikilink")に入社し、マイクロソフトの[CAB](../Page/CAB.md "wikilink")アーカイバにLZXアルゴリズムが採用された。Amiga 版 LZX では探索ウィンドウサイズが64[KiBで固定だったが](https://ja.wikipedia.org/wiki/キビバイト "wikilink")、マイクロソフト版では32KiBから2048KiBまで2のべき乗でウィンドウサイズを指定可能であった。また特別な[プリプロセッサ](../Page/プリプロセッサ.md "wikilink")が追加され、[x86](https://ja.wikipedia.org/wiki/x86 "wikilink") の "CALL" 命令を検出してそのオペランドを相対アドレッシングから絶対アドレッシングに書き換える処理を行った。それにより、同じルーチンのCALL命令は同じパターンとなり、圧縮効率が高まった。

### [Microsoft Compressed HTML Help](https://ja.wikipedia.org/wiki/Microsoft_Compressed_HTML_Help "wikilink") (CHM) ファイル

この[オンラインヘルプ](../Page/オンラインヘルプ.md "wikilink")の形式では、HTMLデータをLZXアルゴリズムで圧縮するようになった。しかし、ランダムアクセスの速度を向上させるため、圧縮ルーチンは64KiB毎にリセットされ、32KiB毎に16ビット境界に再整列するよう変更された。そのため、全体を一度に伸張する必要はなく、直近の64KiBまで高速にシークでき、そこから再度伸張可能となっている。

### Microsoft EBook Reader (LIT) ファイル

LITファイルはCHMのファイル形式を単純に拡張したもので、やはりLZX圧縮を行っている。

### Windows Imaging Format (WIM) ファイル

[Windows Imaging Format](https://ja.wikipedia.org/wiki/Windows_Imaging_Format "wikilink") は [Windows Vista](https://ja.wikipedia.org/wiki/Microsoft_Windows_Vista "wikilink") のインストール/ディスクイメージ用ファイル形式であり、圧縮に LZX を使っている。

## LZXファイルの伸張

Amiga 版 LZX では、**unlzx** プログラムで伸張を行う。CABファイル形式では、LZXで圧縮されているものは **cabextract** プログラムで伸張できる。CHM形式のファイルを伸張してHTMLファイルを取り出すプログラムは各種存在する（[CHMの記事参照](../Page/Microsoft_Compiled_HTML_Help.md "wikilink")）。LITファイルは **Convert LIT** というソフトウェアを使って伸張可能。

## 外部リンク

  - [The LZX page](http://xavprods.free.fr/lzx/) Amiga 版 LZX アーカイバをダウンロード可能
  - [aminet](http://main.aminet.net/misc/unix/) unlzx のソースコードをダウンロード可能
  - [Convert LIT](http://www.convertlit.com/) ソースコードもある。

[Category:データ圧縮](https://ja.wikipedia.org/wiki/Category:データ圧縮 "wikilink")
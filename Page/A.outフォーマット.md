> この記事は[A.out](https://ja.wikipedia.org/wiki/A.out)から翻訳されています。


**a.outフォーマット**は、[UNIX](../Page/UNIX.md "wikilink")における最初の[実行ファイル](../Page/実行ファイル.md "wikilink")および[リンク可能ファイルの](../Page/リンケージエディタ.md "wikilink")[ファイルフォーマット](../Page/ファイルフォーマット.md "wikilink")である。名前は、[コンパイラ](../Page/コンパイラ.md "wikilink")の出力するファイルのデフォルトの名前がa.out（[アセンブラ](https://ja.wikipedia.org/wiki/アセンブラ "wikilink")アウトプット）であることから名付けられた。[Windows](https://ja.wikipedia.org/wiki/Windows "wikilink")上の[gcc](https://ja.wikipedia.org/wiki/gcc "wikilink")ではa.outファイルの代わりにa.exeを生成する。

## ファイル構造

実行可能a.outは3つのセクションを持つ。一つはTEXTと呼ばれる[コードセクションもう一つはDATAと呼ばれる](../Page/プログラム_\(コンピュータ\).md "wikilink")[データ](../Page/データ.md "wikilink")セクションそして、[ヘッダにサイズだけが記録されているBSSと呼ばれる](https://ja.wikipedia.org/wiki/ヘッダ_\(コンピュータ\) "wikilink")0初期化データセクションであり、この順番に配置されている。

ファイルヘッダの先頭に置かれる、識別[マジックナンバーはO](https://ja.wikipedia.org/wiki/マジックナンバー_\(フォーマット識別子\) "wikilink")_MAGIC(8進数で0407), NMAGIC(0410), QMAGIC(0413), ZMAGIC(0314)である。O_MAGICは最初に使われた形式で、コードもデータも区別無く連続して読み込まれる。このマジックナンバーは本来[PDP-11](../Page/PDP-11.md "wikilink")で、ヘッダを飛ばして実行を開始するようなジャンプ命令であり、[スタンドアローン](../Page/スタンドアローン.md "wikilink")のプログラムで使えるように設計されていた。N_MAGICはNew Magicの略で、基本的にO_MAGICと同じように連続してコードもデータも書かれているが、コード[セグメント](../Page/セグメント.md "wikilink")を読み込み可能領域にロードし、データセグメントを書き込み可能領域に配置するように設計されている。このことにより複数の同一プログラムを走らせるとき、コードを共有してプログラムの実行することが出来るようになっている。Z_MAGICはコード領域とデータ領域それぞれをページ境界に整列させたもので、このことにより[ページング](https://ja.wikipedia.org/wiki/ページング "wikilink")環境で、全てを読み込まなくても実行可能にすることで、実行開始を高速化したものである。Q_MAGICは、やはりページングに対応したファイルであるが、ファイル上でのコードの整列をやめ、実行ファイルの先頭を0ページではなく、1ページ目からマップすることで未初期化[ポインタ](../Page/ポインタ_\(プログラミング\).md "wikilink")[参照を検出できるようにし](../Page/参照_\(情報工学\).md "wikilink")、ヘッダやデータの先頭部分を実行コードページの一部として読み込み専用マップすることで、[ハードディスク](https://ja.wikipedia.org/wiki/ハードディスク "wikilink")容量が無駄になる事を防止したものである。

リンク可能ファイルには、[シンボル](../Page/シンボル.md "wikilink")情報や再配置情報が更につけ加わる。

## 欠点

問題点は、1つは[共有ライブラリ](https://ja.wikipedia.org/wiki/共有ライブラリ "wikilink")のサポートが難しいことであるが、[FreeBSD](../Page/FreeBSD.md "wikilink")等のいくつかのシステムにおいては実行ファイルとして、a.outのシンボル情報を残したファイルを使うことで、共有ライブラリを実装していた。また、[C++](../Page/C++.md "wikilink")等で必要な初期化セクション等の特殊な役割を持たせた部分がファイルフォーマットとしてサポートされていないことである。そのため、現在では[COFFまたは](https://ja.wikipedia.org/wiki/Common_Object_File_Format "wikilink")[ELFに役割を譲っている](../Page/Executable_and_Linkable_Format.md "wikilink")。

[Category:UNIX](https://ja.wikipedia.org/wiki/Category:UNIX "wikilink") [Category:オブジェクトファイルフォーマット](https://ja.wikipedia.org/wiki/Category:オブジェクトファイルフォーマット "wikilink")
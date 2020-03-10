> この記事は[Record-oriented filesystem](https://ja.wikipedia.org/wiki/Record-oriented_filesystem)から翻訳されています。


**レコード・オリエンテッド・ファイルシステム** (**record-oriented filesystem**) において、[ファイルは](../Page/ファイル_\(コンピュータ\).md "wikilink")[レコードの集まりを](https://ja.wikipedia.org/wiki/w:record_\(computer_science\) "wikilink")[ストア](https://ja.wikipedia.org/wiki/ストア "wikilink")したものである。通常、レコード・オリエンテッド・ファイルシステムはいくつかの異なったレコード・[フォーマットをサポートする](../Page/ファイルフォーマット.md "wikilink")。固定長データ、可変長データ、異なるレコード長、異なった物理編成など。 また、順次（シーケンシャル）、索引付き（キー・インデクスド）など、異なるアクセスメソッドをサポートする。

またファイルは [MVS](../Page/Multiple_Virtual_Storage.md "wikilink") の区分[データセット](../Page/データセット_\(IBMメインフレーム\).md "wikilink") (PDS, PO) のように、複数のメンバーに分けて扱われることもある。この編成は、[Hierarchical File Systemが一般的になる前の](../Page/Hierarchical_File_System.md "wikilink")、メインフレームシステムが持っていた伝統的な方式で、索引のような小さなディレクトリに依っている。

## 起源

レコード・オリエンテッド・ファイルシステムは特に、MVS、VM/CMS、DOS/VSE、[OS/400](https://ja.wikipedia.org/wiki/OS/400 "wikilink")、[VMS](https://ja.wikipedia.org/wiki/VMS "wikilink") などのような、[メインフレーム](../Page/メインフレーム.md "wikilink")や中型[コンピュータ](../Page/コンピュータ.md "wikilink")の[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink")と関係が深い。このようなシステムでは、オペレーティングシステムはファイルをあるフォーマットから異なるフォーマットにコンバートするユーティリティを提供する場合が多い。

[Unix](https://ja.wikipedia.org/wiki/Unix "wikilink")/[POSIX](../Page/POSIX.md "wikilink") などとは対照をなしていて、これらの PC/デスクトップ オペレーティングシステムのファイルシステムでは、ファイルを構造化されていない連続した[バイトの羅列として取り扱う](../Page/バイト_\(情報\).md "wikilink")。レコードの区切りは、各々の[アプリケーションソフトウェア](../Page/アプリケーションソフトウェア.md "wikilink")の次元で把握される。POSIX コンパチブルを目指した新しいレコード・オリエンテッド・ファイルシステムは、POSIX スタイルのストリーム・オリエンテッド・ファイルを同様にサポートする。

レコード・オリエンテッド・ファイルシステムは一般に、ビジネスデータ処理や [unit record equipment](https://ja.wikipedia.org/wiki/w:unit_record_equipment "wikilink") における [punched cards](https://ja.wikipedia.org/wiki/w:punched_cards "wikilink") の遺産を反映している。ファイルは、固定長のレコードを構成するパンチカードとしてストアされる。そのカードの長さは一般に80カラム、ときにはそれ以上である。

これはまた、[ソースコード](../Page/ソースコード.md "wikilink")の保存の仕方も反映している。Unix の下では、ソースコードは一般に、改行によって分けられた順次行として保存される。別の言葉でいえば、デリミッター付きの可変長レコードの集まりであるということができる。もっとも、それは単にコンパイラやエディターや他のいくつものツールによる慣例であるに過ぎないけれども。対照的に、多くのメインフレームシステムでは、ソースコードはスペースを詰めた80カラムの固定長レコードの集まりとしてストアされる。これは、もともとパンチカードを順に読み取ってソースコードをコンピュータに投入したことの名残である。

## ストリーム・オリエンテッド・ファイルシステムとの比較

今日では、UNIX のアプローチがよりポピュラーである。ストリーム・オリエンテッド・ファイルの擁護者は、そのシンプルさと、フレキシビリティを論ずる。特に、ファイルを扱うツールが、もはや異なる多くのファイルフォーマットに合わせる必要がないことを挙げる。シングルファイルフォーマットによる、UNIX 上で可能なたくさんのコマンドラインユーティリティを論ずる人もいる。彼らはまた、キーシーケンスアクセスメソッドなどのレコードオリエンテッドファイルの集まりは、オペレーティングシステムを複雑化させることなしに、アプリケーションやライブラリで取り扱えることを論ずる。

レコード・オリエンテッド・ファイルの擁護者は、いくつものファイルフォーマットやキーシーケンスドファイルをオペレーティングシステムでサポートすることが、いくつものアプリケーションが互換性のないファイルフォーマットを使えるようにすることはありそうにないことを論ずる。

## 関連項目

  - [ファイル編成法](../Page/ファイル編成法.md "wikilink")
  - [ファイルシステム](../Page/ファイルシステム.md "wikilink")
  - [データセット (IBMメインフレーム)](../Page/データセット_\(IBMメインフレーム\).md "wikilink")
  - [MVS](../Page/Multiple_Virtual_Storage.md "wikilink")

[Category:OSのファイルシステム](https://ja.wikipedia.org/wiki/Category:OSのファイルシステム "wikilink") [Category:IBM](https://ja.wikipedia.org/wiki/Category:IBM "wikilink")
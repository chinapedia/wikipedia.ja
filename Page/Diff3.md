> この記事は[Diff3](https://ja.wikipedia.org/wiki/Diff3)から翻訳されています。


**diff3**は、3つの[ファイルを行単位で比較し](../Page/ファイル_\(コンピュータ\).md "wikilink")、相違点を表示する[コマンドライン](https://ja.wikipedia.org/wiki/コマンドライン "wikilink")[ツールソフトウェア](https://ja.wikipedia.org/wiki/ツールソフトウェア "wikilink")である。また、その結果を用いて1つのファイルに統合することができる。主に[Unix系](../Page/Unix系.md "wikilink")の[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink") (OS) が備えているが、各自で[インストール](../Page/インストール.md "wikilink")することによって、[Windowsで使用することも可能](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")。

例えば、2人が同一のファイルを同時に編集していた場合、確認なしに単純に保存すると、先に保存した編集が失われることになる。このような編集の競合に対処するには、保存時に、ファイル内容が編集を開始した時のものと同一であるか確認する必要がある。

もし違っていたら、編集中に他人にファイルを変更されてしまったといえる。このときdiff3を用いれば、両者の編集を共に最新ファイルへと反映させることが出来るのである。

なお、通常diff3は処理のために[diff](https://ja.wikipedia.org/wiki/diff "wikilink")コマンドを実行するが、環境設定によってこれを別のプログラムに変更することも可能である。また、1つに限りファイル名を指定する代わりに **-** （[ハイフンマイナス](../Page/ハイフンマイナス.md "wikilink")）を指定することで、[標準入力](https://ja.wikipedia.org/wiki/標準入力 "wikilink")から読み込ませることも可能。

## 使用例

    diff3 -e -m MYFILE OLDFILE YOURFILE

*OLDFILE*から*YOURFILE*への全ての変更が*MYFILE*に統合される。

## 関連項目

  - [diff](https://ja.wikipedia.org/wiki/diff "wikilink")
  - [Help:編集の競合](https://ja.wikipedia.org/wiki/Help:編集の競合 "wikilink") - [MediaWiki](https://ja.wikipedia.org/wiki/MediaWiki "wikilink")もdiff3を使用して編集競合を自動的に統合する機構を備えている。
  - [Concurrent Versions System](../Page/Concurrent_Versions_System.md "wikilink")
  - [Apache Subversion](../Page/Apache_Subversion.md "wikilink")
  - [マージ (バージョン管理システム)](https://ja.wikipedia.org/wiki/マージ_\(バージョン管理システム\) "wikilink")

## 外部リンク

  - [Manpage of DIFF3](http://linuxjm.osdn.jp/html/gnumaniak/man1/diff3.1.html)（日本語）
  - [DiffUtils for Windows](http://gnuwin32.sourceforge.net/packages/diffutils.htm)（英語）

[Category:UNIXのソフトウェア](https://ja.wikipedia.org/wiki/Category:UNIXのソフトウェア "wikilink") [Category:オープンソースソフトウェア](https://ja.wikipedia.org/wiki/Category:オープンソースソフトウェア "wikilink") [Category:ファイル比較ツール](https://ja.wikipedia.org/wiki/Category:ファイル比較ツール "wikilink")
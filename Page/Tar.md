> この記事は[Tar](https://ja.wikipedia.org/wiki/Tar)から翻訳されています。


**tar**（ター、**t**ape **ar**chives）は[ファイルアーカイブの](https://ja.wikipedia.org/wiki/アーカイブ_\(コンピュータ\) "wikilink")[ファイルフォーマット](../Page/ファイルフォーマット.md "wikilink")の一種である 。このファイルフォーマットを処理する同名の[UNIX](../Page/UNIX.md "wikilink")コマンド`tar`も指す。UNIXでは圧縮したtar形式のファイルを"tarball"（ターボール）と呼ぶこともある。*[POSIX](https://ja.wikipedia.org/wiki/POSIX "wikilink").1-1988*\[1\]や*POSIX.1-2001*\[2\]で規格化され、UNIX系[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink")では標準のフォーマットである。[Windowsではあまり使われない](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")。類似コマンドにafioがある。

## 機能

[Targzip.svg](https://ja.wikipedia.org/wiki/File:Targzip.svg "fig:Targzip.svg") tarは[ファイルの](https://ja.wikipedia.org/wiki/ファイル_\(コンピュータ\) "wikilink")[アーカイブに用いられ](https://ja.wikipedia.org/wiki/アーカイブ_\(コンピュータ\) "wikilink")、多数のファイルを一つのファイルにまとめることができる。ファイルのユーザ情報とグループ情報、[パーミッション](https://ja.wikipedia.org/wiki/パーミッション "wikilink")、最終更新日時、[ディレクトリ](https://ja.wikipedia.org/wiki/ディレクトリ "wikilink")構造などを同時にアーカイブすることができる。元来tarはアーカイブ、すなわち複数のファイルをまとめることのみで[圧縮の機能はない](../Page/データ圧縮.md "wikilink")。大半の場合アーカイブと同時に[compressや](https://ja.wikipedia.org/wiki/UNIX_Compress "wikilink")[gzip](https://ja.wikipedia.org/wiki/gzip "wikilink")、[bzip2](https://ja.wikipedia.org/wiki/bzip2 "wikilink")などの圧縮方法を用いて圧縮（いわゆる「ソリッド圧縮」）を行う。これによりファイルの[拡張子](../Page/拡張子.md "wikilink")はそれぞれ .tar.Z、.tar.gz、.tar.bz2 となる。特に .tar.Z、.tar.gz は古くから使われておりそれぞれ略して .taz、.tgz とされることも多い。この形式はファイルが一部でも破損した場合、破損箇所に含まれていたファイル以降は取り出すことはできない。この欠点はafioとgzを使うことにより改善できる。

## コマンドオプション

  - \-c　新しいアーカイブを作成する
  - \-d　アーカイブ内のファイルをカレントディレクトリのファイルと比較する
  - \-r　アーカイブにファイルを追加する
  - \-t　アーカイブの内容をリスト表示する
  - \-x　アーカイブからファイルを取り出す
  - \-C *directory*　アーカイブからファイルを取り出して、指定したディリクトリに入れる
  - \-f *file*　テープの代わりに指定したファイルをアーカイブする
  - \-L *n*　テープの容量を*n*KBとする
  - \-N *date*　指定した日付よりも新しいファイルだけをアーカイブに入れる（取り出す）
  - \-T *file*　*file*で指定したファイルをアーカイブに入れる（取り出す）
  - \-v　詳細メッセージを表示する
  - \-z　アーカイブをgzipにフィルターする（GNU 拡張）
  - \-j　アーカイブをbzip2にフィルターする（GNU 拡張）
  - \-J　アーカイブをxzにフィルターする（GNU 拡張）

以下は、実際の圧縮・解凍のコマンド例である。

  - 圧縮

`tar -zcvf name.tar.gz directory`

`tar -cvf /dev/nst0 directory` (テープデバイスに記録する場合)

  - 解凍

`tar -zxvf name.tar.gz`

`tar -xvf /dev/nst0` (テープデバイスから読み出す場合)

  - テープ上のファイルのリストを表示

リスト表示したいアーカイブファイルの先頭にテープを移動させた後、以下を実行

`tar -tvf /dev/nst0`

## 歴史

tarコマンドはその名の通り[磁気テープ](https://ja.wikipedia.org/wiki/磁気テープ "wikilink")の操作が念頭に置かれていた。fオプション\[3\]を省いた場合[デフォルトで磁気テープデバイスを処理する](https://ja.wikipedia.org/wiki/デフォルト_\(コンピュータ\) "wikilink")。fオプションの指定によりファイルシステム上の任意の名前のファイルを処理できる。この語の由来は「」の童話『』に由来し\[4\]、それに油塊（タールボール）を引っ掛けたジョーク的用語である。 その歴史の長さゆえにシステム毎の方言やファイルサイズの制限など多くの非互換部分がある為、異なるシステム間のファイル交換を目的とする場合は慎重に利用する必要がある。

## 関連項目

  - [mt (UNIX)](https://ja.wikipedia.org/wiki/mt_\(UNIX\) "wikilink")
  - [テープドライブ](https://ja.wikipedia.org/wiki/テープドライブ "wikilink")
  - [Linear Tape-Open](https://ja.wikipedia.org/wiki/Linear_Tape-Open "wikilink")
  - [IBM 3592](https://ja.wikipedia.org/wiki/IBM_3592 "wikilink")

## 脚注

## 外部リンク

  - [Man page of TAR](https://linuxjm.osdn.jp/html/GNU_tar/man1/tar.1.html)
  - [TARファイル拡張子](http://www.hotfe.org/ja/data-files/tar-file-extension)
  - [tar(5) - FreeBSD File Formats Manual](https://www.freebsd.org/cgi/man.cgi?query=tar&sektion=5&manpath=FreeBSD+8-current)
  - [Tar - GNU Project](https://www.gnu.org/software/tar/)
  - [GNU tar format](https://www.gnu.org/software/tar/manual/html_node/Standard.html)

[Category:UNIXのソフトウェア](https://ja.wikipedia.org/wiki/Category:UNIXのソフトウェア "wikilink") [Category:ファイルフォーマット](https://ja.wikipedia.org/wiki/Category:ファイルフォーマット "wikilink")

1.  "IEEE Std 1003.1-1988, IEEE Standard for Information Technology - Portable Operating System Interface (POSIX)"
2.  "IEEE Std 1003.1-2001, IEEE Standard for Information Technology - Portable Operating System Interface (POSIX)"
3.  ファイル (file) の頭文字である。
4.  童話の日本語訳書は[アナンシ\#関連書籍](https://ja.wikipedia.org/wiki/アナンシ#関連書籍 "wikilink")を参照。
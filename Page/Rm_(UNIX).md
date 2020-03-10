> この記事は[Rm \(UNIX\)](https://ja.wikipedia.org/wiki/Rm_\(UNIX\))から翻訳されています。


**rm**（アールエム）は[POSIX](../Page/POSIX.md "wikilink")および[Single UNIX Specificationで規定されている](https://ja.wikipedia.org/wiki/Single_UNIX_Specification "wikilink")[コマンドである](https://ja.wikipedia.org/wiki/コマンド_\(コンピュータ\) "wikilink")。

rmは「remove」の略であり、[ファイルシステム](../Page/ファイルシステム.md "wikilink")より[ファイルを削除するために使用される](https://ja.wikipedia.org/wiki/ファイル_\(コンピュータ\) "wikilink")。[AT\&T](../Page/AT&T.md "wikilink") UNIXの最初のバージョンから存在していた。

## 振る舞い

rmは引数に指定されたファイルを削除する。デフォルトではディレクトリの削除は行なわない。-rや-Rオプションを使用すると、指定された[ディレクトリ](../Page/ディレクトリ.md "wikilink")以下の全ディレクトリツリーが削除される。引数のパスが . または .. で終わる場合はエラーとなる。

POSIXオプションを次に示す。

  - \-f 存在しないファイルを指定してもエラーを返さない。確認問い合わせをしない。
  - \-i すべての削除に対して問い合わせを表示する。
  - \-r または -R 指定以下のディレクトリツリーを削除する。

[スティッキービット](https://ja.wikipedia.org/wiki/スティッキービット "wikilink")のセットされているディレクトリ配下のファイルは、そのファイルの所有者かディレクトリの所有者か[スーパーユーザー](https://ja.wikipedia.org/wiki/スーパーユーザー "wikilink")でないと削除できない。

## 名前が `-` で始まるファイルの削除

rmコマンドの多くの実装では、`-` で始まるファイル名を引数に指定する目的で、オプション終了を意味する特殊オプション(`--` または `-`)が用意されている。例えば前者の場合、ファイル `-f` を削除する指定は `rm -- -f` とすれば良い。

ただし、これら特殊オプションが存在しなくとも、パス名を付加した `rm ./-f` とすることで回避可能である。

これらは **[mv (UNIX)](https://ja.wikipedia.org/wiki/mv_\(UNIX\) "wikilink")** や **[cp (UNIX)](https://ja.wikipedia.org/wiki/cp_\(UNIX\) "wikilink")** でも同様のことが言える。

## 注意事項

例えば、スーパーユーザーで以下のコマンドを実行するとファイルシステム /配下のファイルがすべて削除されてしまう。(一部ファイルを除く) `rm -rf /` または`rm -rf /*`

但し一部のLinux系OS(CentOS 5以降 RHEL3以降)ではエラーが返る事があるが、後者コマンドは前述したOSでも実行されてしまうので注意が必要である。

## 外部リンク

  - [Manpage of RM](https://linuxjm.osdn.jp/html/GNU_fileutils/man1/rm.1.html) man page、JM Project（GNU 版）
  - [rm(1)](https://docs.oracle.com/cd/E19455-01/816-3518/6m9ptvr47/index.html) man page（SunOS リファレンスマニュアル）
  - [rm(1)](https://nixdoc.net/man-pages/HP-UX/man1/rm.1.html) man page（HP-UX リファレンス）

[Category:標準UNIXプログラム](https://ja.wikipedia.org/wiki/Category:標準UNIXプログラム "wikilink")
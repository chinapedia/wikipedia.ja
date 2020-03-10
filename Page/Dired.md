> この記事は[Dired](https://ja.wikipedia.org/wiki/Dired)から翻訳されています。


**Dired**（**ディレクトリエディタ**の意）は、[ファイルシステム](../Page/ファイルシステム.md "wikilink")の[ディレクトリ](../Page/ディレクトリ.md "wikilink")を編集するコンピュータ・プログラム。典型的には、[Emacs](../Page/Emacs.md "wikilink")[テキストエディタ](../Page/テキストエディタ.md "wikilink")で特別なモードとして実行されるが、単独版も書かれている。最初のバージョンのDiredは、単独のプログラムとして[1974年](../Page/1974年.md "wikilink")に、SAILのStan Kugellによって書かれた\[1\]。これは[GNU Emacsの最も初期のバージョンに組み込まれ](../Page/GNU_Emacs.md "wikilink")\[2\]、[Cや](../Page/C言語.md "wikilink")[C++](../Page/C++.md "wikilink")で他の[OS](../Page/OS.md "wikilink")に再実装された\[3\]。

[Emacs](../Page/Emacs.md "wikilink")の中で動作するとき、Diredは、[ls](https://ja.wikipedia.org/wiki/ls "wikilink")のようなファイルのリストをEmacsのバッファに表示する。リストは標準的なナビゲーションコマンドを使って操作することができる。また、いくつかの[Emacs LispスクリプトがEmacsにおけるDiredを拡張するために書かれた](../Page/Emacs_Lisp.md "wikilink")。Tramp\[4\]と組み合わせると、[SSH](https://ja.wikipedia.org/wiki/SSH "wikilink")、[FTP](https://ja.wikipedia.org/wiki/FTP "wikilink")、[telnet](https://ja.wikipedia.org/wiki/telnet "wikilink")や多くの他のプロトコルを用いてリモートのファイルシステムにアクセスし、ファイルを編集できるとともに、同じセッションにおいて、他のユーザーとしてローカルファイルにアクセスすることもできる。また、複数のファイルをEmacsの検索と置換の機能経由でリネームできるようにする機能がある\[5\]ほか、複数のファイルを[正規表現](../Page/正規表現.md "wikilink")を用いてマークすることができる。一度マークされると、ファイルは削除、リネーム、外部のシェルコマンドやelispの機能を実行するなど、多くの操作を行うことができる。Lispパッケージのdired-x\[6\]を用いると、既存のlsに似た、ディレクトリのリスト表示を仮想的なDiredモードで行うこともできる。

## 脚注

### 出典

## 外部リンク

  - [Diredマニュアル](https://www.gnu.org/software/emacs/manual/html_node/emacs/Dired.html)

[Category:ファイルマネージャ](https://ja.wikipedia.org/wiki/Category:ファイルマネージャ "wikilink")

1.
2.  [Emacs NEWS.1-17 file](https://github.com/typester/emacs/blob/master/etc/NEWS.1-17)
3.  [DED](http://invisible-island.net/ded/)
4.
5.  [1](https://www.emacswiki.org/emacs/WDired)
6.
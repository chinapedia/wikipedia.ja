> この記事は[Ne \(\)](https://ja.wikipedia.org/wiki/Ne_\(\))から翻訳されています。


**ne**（"nice editor"の意）は[ミラノ大学](https://ja.wikipedia.org/wiki/ミラノ大学 "wikilink")のSebastiano Vignaによって開発されている[Linux](../Page/Linux.md "wikilink")や[macOS](https://ja.wikipedia.org/wiki/macOS "wikilink")のような[POSIX](../Page/POSIX.md "wikilink")準拠のOSのためのコンソール[テキストエディタ](../Page/テキストエディタ.md "wikilink")である。neは、[terminfo](https://ja.wikipedia.org/wiki/terminfo "wikilink")ライブラリを使っているが、[GNU](../Page/GNU.md "wikilink") [Termcap](https://ja.wikipedia.org/wiki/Termcap "wikilink")実装のデータベースを使ってもコンパイルでき、[Cygwin](../Page/Cygwin.md "wikilink")のバージョンもある。

尚、日本国内では、[VZ Editorライクなエディタである](../Page/VZ_Editor.md "wikilink")"NxEdit"もneのファイル名を利用している\[1\]\[2\]が、全く別のソフトウェアである。

neは、[POSIX](../Page/POSIX.md "wikilink")準拠のOSで移植可能で、低速なリモート接続でも使えるとともに、現代のユーザーと初心者にも扱いやすい[vi](https://ja.wikipedia.org/wiki/vi "wikilink")の代替となること\[3\]を目指している。[キーボードショートカットはviのコマンドモードの代わりに](../Page/ショートカットキー.md "wikilink")で終了、でファイルのオープンなど[GUI由来の物に準じた物になっている](https://ja.wikipedia.org/wiki/グラフィカルユーザインタフェース "wikilink")。[構文強調](../Page/シンタックスハイライト.md "wikilink")、[正規表現](../Page/正規表現.md "wikilink")、変更が可能な[メニューとキーバインド](https://ja.wikipedia.org/wiki/メニュー\(コンピュータ\) "wikilink")、[自動補完](https://ja.wikipedia.org/wiki/自動補完 "wikilink")など高度なテキストエディターで一般的な多くの機能をサポートしている。neは、デフォルトで選択されたテキストのブロックをを押下する事で[コマンドラインフィルタに](../Page/フィルタ_\(ソフトウェア\).md "wikilink")[パイプで引き渡すことができ](../Page/パイプ_\(コンピュータ\).md "wikilink")\[4\]、[UTF-8](../Page/UTF-8.md "wikilink")エンコーディングもサポートしており\[5\]、な実装となっている。

neはMartin Taillerferによって書かれた[Amiga](../Page/Amiga.md "wikilink") 3000TのTurboTextエディタに触発され\[6\]、[curses](https://ja.wikipedia.org/wiki/curses "wikilink")ライブラリを使用して開発された。 その後、terminfoライブラリを活用するために[Linux](../Page/Linux.md "wikilink")に開発は移行した。Todd Lewisが開発チームに加わり、[ノースカロライナ大学チャペルヒル校](../Page/ノースカロライナ大学チャペルヒル校.md "wikilink")で必要な機能を加えるコードを寄付した。これは、neを彼らの研究用の[MVS](https://ja.wikipedia.org/wiki/MVS "wikilink")から[UNIX](../Page/UNIX.md "wikilink")への移行の一部として実装したものだった。Daniele Filarettiは、[Joeからのコードを使って構文強調について協力した](https://ja.wikipedia.org/wiki/:en:Joe's_Own_Editor "wikilink")\[7\]。

バージョン2.6は、[ファイル](https://ja.wikipedia.org/wiki/ファイル "wikilink")を開く画面に[逐次検索が追加され](../Page/インクリメンタルサーチ.md "wikilink")、開いているドキュメントのリストのステータスインジケータの追加によって構文強調を改善した。バージョン3.1.0は[64ビット](https://ja.wikipedia.org/wiki/64ビット "wikilink")をフルサポートし、ファイルサイズと行の長さは利用可能な[メモリ](https://ja.wikipedia.org/wiki/メモリ "wikilink")と[ディスク](https://ja.wikipedia.org/wiki/ディスク "wikilink")スペースによってのみ制限され、大きなファイルは透過的にメモリにマッピングされる。

誌はneをLinuxの 3番目に優れたエディターとして評価している\[8\]。

## 脚注

### 出典

[Category:テキストエディタ](https://ja.wikipedia.org/wiki/Category:テキストエディタ "wikilink") [Category:オープンソースソフトウェア](https://ja.wikipedia.org/wiki/Category:オープンソースソフトウェア "wikilink") [Category:UNIXのソフトウェア](https://ja.wikipedia.org/wiki/Category:UNIXのソフトウェア "wikilink")

1.  [涙とともに、夜な夜なパンを齧った ―: 使い方(1) Vzエディターライクな、エディターの使い方 NxEdit](https://poor-user.blogspot.com/2015/06/vz-nxedit.html)
2.  [ne (NxEdit)の詳細情報 : Vector ソフトを探す！](https://www.vector.co.jp/soft/unix/writing/se116961.html)
3.  [20 Text Editors for Linux Overview & Screenshots | TuxArena](http://www.tuxarena.com/2011/06/20-text-editors-for-linux-overview-screenshots/)
4.  [More Advanced Features - ne's manual](http://ne.dsi.unimi.it/docs/More-Advanced-Features.html#More-Advanced-Features)
5.  [Feature request: properly support zero-length 'characters' · Issue \#29 · vigna/ne · GitHub](https://github.com/vigna/ne/issues/29)
6.  [History - ne's manual](http://ne.di.unimi.it/docs/History.html#History)
7.
8.
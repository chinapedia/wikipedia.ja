> この記事は[Nano \(テキストエディタ\)](https://ja.wikipedia.org/wiki/Nano_\(テキストエディタ\))から翻訳されています。


**nano**（ナノ）は、[UNIX](../Page/UNIX.md "wikilink")を中心としたシステムで使われる、[curses](https://ja.wikipedia.org/wiki/curses "wikilink")を使った[テキストエディタ](../Page/テキストエディタ.md "wikilink")の一種である。

スクリーンエディタの一種でありながら、[CUIを用いて編集を行なうことが可能である](../Page/キャラクタユーザインタフェース.md "wikilink")。スクリーンエディタとして有名なものは既に多数存在するが、このエディタの特色は、その操作方法が[WYSIWYG](../Page/WYSIWYG.md "wikilink")に慣れたユーザにとって分かりやすいため、初心者でも比較的容易に扱うことが可能という点にある。

## 歴史

GNU nanoは、最初[1999年](../Page/1999年.md "wikilink")に、TIP（TIP Isn't Pico）という名前で、Chris Allegrettaによって作られた。彼のモチベーションは、フリーではないライセンスで配布されているPicoのフリーソフトウェアの代替物を作ることであった。[2000年](../Page/2000年.md "wikilink")[1月10日](../Page/1月10日.md "wikilink")に、ソフトの名称はnanoに変更された。これは既存の[Unix](https://ja.wikipedia.org/wiki/Unix "wikilink")ユーティリティ[tip](https://ja.wikipedia.org/wiki/tip "wikilink")とのコンフリクトを避けるためである。2001年2月、nanoは[GNUプロジェクト](../Page/GNUプロジェクト.md "wikilink")の一部となった。

GNU nanoは、Picoには欠けているいくつかの機能、シンタクスハイライティング、行番号の表示、[正規表現](../Page/正規表現.md "wikilink")を用いた検索や置換、ライン毎のスクロール、複数のバッファ、グループにわけた行毎のインデント、変更可能なキーバインディング\[1\]、編集のリドゥとアンドゥなどを補完している\[2\]。

[2003年](../Page/2003年.md "wikilink")[8月11日](../Page/8月11日.md "wikilink")、Chris Allgrettaは、公式にソースコードのメンテナンスを、David Lawrence Ramseyに任せた\[3\]。しかし、[2007年](../Page/2007年.md "wikilink")[12月20日](../Page/12月20日.md "wikilink")にRamseyはnanoのメンテナの立場から降りている\[4\]。

2016年6月、nanoプロジェクトの代表開発者と他のアクティブなメンバーは、GNUプロジェクトを離れることに合意した。これは、[FSF](https://ja.wikipedia.org/wiki/FSF "wikilink")の著作権の割り当てに関するポリシーに対する意義に基づくもので、彼らは脱中心化されたコピーライトの所持は[GNU GPLの強化を邪魔することがないと考えていた](https://ja.wikipedia.org/wiki/GNU_GPL "wikilink")\[5\]。このステップは[Debian](../Page/Debian.md "wikilink")と[Arch Linuxで認められ](https://ja.wikipedia.org/wiki/Arch_Linux "wikilink")、GNUプロジェクトはこの移動を"フォーク"と呼んでこれに抵抗した\[6\] 。[2016年](../Page/2016年.md "wikilink")[8月19日](../Page/8月19日.md "wikilink")、Chris Allgrettaは、GNUによるnanoに関する特別なコピーライトに関する譲歩を受け\[7\]、GNUファミリーにプロジェクトを戻すことをアナウンスした。バージョン2.7.0はこの後、2016年9月にリリースされている\[8\]。

## ライセンス

nanoは、[GPLのもとで配布されている](../Page/GNU_General_Public_License.md "wikilink")。

## 使用上の特徴

nanoは[vi](https://ja.wikipedia.org/wiki/vi "wikilink")と異なり、起動すれば即[キーボードより文字入力が可能であり](../Page/キーボード_\(コンピュータ\).md "wikilink")、直感的な操作が可能である。入力位置は[方向キー](../Page/方向キー.md "wikilink")を使って自由に指定が可能である。 [ファイルの読み書きや検索のようなコマンドは](../Page/ファイル_\(コンピュータ\).md "wikilink")[コントロールキー](../Page/コントロールキー.md "wikilink")または[メタキー](../Page/メタキー.md "wikilink")の組み合わせによって実行するが、常に画面の下部に主要なキー割り当てが表示されているため、操作方法を知らないユーザでも扱う事が出来る。それ以外のキー割り当てについては、^G（ヘルプ）を押すことで知ることができる。 最近の主要な[Linuxディストリビューション](../Page/Linuxディストリビューション.md "wikilink")や[macOS](https://ja.wikipedia.org/wiki/macOS "wikilink")では標準で同梱されているが、[Emacs](../Page/Emacs.md "wikilink")や[vim](https://ja.wikipedia.org/wiki/vim "wikilink")といった高機能なエディタに比べて、機能面では制約がある。

nanoの元になったpicoは、1ファイルのみが編集できる単純なエディタであったが、nanoでは大きく拡張されており、[バッファ](../Page/バッファ.md "wikilink")を切り替えて複数のファイルが編集できたり、検索に[正規表現](../Page/正規表現.md "wikilink")が使えたり、[シンタックスハイライト](../Page/シンタックスハイライト.md "wikilink")に対応するなど、必ずしも単純とは言えないエディタになっている。

## 脚注

## 外部リンク

  -
[Category:テキストエディタ](https://ja.wikipedia.org/wiki/Category:テキストエディタ "wikilink") [Category:GNOME](https://ja.wikipedia.org/wiki/Category:GNOME "wikilink")

1.
2.
3.
4.
5.  [nano news](https://nano-editor.org/news.php) on nano-editor.org *"And, with this release, we take leave of the herd... Bye\! And thanks for all the grass\!"* (22 June 2016)
6.  [I'm on the GNU maintainers team; I want to clarify a couple things about this: First, Nano has _not_ left the GNU project](https://news.ycombinator.com/item?id=11953044) on news.ycombinator.com by Mike Gerwitz (June 2016)
7.
8.  [nano news](https://nano-editor.org/news.php) on nano-editor.org *"With this release we return to GNU. For just a little while we dreamt we were tigers. But we are back in the herd, back to a healthy diet of fresh green free grass."* (1 September 2016)
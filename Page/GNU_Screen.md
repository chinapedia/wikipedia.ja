> この記事は[GNU Screen](https://ja.wikipedia.org/wiki/GNU_Screen)から翻訳されています。


**GNU Screen**（グニュー・スクリーン、**screen**）は、[GNUプロジェクト](../Page/GNUプロジェクト.md "wikilink")によって開発された[フリーな](../Page/フリーソフトウェア.md "wikilink")[端末](../Page/端末.md "wikilink")多重接続[ソフトウェア](../Page/ソフトウェア.md "wikilink")である。1台の端末や接続したリモートの端末から、全く別々の複数の端末へと同時に接続する事が出来る。[コマンドライン上で複数のプログラムを実行したり](../Page/コマンドラインインタプリタ.md "wikilink")、[シェル](../Page/シェル.md "wikilink")上で[プログラムを実行させたまま接続を解除したりすることができる](../Page/プログラム_\(コンピュータ\).md "wikilink")。

## 機能

GNU Screenは、[GUIにおける](https://ja.wikipedia.org/wiki/グラフィカルユーザインタフェース "wikilink")[ウィンドウマネージャ](https://ja.wikipedia.org/wiki/ウィンドウマネージャ "wikilink")の[CUI版と考える事も出来る](../Page/キャラクタユーザインタフェース.md "wikilink")。ユーザが単一の[インターフェース内で効率的にプログラムを使用する為の機能を提供したり](../Page/ユーザインタフェース.md "wikilink")、複数のCUIテキストプログラムを同時に実行する為のラッパーとなる。

### 柔軟な接続機能

[VNCと同じく](https://ja.wikipedia.org/wiki/Virtual_Network_Computing "wikilink")、GNU Screenは1台の[コンピュータ](../Page/コンピュータ.md "wikilink")で[アプリケーションを起動し](../Page/アプリケーションソフトウェア.md "wikilink")、別のコンピュータから接続し直しても、起動したアプリケーションを再起動する事無くそのまま使い続ける事が出来る。これで、例えば自宅と職場のように、場所を移動しながら同じ作業を続ける事が出来るようになる。ユーザが異なる端末で接続したり切断したりしても、アプリケーションはそれを意識せず動き続けるのである。

### 多重ウィンドウ

接続した複数の端末には通常それぞれ1つずつアプリケーションが起動しており、ウィンドウには番号が割り振られ、ユーザはキーボード操作で、GUIの[端末エミュレータ](https://ja.wikipedia.org/wiki/端末エミュレータ "wikilink")に搭載されているタブ機能のようにそれらを切り替えつつ作業が出来る。それぞれのウィンドウは出力内容を一定量保存するバッファが存在し、ウィンドウを表示していなくても（たとえ接続していなくても、GNU Screenさえ動いていれば）、あとでそれらを見たり、コピーやペーストをする事も可能である。ウィンドウは分割する事も出来、分割した各ウィンドウ間を自由に行き来出来る。分割数に制限はない。ウィンドウの分割機能は、（[Emacs](../Page/Emacs.md "wikilink")や[Vim](../Page/Vim.md "wikilink")等のように）搭載されているアプリケーションも存在するが、GNU Screenを使用すればいかなるアプリケーションでも分割機能が使用出来る。

### 接続の共有

GNU Screenを使用すれば、複数のコンピュータが一度に接続を共有し、複数のユーザ間で共同作業を行う事が出来る。同じコンピュータに一度に同時接続する事で、マルチモニタの代替としても機能する。

## 他の類似ソフト

  - dtach
  - Text windows (Twin)
  - splitvt
  - tmux

## 関連項目

  - [tmux](https://ja.wikipedia.org/wiki/tmux "wikilink")
  - [Byobu](https://ja.wikipedia.org/wiki/Byobu "wikilink")

## 外部リンク

  - [GNU's Screen オフィシャルサイト](http://www.gnu.org/software/screen)
  - [GNU Screen](http://savannah.gnu.org/projects/screen/) [GNU Savannahのサイト](https://ja.wikipedia.org/wiki/GNU_Savannah "wikilink")
  - [GNU Screen](http://www.linuxmanpages.com/man1/screen.1.php) screenのmanpage
  - [Screenユーザーズマニュアル](http://www.delorie.com/gnu/docs/screen/screen_toc.html)
  - [Screen tutorial](http://linux.talkera.org/multiple-workspaces-on-a-single-terminal-in-linux/)

[Category:オープンソースソフトウェア](https://ja.wikipedia.org/wiki/Category:オープンソースソフトウェア "wikilink") [Category:GNUプロジェクト](https://ja.wikipedia.org/wiki/Category:GNUプロジェクト "wikilink") [Category:1987年のソフトウェア](https://ja.wikipedia.org/wiki/Category:1987年のソフトウェア "wikilink")
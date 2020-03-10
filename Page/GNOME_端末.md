> この記事は[GNOME ](https://ja.wikipedia.org/wiki/GNOME_)から翻訳されています。


**GNOME 端末**（グノームたんまつ、）は、[デスクトップ環境](https://ja.wikipedia.org/wiki/デスクトップ環境 "wikilink")[GNOME](../Page/GNOME.md "wikilink")に付属する[端末エミュレータ](https://ja.wikipedia.org/wiki/端末エミュレータ "wikilink")である。[ハボック・ペニントン](https://ja.wikipedia.org/wiki/ハヴォック・ペニントン "wikilink")（Havoc Pennington）らによって作成された。

## 概要

伝統的な[UNIX](../Page/UNIX.md "wikilink")の[コマンドラインベースの操作ではなく](https://ja.wikipedia.org/wiki/コマンドラインインタフェース "wikilink")[GUI](https://ja.wikipedia.org/wiki/グラフィカルユーザインタフェース "wikilink")[デスクトップ](https://ja.wikipedia.org/wiki/デスクトップ "wikilink")を提供するのがGNOMEデスクトップ環境の目的であるが、従来のコマンドラインインターフェースとの親和性も重視している。GNOME端末を使用することにより、デスクトップ環境を実行したままコマンドライン[シェル](../Page/シェル.md "wikilink")を利用することができる。GNOME端末は、他のウィンドウと全く同じように[ウィンドウ](../Page/ウィンドウ.md "wikilink")の位置を動かしたり大きさを変えたり、別の仮想デスクトップに移動することができるという利点を持つ。

## 特徴

GNOME端末は、[xterm](https://ja.wikipedia.org/wiki/xterm "wikilink")に非常によく似ており、ほぼ同じような特徴をもつ。\[1\]色付き文字（よく使われるものに[lsコマンドの出力などがある](../Page/LS.md "wikilink")）や、ウィンドウ内でのマウスイベントのサポートなどの重要な機能も備わっている。タブ機能などの独自の機能もある。

### プロファイル

GNOME端末は複数のプロファイルをサポートしている。\[2\]ユーザーは自身のアカウントごとに複数のプロファイルを作成することができる。ユーザーはプロファイルごとに設定を変更することができ、プロファイルに名前をつけることができる。プロファイルで設定できるのはフォント、色、ベル、スクロールの挙動、[バックスペースキー](https://ja.wikipedia.org/wiki/バックスペースキー "wikilink")と[削除キー](https://ja.wikipedia.org/wiki/削除キー "wikilink")の挙動である。

GNOME端末を起動すると、ユーザーのデフォルトのシェルが立ち上げられるかもしくは個別に設定したコマンドが実行される。これらの設定はプロファイルごとに設定でき、ユーザーはプロファイルごとに異なるコマンドを実行することができる。例えば、あるプロファイルはデフォルトのシェルを立ち上げるプロファイル、別のプロファイルはリモートのコンピュータに[SSHで接続するプロファイル](../Page/Secure_Shell.md "wikilink")、さらに[GNU Screenを開くプロファイルを持っている人がいるかもしれない](../Page/GNU_Screen.md "wikilink")。

### 互換性

GNOME端末にはいくつかのキーボードからASCIIへの割り当てに依存した古いソフトウェアに対応するいくつかの異なる互換性オプションがある。コンピュータを使用するとき、Back SpaceキーとDeteleキーについて曖昧さがある。バックスペースキーを押すとき、コンピュータはカーソルの前の文字を消すかもしれないし、カーソル位置の文字を消すかもしれない（[ASCII](https://ja.wikipedia.org/wiki/ASCII "wikilink")も参照）。GNOME端末では、どの[制御文字](../Page/制御文字.md "wikilink")もしくは[エスケープシーケンス](../Page/エスケープシーケンス.md "wikilink")をバックスペースキーもしくは削除キーが生成するかをユーザーが指定することができる。\[3\]ユーザーはこのオプションをプロファイルごとに指定することができる。

### 色付き文字

[Linux_command-line._Bash._GNOME_Terminal._screenshot.png](https://ja.wikipedia.org/wiki/File:Linux_command-line._Bash._GNOME_Terminal._screenshot.png "fig:Linux_command-line._Bash._GNOME_Terminal._screenshot.png") GNOME端末では色付き文字が利用できるが、この機能をオフにすることも可能である。GNOME端末は16色の基本セットをサポートしており、ユーザーがその色を指定することができる。\[4\]さらに、GNOME端末はデフォルトで256色パレットをサポートする。いくつかのプログラム、例えば[vim](https://ja.wikipedia.org/wiki/vim "wikilink")では、そのたくさんの色を使うことができる。\[5\]

### 背景

GNOME端末は数多くの背景のオプションをサポートする：\[6\]

1.  **単色**。ユーザーはプロファイルごとにある色を指定する。色はGNOMEデスクトップ上で利用できる何百万のもの色から用いることができる。
2.  **背景画像**を指定することもできる。GNOME端末はJPEG、PNG、GIF、TIFFといったたいていの画像形式をサポートしている。
3.  **透過背景**。ユーザーは（完全に不透明なものから完全に透明なものまで）好きな透明度を選択できる。もしユーザーが合成オプションをオンにしていれば、背景は端末の画面の後ろの画面が透けて見える。合成をオフにしている場合はユーザーのデスクトップの背景が透けて見える。半透明な背景はユーザーが端末の裏側のテキストをコマンドラインにコマンドを入力するときに読むことができるように意図されている。

Gnome端末3.8以降では透過背景オプションは削除された。\[7\]

### マウス操作

GNOME端末は何よりもまずコマンドラインインターフェイスでありほとんどの入力にはキーボードが使われるが、GNOME端末はマウス操作もいくらかサポートしている。GNOME端末はマウススクロールと左右のクリックをとらえることができる。\[8\]目下、マウスの位置を特定するとこはできないが、[aptitude](https://ja.wikipedia.org/wiki/aptitude "wikilink")や[vim](https://ja.wikipedia.org/wiki/vim "wikilink")といったいくつかの端末上のアプリケーションがマウス操作を利用することができる。今のところ、ジェスチャーに基づいたタッチはサポートされていない。

### URLの特定

GNOME端末は出力を解釈し、自動的にURLやEメールアドレスと思われるテキストの断片を特定する。\[9\]ユーザーがURLを指すと、テキストに自動的にアンダーラインが引かれ、クリックできることを示す。クリックすることによって適切なアプリケーションがリソースにアクセスするために開く。

### タブ

GNOME端末はタブをサポートしている\[10\]ユーザーはいくつもの画面を開く代わりにタブで開くことができる。タブバーはスクリーンの上部にボタンのように現れ、ユーザーはそれをクリックすることでタブを切り替えられる。タブの目的はごちゃごちゃしたタスクバーのかわりにユーザーが端末を整理する際の操作性を改良することにある。プロファイルと同様にタブごとに名前を指定できる。

ユーザビリティーを改良するためにタブに関する全ての操作はキーボードショートカットを利用して行うことができる。デフォルトでは、新しいタブの作成はControl + Shift + T、タブを閉じる操作はControl + Shift + Wで行うことができる。次のタブ・前のタブへはそれぞれControl + Shift + PageDown、Control + Shift + PageUpを押せば良い。

### 安全な終了

最近のバージョンでは、ユーザーが全てのグラフィカルなアプリケーションを終了させようとした時、GNOME端末は本当に終了させてよいか確認するダイアログボックスを表示する。\[11\]この機能は（例えばウインドウの閉じるボタンをクリックすることによって）誤って端末ウインドウを閉じるリスクを減らすためにある。もしジョブの実行中にユーザーがウインドウを閉じると、ジョブは終了してしまい、ジョブの終了が事故であるならユーザーはジョブを再スタートさせなければならない。

この機能はユーザーがグラフィカルインターフェイスでアプリケーションを閉じるときのみ存在する。ユーザーがexitシェルコマンドで終了しようとした時、終了の確認はユーザーのシェルの責任となる。GNOME端末の機能ではなく、例えば[tcsh](https://ja.wikipedia.org/wiki/tcsh "wikilink")や[bash](https://ja.wikipedia.org/wiki/bash "wikilink")といったいくつかのシェルは、似たような機能を提供していて、停止されたジョブがあるとき確認してくる。

## 出典

## 関連項目

  - [Konsole](https://ja.wikipedia.org/wiki/Konsole "wikilink") - [KDE](../Page/KDE.md "wikilink")における標準の端末エミュレータ

## 外部リンク

  -
[Category:端末エミュレータ](https://ja.wikipedia.org/wiki/Category:端末エミュレータ "wikilink") [Category:GNOME](https://ja.wikipedia.org/wiki/Category:GNOME "wikilink") [Category:GTK+を使用するソフトウェア](https://ja.wikipedia.org/wiki/Category:GTK+を使用するソフトウェア "wikilink") [Category:オープンソースソフトウェア](https://ja.wikipedia.org/wiki/Category:オープンソースソフトウェア "wikilink")

1.
2.
3.
4.
5.
6.  <http://www.youtube.com/watch?v=4g3LuRwDXLg>
7.  <https://launchpad.net/~gnome3-team/+archive/gnome3-staging/+sourcepub/3077123/+listing-archive-extra>
8.
9.
10.
11.
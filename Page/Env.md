> この記事は[Env](https://ja.wikipedia.org/wiki/Env)から翻訳されています。


**env**（エンブ）は [Unix系](../Page/Unix系.md "wikilink")[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink") (OS) で使われる[ユーティリティ](https://ja.wikipedia.org/wiki/ユーティリティ "wikilink")である。[環境変数](../Page/環境変数.md "wikilink")のリストを出力したり、現在の環境を変えることなく異なる環境変数の下で他の[コマンドを実行するのに使われる](https://ja.wikipedia.org/wiki/コマンド_\(コンピュータ\) "wikilink")。envを使うことで、変数の追加や削除、変数の値の変更を行える。

また、上記のような本来の目的以外に、[インタプリタ](../Page/インタプリタ.md "wikilink")を起動するための一種のトリックによく使われる。[スクリプトでインタプリタの起動を仲介する目的に使われ](../Page/スクリプト言語.md "wikilink")、その用途では通常は、環境に手を加えることはしない。

## 例

### 通常の用法

新しいシェルに対して環境をクリアするには

``` bash
env -i /bin/sh
```

[X Window System](../Page/X_Window_System.md "wikilink")[アプリケーション](../Page/アプリケーションソフトウェア.md "wikilink")[xcalc](https://ja.wikipedia.org/wiki/xcalc "wikilink")を起動し、異なる[ディスプレイに表示させるには](../Page/ディスプレイ_\(コンピュータ\).md "wikilink")

``` bash
env DISPLAY=foo.bar:1.0 xcalc
```

### トリック的用法

[UNIX](../Page/UNIX.md "wikilink")の[シバンでは通常は](../Page/シバン_\(Unix\).md "wikilink")、インタプリタのフルパスを与える必要がある。しかしUnix系OSでは、標準の[プログラムを](../Page/プログラム_\(コンピュータ\).md "wikilink")/usr/binに、管理者が独自に追加したプログラムを/usr/local/binに置いて区別して管理する ([FHS](https://ja.wikipedia.org/wiki/Filesystem_Hierarchy_Standard "wikilink")) といった理由などから、インタプリタのフルパスがシステムにより異なる。そのため、インタプリタのフルパスを直接に記述すると、その[シェルスクリプト](../Page/シェルスクリプト.md "wikilink")に汎用性がなくなる（他のシステムでは動かない可能性がある）。そこで、（インタプリタ自体があらかじめ環境変数PATHで指定されているディレクトリに置いてあることを前提に）フルパスではなく単なるコマンド名を記述してenvに実行させれば、汎用性が保てる。

以下に非常に単純な [Python](../Page/Python.md "wikilink") スクリプトを示す。

``` python
#!/usr/bin/env python
print "Hello World."
```

この例のように、インタプリタの代わりにenvを指定することで、スクリプトの実行時にPATHからインタプリタが検索され実行される。これにより同じスクリプトが、より多くの環境で動く可能性が高くなる。一方で、PATHから検索されるために、例えばユーザのホームディレクトリの下にある同名のプログラムが実行されるなど、同名の異なるプログラムが意図せず実行される危険もある。

なお、 envは/usr/binに置いてあることも/binに置いてあることもあるが、/usr/bin/envと書いても/bin/envと書いても実行されることを保証するため、[シンボリックリンクを張るなどして解決してあることが多い](../Page/ソフトリンク.md "wikilink")。

## 外部リンク

  - [公式GNU envマニュアル](https://www.gnu.org/software/coreutils/manual/coreutils.html#env-invocation)（英語）
  - [Manpage of ENV](https://linuxjm.osdn.jp/html/GNU_sh-utils/man1/env.1.html)
  - [env(1)](https://www.unix.com/man-page/sunos/1/env) man page（SunOSリファレンスマニュアル）
  - [env(1)](https://nixdoc.net/man-pages/HP-UX/man1/env.1.html) man page（HP-UXリファレンス）

[Category:標準UNIXプログラム](https://ja.wikipedia.org/wiki/Category:標準UNIXプログラム "wikilink")
> この記事は[Gnulib](https://ja.wikipedia.org/wiki/Gnulib)から翻訳されています。


**Gnulib**（グニューリブ）とは、基本的な[関数を提供する](../Page/サブルーチン.md "wikilink")[ソースコード](../Page/ソースコード.md "wikilink")[ライブラリ](../Page/ライブラリ.md "wikilink")である。現時点では、30以上のパッケージを提供している。本ライブラリの目的は、[プログラムの移植を容易にすることと](../Page/プログラム_\(コンピュータ\).md "wikilink")、[アプリケーション](https://ja.wikipedia.org/wiki/アプリケーション "wikilink")コードを複数[プラットフォーム間で共有できるようにすることにある](../Page/プラットフォーム_\(コンピューティング\).md "wikilink")。これは特に、[UNIX](../Page/UNIX.md "wikilink")上のアプリケーションを、[Windows](https://ja.wikipedia.org/wiki/Windows "wikilink")に移植する場合に効果を発揮する。

古典的なライブラリの場合、[バイナリ](../Page/バイナリ.md "wikilink")オブジェクトコードで[インストール](../Page/インストール.md "wikilink")されている。しかし、Gnulibは、異なりソースコードライブラリとして提供される。このためGnulibを取り込むパッケージは、Gnulibを取り込んだ形で出荷する必要がある。このため、gnulib-toolというスクリプトを用いて、パッケージをカスタマイズする必要がある。

また、本パッケージは、autoconfのスクリプトconfigure.acからgl_xxとして、呼び出し設定をすることが可能である。

また、版数という概念がこのソフトウェアには無い。このため、必要に応じて各パッケージのメンテナーはGnulibから最新のコードを取得する必要がある。

## 関連項目

  - [Autotools](../Page/Autotools.md "wikilink")
  - [Gnulibのホームページ](http://www.gnu.org/software/gnulib/)

## 外部リンク(Gnulibを取り込んだパッケージ)

[the virtualization API](http://libvirt.org/)

[Category:API](https://ja.wikipedia.org/wiki/Category:API "wikilink") [Category:GNUプロジェクト](https://ja.wikipedia.org/wiki/Category:GNUプロジェクト "wikilink") [Category:オープンソースソフトウェア](https://ja.wikipedia.org/wiki/Category:オープンソースソフトウェア "wikilink") [Category:ライブラリ_(プログラミング)](https://ja.wikipedia.org/wiki/Category:ライブラリ_\(プログラミング\) "wikilink")
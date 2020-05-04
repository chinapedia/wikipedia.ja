> この記事は[GNU Guix](https://ja.wikipedia.org/wiki/GNU_Guix)から翻訳されています。


**GNU Guix**は、クロスプラットフォームのパッケージマネージャで、インスタンス生成とOSの管理を[UNIX系](https://ja.wikipedia.org/wiki/UNIX系 "wikilink")でするためのツールでもある。[Guile](https://ja.wikipedia.org/wiki/Guile "wikilink")スキーム[APIを持つNixパッケージマネージャに基き](../Page/アプリケーションプログラミングインタフェース.md "wikilink")、完全に[フリーソフトウェア](../Page/フリーソフトウェア.md "wikilink")である\[1\]。伝統的なパッケージマネージャと異なり、GuixはNixのように、ソフトウェアは[ハッシュ](https://ja.wikipedia.org/wiki/ハッシュ "wikilink")によって生成された単一のディレクトリにインストールされるという、純粋に関数的なデプロイのモデルを利用している。それぞれのソフトウェアの依存関係はそれぞれのハッシュに含まれており、依存地獄の問題を解決する\[2\]。このパッケージ管理に対するアプローチは、より信頼性があり、再生産的で、ポータブルなパッケージを生成することを約束する\[3\] 。

GNU Guixの開発は、Guixシステムの開発と絡み合っており、これは完全にインストール可能なGNUシステムで[Linux-libre](https://ja.wikipedia.org/wiki/Linux-libre "wikilink")カーネルとGNU Shephered [init](https://ja.wikipedia.org/wiki/init "wikilink")システムを用いている\[4\]。

Guixのロールバック機能は、Nixの設計によるもので、これは[Debian](../Page/Debian.md "wikilink")、[Arch Linux](https://ja.wikipedia.org/wiki/Arch_Linux "wikilink")、[Fedora](../Page/Fedora.md "wikilink")、[CentOS](../Page/CentOS.md "wikilink")、[openSUSE](https://ja.wikipedia.org/wiki/openSUSE "wikilink")とそれぞれの派生物には見られないものである。

プロジェクトは、ボランティアチームにより[インターネット](../Page/インターネット.md "wikilink")を通じて管理されており、これはメンバーとともに[フランス](https://ja.wikipedia.org/wiki/フランス "wikilink")の[非営利組織](https://ja.wikipedia.org/wiki/非営利組織 "wikilink")Guix Europeに組み込まれている\[5\]。

## 特徴

以下の特徴はGuixのパッケージ管理機能に関連している。下記のGuixシステムの特徴を参照のこと。

### ストア

Nixの設計を引き継ぎ、パッケージマネージャの内容の大部分は、/gnu/storeディレクトリに保存されている。このディレクトリは、Guixデーモンのみに書き込み許可権限がある。

#### ガーベジコレクション

GuixはNixのように、組み込まれたガーベジコレクション機能を持っており、これは*dead*状態のストアのアイテムを*live*状態に保つのに役立つ\[6\].。

### プロファイル

Guixのパッケージは、プロファイル生成を使っており、これはストアアイテムを集め、ユーザが何をインストールしたかを特定するシムリンクの集合である。パッケージがインストール、削除されるたびに毎回、新しい生成が構築される。

### ロールバック

Guixのパッケージは、シムリンクをより早い時期のプロファイル生成に変更することを通じて以前のプロファイル生成に手軽にロールバックすることを可能にする\[7\]。

### 環境

Guixの環境は、ユーザーに複数のプロジェクトの依存でデフォルトのプロファイルに問題を起こされることなく、[ソフトウェア開発](../Page/ソフトウェア開発.md "wikilink")に必要なパッケージを含む環境に入ることを可能にする\[8\]。

### パック

Guix packは、ユーザにストアアイテムを複数同時に束ねることを可能にし、[Docker](https://ja.wikipedia.org/wiki/Docker "wikilink")[バイナリ](../Page/バイナリ.md "wikilink")のイメージや、再配置可能なtarball、[squashfs](https://ja.wikipedia.org/wiki/squashfs "wikilink")バイナリなどに出力することを可能にする\[9\]。

### グラフ

Guix packは、ユーザにパッケージとその依存関係の異なった[グラフ](https://ja.wikipedia.org/wiki/グラフ "wikilink")を見ることを可能にする\[10\]。

## Guix System Distribution

*Guix System*（以前は*GuixSD*と呼ばれていた）は、[Linuxディストリビューション](../Page/Linuxディストリビューション.md "wikilink")で、GNU Guixパッケージマネージャを用いて構築されている\[11\]。このディストリビューションは、宣言的なOSの設定\[12\]を可能にし、また容易にロールバックできる信頼性のあるシステムをも可能にしている\[13\]。システムは、[GNU Hurdカーネルの開発中のサポートと共に](../Page/GNU_Hurd.md "wikilink")、[Linux-libre](https://ja.wikipedia.org/wiki/Linux-libre "wikilink")カーネルを使っている。[2015年](../Page/2015年.md "wikilink")[2月3日](../Page/2月3日.md "wikilink")、このディストリビューションは[FSF](https://ja.wikipedia.org/wiki/FSF "wikilink")のフリーなLinuxディストリビューションのリストに加えられた\[14\]。

### アーキテクチャのサポート

[IA-32](../Page/IA-32.md "wikilink")、[x64](https://ja.wikipedia.org/wiki/x64 "wikilink")、AArch32/64がサポートされており\[15\]、また[2019年](../Page/2019年.md "wikilink")4月には[POWER9](https://ja.wikipedia.org/wiki/POWER9 "wikilink")のサポートのための作業が進行中である\[16\]。

### 機能

#### システムサービス

システムサービスは、Guixシステムの核となる機能で、ユーザに宣言的なデーモンとバックグランドサービスの設定の構成と容易に適切な設定を定義することを可能にする。

### GNU Shephred Init system

Guixシステムは、GNU Shepherdデーモンを[init](https://ja.wikipedia.org/wiki/init "wikilink")システムとして使っており、Guixの開発と乗り合せで行われ、またこのデーモンは[Guile](https://ja.wikipedia.org/wiki/Guile "wikilink")で書かれている。これあ以前"dmd"（"Daemon managing Daemons"または"Daemons-managing Daemon"）として知られていたが、Digital Marsの[D](../Page/D言語.md "wikilink")[コンパイラ](../Page/コンパイラ.md "wikilink")との名前の競合を避けるために名称が変更された\[17\]。

### リリースと安定性

最新のGuixシステムは、不安定版の開発[Git](../Page/Git.md "wikilink")レポジトリにのみあり\[18\]、これはGuixによって共有されているが、チャンネル機能を使うことで、ユーザや組織は安定版のリリースチャンネルにすることも可能である\[19\]。

## 歴史

[GNUプロジェクト](../Page/GNUプロジェクト.md "wikilink")は、[2012年](../Page/2012年.md "wikilink")11月にGNU Guixの最初のリリースを宣言した。これはNixをベースとした機能的なパッケージマネージャで、GuileスキームAPIを提供していた\[20\]。プロジェクトはGNU GuileのLudovic Courtèsによって[2012年](../Page/2012年.md "wikilink")6月にスタートされた\[21\]。[2015年](../Page/2015年.md "wikilink")[8月20日](https://ja.wikipedia.org/wiki/8月20日 "wikilink")には、Guixが[GNU Hurdに移植されたことが宣言された](../Page/GNU_Hurd.md "wikilink")\[22\]。

## 関連項目

  - [Debian GNU/Hurd](https://ja.wikipedia.org/wiki/Debian_GNU/Hurd "wikilink")

## 脚注

### 出典

## 外部リンク

  -
  - [Guixパッケージのリスト](https://www.gnu.org/software/guix/packages)

[Category:GNUプロジェクト](https://ja.wikipedia.org/wiki/Category:GNUプロジェクト "wikilink") [Category:フリーパッケージ管理システム](https://ja.wikipedia.org/wiki/Category:フリーパッケージ管理システム "wikilink")

1.  [Functional Package Management with Guix](https://en.wikisource.org/wiki/Functional_Package_Management_with_Guix)
2.  Prins, P., Suresh, J. and Dolstra, E., ["Nix fixes dependency hell on all Linux distributions,"](http://www.linux.com/feature/155922) [linux.com](https://ja.wikipedia.org/wiki/linux.com "wikilink"), December 22, 2008
3.  Dolstra, E. [*The Purely Functional Software Deployment Model.*](https://nixos.org/~eelco/pubs/phd-thesis.pdf) PhD thesis, Faculty of Science, Utrecht, The Netherlands. January 2006. .
4.  [Programming Interface (GNU Guix Reference Manual)](https://www.gnu.org/software/guix/manual/en/html_node/Programming-Interface.html)
5.
6.
7.
8.
9.
10.
11.
12.
13.
14.
15.
16.
17.
18.
19.
20.
21.
22.
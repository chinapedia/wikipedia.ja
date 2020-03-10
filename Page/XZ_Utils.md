> この記事は[XZ Utils](https://ja.wikipedia.org/wiki/XZ_Utils)から翻訳されています。


**XZ Utils**（以前の**LZMA Utils**）は[フリーな](../Page/フリーソフトウェア.md "wikilink")[コマンドライン](https://ja.wikipedia.org/wiki/コマンドライン "wikilink")[可逆圧縮](../Page/可逆圧縮.md "wikilink")ソフトウェアのセットであり、[LZMAと](../Page/Lempel-Ziv-Markov_chain-Algorithm.md "wikilink")[xzを含んでいる](https://ja.wikipedia.org/wiki/xz_\(ファイルフォーマット\) "wikilink")。[Unix系](../Page/Unix系.md "wikilink")オペレーティングシステムおよび、バージョン5.0以降の[Microsoft Windowsに対応している](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")。

xzは[gzip](https://ja.wikipedia.org/wiki/gzip "wikilink")と[bzip2](https://ja.wikipedia.org/wiki/bzip2 "wikilink")のような代替ソフトウェアよりもより高い圧縮率になる。 伸長速度はbzip2より速いが、gzipよりも遅い。圧縮はgzipよりもだいぶ遅くなることがあり、高圧縮ではbzip2よりも遅い。圧縮されたファイルが多くの回数使われるときに最も有用となる。\[1\]\[2\]

XZ Utilsは大まかに2つの構成要素からなる。

  - **xz**。コマンドラインの圧縮・伸長ソフトウェア（[gzip](https://ja.wikipedia.org/wiki/gzip "wikilink")に類似している）
  - **liblzma**。[zlib](https://ja.wikipedia.org/wiki/zlib "wikilink")に似た[APIを持つ](../Page/アプリケーションプログラミングインタフェース.md "wikilink")[ライブラリ](../Page/ライブラリ.md "wikilink")

様々なコマンドラインのショートカットがある。例えば**lzma**（**xz --format=lzma**）、**unxz**（**xz --decompress**。[gunzipに類似している](https://ja.wikipedia.org/wiki/gzip "wikilink")）、そして**xzcat**（**unxz --stdout**。[zcatに類似している](https://ja.wikipedia.org/wiki/gzip "wikilink")）。

XZ Utilsは*xz*と*lzma*ファイル形式の両方を圧縮・伸長できるが、LZMA形式は今や[レガシー](https://ja.wikipedia.org/wiki/レガシーシステム "wikilink")\[3\]であるため、 XZ Utilsはxz形式をデフォルトとして圧縮する。

## 実装

ファイル形式の性質と同じようにソフトウェアの振る舞いもまた、Unix圧縮ツールの[gzip](https://ja.wikipedia.org/wiki/gzip "wikilink")と[bzip2](https://ja.wikipedia.org/wiki/bzip2 "wikilink")に似た動作になるように設計されている。これは[Igor PavlovのLZMA](../Page/7-Zip.md "wikilink")-[SDKのUnix移植版から構成されており](../Page/ソフトウェア開発キット.md "wikilink")、Unix環境とその通常の構造と振る舞いに対してシームレスに組み込むためになじむようにされている。

xzは2014年のバージョン5.2.0以降、\[4\]マルチスレッド圧縮をサポートしている（`-T`フラグ）。\[5\]2019年時点ではスレッド化された伸長はまだ実装されていない。\[6\]ファイルがスレッドに対して与えられた設定よりも十分に大きくはないか、あるいは使用しているスレッドがメモリ使用制限を超過しているならば、定義されているよりも少ないスレッド数になることがありうる。\[7\]

ちょうどgzipとbzipのように、xzとlzmaは入力として単一のファイル（またはデータストリーム）を圧縮することしかできない。複数のファイルを単一の[アーカイブへ束ねることはできない](../Page/アーカイブ_\(コンピュータ\).md "wikilink")。それをするためには、最初に[tar](https://ja.wikipedia.org/wiki/tar "wikilink")のようなアーカイブするプログラムを使用する。

アーカイブを圧縮する:

`xz   my_archive.tar    # 結果はmy_archive.tar.xzへ`
`lzma my_archive.tar    # 結果はmy_archive.tar.lzmaへ`

アーカイブを伸長する:

`unxz    my_archive.tar.xz      # 結果はmy_archive.tarへ`
`unlzma  my_archive.tar.lzma    # 結果はmy_archive.tarへ`

tarの[GNU](../Page/GNU.md "wikilink")実装のバージョン1.22以降ではtarballのlzmaやxzへの透過的な圧縮をサポートしており、xz圧縮については`--xz`または`-J`、LZMA圧縮では`--lzma`が使用できる。

アーカイブを作成して圧縮する:

`tar -c --xz   -f my_archive.tar.xz   /some_directory    # 結果はmy_archive.tar.xzへ`
`tar -c --lzma -f my_archive.tar.lzma /some_directory    # 結果はmy_archive.tar.lzmaへ`

アーカイブを伸長してその内容を展開する:

`tar -x --xz   -f my_archive.tar.xz      # 結果は/some_directoryへ`
`tar -x --lzma -f my_archive.tar.lzma    # 結果は/some_directoryへ`

## 開発と採用

XZ Utilsの開発はTukaani Projectで行われている。Mike Keznerをリーダーとしてかつて[Slackware](../Page/Slackware.md "wikilink")をベースとした[Linuxディストリビューション](../Page/Linuxディストリビューション.md "wikilink")をメンテナンスしていた小さなグループだった。

**xz**と**liblzma**のすべての[ソースコード](../Page/ソースコード.md "wikilink")は[パブリックドメイン](../Page/パブリックドメイン.md "wikilink")でリリースされている。XZ Utilsソースコード配布物は、付加的に、複数の[GPLバージョンの対象となる](../Page/GNU_General_Public_License.md "wikilink")、いくつかのオプションスクリプトとサンプルプログラムを含んでいる。\[8\]

特に、配布されているXZ Utilsソフトウェアが含んでいる[GPLスクリプトとソースコードの一覧は以下のとおりである](../Page/GNU_General_Public_License.md "wikilink")。

  - 一般的なlibc関数であるのオプション実装（[GNU GPL v2と](https://ja.wikipedia.org/wiki/GNU_General_Public_License#Version_2 "wikilink")[GNU LGPL v2.1](../Page/GNU_Lesser_General_Public_License.md "wikilink")）
  - pthreadを検出するm4スクリプト（[GNU GPL v3](https://ja.wikipedia.org/wiki/GNU_General_Public_License#Version_3 "wikilink")）
  - いくつかの必須でないラッパースクリプト（xzgrepなど）（[GNU GPL v2](https://ja.wikipedia.org/wiki/GNU_General_Public_License#Version_2 "wikilink")）
  - そしてサンプルプログラムscanlzma。これはビルドシステムに統合されていない。

結果としてxzとliblzmaのバイナリはパブリックドメインだが、例外的にオプションのLGPL 実装は統合されていない。\[9\]

バイナリは[FreeBSD](../Page/FreeBSD.md "wikilink")、[Linux](../Page/Linux.md "wikilink")システム、[Microsoft Windows](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")、そして[FreeDOS](../Page/FreeDOS.md "wikilink")で利用できる。[Fedora](../Page/Fedora.md "wikilink")、[Slackware](../Page/Slackware.md "wikilink")、[Ubuntu](../Page/Ubuntu.md "wikilink")、そして[Debian](../Page/Debian.md "wikilink")を含む多くの[Linuxディストリビューション](../Page/Linuxディストリビューション.md "wikilink")がソフトウェアパッケージの圧縮にxzを使用している。[Arch Linuxは以前はパッケージの圧縮にxzを使用していたが](https://ja.wikipedia.org/wiki/Arch_Linux "wikilink")、\[10\]2019年12月27日以降は、パッケージは[Zstandard](https://ja.wikipedia.org/wiki/Zstandard "wikilink")で圧縮されている\[11\]。[GNU](../Page/GNU.md "wikilink")のFTPアーカイブもまたxzを使用している。

## 関連項目

## 参考文献

## 外部リンク

  - [Official Website](https://tukaani.org/xz/)
  - [SourceForge project page](https://sourceforge.net/projects/lzmautils/)

[Category:データ圧縮](https://ja.wikipedia.org/wiki/Category:データ圧縮 "wikilink") [Category:UNIXのソフトウェア](https://ja.wikipedia.org/wiki/Category:UNIXのソフトウェア "wikilink") [Category:オープンソースソフトウェア](https://ja.wikipedia.org/wiki/Category:オープンソースソフトウェア "wikilink")

1.
2.
3.
4.  <https://git.tukaani.org/?p=xz.git;a=blob;f=NEWS;hb=HEAD>
5.  <https://man.cx/xz>
6.  <https://man.cx/xz>
7.  <https://man.cx/xz>
8.
9.
10.
11.
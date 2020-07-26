> この記事は[Lempel-Ziv-Markov chain-Algorithm](https://ja.wikipedia.org/wiki/Lempel-Ziv-Markov_chain-Algorithm)から翻訳されています。


*[Lempel](https://ja.wikipedia.org/wiki/エイブラハム・レンペル "wikilink")-[Ziv](https://ja.wikipedia.org/wiki/ジェイコブ・ジヴ "wikilink")-[Markov chain](../Page/マルコフ連鎖.md "wikilink")-[Algorithm](../Page/アルゴリズム.md "wikilink")*（略して**LZMA**）は、[2001年](../Page/2001年.md "wikilink")から開発されている[データ圧縮](../Page/データ圧縮.md "wikilink")アルゴリズムで、[7-Zip](../Page/7-Zip.md "wikilink")アーカイバの[7z](../Page/7z.md "wikilink")フォーマットや[XZ Utilsの](../Page/XZ_Utils.md "wikilink")[xzフォーマットで使用されている](https://ja.wikipedia.org/wiki/xz_\(ファイルフォーマット\) "wikilink")。LZMAは、[LZ77](https://ja.wikipedia.org/wiki/LZ77 "wikilink")に少々類似したを使用し、通常[bzip2](https://ja.wikipedia.org/wiki/bzip2 "wikilink")以上の高い圧縮率と伸張速度、および最大4 [GBのサイズ可変な圧縮辞書を特徴とする](../Page/ギガバイト.md "wikilink")。

**LZMA2**は、圧縮されていないデータとLZMAデータの両方を含むことができ、複数の異なるLZMAエンコーディングパラメータを含むことができる単純なコンテナ形式である。 LZMA2は、任意にスケーラブルなマルチスレッドの圧縮と展開と、部分的に非圧縮データの効率的な圧縮をサポートする。

## 概要

LZMAは、改良[LZ77](https://ja.wikipedia.org/wiki/LZ77 "wikilink")圧縮アルゴリズムと、バックエンドにレンジコーダー（[Range Coder](https://ja.wikipedia.org/wiki/Range_Coder "wikilink")）を使用している。

辞書圧縮アルゴリズムは、巨大な辞書サイズと、繰り返し使用される一致距離の特別なサポートを持つ[LZ77](https://ja.wikipedia.org/wiki/LZ77 "wikilink")の変種を使用し、その出力はレンジコーダーで符号化され、複雑なモデルを使用して各ビットの確率予測を行う。 辞書圧縮で洗練された辞書データ構造を使用して一致列を見つけ、レンジコーダーにより一度に1ビットずつリテラルシンボルとフレーズリファレンスのストリームを生成する。

LZMAより前のほとんどのエンコーダモデルは純粋にバイトベースだった。 LZMAの主な革新は、一般的なバイトベースのモデルの代わりに、リテラルまたはフレーズの各表現のビットフィールドに固有のコンテキストを使用する。これは、一般的なバイトベースのモデルほど簡単だが、関連性のないビットを同じコンテキストで混在させないようにするためである。さらに、古典的な辞書圧縮（zipやgzip形式で使用されているものなど）と比べて、辞書のサイズは、現代のシステムで利用可能な大量のメモリを利用することができる。

### LZMA形式

LZMA圧縮では、圧縮ストリームは、適応バイナリレンジコーダを使用して符号化されたビットストリームである。 ストリームはパケットに分割され、各パケットは1バイトまたはLZ77シーケンスの長さと距離が暗黙的または明示的にエンコードされている。 各パケットの各部分は独立したコンテキストでモデル化されるので、各ビットの確率予測は、同じタイプの以前のパケットのそのビット（および同じフィールドからの関連ビット）の値と相関がある。

### LZMA2形式

LZMA2コンテナは、複数の圧縮LZMAデータと非圧縮データをサポートする。それぞれのLZMA圧縮されたラン（データの塊）は、異なるLZMA構成と辞書を持つことができる。これにより、部分的または完全な非圧縮ファイルの圧縮が改善され、並列に独立して圧縮または展開することができるようにファイルをランに分割しマルチスレッドで処理することが可能になる。

### xz形式と7z形式

LZMA2データを含むことができる[xz](https://ja.wikipedia.org/wiki/xz "wikilink")形式は*tukaani.org*\[1\]に記載されている。また、LZMAまたはLZMA2データを含むことができる.7zファイル形式は、LZMA SDK\[2\]に含まれる7zformat.txtファイルに記載されている。

## LZMA SDK

LZMAを圧縮・伸長するためのSDKが公開されている[1](http://sevenzip.sourceforge.jp/sdk.html)。 ドキュメント、サンプル、[ヘッダファイル](../Page/ヘッダファイル.md "wikilink")、[ソースコード](../Page/ソースコード.md "wikilink")などを含む。 ライセンスはバージョン4.62以降[パブリックドメイン](../Page/パブリックドメイン.md "wikilink")となった。 [C++](../Page/C++.md "wikilink")、[ANSI-C](../Page/C言語.md "wikilink")、[C\#](https://ja.wikipedia.org/wiki/C_sharp "wikilink")、[Java](https://ja.wikipedia.org/wiki/Java "wikilink")で実装されている。 伸長アルゴリズムは全ての[32ビット](../Page/32ビット.md "wikilink")[CPU](../Page/CPU.md "wikilink")で実装可能であり、制約をつければ[16ビット](../Page/16ビット.md "wikilink")CPUでも実装可能である。

### 速度

  - 圧縮速度 - 1GHzのCPUで0.5MB/s
  - 伸長速度 - 1GHzのPentium 3で8\~12MB/s。100MHzのARMで0.5\~1MB/s。

## 7-Zipリファレンス実装

LZMAのリファレンス実装は、[7z](../Page/7z.md "wikilink")や[7-Zip](../Page/7-Zip.md "wikilink")ツールセットの一部に含まれる。ソースコードは[GNU LGPLライセンスで配布されている](../Page/GNU_Lesser_General_Public_License.md "wikilink")。

[オープンソース](../Page/オープンソース.md "wikilink")のリファレンス実装であるLZMA圧縮[ライブラリ](../Page/ライブラリ.md "wikilink")は、 [C++](../Page/C++.md "wikilink")で記述されていて、以下の特性がある。

  - 圧縮速度: 2GHz [CPU](../Page/CPU.md "wikilink")で約1MB/[秒](../Page/秒.md "wikilink")
  - 伸長速度: 2GHz CPUで10\~20MB/秒
  - [マルチスレッドと](../Page/スレッド_\(コンピュータ\).md "wikilink")[Pentium 4マイクロプロセッサの](../Page/Pentium_4.md "wikilink")[ハイパースレッディング機能をサポート](../Page/ハイパースレッディング・テクノロジー.md "wikilink")

7-Zip実装には、[ハッシュチェイン](https://ja.wikipedia.org/wiki/ハッシュチェイン "wikilink")、[二分木](../Page/二分木.md "wikilink")、[基数木](../Page/基数木.md "wikilink")を辞書検索アルゴリズムの基礎とする、複数の変種がある。

LZMAの伸長専用コードは[C言語](../Page/C言語.md "wikilink")で記述されていて、通常5kB前後にコンパイルされる。また、伸長に必要なRAMの量は、主に圧縮時のスライド窓の大きさによって決定する。小さいコードサイズと、辞書を小さくすることにより比較的少量になるメモリ消費量は、LZMA伸長アルゴリズムをアプリケーションに[組み込むのに適するものとしている](../Page/組み込みシステム.md "wikilink")。

最近では、[XZ Embeddedとして](https://ja.wikipedia.org/wiki/XZ_Embedded "wikilink")、特に組み込みシステム向けに特化されたライブラリが提供されている。これは[Linuxカーネル](../Page/Linuxカーネル.md "wikilink")に統合する事を目的としているが、独自のシステムにも容易に組み込みが可能である。

### リファレンス実装の移植性

ソースコードには、広範囲で[Microsoft Windows特有の機能が使用され](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")、しかも分離されていない。このため、リファレンス実装が[フリーソフトウェア](../Page/フリーソフトウェア.md "wikilink")であるにもかかわらず、[UNIX](../Page/UNIX.md "wikilink")互換用バージョンが登場するまでに時間がかかった。

現在、[Unix系](../Page/Unix系.md "wikilink")プラットフォームで動く移植版が2つある:

  - [p7zip](http://sourceforge.net/projects/p7zip/)、これは[7-Zip](../Page/7-Zip.md "wikilink")の[7z](../Page/7z.md "wikilink")と[7za](https://ja.wikipedia.org/wiki/7za "wikilink")コマンドラインツールの移植版である。p7zipは、標準[7z](../Page/7z.md "wikilink")アーカイブストリームを生成する。これはLZMAに組み合せることができる追加フィルタで使用されている。フィルタは、たとえば、実行ファイルのジャンプやサブルーチン呼び出し命令の相対アドレス前処理などである。
  - [LZMA Utils](http://tukaani.org/lzma/)、これはLZMAコード*だけ*からなる移植版である。これは生のLZMAストリームを、[gzip](https://ja.wikipedia.org/wiki/gzip "wikilink")や[bzip2](https://ja.wikipedia.org/wiki/bzip2 "wikilink")圧縮ユーティリティと同様に扱えるように設計されている。`lzma`ツールで、[.tar](https://ja.wikipedia.org/wiki/.tar "wikilink")のように複数のファイルをアーカイブできる。出力は、ヘッダ情報のない生のLZMAである。現在ではXZ Utilsがメインストリームとなり、LZMA Utilsの開発は終息している。
  - [XZ Embedded](http://tukaani.org/xz/embedded.html)、XZ Utilsの伸張コードだけを抜き出して整理したライブラリで、主に[Linux](../Page/Linux.md "wikilink")カーネルのブート時に使用する前提で設計されている。但し、他の独自のシステムにも容易に移植可能となっている。

注意：7-ZipとLZMAで生成されるLZMAストリームは異なる。つまり非互換である。基本的に、一方のツールで生成したファイルはもう一方で扱うことはできない。ただし7-Zipはバージョン4.58でLZMAストリームの伸張をサポートした。7-Zipは非圧縮時のファイルサイズを含む[64ビット](../Page/64ビット.md "wikilink")ヘッダエントリを付加するが、LZMA Utilsではこれがない。

## 関連ソフトウェア

LZMAを使用するか、サポートするソフトウェア。

  - [GNU Tar](../Page/Tar.md "wikilink") … version 1.20 以降は "--lzma" オプションによりLZMAをサポートした。
  - [Nullsoft Scriptable Install System](https://ja.wikipedia.org/wiki/Nullsoft_Scriptable_Install_System "wikilink")
  - [Inno Setup](https://ja.wikipedia.org/wiki/Inno_Setup "wikilink")
  - パッチを適用した[cramfs](https://ja.wikipedia.org/wiki/cramfs "wikilink")や[SquashFS](https://ja.wikipedia.org/wiki/SquashFS "wikilink")
  - [lrzip](http://ck.kolivas.org/apps/lrzip/) （"long range zip"または"LZMA [rzip](https://ja.wikipedia.org/wiki/rzip "wikilink")"）
  - [PyLZMA](http://www.joachim-bauch.de/projects/python/pylzma)、Igor PavlovのLZMA SDKへの[Python](../Page/Python.md "wikilink")インタフェース
  - [FreeArc](http://freearc.narod.ru/)、LZMA SDKへのアーカイバと[Haskell](../Page/Haskell.md "wikilink")インタフェース
  - [Pascal LZMA SDK](http://www.birtles.org.uk/programming/) - [Pascal](../Page/Pascal.md "wikilink")への移植
  - [UPX](https://ja.wikipedia.org/wiki/UPX "wikilink")
  - [lzip](https://ja.wikipedia.org/wiki/lzip "wikilink")

## 参照

## 外部リンク

  - [7-Zip](http://www.7-zip.org/)ホームページ
  - [7-Zip 日本語](http://sevenzip.sourceforge.jp/)ホームページ
  - [p7zip](http://p7zip.sourceforge.net/)ホームページ
  - [PyLZMA](http://www.joachim-bauch.de/projects/python/pylzma)ホームページ

[Category:データ圧縮](https://ja.wikipedia.org/wiki/Category:データ圧縮 "wikilink")

1.
2.
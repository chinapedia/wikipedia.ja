> この記事は[Rsync](https://ja.wikipedia.org/wiki/Rsync)から翻訳されています。


**rsync** は、[UNIX](../Page/UNIX.md "wikilink")システムにおいて、[差分符号化](https://ja.wikipedia.org/wiki/差分符号化 "wikilink")を使って[データ](../Page/データ.md "wikilink")転送量を最小化し、遠隔地間の[ファイルや](https://ja.wikipedia.org/wiki/ファイル_\(コンピュータ\) "wikilink")[ディレクトリ](../Page/ディレクトリ.md "wikilink")の[同期を行う](https://ja.wikipedia.org/wiki/ファイル同期 "wikilink")[アプリケーションソフトウェア](../Page/アプリケーションソフトウェア.md "wikilink")である。類似のプログラムやプロトコルにはない rsync 独自の特徴として、[ミラーサイト](https://ja.wikipedia.org/wiki/ミラーサイト "wikilink")との転送が双方向に高々1回で済む点がある。rsync はディレクトリ内容を表示し、ディレクトリやファイルをコピーできる。オプションで[データ圧縮](../Page/データ圧縮.md "wikilink")や[再帰も指定可能](https://ja.wikipedia.org/wiki/再帰呼び出し "wikilink")。

rsync プロトコルの[デーモン](https://ja.wikipedia.org/wiki/デーモン_\(ソフトウェア\) "wikilink") rsyncd がデフォルトで使う[TCP](../Page/Transmission_Control_Protocol.md "wikilink")[ポート番号](https://ja.wikipedia.org/wiki/ポート番号 "wikilink")は 873 である。rsync はローカルなディレクトリ間の同期にも使えるし、[RSHや](../Page/リモートシェル.md "wikilink")[SSHなどのリモートシェル経由でも使える](../Page/Secure_Shell.md "wikilink")。後者の場合、rsync のクライアントプログラムはローカルとリモートの両方にインストールされている必要がある。

[GNU General Public License](../Page/GNU_General_Public_License.md "wikilink") でリリースされており、[フリーソフトウェア](../Page/フリーソフトウェア.md "wikilink")である。

## アルゴリズム

rsync は、転送先のコンピュータが何らかの構造体（ファイルなど）の別バージョンを既に持っている場合、その構造体を効率的に転送する[アルゴリズム](../Page/アルゴリズム.md "wikilink")を使っている。このアルゴリズムは、[オーストラリア](../Page/オーストラリア.md "wikilink")のプログラマ[アンドリュー・トリジェル](https://ja.wikipedia.org/wiki/アンドリュー・トリジェル "wikilink")が発明した。

受信側は、そのファイルの[複写](https://ja.wikipedia.org/wiki/複写 "wikilink")を固定長のチャンク（塊）に重ならないように分割し、チャンクごとに2つの[チェックサム](../Page/チェックサム.md "wikilink")を計算する。この分割長を \(S\) とする。チェックサムは、[MD4](https://ja.wikipedia.org/wiki/MD4 "wikilink") [ハッシュ関数](../Page/ハッシュ関数.md "wikilink")と弱いローリングチェックサムである。受信側は送信側に対して、それらチェックサムを送る。

送信側は、自身の持つバージョンのファイルについて、長さ \(S\) の各チャンクごとにローリングチェックサムを計算する。このときチャンクは重なるものも含めて計算する。重なりのあるチャンクについてのローリングチェックサムの計算は効率的にできる。[バイト位置](../Page/バイト_\(情報\).md "wikilink") \(n\) から \(n+S-1\) までのローリングチェックサムが \(R\) であったとき、\(n+1\) から \(n+S\) までのローリングチェックサムは、\(R\) と \(n\) 番目のバイトの内容、\(n+S\) 番目のバイトの内容だけから計算でき、全バイトの内容を調べる必要がない。したがって、1 バイト目から 25 バイト目までのローリングチェックサムを既に計算していた場合、2 バイト目から 26 バイト目までのローリングチェックサムは、単に 1 バイト目と 26 バイト目の値がわかれば計算できる。

rsync で使われている[ローリングチェックサムは](https://ja.wikipedia.org/wiki/ローリングハッシュ "wikilink")[マーク・アドラー](https://ja.wikipedia.org/wiki/マーク・アドラー "wikilink")(Mark Adler)の [adler-32](https://ja.wikipedia.org/wiki/adler-32 "wikilink") チェックサムに基づいている。adler-32 は、[フレッチャーのチェックサム](https://ja.wikipedia.org/wiki/フレッチャーのチェックサム "wikilink")に基づいており、[zlib](https://ja.wikipedia.org/wiki/zlib "wikilink") でも使われている。

次に送信側は受信側が送ってきたチェックサムと一致するものがあるかを調べる。一致する場合、その位置について MD4 チェックサムを計算し、受信側が送ってきた MD4 の値と比較する。

一致が見つけられない場合、送信側は自身の持つファイルの部分にマージのための手順を付けて受信側に送信し、ファイル内容が全く同じになるようにする。

送信側と受信側のファイルの内容が多くの部分で一致する場合、同期のために転送が必要となるデータ量は少なくなる。

rsync のこのようなアルゴリズムはアプリケーションとしての rsync の中核であり、2つのコンピュータ間での TCP/IP 上の転送量を最適化するものである。rsync は他にもデータ転送やバックアップに役立つ機能を備えている。

  - zlib を使ったブロック単位の圧縮/伸張
  - [ssh](../Page/Secure_Shell.md "wikilink") や [stunnel](https://ja.wikipedia.org/wiki/stunnel "wikilink") などのプロトコルをサポートし、暗号化が可能

## 利用

初期の利用形態は、UNIXシステム群のうちの1台をサーバとし、他のシステムとの間で[ミラーリング](https://ja.wikipedia.org/wiki/ミラーリング "wikilink")や[バックアップ](https://ja.wikipedia.org/wiki/バックアップ "wikilink")を行うものであった。[cronのようなスケジューリング機構を使えば](https://ja.wikipedia.org/wiki/crontab "wikilink")、自動スケジューリングされ暗号化された複数台の同時ミラーリングが可能である。

## 派生

**rdiff** は、rsync のアルゴリズムを使ってファイル A からファイル B への[差分ファイルを生成するものである](https://ja.wikipedia.org/wiki/差分符号化 "wikilink")（[diff](https://ja.wikipedia.org/wiki/diff "wikilink") に似ているが、出力形式が異なる）。その差分ファイルをファイル A に適用すると、それをファイル B に変換できる（[patch](https://ja.wikipedia.org/wiki/patch "wikilink") に類似）。

diff とは異なり、差分ファイル生成過程は2段階に分かれる。まず、ファイル A からより小さいシグネチャファイルを生成し、次にそのシグネチャファイルとファイル B から差分ファイルを生成する。また、diff とは異なり、rdiff は[バイナリファイル](https://ja.wikipedia.org/wiki/バイナリファイル "wikilink")にも適用可能である。

rdiff を使って、**rdiff-backup** というユーティリティも作られている。これはファイルやディレクトリの[バックアップ](https://ja.wikipedia.org/wiki/バックアップ "wikilink")をネットワーク経由で保守できるものである。rdiff-backup はバックアップと共に rdiff の差分ファイル群を保持しているので、任意の時点のバックアップが可能である。

rdiff-backup からの派生として Duplicity がある。事前に各ブロックのハッシュを生成して暗号化しておき、サーバ上にそれらを格納しておく。[増分バックアップ](https://ja.wikipedia.org/wiki/増分バックアップ "wikilink")に際しては、サーバ上の暗号化されたハッシュを利用する。データの残りも暗号化されて記憶される。

## 歴史

rsync は[1996年](../Page/1996年.md "wikilink")[6月19日](../Page/6月19日.md "wikilink")に発表された\[1\]。オリジナルの作者は[アンドリュー・トリジェル](https://ja.wikipedia.org/wiki/アンドリュー・トリジェル "wikilink")と Paul Mackerras であった。

## 関連項目

  - [CVSup](https://ja.wikipedia.org/wiki/CVSup "wikilink")
  - [Unison](https://ja.wikipedia.org/wiki/Unison "wikilink")
  - [xdelta](https://ja.wikipedia.org/wiki/xdelta "wikilink")
  - [Jigdo](https://ja.wikipedia.org/wiki/Jigdo "wikilink")

## 脚注

## 外部リンク

  - [rsync 公式サイト](https://rsync.samba.org)
  - [rsync algorithm](https://rsync.samba.org/tech_report/)
  - [Andrew Tridgell's PHD on rsync](https://samba.org/~tridge/phd_thesis.pdf)

[Category:ネットワークソフト](https://ja.wikipedia.org/wiki/Category:ネットワークソフト "wikilink") [Category:UNIXのソフトウェア](https://ja.wikipedia.org/wiki/Category:UNIXのソフトウェア "wikilink") [Category:ファイル転送プロトコル](https://ja.wikipedia.org/wiki/Category:ファイル転送プロトコル "wikilink") [Category:1996年のソフトウェア](https://ja.wikipedia.org/wiki/Category:1996年のソフトウェア "wikilink") [Category:オープンソースソフトウェア](https://ja.wikipedia.org/wiki/Category:オープンソースソフトウェア "wikilink")

1.  [First release of rsync - rcp replacement](http://groups.google.com/group/comp.os.linux.announce/msg/3bb93f6484065f20) [1996年](../Page/1996年.md "wikilink")[6月19日](../Page/6月19日.md "wikilink")
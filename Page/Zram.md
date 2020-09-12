> この記事は[Zram](https://ja.wikipedia.org/wiki/Zram)から翻訳されています。


**zram**は、以前は**compcache**と呼ばれた、RAMに圧縮ブロックデバイスを作成する[Linuxカーネルモジュールで](https://ja.wikipedia.org/wiki/ローダブル・カーネル・モジュール "wikilink")、いわゆる[RAMディスク](../Page/RAMディスク.md "wikilink")であるが、中間ファイル出力をしないオンザフライでの「ディスク」の圧縮である。 zramで作成されたブロックデバイスは、スワップまたは汎用RAMディスクとして使用できる。 zramの最も一般的な2つの使用法は、一時ファイル（/ tmp）用ストレージと、スワップ「ディスク」である。 当初、zramには後者の機能しかなかったため、元の名前は「compcache」（「圧縮キャッシュ」）だった。

Linuxのドライバーステージング領域で4年の歳月を経て、2014年3月30日にリリースされたバージョン3.14で、zramはメインラインのLinuxカーネルに導入された。 \[1\] Linuxカーネルバージョン3.15以降（2014年6月8日リリース）以降、zramは複数の圧縮ストリームと複数の[圧縮アルゴリズムをサポートしている](../Page/データ圧縮.md "wikilink")。 圧縮アルゴリズムには、 [LZ4](https://ja.wikipedia.org/wiki/LZ4 "wikilink") 、 [LZO](https://ja.wikipedia.org/wiki/Lempel-Ziv-Oberhumer "wikilink") 、 [ZSTD](https://ja.wikipedia.org/wiki/Zstandard "wikilink") 、 842、およびそれらの修正が含まれる。 デフォルトは「LZO-RLE」で、速度と比率のバランスが非常に良い。 他のほとんどのシステムパラメータと同様に、圧縮アルゴリズムは[sysfs](https://ja.wikipedia.org/wiki/sysfs "wikilink")を介して選択できる。 \[2\]

圧縮スワップ空間として使用される場合、zramはzswapに似ていて、汎用RAMディスクではなく、スワップページ用のカーネル内圧縮キャッシュである。 `CONFIG_ZRAM_WRITEBACK`が導入されるまで 、zswapとは異なり、zramはハードディスクをバッキングストアとして使用できなかった。つまり、使用頻度の低いページをディスクに移動できない。 一方、zswapではバッキングストアが必要だが、zramでは必要ない。

zramをスワップに使用する場合、zswapと同様に、Linuxにとっては、RAMを効率的に使えるようになる。OSにとっては、同じ量のRAMをアプリケーションメモリやディスクキャッシュとして使うのに比べて、メモリページを圧縮スワップの中に保持する方がより多くのメモリのページを保持できる。これは、メモリが少ないマシンで特に効果的である。\[3\] \[4\] 2012年、UbuntuはRAMが小さいコンピューターでzramをデフォルトで有効にすることを簡単に検討した。 \[5\]

zram / zswapを使用した圧縮スワップスペースは、 [組み込みデバイスや](../Page/組み込みシステム.md "wikilink")[ネットブック](https://ja.wikipedia.org/wiki/ネットブック "wikilink")などのローエンドハードウェアデバイスにもメリットをもたらす。 このようなデバイスは、通常、 フラッシュベースストレージを使用していますが、これは[ライトアンプリフィケーション](https://ja.wikipedia.org/wiki/ライトアンプリフィケーション "wikilink")によって寿命が限られていますし、[スワップ領域を提供するためにも使われます](../Page/ページング方式.md "wikilink")。 zramをスワップとして使うと、そのようなフラッシュベースのストレージにかかる摩耗の量を効果的に削減し、その結果、使用可能な寿命を延ばします。 また、zramを使用すると、スワッピングを必要とするLinuxシステムの[I / Oが大幅に削減されます](../Page/入出力.md "wikilink")。 \[6\] \[7\]

2013年以降、Googleの[Chrome OSはデフォルトでzramを使用しています](https://ja.wikipedia.org/wiki/Google_Chrome_OS "wikilink")。\[8\] [Androidには](../Page/Android_\(オペレーティングシステム\).md "wikilink")、バージョン4.4以降のzramが含まれています。 \[9\] [Lubuntu](https://ja.wikipedia.org/wiki/Lubuntu "wikilink")は、バージョン13.10でzramの使用も開始しました。 \[10\]

## こちらもご覧ください

  - [Linuxスワップ](../Page/ページング方式.md "wikilink")
  - [Swap partions on SSD](https://ja.wikipedia.org/wiki/:en:Solid-state_drive#SWAP "wikilink")
  - [zswap](https://ja.wikipedia.org/wiki/zswap "wikilink")

## 参考文献

## 外部リンク

  - [zram](https://www.kernel.org/doc/Documentation/blockdev/zram.txt) Linuxカーネルのドキュメント
  - [Linux用のCompcache、Compressed Caching](https://code.google.com/p/compcache/)
  - [Compcache：インメモリ圧縮スワッピング](https://lwn.net/Articles/334649/) 、2009年5月26日、LWN.net、Nitin Gupta作
  - [カーネル内メモリ圧縮](https://lwn.net/Articles/545244/) 、2013年4月3日、LWN.net、Dan Magenheimer著
  - [圧縮キャッシュ：ハンドヘルドコンピュータの仮想メモリ圧縮](https://www.cs.princeton.edu/~mfreed//docs/6.033/compression.pdf) 、2000年3月16日、 Michael J. Freedman著

[Category:メモリ管理](https://ja.wikipedia.org/wiki/Category:メモリ管理 "wikilink")

1.
2.
3.
4.
5.
6.
7.
8.
9.  Google, [Android KitKat | Android Developers](https://developer.android.com/about/versions/kitkat.html).
10.